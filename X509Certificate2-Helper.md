## Assinatura com X509Certificate2

```c#
public static string Assinar(X509Certificate2 certificado, string xml)
{
    XmlDocument doc = new XmlDocument();
    doc.PreserveWhitespace = false;
    doc.LoadXml(xml);
    try
    {
        SignedXml signedXml = new SignedXml(doc);
        signedXml.SigningKey = certificado.PrivateKey;

        Reference reference = new Reference();
        reference.Uri = "";
        XmlDsigEnvelopedSignatureTransform env = new XmlDsigEnvelopedSignatureTransform();
        reference.AddTransform(env);

        XmlDsigC14NTransform xmlTransform = new XmlDsigC14NTransform();
        reference.AddTransform(xmlTransform);
        signedXml.AddReference(reference);

        KeyInfo keyInfo = new KeyInfo();
        keyInfo.AddClause(new KeyInfoX509Data(certificado));        
        signedXml.KeyInfo = keyInfo;
        signedXml.ComputeSignature();
        XmlElement xmlDigitalSignature = signedXml.GetXml();
        doc.DocumentElement.AppendChild(doc.ImportNode(xmlDigitalSignature, true));
        return doc.InnerXml;
    }
    catch (Exception ex)
    {
    	throw ex;
    }
}
```


## Recuperar Certificado com base na Chave

```c#
public static X509Certificate2 Certificado()
{   
    X509Certificate2 _X509Cert = new X509Certificate2();
    string _Certkey = "Chave do Certificado";
    try
    {
        X509Store store = new X509Store("MY", StoreLocation.LocalMachine);
        store.Open(OpenFlags.ReadOnly | OpenFlags.OpenExistingOnly);
        X509Certificate2Collection collection = (X509Certificate2Collection)store.Certificates;
        X509Certificate2Collection collection2 = (X509Certificate2Collection)collection.Find(X509FindType.FindByKeyUsage, X509KeyUsageFlags.DigitalSignature, false);
        for (int i = 0; i < collection.Count; i++)
        {
            if (String.Compare(collection[i].SerialNumber, _Certkey, true) == 0)
            {
                _X509Cert = (X509Certificate2)collection[i];
                store.Close();
                return _X509Cert;
            }
        }
        store.Close();
        throw new Exception(string.Format("{0} {1}", "Nenhum certificado válido encontrado para a chave informada: ", _Certkey));
    }
    catch (System.Exception ex)
    {
        throw ex;
    }
}

```


## Verificar a assinatura do arquivo xml


```c#
// Verificar Assinatura Desanexada
public static Boolean VerifyDetachedSignature(string XmlSigFileName)
{	
    // Create a new XML document.
    XmlDocument xmlDocument = new XmlDocument();

    // Load the passed XML file into the document.
    xmlDocument.Load(XmlSigFileName);

    // Create a new SignedXMl object.
    SignedXml signedXml = new SignedXml();

    // Find the "Signature" node and create a new
    // XmlNodeList object.
    XmlNodeList nodeList = xmlDocument.GetElementsByTagName("Signature");

    // Load the signature node.
    signedXml.LoadXml((XmlElement)nodeList[0]);

    // Check the signature and return the result.
    return signedXml.CheckSignature();
}
```


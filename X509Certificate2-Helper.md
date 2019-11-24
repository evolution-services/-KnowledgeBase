## Assinatura X509Certificate2

```c#
public static string AssinarXML(X509Certificate2 certificado, string xml)
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


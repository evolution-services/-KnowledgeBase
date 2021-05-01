##### XML WebConfig WebForms - Redirect Https by Default

```xml
<configuration>
 <system.webServer>
 <rewrite>
 <rules>
 <rule name="HTTPS force" enabled="true" stopProcessing="true">
 <match url="(.*)" />
 <conditions>
 <add input="{HTTPS}" pattern="^OFF$" />
 </conditions>
 <action type="Redirect" url="https://{HTTP_HOST}{REQUEST_URI}" redirectType="Permanent" />
 </rule>
 </rules>
 </rewrite>
 </system.webServer>
</configuration>
```

##### C(#)

```c#
Func<Func<int,int>,Func<int,int>> twice = f => x => f(f(x));
	Func<int,int> y = x => x + 3;
	Console.WriteLine(twice(y)(7)); // 13
}
```

##### Parcelamento com Coeficiente de Financiamento

```c#
using System;
					
public class Program
{
	public static void Main()
	{				
		// Formula: 
		
		PMT = [PV. (1 + i) ^ n] i / [(1 + i) ^ n - 1]
		
		// Valor financiado
		double PV = 200.44f;
		// Parcelas
		int n = 2;
		// Taxa mensal
		double i = 0.0888;
		// Prestação a descobrir.
		double PMT = 0;
		
		PMT = (PV * Math.Pow( (1+i) , n) * i) / ( Math.Pow((1 + i) , n) - 1 );
		
		PMT = (PV * Math.Pow((1+i) , n) * i) / ( Math.Pow((1 + i) , n) - 1 );
					
		
		Console.WriteLine("Valor da parcela:" + Math.Round(PMT ,2) );
		Console.WriteLine("Valor Total do financiamento:" + Math.Round( (PMT * n) , 2) );
		
	}
}
```

##### Format DateTime options

```C#
using System;				
public class Program
{
	public static void Main()
	{
		var dateStart = DateTime.Now;
		Console.WriteLine(dateStart.ToString("MM/dd/yyyy"));					// 05/29/2015
		Console.WriteLine(dateStart.ToString("dddd, dd MMMM yyyy"));				// Friday, 29 May 2015
		Console.WriteLine(dateStart.ToString("dddd, dd MMMM yyyy"));				// Friday, 29 May 2015 05:50
		Console.WriteLine(dateStart.ToString("dddd, dd MMMM yyyy"));				// Friday, 29 May 2015 05:50 AM
		Console.WriteLine(dateStart.ToString("dddd, dd MMMM yyyy"));				// Friday, 29 May 2015 5:50
		Console.WriteLine(dateStart.ToString("dddd, dd MMMM yyyy"));				// Friday, 29 May 2015 5:50 AM
		Console.WriteLine(dateStart.ToString("dddd, dd MMMM yyyy HH:mm:ss"));			// Friday, 29 May 2015 05:50:06
		Console.WriteLine(dateStart.ToString("MM/dd/yyyy HH:mm"));				// 05/29/2015 05:50
		Console.WriteLine(dateStart.ToString("MM/dd/yyyy hh:mm tt"));				// 05/29/2015 05:50 AM
		Console.WriteLine(dateStart.ToString("MM/dd/yyyy H:mm"));				// 05/29/2015 5:50
		Console.WriteLine(dateStart.ToString("MM/dd/yyyy h:mm tt"));				// 05/29/2015 5:50 AM
		Console.WriteLine(dateStart.ToString("MM/dd/yyyy HH:mm:ss"));				// 05/29/2015 05:50:06
		Console.WriteLine(dateStart.ToString("MMMM dd"));					// May 29
		Console.WriteLine(dateStart.ToString("yyyy’-‘MM’-‘dd’T’HH’:’mm’:’ss.fffffffK"));	// 2015-05-16T05:50:06.7199222-04:00
		Console.WriteLine(dateStart.ToString("ddd, dd MMM yyy HH’:’mm’:’ss ‘GMT’"));		// Fri, 16 May 2015 05:50:06 GMT
		Console.WriteLine(dateStart.ToString("yyyy’-‘MM’-‘dd’T’HH’:’mm’:’ss"));			// 2015-05-16T05:50:06
		Console.WriteLine(dateStart.ToString("HH:mm"));						// 05:50
		Console.WriteLine(dateStart.ToString("hh:mm tt"));					// 05:50 AM
		Console.WriteLine(dateStart.ToString("H:mm"));						// 5:50
		Console.WriteLine(dateStart.ToString("h:mm tt"));					// 5:50 AM
		Console.WriteLine(dateStart.ToString("HH:mm:ss"));					// 05:50:06
		Console.WriteLine(dateStart.ToString("yyyy MMMM"));					// 2015 May		
	}
}
```

##### Currency Format

```c#
using System;
using System.Globalization;					
public class Program
{
	public static void Main()
	{
		double amount = 999999999.99;
		Console.WriteLine(amount.ToString("N")); // Numeric format.			// 999,999,999.99
		Console.WriteLine(amount.ToString("C")); // Standard system format. 		// ¤999,999,999.99
		Console.WriteLine(amount.ToString("C", CultureInfo.GetCultureInfo("pt-br")));   // R$ 999.999.999,99
		Console.WriteLine(amount.ToString("C", CultureInfo.GetCultureInfo("en-au")));   // $999,999,999.99
		Console.WriteLine(amount.ToString("C", CultureInfo.GetCultureInfo("en-us")));   // $999,999,999.99
		Console.WriteLine(amount.ToString("C", CultureInfo.GetCultureInfo("en-ca")));   // $999,999,999.99		
		Console.WriteLine(amount.ToString("C", CultureInfo.GetCultureInfo("en-ie")));   // €999,999,999.99
		Console.WriteLine(amount.ToString("C", CultureInfo.GetCultureInfo("es-es")));   // 999.999.999,99 € 		
		Console.WriteLine(amount.ToString("C", CultureInfo.GetCultureInfo("en-GB")));   // £999,999,999.99

		
	}
}

```

## 

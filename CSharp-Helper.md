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
## 

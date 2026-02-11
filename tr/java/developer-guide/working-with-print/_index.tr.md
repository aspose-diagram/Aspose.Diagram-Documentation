---
title: Baskı ile Çalışma
type: docs
weight: 80
url: /tr/java/working-with-print/
---
## **Diagram yazdırma**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) diyagramların yazdırılması için dört aşırı yükleme yöntemi sağlar. Bu yöntemler, diagram'i varsayılan yazıcıya veya mevcut yazıcılardan herhangi birine özelleştirilmiş ayarlarla yazdıracak kadar esnektir. Yalnızca gereksinime göre uygun yazdırma yöntemini seçmeniz gerekir.
### **Belirli bir yazıcıya yazdırma**
diagram'in belirli bir yazıcıya yazdırılması, Diagram'in Yazdırma yönteminde parametre olarak yazıcının adını gerektirir. diagram'i istenen yazıcıya yazdırmak için aşağıdaki adımları gerçekleştirin:

- Yazdırılacak bir diagram'i yüklemek için Diagram sınıfının bir örneğini oluşturun
- Yazıcı adı ile Diagram sınıfının Print yöntemini Print yöntemine string parametresi olarak çağırın
#### **Belirli Yazıcı Programlama Örneğine Yazdırma**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(BySpecificPrinter.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name
diagram.print("LaserJet1100");

{{< /highlight >}}
```
### **Yazıcı ve Doküman Adını Ayarlama**
Aspose.Diagram API'ler, bir yazdırma işi için belirli yazıcı ve belge adının ayarlanmasına izin verir. diagram'i istenen yazıcıya yazdırmak için aşağıdaki adımları gerçekleştirin:

- Yazdırılacak bir diagram'i yüklemek için Diagram sınıfının bir örneğini oluşturun
- Diagram sınıfının Print yöntemini, yazıcı ve belge adı ile birlikte Print yöntemine string parametresi olarak çağırın
#### **Yazıcı ve Doküman Adı Ayarı Programlama Örneği**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetPrintJobAndPrinterName.class);   
// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}
```

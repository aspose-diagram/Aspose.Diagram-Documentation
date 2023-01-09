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
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-BySpecificPrinter-BySpecificPrinter.java" >}}
### **Yazıcı ve Doküman Adını Ayarlama**
Aspose.Diagram API'ler, bir yazdırma işi için belirli yazıcı ve belge adının ayarlanmasına izin verir. diagram'i istenen yazıcıya yazdırmak için aşağıdaki adımları gerçekleştirin:

- Yazdırılacak bir diagram'i yüklemek için Diagram sınıfının bir örneğini oluşturun
- Diagram sınıfının Print yöntemini, yazıcı ve belge adı ile birlikte Print yöntemine string parametresi olarak çağırın
#### **Yazıcı ve Doküman Adı Ayarı Programlama Örneği**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPrintJobAndPrinterName-SetPrintJobAndPrinterName.java" >}}

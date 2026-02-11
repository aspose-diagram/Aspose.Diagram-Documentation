---
title: Baskı ile Çalışma
type: docs
weight: 80
url: /tr/net/working-with-print/
description: Bu bölümde via XpsPrint belgesinin Aspose.Diagram ile nasıl yazdırılacağı açıklanmaktadır.
---
## **Bir Sunucuda Belge Nasıl Yazdırılır via XpsPrint API**
Bu makale, bir .NET uygulamasından yönetilmeyen XpsPrint API'e bir XPS belgesi göndermek isteyen herkes için yararlı olabilir. Ancak bu makalenin asıl amacı, Aspose.Diagram ve XpsPrint API kullanılarak bir ASP.NET veya Windows Hizmet uygulamasından diagram'in nasıl yazdırılacağını göstermektir.
### **Sorun**
Bir .NET uygulaması geliştirdiğinizde ve bazı basılı çıktılar üretmeniz gerektiğinde, System.Drawing.Printing ad alanındaki sınıfları veya WPF sınıflarını kullanabilirsiniz. Ancak, bir ASP.NET veya Windows Hizmet uygulaması geliştirirseniz, yazdırma seçenekleriniz ciddi şekilde sınırlıdır, çünkü Microsoft bu yaklaşımların kullanılmamasını önerir. Daha fazla bilgi için aşağıdaki bağlantılara bakın.

<http://support.microsoft.com/kb/324565>

.NET Framework Yazdırma sınıflarının kullanımı bir hizmetten desteklenmiyor. Bu, genellikle sunucu hizmeti bağlamında çalışan ASP sayfalarını içerir.

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

System.Drawing.Printing ad alanındaki sınıfların, bir Windows hizmeti veya ASP.NET uygulaması veya hizmeti içinde kullanımı desteklenmez. Bu sınıfları, bu uygulama türlerinden birinin içinden kullanmaya çalışmak, hizmet performansının düşmesi ve çalışma zamanı istisnaları gibi beklenmeyen sorunlara neden olabilir.

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

Windows hizmetleri oluşturmak için WPF kullanımı desteklenmez. WPF bir sunum teknolojisi olduğundan, Windows hizmeti, kullanıcı etkileşimi içeren görsel işlemleri gerçekleştirmek için uygun izinleri gerektirir. Windows hizmeti uygun izinlere sahip değilse beklenmeyen sonuçlar olabilir.

Document nesnesi, belgeleri yazdırmak için Print yöntemleri ailesini sağlar ve bu yöntemler, System.Drawing.Printing ad alanında tanımlanan via .NET yazdırma sınıflarını yazdırır. Aspose.Diagram'in sunucu taraflı uygulamalarında bu yazdırma yöntemini sorunsuz kullanan birçok müşterisi var ama Microsoft'in tavsiyelerine uymanın bir yolu var ve bu yazıda anlatılıyor.
### **Çözüm**
Belgeleri Microsoft'e göre yazdırmanın doğru yolu, yönetilmeyen XpsPrint API'i kullanmaktır. Bu API, Windows 7, Windows Server 2008 R2'de ve ayrıca Windows Vista için Platform Güncellemesi kurulu olması koşuluyla Windows Vista'da mevcuttur.

Aspose.Diagram, herhangi bir belgeyi kolayca XPS'e dönüştürebildiğinden, yalnızca XPS belgesini XpsPrint API'e geçiren bir kod yazmamız gerekiyor. Tek sorun, XpsPrint API'in yönetilmemesi ve Platform Invoke hakkında biraz bilgi gerektirmesi.
### **Kod**
XpsPrintHelper sınıfını kullanımı oldukça kolay olan Print metodu ile oluşturduk. Yazdırmak istediğiniz belgeyi, yazıcı adını ve isteğe bağlı iş adını belirtmeniz yeterlidir. Belgeyi gönderirken veya yazdırırken herhangi bir sorun olursa, yöntem bir istisna atar.

Son parametre, kodun iş yazdırılana kadar beklemesi mi yoksa yazdırma işi gönderildikten hemen sonra geri dönmesi mi gerektiğini belirten bir Boolean değeridir. Hemen geri dönmeyi seçerseniz, sonunda belgenin başarıyla yazdırılıp yazdırılmadığını belirleyemezsiniz.
#### **Programlama Örneği**
Aşağıdaki kod örneği, via XPS yazdırmak için yardımcı program sınıfının nasıl çağrılacağını gösterir.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
            
// Specify the name of the printer you want to print to.
const string printerName = @"\\COMPANY\Brother MFC-885CW Printer";

// Print the document.
XpsPrintHelper.Print(diagram, printerName, "My Test Job", true);

{{< /highlight >}}
```


XpsPrintHelper.Print yönteminin iki aşırı yüklemesi vardır. İlk aşırı yükleme, bir Aspose.Diagram.Diagram nesnesini alır ve onu XPS biçiminde bir MemoryStream'e kaydeder. Ardından, diğer XpsPrintHelper.Print aşırı yüklemesini başlatır.

Bu örneği Aspose.Diagram olmadan kullanmak istiyorsanız (örneğin, zaten bir XPS belgeniz var ve bunu bir ASP.NET veya Windows Hizmet uygulamasından yazdırmak istiyorsanız), o zaman bu yöntemi silebilirsiniz.
#### **XPS Akış ve Yazdırma Programlama Örneği**
Bu kod örneği, bir Diagram'i XPS akışına dönüştürür ve yazdırır.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
/// <summary>
/// Sends an Aspose.Diagram document to a printer using the XpsPrint API.
/// </summary>
/// <param name="diagram"></param>
/// <param name="printerName"></param>
/// <param name="jobName">Job name. Can be null.</param>
/// <param name="isWait">True to wait for the job to complete. False to return immediately after submitting the job.</param>
/// <exception cref="Exception">Thrown if any error occurs.</exception>
public static void Print(Diagram diagram, string printerName, string jobName, bool isWait)
{
    if (diagram == null)
        throw new ArgumentNullException("document");

    // Use Aspose.Diagram to convert the document to XPS and store in a memory stream.
    MemoryStream stream = new MemoryStream();
    diagram.Save(stream, SaveFileFormat.XPS);
    stream.Position = 0;

    Print(stream, printerName, jobName, isWait);
}

{{< /highlight >}}
```


İkinci XpsPrintHelper.Print aşırı yüklemesi bir Stream nesnesini kabul eder. Akış, XPS biçiminde bir belge içermelidir. Bu yöntem bir XPS yazdırma işini başlatır, belgeyi XpsPrint API'e gönderir ve gerekirse sonucu bekler.
#### **XpsPrint API Programlama Örneği**
Bu kod örneği, XpsPrint API'i kullanarak bir XPS belgesini yazdırır.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
/// <summary>
/// Sends a stream that contains a document in the XPS format to a printer using the XpsPrint API.
/// Has no dependency on Aspose.Diagram, can be used in any project.
/// </summary>
/// <param name="stream"></param>
/// <param name="printerName"></param>
/// <param name="jobName">Job name. Can be null.</param>
/// <param name="isWait">True to wait for the job to complete. False to return immediately after submitting the job.</param>
/// <exception cref="Exception">Thrown if any error occurs.</exception>
public static void Print(Stream stream, string printerName, string jobName, bool isWait)
{
    if (stream == null)
        throw new ArgumentNullException("stream");
    if (printerName == null)
        throw new ArgumentNullException("printerName");

    // Create an event that we will wait on until the job is complete.
    IntPtr completionEvent = CreateEvent(IntPtr.Zero, true, false, null);
    if (completionEvent == IntPtr.Zero)
        throw new Win32Exception();

    try
    {
        IXpsPrintJob job;
        IXpsPrintJobStream jobStream;
        StartJob(printerName, jobName, completionEvent, out job, out jobStream);

        CopyJob(stream, job, jobStream);

        if (isWait)
        {
            WaitForJob(completionEvent);
            CheckJobStatus(job);
        }
    }
    finally
    {
        if (completionEvent != IntPtr.Zero)
            CloseHandle(completionEvent);
    }
}

{{< /highlight >}}
```


StartJob, CopyJob, WaitForJob ve CheckJobStatus yöntemlerinin kodu ile IXpsPrintJob ve IXpsPrintJobStream arabirimlerinin tanımları oldukça düşük düzeydedir ve Platform Invoke ve COM Interop kullanır. Bu kod, kısa olması için makaleye dahil edilmemiştir, ancak örnek indirmede mevcuttur.

XpsPrint API, işin ilerlemesini izlemek gibi ek işlevler de sağlar, ancak XpsPrintHelper'ımız çok basit bir paketleyicidir ve bu işlevi ortaya çıkarmaz. İsterseniz bunu kendiniz ekleyebilirsiniz.

{{% alert color="primary" %}}

Projeyi çalıştırdığınızda, belirtilen yazıcıda örnek bir belge yazdırır. Sonuçları görünür kılmak için konsol penceresi açılır. Program, başarı mesajını veya atılmışsa bir istisnanın metnini görüntüler.

{{% /alert %}}
## **Diagram yazdırma**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) diyagramların yazdırılması için dört aşırı yükleme yöntemi sağlar. Bu yöntemler, diagram'i varsayılan yazıcıya veya mevcut yazıcılardan herhangi birine özelleştirilmiş ayarlarla yazdıracak kadar esnektir. Yalnızca gereksinime göre uygun yazdırma yöntemini seçmeniz gerekir.
### **Varsayılan yazıcıya yazdırma**
diagram'in varsayılan yazıcıya yazdırılması Aspose.Diagram for .NET'de oldukça basittir. diagram'i varsayılan yazıcıya yazdırmak için aşağıdaki adımları gerçekleştirin:

- Yazdırılacak bir diagram'i yüklemek için Diagram sınıfının bir örneğini oluşturun
- Diagram nesnesi tarafından sunulan hiçbir parametre olmadan Yazdır yöntemini çağırın
#### **Varsayılan Yazıcı Programlama Örneğine Yazdırma**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the default printer
diagram.Print();

{{< /highlight >}}
```
### **Belirli bir yazıcıya yazdırma**
diagram'in belirli bir yazıcıya yazdırılması, Diagram'in Yazdırma yönteminde parametre olarak yazıcının adını gerektirir. diagram'i istenen yazıcıya yazdırmak için aşağıdaki adımları gerçekleştirin:

- Yazdırılacak bir diagram'i yüklemek için Diagram sınıfının bir örneğini oluşturun
- Yazıcı adı ile Diagram sınıfının Print yöntemini Print yöntemine string parametresi olarak çağırın
#### **Belirli Yazıcı Programlama Örneğine Yazdırma**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the printer name
diagram.Print("LaserJet1100");

{{< /highlight >}}
```
### **Yazıcı ve Doküman Adını Ayarlama**
Aspose.Diagram API'ler, bir yazdırma işi için belirli yazıcı ve belge adının ayarlanmasına izin verir. diagram'i istenen yazıcıya yazdırmak için aşağıdaki adımları gerçekleştirin:

- Yazdırılacak bir diagram'i yüklemek için Diagram sınıfının bir örneğini oluşturun
- Diagram sınıfının Print yöntemini, yazıcı ve belge adı ile birlikte Print yöntemine string parametresi olarak çağırın
#### **Yazıcı ve Doküman Adı Ayarı Programlama Örneği**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.Print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}
```

---
title: Dış Veri Kaynaklarıyla Çalışma
type: docs
weight: 190
url: /tr/java/working-with-external-data-sources/
---
## **Visio Çiziminin Veri Bağlantısını Güncelle**
Aspose.Diagram API, kullanıcıların bağlantılı Visio çiziminin SQL Server veri bağlantısını düzenlemesine olanak tanır. Visio çizimine veri getirmek için SQL Server verilerine erişmemiz gerekiyor. Veritabanının özel modda açılmadığından emin olun.

 Microsoft Visio diyagramlarının verilerini harici veri kaynaklarından bağlamak artık yaygın bir olgudur. bu[Veri Bağlantısı Koleksiyonu](https://reference.aspose.com/diagram/java/com.aspose.diagram/dataconnectioncollection) sınıf tüm veri bağlantılarını içerir.
### **Programlama Örneği**
Aşağıdaki kod parçası, belirli bir veri bağlantısını düzenler ve ayrıca Visio diagram'deki mevcut tüm kayıt kümelerini yeniler.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(EditDataConAndRefreshRecords.class);
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
// set connecting string
diagram.getDataConnections().get(0).setConnectionString("Data Source=MyServer;Initial Catalog=MyDB;Integrated Security=True");
// set command
diagram.getDataConnections().get(0).setCommand("SELECT * from Project with(nolock)");
// save Visio diagram
diagram.save(dataDir + "EditDataConAndRefreshRecords_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}


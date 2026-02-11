---
title: Dış Veri Kaynaklarıyla Çalışma
type: docs
weight: 200
url: /tr/net/working-with-external-data-sources/
description: Bu bölümde, Aspose.Diagram ile harici veri kaynaklarıyla nasıl çalışılacağı açıklanmaktadır.
---
## **SQL Server Veri Bağlantısını Düzenleyin ve Kayıt Kümelerini Yenileyin**
Aspose.Diagram API, kullanıcıların SQL Server veri bağlantısını düzenlemesine ve tüm kayıt kümelerini yenilemesine olanak tanır. Visio çizimine veri getirmek için SQL Server verilerine erişmemiz gerekiyor. Veritabanının özel modda açılmadığından emin olun.
### **Veri Bağlantısını ve Kayıt Kümelerini Güncelleyin**
 Microsoft Visio diyagramlarının verilerini harici veri kaynaklarından bağlamak artık yaygın bir olgudur. bu[Veri Bağlantısı Koleksiyonu](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection) sınıf tüm veri bağlantılarını içerir.
#### **Programlama Örneği**
Aşağıdaki kod parçası, belirli bir veri bağlantısını düzenler ve ayrıca Visio diagram'deki mevcut tüm kayıt kümelerini yeniler.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ExternalDataSources();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
// Set connecting string
diagram.DataConnections[0].ConnectionString = "Data Source=MyServer;Initial Catalog=MyDB;Integrated Security=True";
// Set command
diagram.DataConnections[0].Command = "SELECT * from Project with(nolock)";
// Refresh all record sets
diagram.Refresh();
// Save Visio diagram
diagram.Save(dataDir + "EditDataConAndRefreshRecords_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}


---
title: Работа с внешними источниками данных
type: docs
weight: 190
url: /ru/java/working-with-external-data-sources/
---
## **Обновление соединения данных чертежа Visio**
Aspose.Diagram API позволяет пользователям редактировать подключение к данным SQL Server связанного чертежа Visio. Чтобы внести данные в чертеж Visio, нам нужен доступ к данным SQL Server. Убедитесь, что база данных не открыта в монопольном режиме.

 В настоящее время обычным явлением является связывание данных диаграмм Microsoft Visio из внешних источников данных.[DataConnectionCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/dataconnectioncollection) класс содержит все подключения к данным.
### **Образец программирования**
Следующий фрагмент кода редактирует конкретное подключение к данным, а также обновляет все доступные наборы записей в файле Visio diagram.


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


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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-ExternalDataSources-EditDataConAndRefreshRecords-EditDataConAndRefreshRecords.java" >}}

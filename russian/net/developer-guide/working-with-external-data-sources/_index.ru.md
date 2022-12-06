---
title: Работа с внешними источниками данных
type: docs
weight: 200
url: /ru/net/working-with-external-data-sources/
description: В этом разделе объясняется, как работать с внешними источниками данных с помощью Aspose.Diagram.
---
## **Изменение подключения к данным SQL Server и обновление наборов записей**
Aspose.Diagram API позволяет пользователям редактировать подключение к данным SQL Server и обновлять все наборы записей. Чтобы внести данные в чертеж Visio, нам нужен доступ к данным SQL Server. Убедитесь, что база данных не открыта в монопольном режиме.
### **Обновление подключения к данным и наборов записей**
 В настоящее время обычным явлением является связывание данных диаграмм Microsoft Visio из внешних источников данных.[DataConnectionCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection) класс содержит все подключения к данным.
#### **Образец программирования**
Следующий фрагмент кода редактирует конкретное подключение к данным, а также обновляет все доступные наборы записей в файле Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-External-Data-Sources-EditDataConAndRefreshRecords-EditDataConAndRefreshRecords.cs" >}}

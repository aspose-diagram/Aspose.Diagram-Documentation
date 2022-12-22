---
title: Arbeta med externa datakällor
type: docs
weight: 190
url: /sv/java/working-with-external-data-sources/
---
## **Uppdatera dataanslutning för Visio-ritningen**
Aspose.Diagram API tillåter användare att redigera SQL Server-dataanslutningen för den länkade Visio-ritningen. För att få in data i Visio-ritningen behöver vi tillgång till SQL Server-data. Se till att databasen inte öppnas i exklusivt läge.

 Det är nu ett vanligt fenomen att länka data från Microsoft Visio diagram från externa datakällor. De[DataConnectionCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/dataconnectioncollection) klass innehåller alla dataanslutningar.
### **Programmeringsexempel**
Följande kod redigerar en viss dataanslutning och uppdaterar även alla tillgängliga postuppsättningar i Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-ExternalDataSources-EditDataConAndRefreshRecords-EditDataConAndRefreshRecords.java" >}}

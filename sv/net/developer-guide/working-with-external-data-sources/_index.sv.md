---
title: Arbeta med externa datakällor
type: docs
weight: 200
url: /sv/net/working-with-external-data-sources/
description: Det här avsnittet förklarar hur du arbetar med externa datakällor med Aspose.Diagram.
---
## **Redigera SQL Server Data Connection och Refresh Record Sets**
Aspose.Diagram API tillåter användare att redigera SQL Server-dataanslutning och uppdatera alla postuppsättningar. För att få in data i Visio-ritningen behöver vi tillgång till SQL Server-data. Se till att databasen inte öppnas i exklusivt läge.
### **Uppdatera dataanslutning och postuppsättningar**
 Det är nu ett vanligt fenomen att länka data från Microsoft Visio diagram från externa datakällor. De[DataConnectionCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection) klass innehåller alla dataanslutningar.
#### **Programmeringsexempel**
Följande kod redigerar en viss dataanslutning och uppdaterar även alla tillgängliga postuppsättningar i Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-External-Data-Sources-EditDataConAndRefreshRecords-EditDataConAndRefreshRecords.cs" >}}

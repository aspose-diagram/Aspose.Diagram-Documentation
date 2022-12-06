---
title: Konfigurera Visio Tidslinjeformer
type: docs
weight: 20
url: /sv/java/configure-visio-timeline-shapes/
---
## **Ställ in egenskaper för milstolpeform**
Aspose.Diagram tillåter utvecklare att ange milstolpsegenskaper. Den här artikeln visar hur du ställer in milstolpedatum, datumformat, flagga och typ för automatisk uppdatering.
### **Ställa in milstolpsdatum, datumformat, flagga för automatisk uppdatering och typ**
 De[MilestoneHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)klass tar en[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) objekt medan du initierar[MilestoneHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper) objekt. Kodexemplet i den här artikeln anger egenskaperna för milstolpedatum, datumformat, flagga för automatisk uppdatering och milstolpetyp.

|<p>**Milstolpen före uppdatering** </p><p>![todo:image_alt_text](http://i.imgur.com/XulWyBC.png)</p><p>\</p>|<p>**Milstolpen efter uppdatering. Notera det ändrade datumformatet.** </p><p>![todo:image_alt_text](http://i.imgur.com/cMJQNch.png)</p><p>\</p>|
|:- |:- |
Processen för uppdatering av milstolpsdatum, datumformat, flagga för automatisk uppdatering och milstolpetyp:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Initiera MilestoneHelper-objektet.
1. Sätt ett milstolpedatum.
1. Ställ in formatet för milstolpedatum.
1. Ställ in en flagga för automatisk uppdatering.
1. Ställ in milstolpetypen
1. Spara Visio-ritningen i valfritt format som stöds.
#### **Ställ in milstolpeprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-SetMilestoneProps-SetMilestoneProps.java" >}}


Tabell över datumformatvärden:

|**Värde**|**Formatera sträng**|
|:- |:- |
|0|dddd, åååå-Md|
|1|åååå-MM-dd|
|2|åå-MMM-d|
|3|åååå/m/d|
|4|åå-MMM.-d|
|5|d MMMM åååå|
|6|åå-M|
|7|MMM-åå|
|8|MMMM d, åååå|
|9|MMM d, åååå|
|10|Md-åå|
|11|Md|
|12|d MMMM, åååå|
|13|d MMM, åååå|
|14|dM-åå|
|15|dM|
|16|åå-Md|
|17|åååå-Md|
|18|M-åå|
|19|M-åååå|
|20|MMMM åååå|
|21|MMMM åå|
|22|MMM åååå|
|23|MMM åå|
|24|åå|
|25|åååå|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
## **Ställ in tidsperiod och datumformat för tidslinjeform**
Aspose.Diagram tillåter utvecklare att konfigurera tidslinjen programmatiskt. Det här förklarar hur du justerar tidsperioden och datumformatet för tidslinjeformer (block, linje, linjal, delad eller cylindrisk).
### **Ställa in tidsperiod och datumformat**
 De[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper)klass tar en[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) objekt när du initierar[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) objekt. Kodexemplet i den här artikeln ställer in tidsperiodens start-, slut- och datumformatvärden.

|<p>**Tidsperiodfliken i dialogrutan Visio Konfigurera tidslinje** </p><p>![todo:image_alt_text](http://i.imgur.com/nHth3W8.png)</p>|<p>**Tidsformatfliken i dialogrutan Visio Konfigurera tidslinje** </p><p>![todo:image_alt_text](http://i.imgur.com/TxFKc1K.png)</p>|
|:- |:- |
|<p>**Ingång diagram** </p><p>![todo:image_alt_text](configure-visio-timeline-shapes_1.png)</p>|<p>**diagram efter att värdena har ändrats** </p><p>![todo:image_alt_text](configure-visio-timeline-shapes_2.png)</p>|
Processen för att uppdatera tidsperiodens start-, slut- och datumformat är:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Initiera TimeLineHelper-objektet.
1. Ställ in tidsperiodens start.
1. Ställ in tidsperiodens slut.
1. Ställ in ett datumformat.
1. Spara Visio-ritningen i valfritt format som stöds.
#### **Ställ in tidsperiod och datumprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-ConfigureTimeLine-ConfigureTimeLine.java" >}}


Tabell över datumformatvärden:

|**Värde**|**Formatera sträng**|
|:- |:- |
|0|dddd, åååå-Md|
|1|åååå-MM-dd|
|2|åå-MMM-d|
|3|åååå/m/d|
|4|åå-MMM.-d|
|5|d MMMM åååå|
|6|åå-M|
|7|MMM-åå|
|8|MMMM d, åååå|
|9|MMM d, åååå|
|10|Md-åå|
|11|Md|
|12|d MMMM, åååå|
|13|d MMM, åååå|
|14|dM-åå|
|15|dM|
|16|åå-Md|
|17|åååå-Md|
|18|M-åå|
|19|M-åååå|
|20|MMMM åååå|
|21|MMMM åå|
|22|MMM åååå|
|23|MMM åå|
|24|åå|
|25|åååå|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
## **Uppdatera milstolpar på tidslinjen i Visio**
Aspose.Diagram tillåter utvecklare att justera milstolpar på tidslinjeformerna (block, linje, linjal, delad eller cylindrisk) enligt tidsperiodens förändring.
### **Uppdatera milstolpar på tidslinjen med TimeLineHelper-klassen**
 Metoden RefreshTimeLine exponerad av[TimeLineHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/timelinehelper) klass kan användas för att återuppliva milstolpar på tidslinjen.

Koden nedan visar hur man:

1. ladda ett prov diagram.
1. få en tidslinjeform.
1. initiera TimeLineHelper-objektet.
1. ställ in tidsperiodens start.
1. ställ in tidsperiodens slut.
1. ställ in datumformat (valfritt).
1. anropa RefreshTimeLine-metoden för TimeLineHelper-objektet.
1. spara diagram
#### **Uppdatera milstolpar med TimeLineHelper-programmeringsexempel**
Använd följande kod i din Java-applikation för att återuppliva milstolpar på tidslinjen med Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshTimeLine-RefreshTimeLine.java" >}}
### **Uppdatera Milestones på tidslinjen med MilestoneHelper-klassen**
 RefreshMilestone-metoden exponerad av[MilestoneHelper](https://reference.aspose.com/diagram/java/com.aspose.diagram/milestonehelper)klass kan användas för att uppdatera milstolpar på tidslinjen.

Koden nedan visar hur man:

1. ladda ett prov diagram.
1. få en tidslinjeform.
1. lägg till Shape i Visio diagram med AddShape-metoden.
1. initiera MilestoneHelper-objektet.
1. ställ in ett milstolpedatum.
1. ställ in Milstones IsAutoUpdate-egenskap till true.
1. anropa RefreshMilestone-metoden för MilestoneHelper-objektet.
1. spara diagram
#### **Uppdatera Milestones med hjälp av MilestoneHelper-programmeringsexempel**
Använd följande kod i din Java-applikation för att uppdatera milstolpar på tidslinjen med Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-TimeLine-RefreshMilestoneWithMilestoneHelper-RefreshMilestoneWithMilestoneHelper.java" >}}

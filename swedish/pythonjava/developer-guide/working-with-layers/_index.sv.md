---
title: Arbeta med lager
type: docs
weight: 160
url: /sv/python-java/working-with-layers/
---
### **Konfigurera formobjekt med lager**
Aspose.Diagram för Python via Java gör det möjligt att konfigurera formobjekt med lager i Microsoft Office Visio diagram. Varje form kan tillhöra flera lager av användarnas behov så att utvecklare kan hantera slutanvändarbehov.

 De[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class object erbjuder LayerMember-egenskapen som gör det möjligt att lägga till/ta bort formobjekt till/från lagren i Visio-ritningen. Användare kan hantera dessa egenskaper programmatiskt med Aspose.Diagram API enligt följande:

**Lägg till, ta bort och flytta formobjekt till/från lager i diagram.** 

Följande kodbit hjälper till att lägga till, ta bort och flytta formobjektegenskaper.
#### **Programmeringsexempel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-ConfigureShapeLayers.py" >}}
### **Lägg till ett lager i sidbladet Visio**
Aspose.Diagram för Python via Java tillåter utvecklare att lägga till nya lager för att organisera anpassade kategorier av former och sedan tilldela former till dessa lager programmatiskt.

 De[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class erbjuder add-metod som gör det möjligt att lägga till en ny[Lager](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) klassobjekt i[Visio ritningen](DrawingFlowChart.vsdx). Utvecklare kan ställa in lageregenskaper genom att initiera dess klassobjekt.

Följande kodbit hjälper till att lägga till Layer-objekt.
#### **Programmeringsexempel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-AddLayer.py" >}}

{{% alert color="primary" %}} 

Aspose.Diagram för Python via Java ger utvecklare tillgång till de befintliga lagren av Visio diagram.

{{% /alert %}} 
### **Få alla tillgängliga lager**
 De[PageSheet](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) egendom av[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) klass gör det möjligt att hämta listan över tillgängliga lager från[Visio ritningen](DrawingFlowChart.vsdx) använder sig av[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) klass.

Följande kodbit hjälper dig att få en lista över lager.
#### **Programmeringsexempel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-RetrieveAllLayers.py" >}}

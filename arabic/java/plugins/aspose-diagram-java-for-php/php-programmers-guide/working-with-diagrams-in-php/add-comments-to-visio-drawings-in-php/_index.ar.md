---
title: أضف تعليقات إلى Visio الرسومات في PHP
type: docs
weight: 10
url: /ar/java/add-comments-to-visio-drawings-in-php/
---
## **Aspose.Diagram - إضافة تعليقات إلى رسومات Visio**
 لإضافة تعليقات إلى Visio الرسومات باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**AddCommentToDiagram** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Add comment

$diagram->getPages()->getPage(0)->addComment(7.205905511811023, 3.880708661417323, "test@");

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddComment.vdx", $saveFileFormat->VDX);

print "Added comment successfully!".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**أضف تعليقات إلى رسومات Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/AddCommentToDiagram.php)

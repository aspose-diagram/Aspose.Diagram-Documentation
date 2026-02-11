---
title: طرق مختلفة لفتح الملفات
type: docs
weight: 10
url: /ar/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

مع Aspose.Diagram ، من السهل فتح الملفات ، على سبيل المثال ، لاسترداد البيانات ، أو استخدام قالب مصمم لتسريع عملية التطوير.

{{% /alert %}}

## **فتح ملف via a مسار**

 يمكن للمطورين فتح ملف Microsoft Diagram باستخدام مسار الملف الخاص به على الكمبيوتر المحلي عن طريق تحديده في**Diagram**منشئ الطبقة. ما عليك سوى تمرير المسار في المُنشئ كملف*سلسلة*. سوف يقوم Aspose.Diagram باكتشاف نوع تنسيق الملف تلقائيًا.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **فتح ملف via a Stream**

 من السهل أيضًا فتح ملف Visio كتدفق. للقيام بذلك ، استخدم إصدارًا محملاً بشكل زائد من المُنشئ يأخذ الامتداد*BufferStream*الكائن الذي يحتوي على الملف.


{{< highlight python >}}
import os
import sys
import aspose.diagram
from aspose.diagram import *
from aspose.pyio import BufferStream

#// Build path of an existing diagram
visioDrawing = os.path.join(sourceDir, "Drawing1.vsdx")
# Create a Stream object
f = open(visioDrawing, 'rb')
data = f.read()
databuff = BufferStream(data)
diagram = Diagram(databuff)

#// Save diagram in the VSDX format
diagram.save("Visio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **فتح ملف مع LoadOptions**

 لفتح ملف مع خيارات التحميل ، استخدم الامتداد**LoadOptions**فئات لتعيين الخيارات ذات الصلة للفئات لملف القالب المراد تحميله.


{{< highlight python >}}
import os
import sys
import aspose.diagram
from aspose.diagram import *

#// Build path of an existing diagram
visioDrawing = os.path.join(sourceDir, "Drawing1.vsdx")
# Instantiate LoadOptions specified by the LoadFileFormat
loadOptions = LoadOptions(LoadFileFormat.VSDX)
diagram = Diagram(visioDrawing,loadOptions)

#// Save diagram in the VSDX format
diagram.save("Visio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}



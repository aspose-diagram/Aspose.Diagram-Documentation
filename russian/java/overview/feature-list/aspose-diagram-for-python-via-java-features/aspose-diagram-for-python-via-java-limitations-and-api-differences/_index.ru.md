---
title: Aspose.Diagram для Python via Java Ограничения и API Различия
type: docs
weight: 20
url: /ru/java/aspose-diagram-for-python-via-java-limitations-and-api-differences/
---
## **Общественный API Различия**
### **Пример**
**Aspose.Diagram for Java**

{{< highlight "java" >}}

 import com.aspose.diagram.*;

public class Test1 {

	public static void main(String[] args) throws Exception {

		Diagram diagram = new Diagram();

		diagram.save("out.vsdx",SaveFileFormat.VSDX);

	}

}

{{< /highlight >}}



**Aspose.Diagram для Python via Java**

{{< highlight "python" >}}

 import jpype

import asposediagram


def run():

    kwargs = dict(convertStrings=True)

    jpype.startJVM(**kwargs)

    from asposediagram.api import Diagram, FileFormatType, License

    diagram = Diagram()
    
    diagram.save( "out.vsdx",SaveFileFormat.VSDX)

    jpype.shutdownJVM()

{{< /highlight >}}

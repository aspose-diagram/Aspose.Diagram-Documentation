---
title: Aspose.Diagram 为 Python 通过 Java 限制和 API 差异
type: docs
weight: 20
url: /zh/java/aspose-diagram-for-python-via-java-limitations-and-api-differences/
---
## **公共 API 差异**
### **例子**
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



**Aspose.Diagram 为 Python 通过 Java**

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

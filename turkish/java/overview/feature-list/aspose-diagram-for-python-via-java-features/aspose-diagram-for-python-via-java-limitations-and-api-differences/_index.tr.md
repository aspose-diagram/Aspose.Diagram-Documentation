---
title: Java aracılığıyla Python için Aspose.Diagram Sınırlamalar ve API Farklar
type: docs
weight: 20
url: /tr/java/aspose-diagram-for-python-via-java-limitations-and-api-differences/
---
## **Kamu API Farklar**
### **Örnek**
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



**Java üzerinden Python için Aspose.Diagram**

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

---
title: Aspose.Diagram per Python via Java Limitazioni e API Differenze
type: docs
weight: 20
url: /it/java/aspose-diagram-for-python-via-java-limitations-and-api-differences/
---
## **Pubblico API Differenze**
### **Esempio**
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



**Aspose.Diagram per Python tramite Java**

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

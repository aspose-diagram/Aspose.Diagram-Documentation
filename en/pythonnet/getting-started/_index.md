---
title: Getting Started
linktitle: Getting Started
type: docs
weight: 4
url: /python-net/getting-started/ 
keywords: "python, visio, install"
description: Setup Aspose.Diagram for Python via .NET and installation guidelines.
---

## **System Requirements**
Aspose.Diagram for Python via .NET is platform-independent API and can be used on any platform (Windows and Linux) where [Python](https://www.python.org/downloads/) is installed. 

## **Python Version**
- Python 3.6 or higher

## **Installation**
### **Windows:**
You can easily use Aspose.Diagram for Python via .NET from [pypi](https://pypi.org/project/aspose-diagram-python/) with the following command.
{{< highlight NET >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

### **Linux:**
You can easily use Aspose.Diagram for Python via .NET from [pypi](https://pypi.org/project/aspose-diagram-python/) with the following command.
{{< highlight NET >}}

 $ pip install aspose-diagram-python

{{< /highlight >}}

## **Creating the Hello World Application**

- Create a file named **CreatingNewVisioFile.py** and use the following sample code:


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram()

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


- Now save the code above to "CreatingNewVisioFile.py" and run "python CreatingNewVisioFile.py" @command prompt.

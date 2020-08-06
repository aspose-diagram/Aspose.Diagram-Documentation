---
title: Public API Changes in Aspose.Diagram 5.7.0
type: docs
weight: 30
url: /java/public-api-changes-in-aspose-diagram-5-7-0/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Diagram API from version 5.6.0 to 5.7.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram. 

{{% /alert %}} 
### **Set Date Pattern Strings on the Timeline**
The new setDateFormatStringForBE and setDateFormatStringForIntm methods have been added in the TimelineHelper class. Example codes:

**Java**

{{< highlight java >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.setDateFormatStringForBE("yyyy-MM-dd");

// set DateFormat String for intm of timeline shape

timelineHelper.setDateFormatStringForIntm("yyyy-MM-dd");

{{< /highlight >}}

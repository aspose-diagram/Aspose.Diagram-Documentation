---
title: Public API Changes in Aspose.Diagram 4.2.0
type: docs
weight: 30
url: /net/public-api-changes-in-aspose-diagram-4-2-0/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Diagram API from version 4.1.0 to 4.2.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram. 

{{% /alert %}} 
### **Adds two methods GetMasterByName and IsExist to MasterCollection**
Developers can now glue group shapes inside the container. Also, this release allows to get Master by its name and check presence of the Master by its name. You can see example topics about these features: [Get Master Object from the Visio], [Check Presence of a Master in the Visio Drawing]
### **Adds a method GlueShapesInContainer to Page**
Previously, it was working perfect with ungroup shapes. However, there’re many points in the group shapes, it was not supported so well. We have now added group shapes support. Please see an example topic about this feature: [Glue Group Shape Inside the Container]
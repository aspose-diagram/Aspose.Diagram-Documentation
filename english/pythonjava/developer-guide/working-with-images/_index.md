---
title: Working with Images
type: docs
weight: 70
url: /python-java/working-with-images/
description: This page describes how to extract, replace or insert an image from a page of the Visio drawing with Aspose.Diagram library.
---

## **Extract All Images From a Visio Page**
In Microsoft Visio, pages are either foreground or background pages. You can extract images from a particular page of [a Visio file](ExtractAllImagesFromPage.vsd).
### **Extract Images**
The Page Class object represents the drawing area of a foreground page or a background page. The Shapes property exposed by the Diagram class supports a collection of Aspose.Diagram.Shape objects. This property can be used to extract all the images from a particular page.
#### **Extract Images Programming Sample**
The following piece of code extracts all images from a particular Visio page.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-ExtractAllImagesFromPage.py" >}}
## **Get Icons of Various Visio Shapes**
Aspose.Diagram for Python via Java API now allows developers to get icons of various [Visio shapes](Timeline.vss). 
### **Getting the Shape Icon**
The code in the samples below show how to:

1. Load an existing diagram or stencil.
1. Get master by its index
1. Get master icon. 
1. Save icon to the local space.
#### **Get Icons Programming Sample**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-GetShapeIcon.py" >}}
## **Replace a Picture Shape of the Visio Diagram**
Aspose.Diagram for Python via Java API allows developers to access and replace available picture shapes in [the Visio diagram](ExtractAllImagesFromPage.vsd).
### **Replacing a Picture Shape**
The code in the samples below show how to:

1. Load an existing diagram.
1. Iterate through the selective page shapes.
1. Apply filter to get picture shapes.
1. Save resultant Visio diagram to the local space.
#### **Replace a Picture Shape Programming Sample**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-ReplaceShapePicture.py" >}}
## **Import Image as a Visio Shape**
Aspose.Diagram for Python via Java API now allows developers to import a image as a Microsoft Visio shape.
### **Insert a Image in Visio**
The code in the samples below show how to:

1. Create a diagram.
1. Get Visio page
1. Import a image as a Visio shape
1. Save the diagram.
#### **Insert a Image Programming Sample**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-InsertImageInVisio.py" >}}

---
title: تباعد تلقائي لمجموعة من الأشكال في صفحة Visio
type: docs
weight: 30
url: /ar/python-java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **تباعد تلقائي لمجموعة من الأشكال في صفحة Visio**
مع Aspose.Diagram لـ Python via Java API ، يمكن للمطورين وضع مسافة تلقائية لمجموعة من الأشكال في رسم Visio. من أجل تحقيق ذلك ، تقدم الفئة `Page` العضو `autoSpaceShapes` الذي يأخذ معلمات ShapeCollection و AutoSpaceOptions. تسمح الفئة `AutoSpaceOptions` بضبط المسافات الأفقية والعمودية.

### **المسافات التلقائية للأشكال في الصفحة**
استخدم الكود التالي في التطبيق الخاص بك لوضع مسافة تلقائية بين مجموعة من الأشكال في أي صفحة من الرسم Visio.

``` python
# load a Visio drawing

diagram = Diagram("Drawing1.vsdx")

# get page of the Visio drawing

page = diagram.getPages().getPage("Page-1")

# initialize auto space options

options = AutoSpaceOptions()

# set horizontal and vertical distances

options.setDistanceInHorizontal(2)

options.setDistanceInVertical(2)

# set auto space 

page.autoSpaceShapes(page.getShapes(), options)

# save Visio drawing

diagram.save("AutoSpaceShapes_Out.vsdx", SaveFileFormat.VSDX)

```

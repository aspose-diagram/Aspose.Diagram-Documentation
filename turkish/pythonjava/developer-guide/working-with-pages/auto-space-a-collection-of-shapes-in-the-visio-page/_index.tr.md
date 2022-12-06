---
title: Visio Sayfasında Şekil Koleksiyonunu Otomatik Olarak Arala
type: docs
weight: 30
url: /tr/python-java/auto-space-a-collection-of-shapes-in-the-visio-page/
---
## **Visio Sayfasında Şekil Koleksiyonunu Otomatik Olarak Arala**
Python via Java API için Aspose.Diagram ile geliştiriciler, Visio çizimindeki bir şekil koleksiyonunu otomatik olarak aralayabilir. Bunu gerçekleştirmek için `Page` sınıfı, ShapeCollection ve AutoSpaceOptions parametrelerini alan `autoSpaceShapes` üyesini sunar. `AutoSpaceOptions` sınıfı, yatay ve dikey mesafelerin ayarlanmasına izin verir.

### **Sayfadaki Şekilleri Otomatik Arala**
Visio çiziminin herhangi bir sayfasında bir şekil koleksiyonunu otomatik olarak boşluk bırakmak için uygulamanızda aşağıdaki kodu kullanın.

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

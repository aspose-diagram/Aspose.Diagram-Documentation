---
title: Calcule los valores de los pines y establezca el tamaño de una forma
type: docs
weight: 40
url: /es/java/calculate-pin-values-and-setting-size-of-a-shape/
---
## **Calcule los valores PinX y PinY de la forma secundaria**
 Si la forma es una forma secundaria de un grupo, su forma x es una coordenada relativa de su forma principal, pero no una coordenada absoluta en el[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/page). Si el usuario necesita obtener la coordenada absoluta, entonces este código de muestra ayuda.

Un punto especificado en coordenadas locales se puede convertir en coordenadas principales aplicando las siguientes transformaciones en el siguiente orden:

1. Reste el valor de la propiedad LocPinX del elemento Cell_Type de la coordenada x.
1. Reste el valor de la propiedad LocPinY de Cell_Type de la coordenada y.
1. Refleje el punto sobre el eje y si el valor de la propiedad FlipX de Cell_Type es igual a uno.
1. Refleje el punto sobre el eje x si el valor de la propiedad FlipY de Cell_Type es igual a uno.
1. Gire el punto en sentido contrario a las agujas del reloj alrededor del origen según el valor de la propiedad Angle de Cell_Type.
1. Agregue el valor de PinX Cell_Type a la coordenada x.
1. Agregue el valor de PinY Cell_Type a la coordenada y.
### **Ejemplo de programación Calcular PinX y PinY**
Use el siguiente código en su aplicación Java para calcular los valores PinX y PinY de una subforma usando Aspose.Diagram for Java API.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CalculateCenterOfSubShapes.class);
        
// load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get group shape
Shape shape = diagram.getPages().get(0).getShapes().getShape(138);
// get sub-shape of the group shape
Shape subShape = shape.getShapes().getShape(140);


AffineTransform m = new AffineTransform();
// apply the translation vector
m.translate(-(float)subShape.getXForm().getLocPinX().getValue(), -(float)subShape.getXForm().getLocPinY().getValue());		
// set the elements of that matrix to a rotation
m.rotate((float)subShape.getXForm().getAngle().getValue());
// apply the translation vector
m.translate((float)subShape.getXForm().getPinX().getValue(), (float)subShape.getXForm().getPinY().getValue());

// get pinx and piny		
double pinx = m.getTranslateX();
double piny = m.getTranslateY();
		
// calculate the sub-shape pinx and piny
double resultx = shape.getXForm().getPinX().getValue() - shape.getXForm().getLocPinX().getValue() - pinx;
double resulty = shape.getXForm().getPinY().getValue() - shape.getXForm().getLocPinY().getValue() - piny;

{{< /highlight >}}
```
## **Establecer la altura y el ancho de una forma**
 los[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Class le permite controlar el tamaño de la forma especificando la altura y el ancho de la forma mediante los métodos SetHeight y SetWidth.

 Los métodos SetHeight y SetWidth, expuestos por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)clase, admite cambiar el tamaño de una forma con el maestro, sin el maestro o en forma de forma de grupo.

Los ejemplos de código de este artículo establecen el alto y el ancho para cambiar el tamaño de la forma en la página.

**Entrada diagram** 

![todo:imagen_alternativa_texto](http://i.imgur.com/cTiNWa7.png)

**El diagram después de cambiar la altura y el ancho**

![todo:imagen_alternativa_texto](calculate-pin-values-and-setting-size-of-a-shape_1.png)

El proceso para configurar Alto y Ancho es:

1. Cargue un diagram.
1. Encuentra una forma particular.
1. Establecer la altura de una forma.
1. Establezca el Ancho de una forma.
1. Guarda el diagram.
### **Ejemplo de programación de ajuste de altura y anchura**
El fragmento de código a continuación muestra cómo establecer la altura y el ancho de la forma. El código busca un rectángulo de nombre de forma, con el ID de forma 1, y establece su Alto y Ancho como doble.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ChangeShapeSize.class);
        
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by id
Shape shape = page.getShapes().getShape(796);
// alter the size of Shape
shape.setWidth(2 * shape.getXForm().getWidth().getValue());
shape.setHeight(2 * shape.getXForm().getHeight().getValue());
// save diagram
diagram.save(dataDir + "ChangeShapeSize_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

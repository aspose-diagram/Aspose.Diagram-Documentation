---
title: Efectos de rotación 3D en un dibujo Visio
type: docs
weight: 90
url: /es/java/3d-rotation-effects-in-a-visio-drawing/
---
## **Establecer propiedades de rotación 3D en Shapesheet**
Aspose.Diagram for Java API permite a los desarrolladores cambiar los valores de rotación 3D en la hoja de forma. Los valores de las celdas RotationXAngle, RotationYAngle y RotationZAngle controlan el grado de rotación en cada uno de los ejes respectivos. El valor de enumeración de RotationType controla el tipo de rotación:

1. Rotación paralela, donde la forma se gira sin tener en cuenta la perspectiva lineal.
1. Rotación de perspectiva, donde la forma se gira con perspectiva lineal.
1. Ajustes preestablecidos de rotación oblicua (abajo a la izquierda, abajo a la derecha, arriba a la izquierda y arriba a la derecha), donde la forma se gira con proyección oblicua.

los**KeepTextFlat**el valor de la celda indica si el texto de una forma ignorará la rotación de la forma en 3D. No se aplica a la rotación 2-D. los**DistanciaDesdeSuelo**el valor de la celda determina la distancia que el objeto se eleva desde el suelo en los puntos cuando se gira en 3-D. los**Perspectiva**el valor de la celda determina el ángulo de perspectiva para una rotación de perspectiva, en grados (0 a 359,9).
### **Establecer propiedades de rotación 3D**
El miembro ThreeDFormat expuesto por el[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)La clase se puede utilizar para establecer propiedades de rotación 3D.

El siguiente código muestra cómo:

1. Cargue un dibujo de origen.
1. Recupere una forma por nombre de página y parámetros de ID.
1. Establecer propiedades de rotación 3D.
1. Guardar dibujo
#### **Ejemplo de programación de rotación 3D**
Use el siguiente código en su aplicación Java para configurar las propiedades de rotación 3D usando Aspose.Diagram for Java API.

**Java**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\TestTemplate.vsdx");

// get shape by ID and page name

Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(0);



// set 3D rotation properties

shape.getThreeDFormat().getRotationXAngle().setValue(2.61);

shape.getThreeDFormat().getRotationYAngle().setValue(2.61);

shape.getThreeDFormat().getRotationZAngle().setValue(3);

shape.getThreeDFormat().getRotationType().setValue(RotationTypeValue.PARALLEL);

shape.getThreeDFormat().getPerspective().setValue(0);

shape.getThreeDFormat().getDistanceFromGround().setValue(0);

shape.getThreeDFormat().getKeepTextFlat().setValue(BOOL.TRUE);

// save drawing

diagram.save("c:\\temp\\TestTemplate.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

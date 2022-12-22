---
title: Trabajando con Protección
type: docs
weight: 90
url: /es/python-java/working-with-protection/
---
## **Establecer Protección del Visio Diagram**
Protecting diagrams allow users to lock backgrounds, masters (stencils), shapes and styles so that they cannot be edited. This is useful for protecting corporate styles, for example, and ensure a consistent look across a set of diagrams. Developers can achieve this using Aspose.Diagram for Python via Java.

### **Editar Protección del Visio Diagram**
Los métodos getProtectBkgnds, getProtectMasters, getProtectShapes y getProtectStyles, expuestos por la clase DocumentSettings, admiten el objeto BoolValue. Estas propiedades se pueden utilizar para proteger y desproteger diagramas Microsoft Visio.

En el Microsoft Visio proteges los documentos de esta manera:

1. Abra un diagram en Microsoft Visio.
1. Abra la ventana Explorador de dibujos.
1.  Haga clic derecho en diagram y seleccione**Proteger documento** del menú.
1. En la ventana Proteger documento, marque o borre las opciones para bloquear o desbloquear diferentes elementos diagram.
1.  Hacer clic**OK**.

**Vea cómo podemos verificar o borrar opciones manualmente.** 

Use the code below in your application to perform the same tasks – lock and unlock different elements of your diagram – using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioDiagramProtection.py" >}}

### **Edite la protección de forma Visio**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.

 los**getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** y**obtenerAnchoBloqueo()** métodos expuestos por los**Proteccion** La clase admite el objeto BoolValue. Estos métodos se pueden utilizar para proteger o desproteger formas.

En Visio, debe realizar las siguientes acciones para proteger cualquier forma:

1. Abra un diagram en Microsoft Visio.
1. Seleccione una forma.
1.  Seleccione**Proteccion** desde el**Formato** menú (Visio 2007), o seleccione**Proteccion** desde el**Desarrollador** menú (Visio 2010).
1.  En el**Proteccion** ventana, seleccione o borre las opciones para bloquear o desbloquear el atributo de forma.
1.  Hacer clic**OK**.

**Las opciones de protección de una forma, como se ve en Microsoft Visio** 

Use the following code in your Java application to do the same thing (lock/unlock any shape attribute) using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioShapeProtection.py" >}}

---
title: Trabajando con Protección
type: docs
weight: 90
url: /es/python-java/working-with-protection/
---
## **Establecer Protección del Visio Diagram**
La protección de diagramas permite a los usuarios bloquear fondos, patrones (plantillas), formas y estilos para que no se puedan editar. Esto es útil para proteger los estilos corporativos, por ejemplo, y garantizar una apariencia coherente en un conjunto de diagramas. Los desarrolladores pueden lograr esto usando Aspose.Diagram para Python a través de Java.

### **Editar Protección del Visio Diagram**
Los métodos getProtectBkgnds, getProtectMasters, getProtectShapes y getProtectStyles, expuestos por la clase DocumentSettings, admiten el objeto BoolValue. Estas propiedades se pueden utilizar para proteger y desproteger diagramas Microsoft Visio.

En el Microsoft Visio proteges los documentos de esta manera:

1. Abra un diagram en Microsoft Visio.
1. Abra la ventana Explorador de dibujos.
1.  Haga clic derecho en diagram y seleccione**Proteger documento** del menú.
1. En la ventana Proteger documento, marque o borre las opciones para bloquear o desbloquear diferentes elementos diagram.
1.  Hacer clic**OK**.

**Vea cómo podemos verificar o borrar opciones manualmente.** 

Use el código a continuación en su aplicación para realizar las mismas tareas: bloquear y desbloquear diferentes elementos de su diagram, usando Aspose.Diagram para Python a través de Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioDiagramProtection.py" >}}

### **Edite la protección de forma Visio**
La protección de formas Visio permite a los usuarios bloquear aspectos específicos de las formas. Los aspectos de las formas que se pueden bloquear a través de la protección de formas incluyen el ancho, la altura, la posición x, la posición y, la rotación y más. Los desarrolladores pueden lograr esto usando Aspose.Diagram para Python a través de Java.

 los**getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** y**obtenerAnchoBloqueo()** métodos expuestos por los**Proteccion** La clase admite el objeto BoolValue. Estos métodos se pueden utilizar para proteger o desproteger formas.

En Visio, debe realizar las siguientes acciones para proteger cualquier forma:

1. Abra un diagram en Microsoft Visio.
1. Seleccione una forma.
1.  Seleccione**Proteccion** desde el**Formato** menú (Visio 2007), o seleccione**Proteccion** desde el**Desarrollador** menú (Visio 2010).
1.  En el**Proteccion** ventana, seleccione o borre las opciones para bloquear o desbloquear el atributo de forma.
1.  Hacer clic**OK**.

**Las opciones de protección de una forma, como se ve en Microsoft Visio** 

Use el siguiente código en su aplicación Java para hacer lo mismo (bloquear/desbloquear cualquier atributo de forma) usando Aspose.Diagram para Python a través de Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioShapeProtection.py" >}}

---
title: Работа с защитой
type: docs
weight: 90
url: /ru/python-java/working-with-protection/
---
## **Комплект защиты Visio Diagram**
Защитные диаграммы позволяют пользователям блокировать фоны, шаблоны (трафареты), формы и стили, чтобы их нельзя было редактировать. Это полезно, например, для защиты корпоративных стилей и обеспечения единообразного отображения набора диаграмм. Разработчики могут добиться этого, используя Aspose.Diagram вместо Python via Java.

### **Редактировать Защита Visio Diagram**
Методы getProtectBkgnds, getProtectMasters, getProtectShapes и getProtectStyles, предоставляемые классом DocumentSettings, поддерживают объект BoolValue. Эти свойства можно использовать для защиты и снятия защиты Microsoft Visio диаграмм.

В Microsoft Visio вы защищаете документы следующим образом:

1. Откройте diagram в Microsoft Visio.
1. Откройте окно обозревателя чертежей.
1.  Щелкните правой кнопкой мыши diagram и выберите**Защитить документ** из меню.
1. В окне «Защитить документ» установите или снимите флажки для блокировки или разблокировки различных элементов diagram.
1.  Нажмите**ХОРОШО**.

**Пожалуйста, посмотрите, как мы можем проверять или очищать параметры вручную.** 

Используйте приведенный ниже код в своем приложении для выполнения тех же задач — блокировки и разблокировки различных элементов вашего diagram — используя Aspose.Diagram для Python via Java.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load diagram
diagram = Diagram("ProtectAndUnprotect.vsd")

diagram.getDocumentSettings().setProtectBkgnds(BOOL.TRUE)
diagram.getDocumentSettings().setProtectMasters(BOOL.TRUE)
diagram.getDocumentSettings().setProtectShapes(BOOL.TRUE)
diagram.getDocumentSettings().setProtectStyles(BOOL.TRUE)

# save diagram
diagram.save("VisioDiagramProtection_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


### **Изменить защиту формы Visio**
Защита фигур Visio позволяет пользователям блокировать определенные аспекты фигур. Аспекты фигур, которые можно заблокировать с помощью защиты формы, включают ширину, высоту, положение x, положение y, поворот и многое другое. Разработчики могут добиться этого, используя Aspose.Diagram вместо Python via Java.

**получитьLockAspect()**, **получитьLockBegin()**, **получитьLockCalcWH()**, **получитьLockCrop()**, **получитьLockCustProp()**, **получитьблокировкуудалить()**, **получитьконец блокировки()**, **получить формат блокировки ()**, **getLockFromGroupFormat()**, **получитьгруппу блокировки()**, **получитьLockHeight()**, **получитьLockMoveX()**, **получитьLockMoveY()**, **получитьLockRotate()**, **получитьблокировкувыбрать()**, **получитьLockTextEdit()**, **получитьLockThemeColors()**, **getLockThemeEffects ()**, **получитьLockVtxEdit()** а также**получитьширину блокировки()** методы, раскрытые**Защита** класс поддерживает объект BoolValue. Эти методы можно использовать для защиты/снятия защиты фигур.

В Visio вам необходимо выполнить следующие действия для защиты любой формы:

1. Откройте diagram в Microsoft Visio.
1. Выберите форму.
1.  Выбирать**Защита** от**Формат** меню (Visio 2007) или выберите**Защита** от**Разработчик** меню (Visio 2010).
1.  в**Защита** выберите или снимите флажок, чтобы заблокировать или разблокировать атрибут формы.
1.  Нажмите**ХОРОШО**.

**Варианты защиты формы, как показано в Microsoft Visio** 

Используйте следующий код в своем приложении Java, чтобы сделать то же самое (заблокировать/разблокировать любой атрибут формы), используя Aspose.Diagram для Python via Java.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load diagram
diagram = Diagram("ProtectAndUnprotect.vsd")
# get page by name
page = diagram.getPages().getPage("Flow 1")
# get shape by ID
shape = page.getShapes().getShape(1)

# set protections
shape.getProtection().getLockAspect().setValue(BOOL.TRUE)
shape.getProtection().getLockBegin().setValue(BOOL.TRUE)
shape.getProtection().getLockCalcWH().setValue(BOOL.TRUE)
shape.getProtection().getLockCrop().setValue(BOOL.TRUE)
shape.getProtection().getLockCustProp().setValue(BOOL.TRUE)
shape.getProtection().getLockDelete().setValue(BOOL.TRUE)
shape.getProtection().getLockEnd().setValue(BOOL.TRUE)
shape.getProtection().getLockFormat().setValue(BOOL.TRUE)
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.TRUE)
shape.getProtection().getLockGroup().setValue(BOOL.TRUE)
shape.getProtection().getLockHeight().setValue(BOOL.TRUE)
shape.getProtection().getLockMoveX().setValue(BOOL.TRUE)
shape.getProtection().getLockMoveY().setValue(BOOL.TRUE)
shape.getProtection().getLockRotate().setValue(BOOL.TRUE)
shape.getProtection().getLockSelect().setValue(BOOL.TRUE)
shape.getProtection().getLockTextEdit().setValue(BOOL.TRUE)
shape.getProtection().getLockThemeColors().setValue(BOOL.TRUE)
shape.getProtection().getLockThemeEffects().setValue(BOOL.TRUE)
shape.getProtection().getLockVtxEdit().setValue(BOOL.TRUE)
shape.getProtection().getLockWidth().setValue(BOOL.TRUE)
        
# save diagram
diagram.save("VisioShapeProtection_Out.vdx", SaveFileFormat.VDX)
jpype.shutdownJVM()

{{< /highlight >}}


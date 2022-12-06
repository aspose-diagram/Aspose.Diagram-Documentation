---
title: Работа с защитой
type: docs
weight: 90
url: /ru/java/working-with-protection/
---
## **Комплект защиты Visio Diagram**
 Защитные диаграммы позволяют пользователям блокировать фоны, шаблоны (трафареты), формы и стили, чтобы их нельзя было редактировать. Это полезно, например, для защиты корпоративных стилей и обеспечения единообразного отображения набора диаграмм. Разработчики могут добиться этого, используя[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Редактировать Защита Visio Diagram**
 Методы getProtectBkgnds, getProtectMasters, getProtectShapes и getProtectStyles, предоставляемые[Настройки документа](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentSettings) класс поддерживает объект com.aspose.diagram.BoolValue. Эти свойства можно использовать для защиты и снятия защиты Microsoft Visio диаграмм.

В Microsoft Visio вы защищаете документы следующим образом:

1. Откройте diagram в Microsoft Visio.
1. Откройте окно обозревателя чертежей.
1.  Щелкните правой кнопкой мыши diagram и выберите**Защитить документ** из меню.
1. В окне «Защитить документ» установите или снимите флажки для блокировки или разблокировки различных элементов diagram.
1.  Нажмите**ХОРОШО**.

**Пожалуйста, посмотрите, как мы можем проверять или очищать параметры вручную.** 

![дело:изображение_альтернативный_текст](working-with-protection_1.png)

Используйте приведенный ниже код в приложении Java для выполнения тех же задач — блокировки и разблокировки различных элементов вашего diagram — с помощью Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioDiagramProtection-VisioDiagramProtection.java" >}}
### **Изменить защиту формы Visio**
 Защита фигур Visio позволяет пользователям блокировать определенные аспекты фигур. Аспекты фигур, которые можно заблокировать с помощью защиты формы, включают ширину, высоту, положение x, положение y, поворот и многое другое. Разработчики могут добиться этого, используя[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

**получитьLockAspect()**, **получитьLockBegin()**, **получитьLockCalcWH()**, **получитьLockCrop()**, **получитьLockCustProp()**, **получитьблокировкуудалить()**, **получитьконец блокировки()**, **получить формат блокировки ()**, **getLockFromGroupFormat()**, **получитьгруппу блокировки()**, **получитьLockHeight()**, **получитьLockMoveX()**, **получитьLockMoveY()**, **получитьLockRotate()**, **получитьблокировкувыбрать()**, **получитьLockTextEdit()**, **получитьLockThemeColors()**, **getLockThemeEffects ()**, **получитьLockVtxEdit()** а также**получитьширину блокировки()** методы, раскрытые[Защита](https://reference.aspose.com/diagram/java/com.aspose.diagram/Protection) класс поддерживает объект com.aspose.diagram.BoolValue. Эти методы можно использовать для защиты/снятия защиты фигур.

В Visio вам необходимо выполнить следующие действия для защиты любой формы:

1. Откройте diagram в Microsoft Visio.
1. Выберите форму.
1.  Выбирать**Защита** от**Формат** меню (Visio 2007) или выберите**Защита** от**Разработчик** меню (Visio 2010).
1.  в**Защита** выберите или снимите флажок, чтобы заблокировать или разблокировать атрибут формы.
1.  Нажмите**ХОРОШО**.

**Варианты защиты формы, как показано в Microsoft Visio** 

![дело:изображение_альтернативный_текст](working-with-protection_2.png)

Используйте следующий код в своем приложении Java, чтобы сделать то же самое (заблокировать/разблокировать любой атрибут формы), используя Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioShapeProtection-VisioShapeProtection.java" >}}

---
title: Защитите формы в Visio
type: docs
weight: 20
url: /ru/net/protect-shapes-in-visio/
---
Свойства LockAspect, LockBegin, LockCalcWH, LockCrop, LockCustProp, LockDelete, LockEnd, LockFormat, LockFromGroupFormat, LockGroup, LockHeight, LockMoveX, LockMoveY, LockRotate, LockSelect, LockTextEdit, LockThemeColors, LockThemeEffects, LockVtxEdit и LockWidth, предоставляемые классом Protection, поддерживают объект Aspose.Diagram.BoolValue . Эти свойства можно использовать для защиты/снятия защиты фигур.

В Visio вам необходимо выполнить следующие действия для защиты любой формы:

- Открыть diagram в MS Visio
- Выберите любую форму
- Выберите «Защита…» в меню «Формат», если вы используете Visio 2007, или выберите «Защита» в меню «Разработчик», если вы используете Visio 2010.
- В окне «Защита» установите или снимите флажок в любом текстовом поле, чтобы заблокировать или разблокировать любой атрибут формы.
- Нажмите «ОК»

Используйте следующий код в своем приложении .NET, чтобы сделать то же самое (заблокировать любой атрибут формы), используя Aspose.Diagram for .NET.

{{< highlight "csharp" >}}

 //Load diagram

Diagram diagram = new Diagram("ProtectShape.vsd");

Page page0 = diagram.Pages[0];

Shape shape = page0.Shapes[0];

shape.Protection.LockAspect.Value = BOOL.True;

shape.Protection.LockBegin.Value = BOOL.True;

shape.Protection.LockCalcWH.Value = BOOL.True;

shape.Protection.LockCrop.Value = BOOL.True;

shape.Protection.LockCustProp.Value = BOOL.True;

shape.Protection.LockDelete.Value = BOOL.True;

shape.Protection.LockEnd.Value = BOOL.True;

shape.Protection.LockFormat.Value = BOOL.True;

shape.Protection.LockFromGroupFormat.Value = BOOL.True;

shape.Protection.LockGroup.Value = BOOL.True;

shape.Protection.LockHeight.Value = BOOL.True;

shape.Protection.LockMoveX.Value = BOOL.True;

shape.Protection.LockMoveY.Value = BOOL.True;

shape.Protection.LockRotate.Value = BOOL.True;

shape.Protection.LockSelect.Value = BOOL.True;

shape.Protection.LockTextEdit.Value = BOOL.True;

shape.Protection.LockThemeColors.Value = BOOL.True;

shape.Protection.LockThemeEffects.Value = BOOL.True;

shape.Protection.LockVtxEdit.Value = BOOL.True;

shape.Protection.LockWidth.Value = BOOL.True;

diagram.Save("ProtectedShapesFile.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **Скачать пример кода**
- [Битбакет](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)

---
title: Aspose.Diagram Операции со шрифтами
type: docs
weight: 170
url: /ru/java/aspose-diagram-font-operations/
---
{{% alert color="primary" %}} 

Aspose.Diagram позволяет разработчикам устанавливать каталоги шрифтов для отображения в диаграммах Visio. В этой статье показано, как использовать шрифты из пользовательских каталогов.

{{% /alert %}} 
### **Работа со шрифтами**
#### **Где Aspose.Diagram ищет шрифты TrueType на Windows**
 Aspose.Diagram ищет шрифты в**Windows\Шрифты** папка. Этот параметр по умолчанию работает большую часть времени, поэтому указывайте свои собственные папки со шрифтами только в том случае, если вам это действительно нужно.
#### **Как явно указать папку со шрифтами**
 Aspose.Diagram API-интерфейсы предоставили метод setFontDirs для[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class, чтобы указать папки шрифтов, как описано ниже.

1. Метод Diagram.setFontDirs принимает массив строк в качестве параметра, поэтому разработчик может указать множество каталогов шрифтов, используя этот подход.

{{% alert color="primary" %}} 

При указании папки шрифтов с использованием вышеупомянутого подхода мы рекомендуем указывать расположение шрифта в начале приложения, иначе вы можете получить плохо отформатированные результаты.

{{% /alert %}} {{% alert color="primary" %}} 

Установка папки шрифтов с помощью любого из вышеперечисленных методов не гарантирует, что Aspose.Diagram API не будет искать шрифты в местах по умолчанию, таких как системная папка шрифтов.

{{% /alert %}} 

Демонстрирует, как настроить Aspose.Diagram для поиска шрифтов TrueType в нескольких папках при визуализации или внедрении шрифтов.
#### **Образец программирования**
В приведенном ниже примере кода показано, как настроить Aspose.Diagram для поиска шрифтов TrueType в нескольких папках при отображении или внедрении шрифтов.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SpecifyFontLocation.class);    

String[] fontDirs = new String[] { "C:\\MyFonts\\", "D:\\Misc\\Fonts\\" };
//Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//setting the custom font directories
diagram.setFontDirs(fontDirs);

//saving Visio diagram in PDF format
diagram.save(dataDir + "SetFontsFolders_Out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}

### **Получение уведомлений об отсутствующих шрифтах и замене шрифтов во время рендеринга**
Aspose.Diagram API требует доступа к точному шрифту для правильного отображения чертежа в формате PDF. Если требуемый шрифт недоступен на компьютере, то Aspose.Diagram API отображает любой экземпляр этого шрифта, используя шрифт по умолчанию или ближайший доступный шрифт на компьютере, поскольку эта замена может изменить внешний вид визуализированного чертежа, разработчикам может потребоваться уведомление об отсутствии шрифта и о том, каким шрифтом он будет заменен.
#### **Уведомление об отсутствующих шрифтах и пример программирования замены шрифтов**
Чтобы получать уведомления о замене шрифта во время рендеринга:

1. Создайте класс, реализующий[IWarningCallback](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)
1. Передайте его свойству PdfSaveOptions.setWarningCallback(com.aspose.diagram.IWarningCallback).

При сохранении чертежа экземпляр[IWarningCallback](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)вызывается, если есть какие-либо потенциальные проблемы с точностью воспроизведения рисунка. В этом случае мы выбираем обработку только предупреждений, связанных с заменой шрифта, и вывод предупреждения на экран. В приведенном ниже примере показано, как получать уведомления о замене шрифта с помощью[IWarningCallback](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback).

**Java**

{{< highlight "java" >}}

 // load the document to render.

Diagram diagram = new Diagram("C:\\temp\\Output.vsdx");


// initialize PdfSaveOptions object

com.aspose.diagram.PdfSaveOptions saveOp = new com.aspose.diagram.PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.setWarningCallback(callback);



// pass the save options along with the save path to the save method.

diagram.save("C:\\temp\\Rendering.MissingFontNotification Out.pdf", saveOp);

{{< /highlight >}}
#### **Реализация IWarningCallback**
Последним шагом является создание класса, реализующего[IWarningCallback](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)интерфейс. Этот класс выведет на консоль все предупреждения о замене шрифта. В приведенном ниже примере показано, как реализовать IWarningCallback для уведомления о любой замене шрифта во время сохранения документа.



**Java**

{{< highlight "java" >}}

 public class HandleDocumentWarnings implements IWarningCallback {

     /**

     * Our callback only needs to implement the "Warning" method. This method is

     * called whenever there is a potential issue during document processing.

     * The callback can be set to listen for warnings generated during document

     * load and/or document save.

     */

     public void warning(WarningInfo info) {

         // We are only interested in fonts being substituted.

         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION) {

         System.out.println("Font substitution: " + info.getDescription());

     }

 }

}

{{< /highlight >}}

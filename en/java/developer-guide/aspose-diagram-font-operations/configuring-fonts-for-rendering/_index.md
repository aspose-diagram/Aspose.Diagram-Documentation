---
title: Configuring Fonts for Rendering
type: docs
weight: 10
url: /java/configuring-fonts-for-rendering/
---

## **Possible Usage Scenarios**

Aspose.Diagram APIs provide the facility to render pages in image formats as well as convert them to PDF & XPS formats. In order to maximize the conversion fidelity, it is necessary that the fonts used in the page should be available in the operating system's default font directory. In case the required fonts are not present then the Aspose.Diagram APIs will try to substitute the required fonts with the ones available.

## **Selection of Fonts**

Below is the process that Aspose.Diagram APIs follow behind the scene.

1. The API tries to find the fonts on the file system matching the exact font name used in the spreadsheet.
1. If API cannot locate the font defined under **[SaveOptions.DefaultFont](https://reference.aspose.com/diagram/java/com.aspose.diagram/saveoptions/#setDefaultFont)** property, it attempts to use the font specified under **[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/java/com.aspose.diagram/fontconfigs/#setDefaultFontName)** property.
1. If API cannot locate the font defined under **[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/java/com.aspose.diagram/fontconfigs/#setDefaultFontName/)** property, it attempts to select the most suitable fonts from all of the available fonts.
1. Finally, if API cannot find any fonts on the file system, it renders the page using Times New Roman.

## **Set Custom Font Folders**

Aspose.Diagram APIs search the operating system's default font directory for the required fonts. In case the required fonts are not available in the system's font directory then the APIs search through the custom (user defined) directories. The **[FontConfigs](https://reference.aspose.com/diagram/java/com.aspose.diagram/fontconfigs/)** class has exposed a number of ways to set custom font directories as detailed below.

1. **[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/java/com.aspose.diagram/fontconfigs/#setFontFolder)**: This method is useful if there is only one folder to be set.

1. **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/java/com.aspose.diagram/fontconfigs/#setFontFolders/)**: This method is useful when the fonts reside in multiple folders and the user wishes to set all folders separately rather than combining all fonts in a single folder.
1. **[FontConfigs.SetFontSources](https://reference.aspose.com/diagram/java/com.aspose.diagram/fontconfigs/#setFontSources/)**: This method is useful when the user wishes to load fonts from multiple folders or a single font file or font data from an array of bytes.

{{% alert color="primary" %}}

Both **[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/java/com.aspose.diagram/fontconfigs/#setFontFolder/)** & **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/java/com.aspose.diagram/fontconfigs/#setFontFolders/)** methods accept a Boolean type second parameter. Passing **true** as the second parameter will direct the Aspose.Diagram APIs to search the subfolders for the fonts files.

{{% /alert %}}

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SpecifyFontLocation.class);    

com.aspose.diagram.FontConfigs.setFontFolder("C:\\Fonts\\", false);
//Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//saving Visio diagram in PDF format
diagram.save(dataDir + "SetFontsFolder_Out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
```

{{% alert color="primary" %}}

Please use any of the above-mentioned methods at the start of the application, that is; before invoking any other objects of Aspose.Diagram APIs.

{{% /alert %}} {{% alert color="primary" %}}

If all of the above-mentioned methods are used to set the font sources, only the last settings will take effect.

{{% /alert %}}


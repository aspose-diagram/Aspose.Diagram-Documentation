---
title: Configuración de fuentes para la representación
type: docs
weight: 10
url: /es/net/configuring-fonts-for-rendering/
---
## **Posibles escenarios de uso**

Aspose.Diagram Las API brindan la posibilidad de representar páginas en formatos de imagen y convertirlas a formatos PDF y XPS. Para maximizar la fidelidad de la conversión, es necesario que las fuentes utilizadas en la hoja de cálculo estén disponibles en el directorio de fuentes predeterminado del sistema operativo. En caso de que las fuentes requeridas no estén presentes, las API Aspose.Diagram intentarán sustituir las fuentes requeridas por las disponibles.

## **Selección de fuentes**

A continuación se muestra el proceso que siguen las API Aspose.Diagram detrás de escena.

1. El API intenta encontrar las fuentes en el sistema de archivos que coincidan con el nombre de fuente exacto utilizado en la hoja de cálculo.
1.  Si API no puede localizar la fuente definida en**[SaveOptions.DefaultFont](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/defaultfont/)** propiedad, intenta utilizar la fuente especificada en**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)**propiedad.
1.  Si API no puede localizar la fuente definida en**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)** propiedad, intenta seleccionar las fuentes más adecuadas de todas las fuentes disponibles.
1. Finalmente, si API no puede encontrar ninguna fuente en el sistema de archivos, representa la página usando Times New Roman.

## **Establecer carpetas de fuentes personalizadas**

 Aspose.Diagram Las API buscan en el directorio de fuentes predeterminado del sistema operativo las fuentes requeridas. En caso de que las fuentes requeridas no estén disponibles en el directorio de fuentes del sistema, las API buscan en los directorios personalizados (definidos por el usuario). los**[Configuraciones de fuentes](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/)** class ha expuesto varias formas de establecer directorios de fuentes personalizados como se detalla a continuación.

1. **[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)**: Este método es útil si solo hay una carpeta para configurar.

1. **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)**este método es útil cuando las fuentes residen en varias carpetas y el usuario desea configurar todas las carpetas por separado en lugar de combinar todas las fuentes en una sola carpeta.
1. **[FontConfigs.SetFontSources](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontsources/)**: este mecanismo es útil cuando el usuario desea cargar fuentes de varias carpetas o un solo archivo de fuentes o datos de fuentes de una matriz de bytes.

{{% alert color="primary" %}}

 Ambas cosas**[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)** & **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)** Los métodos aceptan un segundo parámetro de tipo booleano. Paso**verdadero** ya que el segundo parámetro dirigirá a las API Aspose.Diagram para buscar las subcarpetas de los archivos de fuentes.

{{% /alert %}}

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SetCustomFontFolders-SetCustomFontFolders.cs" >}}

{{% alert color="primary" %}}

Utilice cualquiera de los métodos mencionados anteriormente al inicio de la aplicación, es decir; antes de invocar cualquier otro objeto de las API Aspose.Diagram.

{{% /alert %}} {{% alert color="primary" %}}

Si se utilizan todos los métodos mencionados anteriormente para configurar las fuentes de fuente, solo tendrán efecto los últimos ajustes.

{{% /alert %}}


---
title: Licencia
type: docs
weight: 50
url: /es/net/licensing/
description: Aspose. Diagram for .NET invita a sus clientes a obtener una licencia Clásica y una Licencia Medida. Así como utilizar una licencia limitada para explorar mejor el producto.
---
## **Evaluar Aspose.Diagram**
Puede descargar fácilmente el producto Aspose.Diagram for .NET con fines de evaluación. por favor refiérase a[Aspose.Diagram for .NET página de descarga](https://www.nuget.org/packages/Aspose.Diagram/)para conocer la última versión. La descarga de evaluación es la misma que la descarga comprada. La versión de evaluación simplemente obtiene la licencia cuando agrega unas pocas líneas de código para aplicar la licencia.

La versión de evaluación de Aspose.Diagram (sin una licencia especificada) brinda una funcionalidad completa del producto, pero inserta una marca de agua de evaluación en el medio del documento al abrir y guardar, y se limita a leer solo las primeras diez formas de la primera página de su Visio diagram .

![todo:imagen_alternativa_texto](licensing_1.png)
### **Limitaciones de la versión de evaluación**
La versión de evaluación proporciona todas las características excepto las siguientes:

- Solo puede leer las primeras diez formas de la primera página de Visio diagram.
- También verá una marca de agua de evaluación en imágenes exportadas y archivos PDF.

{{% alert color="primary" %}} 

 Si desea probar Aspose.Diagram sin limitaciones de evaluación, solicite una licencia temporal de 30 días. Por favor refiérase a[¿Cómo obtener una Licencia Temporal?](https://purchase.aspose.com/temporary-license) para más información.

{{% /alert %}} 
## **Aplicar una licencia**
Una vez que esté satisfecho con su[evaluación](https://downloads.aspose.com/diagram/net) de Aspose.Diagram for .NET, compre una licencia en el sitio web Aspose:[Portal de Compra](https://purchase.aspose.com/buy) . Familiarícese con los diferentes tipos de licencia disponibles. Si tienes alguna pregunta,[póngase en contacto con el equipo de ventas Aspose](https://about.aspose.com/contact) y estarán encantados de ayudarte.

Cada licencia Aspose incluye una suscripción de un año para actualizaciones gratuitas a cualquier nueva versión o corrección que surja durante este tiempo. Brindamos soporte técnico gratuito e ilimitado a usuarios con licencia y evaluación.

La licencia es un archivo XML de texto sin formato que contiene detalles como el nombre del producto, la cantidad de desarrolladores con licencia, la fecha de vencimiento de la suscripción, etc. El archivo está firmado digitalmente, así que no lo modifique: incluso agregar un salto de línea adicional al archivo lo invalida.
### **Cuándo aplicar una licencia**
Siga estas sencillas reglas:

- La licencia solo debe establecerse una vez por dominio de aplicación.
- Debe configurar la licencia antes de usar cualquier otra clase Aspose.Diagram.
- Llamar a SetLicense varias veces no es dañino, pero desperdicia tiempo de procesador.
- Si está desarrollando una aplicación de consola o formularios Windows, llame a SetLicense en el código de inicio, antes de usar las clases Aspose.Diagram.
- Al desarrollar una aplicación ASP.NET, llame a SetLicense desde el archivo Global.asax.cs, en el método protegido Aplication_Start. Se llama una vez cuando se inicia la aplicación.
- No llame a SetLicense desde dentro de los métodos Page_Load, ya que significa que la licencia se cargará cada vez que se cargue una página web.
- Si está desarrollando una biblioteca de clases, llame a SetLicense desde un constructor estático de la clase que usa Aspose.Diagram. El constructor estático se ejecuta antes de que se cree una instancia de su clase, asegurándose de que la licencia Aspose.Diagram esté configurada correctamente.
### **Aplicar licencia usando archivo o objeto de transmisión**
 Utilizar el[Licencia.SetLicense](https://reference.aspose.com/diagram/net/aspose.diagram/license)para obtener la licencia del componente. La forma más fácil de configurar una licencia es colocar el archivo de licencia en la misma carpeta que Aspose.Diagram.dll y especificar el nombre del archivo, sin ruta, como se muestra a continuación.
#### **Cargar una licencia desde un archivo**
Este fragmento de código inicializa una licencia almacenada en un archivo o en un recurso incrustado.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-ApplyLicense-ApplyLicenseByPath-ApplyLicenseByPath.cs" >}}
#### **Cargar una licencia desde un objeto de flujo**
Estos fragmentos de código inicializan la licencia de la transmisión.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-ApplyLicense-ApplyLicenseUsingFileStream-ApplyLicenseUsingFileStream.cs" >}}
## **Aplicar licencia medida**
Aspose.Diagram for .NET API permite a los desarrolladores aplicar una licencia medida. Es un nuevo mecanismo de licencia. El nuevo mecanismo de concesión de licencias se utilizará junto con el método de concesión de licencias existente. Aquellos clientes que deseen que se les facture en función del uso de las funciones API pueden utilizar la licencia medida. Para obtener más detalles, consulte[Preguntas frecuentes sobre licencias medidas](https://purchase.aspose.com/faqs/licensing/metered)sección.

una nueva clase[medido](https://reference.aspose.com/diagram/net/aspose.diagram/metered)se ha agregado para aplicar la clave medida. Este ejemplo de código demuestra cómo establecer claves públicas y privadas medidas:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-ApplyLicense-PublicAndPrivateKeys-PublicAndPrivateKeys.cs" >}}

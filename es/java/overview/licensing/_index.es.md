---
title: Licencia
type: docs
weight: 60
url: /es/java/licensing/
---
## **Limitaciones de la versión de evaluación**
 Se puede descargar una versión de evaluación gratuita de Aspose.Diagram for Java desde[Aspose Repositorio](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram).
### **Limitación**
La versión de evaluación proporciona todas las características excepto las siguientes:

- Solo puede leer las primeras diez formas de la primera página de su archivo VSD.
- You will also see evaluation watermark in exoprted images and PDF files.

 Si desea probar Aspose.Diagram sin limitaciones de evaluación, solicite una licencia temporal de 30 días. Por favor refiérase a[¿Cómo obtener una Licencia Temporal?](https://purchase.aspose.com/temporary-license) para más información.
## **Aplicar una licencia**
 Puede descargar una versión de evaluación de**Aspose.Diagram** for Java desde[Aspose Repositorio](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram). La versión de evaluación proporciona absolutamente las mismas capacidades que la versión con licencia del producto. Además, la versión de evaluación simplemente obtiene la licencia cuando compra una licencia y agrega un par de líneas de código para aplicar la licencia.

 Una vez que esté satisfecho con su evaluación de**Aspose.Diagram** , puedes[comprar una licencia](https://purchase.aspose.com/buy) en el sitio web Aspose. Familiarícese con los diferentes tipos de suscripción que se ofrecen. Si tiene alguna pregunta, no dude en ponerse en contacto con el equipo de ventas Aspose.

Cada licencia Aspose incluye una suscripción de un año para actualizaciones gratuitas a cualquier nueva versión o corrección que surja durante este tiempo. El soporte técnico es gratuito e ilimitado y se proporciona tanto a usuarios con licencia como a usuarios de evaluación.

{{% alert color="primary" %}} 

 Si quieres probar**Aspose.Diagram** sin limitaciones de versión de evaluación, solicite una licencia temporal de 30 días. Por favor refiérase a[¿Cómo obtener una Licencia Temporal?](https://purchase.aspose.com/temporary-license) para más información.

{{% /alert %}} 
### **Configuración de una licencia**
La licencia es un archivo XML de texto sin formato que contiene detalles como el nombre del producto, la cantidad de desarrolladores para los que tiene licencia, la fecha de vencimiento de la suscripción, etc. El archivo está firmado digitalmente, así que no modifique el archivo; incluso la adición inadvertida de un salto de línea adicional en el archivo lo invalidará.

Debe solicitar una licencia antes de realizar cualquier operación con documentos. Asegúrese de hacer esto antes de crear un objeto Diagram. Solo debe establecer una licencia una vez por aplicación o proceso.

La licencia se puede cargar desde un flujo o archivo en las siguientes ubicaciones:

1. Camino explícito.
1. La carpeta que contiene el Aspose.Diagram.jar.

 Utilizar el[Licencia.setLicense()](https://reference.aspose.com/diagram/java/com.aspose.diagram/License) para obtener la licencia del componente. A menudo, la forma más fácil de configurar una licencia es colocar el archivo de licencia en la misma carpeta que Aspose.Diagram.jar y especificar solo el nombre del archivo sin la ruta, como se muestra en el siguiente ejemplo:
#### **Ejemplo 1**
 En este ejemplo**Aspose.Diagram** intentará encontrar el archivo de licencia en la carpeta que contiene los archivos JAR de su aplicación.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense("Aspose.Diagram.Java.lic");

{{< /highlight >}}
#### **Ejemplo 2**
Inicializa una licencia de una secuencia.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense(new java.io.FileInputStream("Aspose.Diagram.Java.lic"));

{{< /highlight >}}
### **Validar la Licencia**
 Es posible validar si la licencia se ha configurado correctamente o no. los[Licencia](https://reference.aspose.com/diagram/java/com.aspose.diagram/License)class tiene el campo isLicensed que devolverá verdadero si la licencia se ha configurado correctamente.

**Java**

{{< highlight "csharp" >}}

 License license = new License();

license.setLicense("Aspose.Diagram.Java.lic");

if (License.isLicensed()) {

    System.out.println("License is Set!");

}

{{< /highlight >}}
## **Aplicar licencia medida**
Aspose.Diagram for Java API permite a los desarrolladores aplicar una licencia medida. Es un nuevo mecanismo de licencia. El nuevo mecanismo de concesión de licencias se utilizará junto con el método de concesión de licencias existente. Aquellos clientes que deseen que se les facture en función del uso de las funciones API pueden utilizar la licencia medida. Para obtener más detalles, consulte[Preguntas frecuentes sobre licencias medidas](https://purchase.aspose.com/faqs/licensing/metered)sección.

una nueva clase[medido](https://reference.aspose.com/diagram/java/com.aspose.diagram/Metered) se ha agregado para aplicar la clave medida. Este ejemplo de código demuestra cómo establecer claves públicas y privadas medidas:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// Initialize a Metered license class object
Metered metered = new Metered();
// apply public and private keys
metered.setMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}
```

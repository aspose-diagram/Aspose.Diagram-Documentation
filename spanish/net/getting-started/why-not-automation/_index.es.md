﻿---
title: ¿Por qué no la automatización?
type: docs
weight: 40
url: /es/net/why-not-automation/
description: Esta página describe por qué no la automatización.
---
{{% alert color="primary" %}} 

¿Por qué los componentes Aspose son una opción mucho mejor que la automatización Microsoft Office?*

Hay dos preguntas que escuchamos con más frecuencia aquí en Aspose:

1. **¿Sus productos requieren la instalación de Microsoft Office para que funcionen?** 
La respuesta simple es no. Los componentes de Aspose son totalmente independientes y no están afiliados, autorizados, patrocinados ni aprobados de otro modo por Microsoft Corporation.
1. **¿Por qué deberíamos usar los productos Aspose en lugar de utilizar la automatización Microsoft Office?** 
 La respuesta más corta que podemos dar es que hay muchas razones, siendo la principal que Microsoft recomienda encarecidamente contra Office la automatización de las soluciones de software:[Consideraciones para la automatización del lado del servidor de Office](http://support.microsoft.com/default.aspx?scid=kb;EN-US;q257757).

{{% /alert %}} 
## **¿Por qué no la automatización?**
Hay varias razones por las que los componentes Aspose son una mejor alternativa a la automatización. A continuación se describen algunos de los puntos clave. Además, asegúrese de visitar los enlaces al final de esta sección.
### **Seguridad**
La siguiente es una cita directa del artículo Microsoft mencionado anteriormente:

*"Office Las aplicaciones nunca fueron diseñadas para usarse en el lado del servidor y, por lo tanto, no tienen en cuenta los problemas de seguridad que enfrentan los componentes distribuidos. Office no autentica las solicitudes entrantes y no lo protege de ejecutar macros involuntariamente o iniciar otro servidor que pueden ejecutar macros, desde su código del lado del servidor. ¡No abra archivos que se cargan en el servidor desde una Web anónima! Según la configuración de seguridad que se estableció por última vez, el servidor puede ejecutar macros en un contexto de Administrador o Sistema con total privilegios y comprometer su red! Además, Office utiliza muchos componentes del lado del cliente (como Simple MAPI, WinInet y MSDAIPP) que pueden almacenar en caché la información de autenticación del cliente para acelerar el procesamiento. Si Office se está automatizando del lado del servidor, uno la instancia puede atender a más de un cliente, y debido a que la información de autenticación se ha almacenado en caché para esa sesión, es posible que un cliente pueda usar el caché ed credenciales de otro cliente y, por lo tanto, obtener permisos de acceso no otorgados haciéndose pasar por otros usuarios".*

Los productos Aspose son muy seguros. Los componentes Aspose se ejecutan en el mismo contexto de usuario que todas las aplicaciones ASP.NET, bajo el usuario ASPNET. Por lo tanto, los componentes Aspose no representan un riesgo potencial para los recursos vitales del sistema. Además, cuando un componente Aspose abre un documento, las macros no se ejecutan automáticamente. Los componentes Aspose se crearon con el objetivo de permitir a los desarrolladores crear, manipular y guardar archivos Office. Ninguno de los riesgos asociados con el paquete Microsoft Office son inherentes a los componentes Aspose.
### **Estabilidad**
La siguiente es una cita directa del artículo Microsoft mencionado anteriormente:

*"Office 2000, Office XP y Office 2003 usan la tecnología Microsoft Windows Installer (MSI) para facilitar la instalación y la reparación automática para un usuario final. MSI presenta el concepto de "instalación en el primer uso", que permite que las características se instalen dinámicamente o configurado en tiempo de ejecución (para el sistema, o más a menudo para un usuario en particular). En un entorno del lado del servidor, esto ralentiza el rendimiento y aumenta la probabilidad de que aparezca un cuadro de diálogo que solicite al usuario que apruebe la instalación o proporcione un disco de instalación apropiado. Aunque está diseñado para aumentar la resistencia de Office como un producto de usuario final, la implementación de las capacidades de MSI de Office es contraproducente en un entorno del lado del servidor. Además, la estabilidad de Office en general no se puede garantizar cuando se ejecuta en el servidor. -lado porque no ha sido diseñado o probado para este tipo de uso. El uso de Office como un componente de servicio en un servidor de red puede reducir la estabilidad de esa máquina y como una consecuencia de su red en su conjunto. Si planea automatizar Office del lado del servidor, intente aislar el programa en una computadora dedicada que no pueda afectar las funciones críticas y que pueda reiniciarse según sea necesario".*

Dado que los componentes Aspose están empaquetados en una sola DLL, nunca será necesario instalar piezas o piezas adicionales para que funcionen. Los componentes Aspose solo los utilizan las aplicaciones .NET y no hay ninguna parte del código del componente diseñada para esperar una respuesta humana. Los componentes Aspose se han probado exhaustivamente. Los componentes Aspose son utilizados por empresas como IBM, Hilton, Reader's Digest, Bank of America y muchas más.
### **Escalabilidad/Velocidad**
La siguiente es una cita directa del artículo Microsoft mencionado anteriormente:

*"Los componentes del lado del servidor deben ser componentes COM de subprocesos múltiples y altamente reentrantes con una sobrecarga mínima y un alto rendimiento para múltiples clientes. Office Las aplicaciones son en casi todos los aspectos exactamente lo contrario. diseñado para proporcionar una funcionalidad diversa pero que consume muchos recursos para un solo cliente. Ofrecen poca escalabilidad como una solución del lado del servidor y tienen límites fijos para elementos importantes, como la memoria, que no se pueden cambiar a través de la configuración. Más importante aún, utilizan global recursos (como archivos asignados a la memoria, complementos o plantillas globales y servidores de automatización compartidos), que pueden limitar la cantidad de instancias que pueden ejecutarse simultáneamente y generar condiciones de carrera si se configuran en un entorno multicliente. planee ejecutar más de una instancia de cualquier aplicación Office al mismo tiempo, debe considerar "agrupar" o serializar el acceso a la aplicación Office para evitar problemas interbloqueos iniciales o corrupción de datos".*

Los componentes Aspose son altamente escalables y ultrarrápidos. Las aplicaciones Office no fueron diseñadas para ser utilizadas simultáneamente por cientos y miles de usuarios; sin embargo, los componentes Aspose están diseñados precisamente para eso. Nuestros componentes son una verdadera solución .NET y funcionan a la perfección, ya sea en un solo servidor que alimenta una sola aplicación o en una granja web con equilibrio de carga que impulsa una aplicación de toda la empresa.
### **Precio**
 Cuando una aplicación utiliza la automatización Microsoft Office, se debe comprar una copia de Microsoft Office para cada máquina que ejecuta la aplicación. Hay muchas veces que una aplicación puede necesitar crear o manipular un archivo office, pero no requiere que el usuario tenga Office. Aspose ofrece una muy[económico](https://purchase.aspose.com/buy), libre de regalías, licencia de redistribución que permitirá la implementación a un número ilimitado de usuarios sin preocupaciones de licencia.

Al crear aplicaciones basadas en web, es importante saber que los componentes de automatización Microsoft Office no tienen precio ni licencia para soluciones del lado del servidor ([Licencias de Office 2000 Web Components y Office Server Extensions](http://support.microsoft.com/default.aspx?scid=kb;EN-US;q243006)); por lo tanto, no existe una buena solución de licencia para implementar aplicaciones web que utilicen los componentes Microsoft Office. Aspose también ofrece una solución muy rentable para aplicaciones basadas en servidor.
### **Características**
 Los componentes Aspose brindan todo lo necesario para administrar archivos Office y mucho, mucho más. Están diseñados con la filosofía de permitir que los desarrolladores logren los mejores resultados con la menor cantidad de trabajo. A diferencia de la automatización Office, los componentes Aspose proporcionan muchas funciones potentes que ahorran tiempo. Por ejemplo,[Aspose.Diagram](https://products.aspose.com/diagram/net/) ofrece a los desarrolladores la capacidad de crear, leer, escribir, exportar, imprimir, acceder y proteger Visio diagram y sus formas también.[cada componente](https://products.aspose.com/total/) en la familia Aspose ofrece su propio conjunto de funciones únicas y potentes.

La mejor parte de comprar un componente Aspose o un conjunto de componentes es tener acceso a nuestros equipos de desarrollo. Nuestros equipos de desarrollo se dan cuenta de que si hay una función que su empresa necesita, lo más probable es que otras empresas también la necesiten. Si bien no se pueden agregar todas las solicitudes de funciones, nuestros equipos intentan ser muy abiertos y flexibles al brindar asistencia. Esa mentalidad es lo que ha ayudado a los componentes Aspose a volverse tan poderosos como son. Si hay características adicionales que necesita de los objetos de automatización Office, sus posibilidades de que se agreguen son muy, muy bajas.
### **Conclusión**
{{% alert color="primary" %}} 

 Si bien este artículo ha cubierto muchos de los puntos clave por los que los componentes Aspose son una mejor opción que la automatización Office, hay muchos, muchos más. Este artículo aborda principalmente solo los puntos más importantes. Todos los diferentes componentes de Aspose ofrecen un servicio libre de riesgos y sin compromiso[Versión de evaluación](https://www.nuget.org/packages/Aspose.Diagram/)Lo alentamos a que aproveche esa Evaluación para ver mejor lo que Aspose puede hacer por sus aplicaciones.

{{% /alert %}}

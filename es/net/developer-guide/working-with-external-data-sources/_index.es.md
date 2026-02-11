---
title: Trabajar con orígenes de datos externos
type: docs
weight: 200
url: /es/net/working-with-external-data-sources/
description: Esta sección explica cómo trabajar con fuentes de datos externas con Aspose.Diagram.
---
## **Editar conexión de datos de SQL Server y actualizar conjuntos de registros**
Aspose.Diagram API permite a los usuarios editar la conexión de datos de SQL Server y actualizar todos los conjuntos de registros. Para traer datos al dibujo Visio, necesitamos acceso a los datos de SQL Server. Asegúrese de que la base de datos no esté abierta en modo exclusivo.
### **Actualizar conexión de datos y conjuntos de registros**
 Ahora es un fenómeno común vincular los datos de los diagramas Microsoft Visio de las fuentes de datos externas. los[DataConnectionCollectionDataConnectionCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection) La clase contiene todas las conexiones de datos.
#### **Ejemplo de programación**
El siguiente fragmento de código edita una conexión de datos en particular y también actualiza todos los conjuntos de registros disponibles en Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ExternalDataSources();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
// Set connecting string
diagram.DataConnections[0].ConnectionString = "Data Source=MyServer;Initial Catalog=MyDB;Integrated Security=True";
// Set command
diagram.DataConnections[0].Command = "SELECT * from Project with(nolock)";
// Refresh all record sets
diagram.Refresh();
// Save Visio diagram
diagram.Save(dataDir + "EditDataConAndRefreshRecords_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}


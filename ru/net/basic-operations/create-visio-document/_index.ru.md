---
title: Создать документ Visio программно
linktitle: Создать документ Visio
type: docs
weight: 10
url: /ru/net/create-visio-document/
description: На этой странице описывается, как создать документ Visio с нуля с помощью библиотеки Aspose.Diagram.
---
## **Создание нового чертежа Visio**
Aspose.Diagram for .NET позволяет читать и создавать Microsoft Visio диаграммы из ваших собственных приложений без автоматизации. Первым шагом при создании новых документов является создание diagram. Затем добавьте формы и соединители, чтобы создать diagram.
## **Создать Visio Пример программирования чертежей**
В приведенном ниже коде показано создание нового чертежа Microsoft Visio. Обратите внимание, что пустой чертеж содержит одну пустую страницу.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


{{% alert color="primary" %}} 

Размер бумаги для рисования по умолчанию — Letter.

{{% /alert %}} 


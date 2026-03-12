---
title: Add PDF Bookmarks
type: docs
weight: 10
url: /net/add-pdf-bookmarks/
ai_search_scope: diagram_net
ai_search_endpoint: "https://docsearch.api.aspose.cloud/ask"
---

{{% alert color="primary" %}}

This article provides information on how to insert PDF bookmarks when converting a spreadsheet to PDF.

Aspose.Diagram allows you to add bookmarks on the fly. PDF bookmarks can drastically improve the navigability of long documents. When adding bookmark links to a PDF document, you can have precise control over the exact view you want, and you're not limited to linking to a page. You can set up the precise view by positioning the target page, and then create the bookmark.

{{% /alert %}}

Please see the following sample code to find out how to add PDF bookmarks. The code read diagram, specifies PDF bookmarks with destination locations and generates the PDF file.

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance PDF save options class
Aspose.Diagram.Saving.PdfSaveOptions options = new Aspose.Diagram.Saving.PdfSaveOptions();

// Create a main PDF Bookmark entry object
Aspose.Diagram.Saving.PdfBookmarkEntry pbeRoot = new Aspose.Diagram.Saving.PdfBookmarkEntry();
// Specify its text
pbeRoot.Text = "1.vsdx";
// Set the destination page
pbeRoot.Destination = diagram.Pages[0];
//pbeRoot.IsOpen = true;
// Set its sub entry array list
pbeRoot.SubEntry = new ArrayList();
// Create a sub PDF Bookmark entry object
Aspose.Diagram.Saving.PdfBookmarkEntry subPbe2 = new Aspose.Diagram.Saving.PdfBookmarkEntry();
// Specify its text
subPbe2.Text = "Page 1";
// Set its destination
subPbe2.Destination = diagram.Pages[1];
// Add the object to the main PDF root object
pbeRoot.SubEntry.Add(subPbe2);
// Set the PDF Bookmark root object
options.Bookmark = pbeRoot;
// save Visio drawing
diagram.Save(dataDir + "out.pdf", options);

{{< /highlight >}}

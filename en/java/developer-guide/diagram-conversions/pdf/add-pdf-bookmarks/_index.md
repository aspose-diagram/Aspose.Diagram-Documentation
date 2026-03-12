---
title: Add PDF Bookmarks
type: docs
weight: 10
url: /java/add-pdf-bookmarks/
ai_search_scope: diagram_java
ai_search_endpoint: "https://docsearch.api.aspose.cloud/ask"
---

{{% alert color="primary" %}}

This article provides information on how to insert PDF bookmarks when converting a spreadsheet to PDF.

Aspose.Diagram allows you to add bookmarks on the fly. PDF bookmarks can drastically improve the navigability of long documents. When adding bookmark links to a PDF document, you can have precise control over the exact view you want, and you're not limited to linking to a page. You can set up the precise view by positioning the target page, and then create the bookmark.

{{% /alert %}}

Please see the following sample code to find out how to add PDF bookmarks. The code read diagram, specifies PDF bookmarks with destination locations and generates the PDF file.

{{< highlight java >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

PdfSaveOptions options = new PdfSaveOptions();
// Create a main PDF Bookmark entry object
PdfBookmarkEntry pbeRoot = new PdfBookmarkEntry();
// Specify its text
pbeRoot.setText("1.vsdx");
// Set the destination page
pbeRoot.setDestination(diagram.getPages().get(0));
pbeRoot.setOpen(true);
// Set its sub entry array list
pbeRoot.setSubEntry(new ArrayList());
// Create a sub PDF Bookmark entry object
PdfBookmarkEntry subPbe2 = new PdfBookmarkEntry();
// Specify its text
subPbe2.setText("Page 1");
// Set its destination
subPbe2.setDestination(diagram.getPages().get(1));
// Add the object to the main PDF root object
pbeRoot.getSubEntry().add(subPbe2);
// Set the PDF Bookmark root object
options.setBookmark(pbeRoot);
diagram.save(dataDir + "out.pdf", options);

{{< /highlight >}}

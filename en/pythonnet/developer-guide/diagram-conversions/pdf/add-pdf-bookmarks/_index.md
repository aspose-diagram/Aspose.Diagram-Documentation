---
title: Add PDF Bookmarks
type: docs
weight: 10
url: /python-net/add-pdf-bookmarks/
---

{{% alert color="primary" %}}

This article provides information on how to insert PDF bookmarks when converting a spreadsheet to PDF.

Aspose.Diagram allows you to add bookmarks on the fly. PDF bookmarks can drastically improve the navigability of long documents. When adding bookmark links to a PDF document, you can have precise control over the exact view you want, and you're not limited to linking to a page. You can set up the precise view by positioning the target page, and then create the bookmark.

{{% /alert %}}

Please see the following sample code to find out how to add PDF bookmarks. The code read diagram, specifies PDF bookmarks with destination locations and generates the PDF file.

{{< highlight python >}}

// call the diagram constructor to load diagram from a VSD file
Diagram vsdDiagram = Diagram("Drawing1.vsd")

options = PdfSaveOptions()
#// Create a main PDF Bookmark entry object
pbeRoot = PdfBookmarkEntry()
#// Specify its text
pbeRoot.text = "1.vsdx"
#// Set the destination page
pbeRoot.destination = vsdDiagram.pages[0]
#//pbeRoot.IsOpen = true;
#// Set its sub entry array list
pbeRoot.sub_entry = []
#// Create a sub PDF Bookmark entry object
subPbe2 = PdfBookmarkEntry()
#// Specify its text
subPbe2.text = "Page 1"
#// Set its destination
subPbe2.destination = vsdDiagram.pages[1]
#// Add the object to the main PDF root object
pbeRoot.sub_entry.append(subPbe2)
#// Set the PDF Bookmark root object
options.bookmark = pbeRoot

#// Save as PDF
vsdDiagram.save(os.path.join(outputDir, "out.pdf"), options)

{{< /highlight >}}

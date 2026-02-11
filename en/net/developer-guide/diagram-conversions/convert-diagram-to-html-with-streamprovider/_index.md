---
title: Convert Diagram To Html With Streamprovider
type: docs
weight: 970
url: /net/convert-diagram-to-html-with-streamprovider/
description: This section explains how to convert Diagram To html With Streamprovider.
---

## **Possible Usage Scenarios**

When converting visio files which contain iamges and shapes to html files, we offen face the following two issues:

1.Where should we save the images and shapes when saving visio file to html stream.
2.Replace the default path with excepted path.

This article explains how to implement IStreamProvider interface for setting the HTMLSaveOptions.StreamProvider property. By implementing this interface, you will be able to save the created resources during HTML generation to your specific locations or memory streams.

This is the main code showing the usage of HTMLSaveOptions.StreamProvider property

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
string outputDir = dataDir + @"output\";
// Create digaram
Diagram diagram = new Diagram(dataDir + "sample.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions options = new HTMLSaveOptions();
options.StreamProvider = new ExportStreamProvider(outputDir);

// Save into .html using HTMLSaveOptions 
diagram.Save(dataDir + "output_out.html", options);

{{< /highlight >}}
```

Here is the code for ExportStreamProvider class which implements IStreamProvider interface used inside the above code.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
public class ExportStreamProvider : IStreamProvider
{
    private string outputDir;

    public ExportStreamProvider(string dir)
    {
        outputDir = dir;
    }

    public void InitStream(StreamProviderOptions options)
    {
        string path = outputDir + Path.GetFileName(options.DefaultPath);
        options.CustomPath = path;
        Directory.CreateDirectory(Path.GetDirectoryName(path));
        options.Stream = File.Create(path);
    }

    public void CloseStream(StreamProviderOptions options)
    {
        if (options != null && options.Stream != null)
        {
            options.Stream.Close();
        }
    }
}
{{< /highlight >}}
```



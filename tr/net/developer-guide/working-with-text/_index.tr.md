---
title: Metinle Çalışmak
type: docs
weight: 90
url: /tr/net/working-with-text/
description: Bu bölüm, Aspose.Diagram ile bir metin şeklinin nasıl ekleneceğini veya şeklin metninin nasıl güncelleneceğini açıklar.
---
## **Visio Sayfasına Metin Şekli Ekleme**
 Aspose.Diagram API, geliştiricilerin Visio sayfasında herhangi bir yere bir metin şekli eklemesine olanak tanır. Bunu başarmak için, AddText yöntemi[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) sınıf, PinX, PinY, genişlik, yükseklik ve metin parametrelerini alır.
### **Bir Metin Şekli Programlama Örneği Ekleme**
Aşağıdaki kod parçası, Visio diagram'de bir metin şekli ekler.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Create a new diagram
Diagram diagram = new Diagram();
// Set parameters and add text to a Visio page
double PinX = 1, PinY = 1, Width = 1, Height = 1;                  
diagram.Pages[0].AddText(PinX, PinY, Width, Height, "Test text");
// Save diagram 
diagram.Save(dataDir + "InsertTextShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Güncelleme Visio Şekil Metni**
 Birlikte[diyagramlar oluşturma](/diagram/tr/net/load-or-create-a-visio-drawing/) , Aspose.Diagram for .NET, şekillerle farklı şekillerde çalışmanızı sağlar. Bu makalede, şekillerdeki metne nasıl erişileceği ve bu metnin nasıl güncelleneceği ele alınmaktadır. Tarafından sunulan Text özelliği[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıfı, Aspose.Diagram.Text nesnesini destekler. Özellik, bir şeklin metnini almak veya güncellemek için kullanılabilir. Bir şeklin metnini güncelleme işlemi basittir:

1. diagram yükleyin.
1. Belirli bir şekil bulun.
1. Yeni metni ayarlayın.
1. diagram'i kaydedin.
### **Shape Text Programlama Örneği Güncelleme**
Aşağıdaki kod parçası bir şeklin metnini günceller. Şekiller kimlikleri ile tanımlanır. Aşağıdaki kod parçaları, işlem adı verilen ve kimliği 1 olan bir şekli arar ve metnini değiştirir.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Find a particular shape and update its text
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.Text.Value.Clear();
        shape.Text.Value.Add(new Txt("New Text"));
    }
}
// Save diagram
diagram.Save(dataDir + "UpdateShapeText_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Visio Şekline Yerleşik veya Özel Stil Sayfası Uygulayın**
Microsoft Visio stil sayfaları, tutarlı bir görünüm ve his için şekillere uygulanabilen biçimlendirme bilgilerini saklar. Aspose.Diagram for .NET, bir uygulamanın içinden stil sayfaları uygulamanıza olanak tanır.

 tarafından sunulan TextStyle, FillStyle ve LineStyle özellikleri[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) sınıf desteği[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) nesne. Özellik, stil bilgilerini almak ve bir diagram'e özel metin, çizgi ve dolgu stilleri uygulamak için kullanılabilir.
### **Microsoft Visio'deki Özel Stiller**
Microsoft Visio'deki şekillere özel stiller uygulamak için:

1. Microsoft Visio'de bir diagram açın.
1.  Seçme**Stilleri Tanımla** dan**Biçim** menüsü (Visio 2007) veya sağ tıklayın**stiller** içinde**Çizim Gezgini** penceresini açın ve seçin**Stilleri Tanımla** (Visio 2010).
1.  İçinde**Stilleri Tanımla** iletişim kutusunda, özel stil sayfanız için yeni bir ad yazın. Örneğin, CustomStyle1.
1.  Tıkla**Metin**, **Astar** ve**Doldurmak** Sırasıyla metin, çizgi ve dolgu stillerini ayarlamak için düğmeler.
1.  Tıklamak**TAMAM**.

Microsoft Visio'de özel stil sayfaları tanımladıktan sonra, şekillerinize özel stiller uygulamak için bir .NET uygulamasında aşağıdaki kodu kullanın. Aşağıdaki kod örneklerinin yukarıda tanımlanan özel stil sayfasını çağırdığını unutmayın: uyguladığınız sayfanın adını ve konumunu bilmeniz gerekir. Özel stilleri programlı olarak uygulamak için:

1. diagram yükleyin.
1. Stil uygulamak istediğiniz şekli bulun.
1. Stil sayfasını yükleyin.
1. Stilleri uygulayın.
1. diagram'i kaydedin.
#### **Özel Stiller Programlama Örneği Uygula**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Load diagram
Diagram vsdDiagram = new Diagram(dataDir + "ApplyCustomStyleSheets.vsd");
// Get page by name
Page page = vsdDiagram.Pages.GetPage("Flow 1");

Shape sourceShape = null;
// Find the shape to apply the style
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.Name == "Process")
    {
        sourceShape = shape;
        break;
    }
}

StyleSheet customStyleSheet = null;

// Find the required style sheet
foreach (StyleSheet styleSheet in vsdDiagram.StyleSheets)
{
    if (styleSheet.Name == "Basic")
    {
        customStyleSheet = styleSheet;
        break;
    }
}

if (sourceShape != null && customStyleSheet != null)
{
    // Apply text style
    sourceShape.TextStyle = customStyleSheet;
    // Apply fill style
    sourceShape.FillStyle = customStyleSheet;
    // Apply line style
    sourceShape.LineStyle = customStyleSheet;
}

// Save changed diagram as VDX
vsdDiagram.Save(dataDir + "ApplyCustomStyleSheets_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Bir Şeklin Her Metin Değerine Farklı Stil Uygulayın**
 Birlikte[diyagramlar oluşturma](/diagram/tr/net/load-or-create-a-visio-drawing/), Aspose.Diagram for .NET, şekillerle farklı şekillerde çalışmanızı sağlar. Bu makale, bir şekle birden çok metin değeri eklemeye ve her metin değerine farklı stil uygulamaya yardımcı olur.

{{% alert color="primary" %}} 

Shape öğesi, metnin karakterlerini ve bir çalıştırmanın sonunu ve sonrakinin başlangıcını işaretleyen özel öğeleri (cp, pp, tp ve fld) içeren Metin adlı bir öğe içerir. Karakter Öğesi, şeklin metni için yazı tipi, renk, metin stili, büyük/küçük harf, taban çizgisine göre konum ve punto boyutu gibi biçimlendirme niteliklerini içerir.

{{% /alert %}} 
### **Şekil Metni ve Stilleri Ekleme**

|**Giriş diagram**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](working-with-text_1.png)|


|**Diagram her metin değerinde farklı stile sahip bir şekle çeşitli metin değerleri ekledikten sonra**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](working-with-text_2.png)|
#### **Metin ve Stiller Programlama Örneği Ekleme**
Aşağıdaki kod parçası, bir şeklin metnini ve farklı stilleri ekler.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Clear shape text values and chars
shape.Text.Value.Clear();
shape.Chars.Clear();

// Mark character run and add text
shape.Text.Value.Add(new Cp(0));
shape.Text.Value.Add(new Txt("TextStyle_Regular\n"));
shape.Text.Value.Add(new Cp(1));
shape.Text.Value.Add(new Txt("TextStyle_Bold_Italic\n"));
shape.Text.Value.Add(new Cp(2));
shape.Text.Value.Add(new Txt("TextStyle_Underline_Italic\n"));
shape.Text.Value.Add(new Cp(3));
shape.Text.Value.Add(new Txt("TextStyle_Bold_Italic_Underline"));

// Add formatting characters
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());
shape.Chars.Add(new Aspose.Diagram.Char());

// Set properties e.g. color, font, size and style etc.
shape.Chars[0].IX = 0;
shape.Chars[0].Color.Value = "#FF0000";
shape.Chars[0].Font.Value = 4;
shape.Chars[0].Size.Value = 0.22;
shape.Chars[0].Style.Value = StyleValue.Undefined;

// Set properties e.g. color, font, size and style etc.
shape.Chars[1].IX = 1;
shape.Chars[1].Color.Value = "#FF00FF";
shape.Chars[1].Font.Value = 4;
shape.Chars[1].Size.Value = 0.22;
shape.Chars[1].Style.Value = StyleValue.Bold | StyleValue.Italic;

// Set properties e.g. color, font, size and style etc.
shape.Chars[2].IX = 2;
shape.Chars[2].Color.Value = "#00FF00";
shape.Chars[2].Font.Value = 4;
shape.Chars[2].Size.Value = 0.22;
shape.Chars[2].Style.Value = StyleValue.Underline | StyleValue.Italic;

// Set properties e.g. color, font, size and style etc.
shape.Chars[3].IX = 3;
shape.Chars[3].Color.Value = "#3333FF";
shape.Chars[3].Font.Value = 4;
shape.Chars[3].Size.Value = 0.22;
shape.Chars[3].Style.Value = StyleValue.Bold | StyleValue.Italic | StyleValue.Underline;
// Save diagram
diagram.Save(dataDir + "ApplyFontOnText_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Bir Şeklin Metnini Bul ve Değiştir**
 bu[Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) Class, şeklin metnini düzenlemenizi sağlar. Tarafından sunulan replace yöntemi[Txt](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) sınıf, bir şeklin metnini değiştirmeyi destekler.
Bu makaledeki kod örnekleri, sayfadaki şeklin metnini bulur ve değiştirir.

|**Giriş diagram**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](working-with-text_3.png)|


|**Şekil düzenlendikten sonra diagram**|
|:- |
|![yapılacaklar:resim_alternatif_Metin](working-with-text_4.png)|
Şeklin metnini değiştirme süreci:

1. diagram yükleyin.
1. Bir şeklin belirli bir metnini bulun.
1. Bu şeklin metnini değiştir
1. diagram'i kaydedin.
### **Metin Programlama Örneği Bul ve Değiştir**
Aşağıdaki kod parçacıkları, şeklin metninin nasıl değiştirileceğini gösterir. Kod, bir sayfanın şekillerini yineler.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Prepare a collection old and new text
Dictionary<string, string> replacements = new Dictionary<string, string>();
replacements.Add("[[CompanyName]]", "Research Society of XYZ");
replacements.Add("[[EmployeeName]]", "James Bond");
replacements.Add("[[SubjectTitle]]", "The affect of the internet on social behavior in the industrialize world");
replacements.Add("[[TimePeriod]]", DateTime.Now.AddYears(-1).ToString("dd/MMMM/yyyy") + " -- " + DateTime.Now.ToString("dd/MMMM/yyyy"));
replacements.Add("[[SubmissionDate]]", DateTime.Now.AddDays(-7).ToString("dd/MMMM/yyyy"));
replacements.Add("[[AmountReq]]", "$100,000");
replacements.Add("[[DateApproved]]", DateTime.Now.AddDays(1).ToString("dd/MMMM/yyyy"));

// Load diagram
Diagram diagram = new Diagram(dataDir + "FindReplaceText.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");

// Iterate through the shapes of a page
foreach (Shape shape in page.Shapes)
{
    foreach (KeyValuePair<string, string> kvp in replacements)
    {
        foreach (FormatTxt txt in shape.Text.Value)
        {
            Txt tx = txt as Txt;
            if (tx != null && tx.Text.Contains(kvp.Key))
            {
                // Find and replace text of a shape
                tx.Text = tx.Text.Replace(kvp.Key, kvp.Value);
            }
        }
    }
}
// Save the diagram
diagram.Save(dataDir + "FindAndReplaceShapeText_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Visio Diagram Sayfasından Düz Metni Çıkarın**
Aspose.Diagram API, geliştiricilerin Visio diagram sayfasından düz metin çıkarmasına olanak tanır. Ayrıca Visio diagram metninin tamamını kapsayacak şekilde Visio diagram sayfalarını yineleyebilirler.

 Microsoft Office Visio yazıları şekillere ekliyor. bu[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, metnin karakterlerini ve bir çalıştırmanın sonunu ve sonrakinin başlangıcını işaretleyen özel öğeleri (cp, pp, tp ve fld) içeren Metin adlı bir öğe içerir.
### **Düz Metin Programlama Örneği Çıkarın**
Aşağıdaki kod parçası, Visio Sayfasının şekillerini yineler ve biçimlendirme bilgisi olmadan düz metni filtreler.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
static string text = "";
public static void Run()
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_ShapeText();
    // Load diagram
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

    // Get Visio diagram page
    Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

    // Iterate through the shapes
    foreach (Aspose.Diagram.Shape shape in page.Shapes)
    {
        // Extract plain text from the shape
        GetShapeText(shape);
    }
    // Display extracted text
    Console.WriteLine(text);
}
private static void GetShapeText(Aspose.Diagram.Shape shape)
{
    // Filter shape text
    if (shape.Text.Value.Text != "")
        text += Regex.Replace(shape.Text.Value.Text, "\\<.*?>", "");

    // For image shapes
    if (shape.Type == TypeValue.Foreign)
        text += (shape.Name);

    // For group shapes
    if (shape.Type == TypeValue.Group)
        foreach (Aspose.Diagram.Shape subshape in shape.Shapes)
        {
            GetShapeText(subshape);
        }
}

{{< /highlight >}}


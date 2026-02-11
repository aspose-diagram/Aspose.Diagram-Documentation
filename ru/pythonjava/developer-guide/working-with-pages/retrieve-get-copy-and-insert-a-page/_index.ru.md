---
title: Получить, получить, скопировать и вставить страницу
type: docs
weight: 10
url: /ru/python-java/retrieve-get-copy-and-insert-a-page/
---
## **Получение информации о странице**
В Microsoft Visio страницы являются либо передним планом, либо фоновыми страницами. Чтобы получить информацию о странице, например идентификатор страницы и имя страницы, сначала определите, является ли страница фоновой или приоритетной.

Объект `Page` представляет область рисования страницы переднего плана или страницы фона. Свойство Pages, предоставляемое классом `Diagram`, поддерживает коллекцию объектов Page. Это свойство можно использовать для получения информации о странице.

Используйте свойство `Page.Background`, чтобы определить, является ли страница передним или фоновым.

### **Пример программирования получения информации о странице**
Следующий фрагмент кода извлекает информацию о страницах из файла diagram.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram
diagram = Diagram("RetrievePageInfo.vdx")

for page in diagram.getPages():
    # Checks if current page is a background page
    if page.getBackground() == BOOL.TRUE:
        # Display information about the background page
        print("Background Page ID : " + str(page.getID()))
        print("Background Page Name : " + str(page.getName()))
    else:
        # Display information about the foreground page
        print("\nPage ID : " + str(page.getID()))
        print("Universal Name : " + str(page.getNameU()))
        print("ID of the Background Page : " + str(page.getBackPage()))

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Получите страницу Visio от Diagram**
Иногда разработчикам необходимо получить сведения о странице чертежа Visio. Aspose.Diagram для Python via Java имеет функции, которые помогают им в этом.

Aspose.Diagram для Python via Java предлагает класс `Diagram`, который представляет чертеж Visio. Свойство Pages, предоставляемое классом Diagram, поддерживает коллекцию объектов `Page`. Класс PageCollection предоставляет метод `getPage`, который можно вызвать для получения объекта Page.

### **Получение объекта страницы Visio по идентификатору**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод getPage класса Diagram.Pages.

В следующем примере показано, как получить объект страницы по идентификатору из чертежа Visio.

#### **Пример программирования получения объекта страницы по идентификатору**
```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VDX file
diagram = Diagram("DrawingFlowCharts.vsdx")

# Set page id
page_id = 2
# Get page object by id
page2 = diagram.getPages().getPage(page_id)

jpype.shutdownJVM()

{{< /highlight >}}
```

### **Получение объекта страницы Visio по имени**
Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Вызовите метод GetPage класса Diagram.Pages.

#### **Пример программирования получения объекта страницы по имени**
В следующем примере показано, как получить объект страницы по имени из чертежа Visio.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSDX file
diagram = Diagram("DrawingFlowCharts.vsdx")

# Set page name
pageName = "Flow 2"
# Get page object by name
page2 = diagram.getPages().getPage(pageName)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Скопируйте страницу Visio в другую Diagram**
Aspose.Diagram для Python via Java API позволяет разработчикам копировать и добавлять содержимое из одного Visio diagram в другое. В этом разделе справки объясняется, как выполнить эту задачу.

Aspose.Diagram для Python via Java API имеет класс `Diagram`, который представляет чертеж Visio. Свойство Pages, предоставляемое классом Diagram, поддерживает коллекцию объектов `Page`. Класс PageCollection предоставляет метод `add`, который можно вызвать для добавления другого объекта Page.

Этот пример работает следующим образом:

1. Создайте новый объект класса Diagram.
1. Загрузите существующий Visio diagram в объект класса Diagram.
1. Добавить все мастера из загруженного Visio diagram
1. Получить объект страницы из загруженного diagram (который нужно скопировать).
1. Задайте имя и идентификатор объекта страницы.
1. Удалите пустую страницу нового diagram (необязательно).
1. Вызовите метод добавления класса PageCollection.
1. Сохраните новый diagram в памяти компьютера.

### **Скопируйте пример программирования страницы Visio**
В приведенном ниже примере кода показано, как скопировать объект страницы Visio в другой чертеж Visio.

```
{{< highlight "python" >}}
import jpype
import asposediagram

jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Call the diagram constructor to load diagram from a VSD file
originalDiagram = Diagram("Drawing1.vsdx")

# initialize the new visio diagram
newDiagram = Diagram()

# add all masters from the source Visio diagram
originalMasters = originalDiagram.getMasters()
for master in originalMasters:
    newDiagram.addMaster(originalDiagram, master.getName())

# get the page object from the original diagram
SrcPage = originalDiagram.getPages().getPage("Page-1")
# set page name
SrcPage.setName("new page")

# it calculates max page id
max_page_id = 0
if newDiagram.getPages().getCount() != 0:
    max_page_id = newDiagram.getPages().get(0).getID()

for i in range(0, newDiagram.getPages().getCount() - 1):
    if max_page_id < newDiagram.getPages().get(i).getID():
        max_page_id = newDiagram.getPages().get(i).getID()

MaxPageId = max_page_id
# set page id
SrcPage.setID(MaxPageId)
# add reference of the original diagram page
newDiagram.getPages().add(SrcPage)

# remove first empty page
newDiagram.getPages().remove(newDiagram.getPages().get(0))

# save diagram in VDX format
newDiagram.save("CopyVisioPage_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Скопируйте Visio страницу в другой экземпляр страницы**
Метод `copy` класса `Page` берет экземпляр страницы для клонирования.

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **Вставка пустой страницы в чертеж Visio**
Aspose.Diagram для Python via Java можно вставить новую пустую страницу в чертеж Microsoft Office Visio. В этом примере раздела описано, как это сделать.

Метод `add`, предоставляемый коллекцией Pages, позволяет разработчикам добавлять новую пустую страницу в Visio diagram. Необходимо назначить идентификатор страницы.

### **Вставьте образец программирования пустой страницы**
Следующий фрагмент кода вставляет пустую страницу в чертеж Visio:

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# load diagram
diagram = Diagram("Drawing1.vsdx")
        
# it calculates max page id
max_page_id = 0
if diagram.getPages().getCount() != 0:
    max_page_id = diagram.getPages().get(0).getID()

for i in range(0, diagram.getPages().getCount() - 1):
    if max_page_id < diagram.getPages().get(i).getID():
        max_page_id = diagram.getPages().get(i).getID()
        
# Initialize a new page object
newPage = Page()
# Set name
newPage.setName("new page")
# Set page ID
newPage.setID(max_page_id + 1)

# Or try the Page constructor
# Page newPage = Page(MaxPageId + 1)

# Add a new blank page
diagram.getPages().add(newPage)

# Save diagram
diagram.save("InsertBlankPageInVisio_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

## **Переместить позицию страницы на чертеже Visio**
Aspose.Diagram для Python via Java API может перемещать позицию страницы на чертеже Visio. Метод `moveTo`, предоставляемый классом `Page`, помогает разработчикам перемещать позицию страницы.

### **Пример программирования перемещения страницы**
Элемент MoveTo принимает индекс целевой страницы в качестве параметра для перемещения позиции страницы на чертеже Visio:

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```

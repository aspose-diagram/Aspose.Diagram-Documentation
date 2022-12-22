---
title: Şekilleri bağlamak için Bağlantı dizinlerini kullanın
type: docs
weight: 20
url: /tr/java/use-connection-indexes-to-connect-shapes/
---
## **Şekle yeni Bağlantılar ekleyin ve şekilleri bağlamak için Bağlantı dizinlerini kullanın**
Aspose.Diagram for Java API, geliştiricilerin şekle yeni bağlantı noktaları eklemesine yardımcı olur ve geliştiriciler artık şekilleri bağlantı dizinleriyle bağlayabilir.
### **Şekilleri bağlamak için Bağlantı dizinlerini kullanın**
tarafından sunulan connectShapesViaConnectorIndex üyesi[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)class, bağlantı dizinlerini kullanarak şekilleri bağlamak için kullanılabilir. Aşağıdaki kod, şekillerin nasıl bağlanacağını gösterir:

1. Yeni bir çizim başlatın.
1. Dört dikdörtgen şekli yerleştirin
1. Alt sınır çizgisinde üç bağlantı noktası olacak şekilde iki ek bağlantı noktası ekleyin
1. Her bir alt bağlantıdaki ilk şekli, dinamik bağlayıcılarla Üstteki diğer üç dikdörtgen şekle bağlayın
1. Çizimi kaydet
#### **şekilleri bağlamak için bağlantı dizinlerini kullanın Programlama Örneği**
Şekilleri Aspose.Diagram for Java API ile bağlantı dizinlerine bağlamak için Java uygulamanızda aşağıdaki kodu kullanın.

**Java**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Page page = diagram.getPages().get(0);

// add masters

String connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.addMaster("C:\\temp\\Basic Shapes.vss", rectangle);

diagram.addMaster("C:\\temp\\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.addShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.addShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.addShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.addShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Shape shape1 = page.getShapes().getShape(shape1_ID);

Shape shape2 = page.getShapes().getShape(shape2_ID);

Shape shape3 = page.getShapes().getShape(shape3_ID);

Shape shape4 = page.getShapes().getShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.getX().getUfe().setF("Width*0.33");

connection1.getY().getUfe().setF("Height*0");

Connection connection3 = new Connection();

connection3.getX().getUfe().setF("Width*0.66");

connection3.getY().getUfe().setF("Height*0");

connection1.setIX(shape1.getConnections().add(connection1));

connection3.setIX( shape1.getConnections().add(connection3));

// add connector shapes

Shape connector1 = new Shape();

Shape connector2 = new Shape();

Shape connector3 = new Shape();

long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.addShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.addShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points
page.connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);
page.connectShapesViaConnectorIndex(shape1.getID(), 1, shape3.getID(), 3, connecter2Id);


// save drawing

diagram.save("C:\\temp\\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

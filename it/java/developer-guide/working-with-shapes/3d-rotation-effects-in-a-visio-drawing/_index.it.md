---
title: Effetti di rotazione 3D in un disegno Visio
type: docs
weight: 90
url: /it/java/3d-rotation-effects-in-a-visio-drawing/
---
## **Imposta le proprietà di rotazione 3D in Shapesheet**
Aspose.Diagram for Java API consente agli sviluppatori di modificare i valori di rotazione 3D nel foglio di forma. I valori delle celle RotationXAngle, RotationYAngle e RotationZAngle controllano il grado di rotazione in ciascuno dei rispettivi assi. Il valore enum di RotationType controlla il tipo di rotazione:

1. Rotazione parallela, in cui la forma viene ruotata senza tener conto della prospettiva lineare.
1. Rotazione prospettica, in cui la forma viene ruotata con prospettiva lineare.
1. Preset di rotazione obliqua (in basso a sinistra, in basso a destra, in alto a sinistra e in alto a destra), in cui la forma viene ruotata con proiezione obliqua.

Il**KeepTextFlat**Il valore della cella indica se il testo di una forma ignorerà la rotazione della forma in 3D. Non si applica alla rotazione 2D. Il**Distanza dal suolo**Il valore della cella determina la distanza in cui l'oggetto viene sollevato dal suolo nei punti quando viene ruotato in 3D. Il**Prospettiva**Il valore della cella determina l'angolo prospettico per una rotazione prospettica, in gradi (da 0 a 359,9).
### **Imposta le proprietà di rotazione 3D**
Il membro ThreeDFormat esposto da[Forma](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)class può essere utilizzata per impostare le proprietà di rotazione 3D.

Il codice seguente mostra come:

1. Carica un disegno di origine.
1. Recupera una forma in base al nome della pagina e ai parametri ID.
1. Imposta le proprietà di rotazione 3D.
1. Salva disegno
#### **Esempio di programmazione della rotazione 3D**
Utilizzare il seguente codice nell'applicazione Java per impostare le proprietà di rotazione 3D utilizzando Aspose.Diagram for Java API.

**Java**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram("c:\\temp\\TestTemplate.vsdx");

// get shape by ID and page name

Shape shape = diagram.getPages().getPage("Page-1").getShapes().getShape(0);



// set 3D rotation properties

shape.getThreeDFormat().getRotationXAngle().setValue(2.61);

shape.getThreeDFormat().getRotationYAngle().setValue(2.61);

shape.getThreeDFormat().getRotationZAngle().setValue(3);

shape.getThreeDFormat().getRotationType().setValue(RotationTypeValue.PARALLEL);

shape.getThreeDFormat().getPerspective().setValue(0);

shape.getThreeDFormat().getDistanceFromGround().setValue(0);

shape.getThreeDFormat().getKeepTextFlat().setValue(BOOL.TRUE);

// save drawing

diagram.save("c:\\temp\\TestTemplate.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

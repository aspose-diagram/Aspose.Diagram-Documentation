---
title: Effetti di rotazione 3D in un disegno Visio
type: docs
weight: 90
url: /it/net/3d-rotation-effects-in-a-visio-drawing/
description: Questa sezione spiega come impostare le proprietà di rotazione 3D in Shapesheet con Aspose.Diagram.
---
## **Imposta le proprietà di rotazione 3D in Shapesheet**
Aspose.Diagram API consente agli sviluppatori di modificare i valori di rotazione 3D nel foglio di forma. I valori delle celle RotationXAngle, RotationYAngle e RotationZAngle controllano il grado di rotazione in ciascuno dei rispettivi assi. Il valore enum di RotationType controlla il tipo di rotazione:

1. Rotazione parallela, in cui la forma viene ruotata senza tener conto della prospettiva lineare.
1. Rotazione prospettica, in cui la forma viene ruotata con prospettiva lineare.
1. Preset di rotazione obliqua (in basso a sinistra, in basso a destra, in alto a sinistra e in alto a destra), in cui la forma viene ruotata con proiezione obliqua.

 Il**KeepTextFlat** Il valore della cella indica se il testo di una forma ignorerà la rotazione della forma in 3D. Non si applica alla rotazione 2D. Il**Distanza dal suolo** Il valore della cella determina la distanza in cui l'oggetto viene sollevato dal suolo nei punti quando viene ruotato in 3D. Il**Prospettiva** Il valore della cella determina l'angolo prospettico per una rotazione prospettica, in gradi (da 0 a 359,9).
### **Imposta le proprietà di rotazione 3D**
 Il membro ThreeDFormat esposto da[Forma](https://reference.aspose.com/diagram/net/aspose.diagram/shape)class può essere utilizzata per impostare le proprietà di rotazione 3D.

Il codice seguente mostra come:

1. Carica un disegno di origine.
1. Recupera una forma in base al nome della pagina e ai parametri ID.
1. Imposta le proprietà di rotazione 3D.
1. Salva disegno
#### **Esempio di programmazione della rotazione 3D**
Utilizzare il seguente codice nell'applicazione .NET per impostare le proprietà di rotazione 3D utilizzando Aspose.Diagram for .NET API.

**.NET, C#**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\TestTemplate.vsdx");

// get shape by ID and page name

Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(0);



// set 3D rotation properties

shape.ThreeDFormat.RotationXAngle.Value = 2.61;

shape.ThreeDFormat.RotationYAngle.Value = 2.61;

shape.ThreeDFormat.RotationZAngle.Value = 3;

shape.ThreeDFormat.RotationType.Value = RotationTypeValue.ObliqueFromBottomLeft;

shape.ThreeDFormat.Perspective.Value = 0;

shape.ThreeDFormat.DistanceFromGround.Value = 0;

shape.ThreeDFormat.KeepTextFlat.Value = BOOL.True;

// save drawing

diagram.Save(@"c:\temp\TestTemplate.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

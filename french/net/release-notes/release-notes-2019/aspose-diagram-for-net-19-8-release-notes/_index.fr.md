---
title: Aspose.Diagram for .NET 19.8 Notes de mise à jour
type: docs
weight: 50
url: /fr/net/aspose-diagram-for-net-19-8-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des notes de version pour[Aspose.Diagram for .NET 19.8](https://www.nuget.org/packages/Aspose.Diagram/19.8.0)

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMNET-50334|Ajout du support des codes VBA / Macros (ajouter - modifier - supprimer)|Renforcement|
|DIAGRAMNET-51083|Ajout de la prise en charge du dessin Spline|Renforcement|
|DIAGRAMNET-51676|Visio en HTML - la sortie contient le nom du fichier|Renforcement|
|DIAGRAMNET-50263|Impossible de définir l'emplacement du texte du connecteur en tant que formules|Punaise|
|DIAGRAMNET-50284|VTX en conversion HTML, la couleur de remplissage des formes n'est pas conservée|Punaise|
|DIAGRAMNET-50432|Conversion de VDX en PDF, la méthode Diagram.setFontDirs utilise uniquement la première police sur l'ensemble diagram|Punaise|
|DIAGRAMNET-50463|Conversion VSDX en PDF, rendu des formes manquantes ou incomplètes|Punaise|
|DIAGRAMNET-51033|Les formes de réseau ne sont pas conservées lors de la conversion d'un VSDX en PDF|Punaise|
|DIAGRAMNET-51303|VSDX en PDF - la couleur du texte sur les lignes de connexion est modifiée|Punaise|
|DIAGRAMNET-51663|Une exception non gérée se produit lors de la conversion de VSD en VSDX|Punaise|
|DIAGRAMNET-51664|Le fichier est corrompu après la suppression d'un thème inutilisé|Punaise|
|DIAGRAMNET-51665|Les images sont affichées sous forme de X après la suppression des thèmes inutilisés|Punaise|
|DIAGRAMNET-51667|Lors de la suppression des styles, seule une image a un problème|Punaise|
|DIAGRAMNET-51668|VISIO vers JPG - l'image de sortie n'est pas au bon format|Punaise|
|DIAGRAMNET-51671|Lors de la suppression des formes et des styles principaux inutilisés, seule l'image a un problème|Punaise|
|DIAGRAMNET-51672|Photos perdues lors du chargement et de la sauvegarde|Punaise|
|DIAGRAMNET-51677|Visio vers HTML - Le lien dans le HTML généré ne fonctionne pas|Punaise|
|DIAGRAMNET-51678|Visio en HTML - Format de date incorrect lors de l'enregistrement au format HTML|Punaise|
|DIAGRAMNET-51679|Visio en PDF - Plusieurs erreurs de formatage en PDF|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for .NET. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
### **Ajoute DrawSpline dans la page**
L'extrait de code suivant montre comment dessiner une spline :

{{< highlight "java" >}}

 PointF[]ps = new PointF[]{ new PointF(0, 0.3270758925347308f), 

                             new PointF(0.2926845121364643f, 0.3581517392187368f), 

                             new PointF(0.6526026522346893f, 0.4640748257705201f), 

                             new PointF(1f, 0.327075892534732f) };

                             diagram.Pages[0].DrawSpline(1, 1, 2, 2, ps);

{{< /highlight >}}
### **Ajoute SaveTitle dans HTMLSaveOptions**
L'extrait de code suivant définit si vous souhaitez ou non enregistrer le titre :

{{< highlight "java" >}}

 Aspose.Diagram.Saving.HTMLSaveOptions options = new Aspose.Diagram.Saving.HTMLSaveOptions();

options.SaveTitle = false;

{{< /highlight >}}





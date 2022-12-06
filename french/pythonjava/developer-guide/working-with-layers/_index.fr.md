---
title: Travailler avec des calques
type: docs
weight: 160
url: /fr/python-java/working-with-layers/
---
### **Configuration d'objets de forme avec des calques**
Aspose.Diagram pour Python via Java permet de configurer des objets de forme avec des calques dans Microsoft Office Visio diagram. Chaque forme peut appartenir à plusieurs calques afin que les développeurs puissent gérer les formes en fonction des besoins de l'utilisateur final.

 La[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) L'objet de classe offre la propriété LayerMember qui permet d'ajouter/supprimer des objets de forme aux/des calques dans le dessin Visio. Les utilisateurs peuvent gérer ces propriétés par programmation en utilisant Aspose.Diagram API comme suit :

**Ajoutez, supprimez et déplacez des objets de forme vers / depuis les calques du diagram.** 

Le morceau de code suivant permet d'ajouter, de supprimer et de déplacer les propriétés des objets de forme.
#### **Exemples de programmation**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-ConfigureShapeLayers.py" >}}
### **Ajouter un calque dans la feuille de page Visio**
Aspose.Diagram pour Python via Java permet aux développeurs d'ajouter de nouveaux calques pour organiser des catégories personnalisées de formes, puis d'attribuer des formes à ces calques par programmation.

 La[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) la classe propose une méthode add qui permet d'ajouter un nouveau[Couche](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) objet de classe dans[le dessin Visio](DrawingFlowChart.vsdx). Les développeurs peuvent définir les propriétés de la couche en initialisant son objet de classe.

Le morceau de code suivant permet d'ajouter des objets Layer.
#### **Exemples de programmation**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-AddLayer.py" >}}

{{% alert color="primary" %}} 

Aspose.Diagram pour Python via Java permet aux développeurs d'accéder aux couches existantes de Visio diagram.

{{% /alert %}} 
### **Obtenir toutes les couches disponibles**
 La[Feuille de page](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) propriété de la[Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class permet de récupérer la liste des couches disponibles à partir de[le dessin Visio](DrawingFlowChart.vsdx) utilisant[LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) classer.

Le morceau de code suivant permet d'obtenir la liste des couches.
#### **Exemples de programmation**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-RetrieveAllLayers.py" >}}

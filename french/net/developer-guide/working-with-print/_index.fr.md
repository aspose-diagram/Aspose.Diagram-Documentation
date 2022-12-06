---
title: Travailler avec l'impression
type: docs
weight: 80
url: /fr/net/working-with-print/
description: Cette section explique comment imprimer un document via XpsPrint avec Aspose.Diagram.
---
## **Comment imprimer un document sur un serveur via XpsPrint API**
Cet article peut être utile à toute personne souhaitant soumettre un document XPS au XpsPrint API non géré à partir d'une application .NET. Mais l'objectif principal de cet article est de montrer comment imprimer un diagram à partir d'une application de service ASP.NET ou Windows à l'aide de Aspose.Diagram et de XpsPrint API.
### **Problème**
Lorsque vous développez une application .NET et que vous devez produire une sortie imprimée, vous pouvez utiliser les classes de l'espace de noms System.Drawing.Printing ou les classes WPF. Mais, il s'avère que si vous développez une application de service ASP.NET ou Windows, vos options d'impression sont fortement limitées, car Microsoft déconseille l'utilisation de ces approches. Voir les liens ci-dessous pour plus d'informations.

<http://support.microsoft.com/kb/324565>

L'utilisation des classes d'impression .NET Framework n'est pas prise en charge à partir d'un service. Cela inclut les pages ASP, qui s'exécutent généralement dans le contexte du service serveur.

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

Les classes au sein de l'espace de noms System.Drawing.Printing ne sont pas prises en charge pour une utilisation dans un service Windows ou une application ou un service ASP.NET. Tenter d'utiliser ces classes à partir de l'un de ces types d'application peut entraîner des problèmes inattendus, tels que des performances de service réduites et des exceptions d'exécution.

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

L'utilisation de WPF pour créer les services Windows n'est pas prise en charge. Étant donné que WPF est une technologie de présentation, le service Windows nécessite les autorisations appropriées pour effectuer des opérations visuelles impliquant une interaction de l'utilisateur. Si le service Windows ne dispose pas des autorisations appropriées, des résultats inattendus peuvent se produire.

L'objet Document fournit une famille de méthodes Print pour imprimer des documents et ces méthodes impriment via les classes d'impression .NET définies dans l'espace de noms System.Drawing.Printing. De nombreux clients de Aspose.Diagram utilisent cette méthode d'impression dans leurs applications côté serveur sans aucun problème, mais il existe un moyen de se conformer aux recommandations de Microsoft et il est décrit dans cet article.
### **La solution**
La bonne façon d'imprimer des documents selon Microsoft est d'utiliser XpsPrint API non géré. Ce API est disponible sur Windows 7, Windows Server 2008 R2 et également sur Windows Vista, à condition que la mise à jour de la plate-forme pour Windows Vista soit installée.

Étant donné que Aspose.Diagram peut facilement convertir n'importe quel document en XPS, nous n'avons qu'à écrire du code qui transmet un document XPS à XpsPrint API. Le seul problème est que XpsPrint API n'est pas géré et nécessite une certaine connaissance de la plate-forme Invoke.
### **Le code**
Nous avons créé la classe XpsPrintHelper avec la méthode Print, qui est très facile à utiliser. Il vous suffit de spécifier un document que vous souhaitez imprimer, un nom d'imprimante et un nom de travail facultatif. En cas de problème lors de la soumission ou de l'impression du document, la méthode lèvera une exception.

Le dernier paramètre est une valeur booléenne qui spécifie si le code doit attendre que le travail soit imprimé ou revenir immédiatement après que le travail d'impression a été soumis. Si vous choisissez de revenir immédiatement, vous ne pourrez pas déterminer si le document s'est imprimé avec succès ou non à la fin.
#### **Exemple de programmation**
L'exemple de code suivant montre comment appeler la classe utilitaire pour imprimer via XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-PrintDiagramVisXPSPrinterAPI-PrintDiagramVisXPSPrinterAPI.cs" >}}


Il existe deux surcharges de la méthode XpsPrintHelper.Print. La première surcharge prend un objet Aspose.Diagram.Diagram et l'enregistre dans un MemoryStream au format XPS. Ensuite, il appelle l'autre surcharge XpsPrintHelper.Print.

Si vous souhaitez utiliser cet exemple sans Aspose.Diagram (par exemple, vous avez déjà un document XPS et souhaitez simplement l'imprimer à partir d'une application de service ASP.NET ou Windows), vous pouvez simplement supprimer cette méthode.
#### **Exemple de programmation de flux XPS et d'impression**
Cet exemple de code convertit un Diagram en flux XPS et imprime.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintDocument.cs" >}}


La deuxième surcharge XpsPrintHelper.Print accepte un objet Stream. Le flux doit contenir un document au format XPS. Cette méthode démarre une tâche d'impression XPS, envoie le document à XpsPrint API, puis attend le résultat si nécessaire.
#### **Exemple de programmation XpsPrint API**
Cet exemple de code imprime un document XPS à l'aide de XpsPrint API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintStream.cs" >}}


Le code des méthodes StartJob, CopyJob, WaitForJob et CheckJobStatus ainsi que les définitions des interfaces IXpsPrintJob et IXpsPrintJobStream est assez bas niveau et utilise Platform Invoke et COM Interop. Ce code n'est pas inclus dans l'article par souci de concision, mais il est disponible dans l'exemple de téléchargement.

Le XpsPrint API fournit également des fonctionnalités supplémentaires, telles que la surveillance de la progression du travail, mais notre XpsPrintHelper est un wrapper très simple et n'expose pas cette fonctionnalité. Vous pouvez l'ajouter vous-même si vous le souhaitez.

{{% alert color="primary" %}}

Lorsque vous exécutez le projet, il imprime un exemple de document sur l'imprimante spécifiée. Pour rendre les résultats visibles, la fenêtre de la console s'ouvre. Le programme affiche le message de réussite ou le texte d'une exception si une a été levée.

{{% /alert %}}
## **Impression d'un Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) fournit quatre méthodes de surcharge pour l'impression des diagrammes. Ces méthodes sont suffisamment flexibles pour imprimer le diagram sur l'imprimante par défaut ou sur l'une des imprimantes disponibles avec des paramètres personnalisés. Il vous suffit de sélectionner la méthode d'impression appropriée en fonction des besoins.
### **Impression sur l'imprimante par défaut**
L'impression du diagram sur l'imprimante par défaut est assez simple dans Aspose.Diagram for .NET. Effectuez les étapes suivantes pour imprimer le diagram sur l'imprimante par défaut :

- Créez une instance de la classe Diagram pour charger un diagram à imprimer
- Appelez la méthode Print sans paramètres comme exposé par l'objet Diagram
#### **Impression sur un exemple de programmation d'imprimante par défaut**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-ByDefaultPrinter-ByDefaultPrinter.cs" >}}
### **Impression sur une imprimante spécifique**
L'impression du diagram sur l'imprimante spécifique nécessite le nom de l'imprimante comme paramètre de la méthode d'impression du Diagram. Effectuez les étapes suivantes afin d'imprimer le diagram sur l'imprimante souhaitée :

- Créez une instance de la classe Diagram pour charger un diagram à imprimer
- Appelez la méthode Print de la classe Diagram avec le nom de l'imprimante comme paramètre de chaîne à la méthode Print
#### **Impression sur un exemple de programmation d'imprimante spécifique**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-BySpecificPrinter-BySpecificPrinter.cs" >}}
### **Définition de l'imprimante et du nom du document**
Aspose.Diagram Les API permettent de définir l'imprimante spécifique et le nom du document pour un travail d'impression. Effectuez les étapes suivantes afin d'imprimer le diagram sur l'imprimante souhaitée :

- Créez une instance de la classe Diagram pour charger un diagram à imprimer
- Appelez la méthode Print de la classe Diagram avec l'imprimante et le nom du document comme paramètre de chaîne à la méthode Print
#### **Configuration de l'imprimante et du nom du document Exemple de programmation**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPrintJobAndPrinterName-SetPrintJobAndPrinterName.cs" >}}

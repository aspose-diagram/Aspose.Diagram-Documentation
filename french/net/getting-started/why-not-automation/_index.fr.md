---
title: Pourquoi pas l'automatisation
type: docs
weight: 40
url: /fr/net/why-not-automation/
description: Cette page décrit pourquoi pas l'automatisation.
---
{{% alert color="primary" %}} 

Pourquoi les composants Aspose sont-ils une bien meilleure option que Microsoft Office Automation ?*

Il y a deux questions que l'on entend le plus souvent ici au Aspose :

1. **Vos produits nécessitent-ils l'installation de Microsoft Office pour fonctionner ?** 
La réponse simple est non. Les composants Aspose sont totalement indépendants et ne sont ni affiliés, ni autorisés, parrainés ou autrement approuvés par Microsoft Corporation.
1. **Pourquoi devrions-nous utiliser les produits Aspose plutôt que d'utiliser l'automatisation Microsoft Office ?** 
 La réponse la plus courte que nous puissions donner est qu'il existe de nombreuses raisons, la principale étant que Microsoft lui-même déconseille fortement l'automatisation Office à partir de solutions logicielles :[Considérations pour l'automatisation côté serveur de Office](http://support.microsoft.com/default.aspx?scid=kb;EN-US;q257757).

{{% /alert %}} 
## **Pourquoi pas l'automatisation**
Il y a plusieurs raisons pour lesquelles les composants Aspose sont une meilleure alternative à l'automatisation. Certains des points clés sont décrits ci-dessous. Assurez-vous également de visiter les liens à la fin de cette section.
### **Sécurité**
Ce qui suit est une citation directe de l'article Microsoft référencé ci-dessus :

*"Office Les applications n'ont jamais été conçues pour être utilisées côté serveur et ne prennent donc pas en compte les problèmes de sécurité rencontrés par les composants distribués. Office n'authentifie pas les requêtes entrantes et ne vous protège pas contre l'exécution involontaire de macros ou le démarrage d'un autre serveur susceptibles d'exécuter des macros à partir de votre code côté serveur. N'ouvrez pas les fichiers téléchargés sur le serveur à partir d'un site Web anonyme ! En fonction des derniers paramètres de sécurité définis, le serveur peut exécuter des macros dans un contexte Administrateur ou Système avec une privilèges et compromettre votre réseau ! De plus, Office utilise de nombreux composants côté client (tels que Simple MAPI, WinInet et MSDAIPP) qui peuvent mettre en cache les informations d'authentification du client afin d'accélérer le traitement. Si Office est automatisé côté serveur, un l'instance peut servir plus d'un client, et parce que les informations d'authentification ont été mises en cache pour cette session, il est possible qu'un client puisse utiliser le cache informations d'identification d'un autre client, et ainsi obtenir des autorisations d'accès non accordées en usurpant l'identité d'autres utilisateurs. »*

Les produits Aspose sont très sécurisés. Les composants Aspose s'exécutent dans le même contexte utilisateur que toutes les applications ASP.NET, sous l'utilisateur ASPNET. Par conséquent, les composants Aspose ne présentent pas de risque potentiel pour les ressources système vitales. De plus, lorsqu'un document est ouvert par un composant Aspose, les macros ne sont pas automatiquement exécutées. Les composants Aspose ont été créés dans le but de permettre aux développeurs de créer, manipuler et enregistrer des fichiers Office. Aucun des risques associés au package Microsoft Office n'est inhérent aux composants Aspose.
### **La stabilité**
Ce qui suit est une citation directe de l'article Microsoft référencé ci-dessus :

*"Office 2000, Office XP et Office 2003 utilisent la technologie Microsoft Windows Installer (MSI) pour faciliter l'installation et l'auto-réparation pour un utilisateur final. MSI introduit le concept "d'installation à la première utilisation", qui permet d'installer dynamiquement les fonctionnalités ou configuré au moment de l'exécution (pour le système, ou plus souvent pour un utilisateur particulier). Dans un environnement côté serveur, cela ralentit les performances et augmente la probabilité qu'une boîte de dialogue apparaisse demandant à l'utilisateur d'approuver l'installation ou de fournir un disque d'installation approprié. Bien qu'il soit conçu pour augmenter la résilience de Office en tant que produit d'utilisateur final, la mise en œuvre des fonctionnalités MSI de Office est contre-productive dans un environnement côté serveur. De plus, la stabilité de Office en général ne peut pas être assurée lorsque le serveur exécute -side car il n'a pas été conçu ou testé pour ce type d'utilisation. L'utilisation de Office en tant que composant de service sur un serveur réseau peut réduire la stabilité de cette machine et une conséquence votre réseau dans son ensemble. Si vous envisagez d'automatiser Office côté serveur, essayez d'isoler le programme sur un ordinateur dédié qui ne peut pas affecter les fonctions critiques et qui peut être redémarré si nécessaire."*

Étant donné que les composants Aspose sont regroupés dans une seule DLL, il ne sera jamais nécessaire d'installer des pièces ou des pièces supplémentaires pour qu'ils fonctionnent. Les composants Aspose ne sont utilisés que par les applications .NET et aucune partie du code de composant n'est conçue pour attendre une réponse humaine. Les composants Aspose ont été minutieusement testés. Les composants Aspose sont utilisés par des sociétés telles qu'IBM, Hilton, Reader's Digest, Bank of America et bien d'autres.
### **Évolutivité/Vitesse**
Ce qui suit est une citation directe de l'article Microsoft référencé ci-dessus :

*"Les composants côté serveur doivent être des composants COM multithread hautement réentrants avec une surcharge minimale et un débit élevé pour plusieurs clients. Office Les applications sont à presque tous égards exactement le contraire. Ce sont des serveurs d'automatisation basés sur STA non réentrants conçus pour fournir des fonctionnalités diverses mais gourmandes en ressources pour un seul client. Ils offrent peu d'évolutivité en tant que solution côté serveur et ont des limites fixes pour des éléments importants, tels que la mémoire, qui ne peuvent pas être modifiés via la configuration. Plus important encore, ils utilisent des ressources (telles que les fichiers mappés en mémoire, les compléments ou modèles globaux et les serveurs d'automatisation partagés), ce qui peut limiter le nombre d'instances pouvant s'exécuter simultanément et entraîner des conditions de concurrence si elles sont configurées dans un environnement multi-client. prévoyez d'exécuter plusieurs instances de n'importe quelle application Office en même temps, vous devez envisager de "regrouper" ou de sérialiser l'accès à l'application Office pour éviter le pote interblocages initiaux ou corruption de données."*

Les composants Aspose sont hautement évolutifs et rapides comme l'éclair. les applications Office n'ont pas été conçues pour être utilisées simultanément par des centaines et des milliers d'utilisateurs ; cependant, les composants Aspose sont conçus pour cela. Nos composants sont une véritable solution .NET et fonctionnent parfaitement, que ce soit sur un seul serveur alimentant une seule application ou sur une ferme Web à charge équilibrée alimentant une application à l'échelle de l'entreprise.
### **Prix**
 Lorsqu'une application utilise l'automatisation Microsoft Office, une copie de Microsoft Office doit être achetée pour chaque machine qui exécute l'application. Il arrive souvent qu'une application ait besoin de créer ou de manipuler un fichier office, mais ne nécessite pas que l'utilisateur ait Office. Aspose offre un très[rentable](https://purchase.aspose.com/buy), licence de redistribution libre de droits qui permettra le déploiement vers un nombre illimité d'utilisateurs sans soucis de licence.

Lors de la création d'applications Web, il est important de savoir que les composants d'automatisation Microsoft Office ne sont pas tarifés ni concédés sous licence pour les solutions côté serveur ([Licence des composants Web Office 2000 et des extensions serveur Office](http://support.microsoft.com/default.aspx?scid=kb;EN-US;q243006)); par conséquent, il n'existe pas de bonne solution de licence pour déployer des applications Web qui utilisent les composants Microsoft Office. Aspose offre également une solution très rentable pour les applications basées sur serveur.
### **Fonctionnalités**
 Les composants Aspose fournissent tout ce dont vous avez besoin pour gérer les fichiers Office, et bien plus encore. Ils sont conçus avec la philosophie de permettre aux développeurs d'obtenir les meilleurs résultats avec le moins de travail possible. Contrairement à l'automatisation Office, les composants Aspose offrent de nombreuses fonctions puissantes et rapides. Par exemple,[Aspose.Diagram](https://products.aspose.com/diagram/net/) offre aux développeurs la possibilité de créer, lire, écrire, exporter, imprimer, accéder et protéger Visio diagram ainsi que ses formes.[Chaque composant](https://products.aspose.com/total/) dans la famille Aspose offre son propre ensemble de fonctionnalités uniques et puissantes.

La meilleure partie de l'achat d'un composant Aspose ou d'une suite de composants est d'avoir accès à nos équipes de développement. Nos équipes de développement se rendent compte que si votre entreprise a besoin d'une fonctionnalité, il est fort probable que d'autres entreprises en auront également besoin. Bien que toutes les demandes de fonctionnalités ne puissent pas être ajoutées, nos équipes essaient d'être très ouvertes d'esprit et flexibles lorsqu'elles fournissent une assistance. Cet état d'esprit est ce qui a aidé les composants Aspose à devenir aussi puissants qu'ils le sont. S'il y a des fonctionnalités supplémentaires dont vous avez besoin à partir des objets d'automatisation Office, vos chances de les avoir ajoutées sont très, très faibles.
### **Conclusion**
{{% alert color="primary" %}} 

 Bien que cet article ait couvert de nombreux points clés pour lesquels les composants Aspose sont un meilleur choix que Office Automation, il y en a beaucoup, beaucoup plus. Cet article ne traite principalement que des points les plus importants. Tous les différents composants Aspose offrent un sans risque, sans obligation[Version d'évaluation](https://www.nuget.org/packages/Aspose.Diagram/)Nous vous encourageons à profiter de cette évaluation afin de mieux voir ce que Aspose peut faire pour vos candidatures.

{{% /alert %}}

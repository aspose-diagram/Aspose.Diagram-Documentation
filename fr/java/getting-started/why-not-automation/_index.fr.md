---
title: Pourquoi pas l'automatisation
type: docs
weight: 70
url: /fr/java/why-not-automation/
---
{{% alert color="primary" %}} 

Pourquoi les API Aspose sont-elles une bien meilleure option que l'automatisation Microsoft Office ?

Il y a deux questions que l'on entend le plus souvent ici au Aspose :

1. **Vos produits nécessitent-ils l'installation de Microsoft Office pour fonctionner ?** 
 La réponse simple est non. Les API Aspose sont totalement indépendantes et ne sont ni affiliées, ni autorisées, parrainées ou autrement approuvées par Microsoft Corporation.
1. **Pourquoi devrions-nous utiliser les produits Aspose plutôt que d'utiliser l'automatisation Microsoft Office ?** 
 La réponse la plus courte que nous puissions donner est qu'il existe de nombreuses raisons, la principale étant que Microsoft lui-même déconseille fortement l'automatisation Office à partir de solutions logicielles :[Considérations pour l'automatisation côté serveur de Office](https://support.microsoft.com/en-us/help/257757/considerations-for-server-side-automation-of-office).

Il existe plusieurs raisons pour lesquelles les API Aspose constituent une meilleure alternative à l'automatisation. Certaines des principales raisons sont :

- [Sécurité](/diagram/fr/java/why-not-automation/)
- [La stabilité](/diagram/fr/java/why-not-automation/)
- [Évolutivité/Vitesse](/diagram/fr/java/why-not-automation/)
- [Prix](/diagram/fr/java/why-not-automation/)
- [Fonctionnalités](/diagram/fr/java/why-not-automation/)

Les points clés sont décrits ci-dessous. Assurez-vous également de visiter les liens à la fin de cette section.

{{% /alert %}} 
### **Sécurité**
 Ce qui suit est une citation directe de l'article Microsoft référencé ci-dessus :*"Office Les applications n'ont jamais été conçues pour être utilisées côté serveur et ne prennent donc pas en compte les problèmes de sécurité rencontrés par les composants distribués. Office n'authentifie pas les requêtes entrantes et ne vous protège pas contre l'exécution involontaire de macros ou le démarrage d'un autre serveur susceptibles d'exécuter des macros à partir de votre code côté serveur. N'ouvrez pas les fichiers téléchargés sur le serveur à partir d'un site Web anonyme ! En fonction des derniers paramètres de sécurité définis, le serveur peut exécuter des macros dans un contexte Administrateur ou Système avec une privilèges et compromettre votre réseau ! De plus, Office utilise de nombreux composants côté client (tels que Simple MAPI, WinInet et MSDAIPP) qui peuvent mettre en cache les informations d'authentification du client afin d'accélérer le traitement. Si Office est automatisé côté serveur, un l'instance peut servir plus d'un client, et parce que les informations d'authentification ont été mises en cache pour cette session, il est possible qu'un client puisse utiliser le cache informations d'identification d'un autre client, et ainsi obtenir des autorisations d'accès non accordées en usurpant l'identité d'autres utilisateurs. »*

Les produits Aspose sont très sécurisés. Les API Aspose s'exécutent dans le même contexte utilisateur que toutes les applications .NET et Java. Par conséquent, les API Aspose ne présentent pas de risque potentiel pour les ressources système vitales. De plus, lorsqu'un document est ouvert par un Aspose API, les macros ne sont pas exécutées automatiquement. Les API Aspose ont été conçues dans le but de permettre aux développeurs de créer, manipuler et enregistrer des fichiers Office. Aucun des risques associés au package Microsoft Office n'est inhérent aux API Aspose.
### **La stabilité**
 Ce qui suit est une citation directe de l'article Microsoft référencé ci-dessus :*"Office 2000, Office XP et Office 2003 utilisent la technologie Microsoft Windows Installer (MSI) pour faciliter l'installation et l'auto-réparation pour un utilisateur final. MSI introduit le concept "d'installation à la première utilisation", qui permet d'installer dynamiquement les fonctionnalités ou configuré au moment de l'exécution (pour le système, ou plus souvent pour un utilisateur particulier). Dans un environnement côté serveur, cela ralentit les performances et augmente la probabilité qu'une boîte de dialogue apparaisse demandant à l'utilisateur d'approuver l'installation ou de fournir un disque d'installation approprié. Bien qu'il soit conçu pour augmenter la résilience de Office en tant que produit d'utilisateur final, la mise en œuvre des fonctionnalités MSI par Office est contre-productive dans un environnement côté serveur. De plus, la stabilité de Office en général ne peut pas être assurée lors de l'exécution du serveur -side car il n'a pas été conçu ou testé pour ce type d'utilisation. L'utilisation de Office en tant que composant de service sur un serveur réseau peut réduire la stabilité de cette machine et une conséquence votre réseau dans son ensemble. Si vous envisagez d'automatiser Office côté serveur, essayez d'isoler le programme sur un ordinateur dédié qui ne peut pas affecter les fonctions critiques et qui peut être redémarré si nécessaire."*

Étant donné que les API Aspose sont regroupées dans une seule bibliothèque, il ne sera jamais nécessaire d'installer des pièces ou des pièces supplémentaires pour qu'elles fonctionnent. Les API Aspose sont utilisées par diverses applications et aucune partie du code API n'est conçue pour attendre une réponse humaine. Les API Aspose ont été minutieusement testées. Les API Aspose sont utilisées par des sociétés telles qu'IBM, Hilton, Reader's Digest, Bank of America et bien d'autres.
### **Évolutivité/Vitesse**
 Ce qui suit est une citation directe de l'article Microsoft référencé ci-dessus :*"Les composants côté serveur doivent être des composants COM multithread hautement réentrants avec une surcharge minimale et un débit élevé pour plusieurs clients. Office Les applications sont à presque tous égards exactement le contraire. Ce sont des serveurs d'automatisation basés sur STA non réentrants conçus pour fournir des fonctionnalités diverses mais gourmandes en ressources pour un seul client. Ils offrent peu d'évolutivité en tant que solution côté serveur et ont des limites fixes pour des éléments importants, tels que la mémoire, qui ne peuvent pas être modifiés via la configuration. Plus important encore, ils utilisent des ressources (telles que les fichiers mappés en mémoire, les compléments ou modèles globaux et les serveurs d'automatisation partagés), ce qui peut limiter le nombre d'instances pouvant s'exécuter simultanément et entraîner des conditions de concurrence si elles sont configurées dans un environnement multi-client. prévoyez d'exécuter plusieurs instances de n'importe quelle application Office en même temps, vous devez envisager de "regrouper" ou de sérialiser l'accès à l'application Office pour éviter le pote interblocages initiaux ou corruption de données."*

Les API Aspose sont hautement évolutives et rapides comme l'éclair. les applications Office n'ont pas été conçues pour être utilisées simultanément par des centaines et des milliers d'utilisateurs ; cependant, les API Aspose sont conçues pour cela. Nos API sont une véritable solution et fonctionnent parfaitement, que ce soit sur un seul serveur alimentant une seule application ou sur une ferme Web à charge équilibrée alimentant une application à l'échelle de l'entreprise.
### **Prix**
 Lorsqu'une application utilise l'automatisation Microsoft Office, une copie de Microsoft Office doit être achetée pour chaque machine qui exécute l'application. Il arrive souvent qu'une application ait besoin de créer ou de manipuler un fichier office, mais ne nécessite pas que l'utilisateur ait Office. Aspose offre un très[rentable](https://purchase.aspose.com/), licence de redistribution libre de droits qui permettra le déploiement vers un nombre illimité d'utilisateurs sans soucis de licence.

Lors de la création d'applications Web, il est important de savoir que les composants d'automatisation Microsoft Office ne sont pas tarifés ni concédés sous licence pour les solutions côté serveur ; par conséquent, il n'existe pas de bonne solution de licence pour déployer des applications Web qui utilisent les composants Microsoft Office. Aspose offre également une solution très rentable pour les applications basées sur serveur.
### **Fonctionnalités**
 Les composants Aspose fournissent tout ce dont vous avez besoin pour gérer les fichiers Office, et bien plus encore. Ils sont conçus avec la philosophie de permettre aux développeurs d'obtenir les meilleurs résultats avec le moins de travail possible. Contrairement à l'automatisation Office, les composants Aspose offrent de nombreuses fonctions puissantes et rapides. Par exemple,[Aspose.Diagram](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram) offre aux développeurs la possibilité d'exporter à partir d'un**Tableau de données** ou**Affichage des données** directement dans un fichier Excel.[Chaque composant](https://products.aspose.com/total) dans la famille Aspose offre son propre ensemble de fonctionnalités uniques et puissantes.

La meilleure partie de l'achat d'une suite Aspose API ou API est d'avoir accès à nos équipes de développement. Nos équipes de développement se rendent compte que si votre entreprise a besoin d'une fonctionnalité, il est fort probable que d'autres entreprises en auront également besoin. Bien que toutes les demandes de fonctionnalités ne puissent pas être ajoutées, nos équipes essaient d'être très ouvertes d'esprit et flexibles lorsqu'elles fournissent une assistance. Cet état d'esprit est ce qui a aidé les API Aspose à devenir aussi puissantes qu'elles le sont. S'il y a des fonctionnalités supplémentaires dont vous avez besoin à partir des objets d'automatisation Office, vos chances de les avoir ajoutées sont très, très faibles.
### **Conclusion**
{{% alert color="primary" %}} 

 Cet article a couvert les points clés expliquant pourquoi les API Aspose sont un meilleur choix que l'automatisation Office. Toutes les différentes API Aspose offrent un sans risque, sans obligation[version d'évaluation](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram). Nous vous encourageons à profiter de cette évaluation afin de voir ce que Aspose peut faire pour vos candidatures.

Pour plus d'informations, veuillez consulter cet article Internet :

- [Considérations pour l'automatisation côté serveur de Office](https://support.microsoft.com/en-us/help/257757/considerations-for-server-side-automation-of-office)

{{% /alert %}}

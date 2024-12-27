---
name: Blockstream Green - Mobile
description: Configuration d'un portefeuille logiciel sur mobile
---
![cover](assets/cover.webp)

Un portefeuille logiciel est une application installée sur un ordinateur, un smartphone ou tout autre appareil connecté à Internet, permettant de gérer et de sécuriser les clés de son portefeuille Bitcoin. Contrairement aux hardware wallets, qui isolent les clés privées, les portefeuilles "*chauds*" fonctionnent donc dans un environnement potentiellement exposé aux cyberattaques, ce qui augmente les risques de piratage et de vol.

Les portefeuilles logiciels sont à utiliser pour gérer des montants raisonnables de bitcoins, notamment pour les transactions du quotidien. Cela peut être une option intéressante également pour les personnes possédant un patrimoine limité en bitcoins, pour qui l'investissement dans un hardware wallet peut sembler disproportionné. Cependant, leur exposition constante à Internet les rend moins sûrs pour stocker votre épargne de long terme ou des fonds importants. Pour ces derniers, il est préférable d'opter pour des solutions plus sécurisées, comme les hardware wallets.

Dans ce tutoriel, je vous propose de découvrir une des meilleures solutions de portefeuille logiciel sur mobile : **Blockstream Green**.

![GREEN](assets/fr/01.webp)

Si vous souhaitez découvrir comment utiliser Blockstream Green en version ordinateur, je vous renvoie vers cet autre tutoriel :

https://planb.network/tutorials/wallet/desktop/blockstream-green-desktop-c1503adf-1404-4328-b814-aa97fcf0d5da

## Présentation de Blockstream Green

Blockstream Green est un portefeuille logiciel disponible sur mobile et sur ordinateur. Anciennement connu sous le nom de *Green Address*, ce portefeuille est devenu un projet Blockstream suite à son acquisition en 2016.

Green est une application particulièrement facile à utiliser, ce qui la rend intéressante pour les débutants. Elle propose toutes les fonctionnalités essentielles d'un bon portefeuille Bitcoin, notamment RBF (*Replace-by-Fee*), une option de connexion via Tor, la capacité de connecter son propre nœud, l'option SPV (*Simple Payment Verification*), l'étiquetage et le contrôle des pièces.

Blockstream Green supporte aussi le réseau Liquid, une sidechain de Bitcoin développée par Blockstream pour réaliser des transactions rapides et confidentielles en dehors de la blockchain principale. Ce tutoriel se concentre exclusivement sur Bitcoin, mais un prochain abordera l'utilisation de Liquid.

## Installer et paramétrer l'application Blockstream Green

La première étape est naturellement de télécharger l'application Green. Rendez-vous sur votre store d'applications :
- [Pour Android](https://play.google.com/store/apps/details?id=com.greenaddress.greenbits_android_wallet) ;
- [Pour Apple](https://apps.apple.com/us/app/green-bitcoin-wallet/id1402243590).

![GREEN](assets/fr/02.webp)

Pour les utilisateurs Android, vous avez aussi la possibilité d'installer l'application via le fichier `.apk` [disponible sur le GitHub de Blockstream](https://github.com/Blockstream/green_android/releases).

![GREEN](assets/fr/03.webp)

Lancez l'application, puis cochez la case "*J'accepte les conditions...*".

![GREEN](assets/fr/04.webp)

Lorsque vous ouvrez Green pour la première fois, l’écran d’accueil s’affiche sans portefeuille configuré. Plus tard, si vous créez ou importez des portefeuilles, ils apparaîtront dans cette interface. Avant de passer à la création d’un portefeuille, je vous conseille d’ajuster les paramètres de l’application en fonction de vos attentes. Cliquez sur "*Paramètres de l'application*".

![GREEN](assets/fr/05.webp)

L’option "*Enhanced Privacy*", disponible uniquement sur Android, améliore la confidentialité en désactivant les captures d’écran et en masquant les aperçus d’application. Elle verrouille également automatiquement l’accès à l’application dès que votre téléphone est verrouillé, ce qui rend vos données plus difficiles à exposer.

![GREEN](assets/fr/06.webp)

Pour ceux qui souhaitent renforcer leur confidentialité, l’application propose de rooter votre trafic via Tor, un réseau permettant de chiffrer toutes vos connexions et de rendre vos activités difficiles à tracer. Bien que cette option puisse légèrement ralentir le fonctionnement de l’application, elle est fortement recommandée pour protéger votre vie privée, surtout si vous n'utilisez pas votre propre nœud complet.

![GREEN](assets/fr/07.webp)

Pour les utilisateurs qui disposent de leur nœud complet, Green Wallet offre la possibilité de s'y connecter via un serveur Electrum, ce qui garantit un contrôle total sur les informations du réseau Bitcoin et sur la diffusion des transactions. 

![GREEN](assets/fr/08.webp)

Une autre fonctionnalité alternative est l’option "*SPV Verification*", qui permet de vérifier directement certaines données de la blockchain et donc de réduire le besoin de confiance envers le nœud par défaut de Blockstream, bien que cette méthode ne fournisse pas toutes les garanties d’un nœud complet.

![GREEN](assets/fr/09.webp)

Une fois ces paramètres ajustés selon vos besoins, cliquez sur le bouton "*Sauvegarder*" et redémarrez l’application.

![GREEN](assets/fr/10.webp)

## Créer un portefeuille Bitcoin sur Blockstream Green

Vous êtes maintenant prêt à créer un portefeuille Bitcoin. Cliquez sur le bouton "*Get Started*".

![GREEN](assets/fr/11.webp)

Vous avez le choix entre créer un portefeuille logiciel en local ou gérer un portefeuille froid via un hardware wallet. Pour ce tutoriel, nous nous concentrons sur la création d'un portefeuille chaud, donc vous devrez sélectionner l'option "*On This Device*". Dans un futur tutoriel, je vous montrerai comment utiliser l'autre option.

L'option "*Watch-only*", quant à elle, vous permet d'importer une clé publique étendue (`xpub`) pour consulter les transactions d’un portefeuille sans pouvoir dépenser les fonds associés, ce qui est pratique pour suivre un portefeuille sur un hardware wallet par exemple.

![GREEN](assets/fr/12.webp)

Vous pouvez ensuite choisir de restaurer un portefeuille Bitcoin existant ou d'en créer un nouveau. Pour les besoins de ce tutoriel, nous allons créer un nouveau portefeuille. Cependant, si vous devez régénérer un portefeuille Bitcoin déjà existant à partir de sa phrase mnémonique, par exemple suite à la perte de votre hardware wallet, vous devrez choisir la seconde option.

![GREEN](assets/fr/13.webp)

Vous avez ensuite le choix entre une phrase mnémonique de 12 mots ou de 24 mots. Cette phrase vous permettra de récupérer l'accès à votre portefeuille depuis n'importe quel logiciel compatible en cas de problème sur votre téléphone. Actuellement, opter pour une phrase de 24 mots n'offre pas plus de sécurité qu'une phrase de 12 mots. Je vous recommande donc de choisir une phrase mnémonique de **12 mots**.

Green vous fournira ensuite votre phrase mnémonique. Avant de continuer, assurez-vous de ne pas être observé. Cliquez sur "*Afficher la phrase de récupération*" pour l'afficher à l'écran.

![GREEN](assets/fr/14.webp)

**Cette phrase mnémonique donne un accès complet et non restreint à tous vos bitcoins.** N'importe qui en possession de cette phrase peut subtiliser vos fonds, même sans accès physique à votre téléphone.

Elle permet de restaurer l'accès à vos bitcoins en cas de perte, de vol ou de casse de votre téléphone. Il est donc très important de la sauvegarder soigneusement **sur un support physique (pas numérique)** et de la stocker dans un endroit sécurisé. Vous pouvez l'inscrire sur un bout de papier, ou bien pour plus de sécurité, si ce portefeuille est important, je vous recommande de la graver sur un support en acier inoxydable afin de la protéger contre les risques d'incendies, d'inondations ou d'écroulements (pour un portefeuille chaud destiné à sécuriser une petite quantité de bitcoins, une simple sauvegarde sur papier est probablement suffisante).

*Évidemment, vous ne devez jamais partager ces mots sur internet, contrairement à ce que je fais dans ce tutoriel. Ce portefeuille en exemple sera utilisé uniquement sur le Testnet et sera supprimé à l'issue du tutoriel.*

![GREEN](assets/fr/15.webp)

Après avoir correctement noté votre phrase mnémonique sur un support physique, cliquez sur "*Continuez*". Green Wallet vous demandera ensuite de confirmer certains mots de votre phrase pour vérifier que vous les avez bien enregistrés. Complétez les espaces avec les mots manquants.

![GREEN](assets/fr/16.webp)

Choisissez le code PIN de votre appareil, qui vous servira à déverrouiller votre portefeuille Green. C'est donc une protection contre les accès physiques non autorisés. Ce code PIN n'intervient pas dans la dérivation des clés cryptographiques de votre portefeuille. Ainsi, même sans accès à ce code PIN, la possession de votre phrase mnémonique de 12 ou 24 mots vous permettra de retrouver l'accès à vos bitcoins.

Il est recommandé de choisir un code PIN de 6 chiffres le plus aléatoire possible. Assurez-vous également de sauvegarder ce code pour ne pas l'oublier, sans quoi vous serez contraint de récupérer votre portefeuille depuis la phrase mnémonique. Vous pourrez par la suite ajouter une option de blocage par biométrie afin d’éviter de rentrer le PIN à chaque utilisation. De façon générale, la biométrie est bien moins sécurisée que le PIN en lui-même. Ainsi, par défaut, je vous déconseille de mettre en place cette option de déverrouillage.

![GREEN](assets/fr/17.webp)

Entrez votre PIN une seconde fois pour le confirmer.

![GREEN](assets/fr/18.webp)

Patientez le temps de la création de votre portefeuille, puis cliquez sur le bouton "*Créer un compte*".

![GREEN](assets/fr/19.webp)

Vous avez ensuite le choix entre un portefeuille standard à signature unique, que nous utiliserons dans ce tutoriel, ou un portefeuille protégé par une authentification à deux facteurs (2FA).

![GREEN](assets/fr/20.webp)

L'option 2FA sur Green crée un portefeuille multisignatures 2/2, dont une clé est conservée par Blockstream. Cela signifie que pour réaliser une transaction, les deux clés sont requises : une clé locale protégée par votre code PIN sur votre téléphone, et une clé distante sécurisée par le 2FA sur les serveurs de Blockstream. En cas de perte de l'accès au 2FA ou d'indisponibilité des services de Blockstream, des mécanismes de récupération basés sur des scripts de verrouillage temporel garantissent la possibilité de récupérer vos fonds de manière autonome. Bien que cette configuration réduise significativement les risques de vol de vos bitcoins, elle est plus complexe à gérer et dépend partiellement de Blockstream. Pour ce tutoriel, nous opterons pour un portefeuille classique à signature unique, avec les clés conservées localement sur le téléphone.

Et voilà, votre portefeuille Bitcoin a bien été créé à l'aide de l'application Green !

![GREEN](assets/fr/21.webp)

Avant de recevoir vos premiers bitcoins sur votre portefeuille, **je vous conseille vivement de réaliser un test de récupération à vide**. Notez une information de référence, telle que votre xpub ou la première adresse de réception, puis supprimez votre portefeuille sur l'application Green tant qu'il est encore vide. Ensuite, essayez de restaurer votre portefeuille sur Green en utilisant vos sauvegardes papier. Vérifiez que l'information témoin générée après la restauration correspond à celle que vous aviez notée initialement. Si c'est le cas, vous pouvez être assuré que vos sauvegardes papier sont fiables. Pour en savoir plus sur comment effectuer un test de récupération, je vous conseille de consulter cet autre tutoriel :

https://planb.network/tutorials/wallet/backup/recovery-test-5a75db51-a6a1-4338-a02a-164a8d91b895

## Paramétrer votre portefeuille sur Blockstream Green

Si vous souhaitez personnaliser votre portefeuille, cliquez sur les trois petits points en haut à droite.

![GREEN](assets/fr/22.webp)

L'option "*Renommer*" vous permet de personnaliser le nom de votre portefeuille, ce qui est particulièrement utile si vous gérez plusieurs portefeuilles sur la même application.

![GREEN](assets/fr/23.webp)

Le menu "*Unité*" vous donne la possibilité de changer l'unité de base de votre portefeuille. Vous pouvez par exemple choisir de l'afficher en satoshis plutôt qu'en bitcoins.

![GREEN](assets/fr/24.webp)

Le menu "*Paramètres*" offre un accès aux différentes options de votre portefeuille Bitcoin.

![GREEN](assets/fr/25.webp)

Vous y trouverez par exemple votre clé publique étendue et son *descriptor*, utiles si vous envisagez de configurer un portefeuille en mode watch-only à partir de ce portefeuille.

![GREEN](assets/fr/26.webp)

Vous pouvez aussi y modifier le code PIN de votre portefeuille et activer une connexion par biométrie.

![GREEN](assets/fr/27.webp)

## Utiliser Blockstream Green

Maintenant que votre portefeuille Bitcoin est configuré, vous êtes prêt à recevoir vos premiers sats ! Pour cela, cliquez simplement sur le bouton "*Recevoir*".

![GREEN](assets/fr/28.webp)

Green affichera alors la première adresse de réception vierge de votre portefeuille. Vous pouvez soit scanner le QR code associé, soit copier l'adresse directement pour y envoyer des bitcoins. Ce type d'adresse ne spécifie pas le montant à envoyer par le payeur. Vous pouvez toutefois générer une adresse qui demande un montant spécifique, en cliquant sur les trois petits points en haut à droite, puis sur "*Montant de la demande*", et en saisissant le montant désiré.

Puisque vous utilisez un compte Segwit v0 (BIP84), votre adresse commencera par `bc1q...`. Dans mon exemple, j'utilise un portefeuille Testnet, donc le préfixe est légèrement différent.

![GREEN](assets/fr/29.webp)

Quand la transaction est diffusée sur le réseau, elle apparaîtra dans votre portefeuille.

![GREEN](assets/fr/30.webp)

Attendez d'obtenir suffisamment de confirmations pour considérer la transaction comme définitive.

![GREEN](assets/fr/31.webp)

Avec des bitcoins dans votre portefeuille, vous pouvez maintenant également en envoyer. Cliquez sur "*Envoyer*".

![GREEN](assets/fr/32.webp)

Sur la page suivante, entrez l'adresse du destinataire. Vous pouvez la saisir manuellement ou scanner un QR code.

![GREEN](assets/fr/33.webp)

Choisissez le montant du paiement.

![GREEN](assets/fr/34.webp)

En bas de l'écran, vous pouvez sélectionner le taux de frais pour cette transaction. Vous avez le choix de suivre les recommandations de l'application ou de personnaliser vos frais. Plus les frais sont élevés par rapport aux autres transactions en attente, plus vite votre transaction sera traitée. Pour connaitre le marché de frais, vous pouvez consulter le site [Mempool.space](https://mempool.space/) dans la section "*Transaction Fees*".

![GREEN](assets/fr/35.webp)

Cliquez sur "*Suivant*" pour accéder à un écran récapitulatif de votre transaction. Vérifiez que l'adresse, le montant et les frais sont corrects.

![GREEN](assets/fr/36.webp)

Si tout vous convient, faites glisser le bouton vert en bas de l'écran vers la droite pour signer et diffuser la transaction sur le réseau Bitcoin.

![GREEN](assets/fr/37.webp)

Votre transaction apparaîtra maintenant sur le tableau de bord de votre portefeuille Bitcoin en attente de confirmation.

![GREEN](assets/fr/38.webp)

*Ce tutoriel est établi sur [une version originale appartenant à Bitstack](https://www.bitstack-app.com/blog/installer-portefeuille-bitcoin-green-wallet) rédigée par Loïc Morel. Bitstack est une néo-banque Bitcoin française qui offre la possibilité d'épargner en bitcoins, soit en DCA (Dollar Cost Averaging), soit via un système d'arrondi automatique des dépenses quotidiennes.*

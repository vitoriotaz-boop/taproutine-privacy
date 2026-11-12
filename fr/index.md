---
layout: page
title: "Politique de confidentialité de TapRoutine"
lang: fr-FR
permalink: /fr/
description: "Informations sur la confidentialité et l’utilisation des données de TapRoutine pour Android."
eyebrow: "Confidentialité et données"
brand_label: "Confidentialité"
home_label: "Accueil de la politique de confidentialité TapRoutine"
footer_label: "TapRoutine · Android"
contact_label: "Contact"
---

<p class="last-updated">Dernière mise à jour : 12 novembre 2026</p>
<nav class="language-nav" aria-label="Sélection de la langue">
<a href="{{ '/' | relative_url }}" lang="pt-BR">Português (Brasil)</a>
<a href="{{ '/en/' | relative_url }}" lang="en-US">English</a>
<a href="{{ '/es/' | relative_url }}" lang="es-419">Español</a>
<span aria-current="page" lang="fr-FR">Français</span>
<a href="{{ '/de/' | relative_url }}" lang="de-DE">Deutsch</a>
<a href="{{ '/it/' | relative_url }}" lang="it-IT">Italiano</a>
<a href="{{ '/ja/' | relative_url }}" lang="ja-JP">日本語</a>
</nav>

## À propos de cette version de l’application

TapRoutine est une application Android en version d’aperçu qui permet de configurer une routine pour une application choisie, de la programmer sur l’appareil, d’exécuter les étapes définies par l’utilisateur et de vérifier des points de l’écran à partir de leur couleur. L’APK examiné porte l’identifiant de package `io.github.vitoriotaz.taproutine`, avec `minSdk` 24, `targetSdk` 36 et `android:allowBackup=true`. Les conclusions de ce texte concernent cet APK d’aperçu et peuvent ne pas s’appliquer aux versions futures.

## Données créées ou consultées par l’application

- **Routine et paramètres de l’utilisateur :** ils peuvent inclure le nom de la routine ; le nom et l’identifiant de package de l’application choisie ; les horaires, les jours et le fuseau horaire ; les étapes et les gestes (par exemple des touchers, des balayages, des attentes, la commande Retour ou l’écran d’accueil) ainsi que leurs positions ; la couleur, le point et la tolérance utilisés pour la vérification ; et des paramètres tels que la fréquence des vérifications et la réouverture ou non de l’application cible. Les paramètres peuvent également inclure le Gardien et un écran alternatif doté d’une autre séquence préconfigurée.
- **Applications disponibles :** TapRoutine consulte Android afin d’afficher les applications disposant d’une activité de lancement. L’utilisateur choisit l’application cible ; son nom et son identifiant de package sont conservés localement dans la routine.
- **Informations temporaires sur la fenêtre au premier plan :** tant que le service d’accessibilité de TapRoutine est actif, il reçoit les événements Android `TYPE_WINDOW_STATE_CHANGED` et conserve en mémoire le nom du package indiqué par le système. Le service ne lit pas l’arborescence de l’interface, les textes, les champs ni aucun autre contenu de l’écran.
- **Données et journal locaux :** les routines et les journaux peuvent contenir des horodatages, le package de l’application cible, la progression et le résultat des étapes et des tentatives, des détails techniques sur les échecs, ainsi que des valeurs de couleur, des points/positions et la résolution de l’écran. Les `SharedPreferences` enregistrent également le consentement lié à la divulgation, ainsi que l’état et les horaires des programmations et du Gardien.
- **Capture temporaire pour la vérification de couleur :** lors d’une vérification, l’application récupère en mémoire l’intégralité de l’écran actuellement affiché afin de calculer uniquement la couleur moyenne d’une zone de 3 × 3 au point indiqué. Cette vérification nécessite Android 11 ou une version ultérieure. Une capture peut avoir lieu lors des vérifications d’une routine, de la détection d’un écran alternatif et par le Gardien ; elle n’est pas nécessairement limitée à la fenêtre ou à l’application cible. L’application n’enregistre pas délibérément la capture dans un fichier. Celle-ci est transitoire et, dans le fonctionnement normal, les ressources associées sont libérées après le calcul.

## Utilisation des données

Les données sont utilisées sur l’appareil pour enregistrer et charger la routine, programmer son exécution, effectuer les étapes définies par l’utilisateur, comparer la couleur au point configuré et consigner les résultats. Selon la configuration, la couleur peut sélectionner une séquence alternative préconfigurée ou déclencher l’action préconfigurée du Gardien. L’application n’invente pas d’actions et n’interprète pas le texte ni le contenu de l’écran pour décider quoi faire.

## Traitement, stockage et transmission

Les routines et les journaux sont conservés dans l’espace de stockage privé local de l’application. Les `SharedPreferences` conservent également les données décrites ci-dessus, notamment le consentement lié à la divulgation et l’état et les horaires des programmations et du Gardien. Le package de la fenêtre observé par le service est conservé en mémoire. La capture d’écran est transitoire ; l’application ne l’enregistre pas délibérément dans un fichier et libère les ressources associées dans le fonctionnement normal.

Le code de l’APK examiné n’implémente ni compte, ni serveur, ni synchronisation, ni analytique, ni publicité, ni paiement, ni appels réseau propres à l’application. Cela ne signifie pas qu’aucune copie ne puisse quitter l’appareil : la sauvegarde automatique Android/Google peut copier des données, comme indiqué dans la section ci-dessous. L’application cible choisie peut également avoir ses propres connexions et pratiques en matière de données, qui ne sont pas contrôlées par TapRoutine.

Si vous choisissez de contacter l’assistance par e-mail, votre message et l’adresse utilisés pour l’envoyer seront transmis par votre service de messagerie afin que nous puissions les recevoir et vous répondre. Il s’agit d’une action externe que vous initiez, et non d’un appel réseau propre à TapRoutine.

## Sauvegarde automatique Android/Google

Dans l’APK d’aperçu examiné, `android:allowBackup` est défini sur `true`. Si la sauvegarde automatique Android est activée, Android peut copier les fichiers privés de l’application et les données des `SharedPreferences` — qui peuvent inclure la routine, les journaux, le consentement et l’état/les horaires des programmations et du Gardien — vers le compte Google/Drive de l’utilisateur, selon le fonctionnement du service Android. Le comportement dépend des paramètres de sauvegarde, de la version d’Android et de l’appareil.

Cette sauvegarde est un service Android/Google ; il ne s’agit pas d’un envoi de TapRoutine vers un serveur du développeur. L’application et le développeur n’ont pas accès à la copie de sauvegarde. Il ne faut pas considérer l’effacement des données locales ou la désinstallation de l’application comme une garantie de suppression d’une copie distincte que le service de sauvegarde pourrait conserver.

## Conservation et options de l’utilisateur

La routine et les journaux restent dans le stockage de l’application jusqu’à leur remplacement ou leur suppression. Le bouton **Limpar** (qui signifie « Effacer » en portugais du Brésil) du prototype supprime le journal d’exécution. Si le journal devient trop volumineux, le prototype peut également supprimer les entrées les plus anciennes et conserver les plus récentes. L’enregistrement d’une configuration modifiée remplace la routine locale ; l’annulation de la programmation interrompt l’exécution programmée, mais ne supprime pas à elle seule la configuration enregistrée. Pour supprimer les données locales de l’application, utilisez les commandes de stockage d’Android pour effacer les données de l’application ou désinstallez-la ; cela ne garantit pas la suppression d’une éventuelle copie de sauvegarde distincte. Le système d’exploitation peut présenter les commandes sous des noms différents.

## Services et autorisations Android

- **Service d’accessibilité Android :** l’utilisateur doit l’activer dans les paramètres système pour exécuter les gestes configurés et effectuer les vérifications. Il reçoit les événements `TYPE_WINDOW_STATE_CHANGED` et conserve en mémoire le package indiqué par le système ; il ne lit ni l’arborescence, ni les textes, ni les champs de l’interface. La capture temporaire de l’écran sert à calculer la couleur moyenne décrite ci-dessus.
- **`SCHEDULE_EXACT_ALARM` :** liée à la programmation d’alarmes exactes. Si Android n’autorise pas les alarmes exactes, la programmation peut être moins précise et être retardée.
- **`RECEIVE_BOOT_COMPLETED` :** permet au module de recevoir l’événement de redémarrage de l’appareil afin de gérer la reprogrammation des routines.
- **`WAKE_LOCK` :** permet de maintenir l’appareil actif pendant une exécution qui doit se poursuivre en arrière-plan.
- **`KILL_BACKGROUND_PROCESSES` :** liée à l’action préconfigurée qui consiste à terminer le processus de l’application cible en arrière-plan lorsque la routine prévoit de la rouvrir.
- **`POST_NOTIFICATIONS` :** liée à l’affichage de notifications locales, par exemple pour communiquer un résultat.

La disponibilité de ces autorisations, leur octroi et leurs modalités sont contrôlés par Android et peuvent varier selon les paramètres, la version du système et l’appareil ; ce texte ne présume pas que chacune entraîne une invite d’autorisation à l’exécution qui lui soit propre. N’accordez que les autorisations que vous estimez nécessaires aux fonctions souhaitées.

## Âge visé

Cette version bêta de TapRoutine s’adresse aux adultes âgés de **18 ans ou plus** ; elle n’a pas été conçue pour les enfants ni les adolescents.

## Modifications futures

Les fonctions et pratiques décrites ici correspondent à l’APK d’aperçu examiné et peuvent changer. Si une version future commence à collecter, transmettre, partager ou conserver d’autres données, ou ajoute des services, la politique devra être révisée afin de refléter cette version avant sa distribution. Consultez la version de la politique qui accompagnera la version approuvée.

## Contact

Pour toute question ou demande concernant cette politique : [vitoriotaz@gmail.com](mailto:vitoriotaz@gmail.com).

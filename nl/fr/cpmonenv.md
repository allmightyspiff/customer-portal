---

copyright:

  years: 1994, 2018

lastupdated: "2017-12-04"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Surveillance de votre environnement et des événements système
{: #customerportal_cpmonenvsysevent}

La surveillance de votre environnement signifie que vous avez la possibilité de contrôler les appareils à tout moment et que vous êtes automatiquement notifié si l'un des équipements tombe en panne. Vous pouvez également surveiller les événements système afin de garantir un fonctionnement harmonieux.   
{: shortdesc}

## Surveillance de votre environnement
{: #cpmonenv}

Au minimum, utilisez la surveillance de base par commande ping. Vous avez néanmoins la possibilité de personnaliser vos options de surveillance de la façon la mieux adaptée à vos besoins métier.

### Etre tenu informé de la maintenance réseau et des événements imprévus
{: #cp_stayinfomaintevent}

De temps en temps, des opérations de maintenance réseau planifiées et urgentes sont inévitables. L'infrastructure {{site.data.keyword.BluSoftlayer_full}} gère de nombreux canaux, comme un [compte Twitter ![Icône de lien externe](../icons/launch-glyph.svg)](https://twitter.com/softlayernotify){:new_window}, afin de vous tenir informé de tous les événements de maintenance planifié et d'urgence. En outre, vous pouvez vous [abonner aux notifications par e-mail](/docs/customer-portal/cpsub2not.html){:new_window} depuis le système de gestion d'événements. Ce service gratuit envoie automatiquement des courriers électroniques aux utilisateurs abonnés concernant les événements imprévus qui peuvent impacter des services.

### Utilisation du dispositif mobile de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} 
{: #cp_bmxinframobile}

Utilisez le [dispositif mobile de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg)](https://knowledgelayer.softlayer.com/topic/mobile-devices){:new_window} pour gérer les appareils de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} par mobile à l'aide de votre appareil iOS ou Android. La fonctionnalité au sein du dispositif mobile de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} inclut la prise en charge des demandes de service, le contrôle d'appareil de base et la surveillance de la bande passante.

## Surveillance des événements système
{: #customerportal_monevent}

Vous pouvez surveiller les événements système en affichant les journaux d'audit et les journaux d'accès.

### Affichage d'un journal d'audit pour un compte
{: #cp_viewacctauditlog}

Chaque compte de portail client est fourni avec un journal d'audit qui assure le suivi des interactions de chaque utilisateur au sein du portail client. Les interactions suivies incluent les tentatives de connexion (qu'elles aboutissent ou échouent), les mises à jour de vitesse de port, les mises sous ou hors tension et les réamorçages, ainsi que les interactions effectuées par l'équipe de support de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}}. Procédez comme suit pour afficher un journal d'audit pour un compte utilisateur.

1. Accédez au [portail client ![Icône de lien externe](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window} à l'aide de vos données d'identification uniques.
2. Sélectionnez **Compte** > **Gérer** > **Journal d'audit** depuis la barre de navigation afin d'accéder au journal d'audit.

Le journal d'audit affiche à l'origine les 25 dernières interactions effectuées sur le compte par des utilisateurs. Vous pouvez afficher jusqu'à 200 interactions à tout moment. Mettez à jour le nombre de résultats affichés depuis la liste déroulante **Affichage**. Si des paramètres ont été modifiés, la colonne **Action** de l'interaction comportera un lien. Cliquez sur un lien pour afficher le paramètre impacté par l'action et les détails du changement. Le fait de cliquer sur le nom de l'appareil ou le nom d'utilisateur pour une interaction vous redirige respectivement vers l'écran des détails de l'unité ou l'écran du profil utilisateur.

### Affichage des journaux d'accès d'un utilisateur
{: #cp_viewuserlogs}

Les journaux d'accès affichent les données de chaque tentative d'accès effectuée par un utilisateur du portail client spécifique. Les journaux affichent une date et un horodatage, ainsi que l'adresse IP pour chaque tentative d'accès. Procédez comme suit pour afficher les journaux d'accès d'un utilisateur :

1. Accédez au [portail client ![Icône de lien externe](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window} à l'aide de vos données d'identification uniques.
2. Sélectionnez **Compte** > **Utilisateurs** dans la barre de menus pour accéder à la fenêtre Utilisateurs.
3. Dans la liste déroulante **Actions**, sélectionnez **Afficher journal d'audit** pour afficher le journal d'accès de l'utilisateur.

Le journal d'accès de chaque utilisateur montre les tentatives d'accès effectuées par cet utilisateur par date, ainsi que l'adresse IP à partir de laquelle a eu lieu la tentative d'accès. Les informations du journal d'accès sont en lecture seule, il n'est donc pas possible d'éditer le contenu. Vous pouvez afficher les journaux d'audit à tout moment en répétant la procédure précédente. Pour quitter les journaux et revenir à l'écran Utilisateurs, cliquez sur le lien **Afficher tous les utilisateurs** en haut de l'écran.
# MONDO — Stratégie d'exécution

> Ce document n'ajoute **aucune fonctionnalité** à la vision (`docs/VISION.md`).
> Il répond à une seule question : comment une seule personne obtient, en 10 semaines et avec moins de 500 €, une réponse fiable aux trois hypothèses de la vision.
>
> Les montants, durées et seuils ci-dessous sont des **hypothèses de travail à confronter au terrain**, pas des faits.

---

## 0. Le levier central : lancer MONDO sur un marché, pas dans une ville

Un **marché de plein vent hebdomadaire** est déjà, physiquement, ce que MONDO veut être :

| Marché du samedi | MONDO |
|---|---|
| Chaque étal appartient à quelqu'un | Chaque espace appartient à quelqu'un |
| L'allée relie les étals | LE MARCHÉ relie les espaces |
| On flâne avant d'acheter | La découverte précède la transaction |
| Tout le monde vient du coin | Proximité par construction |
| Ça revient chaque semaine | Indicateur de retour à J+7 |

Ce choix règle d'un coup quatre problèmes de la vision :

1. **L'offre.** Un marché de 30 à 80 exposants permet d'atteindre en quelques samedis les seuils « 8 vendeurs, 3 catégories, 20 offres ».
2. **La contrainte de capacité (§15.4).** Le recrutement se fait dans un seul lieu, une matinée par semaine, au lieu d'être dispersé dans toute une ville.
3. **Le retour à J+7.** Le marché a déjà un rythme hebdomadaire. On mesure si ce rythme physique se prolonge dans le numérique.
4. **L'acquisition sans publicité.** Un QR code sur l'étal envoie vers l'espace du vendeur. Chaque passant du marché devient un visiteur potentiel.

**Garde-fou de la vision :** MONDO n'est pas un outil pour commerçants. Les exposants fournissent l'offre ; les espaces non commerciaux restent le cœur de MONDO (voir §2).

**Point d'attention :** l'alimentaire frais se prête mal à la vente à distance. On cible d'abord les exposants non alimentaires (artisanat, fripe, plantes, brocante, créateurs, services). Les exposants alimentaires restent bienvenus pour la découverte.

---

## 1. Choisir la zone : grille de notation

Évaluer 3 communes candidates de **5 000 à 25 000 habitants**. Les grandes villes diluent la densité ; les villages n'ont pas assez d'offre.

| Critère | Poids | Comment le vérifier |
|---|---|---|
| Marché hebdomadaire ≥ 30 exposants, dont ≥ 10 non alimentaires | 3 | Y aller un jour de marché et compter les étals |
| Réseau personnel du fondateur sur place | 3 | Lister les noms connus |
| ≥ 2 associations créatives actives (dessin, photo, couture, jardin partagé…) | 2 | Annuaire des associations de la mairie |
| Élu ou placier joignable (commerce, vie associative) | 2 | Un appel |
| Groupe local Facebook ou WhatsApp actif | 1 | Nombre de publications par semaine |
| Trajet ≤ 30 min | 1 | — |

Score sur 5 par critère, multiplié par le poids. On retient la commune qui a le score le plus élevé. Il faut **une journée de repérage par commune**, pas plus.

---

## 2. La composition des 50 espaces : trois cercles

| Cercle | Qui | Nombre visé | Rôle dans l'expérience |
|---|---|---|---|
| **A — Exposants** | Vendeurs et artisans du marché | 12 à 15 | Fournir l'offre (au moins 2 propositions chacun) |
| **B — Créateurs non commerçants** | Membres de 2 associations | 18 à 20 | Tester le cœur de la vision : « un espace pour chacun » |
| **C — Habitants** | Passants du marché, clients, proches | 15 à 20 | Visiter, chercher, faire les demandes « Je cherche » |

**Règle de protection de la vision :** au plus 30 % des espaces sont principalement commerciaux. Au-delà, MONDO serait perçu comme un énième site d'annonces.

**Règle anti-biais (la plus importante) :** chaque utilisateur reçoit un marqueur de provenance (`réseau perso`, `marché`, `association`, `QR inconnu`). **Au moins 50 % des 50 espaces doivent venir de l'extérieur du réseau personnel**, et chaque indicateur est aussi calculé sur ce sous-groupe. Des amis qui reviennent par politesse ne valident rien.

---

## 3. Le calendrier : 10 semaines

### Phase 0 — La preuve avant le code (S-4 et S-3)

**15 conversations** autour d'une maquette (Figma ou papier), avec trois exemples d'espaces : un exposant, une personne qui dessine, et une personne « juste moi ».

**Le script** (questions sur ce que les gens font déjà, pas sur ce qu'ils pensent qu'ils feraient) :

1. « Aujourd'hui, où est-ce que tu montres ce que tu fais, ce que tu aimes ou ce que tu vends ? »
2. « La dernière fois que tu as cherché quelque chose près de chez toi, comment tu as fait ? »
3. *(Montrer la maquette)* « **Qu'est-ce que tu mettrais dans ton espace ?** » — noter les trois premiers éléments cités, **mot pour mot**.
4. **Le test d'engagement :** « Tu m'envoies 3 photos et une phrase, et je te prépare ton espace pour le lancement ? »
5. « À qui tu enverrais le lien ? »

**Critère pour passer au code :**
- au moins **8 personnes sur 15 envoient vraiment** leurs photos sous 48 h (un « oui » oral ne compte pas) ;
- au moins **5 personnes sur 15 citent d'abord un élément non commercial**.

Si le premier critère n'est pas atteint, on retravaille la proposition avant d'écrire la moindre ligne de code.
Si c'est le second qui manque, MONDO est perçu comme un site d'annonces, et c'est un signal à prendre au sérieux.

**Effet secondaire utile :** ces 8 personnes ou plus ont des espaces déjà remplis au lancement. On n'ouvre jamais un réseau vide.

**À faire en parallèle :**
- recherche d'antériorité du nom sur INPI et EUIPO, **avant toute impression** ;
- rendez-vous avec le placier et l'élu au commerce : autorisation de circuler sur le marché et de poser des QR codes.

### Phase 1 — Construire le minimum (S-3 à S-1)

**Format :** une application web installable (PWA), sans passer par les magasins d'applications. Il n'y a pas de délai de validation, et le partage par lien fonctionne directement.

**Dans le périmètre :**
- connexion par lien magique (email ou SMS), sans mot de passe ;
- espace : photo, présentation, éléments `Texte`, `Image`, `Création`, `Recherche`, `Proposition` ;
- page publique `mondo.xx/prénom` ;
- mode public / privé ;
- règle de découvrabilité (une photo et une présentation, ou deux éléments) ;
- **compteur de visites visible par le propriétaire** à l'ouverture de son espace ;
- LE MARCHÉ : une liste des propositions et des recherches de la zone, avec rotation (pas de classement payant, pas d'algorithme opaque) ;
- bouton « Contacter » qui affiche le moyen de contact choisi par le propriétaire (email ou WhatsApp) ;
- bouton « Signaler » qui envoie un email au fondateur ;
- compression des images côté téléphone (WebP, 1600 px maximum, environ 200 Ko).

**Hors périmètre :** abonnements, messagerie interne, avis, paiement, notifications push, géolocalisation fine (la zone est la commune).

**La mesure, dès le premier jour.** Sans ces événements, l'expérience produit des opinions, pas des faits :

| Événement | Sert à mesurer |
|---|---|
| `space_created` (+ provenance) | Espaces créés |
| `element_added` | Personnalisation |
| `space_discoverable` | Personnalisation sous 48 h |
| `session_start` (+ source : direct / QR / lien externe / relance humaine) | Retour spontané à J+7 |
| `space_viewed` (visiteur ≠ propriétaire) | Espaces visités par d'autres |
| `contact_revealed` | Premiers contacts |
| `offer_published`, `search_published` (+ catégorie) | Offre, vendeurs, catégories |
| `onboarding_duration` (assisté / autonome) | Objectif de 2 à 5 minutes |

**Outil d'analyse :** une solution sans cookies, auto-hébergée ou hébergée en Europe. Cela simplifie la conformité RGPD.

**Gel des fonctionnalités à S0.** Pendant le terrain, on ne code que :
- les bugs bloquants ;
- les frictions **observées chez au moins 3 personnes différentes**.

Tout le reste va dans une liste « après ».

### Phase 2 — Le terrain (S1 à S6)

**Rythme hebdomadaire** (environ 35 h, avec une marge) :

| Jour | Activité | Heures |
|---|---|---|
| **Samedi (marché)** | Installation des espaces sur place, chronomètre visible | 6 |
| Dimanche | Lecture des chiffres et boucle de révision (§6) | 3 |
| Lundi et mardi | Corrections, uniquement celles observées au moins 3 fois | 12 |
| Mercredi soir | « Soirée espace » dans une association | 4 |
| Jeudi | Modération, échanges individuels | 4 |
| Vendredi | Préparation du marché : QR codes, demandes « Je cherche » | 3 |

**Objectifs cumulés :**

| Semaine | Espaces | Jalon |
|---|---|---|
| S1 | 15 | Espaces préparés en phase 0 + premiers exposants, QR codes sur 8 étals |
| S2 | 25 | Soirée espace n° 1 (association 1), chronométrée |
| S3 | 35 | Soirée espace n° 2 (association 2), **point d'étape** (§5) |
| S4 | 45 | Ouverture du MARCHÉ si le seuil est atteint |
| S5 | 50 | Arrêt du recrutement actif |
| S6 | — | **Observation sans intervention** : on mesure le retour spontané |

**Deux mesures distinctes pour le temps de création :**
- **assistée** : le fondateur tient le téléphone mais **ne tape jamais à la place** de la personne ;
- **autonome** : au moins 15 personnes du cercle C, arrivées par QR code, sans aide.

Seule la mesure autonome valide l'objectif de 2 à 5 minutes.

---

## 4. Six mécaniques qui n'ajoutent aucune fonctionnalité

1. **Le QR d'étal.** Une petite plaque « Mon espace MONDO » relie l'étal physique à l'espace numérique. Elle alimente directement l'indicateur « espaces visités par d'autres ».

2. **Le compteur de passages.** « 12 personnes sont passées dans ton espace cette semaine », affiché quand le propriétaire ouvre son espace. C'est une raison de revenir qui **n'est pas une notification**, donc compatible avec la mesure du retour spontané.

3. **La jauge d'ouverture du MARCHÉ.** Le bouton LE MARCHÉ affiche : « Le marché ouvre à 20 offres réelles — 13/20 ». La règle de la vision (« n'ouvrir que lorsque l'offre est réelle ») devient un objectif collectif visible : les exposants recrutent leurs voisins d'étal.

4. **La question du samedi.** On demande à chaque passant : « Qu'est-ce que tu cherches et que tu ne trouves pas ici ? » Une réponse devient une `Recherche` publiée, donc un espace créé. C'est la porte d'entrée la plus légère : une phrase, sans photo. Les exposants reviennent pour lire les demandes.

5. **Le lien comme canal.** Chaque espace a un lien court, avec une suggestion : « Mets-le dans ta bio ou ton statut WhatsApp ». La part des visites qui viennent de liens externes indique la croissance future possible **sans publicité**.

6. **La personne derrière l'étal.** On suggère à chaque exposant (sans l'imposer) de publier un élément non commercial avant sa première proposition : l'histoire de l'étal, l'atelier, une passion. C'est la différence visible avec un site d'annonces, et l'application concrète du non-objectif n° 3.

---

## 5. Tableau de bord et règles de décision

### Indicateur principal

**Espaces actifs par semaine** : espaces dont le propriétaire est revenu ou a ajouté un élément dans la semaine, **sans relance**.

### Seuils, décidés à l'avance

| Indicateur | Objectif | Seuil rouge | Hypothèse testée |
|---|---|---|---|
| Espaces créés | 50 | < 30 | H1 — envie de posséder un espace |
| Personnalisés sous 48 h | 35 | < 20 | H1 / simplicité |
| Retour à J+7 sans notification | 15 | < 8 | **H2 — retour spontané** |
| Espaces visités par d'autres | 25 | < 12 | Découverte |
| Premiers contacts ou échanges | 10 | < 4 | H3 — marché local |
| Offres réelles / vendeurs / catégories | 20 / 8 / 3 | < 12 / < 5 / < 2 | H3 |
| Temps de création médian (autonome) | ≤ 5 min | > 8 min | Simplicité |

**Règle de pureté pour J+7 :** toute relance humaine (message, appel) est enregistrée. Les sessions de cette personne dans les 7 jours qui suivent sont **exclues** du calcul « spontané ».

### Point d'étape à S3

Si les espaces personnalisés sous 48 h sont en dessous de 50 % des espaces créés, on arrête le recrutement pendant une semaine et on corrige l'installation. Inutile de recruter dans un entonnoir percé.

### La décision finale (fin S6)

Elle est écrite **avant** de voir les chiffres, puis appliquée telle quelle :

| Résultat | Décision |
|---|---|
| H1, H2 et H3 validées | Lancer la V1.1 **et** reproduire dans une 2ᵉ commune **sans réseau personnel**, pour vérifier que la méthode tient seule |
| H1 et H2 validées, H3 non | Les gens veulent un espace, mais le marché manque de densité. Prolonger de 6 semaines sur un 2ᵉ marché de la même zone, **sans nouvelles fonctionnalités** |
| H1 validée, H2 non | Les gens créent mais ne reviennent pas. C'est l'échec le plus grave. Interroger 10 personnes qui ne sont pas revenues, faire **une seule** itération de 4 semaines sur la raison de revenir, puis décider : réorientation ou arrêt |
| H1 non validée | La proposition ne prend pas. **On ne code rien de plus.** Arrêt ou repositionnement radical |

Chaque résultat est aussi calculé **sur le sous-groupe hors réseau personnel**. Si les deux résultats divergent, c'est le sous-groupe qui compte.

---

## 6. La boucle hebdomadaire (chaque dimanche, 3 h)

| Étape | Concrètement pour MONDO |
|---|---|
| **Observer** | Notes mot pour mot du samedi et événements de la semaine |
| **Comprendre** | Où se situe chaque cohorte dans l'entonnoir : créé → personnalisé → visité → revenu |
| **Confronter** | Écart entre le réel et l'objectif de la semaine (§3) |
| **Hypothèses** | Deux explications au plus pour l'écart le plus important |
| **Anticiper** | Ce qui risque de casser samedi prochain |
| **Prioriser** | **Un seul changement par semaine**, choisi selon l'impact sur l'indicateur principal |
| **Décider** | On l'écrit dans le journal des décisions |
| **Simuler** | On le teste sur 2 ou 3 personnes avant de le déployer |
| **Exécuter / Revue humaine** | Risque faible : on déploie. Risque élevé (données personnelles, modération, tout ce qui touche un non-objectif) : on prend 48 h et on demande un avis extérieur |
| **Mesurer** | Même tableau, même définition, chaque semaine |
| **Apprendre** | Journal : « je croyais X, j'ai observé Y » |
| **Réviser** | Mise à jour des 3 hypothèses (plus probable / moins probable) |
| **Dreaming** | Vendredi soir, 30 min : « Qu'est-ce que je refuse de voir ? » |

---

## 7. Le modèle économique : l'ordre d'arrivée des revenus

**Aucun revenu pendant l'expérience.** Mais on prépare le chemin, en respectant les trois non-objectifs.

| Ordre | Source | Qui paie | Pourquoi c'est cohérent | Quand |
|---|---|---|---|---|
| 1 | **Déploiement territorial** | Commune, intercommunalité, chambre consulaire | Les habitants restent gratuits, et la commune finance la visibilité de *tout* son commerce local, pas d'un seul vendeur. À relier aux programmes de revitalisation des centres-villes et des petites villes (éligibilité et état actuel **à vérifier**) | Dès qu'une zone est validée |
| 2 | **Frais de protection acheteur** | L'acheteur, seulement s'il paie dans MONDO | Les vendeurs restent gratuits, ce qui protège l'offre. On paie une protection, pas une visibilité | V2 |
| 3 | **Outils professionnels** | Vendeurs actifs volontaires | Statistiques, catalogue, horaires, retrait en boutique, facturation. **Jamais de classement** | V3 |
| 4 | **Publicité locale identifiée** | Commerces | Plafonnée (par exemple un emplacement pour 10 résultats), toujours marquée « Sponsorisé », jamais en tête de façon permanente | En dernier |

**Le premier test de revenu se fait dès S4, sans rien vendre.** On demande à l'élu : « Si ça marche ici, qui paierait l'extension à la commune voisine ? » La réponse (un nom, un budget, un calendrier, ou rien) vaut plus qu'un tableur.

**Coût unitaire indicatif :** une trentaine d'images de 200 Ko par espace, soit environ 6 Mo. L'hébergement coûte quelques centimes par espace et par mois à cette échelle, donc **l'existence gratuite est soutenable**. À recalculer avec les vrais chiffres en S6.

**Budget de l'expérience :** moins de 500 € (nom de domaine, hébergement, environ 50 plaques QR, cafés offerts lors des soirées espace).

---

## 8. Conformité à anticiper

*Ce n'est pas un avis juridique : à faire valider.*

- **Nom :** « Mondo » est un mot courant, probablement déjà déposé dans certaines classes. Recherche INPI et EUIPO (classes 35, 38, 42) **avant** d'imprimer quoi que ce soit, et garder un nom de repli.
- **RGPD :** collecter le minimum. La localisation se limite à la commune. Mentions d'information, registre des traitements, mesure d'audience sans cookies.
- **DSA (règlement européen sur les services numériques) :** en tant qu'hébergeur, MONDO doit prévoir un mécanisme de signalement, des conditions d'utilisation claires et un point de contact. Les obligations de **traçabilité des vendeurs professionnels** propres aux places de marché sont à cadrer avant l'ouverture large du MARCHÉ (V1.1).
- **DAC7 :** obligations de déclaration des plateformes qui facilitent des ventes. Cela concerne surtout la V2 (transactions).
- **Particulier ou professionnel :** chaque proposition indique le statut du vendeur, car le droit de la consommation diffère selon le cas.

---

## 9. Pré-mortem : comment MONDO peut échouer, et la parade

| Risque | Parade |
|---|---|
| Espaces créés puis vides | Installation accompagnée, espaces pré-remplis en phase 0, règle de découvrabilité |
| Perçu comme « encore un site d'annonces » | Le cercle B arrive avant l'ouverture du MARCHÉ ; le message commence par « ton endroit », pas par « vends » |
| Les exposants ne voient aucun retour | Compteur de passages, demandes « Je cherche » transmises chaque vendredi |
| Données faussées par le réseau personnel | Marqueur de provenance, résultats calculés sur le sous-groupe externe |
| Retour J+7 contaminé par les relances | Relances enregistrées et exclues pendant 7 jours |
| Épuisement du fondateur | Budget d'heures, gel des fonctionnalités, un seul changement par semaine |
| Nom indisponible après impression | Recherche d'antériorité en S-4 |
| Incident de modération | Règles affichées, signalement par email, traitement en moins de 24 h |

---

## 10. Les 7 prochains jours

1. Lister 3 communes candidates et noter leur marché avec la grille du §1.
2. Aller au marché de la mieux notée samedi : compter les étals, parler à 5 exposants.
3. Préparer la maquette : 3 espaces d'exemple (exposant, créateur, « juste moi »).
4. Faire les 5 premières conversations avec le script du §3.
5. Lancer la recherche d'antériorité sur le nom.
6. Demander un rendez-vous au placier et à l'élu au commerce.
7. Ouvrir le journal des décisions et y écrire, avant toute donnée : « Je crois que H1 / H2 / H3 sont vraies parce que… ».

> Le seul livrable de la semaine : **8 personnes qui ont réellement envoyé leurs photos.**

# Politique de Confidentialit&eacute;

*Derni&egrave;re mise &agrave; jour : 15 f&eacute;vrier 2026*

---

## 1. Responsable du traitement

| | |
|---|---|
| **Responsable** | CESYUM SAS |
| **Forme juridique** | SAS au capital variable |
| **Si&egrave;ge social** | 181 Cours de l'Argonne, 33000 Bordeaux, France |
| **RCS Bordeaux** | 990 625 154 |
| **SIRET** | 990 625 154 00010 |
| **Contact RGPD** | [contact@cesyum.com](mailto:contact@cesyum.com) |
| **Repr&eacute;sentant** | Nialy Abdjoubarkoye, Pr&eacute;sident |

Conform&eacute;ment &agrave; l'article 37 du RGPD, la d&eacute;signation d'un D&eacute;l&eacute;gu&eacute; &agrave; la Protection des Donn&eacute;es (DPO) n'est pas obligatoire pour CESYUM. Pour toute question relative &agrave; vos donn&eacute;es, contactez-nous &agrave; [contact@cesyum.com](mailto:contact@cesyum.com).

---

## 2. Donn&eacute;es collect&eacute;es

Dans le cadre du Service de suivi automatique du temps de travail, CESYUM collecte les cat&eacute;gories de donn&eacute;es suivantes :

### 2.1 Donn&eacute;es d'identification

- Nom et pr&eacute;nom
- Adresse e-mail professionnelle
- Mot de passe (stock&eacute; uniquement sous forme de hachage bcrypt, jamais en clair)
- Cabinet de rattachement et grade (collaborateur, senior, manager, associ&eacute;)

### 2.2 Donn&eacute;es d'activit&eacute; professionnelle

- Nom des applications actives (processus Windows d&eacute;tect&eacute;s par l'application Desktop)
- Titres de fen&ecirc;tres des applications en cours d'utilisation
- URLs et titres des pages web visit&eacute;es (collect&eacute;s par l'extension navigateur, uniquement pendant les heures de travail)
- Horodatages de d&eacute;but et fin d'activit&eacute; (au format UTC)
- Dur&eacute;e des sessions de travail
- Client associ&eacute; &agrave; chaque plage de temps (par matching automatique ou attribution manuelle)

### 2.3 Donn&eacute;es du cabinet

- Nom du cabinet
- Liste des clients et informations associ&eacute;es (nom, contacts, informations de facturation)
- Structure des &eacute;quipes

### 2.4 Donn&eacute;es techniques

- Adresse IP (pour la s&eacute;curit&eacute; et la limitation des tentatives de connexion)
- Version de l'application Desktop
- Identifiant unique de l'extension navigateur

### 2.5 Donn&eacute;es NON collect&eacute;es

> L'application Desktop ne capture ni captures d'&eacute;cran, ni frappes clavier, ni contenu des documents, ni donn&eacute;es bancaires, ni e-mails personnels, ni historique de navigation g&eacute;n&eacute;ral.

---

## 3. Finalit&eacute;s du traitement

Les donn&eacute;es collect&eacute;es sont utilis&eacute;es exclusivement pour :

1. **Fourniture du Service :** suivi du temps de travail, association aux clients, g&eacute;n&eacute;ration des feuilles de temps et rapports de productivit&eacute;
2. **Gestion du compte :** authentification, gestion des acc&egrave;s, communication relative au Service
3. **Am&eacute;lioration du Service :** analyse anonymis&eacute;e de l'utilisation pour am&eacute;liorer les fonctionnalit&eacute;s
4. **S&eacute;curit&eacute; :** pr&eacute;vention des acc&egrave;s non autoris&eacute;s, limitation des tentatives de connexion

**Aucune donn&eacute;e n'est utilis&eacute;e &agrave; des fins publicitaires, de profilage commercial ou revendue &agrave; des tiers.**

---

## 4. Base l&eacute;gale du traitement

Les traitements de donn&eacute;es sont fond&eacute;s sur :

- **L'ex&eacute;cution du contrat** (article 6.1.b du RGPD) : traitement n&eacute;cessaire &agrave; la fourniture du Service
- **L'int&eacute;r&ecirc;t l&eacute;gitime** (article 6.1.f du RGPD) : s&eacute;curit&eacute; du Service et am&eacute;lioration des fonctionnalit&eacute;s
- **Le consentement** (article 6.1.a du RGPD) : pour l'installation de l'application Desktop et de l'extension navigateur

---

## 5. H&eacute;bergement et s&eacute;curit&eacute; des donn&eacute;es

### 5.1 Localisation

Toutes les donn&eacute;es sont h&eacute;berg&eacute;es sur des serveurs **Amazon Web Services (AWS)** situ&eacute;s dans la r&eacute;gion **eu-west-3 (Paris, France)**. Les donn&eacute;es ne quittent jamais le territoire de l'Union europ&eacute;enne.

### 5.2 Mesures de s&eacute;curit&eacute;

| Mesure | D&eacute;tail |
|---|---|
| Chiffrement des communications | TLS (HTTPS) |
| Mots de passe | Hach&eacute;s avec bcrypt (12 rounds) |
| Isolation des donn&eacute;es | Row-Level Security (RLS) dans PostgreSQL |
| Authentification | Jeton JWT avec expiration de 8 heures |
| Protection anti-bruteforce | 10 tentatives par 15 minutes |
| Sauvegardes | Automatiques quotidiennes chiffr&eacute;es sur Amazon S3 |
| Infrastructure | Conteneurs Docker avec privil&egrave;ges restreints (read-only, no-new-privileges) |

### 5.3 Stockage local

L'application Desktop stocke temporairement les donn&eacute;es de suivi sur le poste de l'utilisateur avant synchronisation avec le serveur. Ces fichiers sont stock&eacute;s dans le r&eacute;pertoire local de l'application et sont conserv&eacute;s 90 jours localement.

---

## 6. Dur&eacute;e de conservation

| Type de donn&eacute;es | Dur&eacute;e de conservation |
|---|---|
| Donn&eacute;es de compte | Dur&eacute;e de l'abonnement + 30 jours apr&egrave;s suppression |
| Timestamps (donn&eacute;es de suivi) | Dur&eacute;e de l'abonnement (partitionn&eacute;es par ann&eacute;e) |
| Fichiers locaux (Desktop) | 90 jours (nettoyage automatique) |
| Logs de s&eacute;curit&eacute; | 1 an |
| Codes de v&eacute;rification e-mail | 10 minutes (suppression automatique) |

---

## 7. Partage des donn&eacute;es

Les donn&eacute;es peuvent &ecirc;tre partag&eacute;es dans les cas suivants :

- **Au sein du cabinet :** les utilisateurs du m&ecirc;me cabinet peuvent acc&eacute;der aux donn&eacute;es de temps des collaborateurs, selon leur grade et les r&egrave;gles d'acc&egrave;s d&eacute;finies
- **Sous-traitants techniques :** Amazon Web Services (h&eacute;bergement), uniquement dans le cadre de la fourniture d'infrastructure
- **Obligations l&eacute;gales :** en cas de r&eacute;quisition judiciaire ou d'obligation l&eacute;gale

**Aucune donn&eacute;e n'est transmise &agrave; des tiers &agrave; des fins commerciales.**

---

## 8. Vos droits (RGPD)

Conform&eacute;ment au R&egrave;glement G&eacute;n&eacute;ral sur la Protection des Donn&eacute;es (RGPD) et &agrave; la loi Informatique et Libert&eacute;s, vous disposez des droits suivants :

- **Droit d'acc&egrave;s :** obtenir une copie de vos donn&eacute;es personnelles
- **Droit de rectification :** corriger vos donn&eacute;es inexactes ou incompl&egrave;tes
- **Droit &agrave; l'effacement :** supprimer vos donn&eacute;es (disponible dans Param&egrave;tres > Donn&eacute;es personnelles)
- **Droit &agrave; la portabilit&eacute; :** exporter vos donn&eacute;es dans un format structur&eacute; (disponible dans Param&egrave;tres > Donn&eacute;es personnelles)
- **Droit d'opposition :** vous opposer au traitement de vos donn&eacute;es
- **Droit &agrave; la limitation :** limiter le traitement de vos donn&eacute;es

Pour exercer vos droits, contactez-nous &agrave; [contact@cesyum.com](mailto:contact@cesyum.com). Vous pouvez &eacute;galement exercer directement votre droit &agrave; l'effacement et &agrave; la portabilit&eacute; depuis les param&egrave;tres de votre compte.

En cas de r&eacute;clamation, vous pouvez saisir la **CNIL** (Commission Nationale de l'Informatique et des Libert&eacute;s) : [www.cnil.fr](https://www.cnil.fr)

---

## 9. Suivi des collaborateurs et droit du travail

CESYUM est un outil de suivi du temps de travail &agrave; usage professionnel. Le responsable du cabinet (employeur) qui d&eacute;ploie le Service est tenu de :

- Informer les salari&eacute;s de la mise en place du suivi (articles L.1222-3 et L.1222-4 du Code du travail)
- Consulter le Comit&eacute; Social et &Eacute;conomique (CSE) le cas &eacute;ch&eacute;ant
- Effectuer une analyse d'impact (DPIA) si n&eacute;cessaire
- S'assurer que le suivi est proportionn&eacute; et justifi&eacute; par un int&eacute;r&ecirc;t l&eacute;gitime

> L'application Desktop ne capture ni captures d'&eacute;cran, ni frappes clavier, ni contenu des documents. Seuls le nom du processus actif, le titre de la fen&ecirc;tre et l'URL (via l'extension) sont collect&eacute;s.

---

## 10. Cookies et stockage local

Le Service utilise :

- **Un cookie d'authentification** ("cesyum_auth") : strictement n&eacute;cessaire au fonctionnement du Service, expire &agrave; la fermeture du navigateur ou apr&egrave;s 30 jours si &laquo; Se souvenir de moi &raquo; est activ&eacute;
- **Le stockage local du navigateur** (localStorage) : pour conserver le jeton d'authentification et les pr&eacute;f&eacute;rences d'affichage

Aucun cookie tiers, cookie de pistage ou cookie publicitaire n'est utilis&eacute;.

---

## 11. Transferts de donn&eacute;es hors UE

CESYUM n'effectue aucun transfert de donn&eacute;es personnelles en dehors de l'Union europ&eacute;enne. L'ensemble des donn&eacute;es est trait&eacute; et stock&eacute; dans la r&eacute;gion AWS eu-west-3 (Paris, France).

---

## 12. Modifications de la politique

La pr&eacute;sente politique peut &ecirc;tre modifi&eacute;e pour refl&eacute;ter les &eacute;volutions du Service ou les exigences l&eacute;gales. Toute modification sera communiqu&eacute;e par e-mail ou notification dans le Service. La date de derni&egrave;re mise &agrave; jour est indiqu&eacute;e en haut de cette page.

---

## 13. Contact

Pour toute question relative &agrave; la protection de vos donn&eacute;es personnelles :

| | |
|---|---|
| **E-mail** | [contact@cesyum.com](mailto:contact@cesyum.com) |
| **Adresse** | CESYUM SAS &ndash; 181 Cours de l'Argonne, 33000 Bordeaux, France |

---

## Annexe : Extension navigateur CESYUM

### Donn&eacute;es collect&eacute;es par l'extension

L'extension collecte **uniquement des identifiants professionnels** sur les sites de logiciels comptables et de propri&eacute;t&eacute; intellectuelle :

| Donn&eacute;e | Exemple | Objectif |
|---|---|---|
| Nom de dossier client | "DUPONT SARL" | Identifier le client actif |
| Num&eacute;ro SIRET | 12345678901234 | Identifier le client actif |
| Nom du document | "Bilan 2024" | Contexte de l'activit&eacute; |
| P&eacute;riode comptable | "Exercice 2024" | Contexte de l'activit&eacute; |
| Activit&eacute; de navigation | Onglet actif, temps pass&eacute; | Cr&eacute;ation des feuilles de temps |

### Donn&eacute;es NON collect&eacute;es par l'extension

- Mots de passe
- Donn&eacute;es bancaires
- Contenu des documents
- Emails personnels
- Historique de navigation g&eacute;n&eacute;ral

### Sites concern&eacute;s

L'extension fonctionne **uniquement** sur :

**Logiciels comptables :** cegid.com, cegid.fr, sage.com, sage.fr, quadratus.fr, silae.fr, ebp.com, ebp.fr, isacompta.fr, acd-groupe.fr, pennylane.com, fulll.fr

**Sites administratifs :** impots.gouv.fr, urssaf.fr, net-entreprises.fr

**Propri&eacute;t&eacute; intellectuelle :** inpi.fr, data.inpi.fr, euipo.europa.eu, wipo.int, epo.org, espacenet.com, tmdn.org

L'extension n'acc&egrave;de &agrave; aucun autre site.

### Stockage des donn&eacute;es de l'extension

| Lieu | Donn&eacute;es | Dur&eacute;e |
|---|---|---|
| Votre navigateur | Param&egrave;tres extension | Jusqu'&agrave; d&eacute;sinstallation |
| Votre ordinateur (CESYUM Desktop) | Feuilles de temps | Jusqu'&agrave; suppression par vous |
| Serveurs CESYUM | Temps valid&eacute;s uniquement | Selon votre abonnement |

> **Important :** Les donn&eacute;es restent sur votre ordinateur tant que vous ne les validez pas.

### S&eacute;curit&eacute; de l'extension

- Communication locale uniquement (localhost)
- Aucune transmission internet sans votre validation
- Chiffrement HTTPS pour les synchronisations

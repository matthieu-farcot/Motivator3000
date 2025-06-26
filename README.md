# Motivator 3000

*L’assistant IA local et libre pour aider les lycéens à briller dans l’écosystème des stages professionnels.*

![Logo](./pictures/Motivator3000-Logo1.png "Logo")

Motivator 3000 est un projet du *Cormont Computer Club* du lycée Louis de Cormontaigne (Metz).

# Introduction au projet

**Le lien pour télécharger la démo avec le guide d'installation est en bas de la page.**

## Pourquoi l’usage "générique" de l’IA par les lycéens ne suffit pas
Avec la généralisation des outils d’intelligence artificielle accessibles en ligne, de nombreux lycéens ont commencé à utiliser des modèles comme ChatGPT, Gemini ou d’autres assistants IA pour générer leurs CV ou leurs lettres de motivation. Si cette démarche est compréhensible et peut sembler rassurante, elle pose plusieurs limites majeures.

### IA, synonyme de productions textuelles interchangeables
Les modèles d’IA généralistes, même performants, n’ont aucune connaissance réelle du parcours scolaire ou professionnel spécifique des lycéens, en particulier ceux de la voie professionnelle.
Résultat : les lettres générées sont souvent très semblables les unes aux autres, quel que soit :
- le métier visé (électricien, technicien réseau, agent de maintenance...),
- la formation suivie (MELEC, CIEL, Transition numérique...),
- l’annonce à laquelle l’élève répond.

Pire encore : dans un même lycée, plusieurs élèves utilisant les mêmes outils d'IA grand public peuvent se retrouver avec des lettres identiques, ce qui impact négativement la crédibilité de la production.

### IA, synonyme de contenu creux
La majorité des modèles produisent du texte en s’appuyant sur des probabilités de langage et des formulations génériques. Lorsqu’ils ne sont pas alimentés par des informations contextuelles précises, ils finissent par générer toujours les mêmes types de documents, qui manquent :
- de spécificité (compétences réellement acquises),
- de cohérence métier (liens entre formation et mission de stage),
- de personnalité (langage, centres d’intérêt, projet professionnel).

On retrouve systématiquement les mêmes formulations, comme :

"Je suis très motivé pour rejoindre votre entreprise et acquérir de l'expérience. Votre structure correspond parfaitement à mes aspirations professionnelles."

Ces phrases, bien que polies, n’ont aucune valeur différenciante et ne permettent ni de refléter la réalité du parcours de l’élève, ni de réellement convaincre un recruteur. La génération assistée d'une lettre de motivation doit passer par un processus d'adaptation du contenu à l'entreprise ciblée.

### IA, synonyme d'hallucinantes hallucinations 

A l'heure actuelle, toute IA est assujettie aux phénomènes d'hallucinations - des réponses fausses ou trompeuses présentées comme faits certains. Ceci est particulièrement vrai pour les IA locales, surtout si le choix d'architecture logicielle est volontairement fait de couper toute capacité de communication avec des serveurs et services distants - donc toute capacité de vérifier ou au moins partiellement valider une réponse par une recherche sur Internet (note: les raisons à cette coupure dans le projet Motivator 3000 sont exposées à la sous-section suivante portant sur l'importance du respect de la vie privée). Ce phénomène fait générer des réponses aux IA généralistes qui ne joue pas du tout en faveur de la crédibilité des productions réalisées (notre lycée fut ainsi faussement indiqué comme étant localisé à Dijon ou à Saint-Malo par deux IA distinctes lors de nos tests).

### IA, synonyme de normalisation de la mort de la vie privée 

La plupart des conditions générales d'utilisation (CGU) des IA généralistes accessibles via Internet sont explicites quand à la nature non confidentielle des données utilisées en entrée ou générées en sortie par leurs systèmes. Il est intérressant de noter que ces plate-formes semblent être assujetties à un trouble dissociatif de la personnalité (somme toute plutot classique à l'ère du Big Data) entre le discours commercial affiché qui insistera sur le respect de la vie privée, de la confidentialité des échanges (ou du contenu généré) et la transposition des ces "valeurs" dans le cadre légal d'utilisation de la même plate-forme qui renie tout cela sans état d'âme en se justifiant avec la notion d'intérêt légitime.

Nous pourrons citer par exemple la politique de confidentialité dans sa version effective au 27 mai 2025 de Mistral AI. Passé la page d'accueil du site qui insiste sur la protection de la vie privée et la confidentialité, ce service dans sa section "[3. Pourquoi utilisons-nous vos données personnelles ?](https://mistral.ai/fr/terms#privacy-policy)", indique que "pour entraîner les modèles d’intelligence artificielle sont utilisées avec *l'accord de l'utilisateur*" les "données personnelles éventuellement incluses dans des données publiquement accessibles sur Internet (...) et (les) données d’entrée et de sortie" (sous réserve d'un droit d’opposition et [dans le cas de l'usage de la version gratuite du web service](https://www.lefigaro.fr/secteur/high-tech/rgpd-mistral-ai-accuse-d-exploiter-illegalement-les-donnees-personnelles-de-ses-utilisateurs-20250212)).

La situation est similaire (voir encore plus problématique) pour les services d'accès et d'usage d'IA d'entreprises américaines comme [ChatGPT d'Open AI](https://www.edpb.europa.eu/system/files/2024-05/edpb_20240523_report_chatgpt_taskforce_en.pdf).

Plus largement, autant la [CNIL](https://www.cnil.fr/fr/deux-faq-utilisation-des-systemes-dia-scolaire) que le [ministère de l'éducation nationale](https://www.education.gouv.fr/cadre-d-usage-de-l-ia-en-education-450647) ont émis des recommendations claires sur ce sujet qui vont dans le sens d'un projet comme Motivator 3000 : il est recommandé de renoncer aux IA "grand public" (donc en ligne) quand des données personnelles sont en jeu dans le cadre scolaire.

La raison est simple. La protection de la vie privée et des données personnelles n'est pas qu'une norme. Cela doit être une règle absolue (en accord avec le RGPD).

## Motivator 3000 : une réponse adaptée, locale et "intelligente"

![Prototype sur LM Studio](./pictures/Screen4LMStudio.png "Prototype")

La plateforme Motivator 3000 a été conçue précisément pour répondre à ces limites, en proposant un assistant IA :
- contextualisé : il s’appuie sur les référentiels officiels des formations suivies par les élèves,
- personnalisé : il tient compte du profil de chaque utilisateur et de l’annonce à laquelle il répond,
- local : tout fonctionne sans connexion internet, sans cloud, dans le respect total du RGPD,
- libre : le projet est open source, modifiable, auditable, installable et utilisable le tout gratuitement dans n’importe quel établissement.

En combinant la puissance de l’intelligence artificielle avec (à terme) une architecture RAG (Retrieval-Augmented Generation) et un ancrage fort dans les parcours des lycéens, Motivator 3000 permettra enfin de produire des lettres et des CV crédibles, valorisants et réellement adaptés aux ambitions de chaque élève.

C’est une solution concrète pour accompagner les jeunes dans leurs premières démarches professionnelles — sans copier-coller impersonnel, sans cloud, et sans renoncer à l’exigence de qualité.

# Pourquoi ce nom ?
<img align="right" src="./pictures/motivator3000_SM.png" height="500">

Motivator 3000 est un clin d’œil assumé à l’esthétique rétro-futuriste des films de science-fiction de série B et des jeux vidéo vintage des années 80-90. Ce nom a été choisi pour plusieurs raisons stratégiques :

- Le rétro-gaming et l’univers néo-vintage sont très populaires chez les jeunes générations, en particulier chez les lycéens intéressés par les filières techniques ou numériques. Cela crée un lien culturel immédiat avec l’univers visuel et affectif des publics cibles.
- C’est aussi un clin d’œil ludique aux générations plus âgées, encadrants pédagogiques et développeurs, qui y verront une référence ironique aux titres comme RoboCop ou Megatron 3000.
- Ce côté kitsch et second degré a un fort pouvoir d’attractivité dans l’univers open source, souvent sensible à la culture geek, aux blagues techniques et aux projets qui assument leur identité avec humour tout en servant une cause utile.


En résumé, Motivator 3000, c’est un nom qui :
- donne envie de contribuer à un outil libre sympa et utile,
- crée de la curiosité et du capital sympathie,
- affirme une identité décomplexée et accessible, tout en assumant la puissance technique de l’IA embarquée.
 
# Objectif du projet
Développer un assistant logiciel local et libre, capable d’aider les lycéens de la voie professionnelle à :
- rédiger des CV valorisants et bien structurés,
- produire des lettres de motivation personnalisées à partir d’annonces de stage ou d’alternance,
- mettre en avant les compétences issues de leurs référentiels de formation.
 
## Un assistant boosté à l’IA (mais en local)
Le cœur de Motivator 3000 repose sur une IA embarquée, renforcée par une architecture RAG (Retrieval-Augmented Generation).


Le système permet à l’IA de générer des textes contextualisés à partir :
- des référentiels officiels des filières professionnelles,
- des annonces et contenu existant fournis par les élèves (PDF, copier/coller, etc.),
- de modèles de CV/lettres adaptés aux standards professionnels.

Le système permet aussi à l'IA de donner des conseils : en soumettant un cv et une offre d'emploi, il est possible de lui demander des avis sur les points forts et les aspects manquants à la candidature.
 
## RGPD : priorité absolue
Motivator 3000 fonctionne 100% en local, sans traitement distant, afin de garantir :
- le respect du RGPD, en particulier pour les élèves mineurs (certains des élèves considérés ont moins de 16 ans),
- la maîtrise complète des données, sans cloud, sans inscription, sans tracking,
- la possibilité de déploiement même sans connexion internet (réseau local ou poste unique),
- l'absence de stockage des ressources échangées, donc de toutes les donnees y inclut les données personnelles (par exemple les CVs mis à disposition par un élève ou générés par la plateforme ne sont pas conservés).
 
## Open Source et licence libre
Tous les développements sont publiés sous [AGPL v3](./Licence.txt), pour permettre :
- aux autres lycées et structures de déployer librement l’outil,
- aux enseignants, responsables de BDE ou DDFPT et développeurs de l’adapter et l’enrichir (par exemple avec d'autres référentiels académiques pour l'adapter à d'autres secteurs de formation),
- à la communauté de partager les améliorations en toute liberté.

# Motivator 3000, le point sur le projet :
Ce qui a été fait pour l’instant, ou est en cours de réalisation...
 
## Exploration des modèles IA open source adaptés à un usage local
Objectif : identifier des modèles de langage suffisamment puissants pour générer des contenus personnalisés (CV, lettres de motivation), mais légers et respectueux des contraintes locales (pas de cloud, pas de dépendance à des API commerciales).


Modèles testés :
1. Gemma (gemma-3-27b et gemma-3-12b)
2. Mistral (mistral-small-3.2)
3. LLaMA (llama-3.3-70b)
4. DeepSeek (deepseek-r1-0528)
5. Qwen (qwen3-8b)


Critères évalués :
- Qualité de génération (fluidité, structure)
- Capacité à tourner en local (sur CPU ou GPU)
- Volume mémoire et performance sur machine (très) modeste
- Capacité à suivre les instructions (system prompt)
- Influence des réglages de temperature du modèle (influence sur le niveau de créativité)

Pour retrouver ces évaluation, [rendez-vous sur la page dédiée](./benchmark.md).
 
Constat :  Malgré des performances linguistiques solides, les réponses produites par les modèles testés sont trop déterministes et génériques.
 Les lettres générées manquent de variabilité, d’originalité et surtout de prise en compte réelle du contexte scolaire et professionnel des lycéens. On observe que, quelle que soit l’annonce ou le profil fourni, les lettres finissent par se ressembler fortement, avec des tournures stéréotypées et un contenu souvent creux. Toutefois, vu les performances et les résultats obtenus, le choix pour l'instant porte sur Gemma-3-12b de google.


Globalement, ce comportement souligne les limites d’un modèle généraliste non enrichi, incapable d’ajuster sa réponse en fonction de référentiels métier ou de parcours spécifiques.  
Cela justifie pleinement l’adoption d’une architecture RAG (Retrieval-Augmented Generation), permettant de connecter l’IA à une base documentaire métier, adaptée aux formations professionnelles suivies par les élèves.
 
## Conception d’un système de prompt structuré
Objectif : formuler des instructions claires et précises pour guider les modèles dans leurs productions (system prompt).

Actions menées :
- Définition de plusieurs types de prompts : création de CV, lettre pour une alternance, lettre pour un stage, mise en valeur d’un projet scolaire, etc.
- Création de gabarits de prompt intégrant les données contextuelles (niveau d’étude, spécialité, type de poste ciblé, référentiel).
- Tests manuels pour évaluer la réactivité des modèles à ces instructions.

Résultat : Les prompts bien structurés améliorent la pertinence, mais ne suffisent pas en l’absence de connaissance métier spécifique au contexte du lycée professionnel. D’où la nécessité d’implémenter un système RAG avec accès aux référentiels académiques des matières professionnelles enseignées au Lycée Louis de Cormontaigne (Metz). Ceci sera la prochaine étape du projet.

# L'équipe projet

- Matthieu Farcot, Lycée Louis de Cormontaigne : Responsable de projet, Création site web, Création ressources graphiques, Choix plateforme
- Enzo Theveniaud, stagiaire 2PRO TNE (Transition Numérique et Enérgétique), Lycée Louis de Cormontaigne : Benchmarks, Recherche sur le system prompt, Travail sur le démonstrateur, génération des ressources de test
- Cédric Willigsecker Miot, stagiaire 2PRO TNE (Transition Numérique et Enérgétique), Lycée Louis de Cormontaigne : Modèle 3D du logo, Intégration A-Frame

# Accès à la béta

<img width="250" alt="image" src="https://github.com/user-attachments/assets/12833566-81ba-46db-aeec-76e8ba3462bb" />

La procédure d'installation et de configuration du [Motivator 3000 est par ici...](./guide-installation.md)

# Licence et propriété intellectuelle
Motivator 3000 - l'assistant numérique pour une pfmp réussie

Copyright (C) 2025 Cormont Computer Club - Lycée Louis de Cormontaigne - Matthieu Farcot

Ce programme est un logiciel libre : vous pouvez le redistribuer et/ou le modifier selon les termes de la Licence Publique Générale Affero GNU telle que publiée par la Free Software Foundation, soit la version 3 de la licence, soit (à votre choix) toute version ultérieure (voir le document licence.txt à la racine du projet).

Ce programme est distribué dans l’espoir qu’il sera utile, mais SANS AUCUNE GARANTIE ; sans même la garantie implicite de COMMERCIALISATION ou D’ADÉQUATION À UN BUT PARTICULIER.   Consultez la Licence Publique Générale Affero GNU pour plus de détails.



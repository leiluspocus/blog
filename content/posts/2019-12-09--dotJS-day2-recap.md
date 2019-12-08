---
title: Une journée à dotJS (Jour Backend 2)
date: "2019-12-09T19:23:42+00:00"
description: Débrief de la conférence dotJS Jour 2 à Paris en décembre 2019
template: post
draft: false
slug: /fr/recapitulatif-dotJS-jour2-decembre-2019
category: Developer Life
tags:
  - conferences
  - javascript
---

# Récapitulatif - dotJS 2019 

J'ai eu la chance d'assister à dotJS cette année grâce à des places qui ont été offertes par les dotConferences à la communauté <a href="https://paris.ladiesofcode.com/" target="_blank">Ladies of Code</a>. 

<a href="https://twitter.com/Jawache">@Jawache</a> a pris la parole sur notre impact environnemental en tant que développeur. L'électricité est responsable à 30% des émissions de CO2. On ne peut se permettre d'en gaspiller. 
Google Cloud serait un cloud Carbone neutral (ça m'étonne un peu).
Les servers produisent du carbone, on pollue moins avec le serverless.

Le serverless présente aussi des avantages économiques

- Autoscaling 
- On paie selon la durée et la consommation mémoire des fonctions que l'on exécute.


```
Nitr.ooo fireship.io = gcp functions nest.js
```

Si le sujet vous intéresse, consulter climateaction.tech pour s'impliquer plus.

__________________

<a href="https://twitter.com/devdevcharlie">@devdevcharlie</a> nous a montré les possibilités de recognition de sounds en exploitant la WebAudio API en javascript et le Machine Learning (avec TensorFlow). La WebAudio API récupère les données du microphone.

Sa démo présente un spectrogramme (la photo d'un son). Plus le son est fort, plus la couleur sur l'amplitude du spectrogramme est lumineuse.

Gather data from WEBAUDIOAPI and transforme it for tensorflow. Multidimensionnel array with labels for pattern recognition. La démo est accessible <a href="https://acoustic-ml.netlify.com">ici</a>, et c'est plutôt impressionnant : acoustic-ml.netlify.com

__________________

<a href="http://www.twitter.com/BertBelder">BertBelder</a> nous a présenté Deno, un runtime for JavaScript and Typesvript (webassembly) qui vise à résoudre les soucis que Node pose. Il utilise V8, Rust, Tokio (event.loop), TypeScript.

Node a un système de modules complexes, exposé aux failles et il existe un tas de tooling parallèle là où Deno a une API web et un tooling intégré.

_______

Quelques talks qui m'ont été recommandés en discutant durant les breaks: <a href="https://www.youtube.com/watch?v=qTHGmVrOGZo">Universe in a single arrow</a> et <a href="https://www.youtube.com/watch?v=yJDv-zdhzMY">Mother of all demos</a> (la première démonstration d'une souris, d'un clavier pour les amateurs d'images d'archive).


_______

@stefanjudis a donné un lightning talk super sur les expressions régulières. <a href="https://speakerdeck.com/stefanjudis/regular-expressions-my-secret-love">Les slides sont claires</a>, je vous recommande de les checker, une bonne piqûre de rappel pour les humains nuls en regexp comme moi ^_^

```
?: Omit captions group
?<rest> capture group
\p{Emoji} capture emoji 
```
_______

WebAssembly (wasm)
New los level bytecode format for the web. Now officially a web standard.

Librairies like pica use it. Improve performance. Benchmark and keep an eye on wasm module.

WebAssembly.studio

_____

<a href="https://twitter.com/mourner">Vladimir Agafonkin</a> (créateur de Leaftlet) a donné un talk sur l'optimisation d'algorithmes. 

Il a présenté le cas d'une bibliothèque Delaunay qui a subi plusieurs optimisations sur des modules npm. ( delaunay-fast // faster-delaunay // delaunator étant le plus rapide)

fond a bottleneck (slowest part). Profiling in Chrome.
Slow code does unnecessary code. Complexité a vérifier : check algorithm according to input size.

O(n) loop 
O(n2) o(n3) boucles imbriquées
Attention aux indexOf qui ont aussi grosse complexité.
accidentallyquadratic.tumblr.com

Memory complexity _ allocate Much memory than we need slice concat Map filter split.

O.log(n) best complexity.
Binary search.

Organisé data in some way to sort data faster. Do much at beginning (sort data) and less after.

HashTable -> array. Established in not the best.

1. Learn how things work under the wood ! Surtout dans les fonctions JS par défaut qu'on a  l'habitude d'utiliser.

________

Prettier dude.

James Long

Syncing offline apps is hard. Eventual consistency.

Unreliable ordering = setup timestamp to reorder.

Vector clock.
Hybrid logical clock. Exists per device. Generate timestamps assigned to changes.

Simple solution for reliability on distributed systems.

Conflicts :
Conflicts free replicated data types. Data structures with properties (commutative order don't matter). Idempotent.
Ensure consistency with Merkel tree.

____

Midi is not dead musical with JS. @nodebotanist

npm install midi tonal color

npm install ws (websocket)

______

@maggiepint
Programming in the 4th dimension

Date has problèmes.
Months index from 0. Mutability. Timezone gaps.
No date only représentation.

Temporal lib. 

_____

Daniel Ehrenberg
@littledan
tc39.es
# is the new _ for strong encapsulation.

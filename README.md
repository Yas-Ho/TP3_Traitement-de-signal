# TP3_Traitement-de-signal

# Objectifs:
Dans ce troisième Tp on cherche a Supprimer du bruit autour du signal produit par un électrocardiographefaire et faire la représentation temporelle et fréquentielle en utilisant la transformée de fourrier discrète sous le logiciel Matlab.

# introduction :
Un électrocardiogramme (ECG) est un test qui mesure l'activité électrique du cœur. Il est utilisé pour détecter des anomalies cardiaques telles que les troubles du rythme cardiaque, les infarctus du myocarde et les maladies cardiaques congénitales.

![image](https://user-images.githubusercontent.com/97410524/215348321-8b9dd98c-3004-4993-a6d6-1e3136676043.png)
L’onde P représente la première étape du cycle où les oreillettes (ou atriums) se contractent permettant le passage du sang, à travers les valves auriculoventriculaires, vers les ventricules. Ensuite, le complexe QRS symbolise à la fois la contraction ventriculaire (permettant l’éjection du sang vers les artères) notamment par le pic en R, dans le même temps,le relâchement des oreillettes entraîne le remplissage de celles-ci en attente d’un nouveau cycle).

L’onde T représente le relâchement des ventricules suite à leur contraction.L’enchaînement de ces complexes permet par ailleurs de déterminer la fréquence cardiaque, c’est-à-dire le nombre de cycle cardiaque par unité de temps. Une fréquence cardiaque normale est comprise entre 60 et 100 battements par minute, en dessous de cette valeur, le patient est en « bradycardie », au-dessus de cette valeur,le patient est en « tachycardie ».

Les signaux ECG sont contaminés avec différentes sources de bruits. Les bruits de hautes fréquences sont provoqués par l’activité musculaire extracardiaque et les interférences dues aux appareils électriques, et des bruits de basses fréquences provoqués par les mouvements du corps liés à la respiration, les changements physicochimiques induits par l’électrode posée sur la peau et les micro variations du flux sanguin. Le filtrage de ces bruits est une étape très importante pour faire un diagnostic réussi.

1 - Suppression du bruit provoqué par les mouvements du corps:

![image](https://user-images.githubusercontent.com/97410524/215348328-cba8dfea-c7c6-45ce-bdea-0b34a94dea29.png)

Son spectre d'amplitude :

![image](https://user-images.githubusercontent.com/97410524/215348334-b5a8a8b9-c60d-4ebe-9294-392ab26d5c92.png)

Ensuite on procède a supprimer le bruit des mouvements du corps en utilisant un filtrage idéal passe haut et on trace la différence par rapport au signal d'origine

![image](https://user-images.githubusercontent.com/97410524/215348343-82b0f0b6-5f64-4ea7-8b9c-8227a414ccc7.png)

2 - Suppression des interférences des lignes électriques 50Hz:
![image](https://user-images.githubusercontent.com/97410524/215348355-d6318c06-9fdc-4c01-b7f5-9d1dd3e0de9f.png)

On remarque qu'il y a un bruit qu'on doit éliminer avec un filtrage notch 3 - Suppression des interférences des lignes électriques 50Hz :
![image](https://user-images.githubusercontent.com/97410524/215348374-d0667603-75c7-49ac-9691-668a25873f3e.png)

On remarque que ce signal est encore bruité quand on le compare avec le signal ECG qu'on doit avoir. Pour eliminer ce bruit on applique un filtrage pass bas pour eliminer les bruits de basses fréquences.

ECG 2 apres le filtrage notch avec ses spectres et le bruit qui doit etre eliminer

![image](https://user-images.githubusercontent.com/97410524/215348398-391c048c-a162-494e-924b-904145863614.png)
4 - Amélioration du rapport signal sur bruit :

![image](https://user-images.githubusercontent.com/97410524/215348503-455fb19c-4316-4b49-8e16-8db618e7f307.png)

5 - Identification de la fréquence cardiaque avec la fonction d'autocorrélation : La fréquence cardiaque peut être identifiée à partir de la fonction d'autocorrélation du signal ECG. Cela se fait en cherchant le premier maximum local après le maximum global (à tau = 0) de cette fonction. On utilise la fonction xcorr pour le signal ecg3

![image](https://user-images.githubusercontent.com/97410524/215348417-0c036eda-0773-4623-a0b4-9cea89cc77f5.png)

On detecte une correlation dans un maximum a taux = 2

# ENCADRE PAR : Pr.Alae Ammour

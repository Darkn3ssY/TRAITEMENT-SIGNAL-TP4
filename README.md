# TP4 Filtrage analogique
# Objectifs :
Appliquer un filtre réel pour supprimer les composantes indésirables d’un signal.
Améliorer la qualité de filtrage en augmentant l’ordre du filtre.
# Introduction :
Le filtrage analogique est une technique utilisée pour séparer les différentes fréquences d'un signal analogique en utilisant des composants électroniques tels que des résistances, des condensateurs et des inducteurs. Il existe différents types de filtres analogiques, notamment les filtres passe-bas, passe-haut, passe-bande et coupure de bande, chacun ayant des caractéristiques de fréquence de coupure et de pente différentes. Les filtres analogiques sont utilisés dans une variété d'applications, telles que la radio, la télévision, la communication, les équipements audio et les instruments de mesure.

# 1 - Filtrage et diagramme de Bode :

![image](https://user-images.githubusercontent.com/90354895/215359074-2c32b7a9-afca-4500-a574-4b1238386439.png)

On Trace le signal x(t) et sa transformé de Fourrier

![image](https://user-images.githubusercontent.com/90354895/215359076-0a8cbc62-ac23-406e-bb55-d7ded40f3ece.png)

La transmittance complexe est un concept utilisé pour décrire la performance d'un filtre analogique ou d'un autre système de traitement de signal. Elle est définie comme le rapport entre la tension de sortie d'un système et la tension d'entrée, exprimé en tant que nombre complexe. La transmittance complexe est généralement exprimée en fonction de la fréquence, et elle peut être représentée graphiquement sur un diagramme de Bode, qui montre la fréquence en abscisse et la transmittance complexe en ordonnée. La transmittance complexe peut être utilisée pour déterminer les caractéristiques de fréquence d'un système, telles que les fréquences de coupure et la pente, ainsi que pour concevoir et optimiser les filtres et les autres systèmes de traitement de signal.

![image](https://user-images.githubusercontent.com/90354895/215359080-779921d9-079e-4def-8ab6-8879783c5c0f.png)

On trace le module de H, son gain et son déphasage avec T=0.0005

![image](https://user-images.githubusercontent.com/90354895/215359084-4ab2a9c1-07ba-4751-8fd6-c180d921e75e.png)

On applique sur le signal la transmittance complexe de frequence 1000

![image](https://user-images.githubusercontent.com/90354895/215359102-62a3281c-7ee3-40aa-ac3e-e5282af22194.png)

On remarque que les filtres analogiques sont moins efficaces que les filtres réels, on ne peut pas eliminer les bruits de basses frequances complétement, on pourra juste les diminuer.

# 2 - Dé-bruitage d'un signal sonore
Dans son petit studio du CROUS, un mauvais futur ingénieur a enregistré une musique en « .wav » avec un très vieux micro. Le résultat est peu concluant, un bruit strident s'est ajouté à sa musique. Heureusement son voisin, expert en traitement du signal est là pour le secourir :

« C'est un bruit très haute fréquence, il suffit de le supprimer. » dit-il sûr de lui.

On trace le signal et sa transformée de fourrier :

![image](https://user-images.githubusercontent.com/90354895/215359131-b4f31be8-9d29-4c63-bbef-e77ddee2fc38.png)
On remarque que dans le spectre suivant il y a une fréquence entre 4000 et 6000 d'amplitude 2 qui constitue le bruit, pour l'éiminer on doit appliquer un filtre passe bas qui nous permettra de diminuer l'intensité du bruit.

On utilise un filtre butterworth d'ordre 100 :

Spectre du signal apres l'application du filtre :

![image](https://user-images.githubusercontent.com/90354895/215359136-39fe3fd1-3b58-4e92-b1fc-6f5aa5b83221.png)

On remarque qu'on a pu éliminer le bruit.


# Encadré par : Prof Ammour Alae

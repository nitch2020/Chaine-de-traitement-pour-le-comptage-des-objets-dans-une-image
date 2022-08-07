# Chaine-de-traitement-pour-le-comptage-des-objets-dans-une-image
Il s'agit ici d'utiliser les techniques de présegmentation, segmenttion et de postsegmentation afin de compter les objets dans une image.
La segmentation est une étape de traitement d’image très importante dans la reconnaissance d’objets dans une image. On dispose d’un
ensemble d’images dont on souhaite compter les objets contenus dans les images. Pour y parvenir, trois principales étapes sont nécessaires à
savoir la Pré-Segmentation, la Segmentation et la post-segmentation.
# La Pré-Segmentation
Cette étape consiste à préparer les images avant la segmentation. En réalité nous disposons d’un ensemble d’images devant passer par le
même processus de traitement. Pour avoir de meilleurs résultats pour chaque image, nous devons choisir les techniques qui correspondent le
mieux pour chaque image en tenant en compte du contraste, de la luminance et des bruits dans l’image.Nous devons tout d’abord transformer l’image en une image en niveaude gris. Nous pouvons observer qu’il ya de petites différences entre cesimages. Sur certaines images on peut observer que les objets
contiennent les mêmes pixels que le background de l’image. Donc pour pallier ce genre de problème, nous pouvons améliorer le contraste de
l’image. Nous disposons de plusieurs techniques pour améliorer le contraste à savoir: Égalisation de l’histogramme, transformation linéaire
et non linéaire (correction gamma). Nous avons essayé l’égalisation de l’histogramme et la correction gamma.
#La Segmentation
Comme pour la pré-segmentation, pour la segmentation nous disposons aussi de plusieurs techniques divisées en deux principales approches à savoir, l’approche Régions et l’approche Contours. Dans notre cas nousallons utiliser le seuillage adaptatif et plus précisément le seuillage local adaptatif.
# Post-segmentation
Nous constatons que nous avons encore des régions connectées dans le résultats obtenu, ce qui ne nous permet pas de compter les objets
dans l’image. Nous appliquons donc l’érosion et la dilatation pour régler ce problème.
Nous disposons maintenant d’un objet par région, nous pouvons donc passer au comptage après l'avoir labéliser.

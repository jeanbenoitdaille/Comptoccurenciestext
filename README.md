# Comptoccurenciestext
Compter le nombre d'occurences dans un texte 
Exercice assez simple dans lequel il fallait juste prendre quelques précautions.

Le but de l'exercice était de compter le nombre d'occurence du mot "elit" dans le texte contenu dans la variable "lorem".

Peut-être avez-vous directement essayé d'utiliser la fonction count et cela ne fonctionnait pas.

Il fallait en effet quelque peut formater au préalable la chaîne de caractère.

Tout d'abord nous nous débarrassons de tous les signes de ponctuation, à savoir les virgules et les points, avec la méthode replace :

    lorem = lorem.replace(",", "").replace(".", "")

Pour réaliser cette opération en une seule ligne, nous n'hésitons pas à chaîner les méthodes replace l'une à la suite de l'autre.

Puisque notre script ne tiens pas compte de la casse, nous convertissons ensuite notre chaîne de caractère entièrement en minuscules :

    lorem = lorem.lower()

Il ne nous reste plus qu'à séparer les mots les uns des autres avec la méthode split :

    lorem_split = lorem.split()

Vous remarquerez que nous ne passons aucun caractère à la méthode split : en effet, par défaut la méthode split va séparer la chaîne de caractère sur les espaces si elle ne reçoit aucun argument.

Il ne nous reste pour finir plus qu'à utiliser la méthode count sur notre liste "lorem_split" pour compter le nombre d'occurrence du mot "elit" dans notre liste de mots :

    print(lorem_split.count(mot))

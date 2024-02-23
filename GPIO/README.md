## Devoir N°1 : Clignotement de LED avec bouton poussoir

L'énnoncé du premier devoir est le suivant : 

![énnoncé](https://github.com/Theo-Ledent/smartcities/assets/150011544/42e25efd-ff6e-42a6-96a7-e847264b5700)

Nous allons tout d'abord expliquer le code partie par partie suivant les consignes de base, ensuite nous passerons aux bonus.

# Code de base

Décortiquons ensemble le code. 

Premièrement, nous importons les librairies nécessaires au bon déroulement de notre programme et faisons le setup des pins.

![import](https://github.com/Theo-Ledent/smartcities/assets/150011544/1435da1d-f883-4801-86d5-a82920f01a58)


Ensuite, nous créons d'abord une variable **val** qu'on set à 0, puis une fonction permettant de compter le nombre de fois que le bouton est pressé. Ici comme il y a 3 modes différents, on reset le compteur quand il ateint la valeur 4.
Dans cette fonction, nous définirons la variable **val** comme global pour que la fonction comprenne qu'elle est aussi utilisée dans le reste du code.

![fonction1](https://github.com/Theo-Ledent/smartcities/assets/150011544/7f5e7836-7910-4fa4-95db-6975ec9e5d8c)


A présent, il faut créer une interruption permettant de détecter les fronts montants de notre bouton, soit quand il ests pressé.
Nous pouvons voir que dans cette interruption, nous précisons la pin, ce qu'il faut détecter, et ce que cette interruption doit faire.
Ici, l'interruption doit détecter un front montant sur la pin18. Quand c'est le cas, le code exécute la fonction **interruption_handler**.

![interruption](https://github.com/Theo-Ledent/smartcities/assets/150011544/2eaa56ac-1c97-4237-bea3-37be5739be63)


Regardons la boucle.
Pour le premier point, c'est très simple, il faut que la LED clignote avec une fréquence de 0,5s, soit une période de 2s. Je me suis donc trompé car en allumant la LED 0,5s et en l'éteignant 0,5s, la période est de 1s.
Cepandant pour l'expliquaation du code, cela ne rous dérangera pas car il est fonctionnel.
Nous pouvons donc voir que lorsque le bouton à été pressé une fois, on allume et ferme la LED avec une période de 1s.

![partie 1 boucle](https://github.com/Theo-Ledent/smartcities/assets/150011544/11a7d9d2-5a6d-4052-a010-9c235332263e)


Ajoutons les 2 autres modes.
Comme pour le mode 1, en fonction du nombre de fois que le bouton a été pressé, on rentre dans la condition voulue et remplissons la tâche demandée.
Pour le deuxièmemode mode, il faut que la LED clignote plus vite lorsque bouton est pressé 2 fois. On recopie donc le code du premier mode en diminuant les **utime.sleep()**.
Pour le troisième mode, c'est très simple, si on presse encore le bouton, la LED s'éteint.

![Partie 2et3 boucle](https://github.com/Theo-Ledent/smartcities/assets/150011544/145f5f47-3702-4af8-9e45-d8b2f35bcc9d)


# Bonus 1 : Ajout d'un effet lors du passage d'une vitesse de clignotement
L'effet qu'on ajoute ici est simple, on allumer la LED 1s quand le bouton poussoir est pressé. On l'ajoutera dans la fonction pour plus de simplicité.

![bonus 1](https://github.com/Theo-Ledent/smartcities/assets/150011544/7e5cd558-58f4-4c4a-9f81-96e53d8a2bb2)


# Bonus 2 : Modifier le nombre d'appuis nécessaires au passage à un autre mode
Pour le 2e bonus, on change la valeur de la variable **val** à 4 et à 7 pour les 2e et 3e modes.
Ensuite, on modifie légèrement la fonction pour faire l'effet le passage aux bonnes valeurs et on change la valeur de reset.

![bonus 2](https://github.com/Theo-Ledent/smartcities/assets/150011544/8ebdb9d2-e569-4ac5-9c80-e978f3e04c22)

# Code final

![code final](https://github.com/Theo-Ledent/smartcities/assets/150011544/6f08b16a-dc53-4106-862d-472c85c527b6)



# Support vidéo
Voici quelques GIF montrant le bon fonctionnement du code:

![partie 1](https://github.com/Theo-Ledent/smartcities/assets/150011544/d20d62bf-af3e-4039-a9de-4e920248767e)

![partie2](https://github.com/Theo-Ledent/smartcities/assets/150011544/61a3febb-0d61-4400-9177-5a1cb8bf22dd)

![partie3](https://github.com/Theo-Ledent/smartcities/assets/150011544/83561cd8-8f27-4637-a72d-e191990ce139)




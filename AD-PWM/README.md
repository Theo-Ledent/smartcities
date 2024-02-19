## Devoir N°1 : GPIO

L'énnoncé du premier devoir est le suivant : 

![énnoncé](https://github.com/Theo-Ledent/smartcities/assets/150011544/05708d74-411a-4a44-a233-7b4121b0a19e)


Nous allons tout d'abord expliquer le code partie par partie suivant les consignes de base, ensuite nous passerons au bonus.

# Code de base

Décortiquons ensemble le code. 

Premièrement, nous importons les librairies nécessaires au bon déroulement de notre programme.

![setup](https://github.com/Theo-Ledent/smartcities/assets/150011544/08b38f9d-3b37-4fdf-8924-dc928ffe2252)


Ensuite, dans une liste, nous rentrons les différentes fréquences qui composent la musique. Nous créons également une liste contenant les durées de ces fréquences.

![listeFreqDuree](https://github.com/Theo-Ledent/smartcities/assets/150011544/7376e8ee-28f6-4a57-b488-23736f2e28a4)


Nous créons ensuite une première fonction prenant une variable globale **vol** déclarées juste avant avec la variable du compteur **i**. Dans cette fonction, nous lisons la valeur du potentiomètre et la divions par 65,535 pour l'avoir sur une échelle de 1 à 1000 car 1000 est la valeur max que l'on peut mettre dans la commande plus bas.
Ensuite, nous faisons vibrer le buzzer à la fréquence voulue, au volume voulu et pendant la durée voulue.

![fonction1](https://github.com/Theo-Ledent/smartcities/assets/150011544/953a8f71-2a68-4585-98f1-a9ab6d2b0b98)


Enfin, nous jouns chaques notes les unes après les autres. Et quand on arrive à la fin de la liste, c'est à dire quand le compteur dépasse la longueur de la liste, on reset le compteur.

![image](https://github.com/Theo-Ledent/smartcities/assets/150011544/5e91eba8-c286-4366-aa67-b6f91ecf4065)

# Bonus 1

Pour le bonus, nous ajoutons une liste de durée et de fréqences permettant de jouer la marche impériale de Star Wars.
Ensuite, à la maniére du premier labo, nous créeons une fonction attachée à une interruption détectant les fronts montants d'un bouton. Cela permet de stoquer le nombre d'appuis sur ce bouton.

![fonction bonus](https://github.com/Theo-Ledent/smartcities/assets/150011544/d177c7ae-7b2a-4198-ba2e-e1b18f8616d0)


![bonus 1](https://github.com/Theo-Ledent/smartcities/assets/150011544/92f4ff53-7d34-4b75-8125-68056e0634e9)








# Code final

![code final](https://github.com/Theo-Ledent/smartcities/assets/150011544/b03d17ff-9344-4ce7-90a6-0c93b48aa6d5)


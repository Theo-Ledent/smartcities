## Devoir N°2 : Volume d'ue mélodie
L'énnoncé du second devoir est le suivant : 

![énnoncé](https://github.com/Theo-Ledent/smartcities/assets/150011544/05708d74-411a-4a44-a233-7b4121b0a19e)


Nous allons tout d'abord expliquer le code partie par partie suivant les consignes de base, ensuite nous passerons au bonus.

# Montage

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/f7b76dbe-1137-4f38-bb7e-70553dd25ced)


# Code de base

Décortiquons ensemble le code. 

Premièrement, nous importons les librairies nécessaires au bon déroulement de notre programme.

![setup](https://github.com/Theo-Ledent/smartcities/assets/150011544/08b38f9d-3b37-4fdf-8924-dc928ffe2252)


Ensuite, dans une liste, nous rentrons les différentes fréquences qui composent la musique. Nous créons également une liste contenant les durées de ces fréquences.

![listeFreqDuree](https://github.com/Theo-Ledent/smartcities/assets/150011544/7376e8ee-28f6-4a57-b488-23736f2e28a4)


Nous créons une première fonction prenant une variable globale **vol** déclarées juste avant avec la variable du compteur **i**. Dans cette fonction, nous lisons la valeur du potentiomètre et la divions par 65,535 pour l'avoir sur une échelle de 1 à 1000 car 1000 est la valeur max que l'on peut mettre dans la commande plus bas.
Ensuite, nous faisons vibrer le buzzer à la fréquence voulue, au volume voulu et pendant la durée voulue.

![fonction1](https://github.com/Theo-Ledent/smartcities/assets/150011544/953a8f71-2a68-4585-98f1-a9ab6d2b0b98)


Enfin, nous jouns chaques notes les unes après les autres. Et quand on arrive à la fin de la liste, c'est à dire quand le compteur dépasse la longueur de la liste, on reset le compteur.

![image](https://github.com/Theo-Ledent/smartcities/assets/150011544/5e91eba8-c286-4366-aa67-b6f91ecf4065)

# Bonus 1

Pour le bonus, nous ajoutons une liste de durée et de fréqences permettant de jouer la marche impériale de Star Wars.
Ensuite, à la maniére du premier labo, nous créeons une fonction attachée à une interruption détectant les fronts montants d'un bouton. Cela permet de stoquer le nombre d'appuis sur ce bouton.
Dans cette fonction, on reset également le compteur pour recommencer les musique depuis le début.

![fonction bonus](https://github.com/Theo-Ledent/smartcities/assets/150011544/d177c7ae-7b2a-4198-ba2e-e1b18f8616d0)

Cela nous permet de pouvoir changer de musique en vérifiant l'état du bouton. Si le buton est à 0, on joue la première musique, et si il est à 1, on joue la 2e.

![bonus 1](https://github.com/Theo-Ledent/smartcities/assets/150011544/92f4ff53-7d34-4b75-8125-68056e0634e9)


# Code final

![code final](https://github.com/Theo-Ledent/smartcities/assets/150011544/b03d17ff-9344-4ce7-90a6-0c93b48aa6d5)

# Support vidéo

Voici la première mélodie.

https://github.com/hepl-ledent/smartcities/assets/150011544/7f132821-1232-4dcb-b2eb-fb279032350c

Ensuite, lorsque j'appuie sur le boutton, le code joue la 2e mélodie. Nous remarquerons que chatGPT n'est pas très doué pour générer des mélodies. Il y a également un problème lorsque le buzzer joue une note précise.

https://github.com/hepl-ledent/smartcities/assets/150011544/c88771fa-def1-4675-ab11-5519c7f155fe







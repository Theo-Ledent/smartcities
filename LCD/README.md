## Devoir N°3 : Système de contrôle de température
L'énnoncé du second devoir est le suivant : 

![énnoncé3](https://github.com/hepl-ledent/smartcities/assets/150011544/251c55c6-94b8-4d81-a900-0e482232a7f9)



Nous allons tout d'abord expliquer le code partie par partie suivant les consignes de base, ensuite nous passerons au bonus.

# Code de base

Décortiquons ensemble le code. 

Premièrement, nous importons les librairies nécessaires au bon déroulement de notre programme et faisons le setup des pins.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/71b6071d-e11b-433d-afa2-8fe4ba96e1d2)


Avant de créer nos fonction, nous faison le setup de nos pins, nous créons nos variables et faisons le setup de l'écran LCD.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/ba0181de-a52b-4f1d-97c5-b3d81d8f8907)



Nous créons une fonction **Mesure()** qui nous permettra de connaitre l'état dans lequel nous nous situons : 
  - **Etat 1** : La température mesurée est supérieure de 3 degrés à la température de consigne
  - **Etat 2** : La température mesurée est supérieure à la température de consigne
  - **Etat 3** : La température mesurée est inférieure à la température de consigne

Cette fonction lit et compare la valeur définie par le potentiomètre (traduite entre 15 et 35°C) et la valeur mesurée par le capteur de température.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/b8f34c8b-5090-46fe-8e85-896bedd7e8c8)

Enfin, expliquons la boucle **While** du code. 
Premièrement, nous mettons un **sleep** de 0,1s. Nous Incrémentons une untité au compteur, appelons la fonction **Mesure()** et affichons l'état et le compteur.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/e9a0f643-a0f2-4673-addb-83406a728fc5)

Ensuite, en fonction de l'état, nous réalisons le travail demandé.

Tout d'abord, lorsque nous ne sommes pas dans l'état 1, nous affichons la température de consigne et la température mesurée. Nous actualisons ces températures toues les secondes.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/4d78d78f-2aa3-416e-b340-f87bcc9678e6)

Dans le premier état, nous inversons l'état de la LED toutes les 0,1s soit la durée du **sleep**. Avec une période de 1s, nous affichons également le mot **"ALARM"** sur l'écran. Nous faisons aussi aller le buzzer à une fréquence de 1000Hz.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/83c369f1-f13e-48cc-bc02-0b82ff6fa855)


Dans le second état, nous faisons simplement clignoter la LED avec une période de 2s en changeant son état toutes les secondes. Nous mettons également le duty cycle du buzzer à zéro pour éteindre celui-ci.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/61fabb52-a2e5-4269-8247-125818a429cb)

Ici, nous mettons le comtpeur à zéro lorsqu'il atteint la valeur 2O.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/82462192-fde3-4ebf-9594-86ff4f6d1628)


# Bonus : Faire clignoter le mot **ALARM** sur l'écran LCD

Nous créons simplement une variable **screen** pour stocker l'état de l'écran (allumé ou éteint) et allumons ou éteingons l'écran toutes les 0,5s.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/255e2b82-b209-46d5-9326-ae8f95f1a2c1)

# Code complet

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/596434b0-a015-4c3e-881f-73febd84520c)
![image](https://github.com/hepl-ledent/smartcities/assets/150011544/6e1d3541-78bd-4114-bdb0-07a41516b23b)














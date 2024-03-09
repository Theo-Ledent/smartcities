## Devoir N°3 : Système de contrôle de température
L'énnoncé du second devoir est le suivant : 

![énnoncé3](https://github.com/hepl-ledent/smartcities/assets/150011544/251c55c6-94b8-4d81-a900-0e482232a7f9)



Nous allons tout d'abord expliquer le code partie par partie suivant les consignes de base, ensuite nous passerons au bonus.

# Code de base

Décortiquons ensemble le code. 

Premièrement, nous importons les librairies nécessaires au bon déroulement de notre programme et faisons le setup des pins.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/71b6071d-e11b-433d-afa2-8fe4ba96e1d2)


Avant de créer nos fonction, nous faison le setup de nos pins, nous créons nos variables et faisons le setup de l'écran LCD.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/82017a30-0037-4d0f-8ab7-1a520ac6c07a)


Nous créons une fonction **Mesure()** qui nous permettra de connaitre l'état dans lequel nous nous situons : 
  - **Etat 1** : La température mesurée est supérieure de 3 degrés à la température de consigne
  - **Etat 2** : La température mesurée est supérieure à la température de consigne
  - **Etat 2** : La température mesurée est inférieure à la température de consigne

Cette fonction lit et compare la valeur définie par le potentiomètre et la traduit entre 15 et 35°C et la valeur mesurée par le capteur de température.

![image](https://github.com/hepl-ledent/smartcities/assets/150011544/b8f34c8b-5090-46fe-8e85-896bedd7e8c8)












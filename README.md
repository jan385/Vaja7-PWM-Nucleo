# Vaja7-PWM-Nucleo
1.
b) Prvi kanal aktivirajte kot PWM Generation CH1. Kateri pin ste omogočili? Kaj se izpiše poleg njega?

Omogočili smo PA8. Zraven se izpiše TIM1_CH1

d) Vrednost Prescaler v zavihku Counter Settinngs določite tako, da bo časovnik delal s frekvenco 1 Mhz. Koliko je vrednost Perscaler?

Vrednost Perscalerja je 16

e)Parameter Counter Period nastavimo na 100 in s tem še dodatno znižamo takt časovnika. Koliko znaša sedaj?

Sedaj znaša 10khz

f) V PWM Generation Chanel nastavite Pulse na 50. Kaj pomeni ta parameter?

Pomeni širino pulza

2.
c) Poiščite prenastavljeni parameter Pulse (ki je 50) v vaši kodi in prepišite ukaz ki ga je generiral CubeMX.

sConfigOC.Pulse = 50;

3.
a) V kodi spremenite vrednost širine pulza na 25%. Zapišite popravljeni ukaz v kodi.

sConfigOC.Pulse = 25;

c) Zapišite kaj počnejo ukazi v 1., 2. in 3. vrstici

1)Na začetku zanke program nastavi htim1.Instance->CCR1 na vrednost spremenljivke dutyCycle.

2) Vsakič ko program loopa skozi to vrstico doda spremenljivki dutyCycle + 10.

3) Preveri, če je vrednost dutyCycle-a večja od 90, če je potem nastavi dutyCycle nazaj na 10, kar pomeni da je to neskončna zanka.


Komentar: Sprogramirali smo mikroprocesor tako, da bomo generiral PWM signal in ga tudi krmilili na izbranem izhodu STM Nucleo-L476RG. 
 


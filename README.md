## 1. Detalii Tehnice:
  Led-ul RGB reprezintă disponibilitatea stației. Dacă stația este liberă led-ul va fi verde, iar dacă stația este ocupată se va face roșu.

  Led-urile simple reprezintă gradul de încărcare al bateriei, pe care îl vom simula printr-un loader progresiv (L1 = 25%, L2 = 50%, L3 = 75%, L4 = 100%). Loader-ul se încarcă prin aprinderea succesivă a led-urilor, la un interval fix de 3s. LED-ul care semnifică procentul curent de încărcare va avea starea de clipire, LED-urile din urma lui fiind aprinse continuu, iar celelalte stinse.

  Apăsarea scurtă a butonului de start va porni încărcarea. Apăsarea acestui buton în timpul încărcării nu va face nimic.

  Apăsarea lungă a butonului de stop va opri încărcarea forțat și va reseta stația la starea liberă. Apăsarea acestui buton cât timp stația este liberă nu va face nimic.

  ## 2. Flow:
  Starea stației este ‘liberă’. Loader-ul este stins, iar led-ul pentru disponibilitate este verde.

  Se apasă butonul pentru start.

  Led-ul pentru disponibilitate se face roșu, iar încărcarea începe prin aprinderea primului LED L1.

  Led-ul 1 clipește timp de 3s, celelalte fiind stinse.

  După încărcarea primului procent de 25% led-ul rămâne aprins și se trece la următorul led, care va începe să clipească.

  La finalizarea încărcării toate led-urile vor clipi simultan de 3 ori, iar apoi se vor stinge, pentru a semnaliza finalizarea procesului.

  Led-ul pentru disponibilitate se face verde.

  Dacă oricând de la pornirea încărcării până la finalizarea acesteia este apăsat lung (min 1s) butonul de stop, încărcarea se întrerupe prin animația de final (toate led-urile clipesc de 3 ori), iar led-ul pentru disponibilitate devine verde.



## Componentele folosite:
  - Arduino UNO (ATmega328P microcontroller)
  - 1x LED RGB (pentru a semnaliza dacă cuvântul corect e scris greșit sau nu)
  - 2x Butoane (pentru start/stop rundă și pentru selectarea dificultății)
  - 5x Rezistoare (3x 220/330 ohm, 2x 1000 ohm)
  - Breadboard
  - Fire de legătură

  ![img](./poze/image2.jpeg)
  
## Schema electrica a circuitului implementat pe Wokwi
  
![img1](./poze/image3.jpeg)

## Imagini cu Setup-ul Fizic

![img3](./poze/image1.jpeg)

![img2](./poze/image.png)

## link video:
  https://youtube.com/shorts/Hxhs5Td3ljg?si=jBow3Uvh0U9tc2a5

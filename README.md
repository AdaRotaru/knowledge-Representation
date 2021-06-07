# Laboratorul de inteligenta artificiala (kr)


1. Turn Based Game

jocul are interfata grafica realizata cu pygame

Jocul se desfasoara pe un grid NxM cu 10≥N,M≥5, macar unul dintre M, N trebuie sa fie par (utilizatorul va fi întrebat în legătură cu dimensiunea tablei).

Un jucator foloseste simbolul x si celalalt 0 ( o sa ii numim pe scurt jucatorii x si 0)
Jucatorul x pune simbolul primul pe tabla.
Simbolurile se pun in locurile libere ale tablei. In momentul in care o casuta libera e inconjurată (pe linie, coloana, diagonala) de minim 4 simboluri de acelasi fel (iar celalalt jucator are mai putine simboluri in jurul casutei libere), casuta este marcata cu simbolul majoritar din jurul ei. Daca in urma marcarii exista o alta casuta libera care acum are minim 4 simboluri in jurul ei, este marcata si aceea pana nu mai exista casute libere in aceasta situatie. Daca sunt in jurul unei casute sunt mai mult de 4 simboluri si de-ale lui x si de-ale lui 0, numarul de x si de 0 e egal, casuta ramane necompletata, pana se schimba situatia.

De exemplu, în imaginea de mai jos, presupunem că ultima mutare a lui x este x-ul albastru. Deoarece s-au adunat 4 simboluri x vecine față de o căsuță liberă, este adaugat automat x-ul verde. În urma adăugării lui avem o altă poziție cu 4 vecini x, cea pe care s-a pus x-ul portocaliu, care duce la adăugarea x-ului roz, și apoi a celui mov:

![image](https://user-images.githubusercontent.com/58121806/121063088-8f854b80-c7ce-11eb-9b81-20de589014e6.png)



2. 8-puzzle problem 

Se da un grid NxN, cu N impar si doua seturi de placute, numerotate de la 1 la (N*N)div2 

o placuta se poate muta pe linie, coloana sau diagonala in locul liber (daca, evident, locul liber este vecin cu plăcuța), iar costul mutarii este egal cu valoarea inscrisa pe placuta + linia de pe care se mută (de exemplu, dacă se mută plăcuța 4 de pe linia 3, costul e 7) 
Când vorbim de locurile din jurul unei plăcuțe ne referim la cei 8 vecini posibili 

o plăcuță nu se poate muta într-un loc cu proprietatea că e înconjurat de mai multe plăcuțe de paritate diferită de a ei și, în același timp, există minim o plăcuță de paritate diferită aflată pe linia de mai sus, cu număr mai mare decât numărul plăcuței de mutat. De exemplu, o plăcuță cu număr impar se poate muta într-un loc cu 4 vecini impari și 4 pari. Plăcuța nu se poate muta într-un loc cu 5 vecini impari unde pe oricare dintre cele 3 locuri de pe linia de mai sus, vecine cu poziția plăcuței, există macar un număr mai mare decât numărul plăcuței. Condiția asta nu se aplică și stării inițiale (în starea inițială pot exista placuțe înconjurate de oricâți vecini de paritate diferită chiar dacă dintre ei unii au număr mai mare decât plăcuța și sunt pe linia de mai sus).
O stare e considerata finala cand configurata e simetrica (fata de axa care parcurge puzzle-ul pe verticala, pe mijlocul tablei de joc).

![image](https://user-images.githubusercontent.com/58121806/121062856-433a0b80-c7ce-11eb-9958-9b24daad2132.png)
![image](https://user-images.githubusercontent.com/58121806/121062881-4b924680-c7ce-11eb-906c-adb8fc7017a5.png)







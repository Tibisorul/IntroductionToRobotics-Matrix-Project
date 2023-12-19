# IntroductionToRobotics-Matrix-Project
Acesta este primul proiect din cadrul materiei "Introducere in Robotica", anul III, Calculatoare si Tehnologia Informatiei,sustinuta de profesorul Dumitru Andrei si de laborantul Surdu Alexandru. Proiectul presupune implementarea unui joc pe matricea LED 8x8 impreuna cu un LCD si alte componente alese optional de fiecare student. Eu am ales sa realizez jocul "Snake" impreuna cu un meniu interactiv care sa ofere jucatorului o experienta placuta.

Deadline: 19 Decembrie 2023

![image](https://github.com/Tibisorul/IntroductionToRobotics-Matrix-Project/assets/127014075/6e489eea-1dd8-4eda-82ec-a0968175ed4d)


#### Componentele utilizate:
- Matrice LED 8x8 (1): Prin intermediul acestei componente este posibila afisarea joculetului meu.
- LCD(1): Aceasta componenta este responsabila cu afisarea meniului si a altor functionalitati care sunt implementate in cod.
- Joystick(1): Se ocupa cu manipularea sarpelui de pe matrice, dar si cu manipularea meniului si a functionalitatilor care sunt afisate pe LCD.
- Buzzer(1): Datorita acesteia sunt redate sunete, pentru o utilizare mai placuta a jocului.
- LED (2): Avem doua LED-uri, rosu, respectiv verde. Cel verde este utilizat atunci cand sarpele "prinde" fructele, iar cel rosu este utilizat atunci cand sarpele se loveste.
- Rezistoare si fire: Prin intermediul acestora sunt conectate componentele.
- Arduino Board: placa Arduino este componenta centrală a acestui proiect, care integrează și coordonează toate celelalte elemente hardware pentru a oferi o experiență interactivă și personalizabilă utilizatorului.

#### Prezentarea functionalitatilor:

> [!IMPORTANT]  
> Optiunea Highscores nu este momentan disponibila, din oricina mai multor bug-uri. Spre exemplu, am adaugat mai multe "Serial.print-uri" pentru a deduce de unde vine problema, iar in Serial Monitor imi afiseaza corect numele utilizatorilor si scorul acestora, dar pe LCD, odata ce apas pe optiunea "Highscores" nu afiseaza nimic (pur si simplu o pagina goala).

1) Informatiile de tip "Intro": Odata rulat codul, se vor afisa la inceput informatii de tip Intro.
2) Autentificare prin selectarea Nickname-ului dorit: Sunt afisate pentru fiecare spatiu literele de la "A-Z", pentru confirmarea caracterului dorit este necesara apasarea butonului de la Joystick. La final pentru a salva numele dorit, se asteapta cateva momente pana cand se va afisa mesajul "Hold btn to save", iar atunci trebuie tinut apasat butonul Joystick-ului pana cand isi va face aparitia alt mesaj: "Nickname salvat".
3) Meniul: Contine 4 functionalitati:
   - Start Game: Atunci cand este apasata aceasta optiune se va afisa pe ecranul LCD: scorul si numarul de vieti ramase. De asemenea, va fi derulat pe matricea LED 8x8 jocul Snake, iar prin intermediul Joystick-ului este necesara manipularea acestuia pentru colectarea fructelor. Pe masura ce cresti in nivel, dificultatea creste, in sensul ca sarpele se va misca mai repede.
   - Settings: Acesta practic este un submeniu care are incorporat si el 4 functionalitati, si anume: "LCD Brightness", prin care se poate selecta luminozitatea dorita a LCD-ului, "Matrix Brightness", prin intermediul careia se poate modifica luminozitatea dorita a matricei, "Sound", se selecteaza optiunea dorita prin care utilizatorul doreste sau nu sa aiba parte de sunete emise de la buzzer, si "Exit to Meniu" care ne conduce inapoi la meniul principal. De mentionat este faptul ca la "LCD Brightness" si "Matrix Brightness" salvarea se realizeaza prin apasarea mai lunga a butonului pe care il are Joystick-ului, iar la "Sound" se realizeaza automat. Salvarea optiunilor dorite se realizeaza prin intermediul bibliotecii "<EEPROM.h>".
   - "How To Play": Sunt derulate cateva reguli pentru a ajuta utilizatorul cu informatii legate de joc.
   - "Highscores": Sunt afisate numele celor care s-au autentificat impreuna cu scorul acestora (doar primele 5 cele mai mari scoruri sunt afisate).
4) Informatiile de tip AFK(sau About): Aceste informatii sunt afisate atunci cand sistemul detecteaza o inactivitate. Informatiile despre autorul proiectului sunt derulate automat incontinuu pana cand sistemul detecteaza o manipulare a Joystick-ului, astfel se va reveni la meniu.

Mai jos voi prezenta video functionalitate joculetului meu:

### [YouTube Video Showcase](https://www.youtube.com/watch?v=mD_BZTL-Vys) 


#### Bug-uri intalnite:
 - Atunci cand sarpele mananca fructul, se aprinde random, dar temporar un LED pe matrice.
 - In timp ce cresc luminozitatea matricei, scade luminozitatea LCD-ului.
 - Daca nu se alege corect si in timp util numele utilizatorului, nu mai merge butonul Joystick-ului atunci cand doresti sa selectezi o optiune din meniu.
 - Bug-ul la optiunea Highscore mentionat mai sus in categoria "Prezentarea functionalitatilor".
 - (?)Daca la alegerea numelui nu selectezi niciun caracter, va interveni mesajul de "Hold btn to save".
 - (?)Informatiile de tip AFK pot fi neplacute, in sensul ca s-ar putea sa apara cand nu este nevoie.

Pentru a nu risca depunctarea, domnul profesor de la curs ne-a rugat sa mentionam sursele bibliografice sau de unde ne-am inspirat. Mentionez faptul ca nu m-am inspirat de la niciun coleg din anii trecuti sau din anul actual, ci doar am fost ajutat de AI, si anume ChatGPT acolo unde a fost cazul.
Bibliografie: 
 






# Översikt
I denna repo ska jag demonstrera grundläggande kunskaper i att genomföra ett Blink-program med två typiska basfunktioner, samt konfiguration av Arduino.


# Arduino
Efter att ha installerat Arduino IDE behöver man konfigurera nödvändiga inställningar för att kunna sammanställa och ladda upp kod som skickas sen till Arduino kortets mikrokontroller via USB-kabeln, genom att följa nedanstående instruktioner:

## Konfiguera Boards Manager:

1. Navigera till och öppna Arduino.
2. Gå till file ➡️ preferences.
3. När du är väl inne på preferenser, kopiera följande URL in i Additional Boards Manager: https://arduino.esp8266.com/stable/package_esp8266com_index.json Tryck sedan OK.
4. Gå vidare till Board Manager, sök då efter ESP8266 och installera.
5. Navigera till tools ➡️ Board ➡️ ESP8266  ➡️ Generic ESP8266 Module

<img src="https://github.com/user-attachments/assets/35b565ce-ff8b-4d5f-a04a-5d60373a02f9" width="75%">



Du har nu konfigurerat ditt valda Plusivo Board!


# Två Basfunktioner
Inom Arduino programmering, och liknande program, använder man sig av två basfunktioner: void setup () och void loop (), vilka fungerar som startpunkten för programmeringen samt vilka roller/funktioner man vill att den ska kunna då utföra

<img width="113" height="74" alt="Screenshot 2025-12-05 at 08 22 51" src="https://github.com/user-attachments/assets/3c47b449-0e45-496f-ba88-f8b8e5f9bc59" />


🔵 Void setup () körs en gång när programmet startar upp. Här bör man alltså placera sånt som ska förberedas innan programmets funktion börjar, ex. Att ställa in I/O-pinnar.

🔵 Void loop () körs upprepade gånger, så länge Arduino är påslagen och aktiv. Här placeras alltså funktionerna du vill att den ska kunna utföra, ex. Att läsa sensorer och skicka datan till en databank.

# Blinkprogram

Går man in på file ➡️ Examples ➡️ 01. Basics ➡️ Blink, så hittar du ett färdiggjort exemple av kod till ett Blinkprogram.

<img width="634" height="415" alt="IMG_2442" src="https://github.com/user-attachments/assets/95fb7b2d-a8c7-4927-b307-fb92dbff1578" />

# Kod

Koden nedanför styr den inbyggda LED-lampan som finns på ett Arduino kort så att den blinkar med intervall. *Void setup ()* körs en gång när Atduino startas eller återställs, då ställs den in inbyggda LED in som en utgång med hjälp av *pinMode(LED_BUILTIN, HIGH);* . Det här gör så att Arduino kan skicka signaler för att tända eller släcka lampan.

*Void loop ()* Som körs kontinuerligt tänder programmet med 1000 millisekunders mellanrum med kommandot *delay (1000);* vilket skapar en blinkande effekt genom att använda kommandona *digitalWrite(LED_BUILTIN, HIGH);* och *digitalWrite(LED_BUILTIN, LOW) ;* . Slutligen så avslutas processen med hjälp av måsvingen *}* .


<img width="650" alt="IMG_2443" src="https://github.com/user-attachments/assets/c100c7c2-7617-4c8f-8cd2-3eea4f05e850" />







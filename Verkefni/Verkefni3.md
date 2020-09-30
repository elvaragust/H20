## Verkefni 3 -  IoT Samskipti (20%) _drög_

Einstaklingsverkefni<br>
Tími: 3 vikur

---

#### 3.1. Arduino og Raspberry Pi (1%)
  1. Hver er munurinn á Arduino Uno og Raspberry Pi, nefndu helstu atriði?
  1. Hvenær og afhverju getur það verið gagnlegt að tengja Arduino og Raspberry Pi saman? Komdu með dæmi.
  
---

#### 3.2 Serial tenging, Arduino til RPi (2%)
Fylgdu tutorial: [How to Connect and Interface a Raspberry Pi With an Arduino](https://maker.pro/raspberry-pi/tutorial/how-to-connect-and-interface-raspberry-pi-with-arduino)
  - Láttu Arduino senda strenginn “Hello from Arduino” til Raspberry Pi. Raspberry Pi við móttöku prentar út strenginn og lætur LED blikka.
  - **Ath** Laga þarf kóðann í tutorialnum `if` skilar ekki `True`. Hér er lagfærður kóði með decode() og strip(): 
  
    ```
    while True:

      read_ser=ser.readline()
      msg = read_ser.decode('utf-8') # To convert byte strings to Unicode, líka hægt að nota bytes.decode(read_ser)
      print(msg) 
      if(msg.strip()=="Hello From Arduino!"):
          blink(11)
    ```
   - Ef þú færð meldinguna `IndentationError: expected an indented block` þá þarftu að hreinsa til autt svæði(tab/enter) í python kóðanum


#### Bjargir

- [Raspberry Pi Arduino Serial Communication – Everything You Need To Know](https://roboticsbackend.com/raspberry-pi-arduino-serial-communication/)
- [pySerial documentation](https://pythonhosted.org/pyserial/)
- [Python 3 Unicode and Byte Strings](https://blog.feabhas.com/2019/02/python-3-unicode-and-byte-strings/#:~:text=To%20convert%20byte%20strings%20to%20Unicode%20use%20the%20bytes.,than%20UTF%2D8%20is%20required.)


---

#### 3.3 Serial tenging, RPi til Arduino (2%)
Fylgdu tutorial: [Connect Your Raspberry Pi and Arduino Uno!](https://www.instructables.com/id/Connect-Your-Raspberry-Pi-and-Arduino-Uno/)
  
  - Skrifaðu og keyrðu Arduino kóðann í Arduino IDE í Raspberry Pi.
  - **Ath** Notaðu `str.encode()` til að breyta Unicode streng í bytes til að kóði virki.
  
---

#### 3.4 Bluetooth tenging, RPi til snjallsíma (2%)
Fylgdu tutorial: [Connect Your Raspberry Pi and Smartphone via bluetooth !](https://bluedot.readthedocs.io/en/latest/gettingstarted.html)
Munið að fylgja leiðbeiningum vel (ath lesa hverja síðu og fara í NEXT neðst á síðunni), ekki gleyma neinu!!!
  
  - Verkefnið er að rasberryPI prentar út "Hello World" þegar þið smellið á Blue Dot í síma ykkar (gera while true lúppu svo þið getið 
    smellt aftur og aftur.
  - [Blue Dot API](https://bluedot.readthedocs.io/en/latest/dotapi.html#module-bluedot)
  
---

#### 3.5 Bluetooth tenging, RPi til snjallsíma og LED (2%)
Fylgdu tutorial: [Bluetooth and BlueDot with LED !](https://bluedot.readthedocs.io/en/latest/recipes.html#flash-an-led)
  
  - Verkefnið er að rasberryPI kveikir á LED þegar smelt er á Blue Dot í snjallsíma :-) sem þýðir að þið verðið að tengja eina LED peru í breadboard
    og viðeigandi viðnám (reiknið) og tengja við RaspberryPi (ath gera while true lúppu svo þið getið 
    látið led blikka þegar smellt er á BlueDot). 
  -  Unnið er með [GPIOZero](https://www.raspberrypi.org/documentation/usage/gpio/python/) sem er þegar sett upp í RPi OS (default)
  
---

#### 3.6 Bluetooth tenging, RPi til snjallsíma og Myndavél (2%)
Fylgdu tutorial: [Bluetooth and BlueDot using remote camera !](https://bluedot.readthedocs.io/en/latest/recipes.html#remote-camera)
  
  - Verkefnið er að rasberryPI tekur mynd þegar smelt er á Blue Dot í snjallsíma :-) sem þýðir tenging við video :-)
  
---

#### 3.7 Bluetooth og Serial tenging (3%)

- Notaðu BlueDot með RaspberryPi til að kveikja á RGB LED peru sem er tengd við Arduino. 
- Það á að vera hægt að velja um 4 mismunandi liti með BlueDot.
- Getur þú látið BlueDot virka með fleiri litum?

---

#### 3.8 SPI (1%)
Kynntu þér Serial Peripheral Interface (SPI). Sjá t.d. [Introduction to SPI Interface](https://www.analog.com/en/analog-dialogue/articles/introduction-to-spi-interface.html) og [SPI](https://learn.sparkfun.com/tutorials/serial-peripheral-interface-spi/all) og svaraðu eftirfarandi spurningum:
 
  1. Hvað er SPI? Hverjir eru helstu kostir og ókostir?
  1. Hvenær er betra að nota SPI fremur en Serial Ports (TX og RX)?
  1. Hver er helsti munurinn á SPI og I2C og hvenær myndir þú frekar nota SPI?

---

#### 3.9 Þráðlaus samskipti tveggja Arduino Uno með notkun nRF24L01. (2%)
  - Fylgdu tutorial: [How nRF24L01+ Wireless Module Works & Interface with Arduino](https://lastminuteengineers.com/nrf24l01-arduino-wireless-communication/) 
  - **Ath** tengdu nRF24L01 við 3.3V output. Ekki tengja í 5V, það mun skemma nRF24L01
  

---

#### 3.10 væntanlegt!

---

### Námsmat og skil

Gefið er heilt fyrir fullnægjandi lausn og svör, hálft ef ábótavant eða svör vanta.
Skilaðu á Innu vefslóð á **Github wiki** vefsíðu (**private**) sem inniheldur:

- Myndbönd af virkni úr verklegum tilraunum.
  - Passaðu að nafnið þitt og dagsetning komi fram (t.d. á miða) í öllum myndböndum.
- Kóði.
- Svör við spurningum


# Verkefni 3 - (20%) 

Einstaklingsverkefni<br>
Tími: 3 vikur

---

#### 3.1. Arduino og Raspberry Pi (1%)
  1. Hver er munurinn á Arduino Uno og Raspberry Pi, nefndu helstu atriði?
  ##  rasberry pi er tölva og getur runnað mörg forrit á meðan arduino er microcontroller og getur bara runnað eitt forrit í einu.
  ##  rasberry pi er mikið dýrara heldur en arduino
  ##  það er létt fyrir rasberry pi að tengjast við netið með ethernet,usb eða þráðlaust
  ##  rasberry pi er með 4 usb port til að tengjast við ýmis tæki en arduino er bara með eitt usb sem er fyrir að tengjast við tölvuna
  ##  það er mikið léttara að frya rasberry pi heldur en arduino og það er yfir allt bara öruggara
  
  2. Hvenær og afhverju getur það verið gagnlegt að tengja Arduino og Raspberry Pi saman?
  ## arduino er með lélegt user interface og lítið proccesing power en það er betra mep öðrum hlutum eins og skynjara og myndavélar þannig þú getur notað arduino til að tengjast við hardwear en notað svo rasberry pi til að processa og kannski nota web server til að live streama t.d
---

#### 3.2 Serial tenging með usb, Arduino til RPi (2%)
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

**Bjargir:**

- [Raspberry Pi Arduino Serial Communication – Everything You Need To Know](https://roboticsbackend.com/raspberry-pi-arduino-serial-communication/)
- [pySerial documentation](https://pythonhosted.org/pyserial/)
- [Python 3 Unicode and Byte Strings](https://blog.feabhas.com/2019/02/python-3-unicode-and-byte-strings/)

---

#### 3.3 Serial tenging með usb, RPi til Arduino (3%)
Fylgdu tutorial: [Connect Your Raspberry Pi and Arduino Uno!](https://www.instructables.com/id/Connect-Your-Raspberry-Pi-and-Arduino-Uno/)
  
  - Skrifaðu og keyrðu Arduino kóðann í Arduino IDE í Raspberry Pi.
  - **Ath** Notaðu `str.encode()` til að breyta Unicode streng í bytes til að kóði virki.

---

#### 3.4 Bluetooth tenging, RPi til snjallsíma (2%)
Fylgdu tutorial: [Connect Your Raspberry Pi and Smartphone via bluetooth !](https://bluedot.readthedocs.io/en/latest/gettingstarted.html)
Munið að fylgja leiðbeiningum vel, ekki gleyma neinu!!!
  
  - Verkefnið er að rasberryPI prentar út "Hello World" þegar þið smellið á Blue Dot í síma ykkar
  
---

#### 3.5 Bluetooth tenging, RPi til snjallsíma og LED (2%)
Fylgdu tutorial: [Connect Your Raspberry Pi and Smartphone via bluetooth !](https://bluedot.readthedocs.io/en/latest/gettingstarted.html)
  
  - Verkefnið er að rasberryPI kveikir á LED þegar smelt er á Blue Dot í snjallsíma :-) sem þýðir að þið verðið að tengja eina LED peru í breadboard
    og tengja við rasberryPi
  
---

#### 3.6 Bluetooth tenging, RPi til snjallsíma og Myndavél (2%)
Fylgdu tutorial: [Connect Your Raspberry Pi and Smartphone via bluetooth !](https://bluedot.readthedocs.io/en/latest/gettingstarted.html)
  
  - Verkefnið er að rasberryPI tekur mynd þegar smelt er á Blue Dot í snjallsíma :-) sem þýðir tenging við video :-)
  
---

### Fleiri verkefni væntanleg!

---

## Námsmat og skil

Gefið er heilt fyrir fullnægjandi lausn og svör, hálft ef ábótavant eða svör vanta.
Skilaðu á Innu vefslóð á **Github wiki** vefsíðu (private) sem inniheldur:

- Myndbönd af virkni úr verklegum tilraunum.
  - Passaðu að nafnið þitt og dagsetning komi fram (t.d. á miða) í öllum myndböndum.
- Kóði.
- Svör við spurningum


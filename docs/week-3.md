   >>## [Home](/README.md)
  >> [viikko-1](/docs/week-1.md) >> [viikko-2](/docs/week-2.md) >> [viikko-3](/docs/week-3.md) >> [viikko-4](/docs/week-4.md) >> [viikko-5](/docs/week-5.md)  >> [viikko-6](/docs/week-6.md) >> [viikko-7](/docs/week-7.md) >> [viikko-8](/docs/week-8.md) 
---

## Viikko 3- **Järjestelmätuen tavoitteet:** 
📅 24–30 April  

### 🔧 Tehtävät
* Asennan Windows Server 2022 \-palvelimen  
* Teen Active Directory \-domainin  

----




### **1 VMWARE-YMPÄRISTÖN JA VERKKOSOVITTIMIEN MÄÄRITYS**  

**Vaihe 1: Laitteiston määrittäminen VMware:ssa**

Ennen kuin käynnistät virtuaalikoneen, sinun täytyy lisätä toinen verkkosovitin (“kytkeä toinen kaapeli”).

* Sammuta Windows Server \-virtuaalikone.  
* Mene kohtaan **VM Settings** → **Add...** → **Network Adapter**.



Määritä verkkosovittimet seuraavasti:

* **NIC 1 (Internet):** Aseta tilaksi **NAT**. Tämä yhdistää palvelimen Ubuntu-isäntäkoneeseen (internet-yhteys).  
* **NIC 2 (Sisäinen verkko):** Aseta tilaksi **LAN Segment** (luo uusi nimeltä **"Northwind-Internal"**) tai vaihtoehtoisesti **Host-Only**. Tämä yhdistää vain asiakkaat (client-koneet) palvelimeen.

## 



**Vaihe 2: IP-osoitteiden määrittäminen Windowsissa**

Käynnistä palvelin. Näet nyt kaksi verkkosovitinta (**ncpa.cpl**\-ikkunassa). Nimeä ne uudelleen, jotta et mene sekaisin:

* Nimeä **“Ethernet0”** uudelleen **“WAN”**:  
  * Jätä tämä **DHCP-asetukselle**. Se saa internet-yhteyden VMwarelta.  
* Nimeä **“Ethernet1”** uudelleen **“Northwind-internal”**:  
  * Aseta tämä **staattiseksi (Static)**.



Asetukset:

* **IP-osoite:** 192.168.10.1 (valitse uusi aliverkko sisäistä labraa varten)  
* **Aliverkon peite (Subnet Mask):** 255.255.255.0  
* **Yhdyskäytävä (Gateway):** JÄTÄ TYHJÄKSI  
   *(Tietokoneella tulisi olla vain yksi oletusyhdyskäytävä, ja se kuuluu WAN-puolelle)*  
* **DNS:** 127.0.0.1


**![structure of the project](/images/other/Northwind-Page-3.drawio.png)**
**![structure of the project](/images/other/Network.drawio.png)**


##  **LEVYJEN OSIOINTI**
Käytetään Disk Management:iä ja määrittele tarvittavat osiot 

<img width="1217" height="712" alt="Screenshot from 2026-05-22 12-08-50" src="https://github.com/user-attachments/assets/ba2622f8-2f9e-47a0-a342-b3cdd1d8fc81" />


## 🎥 **1 Levyjen osiointi**
https://github.com/user-attachments/assets/5058fb62-6b59-48bc-8ad0-e818e60cc67c



## 🎥 ACTIVE DIRECTORYN ASENTAMINEN

## Demo Video




▶️ Katso video: 

https://github.com/user-attachments/assets/b173b5cd-8502-4628-9867-ff6878026ae6







## **2\. ACTIVE DIRECTORYN ASENTAMINEN** 
1\. Kirjaudu sisään Windows Serveriin.  
2\. Avaa Windows Server ja etsi “Server Manager.”
3\. Valitse asennustyypiksi “**Roolipohjainen tai ominaisuuspohjainen asennus**”  
4\. Valitse kohdepalvelin ja napsauta “**Next**”.


5\. Valitse palvelinrooleista “**Active Directory Domain Services**”, ja napsauta sitten “**Next**”.

6\. kohdassa näet valinnan “**Group Policy Management (Installed)**”. Valitse se ja asenna.

<img width="751" height="470" alt="image" src="https://github.com/user-attachments/assets/bac47b51-a485-4854-9bc8-ba3d5b063ece" />

Roolin asennuksen jälkeen Promota DC1 toimialueen ohjauskoneeksi.

<img width="565" height="266" alt="image" src="https://github.com/user-attachments/assets/0be1553e-7e65-4c8f-a6b8-c330745fedc4" />


Wizard käynnistyy seuraavaksi, lisätään uusi metsä Northwind.local
--

<img width="754" height="556" alt="Screenshot from 2026-05-21 15-52-10" src="https://github.com/user-attachments/assets/24ea8b9e-207e-47a4-8c62-69adb22079c8" />


Next > Määritä Restore Mode salasana, ********


<img width="742" height="369" alt="image" src="https://github.com/user-attachments/assets/ad8d8079-5cce-4012-9a66-abc6b5187fdc" />

Hyväksy esitietovaatimukset > Install > Asennus käynnistyy

<img width="376" height="276" alt="image" src="https://github.com/user-attachments/assets/f7b17678-b821-4423-a36a-0ad7c5bf9194" />


<img width="2560" height="1440" alt="Screenshot from 2026-04-27 12-28-14" src="https://github.com/user-attachments/assets/50f5d124-4060-423e-a969-389a18224303" />


Kirjaudu toimialueelle > Administrator tunnuksella


<img width="2560" height="1440" alt="Screenshot from 2026-05-21 16-02-11" src="https://github.com/user-attachments/assets/53037d54-04b5-4d24-9670-0a79ad1250a5" />




Näin ollen tällä tavalla luodaan Active Directory \-asennus.

### **2.1 ACTIVE DIRECTORY \-METSÄRAKENNE** 

1. **Puu (Tree)** – Hierarkkinen kokoelma toimialueita, joilla on yksi aloitusorganisaatioyksikkö (OU) ja joukko alidomaineja. Toimialueet ja alidomainit käyttävät yhteistä nimeämiskäytäntöä.  
2. **Metsä (Forest)** – Yhden tai useamman puun muodostama kokonaisuus, joka jakaa saman tietokannan, globaalin osoiteluettelon sekä suojausrajan.  
3. **Luottamussuhteet (Trust relationships)** – Puun toimialueilla on transitiviinen luottamussuhde, mikä tarkoittaa, että kun toimialue liittyy puuhun, se luottaa automaattisesti kaikkiin muihin saman puun toimialueisiin.  
4. **Suojausraja (Security boundary)** – Active Directoryn suojausraja on metsätasolla. Oletuksena yhden metsän käyttäjä tai järjestelmänvalvoja ei pääse toiseen metsään.  
5. **Eristäminen (Isolation)** – Metsiä voidaan käyttää Active Directory \-puiden eristämiseen tiettyjen tietojen mukaan.  
6. **Luottamus metsien välillä** – Kahden metsän välille voidaan luoda luottamussuhde, jotta ne voivat jakaa resursseja keskenään. Tätä kutsutaan metsien väliseksi luottamukseksi (**forest trust**).




<< [Home](/README.md)  
<< [week-1](/docs/week-1.md) 
<< [week-2](/docs/week-2.md) 
>>## >> [Week 4 – Palvelimen asennus](/docs/week-4.md)


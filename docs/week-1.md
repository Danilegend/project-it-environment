   >>## [Home](/README.md)
---
## Week 1 – Suunnittelu & alkuasetukset

### 🔧 Tehtävät
- Projektin suunnittelu
- Vaatimusten määrittely
- VMware asennus
- Windows Server ISO lataus


----
## **6.VMWARE WORKSTATIONIN ASENTAMINEN** {#6.vmware-workstationin-asentaminen}

Asensin VMware Workstation **\-**virtualisointiohjelman ja loin virtuaalikoneen Windows Serverille.

* Etsi VMware Workstation millä tahansa hakukoneella tai napsauta suoraan tätä linkkiä:  
   [Download and license VMware Desktop Hypervisor for personal use (Fusion Pro and Workstation Pro](https://knowledge.broadcom.com/external/article?articleNumber=368667))  
   (broadcom.com)  
* Rekisteröidy Broadcomin verkkosivustolle. Rekisteröitymisen jälkeen kirjaudu sisään Broadcom**\-**tunnuksillasi ja valitse VMware Workstation Pro.  
* Voit halutessasi valita kohdat User Experience Settings. Tämä ei ole pakollista, ja jos et tarvitse niitä, on suositeltavaa jättää valinnat tekemättä.

**![][image4]**

Kun kaikki on valmista, napsauta \> **Install**.  
Odota, että asennus valmistuu, ja napsauta lopuksi \> **Finish.**

|  |  |
| :---- | :---- |

Voit käynnistää sovelluksen **Windowsin työpöydällä olevasta pikakuvakkeesta**.   
 Nyt näemme VMware**\-**alustan.

## **7\. WINDOWS SERVER** \-**ISO**\-**TIEDOSTON LATAAMINEN** {#7.-windows-server--iso-tiedoston-lataaminen}

1\. Windows Server **\-**ISO**\-**tiedoston asentamista varten voit etsiä millä tahansa hakukoneella hakusanalla [Windows Server ISO version tai Windows Server 2022 | Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022) ja valita Windows Server 2022:n uusimman version.

|   |
| :---- |

2\. Lataus kestää jonkin aikaa. Kun lataus on valmis, avaa VMware Workstation **\-**sovellus ja luo virtuaalikone.

## **8\. UUDEN VIRTUAALIKONEEN (VM) LUOMINEN** {#8.-uuden-virtuaalikoneen-(vm)-luominen}

Virtuaalikone luotiin VMware Workstation \-ympäristöön, jotta IT-infrastruktuuria voidaan testata turvallisesti ilman vaikutusta fyysiseen laitteistoon. Virtualisointi mahdollistaa useiden erillisten järjestelmien ajamisen samassa ympäristössä, mikä on yleinen käytäntö IT-alalla.

**![][image5]**

**![][image6]**

VMware VM \> New \> Nimi ja käyttöjärjestelmä \> Muisti (RAM) \> Kiintolevy (VDI/VHD) \> Tallennustila (dynaaminen/kiinteä) \> Levyn koko \> Create

## **9\. WINDOWS SERVER SETUP** {#9.-windows-server-setup}

1\. **Valitse kieli ja alueasetukset**  
 Valitse asennuskieli, aika- ja valuuttaformaatti sekä näppäimistön asettelu ja jatka eteenpäin.

2\. **Valitse Windows Server \-versio**  
 Valitse sopiva versio, esimerkiksi *Windows Server 2022 Standard (Desktop Experience)*.

**![][image7]**

* **Hyväksy lisenssiehdot**  
   Lue ja hyväksy Microsoftin lisenssisopimus jatkaaksesi asennusta.  
* **Valitse asennustyyppi ja levy**  
   Valitse *Custom installation* ja määritä levytilaa käyttöjärjestelmän asennusta varten.  
* **Määritä järjestelmänvalvojan salasana**  
   Asennuksen lopuksi luo vahva salasana **Administrator\-**tilille ja kirjaudu järjestelmään.
- 
  ## **3\. PROJEKTIN TAVOITTEET** 

## **3.1 Järjestelmätuen tavoitteet:** 

* Asennan Windows Server 2022 \-palvelimen  
* Teen Active Directory \-domainin  
* Luon käyttäjät, ryhmät ja OU-rakenteen  
* Määritän GPO-käytännöt (esim. ruudunlukitus, USB-esto)  
* Teen varmuuskopion ja testaan palautuksen  
* Seuraan palvelimia (monitorointi)

## **3.2 Teknisen tukipalvelun tavoitteet:**   

* Asennan Windows 10/11 \-työaseman ja liitän domainin  
* Asennan tarvittavat sovellukset  
* Luon 4–6 fiktiivistä helpdesk-tukipyyntöä ja ratkaisen ne  
* Harjoittelen etäyhteyttä (RDP)  
* Dokumentoin kaikki tukipyynnöt

**3.3 Dokumentaation tavoitteet:**

* Kirjoitan projektisuunnitelman, asennusraportit ja tietoturvakuvauksen  
* Teen kuvakaappauksia jokaisesta työvaiheesta  
* Kirjoitan päiväkirjaa joka työpäivä



**5.PERUSTOIMINTO:** 

## **5.1 Active Directoryn käyttöönotto** 

* Tavoite:  
   Määrittää Active Directory **\-**toimialue alusta alkaen.  
* Vaiheet:  
* Asenna Windows Server virtuaalikoneeseen.  
* Ylennä palvelin toimialueen ohjaimeksi (Domain Controller, DC).  
* Luo Active Directory **\-**toimialue.  
* Luo organisaatioyksiköt (OU:t) eri osastoja varten.  
* Luo käyttäjätilit ja ryhmät näihin organisaatioyksiköihin.


## 📑 Sisällysluettelo

- #projektin-yleiskuvaus
- #tekninen-ympäristö
  
  >>## [Week 2 – Virtuaaliympäristö](/docs/week-2.md)
  

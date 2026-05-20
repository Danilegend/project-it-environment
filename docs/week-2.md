
   >>## [Home](/README.md)     - [week-1](/docs/week-1.md) 




## Week 2 – Virtual Environment
📅 18–24 April  

---

### Tasks
- Created Virtual Machine (VM)
- Configured:
  - RAM
  - Disk size
  - Network settings
----



## **3\. WINDOWS SERVER** \-**ISO**\-**TIEDOSTON LATAAMINEN** 
---

1\. Windows Server **\-**ISO**\-**tiedoston asentamista varten voit etsiä millä tahansa hakukoneella hakusanalla [Windows Server ISO version tai Windows Server 2022 | Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022) ja valita Windows Server 2022:n uusimman version.


**![installation VMWARE](/images/server/serla.drawio.png)**


2\. Lataus kestää jonkin aikaa. Kun lataus on valmis, avaa VMware Workstation **\-**sovellus ja luo virtuaalikone.



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


<< [week-1](/docs/week-1.md) 
>>## >> [Week 3 – Palvelimen asennus](/docs/week-3.md)

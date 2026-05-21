
 >>## [Home](/README.md)     - [week-1](/docs/week-1.md)  - [week-2](/docs/week-1.md)  - [week-3](/docs/week-3.md) 


## Week 3 **Järjestelmätuen tavoitteet:** 
📅 2–02 May

----



<img width="1007" height="733" alt="RAS_nat drawio" src="https://github.com/user-attachments/assets/f9e30361-e417-44dc-9614-b7339579e5cd" />



**Vaihe 3: “Routing”-palvelun asentaminen**

Windows ei automaattisesti jaa internet-yhteyttä NIC 1:stä NIC 2:een. Sinun täytyy määrittää se toimimaan reitittimenä.

1. Avaa **Server Manager** → **Add Roles and Features**.  
2. Valitse **Remote Access**.

**![][image18]**

3. **Role Services** \-sivulla rastita **Routing** (tämä valitsee automaattisesti myös **DirectAccess and VPN**).  
4. Viimeistele asennus ja käynnistä palvelin uudelleen, jos sinua pyydetään tekemään niin.

            Nyt palvelimesi pystyy toimimaan reitittimenä.

**![][image19]**

**Vaihe 4: NAT-asetusten määrittäminen (”Taikavaihe”)**

Nyt määritetään Windows jakamaan internet-yhteys WAN-liitännästä LAN-verkkoon.

1. Siirry kohtaan **Tools** → **Routing and Remote Access**.  
2. Napsauta palvelimen nimeä hiiren oikealla ja valitse **Configure and Enable Routing and Remote Access**.  
3. Valitse **Network Address Translation (NAT)**.  
4. **Tärkeää:** Valitse **WAN-liitäntä** (se, jossa on internet-yhteys) julkiseksi verkkoliitännäksi (*public interface*).  
5. Viimeistele ohjattu toiminto (**wizard**).

Nyt palvelin jakaa internet-yhteyden sisäverkkoon.




https://github.com/user-attachments/assets/7c2eb915-238d-4500-b3bc-5375709adb0d





## 

\- WAN (internet)  
\- LAN (sisäverkko)

Palvelin toimii reitittimenä käyttäen NAT**\-**asetuksia.  
Työasemat saavat IP**\-**osoitteet DHCP**\-**palvelun kautta.

## 
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



<< [Home](/README.md)  
<< [week-1](/docs/week-1.md) 
<< [week-2](/docs/week-2.md) 
<< [week-3](/docs/week-3.md) 

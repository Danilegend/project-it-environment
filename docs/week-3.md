 >>## [Home](/README.md)     - [week-1](/docs/week-1.md)  - [week-2](/docs/week-1.md) 


## Week 3 **Järjestelmätuen tavoitteet:** 
📅 24–30 April  

----
* Asennan Windows Server 2022 \-palvelimen  
* Teen Active Directory \-domainin  
* Luon käyttäjät, ryhmät ja OU-rakenteen  
* Määritän GPO-käytännöt (esim. ruudunlukitus, USB-esto)  
* Teen varmuuskopion ja testaan palautuksen  
* Seuraan palvelimia (monitorointi)

**![structure of the project](/images/other/Northwind-Page-3.drawio.png)**
**![structure of the project](/images/other/Network.drawio.png)**









## 🎥 Video

▶️ Katso video:
/images/videos/Delicious sushi awaits.mp4





















## **10\. ACTIVE DIRECTORYN ASENTAMINEN** {#10.-active-directoryn-asentaminen}

1\. Kirjaudu sisään Windows Serveriin.  
2\. Avaa Windows Server ja etsi “Server Manager.”

**![][image8]**

3\. Valitse asennustyypiksi “**Roolipohjainen tai ominaisuuspohjainen asennus**”  
4\. Valitse kohdepalvelin ja napsauta “**Next**”.

**![][image9]**

5\. Valitse palvelinrooleista “**Active Directory Domain Services**”, ja napsauta sitten “**Next**”.

**![][image10]**  
6\. kohdassa näet valinnan “**Group Policy Management (Installed)**”. Valitse se ja asenna.

**![][image11]**

Näin ollen tällä tavalla luodaan Active Directory \-asennus.

### **10.1 ACTIVE DIRECTORY \-METSÄRAKENNE** {#10.1-active-directory--metsärakenne}

1. **Puu (Tree)** – Hierarkkinen kokoelma toimialueita, joilla on yksi aloitusorganisaatioyksikkö (OU) ja joukko alidomaineja. Toimialueet ja alidomainit käyttävät yhteistä nimeämiskäytäntöä.  
2. **Metsä (Forest)** – Yhden tai useamman puun muodostama kokonaisuus, joka jakaa saman tietokannan, globaalin osoiteluettelon sekä suojausrajan.  
3. **Luottamussuhteet (Trust relationships)** – Puun toimialueilla on transitiviinen luottamussuhde, mikä tarkoittaa, että kun toimialue liittyy puuhun, se luottaa automaattisesti kaikkiin muihin saman puun toimialueisiin.  
4. **Suojausraja (Security boundary)** – Active Directoryn suojausraja on metsätasolla. Oletuksena yhden metsän käyttäjä tai järjestelmänvalvoja ei pääse toiseen metsään.  
5. **Eristäminen (Isolation)** – Metsiä voidaan käyttää Active Directory \-puiden eristämiseen tiettyjen tietojen mukaan.  
6. **Luottamus metsien välillä** – Kahden metsän välille voidaan luoda luottamussuhde, jotta ne voivat jakaa resursseja keskenään. Tätä kutsutaan metsien väliseksi luottamukseksi (**forest trust**).

**![][image12]**

### **10.2 VMWARE-YMPÄRISTÖN JA VERKKOSOVITTIMIEN MÄÄRITYS**  {#10.2-vmware-ympäristön-ja-verkkosovittimien-määritys}

**![][image13]**

**Vaihe 1: Laitteiston määrittäminen VMware:ssa**

Ennen kuin käynnistät virtuaalikoneen, sinun täytyy lisätä toinen verkkosovitin (“kytkeä toinen kaapeli”).

* Sammuta Windows Server \-virtuaalikone.  
* Mene kohtaan **VM Settings** → **Add...** → **Network Adapter**.

**![][image14]**

Määritä verkkosovittimet seuraavasti:

* **NIC 1 (Internet):** Aseta tilaksi **NAT**. Tämä yhdistää palvelimen Ubuntu-isäntäkoneeseen (internet-yhteys).  
* **NIC 2 (Sisäinen verkko):** Aseta tilaksi **LAN Segment** (luo uusi nimeltä **"Northwind-Internal"**) tai vaihtoehtoisesti **Host-Only**. Tämä yhdistää vain asiakkaat (client-koneet) palvelimeen.

## 

**![][image15]**

**Vaihe 2: IP-osoitteiden määrittäminen Windowsissa**

Käynnistä palvelin. Näet nyt kaksi verkkosovitinta (**ncpa.cpl**\-ikkunassa). Nimeä ne uudelleen, jotta et mene sekaisin:

* Nimeä **“Ethernet0”** uudelleen **“WAN”**:  
  * Jätä tämä **DHCP-asetukselle**. Se saa internet-yhteyden VMwarelta.  
* Nimeä **“Ethernet1”** uudelleen **“Northwind-internal”**:  
  * Aseta tämä **staattiseksi (Static)**.

**![][image16]**

Asetukset:

* **IP-osoite:** 192.168.10.1 (valitse uusi aliverkko sisäistä labraa varten)  
* **Aliverkon peite (Subnet Mask):** 255.255.255.0  
* **Yhdyskäytävä (Gateway):** JÄTÄ TYHJÄKSI  
   *(Tietokoneella tulisi olla vain yksi oletusyhdyskäytävä, ja se kuuluu WAN-puolelle)*  
* **DNS:** 127.0.0.1

**![][image17]**

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

**![][image20]**

**![][image21]**

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
>>## >> [Week 4 – Palvelimen asennus](/docs/week-4.md)


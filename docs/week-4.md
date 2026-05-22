
   >>## [Home](/README.md)
  >> [viikko-1](/docs/week-1.md) >> [viikko-2](/docs/week-2.md) >> [viikko-3](/docs/week-3.md) >> [viikko-4](/docs/week-4.md) >> [viikko-5](/docs/week-5.md)  >> [viikko-6](/docs/week-6.md) >> [viikko-7](/docs/week-7.md) >> [viikko-8](/docs/week-8.md) 
---

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

<img width="1031" height="1643" alt="DHCP drawio" src="https://github.com/user-attachments/assets/9f23e3ed-6e88-41be-ae9e-3a288fb6e570" />



<< [Home](/README.md)  
<< [week-1](/docs/week-1.md) 
<< [week-2](/docs/week-2.md) 
<< [week-3](/docs/week-3.md) 

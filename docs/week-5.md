
 >>## [Home](/README.md)
>> [viikko-1](/docs/week-1.md) >> [viikko-2](/docs/week-2.md) >> [viikko-3](/docs/week-3.md) >> [viikko-4](/docs/week-4.md) >> [viikko-5](/docs/week-5.md)  >> [viikko-6](/docs/week-6.md) >> [viikko-7](/docs/week-7.md) >> [viikko-8](/docs/week-8.md) 
---

## Week 5 – Käyttäjät & ryhmät** 
📅 2–02 May
----

### 🔧 Tehtävät

  - Käyttäjät & ryhmät
  - Kotikansion luominen
  - Helpdesk‑tehtävät
  - Toisen palvelimen liittäminen 

---

<img width="1031" height="481" alt="Rhymäat drawio" src="https://github.com/user-attachments/assets/48755b2e-4e10-4e7c-9ff6-f780dac96be1" />

<img width="1039" height="2311" alt="AD_rhymät drawio" src="https://github.com/user-attachments/assets/20afd78c-0232-453d-ad10-dd59c2e7eae6" />


## 🎥 **1 Kotikansion luominen**
---



https://github.com/user-attachments/assets/beeb05d1-9128-4238-b270-82614148d86e

## 🎥 **2 Kotikansion luominen**
---

https://github.com/user-attachments/assets/d50d9a82-9153-4b43-80aa-8307b6c5982b

## **Helpdesk‑tehtävät**
---
<img width="3780" height="4444" alt="image" src="https://github.com/user-attachments/assets/3a78652a-1f8e-47e7-a021-7c93265040e9" />


##  **2 Toisen palvelimen liittäminen**
---

Toisen palvelimen liittäminen Toimialueeseen (DAN01 – tiedostopalvelin)
**Administrator ja Password**

<img width="768" height="648" alt="Screenshot from 2026-05-22 17-59-48" src="https://github.com/user-attachments/assets/d1d447d5-2e5f-4d01-ab43-3867cf391b5f" />

<img width="2560" height="1440" alt="Screenshot from 2026-05-22 19-34-52" src="https://github.com/user-attachments/assets/4a65009f-8746-453a-85fe-bb8d038be538" />


## **3-Delegation**
----

<img width="883" height="1465" alt="Deligation drawio" src="https://github.com/user-attachments/assets/322329c7-8ce8-4b3b-9fc4-38d387768a68" />


<img width="4348" height="768" alt="image" src="https://github.com/user-attachments/assets/6d6b9a53-0274-4d9f-ae5a-ab2fddcc39b5" />

https://github.com/user-attachments/assets/a712a340-bdf9-444c-ab1e-c0bf06f25dab


Käyttäjät ja ryhmät

Käyttäjätilien luonti Ryhmät Salasanapolitiikka 

:::
:::
------

Projektin vaiheet
Viikko 1 – Suunnittelu

Projektisuunnitelma
Asiakasvaatimukset
Ympäristön valmistelu
Virtualisointiympäristön asennus

Tuotokset:
Projektisuunnitelma, vaatimusmäärittely, video 1.

Viikko 2 – Palvelin ja verkko

Windows Server ‑asennus
AD‑domainin luonti
IP‑osoitteet

Tuotokset:
Palvelinasennuksen dokumentti, videota 2–3.

Viikko 3 – Käyttäjät ja ryhmät

Käyttäjätilien luonti
Ryhmät
Salasanapolitiikka
Perus‑GPO‑asetukset

Tuotokset:
Käyttäjälista, GPO‑dokumentti, video 4.

Viikko 4 – Työasemat

Windows 10/11 asennus
Työaseman liittäminen domainiin
Sovellusten asennus
Vakioitu työasema

Tuotokset:
Työaseman kuvaus, video 5–6.

Viikko 5 – Tietoturva ja varmuuskopio

Antivirus
Palomuuri
Varmuuskopion tekeminen
Varmuuskopion palautus

Tuotokset:
Tietoturvadokumentti, varmuuskopiointi, video 7.

Viikko 6 – Helpdesk‑tehtävät
Teen 4–6 tyypillistä tukipyyntöä:

En pääse kirjautumaan
Tulostin ei toimi
Ei internet‑yhteyttä
Outlook ei käynnisty

Teen dokumentit ja videot ratkaisusta.
Tuotokset:
Tukipyyntöjen dokumentit, video 8.

Viikko 7 – Dokumentointi ja valmistelu

Kaikkien dokumenttien viimeistely
"Tutkintoexcel" täyttö
PowerPoint esitys (suomeksi)
Harjoittelu


Viikko 8 – Näyttö

Projektin esittely
Videoiden ja ympäristön näyttö
Kysymyksiin vastaaminen


------


* Luon käyttäjät, ryhmät ja OU-rakenteen  
* Määritän GPO-käytännöt (esim. ruudunlukitus, USB-esto)  
* Teen varmuuskopion ja testaan palautuksen  
* Seuraan palvelimia (monitorointi)

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
<< [week-4](/docs/week-4.md) 
>>## >> [Week 6 – Palvelimen asennus](/docs/week-6.md)


# project-it-environment
IT infrastructure project using Windows Server and Active Directory
![General Look of the project ](images/other/Gemini_Generated_Image_1b6s5j1b6s5j1b6s.png)


## **1 JOHDANTO**

Tämän projektin tavoitteena on suunnitella ja toteuttaa Northwind Tech Oy:n IT-ympäristö. Projekti keskittyy erityisesti toimialueympäristön (Active Directory) käyttöönottoon sekä palvelin- ja työasemaympäristön kehittämiseen.

Northwind Tech Oy on kuvitteellinen yritys, jota käytetään tässä projektissa esimerkkinä. Yrityksessä työskentelee noin 35 henkilöä eri osastoilla, kuten IT, myynti, talous ja asiakaspalvelu.

Projektin aikana toteutetaan palvelimen asennus, toimialueen luonti, käyttäjien ja ryhmien hallinta sekä perusasetusten määrittely. Lisäksi huomioidaan järjestelmän ylläpito ja tietoturva.

**![structure of the project](images/other/NorthWind_02.drawio.png)**


## **2 PROJEKTISUUNNITELMA**  

Pienen yrityksen IT-ympäristön rakentaminen ja helpdesk-tuki  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

| Opiskelija | Heyiredin Daniel Sema |
| :---- | :---- |
| **Koulutus** | Tieto- ja viestintätekniikan perustutkinto |
| **Osatutkinnot** | Teknisessä tukipalvelussa toimiminen (TTT) · Järjestelmätuessa toimiminen (JT) |
| **Ajankohta** | 7.4.2026 – 5.6.2026 |
| **Oppilaitos** | Taitotalo, Helsinki |
| **Ohjaaja / Arvioija** | Kari Vikman · [kari.vikman@taitotalo.fi](mailto:kari.vikman@taitotalo.fi) |
| **Tavoitearvosana** | Hyvä 4 |
| **Versio** | 2.0 · Laadittu 7.4.2026 |

## **2.1 Projektin tarkoitus** 

Tämä projekti on näyttö Taitotalon IT-koulutuksessa. Rakennan pienen yrityksen IT-ympäristön virtuaalikoneilla. Harjoittelen IT-tuen ja järjestelmätuen työtehtäviä.

Projektin avulla osoitan osaamiseni järjestelmätuen ja IT**\-**tuen työtehtävissä

## **2.2 Fiktiivinen asiakas** 

| Yrityksen nimi | Northwind Tech Oy |
| :---- | :---- |
| **Henkilöstö** | 50 käyttäjää |
| **Toimiala** | Konsultointi |
| **IT-ympäristö** | Paikallinen palvelin \+ Windows-työasemat |
| **Asiakastarve** | Domain, käyttäjät, GPO, vakioitu työasema, perus-helpdesk-tuki |

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

## **4\. TEKNINEN YMPÄRISTÖ**

| Virtualisointiympäristö | VMware |
| :---- | :---- |
| **Palvelin** | Windows Server 2022 (virtuaalikone) |
| **Työasema** | Windows 10 / 11 (virtuaalikone) |
| **Hakemistopalvelu** | Active Directory Domain Services (AD DS) |
| **Pilvipalvelu (valinnainen)** | Microsoft 365 Developer Tenant |
| **Komentorivi** | PowerShell |
| **Tiedostojen tallennus** | OneDrive (varmuuskopiot \+ dokumentit) |
| **Kommunikaatio** | Microsoft Teams |
| **Projektinhallinta** | ProjectLibre |

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

### 📅 Viikkokohtainen työ
- #week-1--suunnittelu--alkuasetukset
- #week-2--virtuaaliympäristö
- #week-3--palvelimen-asennus
- #week-4--active-directory
- #week-5--käyttäjät--ryhmät
- #week-6--gpo--määritykset
- #week-7--testaus--dokumentaatio

---

# 📅 VIikkokohtainen työ

---

## ✅ Week 1 – Suunnittelu & alkuasetukset

### 🔧 Tehtävät
- Projektin suunnittelu
- Vaatimusten määrittely
- VMware asennus
- Windows Server ISO lataus






























































# 🖥️ IT Environment Project – Northwind Tech Oy

## 📌 Project Overview
This project demonstrates the design and implementation of a small company IT infrastructure.  
The main goal is to build a domain-based network using **Windows Server 2022** and **Active Directory** in a virtual environment.

The project is part of my IT studies and shows my skills in:
- System administration
- Technical support
- Virtualization
- Documentation

---

## 🧰 Environment

### 🔧 Tools & Technologies
- VMware Workstation
- Windows Server 2022
- Windows 10 / Windows 11
- Active Directory Domain Services (AD DS)
- PowerShell

### 🏢 Company (Fictional)
- Name: Northwind Tech Oy  
- Users: ~35–50 employees  
- Departments:
  - IT
  - Sales
  - Finance
  - Customer Support  

---

## 📅 Project Timeline
**Start:** 11 April 2026  
**End:** 30 May 2026  

---

## 📑 Table of Contents
- [Project Overview](#project-overview)
- [Environment](#environment)

### 📅 Weekly Work Plan
- [Week 1 – Planning & Setup](#week-1--planning--setup)
- [Week 2 – Virtual Environment](#week-2--virtual-environment)
- [Week 3 – Server Installation](#week-3--server-installation)
- [Week 4 – Active Directory](#week-4--active-directory)
- [Week 5 – Users & Groups](#week-5--users--groups)
- [Week 6 – GPO & Configuration](#week-6--gpo--configuration)
- [Week 7 – Testing & Documentation](#week-7--testing--documentation)

---

# 📅 Weekly Work Plan

---

## ✅ Week 1 – Planning & Setup
📅 11–17 April  

### Tasks
- Defined project goals
- Analyzed company requirements
- Installed VMware Workstation
- Downloaded Windows Server ISO  

### Result
A working virtual lab environment prepared for server setup.

---

## ✅ Week 2 – Virtual Environment
📅 18–24 April  

### Tasks
- Created Virtual Machine (VM)
- Configured:
  - RAM
  - Disk size
  - Network settings

### Result
A fully configured virtual machine ready for OS installation.

---

## ✅ Week 3 – Server Installation
📅 25 April – 1 May  

### Tasks
- Installed Windows Server 2022
- Configured system settings
- Created Administrator account  

### Result
A functioning Windows Server system.

---

## ✅ Week 4 – Active Directory
📅 2–8 May  

### Tasks
- Installed Active Directory
- Created domain (e.g., **northwind.local**)
- Configured domain controller  

### Result
Domain environment created for centralized management.

---

## ✅ Week 5 – Users & Groups
📅 9–15 May  

### Tasks
- Created Organizational Units (OU)
- Added:
  - Users
  - Groups
- Automated user creation with PowerShell
- Configured home folders  

### Result
Organized and scalable Active Directory structure.

---

## ✅ Week 6 – GPO & Configuration
📅 16–22 May  

### Tasks
- Configured Group Policies:
  - Password policy
  - USB restrictions
  - Desktop wallpaper
- Joined workstation to domain  

### Result
Centralized system control and security policies implemented.

---

## ✅ Week 7 – Testing & Documentation
📅 23–30 May  

### Tasks
- Tested system functionality
- Simulated helpdesk tasks
- Tested backup & recovery
- Final documentation created  

### Result
Fully tested IT environment with documentation.

---

# 🖼️ Screenshots

_(Add your images here)_

Example:
```md
![VM Setup](images/vmware/setup.png)

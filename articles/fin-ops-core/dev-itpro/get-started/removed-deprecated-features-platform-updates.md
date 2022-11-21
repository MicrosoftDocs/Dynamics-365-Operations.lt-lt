---
title: Pašalintos arba nebenaudojamos platformos funkcijos
description: Šiame straipsnyje aprašomos priemonės, kurios buvo pašalintos arba suplanuotos pašalinti į finansų ir operacijų programėlių platformos atnaujinimus.
author: sericks007
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7d74efe7aa4f3a30c116253d647b9d7bec3b508d
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785105"
---
# <a name="removed-or-deprecated-platform-features"></a>Pašalintos arba nebenaudojamos platformos funkcijos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos priemonės, kurios buvo pašalintos arba suplanuotos pašalinti į finansų ir operacijų programėlių platformos atnaujinimus.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą. 

Išsami informacija apie finansų ir operacijų programėlių objektus pateikta techninės [nuorodos ataskaitose](/dynamics/s-e/global/axtechrefrep_61). Galite palyginti skirtingas šių ataskaitų versijas ir sužinoti apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje finansų ir operacijų programėlių versijoje.

## <a name="feature-deprecation-effective-august-2022"></a>Pranešimas apie funkcijos nerekomendavimą, įsigaliojantį nuo 2022 m. rugpjūtis

### <a name="lifecycle-services-lcs-features-deprecated-in-august-2022"></a>Ciklo tarnybų (LCS) funkcijos pasenusios 2022 m. rugpjūčio mėn.

Kaip " [One Dynamics" vienos platformos darbo](/dynamics365-release-plan/2022wave2/finance-operations/finance-operations-crossapp-capabilities/one-dynamics-one-platform) pastangų dalis pasenusios šios LCS funkcijos.

| Funkcijos pavadinimas | Naudojama su AX 2012? | Naudojama su finansų ir operacijų programėle? | Pakeitė kita funkcija? |
|--------------|--------------------|----------------------------------------|------------------------------|
| Pranešimai | Taip | Taip | Taip: užduotų atskirų projektų ir aplinkos puslapių pranešimai. |
| Konfigūracijos tvarkyklė | Taip | Ne | Ne |
| Gedimo ir iškelties analizė | Taip | Ne | Ne |
| Grįžtamasis ryšys ir klaidos | Taip | Taip | Ne |
| Mano abonementas | Taip | Taip | Ne |
| „Office 365“ | Taip | Taip | Taip: arba Azure Active Directory "Microsoft" administratorius portalas. |
| Poveikio analizė | Ne | Taip | Ne |
| Viso ekonominės įtakos vertinimas | Ne | Taip | Ne |
| Aptarnavimo užklausos | Ne | Taip | Taip: [savitarnos diegimas](../deployment/infrastructure-stack.md) |
| „SharePoint“ integravimas | Taip | Taip | Ne |
| Konfigūracijos ir duomenų tvarkytuvas | Ne | Taip | Ne |
| Proceso duomenų paketai | Ne | Taip | Taip: duomenų [importavimo / eksportavimo sistema (DIXF)](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job) |
| Išvardiimo atnaujinimas | Ne | Taip | Taip: [yra vienas versijos](../lifecycle-services/oneversion-overview.md) tarnybos naujinimas. |
| Infrastruktūros įvertinatorius | Taip | Ne | Ne |
| Licencijos dydis | Taip | Ne | Ne |
| Naudojimo analizės įrankis | Taip | Ne | Ne |
| Pritaikymo analizė | Taip | Ne | Ne |
| Sistemos diagnostika | Taip | Taip | Ne |
| Verslo procesų modeliavimo programos Visio valdymas | Taip | Taip | Ne |
| AX 2012 debesies aplinkos valdymas | Taip | Ne | Ne |
| RDFE "Azure" jungtis | Taip | Taip | Ne |
| AX 2012 versijos | Taip | Ne | Ne |
| Darbo elementai, saugomi LCS saugykloje | Taip | Taip | Ne |
| Karštųjų pataisų užklausos | Taip | Taip | Ne |


### <a name="transport-layer-security-tls-rsa-cipher-suites"></a>Transportavimo sluoksnio saugos (TSA) RSA šifravimas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Mes šaliname šį šifrų sąrašą, kad atitiktų mūsų dabartinius saugos protokolus.<br><br>TLS_RSA_WITH_AES_256_GCM_SHA384<br>TLS_RSA_WITH_AES_128_GCM_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA256<br>TLS_RSA_WITH_AES_128_CBC_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA<br>TLS_RSA_WITH_AES_256_CBC_SHA  |
| **Pakeitė kita funkcija?**   | Nuo 2023 m. sausio 31 d. klientai gali naudoti tik standartinius [mūsų standartinius poreikius](/power-platform/admin/server-cipher-tls-requirements). Šis pakeitimas veikia jūsų klientus ir serverius, kurie palaiko ryšį su mūsų serveriais, pvz., tai gali paveikti jūsų trečiųjų šalių integravimą, kuris neatitinka mūsų standartinių programos objektų. |
| **Paveiktos produkto sritys**         | „Finance and operations” programos |
| **Visuotinio diegimo parinktis**              | Debesies diegimas |
| **Būsena**                         | Nerekomenduojama. Klientai turi atnaujinti savo serverius iki 2023 m. sausio 31 d. Daugiau informacijos apie TS Cipher Suite užsakymo konfigūravimą ieškokite Transporto sluoksnio [saugos (NLS) valdymas](/windows-server/security/tls/manage-tls).  |


## <a name="feature-deprecation-effective-june-2022"></a>Funkcija, kuri galioja 2022 m. birželio mėn.

### <a name="finance-and-operations-dynamics-365-mobile-application-and-mobile-platform"></a>Finansų ir operacijų ("Dynamics 365") mobilioji programa ir mobilioji platforma 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Mes atšaukiame finansų ir operacijų ("Dynamics 365") mobiliąją programą ir platformą, kuri konsoliduoja vieną mobiliąją platformą, t. y Power Apps. |
| **Pakeitė kita funkcija?**   | Taip, su finansų ir operacijų programos duomenimis susijusią mobiliąją patirtį galima sukurti integruojant Power Platform. Norėdami gauti daugiau [informacijos, peržiūrėkite](https://cloudblogs.microsoft.com/dynamics365/it/2022/06/03/finance-and-operations-dynamics-365-mobile-app-to-be-deprecated/) žurnalo [skelbimo pranešimą ir](../power-platform/build-mobile-experiences.md) mobiliųjų patirties kūrimą. |
| **Paveiktos produkto sritys**         | „Finance and operations” programos |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Nerekomenduojama. Palaikymo data skirta 2024 m. spalio mėn. |


## <a name="platform-updates-for-version-10029-of-finance-and-operations-apps"></a>Finansų ir operacijų programėlių 10.0.29 versijos platformos naujinimai

### <a name="panorama-tab-style"></a>Skirtukų tamsos stilius

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Horizontaliai paslinkt puslapius sulygiuoti su datuotais maketo modeliais, kurie turi žinomas naudojimo ir pasiekiamumo problemas.  |
| **Pakeitė kita funkcija?**   | Ne, bet kiti skirtuko stiliai vis dar galimi. |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Nerekomenduojama. |


## <a name="feature-deprecation-effective-april-2022"></a>Funkcijos pasenusios 2022 m. balandžio mėn.

### <a name="xml-url-resolution-in-data-management"></a>XML URL sprendimas duomenų valdymo srityje 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Mes šaliname XML URL sprendimo palaikymą, nes tai identifikuojama kaip galima saugumo spraga. Tai reiškia, kad su XML failais susiję išoriniai ištekliai nebebus išspręsti.  |
| **Pakeitė kita funkcija?**   | Ne. |
| **Paveiktos produkto sritys**         | „Finance and operations” programos |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Nerekomenduojama. |

## <a name="feature-deprecation-effective-march-14-2022"></a>Priemonės pasenusios 2022 m. kovo 14 d.

### <a name="xslt-scripting-in-data-management"></a>XSLT scenarijus duomenų valdymo metu

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | XSLT scenarijaus palaikymas duomenų valdymo srityje pasenusias siekiant pagerinti finansų ir operacijų programėlių saugą ir duomenų apsaugą.  |
| **Pakeitė kita funkcija?**   | Ne. Klientai ir ISV turėtų apsvarstyti galimybę iš naujo įgyvendinti savo sprendimus, pagrįstus X++ kalba, vietoje XSLT scenarijaus. |
| **Paveiktos produkto sritys**         | „Finance and operations” programos |
| **Visuotinio diegimo parinktis**              | Viskas |
| **Būsena**                         | Pasenę <br><br>**Išimtis:** klientai, šiuo metu naudojantys XLST scenarijų. Juos galima toliau naudoti, kol bus atnaujinta į 10.0.30 arba vėlesnę versiją. Ankstesnėms versijoms išimtis galios 2023 m. sausio 31 d. Klientų, kurie gauna pranešimą pranešimų centre, kuris yra administravimo centre, gauta ši Microsoft 365 išimtis. |

## <a name="feature-removal-effective-october-2021"></a>Priemonės pašalinimas įsigalioja 2021 m. spalio mėn.

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>„Microsoft Azure“ SQL ataskaitos „Lifecycle Services“ (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Visas veiklas ir stebėjimą atliks platforma per automatizavimą. Tam nereikės jokių neautomatinių veiksmų.|
| **Pakeitė kita funkcija?**   | Taip, dabar yra automatizuota sistema, kuri šių pajėgumų nebenaudojama. |
| **Paveiktos produkto sritys**         | SQL ataskaitos: dabartinis DTU, dabartinio DTU informacija, Gauti užrakto informaciją, dabartinio plano sąrašo vadovas, Gauti užklausos ID sąrašą, Gauti duoto plano ID SQL užklausos planą, Gauti užklausų planus ir vykdymo būseną, Gauti throttle config, Gauti laukimo statistiką, išvardyti tinkamiausias užklausas |
| **Visuotinio diegimo parinktis**              | Debesies diegimas: Paveikia „Microsoft” valdomas gamybos ir 2‑5 pakopų smėlio dėžės aplinkas. |
| **Būsena**                         | Pašalinta |

### <a name="azure-sql-actions-in-lcs"></a>„Azure SQL" veiksmai LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Mes atšaukiame kai kurias SQL veiksmai LCS. Visas veiklas ir stebėjimą atliks platforma per automatizavimą. Tam nereikės jokių neautomatinių veiksmų. |
| **Pakeitė kita funkcija?**   | Taip, dabar yra automatizuota sistema, kuri šių pajėgumų nebenaudojama. |
| **Paveiktos produkto sritys**         | SQL veiksmai: sukurkite plano vadovą, kad planumėte ID, sukurkite plano vadovą, kaip įtraukti lentelės užuominas, pašalinti plano vadovą, išjungti / įgalinti puslapio užrakinimą ir užraktų perskyrimą, atnaujinti statistiką lentelėje, perkurti indeksą, kurti indeksą |
| **Visuotinio diegimo parinktis**              | Debesies diegimas: Paveikia „Microsoft” valdomas gamybos ir 2‑5 pakopų smėlio dėžės aplinkas. |
| **Būsena**                         | Pašalinta |


## <a name="feature-deprecation-effective-october-2021"></a>Funkcijos nuvertinimas įsigalioja 2021 m. spalio mėn.

### <a name="show-related-document-attachments-feature"></a>Funkcija "Rodyti susijusius dokumentų priedus"

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Priemonė grąžino netikėtus rezultatus. |
| **Pakeitė kita funkcija?**   | Ne. Visi tolesni planai, susiję su šia funkcija, bus perduoti per mūsų standartinį bangos atskleidimo procesą. |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas – dokumentų priedų naudojimas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Pasenę  |

## <a name="platform-updates-for-version-10023-of-finance-and-operations-apps"></a>Finansų ir operacijų programėlių 10.0.23 versijos platformos naujinimai

### <a name="ondbsynchronize-event"></a>OnDBSynchronize įvykis

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Nėra valdiklių šiam įvykiui įvykdyti. |
| **Pakeitė kita funkcija?**   | Taip, perkelkite esamus metodus, į kuriuos prenumeruoti **OnDBSynchronize įvykis**, į SysSetup išplėstinę klasę. |
| **Paveiktos produkto sritys**         | Duomenų bazės sinchronizavimas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama. Suplanuota pašalinimo data yra 2022 m. spalio mėn. |


### <a name="systemnotificationsmanageraddnotification-api"></a>SystemNotificationsManager.AddNotification API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Įtraukiant pranešimus Microsoft reikia papildomų parametrų. |
| **Pakeitė kita funkcija?**   | Taip, **SystemNotificationsManager.AddSystemNotification()** API. Šiai API reikia, kad būtų konkrečiai nustatytas sugeneruotų pranešimų ExpirationDateTime ir RuleID. |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama. Suplanuota pašalinimo data yra 2023 m. balandžio mėn. |

## <a name="platform-updates-for-version-10021-of-finance-and-operations-apps"></a>Finansų ir operacijų programėlių 10.0.21 versijos platformos naujinimai

### <a name="skype-for-business-online-support"></a>Verslo klientų aptarnavimo internete palaikymas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Verslo tinklo įmonės atmestas. Norėdami gauti daugiau informacijos, [„The Skype for Business Online“ paslaugos nebegalioja](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/the-skype-for-business-online-service-has-retired/ba-p/2596601). |
| **Pakeitė kita funkcija?**   | Šiuo metu ne, nors galime įtraukti buvimą iš komandų į ateitį.|
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama. **Skype įjungtas** nustatymai buvo išjungti išleidžiant 10.0.21. Šis parametras skirtas 2022 m. balandžio mėn. Tačiau, atlikus šį darbą, prieš išeius iš darbo komandai, „Skype“ nustos veikti. |
 
## <a name="feature-deprecation-effective-august-2021"></a>Pranešimas apie funkcijos nerekomendavimą, įsigaliojantį nuo 2021 m. rugpjūtis

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>„Microsoft Azure“ SQL ataskaitos „Lifecycle Services“ (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | Visas veiklas ir stebėjimą atliks platforma per automatizavimą. Tam nereikės jokių neautomatinių veiksmų.|
| **Pakeitė kita funkcija?**   | Taip, dabar yra automatizuota sistema, kuri šių pajėgumų nebenaudojama. |
| **Paveiktos produkto sritys**         | SQL ataskaitos: dabartinis DTU, dabartinio DTU informacija, Gauti užrakto informaciją, dabartinio plano sąrašo vadovas, Gauti užklausos ID sąrašą, Gauti duoto plano ID SQL užklausos planą, Gauti užklausų planus ir vykdymo būseną, Gauti throttle config, Gauti laukimo statistiką, išvardyti tinkamiausias užklausas |
| **Visuotinio diegimo parinktis**              | Debesies diegimas: Paveikia „Microsoft” valdomas gamybos ir 2‑5 pakopų smėlio dėžės aplinkas. |
| **Būsena**                         | Nerekomenduojama: Suplanuota pašalinimo data yra 2021 m. spalio mėn. |

### <a name="azure-sql-actions-in-lcs"></a>„Azure SQL" veiksmai LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Mes atšaukiame kai kurias SQL veiksmai LCS. Visas veiklas ir stebėjimą atliks platforma per automatizavimą. Tam nereikės jokių neautomatinių veiksmų. |
| **Pakeitė kita funkcija?**   | Taip, dabar yra automatizuota sistema, kuri šių pajėgumų nebenaudojama. |
| **Paveiktos produkto sritys**         | SQL veiksmai: sukurkite plano vadovą, kad planumėte ID, sukurkite plano vadovą, kaip įtraukti lentelės užuominas, pašalinti plano vadovą, išjungti / įgalinti puslapio užrakinimą ir užraktų perskyrimą, atnaujinti statistiką lentelėje, perkurti indeksą, kurti indeksą |
| **Visuotinio diegimo parinktis**              | Debesies diegimas: Paveikia „Microsoft” valdomas gamybos ir 2‑5 pakopų smėlio dėžės aplinkas. |
| **Būsena**                         | Nerekomenduojama: Suplanuota pašalinimo data yra 2021 m. spalio mėn. |

## <a name="feature-deprecation-effective-may-2021"></a>Pranešimas apie funkcijos nerekomendavimą, įsigaliojantį nuo 2021 m. gegužė

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>„Lifecycle Services“ (LCS) Globalizacijos portalas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | Mes neberekomenduojame LCS globalizacijos portalo, nes šią funkciją pakeitė kitos LCS paslaugos. |
| **Pakeitė kita funkcija?**   | Taip, ši funkcija pakeičiama LCS [Problemų ieška](../lifecycle-services/issue-search-lcs.md) ir [„Dynamics” reguliavimo įspėjimo pateikimo tarnyba](../lcs-solutions/submit-localization-alerts.md). |
| **Paveiktos produkto sritys**         | LCS globalizacijos portalas|
| **Visuotinio diegimo parinktis**              | Visuotinis debesies diegimas |
| **Būsena**                         | Nerekomenduojama: Suplanuota pašalinimo data yra 2022 m. gegužės mėn. |


## <a name="feature-removed-effective-january-28-2021"></a>Funkcija bus pašalinta nuo 2021 m. sausio mėn 28 d.

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Paketinė užduotis SQL indekso defragmentavimui apdoroti

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Ši funkcija buvo pašalinta norint sumažinti klientų rodyklės valdymo vykdymo, stebėjimo ir priežiūros pridėtines išlaidas. |
| **Pakeitė kita funkcija?**   | Ateityje rodyklės priežiūrą atliks „Microsoft” tarnybos. Tai bus daroma nuolat, nepaveikiant vartotojo darbo krūvių. |
| **Paveiktos produkto sritys**         | „Finance and operations” programos|
| **Visuotinio diegimo parinktis**              | Debesies diegimas – paveikia „Microsoft” valdomas gamybos ir 2‑5 pakopų smėlio dėžės aplinkas. |
| **Būsena**                         | Ši funkcija yra pašalinta. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Finansų ir operacijų programėlių 10.0.17 versijos platformos naujinimai


### <a name="visual-studio-2015"></a>„Visual Studio 2015“

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Norint, kad būtų palaikomos naujausios „Visual Studio” versijos, reikia atlikti tam tikrus X + + plėtinių, skirtų „Visual Studio”, keitimus. Šie pakeitimai nesuderinami su „Visual Studio” 2015. |
| **Pakeitė kita funkcija?**   | „Visual Studio 2017” bus pakeista „Visual Studio 2015” kaip įdiegta ir reikalinga versija. |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama: Atnaujinant, ankstesni X++ įrankiai bus pašalinti iš „Visual Studio 2015”, o atnaujinti įrankiai nebus įdiegti į „Visual Studio 2015”. Tai neturės įtakos nuomojamoms komponavimo versijoms. Komponavimo versijos virtualiosios mašinos pardavimo galimybės (komponavimo versijos apibrėžimas) turi būti atnaujintos rankiniu būdu tam, kad pakeisti priklausomybę iš „MSBuild 14.0” (2015 m. „Visual Studio”) į „MSBuild 15.0” (2017 m. „Visual Studio”), kaip aprašyta [Senstelėjusių pardavimo galimybių atnaujinimas „Azure” Pardavimo galimybės](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Vartotojo pseudoportretas 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Vartotojo pseudoportretas, rodomas dešinėje naršymo juostos pusėje, buvo nuskaitytas naudojant API iš „Dynamics 365” antraštės valdiklio, kuris yra nerekomenduojamas. |
| **Pakeitė kita funkcija?**   | Vietoj to vartotojai matys savo inicialus naršymo juostos apskritime. Tai tas pats vaizdinis elementas, šiuo metu naudojamas programavimo mašinose. |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Pašalinta iš 10.0.17 versijos |

### <a name="enterprise-portal-ep-deprecation"></a>Įmonės portalo (EP) netinkamumas  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Metaduomenų artefakai, susieti su "Dynamics AX 2012" įmonės portalu (EP), buvo pasenusi, nes EP niekada nebuvo palaikomas finansų ir operacijų programose. |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama: Numatyta, kad visas EP kodas bus pašalintas 2021 m. spalio leidime. |

## <a name="deprecation-effective-december-2020"></a>Pasenusios, 2020 m. gruodžio mėn.

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>„Internet Explorer 11“ palaikymas „Dynamics 365“ yra nutrauktas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Galioja iki 2020 Internet Explorer m. gruodžio 11 d. visi "Dynamics 365" produktai ir "Dynamics" ciklo tarnybos (LCS) pasenusios, Internet Explorer o 11 nebus palaikoma po 2021 m. rugpjūčio mėn.<br><br>Tai turės įtakos klientams, naudojantiems "Dynamics 365" produktus ir LCS, kurie sukurti naudoti naudojant Internet Explorer 11 sąsają. Po rugpjūčio 2021 m Internet Explorer . "11" nebus palaikomi "Dynamics 365" produktai ir LCS. |
| **Pakeitė kita funkcija?**   | Rekomenduojame klientams naudoti „Microsoft Edge“.|
| **Paveiktos produkto sritys**         | Visi "Dynamics 365" produktai ir LCS |
| **Visuotinio diegimo parinktis**              | Viskas|
| **Būsena**                         | Nerekomenduojama: „Internet Explorer 11“ nebus palaikoma nuo 2021 m. rugpjūčio.|

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Finansų ir operacijų programėlių 10.0.15 versijos platformos naujinimai

### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>„Visual Studio“ papildinys, skirtas metaduomenų karštųjų pataisų pritaikymui

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Metaduomenų karštosios pataisos nepalaikomos pristačius [vienos versijos](../../fin-ops/get-started/one-version.md) paslaugų naujinimus, kurie buvo pateikti 2018 m. liepą kartu su 8.1 versija. |
| **Pakeitė kita funkcija?**   | Nėra atskirų metaduomenų karštųjų pataisų, kurios būtų skirtos palaikomoms versijoms. Vietoje jų taikomi kaupiamieji kokybiniai naujinimai. |
| **Paveiktos produkto sritys**         | „Visual Studio“ papildiniai |
| **Visuotinio diegimo parinktis**              | Kūrimo virtualieji įrenginiai |
| **Būsena**                         | 10.0.15 versijoje papildinys nebėra įtrauktas į „Visual Studio“ įrankius. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Finansų ir operacijų programėlių 10.0.14 versijos platformos naujinimai

### <a name="online-users-page"></a>Prisijungusių vartotojų puslapis 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Tai yra ankstesnio kliento/serverio architektūroje sukurtas senstelėjęs puslapis. Šiame puslapyje pateikta informacija ne visada tiksli ir dėl to gali būti paini ir klaidinanti. |
| **Pakeitė kita funkcija?**   | Sekančiame atnaujinime pateiksime naują puslapį.|
| **Paveiktos produkto sritys**         | Sistemos administravimas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Iki 2021 m. spalio ši forma bus pašalinta.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Finansų ir operacijų programėlių 10.0.13 versijos platformos naujinimai


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Tinkintas kodas nustatytas SSRS ataskaitos ypatybėse 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Bendrai, tinkintas kodas siūlo apribotas naudas ir tuo pat metu reikalauja reikšmingų šaltinių papildymų ir paramos skyrimo. Tinkintas kodas daugiausiai naudojamas ataskaitų autorių siekiant iškviesti viešus metodus iš tinkinto kodo surinkimo. Nepaisant to, debesyje patalpintos paslaugos nepalaiko sąsajų su tinkintais susirinkimais SSRS ataskaitoms. |
| **Pakeitė kita funkcija?**   | Ataskaitų autoriai gali pasirinkti, ar tęsti susiejimą su viešomis .NET API matematikos, pavertimo ir formato veiksmams iš bet kurios teksto laukelio išraiškos. Dėl išsamesnės informacijos, žr. [Įtraukti kodą į ataskaitą (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs).  |
| **Paveiktos produkto sritys**         | Programos ataskaitos projektavimo papildomas rinkinys turi tinkintą kodą. |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Su versija 10.0.13, užpildymo įrankis pradės išduoti perspėjimus instancijoms, kuriose tinkintas kodas yra aptiktas SSRS ataskaitos sąvokoje. Tam, kad išspręstumėte šią problemą, atverkite ataskaitos projektavimo sąvoka ir pašalinkite visus tinkintus kodo artefaktus. Šis pranešimas bus pakeistas užpildymo klaida ateities atnaujinimuose.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Trijų „jQuery” komponentų bibliotekų atnaujinimas 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Trijų „jQuery” komponentų bibliotekos atnaujintos dėl saugumo spragų, kad būtų tvarkoma valiuta.   
| **Pakeitė kita funkcija?**   | Šiose bibliotekose matysis pakeitimai: „jQuery” (3.5.0 versiją iš 2.1.4 versijos), „jQuery UI” (1.12.1 versiją iš 1.11.4 versijos), „jQuery qTip” (3.0.3 versiją iš 2.2.1 versijos). „jQuery” internetu pateikė perkėlimo nurodymus.  |
| **Paveiktos produkto sritys**         | Išplėstiniai valdikliai, ypač pasirinktinis „JavaScript” kodas, naudojantis pasenusias arba pašalintas API |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | 10.0.13 versijoje/platformos atnaujinime Nr. 37 klientai gali pasirinktinai perkelti į naujausias bibliotekas įjungdami „Atnaujinti tris „jQuery” komponentų bibliotekas” funkciją. Perkėlimas į naujausias bibliotekas bus privalomas nuo 2021 m. balandžio mėnesio leidimo, kad būtų skirta laiko paveiktoms API perkelti.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Esamas tinklelio valdymas/forceLegacyGrid() API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Esamas tinklelio valdymas yra pakeičiamas nauju tinklelio valdymu. |
| **Pakeitė kita funkcija?**   | [Naujas tinklelio valdymas](../..//fin-ops/get-started/grid-capabilities.md) |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | 10.0.13 versijoje naujas tinklelio valdymas yra bendrai prieinamas ir klientai gali pasirinktinai įjungti šią funkciją. Naujasis tinklelio valdiklis taps numatytuoju 2021 m. spalio leidime ir šiuo metu numatoma, kad jis bus privalomas 2022 m. balandį. Kai naujas tinklelio valdymas tamp privalomas, **forceLegacyGrid()** API nebebus apdovanota. |

### <a name="personalization-without-saved-views"></a>Personalizavimas be įrašytų peržiūrų 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Personalizavimo papildoma sistema buvo perdaryta su naujomis įrašytomis peržiūros funkcijomis taip, kad ji galėtų geriau veikti ir siūlytų papildomas galimybes. |
| **Pakeitė kita funkcija?**   | Įrašyti rodiniai |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | 10.0.13 versijoje/platformos atnaujinimas 37, įrašyta peržiūros funkcija yra dažniausiai prieinama, o klientai gali pasirinktinai ją įjungti. Išsaugotų peržiūrų funkcija taps privaloma 2021 m. spalio mėn. leidime. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Finansų ir operacijų programėlių 10.0.12 versijos platformos naujinimai

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Tinklelio arba grupės valdiklio formų plėtiniai, kuriuose yra netinkamų laukų nuorodų

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Tinklelio arba grupės valdiklių duomenų grupės ypatybė naudojama automatiškai rodyti visus laukų grupės laukus. Tinklelyje arba grupės valdiklyje, pridėtame prie plėtinio, gali būti laukų, kurie nebėra apibrėžti laukų grupėje, arba jame gali būti trūkstamų laukų, kurie apibrėžti laukų grupėje. Tai gali sukelti nenuoseklų veikimą apdorojimo laiko metu. Dabar finansų ir operacijų programėlių 10.0.12 versijos platformos naujinimai klasifikuoja šią problemą kaip kompiliatoriaus *perspėjimą*. Norėdami išspręsti šią problemą, atidarykite formos plėtinį ir jį įrašykite.
| **Pakeitė kita funkcija?**   | Atliekant būsimą naujinimą, šis kompiliatoriaus įspėjimas bus pakeistas kompiliavimo klaidos pranešimu. |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Prie finansų ir operacijų programėlių versijos 10.0.12 atnaujinimų pateikiamas kompiliatoriaus perspėjimas. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Finansų ir operacijų programėlių 10.0.11 versijos platformos naujinimai

### <a name="explicit-safe-lists-for-self-service-environments"></a>Išsamūs baltieji sąrašai savitarnos aplinkoms

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | IP perkėlimo procesas į baltuosius sąrašus pasikeitė. Savitarna nebepalaiko IP baltųjų sąrašų. |
| **Pakeitė kita funkcija?**   | Daugiau informacijos rasite [„Azure Active Directory” sąlyginės prieigos konfigūracija](/appcenter/general/configuring-aad-conditional-access).|
| **Paveiktos produkto sritys**         | Sauga |
| **Visuotinio diegimo parinktis**              | Debesis |
| **Būsena**                         | Nuvertėjęs: Ši funkcija yra visiškai pasenusi savitarnos diegimui. |

### <a name="visual-studio-2015"></a>„Visual Studio 2015“

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Norint, kad būtų palaikomos naujausios „Visual Studio” versijos, reikia atlikti tam tikrus X + + plėtinių, skirtų „Visual Studio”, keitimus. Šie pakeitimai nesuderinami su „Visual Studio” 2015. |
| **Pakeitė kita funkcija?**   | „Visual Studio 2017” bus pakeista „Visual Studio 2015” kaip įdiegta ir reikalinga versija. |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Virtualiosiose mašinose, kurios naudojamos 10.0.13 (platformos atnaujinimas Nr. 37) arba naujesnėje versijoje, yra „Visual Studio 2017“. Versija 10.0.16 (platformos atnaujinimas Nr. 40) yra galutinis leidimas, palaikantis „Visual Studio 2015“. Virtualiųjų mašinų, kuriose veikia tik „Visual Studio 2015“, negalės atnaujinti į versiją 10.0.17 (platformos atnaujinimas Nr. 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Laukų grupės, kuriose pateiktos netinkamos laukų nuorodos

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Lentelės metaduomenų aprašuose gali būti laukų grupių, kuriose yra netinkamų laukų nuorodų. Įdiegus šias laukų grupes gali kiti vykdymo gedimų programose „Financial Reporting“ ir „Microsoft SQL Server Reporting Services“ (SSRS). 23 platformos naujinimas pristatė kompiliatoriaus *įspėjimą*, kuris įgalina šios metaduomenų problemos sprendimą. Finansų ir operacijų programėlių 10.0.11 versijos platformos naujinimai klasifikuoja šią problemą kaip kompiliatoriaus *klaidą*.<p>Norėdami ištaisyti šią problemą, vykdykite šiuos veiksmus.</p><ol><li>Pašalinkite netinkamą lauko nuorodą iš lentelės lauko grupės aprašo.</li><li>Perkompiliuokite.</li><li>Įsitikinkite, kad pašalintos visos klaidos.</li></ol> |
| **Pakeitė kita funkcija?**   | Ši kompiliatoriaus klaida visam laikui pakeičia kompiliatoriaus įspėjimą.  |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visi |
| **Būsena**                         | Pasenusi: kompiliatoriaus įspėjimas yra kompiliatoriaus klaida finansų ir operacijų programėlių 10.0.11 versijos platformoje. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV licencijos, sukurtos naudojant SHA1 maišos algoritmą

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pasikeitė nepriklausomo programinės įrangos tiekėjo (ISV) licencijų kūrimo procesas. Daugiau informacijos žr. [Nepriklausomo programinės įrangos tiekėjo (ISV) licencijavimas](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Pakeitė kita funkcija?**   | Taip. Norėdami sukurti licencijas, naudokite „Windows PowerShell”. |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Nebenaudojama: ISV licencijos, sukurtos naudojant SHA1 maišos algoritmą. Šis algoritmas priklausė nuo sertifikatų, sukurtų naudojant priemonę „MakeCert”, ir ši priemonė nebenaudojama.<br><br>Nebenaudojama: SHA1 naudojimas saugos arba maišos tikslais. SHA1 nustos veikti 2021 m. pradžioje. Todėl jos nebereikėtų naudoti.<br><br>Pašalinta: transportavimo lygmens saugos (TLS) 1.0 ir 1.1 versijų gaunamų ir siunčiamų užklausų palaikymas. |

## <a name="platform-update-32"></a>Platformos „update 32“

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Darbo eigos užklausos keitimo dialogo lange nebėra vartotojų pasirinkimo išplečiamojo sąrašo

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Dėl sąrašo galėjo kilti saugos problemų, nes keitimo užklausa galėjo būti nusiųsta nenumatytam vartotojui. Taip pat kilo tinkamumo naudoti problema, nes vartotojas buvo verčiamas nustatyti darbo eigos iniciatorių ir pasirinkti jį rankiniu būdu.  |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Darbo eiga |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Vartotojų pasirinkimo išplečiamasis sąrašas buvo pašalintas iš „Platform update 32“ keitimo užklausos dialogo lango. Užklausos keitimo užklausos bus automatiškai siunčiamos iniciatoriui, kaip numatyta. Norėdami gauti daugiau informacijos apie šią funkciją, žr. skyrių [Darbo eigos patvirtinimo procesų veiksmai](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Sunumeruoti dokumentai, kuriuos generuoja debesies paslauga, nebepalaiko įterptųjų detalizuotų nuorodų 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Naršymo URL, įterpti į paslaugos generuojamus dokumentus, gali būti slaptų verslo duomenų. Norėdami apsaugoti kliento duomenis, saugumo sumetimais pašalinsime įterptųjų detalizuotų nuorodų, esančių dokumentuose, palaikymą. Dėl šio pakeitimo vartotojai galės kurti dokumentus našiai ir interaktyviai.  |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Ataskaitos |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Ši funkcija yra šalinama iš paslaugos.<br><br>Šiuolaikinis klientas siūlo daugybę galimybių, kaip kurti vaizdus, kuriuose yra automatiškai sugeneruotų nuorodų, padedančių naršyti programoje. Rekomenduojama paslaugoje esančius sunumeruotus dokumentus naudoti išoriniams ryšiams, kurie gavėjams siunčiami el. paštu, archyvuojami ir spausdinami. Patobulinome dokumentų peržiūrą tiesiogiai naršyklėje, per kurią suteikiama tiesioginė prieiga prie vietinių spausdintuvų. Daugiau informacijos ieškokite [„PDF dokumentų peržiūra naudojant įdėtąją peržiūros programą“](../analytics/preview-pdf-documents.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas
Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../migration-upgrade/deprecated-features.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


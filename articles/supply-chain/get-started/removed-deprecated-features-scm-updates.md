---
title: Pašalintos arba nebenaudojamos „Dynamics 365 Supply Chain Management“ funkcijos
description: Šiame straipsnyje aprašomos priemonės, kurios buvo pašalintos arba suplanuotos šalinti Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 949fa0df58bc3338c8bc84ecbd4f2ad17117dd12
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865272"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Pašalintos arba nebenaudojamos „Dynamics 365 Supply Chain Management“ funkcijos

[!include [banner](../includes/banner.md)]

Šis straipsnis bus atnaujintas, nes naujos pašalintos arba pasenusios priemonės bus dokumentuotos Dynamics 365 Supply Chain Management.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą.

> [!NOTE]
> Išsami informacija apie finansų ir operacijų programėlių objektus pateikta techninės [nuorodos ataskaitose](/dynamics/s-e/). Galite palyginti skirtingas šių ataskaitų versijas ir sužinoti apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje finansų ir operacijų programėlių versijoje.


## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Supply Chain Management“ 10.0.19 versijoje

### <a name="job-card-device"></a>Užduoties kortelės įrenginys

| &nbsp;  | &nbsp;  |
|---|---|
| **Nerekomendavimo / pašalinimo priežastis** | Užduočių [kortelės](../production-control/config-job-card-device.md) įrenginys pakeičiamas nauja gamybos [laiko vykdymo](../production-control/production-floor-execution-configure.md) sąsaja. |
| **Pakeitė kita funkcija?**   | Taip, [kortelės](../production-control/config-job-card-device.md) įrenginys bus pakeista nauja gamybos [laiko vykdymo](../production-control/production-floor-execution-configure.md)  sąsaja. |
| **Paveiktos produkto sritys** | „Supply Chain Management“ – gamybos kontrolė |
| **Visuotinio diegimo parinktis** | Debesies ir vietinis |
| **Būsena** | Nerekomenduojama. Darbo kortelės prietaisas vis dar gaus palaikymą su klaidų ir saugumo pataisomis, tačiau nebebus pateikiami funkcijų patobulinimai. Po 2022 m. balandžio mėnesio, darbo kortelės prietaisas nebebus palaikomas, o klientų bus prašoma persikelti į naują gamybos aukšto vykdymo sąsają. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Supply Chain Management“ 10.0.18 versijoje

### <a name="dynamics-365-for-finance-and-operations---warehousing-the-warehouse-app"></a>„Dynamics 365 for Finance and Operations” – sandėliavimas (sandėlio programa)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Galioja nuo 2021 *m. balandžio 365 d. finansų ir operacijų " Dynamics 365" – sandėliavimas (sandėlio programa) yra pasenusi ir po 2022 m. balandžio mėn. nebus palaikomas*. Dabar ji pakeista *Sandėlio valdymo mobiliųjų įrenginių programėle*, kuri buvo išleista kartu su „Supply Chain Management” 10.0.17 versija. Nauja programa yra visiškas pakeitimas, tačiau naudoja tą pačią pagrindinę sistemą, kas palengvina perkėlimą. Jei reikia, dvi programas galima naudoti paraleliai tam, kad padėtų vartotojams palaipsniui prisitaikyti, kol jie mokosi naudotis nauja programa.<br><br>Daugiau informacijos apie naująją sandėlio valdymo mobiliųjų įrenginių programėlę rasite [ Sandėlio valdymo mobiliųjų įrenginių programėlė](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) ir [ Sandėlio valdymo mobiliųjų įrenginių programėlės diegimas ir prijungimas](../warehousing/install-configure-warehouse-management-app.md). |
| **Pakeitė kita funkcija?**   | Taip, pakeista nauja sandėlio valdymo mobiliųjų įrenginių programėle. |
| **Paveiktos produkto sritys**         | „Supply Chain Management” – sandėlio programa |
| **Visuotinio diegimo parinktis**              | Debesies ir vietinis |
| **Būsena**                         | Nerekomenduojama. Sandėlio programa vis dar gaus palaikymą su klaidų ir saugumo pataisomis, tačiau nebebus pateikiami funkcijų patobulinimai. Po 2022 m. balandžio mėnesio, senoji sandėlio programa nebebus palaikoma, o klientų bus prašoma persikelti į naują sandėlio valdymo mobiliųjų įrenginių programėlę. Tada senoji sandėlio programa bus pašalinta iš „Microsoft Store” ir „Google Play” parduotuvės.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Supply Chain Management“ 10.0.15 versijoje

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>„Internet Explorer“ 11 palaikymas „Dynamics 365“ nebegalioja

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Nuo 2020 m. gruodžio „Microsoft Internet Explorer 11“ palaikymas visuose „Dynamics 365“ produktuose yra nutraukiamas, o „Internet Explorer 11“ nebus palaikomas nuo 2021m. rugpjūčio.<br><br>Tai paveiks klientus, kurie naudoja „Dynamics 365“ produktus, skirtus naudoti „Internet Explorer 11“ sąsają. Nuo 2021m. rugpjūčio „Internet Explorer 11“ nebus palaikomas tokiuose „Dynamics 365“ produktuose. |
| **Pakeitė kita funkcija?**   | Rekomenduojame klientams naudoti „Microsoft Edge“.|
| **Paveiktos produkto sritys**         | Visi „Dynamics 365“ produktai |
| **Visuotinio diegimo parinktis**              | Visos|
| **Būsena**                         | Nebenaudojama. „Internet Explorer“ 11 nebebus palaikomas po 2021 m. rugpjūčio.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Naudokite sukurtą „Supply Chain Management“ pagrindinį planavimo variklį gamybos scenarijams

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Siekiant padidinti našumą ir sumažinti SQL duomenų bazės apkrovą bendrojo planavimo vykdymų metu, įtaisytasis „Supply Chain Management” bendrojo planavimo mechanizmas yra pakeičiamas planavimo optimizavimu. Planavimo optimizavimas leidžia greitai planuoti vykdymus, kuriuos galima atlikti netgi darbo valandomis. Dėl to planuotojai iš karto reaguoja į poreikio arba planavimo parametrų pasikeitimus. |
| **Pakeitė kita funkcija?**   | Taip, planavimo optimizavimas pakeis dabartinį įtaisytąjį „Supply Chain Management“ bendrojo planavimo mechanizmą. |
| **Paveiktos produkto sritys**         | „Supply Chain Management” – bendrasis planavimas |
| **Visuotinio diegimo parinktis**              | Tik debesyje. Planavimo optimizavimas nepalaikomas vietiniuose visuotiniuose diegimuose. |
| **Būsena**                         | Nerekomenduojama. Iki 2022 m. balandžio 1 d. įtaisytasis tiekimo grandinės valdymo bendrojo planavimo modulis nebepalaiko gamybos scenarijų. Nuo tos datos Microsoft sustabdys visą aktyvų įtaisytojo planavimo modulio gamybos scenarijų vystymas, neišleis naujų funkcijų ir išleis tik kritines klaidos pataisas. Po tos datos visos įmonės, kurioms reikia gamybos scenarijų palaikymo, savo bendrojo planavimo skaičiavimams turi naudoti planavimo optimizavimą. Tikimasi, kad planavimo optimizavimas visiškai palaikys gamybos scenarijus iki 2022 m. spalio mėn. Daugiau informacijos ieškokite planavimo optimizavimo [dokumentuose](../master-planning/planning-optimization/planning-optimization-overview.md).<br><br>Įmonės, kurioms taikomos jav tiekimo grandinės valdymo sistemos, po 2022 m. balandžio mėn. gali toliau naudoti įtaisytą bendrojo planavimo vedlį gamybos scenarijams. Tačiau daugiau funkcijų patobulinimų nebus teikiama. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Pašalintos arba nebenaudojamos funkcijos, esančios „Supply Chain Management“ 10.0.11 versijoje

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Įtaisytojo „Supply Chain Management“ bendrojo planavimo mechanizmo naudojimas paskirstymo scenarijuose

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Siekiant padidinti našumą ir sumažinti SQL duomenų bazės apkrovą bendrojo planavimo vykdymų metu, įtaisytasis „Supply Chain Management” bendrojo planavimo mechanizmas yra pakeičiamas planavimo optimizavimu. Planavimo optimizavimas leidžia greitai planuoti vykdymus, kuriuos galima atlikti netgi darbo valandomis. Dėl to planuotojai iš karto reaguoja į poreikio arba planavimo parametrų pasikeitimus. |
| **Pakeitė kita funkcija?**   | Taip, planavimo optimizavimas pakeis dabartinį įtaisytąjį „Supply Chain Management“ bendrojo planavimo mechanizmą. |
| **Paveiktos produkto sritys**         | „Supply Chain Management” – bendrasis planavimas |
| **Visuotinio diegimo parinktis**              | Tik debesyje. Planavimo optimizavimas nepalaikomas vietiniuose visuotiniuose diegimuose. |
| **Būsena**                         | Nebenaudojama. Nuo 2021 m. balandžio 1 d. paskirstymo scenarijai nebebus palaikomi su įdiegtu „Dynamics 365 Supply Chain Management“ pagrindinio planavimo varikliu. Paskirstymo scenarijuose klientai turi naudoti bendrojo planavimo skaičiavimo planavimo optimizavimą. Daugiau informacijos žr. [Planavimo optimizavimo dokumentacija](../master-planning/planning-optimization/planning-optimization-overview.md). Klientai, turintys vietinius visuotinius „Dynamics 365 Supply Chain Management” diegimus, po 2021 m. balandžio mėn. gali toliau naudoti „Supply Chain Management” bendrojo planavimo mechanizmą paskirstymo scenarijuose. Tačiau daugiau funkcijų patobulinimų nebus teikiama. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas

Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

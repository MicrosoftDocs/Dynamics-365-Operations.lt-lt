---
title: Sistemos reikalavimai
description: "Šia tema pateikiami dabartinėje Microsoft Dynamics 365 operacijų sistemos reikalavimai."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>Sistemos reikalavimai

Šia tema pateikiami dabartinėje Microsoft Dynamics 365 operacijų sistemos reikalavimai.

<a name="supported-web-browsers"></a>Palaikomos žiniatinklio naršyklės
----------------------

Microsoft Dynamics 365 operacijų žiniatinklio taikomosios programos gali veikti bet kurioje iš šių interneto naršyklių, kurios vykdomos nurodytų operacinių sistemų:

-   "Microsoft Edge" (paskutinis viešai prieinamos versija) "Windows 10"
-   „Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.
-   Google Chrome (naujausios viešai prieinamos versija) Windows 10, Windows 8.1, Windows 8, "Windows 7" arba "Google" Nexus 10 tabletė
-   Apple Safari (paskutinis viešai prieinamos versija) Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) arba 10.12 (Siera) ar Apple iPad

Norėdami rasti naujausią kiekvienos žiniatinklio naršyklės leidimą, eikite į programinės įrangos gamintojo svetainę. **Pastabos**

-   Fiksuoti vaizdus, kurie yra generuojami iš užduočių rašytuvą ir įtraukti juos į "Microsoft Word" dokumentus, turite turėti įdiegtą "Chrome" plėtinį. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Eigų rengyklėje pradėjo kaip "ClickOnce" taikomosios programos. Tik "Microsoft Edge" ir "Internet Explorer" (dėl Microsoft Windows palaikoma versija) parama "ClickOnce" taikomosios programos. Darbo eigos rengyklę "ClickOnce" taikomosios programos, reikia 64 bitų suderinamą operacinę sistemą.
-   Ataskaitų konstruktorius finansinėms ataskaitoms yra pradėjo kaip "ClickOnce" taikomosios programos. Tam reikia 64 bitų suderinamą operacinę sistemą. Jei naudojate "Chrome", turite įdiegti "ClickOnce" taikomosios išplėtimas norint atsisiųsti ataskaitą dizainerio klientas. Jei naudojate "Chrome" inkognito režimu, įsitikinkite, kad "ClickOnce" taikomosios pratęsimo taip pat yra įjungtas inkognito režimu.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Palaikomos „Retail Cloud POS‟ žiniatinklio naršyklės

Retail debesis POS Dynamics "365" operacijoms vykdyti bet kurioje iš šių interneto naršyklių, kurios vykdomos nurodytų operacinių sistemų:

-   "Microsoft Edge" (paskutinis viešai prieinamos versija) "Windows 10"
-   „Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.
-   "Chrome" (paskutinis viešai prieinamos versija) Windows 10, Windows 8.1 arba Windows 7

## <a name="network-requirements"></a>Tinklo reikalavimai
-   Dinamika 365 veiklai skirtas tinklus su latentinis mažiau nei 150 milisekundžių (ms). Tai yra gaištis iš naršyklės kliento Microsoft Azure duomenų centre, kuriame yra Dynamics 365 operacijoms. Mes rekomenduojame, kad jūs išbandyti tinklo latency ne <http://www.azurespeed.com>.
-   Reikalavimai pralaidumo Dynamics 365 operacijoms priklauso nuo jūsų scenarijų. Labiausiai būdingas scenarijus reikalauja pralaidumo daugiau kaip 50 kilobaitų per sekundę (KBps). Tačiau scenarijus, kurie turi aukštos naudingosios apkrovos reikalavimus, pvz., darbo vietos ar scenarijus, kurie apima platų pritaikymą, rekomenduojama daugiau duomenų srauto.

Apskritai, Dynamics 365 operacijoms yra optimizuota internete. Pirmyn ir atgal iš naršyklės kliento Azure duomenų centre yra labai maža, ir visa apkrova yra suspaustas. **Perspėjimas:** negalima apskaičiuoti pralaidumo reikalavimus kliento vietoje, vartotojų skaičius padauginus minimalų pralaidumo reikalavimus. Lygiagrečiojo naudojimo konkrečioje vietoje yra labai sunku apskaičiuoti. Klientams, kurie yra susirūpinę dėl pralaidumo reikalavimus, Dynamics 365 preview versijos naudoti operacijoms.

## <a name="net-framework-requirements"></a>.NET framework reikalavimus
Dinamika 365 operacijoms reikalingas .NET Framework versija 4.6.2 visus spustelėkite-vieną kartą programų, pavyzdžiui, dokumento Kelvados agentas. Diegimo nurodymus, ieškokite [įdiegus .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Palaikomos Microsoft Office programas
-   Paleisti Microsoft Excel ir Word priedai, turite turėti Microsoft Office 2016 skirta "Windows" arba "Mac" įdiegta. Daugiau informacijos apie versijos reikalavimus, [trikčių šalinimas Office integracijos](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Norėdami peržiūrėti dokumentus, kuriuos generuoja eksportuoti į "Excel" arba eksportuoti į Word funkcijos, turite turėti Microsoft Office 2007 arba naujesnė jos versija.

## <a name="retail-modern-pos-requirements"></a>Mažmeninės prekybos šiuolaikinės EKA reikalavimus
### <a name="supported-operating-systems"></a>Palaikomos operacinės sistemos

-   Mažmeninės prekybos šiuolaikinės EKA yra 32 bitų programa, bet ji veiks x86 ir x64 architektūra.
-   Mažmeninės prekybos šiuolaikinės EKA palaiko tik "Windows 10 Pro, Enterprise ir įmonės ilgas terminas aptarnavimo filialas (LTSB) leidimai.

### <a name="minimum-system-requirements"></a>Minimalūs sistemos reikalavimai

-   Minimali palaikoma rezoliucija yra 1280 × 1024 raiška.
-   Kompiuteryje, kuriame veikia modernus Retail POS turi atitikti šiuos reikalavimus:
    -   Jis turi bent dviejų branduolių procesorius, kuris veikia ne mažiau kaip 2 gigahercų (GHz).
    -   Ji turi būti, bent jau 3 gigabaitų (GB) RAM.
    -   Ji turi turėti prieigą prie interneto.

## <a name="retail-hardware-station-requirements"></a>Mažmeninė stotis reikalavimai aparatūrai
### <a name="supported-operating-systems"></a>Palaikomos operacinės sistemos

-   Aparatūros Postal yra 32 bitų programa, bet ji veiks x86 ir x64 architektūra.
-   Postal aparatūra palaiko šias operacines sistemas:
    -   Windows 7 Professional, Enterprise ir Ultimate leidimus **Pastaba:** Windows 7 palaiko tik tuomet Internet Explorer 11 yra rankiniu būdu įdiegtas sistemoje.
    -   Windows 8.1 naujinimas 1 Professional, Enterprise ir Embedded leidimuose
    -   Windows 10 Pro, Enterprise ir Enterprise LTSB leidimai

### <a name="minimum-system-requirements"></a>Minimalūs sistemos reikalavimai

Kompiuteris turi atitikti visos sistemos reikalavimai diegti ir naudoti šių elementų:

-   Interneto informacijos tarnybos (IIS)
-   Trečiųjų šalių aparatūrą

## <a name="retail-store-scale-unit-requirements"></a>Mažmeninės prekybos parduotuvės skalės vieneto reikalavimus
### <a name="supported-operating-systems"></a>Palaikomos operacinės sistemos

-   Mažmeninės prekybos parduotuvėje skalės vieneto yra 32 bitų programa, bet ji veiks x86 ir x64 architektūra.
-   Mažmeninės prekybos parduotuvėje skalės vieneto palaiko šias operacines sistemas:
    -   Windows 7 Professional, Enterprise ir Ultimate leidimus
    -   Windows 8.1 naujinimas 1 Professional, Enterprise ir Embedded leidimuose
    -   Windows 10 Pro, Enterprise ir Enterprise LTSB leidimai

### <a name="minimum-system-requirements"></a>Minimalūs sistemos reikalavimai

-   4 GB RAM
-   1.6 GHz didžiausios procesoriaus greičio branduolio (dviejų branduolių yra minimali).
-   Ne mažiau kaip 10 GB laisvos vietos (kanalo duomenų bazės gali pareikalauti daug vietos.)

### <a name="recommended-system-requirements"></a>Rekomenduojami sistemos reikalavimai

-   6 GB RAM
-   2.4 GHz i7 (arba jo atitikmuo) piko CPU greitis už pagrindinių (keturių šerdžių rekomenduojama).
-   Ne mažiau kaip 10 GB laisvos vietos (kanalo duomenų bazės gali pareikalauti daug vietos.)

## <a name="requirements-for-development-on-local-vms"></a>Reikalavimai plėtrai dėl vietinių LSS
Informacijos apie vystymosi reikalavimus vietinės virtualiosios mašinos (VM), [v. veikia vietiniame](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Gauti vertinimo kopija Dynamics 365 operacijoms](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)



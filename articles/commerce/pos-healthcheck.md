---
title: EKA periferinių įrenginių ir paslaugų sveikatos patikra
description: Šiame straipsnyje pateikta tikrinti sveikatos patikrą point (EKA).
author: BrianShook
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 44fd4b6246d3d7947527416c2b8b447bd64f179f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863326"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>EKA periferinių įrenginių ir paslaugų sveikatos patikra

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma sveikatos tikrinimo operacija, atliekama point of sale (EKA).

## <a name="overview"></a>Peržiūra

Mažmeninėse parduotuvėse naudojama daug įvairių programų ir įrenginių. Kadangi operacijų vis daugėja, gali būti sunku užtikrinti, kad jos visada vyktų sklandžiai. Pavyzdžiui, periferiniai įrenginiai dienos metu gali sugesti ar netyčia atsijungti. Trikčių, susijusių su įrenginiais ir paslaugomis, šalinimas didesniems prekybininkams gali brangiai kainuoti. Ne mažiau varginantis trikčių šalinimas ir mažesniems prekybininkams.

„Microsoft Dynamics 365 Commerce“ 10.0.10 ir naujesnėse versijose yra sveikatos patikros funkcija, kuri gali padėti išvengti nusivylimo ir papildomų išlaidų skyrimo. Ši funkcija tikrina įrenginius tiesiogiai iš EKA, kurie tinkamai neveikia. Todėl ji gali padėti mažmenininkams aptikti problemas prieš joms atsirandant.

## <a name="key-terms"></a>Pagrindiniai terminai

| Semestras | aprašymas |
|---|---|
| Išorinis įrenginys | Bet koks įrenginys, kurį naudoja EKA programa, kad palengvintų įvairių operacijų veikimą parduotuvėje. Pavyzdžiui, kasos stalčiai, brūkšninių kodų skaitytuvai ir mokėjimo terminalai. |
| Aptarnavimas | Šiame straipsnyje paslauga yra papildoma programa, nuo kurios priklauso EKA programa, vykdo operacijas ir kasdienes operacijas. Pavyzdžiui, programėlės, kurios padeda apskaičiuoti mokesčius ar siuntas. |

## <a name="health-check-operation"></a>Sveikatos patikros funkcija

Sveikatos patikros funkcija yra 717 operacija, esanti „Commerce Headquarters“ puslapyje **EKA operacijos**. Ji gali būti naudojama, kai EKA yra ne stalčiaus režime. Tačiau aparatūros stotis turi būti aktyvi.

Pagal numatytuosius nustatymus sveikatos patikros atliekamos tik tuose įrenginiuose, kurie yra sukonfigūruoti aparatūros stoties aparatūros profilyje, kuri šiuo metu yra aktyvi registrui. Jei registras per dieną naudoja kelias aparatinės įrangos stotis, norėdamas atlikti visų jų sveikatos patikrą, jis vienu metu gali prisijungti tik prie vienos aparatūros stoties. Nėra sveikatos patikros parduotuvės lygiu. Tačiau gali būti, kad tokio tipo patikras galima atlikti naudojant „Commerce Server“ išplėtimą.

### <a name="out-of-box-health-checks"></a>Parengtos naudoti sveikatos patikros

| Tipas | Ryšys | Informacija |
|---|---|---|
| Spausdintuvas | OEKA | Ši patikra tikrina pagrindinį objekto susiejimą ir įdėjimą į EKA (OEKA) funkcijas. Štai keletas pavyzdžių:<ul><li>Atidaryti: **Atidaryti** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uždaryti: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Uždaryti**</li></ul> |
| Eilutės rodymas | OEKA | Ši patikra tikrina pagrindines OEKA funkcijas. Štai keletas pavyzdžių:<ul><li>Atidaryti: **Atidaryti** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uždaryti: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Uždaryti**</li></ul> |
| Dvigubas rodymas | „Windows“ | Ši patikra užtikrina, kad operacinė sistema aptiktų antrą „Windows“ ekraną. | 
| MSR | OEKA | Ši patikra tikrina pagrindines OEKA funkcijas. Štai keletas pavyzdžių:<ul><li>Atidaryti: **Atidaryti** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uždaryti: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Uždaryti**</li></ul> |
| Stalčius | OEKA | Ši patikra tikrina pagrindines OEKA funkcijas. Štai keletas pavyzdžių:<ul><li>Atidaryti: **Atidaryti** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uždaryti: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Uždaryti**</li></ul> | 
| Skaitytuvas | OEKA | Ši patikra tikrina pagrindines OEKA funkcijas. Štai keletas pavyzdžių:<ul><li>Atidaryti: **Atidaryti** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uždaryti: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Uždaryti**</li></ul> | 
| Skalė | OEKA | Ši patikra tikrina pagrindines OEKA funkcijas. Štai keletas pavyzdžių:<ul><li>Atidaryti: **Atidaryti** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uždaryti: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Uždaryti**</li></ul> |
| PIN rinkiklis | OEKA | Ši patikra tikrina pagrindines OEKA funkcijas. Štai keletas pavyzdžių:<ul><li>Atidaryti: **Atidaryti** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Uždaryti: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Uždaryti**</li></ul> |
| Mokėjimo terminalas | SDK mokėjimai | Ši patikra tikrina pagrindines mokėjimo terminalo funkcijas, kurias teikia „Payments SDK“. <ul><li>Blokuoti</li><li>Pradėti operaciją</li><li>Baigti operaciją</li><li>ReleaseDevice</li><li>Artimas</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>Sveikatos patikros funkcijos naudojimas EKA

Kai EKA inicijuojama sveikatos patikros operacija, dešinėje esančioje srityje rodomi sukonfigūruoti įrenginiai ir rodoma kiekvieno įrenginio būsena. Norėdami atlikti vieno įrenginio sveikatos patikrą, pasirinkite įrenginį ir pasirinkite **Tikrinti pažymėtus**. Norėdami atlikti visų įrenginių sveikatos patikrą, pasirinkite **Tikrinti visus**. Funkcija **Tikrinti visus** tikrina visus įrenginius vienu metu ir atnaujina kiekvieno įrenginio būseną stulpelyje **Būsena**.

Stulpelis **Paskutinis tikrinimas** parodo, kada paskutinį kartą buvo atlikta kiekvieno įrenginio sveikatos patikra.

Jei įrenginys praeina sveikatos patikrą (t. y., jame nerandama klaidų), įrenginio būsena nustatoma į **Gerai**. Jei sveikatos patikra nepavyko, būsenoje nurodoma klaida. Tokiu atveju dešinėje esančioje srityje pateikiama išsami informacija, susijusi su klaida, arba vartotojui nurodoma susisiekti su sistemos administratoriumi.

Kai kuriuose įrenginiuose, pavyzdžiui, EKA klaviatūros užrakte, nėra parengtų naudoti sveikatos patikrų. Jei bet kuriame naudojamame įrenginyje neaptinkama sveikatos patikra, rodoma būsena **Nepalaikoma**.

### <a name="extending-health-checks"></a>Sveikatos patikrų išplėtimas

Parengtos naudoti sveikatos patikros sukonfigūruotos taip, kad pateiktų kelis vartotojui patogius pranešimus apie tipiškas klaidas. Tačiau įtraukiami ne visi scenarijai. Naudodami išplečiamumą prekybininkai gali susieti vartotojui tinkančius pranešimus su klaidomis, kurios gali būti būdingos jų aplinkai.

Pasirinktines sveikatos patikras taip pat galima sukurti norint išbandyti parengtus naudoti nepalaikomus įrenginius arba išbandyti visas paslaugas, nuo kurių priklauso EKA.

## <a name="related-articles"></a>Susiję straipsniai

[Modernūs EKA (MPOS) paleidikliai ir spausdinimas](dev-itpro/pos-trigger-printing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
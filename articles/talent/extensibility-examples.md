---
title: „Talent“ išplėtimas naudojant „PowerApps“ ir „Microsoft Flow“ – scenarijų pavyzdžiai
description: Šioje temoje aprašomi keli „Microsoft Dynamics 365 for Talent“ išplėtimo scenarijų pavyzdžiai, kai naudojama „Microsoft PowerApps“ ir „Microsoft Flow“.
author: negudava
manager: Annbe
ms.date: 03/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0aa3578047b9397682a7039d0dbcc05cc1b167e4
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/12/2019
ms.locfileid: "949925"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>„Talent“ išplėtimas naudojant „PowerApps“ ir „Microsoft Flow“ – scenarijų pavyzdžiai

Šioje temoje aprašomi keli „Microsoft Dynamics 365 for Talent“ išplėtimo scenarijų pavyzdžiai, kai naudojama „Microsoft PowerApps“ ir „Microsoft Flow“. Su kiekvienu pavyzdžiu susietą sprendimų paketą galite importuoti į savo „PowerApps“ aplinką. Paskui šiais paketais galite naudotis kaip nurodymais arba kaip atskaitos taškais jūsų organizacijai taikomiems scenarijams įgyvendinti.

> [!IMPORTANT]
> Norėdami šioje temoje aprašytus šablonus ir programą naudoti tokius, kokie jie yra, būtinai patikrinkite juos, kad įsitikintumėte, jog jie apima visus jūsų diegimui būdingus scenarijus.


## <a name="prerequisites"></a>Būtinieji komponentai

- Norėdami importuoti paketus, vartotojai privalo turėti teisę **Aplinkos kūrėjas**.
- Norėdami eksportuoti arba importuoti programas, vartotojai privalo turėti „PowerApps“ 2 plano licenciją arba bandomąją „PowerApps“ 2 plano licenciją.

## <a name="flow--form-connect"></a>Srautas – Formos prijungimas

Naudojantis šablonu **Srautas – Formos prijungimas** galima skaityti „Microsoft“ formų duomenis ir išsaugoti juos „Common Data Service“ objekte.

Šį šabloną galima išplėsti, kad jį būtų galima naudoti kitiems scenarijams. Štai keletas pavyzdžių:

- Kandidatų vertinimų fiksavimas.
- Kurso klausimynų rezultatų fiksavimas.
- Iš pokalbiuose su personalo išteklių administratoriais pateiktų klausimų sudarytos bibliotekos kompiliavimas.
- Kandidato pateikto pokalbio proceso vertinimo fiksavimas

Naudojantis „Microsoft Dynamics 365: Attract“, formos gali būti rodomos kandidatų portale ir kandidatai gali įvesti duomenis. Užduoties šablone formas galima įdėti ir kaip veiklas.

Kandidatui pateikus formą, „Microsoft Flow“ užfiksuoja formos pateikimą, nuskaito duomenis ir išsaugo juos „Common Data Service“ objekte.

Norėdami atsisiųsti šabloną **Srautas – Formos prijungimas** ir pasirinktinę objekto struktūrą, „Microsoft“ atsisiuntimo centre eikite į [Srautas – Formos prijungimas](https://go.microsoft.com/fwlink/?linkid=2081988).

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>„Powerapps“ perduodamų parametrų paleidimas ir išskleidimas

Šabloną **„Powerapps“ perduodamų parametrų paleidimas ir išskleidimas** galima naudoti kaip bet kurio „Attract“ būdingo „PowerApps“ scenarijaus pradžios tašką. Jis apima visus numatytuosius „Attract“ perduodamus parametrus, pavyzdžiui, **Prašymas įdarbinti**, **Kandidato ID** ir **JobID**.

Naudojantis šiuo šablonu galima gauti kandidato vertinimo formą, kad samdos vadovas galėtų peržiūrėti kandidato užpildytą vertinimo formą.

Naudojantis „PowerApps“ sukurtas programas galima įdėti į „Attract“ užduoties šabloną.

Norėdami atsisiųsti šabloną **„Powerapps“ perduodamų parametrų paleidimas ir išskleidimas** ir pasirinktinę objekto struktūrą, „Microsoft“ atsisiuntimo centre eikite į [„Powerapps“ perduodamų parametrų paleidimas ir išskleidimas](https://go.microsoft.com/fwlink/?linkid=2081991).

## <a name="integration-with-office-365"></a>Integravimas su „Office 365“

Naudojantis programa **Integravimas su „Office 365“**, iš „Microsoft Office 365“ galima gauti prisijungusių vartotojų komandos informaciją. Nurodomi „Talent“ darbuotojai, kurių atėjimo į darbą ir išėjimo iš darbo duomenys bei išimčių įrašai gaunami. Atėjimo į darbą ir išėjimo iš darbo duomenys saugomi pasirinktiniame „Common Data Service“ objekte. Daroma prielaida, kad šiuos duomenis įveda trečiųjų šalių sistemos naudodamosi integravimu.

Šią programą galima išplėsti, kad ją būtų galima naudoti kitiems scenarijams. Pavyzdžiui, naudojantis ja gali būti rodoma komandos atostogų informaciją, kalendoriaus įvykiai ir visi konkrečios komandos įvykiai.

Norėdami atsisiųsti programą **Integravimas su „Office 365“** ir pasirinktinę objekto struktūrą, „Microsoft“ atsisiuntimo centre eikite į [Integravimas su „Office 365“](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="flow--email-notification"></a>Srautas – El. paštu siunčiamas pranešimas

Šabloną **Srautas – El. paštu siunčiamas pranešimas** galima naudoti el. paštu siunčiamų pranešimų scenarijams. Juo naudojantis galima suaktyvinti el. paštu kandidatams siunčiamus pranešimus, kai samdos komanda bet kuriame įdarbinimo proceso etape juos atmeta.

Šį šabloną galima išplėsti, kad būtų galima sekti kandidato įdarbinimo proceso etapo pokyčius ir siųsti pranešimus samdos komandai ir kandidatui.

Apskritai, jei objektai saugomi „Common Data Service“, galima nustatyti, kad srautai siųstų pranešimus apie „Core HR“, „Attract“ arba „Dynamics 365 Talent: Onboard“ įvykius.

Norėdami atsisiųsti šabloną **Srautas – El. paštu siunčiamas pranešimas**, „Microsoft“ atsisiuntimo centre eikite į [Srautas – El. paštu siunčiamas pranešimas](https://go.microsoft.com/fwlink/?linkid=2082103).

## <a name="flow--sql-connect-and-execute"></a>Srautas – SQL prijungimas ir vykdymas

Naudojantis šablonu **Srautas – SQL prijungimas ir vykdymas** prisijungiama prie „Microsoft SQL Server“ ir galima vykdyti SQL užklausas.

Nors šis šablonas skirtas SQL lentelėms skaityti ir naujinti, jį galima išplėsti, kad jį galima būtų naudoti kitiems scenarijams. Pavyzdžiui, jį galima naudoti „Common Data Service“ išdėstymo lentelėje norint įvesti duomenis iš SQL serverio ir periodiškai sinchronizuojant išdėstymo lentelę naudojantis papildančiuoju skirstymu iš SQL serverio.

Norėdami atsisiųsti šabloną **Srautas – SQL prijungimas ir vykdymas**, „Microsoft“ atsisiuntimo centre eikite į [Srautas – SQL prijungimas ir vykdymas](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="flow--sharepoint-integration"></a>Srautas – „SharePoint“ integravimas

Naudojantis šablonu **Srautas – „SharePoint“ integravimas** galima nuskaityti „Microsoft SharePoint“ sąraše nurodytus duomenis, palyginti sąrašą su bet kurio „Common Data Service“ objekto laukų reikšmėmis ir išsiųsti palyginimo rezultatus kaip el. paštu siunčiamą pranešimą. 

Organizacija gali turėti tam tikrų skubiai reikiamų įgūdžių rinkinį. Šie įgūdžiai gali būti saugomi „SharePoint“ kaip „SharePoint“ sąrašas. Kai kandidatas kreipiasi dėl darbo ir norėdamas įsidarbinti turi turėti reikiamų įgūdžių rinkinyje išvardytų įgūdžių, aptikus didelį kandidato įgūdžių sutapimą su „SharePoint“ saugomais įgūdžiais, el. paštu išsiunčiamas pranešimas. Tokiu būdu pareigoms, kurioms darbuotojų reikia skubiai, jų surandama greičiau, nes naudojantis pranešimais darbdaviams lengviau ieškoti kandidatų visoje organizacijoje ir atlikti kryžminį įdarbinimą.

Šį šabloną galima išplėsti, kad jį būtų galima naudoti bet kuriam „SharePoint“ integraciją apimančiam scenarijui.

Norėdami atsisiųsti šabloną **Srautas – „SharePoint“ integravimas**, „Microsoft“ atsisiuntimo centre eikite į [Srautas – „SharePoint“ integravimas](https://go.microsoft.com/fwlink/?linkid=2082109).



## <a name="additional-resources"></a>Papildomi ištekliai

[„Microsoft Power Platform“](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Programos perkėlimas įvairiems nuomotojams ir į įvairias aplinkas](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)

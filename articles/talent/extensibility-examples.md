---
title: „Talent“ išplėtimas su „Power Apps“ ir „Power Automate“
description: Šiame skyriuje aprašomi keli „Microsoft Dynamics 365 Talent“ išplėtimo scenarijų pavyzdžiai, kuriuose naudojami „Microsoft Power Apps“ ir „Microsoft Power Automate“.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6c8a583a93c2ceb70d8c3b0e0047e2bf2047b56d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898322"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>„Talent“ išplėtimas su „Power Apps“ ir „Power Automate“

Šiame skyriuje aprašomi keli „Microsoft Dynamics 365 Talent“ išplėtimo scenarijų pavyzdžiai, kuriuose naudojami „Microsoft Power Apps“ ir „Microsoft Power Automate“. Su kiekvienu pavyzdžiu susietą sprendimų paketą galite importuoti į savo „Power Apps“ aplinką. Paskui šiais paketais galite naudotis kaip nurodymais arba kaip atskaitos taškais jūsų organizacijai taikomiems scenarijams įgyvendinti.

> [!IMPORTANT]
> Norėdami šioje temoje aprašytus šablonus ir programą naudoti tokius, kokie jie yra, būtinai patikrinkite juos, kad įsitikintumėte, jog jie apima visus jūsų diegimui būdingus scenarijus.


## <a name="prerequisites"></a>Būtinieji komponentai

- Norėdami importuoti paketus, vartotojai privalo turėti teisę **Aplinkos kūrėjas**.
- Norėdami eksportuoti arba importuoti programas, vartotojai privalo turėti „Power Apps“ 2 plano licenciją arba bandomąją „Power Apps“ 2 plano licenciją.

## <a name="power-automate--form-connect"></a>„Power Automate – Form Connect“

**Power Automate – Form Connect** šabloną galima naudoti norint nuskaityti duomenis iš „Microsoft Forms“ ir saugoti juos „Common Data Service“ objekte.

Šį šabloną galima išplėsti, kad jį būtų galima naudoti kitiems scenarijams. Štai keletas pavyzdžių:

- Kandidatų vertinimų fiksavimas.
- Kurso klausimynų rezultatų fiksavimas.
- Iš pokalbiuose su personalo išteklių administratoriais pateiktų klausimų sudarytos bibliotekos kompiliavimas.
- Kandidato pateikto pokalbio proceso vertinimo fiksavimas

Naudojantis „Microsoft Dynamics 365: Attract“, formos gali būti rodomos kandidatų portale ir kandidatai gali įvesti duomenis. Užduoties šablone formas galima įdėti ir kaip veiklas.

Kai kandidatas pateikia formą, „Microsoft Power Automate“ užfiksuoja formos pateikimą, nuskaito duomenis ir saugo juos „Common Data Service“ objekte.

Norėdami atsisiųsti **Power Automate – Form Connect** šabloną ir pasirinktinio objekto struktūrą, „Microsoft“ atsisiuntimų centre eikite į [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988).

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a>Parametrų, perduotų „ Power Apps“, inicijavimas ir ištraukimas

Šabloną **Parametrų, perduotų „Power Apps**“, inicijavimas ir ištraukimas“ galima naudoti kaip kiekvieno „Power Apps“ scenarijaus, kuris yra būdingas „Attract“, pradžios tašką. Jis apima visus numatytuosius „Attract“ perduodamus parametrus, pavyzdžiui, **Prašymas įdarbinti**, **Kandidato ID** ir **JobID**.

Naudojantis šiuo šablonu galima gauti kandidato vertinimo formą, kad samdos vadovas galėtų peržiūrėti kandidato užpildytą vertinimo formą.

Naudojant „Power Apps“ sukurtas programas galima įdėti į „Attract“ užduoties šabloną.

Norėdami atsisiųsti **Parametrų, perduotų „Power Apps“, inicijavimas ir ištraukimas** šabloną ir pasirinktinio objekto struktūrą, eikite į [Parametrų, perduotų „Power Apps“, inicijavimas ir ištraukimas](https://go.microsoft.com/fwlink/?linkid=2081991) „Microsoft“ atsisiuntimų centre.

## <a name="integration-with-office-365"></a>Integravimas su „Office 365“

Naudojantis programa **Integravimas su „Office 365“**, iš „Microsoft Office 365“ galima gauti prisijungusių vartotojų komandos informaciją. Nurodomi „Talent“ darbuotojai, kurių atėjimo į darbą ir išėjimo iš darbo duomenys bei išimčių įrašai gaunami. Atėjimo į darbą ir išėjimo iš darbo duomenys saugomi pasirinktiniame „Common Data Service“ objekte. Daroma prielaida, kad šiuos duomenis įveda trečiųjų šalių sistemos naudodamosi integravimu.

Šią programą galima išplėsti, kad ją būtų galima naudoti kitiems scenarijams. Pavyzdžiui, naudojantis ja gali būti rodoma komandos atostogų informaciją, kalendoriaus įvykiai ir visi konkrečios komandos įvykiai.

Norėdami atsisiųsti programą **Integravimas su „Office 365“** ir pasirinktinę objekto struktūrą, „Microsoft“ atsisiuntimo centre eikite į [Integravimas su „Office 365“](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="power-automate--email-notification"></a>„Power Automate – el. laiško pranešimas“

**Power Automate – el. laiško pranešimas** šabloną galima naudoti el. laiškų pranešimų scenarijams. Juo naudojantis galima suaktyvinti el. paštu kandidatams siunčiamus pranešimus, kai samdos komanda bet kuriame įdarbinimo proceso etape juos atmeta.

Šį šabloną galima išplėsti, kad būtų galima sekti kandidato įdarbinimo proceso etapo pokyčius ir siųsti pranešimus samdos komandai ir kandidatui.

Apskritai, jei objektai saugomi „Common Data Service“, galima nustatyti, kad srautai siųstų pranešimus apie „Core HR“, „Attract“ arba „Onboard“ įvykius.

Norėdami atsisiųsti **Power Automate – el. laiško pranešimas** šabloną, „Microsoft“ atsisiuntimų centre eikite į [Power Automate – el. laiško pranešimas](https://go.microsoft.com/fwlink/?linkid=2082103).

## <a name="power-automate--sql-connect-and-execute"></a>„Power Automate – SQL prisijungimas ir vykdymas“

**Power Automate – SQL prisijungimas ir vykdymas** šablonas prisijungia prie „Microsoft SQL Server“ ir leidžia vykdyti SQL užklausas.

Nors šis šablonas skirtas SQL lentelėms skaityti ir naujinti, jį galima išplėsti, kad jį galima būtų naudoti kitiems scenarijams. Pavyzdžiui, jį galima naudoti „Common Data Service“ išdėstymo lentelėje norint įvesti duomenis iš SQL serverio ir periodiškai sinchronizuojant išdėstymo lentelę naudojantis papildančiuoju skirstymu iš SQL serverio.

Norėdami atsisiųsti **Power Automate – SQL prisijungimas ir vykdymas** šabloną, „Microsoft“ atsisiuntimų centre eikite į [Power Automate – SQL prisijungimas ir vykdymas](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="power-automate--sharepoint-integration"></a>„Power Automate – SharePoint integravimas“

**Power Automate – SharePoint integravimas** šabloną galima naudoti norint nuskaityti duomenis iš „Microsoft SharePoint“ sąrašo, palyginti sąrašą su bet kurio „Common Data Service“ objekto lauko reikšmėmis ir siųsti palyginimo rezultatus kaip pranešimo el. laišką. 

Organizacija gali turėti tam tikrų skubiai reikiamų įgūdžių rinkinį. Šie įgūdžiai gali būti saugomi „SharePoint“ kaip „SharePoint“ sąrašas. Kai kandidatas kreipiasi dėl darbo ir norėdamas įsidarbinti turi turėti reikiamų įgūdžių rinkinyje išvardytų įgūdžių, aptikus didelį kandidato įgūdžių sutapimą su „SharePoint“ saugomais įgūdžiais, el. paštu išsiunčiamas pranešimas. Tokiu būdu pareigoms, kurioms darbuotojų reikia skubiai, jų surandama greičiau, nes naudojantis pranešimais darbdaviams lengviau ieškoti kandidatų visoje organizacijoje ir atlikti kryžminį įdarbinimą.

Šį šabloną galima išplėsti, kad jį būtų galima naudoti bet kuriam „SharePoint“ integraciją apimančiam scenarijui.

Norėdami atsisiųsti **Power Automate – SharePoint integravimas** šabloną, eikite į [Power Automate – SharePoint integravimas](https://go.microsoft.com/fwlink/?linkid=2082109) „Microsoft“ atsisiuntimų centre.

## <a name="referral-app"></a>Programėlė „Referral”
Programėlę „Referral” galite naudoti kandidatams įtraukti į bendrinamą talento telkinį. Pateikdamas kandidatą, jį rekomendavęs asmuo gali įvesti jo **vardą**, **pavardę**, **el. pašto adresą** ir **„LinkedIn“ URL**. Kandidato šaltinio metaduomenys yra įvedami kartu su jį rekomendavusio asmens informacija.

Galite įterpti šią programėlę į darbuotojų savitarną (ESS) teikti rekomendacijoms arba galite naudoti ją kaip hipersaitą įmonės portale ir vykdyti kaip atskirą programėlę.

Norėdami atsisiųsti **programėlę „Referral”**, eikite į [Dynamics 365 Talent išplečiamumo sprendimas: programėlė „Referral”](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) „Microsoft” atsisiuntimo centre. Galite importuoti šią programėlę ir pritaikyti papildomų funkcijų įtraukimui.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Microsoft Power Platform“](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Programos perkėlimas įvairiems nuomotojams ir į įvairias aplinkas](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)

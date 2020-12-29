---
title: „Talent“ išplėtimas su „Power Apps“ ir „Power Automate“
description: Šiame straipsnyje aprašomi keli „Microsoft Dynamics 365 Talent - Attract“ išplėtimo scenarijų pavyzdžiai, kuriuose naudojami „Microsoft Power Apps“ ir „Microsoft Power Automate“.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529639"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>„Talent“ išplėtimas su „Power Apps“ ir „Power Automate“

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šiame straipsnyje aprašomi keli „Microsoft Dynamics 365 Talent: Attract“ išplėtimo scenarijų pavyzdžiai, kuriuose naudojami „Microsoft Power Apps“ ir „Microsoft Power Automate“. Su kiekvienu pavyzdžiu susietą sprendimų paketą galite importuoti į savo „Power Apps“ aplinką. Paskui šiais paketais galite naudotis kaip nurodymais arba kaip atskaitos taškais jūsų organizacijai taikomiems scenarijams įgyvendinti.

> [!IMPORTANT]
> Norėdami šiame straipsnyje aprašytus šablonus ir programą naudoti tokius, kokie jie yra, būtinai patikrinkite juos, kad įsitikintumėte, jog jie apima visus jūsų diegimui būdingus scenarijus.


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

Naudodamiesi „Microsoft Dynamics 365: Attract“, galite naudoti formas kandidatų portale, kuriame kandidatai įveda duomenis. Užduoties šablone formas galite įdėti ir kaip veiklas.

Kai kandidatas pateikia formą, „Microsoft Power Automate“ užfiksuoja formos pateikimą, nuskaito duomenis ir saugo juos „Common Data Service“ objekte.

Norėdami atsisiųsti **Power Automate – Form Connect** šabloną ir pasirinktinio objekto struktūrą, „Microsoft“ atsisiuntimų centre eikite į [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988).

## <a name="power-automate--sharepoint-integration"></a>„Power Automate – SharePoint integravimas“

**Power Automate – SharePoint integravimas** šabloną galima naudoti norint nuskaityti duomenis iš „Microsoft SharePoint“ sąrašo, palyginti sąrašą su bet kurio „Common Data Service“ objekto lauko reikšmėmis ir siųsti palyginimo rezultatus kaip pranešimo el. laišką. 

Organizacija gali turėti tam tikrų skubiai reikiamų įgūdžių rinkinį. Šie įgūdžiai gali būti saugomi „SharePoint“ kaip „SharePoint“ sąrašas. Kai kandidatas kreipiasi dėl darbo ir norėdamas įsidarbinti turi turėti reikiamų įgūdžių rinkinyje išvardytų įgūdžių, aptikus didelį kandidato įgūdžių sutapimą su „SharePoint“ saugomais įgūdžiais, el. paštu išsiunčiamas pranešimas. Tokiu būdu pareigoms, kurioms darbuotojų reikia skubiai, jų surandama greičiau, nes naudojantis pranešimais darbdaviams lengviau atlikti kryžminį kandidatų įdarbinimą visoje organizacijoje.

Šį šabloną galima išplėsti, kad jį būtų galima naudoti bet kuriam „SharePoint“ integraciją apimančiam scenarijui.

Norėdami atsisiųsti **Power Automate – SharePoint integravimas** šabloną, eikite į [Power Automate – SharePoint integravimas](https://go.microsoft.com/fwlink/?linkid=2082109) „Microsoft“ atsisiuntimų centre.

## <a name="referral-app"></a>Programėlė „Referral”

Programėlę „Referral” galite naudoti kandidatams įtraukti į bendrinamą talento telkinį. Pateikdamas kandidatą, jį rekomendavęs asmuo gali įvesti jo duomenis: **Vardas**, **Pavardė**, **El. pašto adresas** ir **„LinkedIn“ URL**. Kandidato šaltinio metaduomenys yra įvedami kartu su jį rekomendavusio asmens informacija.

Galite įterpti šią programą į darbuotojų savitarną teikti rekomendacijoms arba galite naudoti ją kaip hipersaitą įmonės portale ir vykdyti kaip atskirą programą.

Norėdami atsisiųsti **programėlę „Referral”**, eikite į [Dynamics 365 Talent išplečiamumo sprendimas: programėlė „Referral”](https://www.microsoft.com/download/details.aspx?id=58497) „Microsoft” atsisiuntimo centre. Galite importuoti šią programėlę ir pritaikyti papildomų funkcijų įtraukimui.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Microsoft Power Platform“](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Programos perkėlimas įvairiems nuomotojams ir į įvairias aplinkas](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)

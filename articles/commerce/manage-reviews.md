---
title: Įvertinimų ir atsiliepimų tvarkymas
description: Šioje temoje paaiškinama, kaip tvarkyti įvertinimus ir apžvalgas naudojant „Microsoft Dynamics 365 Commerce“ įvertinimų ir apžvalgų moderavimo įrankį.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698031"
---
# <a name="manage-ratings-and-reviews"></a>Įvertinimų ir atsiliepimų tvarkymas

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip tvarkyti įvertinimus ir apžvalgas naudojant „Microsoft Dynamics 365 Commerce“ įvertinimų ir apžvalgų moderavimo įrankį.

## <a name="overview"></a>Peržiūrėti

„Dynamics 365 Commerce“ naudojama „Microsoft Azure“ pažinimo tarnyba automatiškai moderuoti atsiliepimo tekstą pašalinant keiksmažodžius. Be to, moderatoriai gali naudoti įvertinimų ir apžvalgų moderavimo įrankį šioms neautomatinėms užduotims:

- Moderuokite apžvalgas atsakydami į juos arba juos pašalindami.
- Panaikinkite kliento apžvalgas klientui pateikus dėl to užklausą.
- Visų produktų masinio importo įvertinimų ir apžvalgų duomenys į „Microsoft Power BI“ šabloną, kad įvertinimų ir atsiliepimų tendencijos galėtų būti analizuojamos.

## <a name="read-a-review"></a>Apžvalgos skaitymas 

1. Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.
1. Norėdami filtruotiapžvalgas, kurios rodomos produkto ID, produkto pavadinime arba apžvalgos tekste, naudokite ieškos lauką, esantį viršutiniame dešiniajame puslapio kampe.

Papildomais filtrais galima riboti apžvalgas pagal laikotarpį, vertinimą, kanalą arba su būseną (pašalinta, atsakyta arba pranešta).

![Moderavimo pagrindinis puslapis](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Atsakymas į apžvalgą 

Kartais klientai, kurie pirko produktą, pareiškia savo pasitenkinimą ar nepasitenkinimą, arba nesupranta, kaip naudoti produktą. Kaip moderatorius galite paskelbti atsakymą į apžvalgą. Šis atsakymas rodomas kartu su apžvalga svetainėje. 

Norėdami atsakyti į apžvalgą, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.
1. Suraskite ir pasirinkite apžvalgą, į kurį reikia atsakyti.
1. Dešiniojoje ypatybių srityje pasirinkite **Įtraukti atsakymą**.
1. Įveskite atsakymo tekstą ir pavadinimą, kuris turi būti rodomas atsakytojui. Numatytasis atsakytojo pavadinimas yra **Moderatorius**.
1. Baigę pasirinkite **Skelbti atsakymą**.

![Atsakymas į apžvalgą](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Apžvalgos šalinimas 

Kartais dėl verslo priežasčių moderatoriai turi pašalinti klientų apžvalgas. 

Norėdami pašalinti apžvalgą, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.
1. Suraskite ir pasirinkite apžvalgą, kurią reikia pašalinti.
1. Dešinėje pusėje esančioje ypatybių srityje pasirinkite pašalinimo priežastį ir pasirinkite **Pašalinti**.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Kliento apžvalgų naikinimas klientui pateikus užklausą 

Kartais klientai nori, kad jų įvertinimų ir apžvalgų duomenys būtų visam laikui panaikinti iš el. prekybos svetainės. Moderatorius, gavęs pašalinimo užklausą iš kliento, gali pašalinti kliento duomenis naudodamas apžvalgos naikinimo funkciją. Norint surasti ir panaikinti kliento duomenis, moderatoriui reikia el. pašto adreso, kurį klientas naudojo prisijungdamas ir pateikdamas apžvalgas. 

Norėdami rasti ir panaikinti kliento duomenis, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis \> Apžvalgos \>Naikinti**.
1. Lauke **Ieškoti vartotojų pagal el. pašto adresą** įveskite kliento el. pašto adresą ir pasirinkite **Ieškoti**.
1. Jei klientas atliko apžvalgos veiklų (pavyzdžiui, atsiliepimų teikimas, balsavimai, kiek kito kliento atsiliepimai buvo naudingi, arba komentavimas apie kito kliento atsiliepimą), rezultatai rodomi. Kiekviename elemente yra mygtukas **Naikinti**.
1. Kiekvienam elementui, kurį reikia naikinti, pasirinkite **Naikinti**. Kai būsite paraginti patvirtinti, pasirinkite **Taip**. 
    
![Kliento duomenų naikinimas](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Norint, kad duomenys būtų visiškai pašalinti iš sistemos, tai gali užtrukti iki septynių dienų. Moderatoriai turėtų informuoti klientus apie šį vėlavimą.
> - Jei klientai pakeitė savo pavadinimą savo paskyros parametruose, ieškos rezultatuose gali būti rodomi keli elementai. Šiuo atveju, kad būtų visiškai panaikinti kliento duomenys, moderatorius turi pasirinkti **Naikinti** kiekvienam elementui. 

## <a name="download-ratings-and-reviews-data"></a>Įvertinimų ir apžvalgų duomenų atsisiuntimas

Įvertinimų ir apžvalgų moderavimo įrankiu moderatoriai gali importuoti įvertinimų ir atsiliepimų duomenis masiškai, kad jie galėtų analizuoti tendencijas. Galimas „Power BI“ šablonas, kuriame yra pagrindinė metrika. Moderatoriai gali naudoti šį šabloną masiškai importuotiems duomenims sujungti ir peržiūrėti ataskaitų sritį. Jiems nebūtina sukurti tinkintą ataskaitų sritį. Moderatoriai taip pat gali tinkinti „Power BI“ šabloną, kad patenkintų konkrečius poreikius. 

Norėdami atsisiųsti įvertinimų ir apžvalgų duomenis, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis \>Apžvalgos \> Pranešimas**.
1. Norėdami atsisiųsti įvertinimų ir apžvalgų duomenis kableliais atskirtų reikšmių (CSV) formatu, pasirinkite **Atsisiųsti apžvalgų duomenis**.

## <a name="view-ratings-and-reviews-trends"></a>Įvertinimų ir apžvalgų tendencijų peržiūra

Moderatoriai gali atsisiųsti „Power BI“ šabloną, kad galėtų peržiūrėti tendencijas ataskaitų srityje.

Norėdami peržiūrėti įvertinimų ir apžvalgų tendencijas, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis \>Apžvalgos \> Pranešimas**.
1. Pasirinkite **„PowerBI“ šablonas**, kad atsisiųstumėte šabloną.

    ![„Power BI“ šablono atsisiuntimas](media/rnr-moderation-reports.png) 

1. Atidarykite atsisiųstą šabloną naudojantis „Power BI“ programėle. Uždarykite pasirodžiusį dialogo langą **Prieiga prie interneto turinio** ir uždarykite pasirodžiusį klaidos pranešimą „Atnaujinti“.
1. Eikite į **Pagrindinis**, pasirinkite **Redaguoti užklausas** ir pasirinkite **Duomenų šaltinio parametrai**.
1. Dialogo lange **Duomenų šaltinio parametrai** pasirinkite **Keisti šaltinį**.
1. Lauke **URL** įveskite apžvalgų duomenų, kuriuos atsisiuntėte ankstesne procedūra, maršrutą (pvz., **c:\\apžvalgos\\ReviewsData.csv**).

    ![Kableliais atskirtų reikšmių dialogo lango URL laukas](media/rnr-powerbi-datasource-settings.png) 

1. Pasirinkite **Gerai**, tada – **Taikyti keitimus**. Užtruks nuo vienos iki dviejų minučių, kol jūsų keitimai bus pritaikyti duomenų šaltinyje.
1. Norėdami peržiūrėti įvertinimų ir apžvalgų tendencijas, pasirinkite **Tendencijų lapas**.

    ![Įvertinimų ir apžvalgų tendencijos](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](ratings-reviews-overview.md)

[Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus](opt-in-ratings-reviews.md)

[Įvertinimų ir atsiliepimų konfigūravimas](configure-ratings-reviews.md)

[Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Retail“](sync-product-ratings.md)
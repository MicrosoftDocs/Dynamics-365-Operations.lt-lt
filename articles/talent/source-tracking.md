---
title: Kandidatų išteklių sekimas „Attract“
description: Šioje temoje pateikiama informacija apie kandidatų profilių ir prašymų šaltinio sekimą.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8860f508eebc377042c4e101eeb08a14a737ba0c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461982"
---
# <a name="track-candidate-sources-in-attract"></a>Kandidatų išteklių sekimas „Attract“

[!include [banner](includes/banner.md)]

> [!NOTE] 
> Šioje temoje nurodytomis funkcijomis galima naudotis kaip peržiūros leidimo dalimi. Turinys ir funkcijos gali būti keičiami. Norėdami naudotis šia funkcija, paprašykite administratoriaus, kad įjungtų ją „Attract“ naudodamasis sritimi **Administratoriaus parametrai**. Būsimame leidime bus pateiktos šaltinio sekimo ataskaitos. Daugiau informacijos rasite [Prieiga prie „Talent“ peržiūros funkcijų](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

Kai kandidatai kreipiasi dėl darbo, „Attract“ automatiškai seka jų prašymų šaltinį ir suteikia jums vertingos informacijos, kad galėtumėte tinkamai išnaudoti įdarbinimo veiksmus. Įdarbintojai ir samdos vadovai taip pat gali pasirinkti prašymo šaltinį, kai jie neautomatiškai įtraukia kandidatą į darbų arba talentų telkinį.

Prašymo šaltinį galite peržiūrėti prašymų veiklos informacijos skirtuke **Veiklos**, taip pat – prašymų retrospektyvoje, kuri pateikta talentų telkinių skiltyje **Profilis**. Kandidato profilio šaltinį galite rasti kandidato informacijoje skirtuke **Profilis** tiek prašymų, tiek talentų telkiniuose.

> [!NOTE] 
> Proceso šablonus galite rasti [išsamios įdarbinimo informacijos priede](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).

## <a name="pre-configured-sources"></a>Iš anksto sukonfigūruoti šaltiniai

Numatytajame šaltinių sąraše yra bendri prašymų šaltiniai. Kai kuriems šaltinių tipams, pvz., **Darbo skelbimų lenta** ir **Socialinis tinklas**, priskirta papildoma šaltinio informacija. Pvz., tipas **Socialinis tinklas** apima „Facebook“ ir „Twitter“. Šaltinio tipas **Rekomendacija** suteikia galimybę nurodyti vidinį darbuotoją kaip rekomendavusį asmenį. Numatytajame šaltinių sąraše yra toliau nurodyti iš anksto sukonfigūruoti šaltiniai.

-   „Attract“ karjeros svetainė

-   Agentūra

-   Karjeros mugė

-   Įmonės rinkodara

-   Konferencijos ir prekybos parodos

-   Profesinė asociacija

-   Darbo skelbimų lenta

    -   Iš tikrųjų

    -   Ieškoti

    -   CareerBuilder

    -   „Google“ užduotys

    -   Xing

    -   Glassdoor

    -   „Monster“ užduotys

-   Žurnalai ir publikacijos

-   Socialinis tinklas

    -   „Facebook“

    -   „Twitter“

-   Įdarbinimas universitete

-   „LinkedIn“

-   Suklasifikuota

-   Rekomendacija

-   Įtraukta įdarbintojo

-   Kitas

## <a name="customize-the-source-list"></a>Šaltinių sąrašo tinkinimas 

Galite išplėsti šaltinių sąrašą ir įtraukti papildomų prašymų šaltinių. Norėdami tinkinti šį sąrašą, vykdykite instrukcijas, pateiktas temoje [„Attract“ parinkčių rinkinių išplėtimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract). Redaguokite objektą **TalentSource**, kad įtrauktumėte papildomų šaltinių. 

Norėdami išvengti neigiamos įtakos vartotojo sąsajai (UI), neredaguokite ir nenaikinkite parinkties **TalentCategory** išvardijimo reikšmių (ne pavadinimų), skirtų toliau nurodytiems parametrams.

- **Rekomendacija**
- **„LinkedIn“**
- **Kitas**

Vietoj to galite išplėsti parinkties **TalentSource** išvardijimą, kad įtrauktumėte kitų šaltinių tipų.

---
title: Prognozės, darbo užsakymai ir projektai
description: Šioje temoje aiškinamas prognozių ir darbo užsakymo integravimas su moduliu Projektų valdymas ir apskaita modulyje Turto valdymas.
author: johanhoffmann
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b53dcf4e8796f808283b7bd5ea92b869ee0e59aac5359d74bcdc5de37ea7352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770341"
---
# <a name="forecasts-work-orders-and-projects"></a>Prognozės, darbo užsakymai ir projektai

[!include [banner](../../includes/banner.md)]

 

Modulyje Turto valdymas integracija su moduliu **Projektų valdymas ir apskaita** padeda optimizuoti išlaidų kontrolę, kad vartotojai galėtų sekti priežiūros užduočių tipo prognozių ir darbo užsakymo užduočių išlaidas.

Priežiūros užduočių tipo prognozių sekimui būtina nustatyti du parametrus.

1. Pasirinkite projektą **Turto valdymas** > **Sąranka** > **Turto valdymo parametrai**, o tada kortelėje **Turtas** > FastTab **Projektas**, lauke **Priežiūros prognozės projektas** pasirinkite projektą.

2. Kai sukuriate priežiūros užduoties tipo numatytąją eilutę, automatiškai sukuriamas tos eilutės veiklos numeris puslapyje **Priežiūros užduočių tipų numatytosios reikšmės** (**Turto valdymas** > **Sąranka** > **Užduotys** > **Priežiūros užduočių tipo numatytieji parametrai**).

Priežiūros užduoties tipo prognozės naudojamos dviem tikslams. 

- Galite stebėti priežiūros užduoties tipo prognozių išlaidas modulyje **Projektų valdymas ir apskaita**. 
- Prognozės automatiškai perkeliamos į darbo užsakymo užduoties projektą, kai darbo užsakymo užduotyje pasirenkate priežiūros užduoties tipą.

Norėdami sekti darbo užsakymų užduočių išlaidas, pirma turite nustatyti darbo užsakymų projektus. Daugiau informacijos rasite [Darbo užsakymo projekto sąranka](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Darbo užsakymo užduočių projektai

Kai darbo užsakyme sukuriate darbo užsakymo užduotį, darbo užsakymo projektą apibrėžia darbo užsakymų pirminio projekto sąranka puslapyje **Darbo užsakymo projekto sąranka** (**Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Projekto sąranka**).

Darbo užsakymų užduočių projektai sukuriami naudojant toliau pateikiamų darbo užsakymų duomenų derinį.

- Darbo užsakyme pasirinktas darbo užsakymo tipas 
- Su darbo užsakymo užduotyje esančiu turtu susijusi funkcinė vieta
- Su darbo užsakymo užduotyje esančiu turtu susijęs turto tipas  
- Darbo užsakyme nustatyti numatomi pradžios ir pabaigos laikai  

Kai kurios informacijos darbo užsakyme nėra. Todėl, darbo užsakymo pirminis projektas ieškomas naudojant turimą duomenų derinį ir pasirenkant projekto ID, atitinkantį darbo užsakymo duomenis.

Pavyzdžiui, toliau esančiame pavyzdyje dėl to, kaip nustatytas turto tipas **Sunkvežimio variklis**, kiekviena darbo užsakymo užduotis, sukurta naudojant turto tipą **Sunkvežimio variklis**, bus projekto ID 000186 subprojektas.

![1 iliustracija.](media/01-integration-to-pma.png)

Projekto ID darbo užsakymo užduotyje ir susijusio veiklos numerio paskirtis yra sekti išlaidas, susijusias su darbo užsakymo užduotimi ir pasirinktu turtu modulyje **Projektų valdymas ir apskaita**. (Norėdami peržiūrėti projekto ID ir veiklos numerį, pasirinkite **Turto valdymas** > **Bendras** > **Darbo užsakymai** > **Visi darbo užsakymai** ir pasirinkite darbo užsakymą. „FastTab“ **Eilutės informacija**, lauke **Projekto ID** rodomas projekto ID, o lauke **Veiklos numeris** rodomas veiklos numeris.) Norėdami gauti daugiau informacijos apie turto valdymo išlaidų kontrolę, žr. [Kaštų ir datos kontrolė](../controlling-and-reporting/cost-and-date-control.md).

Toliau pateiktame paveikslėlyje matote grafinę darbo užsakymų projektų ir susijusių projektų veiklų apžvalgą.

![2 iliustracija.](media/02-integration-to-pma.png)

Kai darbo užsakyme sukuriama nauja darbo užsakymo užduotis, automatiškai sukuriamas šios užduoties darbo užsakymo projektas. Su darbo užsakymo užduotimi susijusio turto finansinės dimensijos automatiškai perkeliamos į darbo užsakymo užduoties projektą.

Projekto veiklos, sukurtos darbo užsakymo užduočiai, turi susietos informacijos. Tai informacija apie priežiūros užduoties tipą, priežiūros užduoties tipo variantą ir prekybą. Ji naudinga jei, pavyzdžiui, kuriate darbo užsakymo pirkimo užsakymą (žr. skyrių [Įsigijimas](../work-orders/procurement.md)) arba jei naudojate modulį **Projektų valdymas ir apskaita** laikui registruoti.

Jei turtas buvo įdiegtas funkcinėje vietoje, bet vėliau įdiegtas kitoje funkcinėje vietoje, turto finansinės dimensijos, susijusios su nauja funkcine vieta, automatiškai atnaujinamos. Tada, kai sukuriate turto darbo užsakymo užduotį, į darbo užsakymo užduoties darbo užsakymo projektą automatiškai perkeliamos finansinės dimensijos, kurios dabar yra susijusios su turtu. Todėl, kai naudojate funkcines vietas, išlaidas visada galima sekti funkcinėse vietose, kuriose turtas buvo įdiegtas bet kuriuo laikotarpiu. Automatinis finansinių dimensijų naujinimas padeda užtikrinti visišką išlaidų atsekamumą kontroliuojant projektus ir rengiant ataskaitas.

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Darbo užsakymų projektai, darbo užsakymų ciklo būsenos, projekto etapai ir projektų tipai

Siekiant užtikrinti, kad darbo užsakymų ciklo būsenos ir susijusių projektų etapai darbo užsakymuose būtų naudojami tinkamai, išnagrinėkite priklausomybes, susijusias su moduliu **Projektų valdymas ir apskaita**.

- Dirbant su moduliu **Projektų valdymas ir apskaita**, puslapyje **Projektų valdymo ir apskaitos parametrai** nustatomi projektų tipų projektų etapai.  
- Puslapyje **Projektų valdymo ir apskaitos parametrai** pasirinkite atitinkamų projektų etapų žymės langelius visuose projektų tipuose, kuriuos naudosite. Toliau esančiuose paveikslėliuose penki etapai (**Sukurta**, **Numatoma**, **Suplanuota**, **Vykdoma** ir **Baigta**) buvo parinkti projektų tipams **Laikas ir medžiaga** bei **Vidinis**. Šie penki etapai yra susiję ir su vidinės priežiūros užduotimis ir su aptarnavimo priežiūros užduotimis.
- Modulyje **Turto valdymas** projektų tipai nurodomi pagal projektų grupes, kurias nurodėte puslapyje **Darbo užsakymo projekto sąranka** > kortelėje **Projektų grupė** (**Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Projekto sąranka**).  
- Projektų grupės, nustatytos puslapyje **Darbo užsakymų projektų sąranka**, naudojamos kuriant darbo užsakymus. Kai sukuriamas naujas darbo užsakymas, automatiškai sukuriamas darbo užsakymo darbo.  
- Kiekviena darbo užsakymo ciklo būsena turi būti susijusi su projekto etapu.  
- Projekto etapas, susijęs su darbo užsakymo ciklo būsena, turi būti apibrėžtas kaip projektų grupės, apibrėžtos darbo užsakymo projekte, aktyvusis etapas. Automatiškai sukuriamas darbo užsakymo projektas.
- Kai sukuriate naują darbo užsakymą, darbo užsakymo projektas automatiškai priskiriamas pagal sąranką puslapyje **Darbo užsakymų projektų sąranka**.  

Toliau esančiuose paveikslėliuose pavaizduotos sąsajos tarp darbo užsakymų projektų grupių, susijusių projektų tipų, projektų etapų ir darbo užsakymų ciklų būsenų.

![3 iliustracija.](media/03-integration-to-pma.png)

![4 iliustracija.](media/04-integration-to-pma.png)

![5 iliustracija.](media/05-integration-to-pma.png)

Norėdami gauti informacijos apie tai, kaip nustatyti darbo užsakymų projektus, žr. [Darbo užsakymo projekto sąranka](../setup-for-work-orders/work-order-project-setup.md). Daugiau informacijos apie darbo užsakymo ciklo būsenų kūrimą žr. [Darbo užsakymo ciklo būsenos](../setup-for-work-orders/work-order-lifecycle-states.md).

Toliau esančiame paveikslėlyje pavaizduoti įvairūs projektai, sukurti modulyje **Turto valdymas** ir leidžiant integraciją su moduliu **Projektų valdymas ir apskaita**. Be to, čia pavaizduoti su projektais susiję darbo procesai.

![6 iliustracija.](media/06-integration-to-pma.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
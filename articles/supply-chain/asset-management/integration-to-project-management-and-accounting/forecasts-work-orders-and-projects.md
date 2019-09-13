---
title: Prognozės, darbo užsakymai ir projektai
description: Šioje temoje aiškinamas prognozių ir darbo užsakymo integravimas su moduliu Projektų valdymas ir apskaita modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886821"
---
# <a name="forecasts-work-orders-and-projects"></a>Prognozės, darbo užsakymai ir projektai

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Modulyje Turto valdymas integruojama su moduliu **Projektų valdymas ir apskaita** siekiant optimizuoti išlaidų kontrolę, kad vartotojai galėtų sekti priežiūros užduočių tipo prognozių ir darbo užsakymo užduočių išlaidas.

Norint sekti priežiūros užduočių tipo prognozes, būtina nustatyti toliau pateikiamus parametrus.

1. Pasirinkite projektą modulyje **Turto valdymas** > **Sąranka** > **Turto valdymo parametrai** > spustelėję nuorodą **Turtas** > FastTab **Projektas** > lauke **Priežiūros prognozės projektas**.

2. Kai dalyje **Priežiūros užduočių tipų numatytosios reikšmės** sukuriate priežiūros užduoties tipo numatytąją eilutę, automatiškai sukuriamas tos eilutės veiklos numeris (**Turto valdymas** > **Sąranką** > **Užduotys** > **Priežiūros užduočių tipo numatytieji parametrai**).

Yra dvi priežiūros užduočių tipo prognozių paskirtys: modulyje **Projektų valdymas ir apskaita** galite sekti priežiūros užduočių tipo prognozių išlaidas. Be to, prognozės automatiškai perkeliamos į darbo užsakymo užduoties projektą, kai pasirenkate darbo užsakymo užduotyje pasirenkate priežiūros užduoties tipą.

Norėdami sekti darbo užsakymų užduočių išlaidas, pirma turite nustatyti darbo užsakymų projektus.  Žr. skyrių [Darbo užsakymų projektų sąranka](../setup-for-work-orders/work-order-project-setup.md), kuriame aprašoma procedūra.

## <a name="work-order-job-projects"></a>Darbo užsakymo užduočių projektai

Kai darbo užsakyme sukuriate darbo užsakymo užduotį, darbo užsakymo projektą nulemia darbo užsakymų pirminio projekto sąranka, pasiekiama pasirinkus **Turto valdymas** > **Sąranką** > **Darbo užsakymai** > **Projekto sąranka**.

Darbo užsakymų užduočių projektai sukuriami naudojant toliau pateikiamų darbo užsakymų duomenų derinį.

- Darbo užsakyme pasirinktas darbo užsakymo tipas 
- Su darbo užsakymo užduotyje esančiu turtu susijusi funkcinė vieta
- Su darbo užsakymo užduotyje esančiu turtu susijęs turto tipas  
- Darbo užsakyme nustatytas numatomas pradžios ir pabaigos laikas  

Gali būti, kad darbo užsakyme bus pateikta ne visa pirmiau minėta informacija. Todėl, darbo užsakymo pirminis projektas ieškomas naudojant turimą duomenų derinį ir pasirenkant projekto ID, atitinkantį darbo užsakymo duomenis.

Pavyzdys. Toliau pateiktame paveikslėlyje turto tipo Sunkvežimio variklis sąranką reiškia, kad kiekviena sukuriama šio turto tipo darbo užsakymo užduotis bus projekto ID 000186 dalis.

![1 pav.](media/01-integration-to-pma.png)

Darbo užsakymo užduotyje pateikiamo projekto ID ir susijusio veiklos numerio (**Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Visi darbo užsakymai** > sąraše pasirinkite darbo užsakymą > FastTab **Eilutės informacija** > laukas **Projekto ID** ir laukas **Veiklos numeris**) paskirtis yra stebėti išlaidas, susijusias su darbo užsakymo užduotimi, ir turtą, pasirinktą darbo užsakymo užduotyje modulyje **Projektų valdymas ir apskaita**. 

Toliau pateiktame paveikslėlyje matote grafinę darbo užsakymų projektų ir susijusių projektų veiklų apžvalgą.

![2 paveikslėlis](media/02-integration-to-pma.png)

Kai darbo užsakyme sukuriama nauja darbo užsakymo užduotis, automatiškai sukuriamas šios užduoties darbo užsakymo projektas. Su darbo užsakymo užduotimi susijusio turto finansinės dimensijos automatiškai perkeliamos į darbo užsakymo užduoties projektą. Prie darbo užsakymo užduočiai sukurtos projekto veiklos pridedama susijusi informacija dėl priežiūros užduoties tipo, priežiūros užduoties tipo varianto ir pardavimo. Šie duomenys naudingi jei, pavyzdžiui, kuriate darbo užsakymo pirkimo užsakymą (žr. skyrių [Įsigijimas](../work-orders/procurement.md)) arba jei naudojate modulį **Projektų valdymas ir apskaita** laikui registruoti.  

Jei turtas buvo įdiegtas funkcinėje vietoje ir vėliau įdiegtas kitoje funkcinėje vietoje, turto finansinės dimensijos, susijusios su nauja funkcine vieta, automatiškai atnaujinamos. Vėliau, kai sukuriate turto darbo užsakymo užduotį, į darbo užsakymo užduoties darbo užsakymo projektą automatiškai perkeliamos finansinės dimensijos, kurios dabar yra susijusios su turtu. Tai reiškia, kad kai naudojate funkcines vietas, išlaidas visada galima sekti funkcinėse vietose, kuriose turtas buvo tam tikru laikotarpiu įdiegtas. Dėl automatiškai naujinamų finansinių dimensijų užtikrinamas visiškas išlaidų atsekamumas kontroliuojant projektus ir rengiant projektų ataskaitas.  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Darbo užsakymų projektai, darbo užsakymų ciklo būsenos, projekto etapai ir projektų tipai

Siekiant užtikrinti, kad darbo užsakymų ciklo būsenos ir susijusių projektų etapai darbo užsakymuose naudojami tinkamai, išnagrinėkite priklausomybes, susijusias su moduliu **Projektų valdymas ir apskaita**.

- Modulio **Projektų valdymas ir apskaita** dalyje **Projektų valdymo ir apskaitos parametrai** nustatomi projektų tipų projektų etapai.  
- Dalyje **Projektų valdymo ir apskaitos parametrai** būtinai pasirinkite atitinkamų projektų etapų žymės langelius visuose projektų tipuose, kuriuos ketinate naudoti. Toliau pateiktame paveikslėlyje pasirinkti penki projektų tipų Laikas ir medžiagos ir Vidinis etapai: **Sukurta** - **Numatoma** - **Suplanuotas** - **Vykdoma** - **Baigta**. Šie penki etapai yra susiję ir su vidine priežiūra, ir su aptarnavimo techninės priežiūros užduotimis.  
- Modulyje **Turto valdymas** projektų tipai nustatomi pagal projektų grupes, kurias nustatėte formoje **Darbo užsakymų projektų sąranka** > spustelėję nuorodą **Projektų grupė**.  
- Projektų grupės, nustatytos formoje **Darbo užsakymų projektų sąranka**, naudojamos kuriant darbo užsakymus. Kai sukuriamas naujas darbo užsakymas, automatiškai sukuriamas darbo užsakymo darbo.  
- Kiekviena darbo užsakymo ciklo būsena turi būti susijusi su projekto etapu.  
- Projekto etapas, susijęs su darbo užsakymo ciklo būsena, turi būti apibrėžtas kaip projektų grupės, apibrėžtos darbo užsakymo projekte, aktyvusis etapas. Automatiškai sukuriamas darbo užsakymo projektas.  
- Kai sukuriate naują darbo užsakymą, darbo užsakymo projektas automatiškai priskiriamas pagal sąranką formoje **Darbo užsakymų projektų sąranka** (**Turto valdymas** > **Sąranką** > **Darbo užsakymai** > **Projekto sąranka**).  

Sąsajos tarp darbo užsakymų projektų grupių, susijusių projektų tipų, projektų etapų ir darbo užsakymų ciklų būsenų pavaizduotos toliau pateikiamuose paveikslėliuose.  

![3 paveikslėlis](media/03-integration-to-pma.png)

![4 paveikslėlis](media/04-integration-to-pma.png)

![5 paveikslėlis](media/05-integration-to-pma.png)

Žr. skyrių [Darbo užsakymų projektų sąranka](../setup-for-work-orders/work-order-project-setup.md), norėdami sužinoti, kaip nustatyti darbo užsakymų projektus, ir skyrių [Darbo užsakymų ciklo būsenos](../setup-for-work-orders/work-order-lifecycle-states.md), norėdami sužinoti, kaip kurti darbo užsakymų ciklo būsenas.

Toliau pateikiamame paveikslėlyje pavaizduota grafinė įvairių projektų, kuriamų modulyje **Turto valdymas**, norint integruoti su moduliu **Projektų valdymas ir apskaita**, ir darbo procesų, su kuriais minėti projektai yra susiję, apžvalga.

![6 paveikslėlis](media/06-integration-to-pma.png)


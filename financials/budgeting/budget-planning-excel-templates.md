---
title: "Biudžeto planavimo Excel šablonai"
description: "Šioje temoje aprašoma, kaip sukurti Microsoft Excel šablonų, kurie gali būti naudojami su biudžeto planus."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Biudžeto planavimo Excel šablonai

Šioje temoje aprašoma, kaip sukurti Microsoft Excel šablonų, kurie gali būti naudojami su biudžeto planus.

Ši tema parodo, kaip sukurti "Excel" šablonų, kuris bus naudojamas su biudžeto planus naudojant standartinę Parodomoji versija duomenų rinkinys ir administratoriaus vartotojo prisijungimas. Daugiau informacijos apie biudžeto planavimą, rasite [biudžeto planavimo apžvalga.](budget-planning-overview-configuration.md) Jūs taip pat galite sekti ir [biudžeto planavimo 101](budget-plan.md) pamoka išmokti pagrindinio modulio konfigūravimo ir naudojimo principus.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Sukurti darbalapio naudojantis biudžeto planą dokumento maketą
Biudžeto plano dokumentus galima peržiūrėti ir redaguoti naudojant vieną arba daugiau maketų. Kiekvienas maketas gali turėti susijęs biudžeto planą dokumento šabloną, peržiūrėti ir redaguoti biudžeto plano duomenis į "Excel" darbalapį. Šioje temoje, biudžeto planą dokumento šablonas bus sugeneruotas naudojant esamo išdėstymo konfigūracijos. Atviros, **biudžeto planų sąrašą** (**sudaromo biudžeto**&gt;**biudžeto planų**). Spustelėkite **naujas** sukurti naują biudžeto plano dokumentą. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Naudoti su **pridėti** linijos parinktis pridėti eilutes. Spustelėkite **maketai** peržiūrėti biudžeto plano dokumentų išdėstymo konfigūracijos. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Galite peržiūrėti išdėstymo konfigūracijos ir reguliuoti, kiek reikia. Eikite į **šabloną**&gt;**sukurti** sukurti "Excel" failą, šiame makete. Po to, kai sukuriamas šablonas, eikite į **šabloną**&gt;**Peržiūrėti** atidaryti ir peržiūrėti biudžeto planą dokumento šabloną. Galite įrašyti "Excel" failą į vietinį diską. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Biudžeto plano dokumento maketą negalima redaguoti, po to, kai "Excel" šablonas yra susijęs su juo. Keisti maketą, trinti susietas "Excel" šablono failą ir atkurti jį. Tai yra būtina siekiant išlaikyti laukų išdėstymą ir darbalapio sinchronizuoti. 

"Excel" šablonas, bus pateikti visi elementų iš biudžeto planą dokumento maketą, kai į **Laisvas darbalapyje** skiltyje yra nustatyta kaip teisinga. Persidengiančių elementų negalima vestis į "Excel" šablonas. Pavyzdžiui, jei makete yra prašymą Q1, prašymą Q2, prašymą Q3, ir prašymą Q4 stulpelius ir bendrą prašymą stulpelį, kuriame yra visi 4 ketvirčio stulpelių suma, tik ketvirčio stulpelius ar viso stulpelio yra galima naudoti "Excel" šablonas. "Excel" failą negalima atnaujinti persidengiančių stulpelių atnaujinimo metu, nes duomenų lentelėje gali tapti pasenusi ir netiksli.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Norėdami išvengti galimų problemų su peržiūros ir redagavimo biudžeto plano duomenis programa "Excel", tas pats vartotojas turėtų prisijungti tiek Dynamics 365 operacijoms ir duomenų jungties Microsoft Dynamics Office papildinys.

## <a name="add-a-header-to-budget-plan-document-template"></a>Įtraukti antraštę biudžeto plano dokumento šablonas
Jei norite pridėti antraštę informacijos, pažymėkite viršutinę eilutę "Excel" failą ir įterpti tuščių eilučių. Spustelėkite **dizaino**, kad **duomenų jungtį** antraštės laukus įtraukti į "Excel" failą.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

– Į **dizaino** grupėje ** ** spustelėkite **pridėti** laukus, o tada pasirinkite **BudgetPlanHeader** kaip subjekto duomenų šaltinis.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Žymeklį į norimą vietą, "Excel" failą. Spustelėkite **pridėti etiketės** įtraukti lauko žymė į pasirinktą vietą. Pasirinkite **pridėti reikšmę** įtraukti lauką vertė į pasirinktą vietą. Spustelėkite **padaryti**, uždarykite dizaino įrankį.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Įtraukti apskaičiuojamąjį stulpelį į biudžeto planą dokumento šablono lentelė
--------------------------------------------------------------

Kitą, apskaičiuoti stulpeliai įtraukiami sugeneruoto biudžeto planą dokumento šabloną. A **bendras prašymas** stulpelį, kuris apibendrina prašymą Q1: prašymą Q4 stulpelius, ir **koregavimo** kolona, perskaičiuoja į **bendrą prašymą** skiltyje iš anksto veiksnys.

Spustelėkite **dizaino**, kad **duomenų jungtį** įtraukti stulpelių lentelę. Spustelėkite **redaguoti** prie **BudgetPlanWorksheet** duomenų šaltinį, kad pradėti įtraukti stulpelius.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Pasirinktų laukų grupės rodomos stulpelius, kuriuos galima rasti šabloną. Spustelėkite **formulės** pridėti naują stulpelį. Pavadinkite naują stulpelį ir tada įklijuojate formulę į į **formulės** srityje. Spustelėkite **naujinimas** Įterpti stulpelį.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Nustatyti pagal formulę, sukurti formulę skaičiuoklėje ir nukopijuokite jį į **dizaino** lango. Dynamics 365 operacijų Susietosios lentelės bus paprastai vadinamas "AXTable1". Pvz., Apibendrinant prašyti Q1: prašyti Q4 stulpelių skaičiuoklėje, formulė = AxTable1\[prašyti Q1\]+ AxTable1\[Q2 prašyti\]+ AxTable1\[prašyti Q3\]+ AxTable1\[prašyti Q4\].

Pakartokite šiuos veiksmus, Norėdami įterpti į **koregavimo** stulpelio. Naudoti formulę = AxTable1\[iš viso prašymas\]\*$I$ 1 už šiame stulpelyje. Tai nuves reikšmė langelyje I1 ir reikšmes padauginkite ir **iš viso prašymas** stulpelyje suskaičiuoti koregavimo.

Įrašyti ir uždaryti "Excel" failą. Grįžti į Dynamics 365 operacijoms, ir į **maketai**, spustelėkite **šabloną &gt;įkelti** įkelti įrašytą "Excel" šablonas, naudotinas biudžeto planas. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Glaudžiai su **maketai** slankiklį. Į **biudžeto planą** dokumento, spustelėkite **darbalapio** peržiūrėti ir redaguoti dokumentą programoje "Excel". Atkreipkite dėmesį, kad pakoreguotas "Excel" šablonas buvo naudojamas sukurti šį biudžeto planą darbalapį ir apskaičiuojamieji stulpeliai atnaujinami naudojant formules, kuri buvo nurodyta ankstesnius veiksmus. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Patarimai ir gudrybės, kaip kurti biudžeto planą šablonai
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Galite pridėti ir papildomų duomenų šaltiniais biudžeto plano šabloną?

Taip, galite naudoti su **dizaino** meniu, jei norite pridėti papildomų subjektai į tą patį arba kituose lapuose "Excel" šablonas. Pvz., galite įtraukti į **BudgetPlanProposedProject** duomenų šaltinio sukurti ir išlaikyti siūlomų projektų sąrašą tuo pačiu metu, kada darbo su biudžeto plano duomenis programoje "Excel". Atkreipkite dėmesį, kad įskaitant didelės apimties duomenų šaltiniai gali paveikti našumą "Excel" darbaknygės. 

Galite naudoti su **filtras** variantas, **duomenų jungtį** pridėti norimus filtrus papildomų duomenų šaltinių.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Paslėpti projekto variantas, pagrįstas duomenų jungtis kitiems vartotojams?

Taip, atidaryti ir **duomenų jungtį** parinktis Norėdami paslėpti į **dizaino** parinktis iš kitų vartotojų.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Plėsti **duomenų jungties galimybes** ir aišku, **įgalinti dizainas** žymės langelį. Tai bus paslėpti į **dizaino** iš to **duomenų jungtį**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Neleisti vartotojams netyčia uždaryti duomenų jungties dirbant su duomenimis?

Mes rekomenduojame užrakinimo šablono, apsaugoti vartotojus nuo uždaryti. Norėdami įjungti užrakinti, kad **duomenų jungtį**, viršutiniame dešiniajame kampe atsiranda rodyklė. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Spustelėkite rodyklę, esančią už papildomą meniu. Pasirinkite **spyna**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Galite naudoti kitus Excel funkcijos, pavyzdžiui, langelio formatavimą, spalvas, sąlyginis formatavimas ir diagramas su savo biudžeto planą šablonų?

Taip, dauguma standartas "Excel" galimybės dirbti biudžeto planą šablonai. Mes rekomenduojame naudoti kodavimas spalvomis vartotojams atskirti tik skaityti ir redaguoti stulpelius. Sąlyginį formatavimą galima išryškinti problemiškas sritis, biudžeto. Stulpelių sumų lengvai gali būti pateikiami naudojant standartinę "Excel" formulių virš lentelės.

Taip pat galite sukurti ir naudoti suvestinės lentelės ir diagramos papildomų grupių ir biudžeto duomenų vizualizacijas. Dėl į **duomenų** skirtuke, be, **ryšiai** grupės, spustelėkite **viską atnaujinti**, ir tada spustelėkite **ryšio ypatybės**. Spustelėkite į **naudojimo** tab. Pagal **atnaujinti**, pasirinkite į **atidarant failą atnaujinti duomenis** žymės langelį. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)



---
title: Biudžeto planavimo šablonai, skirti „Excel‟
description: Šiame straipsnyje aprašoma, kaip kurti šablonus Microsoft Excel, kuriuos galima naudoti su biudžeto planais.
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: kfend
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8996ad5d03327b9273be7860a3905dc25efa7e90
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070671"
---
# <a name="budget-planning-templates-for-excel"></a>Biudžeto planavimo šablonai, skirti „Excel‟

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip kurti šablonus Microsoft Excel, kuriuos galima naudoti su biudžeto planais.

Šiame straipsnyje aprašoma, kaip sukurti "Excel" šablonus, kurie bus naudojami su biudžeto planais naudojant standartinį demonstracinių duomenų rinkinį ir administratoriaus vartotojo prisijungimą. Daugiau informacijos apie biudžeto planavimą rasite [Biudžeto planavimo apžvalga.](budget-planning-overview-configuration.md). Taip pat galite vadovautis mokymo programa [Biudžeto planavimas](budget-plan.md), kad sužinotumėte pagrindinius modulio konfigūracijos ir naudojimo principus.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Darbalalapio generavimas naudojant biudžeto plano dokumento maketą

Biudžeto plano dokumentus galime peržiūrėti ir redaguoti naudojant vieną arba daugiau maketų. Kiekvienam maketui galima priskirti biudžeto plano dokumento šabloną, kad būtų galima peržiūrėti ir redaguoti biudžeto plano duomenis „Excel“ darbalapyje. Šiame straipsnyje, biudžeto plano dokumento šablonas bus sugeneruotas naudojant esamą maketo konfigūraciją. 

1. Atidarykite **Biudžeto planų sąrašas** (**Biudžeto sudarymas** &gt; **Biudžeto planai**). 
2. Spustelėkite **Naujas**, kad sukurtumėte naują biudžeto plano dokumentą. 

   [![Biudžeto planų sąrašas.](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. Naudokite eilutės parinktį **Įtraukti**, kad įtrauktumėte eilučių. Spustelėkite **Maketai**, kad peržiūrėtumėte biudžeto plano dokumento maketo konfigūraciją. 

   [![Biudžeto planų įtraukimas.](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Maketo konfigūraciją galite peržiūrėti ir pagal poreikį koreguoti. 
1. Atidarykite **Šablonas** &gt; **Generuoti**, kad sukurtumėte šio maketo „Excel“ failą. 
2. Sugeneravę šabloną pasirinkite **Šablonas** &gt; **Peržiūrėti**, kad atidarytumėte ir peržiūrėtumėte biudžeto plano dokumento šabloną. „Excel“ failą galite įrašyti į vietinį diską. 

[![Įrašyti kaip.](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> Biudžeto plano dokumento maketo redaguoti negalima, kai jis susietas su „Excel“ šablonu. Norėdami redaguoti maketą, panaikinkite susietą „Excel“ šablono failą ir sugeneruokite jį iš naujo. Tai būtina, kad maketo ir darbalapio laukai būtų sinchronizuoti. 

„Excel“ šablone bus pateikti visi biudžeto plano dokumento maketo elementai, kurių stulpelis **Pasiekiama darbalapyje** nustatytas į True. Persidengiančių elementų „Excel“ šablone pateikti negalima. Pvz., jei makete yra stulpeliai Užklausa per 1 ketvirtį, Užklausa per 2 ketvirtį, Užklausa per 3 ketvirtį ir Užklausa per 4 ketvirtį bei visų užklausų stulpelis, kuris nurodo visų 4 ketvirčių stulpelių sumą, „Excel“ šablone galima naudoti tik ketvirčių stulpelius arba visų užklausų stulpelį. Naujinimo metu „Excel“ failas negali atnaujinti persidengiančių stulpelių, nes lentelės duomenys gali tapti pasenę ir netikslūs.

> [!NOTE] 
> Norint išvengti galimų problemų peržiūrint ir redaguojant biudžeto plano duomenis naudojant "Excel", Microsoft Dynamics tą patį vartotoją reikia prisijungti ir prie "365 Microsoft Dynamics " finansų ir "Office" priedo duomenų jungties.

## <a name="add-a-header-to-budget-plan-document-template"></a>Antraštės įtraukimas į biudžeto plano dokumento šabloną
Norėdami įtraukti antraštės informaciją, pasirinkite viršutinę „Excel“ failo eilutę ir įterpkite tuščių eilučių. Dalyje **Duomenų jungtis** spustelėkite **Dizainas**, kad į „Excel“ failą įtrauktumėte antraštės laukų.

Skirtuke **Dizainas** spustelėkite **Įtraukti** ir tada **BudgetPlanHeader** pasirinkite kaip objekto duomenų šaltinį.

Nuveskite žymeklį į norimą vietą „Excel“ faile. Spustelėkite **Įtraukti žymą**, kad į pasirinktą vietą įtrauktumėte lauko žymą. Pasirinkite **Įtraukti vertę**, kad į pasirinktą vietą įtrauktumėte vertės lauką. Spustelėkite **Atlikta**, kad uždarytumėte dizaino įrankį.

## <a name="select-add-valuemediabpt7png"></a>[![Pasirinkti „Įtraukti vertę“.](./media/bpt7.png)](./media/bpt7.png)

## <a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Apskaičiuoto stulpelio įtraukimas į biudžeto plano dokumento šablono lentelę

Tada apskaičiuoti stulpeliai įtraukiami į sugeneruotą biudžeto plano dokumento šabloną. Stulpelis **Bendra užklausų suma**, kuriame pateikiama paraiškų už 1–4 ketvirčių stulpelių suma, ir stulpelis **Koregavimas**, kuriame stulpelio **Bendra užklausų suma** vertė perskaičiuojama naudojant iš anksto nustatytą koeficientą.

Dalyje **Duomenų jungtis** spustelėkite **Dizainas**, kad į lentelę įtrauktumėte stulpelių. Šalia duomenų šaltinio **BudgetPlanWorksheet** spustelėkite **Redaguoti**, kad pradėtumėte įkelti stulpelius.

[![Pradėti stulpelių įtraukimą.](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Pasirinktoje laukų grupėje rodomi stulpeliai, pateikiami šablone. Spustelėkite **Formulė**, kad įtrauktumėte naują stulpelį. Pavadinkite naują stulpelį ir tada įklijuokite formulę lauke **Formulė**. Spustelėkite **Naujinti**, kad įterptumėte stulpelį.

[![Pridėti ir įterpti stulpelį.](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Norėdami apibrėžti formulę, sukurkite formulę skaičiuoklėje ir tada nukopijuokite ją į langą **Dizainas**. Finansų ir operacijų apribota lentelė paprastai bus pavadinta "AXTable1". Pvz., norėdami susumuoti paraiškų už 1–4 ketvirčių stulpelius skaičiuoklėje, sukurkite tokią formulę: AxTable1\[Paraiška už 1 ketvirtį\] + AxTable1\[Paraiška už 2 ketvirtį\] + AxTable1\[Paraiška už 3 ketvirtį\] + AxTable1\[Paraiška už 4 ketvirtį\].

Pakartokite šiuos veiksmus ir įterpkite stulpelį **Koregavimas**. Šiam stulpeliui priskirkite formulę: AxTable1\[Bendra užklausų suma\]\*$I$1 Tokiu būdu langelio I1 vertė bus padauginta iš stulpelio **Bendra užklausų suma** verčių, kad būtų apskaičiuotos koregavimo sumos.

Įrašykite ir uždarykite „Excel“ failą. Dalyje **Maketai** spustelėkite **Šablonas &gt; Naujinti**, kad įkeltumėte įrašytą „Excel“ šabloną naudoti biudžeto plane. 

[![Nusiųsti „Excel“ šabloną.](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Uždarykite slankiklį **Maketai**. Dokumente **Biudžeto planas** spustelėkite **Darbalapis**, kad dokumentą peržiūrėtumėte ir redaguotumėte programoje „Excel“. Atkreipkite dėmesį, kad pakoreguotas „Excel“ šablonas buvo naudojamas šiam biudžeto plano darbalapiui sukurti, o apskaičiuoti stulpeliai atnaujinti naudojant formules, kurios buvo apibrėžtos ankstesniuose veiksmuose. 

[![Peržiūrėti ir redaguoti dokumentą programoje „Excel“.](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Biudžeto plano šablonų kūrimo patarimai
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Ar galiu į biudžeto plano šabloną įtraukti ir naudoti papildomus duomenų šaltinius?

Taip, galite naudoti meniu **Dizainas**, kad į tą patį ar kitus „Excel“ šablono lapus įtrauktumėte papildomų objektų. Pvz., galite įtraukti duomenų šaltinį **BudgetPlanProposedProject**, kad sukurtumėte ir tvarkytumėte siūlomų projektų sąrašą tuo pačiu metu, kai dirbate su biudžeto plano duomenimis programoje „Excel“. Atkreipkite dėmesį, kad įtraukiant didelės apimties duomenų šaltinius gali būti paveiktas „Excel“ darbaknygės veikimas. 

Galite naudoti dalyje **Duomenų jungtis** pateiktą parinktį **Filtras**, kad į papildomus duomenų šaltinius įtrauktumėte norimų filtrų.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Ar galiu nuo kitų vartotojų paslėpti duomenų jungties parinktį Dizainas?

Taip, atidarykite dalies **Duomenų jungiklis** parinktis, kad paslėptumėte parinktį **Dizainas** nuo kitų vartotojų.

[![Atidaryti duomenų jungties parinktis.](./media/bpt13-1024x565.png)](./media/bpt13.png)

Išplėskite dalies **Duomenų jungtis** parinktis ir atžymėkite žymės langelį **Įjungti dizainą**. Tokiu būdu paslėpsite dalies **Duomenų jungtis** parinktį **Dizainas**.

[![Slėpti dizaino pasirinktį iš duomenų jungties.](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Ar galiu užtikrinti, kad vartotojai, dirbdami su duomenimis, atsitiktinai neuždarytų duomenų jungties?

Rekomenduojame užrakinti šabloną, kad vartotojai jos atsitiktinai neišjungtų. Norėdami įjungti užraktą, spustelėkite **Duomenų jungtis**, viršutiniame kairiajame kampe pasirodo rodyklė. 

[![Įjungti užraktą.](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Spustelėkite rodyklę, kad būtų parodytas papildomas meniu. Pasirinkite **Užrakinti**.

### <a name="select-lockmediabpt16png"></a>[![Pasirinkti užraktą.](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Ar galiu biudžeto plano šablonuose naudoti kitas „Excel“ funkcijas, pvz., langelių formatavimą, spalvas, sąlyginį formatavimą ir diagramas?

Taip, biudžeto plano šablonuose veiks dauguma standartinių „Excel“ funkcijų. Rekomenduojame naudoti kodavimo spalvomis funkciją, kad vartotojai galėtų lengviau atskirti tik skaitomus ir redaguojamus stulpelius. Sąlyginio formatavimo funkciją galima naudoti norint paryškinti problematiškas biudžeto sritis. Bendras stulpelių sumas galima lengvai pateikti naudojant „Excel“ formules virš lentelės.

Taip pat galite kurti ir naudoti suvestinės lenteles bei diagramas, norėdami atlikti papildomų biudžeto duomenų grupavimo ir vizualizavimo veiksmų. Skirtuko **Duomenys** grupėje **Ryšiai** spustelėkite **Atnaujinti viską**, o tada spustelėkite **Ryšių ypatybės**. Spustelėkite skirtuką **Naudojimas**. Dalyje **Naujinti** pažymėkite žymės langelį **Naujinti duomenis atidarant failą**. 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]


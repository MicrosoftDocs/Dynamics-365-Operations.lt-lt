---
title: "Biudžeto planavimo „Excel“ šablonai"
description: "Šioje temoje aprašoma, kaip kurti „Microsoft Excel“ šablonus, kuriuos galima naudoti biudžeto planuose."
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 156688b705337331e083ebc19fded57b028acb67
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="budget-planning-templates-for-excel"></a>Biudžeto planavimo „Excel“ šablonai

[!include[banner](../includes/banner.md)]


Šioje temoje aprašoma, kaip kurti „Microsoft Excel“ šablonus, kuriuos galima naudoti biudžeto planuose.

Šioje temoje parodoma, kaip kurti biudžeto planuose naudojamus „Excel“ šablonus, naudojant standartinį demonstracinių duomenų rinkinį ir administratoriaus vartotojo prisijungimo informaciją. Daugiau informacijos apie biudžeto planavimą žr. [Biudžeto planavimo apžvalga.](budget-planning-overview-configuration.md) Taip galite vadovautis mokymo programa [Biudžeto planavimo 101](budget-plan.md), kad sužinotumėte pagrindinius modulio konfigūracijos ir naudojimo principus.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Darbalalapio generavimas naudojant biudžeto plano dokumento maketą

Biudžeto plano dokumentus galime peržiūrėti ir redaguoti naudojant vieną arba daugiau maketų. Kiekvienam maketui galima priskirti biudžeto plano dokumento šabloną, kad būtų galima peržiūrėti ir redaguoti biudžeto plano duomenis „Excel“ darbalapyje. Šioje temoje biudžeto plano dokumento šablonas bus sugeneruotas naudojant esamo maketo konfigūraciją. 

1. Atidarykite **Biudžeto planų sąrašas** (**Biudžeto sudarymas** &gt; **Biudžeto planai**). 
2. Spustelėkite **Naujas**, kad sukurtumėte naują biudžeto plano dokumentą. 

  [![Biudžeto planų sąrašas](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. Naudokite eilutės parinktį **Įtraukti**, kad įtrauktumėte eilučių. Spustelėkite **Maketai**, kad peržiūrėtumėte biudžeto plano dokumento maketo konfigūraciją. 

  [![Biudžeto planų įtraukimas](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Maketo konfigūraciją galite peržiūrėti ir pagal poreikį koreguoti. 
1. Atidarykite **Šablonas** &gt; **Generuoti**, kad sukurtumėte šio maketo „Excel“ failą. 
2. Sugeneravę šabloną pasirinkite **Šablonas** &gt; **Peržiūrėti**, kad atidarytumėte ir peržiūrėtumėte biudžeto plano dokumento šabloną. „Excel“ failą galite įrašyti į vietinį diską. 

[![Įrašyti kaip](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> Biudžeto plano dokumento maketo redaguoti negalima, kai jis susietas su „Excel“ šablonu. Norėdami redaguoti maketą, panaikinkite susietą „Excel“ šablono failą ir sugeneruokite jį iš naujo. Tai būtina, kad maketo ir darbalapio laukai būtų sinchronizuoti. 

„Excel“ šablone bus pateikti visi biudžeto plano dokumento maketo elementai, kurių stulpelis **Pasiekiama darbalapyje** nustatytas į True. Persidengiančių elementų „Excel“ šablone pateikti negalima. Pvz., jei makete yra stulpeliai Užklausa per 1 ketvirtį, Užklausa per 2 ketvirtį, Užklausa per 3 ketvirtį ir Užklausa per 4 ketvirtį bei visų užklausų stulpelis, kuris nurodo visų 4 ketvirčių stulpelių sumą, „Excel“ šablone galima naudoti tik ketvirčių stulpelius arba visų užklausų stulpelį. Naujinimo metu „Excel“ failas negali atnaujinti persidengiančių stulpelių, nes lentelės duomenys gali tapti pasenę ir netikslūs.

[![Pavyzdys:](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Siekiant išvengti galimų problemų, susijusių su biudžeto plano duomenų peržiūra ir redagavimu programoje „Excel“, tas pats vartotojas turėtų prisijungti prie „Microsoft Dynamics 365 for Finance and Operations“ ir prie „Microsoft Dynamics Office“ papildinio duomenų jungties.

## <a name="add-a-header-to-budget-plan-document-template"></a>Antraštės įtraukimas į biudžeto plano dokumento šabloną
Norėdami įtraukti antraštės informaciją, pasirinkite viršutinę „Excel“ failo eilutę ir įterpkite tuščių eilučių. Dalyje **Duomenų jungtis** spustelėkite **Dizainas**, kad į „Excel“ failą įtrauktumėte antraštės laukų.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Skirtuke **Dizainas** spustelėkite **Įtraukti** ir tada **BudgetPlanHeader** pasirinkite kaip objekto duomenų šaltinį.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Nuveskite žymeklį į norimą vietą „Excel“ faile. Spustelėkite **Įtraukti žymą**, kad į pasirinktą vietą įtrauktumėte lauko žymą. Pasirinkite **Įtraukti vertę**, kad į pasirinktą vietą įtrauktumėte vertės lauką. Spustelėkite **Atlikta**, kad uždarytumėte dizaino įrankį.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Apskaičiuoto stulpelio įtraukimas į biudžeto plano dokumento šablono lentelę
--------------------------------------------------------------

Tada apskaičiuoti stulpeliai įtraukiami į sugeneruotą biudžeto plano dokumento šabloną. Stulpelis **Bendra užklausų suma**, kuriame pateikiama paraiškų už 1–4 ketvirčių stulpelių suma, ir stulpelis **Koregavimas**, kuriame stulpelio **Bendra užklausų suma** vertė perskaičiuojama naudojant iš anksto nustatytą koeficientą.

Dalyje **Duomenų jungtis** spustelėkite **Dizainas**, kad į lentelę įtrauktumėte stulpelių. Šalia duomenų šaltinio **BudgetPlanWorksheet** spustelėkite **Redaguoti**, kad pradėtumėte įkelti stulpelius.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Pasirinktoje laukų grupėje rodomi stulpeliai, pateikiami šablone. Spustelėkite **Formulė**, kad įtrauktumėte naują stulpelį. Pavadinkite naują stulpelį ir tada įklijuokite formulę lauke **Formulė**. Spustelėkite **Naujinti**, kad įterptumėte stulpelį.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Norėdami apibrėžti formulę, sukurkite formulę skaičiuoklėje ir tada nukopijuokite ją į langą **Dizainas**. „Finance and Operations“ susieta lentelė paprastai būna pavadinta „AXTable1“. Pvz., norėdami susumuoti paraiškų už 1–4 ketvirčių stulpelius skaičiuoklėje, sukurkite tokią formulę: AxTable1\[Paraiška už 1 ketvirtį\] + AxTable1\[Paraiška už 2 ketvirtį\] + AxTable1\[Paraiška už 3 ketvirtį\] + AxTable1\[Paraiška už 4 ketvirtį\].

Pakartokite šiuos veiksmus ir įterpkite stulpelį **Koregavimas**. Šiam stulpeliui priskirkite formulę: AxTable1\[Bendra užklausų suma\]\*$I$1 Tokiu būdu langelio I1 vertė bus padauginta iš stulpelio **Bendra užklausų suma** verčių, kad būtų apskaičiuotos koregavimo sumos.

Įrašykite ir uždarykite „Excel“ failą. Vėl atidarykite „Finance and Operations“ ir dalyje **Maketai** spustelėkite **Šablonas &gt; Naujinti**, kad įkeltumėte įrašytą „Excel“ šabloną naudoti biudžeto plane. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Uždarykite slankiklį **Maketai**. Dokumente **Biudžeto planas** spustelėkite **Darbalapis**, kad dokumentą peržiūrėtumėte ir redaguotumėte programoje „Excel“. Atkreipkite dėmesį, kad pakoreguotas „Excel“ šablonas buvo naudojamas šiam biudžeto plano darbalapiui sukurti, o apskaičiuoti stulpeliai atnaujinti naudojant formules, kurios buvo apibrėžtos ankstesniuose veiksmuose. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Biudžeto plano šablonų kūrimo patarimai
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Ar galiu į biudžeto plano šabloną įtraukti ir naudoti papildomus duomenų šaltinius?

Taip, galite naudoti meniu **Dizainas**, kad į tą patį ar kitus „Excel“ šablono lapus įtrauktumėte papildomų objektų. Pvz., galite įtraukti duomenų šaltinį **BudgetPlanProposedProject**, kad sukurtumėte ir tvarkytumėte siūlomų projektų sąrašą tuo pačiu metu, kai dirbate su biudžeto plano duomenimis programoje „Excel“. Atkreipkite dėmesį, kad įtraukiant didelės apimties duomenų šaltinius gali būti paveiktas „Excel“ darbaknygės veikimas. 

Galite naudoti dalyje **Duomenų jungtis** pateiktą parinktį **Filtras**, kad į papildomus duomenų šaltinius įtrauktumėte norimų filtrų.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Ar galiu nuo kitų vartotojų paslėpti duomenų jungties parinktį Dizainas?

Taip, atidarykite dalies **Duomenų jungiklis** parinktis, kad paslėptumėte parinktį **Dizainas** nuo kitų vartotojų.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Išplėskite dalies **Duomenų jungtis** parinktis ir atžymėkite žymės langelį **Įjungti dizainą**. Tokiu būdu paslėpsite dalies **Duomenų jungtis** parinktį **Dizainas**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Ar galiu užtikrinti, kad vartotojai, dirbdami su duomenimis, atsitiktinai neuždarytų duomenų jungties?

Rekomenduojame užrakinti šabloną, kad vartotojai jos atsitiktinai neišjungtų. Norėdami įjungti užraktą, spustelėkite **Duomenų jungtis**, viršutiniame kairiajame kampe pasirodo rodyklė. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Spustelėkite rodyklę, kad būtų parodytas papildomas meniu. Pasirinkite **Užrakinti**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Ar galiu biudžeto plano šablonuose naudoti kitas „Excel“ funkcijas, pvz., langelių formatavimą, spalvas, sąlyginį formatavimą ir diagramas?

Taip, biudžeto plano šablonuose veiks dauguma standartinių „Excel“ funkcijų. Rekomenduojame naudoti kodavimo spalvomis funkciją, kad vartotojai galėtų lengviau atskirti tik skaitomus ir redaguojamus stulpelius. Sąlyginio formatavimo funkciją galima naudoti norint paryškinti problematiškas biudžeto sritis. Bendras stulpelių sumas galima lengvai pateikti naudojant „Excel“ formules virš lentelės.

Taip pat galite kurti ir naudoti suvestinės lenteles bei diagramas, norėdami atlikti papildomų biudžeto duomenų grupavimo ir vizualizavimo veiksmų. Skirtuko **Duomenys** grupėje **Ryšiai** spustelėkite **Atnaujinti viską**, o tada spustelėkite **Ryšių ypatybės**. Spustelėkite skirtuką **Naudojimas**. Dalyje **Naujinti** pažymėkite žymės langelį **Naujinti duomenis atidarant failą**. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)





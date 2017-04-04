---
title: "Biudžetų sudarymo modulio apžvalga"
description: "Beveik kiekvienoje įmonėje, kuri naudoja Financials funkcionalumą Microsoft Dynamics 365 operacijoms turi turėti galimybę kurti ataskaitas, biudžetas, palyginus su faktinių duomenų palyginimas. Šiame straipsnyje paaiškinama minimumas rankos, kurio reikia siekiant sukurti biudžeto dinamika 365 operacijoms arba įkelti juos iš trečiųjų šalių programos."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a639e509cf6a3d2f1b850f27481d7b95546522b8
ms.openlocfilehash: b62e14f7c91692ae97bb332b38b0deeb328cc1bd
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-overview"></a>Biudžetų sudarymo modulio apžvalga

Beveik kiekvienoje įmonėje, kuri naudoja Financials funkcionalumą Microsoft Dynamics 365 operacijoms turi turėti galimybę kurti ataskaitas, biudžetas, palyginus su faktinių duomenų palyginimas. Šiame straipsnyje paaiškinama minimumas rankos, kurio reikia siekiant sukurti biudžeto dinamika 365 operacijoms arba įkelti juos iš trečiųjų šalių programos.

<a name="overview"></a>Apžvalga
--------

Patvirtintas juridinio subjekto biudžetas yra tvarkomas dokumente, pavadinimu *biudžeto registro įrašas*. Biudžeto registro įrašo dokumento eilutės yra vadinama *biudžeto sąskaitos* įrašų, finansinės dimensijos informaciją, datas ir sumas patvirtinto biudžeto. Biudžeto registro įrašo dokumento yra integruota su pagrindinės finansinės ataskaitos ir tyrimo puslapius, kur knygos faktinės sumos yra palyginti su biudžeto sumas. 

Yra daug būdų sukurti biudžetą registrų įrašų Dynamics 365 operacijoms:

-   Patys įveskite dokumento informaciją puslapyje **Biudžeto registro įrašai**.
-   Naudokite „Microsoft Excel“ šabloną, kurį galite atidaryti spustelėdami mygtuką **Atidaryti „Excel“**, esantį puslapyje **Biudžeto registro įrašai**.
-   Naudokite puslapio **Biudžeto sąskaitos įrašai** dalies Duomenų valdymas duomenų objektą biudžeto registro įrašams importuoti. Jūs turėtumėte apsvarstyti, naudojant šį metodą ir įjungimas į **paremti** ** perdirbimo ** parametras, kai turite importuoti daug biudžeto sąskaitos įrašai į sistemą.
-   Jei įmonė naudoja funkciją Biudžeto planavimas biudžeto duomenims parengti, galite naudoti periodinio apdorojimo parinktį **Generuoti biudžeto registro įrašą**.

Sąmatos registro įrašas yra laikomas baigtas atnaujinus biudžeto pusiausvyrą. Dėl į **biudžetą užregistruoti įrašus** spustelėkite **atnaujinti biudžeto balansai** pasirinktą biudžetą užregistruoti įrašą arba kelis įrašus. Atnaujinus biudžeto balansus, biudžeto registro įrašo būsena pasikeičia į **Baigtas**. Baigto biudžeto registro įrašo negalima atidaryti iš naujo ir redaguoti. Todėl, jei reikia redaguoti biudžeto duomenis, turite sukurti naują biudžeto registro įrašą, o ne redaguoti baigto biudžeto registro įrašo duomenis.

## <a name="configuration"></a>Konfigūravimas
Konfigūruodami biudžetą pradėkite puslapyje **Biudžeto sudarymo parametrai**. Šiame puslapyje turite nustatyti biudžeto žurnalą, biudžeto registro įrašų numeraciją ir numatytąją darbo srities elgseną.

Tada, jei strategijų, valdančių biudžeto registro įrašų tvirtinimą, atsižvelgdami į biudžeto tipą (pvz., perkėlimus arba tikslinimus) turite sukurti biudžeto registro įrašų darbo eigas puslapyje **Biudžeto sudarymo darbo eigos**. Jei yra scenarijų, pagal kuriuose perkėlimai būtų leidžiami be darbo eigos patvirtinimo, galite nustatyti biudžeto perkėlimo taisykles tiems scenarijams palaikyti. 

Puslapyje **Biudžeto sudarymo dimensijos** turite pasirinkti sudarant biudžetą naudojamas finansines dimensijas pagal sąskaitų plane naudojamas dimensijas. Galite pasirinkti visas biudžeto sudarymo finansines dimensijas arba jų subrinkinį.

Nustatyti, * biudžeto modelio *, atitinka visas ar tam tikras biudžeto. Galite vieną visų biudžeto registro įrašų biudžeto modelį. Taip pat galite kurti atskirus modelius pagal biudžeto tipą, geografinę vietą arba naudodami kitą biudžeto klasifikavimo būdą. 

> [!NOTE] 
> Jei biudžeto valdymo, galite susieti tik vieną biudžeto modelis su konkrečių biudžeto ciklo laiko tarpą. 

Kurkite *biudžeto kodus*, nurodančius įrašytinų biudžeto operacijų tipą ir bet kokią susijusią darbo eigą. Biudžeto kodai gali palaikyti toliau nurodytus biudžeto tipus.

-   Pradinis biudžetas
-   Perkėlimas
-   Tikslinimas
-   Biudžeto rezervavimas
-   Preliminarus biudžeto rezervavimas
-   Perkeliamas biudžetas

Biudžeto kodai suteikia galimybę patvirtintų biudžeto pakeitimų įrašus sekti biudžeto ciklo metu. Jei darbo eigos yra susijęs su biudžeto kodas, darbo eiga bus įjungtas visų biudžeto registrų įrašų, naudojančių tą biudžeto kodas ir darbo eigos veiksmai turi būti baigtas prieš biudžeto registro įrašą gali pasiekti ir **atlikta** etapas.  

Galite pasirinktinai nustatyti *biudžeto perkėlimo taisykles*. Naudoti biudžeto perkėlimo taisyklės, pasirinkite **naudoti taisykles dėl biudžeto perkėlimų** ant to **biudžeto parametrai** puslapis. Kai naudojamos biudžeto perkėlimo taisyklės, jei vartotojas sukuria dokumentą naudodamas tipo **Perkėlimas** biudžeto kodą, biudžeto balansai nebus atnaujinami, jei pažeistos biudžeto perkėlimo taisyklės. Pavyzdžiui, galite leisti biudžeto perkėlimo dokumentus, jei išlaidų biudžetas yra perkeliama pagrindinėse pardavimų ir rinkodaros padalinio sąskaitose, bet galite uždrausti biudžeto perkėlimą iš arba į tą padalinį, jei negautas to tipo biudžeto sąskaitos išrašo darbo eigos patvirtinimas.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Darbo sričių ir užklausų puslapių naudojimas biudžetui ir faktinėms sumoms sekti
Biudžeto vadybininkas gali peržiūrėti dabartinę biudžeto būseną darbo srityje **DK biudžetai ir prognozės**. Skirtukuose **Išlaidos, viršijančios biudžetą** ir **Biudžeto įplaukos** galima greitai peržiūrėti finansinių dimensijų derinius, kai biudžeto tikslai neįvykdomi arba artėja prie slenksčio. Biudžeto slenksčio procentą ir finansinių dimensijų rinkinius, naudojamus tuose skirtukuose, galite pritaikyti spustelėdami **Konfigūruoti mano darbo sritį**. Galite spustelėti **Grupių vadovai** ir peržiūrėti darbuotojus, kurie yra atsakingi už konkrečius finansinių dimensijų derinius, pasirinktus tuose skirtukuose. Pvz., jei matote, kad operacijų padalinio išlaidų biudžetas viršija biudžeto slenkstį, galite lengvai rasti ir susisiekti su operacijų padalinio vadovu bei tai aptarti. 

> [!NOTE] 
> Į **departamento vadovas** lauko, **organizacijos vienetus** puslapis nurodo, kurioje profesijų konkrečių finansinių dimensijų derinius. Skirtuko apačioje spustelėkite **Žr. daugiau**, norėdami atidaryti užklausų puslapį **Biudžeto ir faktinė sumos** ir gauti daugiau informacijos apie biudžeto sumas ir faktines sumas. 

Užklausų puslapis **Faktinė ir biudžeto sumos** suteikia galimybę detalizuoti biudžeto ir faktinės sumų informaciją. Užklausų puslapyje pasirinkite eilutę ir tada spustelėkite **Laikotarpio balansai**, norėdami peržiūrėti biudžeto ir faktinę sumas, paskirstytas ataskaitiniuose laikotarpiuose. Puslapyje **Biudžeto sąskaitos įrašai** pateikta detalizuota biudžeto registro įrašų biudžeto sumos informacija. Puslapyje **Bendrojo žurnalo įrašai **atidaromos DK operacijos, kurios yra įtrauktos į apskaičiuotą **faktinę** sumą. 

Įmonė, kuri naudojama funkciją Biudžeto planavimas, gali kurti ir naudoti *biudžeto prognozes * darbo srityje **DK biudžetai ir prognozės**.



---
title: Biudžetų sudarymo modulio apžvalga
description: Beveik kiekviena įmonė, naudojanti finansinių Microsoft Dynamics funkcijų funkciją 365 finansuose, turės turėti galimybę kurti biudžeto ir faktinių duomenų ataskaitas. Šiame straipsnyje paaiškinama konfigūravimo veiksmai, kuriuos reikia atlikti norint kurti biudžetus programoje „Finance and Operations“ arba įkelti juos iš trečiosios šalies programos.
author: panolte
ms.date: 04/29/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60113"
- intro-internal
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48fcfec7126b4835b7d05e431bbc6ad7b9176bbe
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710419"
---
# <a name="budgeting-overview"></a>Biudžetų sudarymo modulio apžvalga

[!include [banner](../includes/banner.md)]

Beveik kiekviena įmonė, naudojanti finansinių Microsoft Dynamics funkcijų funkciją 365 finansuose, turės turėti galimybę kurti biudžeto ir faktinių duomenų ataskaitas. Šiame straipsnyje paaiškinama konfigūravimo veiksmai, kuriuos reikia atlikti norint kurti biudžetus programoje „Finance and Operations“ arba įkelti juos iš trečiosios šalies programos.

## <a name="overview"></a>Apžvalga

Patvirtintas juridinio subjekto biudžetas yra tvarkomas dokumente, pavadinimu *biudžeto registro įrašas*. Biudžeto registro įrašo dokumento eilutės yra vadinamos *biudžeto sąskaitos* įrašais ir jose yra finansinių dimensijų informacija, patvirtinto biudžeto datos ir sumos. Biudžeto registro įrašo dokumentas yra integruotas su pagrindinėmis finansinėmis ataskaitomis ir užklausų puslapiais, kuriuose faktinės DK sumos yra lyginamos su biudžeto sumomis. 

Galima naudoti kelis toliau pateiktus būdus, norint kurti biudžeto registro įrašus.

-   Patys įveskite dokumento informaciją puslapyje **Biudžeto registro įrašai**.
-   Naudokite „Microsoft Excel“ šabloną, kurį galite atidaryti spustelėdami mygtuką **Atidaryti „Excel“**, esantį puslapyje **Biudžeto registro įrašai**.
-   Naudokite puslapio **Biudžeto sąskaitos įrašai** dalies Duomenų valdymas duomenų objektą biudžeto registro įrašams importuoti. Galite apsvarstyti galimybę naudoti šį metodą ir įjungti parametrą **Apdorojimas pagal rinkinį**, kai į sistemą reikia importuoti daug biudžeto sąskaitos įrašų.
-   Jei įmonė naudoja funkciją Biudžeto planavimas biudžeto duomenims parengti, galite naudoti periodinio apdorojimo parinktį **Generuoti biudžeto registro įrašą**.

Biudžeto registro įrašas bus laikomas atliktas, kai biudžeto balansai bus atnaujinti. Puslapyje **Biudžeto registro įrašai** spustelėkite pasirinkto biudžeto registro įrašo arba kelių įrašų parinktį **Atnaujinti biudžetų balansus**. Atnaujinus biudžeto balansus, biudžeto registro įrašo būsena pasikeičia į **Baigtas**. Baigto biudžeto registro įrašo negalima atidaryti iš naujo ir redaguoti. Todėl, jei reikia redaguoti biudžeto duomenis, turite sukurti naują biudžeto registro įrašą, o ne redaguoti baigto biudžeto registro įrašo duomenis.

## <a name="configuration"></a>Konfigūravimas
Konfigūruodami biudžetą pradėkite puslapyje **Biudžeto sudarymo parametrai**. Šiame puslapyje turite nustatyti biudžeto žurnalą, biudžeto registro įrašų numeraciją ir numatytąją darbo srities elgseną.

Tada, jei strategijų, valdančių biudžeto registro įrašų tvirtinimą, atsižvelgdami į biudžeto tipą (pvz., perkėlimus arba tikslinimus) turite sukurti biudžeto registro įrašų darbo eigas puslapyje **Biudžeto sudarymo darbo eigos**. Jei yra scenarijų, pagal kuriuose perkėlimai būtų leidžiami be darbo eigos patvirtinimo, galite nustatyti biudžeto perkėlimo taisykles tiems scenarijams palaikyti. 

Puslapyje **Biudžeto sudarymo dimensijos** turite pasirinkti sudarant biudžetą naudojamas finansines dimensijas pagal sąskaitų plane naudojamas dimensijas. Galite pasirinkti visas biudžeto sudarymo finansines dimensijas arba jų subrinkinį.

Nurodykite *biudžeto modelį*, kuris atitinka visus arba kai kuriuos biudžetus. Galite vieną visų biudžeto registro įrašų biudžeto modelį. Taip pat galite kurti atskirus modelius pagal biudžeto tipą, geografinę vietą arba naudodami kitą biudžeto klasifikavimo būdą. 

> [!NOTE] 
> Jei naudojama biudžeto kontrolė, su konkrečia biudžeto ciklo trukme galima susieti tik vieną biudžeto modelį. 

Kurkite *biudžeto kodus*, nurodančius įrašytinų biudžeto operacijų tipą ir bet kokią susijusią darbo eigą. Biudžeto kodai gali palaikyti toliau nurodytus biudžeto tipus.

-   Pradinis biudžetas
-   Perkėlimas
-   Tikslinimas
-   Biudžeto rezervavimas
-   Preliminarus biudžeto rezervavimas
-   Perkeliamas biudžetas

Biudžeto kodai suteikia galimybę patvirtintų biudžeto pakeitimų įrašus sekti biudžeto ciklo metu. Jei darbo eiga yra susieta su biudžeto kodu, darbo eiga bus įjungta visiems biudžeto registro įrašams, naudojantiems tą biudžeto kodą, o darbo eigos veiksmai turi būti atlikti prieš biudžeto registro įrašo etapą **Baigtas**.  

Taip pat galite pasirinktinai nustatyti *biudžeto perkėlimo taisykles*. Norėdami naudoti biudžeto perkėlimo taisykles, puslapyje **Biudžeto parametrai** pažymėkite **Naudoti biudžeto perkėlimo taisykles**. Kai naudojamos biudžeto perkėlimo taisyklės, jei vartotojas sukuria dokumentą naudodamas tipo **Perkėlimas** biudžeto kodą, biudžeto balansai nebus atnaujinami, jei pažeistos biudžeto perkėlimo taisyklės. Pavyzdžiui, galite leisti biudžeto perkėlimo dokumentus, jei išlaidų biudžetas yra perkeliama pagrindinėse pardavimų ir rinkodaros padalinio sąskaitose, bet galite uždrausti biudžeto perkėlimą iš arba į tą padalinį, jei negautas to tipo biudžeto sąskaitos išrašo darbo eigos patvirtinimas.

Funkcijos, kurios buvo įvestos Microsoft Dynamics 365 finansinės versijos 10.0.7 (2020 m. sausio mėn.) galimybė ir lankstumo biudžeto registro įrašams. Norėdami aktyvinti šiuos patobulinimus, eikite į darbo sritį **Funkcijų valdymas** ir pasirinkite **Biudžeto registro įrašai tik kiekiui** ir (arba) **Numatytieji biudžeto registro įrašų sumos tipai**.

Funkcija **Biudžeto registro įrašai tik kiekiui** leidžia registruoti biudžeto registro įrašą su tik kiekio sumomis. Pavyzdžiui, galite užregistruoti biudžeto įrašą, kurio kiekis yra 32, o kaina – nulis, tokiu būdu gaunant nulinę sumą. Tada šį kiekį galite naudoti finansinės ataskaitos kontekste, kad nustatytumėte kainą pagal kiekį. Atkreipkite dėmesį, kad naudojant šią funkciją nebuvo atnaujinta nė viena iš užklausų ar ataskaitų; funkcija tiesiog leidžia užregistruoti nulinę sumą.

Funkcija **Numatytieji biudžeto registro įrašų sumos tipai** leidžia biudžeto registro įraše naudoti numatytąjį sumos tipą, kurio sumos tipas nėra išlaidos. Kai pagrindinės sąskaitos tipas yra išlaidos, numatytoji biudžeto registro įrašo eilutė dabar bus išlaidos; kai pagrindinės sąskaitos tipas yra išlaidos, numatytoji eilutės bus pajamos; visiems kitiems sąskaitų tipams numatytoji eilutė bus išlaidos.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Darbo sričių ir užklausų puslapių naudojimas biudžetui ir faktinėms sumoms sekti
Biudžeto vadybininkas gali peržiūrėti dabartinę biudžeto būseną darbo srityje **DK biudžetai ir prognozės**. Skirtukuose **Išlaidos, viršijančios biudžetą** ir **Biudžeto įplaukos** galima greitai peržiūrėti finansinių dimensijų derinius, kai biudžeto tikslai neįvykdomi arba artėja prie slenksčio. Biudžeto slenksčio procentą ir finansinių dimensijų rinkinius, naudojamus tuose skirtukuose, galite pritaikyti spustelėdami **Konfigūruoti mano darbo sritį**. Galite spustelėti **Grupių vadovai** ir peržiūrėti darbuotojus, kurie yra atsakingi už konkrečius finansinių dimensijų derinius, pasirinktus tuose skirtukuose. Pvz., jei matote, kad operacijų padalinio išlaidų biudžetas viršija biudžeto slenkstį, galite lengvai rasti ir susisiekti su operacijų padalinio vadovu bei tai aptarti. 

> [!NOTE] 
> Puslapio **Organizacijos vienetai** laukas **Padalinio vadovas** nustato, kurie vadovai palaiko konkrečius finansinių dimensijų derinius. Skirtuko apačioje spustelėkite **Žr. daugiau**, norėdami atidaryti užklausų puslapį **Biudžeto ir faktinė sumos** ir gauti daugiau informacijos apie biudžeto sumas ir faktines sumas. 

Užklausų puslapis **Faktinė ir biudžeto sumos** suteikia galimybę detalizuoti biudžeto ir faktinės sumų informaciją. Užklausų puslapyje pasirinkite eilutę ir tada spustelėkite **Laikotarpio balansai**, norėdami peržiūrėti biudžeto ir faktinę sumas, paskirstytas ataskaitiniuose laikotarpiuose. Puslapyje **Biudžeto sąskaitos įrašai** pateikta detalizuota biudžeto registro įrašų biudžeto sumos informacija. Puslapyje **Bendrojo žurnalo įrašai** atidaromos DK operacijos, kurios yra įtrauktos į apskaičiuotą **faktinę** sumą. 

Įmonė, kuri naudojama funkciją Biudžeto planavimas, gali kurti ir naudoti *biudžeto prognozes* darbo srityje **DK biudžetai ir prognozės**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

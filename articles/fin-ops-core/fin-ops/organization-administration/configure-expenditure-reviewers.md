---
title: Išlaidų tikrintojų konfigūravimas
description: Šioje temoje aprašoma, kaip naudoti išlaidų tikrintojus, norint dinamiškai pasirinkti vartotoją, kuriam priskirta darbo eigos užduotis, patvirtinimas arba rankinis sprendimas.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: ad980889247e0239ad743078cb013c1c5839f676
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070151"
---
# <a name="configure-expenditure-reviewers"></a>Išlaidų tikrintojų konfigūravimas
[!include[banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Galite nustatyti dinaminius išlaidų tikrintojus norėdami nukreipti išlaidas peržiūrai pagal vartotoją, kuris priskirtas projekto vaidmeniui arba pagal finansinę dimensiją, kurioje taikomas mokestis. Darbo eigos procesas naudoja nurodytą projekto vaidmenį arba finansinės dimensijos savininką, kad nustatytų, kam nukreipti išlaidas.

Galite apibrėžti vieną arba daugiau išlaidų tikrintojų konfigūracijų, o tada pasirinkti konfigūraciją kurdami darbo eigą. Taip pat galite sukonfigūruoti išlaidų tikrintojo reikšmes kiekvienam jūsų organizacijos juridiniam subjektui. Apibrėžę išlaidų tikrintojų konfigūracijas, priskirkite konfigūraciją. Išlaidų tikrintojai gali būti priskirti darbo eigos užduotims, patvirtinimams ir rankiniams sprendimams.

> [!NOTE]
> Nors išlaidų tikrintojai nėra privalomi, jie gali padėti supaprastinti jūsų darbo eigos konfigūraciją. Pavyzdžiui, jums nereikia kurti vieno sąlyginio sprendimo, patikrinantį kiekvieną išlaidų centro dimensiją, o tada sukurti kitą elementą, kad patvirtinimas arba užduotis būtų priskirti konkrečiam vartotojui arba vartotojų grupėms. Užuot tai darę, galite sukonfigūruoti išlaidų centro dimensijos savininką ir naudoti išlaidų tikrintoją, kad dinamiškai pasirinktumėte tinkamą vartotoją. Tokiu būdu, kai pasikeičia išlaidų centrų nuosavybė ar priskyrimas, jums reikia tik atnaujinti finansinės dimensijos **Savininko** lauką.

## <a name="types-of-expenditure-reviewers"></a>Išlaidų tikrintojų tipai

Ne visos darbo eigos palaiko išlaidų tikrintojų koncepciją. Pagal numatytuosius nustatymus galite konfigūruoti pirkimo paraiškų, pirkimo užsakymų, tiekėjo sąskaitų faktūrų ir išlaidų ataskaitų išlaidų tikrintojus. Kiekvienas iš šių darbo eigos tipų reikalauja sukonfigūruoti išlaidų tikrintojus atskirame puslapyje, kuris yra konkretus funkcijai ir moduliui. Kiekviename palaikomame dokumente išlaidų tikrintojai gali būti naudojami su antraštės arba eilutės lygio darbo eigomis.

Šioje lentelėje rodoma, kur galite konfigūruoti kiekvieno palaikomo dokumento išlaidų tikrintoją.

| Dokumentas | Naršymo kelias |
|----------|-----------------|
| Išlaidų ataskaitos | Išlaidų valdymas \> Nustatymas \> Strategijos \> Išlaidų tikrintojai |
| Pirkimo užsakymai | Įsigijimas ir išteklių tiekimas \> Nustatymas \> Strategijos \> Pirkimo užsakymo išlaidų tikrintojai |
| Pirkimo paraiškos | Įsigijimas ir išteklių tiekimas \> Nustatymas \> Strategijos \> Pirkimo paraiškos išlaidų tikrintojai |
| Tiekėjo SF | Mokėtinos sumos \> Strategijos nustatymas \> Tiekėjo sąskaitos faktūros išlaidų tikrintojai |

## <a name="expenditure-reviewer-assignments"></a>Išlaidų tikrintojo priskyrimai

Galimi du kiekvieno išlaidų redaktoriaus priskyrimo tipai: *projekto paskirstymai* ir *organizacijos paskirstymai*. Projekto paskirstymui galite pasirinkti projekto vadovus arba finansines dimensijas. Organizacijos paskirstymui galite pasirinkti finansines dimensijas.

Projekto vadovai apima projekto vadovą, projekto kontrolę ir projekto pardavimų vadybininką. Šiuos vadovus nurodote tiesiogiai savo projekte pasirinkdami darbuotoją atitinkamuose laukuose.

Finansines dimensijas kontroliuoja kiekvieno juridinio subjekto sąskaitų struktūros. Kiekvienam juridiniam subjektui galite pasirinkti, kurios finansinės dimensijos bus naudojamos su išlaidų tikrintoju. Dimensijos gali būti iš projekto (šiuo atveju jūs pasirenkate dimensijas skirtuke **Projektų paskirstymas**) arba iš dokumento (šiuo atveju pasirenkate dimensijas skirtuke **Organizacijos paskirstymas**). **Finansinių dimensijų reikšmių** puslapio lauke **Savininkas** galite pasirinkti darbuotoją kiekvienai finansinei dimensijai.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>1 pavyzdys: Išlaidų tikrintojai, pagrįsti organizacijos paskirstymais

Dirbate „Contoso Appliances“, o jūsų organizacijoje yra šeši skyriai ir 10 išlaidų centrų. Kai pateikiama nauja pirkimo paraiška, ją pirmiausia turi patvirtinti padalinio vadovas, o tada išlaidų centro vadovas.

Šiame pavyzdyje konfigūruojate du *pirkimo paraiškų išlaidų tikrintojus*:

- Pirmam tikrintojui pavadinkite padalinį, o tada pasirinkite **Padalinio** finansinę dimensiją skirtuke **Organizacijos paskirstymas**. 
- Antram tikrintojui pavadinkite išlaidų centrą, o tada pasirinkite **Išlaidų centro** finansinę dimensiją skirtuke **Organizacijos paskirstymas**.

Kai konfigūruojate darbo eigą, sukuriate du patvirtinimo veiksmus. Pirmasis yra skirtas padaliniui, o antrasis – išlaidų centrui. Kiekvienam patvirtinimo elementui pasirenkate **Dalyvį** skirtuko **Pagal vaidmenį** lauke **Priskyrimo tipas** bei **Išlaidų dalyviai** lauke **Dalyvio tipas**, o tada pasirinkite atitinkamą dalyvį **Dalyvio** lauke.

Kai sukuriama pirkimo paraiška, padalinio ir išlaidų centro finansinės dimensijos yra priskiriamos pirkimo paraiškos eilutėms. Pateikus darbo eigą, sistema pirmiausia įvertina pirkimo paraiškos padalinį ir priskiria patvirtinimo elementą vartotojui, susijusiam su darbuotoju, kurį pasirinkote padaliniui. Atlikus pirmąjį patvirtinimo veiksmą, sistema įvertina antrąjį patikrinimo veiksmą ir priskiria antrąjį patvirtinimo elementą vartotojui, susijusiam su darbuotoju, kurį pasirinkote išlaidų centrui.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>2 pavyzdys: Išlaidų tikrintojai, pagrįsti projekto paskirstymais

Dirbate „Contoso Appliances“ paslaugų skyriuje. Organizacija reikalauja, kad kiekvieno pirkimo užsakymo projekto vadovas privalo patvirtinti išlaidas. Be to, projekto išlaidų centro vadovas turi jas patvirtinti. Patvirtinimai gali būti atliekami tuo pačiu metu. Bet kuriuo atveju abu vartotojai turi patvirtinti pirkimo užsakymą prieš tęsdami darbo eigą.

Šiame pavyzdyje jūs sukuriate vieną *pirkimo užsakymo išlaidų tikrintoją*, pavadintą **PM ir Išlaidų centru**. Jūs pasirenkate **Projekto vadovo** žymės langelį ir nustatote **Išlaidų centro dimensijos** parinktį į **Taip** skirtuke **Projekto paskirstymai**, esančiame **Pirkimo užsakymo išlaidų tikrintojo** puslapyje. Kaip konfigūracijos dalį turite užtikrinti, kad **Projekto vadovo** laukas būtų nustatytas visiems projektams ir tai, kad savininkas būtų nurodytas visiems išlaidų centrams **Finansinių dimensijų reikšmių** puslapyje.

Kai konfigūruojate darbo eigą, jums reikia patvirtinimo elemento. Pasirenkate **Dalyvį** lauke **Priskyrimo tipas**. Tada skirtuke **Pagal vaidmenį** pasirenkate **Išlaidų dalyviai** lauke **Dalyvių tipai** bei pasirenkate projekto vadovą ir išlaidų centrą **Dalyvio** lauke. Norėdami užtikrinti, kad darbo eigos nebūtų galima tęsti tol, kol projekto vadovas ir išlaidų centro savininkas nepatvirtins darbo eigos, nustatykite **Užbaigimo strategija** lauką į **Visi tvirtintojai**.

Sukūrus pirkimo užsakymą, turi būti nurodytas **Projekto** laukas. Jei jums nereikia visų savo pirkimo užsakymų projekto, turite įtraukti sąlyginį sprendimą į savo darbo eigą, kad prieš paleisdami patvirtinimo veiksmą patikrintumėte projektą. Tada sistema įvertina nurodytą pirkimo užsakymo projektą ir priskiria patvirtinimo elementą vartotojui, susijusiam su darbuotoju **Projekto vadovo** lauke. Be to, sistema sukuria užduotį ir priskiria ją vartotojui, susijusiam su darbuotoju, kurį pasirenkate **Savininko** lauke projekto išlaidų centrui. Atkreipkite dėmesį, kad šiame pavyzdyje naudojamas projekto, o ne pirkimo užsakymo išlaidų centras.

## <a name="set-up-expenditure-reviewers"></a>Išlaidų tikrintojų nustatymas

Šiame pavyzdyje rodoma, kaip sukonfigūruoti pirkimo paraiškų išlaidų tikrintoją. Norėdami sukonfigūruoti kitų tipų išlaidų tikrintojus, pakeiskite 1 veiksmo naršymo maršrutą atitinkamu maršrutu iš [Išlaidų tikrintojų tipų](configure-expenditure-reviewers.md#types-of-expenditure-reviewers) skyriaus lentelės, esančios anksčiau šioje temoje.

1. Eikite į **Įsigijimas ir išteklių tiekimas \> Nustatymas \> Strategijos \> Pirkimo paraiškos išlaidų tikrintojai**.
2. Puslapyje **Pirkimo paraiškos išlaidų tikrintojai** pasirinkite **Naujas**.
3. Lauke **Pavadinimas** įveskite išlaidų tikrintojo konfigūracijos pavadinimą, pavyzdžiui, **išlaidų centras**.
4. „FastTab” skirtuke **Išlaidų tikrintojai pagal juridinį subjektą** pasirinkite juridinį subjektą, kuris bus konfigūruojamas.
5. Projekto paskirstymui pasirinkite žymės langelį kiekvienam projekto vadovui ir pasirinkite **Taip** kiekvienai finansinei dimensijai, kurią norite įgalinti. 
6. Organizacijos paskirstymui skirtuke **Organizacijos paskirstymai** pasirinkite **Taip** kiekvienai finansinei dimensijai, kurią norite įgalinti.
7. Kartokite 4–6 veiksmus su kiekvienu papildomu juridiniu asmeniu.

## <a name="assign-owners-to-financial-dimensions"></a>Savininkų priskyrimas finansinėms dimensijoms

Norėdami priskirti savininką finansinei dimensijai, atlikite šiuos žingsnius.

1. Eikite į **Didžioji knyga \> Sąskaitų planas \> Dimensijos \> Finansinės dimensijos**.
2. Sąraše pasirinkite finansinę dimensiją, kuriai norite priskirti savininkus.
3. Pasirinkite **Dimensijos reikšmės**.
4. Pasirinkite **Redaguoti**, kad atliktumėte dimensijos reikšmių pakeitimus.
5. Sąraše pasirinkite dimensijos reikšmę, kuriai norite priskirti savininką.
6. Lauke **Savininkas** pasirinkite darbuotoją, kuriam norite priskirti dimensijos reikšmę.

## <a name="configure-project-distributions"></a>Projekto paskirstymų konfigūravimas

Norėdami priskirti projekto vadovus projektui, atlikite šiuos veiksmus.

1. Eikite į **Projektų valdymas ir apskaita \> Projektai \> Visi projektai**.
2. Pasirinkite projektą, prie kurio priskirsite vadovus.
3. Pasirinkite **Redaguoti**, kad atliktumėte projekto pakeitimus.
4. „FastTab” skirtuko **Bendra** skyriuje **Atsakingi** pasirinkite darbuotoją **Pardavimų vadybininko**, **Projekto vadovo** ir **Projekto kontrolės** laukams, kaip reikia.
5. „FastTab” skirtuke **Finansinės dimensijos** pasirinkite reikiamas jūsų projekto finansines dimensijas.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Išlaidų tikrintojų priskyrimas darbo eigos užduočiai

Šiame pavyzdyje parodyta, kaip sukonfigūruoti pirkimo paraiškos darbo eigą taip, kad ji naudotų pirkimo paraiškos išlaidų tikrintoją. Norėdami konfigūruoti kitų tipų darbo eigas, darbo eigos puslapis, kurį turite atidaryti 1 veiksmu, gali būti **Išlaidų valdymo** arba **Mokėtinų sumų** modulyje, o ne **Įsigijimo ir išteklių tiekimo** modulyje.

Norėdami priskirti pirkimo paraiškos išlaidų tikrintojus darbo eigos užduočiai, atlikite šiuos veiksmus.

1. Eikite į **Įsigijimas ir išteklių tiekimas \> Sąranka \> Įsigijimo ir šaltinio pasirinkimo darbo srautai**.
2. Dukart bakstelėkite (arba dukart spustelėkite) esamą darbo eigą arba sukurkite naują darbo eigą.
3. Darbo eigos rengyklės srityje **Darbo eiga** pasirinkite užduotį, prie kurios norite priskirti išlaidų tikrintojo konfigūraciją. Tada **Veiksmų srities** grupėje **Rodyti** pasirinkite **Ypatybės**.
4. Kairiojoje puslapio **Ypatybės** srityje pasirinkite **Priskyrimas**.
5. Skirtuke **Priskyrimo tipas** pasirinkite **Dalyvis**.
6. Skirtuko **Vaidmeniu pagrįstas** lauke **Dalyvio tipas** pasirinkite **Išlaidų dalyviai**. Tada **Dalyvio** lauke pasirinkite išlaidų tikrintojo konfigūraciją, kurią norite naudoti darbo eigos užduotyje.

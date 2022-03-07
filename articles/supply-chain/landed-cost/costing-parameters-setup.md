---
title: Įkainojimo parametrų verčių nustatymas
description: Kai nustatote iškrovimo kainos modulį, galite apibrėžti kelis bendrųjų verčių rinkinius, kurie bus prieinami pasirinkus konkrečius įkainojimo parametrų reikšmių tipus kitose programos dalyse. Šioje temoje paaiškinama, kaip nustatyti šiuos verčių rinkinius.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1bcce7af0a15add63f1d9c3b32563de0ab6698bd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577653"
---
# <a name="costing-parameter-values-setup"></a>Įkainojimo parametrų verčių nustatymas

[!include [banner](../../includes/banner.md)]

Kai nustatote modulį **Iškrovimo kaina**, galite apibrėžti kelis bendrųjų verčių rinkinius ir susijusius parametrus kiekvienai vertei. Šios vertės bus prieinamos pasirinkus konkrečius įkainojimo parametrų verčių tipus kitose programos dalyse. Šioje temoje paaiškinama, kaip nustatyti šiuos verčių rinkinius.

## <a name="set-up-cost-type-codes"></a>Savikainos tipų kodų nustatymas

Savikainos tipų kodai apibrėžia savikainos, patiriamos pakraunant prekes į sandėlį, tipą ar reiso iškrovimo kainą. Nors paprastai padidinama prekių vertė, jas taip pat galima naudoti sumoms DK kaupti. DK koregavimai naudojami, kai savikaina kaupiama per tam tikrą laiką arba per reisų seriją ir vienos operacijos korespondentinę sąskaitą.

> [!NOTE]
> Jei savikainos tipų lentelė bendrai naudojama tarp juridinių subjektų, sąskaitų planas taip pat turi būti bendrai naudojamas tarp juridinių subjektų. Priešingu atveju registravimo operacijos veiks netinkamai.

Norėdami nustatyti savo savikainos tipų kodus, eikite į **Iškrovimo kaina \>Įkainojimo nustatymas\> Savikainos tipų kodai**. Veiksmų srities mygtukus galite naudoti naujiems savikainos tipų kodams kurti, esamiems kodams redaguoti arba pasirinktam savikainos tipui panaikinti.

Šioje lentelėje apibūdinami laukeliai, galimi kiekvienam savikainos tipo kodui.

| Laukas | aprašymas |
|---|---|
| Išlaidų tipo kodas | Įveskite savikainos tipo kodo pavadinimą. |
| aprašymas | Įveskite savikainos tipo kodo aprašymą. |
| Naudoti gabenimo kursą | Šią parinktį nustatykite kaip *Taip*, jei reiso valiutos kuras (kartais vadinamas valdymo kursu) turi būti naudojamas šios savikainos vertei apskaičiuoti. Šiuo atveju, siuntimo tarifas bus naudojamas vietoje standartinio numatytojo arba vietos valiutos kurso užsienio valiutos SF konvertuoti. |
| Ataskaitos kategorija | Šiame laukelyje apibrėžiama savikainos tipo ataskaitų teikimo kategorija. Ataskaitas galima spausdinti pagal ataskaitų kategorijas arba pagal savikainos tipą. |
| Debeto tipas | Pasirinkite, ar savikainos tipas turėtų būti debetuojamas prekei, DK sąskaitai ar tiekėjui. |
| Debeto registravimas | Jei laukelis **Debeto tipas** nustatomas kaip *DK sąskaita*, pasirinkite registravimo aprašą. |
| Debeto sąskaita | Jei laukelis **Debeto tipas** nustatomas kaip *DK sąskaita*, pasirinkite naudojamą DK sąskaitą. |
| Kredito tipas | Pasirinkite, ar šis savikainos tipas turėtų būti kredituojamas prekei, DK sąskaitai ar tiekėjui. |
| Kredito registravimas | Jei laukelis **Kredito tipas** nustatomas kaip *DK sąskaita*, pasirinkite registravimo aprašą. |
| Kredito sąskaita | Jei laukelis **Kredito tipas** nustatomas kaip *DK sąskaita*, pasirinkite naudojamą DK sąskaitą. |
| Tarpuskaitos sąskaita | Pasirinkite savikainos tipo kliringo sąskaitą. Suderinimui rekomenduojame kiekvienam savikainos tipui nurodyti atskirą kliringo sąskaitą. |
| Standartinės savikainos registravimo tipas | Jei naudojate standartinį įkainojimą, pasirinkite registravimo aprašymą. |
| Standartinio išlaidų nuokrypio sąskaita | <p>Jei naudojate standartinį įkainojimą, čia nurodyta sąskaita bus naudojama bet kokiam nuokrypiui registruoti. Šioje sąskaitoje naudojamas iškrovimo kainos paskirstymas puslapyje **Prekių kainos**. Šis paskirstymas sukuriamas naudojant periodinę procedūrą kainoms atnaujinti.</p><p>Pavyzdžiui, standartinė prekės savikaina yra 15,00 USD, FOB – 13,00 USD, o transportavimas 2,00 USD. Atsargoms gavus SF, prekė gaunama už 15,00 USD, bet yra standartinis 2,00 kainos nuokrypis vienai prekei, nes faktinis FOB yra 13,00 USD. Šis nuokrypis registruojamas standartinių kainų nuokrypio sąskaitoje, kuri nustatoma prekės registravimo profilyje. Apskaičiuota transportavimo suma yra 2,00 USD, todėl registruojant atsargų SF nėra nuokrypio. Tačiau gavus SF už transportavimą, transportavimo savikaina yra 2,50 USD vienetui. Todėl nurodytai savikainai registruojamas 0,50 USD nukrypimas. |
| Slenkančio vidurkio nuokrypio sąskaita | <p>Jei naudojate slankiojo vidurkio įkainojimą, čia nurodyta sąskaita bus naudojama bet kokiam nuokrypiui registruoti.</p><p>Pavyzdžiui, apskaičiuota pervežimo suma yra 2,00 USD. Tačiau gavus SF už transportavimą, transportavimo savikaina yra 2,50 USD vienetui. Todėl reikia registruoti 0,50 USD nukrypimą.</p><p>Kai parinktis **Koregavimus registruoti kaip nuokrypį** nustatyta kaip *Taip* puslapyje **Iškrovimo kainos parametrai** visi nukrypimai tarp įvertintos ir faktinės siuntos savikainos bus registruojami čia nurodytoje slankiojo vidurkio nuokrypio sąskaitoje. Kai parinktis **Koregavimus registruoti kaip nuokrypį** nustatyta kaip *Ne*, naudojamos standartinės funkcijos, o nuokrypis taikomas čia nurodytoje atsargų arba slankiojo vidurkio nuokrypio sąskaitoje, priklausomai nuo turimų atsargų.</p> |
| Kredito kaupimo sąskaita | Pasirinkite sąskaitą, kuri naudojama numatomai savikainai kaupti registruojant SF. Šis laukelis naudojamas tik tada, kai parinktis **Naudoti savikainos tipo mokesčio kaupimo sąskaitą** nustatoma kaip *Taip* „FastTab“ skirtuke **Įkainojimas**, skirtuke **Bendra**, esančiame puslapyje **Iškrovimo kainos parametrai**. |
| Kredito sąskaita | Pasirinkite sąskaitą, kuri gaunamų medžiagų transportavimo savikainai, kuriai SF išrašė tiekėjas. Suma registruojama kaip debetas. Korespondentinė sąskaita yra atsargų variacijos sąskaita. Šis registravimas naudojamas tada, kai parinktis **Registruoti DK mokesčių sąskaitoje** nustatyta kaip *Taip* puslapyje **Mokėtinų sumų parametrai**. |
| Nuokrypio sąskaita | Sąskaita, kuri bus naudojama sukauptiems mokesčiams dengti, kai registruojama SF. Šis laukelis naudojamas tik tada, kai parinktis **Naudoti savikainos tipo mokesčio kaupimo sąskaitą** nustatoma kaip *Taip* „FastTab“ skirtuke **Įkainojimas**, skirtuke **Bendra**, esančiame puslapyje **Iškrovimo kainos parametrai**. |

## <a name="vendor-cost-type-groups"></a>Tiekėjo išlaidų tipo grupės

Teikėjo savikainos tipų grupės padeda nustatyti, kaip randami *automatinės savikainos* mokesčiai ir pritaikomi reisui. Tiekėjai, kurių importavimo savikaina yra panaši ir susieta. Pavyzdžiui, visi tiekėjai iš naujų rinkų moka tą pačią muito mokesčio dalį procentais už to paties tipo produktą, kuris perkamas iš nustatytos rinkos.

Tiekėjo savikainos tipo grupes galima išlaikyti perėjus į **Iškrovimo kaina \> Įkainojimo sąranka \> Tiekėjo savikainos tipo grupės**. Puslapyje **Tiekėjo savikainos tipo grupės** pateikiamas tinklelis, kuriame nurodomos visos esamos tiekėjo savikainos tipų grupės. Veiksmų srityje esančius mygtukus galima naudoti eilutėms tinklelyje pridėti, pašalinti ir redaguoti.

Šioje lentelėje apibūdinami galimi kiekvienos tinklelio eilutės laukeliai.

| Laukas | aprašymas |
|---|---|
| Tiekėjo išlaidų tipo grupės | Įveskite unikalų pavadinimą tiekėjo savikainos tipo grupei (pvz., *Naujos rinkos*). |
| aprašymas | Įveskite tiekėjo savikainos tipo grupės aprašymą. Šiame aprašyme galima pateikti duomenis apie mokesčio lygį ar tipą, siejamą su tiekėjų grupe. |

## <a name="item-cost-type-groups"></a>Prekės išlaidų tipo grupės

Prekės savikainos tipo grupės padeda nustatyti, kaip randami *automatinės savikainos* mokesčiai ir pritaikomi reisui. Panašios prekės susiejamos. Pavyzdžiui, visos prekės, kurių muito mokesčio tarifas yra 5 procentai, gali priklausyti konkrečiai savikainos tipų grupei.

Tiekėjo savikainos tipo grupes galima išlaikyti perėjus į **Iškrovimo kaina \> Įkainojimo sąranka \> Tiekėjo savikainos tipo grupės**. Puslapyje **Prekės savikainos tipų grupės** pateikiamas tinklelis, kuriame nurodomos visos esamos prekės savikainos tipų grupės. Veiksmų srityje esančius mygtukus galima naudoti eilutėms tinklelyje pridėti, pašalinti ir redaguoti.

Šioje lentelėje apibūdinami galimi kiekvienos tinklelio eilutės laukeliai.

| Laukas | aprašymas |
|---|---|
| Prekės išlaidų tipo grupės | Įveskite unikalų pavadinimą prekės savikainos tipo grupei (pvz., *Mokestis 5 %*). |
| aprašymas | Įveskite prekės savikainos tipo grupės aprašymą. Šiame aprašyme galima pateikti duomenis apie mokesčio lygį ar tipą, siejamą su prekių grupe. |

> [!NOTE]
> Prekės savikainos tipas yra siejamas su preke laukelyje **Savikainos tipo grupė**, esančiame „FastTab“ **Pirkimas**, kuris yra puslapyje **Išleistas produktas**.

## <a name="transfer-order-cost-type-groups"></a>Perkėlimo užsakymo išlaidų tipų grupės

Perkėlimo užsakymo savikainos tipo grupės padeda nustatyti, kaip randami *automatinės savikainos* mokesčiai. Panašios prekės susiejamos. Pavyzdžiui, visos prekės, kurių muito mokesčio tarifas yra 7 procentai, gali priklausyti konkrečiai savikainos tipų grupei.

Perkėlimo užsakymo savikainos tipo grupes galima išlaikyti perėjus į **Iškrovimo kaina \> Įkainojimo sąranka \> Perkėlimo užsakymo savikainos tipo grupės**. Puslapyje **Perkėlimo užsakymo savikainos tipo grupės** pateikiamas tinklelis, kuriame nurodomos visos esamos perkėlimo užsakymo savikainos tipų grupės. Veiksmų srityje esančius mygtukus galima naudoti eilutėms tinklelyje pridėti, pašalinti ir redaguoti.

Šioje lentelėje apibūdinami galimi kiekvienos tinklelio eilutės nustatymai.

| Laukas | aprašymas |
|---|---|
| Perkėlimo užsakymo išlaidų tipų grupės | Įveskite unikalų pavadinimą perkėlimo užsakymo savikainos tipo grupei (pvz., *Mokestis 7 %*). |
| aprašymas | Įveskite perkėlimo užsakymo savikainos tipo grupės aprašymą. Šiame aprašyme galima pateikti duomenis apie mokesčio lygį ar tipą, siejamą su perkėlimo užsakymo savikainos tipo grupe. |

> [!NOTE]
> Perkėlimo užsakymo savikainos tipas yra siejamas su preke laukelyje **Perkėlimo užsakymo savikainos grupė**, esančiame „FastTab“ **Pirkimas**, kuris yra puslapyje **Išleistas produktas**.

## <a name="cost-templates"></a>Išlaidų šablonai

Savikainos šablonus galima naudoti numatytosioms nustatymų vertėms nustatyti, kurių gali nežinoti savikainos įvertinimą gaunantys naudotojai. Savikainos šablonai gali padėti sumažinti įvertinimo proceso sudėtingumą sumažinant naudotojų pasirinkimus tiksliam įvertinimui gauti.

Norėdami dirbti su savikainos šablonais pereikite į **Iškrovimo savikaina\> Įkainojimo nustatymas \> Savikainos šablonai**. Puslapio **Savikainos šablonai** kairėje esančioje sąrašo srityje rodomi visi dabartiniai savikainos šablonai. Veiksmų srityje esančius mygtukus galima naudoti šablonams pridėti, pašalinti ir redaguoti.

Šioje lentelėje apibūdinami galimi kiekvieno šablono laukeliai.

| Laukas | aprašymas |
|---|---|
| Išlaidų šablonas | Įveskite unikalų savikainos šablono pavadinimą. Pavadinimas paprastai aprašo šablono koeficientą arba savikainos daugiklį. |
| aprašymas | Įveskite savikainos šablono aprašymą. |
| Gabenimo įmonė | Pasirinkite siuntimo įmonės tiekėjo sąskaitą susiejimui su savikainos šablonu. |
| Pristatymo būdas | Pasirinkite pristatymo būdą, kurį turėtų naudoti savikainos šablonas apskaičiavus įvertintą prekės savikainą. Šis laukelis padės apibrėžti automatinę savikaina, siejamą su prekėmis savikainos vertinime. |
| Gabenimo konteinerio tipas | Pasirinkite gabenimo konteinerio tipą susiejimui su savikainos šablonu. Šis laukelis padės apibrėžti automatinę savikaina, siejamą su prekėmis savikainos vertinime. |
| Muitinės tarpininkas | Pasirinkite muitinės brokerį (tiekėją), kuris bus siejamas su sąnaudų šablonu. Šis laukelis padės apibrėžti automatinę savikaina, siejamą su savikainos vertinimu. |
| Koeficientas | Įveskite koeficientą, kuris turi būti taikomas galutiniam prekių savikainos vertinimui. Pavyzdžiui, norėdami prie apskaičiuotos įvertintos savikainos pridėti 10 procentų, įveskite *1,10*. |

## <a name="volumetric-divisors"></a>Tūriniai dalikliai

Tūriniai dalikliai naudojami turiniam svoriui apskaičiuoti. Kiekviena siuntimo / transportavimo įmonė formuluoja savo tūrinius daliklius. Be to, įmonės dalikliai paprastai skiriasi, priklausomai nuo pristatymo būdo. Pavyzdžiui, pristatant oru ir jūra dalikliai labai skiriasi. Įmonė taip pat gali sudėtingiau nustatyti savo taisykles, priklausomai nuo išsiuntimo vietos.

Pavyzdžiui, oru siunčiama pakuotė yra 3 kubinių metrų (m³). Įmonei mokesčiai taikomi pagal tūrinį svorį ir taikomas tūrinis daliklis 6. Šis daliklis dauginamas iš tūrio, kad būtų galima nustatyti tūrinį svorį. Todėl tūrinis svoris šiame pavyzdyje yra 3 × 6 = 18 kilogramų (kg).

Norėdami nustatyti tūrinius daliklius, į **Iškrovimo kaina \>Įkainojimo nustatymas\> Tūriniai dalikliai**. Puslapyje **Tūriniai dalikliai** pateikiamas tinklelis, kuriame išvardyti visi esami tūriniai dalikliai. Veiksmų srityje esančius mygtukus galima naudoti eilutėms tinklelyje pridėti, pašalinti ir redaguoti.

Šioje lentelėje apibūdinami galimi kiekvienos tinklelio eilutės laukeliai.

| Laukas | aprašymas |
|---|---|
| Gabenimo įmonė | Pasirinkite su tūriniu dalikliu susietos siuntimo įmonės tiekėjo sąskaitą. |
| Išlaidų tipo kodas | Pasirinkite savikainos tipo kodą, susietą su tūriniu dalikliu. Naudokite šį laukelį savikainos tipams į ataskaitų rinkinius įtraukti. Ataskaitas galima spausdinti pagal ataskaitų kategorijas arba pagal savikainos tipą. |
| Kilmės uostas | Pasirinkite išvykimo uostą, kuriam taikomas tūrinis daliklis. |
| Tūrinis daliklis | Įveskite eilutei taikomą tūrinio daliklio reikšmę. Jūsų įvesta vertė bus *padauginta* iš kiekvieno paketo tūrio to paketo tūriniam svoriui apibrėžti. |

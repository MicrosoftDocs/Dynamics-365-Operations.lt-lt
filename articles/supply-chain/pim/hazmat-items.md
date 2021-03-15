---
title: Pavojingos medžiagos produktuose, užsakymuose, siuntose ir kroviniuose
description: Šioje temoje paaiškinta kaip nustatyti pavojingų medžiagų ypatybes išleistiems produktams, kaip uždėti atsargų limitus ant pavojingų prekių, ir kaip įtraukti pavojingas medžiagas į pardavimo užsakymą, siuntą ar krovinį.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 3836273b1c782fe80172443f4d4c29001ccea83a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007671"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>Pavojingos medžiagos produktuose, užsakymuose, siuntose ir kroviniuose

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje paaiškinta kaip nustatyti pavojingų medžiagų ypatybes išleistiems produktams, kaip uždėti atsargų limitus ant pavojingų prekių, ir kaip įtraukti pavojingas medžiagas į pardavimo užsakymą, siuntą ar krovinį.

## <a name="set-hazardous-material-specifications-for-products"></a>Nustatyti pavojingų medžiagų specifikacijas produktams

Apibrėžus pavojingų medžiagų reglamentą ir nustačius nuorodos kodus kaip apibrėžta skiltyje [Nustatyti pavojingas medžiagas](hazmat-setup.md), galite susieti šią informaciją su išleistomis prekėmis. Siuntimo tekstas siuntimo dokumentams bus išrašytas iš pavojingų medžiagų informacijos išleistoms prekėms.

Kaip patvirtintos prekės susiejimo su pavojinga medžiaga proceso dalis, turite nurodyti reglamento kodą ir medžiagą. Skirtingi reglamento kodai gali būti susieti su preke, priklausomai nuo transporto modelių, ir galite susieti kelis reglamentus bei medžiagų kodus su kiekviena preke.

Kad nustatytumėte išleistą produktą kaip pavojingą medžiagą, atlikite šiuos veiksmus:

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite ar sukurkite produktą, kad atidarytumėte jo **Išleisto produkto informacija** puslapį.
1. „FastTab” **Tvarkyti atsargas**, parinkčiai **Pavojingos medžiagos** nustatykite **Taip**. Šis parametras identifikuoja elementą kaip pavojingą prekę ir yra naudojamas kai siuntimo dokumentacija atspausdinta.
1. Veiksmų srityje, skirtuke **Tvarkyti atsargas**, grupėje **Atitiktis**, pasirinkite **Prekė su pavojingomis medžiagomis**.
1. Užpildykite puslapį **Prekė su pavojingomis medžiagomis** pasirinktai prekei, naudodami laukus, aprašytus tolimesniuose poskyriuose.

### <a name="item-hazardous-materials-header"></a>Prekių su pavojingomis medžiagomis antraštė

Ši lentelė aprašo laisvus laukus, esančius puslapio **Prekė su pavojingomis medžiagomis** viršuje.

| Laukas | aprašymas |
|---|---|
| Prekės Nr. | Išleistas produktas, su kuriuo dirbate. |
| Reglamento kodas | Pasirinkite pavojingos medžiagos reglamentą, taikomą produktui. Reglamentas apibrėžia kaip yra sukuriamas atspausdintas siuntimo tekstas prekei ir susijusius pristatymo būdus. Po reglamento priskyrimo kodas negali būti redaguojamas šiame puslapyje. Tačiau galite priskirti naują reglamento kodą pasirinkdami funkciją **Naujas**. |
| Medžiagos kodas | (Neprivalomas laukas) Pasirinkite pavojingos medžiagos kodą, taikomą produktui. Medžiagos kodas turi šabloną, kuris apima numatytąsias vertes daugeliui kitų laukų šiame puslapyje. Kai pasirinksite kodą, visos jo pavojingų medžiagų specifikacijos bus nukopijuotos ant dabartinio produkto. Tačiau pirmiausia sistema jus ragina patvirtinti, kad prekės medžiagų duomenys turi būti užpildyti naudojantis medžiagos kodu. |
| Grupės kodas | (Neprivalomas laukas) Pasirinkite pavojingos medžiagos klasifikacijos grupės kodą, taikomą produktui. Kai pasirinksite kodą lauke **Medžiagos kodas**, visos jo pavojingų medžiagų specifikacijos bus nukopijuotos ant dabartinio produkto. Tačiau pirmiausia sistema jus ragina patvirtinti, kad prekės klasės grupė turi būti įrašyta naudojant grupės kodą. |

### <a name="descriptions-fasttab"></a><a name="hazmat-description"></a>„FastTab” „Aprašymai”

Ši lentelė aprašo laisvus laukus, esančius **Aprašymai** „FastTab”.

| Laukas | Aprašymas |
|---|---|
| Tinkamas siuntimo pavadinimas | Įveskite medžiagos standartinį aprašymą, kaip nurodyta taikomam reglamente. Galite pateikti šios reikšmės vertimus **Prekės siuntimo teksto vertimas** „FastTab”, kaip aprašyta kitame skyriuje. |
| Techninis pavadinimas | Pasirinkite medžiagos bendrą pavadinimą. Šis medžiagos pavadinimas gali būti pavadinimu, kurį jūsų įmonė naudoja viduje. |
| Kitu atveju nebūdingas (not-otherwise-specific) | Pasirinkite šį žymės langelį, kad nurodytumėte, jog reikšmė **Tinkamas siuntimo pavadinimas** yra kitu atveju nebūdingas (N.O.S.) prekės siuntimo pavadinimas. Kitu atveju nebūdingas (not-otherwise-specific) siuntimo pavadinimai naudojami panašių cheminių preparatų ir medžiagų grupėms, kurie turi tam tikrus galutinius panaudojimus, bet jie gali būti nenurodyti pagal pavadinimą „hazmat” lentelėje konkrečiame reglamente. |

### <a name="item-ship-text-translation-fasttab"></a>Prekės siuntimo teksto vertimas „FastTab”

**Prekės siuntimo teksto vertimas**” „FastTab” yra tinklelis, kuris rodo reikšmių **Tinkamas siuntimo pavadinimas** vertimus, kurios yra nustatytos pirmine kalba **Aprašymai** „FastTab” . Šie vertimai gali būti naudojami atspausdintame siuntimo tekste viena ar daugiau papildomų kalbų.

Ši lentelė aprašo laisvus laukus, esančius „FastTab” **Prekės siuntimo teksto vertimas**.


| Laukas | Aprašymas |
|---|---|
| Kalba | Kalbos kodas naudojamas eilutėje. Pavyzdžiui, „**pt-br**” nurodo portugalų (brazilų) kalbą. |
| Siuntimo teksto spausdinimas | **Tinkamas siuntimo pavadinimas** reikšmė išversta ta kalba, kuri naudojama eilutėje. |

Kad pridėtumėte ar redaguotumėte vertimą, pasirinkite funkciją **Vertimai** virš tinklelio, kad atidarytumėte **Teksto vertimai** puslapį. Tuomet atlikite vieną iš toliau nurodytų veiksmų.

- Kad pridėtumėte naują vertimą, pasirinkite **Pridėti** funkciją veiksmų srityje. Pasirinkite kalbą, ir tada lauke **Išverstas tekstas**, įveskite verstą tekstą.
- Kad redaguotumėte esamą vertimą, lauke **Kalba** pasirinkite paskirties kalbą, ir redaguokite išverstą tekstą lauke **Išverstas tekstas**, kaip reikalaujama.

### <a name="material-management-fasttab"></a>„<a name="material-management"></a>”„FastTab” „Medžiagų valdymas”

Ši lentelė aprašo laisvus laukus, esančius „FastTab” **Medžiagų valdymas**.

| Laukas | Aprašymas |
|---|---|
| Klasė | Pasirinkite pavojingos medžiagos klasę, kuriai priklauso produktas, kaip apibrėžta atitinkamam reglamente. Turite priskirti ir padalinį, ir klasę kiekvienam produktui, kuriame yra pavojingų medžiagų. |
| aprašymas | Klasės, kuri buvo pasirinkta lauke **Klasė**, aprašymas. Šis laukas skirtas tik skaityti. |
| Padalinys | Pasirinkite pavojingos medžiagos padalinį, kuriam priklauso produktas, kaip apibrėžta atitinkamam reglamente. Padalinys yra klasės pogrupis. Turite priskirti ir padalinį, ir klasę kiekvienam produktui, kuriame yra pavojingų medžiagų. |
| Identifikavimas | Nustatykite pavojingos medžiagos identifikavimo kodą. Paprastai šis kodas yra pagrįstas Jungtinių Tautų (JT) standartu. |
| Pakavimo grupė | Pasirinkite pakavimo grupę, taikomą dabartinei prekei. |
| Aprašymas | Grupės, kuri buvo pasirinkta lauke **Pakavimo grupė**, aprašymas. Šis laukas skirtas tik skaityti. |
| Pakavimo aprašymai | Pasirinkite taikytiną pakavimo aprašymo kodą. Šis kodas nurodo aprašymą, kuriame aprašyta kaip produktas turi būti supakuotas. |
| Pavojingos medžiagos žymos | Pasirinkite kodą, kuris nurodo pavojingų medžiagų žymą, taikytiną produktui. |
| Ribotas kiekis | Pasirinkite **Taip** parinktį, kad praneštumėte bendrą produkto svorį, įtrauktą kiekvienoje įkeltyje ir kiekvienoje įkelties eilutėje. |
| Kiekis | Įveskite pavojingos medžiagos kiekį produkte nurodytu vienetu. Ši vertė bus naudojama apskaičiuoti bendrą pavojingos medžiagos balą kroviniams ir siuntoms, kuriuose yra produktas. |
| Daugiklis | Įveskite daugiklį, kuris yra pritaikomas, kai pavojingos medžiagos balas yra apskaičiuotas kiekvienai įkelties eilutei, kurioje yra produktas. Ši vertė nurodyta taikomajame reglamente, pagal pavojingos medžiagos, esančios produkte, tipą. |
| Vienetas | Pasirinkite matavimo vienetą, taikytiną pavojingos medžiagos kiekiui produkte, kaip nurodyta lauke **Kiekis**. Ši vertė bus naudojama apskaičiuoti bendrą pavojingos medžiagos balą kroviniams ir siuntoms, kuriuose yra produktas. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>Kaip pavojingos medžiagos balas yra apskaičiuojamas

Kelios vertės, nurodytos „FastTab” **Medžiagų valdymas**, produktui, naudojamos apskaičiuoti  *pavojingos medžiagos balą* kiekvienai įkelties eilutei, kurioje yra tas produktas. Balas apskaičiuojamas pagal toliau nurodytą formulę:

Pavojingos medžiagos balas = *&lt;LineQty&gt;* × *&lt;HazmatQty&gt;* × *&lt;UnitConversion&gt;* × *&lt;Multiplier&gt;*

Čia yra formulės raktas:

- *&lt;LineQty&gt;* yra produkto kiekis, nustatytas įkelties eilutei.
- *&lt;HazmatQty&gt;* yra pavojingos medžiagos kiekis, nustatytas produktui lauke **Kiekis**, „FastTab” **Medžiagos valdymas**.
- *&lt;UnitConversion&gt;* yra konvertavimo koeficientas, naudojamas konvertavimui tarp vieneto, naudojamo įkelties eilutės kiekiui, ir vieneto, nustatyto produktui lauke **Vienetas**, „FastTab” **Medžiagų valdymas**.
- *&lt;Multiplier&gt;* yra daugiklis nustatytas produktui lauke **Daugiklis**, „FastTab” **Medžiagos valdymas**.

Šis balas yra paskelbtas kiekvienoje įkelties eilutėje, kurioje yra produktas, kuriame tos vertės yra nurodytos. Kad gautumėte daugiau informacijos, žr. [Siuntos, kuriose yra pavojingų medžiagų](#hazmat-shipments) ir [Įkeltys, kuriose yra pavojingų medžiagų](#hazmat-loads) sekcijas, esančias vėliau šioje temoje.

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>Kaip pavojingos medžiagos svoris yra apskaičiuojamas

Įkeltys ir įkelčių eilutės, į kuriuos įeina produktai, kur parinktis **Ribotas kiekis**, **Medžiagų valdymas** „FastTab”, nustatyta **Taip**, rodys bendrą pavojingos medžiagos svorį, kaip aprašyta [Siuntos, kuriose yra pavojingų medžiagų](#hazmat-shipments) ir [Įkeltys, kuriose yra pavojingų medžiagų](#hazmat-loads) sekcijose, esančiose vėliau šioje temoje. Pavojingos medžiagos svoris yra apskaičiuojamas pagal toliau nurodytą formulę:

Pavojingos medžiagos svoris = *&lt;LineQty&gt;* × *&lt;ProductWeight&gt;* × *&lt;UnitConversion&gt;*

Čia yra formulės raktas:

- *&lt;LineQty&gt;* yra produkto kiekis, nustatytas įkelties eilutei.
- *&lt;ProductWeight&gt;* yra grynasis svoris, nustatytas produktui, pagal atsargų vienetą, nustatytą produktui.
- *&lt;UnitConversion&gt;* yra konvertavimo koeficientas, naudojamas konvertavimui tarp vieneto, naudojamo įkelties eilutės kiekiui, ir atsargų vieneto, naudojamo *&lt;ProductWeight&gt;*.

### <a name="transport-information-fasttab"></a>„FastTab” – „Transportavimo informacija”

Ši lentelė aprašo laisvus laukus, esančius „FastTab” **Transportavimo informacija**.

| Laukas | aprašymas |
|---|---|
| Transportavimo kategorija | Pasirinkite susijusią transportavimo kategoriją. |
| Tunelio kodas | Pasirinkite susijusį tunelio apribojimo kodą prekei. |
| Pavojingos medžiagos sandėliavimas | Pasirinkite nuorodos kodą, naudojamą tvarkyti jūrų transporto krovimą, kai prekė išsiųsta jūrų transportu. |
| Orlaivio tipas | Pasirinkite orlaivio apribojimus, taikomus medžiagai, kai ji išsiųsta oro transportu. |
| Pakavimas - tik krovininiai orlaiviai | Remiantis reikšme, kurią pasirinkote lauke **Orlaivio tipas**, pasirinkite pakavimo instrukcijų kodą, taikomą, kai produktas gali būti išsiųstas tik krovininiu orlaiviu. |
| Pakavimas – keleivinis ir krovininis orlaivis | Remiantis reikšme, kurią pasirinkote lauke **Orlaivio tipas**, pasirinkite pakavimo instrukcijų kodą, taikomą, kai produktas gali būti išsiųstas krovininiu orlaiviu arba keleiviniu orlaiviu. |
| IATA žvaigždutė | Nustatykite šią parinktį į **Taip**, kad nurodytumėte, jog oro transporto specifikacijos, įvestos šiame „FastTab”, yra susijusios su Tarptautinės oro transporto asociacijos (IATA) nustatytu pavojingų prekių standartu. Šis laukas naudojamas tik informaciniais tikslais. |
| Reagavimas į ekstremalias situacijas | Pasirinkite kodą, kuris nurodo instrukcijas medžiagos tvarkymui nepaprastoje padėtyje. |

### <a name="environmental-information-fasttab"></a>„FastTab” – „Aplinkos apsaugos informacija”

Ši lentelė aprašo laisvus laukus, esančius „FastTab” **Aplinkos apsaugos informacija**.

| Laukas | Aprašymas |
|---|---|
| Pavojinga aplinkai | Nustatykite šią pasirinktį į **Taip**, kad nurodytumėte, jog produktas yra pavojingas aplinkai. Naudokite šį lauką jūsų ataskaitų rengimo tikslais. |
| Jūros teršalas | Nustatykite šią pasirinktį į **Taip**, kad nurodytumėte, jog produktas yra jūros teršalas. Naudokite šį lauką jūsų ataskaitų rengimo tikslais. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a>Nustatyti atsargų limitus pavojingiems produktams

Saugumo sumetimais Jums gali tekti riboti bendrą konkretaus produkto, kuris gali būti laikomas atskiroje vietoje, kiekį. Kad nustatytumėte atsargų limitus patvirtintam produktui, atlikite šiuos veiksmus:

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite produktą, kad atidarytumėte **Patvirtinto produkto išsami informacija** puslapį.
1. Veiksmų srityje, skirtuke **Tvarkyti atsargas**, grupėje **Atitiktis**, pasirinkite **Ataskaitų informacija**.
1. Laukuose **Pavojingų atsargų limitas** ir **Pavojingų perspėjimų limitas**, nustatykite atitinkamas vertes pasirinktam produktui.

Ataskaita **Pavojingų medžiagų atsargų limitas** leidžia Jums stebėti pavojingų medžiagų atsargų lygius Jūsų sandėlio vietovėse, kad užtikrintumėte, jog atsargos atitinka saugius limitus, nustatytus čia. Daugiau informacijos žr. [Pavojingų medžiagų atsargų limito ataskaita](hazmat-reports.md#stock-limit-report).

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>Pardavimo užsakymo operacijos, į kurias įtrauktos pavojingos medžiagos

Kad įtrauktumėte produktą, kuris klasifikuojamas kaip pavojinga medžiaga ant pardavimo užsakymo, turite susieti susijusį siuntos vežėją su pardavimo užsakymu. Atidarykite pardavimo užsakymą, ir tada „FastTab” **Pristatymas** nustatykite  **Siuntos vežėjas** ir **Vežėjo paslauga** laukus kaip būtinus.

Siuntos vežėjas taip pat yra susietas su pristatymo būdu. Todėl, įsitikinkite, kad ši informacija yra sulygiuota su pavojingų medžiagų reglamentu. Kitaip tariant, pristatymo būdas, nurodytas pavojingų medžiagų reglamente, turi atitikti specifikacijas, nurodytas pardavimo užsakymo antraštėje. Tokiu būdu reglamentas, siuntos vežėjas bei vežėjo paslauga yra sujungti su siuntos eilutėmis, esančiomis ant pardavimo užsakymo.

Po to, kai pardavimo užsakymas yra užbaigtas ir paruoštas išsiuntimui, jis gali būti išleistas į sandėlį, kad nurodyti perkėlimą tarp pardavimų ir sandėlio operacijų.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a>Siuntos, kuriose yra pavojingų medžiagų

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>Peržiūrėkite pavojingos medžiagos balus kiekvienai siuntimo eilutei

Puslapis **Siuntos informacija** rodo bendrą pavojingos medžiagos svorį ir taškų vertes, kurios buvo apskaičiuotos kiekvienai įkelties eilutei, kuri yra įtraukta į tą siuntą. Norėdami peržiūrėti vertinimus ir svorius, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.
1. Pasirinkite siuntą, kad atidarytumėte **Siuntos informacija** puslapį.
1. „FastTab” **Krovinio eilutės** patikrinkite eilutes. Matysite pavojingos medžiagos apskaičiavimus kiekvienai eilutei šiuose laukuose:

    - **Pavojingos medžiagos taškai** – Šis laukas rodo pavojingos medžiagos vertinimą įkelties eilutei. Vertė yra apskaičiuojama pagal taisykles ir vertes, kurios buvo nustatytos taikomajame reglamente ir patvirtinto produkto sąrankoje. Apskaičiuojamas kiekis vienoje įkelties eilutėje ir nurodomas daugiklis [Medžiagų valdymo sąranka](#material-management) puslapyje patvirtintam produktui.
    - **Riboto kiekio grynasis svoris** – Produktams, pažymėtiems kaip riboto kiekio produktai dėl jų pavojingos medžiagos turinio, šis laukas rodo bendrą pavojingo turinio, esančio ant įkelties eilutės, grynąjį svorį. Apskaičiavimas yra pagrįstas produktais, kurie yra pažymėti kaip pavojingos medžiagos patvirtinto produkto sąrankoje. Jei prekė pažymėta kaip riboto kiekio prekė, apskaičiuojamas kiekis ant kiekvienos įkelties eilutės ir nurodomas svoris [Medžiagų valdymo sąranka](#material-management) puslapyje patvirtintam produktui.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>Suderinamumo tarp pavojingų medžiagų, kurios yra įtrauktos į siuntą, patikrinimas

Sistema gali įvertinti, ar visos pavojingos medžiagos, įtrauktos į siuntą, yra tinkamos išsiųsti kartu. Kad įvertinti suderinamumą, sistema patikrina suderinamumo grupę, kuri yra priskirta kiekvienam produktui, kuris yra įtrauktas į siuntą. Daugiau informacijos žr. [Pavojingų medžiagų suderinamumo grupės](hazmat-setup.md#compatibility-groups).

Norėdami vykdyti suderinamumo tikrinimą, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.
1. Pasirinkite siuntą, kad atidarytumėte **Siuntos informacija** puslapį.
1. Veiksmų srityje, skirtuke **Siuntos**, grupėje **Veiksmai**, pasirinkite **Suderinamumo tikrinimas**.

Gausite pranešimą, kuris jus informuos apie patikros rezultatus.

## <a name="loads-that-include-hazardous-materials"></a><a name="hazmat-loads"></a>Įkeltys, kuriose yra pavojingų medžiagų

### <a name="view-hazardous-material-scores-for-each-load-line"></a>Peržiūrėkite pavojingų medžiagų balus kiekvienai įkelties eilutei

Puslapis **Įkelties informacija** rodo bendrą pavojingų medžiagų svorį ir taškų vertes, kurios buvo apskaičiuotos tai įkelčiai ir kiekvienai įkelties eilutei. Norėdami peržiūrėti vertinimus ir svorius, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Siuntos \> Visos įkeltys**.
1. Pasirinkite įkeltį, kad atidarytumėte **Įkelties informacija** puslapį. (Taip pat galite atidaryti įkelties informaciją, pasirinkę saitą iš susijusios siuntos.)
1. „FastTab” **Įkeltis** galite peržiūrėti bendrus pavojingų medžiagų vertinimus ir svorius visai įkelčiai, patikrinę šiuos laukus:

    - **Pavojingos medžiagos taškai** – Šis laukas rodo pavojingos medžiagos vertinimą vienai įkelčiai. Vertė yra apskaičiuojama pagal taisykles ir vertes, kurios buvo nustatytos taikomajame reglamente ir patvirtinto produkto sąrankoje. Apskaičiuojamas įkelties kiekis ir nurodomas daugiklis [Medžiagų valdymo sąranka](#material-management) puslapyje patvirtintam produktui.
    - **Riboto kiekio grynasis svoris** – Produktams, pažymėtiems kaip riboto kiekio produktai dėl jų pavojingos medžiagos turinio, šis laukas rodo bendrą pavojingo turinio, esančio įkeltyje, grynąjį svorį. Apskaičiavimas yra pagrįstas produktais, kurie yra pažymėti kaip pavojingos medžiagos patvirtinto produkto sąrankoje. Jei prekė pažymėta kaip riboto kiekio prekė, apskaičiuojamas kiekis kiekvienoje įkeltyje ir nurodomas svoris [Medžiagų valdymo sąranka](#material-management) puslapyje patvirtintam produktui.

1. Kad peržiūrėtumėte vertinimus ir svorius atskiroms eilutėms, pasirinkite „FastTab” **Įkelčių eilutės**. Vertės, pateiktos kiekvienai eilutei, yra panašios į vertes, pateiktas visai įkelčiai, kaip aprašyta ankstesniame veiksme.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>Suderinamumo tarp pavojingų medžiagų, kurios yra įtrauktos į įkelt, patikrinimas

Sistema gali įvertinti, ar visos pavojingos medžiagos, įtrauktos į įkeltį, yra tinkamos išsiųsti kartu. Kad įvertinti suderinamumą, sistema patikrina suderinamumo grupę, kuri yra priskirta kiekvienam produktui, kuris yra įtrauktas į įkeltį. Daugiau informacijos žr. [Pavojingų medžiagų suderinamumo grupės](hazmat-setup.md#compatibility-groups).

Norėdami vykdyti suderinamumo tikrinimą, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Siuntos \> Visos įkeltys**.
1. Pasirinkite siuntą, kad atidarytumėte **Įkelties informacija** puslapį. (Taip pat galite atidaryti įkelties informaciją, pasirinkę saitą iš susijusios siuntos.)
1. Veiksmų srityje, skirtuke **Įkeltys**, grupėje **Veiksmai**, pasirinkite **Suderinamumo tikrinimas**.

Gausite pranešimą, kuris jus informuos apie patikros rezultatus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
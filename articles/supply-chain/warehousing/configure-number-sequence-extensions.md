---
title: Konfigūruokite sekų numerį sandėlio srautams
description: Šiame skyriuje pateikta funkcijų apžvalga, kurios pateikia sekos numerio plėtinius licencijos numerio identifikavimo kodui, bangos etiketės identifikavimo kodui, talpyklos identifikavimo kodui ir važtaraščio identifikavimo kodui.
author: GarmMSFT
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSNumberSequenceExt
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: fa4074c23baa74983f4922d2d09d7da81c943bfe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973840"
---
# <a name="configure-number-sequences-for-warehouse-flows"></a>Konfigūruokite sekų numerį sandėlio srautams

[!include [banner](../includes/banner.md)]

*Sekos numerio plėtinių* savybės įtraukia naują konfigūravimo puslapį numerio sekų nustatymui. Jis leidžia lanksčiai konfigūruoti GS1 reguliuojamus identifikavimo kodus, įskaitant GS1 priešdėlius ir patikrina skaitmenis (modulis 10) ir įjungia ilgio ribojimą esančiai numerio sekai.

Standartinio numerio sekos segmentai nėra tinkami GS1 įgyvendinimui, nes nėra skaičiuojamas skaitmeninis tikrinimas, o GS1 bendrovės priešdėlis turi būti atnaujintas rankiniu būdu.

Ši savybė apima tokias funkcijas:

- Važtaraščio identifikavimo kodai gali būti kuriami iš anksto.
- Unikali numerio seka gali būti kuriama serijiniam siuntimo talpyklos kodo (SSCC) numeriams.
- GS1 atitikties numerio seka gali būti kuriama BOL ir SSCC numeriams. Savybės nestandartiniai priedai palaiko licencijos numerio identifikavimo kodą, talpyklos identifikavimo kodą, bangos etiketės identifikavimo kodą ir BOL identifikavimo kodą.
- Licencijos numerio identifikavimo kodo konfigūravimas yra lankstus. Pavyzdžiui, galite įtraukti ar neapimti programos identifikatorių (DI), tokių kaip priekyje esančių nulių (00).

Ši funkcija užtikrina efektyvesnį dėžių etikečių palaikymą ir reguliuoja naujus skaičius, kuriuos sukuria sistema.

## <a name="turn-on-the-number-sequence-extensions-feature"></a>Įjunkite numerio sekos plėtinių funkciją

Prieš naudodami šią funkciją, turite ją įjungti savo sistemoje. Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Numerio sekos plėtiniai*

## <a name="set-up-the-feature"></a>Funkcijos nustatymas

Numerio sekos plėtinių savo sistemoje nustatymui, atlikite šiuos žingsnius.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. **Bendri** skirtuke, **GS1 bendrovės priešdėlio** laukelyje įveskite savo bendrovės GS1 priešdėlį. Ši vertė paveiks visas skaičiaus sekas, kai GS1 priešdėlis yra įtrauktas į segmentą.
1. Jei norite sukurti BOL skaičius bangų etiketėms, **Ataskaitos** skirtuke, pasirinkite **Kurti BOl skaičių spausdinant bangos etiketes** žymimą laukelį.

    > [!NOTE]
    > Šis žymimas laukelis yra prieinamas tik jei funkcija [bangos etiketės spausdinimas](configure-wave-label-printing.md) yra įjungta.

1. Eikite į  **Sandėlio tvarkymas** \> **Sąranka** \> **Skaičiaus sekos plėtiniai**
1. Veiksmų juostoje pasirinkite **Sukurti nustatytąją sąranką**. Sukuriama GS1 atitinkanti BOL numerio seka ir trijų tipų SSCC numerio sekos. Visos šios skaičių sekos apima jūsų bendrovės GS1 priešdėlį.

    Dėl išsamesnės informacijos, kaip tinkinti šiuos nustatytąsias skaičių sekas ir (arba) įtraukit naujas sekas, žiūrėkite kitą skyrių. Galite taip pat pašalinti bet kurias iš šių sekų, jei jų jums nebereikia.

1. Eikite atgal į **Sandėlio tvarkymas \> Sąranka \> Sandėlio tvarkymo parametrai**.
1. **Skaičių sekos** skirtuke, pasirinkite reikiamą skaičių sekos plėtinį tam, kad naudotumėte sukurtus skaičius jūsų licencijos numerio identifikavimo kodams, bangos identifikavimo kodams, talpyklos identifikavimo kodams (tuo atveju, pasirinkite reikiamą **SSCC-18 skaičiaus** seką), ir (arba) BOL identifikavimo kodą (šiuo atveju, pasirinkite **BOL** seką). Pagal nutylėjimą, skaičiaus sekos plėtiniai yra palaikomi tik šiems keturiems identifikavimo kodams.

Kaskart, kai naujas skaičius sukuriamas vienai iš šių skaičių sekų, naudojama nauja logika.

> [!NOTE]
> Jei nepasirenkate skaičiaus sekos plėtinio savo licencijos numerio identifikavimo kodui, bus naudojamos esamos taisyklės licencijos numerio identifikavimo kodo kūrimui. Kitu atveju, bus naudojama jūsų pasirinkta skaičiaus seka. Kiti identifikavimo kodai bus naudojami grynųjų skaičių sekoje, kol jiems nepritaikysite skaičiaus sekos plėtinio.

## <a name="create-and-edit-number-sequences"></a>Sukurkite ir redaguokite skaičių sekas

Ankstesniame skyriuje sukūrėte nustatytąjį skaičiaus sekų rinkinį. Šis skyrius paaiškina, kaip apibrėžiamas skaičių seka. Jis taip pat paaiškina, kaip sukurti tinkintas sekas ir kaip redaguoti nustatytąsias ar tinkintas sekas.

Sukurkite ir redaguokite skaičių sekas atlikdami šiuos žingsnius.

1. Eikite į  **Sandėlio tvarkymas** \> **Sąranka** \> **Skaičiaus sekos plėtiniai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. **Skaičiaus sekos plėtinio** laukelyje įveskite naujos sekos pavadinimą. Lauke **Aprašas** įveskite aprašą.
1. **Segementų** „FastTab“, naudokite mygtukus įrankių juostoje tam, kad surinktumėte skaičiaus formatą pridėdami, pašalindami ir tvarkydami segmentus. **Segmento** laukelyje kiekvienai eilute, priskirkite segmento tipą tam, kad nustatytumėte to segmento turinį ir tikslą. Toliau pateiktoje lentelėje aprašomi esamų segmentų tipai.

    | Segmento tipas | aprašymas |
    |---|---|
    | Pastovus | Šis segmento tipas įtraukia tokį patį teksto turinį kiekvienam sukurtam skaičiui sekoje. **Vertės** laukelyje įveskite norimą tekstą. **Ilgio** laukelis yra automatiškai atnaujinamas pagal jūsų įvesto teksto ilgį **Vertės** laukelyje. |
    | Numeravimas | **Vertės** laukelyje, įveskite skaičiaus ženklą (*\#*) kiekvienam ženklui, kuris turi būti rodomas sukurtoje sekoje. Skaičiaus seka gali sukurti ilgesnius skaičius, tačiau bus rodomi tik labiausiai dešinėje esantys ženklai. **Ilgio** laukelis yra automatiškai atnaujinamas pagal jūsų įvesto skaičiaus ženklus, kuriuos įvedėte **Vertės** laukelyje.<p>Tam, kad atitiktumėte GS1 reikalavimams SSCC-18 skaičiams, įsitikinkite, kad šio segmento ilgis yra 16 atėmus GS1 priešdėlio ilgį.</p> |
    | GS1 prefiksas | Segmento tipas įtraukia vertę, kurią nustatėte **GS1 bendrovės priešdėlio** laukelyje **Sandėlio valdymo parametrų** puslapyje. **Vertės** laukelis rodo vertę, kuri yra nustatyta **Sandėlio valdymo parametrų** puslapyje ir **Ilgio** laukelis rodo ženklų skaičių vertėje. **Vertės** laukelis ir **Ilgio** laukelis yra skirti tik skaityti. |
    | Programos identifikatorius | **Vertės** laukelyje, įveskite taikomą identifikavimo kodą, nurodytą GS1 politikoje šio tipo skaičiaus sekai. Pavyzdžiui, įveskite *00* SSCC arba *420* BOL. **Ilgio** laukelis yra automatiškai atnaujinamas pagal jūsų įvesto identifikavimo kodo ilgį **Vertės** laukelyje. |
    | Pakuotės tipas | Elementams, kurie gali būti aiškiai atpažįstami, šio segmento įvestis įtraukia laukelio vertę iš atitinkamos sekos padailinio grupės(iš **Padalinio seko grupės** puslapio). (Toks elgesys atitinka esančią licencijos numerio identifikavimo kodų logiką). Licencijos numeriai turintys daugelį akcijų laikymo prietaisų (SKU), šiame laukelyje įveda *0* (nulį) pagal nutylėjimą. Šiam segmento tipui, **Vertės** laukelis yra visuomet nustatytas ties *P*, o **Ilgio** laukelis yra nustatytas ties *1*.|
    | Tikrinti skaitmenį | Šis segmento tipas įtraukia tikrinamą skaitmenį, kuris yra apskaičiuotas modulyje 10. (Toks elgesys atitinka esamą logiką licencijos numerio identifikavimo kodams) Šio segmento tipui, **Vertės** laukelis visuomet nustatytas ženklais (*^*), o **Ilgio** laukelis visuomet nustatytas *1*. |

1. Galutinio jūsų skaičiaus formato pavyzdžio peržiūrai, patikrinkite **Formato** laukelį **Segmentų** „FastTab“ apačioje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
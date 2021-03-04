---
title: Kredito valdymo nustatymas
description: Šioje temoje aprašomas nustatymas, kurio reikia kredito valdymui.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d1d33dbbd37daaa75f4b64359194a2328728b27f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445864"
---
# <a name="credit-management-setup"></a>Kredito valdymo nustatymas 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a>Kredito valdymo darbo eigos

Eikite į **Kreditai ir mokėjimų priežiūros \> Nustatymas \>Kreditų valdymo darbo eigos**, kad apibrėžtumėte darbo eigas, kurios naudojamos kredito limito koregavimams valdyti.

- Galite sukurti darbo eigą, kuri leidžia patvirtinti kredito limitų koregavimų paketą vienu patvirtinimu.
- Galite įtraukti darbo eigą eilutės lygiu, kad galėtumėte patvirtinti kredito limito koregavimus atskirai.
- Galite sukurti išleidimo darbo eigą, kuri automatiškai nukreipia sulaikymus į darbo eigos procesą.

## <a name="blocking-rules"></a>Blokavimo taisyklės

### <a name="ranking-payment-terms"></a>Mokėjimo sąlygų reitingavimas

Galite sulaikyti pardavimo užsakymą, jei užsakymo mokėjimo sąlygos neatitinka numatytųjų kliento mokėjimo sąlygų. Tačiau kartais mokėjimo sąlygos skiriasi, bet yra pakankamai panašios, todėl nenorite sulaikyti užsakymo. Galite reitinguoti mokėjimo sąlygas, kad kai kurios jų turėtų vienodą reitingą, o kitos – aukštesnį arba žemesnį.

Jeigu mokėjimo sąlygų reitingavimas aktyvus ir užsakymo mokėjimo sąlygos turi aukštesnį reitingą nei numatytosios kliento mokėjimo sąlygos, pardavimo užsakymas bus sulaikytas.

Norėdami nustatyti mokėjimo sąlygų reitingus, eikite į **Kreditas ir surinkimas \> Sąranka \> Kredito valdymo sąranka \> Mokėjimų sąlygų reitingavimas**  

### <a name="ranking-settlement-discounts"></a>Sudengimo nuolaidų reitingavimas

Galite sulaikyti pardavimo užsakymą, jei užsakymo nuolaida neatitinka numatytosios kliento užsakymo nuolaidos. Tačiau kartais užsakymo nuolaidos skiriasi, bet yra pakankamai panašios, todėl nenorite sulaikyti užsakymo. Galite reitinguoti užsakymo nuolaidas, kad kai kurios jų turėtų vienodą reitingą, o kitos – aukštesnį arba žemesnį.

Jeigu sudengimo nuolaidų reitingavimas aktyvus ir sudengimo nuolaidą turi aukštesnį reitingą nei numatytoji kliento sudengimo nuolaida, pardavimo užsakymas bus sulaikytas.

Norėdami nustatyti mokėjimo sąlygų reitingus, eikite į **Kreditas ir surinkimas \> Sąranka \> Kreditų valdymo sąranka \> Sudengimo nuolaidų reitingavimas**  

## <a name="reasons"></a>Priežastys

Kreditų valdyme naudojamos kelių tipų priežastys.

- Sulaikymo priežastys nurodo, kodėl buvo sulaikytas pardavimo užsakymas.
- Išleidimo priežastis priskiriama užsakymui, kai jis išleistas iš sulaikymo.
- Būsenos priežastis nurodo, kodėl sąskaitos būsena buvo priskirta klientui.

Galite nustatyti priežastis puslapyje **Kreditų valdymo priežastys** (**Kreditas ir surinkimas \> Nustatymas \> Kreditų valdymo sąranka \> Kreditų valdymo priežastys**).

1. Lauke **Priežasties tipas** pasirinkite priežasties tipą: **Sulaikymas**, **Išleidimas** arba **Būsena**.
2. Lauke **Priežastis** įveskite priežasties pavadinimą.
3. Lauke **Aprašas** įveskite priežasties kodo aprašą.

## <a name="credit-management-groups"></a>Kredito valdymo grupės

Kreditų valdymo grupės naudojamos siekiant identifikuoti klientus arba klientų grupes, kurios turi tas pačias kreditų valdymo ypatybes. Pavyzdžiui, kreditų valdymo grupes galima naudoti norint nustatyti klientų blokavimo ir pašalinimo kreditų valdymo taisykles.

Galite kurti kreditų valdymo grupes puslapyje **Kreditų valdymo grupės** (**Kreditas ir surinkimas \> Sąranka> Kredito valdymo sąranka \> Kreditų valdymo grupės**).

1. Pasirinkite **Nauja**, kad sukurtumėte eilutę.
2. Įvesti grupės ID. ID gali sudaryti iki 10 simbolių.
3. Lauke **Aprašas** įveskite grupės aprašą. Pavadinimą gali sudaryti iki 60 simbolių.

Kreditų valdymo grupė priskiriama klientui „FastTab“ **Kreditai ir mokėjimų priežiūra** puslapyje **Visi klientai** (**Gautinos sumos \> Klientai \> Visi klientai**).

## <a name="account-statuses"></a>Sąskaitos būsenos

Galite sukurti sąskaitų būsenas, kad nustatytumėte kliento sąskaitos kredito padėtį. Galite nurodyti būseną ir jos poveikį SF išrašymui ir sulaikyto pristatymo procesams. Sąskaitų būsenas taip pat galima naudoti norint nustatyti kliento blokavimo taisykles.

Galite sukurti sąskaitos būsenas puslapyje **Sąskaitų būsenos** (**Kreditas ir surinkimas \> Sąranka > Kredito valdymo sąranka \> Sąskaitų būsenos**).

1. Įtraukite sąskaitos būseną ir įveskite aprašą, nurodantį kliento kredito padėtį. Pavyzdžiui, naudokite **Įprastas**, norėdami nurodyti, kad kliento padėtis yra gera, o atidarytiems užsakymams taikomas standartinis kreditų valdymo apdorojimas.
2. Laukuose **SF išrašymas** ir **Sulaikytas pristatymas** pasirinkite sulaikymo, kuris turėtų būti taikomas klientams, turintiems šios sąskaitos būseną, tipą. Galite sulaikyti visus apdorojus, sulaikyti tik SF apdorojimą arba nesulaikyti jokio apdorojimo, kai taikomos kreditų limito taisyklės.

## <a name="scoring-groups"></a>Rezultatų grupės

Galite nustatyti vertinimo grupes, kad nustatytumėte rizikos faktorius ir kriterijus, naudojamus jiems išmatuoti. Kai informacija apie klientą taikoma vertinimo grupei, apskaičiuojamas kiekvieno rizikos veiksnio balas, pagal kurį klientas įtraukiamas į rizikos grupę. Rizikos grupė gali būti naudojama kredito tinkamumui nustatyti ir automatiniam kredito limitų apskaičiavimui.

Galite sukurti vertinimo grupes puslapyje **Vertinimo grupės** (**Kreditas ir surinkimas \> Sąranka \> Kredito valdymo sąranka \> Rizika \> Vertinimo grupės**).

1. Sukurkite vertinimo grupę ir įveskite jos pavadinimą.
2. Norėdami smulkiau aprašyti vertinimo grupę, įveskite aprašą.
3. Pasirinkti grupės tipą. Yra aštuoni iš anksto nustatyti tipai. Taip pat galite pasirinkti parinktį **Vartotojo nustatyta**, kuri apibrėžia jūsų organizacijai labiau tinkantį grupės tipą.
4. Pasirinkti vertinimo tipą, nurodantį, kaip vertinimo grupė apskaičiuoja rizikos balą. Galimos toliau nurodytos parinktys.

    - **Intervalas** – naudokite šią parinktį, kad nurodytumėte reikšmių intervalą, kuris turi būti naudojamas skaičiuojant balą.
    - **Vartotojo nustatyta** – naudokite šią parinktį, kad rankiniu būdu apibrėžtumėte reikšmių, kurios turi būti naudojamos balui, sąrašą.

5. Jei pasirinkote **Intervalas** kaip vertinimo tipą, įtraukite eilutes, kad apibrėžtumėte reikšmių intervalą ir atitinkamus balus.

    1. Lauke **Vertė nuo** nurodykite žemiausią intervalo reikšmę.
    2. Lauke **Vertė iki** nurodykite aukščiausią intervalo reikšmę.
    3. Lauke **Balas** įveskite balą, kuris turi būti priskirtas, kai pateikta reikšmė yra intervale „nuo iki“.

    Jei pasirinkote **Vartotojo nustatyta** kaip vertinimo tipą, įtraukite eilutes, kad apibrėžtumėte vartotojo nustatytas reikšmes ir atitinkamus balus.

    1. Lauke **Reikšmė** įveskite vartotojo nustatytą reikšmę, kuri turi būti pateikta kliento informacijoje.
    2. Lauke **Balas** įveskite balą, kuris turi būti priskirtas, kai pateikta reikšmė yra intervale „nuo iki“.

## <a name="risk-classification"></a>Rizikos klasifikacija

Galite apibrėžti rizikos įvertinimus, kuriuos galima priskirti klientams pagal jų rizikos balą. Rizikos balas apskaičiuojamas palyginant kliento informaciją su kiekviena vertinimo grupe. Balai susumuojami, o bendras rezultatas palyginamas su rizikos grupės reikšmėmis, nustatytomis siekiant identifikuoti rizikos grupę, kuriai priklauso klientas. Tada rizikos grupės balas naudojamas nustatyti kliento kredito valdymo blokavimo ir pašalinimo taisykles.

Rizikos grupes galite nustatyti puslapyje **Rizikos įvertinimai** (**Kreditas ir surinkimas \> Sąranka \> Kredito valdymo sąranka \> Rizika \> Rizikos klasifikacija**).

1. Įveskite rizikos grupės ID.
2. Norėdami smulkiau paaiškinti rizikos grupę, įveskite aprašą.
3. Įveskite balų intervalą, naudojamą nustatyti, kurie klientai priklauso rizikos grupei.
4. Pasirinkite rizikos grupės indikatorių, kad nurodytumėte simbolį, reprezentuojantį rizikos grupę.

## <a name="guaranteeinsurance-types"></a>Garantijos / draudimo tipai

Galite nustatyti garantijos / draudimo tipus puslapyje **Garantijos / draudimo tipai** (**Kreditas ir surinkimas \> Sąranka \> Kredito valdymo sąranka \> Draudimas ir garantijos \> Garantijos ir draudimo tipai**).

1. Įveskite garantą arba draudimo tipą, kuris identifikuoja laiduotojo arba draudimo brokerio pavadinimą.
2. Įveskite aprašą, aprašantį garantijos / draudimo brokerį.

## <a name="coverage-types"></a>Padengimo tipai

Padengimo tipai gali būti naudojami siekiant smulkiau klasifikuoti draudimo polisus. Jie negali būti naudojami su garantijomis.

Galite įtraukti padengimo tipus puslapyje **Padengimo tipai** (**Kreditas ir surinkimas \> Sąranka \> Kredito valdymo sąranka \> Draudimas ir garantijos \> Padengimo tipai**).

1. Įveskite padengimo tipą, kad identifikuotumėte padengimo tipą, kuris turėtų būti įtrauktas kaip draudimas arba garantija.
2. Įvesti aprašą, aprašantį padengimo tipą.

## <a name="automatic-credit-limits"></a>Automatiniai kredito limitai

Galite sukurti automatinių kredito limitų kriterijus puslapyje **Automatiniai kredito limitai** (**Kreditas ir surinkimas \>Sąranka \> Kredito valdymo sąranka \> Rizika \> Automatiniai kredito limitai**).

1. Pasirinkite rizikos grupę, kuriai reikia priskirti automatinį kredito limitą.
2. Pasirinkite automatinio kredito limito valiutą. Galite sukurti kelis automatinius kreditų limitus skirtingomis valiutomis toje pačioje rizikos grupėje.
3. Įveskite įplaukų sumą, nurodančią maksimalias įmonės įplaukas, kurios gali būti naudojamos šiam automatiniam kredito limitui. Kai kredito limitai sukurti, įplaukų suma palyginama su įplaukų reikšme, randama puslapyje **Finansai** (**Gautinos sumos \> Visi klientai \> Pasirinkti klientą \> Bendri \> Statistika \> Finansai**). Sistema naudoja naujausią reikšmę skyriuje **Peržiūra**.

Atlikite toliau nurodytus veiksmus, kad įtrauktumėte eilutes, kurios nurodo kredito limitą, kuri bus sugeneruota pagal pasirinktus kriterijus.

1. Pasirinkite vertinimo grupę, kuri apibrėžia kliento informaciją, kuri turėtų būti naudojama skaičiuojant kredito limitą.
2. Pasirinkite palyginimo operatorių, nurodantį, kaip turėtų būti įvertinama vertinimo grupės informacija.
3. Įveskite reikšmę, kuri turėtų būti palyginama su vertinimo grupei nurodyta reikšme.
4. Įveskite kredito limitą, kuris turėtų būti priskirtas, jei kliento informacija atitinka reikšmę, nurodytą vertinimo grupėje. Pavyzdžiui, kuriate automatinį kredito limitą vertinimo grupei, kurios balas **Žemas**. Jei verslo metai yra viena iš vertinimo grupių, galite nurodyti vieną eilutę, kuri priskiria 100 000 kredito limitą, jei klientas versle dirba penkerius metus, ir kitą eilutę, kuri priskiria 200 000 kredito limitą, jei klientas versle dirba 10 metų.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
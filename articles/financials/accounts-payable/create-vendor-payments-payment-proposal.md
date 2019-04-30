---
title: Tiekėjo mokėjimų kūrimas naudojant mokėjimo pasiūlymą
description: Šioje temoje apžvelgiamos mokėjimo pasiūlymų parinktys ir pateikiami keli pavyzdžiai, kuriais rodoma, kaip mokėjimo pasiūlymai veikia.
author: abruer
manager: AnnBe
ms.date: 04/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c3d2b6ecae1481fd9b979e5d4ced217a67f5aa
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/25/2019
ms.locfileid: "896861"
---
# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Tiekėjo mokėjimų kūrimas naudojant mokėjimo pasiūlymą

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiamos mokėjimo pasiūlymų parinktys ir pateikiami keli pavyzdžiai, kuriais rodoma, kaip mokėjimo pasiūlymai veikia. Mokėjimo pasiūlymai dažnai naudojami norint sukurti tiekėjų mokėjimus, nes užklausą galima naudoti norint greitai pasirinkti tiekėjų sąskaitas apmokėjimui pagal tokius kriterijus kaip terminas ir nuolaida. 

Įmonės dažnai naudoja mokėjimo pasiūlymus sukurti tiekėjų mokėjimus, nes mokėjimo pasiūlymo užklausą galima naudoti greitai pasirinkti tiekėjų sąskaitas apmokėjimui pagal terminą, nuolaidą ir kitus kriterijus. 

Mokėjimo pasiūlymo užklausoje yra įvairių skirtukų, kurių kiekvienas turi skirtingus variantus pasirenkant sąskaitas apmokėjimui. Skirtuke **Parametrai** yra dažniausiai įmonėse naudojami variantai. Skirtuke **Įtrauktini įrašai** galite nurodyti SF ar tiekėjus, kuriuos reikia įtraukti į mokėjimą, nustatydami įvairias savybes. Pavyzdžiui, jei norite sumokėti tik tam tikrai tiekėjų grupei, galite nustatyti tiekėjų filtrą. Ši funkcija yra dažnai naudojama pasirinkti sąskaitas pagal konkretų mokėjimo būdą. Pavyzdžiui, jei nustatysite filtrą, kur **Apmokėjimo būdas**  =  **Čekis**, apmokėjimui bus atrinktos tik SF, kurių pasirinktas tas mokėjimo būdas, su sąlyga, kad jos taip pat atitinka kitus užklausos kriterijus. **Išplėstinių parametrų** skirtuke yra papildomų variantų, bet kai kurie jų gali netikti jūsų organizacijai. Pavyzdžiui, šiame skirtuke yra centralizuotas sąskaitų mokėjimas.

## <a name="parameters"></a>Parametrai
-   **Pasirinkti sąskaitas pagal** – SF, patenkančias į datų intervalą, nurodytą laukuose **Pradžios data** ir **Pabaigos data**, galima pasirinkti pagal terminą, mokėjimo nuolaidos datą arba pagal abi parinktis. Jei naudojate mokėjimo nuolaidos datą, sistema pirmiausia ieško SF, kurių mokėjimo nuolaidos data patenka į intervalą tarp pradžios ir pabaigos datų. Tada sistema nustato, ar sąskaita faktūra yra tinkama nuolaidai, naudodama sesijos datą patikrinti, ar nuolaidos data jau praėjo.
-   **Nuo** ir **Iki** – sąskaitos faktūros, kurių terminas arba nuolaidos data per šį laikotarpį yra pasirinktos apmokėjimui.
-   **Minimali mokėjimo data** – įveskite minimalaus mokėjimo datą. Pavyzdžiui, laukai **Pradžios data** ir **Pabaigos data** nurodo intervalą nuo rugsėjo 1 d. iki rugsėjo 10 d., o minimali mokėjimo data yra rugsėjo 5 d. Tokiu atveju visų SF, kurių terminas yra nuo rugsėjo 1 d. iki rugsėjo 5 d., mokėjimo data yra rugsėjo 5 d. Tačiau visų SF, kurių terminas yra nuo rugsėjo 5 d. iki rugsėjo 10 d., mokėjimo data yra lygi kiekvienos SF terminui.
-   **Sumos riba** – įveskite maksimalią bendrą visų mokėjimų sumą.
-   **Sukurti mokėjimus be sąskaitos faktūros peržiūros** – jei nustatysite šią parinktį į **Taip**, mokėjimai bus sukurti iš karto puslapyje **Tiekėjo mokėjimai**. Puslapis **Mokėjimo pasiūlymas** bus praleistas. Todėl mokėjimai bus sukurti daug greičiau. Mokėjimus galima redaguoti **Tiekėjo mokėjimų** puslapyje. Arba galite grįžti į **Mokėjimo pasiūlymų** puslapį naudodami mygtuką **Redaguoti sąskaitas pasirinktam mokėjimui**.

## <a name="advanced-options"></a>Išplėstinės parinktys
- **Patikrinti tiekėjo balansą** – jei ši parinktis yra nustatyta **Taip**, prieš bet kurios sąskaitos faktūros apmokėjimą sistema tikrina, ar tiekėjas neturi debeto likučio. Jei tiekėjas turi debeto likutį, mokėjimas nesukuriamas. Pavyzdžiui, tiekėjas gali turėti kredito pažymų arba mokėjimų, kurie buvo užregistruoti bet dar nesudengti. Tokiais atvejais tiekėjui neturėtų būti apmokama. Vietoj to, kredito atmintines arba mokėjimus reikia sudengti pagal neapmokėtas sąskaitas faktūras.
- **Ištrinti neigiamus mokėjimus** – ši parinktis veikia kitaip, priklausomai nuo to, ar mokėjimai atliekami pagal atskiras sąskaitas ar sąskaitų faktūrų, kurios atitinka mokėjimo kriterijus, sumą. Toks elgesys yra apibrėžiamas pagal mokėjimo metodą.
- **Apmokėjimas pagal kiekvieną sąskaitą faktūrą** – jei **Ištrinti neigiamus mokėjimus** parinktis nustatyta **Taip** ir tiekėjui yra neapmokėta sąskaita faktūra, apmokėjimui pasirenkama tik ši sąskaita faktūra. Esamas mokėjimas pagal sąskaitą faktūrą nesudengiamas. Jei **Ištrinti neigiamus mokėjimus** parinktis yra nustatyta **Ne**, ir sąskaita faktūra ir mokėjimas nesudengtas, sąskaita faktūra ir mokėjimas atrenkami mokėjimui. Mokėjimas sukuriamas mokėjimui, o grąžinimas (neigiamas mokėjimas) sukuriamas mokėjimui.
- **Apmokėjimas už sąskaitų sumą** – jei **Ištrinti neigiamus mokėjimus** parinktis nustatyta **Taip** ir tiekėjui yra neapmokėta sąskaita faktūra, neapmokėta sąskaita faktūra ir mokėjimas pasirenkami apmokėjimui, o jų sumos sudedamos, sudarant galutinę mokėjimo sumą. Vienintelė išimtis – jei suma susidaro grąžinant mokėjimą. Šiuo atveju nepasirenkama nei sąskaita faktūra, nei mokėjimas. Jei **Ištrinti neigiamus mokėjimus** parinktis nustatyta **Ne** ir sąskaita faktūra ir mokėjimas nesudengtas, sąskaita faktūra ir mokėjimas atrenkami mokėjimui, o jų sumos sudedamos, sudarant galutinę mokėjimo sumą.
- **Spausdinti tik pranešimą** – nustatykite šią parinktį **Taip**, jei norite pamatyti mokėjimo pasiūlymo ataskaitos rezultatus, nesukuriant jokių mokėjimų.
- **Įtraukti tiekėjo sąskaitas iš kitų juridinių asmenų** – jei jūsų įmonė turi centralizuotą mokėjimo procesą, o mokėjimo pasiūlymas turėtų apimti sąskaitas iš kitų juridinių asmenų, kurie yra įtraukti į paieškos kriterijus, nustatykite šią parinktį **Taip**.
- **Pasiūlyti atskirą tiekėjo mokėjimą juridiniam asmeniui** – jei ši parinktis yra nustatyta **Taip**, kiekvienam juridiniam asmeniui vienam tiekėjui atskira sukuriama išmoka. Tiekėjas mokėjimui yra tiekėjas iš kiekvieno juridinio asmens sąskaitos. Jei ši parinktis yra nustatyta **Ne**, ir tas pats tiekėjas turi sąskaitas iš kelių juridinių asmenų, sukuriamas pasirinktų sąskaitų faktūrų visose pasirinktose įmonėse sumos mokėjimas. Tiekėjas mokėjimui yra esamo juridinio asmens tiekėjas. Jei esamoje įmonėje nėra tiekėjo sąskaitos, bus naudojama pirmosios apmokėtos sąskaitos faktūros tiekėjo sąskaita.
- **Mokėjimo valiuta** – šiame lauke nurodoma valiuta, kuria atliekami visi sukurti mokėjimai. Jeigu valiuta nenurodyta, kiekviena SF apmokama SF valiuta.
- **Mokėjimo savaitės diena** – nurodykite savaitės dieną, kurią turėtų būti atliekamas mokėjimas. Šis laukas naudojamas tik tada, kai yra nustatytas visų sąskaitų apmokėjimas tam tikrą savaitės dieną.
- **Korespondentinės sąskaitos tipas** ir **Korespondentinė sąskaita** – nustatykite šiuos laukus, kai norite nurodyti konkretų sąskaitos tipą (pvz., **Didžioji knyga** arba **Bankas**) ir korespondentinę sąskaitą (pvz., specialią banko sąskaitą). SF apmokėjimo metodas nurodo numatytąjį korespondentinės sąskaitos tipą ir korespondentinę sąskaitą, tačiau šiuos laukus galite naudoti norėdami perrašyti numatytąsias reikšmes.
- **Susumuoto mokėjimo data** – naudojama tik tada, kai mokėjimo būdo laukas **Laikotarpis** yra nustatytas į **Bendras**. Jeigu nurodyta data, visi mokėjimai sukuriami šiai dienai. **Minimalios mokėjimo datos** laukas yra ignoruojamas.
- **Papildomi filtrai** – „FastTab“ **Įtrauktini įrašai** galite nurodyti papildomus kriterijus. Pavyzdžiui, jei norite sumokėti tik tam tikrai tiekėjų grupei, galite nustatyti tiekėjų filtrą. Ši funkcija yra dažnai naudojama pasirinkti sąskaitas pagal konkretų mokėjimo būdą. Pavyzdžiui, jei nustatysite filtrą, kur **Apmokėjimo būdas**  =  **Čekis**, apmokėjimui bus atrinktos tik SF, kurių pasirinktas tas mokėjimo būdas, su sąlyga, kad jos taip pat atitinka kitus užklausos kriterijus.

## <a name="scenarios"></a>Scenarijai

| Tiekėjas | PVM sąskaita faktūra | Data | Iš viso su PVM | Terminas | Mokėjimo nuolaidos data | Mokėjimo nuolaidos suma |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | Birželio 15 d.      | 500,00         | Liepos 15 d.  | Birželio 29 d.            | 10,00                |
| 3050   | 1002    | Birželio 20 d.      | 600,00         | Liepos 20 d.  | Liepos 4 d.             | 12.00                |
| 3075   | 1003    | Birželio 15 d.      | 250,00         | Birželio 29 d.  |                    | 0,00                 |
| 3100   | 1004    | Birželio 17 d.      | 100,00         | Liepos 17 d.  | Liepos 1 d.             | 1.00                 |

Liepos 1 d. Aprilė moka tiekėjams. Ji naudoja mokėjimo pasiūlymą, kad būtų galima efektyviau atlikti šią užduotį.

### <a name="option-1-by-cash-discount"></a>1 variantas: pagal nuolaidą

Aprilė pasirenka  **Nuolaidą** kaip pasiūlymo tipą. Ji įveda datos intervalą nuo birželio 26 d. iki liepos 10 d. Šios SF bus įtrauktos į pasiūlymą:

-   1002, nes nuolaidos data liepos 4 d. yra mokėjimo datų intervale.
-   1004, nes nuolaidos data liepos 1 d. yra mokėjimo datų intervale.

Šios sąskaitos faktūros nebus įtrauktos į pasiūlymą:

-   1001, nes nuolaida data birželio 29 d. jau praėjo, todėl ši SF nebetinka nuolaidai.
-   1003, nes ši SF neturi nuolaidos datos.

### <a name="option-2-by-due-date"></a>2 variantas: iki mokėjimo termino

Aprilė pasirenka **Pagal terminą** kaip pasiūlymo tipą.  Ji įveda datos intervalą nuo birželio 26 d. iki liepos 10 d. Šios SF bus įtrauktos į pasiūlymą:

-   1003, nes terminas liepos 29 d. yra mokėjimo datų intervale.

Šios sąskaitos faktūros nebus įtrauktos į pasiūlymą:

-   1001, nes terminas liepos 15 d. yra ne mokėjimo datų intervale.
-   1002, nes terminas liepos 20 d. yra ne mokėjimo datų intervale.
-   1004, nes terminas liepos 17 d. yra ne mokėjimo datų intervale.

### <a name="option-3-by-due-date-and-cash-discount"></a>3 variantas: pagal terminą ir nuolaidą

Aprilė pasirenka **Terminas ir nuolaida** kaip pasiūlymo tipą. Ji įveda datos intervalą nuo birželio 26 d. iki liepos 10 d. Šios SF bus įtrauktos į pasiūlymą:

-   1003, nes terminas liepos 29 d. yra mokėjimo datų intervale.
-   1002, nes nuolaidos data liepos 4 d. yra mokėjimo datų intervale.
-   1004, nes nuolaidos data liepos 1 d. yra mokėjimo datų intervale.

Šios sąskaitos faktūros nebus įtrauktos į pasiūlymą:

-   1001, nes nuolaida data birželio 29 d. jau praėjo, todėl ši SF nebetinka nuolaidai, o terminas liepos 15 d. taip pat yra ne mokėjimo datų intervale.

## <a name="country-specific-considerations"></a>Šaliai būdingos aplinkybės
### <a name="norway"></a>Norvegija

#### <a name="dimension-control"></a>Dimensijos valdiklis

Dimensijų valdymas suteikia galimybę kontroliuoti sugeneruotų eilučių grupavimą pagal mokėjimo pasiūlymą ir nustatyti numatytąsias dimensijas pagal finansines dimensijas, naudojamas taikomose SF. Norvegijos šalies kontekste kiekvienam mokėjimo būdui priskiriamas finansinės dimensijos skirtukas kuriame galite aktyvinti dimensijų valdymą ir įgalinti kiekvienos dimensijos grupavimą. Galima naudoti šias pasirinktis.

-   Lauko **Dimensijų valdymas** naudoti negalima. Mokėjimo pasiūlymas veikia taip, kaip bet kurioje kitoje šalyje.
-   Laukas **Dimensijų valdymas** yra suaktyvinamas nenustatant dimensijų. Mokėjimo pasiūlymas bus sukurtas neatsižvelgiant į dimensijas. Sukurta operacija iš taikomo įrašo neperima jokių dimensijų.
-   Laukas **Dimensijų valdymas** yra suaktyvinamas ir įjungiamos dimensijos. Dabar galite nustatyti, kaip dimensijos kopijuojamos į žurnalą. Pavyzdžiui: • norėdami kurti verslo struktūros vieneto mokėjimo metodo mokėjimo pasiūlymą, pažymėkite žymės langelį **BusinessUnit**, • Norėdami kurti išlaidų centro mokėjimo metodo mokėjimo pasiūlymą, pažymėkite žymės langelį **Išlaidų centras**.

> [[!NOTE]
> Jei trečiojoje parinktyje pasirinkote daugiau nei vieną dimensiją, sukuriamas to dimensijų derinio mokėjimo pasiūlymas.

#### <a name="bank-account-selection"></a>Banko kodo pasirinkimas

Galite nustatyti mokėjimo metodo standartinę debeto mokėjimo sąskaitą nepriklausomai nuo šalies. Tai bus nustatyta mokėjimo eilutėse, kurias sugeneruos pasiūlymas. Naudodami banko kodo funkciją, galite nurodyti kelis debeto banko kodus, kuriuos valdytų dimensija, valiuta arba jų derinys, kad būtų naudojami skirtingi debeto banko kodai, atsižvelgiant į kiekvieną derinį. Šias kombinacijas galite nustatyti puslapyje **Mokėjimų metodai**, naudodami mygtuką  **Banko kodai**, skirtą kiekvienam mokėjimo metodui, kurio **Registravimo sąskaitos tipas** =  **Bankas**.




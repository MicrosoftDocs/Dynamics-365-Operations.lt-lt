---
title: Elemento konsolidavimas - vietos naudojimas
description: Šiame temoje pateikta informacija apie funkcijas, kurios palengvina sandėlio vadovų vietų kiekio naudojimo peržiūrą ir filtravimą sandėlyje. Vadovai gali pasirinkti vietas ir sukurti inventoriaus judėjimo darbą tiesiai iš elemento konsolidavimo puslapio į konsoliduotus elementus ir taip pagerinti sandėlio vietos naudojimą.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a328b20c1cfb2fc376ab4656c64cf585a5aa015
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433918"
---
# <a name="item-consolidation---location-utilization"></a>Elemento konsolidavimas - vietos naudojimas

[!include [banner](../includes/banner.md)]

Šiame temoje pateikta informacija apie funkcijas, kurios palengvina sandėlio vadovų vietų kiekio naudojimo peržiūrą ir filtravimą sandėlyje. Vadovai gali pasirinkti vietas ir sukurti inventoriaus judėjimo darbą tiesiai iš elemento **Elemento konsolidavimo** puslapio į konsoliduotus elementus ir taip pagerinti sandėlio vietos naudojimą.

## <a name="turn-on-the-features"></a>Savybių įjungimas

Prieš pradedant naudoti šiame skyriuje aprašytas savybes, privalote įjungti jas savo sistemoje. Administratoriai gali naudoti [Savybių valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo srityje tam, kad patikrintų savybių būseną ir jas įjungtų, jei jos būtinos. Įjunkite toliau pateiktas savybes jų išvardijimo tvarka. (Abi savybės yra skirtos **Sandėlio valdymo** moduliui.)

1. Sandėlio vietos būsena
2. Prekės konsolidacijos vietos naudojimas

## <a name="warehouse-location-status"></a>Sandėlio vietos būsena

*Sandėlio vietos būsenos* savybė įtraukia keturis naujus laukelius į **Vietos** puslapį tam, kad būtų sekama papildoma informacija apie esamą vietos būseną:

- **Prekės numeris** – Prekė, kuri šiuo metu yra vietoje. Jei vieta turi keletą elementų, šis laukelis bus tuščias.
- **Paskutinė veiklos data ir laikas** – Paskutinės sandėlio operacijos, atliktos su vieta, laiko žyma.
- **Skirstymo pagal terminus data** – Vietos atsargų įvežimo į sandėlį data. Šie duomenys apskaičiuojami pagal licencijos numerio amžiaus duomenis. Nepaisant to, kad šie duomenys yra tikslųs licencijos numerio sekimo vietoms, jie gali būti netikslūs vietoms, kurių licencijos numeris neseka.
- **Vietos būsena** – Vietos būsena. Dėl prieinamų verčių:

    - **Nenustatyta** – Vietos profilis neseka būsenos. Todėl dabartinė būsena yra nežinoma.
    - **Tuščia** – Vietoje šiuo metu nėra jokio inventoriaus.
    - **Paėmimas** – Siunčiami pervedimai buvo pradėti pagal vietą, kuri galiausiai buvo tuščia.
    - **Laikymas** – Tik įeinantys pervedimai buvo atlikti, nes vieta buvo tuščia.

Šie laukeliai leidžia sandėlio vadovams geriau matyti vietų sandėlyje būseną. Jie taip pat leidžia pateikti geresnes ataskaitas ir pritaikyti filtrus.

## <a name="set-up-item-consolidation-and-location-utilization"></a>Nustatyto elemento konsolidavimas ir vietos naudojimas

Šis skyrius aprašo instrukcijas, kaip parengti sistemą, kuri naudoja konsoliduotą elementą ir vietos naudojimą. Procedūros naudoja paprastas vertes iš standartinių demonstracijos duomenų. Jei planuojate dirbti per visą pavyzdžio scenarijų, kuris pateiktas tolesėje temoje, pasirinkite **USMF** juridinį subjektą (kuriame yra standartiniai demonstracijos duomenys) ir sukurkite visus įrašus aprašytus šiame skyriuje. Jei neplanuojate dirbti su visu pavyzdiniu scenarijumi, čia pateiktos vertės gali būti laikomos nustatymų tipų pavyzdžiais, kuriuos privalote pabaigti tam, kad naudotumėte savybes.

### <a name="released-product"></a>Patvirtintas produktas

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.
1. **Elemento skaičiaus** laukelyje, pasirinkite *M9201* ir atidarykite informacijos puslapį.
1. Veiksmų juostoje, **Inventoriaus valdymo** skirtuke, **Sandėlio** grupėje, pasirinkite **Fiziniai matmenys**.
1. **Fiziniai matmenys** lange, veiksmų juostoje pasirinkite **Naujas**.

    Nauja eilutė pridedama prie tinklelio. **Elemento skaičiaus** laukelis nustatomas iš naujo.

1. **Padalinio** laukelyje pasirinkite *ea*. Likę laukeliai linijoje yra nustatomi automatiškai.
1. Pasirinkite **Išsaugoti** ir uždarykite puslapį.

### <a name="location-profile"></a>Vietos profilis

1. Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlys \> Vietos profiliai**.
1. Vietų profilių sąraše, pasirinkite **FLOOR-05**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. **Bendri** „FastTab“, įsitikinkite, kad abi toliau pateiktos parinktys yra nustatytos į *Taip*:

    - Įgalinti prekę vietoje
    - Įgalinti vietos būseną

1. Pasirinkite **Įrašyti**.

    > [!IMPORTANT]
    > Jei **Įjungti elementą vietoje** ir **Įjungti vietos būseną** parinktys jau buvo nustatytos į *Taip*, praleiskite laukiančias instrukcijas **Matmenų** nustatymui „FastTab“ 10 žingsnyje. Jei parinktys dar nėra nustatytos į *Taip*, turite vykdyti nuolatinį **Sandėlio valdymo** modulio tikrinimą po rankinio jų nustatymo. Šiuo atveju, atlikite kitą žingsnį.

1. Nuolatinio tikrinimo vykdymui, eikite į **Sistemos administravimas \> Periodinės užduotys \> Duomenš bazę \> Periodinis tikrinimas**.
1. **Nuolatinio tikrinimo** teksto laukelyje, nustatykite šias vertes:

    - **Modulis:** *Sandėlio valdymas*
    - **Tikrinti/Taisyti** *Tikrinti*
    - **Nuo datos:** Palikite šį laukelį tuščią.
    - **Sandėlio vietos būsenos nuolatinis tikrinimas:** Pasirinkite šį žymimą laukelį.

1. Pasirinkite **Gerai**.

    > [!TIP]
    > Kai nuolatinis tikrinimas yra užbaigtas, gausite pranešimą. Atidarykite [Veiksmų centrą](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) žinutės peržiūrai. Pasirinkite **Žinutės informacija** informacijos peržiūrai.
    >
    > Jei žinutė dėl nuolatinio tikrinimo sako „Netinkamas vietos būsenos informacija rasta XXXX vietai XX sandėlyje“, privalote vykdyti nuolatinį tikrinimą dar kartą. Šįkart, nustatykite **Tikrinti/Taisyti** laukelį į *Taisyti klaidą*. Peržiūrėkite žinutes, kad įsitikintumėte, jog nebuvo rasta jokių klaidų.

1. Dabar galite užbaigti profilio vietos nustatymą. Eikite atgal į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Vietos profiliai**, pasirinkite vietos profilį **FLOOR-05** ir tuomet veiksmų juostoje pasirinkite **Redaguoti**.
1. **Matmenys** „FastTab“, nustatykite šias vertes:

    - **Tūrio panaudojimo procentas:** *100*
    - **Tūrio matavimo metodas naudojamas inventoriaus vietoms:** *Naudoti vietos tūrį*
    - **Esamas vietos aukštis:** *10*
    - **Esamas vietos plotis:** *10*
    - **Esamas vietos gylis:** *10*
    - **Maksimalus svoris:** *100*

1. Pasirinkite **Įrašyti**.

### <a name="mobile-device-menu-items"></a>Mobiliojo įrenginio meniu elementai

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų juostoje pasirinkite **Naujas** tam, kad sukurtumėte meniu elementą rūšiavimui.
1. Antraštėje nustatykite šias vertes:

    - **Meniu elemento pavadinimas:** *Reguliuoti viduje*
    - **Pavadinimas:** *Reguliuoti viduje*
    - **Režimas:** *Darbas*
    - **Naudoti sukurtą darbą:** *Ne*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Darbo kūrimo procesas:** *Reguliavimas viduje*
    - **Inventoriaus reguliavimo tipai:** *Reguliuoti viduje*

1. Pasirinkite **Įrašyti**.

### <a name="mobile-device-menu"></a>Mobiliojo įrenginio meniu

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
1. Meniu sąraše pasirinkite **Inventorius**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. **Esančiuose meniu ir meniu elementų** sąraše suraskite ir pasirinkite **Reguliavimas viduje** meniu elementą.
1. Pasirinkite dešinės rodyklės mygtuką **Reguliavimas viduje** perkėlimui į **Meniu struktūros** sąrašą. Šiuo būdu, galėsite įtraukite naują meniu elementą į pasirinktą meniu.
1. Pasirinkite **Įrašyti**.

### <a name="movement-types"></a>Perkėlimo tipai

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Inventorius \> Judėjimo tipai**.
1. Veiksmų juostoje “, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes:

    - **Judėjimo tipo kodas:** *KONSOLIDUOTI*
    - **Aprašas:** *Konsoliduoti vietas*
    - **Darbo klasės identifikavimo numeris:** *InvMov*

1. Pasirinkite **Įrašyti**.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Tolesnis scenarijus naudoja sandėlio programą mobiliame prietaise tam, kad sukurtų inventorių *reguliavimą viduje* dvejose sandėlio vietose.

### <a name="add-inventory-to-locations"></a>Įtraukti inventorių į vietas

1. Prisijunkite prie mobilaus prietaiso kaip vartotojas nustatytas sandėliui *51*.
1. Eikite į **Inventorius \> Reguliavimas viduje**.

    Dabar įvesite pirmą vietos reguliavimą.

1. **Reguliavimas viduje** užduotyje, pasirinkite vietą tam, kad sukurtumėte inventoriaus reguliavimą. **LOC** laukelyje pasirinkite *LP-001*.
1. Patvirtinkite vietą.
1. Sukurkite licencijos numerio identifikavimo kodą elementui, kuris bus įtrauktas į vietą. **LP** laukelyje įveskite *LP00101*.
1. Patvirtinkte licencijos numerį.
1. Įveskite elementą, kuris bus įtrauktas į licencijos numerį. **ITEM** lauke įveskite *M9201*.
1. Patvirtinkite elementą.
1. Įveskite elemento kiekį, kuris bus įtrauktas. **QTY** laukelyje įveskite *10*.
1. Patvirtinkite kiekį.

    Gaunate Pabaigtas darbas pranešimą. Dabar įveskite antrą vietos reguliavimą.

1. **Reguliavimas viduje** užduotyje, pasirinkite vietą tam, kad sukurtumėte inventoriaus reguliavimą. **LOC** laukelyje pasirinkite *LP-002*.
1. Patvirtinkite vietą.
1. Sukurkite licencijos numerio identifikavimo kodą elementui, kuris bus įtrauktas į vietą. **LP** laukelyje įveskite *LP00201*.
1. Patvirtinkte licencijos numerį.
1. Įveskite elementą, kuris bus įtrauktas į licencijos numerį. **ITEM** lauke įveskite *M9201*.
1. Patvirtinkite elementą.
1. Įveskite elemento kiekį, kuris bus įtrauktas. **QTY** laukelyje įveskite *15*.
1. Patvirtinkite kiekį.

    Gaunate Pabaigtas darbas pranešimą.

1. Pasirinkite meniu mygtuką (kartais vadinamas mėsainiu ar mėsainio mygtuku) ir tuomet pasirinkite **Atšaukit** tam, kad išeitumėte iš **Rguliavimo viduje** užduoties.

### <a name="consolidate-locations"></a>Vietų konsolidavimas

1. Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Elemento konsolidavimas**.
1. Antraštėje pasirinkite sandėlė, kuriame atliksite konsolidavimą. **Sandėlio** laukelyje įveskite *51*.

    Įrašas rodomas visose vietose, kuriose elementas *M9201* buvo reguliuotas. **Utilizavimo procento** stulpelis rodo naudojamą tūrį visose vietose.

1. Inventoriaus konsilidavimui, pasirinkite visas konsoliduoti būtinas vietas ir tuomet veiksmų juostoje pasirinkite **Konsoliduoti inventorių**.
1. **Konsoliduoti inventorių** teksto laukelyje nurodykite vietą ir judėjimo tipą, kuris turi būti naudojamas inventoriaus judėjimo darbo sukūrimui. Nustatykite toliau nurodytas reikšmes.

    - **Vieta:** *LP-001*
    - **Judėjimo tipo kodas:** *KONSOLIDUOTI*

1. Pasirinkite **Gerai**.
1. Gausite informacinį pranešimą, kuriame bus rodomas sukurto darbo judėjimas. Užsirašykite darbo judėjimo identifikavimo kodą.

### <a name="view-movement-work"></a>Darbo judėjimo peržiūra

1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.
1. Peržiūrėkite sukurtą darbą. Naudokite darbo identifikavimo kodą inventoriaus konsolidavimo filtravimui ar paieškai darbo tinklelyje.

    Šiame scenarijuje, esama vieta turėjusi inventorių buvo naudojama kaip inventoriaus konsolidavimo vieta. Dėl to, buvo sukurtas tik vienas dabo identifikavimo kodas.

    > [!NOTE]
   > Sistema sukuria vieną darbo identifikavimo kodą vienam judėjimui, kuris turi būti atliktas. Jei nurodote vietą, kuri jau turi inventorių, yra sukuriamas tik vienas darbo identifikavimo kodas. Jei nurodote naują vietą, bus sukuriami du darbo identifikavimo kodai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
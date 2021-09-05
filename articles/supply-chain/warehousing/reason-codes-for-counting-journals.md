---
title: Atsargų skaičiavimo priežasčių kodai
description: Šioje temoje aprašoma, kaip nustatyti ir taikyti atsargų skaičiavimo priežasčių kodus.
author: perlynne
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 95f7ceb39d2afef1871f395ed562632865022b39
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345271"
---
# <a name="reason-codes-for-inventory-counting"></a>Atsargų skaičiavimo priežasčių kodai

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Priežasčių kodai suteikia galimybę analizuoti skaičiavimo procesą rezultatus ir visus to proceso metu įvykusius neatitikimus. Galite nurodyti skaičiavimo priežastį, pvz., sugadintas padėklas arba atsargų koregavimas, pagal atsargų pavyzdžius. Tuo pat metu galite naudoti koregavimo funkciją, kad užregistruotumėte turimų atsargų koregavimų vertę į atitinkamą korespondentinę sąskaitą, paremtą kiekvieno atsargų koregavimo priežastimi.

## <a name="recommendation"></a>Rekomendacija

Prieš nustatant sistemą rekomenduojame nustatyti darbo su priežasčių kodais strategiją. Pavyzdžiui, pabandykite atsakyti į toliau nurodytus klausimus.

- Ar sandėliuose priežasčių kodai turėtų būti privalomi?
- Ar kai kuriose prekėse priežasčių kodai turėtų būti privalomi, ar pasirenkami?
- Kiek priežasčių kodų jums reikia?
- Ar turite iš anksto pasirinkti ribotą koregavimų priežasčių kodų sąrašą?
- Kaip brūkšninių kodų skaitytuvų vartotojai turėtų naudoti priežasčių kodus? Ar priežasčių kodai turėtų būti iš anksto pasirenkami, privalomi arba neredaguojami?
- Ar sandėlio darbuotojams reikalingi skirtingų tipų priežasčių kodai mobiliuosiuose skaitytuvuose? Jei atsakymas teigiamas, galite kurti daugiau meniu elementų ir juos priskirti skirtingiems žmonėms.
- Ar priežasčių kodai turi rodyti finansinės korespondentinės sąskaitos registravimą?

## <a name="turn-on-reason-code-features-in-your-system"></a>Savo sistemoje įjunkite priežasties kodo funkcijas

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Jei savo sistemoje nematote visų šioje temoje aprašytų funkcijų, tikriausiai turite įjungti *Registruoti turimų atsargų koregavimus naudojant konfigūruojamus priežasties kodus, prijungtus prie korespondentinės sąskaitos* funkcijas. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Registruoti turimų atsargų koregavimus naudojant konfigūruojamus priežasties kodus, prijungtus prie korespondentinės sąskaitos*

## <a name="set-up-reason-codes"></a>Nustatyti priežasčių kodus

### <a name="set-up-reason-code-policies"></a>Priežasčių kodų strategijų nustatymas

Galite sukurti kelias priežasčių kodų strategijas, kad galėtumėte kontroliuoti, kada ir kaip taikomi skaičiavimo priežasčių kodai. Kiekvienos priežasties kodo strategija gali turėti vieną iš dviejų skaičiavimo priežasčių kodų tipų (*Pasirenkamas* arba *Privalomas*). Skaičiavimo priežasčių kodų strategijas galima naudoti sandėlio lygiu arba prekės lygiu.

Norėdami sukurti priežasties kodo strategiją, atlikite šiuos veiksmus.

1. Eikite į **į Atsargų valdymas** \> **Sąranka** \> **Atsargos** \> **Skaičiavimo priežasčių kodų strategijos**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte strategiją į tinklelį.
1. Nustatykite **Pavadinimas** laukelį naujai strategijai.
1. Lauke **Skaičiavimo priežasties kodo tipas** pasirinkite *Privalomas* arba *Pasirinktinis*, norėdami nurodyti, ar priežasties kodo pasirinkimas yra pasirinktinis, ar privalomas viename iš toliau nurodytų atsargų koregavimo procesų.

    - Ciklo skaičiavimas (mobilusis įrenginys)
    - Vietos skaičiavimas (mobilusis įrenginys)
    - Ribinės reikšmės skaičiavimas (mobilusis įrenginys)
    - Koregavimo taikymas (mobilusis įrenginys)
    - Koregavimo atšaukimas (mobilusis įrenginys)
    - Žurnalo skaičiavimas (raiškusis klientas)
    - Kiekio koregavimas/Skaičiavimas tinkle (raiškusis klientas)

Galite nustatyti tiek atskirų sandėlių, tiek ir produktų priežasčių kodų strategijas. Produkto priežasties kodo nustatymas gali panaikinti produkto sandėlio nustatymą.

> [!NOTE]
> Sandėliams ir prekėms, kai **Skaičiavimo priežasties kodo strategijos** laukas nustatytas kaip *Privalomas*, skaičiavimo žurnalas negali būti užbaigtas ir uždaromas, kol nėra pateiktas priežasties kodas. Daugiau informacijos žr. kitame skyriuje.

### <a name="assign-counting-reason-code-policies-to-warehouses"></a>Priskirkite skaičiavimo priežasties kodo strategijas sandėliams

Norėdami skaičiavimo priežasties kodo strategiją priskirti sandėliui, atlikite šiuos veiksmus.

1. Eikite į **IAtsargų valdymas** \> **Sąranka** \> **Atsargų paskirstymas** \> **Sandėliai**.
1. Sąrašo srityje pasirinkite sandėlį.
1. Veiksmų juostoje, **Sandėlys** skirtuke, **Nustatymai** grupėje, pasirinkite **Skaičiavimo priežasties kodo strategija**. Tada iššokančiame dialogo lange **Priskirti skaičiavimo priežasties kodo strategiją** atlikite vieną iš šių veiksmų:

    - Norėdami naudoti strategijos nustatymą kiekvienai prekei, kad nustatytumėte, ar inventorizacijos žurnalai privalomi, įveskite vertę (arba panaikinkite esamą vertę).
    - Reikalaujant priežasties kodo sandėlio inventorizacijos žurnaluose, pasirinkite priežasčių strategiją, kai **Skaičiavimo priežasties kodo tipo** laukas nustatytas kaip *Privalomas*.
    - Jei priežasties kodas sandėlio inventorizacijos žurnaluose pasirinktinas, pasirinkite priežasčių strategiją, kai **Skaičiavimo priežasties kodo tipo** laukas nustatytas kaip *Pasirinktinas*.

### <a name="assign-counting-reason-code-policies-to-products"></a>Priskirkite skaičiavimo priežasties kodo strategijas produktams

Norėdami skaičiavimo priežasties kodo strategiją priskirti produktui, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas** \> **Produktai** \> **Patvirtinti produktai**.
1. Pasirinkite produktą iš tinklelio.
1. Veiksmų juostoje, **Produktas** skirtuke, **Nustatymai** grupėje, pasirinkite **Skaičiavimo priežasties kodo strategija**. Tada iššokančiame dialogo lange **Priskirti skaičiavimo priežasties kodo strategiją** atlikite vieną iš šių veiksmų:

    - Norėdami naudoti strategijos nustatymą sandėliui, kad nustatytumėte, ar inventorizacijos žurnalai produktui privalomi, įveskite vertę (arba panaikinkite esamą vertę).
    - Reikalaujant priežasties kodo produktui inventorizacijos žurnaluose, pasirinkite priežasčių strategiją, kai **Skaičiavimo priežasties kodo tipo** laukas nustatytas kaip *Privalomas*. Šis parametras perrašo bet kokį priežasties kodo parametrą sandėlio lygiu.
    - Jei priežasties kodas produktui inventorizacijos žurnaluose pasirinktinas, pasirinkite priežasčių strategiją, kai **Skaičiavimo priežasties kodo tipo** laukas nustatytas kaip *Pasirinktinas*. Šis parametras perrašo bet kokį priežasties kodo parametrą sandėlio lygiu.

### <a name="set-up-counting-reason-codes"></a>Skaičiavimo priežasčių kodų nustatymas

Skaičiavimo priežasčių kodų nustatymui, atlikite šiuos žingsnius.

1. Eikite į **į Atsargų valdymas** \> **Sąranka** \> **Atsargos** \> **Skaičiavimo priežasčių kodai**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.
1. Naujai eilutei nustatykite **Skaičiavimo priežasties kodas** ir **Aprašymas** laukelius.
1. Norėdami priskirti korespondentinę sąskaitą, įveskite arba pasirinkite vertę **Korespondentinė sąskaita** laukelyje.

    > [!NOTE]
    > Jei korespondentinė sąskaita priskiriama inventorizacijos priežasties kodui, registruojant inventorizacijos žurnalą naudojamas inventorizacijos priežasties kodas, vertė užregistruojama pagal priskirtą korespondentinę sąskaitą, o ne pagal numatytąją atsargų registravimo šablono sąskaitą.

### <a name="set-up-counting-reason-code-groups"></a><a name="reason-groups"></a>Nustatykite skaičiavimo priežasties kodų grupes

*Skaičiavimo priežasčių kodų grupes* galima naudoti kaip „Warehouse Management“ mobiliųjų įrenginių programos *Koregavimo į* ir *Koregavimo iš* meniu elementų dalį, kad būtų galima apriboti skaičiavimo kodų sąrašą. (Daugiau informacijos apie inventorizacijos priežasčių kodų grupes žr. [Nustatykite mobiliojo įrenginio meniu koregavimui į ir koregavimui iš](#setup-adjustment-in-out) skyrių vėliau šioje temoje.)

1. Eikite į **į Atsargų valdymas** \> **Sąranka** \> **Atsargos** \> **Skaičiavimo priežasčių kodų grupės**.
1. Veiksmų srityje pasirinkite **Naujas**, norėdami pridėti grupę.
1. Naujai grupei nustatykite **Skaičiavimo priežasties grupė** ir **Grupės aprašymas** laukeliuose.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. **Duomenys** skyriuje įrankių juostoje pasirinkite **Naujas**, kad įtraukumėte eilutę į tinklelį. Tada naujai eilutei nustatykite **Skaičiavimo priežasties kodas** laukelį. 
1. Pakartokite ankstesnį veiksmą, jei reikia, norėdami priskirti daugiau kodų. Jei turite pašalinti kodą iš grupės, pasirinkite jį, o tada įrankių juostoje pasirinkite **Naikinti**.

### <a name="set-up-reason-codes-for-mobile-device-menu-items"></a>Mobiliojo įrenginio meniu elementų priežasčių kodų sąranka

Galite konfigūruoti šių turimo koregavimo tipų priežasčių kodus:

- Ciklo skaičiavimas
- Vietos skaičiavimas
- Ribinės reikšmės skaičiavimas
- Koregavimo taikymas
- Koregavimo atšaukimas

Daugeliu atvejų galite nurodyti toliau pateiktą informaciją apie kiekvieną atitinkamą mobiliojo įrenginio meniu elementą:

- Informacija apie tai, ar atliekant skaičiavimą priežasties kodas rodomas darbuotojui, kuriam priklauso mobilusis įrenginys.
- Numatytasis priežasties kodas, rodomas mobiliojo įrenginio meniu elemente.
- Informacija apie tai, ar vartotojas gali redaguoti priežasties kodą.

#### <a name="set-up-mobile-device-menu-items-for-a-counting-process"></a>Nustatykite mobiliojo įrenginio meniu elementus skaičiavimo procesui

Norėdami nustatyti mobiliojo įrenginio meniu elementą skaičiavimo procesui, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Mobilus įrenginys** \> **Mobiliojo įrenginio meniu elementai**.
1. Pasirinkite reikiamą meniu elementą sąrašo srityje arba sukurkite naują meniu elementą.
1. Veiksmų srityje pasirinkite **Ciklo skaičiavimas**.
1. Lauke **Numatytasis skaičiavimo priežasties kodas** nustatykite numatytąjį priežasties kodą, kuris turi būti įrašomas, kai skaičiavimas atliekamas naudojant mobiliojo įrenginio meniu elementą.
1. Laukelyje **Rodyti skaičiavimo priežasties kodą** rinkitės vieną tolesnių verčių:

    - *Eilutė* – rodyti priežasties kodą po to, kai įrašomas kiekvienas nuokrypis.
    - *Slėpti* – nerodyti priežasties kodo.

1. Nustatykite **Redaguoti skaičiavimo priežasties kodą** į *Taip*, kad įgalintumėte darbuotoją redaguoti priežasties kodą, kai atliekant skaičiavimą jis rodomas mobiliajame įrenginyje. Nustatykite į *Ne* jei norite neleisti darbuotojui redaguoti kodo.

> [!NOTE]
> Mygtuką **Ciklo skaičiavimas** galima įjungti bet kuriame mobiliojo įrenginio meniu elemente, kuriame galima atlikti skaičiavimą. Pavyzdžiai: vietos skaičiavimo, vartotojo nurodyto darbo ir sistemos nurodyto darbo meniu elementai.

#### <a name="set-up-mobile-device-menu-items-for-adjustment-in-and-adjustment-out"></a><a name="setup-adjustment-in-out"></a>Mobiliojo įrenginio meniu elementų nustatymas į Koregavimo taikymas ir Koregavimo atšaukimas

Norėdami nustatyti mobiliojo įrenginio meniu elementą koregavimo taikymui ar koregavimo atšaukimui, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas** \> **Sąranka** \> **Mobilus įrenginys** \> **Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite **Naujas** prekių meniu sukūrimui.
1. Nustatykite **Mobiliojo įrenginio prekės pavadinimas** ir **Pavadinimas** laukelius naujam meniu elementui.
1. Nustatykite **Režimas** laukelį į *Dirbti*.
1. Nustatykite pasirinkties **Naudoti esamą darbą** padėtį *Ne*.
1. **Darbo kūrimo procesas** laukelyje pasirinkite *Koregavimo taikymas* arba *Koregavimo atšaukimas*.
1. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus. (Visi šie laukai pridedami pasirinkus *Koregavimo taikymas* arba *Koregavimo atšaukimas* **Darbo kūrimo proceso** laukelyje.)

    - **Naudokite proceso vadovą**– jei kuriate *Koregavimo atšaukimas* procesą, būtinai nustatykite šią pasirinktį į *Taip*. Jei kuriate *Koregavimo atšaukimo* procesą, ši pasirinktis visada nustatoma kaip *Taip*.
    - Lauke **Numatytasis skaičiavimo priežasties kodas** - nustatykite numatytąjį priežasties kodą, kuris turi būti įrašomas, kai skaičiavimas atliekamas naudojant mobiliojo įrenginio meniu elementą.
    - Laukelyje **Rodyti skaičiavimo priežasties kodą** - pasirinkite vieną tolesnių verčių:

        - *Eilutė* – rodyti priežasties kodą po to, kai įrašomas kiekvienas nuokrypis.
        - *Slėpti* – nerodyti priežasties kodo.

    - **Redaguoti skaičiavimo priežasties kodą** - nustatykite šią parinktį į *Taip*, kad įgalintumėte darbuotoją redaguoti priežasties kodą, kai atliekant skaičiavimą jis rodomas mobiliajame įrenginyje. Nustatykite į *Ne* jei norite neleisti darbuotojui redaguoti kodo.
    - **Skaičiavimo priežasčių kodų grupė** - pasirinkite priežasčių kodų grupę, jei norite apriboti pasirinkčių, pateiktų darbuotojams, sąrašą. Kaip nustatyti priežasčių kodų grupes, žr. [Nustatyti inventorizacijos priežasčių kodų grupes](#reason-groups) skyriuje aukščiau. 

> [!NOTE]
> Kai priskiriate skaičiavimo priežasčių kodų grupę *Koregavimo taikymas* ir *Koregavimo atšaukimas* meniu elementams, kai **Naudoti proceso vadovą** parinktis nustatyta į *Taip*, galite gauti ribotą skaičiavimo priežasčių kodų sąrašą kaip skaičiavimo priežasčių kodų apdorojimo dalį „Warehouse Management“ mobiliąją programą.
>
> **Naudoti proceso vadovą** parinktis taip pat gali apsaugoti nuo didelių koregavimo kiekių, kurie gali atsirasti per klaidą. (Pvz., darbuotojas gali atsitiktinai nuskaityti prekės numerio, o ne kiekio vertės, brūkšninius kodus.) Norėdami nustatyti šią funkciją, nustatykite parinktį **Naudoti proceso vadovą** į *Taip* kiekvienam susijusiam meniu elementui. Tada eikite į **Sandėlio valdymas \> Sąranka \> Darbuotojas** ir nustatykite **Koregavimo kiekio riba** laukelį kiekvienam atitinkamam sandėlio darbuotojui, kad nurodytumėte didžiausią koregavimo kiekį, kurį darbuotojas gali registruoti.

## <a name="processing-that-uses-counting-reason-codes"></a>Apdorojimas, naudojantis skaičiavimo priežasčių kodus

Kai darbuotojai naudoja „Warehouse Management“ mobiliąją programą, priežasčių kodai įrašomi. Jei nenurodytas skaičiavimo patvirtinimo procesas, įrašyti priežasčių kodai iš karto naudojami kaip inventorizacijos žurnalo registravimo dalis.

### <a name="cycle-count-approvals"></a>Ciklo skaičiavimo patvirtinimai

Prieš patvirtinant skaičiavimą, darbuotojas gali keisti priežasties kodą, susietą su skaičiavimu. Patvirtinus skaičiavimą, priežasties kodas įvedamas skaičiavimo žurnalo eilutėse.

#### <a name="modify-reason-codes-for-cycle-count-approvals"></a>Modifikuoti ciklų skaičiavimo patvirtinimų priežasčių kodus

Atlikite šiuos veiksmus, jei norite keisti ciklo skaičiavimą:

1. Eikite į **Sandėlio valdymas** \> **Ciklo skaičiavimas** \> **Peržiūros laukiantis ciklo skaičiavimo darbas**.
1. Tinklelyje pasirinkite ciklo skaičiavimą.
1. Veiksmų srities skirtuke **Darbas** pasirinkite **Ciklo skaičiavimas**. Tada laukelyje **Priežasties kodas** pasirinkite naują priežasties kodą.

Priežasčių kodai įtraukiami į žurnalo eilutes tipo *Skaičiavimo žurnalas* skaičiavimo žurnaluose.

1. Eikite į **Atsargų valdymas** \> **Žurnalo įrašai** \> **Prekių skaičiavimas** \> **Skaičiavimas**.
2. Inventorizacijos žurnalo eilutės **Inventorizacijos priežasties kodas** laukelyje pasirinkite priežasties kodą, kuris atitinka esamą situaciją.

### <a name="view-the-reason-codes-recorded-in-the-counting-history"></a>Peržiūrėkite įrašytus priežasčių kodus skaičiavimo retrospektyvoje

Norėdami peržiūrėti priežasčių kodus, įrašytus inventorizacijos retrospektyvoje, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Inventorizacijos retrospektyva**.
1. Sąrašo srityje pasirinkite prekių skaičiavimo įrašą.
1. **Inventorizacijos priežasties kodas** laukelyje peržiūrėkite inventorizacijos retrospektyvą, kuri buvo įrašyta naudojant priežasties kodą.

### <a name="use-reason-codes-for-quantity-adjustment-or-online-counting"></a>Naudokite priežasčių kodus kiekio koregavimui arba skaičiavimui tinkle

Norėdami naudoti kiekio koregavimo arba skaičiavimo tinkle priežasties kodą, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Užklausos ir ataskaitos \> Turimas sąrašas**.
1. Veiksmų srityje pasirinkite **Kiekio koregavimas**.
1. Pasirinkite **Kiekio koregavimas**, tada lauke **Skaičiavimo priežasties kodas** pasirinkite priežasties kodą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

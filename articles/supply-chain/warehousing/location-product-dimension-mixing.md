---
title: Vietos produkto dimensijos maišymas
description: Šioje temoje pateikiama informacija apie vietos produkto dimensijos maišymą. Ši vietos profilio funkcija padeda pagerinti vietos valdymą, kai produkto variantai arba produktai, turintys dimensijas, yra naudojami pvz., mados industrijoje. Ji leidžia Jums nuspręsti, ar konfigūracijas, spalvas, stilius ir dydžius galima maišyti tam tikram vietos profiliui, taip pat ar vieną iš šių dimensijų arba jų derinį galima įtraukti į tą pačią vietą.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 73519f3fe79d3d7d917d3044255f735640b8ccfd
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433916"
---
# <a name="location-product-dimension-mixing"></a>Vietos produkto dimensijos maišymas

[!include [banner](../includes/banner.md)]

Vietos produkto dimensijos maišymas yra vietos profilio funkcija, padedanti pagerinti vietos valdymą, kai produkto variantai arba produktai, turintys dimensijas, yra naudojami pvz., mados industrijoje. Ji leidžia Jums nuspręsti, ar konfigūracijas, spalvas, stilius ir dydžius galima maišyti tam tikram vietos profiliui, taip pat ar vieną iš šių dimensijų arba jų derinį galima įtraukti į tą pačią vietą.

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a>Vietos produkto dimensijos maišymo funkcijos įjungimas

Norėdami naudoti vietos produkto dimensijos maišymą, ši funkcija turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *Vietos produkto dimensijos maišymas*

## <a name="setup"></a>Sąranka

Su kiekviena sandėlio vieta turi būti susietas vietos profilis, nurodantis vietos ypatybes. Todėl visos vietos, kuriose naudojamas tas pats vietos profilis, galės leisti produkto dimensijos maišymą, kai jis bus nustatytas.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Vietos profilių konfigūravimas produkto dimensijai maišyti

1. Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlys \> Vietos profiliai**.
1. Iš vietų profilių sąrašo pasirinkite **KROVINYS**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. „FastTab“ skirtuke **Bendra** nustatykite **Įjungti konkretų vietos produkto dimensijos maišymą** parinktį į *Taip*.

    > [!NOTE]
    > Šią parinktį galite nustatyti į *Taip* tik jeigu parinktis **Leisti mišrias prekes** yra nustatyta į *ne*.

1. „FastTab“ skirtuke **Leidžiamų produktų dimensijos maišymas** parinktį **Dydis** nustatykite į *taip*. Šioje temoje pateiktu atveju, maišymas gali būti atliekamas tik tiems produktams, kurių **Dydžių** dimensijos skiriasi. Tačiau galimos ir kitos parinktis.
1. Pasirinkite **Įrašyti**.

### <a name="create-a-new-product-master-and-product-variants"></a>Bendrųjų produktų ir produktų variantų sukūrimas

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Bendrieji produktai**.
1. Veiksmų srityje pasirinkite **Nauja** bendrajam produktui sukurti.
1. Dialogo lange **Naujas produktas** nustatykite šias vertes:

    - **Produkto tipas:** *Prekė*
    - **Produkto potipis:** *Bendrasis produktas*
    - **Produkto numeris:** *B0001*
    - **Produkto pavadinimas:** *B0001 Dydis*
    - **Produkto dimensijos grupė:** *Dydis*
    - **Konfigūravimo technologija:** *Iš anksto nustatytas variantas*

1. Pasirinkite **Gerai**.
1. Puslapio **Produkto informacija** „FastTab“ skirtuke **Bendra** nustatykite šias vertes:

    - **Generuoti variantus automatiškai** *Taip*
    - **Dydžio grupė:** *CASUALDHIR*

1. Norėdami peržiūrėti iš anksto nustatytus variantus, veiksmų srityje pasirinkite **Produkto variantai**.

    Puslapis **Produkto variantai** atsidarys ir parodys dydžių grupės konfigūravimo variantų sąrašą.

### <a name="release-products-to-the-usmf-company"></a>Produktų išleidimas į USMF įmonę

1. Veiksmų srityje pasirinkite **Produkto variantai**.
1. Puslapyje **Pasirinkti išleidžiamus produktus** patikrinkite, ar produkto numeris *B0001* yra sąraše, o tada pasirinkite **kitas**.
1. Pasirinkite **Toliau** norėdami patvirtinti išleidžiamus produkto variantus.
1. Puslapyje **Pasirinkite išleidimo įmones** pasirinkite *USMF* ir **Toliau** parinkčiai patvirtinti.
1. Puslapyje **Patvirtinti pasirinkimą** pasirinkite **Baigti** išleidimui užbaigti.

    Jūs gausite pranešimą "Operacija atlikta".

### <a name="update-a-released-product-in-the-usmf-company"></a>Išleisto produkto USMF įmonėje atnaujinimas

1. Įsitikinkite, kad esate prisijungęs prie **USMF** įmonės.
1. Pasirinkite **Produkto informacijos valdymas \> Produktai \> Išleisti produktai** pabaigti kurti išleistam produktui.
1. Raskite ir pasirinkite prekės numerį *B0001* puslapiui **Išleisto produkto informacija** atidaryti.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Įsitikinkite, kad „FastTab“ skirtuko **Bendra** laukas **Prekių modelių grupė** nustatytas į *FIFO*.
1. Veiksmų srities skirtuko **Produktas** grupėje **Nustatyti** pasirinkite **Dimensijų grupės**.
1. Nustatykite toliau nurodytas reikšmes.

    - **Saugojimo dimensijos grupė:** *Sandėlis*
    - **Sekimo dimensijos grupė:** *Nėra*

1. Pasirinkite **Gerai**.
1. Veiksmų srities skirtuko **Produktas** grupėje **Nustatyti** pasirinkite **Rezervavimo hierarchija**.
1. Nustatykite **Rezervavimo hierarchijos** lauką į *Numatytasis* ir pasirinkite **Gerai**.
1. Atkreipkite dėmesį, kad jūsų pasirinkimai skyriaus **Administravimas** „FastTab“ skirtuke **Bendra** buvo atnaujinti.
1. „FastTab“ skirtuko **Pirkimas** lauke **Kaina** įveskite *10*.
1. „FastTab“ skirtuko **Tvarkyti išlaidas** lauke **Prekių grupė** įveskite *Audio*.
1. „FastTab“ skirtuko **Pirkimas** lauke **Kaina** įveskite *10*.
1. „FastTab“ skirtuko **Sandėlys** lauke **Vienetų sekų grupės ID** įveskite *EA*.
1. Pasirinkite **Įrašyti**.

### <a name="create-a-location-directive"></a>Vietos nurodymo kūrimas

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Kairinės srities lauke **Darbo užsakymo tipas** pasirinkite *Pirkimo užsakymai*.
1. Iš sąrašo pasirinkite vietos nurodymą pavadinimu *24 Tiesioginis PU*.
1. „FastTab“ skirtuke **Vietos nurodymo veiksmai** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Sekos numeris:** *1*

        Nauja eilutė turi būti priekyje anksčiau sukurtos eilutės. Norėdami atlikti pakeitimą, naudokite įrankių juostoje esančius mygtukus **Perkelti aukštyn** ir **Perkelti žemyn** arba pakeiskite esamos eilutės **Sekos numerio** reikšmę į *2*.

    - **Pavadinimas:** *Pridėti į BULK vietos profilį*
    - **Fiksuotos vietos naudojimas:** *Fiksuotos ir nefiksuotos vietos*
    - **Leisti neigiamas atsargas:** *Išvalyti šį žymės langelį (=Ne)*
    - **Paketas įjungtas:** *Išvalykite šį žymės langelį (=Ne)*
    - **Strategija:** *Nėra*

1. Kol renkamasi nauja eilutė, virš tinklelio pasirinkite **Redaguoti užklausą**.
1. Dialogo lango **Diapazonas** skirtuke pasirinkite **Pridėti** eilutei pridėti į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Lentelė:** *Vietos*
    - **Išvestinė lentelė:** *Vietos*
    - **Laukas:** *Vietos profilio ID*
    - **Kriterijai:** *BULK*

1. Pasirinkite **Gerai**.
1. Veiksmų srities puslapyje **Vietos nurodymai** pasirinkite **Įrašyti**.

> [!NOTE]
> Jei skirtuko **Vietos nurodymai**„FastTab“ lauke **Strategija** pasirinkta vietos strategija yra *Konsolidavimas* nustatymo **Leidžiamų produktų dimensijos maišymas** **Vietos profiliuose** nebus paisoma, o prekės bus pridėtos į tą pačią vietą, net jei šis veiksmas neleidžiamas pagal nustatymą.

### <a name="create-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu elemento kūrimas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite **Nauja** meniu elemento, naudojamo rūšiavimui, sukūrimui.
1. Antraštėje nustatykite šias vertes:

    - **Meniu elemento pavadinimas:** *PU eilutės gavimas*
    - **Pavadinimas:** *PU eilutės gavimas*
    - **Režimas:** *Darbas*
    - **Naudoti sukurtą darbą:** *Ne*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Darbo sukūrimo procesas:** *Pirkimo užsakymo eilutės gavimas ir paėmimas*
    - **Generuoti numerio lentelę:** *Taip*

1. Pasirinkite **Įrašyti**.

### <a name="configure-the-mobile-device-menu"></a>Mobiliojo įrenginio meniu konfigūravimas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
1. Iš meniu sąrašo pasirinkite **Gaunama**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Iš **Galimų meniu ir meniu elementų** sąrašo suraskite ir pasirinkite **PU eilutės gavimo** meniu elementą.
1. Pasirinkti dešiniosios rodyklės mygtuką **PU eilutės gavimo** meniu elementui perkelti į **Meniu struktūros** sąrašą. Tokiu būdu prie pasirinkto meniu pridėsite naują meniu elementą.
1. Pasirinkite **Įrašyti**.

## <a name="scenario"></a>Scenarijus

Šis parodomasis scenarijus parodo, kaip du skirtingi produkto variantai gali būti pridėdami į tą pačią vietą, tuo atveju, kai vietos profilis neleidžia maišyti prekių, bet *Vietos produkto dimensijos maišymo* funkcija yra įjungta. Šiuo atveju kaip kriterijų naudosite **Dydžio** variantą.

Prieš pradėdami įsitikinkite, kad *24* sandėlyje yra tuščių vietų, naudojančių *BULK* vietos profilį.

### <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

Jūs sukursite pirkimo užsakymas, turintį tris eilutes: dvi eilutės yra to pačio produkto numerio, tačiau skirtingų **Dydžio** variantų, o trečia eilutė yra skirta skirtingiems produktams, kuriuose nėra variantų.

1. Eikite į **Mokėtinos sumos \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pirkimo užsakymą** nustatykite šias vertes:

    - **Tiekėjo paskyra:** *1001*
    - **Sandėlis:** *24*

1. Pasirinkite **Gerai**.
1. Sukuriamas pirkimo užsakymas, o nauja eilutė yra įtraukiama į **Pirkimo užsakymo eilutės** „FastTab“ skirtuką. Pasižymėkite pirkimo užsakymo numerį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *B0001*
    - **Dydis** *L*
    - **Kiekis:** *2*

1. Pasirinkite **Pridėti eilutę** antram pirkimo užsakymui pridėti ir nustatykite šias reikšmes:

    - **Prekės numeris:** *B0001*
    - **Dydis** *XL*
    - **Kiekis:** *2*

1. Pasirinkite **Pridėti eilutę** trečiam pirkimo užsakymui pridėti ir nustatykite šias reikšmes:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *1*

1. Pasirinkite **Įrašyti**.

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a>Pirkimo užsakymo eilutės gavimas „Warehousing“ programoje

1. Prisijunkite prie „Warehousing“ programos kaip vartotojas, įgalintas sandėliui *24*.
1. Pasirinkite **Gaunama** meniu.
1. Pasirinkite: **PU eilutės gavimas**.
1. Pasirinkite lauką **PU numeris** ir įveskite pirkimo užsakymo numerį.
1. Patvirtinkite savo įrašą pasirinkdami mygtuką patvirtinti (✔) puslapio apačioje.
1. Įveskite eilutės numerį iš gaunamo pirkimo užsakyme. Pasirinkite lauką **Eilutės numeris** ir naudodami skaičių klaviatūrą, įveskite *1*.
1. Patvirtinkite savo įrašą.
1. Įvesti gaunamą kiekį. Pasirinkite pliuso ženklo (**+**) mygtuką du kartus, kad padidintumėte vertę lauke **Kiekis** į *2*.
1. Užregistruokite savo įrašą pasirinkdami mygtuką (✔) puslapio apačioje ir patvirtinkite savo įrašą pasirinkdami mygtuką (✔) dar kartą.
1. Peržiūrėkite informaciją **Pirkimo užsakymus: Paėmimas** puslapyje. Šiame puslapyje rodomas darbas, sukurtas prekių paėmimui (1 darbas).

    Bus rodoma neseniai užbaigtos **PU eilutės gavimo** užduoties vieta, kurioje bus padėta gaunama prekė, numerio lentelė, prekė, dydis ir kiekis.

1. Paėmimo darbo patvirtinimas.
1. Pakartokite 4-11 žingsnius 2 pirkimo užsakymo eilutei. Tačiau 8 žingsnyje nustatykite kiekį į *1*.

    Naujas paėmimo darbas (2 darbas) yra sukuriamas toje pačioje vietoje kaip 1 darbas.

1. Pakartokite 4-11 žingsnius dar sykį 2 pirkimo užsakymo eilutei. 8 žingsnyje nustatykite likusį kiekį į *1*.

    Naujas paėmimo darbas (3 darbas) yra sukuriamas toje pačioje vietoje kaip 1 darbas ir 2 darbas. Taip atsitinka, nes yra naudojama *Konsolidavimo* vietos nurodymo strategija, o „FastTab“ skirtuko **Leidžiamo produkto dimensijos maišymas**, esančio *Krovinys* **Vietos profiliai**, nustatymas leidžia vietoje maišyti **Dydžio** variantą.

1. Pakartokite 4-11 žingsnius 3 pirkimo užsakymo eilutei. 8 žingsnyje nustatykite kiekį į *1,* skirtą prekės numeriui *A0001*.

    Naujas paėmimo darbas (4 darbas) sukuriamas skirtingai vietai, nei ta, kuri yra naudojama 1 ir 2 pirkimo užsakymo eilutėse. Taip atsitinka, nes vietos profilis neleidžia maišyti produktų, bet leidžia maišyti tos pačio bendrojo produkto dimensijas.

1. Puslapio viršuje pasirinkite meniu mygtuką (kartais jis vadinamas Hamburger arba Hamburger mygtuku) ir tada pasirinkite **Atšaukti,** kad išeitumėte iš **PU eilutės gavimo**.

> [!TIP]
> Galite pakartoti šį scenarijų, bet šį kartą nustatykite *KROVINYS* **Vietos profiliai** „FastTab“ skirtuko **Leisti produkto dimensijos maišymą** **Dydį** - *Ne*, kad nebūtų galima maišyti nė vienos produkto dimensijos. Tokiu atveju, kai gausite pirkimo užsakymą, kiekvienas produkto variantas bus įtrauktas į naują vietą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
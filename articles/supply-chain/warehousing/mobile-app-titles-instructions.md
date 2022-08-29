---
title: „Warehouse Management“ mobiliųjų įrenginių programėlės veiksmų pavadinimų ir instrukcijų tinkinimas
description: Šiame straipsnyje aprašoma, kaip sukurti ir rodyti pasirinktines instrukcijas kiekvienam kiekvieno užduočių srauto, kurį nustatote sandėlio valdymo mobiliai programai, žingsniui.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: faa9bfa320823664603153601c56654170e7e23a
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334483"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>„Warehouse Management“ mobiliųjų įrenginių programėlės veiksmų pavadinimų ir instrukcijų tinkinimas

> [!IMPORTANT]
> Šiame straipsnyje aprašytos funkcijos taikomos tik naujai sandėlio valdymo mobiliąją programai. Jie neturi įtakos senai sandėlio programai, kuri dabar pasenusi.

Šiame straipsnyje aprašoma, kaip sukurti ir rodyti pasirinktines instrukcijas kiekvienam kiekvieno užduočių srauto, kurį nustatote sandėlio valdymo mobiliai programai, žingsniui. Sandėlio darbuotojams tinkamai parašius instrukcijas, jie gali nedelsdami pradėti naudoti naujus srautus nenaudodami ankstesnio mokymo. Ši funkcija suteikia šiuos patobulinimus:

- **Greičiau įsekite darbuotojus paleisdami juos pagal paprastas kiekvieno užduoties veiksmo instrukcijas.** Kiekvienas srauto veiksmas pateikia instrukcijas, kurios įgalina priekinių eilučių darbuotojus suprasti užduotį.
- **Pateikite instrukcijas, kurios atitinka jūsų procesus.** Parašykite savo instrukcijas, kad jos atitiktų jūsų verslo ir sandėlio procesus. Pavyzdžiui, terminologija tinka jūsų fizinei vietai ir vietinėms santrumpoms.

## <a name="turn-the-warehouse-app-step-instructions-feature-on-or-off"></a>Įjungti arba išjungti sandėlio programos veiksmo instrukcijų funkciją

Šią funkciją galėsite naudoti tik tada, kai ją įjungsite savo sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.29 versiją, *·*[tada](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) administratoriai gali įjungti arba išjungti šią funkciją ieškodami sandėlio programos veiksmų instrukcijų funkcijos funkcijų valdymo darbo srityje.

## <a name="step-titles-and-step-instructions-in-the-app"></a>Žingsnių pavadinimai ir veiksmų instrukcijos programoje

Kiekvienas „Warehouse Management“ „mobile app“ užduočių srauto veiksmas identifikuojamas pagal veiksmo ID. Be to, kiekvienas veiksmas turi pavadinimą, piktogramą ir instrukciją. (Daugiau informacijos rasite [„Warehouse Management“ „mobile app“ piktogramų ir pavadinimų priskyrimo veiksmas](step-icons-titles.md).)

### <a name="step-titles"></a>Žingsnių pavadinimai

*Žingsnio pavadinimas* yra trumpas aprašymas, ką darbuotojas turėtų daryti žingsnio metu. Ekrano viršuje rodomas kaip didelis tekstas, kaip parodyta pateiktoje iliustracijoje.

![Veiksmo piktogramos ir veiksmo pavadinimo pavyzdys „Warehouse Management” „mobile app“](media/wma-step-title.png "Veiksmo piktogramos ir veiksmo pavadinimo pavyzdys „Warehouse Management” „mobile app“")

> [!TIP]
> Dėl didelio teksto dydžio turėtumėte bandyti išlaikyti kuo mažiau žingsnių pavadinimus. Kitu atveju tekstą galima išjungti. Tačiau jei pavadinimas ilgas, darbuotojai vis tiek gali paspausti ir laikyti pavadinimą, kad atidarytų dialogo langą, kuriame rodomas visas tekstas.

### <a name="step-instructions"></a>Veiksmo instrukcijos

Žingsnio *instrukcija* yra ilgesnis aprašymas, kuris suteikia daugiau informacijos apie tai, ką darbuotojas turėtų daryti žingsnio metu. Jis pasirodo iššokaiame dialogo lange, kaip pavaizduota šiame pavyzdyje.

![Veiksmo piktogramos ir veiksmo pavadinimo instrukcija „Warehouse Management” „mobile app“](media/wma-step-instructions.png "Veiksmo piktogramos ir veiksmo pavadinimo instrukcija „Warehouse Management” „mobile app“")

Atsidarius veiksmą, veiksmo instrukcija rodoma automatiškai. Darbuotojai gali atmesti jį visur, už dialogo lango lango ribų. Be to, dialogo lange yra žymės langelis **Daugiau nerodyti** kuriuos darbuotojai gali pasirinkti, norėdami neleisti, kad instrukcija būtų rodoma kitą kartą atliekant tą pačia užduotį.

## <a name="load-the-default-setup"></a>Įkelti numatytąjį nustatymą

Kai pirmą kartą įjungiate *sandėlio programos veiksmo instrukcijų* funkciją, sistemoje nėra jokių pritaikomų veiksmų pavadinimų ar instrukcijų. Todėl, visų pirma, ką turite daryti, yra įkelti numatytąjį nustatymą. Numatytasis nustatymas pateikia tekstus visiems pasiekiamims žingsnių DK visomis palaikomomis kalbomis. Norėdami įkelti numatytąjį nustatymą, atlikite šiuos veiksmus.

1. Eikite į **Warehouse management  \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio veiksmai**.
1. Veiksmų juostoje pasirinkite **Sukurti nustatytąją sąranką**. Į puslapį įrašomas standartinis standartinių veiksmų skaičius.

## <a name="customize-step-titles-and-instructions"></a>Tinkinti žingsnių pavadinimus ir instrukcijas

Jei norite pritaikyti veiksmo pavadinimą ir (arba) instrukciją bet kokiu kalbų skaičiumi, atlikite šiuos veiksmus.

1. Eikite į **Warehouse management  \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio veiksmai**.

    Mobiliojo **įrenginio veiksmų puslapyje** pateikiamas sąrašas visų galimų jūsų sistemos veiksmų. Kiekvieną veiksmo ID galima bendrai naudoti su bet kuriuo mobiliojo įrenginio meniu elementų skaičiumi. Jei veiksmo ID yra bendrai naudojamas keliems meniu elementams, tie patys pavadinimai ir instrukcijos rodomi visiems tiems meniu elementams. Tačiau galite sukurti nepaisymus, kad pritaikytumėte konkrečių meniu elementų pavadinimą ir instrukciją. (Daugiau informacijos žr. kitame skyriuje.)

    Tinklelyje yra šie stulpeliai:

    - **Meniu elemento pavadinimas** – eilutės, kurių šis stulpelis tuščias, naudoja numatytojo veiksmo pavadinimą ir instrukciją, kuri taikoma visiems mobiliojo įrenginio meniu elementams, kurių nepaisoma. Eilutės, kuriose šis stulpelis nustatytas į meniu elemento pavadinimą, turi perrašymus, taikymus tik nurodytam meniu elementui.
    - **Veiksmo ID** – unikalus veiksmo ID.
    - **Įvesties pavadinimas** – pavadinimas, rodomas, kai programai reikia naujos informacijos. Paprastai puslapio laukai yra tušti (tai yra, jie neturi iš anksto nustatytų verčių).
    - **Patvirtinimo pavadinimas** – pavadinimas, rodomas, kai programa reikalauja patvirtinti sistemoje jau saugomą vertę. Paprastai puslapio laukai turi iš anksto nustatytas vertes.

1. Raskite veiksmo **Veiksmo ID** ir **Menu prekės pavadinimas** vertės, kurias norite redaguoti ir rinktis vertę **Veiksmo ID** stulpelyje. Atidarytame puslapyje išvardyti visi galimi pasirinkto veiksmo pavadinimo ir instrukcijos vertimai.
1. Norėdami pritaikyti tekstą bet kuria kalba, atlikite vieną iš šių veiksmų. Abi pasirinktys leidžia redaguoti tekstus esamomis kalbomis. Tačiau tik pirma pasirinktis leidžia pridėti tekstus naujomis kalbomis, o tik antra pasirinktis leidžia peržiūrėti ir redaguoti visų esamų meniu nepaisymus pasirinktą kalbą.

    - Įrankių juostoje, norėdami **atidaryti** dialogo langą, kuriame galite pridėti ar redaguoti tekstus bet kuria palaikoma kalba, pasirinkite Įtraukti. Nustatykite **lauką Nuorodos** kalba į kalbą, kurios vertes norite peržiūrėti. Vertės rodomos kairiajame stulpelyje. Nustatyti vertimo **lauko kalbą** į kalbą, kurią norite pridėti arba pritaikyti. Dešiniajame stulpelyje redaguokite įvesties, **įvesties instrukcijos**, **patvirtinimo antraštės**, **patvirtinimo instrukcijų**, ir **Patvirtinimo instrukcija** laukai, kurių reikia. Tada pasirinkite **Gerai**.
    - Tinklelyje raskite ir pasirinkite eilutę, kurioje **kalbos** laukas nustatomas į kalbą, kurią norite redaguoti. Įrankių juostoje pasirinkite **Peržiūrėti &lt;kalba&gt; šio veiksmo vertimai** tam, kad atidarytumėte dialogo langą, kur galėsite redaguoti visų galimų pasirinktos kalbos nepaisymo tekstą. Dialogo lange yra tinklelis, kuriame yra eilutė ir standartiniams tekstams (kur **meniu elemento pavadinimo** laukas yra tuščias) ir kiekvienam galimaam nepaisymo tekstui (kai **meniu elemento pavadinimo** laukas nustatomas kaip meniu elemento, kuris taikomas perrašymo pavadinimas). Dešiniajame stulpelyje redaguokite įvesties, **įvesties instrukcijos**, **patvirtinimo antraštės**, **patvirtinimo instrukcijų**, ir **Patvirtinimo instrukcija** laukai, kurių reikia. Tada pasirinkite **Gerai**.

1. Tęskite, kol apibrėsite kiekvieną reikiamą kiekvienos reikiamos kalbos pavadinimą ir instrukciją.

## <a name="add-menu-specific-overrides"></a>Pridėti meniu buiščius nepaisymus

Kaip buvo nurodyta ankstesniame skyriuje, galite sukurti bet kokį meniu specialių nepaisymo nuo kiekvieno veiksmo ID skaičių. Galite naudoti šią galimybę, norėdami redaguoti ir pakeisti instrukciją, kad ji geriausiai atitiktų jūsų vietinį verslo procesą tam tikro meniu elemento atžvilgiu. Pavyzdžiui, pardavimo paėmimo atveju, jei jūsų įmonė paprastai darbuotojams pateikia darbo ID išspausdintame dokumente, galite pateikti užuominą, kad darbuotojai turėtų pradėti darbą siųsdami darbo ID.

Kiekvienas nepaisimas taikomas konkrečiam mobiliojo įrenginio meniu elementui ir gali būti bet koks vertimų skaičius. Jei meniu elemento nepaisymo nėra, meniu elementas naudos standartinius tekstus. Jei nepaisymo vertimas pateikiamas kalba, naudojami standartiniai tekstai, net ir meniu elementams, kurių nepaisymai nurodyti kitoms kalboms.

Norėdami sukurti ir konfigūruoti viršijimą, atlikite šiuos žingsnius.

1. Eikite į **Warehouse management  \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio veiksmai**.
1. Tinklelyje raskite ir pasirinkite eilutę, kurios nepaisymus norite sukurti.
1. Veiksmų srityje pasirinkite **Įtraukti veiksmo konfigūraciją**.
1. Išplečiamajame dialogo **Įtraukti veiksmo konfigūravimą** nustatykite lauką **Meniu elementas** kaip mobiliojo įrenginio meniu elemento, kuris taikomas jūsų nepaisymo metu, pavadinimą. Tada pasirinkite **Gerai**.
1. Rodomas puslapis rodo visus tekstus, kurie galimi naujam perrašymui. Iš pradžių sukurta tik viena kalba. Visos kitos kalbos toliau naudos standartinius tekstus, nebent čia pridedate tas kalbas. Redaguokite tekstus ir pridėkite naujas kalbas, kaip aprašyta ankstesniame skyriuje.

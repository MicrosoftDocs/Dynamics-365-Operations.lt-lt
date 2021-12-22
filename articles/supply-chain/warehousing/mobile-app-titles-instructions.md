---
title: „Warehouse Management“ mobiliųjų įrenginių programėlės veiksmų pavadinimų ir instrukcijų tinkinimas
description: Šioje temoje aprašoma, kaip sukurti ir rodyti pasirinktines kiekvieno užduočių srauto, kurį nustatėte „Warehouse Management“ „mobile app“ veiksmui, instrukcijas.
author: Mirzaab
ms.date: 08/11/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ffd433427b2c5011740a7ee54c93713689945df3
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902252"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>„Warehouse Management“ mobiliųjų įrenginių programėlės veiksmų pavadinimų ir instrukcijų tinkinimas

> [!IMPORTANT]
> Šioje temoje aprašomos funkcijos taikomos tik naujai „Warehouse Management“ „mobile app“. Jie neturi įtakos senai sandėlio programai, kuri dabar pasenusi.

Šioje temoje aprašoma, kaip sukurti ir rodyti pasirinktines kiekvieno užduočių srauto, kurį nustatėte „Warehouse Management“ „mobile app“ veiksmui, instrukcijas. Sandėlio darbuotojams tinkamai parašius instrukcijas, jie gali nedelsdami pradėti naudoti naujus srautus nenaudodami ankstesnio mokymo. Ši funkcija suteikia šiuos patobulinimus:

- **Greičiau įsekite darbuotojus paleisdami juos pagal paprastas kiekvieno užduoties veiksmo instrukcijas.** Kiekvienas srauto veiksmas pateikia instrukcijas, kurios įgalina priekinių eilučių darbuotojus suprasti užduotį.
- **Pateikite instrukcijas, kurios atitinka jūsų procesus.** Parašykite savo instrukcijas, kad jos atitiktų jūsų verslo ir sandėlio procesus. Pavyzdžiui, terminologija tinka jūsų fizinei vietai ir vietinėms santrumpoms.

## <a name="turn-on-the-warehouse-app-step-instructions-feature"></a>Sandėlio programos veiksmų instrukcijų funkcijos įjungti

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) nustatymus tam, kad patikrintų funkcijos būseną ir ją įjungtų. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Warehouse management*
- **Funkcijos pavadinimas:** *Sandėlio programos veiksmų instrukcija*

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

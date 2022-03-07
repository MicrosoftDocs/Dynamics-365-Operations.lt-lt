---
title: Atskaitymų valdymas, naudojant atskaitymų darbo sritį
description: Šioje temoje aprašoma, kaip naudoti atskaitymų darbo sritį norint apdoroti klientų mokėjimus su atskaitymais.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: bf98529176fbed368708ea925f542a70f2936037
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500407"
---
# <a name="manage-deductions-using-the-deduction-workbench"></a>Atskaitymų valdymas, naudojant atskaitymų darbo sritį

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip naudoti atskaitymų darbo sritį norint apdoroti klientų mokėjimus su atskaitymais.

Jeigu klientui turi būti grąžinta išmoka, jis gali nuspręsti nelaukti, kada ji bus grąžinta. Vietoj to, klientas gali išsiųsti mokėjimą, kuriame yra įtrauktas grąžintinos sumos atskaitymas. Norėdami apdoroti šio tipo operaciją, galite naudoti atskaitymų darbo sritį atskaitymams sugretinti su atidarytomis kredito operacijomis, jiems skaidyti, atmesti bei nurašyti atskaitymus.

> [!NOTE]
> Atskaitymo darbo sritis ilgą laiką buvo „Microsoft Dynamics 365 Supply Chain Management“ pardavimo ir rinkodaros funkcionalumo dalis. Tačiau jis buvo patobulintas, kad galėtų veikti su naujesniu **Grąžinimo valdymo** moduliu. Šioje temoje aprašoma, kaip naudoti ir senesnes funkcijas ir atskaitymo darbo srityje naudojamas grąžinimo valdymo priemones. Tačiau jei [savo sistemoje neįjungėte **Grąžinimo valdymo** modulio](rebate-management-enable.md), kai kurios čia aprašytos funkcijos jums bus neprieinamos.

## <a name="prerequisites"></a>Būtinieji komponentai

### <a name="set-up-the-old-deduction-management-system"></a>Nustatyti seną atskaitymų valdymo sistemą

Galite naudoti atskaitymo darbo sritį kartu su senomis Supply Chain Management atskaitymo valdymo galimybėmis, net jei nenaudojate **Grąžinimo valdymo** modulio. Tačiau pirmiau turite parengti savo sistemą, kaip aprašyta šiame skyriuje.

Kad būtų galima naudoti atskaitymo darbo sritį, turite užbaigti nustatymo užduotis, aprašytas [Atskaitymų valdymo sąranka](/dynamicsax-2012/appuser-itpro/set-up-deduction-management). Be to, reikėtų turėti kokią nors klientui nustatytą grąžinimo sutartį: kliento grąžinimo, kaip aprašyta [Kliento grąžinimo nustatymas ir priežiūra](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates) arba prekybos nuolaidų grąžinimą.

Jei atskaitymą taikote kliento grąžinimui, turite atlikti šias užduotis:

- [Nustatykite savo kliento grąžinimus](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates).
- Patvirtinkite ir apdorokite grąžinimą, kad būtų galima naudoti atskaitymo darbo grupę.

Jei atskaitymą taikote prekybos nuolaidų grąžinimui, turite atlikti šias užduotis:

- Grąžinamųjų sąskaitų grąžinimų nustatymas.
- Pritaikykite grąžinamųjų sąskaitų grąžinimus.

### <a name="configure-accounts-receivable-and-deductions"></a><a name="accounts-receivable-deductions"></a>Gautinų sumų bei atskaitymų konfigūravimas

Sistema įrašo visus atskaitymo įvykius paraiškos žurnale. Todėl jūsų sistemoje turi būti žurnalas, kuris gali būti naudojamas šiuo tikslu. Jei dar neturite paraiškos žurnalo, nustatykite jį dabar. Šio žurnalo reikia norint sukurti atskaitymus tiesiogiai atskaitymo darbo srityje, klientų sudengimo ar kliento puslapyje.

Norėdami nustatyti naują paraiškos žurnalą, skirtą atskaitymams, atlikite toliau nurodytus veiksmus.

1. Eikite į **Didžioji knyga \> Žurnalo nustatymas \> Žurnalo pavadinimai**.
1. Pasirinkite **Naujas** ir nustatykite šiuos naujo žurnalo pavadinimo laukus:

    - **Pavadinimas** – Įveskite unikalų paraiškos žurnalą identifikuojantį pavadinimą.
    - **Aprašas** – įveskite naujo žurnalo aprašą.
    - **Žurnalo tipas** – pasirinkite *Kasdieninis*.
    - **Kvitų serijos** – priskirkite esamą numeraciją. Arba sukurkite naują numeraciją, kuri turi įmonės aprėptį, ir priskirkite ją naujam žurnalo pavadinimui.

1. Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
1. **Atskaitymai** skirtuke, **Bendrieji** "FastTab" skirtuke nustatykite **Paraiškos žurnalo pavadinimo** lauką pagal ką tik sukurto žurnalo pavadinimą.
1. **Grąžinamas užsakymas** "FastTab" skirtuke nustatykite toliau išvardytus laukus:

    - **Kurti grąžinimo užsakymą** – nustatykite šią pasirinktį, kad nurodydumėte ką sistema turėtų daryti, kai patvirtinama kiekiu pagrįsta paraiška:

        - *Taip* - Kurti grąžinimo užsakymą
        - *Ne* – kurti neigiamą pardavimo užsakymą.

    - **Kūrimas be pridėtos sąskaitos-faktūros** - pasirinkite vertę, norėdami nurodyti, ką sistema turėtų daryti, kai kiekiu pagrįsta paraiška patvirtinama, bet nepridedama jokia sąskaitą-faktūra:

        - *Priimti* – grąžinimo užsakymo kūrimas.
        - *Įspėjimas* – kurti grąžinimo užsakymą, bet rodyti tokį įspėjimo pranešimą: "Paraiška neprijungta prie sąskaitos-faktūros".
        - *Klaida* – nekurti grąžinimo užsakymo ir rodyti tokį klaidos pranešimą: "Paraiška neprijungta prie sąskaitos-faktūros. Naujinimas buvo atšauktas."

    - **Kurti grąžinimo užsakymą prieš atskaitymo patvirtinimą** – nustatykite šią parinktį į *Taip*, jei grąžinimo užsakymai gali būti kuriami prieš patvirtinant paraišką. Šis parametras taikomas tik kiekiu pagrįstoms paraiškoms, kai **Sukurti grąžinimo užsakymą** parinktis nustatyta į *Taip*.

### <a name="configure-general-ledger-parameters"></a>Bendrųjų apskaitos knygos parametrų konfigūravimas

Kai sistema naujam atskaitymui sukūria paraiškos žurnalą, ji taip pat sukuria dvi naujas kliento operacijas: vieną, siekiant kompensuoti paraiškos sumą nuo pradinės sąskaitos sumos, o kitą – kliento skolai užregistruoti kaip naujo atskaitymo sumą (nes reikalavimas dar nebuvo patvirtintas). Todėl turite nustatyti savo sistemą, kad viename kvite būtų kelios klientų eilutės.

Norėdami įgalinti vieną kvitą su keliomis kliento eilutėmis, atlikite šiuos veiksmus.

1. Eikite į **Didžioji knyga \> Didžiosios knygos nustatymas \> DK parametrai**.
1. **Didžioji knyga** skirtuke **Bendra** "FastTab" nustatykite pasirinktį **Leisti kelias operacijas viename kvite** parinktį į *Taip*.
1. Jei gaunate perspėjimo pranešimą, pasirinkite **Uždaryti** kad priimtumėte pakeitimą.

### <a name="create-deduction-reasons"></a><a name="deduction-reasons"></a>Kurti atskaitymo priežastis

Sistema reikalauja, kad vartotojai nurodytų kiekvieno atskaitymo, kurį jie tiesiogiai įveda atskaitymo darbo dalyje, kliento sudengimo ar kliento puslapyje, priežastį. Priežastis nurodo, kaip tvarkomas atskaitymas, kai jis patvirtinamas.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų priežastis**.
1. Pasirinkite **Naujas** tam, kad įtrauktumėte į tinklelį eilutę ir tada nustatytumėte tolesnes vertes:

    - **Paraiškos priežastis** – Įveskite unikalų priežasties pavadinimą.
    - **Aprašymas** – Įveskite priežasties aprašymą, jei norite pateikti daugiau informacijos apie jo naudojimą.
    - **Paraiškos pagrindas** – pasirinkite paraiškos pagrindą dėl paraiškos priežasties:

        - *Kaina pagal* – Kurti laisvos formos kreditą prieš patvirtinimą.
        - *Pagal kiekį* – kurti neigiamą pardavimo užsakymą arba grąžinimo užsakymą prieš patvirtinimą.

    - **Grąžinimo priežasties kodas** – pasirinkite grąžinimo priežasties kodą kaip **Grąžinimo priežasties kodo** vertę grąžinimo užsakyme.
    - **Tipas** – pasirinkite atskaitymo tipą. **Atskaitymo korespondentinė** vertė pasirinktam tipui bus naudojama norint nustatyti **Atskaitymo korespondentinį** lauką, kai sukuriamas atskaitymas arba reikalavimas. Atskaitymų tipai nustatomi **Atskaitymų tipai** puslapyje (**Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų tipai**).
    - **Paraiškos registravimo paskyra** – Šis laukas galimas tik tada, kai **Paraiškos pagrindo** laukas nustatytas į *Pagrįsta kaina*. Kai kaina pagrįsta paraiška patvirtinama, sistema priskiria čia jūsų pasirinktą didžiosios knygos paskyrą **Pagrindinės paskyros** vertę kaip juodraščio laisvos formos kredito pastabą.

### <a name="set-up-the-settle-approved-deductions-periodic-task"></a>Nustatyti sudengtų patvirtintų atskaitymų periodinę užduotį

Atskaitymams, kurie sukuriami naudojant komandą **Naujas atskaitymas** atskaitymo darbo srityje, kliento sudengimo arba kliento puslapyje, galite nustatyti *Sudengti patvirtintus atskaitymus* periodinę užduotį, kad automatiškai atitiktų atskaitymus ir kreditus, kurie atitinka **Atskaitymo ID** vertes ir sumas.

Norėdami suplanuoti šią užduotį, eikite į **Pardavimo rinkodara \> Periodinės užduotys \> Nustatyti patvirtintus atskaitymus** ir nustatykite pasirinktis, filtrus ir grafiką, kaip ir kitų periodinių užduočių.

> [!NOTE]
> Jei **Automatinis sudengimas** parinktis nustatyta į *Taip* **Sudengimas** skirtuke **Gautinų sumų parametrų** puslapyje (**Gautinos sumos \> Sąranka \> Gautinų sumų nustatymo parametrai**), *Sudengti patvirtinti atskaitymai* periodinė užduotis nieko nedarys, nes kreditas bus automatiškai sudengtas.

## <a name="create-a-deduction"></a>Atskaitymo kūrimas

### <a name="create-a-deduction-journal-entry-by-using-the-customer-payment-journal"></a>Kurti atskaitymų žurnalo įrašą naudojant kliento mokėjimų žurnalą

Norėdami sukurti atskaitymų žurnalo įrašą atlikite nurodytus veiksmus.

1. Eikite į **Gautinos sumos \> Mokėjimai \> Klientų mokėjimo žurnalas**.
1. Pasirinkite **Naujas** tam, kad įtrauktumėte eilutę į tinklelį.
1. Naujai eilutei **Pavadinimas** laukelyje pasrinkite žurnalo pavadinimą.
1. Veiksmų srityje pasirinkite **Eilutės**.
1. Įveskite datą, įmonės sąskaitą ir kliento sąskaitos numerį.
1. **Sąskaita** lauke pasirinkite sąskaitą faktūrą, su kuria yra susietas atskaitymas.
1. **Kreditas** laukelyje įveskite kliento sumokėtą sumą.
1. Pasirinkite **OK** norėdami patvirtinti, kad suma yra mažesnė už bendrą pažymėtos operacijos sumą.
1. Pasirinkite korespondentinės sąskaitos tipą ir korespondentinę sąskaitą.
1. Įrankių juostoje virš tinklelio pasirinkite **Atskaitymai**.
1. **Atskaitymai** puslapyje Veiksmų juostoje pasirinkite **Naujas** kad įtrauktumėte eilutę tinklelyje. **Atskaitymo ID** laukas automatiškai nustatomas naujai eilutei.
1. Laukelyje **Tipas** pasirinkite atskaitymų tipą.
1. **Suma** laukelyje įveskite sumą, kuri nurodyta **Likutis** laukelyje žemiau atskaitymų sąrašo. Ši suma rodo sumą, kurią klientas atėmė iš mokėjimo.
1. Uždarykite **Atskaitymai** puslapį. Esate grąžinamas į **Kliento mokėjimų** puslapį, kuriame dabar rodoma nauja atskaitymo eilutė.
1. Veiksmų srityje pasirinkite **Patvirtinti \> Patvirtinti**. Turėtumėte gauti tokį pranešimą: „Žurnale problemų nėra“.
1. Veiksmų srityje pasirinkite **Registruoti**.

### <a name="create-a-deduction-by-using-the-deduction-workbench"></a>Sukurkite atskaitymą naudojant atskaitymų darbo sritį

Norėdami sukurti naują atskaitymą, atskaitymų darbo srityje atlikite nurodytus veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Veiksmų srityje pasirinkite **Prižiūrėti \> Naujas atskaitymas**.

    Dialogo lange **Naujas atskaitymas** **Atskaitymo ID** laukas nustatytas, remiantis **Atskaitymų ID** numerio seka, kuri apibrėžta **Prekybos išmokos parametrų** puslapyje (**Pardavimai ir rinkodara\> Sąranka \> Prekybos išmokos \> Prekybos išmokų valdymo parametrai**).

1. Užpildykite toliau nurodytus laukus:

    - **Kliento paskyra** – pasirinkite kliento sąskaitą, kuriai taikomas atskaitymas.
    - **Išorinės paraiškos numeris** – įveskite kliento paraiškos nuorodą.
    - **Paraiškos suma** – įveskite į mokesčius įtraukiamo reikalavimo sumą. Vertė turi būti teigiama.
    - **Valiuta** – pasirinkite atskaitymo valiutą. Numatytoji vertė yra valiuta, kuri nustatyta pasirinktam kliento abonementui.
    - **Paraiškos pagrindas** – pasirinkite paraiškos pagrindą. Pagal paraišką nustatomas kredito operacijos, sukurtos pritaikius atskaitymą arba paraišką, tipas.

        - *Kaina pagrįsta* – bus sukurta laisvos formos juodraštinė sąskaita faktūra.
        - *Pagal kiekį* – bus sukurtas neigiamas pardavimo užsakymas arba grąžinimo užsakymas.

    - **Paraiškos data** – pasirinkite paraiškos datą. Numatytoji vertė yra dabartinė data.
    - **Paraiškos priežastis** – pasirinkite priežasties kodą, kuris taikomas dabartiniam atskaitymui. Pasirinktas reikalavimo pagrindas turi įtakos taikomos pasirinktims. Daugiau informacijos apie tai, kaip kurti ir konfigūruoti paraiškos priežastis, kurias čia galite pasirinkti, žr. šios temos skyriuje [Kurti atskaitymų priežastis](#deduction-reasons).
    - **Pastabos** – pridėkite bet kokias taikomas pastabas. Patvirtinus paraišką, tvirtintojas galės redaguoti arba pridėti prie jos pastabų.
    - **Kurti ataskaitų žurnalą** - nustatykite šią pasirinktį norėdami nurodyti, ar kuriant paraišką ar atskaitymą turi būti sukurtas ataskaitų žurnalas:

        - *Taip* – sistema sukurs ir užregistruos bendrąjį žurnalą, naudodama paraiškos žurnalą, kuris nustatytas **Gautinų sumų parametrų** puslapyje. (Daugiau informacijos ieškokite [Anksčiau šioje temoje konfigūruokite](#accounts-receivable-deductions) gautinų sumų ir atskaitymų skyrių.) Kai prie jos pridėta sąskaita, naudojamas taikomos sąskaitos balansai sumažinti. Jei vėliau paraiška atmetama, bus atšauktas paraiškos žurnalas ir sudengimas (jei sąskaita faktūra buvo pridėta).
        - *Ne* – šiuo metu nekuriamas joks žurnalas. Jis bus sukurtas patvirtinus paraišką. Sąskaitą faktūrą vis tiek galima pridėti prie naujos paraiškos, net jei jis nesukurtas. Tačiau sudengimo be paraiškos žurnalo atlikti negalima.

1. Pasirinkite **Gerai**.

    Sukuriamas naujas atskaitymas. Jei nustatote **Kurti paraiškos žurnalo** parinktį į *Taip*, užregistruojamos šios operacijos:

    - **Dvi naujos kliento operacijos** – viena operacija sudengia prašymo sumą pagal pradinę sąskaitą. Kita operacija užregistruoja kliento skolą paraiškos sumai, nes ji dar nėra patvirtinta. Pradinės sąskaitos operacija ir korespondentinės sąskaitos faktūros operacija bus automatiškai pažymėta sudengti, kai pridėsite sąskaitą veiksmų srityje pasirinkdami **Tvarkyti \> Pridėti sąskaitą**.
    - **Dvi korespondentinės operacijos** – šios operacijos registruojamos **Atskaitymo korespondentinėje** didžiosios knygos paskiroje.
    - **Paraiškos žurnalas** – norėdami peržiūrėti kiekvieno atskaitymo darbo dalyje rodomo atskaitymo pasiūlymų žurnalą, pasirinkite skirtuką **Nuorodos**. Paraiškų žurnalas rodomas **Žurnalo paketo numeris** lauke. Be to, paraiškų žurnalą galite peržiūrėti **Atskaitymų įvykių** skirtuke. Ten bus **Atnaujinimo tipo** vertė nuo *Sugretinti*.

### <a name="create-a-deduction-from-a-customer-settlement"></a>Atskaitymo iš kliento sudengimo kūrimas

Atskaitymo iš kliento sudengimo sukūrimo procesas yra panašus į atskaitymo sukūrimo procesą, naudojant atskaitymo darbo sritį. Tačiau kliento ir sąskaitos valiuta nustatoma automatiškai ir sąskaita pridedama. Nereikia pasirinkti **Tvarkyti \> Pridėti sąskaitą** veiksmų srityje, kai kuriate paraišką arba atskaitymą naudodami klientų sudengimo puslapį.

1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.
1. Pasirinkite klientą, jei norite atskaitymą.
1. Veiksmų srities skirtuko **Surinkimas** grupėje **Sudengimas** spustelėkite **Sudengimo operacijos**.
1. Dialogo lange **Nustatyti operacijas**, skirtuke **Peržiūra** pasirinkite sąskaitą, pagal kuria norite sukurti atskaitymą.
1. Įrankių juostoje pasirinkite **Atskaitymai \> Naujas atskaitymas**.

    Dialogo lange **Naujas atskaitymas** **Atskaitymo ID** laukas nustatytas, remiantis **Atskaitymų ID** numerio seka, kuri apibrėžta **Prekybos išmokos parametrų** puslapyje (**Pardavimai ir rinkodara\> Sąranka \> Prekybos išmokos \> Prekybos išmokų valdymo parametrai**). **Kliento paskyra** laukas nustatytas kaip kliento sąskaitą, kuriai taikomas atskaitymas.

1. Užpildykite toliau nurodytus laukus:

    - **Išorinės paraiškos numeris** – įveskite kliento paraiškos nuorodą.
    - **Paraiškos suma** – įveskite į mokesčius įtraukiamo reikalavimo sumą. Vertė turi būti teigiama.
    - **Valiuta** – pasirinkite atskaitymo valiutą. Numatytoji vertė yra valiuta, kuri nustatyta pasirinktam kliento abonementui.
    - **Paraiškos pagrindas** – pasirinkite paraiškos pagrindą. Pagal paraišką nustatomas kredito operacijos, sukurtos pritaikius atskaitymą arba paraišką, tipas.

        - *Kaina pagrįsta* – bus sukurta laisvos formos juodraštinė sąskaita faktūra.
        - *Pagal kiekį* – bus sukurtas neigiamas pardavimo užsakymas arba grąžinimo užsakymas.

    - **Paraiškos data** – pasirinkite paraiškos datą. Numatytoji vertė yra dabartinė data.
    - **Paraiškos priežastis** – pasirinkite priežasties kodą, kuris taikomas dabartiniam atskaitymui. Pasirinktas reikalavimo pagrindas turi įtakos taikomos pasirinktims. Daugiau informacijos apie tai, kaip kurti ir konfigūruoti paraiškos priežastis, kurias čia galite pasirinkti, žr. šios temos skyriuje [Kurti atskaitymų priežastis](#deduction-reasons).
    - **Pastabos** – pridėkite bet kokias taikomas pastabas. Patvirtinus paraišką, tvirtintojas galės redaguoti arba pridėti prie jos pastabų.
    - **Kurti ataskaitų žurnalą** - nustatykite šią pasirinktį norėdami nurodyti, ar kuriant paraišką ar atskaitymą turi būti sukurtas ataskaitų žurnalas:

        - *Taip* – sistema sukurs ir užregistruos bendrąjį žurnalą, naudodama paraiškos žurnalą, kuris nustatytas **Gautinų sumų parametrų** puslapyje. (Daugiau informacijos ieškokite [Anksčiau šioje temoje konfigūruokite](#accounts-receivable-deductions) gautinų sumų ir atskaitymų skyrių.) Kai prie jos pridėta sąskaita, naudojamas taikomos sąskaitos balansai sumažinti. Jei vėliau paraiška atmetama, bus atšauktas paraiškos žurnalas ir sudengimas (jei sąskaita faktūra buvo pridėta).
        - *Ne* – šiuo metu nekuriamas joks žurnalas. Jis bus sukurtas patvirtinus paraišką. Sąskaitą faktūrą vis tiek galima pridėti prie naujos paraiškos, net jei jis nesukurtas. Tačiau sudengimo be paraiškos žurnalo atlikti negalima.

1. Pasirinkite **Gerai**.

    Sukuriamas naujas atskaitymas. Jei nustatote **Kurti paraiškos žurnalo** parinktį į *Taip*, užregistruojamos šios operacijos:

    - **Dvi naujos kliento operacijos** – viena operacija sudengia prašymo sumą pagal pradinę sąskaitą. Kita operacija užregistruoja kliento skolą paraiškos sumai, nes ji dar nėra patvirtinta. Pradinės sąskaitos operacija ir korespondentinės sąskaitos faktūros operacija bus automatiškai pažymėta sudengti, kai pridėsite sąskaitą veiksmų srityje pasirinkdami **Tvarkyti \> Pridėti sąskaitą**.
    - **Dvi korespondentinės operacijos** – šios operacijos registruojamos **Atskaitymo korespondentinėje** didžiosios knygos paskiroje.
    - **Paraiškos žurnalas** – norėdami peržiūrėti kiekvieno atskaitymo darbo dalyje rodomo atskaitymo pasiūlymų žurnalą, pasirinkite skirtuką **Nuorodos**. Paraiškų žurnalas rodomas **Žurnalo paketo numeris** lauke. Be to, paraiškų žurnalą galite peržiūrėti **Atskaitymų įvykių** skirtuke. Ten bus **Atnaujinimo tipo** vertė nuo *Sugretinti*.

    Jūs grąžintas į puslapį **Sudengtos operacijos**, kuriame dabar rodoma pasirinkta sąskaita kaip pažymėta. **Registruoti** mygtukas galimas tik tada, jei nustatote **Kurti paraiškos žurnalo** parinktį į *Taip*. Jei tai galima, pasirinkite **Registruoti** kad sumažinumėte sąskaitos likutį pagal **Paraiškos sumos** vertę.

### <a name="create-a-deduction-from-a-customer-page"></a>Atskaitymo iš kliento puslapio sudengimo kūrimas

Atskaitymo iš kliento puslapio sudengimo sukūrimo procesas yra panašus į atskaitymo sukūrimo procesą, naudojant atskaitymo darbo sritį. Tačiau klientas nustatomas automatiškai.

1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.
1. Pasirinkite klientą, jei norite atskaitymą.
1. Veiksmų srityje, skirtuke **Surinkimas**, grupėje **Atskaitymai** pasirinkite **Sukurti atskaitymus**.

    Dialogo lange **Naujas atskaitymas** **Atskaitymo ID** laukas nustatytas, remiantis **Atskaitymų ID** numerio seka, kuri apibrėžta **Prekybos išmokos parametrų** puslapyje (**Pardavimai ir rinkodara\> Sąranka \> Prekybos išmokos \> Prekybos išmokų valdymo parametrai**). **Kliento paskyra** laukas nustatytas kaip kliento sąskaitą, kuriai taikomas atskaitymas.

1. Užpildykite toliau nurodytus laukus:

    - **Išorinės paraiškos numeris** – įveskite kliento paraiškos nuorodą.
    - **Paraiškos suma** – įveskite į mokesčius įtraukiamo reikalavimo sumą. Vertė turi būti teigiama.
    - **Valiuta** – pasirinkite atskaitymo valiutą. Numatytoji vertė yra valiuta, kuri nustatyta pasirinktam kliento abonementui.
    - **Paraiškos pagrindas** – pasirinkite paraiškos pagrindą. Pagal paraišką nustatomas kredito operacijos, sukurtos pritaikius atskaitymą arba paraišką, tipas.

        - *Kaina pagrįsta* – bus sukurta laisvos formos juodraštinė sąskaita faktūra.
        - *Pagal kiekį* – bus sukurtas neigiamas pardavimo užsakymas arba grąžinimo užsakymas.

    - **Paraiškos data** – pasirinkite paraiškos datą. Numatytoji vertė yra dabartinė data.
    - **Paraiškos priežastis** – pasirinkite priežasties kodą, kuris taikomas dabartiniam atskaitymui. Pasirinktas reikalavimo pagrindas turi įtakos taikomos pasirinktims. Daugiau informacijos apie tai, kaip kurti ir konfigūruoti paraiškos priežastis, kurias čia galite pasirinkti, žr. šios temos skyriuje [Kurti atskaitymų priežastis](#deduction-reasons).
    - **Pastabos** – pridėkite bet kokias taikomas pastabas. Patvirtinus paraišką, tvirtintojas galės redaguoti arba pridėti prie jos pastabų.
    - **Kurti ataskaitų žurnalą** - nustatykite šią pasirinktį norėdami nurodyti, ar kuriant paraišką ar atskaitymą turi būti sukurtas ataskaitų žurnalas:

        - *Taip* – sistema sukurs ir užregistruos bendrąjį žurnalą, naudodama paraiškos žurnalą, kuris nustatytas **Gautinų sumų parametrų** puslapyje. (Daugiau informacijos ieškokite [Anksčiau šioje temoje konfigūruokite](#accounts-receivable-deductions) gautinų sumų ir atskaitymų skyrių.) Kai prie jos pridėta sąskaita, naudojamas taikomos sąskaitos balansai sumažinti. Jei vėliau paraiška atmetama, bus atšauktas paraiškos žurnalas ir sudengimas (jei sąskaita faktūra buvo pridėta).
        - *Ne* – šiuo metu nekuriamas joks žurnalas. Jis bus sukurtas patvirtinus paraišką. Sąskaitą faktūrą vis tiek galima pridėti prie naujos paraiškos, net jei jis nesukurtas. Tačiau sudengimo be paraiškos žurnalo atlikti negalima.

1. Pasirinkite **Gerai**.

    Sukuriamas naujas atskaitymas. Jei nustatote **Kurti paraiškos žurnalo** parinktį į *Taip*, užregistruojamos šios operacijos:

    - **Dvi naujos kliento operacijos** – viena operacija sudengia prašymo sumą pagal pradinę sąskaitą. Kita operacija užregistruoja kliento skolą paraiškos sumai, nes ji dar nėra patvirtinta. Pradinės sąskaitos operacija ir korespondentinės sąskaitos faktūros operacija bus automatiškai pažymėta sudengti, kai pridėsite sąskaitą veiksmų srityje pasirinkdami **Tvarkyti \> Pridėti sąskaitą**.
    - **Dvi korespondentinės operacijos** – šios operacijos registruojamos **Atskaitymo korespondentinėje** didžiosios knygos paskiroje.
    - **Paraiškos žurnalas** – norėdami peržiūrėti kiekvieno atskaitymo darbo dalyje rodomo atskaitymo pasiūlymų žurnalą, pasirinkite skirtuką **Nuorodos**. Paraiškų žurnalas rodomas **Žurnalo paketo numeris** lauke. Be to, paraiškų žurnalą galite peržiūrėti **Atskaitymų įvykių** skirtuke. Ten bus **Atnaujinimo tipo** vertė nuo *Sugretinti*.

## <a name="create-a-credit-note-for-a-customer"></a>Kaip sukurti kliento kredito pažymą

Esant patvirtintam kliento grąžinimui, kliento sąskaitoje sukurkite kredito pažymą, susijusią su grąžinimu. Po to kreditas parodomas atskaitymų darbo srityje, kur jį galima sugretinti su atskaitymu.

Norėdami sukurti kredito pažymą atlikite nurodytus veiksmus.

1. Eikite į **Pardavimas ir rinkodara \> Klientai \> Visi klientai**.
1. Pasirinkite klientą.
1. Veiksmų srities skirtuko **Surinkimas** grupėje **Sudengimas** spustelėkite **Sudengimo operacijos**.
1. Dialogo lange **Sudengimo operacijos** pasirinkite operaciją, pagal kurią buvo pritaikytas grąžinimas.
1. Įrankių juostoje **Funkcijos** meniu pasirinkite grąžinimo programos tipą, kuris taikomas.
1. **Grąžinimo** puslapyje, skirtuke **Peržiūra** pasirinkite **Žymėti** žymės langelį, esantį šalia grąžinimo ID.
1. Veiksmų srityje pasirinkite **Funkcijos \> Kurti kredito pažymą**.

## <a name="process-a-deduction-on-the-deduction-workbench"></a>Apdorokite atskaitymą atskaitymų darbo srityje

Atskaitymų darbo srityje galite sugretinti atskaitymus su atidarytomis kredito operacijomis, išskaidytais, atmestais ir nurašytais atskaitymais.

Atsižvelgdami į tai, kaip norite apdoroti atskaitymą, atlikite vieną ar daugiau iš šių procedūrų nurodytų šiose poskyriuose: Jei reikia, procedūras galima sujungti. Pvz., galite padalyti atskaitymą į dvi dalis, tada sugretinti vieną dalį su kreditu, o likusią dalį palikti darbo srityje, kad vėliau būtų sugretinta su kitu kreditu. Be to, galite sugretinti atskaitymą su kreditu, kuris yra mažesnis nei atskaitymo suma, tada atmesti arba nurašyti atskaitymo likutį.

### <a name="match-a-deduction-to-a-credit"></a>Sugretinkite atskaitymą su kreditu

Norėdami sugretinti atskaitymą su kreditu, atlikite šiuos veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Pasirinkite **Pažymėti** žymės langelį, kad būtų apdorotas atskaitymas.
1. Skyriuje **Atviros operacijos** **pažymėkite** žymės langelį, kad kreditas atitiktų atskaitymą. Jei išvardyta keletas kreditų, galite pasirinkti daugiau nei vieną kreditą norėdami sugretinti su atskaitymu. Jei norite, kad sistema automatiškai pasirinktų kreditus, kurie atitinka atskaitymo sumą, įrankių juostoje pasirinkite atitinkamą pasirinktį **Pasirinkti atskaitymo sumą** meniu.
1. Veiksmų srityje pasirinkite **Tvarkyti \> Gretinti**. Sistema sugretina atskaitymą su kreditu. Jei balansas lieka atskaityme, jis rodomas skirtuko **Likusi suma** laukelyje **Atskaitymai** skirtuke.

    > [!NOTE]
    > Atskaitymams, kurie buvo sukurti naudojant komandą **Nauji atskaitymai** atskaitymų darbo sityje, kliento sudengimo arba kliento puslapyje **Tvarkyti \> Sugretinti** komanda galima tik jei **paraiškos būsenos** laukas nustatytas į *Priimta*. Šią komandą galima naudoti norint rankiniu būdu sugretinti kaina arba kiekiu grindžiamą operaciją su susijusiu kreditu skyriuje **Atviros operacijos**. Šis kreditas sukuriamas arba kai atskaitymas patvirtinamas (naudojant **Tvarkyti \> Patvirtinti atskaitymus** komanda), arba kai jis pridedamas prie esamo kredito, kaip aprašyta toliau šios temos skyriuje Patvirtinimo atskaitymų procesas sukurtame [Kreditai sukurti ne patvirtinamų atskaitymų procese](#credits-outside-approval). *Sudengti patvirtintus atskaitymus* periodinė užduotis (**Pardavimų rinkodara \> Periodinė užduotis \> Sudengti patvirtintus atskaitymus**) taip pat gali būti naudojama, norint automatiškai sugretinti atskaitymus ir kreditus, kurie turi atitinkamas **Atskaitymų ID** vertes ir sumas.

### <a name="split-a-deduction"></a>Atskaitymo išskaidymas

Norėdami išskaidyti atskaitymą, atlikite šiuos veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Pasirinkite **Pažymėti** žymės langelį, kad būtų apdorotas atskaitymas.
1. Veiksmų srityje pasirinkite **Tvarkyti \> Išskaidyti**.
1. Dialogo lange **Skaidymas** laukelyje **Išskaidyta suma** įveskite sumą, kurią reikia išskaidyti iš pagrindinio atskaitymo. Tada pasirinkite **Gerai**.
1. Skirtuke **Atskaitymai** atkreipkite dėmesį, kad atsiranda naujas išskaidytos sumos įrašas. Pradiniame atskaitymo įraše yra atskaitymo balanso likutis. Dabar galite atskirai tvarkyti dvi pradinio grąžinimo dalis.
1. Pasirinkite pradinį atskaitymo įrašą, tada pasirinkite skirtuką **Nuorodos**. Lauke **Išskaidyta suma** rodoma suma, kuri buvo išskaidyta nuo pradinės sumos.

### <a name="attach-an-invoice-to-a-deduction"></a>Prie atskaitymo pridėkite sąskaitą-faktūrą

Prie atskaitymo galite pridėti sąskaitą-faktūrą, jei atskaitymas buvo sukurtas naudojant komandą **Naujas atskaitymas** atskaitymų darbo srityje, kliento sudengimo arba kliento puslapyje, ir jei šiuo metu prie jo neprijungta jokia sąskaita-faktūra (tai yra **Sąskaita** stulpelis yra tuščias).

Norėdami prie atskaitymo pridėti sąskaitą-faktūrą, atlikite šiuos veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Pasirinkite **Pažymėti** žymės langelį, kad būtų apdorotas atskaitymas.
1. Veiksmų srityje pasirinkite **Prižiūrėti \> Pridėti sąskaitą-faktūrą**.
1. Dialogo lange **Pridėti sąskaitą-faktūrą** pasirinkite sąskaitą ir pasirinkite **OK**.
1. Dialogo lange **Sudengimo operacijos** atlikite vieną iš šių veiksmų, atsižvelgdami į tai, ar kuriant atskaitymą buvo užregistruotas paraiškos žurnalas:

    - Jei buvo užregistruotas paraiškos žurnalas, jūsų pasirinkta sąskaita-faktūra ir žurnalo kliento kredito operacija rodo varnelę stulpelyje **Žymėti**. Pasirinkite **Registruoti**. Likęs pridėtos sąskaitos-faktūros balansas yra sumažinamas pagal paraišką.
    - Jei paraiškos žurnalas nebuvo registruojamas, stulpelyje **Žymėti** jokia operacija varnele nebus pažymėta. Kadangi negalima iš naujo nustatyti paraiškos žurnalo, kol atskaitymas nebus patvirtintas, pasirinkite **Atšaukti**.

### <a name="detach-an-invoice-from-a-deduction"></a>Nuo atskaitymo nuimkite sąskaitą-faktūrą

Nuo atskaitymo galite nuimti sąskaitą-faktūrą, jei atskaitymas buvo sukurtas naudojant **Naujas atskaitymas** atskaitymų darbo srityje, kliento sudengimo arba kliento puslapyje, ir jei šiuo metu yra prijungta sąskaita-faktūra (tai yra **Sąskaitos** stulpelis rodo sąskaitos-faktūros numerį), ir jei **Paraiškos būsena** laukelis nustatytas į *Atidaryti*. Turėtumėte atlikti šią užduotį, nes buvo pridėta netinkama sąskaitą-faktūrą. Sąskaita-faktūra pašalinama iš atskaitymo, o likęs balansas atnaujinamas, jei jis buvo sumažintas, kai buvo pridėta sąskaita.

Norėdami atskirti sąskaitą-faktūrą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Pasirinkite **Pažymėti** žymės langelį, kad būtų apdorotas atskaitymas.
1. Veiksmų srityje pasirinkite **Prižiūrėti \> Atskirti sąskaitą-faktūrą**.

### <a name="approve-a-deduction"></a>Atskaitymo patvirtinimas

Galite patvirtinti atskaitymus, kurie buvo sukurti naudojant komandą **Naujas atskaitymas** darbo srityje, kliento sudengimo arba kliento puslapyje. Tačiau galite patvirtinti tik atskaitymus, kurių **Paraiškos būsena** laukelis nustatytas į *Atidaryta*.

Norėdami patvirtinti atskaitymą, atlikite šiuos veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Pasirinkite **Pažymėti** žymės langelį, kad būtų apdorotas atskaitymas.
1. Veiksmų srityje pasirinkite **Prižiūrėti \> Patvirtinti atskaitymą**.
1. Dialogo lange **Atskaitymo patvirtinimas** redaguokite arba pridėkite informaciją prie **Pastabos** vertės, jei reikia.
1. Jei atskaitymas pagrįstas kaina ir prie jo nebuvo pridėta sąskaita-faktūra, pasirinkite prekės mokesčio grupę. Paprastai mokesčio prekių grupė nurodoma sąskaitoje-faktūroje. Todėl mokesčio prekės kodas turi būti nurodytas, kai nėra pridėtos sąskaitos-faktūros.
1. Pasirinkite **Gerai**.

    Šiuo metu atskaitymui negali būti daromi jokie pakeitimai. Jei **Kurti paraiškos žurnalą** parinktis buvo nustatyta į *Ne* kai buvo kuriamas atskaitymas, paraiškos žurnalas sukuriamas ir registruojamas, kai patvirtinamas atskaitymas. Patvirtinus atskaitymą, kreditas automatiškai sukuriamas ir atidaromas. Tipas priklauso nuo atskaitymo **Paraškos būsenos** vertės:

    - *Remiantis kaina* – jei atskaitymas pagrįstas kaina, sukuriama laisvos formos sąskaita kliento paskyrai. Galite pridėti aprašymą ir registruoti kreditą. Kai sukuriamas juodraštis, atskaitymai užpildomi šiais laukais:

        - **Atskaitymo ID** – šis laukas įtraukiamas į antraštę, kad būtų galima grąžinti atskaitymą.
        - **Pagrindinė sąskaita** - vertė nustatoma pagal **Paraiškos registravimo paskyros** vertę, kuri nustatyta atskaitymo priežasčiai, kuri priskirta tam atskaitymui.
        - **Prekės pardavimo mokesčių grupė** – vertė nustatoma pagal pridėtą sąskaitą arba vertę, pasirinktą patvirtinus atskaitymą.
        - **Vieneto kaina** – vertė yra atskaitomo prašymo sumos kreditas.
        - **Sąskaitos-faktūros tekstas** – pagal numatytąjį nustatymą šis laukas nustatomas į atskaitymo **Pastabos** vertę.

    - *Pagal kiekį* – jei atskaitymas yra pagrįstas kiekiu, sukuriamas atviras pardavimo užsakymas arba grąžinimo užsakymas. **Sukurti grąžinimo užsakymą** nustatymas **[Gautinų sumų parametrai](#accounts-receivable-deductions)** puslapyje apibrėžiama ar sukūrus atskaitymą sukurtas pardavimo, ar grąžinimo užsakymas. Pasirodo **Kopijuoti užsakymus** puslapis ir jis filtruojamas, siekiant parodyti eiles, kur **Sąskaitos paskyra** laukelis nustatytas į atskaitymų kliento paskyra. Atlikite šiuos veiksmus.

        1. FastTab **Isąskaitos** **Antraštės** skyrius rodo pardavimų sąskaitas, kur **sąskaitos paskyra** vertė atitinka atskaitymo kliento paskyrą. Pasirinkite taikomą pardavimo sąskaitą-faktūrą.
        1. **Eilučių** skyrius rodo eilutes iš pasirinktos pardavimo sąskaitos. Pažymėkite žymės langelį **Pasirinkti** kiekvienai eilutei, kurią norite kopijuoti. Arba **Antraštės** skiltyje pasirinkite **Žymėti viską** žymos langelį pardavimo užsakymui, kad pasirinktumėte visas jo eilutes.
        1. Koreguoti vienos ar daugiau eilučių **Kiekio** vertę, jei reikia.

            Visos iki šiol pasirinktos eilutės yra išvardytos **Pasirinktose eilutėse arba antraštėje, kuri turi būti kopijuojama** "FastTab".

        1. Pakartokite ankstesnius du reikiamus veiksmus, kol visos būtinos eilutės bus išvardytos **Pasirinktose eilutėse arba antraštėje, kurias reikia kopijuoti** "FastTab".
        1. Pasirinkite **Gerai**.

            Atidaromas naujas grąžinimo užsakymas ir automatiškai nustatomi šie laukai:

            - **Atskaitymo ID** – šis laukas įtraukiamas į antraštę, kad būtų galima grąžinti atskaitymą.
            - **Grąžinimo priežasties kodas** - pagal numatytuosius nustatymus šiame lauke nustatoma **Grąžinimo priežasties kodo** vertė, kuri nustatyta pagal atskaitymo priežastį, kuri priskirta atskaitymui.

Pateikus kredito sąskaitą-faktūrą, tai matosi **Atviros operacijos** skiltyje atskaitymų darbo srityje prieš taikomą **Atskaitymo ID** vertę ir jos **paraiškos tipas** laukelis nustatytas į *Kiti kreditai*. Kreditas bus galimas, kol nebus sugretintas su atskaitymu vienu iš šių būdų:

- Galite sugretinti rankiniu būdu veiksmų srityje **Tvarkyti \> Gretinti**.
- Jis automatiškai sudengiamas, pasirenkiant *Sudengti patvirtintas paraiškas* periodinis darbas (**Pardavimo ir rinkodaros \> Periodinės užduotys \> Sudengti patvirtintas paraiškas**).
- Jis sudengiamas automatiškai, nes **Automatinio sudengimo** parinktis **Sudengimas** skirtuke **Gautinų paskyrų parametrai** puslapyje yra nustatytas į *Taip*.

Norėdami peržiūrėti kreditą, kuris sukuriamas patvirtinus atskaitymą, taip pat galite naudoti **Atviras kreditas** mygtuką, esantį **Atviros operacijos** skilties atskaitymų darbo srityje.

### <a name="create-a-return-order"></a>Grąžinimo užsakymo kūrimas

Galite sukurti grąžinimo užsakymo atskaitymus, kurie buvo sukurti naudojant komandą **Naujas atskaitymas** darbo srityje, kliento sudengimo arba kliento puslapyje. Tačiau turi būti įvykdytos visos šios sąlygos:

- Laukas **Paraiškos pagrindas** nustatytas kaip *Pagrįstas kiekiu*.
- **Paraiškos būsena** – šis laukelis nustatytas į *Atviras*.
- Parinktis **Kurti grąžinimo užsakymą** **Atskaitymai** skirtuke **[Gautinos sumos parametrai](#accounts-receivable-deductions)** puslapis nustatytas į *Taip*.
- Parinktis **Kurti grąžinimo užsakymą prieš atskaitymo patvirtinimą** **Atskaitymai** skirtuke **[Gautinos sumos parametrai](#accounts-receivable-deductions)** puslapis nustatytas į *Taip*.

Norėdami sukurti grąžinimo užsakymą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Pasirinkite **Pažymėti** žymės langelį, kad būtų apdorotas atskaitymas.
1. Veiksmų srityje, pasirinkite **Tvarkyti \> Sukurti grąžinimo užsakymą**.
1. Dialogo lange **Atskaitymo patvirtinimas** redaguokite arba pridėkite informaciją prie esamos **Pastabos** vertės, jei reikia ir tada pasirinkite **OK**.
1. Dialogo lange **Kopijuoti užsakymus** **Sąskaitos** FastTab, **Antraštės** skiltis rodo pardavimų sąskaitas-faktūras, kur **sąskaitos paskyros** vertė atitinka atskaitymo kliento paskyrą. Pasirinkite taikomą pardavimo sąskaitą-faktūrą.
1. **Eilučių** skyrius rodo eilutes iš pasirinktos pardavimo sąskaitos. Pažymėkite žymės langelį **Pasirinkti** kiekvienai eilutei, kurią norite kopijuoti. Arba **Antraštės** skiltyje pasirinkite **Žymėti viską** žymos langelį pardavimo užsakymui, kad pasirinktumėte visas jo eilutes.
1. Koreguoti vienos ar daugiau eilučių **Kiekio** vertę, jei reikia.

    Visos iki šiol pasirinktos eilutės yra išvardytos **Pasirinktose eilutėse arba antraštėje, kuri turi būti kopijuojama** "FastTab".

1. Pakartokite ankstesnius du reikiamus veiksmus, kol visos būtinos eilutės bus išvardytos **Pasirinktose eilutėse arba antraštėje, kurias reikia kopijuoti** "FastTab".
1. Pasirinkite **Gerai**.

    Atidaromas naujas grąžinimo užsakymas ir automatiškai nustatomi šie laukai:

    - **Atskaitymo ID** – šis laukas įtraukiamas į antraštę, kad būtų galima grąžinti atskaitymą.
    - **Grąžinimo priežasties kodas** - pagal numatytuosius nustatymus šiame lauke nustatoma **Grąžinimo priežasties kodo** vertė, kuri nustatyta pagal atskaitymo priežastį, kuri priskirta atskaitymui.

### <a name="deny-a-deduction"></a>Atskaitymo atmetimas

Norėdami atmesti atskaitymą, atlikite šiuos veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Pasirinkite **Pažymėti** žymės langelį, kad būtų apdorotas atskaitymas.
1. Veiksmų srityje pasirinkite **Tvarkyti \> Atmesti**.
1. Dialogo lange **Atmesti** pasirinkite priežasties kodą, dėl kurios buvo atmestas, tada pasirinkite **OK**.
1. **Rodyti** lauke, esančiame žemiau Veiksmų srities pasirinkite *Uždaryta*.

    **Atskaitymų** skirtukas rodo atmestus atskaitymus ir **Likusi suma** atskaitymo laukelis nustatytas į *0.00*.

    Galite sukurti grąžinimo užsakymo atskaitymus, kurie buvo sukurti naudojant komandą **Naujas atskaitymas** darbo srityje, kliento sudengimo arba kliento puslapyje, atsiranda tokie įvykiai:

    - Skirtuko **Nuorodos** laukai, esantys skyriuje **Atmetimas** yra atnaujinami.
    - Jei pasirinkote kurti paraiškos žurnalą kurdami atskaitymą ir jei prie atskaitymo, sumažinusio sąskaitos balansą, buvo pridėta sąskaita-faktūra, o anksčiau pridėtos sąskaitos-faktūros likęs balansas padidinamas atmestos prašymo sumos.
    - Atskaitymo **Būsenos** laukas nustatytas kaip *Uždarytas*.
    - Atskaitymo **Paraiškos būsena** laukas nustatytas kaip *Atmestas*.

Norėdami atmesti atskaitymą, atlikite šiuos veiksmus.

1. Skirtuke **Atskaitymai** pasirinkite atmestą atskaitymą.
1. Veiksmų srityje pasirinkite **Apsukti atmetimą**.

    Galite sukurti grąžinimo užsakymo atskaitymus, kurie buvo sukurti naudojant komandą **Naujas atskaitymas** darbo srityje, kliento sudengimo arba kliento puslapyje, atsiranda tokie įvykiai:

    - Skirtuko **Nuorodos** laukai, esantys skyriuje **Atmetimas** yra atnaujinami.
    - Atskaitymo **Būsenos** laukas nustatytas kaip *Atviras*.
    - Atskaitymo **Paraiškos būsena** laukas nustatytas kaip *Atviras*.

### <a name="write-off-a-deduction"></a>Atskaitymo nurašymas

Norėdami nurašyti atskaitymą, atlikite šiuos veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Pasirinkite **Pažymėti** žymės langelį, kad būtų apdorotas atskaitymas.
1. Veiksmų srityje pasirinkite **Tvarkyti \> Nurašyti**.
1. Dialogo lange **Nurašyti** pasirinkite nurašymo priežasties kodą, tada pasirinkite **OK**.
1. **Rodyti** lauke pasirinkite *Uždaryta*.

    **Atskaitymų** skirtukas rodo nurašytus atskaitymus ir **Likusi suma** atskaitymo laukelis nustatytas į *0.00*.

    Galite sukurti grąžinimo užsakymo atskaitymus, kurie buvo sukurti naudojant komandą **Naujas atskaitymas** darbo srityje, kliento sudengimo arba kliento puslapyje, atsiranda tokie įvykiai:

    - Skirtuko **Nuorodos** laukai, esantys skyriuje **Nurašyti** yra atnaujinami.
    - Jei kurdami atskaitymą sukūrėte žurnalą, jis užregistruojamas atskaitymo nurašymo priežasties kode. Šį įrašą galite peržiūrėti skirtuke **Atskaitymo įvykiai**, kur **Atnaujinimo tipo** vertė nuo *Nurašymo*.
    - Atskaitymo **Būsenos** laukas nustatytas kaip *Uždarytas*
    - Atskaitymo **Paraiškos būsena** laukas nustatytas kaip *Nurašytas*.

Norėdami apsukti nurašymą, atlikite šiuos veiksmus.

1. Skirtuke **Atskaitymai** pasirinkite atmestą atskaitymą.
1. veiksmų srityje, pasirinkite **Apsukti nurašymą**.

    Galite sukurti grąžinimo užsakymo atskaitymus, kurie buvo sukurti naudojant komandą **Naujas atskaitymas** darbo srityje, kliento sudengimo arba kliento puslapyje, atsiranda tokie įvykiai:

    - Skirtuko **Nuorodos** laukai, esantys skyriuje **Nurašyti** yra atnaujinami.
    - Jei kurdami atskaitymą sukūrėte žurnalą, jis užregistruojamas atskaitymo nurašymo priežasties kode. Šį įrašą galite peržiūrėti skirtuke **Atskaitymo įvykiai**, kur **Atnaujinimo tipo** vertė nuo *Apsukto nurašymo*.
    - Atskaitymo **Būsenos** laukas nustatytas kaip *Atviras*.
    - Atskaitymo **Paraiškos būsena** laukas nustatytas kaip *Atviras*.

## <a name="credits-created-outside-the-approve-deduction-process"></a><a name="credits-outside-approval"></a>Kreditai, sukurti už atskaitymo tvirtinimo proceso ribų

Šis skyrius taikomas tik atskaitymams, kurie buvo sukurti naudojant komandą **Naujas atskaitymas** darbo srityje, kliento sudengimo arba kliento puslapyje.

Skirtingi vartotojai galėjo sukurti laisvos formos sąskaitą-faktūrą, grąžinimo užsakymą arba neigiamą pardavimo užsakymą pagal kliento reikalavimus ne **Patvirtinti atskaitymą** procese. Kai esamas atskaitymas patvirtinamas atskaitymo darbo srityje, sistema automatiškai sukuria kitą laisvos formos sąskaitą, grąžinimo užsakymą arba neigiamą pardavimo užsakymą. Šiame skyriuje aprašoma, kaip pridėti esamus kreditus prie atskaitymo prieš jį patvirtinant, kad būtų išvengta kredito dublikatų.

### <a name="attach-a-credit-to-deduction"></a>Prie atskaitymo pridėkite kreditą

Šiame skyriuje aprašoma, kaip pridėti kreditą prie atskaitymo iš kredito.

Pridėjus kreditą prie atskaitymo, galite peržiūrėti kreditą, kuris sukuriamas patvirtinus atskaitymą, taip pat galite naudoti **Atviras kreditas** mygtuką įrankių juostoje, esantį **Atviros operacijos** skilties atskaitymų darbo srityje.

Pateikus kredito sąskaitą-faktūrąir patvirtinus atskaitymą, kreditas matosi **Atviros operacijos** skiltyje atskaitymų darbo srityje prieš taikomą **Atskaitymo ID** vertę ir jos **paraiškos tipas** laukelis nustatytas į *Kiti kreditai*.

#### <a name="attach-a-free-text-invoice-to-a-deduction"></a>Prie atskaitymo pridėkite laisvo teksto sąskaitą-faktūrą

Norėdami prie atskaitymo pridėti laisvo teksto sąskaitą-faktūrą, atlikite šiuos veiksmus.

1. Pasirinkite **Gautinos sumos \> Sąskaitos faktūros \> Visos laisvos formos SF**.
1. Pasirinkite taisytiną sąskaitą-faktūrą.
1. Veiksmų srities skirtuke **Sąskaitos** pasirinkite **Pridėti kreditą prie atskaitymo**. Šį mygtuką galima naudoti tik pasirinkus laisvo teksto sąskaitą **Atskaitymų ID** laukas yra tuščias. Tuščias laukas nurodo, kad laisvos formos sąskaita-faktūra dar neprijungta prie atskaitymo.
1. Puslapyje **Pridėti kreditą prie atskaitymo** galima pasirinkti *vieną* atskaitymą. Galima pasirinkti tik atvirus *kaina pagrįsta* atskaitymus.
1. Pasirinkite **Gerai**. **Atskaitymo ID** laukas nustatytas laisvos formos sąskaitos-faktūros antraštėje.

#### <a name="attach-a-return-order-to-a-deduction"></a>Grąžinimo užsakymo pridėjimas prie atskaitymo

Norėdami prie atskaitymo pridėti grąžinimo užsakymą, atlikite šiuos veiksmus.

1. Eikite į **Gautinos sumos \> Užsakymai \> Visi grąžinimo užsakymai**.
1. Pasirinkite taikomą gautų ar atidarytų grąžinamų prekių autorizavimo (RMA) numerį.
1. Veiksmų srities skirtuke **Grąžinimo užsakymas** pasirinkite **Pridėti kreditą prie atskaitymo**. Šį mygtuką galima naudoti tik jei grąžinimo užsakymo **Atskaitymų ID** laukas yra tuščias. Tuščias laukas nurodo, kad grąžinimo užsakymas dar neprijungtas prie atskaitymo.
1. Puslapyje **Pridėti kreditą prie atskaitymo** galima pasirinkti *vieną* atskaitymą. Galima pasirinkti tik atvirus *kiekiu pagrįstus* atskaitymus.
1. Pasirinkite **Gerai**. **Atskaitymo ID** laukas nustatytas grąžinimo užsakymo antraštėje.

#### <a name="attach-a-sales-order-to-a-deduction"></a>Pardavimo užsakymo pridėjimas prie atskaitymo

Norėdami prie atskaitymo pridėti pardavimo užsakymą, atlikite šiuos veiksmus.

1. Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite taikomą atvirą, pristatytą arba pardavimo užsakymą, prie kurios išrašyta sąskaita-faktūrą.
1. Veiksmų srities skirtuke **Sąskaitos** pasirinkite **Pridėti kreditą prie atskaitymo**. Šį mygtuką galima naudoti tik jei pardavimo užsakymo **Atskaitymų ID** laukas yra tuščias. Tuščias laukas nurodo, kad pardavimo užsakymas dar neprijungtas prie atskaitymo.
1. Puslapyje **Pridėti atskaitymą** galima pasirinkti *vieną* atskaitymą. Galima pasirinkti tik atvirus *kiekiu pagrįstus* atskaitymus.
1. Pasirinkite **Gerai**. **Atskaitymo ID** laukas nustatytas pardavimo užsakymo antraštėje.

#### <a name="detach-a-deduction-from-a-credit"></a>Atskirkite atskaitymą nuo kredito

Jei pridėtas neteisingas atskaitymas, galite atskirti jį nuo kredito. Tačiau turi būti įvykdytos visos šios sąlygos:

- Prie atskaitymo pridėtas kreditas.
- **Paraiškos būsena** – šis laukelis nustatytas į *Atviras*.

Norėdami atskirti atskaitymą nuo kredito, atlikite vieną iš šių veiksmų, atsižvelgdami į kredito tipą:

- **Laisvos formos sąskaita-faktūra:** **visų laisvos formos sąskaitų** puslapyje pasirinkite sąskaitą-faktūrą. Tada Veiksmų srities skirtuke **Sąskaitos** pasirinkite **Atskirti kreditą nuo atskaitymo**.
- **Grąžinimo užsakymai:** **Visi grąžinimo užsakymai** puslapyje pasirinkite užsakymą. Tada Veiksmų srities skirtuke **Grąžinimo užsakymas** pasirinkite **Atskirti kreditą nuo atskaitymo**.
- **Pardavimų užsakymai:** **Visi pardavimo užsakymai** puslapyje pasirinkite užsakymą. Tada Veiksmų srities skirtuke **Sąskaitos** pasirinkite **Atskirti kreditą nuo atskaitymo**.

### <a name="attach-a-deduction-to-a-credit"></a>Pridėkite atskaitymą prie kredito

Šiame skyriuje aprašoma, kaip pridėti atskaitymą prie kredito iš atskaitymo.

#### <a name="attach-a-deduction-to-a-free-text-return-order-or-sales-order-credit"></a>Atskaitymo pridėjimas prie laisvos formos teksto, grąžinimo užsakymo arba pardavimo užsakymo kredito

Norėdami pridėti atskaitymą prie laisvos formos teksto, grąžinimo užsakymo arba pardavimo užsakymo kredito, atlikite šiuos veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Pasirinkite taikomą atvirą atskaitymą.
1. Veiksmų srityje pasirinkite **Prižiūrėti \> Pridėti atskaitymą prie kredito**. Šis mygtukas galimas tik, jei **Paraiškos būsenos** laukas nustatytas kaip *Atidarytas*.
1. Puslapyje **Pridėti kreditą** galima pasirinkti *vieną* kreditą. Rodomo kreditų tipas priklauso nuo atskaitymo **Paraiškos pagrindo** vertės:

    - *Remiantis kaina* – puslapyje rodomos kliento laisvos formos sąskaitos-faktūros, kur **Atskaitymo ID** laukas tuščias. Klientų paraiškos taip pat rodomos, nes laisvos formos sąskaita gali būti neregistruota. Todėl ji gali turėti numerį, kurį būtų galima nurodyti.
    - *Remiantis kiekiu* - rodomų kreditų tipas priklauso nuo **Kurti grąžinimo užsakymą** parinkties nustatymų **[Gautinų sumų parametrų](#accounts-receivable-deductions)** puslapyje:

        - *Taip* – puslapyje rodomi kliento grąžinimo užsakymai, kur **Atskaitymo ID** laukas tuščias.
        - *Ne* – puslapyje rodomi kliento pardavimo užsakymai, kur **Atskaitymo ID** laukas tuščias.

1. Pasirinkite **Gerai**. **Atskaitymo ID** laukas nustatytas kredito antraštėje.

Pridėjus kreditą prie atskaitymo, galite peržiūrėti kreditą, kuris sukuriamas patvirtinus atskaitymą, taip pat galite naudoti **Atviras kreditas** mygtuką įrankių juostoje, esantį **Atviros operacijos** skilties atskaitymų darbo srityje.

Pateikus kredito sąskaitą-faktūrąir patvirtinus atskaitymą, kreditas matosi **Atviros operacijos** skiltyje atskaitymų darbo srityje prieš taikomą **Atskaitymo ID** vertę ir jos **paraiškos tipas** laukelis nustatytas į *Kiti kreditai*.

#### <a name="detach-a-credit-from-the-deduction"></a>Atskirkite kreditą nuo atskaitymo

Jei pridėtas neteisingas kreditas, galite atskirti jį nuo atskaitymo. Tada Veiksmų srities skirtuke **Tvarkyti** grupėje pasirinkite **Atskirti atskaitymą nuo kredito**. **Atskaitymo ID** vertė pašalinama iš kredito.

**Atskaitymo nuo kredito mygtukas** galimas tik jei tenkinamos šios sąlygos:

- Prie atskaitymo pridėtas kreditas.
- **Paraiškos būsena** – šis laukelis nustatytas į *Atviras*.

## <a name="create-a-one-time-promotion"></a>Kurti vienkartinę akciją

Kartais galite neturėti patvirtinto grąžinimo, kurį galima sugretinti su atskaitymu. Tokiu atveju galite naudoti funkciją *vienkartinė akcija* norėdami sugretinti atskaitymą su prekybos nuolaida, kuri susieta su klientu. Funkcija *vienkartinė akcija* sukuria naują prekybos nuolaidų sutartį ir fiksuotos sumos prekybos įvykį. Tada ji sugretina fiksuotą sumą su atskaitymu ir atlieka registracijas, kurių reikia norint uždaryti atskaitymą.

Ši funkcija naudinga, jei naudojate prekybos nuolaidas. Norėdami gauti daugiau informacijos apie prekybos nuolaidas, žr. [Prekybos akcijų valdymas](../sales-marketing/trade-allowance.md).

Pirmiausia turite nustatyti šabloną, kurį galite naudoti norint sukurti naują prekybos nuolaidų sutartį. Norėdami nustatyti šabloną atlikite nurodytus veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos akcijos \> Šablonai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Laukeliuose įveskite informaciją, kuri turėtų būti rodoma sutartyse, sukurtose naudojant šabloną.
1. **Klientai** "FastTab" **Hierarchijos** laukelyje pasirinkite hierarchijos lygį.
1. Hierarchijų sąraše pasirinkite klientą, kuriam yra nesuderintas atskaitymas, tada pasirinkite rodyklės dešinėn mygtuką (**\>**). Klientas yra įtrauktas į **Prekybos nuolaidas sutarčių klientų** sąrašą.
1. Nustatykite likusius laukus taip, kaip jums reikia, ir uždarykite puslapį.
1. Eikite į **Pardavimas ir rinkodarą \> Sąranka \> Prekybos akcijos \> Prekybos akcijų valdymo parametrai**.
1. Skirtuke **Peržiūra** **Vienkartinės akcijos šablonas** laukelyje pasirinkite šablono, kurį naudosite sukurti vienkartines akcijas, pavadinimą.

Be to, atskaitymo darbo srityje galite sukurti vienkartinę akciją. Norėdami sukurti vienkartinį pasiūlymą, atlikite šiuos veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Pasirinkite **Pažymėti** žymės langelį šalia atskaitymo apdorojimui.
1. Veiksmų srityje pasirinkite **Tvarkyti \>, kad sutvarkytumėte atskaitymą kaip vienkartinį pasiūlymą**.
1. **Vienkartinės akcijos** dialogo lange atlikite šiuos veiksmus, norėdami atskaitymą susieti su vienu ar daugiau lėšų:

    1. pasirinkite **Naujas**, ir tada **Lėšų ID** laukelyje pasirinkite lėšų ID. Pakartokite šį veiksmą norėdami įtraukti tiek fondų, kiek reikia.
    1. **Procentai** laukelyje prie kiekvieno fondo ID įveskite atskaitymo procentą, paskirstytiną fondui. Sumos, kurias įvedate į **Procentai** laukus turi sudaryti 100 procentų.

1. Pasirinkite **Gerai**. Sistema sukuria naują prekybos nuolaidų sutartį, kurioje yra fiksuotos sumos prekybos įvykis, ir sugretina fiksuotą sumą su atskaitymu.

## <a name="do-a-mass-update-of-deductions"></a>Atlikite masinį atskaitymų naujinimą

Jei turite atlikti tokį patį keleto atskaitymų pakeitimą, galite pasirinkti tuos atskaitymus ir masiškai atnaujinti jų laukus.

Norėdami masiškai atnaujinti, atlikite nurodytus veiksmus.

1. Eikite į **Pardavimai ir rinkodara \> Prekybos nuolaidos \> Atskaitymai \> Atskaitymų darbo sritis**.
1. Laukelyje **Rodyti**, esančiu žemiau Veiksmų srities pasirinkite norimų peržiūrėti atskaitymų tipą.
1. Norėdami atnaujinti, prie kiekvieno atskaitymo pažymėkite žymės langelį . Tada Veiksmų srityje pasirinkite **Prižiūrėti \> Masinis atnaujinimas**.
1. **Masinio naujinimo** dialogo lange rodomi pasirinkti atskaitymai. Atnaujinkite laukus taip, kaip jums reikia, tada pasirinkite **OK** kad patvirtintumėte keitimus.

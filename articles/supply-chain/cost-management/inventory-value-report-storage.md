---
title: Atsargų vertės ataskaitos
description: Šioje temoje paaiškinama, kaip nustatyti, generuoti ir naudoti atsargų vertės ataskaitas. Šiose ataskaitose pateikiama informacija apie jūsų atsargų faktinius ir finansinius kiekius ir sumas.
author: banluo-ms
ms.date: 10/19/2021
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: banluo
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 7978c7b326ef1b62f76711ac187c28539eb1f449
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798326"
---
# <a name="inventory-value-reports"></a>Atsargų vertės ataskaitos

[!include [banner](../includes/banner.md)]

Atsargų vertės ataskaitose pateikiama informacija apie faktines ir finansines jūsų atsargų kiekius ir sumas. Ataskaitas galite peržiūrėti įvairiais būdais. Pavyzdžiui, galite rodyti sumas, operacijas arba filtruoti pagal prekes ar laiko intervalą. Galite peržiūrėti parduotų prekių savikainos (PPS) vertes ar nebaigtos gamybos (NG) vertes ir nustatyti kitas pasirinktis.

Atsargų vertės ataskaitos leidžia atlikti šias užduotis:

- Atlikite DK ir atsargų suderinimą.
- Pasikonsultuokite su turimos atsargos ir konkretaus laikotarpio vertėmis.
- Kurti ataskaitų konfigūracijas, kurios pritaikomos konkrečiai paskirtis.
- Įrašykite ataskaitos konfigūracijas, kad jas būtų galima naudoti kelis kartus.
- Pridėkite diapazonus, pagal kuriuos filtruoti duomenis, kai vykdote ataskaitą.

## <a name="types-of-inventory-value-report"></a>Atsargų vertės ataskaitos tipai

Yra du atsargų vertės ataskaitos tipai: **atsargų vertės** (standartinės ataskaitos) ir **atsargų vertės ataskaitos saugojimas**.

### <a name="standard-inventory-value-report"></a>Standartinės atsargų vertės ataskaita

Standartinė atsargų vertės ataskaita yra paprasta ataskaita, leidžianti pasirinkti įtrauktą informaciją ir tada **·** rodo, kad informacija ekrane. Jis neįrašo rezultatų. Taip pat nėra interaktyvių filtravimo, naršymo ar eksportavimo funkcijų. Dėl šių priežasčių rekomenduojame daugeliu atvejų naudoti atsargų vertės ataskaitos **·** saugojimo ataskaitą.

### <a name="inventory-value-report-storage-report"></a>Atsargų vertės ataskaitos saugojimo ataskaita

Atsargų vertės ataskaitos saugojimo ataskaita pateikia išeigą kaip interaktyvią "Microsoft" puslapį arba kaip eksportuotą **dokumentą vienu iš kelių** Dynamics 365 Supply Chain Management formatų.

Kai ataskaitą peržiūrite naršyklėje, stulpeliai ir kaupiamieji balansai yra dinamiškai koreguojami atsižvelgiant į jūsų sukonfigūruotą maketą. Galite surikiuoti rezultatus, filtruoti juos, detalizuoti duomenis ir daugiau.

Ataskaitų rezultatai saugomi duomenų objekte **Atsargų vertė**. Todėl rezultatus galite filtruoti ir eksportuoti formatu, pvz., kableliais atskirtų reikšmių (CSV) arba „Microsoft Excel” formatu.

Atsargų **vertės ataskaitos saugojimo ataskaita yra** naudinga, kai išeigai yra daug eilučių. Pavyzdžiui, jūs turite 50 000 prekių ir 300 parduotuvių, sukurtų kaip sandėliai. Tokiu atveju, pateikus atsargų pabaigos balansų užklausą pagal prekę, svetainę ir sandėlį, išvestyje bus daug eilučių.

> [!NOTE]
> Atsargų **vertės ataskaitos saugojimo** ataskaitoje nėra tarpinių sumų, kurios nustatytos ataskaitos makete. Taip pat nėra DK balansų, net jei šie balansai apibrėžiami ataskaitos makete. Derinimas su DK turi būti atliekamas naudojant bandomuosius balansus. Tačiau standartinėje **atsargų vertės** ataskaitoje yra šių tarpinių sumų ir balansų.

## <a name="turn-on-the-inventory-value-report-storage-feature"></a>Įjungti atsargų vertės ataskaitos saugojimo funkciją

Standartinė atsargų **vertės ataskaita yra įgalinta pagal** numatytuosius nustatymus. Tačiau jei norite generuoti išplėstinę atsargų vertės ataskaitos saugojimo **·** ataskaitą, turite įjungti funkciją savo sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Išlaidų valdymas*
- **Priemonės pavadinimas:** *atsargų vertės ataskaitos saugojimas*

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a> Nustatyti atsargų vertės ataskaitų konfigūracijas

Norėdami nustatyti **turinį, kuris įtrauktas į įvairių tipų atsargų vertės ataskaitą, naudokite** atsargų vertės ataskaitų puslapį. Galite nurodyti bet kokį ataskaitų tipų skaičių. Kiekvieną kartą, kai generuojate bet kurį atsargų vertės ataskaitos tipą, pasirinkite ataskaitos tipą.

1. Eikite **į Išlaidų valdymo atsargų apskaitos strategijų nustatymą Atsargų vertės \>\>** ataskaitos.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami redaguoti esamą ataskaitą, pasirinkite ją sąrašo srityje, tada veiksmų **·** srityje pasirinkite Redaguoti.
    - Norėdami sukurti naują ataskaitą, **veiksmų** srityje pasirinkite Naujas.

1. Naujos ar pasirinktos ataskaitos antraštėje nustatykite šiuos laukus:

    - **ID** – įveskite trumpą ataskaitos identifikatorių. Ši vertė turi būti unikali tarp visų atsargų vertės ataskaitų konfigūracijų. Įrašę naują konfigūraciją jos redaguoti negalima.
    - **Pavadinimas** – įveskite ataskaitos aprašomąjį pavadinimą.

1. Jei kuriate naują ataskaitos konfigūraciją, veiksmų srityje pasirinkite Įrašyti, kad **·** likusį lauką būtų galima naudoti.
1. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.

    - **Datos intervalas** – pasirinkite iš anksto nustatytą datos intervalą. Galite nepaisyti šio datos intervalo, kai vykdote ataskaitą.
    - **Diapazonas – pasirinkite registravimo datą arba operacijos laiką, atsižvelgdami į datą ir laiką, kuris turėtų būti naudojamas nuskaitant** *ataskaitos* *·* įrašus.
    - **Dimensijų** rinkinys – pasirinkite dimensijų rinkinį, į kuriuos reikia vykdyti duomenis. (Dimensijos nustatomos DK.) Pvz., galite paleisti pagrindinės *sąskaitos arba pagrindinės sąskaitos + verslo* *vieneto* duomenis. Jūsų pasirinkti dimensijų rinkinys turi turėti ne daugiau kaip dvi dimensijas. Daugiau informacijos ieškokite finansinių [dimensijų](../../finance/general-ledger/financial-dimension-sets.md) rinkiniuose.

1. Stulpelių **·** "FastTab" nustatykite šiuos laukus. Šie laukai valdo stulpelius, į kuriuos įtraukia jūsų ataskaita, ir duomenų tipus, kurie yra šiuose stulpeliuose.

    - **Atsargos –** nustatykite šią pasirinktį *kaip* Taip, jei norite rodyti atsargų vertes. Tada galite suderinti šias vertes su DK sąskaitos balansais.
    - **NG** – nustatykite šią *pasirinktį kaip Taip,* norėdami rodyti NG vertes. Tada šias vertes galima suderinti su NG sąskaitų balansais DK. Kai nustatote šią pasirinktį kaip Taip, ataskaitoje bus rodomi tik faktiniai atsargų, *·* kurių būsena NG, kiekiai ir sumos. Gamybos užsakymai, kurių NG būsena yra paimti arba pranešti kaip baigti, bet nebuvo baigti.
    - **Atidėta PPK – nustatykite šią pasirinktį kaip Taip, kad būtų rodomas stulpelis, kuriame rodomi atidėtos PPK** *·* faktiniai kiekiai ir atsargų sumos. Atidėta PPK rodoma naudojant faktinius kiekius ir sumas, nes ji koresponduojant važtaraščių kiekius ir sumas.
    - **PPK** – nustatykite šią *pasirinktį kaip Taip, kad būtų rodomas* stulpelis, kuriame rodomi PPS finansiniai kiekiai ir sumos. PPK rodoma naudojant finansinius kiekius ir sumas, nes ji kompensuoja SF kiekius ir sumas.
    - **Pelnas ir nuostolis – nustatykite šią pasirinktį kaip Taip, kad būtų rodomas stulpelis, kuriame rodoma finansinė suma, užregistruota atsargų pelno ir** *·* nuostolio sąskaitose.
    - **Spausdinti kaupiamąsias sąskaitų vertes palyginti** – nustatykite šią pasirinktį kaip Taip, jei *·* norite, kad būtų rodomas stulpelis, kuriame rodomas DK sąskaitos balansas. Tokiu būdu neturėsite tikrinti sekimo balanso. Ši pasirinktis veikia tik su **standartine atsargų vertės** ataskaita, o ne **su atsargų vertės ataskaitos saugojimo** ataskaita. Kai nustatote šią pasirinktį taip, turite naudoti šiuos laukus, norėdami nurodyti kiekvieną norimą pateikti DK sąskaitą, atsižvelgdami į įgalintas finansinės *·* padėties **·** pasirinktis.

        > [!NOTE]
        > Jei pasirinksite bendrą sąskaitą bet kuriam iš šių laukų, bus rodoma ir kiekvienos atsargų sąskaitos suma, kuri įtraukta į bendrą sąskaitą, ir *·* bendrosios sąskaitos suma.

        - **Atsargų sąskaita** – nurodykite DK sąskaitą, kurios atsargų informacija bus rodoma. (Abu **Atsargų** parinktis ir **parinktis Spausdinti kaupiamąsias sąskaitos** vertes, kad būtų galima palyginti, turi būti *nustatyta kaip Taip* .)
        - **NG** sąskaita – nurodykite DK sąskaitą, kurios NG informacija bus rodoma. (Abu **NG** parinktis ir **parinktis Spausdinti kaupiamąsias sąskaitos** vertes, kad būtų galima palyginti, turi būti *nustatyta kaip Taip* .)
        - **Atidėtos PPK** sąskaita – nurodykite DK sąskaitą, kurioje bus rodoma atidėtos PPK informacija. (Abu **Atidėtos PPK** parinktis ir palyginimo parinkties Spausdinti kaupiamąsias sąskaitos vertes **turi būti nustatyta kaip** Taip *·* .)
        - **PPK sąskaita** – nurodykite DK sąskaitą, kurios PPK informacija būtų rodoma. (Abu **PPK** parinktis ir **parinktis Spausdinti kaupiamąsias sąskaitos** vertes, skirtas palyginimui, turi būti nustatyta *kaip Taip* .)

    - **Apibendrinti faktines ir finansines vertes – nustatykite šią pasirinktį kaip Taip, jei norite, kad būtų rodomas stulpelis, kuriame rodomas bendras atsargų kiekis ir atsargų suma (faktinių ir finansinių atsargų** *·* verčių suvestinė). Jei ši pasirinktis nustatyta kaip *·* Ne, ataskaitoje bus parodytos ir faktinių, ir finansinių atsargų vertės.
    - **Įtraukti neužregistruotas DK. Nustatykite šią pasirinktį kaip Taip, jei norite matyti stulpelį, kuriame rodomos** *·* operacijos, kurios niekada nebuvo užregistruotos DK. Šių prekių tipų operacijos gali būti neregistrinės DK:

        - Gautos prekės, kurioms dar neišrašyta SF, kai atitinkamos prekių modelių grupės pasirinktis **·** Registruoti faktines atsargas yra išvalyta.
        - Gautos prekės, kurioms dar neišrašyta SF, kai parinktis Registruoti produkto gavimo kvitą DK išvaloma gavimo dokumento **"FastTab", kuris yra mokėtinų sumų parametrų puslapio skirtuke Bendra** **·** **·** **·** **(mokėtinų \>\>** sumų nustatymo mokėtinų sumų parametrai).

    - **Skaičiuoti vidutinę vieneto** savikainą – nustatyti šią pasirinktį *kaip Taip,* kad būtų rodomas stulpelis, kuriame rodomos vidutinės vieneto išlaidos. Vidutinė vieneto savikaina yra bendras kiekis, padalintas iš bendrosios sumos.
    - **Bendras kiekis ir vertė – nustatykite šią pasirinktį kaip Taip, norėdami rodyti stulpelius, kuriuose rodomas bendras faktinių atsargų kiekis (ir finansiniai kiekiai) ir bendra faktinių** *atsargų suma* (ir finansinės sumos). Šią pasirinktį galite nustatyti tik *·* tada, jei **pasirinktis Apibendrinti faktines ir finansines** vertes nustatyta kaip *·* Ne.
    - **Atsargų dimensijos – šiame tinklelyje pažymėkite kiekvienos dimensijos, kurią norite rodyti ataskaitoje,** **žymės langelį** Rodyti. Tik dimensijos, kuriose **įgalinta finansinių** atsargų parinktis, ataskaitoje bus parodytos vertės. Kitos dimensijos rodys tik tuščius stulpelius. Šioms dimensijoms, kurias pasirenkate rodyti, galite pažymėti žymės langelį Bendroji suma, **kad būtų įtrauktos ir** sumos.
    - **Išteklių ID** – nustatyti parinktį Peržiūrėti kaip **·** *Taip, kad būtų rodomas* stulpelis, identifikuojantis kiekvienos eilutės prekę. Norėdami įtraukti **ir** *sumas,* nustatykite pasirinktį Bendra. Atsižvelgiant į prekės tipą, nurodytą kiekvienoje eilutėje, stulpelyje rodomas vienas iš šių informacijos tipų:

        - **Medžiaga** – stulpelyje `ItemID` rodoma atitinkamo medžiagos įrašo lauko vertė.
        - **Darbas** – stulpelyje `WorkCenterID` rodoma atitinkamo darbo įrašo lauko vertė.
        - **Netiesioginės** išlaidos – stulpelyje rodoma atitinkamo išlaidų įrašo `CodeID` lauko vertė.

        Jei lauke Išteklių ID ir Išteklių grupė nustatyta parinktis Rodinys, matysite tik bendrą atsargų vertę, pagrįstą pasirinktomis atsargų **·** *·* **·** **·** dimensijomis.

    - **Išteklių grupė** – nustatyti parinktį Peržiūrėti kaip **·** *Taip, kad būtų rodomas* stulpelis, identifikuojantis kiekvienos eilutės išteklių grupę. Norėdami įtraukti **ir** *sumas,* nustatykite pasirinktį Bendra. Atsižvelgiant į prekės tipą, nurodytą kiekvienoje eilutėje, stulpelyje rodomas vienas iš šių informacijos tipų:

        - **Medžiaga** – stulpelyje `ItemGroup` rodoma atitinkamo medžiagos įrašo lauko vertė.
        - **Darbas** – stulpelyje `WorkcenterGroup` rodoma atitinkamo darbo įrašo lauko vertė.
        - **Netiesioginės** išlaidos – stulpelyje rodoma atitinkamo išlaidų įrašo `CostGroup` lauko vertė. (Vertė `CostGroupType` turi būti netiesioginė *·* .)

        Jei lauke Išteklių ID ir Išteklių grupė nustatyta parinktis Rodinys, matysite tik bendrą atsargų vertę, pagrįstą pasirinktomis atsargų **·** *·* **·** **·** dimensijomis.

1. Eilučių **·** "FastTab" nustatykite šiuos laukus. Šie laukai leidžia į ataskaitą įtraukti atitinkamus su NG susijusius poskyrius arba juos pašalinti.

    - **Medžiagos** – nustatykite šią pasirinktį *kaip Taip, jei* norite, kad būtų rodoma informacija apie medžiagas. *Medžiaga* yra numatytasis išteklių tipas, kadangi medžiagos turi būti įtrauktos į visas ataskaitų konfigūracijas, kad būtų sukurta patikimas išeiga.
    - **Darbas** – nustatykite šią *pasirinktį kaip Taip,* kad būtų parodytos NG darbo išlaidos.
    - **Netiesioginės** išlaidos – nustatykite šią *pasirinktį kaip Taip,* kad būtų parodytos netiesioginės NG išlaidos.
    - **Tiesioginės užsakomųjų paslaugų paslaugos** – nustatykite šią pasirinktį kaip *Taip,* norėdami parodyti tiesiogines užsakomųjų paslaugų NG išlaidas. Ši informacija naudinga subrangai.
    - **Detalumo** lygis – pasirinkite ataskaitos peržiūros pasirinktį:

        - *Operacijos* – peržiūrėti visas susijusias operacijas ataskaitoje. Atkreipkite dėmesį, kad gali kilti našumo problemų, kai galėsite peržiūrėti ataskaitas, kuriose įtraukta daug operacijų. Todėl, jei norite naudoti šią rodinio pasirinktį, rekomenduojame naudoti atsargų **vertės ataskaitos saugojimo** ataskaitą.
        - *Bendrosios sumos* – peržiūrėti bendrą rezultatą.

    - **Įtraukti pradžios balansą** – nustatykite šią pasirinktį *kaip Taip, kad būtų rodomas pradžios* balansas. Ši pasirinktis galima tik **tada, kai** nustatytas laukas Detalumo lygis kaip *·* Operacijos.

## <a name="generate-an-inventory-value-report-storage-report"></a>Generuoti atsargų vertės ataskaitos saugojimo ataskaitą

Norėdami sugeneruoti ir saugoti atsargų vertės **ataskaitos saugojimo ataskaitą, atlikite šiuos** veiksmus.

1. Eikite į **Išlaidų valdymas \> Užklausos ir ataskaitos \> Atsargų vertės ataskaitų saugykla**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lango **Atsargų** vertė skirtuke Parametrai **·** nustatykite šiuos laukus:

    - **Pavadinimas** – įveskite unikalų ataskaitos pavadinimą.
    - **ID** – pasirinkite atsargų vertės ataskaitos [konfigūraciją, kuri bus naudojama](#report-configuration) ataskaitoje. Konfigūravimas nustato stulpelių ir eilučių, kurios bus įtrauktos į jūsų ataskaitą, pasirinktis.
    - **Datų** intervalas – naudokite šio skyriaus laukus, norėdami nurodyti, kurie įrašai įtraukiami į ataskaitą. Norėdami nustatyti datos intervalą, lauke **Datos intervalo kodas** pasirinkite iš anksto nustatytą intervalą (susijusį su ataskaitos generavimo data) arba laukuose **Nuo datos** ir **Iki datos** įveskite konkrečias datas.

1. **Įrašuose, į kuriuos įtraukiama** "FastTab", nustatykite filtrus ir apribojimus, kad nurodykite, kurie duomenys įtraukiami į ataskaitą. Pasirinkite **Filtras,** norėdami atidaryti standartinį užklausų doroklio dialogo langą, kuriame galite nurodyti pasirinkimo kriterijus, rūšiavimo kriterijus ir jungtis. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ fono užduočių tipams. Visi šie filtrai bus taikomi atsargų operacijoms, bet ne DK balansui. Nustatę filtrus turėkite omenyje šį elgseną. Kitu atveju galite matyti atsargų ir DK neatitikimą.
1. „FastTab” **Vykdyti fone** nurodykite, kaip, kada ir kokiu dažnumu ataskaita generuojama. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ [fono](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams.

    > [!NOTE]
    > Ši ataskaita visada vykdoma kaip paketinės užduoties dalis.

1. Norėdami pritaikyti nustatymus ir uždaryti dialogo langą, pasirinkite **Gerai**.

Po to, kai paketinė užduotis baigiama, ataskaita bus įtraukta į puslapį **Atsargų vertės ataskaitų saugykla**. Gali reikėti atnaujinti puslapį, kad pamatytumėte ataskaitą.

> [!IMPORTANT]
> Pasirinktoje atsargų vertės ataskaitos konfigūracijoje galite gauti neteisingą pradžios balansą, jei lauke Nuo datos ir Iki datos pasirenkate tą pačią datą, ir jei taip pat nustatote pasirinktį Įtraukti pradžios balansą **·** kaip **·** **·** *·* Taip.

## <a name="explore-an-inventory-value-report-storage-report"></a>Atsargų vertės ataskaitos saugojimo ataskaitos ištyrinėja

Sukūrę ataskaitą galite ją peržiūrėti ir naršyti bet kuriuo metu atlikdami tolesnius veiksmus.

1. Eikite į **Išlaidų valdymas \> Užklausos ir ataskaitos \> Atsargų vertės ataskaitų saugykla**.
1. Sąraše pasirinkite ataskaitą. Puslapyje rodoma išsami informacija apie [atsargų vertės ataskaitos](#report-configuration) konfigūraciją, kuri buvo naudojama generuojant pasirinktą ataskaitą.
1. Veiksmų srityje pasirinkite Peržiūrėti informaciją, **kad būtų rodomas ataskaitos** turinys.
1. Susipažinkite su ataskaita atlikdami bet kurį iš tolesnių veiksmų.

    - Galite pasirinkti beveik bet kurio stulpelio antraštę, kad galėtumėte rūšiuoti arba filtruoti tinklelį pagal stulpelio reikšmes, kaip tai darote su dauguma standartinių „Supply Chain Management“ puslapių.
    - Norėdami filtruoti ataskaitą pagal bet kurią kelių galimų stulpelių reikšmę, naudokite lauką **Filtruoti**.
    - Naudokite rodymo meniu (virš lauko **Filtruoti**), kad įrašytumėte ir įkeltumėte mėgstamiausius rūšiavimo ir filtravimo parinkčių derinius.

## <a name="export-an-inventory-value-report-storage-report"></a>Eksportuoti atsargų vertės ataskaitos saugojimo ataskaitą

Kiekviena sugeneruota ataskaita saugoma duomenų objekte **Atsargų vertė**. Norėdami eksportuoti duomenis iš šio objekto bet kokiu palaikomu duomenų formatu, pvz., CSV arba „Excel“ formatu, galite naudoti standartines „Supply Chain Management“ duomenų tvarkymo funkcijas.

Toliau pateikiamas pavyzdys rodo, kaip eksportuoti **atsargų vertės ataskaitos saugojimo** ataskaitą.

1. Eikite į **Sistemos administravimas \> Darbo sritys \> Duomenų valdymas**.
1. Skyriuje **Importavimas / eksportavimas** pasirinkite plytelę **Eksportavimas**.
1. Pasirodžiusiame puslapyje **Eksportavimas** nustatysite eksportavimo užduotį. Pirmiausia įveskite užduoties grupės pavadinimą.
1. Skyriuje **Pasirinkti objektai** pasirinkite **Įtraukti objektą**.
1. Pasirodžiusiame dialogo lange nustatykite tolesnius laukus.

    - **Objekto pavadinimas** – pasirinkite *Atsargų vertė*.
    - **Paskirties duomenų formatas** – pasirinkite formatą, kuriuo bus eksportuojami duomenys.

1. Norėdami pridėti naują eilutę pasirinkite **Įtraukti**, tada pasirinkite **Uždaryti**, kad uždarytumėte dialogo langą.
1. Paprastai vienu metu eksportuojate vieną ataskaitą. Norėdami eksportuoti vieną ataskaitą, nustatykite eilutės, kurią ką tik įtraukėte į dialogo langą **Užklausa**, filtrą. Tokiu būdu galite nurodyti, kuri objekto **Atsargų vertė** ataskaita yra įtraukiama į eksportavimą. Atlikite tolesnius veiksmus, norėdami nustatyti šias filtro pasirinktis vienai ataskaitai eksportuoti.

    1. Skirtuke **Diapazonas** pasirinkite **Įtraukti**, kad įtrauktumėte eilutę.
    2. Nustatykite lauką **Lentelė** į *Atsargų vertė*.
    3. Nustatykite lauką **Išvestinė lentelė** į *Atsargų vertė*.
    4. Nustatykite lauko **Laukas** reikšmę kaip lauką, pagal kurį norite filtruoti. Paprastai naudosite lauką **Vykdymo pavadinimas** ir / arba lauką **Vykdymo laikas**.
    5. Lauką **Kriterijai** nustatykite į reikšmę, kurios norite ieškoti pasirinktame lauke. (Jei ankstesniame veiksme pasirinkote lauką **Vykdymo pavadinimas**, ši reikšmė bus ataskaitos pavadinimas. Jei pasirinkote lauką **Vykdymo laikas**, reikšmė bus laikas, kada buvo sugeneruota ataskaita.)
    6. Jei reikia, įtraukite daugiau eilučių į lentelę **Diapazonas**, kol gausite tiksliai tokią unikalią ataskaitą, kokios reikėjo.

1. Norėdami įrašyti parametrus ir uždaryti dialogo langą, pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti**, kad įrašytumėte eksporto sąranką.
1. Skirtuke **Eksportavimo parinktys** pasirinkite **Eksportuoti dabar**, kad būtų sugeneruotas eksportavimo failas.
1. Pasirodžiusiame puslapyje **Vykdymo suvestinė**, galite peržiūrėti eksportavimo užduoties būseną ir eksportuotų objektų sąrašą. Skyriaus **Objekto apdorojimo būsena** sąraše pasirinkite objektą **Atsargų vertė**, tada pasirinkite **Atsisiųsti failą**, kad atsisiųstumėte iš to objekto eksportuotus duomenis.

Norėdami gauti daugiau informacijos apie tai, kaip naudoti duomenų valdymo funkciją duomenims eksportuoti, žr. [Duomenų importavimo ir eksportavimo užduočių apžvalga](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

## <a name="generate-a-standard-inventory-value-report"></a>Generuoti standartinę atsargų vertės ataskaitą

Naudokite šią procedūrą norėdami sugeneruoti **standartinę atsargų vertės** ataskaitą.

1. Eikite **į Išlaidų valdymo \> užklausas ir ataskaitas Atsargų apskaita – būsenos \> ataskaitos atsargų \>** vertė.
1. Atsargų **vertės ataskaitos dialogo** lango **FastTab Parametrai** nustatykite šiuos laukus:

    - **Pavadinimas** – įveskite unikalų ataskaitos pavadinimą.
    - **ID** – pasirinkite atsargų vertės ataskaitos [konfigūraciją, kuri bus naudojama](#report-configuration) ataskaitoje. Konfigūravimas nustato stulpelių ir eilučių, kurios bus įtrauktos į jūsų ataskaitą, pasirinktis.
    - **Datų** intervalas – naudokite šio skyriaus laukus, norėdami nurodyti, kurie įrašai įtraukiami į ataskaitą. Norėdami nustatyti datos intervalą, lauke **Datos intervalo kodas** pasirinkite iš anksto nustatytą intervalą (susijusį su ataskaitos generavimo data) arba laukuose **Nuo datos** ir **Iki datos** įveskite konkrečias datas.

1. **Įrašuose, į kuriuos įtraukiama** "FastTab", nustatykite filtrus ir apribojimus, kad nurodykite, kurie duomenys įtraukiami į ataskaitą. Pasirinkite **Filtras,** norėdami atidaryti standartinį užklausų doroklio dialogo langą, kuriame galite nurodyti pasirinkimo kriterijus, rūšiavimo kriterijus ir jungtis. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ fono užduočių tipams.
1. „FastTab” **Vykdyti fone** nurodykite, kaip, kada ir kokiu dažnumu ataskaita generuojama. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ [fono](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams.
1. Norėdami pritaikyti nustatymus ir uždaryti dialogo langą, pasirinkite **Gerai**. Rodoma ataskaita.

## <a name="reading-inventory-value-reports"></a>Inventorizacijos aprašomos ataskaitos

Šiame skyriuje pateikiama keletas patarimų, kaip skaityti ir suprasti atsargų vertės ataskaitą.

Tiekimo grandinės valdymas palaiko šias dvi svarbias sąvokas, susijusias su atsargų būsena:

- **Finansiškai atnaujinta** – ši sąvoka nurodo, kad atsargų operacijoms JAU išrašyta SF. Gamybos užsakymuose nurodoma gamybos užsakymo pabaiga.
- **Faktiškai atnaujinta – ši sąvoka nurodo, kad atsargų operacijoms dar nebuvo išrašytos** SF, bet jos gautos arba išsiųstos. Gamybos užsakymuose nurodoma, kad medžiagos yra išrinktos arba paskelbta, kad gamybos užsakymas baigtas.

Suprantant šias dvi sąvokas, reikėtų nesudėtingai suprasti šiuos stulpelius ataskaitos išeigos metu:

- **Atsargos: finansinis kiekis** – finansiškai atnaujintas kiekis.
- **Atsargos: finansinė** suma – finansiškai atnaujintų atsargų sumos vertė.
- **Atsargos: faktinis užregistruotas** kiekis – faktinis atnaujintas kiekis.
- **Atsargos: faktinė užregistruota** suma – atsargų, kurios buvo faktiškai atnaujintos, sumos vertė.
- **Atsargos: faktinis neregistruotas kiekis – kiekis, kuris turi atsargų operacijų,** bet nebuvo užregistruotas DK. Pavyzdžiui, turite prekių modelių grupę, kurios faktinių atsargų registravimo ir finansinių atsargų registravimo pasirinktys yra išvalytos ir jūs turite su ta grupe **·** susietą **·** prekę. Tada sukuriate pirkimo užsakymą, gaunate jį ir išrašote SF. Tuomet, peržiūrėjus prekės atsargų vertės ataskaitą, pamatysite, kad pirkimo užsakyme nurodytas kiekis ir vertė rodomi atsargose: faktinis užregistruotas kiekis ir atsargos: faktinė suma užregistruota **·** **·** stulpeliuose.
- **Atsargos: faktinė neužregistruota** suma – galite nustatyti savo ataskaitas, kad jose būtų rodomos neužregistruotos sumos. Tačiau jei naudojate atsargų suderinimo ataskaitą, šios vertės naudoti nereikia. Kitu atveju suma nebus registruojama DK.
- **Atsargos: kiekis** – bendras visų ataskaitoje esančių kiekio stulpelių kiekis.
- **Atsargos: suma** – bendras visų ataskaitos sumos stulpelių kiekis. Suderinę atsargas, nenaudokite šio stulpelio, jei ataskaitoje yra stulpelis **Atsargos: faktinė neužregistruota** suma. Tokiu atveju turite pašalinti atsargų: **faktinės neregistruotos sumos** iš bendrosios sumos.
- **Vidutinė vieneto** savikaina – bendroji suma, padalinta iš bendrojo kiekio.

Paprastai, jūs naudojate atsargų vertės ataskaitą atsargų vertei ir kiekiui peržiūrėti. Tačiau kartais ataskaitoje nebus parodytos visos atitinkamos atsargų dimensijos. Jei nematote dimensijų, kurių tikitės, patikrinkite šiuos parametrus:

- Peržiūrėkite prekių saugojimo ir sekimo dimensijų grupes. Ataskaitoje gali būti **rodomos tik** tos dimensijos, kuriose įgalinta finansinių atsargų pasirinktis.
- Eikite į Išlaidų valdymo atsargų apskaitos strategijų nustatymą Atsargų vertės ataskaitos, pasirinkite ataskaitos konfigūraciją, kurią naudojote ataskaitai generuoti, ir įsitikinkite, kad stulpelyje Peržiūra pasirinktos reikiamos **\> atsargų \>** **·** dimensijos.

Pavyzdžiui, turite prekę, kurios prekės numeris yra *A0001.* Saugojimo dimensijų grupėje finansinių atsargų svetainė yra įgalinta. Vieta ir sandėlis įgalinami faktinėms atsargomis. Sekimo dimensijų grupėje įgalintas faktinių atsargų, o ne finansinių atsargų paketo numeris. Tada naudojate ataskaitos konfigūraciją, kurioje pasirinkta vieta, sandėlis ir paketo numeris. Kai matote ataskaitą, matote tik svetainės vertę. Sandėlio ir paketo numerio stulpeliai tušti. Kaip parodyta šiame pavyzdyje, atsargų vertės ataskaitose gali būti rodomos tik finansinėse atsargose įgalintos atsargų dimensijos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

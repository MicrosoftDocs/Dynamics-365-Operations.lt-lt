---
title: Sandėlio operacijų produktų filtrų konfigūravimas
description: Šioje temoje apžvelgiama, kaip konfigūruoti produktų filtrus ir filtrų kodus, norint sandėlyje suskirstyti atsargų prekes. Taip pat galite naudoti filtrus, norėdami nustatyti klientus, galinčius užsisakyti konkrečią prekę, bei kurias prekes galima įsigyti iš konkretaus tiekėjo.
author: Mirzaab
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: c3648a2d9df300ecd0c26a12db8093babb3db48f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838255"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a>Sandėlio operacijų produktų filtrų konfigūravimas

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiama, kaip konfigūruoti produktų filtrus ir filtrų kodus, norint sandėlyje suskirstyti atsargų prekes. Taip pat galite naudoti filtrus, norėdami nustatyti klientus, galinčius užsisakyti konkrečią prekę, bei kurias prekes galima nusipirkti iš konkretaus tiekėjo.

Be to, galite nustatyti ir naudoti produktų filtrus, kad sandėlyje būtų automatiškai tvarkomos atsargų prekės, o filtruotos prekės būtų sujungtos į filtrų grupes. Filtrus galima naudoti prekių suskirstymui į kategorijas, skirtas tvarkymo, pirkimo ir pardavimo procesams. Galbūt norėsite sugrupuoti prekes arba atskirti jas viena nuo kitos, kai jų apdorojimo būdas yra pagrįstas svorio arba tvarkymo apribojimais. Taip pat, galite nurodyti, iš kurių klientų ar tiekėjų prekę galima pirkti arba parduoti.

## <a name="prerequisites"></a>Būtinieji komponentai

Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.

| Būtinoji sąlyga | Instrukcijos |
|---|---|
| Prieš pradėdami konfigūruoti produktus **Išleisto produkto informacijos** puslapyje, turite įjungti sandėlio apdorojimą produkto saugojimo dimensijos grupei. | Eikite į **Produkto informacijos valdymas \> Sąranka \> Dimensija ir variantų grupės \> Saugojimo dimensijos grupės** ir pasirinkite arba sukurkite saugojimo dimensijos grupę, kur parinktis **Naudoti sandėlio valdymo procesus** nustatyta į *Taip*. |
| Jei naudosite kliento filtrus ir (arba) tiekėjo filtrus, turite įgalinti jų naudojimą Sandėlio valdymo parametruose. | Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**. Skirtuke **Produktų filtrai** nustatykite parinktis **Įgalinti kliento filtrus** ir (arba) **Įgalinti tiekėjo filtrus** į *Taip*. |

## <a name="set-up-product-filters"></a>Produktų filtrų nustatymas

Produktų filtrai pateikia iki 10 **Filtro pavadinimo** charakteristikų, kurios yra išvardijimo („enum”) reikšmės. Šias išvardijimo reikšmes galima pasirinkti kuriant produktų filtrą. Išvardijimo reikšmes nuo *1 kodo* iki *10 kodo* yra apibrėžtos sistemos ir atitinka konkrečią prekės charakteristiką arba atributą. Pavyzdžiui, *1 kodas* gali rodyti prekes, kurios turi pavojingos medžiagos klasifikaciją. *2 kodas* gali rodyti prekes, kurias gali pirkti tik tiekėjai. Tada produktų filtrai apibrėžia konkrečią **Filtro kodo** reikšmę, susietą su **Filtro pavadinimo** reikšme.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Produktų filtrai \> Produktų filtrai**.
1. Veiksmų srityje pasirinkite **Naujas** produktų filtro pridėjimui į tinklelį.
1. Lauke **Filtro pavadinimas** pasirinkite reikšmę.
1. Lauke **Filtro kodas** įveskite reikšmę.

    ![Produktų filtro nustatymas](media/Product_Filters10.png "Produktų filtro nustatymas")

1. Lauke **Aprašas** įveskite kodo pavadinimą. Pavyzdžiui, *2 kodas* gali rodyti tiekėjus. Tada galite sukurti produktų filtrą konkrečiam tiekėjui ar tiekėjų grupei. Daugiau informacijos žiūrėkite tolesniame šios temos skyriuje [Tiekėjų filtrų kodų nustatymas](#vendor-product-filters).

    ![Produktų filtrų rinkinys](media/Product_Filters.png "Produktų filtrų rinkinys")

## <a name="set-up-product-filter-groups"></a>Produktų filtrų grupių nustatymas

Galite naudoti filtrų grupes filtrų kodams grupuoti. Ši galimybė yra naudinga, kai grupė naudojama vietos nurodymo užklausoje ir norite ieškoti grupės, o ne kodų sekos. Kiekviena filtrų grupė yra susieta su prekių grupe.

> [!IMPORTANT]
> Ne visos filtrų grupės yra galimos filtrų kodams, didesnėms nei *4 kodas* (tai yra, nuo *5 kodo* iki *10 kodo*). Pavyzdžiui, nors išleistiems produktams bus įtraukti visi produktų filtrų kodai, filtrų kodų grupavimas nebus atnaujintas. Šis veikimo būdas gali būti atnaujintas naujesniuose leidimuose.

Norėdami nustatyti filtrų grupes, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Produktų filtrai \> Produktų filtrų grupės**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Laukuose **1 grupė** ir **2 grupė** įveskite pavadinimus, kurie bus naudojami skirstant prekes į kategorijas.
1. „FastTab” skirtuke **Išsami informacija** pasirinkite **Nauja** pridėti naujai eilutei.
1. Laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** įveskite filtrų grupės pradžios ir pabaigos datas.
1. Lauke **Prekių grupė** pasirinkite prekių grupę, kuriai norite taikyti produktų filtrą.
1. Laukuose nuo **1 kodas** iki **10 kodas** pasirinkite filtrų kodus jų įtraukimui į grupę, kaip reikalaujama.

    ![Prekių grupė](media/ProdFilterGroup.png "Prekių grupė")

> [!NOTE]
> Jei uždarydami puslapį gaunate klaidos pranešimą, galimai trūksta kodo nustatymo. Puslapyje **Prekių grupės** galite padaryti kodus privalomus prekių grupei pasirinkdami žymės langelius **Priskirti 1 filtro kodą prekės grupei**, **Priskirti 2 filtro kodą prekės grupei** ir taip toliau.

## <a name="set-up-filter-codes-on-item-groups"></a>Nustatykite filtrų kodus prekių grupėms

Nustatydami prekių grupės filtrų kodus, galite sukurti kodus, kurie yra būtini produktams, susietiems su ta prekių grupe.

Norėdami nustatyti filtrų kodus prekių grupėms, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Nustatymas \> Atsargos \> Prekių grupės**.
1. Veiksmų srityje pasirinkite **Nauja** prekių grupės sukūrimui.
1. Lauke **Prekių grupė** įveskite pavadinimą.
1. Lauke **Pavadinimas** įveskite aprašomąjį pavadinimą.
1. „FastTab“ skirtuko **Sandėlis** skyriuje **Reikalaujamas filtras** pasirinkite žymės langelius filtrų kodams, kurie turi būti nustatyti su prekių grupe susietiems produktams.

    Norėdami atnaujinti išleistą produktą, veiksmo srityje atidarykite jo puslapį **Išleisto produkto informacija** ir pasirinkite **Redaguoti**. Tada su kodais susieti filtrai tampa prieinami **Sandėlio** „FastTab” skirtuke.

    ![Prekių grupės](media/ItemGroup10.png "Prekių grupės")

1. Skyriuje **Prekių grupės filtras** pasirinkite žymės langelius grupėms, kurie turi atitikti filtro grupę, kuri yra numatytoji filtro grupė prekei.

    Pavyzdžiui, jei pasirinkti **Naudoti 1 filtro kodą** ir **Naudoti 2 filtro kodą** žymės langeliai, abu prekės 1 ir 2 filtrų kodai turi atitikti filtrų grupės konfigūraciją prekės grupei, nes tik tokiu atveju bus galima pasirinkti filtrų grupę. Kai kuriate naują prekė, pasirinkta filtro grupė bus numatytoji filtro grupė **1 grupė** ir **2 grupė** laukuose, esančiuose **Sandėlio** „FastTab skirtuke”, **Išleisto produkto informacija** puslapyje.

> [!IMPORTANT]
> Produktų filtro kodai įgalinami tik prekėms, naudojančioms išplėstinį sandėlio valdymą.

## <a name="specify-filter-codes-for-released-products"></a>Filtrų kodų nurodymas išleistiems produktams

Norėdami nustatyti filtrų kodus išleistiems produktams, atlikite šiuos veiksmus. Pavyzdžiui, galite naudoti filtrų kodus grupuoti pavojingiems produktams, kuriuos perka tam tikras tiekėjas.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Veiksmų srityje pasirinkite **Naujas** produktui sukurti.
1. Dialogo lange **Naujas išleistas produktas** įveskite duomenis, kurių reikia norint sukurti naujo produkto pagrindą, o tada pasirinkite **Gerai**.

    Produktų filtrų kodai nėra įgalinti, nebent su produktu susieta prekių grupė yra sukonfigūruota filtrų kodams.

    Daugiau informacijos žiūrėkite [Naujo produkto kūrimas](../pim/tasks/create-new-product.md).

1. „FastTab” skirtuko **Sandėlis** skyriuje **Produktų filtrų kodai** pasirinkite filtrų kodus nuo **1 kodo** iki **10 kodo** laukų, kaip reikalaujama, kad būtų galima nurodyti produkto filtrų kodus.

## <a name="set-up-generally-available-items"></a>Bendrai pasiekiamų prekių nustatymas

Galite nustatyti, kad konkrečios atsargų prekės būtų pasiekiamos tik klientams, tik tiekėjams, arba tiek klientams, tiek tiekėjams.

> [!NOTE]
> Klientų ir tiekėjų filtrai netaikomi jokiai prekei, kuri nustatyta kaip bendrai pasiekiama prekė.

Norėdami nustatyti bendrai pasiekiamas prekes, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Produktų filtrai \> Bendrai pasiekiami produktai**.
1. Veiksmų srityje pasirinkite **Naujas** įrašui sukurti.
1. Lauke **Klientas ir tiekėjas** pasirinkite *Klientas*, *Tiekėjas* arba *Visi* tam, kad padarytumėte prekes prieinamas klientams, tiekėjams arba abiems.
1. Lauke **Pradžios data/laikas** įveskite datą ir laiką, kada prekė taps prieinama.
1. Lauke **Prekių grupė** pasirinkite prekių grupę.
1. Laukuose nuo **1 kodo** iki **10 kodo** pasirinkite filtrų kodus, kuriuos naudojant bus apribotos bendrai pasiekiamos prekės.

    Pasirinkę prekių grupę, nustatote ją kaip bendrai pasiekiamą. Pasirinkdami filtrų kodus šiuose laukuose, apribojate pasiekiamas prekes.

## <a name="set-up-customer-product-filters"></a>Kliento produktų filtrų nustatymas

Galite naudoti šią pasirinktinę procedūrą nurodyti prekes, kurios turėtų būti pasiekiamos klientui, kaip ir prekės padarytos prieinamomis naudojant filtro konfigūraciją **Bendrai pasiekiamų prekių** puslapyje. Galite nustatyti kelis filtrus vienam klientui.

Kliento filtrų kodų nustatymui atlikite šiuos veiksmus.

1. Eikite į **Pardavimas ir rinkodara \> Klientai \> Visi klientai**.
1. Pasirinkti klientą.
1. Veiksmų srities skirtuko **Klientas** grupėje **Nustatyti** pasirinkite **Produktų filtrai**.
1. Veiksmų srities puslapyje **Produkto filtrų kodai** pasirinkite **Naujas**.
1. Laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** įveskite pasirinktos prekių grupės pradžios ir pabaigos datas.
1. Lauke **Prekių grupė** pasirinkite prekių grupę.
1. Laukuose nuo **1 kodo** iki **10 kodo** pasirinkite filtrų kodus, kurie bus naudojami kaip apribojimo kriterijai prekėms, pasiekiamoms klientams pasirinktoje prekių grupėje. Turite pasirinkti kiekvienam filtro kodui, nustatytam prekės grupei.

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a>Tiekėjo produktų filtrų nustatymas

Galite naudoti šią pasirinktinę procedūrą nurodyti prekes, kurios turėtų būti pasiekiamos tiekėjui, kaip ir prekės padarytos prieinamomis naudojant filtro konfigūraciją **Bendrai pasiekiamų prekių** puslapyje. Vienam tiekėjui galite nustatyti kelis filtrus.

Tiekėjo filtrų kodų nustatymui atlikite šiuos veiksmus.

1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Tiekėjai \> Visi tiekėjai**.
1. Pasirinkite tiekėją.
1. Veiksmų srities skirtuko **Tiekėjas** grupėje **Nustatyti** pasirinkite **Produktų filtrai**.
1. Veiksmų srities puslapyje **Filtrų kodai** pasirinkite **Naujas**.
1. Laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** įveskite pasirinktos prekių grupės pradžios ir pabaigos datas.
1. Lauke **Prekių grupė** pasirinkite prekių grupę.
1. Laukuose nuo **1 kodo** iki **10 kodo** pasirinkite filtrų kodus, kurie bus naudojami kaip apribojimo kriterijai prekėms, pasiekiamoms tiekėjams pasirinktoje prekių grupėje. Turite pasirinkti kiekvienam filtro kodui, nustatytam prekės grupei.

> [!NOTE]
> Tiekėjo produktų filtro konfigūracija taikoma išleistiems produktams, kuriuose įgalinti sandėlio valdymo procesai susietai saugojimo dimensijų grupei. Filtro kodai naudojami siekiant nustatyti, ar sistema leis vartotojams įsigyti tam tikrą prekę iš tam tikro tiekėjo, kai jie kuria pirkimo užsakymo eilutes. „Microsoft Dynamics 365 Supply Chain Management” yra du tiekėjo patvirtinimo tvarkymo metodai. Jei yra vienas ar daugiau išleistų produktų, kurio laukas **Patvirtinto tiekėjo patikrinimo metodas** yra nustatytas į *Tik įspėjimas* arba *Neleidžiama*, abu tiekėjo patvirtinimo metodai gali būti įjungti toms prekėms. Ši situacija gali sukelti problemų, kai vartotojai kuria pirkimo užsakymo eilutes.

## <a name="see-also"></a>Taip pat žiūrėkite

[Daugiau informacijos ieškokite tinklaraščio įraše WMS-sandėlio filtrų kodai](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
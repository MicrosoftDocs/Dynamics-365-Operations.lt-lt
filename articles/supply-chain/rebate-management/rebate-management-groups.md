---
title: Grąžinimų valdymo grupės
description: Šiame skyriuje paaiškinta, kaip nustatyti grąžinimų valdymų grupes. Grąžinimų valdymo grupės gali būti naudojamos skaičiuojant grąžinimus ir pridėtos prie pagrindinio įrašo.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271082"
---
# <a name="rebate-management-groups"></a>Grąžinimų valdymo grupės

[!include [banner](../includes/banner.md)]

Grąžinimo valdymo skaičiavimus galima pagrįsti grupėmis. Grąžinimų valdymo grupės gali būti sukurtos klientams, tiekėjams ir prekėms. Jas galima pridėti prie pagrindinio įrašo.

## <a name="rebate-management-customer-groups"></a>Grąžinimų valdymo kliento grupės

Skaičiavimas klientų grupei dažnai sukuriamas įmonių grandinei, pavyzdžiui, prekybos centrų grandinei ar franšizės įmonei. Tokio tipo skaičiavimas įprastai susijęs su grąžinimu.

Atskaitymas dažnai apskaičiuojamas neatsižvelgiant į tai, kam buvo parduotas tinkamumo užsakymas. Tačiau yra išimčių. Pavyzdžiui, licencijos klientas gali sukurti atskaitymo schemą, pagal kurią klientų grupė A gaus 4 procentus, tačiau klientų grupė B gaus tik 3 procentus.

### <a name="set-up-customer-groups"></a>Nustatyti klientų grupes

Norėdami dirbti su grąžinimų valdymo kliento grupėmis, eikite į **Grąžinimo valdymas \> Grąžinimo valdymo grupių nustatymas \> Kliento grupės**. Galite naudoti veiksmų srities mygtukus grupių pridėjimui ir panaikinimui, kaip reikalinga. Kiekvienai grupei nustatykite toliau pateiktus laukus:

- **Grąžinimų valdymo grupė** – įveskite unikalųjį grupės pavadinimą.
- **Aprašymas** – Įveskite grupės aprašymą, jei norite pateikti daugiau informacijos apie jos naudojimą.

### <a name="manage-customer-group-assignments"></a>Klientų grupių priskyrimų tvarkymas

Kiekvienas klientas gali priklausyti bet kokiam grąžinimo valdymo grupių skaičiui. Norėdami peržiūrėti ir priskirti grupės narius, galite pradėti nuo grupių arba nuo klientų sąrašo.

Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos grupės klientus, atlikite šiuos veiksmus.

1. Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Klientų grupės**.
1. Pasirinkite norimą valdyti grupę.
1. Veiksmų srityje pasirinkite **Klientai**. Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas klientų, kurie jau yra pasirinktos grupės nariai, sąrašas.
1. Norėdami pridėti naują klientą į grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį. Tada nustatykite šį lauką naujai eilutei:

    - **Kliento sąskaita** – pasirinkite kliento sąskaitos ID.

1. Norėdami pašalinti klientą iš grupės, pasirinkite klientą, o tada veiksmų srityje pasirinkite **Naikinti**.

Norėdami peržiūrėti, pridėti arba pašalinti pasirinkto kliento priskyrimus grupėms, atlikite šiuos veiksmus.

1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.
1. Pasirinkite klientą, su kuriuo norite dirbti.
1. Veiksmų srities skirtuke **Klientas**, grupėje **Grąžinimų valdymas** pasirinkite **Grąžinimų valdymo grupės**. Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas grupių, kurioms pasirinktas klientas jau priklauso, sąrašas.
1. Norėdami pridėti klientą į naują grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį. Tada nustatykite šį lauką naujai eilutei:

    - **Grąžinimų valdymo grupė** – pasirinkite grupę, į kurią norite įtraukti klientą.

1. Norėdami pašalinti klientą iš grupės, pasirinkite grupę, o tada veiksmų srityje pasirinkite **Naikinti**.

## <a name="rebate-management-vendor-groups"></a>Grąžinimų valdymo tiekėjo grupės

Skaičiavimas tiekėjų grupei dažnai kuriamas pristatymo taškų grupei. Tokio tipo skaičiavimas įprastai susijęs su grąžinimu.

### <a name="set-up-vendor-groups"></a>Tiekėjo grupių nustatymas

Norėdami dirbti su grąžinimų valdymo tiekėjo grupėmis, eikite į **Grąžinimo valdymas \> Grąžinimo valdymo grupių nustatymas \> Tiekėjo grupės**. Galite naudoti veiksmų srities mygtukus grupių pridėjimui ir panaikinimui, kaip reikalinga. Kiekvienai grupei nustatykite toliau pateiktus laukus:

- **Grąžinimų valdymo grupė** – įveskite unikalųjį grupės pavadinimą.
- **Aprašymas** – Įveskite grupės aprašymą, jei norite pateikti daugiau informacijos apie jos naudojimą.

### <a name="manage-vendor-group-assignments"></a>Tiekėjo grupių priskyrimų tvarkymas

Kiekvienas tiekėjas gali priklausyti bet kokiam grąžinimo valdymo grupių skaičiui. Norėdami peržiūrėti ir priskirti grupės narius, galite pradėti nuo grupių arba nuo tiekėjų sąrašo.

Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos grupės tiekėjus, atlikite šiuos veiksmus.

1. Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Tiekėjų grupės**.
1. Pasirinkite norimą valdyti grupę.
1. Veiksmų srityje pasirinkite **Tiekėjai**. Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas tiekėjų, kurie jau yra pasirinktos grupės nariai, sąrašas.
1. Norėdami pridėti naują tiekėją į grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį. Tada nustatykite šį lauką naujai eilutei:

    - **Tiekėjo sąskaita** – pasirinkite tiekėjo sąskaitos ID.

1. Norėdami pašalinti tiekėją iš grupės, pasirinkite tiekėją, o tada veiksmų srityje pasirinkite **Naikinti**.

Norėdami peržiūrėti, pridėti arba pašalinti pasirinkto tiekėjo priskyrimus grupėms, atlikite šiuos veiksmus.

1. Eikite į **Mokėtinos sumos \> Tiekėjai \> Visi tiekėjai**.
1. Pasirinkite tiekėją, su kuriuo norite dirbti.
1. Veiksmų srities skirtuke **Tiekėjas**, grupėje **Grąžinimų valdymas** pasirinkite **Grąžinimų valdymo grupės**. Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas grupių, kurioms pasirinktas tiekėjas jau priklauso, sąrašas.
1. Norėdami pridėti tiekėją į naują grupę, iš veiksmų srities pasirinkite **Naujas** eilutės įtraukimui į tinklelį. Tada nustatykite šį lauką naujai eilutei:

    - **Grąžinimų valdymo grupė** – pasirinkite grupę, į kurią norite įtraukti tiekėją.

1. Norėdami pašalinti tiekėją iš grupės, pasirinkite grupę, o tada veiksmų srityje pasirinkite **Naikinti**.

## <a name="item-rebate-groups"></a>Prekių grąžinimo grupės

Grupuodami prekes turite daugiau lankstumo, kai apskaičiuojami grąžinimai ir atskaitymai. Šis būdas dažnai yra efektyvesnis nustatant grąžinimus ir atskaitymus klientams ir tiekėjams.

### <a name="set-up-item-groups"></a>Nustatyti prekių grupes

Norėdami dirbti su grąžinimų valdymo prekių grupėmis, eikite į **Grąžinimo valdymas \> Grąžinimo valdymo grupių nustatymas \> Prekių grupės**. Galite naudoti veiksmų srities mygtukus grupių pridėjimui ir panaikinimui, kaip reikalinga. Kiekvienai grupei nustatykite toliau pateiktus laukus:

- **Grąžinimų valdymo grupė** – įveskite unikalųjį grupės pavadinimą.
- **Aprašymas** – Įveskite grupės aprašymą, jei norite pateikti daugiau informacijos apie jos naudojimą.

### <a name="manage-item-group-assignments"></a>Prekių grupių priskyrimų tvarkymas

Kiekviena prekė gali priklausyti bet kokiam grąžinimo valdymo grupių skaičiui. Norėdami peržiūrėti ir priskirti grupės narius, galite pradėti nuo grupių arba nuo prekių sąrašo. Taip pat galite įtraukti prekes ir pagal kategorijų hierarchiją.

Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos grupės prekes, atlikite šiuos veiksmus.

1. Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Prekių grupės**.
1. Pasirinkite norimą valdyti grupę.
1. Veiksmų srityje pasirinkite **Prekės**. Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas prekių, kurios jau yra pasirinktos grupės narės, sąrašas.
1. Norėdami pridėti prekę į grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį. Tada nustatykite šį lauką naujai eilutei:

    - **Prekės sąskaita** – pasirinkite prekės sąskaitos ID.

1. Norėdami pašalinti prekę iš grupės, pasirinkite prekę, o tada veiksmų srityje pasirinkite **Naikinti**.

Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos prekės priskyrimus grupėms, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite prekę, su kuria norite dirbti.
1. Veiksmų srities skirtuke **Produktas**, grupėje **Grąžinimų valdymas** pasirinkite **Grąžinimų valdymo grupės**. Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas grupių, kurioms pasirinkta prekė jau priklauso, sąrašas.
1. Norėdami pridėti prekę į naują grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį. Tada nustatykite šį lauką naujai eilutei:

    - **Grąžinimų valdymo grupė** – pasirinkite grupę, į kurią norite įtraukti prekę.

1. Norėdami pašalinti prekę iš grupės, pasirinkite grupę, o tada veiksmų srityje pasirinkite **Naikinti**.

Norėdami įtraukti prekes į grupę pagal jūsų kategorijų hierarchiją, atlikite šiuos veiksmus.

1. Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Prekių grupės**.
1. Pasirinkite norimą valdyti grupę.
1. Veiksmų srityje pasirinkite **Įtraukti prekes**.
1. Dialogo lango **Įtraukti elementus** lauke **Kategorijų hierarchija** pasirinkite aukščiausio lygio kategoriją.
1. Kairiojoje srityje atidaroma prekių hierarchija. Pasirinkite ieškomą hierarchijos lygį. 
1. Dabar prekės iš pasirinktos hierarchijos ir jos lygio yra išvardintos dešinėje srityje. Norėdami dirbti su sritimi, atlikite šiuos veiksmus:

    - Pasirinkite kiekvienos prekės, kurią norite įtraukti, žymės langelį.
    - Pasirinkite žymės langelį tinklelio antraštėje, kad pasirinktumėte visas išvardytas prekes.
    - Pasirinkite mygtuką **Rodyti pasirinktus**, kad būtų filtruojamas tinklelis taip, jog jame būtų rodomos tik jūsų pasirinktos prekės. Vėl pasirinkite mygtuką, jei norite grįžti į pilną sąrašą.

1. Pasirinkite **Gerai**, jei norite pritaikyti savo prekių pasirinkimą pasirinktai grupei.

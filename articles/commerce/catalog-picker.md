---
title: Katalogo išrinkiklio modulis
description: Šiame straipsnyje aprašomi katalogo išrinkiklio moduliai Microsoft Dynamics 365 Commerce ir aprašoma, kaip įtraukti juos į "business-to-business" (B2B) el. komercijos svetaines.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136931"
---
# <a name="catalog-picker-module"></a>Katalogo išrinkiklio modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi katalogo išrinkiklio moduliai Microsoft Dynamics 365 Commerce ir aprašoma, kaip įtraukti juos į "business-to-business" (B2B) el. komercijos svetaines.

Katalogo išrinkiklio modulis yra specialus konteineris, naudojamas išvardyti visus produktų katalogus, kuriuos gali naudoti B2B svetainės prekybos vartotojai. Keli katalogai šiuo metu palaikomi tik B2B svetainėse.

Šioje iliustracijoje pateikiamas katalogo išrinkiklio modulio pavyzdys.

![Katalogo išrinkiklio modulio, kuriame išvardyti trys produktų katalogai, pavyzdys.](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>Įtraukti katalogo išrinkiklio modulį į savo svetainę

Norėdami įtraukti katalogo išrinkiklio modulį į savo svetainę "Commerce" svetainių generatoriuje, atlikite šiuos veiksmus.

### <a name="create-a-catalog-picker-page"></a>Sukurti katalogo išrinkiklio puslapį

Pirma sukurkite katalogo išrinkiklio puslapį.

1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Kurti naują puslapį** po Puslapio pavadinimas **įveskite** Katalogo **parinkiklis**.
1. Prie **puslapio URL** įveskite puslapio URL ir pasirinkite **Pirmyn**.

    ![Kurti naują puslapio dialogo langą.](./media/Create-catalog-picker-page.png)

1. Dalyje **Pasirinkti šabloną** pasirinkite **Bendrasis turinys**, tada – **Pirmyn**.
1. Dalyje **Pasirinkti maketą** pasirinkite **Kintamas maketas** ir pasirinkite **Pirmyn**.
1. Dalyje **Peržiūrėti ir baigti** peržiūrėkite puslapio konfigūraciją. Jei turite redaguoti puslapio informaciją, pasirinkite **Atgal**. Jei puslapio informacija teisinga, pasirinkite Kurti **puslapį**.
1. Dalyje **Katalogo išrinkiklis** pasirinkite **Pagrindinis atrinkiklis**, pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.

    ![Modulio įtraukimas į pagrindinį atminties atminties laiką modulyje Katalogo išrinkiklis.](./media/Author-web-page-catalog-picker-1.png)

1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Pasirinkite konteinerio **laiko** atminties laiką, pasirinkite elipsę (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite katalogo išrinkiklio **modulį**, tada pasirinkite **Gerai**.
1. Katalogo išrinkiklio **ypatybės** srityje antraštė **pasirinkite** Katalogai **·**, tada įveskite katalogo išrinkiklio puslapio antraštę.
1. Dalyje **Antraštės lygis** pasirinkite antraštės lygį ir pasirinkite **Gerai**.
1. Įveskite **tekstą**, kuris bus rodomas katalogo parinkiklio puslapio viršuje.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

### <a name="add-a-link-on-your-account-page"></a>Pridėti saitą savo sąskaitos puslapyje

Tada pridėkite nuorodą prie savo katalogo išrinkiklio puslapio savo **Puslapyje Mano** sąskaita.

1. Eikite **į Puslapius**, suraskite ir pasirinkite savo svetainės **Puslapį** Mano sąskaita, tada pasirinkite **Redaguoti**.
1. Pagrindinį puslapio **atminties** atminties lauką pasirinkite bendrosios sąskaitos išklotinės **dalies atminties laiką**. 
1. Abonemento bendrosios **išklotinės dalies** ypatybės srityje Saitai **pasirinkite** Įtraukti **veiksmo saitą**, tada pasirinkite Veiksmo **saitas**.
1. Veiksmo saito **dialogo** lange prie Saito **teksto** įveskite saito su katalogo parinkiklio puslapiu tekstą.
1. Prie **Saito** paskirties vietos pasirinkite **Įtraukti saitą**.
1. Dialogo lange **Įtraukti saitą** pasirinkite Pasirinktinį **puslapį**, tada – **Pirmyn**.
1. Dalyje **Pavadinimas** pasirinkite katalogo išrinkiklio puslapį, pasirinkite **Taikyti**, tada – **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Šioje iliustracijoje pateikiamas sąskaitų puslapio su nuoroda į katalogo puslapį pavyzdys.

![Mano sąskaitų puslapis su saitu su katalogu.](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>Įtraukti saitą iš antraštės

Galiausiai, pridėkite saitą iš svetainės antraštės į savo katalogus.

1. Eikite **į** Fragmentus, raskite ir pasirinkite savo svetainės antraštės fragmentą, tada pasirinkite **Redaguoti**.
1. Pasirinkite atkarpą **Antraštė**. 
1. Antraštės ypatybės **srityje**, po Mano sąskaitos **saitais**, pasirinkite Įtraukti **veiksmo** saitą, tada pasirinkite Veiksmo **saitas**.
1. Veiksmo saito **dialogo** lange prie Saito **teksto** įveskite saito su katalogo parinkiklio puslapiu tekstą.
1. Prie **Saito** paskirties vietos pasirinkite **Įtraukti saitą**.
1. Dialogo lange **Įtraukti saitą** pasirinkite Pasirinktinį **puslapį**, tada – **Pirmyn**.
1. Dalyje **Pavadinimas** pasirinkite katalogo išrinkiklio puslapį, pasirinkite **Taikyti**, tada – **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte antraštės fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Šioje iliustracijoje pateikiamas eleksinės svetainės antraštės su saitais į B2B katalogą pavyzdys.

![El. pašto svetainės antraštė su išplečiamu saitu su katalogu.](./media/catalog-in-header.png)


## <a name="additional-resources"></a>Papildomi ištekliai 

[B2B svetainių „Commerce“ katalogų kūrimas](catalogs-b2b-sites.md)

[„Commerce“ katalogų išplečiamumo poveikis, skirtas B2B tinkinimams](catalogs-b2b-sites-dev.md)

[B2B DUK svetainių „Commerce“ katalogai](catalogs-b2b-sites-FAQ.md)

[Sąskaitos valdymo puslapiai ir moduliai](account-management.md)

[Antraštės modulis](author-header-module.md)

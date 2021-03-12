---
title: Naršymo kelio modulis
description: Šioje temoje aprašomi naršymo kelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1883281c62575ae0b48b6e584876185bb179b4f4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986084"
---
# <a name="breadcrumb-module"></a>Naršymo kelio modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi naršymo kelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūra

Naršymo kelio moduliai naudojami antrinei navigacijai svetainės puslapiuose. Jis paprastai rodomas puslapio viršuje, po antrašte. Nors naršymo kelio modulius galima įtraukti į bet kurį puslapį, dažniausiai jie naudojami produkto informacijos puslapiuose (PDP), kad būtų rodoma produktų kategorijų hierarchija ir būtų užtikrintas greitas būdas naršyti po svetainę. Naršymo kelio modulis taip pat gali būti naudojamas siekiant parodyti saitą „Atgal į rezultatus“, kai vartotojai atidaro PDP ieškos ar sąrašo puslapyje. Šitaip vartotojai gali greitai grįžti prie filtruoto sąrašo puslapio ir tęsti apsipirkimą.

Puslapiuose, kurie turi produktų kategorijos konteksto, pvz., PDP ir kategorijos puslapiuose, naršymo kelio moduliai rodo kategorijų hierarchiją. Puslapiuose, kuriuose nėra kategorijos konteksto, naršymo kelio moduliai pagal numatytąją nuostatą rodo **&lt;Svetainės šaknis&gt; / &lt;Dabartinis puslapis&gt;**. Naršymo kelio modulius taip pat galima rankiniu būdu konfigūruoti ir kitų tipų svetainės puslapiuose, kad būtų rodomi saitai į konkrečius svetainės puslapius.

> [!NOTE]
> Naršymo kelio modulį galima naudoti „Dynamics 365 Commerce“ 10.0.12 leidime.

Toliau pateiktame paveikslėlyje parodytas naršymo kelio modulio pavyzdys, rodantis kategorijų hierarchiją PDP.

![Naršymo kelio modulio pavyzdys](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>Naršymo modulio parametrai

Naršymo kelio modulis priklauso nuo parametro **Naršymo kelio rodymo tipas PDP**, kuris nurodytas svetainių daryklės dalyje **Svetainės parametrai \> Plėtiniai**. Galimos trys šio parametro vertės:

- **Rodyti kategorijų hierarchiją** – kai ši vertė pasirinkta, naudojant naršymo kelio modulį bus rodoma išsami PDP peržiūrimo produkto kategorijų hierarchija.
- **Rodyti „atgal į rezultatus“** – kai ši vertė pasirinkta, naršymo kelio modulis rodo saitą „Atgal į rezultatus“ PDP, jei vartotojas atidarė PDP modulyje, kuriame galima naudoti saitą „Atgal į rezultatus“. Šią funkciją galima, kai vartotojai naršo iš kategorijos, ieškos, sąrašo ir rekomendacijų sąrašų puslapių. Tam, kad ši funkcija veiktų, produktų rinkinys ir ieškos rezultatų moduliai turi ypatybę, kuri pavadinta **Leisti grįžti į rezultatus PDP**. Ši ypatybė suteikia jums galimybę apibrėžti, kurie moduliai turi palaikyti saito „Atgal į rezultatus“ funkciją PDP. Pavyzdžiui, kai pasirinkta naršymo kelio modulio parametro **Naršymo kelio rodymo tipas PDP** ypatybė **Rodyti „atgal į rezultatus“** ir pasirinkta ieškos puslapio ieškos rezultatų modulio ypatybė **Leisti grįžti į rezultatus PDP**, saitą „Atgal į rezultatus“ bus rodoma tada, kai vartotojai pereina iš ieškos puslapio į PDP.
- **Rodyti kategorijų hierarchiją ir grįžimo į rezultatus saitą** – ši vertė yra ankstesnių dviejų verčių derinys. Pasirinkus šią vertę, naudojant naršymo kelio modulį, PDP bus rodoma ir išsami kategorijų hierarchija ir saitą „Atgal į rezultatus“ (jei sukonfigūruota).

> [!IMPORTANT]
> Šie parametrai galimi „Dynamics 365 Commerce” 10.0.12 leidime. Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json. Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="breadcrumb-module-properties"></a>Naršymo kelio modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | aprašymas |
|---------------|--------|-------------|
| Šakninis | Tekstas arba saitas| Ši neprivaloma ypatybė nurodo naršymo kelio šakninės svetainės saito tekstą ir paskirtį. Jei ši ypatybė nesukonfigūruota, šaknis nebus apibrėžta. |
| Naršymo kelio saitas | Saitas | Ši pasirenkama ypatybė nurodo neautomatiniu būdu sukonfigūruoto naršymo kelio saitus, jei šie saitai būtini. Saitai rodomi tokia tvarka, kokia jie pateikti sąraše. |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>Naršymo kelio modulio įtraukimas į naują puslapį

Norėdami į PDP įtraukti naršymo kelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Saito nustatymus \> Plėtiniai** ir tada **Naršymo kelio rodymo tipo PDP** nustatymuose pasirinkite **Rodyti kategorijos hierarchiją**.
1. Eikite į **Šablonai** ir pasirinkite PDP šabloną.
1. Vietoje **Konteineris**, kurioje yra pirkimo langelio modulis, pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir atidarykite PDP, kuris naudoja PDP šabloną. Jei PDP dar nėra, sukurkite jį.
1. Vietoje **Konteineris**, kurioje yra pirkimo langelio modulis, pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.
1. Dalies **Naršymo kelias** ypatybių srityje, dalyje **Šaknis**, pasirinkite **Saito tekstas**.
1. Dialogo lange **Saito tekstas** įveskite **Pagrindinis**, tada dalyje **Saito paskirtis** pasirinkite **Įtraukti saitą**.
1. Dialogo lange **Įtraukti saitą** pasirinkite naršymo kelio šaknies saitą, tada – **Gerai**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Naršymo meniu modulis](nav-menu-module.md)

[Svetainės išrinkiklio modulis](site-selector.md)

[Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga](category-search-page-overview.md)

[Produktų rinkinio moduliai](product-collection-module-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md)

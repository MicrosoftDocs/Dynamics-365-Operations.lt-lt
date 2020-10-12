---
title: Naršymo kelio modulis
description: Šioje temoje aprašomi naršymo kelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7c6f215c3a7539cc16b0d72594702e6bdde7c58e
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817115"
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

1. Eikite į **Svetainės parametrai /> Plėtiniai**, tada pasirinkite parametro **Naršymo kelio rodymo tipas PDP** vertę **Rodyti kategorijų hierarchiją**.
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

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga](category-search-page-overview.md)

[Produktų rinkinio moduliai](product-collection-module-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md)

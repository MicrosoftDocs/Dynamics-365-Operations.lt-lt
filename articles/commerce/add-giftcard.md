---
title: Dovanų kortelės modulis
description: Šioje temoje aprašomi dovanų kortelių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fa6b98bb41c0845cfa3ab36767f304ad70f46399
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/07/2020
ms.locfileid: "4414511"
---
# <a name="gift-card-module"></a>Dovanų kortelės modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi dovanų kortelių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūra

Dovanų kortelių moduliai yra įprasta mokėjimo forma, naudojama „e-Commerce” operacijose, ir juos galima naudoti pirkimo užbaigimo moduliuose, kad dovanų kortelės būtų priimtos. Dovanų kortelės modulis palaiko „Dynamics 365”, „SVS” ir „Givex” dovanų korteles. „SVS” ir „Givex” dovanų kortelėmis apmokama naudojant „Adyen” mokėjimo paslaugų teikėją. Daugiau informacijos apie išorinių dovanų kortelių, pvz., „SVS” ir „Givex”, palaikymą žr. [Išorinių dovanų kortelių palaikymas](./dev-itpro/gift-card.md).

> [!NOTE]
> „SVS” ir „Givex” dovanų kortelių panaudojimo pirkimo užbaigimo srauto metu palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.11 leidime. 

Galimi du dovanų kortelių moduliai:

- **Dovanų kortelė** – šis modulis gali būti naudojamas pirkimo užbaigimo puslapyje, norint naudoti dovanų kortelę kaip mokėjimo priemonę. 
- **Dovanų kortelės balanso tikrinimas** – šis modulis gali būti naudojamas bet kuriame puslapyje, norint patikrinti dovanų kortelės balansą. Šis modulis pasiekiamas 10.0.14 arba vėlesnio leidimo „Commerce“.

> [!NOTE]
> Dovanų kortelės balanso tikrinimo modulio palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.14 leidime.

Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapyje esančio dovanų kortelės modulio pavyzdys.

![Dovanų kortelės modulio pavyzdys](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Modulio ypatybės

- **Rodyti papildomus laukus** – ši ypatybė nurodo, kuriuos laukus reikia rodyti kartu su dovanų kortelės numeriu, kuris visada rodomas pagal numatytuosius nustatymus, naudojant dovanų korteles. Pavyzdžiui, kai kurios dovanų kortelės palaiko asmeninio identifikacijos numerio (PIN) rodymą, o kitos palaiko PIN ir galiojimo datos rodymą. Taip pat gali būti, kad ši ypatybė nustatyta į Nėra, tokiu atveju būtų rodomas tik dovanų kortelės numeris ir nebūtų jokių papildomų laukų.

Palaikomos reikšmės:
-   PIN
-   Galiojimo data
-   PIN ir galiojimo data 
-   Jokia

## <a name="site-settings-for-gift-card-modules"></a>Dovanų kortelių modulių svetainės parametrai

„Commerce“ svetainių rengyklės dalyje **Svetainės parametrai \> Plėtiniai** yra dovanų kortelės modulio parametras pavadinimu **Palaikomos dovanų kortelės tipas**. Šis parametras palaiko tris toliau pateiktas reikšmes.
- **„Dynamics 365” dovanų kortelė** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Dynamics 365” dovanų kortelėmis. Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.
- **„SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti tik „Givex” ir „SVS” dovanų kortelėmis. Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems ir anoniminiams vartotojams.
- **„Dynamics 365”, „SVS” ir „Givex” dovanų kortelės** – kai taikomas šis parametras, dovanų kortelės modulis leidžia apmokėti „Dynamics 365”, „Givex” ir „SVS” dovanų kortelėmis. Šis parametras palaikomas tik el. prekybos svetainėje prisijungusiems vartotojams.

> [!IMPORTANT]
> Šie parametrai pasiekiami „Dynamics 365 Commerce” 10.0.11 leidime ir reikalingi tik tada, kai reikia „SVS” ar „Givex” dovanų kortelių palaikymo. Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json. Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="add-a-gift-card-module-to-a-page"></a>Dovanų kortelės modulio įtraukimas į puslapį

Instrukcijų, kaip įtraukti dovanų kortelės modulį į pirkimo užbaigimo puslapį ir nustatyti reikiamas ypatybes, žr. [Pirkimo užbaigimo modulis](add-checkout-module.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Krepšelio modulis](add-cart-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Mokėjimo modulis](payment-module.md)

[Siuntimo adreso modulis](ship-address-module.md)

[Pristatymo parinkčių modulis](delivery-options-module.md)

[Paėmimo informacijos modulis](pickup-info-module.md)

[Išsamios užsakymo informacijos modulis](order-confirmation-module.md)

[Išorinių dovanų kortelių palaikymas](./dev-itpro/gift-card.md)

[SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md)

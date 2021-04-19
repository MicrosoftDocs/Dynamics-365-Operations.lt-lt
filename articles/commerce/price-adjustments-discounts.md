---
title: Kainų koregavimas ir nuolaidos
description: Šiame straipsnyje pateikiama informacija apie kainų koregavimus ir nuolaidas „Dynamics 365 Commerce“.
author: scott-tucker
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2d3e8025c5ab28296713634094694156f9addf62
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802796"
---
# <a name="price-adjustments-and-discounts"></a>Kainų koregavimas ir nuolaidos

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie kainų koregavimus ir nuolaidas „Dynamics 365 Commerce“.

„Commerce“ galite koreguoti produktų kainą, taip pat galite nustatyti nuolaidas, taikomas eilutės elementui arba operacijai elektroniniame kasos aparate (EKA), skambučių centro pardavimo užsakyme arba užsakyme internetu. Tiek kainų korekcijas, tiek nuolaidas galima susieti su kainų grupėmis. Kainų koregavimams ir nuolaidoms galite nurodyti vieną pradžios datą ir pabaigos datą arba pasikartojimo laikotarpį, nuolaidos kodą ir keletą papildomų atributų. 

Kainų koregavimą ir nuolaidos galima taikyti produktams, variantams arba kategorijoms. Jei produktui taikoma daugiau nei viena nuolaida, klientas gali gauti vieną iš nuolaidų arba jungtinę nuolaidą, atsižvelgiant į nuolaidos konfigūraciją. „Commerce“ automatiškai taiko nuolaidą ar nuolaidų derinį, kuris klientui pasiūlo geriausią kainą. Nustatydami kainos koregavimą arba nuolaidą įsitikinkite, kad kainų grupės priskiriamos tinkamiems kanalams, katalogams, priskyrimams arba lojalumo programoms, kurioms norite taikyti nuolaidą. Be to, jei norite automatiškai sugeneruoti nuolaidos ID, prieš nustatant naują kainą ar nuolaidą, puslapyje **„Commerce“ parametrai** nustatykite skaičių sekas.

> [!NOTE]
> Kainos koregavimą arba nuolaidą galima panaikinti. Tačiau bus prarasta statistinė informacija.

## <a name="types-of-discounts"></a>Nuolaidų tipai

Yra daug tipų nuolaidų:

- **Paprasta nuolaida** – vienas procentinis dydis arba suma.
- **Kiekio nuolaida** – nuolaida, taikoma perkant du ar daugiau produktų.
- **Nuolaida prekių rinkiniui** – nuolaida, suteikiama perkant tam tikrą produktų derinį.
- **Ribinė nuolaida** – nuolaida, taikoma, kai operacijos bendroji suma yra didesnė nei nurodyta suma.
- **Nuomotoju pagrįsta nuolaida** – Nuolaida, kuri yra taikoma, kai perlaidos bendra suma yra didesnė nei nurodyta suma ir konkretus apmokėjimo tipas (pavyzdžiui, grynieji, kredito ar debeto kortelė) naudojama apmokėjimui.
- **Siuntimo nuolaida** – Nuolaida, kuri yra taikoma, kai perlaidos bendra suma yra didesnė nei nurodyta suma ir konkretus pristatymo būdas (pavyzdžiui, dviejų dienų siuntimas ar siuntimas per naktį) naudojamas užsakyme.

Tiek kainų korekcijas, tiek nuolaidas galima susieti su kainų grupėmis. Kainų grupės gali būti susietos su kanalais, katalogais, priskyrimais ir lojalumo programomis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
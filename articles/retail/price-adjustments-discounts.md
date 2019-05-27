---
title: Kainų koregavimas ir nuolaidos
description: Šiame straipsnyje pateikiama informacija apie kainų koregavimus ir nuolaidas „Microsoft Dynamics 365 for Retail“.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 61ac8e5fbdc4d91bb5bc5372a7fb96633043473a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549457"
---
# <a name="price-adjustments-and-discounts"></a>Kainų koregavimas ir nuolaidos

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie kainų koregavimus ir nuolaidas „Microsoft Dynamics 365 for Retail“.

Naudodami „Dynamics 365 for Retail“ galite koreguoti produktų kainas ir nustatyti nuolaidas, taikomas eilutės elementui arba elektroninio kasos aparato (EKA) operacijai, vykdydami skambučių centro pardavimo užsakymą arba internetinį užsakymą. Tiek kainų korekcijas, tiek nuolaidas galima susieti su kainų grupėmis. Kainų koregavimams ir nuolaidoms galite nurodyti vieną pradžios datą ir pabaigos datą arba pasikartojimo laikotarpį, nuolaidos kodą ir keletą papildomų atributų. Kainų koregavimą ir nuolaidos galima taikyti produktams, variantams arba kategorijoms. Jei produktui taikoma daugiau nei viena nuolaida, klientas gali gauti vieną iš nuolaidų arba jungtinę nuolaidą, atsižvelgiant į nuolaidos konfigūraciją. „Dynamics 365 for Retail“ automatiškai taikoma nuolaida ar jungtinė nuolaida ir taip klientui suteikiama geriausia kaina. Nustatydami kainos koregavimą arba nuolaidą įsitikinkite, kad kainų grupės priskiriamos tinkamiems kanalams, katalogams, priskyrimams arba lojalumo programoms, kurioms norite taikyti nuolaidą. Be to, jei norite automatiškai generuoti nuolaidos ID, prieš koreguodami kainą arba nuolaidą, puslapyje **Mažmeninės prekybos parametrai** nustatykite numerių sekas.

> [!NOTE]
> Kainos koregavimą arba nuolaidą galima panaikinti. Tačiau bus prarasta statistinė informacija.

## <a name="types-of-discounts"></a>Nuolaidų tipai

Mažmeninės prekybos nuolaidos būna keturių tipų.

- **Paprasta nuolaida** – vienas procentinis dydis arba suma.
- **Kiekio nuolaida** – nuolaida, taikoma perkant du ar daugiau produktų.
- **Nuolaida prekių rinkiniui** – nuolaida, suteikiama perkant tam tikrą produktų derinį.
- **Ribinė nuolaida** – nuolaida, taikoma, kai operacijos bendroji suma yra didesnė nei nurodyta suma.

Tiek kainų korekcijas, tiek nuolaidas galima susieti su kainų grupėmis. Kainų grupės gali būti susietos su kanalais, katalogais, priskyrimais ir lojalumo programomis.

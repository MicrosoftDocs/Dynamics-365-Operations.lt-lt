---
title: Kainų koregavimas ir nuolaidos
description: Šiame straipsnyje pateikiama informacija apie kainų koregavimus ir nuolaidas „Dynamics 365 Commerce“.
author: scott-tucker
ms.date: 06/11/2021
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
ms.openlocfilehash: 96a695df250cda514b7bd8b9716c0f03fb2bfd28d3af4daedaf1335c3099fbb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748503"
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

> [!NOTE]
> Nuolaidos prekių nuolaidai ir ribinei vertei taikomos ypatybės, kurių pavadinimai Skaičiuoti produktus, kuriems nuolaida nėra taikoma" ir „Skaičiuoti produktus, kuriems nuolaida nėra taikoma, kaip ribinė reikšmė". Jei šios ypatybės įgalintos, prekė, kuri neturi teisės į jokias nuolaidas, vis tiek gali padėti nustatyti nuolaidos operaciją, bet netinkama prekė negaus nuolaidos. 
> 
> Pavyzdžiui, jei sukuriate nuolaidą prekių maišai su dviem eilutėmis A ir B, kur klientui 10% nuolaida turi būti atjungta, o A prekės konfigūracija pažymėta Kaip Neleisti visų nuolaidų, tai paprastai reiškia, kad A prekė neįtraukiama į nuolaidą. Tačiau, jei įgalinta ypatybė Skaičiuoti produktus, kuriems netaikoma nuolaida, prekę A galima naudoti norint pritaikyti nuolaidą prekių prekių nuolaidai, tačiau 10% nuolaida bus taikoma tik prekei B. Panaši logika taikoma ribinei nuolaidai. 
>
> Tačiau ypatybė „Skaičiuoti produktus, kuriems taikoma nuolaida siekiant slenkstį“, turi papildomą galimybę, kai ji lyginama su nuolaidų prekių nuolaidai taikoma ypatybė Skaičiuoti produktus, kuriems nuolaida nėra taikoma. Jei įgalinta ribinė nuolaida ir jei yra prekė, kuriai taikoma esama nuolaida, kuri apsaugotų nuo bet kokių kitų nuolaidų, už šią prekę sumokėta kaina atitiktų ribinę vertę, tačiau ši prekė negaus papildomos nuolaidos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

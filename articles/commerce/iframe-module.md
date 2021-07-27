---
title: „Iframe“ modulis
description: Šis skyrius aprašo „iframe“ modulį ir tai, kaip įtraukti jį į vietos puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 55526b34eb057abb9a8c33cbfea1807601da6577
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348219"
---
# <a name="iframe-module"></a>„Iframe“ modulis

[!include [banner](includes/banner.md)]

Šis skyrius aprašo „iframe“ modulį ir tai, kaip įtraukti jį į vietos puslapius „Microsoft Dynamics 365 Commerce“.

„iframe“ modulis suteikia „iframe“ (rėmelį pagal liniją), kuris apima išorės turinį svetainėje. Pavyzdžiui, jis gali būti naudojamas „YouTube“ vaizdo įrašo ar PDF failo peržiūros patalpinimui bet kuriame svetainės puslapyje. 

„iframe“ modulis reikalauja galutinio URL. Tuomet jis patalpina galutinio puslapio turinį HTML **„iframe“** elemente. Išorės URL turi būti leidžiamųjų sąraše vietos turinio saugumo politikos (CSP) direktyvoms. URL, skirti „iframe“ turiniui, turi būti leidžiami naudojant **rėmelio protėvio** gairę. - Norėdami gauti daugiau informacijos, žr. [turinio saugumo politikos valdymas (CSP)](manage-csp.md).

> [!NOTE]
> „iframe“ modulį galima naudoti „Dynamics 365 Commerce“ 10.0.13 leidime.

Toliau pateiktas paveikslėlis rodo „iframe“ modulių pavyzdžius, kurie iliustruoja išorės vaizdo įrašus svetainės puslapiuose.

![„iframe“ modulio pavyzdys rodo išorinius vaizdo įrašus.](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>„iframe“ modulio ypatybės

| Ypatybės pavadinimas             | Reikšmė                 | Aprašas |
|---------------------------|-----------------------|-------------|
| Antraštė | Tekstas | Modulio antraštė. |
| Paskirties URL | URL | URL, kuris yra patalpintas modulyje. |
| Aukštis | Procentų skaičius | Modulio aukštis pikseliais arba procentais. Pavyzdžiui,**100** vertė bus laikoma pikselių numeriais, o vertė **100%** traktuojama kaip procentai. |
| ARIA žyma | Tekstas | Prieinamų praturtinto interneto programų (ARIA) etiketės gali būti nustatytas prieinamumo tikslais. |

## <a name="add-an-iframe-module-to-a-page"></a>Įtraukti „iframe“ modulį į puslapį

Siekiant įtraukti „iframe“ modulį į puslapį ir parodyti išorinį vaizdo įrašą, atlikite šiuos žingsnius.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. **Naujo šablono** teksto laukelyje, skyriuje **Šablono pavadinimas** įveskite **Komercijos šablono** ir tuomet pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. **Pasirinkite šabloną** teksto laukelyje, pasirinkite **Komercijos šablono** šabloną. Skyriuje **Puslapio pavadinimas**, įveskite **Komercijos puslapis** ir tuomet pasirinkite **Gerai**.
1. Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.
1. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.
1. Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. **Modulio įtraukimo** teksto laukelyje pasirinkite **„iframe“** modulį ir tuomet pasirinkite **Gerai**.
1. Modulio ypatybių juostoje, nustatykite **Galutinis URL** vertę išorės URL vaizdo įrašui.
1. Nustatykite kitas ypatybes, tokias kaip **Antraštė** ir **Aukštis**, kaip norite.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į komercijos puslapį savo svetainėje. Turėtumėte matyti, kad vaizdo įrašas yra sukurtas „iframe“ modulyje.
 
## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Turinio saugos strategijos (CSP) tvarkymas](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
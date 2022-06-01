---
title: „Iframe“ modulis
description: Šis skyrius aprašo „iframe“ modulį ir tai, kaip įtraukti jį į vietos puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: eeb9d76367be6b2d2153578f6358594b807382ac
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780239"
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
1. Dialogo lange **Naujas šablonas**, po Šablono **pavadinimu**, įveskite **Rinkodaros šabloną** ir pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Kurti naują puslapį**, po Puslapio **pavadinimas**, įveskite Rinkodaros **puslapį** ir pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti šabloną pasirinkite** rinkodaros šabloną **, kurį sukūrėte**, tada pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti maketą** pasirinkite puslapio maketą (pvz., Lankstusis **maketas**) ir pasirinkite **Pirmyn**.
1. Dalyje **Peržiūrėti ir baigti** peržiūrėkite puslapio konfigūraciją. Jei reikia redaguoti puslapio informaciją, pasirinkite **Atgal**. Jei puslapio informacija teisinga, pasirinkite Kurti **puslapį**. 
1. Naujo puslapio **pagrindiniame** atrinkinyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite iframe **modulį** ir pasirinkite **Gerai**.
1. Modulio ypatybių juostoje, nustatykite **Galutinis URL** vertę išorės URL vaizdo įrašui.
1. Nustatykite kitas ypatybes, tokias kaip **Antraštė** ir **Aukštis**, kaip norite.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į komercijos puslapį savo svetainėje. Turėtumėte matyti, kad vaizdo įrašas yra sukurtas „iframe“ modulyje.

> [!NOTE]
> Kadangi iframe modulis nuomoja išorinį turinį, svetainės autoriai turi užtikrinti, kad iframe modulyje laikomas turinys nepažeidžia turinio apribojimo strategijų atitinkamoje rinkoje. Jei puslapyje, kuris naudoja iframe modulį, yra turinio pažeidimas, svetainės autorius gali pašalinti iframe modulį atidarydamas puslapį svetainės generatoriuje, **pasirinkdamas** Pašalinti modulį iframe modulio laiko atminties dalyje ir įrašęs bei paskelbdamas puslapį iš naujo.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Turinio saugos strategijos (CSP) tvarkymas](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

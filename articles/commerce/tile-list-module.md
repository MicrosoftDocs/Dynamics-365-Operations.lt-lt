---
title: Plytelių sąrašo modulis
description: Šioje temoje aprašomi plytelių sąrašo moduliai ir tai, kaip juos įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dd714f29fe2f9acd459be7bda1c0bfac65b72cb0
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780798"
---
# <a name="tile-list-module"></a>Plytelių sąrašo modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi plytelių sąrašo moduliai ir tai, kaip juos įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

Plytelių sąrašo modulis yra plytelių rinkinys karuselėje. Jis naudojamas produktų kategorijų arba prekės ženklų rinkodarai naudojant vaizdus ir tekstą. Pavyzdžiui, mažmeninis prekybininkas gali įtraukti plytelių sąrašo modulį į pagrindinį elektroninės prekybos svetainės puslapį, kad pareklamuotų geriausiai parduodančias kategorijas.

Plytelių sąrašo modulis grindžiamas duomenimis iš turinio valdymo sistemos (TVS). Jis nepriklauso nuo jokių kitų „Commerce” būstinės modulių ar duomenų. Plytelių sąrašo modulį galima įtraukti į bet kurį svetainės puslapį, kuriame pardavėjas nori kažką parduoti ar reklamuoti, (pavyzdžiui, produktus, kategorijas ar prekės ženklus).

Šioje iliustracijoje pateikiamas plytelių sąrašo modulio ir plytelių modulių pavyzdys „Adventure Works” pagrindiniame puslapyje.

![Plytelių sąrašo modulio ir plytelių modulių pavyzdys „Adventure Works” pagrindiniame puslapyje](./media/Tile_list.PNG)

> [!IMPORTANT]
> Plytelių sąrašo modulis yra prieinamas 10.0.20 „Dynamics 365 Commerce” versijos leidime.
> Plytelių sąrašo modulis rodomas „Adventure Works” temoje.

## <a name="tile-list-modules-and-themes"></a>Plytelių sąrašo moduliai ir temos

Plytelių sąrašo modulis gali palaikyti įvairius maketus ir stilius, pagrįstus tema. Pavyzdžiui, „Adventure Works” temoje plytelės rodo animacijos efektą, kai svetainės vartotojai jas pažymi pele. Kiekvienoje temoje gali būti papildomos plytelių sąrašo ir plytelių modulių ypatybės. Temų kūrėjai taip pat gali kurti papildomus maketus plytelių sąrašui ir plytelių moduliams.

## <a name="tile-list-module-properties"></a>Plytelių sąrašo modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Antraštė       | Antraštės tekstas ir antraštės žymė | Plytelės sąrašo modulio teksto antraštė. |

## <a name="tile-module-properties"></a>Plytelės modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Nuotrauka         | Vaizdo failas | Parodyti produktą ar kategoriją galima naudojant vaizdą. Vaizdą galima įkelti į „Commerce” svetainės generatoriaus medijos biblioteką arba naudoti esamą vaizdą. |
| Antraštė       | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Numatyta, kad naudojama antraštės žymė **„H2”**, tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Pastraipa     | Pastraipos tekstas | Modulis palaiko pastraipos tekstą raiškiojo teksto formatu. Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pavyzdžiui, hipersaitai, paryškintasis, pabrauktasis ir pasvirasis tekstas. Kai kurias iš šių galimybių gali perrašyti moduliui pritaikoma puslapio tema. |
| Saitas          | Saito tekstas, saito URL, „Accessible Rich Internet Applications“ (ARIA) žyma ir **Saitą atidaryti naujame skirtuke** | Moduliai palaiko vieną ar kelis raginimo imtis veiksmų saitus. Jei įtraukiamas saitas, reikalingas saito tekstas, URL ir ARIA žyma. ARIA žymos turi būti aprašomosios, jog atitiktų pritaikymo neįgaliesiems reikalavimus. Saitus galima konfigūruoti taip, kad jie būtų atidaromi naujame skirtuke. |
| Plytelės saitas     | Saito tekstas, saito URL, ARIA žyma ir **Saitą atidaryti naujame skirtuke** parinkiklis | Ši ypatybė naudojama apibrėžti saitui „iškviesti veiksmą”. Jei įtraukiamas saitas, reikalingas saito tekstas, URL ir ARIA žyma. ARIA žymos turi būti aprašomosios, jog atitiktų pritaikymo neįgaliesiems reikalavimus. Saitus galima konfigūruoti taip, kad jie būtų atidaromi naujame skirtuke.|
| Piktograma          | Nuotrauka | Be produkto ar kategorijos vaizdo, galima pridėti piktogramos simbolį. Piktogramos simbolis bus rodomas virš produkto ar kategorijos vaizdo. |

## <a name="add-a-tile-list-module-to-a-new-page"></a>Plytelių sąrašo modulio įtraukimas į naują puslapį

Norėdami į naują puslapį įtraukti plytelių sąrašo modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai** ir atidarykite jūsų svetainės pagrindinio puslapio rinkodaros šabloną (arba sukurkite naują rinkodaros šabloną).
1. Numatytojo **puslapio** pagrindiniame atrinkinyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite išklotinės dalies **sąrašo** modulį, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir atidarykite pagrindinį svetainės puslapį (arba sukurkite naują pagrindinį puslapį naudodami rinkodaros šabloną).
1. Numatytojo **puslapio** pagrindiniame atrinkinyje pasirinkite elipsės mygtuką (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite išklotinės dalies **sąrašo** modulį, tada pasirinkite **Gerai**.
1. Plytelių sąrašo modulio ypatybių srityje įtraukite antraštę.
1. Išklotinės **dalies sąrašo** atminties sąraše pasirinkite elipsės mygtuką (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite modulį Išklotinė **vieta**, tada pasirinkite **Gerai**.
1. Plytelės modulio ypatybių srityje įtraukite vaizdą, antraštę ir piktogramos simbolio vaizdą.
1. Jei reikia, įtraukite ir sukonfigūruokite papildomus plytelės modulius.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[„Adventure Works” tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

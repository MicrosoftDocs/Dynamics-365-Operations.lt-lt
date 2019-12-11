---
title: Puslapio modelio žodynas
description: Šioje temoje aprašomi įvairūs elementai, naudojami „Microsoft Dynamics 365 Commerce“ svetainės puslapiuose.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
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
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c7b79e8b3bd68ba6246fe24916c60f476a26605
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697962"
---
# <a name="page-model-glossary"></a>Puslapio modelio žodynas

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi įvairūs elementai, naudojami „Microsoft Dynamics 365 Commerce“ svetainės puslapiuose.

## <a name="page-element-definitions"></a>Puslapio elementų aprašai

Toliau pateikiamoje lentelėje pateikiama terminų, kuriuos reikia žinoti, kai keičiate savo svetainės išvaizdą, įspūdį ir turinį, suvestinė. Norėdami daugiau sužinoti apie paaiškinimus ir procedūras, atidarykite šiuos saitus.

| Semestras | Aprašas ir pastabos |
|------|-----------------------|
| [Modulis](work-with-modules.md) | <p>**Aprašas:** moduliai yra kūrimo blokas, kuris gali būti sukurtas ir sudaryti tinklalapio griaučius. Pavyzdžiai apima antraštės, pagrindinės reklaminės juostos ir karuselės modulius.</p><p>**Kur jis pasirinktas:** diegti modulius galima parinkti ir konfigūruoti įvairiuose svetainės kūrimo darbo eigos etapuose, pvz., šablono, maketo, puslapio ir fragmento kūrimo etapuose.</p><p>**Kur jis redaguojamas:** naudojant programinės įrangos kūrimo rinkinį (SDK), kode sukuriami tinkinti moduliai. Tada jie nusiunčiami į jūsų svetainę, kur tampa pasirinktini.</p> |
| Modulio ypatybė | <p>**Aprašas:** modulio ypatybės yra konkretūs parametrai, kurie apibrėžiami modulyje. Juos galima redaguoti el. prekybos kūrimo įrankiuose. Pavyzdžiui, modulio ypatybės naudojamos norint nustatyti reklamjuostės modulio antraštę ir fono vaizdą.</p><p>**Kur jis sukonfigūruotas:** modulio ypatybės yra pasirenkamos ir sukonfigūruotos ypatybių srityje, kuri rodoma šablonų, maketų, puslapių, fragmentų ir programos parametrų kūrimo aplinkose (rengyklėse).</p> |
| [Šablonas](templates-layouts-overview.md) | <p>**Aprašas:** šablonai apibrėžia modulių derinius ir parinktis, naudojamus puslapių kategorijai (pavyzdžiui, rinkodaros puslapių, kategorijos puslapių ir produktų puslapių).</p><p>**Kur jis buvo pasirinktas:** šablonai gali būti pasirenkami puslapio arba maketo kūrimo darbo eigoje.</p><p>**Kur jis redaguojamas:** šablonų rengyklėje yra kuriami šablonai. Jiems sukurti ar modifikuoti nereikia jokio kodo.</p> |
| [Maketas](templates-layouts-overview.md) | <p>**Aprašas:** maketai apibrėžia galutinį modulių pasirinkimą ir išdėstymą iš pirminio šablono parinkčių rinkinio. Gali būti sukonfigūruotas vieno puslapio maketas (*tinkintas maketas*) arba jį gali naudoti keli puslapiai (*iš anksto nustatytas maketas*).</p><p>**Kur jis yra pasirinktas:** maketai gali būti pasirenkami kuriant naują puslapį arba, kai yra reikalingas kitoks maketas esamame puslapyje.</p><p>**Kur jis redaguojamas:** maketų rengyklėje yra kuriami maketai. Jiems sukurti ar modifikuoti nereikia jokio kodo.</p> |
| Puslapio egzempliorius | <p>**Aprašas:** puslapio egzemplioriai nustato galutinį puslapio konkretų lokalizuotą turinį viename puslapyje. Šis turinys išvedamas iš modulio ypatybių reikšmių.</p><p>**Kur jis buvo pasirinktas:** puslapiai pasirenkami, kai priskiriami URL.</p><p>**Kur jis redaguojamas:** puslapių rengyklėje yra kuriami puslapiai. Jiems sukurti ar modifikuoti nereikia jokio kodo.</p> |
| [Tema](select-site-theme.md) | <p>**Aprašas:** temos apibrėžia pakopinio stiliaus aprašą (CSS) ir nustato puslapyje teikiamų modulių apipavidalinimą.</p><p>**Kur jis pasirinktas:** kai tema įkeliama į jūsų svetainę naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS), ją galima rinktis kaip puslapio konteinerio modulio ypatybę.</p><p>**Kur jis redaguojamas:** temos šiuo metu sukuriamos ir redaguojamos naudojant SDK. Tada jos įkeliamos į jūsų svetainę naudojant LCS.</p> |
| [Fragmentas](work-with-fragments.md) | <p>**Aprašas:** fragmentai yra visiškai sukonfigūruoti moduliai, kuriuose yra lokalizuotas turinys, kuris gali būti pakartotinai panaudotas ir centralizuotai atnaujintas keliuose puslapiuose. Pavyzdžiui, fragmentas, sukurtas naudojant antraštės modulį, gali būti naudojamas visuose jūsų svtainės šablonuose ir visuose puslapiuose ir centralizuotai atnaujintas vienoje vietoje.</p><p>**Kur jis buvo pasirinktas:** fragmentai gali būti parenkami bet kur, kur galima pasirinkti modulius. Galima pakeisti modulį į juos, siekiant padidinti efektyvumą ir naudojant daugkartinio naudojimo ir centralizuotą kūrimą.</p><p>**Kur jis redaguojamas:** fragmentų rengyklėje yra kuriami fragmentai. Jiems sukurti ar modifikuoti nereikia jokio kodo.</p> |
| URL | <p>**Aprašas:** vieningieji išteklių adresai (URL) yra adresai, nukreipti į tinklalapius ir kitus URL.</p><p>**Kur jis buvo pasirinktas:** URL pasirenkami bet kur, kur reikia saitų su puslapiais.</p><p>**Kur jis redaguojamas:** URL rengyklėje yra kuriami URL. Jiems sukurti ar modifikuoti nereikia jokio kodo.</p> |
| Ilgalaikio turto | <p>**Aprašas:** ištekliai yra failų dvejetainiai failai, kurių plėtinys yra .jpg, .docx, .pdf arba .mpg.</p><p>**Kur jis buvo pasirinktas:** ištekliai pasirenkami kaip modulių ypatybės, kurių reikia moduliams.</p><p>**Kur jis redaguojamas:** ištekliai nusiunčiami, o susiję metaduomenys redaguojami išteklių tvarkytuvėje.</p> |

## <a name="additional-resources"></a>Papildomi ištekliai

[Turinio įtraukimo būdai](add-manage-content.md)

[Dokumentų būsenos ir vykdymo ciklas](document-states-overview.md)

[Darbas su moduliais](work-with-modules.md)

[Darbas su fragmentais](work-with-fragments.md)

[Šablonų ir maketų apžvalga](templates-layouts-overview.md)

[Svetainės naršymo tinkinimas](customize-site-navigation.md)

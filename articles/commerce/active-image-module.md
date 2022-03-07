---
title: Aktyvaus vaizdo modulis
description: Šioje temoje aprašomi aktyvaus vaizdo moduliai ir tai, kaip juos įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 36b7d6dea87c7f309c07608794d443a0ae19be211847d2cddcad95f2d933a8db
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716913"
---
# <a name="active-image-module"></a>Aktyvaus vaizdo modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi aktyvaus vaizdo moduliai ir tai, kaip juos įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

Aktyvaus vaizdo modulis gali būti naudojamas įtraukti produkto žymėms į vaizdą. Tada elektroninės prekybos svetainės vartotojai gali užvesti pelę ant žymių, kad peržiūrėtų vaizde rodomus produktus. Peržiūros rodomos išskleidžiamuose languose. Pasirinkdami peržiūros laikinąjį langą vartotojai gali tiesiogiai eiti į atitinkamo produkto išsamios informacijos puslapį (PDP).

Žymės nustatomos naudojant X ir Y koordinates vaizde. Kiekvieną pažymėtą tašką reikia sukonfigūruoti naudojant produkto ID, kuris rodomas paveikslėlyje.

Šioje iliustracijoje pateikiamas „Adventure Works” pagrindinio puslapio peržiūros išskleidžiamojo lango pagrindinės reklaminės juostos vaizde pavyzdys.

![Peržiūros išskleidžiamojo lango pavyzdys aktyvaus vaizdo modulyje](./media/Active_image.PNG)

> [!IMPORTANT]
> - Aktyvaus vaizdo modulis yra prieinamas kaip 10.0.20 „Dynamics 365 Commerce” versijos leidimas.
> - Aktyvaus vaizdo sąrašo modulis rodomas „Adventure Works” temoje.

## <a name="active-image-module-properties"></a>Aktyvaus vaizdo modulio ypatybės

| Ypatybės pavadinimas      | Reikšmės | Aprašas |
|--------------------|--------|-------------|
| Nuotrauka              | Vaizdo failas | Parodyti vieną ar daugiau produktų galima naudojant vaizdą. Vaizdą galima įkelti į „Commerce” svetainės generatoriaus medijos biblioteką arba naudoti esamą vaizdą. |
| Plotis              | Pikselių skaičius | Ši ypatybė nurodo vaizdo plotį. Aktyvios koordinatės yra skaičiuojamos pagal paveikslėlio plotį.|
| Aktyvios koordinatės | X ir Y koordinatės, bei produkto ID numeris | Kiekvieną aktyvaus vaizdo masyvą sudaro X ir Y koordinatės, bei produkto ID numeris.|
| Antraštė            | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Numatyta, kad naudojama antraštės žymė **„H2”**, tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Pastraipa          | Pastraipos tekstas | Modulis palaiko pastraipos tekstą raiškiojo teksto formatu. Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pavyzdžiui, hipersaitai, paryškintasis, pabrauktasis ir pasvirasis tekstas. Kai kurias iš šių galimybių gali perrašyti moduliui pritaikoma puslapio tema. |
| Saitas               | Saito tekstas, saito URL, „Accessible Rich Internet Applications“ (ARIA) žyma ir **Saitą atidaryti naujame skirtuke** parinkiklis | Modulis palaiko vieną ar kelis raginimo imtis veiksmų saitus. Jei įtraukiamas saitas, reikalingas saito tekstas, URL ir ARIA žyma. ARIA žymos turi būti aprašomosios, jog atitiktų pritaikymo neįgaliesiems reikalavimus. Saitus galima konfigūruoti taip, kad jie būtų atidaromi naujame skirtuke. |
| Papildomas tekstas           | Antraštės, tekstas ir saitai | Gali būti pridėtas papildomas vaizdo kontekstas, pavyzdžiui, autoriaus ar dizainerio vardas arba saitai į asmeninį tinklaraštį.|
| Teksto tema         | **Šviesi** arba **Tamsi** | Ši ypatybė leidžia vartotojui nustatyti tekstą šviesų arba tamsų pagal fono paveikslėlį. Ji galima kaip temos plėtinys „Adventure Works” temoje. |

## <a name="add-an-active-image-module-to-a-new-page"></a>Aktyvaus vaizdo modulio įtraukimas į naują puslapį

Norėdami pridėti aktyvaus vaizdo modulį naujame puslapyje ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai** ir atidarykite jūsų svetainės pagrindinio puslapio rinkodaros šabloną (arba sukurkite naują rinkodaros šabloną).
1. Nustatytojo puslapio **Pagrindinis** vietoje pasirinkite elipsę (**...**), ir tuomet pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Aktyvus vaizdas**, o tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir atidarykite pagrindinį svetainės puslapį (arba sukurkite naują pagrindinį puslapį naudodami rinkodaros šabloną).
1. Numatytojo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Aktyvus vaizdas**, o tada pasirinkite **Gerai**.
1. Aktyvaus vaizdo modulio ypatybių srityje pridėkite paveikslėlį ir nustatykite drobės plotį kaip vaizdo dydį.
1. Nustatykite X ir Y koordinates, bei pridėkite atitinkamą produkto ID numerį.
1. Jei reikia, įtraukite ir sukonfigūruokite papildomus aktyvaus vaizdo modulius.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[„Adventure Works” tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

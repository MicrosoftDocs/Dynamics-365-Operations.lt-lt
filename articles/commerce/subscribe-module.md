---
title: Prenumeravimo modulis
description: Šioje temoje aprašomi prenumeravimo moduliai ir tai, kaip juos įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: efc9150ea5ddeb7051f82fb07c4d566ac8a48dfa
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780594"
---
# <a name="subscribe-module"></a>Prenumeravimo modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi prenumeravimo moduliai ir tai, kaip juos įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

Prenumeravimo moduliai gali būti naudojami svetainės puslapiuose, kad būtų galima fiksuoti klientų informaciją naujienlaiškiams ar akcijoms.

Šioje iliustracijoje pateikiamas prenumeravimo modulio pavyzdys „Adventure Works” svetainės puslapio poraštėje.

![Prenumeravimo modulio pavyzdys „Adventure Works” svetainės puslapio poraštėje](./media/Subscribe.PNG)

> [!IMPORTANT]
> - Prenumeravimo modulis galimas „Commerce” modulių bibliotekoje kaip 10.0.20 „Dynamics 365 Commerce” versijos dalis.
> - Prenumeravimo modulis rodomas „Adventure Works” temoje.
> - Prenumeravimo moduliui reikia duomenų veiksmo plėtinio, kad būtų galima dirbti su kai kuriais rinkodaros el. pašto teikėjais, kad naujienlaiškiai ar reklaminiai el. laiškai būtų siunčiami užfiksavus kliento informaciją.

## <a name="subscribe-module-properties"></a>Prenumeravimo modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Antraštė       | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Prenumeravimo modulio teksto antraštė pavyzdžiui, **Prenumeruoti naujienlaiškį** arba **Registruotis 10% nuolaidai**. |
| Pastraipa     | Pastraipos tekstas | Prenumeravimo modulis palaiko paragrafo tekstą raiškiojo teksto formatu, kad pateiktų papildomos informacijos apie veiksmą antraštėje. |

## <a name="add-a-subscribe-module-to-a-new-page"></a>Prenumeravimo modulio įtraukimas į naują puslapį

Norėdami į naują puslapį įtraukti prenumeravimo sąrašo modulį ir nustatyti reikiamas ypatybes „Commerce” svetainių daryklėje, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai** ir atidarykite jūsų svetainės pagrindinio puslapio rinkodaros šabloną (arba sukurkite naują rinkodaros šabloną).
1. Numatytojo **puslapio** pagrindiniame atrinkinyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite modulį **Prenumeruoti**, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir atidarykite pagrindinį svetainės puslapį (arba sukurkite naują pagrindinį puslapį naudodami rinkodaros šabloną).
1. Numatytojo **puslapio** pagrindiniame atrinkinyje pasirinkite elipsės mygtuką (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite modulį **Prenumeruoti**, tada pasirinkite **Gerai**.
1. Prenumeravimo modulio ypatybių srityje pridėkite antraštę, pavyzdžiui, **Prenumeruoti**.
1. Įtraukite paragrafo tekstą, pavyzdžiui, **Naujausios tendencijos, stiliai ir akcijos. Ar jūs sąraše? Prenumeruokite ir gaukite naujausius karštus pasiūlymus!**
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[„Adventure Works” tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

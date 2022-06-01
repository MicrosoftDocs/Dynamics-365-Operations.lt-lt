---
title: Skirtuko modulis
description: Šioje temoje aprašomi skirtuko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: 104fb57cfdcd96a0da50899c0eac576074282017
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780619"
---
# <a name="tab-module"></a>Skirtuko modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi skirtuko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

Skirtuko moduliai yra talpyklas primenantys moduliai, naudojami siekiant surūšiuoti svetainės puslapyje esančią informaciją į skirtukus. Jie gali būti naudojami bet kuriame puslapyje, kuriame informacija turi būti pateikta skirtukuose.

Kiekviename skirtuko modulyje galima įtraukti vieną ar daugiau skirtuko modulių. Kiekvienas skirtuko elementų modulis yra vienas skirtukas. Į kiekvieną skirtuko elementų modulį galima įtraukti vieną arba daugiau modulių. Modulių, kuriuos galima įtraukti į skirtuko elementų modulį, tipų apribojimų nėra.

Toliau pateiktame paveikslėlyje parodytas svetainės puslapyje esančio skirtuko modulio pavyzdys. Šiame pavyzdyje pasirinktas skirtukas **Siuntimas**.

![Skirtuko modulio pavyzdys.](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Skirtuko modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Antraštė | Tekstas | Ši ypatybė nurodo pasirinktinę skirtuko modulio teksto antraštę. |
| Aktyvaus skirtuko indeksas | Skaičius | Ši ypatybė nurodo skirtuką, kuris pagal numatytuosius parametrus turi būti suaktyvintas, kai puslapis įkeliamas. Jei nenurodyta jokia vertė, pagal numatytuosius parametrus suaktyvinamas pirmas skirtuko elementas. |

## <a name="tab-item-module-properties"></a>Skirtuko elementų modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | aprašymas |
|---------------|--------|-------------|
| Kreipinys | Tekstas | Ši ypatybė nurodo skirtuko elementų modulio pavadinimo tekstą. |

## <a name="add-a-tab-module-to-a-page"></a>Skirtuko modulio įtraukimas į puslapį

Norėdami į puslapį įtraukti skirtuko modulį ir nustatyti ypatybes, atlikite tolesnius veiksmus.

1. Naudodami „Fabrikam“ rinkodaros šabloną (ar bet kokį kitą šabloną be apribojimų) sukurkite naują puslapį su pavadinimu **Parduotuvės strategijos puslapis**.
1. Numatytojo **puslapio** pagrindiniame atrinkinyje **pasirinkite** daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite modulį **Skirtukas**, tada pasirinkite **Gerai**.
1. Skirtuko modulio ypatybių srityje, šalia pieštuko simbolio, pasirinkite **Antraštė**.
1. Dialogo lange **Antraštė**, dalyje **Antraštės tekstas**, įveskite antraštės tekstą (pavyzdžiui, **Strategija**). Tada pasirinkite **Gerai**.
1. Tabuliacijos **atminties** atminties lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite prekių **modulį** Skirtukas, tada pasirinkite **Gerai**.
1. Skirtuko elementų modulio ypatybių srityje, dalyje **Pavadinimas**, įveskite pavadinimo tekstą (pavyzdžiui, **Pristatymas**).
1. Skirtuke **prekės atminties** laiko atminties pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite modulį **Teksto blokas**, tada – **Gerai**.
1. Teksto bloko modulio ypatybių srityje, dalyje **Raiškusis tekstas**, įveskite teksto pastraipą.
1. Vietoje **Skirtukas** įtraukite dar kelis skirtuko elementų modulius su pavadinimais. Kiekviename skirtuko elementų modulyje pridėkite tekstinio bloko modulį, kuriame yra turinio.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Puslapyje bus rodomas skirtuko modulis, kuriame yra skirtuko elementų modulių su jūsų įtrauktu turiniu.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Akordeono modulis](add-accordion.md)

[Teksto bloko modulis](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

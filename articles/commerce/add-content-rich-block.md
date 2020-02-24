---
title: Teksto bloko modulis
description: Šioje temoje aprašomi teksto bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025602"
---
# <a name="text-block-module"></a>Teksto bloko modulis


[!include [banner](includes/banner.md)]

Šioje temoje aprašomi teksto bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Teksto bloko modulis yra modulis, kuris naudojamas teksto turiniui pridėti. Šis turinys gali būti informacinis arba reklaminis.

Teksto bloko moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje. Jie yra atskiri moduliai, nepriklausantys nuo puslapio konteksto ar kitų modulių.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Teksto bloko modulių pavyzdžiai el. prekyboje

Teksto bloko modulius galima naudoti toliau nurodytais būdais.

* Norint produktų išsamios informacijos puslapyje parodyti produktų ypatybes.
* Informaciniais tikslais bet kuriame puslapyje. Pavyzdžiui, juos naudojant galima paaiškinti lojalumo programų privalumus, aprašyti siuntimo ir grąžinimo strategijas, atsakyti į dažnai užduodamus klausimus arba pateikti turinio „apie mus“.
* Norint produktų išsamios informacijos puslapyje įtraukti pasirinktinių pranešimų. (Pavyzdžiui, „Didesni, nei 50 USD, užsakymai pristatomi nemokamai“).
* Norint produktų išsamios informacijos puslapiuose, krepšelio puslapiuose, pirkimo užbaigimo puslapiuose ir kituose puslapiuose įtraukti informaciją apie atsakomės atsisakymą ir kontaktinę informaciją (pavyzdžiui, „Siunčiant ir grąžinant prekes taikomos parduotuvės strategijos“).

## <a name="text-block-module-properties"></a>Teksto bloko modulio ypatybės

| Ypatybės pavadinimas     | Value                                            | Aprašymas |
|-------------------|--------------------------------------------------|-------------|
| Raiškusis tekstas         | Raiškusis tekstas                                        | Pastraipos tekstas. Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas. |
| Pasirinktinis klasės pavadinimas | Pakopinio stiliaus aprašų (CSS) klasės pavadinimas        | Pasirinktinės CSS klasės, kurią kūrėjas teikia formatuoti šį modulį, pavadinimas. Klasės pavadinimas turi būti nurodytas temų pakete. |
| Šrifto dydis         | **Mažas**, **Vidutinis**, **Didelis** arba **X dydžio** | Turinio šrifto dydis. |

## <a name="add-a-text-block-module-to-a-page"></a>Teksto bloko modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti teksto bloko modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Sukurkite puslapio šabloną, pavadintą **Turinio šablonas**. 
1. Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis modulis**.
1. Baikite šablono redagavimą ir publikuokite.
1. Naudodami ką tik sukurtą turinio šabloną, sukurkite puslapį, pavadintą **Turinio puslapis**.
1. Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.
1. Konteinerio modulio ypatybių srityje nustatykite ypatybę **Plotis** į **Užpildyti konteinerį**.
1. Į konteinerio modulį įtraukite teksto bloko modulį. 
1. Teksto bloko modulio ypatybių srityje įtraukite tekstą į lauką **Raiškusis tekstas**.
1. Baikite puslapio redagavimą ir publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Reklaminės juostos modulis](add-alert.md)

[Karuselės modulis](add-carousel.md)

[Turinio bloko modulis](add-hero-module.md)

[Vaizdo įrašų leistuvo modulis](add-video-player.md)


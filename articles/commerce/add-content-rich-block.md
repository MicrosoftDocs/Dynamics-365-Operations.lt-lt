---
title: Raiškiojo turinio bloko modulis
description: Šioje temoje aprašomi raiškiojo turinio bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785426"
---
# <a name="content-rich-block-module"></a>Raiškiojo turinio bloko modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi raiškiojo turinio bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Raiškiojo turinio bloko modulis yra specialus konteineris, į kurį galima įdėti vieną ar kelis raiškiojo turinio bloko elementus. Raiškiojo turinio bloko moduliai naudojami tekstiniam puslapio turiniui. Šis turinys gali būti informacinis arba reklaminis.

Raiškiojo turinio bloko elementų moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje. Jie yra atskiri moduliai, nepriklausantys nuo puslapio konteksto ar kitų modulių.

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>Raiškiojo turinio bloko modulių pavyzdžiai el. prekyboje

Raiškiojo turinio bloko modulius galima naudoti toliau nurodytais būdais.

* Norint produktų išsamios informacijos puslapyje parodyti produktų ypatybes.
* Informaciniais tikslais bet kuriame puslapyje. Pavyzdžiui, juos naudojant galima paaiškinti lojalumo programų privalumus, aprašyti siuntimo ir grąžinimo strategijas, atsakyti į dažnai užduodamus klausimus arba pateikti turinio „apie mus“.
* Norint produktų išsamios informacijos puslapyje įtraukti pasirinktinių pranešimų. (Pavyzdžiui, „Didesni, nei 50 USD, užsakymai pristatomi nemokamai“).
* Norint produktų išsamios informacijos puslapiuose, krepšelio puslapiuose, pirkimo užbaigimo puslapiuose ir kituose puslapiuose įtraukti informaciją apie atsakomės atsisakymą ir kontaktinę informaciją (pavyzdžiui, „Siunčiant ir grąžinant prekes taikomos parduotuvės strategijos“).

## <a name="content-rich-block-module-properties"></a>Raiškiojo turinio bloko modulių ypatybės

| Ypatybės pavadinimas     | Vertė                                 | Ypatybė |
|-------------------|---------------------------------------|----------|
| Stulpelių skaičius | Skaičius nuo **1** iki **4**     | Raiškiojo turinio bloko stulpelių skaičius. Gali būti iki keturių stulpelių. |
| Plotis             | **Užpildyti konteinerį** arba **Užpildyti ekraną** | Jei reikšmė nustatoma kaip **Užpildyti konteinerį**, konteinerio elementų plotį riboja konteineris. Jei reikšmė nustatoma kaip **Užpildyti ekraną**, elementų pločio konteineris neriboja ir juos galima vaizduoti viso ekrano režimu. Keisdami reikšmę, galite pasiekti norimą išdėstymą. |

## <a name="content-rich-block-item-module-properties"></a>Raiškiojo turinio bloko elementų modulių ypatybės

| Ypatybės pavadinimas | Vertė          | Aprašymas |
|---------------|----------------|-------------|
| Pastraipa     | Pastraipos tekstas | Tekstas, pridedamas prie kiekvieno raiškiojo turinio bloko elemento. Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas. |

## <a name="add-a-content-rich-block-module-to-a-page"></a>Raiškiojo turinio bloko modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti raiškiojo turinio bloko modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Sukurkite puslapio šabloną, pavadintą **Turinio šablonas**.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite raiškiojo turinio bloko modulį.
1. Šabloną įrašykite ir atrakinkite bei publikuokite.
1. Naudodami ką tik sukurtą turinio šabloną, sukurkite puslapį, pavadintą **Turinio puslapis**.
1. Naujo puslapio vietoje **Pagrindinis** įtraukite raiškiojo turinio bloko modulį.
1. Raiškiojo turinio bloko modulio ypatybėse stulpelių skaičių nustatykite kaip **2**.
1. Raiškiojo turinio bloko modulyje pasirinkite **Įtraukti modulį** ir įtraukite raiškiojo turinio bloko elementą (pavyzdžiui, **1elementas**).
1. Naujame raiškiojo turinio bloko elemente įtraukite pastraipos tekstą.
1. Raiškiojo turinio bloko modulyje pasirinkite **Įtraukti modulį** ir įtraukite raiškiojo turinio bloko elementą (pavyzdžiui, **2elementas**).
1. Naujame raiškiojo turinio bloko elemente įtraukite pastraipos tekstą.
1. Įrašykite puslapį ir peržiūrėkite keitimus. Turėtumėte matyti du raiškiojo teksto blokus dviejų stulpelių rodinyje.
1. Puslapį įrašykite ir atrakinkite bei publikuokite.

> [!NOTE]
> Jei įtrauksite trečią raiškiojo turinio bloko elementą, jis bus padėtas po anksčiau įtrauktais dviem elementais. Keisdami konteinerio stulpelių ir elementų skaičių, galite pasiekti skirtingus tekstinio turinio maketus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Įspėjimo modulis](add-alert.md)

[Karuselės modulis](add-carousel.md)

[Turinio išdėstymo modulis](add-content-placement-modules.md)

[Funkcijos modulis](add-feature-module.md)

[Pagrindinės reklaminės juostos modulis](add-hero-module.md)

[Vaizdo įrašų leistuvo modulis](add-video-player.md)


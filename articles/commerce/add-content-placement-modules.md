---
title: Turinio išdėstymo modulis
description: Šioje temoje aprašomi turinio išdėstymo ir turinio išdėstymo elementų moduliai bei tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785305"
---
# <a name="content-placement-module"></a>Turinio išdėstymo modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi turinio išdėstymo ir turinio išdėstymo elementų moduliai bei tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Turinio išdėstymo modulis yra specialus konteineris, į kurį kaip konkretų maketą galima įdėti kitų modulių. Turinio išdėstymo moduliai kaip antrinius modulius palaiko šių tipų modulius: turinio išdėstymo elementų, paskyros pasisveikinimo elementų, paskyros užsakymo elementų, paskyros pageidavimų sąrašo elementų ir paskyros profilio elementų.

Turinio išdėstymo moduliuose duomenys gaunami iš jų palaikomų antrinių modulių. Todėl turinio išdėstymo modulius galima naudoti įvairiai, atsižvelgiant į modulius, įtrauktus į juos.

Turinio išdėstymo elementų moduliuose naudojant tiek vaizdus, tiek tekstą rodomos akcijos, strategijos ir produktų ypatybės. Pavyzdžiui, turinio išdėstymo elementų modulį naudojant pagrindiniame puslapyje, galima rodyti parduotuvės strategijas ar siuntimo informaciją. Turinio išdėstymo elementų moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje. Tačiau juos galima naudoti tik turinio išdėstymo modulyje.

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>Turinio išdėstymo modulių pavyzdžiai el. prekyboje

* Turinio išdėstymo modulius, kuriuose yra turinio išdėstymo elementų modulių, naudojant pagrindiniame puslapyje ar rinkodaros puslapiuose, galima tiek vaizdais, tiek tekstu rodyti produktų ypatybes, parduotuvės strategijas, siuntimo informaciją ir kitą informaciją.
* Turinio išdėstymo modulius, kuriuose yra turinio išdėstymo elementų modulių, naudojant produktų išsamios informacijos puslapiuose, galima parodyti produktų ypatybes.
* Turinio išdėstymo modulius, kuriuose yra paskyros pasisveikinimo elementų arba paskyros užsakymo elementų modulių, galima naudoti paskyros valdymo puslapiuose.

## <a name="content-placement-module-properties"></a>Turinio išdėstymo modulių ypatybės

| Ypatybės pavadinimas | Vertė | Aprašymas |
|---------------|-------|-------------|
| Plotis         | **Priderinti prie konteinerio** arba **Užpildyti ekraną** | Jei reikšmė nustatoma kaip **Priderinti prie konteinerio**, turinio išdėstymo modulio elementų plotį riboja turinio išdėstymo modulis. Jei reikšmė nustatoma kaip **Užpildyti ekraną**, elementų pločio turinio išdėstymo modulis neriboja ir juos galima vaizduoti viso ekrano režimu. |

## <a name="content-placement-item-module-properties"></a>Turinio išdėstymo elementų modulių ypatybės

| Ypatybės pavadinimas | Vertė | Aprašymas |
|---------------|-------|-------------|
| Antraštė       | Antraštės tekstas ir antraštės žymės (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Antraštę gali turėti kiekvienas turinio išdėstymo elementų modulis. Ypatybė **Antraštė** palaiko antraštės žymes. Numatyta, kad naudojama antraštės žymė **H2**, tačiau antraštės žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Pastraipa     | Pastraipos tekstas | Turinio išdėstymo elementų moduliai palaiko pastraipos tekstą raiškiojo teksto formatu. Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas bei hipersaitai. Kai kurias iš šių galimybių gali perrašyti moduliui pritaikoma puslapio tema. |
| Vaizdas         | Vaizdo failas | Su tekstu galima susieti vaizdą. |
| Saitas          | Saito URL ir saito tekstas | Į tekstą galima įtraukti saitą, kad vartotojai būtų nukreipiami į konkretų puslapį. |
| Plytelės dydis     | Skaičius nuo **1** iki **12** | Ši ypatybė nustato, kiek vietų kiekvienas turinio išdėstymo elementas turi užpildyti turinio išdėstymo modulyje. Maksimalus turinio išdėstymo modulio dydis yra 12 vietų. Jei visas turinio išdėstymo modulio pirmųjų *n* elementų plytelių dydis viršija 12 vietų, elementai perkeliami į kitą eilutę. |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>Turinio išdėstymo modulio, kuriame yra turinio išdėstymo elementų modulis, įtraukimas į puslapį

Norėdami į naują puslapį įtraukti turinio išdėstymo modulį, kuriame yra turinio išdėstymo elementų modulis, ir nustatyti būtinas ypatybes, atlikite tolesnius veiksmus.

1. Sukurkite šabloną, pavadintą **turinio išdėstymo šablonas**.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite turinio išdėstymo modulį.
1. Turinio išdėstymo modulyje įtraukite turinio išdėstymo elementų modulį.
1. Šabloną įrašykite ir atrakinkite bei publikuokite.
1. Naudodami ką tik sukurtą turinio išdėstymo šabloną, sukurkite puslapį, pavadintą **Turinio išdėstymo puslapis**.
1. Naujo puslapio vietoje **Pagrindinis** įtraukite turinio išdėstymo modulį.
1. Turinio išdėstymo modulyje įtraukite turinio išdėstymo elementų modulį.
1. Turinio išdėstymo elementų modulio ypatybių srityje pasirinkite vaizdą, įtraukite antraštę, įtraukite pastraipą, įtraukite saitą, nustatykite saito URL ir plytelių dydį nustatykite kaip **6**.
1. Pakartodami 7 ir 8 veiksmus, įtraukite kitą turinio išdėstymo elementų modulį, kurio plytelių dydis yra toks pat.
1. Puslapį įrašykite ir peržiūrėkite. Turėtumėte matyti du turinio išdėstymo elementus, kurie rodomi vienas šalia kito. Norėdami pasiekti norimą maketą, galite koreguoti kiekvieno turinio išdėstymo elemento ypatybę **Plytelių dydis** arba įtraukti daugiau modulių.
1. Puslapį įrašykite ir atrakinkite bei publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Įspėjimo modulis](add-alert.md)

[Karuselės modulis](add-carousel.md)

[Raiškiojo turinio bloko modulis](add-content-rich-block.md)

[Funkcijos modulis](add-feature-module.md)

[Pagrindinės reklaminės juostos modulis](add-hero-module.md)

[Vaizdo įrašų leistuvo modulis](add-video-player.md)

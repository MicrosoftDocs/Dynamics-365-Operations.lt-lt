---
title: Eksperimento nustatymas
description: Šioje temoje aprašoma, kaip nustatyti eksperimentą trečiosios šalies paslaugoje.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 29c21ceb4c259f463f4a039942e51141201a9809
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2020
ms.locfileid: "4414489"
---
# <a name="set-up-an-experiment"></a>Eksperimento nustatymas

[Nustatę hipotezę ir sėkmės metriką, kurią norite naudoti](experimentation-identify.md), turite nustatyti jūsų eksperimentą trečiosios šalies paslaugoje. Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”. Papildomi veiksmai aprašomi kitose temose.

[ ![Vartotojo eksperimentavimo kelionė – nustatymas](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Eksperimento nustatymas trečiosios šalies paslaugoje
Jau turėjote pasirinkti trečiosios šalies paslaugą, kuri vykdys ir stebės jūsų eksperimentą, ir nustatyti eksperimento jungtį. Šios būtinosios sąlygos išvardytos [Eksperimentavimas „Dynamics 365 Commerce”](experimentation-overview.md).

Atlikite veiksmus, reikalingus eksperimentui sukurti trečiosios šalies paslaugoje. Jei jungtis tinkamai sukonfigūruota, visas eksperimentų, kuriuos nustatysite trečiosios šalies paslaugoje, sąrašas atsiras „Commerce” svetainių daryklėje per maždaug 5 minutes.

## <a name="set-up-your-success-metrics"></a>Jūsų sėkmės metrikos nustatymas
Kiekvienam eksperimentui reikia metrikos, kad būtų galima įvertinti variacijų poveikį ir patvirtinti hipotezę. Atlikite toliau nurodytus veiksmus, norėdami įgalinti metrikos skaičiavimą trečiosios šalies paslaugoje naudojant aktyvius „Dynamics 365 Commerce” telemetrijos įvykius.

Norėdami nustatyti jūsų sėkmės metriką, atlikite toliau pateiktus veiksmus.

1. „Commerce” svetainių daryklės kairiojoje naršymo srityje pasirinkite **Puslapiai** ir pasirinkite puslapį, kurio metriką norite rinkti. 
1. Eikite į puslapio ar modulio, kurį norite sekti, dešinėje esančios ypatybių srities sekciją **Įvykių ID, kurie bus sekami**.
1. Pasirinkite **Peržiūrėti**. Rodomas visų įvykių ID sąrašas. Kopijuokite įvykį, kurį norite sekti, ir įklijuokite įvykio raktą į nurodytą vietą trečiosios šalies paslaugoje. Jei reikia daugiau nei vieno įvykio, vienu metu kopijuokite po vieną raktą. 
    - Norėdami sužinoti, kaip peržiūrėti visus galimus įvykius ir atributus, įskaitant puslapių rodinius ir įplaukų sekimą, žr. [„Commerce“ komponentų įvykiai triktims diagnozuoti ir šalinti](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).
1. Atlikite kitus reikalingus metrikos sekimo veiksmus trečiosios šalies paslaugoje.

## <a name="previous-step"></a>Ankstesnis veiksmas
[Eksperimento hipotezės ir metrikos nustatymas](experimentation-identify.md) 


## <a name="next-step"></a>Kitas veiksmas
[Eksperimento prijungimas ir redagavimas](experimentation-connect-edit.md)

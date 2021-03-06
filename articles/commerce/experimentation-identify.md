---
title: Eksperimento hipotezės ir metrikos nustatymas
description: Šioje temoje aprašoma, kaip nustatyti eksperimento, kurį vykdysite „e-Commerce“ svetainėje „Dynamics 365 Commerce”, hipotezę ir sėkmės metriką.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: a3f5d44e008e4092557d75c8f5d830d5ae36a091
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799057"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Eksperimento hipotezės ir sėkmės metrikos nustatymas
Pirmojo eksperimento ciklo etapo metu nustatoma eksperimento hipotezė ir metrika, sekama norint įvertinti sėkmę. Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su [eksperimento nustatymu ir vykdymu](experimentation-overview.md) „e-Commerce“ svetainėje „Dynamics 365 Commerce”. Papildomi veiksmai aprašomi kitose temose. 

[ ![Vartotojo eksperimentavimo kelionė – nustatymas](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

Hipotezė yra teiginys, kuriame numatote eksperimento rezultatą. Daug veiksnių padeda apibrėžti hipotezę, pvz., tyrimai apie vartotojų elgseną ir jūsų surinkti svetainių duomenys. Kurdami hipotezę nurodysite prielaidą ar teoriją, kurią norite patvirtinti atlikdami eksperimentą. Jūsų eksperimento hipotezės pavyzdys gali būti „*mano pagrindiniame puslapyje esančių baltų marškinėlių nuotrauka vasaros mėnesiais padidins paspaudimų rodiklį labiau nei tamsaus megztinio nuotrauka, nes vasarą žmonės nori dėvėti ką nors lengvo ir šviesaus.*” Tokiu atveju sukurkite variacijas, apimančias baltų marškinėlių ir tamsaus megztinio atvejus, ir publikuokite abi tuo pačiu metu.

Norint patvirtinti hipotezę, eksperimento sėkmė arba nesėkmė turėtų būti tiesiogiai susieta su vartotojų veiksmais; pavyzdžiui, jei svetainės vartotojas spusteli saitą arba mygtuką. Šie veiksmai turi atitikti įvykius, kurie bus pateikti eksperimentą stebinčiai trečiosios šalies paslaugai. Ilgainiui vartotojų, atliekančių veiksmą, procentinė dalis bus susumuota kaip metrika, kurią galėsite naudoti ataskaitoms generuoti ir analizei atlikti. Norėdami peržiūrėti visus galimus įvykius ir atributus, žr. [„Commerce” komponentų įvykiai triktims diagnozuoti ir šalinti](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).

## <a name="previous-step"></a>Ankstesnis veiksmas
[Eksperimentavimas „Dynamics 365 Commerce”](experimentation-overview.md)


## <a name="next-step"></a>Kitas veiksmas
[Eksperimento nustatymas](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
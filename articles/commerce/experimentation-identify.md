---
title: Eksperimento hipotezės ir metrikos nustatymas
description: Šiame straipsnyje aprašoma, kaip nustatyti el. komercijos svetainės, kurią galite vykdyti el. komercijos svetainėje, netenką ir sėkmės metriką Dynamics 365 Commerce.
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
ms.openlocfilehash: 0b6bdf160522fc93e841ec2f8a4542ff80d8f67f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852791"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Eksperimento hipotezės ir sėkmės metrikos nustatymas
Pirmojo eksperimento ciklo etapo metu nustatoma eksperimento hipotezė ir metrika, sekama norint įvertinti sėkmę. Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su [eksperimento nustatymu ir vykdymu](experimentation-overview.md) „e-Commerce“ svetainėje „Dynamics 365 Commerce”. Papildomi veiksmai įtraukti atskiruose straipsnius. 

[ ![Vartotojo eksperimentavimo kelionė – nustatymas.](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

Hipotezė yra teiginys, kuriame numatote eksperimento rezultatą. Daug veiksnių padeda apibrėžti hipotezę, pvz., tyrimai apie vartotojų elgseną ir jūsų surinkti svetainių duomenys. Kurdami hipotezę nurodysite prielaidą ar teoriją, kurią norite patvirtinti atlikdami eksperimentą. Jūsų eksperimento hipotezės pavyzdys gali būti „*mano pagrindiniame puslapyje esančių baltų marškinėlių nuotrauka vasaros mėnesiais padidins paspaudimų rodiklį labiau nei tamsaus megztinio nuotrauka, nes vasarą žmonės nori dėvėti ką nors lengvo ir šviesaus.*” Tokiu atveju sukurkite variacijas, apimančias baltų marškinėlių ir tamsaus megztinio atvejus, ir publikuokite abi tuo pačiu metu.

Norint patvirtinti hipotezę, eksperimento sėkmė arba nesėkmė turėtų būti tiesiogiai susieta su vartotojų veiksmais; pavyzdžiui, jei svetainės vartotojas spusteli saitą arba mygtuką. Šie veiksmai turi atitikti įvykius, kurie bus pateikti eksperimentą stebinčiai trečiosios šalies paslaugai. Ilgainiui vartotojų, atliekančių veiksmą, procentinė dalis bus susumuota kaip metrika, kurią galėsite naudoti ataskaitoms generuoti ir analizei atlikti. Norėdami peržiūrėti visus galimus įvykius ir atributus, žr. [„Commerce” komponentų įvykiai triktims diagnozuoti ir šalinti](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).

## <a name="previous-step"></a>Ankstesnis veiksmas
[Eksperimentavimas „Dynamics 365 Commerce”](experimentation-overview.md)


## <a name="next-step"></a>Kitas veiksmas
[Eksperimento nustatymas](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
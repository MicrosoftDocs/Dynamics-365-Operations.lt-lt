---
title: Kaip galiu atlikti inventoriaus būsenos keitimą daliniam kiekio darbui
description: Šiame puslapyje paaiškinama, kaip sukurti meniu elementą naudojant atitinkamus parametrus, siekiant įgalinti darbuotojus keisti dalinio paketo kiekio atsargų būseną.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 056ce412955808ddf126025ad917b874c54a5e62
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477042"
---
# <a name="enable-inventory-status-change-for-partial-quantity-work"></a>Kaip galiu įjungti inventoriaus būsenos keitimą daliniam kiekio darbui

## <a name="symptoms"></a>Požymiai

Turite atlikti inventoriaus būsenos keitimą daliniam bendram kiekiui.

## <a name="resolution"></a>Sprendimas

Norėdami leisti darbuotojams atlikti šį keitimą, galite sukurti meniu prekę sandėlio valdymo mobiliųjų įrenginių programėlei. Puslapyje **Mobilaus įrenginio meniu prekės** sukurkite (ar redaguokite) meniu prekę, kuri turi tolesnius nustatymus:

- **Režimas:** *Darbas*
- **Naudoti sukurtą darbą:** *Ne*
- **Darbo sukūrimo procesas:** *Judėjimas*
- **Rodyti inventoriaus būseną:** *Taip*

Galite nustatyti kitus laukelius puslapyje, kaip būtina.

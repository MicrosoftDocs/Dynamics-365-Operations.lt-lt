---
title: Bendrasis planavimas planuoja daugiau, nei yra galimas pajėgumas
description: Pagrindinis planavimas nesilaiko pajėgumo apribojimų ir yra suplanuotas daugiau nei prieinamas pajėgumas
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477106"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>Bendrasis planavimas planuoja daugiau, nei yra galimas pajėgumas

## <a name="symptoms"></a>Požymiai

Pagrindinis planavimas nesilaiko pajėgumo apribojimų ir yra suplanuotas daugiau nei prieinamas pajėgumas.

Jums naudojant operacijos planavimą, kai yra baigtinis pajėgumas ir kai maršrutas nurodo reikalavimų mišinį tiek išteklių grupei, tiek ir atskiriems resursams, yra nedidelė per didelio rezervavimo tikimybė dėl būdo, kuriuo algoritmas patvirtina pajėgumo konfliktus. Per didelis rezervavimas gali įvykti jums naudojant padedančius įrankius siekiant vykdyti pagrindinį planavimą. Labiausiai tikėtina, kad jis įvyks, jei yra per daug darbų turinčių atitinkamą trumpą vykdymo laiką.

## <a name="resolution"></a>Sprendimas

Jei reikia, kad nebūtų per didelio rezervavimo veikimo planavimui, galite atlikti vienos linijos pagrindinio planavimo dalies naują planavimą įjungdami **Tikslus baigtas pajėgumas operacijos planavimui** parinktį puslapyje **Pagrindinio planavimo parametrai**. Ši parinktis nėra prieinama pagal nutylėjimą. Privalote rankiniu būdu įtraukti ją į puslapį naudodami suasmenintas funkcijas. Jums naudojant šią parinktį, planavimas bus vykdomas lėčiau dėl paralelaus apdorojimo trūkumo.

---
title: Turimos biudžeto lėšos
description: Šioje temoje pristatyta turima biudžeto lėšų priemonė ir pateikiama informacija, kuri gali padėti konfigūruoti biudžeto kontrolę, optimizuojant jūsų organizacijos finansinių išteklių valdymą.
author: RyanCCarlson2
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 1e7b2bf7ef7bd1bca6db27371f87dfddcdceef89
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710255"
---
# <a name="budget-funds-available"></a>Turimos biudžeto lėšos

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje pristatyta turima biudžeto lėšų priemonė ir pateikiama informacija, kuri gali padėti konfigūruoti biudžeto kontrolę, optimizuojant jūsų organizacijos finansinių išteklių valdymą.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>Patobulinta galimų biudžeto lėšų skaičiavimo funkcija

Tik **galimų** biudžeto lėšų skaičiavimo funkcijos sumos leidžia sekti dokumentų tipų ir valstijų biudžeto kontrolės lenteles, **remiantis puslapio Nustatyti biudžeto kontrolės parametrus parametrais**.

Kai kurios biudžeto kontrolės konfigūracijos parinktys turi turėti konkrečius parametrus, kad funkcija veiktų tinkamai. Šios pasirinktys yra pasirinktos arba išvalytos skirtuke **Biudžeto lėšos,** kuris yra puslapyje **Nustatyti biudžeto kontrolės** parametrus. Toliau pateikiamoje lentelėje rodomi parametrai, reikalingi turimai biudžeto lėšų funkcijai.

| Jei ši pasirinktis pasirinkta | Šią pasirinktį taip pat reikia pasirinkti |
| ------------------------- | -------------------------------- |
| Biudžeto rezervavimai preliminariems biudžeto rezervavimams | Biudžeto rezervavimai ir faktinės *išlaidos* |
| Biudžeto rezervavimai | Faktinės išlaidos |
| Biudžeto rezervavimai biudžeto rezervavimams su pirkimo paraiškos tipo dokumentais | Biudžeto rezervavimai preliminariems biudžeto rezervavimams |

Ši priemonė daro įtaką tik naujiems dokumentams. Esamų dokumentų sumos bus toliau sekamos ir rodomos biudžeto kontrolės statistikos užklausoje, kol bus pakeisti galimi biudžeto lėšų parametrai ir suaktyvinta nauja biudžeto kontrolės konfigūracija. Tada bus pašalinti dokumentų, kurie buvo pašalinti iš galimų biudžeto lėšų skaičiavimo, biudžeto sekimo duomenys.

Rekomenduojame panaikinti neužregistruotų **faktinių išlaidų** pasirinktį. Jį pasirinkus, užregistruotuose dokumentuose, pvz., laukiančiose tiekėjo SF, bus atliekamas daug laiko reikalaujantis biudžeto kontrolės skaičiavimas.

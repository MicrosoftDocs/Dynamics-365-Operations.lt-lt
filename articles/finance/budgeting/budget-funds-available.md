---
title: Turimos biudžeto lėšos
description: Šiame straipsnyje pristatyta turima biudžeto lėšų funkcija ir pateikiama informacija, kuri gali padėti konfigūruoti biudžeto kontrolę, optimizuojant jūsų organizacijos finansinių išteklių valdymą.
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
ms.openlocfilehash: b6f94931ba3514c1c66d80b64846d882861d555c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898246"
---
# <a name="budget-funds-available"></a>Turimos biudžeto lėšos

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje pristatyta turima biudžeto lėšų funkcija ir pateikiama informacija, kuri gali padėti konfigūruoti biudžeto kontrolę, optimizuojant jūsų organizacijos finansinių išteklių valdymą.

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

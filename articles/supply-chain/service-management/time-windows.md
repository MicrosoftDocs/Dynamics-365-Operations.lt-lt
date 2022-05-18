---
title: Laiko langai
description: Galite naudoti laiko langus, kad optimizuotumėte aptarnavimo užsakymo eilučių planavimą.
author: sorenva
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 857e9e023aa5648a06ae564936f06c491ea7cefc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678100"
---
# <a name="time-windows"></a>Laiko langai  

[!include [banner](../includes/banner.md)]

Galite naudoti laiko langus, kad optimizuotumėte aptarnavimo užsakymo eilučių planavimą. Galite nustatyti sistemą taip, kad ji kurtų aptarnavimo užsakymus automatiškai. Pagal laiko lange nurodytus kriterijus galite prijungti kuo daugiau aptarnavimo užsakymo eilučių prie kuo mažesnio skaičiaus aptarnavimo užsakymų.

Laiko langai nurodo, kiek toli aptarnavimo užsakymo eilutė gali būti perkelta nuo jos apskaičiuotos datos. Apskaičiuota data yra numatyta diena, kada turi būti įvykdyta aptarnavimo užsakymo eilutė. Data nustatoma pagal jos intervalo parametrus ir aptarnavimo laikotarpį, kurį nustatėte puslapyje **Aptarnavimo užsakymų kūrimas**. Laiko langą galima nustatyti naudojant toliau pateiktoje lentelėje nurodytas reikšmes.

| Metodas | aprašymas                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Savaitė   | Aptarnavimo užsakymo eilutės data gali būti perkelta į bet kurią laisvą tos pačios savaitės kaip ir pirminė apskaičiuota data dieną.                                                                                                                                                                                    |
| Mėnuo  | Aptarnavimo užsakymo eilutės data gali būti perkelta į bet kurią laisvą to paties mėnesio kaip ir pirminė apskaičiuota data dieną. Pavyzdžiui, aptarnavimo užsakymo eilutės apskaičiuota data yra 2017 m. vasario 15 d. Aptarnavimo užsakymo eilutę galima numatyti bet kurią savaitės dieną nuo 2017 m. vasario 1 d. iki vasario 28 d. |
| Neautomatinis | Galite nurodyti didžiausią dienų iki arba po pirminės apskaičiuotos datos skaičių, per kurį gali būti perkeltas aptarnavimo užsakymas.                                                                                                                                                                           |

Jei aptarnavimo sutarties eilutės laiko lango nenurodysite, iš aptarnavimo sutarties išvesta aptarnavimo užsakymo eilutė turės būti įvykdyta tiksliai tą dieną, kurią ji buvo numatyta iš pradžių.

## <a name="related-topics"></a>Susijusios temos

[Laiko langų kūrimas](create-time-windows.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
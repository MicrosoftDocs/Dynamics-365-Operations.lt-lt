---
title: Į KS eilučių sunaudojimo principo parametrus nepaisoma
description: Į KS (medžiagų važtaraščio) eilučių sunaudojimo principo parametrus nepaisoma.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ee40eff53efd920ebe43a7b2dd28129f01e6ebb5e75bd480a91f758529f77fc5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716961"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>Į KS eilučių sunaudojimo principo parametrus nepaisoma

KB numeris: 4612725

## <a name="symptoms"></a>Požymiai

Problema atsitinka, kai **Automatinis KS suvartojimas** laukelyje **Automatiinis naujinimas** skirtuke, **Gamybos valdymo parametrai** puslapyje yra nustatytas į *Sunaudojimo principas*. Šis parametras nurodo, kad visos komplektavimo specifikacijos (KS) eilutės turėtų būti automatiškai suvartotos, kai gaunamas pirkimo užsakymas. Jei **Sunaudojimo principas** KM eilutės yra aiškiai nustatytas kaip *Rankinis*, galite tikėtis, kad KS eilutės nebus suvartojamos automatiškai. Tačiau, kai iškyla šis problema, KS eilutės, kurių laukas **Sunaudojimo principas** yra nustatytas kaip *Rankinis*, vis tiek suvartojamos automatiškai.

## <a name="resolution"></a>Skiriamoji geba

Jei patiriate šią problemą, gali būti, kad gamybos valdymo parametrai bus nustatyti taip, kad būtų nepaisoma KS eilučių parametro **Sunaudojimo principas**. Puslapyje **Gamybos valdymo parametrai**, skirtuke **Automatinis naujinimas**, patikrinkite lauko **Automatinis KS suvartojimas** vertę. Jei nustatyta kaip *Visada*, sistema nepaisys parametro **Sunaudojimo principo** visose KS eilutėse ir išvalys eilutes. Norėdami, kad sistema gerbtų **Sunaudojimo principo** parametro BOM eilutėse, keiskite **Automatinio BOM suvartojimo** laukelio vertę į *Sunaudojimo principas*.

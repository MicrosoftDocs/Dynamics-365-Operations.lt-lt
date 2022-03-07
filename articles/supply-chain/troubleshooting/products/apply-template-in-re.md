---
title: Negalima taikyti šablono išleistame produkte
description: Negalima taikyti šablono išleistame produkte.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 566686b6a86e67c87f75f9f2e397592174d3d749034f18997ca8ce651c2594a2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760399"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>Negalima kurti šablono išleistame produkte.

KB numeris: 4612097

## <a name="symptoms"></a>Požymiai

Kai sukuriate naują išleistą produktą, naudodami dialogo langą **Naujas išleistas produktas**, galite pasirinkti šabloną. Šablonas turi pateikti numatytuosius daugelio naujo išleisto produkto laukų parametrus. Tačiau kai kurie arba visi laukai nėra nustatomi jums pažymus šabloną.

## <a name="cause"></a>Priežastis

Daug puslapių „Microsoft Dynamics 365 Supply Chain Management“ leidžia jums sukurti šabloną, kuris nustato pradinius įrašams, kurie rodomi tuose puslapiuose, parametrus. Vieną iš šių šablonų galite sukurti **veiksmų srities** skirtuke **Pasirinktys** pasirinkdami Įrašo informacija. Tačiau išleisti produktai yra daug sudėtingesni nei dauguma kitų įrašų tipų. Nepaisant to, kad galite pasirinkti **Įrašo informacija** puslapyje **Išleisti produktai** tačiau norėdami sukurti šabloną galite pasirinkti jį, kai kuriate išleistą produktą, šablone nebus pateikti numatytų naujo išleisto produkto laukų verčių. Todėl išleistiems produktams negalite naudoti „įrašų informacijos“ šablonų. Užuot tai darę, turite sukurti paskirtus produktų šablonus.

## <a name="resolution"></a>Skiriamoji geba

Norėdami sukurti produkto šabloną, naudokite **Šablonas** meniu **Produktas** skirtuke veiksmuų juostoje, o ne **Įrašo informacijos** mygtuką **Parinktys** skirtuke.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Veiksmų juostoje **Produktas** skirtuke **Nauja** grupė rinkitės **Šablonas** ir rinkitės **Kurti asmeninį šabloną** ar **Kurti bendrintą šabloną**, kaip tinkama.

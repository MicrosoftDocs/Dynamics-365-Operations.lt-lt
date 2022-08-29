---
title: Iš dalies rezervuotų perkėlimo užsakymų paketinis išleidimas
description: Šiame straipsnyje aprašoma, kaip nustatyti ir taikyti iš dalies rezervuotų perkėlimo užsakymų iš mobiliojo įrenginio paketinį paleidimą.
author: perlynne
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 741377a43e2bfe702b213647cc6460a3d6ad93fb
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218689"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Iš dalies rezervuotų perkėlimo užsakymų paketinis išleidimas

[!include [banner](../includes/banner.md)]

Paketinio iš dalies rezervuotų perkėlimo užsakymų išleidimo funkcija leidžia naudojant paketinę užduotį į sandėlį iš dalies išleisti perkėlimo užsakymus.
Kadangi galite pasirinkti išleisti dalinį kiekį, prieš išleisdami užsakymą neprivalote laukti, kol sandėlyje bus visas užsakymo kiekis.

Užsakymų paleidimas į sandėlį yra sandėlio valdymo procesų (WMS) procesas. Šis procesas apima tokias veiklas kaip paėmimas, pakavimas ir siuntimas, kurias sandėlio darbininkas gali atlikti naudodamas mobilųjį įrenginį.

## <a name="where-it-applies"></a>Kai taikoma

Naudojant šią funkciją užsakymai į sandėlį išleidžiami naudojant paketinę užduotį. Ši funkcija yra naudinga, kai sandėlyje neturite pakankamai atsargų, tačiau vis tiek norite iš vieno sandėlio į kitą perkelti prekių.

## <a name="how-it-is-set-up"></a>Kaip tai nustatoma

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Perkėlimo užsakymų ir pardavimo užsakymų įvykdymo kriterijų nurodymas

Kad, naudojant paketinę užduotį, užsakymą būtų galima iš dalies išleisti į sandėlį, turi būti patenkinti įvykdymo kriterijai. Šiuos įvykdymo kriterijus nustato įvykdymo strategija.

Perkėlimo užsakymų ir pardavimo užsakymų įvykdymo strategijos nurodomos įmonės lygiu. Atsižvelgiant į įvykdymo strategijos sąranką, paketinio užsakymų išleidimo procesas bus patvirtintas arba atmestas. Tada užsakymai bus atitinkamai apdorojami.

- Norėdami kurti perkėlimo užsakymų ir pardavimo užsakymų įvykdymo strategijas, **\>\>\> eikite į Sandėlio valdymo nustatymas Išleidimo į sandėlio įvykdymo** strategijas ir sukurkite įvykdymo strategiją įvesdami pavadinimą ir aprašymą.
- Norėdami nurodyti įvykdymo koeficientą, vertės tipą ir pranešimą, kuris rodomas pažeidus įvykdymo strategiją, **\>\>\>** **eikite į sandėlio valdymo nustatymo išleidimą į sandėlio įvykdymo strategijas ir nustatykite įvykdymo koeficiento**,**·** **vertės tipo ir įvykdymo pažeidimo pranešimo** laukus.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Perkėlimo užsakymų ir pardavimo užsakymų įvykdymo strategijų nustatymas

- Norėdami nustatyti perkėlimo užsakymų įvykdymo strategijas, **\>\> eikite į Atsargų valdymo nustatymo atsargų ir sandėlio valdymo** parametrus, **·** **tada** sandėlio valdymo skyriaus skirtuke Perkėlimo užsakymai pasirinkite perkėlimo užsakymo vykdymo strategiją.
- Norėdami nustatyti pardavimo užsakymų įvykdymo strategijas, **\>\>** eikite į Gautinų sumų nustatymo parametrus, **tada** skirtuke Sandėlio valdymas pasirinkite pardavimo užsakymo vykdymo strategiją.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-released-in-a-batch"></a>Leisti išleisti pakete ir nurodyti kiekį, kuris turėtų būti išleistas į paketą

Užsakymai į sandėlį kaip paketas išleidžiami naudojant paketinę užduotį. Parametrai, atskiriantys užsakymus, kurie turi būti vykdomi naudojant paketinę užduotį, yra nustatomi pačioje paketinėje užduotyje.

Parametras **Kiekis** nurodo, ar kaip paketas turi būti išleistas visas kiekis, ar fiziškai rezervuotas kiekis. Parametras **Leisti išleisti iš dalies išleistus užsakymus** nurodo, ar kaip paketas išleidžiami užsakymai turi būti patvirtinti, ar atmesti, jei jie buvo iš dalies išleisti anksčiau.

- Norėdami nustatyti perkėlimo užsakymų kiekio ir **leisti** iš dalies išleistų užsakymų parametrus, **eikite** į Sandėlio valdymo paleidimas į sandėlį **Automatinis perkėlimo užsakymų paleidimas \>.\>**
- Norėdami nustatyti pardavimo užsakymų kiekio ir **leisti** išleisti iš dalies išleistų užsakymų parametrus, **eikite** į Sandėlio valdymo paleidimas į sandėlį **Automatinis pardavimo užsakymų paleidimas \>.\>**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

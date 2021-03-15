---
title: Aptarnavimo objektų apžvalga
description: Aptarnavimo objektai yra kliento turtas ir produktai, dėl kurių galite teikti paslaugas.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e0a40d351150ce432164438cd9680cf80792e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974315"
---
# <a name="service-objects-overview"></a>Aptarnavimo objektų apžvalga

[!include [banner](../includes/banner.md)]

Aptarnavimo objektai yra kliento turtas ir produktai, dėl kurių galite teikti paslaugas. Atsižvelgiant į paslaugų, kurias teikiate, tipą, objektai gali būti materialūs ir nematerialūs:

-  Materialūs objektai yra daiktai, tokie kaip mašina ar pastatas, kuriems galite atlikti fizinį faktinę aptarnavimo užduotį.

    Materialus aptarnavimo objektas taip pat gali būti atsargų prekė, kurią sukuriate formoje Išleisto produkto informacija. Atsižvelgiant į atsargų dimensijų grupę, pridedamą prie prekės, jūs galite sukurti aptarnavimo objektą pagal išsamumo lygį, į kurį įeina prekės serijos numeris. Tai pasitarnauja, kai jums reikia stebėti konkrečią prekę, kurią žymi aptarnavimo objektas.

    Materialus aptarnavimo objektas taip pat gali būti prekė, netiesiogiai susijusi su įmonės tiesioginės gamybos arba tiekimo grandine. Pvz., įrankių rinkinys, naudojamas remonto darbams atlikti ir esantis aptarnavimo užsakyme, gali būti aptarnavimo objektas, kuris neįtrauktas į atsargas. Šiuo atveju negalite užregistruoti jo kaip atsargų prekės.

-  Nematerialūs objektai yra nefiziniai objektai, tokie kaip sąskaitų rinkinys arba teisinis dokumentas, pagal kuriuos atliekama aptarnavimo užduotis.

## <a name="example-of-an-intangible-service-object"></a>Nematerialaus aptarnavimo objekto pavyzdys

Įmonė A tvarko finansinius įrašus keliose mažose įmonėse. Vienas įmonės A klientų yra vietinė futbolo komanda, kuriai įmonė A atlieka kassavaitinį buhalterijos tvarkymą ir kasmetinį klubo sąskaitų auditą. Klubo sąskaitos yra nustatytos formoje Aptarnavimo objektai, o aptarnavimo sutartyje jos nurodytos kaip objektas. Objektui priskiriamos dvi aptarnavimo sutarties eilutės. 1 eilutė yra kassavaitinis buhalterijos tvarkymas ir eilutei priskirtas savaitės intervalas, o 2 eilutė – kasmetinis auditas, kuriai priskirtas metų intervalas.

## <a name="related-topics"></a>Susijusios temos

[Aptarnavimo objektų kūrimas](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
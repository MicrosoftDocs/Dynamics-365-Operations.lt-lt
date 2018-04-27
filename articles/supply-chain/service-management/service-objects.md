---
title: Aptarnavimo objektai
description: "Aptarnavimo objektai yra kliento turtas ir produktai, dėl kurių galite teikti paslaugas."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: a69fd6a1b07683383d88c7f5c7986529c7bb1875
ms.contentlocale: lt-lt
ms.lasthandoff: 02/21/2018

---

# <a name="service-objects"></a>Aptarnavimo objektai 

[!INCLUDE [banner](../includes/banner.md)]

Aptarnavimo objektai yra kliento turtas ir produktai, dėl kurių galite teikti paslaugas. Atsižvelgiant į paslaugų, kurias teikiate, tipą, objektai gali būti materialūs ir nematerialūs:

-  Materialūs objektai yra daiktai, tokie kaip mašina ar pastatas, kuriems galite atlikti fizinį faktinę aptarnavimo užduotį.

    Materialus aptarnavimo objektas taip pat gali būti atsargų prekė, kurią sukuriate formoje Išleisto produkto informacija. Atsižvelgiant į atsargų dimensijų grupę, pridedamą prie prekės, jūs galite sukurti aptarnavimo objektą pagal išsamumo lygį, į kurį įeina prekės serijos numeris. Tai pasitarnauja, kai jums reikia stebėti konkrečią prekę, kurią žymi aptarnavimo objektas.

    Materialus aptarnavimo objektas taip pat gali būti prekė, netiesiogiai susijusi su įmonės tiesioginės gamybos arba tiekimo grandine. Pvz., įrankių rinkinys, naudojamas remonto darbams atlikti ir esantis aptarnavimo užsakyme, gali būti aptarnavimo objektas, kuris neįtrauktas į atsargas. Šiuo atveju negalite užregistruoti jo kaip atsargų prekės.

-  Nematerialūs objektai yra nefiziniai objektai, tokie kaip sąskaitų rinkinys arba teisinis dokumentas, pagal kuriuos atliekama aptarnavimo užduotis.

## <a name="example-of-an-intangible-service-object"></a>Nematerialaus aptarnavimo objekto pavyzdys

Įmonė A tvarko finansinius įrašus keliose mažose įmonėse. Vienas įmonės A klientų yra vietinė futbolo komanda, kuriai įmonė A atlieka kassavaitinį buhalterijos tvarkymą ir kasmetinį klubo sąskaitų auditą. Klubo sąskaitos yra nustatytos formoje Aptarnavimo objektai, o aptarnavimo sutartyje jos nurodytos kaip objektas. Objektui priskiriamos dvi aptarnavimo sutarties eilutės. 1 eilutė yra kassavaitinis buhalterijos tvarkymas ir eilutei priskirtas savaitės intervalas, o 2 eilutė – kasmetinis auditas, kuriai priskirtas metų intervalas.

## <a name="related-topics"></a>Susijusios temos

[Aptarnavimo objektų kūrimas](create-service-objects.md)



---
title: Nesutapimų šalinimas gretinant SF bendrąsias sumas
description: Galite naudoti SF bendrųjų sumų gretinimo parinktį, kad užtikrintumėte, jog SF bendrosios sumos nenukryptų nuo numatytų sumų didesniu nei priimtinu nuokrypiu.
author: abruer
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c664f0b66b41b3db8f45b4507bca39e1ffefb599
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834566"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Nesutapimų šalinimas gretinant SF bendrąsias sumas

[!include [banner](../includes/banner.md)]

Vienas iš SF gretinimo tikrinimo tipų – SF bendrųjų sumų gretinimas. Norėdami nurodyti, kad sistemoje būtų gretinamos SF bendrosios sumos, puslapio **Mokėtinų sumų parametrai** skirtuke **SF tikrinimas** nustatykite parinkties **Gretinti SF bendrąsias sumas** reikšmę **Taip**. 

Galite naudoti SF bendrųjų sumų gretinimo parinktį, kad užtikrintumėte, jog SF bendrosios sumos nenukryptų nuo numatytų sumų didesniu nei priimtinu nuokrypiu. Puslapyje **SF bendrųjų sumų gretinimo informacija** palyginamos šešios bendrosios sumos. Jei bet kuri bendroji suma nukrypsta nuo numatomos atitinkamos pirkimo užsakymo bendrosios sumos, vėliavėle pažymimas gretinimo nesutapimas. 

Norėdami peržiūrėti SF, kurioje yra bendrųjų sumų gretinimo nesutapimų, darbo srityje **Tiekėjo SF įrašas** spustelėkite plytelę **Laukiančios SF**. Tada veiksmų srities skirtuke **Peržiūra** spustelėkite **Gretinimo informacija**. Aptikus gretinimo nesutapimus šalia SF sumos rodomos įspėjimo piktogramos. Jei reikia daugiau informacijos apie bendrąsias sumas, galite peržiūrėti SF bendrųjų sumų gretinimo informaciją. 

Jei identifikavę nesutapimą manote, kad SF informacija yra neteisinga, kreipkitės į tiekėją. Atsižvelgdami į galutinę sutartį su tiekėju galite atlikti kurį nors toliau nurodytą veiksmą.

-   Patvirtinkite kainų skirtumą ir užregistruokite SF, kurioje yra gretinimo nesutapimų. Sistemoje gali būti nustatytas patvirtinimo reikalavimas, kad būtų galima užregistruoti SF su gretinimo nesutapimais. Tokiu atveju turite patvirtinti gretinimo nesutapimą ir galite įvesti patvirtinimo komentarą. Tada galėsite pasirinkti SF registravimo veiksmą.
-   Peržiūrėkite SF sumą pagal numatomą sumą ir registruokite SF.
-   Iš tiekėjo reikalaukite viso kredito ir naujos pataisytos SF.

Daugiau informacijos žr. [Išnagrinėti arba pašalinti išimtis](tasks/research-resolve-exceptions.md).



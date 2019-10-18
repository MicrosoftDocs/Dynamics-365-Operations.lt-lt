---
title: Nesutapimų sprendimo SF bendrųjų sumų gretinimo metu apžvalga
description: Galite naudoti SF bendrųjų sumų gretinimo parinktį, kad užtikrintumėte, jog SF bendrosios sumos nenukryptų nuo numatytų sumų didesniu nei priimtinu nuokrypiu.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: d4a20368385ec43547ee3d29770bd83cdec47e4a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189504"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a>Nesutapimų sprendimo SF bendrųjų sumų gretinimo metu apžvalga

[!include [banner](../includes/banner.md)]

Vienas iš SF gretinimo tikrinimo tipų – SF bendrųjų sumų gretinimas. Norėdami nurodyti, kad sistemoje būtų gretinamos SF bendrosios sumos, puslapio **Mokėtinų sumų parametrai** skirtuke **SF tikrinimas** nustatykite parinkties **Gretinti SF bendrąsias sumas** reikšmę **Taip**. 

Galite naudoti SF bendrųjų sumų gretinimo parinktį, kad užtikrintumėte, jog SF bendrosios sumos nenukryptų nuo numatytų sumų didesniu nei priimtinu nuokrypiu. Puslapyje **SF bendrųjų sumų gretinimo informacija** palyginamos šešios bendrosios sumos. Jei bet kuri bendroji suma nukrypsta nuo numatomos atitinkamos pirkimo užsakymo bendrosios sumos, vėliavėle pažymimas gretinimo nesutapimas. 

Norėdami peržiūrėti SF, kurioje yra bendrųjų sumų gretinimo nesutapimų, darbo srityje **Tiekėjo SF įrašas** spustelėkite plytelę **Laukiančios SF**. Tada veiksmų srities skirtuke **Peržiūra** spustelėkite **Gretinimo informacija**. Aptikus gretinimo nesutapimus šalia SF sumos rodomos įspėjimo piktogramos. Jei reikia daugiau informacijos apie bendrąsias sumas, galite peržiūrėti SF bendrųjų sumų gretinimo informaciją. 

Jei identifikavę nesutapimą manote, kad SF informacija yra neteisinga, kreipkitės į tiekėją. Atsižvelgdami į galutinę sutartį su tiekėju galite atlikti kurį nors toliau nurodytą veiksmą.

-   Patvirtinkite kainų skirtumą ir užregistruokite SF, kurioje yra gretinimo nesutapimų. Sistemoje gali būti nustatytas patvirtinimo reikalavimas, kad būtų galima užregistruoti SF su gretinimo nesutapimais. Tokiu atveju turite patvirtinti gretinimo nesutapimą ir galite įvesti patvirtinimo komentarą. Tada galėsite pasirinkti SF registravimo veiksmą.
-   Peržiūrėkite SF sumą pagal numatomą sumą ir registruokite SF.
-   Iš tiekėjo reikalaukite viso kredito ir naujos pataisytos SF.

Daugiau informacijos žr. [Išnagrinėti arba pašalinti išimtis](tasks/research-resolve-exceptions.md).



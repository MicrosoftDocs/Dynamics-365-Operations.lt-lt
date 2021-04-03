---
title: Vieno kvito žurnalų ir valiutos kurso pasikeitimų plėtojimas
description: Šioje temoje aprašoma, kaip atnaujinti vienkartinių kvitų žurnalus ir valiutos perkainojimus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb4eca4933716105789d3bbc21dd374395211d1d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559526"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Vieno kvito žurnalų ir valiutos kurso pasikeitimų plėtojimas

[!include [banner](../includes/banner.md)]

Kai kurios organizacijos įveda žurnalus, kuriuose yra vienas kvitas, turintis daugiau nei vieną klientą ar tiekėją, be to, vykdo Gautinų sumų ar Mokėtinų sumų užsienio valiutos kurso pasikeitimo procesą. Šioje temoje aprašyti veiksmai, kuriuos tos organizacijos turi atlikti, atnaujinant „Microsoft Dynamics 365 for Operations“ į 1611 versiją.

Atlikite šiuos veiksmus atnaujindami „Microsoft Dynamics 365 for Operations“ į 1611 versiją.

1.  Prieš atnaujindami į „Finance and Operations“, įvykdykite Gautinų sumų ir Mokėtinų sumų užsienio valiutos kurso pasikeitimo procesą. Nustatykite lauką **Metodas** į **Sąskaitos faktūros data**. Sukuriama pasikeitimo operacija, kuri anuliuoja paskutinį užsienio valiutos pasikeitimą. Todėl atidarytos operacijos vertinamos pradine operacijos apskaitos valiuta.
2.  Atnaujinkite į 1611 versiją.
3.  Įvykdykite Gautinų sumų ir mokėtinų sumų užsienio valiutos pasikeitimo procesą dar kartą. Šį kartą lauką **Metodas** nustatykite į **Standartinis**. Sukuriama nauja pasikeitimo operacija, kuri pagrįsta dabartiniu užsienio valiutos kursu. Ši operacija įrašo nerealizuotą pelną / nuostolį ir koreguoja suvestinę DK sąskaitą.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
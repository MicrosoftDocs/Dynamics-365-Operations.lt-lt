---
title: "Vieną kuponą ir valiutos perkainojimo atnaujinti &quot;Microsoft Dynamics 365&quot; operacijų versija 1611"
description: "Kai kurios organizacijos įveskite žurnalai, kuriuose vieno kvito, kuriame yra daugiau nei vienas kliento arba tiekėjo, ir jie taip pat organizuoja gautinų sąskaitų arba sąskaitų mokėtinos užsienio valiutos perkainojimo procesas. Šioje temoje aprašoma į veiksmus, šios organizacijos turėtų laikytis, kai jie atnaujinti Microsoft Dynamics 365 operacijų versija 1611."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Vieną kuponą ir valiutos perkainojimo atnaujinti "Microsoft Dynamics 365" operacijų versija 1611

Kai kurios organizacijos įveskite žurnalai, kuriuose vieno kvito, kuriame yra daugiau nei vienas kliento arba tiekėjo, ir jie taip pat organizuoja gautinų sąskaitų arba sąskaitų mokėtinos užsienio valiutos perkainojimo procesas. Šioje temoje aprašoma į veiksmus, šios organizacijos turėtų laikytis, kai jie atnaujinti Microsoft Dynamics 365 operacijų versija 1611.

Kai atnaujinate į Microsoft Dynamics 365 operacijų versija 1611, atlikite toliau nurodytus veiksmus.

1.  Prieš naujindami į "Dynamics 365" operacijoms, vykdyti užsienio valiuta perkainojimo procesus, gautinos ir mokėtinos sąskaitos. Nustatyti, **metodas** lauko į **SF data**. Kad perkainojimo operacija bus sukurtas, panaikina paskutinio valiutos perkainojimo. Todėl atviras operacijas yra įvertinami jų originalus numatytąja valiuta.
2.  Atnaujinti Dynamics 365 operacijų versija 1611.
3.  Dar kartą paleiskite gautinas sąskaitas ir sąskaitų mokėtinos užsienio valiutos perkainojimo procesus. Šį kartą, nustatyti į **metodas** lauko į **standartinis**. Sukuriama nauja perkainojimo operacija, pagal dabartinį keitimo kursą. Šios operacijos įrašai nerealizuotas pelnas/nuostolis ir teisingą suminėje DK sąskaitoje.




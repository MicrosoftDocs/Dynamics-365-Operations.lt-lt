---
title: "Projekto pirkimo užsakymai"
description: "Šiame straipsnyje aprašomi įvairūs metodai, kuriuos naudodami galite kurti projekto pirkimo užsakymų. Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties ir nuo to, kada įsigytos prekės suvartojamos bei priskiriamos projektui."
author: twheeloc
manager: AnnBe
ms.date: 08/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: d55c999ed1f506a2d9487c8cc94bf0e9cce3bed1
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2017

---

# <a name="purchase-orders-for-a-project"></a>Projekto pirkimo užsakymai

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašomi įvairūs metodai, kuriuos naudodami galite kurti projekto pirkimo užsakymų. Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties ir nuo to, kada įsigytos prekės suvartojamos bei priskiriamos projektui.

„Microsoft Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidime kurti projekto pirkimo užsakymus galite keliais būdais. Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties, nuo to, kada įsigytos prekės suvartojamos ir kada įsigytos prekės priskiriamos projektui.

### <a name="methods-for-creating-a-purchase-order"></a>Pirkimo užsakymo kūrimo metodai

Galite naudoti vieną iš tolesnių metodų, norėdami sukurti pirkimo užsakymą naudodami projekto valdymą ir apskaitą. Pirkimo užsakymo paskirtis lemia, kada pirkimo užsakymas turi būti įvykdytas ir, tuo pačiu, kada reikia sumokėti už projekto prekes.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metodas</th>
<th>Paskirtis</th>
<th>Prekių suvartojimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pirkimo užsakymo kūrimas tiesiai iš projekto.</td>
<td>Naudokite šį metodą, kad pirktumėte prekes iš išorinio tiekėjo suvartoti vykdant projektą. Kurti pirkimo užsakymą galite tolesniais dviem būdais.
<ul>
<li>Iš paties projekto. Šiuo atveju pirkimo užsakymo projektas jau yra nustatytas.</li>
<li>Pereidami į projekto pirkimo užsakymą. Turite pasirinkti ir tiekėją, ir projektą, kuriame reikia sukurti pirkimo užsakymą.</li>
</ul></td>
<td>Prekės suvartojamos atnaujinus tiekėjo SF.</td>
</tr>
<tr class="even">
<td>Sukurkite pirkimo užsakymą pagal pardavimo užsakymą.</td>
<td>Naudokite šį metodą, jei norite pirkti prekes, kai kuriate projekto pardavimo užsakymą.</td>
<td>Prekės suvartojamos, kai klientui išrašoma pardavimo užsakymo SF.</td>
</tr>
<tr class="odd">
<td>Sukurkite pirkimo užsakymą pagal prekės poreikį.</td>
<td>Naudokite šį metodą, jei norite pirkti prekes, kai kuriate projekto prekės poreikį.</td>
<td>Prekės suvartojamos, kai atnaujinamas prekės poreikio važtaraštis.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Kai atnaujinsite tiekėjo SF arba važtaraštį, jus paragins atnaujinti ir prekės poreikio važtaraštį.

Daugiau informacijos žr. [Gauti pirkimo užsakyme pateiktas prekes pagal prekės poreikį](tasks/receive-items-purchase-order-item-requirement.md).



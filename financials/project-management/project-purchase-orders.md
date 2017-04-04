---
title: "Projekto pirkimo užsakymai"
description: "Šiame straipsnyje aprašomi įvairūs metodai, kuriuos naudodami galite kurti projekto pirkimo užsakymų. Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties ir nuo to, kada įsigytos prekės suvartojamos bei priskiriamos projektui."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 82305cfe38e7193cece3b9e7784fb81fd40f9c70
ms.lasthandoff: 03/31/2017


---

# <a name="purchase-orders-for-a-project"></a>Projekto pirkimo užsakymai

Šiame straipsnyje aprašomi įvairūs metodai, kuriuos naudodami galite kurti projekto pirkimo užsakymų. Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties ir nuo to, kada įsigytos prekės suvartojamos bei priskiriamos projektui.

Microsoft Dynamics 365 operacijoms, galite naudoti kelis metodus projekto pirkimo užsakymų kūrimas. Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties, nuo to, kada įsigytos prekės suvartojamos ir kada įsigytos prekės priskiriamos projektui.

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
> Atnaujinus pirkimo užsakymo SF arba važtaraštį, jus paragins atnaujinti dėl prekės poreikio važtaraštis.



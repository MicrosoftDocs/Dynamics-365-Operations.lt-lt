---
title: Projekto pirkimo užsakymai
description: Šiame straipsnyje aprašomi įvairūs metodai, kuriuos naudodami galite kurti projekto pirkimo užsakymų. Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties ir nuo to, kada įsigytos prekės suvartojamos bei priskiriamos projektui.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 767a1805e7a2609c5c28bed891b42f7c8c3aaffc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556509"
---
# <a name="purchase-orders-for-a-project"></a>Projekto pirkimo užsakymai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi įvairūs metodai, kuriuos naudodami galite kurti projekto pirkimo užsakymų. Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties ir nuo to, kada įsigytos prekės suvartojamos bei priskiriamos projektui.

Programoje „Microsoft Dynamics 365 for Finance and Operations“ kurti projekto pirkimo užsakymus galite keliais metodais. Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties, nuo to, kada įsigytos prekės suvartojamos ir kada įsigytos prekės priskiriamos projektui.

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


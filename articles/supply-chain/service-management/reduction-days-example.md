---
title: Mažinimo dienų pavyzdys
description: Mažinimo dienų pavyzdys.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90a2efff0add508ddb3d750bb3ca27ea35bf113a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836067"
---
# <a name="reduction-days-example"></a>Mažinimo dienų pavyzdys 

[!include [banner](../includes/banner.md)]


Sukūrėte abonementinę operaciją kliento abonementui tvarkyti, kaip aprašyta toliau pateiktoje lentelėje.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nuo datos</p></th>
<th><p>Iki datos</p></th>
<th><p>Prenumerata</p></th>
<th><p>Abonemento tipas</p></th>
<th><p>Projektas</p></th>
<th><p>Kategorija</p></th>
<th><p>Pardavimo valiuta</p></th>
<th><p>Pardavimo kaina</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2011 m. kovo 01 d.</p></td>
<td><p>2011 m. kovo 31 d.</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Reguliarus</strong></p></td>
<td><p>9013</p></td>
<td><p>SubKat2</p></td>
<td><p>EUR</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>


Klientas praneša, kad jam dvi dienas (kovo 10 d. ir kovo 11 d.) nereikės aptarnavimo. Sutinkate sutrumpinti abonementą šiomis dvejomis dienomis.

Sukuriate naują **Mažinimo dienų** tipo operaciją, kaip aprašyta toliau pateiktoje lentelėje.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nuo datos</p></th>
<th><p>Iki datos</p></th>
<th><p>Prenumerata</p></th>
<th><p>Abonemento tipas</p></th>
<th><p>Projektas</p></th>
<th><p>Kategorija</p></th>
<th><p>Pardavimo valiuta</p></th>
<th><p>Pardavimo kaina</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2011 m. kovo 10 d.</p></td>
<td><p>2011 m. kovo 11 d.</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Sumažinimo dienos</strong></p></td>
<td><p>9013</p></td>
<td><p>SubKat2</p></td>
<td><p>EUR</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>


Kai išrašoma SF už 2011 m. kovo mėn. operacijas, 200 EUR pardavimo kaina yra sumažinama 12,90 EUR. Todėl mokėtina abonementinės operacijos suma yra 187,10 EUR, tad bendra SF suma už dvi operacijas yra 187,10 EUR.

## <a name="see-also"></a>Taip pat žiūrėkite

[Abonementinio mokesčio dienų sumažinimas](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
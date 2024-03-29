---
title: Aptarnavimo būsenos ir eigos lauko sąveika
description: Formoje Aptarnavimo užsakymai antraštės lauke Eiga nurodoma viso aptarnavimo užsakymo būsena, o lauke Būsena nurodoma atskirų aptarnavimo užsakymo eilučių būsena.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e83df9ca8ee19b5e29d4eccf2bd883ee6ddff62
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677652"
---
# <a name="service-status-and-progress-field-interaction"></a>Aptarnavimo būsenos ir eigos lauko sąveika

[!include [banner](../includes/banner.md)]

Formoje **Aptarnavimo užsakymai** aptarnavimo užsakymo lauke **Eiga** nurodoma viso aptarnavimo užsakymo būsena, o lauke **Būsena** nurodoma atskirų aptarnavimo užsakymo eilučių būsena.

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Eiga</p></th>
<th><p>1 eilutės būsena</p></th>
<th><p>2 eilutės būsena</p></th>
<th><p>3 eilutės būsena</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Vykdoma</strong></p></td>
<td><p><strong>Sukurta</strong></p></td>
<td><p><strong>Sukurta</strong></p></td>
<td><p><strong>Sukurta</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Vykdoma</strong></p></td>
<td><p><strong>Atšaukta</strong></p></td>
<td><p><strong>Sukurta</strong></p></td>
<td><p><strong>Sukurta</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Vykdoma</strong></p></td>
<td><p><strong>Sukurta</strong></p></td>
<td><p><strong>Atšaukta</strong></p></td>
<td><p><strong>Užregistruota</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Atšaukta</strong></p></td>
<td><p><strong>Atšaukta</strong></p></td>
<td><p><strong>Atšaukta</strong></p></td>
<td><p><strong>Atšaukta</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Užregistruota</strong></p></td>
<td><p><strong>Užregistruota</strong></p></td>
<td><p><strong>Užregistruota</strong></p></td>
<td><p><strong>Užregistruota</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Užregistruota</strong></p></td>
<td><p><strong>Užregistruota</strong></p></td>
<td><p><strong>Atšaukta</strong></p></td>
<td><p><strong>Atšaukta</strong></p></td>
</tr>
</tbody>
</table>

Aptarnavimo užsakymo eiga vykdoma, jei visų eilučių būsena **Sukurta**; taip pat ji vykdoma, jei kai kurių eilučių būsena yra **Atšaukta** arba **Užregistruota**.

Jei visos aptarnavimo užsakymo eilutės yra pažymėtos nurodant būseną **Užregistruota**, būsenos užsakymo eiga yra **Užregistruota**.. Jei kai kurios eilutės pažymėtos nurodant būseną **Užregistruota**, o kai kurios – nurodant būseną **Atšaukta**, eigos būsena vis dar **Užregistruota**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Aptarnavimo būsenos ir eigos lauko sąveika
description: Formoje Aptarnavimo užsakymai antraštės lauke Eiga nurodoma viso aptarnavimo užsakymo būsena, o lauke Būsena nurodoma atskirų aptarnavimo užsakymo eilučių būsena.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd7b5160149a38dd62535901c1225bf704f404d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570791"
---
# <a name="service-status-and-progress-field-interaction"></a>Aptarnavimo būsenos ir eigos lauko sąveika 

[!include [banner](../includes/banner.md)]


Formoje **Aptarnavimo užsakymai** aptarnavimo užsakymo lauke **Eiga** nurodoma viso aptarnavimo užsakymo būsena, o lauke **Būsena** nurodoma atskirų aptarnavimo užsakymo eilučių būsena.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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

  



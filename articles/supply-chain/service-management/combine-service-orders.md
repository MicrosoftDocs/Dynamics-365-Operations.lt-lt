---
title: Jungti aptarnavimo užsakymus
description: Galite jungti aptarnavimo užsakymus.
author: kamaybac
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5df9571cb1330489651a28462b747cacd7ac7e46
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580461"
---
# <a name="combine-service-orders"></a>Jungti aptarnavimo užsakymus   

[!include [banner](../includes/banner.md)]


Kurdami aptarnavimo užsakymo eilutes automatiškai, formoje **Aptarnavimo sutartys** galite pasirinkti vieną iš toliau pateiktų parinkčių, skirtų nurodyti, kaip juos norite grupuoti:

  - **Pagal aptarnavimo sutartį**

  - **Pagal aptarnavimo užduotį**

  - **Pagal darbuotoją**

  - **Pagal aptarnavimo objektą**

## <a name="example"></a>Pavyzdys

Sukūrėte aptarnavimo sutartį, kurios pradžios data yra 2007-03-31. Lauke **Jungti aptarnavimo užsakymus** nurodykite **Pagal aptarnavimo objektą**. Tada sukuriate šias aptarnavimo sutarties eilutes:

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Sutarties eilutės numeris</p></th>
<th><p>Operacijos tipas</p></th>
<th><p>aprašymas</p></th>
<th><p>Intervalas</p></th>
<th><p>Aptarnavimo objektas</p></th>
<th><p>Pradžios data</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Valanda</strong></p></td>
<td><p>SAL1</p></td>
<td><p>Savaitinis</p></td>
<td><p>X-1</p></td>
<td><p>2007-04-01</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Valanda</strong></p></td>
<td><p>SAL2</p></td>
<td><p>Kas dvi savaites</p></td>
<td><p>X-2</p></td>
<td><p>2007-04-01</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Valanda</strong></p></td>
<td><p>SAL3</p></td>
<td><p>Savaitinis</p></td>
<td><p>X-2</p></td>
<td><p>2007-04-01</p></td>
</tr>
</tbody>
</table>


Nenurodote jokios aptarnavimo sutarties eilutės laiko lango. Dėl to aptarnavimo užsakymo eilutės nebus perkeltos iš apskaičiuotos dienos, į kurią jos patenka.

Toliau formoje **Kurti aptarnavimo užsakymus** sugeneruokite aptarnavimo užsakymo eilutes nuo 2007-04-01 iki 2007-04-30.

Iš viso sukuriama 10 aptarnavimo užsakymų. Kadangi jūsų pasirinkti sujungti nustatymai buvo **Pagal aptarnavimo objektą**, visuose sukurtuose aptarnavimo užsakymuose yra tik tos aptarnavimo užsakymo eilutės, kuriose nurodytas vienas konkretus aptarnavimo objektas. Aptarnavimo užsakymo eilutės, sugeneruotos aptarnavimo sutartyje, kurių aptarnavimo data ir objektas yra tokie patys, sujungiamos į vieną aptarnavimo užsakymą.


> [!NOTE]
> <P>Šiame pavyzdyje kalendoriuje, kuris nurodytas formoje <STRONG>Aptarnavimo valdymo parametrai</STRONG>, nėra uždarytų dienų.</P>



Papildomas aptarnavimo užsakymo eilučių grupavimas į aptarnavimo užsakymus vykdomas pagal bet kokį laiko langą, kurį nurodote aptarnavimo sutarties eilutėse.

## <a name="see-also"></a>Taip pat žiūrėkite

[Automatiškai kurkite aptarnavimo užsakymus](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
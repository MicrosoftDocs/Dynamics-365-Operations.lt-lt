---
title: Nustatymas, kaip išmesti grąžintas prekes
description: Nustatykite,, kaip išmesti grąžintas prekes.
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3123f49ef5fbd07afa61b035a2f6dd4c0af2ce40
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679225"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>Nustatymas, kaip išmesti grąžintas prekes

[!include [banner](../includes/banner.md)]

Rengiant grąžinimo užsakymą būtina nurodyti grąžinimo priežasties kodą, taip nustatant, kodėl produktas grąžinamas. Taip pat būtina nurodyti perdavimo kodą ir perdavimo veiksmą, taip nurodant, kokius veiksmus reikia atlikti su grąžinamu produktu.

Perdavimo kodas gali būti taikomas, kai kuriate grąžinimo užsakymą, registruojate prekės gavimą arba prekės gavimo važtaraščio atnaujinimą ir sulaikymo užsakymo pabaigą.

Galite nurodyti bet kuriuos perdavimo kodus, būtinus verslo procesams palaikyti. Šioje lentelėje pateikti kodai, pagal kuriuos paprastai priskiriamas grąžinamos prekės perdavimas.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Perdavimo tipas</p></th>
<th><p>Bendrasis kodas</p></th>
<th><p>Aprašas</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Likvidavimas</p></td>
<td><p>SC</p></td>
<td><p>Nurašyti / Sunaikinti</p></td>
</tr>
<tr class="even">
<td><p>Likvidavimas</p></td>
<td><p>DC</p></td>
<td><p>Paaukoti labdarai</p></td>
</tr>
<tr class="odd">
<td><p>Likvidavimas</p></td>
<td><p>TD</p></td>
<td><p>Trečiosios šalies turto realizavimas</p></td>
</tr>
<tr class="even">
<td><p>Likvidavimas</p></td>
<td><p>SL</p></td>
<td><p>Turto išgelbėjimas</p></td>
</tr>
<tr class="odd">
<td><p>Likvidavimas</p></td>
<td><p>TS</p></td>
<td><p>Trečiosios šalies turto pardavimas (antrinė rinka)</p></td>
</tr>
<tr class="even">
<td><p>Remontuoti / Modifikuoti</p></td>
<td><p>RW</p></td>
<td><p>Perdirbti</p></td>
</tr>
<tr class="odd">
<td><p>Remontuoti / Modifikuoti</p></td>
<td><p>RF</p></td>
<td><p>Perdaryti / Atnaujinti</p></td>
</tr>
<tr class="even">
<td><p>Remontuoti / Modifikuoti</p></td>
<td><p>MD</p></td>
<td><p>Modifikuoti</p></td>
</tr>
<tr class="odd">
<td><p>Remontuoti / Modifikuoti</p></td>
<td><p>RP</p></td>
<td><p>Remontas</p></td>
</tr>
<tr class="even">
<td><p>Remontuoti / Modifikuoti</p></td>
<td><p>RV</p></td>
<td><p>Grąžinti tiekėjui</p></td>
</tr>
<tr class="odd">
<td><p>Kita</p></td>
<td><p>AI</p></td>
<td><p>Naudoti taip, kaip yra</p></td>
</tr>
<tr class="even">
<td><p>Kita</p></td>
<td><p>RS</p></td>
<td><p>Perparduoti</p></td>
</tr>
<tr class="odd">
<td><p>Kita</p></td>
<td><p>EX</p></td>
<td><p>Keitimas</p></td>
</tr>
<tr class="even">
<td><p>Kita</p></td>
<td><p>MS</p></td>
<td><p>Įvairios</p></td>
</tr>
</tbody>
</table>


Nurodydami kiekvieną perdavimo kodą turite pasirinkite perdavimo veiksmą. Perdavimo veiksmas apibrėžia su perdavimo kodu susietus fizinius ir finansinius veiksmus. Pvz., perdavimo veiksmas gali nurodyti, kokie fiziniai veiksmai turi būti atlikti su grąžinta preke, koks finansinis poveikis bus patirtas dėl grąžintos prekės, taip pat, ar prekę reikia pakeisti ir nusiųsti klientui. Atsižvelgdami į verslo poreikius, galite nurodyti bet kokį perdavimo kodų skaičių, bet yra tik šeši galimi perdavimo veiksmai. Šioje lentelėje pateikti perdavimo veiksmai ir jų aprašai.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Perdavimo veiksmas</p></th>
<th><p>aprašymas</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Kreditas</strong></p></td>
<td><p>Grąžinti prekę į atsargas ir suteikti klientui kreditą.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tik kreditas</strong></p></td>
<td><p>Suteikti klientui kreditą jam nereikalaujant ir nesitikint, kad prekė bus grąžinta.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nurašyta</strong></p></td>
<td><p>Nurašyti prekę į atliekas ir suteikti klientui kreditą.</p></td>
</tr>
<tr class="even">
<td><p><strong>Keitimas ir kreditas</strong></p></td>
<td><p>Grąžinti prekę į atsargas, sukurti keitimo užsakymą ir suteikti klientui kreditą.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Keitimas ir nurašymas</strong></p></td>
<td><p>Nurašyti prekę į atliekas, sukurti keitimo užsakymą ir suteikti klientui kreditą.</p></td>
</tr>
<tr class="even">
<td><p><strong>Grąžinti klientui</strong></p></td>
<td><p>Atmesti grąžintą prekę ir grąžinti ją klientui.</p></td>
</tr>
</tbody>
</table>

## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Pasirinkite sulaikymo užsakymo perdavimo kodą

1. Eikite į **Atsargų valdymas** \> **Periodinis** \> **Kokybės valdymas** \> **Sulaikymo užsakymai**.
1. Skirtuko **Apžvalga** lauke **Perdavimo kodas** pasirinkite jau egzistuojančio sulaikymo užsakymo veiksmą.

## <a name="see-also"></a>Taip pat žiūrėkite

[Sulaikymo užsakymas (forma)](/dynamicsax-2012//quarantine-order-form)

[Perdavimo kodai (forma)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

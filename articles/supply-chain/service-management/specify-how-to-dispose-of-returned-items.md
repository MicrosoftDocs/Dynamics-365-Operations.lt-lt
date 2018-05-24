---
title: "Nustatymas, kaip išmesti grąžintas prekes"
description: "Nustatykite,, kaip išmesti grąžintas prekes."
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d25a53ac58b0ab44605af253f174ba2ec7b74174
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="specify-how-to-dispose-of-returned-items"></a>Nustatymas, kaip išmesti grąžintas prekes 

[!include [banner](../includes/banner.md)]


Rengiant grąžinimo užsakymą būtina nurodyti grąžinimo priežasties kodą, taip nustatant, kodėl produktas grąžinamas. Taip pat būtina nurodyti perdavimo kodą ir perdavimo veiksmą, taip nurodant, kokius veiksmus reikia atlikti su grąžinamu produktu.

Perdavimo kodas gali būti taikomas, kai kuriate grąžinimo užsakymą, registruojate prekės gavimą arba prekės gavimo važtaraščio atnaujinimą ir sulaikymo užsakymo pabaigą.

Galite nurodyti bet kuriuos perdavimo kodus, būtinus verslo procesams palaikyti. Šioje lentelėje pateikti kodai, pagal kuriuos paprastai priskiriamas grąžinamos prekės perdavimas.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<col style="width: 50%" />
<col style="width: 50%" />
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

1.  Spustelėkite **Atsargų valdymas** \> **Periodinis** \> **Kokybės valdymas** \> **Sulaikymo užsakymai**.

2.  Skirtuko **Apžvalga** lauke **Perdavimo kodas** pasirinkite jau egzistuojančio sulaikymo užsakymo veiksmą.



## <a name="see-also"></a>Taip pat žiūrėkite

[Sulaikymo užsakymas (forma)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))

[Perdavimo kodai (forma)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))

  




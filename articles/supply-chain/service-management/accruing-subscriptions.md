---
title: Kaupimo abonementai
description: Naudodami aptarnavimo abonementus, rankiniu būdu sukaupiate įplaukas laikotarpiuose po datos, kai išrašėte SF apmokėjimo operacijai.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a2b581c8ae52f4c379e8e511dc898a8d106d149
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908065"
---
# <a name="accruing-subscriptions"></a>Kaupimo abonementai 

[!include [banner](../includes/banner.md)]


Naudodami aptarnavimo abonementus, rankiniu būdu sukaupiate įplaukas laikotarpiuose po datos, kai išrašėte SF apmokėjimo operacijai.

Kaupimo laikotarpiai kuriami SF laikotarpiui, nurodytam abonemento apmokėjime ir kaupimo laikotarpiai yra paremti abonemento laikotarpio kodu.

Galite kaupti ir grąžinti sukauptas įplaukas.

## <a name="reverse-accruals-of-credit-amounts"></a>Atšaukti kredito sumų kaupimus

Jei priskyrėte abonemento sumas, kurioms išrašytos SF, galite naudoti du metodus kaupimo sumoms atšaukti:

  - Galite atšaukti kiekvieną sukauptų įplaukų operaciją atskirai prieš sukurdami operacijos kredito pažymos pasiūlymą. Tai rankinis metodas. (rankinis)

  - Galima nustatyti, kad sukauptos sumos būtų atšauktos tą dieną, kai užregistruojama kredito pažyma, arba tikrąją kaupimo registravimo dieną.

Daugiau informacijos rasite [Abonemento parametrai (forma)](/dynamicsax-2012//subscription-parameters-form).

## <a name="setup-requirements"></a>Nustatyti reikalavimus

Norėdami kaupti įplaukas, įsitikinkite, kad šie duomenų reikalavimai atitinka pateiktus:

## <a name="account-setup"></a>Abonento nustatymas

**NG – abonementas** ir **Sukauptos įplaukos – abonementas** sumos turi būti nustatytos modulyje **Projektas**.

Registruojant sukauptas įplaukas, nuo sąskaitos **NG – abonementas** nurašoma sukaupta suma ir į sąskaitą **Sukauptos įplaukos – abonementas** įrašoma sukaupta suma.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Nustatyti sąskaitas sukauptoms abonementų įplaukoms

1.  Spustelėkite **Projektų valdymas ir apskaita** \> **Nustatymas** \> **Registravimas** \> **Registravimo DK nustatymai**.

2.  Spustelėkite skirtuką **Įplaukų sąskaitos** ir pasirinkite **NG – abonementas** arba **Sukauptos įplaukos – abonementas** norėdami nustatyti sąskaitas.

## <a name="subscription-group-setup"></a>Abonementų grupės nustatymas

Kad būtų galima kaupti įplaukas abonementams, turi būti pažymėtas žymės langelis **Kaupti įplaukas**. Tai rasite tos grupės, kuri susieta su abonementu, formoje **Abonementų grupės**. Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo abonementai** \> **Abonementų grupės**.

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Įplaukų abonementų grupėje kaupimo įjungimas

1.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo abonementai** \> **Abonementų grupės**.

## <a name="periods"></a>Laikotarpiai

Turite nustatyti apskaitomo laikotarpio kodą. Išskyrus atvejį, kai norite kaupti įplaukas tuose pačiuose laiko intervaluose, kaip ir sąskaitų faktūrų išrašymo atveju, taip pat turite nustatyti kaupimo laikotarpį.

Toliau pateiktoje lentelėje rasite sąrašą kaupimo laikotarpių, kuriuos galite nustatyti kiekvienam apskaitos laikotarpiui:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>SF išrašymo laikotarpis</p></th>
<th><p>Kaupimo laikotarpis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Metai</strong></p></td>
<td><ul>
<li><p><strong>Metai</strong></p></li>
<li><p><strong>Ketvirtis</strong></p></li>
<li><p><strong>Mėnuo</strong></p></li>
<li><p><strong>Diena</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Ketvirtis</strong></p></td>
<td><ul>
<li><p><strong>Ketvirtis</strong></p></li>
<li><p><strong>Mėnuo</strong></p></li>
<li><p><strong>Diena</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Mėnuo</strong></p></td>
<td><ul>
<li><p><strong>Mėnuo</strong></p></li>
<li><p><strong>Diena</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Savaitė</strong></p></td>
<td><ul>
<li><p><strong>Diena</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Diena</strong></p></td>
<td><ul>
<li><p><strong>Diena</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

SF išrašymo laikotarpio nustatymas yra privaloma visos abonementų grupės nustatymo dalis. Galite nuspręsti, ar nustatyti ir abonementų grupės kaupimo laikotarpį. Jei nustatysite abonementų grupės kaupimo laikotarpį, šis laikotarpis bus pasiūlytas lauke **Laikotarpio kodas**. Šį lauką rasite formoje **Kaupti abonemento įplaukas**, kai kaupiate abonemento įplaukas. Tačiau kaupimo laikotarpis yra pasirenkama informacija apie abonementų grupę.


> [!NOTE]
> <P>Naudodami šį maršrutą atidarykite formą <STRONG>Kaupti abonemento įplaukas</STRONG>. Spustelėkite <STRONG>Aptarnavimo valdymas</STRONG> &gt; <STRONG>Periodinis</STRONG> &gt; <STRONG>Aptarnavimo abonementai</STRONG> &gt; <STRONG>Kaupti abonemento įplaukas</STRONG>.</P>


## <a name="transactions"></a>Operacijos

Galite valdyti DK operacijų, sukurtų registruojant sukauptas įplaukas, skaičių. Abonementuose nurodykite, ar DK operacijos turi būti sukurtos kaip suma, ar vienoje eilutėje.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Nurodykite rodomą sukauptų operacijų registravimo informacijos lygį

1.  Spustelėkite **Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**.

2.  Skirtuke **Finansinis**, esančiame lauke **Sąskaita faktūra**, pasirinkite **Bendroji suma** arba **Eilutė**.


## <a name="see-also"></a>Taip pat žiūrėkite

[Kaupti abonemento įplaukas](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
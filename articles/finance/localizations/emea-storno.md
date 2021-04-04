---
title: Storno apskaita
description: Storno apskaita yra neigiamų skaičių naudojimo praktika, norint pakeisti pradinius žurnalo sąskaitos įrašus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 1219713
ms.search.region: Czech Republic, Germany, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85f9a99383aca88306a29f15ba139076c9c3c81e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236211"
---
# <a name="storno-accounting"></a>Storno apskaita

[!include [banner](../includes/banner.md)]

Storno apskaita yra neigiamų skaičių naudojimo praktika, norint pakeisti pradinius žurnalo sąskaitos įrašus.

*Storno apskaita* yra neigiamų debeto arba kredito sumų naudojimo praktika, norint pakeisti pradinius žurnalo sąskaitos įrašus. Kadangi finansininkai paprastai Storno įrašus rašo raudonu rašalu, šis apskaitos praktika dar vadinama *raudonuoju Storno*. Naudodami „Storno“ apskaitą galite atšaukti dokumentą su netiksliomis sumomis, bet turite visuomet įvesti tinkamą dokumento sumą po atšaukimo.

## <a name="example"></a>Pavyzdys
Buhalteris publikuoja sąskaitą iš pardavėjo 120 USD. Mokėjimo proceso metu nustatoma, kad buhalteris per klaidą įvedė 120 USD, o ne 102 USD. Dabar buhalteriui reikia sukurti „Storno“ originaliam dokumentui ir tuomet sukurti tinkamą sąskaitą 102 USD. Dėl daugiau informacijos, žr. [Pardavėjo sąskaitų apžvalga](../accounts-payable/vendor-invoices-overview.md). Toliau pateikiamoje lentelėje parodytas bendrasis Storno įrašas.

| **Dokumento ID** | **Sąskaita** | **Debetas** | **Kreditas** | **Komentaras**                  |
|-----------------|-------------|-----------|------------|------------------------------|
| Invoice0001     | Pirkimo sąskaita   | 120       |            | Pradinė SF (klaidinga) |
| Invoice0001     | Tiekėjo kodas  |           | 120        | Pradinė SF (klaidinga) |
|                 |             |           |            |                              |
| Storno0001      | Pirkimo sąskaita   | -120     |            | Storno                       |
| Storno0001      | Tiekėjo kodas  |           | -120      | Storno                       |
|                 |             |           |            |                              |
| Invoice0002     | Pirkimo sąskaita   | 102       |            | Teisinga SF              |
| Invoice0002     | Tiekėjo kodas  |           | 102        | Teisinga SF              |

Šiame pavyzdyje balanso ataskaita nurodo tolesnę informaciją.

| Paskyra    | Debetas | Kreditas | Likutis |
|------------|-------|--------|---------|
| Pirkimo sąskaita  | 102   | 0      | 102     |
| Tiekėjo kodas | 0     | 102    | -102    |

## <a name="differences-between-storno-and-reverse-entries"></a>Storno ir atvirkštinių įrašų skirtumai
Yra du būdai, kuriais galima tinkamai publikuoti įrašus - atvirkštinis ir „Storno“. Jei naudosite atvirkštinį įrašą, originalaus bendro įrašo kopija bus sukurta su atvirkštine skola ir kredito sumomis, o sumos liks tame pačiame ženkle. Jei naudojate Storno, sistema sukuria pradinio bendrojo įrašo kopiją, tačiau sumos įrašomos naudojant neigiamą ženklą. Toliau pateikiamoje lentelėje parodytas bendrasis Storno įrašas.

| **Dokumento ID** | **Sąskaita** | **Debetas** | **Kreditas** | **Komentaras**                  |
|-----------------|-------------|-----------|------------|------------------------------|
| Invoice0001     | Pirkimo sąskaita   | 120       |            | Pradinė SF (klaidinga) |
| Invoice0001     | Tiekėjo kodas  |           | 120        | Pradinė SF (klaidinga) |
|                 |             |           |            |                              |
| Reverse0001     | Pirkimo sąskaita   |           | 120        | Atšaukti                      |
| Reverse0001     | Tiekėjo kodas  | 120       |            | Atšaukti                      |
|                 |             |           |            |                              |
| Invoice0002     | Pirkimo sąskaita   | 102       |            | Teisinga SF              |
| Invoice0002     | Tiekėjo kodas  |           | 102        | Teisinga SF              |

Šiame pavyzdyje balanso ataskaita nurodo tolesnę informaciją.

| Paskyra    | Debetas | Kreditas | Likutis |
|------------|-------|--------|---------|
| Pirkimo sąskaita  | 222   | 120    | 102     |
| Tiekėjo kodas | 120   | 222    | -102    |

Atkreipkite dėmesį, kad atvirkštinių ir storno įrašų balansai yra lygūs. Esama skirtumo tarp skolos pajamų ir kredito pajamų, nes atvirkštinis įrašas padaro skolos ir kredito pajamas nereikalingas. Atšaukti įrašai naudojami šalyse / regionuose, kuriuose apyvarta naudojama retai. Kitose šalyse / regionuose naudojama Storno apskaita.

## <a name="partial-storno"></a>Dalinis Storno
*Dalinis „Storno“* yra apskaitos praktika naudojanti neigiamas skolos ir kredito sumas siekiant atgręžti pradinio žurnalo apskaitos įrašus. Kai kuriose šalyse / regionuose galima naudoti dalinį Storno. Pavyzdžiui, buhalteris publikuoja sąskaitą iš pardavėjo 120 USD. Mokėjimo proceso metu nustatoma, kad buhalteris per klaidą įvedė klaidingą skaičių seką. Pradinė sąskaita 102 USD turėjo klaidą skaičių sekoje. Naudodamas dalinį „Storno“, buhalteris turėtų sukurti „Storno“ 18 USD. Tolesnė lentelė rodo bendrą įrašą daliniam „Storno“.

| **Dokumento ID** | **Sąskaita** | **Debetas** | **Kreditas** | **Komentaras**                  |
|-----------------|-------------|-----------|------------|------------------------------|
| Invoice0001     | Pirkimo sąskaita   | 120       |            | Pradinė SF (klaidinga) |
| Invoice0001     | Tiekėjo kodas  |           | 120        | Pradinė SF (klaidinga) |
|                 |             |           |            |                              |
| Storno0001      | Pirkimo sąskaita   | \-18      |            | Dalinis Storno               |
| Storno0001      | Tiekėjo kodas  |           | \-18       | Dalinis Storno               |

Šiame pavyzdyje balanso ataskaita nurodo tolesnę informaciją.

| Paskyra    | Debetas | Kreditas | Likutis |
|------------|-------|--------|---------|
| Pirkimo sąskaita  | 102   | 0      | 102     |
| Tiekėjo kodas | 0     | 102    | -102    |

Dalinis Storno gali sukelti problemą pradinėje spausdinimo formoje. Jei esama skirtumo tarp originalaus dokumento datos ir „Storno“ datos, gali būti sunku gauti tikslią valiutos sumą. Dėl to, dalinis „Storno“ leidžiamas tik tam tikriems dokumentams. „Dynamics 365 Finance“ teikia dalinio Storno funkciją, skirtą tik dokumentams ir šalims / regionams, kuriuose ją galima naudoti.

## <a name="how-to-enter-storno-on-journal-lines"></a>Kaip įvesti „Storno“ žurnalų eilutėse
Įveskite skolos ir kredito sumas su neigiamu ženklu žurnalo eilutėje tam, kad sukurtumėte „Storno“ įrašą. Laukelis **Taisymas** yra nustatomas publikavimo proceso metu. 

## <a name="how-storno-is-displayed"></a>Kaip Storno rodomas
„Finance“ neigiamas žurnalo sumas tvarko specialiu būdu. Bendras žurnalo įrašas, kliento transakcija, pardavėjo transakcijos ir kitos transakcijos suteikia „Storno“ funkciją, kaip parodyta toliau.

<table>
<thead>
<tr class="row-1">
<th class="column-1" rowspan="2">Vartotojo įvestis žurnalo eilutėje</th>
<th class="column-2" colspan="2">Saugojimo principas</th>
<th class="column-4" colspan="2">Rodymo principas</th>
<th class="column-6" colspan="3">Poveikis išrašo ataskaitai</th>
</tr>
<tr class="row-1">
<th class="column-2">Laukas Koregavimas</th>
<th class="column-3">Laukas Suma</th>
<th class="column-4">Suma operacijos valiuta</th>
<th class="column-5">Suma</th>
<th class="column-6">Stulpelis Debetas</th>
<th class="column-7">Stulpelis Kreditas</th>
<th class="column-8">Stulpelis Balansas</th>
</tr>
</thead>
<tbody>
<tr class="row-2">
<td class="column-1"> Debetas</td>
<td class="column-2">Nr.</td>
<td class="column-3">&gt;0</td>
<td class="column-4" align="right">Suma</td>
<td class="column-5" align="right">Suma</td>
<td class="column-6">Padidėja</td>
<td class="column-7"></td>
<td class="column-8">Padidėja</td>
</tr>
<tr class="row-3">
<td class="column-1"> Kreditas</td>
<td class="column-2">Nr.</td>
<td class="column-3">&lt;0</td>
<td class="column-4" align="right">–Suma</td>
<td class="column-5" align="right">Suma</td>
<td class="column-6"></td>
<td class="column-7">Padidėja</td>
<td class="column-8">Sumažėja</td>
</tr>
<tr class="row-4">
<td class="column-1">–Debetas</td>
<td class="column-2">Taip</td>
<td class="column-3">&gt;0</td>
<td class="column-4" align="right">+Suma</td>
<td class="column-5" align="right">–Suma</td>
<td class="column-6">Sumažėja</td>
<td class="column-7"></td>
<td class="column-8">Padidėja</td>
</tr>
<tr class="row-5">
<td class="column-1">–Kreditas</td>
<td class="column-2">Taip</td>
<td class="column-3">&lt;0</td>
<td class="column-4" align="right">–Suma</td>
<td class="column-5" align="right">–Suma</td>
<td class="column-6"></td>
<td class="column-7">Sumažėja</td>
<td class="column-8">Sumažėja</td>
</tr>
</tbody>
</table>

Storno rodinį formose, tinkleliuose, stulpeliuose ir laukuose galite tinkinti. Pavyzdžiui, galite išjungti rodymą ar keisti išplėtimą neigiamoms sumoms. Taip pat, galite naudoti **Koregavimo** laukelį visiems rodomams nustatymams, jei **Koregavimo** laukelis turi „Taip“, kai tai yra „Storno“ įrašas.

![Žurnalo įrašo Storno sumos](./media/journal-storno.png)

## <a name="how-documents-create-storno"></a>Kaip dokumentai kuria Storno
Kai kurie dokumentai sukuria atšaukimo transakcijas. Pvz., DK, mokėtinų sumų ir gautinų sumų dokumentų užsienio valiutos kurso pasikeitimo operacija atšaukia negautą pelną ir nuostolį. Norėdami gauti daugiau informacijos, žr. [Užsienio valiutos kurso pasikeitimas modulyje Didžioji knyga](../general-ledger/foreign-currency-revaluation-general-ledger.md) arba [Užsienio valiutos kurso pasikeitimas moduliuose Mokėtinos sumos ir Gautinos sumos](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md). Po atšaukimo transakcijos sukūrimo, naujos transakcijos bus sukurtos su nesuprastais padidėjimais ar praradimais. Transakcijų atšaukimai taip pat kuriami inventoriui. Dėl daugiau informacijos, žr. [Inventoriaus uždarymas](../../supply-chain/cost-management/inventory-close.md). Tam tikri dokumentai suteikia galimybę atšaukti anksčiau užregistruotą dokumentą. Pavyzdžiui, vartotojas gali sukurti kredito pažymą, norėdamas atšaukti anksčiau sukurtą SF. Dokumentai naudoti konkrečius parametrus, kad sukurtų atvirkštines ir „Storno“ transakcijas. Pavyzdžiui, užsienio valiutos pervertinimas sukuria atvirkštines ir „Storno“ transakcijas pagal bendrą buhalterinės knygos korekcijos parametrą. Kliento kredito pažyma sukuria atvirkštines arba Storno operacijas pagal gautinų sumų kredito pažymos koregavimo parametrą.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
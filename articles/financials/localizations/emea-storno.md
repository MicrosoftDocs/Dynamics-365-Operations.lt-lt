---
title: Storno apskaita
description: "Storno apskaita yra neigiamų skaičių naudojimo praktika, norint pakeisti pradinius žurnalo sąskaitos įrašus."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 1219713
ms.search.region: Czech Republic, Germany, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-semaz
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: be02501c8a18c9f4a1ad6354372191ae07b0e5b3
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="storno-accounting"></a>Storno apskaita

Storno apskaita yra neigiamų skaičių naudojimo praktika, norint pakeisti pradinius žurnalo sąskaitos įrašus.

*Storno apskaita* yra neigiamų debeto arba kredito sumų naudojimo praktika, norint pakeisti pradinius žurnalo sąskaitos įrašus. Kadangi finansininkai paprastai Storno įrašus rašo raudonu rašalu, šis apskaitos praktika dar vadinama *raudonuoju Storno*. Storno apskaita suteikia galimybę atšaukti dokumentą su neteisingomis sumomis, tačiau po atšaukimo visada reikia įvesti teisingą dokumento sumą.

## <a name="example"></a>Pavyzdys
Finansininkas užregistruoja tiekėjo SF už 120 USD. Mokėjimo proceso metu finansininkas klaidingai įveda 120 USD, o ne 102 USD. Dabar finansininkas turi sukurti pradinio dokumento Storno ir tada sukurti teisingą 102 USD vertės SF. Daugiau informacijos žr. [Tiekėjo SF](../accounts-payable/vendor-invoices-overview.md). Toliau pateikiamoje lentelėje parodytas bendrasis Storno įrašas.

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
Registravimo įrašus – atvirkštinius ir storno – galima ištaisyti dviem būdais. Jei naudojate atvirkštinį įrašą, sukuriama pradinio bendrojo įrašo kopija su atvirkštinėmis debeto ir kredito sąskaitomis, ir sumų ženklas lieka toks pat. Jei naudojate Storno, sistema sukuria pradinio bendrojo įrašo kopiją, tačiau sumos įrašomos naudojant neigiamą ženklą. Toliau pateikiamoje lentelėje parodytas bendrasis Storno įrašas.

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

Atkreipkite dėmesį, kad atvirkštinių ir storno įrašų balansai yra lygūs. Debeto apyvarta ir kredito apyvarta skiriasi, nes atvirkštiniuose įrašuose debeto ir kredito apyvarta tampa perteklinė. Atšaukti įrašai naudojami šalyse / regionuose, kuriuose apyvarta naudojama retai. Kitose šalyse / regionuose naudojama Storno apskaita.

## <a name="partial-storno"></a>Dalinis Storno
*Dalinis Storno* yra neigiamų debeto arba kredito sumų naudojimo apskaitos praktika, norint pakeisti pradinius žurnalo sąskaitos įrašų dalį. Kai kuriose šalyse / regionuose galima naudoti dalinį Storno. Pavyzdžiui, finansininkas užregistruoja tiekėjo SF už 120 USD. Mokėjimo proceso metu nustatoma, kad finansininkas klaidingai įvedė neteisingą numeraciją. Pradinės 102 USD vertės SF numeracijoje buvo klaida. Naudodamas dalinį Storno, finansininkas turėtų sukurti 18 USD vertės Storno. Toliau pateikiamoje lentelėje parodytas dalinio Storno įrašas.

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

Dalinis Storno gali sukelti problemą pradinėje spausdinimo formoje. Jei skiriasi pradinio dokumento ir storno datos, gali būti sunku tiksliai apskaičiuoti valiutos sumą. Todėl dalinį Storno galima naudoti tik tam tikruose dokumentuose. „Microsoft Dynamics 365 for Operations“ teikia dalinio Storno funkciją, skirtą tik dokumentams ir šalims / regionams, kuriuose ją galima naudoti.

## <a name="how-to-enter-storno-on-journal-lines"></a>Kaip įvesti Storno žurnalo eilutes
Įveskite debeto arba kredito sumą su neigiamu ženklu žurnalo eilutėje, kad sukurtumėte Storno įrašą. Laukas **Koregavimas** nustatomas registravimo proceso metu. 

## <a name="how-storno-is-displayed"></a>Kaip Storno rodomas
„Dynamics 365 for Operations“ neigiamas žurnalo sumas tvarko specialiu būdu. Bendrojo žurnalo įrašas, kliento operacija, tiekėjo operacija ir kitos operacijos teikia Storno funkciją, kaip parodyta toliau.

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

Storno rodinį formose, tinkleliuose, stulpeliuose ir laukuose galite tinkinti. Pavyzdžiui, galite išjungti ženklo rodymą arba keisti neigiamų sumų užpildymą. Taip pat galite naudoti lauką **Koregavimas** su visais rodymo parametrais, jei lauko **Koregavimas** parinktis yra Taip, tada tai yra Storno įrašas.

![Žurnalo įrašo Storno sumos](./media/journal-storno.png)

## <a name="how-documents-create-storno"></a>Kaip dokumentai kuria Storno
Tam tikri dokumentai kuria atšaukimo operacijas. Pvz., DK, mokėtinų sumų ir gautinų sumų dokumentų užsienio valiutos kurso pasikeitimo operacija atšaukia negautą pelną ir nuostolį. Daugiau informacijos žr. [DK užsienio valiutos kurso pasikeitimas](../general-ledger/foreign-currency-revaluation-general-ledger.md) arba [Mokėtinos sumos ir gautinos sumos](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md). Sukūrus atšaukimo operaciją, sukuriamos naujos operacijos su negautu pelnu ir nuostoliu. Taip pat sukuriamos atsargų atšaukimo operacijos. Daugiau informacijos žr. [Atsargų uždarymas](../../supply-chain/cost-management/inventory-close.md). Tam tikri dokumentai suteikia galimybę atšaukti anksčiau užregistruotą dokumentą. Pavyzdžiui, vartotojas gali sukurti kredito pažymą, norėdamas atšaukti anksčiau sukurtą SF. Dokumentuose naudojami konkretūs parametrai, kad būtų sukurtos atvirkštinės arba Storno operacijos. Pavyzdžiui, užsienio valiutos kurso pasikeitimo operacija sukuria atvirkštines arba Storno operacijas pagal DK koregavimo parametrą. Kliento kredito pažyma sukuria atvirkštines arba Storno operacijas pagal gautinų sumų kredito pažymos koregavimo parametrą.



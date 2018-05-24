---
title: Prenumeratos pardavimo kainos
description: "Kai kuriate abonementą, pardavimo kainą gaunate iš pardavimo kainos nustatymo, sukurto formoje Pardavimo kaina (abonementas)."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASalespriceSubscription
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
ms.openlocfilehash: d9d462121915ce3f800581a9540dc1ef8f6e785f
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="subscription-sales-prices"></a>Prenumeratos pardavimo kainos   

[!include [banner](../includes/banner.md)]


Kai kuriate abonementą, pardavimo kainą gaunate iš pardavimo kainos nustatymo, sukurto formoje **Pardavimo kaina (abonementas)**.

Formoje **Pardavimo kaina (abonementas)** galite sukurti pardavimo kainas, skirtas tam tikriems abonementams, arba galite sukurti pardavimo kainas, kurios taikomos plačiau. Pardavimo kainos, kuri turi būti taikoma abonementui, atveju, laikotarpio kodas bei abonemento valiuta turi būti identiški laikotarpio kodui ir pardavimo kainos valiutai.

Jei abonemento ir pardavimo kainos laikotarpio kodas ir valiuta yra identiški, abonemento pardavimo kainos pasirenkamos remiantis prioritetais, kurie nurodyti toliau pateiktoje lentelėje. Tuščias lentelės langelis reiškią tuščią lauką, o X reiškia vertę, kuri lygi vertei, esančiai abonemente, iš kurio sukuriama operacija.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Pirmenybė</p></th>
<th><p><strong>Kategorija</strong></p></th>
<th><p><strong>Projekto ID</strong></p></th>
<th><p><strong>Abonementas</strong></p></th>
<th><p><strong>Pardavimo valiuta</strong></p></th>
<th><p><strong>Laikotarpio kodas</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
</tbody>
</table>


Kai sukuriamas abonemento mokestis, pardavimo kaina, kuri yra išsamiausia (kaip parodyta anksčiau pateiktoje lentelėje), pažymima kaip abonemento pardavimo kaina.

## <a name="update-and-index-subscription-sales-prices"></a>Abonemento pardavimo kainų naujinimas ir indeksavimas

Abonemento pardavimo kainą galite atnaujinti atnaujindami bazinę kainą arba indeksą. Galite naujinti tam pagal tam tikrą procentinę dalį arba pagal naują vertę.

## <a name="subscription-fee-sales-prices"></a>Abonemento mokesčio pardavimo kainos

Kai sukuriate abonemento mokestį, pardavimo kaina yra pagrįsta tam abonementui nustatyta pardavimo kaina. Galite arba naudoti bazinę kainą iš abonemento kainų nustatymo, arba sukurti indeksuotas pardavimo kainas.

## <a name="example"></a>Pavyzdys

Jūs norite nustatyti naujam projektui 9030 nustatyti 500 eurų abonemento pardavimo kainas. Formoje **Pardavimo kaina (abonementas)**, kaip nurodyta toliau pateiktoje lentelėje, galite sukurti abonemento pardavimo kainos eilutę.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Galioja nuo</p></th>
<th><p>Kategorija</p></th>
<th><p>Project</p></th>
<th><p>Prenumerata</p></th>
<th><p>Laikotarpio kodas</p></th>
<th><p>Pardav. valiuta</p></th>
<th><p>Pardavimo kaina</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2006 08 28</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Mėnuo</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Įsidėmėkite, kad laukai **Kategorija** ir **Abonementas** yra tušti.

Tada sukurkite toliau nurodytus abonementus.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aptarnavimo abonementas</p></th>
<th><p>Project</p></th>
<th><p>Abonementų grupė</p></th>
<th><p>Kategorija</p></th>
<th><p>Valiuta</p></th>
<th><p>Laikotarpio kodas</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubKat1</p></td>
<td><p>EUR</p></td>
<td><p>Mėnesinis</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubKat2</p></td>
<td><p>EUR</p></td>
<td><p>Mėnesinis</p></td>
</tr>
</tbody>
</table>


Dabar galite sukurti abonemento mokesčius abiems abonementams, esantiems abonementų grupėje Sub1:

1.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo abonementai** \> **Abonementų grupės**.

2.  Formoje **Abonementų grupės** spustelėkite **Funkcija** \> **Sukurti abonementinį mokestį**.

3.  Formoje **sukurti abonementinį mokestį** įveskite atitinkamą informaciją. Daugiau informacijos ieškokite [Abonementinio mokesčio operacijų kūrimas](create-subscription-fee-transactions.md).

Abonementiniai mokesčiai, kurių pardavimo kaina lygi 500 EUR, sukuriami abiejuose abonementuose, kaip parodyta toliau pateiktoje lentelėje.

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
<th><p>Projekto data</p></th>
<th><p>Aptarnavimo abonementas</p></th>
<th><p>Project</p></th>
<th><p>Kategorija</p></th>
<th><p>Pradžios data</p></th>
<th><p>Pabaigos data</p></th>
<th><p>Pardavimo valiuta</p></th>
<th><p>Pardavimo kaina</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2006 08 28</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubKat1</p></td>
<td><p>2007 01 01</p></td>
<td><p>2007 03 31</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>2006 08 28</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubKat2</p></td>
<td><p>2007 01 01</p></td>
<td><p>2007 03 31</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Vėliau, jūs galite nuspręsti, kad norite nurodyti projekto 9030 SubKat1 kategorijos pardavimo kainas. Todėl jūs turite sukurti naują pardavimo kainų eilutę, kurioje būtų nurodyta 550 EUR pardavimo kaina, skirta projekto 9030 ir SubKat1 mokesčių kategorijos kombinacijai. Dabar projekte 9030 pateiktos dvi abonemento pardavimo kainų eilutės, kaip parodyta toliau pateiktoje lentelėje.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Galioja nuo</p></th>
<th><p>Kategorija</p></th>
<th><p>Project</p></th>
<th><p>Prenumerata</p></th>
<th><p>Laikotarpio kodas</p></th>
<th><p>Valiuta</p></th>
<th><p>Pardavimo kaina</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2007 08 28</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Mėnuo</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>2007 08 28</p></td>
<td><p>SubKat1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>Mėnuo</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>


Pakartokite pirmiau aprašytą procedūrą, kad sukurtumėte abonemento mokesčius abiems abonementams, esantiems abonementų grupėje Sub1. Toliau pateiktoje lentelėje nurodytos operacijos, kurios buvo sukurtos kiekvienam abonementui, susietam su abonementų grupe.

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
<th><p>Projekto data</p></th>
<th><p>Prenumerata</p></th>
<th><p>Project</p></th>
<th><p>Kategorija</p></th>
<th><p>Pradžios data</p></th>
<th><p>Pabaigos data</p></th>
<th><p>Pardavimo valiuta</p></th>
<th><p>Pardavimo kaina</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>2007 07 28</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubKat1</p></td>
<td><p>2008 01 01</p></td>
<td><p>2008 03 31</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>2008 07 28</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubKat2</p></td>
<td><p>2008 01 01</p></td>
<td><p>2008 03 31</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Pirmojoje 00020\_135 abonemento operacijoje 550 EUR pardavimo kaina gaunama iš abonemento pardavimo kainos, kuri nustatyta konkretaus projekto ir kategorijos kombinacijai. Antrojoje 00021\_135 abonemento operacijoje 500 EUR pardavimo kaina naudojama kaip projekto abonemento pardavimo kaina, kadangi nėra nustatytos kainos 9030 projekto ir SubKat2 kategorijos kombinacijai.

## <a name="see-also"></a>Taip pat žiūrėkite

[Abonemento pardavimo kainų naujinimas ir indeksavimas](update-and-index-subscription-sales-prices.md)

  




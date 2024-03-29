---
title: Permokėjimų mokėjimo nuolaidos
description: Šiame straipsnyje pateikti scenarijai, rodantys, kaip tvarkyti mokėjimą, kai klientas gauna mokėjimo nuolaidą, bet ir permoka.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7c4e98481bc3607d3dce68a6b6cb0478524442f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804161"
---
# <a name="cash-discounts-for-overpayments"></a>Permokėjimų mokėjimo nuolaidos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikti scenarijai, rodantys, kaip tvarkyti mokėjimą, kai klientas gauna mokėjimo nuolaidą, bet ir permoka. 

Laikoma, kad permokėta pagal SF, kai mokėjimo suma yra didesnė už SF sumos ir mokėjimo nuolaidos skirtumą. Norėdami nurodyti, kaip bus apdorojamas gautinas mokėjimo nuolaidos skirtumas permokėjus pagal SF, naudokite puslapio **Gautinų sumų parametrai** laukus **Mokėjimo nuolaidų administravimas** ir **Maksimalus permokėjimas / neprimokėjimas**. Šiame pavyzdyje, klientas permokėjo sąskaitą faktūrą 0,50.

| Bendroji SF suma | Galima mokėjimo nuolaida | Suma, kurią reikia sumokėti, įskaitant mokėjimo nuolaidą | Suma, kurią klientas iš tikrųjų moka |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00        | 10,50                   | 94,50                                               | 95,00                             |

## <a name="cash-discount-administration--specific"></a>Mokėjimo nuolaidų administravimas = specifinis
Kai puslapyje **Automatinių operacijų sąskaitos** pasirenkama lauko **Mokėjimo nuolaidų administravimas** parinktis **Specifinis**, naudojama visa mokėjimo nuolaida. Permokėjimo suma yra užregistruojama mokėjimo nuolaidų skirtumų DK sąskaitoje arba išlieka kaip kliento sąskaitos balansas. Atliekamą veiksmą lemia šios sąlygos: permokėjimo suma yra tarp 0,00 ir lauke **Maksimalus permokėjimas / neprimokėjimas** įvestos sumos, ar permokėjimo suma yra didesnė už lauko **Maksimalus permokėjimas / neprimokėjimas** sumą.

### <a name="scenario-1"></a>1 scenarijus

Pagal šį scenarijų permokėjimo suma yra tarp 0,00 ir maksimalaus permokėjimo / neprimokėjimo sumos. SF įvedama 105,00, o jei per septynias dienas apmokama pagal SF, mokėjimo nuolaida bus galima.

| Bendroji SF suma | Galima mokėjimo nuolaida | Suma, kurią reikia sumokėti, įskaitant mokėjimo nuolaidą |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Klientas mokėjimo nuolaidos laikotarpiu sumoka 95,00. Mokėjimas yra sudengiamas su 105,00 SF. Sudengus SF ir mokėjimą, bus sukurtos šios kliento gautinų sumų operacijos.

| Operacija   | Suma | Likutis |
|---------------|--------|---------|
| PVM sąskaita faktūra       | 105,00 | 0,00    |
| Mokėjimas       | –95,00 | 0,00    |
| Mokėjimo nuolaida | –10,50 | 0,00    |

Sugeneruojami šie mokėjimo ir sudengimo apskaitos įrašai.

**Mokėjimas**

| Paskyra             | Debeto suma | Kredito suma |
|---------------------|--------------|---------------|
| Grynieji pinigai                | 95,00        |               |
| Gautinos sumos |              | 95,00         |

**Sudengimas**

| Paskyra                                                                                                          | Debeto suma | Kredito suma |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Mokėjimo nuolaida (puslapio **Mokėjimo nuolaidos** laukas **Pagrindinė sąskaita, skirta kliento nuolaidoms**)                 | 10,50        |               |
| Gautinos sumos                                                                                              |              | 10,50         |
| Kliento mokėjimo nuolaida (puslapio **Automatinių operacijų sąskaita** laukas **Kliento mokėjimo nuolaida**) |              | 0,50          |
| Gautinos sumos                                                                                              | 0,50         |               |

### <a name="scenario-2"></a>2 scenarijus

Pagal šį scenarijų permokėjimo suma yra didesnė už maksimalaus permokėjimo / neprimokėjimo sumą. SF įvedama 105,00, o jei per septynias dienas apmokama pagal SF, mokėjimo nuolaida bus galima.

| Bendroji SF suma | Galima mokėjimo nuolaida | Suma, kurią reikia sumokėti, įskaitant mokėjimo nuolaidą |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Klientas mokėjimo nuolaidos laikotarpiu sumoka 95,00. Mokėjimas yra sudengiamas su 105,00 SF. Sudengus SF ir mokėjimą, bus sukurtos šios kliento gautinų sumų operacijos.

| Operacija   | Suma | Likutis |
|---------------|--------|---------|
| PVM sąskaita faktūra       | 105,00 | 0,00    |
| Mokėjimas       | –95,00 | –0,50   |
| Mokėjimo nuolaida | –10,50 | 0,00    |

Permokėta 0,50 suma lieka kaip atviras mokėjimo balansas mokėjimo ir gali būti sudengta su kita SF. Sugeneruojami šie mokėjimo ir sudengimo apskaitos įrašai. 

**Mokėjimas**

| Paskyra             | Debeto suma | Kredito suma |
|---------------------|--------------|---------------|
| Grynieji pinigai                | 95,00        |               |
| Gautinos sumos |              | 95,00         |

**Sudengimas**

| Paskyra                                                                                          | Debeto suma | Kredito suma |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Mokėjimo nuolaida (puslapio **Mokėjimo nuolaidos** laukas **Pagrindinė sąskaita, skirta kliento nuolaidoms**) | 10,50        |               |
| Gautinos sumos                                                                              |              | 10,50         |

## <a name="cash-discount-administration--unspecific"></a>Mokėjimo nuolaidų administravimas = nespecifinis
Kai puslapyje **Automatinių operacijų sąskaitos** pasirenkama lauko **Mokėjimo nuolaidų administravimas** parinktis **Nespecifinis**, mokėjimo nuolaidos suma sumažinama permokėjimo sumos dydžiu. Šis veiksmas visada taikomas neatsižvelgiant, ar permokėjimo suma didesnė ar mažesnė už lauke **Maksimalus permokėjimas / neprimokėjimas** įvestą sumą.

### <a name="scenario-3"></a>3 scenarijus

Pagal šį scenarijų SF įvedama 105,00, o jei per septynias dienas apmokama pagal SF, mokėjimo nuolaida bus galima.

| Bendroji SF suma | Galima mokėjimo nuolaida | Suma, kurią reikia sumokėti, įskaitant mokėjimo nuolaidą |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Klientas mokėjimo nuolaidos laikotarpiu sumoka 95,00. Mokėjimas yra sudengiamas su 105,00 SF. Sudengus SF ir mokėjimą, bus sukurtos šios kliento gautinų sumų operacijos.

| Operacija   | Suma | Likutis |
|---------------|--------|---------|
| PVM sąskaita faktūra       | 105,00 | 0,00    |
| Mokėjimas       | –95,00 | –0,00   |
| Mokėjimo nuolaida | –10,00 | 0,00    |

Mokėjimo nuolaidos suma yra sumažinama nuo 10,50 iki 10,00. Mokėjimo ir SF laikomos sudengtomis. 

**Mokėjimas**

| Sąskaita             | Debeto suma | Kredito suma |
|---------------------|--------------|---------------|
| Grynieji pinigai                | 95,00        |               |
| Gautinos sumos |              | 95,00         |

**Sudengimas**

| Paskyra                                                                                          | Debeto suma | Kredito suma |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Mokėjimo nuolaida (puslapio **Mokėjimo nuolaidos** laukas **Pagrindinė sąskaita, skirta kliento nuolaidoms**) | 10,50        |               |
| Gautinos sumos                                                                              |              | 10,50         |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

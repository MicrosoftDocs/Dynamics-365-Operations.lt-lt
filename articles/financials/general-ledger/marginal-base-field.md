---
title: "PVM tarifai pagal bazinę ribą ir skaičiavimo metodus"
description: "Šioje temoje aiškinama, kaip naudojant vertes laukuose Bazinės ribos ir Skaičiavimo metodas nustatomas (-i) pardavimo ir pirkimo operacijų mokesčių tarifas (-ai)."
author: twheeloc
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bf0f8f2e3f553ea181e8cc9ab5b712fce64a89d4
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>PVM tarifai pagal bazinę ribą ir skaičiavimo metodus

[!include[banner](../includes/banner.md)]


Šioje temoje aiškinama, kaip naudojant vertes laukuose Bazinės ribos ir Skaičiavimo metodas nustatomas (-i) pardavimo ir pirkimo operacijų mokesčių tarifas (-ai).

Puslapio PVM kodai Skaičiavimo „FastTab‟ Bazinės ribos laukas nustato, kuri suma naudojama parinkti tinkamam mokesčio tarifui (-ams) iš tarifų PVM kodų reikšmių puslapyje. Sumos tipas lauke Bazinė riba kartu su lauko Skaičiavimo metodas metodu nustato logiką, kuria ieškoma tinkamo operacijos mokesčio tarifo (-ų). 

Kaip pateikta toliau esančiuose pavyzdžiuose, šiuose laukuose naudojant įvairias verčių kombinacijas, gaunami labai skirtingi PVM skaičiavimų rezultatai. Pavyzdžiuose naudojamos tos pačios mokesčių intervalo reikšmės, puslapyje PVM kodų reikšmės nustatytos kiekvienam mokesčio kodui. Norėdami atidaryti šį puslapį, puslapyje PVM kodai spustelėkite PVM kodas &gt; Reikšmės.

> [!Important]                                                                                                                  
> Jei vieno ar kelių jūsų PVM kodų Bazinė riba paremta eilučių sumomis ar vienetais, lauko Skaičiavimo metodas, esančio DK parametrų puslapyje, reikšmė, turi būti nustatyta į Eilutė. |

## <a name="net-amount-per-line"></a> Grynoji kiekvienos eilutės suma
Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal SF eilučių grynąją sumą, išskyrus bet kokius kitus mokesčius.

### <a name="example"></a>Pavyzdys

PVM tarifai yra nustatomi toliau nurodytais intervalais.

| Sumos intervalas    | Mokesčio tarifas |
|--------------------|----------|
| 0 – 50             | 30 %      |
| 50 – 100           | 20 %      |
| 100 – 0 (&gt; 100) | 10 %      |

> [!NOTE]                                                                                                             
> Viršutinė paskutinio intervalo riba nulis (0) reiškia, kad į intervalą įtraukiamos visos sumos, viršijančios 100.

Bazinė riba: **Grynoji kiekvienos eilutės suma** 

Skaičiavimo metodas: **Intervalas** 

Perkate 8 lempas, kurių kiekviena kainuoja 25,00. 

Grynoji SF eilutės suma yra 200,00. 

Mokestis apskaičiuojamas taip: 

Bendra PVM suma = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00. 

Bendra SF suma = 200,00 + 35,00 = 235,00. 

**Nuokrypis** 

Jei SF yra dvi eilutės, kurių kiekvienoje – keturios prekės, kiekvienos eilutės grynoji suma yra 100,00, o PVM apskaičiuojamas taip: 

1 PVM eilutė = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00. 

2 PVM eilutė = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00. 

Bendras PVM = 25,00 + 25,00 = 50,00 

Bendra SF suma = 200,00 + 50,00 = 250,00.

## <a name="net-amount-per-unit"></a> Grynoji kiekvieno vieneto suma
Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal kiekvieno vieneto vertę, išskyrus bet kokius kitus mokesčius. Kai pasirenkama vienetu paremta Bazinė riba, taip pat turi būti nurodytas PVM kodo Vienetas.

### <a name="example"></a>Pavyzdys

PVM tarifai yra nustatomi toliau nurodytais intervalais.

| Suma             | Mokesčio tarifas |
|--------------------|----------|
| 0 – 50             | 30 %      |
| 50 – 100           | 20 %      |
| 100 – 0 (&gt; 100) | 10 %      |

Bazinė riba: **Grynoji kiekvieno vieneto suma** 

Skaičiavimo metodas: **Visa suma** 

Perkate 8 lempas, kurių kiekviena kainuoja 25,00. 

Grynoji SF eilutės suma yra 200,00. 

Mokestis apskaičiuojamas taip: Vieneto PVM = 25,00 x 30 % = 7,50 Bendras PVM = 7,50 x 8 vienetai = 60,00 Bendroji SF suma = 200,00 + 60,00 = 260,00

## <a name="net-amount-of-invoice-balance"></a> Grynoji SF balanso suma

Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal visą SF vertę, išskyrus bet kokius kitus mokesčius.

### <a name="example"></a>Pavyzdys

PVM tarifai yra nustatomi toliau nurodytais intervalais.

| Suma            | Mokesčio tarifas |
|-------------------|----------|
| 0 – 50            | 30 %      |
| 50 – 100          | 20 %      |
| 100 – 0 (&gt; 100) | 10 %      |

Bazinė riba: **Grynoji SF balanso suma** 

Skaičiavimo metodas: **Intervalas** Pardavimo SF yra 2 eilutės, kurių kiekvienoje – 4 lempos po 25,00 už vienetą. Grynoji SF balanso suma yra 4 x 25,00 + 4 x 25,00 = 200,00. Mokestis apskaičiuojamas taip: Bendras PVM = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Bendra SF suma = 200,00 + 35,00 = 235,00

## <a name="gross-amount-per-line"></a> Bendra suma pagal eilutę

Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal eilutės vertę, įtraukiant visus kitus tos eilutės mokesčius.

> [!NOTE]
> PVM grupėje gali būti tik vienas PVM kodas su šiuo pasirinkimu, atliktu lauke Bazinė riba.

### <a name="example"></a>Pavyzdys

PVM tarifai yra nustatomi toliau nurodytais intervalais.

| Suma             | Mokesčio tarifas |
|--------------------|----------|
| 0 – 50             | 30 %      |
| 50 – 100           | 20 %      |
| 100 – 0 (&gt; 100) | 10 %      |

Bazinė riba: **Bendra suma pagal eilutę** Skaičiavimo metodas: **Intervalas** Dar yra apskaičiuotas kitas mokesčio kodas už specialų muitą – 5,00 už kiekvieną lempą. Prieš skaičiuojant PVM, šis muito mokestis pridedamas prie grynosios sumos. Perkate 8 lempas, kurių kiekviena kainuoja 25,00. Grynoji SF eilutės suma yra 200,00. Bendra SF eilutės suma yra 8 x 25,00 + 8 x 5,00 = 240,00. Mokestis apskaičiuojamas taip: Bendras PVM = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Bendra muito mokesčio suma = 5,00 x 8 = 40,00 Bendra SF suma = 200,00 + 39,00 + 40,00 = 279,00

**Nuokrypis** 

Jei SF sudaro 2 eilutės, kurių kiekvienoje – 4 prekės, grynoji SF eilutės suma yra 100,00. Bendra SF eilutės suma (įskaitant muitą: 4 x 5,00) būtų 120,00, o PVM sukuriamas taip: 1 PVM SF eilutė = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 2 PVM SF eilutė = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Bendras PVM = 27,00 + 27,00 = 54,00 Bendra muito mokesčio suma = 5,00 x 8 = 40,00 Bendra SF suma = 200,00 + 54,00 + 40,00 = 294.00

## <a name="gross-amount-per-unit"></a> Bendra suma pagal vnt.

Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal vieneto vertę, įskaitant visus kitus mokesčius.

> [!NOTE]
> PVM grupėje gali būti tik vienas PVM kodas su šiuo pasirinkimu, atliktu lauke Bazinė riba.

### <a name="example"></a>Pavyzdys

PVM tarifai yra nustatomi toliau nurodytais intervalais.

| Suma             | Mokesčio tarifas |
|--------------------|----------|
| 0 – 50             | 30 %      |
| 50 – 100           | 20 %      |
| 100 – 0 (&gt; 100) | 10 %      |

Bazinė riba: **Bendra suma pagal vnt.** Kiekvienai lempai taikomas specialus 5,00 muito mokestis. Prieš skaičiuojant PVM, šis muito mokestis pridedamas prie grynosios sumos. Perkate 8 lempas, kurių kiekviena kainuoja 25,00. Bendra vieneto suma yra 30,00. Mokestis apskaičiuojamas taip: PVM pagal vnt. = 30 x 30 % = 9,00 Bendras PVM = 9,00 x 8 = 72,00 Bendras muito mokestis = 5,00 x 8 = 40,00 Bendra SF suma = 200,00 + 72,00 + 40,00 = 312,00

## <a name="invoice-total-incl-other-sales-tax-amounts"></a> SF suma, įskaitant kitas PVM sumas

Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal visą SF vertę, įskaitant visus kitus mokesčius.
> [!NOTE]
> PVM grupėje gali būti tik vienas PVM kodas su šiuo pasirinkimu, atliktu lauke Bazinė riba

### <a name="example"></a>Pavyzdys

PVM tarifai yra nustatomi toliau nurodytais intervalais.

| Suma             | Mokesčio tarifas |
|--------------------|----------|
| 0 – 50             | 30 %      |
| 50 – 100           | 20 %      |
| 100 – 0 (&gt; 100) | 10 %      |

Bazinė riba: **SF suma, įskaitant kitas PVM sumas** Skaičiavimo metodas: **Intervalas**   
Kiekvienai lempai taikomas specialus 5,00 muito mokestis. Prieš skaičiuojant PVM, šis muito mokestis pridedamas prie grynosios sumos. Perkate 8 lempas, kurių kiekviena kainuoja 25,00. Grynoji SF suma yra 200,00. Bendra SF suma yra 200,00 + (8 x 5,00) = 240,00. Mokestis apskaičiuojamas taip: Bendras PVM = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Bendra muito mokesčio suma = 5,00 x 8 = 40,00 Bendra SF suma = 200,00 + 39,00 + 40,00 = 279,00

Daugiau informacijos žr. temose [Visa suma ir PVM kodų intervalo skaičiavimo pasirinktys](whole-amount-interval-options-sales-tax-codes.md) ir [PVM skaičiavimo metodai lauke Kilmė](sales-tax-calculation-methods-origin-field.md).





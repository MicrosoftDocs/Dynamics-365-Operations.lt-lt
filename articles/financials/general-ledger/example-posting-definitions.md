---
title: Registravimo aprašai
description: Šiame straipsnyje pateikiami pavyzdžiai, kuriais parodoma, kaip registravimo aprašai naudojami atliekant pirkimo užsakymo biudžeto rezervavimus ir biudžeto asignavimus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09b78a40d3bac5794a66d0ea743f11a27cfacf4e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839334"
---
# <a name="posting-definition-examples"></a>Registravimo aprašų pavyzdžiai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiami pavyzdžiai, kuriais parodoma, kaip registravimo aprašai naudojami atliekant pirkimo užsakymo biudžeto rezervavimus ir biudžeto asignavimus.

Prieš pradėdami skaityti šią temą, turite būti susipažinę su registravimo aprašais ir operacijos registravimo aprašais. Daugiau informacijos žr. [Registravimo aprašai](posting-definitions.md). Toliau pateikti pavyzdžiai gali būti nustatyti puslapyje **Registravimo aprašai**. Kiekviename pavyzdyje yra šie skyriai:

-   Registravimo aprašas – gretinimo kriterijai
-   Registravimo aprašas – sugeneruoti įrašai
-   Operacijos su sąskaitomis, dimensijų vertėmis ir sumomis
-   Pagal registravimo aprašą sugeneruoti DK įrašai

Kai registravimo aprašo ir sąskaitos bei operacijos dimensijų verčių srityje **Gretinimo kriterijai** sugretinamos sąskaitos ir dimensijų vertės, pagal registravimo aprašo sritį **Sugeneruoti įrašai** sugeneruojami didžiosios knygos įrašai. 
> [!NOTE]
> Norėdami susieti registravimo aprašą su konkrečios operacijos tipu, naudokite puslapį **Operacijos registravimo aprašai**. Susiejus registravimo aprašą su operacijos tipu ir puslapyje **DK parametrai** pasirinkus **Naudoti registravimo aprašus**, su visomis pasirinkto tipo operacijomis reikės naudoti registravimo aprašus.

## <a name="example-purchase-order-encumbrances"></a>Pavyzdys: pirkimo užsakymo biudžeto rezervavimas
Kai puslapyje **DK parametrai** pasirinkus **Įgalinti biudžeto rezervavimo procesą** įjungiamas biudžeto rezervavimo apdorojimas, norint įrašyti sąskaitų, kurias reikia rezervuoti, biudžeto rezervavimus į didžiąją knygą reikia naudoti registravimo aprašus. Daugeliu atvejų balanse rezervuojamos visų išlaidų sąskaitos. 

Modulio **Pirkimas** biudžeto rezervavimų registravimo aprašai nustatomi puslapyje **Registravimo aprašai**. Tada puslapio **Operacijos registravimo aprašai** srityje **Pirkimas** galite pasirinkti operacijos tipą **Pirkimo užsakymas**, kad susietumėte registravimo aprašą su pirkimo užsakymais. 

Visos pirkimo užsakymo rezervavimų kvitų operacijos turi būti subalansuotos (t. y. debetas turi būti lygus kreditui) kiekvienoje unikalioje kvito dimensijoje.

### <a name="posting-definition--match-criteria"></a>Registravimo aprašas – gretinimo kriterijai

| Sąskaitos struktūra       | Gretinti sąskaitos numerį | Pirmenybė |
|-------------------------|----------------------|----------|
| Sąskaitos struktūra – pelnas ir nuostolis | \*                   | 1        |

<em>Tuščia vertė lauke **Gretinti sąskaitos numerį</em>* reiškia, kad visos apibrėžtos sąskaitos struktūros sugretintos sąskaitos yra gretinimo taisyklių dalis.

### <a name="posting-definition--generated-entries"></a>Registravimo aprašas – sugeneruoti įrašai

| Sąskaitos struktūra | Sugeneruotas sąskaitos numeris                    | Sugeneruotas debetas / kreditas |
|-------------------|---------------------------------------------|------------------------|
| Likutis           | 300143 - -(biudžeto rezervavimo sąskaita)             | Tas pats                   |
| Likutis           | 300144 - -(biudžeto rezervavimo sąskaitos rezervas) | Pusiausvyros laikymas              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Operacijos su sąskaitomis, dimensijų vertėmis ir sumomis

Sąskaitų ir dimensijų vertės gaunamos iš apskaitos paskirstymų, kuriuos įvedate pirkimo užsakymo eilutėse, arba iš sąskaitų ir dimensijų, automatiškai sugeneruojamų pagal tiekėjų, prekių, kategorijų ir dimensijos šablonų numatytuosius nustatymus.

| Sąskaita + dimensijos           | Debetas  | Kreditas | Komentuoti |
|--------------------------------|--------|--------|---------|
| 606400-OU\_1-OU\_3566-Training | 250,00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Pagal registravimo aprašą sugeneruoti DK įrašai

Sugeneruoti knygos įrašai kuriami siekiant įrašyti į biudžeto rezervavimus.

| Sąskaita + dimensijos           | Debetas  | Kreditas | Komentuoti |
|--------------------------------|--------|--------|---------|
| 300143-OU\_1-OU\_3566-Training | 250,00 |        |         |
| 300144-OU\_1-OU\_3566-Training |        | 250,00 |         |

Šiame pavyzdyje, bet kuri sąskaita, kuri yra srities Sąskaitos struktūra – pelnas ir nuostolis dalis, atitinka registravimo aprašo kriterijus. Todėl, kai įvertinama 606500-OU\_1-OU\_3566-Training, sąskaitose, nurodytose registravimo aprašo srityje **Sugeneruoti įrašai**, sukuriami sugeneruoti įrašai.

## <a name="example-budget-appropriations"></a>Pavyzdys: biudžeto asignavimai
Įjungus biudžeto asignavimą puslapyje **DK parametrai** pasirenkant **Įgalinti biudžeto asignavimą**, biudžeto registro įrašams įrašyti DK reikia naudoti registravimo aprašus. Kai aktyvi ir įjungta biudžeto kontrolės konfigūracija, registravimo aprašus ir operacijos registravimo aprašus galima naudoti, kad būtų palaikomas asignavimų, tikslinimų, perkėlimų, projektų, ilgalaikio turto bei pasiūlos ir paklausos prognozių įrašų įrašymas į didžiąją knygą. 

Norėdami nustatyti biudžeto registravimo įrašų, kurių biudžeto tipas **Pradinis biudžetas** ir kurių asignavimas įjungtas, registravimo aprašą puslapyje **Registravimo aprašai** pasirinkite modulį **Biudžetas**. Tada puslapio **Operacijos registravimo aprašai** srityje **Biudžetas** galite naudoti biudžeto kodus, kad susietumėte registravimo aprašą su biudžeto registro įrašais, kurių biudžeto tipas yra **Pradinis biudžetas**. 

Kai įjungta biudžeto asignavimų ir registravimo aprašų funkcija, biudžeto registro įrašai įrašomi biudžeto kontrolės tikslais ir didžiojoje knygoje.

### <a name="posting-definition--match-criteria"></a>Registravimo aprašas – gretinimo kriterijai

| Sąskaitos struktūra       | Gretinti sąskaitos numerį | Pirmenybė |
|-------------------------|----------------------|----------|
| Sąskaitos struktūra – pelnas ir nuostolis | \*                   | 1        |

<em>Tuščia vertė lauke **Gretinti sąskaitos numerį</em>* reiškia, kad visos apibrėžtos sąskaitos struktūros sugretintos sąskaitos yra gretinimo taisyklių dalis.

### <a name="posting-definition--generated-entries"></a>Registravimo aprašas – sugeneruoti įrašai

| Sąskaitos struktūra | Sugeneruotas sąskaitos numeris              | Sugeneruotas debetas / kreditas |
|-------------------|---------------------------------------|------------------------|
| Sąskaitos struktūra | 300145 - -(įvertintų įplaukų sąskaita) | Tas pats                   |
| Sąskaitos struktūra | 300146 - -(asignavimo sąskaita)     | Pusiausvyros laikymas              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Operacijos su sąskaitomis, dimensijų vertėmis ir sumomis

Galite įvesti biudžeto sąskaitos įrašo sąskaitas, dimensijų vertes ir sumas į puslapį **Biudžeto registro įrašas**.

| Sąskaita + dimensijos           | Debetas | Kreditas | Komentuoti |
|--------------------------------|-------|--------|---------|
| 606400-OU\_1-OU\_3566-Training |       | 250,00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Pagal registravimo aprašą sugeneruoti DK įrašai

Sugeneruoti didžiosios knygos įrašai sukuriami siekiant įrašyti kiekvienos dimensijos pradinį biudžetą.

| Sąskaita + dimensijos           | Debetas  | Kreditas | Komentuoti |
|--------------------------------|--------|--------|---------|
| 300145-OU\_1-OU\_3566-Training |        | 250,00 |         |
| 300146-OU\_1-OU\_3566-Training | 250,00 |        |         |

Šiame pavyzdyje, bet kuri sąskaita, kuri yra srities Sąskaitos struktūra – pelnas ir nuostolis dalis, atitinka registravimo aprašo kriterijus. Todėl, kai įvertinama 606400-OU\_1-OU\_3566-Training, sukuriami sugeneruoti DK įrašai.






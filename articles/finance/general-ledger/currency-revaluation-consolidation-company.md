---
title: Valiutos kurso pasikeitimas konsoliduotoje įmonėje
description: Šioje temoje aprašoma, kaip pakeisti valiutos kursą konsoliduotoje įmonėje.
author: roschlom
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4f2d4e1340e6ed986a1a079a7e88fea3bbe6e1d6af8aee99837adbfe03c39f1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713191"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>Valiutos kurso pasikeitimas konsoliduotoje įmonėje

[!include [banner](../includes/banner.md)]

Konsoliduojant duomenis iš vienos apskaitos valiutos į kitą, vis tiek reikia vykdyti valiutos kurso pakeitimą, jei pasikeitė valiutų kursai, kad sąskaitos balansai būtų tinkamai perkainoti. Pirmą kartą konsoliduodami duomenis, naudodami skirtuką **Valiutos konvertavimas** pasirinkite pradinius valiutos kursus, kurie bus konvertuojami vykdant konsolidavimo procesą. Įvedę naują valiutos kursą (pavyzdžiui, kitą mėnesį), turite perkainoti sąskaitų balansus. Negautas pelnas arba nuostoliai tada atitinkamai atnaujinami atsižvelgiant į naują valiutos kursą ir datą. Šiame pavyzdyje parodyti apskaitos įrašai, sukurti vykdant procesą.

## <a name="company-setup"></a>Įmonės sąranka
-   **Šaltinio / veikianti įmonė (USMF)** – JAV doleriai (USD) naudojami kaip apskaitos ir ataskaitų valiuta.
-   **Konsoliduota įmonės (CON)** – eurai (EUR) naudojami kaip apskaitos ir ataskaitų valiuta.
    -   **Gautas pelnas** – DK sąskaita 801500
    -   **Patirtas nuostolis** – DK sąskaita 801600
    -   **Negautas pelnas** – DK sąskaita 801600
    -   **Nepatirtas nuostolis** – DK sąskaita 801400

## <a name="original-transactions"></a>Pradinės operacijos
### <a name="cash-receipt-transactions-in-usmf"></a>Grynųjų pinigų gavimo operacijos USMF

| Data       | DK sąskaita               | Valiuta | Suma |
|------------|------------------------------|----------|--------|
| 10/11/2015 | 110110 – grynieji                | USD      | 500    |
| 10/11/2015 | 130100 – gautinos sumos | USD      | –500   |

## <a name="exchange-rates"></a>Valiutos kursai

| Iš valiutos | Į valiutą | Pradžios data | Valiutos kursas |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 10/1/2015  | 200           |
| EUR           | USD         | 11/1/2015  | 150           |
| EUR           | USD         | 12/1/2012  | 100           |

## <a name="perform-the-consolidation-for-october-2015"></a>2015 m. spalio konsolidavimas
### <a name="balances-in-the-consolidation-company"></a>Konsoliduotos įmonės balansai

| DK sąskaita | Valiuta | Suma | Skaičiavimas    |
|----------------|----------|--------|----------------|
| 110110         | EUR      | 250    | 500 USD × 50 %  |
| 130100         | EUR      | –250   | –500 USD × 50 % |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. lapkričio 30 d. valiutos kursą
### <a name="balances-in-the-consolidation-company"></a>Konsoliduotos įmonės balansai

| DK sąskaita | Valiuta | Suma  | Skaičiavimas                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR      | 333.33  | Pradinė suma 500 × 66,6667 %  |
| 130100         | EUR      | –333,33 | Pradinė suma –500 × 66,6667 % |
| 801400         | EUR      | 83.33   | 333,33 – 250                       |
| 801600         | EUR      | –83,33  | -333,33 – (–250)                   |

Matysite papildomas ataskaitų valiutos sumų operacijas.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>Pakeisti sąskaitų nuo 2015 m. spalio 1 d. iki 2015 m. gruodžio 31 d. valiutos kursą
### <a name="balances-in-the-consolidation-company"></a>Konsoliduotos įmonės balansai

| DK sąskaita | Valiuta | Suma  | Skaičiavimas                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR      | 500,00  | Pradinė suma 500 × 1                           |
| 130100         | EUR      | –500,00 | Pradinė suma –500 × 1                          |
| 801400         | EUR      | 250     | 500 – 333,33 = 166,67 166,67 + 83,33 = 250           |
| 801600         | EUR      | –250    | -500 – (–333,33) = –166,67 – 166,67 + (–83,33) = –250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
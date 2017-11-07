---
title: "Mokėtinų sumų centralizuoti mokėjimai"
description: "Organizacijos, sudarytos iš kelių juridinių subjektų, gali kurti ir valdyti mokėjimus naudodamos vieną juridinį subjektą, kuris tvarko visus mokėjimus. Todėl to pačio mokėjimo nereikia įvesti į kelis juridinius subjektus. Šiame straipsnyje pateikti pavyzdžiai, parodantys, kaip įvairių scenarijų atvejais atliekamas centralizuotų mokėjimų registravimas."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 49d5242168cd43e78dd4b0c63da363f91f680904
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="centralized-payments-for-accounts-payable"></a>Mokėtinų sumų centralizuoti mokėjimai

[!include[banner](../includes/banner.md)]


Organizacijos, sudarytos iš kelių juridinių subjektų, gali kurti ir valdyti mokėjimus naudodamos vieną juridinį subjektą, kuris tvarko visus mokėjimus. Todėl to pačio mokėjimo nereikia įvesti į kelis juridinius subjektus. Šiame straipsnyje pateikti pavyzdžiai, parodantys, kaip įvairių scenarijų atvejais atliekamas centralizuotų mokėjimų registravimas.

Organizacijos, sudarytos iš kelių juridinių subjektų, gali kurti ir valdyti mokėjimus naudodamos juridinį subjektą, kuris tvarko visus mokėjimus. Todėl to pačio mokėjimo nereikia įvesti į kelis juridinius subjektus. Be to, organizacija sutaupo laiko, nes mokėjimo procesas yra supaprastinamas.

Centralizuotų mokėjimų organizacijoje yra daug operacijų juridinių subjektų, o kiekvienas veikiantis juridinis subjektas valdo savo tiekėjo SF. Visų veikiančių juridinių subjektų mokėjimai yra generuojami iš vieno juridinio subjekto, kuris vadinamas mokėjimo juridiniu subjektu. Atsiskaitymo proceso metu generuojamos taikomos mokėjimų ir mokėjimų priėmimo operacijos. Galite nurodyti, kuris organizacijos juridinis subjektas gaus patirto pelno ar patirto nuostolio operacijas, ir kaip tvarkomos su visos įmonės mokėjimu susijusios mokėjimo nuolaidų operacijos. 

Toliau pateiktame pavyzdyje parodyta, kaip atliekamas registravimas įvairių scenarijų atvejais. Ši konfigūracija naudojama visų toliau nurodytų pavyzdžių atvejais.

-   Juridiniai subjektai yra Fabrikam, Fabrikam East ir Fabrikam West. Mokėjimai atliekami iš „Fabrikam“.
-   Laukas **Registruoti mokėjimo nuolaidą**, esantis **Vidinės įmonės apskaitos** puslapyje, nustatytas į **SF juridinis subjektas**.
-   Laukas **Registruoti valiutos kurso pelną arba nuostolį**, esantis **Vidinės įmonės apskaitos** puslapyje, nustatytas į **Mokėjimo juridinis subjektas**.
-   Tiekėjas „Fourth Coffee ‟ kaip tiekėjas nustatytas kiekviename juridiniame subjekte. Tiekėjai iš įvairių juridinių subjektų identifikuojami kaip tas pats tiekėjas, nes jų visuotinės adresų knygelės ID yra toks pats.

| Katalogo ID | Tiekėjo kodas | Vardas          | Juridinis subjektas  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Fourth Coffee | Fabrikam      |
| 1050         | 100            | Fourth Coffee | Fabrikam East |
| 1050         | 3004           | Fourth Coffee | Fabrikam West |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>1 pavyzdys: tiekėjo SF mokėjimas iš kito juridinio subjekto
Fabrikam East turi atvirą tiekėjo 100, Fourth Coffee, SF. Fabrikam įveda ir užregistruoja mokėjimą į Fabrikam tiekėjo sąskaitą 3004, Fourth Coffee. Mokėjimas yra sudengiamas su atvira SF.

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>Įmonėje Fabrikam East registruojama tiekėjo 100 SF

| Sąskaita                          | Debeto suma | Kredito suma |
|----------------------------------|--------------|---------------|
| Išlaidos (Fabrikam East)          | 600,00       |               |
| Mokėtinos sumos (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Mokėjimas sugeneruotas ir užregistruotas 3004 tiekėjui įmonėje Fabrikam

| Sąskaita                     | Debeto suma | Kredito suma |
|-----------------------------|--------------|---------------|
| Mokėtinos sumos (Fabrikam) | 600,00       |               |
| Grynieji pinigai (Fabrikam)             |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam mokėjimas sudengtas su Fabrikam East sąskaita faktūra

**Fabrikam registravimas**

| Sąskaita                           | Debeto suma | Kredito suma |
|-----------------------------------|--------------|---------------|
| Mokėtojas – Fabrikam East (Fabrikam) | 600,00       |               |
| Mokėtinos sumos (Fabrikam)       |              | 600,00        |

**Fabrikam East registravimas**

| Sąskaita                          | Debeto suma | Kredito suma |
|----------------------------------|--------------|---------------|
| Mokėtinos sumos (Fabrikam East) | 600,00       |               |
| Mokėtojas – Fabrikam (Fabrikam East)  |              | 600,00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>2 pavyzdys: Tiekėjo SF mokėjimas iš kito juridinio subjekto su mokėjimo nuolaida
Fabrikam East turi tiekėjo 100, Fourth Coffee, atvirą SF. SF galima 20,00 dydžio mokėjimo nuolaida. Fabrikam įveda ir užregistruoja 580,00 dydžio mokėjimą Fabrikam tiekėjui 3004, Fourth Coffee. Mokėjimas yra sudengiamas su atviromis Fabrikam East SF. Mokėjimo nuolaida yra užregistruojama SF juridiniame subjekte, Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Sąskaita faktūra užregistruota Fabrikam East 100 tiekėjui įmonėje Fabrikam East

| Sąskaita                          | Debeto suma | Kredito suma |
|----------------------------------|--------------|---------------|
| Išlaidos (Fabrikam East)          | 600,00       |               |
| Mokėtinos sumos (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Mokėjimas sugeneruotas ir užregistruotas Fabrikam 3004 tiekėjui įmonėje Fabrikam

| Sąskaita                     | Debeto suma | Kredito suma |
|-----------------------------|--------------|---------------|
| Mokėtinos sumos (Fabrikam) | 580,00       |               |
| Grynieji pinigai (Fabrikam)             |              | 580,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam mokėjimas sudengtas su Fabrikam East sąskaita faktūra

**Fabrikam registravimas**

| Sąskaita                           | Debeto suma | Kredito suma |
|-----------------------------------|--------------|---------------|
| Mokėtojas – Fabrikam East (Fabrikam) | 580,00       |               |
| Mokėtinos sumos (Fabrikam)       |              | 580,00        |

**Fabrikam East registravimas**

| Sąskaita                          | Debeto suma | Kredito suma |
|----------------------------------|--------------|---------------|
| Mokėtinos sumos (Fabrikam East) | 580,00       |               |
| Mokėtojas – Fabrikam (Fabrikam East)  |              | 580,00        |
| Mokėtinos sumos (Fabrikam East) | 20,00        |               |
| Mokėjimo nuolaida (Fabrikam East)    |              | 20,00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>3 pavyzdys: Tiekėjo SF mokėjimas iš kito juridinio subjekto taikant patirtą valiutos kurso nuostolį
Fabrikam East turi tiekėjo 100, Fourth Coffee, atvirą SF. Fabrikam įveda ir užregistruoja mokėjimą Fabrikam tiekėjui 3004, Fourth Coffee. Mokėjimas yra sudengiamas su atvira Fabrikam East SF. Sudengimo proceso metu sugeneruojama valiutos keitimo nuostolio operacija.

-   Sąskaitos faktūros išrašymo dieną euro (EUR) ir JAV dolerio (USD) valiutos kurso santykis: 1,2062
-   Mokėjimo dieną EUR ir USD valiutos kurso santykis: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Sąskaita faktūra užregistruota Fabrikam East 100 tiekėjui įmonėje Fabrikam East

| Sąskaita                          | Debeto suma            | Kredito suma           |
|----------------------------------|-------------------------|-------------------------|
| Išlaidos (Fabrikam East)          | 600,00 EUR / 723,72 USD |                         |
| Mokėtinos sumos (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Mokėjimas sugeneruotas ir užregistruotas Fabrikam 3004 tiekėjui įmonėje Fabrikam

| Sąskaita                     | Debeto suma            | Kredito suma           |
|-----------------------------|-------------------------|-------------------------|
| Mokėtinos sumos (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Grynieji pinigai (Fabrikam)             |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam mokėjimas sudengtas su Fabrikam East sąskaita faktūra

**Fabrikam registravimas**

| Sąskaita                           | Debeto suma            | Kredito suma           |
|-----------------------------------|-------------------------|-------------------------|
| Mokėtojas – Fabrikam East (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Mokėtinos sumos (Fabrikam)       |                         | 600,00 EUR / 736,62 USD |
| Patirtas nuostolis (Fabrikam)          | 0,00 EUR / 12,90 USD    |                         |
| Mokėtojas – Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,90 USD    |

**Fabrikam East registravimas**

| Sąskaita                          | Debeto suma            | Kredito suma           |
|----------------------------------|-------------------------|-------------------------|
| Mokėtinos sumos (Fabrikam East) | 600,00 EUR / 736,62 USD |                         |
| Mokėtojas – Fabrikam (Fabrikam East)  |                         | 600,00 EUR / 736,62 USD |
| Mokėtojas – Fabrikam (Fabrikam East)  | 0,00 EUR / 12,90 USD    |                         |
| Mokėtinos sumos (Fabrikam East) |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>4 pavyzdys: Tiekėjo SF mokėjimas iš kito juridinio subjekto, taikant mokėjimo nuolaidą ir patirtą valiutos kurso nuostolį
Fabrikam East turi tiekėjo 100, Fourth Coffee, atvirą SF. SF galima mokėjimo nuolaida, ir sugeneruojama PVM operacija. „Fabrikam“ užregistruoja mokėjimą „Fabrikam“ tiekėjui 3004, „Fourth Coffee“. Mokėjimas sudengiamas su atvira Fabrikam East SF. Sudengimo proceso metu sugeneruojama valiutos keitimo nuostolio operacija. Mokėjimo nuolaida užregistruojama SF juridiniame subjekte („Fabrikam East“), o valiutos keitimo nuostolis užregistruojamas mokėjimo juridiniame subjekte („Fabrikam“).

-   Sąskaitos faktūros išrašymo dieną EUR ir USD valiutos kurso santykis: 1,2062
-   Mokėjimo dieną EUR ir USD valiutos kurso santykis: 1,2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>SF užregistruota ir mokesčių operacija sugeneruota tiekėjui 100 įmonėje Fabrikam East

| Sąskaita                          | Debeto suma            | Kredito suma           |
|----------------------------------|-------------------------|-------------------------|
| Išlaidos (Fabrikam East)          | 564,07 EUR / 680,38 USD |                         |
| PVM (Fabrikam East)        | 35,93 EUR / 43,34 USD   |                         |
| Mokėtinos sumos (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Mokėjimas sugeneruotas ir užregistruotas 3004 tiekėjui įmonėje Fabrikam

| Sąskaita                     | Debeto suma            | Kredito suma           |
|-----------------------------|-------------------------|-------------------------|
| Mokėtinos sumos (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Grynieji pinigai (Fabrikam East)        |                         | 588,72 EUR / 722,77 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam mokėjimas sudengtas su Fabrikam East sąskaita faktūra

**Fabrikam registravimas**

| Sąskaita                           | Debeto suma            | Kredito suma           |
|-----------------------------------|-------------------------|-------------------------|
| Mokėtojas – Fabrikam East (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Mokėtinos sumos (Fabrikam)       |                         | 588,72 EUR / 722,77 USD |
| Patirtas nuostolis (Fabrikam)          | 0,00 EUR / 12,66 USD    |                         |
| Mokėtojas – Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,66 USD    |

**Fabrikam East registravimas**

| Sąskaita                          | Debeto suma            | Kredito suma           |
|----------------------------------|-------------------------|-------------------------|
| Mokėtinos sumos (Fabrikam East) | 588,72 EUR / 722,77 USD |                         |
| Mokėtojas – Fabrikam (Fabrikam East)  |                         | 588,72 EUR / 722,77 USD |
| Mokėti įmonei Fabrikam (Fabrikam East)   | 0,00 EUR / 12,66 USD    |                         |
| Mokėtinos sumos (Fabrikam East) |                         | 0,00 EUR / 12,66 USD    |
| Mokėtinos sumos (Fabrikam East) | 11,28 EUR / 13,61 USD   |                         |
| Mokėjimo nuolaida (Fabrikam East)    |                         | 11,28 EUR / 13,61 USD   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>5 pavyzdys: Tiekėjo kredito pažyma taikant pirminį mokėjimą
Fabrikam sugeneruoja 75,00 dydžio mokėjimą tiekėjui 3004, Fourth Coffee. Mokėjimas yra sudengiamas su Fabrikam West tiekėjo 3004 atvira SF ir Fabrikam East tiekėjo 100 atvira kredito pažyma. Mokėjimas puslapyje **Operacijų sudengimas** yra pažymimas kaip pirminis mokėjimas.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Sąskaita faktūra užregistruota 3004 tiekėjui įmonėje Fabrikam West

| Paskyra                          | Debeto suma | Kredito suma |
|----------------------------------|--------------|---------------|
| Išlaidos (Fabrikam West)          | 100,00       |               |
| Mokėtinos sumos (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kredito pažyma užregistruota 100 tiekėjui įmonėje Fabrikam East

| Sąskaita                          | Debeto suma | Kredito suma |
|----------------------------------|--------------|---------------|
| Mokėtinos sumos (Fabrikam East) | 25,00        |               |
| Pirkimų grąžinimai (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Mokėjimas užregistruotas 3004 tiekėjui įmonėje Fabrikam

| Sąskaita                     | Debeto suma | Kredito suma |
|-----------------------------|--------------|---------------|
| Mokėtinos sumos (Fabrikam) | 75,00        |               |
| Grynieji pinigai (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam mokėjimas sudengtas su Fabrikam West SF ir Fabrikam East kredito pažyma

**Fabrikam registravimas**

| Sąskaita                           | Debeto suma | Kredito suma |
|-----------------------------------|--------------|---------------|
| Mokėtinos sumos (Fabrikam)       | 25,00        |               |
| Mokėti Fabrikam East (Fabrikam)   |              | 25,00         |
| Mokėtojas – Fabrikam West (Fabrikam) | 100,00       |               |
| Mokėtinos sumos (Fabrikam)       |              | 100,00        |

**Fabrikam East registravimas**

| Sąskaita                           | Debeto suma | Kredito suma |
|-----------------------------------|--------------|---------------|
| Mokėtojas – Fabrikam (Fabrikam East) | 25,00        |               |
| Mokėtinos sumos (Fabrikam East)  |              | 25,00         |

**Fabrikam West registravimas**

| Sąskaita                          | Debeto suma | Kredito suma |
|----------------------------------|--------------|---------------|
| Mokėtinos sumos (Fabrikam West) | 100,00       |               |
| Mokėti Fabrikam (Fabrikam West)  |              | 100,00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>6 pavyzdys: Tiekėjo kredito pažyma netaikant pirminio mokėjimo
Fabrikam sugeneruoja 75,00 dydžio mokėjimą tiekėjui 3004, Fourth Coffee. Mokėjimas yra sudengiamas su Fabrikam West tiekėjo 3004 atvira SF ir Fabrikam East tiekėjo 100 atvira kredito pažyma. Mokėjimas puslapyje **Operacijų sudengimas** nėra pažymimas kaip pirminis mokėjimas.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Sąskaita faktūra užregistruota 3004 tiekėjui įmonėje Fabrikam West

| Paskyra                          | Debeto suma | Kredito suma |
|----------------------------------|--------------|---------------|
| Išlaidos (Fabrikam West)          | 100,00       |               |
| Mokėtinos sumos (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kredito pažyma užregistruota 100 tiekėjui įmonėje Fabrikam East

| Sąskaita                          | Debeto suma | Kredito suma |
|----------------------------------|--------------|---------------|
| Mokėtinos sumos (Fabrikam East) | 25,00        |               |
| Pirkimų grąžinimai (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Mokėjimas užregistruotas 3004 tiekėjui įmonėje Fabrikam

| Sąskaita                     | Debeto suma | Kredito suma |
|-----------------------------|--------------|---------------|
| Mokėtinos sumos (Fabrikam) | 75,00        |               |
| Grynieji pinigai (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam mokėjimas sudengtas su Fabrikam West SF ir Fabrikam East kredito pažyma

**Fabrikam registravimas**

| Sąskaita                           | Debeto suma | Kredito suma |
|-----------------------------------|--------------|---------------|
| Mokėtojas – Fabrikam West (Fabrikam) | 75,00        |               |
| Mokėtinos sumos (Fabrikam)       |              | 75,00         |

**Fabrikam East registravimas**

| Sąskaita                                | Debeto suma | Kredito suma |
|----------------------------------------|--------------|---------------|
| Moka įmonė Fabrikam West (Fabrikam East) | 25,00        |               |
| Mokėtinos sumos (Fabrikam East)       |              | 25,00         |

**Fabrikam West registravimas**

| Sąskaita                              | Debeto suma | Kredito suma |
|--------------------------------------|--------------|---------------|
| Mokėtinos sumos (Fabrikam West)     | 75,00        |               |
| Mokėti Fabrikam (Fabrikam West)      |              | 75,00         |
| Mokėtinos sumos (Fabrikam West)     | 25,00        |               |
| Mokėti įmonei Fabrikam East (Fabrikam West) |              | 25,00         |







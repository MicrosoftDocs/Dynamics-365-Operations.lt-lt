---
title: Gautinų sumų centralizuoti mokėjimai
description: Organizacijos, sudarytos iš kelių juridinių subjektų, gali kurti ir valdyti mokėjimus naudodamos vieną juridinį subjektą, kuris tvarko visus mokėjimus. Todėl tos pačios operacijos nereikia įvesti į kelis juridinius subjektus. Šiame straipsnyje pateikti pavyzdžiai, parodantys, kaip įvairių scenarijų atvejais atliekamas centralizuotų mokėjimų registravimas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 644ef7cc9535522b72b03ba81a72b1070c8e2ba1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993044"
---
# <a name="centralized-payments-for-accounts-receivable"></a>Gautinų sumų centralizuoti mokėjimai

[!include [banner](../includes/banner.md)]

Organizacijos, sudarytos iš kelių juridinių subjektų, gali kurti ir valdyti mokėjimus naudodamos vieną juridinį subjektą, kuris tvarko visus mokėjimus. Todėl tos pačios operacijos nereikia įvesti į kelis juridinius subjektus. Šiame straipsnyje pateikti pavyzdžiai, parodantys, kaip įvairių scenarijų atvejais atliekamas centralizuotų mokėjimų registravimas.

Organizacijos, sudarytos iš kelių juridinių subjektų, gali kurti ir valdyti mokėjimus naudodamos juridinį subjektą, kuris tvarko visus mokėjimus. Todėl tos pačios operacijos nereikia įvesti į kelis juridinius subjektus. Be to, organizacija sutaupo laiko, nes supaprastinami mokėjimo pasiūlymų, sudengimų ir atidarytų bei uždarytų centralizuotų mokėjimų operacijų redagavimo procesai. 

Centralizuotų mokėjimų organizacijoje yra daug operacijų juridinių subjektų, ir kiekvienas veikiantis juridinis subjektas valdo savo gautinų SF informaciją. Visų veikiančių juridinių subjektų mokėjimus gauna vienas juridinis subjektas, kuris vadinamas mokėjimo juridiniu subjektu. Atsiskaitymo proceso metu generuojamos taikomos mokėjimų ir mokėjimų priėmimo operacijos. Galite nurodyti, kuris organizacijos juridinis subjektas gauna patirto pelno ar patirto nuostolio operacijas, ir kaip tvarkomos su centralizuotu mokėjimu susijusios mokėjimo nuolaidų operacijos. Centralizuoto mokėjimo žurnalo eilutės lauke **Sąskaitos tipas** turi būti nustatyta reikšmė Klientas. Lauke **Korespondentinės sąskaitos tipas** turi būti nustatyta reikšmė Bankas arba DK. Banko sąskaita turi būti esamoje įmonėje. 

Toliau pateiktame pavyzdyje parodyta, kaip atliekamas registravimas įvairių scenarijų atvejais. Ši konfigūracija naudojama visų toliau nurodytų pavyzdžių atvejais.

-   Juridiniai subjektai yra Fabrikam, Fabrikam East ir Fabrikam West. Klientų mokėjimai įvedami į Fabrikam.
-   Laukas **Registruoti mokėjimo nuolaidą**, esantis **Vidinės įmonės apskaitos** puslapyje, nustatytas į **SF juridinis subjektas**.
-   Laukas **Registruoti valiutos kurso pelną arba nuostolį**, esantis **Vidinės įmonės apskaitos** puslapyje, nustatytas į **Mokėjimo juridinis subjektas**.
-   Klientas „Northwind Traders‟ kaip klientas nustatytas kiekviename juridiniame subjekte. Klientai iš įvairių juridinių subjektų identifikuojami kaip tas pats klientas, nes jų yra toks pats visuotinės adresų knygelės ID.

| Adresų knygelės ID | Kliento sąskaita | Vardas              | Juridinis subjektas  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Northwind Traders | Fabrikam      |
| 4050            | 4000             | Northwind Traders | Fabrikam East |
| 4050            | 10000            | Northwind Traders | Fabrikam West |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>1 pavyzdys: Kliento SF mokėjimas iš kito juridinio subjekto
Fabrikam gauna 600,00 dydžio mokėjimą iš Fabrikam kliento sąskaitos 4000, Northwind Traders. Mokėjimas sudengiamas su kliento sąskaita 4000, Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>Įmonėje Fabrikam East registruojama kliento 4000 SF

| Sąskaita                             | Debeto suma | Kredito suma |
|-------------------------------------|--------------|---------------|
| Gautinos sumos (Fabrikam East) | 600,00       |               |
| Pardavimas (Fabrikam East)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Mokėjimas gautas ir užregistruotas 4000 klientui įmonėje Fabrikam

| Sąskaita                        | Debeto suma | Kredito suma |
|--------------------------------|--------------|---------------|
| Grynieji pinigai (Fabrikam)                | 600,00       |               |
| Gautinos sumos (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam mokėjimas sudengtas su Fabrikam East sąskaita faktūra

**Fabrikam registravimas**

| Sąskaita                         | Debeto suma | Kredito suma |
|---------------------------------|--------------|---------------|
| Gautinos sumos (Fabrikam)  | 600,00       |               |
| Mokėti Fabrikam East (Fabrikam) |              | 600,00        |

**Fabrikam East registravimas**

| Sąskaita                             | Debeto suma | Kredito suma |
|-------------------------------------|--------------|---------------|
| Mokėtojas – Fabrikam (Fabrikam East)   | 600,00       |               |
| Gautinos sumos (Fabrikam East) |              | 600,00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>2 pavyzdys: Kliento SF mokėjimas iš kito juridinio subjekto su mokėjimo nuolaida
Fabrikam gauna 580,00 dydžio mokėjimą iš Fabrikam kliento 4000, Northwind Traders. Fabrikam East turi atidarytą 4000 kliento SF. SF galima 20,00 dydžio mokėjimo nuolaida. Mokėjimas yra sudengiamas su atviromis Fabrikam East SF. Mokėjimo nuolaida yra užregistruojama SF juridiniame subjekte, Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Sąskaita faktūra užregistruota Fabrikam East 4000 klientui įmonėje Fabrikam East

| Sąskaita                             | Debeto suma | Kredito suma |
|-------------------------------------|--------------|---------------|
| Gautinos sumos (Fabrikam East) | 580.00       |               |
| Pardavimas (Fabrikam East)               |              | 580.00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Mokėjimas gautas ir užregistruotas Fabrikam 4000 klientui įmonėje Fabrikam

| Sąskaita                        | Debeto suma | Kredito suma |
|--------------------------------|--------------|---------------|
| Grynieji pinigai (Fabrikam)                | 600,00       |               |
| Gautinos sumos (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam mokėjimas sudengtas su Fabrikam East sąskaita faktūra

**Fabrikam registravimas**

| Sąskaita                         | Debeto suma | Kredito suma |
|---------------------------------|--------------|---------------|
| Gautinos sumos (Fabrikam)  | 580,00       |               |
| Mokėti Fabrikam East (Fabrikam) |              | 580,00        |

**Fabrikam East registravimas**

| Sąskaita                             | Debeto suma | Kredito suma |
|-------------------------------------|--------------|---------------|
| Mokėtojas – Fabrikam (Fabrikam East)   | 580,00       |               |
| Gautinos sumos (Fabrikam East) |              | 580,00        |
| Mokėjimo nuolaida (Fabrikam East)       | 20,00        |               |
| Gautinos sumos (Fabrikam East) |              | 20,00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>3 pavyzdys: Kliento SF mokėjimas iš kito juridinio subjekto taikant įvykdytą valiutos kurso pelną
Fabrikam gauna 600,00 eurų (EUR) mokėjimą iš Fabrikam 4000 kliento, „Northwind Traders‟. Mokėjimas sudengiamas su kliento 4000 iš Fabrikam East atvira SF. Sudengimo proceso metu sugeneruojama valiutos keitimo pelno operacija.

-   Sąskaitos faktūros išrašymo dieną EUR ir JAV dolerio (USD) valiutos kurso santykis: 1,2062
-   Mokėjimo dieną EUR ir USD valiutos kurso santykis: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Sąskaita faktūra užregistruota Fabrikam East 4000 klientui įmonėje Fabrikam East

| Sąskaita                             | Debeto suma            | Kredito suma           |
|-------------------------------------|-------------------------|-------------------------|
| Gautinos sumos (Fabrikam East) | 600,00 EUR / 723,72 USD |                         |
| Pardavimas (Fabrikam East)               |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Mokėjimas gautas ir užregistruotas Fabrikam 4000 klientui įmonėje Fabrikam

| Sąskaita                        | Debeto suma            | Kredito suma           |
|--------------------------------|-------------------------|-------------------------|
| Grynieji pinigai (Fabrikam)                | 600,00 EUR / 736,62 USD |                         |
| Gautinos sumos (Fabrikam) |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam mokėjimas sudengtas su Fabrikam East sąskaita faktūra

**Fabrikam registravimas**

| Sąskaita                         | Debeto suma            | Kredito suma           |
|---------------------------------|-------------------------|-------------------------|
| Gautinos sumos (Fabrikam)  | 600,00 EUR / 736,62 USD |                         |
| Mokėti Fabrikam East (Fabrikam) |                         | 600,00 EUR / 736,62 USD |
| Mokėti Fabrikam East (Fabrikam) | 0,00 EUR / 12,90 USD    |                         |
| Gautas pelnas (Fabrikam)        |                         | 0,00 EUR / 12,90 USD    |

**Fabrikam East registravimas**

| Sąskaita                             | Debeto suma            | Kredito suma           |
|-------------------------------------|-------------------------|-------------------------|
| Mokėtojas – Fabrikam (Fabrikam East)   | 600,00 EUR / 736,62 USD |                         |
| Gautinos sumos (Fabrikam East) |                         | 600,00 EUR / 736,62 USD |
| Gautinos sumos (Fabrikam East) | 0,00 EUR / 12,90 USD    |                         |
| Mokėtojas – Fabrikam (Fabrikam East)   |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>4 pavyzdys: Kliento SF mokėjimas iš kito juridinio subjekto, taikant mokėjimo nuolaidą ir įvykdytą valiutos kurso pelną
Fabrikam užregistruoja Fabrikam kliento 4000, Northwind Traders, atviros SF mokėjimą įmonėje Fabrikam East. SF galima mokėjimo nuolaida, ir sugeneruojama PVM operacija. Mokėjimas sudengiamas su atvira Fabrikam East SF. Sudengimo proceso metu sugeneruojama valiutos keitimo pelno operacija. Mokėjimo nuolaida užregistruojama SF juridiniame subjekte (Fabrikam East), o valiutos kurso pelnas užregistruojamas mokėjimo juridiniame subjekte (Fabrikam).

-   Sąskaitos faktūros išrašymo dieną EUR ir USD valiutos kurso santykis: 1,2062
-   Mokėjimo dieną EUR ir USD valiutos kurso santykis: 1,2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>Registruojama laisvos formos SF ir sugeneruojama kliento 4000 mokesčių operacija įmonėje Fabrikam East

| Sąskaita                             | Debeto suma            | Kredito suma           |
|-------------------------------------|-------------------------|-------------------------|
| Gautinos sumos (Fabrikam East) | 638,22 EUR / 769,82 USD |                         |
| Pardavimas (Fabrikam East)               |                         | 600,00 EUR / 723,72 USD |
| PVM (Fabrikam East)           |                         | 38,22 EUR / 46,10 USD   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Mokėjimas gautas ir užregistruotas 4000 klientui įmonėje Fabrikam

| Sąskaita                        | Debeto suma            | Kredito suma           |
|--------------------------------|-------------------------|-------------------------|
| Grynieji pinigai (Fabrikam)                | 626,22 EUR / 768,81 USD |                         |
| Gautinos sumos (Fabrikam) |                         | 626,22 EUR / 768,81 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam mokėjimas sudengtas su Fabrikam East sąskaita faktūra

**Fabrikam registravimas**

| Sąskaita                         | Debeto suma            | Kredito suma           |
|---------------------------------|-------------------------|-------------------------|
| Gautinos sumos (Fabrikam)  | 626,22 EUR / 768,81 USD |                         |
| Mokėti Fabrikam East (Fabrikam) |                         | 626,22 EUR / 768,81 USD |
| Mokėti Fabrikam East (Fabrikam) | 0,00 EUR / 13,46 USD    |                         |
| Gautas pelnas (Fabrikam)        |                         | 0,00 EUR / 13,46 USD    |

**Fabrikam East registravimas**

| Sąskaita                             | Debeto suma            | Kredito suma           |
|-------------------------------------|-------------------------|-------------------------|
| Mokėtojas – Fabrikam (Fabrikam East)   | 626,22 EUR / 768,81 USD |                         |
| Gautinos sumos (Fabrikam East) |                         | 626,22 EUR / 768,81 USD |
| Gautinos sumos (Fabrikam East)  | 0,00 EUR / 13,46 USD    |                         |
| Mokėtojas – Fabrikam (Fabrikam East)   |                         | 0,00 EUR / 13,46 USD    |
| Mokėjimo nuolaida (Fabrikam East)       | 12,00 EUR / 14,47 USD   |                         |
| Gautinos sumos (Fabrikam East) |                         | 12,00 EUR / 14,47 USD   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>5 pavyzdys: Kliento kredito pažyma taikant pirminį mokėjimą
Fabrikam gauna 75,00 mokėjimą iš kliento 4000, Northwind Traders. Mokėjimas yra sudengiamas su Fabrikam West kliento 10 000 atvira SF ir Fabrikam East kliento 4000 atvira kredito pažyma. Mokėjimas puslapyje **Operacijų sudengimas** yra pažymimas kaip pirminis mokėjimas.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Sąskaita faktūra užregistruota 10000 klientui įmonėje Fabrikam West

| Paskyra                             | Debeto suma | Kredito suma |
|-------------------------------------|--------------|---------------|
| Gautinos sumos (Fabrikam West) | 100,00       |               |
| Pardavimas (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kredito pažyma užregistruota 4000 klientui įmonėje Fabrikam East

| Sąskaita                             | Debeto suma | Kredito suma |
|-------------------------------------|--------------|---------------|
| Pardavimo grąžinimai (Fabrikam East)       | 25,00        |               |
| Gautinos sumos (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Mokėjimas užregistruotas 4000 klientui įmonėje Fabrikam

| Sąskaita                        | Debeto suma | Kredito suma |
|--------------------------------|--------------|---------------|
| Grynieji pinigai (Fabrikam)                | 75,00        |               |
| Gautinos sumos (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam mokėjimas sudengtas su Fabrikam West SF ir Fabrikam East kredito pažyma

**Fabrikam registravimas**

| Sąskaita                           | Debeto suma | Kredito suma |
|-----------------------------------|--------------|---------------|
| Mokėtojas – Fabrikam East (Fabrikam) | 25,00        |               |
| Gautinos sumos (Fabrikam)    |              | 25,00         |
| Gautinos sumos (Fabrikam)    | 100,00       |               |
| Mokėti Fabrikam West (Fabrikam)   |              | 100,00        |

**Fabrikam East registravimas**

| Sąskaita                             | Debeto suma | Kredito suma |
|-------------------------------------|--------------|---------------|
| Gautinos sumos (Fabrikam East) | 25,00        |               |
| Mokėtojas – Fabrikam (Fabrikam East)     |              | 25,00         |

**Fabrikam West registravimas**

| Sąskaita                             | Debeto suma | Kredito suma |
|-------------------------------------|--------------|---------------|
| Mokėtojas – Fabrikam (Fabrikam West)   | 100,00       |               |
| Gautinos sumos (Fabrikam West) |              | 100,00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>6 pavyzdys: Kliento kredito pažyma netaikant pirminio mokėjimo
Fabrikam gauna 75,00 dydžio mokėjimą iš kliento 4000, Northwind Traders. Mokėjimas yra sudengiamas su Fabrikam West kliento 10 000 atvira SF ir Fabrikam East kliento 4000 atvira kredito pažyma. Mokėjimas puslapyje **Operacijų sudengimas** nėra pažymimas kaip pirminis mokėjimas.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Sąskaita faktūra užregistruota 10000 klientui įmonėje Fabrikam West

| Paskyra                             | Debeto suma | Kredito suma |
|-------------------------------------|--------------|---------------|
| Gautinos sumos (Fabrikam West) | 100,00       |               |
| Pardavimas (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kredito pažyma užregistruota 4000 klientui įmonėje Fabrikam East

| Sąskaita                             | Debeto suma | Kredito suma |
|-------------------------------------|--------------|---------------|
| Pardavimo grąžinimai (Fabrikam East)       | 25,00        |               |
| Gautinos sumos (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Mokėjimas užregistruotas 4000 klientui įmonėje Fabrikam

| Sąskaita                        | Debeto suma | Kredito suma |
|--------------------------------|--------------|---------------|
| Grynieji pinigai (Fabrikam)                | 75,00        |               |
| Gautinos sumos (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam mokėjimas sudengtas su Fabrikam West SF ir Fabrikam East kredito pažyma

**Fabrikam registravimas**

| Sąskaita                         | Debeto suma | Kredito suma |
|---------------------------------|--------------|---------------|
| Gautinos sumos (Fabrikam)  | 75,00        |               |
| Mokėti Fabrikam West (Fabrikam) |              | 75,00         |

**Fabrikam East registravimas**

| Sąskaita                              | Debeto suma | Kredito suma |
|--------------------------------------|--------------|---------------|
| Gautinos sumos (Fabrikam East)  | 25,00        |               |
| Mokėti įmonei Fabrikam West (Fabrikam East) |              | 25,00         |

**Fabrikam West registravimas**

| Sąskaita                                | Debeto suma | Kredito suma |
|----------------------------------------|--------------|---------------|
| Mokėtojas – Fabrikam (Fabrikam West)      | 75,00        |               |
| Gautinos sumos (Fabrikam West)    |              | 75,00         |
| Mokėtojas – Fabrikam East (Fabrikam West) | 25,00        |               |
| Gautinos sumos (Fabrikam West)    |              | 25,00         |

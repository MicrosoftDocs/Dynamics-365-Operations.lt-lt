---
title: Pardavimo ir mokėjimų internetu registravimas
description: Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbc85b957e716d07d9073d889c47f157ea0ead01
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982296"
---
# <a name="posting-of-online-sales-and-payments"></a>Pardavimo ir mokėjimų internetu registravimas

[!include [banner](../includes/banner.md)]

Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus.

Internetinių pardavimo ir mokėjimų registravimas apima du etapus.

- Internetinių „Commerce“ operacijų duomenų rinkimas būstinėje.
- Sinchronizuojant užsakymus, siekiant sukurti pardavimo užsakymus buveinėje.

Internetinių operacijų duomenis galite rinkti rankiniu būdu paleidę P užduotį arba sukurdami pasikartojančią paketinę užduotį.

### <a name="manually-running-the-p-job"></a>Gavimo užduoties vykdymas rankiniu būdu

1. Eikite į Visos darbo sritys > „Retail and Commerce IT“.
2. Spustelėkite paskirstymo grafiką.
3. Pasirinkite P-0001.
4. Jei reikia, pritaikykite kanalo duomenų bazės grupes.
5. Spustelėkite Paleisti dabar.
6. Spustelėkite Taip.

### <a name="scheduling-a-recurring-p-job"></a>Pasikartojančios gavimo užduoties planavimas

1. Eikite į Visos darbo sritys > „Retail and Commerce IT“.
2. Spustelėkite paskirstymo grafiką.
3. Pasirinkite P-0001.
4. Spustelėkite Kurti paketinę užduotį.
5. Spustelėkite Veikti fone.
5. Įgalinkite paketinį vykdymą.
6. Spustelėkite Pasikartojimas.
7. Pasirinkite parinktį Nėra pabaigos datos.
8. Lauke Skaičius įveskite paleisčių per minutę intervalą. Įprastai nurodoma 5-10.
9. Spustelėkite Gerai.
10. Spustelėkite Gerai.

Užsakymai gali būti sinchronizuojami rankiniu būdu paleidžiant „Sinchronizuoti užsakymus“ užduotį arba sukuriant pasikartojančią paketinę užduotį.

### <a name="manually-running-order-synchronization"></a>Užsakymo sinchronizacijos paleidimas rankiniu būdu 

Norėdami rankiniu būdu vieną kartą paleisti „Sinchronizuoti užsakymus“ užduotį, vadovaukitės šiais žingsniais.

1. Eikite į Visos darbo sritys > Parduotuvės finansai.
2. Spustelėkite Sinchronizuoti užsakymus.
3. Lauke Organizacijos hierarchija pasirinkite „Parduotuvės pagal regioną“.
    * Pasirinkite konkrečią interneto parduotuvę arba pasirinkite mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.  
    * Spustelėkite rodyklę ir įtraukite savo pasirinkimą.  
4. Spustelėkite skirtuką Vykdyti fone.
5. Išjunkite paketinį vykdymą
6. Spustelėkite Pasikartojimas.
7. Pasirinkite parinktį Baigto po.
8. Lauke Baigti po įveskite 1.
9. Spustelėkite Gerai.
10. Spustelėkite Gerai.

### <a name="scheduling-recurring-order-synchronization"></a>Pasikartojančio užsakymų sinchronizavimo planavimas

Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus. Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.

1. Eikite į Visos darbo sritys > Parduotuvės finansai.
2. Spustelėkite Sinchronizuoti užsakymus.
3. Lauke Organizacijos hierarchija pasirinkite „Parduotuvės pagal regioną“.
    * Pasirinkite konkrečią interneto parduotuvę arba pasirinkite mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.  
    * Spustelėkite rodyklę ir įtraukite savo pasirinkimą.  
4. Spustelėkite skirtuką Vykdyti fone.
5. Įgalinkite paketinį vykdymą
6. Spustelėkite Pasikartojimas.
7. Pasirinkite parinktį Nėra pabaigos datos.
8. Lauke Skaičius įveskite paleisčių per minutę intervalą. Įprastai nurodoma 2-20
9. Spustelėkite Gerai.
10. Spustelėkite Gerai.

## <a name="data-entities-involved-in-the-process"></a>Proceso duomenų objektai

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans

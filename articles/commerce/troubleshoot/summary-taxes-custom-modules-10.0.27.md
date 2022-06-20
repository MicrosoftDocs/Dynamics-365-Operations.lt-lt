---
title: Užsakymo suvestinės tarpinė suma neapima mokesčių, naudojant pritaikytus užsakymo suvestinės modulius
description: Šiame straipsnyje pateikiamos trikčių diagnostikos instrukcijos, kurios gali padėti naudojant pritaikytus užsakymų suvestinės modulius, o užsakymo suvestinės tarpinė suma neapima išlaidų mokesčių į scenarijų "Kaina su PVM".
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 260dcb6bc1585615195e32adfcd1da6bfbca294e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848842"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Užsakymo suvestinės tarpinė suma neapima mokesčių, naudojant pritaikytus užsakymo suvestinės modulius

Šiame straipsnyje pateikiamos trikčių diagnostikos instrukcijos, kurios gali padėti naudojant pritaikytus užsakymų suvestinės modulius, o užsakymo suvestinės tarpinė suma neapima išlaidų mokesčių į scenarijų "Kaina su PVM".

## <a name="description"></a>Aprašymas

Microsoft Dynamics 365 Commerce Kaip ir versijos 10.0.27 leidimą atlikti toliau nurodyti "Kainos su PVM" scenarijaus pakeitimai, siekiant pateikti nuoseklią užsakymų suvestinės modulių patirtį el. komercijos svetainės puslapiuose.

- Įtraukti du nauji laukai: **TaxOnShippingCharge ir** **TaxOnNonShippingCharges**.
- **GetSalesOrderBySalesId** **ir GetSalesOrderByTransactionId** programos programavimo sąsajose (APIs) yra nurodytos toliau nurodytų scenarijaus "Kaina su PVM" laukų vertės:

    - Tarpinė sumaSalesAmount
    - Tarpinė sumaAmountWithoutTax
    - Tarpinė suma
    - Siuntimo privilegija
    - KitachargeAmount

Tačiau jei naudojate pritaikytus užsakymo suvestinės modulius, šie pakeitimai gali paveikti užsakymo suvestinės tarpines sumas, neįskaitant mokesčių.

## <a name="resolution"></a>Paaiškinimas

Jei naudojate pritaikytus užsakymų suvestinės modulius ir nenorite paveldėti "Kainos su PVM" scenarijaus pakeitimų, "Commerce version 10.0.27" ir vėlesnės versijos, vadovaukitės šio skyriaus instrukcijomis.

Atkurdami ankstesnį (prieš versijos 10.0.27) **užsakymo suvestinės veikimo būdą salesTransaction.SubtotalAmount ir salesTransaction.SubtotalAmountWithoutTax** **·**, atkurkite bendrosios PVM sumos (**TaxOnShippingCharge** **ir TaxOnNonShippingCharges**) įtraukimą į tarpines sumas (**Tarpinė sumaAmount** **ir SubtotalAmountWithoutTax).**

Norėdami grįžti prie ankstesnio užsakymo suvestinės veikimo būdo, atlikite šiuos veiksmus.

1. "Commerce Headquarters" atidarykite "Commerce" parametrų puslapį ("Retail" ir "**Commerce \> Headquarters" nustatymo \> "Commerce" \> parametrai**).
1. Kairiojoje naršymo srityje pasirinkite Konfigūracijos **parametrus**.
1. Įtraukite šiuos konfigūracijos parametrus ir nustatykite kiekvieno vertę kaip **teisingą**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryLitationEnabled

> [!NOTE]
> Jei anksčiau naudojote **konfigūracijos parametrą IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** **ir norite išlaikyti tą patį užsakymo veikimo būdą. NetAmountWithoutTax** ypatybė, **taip pat turite įtraukti konfigūracijos parametrą IsIjąacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** **ir nustatyti jo reikšmę True**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Slėpti mokesčių skaidymo informaciją užsakymo suvestinėse](../hide-taxes-breakup.md)

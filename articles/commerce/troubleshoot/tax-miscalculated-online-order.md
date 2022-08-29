---
title: Neteisingai apskaičiuoti internetinių užsakymų mokesčiai
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, galinčios padėti, kai netinkamai apskaičiuojami interneto užsakymų mokesčiai arba, kai netinkamai nustatyta pardavimo eilutės mokesčių grupė.
author: Reza-Assadi
ms.date: 02/16/2022
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: a85b03cb6245c7c2e3622abc61a7887030927432
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285584"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Neteisingai apskaičiuoti internetinių užsakymų mokesčiai

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, galinčios padėti, kai netinkamai apskaičiuojami interneto užsakymų mokesčiai arba, kai netinkamai nustatyta pardavimo eilutės mokesčių grupė.

## <a name="description"></a>Aprašymas

Kai pateikiamas el. prekybos užsakymas, mokesčiai apskaičiuojami neteisingai arba netinkamai nustatoma pardavimo eilutės mokesčių grupė.

## <a name="resolution"></a>Paaiškinimas

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Bendrųjų PVM grupių konfigūravimas „Commerce Headquarters”

Norėdami konfigūruoti bendrąsias PVM grupes „Commerce Headquarters“, atlikite šiuos veiksmus.

1. Eikite į **Mokestis \> Netiesioginiai mokesčiai \> PVM \> PVM grupė**.
1. Kairiojoje naršymo srityje pasirinkite norimą konfigūruoti mokesčių grupę.
1. „FastTab” **Mažmeninės prekybos paskirties vietos mokestis** sukonfigūruokite PVM grupės mokesčius.

> [!NOTE]
> Siuntai, kurios neapima PVM, kurį nustato kliento adresas, eilutės pristatymo adresas ir paskirties vietos mokesčiai, sukonfigūruoti mokesčių grupei, lemia mokesčių grupę. Dėl išsamesnės informacijos, žr. [Nustatyti mokesčius interneto parduotuvėms pagrįstoms paskirties vietoms](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Konfigūruoti mažmeninės prekybos parduotuvės PVM „Commerce Headquarters“

Norėdami konfigūruoti mažmeninės prekybos parduotuvės PVM „Commerce Headquarters“, atlikite šiuos veiksmus.

1. Eikite į **„Retail” ir „Commerce” \> Kanalai \> Visos parduotuvės**.
1. Pasirinkite parduotuvę, kurios PVM bus konfigūruojamas.
1. „FastTab” **Bendra** skyriuje **PVM** sukonfigūruokite parduotuvės PVM informaciją.

> [!NOTE]
> Jei produktai paimami iš parduotuvės, mokesčių grupė gaunama iš parduotuvės, iš kurios pasirinkta paimti. Daugiau informacijos žr. [Kitų mokesčių pasirinkčių nustatymas parduotuvėms](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Kliento adreso PVM konfigūravimas „Commerce Headquarters“

Norėdami konfigūruoti kliento adreso PVM „Commerce Headquarters“, atlikite šiuos veiksmus.

1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.
1. Pasirinkite klientą, kurio PVM bus konfigūruojamas.
1. „FastTab” **Adresai** pasirinkite adresą, kurio PVM norite konfigūruoti, pasirinkite **Daugiau parinkčių**, tada pasirinkite **Išplėstinės**.
1. „FastTab“ **Bendra** pasirinkite **Mokesčių grupė**.
1. Lauke **PVM** pasirinkite tinkamą vertę.

> [!NOTE]
> Siuntimo, kuriam taikomas kliento adreso PVM, eilutės pristatymo adresas nurodo eilutės mokesčių grupę. Jei klientas siunčia į esamą adresą, kurio mokesčių grupė jau yra sukonfigūruota, bus naudojama esama mokesčių grupė. Pagal numatytuosius nustatymus, kai adresai kuriami, jie neturi mokesčių grupės.

## <a name="additional-resources"></a>Papildomi ištekliai

[Internetinių užsakymų PVM konfigūravimas](../sales-tax-config.md)

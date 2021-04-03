---
title: Neteisingai apskaičiuoti internetinių užsakymų mokesčiai
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai netinkamai apskaičiuojami internetinių užsakymų mokesčiai arba kai pardavimo eilutės mokesčių grupė nustatyta neteisingai.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 421df7545e285950ef8a3c4b753c8c6dc5f26422
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585443"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Neteisingai apskaičiuoti internetinių užsakymų mokesčiai

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai netinkamai apskaičiuojami internetinių užsakymų mokesčiai arba kai pardavimo eilutės mokesčių grupė nustatyta neteisingai.

## <a name="description"></a>Aprašymas

Kai pateikiamas el. prekybos užsakymas, mokesčiai apskaičiuojami neteisingai arba netinkamai nustatoma pardavimo eilutės mokesčių grupė.

## <a name="resolution"></a>Sprendimas

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Konfigūruoti mažmeninės prekybos parduotuvės PVM „Commerce Headquarters“

Norėdami konfigūruoti mažmeninės prekybos parduotuvės PVM „Commerce Headquarters“, atlikite šiuos veiksmus.

1. Eikite į **„Retail” ir „Commerce” \> Kanalai \> Visos parduotuvės**.
1. Pasirinkite parduotuvę, kurios PVM bus konfigūruojamas.
1. „FastTab” **Bendra** skyriuje **PVM** sukonfigūruokite parduotuvės PVM informaciją.

> [!NOTE]
> Jei produktai paimami iš parduotuvės, mokesčių grupė gaunama iš parduotuvės, iš kurios pasirinkta paimti. Daugiau informacijos žr. [Kitų mokesčių pasirinkčių nustatymas parduotuvėms](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Kliento adreso PVM konfigūravimas „Commerce Headquarters“

Norėdami konfigūruoti kliento adreso PVM „Commerce Headquarters“, atlikite šiuos veiksmus.

1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.
1. Pasirinkite klientą, kurio PVM bus konfigūruojamas.
1. „FastTab” **Adresai** pasirinkite adresą, kurio PVM norite konfigūruoti, pasirinkite **Daugiau parinkčių**, tada pasirinkite **Išplėstinės**.
1. „FastTab“ **Bendra** pasirinkite **Mokesčių grupė**.
1. Lauke **PVM** pasirinkite tinkamą vertę.

> [!NOTE]
> Siuntimo, kuriam taikomas kliento adreso PVM, eilutės pristatymo adresas nurodo eilutės mokesčių grupę. Jei klientas siunčia į esamą adresą, kurio mokesčių grupė jau yra sukonfigūruota, bus naudojama esama mokesčių grupė. Pagal numatytuosius nustatymus, kai adresai kuriami, jie neturi mokesčių grupės.

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Bendrųjų PVM grupių konfigūravimas „Commerce Headquarters”

Norėdami konfigūruoti bendrąsias PVM grupes „Commerce Headquarters“, atlikite šiuos veiksmus.

1. Eikite į **Mokestis \> Netiesioginiai mokesčiai \> PVM \> PVM grupė**.
1. Kairiojoje naršymo srityje pasirinkite mokesčių grupę, kurią norite konfigūruoti.
1. „FastTab” **Mažmeninės prekybos paskirties vietos mokestis** sukonfigūruokite PVM grupės mokesčius.

> [!NOTE]
> Siuntimo, kai nėra kliento adreso PVM, mokesčių grupę nustato eilutės pristatymo adresas ir paskirties vietos mokesčiai, sukonfigūruoti mokesčių grupei. Dėl išsamesnės informacijos, žr. [Nustatyti mokesčius interneto parduotuvėms pagrįstoms paskirties vietoms](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="additional-resources"></a>Papildomi ištekliai

[Internetinių užsakymų PVM konfigūravimas](../sales-tax-config.md)

---
title: Grynųjų pinigų srautų prognozavimo įjungimas
description: Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Grynųjų pinigų srautų prognozės.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8dba56af53090d5d78632da4d414143b136f8a8d
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713760"
---
# <a name="enable-cash-flow-forecasting"></a>Grynųjų pinigų srautų prognozavimo įjungimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip įjungti pinigų srautų prognozių funkciją finansų žinių srityje.

> [!NOTE]
> Norėdami grynųjų pinigų sraute naudoti mokėjimo prognozes, turite nustatyti funkciją Kliento mokėjimo prognozės, kaip aprašyta temoje [Kliento mokėjimo prognozių įjungimas](enable-cust-paymnt-prediction.md).
  
1. Atidarykite darbo sritį **Funkcijų valdymas** ir atlikite tolesnius veiksmus.

    1. Pasirinkite **Tikrinti, ar yra naujinimų**.
    2. Skirtuke **Viskas** ieškokite pinigų srautų **prognozių**. Jei tos priemonės nerandate, ieškokite **(Peržiūrėti) pinigų srautų prognozių**. 
    3. Įjungti funkciją.

2. Eikite į **Grynųjų pinigų ir banko valdymas \> Grynųjų pinigų srautų prognozių sąranka** ir įtraukite likvidumo sąskaitas, kurios turi būti įtrauktos į prognozes. Mokėjimų likvidumo sąskaitą taip pat nustatykite gautinų sumų **ir** mokėtinų **sumų skirtukuose**. Įsitikinkite, kad perskaičiuoti pinigų srautų prognozę.

    > [!NOTE]
    > Jei likvidumo sąskaitos nenustatytos, grynųjų pinigų srauto sugeneruoti negalima.
    >
    > Daugiau informacijos apie tai, kaip nustatyti pinigų srautų prognozes, ieškokite pinigų [srautų prognozei.](../cash-bank-management/cash-flow-forecasting.md)

3. Eikite į **Grynųjų pinigų ir banko valdymas \> Sąranka \> Finansinės įžvalgos (peržiūros versija) \> Grynųjų pinigų srautų prognozes (peržiūros versija)** ir atlikite tolesnius veiksmus.

    1. Skirtuke **Grynųjų pinigų srautų prognozė** pasirinkite **Įjungti funkciją**.
    2. Pasirinkite **Sukurti prognozavimo modelį**.

> [!NOTE]
> Pinigų **srautų prognozės** modelio mokymas reikalauja duomenų su 100 ar daugiau operacijų, kurios apima daugiau nei metus. Rekomenduojame turėti mažiausiai dviejų metų duomenis su daugiau nei 1000 operacijų.

Daugiau informacijos apie grynųjų pinigų srautų prognozavimo galimybę žr. [Grynųjų pinigų srautų prognozavimas](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

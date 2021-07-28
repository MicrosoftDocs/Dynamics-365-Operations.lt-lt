---
title: Vidinės įmonės užsakymų filtravimas siekiant išvengti užsakymų ir jų eilučių sinchronizavimo
description: Šioje temoje paaiškinama, kaip filtruoti vidinės įmonės užsakymus, kad objektai Užsakymai ir Užsakymų eilutės nebūtų sinchronizuojami.
author: negudava
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 5e7b0188d5c2dc4ee7691266aa4c857fc189d0f0
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347253"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Vidinės įmonės užsakymų filtravimas siekiant išvengti užsakymų ir jų eilučių sinchronizavimo

[!include [banner](../../includes/banner.md)]

Galite filtruoti vidinės įmonės užsakymus, kad lentelės **Užsakymų** ir **Užsakymų eilutės** nebūtų sinchronizuojamos. Kai kuriais atvejais vidinės įmonės užsakymo informacija nėra reikalinga „Customer Engagement” programoje.

Kiekviena iš standartinių „Dataverse“ lentelių yra išplečiamas per nuorodomis į **Vidinės įmonės užsakymas** lauką, o dvejopo rašymo žemėlapiai modifikuojami, kad būtų galima nurodyti papildomus filtrų stulpelius. Todėl vidinės įmonės užsakymai yra nebesinchronizuojami. Šis procesas padeda neleisti nereikalingų duomenų „Customer Engagement“ programoje.

1. Išplėskite **CDS pardavimo užsakymų antraštės** lentelę įtraukdami nuorodą į **Vidinės įmonės užsakymo** stulpelį. Šis stulpelis pildomas tik vidinės įmonės užsakymuose. Stulpelis **Vidinės įmonės užsakymas** prieinamas **Pardavimo lentelė** lentelėje.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Susieti išdėstymą su paskirties vietos puslapiu CDS pardavimo užsakymo antraštėms.":::

2. Išplėtus **CDS pardavimo užsakymų antraštės**, stulpelį **Vidinės įmonės užsakymas** galima susieti. Taikykite filtrą su `INTERCOMPANYORDER == ""` užklausos eilute.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Redaguoti CDS pardavimo užsakymo antraščių užklausos dialogo langą.":::

3. Išplėskite **CDS pardavimo užsakymų eilutės** lentelę įtraukdami nuorodą į **Vidinės įmonės TransId** stulpelį. Šis stulpelis pildomas tik vidinės įmonės užsakymuose. Stulpelis **Vidinės įmonės TransId** prieinamas **Pardavimo eilutė** lentelėje.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Susieti išdėstymą su paskirties vietos puslapiu CDS pardavimo užsakymo eilutėms.":::

4. Išplėtus **CDS pardavimo užsakymų eilutės**, stulpelį **IntercompanyInventTransId** galima susieti. Taikykite filtrą su `INTERCOMPANYINVENTTRANSID == ""` užklausos eilute.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Redaguoti CDS pardavimo užsakymo eilučių užklausos dialogo langą.":::

5. Norėdami išplėsti lentelę **Pardavimo sąskaitos faktūros antraštė V2** ir pridėti filtro užklausą, pakartokite 1 ir 2 veiksmus. Šiuo atveju naudokite `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` filtro užklausos eilutę.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Susieti išdėstymą su paskirties vietos puslapiu pardavimo sąskaitos faktūros antraštei V2.":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Redaguoti pardavimo sąskaitos faktūros antraštės V2 užklausos dialogo langą.":::

6. Norėdami išplėsti lentelę **Pardavimo sąskaitos faktūros eilutės V2** ir pridėti filtro užklausą, pakartokite 3 ir 4 veiksmus. Šiuo atveju naudokite `INTERCOMPANYINVENTTRANSID == ""` filtro užklausos eilutę.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Redaguoti pardavimo sąskaitos faktūros eilutės V2 užklausos dialogo langą.":::

7. Lentelė **Pasiūlymai** neturi vidinės įmonės ryšio. Jei kuris nors iš vidinės įmonės klientų sukuria pasiūlymą, galite naudoti stulpelį **Pasirinktinė grupė** tam, kad įdėtumėte šiuos visus klientus į vieną klientų grupę. Įtraukdami stulpelį **Pasirinktinė grupė** galite išplėsti antraštę ir eilutes, o tada filtruoti, kad ta grupė nebūtų įtraukta.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Susieti išdėstymą su paskirties vietos puslapiu CDS pardavimų pasiūlymų antraštei.":::

8. Po to, kai **Pasiūlymai** išplečiami, pritaikykite filtrą su `CUSTGROUP != "<company>"` užklausos eilute.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Redaguoti CDS pardavimų pasiūlymo antraštės užklausos dialogo langą.":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
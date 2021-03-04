---
title: Vidinės įmonės užsakymų filtravimas siekiant išvengti užsakymų ir užsakymų eilučių sinchronizavimo
description: Šioje temoje aprašoma, kaip filtruoti vidinės įmonės užsakymus siekiant išvengti užsakymų ir užsakymų eilučių sinchronizavimo.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701038"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Vidinės įmonės užsakymų filtravimas siekiant išvengti užsakymų ir užsakymų eilučių sinchronizavimo

[!include [banner](../../includes/banner.md)]

Galite filtruoti vidinės įmonės užsakymus siekdami išvengti **užsakymų** ir **užsakymų eilučių** sinchronizavimo. Kai kuriais atvejais vidinės įmonės užsakymo informacija nėra būtina kliento programos įjungimo programėlėje.

Kiekvienas iš standartinių „Common Data Service“ objektų yra išplečiamas su nuorodomis į lauką **IntercompanyOrder**, o dvejopo rašymo žemėlapiai modifikuojami, kad būtų galima nurodyti papildomus filtrų laukus. Rezultatas yra tai, kad vidinės įmonės užsakymai nebėra sinchronizuojami. Šis procesas padeda išvengti nereikalingų duomenų „Customer Engagement“ programoje.

1. Įtraukite nuorodą į **IntercompanyOrder** į **CDS pardavimo užsakymų antraštės**. Jis užpildomas tik vidinės įmonės užsakymuose. Laukas **IntercompanyOrder** siūlomas **Pardavimo lentelėje**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Susieti išdėstymą su paskirties vieta, SalesOrderHeader":::
    
2. Išplėtus **CDS pardavimo užsakymų antraštės**, lauką **IntercompanyOrder** galima susieti. Taikykite filtrą teikdami užklausos eilutę `INTERCOMPANYORDER == ""`.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Pardavimo užsakymų antraštės, redaguoti užklausą":::

3. Įtraukite nuorodą į **IntercompanyInventTransId** į **CDS pardavimo užsakymo eilutės**.  Jis užpildomas tik vidinės įmonės užsakymuose. Laukas **InterCompanyInventTransID** siūlomas **Pardavimo eilutėje**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Susieti išdėstymą su paskirties vieta, SalesOrderLine":::

4. Išplėtus **CDS pardavimo užsakymų eilutės**, lauką **IntercompanyInventTransId** galima susieti. Taikykite filtrą teikdami užklausos eilutę `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Pardavimo užsakymo eilutės, redaguoti užklausą":::

5. Išplėskite **Pardavimo SF antraštės V2** ir **Pardavimo SF eilutės V2** taip pat, kaip išplečiate „Common Data Service“ objektus atlikdami 1 ir 2 veiksmus. Tada pridėkite filtrų užklausas. **Pardavimo SF antraštės V2** filtro eilutė yra `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. **Pardavimo SF eilutės V2** filtro eilutė yra `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Susieti išdėstymą su paskirties vieta, Pardavimo SF antraštės":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Pardavimo SF antraštės, redaguoti užklausą":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Pardavimo SF eilutės, redaguoti užklausą":::

6. Objektas **Pasiūlymai** neturi vidinės įmonės ryšio. Jei kas nors iš vidinės įmonės klientų sukuria pasiūlymą, visi šie klientai gali nustatyti vienoje klientų grupėje naudodami lauką **CustGroup**.  Antraštė ir eilutės gali būti išplėstos, kad būtų galima įtraukti lauką **CustGroup**, o tada filtruoti, kad nebūtų įtraukta ši grupė.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Susieti išdėstymą su paskirties vieta, Pardavimo pasiūlymo antraštė":::

7. Išplėtę objektą **Pasiūlymai**, pritaikykite filtrą su užklausos eilute `CUSTGROUP !=  "<company>"`.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Pardavimo pasiūlymo antraštė, redaguoti užklausą":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
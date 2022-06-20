---
title: Sąskaitų plano rengimas
description: Šiame straipsnyje pateikta informacija, kuri padės jums suplanuoti jūsų organizacijos sąskaitų planą.
author: aprilolson
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e797117199ff57cb4d3beae187ae7649579d33b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853354"
---
# <a name="plan-your-chart-of-accounts"></a>Sąskaitų plano rengimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta informacija, kuri padės jums suplanuoti jūsų organizacijos sąskaitų planą.

Norėdami sekti ir prižiūrėti finansinę informaciją organizacijoje, galite nustatyti sąskaitų planą. Sąskaitų planas yra sąskaitų rinkinys, kuris apibrėžia finansinę sistemą. Norėdami toliau sekti šių sąskaitų operacijas, galite pridėti segmentus. Šie segmentai vadinami finansinėmis dimensijomis. Pavyzdžiui, išlaidų sąskaita gali apimti finansines dimensijas, pavadintas „Padalinys“, „Išlaidų centras“ ir „Paskirtis“. Vartotojo nustatytos taisyklės nurodo, kaip šios finansinės dimensijos yra susietos su pagrindinėmis sąskaitomis ir kitomis finansinėmis dimensijomis ir kaip įvedamos operacijos. Šios vartotojo nustatytos taisyklės žinomos kaip sąskaitos struktūros ir išplėstinės taisyklės.

Sąskaitų planas yra susistemintas juridinio subjekto DK sąskaitų sąrašas. Sąrašas naudojamas norint parengti finansines ataskaitas institucijoms ir savininkams. Pirmiausia sąskaitos grupuojamos į sąskaitų tipus, o tada sujungiamos į didesnes kategorijas. Žvelgiant bendrai, sąskaitos grupuojamos kaip įplaukos ir išlaidos (operacijų sąskaitos) bei turtas ir įsipareigojimai (balanso sąskaitos).

Sąskaitų planu galima dalintis ir juo naudotis gali bet kuris juridinis subjektas organizacijoje. Sąskaitų planas, kurį naudoja juridinis subjektas, nurodomas puslapyje **Didžioji knyga**.

Toliau pateikiami kai kurie veiksniai, į kuriuos privalote atsižvelgti, kai planuojate savo organizacijos sąskaitų plano struktūrą:

- Ataskaitų kūrimo reikalavimai šalyje arba regione, kuriame yra jūsų organizacija.
- Jūsų juridinio subjekto ataskaitų kūrimo reikalavimai
- Išorinėms organizacijoms ir jūsų organizacijai reikalingas specifikacijų laipsnis

Kurkite sąskaitų planą puslapyje **Sąskaitų planas**. Galite kurti pagrindines sąskaitas puslapyje **Sąskaitų planas** arba puslapyje **Pagrindinės sąskaitos**. Pagrindinėse sąskaitose nereikėtų naudoti jokių specialių simbolių, kurie naudojami kaip sąskaitų plano skyrikliai. Kitu atveju gali kilti nestabilumų arba poreikis visada naudoti peržvalgas arba dialogo langą, įvedant sąskaitos ir dimensijų kombinacijas. Daugiau informacijos žr. [Kurti pagrindinę sąskaitą](tasks/create-main-account.md).

> [!NOTE]
> „Dynamics 365 for Finance and Operations“ 8.0 versijoje (2018 m. balandžio mėn.) galite modifikuoti sąskaitų plano skyriklį iš puslapio **DK parametrai**.

Tikslinga susieti pagrindines sąskaitas su pagrindinių sąskaitų kategorijomis, kad galėtumėte išnaudoti numatytąsias finansines ataskaitas nedarydami jokių modifikacijų. Todėl jūs galite greičiau ir lengviau kurti ir prižiūrėti ataskaitas.

Naudokite puslapį **Sąskaitų struktūrų konfigūravimas**, kad sukurtumėte sąskaitų struktūras. Sąskaitų struktūros apibrėžia galiojančias kombinacijas. Šios kombinacijos, kartu su pagrindinėmis sąskaitomis, formuoja sąskaitų planą. Daugiau informacijos žr. [Kurti sąskaitos struktūrą](tasks/create-account-structures.md).

**Juridinio subjekto nepaisymai**

Ne visos pagrindinės sąskaitos tinkamos visiems juridiniams subjektams, o kai kurios pagrindinės sąskaitos gali būti aktualios tik tam tikrą laikotarpį. Tokiais atvejais skiltį **Juridinio subjekto nepaisymas** galite naudoti norėdami nustatyti, kuriose įmonėse pagrindinės sąskaitos turi būti sustabdytos, kas jų savininkas ir kurį laikotarpį dimensija yra aktyvi. Nepaisymai bendrame lygyje negali būti labiau ribojantys nei nepaisymai juridinio subjekto lygyje.

Daugiau informacijos ieškokite šiose temose:

- [Finansinės dimensijos](financial-dimensions.md)
- [Kurti ir priskirti išplėstinės taisyklės struktūras](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

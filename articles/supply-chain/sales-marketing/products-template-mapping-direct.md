---
title: "Tiesioginis „Finance and Operations“ produktų sinchronizavimas su „Sales“ produktais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus sinchronizuojant su Microsoft Dynamics 365 for Sales“."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3ae50372edcd473f2288f8172b71eac33e24b636
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a>Tiesioginis „Finance and Operations“ produktų sinchronizavimas su „Sales“ produktais

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration).

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus sinchronizuojant tiesiogiai su „Microsoft Dynamics 365 for Sales“.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus. Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami sinchronizuojant „Finance and Operations“ produktus su „Sales“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis
- **Užduoties pavadinimas projekte Duomenų integravimas:**Produktai

Prieš sinchronizuojant produktą, nereikia atlikti jokių sinchronizavimo užduočių.

## <a name="entity-set"></a>Objektų rinkinys

| „Finance and Operations”     | Pardavimas    |
|----------------------------|----------|
| Parduodami išleisti produktai | Produktai |

## <a name="entity-flow"></a>Objekto srautas

Produktai tvarkomi „Finance and Operations“ ir sinchronizuojami su „Sales“. „Finance and Operations“ duomenų objektas **Parduodami patvirtinti produktai** eksportuoja tik *parduodamus* produktus. Parduodami produktai – tai produktai, apie kuriuos pateikta informacija, reikalinga norint produktus naudoti pardavimo užsakyme. Tos pačios taisyklės taikomos, kai produktas patvirtinamas naudojant puslapio **Patvirtintas produktas** funkciją **Tikrinti**.

Produkto numeris naudojamas kaip raktas. Todėl produkto variantus susinchronizavus su „Sales“, kiekvienam produkto variantui priskiriamas atskiras produkto ID.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Į „Sales“ įtrauktas naujas produktų laukas **Tvarkomas išoriškai**, kad būtų galima nurodyti, jog tam tikras produktas yra tvarkomas išoriškai. Pagal numatytuosius nustatymus, importuojant į „Sales“ reikšmė nustatoma į parinktį **Taip**. Galimos šios vertės:

- **Taip** – produktas paimtas iš „Finance and Operations“ ir jo nebus galima redaguoti sprendime „Sales“.
- **Ne** – produktas į „Sales“ buvo įtrauktas tiesiogiai.
- **(Tuščia)** – prieš įgalinant sprendimą Potencialūs klientai ir grynieji pinigai, produktas teikiamas sprendime „Sales“.

Laukas **Tvarkomas išoriškai** padeda užtikrinti, kad su „Finance and Operations“ bus sinchronizuojami tik pasiūlymai ir pardavimo užsakymai, kuriuose yra išoriškai tvarkomų produktų.

Išoriškai tvarkomi produktai automatiškai įtraukiami į pirmąjį tinkamą kainoraštį ta pačia valiuta. Kainoraščiai išrikiuojami abėcėlės tvarka pagal pavadinimą. „Finance and Operations“ produkto pardavimo kaina naudojama kaip kainoraščio kaina. Todėl „Sales“ turi būti pateiktas kainoraštis, atitinkantis kiekvieno produkto pardavimo valiutą „Finance and Operations“. Patvirtintų parduodamų produktų valiuta nustatyta į juridinio subjekto, iš kurio produktas eksportuojamas, apskaitos valiutą.

> [!NOTE]
> Jei nebus valiutą atitinkančio kainoraščio, sinchronizavimo atlikti nepavyks.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

- Prieš sinchronizuojant pirmą kartą, Išskirtųjų produktų lentelė turi būti užpildyta naudojant „Finance and Operations“ esamus produktus. Esami produktai nebus sinchronizuojami, kol ši užduotis nebus baigta.

    1. „Finance and Operations“ naudokite parinktį Ieška, norėdami rasti parinktį **Automatiškai įvesti išskirtųjų produktų lentelę**.
    2. Norėdami vykdyti užduotį pasirinkite **Automatiškai įvesti išskirtųjų produktų lentelę**. Šią užduotį reikia vykdyti tik vieną kartą.

- Įsitikinkite, kad susiejime **SalesUnitSymbol** į **DefaultUnit (pavadinimas)** tarp „Finance and Operations“ ir „Sales“ yra būtina pardavimo matavimo vieneto (MV) reikšmių schema.
- Atnaujinkite **vienetų grupės** (**defaultuomscheduleid.name**) reikšmių schemą, kad ji atitiktų „Sales“ **vienetų grupes**.

    Numatytoji šablono reikšmė yra **Numatytasis vienetas**.

- Įsitikinkite, kad visų „Finance and Operations“ produktų pardavimo MV pateikiami „Sales“.
- Įsitikinkite, kad „Sales“ nustatyti kainoraščiai, atitinkantys kiekvieno produkto pardavimo valiutą „Finance and Operations“.
- „Sales“ sukūrus produktų, jiems gali būti suteikta būsena **Juodraštis** arba **Aktyvus**. Veikimas valdomas „Sales“ parinktyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas**.

    Sukūrus būsenos **Juodraštis** produktų, šie turi būti suaktyvinti prieš tai, kai juos galima įtraukti į pasiūlymus arba pardavimo užsakymus.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktoje iliustracijoje vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas. 

> [!NOTE]
> Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Finance and Operations“.

![Šablono susiejimas duomenų integratoriuje](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Susijusios temos

[Potencialūs klientai ir grynieji pinigai](prospect-to-cash.md)

[Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais](accounts-template-mapping-direct.md)

[Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais](contacts-template-mapping-direct.md)

[Tiesioginis „Finance and Operations“ pardavimo užsakymų antraščių ir eilučių sinchronizavimas su „Sales“](sales-order-template-mapping-direct-two-ways.md)

[Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“](sales-invoice-template-mapping-direct.md)





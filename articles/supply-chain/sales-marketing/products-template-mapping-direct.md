---
title: Tiesioginis produktų sinchronizavimas naudojant Tiekimo grandinės valdymą su „Sales“ produktais
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojamos „Dynamics 365 Supply Chain Management“ produktus sinchronizuojant su „Dynamics 365 Sales“.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6ffd55585ff43f993876de6c669eb61e74a9fd79
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527319"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Tiesioginis produktų sinchronizavimas naudojant Tiekimo grandinės valdymą su „Sales“ produktais

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Common Data Service“, skirtą programoms](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojamos „Dynamics 365 Supply Chain Management“ produktus tiesiogiai sinchronizuojant su „Dynamics 365 Sales“.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Supply Chain Management“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus. Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„Power Apps“ administravimo centrą](https://admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami sinchronizuojant Tiekimo grandinės valdymo produktus su „Sales“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Produktai (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis
- **Užduoties pavadinimas projekte Duomenų integravimas:** Produktai

Prieš sinchronizuojant produktą, nereikia atlikti jokių sinchronizavimo užduočių.

## <a name="entity-set"></a>Objektų rinkinys

| Tiekimo grandinės valdymas    | Pardavimas    |
|----------------------------|----------|
| Parduodami išleisti produktai | Produktai |

## <a name="entity-flow"></a>Objekto srautas

Produktai tvarkomi Tiekimo grandinės valdyme ir sinchronizuojami su „Sales“. Tiekimo grandinės valdymo duomenų objektas **Parduodami patvirtinti produktai** eksportuoja tik *parduodamus* produktus. Parduodami produktai – tai produktai, apie kuriuos pateikta informacija, reikalinga norint produktus naudoti pardavimo užsakyme. Tos pačios taisyklės taikomos, kai produktas patvirtinamas naudojant puslapio **Patvirtintas produktas** funkciją **Tikrinti**.

Produkto numeris naudojamas kaip raktas. Todėl produkto variantus susinchronizavus su „Sales“, kiekvienam produkto variantui priskiriamas atskiras produkto ID.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Į „Sales“ įtrauktas naujas produktų laukas **Tvarkomas išoriškai**, kad būtų galima nurodyti, jog tam tikras produktas yra tvarkomas išoriškai. Pagal numatytuosius nustatymus, importuojant į „Sales“ reikšmė nustatoma į parinktį **Taip**. Galimos šios vertės:

- **Taip** – produktas paimtas iš Tiekimo grandinės valdymo ir jo nebus galima redaguoti sprendime „Sales“.
- **Ne** – produktas į „Sales“ buvo įtrauktas tiesiogiai.
- **(Tuščia)** – prieš įgalinant sprendimą Potencialūs klientai ir grynieji pinigai, produktas teikiamas sprendime „Sales“.

Laukas **Tvarkomas išoriškai** padeda užtikrinti, kad su Tiekimo grandinės valdymu bus sinchronizuojami tik pasiūlymai ir pardavimo užsakymai, kuriuose yra išoriškai tvarkomų produktų.

Išoriškai tvarkomi produktai automatiškai įtraukiami į pirmąjį tinkamą kainoraštį ta pačia valiuta. Kainoraščiai išrikiuojami abėcėlės tvarka pagal pavadinimą. Tiekimo grandinės valdymo produkto pardavimo kaina naudojama kaip kainoraščio kaina. Todėl „Sales“ turi būti pateiktas kainoraštis, atitinkantis kiekvieno produkto pardavimo valiutą Tiekimo grandinės valdyme. Patvirtintų parduodamų produktų valiuta nustatyta į juridinio subjekto, iš kurio produktas eksportuojamas, apskaitos valiutą.

> [!NOTE]
> - Jei nebus valiutą atitinkančio kainoraščio, produktų sinchronizuoti nepavyks.
> - Negalite kontroliuoti naudoto kainų sąrašo su integravimu sudarant žemėlapį pagal pricelevelid.name [Numatytasis kainų sąrašas (Pavadinimas)] „Data Integration“ projekte. Visą įvestį turi sudaryti mažosios raidės. Pavyzdžiui, numatytasis kainų sąrašas „Sales“ pavadinimų „Standard“ būtų: Paskirties laukelis: pricelevelid.name [Numatytasis kainų sąrašas (Pavadinimas)] ir žemėlapio tipas: [ { "keitimo Tipas": „Numatytasis", „Numatytoji vertė": „standartinė" } ].

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

- Prieš sinchronizuojant pirmą kartą, Išskirtųjų produktų lentelė turi būti užpildyta naudojant esamus produktus Tiekimo grandinės valdyme. Esami produktai nebus sinchronizuojami, kol ši užduotis nebus baigta.

    1. Tiekimo grandinės valdyme naudokite parinktį Ieška, norėdami rasti parinktį **Automatiškai įvesti išskirtųjų produktų lentelę**.
    2. Norėdami vykdyti užduotį pasirinkite **Automatiškai įvesti išskirtųjų produktų lentelę**. Šią užduotį reikia vykdyti tik vieną kartą.

- Įsitikinkite, kad susiejime **SalesUnitSymbol** į **DefaultUnit (pavadinimas)** tarp Tiekimo grandinės valdymo ir „Sales“ yra būtina pardavimo matavimo vieneto (MV) reikšmių schema.
- Atnaujinkite **vienetų grupės** (**defaultuomscheduleid.name**) reikšmių schemą, kad ji atitiktų „Sales“ **vienetų grupes**.

    Numatytoji šablono reikšmė yra **Numatytasis vienetas**.

- Įsitikinkite, kad visų Tiekimo grandinės valdymo produktų pardavimo MV pateikiami „Sales“.
- Įsitikinkite, kad „Sales“ nustatyti kainoraščiai, atitinkantys kiekvieno produkto pardavimo valiutą Tiekimo grandinės valdyme.
- „Sales“ sukūrus produktų, jiems gali būti suteikta būsena **Juodraštis** arba **Aktyvus**. Veikimas valdomas „Sales“ parinktyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas**.

    Sukūrus būsenos **Juodraštis** produktų, šie turi būti suaktyvinti prieš tai, kai juos galima įtraukti į pasiūlymus arba pardavimo užsakymus.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktoje iliustracijoje vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas. 

> [!NOTE]
> Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Supply Chain Management“.

![Šablono susiejimas duomenų integratoriuje](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Susijusios temos

[Potencialaus kliento pavertimas pinigais](prospect-to-cash.md)

[Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais](accounts-template-mapping-direct.md)

[Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais](contacts-template-mapping-direct.md)

[Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir Tiekimo grandinės valdymo](sales-order-template-mapping-direct-two-ways.md)

[Tiesioginis „Supply Chain Management“ pardavimo SF antraščių ir eilučių sinchronizavimas su „Sales“](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
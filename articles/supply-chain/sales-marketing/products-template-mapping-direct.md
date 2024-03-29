---
title: Tiesioginis produktų sinchronizavimas naudojant „Supply Chain Management” su „Sales“ produktais
description: Šiame straipsnyje aptariamos šablonus ir su juos susijusias užduotis, kurios naudojamos produktams sinchronizuoti su Dynamics 365 Supply Chain Management "Dynamics 365" pardavimu.
author: Henrikan
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 5195368f3de12c7e361905c3cca442067e39e000
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855996"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Tiesioginis produktų sinchronizavimas naudojant „Supply Chain Management” su „Sales“ produktais

[!include [banner](../includes/banner.md)]



> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Microsoft Dataverse“, skirtą programoms](/powerapps/administrator/data-integrator).

Šiame straipsnyje aptariamos šablonai ir susijusios užduotys, naudojamos tiesiogiai Dynamics 365 Supply Chain Management sinchronizuoti produktus iš "Dynamics 365" pardavimo.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Supply Chain Management“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus. Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„Power Apps“ administravimo centrą](https://admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami sinchronizuojant „Supply Chain Management” produktus su „Sales“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Produktai (iš „Supply Chain Management” į „Sales“) – tiesioginis
- **Užduoties pavadinimas projekte Duomenų integravimas:** Produktai

Prieš sinchronizuojant produktą, nereikia atlikti jokių sinchronizavimo užduočių.

## <a name="entity-set"></a>Objektų rinkinys

| „Supply Chain Management”    | Pardavimas    |
|----------------------------|----------|
| Parduodami išleisti produktai | Produktai |

## <a name="entity-flow"></a>Objekto srautas

Produktai tvarkomi „Supply Chain Management” ir sinchronizuojami su „Sales“. „Supply Chain Management” duomenų objektas **Parduodami patvirtinti produktai** eksportuoja tik *parduodamus* produktus. Parduodami produktai – tai produktai, apie kuriuos pateikta informacija, reikalinga norint produktus naudoti pardavimo užsakyme. Tos pačios taisyklės taikomos, kai produktas patvirtinamas naudojant puslapio **Patvirtintas produktas** funkciją **Tikrinti**.

Produkto numeris naudojamas kaip raktas. Todėl produkto variantus susinchronizavus su „Sales“, kiekvienam produkto variantui priskiriamas atskiras produkto ID.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Į „Sales“ įtrauktas naujas produktų laukas **Tvarkomas išoriškai**, kad būtų galima nurodyti, jog tam tikras produktas yra tvarkomas išoriškai. Pagal numatytuosius nustatymus, importuojant į „Sales“ reikšmė nustatoma į parinktį **Taip**. Galimos šios vertės:

- **Taip** – produktas paimtas iš „Supply Chain Management” ir jo nebus galima redaguoti sprendime „Sales“.
- **Ne** – produktas į „Sales“ buvo įtrauktas tiesiogiai.
- **(Tuščia)** – prieš įgalinant sprendimą Potencialūs klientai ir grynieji pinigai, produktas teikiamas sprendime „Sales“.

Laukas **Tvarkomas išoriškai** padeda užtikrinti, kad su „Supply Chain Management” bus sinchronizuojami tik pasiūlymai ir pardavimo užsakymai, kuriuose yra išoriškai tvarkomų produktų.

Išoriškai tvarkomi produktai automatiškai įtraukiami į pirmąjį tinkamą kainoraštį ta pačia valiuta. Kainoraščiai išrikiuojami abėcėlės tvarka pagal pavadinimą. „Supply Chain Management” produkto pardavimo kaina naudojama kaip kainoraščio kaina. Todėl „Sales“ turi būti pateiktas kainoraštis, atitinkantis kiekvieno produkto pardavimo valiutą „Supply Chain Management”. Patvirtintų parduodamų produktų valiuta nustatyta į juridinio subjekto, iš kurio produktas eksportuojamas, apskaitos valiutą.

> [!NOTE]
> - Jei nebus valiutą atitinkančio kainoraščio, produktų sinchronizuoti nepavyks.
> - Naudojamą kainoraštį su integracija galite valdyti projekte Duomenų integravimas susieję pricelevelid.name [Numatytasis kainoraštis (pavadinimas)]. Visą įvestį turi sudaryti mažosios raidės. Pavyzdžiui, numatytoji „Sales“ kainoraščio pavadinimu „Standartinis“ reikšmė būtų: Paskirties laukas: pricelevelid.name [Numatytasis kainoraštis (pavadinimas)], o Susiejimo tipas: [ { "transformType": "Default", "defaultValue": "standard" } ].

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

- Prieš sinchronizuojant pirmą kartą, Išskirtųjų produktų lentelė turi būti užpildyta naudojant esamus produktus „Supply Chain Management”. Esami produktai nebus sinchronizuojami, kol ši užduotis nebus baigta.

    1. „Supply Chain Management” naudokite parinktį Ieška, norėdami rasti parinktį **Automatiškai įvesti išskirtųjų produktų lentelę**.
    2. Norėdami vykdyti užduotį pasirinkite **Automatiškai įvesti išskirtųjų produktų lentelę**. Šią užduotį reikia vykdyti tik vieną kartą.

- Įsitikinkite, kad susiejime **SalesUnitSymbol** į **DefaultUnit (pavadinimas)** tarp „Supply Chain Management” ir „Sales“ yra būtina pardavimo matavimo vieneto (MV) reikšmių schema.
- Atnaujinkite **vienetų grupės** (**defaultuomscheduleid.name**) reikšmių schemą, kad ji atitiktų „Sales“ **vienetų grupes**.

    Numatytoji šablono reikšmė yra **Numatytasis vienetas**.

- Įsitikinkite, kad visų „Supply Chain Management” produktų pardavimo MV pateikiami „Sales“.
- Įsitikinkite, kad „Sales“ nustatyti kainoraščiai, atitinkantys kiekvieno produkto pardavimo valiutą „Supply Chain Management”.
- „Sales“ sukūrus produktų, jiems gali būti suteikta būsena **Juodraštis** arba **Aktyvus**. Veikimas valdomas „Sales“ parinktyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas**.

    Sukūrus būsenos **Juodraštis** produktų, šie turi būti suaktyvinti prieš tai, kai juos galima įtraukti į pasiūlymus arba pardavimo užsakymus.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktoje iliustracijoje vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas. 

> [!NOTE]
> Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Supply Chain Management“.

![Šablono susiejimas duomenų integratoriuje.](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-articles"></a>Susiję straipsniai

[Potencialaus kliento pavertimas pinigais](prospect-to-cash.md)

[Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais](accounts-template-mapping-direct.md)

[Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais](contacts-template-mapping-direct.md)

[Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir „Supply Chain Management”](sales-order-template-mapping-direct-two-ways.md)

[Tiesioginis „Supply Chain Management“ pardavimo SF antraščių ir eilučių sinchronizavimas su „Sales“](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
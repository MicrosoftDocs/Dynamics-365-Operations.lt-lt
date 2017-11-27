---
title: "Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimo) produktus sinchronizuojant su „Microsoft Dynamics 365 for Sales“."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 405a6cf9f3e6cc52925ff7d9f10836196343c36b
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai susipažinkite su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration). 

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimo) produktus sinchronizuojant su „Microsoft Dynamics 365 for Sales“.

## <a name="template-and-task"></a>Šablonai ir užduotys

Toliau nurodyti šablonai ir pagrindinės užduotys naudojami „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo („Finance and Operations“) produktus sinchronizuojant su „Microsoft Dynamics 365 for Sales“.

-   Šablono pavadinimas: Produktai (iš „Finance and Operations“ į „Sales“)

-   Projekto užduoties pavadinimas: Produktai

Prieš sinchronizuojant produktus būtina sinchronizuoti užduotis: Nėra

## <a name="entity-set"></a>Objektų rinkinys

| **Finance and Operations** | **CDS** | **Pardavimas**  |
|----------------------------|---------|------------|
| Parduodami išleisti produktai | Produktas | Produktai   |

## <a name="entity-flow"></a>Objekto srautas

Produktai tvarkomi „Finance and Operations“ ir sinchronizuojami su „Sales“. „Finance and Operations“ duomenų objektas **Parduodami patvirtinti produktai** eksportuoja tik parduodamus produktus, tai reiškia, kad nurodyta produktų informacija, reikalinga juos norint naudoti pardavimo užsakyme. Tos pačios taisyklės taikomos, kai produktas patvirtinamas naudojant puslapio **Patvirtintas produktas** funkciją **Tikrinti**.

**Produkto numeris** naudojamas kaip raktas, t. y. produkto variantai sinchronizuojami su CDS ir „Sales“ naudojant atskirus **produkto varianto** **produkto ID**.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Į „Sales“ įtrauktas naujas produktų laukas **Tvarkomas išoriškai**, kad būtų galima nurodyti, jog tam tikras produktas yra tvarkomas išoriškai. Pagal numatytuosius parametrus importuojant į „Sales“ reikšmė nustatyta į parinktį **Taip**.

-   **Tvarkomas išoriškai = Taip**: produktas paimtas iš „Finance and Operations“ ir jo nebus galima redaguoti „Sales“.

-   **Tvarkomas išoriškai = Ne**: produktas įvestas tiesiogiai į „Sales“.

-   **Tvarkomas išoriškai = Tuščia**: produktas įtrauktas į „Sales“ prieš įjungiant sprendimą Potencialūs klientai ir grynieji pinigai.

Parinkties **Tvarkomas išoriškai** informacija naudojama norint užtikrinti, kad su „Finance and Operations“ bus sinchronizuojami tik **Pasiūlymai** ir **Pardavimo užsakymai** su **išoriškai tvarkomais produktais**.

**Išoriškai tvarkomi produktai** automatiškai įtraukiami į pirmąjį tinkamą **kainoraštį** ta pačia valiuta. Atkreipkite dėmesį, kad sąrašas rikiuojamas abėcėlės tvarka pagal **pavadinimą**. „Finance and Operations“ produkto pardavimo kaina naudojama kaip **kainoraščio** kaina. Tai reiškia, kad „Sales“ turi būti sukurtas **Kainoraštis**, skirtas kiekvienai atskirai „Finance and Operations“ **produkto pardavimo valiutai**. Patvirtintų parduodamų produktų valiuta nustatyta į juridinio subjekto, iš kurio produktas eksportuojamas, apskaitos valiutą.

> [!NOTE]
> Produkto sinchronizavimo nepavyks atlikti, jei nebus valiutą atitinkančio **kainoraščio**.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

-   Prieš sinchronizuojant pirmą kartą, **Išskirtųjų produktų lentelė** turi būti užpildyta naudojant „Finance and Operations“ esamus produktus. Esami produktai nebus sinchronizuojami, kol ši užduotis nebus baigta.

    -   „Finance and Operations“ naudokite parinktį Ieška, norėdami rasti parinktį **Automatiškai įvesti išskirtųjų produktų lentelę**.

    -   Norėdami vykdyti užduotį spustelėkite parinktį **Automatiškai įvesti išskirtųjų produktų lentelę**. Šią užduotį reikia vykdyti tik vieną kartą.

-   Įsitikinkite, kad **Source -\> CDS susiejime (SalesUnitSymbol / DefaultSellingUnitOfMeasure**) yra būtina „Finance and Operations“ pardavimo **matavimo vieneto** (MV) **Reikšmių schema**.

-   Atnaujinkite **CDS organizacijos ID (Organization_OrganizationId)** dalyje **Šaltinis \> CDS**.

    -   Numatytoji šablono reikšmė yra ORG001.

-   Atnaujinkite **vienetų grupės** (**defaultuomscheduleid.name**) **reikšmių schemą** dalyje **CDS -\> Paskirties vieta**, kad ji atitiktų „Sales“ **vienetų grupes**.

    -   Numatytoji šablono reikšmė **Numatytasis vienetas**.

-   Naudodami **Išrinkimo dokumentai** reikšmę įsitikinkite, kad visų „Finance and Operations“ produktų pardavimo MV pateikiami „Sales“.

-   Įsitikinkite, „Sales“ nustatyti **Kainoraščiai**, atitinkantys kiekvieno produkto pardavimo valiutą „Finance and Operations“.

-   „Sales“ produktus galima kurti nustatant būseną **Juodraštis** arba **Aktyvus**. Tai valdoma naudojant „Sales“ **sistemos parametrus**, pateikiamus dalyje **Pardavimas**.

    -   Produktus, sukurtus naudojant juodraščio būseną, reikia suaktyvinti, kad juos būtų galima įtraukti į **pasiūlymą** arba **pardavimo užsakymą**.

## <a name="template-mapping-in-data-integrator"></a>Šablono susiejimas duomenų integratoriuje

Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.

![šablono susiejimas duomenų integratoriuje](./media/products-template-mapping-data-integrator-1.png)

![produktų šablono susiejimas duomenų integratoriuje](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Susijusios temos

[Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais](accounts-template-mapping.md)

[Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais](contacts-template-mapping.md)

[Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“](sales-quotation-template-mapping.md)

[Sinchronizuoti „Finance and Operations“ pardavimo užsakymo antraštes ir eilutes su „Sales“](sales-order-template-mapping.md)

[Sinchronizuoti „Finance and Operations“ pardavimo SF antraštes ir eilutes su „Sales“](sales-invoice-template-mapping.md)



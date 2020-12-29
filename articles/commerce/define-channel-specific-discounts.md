---
title: Apibrėžti konkretaus kanalo nuolaidas
description: Pardavėjai dažnai nustato skirtingas nuolaidas skirtinguose kanaluose. Šioje temoje apžvelgtos sąvokas, kurias turite žinoti, norėdami sukurti konkretaus kanalo nuolaidą.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 539a6f2df46450c5e0fd18ba69501432d6f3fbdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414357"
---
# <a name="define-channel-specific-discounts"></a>Kanalui būdingų nuolaidų nustatymas

[!include [banner](includes/banner.md)]

Šioje temoje apžvelgtos sąvokas, kurias turite žinoti, norėdami sukurti konkretaus kanalo nuolaidą.

## <a name="channel-specific-discounts"></a>Konkretaus kanalo nuolaidos

Pardavėjai dažnai skirtinguose kanaluose siūlo skirtingas nuolaidas. Taip gali būti daroma reaguojant į vietos rinkos sąlygas arba konkuruojant su kitais pardavėjais.

„Commerce“ naudoja kainų grupes konkrečių kanalų nuolaidoms apibrėžti. Kainų grupės gali būti priskirtos vienam ar keliems toliau nurodytiems objektams: kanalams, katalogams, priskyrimams ir lojalumo programoms. Šiame straipsnyje aptariami kanalai, tačiau tos pačios koncepcijos taikomos katalogų nuolaidoms, priskyrimų nuolaidoms ir lojalumo nuolaidoms.

## <a name="price-groups"></a>Kainų grupės

[![Kainų grupės](./media/price-groups-1024x608.png)](./media/price-groups.png)

Aukščiau pateiktoje diagramoje iliustruojamas ryšys tarp galimų operacijos (kanalo, katalogo, priskyrimo, kliento, lojalumo kortelės) objektų ir įvairių nuolaidų tipų, kuriuos galima sukonfigūruoti. Visos operacijos vyksta kanale, todėl kanalas operacijoje tikrai bus. Likę objektai yra neprivalomi. Kiekviename bendrųjų duomenų puslapyje yra saitas į susijusių kainų grupių puslapį, kuriame galite peržiūrėti kainų grupes ir pagal poreikį jų pridėti. Kainų grupė naudojama keturių skirtingų tipų objektams susieti su nuolaidomis, kainų koregavimais ir prekybos sutartimis. Rekomenduojame susiplanuoti strategiją, kaip savo kainų grupes įvardysite, kad jos išliktų susistemintos. Viena galimybė galėtų būti naudoti raidinį arba skaitinį prievardį ar povardį, kad būtų galima atskirti skirtingus tipus. Pavyzdžiui, 1-xxxxx naudoti kanalų kainų grupėms, o 2-xxxxx – katalogų kainų grupėms. Yra keturi užklausų puslapiai, kuriuose dėmesys skiriamas kiekvienam prekybos objektui, su kuriuo gali būti susietos nuolaidos.

- **Kanalo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų kanalų ir nuolaidų sąrašas.
- **Katalogo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų katalogų ir nuolaidų sąrašas.
- **Lojalumo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų lojalumo programų ir nuolaidų sąrašas.
- **Priskyrimo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų priskyrimų ir nuolaidų sąrašas.

## <a name="example-channel-discount-set-up"></a>Kanalo nuolaidos sąrankos pavyzdys

Toliau pateiktame pavyzdyje iliustruojamos užduotys, atliekamos nustatant kanalo nuolaidą.

1. Šiame pavyzdyje turite kanalą pavadinimu **Hiustonas** ir ketinate sukurti naują nuolaidą pavadinimu **Atgal į mokyklą**.
2. Kadangi kainodaros ir nuolaidų strategija apima kanalo nuolaidų galimybę, kurdami kanalą visada sukuriate konkretaus kanalo kainų grupę.
3. Turite kainų grupę **Hiustono KG**, ir ji priskirta **Hiustono** kanalui.
4. Sukūrę naująją nuolaidą **Atgal į mokyklą**, **Nuolaidos** puslapio viršuje turite spustelėti **Kainų grupės**. Atsidarys **Nuolaidos kainų grupių** puslapis. Toliau spustelėkite **Naujas** ir pasirinkite kainų grupę **Hiustono KG**.
5. Dabar galite įgalinti nuolaidą ir ją perduoti į kanalą.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kainų koregavimas ir nuolaidos](price-adjustments-discounts.md)

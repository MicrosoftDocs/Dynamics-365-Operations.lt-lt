---
title: Apibrėžti konkretaus kanalo nuolaidas
description: Pardavėjai dažnai nustato skirtingas nuolaidas skirtinguose kanaluose. Šiame straipsnyje peržiūrios sąvokas, apie kuriuos jums reikia žinoti, kad sukurtumėte nuolaidą konkrečiam kanalui.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.industry: Retail
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
ms.openlocfilehash: f426503a6897a73010b77082f4277b65545bfcc3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273560"
---
# <a name="define-channel-specific-discounts"></a>Kanalui būdingų nuolaidų nustatymas

[!include [banner](includes/banner.md)]

Šiame straipsnyje peržiūrios sąvokas, apie kuriuos jums reikia žinoti, kad sukurtumėte nuolaidą konkrečiam kanalui.

## <a name="channel-specific-discounts"></a>Konkretaus kanalo nuolaidos

Pardavėjai dažnai skirtinguose kanaluose siūlo skirtingas nuolaidas. Taip gali būti daroma reaguojant į vietos rinkos sąlygas arba konkuruojant su kitais pardavėjais.

„Commerce“ naudoja kainų grupes konkrečių kanalų nuolaidoms apibrėžti. Kainų grupės gali būti priskirtos vienam ar keliems toliau nurodytiems objektams: kanalams, katalogams, priskyrimams ir lojalumo programoms. Šiame straipsnyje aptariami kanalai, tačiau tos pačios koncepcijos taikomos katalogų nuolaidoms, priskyrimų nuolaidoms ir lojalumo nuolaidoms.

## <a name="price-groups"></a>Kainų grupės

[![Kainų grupės.](./media/price-groups-1024x608.png)](./media/price-groups.png)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]

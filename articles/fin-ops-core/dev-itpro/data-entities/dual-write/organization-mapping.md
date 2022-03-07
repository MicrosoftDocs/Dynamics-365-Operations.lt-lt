---
title: Organizacijos hierarchija Dataverse
description: Šioje temoje aprašomas organizacinių duomenų integravimas tarp „Finance and Operations“ programų ir „Dataverse“.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: afc1b5996667835c460f467526493380aa2d6403
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062091"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organizacijos hierarchija Dataverse

[!include [banner](../../includes/banner.md)]



Kadangi „Dynamics 365 Finance“ yra finansų sistema, *„organizacija“* yra pagrindinė sąvoka, o sistemos sąranka pradedama nuo organizacijos hierarchijos konfigūracijos. Verslo finansai gali būti stebimi organizacijos lygiu ir taip pat bet kuriuo organizacijos hierarchijos lygiu.

Nors „Dataverse“ neturi organizacijos hierarchijos sąvokos, joje yra kelios laisvos sąvokos, pvz., visų pardavimo įplaukos. Kaip „Dataverse“ integravimo dalis, organizacijos hierarchijos duomenų struktūra įtraukiamą į „Dataverse“

## <a name="data-flow"></a>Duomenų srautas

Verslo ekosistema, kurią sudaro „Finance and Operations“ programos ir „Dataverse“, toliau turės organizacijos hierarchiją. Ši organizacijos hierarchija pagrįsta „Finance and Operations“ programomis, tačiau ji rodoma programoje „Dataverse“ informaciniais ir išplėtimo tikslais. Toliau pateiktame paveikslėlyje pavaizduota organizacijos hierarchijos informacija, kuri rodoma programoje „Dataverse” kaip vienpusis duomenų srautas iš „Finance and Operations“ programų į „Dataverse”.

![Struktūros vaizdas.](media/dual-write-data-flow.png)

Galimi organizacijos hierarchijos lentelių žemėlapiai, leidžiantys vienpusiškai sinchronizuoti duomenis iš „Finance and Operations“ programų į Dataverse.

## <a name="templates"></a>Šablonai

Produkto informacija apima visą su produktu ir jo apibrėžtimi susijusią informaciją, pvz., produkto dimensijas arba sekimo ir saugojimo dimensijas. Kaip parodyta toliau esančioje lentelėje, sukurtas lentelių schemų rinkinys, skirtas produktų ir susijusios informacijos sinchronizavimui.

„Finance and operations” programos | „Customer engagement“ programos     | Aprašas
-----------------------|--------------------------------|---
[Juridiniai subjektai](mapping-reference.md#102) | cdm_companies | Suteikiama juridinio subjekto (įmonės) informacijos dvikrypčio sinchronizavimo galimybė.
[Juridiniai subjektai](mapping-reference.md#142) | msdyn_internalorganizations |
[Valdymo vienetas](mapping-reference.md#143) | msdyn_internalorganizations |
[Organizacijos hierarchija – publikuota](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchija publikuota.
[Organizacijos hierarchijos tikslai](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchijos paskirtis.
[Organizacijos hierarchijos tipas](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchijos tipas.

## <a name="internal-organization"></a>Vidinė organizacija

Vidinės organizacijos informacija „Dataverse“ platformoje gaunama iš dviejų lentelių – **Valdymo vieneto** ir **Juridinių subjektų**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

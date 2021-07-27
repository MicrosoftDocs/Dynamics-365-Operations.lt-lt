---
title: Organizacijos hierarchija Dataverse
description: Šioje temoje aprašomas organizacijos duomenų integravimas tarp programų „Finance and Operations“ ir „Dataverse“.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 77625e6e80bfa45add6839df89d9aae27e41d456
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355303"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organizacijos hierarchija Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Kadangi „Dynamics 365 Finance“ yra finansų sistema, *„organizacija“* yra pagrindinė sąvoka, o sistemos sąranka pradedama nuo organizacijos hierarchijos konfigūracijos. Verslo finansai gali būti stebimi organizacijos lygiu ir taip pat bet kuriuo organizacijos hierarchijos lygiu.

Nors „Dataverse“ neturi organizacijos hierarchijos sąvokos, joje yra kelios laisvos sąvokos, pvz., visų pardavimo įplaukos. Kaip „Dataverse“ integravimo dalis, organizacijos hierarchijos duomenų struktūra įtraukiamą į „Dataverse“

## <a name="data-flow"></a>Duomenų srautas

Verslo ekosistema, kurią sudaro programos „Finance and Operations“ ir „Dataverse“, ir toliau turės organizacijos hierarchiją. Ši organizacijos hierarchija yra sukurta programose „Finance and Operations“, tačiau ji rodoma ir „Dataverse“ informacijos ir išplėtimo tikslais. Toliau pateiktoje iliustracijoje parodyta organizacijos hierarchijos informacija, kuri rodoma „Dataverse“ kaip vienpusis duomenų srautas iš programų „Finance and Operations“ į „Dataverse“.

![Struktūros vaizdas.](media/dual-write-data-flow.png)

Organizacijos hierarchijos lentelių schemos yra prieinamos duomenų sinchronizavimui į vieną pusę iš programų „Finance and Operations“ į „Dataverse“.

## <a name="templates"></a>Šablonai

Produkto informacija apima visą su produktu ir jo apibrėžtimi susijusią informaciją, pvz., produkto dimensijas arba sekimo ir saugojimo dimensijas. Kaip parodyta toliau esančioje lentelėje, sukurtas lentelių schemų rinkinys, skirtas produktų ir susijusios informacijos sinchronizavimui.

„Finance and Operations” programėlės | Kitos „Dynamics 365” programos | aprašymas
-----------------------|--------------------------------|---
Organizacijos hierarchijos tikslai | msdyn_internalorganizationhierarchypurposes | Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchijos paskirtis.
Organizacijos hierarchijos tipas | msdyn_internalorganizationhierarchytypes | Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchijos tipas.
Organizacijos hierarchija – publikuota | msdyn_internalorganizationhierarchies | Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchija publikuota.
Valdymo vienetas | msdyn_internalorganizations |
Juridiniai subjektai | msdyn_internalorganizations |
Juridiniai subjektai | cdm_companies | Suteikiama juridinio subjekto (įmonės) informacijos dvikrypčio sinchronizavimo galimybė.

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Vidinė organizacija

Vidinės organizacijos informacija, esanti „Dataverse“ gaunama iš dviejų lentelių – **valdymo vieneto** ir **juridinių subjektų**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
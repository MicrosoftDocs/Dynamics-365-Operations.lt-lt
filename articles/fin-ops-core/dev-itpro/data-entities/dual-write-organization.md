---
title: Organizacijos hierarchija Common Data Service
description: Šioje temoje aprašomas organizacinių duomenų integravimas tarp „Finance and Operations“ programų ir „Common Data Service“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182030"
---
## <a name="organization-hierarchy-in-common-data-service"></a>Organizacijos hierarchija Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Kadangi „Dynamics 365 Finance“ yra finansų sistema, *„organizacija“* yra pagrindinė sąvoka, o sistemos sąranka pradedama nuo organizacijos hierarchijos konfigūracijos. Verslo finansai gali būti stebimi organizacijos lygiu ir taip pat bet kuriuo organizacijos hierarchijos lygiu.

Nors „Common Data Service“ neturi organizacijos hierarchijos sąvokos, joje yra kelios laisvos sąvokos, pvz., visų pardavimo įplaukos. Kaip „Common Data Service“ integravimo dalis, organizacijos hierarchijos duomenų struktūra įtraukiamą į „Common Data Service“

## <a name="data-flow"></a>Duomenų srautas

Verslo ekosistema, kurią sudaro „Finance and Operations“ programos ir „Common Data Service“, toliau turės organizacijos hierarchiją. Ši organizacijos hierarchija pagrįsta „Finance and Operations“ programomis, tačiau ji rodoma programoje „Common Data Service“ informaciniais ir išplėtimo tikslais. Toliau pateiktame paveikslėlyje pavaizduota organizacijos hierarchijos informacija, kuri rodoma programoje „Common Data Service” kaip vienpusis duomenų srautas iš „Finance and Operations“ programų į „Common Data Service”.

![Struktūros vaizdas](media/dual-write-data-flow.png)

## <a name="templates"></a>Šablonai

Organizacijos hierarchijos objekto schemos prieinamos vienpusiui duomenų sinchronizavimui iš „Finance and Operations“ programų į „Common Data Service”.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Prižiūrėti organizacijos hierarchijos paskirtis

Šis šablonas pateikia organizacijos hierarchijos paskirties objekto vienpusį sinchronizavimą iš „Finance and Operations“ į kitas „Dynamics 365“ programas.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
Hierarchijos tipas | \> | msdyn\_hierarchypurposetypename
Hierarchijos tipas | \> | msdyn\_hierarchytype.msdyn\_name
Hierarchijos paskirtis | \>\> | msdyn\_hierarchypurpose
Nekintamas | \>\> | msdyn\_immutable
Nustatyti kaip numatytąją | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Vidinis organizacijos hierarchijos tipas

Šis šablonas pateikia organizacijos hierarchijos tipo objekto vienpusį sinchronizavimą iš „Finance and Operations“ į kitas „Dynamics 365“ programas.

<!-- ![architecture image](media/dual-write-type.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
PAVADINIMAS | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>Vidinis organizacijos hierarchija

Šis šablonas pateikia organizacijos hierarchijos publikuoto objekto vienpusį sinchronizavimą iš „Finance and Operations“ į kitas „Dynamics 365“ programas.

<!-- ![architecture image](media/dual-write-organization.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
Galioja iki | \> | msdyn\_validto
Galioja nuo | \> | msdyn\_validfrom
Hierarchijos tipas | \> | msdyn\_hierarchytypename
Pirminės organizacijos įrašo numeris | \> | msdyn\_parentpartyid
Antrinės organizacijos įrašo numeris | \> | msdyn\_childpartyid
Hierarchijos tipas | \> | msdyn\_hierarchytypeid.msdyn\_name
Antrinės organizacijos įrašo numeris | \> | msdyn\_childid.msdyn\_partynumber
Pirminės organizacijos įrašo numeris | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Vidinė organizacija

Vidinės organizacijos informacija, esanti „Common Data Service“ gaunama iš dviejų objektų – **valdymo vieneto** ir **juridinių subjektų**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Valdymo vienetas

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
Kalbos ID | \> | msdyn\_languageid
Vardo pseudonimas | \> | msdyn\_namealias
PAVADINIMAS | \> | msdyn\_name
Įrašo numeris | \> | msdyn\_partynumber
Valdymo vienetų tipai | \>\> | msdyn\_type

### <a name="legal-entity"></a>Juridinis subjektas

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
Vardo pseudonimas | \> | msdyn\_namealias
Kalbos ID | \> | msdyn\_languageid
PAVADINIMAS | \> | msdyn\_name
Įrašo numeris | \> | msdyn\_partynumber
nėra | \>\> | msdyn\_type
Juridinio subjekto ID | \> | msdyn\_companycode

## <a name="company"></a>Įmonė

Pateikia juridinio subjekto (įmonės) informacijos dvikryptį sinchronizavimą tarp „Finance and Operations“ ir ir kitų „Dynamics 365” programų.

<!-- ![architecture image](media/dual-write-company.png) -->

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
PAVADINIMAS | = | cdm\_name
Juridinio subjekto ID | = | cdm\_companycode

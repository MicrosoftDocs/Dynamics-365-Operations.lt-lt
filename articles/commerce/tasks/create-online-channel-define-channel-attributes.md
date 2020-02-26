---
title: Kurti interneto kanalą ir nurodyti kanalo atributus
description: Ši procedūra padeda kurti naują interneto kanalą ir įtraukti jį į organizacijos hierarchiją.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bac365217c20bececa1b4ff2b9de12288326dcc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023415"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Kurti interneto kanalą ir nurodyti kanalo atributus

[!include[task guide banner](../includes/task-guide-banner.md)]

Ši procedūra padeda kurti naują interneto kanalą ir įtraukti jį į organizacijos hierarchiją. Prieš kurdami naują interneto kanalą, turite sukurti organizacijos hierarchiją. Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.


## <a name="create-a-new-online-channel"></a>Naujo interneto kanalo kūrimas
1. Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Interneto parduotuvės.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Lauke Sandėlis įveskite arba pasirinkite reikšmę.
5. Lauke Saugojimo laiko juosta pasirinkite parinktį.
6. Lauke Numatytasis klientas įveskite arba pasirinkite reikšmę.
7. Lauke Kliento adresų knygelė įveskite arba pasirinkite reikšmę.
8. Lauke Mokėjimo sąlygos įveskite arba pasirinkite reikšmę.
9. Lauke Mokėjimo metodas įveskite arba pasirinkite vertę.
10. Lauke El. paštu siunčiamo pranešimo šablonas įveskite arba pasirinkite reikšmę.
11. Išplėskite sekciją Finansinės dimensijos.
12. Lauke „BusinessUnit“ įveskite arba pasirinkite reikšmę.
    * Taip pat nustatykite visų kitų numatytųjų dimensijų reikšmes.  
13. Spustelėkite Įrašyti.

## <a name="add-the-online-channel-to-organization-hierarchy"></a>Interneto kanalo įtraukimas į organizacijos hierarchiją
1. Uždarykite puslapį.
2. Pasirinkite Organizacijos administravimas > Organizacijos > Organizacijų hierarchijos.
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Spustelėkite Peržiūrėti.
5. Spustelėkite Redaguoti.
    * Galite pasirinkti bet kurį hierarchijos mazgą, į kurį norite įterpti naują kanalą.  
6. Spustelėkite Įterpti.
7. Spustelėkite kanalą Prekyba.
8. Spustelėkite Gerai.
9. Spustelėdami Publikuoti atidarykite išplečiamąjį dialogo langą.
10. Lauke Įsigaliojimo data įveskite datą ir laiką.
11. Spustelėkite Publikuoti.

## <a name="configure-orders-for-near-real-time-notification"></a>Užsakymų konfigūravimas norint nustatyti beveik realiuoju laiku teikiamus pranešimus
1. Eikite į Mažmeninė prekyba ir prekyba > Būstinės sąranka > Parametrai > Prekybos parametrai.
2. Nustatykite parinkties Naudoti realiojo laiko paslaugą norint sukurti „eCommerce“ užsakymą vertę Taip.
3. Naudodami 1070 paskirstymo grafiką sinchronizuokite kanalo duomenų bazės pakeitimus. 



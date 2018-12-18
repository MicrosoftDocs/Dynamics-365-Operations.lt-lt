---
title: Darbo eigos sistema
description: "Šioje temoje aprašyta „Microsoft Dynamics 365 for Finance and Operations“ darbo eigos sistema."
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 770796b42e79ad616b469e1dbf5149789bff0788
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="workflow-system"></a>Darbo eigos sistema

[!include [banner](../includes/banner.md)]

Šioje temoje aprašyta „Microsoft Dynamics 365 for Finance and Operations“ darbo eigos sistema.

## <a name="what-is-workflow"></a>Kas yra darbo eiga?

Terminą *darbo eiga* galima apibrėžti dviem būdais: kaip sistemą ir kaip veiklos procesą.

### <a name="workflow-is-a-system"></a>Darbo eiga yra sistema

Darbo eiga yra sistema, diegiama kartu su „Finance and Operations“ ir veikianti programos objektų serveryje (AOS). Darbo eigos sistema turi funkcijų, kurias galite naudoti atskiroms darbo eigoms arba verslo procesams kurti.

### <a name="workflow-is-a-business-process"></a>Darbo eiga yra verslo procesas

Darbo eiga rodo verslo procesą. Ji apibrėžia, kaip dokumentas juda sistemoje, parodydama, kas turi įvykdyti užduotį, priimti sprendimą ar patvirtinti dokumentą. Pavyzdžiui, toliau pateikiamoje iliustracijoje rodoma išlaidų ataskaitų darbo eiga.

![Darbo eiga, kurios elementai priskirti vartotojams](./media/workflow_user.gif)

Norėdami geriau suprasti šią darbo eigą, įsivaizduokite, kad Semas pateikia 7 000 USD išlaidų ataskaitą. Tokiu atveju Ivanas turi peržiūrėti Semo jam pateiktus kvitus. Tada Frank ir Sue turi patvirtinti išlaidų ataskaitą. O dabar tarkime, kad Semas pateikia 11 000 USD išlaidų ataskaitą. Tokiu atveju Ivanas turi peržiūrėti kvitus, o Frenkas, Sju ir Ana turi patvirtinti išlaidų ataskaitą.

## <a name="benefits-of-using-the-workflow-system"></a> Darbo eigos sistemos naudojimo privalumai

Darbo eigos sistemos naudojimas jūsų organizacijoje duoda keleriopos naudos:

- **Procesų nuoseklumas** – galite nustatyti, kaip apdorojami konkretūs dokumentai, pvz., pirkimo paraiškos ir išlaidų ataskaitos. Naudodamiesi darbo eigos sistema užtikrinate, kad dokumentai bus apdoroti ir patvirtinti nuosekliai ir veiksmingai.
- **Proceso matomumas** – galite sekti darbo eigos egzempliorių efektyvumo metriką. Tai padeda nustatyti, ar reikia atlikti darbo eigos pokyčius, siekiant gerinti efektyvumą.
- **Centralizuotas darbų sąrašas** – vartotojai gali peržiūrėti centralizuotų darbų sąrašą, kuriame rodomos jiems priskirtos darbo eigos užduotys ir patvirtinimai.


## <a name="workflow-content"></a>Darbo eigos turinys

+ [Darbo eigos architektūra](workflow-system-architecture.md)
+ [Darbo eigos elementai](workflow-elements.md)
+ [Darbo eigos veiksmai](workflow-actions.md)
+ [Darbo eigos kūrimas](create-workflow.md)
+ [Darbo eigos ypatybių konfigūravimas](configure-workflow-properties.md)
+ [Neautomatizuotos darbo eigos užduoties konfigūravimas](configure-manual-task-workflow.md)
+ [Automatizuotos darbo eigos užduoties konfigūravimas](configure-automated-task-workflow.md)
+ [Darbo eigos patvirtinimo proceso konfigūravimas](configure-approval-process-workflow.md)
+ [Darbo eigos patvirtinimo veiksmo konfigūravimas](configure-approval-step-workflow.md)
+ [Neautomatizuoto darbo eigos sprendimo konfigūravimas](configure-manual-decision-workflow.md)
+ [Sąlyginio darbo eigos sprendimo konfigūravimas](configure-conditional-decision-workflow.md)
+ [Lygiagrečios darbo eigos veiklos konfigūravimas](configure-parallel-activity-workflow.md)
+ [Lygiagrečios darbo eigos šakos konfigūravimas](configure-parallel-branch-workflow.md)
+ [Eilutės elemento darbo eigos konfigūravimas](configure-line-item-workflow.md)


---
title: Darbo eigos sistemos apžvalga
description: Šioje temoje aprašyta darbo eigų sistema.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e5e795ca6f7831ecd3fa28be9782f0b287eea6e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190010"
---
# <a name="workflow-system-overview"></a>Darbo eigos sistemos apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje aprašyta darbo eigų sistema.

## <a name="what-is-workflow"></a>Kas yra darbo eiga?

Terminą *darbo eiga* galima apibrėžti dviem būdais: kaip sistemą ir kaip veiklos procesą.

### <a name="workflow-is-a-system"></a>Darbo eiga yra sistema

Darbo eiga yra sistema, veikianti programos objektų serveryje (AOS). Darbo eigos sistema turi funkcijų, kurias galite naudoti atskiroms darbo eigoms arba verslo procesams kurti.

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
+ [DUK apie darbo eigas](workflow-FAQ.md)
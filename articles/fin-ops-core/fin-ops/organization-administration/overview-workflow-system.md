---
title: Darbo eigos sistemos apžvalga
description: Šioje temoje aprašyta darbo eigų sistema.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd8fba1376dc5e3dbfea888ca5ff5fdeb608fc9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560706"
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

## <a name="benefits-of-using-the-workflow-system"></a>Darbo eigos sistemos naudojimo privalumai

Darbo eigos sistemos naudojimas jūsų organizacijoje duoda keleriopos naudos:

- **Procesų nuoseklumas** – galite nustatyti, kaip apdorojami konkretūs dokumentai, pvz., pirkimo paraiškos ir išlaidų ataskaitos. Naudodamiesi darbo eigos sistema užtikrinate, kad dokumentai bus apdoroti ir patvirtinti nuosekliai ir veiksmingai.
- **Proceso matomumas** – galite sekti darbo eigos egzempliorių efektyvumo metriką. Tai padeda nustatyti, ar reikia atlikti darbo eigos pokyčius, siekiant gerinti efektyvumą.
- **Centralizuotas darbų sąrašas** – vartotojai gali peržiūrėti centralizuotų darbų sąrašą, kuriame rodomos jiems priskirtos darbo eigos užduotys ir patvirtinimai.


## <a name="workflow-content"></a>Darbo eigos turinys

+ [Darbo eigos sistemos architektūra](workflow-system-architecture.md)
+ [Darbo eigos elementai](workflow-elements.md)
+ [Darbo eigos patvirtinimo procesų veiksmai](workflow-actions.md)
+ [Darbo eigų kūrimo apžvalga](create-workflow.md)
+ [Darbo eigos ypatybių konfigūravimas](configure-workflow-properties.md)
+ [Neautomatizuotų darbo eigos užduočių konfigūravimas](configure-manual-task-workflow.md)
+ [Automatizuotų darbo eigos užduočių konfigūravimas](configure-automated-task-workflow.md)
+ [Darbo eigos patvirtinimo procesų konfigūravimas](configure-approval-process-workflow.md)
+ [Darbo eigos patvirtinimo veiksmų konfigūravimas](configure-approval-step-workflow.md)
+ [Neautomatinių darbo eigos sprendimų konfigūravimas](configure-manual-decision-workflow.md)
+ [Sąlyginių darbo eigos sprendimų konfigūravimas](configure-conditional-decision-workflow.md)
+ [Lygiagrečių darbo eigos veiklų konfigūravimas](configure-parallel-activity-workflow.md)
+ [Lygiagrečių darbo eigos šakų konfigūravimas](configure-parallel-branch-workflow.md)
+ [Eilutės elemento darbo eigų konfigūravimas](configure-line-item-workflow.md)
+ [DUK apie darbo eigas](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
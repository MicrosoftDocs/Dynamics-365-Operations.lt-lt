---
title: Pirkimo užsakymo pakartotinio išdavimo į darbo eigą po pakeitimo klaida
description: Pirkimo užsakymo pakartotinio išdavimo į darbo eigą po pakeitimo klaida
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477139"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Pirkimo užsakymo pakartotinio išdavimo į darbo eigą po pakeitimo klaida


## <a name="symptoms"></a>Požymiai

Ši klaida įvyksta darbo eigoje, kai pirkimo užsakymas iš naujo pateikiamas po jo pakeitimo:

> Sustabdyta (klaida): X++ Išimtis: Pirkimo užsakymo PO0000569 pakeitimai leidžiami tik būsenos juodraštyje, kai įjungiamas keitimų valdymas<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

Ši problema kyla tik tada, kai pirkimo užsakymo būsena buvo *Patvirtinta* dar prieš tai, kai pareikalavote pakeitimų. Jei pareikalaujate pakeitimų, kai pirkimo užsakymo būsena yra *Patvirtinta*, tada darbo eigą pavyks sėkmingai apdoroti.

## <a name="resolution"></a>Sprendimas

Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.

Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**. Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Problema bus išspręsta naudojant [šį „Microsoft” žinių bazės (KB) straipsnį](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

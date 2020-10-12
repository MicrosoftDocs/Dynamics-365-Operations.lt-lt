---
title: Įsigijimo trikčių diagnostika ir šaltinio pasirinkimo darbo eigos
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti dirbant su įsigijimo ir šaltinio pasirinkimo darbo eigomis.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 940a6c39ac83e7388d4e1a08b656b75df81ed801
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834396"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>Įsigijimo trikčių diagnostika ir šaltinio pasirinkimo darbo eigos

Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti dirbant su įsigijimo ir šaltinio pasirinkimo darbo eigomis.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>Klaida iš naujo pateikiant pirkimo užsakymą darbo eigai po pakeitimo: „Pirkimo užsakymo X pakeitimai yra leidžiami tik juodraštyje, kai suaktyvinamas keitimų valdymas”

Ši problema kyla tik tada, kai pirkimo užsakymo būsena buvo *Patvirtinta* dar prieš tai, kai pareikalavote pakeitimų. Jei pareikalaujate pakeitimų, kai pirkimo užsakymo būsena yra *Patvirtinta*, tada darbo eigą pavyks sėkmingai apdoroti.

### <a name="error-description"></a>Klaidos aprašas

Ši klaida įvyksta darbo eigoje, kai pirkimo užsakymas iš naujo pateikiamas po jo pakeitimo:

> Sustabdyta (klaida): X++ Išimtis: Pirkimo užsakymo PO0000569 pakeitimai leidžiami tik būsenos juodraštyje, kai įjungiamas keitimų valdymas<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>Problemos paaiškinimas

Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.

Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**. Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Problema bus išspręsta naudojant [šį „Microsoft” žinių bazės (KB) straipsnį](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Vienas ar daugiau apskaitos paskirstymų yra paskirstytas per daug arba per mažai.

Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.

Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**. Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>Jei pristatymo likutis atšaukiamas pirkimo užsakyme, kur įjungtas keitimų valdymas, pirkimo užsakymo būsena yra patvirtinta.

### <a name="issue-description"></a>Problemos aprašas

Jei vienintelis prašomas pirkimo užsakymo, kuriam taikomas keitimų valdymas, pakeitimas yra pristatymo likučio panaikinimas vienoje ar keliose eilutėse, pirkimo užsakymas bus priskirtas tiesiai į *Patvirtintą* būseną, kai jis bus patvirtintas, o žurnalas nebus sukurtas.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Pristatymo likučio atšaukimas nedaro poveikio patvirtinimo žurnalo turiniui. Ši funkcija turėtų būti naudojama, kai eilutė buvo gauta iš dalies ir likučio kiekis turėtų būti atšauktas proceso etape po to, kai pirkimo užsakymas yra patvirtintas tiekėjo.

Jei tai turi atsispindėti pirkimo užsakymo patvirtinime, kiekis turi būti pakoreguotas pirkimo užsakymo eilutėje, kad būtų reikalingas patvirtinimas. Taip pat, jei eilutėje nieko negauta, kiekis gali būti pašalintas. Šiuo atveju reikės patvirtinti iš naujo.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>Atšaukti pirkimo užsakymai rodomi juodraštyje, esančiame pirkimo užsakymo paruošimo darbo srityje.

### <a name="issue-description"></a>Problemos aprašas

Atšaukus pirkimo užsakymus, kurių būsena buvo *Patvirtinta*, atšaukti pirkimo užsakymai vis dar rodomi **Pirkimo užsakymo paruošimo** darbo srities pirkimo užsakymų juodraščių sąraše.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Ši problema kyla tik pirkimo užsakymams, kuriems taikomas keitimų valdymas. Tai įvyksta, nes atšaukimas laikomas pakeitimu, kuris turi būti patvirtintas. Šį patvirtinimą sistema gali atlikti automatiškai. Todėl reikalingas procesas pateikti atšauktą pirkimo užsakymą į patvirtinimo darbo eigą, kad jis galėtų patekti į *Patvirtintą* būseną. Tuo metu pirkimo užsakymas nebebus rodomas **Pirkimo užsakymo paruošimo** darbo srities pirkimo užsakymų juodraščių sąraše.


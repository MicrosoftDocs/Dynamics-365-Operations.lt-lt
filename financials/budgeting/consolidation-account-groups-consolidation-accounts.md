---
title: "Konsolidavimo sąskaitų grupės ir papildomos konsolidavimo sąskaitos"
description: "Šioje temoje pateikiama informacija apie konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas bei paaiškinama, kaip jos naudojamos programoje „Microsoft Dynamics 365 for Finance and Operations“ (leidimas „Enterprise‟)."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 3c08e48b22f964c3f643c5ddc4ecd687502d7fda
ms.contentlocale: lt-lt
ms.lasthandoff: 08/01/2017

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolidavimo sąskaitų grupės ir papildomos konsolidavimo sąskaitos

[!include[banner](../includes/banner.md)]


Šioje temoje pateikiama informacija apie konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas bei paaiškinama, kaip jos naudojamos programoje „Microsoft Dynamics 365 for Finance and Operations“ (leidimas „Enterprise‟).

<a name="consolidation-account-groups"></a>Konsolidacijos sąskaitų grupės
----------------------------

Konsolidavimo sąskaitų grupės suteikia galimybę kurti sąskaitų, kurias norite naudoti duomenims konsoliduoti, grupes. Dažniausiai konsolidavimo sąskaitų grupė nurodo vyriausybės įgaliotą sąskaitų planą arba susieja sąskaitas su grupe, kurią nurodo įmonės būstinė. Konsolidavimo sąskaitų grupes galite rasti modulio **Konsolidavimas** srityje **Sąranka**. Įtraukdami naują grupę turite įvesti sąskaitų grupės unikalų identifikatorių ir pavadinimą.

## <a name="additional-consolidation-accounts"></a>Papildomos konsolidacijos sąskaitos
Papildomos konsolidavimo sąskaitos suteikia galimybę sąskaitą iš esamo sąskaitų plano priskirti konsolidavimo sąskaitų grupei. Tada galima nurodyti konsolidavimo sąskaitos vertę ir pavadinimą. 

Papildomas konsolidavimo sąskaitas galite rasti modulio **Konsolidavimas** srityje **Sąranka**. Kurdami naują konsolidavimo sąskaitą turite nurodyti tolesnę informaciją.

-   **Pagrindinė sąskaita** – šis laukas yra peržvalga, kurioje rodomos visos pagrindinės sąskaitos, pagrįstos puslapyje pasirinktu sąskaitų planu. Pasirinkus sąskaitą pavadinimas automatiškai įvedamas lauke **Pagrindinės sąskaitos pavadinimas**.
-   **Konsolidavimo sąskaitų grupė** – naudokite šį lauką norėdami nurodyti grupę, kuriai priskirti sąskaitą. Jei konsoliduojate dviem skirtingais būdais, tą pačią sąskaitą turite įtraukti į visas keturias konsolidavimo sąskaitų grupes.
-   **Konsolidavimo sąskaita** – įveskite konsoliduotos sąskaitos vertę. Ši vertė neprivalo būti sąskaita iš sąskaitų plano. Tai gali būti bet kokia jums reikalinga vertė.
-   **Konsolidavimo sąskaitos pavadinimas** – įveskite sąskaitos, kurią norite rodyti užklausose ir ataskaitose, pavadinimą.
-   **SAT lygis** – šis laukas naudojamas norint teikti sąskaitų išrašų ataskaitas Meksikos mokesčių inspekcijai. 

Baigę kurti konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas, grupę galite pasirinkti vykdydami procesą Konsoliduoti tinkle.


Daugiau informacijos žr. [Konsolidavimo grupių ir papildomų konsolidavimo sąskaitų kūrimas](../general-ledger/tasks/create-consolidation-groups.md). 





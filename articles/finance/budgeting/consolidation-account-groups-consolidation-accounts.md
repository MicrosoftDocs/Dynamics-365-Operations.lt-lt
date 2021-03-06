---
title: Konsolidavimo sąskaitų grupės ir papildomos konsolidavimo sąskaitos
description: Šioje temoje pateikiama informacija apie konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas bei paaiškinama, kaip jos naudojamos programoje „Microsoft Dynamics 365 Finance“.
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 245b61c8cb85ab1282a921ac99b9ac7c2efbadc5
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189426"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolidavimo sąskaitų grupės ir papildomos konsolidavimo sąskaitos

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas bei paaiškinama, kaip jos naudojamos programoje „Microsoft Dynamics 365 Finance“.

## <a name="consolidation-account-groups"></a>Konsolidacijos sąskaitų grupės

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
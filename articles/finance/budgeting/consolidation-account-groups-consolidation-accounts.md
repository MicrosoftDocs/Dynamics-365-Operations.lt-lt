---
title: Konsolidavimo sąskaitų grupės ir papildomos konsolidavimo sąskaitos
description: Šioje temoje pateikiama informacija apie konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas bei paaiškinama, kaip jos naudojamos.
author: panolte
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: kfend
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5ca7a50fcac53f1636da15b2d7977174b087ac25
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711699"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolidavimo sąskaitų grupės ir papildomos konsolidavimo sąskaitos

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas bei paaiškinama, kaip jos naudojamos.

## <a name="consolidation-account-groups"></a>Konsolidacijos sąskaitų grupės

Konsolidavimo sąskaitų grupės suteikia galimybę kurti sąskaitų, kurias norite naudoti duomenims konsoliduoti, grupes. Paprastai konsolidavimo sąskaitų grupė pateikia vyriausybės įgaliotą sąskaitų planą. Konsolidavimo sąskaitų grupė taip pat gali susieti sąskaitas su grupe, kuri apibrėžiama įmonės būstinėje. Konsolidavimo sąskaitų grupes galite rasti modulio **Konsolidavimas** srityje **Sąranka**. Pridę naują grupę, įveskite unikalų sąskaitos grupės identifikatorių ir pavadinimą.

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

---
title: „Dynamics 365 Commerce“ kainodaros mechanizmo naudojimas su „Dynamics 365 Sales“
description: Šioje temoje aprašoma, kaip naudoti „Microsoft Dynamics 365 Commerce” kainodaros mechanizmą, norint kurti pardavimo pasiūlymus programoje „Dynamics 365 Sales”.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594923"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>„Dynamics 365 Commerce“ kainodaros mechanizmo naudojimas su „Dynamics 365 Sales“

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip naudoti „Microsoft Dynamics 365 Commerce” kainodaros mechanizmą, norint kurti pardavimo pasiūlymus programoje „Dynamics 365 Sales”.

„Dynamics 365 Commerce“ kainodaros mechanizmas palaiko daugumą įmonių ir vartotojų (B2C) kainodaros scenarijų, pvz., parduotuvės lygio kainodarą, kainodarą pagal priskyrimą ir lojalumą, prekių rinkinio nuolaidas, kiekio nuolaidas ir ribines nuolaidas. Kainodaros mechanizmas naudoja sudėtingas taisykles nustatyti geriausią konkretaus pasiūlymo ar užsakymo kainą.

Kai naudojate [dvigubą rašymą](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), turite tris parinktis savo kainodaros poreikiams. Galite naudoti statinę kainodarą, gaunamą iš „Dynamics 365 Sales“ kainoraščio, „Dynamics 365 Supply Chain Management“ kainodaros mechanizmą arba „Dynamics 365 Commerce“ kainodaros mechanizmą. Iš šių parinkčių „Commerce“ kainodaros mechanizmas geriausiai atitinka B2C scenarijus.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>„Commerce“ kainodaros mechanizmo naudojimas programoje „Sales“

> [!NOTE]
> Šiuo metu „Commerce“ kainodaros mechanizmą galima naudoti tik pasiūlymams kurti programoje „Sales“. „Sales“ užsakymų integravimo su „Commerce“ kainodaros mechanizmu galimybės dar nėra.

Kai vartotojai pradeda pasiūlymą programoje „Sales“, dvigubo rašymo sistema nukopijuoja pasiūlymo informaciją į „Commerce“. Bet kokie esamų pasiūlymo eilučių pakeitimai arba naujai pridėtos „Sales“ pasiūlymo eilutės nukopijuojamos į „Commerce“. Kai vartotojai nori naudoti „Commerce“ kainodaros mechanizmą pasiūlymui įkainoti, jie gali pasirinkti **Įkainoti pasiūlymą** ir atnaujinti pasiūlymo kainas pagal „Commerce“ kainodaros mechanizmą. Kainos tada automatiškai atnaujinamos ir programoje „Sales“, ir „Commerce“.

## <a name="prerequisites"></a>Būtinieji komponentai

- Kad galėtumėte naudoti „Commerce“ kainodaros mechanizmą programoje „Sales“, turite atlikti veiksmus, nurodytus dokumente iš [Potencialių klientų pavertimas grynaisiais pinigais naudojant dvigubo rašymo funkciją](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).
- Turite išjungti prekybos sutarties vertinimą, skirtą neautomatinei įvesčiai, atlikdami tolesnius veiksmus.

    1. Savo „Commerce“ aplinkoje eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
    1. Skirtuko **Kainos**, „FastTab“ **Prekybos sutarties vertinimas** išvalykite žymės langelį **Neautomatinis įvedimas**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Potencialių klientų pavertimas grynaisiais pinigais dvigubo rašymo funkcijoje](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
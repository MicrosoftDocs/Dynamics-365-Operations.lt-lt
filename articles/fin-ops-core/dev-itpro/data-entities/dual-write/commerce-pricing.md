---
title: „Dynamics 365 Commerce“ kainodaros mechanizmo naudojimas su „Dynamics 365 Sales“
description: Šioje temoje aprašoma, kaip naudoti „Microsoft Dynamics 365 Commerce” kainodaros mechanizmą, norint kurti pardavimo pasiūlymus programoje „Dynamics 365 Sales”.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c3f1527e5f37bebba57661ca86b1a3aae7e62da0
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416760"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>„Dynamics 365 Commerce“ kainodaros mechanizmo naudojimas su „Dynamics 365 Sales“

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip naudoti „Microsoft Dynamics 365 Commerce” kainodaros mechanizmą, norint kurti pardavimo pasiūlymus programoje „Dynamics 365 Sales”.

„Dynamics 365 Commerce“ kainodaros mechanizmas palaiko daugumą įmonių ir vartotojų (B2C) kainodaros scenarijų, pvz., parduotuvės lygio kainodarą, kainodarą pagal priskyrimą ir lojalumą, prekių rinkinio nuolaidas, kiekio nuolaidas ir ribines nuolaidas. Kainodaros mechanizmas naudoja sudėtingas taisykles nustatyti geriausią konkretaus pasiūlymo ar užsakymo kainą.

Kai naudojate [dvigubą rašymą](./dual-write-overview.md), turite tris parinktis savo kainodaros poreikiams. Galite naudoti statinę kainodarą, gaunamą iš „Dynamics 365 Sales“ kainoraščio, „Dynamics 365 Supply Chain Management“ kainodaros mechanizmą arba „Dynamics 365 Commerce“ kainodaros mechanizmą. Iš šių parinkčių „Commerce“ kainodaros mechanizmas geriausiai atitinka B2C scenarijus.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>„Commerce“ kainodaros mechanizmo naudojimas programoje „Sales“

> [!NOTE]
> Šiuo metu „Commerce“ kainodaros mechanizmą galima naudoti tik pasiūlymams kurti programoje „Sales“. „Sales“ užsakymų integravimo su „Commerce“ kainodaros mechanizmu galimybės dar nėra.

Kai vartotojai pradeda pasiūlymą programoje „Sales“, dvigubo rašymo sistema nukopijuoja pasiūlymo informaciją į „Commerce“. Bet kokie esamų pasiūlymo eilučių pakeitimai arba naujai pridėtos „Sales“ pasiūlymo eilutės nukopijuojamos į „Commerce“. Kai vartotojai nori naudoti „Commerce“ kainodaros mechanizmą pasiūlymui įkainoti, jie gali pasirinkti **Įkainoti pasiūlymą** ir atnaujinti pasiūlymo kainas pagal „Commerce“ kainodaros mechanizmą. Kainos tada automatiškai atnaujinamos ir programoje „Sales“, ir „Commerce“.

## <a name="prerequisites"></a>Būtinieji komponentai

- Kad galėtumėte naudoti „Commerce“ kainodaros mechanizmą programoje „Sales“, turite atlikti veiksmus, nurodytus dokumente iš [Potencialių klientų pavertimas grynaisiais pinigais naudojant dvigubo rašymo funkciją](./dual-write-prospect-to-cash.md).
- Turite išjungti prekybos sutarties vertinimą, skirtą neautomatinei įvesčiai, atlikdami tolesnius veiksmus.

    1. Savo „Commerce“ aplinkoje eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
    1. Skirtuko **Kainos**, „FastTab“ **Prekybos sutarties vertinimas** išvalykite žymės langelį **Neautomatinis įvedimas**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Potencialių klientų pavertimas grynaisiais pinigais dvigubo rašymo funkcijoje](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
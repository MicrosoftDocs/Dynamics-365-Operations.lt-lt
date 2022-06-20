---
title: „Dynamics 365 Commerce“ kainodaros mechanizmo naudojimas su „Dynamics 365 Sales“
description: Šiame straipsnyje aprašoma, kaip naudoti kainodaros Microsoft Dynamics 365 Commerce modulį pardavimo pasiūlymams sukurti "Dynamics 365" pardavimams.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 11a164ec15c8b7a69172a153b961011a8b324712
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881400"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>„Dynamics 365 Commerce“ kainodaros mechanizmo naudojimas su „Dynamics 365 Sales“

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti kainodaros Microsoft Dynamics 365 Commerce modulį pardavimo pasiūlymams sukurti "Dynamics 365" pardavimams.

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
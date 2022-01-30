---
title: Kanalų apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ kanalų apžvalga.
author: samjarawan
ms.date: 01/27/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: cc7f00d69a6fd57efcd9b6eece56ddc0702c6935
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985010"
---
# <a name="channels-overview"></a>Kanalų apžvalga


[!include [banner](includes/banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ kanalų apžvalga. Jame pateikiama informacija apie užduotis, kurias turite atlikti prieš ir po kiekvieno kanalo nustatymo.

## <a name="types-of-channels"></a>Kanalų tipai

„Dynamics 365 Commerce“ palaiko tris skirtingus kanalų tipus: mažmeninė prekyba, skambučių centras ir interneto kanalai.

### <a name="retail-channels"></a>Mažmeninės prekybos kanalai

Mažmeninės prekybos kanalai yra standartinės fizinės parduotuvės. Kiekvienoje parduotuvėje yra nuosavi elektroninių kasos aparatų (EKA) registrai, pajamų ir išlaidų sąskaitos bei darbuotojai. 

### <a name="call-center-channels"></a>Skambučių centro kanalai

Skambučių centro kanalai – tai skambučių centro užsakymai ir klientų valdymas.

### <a name="online-channels"></a>Interneto kanalai

Interneto kanalai internetinės el. prekybos vitrinos. Kai sukurtas interneto kanalas, reikia sukurti saitą naudojant „Microsoft Dynamics 365 Commerce“ svetainės generatoriaus įrankį arba kitą trečiosios šalies el. prekybos sprendimą.

## <a name="channel-setup-basics"></a>Kanalo sąrankos pagrindai

Kanalų nustatymas atliekamas naudojant „Commerce“ įrankį. Kiekvienas kanalas gali turėti savo mokėjimo metodus, kainų grupes, produktų hierarchijas, asortimentus ir produktų rinkinius. Kai sukuriate kanalą, galite priskirti produktus, kuriuos norite, kad jis platintų ir parduotų. Kiekvienas kanalo tipas turi unikalų funkcijų rinkinį, kurį gali reikėti sukonfigūruoti. Pavyzdžiui, mažmeninės prekybos kanalui reikia priskirti darbuotojus, registrus ir klientus. Sukūrus naują kanalą, jis turi būti priskirtas organizacijos hierarchijai.

## <a name="channel-setup-prerequisites"></a>Būtinosios kanalo nustatymo sąlygos

Kad galėtumėte nustatyti kanalą, turite atlikti keletą būtinųjų užduočių pagal kanalo tipą. Daugiau informacijos žr. [Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>Kanalo nustatymas

Pabaigę būtinąsias užduotis, tolesnes nustatymo funkcijas žr. toliau pateiktuose saituose.

- [Mažmeninės prekybos kanalo nustatymas](channel-setup-retail.md)
- [Skambučių centro kanalo nustatymas](channel-setup-callcenter.md)
- [Interneto kanalo nustatymas](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Papildomi ištekliai

[Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md)

[Mažmeninės prekybos kanalo nustatymas](channel-setup-retail.md)
    
[Interneto kanalo nustatymas](channel-setup-online.md)

[Skambučių centro kanalo nustatymas](channel-setup-callcenter.md)

[Organizacijų hierarchijų nustatymas](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
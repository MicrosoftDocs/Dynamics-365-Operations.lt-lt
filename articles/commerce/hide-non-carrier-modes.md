---
title: Slėpti ne vežėjo pristatymo būdus EKA siuntimo pasirinktyse
description: Šioje temoje aprašoma konfigūracijos parinktis, kuri neleidžia pasirinkti ne vežėjo pristatymo būdus, kai elektroninio kasos aparato (EKA) programoje kuriami siuntimo užsakymai.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 75e7e8f183982f7829db78eb75b8c29c9ab95e89
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023486"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="c1828-103">Slėpti ne vežėjo pristatymo būdus EKA siuntimo pasirinktyse</span><span class="sxs-lookup"><span data-stu-id="c1828-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c1828-104">Šioje temoje aprašoma konfigūracijos parinktis, kuri galima naudoti elektroninio kasos aparato (EKA) programoje.</span><span class="sxs-lookup"><span data-stu-id="c1828-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="c1828-105">Ši konfigūracijos pasirinktis keičia pristatymo būdo pasirinkimo elgseną, kai EKA kuriami siuntimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="c1828-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="c1828-106">Vartotojai gali pasirinkti siuntos pristatymo būdą, kai kuria kliento siuntimo užsakymus EKA.</span><span class="sxs-lookup"><span data-stu-id="c1828-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="c1828-107">Ši funkcija yra prieinama neatsižvelgiant į tai, ar siunčiamas visas užsakymas, ar tik pasirinktos eilutės.</span><span class="sxs-lookup"><span data-stu-id="c1828-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="c1828-108">Pagal numatytuosius nustatymus dialogo lange, kuriame pasirinktas pristatymo būdas, rodomi visi leistini pristatymo būdai, skirti kanalo, prekės ir pristatymo adreso kombinacijai.</span><span class="sxs-lookup"><span data-stu-id="c1828-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="c1828-109">Šie pristatymo būdai apibrėžti „Headquarters” puslapyje **Pristatymo būdai** (**Pardavimas ir rinkodara \> Sąranka \> Platinimas \> Pristatymo būdai**).</span><span class="sxs-lookup"><span data-stu-id="c1828-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="c1828-110">„Ne vežėjo” pristatymo būdai, pvz., **Išsineštinis** arba**Paėmimas**, taip pat gali būti pasirinkti dialogo lange.</span><span class="sxs-lookup"><span data-stu-id="c1828-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="c1828-111">Tačiau buvo įtraukta funkcija, leidžianti paslėpti ne vežėjo pristatymo būdus dialogo lange.</span><span class="sxs-lookup"><span data-stu-id="c1828-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="c1828-112">Norėdami įjungti šią funkciją, puslapyje **Prekybos parametrai**, skirtuke **Kliento užsakymai**, nustatykite pasirinktį **Rodyti tik vežėjo pristatymo būdus, skirtus užsakymų siuntimui** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c1828-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="c1828-113">Įjungus šią funkciją ir vykdant atitinkamas paskirstymo užduotis, skirtas sinchronizuoti informaciją su kanalo duomenų baze, ne vežėjo pristatymo būdų nebus galima pasirinkti siuntimo užsakymų kūrimo EKA proceso metu.</span><span class="sxs-lookup"><span data-stu-id="c1828-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>

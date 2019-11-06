---
title: Išjungti mažmeninės prekybos operacijų vientisumo tikrintuvo taisykles
description: Šioje temoje aprašomos funkcijos, skirtos išjungti mažmeninės prekybos operacijų vientisumo tikrintuvo taisykles, veikiančias „Microsoft Dynamics 365 Retail“.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586302"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="6f646-103">Išjungti mažmeninės prekybos operacijų vientisumo tikrintuvo taisykles</span><span class="sxs-lookup"><span data-stu-id="6f646-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="6f646-104">Mažmenininkai gali turėti unikalius jiems skirtus verslo scenarijus ir procesus.</span><span class="sxs-lookup"><span data-stu-id="6f646-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="6f646-105">Todėl ne visos taisyklės, kurios pagal numatytuosius nustatymus yra įtrauktos į mažmeninės prekybos operacijų vientisumo tikrintuvą, taikomos visiems mažmenininkams.</span><span class="sxs-lookup"><span data-stu-id="6f646-105">Therefore, not all the rules that are included by default in the retail transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="6f646-106">Norint atsižvelgti į skirtumus, „Microsoft Dynamics 365 Retail” suteikia funkcijas, kurias galima naudoti netaikomoms taisyklėms išjungti.</span><span class="sxs-lookup"><span data-stu-id="6f646-106">To accommodate differences, Microsoft Dynamics 365 Retail provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="6f646-107">Norėdami peržiūrėti sąrašo taisykles, prieinamas mažmeninės prekybos operacijų vientisumo tikrintuve jūsų aplinkoje, ir norėdami peržiūrėti kiekvienos taisyklės būseną, eikite į **Mažmeninė prekyba \> Būstinės sąranka \> Parametrai \> Mažmeninės prekybos parametrai** ir pasirinkite skirtuką **Operacijų tikrinimas**.</span><span class="sxs-lookup"><span data-stu-id="6f646-107">To view the list of rules that are available in the retail transaction consistency checker in your environment, and to see the status of each rule, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="6f646-108">Pagal numatytuosius nustatymus kiekvienos taisyklės būsena nustatyta kaip **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="6f646-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="6f646-109">Todėl visos taisyklės naudojamos mažmeninės prekybos operacijoms patikrinti prieš jas perkeliant į mažmeninės prekybos išrašus.</span><span class="sxs-lookup"><span data-stu-id="6f646-109">Therefore, all the rules are used to validate retail transactions before they are pulled into the retail statements.</span></span> <span data-ttu-id="6f646-110">Norėdami išjungti taisyklę, pakeiskite jos būseną į **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="6f646-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="6f646-111">Į išjungtas taisykles neatsižvelgiama tikrinant mažmeninės prekybos operacijas išrašų apskaičiavimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="6f646-111">Disabled rules aren't considered when retail transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="6f646-112">Norėdami apeiti visą tikrinimo procesą nepaisydami įjungtų taisyklių, eikite į **Mažmeninė prekyba \> Būstinės sąranka \> Parametrai \> Mažmeninės prekybos parametrai** ir tada skirtuke **Operacijų tikrinimas** nustatykite parinktį **Išjungti mažmeninės prekybos operacijų vientisumo tikrintuvą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="6f646-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Retail transactions** option to **Yes**.</span></span> <span data-ttu-id="6f646-113">Nustačius šią parinktį į **Ne**, jos nebus galima nustatyti atgal į **Taip** naudojantis vartotojo sąsaja (UI).</span><span class="sxs-lookup"><span data-stu-id="6f646-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>

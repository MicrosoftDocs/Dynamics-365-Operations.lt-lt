---
title: Išjungti mažmeninės prekybos operacijų vientisumo tikrintuvo taisykles
description: Šioje temoje aprašomos funkcijos, skirtos išjungti mažmeninės prekybos operacijų vientisumo tikrintuvo taisykles, veikiančias „Microsoft Dynamics 365 Commerce“.
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
ms.openlocfilehash: b11b901fafc3907e9d3cae5cd554cc9a868a414c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004348"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="20b65-103">Išjungti mažmeninės prekybos operacijų vientisumo tikrintuvo taisykles</span><span class="sxs-lookup"><span data-stu-id="20b65-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="20b65-104">Mažmenininkai gali turėti unikalius jiems skirtus verslo scenarijus ir procesus.</span><span class="sxs-lookup"><span data-stu-id="20b65-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="20b65-105">Todėl ne visos taisyklės, kurios pagal numatytuosius nustatymus yra įtrauktos į prekybos operacijų vientisumo tikrintuvą, taikomos visiems mažmenininkams.</span><span class="sxs-lookup"><span data-stu-id="20b65-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="20b65-106">Skirtumams suderinti „Microsoft Dynamics 365 Commerce” suteikia funkcijas, kurias galima naudoti netaikomoms taisyklėms išjungti.</span><span class="sxs-lookup"><span data-stu-id="20b65-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="20b65-107">Norėdami peržiūrėti sąrašo taisykles, prieinamas operacijų vientisumo tikrintuve jūsų aplinkoje, ir norėdami peržiūrėti kiekvienos taisyklės būseną, eikite į **Mažmeninė prekyba ir prekyba\> Būstinės sąranka \> Parametrai \> Prekybos parametrai** ir pasirinkite skirtuką **Operacijų tikrinimas**.</span><span class="sxs-lookup"><span data-stu-id="20b65-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="20b65-108">Pagal numatytuosius nustatymus kiekvienos taisyklės būsena nustatyta kaip **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="20b65-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="20b65-109">Todėl visos taisyklės naudojamos operacijoms patikrinti prieš jas perkeliant į prekybos išrašus.</span><span class="sxs-lookup"><span data-stu-id="20b65-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="20b65-110">Norėdami išjungti taisyklę, pakeiskite jos būseną į **Išjungta**.</span><span class="sxs-lookup"><span data-stu-id="20b65-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="20b65-111">Į išjungtas taisykles neatsižvelgiama tikrinant operacijas išrašų apskaičiavimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="20b65-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="20b65-112">Norėdami apeiti visą tikrinimo procesą nepaisydami įjungtų taisyklių, eikite į **Mažmeninė prekyba ir prekyba\> Būstinės sąranka \> Parametrai \> Prekybos parametrai** ir tada skirtuke **Operacijų tikrinimas** nustatykite parinktį **Išjungti prekybos operacijų vientisumo tikrintuvą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="20b65-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="20b65-113">Nustačius šią parinktį į **Ne**, jos nebus galima nustatyti atgal į **Taip** naudojantis vartotojo sąsaja (UI).</span><span class="sxs-lookup"><span data-stu-id="20b65-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>

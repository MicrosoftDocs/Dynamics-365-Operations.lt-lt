---
title: "Kaip nustatyti RFM analizę"
description: "Šioje temoje aiškinama, kaip nustatyti jūsų klientų „Recency“, dažnumo ir piniginę (RFM) analizę."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: e11ec02d7392601b22e17384a4dbf620b79df035
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017



---

# <a name="set-up-rfm-analysis"></a><span data-ttu-id="fecf0-103">Kaip nustatyti RFM analizę</span><span class="sxs-lookup"><span data-stu-id="fecf0-103">Set up RFM analysis</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="fecf0-104">Šioje temoje aiškinama, kaip nustatyti jūsų klientų „Recency“, dažnumo ir piniginę (RFM) analizę.</span><span class="sxs-lookup"><span data-stu-id="fecf0-104">This topic explains how to set up a Recency, Frequency, and Monetary (RFM) analysis of your customers.</span></span>

<span data-ttu-id="fecf0-105">„Recency“, dažnumo ir piniginę (RFM) analizė yra rinkodaros įrankis, kurį jūsų organizacija gali naudoti generuojamiems klientų pirkimų duomenims įvertinti.</span><span class="sxs-lookup"><span data-stu-id="fecf0-105">Recency, frequency, and monetary (RFM) analysis is a marketing tool that your organization can use to evaluate the data that is generated by customer purchases.</span></span> <span data-ttu-id="fecf0-106">Nustačius RFM analizę, klientams, kai šie perka, priskiriamas apskaičiuotas RFM rezultatas.</span><span class="sxs-lookup"><span data-stu-id="fecf0-106">After you set up RFM analysis, customers are assigned a calculated RFM score as they make purchases.</span></span> <span data-ttu-id="fecf0-107">RFM rezultatas gali būti trijų skaitmenų vertinimas arba sudėtinis numeris – tai priklauso nuo to, kaip jūsų organizacija sukonfigūravo RFM analizę.</span><span class="sxs-lookup"><span data-stu-id="fecf0-107">The RFM score can be a three-digit rating or an aggregate number, depending on how your organization has configured RFM analysis.</span></span> <span data-ttu-id="fecf0-108">Jei jūsų organizacija naudoja rezultatuose naudoja trijų skaitmenų vertinimą, pirmasis skaitmuo yra kliento „recency“ vertinimas (kaip seniai klientas pirko iš jūsų organizacijos).</span><span class="sxs-lookup"><span data-stu-id="fecf0-108">If your organization uses a three-digit rating for the score, the first digit is the customer's recency rating (how recently the customer made a purchase from your organization).</span></span> <span data-ttu-id="fecf0-109">Antrasis skaitmuo yra kliento pirkimų dažnumo vertinimas (kaip dažnai klientas perka iš jūsų organizacijos).</span><span class="sxs-lookup"><span data-stu-id="fecf0-109">The second digit is the customer's frequency rating (how often the customer makes purchases from your organization).</span></span> <span data-ttu-id="fecf0-110">Trečiasis skaitmuo yra kliento piniginės vertės vertinimas (kiek klientas išleidžia, pirkdamas iš jūsų organizacijos).</span><span class="sxs-lookup"><span data-stu-id="fecf0-110">The third digit is the customer's monetary rating (how much the customer spends when he or she makes purchases from your organization).</span></span> <span data-ttu-id="fecf0-111">Pavyzdžiui, jūsų organizacija vertinimus nustato skalėje nuo 1 iki 5, kai 5 yra aukščiausias vertinimas.</span><span class="sxs-lookup"><span data-stu-id="fecf0-111">For example, your organization has set the ratings on a scale of 1 through 5, where 5 is the highest rating.</span></span> <span data-ttu-id="fecf0-112">Šiuo atveju 535 kliento vertinimas nurodo toliau pateiktą informaciją apie klientą.</span><span class="sxs-lookup"><span data-stu-id="fecf0-112">In this case, a customer rating of 535 tells you the following information about the customer:</span></span>

-   <span data-ttu-id="fecf0-113">**„Recency“ vertinimas 5** – klientas pastaruoju metu pirko.</span><span class="sxs-lookup"><span data-stu-id="fecf0-113">**Recency rating of 5** – The customer recently made a purchase.</span></span>
-   <span data-ttu-id="fecf0-114">**Dažnumo vertinimas 3** – klientas gana dažnai perka produktus iš jūsų organizacijos.</span><span class="sxs-lookup"><span data-stu-id="fecf0-114">**Frequency rating of 3** – The customer purchases products from your organization moderately often.</span></span>
-   <span data-ttu-id="fecf0-115">**Piniginės vertės vertinimas 5** – pirkdamas klientas išleidžia didelę pinigų sumą.</span><span class="sxs-lookup"><span data-stu-id="fecf0-115">**Monetary rating of 5** – When the customer makes a purchase, he or she spends a significant amount of money.</span></span>

<span data-ttu-id="fecf0-116">Jei jūsų organizacija naudoja sudėtinį rezultatų numerį, atskiri vertinimai sudedami.</span><span class="sxs-lookup"><span data-stu-id="fecf0-116">If your organization uses an aggregate number for the score, the individual ratings are added together.</span></span> <span data-ttu-id="fecf0-117">Naudojant tą patį pavyzdį kliento vertinimas yra 13 (5 + 3 + 5).</span><span class="sxs-lookup"><span data-stu-id="fecf0-117">For the same example, the customer has a rating of 13 (5 + 3 + 5).</span></span>




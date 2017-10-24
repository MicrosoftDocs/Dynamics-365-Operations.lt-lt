---
title: "Teigiamo mokėjimo apžvalga"
description: "Šiame straipsnyje pateikiama informacija apie teikiamą mokėjimą, kuris naudojamas norint generuoti elektroninį čekių sąrašą, kurį galima teikti bankui."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5b88b940e7a590ff99b6ab8a99ce45d32dfe0505
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="positive-pay-overview"></a><span data-ttu-id="43026-103">Teigiamo mokėjimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="43026-103">Positive pay overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="43026-104">Šiame straipsnyje pateikiama informacija apie teikiamą mokėjimą, kuris naudojamas norint generuoti elektroninį čekių sąrašą, kurį galima teikti bankui.</span><span class="sxs-lookup"><span data-stu-id="43026-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="43026-105">Teigiamas mokėjimas naudojamas norint generuoti elektroninį čekių sąrašą, kurį galima teikti bankui.</span><span class="sxs-lookup"><span data-stu-id="43026-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="43026-106">Naudojant teigiamo mokėjimo failus, bankams lengviau išvengti su čekiais susijusio sukčiavimo.</span><span class="sxs-lookup"><span data-stu-id="43026-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="43026-107">Teigiamas mokėjimas nustatomas, kad būtų generuojamas elektroninis čekių sąrašas, kiekvieną kartą spausdinant čekius.</span><span class="sxs-lookup"><span data-stu-id="43026-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="43026-108">Tada, čekį pateikus bankui, bankas jį lygina su jūsų anksčiau pateiktu čekių sąrašu.</span><span class="sxs-lookup"><span data-stu-id="43026-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="43026-109">Jei čekis atitinka sąraše esantįjį, bankas jį patvirtina.</span><span class="sxs-lookup"><span data-stu-id="43026-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="43026-110">Jei čekis sąraše esančio čekio neatitinka, bankas jį pasilieka peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="43026-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="43026-111">Teigiamas mokėjimas dar vadinamas „SafePay‟.</span><span class="sxs-lookup"><span data-stu-id="43026-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="43026-112">Teigiamo mokėjimo failuose gali būti neskelbtinos informacijos apie mokėjimų gavėjus ir čekių sumas.</span><span class="sxs-lookup"><span data-stu-id="43026-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="43026-113">Todėl būtinai naudokite reikiamas saugos priemones nuo failų sugeneravimo akimirkos iki jų gavimo banke.</span><span class="sxs-lookup"><span data-stu-id="43026-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="43026-114">Teigiamo mokėjimo failai atsisiunčiami pagal žiniatinklio naršyklės atsisiuntimo instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="43026-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="43026-115">Teigiamo mokėjimo failai kuriami naudojant duomenų objektus.</span><span class="sxs-lookup"><span data-stu-id="43026-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="43026-116">Prieš generuodami teigiamo mokėjimo failą, turite nustatyti XML transformavimo formatus, kuriais duomenys paverčiami į formatą, kurį gali naudoti bankas.</span><span class="sxs-lookup"><span data-stu-id="43026-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="43026-117">Kiekvienai banko sąskaitai, kuriai norite generuoti teigiamo mokėjimo informaciją, turite priskirti teigiamo mokėjimo formatą.</span><span class="sxs-lookup"><span data-stu-id="43026-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="43026-118">Sugeneravę mokėjimus galite generuoti teigiamo mokėjimo failą vienam juridiniam subjektui ir vienai banko sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="43026-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="43026-119">Taip pat tuo pačiu metu teigiamo mokėjimo failus galite generuoti keliems juridiniams subjektams ir banko sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="43026-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="43026-120">Po to, kai teigiamo mokėjimo faile nurodyti čekiai apmokami, iš bango gausite patvirtinimo numerį.</span><span class="sxs-lookup"><span data-stu-id="43026-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="43026-121">Tada teigiamo mokėjimo failą galite patvirtinti programoje „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“.</span><span class="sxs-lookup"><span data-stu-id="43026-121">You can then confirm the positive pay file in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> 

<span data-ttu-id="43026-122">Jei turite teigiamo mokėjimo failą pakeisti, galite jį atšaukti.</span><span class="sxs-lookup"><span data-stu-id="43026-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="43026-123">Tada iš naujo nustatomas kiekvieno teigiamo mokėjimo failo čekio laukas, kuriame nurodoma, ar tas čekis įtrauktas į teigiamo mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="43026-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="43026-124">Norėdami gauti daugiau informacijos, žr. [Teigiamų mokėjimų failų nustatymas ir generavimas](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="43026-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>





---
title: Teigiamo mokėjimo apžvalga
description: Šiame straipsnyje pateikiama informacija apie teikiamą mokėjimą, kuris naudojamas norint generuoti elektroninį čekių sąrašą, kurį galima teikti bankui.
author: panolte
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 611cd7c46cf160a3e4e2b43acecaacdb6c79b16d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235914"
---
# <a name="positive-pay-overview"></a><span data-ttu-id="e7935-103">Teigiamo mokėjimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="e7935-103">Positive pay overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7935-104">Šiame straipsnyje pateikiama informacija apie teikiamą mokėjimą, kuris naudojamas norint generuoti elektroninį čekių sąrašą, kurį galima teikti bankui.</span><span class="sxs-lookup"><span data-stu-id="e7935-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="e7935-105">Teigiamas mokėjimas naudojamas norint generuoti elektroninį čekių sąrašą, kurį galima teikti bankui.</span><span class="sxs-lookup"><span data-stu-id="e7935-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="e7935-106">Naudojant teigiamo mokėjimo failus, bankams lengviau išvengti su čekiais susijusio sukčiavimo.</span><span class="sxs-lookup"><span data-stu-id="e7935-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="e7935-107">Teigiamas mokėjimas nustatomas, kad būtų generuojamas elektroninis čekių sąrašas, kiekvieną kartą spausdinant čekius.</span><span class="sxs-lookup"><span data-stu-id="e7935-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="e7935-108">Tada, čekį pateikus bankui, bankas jį lygina su jūsų anksčiau pateiktu čekių sąrašu.</span><span class="sxs-lookup"><span data-stu-id="e7935-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="e7935-109">Jei čekis atitinka sąraše esantįjį, bankas jį patvirtina.</span><span class="sxs-lookup"><span data-stu-id="e7935-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="e7935-110">Jei čekis sąraše esančio čekio neatitinka, bankas jį pasilieka peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="e7935-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="e7935-111">Teigiamas mokėjimas dar vadinamas „SafePay‟.</span><span class="sxs-lookup"><span data-stu-id="e7935-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="e7935-112">Teigiamo mokėjimo failuose gali būti neskelbtinos informacijos apie mokėjimų gavėjus ir čekių sumas.</span><span class="sxs-lookup"><span data-stu-id="e7935-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="e7935-113">Todėl būtinai naudokite reikiamas saugos priemones nuo failų sugeneravimo akimirkos iki jų gavimo banke.</span><span class="sxs-lookup"><span data-stu-id="e7935-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="e7935-114">Teigiamo mokėjimo failai atsisiunčiami pagal žiniatinklio naršyklės atsisiuntimo instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="e7935-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="e7935-115">Teigiamo mokėjimo failai kuriami naudojant duomenų objektus.</span><span class="sxs-lookup"><span data-stu-id="e7935-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="e7935-116">Prieš generuodami teigiamo mokėjimo failą, turite nustatyti XML transformavimo formatus, kuriais duomenys paverčiami į formatą, kurį gali naudoti bankas.</span><span class="sxs-lookup"><span data-stu-id="e7935-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="e7935-117">Kiekvienai banko sąskaitai, kuriai norite generuoti teigiamo mokėjimo informaciją, turite priskirti teigiamo mokėjimo formatą.</span><span class="sxs-lookup"><span data-stu-id="e7935-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="e7935-118">Sugeneravę mokėjimus galite generuoti teigiamo mokėjimo failą vienam juridiniam subjektui ir vienai banko sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="e7935-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="e7935-119">Taip pat tuo pačiu metu teigiamo mokėjimo failus galite generuoti keliems juridiniams subjektams ir banko sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="e7935-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="e7935-120">Po to, kai teigiamo mokėjimo faile nurodyti čekiai apmokami, iš bango gausite patvirtinimo numerį.</span><span class="sxs-lookup"><span data-stu-id="e7935-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="e7935-121">Tada teigiamo mokėjimo failą galite patvirtinti sistemoje.</span><span class="sxs-lookup"><span data-stu-id="e7935-121">You can then confirm the positive pay file in the system.</span></span> 

<span data-ttu-id="e7935-122">Jei turite teigiamo mokėjimo failą pakeisti, galite jį atšaukti.</span><span class="sxs-lookup"><span data-stu-id="e7935-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="e7935-123">Tada iš naujo nustatomas kiekvieno teigiamo mokėjimo failo čekio laukas, kuriame nurodoma, ar tas čekis įtrauktas į teigiamo mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="e7935-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="e7935-124">Norėdami gauti daugiau informacijos, žr. [Teigiamų mokėjimų failų nustatymas ir generavimas](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="e7935-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: "Sparčiojo importavimo / eksportavimo funkcijos naudojimas"
description: "Sparčiojo importavimo / eksportavimo funkcijos paskirtis yra suteikti galimybę importuoti ir eksportuoti atliekant mažiau veiksmų."
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: AX 2012 R3 CU8, UnifiedOperations
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5c54d0590856755e208ada9d97af7790a6de95ec
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="run-the-test-data-transfer-tool-beta-for-dynamics-ax-ax-2012"></a><span data-ttu-id="ca46d-103">Paleiskite duomenų tikrinimo perkėlimo įrankį (beta versija), skirtą „Dynamics AX“ (AX 2012)</span><span class="sxs-lookup"><span data-stu-id="ca46d-103">Run the Test Data Transfer Tool (beta) for Dynamics AX (AX 2012)</span></span>

[!include[banner](../../includes/banner.md)]


<span data-ttu-id="ca46d-104">Sparčiojo importavimo / eksportavimo funkcijos paskirtis yra suteikti galimybę importuoti ir eksportuoti atliekant mažiau veiksmų.</span><span class="sxs-lookup"><span data-stu-id="ca46d-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="ca46d-105">Mes įtraukėme sparčiojo importavimo eksportavimo funkciją, kad vartotojai galėtų importuoti arba eksportuoti paprastas užduotis, kuriais jie nori vykdyti sparčiai.</span><span class="sxs-lookup"><span data-stu-id="ca46d-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="ca46d-106">Idealiu atveju ši funkcija naudojama scenarijuose, kuriuose failas automatiškai susiejamas su sistema ir vartotojui nereikia vykdyti išplėstinio susiejimo proceso arba kurti pakartotines importavimo ar eksportavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="ca46d-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

-   <span data-ttu-id="ca46d-107">Šią funkciją galima naudoti tiek su parengtais naudoti, tiek su pasirinktiniais objektais.</span><span class="sxs-lookup"><span data-stu-id="ca46d-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
-   <span data-ttu-id="ca46d-108">Galite importuoti failus ir, jei naudojate ODBC duomenų šaltinį, galite pasirinkti užklausą importui nurodyti.</span><span class="sxs-lookup"><span data-stu-id="ca46d-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
-   <span data-ttu-id="ca46d-109">Turite būti anksčiau nustatę AX arba failo šaltinio duomenų formatus ir žinoti, kur jie yra.</span><span class="sxs-lookup"><span data-stu-id="ca46d-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
-   <span data-ttu-id="ca46d-110">Jums nereikia kurti apdorojimo grupės, kad galėtumėte naudoti sparčiojo importavimo / eksportavimo funkciją, sistema ją sukurs automatiškai, kai bus vykdoma importavimo arba eksportavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="ca46d-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="ca46d-111">Taip pat galite pasirinkti saugoti duomenų, importuotų naudojant sparčiojo importavimo / eksportavimo funkciją, retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="ca46d-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="ca46d-112">Atkreipkite dėmesį, kad sparčiojo importavimo / eksportavimo funkcija daro prielaidą, kad jūs esate susipažinę su DIXF sąvokomis.</span><span class="sxs-lookup"><span data-stu-id="ca46d-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>





---
title: Sukurti įrašo šabloną, kad būtų paprasčiau įvesti duomenis
description: Šioje temoje rodoma, kaip sukurti įrašo šabloną, kad dažnai naudojamų lauko reikšmių nereikėtų atskirai įvesti kiekviename naujame įraše.
author: margoc
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6a2eec8d730cb4c63c854433cf6160c475ce660
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753969"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="4a562-103">Sukurti įrašo šabloną, kad būtų paprasčiau įvesti duomenis</span><span class="sxs-lookup"><span data-stu-id="4a562-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a562-104">Šioje temoje rodoma, kaip sukurti įrašo šabloną, kad dažnai naudojamų lauko reikšmių nereikėtų atskirai įvesti kiekviename naujame įraše.</span><span class="sxs-lookup"><span data-stu-id="4a562-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="4a562-105">Atlikdami šią procedūrą sukursite naują įrašą apie naujus nešiojamuosius kompiuterius, kurie turėtų būti įtraukti į jūsų ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="4a562-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="4a562-106">Šioje procedūroje naudojama pavyzdinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="4a562-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="4a562-107">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="4a562-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="4a562-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4a562-108">Select **New**.</span></span>
3. <span data-ttu-id="4a562-109">Lauke **Ilgalaikio turto grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4a562-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="4a562-110">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4a562-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="4a562-111">Pavyzdžiui, įveskite **Įmonės pagrindinis nešiojamasis kompiuteris**.</span><span class="sxs-lookup"><span data-stu-id="4a562-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="4a562-112">Lauke **Ieškoti pavadinimo** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4a562-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="4a562-113">Pavyzdžiui, įveskite **nešiojamasis kompiuteris**.</span><span class="sxs-lookup"><span data-stu-id="4a562-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="4a562-114">Išplėskite skyrių **Techninė informacija**.</span><span class="sxs-lookup"><span data-stu-id="4a562-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="4a562-115">Laukuose **Gamintojas**, **Modelis** ir **Modelio metai** įveskite reikšmes.</span><span class="sxs-lookup"><span data-stu-id="4a562-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="4a562-116">Veiksmų srityje pasirinkite **Parinktys**.</span><span class="sxs-lookup"><span data-stu-id="4a562-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="4a562-117">Pažymėkite **Įrašo informacija**.</span><span class="sxs-lookup"><span data-stu-id="4a562-117">Select **Record info**.</span></span>
10. <span data-ttu-id="4a562-118">Pažymėkite **Vartotojo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="4a562-118">Select **User template**.</span></span>
11. <span data-ttu-id="4a562-119">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4a562-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="4a562-120">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4a562-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="4a562-121">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4a562-121">Select **OK**.</span></span>
14. <span data-ttu-id="4a562-122">Pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="4a562-122">Select **Close**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
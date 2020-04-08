---
title: Sukurti įrašo šabloną, kad būtų paprasčiau įvesti duomenis
description: Šioje temoje rodoma, kaip sukurti įrašo šabloną, kad dažnai naudojamų lauko reikšmių nereikėtų atskirai įvesti kiekviename naujame įraše.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec21415158ad611d0ad55778e76aa128f53561bd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143389"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="f5b1e-103">Sukurti įrašo šabloną, kad būtų paprasčiau įvesti duomenis</span><span class="sxs-lookup"><span data-stu-id="f5b1e-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5b1e-104">Šioje temoje rodoma, kaip sukurti įrašo šabloną, kad dažnai naudojamų lauko reikšmių nereikėtų atskirai įvesti kiekviename naujame įraše.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="f5b1e-105">Atlikdami šią procedūrą sukursite naują įrašą apie naujus nešiojamuosius kompiuterius, kurie turėtų būti įtraukti į jūsų ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="f5b1e-106">Šioje procedūroje naudojama pavyzdinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="f5b1e-107">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="f5b1e-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-108">Select **New**.</span></span>
3. <span data-ttu-id="f5b1e-109">Lauke **Ilgalaikio turto grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="f5b1e-110">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="f5b1e-111">Pavyzdžiui, įveskite **Įmonės pagrindinis nešiojamasis kompiuteris**.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="f5b1e-112">Lauke **Ieškoti pavadinimo** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="f5b1e-113">Pavyzdžiui, įveskite **nešiojamasis kompiuteris**.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="f5b1e-114">Išplėskite skyrių **Techninė informacija**.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="f5b1e-115">Laukuose **Gamintojas**, **Modelis** ir **Modelio metai** įveskite reikšmes.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="f5b1e-116">Veiksmų srityje pasirinkite**Parinktys**.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="f5b1e-117">Pažymėkite **Įrašo informacija**.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-117">Select **Record info**.</span></span>
10. <span data-ttu-id="f5b1e-118">Pažymėkite **Vartotojo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-118">Select **User template**.</span></span>
11. <span data-ttu-id="f5b1e-119">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="f5b1e-120">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="f5b1e-121">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-121">Select **OK**.</span></span>
14. <span data-ttu-id="f5b1e-122">Pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="f5b1e-122">Select **Close**.</span></span>


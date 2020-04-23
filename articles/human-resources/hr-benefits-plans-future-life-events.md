---
title: Būsimų gyvenimo įvykių konfigūravimas
description: Galite planuoti būsimus gyvenimo įvykius programoje „Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 134152bb8ae2b9f42b59cc9202e244435a607eba
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230090"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="6e697-103">Būsimų gyvenimo įvykių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="6e697-103">Configure future life events</span></span>

<span data-ttu-id="6e697-104">Galite planuoti būsimus gyvenimo įvykius programoje „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="6e697-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="6e697-105">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Būsimi gyvenimo įvykiai**.</span><span class="sxs-lookup"><span data-stu-id="6e697-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="6e697-106">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6e697-106">Select **New**.</span></span>

3. <span data-ttu-id="6e697-107">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="6e697-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="6e697-108">Laukas</span><span class="sxs-lookup"><span data-stu-id="6e697-108">Field</span></span> | <span data-ttu-id="6e697-109">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="6e697-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="6e697-110">Gyvenimo įvykio data</span><span class="sxs-lookup"><span data-stu-id="6e697-110">Life event date</span></span> | <span data-ttu-id="6e697-111">Sistema apdoroja visus įvykius registravimo laikotarpiu, kurie įvyksta iki šios datos.</span><span class="sxs-lookup"><span data-stu-id="6e697-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="6e697-112">Gyvenimo įvykis užregistruotas</span><span class="sxs-lookup"><span data-stu-id="6e697-112">Life event logged</span></span> | <span data-ttu-id="6e697-113">Data ir laikas, kai gyvenimo įvykis yra užregistruotas.</span><span class="sxs-lookup"><span data-stu-id="6e697-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="6e697-114">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="6e697-114">Log type</span></span> | <span data-ttu-id="6e697-115">Nurodo, ar veiksmas yra vienas iš šių veiksmų:</span><span class="sxs-lookup"><span data-stu-id="6e697-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="6e697-116">- **Naujinti** – esamo įrašo, sekančio gyvenimo įvykius, keitimas</span><span class="sxs-lookup"><span data-stu-id="6e697-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="6e697-117">- **Įterpti** – naujo gyvenimo įvykio įrašo kūrimas</span><span class="sxs-lookup"><span data-stu-id="6e697-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="6e697-118">Gyvenimo įvykio tipo ID</span><span class="sxs-lookup"><span data-stu-id="6e697-118">Life event type ID</span></span> | <span data-ttu-id="6e697-119">Unikalus gyvenimo įvykio tipo identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="6e697-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="6e697-120">Gyvenimo įvykio tipas</span><span class="sxs-lookup"><span data-stu-id="6e697-120">Life event type</span></span> | <span data-ttu-id="6e697-121">Katalizatorius, skirtas atnaujinti darbuotojo išmokų registravimą.</span><span class="sxs-lookup"><span data-stu-id="6e697-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="6e697-122">Norėdami gauti daugiau informacijos, žr. skyriuje Gyvenimo įvykių paleidikliai.</span><span class="sxs-lookup"><span data-stu-id="6e697-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="6e697-123">Būsena</span><span class="sxs-lookup"><span data-stu-id="6e697-123">Status</span></span> | <span data-ttu-id="6e697-124">Ar gyvenimo įvykis apdorotas ar neapdorotas.</span><span class="sxs-lookup"><span data-stu-id="6e697-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="6e697-125">Eilutė</span><span class="sxs-lookup"><span data-stu-id="6e697-125">Line</span></span> | <span data-ttu-id="6e697-126">Būsimo gyvenimo įvykio eilutės numeris.</span><span class="sxs-lookup"><span data-stu-id="6e697-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="6e697-127">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6e697-127">Select **Save**.</span></span> 

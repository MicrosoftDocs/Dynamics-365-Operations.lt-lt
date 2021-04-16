---
title: Išjungti gamybos eigos versiją
description: Kai aktyvi gamybos eigos versija nebereikalinga, galite jį išjungti.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e47cb950ce488d8b6170f829e1fedc664b921a1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811563"
---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="22240-103">Išjungti gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="22240-103">Deactivate a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="22240-104">Kai aktyvi gamybos eigos versija nebereikalinga, galite jį išjungti.</span><span class="sxs-lookup"><span data-stu-id="22240-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="22240-105">Turėtumėte šią parinktį naudoti tik jei visos „kanban“ taisyklės ir veiklos yra baigtos ir nebus vėl suaktyvintos.</span><span class="sxs-lookup"><span data-stu-id="22240-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="22240-106">Atkreipkite dėmesį, kad visų su šia gamybos versija susijusių „kanban“ taisyklių galiojimo data bus atnaujinta į dabartinę datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="22240-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="22240-107">Norėdami keisti aktyvią gamybos eigos versiją, galite nustatyti aktyvios versijos galiojimo datą ir sukurti naują versiją.</span><span class="sxs-lookup"><span data-stu-id="22240-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="22240-108">Tokiu būdu galėsite tęsti gamybos operacijas, tuo pat metu ruošdami naują versiją ir susijusias „kanban“ taisykles.</span><span class="sxs-lookup"><span data-stu-id="22240-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="22240-109">Norėdami, kad baigtų galioti aktyvi gamybos eigos versija, turite nustatyti galiojimo datą.</span><span class="sxs-lookup"><span data-stu-id="22240-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="22240-110">Šia prasme išjungimas yra daugiau išimtis negu taisyklė.</span><span class="sxs-lookup"><span data-stu-id="22240-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="22240-111">Šiai procedūrai atlikti reikalinga gamybos eiga, kurios versiją galima išjungti.</span><span class="sxs-lookup"><span data-stu-id="22240-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="22240-112">Nebandykite to atlikti gamybos aplinkoje, nebent esate 100 % tikri, kad versija yra visiškai pasenusi.</span><span class="sxs-lookup"><span data-stu-id="22240-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="22240-113">Išjungti gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="22240-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="22240-114">Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.</span><span class="sxs-lookup"><span data-stu-id="22240-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="22240-115">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="22240-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="22240-116">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="22240-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="22240-117">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="22240-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="22240-118">Spustelėkite Išjungti.</span><span class="sxs-lookup"><span data-stu-id="22240-118">Click Deactivate.</span></span>
    * <span data-ttu-id="22240-119">Tęskite tik jei esate 100 % tikri, kad ši gamybos eigos versija yra pasenusi.</span><span class="sxs-lookup"><span data-stu-id="22240-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="22240-120">Spustelėjus Gerai nustos galioti visos aktyvios „kanban“ taisyklės ir nedelsiant bus sustabdytos visos šios gamybos eigos versijos gamybos ir papildymo veiklos.</span><span class="sxs-lookup"><span data-stu-id="22240-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="22240-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="22240-121">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
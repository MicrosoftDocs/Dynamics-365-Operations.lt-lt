---
title: Procesų automatizavimas
description: Šioje temoje pateikiama informacija apie tai, kaip procesų automatizavimas leidžia paprastai suplanuoti procesus, kuriuos vykdys paketų serveris.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508190"
---
# <a name="process-automation"></a><span data-ttu-id="4dbcc-103">Procesų automatizavimas</span><span class="sxs-lookup"><span data-stu-id="4dbcc-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4dbcc-104">Procesų automatizavimas leidžia paprastai suplanuoti procesus, kuriuos vykdys paketų serveris.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="4dbcc-105">Atnaujinto suplanuotų užduočių kalendoriaus rodinys leidžia galutiniams vartotojams peržiūrėti ir atlikti veiksmus su suplanuotomis ir pabaigtomis užduotimis.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="4dbcc-106">Administravimas</span><span class="sxs-lookup"><span data-stu-id="4dbcc-106">Administration</span></span>

<span data-ttu-id="4dbcc-107">Visų procesų automatizavimų centrinis administravimo puslapis yra sistemos administravimo modulyje **Nustatymas** meniu.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="4dbcc-108">Šiame puslapyje bus išvardyti visi sistemoje nustatyti automatizuoti procesai (serija).</span><span class="sxs-lookup"><span data-stu-id="4dbcc-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="4dbcc-109">Be to, leidžiama pridėti naujų procesų automatizavimus tiesiogiai iš šio puslapio.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="4dbcc-110">Nustačius seriją, galite valdyti kiekvieną šio sąrašo seriją.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="4dbcc-111">Galite pasirinkti redaguoti visą seriją, panaikinti ją, peržiūrėti visus įvykius sąrašo rodinyje arba išjungti seriją, jei norite, kad suplanuotos užduotys būtų pristabdytos tam tikram laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-111">You can chose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a period of time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="4dbcc-112">Kalendoriaus rodinys</span><span class="sxs-lookup"><span data-stu-id="4dbcc-112">Calendar view</span></span> 
<span data-ttu-id="4dbcc-113">Vienas iš pagrindinių procesų automatizavimo privalumų yra galimybė peržiūrėti suplanuotas užduotis paprastajame kalendoriaus rodinyje.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-113">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="4dbcc-114">Šis rodinys leidžia peržiūrėti visos savaitės užduotis vienu metu.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-114">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="4dbcc-115">Šį rodinį pamatysite dešinėje puslapio **Procesų automatizavimas** pusėje.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-115">You will see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="4dbcc-116">Jis bus automatiškai užpildytas pasirinktų serijų suplanuotomis užduotimis.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-116">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="4dbcc-117">[![Apdoroti automatizavimo kalendorių](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="4dbcc-117">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="4dbcc-118">Įvykių pakeitimai</span><span class="sxs-lookup"><span data-stu-id="4dbcc-118">Occurrence changes</span></span>
<span data-ttu-id="4dbcc-119">Kiekvieną įvykį galima modifikuoti nedarant įtakos kitiems įvykiams, nustatytiems juos sukūrusios serijos.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-119">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="4dbcc-120">Suplanuotas užduotis galima redaguoti kalendoriaus rodinyje pasirenkant mygtuką **Peržiūrėti/redaguoti** ir **Įvykis**.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-120">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="4dbcc-121">Tai suteikia prieigą prie visų parametrų, rodomų serijos nustatymo vedlyje ir galimybę atlikti vienkartinius pasirinkto įvykio pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-121">This allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="4dbcc-122">Suplanuota užduotis gali būti išjungta pasirenkant mygtuką **Išjungti** kalendoriaus rodinyje.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-122">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span> 

## <a name="developer-documentation"></a><span data-ttu-id="4dbcc-123">Kūrėjo dokumentacija</span><span class="sxs-lookup"><span data-stu-id="4dbcc-123">Developer documentation</span></span> 
<span data-ttu-id="4dbcc-124">Šiuo metu kuriama kūrėjo dokumentacija, leisianti kūrėjams išplėsti procesų automatizavimo sistemą.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-124">Developer documentation is currently being written to allow developers to extend the process automation framework.</span></span> <span data-ttu-id="4dbcc-125">Šioje dokumentacijoje bus pateikta informacija apie tai, kaip galite sukurti pasirinktinius procesus, kurie yra vykdomi paketų serveryje, numatyti procesų automatizavimo vedlyje ir automatiškai atsirandantys kalendoriaus rodinyje.</span><span class="sxs-lookup"><span data-stu-id="4dbcc-125">This documentation will provide information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>

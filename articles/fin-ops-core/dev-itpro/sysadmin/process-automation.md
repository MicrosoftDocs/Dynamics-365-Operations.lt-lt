---
title: Procesų automatizavimas
description: Šioje temoje pateikiama informacija apie tai, kaip procesų automatizavimas leidžia paprastai suplanuoti procesus, kuriuos vykdys paketų serveris.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
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
ms.openlocfilehash: afbef26cb7b37bafb34f12cc20a88fb4aea9f343
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885256"
---
# <a name="process-automation"></a><span data-ttu-id="3512b-103">Procesų automatizavimas</span><span class="sxs-lookup"><span data-stu-id="3512b-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3512b-104">Procesų automatizavimas leidžia paprastai suplanuoti procesus, kuriuos vykdys paketų serveris.</span><span class="sxs-lookup"><span data-stu-id="3512b-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="3512b-105">Atnaujinto suplanuotų užduočių kalendoriaus rodinys leidžia galutiniams vartotojams peržiūrėti ir atlikti veiksmus su suplanuotomis ir pabaigtomis užduotimis.</span><span class="sxs-lookup"><span data-stu-id="3512b-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="3512b-106">Administravimas</span><span class="sxs-lookup"><span data-stu-id="3512b-106">Administration</span></span>

<span data-ttu-id="3512b-107">Visų procesų automatizavimų centrinis administravimo puslapis yra sistemos administravimo modulyje **Nustatymas** meniu.</span><span class="sxs-lookup"><span data-stu-id="3512b-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="3512b-108">Šiame puslapyje bus išvardyti visi sistemoje nustatyti automatizuoti procesai (serija).</span><span class="sxs-lookup"><span data-stu-id="3512b-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="3512b-109">Be to, leidžiama pridėti naujų procesų automatizavimus tiesiogiai iš šio puslapio.</span><span class="sxs-lookup"><span data-stu-id="3512b-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="3512b-110">Nustačius seriją, galite valdyti kiekvieną šio sąrašo seriją.</span><span class="sxs-lookup"><span data-stu-id="3512b-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="3512b-111">Galite pasirinkti redaguoti visą seriją, panaikinti ją, peržiūrėti visus įvykius sąrašo rodinyje arba išjungti seriją, jei norite, kad suplanuotos užduotys būtų pristabdytos kuriam laikui.</span><span class="sxs-lookup"><span data-stu-id="3512b-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="3512b-112">Visi funkcijų valdyme neįjungti procesai nebus rodomi funkcijai esant išjungtai.</span><span class="sxs-lookup"><span data-stu-id="3512b-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="3512b-113">Taip pat, procesų automatizavimo grafiko variklis nenustatys jokių įvykių ar fone vykstančių procesų išjungtai funkcijai.</span><span class="sxs-lookup"><span data-stu-id="3512b-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="3512b-114">Funkcijos įjungimas įjungs visus suplanuotus įvykius ir anksčiau pradėtus fone vykstančius procesus neatidėliotinam vykdymui.</span><span class="sxs-lookup"><span data-stu-id="3512b-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="3512b-115">Kalendoriaus rodinys</span><span class="sxs-lookup"><span data-stu-id="3512b-115">Calendar view</span></span>

<span data-ttu-id="3512b-116">Vienas iš pagrindinių procesų automatizavimo privalumų yra galimybė peržiūrėti suplanuotas užduotis paprastajame kalendoriaus rodinyje.</span><span class="sxs-lookup"><span data-stu-id="3512b-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="3512b-117">Šis rodinys leidžia peržiūrėti visos savaitės užduotis vienu metu.</span><span class="sxs-lookup"><span data-stu-id="3512b-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="3512b-118">Šį rodinį pamatysite dešinėje puslapio **Procesų automatizavimas** pusėje.</span><span class="sxs-lookup"><span data-stu-id="3512b-118">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="3512b-119">Jis bus automatiškai užpildytas pasirinktų serijų suplanuotomis užduotimis.</span><span class="sxs-lookup"><span data-stu-id="3512b-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="3512b-120">[![Apdoroti automatizavimo kalendorių](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="3512b-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="3512b-121">Įvykių pakeitimai</span><span class="sxs-lookup"><span data-stu-id="3512b-121">Occurrence changes</span></span>

<span data-ttu-id="3512b-122">Kiekvieną įvykį galima modifikuoti nedarant įtakos kitiems įvykiams, nustatytiems juos sukūrusios serijos.</span><span class="sxs-lookup"><span data-stu-id="3512b-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="3512b-123">Suplanuotas užduotis galima redaguoti kalendoriaus rodinyje pasirenkant mygtuką **Peržiūrėti/redaguoti** ir **Įvykis**.</span><span class="sxs-lookup"><span data-stu-id="3512b-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="3512b-124">Šis puslapis suteikia prieigą prie visų parametrų, rodomų serijos nustatymo vedlyje ir galimybę atlikti vienkartinius pasirinkto įvykio pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="3512b-124">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="3512b-125">Suplanuota užduotis gali būti išjungta pasirenkant mygtuką **Išjungti** kalendoriaus rodinyje.</span><span class="sxs-lookup"><span data-stu-id="3512b-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="3512b-126">Kūrėjo dokumentacija</span><span class="sxs-lookup"><span data-stu-id="3512b-126">Developer documentation</span></span>

<span data-ttu-id="3512b-127">Procesų automatizavimo sistema leidžia programuotojams išplėsti proceso automatizavimo sistemą.</span><span class="sxs-lookup"><span data-stu-id="3512b-127">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="3512b-128">[Procesų automatizavimo sistema](../process-automation/process-automation-framework.md) dokumentacijoje pateikta informacija apie tai, kaip galite sukurti pasirinktinius procesus, kurie yra vykdomi paketų serveryje, numatyti procesų automatizavimo vedlyje ir automatiškai atsirandantys kalendoriaus rodinyje.</span><span class="sxs-lookup"><span data-stu-id="3512b-128">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>

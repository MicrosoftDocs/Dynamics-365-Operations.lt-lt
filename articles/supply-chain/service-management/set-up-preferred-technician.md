---
title: Pageidaujamo techniko nustatymas
description: Galite pasirinkti bet kurį darbuotoją, kaip pageidaujamą techniką aptarnavimo sutarčiai ar aptarnavimo užsakymui.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43327b5c9077ab6cbde23fe069cccfc74a0edf88
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815024"
---
# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="3929a-103">Pageidaujamo techniko nustatymas</span><span class="sxs-lookup"><span data-stu-id="3929a-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3929a-104">Galite pasirinkti bet kurį darbuotoją, kaip pageidaujamą techniką aptarnavimo sutarčiai ar aptarnavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="3929a-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="3929a-105">Tačiau gera mintis įtraukti darbuotoją į atitinkamą išsiuntimo komandą, kad darbuotojas būtų įtrauktas į sritį **Išsiuntimo informacijos lenta**.</span><span class="sxs-lookup"><span data-stu-id="3929a-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="3929a-106">Darbuotojo priskyrimas išsiuntimo komandai</span><span class="sxs-lookup"><span data-stu-id="3929a-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="3929a-107">Spustelėkite **Personalas** \> **Bendra** \> **Darbuotojai** \> **Darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="3929a-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="3929a-108">Dukart spustelėkite darbuotoją norėdami atidaryti darbuotojo informacijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="3929a-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="3929a-109">Srityje **Veiksmų sritis** spustelėję **Sąranka** \>**Išsiuntimo komanda** atidarykite formą **Išsiuntimo darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="3929a-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="3929a-110">Lauke **Išsiuntimo komanda** pasirinkite komandą, kuriai norite priskirti darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="3929a-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="3929a-111">Pageidaujamo techniko priskyrimas aptarnavimo sutarčiai</span><span class="sxs-lookup"><span data-stu-id="3929a-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="3929a-112">Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="3929a-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="3929a-113">Dukart spustelėkite aptarnavimo sutartį norėdami atidaryti išsamios informacijos formą.</span><span class="sxs-lookup"><span data-stu-id="3929a-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="3929a-114">Skirtuke **Bendra** pasirinkite lauką **Pageidaujamas technikas**, po to pasirinkite atitinkamos išsiuntimo komandos narį, kaip pageidaujamą aptarnavimo sutarties techniką.</span><span class="sxs-lookup"><span data-stu-id="3929a-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="3929a-115">Pageidaujamo techniko priskyrimas aptarnavimo užsakymui</span><span class="sxs-lookup"><span data-stu-id="3929a-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="3929a-116">Spustelėkite **Aptarnavimo valdymas** \> **Periodinis** \> **Išsiuntimo informacijos lenta**.</span><span class="sxs-lookup"><span data-stu-id="3929a-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="3929a-117">Formoje <STRONG>Išsiuntimo informacijos lenta</STRONG> nurodykite išsiuntimo veiklos, kurią norite peržiūrėti, datos intervalą.</span><span class="sxs-lookup"><span data-stu-id="3929a-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="3929a-118">Taip pat nurodykite, ar rodyti uždarytą veiklą ir ar riboti išsiuntimo veiklos sąrašą komandoms, kurioms jūs priklausote arba esate įgalioti stebėti.</span><span class="sxs-lookup"><span data-stu-id="3929a-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="3929a-119">Spustelėję <STRONG>Gerai</STRONG> atidarykite <STRONG>Išsiuntimo informacijos lenta</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3929a-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="3929a-120">Pasirinkite norimą modifikuoti aptarnavimo veiklos eilutę.</span><span class="sxs-lookup"><span data-stu-id="3929a-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="3929a-121">Skirtuke **Susiję** naudodami sąrašą **Darbuotojas** tam tikros išsiuntimo komandos narį priskirkite pageidaujamu techninės pagalbos techniku.</span><span class="sxs-lookup"><span data-stu-id="3929a-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="3929a-122">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="3929a-122">See also</span></span>

[<span data-ttu-id="3929a-123">Sutarčių sudarymo ir pasirašymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="3929a-123">Develop and establish service agreements overview</span></span>](service-agreements.md)

[<span data-ttu-id="3929a-124">Aptarnavimo užsakymų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="3929a-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="3929a-125">[Aptarnavimo sutartys (forma)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="3929a-125">[Service agreements (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span></span>
  



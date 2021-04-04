---
title: Aptarnavimo užsakymų kūrimas rankiniu būdu
description: Galite aptarnavimo užsakymus kurti rankiniu būdu naudodami aptarnavimo sutartį arba naudodami formą **Aptarnavimo užsakymai**.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72b600bc59119a6304fa043240a34051435f8691
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470958"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="ec86a-103">Aptarnavimo užsakymų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="ec86a-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ec86a-104">Galite aptarnavimo užsakymus kurti rankiniu būdu naudodami aptarnavimo sutartį arba naudodami formą **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="ec86a-105">Taip pat galite kurti aptarnavimo užsakymą iš projekto.</span><span class="sxs-lookup"><span data-stu-id="ec86a-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="ec86a-106">Aptarnavimo užsakymams kurti galite naudoti automatizuotus procesus.</span><span class="sxs-lookup"><span data-stu-id="ec86a-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="ec86a-107">Rankinis aptarnavimo užsakymo kūrimas iš aptarnavimo sutarties</span><span class="sxs-lookup"><span data-stu-id="ec86a-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="ec86a-108">Pasirinkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-108">Select **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="ec86a-109">Pasirinkite aptarnavimo sutartį arba sukurkite naują aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="ec86a-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="ec86a-110">Pasirinkite skirtuką **Pristatyti** ir grupėje **Kurti** pasirinkite **Suplanuoti aptarnavimo užsakymai** norėdami atidaryti formą **Kurti aptarnavimo užsakymus**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-110">Select the **Deliver** tab and in the **Create** group select **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="ec86a-111">Neautomatinis aptarnavimo užsakymo kūrimas formoje Aptarnavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="ec86a-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="ec86a-112">Pasirinkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-112">Select **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="ec86a-113">Pasirinkite **Nauja**, kad sukurtumėte naują paslaugų užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ec86a-113">Select **New** to create a new service order.</span></span>

3.  <span data-ttu-id="ec86a-114">Sukurkite aptarnavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="ec86a-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="ec86a-115">Jei žymės langelis <STRONG>Leisti be aptarnavimo sutarties</STRONG> pažymėtas formoje <STRONG>Aptarnavimo valdymo parametrai</STRONG>, galite registruoti aptarnavimo užsakymo eilučių operacijas, nepridėdami aptarnavimo užsakymo prie aptarnavimo sutarties.</span><span class="sxs-lookup"><span data-stu-id="ec86a-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="ec86a-116">Jei žymės langelis išvalytas, prieš registruodami aptarnavimo užsakymo eilutes prie projekto turite pridėti rankiniu būdu sukurtą aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ec86a-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="ec86a-117">Aptarnavimo užsakymo kūrimas iš projekto</span><span class="sxs-lookup"><span data-stu-id="ec86a-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="ec86a-118">Eikite į **Projektų valdymas ir apskaita** \> **Bendra** \> **Projektai** \> **Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-118">Go to **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="ec86a-119">Formoje **Projektai**, esančioje **Veiksmų sritis**, pasirinkite skirtuką **Valdyti** \> pasirinkite **Aptarnavimas** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-119">In the **Projects** form, on the **Action Pane**, select the **Manage** tab \> select **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="ec86a-120">Vadovaukitės ankstesne aptarnavimo užsakymo kūrimo rankiniu būdu procedūra formoje **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="ec86a-121">Lauke **Projekto ID** rodoma projekto nuoroda.</span><span class="sxs-lookup"><span data-stu-id="ec86a-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="ec86a-122">Jei žymės langelis <STRONG>Leisti be aptarnavimo sutarties</STRONG> pažymėtas formoje <STRONG>Aptarnavimo valdymo parametrai</STRONG>, galite registruoti aptarnavimo užsakymo eilučių operacijas, nepridėdami aptarnavimo užsakymo prie aptarnavimo sutarties.</span><span class="sxs-lookup"><span data-stu-id="ec86a-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="ec86a-123">Jei žymės langelis išvalytas, prieš registruodami aptarnavimo užsakymo eilutes prie projekto turite pridėti rankiniu būdu sukurtą aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ec86a-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="ec86a-124">Aptarnavimo užsakymų kūrimas iš pardavimo užsakymo formos</span><span class="sxs-lookup"><span data-stu-id="ec86a-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="ec86a-125">Aptarnavimo užsakymą galima sukurti formoje **Pardavimo užsakymai** naudodami vedlį **Kurti naują aptarnavimo užsakymą pagal pardavimo užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="ec86a-126">Eikite į **Pardavimas ir rinkodara** \> **Bendra** \> **Pardavimo užsakymai** \> **Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-126">Go to **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="ec86a-127">Atidarykite reikalingą pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ec86a-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="ec86a-128">Skirtuke **Pardavimo užsakymas** pasirinkę **Aptarnavimo užsakymas** paleiskite vedlį **Kurti naują aptarnavimo užsakymą, pagrįstą pardavimo užsakymu**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-128">On the **Sales order** tab, select **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="ec86a-129">Pasirinkite **Tolesnis \>**, tuomet atlikite toliau nurodytus veiksmus puslapyje **Pasirinkite aptarnavimo užsakymo sutartį**:</span><span class="sxs-lookup"><span data-stu-id="ec86a-129">Select **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="ec86a-130">Naudokite lauką **Aptarnavimo sutartis** aptarnavimo sutarčiai, su kuria naujasis aptarnavimo užsakymas turi būti susietas, pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="ec86a-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="ec86a-131">(Pasirinktinai:) naudokite lauką **Projekto ID**, kad šį aptarnavimo užsakymą susietumėte su tam tikru projektu.</span><span class="sxs-lookup"><span data-stu-id="ec86a-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="ec86a-132">Pasirinkite **Tolesnis \>**, tuomet atlikite toliau nurodytus veiksmus puslapyje **Kurti aptarnavimo užsakymą**:</span><span class="sxs-lookup"><span data-stu-id="ec86a-132">Select **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="ec86a-133">Įveskite datą ir laiką, kad aptarnavimo skambutis prasidėtų lauke **Pageidaujamas aptarnavimo laikas**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="ec86a-134">Pasirinktinai: jei reikia, tekstą galite modifikuoti lauke **Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="ec86a-135">Pagal numatytuosius nustatymus, šiame lauke pateikiamas aptarnavimo sutarties aprašas, kurį pasirinkote ankstesniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="ec86a-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="ec86a-136">Lauke **Atsakingas** pasirinkite darbuotojo, kuris atsakingas už sutartį, ID ir jei žinote, kas tai yra, įveskite kliento pageidaujamo aptarnavimui atlikti techniko ID.</span><span class="sxs-lookup"><span data-stu-id="ec86a-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="ec86a-137">Lauke **Kontakto ID** pasirinkite kliento įmonės asmenį, su kuriuo bus susisiekta dėl aptarnavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="ec86a-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="ec86a-138">Pasirinkite **Tolesnis\>** ir pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="ec86a-138">Select **Next \>**, and then select **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="ec86a-139">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="ec86a-139">See also</span></span>

[<span data-ttu-id="ec86a-140">Aptarnavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="ec86a-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="ec86a-141">Automatinis aptarnavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="ec86a-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="ec86a-142">[Aptarnavimo užsakymų kūrimas (klasės forma)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="ec86a-142">[Create service orders (class form)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
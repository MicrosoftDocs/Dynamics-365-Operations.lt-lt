---
title: Reiso būsenos nustatymas
description: Šioje temoje aprašoma, kaip nustatyti būsenos reikšmes, kurias vartotojai gali priskirti reisams.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500891"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="526ce-103">Reiso būsenos nustatymas</span><span class="sxs-lookup"><span data-stu-id="526ce-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="526ce-104">Puslapyje **Reiso būsenos** jūs nustatote būsenos reikšmių, kurias vartotojai gali priskirti reisams, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="526ce-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="526ce-105">Vartotojai gali priskirti reiso būsenos reikšmes visiems reiso lygiams: reisui, gabenimo konteineriui, registracijai, pirkimo užsakymui ir prekei (pirkimo eilutėms ir perkėlimo užsakymo eilutėms).</span><span class="sxs-lookup"><span data-stu-id="526ce-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="526ce-106">Jos yra naudojamos dviem tikslais:</span><span class="sxs-lookup"><span data-stu-id="526ce-106">They are used for two purposes:</span></span>

- <span data-ttu-id="526ce-107">Informuoti vartotoją apie reiso, gabenimo konteinerio, registracijos, pirkimo užsakymo arba prekės (pirkimo eilučių ir perkėlimo užsakymo eilučių) būseną.</span><span class="sxs-lookup"><span data-stu-id="526ce-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="526ce-108">Apriboti išlaidų srities naudojimą užkertant kelią modifikavimui arba naikinimui.</span><span class="sxs-lookup"><span data-stu-id="526ce-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="526ce-109">Norėdami nustatyti savo reiso būsenas, eikite į **Įkeltos išlaidos \> Nustatymas \> Reiso būsenos**.</span><span class="sxs-lookup"><span data-stu-id="526ce-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="526ce-110">Ten galite įtraukti, pašalinti ir redaguoti būsenas naudodami veiksmų srities mygtukus.</span><span class="sxs-lookup"><span data-stu-id="526ce-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="526ce-111">Kiekviena išlaidų sritis turi nuosavą reiso būsenų rinkinį ir hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="526ce-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="526ce-112">Taigi, puslapio **Reiso būsenos** lauke **Išlaidų sritis** pirmiausia turite pasirinkti išlaidų sritį, kuriai norite peržiūrėti ar sukurti reiso būsenas.</span><span class="sxs-lookup"><span data-stu-id="526ce-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="526ce-113">Tada, kiekvienai reiso būsenai nustatykite laukus, aprašytus toliau pateikiamoje lentelėje, kaip reikalaujama.</span><span class="sxs-lookup"><span data-stu-id="526ce-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="526ce-114">Atkreipkite dėmesį, kad reiso būseną taip pat gali automatiškai pakeisti sistemos įvykiai, pavyzdžiui, taisyklės, kurios buvo nustatytos naudojant sekimo kontrolės centrą.</span><span class="sxs-lookup"><span data-stu-id="526ce-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="526ce-115">Laukas</span><span class="sxs-lookup"><span data-stu-id="526ce-115">Field</span></span> | <span data-ttu-id="526ce-116">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="526ce-116">Description</span></span> |
|---|---|
| <span data-ttu-id="526ce-117">Reiso būsena</span><span class="sxs-lookup"><span data-stu-id="526ce-117">Voyage status</span></span> | <span data-ttu-id="526ce-118">Įvesti reiso būsenos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="526ce-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="526ce-119">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="526ce-119">Description</span></span> | <span data-ttu-id="526ce-120">Įveskite reiso būsenos aprašą.</span><span class="sxs-lookup"><span data-stu-id="526ce-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="526ce-121">Modifikuoti</span><span class="sxs-lookup"><span data-stu-id="526ce-121">Modify</span></span> | <span data-ttu-id="526ce-122">Pasirinkite šį žymės langelį, jeigu vartotojams leidžiama modifikuoti šios būsenos reisus.</span><span class="sxs-lookup"><span data-stu-id="526ce-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="526ce-123">Panaikinti</span><span class="sxs-lookup"><span data-stu-id="526ce-123">Delete</span></span> | <span data-ttu-id="526ce-124">Pasirinkite šį žymės langelį, jeigu vartotojams leidžiama panaikinti šios būsenos reisus.</span><span class="sxs-lookup"><span data-stu-id="526ce-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="526ce-125">Privalomas</span><span class="sxs-lookup"><span data-stu-id="526ce-125">Mandatory</span></span> | <span data-ttu-id="526ce-126">Pasirinkite šį žymės langelį, jei norite padaryti reiso būseną privaloma, kad jo nebūtų galima praleisti.</span><span class="sxs-lookup"><span data-stu-id="526ce-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="526ce-127">Pirminis</span><span class="sxs-lookup"><span data-stu-id="526ce-127">Parent</span></span> | <span data-ttu-id="526ce-128">Naudokite šį lauką hierarchijos tarp būsenos reikšmių nustatymui.</span><span class="sxs-lookup"><span data-stu-id="526ce-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="526ce-129">Reiso būsenos gali būti pakeistos (rankiniu arba automatiniu būdu) tik į žemesnę hierarchijos pakopą, nuo pirminės būsenos iki vienos iš jos antrinių būsenų.</span><span class="sxs-lookup"><span data-stu-id="526ce-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="526ce-130">Jūs turite nustatyti tik konkrečias reiso būsenas, kurias naudoja jūsų organizacija.</span><span class="sxs-lookup"><span data-stu-id="526ce-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="526ce-131">Įprastos reiso būsenos yra *Patvirtinta*, *Prekės tranzite*, *Gauta*, *Paruošta įkainojimui* ir *Įkainota*.</span><span class="sxs-lookup"><span data-stu-id="526ce-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="526ce-132">Tačiau gali būti ir kitokių būsenų.</span><span class="sxs-lookup"><span data-stu-id="526ce-132">However, other statuses might be present.</span></span>

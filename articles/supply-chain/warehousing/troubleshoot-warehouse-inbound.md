---
title: Trikčių šalinimo įvesties sandėlio veiksmai
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su įvesties sandėli veiksmais „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920992"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="37401-103">Trikčių šalinimo įvesties sandėlio veiksmai</span><span class="sxs-lookup"><span data-stu-id="37401-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37401-104">Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su įvesties sandėli veiksmais „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="37401-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="37401-105">Gautu tolesnį klaidos pranešimą: „Kokybės užsakymas %1 buvo sukurtas.</span><span class="sxs-lookup"><span data-stu-id="37401-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="37401-106">Klasterio profilio nepavyko rasti, prašome patikrinti konfigūravimą."</span><span class="sxs-lookup"><span data-stu-id="37401-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="37401-107">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="37401-107">Issue description</span></span>

<span data-ttu-id="37401-108">Šis klaidos pranešimas yra susijęs su gavimo procesu, nes kokybės valdymas (QMS) yra įjungtas.</span><span class="sxs-lookup"><span data-stu-id="37401-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="37401-109">Priklausomai nuo konfigūravimų jūsų aplinkoje, papildoma informacija apie perlaidą, sukurianti klaidos pranešimą, gali padėti ištaisyti triktį.</span><span class="sxs-lookup"><span data-stu-id="37401-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="37401-110">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="37401-110">Issue resolution</span></span>

<span data-ttu-id="37401-111">Pirmiausia, peržiūrėkite [klasterio paėmimo](set-up-cluster-picking.md) nustatymus ir įsitikinkite, kad klasterio profiliai yra tinkamai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="37401-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="37401-112">Negalite naudoti prekės mobiliojo įrenginio meniu klasterio paėmimui nebent klasterio profilis yra nustatytas.</span><span class="sxs-lookup"><span data-stu-id="37401-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="37401-113">Priklausomai nuo aplinkos, galbūt jums reikės peržiūrėti taip pat kitas susijusias konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="37401-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="37401-114">Maišytos licencijos plokštelės gavimas neveikia jokiam suteiktam kodui, išskyrus kredito.</span><span class="sxs-lookup"><span data-stu-id="37401-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="37401-115">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="37401-115">Issue description</span></span>

<span data-ttu-id="37401-116">Kai **Veiksmo** laukelis nustatytam kodui yra nustatytas *Kreditas* ar *Atmestas*, galite naudoti tik [Maišytos licencijos plokštelės gavimas](mixed-license-plate-receiving.md) meniu prekės į proceso sugrąžintas prekes.</span><span class="sxs-lookup"><span data-stu-id="37401-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="37401-117">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="37401-117">Issue resolution</span></span>

<span data-ttu-id="37401-118">„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą.</span><span class="sxs-lookup"><span data-stu-id="37401-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="37401-119">Šiuo metu tik [suteikti kodai](../service-management/set-up-disposition-codes.md), kai **Veiksmo** laukelis yra nustatytas į *Kreditai* ar *Atmestas* yra palaikomi maišytos licencijos plokštelės gavime.</span><span class="sxs-lookup"><span data-stu-id="37401-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="37401-120">Man vykdant naujinimo produkto gavimų periodinę užduotį, nepatvirtinti pirkimo užsakymai yra patvirtinami.</span><span class="sxs-lookup"><span data-stu-id="37401-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="37401-121">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="37401-121">Issue description</span></span>

<span data-ttu-id="37401-122">Man įvykdžius *Naujinimo produkto gavimų* periodinę užduotį, sistema automatiškai patvirtina nepatvirtintus pirkimo užsakymus, kurie turi inventoriaus perlaidos būseną *Registruotą*.</span><span class="sxs-lookup"><span data-stu-id="37401-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="37401-123">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="37401-123">Issue resolution</span></span>

<span data-ttu-id="37401-124">Nauja įvesties apkrovos tvarkymo funkcija, *Per krovinio kiekių gavimą*, ištaiso šią triktį.</span><span class="sxs-lookup"><span data-stu-id="37401-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="37401-125">Norėdami įjungti šią funkciją, eikite į [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį ir įjunkite tolesnes funkcijas (tam, kad jos būtų sąraše):</span><span class="sxs-lookup"><span data-stu-id="37401-125">To turn on this feature, go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="37401-126">Susieti pirkimo užsakymo atsargų operacijas su kroviniu</span><span class="sxs-lookup"><span data-stu-id="37401-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="37401-127">Krovinio kiekio perviršis</span><span class="sxs-lookup"><span data-stu-id="37401-127">Over receipt of load quantities</span></span>

<span data-ttu-id="37401-128">Dėl išsamesnės informacijos, žr. [Publikuoti registruotus produktų kiekius pagal pirkimo užsakymus](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="37401-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="37401-129">Registruodamas gaunamus užsakymus, gaunu tokį klaidos pranešimą: „Netinkamas kiekis.”</span><span class="sxs-lookup"><span data-stu-id="37401-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="37401-130">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="37401-130">Issue description</span></span>

<span data-ttu-id="37401-131">Jeigu laukas **Numerio lentelių grupavimo politika** nustatytas į *Vartotojo apibrėžtas* mobiliojo įrenginio meniu elementui, naudojamam registruoti gaunamiems užsakymams, gausite klaidos pranešimą („Netinkamas kiekis”) ir negalėsite užbaigti registracijos.</span><span class="sxs-lookup"><span data-stu-id="37401-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="37401-132">Problemos priežastis</span><span class="sxs-lookup"><span data-stu-id="37401-132">Issue cause</span></span>

<span data-ttu-id="37401-133">Kai *Vartotojo apibrėžta* yra naudojama kaip registracijos numerių grupavimo strategija, sistema išskaido gaunamas atsargas į atskiras numerio lenteles, kaip nurodyta pagal vienetų sekų grupę.</span><span class="sxs-lookup"><span data-stu-id="37401-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="37401-134">Jeigu paketo ar serijos numeriai yra naudojami gaunamai prekei sekti, kiekvieno paketo ar serijos kiekiai turi būti nurodyti užregistruotoje numerio lentelėje.</span><span class="sxs-lookup"><span data-stu-id="37401-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="37401-135">Jeigu numerio lentelėje nurodytas kiekis viršija kiekį, kurį vis dar reikia gauti pagal dabartines dimensijas, gausite klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="37401-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="37401-136">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="37401-136">Issue resolution</span></span>

<span data-ttu-id="37401-137">Kai registruojate prekę naudodami mobiliojo įrenginio meniu elementą, kurio laukas **Numerio lentelių grupavimo strategija** nustatytas į *Vartotojo apibrėžta*, sistema gali reikalauti, kad patvirtintumėte arba įvestumėte numerio lentelės, paketo arba serijos numerius.</span><span class="sxs-lookup"><span data-stu-id="37401-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="37401-138">Numerio lentelės patvirtinimo puslapyje sistema rodys kiekį, priskirtą dabartinei numerio lentelei.</span><span class="sxs-lookup"><span data-stu-id="37401-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="37401-139">Paketo arba serijos patvirtinimo puslapiuose sistema rodys kiekį, kuris vis dar turi būti gautas pagal dabartinę numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="37401-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="37401-140">Juose taip pat bus laukas, kuriame galite įvesti registruotiną kiekį tam numerio lentelės ir paketo ar serijos numerio deriniui.</span><span class="sxs-lookup"><span data-stu-id="37401-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="37401-141">Tokiu atveju įsitikinkite, kad registruojamas numerio lentelės kiekis neviršija kiekio, kuris vis dar turi būti gautas.</span><span class="sxs-lookup"><span data-stu-id="37401-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="37401-142">Kitu atveju, jei gavimo užsakymo registracijoje generuojama per daug numerio numerių, lauko **Numerio lentelių grupavimo strategija** reikšmė gali pasikeisti į *Numerio lentelių grupavimas*, nauja vienetų sekos grupės gali būti priskirta prekei arba parinktis **Numerio lentelių grupavimas** vienetų sekos grupei gali būti deaktyvuota.</span><span class="sxs-lookup"><span data-stu-id="37401-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

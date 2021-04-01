---
title: Trikčių šalinimo įvesties sandėlio veiksmai
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su įvesties sandėli veiksmais „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 6875c3c644b9993a384ba4d8623640536d7307e1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250887"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="cd2cd-103">Trikčių šalinimo įvesties sandėlio veiksmai</span><span class="sxs-lookup"><span data-stu-id="cd2cd-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd2cd-104">Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su įvesties sandėli veiksmais „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="cd2cd-105">Gautu tolesnį klaidos pranešimą: „Kokybės užsakymas %1 buvo sukurtas.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="cd2cd-106">Klasterio profilio nepavyko rasti, prašome patikrinti konfigūravimą."</span><span class="sxs-lookup"><span data-stu-id="cd2cd-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="cd2cd-107">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="cd2cd-107">Issue description</span></span>

<span data-ttu-id="cd2cd-108">Šis klaidos pranešimas yra susijęs su gavimo procesu, nes kokybės valdymas (QMS) yra įjungtas.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="cd2cd-109">Priklausomai nuo konfigūravimų jūsų aplinkoje, papildoma informacija apie perlaidą, sukurianti klaidos pranešimą, gali padėti ištaisyti triktį.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cd2cd-110">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="cd2cd-110">Issue resolution</span></span>

<span data-ttu-id="cd2cd-111">Pirmiausia, peržiūrėkite [klasterio paėmimo](set-up-cluster-picking.md) nustatymus ir įsitikinkite, kad klasterio profiliai yra tinkamai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="cd2cd-112">Negalite naudoti prekės mobiliojo įrenginio meniu klasterio paėmimui nebent klasterio profilis yra nustatytas.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="cd2cd-113">Priklausomai nuo aplinkos, galbūt jums reikės peržiūrėti taip pat kitas susijusias konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="cd2cd-114">Maišytos licencijos plokštelės gavimas neveikia jokiam suteiktam kodui, išskyrus kredito.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="cd2cd-115">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="cd2cd-115">Issue description</span></span>

<span data-ttu-id="cd2cd-116">Kai **Veiksmo** laukelis nustatytam kodui yra nustatytas *Kreditas* ar *Atmestas*, galite naudoti tik [Maišytos licencijos plokštelės gavimas](mixed-license-plate-receiving.md) meniu prekės į proceso sugrąžintas prekes.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cd2cd-117">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="cd2cd-117">Issue resolution</span></span>

<span data-ttu-id="cd2cd-118">„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="cd2cd-119">Šiuo metu tik [suteikti kodai](../service-management/set-up-disposition-codes.md), kai **Veiksmo** laukelis yra nustatytas į *Kreditai* ar *Atmestas* yra palaikomi maišytos licencijos plokštelės gavime.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="cd2cd-120">Man vykdant naujinimo produkto gavimų periodinę užduotį, nepatvirtinti pirkimo užsakymai yra patvirtinami.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="cd2cd-121">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="cd2cd-121">Issue description</span></span>

<span data-ttu-id="cd2cd-122">Man įvykdžius *Naujinimo produkto gavimų* periodinę užduotį, sistema automatiškai patvirtina nepatvirtintus pirkimo užsakymus, kurie turi inventoriaus perlaidos būseną *Registruotą*.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cd2cd-123">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="cd2cd-123">Issue resolution</span></span>

<span data-ttu-id="cd2cd-124">Nauja įvesties apkrovos tvarkymo funkcija, *Per krovinio kiekių gavimą*, ištaiso šią triktį.</span><span class="sxs-lookup"><span data-stu-id="cd2cd-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="cd2cd-125">Norėdami įjungti šią funkciją, eikite į [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir įjunkite tolesnes funkcijas (tam, kad jos būtų sąraše):</span><span class="sxs-lookup"><span data-stu-id="cd2cd-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="cd2cd-126">Susieti pirkimo užsakymo atsargų operacijas su kroviniu</span><span class="sxs-lookup"><span data-stu-id="cd2cd-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="cd2cd-127">Krovinio kiekio perviršis</span><span class="sxs-lookup"><span data-stu-id="cd2cd-127">Over receipt of load quantities</span></span>

<span data-ttu-id="cd2cd-128">Dėl išsamesnės informacijos, žr. [Publikuoti registruotus produktų kiekius pagal pirkimo užsakymus](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="cd2cd-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: "Produkto patvirtinimas klasterio paėmimui"
description: "Šioje temoje aprašoma, kaip nustatyti prekės patikrinimą, kurį atliekant būtų parenkamas ir klasteris."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 17f5761df4294abfea28e7cb8d50c86f1e3e136f
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

[!include[banner](../includes/banner.md)]

# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="824a9-103">Produkto patvirtinimas klasterio paėmimui</span><span class="sxs-lookup"><span data-stu-id="824a9-103">Product confirmation for cluster picking</span></span>
<span data-ttu-id="824a9-104">Pasirinkdami klasterius vienu metu galite pasirinkti keliems užsakymams skirtas prekes.</span><span class="sxs-lookup"><span data-stu-id="824a9-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="824a9-105">Kai taikomas klasterio pasirinkimas, būtina patvirtinti prekes, kad būtų galima patikrinti į klasterius įtraukiamas prekes.</span><span class="sxs-lookup"><span data-stu-id="824a9-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="824a9-106">Galite patikrinti prekes atlikdami klasterių pasirinkimą, vykstant klasterio parinkimo procesui.</span><span class="sxs-lookup"><span data-stu-id="824a9-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="824a9-107">Kai taikoma</span><span class="sxs-lookup"><span data-stu-id="824a9-107">Where it applies</span></span>
<span data-ttu-id="824a9-108">Prekių patikrinimas atliekant klasterio parinkimą atliekamas tuo pačiu būdu kaip ir tikrinant prekes nevykstant klasterių parinkimo procesams.</span><span class="sxs-lookup"><span data-stu-id="824a9-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="824a9-109">Sąranka pagrįsta produkto brūkšninio kodo sąranka.</span><span class="sxs-lookup"><span data-stu-id="824a9-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="824a9-110">Prekės patikrinimo nustatymas atliekant klasterio parinkimą</span><span class="sxs-lookup"><span data-stu-id="824a9-110">Set up item verification with cluster picking</span></span>
1.  <span data-ttu-id="824a9-111">Mobiliojo įrenginio meniu elemente atidarykite darbo patvirtinimo sąrankos formą: **Sandėlio valdymas** > **Sandėlio valdymas** > **Sąranka** > **Mobilusis įrenginys** > **Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="824a9-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
2.  <span data-ttu-id="824a9-112">Mobiliojo įrenginio meniu elemente atidarykite **Darbo patvirtinimo sąranka**.</span><span class="sxs-lookup"><span data-stu-id="824a9-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

| <span data-ttu-id="824a9-113">Parinktis</span><span class="sxs-lookup"><span data-stu-id="824a9-113">Option</span></span>        | <span data-ttu-id="824a9-114">aprašymas</span><span class="sxs-lookup"><span data-stu-id="824a9-114">Description</span></span>   | 
| ------------- | ------------- |
|<span data-ttu-id="824a9-115">Produkto patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="824a9-115">Product confirmation</span></span> | <span data-ttu-id="824a9-116">Mobiliuoju įrenginiu nuskaitydami galite patikrinti kiekvieną atsargų dalį.</span><span class="sxs-lookup"><span data-stu-id="824a9-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span>|

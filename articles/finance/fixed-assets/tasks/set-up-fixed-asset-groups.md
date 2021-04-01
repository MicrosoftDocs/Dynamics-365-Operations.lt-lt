---
title: Ilgalaikio turto grupių nustatymas
description: Šioje temoje paaiškinta, kaip sukurti naują ilgalaikio turto grupę.
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee3cec5c6abf08c88a61af2ec4bde6a863de2f95
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224650"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="bbba1-103">Ilgalaikio turto grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="bbba1-103">Set up fixed asset groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bbba1-104">Šioje temoje paaiškinta, kaip sukurti naują ilgalaikio turto grupę.</span><span class="sxs-lookup"><span data-stu-id="bbba1-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="bbba1-105">Jis naudoja vaidmenį Buhalteris ir USMF juridinio subjekto demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="bbba1-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="bbba1-106">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Sąranka > Ilgalaikio turto grupės**.</span><span class="sxs-lookup"><span data-stu-id="bbba1-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="bbba1-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="bbba1-107">Select **New**.</span></span>
3. <span data-ttu-id="bbba1-108">Lauke **Ilgalaikio turto grupė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bbba1-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="bbba1-109">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bbba1-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="bbba1-110">**Ilgalaikio turto** grupės parinktys Automatiškai numeruoti ilgalaikį turtą ir Numeracijos kodas perrašys ilgalaikio turto parametrų nuostatas.</span><span class="sxs-lookup"><span data-stu-id="bbba1-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="bbba1-111">Jei šios ilgalaikio turto grupės turtas bus numeruojamas kitaip nei kitose grupėse, čia numeravimą galite keisti.</span><span class="sxs-lookup"><span data-stu-id="bbba1-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="bbba1-112">Pasirinkite **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="bbba1-112">Select **Books**.</span></span>
6. <span data-ttu-id="bbba1-113">Lauke **Knyga** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bbba1-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="bbba1-114">Lauke **Skaičiuoti nusidėvėjimą** nustatyta reikšmė **Taip**, todėl turto knyga bus įtraukta į nusidėvėjimo pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="bbba1-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="bbba1-115">Jei lauke **Skaičiuoti nusidėvėjimą** nustatyta reikšmė **Ne**, turtas automatiškai nebus laikomas nusidėvėjusiu. </span><span class="sxs-lookup"><span data-stu-id="bbba1-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="bbba1-116">Nustatykite turto dėvėjimo laiką metais.</span><span class="sxs-lookup"><span data-stu-id="bbba1-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="bbba1-117">Atkreipkite dėmesį, kad lauko **Nusidėvėjimo laikotarpiai** reikšmė apskaičiuojama nustačius dėvėjimo laiką.</span><span class="sxs-lookup"><span data-stu-id="bbba1-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="bbba1-118">Lauke **Nusidėvėjimo konvencija** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="bbba1-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="bbba1-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bbba1-119">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
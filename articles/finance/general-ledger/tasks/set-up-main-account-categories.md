---
title: Pagrindinės sąskaitos kategorijų nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti pagrindinės sąskaitos kategorijas sistemoje „Dynamics 365 Finance“.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 957fdc184410dc85f54cd3163799a9003f0727bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222222"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="a17bc-103">Pagrindinės sąskaitos kategorijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a17bc-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a17bc-104">Šioje temoje paaiškinta, kaip nustatyti pagrindinės sąskaitos kategorijas.</span><span class="sxs-lookup"><span data-stu-id="a17bc-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="a17bc-105">Pagrindinės sąskaitos kategorijos naudojamos finansinių ataskaitų ir „Power BI“ numatytosioms ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="a17bc-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="a17bc-106">Pagrindines sąskaitos kategorijas, sukurtas pagal numatytuosius nustatymus, galima pervardyti, bet jų negalima panaikinti.</span><span class="sxs-lookup"><span data-stu-id="a17bc-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="a17bc-107">Ataskaitų ir analizės tikslams galima sukurti ir naudoti papildomas sąskaitos kategorijas.</span><span class="sxs-lookup"><span data-stu-id="a17bc-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="a17bc-108">Šioje temoje aprašoma demonstravimo įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="a17bc-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="a17bc-109">Pagrindinės sąskaitos kategorijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="a17bc-109">Create a main account category</span></span>
1. <span data-ttu-id="a17bc-110">Naršymo srityje eikite į **Moduliai > Didžioji knyga > Sąskaitų planas > Sąskaitos > Pagrindinės sąskaitos kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="a17bc-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="a17bc-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a17bc-111">Select **New**.</span></span>
3. <span data-ttu-id="a17bc-112">Lauke **Pagrindinės sąskaitos kategorija** įveskite unikalų pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="a17bc-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="a17bc-113">Lauke **Aprašas** įveskite pagrindinės sąskaitos kategorijos aprašą.</span><span class="sxs-lookup"><span data-stu-id="a17bc-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="a17bc-114">Lauke **Pagrindinės sąskaitos tipas** pasirinkite pagrindinės sąskaitos tipą, kuris bus susietas su kategorija.</span><span class="sxs-lookup"><span data-stu-id="a17bc-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="a17bc-115">Pagrindinių sąskaitų susiejimas su sąskaitos kategorija</span><span class="sxs-lookup"><span data-stu-id="a17bc-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="a17bc-116">Spustelėkite **Susieti pagrindines sąskaitas**.</span><span class="sxs-lookup"><span data-stu-id="a17bc-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="a17bc-117">Sąraše pasirinkite pagrindines sąskaitas, kurias norite priskirti pagrindinės sąskaitos kategorijai, pažymėdami langelius stulpelyje **Susieta**.</span><span class="sxs-lookup"><span data-stu-id="a17bc-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="a17bc-118">Pagrindines sąskaitas priskyrus pagrindinės sąskaitos kategorijai ir naudojant tą kategoriją finansinėms ataskaitoms ir analizei, bus sujungti sąskaitų balansai.</span><span class="sxs-lookup"><span data-stu-id="a17bc-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="a17bc-119">Norėdami pasirinkti pagrindines sąskaitas pažymėkite arba išvalykite parinktį **Susieta**.</span><span class="sxs-lookup"><span data-stu-id="a17bc-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="a17bc-120">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a17bc-120">Select **OK**.</span></span>
5. <span data-ttu-id="a17bc-121">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a17bc-121">Select **Yes**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
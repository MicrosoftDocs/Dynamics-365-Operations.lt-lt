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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0a015283064af2287013bccc065b4467a308c5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144794"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="f9fd0-103">Pagrindinės sąskaitos kategorijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="f9fd0-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9fd0-104">Šioje temoje paaiškinta, kaip nustatyti pagrindinės sąskaitos kategorijas.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="f9fd0-105">Pagrindinės sąskaitos kategorijos naudojamos finansinių ataskaitų ir „Power BI“ numatytosioms ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="f9fd0-106">Pagrindines sąskaitos kategorijas, sukurtas pagal numatytuosius nustatymus, galima pervardyti, bet jų negalima panaikinti.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="f9fd0-107">Ataskaitų ir analizės tikslams galima sukurti ir naudoti papildomas sąskaitos kategorijas.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="f9fd0-108">Šioje temoje aprašoma demonstravimo įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="f9fd0-109">Pagrindinės sąskaitos kategorijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="f9fd0-109">Create a main account category</span></span>
1. <span data-ttu-id="f9fd0-110">Naršymo srityje eikite į **Moduliai > Didžioji knyga > Sąskaitų planas > Sąskaitos > Pagrindinės sąskaitos kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="f9fd0-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-111">Select **New**.</span></span>
3. <span data-ttu-id="f9fd0-112">Lauke **Pagrindinės sąskaitos kategorija** įveskite unikalų pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="f9fd0-113">Lauke **Aprašas** įveskite pagrindinės sąskaitos kategorijos aprašą.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="f9fd0-114">Lauke **Pagrindinės sąskaitos tipas** pasirinkite pagrindinės sąskaitos tipą, kuris bus susietas su kategorija.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="f9fd0-115">Pagrindinių sąskaitų susiejimas su sąskaitos kategorija</span><span class="sxs-lookup"><span data-stu-id="f9fd0-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="f9fd0-116">Spustelėkite **Susieti pagrindines sąskaitas**.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="f9fd0-117">Sąraše pasirinkite pagrindines sąskaitas, kurias norite priskirti pagrindinės sąskaitos kategorijai, pažymėdami langelius stulpelyje **Susieta**.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="f9fd0-118">Pagrindines sąskaitas priskyrus pagrindinės sąskaitos kategorijai ir naudojant tą kategoriją finansinėms ataskaitoms ir analizei, bus sujungti sąskaitų balansai.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="f9fd0-119">Norėdami pasirinkti pagrindines sąskaitas pažymėkite arba išvalykite parinktį **Susieta**.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="f9fd0-120">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-120">Select **OK**.</span></span>
5. <span data-ttu-id="f9fd0-121">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="f9fd0-121">Select **Yes**.</span></span>

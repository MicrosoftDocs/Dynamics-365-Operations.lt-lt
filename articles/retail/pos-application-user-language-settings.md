---
title: EKA programos ir vartotojo kalbos parametrai
description: "Šioje temoje aprašoma, kaip keisti kalbos parametrus naudojant „Retail Modern POS“ (MPOS) ir „Cloud POS“."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: dacc072ab5c070010d86302fa08a3066125b23a6
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="c4fb8-103">EKA programos ir vartotojo kalbos parametrai</span><span class="sxs-lookup"><span data-stu-id="c4fb8-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="c4fb8-104">Šioje temoje aprašoma, kaip keisti kalbos parametrus naudojant „Retail Modern POS“ (MPOS) ir „Cloud POS“.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="c4fb8-105">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="c4fb8-105">Overview</span></span>
========

<span data-ttu-id="c4fb8-106">„Retail Modern POS“ (MPOS) ir „Cloud POS“ palaiko aplinkas, kuriose parduotuvės ir vartotojų nustatyti kalbos parametrai ir vertimai gali skirtis.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="c4fb8-107">Pavyzdžiui, parduotuvė gali būti regione, kuriame klientai dažniausiai vartoja anglų kalbą, bet kai kurie darbuotojai labiau norėtų naudoti programą, kuri išversta į prancūzų kalbą.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="c4fb8-108">Duomenų kalba</span><span class="sxs-lookup"><span data-stu-id="c4fb8-108">Data language</span></span>
<span data-ttu-id="c4fb8-109">Nepriklausomai nuo to, kokie yra vartotojo parametrai, nusprendžiant, kokius naudoti duomenų vertimus, MPOS ir „Cloud POS“ visada naudojami parduotuvės kalbos parametrai.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="c4fb8-110">Taip užtikrinama, kad visų vartotojų ir klientų patirtis būtų nuosekli.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="c4fb8-111">Duomenų pavyzdžiai:</span><span class="sxs-lookup"><span data-stu-id="c4fb8-111">Examples of data include:</span></span>

-   <span data-ttu-id="c4fb8-112">Produktai</span><span class="sxs-lookup"><span data-stu-id="c4fb8-112">Products</span></span>
-   <span data-ttu-id="c4fb8-113">Atributai ir reikšmės</span><span class="sxs-lookup"><span data-stu-id="c4fb8-113">Attributes and values</span></span>
-   <span data-ttu-id="c4fb8-114">Kategorijų pavadinimai</span><span class="sxs-lookup"><span data-stu-id="c4fb8-114">Category names</span></span>
-   <span data-ttu-id="c4fb8-115">Išspausdinti arba el. paštu išsiųsti operacijų kvitai</span><span class="sxs-lookup"><span data-stu-id="c4fb8-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="c4fb8-116">Mokėjimo būdo pavadinimai</span><span class="sxs-lookup"><span data-stu-id="c4fb8-116">Payment method names</span></span>
-   <span data-ttu-id="c4fb8-117">Eilutės rodymo pranešimai</span><span class="sxs-lookup"><span data-stu-id="c4fb8-117">Line display messages</span></span>

<span data-ttu-id="c4fb8-118">Parduotuvės kalba taip pat naudojama pagrindiniame EKA prisijungimo ekrane, nes kol neprisijungiama vartotojas nežinomas.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="c4fb8-119">Jei parduotuvės kalba vertimo nėra, EKA iš naujo nustatys įmonės kalbą.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="c4fb8-120">Parduotuvės kalbos parametro konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c4fb8-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="c4fb8-121">Parduotuvės kalbos parametras yra nustatomas dalyje **Visos mažmeninės prekybos parduotuvės**, kurią galima rasti puslapyje **Mažmeninės prekybos parduotuvė** pasirinkus **Bendrieji parametrai &gt; Regiono parametrai &gt; Kalba.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="c4fb8-122">**Naudodami išskleidžiamąjį sąrašą pasirinkite kiekvienos parduotuvės kalbą.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="c4fb8-123">Vartotojo sąsajos kalba</span><span class="sxs-lookup"><span data-stu-id="c4fb8-123">User interface language</span></span>
<span data-ttu-id="c4fb8-124">Pagal EKA vartotojo kalbos parametrus nustatomi programos vartotojo sąsajoje naudojami vertimai.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="c4fb8-125">Vertimai naudojami visose etiketėse, meniu ir sąrašuose, kurie nelaikomi duomenimis.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="c4fb8-126">Viena išimtis yra EKA mygtukynuose rodomas tekstas.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="c4fb8-127">Mygtukynuose vertimai nepalaikomi, todėl tekstas juose visada rodomas taip, kaip nurodyta ant mygtuko.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="c4fb8-128">Norint, kad būtų palaikomi išversti mygtukai, reikia nukopijuoti ir išlaikyti atskirus mygtukynus ir priskirti juos atitinkamiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="c4fb8-129">Vartotojo kalbos parametro konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c4fb8-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="c4fb8-130">EKA vartotojo kalbos parametras yra nustatomas dalyje **Visi darbuotoji**, kurią galima rasti puslapyje **Darbuotojas** pasirinkus **Mažmeninė prekyba &gt; Kalba**.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="c4fb8-131">Jis nėra nustatomas pagrindiniame profilio skirtuke. EKA šio parametro nenaudoja.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-131">It is not set on the main Profile tab.  This setting is not used by POS.</span></span> <span data-ttu-id="c4fb8-132">Jei nenustatyta vartotojo kalba arba nustatyta kalba, kurios vertimų nėra, EKA iš naujo nustatys parduotuvės kalbą.</span><span class="sxs-lookup"><span data-stu-id="c4fb8-132">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="c4fb8-133">** **</span><span class="sxs-lookup"><span data-stu-id="c4fb8-133">** **</span></span>       | <span data-ttu-id="c4fb8-134">**Vartotojo sąsajos kalba** ** **</span><span class="sxs-lookup"><span data-stu-id="c4fb8-134">**UI language** ** **</span></span>      | <span data-ttu-id="c4fb8-135">**Duomenų kalba (produktų, gavimo kvitų formatų, eilutės rodymo ir kt.)**</span><span class="sxs-lookup"><span data-stu-id="c4fb8-135">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="c4fb8-136">**Įmonė**</span><span class="sxs-lookup"><span data-stu-id="c4fb8-136">**Company**</span></span> | <span data-ttu-id="c4fb8-137">Numatytoji</span><span class="sxs-lookup"><span data-stu-id="c4fb8-137">Default</span></span>                    | <span data-ttu-id="c4fb8-138">Numatytoji</span><span class="sxs-lookup"><span data-stu-id="c4fb8-138">Default</span></span>                                                           |
| <span data-ttu-id="c4fb8-139">**Parduotuvė**</span><span class="sxs-lookup"><span data-stu-id="c4fb8-139">**Store**</span></span>   | <span data-ttu-id="c4fb8-140">Perrašoma įmonė</span><span class="sxs-lookup"><span data-stu-id="c4fb8-140">Overrides company</span></span>          | <span data-ttu-id="c4fb8-141">Perrašoma įmonė</span><span class="sxs-lookup"><span data-stu-id="c4fb8-141">Overrides company</span></span>                                                 |
| <span data-ttu-id="c4fb8-142">**Vartotojas**</span><span class="sxs-lookup"><span data-stu-id="c4fb8-142">**User**</span></span>    | <span data-ttu-id="c4fb8-143">Perrašoma parduotuvė arba įmonė</span><span class="sxs-lookup"><span data-stu-id="c4fb8-143">Overrides store or company</span></span> | <span data-ttu-id="c4fb8-144">Niekada</span><span class="sxs-lookup"><span data-stu-id="c4fb8-144">Never</span></span>                                                             |







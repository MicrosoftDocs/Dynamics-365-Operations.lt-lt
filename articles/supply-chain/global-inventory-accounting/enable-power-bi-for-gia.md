---
title: Įgalinti „Power BI” Visuotinę atsargų apskaitą
description: Šioje temoje aprašoma, kaip įgalinti „Microsoft Power BI” Visuotinei atsargų apskaitai.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273197"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="8b88b-103">Įgalinti „Power BI” Visuotinę atsargų apskaitą</span><span class="sxs-lookup"><span data-stu-id="8b88b-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="8b88b-104">Galite prisegti plyteles, ataskaitų sritis ir ataskaitas iš savo [„PowerBI.com”](https://powerbi.com/) paskyros į savo „Microsoft Dynamics 365” programos darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="8b88b-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8b88b-105">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="8b88b-105">Prerequisites</span></span>

<span data-ttu-id="8b88b-106">Prieš įgalindami „Power BI” ataskaitas privalote atitikti šias būtinąsias sąlygas:</span><span class="sxs-lookup"><span data-stu-id="8b88b-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="8b88b-107">Turite būti sistemos administratorius „Dynamics 365” programoje.</span><span class="sxs-lookup"><span data-stu-id="8b88b-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="8b88b-108">Privalote turėti [„PowerBI.com”](https://powerbi.com/) paskyrą.</span><span class="sxs-lookup"><span data-stu-id="8b88b-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="8b88b-109">Privalote turėti bent vieną ataskaitų sritį ir ataskaitą savo „Power BI” paskyroje.</span><span class="sxs-lookup"><span data-stu-id="8b88b-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="8b88b-110">Turite būti savo „Azure Active Directory” („Azure AD”) paskyros administratorius.</span><span class="sxs-lookup"><span data-stu-id="8b88b-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="8b88b-111">„Azure AD” domenas turi būti tas pats domenas, kurį naudojote savo [„PowerBI.com”](https://powerbi.com/) paskyrai.</span><span class="sxs-lookup"><span data-stu-id="8b88b-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="8b88b-112">Sąranka</span><span class="sxs-lookup"><span data-stu-id="8b88b-112">Setup</span></span>

<span data-ttu-id="8b88b-113">Norėdami nustatyti „Power BI” integravimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8b88b-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="8b88b-114">Prisijunkite prie [„Microsoft Dynamics” „Lifecycle Services” (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="8b88b-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="8b88b-115">Eikite į **Bendrai naudojamo turto biblioteką**, pasirinkite **„Power BI” ataskaitos modelį** kaip turto tipą ir atsisiųskite **Visuotinės atsargų apskaitos** paketą.</span><span class="sxs-lookup"><span data-stu-id="8b88b-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="8b88b-116">Prisijunkite prie [„PowerBI.com”](https://app.powerbi.com/) ir įkelkite **Visuotinės atsargų apskaitos** „Power BI” ataskaitos failą atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="8b88b-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="8b88b-117">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="8b88b-117">Select **New**.</span></span>
    1. <span data-ttu-id="8b88b-118">Pasirinkite **Įkelti failą**.</span><span class="sxs-lookup"><span data-stu-id="8b88b-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="8b88b-119">Pasirinkite **Visuotinės atsargų apskaitos** „Power BI” ataskaitos failą.</span><span class="sxs-lookup"><span data-stu-id="8b88b-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="8b88b-120">Sukonfigūruokite **Visuotinės atsargų apskaitos** „Power BI” ataskaitą atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="8b88b-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="8b88b-121">Eikite į **Mano darbo sritis**, suraskite Visuotinės atsargų apskaitos duomenų rinkinį, o tada iš meniu **Parinktys** pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="8b88b-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="8b88b-122">**Visuotinės atsargų apskaitos parametruose** išplėskite **Parametrus** ir atnaujinkite visus parametrus, kaip reikalinga.</span><span class="sxs-lookup"><span data-stu-id="8b88b-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="8b88b-123">Užregistruokite programą, kaip aprašyta [PowerBI.com integravimo konfigūravimas](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span><span class="sxs-lookup"><span data-stu-id="8b88b-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="8b88b-124">Integruokite **Visuotinės atsargų ataskaitos** „Power BI” ataskaitos failą į „Dynamics 365 Supply Chain Management” atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="8b88b-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="8b88b-125">Eikite į **Sistemos administravimas \> Sąranka \> PowerBI.com konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="8b88b-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="8b88b-126">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="8b88b-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="8b88b-127">Pasirinkite **Įgalinti PowerBI.Com integravimą**.</span><span class="sxs-lookup"><span data-stu-id="8b88b-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="8b88b-128">Lauke **Programos ID** įveskite programos ID.</span><span class="sxs-lookup"><span data-stu-id="8b88b-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="8b88b-129">Lauke **Programos raktas** įveskite programos raktą.</span><span class="sxs-lookup"><span data-stu-id="8b88b-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="8b88b-130">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="8b88b-130">Select **Save**.</span></span>

1. <span data-ttu-id="8b88b-131">Atnaujinkite puslapį, kad atsirastų „Power BI” prisijungimo dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="8b88b-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="8b88b-132">Skirtuke **Parinktys** pasirinkite **Atidaryti ataskaitos katalogą**, o tada pasirinkite **Visuotinės atsargų apskaitos** „Power BI” ataskaitos failą, kurį įkėlėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="8b88b-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="8b88b-133">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8b88b-133">Refresh the page.</span></span> <span data-ttu-id="8b88b-134">Turėtumėte pamatyti, kad jūsų ataskaita įtraukta.</span><span class="sxs-lookup"><span data-stu-id="8b88b-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="8b88b-135">Dalyje **„Power BI” ataskaitos** pasirinkite **Visuotinės atsargų apskaitos** nuorodą.</span><span class="sxs-lookup"><span data-stu-id="8b88b-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="8b88b-136">Daugiau informacijos rasite [PowerBI.com integravimo konfigūravimas](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="8b88b-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>

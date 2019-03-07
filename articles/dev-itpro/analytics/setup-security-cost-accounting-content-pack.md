---
title: Kaštų apskaitos analizės „Power BI“ turinio apsaugos nustatymas
description: Šioje temoje paaiškinta, kaip Kaštų apskaitoje galite išplatinti prieigos lygio saugą į eilutės lygio saugą in „Microsoft Power BI“. Ši funkcija padeda užtikrinti, kad vartotojai matys tik „Power BI“ duomenis, kuriems matyti prieiga yra suteikta.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d1cd378a58d4a4fe4388238f97e84a8e2b07937b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "352878"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="eb23c-104">Kaštų apskaitos analizės „Power BI“ turinio apsaugos nustatymas</span><span class="sxs-lookup"><span data-stu-id="eb23c-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb23c-105">Šioje temoje paaiškinta, kaip Kaštų apskaitoje galite išplatinti prieigos lygio saugą į eilutės lygio saugą in „Microsoft Power BI“.</span><span class="sxs-lookup"><span data-stu-id="eb23c-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="eb23c-106">Ši funkcija padeda užtikrinti, kad vartotojai matys tik „Power BI“ duomenis, kuriems matyti prieiga yra suteikta.</span><span class="sxs-lookup"><span data-stu-id="eb23c-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="eb23c-107">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="eb23c-107">Overview</span></span>

<span data-ttu-id="eb23c-108">„Microsoft Power BI“ turinys **Kaštų apskaitos analizė** naudoja „Power BI“ eilutės lygio saugą vartotojo prieigai apriboti.</span><span class="sxs-lookup"><span data-stu-id="eb23c-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="eb23c-109">Sauga pagrįsta prieigos lygio organizacijos hierarchija, kuri nustatyta Kaštų apskaitos parametruose.</span><span class="sxs-lookup"><span data-stu-id="eb23c-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="eb23c-110">Išsamesnės informacijos apie „Power BI“ turinį **Kaštų apskaitos analizė** žr. [„Power BI“ turinys Kaštų apskaitos analizė](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="eb23c-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="eb23c-111">Sąranka</span><span class="sxs-lookup"><span data-stu-id="eb23c-111">Setup</span></span>
<span data-ttu-id="eb23c-112">Norint paskirstyti prieigos lygio saugą „Power BI“, „Power BI“ turinio savininkas turi atlikti šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="eb23c-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="eb23c-113">„Power BI“ turinį **Kaštų apskaitos analizė** publikavęs vartotojas automatiškai tampa savininku.</span><span class="sxs-lookup"><span data-stu-id="eb23c-113">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="eb23c-114">Tik savininkas gali nustatyti „Power BI“ saugą.</span><span class="sxs-lookup"><span data-stu-id="eb23c-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="eb23c-115">Be to, kol savininkas neįtraukia kitų vartotojų į PowerBI.com, niekas, išskyrus savininką, negali matyti jokių duomenų „Power BI“ turinyje **Kaštų apskaitos analizė**.</span><span class="sxs-lookup"><span data-stu-id="eb23c-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="eb23c-116">Publikuokite apibrėžimo failą į „Power BI“.</span><span class="sxs-lookup"><span data-stu-id="eb23c-116">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="eb23c-117">Prisijunkite prie PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="eb23c-117">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="eb23c-118">Raskite „Power BI“ turinio **Kaštų apskaitos analizė** duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="eb23c-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="eb23c-119">Atidarykite saugos puslapį.</span><span class="sxs-lookup"><span data-stu-id="eb23c-119">Open the security page.</span></span>

    ![Saugos puslapio atidarymas](./media/CA-picture-1.png)

5. <span data-ttu-id="eb23c-121">**Savikainos objekto valdiklis** vaidmuo jau sukurtas.</span><span class="sxs-lookup"><span data-stu-id="eb23c-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="eb23c-122">Įtraukite kitų narių, kurie yra Kaštų apskaitos prieigos lygio organizacijos hierarchijos dalis.</span><span class="sxs-lookup"><span data-stu-id="eb23c-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Narių įtraukimas](./media/CA-picture-2.png)

<span data-ttu-id="eb23c-124">Į **Savikainos objekto valdiklis** vaidmenį įtraukti vartotojai, matys tik tuos duomenis, kuriuos jiems leidžiama matyti, pagal apibrėžimą Kaštų apskaitos prieigos lygio organizacijos hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="eb23c-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="eb23c-125">Eilutės lygio sauga taikoma išklotinėms ir ataskaitoms sprendime „Microsoft Dynamics 365 for Finance and Operations“, kurios įdėtos iš „Power BI“.</span><span class="sxs-lookup"><span data-stu-id="eb23c-125">Row-level security applies to tiles and reports in Microsoft Dynamics 365 for Finance and Operations that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="eb23c-126">Saugos atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="eb23c-126">Updating security</span></span>
<span data-ttu-id="eb23c-127">Jei atliekama Kaštų apskaitos prieigos lygio saugos atnaujinimų, o jūs norite, kad „Power BI“ atspindėtų šiuos atnaujinimus, turime atnaujinti objekto parduotuvės „Power BI“ turinį **Kaštų apskaitos analizė**.</span><span class="sxs-lookup"><span data-stu-id="eb23c-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="eb23c-128">Baigę naujinti objektų saugyklą iš „Finance and Operations“, turite atnaujinti PowerBI.com artefaktus.</span><span class="sxs-lookup"><span data-stu-id="eb23c-128">After you complete the entity store update from Finance and Operations, you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="eb23c-129">Išsamesnės informacijos apie tai, kaip atnaujinti objekto parduotuvės saugą, žr. [Objekto parduotuvės atnaujinimas](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="eb23c-129">For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="eb23c-130">„Power BI“ turinio **Kaštų apskaitos analizė** savininkas taip pat turi atnaujinti objekto parduotuvę, jei naujiems vartotojams suteikiama prieiga prie organizacijos hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="eb23c-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="eb23c-131">Be to, savininkas turi įtraukti naujus vartotojus į **Savikainos objekto valdiklis** vaidmenį PowerBI.com, kad jiems būtų taikoma eilutės lygio sauga.</span><span class="sxs-lookup"><span data-stu-id="eb23c-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="eb23c-132">Saugos išjungimas</span><span class="sxs-lookup"><span data-stu-id="eb23c-132">Disabling security</span></span>
<span data-ttu-id="eb23c-133">Laikome, kad jūsų organizacija nori apriboti duomenų prieigą.</span><span class="sxs-lookup"><span data-stu-id="eb23c-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="eb23c-134">Jei dėl tam tikrų priežasčių vykdant Kaštų apskaitą saugos parametrai yra išjungti, savininkas turi įtraukti vartotojus į „Power BI“ **Išlaidų buhalteris**.</span><span class="sxs-lookup"><span data-stu-id="eb23c-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="eb23c-135">Jei saugą pakeisite iš įgalintos būsenos į išjungtą būseną, pravartu pašalinti vartotojus iš vaidmens **Savikainos objekto valdiklis**.</span><span class="sxs-lookup"><span data-stu-id="eb23c-135">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="eb23c-136">Ir atvirkščiai, jei saugą vėl įgalinsite.</span><span class="sxs-lookup"><span data-stu-id="eb23c-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="eb23c-137">Vartotojai gali priklausyti abiems vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="eb23c-137">Users can belong to both roles.</span></span> <span data-ttu-id="eb23c-138">Bendra prieiga yra abiejų vaidmenų jungtis.</span><span class="sxs-lookup"><span data-stu-id="eb23c-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="eb23c-139">„Power BI“ turinio **Kaštų apskaitos analizė** atveju bendrą prieigą turintys vartotojai turi neribotą duomenų prieigą.</span><span class="sxs-lookup"><span data-stu-id="eb23c-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="eb23c-140">Jei norite taikyti apribotą prieigą, vartotojus priskirkite tik vaidmeniui **Savikainos objekto valdiklis**.</span><span class="sxs-lookup"><span data-stu-id="eb23c-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="eb23c-141">Šie eilutės lygio saugos naujinimai įsigalioja nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="eb23c-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="eb23c-142">Paveikti vartotojai turi atnaujinti savo naršykles.</span><span class="sxs-lookup"><span data-stu-id="eb23c-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb23c-143">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="eb23c-143">Additional resources</span></span>
<span data-ttu-id="eb23c-144">Norėdami daugiau sužinoti apie „Power BI“ eilutės lygio saugą žr. [Saugos valdymas savo modelyje „Power BI“](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="eb23c-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>

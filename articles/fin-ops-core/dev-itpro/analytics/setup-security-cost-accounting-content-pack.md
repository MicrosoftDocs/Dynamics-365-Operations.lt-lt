---
title: Kaštų apskaitos analizės „Power BI“ turinio apsaugos nustatymas
description: Šioje temoje paaiškinta, kaip Kaštų apskaitoje galite išplatinti prieigos lygio saugą į eilutės lygio saugą in „Microsoft Power BI“.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 10b87d01fd1172f4509f6fa803522eb25e73f9f5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559680"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="664a4-103">Kaštų apskaitos analizės „Power BI“ turinio apsaugos nustatymas</span><span class="sxs-lookup"><span data-stu-id="664a4-103">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="664a4-104">Šioje temoje paaiškinta, kaip Kaštų apskaitoje galite išplatinti prieigos lygio saugą į eilutės lygio saugą in „Microsoft Power BI“.</span><span class="sxs-lookup"><span data-stu-id="664a4-104">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="664a4-105">Ši funkcija padeda užtikrinti, kad vartotojai matys tik „Power BI“ duomenis, kuriems matyti prieiga yra suteikta.</span><span class="sxs-lookup"><span data-stu-id="664a4-105">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="664a4-106">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="664a4-106">Overview</span></span>

<span data-ttu-id="664a4-107">„Microsoft Power BI“ turinys **Kaštų apskaitos analizė** naudoja „Power BI“ eilutės lygio saugą vartotojo prieigai apriboti.</span><span class="sxs-lookup"><span data-stu-id="664a4-107">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="664a4-108">Sauga pagrįsta prieigos lygio organizacijos hierarchija, kuri nustatyta Kaštų apskaitos parametruose.</span><span class="sxs-lookup"><span data-stu-id="664a4-108">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="664a4-109">Išsamesnės informacijos apie „Power BI“ turinį **Kaštų apskaitos analizė** žr. [„Power BI“ turinys Kaštų apskaitos analizė](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="664a4-109">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="664a4-110">Sąranka</span><span class="sxs-lookup"><span data-stu-id="664a4-110">Setup</span></span>
<span data-ttu-id="664a4-111">Norint paskirstyti prieigos lygio saugą „Power BI“, „Power BI“ turinio savininkas turi atlikti šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="664a4-111">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="664a4-112">„Power BI“ turinį **Kaštų apskaitos analizė** publikavęs vartotojas automatiškai tampa savininku.</span><span class="sxs-lookup"><span data-stu-id="664a4-112">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="664a4-113">Tik savininkas gali nustatyti „Power BI“ saugą.</span><span class="sxs-lookup"><span data-stu-id="664a4-113">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="664a4-114">Be to, kol savininkas neįtraukia kitų vartotojų į PowerBI.com, niekas, išskyrus savininką, negali matyti jokių duomenų „Power BI“ turinyje **Kaštų apskaitos analizė**.</span><span class="sxs-lookup"><span data-stu-id="664a4-114">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="664a4-115">Publikuokite apibrėžimo failą į „Power BI“.</span><span class="sxs-lookup"><span data-stu-id="664a4-115">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="664a4-116">Prisijunkite prie PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="664a4-116">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="664a4-117">Raskite „Power BI“ turinio **Kaštų apskaitos analizė** duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="664a4-117">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="664a4-118">Atidarykite saugos puslapį.</span><span class="sxs-lookup"><span data-stu-id="664a4-118">Open the security page.</span></span>

    ![Saugos puslapio atidarymas](./media/CA-picture-1.png)

5. <span data-ttu-id="664a4-120">**Savikainos objekto valdiklis** vaidmuo jau sukurtas.</span><span class="sxs-lookup"><span data-stu-id="664a4-120">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="664a4-121">Įtraukite kitų narių, kurie yra Kaštų apskaitos prieigos lygio organizacijos hierarchijos dalis.</span><span class="sxs-lookup"><span data-stu-id="664a4-121">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Narių įtraukimas](./media/CA-picture-2.png)

<span data-ttu-id="664a4-123">Į **Savikainos objekto valdiklis** vaidmenį įtraukti vartotojai, matys tik tuos duomenis, kuriuos jiems leidžiama matyti, pagal apibrėžimą Kaštų apskaitos prieigos lygio organizacijos hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="664a4-123">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="664a4-124">Eilutės lygio sauga taikoma išklotinėms ir ataskaitoms, kurios įdėtos iš „Power BI“.</span><span class="sxs-lookup"><span data-stu-id="664a4-124">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="664a4-125">Saugos atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="664a4-125">Updating security</span></span>
<span data-ttu-id="664a4-126">Jei atliekama Kaštų apskaitos prieigos lygio saugos atnaujinimų, o jūs norite, kad „Power BI“ atspindėtų šiuos atnaujinimus, turime atnaujinti objekto parduotuvės „Power BI“ turinį **Kaštų apskaitos analizė**.</span><span class="sxs-lookup"><span data-stu-id="664a4-126">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="664a4-127">Baigę naujinti objektų saugyklą, turite atnaujinti PowerBI.com artefaktus.</span><span class="sxs-lookup"><span data-stu-id="664a4-127">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="664a4-128">Daugiau informacijos apie tai, kaip naujinti objekto parduotuvės saugą, žr. [„Power BI“ integravimas su objekto parduotuve](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="664a4-128">For more information about how to do an entity store update, see [Power BI integration with Entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="664a4-129">„Power BI“ turinio **Kaštų apskaitos analizė** savininkas taip pat turi atnaujinti objekto parduotuvę, jei naujiems vartotojams suteikiama prieiga prie organizacijos hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="664a4-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="664a4-130">Be to, savininkas turi įtraukti naujus vartotojus į **Savikainos objekto valdiklis** vaidmenį PowerBI.com, kad jiems būtų taikoma eilutės lygio sauga.</span><span class="sxs-lookup"><span data-stu-id="664a4-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="664a4-131">Saugos išjungimas</span><span class="sxs-lookup"><span data-stu-id="664a4-131">Disabling security</span></span>
<span data-ttu-id="664a4-132">Laikome, kad jūsų organizacija nori apriboti duomenų prieigą.</span><span class="sxs-lookup"><span data-stu-id="664a4-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="664a4-133">Jei dėl tam tikrų priežasčių vykdant Kaštų apskaitą saugos parametrai yra išjungti, savininkas turi įtraukti vartotojus į „Power BI“ **Išlaidų buhalteris**.</span><span class="sxs-lookup"><span data-stu-id="664a4-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="664a4-134">Jei saugą pakeisite iš įgalintos būsenos į išjungtą būseną, pravartu pašalinti vartotojus iš vaidmens **Savikainos objekto valdiklis**.</span><span class="sxs-lookup"><span data-stu-id="664a4-134">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="664a4-135">Ir atvirkščiai, jei saugą vėl įgalinsite.</span><span class="sxs-lookup"><span data-stu-id="664a4-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="664a4-136">Vartotojai gali priklausyti abiems vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="664a4-136">Users can belong to both roles.</span></span> <span data-ttu-id="664a4-137">Bendra prieiga yra abiejų vaidmenų jungtis.</span><span class="sxs-lookup"><span data-stu-id="664a4-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="664a4-138">„Power BI“ turinio **Kaštų apskaitos analizė** atveju bendrą prieigą turintys vartotojai turi neribotą duomenų prieigą.</span><span class="sxs-lookup"><span data-stu-id="664a4-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="664a4-139">Jei norite taikyti apribotą prieigą, vartotojus priskirkite tik vaidmeniui **Savikainos objekto valdiklis**.</span><span class="sxs-lookup"><span data-stu-id="664a4-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="664a4-140">Šie eilutės lygio saugos naujinimai įsigalioja nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="664a4-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="664a4-141">Paveikti vartotojai turi atnaujinti savo naršykles.</span><span class="sxs-lookup"><span data-stu-id="664a4-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="664a4-142">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="664a4-142">Additional resources</span></span>
<span data-ttu-id="664a4-143">Norėdami daugiau sužinoti apie „Power BI“ eilutės lygio saugą žr. [Saugos valdymas savo modelyje „Power BI“](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="664a4-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
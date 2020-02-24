---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2020 m. sausio 7 d.)
description: Šiame straipsnyje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974435"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="7cf61-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2020 m. sausio 7 d.)</span><span class="sxs-lookup"><span data-stu-id="7cf61-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="7cf61-104">Šiame straipsnyje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="7cf61-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="7cf61-105">„Attract“ pakeitimai</span><span class="sxs-lookup"><span data-stu-id="7cf61-105">Changes in Attract</span></span>

<span data-ttu-id="7cf61-106">Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.</span><span class="sxs-lookup"><span data-stu-id="7cf61-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="7cf61-107">Supažindinimo pakeitimai</span><span class="sxs-lookup"><span data-stu-id="7cf61-107">Changes in Onboard</span></span>

<span data-ttu-id="7cf61-108">Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.</span><span class="sxs-lookup"><span data-stu-id="7cf61-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="7cf61-109">„Core HR“ pakeitimai</span><span class="sxs-lookup"><span data-stu-id="7cf61-109">Changes in Core HR</span></span>

<span data-ttu-id="7cf61-110">Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2697 komponavimo versijai.</span><span class="sxs-lookup"><span data-stu-id="7cf61-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="7cf61-111">Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="7cf61-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="7cf61-112">Negalima panaikinti darbininkų, kurie neturi įdarbinimo įrašų – (386157)</span><span class="sxs-lookup"><span data-stu-id="7cf61-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="7cf61-113">Šiuo keitimu į formą **Nedirbantys darbininkai** įtraukiama panaikinimo parinktis.</span><span class="sxs-lookup"><span data-stu-id="7cf61-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="7cf61-114">Darbininkai rodomi šioje formoje, kai nėra įrašų apie būsimą, aktyvų arba praeityje buvusį įdarbinimą.</span><span class="sxs-lookup"><span data-stu-id="7cf61-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="7cf61-115">Šiame leidime panaikinimo funkcija įjungta tik sistemos administratoriams.</span><span class="sxs-lookup"><span data-stu-id="7cf61-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="7cf61-116">Tačiau kitą savaitę pasirodysiančiame leidime bus atnaujintos saugos funkcijos, todėl visi vartotojai, kuriems priskiriamas personalo asistento vaidmuo, galės panaikinti nedirbančius darbininkus.</span><span class="sxs-lookup"><span data-stu-id="7cf61-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="7cf61-117">Šiuos keitimus taip pat galite atlikti neautomatiniu būdu, atlikdami tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7cf61-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="7cf61-118">Eikite į **Saugos konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="7cf61-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="7cf61-119">Skirtuke **Teisės** filtruokite sąrašą **Teisės**, kad būtų rodoma parinktis **Prižiūrėti darbininkus**.</span><span class="sxs-lookup"><span data-stu-id="7cf61-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="7cf61-120">Stulpelyje **Nuorodos** pasirinkite **Rodyti meniu elementus**.</span><span class="sxs-lookup"><span data-stu-id="7cf61-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="7cf61-121">**Rodyti meniu elementus** pasirinkite **HcmWOrkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="7cf61-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="7cf61-122">Prie funkcijos **Panaikinti** teisės pasirinkite „Suteikti”.</span><span class="sxs-lookup"><span data-stu-id="7cf61-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="7cf61-123">Pasirinkite skirtuką **Nepublikuoti objektai**.</span><span class="sxs-lookup"><span data-stu-id="7cf61-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="7cf61-124">Pasirinkite **Publikuoti viską**.</span><span class="sxs-lookup"><span data-stu-id="7cf61-124">Select **Publish all**.</span></span>

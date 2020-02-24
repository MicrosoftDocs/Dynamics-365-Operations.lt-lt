---
title: Funkcijų valdymas
description: Šioje temoje aprašoma, kaip administratorius gali įjungti „Microsoft Dynamics 365 Talent“ peržiūros funkcijas, taip pat pateikiamos funkcijos, kurios šiuo metu įgalintos peržiūroje.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006435"
---
# <a name="manage-features"></a><span data-ttu-id="5d2bb-103">Funkcijų valdymas</span><span class="sxs-lookup"><span data-stu-id="5d2bb-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5d2bb-104">Mūsų nuolatinis žmogiškųjų išteklių kapitalo valdymo (HCM) galimybių, skirtų „Microsoft Dynamics 365 Human Resources“, išleidimas apima norą leisti vartotojams kuo greičiau išbandyti naujas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="5d2bb-105">Administratoriai gali matyti ir naudoti peržiūros funkcijas savo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="5d2bb-106">Šios funkcijos yra beveik paruoštos bendrajam prieinamumui ir jau atlikta daug bandymų.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="5d2bb-107">Mes tiesiog laukiame galutinio klientų atsiliepimų etapo ir tikrinimo prieš jas bendrai išleisdami.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="5d2bb-108">Šioje temoje aprašoma, kaip galima įgalinti peržiūros funkcijas, taip pat pateikiamos funkcijos, kurias šiuo metu galima naudoti peržiūroje.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="5d2bb-109">Šis sąrašas bus atnaujintas išleidus funkcijas bendrajam prieinamumui ir kai bus išleista naujų peržiūros funkcijų.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="5d2bb-110">Pranešimas nepateikiamas, kai išleidžiamos naujos peržiūros funkcijos.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="5d2bb-111">Vartotojai tiesiog jau galės matyti šias funkcijas.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-111">Users will just start to see the features.</span></span> <span data-ttu-id="5d2bb-112">Daugiau informacijos apie naujas „Talent“ funkcijas žr. [Kas nauja arba pakeista programoje „Dynamics 365 Talent“](./whats-new.md)ir [„Dynamics 365“ ir „Power Platform“ leidimo pastabos](https://docs.microsoft.com/business-applications-release-notes).</span><span class="sxs-lookup"><span data-stu-id="5d2bb-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="5d2bb-113">Peržiūros funkcijų įjungimas arba išjungimas</span><span class="sxs-lookup"><span data-stu-id="5d2bb-113">Enable or disable preview features</span></span>

<span data-ttu-id="5d2bb-114">Norėdami pasiekti peržiūros funkcijas, pirmiausia turite jas įjungti savo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="5d2bb-115">Peržiūros funkcijų įjungimas arba išjungimas priklauso nuo aplinkos.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d2bb-116">Įjungę nustatymą **Peržiūros funkcijos**, peržiūros funkcijas įjungsite visiems jūsų organizacijoje dirbantiems vartotojams, esantiems šioje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="5d2bb-117">Išjungę šį parametrą, peržiūros funkcijas išjungsite ir jos taps nepasiekiamos jūsų vartotojams.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="5d2bb-118">Peržiūros funkcijos programoje „Talent“ turi ribotą palaikymą.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="5d2bb-119">Galima naudoti mažiau privatumo ir saugos priemonių, jos nėra įtrauktos į „Talent“ teikiamų paslaugų sutartį (SLA).</span><span class="sxs-lookup"><span data-stu-id="5d2bb-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="5d2bb-120">Asmens duomenims (t. y., bet kokiai informacijai, kuri galėtų jus identifikuoti) arba kitiems duomenims, kuriems yra taikomi teisiniai ar atitikties reikalavimai, apdoroti nenaudokite peržiūros funkcijų.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="5d2bb-121">„Attract“</span><span class="sxs-lookup"><span data-stu-id="5d2bb-121">Attract</span></span>

1. <span data-ttu-id="5d2bb-122">Prisijunkite prie „Microsoft Dynamics 365 Talent: Attract“.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="5d2bb-123">Meniu **Sąranka** (krumpliaračio simbolis) viršutiniame dešiniajame kampe pasirinkite **Administravimo centras**.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="5d2bb-124">Skirtuke **Funkcijų valdymas** pasirinkite šalia **Peržiūros funkcijos** esančią parinktį, kad ji būtų pažymėta mėlynai ir būtų **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Peržiūros funkcijų įjungimas programoje „Attract“](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="5d2bb-126">Pažymėkite arba atšaukite atskirų peržiūros funkcijų žymėjimą.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="5d2bb-127">Jei nedarysite nieko, bus įjungtos visos galimos peržiūros funkcijos.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="5d2bb-128">Atnaujinkite naršyklę, kad galėtumėte matyti naujas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="5d2bb-129">Vartotojai, kurie jau yra prisijungę, funkcijas matys prisijungę kitą kartą, arba jie gali atnaujinti savo naršyklę, kad funkcijas pamatytų nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="5d2bb-130">Kai kurias peržiūros funkcijas gali reikėti papildomai konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="5d2bb-131">Norėdami baigti sąranką, vadovaukitės greta peržiūros funkcijos pateiktais saitais.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="5d2bb-132">Grižt. ryšys</span><span class="sxs-lookup"><span data-stu-id="5d2bb-132">Feedback</span></span>

<span data-ttu-id="5d2bb-133">Norime sužinoti jūsų nuomonę apie jūsų įspūdžius naudojant šias peržiūras funkcijas.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="5d2bb-134">Naudojant šias arba bet kurias kitas funkcijas, skatiname reguliariai registruoti savo atsiliepimus toliau nurodytose svetainėse.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="5d2bb-135">[Bendruomenė](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – ši svetainė yra puikus šaltinis, kuriame vartotojai gali diskutuoti, naudoti atvejus, užduoti klausimų ir gauti bendruomenės pagalbos.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="5d2bb-136">Praneškite mums apie funkcijas, kurias norite matyti produkte, arba praneškite apie esamų funkcijų pakeitimus, kurie, jūsų manymu, turi būti atlikti.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="5d2bb-137">Naujas idėjas siūlykite toliau nurodytose svetainėse.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="5d2bb-138">„Attract“ idėjos</span><span class="sxs-lookup"><span data-stu-id="5d2bb-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="5d2bb-139">„Onboard“ idėjos</span><span class="sxs-lookup"><span data-stu-id="5d2bb-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="5d2bb-140">Įsitikinkite, kad neįtraukėte asmeninių duomenų (bet kokios informacijos, kuri gali jus identifikuoti) į savo atsiliepimą ar produkto peržiūros pateikimus.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="5d2bb-141">Surinkta informacija gali būti analizuojama toliau, ji nebus naudojama atsakyti į užklausas pagal taikomus privatumo įstatymus.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="5d2bb-142">Atskirai surinktiems asmeniniams duomenims pagal šias programas taikomos [„Microsoft“ privatumo nuostatos](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="5d2bb-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="5d2bb-143">Pasižymėkite šią temą ir dažnai prie jos grįžkite, kad sužinotumėte apie naujas peržiūros funkcijas, kai jas išleisime.</span><span class="sxs-lookup"><span data-stu-id="5d2bb-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d2bb-144">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="5d2bb-144">See also</span></span>

- [<span data-ttu-id="5d2bb-145">Išbandykite arba įsigykite „Talent“ programas</span><span class="sxs-lookup"><span data-stu-id="5d2bb-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="5d2bb-146">Kas nauja arba pasikeitė „Dynamics 365 Talent“</span><span class="sxs-lookup"><span data-stu-id="5d2bb-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="5d2bb-147">Leidimo planai</span><span class="sxs-lookup"><span data-stu-id="5d2bb-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="5d2bb-148">Palaikymo dėl „Microsoft Dynamics 365 Talent“ gavimas</span><span class="sxs-lookup"><span data-stu-id="5d2bb-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)

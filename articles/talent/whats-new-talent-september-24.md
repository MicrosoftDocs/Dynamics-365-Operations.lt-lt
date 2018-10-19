---
title: "Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. rugsėjo 24 d.)"
description: "Šioje temoje aprašomos naujos ir pakeistos šio „Microsoft Dynamics 365 for Talent“ „Core HR“ funkcijos."
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 94950fbe5c1aad3dfbd3de59d1bcb47337ff68ea
ms.openlocfilehash: aeb75fe4c775b9003c6429de536498f495224098
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-24-2018"></a><span data-ttu-id="294dc-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. rugsėjo 24 d.)</span><span class="sxs-lookup"><span data-stu-id="294dc-103">What's new or changed in Dynamics 365 for Talent Core HR (September 24, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="294dc-104">**8.1.1015.0 versija**</span><span class="sxs-lookup"><span data-stu-id="294dc-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="294dc-105">Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="294dc-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="294dc-106">Valiuta įtraukta į išmokas</span><span class="sxs-lookup"><span data-stu-id="294dc-106">Currency added to Benefits</span></span>

<span data-ttu-id="294dc-107">Išmokų planai atnaujinti – įtraukta išmokos valiuta.</span><span class="sxs-lookup"><span data-stu-id="294dc-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="294dc-108">Šis naujas laukas taip pat pateikiamas užregistruotose darbininkų išmokose.</span><span class="sxs-lookup"><span data-stu-id="294dc-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="294dc-109">Šis naujas laukas yra saugos teisės funkcijų Tvarkyti išmokas ir Peržiūrėti išmokų sąrašą dalis.</span><span class="sxs-lookup"><span data-stu-id="294dc-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="294dc-110">Proporcingo paskirstymo procento naujinimas – atostogos ir neatvykimai</span><span class="sxs-lookup"><span data-stu-id="294dc-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="294dc-111">Organizacijos paskirsto nedarbo laiką skirtingai pagal tai, kada darbuotojai prisijungia prie įmonės arba iš jos išeina.</span><span class="sxs-lookup"><span data-stu-id="294dc-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="294dc-112">Kai darbuotojai palieka organizaciją, kai kuriems gali reikėti nutraukti premijas atleidimo datą, o kitų kaupimo procesas sustabdomas paskutinę darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="294dc-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="294dc-113">Šie pakeitimai įmonėms suteikia galimybę pasirinkti, kada atleidimo proceso metu nutraukti registraciją.</span><span class="sxs-lookup"><span data-stu-id="294dc-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="294dc-114">Šios naujos galimybės teisių Atleisti darbininką ir Atleisti darbininką iš vadovo savitarnos dalis.</span><span class="sxs-lookup"><span data-stu-id="294dc-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="294dc-115">Kiti pakeitimai</span><span class="sxs-lookup"><span data-stu-id="294dc-115">Other changes</span></span>

<span data-ttu-id="294dc-116">Šiame leidime įtraukti keli papildomi klaidų ištaisymai.</span><span class="sxs-lookup"><span data-stu-id="294dc-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="294dc-117">Žinoma problema</span><span class="sxs-lookup"><span data-stu-id="294dc-117">Known Issue</span></span>

-   <span data-ttu-id="294dc-118">**Problema:** pridedant naują priedą prie darbininko, mygtukai **Naujas** ir **Redaguoti** yra pateikiami pilka spalva. **Problemos sprendimas:** prieš atidarydami priedo puslapį įsitikinkite, kad FactBoxes laukai puslapyje **Darbininkas** yra uždaryti.</span><span class="sxs-lookup"><span data-stu-id="294dc-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="294dc-119">Jei FactBoxes laukai yra uždaryti, kai įkeliamas puslapis **Darbininkas**, priedų mygtukus bus galima naudoti.</span><span class="sxs-lookup"><span data-stu-id="294dc-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="294dc-120">(Ši problema bus pašalinta kitame platformos naujinime.)</span><span class="sxs-lookup"><span data-stu-id="294dc-120">(This issue will be fixed in the next platform update.)</span></span>


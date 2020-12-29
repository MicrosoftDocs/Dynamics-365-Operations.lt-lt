---
title: Konfigūruoti priedų valdymo parametrus įmonei
description: Konfigūruoti priedų valdymo parametrus įmonei „Microsoft Dynamics 365 Human Resources“.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692750"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="3e12f-103">Konfigūruoti priedų valdymo parametrus įmonei</span><span class="sxs-lookup"><span data-stu-id="3e12f-103">Configure Benefits management parameters per company</span></span>

<span data-ttu-id="3e12f-104">Kiekvienai organizacijai, kuri siūlo priedus, turite sukonfigūruoti nustatymus skirtus priedų patvirtinimo el. laiškams.</span><span class="sxs-lookup"><span data-stu-id="3e12f-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="3e12f-105">Konfigūruoti patvirtinimo el. laiškų nustatymus</span><span class="sxs-lookup"><span data-stu-id="3e12f-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="3e12f-106">**Išmokų valdymo** darbo srityje, **Nustatymo** skyriuje, pasirinkite **Žmogiškųjų išteklių pasidalyti parametrai**.</span><span class="sxs-lookup"><span data-stu-id="3e12f-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="3e12f-107">Skirtuke **Išmokų valdymas** įveskite toliau pateiktų laukų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="3e12f-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="3e12f-108">Laukas</span><span class="sxs-lookup"><span data-stu-id="3e12f-108">Field</span></span> | <span data-ttu-id="3e12f-109">aprašymas</span><span class="sxs-lookup"><span data-stu-id="3e12f-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3e12f-110">**Siųsto patvirtinimo el. laišką**</span><span class="sxs-lookup"><span data-stu-id="3e12f-110">**Send confirmation email**</span></span> | <span data-ttu-id="3e12f-111">Įjungus šią funkciją, patvirtinimo el. laiškas bus nusiųstas darbuotojams, kai jie išsiregistruos iš naudų įtraukimo patirties darbuotojo savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="3e12f-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="3e12f-112">**Patvirtinimo el. laiško šablonas**</span><span class="sxs-lookup"><span data-stu-id="3e12f-112">**Confirmation email template**</span></span> | <span data-ttu-id="3e12f-113">Pasirinkite organizacijos el. laiško šabloną, kuris bus naudojamas siunčiant įsitraukimo patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="3e12f-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="3e12f-114">Jei nepsirinksite šablono, tolesnis bendras el. laiškas bus nusiųstas:</span><span class="sxs-lookup"><span data-stu-id="3e12f-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="3e12f-115">%Darbuotojovardas%,</span><span class="sxs-lookup"><span data-stu-id="3e12f-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="3e12f-116">Sveikiname!</span><span class="sxs-lookup"><span data-stu-id="3e12f-116">Congratulations!</span></span> <span data-ttu-id="3e12f-117">Sėkmingai užbaigėte priedų įtraukimą.</span><span class="sxs-lookup"><span data-stu-id="3e12f-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="3e12f-118">Dėkojame,</span><span class="sxs-lookup"><span data-stu-id="3e12f-118">Thank you,</span></span><br><span data-ttu-id="3e12f-119"><Įmonės/Organizacijos pavadinimas> Priedai.</span><span class="sxs-lookup"><span data-stu-id="3e12f-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="3e12f-120">**Numatytojo el. pašto siuntėjo adresas**</span><span class="sxs-lookup"><span data-stu-id="3e12f-120">**Default email sender address**</span></span> | <span data-ttu-id="3e12f-121">El. pašto adresas naudojamas siunčiant patvirtinimo el. laišką.</span><span class="sxs-lookup"><span data-stu-id="3e12f-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="3e12f-122">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3e12f-122">Select **Save**.</span></span>
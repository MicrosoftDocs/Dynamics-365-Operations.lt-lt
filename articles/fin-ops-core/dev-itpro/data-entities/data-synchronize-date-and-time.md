---
title: Datos ir laiko sinchronizavimas importavimo užduotyse
description: Naudokite UTC laiko juostas importavimo užduotyse tam, kad išvengtumėte problemų, susijusių su laiko juostų konvertavimu.
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748674"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="2ef32-103">Datos ir laiko sinchronizavimas importavimo užduotyse</span><span class="sxs-lookup"><span data-stu-id="2ef32-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ef32-104">Svarbu nustatyti jūsų importavimo užduoties laiko juostą kaip Universaliojo laiko (UTC).</span><span class="sxs-lookup"><span data-stu-id="2ef32-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="2ef32-105">Jei naudojate kitą parametrą, jūsų importuotuose duomenyse galite matyti netikėtas datas ir laikus.</span><span class="sxs-lookup"><span data-stu-id="2ef32-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="2ef32-106">Be tinkamo parametro, importavimo procese UTC formato data konvertuojama į vietinį formatą, o tada sistemos parametrai konvertuoja ją dar kartą.</span><span class="sxs-lookup"><span data-stu-id="2ef32-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="2ef32-107">Dėl šio dvigubo konvertavimo, datos gali pasikeisti tarp programų.</span><span class="sxs-lookup"><span data-stu-id="2ef32-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="2ef32-108">Pavyzdžiui, dėl dvigubo konvertavimo darbuotojo darbo pradžios data gali skirtis tarp „Dynamics 365 Human Resources” ir „Dynamics 365 Finance”, kadangi egzistuoja skirtumai tarp vietinio laiko zonų.</span><span class="sxs-lookup"><span data-stu-id="2ef32-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="2ef32-109">Importavimo užduoties nustatymas į UTC laiko zoną išsprendžia šią problemą.</span><span class="sxs-lookup"><span data-stu-id="2ef32-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="2ef32-110">„Dynamics 365 Finance and Operations” pasirinkit **Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="2ef32-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="2ef32-111">Pasirinkite **Importuoti projektus**, o tada pasirinkite projektą.</span><span class="sxs-lookup"><span data-stu-id="2ef32-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="2ef32-112">Dalyje **Šaltinio datos formatas** pasirinkite **„CSV-Unicode”**.</span><span class="sxs-lookup"><span data-stu-id="2ef32-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="2ef32-113">[![Šaltinio datos formatą pakeitimas į UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="2ef32-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="2ef32-114">Pakeiskite **Laiko zoną** į **Universaliojo laiko zoną** ir pakeiskite **Kalbą** į **„En-US”**.</span><span class="sxs-lookup"><span data-stu-id="2ef32-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
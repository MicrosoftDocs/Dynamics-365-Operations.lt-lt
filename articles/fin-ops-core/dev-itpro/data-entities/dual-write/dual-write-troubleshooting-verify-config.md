---
title: Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Common Data Service”
description: Šioje temoje paaiškinama, kaip galima nustatyti, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Common Data Service”.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997235"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="53b11-103">Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Common Data Service”</span><span class="sxs-lookup"><span data-stu-id="53b11-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="53b11-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="53b11-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="53b11-105">Tiksliau sakant, paaiškinama, kaip galima nustatyti, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="53b11-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="53b11-106">Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programoje</span><span class="sxs-lookup"><span data-stu-id="53b11-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="53b11-107">Norėdami nustatyti, ar klaidos, kurias matote bandydami įrašyti atnaujinimo įrašus, yra gaunamos iš dvigubo rašymo funkcijos, pirma patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="53b11-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="53b11-108">Jeigu turite administratoriaus teises „Finance and Operations” programoje, eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite plytelę **Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="53b11-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management** , and select the **Dual-write** tile.</span></span> <span data-ttu-id="53b11-109">Jeigu rodoma susietų aplinkų informacija ir vykdomų objektų schemų sąrašas, dvigubo rašymo funkcija yra sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="53b11-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![„Finance and Operations” programos ryšio tikrinimas, kai turite administratoriaus teises](media/verify_fin_ops_1.png)

+ <span data-ttu-id="53b11-111">Jei neturite administratoriaus teisių, gausite klaidos pranešimą *Nepavyksta įrašyti duomenų į objektą \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="53b11-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="53b11-112">Tolesnėje iliustracijoje pateiktame pavyzdyje parodyta, kad nepavyksta sukurti kliento įrašo „Finance and Operations” programoje, nes dvigubo rašymo funkcija yra sukonfigūruota, bet klientų grupė ir mokėjimo terminų nuorodos duomenų nėra „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="53b11-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![„Finance and Operations” programos ryšio tikrinimas, kai neturite administratoriaus teisių](media/verify_fin_ops_2.png)

<span data-ttu-id="53b11-114">Informacijos apie tai, kaip spręsti problemas, kai kuriate duomenis „Finance and Operations” programose, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="53b11-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="53b11-115">Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="53b11-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="53b11-116">Jei kurdami duomenis, matote lauką **Įmonė** „Common Data Service” puslapiuose, dvigubo rašymo funkcija yra sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="53b11-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![„Common Data Service” ryšio tikrinimas](media/verify_cds.png)

<span data-ttu-id="53b11-118">Informacijos apie tai, kaip spręsti problemas, kai kuriate duomenis „Common Data Service”, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="53b11-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="53b11-119">Informacijos apie tai, kaip peržiūrėti klaidos informaciją, jei susiduriate su klaidomis, kurdami duomenis „Common Data Service”, žr. [Priedo sekimo žurnalo „Common Data Service“ įgalinimas ir peržiūra, siekiant peržiūrėti klaidos informaciją](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span><span class="sxs-lookup"><span data-stu-id="53b11-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>

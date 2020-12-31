---
title: Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Dataverse”
description: Šioje temoje paaiškinama, kaip galima nustatyti, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Dataverse”.
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
ms.openlocfilehash: f389bcf133cc7e6a086167d5e26c1b8795d0fa30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685544"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="24cd2-103">Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Dataverse”</span><span class="sxs-lookup"><span data-stu-id="24cd2-103">Verify that dual-write is configured in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="24cd2-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Dataverse“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="24cd2-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="24cd2-105">Tiksliau sakant, paaiškinama, kaip galima nustatyti, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="24cd2-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="24cd2-106">Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programoje</span><span class="sxs-lookup"><span data-stu-id="24cd2-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="24cd2-107">Norėdami nustatyti, ar klaidos, kurias matote bandydami įrašyti atnaujinimo eilutes, yra gaunamos iš dvigubo rašymo funkcijos, pirma patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="24cd2-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="24cd2-108">Jeigu turite administratoriaus teises „Finance and Operations” programoje, eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite plytelę **Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="24cd2-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="24cd2-109">Jeigu rodoma susietų aplinkų informacija ir vykdomų eilučių schemų sąrašas, dvigubo rašymo funkcija yra sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="24cd2-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![„Finance and Operations” programos ryšio tikrinimas, kai turite administratoriaus teises](media/verify_fin_ops_1.png)

+ <span data-ttu-id="24cd2-111">Jei neturite administratoriaus teisių, gausite klaidos pranešimą *Nepavyksta įrašyti duomenų į objektą \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="24cd2-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="24cd2-112">Tolesnėje iliustracijoje pateiktame pavyzdyje parodyta, kad nepavyksta sukurti kliento eilutės „Finance and Operations” programoje, nes dvigubo rašymo funkcija yra sukonfigūruota, bet klientų grupė ir mokėjimo terminų nuorodos duomenų nėra „Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="24cd2-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![„Finance and Operations” programos ryšio tikrinimas, kai neturite administratoriaus teisių](media/verify_fin_ops_2.png)

<span data-ttu-id="24cd2-114">Informacijos apie tai, kaip spręsti problemas, kai kuriate duomenis „Finance and Operations” programose, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="24cd2-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="24cd2-115">Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="24cd2-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="24cd2-116">Jei kurdami duomenis, matote lauką **Įmonė** „Dataverse” puslapiuose, dvigubo rašymo funkcija yra sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="24cd2-116">When you create data, if you see the **Company** field on pages in Dataverse, dual-write is configured.</span></span>

![„Dataverse” ryšio tikrinimas](media/verify_cds.png)

<span data-ttu-id="24cd2-118">Informacijos apie tai, kaip spręsti problemas, kai kuriate duomenis „Dataverse”, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="24cd2-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="24cd2-119">Informacijos apie tai, kaip peržiūrėti klaidos informaciją, jei susiduriate su klaidomis, kurdami duomenis „Dataverse”, žr. [Priedo sekimo žurnalo „Dataverse“ įgalinimas ir peržiūra, siekiant peržiūrėti klaidos informaciją](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="24cd2-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>

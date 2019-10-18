---
title: Brūkšninių kodų nuskaitymas naudojant kamerą „Dynamics 365 Supply Chain Management“ – Sandėliavimo programa
description: Šioje temoje paaiškinama, kaip nustatyti „Dynamics 365 Supply Chain Management“ – Sandėliavimo programą, kad būtų galima nuskaityti brūkšninius kodus naudojant mobiliojo įrenginio kamerą.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8062a981f792bcfed2713d3cb6a42f414394f6a4
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251471"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a><span data-ttu-id="cd574-103">Brūkšninių kodų nuskaitymas naudojant kamerą „Dynamics 365 Supply Chain Management“ – Sandėliavimo programa</span><span class="sxs-lookup"><span data-stu-id="cd574-103">Scan bar codes using a camera in Dynamics 365 Supply Chain Management - Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd574-104">Šioje temoje paaiškinama, kaip nustatyti „Dynamics 365 Supply Chain Management“ – Sandėliavimo programą, kad būtų galima nuskaityti brūkšninius kodus naudojant mobiliojo įrenginio kamerą.</span><span class="sxs-lookup"><span data-stu-id="cd574-104">This topic explains how to set up Dynamics 365 Supply Chain Management - Warehousing app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="cd574-105">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="cd574-105">Prerequisites</span></span>
<span data-ttu-id="cd574-106">Norėdami naudoti šią funkciją, turite įsidiegti Sandėliavimo programos 1.2.0.0 versiją ir jūsų įrenginyje turi būti kamera.</span><span class="sxs-lookup"><span data-stu-id="cd574-106">To use this feature, you need to have version 1.2.0.0 of the Warehousing app installed, and your device must have a camera.</span></span> <span data-ttu-id="cd574-107">Atidarę programą po atnaujinimo, būsite paraginti leisti programai naudoti kamerą.</span><span class="sxs-lookup"><span data-stu-id="cd574-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="cd574-108">Jei įrenginyje kameros nėra, raginimas nebus rodomas ir negalėsite naudoti kameros kaip skaitytuvo.</span><span class="sxs-lookup"><span data-stu-id="cd574-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="cd574-109">Sąranka</span><span class="sxs-lookup"><span data-stu-id="cd574-109">Setup</span></span>
<span data-ttu-id="cd574-110">„Warehousing“ programos rodymo parametruose galite pasirinkti, ar leisti naudoti kamerą brūkšniniams kodams nuskaityti.</span><span class="sxs-lookup"><span data-stu-id="cd574-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="cd574-111">Jei įjungsite **Naudoti kamerą kaip skaitytuvą**, galėsite naudoti kamerą kiekviename įvesties lauke, kuriame kaip pageidaujamas įvesties režimas nustatytas **Nuskaitymas**.</span><span class="sxs-lookup"><span data-stu-id="cd574-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="cd574-112">Norėdami įvesties lauką nustatyti kaip nuskaitomą, puslapyje **Sandėlio programos laukų pavadinimai** nustatykite parametro **Pageidaujamas įvesties režimas** parinktį **Nuskaitymas**.</span><span class="sxs-lookup"><span data-stu-id="cd574-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="cd574-113">Pasirinkus šią pasirinktį, nuskaitymus „Warehouse“ programoje bus galima atlikti su kamera.</span><span class="sxs-lookup"><span data-stu-id="cd574-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="cd574-114">Norėdami gauti daugiau informacijos apie tai, kaip konfigūruoti laukų pavadinimus programoje „Warehousing“, žr. [Programos „Warehousing“ laukų pavadinimų konfigūravimas](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="cd574-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="cd574-115">Palaikomi brūkšninių kodų formatai</span><span class="sxs-lookup"><span data-stu-id="cd574-115">Supported bar code formats</span></span>
<span data-ttu-id="cd574-116">Palaikomi dažniausi brūkšninių kodų formatai, įskaitant kodą 128, kodą 39, kodą 93, EAN-8, EAN-13, UPC-E, UPC-A ir QR kodus.</span><span class="sxs-lookup"><span data-stu-id="cd574-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="cd574-117">Naršymas</span><span class="sxs-lookup"><span data-stu-id="cd574-117">Navigation</span></span>
<span data-ttu-id="cd574-118">Kameros puslapis bus paleistas kiekviename puslapyje, kurio įvesties lauke kaip pageidaujamas įvesties režimas bus nustatytas Nuskaitymas. Įjungę kameros puslapį, naršykite naudodami šiuos mygtukus:</span><span class="sxs-lookup"><span data-stu-id="cd574-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="cd574-119">Spustelėkite sugrįžimo mygtuką, jei norite grįžti į užduočių ir informacijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="cd574-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="cd574-120">Spustelėkite užduočių ir informacijos puslapyje esantį pieštuką, kad pereitumėte į puslapį, kuriame galėsite įvesti informaciją rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="cd574-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="cd574-121">Spustelėkite užduočių ir informacijos puslapyje esančią kamerą, jei norite grįžti į kameros puslapį.</span><span class="sxs-lookup"><span data-stu-id="cd574-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="cd574-122">Užduočių ir informacijos puslapis</span><span class="sxs-lookup"><span data-stu-id="cd574-122">Task and details page</span></span> | <span data-ttu-id="cd574-123">Kameros puslapis</span><span class="sxs-lookup"><span data-stu-id="cd574-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="cd574-126">Kameros puslapyje spustelėjus kameros mygtuką, jis bus rodomas blankesne spalva, kai bus bandoma identifikuoti brūkšninį kodą.</span><span class="sxs-lookup"><span data-stu-id="cd574-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="cd574-127">Jei per 5 sekundes brūkšninis kodas nebus identifikuotas, procesas bus sustabdytas ir vėl bus galima naudoti kameros mygtuką.</span><span class="sxs-lookup"><span data-stu-id="cd574-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="cd574-128">Tada galėsite bandyti nuskaityti brūkšninį kodą dar kartą.</span><span class="sxs-lookup"><span data-stu-id="cd574-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="cd574-129">Nukreipę kamerą brūkšninį kodą, laikykite brūkšninį kodą tarp rėmelių, kad būtų geriausias rezultatas.</span><span class="sxs-lookup"><span data-stu-id="cd574-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="cd574-130">Kai brūkšninis kodas nuskaitomas sėkmingai, bus apdorojamas rezultatas ir būsite nukreipti atlikti kitą veiksmą.</span><span class="sxs-lookup"><span data-stu-id="cd574-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="cd574-131">Jei kitame veiksme bus kitas įvesties laukas, kur kaip pageidaujamas įvesties režimas nustatytas Nuskaitymas, vėl bus atidarytas kameros puslapis.</span><span class="sxs-lookup"><span data-stu-id="cd574-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="cd574-132">Jei kitame veiksme nebus nuskaitymo lauko, tada kameros puslapis nebus atidarytas.</span><span class="sxs-lookup"><span data-stu-id="cd574-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>


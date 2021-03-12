---
title: Brūkšninių kodų nuskaitymas sandėlio programėle naudojant kamerą
description: Šioje temoje paaiškinama, kaip nustatyti „Warehousing“ programėlę brūkšninių kodų nuskaitymui naudojant mobiliojo įrenginio kamerą.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 71ec15b2568eefd8bea99e64c258a65461a7ad95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965647"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a><span data-ttu-id="be578-103">Brūkšninių kodų nuskaitymas sandėlio programėle naudojant kamerą</span><span class="sxs-lookup"><span data-stu-id="be578-103">Scan bar codes using a camera in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be578-104">Šioje temoje paaiškinama, kaip nustatyti „Warehousing“ programėlę brūkšninių kodų nuskaitymui naudojant mobiliojo įrenginio kamerą.</span><span class="sxs-lookup"><span data-stu-id="be578-104">This topic explains how to set up the warehouse app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="be578-105">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="be578-105">Prerequisites</span></span>
<span data-ttu-id="be578-106">Norėdami naudotis šia funkcija, Jūsų įrenginyje turi būti įdiegta „Warehousing“ programėlės 1.2.0.0 versija ir įrenginyje turi būti kamera.</span><span class="sxs-lookup"><span data-stu-id="be578-106">To use this feature, you need to have version 1.2.0.0 of the warehouse app installed, and your device must have a camera.</span></span> <span data-ttu-id="be578-107">Atidarę programą po atnaujinimo, būsite paraginti leisti programai naudoti kamerą.</span><span class="sxs-lookup"><span data-stu-id="be578-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="be578-108">Jei įrenginyje kameros nėra, raginimas nebus rodomas ir negalėsite naudoti kameros kaip skaitytuvo.</span><span class="sxs-lookup"><span data-stu-id="be578-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="be578-109">Sąranka</span><span class="sxs-lookup"><span data-stu-id="be578-109">Setup</span></span>
<span data-ttu-id="be578-110">„Warehousing“ programėlės Ekrano parametruose galite pasirinkti, ar leisti naudoti kamerą brūkšniniams kodams nuskaityti.</span><span class="sxs-lookup"><span data-stu-id="be578-110">In the Display settings of the warehouse application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="be578-111">Jei įjungsite **Naudoti kamerą kaip skaitytuvą**, galėsite naudoti kamerą kiekviename įvesties lauke, kuriame kaip pageidaujamas įvesties režimas nustatytas **Nuskaitymas**.</span><span class="sxs-lookup"><span data-stu-id="be578-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="be578-112">Norėdami įvesties lauką nustatyti kaip nuskaitomą, puslapyje **Sandėlio programos laukų pavadinimai** nustatykite parametro **Pageidaujamas įvesties režimas** parinktį **Nuskaitymas**.</span><span class="sxs-lookup"><span data-stu-id="be578-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="be578-113">Pasirinkus šią parinktį, „Warehousing“ programėlė naudos kamerą kodų nuskaitymui.</span><span class="sxs-lookup"><span data-stu-id="be578-113">When this option is selected, a camera can be used for scanning in the warehouse app.</span></span> <span data-ttu-id="be578-114">Daugiau informacijos apie tai, kaip konfigūruoti „Warehousing“ laukų pavadinimus, rasite [„Warehousing“ programėlės laukų pavadinimų konfigūravimas](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="be578-114">For information about how to configure app field names in Warehousing, see [Configure app field names in warehouse app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="be578-115">Palaikomi brūkšninių kodų formatai</span><span class="sxs-lookup"><span data-stu-id="be578-115">Supported bar code formats</span></span>
<span data-ttu-id="be578-116">Palaikomi dažniausi brūkšninių kodų formatai, įskaitant kodą 128, kodą 39, kodą 93, EAN-8, EAN-13, UPC-E, UPC-A ir QR kodus.</span><span class="sxs-lookup"><span data-stu-id="be578-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="be578-117">Naršymas</span><span class="sxs-lookup"><span data-stu-id="be578-117">Navigation</span></span>
<span data-ttu-id="be578-118">Kameros puslapis bus paleistas kiekviename puslapyje, kurio įvesties lauke kaip pageidaujamas įvesties režimas bus nustatytas Nuskaitymas. Įjungę kameros puslapį, naršykite naudodami šiuos mygtukus:</span><span class="sxs-lookup"><span data-stu-id="be578-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="be578-119">Spustelėkite sugrįžimo mygtuką, jei norite grįžti į užduočių ir informacijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="be578-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="be578-120">Spustelėkite užduočių ir informacijos puslapyje esantį pieštuką, kad pereitumėte į puslapį, kuriame galėsite įvesti informaciją rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="be578-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="be578-121">Spustelėkite užduočių ir informacijos puslapyje esančią kamerą, jei norite grįžti į kameros puslapį.</span><span class="sxs-lookup"><span data-stu-id="be578-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="be578-122">Užduočių ir informacijos puslapis</span><span class="sxs-lookup"><span data-stu-id="be578-122">Task and details page</span></span> | <span data-ttu-id="be578-123">Kameros puslapis</span><span class="sxs-lookup"><span data-stu-id="be578-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![Kameros nuskaitymo užduočių informacijos puslapio pavyzdys](./media/camera-scanning-example-task-detail-page50.png)          | ![Kameros nuskaitymo kameros mažesnio puslapio pavyzdys](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="be578-126">Kameros puslapyje spustelėjus kameros mygtuką, jis bus rodomas blankesne spalva, kai bus bandoma identifikuoti brūkšninį kodą.</span><span class="sxs-lookup"><span data-stu-id="be578-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="be578-127">Jei per 5 sekundes brūkšninis kodas nebus identifikuotas, procesas bus sustabdytas ir vėl bus galima naudoti kameros mygtuką.</span><span class="sxs-lookup"><span data-stu-id="be578-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="be578-128">Tada galėsite bandyti nuskaityti brūkšninį kodą dar kartą.</span><span class="sxs-lookup"><span data-stu-id="be578-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="be578-129">Nukreipę kamerą brūkšninį kodą, laikykite brūkšninį kodą tarp rėmelių, kad būtų geriausias rezultatas.</span><span class="sxs-lookup"><span data-stu-id="be578-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="be578-130">Kai brūkšninis kodas nuskaitomas sėkmingai, bus apdorojamas rezultatas ir būsite nukreipti atlikti kitą veiksmą.</span><span class="sxs-lookup"><span data-stu-id="be578-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="be578-131">Jei kitame veiksme bus kitas įvesties laukas, kur kaip pageidaujamas įvesties režimas nustatytas Nuskaitymas, vėl bus atidarytas kameros puslapis.</span><span class="sxs-lookup"><span data-stu-id="be578-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="be578-132">Jei kitame veiksme nebus nuskaitymo lauko, tada kameros puslapis nebus atidarytas.</span><span class="sxs-lookup"><span data-stu-id="be578-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>


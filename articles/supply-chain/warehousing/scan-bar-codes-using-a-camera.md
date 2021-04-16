---
title: Brūkšninių kodų nuskaitymas sandėlio valdymo mobiliųjų įrenginių programėle naudojant kamerą
description: Šioje temoje paaiškinama, kaip nustatyti sandėlio valdymo mobiliųjų įrenginių programėlę brūkšninių kodų nuskaitymui naudojant mobiliojo įrenginio kamerą.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831223"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="4b286-103">Brūkšninių kodų nuskaitymas sandėlio valdymo mobiliųjų įrenginių programėle naudojant kamerą</span><span class="sxs-lookup"><span data-stu-id="4b286-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b286-104">Šioje temoje paaiškinama, kaip nustatyti sandėlio valdymo mobiliųjų įrenginių programėlę brūkšninių kodų nuskaitymui naudojant mobiliojo įrenginio kamerą.</span><span class="sxs-lookup"><span data-stu-id="4b286-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="4b286-105">Sąranka</span><span class="sxs-lookup"><span data-stu-id="4b286-105">Setup</span></span>

<span data-ttu-id="4b286-106">Sandėlio valdymo mobiliųjų įrenginių programėlės rodymo parametruose galite pasirinkti, ar leisti naudoti kamerą brūkšniniams kodams nuskaityti.</span><span class="sxs-lookup"><span data-stu-id="4b286-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="4b286-107">Jei įjungsite **Naudoti kamerą kaip skaitytuvą**, galėsite naudoti kamerą kiekviename įvesties lauke, kuriame kaip pageidaujamas įvesties režimas nustatytas **Nuskaitymas**.</span><span class="sxs-lookup"><span data-stu-id="4b286-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="4b286-108">Norėdami įvesties lauką nustatyti kaip nuskaitomą, puslapyje **Sandėlio programos laukų pavadinimai** nustatykite parametro **Pageidaujamas įvesties režimas** parinktį **Nuskaitymas**.</span><span class="sxs-lookup"><span data-stu-id="4b286-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="4b286-109">Pasirinkus šią parinktį, sandėlio valdymo mobiliųjų įrenginių programėlė naudos kamerą kodų nuskaitymui.</span><span class="sxs-lookup"><span data-stu-id="4b286-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="4b286-110">Daugiau informacijos rasite [Sandėlio valdymo mobiliųjų įrenginių programėlės laukų konfigūravimas](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="4b286-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="4b286-111">Palaikomi brūkšninių kodų formatai</span><span class="sxs-lookup"><span data-stu-id="4b286-111">Supported bar code formats</span></span>

<span data-ttu-id="4b286-112">Palaikomi dažniausi brūkšninių kodų formatai, įskaitant kodą 128, kodą 39, kodą 93, EAN-8, EAN-13, UPC-E, UPC-A ir QR kodus.</span><span class="sxs-lookup"><span data-stu-id="4b286-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="4b286-113">Naršymas</span><span class="sxs-lookup"><span data-stu-id="4b286-113">Navigation</span></span>

<span data-ttu-id="4b286-114">Kameros puslapis bus paleistas kiekviename puslapyje, kurio įvesties lauko **Pageidaujamas įvesties režimas** yra nustatytas *Nuskaitymas*, kai būsite kameros puslapyje, naršymui naudokite šias parinktis:</span><span class="sxs-lookup"><span data-stu-id="4b286-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="4b286-115">Pasirinkite sugrįžimo mygtuką, jei norite grįžti į **Užduočių ir išsamios informacijos** puslapį.</span><span class="sxs-lookup"><span data-stu-id="4b286-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="4b286-116">Pasirinkite **Užduočių ir išsamios informacijos** puslapyje esantį pieštuką, jei norite pereiti į puslapį, kuriame galėsite įvesti informaciją rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="4b286-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="4b286-117">Pasirinkite **Užduočių ir informacijos** puslapyje esančią kamerą, jei norite sugrįžti į kameros puslapį.</span><span class="sxs-lookup"><span data-stu-id="4b286-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="4b286-118">Kameros puslapyje pasirinkus kameros mygtuką, jis bus rodomas blankesne spalva, kai bus bandoma identifikuoti brūkšninį kodą.</span><span class="sxs-lookup"><span data-stu-id="4b286-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="4b286-119">Jeigu per 5 sekundes brūkšninis kodas nebus identifikuotas, procesas bus sustabdytas ir vėl bus galima naudoti kameros mygtuką.</span><span class="sxs-lookup"><span data-stu-id="4b286-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="4b286-120">Tada galėsite bandyti nuskaityti brūkšninį kodą dar kartą.</span><span class="sxs-lookup"><span data-stu-id="4b286-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="4b286-121">Nukreipę kamerą brūkšninį kodą, laikykite brūkšninį kodą tarp rėmelių, kad būtų geriausias rezultatas.</span><span class="sxs-lookup"><span data-stu-id="4b286-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="4b286-122">Kai brūkšninis kodas nuskaitomas sėkmingai, bus apdorojamas rezultatas ir būsite nukreipti atlikti kitą veiksmą.</span><span class="sxs-lookup"><span data-stu-id="4b286-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="4b286-123">Jei kitame veiksme bus kitas įvesties laukas, kur kaip pageidaujamas įvesties režimas nustatytas Nuskaitymas, vėl bus atidarytas kameros puslapis.</span><span class="sxs-lookup"><span data-stu-id="4b286-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="4b286-124">Jei kitame veiksme nebus nuskaitymo lauko, tada kameros puslapis nebus atidarytas.</span><span class="sxs-lookup"><span data-stu-id="4b286-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
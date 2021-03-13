---
title: Elektroninių ataskaitų formatų modifikavimas iš naujo pritaikant „Excel“ šablonus
description: Šioje temoje aprašoma, kaip modifikuoti elektroninių ataskaitų (ER) formatą, naudojamą verslo dokumentams generuoti, iš naujo pritaikant modifikuotą „Excel“ šabloną.
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d828412e0d804acf6e6141778512e899bc78a7d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092849"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a><span data-ttu-id="5f70b-103">Elektroninių ataskaitų formatų modifikavimas iš naujo pritaikant „Excel‟ šablonus</span><span class="sxs-lookup"><span data-stu-id="5f70b-103">Modify Electronic reporting formats by reapplying Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f70b-104">Elektroninės ataskaitos (ER) įrankis naudojamas verslo dokumentams elektroniniu formatu generuoti.</span><span class="sxs-lookup"><span data-stu-id="5f70b-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="5f70b-105">Norėdami sugeneruoti verslo dokumentą, turite sukurti ER formatą ir, naudodami ER kūrimo priemonę, apibrėžti verslo dokumento maketą bei nurodyti duomenis, kurie turi būti į jį įtraukti.</span><span class="sxs-lookup"><span data-stu-id="5f70b-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="5f70b-106">Tada galite paleisti ER formatą ir sugeneruoti verslo dokumentą.</span><span class="sxs-lookup"><span data-stu-id="5f70b-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="5f70b-107">ER įrankį galima naudoti verslo dokumentams kaip „Microsoft Excel“ failams generuoti.</span><span class="sxs-lookup"><span data-stu-id="5f70b-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="5f70b-108">Kaip šių dokumentų šabloną galite naudoti „Excel“ dokumentą.</span><span class="sxs-lookup"><span data-stu-id="5f70b-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="5f70b-109">Norėdami nurodyti dokumento maketą ER kūrimo priemonėje, kaip šablonas norimo naudoti „Excel“ dokumento turinį galite importuoti į nurodytą ER formatą.</span><span class="sxs-lookup"><span data-stu-id="5f70b-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="5f70b-110">Jei norite gauti daugiau informacijos ir išbandyti šį scenarijų, paleiskite užduočių vedlį **ER konfigūracijos, skirtos generuoti ataskaitas OPENXML formatu, kūrimas** (verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų / sprendimų komponentų (10677) dalis).</span><span class="sxs-lookup"><span data-stu-id="5f70b-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="5f70b-111">Jei redaguosite kaip verslo dokumento šabloną naudojamą „Excel“ dokumentą, nauja ER funkcija leis iš naujo pritaikyti atnaujintą ER formato šabloną.</span><span class="sxs-lookup"><span data-stu-id="5f70b-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="5f70b-112">Tada ER formatas bus atnaujintas, kad atitiktų atnaujintą šabloną.</span><span class="sxs-lookup"><span data-stu-id="5f70b-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="5f70b-113">Jei norite gauti daugiau informacijos apie šią funkciją, paleiskite užduočių vedlį **ER formato modifikavimas iš naujo pritaikant „Excel‟ šabloną** (verslo proceso 7.5.5.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10683) dalis).</span><span class="sxs-lookup"><span data-stu-id="5f70b-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="5f70b-114">Vykdydami užduočių vedlio veiksmą, kurio metu importuojate atnaujintą šabloną, kaip šabloną naudokite modifikuotą „Excel“ failo Mokėjimo ataskaita, SampleVendPaymWsReport2, šabloną.</span><span class="sxs-lookup"><span data-stu-id="5f70b-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>

---
title: Elektroninių dokumentų generavimas ir prašymų duomenų naujinimas naudojant ER
description: Galite kurti elektroninių ataskaitų (ER) formatus, kuriuos galima naudoti programoje norint generuoti siunčiamus elektroninius dokumentus.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ae3405a882ac37fd9758d8ff0902896562fa06b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093878"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="18e0a-103">Elektroninių dokumentų generavimas ir prašymų duomenų naujinimas naudojant ER</span><span class="sxs-lookup"><span data-stu-id="18e0a-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18e0a-104">Galite kurti elektroninių ataskaitų (ER) formatus, kuriuos galima naudoti programoje norint generuoti siunčiamus elektroninius dokumentus.</span><span class="sxs-lookup"><span data-stu-id="18e0a-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="18e0a-105">Taip pat galite kurti ER formatus, kurie analizuoja gaunamus elektroninius dokumentus ir naudoja šių dokumentų turinį programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="18e0a-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="18e0a-106">Naudojant šią funkciją, vieną ER formatą galima naudoti siunčiamiems elektroniniams dokumentams generuoti ir tada programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="18e0a-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="18e0a-107">Šią funkciją galima naudoti esant toliau nurodytiems scenarijams.</span><span class="sxs-lookup"><span data-stu-id="18e0a-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="18e0a-108">Norėdami išvengti pakartotinio programos naudojimo paskesniuose procesuose, programos duomenis galite pažymėti iš karto po to, kai jie panaudojami elektroniniams dokumentams generuoti.</span><span class="sxs-lookup"><span data-stu-id="18e0a-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="18e0a-109">Pavyzdžiui, mokėjimo operacijas galite pažymėti kaip jau apdorotas iš karto po to, kai jos buvo įtrauktos į sugeneruotą mokėjimo pranešimą.</span><span class="sxs-lookup"><span data-stu-id="18e0a-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="18e0a-110">Saugoti elektroninių dokumentų, kurie buvo sugeneruoti naudojant ER logiką, apdorojimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="18e0a-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="18e0a-111">Pavyzdžiui, unikalią mokėjimo pranešimo identifikaciją, sukurtą naudojant ER išraišką.</span><span class="sxs-lookup"><span data-stu-id="18e0a-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="18e0a-112">Išraiška grindžiama informacija, kuri įvesta į ER dialogo langą paleidus ER formatą dokumentams generuoti.</span><span class="sxs-lookup"><span data-stu-id="18e0a-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="18e0a-113">Norėdami sužinoti daugiau apie šią funkciją, paleiskite užduočių vedlių rinkinį ER: dokumentų su programos duomenų atnaujinimu generavimas (Verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677) dalis), kuriame pateikta informacija apie Intrastat ataskaitų teikimą ir archyvavimą.</span><span class="sxs-lookup"><span data-stu-id="18e0a-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="18e0a-114">Šiuose užduočių vedliuose nurodyti failai turi atlikti tam tikrus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="18e0a-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="18e0a-115">Atsisiųskite ir įrašykite šiuos failus į savo vietinį kompiuterį.</span><span class="sxs-lookup"><span data-stu-id="18e0a-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="18e0a-116">ER duomenų modelio konfigūracija: Intrastat (modelis)</span><span class="sxs-lookup"><span data-stu-id="18e0a-116">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="18e0a-117">ER modelio susiejimo konfigūracija: Intrastat (susiejimas)</span><span class="sxs-lookup"><span data-stu-id="18e0a-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="18e0a-118">ER formato konfigūracija: Intrastat (formatas)</span><span class="sxs-lookup"><span data-stu-id="18e0a-118">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)

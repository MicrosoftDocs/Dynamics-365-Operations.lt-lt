---
title: Elektroninių dokumentų generavimas ir prašymų duomenų naujinimas naudojant ER
description: Galite kurti elektroninių ataskaitų (ER) formatus, kuriuos galima naudoti programoje norint generuoti siunčiamus elektroninius dokumentus.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5f66a173c7d66f915a7802e42caf1a36f661eea1
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944322"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="d7f03-103">Elektroninių dokumentų generavimas ir prašymų duomenų naujinimas naudojant ER</span><span class="sxs-lookup"><span data-stu-id="d7f03-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7f03-104">Galite kurti elektroninių ataskaitų (ER) formatus, kuriuos galima naudoti programoje norint generuoti siunčiamus elektroninius dokumentus.</span><span class="sxs-lookup"><span data-stu-id="d7f03-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="d7f03-105">Taip pat galite kurti ER formatus, kurie analizuoja gaunamus elektroninius dokumentus ir naudoja šių dokumentų turinį programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="d7f03-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="d7f03-106">Naudojant šią funkciją, vieną ER formatą galima naudoti siunčiamiems elektroniniams dokumentams generuoti ir tada programos duomenims atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="d7f03-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="d7f03-107">Šią funkciją galima naudoti esant toliau nurodytiems scenarijams.</span><span class="sxs-lookup"><span data-stu-id="d7f03-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="d7f03-108">Norėdami išvengti pakartotinio programos naudojimo paskesniuose procesuose, programos duomenis galite pažymėti iš karto po to, kai jie panaudojami elektroniniams dokumentams generuoti.</span><span class="sxs-lookup"><span data-stu-id="d7f03-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="d7f03-109">Pavyzdžiui, mokėjimo operacijas galite pažymėti kaip jau apdorotas iš karto po to, kai jos buvo įtrauktos į sugeneruotą mokėjimo pranešimą.</span><span class="sxs-lookup"><span data-stu-id="d7f03-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="d7f03-110">Saugoti elektroninių dokumentų, kurie buvo sugeneruoti naudojant ER logiką, apdorojimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="d7f03-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="d7f03-111">Pavyzdžiui, unikalią mokėjimo pranešimo identifikaciją, sukurtą naudojant ER išraišką.</span><span class="sxs-lookup"><span data-stu-id="d7f03-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="d7f03-112">Išraiška grindžiama informacija, kuri įvesta į ER dialogo langą paleidus ER formatą dokumentams generuoti.</span><span class="sxs-lookup"><span data-stu-id="d7f03-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="d7f03-113">Norėdami sužinoti daugiau apie šią funkciją, paleiskite užduočių vedlių rinkinį ER: dokumentų su programos duomenų atnaujinimu generavimas (Verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677) dalis), kuriame pateikta informacija apie Intrastat ataskaitų teikimą ir archyvavimą.</span><span class="sxs-lookup"><span data-stu-id="d7f03-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="d7f03-114">Šiuose užduočių vedliuose nurodyti failai turi atlikti tam tikrus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d7f03-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="d7f03-115">Atsisiųskite ir įrašykite šiuos failus į savo vietinį kompiuterį.</span><span class="sxs-lookup"><span data-stu-id="d7f03-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="d7f03-116">ER duomenų modelio konfigūracija: Intrastat (modelis)</span><span class="sxs-lookup"><span data-stu-id="d7f03-116">ER data model configuration: Intrastat (model)</span></span>](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [<span data-ttu-id="d7f03-117">ER modelio susiejimo konfigūracija: Intrastat (susiejimas)</span><span class="sxs-lookup"><span data-stu-id="d7f03-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [<span data-ttu-id="d7f03-118">ER formato konfigūracija: Intrastat (formatas)</span><span class="sxs-lookup"><span data-stu-id="d7f03-118">ER format configuration: Intrastat (format)</span></span>](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

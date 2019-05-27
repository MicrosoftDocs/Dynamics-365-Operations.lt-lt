---
title: Importuoti ISO20022 tiesioginio debeto konfigūraciją
description: Šioje procedūroje parodoma, kaip importuoti kliento mokėjimų elektroninių ataskaitų konfigūraciją.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1757a1477e46f71e327bb70cf4780767b7509e55
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568728"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="841e7-103">Importuoti ISO20022 tiesioginio debeto konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="841e7-103">Import ISO20022 direct debit configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="841e7-104">Šioje procedūroje parodoma, kaip importuoti kliento mokėjimų elektroninių ataskaitų konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="841e7-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="841e7-105">Šioje procedūroje kaip pavyzdys naudojamas ISO 20022 tiesioginio debeto formatas.</span><span class="sxs-lookup"><span data-stu-id="841e7-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="841e7-106">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, tačiau šiuo tikslu galite naudoti bet kokią demonstracinių duomenų įmonę.</span><span class="sxs-lookup"><span data-stu-id="841e7-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="841e7-107">Tai yra pirmoji iš penkių procedūrų, kuriose apibūdinamas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="841e7-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="841e7-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="841e7-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="841e7-109">Galimų konfigūracijos teikėjų sąraše pasirinkite „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="841e7-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="841e7-110">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="841e7-110">Click Set active.</span></span>
4. <span data-ttu-id="841e7-111">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="841e7-111">Click Repositories.</span></span>
5. <span data-ttu-id="841e7-112">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="841e7-112">Click Open.</span></span>
6. <span data-ttu-id="841e7-113">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="841e7-113">Click Show filters.</span></span>
7. <span data-ttu-id="841e7-114">Taikykite šiuos filtrus: lauke Konfigūracijos pavadinimas įveskite filtro reikšmę ISO20022 tiesioginis debetas (DE) naudodami filtro operatorių Prasideda.</span><span class="sxs-lookup"><span data-stu-id="841e7-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="841e7-115">Jei norite, konfigūraciją galite rasti sąraše, ją pasirinkti ir praleisti šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="841e7-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="841e7-116">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="841e7-116">Click Import.</span></span>
    * <span data-ttu-id="841e7-117">Jei mygtuko Importuoti naudoti negalima, tai reiškia, kad ši konfigūracija jau importuota.</span><span class="sxs-lookup"><span data-stu-id="841e7-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="841e7-118">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="841e7-118">Click Yes.</span></span>


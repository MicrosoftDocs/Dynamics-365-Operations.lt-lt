---
title: Importuoti ISO20022 tiesioginio debeto konfigūraciją
description: Šioje procedūroje parodoma, kaip importuoti kliento mokėjimų elektroninių ataskaitų konfigūraciją.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d0358c414af20558e7e5aaadad5d9844f7853bf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840894"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="c9b3e-103">Importuoti ISO20022 tiesioginio debeto konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="c9b3e-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c9b3e-104">Šioje procedūroje parodoma, kaip importuoti kliento mokėjimų elektroninių ataskaitų konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="c9b3e-105">Šioje procedūroje kaip pavyzdys naudojamas ISO 20022 tiesioginio debeto formatas.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="c9b3e-106">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, tačiau šiuo tikslu galite naudoti bet kokią demonstracinių duomenų įmonę.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="c9b3e-107">Tai yra pirmoji iš penkių procedūrų, kuriose apibūdinamas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="c9b3e-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c9b3e-109">Galimų konfigūracijos teikėjų sąraše pasirinkite „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="c9b3e-110">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-110">Click Set active.</span></span>
4. <span data-ttu-id="c9b3e-111">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-111">Click Repositories.</span></span>
5. <span data-ttu-id="c9b3e-112">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-112">Click Open.</span></span>
6. <span data-ttu-id="c9b3e-113">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-113">Click Show filters.</span></span>
7. <span data-ttu-id="c9b3e-114">Taikykite šiuos filtrus: lauke Konfigūracijos pavadinimas įveskite filtro reikšmę ISO20022 tiesioginis debetas (DE) naudodami filtro operatorių Prasideda.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="c9b3e-115">Jei norite, konfigūraciją galite rasti sąraše, ją pasirinkti ir praleisti šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="c9b3e-116">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-116">Click Import.</span></span>
    * <span data-ttu-id="c9b3e-117">Jei mygtuko Importuoti naudoti negalima, tai reiškia, kad ši konfigūracija jau importuota.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="c9b3e-118">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c9b3e-118">Click Yes.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
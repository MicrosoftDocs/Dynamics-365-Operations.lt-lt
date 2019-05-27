---
title: Finansinės dimensijos ir pagrindinės sąskaitos, naudojamos iš dešinės į kairę rašomose kalbose
description: Šioje temoje aprašomi kai kurie diegimo sprendimai, kuriuos turėtumėte apsvarstyti, kai naudojate kalbą, kurioje rašoma iš dešinės į kairę, ir norite nustatyti finansines dimensijas bei pagrindines sąskaitas.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9609c052083dc3157618584da9311211ea036eba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555599"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="7f249-103">Finansinės dimensijos ir pagrindinės sąskaitos, naudojamos iš dešinės į kairę rašomose kalbose</span><span class="sxs-lookup"><span data-stu-id="7f249-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f249-104">Šioje temoje aprašomi kai kurie diegimo sprendimai, kuriuos turėtumėte apsvarstyti, kai naudojate kalbą, kurioje rašoma iš dešinės į kairę, ir norite nustatyti finansines dimensijas bei pagrindines sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="7f249-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="7f249-105">Finansinės dimensijos ir pagrindinės sąskaitos yra pagrindiniai taikymo planavimo etapo komponentai.</span><span class="sxs-lookup"><span data-stu-id="7f249-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="7f249-106">Sistemoje sukūrus finansines dimensijas ir pagrindines sąskaitas, jos yra naudojamos puslapiuose **Sąskaitų struktūrų konfigūravimas**, **Išplėstinės taisyklės struktūros** ir **Finansinių dimensijų konfigūravimas, kad būtų galima integruoti programas**.</span><span class="sxs-lookup"><span data-stu-id="7f249-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="7f249-107">Tuose puslapiuose nustatyta tvarka sistemoje naudojama duomenims įvesti ir naudoti.</span><span class="sxs-lookup"><span data-stu-id="7f249-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="7f249-108">Kai kuriose sistemos vietose, finansinės dimensijos ir pagrindinės sąskaitos rodomos atskiruose laukuose.</span><span class="sxs-lookup"><span data-stu-id="7f249-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="7f249-109">Tačiau kitose vietose, pvz., žurnaluose, finansinės dimensijos ir pagrindinės sąskaitos rodomos vienoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7f249-109">However, in other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="7f249-110">Kaip geriausia nustatyti finansines dimensijas ir pagrindines sąskaitas, kai sistemoje naudojama kalba, kurioje rašoma iš dešinės į kairę</span><span class="sxs-lookup"><span data-stu-id="7f249-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

-   <span data-ttu-id="7f249-111">Kai renkatės sąskaitų plano skyriklį, pasirinkite vieną iš dvigubų skyriklių: dvigubą brūkšnelį (--), dvigubą juostą (||), dvigubą tašką (..) arba dvigubą pabraukimą (\_\_).</span><span class="sxs-lookup"><span data-stu-id="7f249-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (--), double bar (||) or double period (..), or double underscore (\_\_).</span></span>
-   <span data-ttu-id="7f249-112">Kurdami finansinių dimensijų ir pagrindinių sąskaitų reikšmes, naudokite tik kalbos, kurioje rašoma iš dešinės į kairę, skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="7f249-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
-   <span data-ttu-id="7f249-113">Nenaudokite pasirinkto sąskaitų plano skyriklio finansinių dimensijų ir pagrindinių sąskaitų reikšmėse.</span><span class="sxs-lookup"><span data-stu-id="7f249-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="7f249-114">Laikydamiesi šių patarimų, užtikrinsite, kad vartotojo nurodyta tvarka būtų nuosekliai rodoma visoje sistemoje.</span><span class="sxs-lookup"><span data-stu-id="7f249-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>




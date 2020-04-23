---
title: Produktų, kuriuos galima gaminti arba įsigyti, nustatymas
description: 'Produktai gali būti gaunami įvairiais būdais: jų galima pagaminti arba įsigyti (nusipirkti). Šiame straipsnyje aprašomi keli dažni punktai, kuriuos reikėtų apsvarstyti konfigūruojant kelių produktų šaltinių naudojimą.'
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e68488a714764e7260fb141ccecdc361a8fd7bfa
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214716"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="cd5b3-104">Produktų, kuriuos galima gaminti arba įsigyti, nustatymas</span><span class="sxs-lookup"><span data-stu-id="cd5b3-104">Set up products that can be produced or procured</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd5b3-105">Produktai gali būti gaunami įvairiais būdais: jų galima pagaminti arba įsigyti (nusipirkti).</span><span class="sxs-lookup"><span data-stu-id="cd5b3-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="cd5b3-106">Šiame straipsnyje aprašomi keli dažni punktai, kuriuos reikėtų apsvarstyti konfigūruojant kelių produktų šaltinių naudojimą.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="cd5b3-107">Keli šaltiniai paprastai naudojami nupirktai prekei, kuri kartais gaminama, arba kai prekė, kuri pirmiausia buvo gaminama prekė, pakeičiama į pirmiausia perkamą prekę.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="cd5b3-108">Prekė pradžioje bus priskirta kaip pagaminta prekė, kad būtų galima apibūdinti komplektavimo specifikaciją (KS) ir maršruto informaciją, ir palaikyti prekės gamybos užsakymus.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="cd5b3-109">Gamybos tipas turi būti nustatytas į **KS** (arba gamybos procese – į **Formulė** arba **Sudėtinis produktas**).</span><span class="sxs-lookup"><span data-stu-id="cd5b3-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="cd5b3-110">Naudodami standartines išlaidas, galite apskaičiuoti pagamintos prekės išlaidų įrašą.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="cd5b3-111">Tačiau prekės išlaidų įrašas negali sutapti su standartine kaina, kurios jums reikia pirkimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="cd5b3-112">Šiuo atveju standartinė kaina turi būti įvesta neautomatiškai ir suaktyvinta prekės kainos įrašui.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="cd5b3-113">Skaičiuodami išlaidas, galite naudoti specialią KS ir maršrutą, kurie nurodo produktų rinkinio pasiūlą per ataskaitinį laikotarpį, siekiant per tam tikrą laiką sumažinti nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="cd5b3-114">Be to, vienoje teritorijoje pagaminta prekė gali būti perkelta į kitą teritoriją.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="cd5b3-115">Todėl prekės savikaina turi būti įvesta neautomatiškai ir suaktyvinta teritorijai, į kurią prekė perkeliama.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="cd5b3-116">Kai naudojate pagamintą prekę kaip aukšto lygio produktų komponentą, komponento išlaidos turi būti laikomos nupirkta preke.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="cd5b3-117">Šios gairės taikomos nepriklausomai nuo to, ar komponento išlaidos buvo apskaičiuotos, ar įvestos neautomatiškai.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="cd5b3-118">Kitaip tariant, KS apskaičiavimas turi prekės išlaidas laikyti nupirktu komponentu, o ne naudoti prekės KS ir maršruto informaciją išlaidoms apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="cd5b3-119">Norėdami neleisti skaičiuoti, pasirinkite išskleidimo vėliavėlę **Stabdyti išskleidimą**, kuri yra KS skaičiavimo grupėje, priskirtoje prekei.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="cd5b3-120">Norėdami bendrojo planavimo skaičiavimams neleisti išskleisti poreikių naudojant prekę, prekės padengimo arba padengimo grupėje nustatykite išskleidimo ribą į 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="cd5b3-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="cd5b3-121">Tada bendrojo planavimo skaičiavimas prekę laikys nupirkta preke ir daugiau neatliks prekės KS ir maršruto informacijos skaičiavimų.</span><span class="sxs-lookup"><span data-stu-id="cd5b3-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>






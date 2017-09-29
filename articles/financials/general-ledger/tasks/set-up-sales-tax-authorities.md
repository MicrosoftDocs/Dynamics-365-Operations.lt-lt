--- 
title: "PVM rinkėjų nustatymas"
description: "PVM institucijos yra subjektai, kuriems reikia pranešti apie surinktą PVM ir jį sumokėti."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f75ee28343161026a73dd889b345d65ecc345884
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="ff100-103">PVM rinkėjų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ff100-103">Set up sales tax authorities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff100-104">PVM institucijos yra subjektai, kuriems reikia pranešti apie surinktą PVM ir jį sumokėti.</span><span class="sxs-lookup"><span data-stu-id="ff100-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="ff100-105">Galite mokėti mokesčius PVM institucijai tiesiogiai arba per tiekėjo sąskaitą, kuri sukurta PVM institucijai.</span><span class="sxs-lookup"><span data-stu-id="ff100-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="ff100-106">Jei tai padarote, įmonė gali naudoti savo įprastas mokėjimo procedūras, kad PVM sumokėtų laiku.</span><span class="sxs-lookup"><span data-stu-id="ff100-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="ff100-107">Jei nenustatote PVM rinkėjo kaip tiekėjo, mokėjimą PVM rinkėjui mokėjimo dieną reikia parengti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="ff100-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="ff100-108">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="ff100-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ff100-109">Pasirinkite Mokestis > Netiesioginiai mokesčiai > PVM > PVM institucijos.</span><span class="sxs-lookup"><span data-stu-id="ff100-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="ff100-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ff100-110">Click New.</span></span>
3. <span data-ttu-id="ff100-111">Lauke Institucija surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ff100-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="ff100-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ff100-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ff100-113">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ff100-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ff100-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ff100-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ff100-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ff100-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ff100-116">Pasirinkite ataskaitos maketą, skirtą jūsų šaliai / regionui, jei toks yra.</span><span class="sxs-lookup"><span data-stu-id="ff100-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="ff100-117">Jei ataskaitų maketai neatitinka PVM institucijos reikalavimų, naudokite numatytąjį maketą.</span><span class="sxs-lookup"><span data-stu-id="ff100-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="ff100-118">Įveskite reikšmes formoje Apvalinimas ir laukuose Apvalinti, kad nurodytumėte, kaip turėtų būti apvalinama mokėtina visa mokesčių suma.</span><span class="sxs-lookup"><span data-stu-id="ff100-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="ff100-119">Visi apvalinimo skirtumai bus registruojami DK sąrankoje Automatinių operacijų sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="ff100-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="ff100-120">Lauke Apvalinti įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ff100-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="ff100-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ff100-121">Click Save.</span></span>


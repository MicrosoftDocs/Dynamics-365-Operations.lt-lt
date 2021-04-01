---
title: PVM rinkėjų nustatymas
description: PVM institucijos yra subjektai, kuriems reikia pranešti apie surinktą PVM ir jį sumokėti.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eff67bc32eafea86d0ff582c56059c28706ed2a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222243"
---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="126fa-103">PVM rinkėjų nustatymas</span><span class="sxs-lookup"><span data-stu-id="126fa-103">Set up sales tax authorities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="126fa-104">PVM institucijos yra subjektai, kuriems reikia pranešti apie surinktą PVM ir jį sumokėti.</span><span class="sxs-lookup"><span data-stu-id="126fa-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="126fa-105">Galite mokėti mokesčius PVM institucijai tiesiogiai arba per tiekėjo sąskaitą, kuri sukurta PVM institucijai.</span><span class="sxs-lookup"><span data-stu-id="126fa-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="126fa-106">Jei tai padarote, įmonė gali naudoti savo įprastas mokėjimo procedūras, kad PVM sumokėtų laiku.</span><span class="sxs-lookup"><span data-stu-id="126fa-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="126fa-107">Jei nenustatote PVM rinkėjo kaip tiekėjo, mokėjimą PVM rinkėjui mokėjimo dieną reikia parengti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="126fa-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="126fa-108">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="126fa-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="126fa-109">Pasirinkite Mokestis > Netiesioginiai mokesčiai > PVM > PVM institucijos.</span><span class="sxs-lookup"><span data-stu-id="126fa-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="126fa-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="126fa-110">Click New.</span></span>
3. <span data-ttu-id="126fa-111">Lauke Institucija surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="126fa-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="126fa-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="126fa-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="126fa-113">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="126fa-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="126fa-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="126fa-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="126fa-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="126fa-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="126fa-116">Pasirinkite ataskaitos maketą, skirtą jūsų šaliai / regionui, jei toks yra.</span><span class="sxs-lookup"><span data-stu-id="126fa-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="126fa-117">Jei ataskaitų maketai neatitinka PVM institucijos reikalavimų, naudokite numatytąjį maketą.</span><span class="sxs-lookup"><span data-stu-id="126fa-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="126fa-118">Įveskite reikšmes formoje Apvalinimas ir laukuose Apvalinti, kad nurodytumėte, kaip turėtų būti apvalinama mokėtina visa mokesčių suma.</span><span class="sxs-lookup"><span data-stu-id="126fa-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="126fa-119">Visi apvalinimo skirtumai bus registruojami DK sąrankoje Automatinių operacijų sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="126fa-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="126fa-120">Lauke Apvalinti įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="126fa-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="126fa-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="126fa-121">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
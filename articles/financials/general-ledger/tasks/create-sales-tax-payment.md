--- 
title: "Kurti PVM mokėjimą"
description: "PVM sudengimo ir registravimo užduotis PVM balansus sudengia PVM sąskaitose ir juos koresponduoja į PVM sudengimo sąskaitą už tam tikrą laikotarpį."
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
ms.openlocfilehash: 6ee84da7fd055c8b0b50c43f134c0fc048ecfaeb
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="0042f-103">Kurti PVM mokėjimą</span><span class="sxs-lookup"><span data-stu-id="0042f-103">Create a sales tax payment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0042f-104">PVM sudengimo ir registravimo užduotis PVM balansus sudengia PVM sąskaitose ir juos koresponduoja į PVM sudengimo sąskaitą už tam tikrą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="0042f-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="0042f-105">Eikite į Mokestis > Deklaracijos > PVM > Sudengti ir užregistruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="0042f-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="0042f-106">Lauke Sudengimo laikotarpis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0042f-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0042f-107">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0042f-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0042f-108">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="0042f-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="0042f-109">Jei puslapyje DK parametrai nepasirinkta parinktis įtraukti taisymus, galima apdoroti skirtingų versijų sudengimą.</span><span class="sxs-lookup"><span data-stu-id="0042f-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="0042f-110">Pradinis yra pirmasis laikotarpio intervalo sudengimas, ir jį galima apdoroti tik vieną kartą per laikotarpio intervalą.</span><span class="sxs-lookup"><span data-stu-id="0042f-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="0042f-111">Funkcija Paskutiniai pataisymai sudengs tas PVM operacijas, kurios užregistruotos sukūrus pradinę versiją.</span><span class="sxs-lookup"><span data-stu-id="0042f-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="0042f-112">Lauke Operacijos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="0042f-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="0042f-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0042f-113">Click OK.</span></span>



---
title: PVM mokėjimo kūrimas
description: PVM sudengimo ir registravimo užduoties procedūra PVM balansus sudengia PVM sąskaitose ir juos koresponduoja į PVM sudengimo sąskaitą už tam tikrą laikotarpį.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9523ef75953bdca36f509f596c51c08b12b3fdb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254468"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="fe632-103">PVM mokėjimo kūrimas</span><span class="sxs-lookup"><span data-stu-id="fe632-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe632-104">PVM sudengimo ir registravimo užduoties procedūra PVM balansus sudengia PVM sąskaitose ir juos koresponduoja į PVM sudengimo sąskaitą už tam tikrą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="fe632-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="fe632-105">Eikite į **Mokestis > Deklaracijos > PVM > Sudengti ir užregistruoti PVM**.</span><span class="sxs-lookup"><span data-stu-id="fe632-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="fe632-106">Lauke **Sudengimo laikotarpis** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fe632-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="fe632-107">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="fe632-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="fe632-108">Lauke **Pradžios data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="fe632-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="fe632-109">Jei puslapyje **DK parametrai** nepasirenkate parinkties **įtraukti taisymus**, galima apdoroti skirtingų versijų sudengimą.</span><span class="sxs-lookup"><span data-stu-id="fe632-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="fe632-110">Pradinis yra pirmasis laikotarpio intervalo sudengimas, ir jį galima apdoroti tik vieną kartą per laikotarpio intervalą.</span><span class="sxs-lookup"><span data-stu-id="fe632-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="fe632-111">Funkcija Paskutiniai pataisymai sudengs tas PVM operacijas, kurios užregistruotos sukūrus pradinę versiją.</span><span class="sxs-lookup"><span data-stu-id="fe632-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="fe632-112">Lauke **Operacijos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="fe632-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="fe632-113">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fe632-113">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7aec00c2fb657f0b4074063ef7acad5f4372ebca
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646340"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="cbed2-103">PVM mokėjimo kūrimas</span><span class="sxs-lookup"><span data-stu-id="cbed2-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cbed2-104">PVM sudengimo ir registravimo užduoties procedūra PVM balansus sudengia PVM sąskaitose ir juos koresponduoja į PVM sudengimo sąskaitą už tam tikrą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="cbed2-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="cbed2-105">Eikite į **Mokestis > Deklaracijos > PVM > Sudengti ir užregistruoti PVM**.</span><span class="sxs-lookup"><span data-stu-id="cbed2-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="cbed2-106">Lauke **Sudengimo laikotarpis** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cbed2-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cbed2-107">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cbed2-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="cbed2-108">Lauke **Pradžios data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="cbed2-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="cbed2-109">Jei puslapyje **DK parametrai** nepasirenkate parinkties **įtraukti taisymus**, galima apdoroti skirtingų versijų sudengimą.</span><span class="sxs-lookup"><span data-stu-id="cbed2-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="cbed2-110">Pradinis yra pirmasis laikotarpio intervalo sudengimas, ir jį galima apdoroti tik vieną kartą per laikotarpio intervalą.</span><span class="sxs-lookup"><span data-stu-id="cbed2-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="cbed2-111">Funkcija Paskutiniai pataisymai sudengs tas PVM operacijas, kurios užregistruotos sukūrus pradinę versiją.</span><span class="sxs-lookup"><span data-stu-id="cbed2-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="cbed2-112">Lauke **Operacijos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="cbed2-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="cbed2-113">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="cbed2-113">Click **OK**.</span></span>


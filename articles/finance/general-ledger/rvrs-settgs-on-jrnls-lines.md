---
title: Žurnalų ir eilučių parametrų atšaukimas
description: Šioje temoje nagrinėjama, kodėl bendrajame žurnale įvestas atšaukimo įrašas gali būti neįtrauktas į užregistruotą operaciją.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028576"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="ae1f2-103">Žurnalų ir eilučių parametrų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="ae1f2-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae1f2-104">Šioje temoje nagrinėjama, kodėl bendrajame žurnale įvestas atšaukimo įrašas gali būti neįtrauktas į užregistruotą operaciją.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="ae1f2-105">Požymis</span><span class="sxs-lookup"><span data-stu-id="ae1f2-105">Symptom</span></span>

<span data-ttu-id="ae1f2-106">Bendrajame žurnale yra žurnalo atšaukimo įrašas ir atšaukimo data.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="ae1f2-107">Kai registruojate žurnalą, joks kvitas nėra atšauktas.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="ae1f2-108">Kodėl taip atsitinka?</span><span class="sxs-lookup"><span data-stu-id="ae1f2-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="ae1f2-109">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="ae1f2-109">Resolution</span></span>

<span data-ttu-id="ae1f2-110">Užregistravus žurnalą, vykdant atšaukimo procesą atsižvelgiama tik į parametrus **Atšaukimo įrašas** ir **Atšaukimo data** kvito skyriuje **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="ae1f2-111">Šis metodas leidžia žurnalui įtraukti kai kuriuos kvitus, kurie yra pažymėti atšaukti, ir kitus, kurie nėra pažymėti.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="ae1f2-112">Žurnalo reikšmės naudojamos tik kaip numatytosios, kai įtraukiama *naujų* eilučių.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="ae1f2-113">Reikšmių keitimas žurnale neturi įtakos esamoms eilutėms.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="ae1f2-114">Šiame pavyzdyje pirmiausia buvo įtrauktos kvito eilutės.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="ae1f2-115">Kai įvedate eilutės informaciją prieš nurodydami žurnalą kaip atšaukiamą, nurodymas kaip atšaukimo įrašas ir data nebus taikomas esančioms eilutėms.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="ae1f2-116">Keičiant esamos eilutės atšaukimo įrašą arba atšaukimo datą keitimas atliekamas ir kitose to paties kvito eilutėse.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="ae1f2-117">Siekiant optimizuoti našumą, tinklelis neatnaujinamas atlikus keitimus kitose eilutėse.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="ae1f2-118">Atnaujintos reikšmės gali būti rodomos atnaujintus tinklelį.</span><span class="sxs-lookup"><span data-stu-id="ae1f2-118">You can display the updated values by refreshing the grid.</span></span>



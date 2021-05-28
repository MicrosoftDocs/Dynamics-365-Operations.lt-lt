---
title: Į KS eilučių sunaudojimo principo parametrus nepaisoma
description: Į KS (medžiagų važtaraščio) eilučių sunaudojimo principo parametrus nepaisoma.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026747"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="54208-103">Į KS eilučių sunaudojimo principo parametrus nepaisoma</span><span class="sxs-lookup"><span data-stu-id="54208-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="54208-104">KB numeris: 4612725</span><span class="sxs-lookup"><span data-stu-id="54208-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="54208-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="54208-105">Symptoms</span></span>

<span data-ttu-id="54208-106">Problema atsitinka, kai **Automatinis KS suvartojimas** laukelyje **Automatiinis naujinimas** skirtuke, **Gamybos valdymo parametrai** puslapyje yra nustatytas į *Sunaudojimo principas*.</span><span class="sxs-lookup"><span data-stu-id="54208-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="54208-107">Šis parametras nurodo, kad visos komplektavimo specifikacijos (KS) eilutės turėtų būti automatiškai suvartotos, kai gaunamas pirkimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="54208-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="54208-108">Jei **Sunaudojimo principas** KM eilutės yra aiškiai nustatytas kaip *Rankinis*, galite tikėtis, kad KS eilutės nebus suvartojamos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="54208-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="54208-109">Tačiau, kai iškyla šis problema, KS eilutės, kurių laukas **Sunaudojimo principas** yra nustatytas kaip *Rankinis*, vis tiek suvartojamos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="54208-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="54208-110">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="54208-110">Resolution</span></span>

<span data-ttu-id="54208-111">Jei patiriate šią problemą, gali būti, kad gamybos valdymo parametrai bus nustatyti taip, kad būtų nepaisoma KS eilučių parametro **Sunaudojimo principas**.</span><span class="sxs-lookup"><span data-stu-id="54208-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="54208-112">Puslapyje **Gamybos valdymo parametrai**, skirtuke **Automatinis naujinimas**, patikrinkite lauko **Automatinis KS suvartojimas** vertę.</span><span class="sxs-lookup"><span data-stu-id="54208-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="54208-113">Jei nustatyta kaip *Visada*, sistema nepaisys parametro **Sunaudojimo principo** visose KS eilutėse ir išvalys eilutes.</span><span class="sxs-lookup"><span data-stu-id="54208-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="54208-114">Norėdami, kad sistema gerbtų **Sunaudojimo principo** parametro BOM eilutėse, keiskite **Automatinio BOM suvartojimo** laukelio vertę į *Sunaudojimo principas*.</span><span class="sxs-lookup"><span data-stu-id="54208-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>

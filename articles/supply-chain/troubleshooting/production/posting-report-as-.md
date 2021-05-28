---
title: Ataskaitos kaip baigto publikuto žurnalo klaida
description: Kai registruojate žurnalą Skelbti baigtu, gaunate klaidos pranešimą, kuriame teigiama, kad užsakyto kiekio negalima sumažinti.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026734"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="e4331-103">Ataskaitos kaip baigto publikuto žurnalo klaida</span><span class="sxs-lookup"><span data-stu-id="e4331-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="e4331-104">KB numeris: 4612891</span><span class="sxs-lookup"><span data-stu-id="e4331-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="e4331-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="e4331-105">Symptoms</span></span>

<span data-ttu-id="e4331-106">Kai registruojate **žurnalą Skelbti baigtu**, įvyksta klaida ir gaunate tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="e4331-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="e4331-107">Užsakyto kiekio mažinti negalima, nes nepakanka atvirų atsargų operacijų, kurių būsena Užsakyta.</span><span class="sxs-lookup"><span data-stu-id="e4331-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="e4331-108">Prekės yra Nupirktos, Gautos arba Užregistruotos.</span><span class="sxs-lookup"><span data-stu-id="e4331-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="e4331-109">Ši klaida įvyksta tik tada, kai laukas **Klaidų kiekis** laukelis yra nustatytas ant pirmosios eiltuės **Pranešti apie baigtą** žurnale, o **Geros kokybės** laukelis yra nustatytas paskutinėje.</span><span class="sxs-lookup"><span data-stu-id="e4331-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="e4331-110">Jei **Klaidos kiekis** laukelyje nustatytas paskutinėje eilutėje, klaidų nėra.</span><span class="sxs-lookup"><span data-stu-id="e4331-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="e4331-111">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="e4331-111">Resolution</span></span>

<span data-ttu-id="e4331-112">Norėdami išvengti šios klaidos, atidarykite **gamybos valdymo parametrų** puslapį ir tada **Bendra** skirtuke, nustatykite **Padidėjimas su klaidų kiekis** parinktį į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="e4331-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>

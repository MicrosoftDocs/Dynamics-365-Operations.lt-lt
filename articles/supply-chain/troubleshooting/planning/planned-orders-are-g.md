---
title: Bendrasis planavimas generuoja vienišų produktų suplanuotus užsakymus
description: Suplanuoti užsakymai yra sukuriami vienišiems produktams po pagrindinio planavimo vykdymo.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026752"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="3c636-103">Bendrasis planavimas generuoja vienišų produktų suplanuotus užsakymus</span><span class="sxs-lookup"><span data-stu-id="3c636-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="3c636-104">KB numeris: 4614729</span><span class="sxs-lookup"><span data-stu-id="3c636-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="3c636-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="3c636-105">Symptoms</span></span>

<span data-ttu-id="3c636-106">Suplanuoti užsakymai yra sukuriami vienišiems produktams po pagrindinio planavimo vykdymo.</span><span class="sxs-lookup"><span data-stu-id="3c636-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="3c636-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="3c636-107">Resolution</span></span>

<span data-ttu-id="3c636-108">Išleistų produktų parinkties **„Phantom“** parametras nustato numatytąjį komplektavimo specifikacijos (KS) eilutės tipą.</span><span class="sxs-lookup"><span data-stu-id="3c636-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="3c636-109">Kai nustatyta prinktias **„Phantom“** į *Taip*, sistema vis tiek sukurs suplanuotus prekės užsakymus, tačiau kiekvienam suplanuotam užsakymui bus nustatyta parinktis **Tiesiogiai išvestas poreikis** bus nustatyta kaip *Taip*.</span><span class="sxs-lookup"><span data-stu-id="3c636-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="3c636-110">Todėl suplanuoto gamybos užsakymo negalima patvirtinti pats.</span><span class="sxs-lookup"><span data-stu-id="3c636-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="3c636-111">Jis visada bus automatiškai įtrauktas, kai patvirtinsite pirminį gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3c636-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="3c636-112">Be to, suplanuoto vienišo užsakymo KS eilutės bus įtrauktos į pirminio gamybos užsakymo KS.</span><span class="sxs-lookup"><span data-stu-id="3c636-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>

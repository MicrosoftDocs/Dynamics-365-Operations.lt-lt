---
title: Vidinės įmonės operacijų TDS skaičiavimas
description: Šioje temoje aprašomas procesas, naudojamas apskaičiuoti atskaičius mokesčius šaltinio (TDS) vidinės įmonės operacijose etapais.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023451"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="e1e67-103">Vidinės įmonės operacijų TDS skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="e1e67-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1e67-104">Šioje temoje aprašomas procesas, naudojamas apskaičiuoti atskaičius mokesčius šaltinio (TDS) vidinės įmonės operacijose etapais.</span><span class="sxs-lookup"><span data-stu-id="e1e67-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="e1e67-105">Kai sukuriamas vidinės įmonės pirkimo užsakymas arba pardavimo užsakymas, TDS grupė, nurodyta klientui ar tiekėjui, naudojama TDS sumai apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="e1e67-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="e1e67-106">TDS suma užregistruojama susigrąžinamose arba mokėtinose sąskaitose po to, kai UŽREGISTRUOJAma SF.</span><span class="sxs-lookup"><span data-stu-id="e1e67-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="e1e67-107">Vidinės įmonės pardavimo arba pirkimo užsakymas automatiškai sukuriamas pradiniam pirkimo užsakymui arba pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="e1e67-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="e1e67-108">Vidinės įmonės užsakyme rodoma numatytoji TDS grupė, kad būtų galima apskaičiuoti TDS.</span><span class="sxs-lookup"><span data-stu-id="e1e67-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="e1e67-109">TDS grupę galite keisti.</span><span class="sxs-lookup"><span data-stu-id="e1e67-109">You can change the TDS group.</span></span> <span data-ttu-id="e1e67-110">SF galima registruoti tik tada, jei vidinės įmonės užsakymo, kuris automatiškai sukuriamas, grynoji SF suma sutampa su pradinio užsakymo SF suma.</span><span class="sxs-lookup"><span data-stu-id="e1e67-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="e1e67-111">(Grynoji suma yra SF suma, atskaičius TDS.)</span><span class="sxs-lookup"><span data-stu-id="e1e67-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="e1e67-112">Pavyzdžiui, sukuriama 50 000 pardavimo SF, prie jos pridedama **10%** TDS grupė.</span><span class="sxs-lookup"><span data-stu-id="e1e67-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="e1e67-113">Užregistruota SF suma yra 45 000, o užregistruota pardavimo SF TDS suma yra 5000.</span><span class="sxs-lookup"><span data-stu-id="e1e67-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="e1e67-114">Automatiškai sukuriamas vidinės įmonės pardavimo užsakymo pirkimo užsakymas, prie jo pridedama **10%** TDS grupė.</span><span class="sxs-lookup"><span data-stu-id="e1e67-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="e1e67-115">Jeigu TDS grupę pakeisite į **15%**  SF užregistruoti nepavyks, nes automatiškai sukurto vidinės įmonės pardavimo užsakymo grynoji SF suma neatitinka pradinio pardavimo užsakymo grynosios SF sumos.</span><span class="sxs-lookup"><span data-stu-id="e1e67-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="e1e67-116">Automatiškai užregistruojamas vidinės įmonės SF sukurtas mokėjimo žurnalas.</span><span class="sxs-lookup"><span data-stu-id="e1e67-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="e1e67-117">Šį mokėjimų žurnalą galima registruoti tik tada, jei jo grynoji mokėjimo suma atitinka pradinio mokėjimų žurnalo grynąją mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="e1e67-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>

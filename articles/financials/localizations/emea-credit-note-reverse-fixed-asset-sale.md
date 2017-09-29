---
title: Ilgalaikio turto likvidavimas (Estija ir Lietuva)
description: "Šioje temoje pateikiama informacija apie ilgalaikio turto likvidavimo kredito pažymas, kai laisvos formos SF užregistruojamos vartotojams, kurių juridiniai subjektai yra Estijoje ir Lietuvoje."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeCreditNote_W, CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 266944
ms.search.region: Estonia, Lithuania
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: bc181f51dec0a18416f095030c8c698ce95987c2
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-assets-disposal-for-estonia-and-lithuania"></a><span data-ttu-id="108cb-103">Ilgalaikio turto likvidavimas (Estija ir Lietuva)</span><span class="sxs-lookup"><span data-stu-id="108cb-103">Fixed assets disposal for Estonia and Lithuania</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="108cb-104">Šioje temoje pateikiama informacija apie ilgalaikio turto likvidavimo kredito pažymas, kai laisvos formos SF užregistruojamos vartotojams, kurių juridiniai subjektai yra Estijoje ir Lietuvoje.</span><span class="sxs-lookup"><span data-stu-id="108cb-104">This topic provides information about credit notes for fixed assets disposal posted by a free text invoice for users in legal entities in Estonia and Lithuania.</span></span>

<span data-ttu-id="108cb-105">Ilgalaikį turtą galima parduoti naudojant likvidavimo funkciją, pateiktą laisvos formos SF, ilgalaikio turto žurnale bendrajame žurnale DK.</span><span class="sxs-lookup"><span data-stu-id="108cb-105">Fixed assets can be sold using disposal functionality through a free text invoice, fixed asset journal, or general journal in General ledger.</span></span> <span data-ttu-id="108cb-106">Daugiau informacijos žr. puslapyje [Ilgalaikio turto likvidavimo registravimo sąskaitos](../fixed-assets/fixed-asset-disposal-posting-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="108cb-106">For more information, see [Fixed asset disposal posting accounts](../fixed-assets/fixed-asset-disposal-posting-accounts.md).</span></span> <span data-ttu-id="108cb-107">Ilgalaikio turto likvidavimo kredito pažymų funkcija suteikia galimybę vartotojams, kurių juridiniai subjektai yra Estijoje ir Lietuvoje, kurti laisvos formos SF kredito pažymą su ilgalaikio turto pardavimu ir tada ją užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="108cb-107">Fixed assets disposal credit note functionality allows users in legal entities in Estonia and Latvia to create a credit note for a free text invoice with sales of a fixed asset and then post it.</span></span> <span data-ttu-id="108cb-108">Norėdami kurti kredito pažymą ir atšaukti laisvos formos SF, kuri buvo sugeneruota ilgalaikiam turtui parduoti, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="108cb-108">To create a credit note to reverse a free text invoice that was generated for the sale of a fixed asset, complete the following steps:</span></span>

1.  <span data-ttu-id="108cb-109">Spustelėkite **Gautinos sumos** &gt; **SF** &gt; **Visos laisvos formos SF**.</span><span class="sxs-lookup"><span data-stu-id="108cb-109">Click **Accounts receivable** &gt; **Invoices** &gt; **All free text invoices**.</span></span>
2.  <span data-ttu-id="108cb-110">Pasirinkite laisvos formos SF, kurios kredito pažymą kuriate.</span><span class="sxs-lookup"><span data-stu-id="108cb-110">Select the free text invoice that you are creating a credit note for.</span></span>
3.  <span data-ttu-id="108cb-111">Veiksmų srities skirtuko **SF** grupėje **Atšaukti** spustelėkite **Kurti kredito pažymą**.</span><span class="sxs-lookup"><span data-stu-id="108cb-111">On the Action Pane, in the **Cancel** group of the **Invoice** tab, click **Create credit note**.</span></span> <span data-ttu-id="108cb-112">**Pastaba.** Kurdami kredito pažymą turite įtraukti kiekvieną operacijos eilutę iš laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="108cb-112">**Note:** When you create a credit note, you must include each transaction line from the free text invoice.</span></span>
4.  <span data-ttu-id="108cb-113">Pažymėkite žymės langelį **Kurti koreguojamąsias eilutes**, norėdami įtraukti kiekvienos pradinės laisvos formos SF operacijos eilutės atšaukimo eilutę ir koreguojamąją eilutę.</span><span class="sxs-lookup"><span data-stu-id="108cb-113">Select the **Create corrective lines** check box to add a reversal line and a corrective line to the credit note for each transaction line in the original free text invoice.</span></span>
5.  <span data-ttu-id="108cb-114">Registruokite kredito pažymą.</span><span class="sxs-lookup"><span data-stu-id="108cb-114">Post the credit note.</span></span>

<span data-ttu-id="108cb-115">Atšaukiamos ilgalaikio turto likvidavimo operacijos, sukurtos užregistravus kredito pažymą.</span><span class="sxs-lookup"><span data-stu-id="108cb-115">The fixed asset disposal transactions, created when you posted the credit note, are reversed.</span></span> <span data-ttu-id="108cb-116">Ilgalaikio turto būsena lieka **Parduota**.</span><span class="sxs-lookup"><span data-stu-id="108cb-116">The status of the fixed asset remains **Sold**.</span></span> <span data-ttu-id="108cb-117">Tačiau, jei reikia, ilgalaikio turto būseną galite pakeisti patys.</span><span class="sxs-lookup"><span data-stu-id="108cb-117">You can still change the status of the fixed asset manually, if necessary.</span></span>




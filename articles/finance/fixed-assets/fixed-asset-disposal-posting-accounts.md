---
title: Ilgalaikio turto likvidavimo registravimo sąskaitos
description: Šioje temoje paaiškinama, kaip nustatyti turto likvidavimo DK registravimo sąskaitas.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d1d6a3dc6348e64bcf247544bc7b56c5314db4c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826863"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="f9103-103">Ilgalaikio turto likvidavimo registravimo sąskaitos</span><span class="sxs-lookup"><span data-stu-id="f9103-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9103-104">Šioje temoje paaiškinama, kaip nustatyti turto likvidavimo DK registravimo sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="f9103-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="f9103-105">Puslapio Ilgalaikio turto registravimo šablonai „FastTab“ skirtuke DK sąskaitos pasirinkite Likvidavimas – pardavimas ir Likvidavimas – nurašymas, kad nustatytumėte registravimą į didžiąją knygą.</span><span class="sxs-lookup"><span data-stu-id="f9103-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="f9103-106">Abiejų tipų operacijose ilgalaikio turto likvidavimo vertė kredituojama didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="f9103-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="f9103-107">Debetas registruojamas korespondentinėje sąskaitoje, kuri gali būti, pvz., banko sąskaita.</span><span class="sxs-lookup"><span data-stu-id="f9103-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="f9103-108">Jei ilgalaikis turtas parduodamas klientui, kliento sąskaita naudojama vietoje korespondentinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="f9103-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="f9103-109">Spustelėkite Likvidavimas, tada spustelėkite Pardavimas arba Nurašymas ir nustatykite išsamias sąskaitas ilgalaikio turto balansinei vertei atšaukti.</span><span class="sxs-lookup"><span data-stu-id="f9103-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="f9103-110">Taip pat galite įvesti informaciją puslapio Likvidavimo parametrai laukuose Registruoti vertę ir Pardavimo vertės tipas.</span><span class="sxs-lookup"><span data-stu-id="f9103-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="f9103-111">Turto likvidavimo operacija mažos vertės telkinyje sumažina mažos vertės telkinio balansinę vertę tik likviduojama suma.</span><span class="sxs-lookup"><span data-stu-id="f9103-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="f9103-112">Bet jei turto pardavimas viršija balansinę mažos vertės telkinio vertę, balansinė vertė sumažinama iki nulio.</span><span class="sxs-lookup"><span data-stu-id="f9103-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
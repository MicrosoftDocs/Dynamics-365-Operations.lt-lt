---
title: Paketinis mėnesinių žurnalų įrašų kūrimas
description: Šioje temoje paaiškinama, kaip sukurti žurnalų įrašus pakete, siekiant padidinti efektyvumą, kai įrašomos mėnesinės nuomos išlaidos.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6fd1815620095909e290fd03c404d964baa04a94
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241567"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="5531f-103">Paketinis mėnesinių žurnalų įrašų kūrimas</span><span class="sxs-lookup"><span data-stu-id="5531f-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5531f-104">Šioje temoje paaiškinama, kaip sukurti žurnalų įrašus pakete, siekiant padidinti efektyvumą, kai įrašomos mėnesinės nuomos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="5531f-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="5531f-105">Paketinį vykdymą galima naudoti žurnalų įrašams iš kelių grafikų sukurti.</span><span class="sxs-lookup"><span data-stu-id="5531f-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="5531f-106">Šie žurnalo įrašai gali apimti nuomos mokesčius, įsipareigojimų amortizaciją, naudojimo teise valdomo turto amortizaciją ir eksploatavimo išlaidas</span><span class="sxs-lookup"><span data-stu-id="5531f-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="5531f-107">Taip pat galite naudoti paketinį vykdymą tam, kad būtų galima atlikti pradinį kelių nuomų pripažinimą tuo pačiu metu arba sukurti kelių nuomų perėjimo koregavimus vienu metu.</span><span class="sxs-lookup"><span data-stu-id="5531f-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="5531f-108">Norėdami nustatyti paketinę užduotį arba apdoroti kelių nuomų SF mokėjimą, nusidėvėjimą ar palūkanas, eikite į **Turto nuoma \> Periodinė \> Paketinis žurnalų kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="5531f-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="5531f-109">Pasirodžiusiame dialogo lange galite pasirinkti grafiką, iš kurio bus kuriami žurnalo įrašai.</span><span class="sxs-lookup"><span data-stu-id="5531f-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="5531f-110">Taip pat galite nurodyti, ar turi būti vykdomas konkrečių objektų, nuomos grupių ar nuomos knygų paketinis apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="5531f-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="5531f-111">Vėlesnės operacijos, pvz., įsipareigojimų amortizacijos grafikai, mokėjimai, nusidėvėjimas ir išlaidos, bus registruojamos tik po to, kai užregistruojamas pradinis atitinkamų nuomų pripažinimas</span><span class="sxs-lookup"><span data-stu-id="5531f-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="5531f-112">Žurnalo įrašai sukuriami, tačiau jie nebus užregistruoti tol, kol nepasirinksite komandos **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="5531f-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
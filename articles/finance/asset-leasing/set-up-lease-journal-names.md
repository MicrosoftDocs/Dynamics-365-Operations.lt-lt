---
title: Nuomos žurnalo pavadinimų nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti nuomos žurnalų pavadinimus. Nuomos žurnalų pavadinimai nurodo žurnalus, kuriuose įrašai, kilę iš turto nuomos, registruojami.
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
ms.openlocfilehash: 89c5fc768aafe9e5de9adcde32e7b4d0a084941b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990922"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="99be3-104">Nuomos žurnalo pavadinimų nustatymas</span><span class="sxs-lookup"><span data-stu-id="99be3-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99be3-105">Nuomos žurnalų pavadinimai nurodo žurnalus, kuriuose turto nuomos operacijos registruojamos.</span><span class="sxs-lookup"><span data-stu-id="99be3-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="99be3-106">Puslapio **Turto nuomos parametrai** laukuose **Pirminis pripažinimas** ir **Mėnesio žurnalo pavadinimas** bus rodomi tik tie žurnalų pavadinimai, kurie priskirti žurnalo tipui **Turto nuoma**.</span><span class="sxs-lookup"><span data-stu-id="99be3-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="99be3-107">Lauke **SF žurnalo pavadinimas** galima priskirti tik žurnalo tipą **Tiekėjo SF įrašymas**.</span><span class="sxs-lookup"><span data-stu-id="99be3-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="99be3-108">Norėdami sukonfigūruoti nuomos žurnalų pavadinimus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="99be3-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="99be3-109">Eikite į **Turto nuoma \> Sąranka \> Turto nuomos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="99be3-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="99be3-110">Skirtuko **Bendra** lauke **Pirminio pripažinimo žurnalo pavadinimas** pasirinkite žurnalą.</span><span class="sxs-lookup"><span data-stu-id="99be3-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="99be3-111">Visi pradiniai pripažinimo žurnalo įrašai bus registruojami į šį žurnalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="99be3-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="99be3-112">Lauke **SF žurnalo pavadinimas** pasirinkite žurnalą.</span><span class="sxs-lookup"><span data-stu-id="99be3-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="99be3-113">Jei nuomos knygos parinktis **Sumokėti tiekėjui** nustatyta į **Taip**, nuomos ir išlaidų apmokėjimo SF bus užregistruotos šiame žurnalo pavadinime.</span><span class="sxs-lookup"><span data-stu-id="99be3-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="99be3-114">Lauke **Nuomos žurnalo pavadinimas** pasirinkite žurnalą.</span><span class="sxs-lookup"><span data-stu-id="99be3-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="99be3-115">Visi nusidėvėjimo, palūkanų ir trumpojo laikotarpio perklasifikavimo įrašai bus registruojami į šį žurnalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="99be3-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="99be3-116">Jei nuomos knygos parinktis **Sumokėti tiekėjui** nustatyta į **Ne**, nuomos mokėjimo ir išlaidų apmokėjimo įrašai bus taip pat užregistruoti šiame žurnalo pavadinime.</span><span class="sxs-lookup"><span data-stu-id="99be3-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>

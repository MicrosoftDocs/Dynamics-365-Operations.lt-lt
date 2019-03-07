---
title: Vieno kvito žurnalų ir valiutos kurso pasikeitimo atnaujinimas
description: Kai kurios organizacijos įveda žurnalus, kuriuose yra vienas kvitas, turintis daugiau nei vieną klientą ar tiekėją, be to, vykdo Gautinų sumų ar Mokėtinų sumų užsienio valiutos kurso pasikeitimo procesą. Šioje temoje aprašyti veiksmai, kuriuos tos organizacijos turi atlikti, atnaujinant „Microsoft Dynamics 365 for Operations“ į 1611 versiją.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 343fa226e1cf9072696082e9ebf0a1629e553ae9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "328153"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="c9f8d-104">Vieno kvito žurnalų ir valiutos kurso pasikeitimų plėtojimas</span><span class="sxs-lookup"><span data-stu-id="c9f8d-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9f8d-105">Kai kurios organizacijos įveda žurnalus, kuriuose yra vienas kvitas, turintis daugiau nei vieną klientą ar tiekėją, be to, vykdo Gautinų sumų ar Mokėtinų sumų užsienio valiutos kurso pasikeitimo procesą.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="c9f8d-106">Šioje temoje aprašyti veiksmai, kuriuos tos organizacijos turi atlikti, atnaujinant „Microsoft Dynamics 365 for Operations“ į 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="c9f8d-107">Atlikite šiuos veiksmus atnaujindami „Microsoft Dynamics 365 for Operations“ į 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="c9f8d-108">Prieš atnaujindami į „Dynamics 365 for Operations“, įvykdykite Gautinų sumų ir Mokėtinų sumų užsienio valiutos kurso pasikeitimo procesą.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="c9f8d-109">Nustatykite lauką **Metodas** į **Sąskaitos faktūros data**.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="c9f8d-110">Sukuriama pasikeitimo operacija, kuri anuliuoja paskutinį užsienio valiutos pasikeitimą.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="c9f8d-111">Todėl atidarytos operacijos vertinamos pradine operacijos apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="c9f8d-112">Atnaujinkite „Dynamics 365 for Operations“ į 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="c9f8d-113">Įvykdykite Gautinų sumų ir mokėtinų sumų užsienio valiutos pasikeitimo procesą dar kartą.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="c9f8d-114">Šį kartą lauką **Metodas** nustatykite į **Standartinis**.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="c9f8d-115">Sukuriama nauja pasikeitimo operacija, kuri pagrįsta dabartiniu užsienio valiutos kursu.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="c9f8d-116">Ši operacija įrašo nerealizuotą pelną / nuostolį ir koreguoja suvestinę DK sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="c9f8d-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





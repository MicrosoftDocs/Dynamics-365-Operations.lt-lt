---
title: Vieno kvito žurnalų ir valiutos kurso pasikeitimų plėtojimas
description: Šioje temoje aprašoma, kaip atnaujinti vienkartinių kvitų žurnalus ir valiutos perkainojimus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3504c01a4ed1571866fd2a0cd83eef86a57d684a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127308"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="b88e1-103">Vieno kvito žurnalų ir valiutos kurso pasikeitimų plėtojimas</span><span class="sxs-lookup"><span data-stu-id="b88e1-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b88e1-104">Kai kurios organizacijos įveda žurnalus, kuriuose yra vienas kvitas, turintis daugiau nei vieną klientą ar tiekėją, be to, vykdo Gautinų sumų ar Mokėtinų sumų užsienio valiutos kurso pasikeitimo procesą.</span><span class="sxs-lookup"><span data-stu-id="b88e1-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="b88e1-105">Šioje temoje aprašyti veiksmai, kuriuos tos organizacijos turi atlikti, atnaujinant „Microsoft Dynamics 365 for Operations“ į 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="b88e1-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="b88e1-106">Atlikite šiuos veiksmus atnaujindami „Microsoft Dynamics 365 for Operations“ į 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="b88e1-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="b88e1-107">Prieš atnaujindami į „Finance and Operations“, įvykdykite Gautinų sumų ir Mokėtinų sumų užsienio valiutos kurso pasikeitimo procesą.</span><span class="sxs-lookup"><span data-stu-id="b88e1-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="b88e1-108">Nustatykite lauką **Metodas** į **Sąskaitos faktūros data**.</span><span class="sxs-lookup"><span data-stu-id="b88e1-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="b88e1-109">Sukuriama pasikeitimo operacija, kuri anuliuoja paskutinį užsienio valiutos pasikeitimą.</span><span class="sxs-lookup"><span data-stu-id="b88e1-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="b88e1-110">Todėl atidarytos operacijos vertinamos pradine operacijos apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="b88e1-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="b88e1-111">Atnaujinkite į 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="b88e1-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="b88e1-112">Įvykdykite Gautinų sumų ir mokėtinų sumų užsienio valiutos pasikeitimo procesą dar kartą.</span><span class="sxs-lookup"><span data-stu-id="b88e1-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="b88e1-113">Šį kartą lauką **Metodas** nustatykite į **Standartinis**.</span><span class="sxs-lookup"><span data-stu-id="b88e1-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="b88e1-114">Sukuriama nauja pasikeitimo operacija, kuri pagrįsta dabartiniu užsienio valiutos kursu.</span><span class="sxs-lookup"><span data-stu-id="b88e1-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="b88e1-115">Ši operacija įrašo nerealizuotą pelną / nuostolį ir koreguoja suvestinę DK sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="b88e1-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>

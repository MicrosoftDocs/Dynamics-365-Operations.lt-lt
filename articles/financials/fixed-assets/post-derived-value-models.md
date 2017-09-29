---
title: "Registruoti naudojant išvestines knygas"
description: "Šiame straipsnyje aprašyta, kaip naudoti išvestines knygas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: aaacf596f2ea1107a53647d779e9d2b6c37ab530
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="post-with-derived-books"></a><span data-ttu-id="07079-103">Registruoti naudojant išvestines knygas</span><span class="sxs-lookup"><span data-stu-id="07079-103">Post with derived books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="07079-104">Šiame straipsnyje aprašyta, kaip naudoti išvestines knygas.</span><span class="sxs-lookup"><span data-stu-id="07079-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="07079-105">Registruojant knygos, kuriai yra priskirtų išvestinių knygų, operacijas, išvestinės knygos operacijos automatiškai užregistruojamos žurnaluose, pirkimo užsakymuose arba laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="07079-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="07079-106">Tačiau, jei pagrindinės knygos operacijas ruošiate žurnale Ilgalaikis turtas, išvestinių nusidėvėjimo operacijų sumas galite peržiūrėti ir modifikuoti prieš jas užregistruodami.</span><span class="sxs-lookup"><span data-stu-id="07079-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="07079-107">Tam tikros sąskaitos, pavyzdžiui, PVM ir kliento arba tiekėjo sąskaitos, atnaujinamos tik kartą registruojant pagrindinę knygą.</span><span class="sxs-lookup"><span data-stu-id="07079-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="07079-108">Išvestinės knygos operacijos registruojamos sąskaitose, kurios išvestinei knygai buvo nurodytos puslapyje Ilgalaikio turto registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="07079-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="07079-109">Įsigijimas dažnai naudojamas kaip išvestinių knygų operacijų tipas.</span><span class="sxs-lookup"><span data-stu-id="07079-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="07079-110">Naudokite tai, kai knyga ir išvestinė nusidėvėjimo knyga turėtų būti taikomos ilgalaikiam turtui nuo tada, kai ilgalaikis turtas buvo įsigytas.</span><span class="sxs-lookup"><span data-stu-id="07079-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="07079-111">Operacijų tipui taip pat gali būti taikomos kitos vertės.</span><span class="sxs-lookup"><span data-stu-id="07079-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="07079-112">Pavyzdžiui, jei pagrindinė knyga ir išvestinė knyga turi tuos pačius intervalus atsižvelgiant į pardavimą ar likvidavimą, visus ilgalaikio turto operacijos tipus galima nustatyti išvestinėje knygoje.</span><span class="sxs-lookup"><span data-stu-id="07079-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="07079-113">Išvestinėje knygoje užregistruotas nusidėvėjimas bus išreikštas ta pačia suma, kokia buvo užregistruota pagrindinėje knygoje.</span><span class="sxs-lookup"><span data-stu-id="07079-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="07079-114">Jei skirtingų knygų nusidėvėjimo metodai yra skirtingi, neturėtumėte generuoti nusidėvėjimo operacijų naudodami išvestinius procesus.</span><span class="sxs-lookup"><span data-stu-id="07079-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="07079-115">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="07079-115">Example</span></span> 
<span data-ttu-id="07079-116">Toliau pateikiama informacija apie tai, kaip įsigijimo operacijas nustatyti naudojant išvestinės knygos funkciją.</span><span class="sxs-lookup"><span data-stu-id="07079-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="07079-117">Kurkite knygas puslapyje Knygos.</span><span class="sxs-lookup"><span data-stu-id="07079-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="07079-118">Apskaitos knyga: VM 1, dabartinis registravimo sluoksnis</span><span class="sxs-lookup"><span data-stu-id="07079-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="07079-119">Apskaitos knyga mokesčiams: VM 2, mokesčių registravimo sluoksnis</span><span class="sxs-lookup"><span data-stu-id="07079-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="07079-120">VM 1 spustelėkite skirtuką Išvestinės knygos.</span><span class="sxs-lookup"><span data-stu-id="07079-120">On VM 1, click the Derived books tab.</span></span> <span data-ttu-id="07079-121">Lauke Knyga pasirinkite VM 2, o lauke Operacijos tipas pasirinkite Įsigijimas.</span><span class="sxs-lookup"><span data-stu-id="07079-121">Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="07079-122">Tada knygas galima pridėti prie konkretaus ilgalaikio turto.</span><span class="sxs-lookup"><span data-stu-id="07079-122">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="07079-123">Kai ilgalaikio turto įsigijimas užregistruojamas naudojant knygą VM 1, įsigijimas užregistruojamas ne tik vertinimo modelyje VM 1, bet ir išvestinėje knygoje VM 2.</span><span class="sxs-lookup"><span data-stu-id="07079-123">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="07079-124">Abiejų ilgalaikio turto knygų būsena atnaujinama į Atidaryta.</span><span class="sxs-lookup"><span data-stu-id="07079-124">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="07079-125">Jei išvestinių knygų nenaudojate, ilgalaikio turto įsigijimą turite registruoti ir knygoje VM 1, ir knygoje VM 2.</span><span class="sxs-lookup"><span data-stu-id="07079-125">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="07079-126">Daugiau informacijos ieškokite [Išvestinės knygos](derived-books.md).</span><span class="sxs-lookup"><span data-stu-id="07079-126">For more information, see [Derived books](derived-books.md)</span></span>




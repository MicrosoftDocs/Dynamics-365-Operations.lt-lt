---
title: Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms
description: Šioje temoje aprašomas nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms „Microsoft Dynamics365 Retail”.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 80233a73dbffc7380503cf03703758b187824c2a
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622671"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="8e2c2-103">Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms (viešoji vertinimo versija)</span><span class="sxs-lookup"><span data-stu-id="8e2c2-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="8e2c2-104">„Dynamics 365 Retail” 10.0.4 ir ankstesnėse versijose mažmeninės prekybos išrašo registravimas yra dienos pabaigoje atliekama operacija, o visos operacijos knygose įregistruojamos dienos pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-104">In Dynamics 365 Retail versions 10.0.4 and earlier, retail statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="8e2c2-105">Tuomet dideles operacijas reikia apdoroti per ribotą laiką, dėl to kartais kyla apkrovos ir užraktų bei išrašo registravimo klaidų.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="8e2c2-106">Be to, mažmenininkai savo knygose negali atpažinti įplaukų ir mokėjimų per dieną.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="8e2c2-107">Su „Retail” 10.0.5 versijoje pristatyta nuolatiniu duomenų perdavimu mažais kiekiais pagrįsto užsakymų kūrimo viešąja vertinimo versija operacijos apdorojamos visą dieną, o dienos pabaigoje tvarkomas tik finansinis mokėjimo priemonių derinimas ir kitos grynųjų pinigų valdymo operacijos.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="8e2c2-108">Ši funkcija išskaido pardavimo užsakymų, SF ir mokėjimų kūrimą per visą dieną, taip užtikrindama didesnį našumą ir galimybę atpažinti įplaukas bei mokėjimus knygose beveik tikruoju laiku.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="8e2c2-109">Kaip naudoti nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą registravimą</span><span class="sxs-lookup"><span data-stu-id="8e2c2-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="8e2c2-110">Norėdami įjungti nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą mažmeninės prekybos operacijų registravimą, eikite į **Sistemos administravimas > Sąranka > Licencijos konfigūracija** ir išjunkite raktą **Mažmeninės prekybos išrašai**.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-110">To enable trickle feed-based posting of retail transactions, go to **System administration > Set up > License configuration** and disable the the **Retail statements** key.</span></span>

2. <span data-ttu-id="8e2c2-111">Tame pačiame puslapyje įjunkite licencijos raktą **Mažmeninės prekybos išrašai (duomenų perdavimas mažais kiekiais) – Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-111">On the same page, enable the **Retail statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="8e2c2-112">Įjungę šį raktą įsitikinkite, kad nėra patvirtinimo laukiančių išrašų, kuriuos reikia užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

> [!Important]
> <span data-ttu-id="8e2c2-113">Prieš įjungdami licencijos raktą **Mažmeninės prekybos išrašai (duomenų perdavimas mažais kiekiais) – Peržiūra**, įsitikinkite, kad nėra patvirtinimo laukiančių išrašų, kuriuos reikia užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-113">Before you enable the **Retail statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="8e2c2-114">Dabartinis išrašo dokumentas bus padalintas į du skirtingus tipus: operacijų išrašą ir finansinę ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="8e2c2-115">Operacijų išraše bus pateikiamos visos neužregistruotos ir patvirtintos mažmeninės prekybos operacijos ir kuriami pardavimo užsakymai, pardavimo SF, įmokų ir nuolaidų žurnalai bei pajamų ir išlaidų operacijos jūsų sukonfigūruotame režime.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-115">The transactional statement will pick up all unposted and validated retail transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="8e2c2-116">Turite sukonfigūruoti šį procesą taip, kad šis veiktų dideliu dažnumu ir dokumentai būtų sukuriami mažmeninės prekybos operacijas įkėlus į „Retail Headquarters” per P užduotį.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-116">You should configure this process to run at a high frequency so that documents are created when the retail transactions are uploaded into Retail Headquarters through the P-job.</span></span> <span data-ttu-id="8e2c2-117">Naudojant operacijų išrašą, kuris jau sukuria pardavimo užsakymus ir pardavimo SF, nėra realaus poreikio konfigūruoti paketinę užduotį **Registruoti atsargas**.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="8e2c2-118">Tačiau ją vis tiek galite naudoti konkretiems verslo poreikiams patenkinti.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="8e2c2-119">Finansinė ataskaita turi būti sukurta dienos pabaigoje, ji palaiko tik **Pamaina** uždarymo metodą.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="8e2c2-120">Šis išrašas bus taikomas tik finansiniam suderinimui ir sukurs tik skirtingų mokėjimo priemonių apskaičiuotos sumos ir operacijos sumos skirtumo sumų žurnalus bei kitų grynųjų pinigų valdymo operacijų žurnalus.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between           counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="8e2c2-121">Norėdami apskaičiuoti operacijų išrašą, spustelėkite **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti operacijų išrašų paketinį skaičiavimą**.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-121">To calculate the transactional statement, click **Retail > Retail IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="8e2c2-122">Norėdami atlikti paketinį operacijų išrašų registravimą, spustelėkite **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti operacijų išrašų paketinį registravimą**.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-122">To post the transactional statement statements in batch, click **Retail > Retail IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="8e2c2-123">Norėdami apskaičiuoti finansinę ataskaitą, spustelėkite **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti finansinių ataskaitų paketinį skaičiavimą**.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-123">To calculate the financial statement, click **Retail > Retail IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="8e2c2-124">Norėdami atlikti finansinių ataskaitų paketinį registravimą, spustelėkite **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti finansinių ataskaitų paketinį registravimą**.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-124">To post the financial statements in batch, click **Retail > Retail IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="8e2c2-125">Iš šios naujos funkcijos pašalinti meniu elementai **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti paketinį išrašų apskaičiavimą** ir **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti paketinį išrašų registravimą**.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-125">The menu items **Retail > Retail IT > POS Posting > Calculate statements in batch** and **Retail > Retail IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="8e2c2-126">Operacijų ir finansinių ataskaitų tipus galima kurti ir neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="8e2c2-127">Eikite į **Mažmeninė prekyba > Kanalai > Mažmeninės prekybos parduotuvės** ir spustelėkite **Mažmeninės prekybos išrašai**.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-127">Go to **Retail > Channels > Retail stores** and click **Retail statements**.</span></span> <span data-ttu-id="8e2c2-128">Spustelėkite **Naujas** ir pasirinkite norimo sukurti išrašo tipą.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="8e2c2-129">Puslapyje **Mažmeninės prekybos išrašai** esančiuose laukuose ir puslapyje **Išrašo grupė** esančiuose veiksmuose bus rodomi susiję duomenys ir veiksmai pagal pasirinktą išrašo tipą.</span><span class="sxs-lookup"><span data-stu-id="8e2c2-129">Fields on the **Retail statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>

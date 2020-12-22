---
title: Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms
description: Šioje temoje aprašomas nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas operacijoms „Microsoft Dynamics 365 Commerce”.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
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
ms.openlocfilehash: 79f99b9b401de3e3bcca6ec5a13a3b4f7bad6f8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459577"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="3233b-103">Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms</span><span class="sxs-lookup"><span data-stu-id="3233b-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3233b-104">„Dynamics 365 Retail” 10.0.4 ir ankstesnėse versijose išrašo registravimas yra dienos pabaigoje atliekama operacija. Visos operacijos knygose įregistruojamos dienos pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="3233b-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="3233b-105">Tuomet dideles operacijas reikia apdoroti per ribotą laiką, dėl to kartais kyla apkrovos ir užraktų bei išrašo registravimo klaidų.</span><span class="sxs-lookup"><span data-stu-id="3233b-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="3233b-106">Be to, mažmenininkai savo knygose negali atpažinti įplaukų ir mokėjimų per dieną.</span><span class="sxs-lookup"><span data-stu-id="3233b-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="3233b-107">Naudojant „Retail” 10.0.5 versijoje pristatytą nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą užsakymų kūrimą operacijos apdorojamos visą dieną, o dienos pabaigoje tvarkomas tik finansinis mokėjimo priemonių derinimas ir kitos grynųjų pinigų valdymo operacijos.</span><span class="sxs-lookup"><span data-stu-id="3233b-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="3233b-108">Ši funkcija išskaido pardavimo užsakymų, SF ir mokėjimų kūrimą per visą dieną, taip užtikrindama didesnį našumą ir galimybę atpažinti įplaukas bei mokėjimus knygose beveik tikruoju laiku.</span><span class="sxs-lookup"><span data-stu-id="3233b-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="3233b-109">Kaip naudoti nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą registravimą</span><span class="sxs-lookup"><span data-stu-id="3233b-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="3233b-110">Norėdami įjungti mažmeninės prekybos operacijų nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą registravimą, įjunkite funkciją pavadinimu **Mažmeninės prekybos išrašai – duomenų perdavimas mažais kiekiais** naudodami funkcijų valdymą.</span><span class="sxs-lookup"><span data-stu-id="3233b-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="3233b-111">Prieš įjungdami šią funkciją įsitikinkite, kad nėra patvirtinimo laukiančių išrašų, kuriuos reikia užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="3233b-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="3233b-112">Dabartinis išrašo dokumentas bus padalintas į du tipus: operacijų išrašą ir finansinę ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="3233b-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="3233b-113">Operacijų išraše bus pateikiamos visos neužregistruotos ir patvirtintos operacijos ir kuriami pardavimo užsakymai, pardavimo sąskaitos faktūros, įmokų ir nuolaidų žurnalai bei pajamų ir išlaidų operacijos jūsų sukonfigūruotame režime.</span><span class="sxs-lookup"><span data-stu-id="3233b-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="3233b-114">Turite sukonfigūruoti šį procesą taip, kad šis veiktų dideliu dažnumu ir dokumentai būtų sukuriami operacijas įkėlus į būstinę per P užduotį.</span><span class="sxs-lookup"><span data-stu-id="3233b-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="3233b-115">Naudojant operacijų išrašą, kuris jau sukuria pardavimo užsakymus ir pardavimo sąskaitas faktūras, nėra realaus poreikio konfigūruoti paketinę užduotį **Registruoti atsargas**.</span><span class="sxs-lookup"><span data-stu-id="3233b-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="3233b-116">Tačiau ją vis tiek galite naudoti konkretiems verslo poreikiams patenkinti.</span><span class="sxs-lookup"><span data-stu-id="3233b-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="3233b-117">Finansinė ataskaita turi būti sukurta dienos pabaigoje, ji palaiko tik **Pamaina** uždarymo metodą.</span><span class="sxs-lookup"><span data-stu-id="3233b-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="3233b-118">Šis išrašas bus taikomas tik finansiniam suderinimui ir sukurs tik skirtingų mokėjimo priemonių apskaičiuotos sumos ir operacijos sumos skirtumo sumų žurnalus bei kitų grynųjų pinigų valdymo operacijų žurnalus.</span><span class="sxs-lookup"><span data-stu-id="3233b-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="3233b-119">Norėdami apskaičiuoti operacijų išrašą, eikite į **„Retail“ ir „Commerce“> „Retail“ ir „Commerce“ IT > EKA registravimas > Atlikti operacijų išrašų paketinį skaičiavimą**.</span><span class="sxs-lookup"><span data-stu-id="3233b-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="3233b-120">Norėdami atlikti paketinį operacijų išrašų registravimą, eikite į **„Retail“ ir „Commerce“ > „Retail“ ir „Commerce“ IT > EKA registravimas > Atlikti operacijų išrašų paketinį registravimą**.</span><span class="sxs-lookup"><span data-stu-id="3233b-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="3233b-121">Norėdami apskaičiuoti finansinę ataskaitą, eikite į **„Retail“ ir „Commerce“ > „Retail“ ir „Commerce“ IT > EKA registravimas > Atlikti finansinių ataskaitų paketinį skaičiavimą**.</span><span class="sxs-lookup"><span data-stu-id="3233b-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="3233b-122">Norėdami atlikti finansinių ataskaitų paketinį registravimą, eikite į **„Retail“ ir „Commerce“ > „Retail“ ir „Commerce“ IT > EKA registravimas > Registruoti finansines ataskaitas pakete**.</span><span class="sxs-lookup"><span data-stu-id="3233b-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="3233b-123">Iš šios naujos funkcijos pašalinti meniu elementai **„Retail“ ir „Commerce“ > „Retail“ ir „Commerce“ IT > EKA registravimas > Atlikti paketinį išrašų apskaičiavimą** ir **„Retail“ ir „Commerce“ > „Retail“ ir „Commerce“ IT > EKA registravimas > Atlikti paketinį išrašų registravimą**.</span><span class="sxs-lookup"><span data-stu-id="3233b-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="3233b-124">Operacijų ir finansinių ataskaitų tipus galima kurti ir neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="3233b-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="3233b-125">Eikite į **„Retail“ ir „Commerce“ > Kanalai > Parduotuvės** ir spustelėkite **Išrašai**.</span><span class="sxs-lookup"><span data-stu-id="3233b-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="3233b-126">Spustelėkite **Naujas** ir pasirinkite norimo sukurti išrašo tipą.</span><span class="sxs-lookup"><span data-stu-id="3233b-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="3233b-127">Puslapyje **Išrašai** esančiuose laukuose ir puslapyje **Išrašo grupė** esančiuose veiksmuose bus rodomi susiję duomenys ir veiksmai pagal pasirinktą išrašo tipą.</span><span class="sxs-lookup"><span data-stu-id="3233b-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>

---
title: Kryžminio tarifo nurodymas
description: Šioje temoje pateikiama informacija apie kryžminius tarifus programoje „Microsoft Dynamics 365 for Finance and Operations“.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9c2cba3ed655e2b4b1ada75bdbb5f01c300b25a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834540"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="15c29-103">Kryžminio tarifo nurodymas</span><span class="sxs-lookup"><span data-stu-id="15c29-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15c29-104">Šioje temoje paaiškinama kryžminio kurso paskirtis, ir kaip nurodyti kryžminį kursą sudengiant mokėjimą su SF.</span><span class="sxs-lookup"><span data-stu-id="15c29-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="15c29-105">Naudokite kryžminį kursą, kai taikomi visi šie kriterijai.</span><span class="sxs-lookup"><span data-stu-id="15c29-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="15c29-106">Sudengiate mokėjimą su SF.</span><span class="sxs-lookup"><span data-stu-id="15c29-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="15c29-107">Skirtingos valiutos naudojamos mokėjimo eilutėje ir SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="15c29-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="15c29-108">Nei viena valiuta nėra apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="15c29-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="15c29-109">Kryžminis tarifas nenaudojamas siekiant apskaičiuoti mokėjimo operacijos valiutos konvertavimo į mokėjimo apskaitos valiutą vertę.</span><span class="sxs-lookup"><span data-stu-id="15c29-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="15c29-110">Vietoj to, iš valiutos kursų lentelės nuskaitomi valiutos kursai, siekiant apskaičiuoti mokėjimo operacijos valiutos sumos vertę ir mokėjimo apskaitos valiutos sumos vertę.</span><span class="sxs-lookup"><span data-stu-id="15c29-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="15c29-111">Pavyzdžiui, apskaitos valiuta yra USD, SF valiuta – CAD, o mokėjimo valiuta – EUR.</span><span class="sxs-lookup"><span data-stu-id="15c29-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="15c29-112">Naudodami kryžminį kursą galite įvesti valiutos kursą – tuomet bus tiesiogiai konvertuojama iš CAD į EUR ir atvirkščiai, ir nebereikės konvertuoti naudojant USD.</span><span class="sxs-lookup"><span data-stu-id="15c29-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="15c29-113">Pasirinkdami SF ir pirminį mokėjimą, galite įvesti kryžminį kursą SF eilutei.</span><span class="sxs-lookup"><span data-stu-id="15c29-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="15c29-114">Kryžminis kursas yra valiutos kursas tarp dviejų valiutų, taikomas toms operacijoms sudengimo datą.</span><span class="sxs-lookup"><span data-stu-id="15c29-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="15c29-115">Eikite į vieną iš šių puslapių:</span><span class="sxs-lookup"><span data-stu-id="15c29-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="15c29-116">**Gautinos sumos > Bendra > Klientai > Visi klientai**</span><span class="sxs-lookup"><span data-stu-id="15c29-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="15c29-117">**Mokėtinos sumos > Bendra > Tiekėjai > Visi tiekėjai**</span><span class="sxs-lookup"><span data-stu-id="15c29-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="15c29-118">**Paraiškos > Bendra > Tiekėjai > Visi tiekėjai**</span><span class="sxs-lookup"><span data-stu-id="15c29-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="15c29-119">Pasirinkite klientą arba tiekėją, kurio atviras operacijas sudengiate.</span><span class="sxs-lookup"><span data-stu-id="15c29-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="15c29-120">Pasirinkę klientą, sąrašo **Visi klientai** puslapyje eikite į **Surinkimas > Sudengti atidarytas operacijas**.</span><span class="sxs-lookup"><span data-stu-id="15c29-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="15c29-121">Pasirinkę tiekėją, sąrašo **Visi tiekėjai** puslapyje eikite į **Sąskaita faktūra > Sudengti atidarytas operacijas**.</span><span class="sxs-lookup"><span data-stu-id="15c29-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="15c29-122">Pasirinkite operaciją, kuri yra pirminis mokėjimas, ir spustelėkite **Pažymėti mokėjimą**.</span><span class="sxs-lookup"><span data-stu-id="15c29-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="15c29-123">Pažymimas žymės langelis stulpelyje **Pažymėti**, o stulpelyje **Pirminis mokėjimas** rodoma informacijos piktograma.</span><span class="sxs-lookup"><span data-stu-id="15c29-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="15c29-124">Lauke **Kryžminis tarifas** įveskite valiutos kursą, kuris sudengimo datą taikomas tarp SF valiutos ir mokėjimo valiutos.</span><span class="sxs-lookup"><span data-stu-id="15c29-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 

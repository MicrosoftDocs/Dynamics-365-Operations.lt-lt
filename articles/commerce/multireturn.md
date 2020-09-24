---
title: Kelių klientų užsakymų ir sąskaitų faktūrų grąžinamos prekės
description: Šioje temoje aprašomos funkcijos, padedančios atlikti kelių klientų užsakymų ir SF grąžinimus „Dynamics 365 Commerce“.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760255"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="aeff5-103">Kelių klientų užsakymų ir sąskaitų faktūrų grąžinamos prekės</span><span class="sxs-lookup"><span data-stu-id="aeff5-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="aeff5-104">Šiame straipsnyje aprašomos dvi funkcijos, optimizuojančios kliento užsakymų grąžinimą naudojant kelias sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="aeff5-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="aeff5-105">Įjungti grąžinimą už kelis patvirtinimus</span><span class="sxs-lookup"><span data-stu-id="aeff5-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="aeff5-106">Šia funkcija įgalinami keli susieti to paties kliento užsakymo grąžinimai.</span><span class="sxs-lookup"><span data-stu-id="aeff5-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="aeff5-107">Eikite į darbo sritį **Funkcijų valdymas**ir ieškokite **Įjungti grąžinimą už kelis patvirtinimus**.</span><span class="sxs-lookup"><span data-stu-id="aeff5-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="aeff5-108">Pasirinkite **Įjungti grąžinimą už kelis užsakymus** ir spustelėkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="aeff5-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="aeff5-109">Įjungti tinkamą mokesčių skaičiavimą, kai grąžinamas dalinis kiekis</span><span class="sxs-lookup"><span data-stu-id="aeff5-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="aeff5-110">Šia funkcija užtikrinama, kad užsakymą grąžinus naudojant kelias sąskaitas faktūras, galiausiai mokesčiai bus lygūs pirminei mokėtinai mokesčių sumai.</span><span class="sxs-lookup"><span data-stu-id="aeff5-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="aeff5-111">Eikite į darbo sritį **Funkcijų valdymas** ir ieškokite **Įjungti tinkamą mokesčių skaičiavimą, kai grąžinamas dalinis kiekis**.</span><span class="sxs-lookup"><span data-stu-id="aeff5-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="aeff5-112">Pasirinkite **Įjungti tinkamą mokesčių skaičiavimą, kai grąžinamas dalinis kiekis** ir spustelėkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="aeff5-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="aeff5-113">Grąžinimų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="aeff5-113">Process returns</span></span>

<span data-ttu-id="aeff5-114">Įjungus šias funkcijas ir pakeitimus sinchronizavus su parduotuvėmis, parduotuvės kasininkas gali pasirinkti kelis kliento pardavimo užsakymus dėl grąžinimo.</span><span class="sxs-lookup"><span data-stu-id="aeff5-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="aeff5-115">Pasirinkus užsakymus, bus parodytas visų grąžintinų produktų iš visų užsakymų SF sąrašas.</span><span class="sxs-lookup"><span data-stu-id="aeff5-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="aeff5-116">Tada kasininkas gali pasirinkti grąžintinus produktus.</span><span class="sxs-lookup"><span data-stu-id="aeff5-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="aeff5-117">Sukuriamas vienas grąžinimo užsakymas visiems pasirinktiems produktams.</span><span class="sxs-lookup"><span data-stu-id="aeff5-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="aeff5-118">Jei grąžintas visas užsakymas, klientui grąžinta mokesčių suma bus lygi pirminei mokėtinai mokesčių sumai.</span><span class="sxs-lookup"><span data-stu-id="aeff5-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>


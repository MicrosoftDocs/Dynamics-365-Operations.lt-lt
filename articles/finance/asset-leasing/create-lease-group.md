---
title: Nuomos grupės kūrimas
description: Šioje temoje paaiškinama, kaip nustatyti nuomos grupes. Norint sukurti naują nuomą, reikalingos nuomos grupės.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2c06f6f943c8a47fbe650a67017b95d799914a0e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971358"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="98858-104">Nuomos grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="98858-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98858-105">Šioje temoje paaiškinama, kaip nustatyti nuomos grupes.</span><span class="sxs-lookup"><span data-stu-id="98858-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="98858-106">Norint sukurti naują nuomą, reikalingos nuomos grupės.</span><span class="sxs-lookup"><span data-stu-id="98858-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="98858-107">Su kiekviena nuomos grupe susiejamos nuomos knygos.</span><span class="sxs-lookup"><span data-stu-id="98858-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="98858-108">Nuomos knygos nustato numatytąsias knygas, kurias reikia sukurti kiekvienai nuomai.</span><span class="sxs-lookup"><span data-stu-id="98858-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="98858-109">Galite priskirti konkrečių nuomos grupės sąskaitų puslapyje **Nuomos registravimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="98858-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="98858-110">Nuomos knygos sukūrimas ir nuomos grupės įtraukimas</span><span class="sxs-lookup"><span data-stu-id="98858-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="98858-111">Eikite į **Turto nuoma \> Sąranka \> Nuomos grupės**.</span><span class="sxs-lookup"><span data-stu-id="98858-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="98858-112">Veiksmų srityje pasirinkite **Nauja**, norėdami įtraukti nuomos grupę.</span><span class="sxs-lookup"><span data-stu-id="98858-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="98858-113">Eilutė pridedama prie tinklelio.</span><span class="sxs-lookup"><span data-stu-id="98858-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="98858-114">Naujoje eilutėje, esančioje lauke **Nuomos grupė**, įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="98858-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="98858-115">Lauke **Aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="98858-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="98858-116">Informacija, kurią ką tik įvedėte, įtraukiama į puslapio **Nuomos įtraukimas** lauką **Nuomos grupė**.</span><span class="sxs-lookup"><span data-stu-id="98858-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="98858-117">Knygos susiejimas su nuomos grupe</span><span class="sxs-lookup"><span data-stu-id="98858-117">Associate a book with a lease group</span></span>

<span data-ttu-id="98858-118">Sukūrę nuomos grupes, kiekvienai grupei galite priskirti knygų.</span><span class="sxs-lookup"><span data-stu-id="98858-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="98858-119">Kai kuriate nuomą ir priskiriate ją nuomos grupei, sistema sukuria kiekvienos knygos, susietos su ta nuomos grupe, grafikų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="98858-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="98858-120">Prieš priskiriant knygas nuomos grupei, jas reikia nustatyti.</span><span class="sxs-lookup"><span data-stu-id="98858-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="98858-121">Eikite į **Turto nuoma \> Sąranka \> Nuomos grupė**.</span><span class="sxs-lookup"><span data-stu-id="98858-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="98858-122">Pasirinkite nuomos grupę ir **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="98858-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="98858-123">Pasirinkite **Nauja**, tada lauke **Knygos tipas** pasirinkite knygą, kuri bus priskirta nuomos grupei.</span><span class="sxs-lookup"><span data-stu-id="98858-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="98858-124">Galite priskirti keletą knygų nuomos grupei, jei nuoma turi būti apskaitoma skirtingais būdais.</span><span class="sxs-lookup"><span data-stu-id="98858-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>

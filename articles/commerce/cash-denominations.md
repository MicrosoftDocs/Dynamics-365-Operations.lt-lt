---
title: Grynųjų pinigų nominaliųjų verčių konfigūracija, skirta elektroniniam kasos aparatui (EKA)
description: Grynųjų pinigų nominaliosios vertės banknotams ir monetoms gali būti nurodomi operacijų skyriuje, kurį naudos kasininkai, pardavimo darbuotojai ir vadybininkai parduotuvėje per EKA.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a34ae8084c0ad55221f4ab93eb8c6481fa8c4771
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023383"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a><span data-ttu-id="df731-103">Grynųjų pinigų nominaliųjų verčių konfigūracija, skirta elektroniniam kasos aparatui (EKA)</span><span class="sxs-lookup"><span data-stu-id="df731-103">Configure cash denominations for the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="df731-104">Grynųjų pinigų nominaliosios vertės banknotams ir monetoms gali būti nurodomi operacijų skyriuje, kurį naudos kasininkai, pardavimo darbuotojai ir vadybininkai parduotuvėje per EKA.</span><span class="sxs-lookup"><span data-stu-id="df731-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="df731-105">Šias nominaliąsias vertes galima naudoti skaičiuojant grynuosius dienos pabaigos mokėjimų deklaravimams arba greitai taikant mokėjimą pardavimui.</span><span class="sxs-lookup"><span data-stu-id="df731-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="df731-106">Nominaliųjų verčių apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="df731-106">Define denominations</span></span>

<span data-ttu-id="df731-107">Nominaliųjų verčių apibrėžimai nustatomi kiekvienai parduotuvei atskirai parduotuvės ypatybių puslapyje pasirinkus parinktį **Nustatyti** \> **Grynųjų pinigų deklaravimas**.</span><span class="sxs-lookup"><span data-stu-id="df731-107">The denominations are set up per store on the **Set up** \> **Cash declaration** option from the store property page.</span></span>

![Parinktis Grynųjų pinigų deklaravimas](./media/image1-denomination.png)

<span data-ttu-id="df731-109">Norėdami apibrėžti nominaliąsias vertes</span><span class="sxs-lookup"><span data-stu-id="df731-109">To define a denomination:</span></span>

1. <span data-ttu-id="df731-110">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="df731-110">Click **New**.</span></span>
1. <span data-ttu-id="df731-111">Nurodykite tipą (monetos arba banknotai).</span><span class="sxs-lookup"><span data-stu-id="df731-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="df731-112">Nurodykite sumą (vertę).</span><span class="sxs-lookup"><span data-stu-id="df731-112">Specify the amount (value).</span></span>

![Puslapis Deklaruotų grynųjų pinigų nominalioji vertė](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="df731-114">Funkcijų šablono konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="df731-114">Configure the functionality profile</span></span>

<span data-ttu-id="df731-115">Mokant grynaisiais pinigais EKA, vartotojas gali naudoti banknotų nominaliąsias vertes, kad galėtų greitai vesti kliento mokamą sumą.</span><span class="sxs-lookup"><span data-stu-id="df731-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="df731-116">Funkcijų šablone galima konfigūruoti dvi pasirinktis, nurodančias nominaliąsias vertes EKA.</span><span class="sxs-lookup"><span data-stu-id="df731-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

- <span data-ttu-id="df731-117">**Didesnė arba lygi mokėtina suma** – pagal numatytuosius nustatymus EKA bus rodomos tik nominaliosios vertės, kurios yra didesnės už mokamą sumą, kad būtų galima mokėti vienu palietimu.</span><span class="sxs-lookup"><span data-stu-id="df731-117">**Greater or equal to amount due** – By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="df731-118">Jeigu mokėtina suma yra $7,50, EKA rodys šias nominaliąsias vertes: $10, $20, $50 ir $100.</span><span class="sxs-lookup"><span data-stu-id="df731-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="df731-119">Palietus bet kurią iš šių sumų bus automatiškai sukuriamas tos sumos pardavimo mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="df731-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="df731-120">$1 ir $5 vertės nėra rodomos, nes šios sumos yra mažesnės nei mokėtina suma.</span><span class="sxs-lookup"><span data-stu-id="df731-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>
- <span data-ttu-id="df731-121">**Visos nominaliosios vertės** – pasirinkite šią pasirinktį norėdami visada matyti banknotų nominaliąsias vertes EKA, neatsižvelgiant į mokėtiną sumą.</span><span class="sxs-lookup"><span data-stu-id="df731-121">**All denominations** – Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="df731-122">Tai reiškia, kad vartotojas gali naudoti banknotų derinius, kad pasiektų mokėtiną sumą.</span><span class="sxs-lookup"><span data-stu-id="df731-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="df731-123">Pavyzdžiui, jei mokėtina suma yra $25,00, vartotojas gali pasirinkti $20 ir $5, kad užbaigtų pardavimą.</span><span class="sxs-lookup"><span data-stu-id="df731-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>
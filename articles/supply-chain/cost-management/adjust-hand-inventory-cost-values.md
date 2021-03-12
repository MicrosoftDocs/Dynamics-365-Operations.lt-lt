---
title: Turimų atsargų išlaidų verčių koregavimas
description: Naudokite puslapį „Turimų atsargų koregavimas“, kad koreguotumėte turimų atsargų kiekių savikainos vertę po atsargų uždarymo proceso.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a702a083d60bdb289712027fbaee5c0a72e60cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963843"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="386ba-103">Turimų atsargų išlaidų verčių koregavimas</span><span class="sxs-lookup"><span data-stu-id="386ba-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="386ba-104">Naudokite puslapį „Turimų atsargų koregavimas“, kad koreguotumėte turimų atsargų kiekių savikainos vertę po atsargų uždarymo proceso.</span><span class="sxs-lookup"><span data-stu-id="386ba-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="386ba-105">Galite naudoti puslapį **Turimų atsargų koregavimas**, kad koreguotumėte turimų atsargų kiekių savikainos vertę po atsargų uždarymo proceso.</span><span class="sxs-lookup"><span data-stu-id="386ba-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="386ba-106">**Pastaba:** norėdami atidaryti puslapį **Turimų atsargų koregavimas** puslapyje **Uždarymas ir koregavimas** pasirinkite užbaigto atsargų uždarymo proceso įrašą ir spustelėkite **Koregavimas** &gt; **Turimos atsargos**.</span><span class="sxs-lookup"><span data-stu-id="386ba-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="386ba-107">**Pavyzdys:** vasario mėnesį atliktos tokios operacijos:</span><span class="sxs-lookup"><span data-stu-id="386ba-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="386ba-108">Vasario 1 d.: 2 vienetų, kurių savaikaina 10,00 USD, finansinis gavimas į atsargas</span><span class="sxs-lookup"><span data-stu-id="386ba-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="386ba-109">Vasario 5 d.: 1 vieneto, kurio kaina 13,00 USD, finansinis gavimas į atsargas</span><span class="sxs-lookup"><span data-stu-id="386ba-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="386ba-110">Vasario 19 d.: 1 vieneto, kurio einamoji vidurkio savikaina 11 USD, finansinis išdavimas iš atsargų</span><span class="sxs-lookup"><span data-stu-id="386ba-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="386ba-111">Ši prekė buvo nustatyta su „pirmasis į, pirmasis iš“ (FIFO) atsargų modeliu, o atsargų uždarymas buvo atliktas vasario 28 d.</span><span class="sxs-lookup"><span data-stu-id="386ba-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="386ba-112">11,00 USD vertės finansinio išdavimo operacija bus sudengta su finansiniu vasario mėn. 1 d. gavimu ir bus atliktas 1,00 USD vertės koregavimas.</span><span class="sxs-lookup"><span data-stu-id="386ba-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="386ba-113">Tada toliau pateikiamuose atsargų gavimuose bus atvirų atsargų kiekių:</span><span class="sxs-lookup"><span data-stu-id="386ba-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="386ba-114">Vasario 1 d.: 1 vienetas, kurio kaina 10,00 USD</span><span class="sxs-lookup"><span data-stu-id="386ba-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="386ba-115">Vasario 5 d.: 1 vienetas, kurio kaina 13,00 USD</span><span class="sxs-lookup"><span data-stu-id="386ba-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="386ba-116">Norėdami nustatyti šių dviejų prekių kainą į 15,00 USD, naudokite turimą koregavimo pasirinktį, kad pakoreguotumėte po paskutinio atsargų uždarymo laikotarpio turimus atvirus kiekius.</span><span class="sxs-lookup"><span data-stu-id="386ba-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="386ba-117">**Pastaba:** turimo kiekio koregavimo operacijos registravimo data bus paskutinio atsargų uždarymo data.</span><span class="sxs-lookup"><span data-stu-id="386ba-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="386ba-118">Šios datos modifikuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="386ba-118">This date can't be modified.</span></span>

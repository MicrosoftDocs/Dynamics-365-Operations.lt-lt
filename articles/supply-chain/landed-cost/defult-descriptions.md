---
title: Numatytieji didžiosios knygos aprašai
description: Numatytuosius aprašus galima naudoti laukeliui „Aprašas“ atnaujinti DK kvitų registracijose.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 25dd72c86b22b50eccef22a5d2cbcfcf04280684
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021617"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="ad4db-103">Numatytieji didžiosios knygos aprašai</span><span class="sxs-lookup"><span data-stu-id="ad4db-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad4db-104">Numatytuosius aprašus galima naudoti laukeliui **Aprašas** atnaujinti DK kvitų registracijose.</span><span class="sxs-lookup"><span data-stu-id="ad4db-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="ad4db-105">Ši funkcija patobulinta darbui su iškrovimo kaina.</span><span class="sxs-lookup"><span data-stu-id="ad4db-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="ad4db-106">Kad nustatytumėte DK registracijų numatytuosius aprašus, eikite į **Organizacijos administravimas \> Sąranka \> Numatytieji aprašai**.</span><span class="sxs-lookup"><span data-stu-id="ad4db-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="ad4db-107">Šioje lentelėje pateikiamas naujų verčių, kurios buvo pridėtos laukelyje **Aprašas**, vertės puslapyje **Numatytieji aprašai** iškrovimo kainai palaikyti.</span><span class="sxs-lookup"><span data-stu-id="ad4db-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="ad4db-108">Aprašo tipas</span><span class="sxs-lookup"><span data-stu-id="ad4db-108">Description type</span></span> | <span data-ttu-id="ad4db-109">Pastabos</span><span class="sxs-lookup"><span data-stu-id="ad4db-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="ad4db-110">Importavimo įkainojimas – savikainos kaupimas</span><span class="sxs-lookup"><span data-stu-id="ad4db-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="ad4db-111">Pirkimo užsakyme užregistravus SF, savikainos kaupimas apdorojimas vertinamai reiso savikainai.</span><span class="sxs-lookup"><span data-stu-id="ad4db-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="ad4db-112">Galima nurodyti prie reiso numerio aprašo pridėti numatytuosius aprašus.</span><span class="sxs-lookup"><span data-stu-id="ad4db-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="ad4db-113">Siuntos numeriui naudokite *%4*.</span><span class="sxs-lookup"><span data-stu-id="ad4db-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="ad4db-114">Importavimo įkainojimas – tranzito prekių užsakymas</span><span class="sxs-lookup"><span data-stu-id="ad4db-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="ad4db-115">Jei naudojate tranzitinį apdorojimą, užregistruojama pirkimo užsakymo SF, o prekės registruojamos tranzito prekių sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="ad4db-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="ad4db-116">Galima nurodyti prie tranzito užsakymo numerio aprašo pridėti numatytuosius aprašus.</span><span class="sxs-lookup"><span data-stu-id="ad4db-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="ad4db-117">Kaip tranzito užsakymo numerį naudokite *%4*.</span><span class="sxs-lookup"><span data-stu-id="ad4db-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="ad4db-118">Atsargos – Uždarymas – Koregavimas</span><span class="sxs-lookup"><span data-stu-id="ad4db-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="ad4db-119">Kai mokėtinų sumų (MS) SF apdorojama reiso savikainai, atsargų koregavimas apdorojamas reiso savikainai įvertinti.</span><span class="sxs-lookup"><span data-stu-id="ad4db-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="ad4db-120">Galima nurodyti prie reiso numerio aprašo pridėti numatytuosius aprašus.</span><span class="sxs-lookup"><span data-stu-id="ad4db-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="ad4db-121">Siuntos numeriui naudokite *%4*.</span><span class="sxs-lookup"><span data-stu-id="ad4db-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="ad4db-122">Daugiau informacijos apie tai, kaip dirbti su puslapiu **Numatytieji aprašai**, žr. [Numatytųjų aprašų nustatymas automatiniam registravimui](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="ad4db-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>

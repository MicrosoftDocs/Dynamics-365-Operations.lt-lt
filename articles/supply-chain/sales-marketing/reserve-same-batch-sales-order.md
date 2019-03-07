---
title: To paties pardavimo užsakymo paketo rezervavimas
description: Šiame straipsnyje paaiškinta, kaip nustatyti produktą, kad būtų leidžiamas atsargų rezervavimas pagal vieną atsargų paketą.
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d6089d07b0f8bc1a36703b5b1c2f24af72770d5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "309546"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="61553-103">To paties pardavimo užsakymo paketo rezervavimas</span><span class="sxs-lookup"><span data-stu-id="61553-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61553-104">Šiame straipsnyje paaiškinta, kaip nustatyti produktą, kad būtų leidžiamas atsargų rezervavimas pagal vieną atsargų paketą.</span><span class="sxs-lookup"><span data-stu-id="61553-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="61553-105">To paties paketo rezervavimas leidžia pardavimo užsakymo eilutės atsargas rezervuoti pagal vieną atsargų paketą.</span><span class="sxs-lookup"><span data-stu-id="61553-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="61553-106">Pvz., klientas, kuris užsisako tapetų, gali reikalauti, kad visas užsakymas būtų užpildytas iš to pačio paketo ar partijos, kad būtų išvengta rulonų neatitikimų.</span><span class="sxs-lookup"><span data-stu-id="61553-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="61553-107">Norint nustatyti, kad su produktu būtų naudojamas to paties paketo rezervavimas, prekių modelių grupėje, sekimo dimensijų grupėje ir saugojimo dimensijų grupėje, kurias priskiriate produktui, turi būti aktyvios tolesnės nuostatos.</span><span class="sxs-lookup"><span data-stu-id="61553-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="61553-108">**Prekių modelių grupės** – prekių modelių grupėje turi būti pasirinkti atsargų strategijų laukų grupės **Rezervavimas** laukai **To paties paketo parinkimas** ir **Konsoliduoti reikalavimą**.</span><span class="sxs-lookup"><span data-stu-id="61553-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="61553-109">**Sekimo dimensijų grupės** – sekimo dimensijų grupėje turi būti pasirinktas paketo numerio laukas **Padengimo planas pagal dimensiją**.</span><span class="sxs-lookup"><span data-stu-id="61553-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="61553-110">**Saugojimo dimensijų grupės** – saugojimo dimensijų grupėje turi būti pasirinktas **Teritorijos** ir **Sandėlio** laukas **Padengimo planas pagal dimensiją**.</span><span class="sxs-lookup"><span data-stu-id="61553-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="61553-111">Kai produkto atsargas rezervuojate pardavimo užsakymo eilutėje, su kuria nustatyta naudoti to paties paketo parinkimą, „Microsoft Dynamics 365 for Finance and Operations“ užsakytą kiekį bando rezervuoti iš vieno atsargų paketo.</span><span class="sxs-lookup"><span data-stu-id="61553-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="61553-112">Taip pat atsižvelgiama į visus konkrečius paketo atributo reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="61553-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="61553-113">Jei kiekio iš vieno paketo užpildyti negalima, rodomas puslapis **To paties paketo rezervavimo nesuderinamumas**.</span><span class="sxs-lookup"><span data-stu-id="61553-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="61553-114">Šiame puslapyje apibūdinamos problemos bei veiksmai, kuriuos galite atlikti norėdami tęsti rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="61553-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="61553-115">Paketas gali būti nerezervuojamas esant tolesnėms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="61553-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="61553-116">Paketo perdavimo kodo pardavimo parinktis **Blokuoti rezervavimą** pažymėta kaip **Užblokuota**.</span><span class="sxs-lookup"><span data-stu-id="61553-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="61553-117">Paketas baigė galioti pagal galiojimo pabaigos datą ir bet kokias taikomas klientų pardavimo dienas.</span><span class="sxs-lookup"><span data-stu-id="61553-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="61553-118">Prekė vis dar gali būti svarstytina rezervuoti, jei prekės modelių grupė yra data valdomas rezervavimas „pirmas baigė galioti – pirmas baigėsi“ (FEFO) ir jei kaip paėmimo kriterijus pasirinkta galiojimo pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="61553-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="61553-119">Liko nepakankamai paketo galiojimo dienų, atsižvelgiant į galiojimo pabaigos datą ir geriausia iki datą bei visas kliento pardavimo dienas.</span><span class="sxs-lookup"><span data-stu-id="61553-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>





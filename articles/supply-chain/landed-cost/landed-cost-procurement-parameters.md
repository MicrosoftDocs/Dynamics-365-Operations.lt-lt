---
title: Modulio Iškrovimo kaina įsigijimo ir šaltinio parinkimo parametrai
description: Šioje temoje aprašoma, kaip nustatyti tinkamus įsigijimo ir šaltinio parinkimo parametrus, kai naudojamas modulis Iškrovimo kaina.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: df91fcb97794be32924707fcecf2b5fb34844596
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833934"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="59a41-103">Modulio Iškrovimo kaina įsigijimo ir šaltinio parinkimo parametrai</span><span class="sxs-lookup"><span data-stu-id="59a41-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59a41-104">Puslapyje **Įsigijimo ir šaltinio parinkimo parametrai** yra keletą parametrų, kurie ypač svarbūs naudojant modulį **Iškrovimo kaina**.</span><span class="sxs-lookup"><span data-stu-id="59a41-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="59a41-105">Naudokite dialogo langą **Atnaujinti užsakymo eilutes**, atidarytą puslapyje **Įsigijimo ir šaltinio parinkimo parametrai**, norėdami nurodyti, ar pirkimo užsakymo eilutės turėtų būti automatiškai atnaujinamos, kai pirkimo užsakymo antraštėje atliekami pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="59a41-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="59a41-106">Norėdami užbaigti šią sąranką, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="59a41-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="59a41-107">Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Sąranka \> Įsigijimo ir šaltinio pasirinkimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="59a41-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="59a41-108">Skirtuke **Bendra** pasirinkite saitą **Atnaujinti užsakymo eilutes**.</span><span class="sxs-lookup"><span data-stu-id="59a41-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="59a41-109">Dialogo lange **Atnaujinti užsakymo eilutes** išvardyti užsakymo antraštės laukai, kurie taip pat gali taikyti automatinius naujinimus susijusiems užsakymo eilučių laukams.</span><span class="sxs-lookup"><span data-stu-id="59a41-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="59a41-110">Nustatykite kiekvieną sąrašo lauką į vieną iš toliau pateiktų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="59a41-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="59a41-111">**Visada** – atnaujinus užsakymo antraštę, užsakymo eilutės atnaujinamos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="59a41-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="59a41-112">**Niekada** – atnaujinus užsakymo antraštę, užsakymo eilutės niekada nėra atnaujinamos.</span><span class="sxs-lookup"><span data-stu-id="59a41-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="59a41-113">**Raginimas** – vartotojas bus paragintas pasirinkti, ar reikia atnaujinti užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="59a41-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>

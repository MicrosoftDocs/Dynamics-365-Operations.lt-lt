---
title: Modulio Iškrovimo kaina įsigijimo ir šaltinio parinkimo parametrai
description: Šioje temoje aprašoma, kaip nustatyti tinkamus įsigijimo ir šaltinio parinkimo parametrus, kai naudojamas modulis Iškrovimo kaina.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccda3bd769a646e2390711883b8e40bec50e4d6a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020988"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="8c37b-103">Modulio Iškrovimo kaina įsigijimo ir šaltinio parinkimo parametrai</span><span class="sxs-lookup"><span data-stu-id="8c37b-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c37b-104">Puslapyje **Įsigijimo ir šaltinio parinkimo parametrai** yra keletą parametrų, kurie ypač svarbūs naudojant modulį **Iškrovimo kaina**.</span><span class="sxs-lookup"><span data-stu-id="8c37b-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="8c37b-105">Naudokite dialogo langą **Atnaujinti užsakymo eilutes**, atidarytą puslapyje **Įsigijimo ir šaltinio parinkimo parametrai**, norėdami nurodyti, ar pirkimo užsakymo eilutės turėtų būti automatiškai atnaujinamos, kai pirkimo užsakymo antraštėje atliekami pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="8c37b-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="8c37b-106">Norėdami užbaigti šią sąranką, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8c37b-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="8c37b-107">Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Sąranka \> Įsigijimo ir šaltinio pasirinkimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="8c37b-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="8c37b-108">Skirtuke **Bendra** pasirinkite saitą **Atnaujinti užsakymo eilutes**.</span><span class="sxs-lookup"><span data-stu-id="8c37b-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="8c37b-109">Dialogo lange **Atnaujinti užsakymo eilutes** išvardyti užsakymo antraštės laukai, kurie taip pat gali taikyti automatinius naujinimus susijusiems užsakymo eilučių laukams.</span><span class="sxs-lookup"><span data-stu-id="8c37b-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="8c37b-110">Nustatykite kiekvieną sąrašo lauką į vieną iš toliau pateiktų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="8c37b-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="8c37b-111">**Visada** – atnaujinus užsakymo antraštę, užsakymo eilutės atnaujinamos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="8c37b-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="8c37b-112">**Niekada** – atnaujinus užsakymo antraštę, užsakymo eilutės niekada nėra atnaujinamos.</span><span class="sxs-lookup"><span data-stu-id="8c37b-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="8c37b-113">**Raginimas** – vartotojas bus paragintas pasirinkti, ar reikia atnaujinti užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="8c37b-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>

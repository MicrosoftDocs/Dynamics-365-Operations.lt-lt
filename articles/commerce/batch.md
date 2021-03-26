---
title: Patobulintas pagal paketą sekamų prekių tvarkymas
description: Šioje temoje aprašoma, kaip patobulintas pagal paketą sekamų prekių paketų tvarkymas atliekant išrašo registravimo procesą.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 00e1fcb36d685798f3ad7d667805c97bddcceb36
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211158"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="20bfe-103">Patobulintas pagal paketą sekamų prekių tvarkymas</span><span class="sxs-lookup"><span data-stu-id="20bfe-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="20bfe-104">Elektroniniame kasos aparate (EKA) parduodant pagal paketą sekamas prekes jų paketų numerių užfiksuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="20bfe-104">In Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="20bfe-105">Tačiau, naudojant tam tikras konfigūracijas, kai pardavimai būstinėje registruojami per klientų užsakymus arba registruojant išrašus, „Microsoft Dynamics“ sistema tikisi, kad egzistuoja galiojantys pagal paketą sekamų prekių paketų numeriai ir kad jie bus naudojami atliekant SF išrašymo procesą.</span><span class="sxs-lookup"><span data-stu-id="20bfe-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="20bfe-106">Jei egzistuoja galiojantys produktų paketų numeriai, jie naudojami atliekant klientų užsakymų SF išrašymo procesą ir pardavimo užsakymų SF išrašymo procesą, kai registruojami išrašai.</span><span class="sxs-lookup"><span data-stu-id="20bfe-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="20bfe-107">Kitu atveju atliekant klientų užsakymų SF išrašymo procesą negalima registruoti, o EKA vartotojas gauna klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="20bfe-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="20bfe-108">Išrašų registravimas tada tampa klaidos būsenos.</span><span class="sxs-lookup"><span data-stu-id="20bfe-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="20bfe-109">Ši klaidos būsena atsiranda net tada, kai įjungtos produktų neigiamos atsargos.</span><span class="sxs-lookup"><span data-stu-id="20bfe-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="20bfe-110">„Retail“ 10.0.4 ir naujesnėse versijose atlikti patobulinimai padeda užtikrinti, kad, kai yra įjungtos pagal paketą sekamų prekių neigiamos atsargos, toms prekėms klientų užsakymų SF išrašymas ir pardavimo užsakymų SF išrašymas registruojant išrašus nebūtų blokuojamas, jei atsargos yra 0 (nulis) arba nėra paketo numerio.</span><span class="sxs-lookup"><span data-stu-id="20bfe-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="20bfe-111">Kai nėra paketų numerių, naujoji funkcija pardavimo eilutėms naudoja numatytąjį paketo ID.</span><span class="sxs-lookup"><span data-stu-id="20bfe-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="20bfe-112">Norėdami nustatyti numatytąjį paketo ID, naudojamą klientų užsakymuose, puslapio **Prekybos parametrai** skirtuko **Klientų užsakymai** „FastTab“ konteineryje **Užsakymas** nustatykite lauką **Numatytasis paketo ID**.</span><span class="sxs-lookup"><span data-stu-id="20bfe-112">To define the default batch ID that is used for customer orders, on the **Commerce parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="20bfe-113">Norėdami nustatyti numatytąjį paketo ID, kuris yra naudojamas, kai registruojant išrašus išrašomos pardavimo užsakymų sąskaitos faktūros, puslapio **Prekybos parametrai** skirtuko **Registravimas** „FastTab“ konteineryje **Atsargų atnaujinimas** nustatykite lauką **Numatytasis paketo ID**.</span><span class="sxs-lookup"><span data-stu-id="20bfe-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Commerce parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="20bfe-114">Šią funkciją galima naudoti tik tada, kai konkrečiam parduotuvės sandėliui ir prekėms įjungtas pažangus sandėliavimas.</span><span class="sxs-lookup"><span data-stu-id="20bfe-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="20bfe-115">Naujesniame leidime ši funkcija taip pat bus palaikoma situacijose, kai pažangus sandėlių valdymas nenaudojamas.</span><span class="sxs-lookup"><span data-stu-id="20bfe-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="20bfe-116">„Retail” 10.0.5 versijoje įvestas patobulinto pagal paketą sekamų prekių tvarkymo palaikymas atliekant neišplėstinių sandėlių valdymo scenarijų išrašų tvarkymą.</span><span class="sxs-lookup"><span data-stu-id="20bfe-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
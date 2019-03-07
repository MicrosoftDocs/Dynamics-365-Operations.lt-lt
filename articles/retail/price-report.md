---
title: Mažmeninės kainos ataskaitos
description: Šioje temoje apžvelgiama kainų ataskaitos funkcija, kurią galima naudoti norint peržiūrėti būsimus pateiktų produktų kainų pokyčius.
author: shajain
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 6db6d1c6b6eb1d69b40fe75d97eeb71564986707
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "353062"
---
# <a name="retail-price-reports"></a><span data-ttu-id="19c14-103">Mažmeninės kainos ataskaitos</span><span class="sxs-lookup"><span data-stu-id="19c14-103">Retail price reports</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]


<span data-ttu-id="19c14-104">Siekdami teikti konkurencingas kainas savo klientams, mažmenininkai dažnai keičia produktų kainas.</span><span class="sxs-lookup"><span data-stu-id="19c14-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="19c14-105">Parduotuvių vadovai nori galimybės lengvai pasiekti nesenus arba būsimus kainų pakeitimus, kad jie galėtų suplanuoti, jog reikiami ištekliai atnaujintų kainų etiketes, rodomas parduotuvės lentynose.</span><span class="sxs-lookup"><span data-stu-id="19c14-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="19c14-106">Išleidus „Dynamics 365 for Retail 10.0“, parduotuvės vadovas gali atidaryti ataskaitą **Kaina** pasirinkęs **Visos mažmeninės prekybos parduotuves \> Parduotuvė \> Kainų ataskaita** ir peržiūrėti atnaujintų su parduotuve susietų produktų kainas.</span><span class="sxs-lookup"><span data-stu-id="19c14-106">With release 10.0 of Dynamics 365 for Retail, a store manager can open the **Price** report by navigating to **All retail stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="19c14-107">Norėdami įjungti kainų ataskaitą, turite įjungti parametrą **Įjungti mažmeninės prekybos parduotuvės kainų ataskaitą**.</span><span class="sxs-lookup"><span data-stu-id="19c14-107">To enable the price report, the **Enable price report for Retail store** parameter must be turned on.</span></span> <span data-ttu-id="19c14-108">Šis parametras pateiktas skirtuke **Mažmeninės prekybos parametrai \> Nuolaidos \> Įvairios**. Atidarius puslapį **Kainų ataskaita** rodomas dialogo langas ir įvairios konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="19c14-108">This parameter is located on the **Retail parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="19c14-109">Galimos konfigūracijos pateiktos toliau.</span><span class="sxs-lookup"><span data-stu-id="19c14-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="19c14-110">Konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="19c14-110">Configuration</span></span> | <span data-ttu-id="19c14-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="19c14-111">Description</span></span> |
|---|---|
| <span data-ttu-id="19c14-112">Pradžios data / pabaigos data</span><span class="sxs-lookup"><span data-stu-id="19c14-112">From date / To date</span></span>| <span data-ttu-id="19c14-113">Generuotinos kainų ataskaitos datų intervalas.</span><span class="sxs-lookup"><span data-stu-id="19c14-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="19c14-114">Šiuo metu trukmė apribota iki 7 dienų.</span><span class="sxs-lookup"><span data-stu-id="19c14-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="19c14-115">Kanalas</span><span class="sxs-lookup"><span data-stu-id="19c14-115">Channel</span></span>| <span data-ttu-id="19c14-116">Generuotinos kainų ataskaitos mažmeninės prekybos parduotuvė.</span><span class="sxs-lookup"><span data-stu-id="19c14-116">The retail store for which the price report should be generated.</span></span> |
| <span data-ttu-id="19c14-117">Rodyti produktus su turimomis atsargomis</span><span class="sxs-lookup"><span data-stu-id="19c14-117">Display products with available inventory</span></span>| <span data-ttu-id="19c14-118">Nustačius šio parametro parinktį **Taip**, bus rodomos tik tų produktų, kurių faktinių atsargų tuo metu yra parduotuvėje, kainos.</span><span class="sxs-lookup"><span data-stu-id="19c14-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="19c14-119">Rodyti variantų kainas</span><span class="sxs-lookup"><span data-stu-id="19c14-119">Display prices for variants</span></span> | <span data-ttu-id="19c14-120">Nustačius šio parametro parinktį **Taip**, bus rodomi variantų ir bendrųjų produktų kainos.</span><span class="sxs-lookup"><span data-stu-id="19c14-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="19c14-121">Šis parametras turėtų būti **Įjungtas** tik jei esate nustatę konkrečių variantų kainas, nes eilučių skaičius gali labai išaugti.</span><span class="sxs-lookup"><span data-stu-id="19c14-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="19c14-122">Būsimuose leidimuose įjungsime dimensijomis pagrįstas kainas, kad parduotuvės vadovas galėtų pasirinkti dimensijas, kurių kainos turėtų būti rodomos.</span><span class="sxs-lookup"><span data-stu-id="19c14-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="19c14-123">Rodyti produktus su kainų pokyčiais</span><span class="sxs-lookup"><span data-stu-id="19c14-123">Display products with price changes</span></span> | <span data-ttu-id="19c14-124">Nustačius šio parametro parinktį **Taip**, bus rodomos tik tų dienų, per kurias kaina buvo pakeista, kainos.</span><span class="sxs-lookup"><span data-stu-id="19c14-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="19c14-125">*Vienos dienos prieš* pasirinktą **pradžios datą** kaina visada bus rodoma, kad parduotuvės vadovas galėtų lengvai nustatyti produktus, kurių kainos nepasikeitė per visą pasirinktą laikotarpį, ir taip pat peržiūrėti esamą kainą.</span><span class="sxs-lookup"><span data-stu-id="19c14-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="19c14-126">Sugeneravus ataskaitą, galima atsisiųsti „Excel“ failą, jei reikia atlikti papildomų filtravimo veiksmų.</span><span class="sxs-lookup"><span data-stu-id="19c14-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="19c14-127">Kainų ataskaitą taip pat galima naudoti norint patikrinti praeities datų produktų kainas.</span><span class="sxs-lookup"><span data-stu-id="19c14-127">The price report can also be used to check the historical prices of products for past dates.</span></span>

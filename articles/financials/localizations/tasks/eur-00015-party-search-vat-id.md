---
title: 'EUR-00015: šalies ieška naudojant PVM ID'
description: Šioje procedūroje parodoma, kaip atlikti šalies iešką naudojant registracijos ID.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec36ead402882c1022811b7b398a03c6325ef7c0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "371204"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="4ca89-103">EUR-00015: šalies ieška naudojant PVM ID</span><span class="sxs-lookup"><span data-stu-id="4ca89-103">EUR-00015 Party search using VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ca89-104">Šioje procedūroje parodoma, kaip atlikti šalies iešką naudojant registracijos ID.</span><span class="sxs-lookup"><span data-stu-id="4ca89-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="4ca89-105">Prieš atlikdami šią procedūrą, turite nustatyti PVM ID ir įvesti tiekėjų, klientų arba juridinių subjektų PVM ID.</span><span class="sxs-lookup"><span data-stu-id="4ca89-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="4ca89-106">Ši procedūra taikoma visoms Europos šalims / regionams.</span><span class="sxs-lookup"><span data-stu-id="4ca89-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="4ca89-107">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="4ca89-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="4ca89-108">Ši procedūra yra skirta mokėtinų sumų vadovui arba gautinų sumų vadovui.</span><span class="sxs-lookup"><span data-stu-id="4ca89-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="4ca89-109">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="4ca89-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="4ca89-110">Pasirinkite Organizacijos administravimas > Visuotinė adresų knygelė > Visuotinė adresų knygelė.</span><span class="sxs-lookup"><span data-stu-id="4ca89-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="4ca89-111">Spustelėkite Registracijos ID ieška.</span><span class="sxs-lookup"><span data-stu-id="4ca89-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="4ca89-112">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="4ca89-112">Click Add.</span></span>
4. <span data-ttu-id="4ca89-113">Lauke Registracijos tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4ca89-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="4ca89-114">Pavyzdžiui, jei norite ieškoti šalių, kurių registracijos ID tipas yra PVM ID, pasirinkite PVM ID.</span><span class="sxs-lookup"><span data-stu-id="4ca89-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="4ca89-115">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4ca89-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="4ca89-116">Pavyzdžiui, įveskite DEU.</span><span class="sxs-lookup"><span data-stu-id="4ca89-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="4ca89-117">Lauke Registracijos numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4ca89-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="4ca89-118">Spauskite Rasti.</span><span class="sxs-lookup"><span data-stu-id="4ca89-118">Click Find.</span></span>
    * <span data-ttu-id="4ca89-119">Bus rodomos visos šalys su tuo registracijos ID.</span><span class="sxs-lookup"><span data-stu-id="4ca89-119">All parties with that registration ID will be displayed.</span></span>  


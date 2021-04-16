---
title: 'EUR-00015: šalies ieška naudojant PVM ID'
description: Šioje procedūroje parodoma, kaip atlikti šalies iešką naudojant registracijos ID.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8e5cbbbc15a0e33afb04f00d8b1a0b0cd5cab2c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821791"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="4b3b4-103">EUR-00015: šalies ieška naudojant PVM ID</span><span class="sxs-lookup"><span data-stu-id="4b3b4-103">EUR-00015 Party search using VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b3b4-104">Šioje procedūroje parodoma, kaip atlikti šalies iešką naudojant registracijos ID.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="4b3b4-105">Prieš atlikdami šią procedūrą, turite nustatyti PVM ID ir įvesti tiekėjų, klientų arba juridinių subjektų PVM ID.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="4b3b4-106">Ši procedūra taikoma visoms Europos šalims / regionams.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="4b3b4-107">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="4b3b4-108">Ši procedūra yra skirta mokėtinų sumų vadovui arba gautinų sumų vadovui.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="4b3b4-109">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="4b3b4-110">Pasirinkite Organizacijos administravimas > Visuotinė adresų knygelė > Visuotinė adresų knygelė.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="4b3b4-111">Spustelėkite Registracijos ID ieška.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="4b3b4-112">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-112">Click Add.</span></span>
4. <span data-ttu-id="4b3b4-113">Lauke Registracijos tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="4b3b4-114">Pavyzdžiui, jei norite ieškoti šalių, kurių registracijos ID tipas yra PVM ID, pasirinkite PVM ID.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="4b3b4-115">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="4b3b4-116">Pavyzdžiui, įveskite DEU.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="4b3b4-117">Lauke Registracijos numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="4b3b4-118">Spauskite Rasti.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-118">Click Find.</span></span>
    * <span data-ttu-id="4b3b4-119">Bus rodomos visos šalys su tuo registracijos ID.</span><span class="sxs-lookup"><span data-stu-id="4b3b4-119">All parties with that registration ID will be displayed.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
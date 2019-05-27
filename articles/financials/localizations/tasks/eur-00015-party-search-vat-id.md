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
ms.openlocfilehash: d3cb847d4950b02aa7392cd3b307934b008d5e1c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538107"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="3d514-103">EUR-00015: šalies ieška naudojant PVM ID</span><span class="sxs-lookup"><span data-stu-id="3d514-103">EUR-00015 Party search using VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d514-104">Šioje procedūroje parodoma, kaip atlikti šalies iešką naudojant registracijos ID.</span><span class="sxs-lookup"><span data-stu-id="3d514-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="3d514-105">Prieš atlikdami šią procedūrą, turite nustatyti PVM ID ir įvesti tiekėjų, klientų arba juridinių subjektų PVM ID.</span><span class="sxs-lookup"><span data-stu-id="3d514-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="3d514-106">Ši procedūra taikoma visoms Europos šalims / regionams.</span><span class="sxs-lookup"><span data-stu-id="3d514-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="3d514-107">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="3d514-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="3d514-108">Ši procedūra yra skirta mokėtinų sumų vadovui arba gautinų sumų vadovui.</span><span class="sxs-lookup"><span data-stu-id="3d514-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="3d514-109">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="3d514-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="3d514-110">Pasirinkite Organizacijos administravimas > Visuotinė adresų knygelė > Visuotinė adresų knygelė.</span><span class="sxs-lookup"><span data-stu-id="3d514-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="3d514-111">Spustelėkite Registracijos ID ieška.</span><span class="sxs-lookup"><span data-stu-id="3d514-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="3d514-112">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3d514-112">Click Add.</span></span>
4. <span data-ttu-id="3d514-113">Lauke Registracijos tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3d514-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="3d514-114">Pavyzdžiui, jei norite ieškoti šalių, kurių registracijos ID tipas yra PVM ID, pasirinkite PVM ID.</span><span class="sxs-lookup"><span data-stu-id="3d514-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="3d514-115">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3d514-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="3d514-116">Pavyzdžiui, įveskite DEU.</span><span class="sxs-lookup"><span data-stu-id="3d514-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="3d514-117">Lauke Registracijos numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3d514-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="3d514-118">Spauskite Rasti.</span><span class="sxs-lookup"><span data-stu-id="3d514-118">Click Find.</span></span>
    * <span data-ttu-id="3d514-119">Bus rodomos visos šalys su tuo registracijos ID.</span><span class="sxs-lookup"><span data-stu-id="3d514-119">All parties with that registration ID will be displayed.</span></span>  


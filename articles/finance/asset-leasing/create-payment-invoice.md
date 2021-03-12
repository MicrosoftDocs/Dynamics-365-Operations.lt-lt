---
title: Mokėjimo SF kūrimas
description: Šioje temoje paaiškinama, kaip kurti mėnesines nuomos SF. Galite kurti atskiros nuomos SF arba galite naudoti paketinį procesą, kad sukurtumėte kelių nuomų SF.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 303fb0e70530fdc29cb129736b01c0e0e8d02075
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969583"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="9f2c8-104">Mokėjimo SF kūrimas</span><span class="sxs-lookup"><span data-stu-id="9f2c8-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f2c8-105">Galite kurti mėnesines atskiros nuomos SF arba galite naudoti paketinį procesą, kad sukurtumėte kelių nuomų SF.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="9f2c8-106">Tolesnė procedūra nurodo, kaip sukurti atskirą nuomos mokesčio įrašą, kai puslapyje **Nuomos knygų sąranka** parametras **Mokėti tiekėjui** yra įjungtas.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="9f2c8-107">Puslapyje **Nuomos suvestinė** pasirinkite nuomą, tada – **Knygos \> Mokėjimo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="9f2c8-108">Pasirinkite mokėjimą, kurį reikia atlikti, tada pasirinkite **Kurti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="9f2c8-109">Gausite pranešimą, kuriame bus nurodoma, kad buvo sukurtas žurnalas pagal pasirinktą mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="9f2c8-110">Pasirinkite **SF žurnalai**, tada pasirinkite SF, kuri turi būti apmokėta.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="9f2c8-111">Skirtuke **Eilutės** peržiūrėkite žurnalo įrašą, prieš jį registruodami didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9f2c8-112">Pagal numatytuosius parametrus sukurtose tiekėjo SF eilutėse naudojamas tiekėjo registravimo šablonas iš puslapio **Mokėtinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="9f2c8-113">Pasirinkite tinkamą žurnalą, tada pasirinkite SF, kuri turi būti apmokėta.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="9f2c8-114">Šiame pavyzdyje nuomos knygos parametras **Mokėti tiekėjui** yra įjungtas.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="9f2c8-115">Todėl SF bus SF žurnale.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="9f2c8-116">Skyriuje **Apžvaga** pateikiama žurnalo įrašo suvestinė, o skyriuje **Eilutės** rodoma informacija apie faktines žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9f2c8-117">Jei parametras **Mokėti tiekėjui** yra išjungtas, mokėjimo žurnalo įrašai bus pateikti nuomos knygos puslapyje **Turto nuoma**, o sistema sukurs turto nuomos įrašą vietoj SF.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="9f2c8-118">Nuomos mokesčio įrašas bus užregistruotas žurnalo pavadinime, kuris nurodytas lauke **Mėnesinis nuomos žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="9f2c8-119">Užregistravę operaciją, galite peržiūrėti operacijos informaciją ir nuomos įsipareigojimo balansinę vertę nuomos knygoje pasirinkdami **Įsipareigojimų operacijos**.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="9f2c8-120">Mokėjimo grafike bus pažymėtas žymės langelis **Žurnalas užregistruotas**, o eilutėje bus rodomas SF žurnalo numeris.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="9f2c8-121">Kai sukurtas mokėjimo žurnalas ir to žurnalo įrašas, reikia atšaukti įrašą, kad būtų galima jį sukurti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="9f2c8-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>

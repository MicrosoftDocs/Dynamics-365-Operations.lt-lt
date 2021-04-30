---
title: Mokėjimo SF kūrimas
description: Šioje temoje paaiškinama, kaip kurti mėnesines nuomos SF. Galite kurti atskiros nuomos SF arba galite naudoti paketinį procesą, kad sukurtumėte kelių nuomų SF.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8d0b10993c61c64dadc00046907485f3886e2e01
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881185"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="4c40c-104">Mokėjimo SF kūrimas</span><span class="sxs-lookup"><span data-stu-id="4c40c-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c40c-105">Galite kurti mėnesines atskiros nuomos SF arba galite naudoti paketinį procesą, kad sukurtumėte kelių nuomų SF.</span><span class="sxs-lookup"><span data-stu-id="4c40c-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="4c40c-106">Tolesnė procedūra nurodo, kaip sukurti atskirą nuomos mokesčio įrašą, kai puslapyje **Nuomos knygų sąranka** parametras **Mokėti tiekėjui** yra įjungtas.</span><span class="sxs-lookup"><span data-stu-id="4c40c-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="4c40c-107">Puslapyje **Nuomos suvestinė** pasirinkite nuomą, tada – **Knygos \> Mokėjimo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="4c40c-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="4c40c-108">Pasirinkite mokėjimą, kurį reikia atlikti, tada pasirinkite **Kurti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="4c40c-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="4c40c-109">Gausite pranešimą, kuriame bus nurodoma, kad buvo sukurtas žurnalas pagal pasirinktą mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="4c40c-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="4c40c-110">Pasirinkite **SF žurnalai**, tada pasirinkite SF, kuri turi būti apmokėta.</span><span class="sxs-lookup"><span data-stu-id="4c40c-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="4c40c-111">Skirtuke **Eilutės** peržiūrėkite žurnalo įrašą, prieš jį registruodami didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="4c40c-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4c40c-112">Pagal numatytuosius parametrus sukurtose tiekėjo SF eilutėse naudojamas tiekėjo registravimo šablonas iš puslapio **Mokėtinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="4c40c-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="4c40c-113">Pasirinkite tinkamą žurnalą, tada pasirinkite SF, kuri turi būti apmokėta.</span><span class="sxs-lookup"><span data-stu-id="4c40c-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="4c40c-114">Šiame pavyzdyje nuomos knygos parametras **Mokėti tiekėjui** yra įjungtas.</span><span class="sxs-lookup"><span data-stu-id="4c40c-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="4c40c-115">Todėl SF bus SF žurnale.</span><span class="sxs-lookup"><span data-stu-id="4c40c-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="4c40c-116">Skyriuje **Apžvaga** pateikiama žurnalo įrašo suvestinė, o skyriuje **Eilutės** rodoma informacija apie faktines žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="4c40c-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4c40c-117">Jei parametras **Mokėti tiekėjui** yra išjungtas, mokėjimo žurnalo įrašai bus pateikti nuomos knygos puslapyje **Turto nuoma**, o sistema sukurs turto nuomos įrašą vietoj SF.</span><span class="sxs-lookup"><span data-stu-id="4c40c-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="4c40c-118">Nuomos mokesčio įrašas bus užregistruotas žurnalo pavadinime, kuris nurodytas lauke **Mėnesinis nuomos žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="4c40c-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="4c40c-119">Užregistravę operaciją, galite peržiūrėti operacijos informaciją ir nuomos įsipareigojimo balansinę vertę nuomos knygoje pasirinkdami **Įsipareigojimų operacijos**.</span><span class="sxs-lookup"><span data-stu-id="4c40c-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="4c40c-120">Mokėjimo grafike bus pažymėtas žymės langelis **Žurnalas užregistruotas**, o eilutėje bus rodomas SF žurnalo numeris.</span><span class="sxs-lookup"><span data-stu-id="4c40c-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="4c40c-121">Kai sukurtas mokėjimo žurnalas ir to žurnalo įrašas, reikia atšaukti įrašą, kad būtų galima jį sukurti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="4c40c-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

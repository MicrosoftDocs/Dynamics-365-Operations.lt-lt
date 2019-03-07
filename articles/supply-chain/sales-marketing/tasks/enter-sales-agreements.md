---
title: Įvesti pardavimo sutartis
description: Ši procedūra nurodo, kaip kurti pardavimo sutartį, kuri jūsų klientus įpareigoja pirkti nustatytą produktų kiekį per tam tikrą laikotarpį, suteikiant jiems specialias nuolaidas.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 025c9fe2f769f37b63bd79c6c3afedc31a955310
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "346875"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="826b3-103">Įvesti pardavimo sutartis</span><span class="sxs-lookup"><span data-stu-id="826b3-103">Enter sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="826b3-104">Ši procedūra nurodo, kaip kurti pardavimo sutartį, kuri jūsų klientus įpareigoja pirkti nustatytą produktų kiekį per tam tikrą laikotarpį, suteikiant jiems specialias nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="826b3-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="826b3-105">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="826b3-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="826b3-106">Pardavimo sutarties eilutės nustatymas</span><span class="sxs-lookup"><span data-stu-id="826b3-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="826b3-107">Eikite į Pardavimas ir rinkodara > Pardavimo sutartys > Pardavimo sutartys.</span><span class="sxs-lookup"><span data-stu-id="826b3-107">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="826b3-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="826b3-108">Click New.</span></span>
3. <span data-ttu-id="826b3-109">Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="826b3-109">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="826b3-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="826b3-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="826b3-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="826b3-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="826b3-112">Lauke Pardavimo sutarčių klasifikacija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="826b3-112">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="826b3-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="826b3-113">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="826b3-114">Išplėskite skyrių Bendra.</span><span class="sxs-lookup"><span data-stu-id="826b3-114">Expand the General section.</span></span>
9. <span data-ttu-id="826b3-115">Lauke Numatytasis įsipareigojimas pasirinkite „Produkto vertės įsipareigojimas“.</span><span class="sxs-lookup"><span data-stu-id="826b3-115">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="826b3-116">Įsipareigojimo tipas yra privalomas kriterijus, kurį turite priskirti sutarčiai, kad nustatytumėte, kaip sutartis bus įvykdyta.</span><span class="sxs-lookup"><span data-stu-id="826b3-116">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="826b3-117">Naudojant keturis iš anksto nustatytus tipus galima nustatyti kliento įsipareigojimo tikslą, kuris išreiškiamas kaip kiekis arba vertė.</span><span class="sxs-lookup"><span data-stu-id="826b3-117">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="826b3-118">Kiekio įsipareigojimo tipą galima taikyti tik konkrečiam produktui, bet verte grįstus tipus galima taikyti parduodant konkrečius ir nekonkrečius produktus.</span><span class="sxs-lookup"><span data-stu-id="826b3-118">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="826b3-119">Lauke Galiojimo data nustatykite ateities datą, kurią sutartis nustos galioti.</span><span class="sxs-lookup"><span data-stu-id="826b3-119">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="826b3-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="826b3-120">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="826b3-121">Produkto vertės įsipareigojimo eilučių nustatymas</span><span class="sxs-lookup"><span data-stu-id="826b3-121">Set up product value commitment lines</span></span>
1. <span data-ttu-id="826b3-122">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="826b3-122">Click Add line.</span></span>
2. <span data-ttu-id="826b3-123">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="826b3-123">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="826b3-124">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="826b3-124">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="826b3-125">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="826b3-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="826b3-126">Pasirinktas sutarties įsipareigojimo tipas įtakoja, kokią informaciją galite įvesti sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="826b3-126">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="826b3-127">Pvz., jei sutartis pagrįsta verte, turite nurodyti bendrą grynąją sumą (sutarta valiuta), už kurią klientas įsipareigoja nusipirkti iš jūsų prekių.</span><span class="sxs-lookup"><span data-stu-id="826b3-127">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="826b3-128">Šiame pavyzdyje eilučių laukų Kiekis ir Vienetas naudoti negalima, nes kuriate sutartį, pagal kurią klientas pirks konkrečios vertės produktų kiekį.</span><span class="sxs-lookup"><span data-stu-id="826b3-128">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="826b3-129">Lauke Grynoji suma įveskite piniginę sumą, už kurią klientas įsipareigojo pirkti.</span><span class="sxs-lookup"><span data-stu-id="826b3-129">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="826b3-130">Lauke Nuolaidos procentas įveskite procentinę reikšmę, kuri bus taikoma kliento pardavimo užsakymo eilutėms, susietoms su šia sutartimi.</span><span class="sxs-lookup"><span data-stu-id="826b3-130">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="826b3-131">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="826b3-131">Expand the Line details section.</span></span>
8. <span data-ttu-id="826b3-132">Lauke Maksimaliai vykdoma pasirinktie Taip.</span><span class="sxs-lookup"><span data-stu-id="826b3-132">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="826b3-133">Jei pasirenkate Maksimaliai vykdoma, bendra visų pardavimo užsakymo eilučių, kurios naudoja konkrečias įsipareigojimo kainas, nuolaidas ir (arba) mokėjimo sąlygas, suma negali viršyti nurodytos įsipareigojimo sumos.</span><span class="sxs-lookup"><span data-stu-id="826b3-133">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="826b3-134">Mažiausia ir didžiausia išleidimo sumos nurodo vertės, už kurią reikia parduoti prekių vykdant kiekvieną pasirinktos sutarties pardavimo užsakymą, intervalą.</span><span class="sxs-lookup"><span data-stu-id="826b3-134">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="826b3-135">Išplėskite sekciją Pardavimo sutarties antraštė.</span><span class="sxs-lookup"><span data-stu-id="826b3-135">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="826b3-136">Jei sutarties būsena nėra nustatyta kaip Galiojanti, pardavimo užsakymų negalima susieti su sutartimi ir todėl jie neturi įtakos sutarties sąlygų vykdymui.</span><span class="sxs-lookup"><span data-stu-id="826b3-136">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="826b3-137">Šio etapo metu būseną galite neautomatiškai pakeisti.</span><span class="sxs-lookup"><span data-stu-id="826b3-137">You can change the status manually at this stage.</span></span> <span data-ttu-id="826b3-138">Tačiau įprastai būsena keičiama tvirtinant kliento sutartį.</span><span class="sxs-lookup"><span data-stu-id="826b3-138">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="826b3-139">Srityje Veiksmas spustelėkite Pardavimo sutartis.</span><span class="sxs-lookup"><span data-stu-id="826b3-139">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="826b3-140">Spustelėkite „Patvirtinimas“.</span><span class="sxs-lookup"><span data-stu-id="826b3-140">Click Confirmation.</span></span>
    * <span data-ttu-id="826b3-141">Įsitikinkite, kad parinktis Pažymėti sutartį kaip galiojančią, nustatyta kaip Taip.</span><span class="sxs-lookup"><span data-stu-id="826b3-141">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="826b3-142">Lauke Spausdinti ataskaitą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="826b3-142">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="826b3-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="826b3-143">Click OK.</span></span>
14. <span data-ttu-id="826b3-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="826b3-144">Close the page.</span></span>
    * <span data-ttu-id="826b3-145">Dabar sutartis galioja ir jūs galite pradėti kliento užsakymus sieti su sutartimi ir dengti įsipareigoto tikslo sumą.</span><span class="sxs-lookup"><span data-stu-id="826b3-145">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


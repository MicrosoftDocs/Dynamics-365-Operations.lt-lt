---
title: "Personalizuotų produktų rekomendacijų apžvalga"
description: "Šioje temoje pateikiama informacija apie „Dynamics 365 for Retail“ produkto rekomendacijas, kurios gali būti rodomos elektroninio kasos aparato (EKA) įrenginyje."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 64f0a9a44b97a9980f8d1b76ff158f1ac9cbc114
ms.openlocfilehash: 942d6225a46b108ea39d3b8e4376b644c128ae6d
ms.contentlocale: lt-lt
ms.lasthandoff: 11/14/2017

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="69fff-103">Personalizuotų produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="69fff-103">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="69fff-104">Šią funkciją dabar galima naudoti tik smėlio dėžės ir gamybos (plataus pasiekiamumo) visuotinio diegimo topologijose.</span><span class="sxs-lookup"><span data-stu-id="69fff-104">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="69fff-105">Programoje „Dynamics 365 for Retail“ produkto rekomendacijos gali būti rodomos elektroninio kasos aparato (EKA) įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="69fff-105">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="69fff-106">Rekomendacijos –tai prekės, kurios gali sudominti klientą atsižvelgiant į jo pirkimo istoriją, prekės, kurias klientas įtraukė į savo norų sąrašą, ir prekės, kurias kiti klientai įsigijo internetu ir įprastose parduotuvėse.</span><span class="sxs-lookup"><span data-stu-id="69fff-106">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="69fff-107">Mažmenininkų, turinčių didelius prekių katalogus, klientams rekomendacijos padeda surasti produktus.</span><span class="sxs-lookup"><span data-stu-id="69fff-107">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="69fff-108">Kadangi pateikiant produkto rekomendacijas demonstruojami į kliento pomėgius ir pirkimo įpročius orientuoti produktai, mažmenininkams tai gali padėti atlikti papildomą ir kryžminį pardavimą ir išsaugoti klientus.</span><span class="sxs-lookup"><span data-stu-id="69fff-108">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="69fff-109">Naudojant „Dynamics 365 for Retail“ produkto rekomendacijos pateikiamos pagal pažintines paslaugas ir „Microsoft Azure“ mašininį mokymą.</span><span class="sxs-lookup"><span data-stu-id="69fff-109">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="69fff-110">Scenarijai</span><span class="sxs-lookup"><span data-stu-id="69fff-110">Scenarios</span></span>
---------

<span data-ttu-id="69fff-111">Produktų rekomendacijas galima naudoti taikant toliau nurodytus EKA scenarijus.</span><span class="sxs-lookup"><span data-stu-id="69fff-111">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="69fff-112">Juos rasite naudodami „Cloud POS“ arba „Modern POS“ (MPOS).</span><span class="sxs-lookup"><span data-stu-id="69fff-112">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="69fff-113">Puslapyje **Produkto informacija**:</span><span class="sxs-lookup"><span data-stu-id="69fff-113">On the **Product details** page:</span></span>

-   <span data-ttu-id="69fff-114">Jeigu parduotuvės atstovas puslapyje **Produkto informacija** apsilanko skirtinguose kanaluose žiūrėdamas į ankstesnes operacijas, rekomendacijų variklis siūlo kitų prekių, kurios gali būti perkamos papildomai.</span><span class="sxs-lookup"><span data-stu-id="69fff-114">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="69fff-115">Jei parduotuvės atstovas į operaciją įtraukia klientą, o po to apsilanko puslapyje **Produkto informacija**, naudodamas kliento operacijų istoriją ir krepšelyje esančių prekių sąrašą rekomendacijų variklis pateikia personalizuotas rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="69fff-115">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="69fff-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="69fff-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="69fff-117">Puslapyje **Operacija**:</span><span class="sxs-lookup"><span data-stu-id="69fff-117">On the **Transaction** page:</span></span>

-   <span data-ttu-id="69fff-118">Rekomendacijų variklis siūlo prekes atsižvelgdamas į visą krepšelyje esančių prekių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="69fff-118">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="69fff-119">Jei parduotuvės atstovas į operaciją įtraukia klientą, naudodamas kliento operacijų istoriją ir krepšelyje esančių prekių sąrašą rekomendacijų variklis pateikia asmenines rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="69fff-119">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="69fff-120">Norėdamas, kad rekomendacijos būtų rodomos puslapyje **Operacija**, pardavėjas turi atnaujinti „Dynamics 365 for Retail“ ekrano išdėstymą.</span><span class="sxs-lookup"><span data-stu-id="69fff-120">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="69fff-121">Valdiklis **Rekomendacijos** turi būti perkeliamas į puslapį **Operacija**.</span><span class="sxs-lookup"><span data-stu-id="69fff-121">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="69fff-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="69fff-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="69fff-123">Puslapyje **Kliento informacija**:</span><span class="sxs-lookup"><span data-stu-id="69fff-123">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="69fff-124">Rekomendacijų variklis siūlo prekes atsižvelgdamas į vartotojo ID ir kliento norų sąraše esančias prekes.</span><span class="sxs-lookup"><span data-stu-id="69fff-124">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="69fff-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="69fff-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="69fff-126">Sukonfigūruokite „Dynamics 365 for Retail“, kad būtų leidžiamos EKA rekomendacijos</span><span class="sxs-lookup"><span data-stu-id="69fff-126">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="69fff-127">Norėdami nustatyti produktų rekomendacijas turite atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="69fff-127">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="69fff-128">Įsitikinkite, kad pasirinkote tinkamą **Juridinį subjektą**.</span><span class="sxs-lookup"><span data-stu-id="69fff-128">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="69fff-129">Eikite į **Objekto parduotuvė**, pasirinkite **Mažmeninės prekybos pardavimai**, tada spustelėkite **Atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="69fff-129">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="69fff-130">Taip demonstraciniai duomenys (arba jūsų duomenys) bus naudojami iš jūsų operacinės duomenų bazės ir perkeliami į objektų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="69fff-130">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="69fff-131">Nebūtina: norėdami, kad rekomendacijos būtų rodomos operacijos ekrane, eikite į dalį **Ekrano išdėstymas**, pasirinkite savo ekrano išdėstymą, paleiskite **ekrano išdėstymo kūrimo priemonę**, o po to kur reikia perkelkite **rekomendacijų** valdiklį.</span><span class="sxs-lookup"><span data-stu-id="69fff-131">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="69fff-132">Eikite į **Mažmeninės prekybos parametrai**, pasirinkite **Mašininis mokymas**, dalyje **Įjungti EKA rekomendacijas** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="69fff-132">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="69fff-133">Norėdami pamatyti rekomendacijas naudodami EKA, paleiskite visuotinės konfigūracijos užduotį **1110**.</span><span class="sxs-lookup"><span data-stu-id="69fff-133">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="69fff-134">Norėdami, kad būtų rodomi EKA ekrano išdėstymo kūrimo priemonei atlikti pakeitimai, paleiskite kanalo konfigūracijos užduotį **1070**.</span><span class="sxs-lookup"><span data-stu-id="69fff-134">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="69fff-135">[]()Kaip tai veikia?</span><span class="sxs-lookup"><span data-stu-id="69fff-135">[]()How does it work?</span></span>
<span data-ttu-id="69fff-136">Atnaujinus objektą **Objekto parduotuvė** atliekami toliau nurodyti veiksmai.</span><span class="sxs-lookup"><span data-stu-id="69fff-136">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="69fff-137">Pažintinėms paslaugoms reikiamu formatu pateikti duomenys ištraukiami iš „Dynamics 365 for Retail“ operacinės duomenų bazės ir siunčiami į objekto parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="69fff-137">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="69fff-138">Duomenis naudoja programa „Azure Data Factory“ (ADF), kuri išvalo juos kaip ADF veiklų dalį naudodama „Hive“ scenarijus.</span><span class="sxs-lookup"><span data-stu-id="69fff-138">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="69fff-139">Išvalyti duomenys saugomi didelių dvejetainių objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="69fff-139">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="69fff-140">Iš didelių dvejetainių objektų saugyklos gautus duomenis naudoja pažintinių paslaugų API, kad paruoštų rekomendacijos modelį.</span><span class="sxs-lookup"><span data-stu-id="69fff-140">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="69fff-141">Kai įjungiate **Įjungti rekomendacijas** ir paleidžiate konfigūracijos užduotis, atliekami toliau nurodyti veiksmai.</span><span class="sxs-lookup"><span data-stu-id="69fff-141">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="69fff-142">Iš API gaunami modelio kredencialai ir ID, kurie saugomi „Dynamics 365 for Retail“ operacinėje duomenų bazėje, AOS skirtame web.config ir mažmeninės prekybos serveryje.</span><span class="sxs-lookup"><span data-stu-id="69fff-142">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="69fff-143">Modelio kredencialais ir ID gali naudotis CRT, kad būtų galima apmokėti naudojant internetinį režimą iš „Cloud POS“ ir MPOS atliktus skambučius dėl produkto rekomendacijų.</span><span class="sxs-lookup"><span data-stu-id="69fff-143">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="69fff-144">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="69fff-144">See also</span></span>
--------

[<span data-ttu-id="69fff-145">Rekomendacijų valdiklio įtraukimas į EKA įrenginio operacijų puslapį</span><span class="sxs-lookup"><span data-stu-id="69fff-145">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)





---
title: "Personalizuotų produktų rekomendacijų apžvalga"
description: "Šioje temoje pateikiama informacija apie „Dynamics 365 for Retail“ produkto rekomendacijas, kurios gali būti rodomos elektroninio kasos aparato (EKA) įrenginyje."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: c5b9ee57b0b855766628caca239059205c103b86
ms.openlocfilehash: 4a0586324dddc10d64ad6760222f2540f31d6bce
ms.contentlocale: lt-lt
ms.lasthandoff: 03/08/2018

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="26748-103">Personalizuotų produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="26748-103">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="26748-104">Pašalinsime dabartinę produktų rekomendavimo paslaugos versiją ir šią funkciją pertvarkysime, suteikdami jai geresnį algoritmą ir naujesnes į mažmeninę prekybą orientuotas galimybes.</span><span class="sxs-lookup"><span data-stu-id="26748-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="26748-105">Daugiau informacijos žr. [Pašalintos arba nebenaudojamos funkcijos](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="26748-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> <span data-ttu-id="26748-106">Jei kyla problemų dėl jūsų aplinkai skirtų jau įjungtų produktų rekomendacijų, nueikite į puslapio apačią,</span><span class="sxs-lookup"><span data-stu-id="26748-106">Navigate to the bottom of the page if you are facing issues with already-enabled product recommendations for your environment.</span></span> 

<span data-ttu-id="26748-107">Programoje „Dynamics 365 for Retail“ produkto rekomendacijos gali būti rodomos elektroninio kasos aparato (EKA) įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="26748-107">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="26748-108">Rekomendacijos –tai prekės, kurios gali sudominti klientą atsižvelgiant į jo pirkimo istoriją, prekės, kurias klientas įtraukė į savo norų sąrašą, ir prekės, kurias kiti klientai įsigijo internetu ir įprastose parduotuvėse.</span><span class="sxs-lookup"><span data-stu-id="26748-108">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="26748-109">Mažmenininkų, turinčių didelius prekių katalogus, klientams rekomendacijos padeda surasti produktus.</span><span class="sxs-lookup"><span data-stu-id="26748-109">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="26748-110">Kadangi pateikiant produkto rekomendacijas demonstruojami į kliento pomėgius ir pirkimo įpročius orientuoti produktai, mažmenininkams tai gali padėti atlikti papildomą ir kryžminį pardavimą ir išsaugoti klientus.</span><span class="sxs-lookup"><span data-stu-id="26748-110">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="26748-111">Naudojant „Dynamics 365 for Retail“ produkto rekomendacijos pateikiamos pagal pažintines paslaugas ir „Microsoft Azure“ mašininį mokymą.</span><span class="sxs-lookup"><span data-stu-id="26748-111">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="26748-112">Scenarijai</span><span class="sxs-lookup"><span data-stu-id="26748-112">Scenarios</span></span>
---------

<span data-ttu-id="26748-113">Produktų rekomendacijas galima naudoti taikant toliau nurodytus EKA scenarijus.</span><span class="sxs-lookup"><span data-stu-id="26748-113">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="26748-114">Juos rasite naudodami „Cloud POS“ arba „Modern POS“ (MPOS).</span><span class="sxs-lookup"><span data-stu-id="26748-114">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="26748-115">Puslapyje **Produkto informacija**:</span><span class="sxs-lookup"><span data-stu-id="26748-115">On the **Product details** page:</span></span>

-   <span data-ttu-id="26748-116">Jeigu parduotuvės atstovas puslapyje **Produkto informacija** apsilanko skirtinguose kanaluose žiūrėdamas į ankstesnes operacijas, rekomendacijų variklis siūlo kitų prekių, kurios gali būti perkamos papildomai.</span><span class="sxs-lookup"><span data-stu-id="26748-116">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="26748-117">Jei parduotuvės atstovas į operaciją įtraukia klientą, o po to apsilanko puslapyje **Produkto informacija**, naudodamas kliento operacijų istoriją ir krepšelyje esančių prekių sąrašą rekomendacijų variklis pateikia personalizuotas rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="26748-117">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="26748-118">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="26748-118">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="26748-119">Puslapyje **Operacija**:</span><span class="sxs-lookup"><span data-stu-id="26748-119">On the **Transaction** page:</span></span>

-   <span data-ttu-id="26748-120">Rekomendacijų variklis siūlo prekes atsižvelgdamas į visą krepšelyje esančių prekių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="26748-120">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="26748-121">Jei parduotuvės atstovas į operaciją įtraukia klientą, naudodamas kliento operacijų istoriją ir krepšelyje esančių prekių sąrašą rekomendacijų variklis pateikia asmenines rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="26748-121">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="26748-122">Norėdamas, kad rekomendacijos būtų rodomos puslapyje **Operacija**, pardavėjas turi atnaujinti „Dynamics 365 for Retail“ ekrano išdėstymą.</span><span class="sxs-lookup"><span data-stu-id="26748-122">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="26748-123">Valdiklis **Rekomendacijos** turi būti perkeliamas į puslapį **Operacija**.</span><span class="sxs-lookup"><span data-stu-id="26748-123">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="26748-124">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="26748-124">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="26748-125">Puslapyje **Kliento informacija**:</span><span class="sxs-lookup"><span data-stu-id="26748-125">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="26748-126">Rekomendacijų variklis siūlo prekes atsižvelgdamas į vartotojo ID ir kliento norų sąraše esančias prekes.</span><span class="sxs-lookup"><span data-stu-id="26748-126">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="26748-127">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="26748-127">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="26748-128">Sukonfigūruokite „Dynamics 365 for Retail“, kad būtų leidžiamos EKA rekomendacijos</span><span class="sxs-lookup"><span data-stu-id="26748-128">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="26748-129">Norėdami nustatyti produktų rekomendacijas turite atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="26748-129">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="26748-130">Įsitikinkite, kad pasirinkote tinkamą **Juridinį subjektą**.</span><span class="sxs-lookup"><span data-stu-id="26748-130">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="26748-131">Eikite į **Objekto parduotuvė**, pasirinkite **Mažmeninės prekybos pardavimai**, tada spustelėkite **Atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="26748-131">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="26748-132">Taip demonstraciniai duomenys (arba jūsų duomenys) bus naudojami iš jūsų operacinės duomenų bazės ir perkeliami į objektų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="26748-132">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="26748-133">Nebūtina: norėdami, kad rekomendacijos būtų rodomos operacijos ekrane, eikite į dalį **Ekrano išdėstymas**, pasirinkite savo ekrano išdėstymą, paleiskite **ekrano išdėstymo kūrimo priemonę**, o po to kur reikia perkelkite **rekomendacijų** valdiklį.</span><span class="sxs-lookup"><span data-stu-id="26748-133">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="26748-134">Eikite į **Mažmeninės prekybos parametrai**, pasirinkite **Mašininis mokymas**, dalyje **Įjungti EKA rekomendacijas** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="26748-134">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="26748-135">Norėdami pamatyti rekomendacijas naudodami EKA, paleiskite visuotinės konfigūracijos užduotį **1110**.</span><span class="sxs-lookup"><span data-stu-id="26748-135">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="26748-136">Norėdami, kad būtų rodomi EKA ekrano išdėstymo kūrimo priemonei atlikti pakeitimai, paleiskite kanalo konfigūracijos užduotį **1070**.</span><span class="sxs-lookup"><span data-stu-id="26748-136">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="26748-137">[]()Kaip tai veikia?</span><span class="sxs-lookup"><span data-stu-id="26748-137">[]()How does it work?</span></span>
<span data-ttu-id="26748-138">Atnaujinus objektą **Objekto parduotuvė** atliekami toliau nurodyti veiksmai.</span><span class="sxs-lookup"><span data-stu-id="26748-138">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="26748-139">Pažintinėms paslaugoms reikiamu formatu pateikti duomenys ištraukiami iš „Dynamics 365 for Retail“ operacinės duomenų bazės ir siunčiami į objekto parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="26748-139">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="26748-140">Duomenis naudoja programa „Azure Data Factory“ (ADF), kuri išvalo juos kaip ADF veiklų dalį naudodama „Hive“ scenarijus.</span><span class="sxs-lookup"><span data-stu-id="26748-140">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="26748-141">Išvalyti duomenys saugomi didelių dvejetainių objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="26748-141">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="26748-142">Iš didelių dvejetainių objektų saugyklos gautus duomenis naudoja pažintinių paslaugų API, kad paruoštų rekomendacijos modelį.</span><span class="sxs-lookup"><span data-stu-id="26748-142">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="26748-143">Kai įjungiate **Įjungti rekomendacijas** ir paleidžiate konfigūracijos užduotis, atliekami toliau nurodyti veiksmai.</span><span class="sxs-lookup"><span data-stu-id="26748-143">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="26748-144">Iš API gaunami modelio kredencialai ir ID, kurie saugomi „Dynamics 365 for Retail“ operacinėje duomenų bazėje, AOS skirtame web.config ir mažmeninės prekybos serveryje.</span><span class="sxs-lookup"><span data-stu-id="26748-144">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="26748-145">Modelio kredencialais ir ID gali naudotis CRT, kad būtų galima apmokėti naudojant internetinį režimą iš „Cloud POS“ ir MPOS atliktus skambučius dėl produkto rekomendacijų.</span><span class="sxs-lookup"><span data-stu-id="26748-145">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>

> ## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="26748-146">Trikčių šalinimas, kai funkcija Produktų rekomendacijos jau įjungta</span><span class="sxs-lookup"><span data-stu-id="26748-146">Troubleshoot issues where you have Product recommendations already enabled</span></span> 
>- <span data-ttu-id="26748-147">Nueikite į **Mažmeninės prekybos parametrai** > **Mašininis mokymas** > **Išjungti produktų rekomendacijas** ir paleiskite **visuotinės konfigūracijos užduotį [1110]**.</span><span class="sxs-lookup"><span data-stu-id="26748-147">Navigate to **Retail Parameters** > **Machine learning** > **Disable product recommendations** and run **Global configuration job [1110]**.</span></span> <span data-ttu-id="26748-148">Jei nerandate skirtuko **Mašininis mokymas**, kreipkitės į „Dynamics“ palaikymo tarnybą.</span><span class="sxs-lookup"><span data-stu-id="26748-148">If you are not able to locate **Machine learning** tab, please contact Dynamics Support.</span></span> 

>- <span data-ttu-id="26748-149">Jei, naudodami **ekrano maketo dizaino įrankį**, į savo operacijų ekraną įtraukėte **rekomendacijų valdiklį**, jį taip pat pašalinkite.</span><span class="sxs-lookup"><span data-stu-id="26748-149">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span> 



<a name="see-also"></a><span data-ttu-id="26748-150">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="26748-150">See also</span></span>
--------

[<span data-ttu-id="26748-151">Rekomendacijų valdiklio įtraukimas į EKA įrenginio operacijų puslapį</span><span class="sxs-lookup"><span data-stu-id="26748-151">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)





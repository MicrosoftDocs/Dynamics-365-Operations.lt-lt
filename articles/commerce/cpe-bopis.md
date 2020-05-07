---
title: BOPIS konfigūravimas „Dynamics 365 Commerce“ aplinkoje
description: Šioje temoje paaiškinama, kaip konfigūruoti „pirkimas internetu, atsiėmimas parduotuvėje“ (BOPIS) „Microsoft Dynamics 365 Commerce” aplinkoje po to, kai ji parengta.
author: rubendel
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 956d66d09885d4d54655ce25b3aa7ba6a9c34cf4
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282801"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="749a7-103">BOPIS konfigūravimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="749a7-103">Configure BOPIS in a Dynamics 365 Commerce environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="749a7-104">Šioje temoje paaiškinama, kaip konfigūruoti „pirkimas internetu, atsiėmimas parduotuvėje“ (BOPIS) „Microsoft Dynamics 365 Commerce” aplinkoje po to, kai aplinka parengta.</span><span class="sxs-lookup"><span data-stu-id="749a7-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="749a7-105">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="749a7-105">Prerequisite</span></span>

<span data-ttu-id="749a7-106">Šios temos procedūras atlikite tik tada, kai „Commerce“ peržiūros aplinka yra parengta ir sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="749a7-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned and configured.</span></span> <span data-ttu-id="749a7-107">Informacijos apie tai, kaip parengti ir sukonfigūruoti aplinką, rasite skyriuose [„Dynamics 365 Commerce” peržiūros aplinkos parengimas](provisioning-guide.md) ir [„Dynamics 365 Commerce” peržiūros aplinkos konfigūravimas](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span><span class="sxs-lookup"><span data-stu-id="749a7-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce preview environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce preview environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="749a7-108">Po to, kai jūsų „Commerce” aplinka visapusiškai parengta ir sukonfigūruota, galite pasinaudoti šia tema, kad įgalintumėte BOPIS scenarijus.</span><span class="sxs-lookup"><span data-stu-id="749a7-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="749a7-109">EKA konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="749a7-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="749a7-110">„Modern POS” konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="749a7-110">Configure Modern POS</span></span>

<span data-ttu-id="749a7-111">BOPIS scenarijams, apimantiems mokėjimą kredito kortele, reikia aparatūros stoties.</span><span class="sxs-lookup"><span data-stu-id="749a7-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="749a7-112">Aparatūros stotis yra įmontuota į „Windows“ ir „Android“ klientų „Modern POS“.</span><span class="sxs-lookup"><span data-stu-id="749a7-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="749a7-113">Jei naudojate „Cloud POS“ arba „Modern POS“, skirtas „iOS“, elektroninio kasos aparato (EKA) klientas turi būti susietas su bendrai naudojama aparatūros stotimi.</span><span class="sxs-lookup"><span data-stu-id="749a7-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="749a7-114">Šioje temoje paaiškinama, kaip sukonfigūruoti BOPIS, skirtą „Windows” ir „Android” klientams.</span><span class="sxs-lookup"><span data-stu-id="749a7-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="749a7-115">Informacijos apie tai, kaip nustatyti bendrai naudojamą aparatūros stotį, žr. [Mažmeninės prekybos aparatūros stoties konfigūracija ir diegimas](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="749a7-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="749a7-116">Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> Registrai**.</span><span class="sxs-lookup"><span data-stu-id="749a7-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="749a7-117">Pasirinkite registrą **SANFRAN-5**, tada pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="749a7-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="749a7-118">Pakeiskite lauko **Aparatūros šablonas** reikšmę iš **HW002** į **HW001**, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="749a7-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="749a7-119">Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**, kad sinchronizuotumėte pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="749a7-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="749a7-120">Pasirinkite paskirstymo grafiką **1090**, tada veiksmų srityje pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="749a7-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="749a7-121">Pasirinkite **Taip** ir **Gerai**, kad būtų pradėtas duomenų sinchronizavimas.</span><span class="sxs-lookup"><span data-stu-id="749a7-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="749a7-122">„Modern POS“ diegimas</span><span class="sxs-lookup"><span data-stu-id="749a7-122">Install Modern POS</span></span>

1. <span data-ttu-id="749a7-123">Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> Įrenginiai**.</span><span class="sxs-lookup"><span data-stu-id="749a7-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="749a7-124">Pasirinkite įrenginį **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="749a7-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="749a7-125">Veiksmų srityje pasirinkite **Atsisiųsti**, tada – **Konfigūracijos failas**.</span><span class="sxs-lookup"><span data-stu-id="749a7-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="749a7-126">Pasirinkite **Atsisiųsti**, tada – **„Retail Modern POS”**.</span><span class="sxs-lookup"><span data-stu-id="749a7-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="749a7-127">Kai **ModernPOSSetup.exe** failo atsisiuntimas baigtas, pasirinkite **Atidaryti failą**.</span><span class="sxs-lookup"><span data-stu-id="749a7-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Atidaryti failą](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="749a7-129">Pasirinkite **Pirmyn**, kad būtų pradėtas diegimo procesas.</span><span class="sxs-lookup"><span data-stu-id="749a7-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="749a7-130">Kai diegimas baigtas, pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="749a7-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="749a7-131">„Modern POS” aktyvinimas</span><span class="sxs-lookup"><span data-stu-id="749a7-131">Activate Modern POS</span></span>

1. <span data-ttu-id="749a7-132">„Windows” darbalaukyje pasirinkite mygtuką **Pradžia** ir įveskite **„Retail Modern POS”**.</span><span class="sxs-lookup"><span data-stu-id="749a7-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="749a7-133">Pasirinkite **„Retail Modern POS”** programą, kad būtų pradėtas aktyvinimas.</span><span class="sxs-lookup"><span data-stu-id="749a7-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="749a7-134">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="749a7-134">Select **Next**.</span></span> <span data-ttu-id="749a7-135">Laukai **Serverio URL**, **Įrenginio ID** ir **Registro numeris** turi būti nustatyti iš anksto naudojant konfigūracijos failo, atsisiųsto atliekant ankstesnę procedūrą, informaciją.</span><span class="sxs-lookup"><span data-stu-id="749a7-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="749a7-136">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="749a7-136">Select **Activate**.</span></span>
5. <span data-ttu-id="749a7-137">Pasirodo autentifikavimo dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="749a7-137">An authentication dialog box appears.</span></span> <span data-ttu-id="749a7-138">Pasirinkite sąskaitą, kuri naudoja el. pašto adresą, anksčiau susietą su darbuotoju **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="749a7-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="749a7-139">Jei dar nesusiejote darbuotojo su jūsų tapatybe, aktyvinimas bus nesėkmingas.</span><span class="sxs-lookup"><span data-stu-id="749a7-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="749a7-140">Šiuo atveju atlikite veiksmus, nurodytus skyriuje „Darbuotojo susiejimas su jūsų tapatybe”, temoje [„Dynamics 365 Commerce” peržiūros aplinkos konfigūravimas](cpe-post-provisioning.md#associate-a-worker-with-your-identity).</span><span class="sxs-lookup"><span data-stu-id="749a7-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce preview environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="749a7-141">Kai būsite paraginti leisti jūsų organizacijai valdyti įrenginį, pasirinkite **Tik šią programą**.</span><span class="sxs-lookup"><span data-stu-id="749a7-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="749a7-142">Kai aktyvinimas baigtas, pasirinkite **Pradžia**.</span><span class="sxs-lookup"><span data-stu-id="749a7-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="749a7-143">BOPIS įgalinimas „Modern POS”</span><span class="sxs-lookup"><span data-stu-id="749a7-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="749a7-144">Prisijunkite prie „Modern POS” naudodami **000713** kaip operatoriaus ID ir **123** kaip slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="749a7-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="749a7-145">Kol leidžiamas įvadinis supažindinimo vaizdo įrašas, pažymėkite du žymės langelius, esančius apatiniame kairiajame dialogo lango kampe, ir uždarykite dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="749a7-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="749a7-146">Jei nebūsite paraginti uždaryti pamainos, slinkite į dešinę puslapyje **Sveiki**, pasirinkite **Uždaryti pamainą** ir vėl prisijunkite prie EKA.</span><span class="sxs-lookup"><span data-stu-id="749a7-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="749a7-147">Kai prisijungsite ir būsite paraginti, pasirinkite **Atlikti ne stalčiaus operaciją**.</span><span class="sxs-lookup"><span data-stu-id="749a7-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="749a7-148">Puslapyje **Sveiki** slinkite į dešinę ir pasirinkite operaciją **Pasirinkti aparatūros stotį**.</span><span class="sxs-lookup"><span data-stu-id="749a7-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="749a7-149">Pasirinkite **Valdyti**, nustatykite pasirinktį **Naudoti aparatūros stotį** į **Įjungta** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="749a7-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="749a7-150">Atsijunkite nuo EKA ir vėl prisijunkite.</span><span class="sxs-lookup"><span data-stu-id="749a7-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="749a7-151">Po to, kai prisijungsite, pasirinkite **Atidaryti naują pamainą** ir tada – **Stalčius**.</span><span class="sxs-lookup"><span data-stu-id="749a7-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="749a7-152">BOPIS scenarijaus baigimas</span><span class="sxs-lookup"><span data-stu-id="749a7-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="749a7-153">Parduotuvėje paimamo parduotuvės užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="749a7-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="749a7-154">Eikite į URL, kurį nurodėte veiksmo [El. prekybos inicijavimas](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) metu atliekant aplinkos konfigūravimą.</span><span class="sxs-lookup"><span data-stu-id="749a7-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="749a7-155">Pasirinkite prekę, tada – **Įtraukti į krepšelį**.</span><span class="sxs-lookup"><span data-stu-id="749a7-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="749a7-156">Pirkinių krepšelio puslapyje pasirinkite **Paimti** ką tik įtrauktoje užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="749a7-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="749a7-157">Dialogo lange **Pasirinkti parduotuvę** įveskite **San Fransiskas** ir pasirinkite mygtuką **Paieška**.</span><span class="sxs-lookup"><span data-stu-id="749a7-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="749a7-158">Rezultatų sąraše suraskite San Francisko parduotuvę ir pasirinkite **Paimti čia**.</span><span class="sxs-lookup"><span data-stu-id="749a7-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="749a7-159">Pirkinių krepšelio puslapyje pasirinkite **Užbaigti pirkimą kaip svečias**.</span><span class="sxs-lookup"><span data-stu-id="749a7-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="749a7-160">Norėdami tęsti pirkimo užbaigimą, turite sutikti su slapukų pranešimu.</span><span class="sxs-lookup"><span data-stu-id="749a7-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="749a7-161">Šis pranešimas rodomas kaip reklaminė juosta pirkimo užbaigimo puslapio viršuje.</span><span class="sxs-lookup"><span data-stu-id="749a7-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="749a7-162">Mokėjimo kredito kortele būdo atveju įveskite toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="749a7-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="749a7-163">**Kortelės savininko vardas:** įveskite bet kokį vardą.</span><span class="sxs-lookup"><span data-stu-id="749a7-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="749a7-164">**Kortelės numeris:** įveskite **4111-1111-1111-1111**.</span><span class="sxs-lookup"><span data-stu-id="749a7-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="749a7-165">**Galiojimo data:** įveskite **10/20**.</span><span class="sxs-lookup"><span data-stu-id="749a7-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="749a7-166">**Kortelės tikrinimo vertės (CVV) kodas**: įveskite **737**.</span><span class="sxs-lookup"><span data-stu-id="749a7-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="749a7-167">Bandomojoje svetainėje niekada esant jokioms aplinkybėms nenaudokite faktinės kredito kortelės informacijos.</span><span class="sxs-lookup"><span data-stu-id="749a7-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="749a7-168">Tęskite pirkimo užbaigimą įvesdami sąskaitų siuntimo adreso informaciją, tada pasirinkite **Įrašyti ir tęsti**.</span><span class="sxs-lookup"><span data-stu-id="749a7-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="749a7-169">Kai užsakymas paruoštas, pasirinkite **Užbaigti pirkimą**.</span><span class="sxs-lookup"><span data-stu-id="749a7-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="749a7-170">Internetinių užsakymų sinchronizavimas su tarnybiniu biuru</span><span class="sxs-lookup"><span data-stu-id="749a7-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="749a7-171">Informacijos apie tai, kaip sinchronizuoti internetinius užsakymus, žr. [Pardavimo ir mokėjimų internetu registravimas](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span><span class="sxs-lookup"><span data-stu-id="749a7-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="749a7-172">Užsakymo paėmimas parduotuvėje</span><span class="sxs-lookup"><span data-stu-id="749a7-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="749a7-173">Prisijunkite prie EKA.</span><span class="sxs-lookup"><span data-stu-id="749a7-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="749a7-174">**Darbo pradžios** ekrane pasirinkite **Užsakymo įvykdymas**</span><span class="sxs-lookup"><span data-stu-id="749a7-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="749a7-175">Paimamų prekių sąraše pasirinkite užsakymo, kuris buvo pateiktas internetu, eilutę.</span><span class="sxs-lookup"><span data-stu-id="749a7-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="749a7-176">Pasirinkę užsakymo eilutę pasirinkite **Paimti**.</span><span class="sxs-lookup"><span data-stu-id="749a7-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="749a7-177">Eilutės elementas įtraukiamas į operacijos ekraną, o **0,00 USD** rodoma kaip mokėtinas balansas.</span><span class="sxs-lookup"><span data-stu-id="749a7-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="749a7-178">Pasirinkite mokėtiną **0,00 USD** balansą arba bet kokį mokėjimo būdą operacijai atlikti.</span><span class="sxs-lookup"><span data-stu-id="749a7-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="749a7-179">Trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="749a7-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="749a7-180">Internetiniai užsakymai, kurie nuskaitomi EKA, turi ne nulinį mokėtiną balansą</span><span class="sxs-lookup"><span data-stu-id="749a7-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="749a7-181">Kai užsakymas nuskaitomas paėmimui iš parduotuvės, jei mokėtinas balansas nėra 0 (nulis), įsitikinkite, kad naudojama „Modern POS” ir kad aparatūros stotis yra aktyvi.</span><span class="sxs-lookup"><span data-stu-id="749a7-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="749a7-182">Jei naudojama „Cloud POS“ arba „Modern POS“, skirtos „iOS“, įsitikinkite, kad bendrai naudojama aparatūros stotis yra aktyvi.</span><span class="sxs-lookup"><span data-stu-id="749a7-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="749a7-183">Norint nuskaityti mokėjimus, atliktus internetu, reikia tam tikros aktyvios aparatūros stoties.</span><span class="sxs-lookup"><span data-stu-id="749a7-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="749a7-184">Problemos, susijusios su mokėjimo fiksavimu</span><span class="sxs-lookup"><span data-stu-id="749a7-184">General issues with payment capture</span></span>

<span data-ttu-id="749a7-185">Susidūrę su problemomis pirmiausia perskaitykite „Modern POS” arba informacinių interneto paslaugų (IIS) aparatūros stoties įvykių žurnalus.</span><span class="sxs-lookup"><span data-stu-id="749a7-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="749a7-186">Šiuos žurnalus galite rasti toliau nurodytuose „Windows” įvykių žurnalo mazguose.</span><span class="sxs-lookup"><span data-stu-id="749a7-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="749a7-187">Programų ir paslaugų žurnalai \> „Microsoft” \> „Dynamics” \> „Commerce-ModernPOS”</span><span class="sxs-lookup"><span data-stu-id="749a7-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="749a7-188">Programų ir paslaugų žurnalai \> „Microsoft” \> „Dynamics” \> „Commerce-Hardware Station”</span><span class="sxs-lookup"><span data-stu-id="749a7-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="749a7-189">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="749a7-189">Additional resources</span></span>

[<span data-ttu-id="749a7-190">„Dynamics 365 Commerce“peržiūros aplinkos apžvalga</span><span class="sxs-lookup"><span data-stu-id="749a7-190">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="749a7-191">„Dynamics 365 Commerce“ peržiūros aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="749a7-191">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="749a7-192">„Dynamics 365 Commerce“ peržiūros aplinkos pasirinktinių funkcijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="749a7-192">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="749a7-193">„Dynamics 365 Commerce“peržiūros aplinkos DUK</span><span class="sxs-lookup"><span data-stu-id="749a7-193">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="749a7-194">„Microsoft Lifecycle Services“ (LCS)</span><span class="sxs-lookup"><span data-stu-id="749a7-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="749a7-195">„Retail Cloud Scale Unit“ (RCSU)</span><span class="sxs-lookup"><span data-stu-id="749a7-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="749a7-196">„Microsoft Azure“ portalas</span><span class="sxs-lookup"><span data-stu-id="749a7-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="749a7-197">„Dynamics 365 Commerce“ svetainė</span><span class="sxs-lookup"><span data-stu-id="749a7-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="749a7-198">„Adyen“ mokėjimo jungtis</span><span class="sxs-lookup"><span data-stu-id="749a7-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="749a7-199">Internetinių mokėjimo priemonių įrašymas naudojant „Adyen“ jungtį</span><span class="sxs-lookup"><span data-stu-id="749a7-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="749a7-200">Integruotų kanalų mokėjimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="749a7-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)

---
title: Subranga
description: Šioje temoje paaiškinama, kaip sukurti subrangos vadovą kai gamyboje naudojama „Dynamics 365 Supply Chain Management“.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3e282e0676e53200b0993dd9cb2b52e08fe97dca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981461"
---
# <a name="subcontracting"></a><span data-ttu-id="0673e-103">Subranga</span><span class="sxs-lookup"><span data-stu-id="0673e-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0673e-104">Šioje temoje paaiškinama, kaip sukurti gamybos subrangos vadovą kai naudojama „Microsoft“ „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="0673e-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0673e-105">Pirmoje šios temos dalyje aprašoma duomenų sąranka.</span><span class="sxs-lookup"><span data-stu-id="0673e-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="0673e-106">Antroje dalyje aprašomi apžvalgos veiksmai.</span><span class="sxs-lookup"><span data-stu-id="0673e-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="0673e-107">Tikslinė auditorija</span><span class="sxs-lookup"><span data-stu-id="0673e-107">Target audience</span></span>

<span data-ttu-id="0673e-108">Šioje temoje sužinosite, kaip nustatyti subrangą gamyboje.</span><span class="sxs-lookup"><span data-stu-id="0673e-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="0673e-109">Naudokite esamus duomenis juridiniame subjekte HQUS norėdami atlikti pagrindinę subrangos veiklos srauto sąranką.</span><span class="sxs-lookup"><span data-stu-id="0673e-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="0673e-110">Demonstraciniai duomenys juridiniame subjekte HQUS apima sąrankos parametrus, kurie buvo iš anksto nustatyti, kad būtų galima atlikti apžvalgos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0673e-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="0673e-111">Nors apžvalgoje nurodyti įvairiems vaidmenims skirti klausimai ir problemos, apžvalgos veiksmus gali atlikti sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="0673e-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="0673e-112">Demonstracinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="0673e-112">Demo scenario</span></span>

<span data-ttu-id="0673e-113">Juridiniame subjekte HQUS gaminami aukštos kokybės garsiakalbiai.</span><span class="sxs-lookup"><span data-stu-id="0673e-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="0673e-114">Garsiakalbių gamybos procesą sudaro trys toliau nurodytos operacijos.</span><span class="sxs-lookup"><span data-stu-id="0673e-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="0673e-115">**Išankstinis surinkimas** – surenkama garsiakalbio dėžė.</span><span class="sxs-lookup"><span data-stu-id="0673e-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="0673e-116">Dėžės medžiaga paimama medžiagų sandėlyje prieš operacijos pradžią.</span><span class="sxs-lookup"><span data-stu-id="0673e-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="0673e-117">**Padengimas** – surinktą garsiakalbio dėžę reikia padengti.</span><span class="sxs-lookup"><span data-stu-id="0673e-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="0673e-118">Šią operaciją atlieka tiekėjas (rangovas).</span><span class="sxs-lookup"><span data-stu-id="0673e-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="0673e-119">Iš anksto surinkta garsiakalbio dėžė siunčiama padengimo subrangovui kartu su dviem medžiagomis.</span><span class="sxs-lookup"><span data-stu-id="0673e-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="0673e-120">**Baigimas** – kai subrangovas padengia iš anksto surinktą garsiakalbio dėžę, ji grąžinama juridiniam subjektui HQUS, kad būtų galima baigti galutinius surinkimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0673e-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="0673e-121">Toliau pateiktoje iliustracijoje parodytos tys operacijos ir medžiagos, sunaudojamos jas atliekant.</span><span class="sxs-lookup"><span data-stu-id="0673e-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Išankstinio surinkimo, padengimo ir baigimo operacijos bei medžiagos, sunaudojamos jas atliekant](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="0673e-123">Sąranka</span><span class="sxs-lookup"><span data-stu-id="0673e-123">Setup</span></span>

<span data-ttu-id="0673e-124">Prieš pradėdami apžvalgos veiksmus, turite nustatyti duomenis.</span><span class="sxs-lookup"><span data-stu-id="0673e-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="0673e-125">Baigto produkto sąranka</span><span class="sxs-lookup"><span data-stu-id="0673e-125">Set up the finished product</span></span>

<span data-ttu-id="0673e-126">Šios procedūros metu bus nustatytas išleistas produktas D8100, „Padengta dėžė“.</span><span class="sxs-lookup"><span data-stu-id="0673e-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="0673e-127">Pasirinkite **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**, kad atidarytumėte puslapį **Išleisto produkto informacija**.</span><span class="sxs-lookup"><span data-stu-id="0673e-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="0673e-128">Sparčiojo filtro lauke įveskite **D8100**, kad rastumėte esamą išleistą produktą.</span><span class="sxs-lookup"><span data-stu-id="0673e-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Išleisto produkto D8100 filtravimas puslapyje Išleisto produkto informacija](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="0673e-130">Veiksmų srities skirtuke **Inžinierius** pasirinkite **Maršrutas**, kad atidarytumėte puslapį **Maršrutas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="0673e-131">Puslapyje **Maršrutas** rodomos aštuonios išleisto produkto D8100 maršruto versijos.</span><span class="sxs-lookup"><span data-stu-id="0673e-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="0673e-132">Aštuonios maršruto versijos paskirstomos keturiems maršrutams 1 ir 5 vietose.</span><span class="sxs-lookup"><span data-stu-id="0673e-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="0673e-133">Maršrutas 000400 naudojamas įkainojimo metu, maršrutas 00041 naudojamas atliekant padengimo operaciją viduje, o maršrutas 00042 naudojamas atliekant padengimo operaciją išorėje.</span><span class="sxs-lookup"><span data-stu-id="0673e-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Aštuonios maršruto versijos puslapyje Maršrutas](./media/subcontract03_route-page.png)

4. <span data-ttu-id="0673e-135">Viršutinės srities tinklelyje **Versijos** pasirinkite maršruto versiją **00042**, skirtą **5** vietai.</span><span class="sxs-lookup"><span data-stu-id="0673e-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="0673e-136">Apatinės srities skirtuke **Apžvalga**, tinklelyje pasirinkite **20** operaciją (**Cbnt CtSc**).</span><span class="sxs-lookup"><span data-stu-id="0673e-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Pasirinkta 00042 maršruto versijos operacija, skirta 5 vietai](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="0673e-138">Pasirinkite skirtuką **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="0673e-138">Select the **General** tab.</span></span>

    <span data-ttu-id="0673e-139">Atkreipkite dėmesį, kad laukas **Maršruto tipas** nustatytas į parinktį **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="0673e-140">Ši vertė nurodo, kad 20 operacija („Cbnt CtSc“) yra subrangos operacija.</span><span class="sxs-lookup"><span data-stu-id="0673e-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Skirtuko Bendra laukas Maršruto tipas nustatytas į parinktį Tiekėjas](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="0673e-142">Pasirinkite skirtuką **Išteklių reikalavimai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="0673e-143">Galimybės bus naudojamos siekiant rasti tinkama išteklių gamybos planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="0673e-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="0673e-144">Atlikdami 20 operaciją („Cbnt CtSc“) atkreipkite dėmesį, kad būtinas išteklius, kuriam priskirtos dvi galimybės, **Padengimas** ir **Padengtos dėžės**.</span><span class="sxs-lookup"><span data-stu-id="0673e-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Skirtuko Išteklių reikalavimai galimybės Padengimas ir Padengtos dėžės](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="0673e-146">Pasirinkite **Taikomi ištekliai**, kad atidarytumėte dialogo langą **Taikomi ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="0673e-147">Rasti trys išteklių, atitinkantys operacijos išteklių reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="0673e-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="0673e-148">Atkreipkite dėmesį, kad ištekliai 8851 ir 8852 yra tipo **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Trys taikomi ištekliai dialogo lange Taikomi ištekliai](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="0673e-150">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Taikomi ištekliai** ir vėl atidarytumėte puslapį **Maršrutas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="0673e-151">Uždarykite puslapį **Maršrutas**, kad vėl atidarytumėte puslapį **Išleisto produkto informacija**.</span><span class="sxs-lookup"><span data-stu-id="0673e-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Puslapis Išleisto produkto informacija](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="0673e-153">Veiksmų srities skirtuke **Inžinierius** pasirinkite **KS versijos**, kad atidarytumėte puslapį **KS versijos**.</span><span class="sxs-lookup"><span data-stu-id="0673e-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="0673e-154">Puslapyje **KS versijos** rodomos keturios komplektavimo specifikacijos (KS) versijos, skirtos išleistam produktui D8100.</span><span class="sxs-lookup"><span data-stu-id="0673e-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="0673e-155">KS 000040 naudojama įkainojimo ir planavimo metu, KS 000041 naudojama, jei padengimo operacija atliekama įmonėje, o KS 000042 ir 000043 naudojamos, jei padengimo operaciją atlieka subrangovai.</span><span class="sxs-lookup"><span data-stu-id="0673e-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="0673e-156">Atkreipkite dėmesį, kad prekė S8050 yra produktas, kurio prekės tipas yra **Paslauga**.</span><span class="sxs-lookup"><span data-stu-id="0673e-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="0673e-157">Ši prekė nurodo subrangovo darbą.</span><span class="sxs-lookup"><span data-stu-id="0673e-157">This item represents the subcontracted work.</span></span>

    ![Keturios KS versijos puslapyje KS versijos](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="0673e-159">„FastTab“ **KS eilutės** pasirinkite **Redaguoti**, kad atidarytumėte dialogo langą **Redaguoti KS eilutę**.</span><span class="sxs-lookup"><span data-stu-id="0673e-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="0673e-160">Kai išleisto produkto D8100 gamybos užsakymas yra sukurtas ir nustatytas, automatiškai sugeneruojamas prekės S8050 pirkimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="0673e-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="0673e-161">Šis pirkimo užsakymas bus susietas su gamybos užsakymu.</span><span class="sxs-lookup"><span data-stu-id="0673e-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="0673e-162">Tam, kad pirkimo užsakymai būtų automatiškai generuojami, laukas **Eilutės tipas** turi būti nustatytas į parinktį **Tiekėjas** ir turi būti pasirinkta subrangovo tiekėjo sąskaita.</span><span class="sxs-lookup"><span data-stu-id="0673e-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="0673e-163">Šiuo atveju tiekėjo sąskaita yra US-801.</span><span class="sxs-lookup"><span data-stu-id="0673e-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="0673e-164">Atkreipkite dėmesį, kad KS eilutė yra susieta su operacija Padengimas naudojant operacijos numerį (šiuo atveju – 20).</span><span class="sxs-lookup"><span data-stu-id="0673e-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Dialogo lango KS eilutė redagavimas](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="0673e-166">Sandėlio darbuotojų slaptažodžio kūrimas</span><span class="sxs-lookup"><span data-stu-id="0673e-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="0673e-167">Turite nustatyti slaptažodį, skirtą sandėlio darbuotojams, kurie naudoja rankinius įrenginius.</span><span class="sxs-lookup"><span data-stu-id="0673e-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="0673e-168">Pasirinkite **Sandėlio valdymas \> Sąranka \> Darbuotojas**, kad atidarytumėte puslapį **Darbo vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="0673e-169">„FastTab“ **Vartotojai** pasirinkite eilutę, skirtą vartotojui **51**.</span><span class="sxs-lookup"><span data-stu-id="0673e-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Puslapis Darbo vartotojai](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="0673e-171">Pasirinkite **Iš naujo nustatyti slaptažodį**.</span><span class="sxs-lookup"><span data-stu-id="0673e-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="0673e-172">Laukuose **Slaptažodis** ir **Patvirtinkite slaptažodį** įveskite **1**.</span><span class="sxs-lookup"><span data-stu-id="0673e-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="0673e-173">Pasirinkite **Nustatyti slaptažodį**.</span><span class="sxs-lookup"><span data-stu-id="0673e-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="0673e-174">Nuosekli apžvalga</span><span class="sxs-lookup"><span data-stu-id="0673e-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="0673e-175">**Scenarijus ir apžvalga**</span><span class="sxs-lookup"><span data-stu-id="0673e-175">**Scenario and background**</span></span>

<span data-ttu-id="0673e-176">Sukuriamas 10 vienetų gamybos užsakymas, skirtas produktui D8100, kuris vadinasi „Padengta dėžė“.</span><span class="sxs-lookup"><span data-stu-id="0673e-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="0673e-177">Dėžių padengimas yra subrangos operacija, kurią atlieka tiekėjas US-801, „Perfect Coating Solutions“.</span><span class="sxs-lookup"><span data-stu-id="0673e-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="0673e-178">Gamybos užsakymas susideda iš trijų operacijų.</span><span class="sxs-lookup"><span data-stu-id="0673e-178">The production order consists of three operations.</span></span> <span data-ttu-id="0673e-179">Pirmoji operacija yra išankstinio dėžės surinkimo operacija, atliekama įmonėje.</span><span class="sxs-lookup"><span data-stu-id="0673e-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="0673e-180">Medžiagos, iš kurių iš anksto surenkama dėžė, paruošiamos paimti žaliavų sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="0673e-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="0673e-181">Baigus išankstinio surinkimo operaciją, iš anksto surinkta dėžė siunčiama „Perfect Coating Solutions“ kartu su dviem medžiagomis, kurių reikia padengimo operacijai atlikti.</span><span class="sxs-lookup"><span data-stu-id="0673e-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="0673e-182">Kai padengta dėžė gaunama iš tiekėjo, atliekama galutinė surinkimo operacija įmonėje prieš paskelbiant operaciją baigta.</span><span class="sxs-lookup"><span data-stu-id="0673e-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="0673e-183">Pasirinkite **Gamybos kontrolė \> Gamybos užsakymai \> Visi gamybos užsakymai**, kad atidarytumėte puslapį **Visi gamybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="0673e-184">Veiksmų srityje pasirinkite **Naujas gamybos užsakymas**, kad atidarytumėte dialogo langą **Kurti gamybos užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="0673e-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Dialogo langas Kurti gamybos užsakymą](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="0673e-186">Lauke **Prekės numeris** pasirinkite **D8100**.</span><span class="sxs-lookup"><span data-stu-id="0673e-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="0673e-187">Atsargų dimensijų laukai rodomi pasirinkus prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="0673e-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="0673e-188">Lauke **Spalva** pasirinkite **Chromuota**.</span><span class="sxs-lookup"><span data-stu-id="0673e-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="0673e-189">Pasirodys pranešimo langas, kuriame klausiama, ar įterpti aktyvias KS ir maršruto versijas.</span><span class="sxs-lookup"><span data-stu-id="0673e-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Pranešimo laukas](./media/subcontract13_message-box.png)

5. <span data-ttu-id="0673e-191">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0673e-191">Select **Yes**.</span></span> 

    <span data-ttu-id="0673e-192">Dialogo lange **Kurti gamybos užsakymą** aktyvios KS ir maršruto versijos, skirtos produktui D8100, yra automatiškai pasirenkamos laukuose **KS numeris** ir **Maršruto numeris** atitinkamai.</span><span class="sxs-lookup"><span data-stu-id="0673e-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="0673e-193">Šiuo atveju pasirenkami KS **000040** ir maršrutas **000040**.</span><span class="sxs-lookup"><span data-stu-id="0673e-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="0673e-194">KS ir maršruto versija 000040 naudojama įkainojimo ir planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="0673e-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="0673e-195">Lauke **Vieta** pasirinkite **5**.</span><span class="sxs-lookup"><span data-stu-id="0673e-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="0673e-196">Lauke **Sandėlis** pasirinkite **51**.</span><span class="sxs-lookup"><span data-stu-id="0673e-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="0673e-197">Laukuose **KS numeris** ir **Maršruto numeris** pakeiskite reikšmę, kuri buvo automatiškai pasirinkta, į **000042**.</span><span class="sxs-lookup"><span data-stu-id="0673e-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0673e-198">KS ir maršruto versija 000042 naudojama teikiant dėžės padengimo subrangos užduotį tiekėjui US-801.</span><span class="sxs-lookup"><span data-stu-id="0673e-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Dialogo lange Kurti gamybos užsakymą nustatomos reikšmės](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="0673e-200">Pasirinkite **Kurti**, kad sukurtumėte gamybos užsakymą ir atidarytumėte puslapį **Visi gamybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Naujas gamybos užsakymas puslapyje Visi gamybos užsakymai](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="0673e-202">Veiksmų srities skirtuke **Gamybos užsakymas** pasirinkite **Įvertinti**, kad atidarytumėte dialogo langą **Įvertinti**.</span><span class="sxs-lookup"><span data-stu-id="0673e-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Dialogo langas Įvertinti](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="0673e-204">Pasirinkite **Gerai**, kad patvirtintumėte įvertinimą ir atidarytumėte puslapį **Visi gamybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0673e-205">Vertinant gamybos užsakymą, aptarnavimo prekės S8050 pirkimo užsakymas generuojamas pasirenkant tiekėją US-801.</span><span class="sxs-lookup"><span data-stu-id="0673e-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="0673e-206">Veiksmų srities skirtuke **Gamybos užsakymas** pasirinkite **KS**, kad atidarytumėte puslapį **KS**, kuriame galite peržiūrėti gamybos užsakymo KS eilutes.</span><span class="sxs-lookup"><span data-stu-id="0673e-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="0673e-207">Aptarnavimo prekė S8050: atkreipkite dėmesį, kad pateikta nuoroda į pirkimo užsakymą, kuri buvo sugeneruota įvertinant gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0673e-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Gamybos užsakymo KS eilutės KS puslapyje](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="0673e-209">Uždarykite puslapį **KS**, kad vėl atidarytumėte puslapį **Visi gamybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="0673e-210">Veiksmų srities skirtuke **Grafikas** pasirinkite **Grafiko užduotys**, kad atidarytumėte dialogo langą **Užduočių planavimas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="0673e-211">Nurodykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="0673e-211">Specify the following values:</span></span>

    - <span data-ttu-id="0673e-212">Lauke **Planavimo kryptis** pasirinkite **Pradedant nuo rytojaus**.</span><span class="sxs-lookup"><span data-stu-id="0673e-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="0673e-213">Nustatykite parinktį **Ribotas pajėgumas** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0673e-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Dialogo langas Užduočių planavimas](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="0673e-215">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Užduočių planavimas** ir vėl atidarytumėte puslapį **Visi gamybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="0673e-216">Veiksmų srities skirtuke **Grafikas** pasirinkite **Gantt**, kad atidarytumėte puslapį **Gantt diagrama – išteklių rodinys**.</span><span class="sxs-lookup"><span data-stu-id="0673e-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="0673e-217">Gantt diagramoje pateikiama vaizdinė gamybos užduočių planavimo ir priskyrimo ištekliams apžvalga.</span><span class="sxs-lookup"><span data-stu-id="0673e-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="0673e-218">Atkreipkite dėmesį, kad išorės operacija Padengimas susideda iš trijų užduočių: apdorojimo užduoties, transportavimo užduoties ir laukimo eilėje laiko užduoties.</span><span class="sxs-lookup"><span data-stu-id="0673e-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Ganto diagrama Gantt diagramoje – išteklių peržiūros puslapis](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="0673e-220">Uždarykite puslapį **Gantt diagrama – išteklių peržiūra**, kad vėl atidarytumėte puslapį **Visi gamybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="0673e-221">Veiksmų srities skirtuke **Gamybos užsakymas** pasirinkite **Išleisti**, kad atidarytumėte dialogo langą **Išleisti**.</span><span class="sxs-lookup"><span data-stu-id="0673e-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Dialogo langas Išleisti](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="0673e-223">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Išleisti**.</span><span class="sxs-lookup"><span data-stu-id="0673e-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="0673e-224">Pasirinkite **Gamybos kontrolė \> Periodinės užduotys \> Išleidimas į sandėlį \> Automatinis KS ir formulės eilučių išleidimas**, kad atidarytumėte dialogo langą **Automatinis KS ir formulės eilučių išleidimas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Dialogo langas Automatinis KS ir formulių eilučių išleidimas](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="0673e-226">Pasirinkite **Gerai**, kad paleistumėte automatinio KS ir formulės eilučių išleidimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="0673e-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="0673e-227">Ši užduotis išleidžia žaliavų paėmimo iš sandėlio užduotį.</span><span class="sxs-lookup"><span data-stu-id="0673e-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="0673e-228">Pasirinkite **Gamybos kontrolė \> Gamybos užsakymai \> Visi gamybos užsakymai**, kad atidarytumėte puslapį **Visi gamybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="0673e-229">Naudokite sparčiojo filtro lauką, kad pasirinktumėte gamybos užsakymą, su kuriuo dirbote.</span><span class="sxs-lookup"><span data-stu-id="0673e-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="0673e-230">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Darbo informacija**, kad atidarytumėte puslapį **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="0673e-231">Atkreipkite dėmesį, kad puslapyje rodomi du žaliavų paėmimo darbo rinkiniai.</span><span class="sxs-lookup"><span data-stu-id="0673e-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="0673e-232">Pirmasis darbas yra medžiagų M8100 ir M8101 paėmimas.</span><span class="sxs-lookup"><span data-stu-id="0673e-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="0673e-233">Šios medžiagos vartojamos atliekant 10 operaciją.</span><span class="sxs-lookup"><span data-stu-id="0673e-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="0673e-234">Antrasis darbas yra medžiagų M8202 ir M8250 paėmimas.</span><span class="sxs-lookup"><span data-stu-id="0673e-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="0673e-235">Šios medžiagos vartojamos atliekant 20 operaciją, kuri yra subrangos operacija.</span><span class="sxs-lookup"><span data-stu-id="0673e-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![Puslapyje Darbas rodomi du žaliavų paėmimo darbo rinkiniai](./media/subcontract22_work-page.png)

26. <span data-ttu-id="0673e-237">Paleiskite sandėlio programą, kad apdorotumėte 10 operacijos sandėlio darbą.</span><span class="sxs-lookup"><span data-stu-id="0673e-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="0673e-238">Pasirinkite **Gamybos kontrolė \> Gamybos užsakymai \> Visi gamybos užsakymai**, kad atidarytumėte puslapį **Visi gamybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="0673e-239">Naudokite sparčiojo filtro lauką, kad pasirinktumėte gamybos užsakymą, su kuriuo dirbote.</span><span class="sxs-lookup"><span data-stu-id="0673e-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="0673e-240">Veiksmų srities skirtuke **Gamybos užsakymas** pasirinkite **Pradėti**, kad atidarytumėte dialogo langą **Pradėti**.</span><span class="sxs-lookup"><span data-stu-id="0673e-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="0673e-241">Skirtuke **Bendra** įveskite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="0673e-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="0673e-242">Lauke **Šaltinio oper. nr.**</span><span class="sxs-lookup"><span data-stu-id="0673e-242">In the **From Oper. No.**</span></span> <span data-ttu-id="0673e-243">pasirinkite **10**.</span><span class="sxs-lookup"><span data-stu-id="0673e-243">field, select **10**.</span></span>
    - <span data-ttu-id="0673e-244">Lauke **Paskirties oper. nr.**</span><span class="sxs-lookup"><span data-stu-id="0673e-244">In the **To Oper. No.**</span></span> <span data-ttu-id="0673e-245">pasirinkite **10**.</span><span class="sxs-lookup"><span data-stu-id="0673e-245">field, select **10**.</span></span>

    ![Skirtuke Bendra nustatomos reikšmės](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="0673e-247">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Pradėti** ir vėl atidarytumėte puslapį **Visi gamybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="0673e-248">Atkreipkite dėmesį, kad dabar gamybos užsakymo būsena yra **Pradėtas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="0673e-249">10 operacijos medžiagos naudojamos vykdant automatinį išrinkimo žurnalo registravimą.</span><span class="sxs-lookup"><span data-stu-id="0673e-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="0673e-250">10 operacijos laiko sąnaudos užregistruojamos vykdant automatinį maršruto kortelės žurnalo registravimą.</span><span class="sxs-lookup"><span data-stu-id="0673e-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="0673e-251">Paleiskite sandėlio programą, kad apdorotumėte 20 operacijos sandėlio darbą.</span><span class="sxs-lookup"><span data-stu-id="0673e-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="0673e-252">Veiksmų srities skirtuke **Gamybos užsakymas** pasirinkite **Pradėti**, kad atidarytumėte dialogo langą **Pradėti**.</span><span class="sxs-lookup"><span data-stu-id="0673e-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="0673e-253">Skirtuke **Bendra** įveskite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="0673e-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="0673e-254">Lauke **Šaltinio oper. nr.**</span><span class="sxs-lookup"><span data-stu-id="0673e-254">In the **From Oper. No.**</span></span> <span data-ttu-id="0673e-255">pasirinkite **20**.</span><span class="sxs-lookup"><span data-stu-id="0673e-255">field, select **20**.</span></span>
    - <span data-ttu-id="0673e-256">Lauke **Paskirties oper. nr.**</span><span class="sxs-lookup"><span data-stu-id="0673e-256">In the **To Oper. No.**</span></span> <span data-ttu-id="0673e-257">pasirinkite **20**.</span><span class="sxs-lookup"><span data-stu-id="0673e-257">field, select **20**.</span></span>
    - <span data-ttu-id="0673e-258">Lauke **Kiekis** įveskite **10**.</span><span class="sxs-lookup"><span data-stu-id="0673e-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="0673e-259">Nustatykite lauko **Registruoti išrinkimo dokumentą dabar** parinktį **Ne**.</span><span class="sxs-lookup"><span data-stu-id="0673e-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Skirtuke Bendra nustatomos reikšmės](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="0673e-261">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Pradėti** ir vėl atidarytumėte puslapį **Visi gamybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0673e-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="0673e-262">Sukuriamas medžiagų, kurios naudojamos atliekant padengimo operaciją, ir aptarnavimo prekės išrinkimo dokumentas.</span><span class="sxs-lookup"><span data-stu-id="0673e-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="0673e-263">Aptarnavimo prekė nurodo subrangos operacijos savikainą.</span><span class="sxs-lookup"><span data-stu-id="0673e-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="0673e-264">Veiksmų srities skirtuke **Rodinys** pasirinkite **Išrinkimo dokumentas**, kad atidarytumėte puslapį **Išrinkimo dokumentas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="0673e-265">Pasirinkite išrinkimo dokumentą, kuris nėra užregistruotas, tada pasirinkite žurnalo numerį, kad peržiūrėtumėte žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="0673e-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Žurnalo eilutės puslapyje Išrinkimo dokumentas](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="0673e-267">Veiksmų srityje pasirinkite **Spausdinti** \> **Išrinkimo dokumento ataskaita**, kad atidarytumėte dialogo langą **Išrinkimo dokumento ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="0673e-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="0673e-268">Nustatykite parinktį **Naudoti pristatymo pažymos maketą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0673e-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Dialogo langas Išrinkimo dokumento ataskaita](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="0673e-270">Pasirinkite **Gerai**, kad generuotumėte ataskaitą **Išrinkimo dokumentas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="0673e-271">Šiuo atveju tiekėjo pristatymo pažyma išspausdinta iš gamybos išrinkimo dokumento žurnalo.</span><span class="sxs-lookup"><span data-stu-id="0673e-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="0673e-272">Pristatymo pažymoje nurodomos medžiagos, siunčiamos tiekėjui, kuris atliks operaciją Padengimas.</span><span class="sxs-lookup"><span data-stu-id="0673e-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Išrinkimo dokumentų ataskaita](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="0673e-274">Uždarykite ataskaitą **Išrinkimo dokumentas**, kad vėl atidarytumėte puslapį **Išrinkimo sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="0673e-275">Veiksmų srityje pasirinkite **Registruoti**, kad atidarytumėte dialogo langą **Registruoti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="0673e-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Dialogo langas Registruoti žurnalą](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="0673e-277">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Registruoti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="0673e-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="0673e-278">Atidarykite pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0673e-278">Open the purchase order.</span></span>

    ![Puslapis Pirkimo užsakymas](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="0673e-280">Veiksmų srities skirtuke **Pirkimas** pasirinkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="0673e-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="0673e-281">Pasirinkite **Registruoti**, kad atidarytumėte dialogo langą **Registruoti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="0673e-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="0673e-282">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Registruoti žurnalą** ir vėl atidarytumėte puslapį **Pirkimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="0673e-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="0673e-283">Pakeiskite vieneto kainą **33** į **40**.</span><span class="sxs-lookup"><span data-stu-id="0673e-283">Change the unit price from **33** to **40**.</span></span>

    ![Vieneto kaina pakeista puslapyje Pirkimo užsakymas](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="0673e-285">Patvirtinkite pirkimo užsakymą dar kartą.</span><span class="sxs-lookup"><span data-stu-id="0673e-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="0673e-286">Gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="0673e-286">Product receipt.</span></span>

    ![Dialogo langas Gavimo dokumento registravimas](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="0673e-288">Pirkimo SF.</span><span class="sxs-lookup"><span data-stu-id="0673e-288">Purchase invoice.</span></span>
52. <span data-ttu-id="0673e-289">Atnaujinkite gretinimo būseną.</span><span class="sxs-lookup"><span data-stu-id="0673e-289">Update the match status.</span></span>

    ![Puslapis Tiekėjo SF](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="0673e-291">Skelbkite baigtu.</span><span class="sxs-lookup"><span data-stu-id="0673e-291">Report as finished.</span></span>

    ![Dialogo langas Skelbimas baigtu](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="0673e-293">Baikite.</span><span class="sxs-lookup"><span data-stu-id="0673e-293">End.</span></span>

    ![Dialogo langas Baigimas](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="0673e-295">Savikainos palyginimas.</span><span class="sxs-lookup"><span data-stu-id="0673e-295">Cost comparison.</span></span>

    ![Savikainos palyginimo diagramos](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="0673e-297">Trūksta sąrankos duomenų.</span><span class="sxs-lookup"><span data-stu-id="0673e-297">Missing setup in data.</span></span>

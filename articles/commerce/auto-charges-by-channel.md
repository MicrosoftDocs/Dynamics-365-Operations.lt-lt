---
title: Automatinių išlaidų įjungimas ir konfigūravimas pagal kanalą
description: Šioje temoje paaiškinama, kaip įgalinti ir konfigūruoti automatines išlaidas pagal kanalą „Microsoft Dynamics 365 Commerce”.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 834d90c8ec8515c6bced2d8a4fabc79b4e4e4c3e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211278"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="b231d-103">Automatinių išlaidų įjungimas ir konfigūravimas pagal kanalą</span><span class="sxs-lookup"><span data-stu-id="b231d-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="b231d-104">Šioje temoje paaiškinama, kaip įgalinti ir konfigūruoti automatines išlaidas pagal kanalą „Microsoft Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="b231d-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b231d-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="b231d-105">Overview</span></span>

<span data-ttu-id="b231d-106">Gali būti scenarijų, kai perdirbimo ar kitus mokesčius reikia pritaikyti produktų, kurie parduodami visose arba kai kuriose tam tikros šalies parduotuvėse (pvz., Kalifornijoje), grupei.</span><span class="sxs-lookup"><span data-stu-id="b231d-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="b231d-107">Funkcija **Įjungti automatinių išlaidų filtravimą pagal kanalą** programoje „Commerce“ leidžia nurodyti automatines išlaidas pagal kanalą (pvz., konkretų fizinį kanalą).</span><span class="sxs-lookup"><span data-stu-id="b231d-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="b231d-108">Šią funkcija pasiekiama 10.0.10 arba vėlesnės versijos „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="b231d-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="b231d-109">Norėdami įgalinti ir konfigūruoti automatines išlaidas pagal kanalą, turite atlikti toliau nurodytas užduotis.</span><span class="sxs-lookup"><span data-stu-id="b231d-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="b231d-110">Įjunkite funkciją **Įjungti automatinių išlaidų filtravimą pagal kanalą**.</span><span class="sxs-lookup"><span data-stu-id="b231d-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="b231d-111">Sukonfigūruokite organizacijos hierarchijos paskirtį.</span><span class="sxs-lookup"><span data-stu-id="b231d-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="b231d-112">Nustatykite automatines išlaidas pagal kanalą.</span><span class="sxs-lookup"><span data-stu-id="b231d-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="b231d-113">Funkcija **Įjungti automatinių išlaidų filtravimą pagal kanalą** veikia tik tada, jei įjungta išplėstinė automatinių išlaidų funkcija.</span><span class="sxs-lookup"><span data-stu-id="b231d-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="b231d-114">Informacijos apie tai, kaip įjungti išplėstinę automatinių išlaidų funkciją, žr. [Integruoto kanalo išplėstinės automatinės išlaidos](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="b231d-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="b231d-115">Įjunkite funkciją Įjungti automatinių išlaidų filtravimą pagal kanalą.</span><span class="sxs-lookup"><span data-stu-id="b231d-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="b231d-116">Norėdami įjungti automatines išlaidas pagal kanalą programoje „Commerce“, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b231d-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b231d-117">Eikite į **Sistemos administratorius \> Darbo sritys \> Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="b231d-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="b231d-118">Skirtuko **Neįjungta** sąraše **Funkcijos pavadinimas** raskite ir pasirinkite **Įjungti automatinių išlaidų filtravimą pagal kanalą**.</span><span class="sxs-lookup"><span data-stu-id="b231d-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="b231d-119">Apatiniame dešiniajame kampe pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="b231d-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="b231d-120">Kai funkcija įjungta, ji bus rodoma skirtuko **Visi** sąraše.</span><span class="sxs-lookup"><span data-stu-id="b231d-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="b231d-121">Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="b231d-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="b231d-122">Kairiojoje srityje raskite ir pasirinkite **1110** (**visuotinės konfigūracijos**) užduotį.</span><span class="sxs-lookup"><span data-stu-id="b231d-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="b231d-123">Veiksmų srityje pasirinkite **Vykdyti dabar**, kad būtų paskirstyti konfigūracijos pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="b231d-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="b231d-124">Jei jau naudojote funkciją **Įjungti automatinių išlaidų filtravimą pagal kanalą** ir ją išjungsite, laukas **Mažmeninės prekybos kanalų ryšys** dalyje **Automatinės išlaidos** nebebus rodomas ir neteksite visų esamų konfigūracijų.</span><span class="sxs-lookup"><span data-stu-id="b231d-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="b231d-125">Jei **Mažmeninės prekybos kanalų ryšys** konfigūracijų pašalinimas sukels automatinių išlaidų taisyklių dubliavimą, funkcijos išjungti nepavyks.</span><span class="sxs-lookup"><span data-stu-id="b231d-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="b231d-126">Prieš išjungdami funkciją įsitikinkite, kad peržiūrėjote visas automatinių išlaidų taisykles ir atlikote reikalingus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="b231d-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="b231d-127">Organizacijos hierarchijos paskirties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b231d-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="b231d-128">Siekiant valdyti automatinių išlaidų hierarchiją pagal kanalą, sukurta nauja organizacijos hierarchijos paskirtis, kurios pavadinimas **Mažmeninės prekybos automatinės išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="b231d-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="b231d-129">Norėdami priskirti numatytąją hierarchiją organizacijos hierarchijos paskirčiai programoje „Commerce“, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b231d-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="b231d-130">Eikite į **Organizacijos administravimas \> Organizacijos \> Organizacijos hierarchijos paskirtis**.</span><span class="sxs-lookup"><span data-stu-id="b231d-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="b231d-131">Kairiojoje srityje pasirinkite **Mažmeninės prekybos automatinės išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="b231d-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="b231d-132">Dalyje **Priskirtos hierarchijos** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="b231d-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="b231d-133">Dialogo lange **Organizacijų hierarchijos** pasirinkite organizacijos hierarchiją (pvz., **Mažmeninės prekybos parduotuvės pagal regioną**) ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b231d-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="b231d-134">Dalyje **Priskirtos hierarchijos** pasirinkite **Nustatyti kaip numatytąjį**.</span><span class="sxs-lookup"><span data-stu-id="b231d-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="b231d-135">Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="b231d-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="b231d-136">Kairiojoje srityje raskite ir pasirinkite **1040** (**produktų**) užduotį.</span><span class="sxs-lookup"><span data-stu-id="b231d-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="b231d-137">Veiksmų srityje pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="b231d-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="b231d-138">Pakartokite ankstesnius du veiksmus, norėdami paleisti **1070** (**kanalo konfigūraciją**) ir **1110** (**visuotinės konfigūracijos**) užduotis.</span><span class="sxs-lookup"><span data-stu-id="b231d-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Mažmeninės prekybos automatinių išlaidų organizacijos hierarchijos paskirties konfigūracija](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="b231d-140">Automatines išlaidų nustatymas pagal kanalą</span><span class="sxs-lookup"><span data-stu-id="b231d-140">Define auto charges by channel</span></span>

<span data-ttu-id="b231d-141">Įjungus funkciją **Įjungti automatinių išlaidų filtravimą pagal kanalą** ir sukonfigūravus **Mažmeninės prekybos automatinių išlaidų** organizacijos hierarchijos paskirtį, automatinės išlaidos pagal kanalą gali būti nurodytos arba užsakymo antraštės lygiu, arba užsakymo eilutės lygiu.</span><span class="sxs-lookup"><span data-stu-id="b231d-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="b231d-142">Norėdami nustatyti automatines išlaidas pagal kanalą programoje „Commerce“, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b231d-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b231d-143">Pasirinkite **Gautinos sumos \> Išlaidų sąranka \> Automatinės išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="b231d-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="b231d-144">Kairiosios srities lauke **Lygis** pasirinkite **Antraštė** arba **Eilutė**, atsižvelgdami į savo verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="b231d-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="b231d-145">Lauke **Mažmeninės prekybos kanalo kodas** pasirinkite reikiamą kanalo kodą (pvz., **Lentelė** arba **Grupė**).</span><span class="sxs-lookup"><span data-stu-id="b231d-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="b231d-146">Jei naudojamas numatytasis parametras **Visi**, išlaidų taisyklės taikomos visiems kanalams.</span><span class="sxs-lookup"><span data-stu-id="b231d-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="b231d-147">Jei pasirinksite **Grupė**, įsitikinkite, kad mažmeninės prekybos kanalo išlaidų grupė yra sukurta **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Išlaidos \> Mažmeninės prekybos kanalo išlaidų grupės**.</span><span class="sxs-lookup"><span data-stu-id="b231d-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="b231d-148">Jei pasirinksite **Lentelė**, lauke **Mažmeninės prekybos kanalų ryšys** galite pasirinkti konkretų kanalą, pvz., **San Fransiskas**.</span><span class="sxs-lookup"><span data-stu-id="b231d-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="b231d-149">Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="b231d-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="b231d-150">Kairiojoje srityje raskite ir pasirinkite **1040** (**produktų**) užduotį.</span><span class="sxs-lookup"><span data-stu-id="b231d-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="b231d-151">Veiksmų srityje pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="b231d-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="b231d-152">Pakartokite ankstesnius du veiksmus, norėdami paleisti **1070** (**kanalo konfigūraciją**) ir **1110** (**visuotinės konfigūracijos**) užduotis.</span><span class="sxs-lookup"><span data-stu-id="b231d-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Automatinės išlaidos, nustatytos pagal kanalą](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="b231d-154">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="b231d-154">Example scenario</span></span>

<span data-ttu-id="b231d-155">Toliau pateiktame pavyzdyje aprašomi veiksmai, kurių reikia produktui sukonfigūruoti, kad būtų taikomi perdirbimo mokesčiai, kai produktas parduodamas naudojant San Francisko fizinį kanalą.</span><span class="sxs-lookup"><span data-stu-id="b231d-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="b231d-156">Taip pat pavyzdyje rodoma, kaip automatinės išlaidos bus rodomos „Commerce” elektroninio kasos aparato (EKA) programoje.</span><span class="sxs-lookup"><span data-stu-id="b231d-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="b231d-157">Organizacija apibrėžia išlaidų kodą, kurio pavadinimas **PERDIRBIMAS**, kaip parodyta toliau pateiktoje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="b231d-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![Išlaidų kodas PERDIRBIMAS](media/Auto-charges-charge-code.png)

<span data-ttu-id="b231d-159">Sukuriamos automatinės išlaidos eilutės lygiu.</span><span class="sxs-lookup"><span data-stu-id="b231d-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="b231d-160">Jam būdinga toliau pateikta konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="b231d-160">It has the following configuration:</span></span>

- <span data-ttu-id="b231d-161">Laukas **Sąskaitos kodas** nustatomas į **Visi**.</span><span class="sxs-lookup"><span data-stu-id="b231d-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="b231d-162">Laukas **Prekės kodas** nustatomas į **Lentelė**.</span><span class="sxs-lookup"><span data-stu-id="b231d-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="b231d-163">Laukas **Prekės ryšys** nustatomas į produkto ID **91001**.</span><span class="sxs-lookup"><span data-stu-id="b231d-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="b231d-164">Laukas **Pristatymo kodo režimas** nustatomas į **Visi**.</span><span class="sxs-lookup"><span data-stu-id="b231d-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="b231d-165">Laukas **Mažmeninės prekybos kanalo kodas** nustatomas į **Lentelė**.</span><span class="sxs-lookup"><span data-stu-id="b231d-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="b231d-166">Laukas **Mažmeninės prekybos kanalo ryšys** nustatomas į **San Francisko** parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="b231d-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="b231d-167">Sukuriama automatinių išlaidų eilutė.</span><span class="sxs-lookup"><span data-stu-id="b231d-167">An auto charges line is created.</span></span> <span data-ttu-id="b231d-168">Jam būdinga toliau pateikta konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="b231d-168">It has the following configuration:</span></span>

- <span data-ttu-id="b231d-169">Laukas **Valiuta** nustatytas į **USD**.</span><span class="sxs-lookup"><span data-stu-id="b231d-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="b231d-170">Laukas **Išlaidų kodas** nustatomas į **PERDIRBIMAS**.</span><span class="sxs-lookup"><span data-stu-id="b231d-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="b231d-171">Laukas **Kategorija** nustatytas į **Fiksuotas**.</span><span class="sxs-lookup"><span data-stu-id="b231d-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="b231d-172">Laukas **Išlaidos** nustatytas į **6,25 USD**.</span><span class="sxs-lookup"><span data-stu-id="b231d-172">The **Charges** field is set to **$6.25**.</span></span>

![Automatinių išlaidų eilutės lygiu ir automatinių išlaidų eilutės konfigūracija](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="b231d-174">EKA programos **San Francisko** parduotuvės kanale sukuriamas pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="b231d-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="b231d-175">Eilutėje **Išlaidos** nurodytas **6,25 USD** perdirbimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="b231d-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="b231d-176">EKA programoje pasirinkę **Operacijų parinktys \> Išlaidos \> Valdyti išlaidas** galite peržiūrėti perdirbimo mokesčio išlaidų kodą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="b231d-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![Perdirbimo mokestis EKA programoje](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="b231d-178">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b231d-178">Additional resources</span></span>

[<span data-ttu-id="b231d-179">Integruoto kanalo išplėstinės automatinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b231d-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="b231d-180">Proporcingas antraštės išlaidų paskirstymas atitinkančioms pardavimo eilutėms</span><span class="sxs-lookup"><span data-stu-id="b231d-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
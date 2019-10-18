---
title: „Microsoft Dynamics 365 Talent - Attract“ el. pašto parametrų konfigūravimas
description: Šioje temoje paaiškinama, kaip konfigūruoti el. pašto, siunčiamo iš „Microsoft Dynamcis 365 Talent - Attract“, parametrus.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c891a36f01d36774bd921475fa5995d207cd2d51
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008667"
---
# <a name="configure-email-settings"></a><span data-ttu-id="cb437-103">El. pašto parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cb437-103">Configure email settings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cb437-104">Jūsų prekės ženklas kuria patikimumo įspūdį ir padeda užmegzti ryšį su kandidatais dar prieš jiems kandidatuojant į jūsų siūlomas darbo vietas.</span><span class="sxs-lookup"><span data-stu-id="cb437-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="cb437-105">Teigiamas prekės ženklo įvaizdis pritraukia geriausius talentus ir didina esamų darbuotojų lojalumą.</span><span class="sxs-lookup"><span data-stu-id="cb437-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="cb437-106">„Microsoft Dynamics 365 Talent: Attract“ galima sukonfigūruoti el. laiškus, kad juose atsispindėtų jūsų įmonės prekės ženklas.</span><span class="sxs-lookup"><span data-stu-id="cb437-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="cb437-107">Todėl kandidatavimo proceso metu užtikrinsite nuoseklią kandidatų patirtį.</span><span class="sxs-lookup"><span data-stu-id="cb437-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="cb437-108">„Attract“ galite atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cb437-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="cb437-109">Konfigūruokite el. pašto parametrus, kad būtų naudojama jūsų įmonės „Microsoft Exchange“ el. pašto tarnybos paskyra.</span><span class="sxs-lookup"><span data-stu-id="cb437-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="cb437-110">Taip kandidatai žinos, kad el. laiškai gaunami iš jūsų įmonės.</span><span class="sxs-lookup"><span data-stu-id="cb437-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="cb437-111">Pavyzdžiui, galite sukonfigūruoti savo parametrus, kad kandidatai gautų el. laiškus iš `recruiting@contoso.com`, o ne `contoso@microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="cb437-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="cb437-112">Užtikrinkite nuoseklų prekės ženklo naudojimą visuose el. laiškuose, nustatydami visuotines el. laiško šablonų antraštes ir poraštes.</span><span class="sxs-lookup"><span data-stu-id="cb437-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="cb437-113">Jei norite sukonfigūruoti „Attract“, kad el. laiškai būtų siunčiami naudojant jūsų įmonės el. pašto tarnybos paskyrą, reikalingas priedas „Comprehensive hiring“.</span><span class="sxs-lookup"><span data-stu-id="cb437-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="cb437-114">El. pašto tarnybos paskyros prijungimas</span><span class="sxs-lookup"><span data-stu-id="cb437-114">Connect an email service account</span></span>

<span data-ttu-id="cb437-115">Prijungus savo įmonės el. pašto tarnybos paskyrą, kandidatai į darbo vietas gaus el. laiškus, kuriuose atsispindės jūsų prekės ženklas.</span><span class="sxs-lookup"><span data-stu-id="cb437-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="cb437-116">Jei neprijungsite savo įmonės paskyros, „Attract“ naudos numatytąją „Microsoft“ prekės ženklo el. pašto tarnybos paskyrą.</span><span class="sxs-lookup"><span data-stu-id="cb437-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="cb437-117">Pasirinkite **Parametrai** (viršutiniame dešiniajame kampe esantis krumpliaračio simbolis) ir pasirinkite **Administravimo centras**.</span><span class="sxs-lookup"><span data-stu-id="cb437-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="cb437-118">Skirtuko **El. pašto parametrai** dalyje **El. pašto tarnybos paskyros** pasirinkite **Prijungti įmonės paskyrą**.</span><span class="sxs-lookup"><span data-stu-id="cb437-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![Įmonės el. pašto tarnybos paskyros prijungimas naudojant „Attract“](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="cb437-120">Daugiau informacijos, kaip kurti bendrinamą el. pašto paskyrą, žr. [Bendrinamos pašto dėžutės programoje „Exchange Online“](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="cb437-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="cb437-121">„Microsoft“ prisijungimo lange prisijunkite naudodami savo įmonės kredencialus.</span><span class="sxs-lookup"><span data-stu-id="cb437-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="cb437-122">Jei dar nesate nustatę el. pašto tarnybos paskyros arba jei norite įtraukti naują, pasirinkite **Įtraukti naują tarnybos paskyrą** ir įveskite savo el. pašto paskyros informaciją.</span><span class="sxs-lookup"><span data-stu-id="cb437-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="cb437-123">Jei jau nustatėte el. pašto tarnybos paskyrą, kurią norite naudoti, pasirinkite ją.</span><span class="sxs-lookup"><span data-stu-id="cb437-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="cb437-124">Sėkmingai sukonfigūravus jūsų el. pašto tarnybos paskyrą, ji bus rodoma dalyje **El. pašto tarnybos paskyros**.</span><span class="sxs-lookup"><span data-stu-id="cb437-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="cb437-125">El. pašto tarnybos paskyros atjungimas</span><span class="sxs-lookup"><span data-stu-id="cb437-125">Disconnect an email service account</span></span>

<span data-ttu-id="cb437-126">Jei nebenorite naudoti savo įmonės domeno el. laiškuose, siunčiamuose naudojant „Attract“, galite atjungti el. pašto tarnybos paskyrą.</span><span class="sxs-lookup"><span data-stu-id="cb437-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="cb437-127">Pasirinkite **Parametrai** (viršutiniame dešiniajame kampe esantis krumpliaračio simbolis) ir pasirinkite **Administravimo centras**.</span><span class="sxs-lookup"><span data-stu-id="cb437-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="cb437-128">Skirtuko **El. pašto parametrai** dalyje **El. pašto tarnybos paskyros** pasirinkite mygtuką **Daugiau** (trys vertikalūs taškai), esantį šalia el. pašto tarnybos paskyros, kurią norite atjungti.</span><span class="sxs-lookup"><span data-stu-id="cb437-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="cb437-129">Pasirinkite **Atjungti el. pašto paskyrą**.</span><span class="sxs-lookup"><span data-stu-id="cb437-129">Select **Disconnect email account**.</span></span>

    ![Įmonės el. pašto tarnybos paskyros atjungimas](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="cb437-131">Kai būsite paraginti patvirtinti operaciją, pasirinkite **Atjungti**.</span><span class="sxs-lookup"><span data-stu-id="cb437-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Įmonės el. pašto tarnybos paskyros atjungimo patvirtinimas](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="cb437-133">Jei neprijungsite kitos el. pašto tarnybos paskyros, siunčiant el. laiškus iš „Attract“ bus naudojama numatytoji „Microsoft“ prekės ženklo el. pašto tarnybos paskyra.</span><span class="sxs-lookup"><span data-stu-id="cb437-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="cb437-134">El. pašto šablonų parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cb437-134">Configure email template settings</span></span>

<span data-ttu-id="cb437-135">Galite el. laiškų antraštėje naudoti savo įmonės logotipo vaizdą ir kitą informaciją.</span><span class="sxs-lookup"><span data-stu-id="cb437-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="cb437-136">Taip pat galite el. laiško poraštėse nurodyti savo privatumo strategijos ir naudojimo sąlygų saitų.</span><span class="sxs-lookup"><span data-stu-id="cb437-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="cb437-137">Turite laikytis ne tik visų jūsų šalyje arba regione, bet ir el. laiško gavėjo šalyje arba regione galiojančių teisės aktų.</span><span class="sxs-lookup"><span data-stu-id="cb437-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="cb437-138">Tai apima ir apsaugos nuo pašto šiukšlių nuostatas.</span><span class="sxs-lookup"><span data-stu-id="cb437-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="cb437-139">Pasirinkite **Parametrai** (viršutiniame dešiniajame kampe esantis krumpliaračio simbolis) ir pasirinkite **Administravimo centras**.</span><span class="sxs-lookup"><span data-stu-id="cb437-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="cb437-140">Skirtuko **El. pašto parametrai** dalyje **El. pašto šablonų parametrai** nuvilkite vaizdą, kurį norite naudoti kaip el. laiško antraštę, į vaizdo lauką arba spustelėkite vaizdo lauką ir raskite failą.</span><span class="sxs-lookup"><span data-stu-id="cb437-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="cb437-141">Norėdami pakeisti esamą vaizdą, pirmiausia šalia vaizdo pasirinkite **Pašalinti**.</span><span class="sxs-lookup"><span data-stu-id="cb437-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="cb437-142">Vaizdas turi būti JPEG, JPG, PNG arba SVG formato failas.</span><span class="sxs-lookup"><span data-stu-id="cb437-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="cb437-143">Rekomenduojamas vaizdų dydis: 25–800 pikselių pločio ir 25–150 pikselių aukščio.</span><span class="sxs-lookup"><span data-stu-id="cb437-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="cb437-144">Didžiausias antraštei tinkamas failo dydis yra 1 megabaitas (MB).</span><span class="sxs-lookup"><span data-stu-id="cb437-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Vaizdo įtraukimas į įmonės el. laiškų antraštę](./media/attract-admin-email-header.png)

3. <span data-ttu-id="cb437-146">Dalyje **Jūsų privatumo strategija bendravimui** nurodykite savo įmonės privatumo strategijos saitą.</span><span class="sxs-lookup"><span data-stu-id="cb437-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="cb437-147">Dalyje **Jūsų bendravimo sąlygos** nurodykite savo įmonės naudojimo sąlygų saitą.</span><span class="sxs-lookup"><span data-stu-id="cb437-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Įmonės privatumo strategijos ir naudojimo sąlygų saitų įtraukimas į el. laiško poraštę](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="cb437-149">Pasirinkite **Įrašyti**, kad įrašytumėte savo el. pašto šablono parametrus.</span><span class="sxs-lookup"><span data-stu-id="cb437-149">Select **Save** to save your email template settings.</span></span>

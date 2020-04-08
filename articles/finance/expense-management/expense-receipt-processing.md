---
title: Išlaidų kvitų apdorojimas
description: Šioje temoje pateikiama informacija apie kvitų apdorojimą naudojant optinį ženklų atpažinimą (OCR). Ši funkcija sukurta siekiant pagerinti vartotojo patirtį kuriant išlaidų ataskaitas programoje „Microsoft Dynamics 365 Finance“.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 49cdfeac8cda9f1ddd3aca61f902f00f30f3485b
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154045"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="08f21-104">Išlaidų kvitų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="08f21-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="08f21-105">Išlaidų įvedimas buvo patobulintas įvedus kvitų apdorojimą per optinį ženklų atpažinimą (OCR).</span><span class="sxs-lookup"><span data-stu-id="08f21-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="08f21-106">Ši funkcija sukurta siekiant pagerinti vartotojo patirtį kuriant išlaidų ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="08f21-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="08f21-107">Pagrindinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="08f21-107">Key features</span></span>

- <span data-ttu-id="08f21-108">Prekybininko pavadinimas, data ir bendra suma paimami iš kvitų.</span><span class="sxs-lookup"><span data-stu-id="08f21-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="08f21-109">Funkcija bando sugretinti nepridėtus kvitus su nepridėtomis išlaidų operacijomis.</span><span class="sxs-lookup"><span data-stu-id="08f21-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="08f21-110">Vartotojai gali kurti rankiniu būdu įvestas išlaidų operacijas pagal kvitus.</span><span class="sxs-lookup"><span data-stu-id="08f21-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="08f21-111">Naudojimo pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="08f21-111">Usage examples</span></span>

- <span data-ttu-id="08f21-112">**Automatiškai pridėti kvitus, kuriuose yra kredito kortelės operacijų, kai sukuriama išlaidų ataskaita.**</span><span class="sxs-lookup"><span data-stu-id="08f21-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="08f21-113">Atidarykite darbo sritį **Išlaidų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="08f21-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="08f21-114">Skirtuke **Kvitai** patikrinkite, ar yra nepridėtų kvitų.</span><span class="sxs-lookup"><span data-stu-id="08f21-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="08f21-115">Skirtuke **Kvitai** taip pat galite nusiųsti kvitus.</span><span class="sxs-lookup"><span data-stu-id="08f21-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="08f21-116">Skirtuke **Išlaidos** patikrinkite, ar yra nepridėtų išlaidų.</span><span class="sxs-lookup"><span data-stu-id="08f21-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="08f21-117">Paprastai išlaidų administratorius importuoja šias išlaidas iš kredito kortelės teikėjo.</span><span class="sxs-lookup"><span data-stu-id="08f21-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="08f21-118">Pasirinkite **Nauja išlaidų ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="08f21-118">Select **New expense report**.</span></span> <span data-ttu-id="08f21-119">Atkreipkite dėmesį, kad kurdami išlaidų ataskaitą, dabar taip pat galite į ją įtraukti išlaidų ir kvitų.</span><span class="sxs-lookup"><span data-stu-id="08f21-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="08f21-120">Jei įtrauksite ir išlaidų, ir kvitų, paleidžiamas automatinis kvitų ir išlaidų gretinimas.</span><span class="sxs-lookup"><span data-stu-id="08f21-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="08f21-121">**Sukurti išlaidas arba sugretinti išlaidas iš kvito.**</span><span class="sxs-lookup"><span data-stu-id="08f21-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="08f21-122">Išlaidų ataskaitoje skirtuke **Kvitai** pridėkite kvitą, pasirinkdami **Įtraukti kvitų**.</span><span class="sxs-lookup"><span data-stu-id="08f21-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="08f21-123">Atkreipkite dėmesį, kad po nusiųsto kvito vaizdu yra parinktys **Kurti** ir **Sugretinti**.</span><span class="sxs-lookup"><span data-stu-id="08f21-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="08f21-124">Pasirinkite **Kurti**, kad sukurtumėte rankiniu būdu įvestą išlaidų operaciją ir įvestumėte iš kvito paimtas vertes.</span><span class="sxs-lookup"><span data-stu-id="08f21-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="08f21-125">Jei pasirinksite **Sugretinti**, sistema bandys sugretinti esamas išlaidas su kvitu.</span><span class="sxs-lookup"><span data-stu-id="08f21-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="08f21-126">Diegimas</span><span class="sxs-lookup"><span data-stu-id="08f21-126">Installation</span></span>

<span data-ttu-id="08f21-127">Ši funkcija veikia kartu su funkcija **Išlaidų ataskaitos iš naujo atvaizduotos**, kad išlaidų patirtis būtų paprastesnė.</span><span class="sxs-lookup"><span data-stu-id="08f21-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="08f21-128">Norėdami naudoti šias išplėstines išlaidų galimybes, įdiekite „Microsoft Dynamics 365 Finance“ išlaidų valdymo paslaugos papildinį ir įjunkite funkcijas savo egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="08f21-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="08f21-129">Papildinį galite pasiekti iš savo projekto „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="08f21-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="08f21-130">Prisijunkite prie LCS ir atsidarykite pageidaujamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="08f21-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="08f21-131">Eikite į **Išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="08f21-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="08f21-132">Pasirinkite **Tvarkyti**arba slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="08f21-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="08f21-133">Pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="08f21-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="08f21-134">Pasirinkite **Išlaidų valdymo paslauga**.</span><span class="sxs-lookup"><span data-stu-id="08f21-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="08f21-135">Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.</span><span class="sxs-lookup"><span data-stu-id="08f21-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="08f21-136">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="08f21-136">Select **Install**.</span></span>

<span data-ttu-id="08f21-137">Darbo srityje **Funkcijų valdymas** įjunkite toliau pateikiamas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="08f21-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="08f21-138">Išlaidų ataskaitos iš naujo atvaizduotos</span><span class="sxs-lookup"><span data-stu-id="08f21-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="08f21-139">Automatiškai suderinkite ir sukurkite išlaidas pagal kvitą.</span><span class="sxs-lookup"><span data-stu-id="08f21-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="08f21-140">Kai įjungiate šias funkcijas, atliekami tolesni veiksmai.</span><span class="sxs-lookup"><span data-stu-id="08f21-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="08f21-141">Esama darbo sritis **Išlaidų valdymas** pakeičiama nauja darbo sritimi.</span><span class="sxs-lookup"><span data-stu-id="08f21-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="08f21-142">Įtrauktas naujas meniu elementas išlaidų lauko matomumui.</span><span class="sxs-lookup"><span data-stu-id="08f21-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="08f21-143">Vis tiek galite atidaryti ankstesnį puslapį **Išlaidų ataskaitos**, perėję į **Išlaidų valdymas > Mano išlaidos > Išlaidų ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="08f21-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="08f21-144">Darbo eigos ir patvirtinimai vis dar nukreipia į esamą išlaidų ataskaitų puslapį.</span><span class="sxs-lookup"><span data-stu-id="08f21-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="08f21-145">Kvitai bus apdorojami naudojant „Microsoft Azure Cognitive Services“, o metaduomenys bus gaunami ir įtraukiami.</span><span class="sxs-lookup"><span data-stu-id="08f21-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="08f21-146">Pridėta parinktis, leidžianti sukurti išlaidų ataskaitą, kurioje yra sugretintų nepridėtų kvitų.</span><span class="sxs-lookup"><span data-stu-id="08f21-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="08f21-147">Parinktis, kuri įtraukiama į išlaidų ataskaitas, leidžia sukurti išlaidų eilutę pagal kvitą arba bando sugretinti esamą kvitą ir esamą išlaidų eilutę.</span><span class="sxs-lookup"><span data-stu-id="08f21-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="08f21-148">Daugiau informacijos apie funkciją Išlaidų ataskaitos iš naujo atvaizduotos žr. [Išlaidų ataskaitos iš naujo atvaizduotos](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="08f21-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="08f21-149">Dažnai užduodami klausimai</span><span class="sxs-lookup"><span data-stu-id="08f21-149">Frequently asked questions</span></span>

<span data-ttu-id="08f21-150">**Ar „Microsoft“ savo modeliuose naudoja mano duomenis?**</span><span class="sxs-lookup"><span data-stu-id="08f21-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="08f21-151">Ne, „Microsoft“ savo kvitų apdorojimo paslaugai sukūrė bendrą mašininio mokymo modelį.</span><span class="sxs-lookup"><span data-stu-id="08f21-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="08f21-152">Šis modelis negrindžiamas kvitais, kuriuos nusiunčiate.</span><span class="sxs-lookup"><span data-stu-id="08f21-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="08f21-153">**Kur ši funkcija yra pasiekiama ir apdorojama?**</span><span class="sxs-lookup"><span data-stu-id="08f21-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="08f21-154">Šiuo metu palaikomos Jungtinės Valstijos.</span><span class="sxs-lookup"><span data-stu-id="08f21-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="08f21-155">**Kas atsitinka mano kvitams?**</span><span class="sxs-lookup"><span data-stu-id="08f21-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="08f21-156">„Finance“ susisieks su „Cognitive Services“, kad gautų laukų duomenis.</span><span class="sxs-lookup"><span data-stu-id="08f21-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="08f21-157">„Cognitive Services“ saugo jūsų kvito kopiją iki 24 valandų, kol vyksta apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="08f21-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="08f21-158">Baigus apdoroti, „Cognitive Services“ pašalins kvitą.</span><span class="sxs-lookup"><span data-stu-id="08f21-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="08f21-159">Kvitai vis tiek saugomi „Finance“.</span><span class="sxs-lookup"><span data-stu-id="08f21-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="08f21-160">Norėdami gauti daugiau informacijos, žr. [Įjungti kvitų supratimą naudojant naują formų atpažinimo funkcijos galimybę](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="08f21-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>

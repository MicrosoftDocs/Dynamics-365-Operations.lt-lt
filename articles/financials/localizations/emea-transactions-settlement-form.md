---
title: "Sudengimo operacijų peržiūra (Rytų Europa)"
description: "Šioje temoje pateikiama informacija apie klientų ir tiekėjų puslapį Sudengimo operacijos."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustVendTransPostingLog_RU
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 270544
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 00c7ae430cbcf92b211a3525ff8b41e042b033e4
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="view-transactions-on-settlement-for-eastern-europe"></a><span data-ttu-id="dbb01-103">Sudengimo operacijų peržiūra (Rytų Europa)</span><span class="sxs-lookup"><span data-stu-id="dbb01-103">View transactions on settlement for Eastern Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="dbb01-104">Šioje temoje pateikiama informacija apie klientų ir tiekėjų puslapį Sudengimo operacijos.</span><span class="sxs-lookup"><span data-stu-id="dbb01-104">This topic provides information about the Transactions on settlement page for customers and vendors.</span></span>

<span data-ttu-id="dbb01-105">Naudokite puslapį **Sudengimo operacijos**, norėdami peržiūrėti informaciją apie sudėtingas kliento arba tiekėjo sudengimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="dbb01-105">Use the **Transactions on settlement** page to view information about complex settlement transactions for a customer or a vendor.</span></span> <span data-ttu-id="dbb01-106">Šią funkciją gali naudoti juridiniai subjektai, kurių pagrindinis adresas yra Lietuvoje, Latvijoje, Estijoje, Čekijos Respublikoje, Vengrijoje Lenkijoje.</span><span class="sxs-lookup"><span data-stu-id="dbb01-106">This feature is available only for legal entities that have their primary address in Lithuania, Latvia, Estonia, Czech Republic, Hungary, or Poland.</span></span> <span data-ttu-id="dbb01-107">Puslapį **Sudengimo operacijos** galite rasti toliau nurodytose vietose.</span><span class="sxs-lookup"><span data-stu-id="dbb01-107">You can find the **Transactions on settlement** page at the following locations:</span></span>

-   <span data-ttu-id="dbb01-108">**Mokėtinos sumos** &gt; **Tiekėjai** &gt; **Visi tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="dbb01-108">**Accounts payable** &gt; **Vendors** &gt; **All vendors**.</span></span> <span data-ttu-id="dbb01-109">Veiksmų srities skirtuke **Tiekėjas** spustelėkite **Operacijos** &gt; **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="dbb01-109">On the Action Pane, on the **Vendor** tab, click **Transactions** &gt; **Transactions**.</span></span> <span data-ttu-id="dbb01-110">Puslapyje **Tiekėjo operacijos** pasirinkite operaciją, o tada spustelėkite **Sudengimo operacijos**.</span><span class="sxs-lookup"><span data-stu-id="dbb01-110">On the **Vendor transactions** page, select a transaction, and then click **Transactions on settlement**.</span></span>
-   <span data-ttu-id="dbb01-111">**Gautinos sumos** &gt; **Klientai** &gt; **Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="dbb01-111">**Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span> <span data-ttu-id="dbb01-112">Veiksmų srities skirtuke **Klientas** spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="dbb01-112">On the Action Pane, on the **Customer** tab, click **Transactions**.</span></span> <span data-ttu-id="dbb01-113">Puslapyje **Kliento operacijos** pasirinkite operaciją, o tada spustelėkite **Sudengimo operacijos**.</span><span class="sxs-lookup"><span data-stu-id="dbb01-113">On the **Customer transactions** page, select a transaction, and then click **Transactions on settlement**.</span></span>

<span data-ttu-id="dbb01-114">Su sudengimu susijusi informacija yra išsaugoma ir ją galima peržiūrėti puslapyje **Sudengimo operacijos**, jei operacijos buvo sukurtos pagal vieną iš toliau pateiktų scenarijų.</span><span class="sxs-lookup"><span data-stu-id="dbb01-114">Settlement-related information is captured and can be shown on the **Transactions on settlement** page for transactions that were created in the following scenarios:</span></span>

-   <span data-ttu-id="dbb01-115">**Derinimas dėl valiutos kurso** – SF sudengimas ir mokėjimas generuoja realizuotą arba nerealizuotą valiutos kurso skirtumą.</span><span class="sxs-lookup"><span data-stu-id="dbb01-115">**Exchange adjustment** – Settlement of an invoice and a payment generates a realized or unrealized exchange rate difference.</span></span>
-   <span data-ttu-id="dbb01-116">**Registravimo profilis pakeitimas** – sudengiami du įrašai, pvz., SF ir kredito pažyma, kurių registravimo profiliai yra skirtingi.</span><span class="sxs-lookup"><span data-stu-id="dbb01-116">**Posting profile change** – Two entries, such as an invoice and a credit memo, that have different posting profiles are settled.</span></span>
-   <span data-ttu-id="dbb01-117">Išankstinis apmokėjimas konvertuojamas į mokėjimą arba mokėjimas konvertuojamas į išankstinį apmokėjimą.</span><span class="sxs-lookup"><span data-stu-id="dbb01-117">A prepayment is converted to a payment, or a payment is converted to a prepayment.</span></span>
-   <span data-ttu-id="dbb01-118">**Mokėjimo nuolaida** – sudengiama SF su mokėjimu, iš kurio atskaityta nuolaidos suma.</span><span class="sxs-lookup"><span data-stu-id="dbb01-118">**Cash discount** – An invoice is settled with a payment that a discount amount has been deducted from.</span></span>
-   <span data-ttu-id="dbb01-119">**Skirtumas centais** – sudengiama SF su mokėjimu, kurio suma šiek tiek skiriasi nuo SF sumos.</span><span class="sxs-lookup"><span data-stu-id="dbb01-119">**Penny difference** – An invoice is settled with a payment that has a slightly different amount than the invoice.</span></span>
-   <span data-ttu-id="dbb01-120">**Sąlyginis mokesčių registravimas** sudengiama SF su mokėjimu, kuriam pritaikytas sąlyginis mokestis.</span><span class="sxs-lookup"><span data-stu-id="dbb01-120">**Conditional tax posting** – An invoice is settled with a payment that conditional tax has been applied to.</span></span>
-   <span data-ttu-id="dbb01-121">**Visų įmonių sudengimas** – vidinės įmonės funkcija naudojama norint sudengti SF su mokėjimu iš organizacijos.</span><span class="sxs-lookup"><span data-stu-id="dbb01-121">**Cross-company settlement** – Intercompany functionality is used to settle an invoice with a payment from an organization.</span></span>






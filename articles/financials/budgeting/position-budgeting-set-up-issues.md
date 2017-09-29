---
title: "Pareigų biudžeto trikčių šalinimas"
description: "Šiame straipsnyje pateikiami atsakymai į klausimus, kurie gali kilti, kai konfigūruojate pareigų biudžetą. Ji skirta dažnai užduodami klausimai apie tai, kaip sukurti biudžeto išlaidų elementus, kompensacijų grupes ir kompensavimo tinklelius."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 421520fcd1b215a19c126ccea51b025977552448
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="cee07-104">Pareigų biudžeto trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="cee07-104">Position budgeting troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cee07-105">Šiame straipsnyje pateikiami atsakymai į klausimus, kurie gali kilti, kai konfigūruojate pareigų biudžetą.</span><span class="sxs-lookup"><span data-stu-id="cee07-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="cee07-106">Ji skirta dažnai užduodami klausimai apie tai, kaip sukurti biudžeto išlaidų elementus, kompensacijų grupes ir kompensavimo tinklelius.</span><span class="sxs-lookup"><span data-stu-id="cee07-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="cee07-107">Kodėl modulyje Personalas nerandu prognozuojamų pareigų puslapio?</span><span class="sxs-lookup"><span data-stu-id="cee07-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="cee07-108">Prognozuojamos pareigos perkeltos į modulį Biudžeto sudarymas.</span><span class="sxs-lookup"><span data-stu-id="cee07-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="cee07-109">Kodėl negaliu panaikinti biudžeto išlaidų elemento?</span><span class="sxs-lookup"><span data-stu-id="cee07-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="cee07-110">Negalite panaikinti biudžeto išlaidų elemento, kuris priskirtas prognozuojamoms pareigoms.</span><span class="sxs-lookup"><span data-stu-id="cee07-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="cee07-111">Biudžeto išlaidų elemento panaikinti negalėsite tol, kol jo nepašalinsite iš visų prognozuojamų pareigų.</span><span class="sxs-lookup"><span data-stu-id="cee07-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="cee07-112">**Patarimas.** Norėdami rasti visas pareigas, kurioms priskirtas biudžeto išlaidų elementas, tą išlaidų elementą pasirinkite puslapyje **Biudžeto išlaidų elementai** ir spustelėkite **Naujinti pareigas**.</span><span class="sxs-lookup"><span data-stu-id="cee07-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="cee07-113">Pareigos, naudojančios išlaidų elementą yra pateiktos viršutiniame tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="cee07-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="cee07-114">Kaip pašalinti išlaidų elementą iš kelių prognozuojamų pareigų neatidarius kiekvienos?</span><span class="sxs-lookup"><span data-stu-id="cee07-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="cee07-115">Išlaidų elemento pašalinti negalite.</span><span class="sxs-lookup"><span data-stu-id="cee07-115">You can’t remove a cost element.</span></span> <span data-ttu-id="cee07-116">Tačiau, jei pakeisite pradžios ir pabaigos datas taip, kad jos nepatektų į biudžeto planavimo ciklo datų intervalą, išlaidų elementas nebebus priskirtas prognozuojamoms pareigoms tame biudžeto planavimo cikle.</span><span class="sxs-lookup"><span data-stu-id="cee07-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="cee07-117">Norėdami atlikti šį keitimą, atidarykite biudžeto išlaidų elementą, „FastTab‟ skirtuke **Išlaidų skaičiavimas** spustelėkite **Keisti datas** ir pakeiskite įsigaliojimo datą arba galiojimo pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="cee07-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="cee07-118">Tada spustelėkite **Gerai** – bus automatiškai atnaujintos visos prognozuojamos pareigos, kurioms priskirtas išlaidų elementas.</span><span class="sxs-lookup"><span data-stu-id="cee07-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="cee07-119">**Patarimas.** Jei naudosite šį metodą, turėkite omenyje, kad jis pašalina biudžeto išlaidų elementą iš **visų** prognozuojamų pareigų, kurių pradžios ir pabaigos datos nebėra reikiamame intervale.</span><span class="sxs-lookup"><span data-stu-id="cee07-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="cee07-120">Jei tai yra ne tai, ką norite padaryti, turėsite atidaryti visas prognozuojamas pareigas, iš kurių norite pašalinti biudžeto išlaidų elementą ir rankiniu būdu atlikti pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="cee07-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="cee07-121">Kodėl biudžeto išlaidų elemento „FastTab‟ skirtuke Išlaidų skaičiavimas negalima įvesti metinės sumos?</span><span class="sxs-lookup"><span data-stu-id="cee07-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="cee07-122">Metinės sumos negalite įvesti, jei biudžeto išlaidų elementai yra „FastTab‟ skirtuke **Skaičiavimo pagrindas**, nes sistemai reikia procentų reikšmei apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="cee07-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="cee07-123">Norėdami reikšmę pakeisti, iš „FastTab‟ skirtuko **Skaičiavimo pagrindas** pašalinkite visus biudžeto išlaidų elementus.</span><span class="sxs-lookup"><span data-stu-id="cee07-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="cee07-124">Kodėl negaliu keisti biudžeto išlaidų tipo „uždarbis“ į kitą biudžeto išlaidų tipą?</span><span class="sxs-lookup"><span data-stu-id="cee07-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="cee07-125">Kai kurie biudžeto išlaidų elementai išlaidų elementą „uždarbis“ naudoja kaip skaičiavimo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="cee07-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="cee07-126">Norėdami lauką **Biudžeto išlaidų tipas** pakeisti, iš visų biudžeto išlaidų elementų „FastTab‟ skirtukų **Skaičiavimo pagrindas** pašalinkite uždarbio išlaidų elementą.</span><span class="sxs-lookup"><span data-stu-id="cee07-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="cee07-127">Kodėl negaliu keisti d tos biudžeto išlaidų elemento biudžeto išlaidų elemento eilutėse?</span><span class="sxs-lookup"><span data-stu-id="cee07-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="cee07-128">Negalite pakeisti datos biudžeto išlaidų elementų eilutėje, kai biudžeto išlaidų elementas naudojamas prognozuojamoms pareigoms.</span><span class="sxs-lookup"><span data-stu-id="cee07-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="cee07-129">Šis apribojimas skirtas užtikrinti, kad prognozuojamos pareigos visada yra biudžeto išlaidų elemento gairėse.</span><span class="sxs-lookup"><span data-stu-id="cee07-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="cee07-130">Norėdami datą pakeisti, „FastTab‟ skirtuke **Išlaidų skaičiavimas** spustelėkite **Keisti datas** ir įveskite naująsias datas.</span><span class="sxs-lookup"><span data-stu-id="cee07-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="cee07-131">Tada spustelėkite **Gerai** – bus atnaujintos pareigos, kurioms priskirtas išlaidų elementas.</span><span class="sxs-lookup"><span data-stu-id="cee07-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="cee07-132">Kodėl negaliu keisti biudžeto išlaidų elemento išlaidų puslapyje Kompensacijų grupė?</span><span class="sxs-lookup"><span data-stu-id="cee07-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="cee07-133">Kurti ir keisti biudžeto išlaidų elementus galite tik puslapyje **Biudžeto išlaidų elementai**.</span><span class="sxs-lookup"><span data-stu-id="cee07-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="cee07-134">Kodėl gaunu klaidos pranešimą, kai keičiu išlaidų elemento datą prognozuojamoms pareigoms?</span><span class="sxs-lookup"><span data-stu-id="cee07-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="cee07-135">Datos prognozuojamų pareigų išlaidų elemento eilutėje turi tilpti į tolesnius intervalus.</span><span class="sxs-lookup"><span data-stu-id="cee07-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="cee07-136">Pareigų aktyvinimo ir galiojimo pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="cee07-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="cee07-137">Biudžeto išlaidų elemento aktyvinimo ir galiojimo pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="cee07-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="cee07-138">Biudžeto ciklo, susieto su biudžeto planavimo procesu prognozuojamoms pareigoms, pradžios ir pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="cee07-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>





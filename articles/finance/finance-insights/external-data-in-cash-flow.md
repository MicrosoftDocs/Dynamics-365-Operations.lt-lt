---
title: Išorinių duomenų naudojimas prognozuojant grynųjų pinigų srautus (peržiūros versija)
description: Šioje temoje aprašomi nustatymo veiksmai, kuriuos reikia atlikti, kad išoriniai duomenys galėtų būti įvedami arba importuojami į pinigų srautų prognozes.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 03318eaae0b3329dc758c48202f8f47ca2c4ab08
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245573"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="eb36c-103">Išorinių duomenų naudojimas prognozuojant grynųjų pinigų srautus (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="eb36c-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="eb36c-104">Išorinius duomenis galima įvesti arba importuoti į pinigų srautų prognozes.</span><span class="sxs-lookup"><span data-stu-id="eb36c-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="eb36c-105">Šioje temoje aprašomi nustatymo veiksmai, būdingi išorinių duomenų naudojimui ir įgalinantys išorinius duomenis įtraukti į pinigų srautų prognozę.</span><span class="sxs-lookup"><span data-stu-id="eb36c-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="eb36c-106">Išorinių duomenų nustatymas</span><span class="sxs-lookup"><span data-stu-id="eb36c-106">External data setup</span></span>

<span data-ttu-id="eb36c-107">Norėdami įvesti parametrus, palaikančius išorinių duomenų naudojimą grynųjų pinigų srautų prognozėse, naudokite skirtuką **Išorinis šaltinis**, esantį puslapyje **Grynųjų pinigų srautų prognozės sąranka** (**Grynųjų pinigų ir banko valdymas \> Grynųjų pinigų srauto prognozavimas**).</span><span class="sxs-lookup"><span data-stu-id="eb36c-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="eb36c-108">Daugiau informacijos, kaip nustatyti skaitiklius, žr. [Grynųjų pinigų srauto prognozė](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="eb36c-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="eb36c-109">Norėdami įvesti išorinius pinigų srautų prognozių duomenis, galite naudotis „Excel“ patirtimi, kad galėtumėte įvesti ir modifikuoti išorinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="eb36c-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="eb36c-110">Pasirinkite mygtuką **Išoriniai duomenys**, tada pasirinkite **Įtraukti išorinius duomenis** arba **Redaguoti esamus išorinius duomenis**.</span><span class="sxs-lookup"><span data-stu-id="eb36c-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="eb36c-111">Atidarę „Microsoft Excel“ failą, galite įvesti informaciją šiuose laukuose.</span><span class="sxs-lookup"><span data-stu-id="eb36c-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="eb36c-112">**Įrašo ID**</span><span class="sxs-lookup"><span data-stu-id="eb36c-112">**Entry ID**</span></span>
- <span data-ttu-id="eb36c-113">**Aprašas** (nebūtinas)</span><span class="sxs-lookup"><span data-stu-id="eb36c-113">**Description** (optional)</span></span>
- <span data-ttu-id="eb36c-114">**Išorinis šaltinio pavadinimas** – pasirinkite vieną iš sąrašo reikšmių, kurias nurodėte nustatydami finansines įžvalgas.</span><span class="sxs-lookup"><span data-stu-id="eb36c-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="eb36c-115">**Juridinis subjektas**</span><span class="sxs-lookup"><span data-stu-id="eb36c-115">**Legal Entity**</span></span>
- <span data-ttu-id="eb36c-116">**Data**</span><span class="sxs-lookup"><span data-stu-id="eb36c-116">**Date**</span></span>
- <span data-ttu-id="eb36c-117">**Suma operacijos valiuta**</span><span class="sxs-lookup"><span data-stu-id="eb36c-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="eb36c-118">**Valiutos kodas**</span><span class="sxs-lookup"><span data-stu-id="eb36c-118">**Currency Code**</span></span>
- <span data-ttu-id="eb36c-119">**Numatytoji dimensija** (pasirinktinai)</span><span class="sxs-lookup"><span data-stu-id="eb36c-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="eb36c-120">**Dokumento numeris** (pasirinktinai)</span><span class="sxs-lookup"><span data-stu-id="eb36c-120">**Document number** (optional)</span></span>
- <span data-ttu-id="eb36c-121">**Sąskaitos numeris** (pasirinktinai)</span><span class="sxs-lookup"><span data-stu-id="eb36c-121">**Account number** (optional)</span></span>
- <span data-ttu-id="eb36c-122">**Sąskaitos pavadinimas** (pasirinktinai)</span><span class="sxs-lookup"><span data-stu-id="eb36c-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="eb36c-123">Išorinių duomenų importavimas naudojant duomenų valdymo sistemą</span><span class="sxs-lookup"><span data-stu-id="eb36c-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="eb36c-124">Naudodami darbo sritį **Duomenų valdymas** ir objektą, pavadintą **Grynųjų pinigų srauto prognozės išorinio šaltinio įrašas**, galite importuoti duomenis, skirtus grynųjų pinigų srautų prognozėms.</span><span class="sxs-lookup"><span data-stu-id="eb36c-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="eb36c-125">Be to, jei reikia perkelti nustatymo duomenis iš vienos aplinkos į kitą, reikia nustatyti šias objektų sritis, kurias galima nustatyti atliekant nustatymo lenteles:</span><span class="sxs-lookup"><span data-stu-id="eb36c-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="eb36c-126">Grynųjų pinigų srauto prognozės išorinio šaltinio nustatymas</span><span class="sxs-lookup"><span data-stu-id="eb36c-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="eb36c-127">Grynųjų pinigų srauto prognozės išorinio šaltinio juridinio subjekto nustatymas</span><span class="sxs-lookup"><span data-stu-id="eb36c-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="eb36c-128">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="eb36c-128">Privacy notice</span></span>
<span data-ttu-id="eb36c-129">Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="eb36c-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
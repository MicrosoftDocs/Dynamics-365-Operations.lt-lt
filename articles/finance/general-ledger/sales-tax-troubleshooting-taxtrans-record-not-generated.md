---
title: TaxTrans įrašas nesugeneruojamas
description: Šioje temoje pateikiama trikčių diagnostikos informacija, kuri gali padėti, kai „TaxTrans“ įrašas nėra kuriamas.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947679"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="9a127-103">TaxTrans įrašas nesugeneruojamas</span><span class="sxs-lookup"><span data-stu-id="9a127-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a127-104">Jei pasirenkate operacijos užregistruotą PVM, bet užregistruoto PVM puslapyje nėra mokesčio eilučių arba trūksta mokesčio eilutės, „TaxTrans“ įrašas **galėjo** **būti** **nesugeneruotas**.</span><span class="sxs-lookup"><span data-stu-id="9a127-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="9a127-105">[![Užregistruotas PVM puslapis, kuriame nėra eilučių elementų](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="9a127-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="9a127-106">Norėdami išspręsti šią problemą, atlikite tolesniuose skyriuose nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9a127-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="9a127-107">Pvm tikrinimas prieš užregistruojant operaciją</span><span class="sxs-lookup"><span data-stu-id="9a127-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="9a127-108">Prieš registruodami operaciją, SF **registravimo** puslapyje pasirinkite **PVM, norėdami patikrinti** skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="9a127-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="9a127-109">[![PVM mygtukas SF registravimo puslapyje](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="9a127-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="9a127-110">Laikinų **PVM operacijų puslapyje** peržiūrėkite skaičiavimo rezultatą.</span><span class="sxs-lookup"><span data-stu-id="9a127-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="9a127-111">Jei mokestis nėra skaičiuojamas, [žr. mokestis nesuskaičiuotas arba mokesčio suma yra](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md) nulis.</span><span class="sxs-lookup"><span data-stu-id="9a127-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="9a127-112">Rasti TaxTrans įrašą visuose užregistruotuose PVM</span><span class="sxs-lookup"><span data-stu-id="9a127-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="9a127-113">Eikite į **Mokestis** \> **Užklausos ir ataskaitos** \> **ataskaitos** > **Registruotas PVM**.</span><span class="sxs-lookup"><span data-stu-id="9a127-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="9a127-114">Kvito **stulpelio** antraštėje pasirinkite filtro simbolį, kad rastumėte **TaxTrans** įrašą.</span><span class="sxs-lookup"><span data-stu-id="9a127-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="9a127-115">Jei radote PVM įrašus, kurių ieškote, patikrinkite datą.</span><span class="sxs-lookup"><span data-stu-id="9a127-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="9a127-116">Jei data skiriasi nuo žurnalo antraštės datos, sukurkite „Microsoft“ aptarnavimo papildomos pagalbos užklausą.</span><span class="sxs-lookup"><span data-stu-id="9a127-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="9a127-117">[![Registruoto PVM puslapis](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="9a127-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="9a127-118">Derinti norint patikrinti informaciją</span><span class="sxs-lookup"><span data-stu-id="9a127-118">Debug to check details</span></span>

1. <span data-ttu-id="9a127-119">Norėdami gauti informacijos, kaip suderinti ir nustatyti, ar **TmpTaxWorkTrans ir TaxUncommitted sugeneruota teisingai, žr.** **TaxTrans** [lauko](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md) vertę.</span><span class="sxs-lookup"><span data-stu-id="9a127-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="9a127-120">Jei TaxTmpWorkTrans arba TaxUncommitted sugeneruotas teisingai, pridėkite stabdos **tašką** **TaxPost** **SaveAndPost::() ir** **Mokesčių ::saveAndPost,** **kad** būtų suderinti TaxTrans įterpimo priežastis.</span><span class="sxs-lookup"><span data-stu-id="9a127-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="9a127-121">[![Kode įtraukti stabdos taškai](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="9a127-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="9a127-122">[![Pridėtų stabdos taškų rezultatai](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="9a127-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="9a127-123">Nustatyti, ar yra tinkinimas</span><span class="sxs-lookup"><span data-stu-id="9a127-123">Determine whether customization exists</span></span>

<span data-ttu-id="9a127-124">Jei atlikote veiksmus ankstesniuose skyriuose, bet neradote problemos, nustatykite, ar yra tinkinimas.</span><span class="sxs-lookup"><span data-stu-id="9a127-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="9a127-125">Jei tinkinimo nėra, sukurkite „Microsoft" aptarnavimo užklausą, kad ji būtų tolimesnė.</span><span class="sxs-lookup"><span data-stu-id="9a127-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

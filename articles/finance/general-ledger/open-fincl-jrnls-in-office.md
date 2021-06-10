---
title: Finansinių žurnalų šablonų atidarymas „Office“
description: Šioje temoje aprašomos problemos, kurios gali kilti kuriant pasirinktinius finansinius žurnalus naudojant „Microsoft Excel“ šabloną.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089462"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="f7541-103">Finansinių žurnalų šablonų atidarymas „Office“</span><span class="sxs-lookup"><span data-stu-id="f7541-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7541-104">Šioje temoje aprašomos problemos, kurios gali kilti kuriant pasirinktinius finansinius žurnalus naudojant „Microsoft Excel“ šabloną.</span><span class="sxs-lookup"><span data-stu-id="f7541-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="f7541-105">Požymis</span><span class="sxs-lookup"><span data-stu-id="f7541-105">Symptom</span></span>

<span data-ttu-id="f7541-106">Sukūrėte pasirinktinį finansinių žurnalų „Excel“ šabloną, bet jis nerodomas meniu **Atidaryti eilutes programoje „Excel“**.</span><span class="sxs-lookup"><span data-stu-id="f7541-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="f7541-107">Arba jis rodomas meniu, tačiau jį pasirinkus atidaromas kitas šablonas.</span><span class="sxs-lookup"><span data-stu-id="f7541-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="f7541-108">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="f7541-108">Resolution</span></span>

<span data-ttu-id="f7541-109">Numatytoji atidarymo programoje „Excel“ funkcija naudoja dabartinio puslapio šakninį duomenų šaltinį (lentelę) nustatyti, kurie „Office“ šablonai ar duomenų objektai rodomi kaip parinktys meniu **Atidaryti programoje „Excel“**.</span><span class="sxs-lookup"><span data-stu-id="f7541-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="f7541-110">Tai nėra geriausias finansinių žurnalų veikimo būdas, nes finansiniai žurnalai naudoja tas pačias lenteles (LedgerJournalTable ir LedgerJournalTrans) kaip daugelio kitų žurnalų tipų šakninį duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="f7541-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="f7541-111">Finansinių žurnalų funkcija Atidaryti eilutes programoje „Excel“ skirta šablonams, sukurtiems žurnalui, su kuriuo šiuo metu dirbate, pavyzdžiui, bendrajam žurnalui arba mokėjimų žurnalui, rodyti.</span><span class="sxs-lookup"><span data-stu-id="f7541-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="f7541-112">Pavyzdžiui, šablonas, kurį norite naudoti su tiekėjo mokėjimų žurnalu, bus sukurtas jūsų pirminei sąskaitai kaip tiekėjo sąskaitai vykdyti.</span><span class="sxs-lookup"><span data-stu-id="f7541-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="f7541-113">Jei norite paaukštinti šabloną, kad jis būtų prieinamas meniu **Atidaryti eilutes programoje „Excel“** ir **Atidaryti programoje „Excel“**, kūrėjai paprasčiausia gali įdiegti sąsają **LedgerIJournalExcelTemplate** ir išplėsti klasę **DocuTemplateRegistrationBase**.</span><span class="sxs-lookup"><span data-stu-id="f7541-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="f7541-114">Sistemoje įdiegta daug šio metodo pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="f7541-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="f7541-115">Vienas pavyzdys, kurį galima naudoti kaip nuorodą, yra sąsaja **LedgerDailyJournalExcelTemplate**, kuri buvo sukurta bendrajam žurnalui (arba kasdieniam žurnalui).</span><span class="sxs-lookup"><span data-stu-id="f7541-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="f7541-116">Kai sąsaja **LedgerIJournalExcelTemplate** įdiegta jūsų šablonui, meniu **Atidaryti eilutes programoje „Excel“** išfiltruos šablonus pagal jūsų žurnalo tipą ir rodys tik tam žurnalui galimus šablonus.</span><span class="sxs-lookup"><span data-stu-id="f7541-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="f7541-117">Sąsaja taip pat pateikia tikrinimo metodą, kuris užtikrina, kad žurnalo šablono negalima atidaryti, jei jis neatitinka sąskaitos tipo reikalavimų.</span><span class="sxs-lookup"><span data-stu-id="f7541-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="f7541-118">Pavyzdžiui, galite nurodyti, kad sąskaitos tipas turi būti **Tiekėjas** arba **Didžioji knyga**.</span><span class="sxs-lookup"><span data-stu-id="f7541-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="f7541-119">Daugiau informacijos apie šią funkciją žr. [Šablonų įtraukimas į meniu Atidaryti eilutes programoje „Excel“](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="f7541-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>

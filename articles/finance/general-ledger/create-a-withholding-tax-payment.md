---
title: Sukurkite mokesčių mokėjimo sustabdymą
description: Mokesčių mokėjimo sustabdymo darbo procedūra nustato mokesčių balanso sustabdymą mokėtinoms sąskaitoms dėl sustabdomų mokesčių sąskaitų ir jas paleidžia į sustabdytą mokesčių nustatymo sąskaitą už nustatytą laikotarpį. Šioje temoje išvardyti žingsniai, kuriais galima nustatyti sustabdytą mokesčių mokėjimą.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: eae914ccafad12426cadd91c0950bada23548005
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212282"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="c3fd6-104">Sukurkite mokesčių mokėjimo sustabdymą</span><span class="sxs-lookup"><span data-stu-id="c3fd6-104">Create a withholding tax payment</span></span>

<span data-ttu-id="c3fd6-105">Mokesčių mokėjimo sustabdymo darbo procedūra nustato mokesčių balanso sustabdymą mokėtinoms sąskaitoms dėl sustabdomų mokesčių sąskaitų ir jas paleidžia į sustabdytą mokesčių nustatymo sąskaitą už nustatytą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="c3fd6-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="c3fd6-106">Šioje temoje išvardyti žingsniai, kuriais galima nustatyti sustabdytą mokesčių mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="c3fd6-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="c3fd6-107">Sustabdyto mokesčio paleidimas (iš gautinų sąskaitų) nėra priimamas domėn, kai sustabdymo mokesio mokėjimas yra skaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="c3fd6-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="c3fd6-108">Eiktie į **Naršymo juostą > Moduliia > Mokesčiai > Deklaracijos > Sustabdyti mokesčiai > Sustabdytas mokesčio mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="c3fd6-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="c3fd6-109">Lauke **Sudengimo laikotarpis** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="c3fd6-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c3fd6-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c3fd6-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c3fd6-111">Lauke **Pradžios data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="c3fd6-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="c3fd6-112">Lauke **Operacijos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="c3fd6-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="c3fd6-113">Rinkitės **Naujinti** tam, kad publikuotumėte sustabdytą mokesčio mokėjimo kuponą į sustabdymo mokesčio nustatymo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="c3fd6-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="c3fd6-114">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c3fd6-114">Click **OK**.</span></span>

![Sustabdymo mokesčio mokėjimo parametrai](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
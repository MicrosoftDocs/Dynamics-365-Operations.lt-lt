---
title: Visuotinis išskaitomas mokestis
description: Šioje temoje patiekiama informacija apie visuotino išskaitomo mokesčio funkcijas ir kaip jas nustatyti. Visuotino išskaitomo mokesčio funkcijos yra padidintos pardavėjo ir kliento transakcijoms taip, kad išskaitomas mokestis yra apskaičiuojamas prekės lygiu.
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
ms.openlocfilehash: 25fc503d6145872b8e9f28b8d9a4d7b9c1ba53a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249172"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="a3b78-104">Visuotinis išskaitomas mokestis</span><span class="sxs-lookup"><span data-stu-id="a3b78-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3b78-105">Šioje temoje patiekiama informacija apie visuotino išskaitomo mokesčio funkcijas ir paaiškinta, kaip jas nustatyti.</span><span class="sxs-lookup"><span data-stu-id="a3b78-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="a3b78-106">Naujos funkcijos yra prieinamos 10.0.17 versijoje ir vėlesnėse.</span><span class="sxs-lookup"><span data-stu-id="a3b78-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="a3b78-107">Visuotino išskaitomo mokesčio funkcijos yra padidintos pardavėjo ir kliento transakcijoms taip, kad išskaitomas mokestis yra apskaičiuojamas prekės lygiu.</span><span class="sxs-lookup"><span data-stu-id="a3b78-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="a3b78-108">Balansas išskaitomo mokesčio sąskaitoje nuo pirkimo transakcijų gali būti nustatytas vykdant išskaitomo mokesčio mokėjimo darbą pagal išskaitomo mokesčio nustatymo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="a3b78-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="a3b78-109">Visuotinis išskaitomas mokestis nepalaiko **Palaikymo keitimai** funkcijos įsigijimo užsakymo, pardavėjo sąskaitoje ir prekybos užsakymo puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="a3b78-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="a3b78-110">Įjunkite visuotinį išskaitymo mokestį</span><span class="sxs-lookup"><span data-stu-id="a3b78-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="a3b78-111">Darbo srityje **Funkcijos valdymas** rinkitės **Visuotinis išskaitomas mokestis** ir tada rinkiės **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="a3b78-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="a3b78-112">Eikiteį **Mokestis \> Nustatymai \> Parameterai \> Bendri sąskaitų knygos parametrai** ir tada **Išskaitomo mokesčio** skirtuke, nustatykite **Įjungti visuotinį išskaitomą mokestį** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a3b78-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="a3b78-113">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a3b78-113">Select **Save**.</span></span>
4. <span data-ttu-id="a3b78-114">Naujinkite puslapį savo žiniatinklio naršyklėje.</span><span class="sxs-lookup"><span data-stu-id="a3b78-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="a3b78-115">Visuotinio išskaitomo mokesčio funkcija negali būti įjungta šalims ar regionams, kuriuose lokalizuojami išskaitomo mokesčio sprendimai jau egzistuoja.</span><span class="sxs-lookup"><span data-stu-id="a3b78-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="a3b78-116">Šios sritys apima, tačiau neapsiriboja Indija, Brazilija, Tailandu, Saudo Arabija, Airija, Didžiąja Britanija ir Jungtinėmis Amerikos Valstijomis.</span><span class="sxs-lookup"><span data-stu-id="a3b78-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
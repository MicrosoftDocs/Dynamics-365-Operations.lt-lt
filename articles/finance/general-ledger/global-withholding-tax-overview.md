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
ms.openlocfilehash: 17ed1dcae97f6cd28175c483be5ca3ce96d59e05
ms.sourcegitcommit: 053f4cda6862fbcd9e3aa6e9cb009e7de833beac
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/28/2021
ms.locfileid: "5075743"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="0408c-104">Visuotinis išskaitomas mokestis</span><span class="sxs-lookup"><span data-stu-id="0408c-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0408c-105">Šioje temoje patiekiama informacija apie visuotino išskaitomo mokesčio funkcijas ir paaiškinta, kaip jas nustatyti.</span><span class="sxs-lookup"><span data-stu-id="0408c-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="0408c-106">Naujos funkcijos yra prieinamos 10.0.17 versijoje ir vėlesnėse.</span><span class="sxs-lookup"><span data-stu-id="0408c-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="0408c-107">Visuotino išskaitomo mokesčio funkcijos yra padidintos pardavėjo ir kliento transakcijoms taip, kad išskaitomas mokestis yra apskaičiuojamas prekės lygiu.</span><span class="sxs-lookup"><span data-stu-id="0408c-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="0408c-108">Balansas išskaitomo mokesčio sąskaitoje nuo pirkimo transakcijų gali būti nustatytas vykdant išskaitomo mokesčio mokėjimo darbą pagal išskaitomo mokesčio nustatymo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="0408c-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="0408c-109">Visuotinis išskaitomas mokestis nepalaiko **Palaikymo keitimai** funkcijos įsigijimo užsakymo, pardavėjo sąskaitoje ir prekybos užsakymo puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="0408c-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="0408c-110">Įjunkite visuotinį išskaitymo mokestį</span><span class="sxs-lookup"><span data-stu-id="0408c-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="0408c-111">Darbo srityje **Funkcijos valdymas** rinkitės **Visuotinis išskaitomas mokestis** ir tada rinkiės **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="0408c-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="0408c-112">Eikiteį **Mokestis \> Nustatymai \> Parameterai \> Bendri sąskaitų knygos parametrai** ir tada **Išskaitomo mokesčio** skirtuke, nustatykite **Įjungti visuotinį išskaitomą mokestį** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0408c-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="0408c-113">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0408c-113">Select **Save**.</span></span>
4. <span data-ttu-id="0408c-114">Naujinkite puslapį savo žiniatinklio naršyklėje.</span><span class="sxs-lookup"><span data-stu-id="0408c-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="0408c-115">Visuotinio išskaitomo mokesčio funkcija negali būti įjungta šalims ar regionams, kuriuose lokalizuojami išskaitomo mokesčio sprendimai jau egzistuoja.</span><span class="sxs-lookup"><span data-stu-id="0408c-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="0408c-116">Šios sritys apima, tačiau neapsiriboja Indija, Brazilija, Tailandu, Saudo Arabija, Airija, Didžiąja Britanija ir Jungtinėmis Amerikos Valstijomis.</span><span class="sxs-lookup"><span data-stu-id="0408c-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>
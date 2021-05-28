---
title: Parametrų mokėtinos sąskaitose ir gautinose sąskaitose TDS nustatymas
description: Šioje temoje aiškinama, kaip nustatyti mokėtinų sumų ir gautinų sumų parametrus, kad būtų palaikomi šaltinio (TDS) atskaitymai.
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023448"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="d20ce-103">Parametrų mokėtinos sąskaitose ir gautinose sąskaitose TDS nustatymas</span><span class="sxs-lookup"><span data-stu-id="d20ce-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d20ce-104">Šioje temoje aiškinama, kaip nustatyti mokėtinų sumų ir gautinų sumų parametrus, kad būtų palaikomi šaltinio (TDS) atskaitymai.</span><span class="sxs-lookup"><span data-stu-id="d20ce-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="d20ce-105">Eikite į **Mokestis \> Sąranka \> Parametrai \> Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="d20ce-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="d20ce-106">Skirtuke **Naujinimai** pasirinkite **Naujinti užsakymo eilutes**, kad atidarytumėte dialogo langą **Naujinti užsakymo eilutes**.</span><span class="sxs-lookup"><span data-stu-id="d20ce-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="d20ce-107">Sekcijos **TDS grupė** lauke **TDS grupės naujinimas** nurodykite metodą, kuris bus naudojamas TDS grupei atnaujinti eilutės lygiu.</span><span class="sxs-lookup"><span data-stu-id="d20ce-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="d20ce-108">Šis parametras naudojamas atnaujinant TDS grupę užsakymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="d20ce-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="d20ce-109">Galimos toliau nurodytos parinktys:</span><span class="sxs-lookup"><span data-stu-id="d20ce-109">The following options are available:</span></span>

    - <span data-ttu-id="d20ce-110">**Niekada** – TDS grupė neatnaujinama užsakymo eilutėse, kai ji atnaujinama užsakymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="d20ce-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="d20ce-111">**Visada** – TDS grupė automatiškai naujinama užsakymo eilutėse, kai ji atnaujinama užsakymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="d20ce-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="d20ce-112">**Raginimas** – vartotojai gauna pranešimą, raginantį atnaujinti užsakymo eilučių TDS grupę.</span><span class="sxs-lookup"><span data-stu-id="d20ce-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="d20ce-113">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d20ce-113">Select **OK**.</span></span>

    <span data-ttu-id="d20ce-114">[![Dialogo langas Atnaujinti užsakymo eilutes](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="d20ce-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="d20ce-115">Eikite į **Mokestis \> Sąranka \> Parametrai \> Gautinų mokėtinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="d20ce-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="d20ce-116">Skirtuko **Bendra** „FastTab“ **Skaidymas pagal pristatymo informaciją** nustatykite parinktį **Produkto gavimo kvitas** kaip **Taip,** kad užregistruotumėte ir padalintumėte produkto gavimo kvitą, kuriame yra skirtingi pristatymo adresai ir mokesčių sąskaitų numeriai (BLSK).</span><span class="sxs-lookup"><span data-stu-id="d20ce-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="d20ce-117">Jei ši pasirinktis nustatyta kaip **Ne**, negalite registruoti pirkimo važtaraščio, kuriame yra skirtingi pristatymo adresai ir BLSK.</span><span class="sxs-lookup"><span data-stu-id="d20ce-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="d20ce-118">Nustatykite parinktį **SF** kaip **Taip**, kad užregistruotumėte ir padalintumėte pirkimo SF, kurioje yra skirtingi pristatymo adresai ir BLSK.</span><span class="sxs-lookup"><span data-stu-id="d20ce-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="d20ce-119">[![Skaidyti pagal „FastTab“ pristatymo informacija](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="d20ce-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="d20ce-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d20ce-120">Close the page.</span></span>

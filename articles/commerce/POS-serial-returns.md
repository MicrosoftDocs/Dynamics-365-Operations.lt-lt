---
title: Grąžinti serijos numeriais kontroliuojamus produktus naudojant EKA
description: Šioje temoje aprašomos galimybės galiojant eilutėmis išrašomas prekes kaip grąžinimo proceso dalį „Microsoft Dynamics 365 Commerce“ (EKA) programoje.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129821"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="dcabd-103">Grąžinti serijos numeriais kontroliuojamus produktus naudojant EKA</span><span class="sxs-lookup"><span data-stu-id="dcabd-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="dcabd-104">Šioje temoje aprašomos galimybės galiojant eilutėmis išrašomas prekes kaip grąžinimo proceso dalį „Microsoft Dynamics 365 Commerce“ (EKA) programoje.</span><span class="sxs-lookup"><span data-stu-id="dcabd-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="dcabd-105">"Commerce 10.0.20" versijoje ir vėliau galima naudoti naują funkciją, kuri **EKA vadinama bendrojo grąžinamo apdorojimo** patirtimi.</span><span class="sxs-lookup"><span data-stu-id="dcabd-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="dcabd-106">Norėdami naudoti serijos numerio tikrinimą apdorojant grąžinimo užsakymą EKA, turite įjungti šią funkciją.</span><span class="sxs-lookup"><span data-stu-id="dcabd-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="dcabd-107">Informacijos apie kitas galimybes, kurias suteikia ši funkcija, kai ji įjungta, žr. [Kurti grąžinimus EKA)](POS-returns.md).</span><span class="sxs-lookup"><span data-stu-id="dcabd-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="dcabd-108">Kai priemonė įjungta, jos išjungti negalima.</span><span class="sxs-lookup"><span data-stu-id="dcabd-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="dcabd-109">Eilutėmis grąžintų grąžinimų pateisinimo parinktys</span><span class="sxs-lookup"><span data-stu-id="dcabd-109">Options for validating serialized returns</span></span>

<span data-ttu-id="dcabd-110">Kai **EKA priemonėje įjungta bendrojo grąžinimo apdorojimo** organizacijos gali atlikti prekių, kurių serijos numeris kontroliuojamas naudojant EKA, grąžinamų tikrinimą.</span><span class="sxs-lookup"><span data-stu-id="dcabd-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="dcabd-111">Ši galimybė gali įspėti vartotojus, jei grąžinamas serijos numeris skiriasi nuo pradinio parduoto serijos numerio.</span><span class="sxs-lookup"><span data-stu-id="dcabd-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="dcabd-112">„Commerce" 10.0.20 versijoje ir vėliau pranešimas, kurį gauna vartotojai, yra tik įspėjamasis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="dcabd-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="dcabd-113">Vartotojai gali toliau apdoroti grąžinimą pagal serijos numerį, kuris skiriasi nuo serijos numerio, kuris buvo parduotas iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="dcabd-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="dcabd-114">Norėdami konfigūruoti organizacijos serijos numerio tikrinimą įjungę **bendrojo grąžinimo apdorojimo funkciją EKA** eikite į **Mažmena ir komercija \> Štabo nustatymai \> Parameters \> „Commerce“ parametrai** „Commerce“ štabe.</span><span class="sxs-lookup"><span data-stu-id="dcabd-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="dcabd-115">Skirtuko **Atsargos** „FastTab“ **Parduotuvės atsargų operacijų** nustatykite **Įgalinti EKA grąžinimų serijos numerių tinkinimo** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="dcabd-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="dcabd-116">Apdoroti EKA eilutėmis išduotų prekių grąžinimus</span><span class="sxs-lookup"><span data-stu-id="dcabd-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="dcabd-117">Jei **parinktis Įgalinti serijos numerių tikrinimą EKA grąžinimo pasirinktyje nustatyta** kaip **Taip**, ai naudojant EKA grąžinama serijos numeriu kontroliuojama prekė, vartotojas gali įvesti grąžinimo eilutės serijos numerį į informacijos sritį, esančioje **Produktų grąžinimo** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="dcabd-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="dcabd-118">Jei įvestas serijos numeris neatitinka pradinio serijos numerio, parduoto pardavimo operacijai, vartotojas gauna įspėjimo pranešimą.</span><span class="sxs-lookup"><span data-stu-id="dcabd-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="dcabd-119">Tačiau programa neleidžia vartotojui tęsti grąžinimo.</span><span class="sxs-lookup"><span data-stu-id="dcabd-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="dcabd-120">Šiuo metu EKA palaiko tik grąžinimo eilučių serijos numerių tikrinimą, kai pradinis užsakytas kiekis ne didesnis kaip vienas.</span><span class="sxs-lookup"><span data-stu-id="dcabd-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="dcabd-121">Jei pradinė pardavimo užsakymo eilutė sukurta ne EKA kanale ir jei kiekis, užsakytas šios pardavimo eilutės eilutėms išdėstyti, yra didesnis nei vienas, per EKA negalima teisingai grąžinti prekės.</span><span class="sxs-lookup"><span data-stu-id="dcabd-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dcabd-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="dcabd-122">Additional resources</span></span>

[<span data-ttu-id="dcabd-123">Kurti grąžinimus EKA</span><span class="sxs-lookup"><span data-stu-id="dcabd-123">Create returns in POS</span></span>](POS-returns.md)

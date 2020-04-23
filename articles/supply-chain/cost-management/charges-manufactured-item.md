---
title: Pagamintos prekės išlaidų rodymas
description: Gamintojo prekės pastovios išlaidos rodo operacijos nustatymo laikus ir komponentus, turinčius pastovų kiekį arba pastovią nurašymų sumą.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: b955bfe4f26620724d297691e052edaca239937a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201990"
---
# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="9bf5c-103">Pagamintos prekės išlaidų rodymas</span><span class="sxs-lookup"><span data-stu-id="9bf5c-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bf5c-104">Gamintojo prekės pastovios išlaidos rodo operacijos nustatymo laikus ir komponentus, turinčius pastovų kiekį arba pastovią nurašymų sumą.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="9bf5c-105">Prekės išlaidų apskaičiuota suma gali būti rodoma kaip prekės vieneto išlaidos.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="9bf5c-106">Tačiau išlaidos kartais rodomos kaip atskiri laukai ir neįtraukiamos į prekės vieneto išlaidas.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="9bf5c-107">Kai išlaidos parodomos atskirais laukais, vienas laukas rodo bendrą mokesčių sumą, o kitas – įkainojimo partijos dydį, naudojamą amortizuoti sumą.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="9bf5c-108">Pavyzdžiui, prekės kainos puslapyje išlaidos rodomos kaip du atskiri laukai.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="9bf5c-109">Tačiau puslapyje Baigta rodoma prekės bendra vieneto savikaina su į vieneto savikainą įskaitytomis papildomomis išlaidomis.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="9bf5c-110">Pagamintos prekės išlaidos visada įtrauktos į prekės vieneto savikainą, kad būtų žinoma standartinė savikaina.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="9bf5c-111">Jos gali būti pasirinktinai įtraukiamos norint žinoti suplanuotas išlaidas.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="9bf5c-112">Įkainojimo versijos strategija įgalina įtraukti išlaidas į pagamintos prekės išlaidas.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="9bf5c-113">Kai suaktyvinsite prekės išlaidų įrašą, atnaujinkite informaciją apie prekės bazinės savikainos išlaidas, rodomas prekės kainos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="9bf5c-114">Išlaidos rodomos kaip du atskiri laukai ir neįtraukiamos į prekės vieneto išlaidas.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="9bf5c-115">Kiekvieno suaktyvinimo metu bus atnaujinama informacija apie prekės bazinę savikainą, net jei suaktyvinimas atspindi skirtingas teritorijas.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="9bf5c-116">Todėl reikia peržiūrėti informaciją apie bazinę savikainą kaip nuorodos informaciją.</span><span class="sxs-lookup"><span data-stu-id="9bf5c-116">Therefore, you should view the base cost information as reference information.</span></span>






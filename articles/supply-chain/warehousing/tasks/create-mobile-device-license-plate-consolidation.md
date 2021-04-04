---
title: Mobiliojo įrenginio meniu elemento, skirto numerių lentelėms konsoliduoti, kūrimas
description: Šioje procedūroje parodoma, kaip kurti mobiliojo įrenginio meniu elementą, skirtą numerių lentelių konsolidavimui atlikti.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54457261d4f80648050845f309bcbbcc16caa629
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239019"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="fa16a-103">Mobiliojo įrenginio meniu elemento, skirto numerių lentelėms konsoliduoti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="fa16a-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa16a-104">Šioje procedūroje parodoma, kaip kurti mobiliojo įrenginio meniu elementą, skirtą numerių lentelių konsolidavimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="fa16a-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="fa16a-105">Tai sandėlio darbuotojams suteikia galimybę konsoliduoti prekes vienoje numerio lentelėje su tos pačios vietos prekėmis kitoje numerio lentelėje.</span><span class="sxs-lookup"><span data-stu-id="fa16a-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="fa16a-106">Pavyzdžiui, jie gali naudoti šią funkciją, jei abiejų darbo užsakymų paskesni paruošimo veiksmai buvo vienodi, kad darbą su sulietomis prekėmis reikėtų atlikti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="fa16a-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="fa16a-107">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="fa16a-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="fa16a-108">Užduotį paprastai turėtų atlikti sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="fa16a-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="fa16a-109">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="fa16a-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="fa16a-110">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="fa16a-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="fa16a-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fa16a-111">Click New.</span></span>
3. <span data-ttu-id="fa16a-112">Lauke Meniu elemento pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fa16a-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="fa16a-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fa16a-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="fa16a-114">Lauke Režimas pasirinkite Netiesioginis.</span><span class="sxs-lookup"><span data-stu-id="fa16a-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="fa16a-115">Lauke Veiklos kodas pasirinkite Konsoliduoti numerių lenteles.</span><span class="sxs-lookup"><span data-stu-id="fa16a-115">In the Activity code field, select 'Consolidate license plates'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
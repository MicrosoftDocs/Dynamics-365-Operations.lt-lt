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
ms.openlocfilehash: b3f5f572461de007f137ffa7ea05c535371f95b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977243"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="34fb4-103">Mobiliojo įrenginio meniu elemento, skirto numerių lentelėms konsoliduoti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="34fb4-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34fb4-104">Šioje procedūroje parodoma, kaip kurti mobiliojo įrenginio meniu elementą, skirtą numerių lentelių konsolidavimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="34fb4-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="34fb4-105">Tai sandėlio darbuotojams suteikia galimybę konsoliduoti prekes vienoje numerio lentelėje su tos pačios vietos prekėmis kitoje numerio lentelėje.</span><span class="sxs-lookup"><span data-stu-id="34fb4-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="34fb4-106">Pavyzdžiui, jie gali naudoti šią funkciją, jei abiejų darbo užsakymų paskesni paruošimo veiksmai buvo vienodi, kad darbą su sulietomis prekėmis reikėtų atlikti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="34fb4-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="34fb4-107">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="34fb4-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="34fb4-108">Užduotį paprastai turėtų atlikti sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="34fb4-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="34fb4-109">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="34fb4-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="34fb4-110">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="34fb4-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="34fb4-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="34fb4-111">Click New.</span></span>
3. <span data-ttu-id="34fb4-112">Lauke Meniu elemento pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="34fb4-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="34fb4-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="34fb4-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="34fb4-114">Lauke Režimas pasirinkite Netiesioginis.</span><span class="sxs-lookup"><span data-stu-id="34fb4-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="34fb4-115">Lauke Veiklos kodas pasirinkite Konsoliduoti numerių lenteles.</span><span class="sxs-lookup"><span data-stu-id="34fb4-115">In the Activity code field, select 'Consolidate license plates'.</span></span>


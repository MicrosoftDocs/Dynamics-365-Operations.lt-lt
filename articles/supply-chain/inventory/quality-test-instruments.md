---
title: Kokybės valdymo bandymo instrumentai
description: Šioje temoje aprašoma, kaip sukurti tikrinimo priemones, kurias galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3806ca26b8909b03768dad54ddad0084e1cea4a6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021737"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="3c5fa-103">Kokybės valdymo bandymo instrumentai</span><span class="sxs-lookup"><span data-stu-id="3c5fa-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c5fa-104">Šioje temoje aprašoma, kaip sukurti tikrinimo priemones, kurias galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="3c5fa-105">Naudokitės bandymo instrumentų puslapiu, norėdami nurodyti ir peržiūrėti informaciją apie **įrenginius**, naudojamus kokybės užsakymų bandymams vykdyti.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="3c5fa-106">Bandymo instrumentai pasirinktini.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-106">Test instruments are optional.</span></span> <span data-ttu-id="3c5fa-107">Tačiau jie gali padėti kokybės darbuotojams žinoti, kurį įrenginį ar įrankį jie turėtų naudoti atlikdami konkretų testą.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="3c5fa-108">Bandymo prietaiso pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3c5fa-108">Test instrument example</span></span>

<span data-ttu-id="3c5fa-109">Atliekate įvairius elektros komponentų bandymus.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="3c5fa-110">Kai kurie bandymai yra skirti komponentų išeigai, vienas bandymas skirtas jų temperatūrai, o vienas bandymas skirtas jų svoriui.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="3c5fa-111">Kiekvienam bandymui atlikti naudojami skirtingi įrankiai, įrenginiai arba įranga.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="3c5fa-112">Pavyzdžiui, kasos skaitiklis yra naudojamas matuoti pagal kilometrelį, temperatūrai matuoti naudojamas skaitiklis, o svarstyklės naudojamos svoriui matuoti.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="3c5fa-113">Galite konfigūruoti kiekvieną iš šių įrenginių kaip tikrinimo prietaisą ir nurodyti matavimo vienetą, į kurį turi būti įrašyti tikrinimo rezultatai.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="3c5fa-114">Pvz., kasos skaitiklio rezultatai įrašomi į kilogramus, o už svarus arba kilogramus neįrašomi į metrą, o rezultatai iš svarų ar kilogramų įrašomi fiksuotais laipsniais Fahrenheit arba degrees.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="3c5fa-115">Naujo testavimo kūrimas</span><span class="sxs-lookup"><span data-stu-id="3c5fa-115">Create a test instrument</span></span>

1. <span data-ttu-id="3c5fa-116">Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Instrumentų testas**.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="3c5fa-117">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="3c5fa-118">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="3c5fa-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="3c5fa-119">**Bandymo instrumentas** – įveskite unikalų tikrinimo prietaiso ID arba pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="3c5fa-120">**Aprašas** – įveskite išsamų bandymo instrumento aprašą.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="3c5fa-121">**Vienetas** – pasirinkite vienetą, kuris bus matavimo vienetas.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="3c5fa-122">Tikslumo **laukas** nustatomas automatiškai, remiantis jūsų pasirinktu vienetu.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="3c5fa-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3c5fa-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c5fa-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3c5fa-124">Additional resources</span></span>

- [<span data-ttu-id="3c5fa-125">Kokybės valdymo bandymas</span><span class="sxs-lookup"><span data-stu-id="3c5fa-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="3c5fa-126">Kokybės valdymo bandymo grupės</span><span class="sxs-lookup"><span data-stu-id="3c5fa-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

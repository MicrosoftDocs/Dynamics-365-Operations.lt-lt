---
title: Aptarnavimo KS modifikavimas
description: Modifikuokite aptarnavimo KS.
author: ShylaThompson
manager: AnnBe
ms.date: 05/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a66f7ea7b30e033a39c292dff4064deef6bff4c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "321575"
---
# <a name="modify-a-service-bom"></a><span data-ttu-id="a487e-103">Aptarnavimo KS modifikavimas</span><span class="sxs-lookup"><span data-stu-id="a487e-103">Modify a Service BOM</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a487e-104">Aptarnavimo KS galite įrašyti elementų retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="a487e-104">You can record the history of an element in a service BOM.</span></span> <span data-ttu-id="a487e-105">Kiekvieną kartą, kai atnaujinate KS eilutę, srityje **Retrospektyva** sukuriama retrospektyvos eilutė.</span><span class="sxs-lookup"><span data-stu-id="a487e-105">Every time that you update a BOM line, a history line is created in the **History** pane.</span></span> <span data-ttu-id="a487e-106">Retrospektyvos eilutėje rodoma dabartinė KS eilutės būsena.</span><span class="sxs-lookup"><span data-stu-id="a487e-106">The history line shows the current state of the BOM line.</span></span>

## <a name="update-a-service-bom-element"></a><span data-ttu-id="a487e-107">Aptarnavimo KS elemento atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="a487e-107">Update a service BOM element</span></span>

1.  <span data-ttu-id="a487e-108">Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="a487e-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="a487e-109">Spustelėję **Redaguoti** atidarysite informacijos formą **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="a487e-109">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="a487e-110">Dalyje **Veiksmų sritis** spustelėję **Aptarnavimo objektai** atidarysite formą **Aptarnavimo objektai**.</span><span class="sxs-lookup"><span data-stu-id="a487e-110">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="a487e-111">Pasirinkite objektą, kurio KS eilutę atnaujinsite, tada spustelėkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="a487e-111">Select the object to update a BOM line for, and then click **Designer**.</span></span>

5.  <span data-ttu-id="a487e-112">Formoje **Dizaino įrankis** pasirinkite norimą atnaujinti KS eilutę, tada spustelėkite **Redaguoti KS eilutę**.</span><span class="sxs-lookup"><span data-stu-id="a487e-112">In the **Designer** form, select the BOM line to update, and then click **Edit BOM line**.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="a487e-113">Skirtuke <STRONG>Sąranka</STRONG> pažymėkite žymės langelį <STRONG>Redaguoti įtraukiant</STRONG>, jei norite, kad atsidarytų forma <STRONG>Redaguoti KS eilutę</STRONG>, vilkite eilutę į aptarnavimo KS.</span><span class="sxs-lookup"><span data-stu-id="a487e-113">On the <STRONG>Setup</STRONG> tab, select the <STRONG>Edit when adding</STRONG> check box if you want the <STRONG>Edit BOM line</STRONG> form to open when you drag a line into the service BOM.</span></span></P>

6.  <span data-ttu-id="a487e-114">Lauke **Kiekis** įveskite kiekį.</span><span class="sxs-lookup"><span data-stu-id="a487e-114">In the **Quantity** field, enter the quantity.</span></span>

7.  <span data-ttu-id="a487e-115">Jei norite sukurti prekės, kuriai bus išrašoma SF, pakeitimo aptarnavimo užsakymo eilutę, pažymėkite žymės langelį **Kurti aptarnavimo užsakymo eilutę**.</span><span class="sxs-lookup"><span data-stu-id="a487e-115">If you want to create a service order line for the replacement item, which can then be invoiced, select the **Create service order line** check box.</span></span>

8.  <span data-ttu-id="a487e-116">Spustelėkite **Gerai** formai uždaryti.</span><span class="sxs-lookup"><span data-stu-id="a487e-116">Click **OK** to close the form.</span></span>

## <a name="delete-a-service-bom-line"></a><span data-ttu-id="a487e-117">Aptarnavimo KS eilutės naikinimas</span><span class="sxs-lookup"><span data-stu-id="a487e-117">Delete a service BOM line</span></span>

1.  <span data-ttu-id="a487e-118">Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="a487e-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="a487e-119">Spustelėję **Redaguoti** atidarysite informacijos formą **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="a487e-119">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="a487e-120">Dalyje **Veiksmų sritis** spustelėję **Aptarnavimo objektai** atidarysite formą **Aptarnavimo objektai**.</span><span class="sxs-lookup"><span data-stu-id="a487e-120">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="a487e-121">Pasirinkite objektą, iš kurio norite ištrinti aptarnavimo KS eilutę, o tada spustelėkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="a487e-121">Select the object to delete a service BOM line from, and then click **Designer**.</span></span>

5.  <span data-ttu-id="a487e-122">Formoje **Dizaino įrankis** pasirinkite norimą naikinti KS eilutę, tada spustelėkite **Naikinti KS eilutę**.</span><span class="sxs-lookup"><span data-stu-id="a487e-122">In the **Designer** form, select the BOM line to delete, and then click **Delete BOM line**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a487e-123">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="a487e-123">See also</span></span>

[<span data-ttu-id="a487e-124">Šabloninės KS</span><span class="sxs-lookup"><span data-stu-id="a487e-124">Template BOMs</span></span>](template-boms.md)

  



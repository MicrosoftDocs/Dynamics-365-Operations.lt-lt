---
title: Už priežiūrą atsakingi darbuotojai
description: Šiame straipsnyje aprašoma, kaip priskirti už priežiūrą atsakingus darbuotojus modulyje „Turto valdymas“.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 432a235668bbd969f497003a98b7f66390e5308f
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790520"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="24c7c-103">Už priežiūrą atsakingi darbuotojai</span><span class="sxs-lookup"><span data-stu-id="24c7c-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="24c7c-104">Už priežiūrą atsakingi darbuotojai gali būti susiję su turto tipais, turtu, funkcinėmis vietovėmis, priežiūros užduoties tipo kategorijomis, priežiūros užduočių tipais, priežiūros užduoties tipo variantais ir prekyba.</span><span class="sxs-lookup"><span data-stu-id="24c7c-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="24c7c-105">Jie gali būti naudojami darbo užsakymuose ir priežiūros užklausose, siekiant nurodyti nuostatą, kurie priežiūros darbuotojai turėtų būti atsakingi už darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="24c7c-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="24c7c-106">(Tačiau šie techninės priežiūros darbuotojai nebūtinai yra tie patys darbuotojai, kuriems numatyta atlikti darbų užsakymą.) Šios funkcijos naudojimas yra neprivalomas.</span><span class="sxs-lookup"><span data-stu-id="24c7c-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="24c7c-107">Pavyzdžiui, ji gali būti naudojama norint pasirinkti atsakingus darbuotojus arba darbuotojų grupes konkretiems darbo tipams arba darbo sritims.</span><span class="sxs-lookup"><span data-stu-id="24c7c-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="24c7c-108">Darbo užsakymo ciklo arba priežiūros užklausos ciklo metu, už priežiūrą atsakingi darbuotojai gali būti keičiami arba atnaujinami.</span><span class="sxs-lookup"><span data-stu-id="24c7c-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="24c7c-109">Šis pakeitimas arba atnaujinimas gali būti susijęs, pavyzdžiui, su priežiūros užklausos ciklo būsenos arba darbo užsakymo ciklo būsenos pasikeitimu.</span><span class="sxs-lookup"><span data-stu-id="24c7c-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="24c7c-110">Puslapio **Už priežiūrą atsakingi darbuotojai** konfigūracija *nėra* naudojama darbo užsakymo planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="24c7c-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="24c7c-111">Modulyje „Turto valdymas“ taip pat galite pasirinkti *pageidaujamus* priežiūros darbuotojus, kurie gali būti priskirti darbo užsakymams darbo užsakymo planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="24c7c-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="24c7c-112">Kad galėtumėte nustatyti už priežiūrą atsakingus darbuotojus, turite nustatyti darbuotojų ir priežiūros darbuotojų grupes, kurias būtų galima pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="24c7c-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="24c7c-113">Informacijos apie tai, kaip nustatyti darbuotojus ir priežiūros darbuotojų grupes, rasite temoje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="24c7c-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="24c7c-114">Už priežiūrą atsakingų darbuotojų nustatymas</span><span class="sxs-lookup"><span data-stu-id="24c7c-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="24c7c-115">Pasirinkite **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span><span class="sxs-lookup"><span data-stu-id="24c7c-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="24c7c-116">Pasirinkite **Naujas** pranešimui sukurti.</span><span class="sxs-lookup"><span data-stu-id="24c7c-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="24c7c-117">Visų pirma sukurkite numatytąjį už priežiūrą atsakingą darbuotoją arba už priežiūrą atsakingų darbuotojų grupės konfigūraciją, kurioje nustatysite tik lauką **Už priežiūrą atsakingų darbuotojų grupė** ir (arba) lauką **Atsakingas darbuotojas**.</span><span class="sxs-lookup"><span data-stu-id="24c7c-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="24c7c-118">Likusius laukus palikite tuščius.</span><span class="sxs-lookup"><span data-stu-id="24c7c-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="24c7c-119">Ši numatytoji konfigūracija bus naudojama darbo užsakymų planavimo metu, jei nebus rasta jokia kita, konkrečiau darbo užsakymo turinį atitinkanti kombinacija.</span><span class="sxs-lookup"><span data-stu-id="24c7c-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="24c7c-120">Kuriant priežiūros užklausą, puslapyje **Visos priežiūros užklausos** aktyvavus galimybę pasirinkti už priežiūrą atsakingą darbuotoją arba už priežiūrą atsakingų darbuotojų grupę, modulyje „Turto valdymas“ peržiūrimi visi už priežiūrą atsakingų darbuotojų įrašai, siekiant surasti galimą atitiktį.</span><span class="sxs-lookup"><span data-stu-id="24c7c-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="24c7c-121">Jis visada pirmiausiai tikrina konkrečiausius derinius.</span><span class="sxs-lookup"><span data-stu-id="24c7c-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="24c7c-122">Kitaip tariant, modulyje „Turto valdymas“ visų pirma ieškoma lauko **Prekyba** atitikties.</span><span class="sxs-lookup"><span data-stu-id="24c7c-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="24c7c-123">Jei atitiktis nerasta, ieškoma lauko **Priežiūros užduoties tipo variantas** atitikties.</span><span class="sxs-lookup"><span data-stu-id="24c7c-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="24c7c-124">Jei atitiktis nerasta, ieškoma lauko **Priežiūros užduoties tipas** atitikties ir t.t.</span><span class="sxs-lookup"><span data-stu-id="24c7c-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="24c7c-125">Kaip matote pagal puslapio išdėstymą, toks paieškos metodas reiškia, kad, siekiant rasti pačią konkrečiausią kombinaciją, modulyje „Turto valdymas“, kiekviename įraše atitikčių ieškoma iš dešinės į kairę (iš pradžių **Prekyba**, tada **Priežiūros užduočių tipo variantas**, tada **Priežiūros užduoties tipas**, tada **Priežiūros užduoties tipo kategorija**, tada **Funkcinė vietovė**, tada **Turtas** ir galiausiai **Turto tipas**).</span><span class="sxs-lookup"><span data-stu-id="24c7c-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="24c7c-126">Jei atitikties rasti nepavyksta, naudojamas numatytasis įrašas, kuriame šie septyni laukai yra tušti.</span><span class="sxs-lookup"><span data-stu-id="24c7c-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="24c7c-127">Paveikslėlyje pavaizduotas puslapio **Už priežiūrą atsakingi darbuotojai** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="24c7c-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![1 paveikslėlis](media/08-setup-for-requests.png)

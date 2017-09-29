---
title: "Pagal sistemas arba vartotojus nustatyti lentelės apribojimai"
description: "Šiame straipsnyje aprašomi du lentelės apribojimų, skirtų komponentams produktų konfigūravimo modelyje, tipai – apibrėžti vartotojo ir apibrėžti sistemos. Lentelės apribojimai – tai leistinų atributų derinių matricos, kurių kiekvienoje eilutėje apibrėžiamas vienas galimų atributų reikšmių rinkinys."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: b59452496f0ad47f1fe2ff034895a082a205dda9
ms.contentlocale: lt-lt
ms.lasthandoff: 09/14/2017

---

# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="f103e-104">Pagal sistemas arba vartotojus nustatyti lentelės apribojimai</span><span class="sxs-lookup"><span data-stu-id="f103e-104">System-defined and user-defined table constraints</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f103e-105">Šiame straipsnyje aprašomi du lentelės apribojimų, skirtų komponentams produktų konfigūravimo modelyje, tipai – apibrėžti vartotojo ir apibrėžti sistemos.</span><span class="sxs-lookup"><span data-stu-id="f103e-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="f103e-106">Lentelės apribojimai – tai leistinų atributų derinių matricos, kurių kiekvienoje eilutėje apibrėžiamas vienas galimų atributų reikšmių rinkinys.</span><span class="sxs-lookup"><span data-stu-id="f103e-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="f103e-107">Lentelės apribojimai nurodo produkto konfigūracijos modelyje leidžiamų komponentų atributų derinių matricas.</span><span class="sxs-lookup"><span data-stu-id="f103e-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="f103e-108">Kiekviena eilutė lentelėje nurodo vieną galimų atributų reikšmių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f103e-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="f103e-109">Produkto konfigūracijos modelyje galite nurodyti dviejų toliau nurodytų tipų apribojimus.</span><span class="sxs-lookup"><span data-stu-id="f103e-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="f103e-110">**Išraiškos apribojimas** – kurkite išraišką, kuri apibrėžia atributų ryšius, siekdami užtikrinti, kad prekės konfigūravimo metu būtų galima pasirinkti tik suderinamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="f103e-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="f103e-111">**Lentelės apribojimas** – kurkite lentelę, kuri nurodo visus leidžiamus konkretaus atributų rinkinio derinius.</span><span class="sxs-lookup"><span data-stu-id="f103e-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="f103e-112">Galima naudoti dviejų tipų lentelės apribojimus: vartotojo nustatytus lentelės apribojimus ir sistemos nustatytus lentelės apribojimus.</span><span class="sxs-lookup"><span data-stu-id="f103e-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="f103e-113">Šiame straipsnyje aprašomi vartotojo ir sistemos nustatyti lentelės apribojimai, skirti komponentams produktų konfigūravimo modelyje.</span><span class="sxs-lookup"><span data-stu-id="f103e-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="f103e-114">Vartotojo nustatyti lentelės apribojimai</span><span class="sxs-lookup"><span data-stu-id="f103e-114">User-defined table constraints</span></span>
<span data-ttu-id="f103e-115">Vartotojo nustatytas lentelės apribojimas yra matricos tipas, naudojamas atributų reikšmių, kurias apibrėžia atributo tipas, deriniams apibūdinti.</span><span class="sxs-lookup"><span data-stu-id="f103e-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="f103e-116">Pavyzdžiui, jei gaminate garsiakalbius, į vartotojo nustatytą lentelės apribojimą galite įtraukti spintelės apdailos ir priekinių grotelių stulpelius.</span><span class="sxs-lookup"><span data-stu-id="f103e-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="f103e-117">Spintelės apdailos atributo tipas gali turėti keturias reikšmes, o priekinių grotelių atributo tipas gali turėti tris reikšmes.</span><span class="sxs-lookup"><span data-stu-id="f103e-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="f103e-118">Todėl, jei apribojimai nėra taikomi, galimų derinių skaičius yra 4 × 3 = 12.</span><span class="sxs-lookup"><span data-stu-id="f103e-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="f103e-119">Tačiau pagal šį pavyzdį galima naudoti tik šešis derinius, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="f103e-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="f103e-120">Ši informacija rodoma puslapio **Redaguoti lentelės apribojimą** skirtuke **Leistini deriniai**.</span><span class="sxs-lookup"><span data-stu-id="f103e-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="f103e-121">Spintelės apdaila</span><span class="sxs-lookup"><span data-stu-id="f103e-121">Cabinet finish</span></span> | <span data-ttu-id="f103e-122">Priekinės grotelės</span><span class="sxs-lookup"><span data-stu-id="f103e-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="f103e-123">Juoda</span><span class="sxs-lookup"><span data-stu-id="f103e-123">Black</span></span>          | <span data-ttu-id="f103e-124">Juoda</span><span class="sxs-lookup"><span data-stu-id="f103e-124">Black</span></span>       |
| <span data-ttu-id="f103e-125">Juoda</span><span class="sxs-lookup"><span data-stu-id="f103e-125">Black</span></span>          | <span data-ttu-id="f103e-126">Metalo</span><span class="sxs-lookup"><span data-stu-id="f103e-126">Metal</span></span>       |
| <span data-ttu-id="f103e-127">Ąžuolo</span><span class="sxs-lookup"><span data-stu-id="f103e-127">Oak</span></span>            | <span data-ttu-id="f103e-128">Juoda</span><span class="sxs-lookup"><span data-stu-id="f103e-128">Black</span></span>       |
| <span data-ttu-id="f103e-129">Raudonmedžio</span><span class="sxs-lookup"><span data-stu-id="f103e-129">Rosewood</span></span>       | <span data-ttu-id="f103e-130">Balta</span><span class="sxs-lookup"><span data-stu-id="f103e-130">White</span></span>       |
| <span data-ttu-id="f103e-131">Balta</span><span class="sxs-lookup"><span data-stu-id="f103e-131">White</span></span>          | <span data-ttu-id="f103e-132">Juoda</span><span class="sxs-lookup"><span data-stu-id="f103e-132">Black</span></span>       |
| <span data-ttu-id="f103e-133">Balta</span><span class="sxs-lookup"><span data-stu-id="f103e-133">White</span></span>          | <span data-ttu-id="f103e-134">Balta</span><span class="sxs-lookup"><span data-stu-id="f103e-134">White</span></span>       |

<span data-ttu-id="f103e-135">Vartotojo nustatytus lentelės apribojimus apibrėžia statinė lentelės įvestis, kuri veikia taip pat, kaip išraiškos apribojimas.</span><span class="sxs-lookup"><span data-stu-id="f103e-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="f103e-136">Privalumas naudojant vartotojo nustatytą lentelės apribojimą yra tai, kad dažnai lengviau kurti, suprasti ir prižiūrėti lenteles, o ne ilgis išraiškos apribojimus.</span><span class="sxs-lookup"><span data-stu-id="f103e-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="f103e-137">Sistemos nustatyti lentelės apribojimai</span><span class="sxs-lookup"><span data-stu-id="f103e-137">System-defined table constraints</span></span>
<span data-ttu-id="f103e-138">Sistemos nustatytas lentelės apribojimas sukuria dinaminį susiejimą tarp atributo tipo ir lauko lentelėje.</span><span class="sxs-lookup"><span data-stu-id="f103e-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="f103e-139">Kai sistemos nustatytas lentelės apribojimas įtraukiamas į produkto konfigūracijos modelį, susiejimas garantuoja, bus rodomi lentelės duomenys, o ne atributo tipo reikšmės.</span><span class="sxs-lookup"><span data-stu-id="f103e-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="f103e-140">Rezultatas yra dinaminis apribojimas, nes lentelės turinį galima modifikuoti (pvz., naudojant kitus modulius).</span><span class="sxs-lookup"><span data-stu-id="f103e-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="f103e-141">Kurdami sistemos nustatytą lentelės apribojimą, turite pasirinkti lentelę, pasirinktinai nustatyti naudotiną užklausą, o tada atributų tipus susieti su pasirinktos lentelės laukais.</span><span class="sxs-lookup"><span data-stu-id="f103e-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="f103e-142">Laukų tipai turi atitikti atributų tipus .</span><span class="sxs-lookup"><span data-stu-id="f103e-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="f103e-143">Prieš lentelių apribojimus įsigaliojant produkto konfigūracijos modelio komponentui, lentelių apribojimą reikia įtraukti į vieną iš modelio komponentų.</span><span class="sxs-lookup"><span data-stu-id="f103e-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="f103e-144">Ši procedūra skirta sukurti naują apribojimą, pasirinkite lentelės apribojimo tipą, tada pasirinkite lentelės apribojimo apibėžimą, kurį naudosite.</span><span class="sxs-lookup"><span data-stu-id="f103e-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="f103e-145">Galiausiai visus lentelės apribojimo laukus turite susieti su atributais produkto konfigūracijos modelyje.</span><span class="sxs-lookup"><span data-stu-id="f103e-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="see-also"></a><span data-ttu-id="f103e-146">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="f103e-146">See also</span></span>
--------

[<span data-ttu-id="f103e-147">Pagrindinės produkto konfigūracijos modelių koncepcijos</span><span class="sxs-lookup"><span data-stu-id="f103e-147">Key concepts in product configuration models</span></span>](product-configuration-models.md)




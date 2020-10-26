---
title: Pakartotinai naudoti produkto konfigūracijas
description: Galite nurodyti, kad produkto konfigūracija būtų pakartotinai naudojama automatiškai. Tada, kai vartotojas baigia konfigūravimo seansą, sistema patikrina, ar konfigūracija, kuris atitinka vartotojo pasirinkimus, jau yra. Jei sutampanti konfigūracija rasta, pakartotinai naudojami konfigūracijos ID, atitinkama komplektavimo specifikacija (KS) ir maršrutas.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd6d730528522f4074b6e2a3ce6059cc12ff5a0f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984758"
---
# <a name="reuse-product-configurations"></a><span data-ttu-id="ae514-105">Pakartotinai naudoti produkto konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="ae514-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae514-106">Galite nurodyti, kad produkto konfigūracija būtų pakartotinai naudojama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="ae514-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="ae514-107">Tada, kai vartotojas baigia konfigūravimo seansą, sistema patikrina, ar konfigūracija, kuris atitinka vartotojo pasirinkimus, jau yra.</span><span class="sxs-lookup"><span data-stu-id="ae514-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="ae514-108">Jei sutampanti konfigūracija rasta, pakartotinai naudojami konfigūracijos ID, atitinkama komplektavimo specifikacija (KS) ir maršrutas.</span><span class="sxs-lookup"><span data-stu-id="ae514-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="ae514-109">Pakartotinio konfigūracijų naudojimo reikalavimai</span><span class="sxs-lookup"><span data-stu-id="ae514-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="ae514-110">Norėdami įjungti pakartotinio konfigūracijų naudojimo funkciją, turite nurodyti toliau pateiktą komponentų ir atributų informaciją puslapyje **Produkto konfigūracijos modelio informacija**.</span><span class="sxs-lookup"><span data-stu-id="ae514-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="ae514-111">**Komponentai ir subkomponentai** – „FastTab“ **Bendra** lauke **Pakartotinai naudoti konfigūracijas** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ae514-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="ae514-112">**Atributai** – „FastTab“ **Atributai** pasirinkite parinktį **Įtraukti į pakartotinį naudojimą**.</span><span class="sxs-lookup"><span data-stu-id="ae514-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="ae514-113">Ši pasirinktis rodoma tik kai įjungta susijusio komponento pakartotinio naudojimo funkcija.</span><span class="sxs-lookup"><span data-stu-id="ae514-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="ae514-114">Jei nepasirinksite jokių komponentų, kuriuos norėtumėte naudoti pakartotinai, konfigūracija visada naudojama pakartotinai, nepriklausomai nuo to, ką vartotojas pasirenka konfigūravimo seanso metu.</span><span class="sxs-lookup"><span data-stu-id="ae514-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="ae514-115">Esamos konfigūracijos atributo reikšmės turi atitikti vartotojo pasirinkimus.</span><span class="sxs-lookup"><span data-stu-id="ae514-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="ae514-116">Pavyzdžiui, jei konfigūracijos seanso metu vartotojas kaip spalvą pasirenka parinktį **Mėlyna**, sistema patikrina, ar dabartinėje komponento konfigūracijoje yra mėlyna spalva.</span><span class="sxs-lookup"><span data-stu-id="ae514-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="ae514-117">Pakartotinio konfigūracijos naudojimo nustatymas iš naujo</span><span class="sxs-lookup"><span data-stu-id="ae514-117">Resetting configuration reuse</span></span>
<span data-ttu-id="ae514-118">Kai iš naujo nustatote pakartotinio konfigūracijos naudojimo funkciją, anksčiau sukurtos konfigūracijos nebenaudojamos.</span><span class="sxs-lookup"><span data-stu-id="ae514-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="ae514-119">Galite iš naujo nustatyti pakartotinio konfigūracijos naudojimo funkciją, jei buvo pakeistas maršrutas arba KS, bet atributai pakeisti nebuvo.</span><span class="sxs-lookup"><span data-stu-id="ae514-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="ae514-120">Pakartotinio konfigūracijos naudojimo funkcija nustatoma komponento „FastTab“ **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="ae514-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>




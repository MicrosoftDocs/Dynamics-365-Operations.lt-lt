---
title: Tiekėjo portalo vartotojų sauga
description: Šiame straipsnyje paaiškinama, kaip nustatyti išorinių tiekėjų, kurie naudoja Tiekėjo portalą, saugą. Ši informacija taikoma tik 2016 m. vasario mėn. ir 2016 m. &amp; gegužės mėn. „Dynamics AX“ versijoms.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1be210728a6d5fa9a26daf9f13865ff08de03d2d
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018192"
---
# <a name="vendor-portal-user-security"></a><span data-ttu-id="1ceab-104">Tiekėjo portalo vartotojų sauga</span><span class="sxs-lookup"><span data-stu-id="1ceab-104">Vendor portal user security</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ceab-105">Šiame straipsnyje paaiškinama, kaip nustatyti išorinių tiekėjų, kurie naudoja Tiekėjo portalą, saugą.</span><span class="sxs-lookup"><span data-stu-id="1ceab-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="1ceab-106">Ši informacija taikoma tik 2016 m. vasario mėn. ir 2016 m. &amp; gegužės mėn. „Dynamics AX“ versijoms.</span><span class="sxs-lookup"><span data-stu-id="1ceab-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="1ceab-107">Tiekėjo portalo funkcija buvo pakeistą išplėstine tiekėjo bendradarbiavimo funkcija 1611 „Dynamics 365 for Operations“ versija.</span><span class="sxs-lookup"><span data-stu-id="1ceab-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="1ceab-108">Daugiau informacijos apie tiekėjo bendradarbiavimo saugos nustatymą [Tiekėjo bendradarbiavimo saugos nustatymas ir tvarkymas](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="1ceab-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="1ceab-109">Tiekėjo portale išoriniams tiekėjams pateikiamas ribotas informacijos apie pirkimo užsakymus (PU) kiekis.</span><span class="sxs-lookup"><span data-stu-id="1ceab-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="1ceab-110">Svarbu tinkamai nustatyti Tiekėjo portalo vartotojų teises programoje „Microsoft Dynamics AX“, kad tiekėjai neturėtų nenumatytų prieigos prie papildomos informacijos teisių jūsų „Dynamics AX“ sistemoje.</span><span class="sxs-lookup"><span data-stu-id="1ceab-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="1ceab-111">**Svarbu:** skirtingai nuo kitų vartotojų, išoriniams tiekėjams neturėtų būti priskiriamas vaidmuo **Sistemos vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="1ceab-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="1ceab-112">Vaidmuo **Sistemos vartotojas** suteikia prieigą prie tam tikrų teisių, kurios nėra skirtos išoriniams vartotojams.</span><span class="sxs-lookup"><span data-stu-id="1ceab-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="1ceab-113">Tiekėjo portalo vartotojo nustatymas</span><span class="sxs-lookup"><span data-stu-id="1ceab-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="1ceab-114">Prieš kurdami asmens, kuris naudos tiekėjo portalą, vartotojo paskyrą, turite leisti tiekėjui leisti bendradarbiauti naudojant tiekėjo portalą.</span><span class="sxs-lookup"><span data-stu-id="1ceab-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="1ceab-115">Naudokite puslapio **Tiekėjai** skirtuko **Bendra** lauką **Pirkimo užsakymo bendradarbiavimas**.</span><span class="sxs-lookup"><span data-stu-id="1ceab-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="1ceab-116">Toliau pateikiama tiekėjo portalą naudojančių išorinių tiekėjų sąranka.</span><span class="sxs-lookup"><span data-stu-id="1ceab-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="1ceab-117">Turi būti užregistruota tiekėjo „Microsoft Azure Active Directory“ (AAD) vartotojo paskyra „Dynamics AX“ puslapyje **Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="1ceab-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="1ceab-118">Tiekėjo saugos vaidmuo turi būti **Tiekėjas (išorinis)**, o ne **Sistemos vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="1ceab-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="1ceab-119">**Pastaba**: vaidmuo **Sistemos vartotojas** yra suteikiamas automatiškai, kai „Dynamics AX“ sukuriate naują vartotojo paskyrą.</span><span class="sxs-lookup"><span data-stu-id="1ceab-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="1ceab-120">Todėl turite pašalinti šį vaidmenį ir patvirtinti įspėjimo pranešimą, kurį gausite.</span><span class="sxs-lookup"><span data-stu-id="1ceab-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="1ceab-121">Su tiekėju susijęs vartotojas neturėtų gauti teisės įtraukti papildomų laukų iš PU lentelių į savo PU rodinį.</span><span class="sxs-lookup"><span data-stu-id="1ceab-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="1ceab-122">Skirtuke **Personalizavimas**, kuris yra skirtuke **Vartotojai**, nustatykite parinkties **Leidžiamas tiesioginis personalizavimas** reikšmę kaip **Ne**.</span><span class="sxs-lookup"><span data-stu-id="1ceab-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="1ceab-123">Vartotojo paskyra turi būti susieta su užregistruotu kontaktiniu asmenimi.</span><span class="sxs-lookup"><span data-stu-id="1ceab-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="1ceab-124">Puslapyje **Vartotojai** pasirinkite kontaktinį asmenį lauke **Vardas**.</span><span class="sxs-lookup"><span data-stu-id="1ceab-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="1ceab-125">Atitinkamo tiekėjo pasirinkto asmens vaidmuo turi būti **Kontaktas**.</span><span class="sxs-lookup"><span data-stu-id="1ceab-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="1ceab-126">Jei asmeniui reikia suteikti tiekėjo portalo prieigą prie kelių tiekėjų paskyrų (pvz., skirtingų juridinių subjektų), visos to asmens vartotojo paskyros turi būti susietos su tuo pačiu užregistruotu kontaktiniu asmenimi.</span><span class="sxs-lookup"><span data-stu-id="1ceab-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="1ceab-127">Vaidmuo **Tiekėjas (išorinis)** apima visas pagrindines galimybes, kurių reikia norint naudoti tiekėjo portale pateikiamas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="1ceab-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="1ceab-128">Ši sąranka padeda užtikrinti, kad vartotojo sąsaja, kurią išorinis vartotojas mato, atitiktų tik numatomą scenarijų.</span><span class="sxs-lookup"><span data-stu-id="1ceab-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="additional-resources"></a><span data-ttu-id="1ceab-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1ceab-129">Additional resources</span></span>
--------

[<span data-ttu-id="1ceab-130">Bendradarbiavimas su tiekėjais naudojant tiekėjo portalą</span><span class="sxs-lookup"><span data-stu-id="1ceab-130">Collaborate with vendors by using the Vendor portal</span></span>](collaborate-vendors-vendor-portal.md)




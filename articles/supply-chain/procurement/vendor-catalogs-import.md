---
title: Importuoti tiekėjų katalogus
description: Šioje temoje aprašomas tiekėjo katalogo duomenų importavimo procesas.
author: mkirknel
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 608d2b57bb4d5ab80d75b22ed5c8a4df5263e5f3
ms.sourcegitcommit: 86052c58e3c365c443bd6f37ad1054bea395e21b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/06/2020
ms.locfileid: "3338313"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="3fc37-103">Importuoti tiekėjų katalogus</span><span class="sxs-lookup"><span data-stu-id="3fc37-103">Import vendor catalogs</span></span>

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="3fc37-104">Tiekėjo katalogų importavimas</span><span class="sxs-lookup"><span data-stu-id="3fc37-104">Vendor catalogs import</span></span>

<span data-ttu-id="3fc37-105">Naudojant „Dynamics 365 Supply Chain Management“, pirkimo specialistai gali kurti ir tvarkyti katalogus, kuriuos įmonės darbuotojai gali naudoti užsakydami prekes ir paslaugas vidaus naudojimui.</span><span class="sxs-lookup"><span data-stu-id="3fc37-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="3fc37-106">Norėdami sukurti įsigijimo katalogą, norimas darbuotojams siūlyti prekes ir paslaugas galite įtraukti importuodami produktų katalogo duomenis arba patys neautomatiškai įtraukdami produktų katalogo duomenis į bendrąjį produktą.</span><span class="sxs-lookup"><span data-stu-id="3fc37-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="3fc37-107">Galite įkelti tiekėjo naudojantis „Microsoft Dynamics 365“ klientu pateiktus katalogo duomenis.</span><span class="sxs-lookup"><span data-stu-id="3fc37-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="3fc37-108">Tiekėjas produkto duomenis turi pateikti kaip katalogo techninės priežiūros užklausos (CRM) failą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="3fc37-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="3fc37-109">CMR faile turi būti pateikiama informacija apie tiekėjo jūsų įmonei tiekiamus produktus.</span><span class="sxs-lookup"><span data-stu-id="3fc37-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="3fc37-110">Importuoti tiekėjo katalogo duomenis</span><span class="sxs-lookup"><span data-stu-id="3fc37-110">Import vendor catalog data</span></span>

<span data-ttu-id="3fc37-111">Norėdami importuoti tiekėjo katalogo duomenis, turite atlikti toliau nurodytas užduotis.</span><span class="sxs-lookup"><span data-stu-id="3fc37-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1. <span data-ttu-id="3fc37-112">Darbo srityje Duomenų valdymas, kurioje nurodėte savo duomenų išdėstymo taisykles, parenkite projektą.</span><span class="sxs-lookup"><span data-stu-id="3fc37-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="3fc37-113">Pasirinkite **Duomenų valdymas**, po to pasirinkite **Nustatyti duomenų projektų vaidmenis**.</span><span class="sxs-lookup"><span data-stu-id="3fc37-113">Select **Data management** and then select **Set up roles for data projects**.</span></span>

2. <span data-ttu-id="3fc37-114">Nustatykite įsigijimo kategorijų hierarchiją ir priskirkite savo tiekėjus įsigijimo kategorijoms.</span><span class="sxs-lookup"><span data-stu-id="3fc37-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="3fc37-115">Jei naudojate prekių kodus, įtraukite juos į įsigijimo kategorijas.</span><span class="sxs-lookup"><span data-stu-id="3fc37-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="3fc37-116">Informacijos apie tai, kaip nustatyti įsigijimo kategorijų hierarchiją, ieškokite dalyje [Nustatyti įsigijimo kategorijų hierarchiją](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="3fc37-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3. <span data-ttu-id="3fc37-117">Sukonfigūruokite katalogo importavimo tiekėją.</span><span class="sxs-lookup"><span data-stu-id="3fc37-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="3fc37-118">Pasirinkite tiekėją, po to pasirinkite **Įsigijimas** > **Sąranka** > **Sukonfigūruoti katalogo importavimo tiekėją**.</span><span class="sxs-lookup"><span data-stu-id="3fc37-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4. <span data-ttu-id="3fc37-119">Sukonfigūruokite katalogo importavimo darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="3fc37-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="3fc37-120">Sukurkite CMR failo šabloną ir pasidalinkite juo su savo tiekėju.</span><span class="sxs-lookup"><span data-stu-id="3fc37-120">Create a CMR file template and share this with your vendor.</span></span>

5. <span data-ttu-id="3fc37-121">Norėdami sukurti tiekėjo katalogą, pasirinkite **Įsigijimas ir šaltinio pasirinkimas** \> **Bendra** \> **Katalogai** \> **Tiekėjo katalogai**.</span><span class="sxs-lookup"><span data-stu-id="3fc37-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="3fc37-122">Iš tiekėjo gauti katalogo techninės priežiūros užklausos (CMR) failai grupuojami šiame kataloge.</span><span class="sxs-lookup"><span data-stu-id="3fc37-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6. <span data-ttu-id="3fc37-123">Nusiųskite CMR failą.</span><span class="sxs-lookup"><span data-stu-id="3fc37-123">Upload the CMR file.</span></span>

7. <span data-ttu-id="3fc37-124">Peržiūrėkite, patvirtinkite arba atmeskite tiekėjo katalogo produktus.</span><span class="sxs-lookup"><span data-stu-id="3fc37-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="3fc37-125">Produktai automatiškai priskiriami įsigijimo kategorijoms.</span><span class="sxs-lookup"><span data-stu-id="3fc37-125">The products are automatically mapped to the procurement categories.</span></span> 

<span data-ttu-id="3fc37-126">Patvirtinti produktai įtraukiami į bendrąjį produktą ir pateikiami pasirinktiems juridiniams subjektams.</span><span class="sxs-lookup"><span data-stu-id="3fc37-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="3fc37-127">Į įsigijimo katalogą glima įtraukti tik patvirtintus produktus.</span><span class="sxs-lookup"><span data-stu-id="3fc37-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="3fc37-128">Generuoti katalogo importavimo failo šabloną</span><span class="sxs-lookup"><span data-stu-id="3fc37-128">Generate a catalog import file template</span></span>

<span data-ttu-id="3fc37-129">Katalogo importavimo failo šablonas yra XSD failas, kurį galite naudoti kurdami CMR failą tiekėjo produktams.</span><span class="sxs-lookup"><span data-stu-id="3fc37-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="3fc37-130">Jūs galite naudoti CMR failą, kad sukurtumėte naują katalogą, pakeistumėte esamą katalogą arba modifikuotumėte esamą katalogą.</span><span class="sxs-lookup"><span data-stu-id="3fc37-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1. <span data-ttu-id="3fc37-131">Pasirinkite **Įsigijimas ir šaltinio pasirinkimas** \> **Katalogai** \> **Tiekėjo katalogai** ir dukart spustelėkite katalogą, su kuriuo norite dirbti.</span><span class="sxs-lookup"><span data-stu-id="3fc37-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor  catalogs** and double-click the catalog that you want  to work with.</span></span>

2. <span data-ttu-id="3fc37-132">Atsisiųskite dabartinio katalogo importavimo šabloną (XSD failas).</span><span class="sxs-lookup"><span data-stu-id="3fc37-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="3fc37-133">Grupės **Susijusi informacija** skirtuko **Katalogai** srities **Veiksmų sritis** puslapyje **Katalogo atnaujinimas** spustelėkite **Kurti katalogo šabloną** ir pasirinkite **Įsigijimo kategorija**.</span><span class="sxs-lookup"><span data-stu-id="3fc37-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    - <span data-ttu-id="3fc37-134">Naudodamiesi parinktimi **Įsigijimo kategorija** galite kurti katalogo šabloną, kuriame nurodomos įsigijimų kategorijos, kuriose tiekėjas yra įgaliotas teikti produktus.</span><span class="sxs-lookup"><span data-stu-id="3fc37-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="3fc37-135">Dialogo lange **Įrašyti kaip** pasirinkite vietą, kurioje norite saugoti katalogo failų šabloną ir įrašykite failą.</span><span class="sxs-lookup"><span data-stu-id="3fc37-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="3fc37-136">Daugiau informacijos ir pavyzdžių rasite šiame tinklaraščio įraše: [„Dynamics AX“ tiekėjo katalogai](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="3fc37-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>

---
title: Kurti juridinius subjektus
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti juridinius subjektus, kuriuos reikia sukurti ir sukonfigūruoti prieš sukuriant kanalus.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 016b67631a53139d12d65dfaf594f49b030326b1
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478217"
---
# <a name="create-legal-entities"></a><span data-ttu-id="eb8a1-103">Kurti juridinius subjektus</span><span class="sxs-lookup"><span data-stu-id="eb8a1-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eb8a1-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti juridinius subjektus, kuriuos reikia sukurti ir sukonfigūruoti prieš sukuriant kanalus.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="eb8a1-105">Juridinis subjektas yra organizacija, turinti registruotą ar įteisintą teisinę struktūrą.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="eb8a1-106">Juridiniai subjektai gali sudaryti teisines sutartis ir privalo paruošti išrašus apie savo veiklą.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="eb8a1-107">Įmonė yra juridinio subjekto tipas.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-107">A company is a type of legal entity.</span></span> <span data-ttu-id="eb8a1-108">Šiuo metu įmonės yra vienintelė juridinių subjektų rūšis, kurią galima kurti, o kiekvienas juridinis subjektas susiejamas su įmonės ID.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="eb8a1-109">Šis susiejimas taikomas todėl, kad kai kuriose duomenų modelių funkcinėse programos srityse naudojamas įmonės ID arba *DataAreaId*.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="eb8a1-110">Dėl duomenų saugumo, šiose funkcinėse srityse naudojimas ribojamas įmonės viduje.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="eb8a1-111">Vartotojai gali gauti prieigą tik prie tos įmonės duomenų, prie kurios yra prisiregistravę.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="eb8a1-112">Kurdami kanalą, turite nurodyti, kuris juridinis subjektas kuriam kanalui priklauso.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="eb8a1-113">Naujo juridinio subjekto kūrimas</span><span class="sxs-lookup"><span data-stu-id="eb8a1-113">Create a new legal entity</span></span>

<span data-ttu-id="eb8a1-114">Norėdami sukurti naują juridinė subjektą „Dynamics 365 Commerce“, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="eb8a1-115">Naršymo srityje eikite į **Moduliai \>Būstinės sąranka \>Juridiniai subjektai**.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="eb8a1-116">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-116">On the action pane, select **New**.</span></span> <span data-ttu-id="eb8a1-117">Dešinėje pradedama rodyti sritis **Naujas juridinis subjektas**.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="eb8a1-118">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="eb8a1-119">Lauke **Įmonė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="eb8a1-120">Lauke **Šalis / regionas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="eb8a1-121">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-121">Select **OK**.</span></span> 

   ![Juridinio subjekto kūrimas](media/legal-entities.png)

1. <span data-ttu-id="eb8a1-123">Skyriuje **Bendri** pateikite toliau išvardytą bendrą informaciją apie juridinį subjektą:</span><span class="sxs-lookup"><span data-stu-id="eb8a1-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="eb8a1-124">Įveskite ieškos pavadinimą, jei paieškos pavadinimas reikalingas.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="eb8a1-125">Ieškos pavadinimas yra alternatyvus pavadinimas, kuris gali būti naudojamas šiam juridiniam subjektui ieškoti.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="eb8a1-126">Pasirinkite, ar šis juridinis subjektas yra naudojamas kaip konsoliduota įmonė.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="eb8a1-127">Pasirinkite, ar šis juridinis subjektas yra naudojamas kaip pašalinimo įmonė.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="eb8a1-128">Pasirinkite subjekto **numatytoji kalba**.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="eb8a1-129">Pasirinkite subjekto **laiko zona**.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="eb8a1-130">Skyriuje **Adresai** pasirinkite **Redaguoti**, kad įvestumėte adreso informaciją, pavyzdžiui, gatvės pavadinimą ir numerį, pašto kodą ir miestą.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="eb8a1-131">Dalyje **Kontaktinė informacija** įveskite informaciją apie bendravimo metodus, pvz., elektroninio pašto adresus, URL ir telefono numerius.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="eb8a1-132">Dalyje **Privalomosios ataskaitos** įveskite registracijos numerius, kurie naudojami privalomosioms ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="eb8a1-133">Dalyje **Registracijos numeriai** įveskite visą informaciją, kurios reikia juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="eb8a1-134">Dalyje **Banko sąskaitos informacija** įveskite juridinio subjekto banko sąskaitas ir banko kodus.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="eb8a1-135">Dalyje **Užsienio prekyba ir logistika** įveskite juridinio subjekto siuntimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="eb8a1-136">Dalyje **Numeracijos** galite peržiūrėti numeracijas, susijusias su juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="eb8a1-137">Tai bus tuščia, kad būtų galima pradėti.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="eb8a1-138">Skyriuje **Ataskaitų srities vaizdas** peržiūrėkite arba keiskite logotipą ir ataskaitų srities vaizdą, susijusį su juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="eb8a1-139">Dalyje **PVM mokėtojo kodas** įveskite registracijos numerius, naudojamus teikiant ataskaitas mokesčių institucijoms.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="eb8a1-140">Dalyje **Mokestis 1099** įveskite juridinio subjekto 1099 informaciją.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="eb8a1-141">Skyriuje **Mokesčių informacija** įveskite juridinio subjekto mokesčių informaciją.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="eb8a1-142">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-142">Select **Save**.</span></span>

<span data-ttu-id="eb8a1-143">Toliau pateiktame vaizde parodytas išsamus juridinio subjekto pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="eb8a1-143">The following image shows details of an example legal entity.</span></span>

![Juridinio subjekto bendrasis skyrius](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="eb8a1-145">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="eb8a1-145">Additional resources</span></span>

[<span data-ttu-id="eb8a1-146">Organizacijų ir organizacijų hierarchijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="eb8a1-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="eb8a1-147">Organizacijos hierarchijos planavimas</span><span class="sxs-lookup"><span data-stu-id="eb8a1-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="eb8a1-148">Organizacijų hierarchijos</span><span class="sxs-lookup"><span data-stu-id="eb8a1-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="eb8a1-149">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="eb8a1-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="eb8a1-150">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="eb8a1-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

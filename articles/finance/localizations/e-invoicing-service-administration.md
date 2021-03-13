---
title: Elektroninių sąskaitų priedo administravimo komponentai
description: Šioje temoje pateikta informacija apie kompnentus, kurie susiję su elektroninių sąskaitų priedų administravimu.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104415"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="86f0c-103">Elektroninių sąskaitų priedo administravimo komponentai</span><span class="sxs-lookup"><span data-stu-id="86f0c-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="86f0c-104">Šioje temoje pateikta informacija apie kompnentus, kurie susiję su elektroninių sąskaitų priedų administravimu.</span><span class="sxs-lookup"><span data-stu-id="86f0c-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="86f0c-105">Taip pat pateikiama informacija apie tai, kaip konfigūruoti elektroninių SF išrašymo papildomą paslaugą.</span><span class="sxs-lookup"><span data-stu-id="86f0c-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="86f0c-106">Azure</span><span class="sxs-lookup"><span data-stu-id="86f0c-106">Azure</span></span>

<span data-ttu-id="86f0c-107">Naudokite „Microsoft Azure“ norėdami sukurti rakto saugyklos ir saugyklos sąskaitos slaptus duomenis.</span><span class="sxs-lookup"><span data-stu-id="86f0c-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="86f0c-108">Tada konfigūruojant elektroninės SF išrašymo priedą naudokite paslapius.</span><span class="sxs-lookup"><span data-stu-id="86f0c-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="86f0c-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="86f0c-109">Lifecycle Services</span></span>

<span data-ttu-id="86f0c-110">Naudokite „Microsoft Dynamics Lifecycle Services“ LCS tam, kad įgalintumėte mikroservices priedą LCS diegimo projektui.</span><span class="sxs-lookup"><span data-stu-id="86f0c-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="86f0c-111">LCS pasirinkite **peržiūros funkcijų valdymo išklotinės** plytelę ir tada įjunkite **el. SF išrašymo paslaugos** funkciją.</span><span class="sxs-lookup"><span data-stu-id="86f0c-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="86f0c-112">„Regulatory Configuration Services“ (RCS)</span><span class="sxs-lookup"><span data-stu-id="86f0c-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="86f0c-113">„Dynamics 365 Regulatory Configuration Services“ (RCS) yra sąsaja, naudojama elektroninio SF išrašymo priedams konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="86f0c-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="86f0c-114">Tokie ištekliai kaip aplinkos ir elektroninių SF išrašymo priemonės kuriamos, prižiūrimos ir laikomos RCS.</span><span class="sxs-lookup"><span data-stu-id="86f0c-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="86f0c-115">Kai ištekliai parengti, jie publikuojami elektroninių SF išrašymo papildomų paslaugų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="86f0c-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="86f0c-116">Daugiau informacijos apie RCS žr. [„Regulatory Configuration Services“ (RCS) – globalizacijos funkcijos](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="86f0c-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="86f0c-117">Darbo su elektroninių SF priedu integravimas</span><span class="sxs-lookup"><span data-stu-id="86f0c-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="86f0c-118">Prieš konfigūruojant elektronines SF naudojant RCS, būtina sukonfigūruoti RCS, kad būtų leidžiama susisiekti su elektroninių SF išrašymo papildymu.</span><span class="sxs-lookup"><span data-stu-id="86f0c-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="86f0c-119">Šią konfigūraciją užbaikite skirtuko **Elektroninės sąskaitos faktūros priedai** **Elektroninės ataskaitos parametrai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="86f0c-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="86f0c-120">Paslaugos galinis punktas</span><span class="sxs-lookup"><span data-stu-id="86f0c-120">Service endpoint</span></span>

<span data-ttu-id="86f0c-121">Elektroninio SF išrašymo galinio punkto URL gali skirtis, atsižvelgiant į "Azure" duomenų centro geografijos metodą.</span><span class="sxs-lookup"><span data-stu-id="86f0c-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="86f0c-122">Toliau esančioje lentelėje pateikiamas pasiekiamumo sąrašas pagal regioną:</span><span class="sxs-lookup"><span data-stu-id="86f0c-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="86f0c-123">„Azure" duomenų centro geografija</span><span class="sxs-lookup"><span data-stu-id="86f0c-123">Azure datacenter geography</span></span> | <span data-ttu-id="86f0c-124">Paslaugos galinio punkto URL</span><span class="sxs-lookup"><span data-stu-id="86f0c-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="86f0c-125">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="86f0c-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="86f0c-126">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="86f0c-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="86f0c-127">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="86f0c-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="86f0c-128">Vakarinė ES</span><span class="sxs-lookup"><span data-stu-id="86f0c-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="86f0c-129">Programos ID</span><span class="sxs-lookup"><span data-stu-id="86f0c-129">Application ID</span></span>

<span data-ttu-id="86f0c-130">Prašymo ID yra elektroninio SF išrašymo priedo prašymo ID.</span><span class="sxs-lookup"><span data-stu-id="86f0c-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="86f0c-131">Šiuo atveju, vertė yra fiksuota: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="86f0c-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="86f0c-132">LCS aplinkos ID</span><span class="sxs-lookup"><span data-stu-id="86f0c-132">LCS environment ID</span></span>

<span data-ttu-id="86f0c-133">LCS aplinkos ID yra jūsų organizacijos LCS abonemento ID.</span><span class="sxs-lookup"><span data-stu-id="86f0c-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="86f0c-134">Paslaugų aplinkos</span><span class="sxs-lookup"><span data-stu-id="86f0c-134">Service environments</span></span>

<span data-ttu-id="86f0c-135">Aptarnavimo aplinkos yra loginiai skaidiniai, kurie sukurti elektroninių SF išrašymo funkcijų vykdymui elektroninio SF išrašymo papildinyje palaikyti.</span><span class="sxs-lookup"><span data-stu-id="86f0c-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="86f0c-136">Saugos slapyme ir skaitmeniniuose sertifikatuose, ir pereigimas (t. y. prieigos teisės) turi būti konfigūruojamas tarnybos aplinkos lygiu.</span><span class="sxs-lookup"><span data-stu-id="86f0c-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="86f0c-137">Klientai gali sukurti tiek aptarnavimo aplinkos, kiek tik norite.</span><span class="sxs-lookup"><span data-stu-id="86f0c-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="86f0c-138">Visos kliento sukuriamos aptarnavimo aplinkos yra nepriklausomos vienas nuo kito.</span><span class="sxs-lookup"><span data-stu-id="86f0c-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="86f0c-139">Aptarnavimo aplinkos turi būti sukurtos ir tvarkomos RCS.</span><span class="sxs-lookup"><span data-stu-id="86f0c-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="86f0c-140">Kai paslaugų aplinkos parengti, jie turi būti publikuoti elektroninių SF išrašymo papildomų paslaugų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="86f0c-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="86f0c-141">Paslaugų aplinkos būsena</span><span class="sxs-lookup"><span data-stu-id="86f0c-141">Service environment status</span></span>

<span data-ttu-id="86f0c-142">Aptarnavimo aplinkas galima valdyti naudojant būseną.</span><span class="sxs-lookup"><span data-stu-id="86f0c-142">Service environments can be managed through status.</span></span> <span data-ttu-id="86f0c-143">Galimos parinktys yra šios:</span><span class="sxs-lookup"><span data-stu-id="86f0c-143">The possible options are:</span></span>

- <span data-ttu-id="86f0c-144">**Nepaskelbta** – aplinka sukurta, bet dar nepaskelbta.</span><span class="sxs-lookup"><span data-stu-id="86f0c-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="86f0c-145">**Publikuota** – aplinka publikuota elektroninio SF išrašymo prieduose.</span><span class="sxs-lookup"><span data-stu-id="86f0c-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="86f0c-146">**Pakeista** – publikuoto aplinkos atributai pakeisti, bet pakeitimai dar nebuvo publikuoti.</span><span class="sxs-lookup"><span data-stu-id="86f0c-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="86f0c-147">Kliento raktai</span><span class="sxs-lookup"><span data-stu-id="86f0c-147">Customer secrets</span></span>

<span data-ttu-id="86f0c-148">Elektroninių SF išrašymo priedo paslauga yra atsakinga už visų jūsų verslo duomenų saugojimą „Azure” ištekliuose, kurie priklauso jūsų įmonei.</span><span class="sxs-lookup"><span data-stu-id="86f0c-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="86f0c-149">Siekiant užtikrinti, kad paslauga veiktų tinkamai ir kad visus verslo duomenis, kurie būtini elektroninių SF išrašymo priedui ir kuriuos jis sugeneravo, galėtų pasiekti tik priedas, turite sukurti du pagrindinius toliau pateiktus „Azure” išteklius.</span><span class="sxs-lookup"><span data-stu-id="86f0c-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="86f0c-150">„Azure” saugyklos abonementas („Blob“ saugykla) saugos elektronines SF</span><span class="sxs-lookup"><span data-stu-id="86f0c-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="86f0c-151">„Azure” raktų saugykla, kuri laikys sertifikatus ir suvienodintą saugyklos paskyros išteklių identifikatorių (URI)</span><span class="sxs-lookup"><span data-stu-id="86f0c-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="86f0c-152">Paskirti raktų saugyklos ištekliai ir kliento talpyklos paskyra turi būti priskirti tik elektroninių SF išrašymo priedo naudojimui.</span><span class="sxs-lookup"><span data-stu-id="86f0c-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="86f0c-153">Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="86f0c-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="86f0c-154">Vartotojai</span><span class="sxs-lookup"><span data-stu-id="86f0c-154">Users</span></span>

<span data-ttu-id="86f0c-155">Kiekviena aptarnavimo aplinka turi pateikti vartotojų, kurie gali prisijungti „Dynamics 365 Finance“ prie elektroninių „Dynamics 365 Supply Chain Management“ SF išrašymo priedo ir prie jo prisijungti, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="86f0c-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="86f0c-156">Publikavimas</span><span class="sxs-lookup"><span data-stu-id="86f0c-156">Publication</span></span>

<span data-ttu-id="86f0c-157">Paslaugų aplinkos turi būti publikuotos elektroninių SF išrašymo priede prieš jų naudojimą.</span><span class="sxs-lookup"><span data-stu-id="86f0c-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="86f0c-158">„Finance and Supply Chain Management“ gali pasiekti tik paskelbtas aplinkas.</span><span class="sxs-lookup"><span data-stu-id="86f0c-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="86f0c-159">Be to, paslaugų aplinka turi būti publikuota prieš tai, kai visi atributų naujinimai įsigalios elektroninių SF išrašymo paslaugai.</span><span class="sxs-lookup"><span data-stu-id="86f0c-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="86f0c-160">Prijungtos programos</span><span class="sxs-lookup"><span data-stu-id="86f0c-160">Connected applications</span></span>

<span data-ttu-id="86f0c-161">Susijusios programos yra „Finance and Supply Chain Management“ egzemplioriai, kuriuos jūs galite norėti pasiekti naudodami RCS.</span><span class="sxs-lookup"><span data-stu-id="86f0c-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="86f0c-162">Be programos URL ir jo nuomininko, susijusioje programoje yra kredencialai, kurie leidžia RCS prisijungti prie aplinkos.</span><span class="sxs-lookup"><span data-stu-id="86f0c-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="86f0c-163">Naudodami susijusias programas galite konfigūruoti dalį elektroninių SF išrašymo priemonės „Finance and Supply Chain Management“, kad būtų veikia visa elektroninių SF išrašymo priemonė.</span><span class="sxs-lookup"><span data-stu-id="86f0c-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="86f0c-164">„Finance and Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="86f0c-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="86f0c-165">Integravimas su elektroninių SF priedu</span><span class="sxs-lookup"><span data-stu-id="86f0c-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="86f0c-166">Prieš naudojant „Finance and Supply Chain Management“ elektroninėms SF išduoti naudojant elektroninių SF išrašymo priedą, priedas turi būti sukonfigūruotas taip, kad leistų ryšį su tarnyba.</span><span class="sxs-lookup"><span data-stu-id="86f0c-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="86f0c-167">Elektroninių SF išrašymo priedo funkcijos integravimas</span><span class="sxs-lookup"><span data-stu-id="86f0c-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="86f0c-168">Norėdami įgalinti „Finance and Supply Chain Management“ ir elektroninio SF išrašymo priedo ryšį, turite įjungti integravimo priemonę **Elektroninio SF išrašymo priedo integravimas** funkciją **Funkcijų valdymas** darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="86f0c-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="86f0c-169">Paslaugos galinis punktas</span><span class="sxs-lookup"><span data-stu-id="86f0c-169">Service endpoint</span></span>

<span data-ttu-id="86f0c-170">Paslaugos galinis punktas yra URL, kuriame yra elektroninio SF išrašymo priedas.</span><span class="sxs-lookup"><span data-stu-id="86f0c-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="86f0c-171">Prieš elektroninių sąskaitų išleidimą, paslaugos galinis taškas turi būti konfigūruotas „Finance and Supply Chain Management“ siekiant leisti komunikaciją su paslaugomis.</span><span class="sxs-lookup"><span data-stu-id="86f0c-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="86f0c-172">Norėdami konfigūruoti paslaugų galinį tašką, eikite į **Organizacijos administravimas \> Nustatymai \> Elektroninio dokumento parametras** ir tada **Pateikimo tarnybos** skirtukas, laukelyje **Elektroninės sąskaitos priedo URL** laukelis ir įveskite URL kaip aprašyta lentelėje skyriuje **Paslaugos galinis taškas**.</span><span class="sxs-lookup"><span data-stu-id="86f0c-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="86f0c-173">Aplinkos</span><span class="sxs-lookup"><span data-stu-id="86f0c-173">Environments</span></span>

<span data-ttu-id="86f0c-174">Aplinkos pavadinimas, įvestas „Finance and Supply Chain Management“ remiasi aplinkos, kuri sukurta RCS ir paskelbta elektroninio SF išrašymo prieduose, pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="86f0c-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="86f0c-175">Aplinka turi būti konfigūruojama **Pateikimo paslaugų** skirtuke **Elektroninio dokumento parametro** puslapyje taip, kad kiekvienoje užklausoje išduoti elektronines SF būtų aplinka, kur elektroninio SF išrašymo priedas gali nustatyti, kuri elektroninių SF išrašymo funkcija turi apdoroti užklausą.</span><span class="sxs-lookup"><span data-stu-id="86f0c-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86f0c-176">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="86f0c-176">Additional resources</span></span>

- [<span data-ttu-id="86f0c-177">Elektroninių sąskaitų konfigūravimas RCS</span><span class="sxs-lookup"><span data-stu-id="86f0c-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="86f0c-178">Išduoti elektronines sąskaitas „Finance and Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="86f0c-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)

---
title: Elektroninių SF išrašymo administravimo komponentai
description: Šioje temoje pateikta informacija apie kompnentus, kurie susiję su elektroninių sąskaitų priedų administravimu.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2e859875e124796e49000cd5ea94cfb75ecd768a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840033"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="7fabc-103">Elektroninių SF išrašymo administravimo komponentai</span><span class="sxs-lookup"><span data-stu-id="7fabc-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7fabc-104">Šioje temoje pateikta informacija apie kompnentus, kurie susiję su elektroninių sąskaitų priedų administravimu.</span><span class="sxs-lookup"><span data-stu-id="7fabc-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="7fabc-105">Taip pat pateikiama informacija apie tai, kaip konfigūruoti elektroninių SF išrašymo papildomą paslaugą.</span><span class="sxs-lookup"><span data-stu-id="7fabc-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="7fabc-106">Azure</span><span class="sxs-lookup"><span data-stu-id="7fabc-106">Azure</span></span>

<span data-ttu-id="7fabc-107">Naudokite „Microsoft Azure“ norėdami sukurti rakto saugyklos ir saugyklos sąskaitos slaptus duomenis.</span><span class="sxs-lookup"><span data-stu-id="7fabc-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="7fabc-108">Tada konfigūruojant elektroninės SF išrašymo priedą naudokite paslapius.</span><span class="sxs-lookup"><span data-stu-id="7fabc-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="7fabc-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="7fabc-109">Lifecycle Services</span></span>

<span data-ttu-id="7fabc-110">Naudokite „Microsoft Dynamics Lifecycle Services“ LCS tam, kad įgalintumėte mikroservices priedą LCS diegimo projektui.</span><span class="sxs-lookup"><span data-stu-id="7fabc-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="7fabc-111">Mikropaslaugos LCS priedo įdiegimui reikalingas bent 2 pakopos virtualusis įrenginys.</span><span class="sxs-lookup"><span data-stu-id="7fabc-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="7fabc-112">Daugiau informacijos apie aplinkų planavimą ieškokite skyriuje [Aplinkos planavimas](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="7fabc-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="7fabc-113">„Regulatory Configuration Services“ (RCS)</span><span class="sxs-lookup"><span data-stu-id="7fabc-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="7fabc-114">„Dynamics 365 Regulatory Configuration Services“ (RCS) yra sąsaja, naudojama elektroninio SF išrašymo priedams konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="7fabc-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="7fabc-115">Tokie ištekliai kaip aplinkos ir elektroninių SF išrašymo priemonės kuriamos, prižiūrimos ir laikomos RCS.</span><span class="sxs-lookup"><span data-stu-id="7fabc-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="7fabc-116">Kai ištekliai parengti, jie publikuojami elektroninių SF išrašymo papildomų paslaugų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="7fabc-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="7fabc-117">Norėdami sužinoti RCS prisijungimą, žr. skyrių [„Regulatory Services”](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="7fabc-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="7fabc-118">Daugiau informacijos apie RCS žr. [„Regulatory Configuration Services“ (RCS) – globalizacijos funkcijos](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="7fabc-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="7fabc-119">Integravimas su elektroninių SF priedu</span><span class="sxs-lookup"><span data-stu-id="7fabc-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="7fabc-120">Prieš konfigūruojant elektronines SF naudojant RCS, būtina sukonfigūruoti RCS, kad būtų leidžiama susisiekti su elektroninių SF išrašymo papildymu.</span><span class="sxs-lookup"><span data-stu-id="7fabc-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="7fabc-121">Šią konfigūraciją užbaikite skirtuko **Elektroninės sąskaitos faktūros priedai** **Elektroninės ataskaitos parametrai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="7fabc-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="7fabc-122">Paslaugos galinis punktas</span><span class="sxs-lookup"><span data-stu-id="7fabc-122">Service endpoint</span></span>

<span data-ttu-id="7fabc-123">Elektroninių SF išrašymo priedas yra keliuose „Azure” duomenų centro regionuose.</span><span class="sxs-lookup"><span data-stu-id="7fabc-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="7fabc-124">Toliau esančioje lentelėje pateikiamas pasiekiamumo sąrašas pagal regioną.</span><span class="sxs-lookup"><span data-stu-id="7fabc-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="7fabc-125">„Azure" duomenų centro geografija</span><span class="sxs-lookup"><span data-stu-id="7fabc-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="7fabc-126">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="7fabc-126">East US</span></span>                    |
| <span data-ttu-id="7fabc-127">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="7fabc-127">West US</span></span>                    |
| <span data-ttu-id="7fabc-128">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="7fabc-128">North EU</span></span>                   |
| <span data-ttu-id="7fabc-129">Vakarų ES</span><span class="sxs-lookup"><span data-stu-id="7fabc-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="7fabc-130">Paslaugų aplinkos</span><span class="sxs-lookup"><span data-stu-id="7fabc-130">Service environments</span></span>

<span data-ttu-id="7fabc-131">Aptarnavimo aplinkos yra loginiai skaidiniai, kurie sukurti elektroninių SF išrašymo funkcijų vykdymui elektroninio SF išrašymo papildinyje palaikyti.</span><span class="sxs-lookup"><span data-stu-id="7fabc-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="7fabc-132">Saugos slapyme ir skaitmeniniuose sertifikatuose, ir pereigimas (t. y. prieigos teisės) turi būti konfigūruojamas tarnybos aplinkos lygiu.</span><span class="sxs-lookup"><span data-stu-id="7fabc-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="7fabc-133">Klientai gali sukurti tiek aptarnavimo aplinkos, kiek tik norite.</span><span class="sxs-lookup"><span data-stu-id="7fabc-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="7fabc-134">Visos kliento sukuriamos aptarnavimo aplinkos yra nepriklausomos vienas nuo kito.</span><span class="sxs-lookup"><span data-stu-id="7fabc-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="7fabc-135">Aptarnavimo aplinkos turi būti sukurtos ir tvarkomos RCS.</span><span class="sxs-lookup"><span data-stu-id="7fabc-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="7fabc-136">Kai paslaugų aplinkos parengti, jie turi būti publikuoti elektroninių SF išrašymo papildomų paslaugų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="7fabc-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="7fabc-137">Paslaugų aplinkos būsena</span><span class="sxs-lookup"><span data-stu-id="7fabc-137">Service environment status</span></span>

<span data-ttu-id="7fabc-138">Aptarnavimo aplinkas galima valdyti naudojant būseną.</span><span class="sxs-lookup"><span data-stu-id="7fabc-138">Service environments can be managed through status.</span></span> <span data-ttu-id="7fabc-139">Galimos parinktys yra šios:</span><span class="sxs-lookup"><span data-stu-id="7fabc-139">The possible options are:</span></span>

- <span data-ttu-id="7fabc-140">**Nepaskelbta** – aplinka sukurta, bet dar nepaskelbta.</span><span class="sxs-lookup"><span data-stu-id="7fabc-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="7fabc-141">**Publikuota** – aplinka publikuota elektroninio SF išrašymo prieduose.</span><span class="sxs-lookup"><span data-stu-id="7fabc-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="7fabc-142">**Pakeista** – publikuoto aplinkos atributai pakeisti, bet pakeitimai dar nebuvo publikuoti.</span><span class="sxs-lookup"><span data-stu-id="7fabc-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="7fabc-143">Kliento raktai</span><span class="sxs-lookup"><span data-stu-id="7fabc-143">Customer secrets</span></span>

<span data-ttu-id="7fabc-144">Elektroninių SF išrašymo priedo paslauga yra atsakinga už visų jūsų verslo duomenų saugojimą „Azure” ištekliuose, kurie priklauso jūsų įmonei.</span><span class="sxs-lookup"><span data-stu-id="7fabc-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="7fabc-145">Siekiant užtikrinti, kad paslauga veiktų tinkamai ir kad visus verslo duomenis, kurių reikia elektroninių SF išrašymo priedui ir kuriuos jis sugeneravo, galėtų pasiekti tik priedas, turite sukurti du pagrindinius toliau pateiktus „Azure” išteklius:</span><span class="sxs-lookup"><span data-stu-id="7fabc-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="7fabc-146">„Azure” saugyklos abonementas („Blob“ saugykla) saugos elektronines SF</span><span class="sxs-lookup"><span data-stu-id="7fabc-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="7fabc-147">„Azure” raktų saugykla, kuri laikys sertifikatus ir suvienodintą saugyklos paskyros išteklių identifikatorių (URI)</span><span class="sxs-lookup"><span data-stu-id="7fabc-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="7fabc-148">Paskirti raktų saugyklos ištekliai ir kliento talpyklos paskyra turi būti priskirti tik elektroninių SF išrašymo priedo naudojimui .</span><span class="sxs-lookup"><span data-stu-id="7fabc-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing .</span></span>

<span data-ttu-id="7fabc-149">Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="7fabc-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="7fabc-150">Vartotojai</span><span class="sxs-lookup"><span data-stu-id="7fabc-150">Users</span></span>

<span data-ttu-id="7fabc-151">Kiekviena aptarnavimo aplinka turi pateikti vartotojų, kurie gali prisijungti „Dynamics 365 Finance“ prie elektroninių „Dynamics 365 Supply Chain Management“ SF išrašymo priedo ir prie jo prisijungti, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="7fabc-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="7fabc-152">Publikavimas</span><span class="sxs-lookup"><span data-stu-id="7fabc-152">Publication</span></span>

<span data-ttu-id="7fabc-153">Paslaugų aplinkos turi būti publikuotos elektroninių SF išrašymo priede prieš jų naudojimą.</span><span class="sxs-lookup"><span data-stu-id="7fabc-153">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="7fabc-154">„Finance and Supply Chain Management“ gali pasiekti tik paskelbtas aplinkas.</span><span class="sxs-lookup"><span data-stu-id="7fabc-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="7fabc-155">Be to, paslaugų aplinka turi būti publikuota prieš tai, kai visi atributų naujinimai įsigalios elektroninių SF išrašymo paslaugai.</span><span class="sxs-lookup"><span data-stu-id="7fabc-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="7fabc-156">Prijungtos programos</span><span class="sxs-lookup"><span data-stu-id="7fabc-156">Connected applications</span></span>

<span data-ttu-id="7fabc-157">Susijusios programos yra „Finance and Supply Chain Management“ egzemplioriai, kuriuos jūs galite norėti pasiekti naudodami RCS.</span><span class="sxs-lookup"><span data-stu-id="7fabc-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="7fabc-158">Be programos URL ir jo nuomininko, susijusioje programoje yra kredencialai, kurie leidžia RCS prisijungti prie aplinkos.</span><span class="sxs-lookup"><span data-stu-id="7fabc-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="7fabc-159">Naudodami susijusias programas galite konfigūruoti dalį elektroninių SF išrašymo priemonės „Finance and Supply Chain Management“, kad būtų veikia visa elektroninių SF išrašymo priemonė.</span><span class="sxs-lookup"><span data-stu-id="7fabc-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="7fabc-160">„Finance and Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="7fabc-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="7fabc-161">Integravimas su elektroninių SF priedu</span><span class="sxs-lookup"><span data-stu-id="7fabc-161">Integration with Electronic invoicing</span></span>

<span data-ttu-id="7fabc-162">Prieš naudojant „Finance and Supply Chain Management“ elektroninėms SF išduoti naudojant elektroninių SF išrašymo priedą, priedas turi būti sukonfigūruotas taip, kad leistų ryšį su tarnyba.</span><span class="sxs-lookup"><span data-stu-id="7fabc-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="7fabc-163">Elektroninių SF išrašymo priedo funkcijos integravimas</span><span class="sxs-lookup"><span data-stu-id="7fabc-163">Electronic invoicing integration feature</span></span>

<span data-ttu-id="7fabc-164">Norėdami įgalinti „Finance and Supply Chain Management“ ir elektroninio SF išrašymo priedo ryšį, turite įjungti integravimo priemonę **Elektroninio SF išrašymo priedo integravimas** funkciją **Funkcijų valdymas** darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="7fabc-164">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="7fabc-165">Paslaugos galinis punktas</span><span class="sxs-lookup"><span data-stu-id="7fabc-165">Service endpoint</span></span>

<span data-ttu-id="7fabc-166">Paslaugos galinis punktas yra URL, kuriame yra elektroninio SF išrašymo priedas.</span><span class="sxs-lookup"><span data-stu-id="7fabc-166">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="7fabc-167">Prieš elektroninių sąskaitų išleidimą, paslaugos galinis taškas turi būti konfigūruotas „Finance and Supply Chain Management“ siekiant leisti komunikaciją su paslaugomis.</span><span class="sxs-lookup"><span data-stu-id="7fabc-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="7fabc-168">Norėdami konfigūruoti paslaugų galinį tašką, eikite į **Organizacijos administravimas \> Nustatymai \> Elektroninio dokumento parametras** ir tada **Pateikimo tarnybos** skirtukas, laukelyje **Elektroninės sąskaitos priedo URL** laukelis ir įveskite URL kaip aprašyta lentelėje skyriuje **Paslaugos galinis taškas**.</span><span class="sxs-lookup"><span data-stu-id="7fabc-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="7fabc-169">Aplinkos</span><span class="sxs-lookup"><span data-stu-id="7fabc-169">Environments</span></span>

<span data-ttu-id="7fabc-170">Aplinkos pavadinimas, įvestas „Finance and Supply Chain Management“ remiasi aplinkos, kuri sukurta RCS ir paskelbta elektroninio SF išrašymo prieduose, pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="7fabc-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="7fabc-171">Aplinka turi būti konfigūruojama **Pateikimo paslaugų** skirtuke **Elektroninio dokumento parametro** puslapyje taip, kad kiekvienoje užklausoje išduoti elektronines SF būtų aplinka, kur elektroninio SF išrašymo priedas gali nustatyti, kuri elektroninių SF išrašymo funkcija turi apdoroti užklausą.</span><span class="sxs-lookup"><span data-stu-id="7fabc-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fabc-172">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7fabc-172">Additional resources</span></span>

- [<span data-ttu-id="7fabc-173">Elektroninių sąskaitų konfigūravimas RCS</span><span class="sxs-lookup"><span data-stu-id="7fabc-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="7fabc-174">Išduoti elektronines sąskaitas „Finance and Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="7fabc-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

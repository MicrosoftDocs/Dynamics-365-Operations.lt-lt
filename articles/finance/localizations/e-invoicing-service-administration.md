---
title: Elektroninių SF išrašymo administravimo komponentai
description: Šioje temoje pateikta informacija apie kompnentus, kurie susiję su elektroninių sąskaitų priedų administravimu.
author: gionoder
ms.date: 04/29/2021
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
ms.openlocfilehash: 3ac4a03d75898680b5655421f3024dc6f666464c
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963196"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="055d9-103">Elektroninių SF išrašymo administravimo komponentai</span><span class="sxs-lookup"><span data-stu-id="055d9-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="055d9-104">Šioje temoje pateikta informacija apie kompnentus, kurie susiję su elektroninių sąskaitų priedų administravimu.</span><span class="sxs-lookup"><span data-stu-id="055d9-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="055d9-105">Taip pat pateikiama informacija apie tai, kaip konfigūruoti elektroninių SF išrašymo papildomą paslaugą.</span><span class="sxs-lookup"><span data-stu-id="055d9-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="055d9-106">Azure</span><span class="sxs-lookup"><span data-stu-id="055d9-106">Azure</span></span>

<span data-ttu-id="055d9-107">Naudokite „Microsoft Azure“ norėdami sukurti rakto saugyklos ir saugyklos sąskaitos slaptus duomenis.</span><span class="sxs-lookup"><span data-stu-id="055d9-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="055d9-108">Tada konfigūruojant elektroninės SF išrašymo priedą naudokite paslapius.</span><span class="sxs-lookup"><span data-stu-id="055d9-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="055d9-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="055d9-109">Lifecycle Services</span></span>

<span data-ttu-id="055d9-110">Naudokite „Microsoft Dynamics Lifecycle Services“ LCS tam, kad įgalintumėte mikroservices priedą LCS diegimo projektui.</span><span class="sxs-lookup"><span data-stu-id="055d9-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="055d9-111">Mikropaslaugos LCS priedo įdiegimui reikalingas bent 2 pakopos virtualusis įrenginys.</span><span class="sxs-lookup"><span data-stu-id="055d9-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="055d9-112">Daugiau informacijos apie aplinkų planavimą ieškokite skyriuje [Aplinkos planavimas](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="055d9-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="055d9-113">„Regulatory Configuration Services“ (RCS)</span><span class="sxs-lookup"><span data-stu-id="055d9-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="055d9-114">„Dynamics 365 Regulatory Configuration Services“ (RCS) yra sąsaja, naudojama elektroninio SF išrašymo priedams konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="055d9-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="055d9-115">Tokie ištekliai kaip aplinkos ir elektroninių SF išrašymo priemonės kuriamos, prižiūrimos ir laikomos RCS.</span><span class="sxs-lookup"><span data-stu-id="055d9-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="055d9-116">Kai ištekliai parengti, jie publikuojami elektroninių SF išrašymo papildomų paslaugų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="055d9-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="055d9-117">Norėdami sužinoti RCS prisijungimą, žr. skyrių [„Regulatory Services”](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="055d9-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="055d9-118">Daugiau informacijos apie RCS žr. [„Regulatory Configuration Services“ (RCS) – globalizacijos funkcijos](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="055d9-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="055d9-119">Integravimas su elektroninių SF priedu</span><span class="sxs-lookup"><span data-stu-id="055d9-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="055d9-120">Prieš konfigūruojant elektronines SF naudojant RCS, būtina sukonfigūruoti RCS, kad būtų leidžiama susisiekti su elektroninių SF išrašymo papildymu.</span><span class="sxs-lookup"><span data-stu-id="055d9-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="055d9-121">Šią konfigūraciją užbaikite skirtuko **Elektroninės sąskaitos faktūros priedai** **Elektroninės ataskaitos parametrai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="055d9-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="055d9-122">Paslaugos galinis punktas</span><span class="sxs-lookup"><span data-stu-id="055d9-122">Service endpoint</span></span>

<span data-ttu-id="055d9-123">Elektroninių SF išrašymo priedas yra keliuose „Azure” duomenų centro regionuose.</span><span class="sxs-lookup"><span data-stu-id="055d9-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="055d9-124">Toliau esančioje lentelėje pateikiamas pasiekiamumo sąrašas pagal regioną.</span><span class="sxs-lookup"><span data-stu-id="055d9-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="055d9-125">„Azure" duomenų centro geografija</span><span class="sxs-lookup"><span data-stu-id="055d9-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="055d9-126">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="055d9-126">East US</span></span>                    |
| <span data-ttu-id="055d9-127">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="055d9-127">West US</span></span>                    |
| <span data-ttu-id="055d9-128">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="055d9-128">North EU</span></span>                   |
| <span data-ttu-id="055d9-129">Vakarų ES</span><span class="sxs-lookup"><span data-stu-id="055d9-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="055d9-130">Paslaugų aplinkos</span><span class="sxs-lookup"><span data-stu-id="055d9-130">Service environments</span></span>

<span data-ttu-id="055d9-131">Aptarnavimo aplinkos yra loginiai skaidiniai, kurie sukurti elektroninių SF išrašymo funkcijų vykdymui elektroninio SF išrašymo papildinyje palaikyti.</span><span class="sxs-lookup"><span data-stu-id="055d9-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="055d9-132">Saugos slapyme ir skaitmeniniuose sertifikatuose, ir pereigimas (t. y. prieigos teisės) turi būti konfigūruojamas tarnybos aplinkos lygiu.</span><span class="sxs-lookup"><span data-stu-id="055d9-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="055d9-133">Klientai gali sukurti tiek aptarnavimo aplinkos, kiek tik norite.</span><span class="sxs-lookup"><span data-stu-id="055d9-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="055d9-134">Visos kliento sukuriamos aptarnavimo aplinkos yra nepriklausomos vienas nuo kito.</span><span class="sxs-lookup"><span data-stu-id="055d9-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="055d9-135">Aptarnavimo aplinkos turi būti sukurtos ir tvarkomos RCS.</span><span class="sxs-lookup"><span data-stu-id="055d9-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="055d9-136">Kai paslaugų aplinkos parengti, jie turi būti publikuoti elektroninių SF išrašymo papildomų paslaugų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="055d9-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="055d9-137">Paslaugų aplinkos būsena</span><span class="sxs-lookup"><span data-stu-id="055d9-137">Service environment status</span></span>

<span data-ttu-id="055d9-138">Aptarnavimo aplinkas galima valdyti naudojant būseną.</span><span class="sxs-lookup"><span data-stu-id="055d9-138">Service environments can be managed through status.</span></span> <span data-ttu-id="055d9-139">Galimos parinktys yra šios:</span><span class="sxs-lookup"><span data-stu-id="055d9-139">The possible options are:</span></span>

- <span data-ttu-id="055d9-140">**Nepaskelbta** – aplinka sukurta, bet dar nepaskelbta.</span><span class="sxs-lookup"><span data-stu-id="055d9-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="055d9-141">**Publikuota** – aplinka publikuota elektroninio SF išrašymo prieduose.</span><span class="sxs-lookup"><span data-stu-id="055d9-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="055d9-142">**Pakeista** – publikuoto aplinkos atributai pakeisti, bet pakeitimai dar nebuvo publikuoti.</span><span class="sxs-lookup"><span data-stu-id="055d9-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="055d9-143">Kliento raktai</span><span class="sxs-lookup"><span data-stu-id="055d9-143">Customer secrets</span></span>

<span data-ttu-id="055d9-144">Elektroninių SF išrašymo priedo paslauga yra atsakinga už visų jūsų verslo duomenų saugojimą „Azure” ištekliuose, kurie priklauso jūsų įmonei.</span><span class="sxs-lookup"><span data-stu-id="055d9-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="055d9-145">Siekiant užtikrinti, kad paslauga veiktų tinkamai ir kad visus verslo duomenis, kurių reikia elektroninių SF išrašymo priedui ir kuriuos jis sugeneravo, galėtų pasiekti tik priedas, turite sukurti du pagrindinius toliau pateiktus „Azure” išteklius:</span><span class="sxs-lookup"><span data-stu-id="055d9-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="055d9-146">„Azure” saugyklos abonementas („Blob“ saugykla) saugos elektronines SF</span><span class="sxs-lookup"><span data-stu-id="055d9-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="055d9-147">„Azure Key Vault”, kuri laikys sertifikatus ir suvienodintą saugyklos paskyros išteklių identifikatorių (URI)</span><span class="sxs-lookup"><span data-stu-id="055d9-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="055d9-148">Paskirti „Key Vault“ ištekliai ir kliento talpyklos paskyra turi būti priskirti tik elektroninių SF išrašymo priedo naudojimui .</span><span class="sxs-lookup"><span data-stu-id="055d9-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="055d9-149">Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir „Key Vault“ raktą](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="055d9-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="055d9-150">Norėdami stebėti „Key Vault" apsaugą ir gauti įspėjimus, sukonfigūruokite „Azure Monitor for Key Vault".</span><span class="sxs-lookup"><span data-stu-id="055d9-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="055d9-151">Įjungus „Key Vault" registravimą, galima stebėti, kaip, kada ir kas turi prieigą prie „Key Vault".</span><span class="sxs-lookup"><span data-stu-id="055d9-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="055d9-152">Norėdami gauti daugiau informacijos, [žr. „Azure Key Vault" stebėjimą ir įspėjimą](/azure/key-vault/general/alert) bei kaip įgalinti [„Key Vault"](/azure/key-vault/general/howto-logging?tabs=azure-cli) registravimą.</span><span class="sxs-lookup"><span data-stu-id="055d9-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="055d9-153">Geriausia, jei norite periodiškai pasukti paslapius.</span><span class="sxs-lookup"><span data-stu-id="055d9-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="055d9-154">Daugiau informacijos ieškokite [Raktų dokumentacijoje](/azure/key-vault/secrets/).</span><span class="sxs-lookup"><span data-stu-id="055d9-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="055d9-155">Vartotojai</span><span class="sxs-lookup"><span data-stu-id="055d9-155">Users</span></span>

<span data-ttu-id="055d9-156">Kiekviena aptarnavimo aplinka turi pateikti vartotojų, kurie gali prisijungti „Dynamics 365 Finance“ prie elektroninių „Dynamics 365 Supply Chain Management“ SF išrašymo priedo ir prie jo prisijungti, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="055d9-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="055d9-157">Publikavimas</span><span class="sxs-lookup"><span data-stu-id="055d9-157">Publication</span></span>

<span data-ttu-id="055d9-158">Paslaugų aplinkos turi būti publikuotos elektroninių SF išrašymo priede prieš jų naudojimą.</span><span class="sxs-lookup"><span data-stu-id="055d9-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="055d9-159">„Finance and Supply Chain Management“ gali pasiekti tik paskelbtas aplinkas.</span><span class="sxs-lookup"><span data-stu-id="055d9-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="055d9-160">Be to, paslaugų aplinka turi būti publikuota prieš tai, kai visi atributų naujinimai įsigalios elektroninių SF išrašymo paslaugai.</span><span class="sxs-lookup"><span data-stu-id="055d9-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="055d9-161">Prijungtos programos</span><span class="sxs-lookup"><span data-stu-id="055d9-161">Connected applications</span></span>

<span data-ttu-id="055d9-162">Susijusios programos yra „Finance and Supply Chain Management“ egzemplioriai, kuriuos jūs galite norėti pasiekti naudodami RCS.</span><span class="sxs-lookup"><span data-stu-id="055d9-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="055d9-163">Be programos URL ir jo nuomininko, susijusioje programoje yra kredencialai, kurie leidžia RCS prisijungti prie aplinkos.</span><span class="sxs-lookup"><span data-stu-id="055d9-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="055d9-164">Naudodami susijusias programas galite konfigūruoti dalį elektroninių SF išrašymo priemonės „Finance and Supply Chain Management“, kad būtų veikia visa elektroninių SF išrašymo priemonė.</span><span class="sxs-lookup"><span data-stu-id="055d9-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="055d9-165">„Finance and Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="055d9-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="055d9-166">Integravimas su elektroninių SF priedu</span><span class="sxs-lookup"><span data-stu-id="055d9-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="055d9-167">Prieš naudojant „Finance and Supply Chain Management“ elektroninėms SF išduoti naudojant elektroninių SF išrašymo priedą, priedas turi būti sukonfigūruotas taip, kad leistų ryšį su tarnyba.</span><span class="sxs-lookup"><span data-stu-id="055d9-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="055d9-168">Elektroninių SF išrašymo priedo funkcijos integravimas</span><span class="sxs-lookup"><span data-stu-id="055d9-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="055d9-169">Norėdami įgalinti „Finance and Supply Chain Management“ ir elektroninio SF išrašymo priedo ryšį, turite įjungti integravimo priemonę **Elektroninio SF išrašymo priedo integravimas** funkciją **Funkcijų valdymas** darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="055d9-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="055d9-170">Paslaugos galinis punktas</span><span class="sxs-lookup"><span data-stu-id="055d9-170">Service endpoint</span></span>

<span data-ttu-id="055d9-171">Paslaugos galinis punktas yra URL, kuriame yra elektroninio SF išrašymo priedas.</span><span class="sxs-lookup"><span data-stu-id="055d9-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="055d9-172">Prieš elektroninių sąskaitų išleidimą, paslaugos galinis taškas turi būti konfigūruotas „Finance and Supply Chain Management“ siekiant leisti komunikaciją su paslaugomis.</span><span class="sxs-lookup"><span data-stu-id="055d9-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="055d9-173">Norėdami konfigūruoti paslaugų galinį tašką, eikite į **Organizacijos administravimas \> Nustatymai \> Elektroninio dokumento parametras** ir tada **Pateikimo tarnybos** skirtukas, laukelyje **Elektroninės sąskaitos priedo URL** laukelis ir įveskite URL kaip aprašyta lentelėje skyriuje **Paslaugos galinis taškas**.</span><span class="sxs-lookup"><span data-stu-id="055d9-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="055d9-174">Aplinkos</span><span class="sxs-lookup"><span data-stu-id="055d9-174">Environments</span></span>

<span data-ttu-id="055d9-175">Aplinkos pavadinimas, įvestas „Finance and Supply Chain Management“ remiasi aplinkos, kuri sukurta RCS ir paskelbta elektroninio SF išrašymo prieduose, pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="055d9-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="055d9-176">Aplinka turi būti konfigūruojama **Pateikimo paslaugų** skirtuke **Elektroninio dokumento parametro** puslapyje taip, kad kiekvienoje užklausoje išduoti elektronines SF būtų aplinka, kur elektroninio SF išrašymo priedas gali nustatyti, kuri elektroninių SF išrašymo funkcija turi apdoroti užklausą.</span><span class="sxs-lookup"><span data-stu-id="055d9-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="055d9-177">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="055d9-177">Additional resources</span></span>

- [<span data-ttu-id="055d9-178">Elektroninių sąskaitų konfigūravimas RCS</span><span class="sxs-lookup"><span data-stu-id="055d9-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="055d9-179">Išduoti elektronines sąskaitas „Finance and Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="055d9-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

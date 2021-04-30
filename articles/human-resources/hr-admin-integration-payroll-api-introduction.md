---
title: Algalapių integravimo API įžanga
description: Šioje temoje aprašomas „Dynamics 365 Human Resources” algalapio integravimo API.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61b90c566325bb8d83b09fceebc721cfb14d3fc8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891131"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="1da82-103">Algalapių integravimo API įžanga</span><span class="sxs-lookup"><span data-stu-id="1da82-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1da82-104">Šiame dokumente aprašomas „Dynamics 365 Human Resources” algalapio integravimo API.</span><span class="sxs-lookup"><span data-stu-id="1da82-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="1da82-105">API įgalina supaprastintą visapusišką integravimą tarp Personalo valdymo ir algalapio sistemų partnerių.</span><span class="sxs-lookup"><span data-stu-id="1da82-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="1da82-106">Integravimo patirtis prasideda Personalo valdymo srityje su darbuotojo profilio, atlyginimo, atskaitymo ir įnašo informacija.</span><span class="sxs-lookup"><span data-stu-id="1da82-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="1da82-107">Kai pasamdote darbuotoją ir įvedate reikiamą profilio bei mokėjimo informaciją į Personalo valdymo sritį, algalapio sistema naudoja šią informaciją algalapio apdorojimui.</span><span class="sxs-lookup"><span data-stu-id="1da82-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="1da82-108">Bet kokie darbuotojo ar mokėjimo informacijos atnaujinimai taip pat yra naudojami vėlesniuose mokėjimo vykdymuose.</span><span class="sxs-lookup"><span data-stu-id="1da82-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Algalapių integravimo srautas](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="1da82-110">Dėl integravimo įgalinimo, Personalo valdyme yra šie komponentai:</span><span class="sxs-lookup"><span data-stu-id="1da82-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="1da82-111">Funkcija pažymėti darbuotoją kaip pasirengusį mokėti</span><span class="sxs-lookup"><span data-stu-id="1da82-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="1da82-112">Integravimo API, atveriantis naujas programų integravimo funkcijas</span><span class="sxs-lookup"><span data-stu-id="1da82-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="1da82-113">„Microsoft Dataverse“</span><span class="sxs-lookup"><span data-stu-id="1da82-113">Microsoft Dataverse</span></span>

<span data-ttu-id="1da82-114">API yra sukurtos „Microsoft Dataverse“ (anksčiau „Common Data Service“).</span><span class="sxs-lookup"><span data-stu-id="1da82-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="1da82-115">Visos RESTful sąveikos su šiuo API yra daromos per „Microsoft Dataverse“ žiniatinklio API, kurios naudoja OData.</span><span class="sxs-lookup"><span data-stu-id="1da82-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="1da82-116">Šis API yra papildomas rinkinys „Dataverse“ žiniatinklio API.</span><span class="sxs-lookup"><span data-stu-id="1da82-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="1da82-117">„Dataverse“ žiniatinklio API nustato savybes, tokias kaip autentifikavimas, SLA, rinkinys, konkurencijos kontrolė ir klaidų tvarkymas.</span><span class="sxs-lookup"><span data-stu-id="1da82-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="1da82-118">Dėl bendresnės informacijos apie „Microsoft Dataverse“ žiniatinklio API, žr.:</span><span class="sxs-lookup"><span data-stu-id="1da82-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="1da82-119">Kas yra „Microsoft Dataverse“?</span><span class="sxs-lookup"><span data-stu-id="1da82-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="1da82-120">Naudokite „Microsoft Dataverse“ žiniatinklio API</span><span class="sxs-lookup"><span data-stu-id="1da82-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="1da82-121">„Microsoft Dataverse“ kūrėjo gairės</span><span class="sxs-lookup"><span data-stu-id="1da82-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="1da82-122">Šiame dokumente pateikiama išsami informacija ir gairės programuotojams, kaip naudoti „Dataverse” žiniatinklio API, įskaitant šias temas:</span><span class="sxs-lookup"><span data-stu-id="1da82-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="1da82-123">„Microsoft Dataverse” autentifikavimas su Žiniatinklio API</span><span class="sxs-lookup"><span data-stu-id="1da82-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="1da82-124">Operacijų atlikimas naudojant Žiniatinklio API</span><span class="sxs-lookup"><span data-stu-id="1da82-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="1da82-125">Paštininko naudojimas su Žiniatinklio API</span><span class="sxs-lookup"><span data-stu-id="1da82-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="1da82-126">Keitimų sekimo naudojimas duomenims su išorinėmis sistemomis sinchronizuoti</span><span class="sxs-lookup"><span data-stu-id="1da82-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="1da82-127">Virtualios lentelės žmogiškiesiems ištekliams „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="1da82-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="1da82-128">Galiniai Algalapio integravimo API punktai naudoja virtualios lentelės platformos galimybes „Microsoft Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="1da82-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="1da82-129">Pagal nutylėjimą, virtualios lentelės ir jų susieti API galiniai punktai nėra diegiami Personalo valdymo aplinkose, taip įgalinant organizacijas nustatyti, kurie „OData” galiniai punktai turi būti rodomi aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="1da82-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="1da82-130">Norėdami naudoti API, virtualios lentelės, skirtos žmogiškųjų išteklių objektams, turi būti sukurtos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="1da82-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="1da82-131">Dėl informacijos apie virtualių lentelių kūrimą API, žr. [Konfigūruoti „Dataverse“ virtualias lenteles](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="1da82-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="1da82-132">Duomenų modelis</span><span class="sxs-lookup"><span data-stu-id="1da82-132">Data model</span></span>

<span data-ttu-id="1da82-133">Tolesnėje diagramoje rodomi santykiai su API.</span><span class="sxs-lookup"><span data-stu-id="1da82-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="1da82-134">Keli tipai turi užsienio raktus su kitais, iš anksto esantys objektai žmogiškuosiuose ištekliuose čia nerodomi.</span><span class="sxs-lookup"><span data-stu-id="1da82-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="1da82-135">Šiame dokumente pateikta informacija apie objektus, kurie yra būdingi algalapio integravimo scenarijams.</span><span class="sxs-lookup"><span data-stu-id="1da82-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="1da82-136">Tačiau yra daugelis kitų Personalo valdymui skirto „Dataverse“ žiniatinklio API objektų, kurie taip pat gali būti svarbūs jūsų integravimui.</span><span class="sxs-lookup"><span data-stu-id="1da82-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="1da82-137">Kai kurie iš šių objektų yra nurodyti išorinių raktų ryšiuose ar naršymo ypatybėse.</span><span class="sxs-lookup"><span data-stu-id="1da82-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Algalapio integravimo API duomenų modelis](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="1da82-139">Algalapio darbuotojas ir susiję objektai</span><span class="sxs-lookup"><span data-stu-id="1da82-139">Payroll employee and related entities</span></span>

<span data-ttu-id="1da82-140">Objektai:</span><span class="sxs-lookup"><span data-stu-id="1da82-140">Entities:</span></span>

- [<span data-ttu-id="1da82-141">Algalapio darbuotojas</span><span class="sxs-lookup"><span data-stu-id="1da82-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="1da82-142">Algalapio darbuotojo adresas</span><span class="sxs-lookup"><span data-stu-id="1da82-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="1da82-143">Algalapio pastoviosios atlyginimo dalies planas</span><span class="sxs-lookup"><span data-stu-id="1da82-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="1da82-144">Algalapių padėties užduotis</span><span class="sxs-lookup"><span data-stu-id="1da82-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="1da82-145">Algalapių padėtis</span><span class="sxs-lookup"><span data-stu-id="1da82-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="1da82-146">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="1da82-146">See also</span></span>

[<span data-ttu-id="1da82-147">Algalapio objektų generavimas ir peržiūra</span><span class="sxs-lookup"><span data-stu-id="1da82-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="1da82-148">Personalo valdymo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1da82-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="1da82-149">Bendrai naudojamų Personalo valdymo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1da82-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="1da82-150">Kas yra „Microsoft Dataverse“?</span><span class="sxs-lookup"><span data-stu-id="1da82-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="1da82-151">Naudokite „Microsoft Dataverse“ žiniatinklio API</span><span class="sxs-lookup"><span data-stu-id="1da82-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
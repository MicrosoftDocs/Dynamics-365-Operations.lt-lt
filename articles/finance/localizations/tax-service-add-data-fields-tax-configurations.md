---
title: Įtraukti duomenų laukus į mokesčių konfigūracijas
description: Šioje temoje paaiškinama, kaip pritaikyti mokesčių konfigūracijas, pridedant duomenų laukus.
author: kailiang
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9d9fce81151ad70d57c69e389e238a6f9137d56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819429"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="8726d-103">Įtraukti duomenų laukus į mokesčių konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="8726d-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="8726d-104">Šioje temoje paaiškinama, kaip pritaikyti mokesčių konfigūracijas [naudojant duomenų laukus, pridėtus prie mokesčių](tax-service-add-data-fields-tax-integration-by-extension.md) integravimo.</span><span class="sxs-lookup"><span data-stu-id="8726d-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="8726d-105">Mokesčių duomenų modelio tinkinimas</span><span class="sxs-lookup"><span data-stu-id="8726d-105">Customize the tax data model</span></span>

1. <span data-ttu-id="8726d-106">„Microsoft Dynamics 365 Finance“, eikite į **Elektroninės ataskaitos** \> **Mokesčių konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="8726d-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="8726d-107">Konfigūracijos medyje pasirinkite **Mokesčių duomenų modelis** - Europa.</span><span class="sxs-lookup"><span data-stu-id="8726d-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="8726d-108">Tada, veiksmų srityje pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="8726d-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="8726d-109">Išplečiamajame dialogo lange pasirinkite apmokestinamo dokumento modelį, išvestą iš pavadinimo: mokesčio duomenų modelis **– Europa, „Microsoft", įveskite naujo mokesčių duomenų modelio pavadinimą, tada pasirinkite** Kurti **konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="8726d-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="8726d-110">Pasirinkite ką tik sukurtą mokesčių duomenų modelį, tada veiksmų srityje pasirinkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="8726d-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="8726d-111">Išplėskite duomenų modelio medį, **pasirinkite** Eilutės, tada pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="8726d-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="8726d-112">Dialogo lange **Kurti mazgą** įveskite pavadinimą, nurodykite prekės tipą, tada pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="8726d-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="8726d-113">Pridėkite būtinus stulpelius.</span><span class="sxs-lookup"><span data-stu-id="8726d-113">Add any required columns.</span></span>
8. <span data-ttu-id="8726d-114">Veiksmų juostoje pasirinkite **Įrašyti** ir tada pasirinkite **Užbaigta**.</span><span class="sxs-lookup"><span data-stu-id="8726d-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="8726d-115">Uždaryti puslapį ir peržiūrėti jūsų mokesčių duomenų modelio užbaigtą versiją.</span><span class="sxs-lookup"><span data-stu-id="8726d-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="8726d-116">Tinkinti mokesčių konfigūravimą</span><span class="sxs-lookup"><span data-stu-id="8726d-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="8726d-117">„Finance“, eikite į **Elektroninės ataskaitos** \> **Mokesčių konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="8726d-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="8726d-118">Konfigūracijos medyje pasirinkite **Mokesčių konfigūravimas** - Europa.</span><span class="sxs-lookup"><span data-stu-id="8726d-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="8726d-119">Tada, veiksmų srityje pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="8726d-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="8726d-120">Išplečiamajame dialogo lange pasirinkite Mokesčių paslaugų konfigūravimą, išvestą iš pavadinimo: mokesčių konfigūravimas **– Europa, „Microsoft", įveskite naujo mokesčių konfigiūravimo pavadinimą, tada pasirinkite** Kurti **konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="8726d-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="8726d-121">Pasirinkite ką tik sukurtą mokesčių konfigūravimą, tada veiksmų srityje pasirinkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="8726d-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="8726d-122">Skyriaus **Ypatybės** lauke **Duomenų modelis** pasirinkite pritaikytą mokesčių duomenų modelį, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="8726d-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="8726d-123">Lauke **Duomenų modelio** versija pasirinkite užbaigtą mokesčių duomenų modelio versiją.</span><span class="sxs-lookup"><span data-stu-id="8726d-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="8726d-124">Pasirinkite **Pridėti** ir pridėkite reikiamus mokesčių priemones.</span><span class="sxs-lookup"><span data-stu-id="8726d-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="8726d-125">Veiksmų juostoje pasirinkite **Įrašyti** ir tada pasirinkite **Užbaigta**.</span><span class="sxs-lookup"><span data-stu-id="8726d-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="8726d-126">Uždaryti puslapį ir peržiūrėti jūsų mokesčių konfigūravimo užbaigtą versiją.</span><span class="sxs-lookup"><span data-stu-id="8726d-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="8726d-127">Įdiegti mokesčių priemones pritaikytame mokesčių konfigūracijoje</span><span class="sxs-lookup"><span data-stu-id="8726d-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="8726d-128">„Regulatory Configuration Service“ (RCS), eikite į **Globalizavimo funkcijos** \> **Mokesčiai**.</span><span class="sxs-lookup"><span data-stu-id="8726d-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="8726d-129">Pasirinkite **Įtraukti**, įveskite informaciją apie naują priemonę, tada pasirinkite **Sukurti** funkciją.</span><span class="sxs-lookup"><span data-stu-id="8726d-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="8726d-130">Skirtuke **Versijos** pasirinkite priemonę, o tada – **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="8726d-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="8726d-131">Konfigūracijos **versijos** lauko skirtuke **Bendra pasirinkite** pritaikytą mokesčių konfigūraciją ir versiją.</span><span class="sxs-lookup"><span data-stu-id="8726d-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="8726d-132">Dialogo lange Stulpelių valdymas pasirinkite antraštę ir eilutės stulpelius, kuriuos norite įtraukti į pritaikytą mokesčių matą, tada pasirinkite rodyklės dešinėn mygtuką, norėdami juos įtraukti į **stulpelių** sąrašą **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="8726d-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>

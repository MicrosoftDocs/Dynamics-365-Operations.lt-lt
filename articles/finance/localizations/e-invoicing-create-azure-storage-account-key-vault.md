---
title: „Azure” saugyklos abonemento ir raktų saugyklos kūrimas
description: Šioje temoje paaiškinama, kaip sukurti „Azure” saugyklos abonementą ir raktų saugyklą.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
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
ms.openlocfilehash: d076aa5230437d1ef90f6b46d49ee4dea526db24
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104234"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="75037-103">„Azure” saugyklos abonemento ir raktų saugyklos kūrimas</span><span class="sxs-lookup"><span data-stu-id="75037-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="75037-104">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="75037-104">Prerequisites</span></span>

<span data-ttu-id="75037-105">Norėdami atlikti šioje temoje esančius veiksmus, turite įsitikinti, kad atliktos toliau nurodytos užduotys.</span><span class="sxs-lookup"><span data-stu-id="75037-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="75037-106">Sukurti raktų saugyklos išteklius „Azure”.</span><span class="sxs-lookup"><span data-stu-id="75037-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="75037-107">Daugiau informacijos žr. [Apie „Azure Key Vault”](https://docs.microsoft.com/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="75037-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="75037-108">Sukurti „Azure” saugyklos abonementą (didelių dvejetainių objektų saugykla).</span><span class="sxs-lookup"><span data-stu-id="75037-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="75037-109">Daugiau informacijos žr. [„Azure” saugyklos abonemento priežiūra](https://docs.microsoft.com/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="75037-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="75037-110">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="75037-110">Overview</span></span>

<span data-ttu-id="75037-111">Šioje temoje galėsite atlikti du toliau pateiktus pagrindinius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="75037-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="75037-112">Nustatyti „Azure” saugyklos abonementą, kad būtų gautas saugyklos abonemento URI.</span><span class="sxs-lookup"><span data-stu-id="75037-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="75037-113">Nustatyti raktų saugyklą, kad būtų saugomas saugyklos abonemento URI.</span><span class="sxs-lookup"><span data-stu-id="75037-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="75037-114">„Azure” saugyklos abonemento nustatymas siekiant gauti saugyklos abonemento URI</span><span class="sxs-lookup"><span data-stu-id="75037-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="75037-115">Atidarykite saugyklos abonementą, kurį planuojate naudoti su elektroninių SF išrašymo priedu.</span><span class="sxs-lookup"><span data-stu-id="75037-115">Open the storage account that you plan to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="75037-116">Eikite į **Didelio dvejetainio objekto paslauga** \> **Konteineriai** ir sukurkite naują konteinerį.</span><span class="sxs-lookup"><span data-stu-id="75037-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="75037-117">Įveskite konteinerio pavadinimą ir nustatykite lauką **Viešosios prieigos lygis** į **Privatus (ne anoniminė prieiga)**.</span><span class="sxs-lookup"><span data-stu-id="75037-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="75037-118">Atidarykite konteinerį ir eikite į **Parametrai \> Prieigos strategija**.</span><span class="sxs-lookup"><span data-stu-id="75037-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="75037-119">Pasirinkite **Įtraukti strategiją**, norėdami įtraukti saugomą prieigos strategiją.</span><span class="sxs-lookup"><span data-stu-id="75037-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="75037-120">Atitinkamai nustatykite laukus **Identifikatorius** ir **Teisės**.</span><span class="sxs-lookup"><span data-stu-id="75037-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="75037-121">Lauke **Teisės** turite pasirinkti visas teises.</span><span class="sxs-lookup"><span data-stu-id="75037-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Didelių dvejetainių objektų saugyklos teisių suteikimas](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="75037-123">Įveskite pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="75037-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="75037-124">Galiojimo data turi būti data ateityje.</span><span class="sxs-lookup"><span data-stu-id="75037-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="75037-125">Pasirinkite **Gerai**, norėdami įrašyti strategiją, tada įrašykite konteinerio keitimus.</span><span class="sxs-lookup"><span data-stu-id="75037-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="75037-126">Grįžkite į saugyklos abonementą ir atidarykite **Saugyklos naršyklė (peržiūra)**.</span><span class="sxs-lookup"><span data-stu-id="75037-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="75037-127">Dešiniuoju pelės klavišu spustelėkite konteinerį ir pasirinkite **Gauti bendrai naudojamą prieigos parašą**.</span><span class="sxs-lookup"><span data-stu-id="75037-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="75037-128">Dialogo lange **Bendrai naudojamas prieigos parašas** kopijuokite ir išsaugokite reikšmę, esančią lauke **URI**.</span><span class="sxs-lookup"><span data-stu-id="75037-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="75037-129">Ši reikšmė bus naudojama kitoje procedūroje ir bus vadinama *bendrai naudojamo prieigos parašo URI*.</span><span class="sxs-lookup"><span data-stu-id="75037-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![URI reikšmės pasirinkimas ir kopijavimas](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="75037-131">Raktų saugyklos nustatymas siekiant saugoti saugyklos abonemento URI</span><span class="sxs-lookup"><span data-stu-id="75037-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="75037-132">Atidarykite raktų saugyklą, kurią planuojate naudoti su elektroninių SF išrašymo priedu.</span><span class="sxs-lookup"><span data-stu-id="75037-132">Open the key vault that you intend to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="75037-133">Norėdami sukurti naują slaptąjį raktą, eikite į **Parametrai** \> **Slaptieji raktai** ir pasirinkite **Generuoti / importuoti**.</span><span class="sxs-lookup"><span data-stu-id="75037-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="75037-134">Puslapio **Sukurti slaptąjį raktą** lauke **Nusiuntimo parinktys** pasirinkite **Rankinis**.</span><span class="sxs-lookup"><span data-stu-id="75037-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="75037-135">Įveskite slaptojo rakto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="75037-135">Enter the name of the secret.</span></span> <span data-ttu-id="75037-136">Šis pavadinimas bus naudojamas paslaugos nustatymo metu „Regulatory Configuration Services” (RCS) ir bus nurodomas kaip *raktų saugyklos slaptojo rakto pavadinimas*.</span><span class="sxs-lookup"><span data-stu-id="75037-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="75037-137">Lauke **Reikšmė** pasirinkite **Bendrai naudojamo prieigos parašo URI** ir tada pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="75037-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="75037-138">Nustatykite prieigos strategiją, kad elektroninių SF išrašymo priedui būtų galima suteikti tinkamą saugios prieigos prie jūsų sukurto slaptojo rakto lygį.</span><span class="sxs-lookup"><span data-stu-id="75037-138">Set up the access policy to grant the Electronic invoicing add-on the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="75037-139">Eikite į **Parametrai \> Prieigos strategija** ir pasirinkite **Įtraukti prieigos strategiją**.</span><span class="sxs-lookup"><span data-stu-id="75037-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="75037-140">Nustatykite operacijų **Gauti** ir **Išvardyti** slaptųjų raktų teises.</span><span class="sxs-lookup"><span data-stu-id="75037-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Paslaugos prieigos suteikimas](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="75037-142">Nustatykite operacijų **Gauti** ir **Išvardyti** sertifikatų teises.</span><span class="sxs-lookup"><span data-stu-id="75037-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Sertifikatų teisių suteikimas](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="75037-144">Dialogo lange **Pagrindas** pasirinkite pagrindą, įtraukdami **Elektroninių SF išrašymo priedas**.</span><span class="sxs-lookup"><span data-stu-id="75037-144">In the **Principal** dialog box, select the principal by adding **Electronic invoicing add-on**.</span></span>
10. <span data-ttu-id="75037-145">Pasirinkite **Įtraukti**, tada pasirinkite **Įrašyti „Key Vault” keitimus**.</span><span class="sxs-lookup"><span data-stu-id="75037-145">Select **Add**, and then select **Save Key Vault changes**.</span></span>
11. <span data-ttu-id="75037-146">Puslapyje **Apžvalga** nukopijuokite raktų saugyklos reikšmę **DNS pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="75037-146">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="75037-147">Ši reikšmė bus naudojama paslaugos nustatymo metu RCS ir bus vadinama *raktų saugyklos URI*.</span><span class="sxs-lookup"><span data-stu-id="75037-147">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>

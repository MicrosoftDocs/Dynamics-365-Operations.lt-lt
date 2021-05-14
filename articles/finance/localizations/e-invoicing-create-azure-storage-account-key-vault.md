---
title: „Azure” saugyklos abonemento ir raktų saugyklos kūrimas
description: Šioje temoje paaiškinama, kaip sukurti „Azure” saugyklos abonementą ir raktų saugyklą.
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
ms.openlocfilehash: 5c2ddad10f9cbedd77a04fe0f42bdc217fd43344
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963244"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="5bcba-103">„Azure” saugyklos abonemento ir raktų saugyklos kūrimas</span><span class="sxs-lookup"><span data-stu-id="5bcba-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="5bcba-104">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="5bcba-104">Prerequisites</span></span>

<span data-ttu-id="5bcba-105">Norėdami atlikti šioje temoje esančius veiksmus, turite įsitikinti, kad atliktos toliau nurodytos užduotys.</span><span class="sxs-lookup"><span data-stu-id="5bcba-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="5bcba-106">Sukurti raktų saugyklos išteklius „Azure”.</span><span class="sxs-lookup"><span data-stu-id="5bcba-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="5bcba-107">Daugiau informacijos žr. [Apie „Azure Key Vault”](/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="5bcba-107">For more information, see [About Azure Key Vault](/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="5bcba-108">Sukurti „Azure” saugyklos abonementą (didelių dvejetainių objektų saugykla).</span><span class="sxs-lookup"><span data-stu-id="5bcba-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="5bcba-109">Daugiau informacijos žr. [„Azure” saugyklos abonemento priežiūra](/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="5bcba-109">For more information, see [Maintaining Azure Storage Account](/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="5bcba-110">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="5bcba-110">Overview</span></span>

<span data-ttu-id="5bcba-111">Šioje temoje galėsite atlikti du toliau pateiktus pagrindinius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5bcba-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="5bcba-112">Nustatyti „Azure” saugyklos abonementą, kad būtų gautas saugyklos abonemento URI.</span><span class="sxs-lookup"><span data-stu-id="5bcba-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="5bcba-113">Nustatyti raktų saugyklą, kad būtų saugomas saugyklos abonemento URI.</span><span class="sxs-lookup"><span data-stu-id="5bcba-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="5bcba-114">„Azure” saugyklos abonemento nustatymas siekiant gauti saugyklos abonemento URI</span><span class="sxs-lookup"><span data-stu-id="5bcba-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="5bcba-115">Atidarykite saugyklos abonementą, kurį planuojate naudoti su elektroninių SF išrašymo priedu.</span><span class="sxs-lookup"><span data-stu-id="5bcba-115">Open the storage account that you plan to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="5bcba-116">Eikite į **Didelio dvejetainio objekto paslauga** \> **Konteineriai** ir sukurkite naują konteinerį.</span><span class="sxs-lookup"><span data-stu-id="5bcba-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="5bcba-117">Įveskite konteinerio pavadinimą ir nustatykite lauką **Viešosios prieigos lygis** į **Privatus (ne anoniminė prieiga)**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="5bcba-118">Atidarykite konteinerį ir eikite į **Parametrai \> Prieigos strategija**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="5bcba-119">Pasirinkite **Įtraukti strategiją**, norėdami įtraukti saugomą prieigos strategiją.</span><span class="sxs-lookup"><span data-stu-id="5bcba-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="5bcba-120">Atitinkamai nustatykite laukus **Identifikatorius** ir **Teisės**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="5bcba-121">Lauke **Teisės** turite pasirinkti visas teises.</span><span class="sxs-lookup"><span data-stu-id="5bcba-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Didelių dvejetainių objektų saugyklos teisių suteikimas](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="5bcba-123">Įveskite pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="5bcba-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="5bcba-124">Galiojimo data turi būti data ateityje.</span><span class="sxs-lookup"><span data-stu-id="5bcba-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="5bcba-125">Pasirinkite **Gerai**, norėdami įrašyti strategiją, tada įrašykite konteinerio keitimus.</span><span class="sxs-lookup"><span data-stu-id="5bcba-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="5bcba-126">Grįžkite į saugyklos abonementą ir atidarykite **Saugyklos naršyklė (peržiūra)**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="5bcba-127">Dešiniuoju pelės klavišu spustelėkite konteinerį ir pasirinkite **Gauti bendrai naudojamą prieigos parašą**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="5bcba-128">Dialogo lange **Bendrai naudojamas prieigos parašas** kopijuokite ir išsaugokite reikšmę, esančią lauke **URI**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="5bcba-129">Ši reikšmė bus naudojama kitoje procedūroje ir bus vadinama *bendrai naudojamo prieigos parašo URI*.</span><span class="sxs-lookup"><span data-stu-id="5bcba-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![URI reikšmės pasirinkimas ir kopijavimas](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="5bcba-131">Raktų saugyklos nustatymas siekiant saugoti saugyklos abonemento URI</span><span class="sxs-lookup"><span data-stu-id="5bcba-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="5bcba-132">Atidarykite raktų saugyklą, kurią planuojate naudoti su elektroninių SF išrašymo priedu.</span><span class="sxs-lookup"><span data-stu-id="5bcba-132">Open the key vault that you intend to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="5bcba-133">Norėdami sukurti naują slaptąjį raktą, eikite į **Parametrai** \> **Slaptieji raktai** ir pasirinkite **Generuoti / importuoti**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="5bcba-134">Puslapio **Sukurti slaptąjį raktą** lauke **Nusiuntimo parinktys** pasirinkite **Rankinis**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="5bcba-135">Įveskite slaptojo rakto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5bcba-135">Enter the name of the secret.</span></span> <span data-ttu-id="5bcba-136">Šis pavadinimas bus naudojamas paslaugos nustatymo metu „Regulatory Configuration Services” (RCS) ir bus nurodomas kaip *raktų saugyklos slaptojo rakto pavadinimas*.</span><span class="sxs-lookup"><span data-stu-id="5bcba-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="5bcba-137">Lauke **Reikšmė** pasirinkite **Bendrai naudojamo prieigos parašo URI** ir tada pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="5bcba-138">Nustatykite prieigos strategiją, kad elektroninių SF išrašymo priedui būtų galima suteikti tinkamą saugios prieigos prie jūsų sukurto slaptojo rakto lygį.</span><span class="sxs-lookup"><span data-stu-id="5bcba-138">Set up the access policy to grant Electronic invoicing the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="5bcba-139">Eikite į **Parametrai \> Prieigos strategija** ir pasirinkite **Įtraukti prieigos strategiją**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="5bcba-140">Nustatykite operacijų **Gauti** ir **Išvardyti** slaptųjų raktų teises.</span><span class="sxs-lookup"><span data-stu-id="5bcba-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Paslaugos prieigos suteikimas](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="5bcba-142">Nustatykite operacijų **Gauti** ir **Išvardyti** sertifikatų teises.</span><span class="sxs-lookup"><span data-stu-id="5bcba-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Sertifikatų teisių suteikimas](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="5bcba-144">Laukelyje **Pasirinkti pagrindą** pasirinkite **Nieko nepasirinkta**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="5bcba-145">Dialogo lange **Pagrindas** pasirinkite pagrindą, įtraukdami **El. SF išrašymo paslaugą**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="5bcba-146">Pasirinkite **Įtraukti**, tada pasirinkite **Įrašyti „Key Vault” keitimus**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="5bcba-147">Puslapyje **Apžvalga** nukopijuokite raktų saugyklos reikšmę **DNS pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="5bcba-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="5bcba-148">Ši reikšmė bus naudojama paslaugos nustatymo metu RCS ir bus vadinama *raktų saugyklos URI*.</span><span class="sxs-lookup"><span data-stu-id="5bcba-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>

> [!NOTE]
> <span data-ttu-id="5bcba-149">Norėdami gauti papildomos saugojimo sąskaitos saugos, sukonfigūruokite „Azure Defender for Storage".</span><span class="sxs-lookup"><span data-stu-id="5bcba-149">For additional security on the storage account, configure the Azure Defender for Storage.</span></span>
> 
> <span data-ttu-id="5bcba-150">Daugiau informacijos rasite [Įžanga į „Azure Defender for Storage“](/azure/security-center/defender-for-storage-introduction).</span><span class="sxs-lookup"><span data-stu-id="5bcba-150">For more information, see [Introduction to Azure Defender for Storage](/azure/security-center/defender-for-storage-introduction).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

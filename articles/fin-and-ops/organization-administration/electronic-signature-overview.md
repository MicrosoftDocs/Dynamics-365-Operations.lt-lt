---
title: "Elektroninio parašo apžvalga"
description: "Šiame straipsnyje apžvelgiami elektroniniai parašai ir aprašoma, kaip juos naudoti programoje „Microsoft Dynamics 365 for Finance and Operations“."
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e81d4a29cf1624619c1f0c2bfc6bc66c715a6b7f
ms.openlocfilehash: fa3aff17f3f55cdee9abf1f0326ac2bbe599bf94
ms.contentlocale: lt-lt
ms.lasthandoff: 08/24/2017

---

# <a name="electronic-signature-overview"></a><span data-ttu-id="85079-103">Elektroninio parašo apžvalga</span><span class="sxs-lookup"><span data-stu-id="85079-103">Electronic signature overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="85079-104">Šiame straipsnyje apžvelgiami elektroniniai parašai ir aprašoma, kaip juos naudoti programoje „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="85079-104">This article provides an overview of electronic signatures and describes how they can be used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-an-electronic-signature"></a><span data-ttu-id="85079-105">Kas yra elektroninis parašas?</span><span class="sxs-lookup"><span data-stu-id="85079-105">What is an electronic signature?</span></span>
--------------------------------

<span data-ttu-id="85079-106">Elektroninis parašas patvirtina asmens, kuris ketina pradėti ar patvirtinti skaičiavimo procesą, tapatybę.</span><span class="sxs-lookup"><span data-stu-id="85079-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="85079-107">Kai kuriose pramonės šakose elektroninis parašas turi tokią pat teisinę galią kaip parašas ranka.</span><span class="sxs-lookup"><span data-stu-id="85079-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> 

<span data-ttu-id="85079-108">Elektroniniai parašai yra reglamentus atitinkantis reikalavimas kai kurioms reguliuojamoms pramonės šakoms, pvz., vaistų, maisto ir gėrimų, aviacijos ir gynybos.</span><span class="sxs-lookup"><span data-stu-id="85079-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="85079-109">Jie taip pat būtini siekiant vykdyti JAV Maisto ir vaistų administracijos (FDA) 21 CFR 11 dalies nuostatas.</span><span class="sxs-lookup"><span data-stu-id="85079-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span> 

<span data-ttu-id="85079-110">**Pastaba.** Elektroninis parašas nėra tas pat, kas skaitmeninis parašas.</span><span class="sxs-lookup"><span data-stu-id="85079-110">**Note:** An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="85079-111">Elektroninis parašas yra tiesiog pasirašymo ranka pakaitas, o skaitmeninis parašas suteikia papildomų saugos priemonių.</span><span class="sxs-lookup"><span data-stu-id="85079-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="85079-112">Skaitmeninis parašas gali padėti nustatyti, ar kitas vartotojas arba procesas mėgino piktavališkai pakeisti duomenis.</span><span class="sxs-lookup"><span data-stu-id="85079-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="85079-113">Skaitmeninį parašą taip pat galima patikrinti, o šio tikrinimo negali paneigti sertifikato, kuris buvo naudojamas pasirašyti duomenis, savininkas.</span><span class="sxs-lookup"><span data-stu-id="85079-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="85079-114">Kaip aprašyta toliau, elektroniniuose „Microsoft Dynamics 365 for Finance and Operations“ parašuose yra įdiegtos skaitmeninio parašo funkcijos.</span><span class="sxs-lookup"><span data-stu-id="85079-114">As described below, electronic signatures in Microsoft Dynamics 365 for Finance and Operations have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="85079-115">Elektroniniai parašai programoje „Dynamics 365 for Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="85079-115">Electronic signatures in Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="85079-116">Programoje „Finance and Operations“ galite naudoti elektroninius parašus svarbiems verslo procesams.</span><span class="sxs-lookup"><span data-stu-id="85079-116">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="85079-117">Kai kuriuose procesuose yra įdiegtos elektroninio parašo galimybės.</span><span class="sxs-lookup"><span data-stu-id="85079-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="85079-118">Taip pat galite sukurti pasirinktinius parašo reikalavimus bet kuriai duomenų bazės lentelei ir laukui.</span><span class="sxs-lookup"><span data-stu-id="85079-118">You can also create custom signature requirements for any database table and field.</span></span> 

<span data-ttu-id="85079-119">Elektroniniuose parašuose yra įdiegtos skaitmeninio parašo funkcijos.</span><span class="sxs-lookup"><span data-stu-id="85079-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="85079-120">Kiekvienas dokumentus pasirašantis vartotojas turi įsigyti galiojantį kriptografijos sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="85079-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="85079-121">Pasirašant dokumentą patikrinamas su tuo sertifikatu susietas privatusis raktas.</span><span class="sxs-lookup"><span data-stu-id="85079-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="85079-122">„Finance and Operations” įrašo elektroninio parašo informaciją į žurnalą, kad būtų galima sekti įrašą.</span><span class="sxs-lookup"><span data-stu-id="85079-122">Finance and Operations records electronic signature information in a log to provide an audit trail.</span></span> <span data-ttu-id="85079-123">Norėdami nustatyti elektroninius parašus, žr. dalį [Elektroninių parašų nustatymas (užduočių vedlys)](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-up-electronic-signatures).</span><span class="sxs-lookup"><span data-stu-id="85079-123">To set up electronic signatures, see [Set up electronic signatures (Task guide)](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-up-electronic-signatures).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="85079-124">Vartotojai, kuriems reikia prieigos prie elektroninių parašų</span><span class="sxs-lookup"><span data-stu-id="85079-124">Users who require access to electronic signatures</span></span>
<span data-ttu-id="85079-125">Trijų tipų vartotojams paprastai reikia saugumo prieigos prie elektroninių parašų: elektroninio parašo administratoriams, pasirašantiems ir elektroninio parašo auditoriams.</span><span class="sxs-lookup"><span data-stu-id="85079-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="85079-126">Elektroninio parašo administratorius</span><span class="sxs-lookup"><span data-stu-id="85079-126">Electronic signature administrator</span></span>

<span data-ttu-id="85079-127">Elektroninio parašo administratorius nustato parašo reikalavimus, bendruosius parametrus, tvirtintojus ir gauna įspėjimus, kai parašų patikrinti nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="85079-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="85079-128">Pagal numatytuosius nustatymus, vartotojas, kuris priklauso saugos vaidmeniui **Informacinių technologijų vadovas**, turi teisę administruoti elektroninius parašus.</span><span class="sxs-lookup"><span data-stu-id="85079-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="85079-129">Pasirašantysis</span><span class="sxs-lookup"><span data-stu-id="85079-129">Signer</span></span>

<span data-ttu-id="85079-130">Pasirašantysis elektroniniu būdu pasirašo dokumentus ir procesus, kuriems reikalingi parašai.</span><span class="sxs-lookup"><span data-stu-id="85079-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="85079-131">Pagal numatytuosius nustatymus, vartotojas, kuris priklauso **Sistemos vartotojas** saugos vaidmeniui, turi teisę pasirašyti dokumentus elektroniniu būdu.</span><span class="sxs-lookup"><span data-stu-id="85079-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span> 

<span data-ttu-id="85079-132">**Pastaba.** Pasirašančiajam gali reikėti papildomų teisių norint pasiekti duomenis, susijusius su pasirašomu dokumentu arba procesu.</span><span class="sxs-lookup"><span data-stu-id="85079-132">**Note:** The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="85079-133">Vartotojas, kuris pakeičia duomenis ir turi pasirašyti tuos pakeitimus, turi turėti teisę keisti duomenis.</span><span class="sxs-lookup"><span data-stu-id="85079-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="85079-134">Vartotojas, kuris pasirašo kito vartotojo vardu, negali reikalauti prieigos prie duomenų.</span><span class="sxs-lookup"><span data-stu-id="85079-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="85079-135">Tokios rūšies vartotojo pavyzdys yra vadovas, kuris pasirašo darbuotojo pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="85079-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="85079-136">Elektroninio parašo auditorius</span><span class="sxs-lookup"><span data-stu-id="85079-136">Electronic signature auditor</span></span>

<span data-ttu-id="85079-137">Elektroninio parašo auditorius peržiūri duomenų bazės žurnalą ir parašų peržiūros žurnalą, esantį duomenų bazės žurnale.</span><span class="sxs-lookup"><span data-stu-id="85079-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="85079-138">Pagal numatytuosius nustatymus, vartotojas, kuris priklauso saugos vaidmeniui **Informacinių technologijų vadovas**, turi teisę audituoti elektroninius parašus.</span><span class="sxs-lookup"><span data-stu-id="85079-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span> 

<span data-ttu-id="85079-139">Jei naudojate ne vaidmenį **Informacinių technologijų vadovas**, įsitikinkite, kad vaidmeniui priskiriamos nurodytos teisės:</span><span class="sxs-lookup"><span data-stu-id="85079-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

-   <span data-ttu-id="85079-140">Peržiūrėti elektroninio parašo triktis</span><span class="sxs-lookup"><span data-stu-id="85079-140">View electronic signature failures</span></span>
-   <span data-ttu-id="85079-141">Peržiūrėti duomenų bazės žurnalą</span><span class="sxs-lookup"><span data-stu-id="85079-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="85079-142">Dokumentų pasirašymas elektroniniu būdu</span><span class="sxs-lookup"><span data-stu-id="85079-142">Signing documents electronically</span></span>
### <a name="get-a-certificate"></a><span data-ttu-id="85079-143">Sertifikato gavimas</span><span class="sxs-lookup"><span data-stu-id="85079-143">Get a certificate</span></span>

<span data-ttu-id="85079-144">Prieš pasirašydami dokumentus elektroniniu būdu programoje „Finance and Operations”, turite prašyti sertifikato.</span><span class="sxs-lookup"><span data-stu-id="85079-144">Before you sign documents electronically in Finance and Operations, you must request a certificate.</span></span> 

<span data-ttu-id="85079-145">**Pastaba.** Sertifikatams kurti ir elektroniniam pasirašymui įgalinti programa „Finance and Operations” naudoja „Microsoft“ SQL serverio funkcijas.</span><span class="sxs-lookup"><span data-stu-id="85079-145">**Note:** Finance and Operations uses Microsoft SQL Server features to create certificates and enable electronic signing.</span></span> <span data-ttu-id="85079-146">Nereikia jokio papildomo sertifikato arba viešųjų raktų sistemos infrastruktūros (PKI).</span><span class="sxs-lookup"><span data-stu-id="85079-146">No additional certificate or public key infrastructure (PKI) is required.</span></span> 

<span data-ttu-id="85079-147">Kai prašote sertifikato, programos „Finance and Operations” duomenų bazėje jums sukuriamas viešasis raktas ir privatusis raktas.</span><span class="sxs-lookup"><span data-stu-id="85079-147">When you request a certificate, a public key and a private key are created for you in the Finance and Operations database.</span></span> <span data-ttu-id="85079-148">Privatusis raktas šifruojamas naudojant tik jums žinomą slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="85079-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="85079-149">Kai dokumentą pasirašote elektroniniu būdu, jūsų tapatybė patikrinama įvedant slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="85079-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span> 

<span data-ttu-id="85079-150">Norėdami prašyti sertifikato, puslapio **Parinktys** skirtuke **Sąskaitos** spustelėkite **Gauti sertifikatą**.</span><span class="sxs-lookup"><span data-stu-id="85079-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span> 

<span data-ttu-id="85079-151">Turite įvesti ir patvirtinti slaptažodį, kurį naudosite pasirašydami.</span><span class="sxs-lookup"><span data-stu-id="85079-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="85079-152">Slaptažodis naudojamas apsaugoti jūsų privatųjį raktą ir leisti naudoti jūsų sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="85079-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="85079-153">Šis slaptažodis nesaugomas duomenų bazėje, jo negali žinoti niekas kitas, net „Finance and Operations” administratorius.</span><span class="sxs-lookup"><span data-stu-id="85079-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the Finance and Operations administrator.</span></span> 

<span data-ttu-id="85079-154">Jeigu pamiršote su savo sertifikatu susietą slaptažodį, sertifikatą reikia atkurti.</span><span class="sxs-lookup"><span data-stu-id="85079-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="85079-155">Sertifikato nustatymas iš naujo neturi įtakos dokumentams, kuriuos pasirašėte naudodami ankstesnį sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="85079-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="85079-156">Norėdami iš naujo nustatyti sertifikatą, puslapyje **Parinktys** spustelėkite **Nustatyti iš naujo sertifikatą**.</span><span class="sxs-lookup"><span data-stu-id="85079-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="85079-157">Dokumento pasirašymas elektroniniu būdu</span><span class="sxs-lookup"><span data-stu-id="85079-157">Sign a document electronically</span></span>

<span data-ttu-id="85079-158">Puslapis **Dokumento pasirašymas** rodomas, kai atliekate keitimą, kuriam reikalingas elektroninis parašas.</span><span class="sxs-lookup"><span data-stu-id="85079-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1.  <span data-ttu-id="85079-159">Puslapyje **Dokumento pasirašymas** spustelėkite skirtuką **Dokumentas**, norėdami peržiūrėti dokumento keitimus.</span><span class="sxs-lookup"><span data-stu-id="85079-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2.  <span data-ttu-id="85079-160">Skirtuke **Parašas** pasirinkite priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="85079-160">On the **Signature** tab, select a reason code.</span></span>
3.  <span data-ttu-id="85079-161">Įveskite komentarą, jei komentaras yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="85079-161">Enter a comment, if a comment is required.</span></span>
4.  <span data-ttu-id="85079-162">Jeigu jūsų vartotojo ID nerodomas lauke **Pasirašantysis**, pasirinkite jį iš sąrašo.</span><span class="sxs-lookup"><span data-stu-id="85079-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5.  <span data-ttu-id="85079-163">Įveskite savo buvimo vietą, jei ši informacija yra reikalinga.</span><span class="sxs-lookup"><span data-stu-id="85079-163">Enter your location, if this information is required.</span></span>
6.  <span data-ttu-id="85079-164">Spustelėkite **GERAI**.</span><span class="sxs-lookup"><span data-stu-id="85079-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="85079-165">Kito vartotojo atliktų keitimų pasirašymas</span><span class="sxs-lookup"><span data-stu-id="85079-165">Sign for another user's changes</span></span>

<span data-ttu-id="85079-166">Kartais galite norėti, kad vartotojas pasirašytų už kito vartotojo keitimus.</span><span class="sxs-lookup"><span data-stu-id="85079-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="85079-167">Pavyzdžiui, darbuotojo atliktus komplektavimo specifikacijos (KS) keitimus gali reikėti pasirašyti vadovui.</span><span class="sxs-lookup"><span data-stu-id="85079-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="85079-168">Taikykite šią procedūrą norėdami „Finance and Operations” vartotoją paskirti pasirašyti už kitą vartotoją.</span><span class="sxs-lookup"><span data-stu-id="85079-168">Use this procedure to designate a Finance and Operations user as a signer for another user.</span></span> 

<span data-ttu-id="85079-169">**Pastaba.** Kai vartotojas pasirašo už kito vartotojo keitimą, parašas turi būti pateiktas keitimą atlikusio vartotojo darbo vietoje.</span><span class="sxs-lookup"><span data-stu-id="85079-169">**Note:** When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="85079-170">Vartotojas negalės įrašyti keitimo, kol nebus pasirašyta.</span><span class="sxs-lookup"><span data-stu-id="85079-170">The user can't save the change until the signature has been provided.</span></span> 

<span data-ttu-id="85079-171">Norėdami paskirti tvirtintojus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="85079-171">To designate approvers, follow these steps.</span></span>

1.  <span data-ttu-id="85079-172">Puslapio **Parinktys** skirtuke **Sąskaitos** spustelėkite **Paskirti tvirtintoją**.</span><span class="sxs-lookup"><span data-stu-id="85079-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2.  <span data-ttu-id="85079-173">Lauke **Tvirtintojo vartotojo ID** pasirinkite vartotojo, kuris turi pasirašyti kito vartotojo keitimus, ID.</span><span class="sxs-lookup"><span data-stu-id="85079-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3.  <span data-ttu-id="85079-174">Lauke **Vartotojo, už kurį pasirašoma, ID** pasirinkite vartotojo, kurio keitimai turi būti pasirašyti, ID.</span><span class="sxs-lookup"><span data-stu-id="85079-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>






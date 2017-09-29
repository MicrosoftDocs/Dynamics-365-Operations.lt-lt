---
title: "Teigiamų mokėjimų failų nustatymas ir generavimas"
description: "Šiame straipsnyje paaiškinama, kaip nustatyti teigiamą mokėjimą ir generuoti teigiamo mokėjimo failus."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8294eb2861f48402c8489b84cc5f139408a22262
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="6697a-103">Teigiamų mokėjimų failų nustatymas ir generavimas</span><span class="sxs-lookup"><span data-stu-id="6697a-103">Set up and generate positive pay files</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6697a-104">Šiame straipsnyje paaiškinama, kaip nustatyti teigiamą mokėjimą ir generuoti teigiamo mokėjimo failus.</span><span class="sxs-lookup"><span data-stu-id="6697a-104">This article explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="6697a-105">Nustatykite teigiamą mokėjimą, jei norite generuoti bankui teikiamą elektroninį čekių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="6697a-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="6697a-106">Tada, kai čekis pateikiamas bankui, bankas jį lygina su čekių sąrašu.</span><span class="sxs-lookup"><span data-stu-id="6697a-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="6697a-107">Jei čekis atitinka sąraše esantįjį, bankas jį patvirtina.</span><span class="sxs-lookup"><span data-stu-id="6697a-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="6697a-108">Jei čekis sąraše esančio čekio neatitinka, bankas jį pasilieka peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="6697a-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="6697a-109">Teigiamų mokėjimų failų sauga</span><span class="sxs-lookup"><span data-stu-id="6697a-109">Security for positive pay files</span></span>
<span data-ttu-id="6697a-110">Teigiamo mokėjimo failuose gali būti neskelbtinos informacijos apie mokėjimų gavėjus ir čekių sumas.</span><span class="sxs-lookup"><span data-stu-id="6697a-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="6697a-111">Todėl būtinai naudokite reikiamas saugos priemones nuo failų sugeneravimo akimirkos iki jų gavimo banke.</span><span class="sxs-lookup"><span data-stu-id="6697a-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="6697a-112">Teigiamų mokėjimų failai atsiunčiami į vietą, kurią nurodo jūsų žiniatinklio naršyklė.</span><span class="sxs-lookup"><span data-stu-id="6697a-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="6697a-113">Kadangi teigiamų mokėjimų failuose gali būti slaptos informacijos, svarbu, kad „Microsoft Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidime šios informacijos generavimo ir peržiūros prieigą turėtų tik įgaliotieji vartotojai.</span><span class="sxs-lookup"><span data-stu-id="6697a-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="6697a-114">Tolesnė lentelė jums padės nustatyti reikiamas teises.</span><span class="sxs-lookup"><span data-stu-id="6697a-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6697a-115">Užduotis</span><span class="sxs-lookup"><span data-stu-id="6697a-115">Task</span></span></th>
<th><span data-ttu-id="6697a-116">Privilegija</span><span class="sxs-lookup"><span data-stu-id="6697a-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6697a-117">Generuoti teigiamų mokėjimų failus iš sąrašo puslapio <strong>Banko sąskaitos</strong> arba puslapio <strong>Banko sąskaitos</strong>.</span><span class="sxs-lookup"><span data-stu-id="6697a-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="6697a-118"><strong>Tvarkyti banko teigiamų mokėjimų informaciją</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="6697a-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="6697a-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="6697a-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6697a-120">Generuoti kelių juridinių subjektų ir banko sąskaitų teigiamų mokėjimų failus iš puslapio <strong>Generuoti teigiamo mokėjimo failą</strong>.</span><span class="sxs-lookup"><span data-stu-id="6697a-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="6697a-121"><strong>Tvarkyti banko teigiamų mokėjimų informaciją</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="6697a-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="6697a-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="6697a-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6697a-123">Peržiūrėti teigiamų mokėjimų failus puslapyje <strong>Teigiamų mokėjimų failų suvestinė</strong>.</span><span class="sxs-lookup"><span data-stu-id="6697a-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="6697a-124"><strong>Peržiūrėti banko teigiamų mokėjimų informaciją keliems juridiniams subjektams</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="6697a-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6697a-125">Patvirtinti banko teigiamo mokėjimo failą puslapyje <strong>Teigiamų mokėjimų failų suvestinė</strong>.</span><span class="sxs-lookup"><span data-stu-id="6697a-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="6697a-126"><strong>Patvirtinti teigiamo mokėjimo failą</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="6697a-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6697a-127">Atšaukti banko teigiamo mokėjimo failą puslapyje <strong>Teigiamų mokėjimų failų suvestinė</strong>.</span><span class="sxs-lookup"><span data-stu-id="6697a-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="6697a-128"><strong>Atšaukti teigiamo mokėjimo failą</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="6697a-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="6697a-129">Teigiamo mokėjimo formato nustatymas</span><span class="sxs-lookup"><span data-stu-id="6697a-129">Set up a positive pay format</span></span>
<span data-ttu-id="6697a-130">Teigiamo mokėjimo failai kuriami naudojant duomenų objektus.</span><span class="sxs-lookup"><span data-stu-id="6697a-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="6697a-131">Negalėsite generuoti teigiamo mokėjimo failo, kol nenustatysite transformacijos įvesties duomenų formato, kuris bus naudojamas čekio informacijai paversti į formatą, galintį bendrauti su banku.</span><span class="sxs-lookup"><span data-stu-id="6697a-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="6697a-132">Puslapyje **Teigiamo mokėjimo formatas** galite sukurti failo formato identifikatorių ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="6697a-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="6697a-133">Transformacijos įvesties duomenų formato tipas turi būti XML.</span><span class="sxs-lookup"><span data-stu-id="6697a-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="6697a-134">Konkretus formatas priklauso nuo jūsų naudojamo transformavimo failo.</span><span class="sxs-lookup"><span data-stu-id="6697a-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="6697a-135">Pvz., pateiktame išplėstinės stiliaus aprašų kalbos transformacijų (XSLT) failo pavyzdyje naudojamas formatas **XML elementas**.</span><span class="sxs-lookup"><span data-stu-id="6697a-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="6697a-136">Naudodami veiksmą **Nusiųsti failą, naudotą transformacijai atlikti**, galite nurodyti jūsų banko reikalaujamo formato transformavimo failo vietą.</span><span class="sxs-lookup"><span data-stu-id="6697a-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="6697a-137">Pavyzdys: teigiamo mokėjimo failo XSLT failas</span><span class="sxs-lookup"><span data-stu-id="6697a-137">Example: XSLT file for positive pay file</span></span>
    <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
      <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
      <xsl:template match="/">
        <xsl:value-of select="'
    '" />
        <Document>
          <xsl:value-of select="'
    '" />
          <!--Header Begin-->
          <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
          <xsl:value-of select="'
    '" />
          <!--Header End-->
          <xsl:for-each select="Document/BankPositivePayExportEntity">
            <!--Cheque Detail begin-->
            <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
                <xsl:value-of select='string("Yes")'/>
              </xsl:when>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
                <xsl:value-of select='string("No")'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='string(" ")'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("Payment")'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='CHEQUENUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='AMOUNTCUR/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("BOA-#1812")'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
                <xsl:value-of select='VENDGROUP/text()'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='CUSTGROUP/text()'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="'
    '" />
          </xsl:for-each>
        </Document>
      </xsl:template>
    </xsl:stylesheet>

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="6697a-138">Teigiamo mokėjimo formato priskyrimas banko sąskaitai</span><span class="sxs-lookup"><span data-stu-id="6697a-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="6697a-139">Kiekvienai banko sąskaitai, kuriai norite generuoti teigiamo mokėjimo informaciją, turite priskirti teigiamo mokėjimo formatą, kurį nurodėte ankstesnėje dalyje.</span><span class="sxs-lookup"><span data-stu-id="6697a-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="6697a-140">Puslapyje **Banko sąskaitos** pasirinkite teigiamo mokėjimo formatą, kuris atitinka banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="6697a-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="6697a-141">Lauke **Teigiamo mokėjimo pradžios data** įveskite pirmąją teigiamo mokėjimo failų generavimo datą.</span><span class="sxs-lookup"><span data-stu-id="6697a-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="6697a-142">Svarbu šiame lauke įvesti datą.</span><span class="sxs-lookup"><span data-stu-id="6697a-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="6697a-143">Priešingu atveju pirmasis jūsų sugeneruotas teigiamo mokėjimo failas apims visus kada nors sukurtus šios banko sąskaitos čekius.</span><span class="sxs-lookup"><span data-stu-id="6697a-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="6697a-144">Teigiamo mokėjimo failų numeracijos priskyrimas</span><span class="sxs-lookup"><span data-stu-id="6697a-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="6697a-145">Kiekvienas teigiamo mokėjimo failas turi turėti unikalų numerį.</span><span class="sxs-lookup"><span data-stu-id="6697a-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="6697a-146">Norėdami sukurti teigiamo mokėjimo failų numeraciją, naudokite skirtuką **Numeracijos**, esantį puslapyje **Grynųjų pinigų ir banko valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6697a-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="6697a-147">Vienos banko sąskaitos teigiamo mokėjimo failo generavimas</span><span class="sxs-lookup"><span data-stu-id="6697a-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="6697a-148">Galite generuoti teigiamo mokėjimo failą vienam juridiniam subjektui ir vienai banko sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="6697a-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="6697a-149">Informacijos apie tai, kaip generuoti teigiamo mokėjimo failus keletui juridinių subjektų ir banko sąskaitų vienu metu, rasite kitame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="6697a-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="6697a-150">Norėdami generuoti vieno juridinio subjekto ir vienos banko sąskaitos teigiamo mokėjimo failą, iš puslapio **Banko sąskaitos** atidarykite dialogo langą **Generuoti teigiamo mokėjimo failą**.</span><span class="sxs-lookup"><span data-stu-id="6697a-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="6697a-151">Lauke **Nutraukimo data** įveskite paskutinę čekio datą, kurią norite įtraukti į teigiamo mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="6697a-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="6697a-152">Visi čekiai, kurie nebuvo įtraukti į teigiamo mokėjimo failą iki šios čekio datos, įtraukiami į failą.</span><span class="sxs-lookup"><span data-stu-id="6697a-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="6697a-153">Kelių banko sąskaitų teigiamo mokėjimo failo generavimas</span><span class="sxs-lookup"><span data-stu-id="6697a-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="6697a-154">Norėdami generuoti kelių banko sąskaitų teigiamo mokėjimo failą, naudokite periodinę užduotį **Generuoti teigiamo mokėjimo failą**.</span><span class="sxs-lookup"><span data-stu-id="6697a-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="6697a-155">Pasirinkite failo teigiamo mokėjimo formatą ir nurodykite, ar failą norite generuoti visiems juridiniams subjektams, ar pasirinktam juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="6697a-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="6697a-156">Teigiamo mokėjimo failą taip pat galite generuoti visoms banko sąskaitoms, kurios naudoja nurodytą teigiamo mokėjimo formatą, arba atskirai banko sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="6697a-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="6697a-157">Lauke **Nutraukimo data** įveskite paskutinę čekio datą, kurią norite įtraukti į teigiamo mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="6697a-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="6697a-158">Visi čekiai, kurie nebuvo įtraukti į teigiamo mokėjimo failą iki šios čekio datos, įtraukiami į failą.</span><span class="sxs-lookup"><span data-stu-id="6697a-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="6697a-159">Teigiamo mokėjimo failų generavimo rezultatų peržiūra</span><span class="sxs-lookup"><span data-stu-id="6697a-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="6697a-160">Kai teigiamo mokėjimo failas sugeneruotas, rezultatus galite peržiūrėti puslapyje **Teigiamo mokėjimo failų suvestinė**.</span><span class="sxs-lookup"><span data-stu-id="6697a-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="6697a-161">Norėdami peržiūrėti išsamią atskirų čekių informaciją, naudokite puslapį **Teigiamo mokėjimo failų informacija**.</span><span class="sxs-lookup"><span data-stu-id="6697a-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="6697a-162">Patvirtinti teigiamo mokėjimo failą</span><span class="sxs-lookup"><span data-stu-id="6697a-162">Confirm a positive pay file</span></span>
<span data-ttu-id="6697a-163">Po to, kai teigiamo mokėjimo faile nurodyti čekiai apmokami, iš bango gausite patvirtinimo numerį.</span><span class="sxs-lookup"><span data-stu-id="6697a-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="6697a-164">Tada teigiamo mokėjimo failą galite patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="6697a-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="6697a-165">Puslapyje **Teigiamo mokėjimo failų suvestinė** pasirinkite teigiamo mokėjimo failą, kurio būsena – **Sukurtas**, tada pasirinkite veiksmą **Įvesti patvirtinimą**.</span><span class="sxs-lookup"><span data-stu-id="6697a-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="6697a-166">Kai tvirtinate teigiamo mokėjimo failą, įrašomas jūsų iš banko gautas patvirtinimo numeris.</span><span class="sxs-lookup"><span data-stu-id="6697a-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="6697a-167">Teigiamo mokėjimo failo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="6697a-167">Recall a positive pay file</span></span>
<span data-ttu-id="6697a-168">Jei turite teigiamo mokėjimo failą pakeisti, galite jį atšaukti.</span><span class="sxs-lookup"><span data-stu-id="6697a-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="6697a-169">Puslapyje **Teigiamo mokėjimo failų suvestinė** pasirinkite teigiamo mokėjimo failą, kurio būsena – **Sukurtas**, tada pasirinkite veiksmą **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="6697a-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="6697a-170">Iš naujo nustatomas kiekvieno teigiamo mokėjimo failo čekio laukas, kuriame nurodoma, ar tas čekis įtrauktas į teigiamo mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="6697a-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="6697a-171">Tada galite sukurti naują teigiamo mokėjimo failą, kuriame yra atšauktas čekis.</span><span class="sxs-lookup"><span data-stu-id="6697a-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>




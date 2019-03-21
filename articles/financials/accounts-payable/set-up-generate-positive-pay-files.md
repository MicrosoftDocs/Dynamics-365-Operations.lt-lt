---
title: Teigiamų mokėjimų failų nustatymas ir generavimas
description: Šioje temoje paaiškinama, kaip nustatyti teigiamą mokėjimą ir generuoti teigiamo mokėjimo failus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: dbc512c6d214dc8cf2527ac23103529111896ec5
ms.sourcegitcommit: 065d9fab832b6bcc88c00dc78ac1ae854c762ec7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/06/2019
ms.locfileid: "778183"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="cb0bd-103">Teigiamų mokėjimų failų nustatymas ir generavimas</span><span class="sxs-lookup"><span data-stu-id="cb0bd-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb0bd-104">Šioje temoje paaiškinama, kaip nustatyti teigiamą mokėjimą ir generuoti teigiamo mokėjimo failus.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="cb0bd-105">Nustatykite teigiamą mokėjimą, jei norite generuoti bankui teikiamą elektroninį čekių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="cb0bd-106">Tada, kai čekis pateikiamas bankui, bankas jį lygina su čekių sąrašu.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="cb0bd-107">Jei čekis atitinka sąraše esantįjį, bankas jį patvirtina.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="cb0bd-108">Jei čekis sąraše esančio čekio neatitinka, bankas jį pasilieka peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="cb0bd-109">Teigiamų mokėjimų failų sauga</span><span class="sxs-lookup"><span data-stu-id="cb0bd-109">Security for positive pay files</span></span>
<span data-ttu-id="cb0bd-110">Teigiamo mokėjimo failuose gali būti neskelbtinos informacijos apie mokėjimų gavėjus ir čekių sumas.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="cb0bd-111">Todėl būtinai naudokite reikiamas saugos priemones nuo failų sugeneravimo akimirkos iki jų gavimo banke.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="cb0bd-112">Teigiamų mokėjimų failai atsiunčiami į vietą, kurią nurodo jūsų žiniatinklio naršyklė.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="cb0bd-113">Kadangi teigiamų mokėjimų failuose gali būti slaptos informacijos, svarbu, kad programoje „Microsoft Dynamics 365 for Finance and Operations“ šios informacijos generavimo ir peržiūros prieigą turėtų tik įgaliotieji vartotojai.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="cb0bd-114">Tolesnė lentelė jums padės nustatyti reikiamas teises.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb0bd-115">Užduotis</span><span class="sxs-lookup"><span data-stu-id="cb0bd-115">Task</span></span></th>
<th><span data-ttu-id="cb0bd-116">Privilegija</span><span class="sxs-lookup"><span data-stu-id="cb0bd-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb0bd-117">Generuoti teigiamų mokėjimų failus iš sąrašo puslapio <strong>Banko sąskaitos</strong> arba puslapio <strong>Banko sąskaitos</strong>.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="cb0bd-118"><strong>Tvarkyti banko teigiamų mokėjimų informaciją</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="cb0bd-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="cb0bd-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="cb0bd-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb0bd-120">Generuoti kelių juridinių subjektų ir banko sąskaitų teigiamų mokėjimų failus iš puslapio <strong>Generuoti teigiamo mokėjimo failą</strong>.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="cb0bd-121"><strong>Tvarkyti banko teigiamų mokėjimų informaciją</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="cb0bd-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="cb0bd-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="cb0bd-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb0bd-123">Peržiūrėti teigiamų mokėjimų failus puslapyje <strong>Teigiamų mokėjimų failų suvestinė</strong>.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="cb0bd-124"><strong>Peržiūrėti banko teigiamų mokėjimų informaciją keliems juridiniams subjektams</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="cb0bd-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb0bd-125">Patvirtinti banko teigiamo mokėjimo failą puslapyje <strong>Teigiamų mokėjimų failų suvestinė</strong>.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="cb0bd-126"><strong>Patvirtinti teigiamo mokėjimo failą</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="cb0bd-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb0bd-127">Atšaukti banko teigiamo mokėjimo failą puslapyje <strong>Teigiamų mokėjimų failų suvestinė</strong>.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="cb0bd-128"><strong>Atšaukti teigiamo mokėjimo failą</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="cb0bd-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="cb0bd-129">Teigiamo mokėjimo formato nustatymas</span><span class="sxs-lookup"><span data-stu-id="cb0bd-129">Set up a positive pay format</span></span>
<span data-ttu-id="cb0bd-130">Teigiamo mokėjimo failai kuriami naudojant duomenų objektus.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="cb0bd-131">Negalėsite generuoti teigiamo mokėjimo failo, kol nenustatysite transformacijos įvesties duomenų formato, kuris bus naudojamas čekio informacijai paversti į formatą, galintį bendrauti su banku.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="cb0bd-132">Puslapyje **Teigiamo mokėjimo formatas** galite sukurti failo formato identifikatorių ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="cb0bd-133">Transformacijos įvesties duomenų formato tipas turi būti XML.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="cb0bd-134">Konkretus formatas priklauso nuo jūsų naudojamo transformavimo failo.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="cb0bd-135">Pvz., pateiktame išplėstinės stiliaus aprašų kalbos transformacijų (XSLT) failo pavyzdyje naudojamas formatas **XML elementas**.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="cb0bd-136">Naudodami veiksmą **Nusiųsti failą, naudotą transformacijai atlikti**, galite nurodyti jūsų banko reikalaujamo formato transformavimo failo vietą.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="cb0bd-137">Pavyzdys: teigiamo mokėjimo failo XSLT failas</span><span class="sxs-lookup"><span data-stu-id="cb0bd-137">Example: XSLT file for positive pay file</span></span>
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
          <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
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

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="cb0bd-138">Teigiamo mokėjimo formato priskyrimas banko sąskaitai</span><span class="sxs-lookup"><span data-stu-id="cb0bd-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="cb0bd-139">Kiekvienai banko sąskaitai, kuriai norite generuoti teigiamo mokėjimo informaciją, turite priskirti teigiamo mokėjimo formatą, kurį nurodėte ankstesnėje dalyje.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="cb0bd-140">Puslapyje **Banko sąskaitos** pasirinkite teigiamo mokėjimo formatą, kuris atitinka banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="cb0bd-141">Lauke **Teigiamo mokėjimo pradžios data** įveskite pirmąją teigiamo mokėjimo failų generavimo datą.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="cb0bd-142">Svarbu šiame lauke įvesti datą.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="cb0bd-143">Priešingu atveju pirmasis jūsų sugeneruotas teigiamo mokėjimo failas apims visus kada nors sukurtus šios banko sąskaitos čekius.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="cb0bd-144">Teigiamo mokėjimo failų numeracijos priskyrimas</span><span class="sxs-lookup"><span data-stu-id="cb0bd-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="cb0bd-145">Kiekvienas teigiamo mokėjimo failas turi turėti unikalų numerį.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="cb0bd-146">Norėdami sukurti teigiamo mokėjimo failų numeraciją, naudokite skirtuką **Numeracijos**, esantį puslapyje **Grynųjų pinigų ir banko valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="cb0bd-147">Vienos banko sąskaitos teigiamo mokėjimo failo generavimas</span><span class="sxs-lookup"><span data-stu-id="cb0bd-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="cb0bd-148">Galite generuoti teigiamo mokėjimo failą vienam juridiniam subjektui ir vienai banko sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="cb0bd-149">Informacijos apie tai, kaip generuoti teigiamo mokėjimo failus keletui juridinių subjektų ir banko sąskaitų vienu metu, rasite kitame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="cb0bd-150">Norėdami generuoti vieno juridinio subjekto ir vienos banko sąskaitos teigiamo mokėjimo failą, iš puslapio **Banko sąskaitos** atidarykite dialogo langą **Generuoti teigiamo mokėjimo failą**.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="cb0bd-151">Lauke **Nutraukimo data** įveskite paskutinę čekio datą, kurią norite įtraukti į teigiamo mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="cb0bd-152">Visi čekiai, kurie nebuvo įtraukti į teigiamo mokėjimo failą iki šios čekio datos, įtraukiami į failą.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="cb0bd-153">Kelių banko sąskaitų teigiamo mokėjimo failo generavimas</span><span class="sxs-lookup"><span data-stu-id="cb0bd-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="cb0bd-154">Norėdami generuoti kelių banko sąskaitų teigiamo mokėjimo failą, naudokite periodinę užduotį **Generuoti teigiamo mokėjimo failą**.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="cb0bd-155">Pasirinkite failo teigiamo mokėjimo formatą ir nurodykite, ar failą norite generuoti visiems juridiniams subjektams, ar pasirinktam juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="cb0bd-156">Teigiamo mokėjimo failą taip pat galite generuoti visoms banko sąskaitoms, kurios naudoja nurodytą teigiamo mokėjimo formatą, arba atskirai banko sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="cb0bd-157">Lauke **Nutraukimo data** įveskite paskutinę čekio datą, kurią norite įtraukti į teigiamo mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="cb0bd-158">Visi čekiai, kurie nebuvo įtraukti į teigiamo mokėjimo failą iki šios čekio datos, įtraukiami į failą.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="cb0bd-159">Teigiamo mokėjimo failų generavimo rezultatų peržiūra</span><span class="sxs-lookup"><span data-stu-id="cb0bd-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="cb0bd-160">Kai teigiamo mokėjimo failas sugeneruotas, rezultatus galite peržiūrėti puslapyje **Teigiamo mokėjimo failų suvestinė**.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="cb0bd-161">Norėdami peržiūrėti išsamią atskirų čekių informaciją, naudokite puslapį **Teigiamo mokėjimo failų informacija**.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="cb0bd-162">Patvirtinti teigiamo mokėjimo failą</span><span class="sxs-lookup"><span data-stu-id="cb0bd-162">Confirm a positive pay file</span></span>
<span data-ttu-id="cb0bd-163">Po to, kai teigiamo mokėjimo faile nurodyti čekiai apmokami, iš bango gausite patvirtinimo numerį.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="cb0bd-164">Tada teigiamo mokėjimo failą galite patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="cb0bd-165">Puslapyje **Teigiamo mokėjimo failų suvestinė** pasirinkite teigiamo mokėjimo failą, kurio būsena – **Sukurtas**, tada pasirinkite veiksmą **Įvesti patvirtinimą**.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="cb0bd-166">Kai tvirtinate teigiamo mokėjimo failą, įrašomas jūsų iš banko gautas patvirtinimo numeris.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="cb0bd-167">Teigiamo mokėjimo failo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="cb0bd-167">Recall a positive pay file</span></span>
<span data-ttu-id="cb0bd-168">Jei turite teigiamo mokėjimo failą pakeisti, galite jį atšaukti.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="cb0bd-169">Puslapyje **Teigiamo mokėjimo failų suvestinė** pasirinkite teigiamo mokėjimo failą, kurio būsena – **Sukurtas**, tada pasirinkite veiksmą **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="cb0bd-170">Iš naujo nustatomas kiekvieno teigiamo mokėjimo failo čekio laukas, kuriame nurodoma, ar tas čekis įtrauktas į teigiamo mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="cb0bd-171">Tada galite sukurti naują teigiamo mokėjimo failą, kuriame yra atšauktas čekis.</span><span class="sxs-lookup"><span data-stu-id="cb0bd-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>




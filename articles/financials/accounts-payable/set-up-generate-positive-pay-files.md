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
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 41d7b64f8414385629acef071c47a654d56005bd
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="set-up-and-generate-positive-pay-files"></a>Teigiamų mokėjimų failų nustatymas ir generavimas

[!INCLUDE [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti teigiamą mokėjimą ir generuoti teigiamo mokėjimo failus. 

Nustatykite teigiamą mokėjimą, jei norite generuoti bankui teikiamą elektroninį čekių sąrašą. Tada, kai čekis pateikiamas bankui, bankas jį lygina su čekių sąrašu. Jei čekis atitinka sąraše esantįjį, bankas jį patvirtina. Jei čekis sąraše esančio čekio neatitinka, bankas jį pasilieka peržiūrėti.

## <a name="security-for-positive-pay-files"></a>Teigiamų mokėjimų failų sauga
Teigiamo mokėjimo failuose gali būti neskelbtinos informacijos apie mokėjimų gavėjus ir čekių sumas. Todėl būtinai naudokite reikiamas saugos priemones nuo failų sugeneravimo akimirkos iki jų gavimo banke. Teigiamų mokėjimų failai atsiunčiami į vietą, kurią nurodo jūsų žiniatinklio naršyklė. Kadangi teigiamų mokėjimų failuose gali būti slaptos informacijos, svarbu, kad programoje „Microsoft Dynamics 365 for Finance and Operations‟ šios informacijos generavimo ir peržiūros prieigą turėtų tik įgaliotieji vartotojai. Tolesnė lentelė jums padės nustatyti reikiamas teises.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Užduotis</th>
<th>Privilegija</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Generuoti teigiamų mokėjimų failus iš sąrašo puslapio <strong>Banko sąskaitos</strong> arba puslapio <strong>Banko sąskaitos</strong>.</td>
<td><ul>
<li><strong>Tvarkyti banko teigiamų mokėjimų informaciją</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Generuoti kelių juridinių subjektų ir banko sąskaitų teigiamų mokėjimų failus iš puslapio <strong>Generuoti teigiamo mokėjimo failą</strong>.</td>
<td><ul>
<li><strong>Tvarkyti banko teigiamų mokėjimų informaciją</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Peržiūrėti teigiamų mokėjimų failus puslapyje <strong>Teigiamų mokėjimų failų suvestinė</strong>.</td>
<td><strong>Peržiūrėti banko teigiamų mokėjimų informaciją keliems juridiniams subjektams</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Patvirtinti banko teigiamo mokėjimo failą puslapyje <strong>Teigiamų mokėjimų failų suvestinė</strong>.</td>
<td><strong>Patvirtinti teigiamo mokėjimo failą</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Atšaukti banko teigiamo mokėjimo failą puslapyje <strong>Teigiamų mokėjimų failų suvestinė</strong>.</td>
<td><strong>Atšaukti teigiamo mokėjimo failą</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>Teigiamo mokėjimo formato nustatymas
Teigiamo mokėjimo failai kuriami naudojant duomenų objektus. Negalėsite generuoti teigiamo mokėjimo failo, kol nenustatysite transformacijos įvesties duomenų formato, kuris bus naudojamas čekio informacijai paversti į formatą, galintį bendrauti su banku. Puslapyje **Teigiamo mokėjimo formatas** galite sukurti failo formato identifikatorių ir aprašą. Transformacijos įvesties duomenų formato tipas turi būti XML. Konkretus formatas priklauso nuo jūsų naudojamo transformavimo failo. Pvz., pateiktame išplėstinės stiliaus aprašų kalbos transformacijų (XSLT) failo pavyzdyje naudojamas formatas **XML elementas**. Naudodami veiksmą **Nusiųsti failą, naudotą transformacijai atlikti**, galite nurodyti jūsų banko reikalaujamo formato transformavimo failo vietą.

## <a name="example-xslt-file-for-positive-pay-file"></a>Pavyzdys: teigiamo mokėjimo failo XSLT failas
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

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Teigiamo mokėjimo formato priskyrimas banko sąskaitai
Kiekvienai banko sąskaitai, kuriai norite generuoti teigiamo mokėjimo informaciją, turite priskirti teigiamo mokėjimo formatą, kurį nurodėte ankstesnėje dalyje. Puslapyje **Banko sąskaitos** pasirinkite teigiamo mokėjimo formatą, kuris atitinka banko sąskaitą. Lauke **Teigiamo mokėjimo pradžios data** įveskite pirmąją teigiamo mokėjimo failų generavimo datą. Svarbu šiame lauke įvesti datą. Priešingu atveju pirmasis jūsų sugeneruotas teigiamo mokėjimo failas apims visus kada nors sukurtus šios banko sąskaitos čekius.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Teigiamo mokėjimo failų numeracijos priskyrimas
Kiekvienas teigiamo mokėjimo failas turi turėti unikalų numerį. Norėdami sukurti teigiamo mokėjimo failų numeraciją, naudokite skirtuką **Numeracijos**, esantį puslapyje **Grynųjų pinigų ir banko valdymo parametrai**.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Vienos banko sąskaitos teigiamo mokėjimo failo generavimas
Galite generuoti teigiamo mokėjimo failą vienam juridiniam subjektui ir vienai banko sąskaitai. Informacijos apie tai, kaip generuoti teigiamo mokėjimo failus keletui juridinių subjektų ir banko sąskaitų vienu metu, rasite kitame skyriuje. Norėdami generuoti vieno juridinio subjekto ir vienos banko sąskaitos teigiamo mokėjimo failą, iš puslapio **Banko sąskaitos** atidarykite dialogo langą **Generuoti teigiamo mokėjimo failą**. Lauke **Nutraukimo data** įveskite paskutinę čekio datą, kurią norite įtraukti į teigiamo mokėjimo failą. Visi čekiai, kurie nebuvo įtraukti į teigiamo mokėjimo failą iki šios čekio datos, įtraukiami į failą.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Kelių banko sąskaitų teigiamo mokėjimo failo generavimas
Norėdami generuoti kelių banko sąskaitų teigiamo mokėjimo failą, naudokite periodinę užduotį **Generuoti teigiamo mokėjimo failą**. Pasirinkite failo teigiamo mokėjimo formatą ir nurodykite, ar failą norite generuoti visiems juridiniams subjektams, ar pasirinktam juridiniam subjektui. Teigiamo mokėjimo failą taip pat galite generuoti visoms banko sąskaitoms, kurios naudoja nurodytą teigiamo mokėjimo formatą, arba atskirai banko sąskaitai. Lauke **Nutraukimo data** įveskite paskutinę čekio datą, kurią norite įtraukti į teigiamo mokėjimo failą. Visi čekiai, kurie nebuvo įtraukti į teigiamo mokėjimo failą iki šios čekio datos, įtraukiami į failą.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Teigiamo mokėjimo failų generavimo rezultatų peržiūra
Kai teigiamo mokėjimo failas sugeneruotas, rezultatus galite peržiūrėti puslapyje **Teigiamo mokėjimo failų suvestinė**. Norėdami peržiūrėti išsamią atskirų čekių informaciją, naudokite puslapį **Teigiamo mokėjimo failų informacija**.

## <a name="confirm-a-positive-pay-file"></a>Patvirtinti teigiamo mokėjimo failą
Po to, kai teigiamo mokėjimo faile nurodyti čekiai apmokami, iš bango gausite patvirtinimo numerį. Tada teigiamo mokėjimo failą galite patvirtinti. Puslapyje **Teigiamo mokėjimo failų suvestinė** pasirinkite teigiamo mokėjimo failą, kurio būsena – **Sukurtas**, tada pasirinkite veiksmą **Įvesti patvirtinimą**. Kai tvirtinate teigiamo mokėjimo failą, įrašomas jūsų iš banko gautas patvirtinimo numeris.

## <a name="recall-a-positive-pay-file"></a>Teigiamo mokėjimo failo atšaukimas
Jei turite teigiamo mokėjimo failą pakeisti, galite jį atšaukti. Puslapyje **Teigiamo mokėjimo failų suvestinė** pasirinkite teigiamo mokėjimo failą, kurio būsena – **Sukurtas**, tada pasirinkite veiksmą **Atšaukti**. Iš naujo nustatomas kiekvieno teigiamo mokėjimo failo čekio laukas, kuriame nurodoma, ar tas čekis įtrauktas į teigiamo mokėjimo failą. Tada galite sukurti naują teigiamo mokėjimo failą, kuriame yra atšauktas čekis.





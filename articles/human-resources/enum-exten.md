---
title: Lytį pagrindinio enum extensibility
description: Šiame straipsnyje pateikiama apžvalga apie tai, kaip gali būti išvardijimas pagal lytį (išvardijimas).
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749303"
---
# <a name="gender-base-enum-extensibility"></a>Lytį pagrindinio enum extensibility

Dabar **giminės** išvardijimas (išvardijimas) dabar yra extensible. Šiame straipsnyje aprašomi pakeitimai, kuriuos turite atlikti kodo pagrindu, jei planuojate išplėsti išvardijus **lytį**.

## <a name="gender-vs-hcmpersongender"></a>Lytis, vs. HcmPersonGender

Yra du išvardi įrašai, skirti lytį vertėms:

- **Lytis** (programos platforma)
- **HcmPersonGender** (PersonnelManagement)

Išvardiimas **pagal** lytį naudojamas Microsoft Dynamics visoje 365 finansų dalyje, **o HcmPersonGender** yra konkretus žmogiškojo kapitalo valdymo (HCM) funkcijai. Jei naudojate HCM funkciją ir pakeičiate lytį, **·** **turėtumėte apsvarstyti galimybę atlikti tuos pačius HcmPersonGender pakeitimus.** Pvz., jei pridedate **Transgender** **į** lytį išvarditi, **pridėkite Transgender** **prie HcmPersonGender išvardijote** taip pat.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (klasė)

**Nauja HcmPersonGenderTranformUtil** klasė buvo sukurta taip, kad leistų vertimą tarp dviejų pagrindinių išvardintojų. Šioje klasėje yra du metodai: **convertGenderToHcmPersonGender** **ir convertHcmPersonGenderToGender**. Plėtinį turėtumėte sukurti **naudodami** **komandų** klasės arba įvykių apdorojimo programos grandinę, ir pratęskite abu metodus, kad susieumėte naujas vertes, kurios pridėtos prie pagrindinio išvardi sudaryti.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (klasė)

**PayrollStateWageTaxPrepDP** **yra duomenų teikėjo klasė, skirta algalapio valstybės atlyginimo mokesčių išankstinių** SQL serverio ataskaitų tarnybų (SSRS) ataskaitai. Galimos trys Jungtinių Amerikos Valstijų vertės: Vyras, Moteris **ir** Nenurodyta **.** **·** Naudojant metodą populatePayrollStateWageTaxPrepTmp **yra switch sakinys,** naudojamas susieti HcmPersonGender **išvardijo vertę su vienu iš trijų laukų:** IsMale **,** IsFemale **arba** IsUnspecifiedGender **.** Numatytoji perjungimo išrašo reikšmė yra **IsUnspecifiedGender**. **Jei prie HcmPersonGender** enum pridedate kokias nors vertes, **norėdami ją susieti turite sukurti plėtinį naudodami klasės Command** **grandinę, o ne metodą populatePayrollStateWageTaxPrepTmp**, kad pakeistumėte vertę pagal poreikius.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (klasė)

Ši **smmOutlookSync_Contact** integravimo klasė susieja vertes su Outlook ir **Kontaktiniais** asmenimis **ir iš jų**. **Outlook** palaiko tris vertes: **Neapdorota**,**Moterys** **ir Nenurodyta**. Klasė turi du metodus, kurie padės susieti **lytį su** **OutlookGenders**. Numatytasis metodas nėra **nespecifinis/nenurodytas**. Jei sukursite papildomas vertes, skirtas **lytį** išvarditi, **turėtumėte** sukurti plėtinį naudodami komandų klasės grandinę ir pagal poreikį susieti metodus ir schemą.

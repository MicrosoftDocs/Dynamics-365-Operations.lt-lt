---
title: Audito strategijos taisyklės
description: Norėdami įvertinti išlaidų ataskaitas, tiekėjo SF ir pirkimo užsakymus ir įsitikinti, kad jie atitinka jūsų kuriamas strategijos taisyklės, galite naudoti audito strategijas. Visos su audito strategija susietos taisyklės vykdomos paketiniu režimu pagal jūsų nurodytą grafiką.  Kiekviena strategijos taisyklė yra strategijos taisyklės tipo egzempliorius. Vienu metu gali būti aktyvi tik viena strategijos taisyklės tipo strategijos taisyklė.
author: panolte
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998d4dbabec74528b4acb9e797faef0c449e7c28
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021246"
---
# <a name="audit-policy-rules"></a>Audito strategijos taisyklės

[!include [banner](../includes/banner.md)]

Norėdami įvertinti išlaidų ataskaitas, tiekėjo SF ir pirkimo užsakymus ir įsitikinti, kad jie atitinka jūsų kuriamas strategijos taisyklės, galite naudoti audito strategijas. Visos su audito strategija susietos taisyklės vykdomos paketiniu režimu pagal jūsų nurodytą grafiką.  Kiekviena strategijos taisyklė yra strategijos taisyklės tipo egzempliorius. Vienu metu gali būti aktyvi tik viena strategijos taisyklės tipo strategijos taisyklė. 

<a name="queries-and-query-types"></a>Užklausos ir užklausų tipai
-----------------------

Kai kuriate audito strategijos taisyklę, pirmiausia pasirenkate strategijos taisyklės tipą. Strategijos taisyklės tipas nurodo programos objektų medžio (AOT) užklausą, kuri turi būti naudojama kaip pradinis strategijos taisyklės kūrimo taškas. Jis taip pat nurodo naudotiną strategijos taisyklės užklausos tipą. Užklausa nurodo šaltinio dokumentą, kurį įvertina strategijos taisyklė. Ji taip pat apibrėžia šaltinio dokumento laukus, nurodančius juridinį subjektą ir datą, kurie bus naudojami pasirinkus dokumentus auditui atlikti. Užklausos tipas valdo numatytuosius laukus užklausos puslapyje ir audito strategijos taisyklių puslapyje. Toliau pateiktoje lentelėje nurodyti galimi audito strategijos taisyklių užklausų tipai.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Užklausos tipas</th>
<th>Paskirtis</th>
<th>Daugiau informacijos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sąlyginis</td>
<td>Įvertinti šaltinio dokumento atributus pagal nurodytas vertes.</td>
<td></td>
</tr>
<tr class="even">
<td>Agreguoti</td>
<td>Įvertinti kelis šaltinio dokumentus arba šaltinio dokumento eilutes pagal strategijos taisyklę sudedant skaitines vertes.</td>
<td></td>
</tr>
<tr class="odd">
<td>Pavyzdžio ėmimas</td>
<td>Atsitiktine tvarka pasirinkti nurodytą šaltinio dokumentų procentinį dydį strategijos pažeidimams įvertinti.</td>
<td>Kai pasirenkate šią parinktį, naudokite audito strategijos taisyklių puslapį, nurodydami, kiek procentų dokumentų reikia atsitiktine tvarka pasirinkti auditui.</td>
</tr>
<tr class="even">
<td>Dublikatas</td>
<td>Įvertinti šaltinio dokumentus, siekiant nustatyti, ar nurodytuose jų laukuose yra įrašų dublikatų.</td>
<td>Kai pasirenkate šią parinktį, naudokite audito strategijos taisyklių puslapį, kad nurodytumėte, kiek dienų įtraukti į dokumentų pasirinkimo datų intervalo pradžią, kai įvertinama, ar dokumentuose nėra įrašų dublikatų.</td>
</tr>
<tr class="odd">
<td>Sąrašo ieška</td>
<td>Įvertinti šaltinio dokumentus, ar juose yra konkrečių objektų.</td>
<td>Šakninis užklausos dokumentas apibrėžia dokumentą, kurio auditas atliekamas. Užklausa turi būti sąrašo užklausa, apimanti nuorodą į „dirpartytable“ lentelę. Šią parinktį galima naudoti tik su toliau nurodytomis AOT užklausomis.
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (Išlaidų ataskaitoje stebimi darbuotojai)</li>
<li><span class="ui">AuditPolicyPurchList</span> (Pirkimo užsakyme stebimi tiekėjai)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (Tiekėjo SF stebimi tiekėjai)</li>
</ul>
Kai pasirenkate šią parinktį, nurodykite stebimus objektus audito strategijos taisyklių puslapyje.</td>
</tr>
<tr class="even">
<td>Raktažodžių ieška</td>
<td>Įvertinti šaltinio dokumentus, siekiant nustatyti, ar juose yra tam tikrų žodžių.</td>
<td>Kai pasirenkate šią parinktį, įveskite žodžius, kurių reikia ieškoti audito strategijos taisyklių puslapyje. Audito strategijos taisyklių puslapyje taip pat yra parinkčių, leidžiančių nurodyti lenteles ir laukus, kuriuos norite įvertinti pagal įvestus žodžius.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Bendri parametrai
Visos tam tikros audito strategijos taisyklės bendrai naudoja tuos pačius paketinius parametrus ir tą patį dokumentų pasirinkimo datų intervalą. Šie parametrai strategijai nurodomi puslapyje „Papildomos parinktys“.



<a name="additional-resources"></a>Papildomi ištekliai
--------

[Audito strategijos pažeidimai ir atvejai](audit-policy-violations-cases.md)
[Apibrėžti šaltinio dokumento audito strategijas](tasks/define-audit-policies-source-documents.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
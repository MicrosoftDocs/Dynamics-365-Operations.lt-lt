---
title: Nustatyti ir sugeneruoti teigiamo mokėjimo failus naudojant elektronines ataskaitas
description: Šioje temoje paaiškinama, kaip nustatyti teigiamą užmokestį naudojant elektronines ataskaitas.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: bc2f17d62b429b599d5ac5f2a521819275d36b64
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770253"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Nustatyti teigiamo mokėjimo failus naudojant elektroninę ataskaitą

Šioje temoje paaiškinama, kaip nustatyti teigiamą atlyginimą ir sugeneruoti teigiamo mokėjimo failus naudojant elektroninę ataskaitą.

> [!NOTE] 
> Prieš naudodami funkciją **Generuoti banko teigiamų išlaidų** failą, pirmiausia turėsite atnaujinti objektų sąrašą.
> Eikite į **Duomenų valdymas > Importas / eksportas > Sistemos parametrai** 
> „FastTab“ **Objekto parametrai**, pasirinkite **Atnaujinti objektų sąrašą**.


Nustatykite teigiamą mokėjimą, jei norite generuoti bankui teikiamą elektroninį čekių sąrašą. Kai čekis pateikiamas bankui, bankas jį palygina su čekių sąrašu. Jei čekis atitinka sąraše esantįjį, bankas jį patvirtina. Jei čekis sąraše esančio čekio neatitinka, bankas jį pasilieka peržiūrėti.

## <a name="security-for-positive-pay-files"></a>Teigiamų mokėjimų failų sauga
Teigiamo mokėjimo failuose gali būti neskelbtinos informacijos apie mokėjimų gavėjus ir čekių sumas. Todėl būtinai naudokite reikiamas saugos priemones nuo failų sugeneravimo akimirkos iki jų gavimo banke. Teigiamų mokėjimų failai atsiunčiami į vietą, kurią nurodo jūsų žiniatinklio naršyklė. Teigiamo mokėjimo failuose gali būti slaptos informacijos, todėl svarbu, Microsoft Dynamics kad šią informaciją sugeneruotų ir peržiūrėti tik įgaliotieji vartotojai, naudojantys 365 finansus. Tolesnė lentelė jums padės nustatyti reikiamas teises.

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

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektroninių ataskaitų konfigūracijos parametrai

1. Eikite į **darbo sričių elektronines \> ataskaitas**.
2. "Microsoft" konfigūracijos teikėjo **išklotijoje** pasirinkite **Saugyklos**.
3. Pasirinkite **Visuotiniai ištekliai** ir pasirinkite **Atidaryti**.
4. Jei reikia užmegzti ryšį su saugykla, dialogo lange pasirinkite mėlyną saitą.
5. Konfigūracijos sąraše suraskite ir pasirinkite Teigiamo mokėjimo **modelio teigiamo \> mokėjimo formatą**.
6. Skirtuke **Versijos** FastTab pasirinkite naujausią versiją, tada pasirinkite **Importuoti**.

## <a name="set-up-a-positive-pay-format"></a>Teigiamo mokėjimo formato nustatymas

1. Eikite į **grynųjų pinigų ir banko valdymo nustatymo \> teigiamo \> mokėjimo formatus**.
2. Pasirinkite **Nauja**.
3. Nustatykite **mokėjimo formatą** ir **aprašymo** laukus.
4. Pažymėkite žymės **langelį Bendrasis elektroninis eksportavimo** formatas.
5. Nustatykite eksportavimo **formato konfigūracijos** lauką kaip **teigiamo mokėjimo formatą**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Teigiamo mokėjimo formato priskyrimas banko sąskaitai
Kiekvienai banko sąskaitai, kuriai norite generuoti teigiamo mokėjimo informaciją, turite priskirti teigiamo mokėjimo formatą, kurį nurodėte ankstesnėje dalyje. Puslapyje Banko sąskaitos pasirinkite teigiamo mokėjimo formatą, kuris atitinka banko sąskaitą. Lauke **Teigiamo mokėjimo pradžios data** įveskite pirmąją teigiamo mokėjimo failų generavimo datą. 

>[!Important]
> Įveskite datą lauke **Teigiamo mokėjimo pradžios** data. Jei paliksite tuščią, į pirmąjį sugeneruotą teigiamo mokėjimo failą bus įtraukti visi čekiai, kurie buvo sukurti šiai banko sąskaitai.

1. Eiti į grynųjų **pinigų ir banko valdymo \> banko sąskaitas \> Banko sąskaitos**.
2. Atidarykite banko sąskaitą.
3. Skirtuko Bendra **FastTab** lauke Teigiamo mokėjimo **formatas nustatykite** anksčiau sukurtą formatą.
4. Nustatykite **teigiamo mokėjimo pradžios datos** lauką į dabartinę datą.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Teigiamo mokėjimo failų numeracijos priskyrimas
Kiekvienas teigiamo mokėjimo failas turi turėti unikalų numerį. Grynųjų **pinigų ir banko valdymo parametrų** puslapyje, numeraciją teigiamo mokėjimo failams, sukurkite **numeraciją skirtuke Numeracijos**.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Vienos banko sąskaitos teigiamo mokėjimo failo generavimas
Galite generuoti teigiamo mokėjimo failą vienam juridiniam subjektui ir vienai banko sąskaitai. Informacijos apie tai, kaip generuoti teigiamo mokėjimo failus keletui juridinių subjektų ir banko sąskaitų vienu metu, rasite kitame skyriuje. Norėdami generuoti vieno juridinio subjekto ir vienos banko sąskaitos teigiamo mokėjimo failą, iš puslapio **Banko sąskaitos** atidarykite dialogo langą **Generuoti teigiamo mokėjimo failą**. Lauke **Nutraukimo data** įveskite paskutinę čekio datą, kurią norite įtraukti į teigiamo mokėjimo failą. Visi čekiai, kurie nebuvo įtraukti į teigiamo mokėjimo failą iki šios čekio datos, įtraukiami į failą.

1. Eiti į grynųjų **pinigų ir banko valdymo \> banko sąskaitų \> banko sąskaitas**.
2. Atidarykite banko sąskaitą, kurios teigiamas mokėjimas nustatytas.
3. Pasirinkite Tvarkyti **mokėjimus teigiamo mokėjimo \> teigiamo mokėjimo failą \>**.
4. Nustatykite **iškirptos datos lauką**. Čekiai, sugeneruoti prieš šią datą, bus įtraukti.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Kelių banko sąskaitų teigiamo mokėjimo failo generavimas
Norėdami sugeneruoti kelių banko sąskaitų teigiamo mokėjimo failą, naudokite teigiamo mokėjimo **failo periodinę** užduotį. Pasirinkite failo teigiamo mokėjimo formatą ir nurodykite, ar failą norite generuoti visiems juridiniams subjektams, ar pasirinktam juridiniam subjektui. Teigiamo mokėjimo failą taip pat galite generuoti visoms banko sąskaitoms, kurios naudoja nurodytą teigiamo mokėjimo formatą, arba atskirai banko sąskaitai. Lauke **Nutraukimo data** įveskite paskutinę čekio datą, kurią norite įtraukti į teigiamo mokėjimo failą. Visi čekiai, kurie nebuvo įtraukti į teigiamo mokėjimo failą iki šios čekio datos, įtraukiami į failą.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Teigiamo mokėjimo failų generavimo rezultatų peržiūra
Kai teigiamo mokėjimo failas sugeneruotas, rezultatus galite peržiūrėti puslapyje **Teigiamo mokėjimo failų suvestinė**. Norėdami peržiūrėti atskirų čekių informaciją, eikite į teigiamo mokėjimo **failo informacijos** puslapį.

## <a name="confirm-a-positive-pay-file"></a>Patvirtinti teigiamo mokėjimo failą
Po to, kai teigiamo mokėjimo faile nurodyti čekiai apmokami, iš bango gausite patvirtinimo numerį. Tada teigiamo mokėjimo failą galite patvirtinti. Puslapyje **Teigiamo mokėjimo failų suvestinė** pasirinkite teigiamo mokėjimo failą, kurio būsena – **Sukurtas**, tada pasirinkite veiksmą **Įvesti patvirtinimą**. Kai tvirtinate teigiamo mokėjimo failą, įrašomas jūsų iš banko gautas patvirtinimo numeris.

## <a name="recall-a-positive-pay-file"></a>Teigiamo mokėjimo failo atšaukimas
Jei turite teigiamo mokėjimo failą pakeisti, galite jį atšaukti. Puslapyje **Teigiamo mokėjimo failų suvestinė** pasirinkite teigiamo mokėjimo failą, kurio būsena – **Sukurtas**, tada pasirinkite veiksmą **Atšaukti**. Iš naujo nustatomas kiekvieno teigiamo mokėjimo failo čekio laukas, kuriame nurodoma, ar tas čekis įtrauktas į teigiamo mokėjimo failą. Tada galite sukurti naują teigiamo mokėjimo failą, kuriame yra atšauktas čekis.


Gautas XML failas bus atsisiųstas.

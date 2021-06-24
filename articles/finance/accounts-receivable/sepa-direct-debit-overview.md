---
title: SEPA tiesioginio debeto apžvalga
description: Bendrą mokėjimų eurais erdvę (SEPA) nustato Europos Komisija ir nurodo, kad visi elektroniniai mokėjimai laikomi vietiniais, nepaisant asmens, verslo arba organizacijos buvimo vietos šalies / regiono. Nacionaliniai ir tarptautiniai mokėjimai niekuo nesiskiria. SEPA apima 28 Europos Sąjungos (ES) valstybes nares bei Islandiją, Lichtenšteiną, Norvegiją, Šveicariją, Monaką ir San Mariną. SEPA padeda skurti bendrą mokėjimo operacijų rinką Europos ekonominėje erdvėje (EEE). Galiausiai, naudojant SEPA tikimasi sumažinti mokėjimo formatų, su kuriais dirba bankai, verslo įmonės ir asmenys, skaičių.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b1ec24c84d2b1a3dc88bf96ae6f52441b58a694
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188691"
---
# <a name="sepa-direct-debit-overview"></a>SEPA tiesioginio debeto apžvalga

[!include [banner](../includes/banner.md)]

Bendrą mokėjimų eurais erdvę (SEPA) nustato Europos Komisija ir nurodo, kad visi elektroniniai mokėjimai laikomi vietiniais, nepaisant asmens, verslo arba organizacijos buvimo vietos šalies / regiono. Nacionaliniai ir tarptautiniai mokėjimai niekuo nesiskiria. SEPA apima 28 Europos Sąjungos (ES) valstybes nares bei Islandiją, Lichtenšteiną, Norvegiją, Šveicariją, Monaką ir San Mariną. SEPA padeda skurti bendrą mokėjimo operacijų rinką Europos ekonominėje erdvėje (EEE). Galiausiai, naudojant SEPA tikimasi sumažinti mokėjimo formatų, su kuriais dirba bankai, verslo įmonės ir asmenys, skaičių.   

## <a name="what-is-the-goal-of-sepa-direct-debits"></a>Koks yra SEPA tiesioginio debeto tikslas?

SEPA tiesioginis debetas leidžia kreditoriui surinkti lėšas iš kliento banko sąskaitos, jei klientas kreditoriui suteikė pasirašytą įgaliojimą. Klientas pasirašo įgaliojimą, kuris įgalioja kreditorių surinkti mokėjimą ir nurodo kliento bankui jį išmokėti. 

SEPA tiesioginis debetas pirmą kartą sukuria mokėjimo priemonę, kurią galima naudoti nacionalinėms ir tarptautinėms tiesioginio debeto operacijoms eurais 32 SEPA šalyse / regionuose. 

Yra du galimi planai: SEPA pagrindinis tiesioginio debeto planas ir SEPA verslas verslui (B2B) tiesioginio debeto planas. Abiejuose planuose naudojamas toks pat failų formatas.

## <a name="what-is-the-core-direct-debit-scheme"></a>Kas yra pagrindinis tiesioginio debeto planas?
SEPA pagrindinis tiesioginio debeto planas yra bendrasis planas. Jam būdingi šie atributai:
-   Lėšos pervedamos eurais (nors banko sąskaitose lėšos gali būti laikomos kitomis valiutomis).
-   Klientas ir kreditorius turi turėti sąskaitas kredito institucijoje, priklausančioje SEPA.
-   Klientas turi pateikti kreditoriui pasirašytą įgaliojimą.
-   Įgaliojimai baigia galioti po 36 mėnesių nuo paskutinio inicijuoto surinkimo.
-   Kreditorius turi saugoti įgaliojimus tol, kol jie galioja – bent 14 mėnesių nuo paskutinio surinkimo.
-   Planas gali būti naudojamas vienam (vienkartiniam) arba pasikartojančiam tiesioginio debeto surinkimui.
-   Klientai turi teisę „neužduodant jokių klausimų" gauti grąžinimą iki aštuonių savaičių nuo sąskaitos debetavimo.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>Kas yra SEPA verslas verslui (B2B) tiesioginio debeto planas?
SEPA B2B tiesioginio debeto planas taikomas operacijoms verslas verslui ir remiasi SEPA pagrindiniu tiesioginio debeto planu. Pagrindiniai skirtumai:
-   SEPA B2B tiesioginio debeto planas neleidžiamas, kai klientas yra privatus asmuo (vartotojas).
-   Klientas neturi teisės gauti autorizuotos operacijos grąžinimo.
-   Klientų bankai turi įsitikinti, kad rinkimas yra leidžiamas, patikrindami pagal įgaliojimo informaciją. Klientų bankai ir klientai turi susitarti dėl patikrinimo, kuris bus taikomas kiekvienam tiesioginiam debetui.
-   Planas siūlo trumpesnį tiesioginio debeto atlikimo ir grąžinimo laikotarpį.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>Ar galiu naudoti COR1 planą tiesioginio debeto įgaliojimams?
Taip. COR1 planą SEPA tiesioginio debeto įgaliojimams galite naudoti Austrijoje, Belgijoje, Ispanijoje, Italijoje, Nyderlanduose, Prancūzijoje ir Vokietijoje. Planas suteikia trumpesnį išankstinio pranešimo laikotarpį kreditoriui renkant tiesioginio debeto mokėjimus.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>Kas yra tarptautiniai banko sąskaitų numeriai (IBAN) ir banko identifikavimo kodai (BIC)?
Tarptautinis banko sąskaitos numeris (IBAN) ir banko identifikavimo kodas (BIC) yra naudojami norint nustatyti bet kurią sąskaitą 32 SEPA šalyse / regionuose. Įveskite BIC lauke SWIFT kodas ir IBAN – lauke IBAN. Abu laukai yra Papildomos identifikacijos „FastTab‟, esančiame puslapio Banko sąskaitos skirtuke Banko sąskaita. Tai taikoma kreditoriaus banko sąskaitai ir kliento banko sąskaitai.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>Kur įvesti kreditoriaus identifikatorius (tiesioginio debeto ID)?
Naudojant SEPA kiekvieną kreditorių identifikuoja unikalus kreditoriaus identifikatorius. Šis identifikatorius leidžia klientui ir kliento bankui filtruoti kiekvieną tiesioginį debetą, tada apdoroti arba atmesti tiesioginį debetą pagal kliento nurodymus. Kreditoriai turi prašyti šio identifikatoriaus per savo banką. Šį identifikatorių įveskite juridinio subjekto banko sąskaitos lauke Tiesioginio debeto ID.

## <a name="what-are-mandates"></a>Kas yra įgaliojimai?
Klientas pasirašo įgaliojimą, kuris įgalioja kreditorių surinkti mokėjimą ir nurodo kliento bankui jį išmokėti. Klientas gali išduoti įgaliojimą popieriniu arba elektroniniu pavidalu. Pagal numatytuosius nustatymus įgaliojimas baigia galioti po 36 mėnesių nuo tiesioginio debeto paskutinio inicijavimo.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>Kur nurodyti SEPA tiesioginio debeto failo formatą (ISO 20022)?
SEPA duomenų formatai pagrįsti ISO 20022 pranešimų standartais. Konfigūruodami gautinų sumų mokėjimo būdus, pažymėsite žymės langelį Bendrosios elektroninės ataskaitos ir pasirinksite SEPA tiesioginio debeto formatą kaip eksportavimo formato konfigūraciją. Šį mokėjimo būdą naudojate, kai generuojate mokėjimo failą kliento mokėjimų žurnale.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>Kokiais failų formatais galiu sugeneruoti SEPA tiesioginio debeto mokėjimo failus?
SEPA tiesioginio debeto elektroninio mokėjimo failus galite generuoti toliau nurodytais formatais.
-   SEPA tiesioginio debeto mokėjimo failus galite generuoti PAIN.008.001.02 XML failo formatu Belgijoje, Ispanijoje, Italijoje, Nyderlanduose, Prancūzijoje ir Vokietijoje.
-   SEPA tiesioginio debeto mokėjimo failus galite generuoti PAIN.008.001.02 XML failų formatu Austrijoje ir PAIN.008.003.02 XML failų formatu Vokietijoje.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>Kaip naudojant SEPA tiesioginį debetą veikia grąžinimas?
Abiejuose SEPA tiesioginio debeto planuose klientai turi tam tikras teises į grąžinimą. Klientui leidžiama atšaukti bet kokias autorizuotas operacijas per aštuonias savaites nuo termino datos nenurodžius jokios priežasties. Neautorizuotų operacijų atveju laikotarpis pratęsiamas iki 13 mėnesių nuo termino datos. Bet kokie atlikti mokėjimai atšaukiami neautomatiškai: naudojant Klientų operacijų puslapio mygtuką Atšaukti mokėjimą.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
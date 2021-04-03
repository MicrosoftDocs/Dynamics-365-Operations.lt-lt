---
title: Įvykdyto ER formato duomenų šaltinių derinimas duomenų srautams ir transformacijai analizuoti
description: Šioje temoje paaiškinama, kaip galima derinti įvykdyto ER formato duomenų šaltinius, siekiant geriau suprasti sukonfigūruotą duomenų srautą ir transformaciją.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: bda81da80996d8cba38ac48e29c47ffef61d3bdb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562195"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>Įvykdyto ER formato duomenų šaltinių derinimas duomenų srautams ir transformacijai analizuoti

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Kai [konfigūruojate](tasks/er-format-configuration-2016-11.md) elektroninių ataskaitų (ER) sprendimą, kuris generuoja siunčiamus dokumentus, nurodote būdus, kuriais duomenys gaunami iš programos ir įvedami į sugeneruotą išvestį. Norint, kad ER sprendimo ciklo palaikymas būtų efektyvesnis, jūsų sprendimas turėtų būti sudarytas iš ER [duomenų modelio](general-electronic-reporting.md#DataModelComponent) ir jo [susiejimo](general-electronic-reporting.md#ModelMappingComponent) komponentų, taip pat ER [formato](general-electronic-reporting.md#FormatComponentOutbound) ir jo susiejimo komponentų, kad modelio susiejimas būtų būdingas konkrečiai programai, o kiti komponentai liktų nesusiję su programa. Todėl keli ER komponentai gali [paveikti](general-electronic-reporting.md#FormatComponentOutbound) duomenų įvedimo į sugeneruotą išvestį procesą.

Kartais sugeneruotos išvesties duomenys atrodo kitokie nei tokie patys duomenys programos duomenų bazėje. Tokiais atvejais reikia nustatyti, kuris ER komponentas yra atsakingas už duomenų transformaciją. ER duomenų šaltinio derintuvo funkcija reikšmingai sumažina šio tyrimo laiką ir išlaidas. Galite nutraukti ER formato vykdymą ir atidaryti duomenų šaltinio derintuvo sąsają. Joje galite naršyti esamus duomenų šaltinius ir pasirinkti vykdyti atskirą duomenų šaltinį. Šis neautomatinis vykdymas imituoja duomenų šaltinio vykdymą atliekant realų ER formato vykdymą. Rezultatas pateikiamas puslapyje, kur galite analizuoti gaunamus duomenis.

Norėdami įjungti duomenų šaltinio derinimo funkciją, ER vartotojo parametruose nustatykite parinkties **Įgalinti duomenų derinimą formato vykdymo metu** reikšmę į **Taip**. Tada kol vykdote ER formatą siunčiamiems dokumentams generuoti, galite pradėti derinti duomenų šaltinį. Taip pat galite naudoti parinktį **Pradėti derinimą**, kad inicijuotumėte ER formato, sukonfigūruoto [ER operacijų kūrimo įrankyje](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document), duomenų šaltinio derinimą.

Šioje temoje pateikiamos gairės, kaip inicijuoti vykdomų ER formatų duomenų šaltinio derinimą. Joje aiškinama, kaip informacija gali padėti suprasti duomenų srautą ir duomenų transformacijas. Šios temos pavyzdžiuose naudojamas tiekėjo mokėjimų apdorojimo verslo procesas.

## <a name="limitations"></a>Apribojimai

Duomenų šaltinio derintuvę galima naudoti norint pasiekti duomenis, esančius duomenų šaltiniuose, kurie yra naudojami ER formatuose, vykdomuose generuojant siunčiamus dokumentus. Jos negalima naudoti, norint derinti gaunamiems dokumentams analizuoti skirtų ER formatų duomenų šaltinius.

Šiuo metu toliau nurodyti ER formatų parametrai duomenų šaltiniui derinti nėra pasiekiami.

- Formatų transformacijos
- Formato ir susiejimo tikrinimo taisyklės
- Išraiškų įgalinimas
- Išsami informacija apie atminties duomenų rinkimą

## <a name="prerequisites"></a>Būtinieji komponentai

- Norėdami atlikti šioje temoje pateiktus pavyzdžius, turite turėti prieigą prie vieno iš toliau nurodytų [vaidmenų](../sysadmin/tasks/assign-users-security-roles.md).

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

- Įmonė turi būti nustatyta kaip **DEMF**.

- Norėdami atsisiųsti „Microsoft“ ER sprendimo komponentus, kurių reikia tiekėjo mokėjimams apdoroti, atlikite šios temos [1 priede](#appendix1) nurodytus veiksmus.
- Jei norite tiekėjo mokėjimo apdorojimui mokėtinas sumas parengti naudodami atsisiųstą ER sprendimą, atlikite šios temos [2 priede](#appendix2) nurodytus veiksmus.

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>Tiekėjo mokėjimo apdorojimas mokėjimo failui gauti

1. Norėdami apdoroti tiekėjo mokėjimus, atlikite šios temos [3 priede](#appendix3) nurodytus veiksmus.

    ![Vykdomas tiekėjo mokėjimo apdorojimas](./media/er-data-debugger-process-payment.png)

2. Atsisiųskite ir įrašykite ZIP failą savo vietiniame kompiuteryje.
3. Išskleiskite iš ZIP failo mokėjimo failą **ISO20022 Credit transfer.xml**.
4. Atidarykite išskleistą mokėjimo failą naudodami XML failų peržiūros programą.

    Mokėjimo faile nurodytame tiekėjo banko sąskaitos tarptautiniame banko sąskaitos numeryje (IBAN) nėra tarpų. Todėl ji skiriasi nuo reikšmės [įvestos](#enteredIBANcode) puslapyje **Bankų kodai**.

    ![IBAN kodas be tarpų](./media/er-data-debugger-payment-file.png)

    Norėdami sužinoti, kuris ER sprendimo komponentas naudojamas IBAN kodo tarpams pašalinti, galite naudoti ER duomenų šaltinio derintuvę.

## <a name="turn-on-data-source-debugging"></a>Duomenų šaltinio derinimo įjungimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Parinkties **Įgalinti duomenų derinimą formato vykdymo metu** reikšmę nustatykite į **Taip**.

    > [!NOTE]
    > Šis parametras yra susijęs su konkrečiu vartotoju ir įmone.

    ![Vartotojo parametrų dialogo langas](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>Tiekėjo mokėjimą apdorojimas derinimui

1. Norėdami apdoroti tiekėjo mokėjimus, atlikite šios temos [3 priede](#appendix3) nurodytus veiksmus.
2. Pranešimo lange pasirinkite **Taip**, kad patvirtintumėte, jog norite pertraukti tiekėjo mokėjimo apdorojimą ir vietoj to pradėti duomenų šaltinio derinimą puslapyje **Duomenų šaltinių derinimas**.

    ![Patvirtinimo pranešimo langas](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>Duomenų šaltinius, naudojamų mokėjimui apdoroti, derinimas

### <a name="debug-the-model-mapping"></a>Modelio susiejimo derinimas

1. Puslapyje **Duomenų šaltinių derinimas** esančioje veiksmų srityje pasirinkite **Modelio susiejimas**, kad pradėtumėte derinti iš šio ER komponento.
2. Kairėje esančioje duomenų šaltinio srityje pasirinkite duomenų šaltinį **\$notSentTransactions**, tada pasirinkite **Skaityti visus įrašus**.

    Jei norite, kad iš pasirinkto duomenų šaltinio būtų skaitomas atitinkamas skaičius įrašų, galite pasirinkti **Skaityti 1 įrašą**, **Skaityti 10 įrašų**, **Skaityti 100 įrašų** arba **Skaityti visus įrašus**. Tokiu būdu galite imituoti prieigą prie duomenų šaltinio iš vykdomo ER formato.

3. Dešinėje esančioje duomenų srityje pasirinkite **Išplėsti viską**.

    Galite matyti, kad pasirinktame duomenų šaltinyje, kurio tipas – **Įrašų sąrašas**, yra vienas įrašas.

4. Išplėskite duomenų šaltinį **\$notSentTransactions** ir pasirinkite įterptąjį metodą **vendBankAccountInTransactionCompany()**.
5. Išplėskite metodą **vendBankAccountInTransactionCompany()** ir pasirinkite įterptąjį lauką **IBAN**.
6. Pasirinkti **Gauti reikšmę**.

    Jei norite, kad būtų nuskaitoma pasirinkto duomenų šaltinio pasirinktos lauko reikšmė, galite pasirinkti **Gauti reikšmę**. Tokiu būdu galite imituoti prieigą prie šio lauko iš vykdomo ER formato.

7. Pažymėkite **Išplėsti viską**.

    ![IBAN lauko reikšmė modelio susiejime](./media/er-data-debugger-debugging-model-mapping.png)

    Kaip matote, modelio susiejimas neatsako už pašalintus tarpus, nes tarpai yra IBAN kode, kurį jis grąžina tiekėjo banko sąskaitai. Todėl turite tęsti duomenų šaltinio derinimą.

### <a name="debug-the-format-mapping"></a>Formato susiejimo derinimas

1. Puslapyje **Duomenų šaltinių derinimas** esančioje veiksmų srityje pasirinkite **Formato susiejimas**, kad galėtumėte tęsti derinimą iš šio ER komponento.
2. Pasirinkite duomenų šaltinį **\$PaymentByDebtor**, tada – **Skaityti visus įrašus**.
3. Išplėskite **\$PaymentByDebtor**.
4. Išplėskite **\$PaymentByDebtor.Lines**, tada pasirinkite **Skaityti visus įrašus**.
5. Išplėskite **\$PaymentByDebtor.Lines.CreditorAccount**.
6. Išplėskite **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, tada pasirinkite **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.
7. Pasirinkti **Gauti reikšmę**.
8. Pažymėkite **Išplėsti viską**.

    ![IBAN lauko reikšmė formato susiejime](./media/er-data-debugger-debugging-format-mapping.png)

    Kaip matote, formato susiejimo duomenų šaltiniai neatsako už pašalintus tarpus, nes tarpai yra IBAN kode, kurį jie grąžina tiekėjo banko sąskaitai. Todėl turite tęsti duomenų šaltinio derinimą.

### <a name="debug-the-format"></a>Formato derinimas

1. Puslapyje **Duomenų šaltinių derinimas** esančioje veiksmų srityje pasirinkite **Formatas**, kad galėtumėte tęsti derinimą iš šio ER komponento.
2. Išplėskite formato elementus, kad pasirinktumėte **ISO20022CTReports** \> **XMLHeader** \> **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf**, tada pasirinkite **Skaityti visus įrašus**.
3. Išplėskite formato elementus, kad pasirinktumėte **ISO20022CTReports** \> **XMLHeader** \> **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, tada pasirinkite **Skaityti visus įrašus**.
4. Išplėskite formato elementus, kad pasirinktumėte **ISO20022CTReports** \> **XMLHeader** \> **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, tada pasirinkite **Gauti reikšmę**.
5. Pažymėkite **Išplėsti viską**.

    ![IBAN lauko reikšmė formate](./media/er-data-debugger-debugging-format.png)

   Kaip matote, formato susiejimas neatsako už pašalintus tarpus, nes tarpai yra IBAN kode, kurį jis grąžina tiekėjo banko sąskaitai. Todėl **BankIBAN** elementas sukonfigūruotas naudoti formato transformaciją, kuri pašalina tarpus.

6. Uždarykite duomenų šaltinio derintuvę.

### <a name="review-the-format-transformations"></a>Formato transformacijų peržiūra

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapyje **Konfigūracijos** pasirinkite **Mokėjimo modelis** \> **ISO20022 kredito pervedimas**.
3. Pasirinkite **Kūrimo įrankis**, tada išplėskite formato elementus, kad pasirinktumėte **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.

    ![BankIBAN elementas puslapyje Formato kūrimo įrankis](./media/er-data-debugger-referred-transformation.png)

    Kaip matote, **BankIBAN** elementas sukonfigūruotas naudoti transformaciją **pašalinti ne raidinius-skaitinius simbolius**.

4. Pasirinkite skirtuką **Transformacijos**.

    ![BankIBAN elemento skirtukas Transformacijos](./media/er-data-debugger-transformation.png)

    Kaip matote, transformacija **pašalinti ne raidinius-skaitinius simbolius** sukonfigūruota naudoti išraišką, kuri pašalina tarpus pateiktoje teksto eilutėje.

## <a name="start-to-debug-in-the-operation-designer"></a>Derinimo operacijų kūrimo įrankyje pradžia

Kai sukonfigūruojate ER formato juodraštinę versiją, kurią galima tiesiogiai paleisti iš operacijų kūrimo įrankio, duomenų šaltinio derintuvę galite pasiekti veiksmų srityje pasirinkdami **Pradėti derinimą**.

![Mygtukas Pradėti derinimą puslapyje Formato kūrimo įrankis](./media/er-data-debugger-run-from-designer.png)

Redaguojamo ER formato susiejimą ir komponentus galima derinti.

## <a name="start-to-debug-in-the-model-mapping-designer"></a>Derinimo modelio susiejimų kūrimo įrankyje pradžia

Kai sukonfigūruojate ER modelio susiejimą, kurį galima paleisti iš puslapio **Modelio susiejimas**, duomenų šaltinio derintuvę galite pasiekti veiksmų srityje pasirinkdami **Pradėti derinimą**.

![Mygtukas Pradėti derinimą puslapyje Modelio susiejimų kūrimo įrankis](./media/er-data-debugger-run-from-designer-mapping.png)

Redaguojamo ER susiejimo modelio susiejimo komponentą galima derinti.

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>1 priedas. ER sprendimo gavimas

### <a name="download-an-er-solution"></a>ER sprendimo atsisiuntimas

Jei apdorojamo tiekėjo elektroninio mokėjimo failui generuoti norite naudoti ER sprendimą, galite [atsisiųsti](download-electronic-reporting-configuration-lcs.md) ER mokėjimo formatą **ISO20022 kredito pervedimas**, kurį galima gauti iš bendrai naudojamo turto bibliotekos, esančios „Microsoft Dynamics Lifecycle Services (LCS)“, arba iš bendrosios saugyklos.

![ER mokėjimo formato atsisiuntimas puslapyje Konfigūracijos saugykla](./media/er-data-debugger-import-from-repo.png)

Kartu su pasirinktu ER formatu, kaip ER sprendimo **ISO20022 kredito pervedimas** dalis, į „Microsoft Dynamics 365 Finance“ egzempliorių turi būti automatiškai importuotos toliau nurodytos [konfigūracijos](general-electronic-reporting.md#Configuration).

- [ER duomenų modelio konfigūracija](general-electronic-reporting.md#DataModelComponent) **Mokėjimo modelis**
- [ER formato konfigūracija](general-electronic-reporting.md#FormatComponentOutbound) **ISO20022 kredito pervedimas**
- [ER modelio susiejimo konfigūracija](general-electronic-reporting.md#ModelMappingComponent) **Mokėjimo modelio susiejimas 1611**
- ER modelio susiejimo konfigūracija **Mokėjimo modelio susiejimas su paskirtimi ISO20022**

Šias konfigūracijas galite rasti ER sistemos puslapyje **Konfigūracijos** (**Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**).

![Puslapyje Konfigūracijos importuotos konfigūracijos](./media/er-data-debugger-configurations.png)

Jeigu konfigūracijos medyje nėra anksčiau išvardytų konfigūracijų, turite jas atsisiųsti rankiniu būdu iš LCS bendrai naudojamo turto bibliotekos taip pat, kaip atsisiuntėte ER mokėjimo formatą **ISO20022 kredito pervedimas**.

### <a name="analyze-the-downloaded-er-solution"></a>Atsisiųsto ER sprendimo analizė

#### <a name="review-the-model-mapping"></a>Modelio susiejimo peržiūra

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Pasirinkite **Mokėjimo modelis** \> **Mokėjimo modelio susiejimas 1611**.
3. Pasirinkite **Dizaino įrankis**.
4. Pasirinkite susiejimo įrašą **Mokėjimo modelio susiejimas ISO20022 CT**.
5. Pasirinkite **Kūrimo įrankis**, tada peržiūrėkite atidarytą modelio susiejimą.

    Atkreipkite dėmesį, kad duomenų modelio laukas **Mokėjimai** yra susietas su duomenų šaltiniu **\$notSentTransactions**, kuris grąžina apdorojamų tiekėjo mokėjimo eilučių sąrašą.

    ![Laukas Mokėjimai puslapyje Modelių susiejimo kūrimo įrankis](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>Formato susiejimo peržiūra

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Pasirinkite **Mokėjimo modelis** \> **ISO20022 kredito pervedimas**.
3. Pasirinkite **Dizaino įrankis**.
4. Skirtuke **Susiejimas** peržiūrėkite atidarytą formato susiejimą.

    Atkreipkite dėmesį, kad failo **ISO20022CTReports** \> **XMLHeader** elementas **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf** yra susietas su duomenų šaltiniu **\$PaymentByDebtor**, kuris yra sukonfigūruotas grupuoti duomenų modelio lauko **Mokėjimai** įrašus.

    ![PmtInf elementas puslapyje Formato kūrimo įrankis](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>Formato peržiūra

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Pasirinkite **Mokėjimo modelis** \> **ISO20022 kredito pervedimas**.
3. Pasirinkite **Kūrimo įrankis**, tada peržiūrėkite atidarytą formatą.

    Atkreipkite dėmesį, kad formato elementas, esantis **Dokumentas** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, yra sukonfigūruotas tiekėjo sąskaitos IBAN kodui įvesti mokėjimo faile.

    ![BankIBAN elementas puslapyje Formato kūrimo įrankis](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>2 priedas. Mokėtinų sumų konfigūravimas

### <a name="modify-a-vendor-property"></a>Tiekėjo ypatybės modifikavimas

1. Eikite į **Mokėtinos sumos** \> **Tiekėjai** \> **Visi tiekėjai**.
2. Pasirinkite tiekėją **DE-01002**, tada veiksmų srities skirtuko **Tiekėjas** grupėje **Nustatymas** pasirinkite **Bankų sąskaitos**.
3. „FastTab“ konteineryje **Identifikacija**, lauke **IBAN**, <a name="enteredIBANcode"></a>įveskite **GB33 BUKB 2020 1555 5555 55**.
4. Pasirinkite **Įrašyti**.

![Puslapyje Tiekėjo banko sąskaitos nustatytas IBAN laukas](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>Mokėjimo būdo nustatymas

1. Eikite į **Mokėtinos sumos** \> **Mokėjimo nustatymas** \> **Mokėjimo būdai**.
2. Pasirinkite mokėjimo būdą **SEPA CT**.
3. „FastTab“ konteineryje **Failų formatai**, dalyje **Failų formatai** parinkties **Bendras elektroninis eksportavimo formatas** reikšmę nustatykite kaip **Taip**.
4. Lauke **Eksportuoti formato konfigūraciją** pasirinkite ER formatą **ISO20022 kredito pervedimas**.
5. Pasirinkite **Įrašyti**.

![Failo formato parametrai puslapyje Mokėjimo būdai](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>Tiekėjo mokėjimo įtraukimas

1. Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.
2. Įtraukite naują mokėjimų žurnalą.
3. Pasirinkite **Eilutės** ir įtraukite naują mokėjimo eilutę.
4. Lauke **Sąskaita** įveskite tiekėją **DE-01002**.
5. Lauke **Debetas** įveskite reikšmę.
6. Lauke **Mokėjimo būdas** pasirinkite **SEPA CT**.
7. Pasirinkite **Įrašyti**.

![Tiekėjo mokėjimai įtraukti puslapyje Tiekėjo mokėjimai](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>3 priedas. Tiekėjo mokėjimo apdorojimas

1. Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.
2. Puslapyje **Tiekėjo mokėjimų žurnalas** pasirinkite anksčiau sukurtą mokėjimų žurnalą, tada pasirinkite **Eilutės**.
3. Pasirinkite mokėjimo eilutę ir pasirinkite **Mokėjimo būsena** \> **Nėra**.
4. Pasirinkite **Generuoti mokėjimus**.
5. Lauke **Mokėjimo būdas** pasirinkite **SEPA CT**.
6. Lauke **Banko sąskaita** įveskite **DEMF OPER**.
7. Dialogo lange **Generuoti mokėjimus** pasirinkite **Gerai**.
8. Dialogo lange **Elektroninių ataskaitų parametrai** pasirinkite **Gerai**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
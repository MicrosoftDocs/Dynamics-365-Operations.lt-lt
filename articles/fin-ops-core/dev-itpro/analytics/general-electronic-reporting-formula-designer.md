---
title: Elektroninių ataskaitų (ER) formulių kūrimo įrankis
description: Šioje temoje pateikiama informacija apie tai, kaip naudoti elektroninėse ataskaitose (ER) formulių kūrimo įrankį.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d96fe041fd0ffb292909c1e724068efebe0184b9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682654"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Elektroninių ataskaitų (ER) formulių kūrimo įrankis

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip naudoti formulių kūrimo įrankį teikiant elektronines ataskaitas (ER). Kurdami ER konkretaus elektroninio dokumento formatą, naudodami formules galite transformuoti duomenis, kad jie atitiktų dokumento įvykdymo ir formatavimo reikalavimus. Šios formulės panašios į „Microsoft Excel“ formules. Formulėse palaikomos įvairių tipų funkcijos: tekstinės, datos ir laiko, matematinės, loginės, informacijos, duomenų tipo konvertavimo, ir kitos konkrečios verslo srities funkcijos.

## <a name="formula-designer-overview"></a>Formulių kūrimo įrankio apžvalga

ER palaiko formulių kūrimo įrankį. Todėl kūrimo metu galite konfigūruoti išraiškas, kurias galima naudoti tolesnių užduočių vykdymo metu.

- Transformuokite iš programos duomenų bazės gautus duomenis, kurie turėtų būti įvesti į ER duomenų modelį, sukurtą kaip ER formatų duomenų šaltinis. (Pavyzdžiui, toks transformavimas gali būti filtravimas, grupavimas ir duomenų tipo konvertavimas.)
- Duomenų, kurie turi būti siunčiami į generuojamą elektroninį dokumentą pagal konkretaus ER formato maketą ir sąlygas, formatavimas. (Pvz., formatuoti galima pagal norimą kalbą ar kultūrą, arba kodavimą).
- Elektroninių dokumentų kūrimo proceso kontroliavimas. (Pavyzdžiui, pagal apdorojamus duomenis išraiškomis galima įjungti ar išjungti tam tikrus išvedamus formato elementus. Jomis taip pat galima pertraukti dokumentų kūrimo procesą, ar pateikti pranešimus vartotojams.)

Puslapį **Formulių konstruktorius** galite atidaryti atlikdami bet kurį iš tolesnių veiksmų.

- Susiejus duomenų šaltinio elementus su duomenų modelio komponentais.
- Susiejus duomenų šaltinio elementus su formato komponentais.
- Atlikus apskaičiuotų laukų, kurie yra duomenų šaltinių dalis, priežiūrą.
- Nurodžius vartotojo įvesties parametrų matomumo sąlygas.
- Sukūrus formato pakeitimus.
- Nurodžius formato komponentus įgalinančių sąlygas.
- Nurodžius formato FILE komponentų failų vardus.
- Nurodžius proceso kontrolės tikrinimų sąlygas.
- Nurodžius proceso kontrolės tikrinimų pranešimo tekstą.

## <a name="data-binding"></a><a name="Binding"></a>Duomenų susiejimas

ER formulių kūrimo įrankį galima naudoti apibrėžiant išraišką, kuri transformuoja iš duomenų šaltinių gautus duomenis, kad tuos duomenis būtų galima įvesti į duomenų vartotoją vykdymo metu tokiais būdais:

- iš programos duomenų šaltinių ir vykdymo laiko parametrų į ER duomenų modelį;
- iš ER duomenų modelio į ER formatą;
- iš programos duomenų šaltinių ir vykdymo laiko parametrų į ER formatą.

Tolesnė iliustracija rodo šio tipo išraiškos kūrimą. Šiame pavyzdyje išraiška suapvalina „Intrastat“ lentelės lauko **Intrastat.AmountMST** reikšmę iki dviejų skaičių po kablelio ir pateikia suapvalintą reikšmę.

[![Duomenų susiejimo išraiška](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Tolesnėje iliustracijoje parodyta, kaip galima naudoti šio tipo išraišką. Šiame pavyzdyje sukurtos išraiškos rezultatas įvedamas į duomenų modelio **Mokesčių ataskaitos modelis** komponentą **Transaction.InvoicedAmount**.

[![Naudojama duomenų susiejimo išraiška](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Vykdymo metu sukurta formulė `ROUND (Intrastat.AmountMST, 2)` kiekvieno „Intrastat“ lentelės įrašo lauko **AmountMST** reikšmę suapvalina iki dviejų skaičių po kablelio. Suapvalintą reikšmę ji tada įveda į duomenų modelio **Mokesčių ataskaitos** komponentą **Transaction.InvoicedAmount**.

## <a name="data-formatting"></a><a name="Transformation"></a>Duomenų formatavimas

ER formulių kūrimo įrankį galima naudoti apibrėžiant išraišką, kuri formatuoja iš duomenų šaltinių gautus duomenis, kad tuos duomenis būtų galima siųsti kaip generuojamo elektroninio dokumento dalį. Galite turėti formatavimą, kuris turi būti taikomas kaip įprasta pakartotinai naudojama formato taisyklė. Tokiu atveju šį formatavimą galite vienu kartu įvesti į formato konfigūraciją kaip įvardytąją transformaciją, kuri turi formatavimo išraišką. Tada šią įvardytąją transformaciją galima susieti su daugeliu formato komponentų, kurių išvedami duomenys turi būti formatuojami pagal jūsų sukurtą formatavimo išraišką.

Tolesnė iliustracija rodo šio tipo pakeitimo kūrimą. Šiame pavyzdyje transformacija **TrimmedString** sutrumpina duomenų tipo *Eilutė* duomenis pašalindama priekinius ir galinius tarpus. Tada ji pateikia sutrumpintą eilutės reikšmę.

[![Transformacija](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Tolesnė iliustracija parodo, kaip galima naudoti tipo transformaciją. Šiame pavyzdyje keletas formato komponentų vykdymo metu siunčia tekstą kaip išeigą į generuojamą elektroninį dokumentą. Visi šie formato keitimai nurodo transformaciją **TrimmedString** pagal pavadinimą.

[![Naudojama transformacija](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Kai formato komponentai, pvz., komponentas **partyName** ankstesnėje iliustracijoje, nurodo transformaciją **TrimmedString**, transformacija į generuojamą elektrinį dokumentą kaip išeigą siunčia tekstą. Šiame tekste nėra priekinių ir galinių tarpų.

Jei formatavimą būtina taikyti atskirai, galite jį nustatyti kaip atskirą konkretaus formato komponento susiejimo išraišką. Tolesnė iliustracija rodo šio tipo išraišką. Šiame pavyzdyje formato komponentas **partyType** yra susietas su duomenų šaltiniu per išraišką, kuri konvertuoja iš duomenų šaltinyje esančio lauko **Model.Company.RegistrationType** gaunamus duomenis į tekstą didžiosiomis raidėmis. Tada išraiška šį tekstą kaip išeigą siunčia į elektroninį dokumentą.

[![Formatavimo taikymas atskiram komponentui](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>Proceso eigos valdymas

ER formulių dizaino įrankis gali būti naudojamas apibrėžiant išraiškas, kurios valdo elektroninių dokumentų generavimo proceso eigą. Galite atlikti šias užduotis:

- Apibrėžkite sąlygas, kurios lemia, kada sustabyti dokumentų kūrimo procesą.
- Nurodykite išraiškas, kurios kuria vartotojams skirtus pranešimus apie sustabdytus procesus arba pateikia vykdymo žurnalo pranešimus apie besitęsiantį ataskaitų generavimo procesą.
- Nurodykite generuojamų elektroninių dokumentų failų pavadinimus ir kontroliuokite jų kūrimo sąlygas.

Kiekviena proceso eigos valdymo taisyklė sukuriama kaip atskiras tikrinimo elementas. Tolesnė iliustracija rodo šio tipo tikrinimą. Čia pateikiamas šiame pavyzdyje esančios konfigūracijos paaiškinimas:

- Tikrinimas įvertinamas, kai generuojant XML failą sukuriamas mazgas **INSTAT**.
- Jei operacijų sąrašas yra tuščias, tikrinimas sustabdo vykdymo procesą ir pateikia **FALSE**.
- Tikrinimas pateikia klaidos pranešimą, kuriame yra žymės SYS70894 tekstas vartotojo pageidaujama kalba.

[![Tikrinimas](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER formulių kūrimo įrankį taip pat galima naudoti ir generuojamo elektroninio dokumento failo pavadinimui generuoti bei failų kūrimo procesui kontroliuoti. Tolesnė iliustracija rodo šio tipo proceso eigos valdymo kūrimą. Čia pateikiamas šiame pavyzdyje esančios konfigūracijos paaiškinimas:

- Duomenų šaltinio **model.Intrastat** įrašų sąrašas padalijamas į paketus. Kiekviename pakete yra iki 1000 įrašų.
- Išeiga sukuria „zip“ failą, kuriame yra po vieną failą XML formatu kiekvienam sukurtam paketui.
- Išraiška pateikia generuojamų elektroninių dokumentų failo pavadinimą sujungdama failo pavadinimą ir jo plėtinį. Antrojo paketo ir visų vėlesnių paketų failo varde kaip priedėlis nurodytas paketo ID.
- Išraiška įgalina (pateikdama reikšmę **TRUE**) paketų, kuriuose yra bent vienas įrašas, failų kūrimo procesą.

[![Proceso eigos valdymas](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Dokumento turinio kontrolė

ER formulių kūrimo įrankį galima naudoti konfigūruojant išraiškas, kontroliuojančias duomenis, įtraukiamus į generuojamus elektroninius dokumentus vykdymo metu. Pagal išraiškas įjungiama arba išjungiama tam tikrų formato elementų išvestis, atsižvelgiant į apdorojamus duomenis ir sukonfigūruotą logiką. Vieno formato elemento išraiškas galima įvesti lauke **Įjungta** skirtuke **Susiejimas** puslapyje **Operacijų kūrimo įrankis**. Išraiškas galite įvesti kaip loginę sąlygą, kuri grąžina *Bulio logikos* reikšmę:

- Jei sąlyga grąžina **teisinga**, paleidžiamas dabartinis formato elementas.
- Jei sąlyga grąžina **klaidinga**, praleidžiamas dabartinis formato elementas.

Tolesnė iliustracija nurodo šio tipo išraiškas. (**ISO20022 kredito perdavimo (NO)** formato konfigūracijos, kurią teikia „Microsoft“, versija 11.12.11 naudojama kaip pavyzdys.) **XMLHeader** formato komponentas sukonfigūruotas apibrėžti kredito pervedimo pranešimo struktūrą pagal ISO 20022 XML pranešimo standartus. Formato komponentas **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** konfigūruojamas į generuojamą pranešimą įtraukiant XML elementą **Ustrd** ir įtraukiant pavedimo informaciją nestruktūriniu formatu kaip toliau pateikiamų XML elementų tekstą.

- Komponentas **PaymentNotes** naudojamas generuojant mokėjimo pastabų tekstą.
- Nustačius komponentą **DelimitedSequence**, sugeneruojami kableliais atskirti sąskaitų faktūrų numeriai, naudojami apmokant esamą kredito pervedimą.

[![„PaymentNotes“ ir „DelimitedSequence“ komponentai](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> Komponentai **PaymentNotes** ir **DelimitedSequence** pažymėti klaustukais. Klaustukas rodo, kad komponento naudojimas yra sąlyginis. Šiuo atveju komponentai naudojami remiantis šiais kriterijais:
>
> - Išraiška `@.PaymentsNotes <> ""`, kurios apibrėžtis skirta komponentui **PaymentNotes**, įgalina (gavus **TEISINGA**) XML elementą **Ustrd** užpildymui mokėjimo pastabų tekstu, jei dabartinio kredito pervedimo tekstas nėra tuščias.
>
>    [![„PaymentNotes“ komponento išraiška](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - Išraiška `@.PaymentsNotes = ""`, kurios apibrėžtis skirta komponentui **DelimitedSequence**, įgalina (gavus **TEISINGA**) XML elementą **Ustrd** užpildymui sąskaitų faktūrų kableliais atskirtų numerių sąrašais, naudojamais  apmokant esamą kredito pervedimą, jei to kredito pervedimo mokėjimo pastabų tekstas yra tuščias.
>
>    [![„DelimitedSequence“ komponento išraiška](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> Remiantis šia sąranka, į kiekvieno skolininko mokėjimo generuojamą pranešimą, XML elementą **Ustrd** bus įtrauktas arba mokėjimo pastabų tekstas, arba, kai toks tekstas yra tuščias, kableliais atskirtų sąskaitų faktūrų numerių, naudojamų atliekant šį mokėjimą, tekstas.

## <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Sukonfigūruotų formulių tikrinimas

Puslapyje **Formulių kūrimo įrankis** pasirinkite **Bandymas**, kad patikrintumėte, kaip veikia sukonfigūruota formulė.

[![Bandymo pasirinkimas tikrinant formulę](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Kai reikia argumentų formulės reikšmių, galite atidaryti dialogo langą **Tikrinimo išraiškos** puslapyje **Formulių kūrimo įrankis**. Daugeliu atvejų šiuos argumentus reikia nustatyti neautomatiniu būdu, nes sukonfigūruoti susiejimai nepaleidžiami kūrimo metu. Skirtuko **Bandymo rezultatas** puslapyje **Formulių kūrimo įrankis** rodomas sukonfigūruotos formulės vykdymo rezultatas.

Toliau pateikiamas pavyzdys, kaip patikrinti formulę, kuri sukonfigūruota užsienio prekybos domenui, kad įsitikintumėte, jog „Intrastat“ prekės kode yra tik skaitmenys.

Kai išbandote šią formulę, galite naudoti dialogo langą **Tikrinimo išraiška** norėdami nurodyti „Intrastat“ prekės testavimo kodo vertę.

[![„Intrastat“ prekės testavimo kodo nurodymas](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Nurodę „Intrastat“ prekės kodą ir pasirinkę **Gerai**, skirtuko **Bandymo rezultatas** puslapyje **Formulės kūrimo įrankis** rodomas sukonfigūruotos formulės vykdymo rezultatas. Tada galite įvertinti, ar rezultatas yra priimtinas. Jei rezultatas nėra priimtinas, galite atnaujinti formulę ir tikrinti ją dar kartą.

[![Bandymo rezultatas](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Kai kurios formulės negali būti išbandytos kūrimo metu. Pvz., formulė gali grąžinto duomenų tipo, kurio negalima parodyti skirtuke **Bandymo rezultatas**, rezultatą. Tokiu atveju parodomas klaidos pranešimas, kuriame nurodoma, kad formulė negali būti išbandyta.

[![Klaidos pranešimas](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų formulių kalba](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
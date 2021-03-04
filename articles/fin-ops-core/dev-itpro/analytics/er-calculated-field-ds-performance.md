---
title: ER sprendimų našumo didinimas įtraukiant parametrizuotų duomenų šaltinių APSKAIČIUOTAS LAUKAS
description: Šioje temoje paaiškinama, kaip galite padėti padidinti elektroninių ataskaitų (ER) sprendimų našumą įtraukdami parametrizuotų duomenų šaltinių APSKAIČIUOTAS LAUKAS.
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 940b696a06fb46bcd0557f059327cd4340448137
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681285"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>ER sprendimų našumo didinimas įtraukiant parametrizuotų duomenų šaltinių APSKAIČIUOTAS LAUKAS

[!include [banner](../includes/banner.md)]

Šioje temoje aiškinama, kaip galima naudoti vykdomų [elektroninių ataskaitų (ER)](general-electronic-reporting.md) formatų [našumo sekimo](trace-execution-er-troubleshoot-perf.md) informaciją našumo gerinimui sukonfigūruojant parametruojamą duomenų šaltinį **Apskaičiuotas laukas**.

Kurdami ER konfigūracijas, kuriomis naudojantis generuojami verslo dokumentai, nurodote būdą, kuriuo naudodamiesi gaunate duomenis iš programos, ir įvedate jį į sugeneruotą išvestį. Sukūrę parametrizuotą ER duomenų šaltinį **Apskaičiuotas laukas**, galite sumažinti duomenų bazės skambučių skaičių ir žymiai sumažinti laiką ir išlaidas, susijusias su ER formato vykdymo informacijos rinkimu.

## <a name="prerequisites"></a>Būtinieji komponentai

- Norėdami atlikti šioje temoje pateiktus pavyzdžius, turite turėti prieigą prie vieno iš toliau nurodytų [vaidmenų](../sysadmin/tasks/assign-users-security-roles.md).

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

- Įmonė turi būti nustatyta kaip **DEMF**.
- Norėdami atsisiųsti pavyzdinio „Microsoft“ ER sprendimo, kurio reikia šios temos pavyzdžiams įvykdyti, komponentus, atlikite šios temos [1 priede](#appendix1) nurodytus veiksmus.
- Norėdami sukonfigūruoti minimalų ER parametrų rinkinį, kurio reikia norint naudoti ER sistemą, kad būtų galima pagerinti pavyzdinio „Microsoft“ ER sprendimo našumą, atlikite šios temos [2 priede](#appendix2) nurodytus veiksmus.

## <a name="import-the-sample-er-solution"></a>Pavyzdinio ER sprendimo importavimas

Tarkime, kad turite sukurti ER sprendimą, kad būtų sugeneruota nauja ataskaita, kurioje pateikiamos tiekėjo operacijos. Šiuo metu pasirinkto tiekėjo operacijas rasite puslapyje **Tiekėjo operacijos** (eikite į **Mokėtina suma** \> **Tiekėjai** \> **Visi tiekėjai**, pasirinkite tiekėją, paskui veiksmų srities skirtuko **Tiekėjas** grupėje **Operacijos** pasirinkite **Operacijos**). Tačiau norite turėti visas tiekėjo operacijas viename elektroniniame dokumente XML formatu. Šį sprendimą sudaro kelios ER konfigūracijos, apimančios reikiamą duomenų modelį, modelio susiejimą ir formato komponentus.

Pirmas veiksmas yra importuoti pavyzdinį ER sprendimą, kad būtų galima sugeneruoti tiekėjo operacijų ataskaitą.

1. Prisijunkite prie jūsų įmonei sukurto „Microsoft Dynamics 365 Finance” egzemplioriaus.
2. Šioje temoje kursite ir modifikuosite pavyzdinės įmonės **„Litware, Inc.“** konfigūracijas. Įsitikinkite, kad šis konfigūracijos teikėjas buvo įtrauktas į jūsų „Finance“ egzempliorių ir pažymėtas kaip aktyvus. Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.
4. Puslapyje **Konfigūracijos** importuokite į „Finance” kaip būtinąjį komponentą atsisiųstas ER konfigūracijas tokia tvarka: duomenų modelis, modelio susiejimas, formatas. Kurdami kiekvieną konfigūraciją atlikite toliau nurodytus veiksmus.

    1. Veiksmų srityje pasirinkite **Pakeisti** \> **Įkelti iš XML failo**.
    2. Paspaudę **Naršyti** pasirinkite ER konfigūracijos failą XML formatu.
    3. Pasirinkite **Gerai**.

![Puslapyje Konfigūracijos importuotos konfigūracijos](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>Pavyzdinio ER sprendimo peržiūra

### <a name="review-the-model-mapping"></a>Modelio susiejimo peržiūra

1. Puslapyje **Konfigūravimai**, konfigūravimo medyje, išplėskite **Našumo didinimo modelis** ir pasirinkite **Našumo didinimo susiejimas**.
2. Veiksmų srityje pasirinkite **Dizaino įrankis**.
3. Veiksmų srities puslapyje **Duomenų šaltinio susiejimo modelis** pasirinkite **Dizaino įrankis**.

    Šis ER modelio susiejimas sukurtas toliau nurodytiems veiksmams atlikti.

    - Raskite tiekėjo operacijų, saugomų lentelėje VendTrans, sąrašą (duomenų šaltinis **Operacija**).
    - Lentelėje VendTable raskite kiekvienos operacijos tiekėjo įrašą, kuriame buvo užregistruota operacija (duomenų šaltinis **\#Tiekėjas**)

    > [!NOTE]
    > Duomenų šaltinis **\#Tiekėjas** sukonfigūruotas, kad būtų galima gauti atitinkamą tiekėjo įrašą naudojant esamą ryšį „daugelis su vienu“ **\@.'\>Relations'.VendTable\_AccountNum**.

    Modelio žemėlapio nustatymas šiame konfigūravime įgyvendina pagrindinius duomenų modelius bet kuriems ER formatams sukurtiems šiam modeliui ir vykdomiems „Finance“. Todėl duomenų šaltinio **Operacija** turinys tampa prieinamas ER formatams, pvz., abstraktiems **modelio** duomenų šaltiniams.

    ![Duomenų šaltinis Operacija puslapyje Modelio susiejimo dizaino įrankis](media/er-calculated-field-ds-performance-mapping-1.png)

4. Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.
5. Uždarykite puslapį **Duomenų šaltinio susiejimo modelis**.

### <a name="review-format"></a>Formato peržiūra

1. Puslapyje **Konfigūravimai**, konfigūravimo medyje, išplėskite **Našumo didinimo modelis** ir pasirinkite **Našumo didinimo formatas**.
2. Veiksmų srityje pasirinkite **Dizaino įrankis**.
3. Puslapio **Formato dizaino įrankis** skirtuke **Susiejimas** pasirinkite **Išplėsti / sutraukti**.
4. Išskleiskite elementus **Modelis**, **Duomenys** ir **Operacija**.

    Šis ER formatas sukurtas generuoti tiekėjo operacijų ataskaitą XML formatu.

    ![Duomenų šaltinių ir sukonfigūruotų formato elementų susiejimų formatavimas formato dizaino įrankio puslapyje](media/er-calculated-field-ds-performance-format.png)

5. Uždarykite puslapį **Formato dizaino įrankis**.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>Pavyzdinio ER vykdymo sekimo sprendimo vykdymas

Tarkime, kad baigėte kurti pirmąją ER sprendimo versiją. Dabar norite patikrinti sprendimą naudodami savo „Finance“ egzempliorių ir išanalizuoti vykdymo našumą.

### <a name="turn-on-the-er-performance-trace"></a>ER našumo sekimo įjungimas

1. Pasirinkite įmonę **DEMF**.
2. Atlikite veiksmus, nurodytus [ER našumo sekimo įjungimas](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace), kad būtų sugeneruotas našumo sekimas, kai vykdomas ER formatas.

    ![Vartotojo parametrų dialogo langas](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>ER formato vykdymas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Našumo didinimo formatas**.
3. Veiksmų srityje pasirinkite **Vykdyti**.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>Našumo sekimo naudojimas modelio susiejimo našumui analizuoti

1. Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Našumo didinimo susiejimas**.
2. Veiksmų srityje pasirinkite **Dizaino įrankis**.
3. Veiksmų srities puslapyje **Modelio susiejimai** pasirinkite **Dizaino įrankis**.
4. Puslapio **Modelio susiejimo dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.
5. Pasirinkite naujausią sugeneruotą sekimą ir pasirinkite **Gerai** .

Atsiranda naujos informacijos apie kai kuriuos dabartinio modelio susiejimo duomenų šaltinio elementus.

- Faktinis laikas, sugaištas gaunant duomenis naudojant duomenų šaltinį
- Tas pats laikas, išreikštas kaip viso laiko, praleisto vykdant visą modelio susiejimą, procentinė dalis

![Vykdymo laiko informacija puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-2.png)

Tinklelyje **Našumo statistika** parodyta, kad duomenų šaltinis **Operacija** iškviečia lentelę VendTrans vieną kartą. Duomenų šaltinio **Operacija** reikšmė **\[265\]\[Q:265\]** nurodo, kad 265 tiekėjo operacijos buvo gautos iš programos lentelės ir grąžintos į duomenų modelį.

Tinklelis **Našumo statistika** taip pat parodo, kad dabartinis modelio susiejimas dubliuoja duomenų bazės užklausas, kai vykdomas duomenų šaltinis **\#Tiekėjas**. Šis dubliavimas įvyksta dėl toliau pateiktų priežasčių.

- Tiekėjo lentelė iškviečiama dviem kartus kiekvienai iš 265 pasikartojančių tiekėjo operacijų, iš viso įvykdoma 530 iškvietimų.

    - Vienas iškvietimas atliekamas norint įvesti tiekėjo kodo numerį.
    - Vienas iškvietimas atliekamas norint įvesti tiekėjo pavadinimą.

- Tiekėjo lentelė iškviečiama kiekvienai pasikartojančiai tiekėjo operacijai, net jei buvo užregistruotos tik penkių tiekėjų gautos operacijos. Iš 530 iškvietimų 525 yra dublikatai. Toliau pateiktame paveikslėlyje parodytas pranešimas apie pasikartojančius iškvietimus, kurį gaunate (duomenų bazės užklausos).

![Pranešimas apie pasikartojančias duomenų bazės užklausas puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-2a.png)

Atkreipkite dėmesį, kad daugiau nei 80 procentų (maždaug šešios sekundės) viso modelio susiejimo vykdymo laiko (apytiksliai aštuonių sekundžių) buvo panaudota gaunant reikšmes iš programos lentelės VendTable. Šis procentas yra per didelis dviems penkių tiekėjų atributams, palyginti su programos lentelės VendTrans informacijos kiekiu.

Norėdami sumažinti atliekamų iškvietimų skaičių, kad būtų galima gauti kiekvienos operacijos tiekėjo informaciją ir padidinti modelio susiejimo našumą, naudokite duomenų šaltinio **\#Tiekėjas** kaupimą talpykloje.

> [!NOTE]
> Duomenų šaltinis **Operacija\\\#Tiekėjas** bus kaupiamas talpykloje vykdymo metu, duomenų šaltinio **Operacija** dabartinės operacijos aprėptyje.

Kaupdami duomenų šaltinį **\#Tiekėjas** saugykloje sumažinate pasikartojančių iškvietimų skaičių nuo 525 iki 260, tačiau pilnai nepašalinate dubliavimo. Norėdami visiškai pašalinti dubliavimą, galite sukonfigūruoti naują parametrizuotą duomenų šaltinį, kurio tipas yra **Apskaičiuotas laukas**.

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Patobulinkite modelio susiejimą pagal iš vykdymo sekimo gautą informacija

### <a name="change-the-logic-of-the-model-mapping"></a>Modelio susiejimo logikos keitimas

Atlikite toliau pateiktus veiksmus, norėdami naudoti kaupimą talpykloje ir duomenų šaltinį, kurio tipas yra **Apskaičiuotas laukas**, kad išvengtumėte pasikartojančių iškvietimų į duomenų bazę.

1. Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Našumo didinimo susiejimas**.
2. Veiksmų srityje pasirinkite **Dizaino įrankis**.
3. Veiksmų srities puslapyje **Modelio susiejimai** pasirinkite **Dizaino įrankis**.
4. Puslapyje **Modelio susiejimo dizaino įrankis** atlikite toliau pateiktus veiksmus, norėdami įtraukti duomenų šaltinį, kurio tipas yra **Lentelės įrašai**, kad pasiektumėte įrašus programos lentelėje VendTable.

    1. Srityje **Duomenų šaltinio tipai** išplėskite **„Dynamics 365 for Operations”** ir pasirinkite **Lentelės įrašai**.
    2. Pasirinkite **Įtraukti šaknį**.
    3. Dialogo lango lauke **Pavadinimas** įveskite **Tiekėjas**.
    4. Lauke **Lentelė** įveskite **VendTable**.
    5. Pasirinkite **Gerai**.

5. Galite parametrizuoti iškvietimus į duomenų šaltinius, kurių tipas yra **Apskaičiuotas laukas**, tik jei šie duomenų šaltiniai yra konteineryje. Todėl atlikite toliau pateiktus veiksmus, norėdami įtraukti duomenų šaltinį, kurio tipas yra **Tuščias konteineris**, kad būtų galima apdoroti naują parametrizuotą duomenų šaltinį, kurio tipas yra **Apskaičiuotas laukas**.

    1. Srityje **Duomenų šaltinio tipai** išplėskite **Bendra** ir pasirinkite **Tuščias konteineris**.
    2. Pasirinkite **Įtraukti šaknį**.
    3. Dialogo lango lauke **Pavadinimas** įveskite **Dėžė**.
    3. Pasirinkite **Gerai**.

    ![Duomenų šaltinis Dėžė puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-3.png)

6. Atlikite toliau pateiktus veiksmus, norėdami įtraukti parametrizuotą duomenų šaltinį, kurio tipas yra **Apskaičiuotas laukas**.

    1. Srityje **Duomenų šaltiniai** pasirinkite **Dėžė**.
    2. Srityje **Duomenų šaltinio tipai** išplėskite **Funkcijos** ir pasirinkite **Apskaičiuotasis laukas**.
    3. Pasirinkite **Įtraukti**.
    4. Dialogo lango lauke **Pavadinimas** įveskite **Tiekėjas**.
    5. Pasirinkite **Redaguoti formulę**.
    6. Puslapyje **Formulės dizaino įrankis** pasirinkite **Parametrai**, norėdami nurodyti parametrus, kuriuos reikia pateikti, kai šis duomenų šaltinis iškviečiamas.
    7. Dialogo lange **Parametrai** pasirinkite **Naujas**.
    8. Lauke **Pavadinimas** įveskite **parmVendAccNumber**.
    9. Lauke **Tipas** pasirinkite **Eilutė**.
    10. Pasirinkite **Gerai**.
    11. Lauke **Formulė** įveskite **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))** .
    12. Pasirinkite **Įrašyti** ir uždarykite puslapį **Formulių dizaino įrankis**.
    13. Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.

7. Atlikite toliau pateiktus veiksmus, kad įtrauktas duomenų šaltinis būtų pažymėtas kaip kaupiamas talpykloje vykdymo metu.

    1. Srityje **Duomenų šaltiniai** pasirinkite **Dėžė\\Tiekėjas**.
    2. Pasirinkite **Talpykla**.

    > [!NOTE]
    > Duomenų šaltinis **Dėžė\\Tiekėjas** bus kaupiamas talpykloje vykdymo metu, visų duomenų šaltinio **Operacija** tiekėjo operacijų aprėptyje.

8. Atlikite toliau pateiktus veiksmus, norėdami atnaujinti įdėtąjį duomenų šaltinį **Operacija\\\#Tiekėjas**, kad jis naudotų duomenų šaltinį **Dėžė\\Tiekėjas**.

    1. Srityje **Duomenų šaltiniai** išplėskite **Operacija**.
    2. Pasirinkite duomenų šaltinį **Operacija\\\#Tiekėjas** ir pasirinkite **Redaguoti** \> **Redaguoti formulę** .
    3. Puslapio **Formulės dizaino įrankis** lauke **Formulė** įveskite **Box.Vend(\@.AccountNum)** .
    4. Pasirinkite **Įrašyti** ir uždarykite puslapį **Formulių dizaino įrankis**.
    5. Pasirinkite **Gerai** , kad užbaigtumėte jūsų keitimus pasirinktame duomenų šaltinyje.

9. Pasirinkite **Įrašyti**.

    ![Duomenų šaltinis Tiekėjas puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-4.png)

10. Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.
11. Uždarykite puslapį **Modelio susiejimai**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Modifikuotos ER modelio susiejimo versijos užbaigimas

1. Puslapio **Konfigūracijos** „FastTab“ **Versijos** pasirinkite konfigūracijos **Našumo didinimo susiejimas** versiją **1.2**.
2. Pasirinkite **Keisti būseną** \> **Baigti** ir pasirinkite **Gerai**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Modifikuoto ER vykdymo sekimo sprendimo vykdymas

Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>Našumo sekimo naudojimas modelio susiejimo koregavimams analizuoti 

1. Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Našumo didinimo susiejimas**.
2. Veiksmų srityje pasirinkite **Dizaino įrankis**.
3. Veiksmų srities puslapyje **Modelio susiejimai** pasirinkite **Dizaino įrankis**.
4. Puslapio **Modelio susiejimo dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.
5. Pasirinkite naujausią sugeneruotą sekimą ir pasirinkite **Gerai** .

Atkreipkite dėmesį, kad atlikus modelio susiejimo pakeitimus, nebeliko pasikartojančių užklausų į duomenų bazę. Taip pat sumažėjo šio modelio susiejimo iškvietimų į duomenų bazės lenteles ir duomenų šaltinius skaičius.

![Informacijos sekimas 1 puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-5.png)

Bendras vykdymo laikas buvo sumažintas 20 kartų (nuo maždaug 8 sekundžių iki maždaug 400 milisekundžių). Todėl pagerėjo viso ER sprendimo našumas.

![Informacijos sekimas 2 puslapyje Modelio susiejimo dizaino įrankis](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>1 priedas: pavyzdinio „Microsoft” ER sprendimo komponentų atsisiuntimas

Turite atsiųsti ir vietoje saugoti toliau nurodytus failus.

| Failas                                        | Turinys |
|---------------------------------------------|---------|
| Našumo didinimo model.version.1     | [ER duomenų modelio konfigūracijos pavyzdys](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Našumo didinimo mapping.version.1.1 | [ER modelio susiejimo konfigūracijos pavyzdys](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Našumo didinimo format.version.1.1  | [ER formato konfigūracijos pavyzdys](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>2 priedas: ER sistemos konfigūracija

Prieš pradėdami naudoti ER sistemą, kad būtų padidintas pavyzdinio „Microsoft” ER sprendimo našumas, turite sukonfigūruoti minimalų ER parametrų rinkinį.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>ER parametrų konfigūravimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.
3. **Elektroninių ataskaitų parametrai** puslapyje **Bendra** skirtuke nustatykite **Įjungti dizaino režimą** parinktį į **Taip**.
4. **Priedai** skirtuke nustatykite tolesnius parametrus:

    - **Konfigūracijos** lauke pasirinkite **Failas** tipą, skirtą **DEMF** įmonei.
    -  **Užduoties archyvas**, **Laikini**, **Bazinė linija** ir **Kiti** laukuose pasirinkite **Failas** tipą.

Norėdami sužinoti daugiau apie ER parametrus, žr. [ER sistemos konfigūracija](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>ER konfigūracijos tiekėjo aktyvavimas

Kiekviena pridėta ER konfigūracija pažymėta kaip priklausanti ER konfigūracijos teikėjui. ER konfigūracijos tiekėjas, kuris aktyvuojamas **Elektroninė ataskaita** darbo srityje naudojamas šiam tikslui. Todėl turite aktyvuoti ER konfigūracijos tiekėją **Elektroninė ataskaita** darbo srityje prieš pridėdami ar redaguodami ER konfigūracijas.

> [!NOTE]
> Tik ER konfigūracijos savininkas gali redaguoti konfigūraciją. Todėl prieš redaguojant ER konfigūraciją atitinkamas ER konfigūracijos tiekėjas turi būti aktyvuotas **Elektroninė ataskaita** darbo srityje.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER konfigūracijos teikėjų sąrašo peržiūra

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Konfigūracijos tiekėjai**.
3. **Konfigūracijos teikėjo lentelė** puslapyje kiekvienas teikėjo įrašas turi unikalų pavadinimą ir URL. Peržiūrėkite šio puslapio turinį. Jei įrašas, skirtas **Litware, Inc.** jau yra, praleiskite sekančią procedūrą, [Pridėkite naują ER konfigūracijos teikėją](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Pridėkite naują ER konfigūracijos tiekėją

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Konfigūracijos tiekėjai**.
3. **Konfigūracijos tiekėjai** puslapyje pasirinkite **Nauja**.
4. Lauke **Pavadinimas** įveskite **Litware, Inc.**
5. **Internetinis adresas** lauke įveskite `https://www.litware.com`.
6. Pasirinkite **Įrašyti**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>ER konfigūracijos tiekėjo aktyvavimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos teikėjai** dalyje pasirinkite **„Litware, Inc.”** plytelę ir pasirinkite **Nustatyti kaip aktyvų**.

Daugiau informacijos apie ER konfigūracijos tiekėjus žr. [Konfigūracijos teikėjų kūrimas pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas](trace-execution-er-troubleshoot-perf.md)
- [Apskaičiuoto lauko tipo ER duomenų šaltinių parametrizuotų kvietimų palaikymas](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
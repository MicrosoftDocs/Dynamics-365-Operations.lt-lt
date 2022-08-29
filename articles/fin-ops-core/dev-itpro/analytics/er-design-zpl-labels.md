---
title: Naujo ER sprendimo, skirto spausdinti ZPL žymes, kūrimas
description: Šiame straipsnyje paaiškinama, kaip sukurti naują elektroninių ataskaitų (ER) sprendimą spausdinant Javų programavimo kalbos (ZPL) žymes.
author: kfend
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7ef83cf4822ca129af3ca01fa6ddd05219fee0d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271770"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>Naujo ER sprendimo, skirto spausdinti ZPL žymes, kūrimas

[!include [banner](../includes/banner.md)]


Šiame straipsnyje paaiškinama, kaip sistemos administratoriaus, [elektroninių ataskaitų kūrėjo arba elektroninio ataskaitų funkcinių konsultanto vaidmens vartotojas gali konfigūruoti elektroninių ataskaitų (ER)](general-electronic-reporting.md) sistemos parametrus, sukurti reikiamas ER konfigūracijas [naujam ER](general-electronic-reporting.md#Configuration) sprendimą, kad būtų galima pasiekti sandėlio valdymo sistemos duomenis, ir generuoti pasirinktines sandėlio vietos žymes "Vz." programavimo kalbos (ZPL) II formatu. Šie žingsniai gali būti užbaigti **USRT** bendrovėje.

## <a name="business-scenario"></a>Verslo scenarijus

Jūs esate įmonė, kuri įdiegė sandėlių valdymą " Microsoft Dynamics 365 Finance". Kiekviena sandėlio vieta turi būti žymima naudojant savitarnos etiketę su brūkšniniu kodu. Sandėlio darbuotojai brūkšniniams kodams nuskaityti naudos kišeninių brūkšninių kodų skaitytuvus.

Visos sandėlio vietos buvo pažymėtos pagal nefiksuotos veiklos rūšis. Tačiau, jei esamos žymės sugadintos arba sandėlio lentynos konfigūruotos iš naujo, pagal poreikį turite spausdinti sandėlio vietos žymes. Naudodami neseniai išleistas ER funkcijas, galite konfigūruoti naują ER sprendimą, kuris leidžia sandėlio vadovui spausdinti etiketes tiesiai į etikečių spausdintuvą.

## <a name="configure-the-er-framework"></a>ER sistemos konfigūracija

Atlikite veiksmus, aprašytus skyriuje [Konfigūruoti ER sistemą](er-quick-start2-customize-report.md#ConfigureFramework), kad nustatytumėte minimalų ER parametrų rinkinį. Prieš pradėdami naudoti ER sistemą, kad kurdami naują ER sprendimą, turite užbaigti šį nustatymą.

## <a name="design-a-domain-specific-data-model"></a>Suprojektuoti domeno konkretų duomenų modelį

Sukurkite naują ER konfigūraciją, kurioje būtų sandėlio [valdymo](er-overview-components.md#data-model-component) domeno duomenų modelio komponentas. Šis duomenų modelis vėliau bus naudojamas kaip duomenų šaltinis, kai ER formatą sukursite sandėlio vietos etiketėms generuoti.

### <a name="import-a-data-model-configuration"></a>Importuoti duomenų modelio konfigūraciją

Norėdami importuoti reikiamą duomenų modelį iš "Microsoft" teikiamo XML failo, atlikite šiuos veiksmus. Taip pat galite kurti savo duomenų modelį, kaip aprašyta kitame skyriuje.

1. Atsisiųskite [sandėlį model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) failą ir įrašykite jį į vietinį kompiuterį.
2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. **Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.
4. **Konfigūracijos puslapio** veiksmų srityje iš XML failo pasirinkite **Mainų** \> **įkėlimą**.
5. Pasirinkite **Naršyti**, raskite ir pasirinkite failą **Warehouse model.version.1.xml**.
6. Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.

![Importuota ER duomenų modelio konfigūracija konfigūracijos puslapyje.](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Duomenų modelio konfigūracijos kūrimas

Užuot importuodami "Microsoft" pateiktą duomenų modelio failą, galite sukurti duomenų modelį nuo pradžių. Pavyzdyje, kuriame parodyta, kaip atlikti šią užduotį, žr [. Sukurkite naują duomenų modelio konfigūraciją](er-quick-start1-new-solution.md#DesignDataModel).

### <a name="review-the-data-model"></a>Peržiūrėti duomenų modelį

Duomenų modelio dizaino įrankio puslapyje galite peržiūrėti redaguojamą sukonfigūruoto **duomenų modelio** versiją.

![ER duomenų modelio struktūra duomenų modelio dizaino įrankio puslapyje.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Suprojektuokite konfigūruoto duomenų modelio žemėlapį

Kaip elektroninių ataskaitų kūrėjo vaidmens vartotojas turite sukurti naują ER [konfigūraciją](er-overview-components.md#model-mapping-component), kurioje būtų sandėlio duomenų modelio susiejimo komponentas. Šis komponentas įdiegia sukonfigūruotą duomenų modelį, skirtą "Dynamics 365" finansai, ir yra konkretus tai programai. Turite jį sukonfigūruoti, kad būtų galima nurodyti programos objektus, kurie bus naudojami sukonfigūruotui duomenų modeliui užpildyti programos duomenimis apdorojimo metu. Norėdami baigti šią užduotį turite suprasti, kaip sandėlio valdymo verslo domeno duomenų struktūra yra įdiegta finansuose.

### <a name="import-a-model-mapping-configuration"></a>Importuoti modelio susiejimo konfigūraciją

Norėdami importuoti reikiamą modelio susiejimą iš "Microsoft" teikiamo XML failo, atlikite šiuos veiksmus. Arba galite sukurti savo modelio išdėstymą, kaip aprašyta kitame skyriuje.

1. Atsisiųskite [sandėlio modelio susiejimo.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) failą ir įrašykite jį į savo vietinį kompiuterį.
2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. **Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.
4. **Konfigūracijos puslapio** veiksmų srityje iš XML failo pasirinkite **Mainų** \> **įkėlimą**.
5. Pasirinkite **Naršyti**, raskite ir pasirinkite sandėlio **modelio susiejimo.version.1.1.xml** failą.
6. Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.

![Importuota ER modelio susiejimo konfigūracija konfigūracijos puslapyje.](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Modelio susiejimo konfigūracijos kūrimas

Užuot importuodami "Microsoft" pateiktą modelio susiejimo failą, galite sukurti modelių išdėstymą nuo pradžių. Pavyzdyje, kuriame parodyta, kaip atlikti šią užduotį, žr. [Naujo modelio susiejimo konfigūracijos kūrimas](er-quick-start1-new-solution.md#CreateModelMapping).

### <a name="review-the-model-mapping"></a>Modelio susiejimo peržiūra

Modelio susiejimo dizainerio puslapyje galite peržiūrėti redaguojamą konfigūruojamo **modelio susiejimo** versiją.

![ER modelio susiejimo struktūra modelio susiejimo dizainerio puslapyje.](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Formato kūrimas

Kaip vartotojas elektroninės ataskaitos funkcijų konsultanto vaidmenyje, turite sukurti naują ER konfigūraciją, kurioje būtų [formato](er-overview-components.md#format-component) komponentas. Norėdami sukonfigūruoti šį komponentą, naudodami ZPL II kodą nurodysite sandėlio vietos žymos maketą.

### <a name="import-a-format-configuration"></a>Formato konfigūracijos importavimas

Norėdami importuoti reikiamą formatą iš Microsoft teikiamo XML failo, atlikite šiuos veiksmus. Taip pat galite sukurti savo formatą, kaip aprašyta kitame skyriuje.

1. Atsisiųskite [sandėlio vietos žymes.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) failą ir įrašykite į savo vietinį kompiuterį.
2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. **Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.
4. **Konfigūracijos puslapio** veiksmų srityje iš XML failo pasirinkite **Mainų** \> **įkėlimą**.
5. Pasirinkite **Naršyti**, raskite ir pasirinkite sandėlio **vietos žymes.version.1.1.xml** failą.
6. Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.

![Importuota ER formato konfigūracija konfigūracijos puslapyje.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Formato konfigūracijos kūrimas

Užuot importuodami "Microsoft" pateiktą formato failą, galite kurti formatą nuo pradžių. Kaip atlikti šią užduotį, pvz., žr. [naujo formato konfigūracijos kūrimas](er-quick-start1-new-solution.md#FormatCreate).

### <a name="review-the-format"></a>Formato peržiūra

Galite peržiūrėti redaguojamą konfigūruojamo formato versiją formato konstruktoriaus **puslapyje**.

![ER formato struktūra formato konstruktoriaus puslapyje.](./media/er-design-zpl-labels-format.png)

Šio `model.Location.Label` formato duomenų šaltinis konfigūruojamas generuoti žymes, kuriose yra ši informacija:

- Sandėlio pavadinimas kaip tekstas
- Sandėlio pavadinimas kaip brūkšninis kodas
- Vietos pavadinimas
- Kontroliniai skaitmenys

Duomenų šaltinio **formulės dizainerio** puslapyje ER formulė, kuri naudojama žymoms `CONCATENATE` generuoti, apima funkciją, kuri sujungia informaciją norimu maketu.

![Duomenų šaltinio formulė formulės konstruktoriaus puslapyje.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> Žymės maketas sukurtas taip, kad vietos pavadinimas ir kontroliniai skaitmenys būtų sulygiuoti žymos centre. Tačiau ZPL II nepalaiko brūkšninių kodų centro lygiuotės. Todėl duomenų šaltinio formulė `model.Location.Warehouse.Alignment` naudojama brūkšniniui kodui žymos centre sulygiuoti. Ši formulė apskaičiuoja kairiąją brūkšninio kodo korespondentinę sąskaitą pagal sandėlio pavadinimo simbolių skaičių.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Paruoškite aplinką peržiūrėti sugeneruotas etiketes

Toliau pateiktame pavyzdyje naudojant ZPL žymių spausdintuvo iasuliatoriaus programą, kad būtų galima peržiūrėti ekrane sugeneruotas etiketes. Norėdami įgalinti šią pasirinktį, atlikite šiuos veiksmus.

1. Įtraukite [spausdintuvo](er-destination-type-print.md) ER **paskirties** vietą į sandėlio vietos ŽYMų ER formatą ir sukonfigūruokite ją, kad iš finansų siųsti dokumentų [maršruto agentui (DRA)](install-document-routing-agent.md) sugeneruotas žymes.
2. Įdiekite ir sukonfigūruokite DRA pagal sugeneruotas žymas iš finansų į vietinį spausdintuvą, kuris pasiekiamas iš dabartinės darbo vietos.
3. Įtraukite vietinį spausdintuvą į dabartinę darbo vietą ir sukonfigūruokite, kad iš DRA sugeneruotos etiketės būtų perduodamos į spausdintuvo iždatoriaus programą.
4. Įdiekite spausdintuvo iždatoriaus programą kaip "Chrom" interneto naršyklės plėtinį ir sukonfigūruokite ją, kad sugeneruotos etiketės būtų perduodamos iš vietinio spausdintuvo į žiniatinklio tarnybą, kuri atvaizduos sugeneruotas etiketes ir grąžins jas į spausdintuvo iždą peržiūrai.

<table>
<tbody>
<tr align="center">
<td>
<p>„Finance“</p>
<p>ER ataskaita</p>
<p>Spausdintuvo paskirties vieta</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Dokumento maršruto parinkimo agentas</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Vietinis spausdintuvas</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Spausdintuvo iždatorius</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Atvaizdavimo žiniatinklio tarnyba</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Įdiegti ir konfigūruoti spausdintuvo iasuliatoriaus programą

Įtraukite spausdintuvo iždatoriaus programą į ZPL atvaizdavimo įrenginį į savo chromuoto žiniatinklio naršyklę. Šiame pavyzdyje naudojamas [Zpl spausdintuvo](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo) iasuliatorius, pagrįstas žymių [ZPL žiniatinklio tarnyba](http://labelary.com/service.html). Spausdintuvo iždatoriaus programa iš vietinio spausdintuvo perduoda sugeneruotas ZPL formato etiketes į žiniatinklio tarnybą, o tada grąžina žymas kaip PDF arba PNG failus peržiūrai.

1. Chromuoto interneto parduotuvėje raskite ir pasirinkite norimą naudoti spausdintuvo iuliatoriaus programą. Tada pasirinkite Įtraukti į **chromuotas,** norėdami įtraukti jį į savo chromuoto žiniatinklio naršyklę.

    ![Spausdintuvo iždatoriaus programa pridedama prie "Chrom" žiniatinklio naršyklės iš "Chrom" interneto parduotuvės.](./media/er-design-zpl-labels-add-app.png)

2. Pasirinkite Paleisti **programą, kad** būtų paleista spausdintuvo iždatoriaus programa iš chromuoto žiniatinklio naršyklės.

    ![Iš "Chrom" žiniatinklio naršyklės paleisite spausdintuvo iždatoriaus programą.](./media/er-design-zpl-labels-run-app.png)

3. Konfigūruoti paleisdami programą:

    1. Išjunkite programą.
    2. Spausdintuvo parametruose nustatykite pagrindinį kompiuterį kaip **127.0.0.1**.
    3. Nustatyti prievadą **9100**.

        ![Konfigūruojama spausdintuvo iždatoriaus programa.](./media/er-design-zpl-labels-configure-app.png)

    4. Įjunkite programą atgal. Turėtumėte gauti pranešimą, kuriame nurodoma, kad spausdintuvas buvo paleistas nurodytame pagrindinio kompiuterio ir prievade.

        ![Spausdintuvo iždatoriaus programa įjungta atgal.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Kadangi šiame pavyzdyje naudojama spausdintuvo iaskraukite programa naudoja žiniatinklio tarnybą etiketėms atvaizduoti, įsitikinkite, kad saugos parametrai leidžia jums susisiekti su tarnyba. Kitu atveju programa negaus atvaizduoti žymių ir nebus galima peržiūrėti šių žymių.

### <a name="add-and-configure-a-local-printer"></a>Vietinio spausdintuvo pridėjimas ir konfigūravimas

[Pridėkite naują vietinį spausdintuvą](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b), kurį dabartinis įrenginys gali naudoti sugeneruotas žymas iš DRA į spausdintuvo ieškiatoriaus programą.

1. Sistemoje "Windows" pasirinkite Paleisti **parametrų** \> **·** \> **įrenginių** \> **spausdintuvų \& skaitytuvus.**
2. Pasirinkite spausdintuvų **skaitytuvų \& parametrus**.
3. Norėdami įtraukti **spausdintuvą arba skaitytuvą**, pasirinkite Įtraukti **įrenginį**.
4. Norimo **spausdintuvo nėra sąraše, pasirinkite** Įtraukti **rankiniu būdu**.
5. Lauke Rasti **spausdintuvą pagal kitas pasirinktis pasirinkite** Įtraukti **vietinį spausdintuvą arba tinklo spausdintuvą, kuris turi rankiniu būdu nustato parametrus**.
6. Lauke Pasirinkti **spausdintuvo prievadą** pasirinkite Kurti **naują prievadą**, tada atlikite šiuos veiksmus:

    1. Lauke Prievado **tipas pasirinkite** Standartinis **TCP/IP prievadas**.
    2. Lauke Pagrindinio **kompiuterio vardas arba IP adresas** įveskite **127.0.0.1**.
    3. **Lauke Prievado pavadinimas** įveskite **ZPL**.
    4. Palaukite, kol **bus užbaigta TCP/IP** prievado aptikimo operacija.
    5. Lauke Įrenginio **tipas** pasirinkite **Pasirinktinis**, tada – **Parametrai**.
    6. Įsitikinkite, kad nurodyti šie prievado parametrai:

        - **Prievado pavadinimas:** ZPL
        - **Spausdintuvo pavadinimas arba IP adresas:** 127.0.0.1
        - **Protokolas: neapdorotas**
        - **Prievado numeris:** 9100

7. Lauke Diegti **spausdintuvo tvarkyklę** pasirinkite Tik **bendrasis / tekstas**.
8. Lauke Spausdintuvo **pavadinimas** įveskiteVzbraPrinter **·**.

![Į dabartinį įrenginį pridedamas vietinis spausdintuvas.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>DRA įdiegimas ir konfigūravimas

Paruoškite DRA perduoti sugeneruotas žymas iš finansų į sukonfigūruotą vietinį spausdintuvą.

1. [Įdiekite DRA](install-document-routing-agent.md#install-the-document-routing-agent).
2. [Konfigūruokite DRA](install-document-routing-agent.md#configure-the-document-routing-agent).
3. [Užregistruokite vietinį](install-document-routing-agent.md#register-network-printers) spausdintuvą DRA.
4. [Aktyvinti vietinį spausdintuvą](install-document-routing-agent.md#administer-network-printers) jūsų finansų aplinkoje.

![DRA paruošimas spausdinti sugeneruotas žymes.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>ER paskirties vietos konfigūravimas

Paruoškite ER paskirties vietą perduoti sugeneruotas žymas iš finansų į DRA.

1. Eikite **Organizacijos administravimas** \> **Elektroninė ataskaita** \> **Elektroninės ataskaitos paskirtis**.
2. **Elektroninių ataskaitų paskirties** puslapio veiksmų srityje pasirinkite **Naujas**.
3. Nuorodos lauke **pasirinkite** Sandėlio **vietos žymes**.
4. **Failo paskirties** "FastTab" pasirinkite **Naujas**.
5. Lauke Pavadinimas **įveskite** **Žymes**.
6. Lauke Failo **komponento** vardas pasirinkite **Ataskaita**.
7. Pasirinkite **Parametrai**.
8. Dialogo lange **Paskirties parametrai** skirtuke **Spausdintuvas** nustatykite pasirinktį **Įgalinta** kaip **Taip**.
9. Lauke Spausdintuvo **pavadinimas** pasirinkiteVzbraPrinter **·**.
10. Dokumento maršruto **tipo** lauke pasirinkite **ZPL**.
11. Pasirinkite **Gerai**.

![Konfigūruojama sandėlio vietos žymių formato ER paskirties vieta elektroninės ataskaitos paskirties puslapyje.](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Peržiūrėti sandėlio vietas

1. Eiti į sandėlio **valdymo nustatymo** \> **·** \> **sandėlio** \> **vietas.**
2. Puslapyje Vietos **filtruoti**, kad būtų galima peržiūrėti tik tas vietas, kurių vertė yra lauke **Tikrinimo skaitmenys**.

![Sandėlių vietų peržiūra vietų puslapyje.](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Spausdinti sandėlio vietos žymes

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Konfigūracijos puslapyje **konfigūracijos** medyje išplėskite Sandėlio modelį **ir** pasirinkite Sandėlio **vietos žymes**.
3. Veiksmų srityje pasirinkite **Vykdyti**.
4. Elektroninės ataskaitos **parametrų dialogo** lange, skirtuke Įrašai **, kuriuos norite įtraukti**, pasirinkite **Filtras**.
5. Skirtuke **Diapazonas** raskite eilutę, kurioje **lentelės laukas** nustatytas kaip **Vietos,** **o laukas** lauke nustatytas kaip **Vieta**. **Kriterijų lauke** įveskite **LPEnabled**.
6. Pasirinkite **Gerai**.
7. Pasirinkite **Gerai**. Etiketė sugeneruota ir rodoma spausdintuvo iuliatoriaus programos peržiūros puslapyje.

![Zpl spausdintuvo iuliatoriaus programos peržiūros puslapyje peržiūrima sugeneruota žymė.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>Modifikuoti žymės maketą

Galite pakeisti dabartinį sandėlio vietos žymių maketą. Toliau pavyzdyje parodyta, kaip pakeisti maketą, kad sugeneruotoje etiketėje būtų vietos šablono ID.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Nustatykite **juodraščio būsenos ER vartotojo**[parametro paskirties vietas](electronic-reporting-destinations.md#applicability) kaip **Taip**.
3. Konfigūracijos puslapyje **konfigūracijos** medyje išplėskite Sandėlio modelį **ir** pasirinkite Sandėlio **vietos žymes**.
4. Pasirinkite **Dizaino įrankis**.
5. Skirtuko Susiejimas **puslapyje** Formato konstruktorius **pasirinkite** duomenų `model.Location.Label` šaltinį.
6. Duomenų šaltinio **ypatybės dialogo lange** pasirinkite Redaguoti **formulę** \> **·**.
7. Formulės dizainerio **puslapio** formulės lauke **peržiūrėkite** ER formulę, naudojamą žymiams generuoti.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Atnaujinkite formulę, norėdami įtraukti vietos šablono ID į sugeneruotas žymes.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. Pasirinkite **Įrašyti**.
10. Pasirinkite **Gerai**.
11. Veiksmų srityje pasirinkite **Vykdyti**.
12. Elektroninės ataskaitos **parametrų dialogo** lange, skirtuke Įrašai **, kuriuos norite įtraukti**, pasirinkite **Filtras**.
13. Skirtuke **Diapazonas** raskite eilutę, kurioje **lentelės laukas** nustatytas kaip **Vietos,** **o laukas** lauke nustatytas kaip **Vieta**. Kriterijų lauke **įveskite** **Baja**.
14. Pasirinkite **Gerai**.
15. Pasirinkite **Gerai**. Etiketė sugeneruota ir rodoma spausdintuvo iuliatoriaus programos peržiūros puslapyje.

![Zpl spausdintuvo iuliatoriaus programos peržiūros puslapyje peržiūrima sugeneruota žymė, kurioje yra vietos šablono ID.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Kodavimas

> [!NOTE]
> Turite sinchronizuoti redaguojamo ER formato **Common\\File** komponento kodavimo parametrą ir atitinkamus sukurtos žymės parametrus. **[...](er-suppress-bom-characters.md)** **Common\\File**  komponento kodavimo lauko vertė neturi prieštarauja ZPL komandai, kuri naudojama žymos kodavimui (pvz., komandai`^CI`) valdyti. ER nepatikrinta, ar šie parametrai yra sinchronizuojami.

## <a name="additional-resources"></a>Papildomi ištekliai

[Spausdintuvo paskirties vieta](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

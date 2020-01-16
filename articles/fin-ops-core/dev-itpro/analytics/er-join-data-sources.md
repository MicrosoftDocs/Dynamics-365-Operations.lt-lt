---
title: Norėdami gauti duomenis iš kelių programos lentelių, ER modelio susiejimuose naudokite duomenų šaltinių jungimo funkciją
description: Šioje temoje paaiškinta, kaip galima naudoti duomenų šaltinių jungimo funkciją elektroninėms ataskaitoms (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 224acc19ee5dda430cd9471aa50e9d870a4f8c60
ms.sourcegitcommit: 564aa8eec89defdbe2abaf38d0ebc4cca3e28109
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667959"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>Norėdami gauti duomenis iš kelių programos lentelių elektroninių ataskaitų (ER) modelio susiejimuose, naudokite duomenų šaltinių jungimo funkciją

[!include[banner](../includes/banner.md)]

Konfigūruodami elektroninės ataskaitos (ER) modelio susiejimus arba formatus, galite [pridėti](#review) reikalingus **sujungimo** tipo duomenų šaltinius. Projektavimo metu **sujungimo** duomenų šaltinis konfigūruojamas kaip kelių duomenų šaltinių, kurie grąžina įrašų sąrašus, rinkinys. Kiekvienam duomenų šaltiniui, išskyrus pirmąjį, reikia nustatyti būtinas sąlygas, kad būtų sujungti dabartinių ir ankstesnių duomenų šaltinių įrašai. Vykdymo metu sukonfigūruotas **sujungimo** tipo duomenų šaltinis [grąžina](#executeERformat) vieną sujungtą įrašų sąrašą, kuriame yra laukai iš įdėtųjų duomenų šaltinių įrašų.

Šiuo metu galimi toliau nurodyti sujungimų tipai:

- Išorinis (kairysis) sujungimas:
    - Sujungti visus pirmojo (kairiausio) duomenų šaltinio įrašus, o tada visus atitinkančius pagal antrojo (dešiniojo) duomenų šaltinio sukonfigūruotų sąlygų įrašus.
- Vidinis (dešinysis) sujungimas:
    - Sujungti tik pirmojo (kairiausio) duomenų šaltinio įrašus ir tik antrojo (dešiniojo) duomenų šaltinio įrašus, atitinkančius pagal sukonfigūruotas sąlygas.

Sukonfigūruotame **sujungimo** duomenų šaltinyje, kai visų duomenų šaltinių tipas yra **Lentelės įrašai**, duomenų šaltinių sujungimo funkcija gali būti [vykdoma duomenų bazės lygiu](#analyze) naudojant vieną SQL sakinį. Taip sumažinamas duomenų bazės kvietimų skaičius ir pagerinamas modelio susiejimo efektyvumas. Kitu atveju **duomenų šaltinio sujungimo** vykdymas atliekamas atmintyje.

> [!NOTE]
> Šiuo metu dar nėra galimybės ER išraiškose naudoti funkcijos **VALUEIN**, kuri nurodo sąlygas įrašų sujungimui sujungimo tipo duomenų šaltiniuose. Norėdami sužinoti daugiau apie šią funkciją, apsilankykite puslapyje [Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md).

Norėdami sužinoti daugiau apie šią funkciją, atlikite šioje temoje esantį pavyzdį.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>Pavyzdys: sujungimo tipo duomenų šaltinių naudojimas, ER modelio susiejimuose

Toliau pateikti veiksmai paaiškina, kaip sistemos administratorius arba elektroninių ataskaitų kūrėjas gali konfigūruoti elektroninių ataskaitų (ER) modelio susiejimą, kad gautų duomenis iš kelių programos lentelių naudojant **sujungimo** tipo duomenų šaltinius, tokiu būdu pagerinant duomenų prieigos efektyvumą. Šiuos veiksmus galima atlikti bet kuriai „Dynamics 365 Finance“ arba „Regulatory Configuration Service“ (RCS) įmonei.

### <a name="prerequisites"></a>Būtinieji komponentai

Norėdami naudoti šios temos pavyzdžius, turite turėti vieną iš toliau nurodytų prieigų, atsižvelgiant į tai, kokia paslauga naudojama šiems veiksmams atlikti:

**Prieiga prie „Finance“ naudojant vieną iš tolesnių vaidmenų.**

- Elektroninės ataskaitos kūrėjas
- Elektroninės ataskaitos funkcijų konsultantas
- Sistemos administratorius

**Prieiga prie RCS naudojant vieną iš tolesnių vaidmenų.**

- Elektroninės ataskaitos kūrėjas
- Elektroninės ataskaitos funkcijų konsultantas
- Sistemos administratorius

Be to, pirmiausia turite atlikti veiksmus, nurodytus procedūroje [Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu](tasks/er-configuration-provider-mark-it-active-2016-11.md).

Taip pat turite iš [„Microsoft“ atsisiuntimo centro](https://go.microsoft.com/fwlink/?linkid=000000) iš anksto atsisiųsti ir įrašyti vietoje šiuos pavyzdinius ER konfigūracijos failus:

| **Turinio aprašas**  | **Failo vardas**   |
|--------------------------|-----------------|
| Pavyzdinis **ER duomenų modelio** konfigūracijos failas, kuris dirbant su pavyzdžiais naudojamas kaip duomenų šaltinis.| [Sujungimo duomenų šaltinio mokymo modelis.versija.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Pavyzdinis **ER modelio susiejimo** konfigūracijos failas, kuris dirbant su pavyzdžiais realizuoja ER duomenų modelį. | [Sujungimo duomenų šaltinio mokymo susiejimas.versija.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Pavyzdinis **ER formato** konfigūracijos failas. Šis failas aprašo duomenis ER formato komponento užpildymui pavyzdžiuose. | [Sujungimo duomenų šaltinio mokymo formatas.versija.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a>Aktyvinti konfigūracijų teikėją

1. Pasiekite „Finance“ arba RCS pirmajame žiniatinklio naršyklės seanse.
2. Eikite į **Organizacijos administravimas \> Darbo sritys \> Elektroninės ataskaitos**.
3. Puslapio **Lokalizavimo konfigūracijos** dalyje **Konfigūravimo teikėjai** įsitikinkite, kad sąraše yra pavyzdinės įmonės „Litware, Inc.“ (http://www.litware.com) konfigūracijos teikėjas ir kad jis pažymėtas kaip **Aktyvus**. Jei nematote šio konfigūracijos teikėjo, atlikite procedūroje [Sukurti konfigūracijų teikėją ir jį pažymėti kaip aktyvų](tasks/er-configuration-provider-mark-it-active-2016-11.md) nurodytus veiksmus.

    ![Elektroninių ataskaitų darbo sritis](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>Pavyzdinių ER konfigūracijos failų importavimas

1. Pasirinkite **Ataskaitų konfigūracijos**.
2. Importuokite ER duomenų modelio konfigūracijos failą.
    1. Pasirinkite **Keitimas**.
    2. Pasirinkite **Įkelti iš XML failo**.
    3. Pasirinkite **Naršyti**, kad surastumėte failą **Sujungimo duomenų šaltinio mokymo modelis.versija.1.1.xml**.
    4. Pasirinkite **Gerai**.
3. Importuokite ER modelio susiejimo konfigūracijos failą.
    1. Pasirinkite **Keitimas**.
    2. Pasirinkite **Įkelti iš XML failo**.
    3. Pasirinkite **Naršyti**, kad surastumėte failą **Sujungimo duomenų šaltinio mokymo susiejimas.versija.1.1.xml**.
    4. Pasirinkite **Gerai**.
4.  Importuokite ER formato konfigūracijos failą.
    1. Pasirinkite **Keitimas**.
    2. Pasirinkite **Įkelti iš XML failo**.
    3. Pasirinkite **Naršyti**, kad surastumėte failą **Sujungimo duomenų šaltinio mokymo formatas.versija.1.1.xml**.
    4. Pasirinkite **Gerai**.
5.  Konfigūracijų medyje išplėskite elementą **Sujungimo duomenų šaltinio mokymo modelis** ir kitus modelio elementus (jei yra).
6.  Atkreipkite dėmesį į ER konfigūracijų sąrašą medyje ir versijos informaciją „FastTab“ **Versijos** – jos bus naudojamos kaip pavyzdinės ataskaitos duomenų šaltinis.

    ![Elektroninių ataskaitų konfigūracijų puslapis](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Vykdymo sekimo parinkčių įjungimas
1.  Pasirinkite **KONFIGŪRACIJOS**.
2.  Pasirinkite **Vartotojo parametrai**.
3.  Nustatykite vykdymo sekimo parametrus, kaip parodyta toliau esančioje ekrano kopijoje.

    ![Elektroninių ataskaitų vartotojo parametrų puslapis](./media/GER-JoinDS-Parameters.PNG)

    Kai šie parametrai įjungti, kiekvienam vykdomam importuotam ER formato failui bus sugeneruota vykdymo sekimo ataskaita. Naudodami sugeneruotos vykdymo sekimo ataskaitos informaciją, galite analizuoti, kaip vykdomas ER formatas bei ER modelio susiejimo komponentai. Norėdami gauti daugiau informacijos apie ER vykdymo sekimo funkciją, eikite į [ER formato vykdymo sekimas siekiant diagnozuoti našumo problemas](trace-execution-er-troubleshoot-perf.md).

### <a name="review-er-model-mapping-part-1"></a>ER modelio susiejimo peržiūra (1 dalis)

Peržiūrėkite ER modelio susiejimo komponento parametrus. Komponentas sukonfigūruotas taip, kad pasiektų informaciją apie ER konfigūracijų versijas, informaciją apie konfigūracijas ir konfigūracijos teikėjus nenaudodamas **sujungimo** tipo duomenų šaltinių.

1.  Pasirinkite konfigūraciją **Sujungimo duomenų šaltinio mokymo susiejimas**.
2.  Norėdami atidaryti susiejimų sąrašą, pasirinkite **Dizaino įrankis**.
3.  Norėdami peržiūrėti susiejimo informaciją, pasirinkite **Dizaino įrankis**. 
4.  Pasirinkite **Rodyti informaciją**.
5.  Konfigūracijų medyje išplėskite duomenų modelio elementus **Set1** ir **Set1.Details**:

    1. Ryšys **Details: Record list = Versions** nurodo, kad elementas **Set1.Details** yra susietas su duomenų šaltiniu **Versijos**, grąžinančiu lentelės **ERSolutionVersionTable** įrašus. Kiekvienas šios lentelės įrašas atitinka vieną ER konfigūracijos versiją. Šios lentelės turinys yra pateikiamas „FastTab“ **Versijos**, esančiame puslapyje **Konfigūracijos**.
    2. Ryšys **ConfigurationVersion: String = @.PublicVersionNumber** reiškia, kad kiekvienos ER konfigūracijos versijos viešosios versijos reikšmė yra paimama iš lauko **PublicVersionNumber** lentelėje **ERSolutionVersionTable** ir įkeliama į elementą **ConfigurationVersion**.
    3. Ryšys **ConfigurationTitle: String = @.'>Relations'.Solution.Name** nurodo, kad ER konfigūracijos pavadinimas yra paimtas iš lauko **Name** lentelėje **ERSolutionTable** naudojant sąryšį (**'>Ryšiai'**) „daugelis su vienu“ tarp lentelių **ERSolutionVersionTable** ir **ERSolutionTable**. Esamos programos egzemplioriaus ER konfigūracijų pavadinimas pateikiami konfigūracijų medyje, esančiame puslapyje **Konfigūracijos**.
    4. Ryšys **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** reiškia, kad konfigūracijos teikėjo, kuriam priklauso esama konfigūracija, pavadinimas yra paimtas iš lauko **Name** lentelėje **ERVendorTable** naudojant sąryšį „daugelis su vienu“ tarp lentelių **ERSolutionTable** ir **ERVendorTable**. ER konfigūracijos teikėjų pavadinimai pateikiami konfigūracijų medyje, esančiame puslapyje **Konfigūracijos**, kiekvienos konfigūracijos puslapio antraštėje. Visą ER konfigūracijos teikėjų sąrašą galima rasti lentelės puslapyje **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos teikėjas**.

    ![ER modelio susiejimo dizaino įrankio puslapis](./media/GER-JoinDS-Set1Review.PNG)

6.  Konfigūracijų medyje išplėskite duomenų modelio elementą **Set1.Summary**:

    1. Ryšys **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** reiškia, kad elementas **Set1.Summary.VersionsNumber** yra susietas su agregavimo lauku **VersionsNumber** duomenų šaltinyje **VersionsSummary**, kurio tipas **GroupBy** ir kuris buvo sukonfigūruotas grąžinti įrašų skaičių lentelėje **ERSolutionVersionTable** naudojant duomenų šaltinį **Versions**.

    ![Duomenų šaltinio GROUPBY parametrų puslapis](./media/GER-JoinDS-Set1GroupByReview.PNG)

7.  Uždarykite puslapį.

### <a name="review"></a>ER modelio susiejimo peržiūra (2 dalis)

Peržiūrėkite ER modelio susiejimo komponento parametrus. Komponentas sukonfigūruotas taip, kad pasiektų informaciją apie ER konfigūracijų versijas, informaciją apie konfigūracijas ir konfigūracijos teikėjus naudodamas **sujungimo** tipo duomenų šaltinį.

1.  Konfigūracijų medyje išplėskite duomenų modelio elementus **Set2** ir **Set2.Details**: Atkreipkite dėmesį, kad ryšys **Details: Record list = Details** reiškia, kad elementas **Set2.Details** yra susietas su duomenų šaltiniu **Details**, kuris yra sukonfigūruotas kaip **sujungimo** tipo duomenų šaltinis.

    ![ER modelio susiejimo dizaino įrankio puslapis](./media/GER-JoinDS-Set2Review.PNG)

    **Sujungimo** tipo duomenų šaltinį galima įtraukti pasirenkant duomenų šaltinį **Functions\Join**:

    ![ER modelio susiejimo dizaino įrankio puslapis](./media/GER-JoinDS-AddJoinDS.PNG)

2.  Pasirinkite duomenų šaltinį **Details**.
3.  Pasirinkite **Redaguoti** srityje **Duomenų šaltiniai**.
4.  Pasirinkite **Redaguoti sujungimą**.
5.  Pasirinkite **Rodyti informaciją**.

    ![Duomenų šaltinio JOIN parametrų puslapis](./media/GER-JoinDS-JoinDSEditor.PNG)

    Šis puslapis naudojamas kuriant reikiamą **sujungimo** tipo duomenų šaltinį. Vykdymo metu šis duomenų šaltinis sukurs vieną jungtinį įrašų iš lentelėje **Jungtinis sąrašas** esančių duomenų šaltinių sąrašą. Įrašų sujungimas prasidės nuo duomenų šaltinio **ConfigurationProviders**, kuris lentelėje yra pirmasis (stulpelis **Tipas** yra tuščias). Kiekvieno kito duomenų šaltinio įrašai bus sujungti atitinkamai su pirminio duomenų šaltinio įrašais, atsižvelgiant į tvarką šioje lentelėje. Kiekvieną sujungiamą duomenų šaltinį reikia sukonfigūruoti kaip duomenų šaltinį, įtrauktą į tikslinį duomenų šaltinį (duomenų šaltinis **1Versions** yra įtrauktas į **1Configurations**, duomenų šaltinis **1Configurations** yra įtrauktas į **ConfigurationProviders**). Kiekviename sukonfigūruotame duomenų šaltinyje turi būti sujungimo sąlygos. Šio konkretaus **sujungimo** duomenų šaltinyje apibrėžiami šie sujungimai:

    - Kiekvienas duomenų šaltinio **ConfigurationProviders** įrašas (nurodytas lentelėje **ERVendorTable**) yra sujungtas su tik **1Configurations** įrašais (nurodytas lentelėje **ERSolutionTable**), kurių vertė tokia pati kaip ir laukų **SolutionVendor** bei **RecId**. Šiam sujungimui naudojamas **vidinio sujungimo** tipas kartu su šioms sutampančių įrašų sąlygoms: 

    FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - Kiekvienas duomenų šaltinio **Configurations** įrašas (nurodytas lentelėje **ERSolutionTable**) yra sujungtas su tik **1Versions** įrašais (nurodytas lentelėje **ERSolutionVersionTable**), kurių vertė tokia pati kaip ir laukų **Solution** bei **RecId**. Šiam sujungimui naudojamas **vidinio sujungimo** tipas kartu su šioms sutampančių įrašų sąlygoms:

    FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - Parinktis **Vykdyti** yra sukonfigūruota kaip **Užklausa**, o tai reiškia, kad šis sujungimo duomenų šaltinis bus vykdomas vykdymo metu duomenų bazės lygiu kaip tiesioginis SQL kvietimas.

    Atkreipkite dėmesį, kad sujungiant duomenų šaltinių, atitinkančių programos lenteles, įrašus, sujungimo sąlygas galima nurodyti naudojant kitų laukų poras, o ne tas, kurios aprašo esamus AOT ryšius tarp šių lentelių. Šis sujungimo tipas taip pat gali būti sukonfigūruotas vykdymui duomenų bazės lygiu.

6.  Uždarykite puslapį.
7.  Pasirinkite **Atšaukti**.
8.  Konfigūracijų medyje išplėskite duomenų modelio elementą **Set2.Summary**:

    - Ryšys **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** reiškia, kad elementas **Set2.Summary.VersionsNumber** yra susietas su agregavimo lauku **VersionsNumber** duomenų šaltinyje **DetailsSummary**, kurio tipas **GroupBy** ir kuris buvo sukonfigūruotas grąžinti duomenų šaltinio **Details**, kurio tipas yra **sujungimas**, sujungtų įrašų skaičių.
    - Atkreipkite dėmesį, kad **Vykdymo** vietos parinktis yra sukonfigūruota kaip **Užklausa**, o tai reiškia, kad šis **GroupBy** duomenų šaltinis bus vykdomas vykdymo metu duomenų bazės lygiu kaip tiesioginis SQL kvietimas. Tai yra įmanoma, nes pagrindinis duomenų šaltinis **Details**, kurio tipas yra **Sujungimas**, yra sukonfigūruotas kaip vykdomas duomenų bazės lygiu.

    ![Duomenų šaltinio GROUPBY parametrų puslapis](./media/GER-JoinDS-Set2GroupByReview.PNG)

9.  Uždarykite puslapį.
10. Pasirinkite **Atšaukti**.

### <a name="executeERformat"></a> ER formato vykdymas

1.  Prisijunkite prie „Finance“ arba RCS antrojo jūsų žiniatinklio naršyklės seanso metu, naudodami tuos pačius kredencialus ir įmonę kaip ir pirmojo seanso metu.
2.  Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
3.  Išplėskite konfigūraciją **Sujungimo duomenų šaltinio mokymo modelis**.
4.  Pasirinkite konfigūraciją **Sujungimo duomenų šaltinio mokymo formatas**.
5.  Pasirinkite **Dizaino įrankis**.
6.  Pasirinkite **Rodyti informaciją**.
7.  Pasirinkite **Susiejimas**.
8.  Pasirinkite **Išplėsti / sutraukti**.

    Atkreipkite dėmesį, kad šis formatas yra skirtas užpildyti sugeneruotą tekstinį failą, kuriame kiekvienai ER konfigūracijos versijai yra skirta nauja eilutė (seka **Versija**). Kiekvienoje sugeneruotoje eilutėje bus konfigūracijos teikėjo, kuriam priklauso dabartinę konfigūracija, pavadinimas ir konfigūracijos versija, atskirta kabliataškiu. Galutinėje sugeneruoto failo eilutėje yra rastų ER konfigūracijos versijų skaičius (seka **Suvestinė**).

    ![ER formato dizaino įrankio puslapis](./media/GER-JoinDS-FormatReview.PNG)

    Duomenų šaltiniai **Data** ir **Summary** naudojami užpildyti konfigūracijos versijos informacijai sugeneruotame faile:

    - Informacija iš duomenų modelio **Set1** naudojama, kai vartotojo dialogo lange vykdymo metu pasirenkate parinktį **Ne**, skirtą duomenų šaltiniui **Selector**.
    - Informacija iš duomenų modelio **Set2** naudojama, kai vartotojo dialogo lange vykdymo metu pasirenkate parinktį **Taip**, skirtą duomenų šaltiniui **Selector**.

    ![ER formato dizaino įrankio puslapis](./media/GER-JoinDS-FormatMappingReview.PNG)

9.  Pasirinkite **Vykdyti**.
10. Dialogo lange pasirinkite parinktį **Ne**, esančią lauke **Naudoti sujungimo duomenų šaltinį**.
11. Pasirinkite **Gerai**.
12. Peržiūrėkite sugeneruotą failą.

    ![ER vartotojo dialogo puslapis](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>ER formato vykdymo sekimo analizė

1.  Pirmajame „Finance“ arba RCS seanse pasirinkite **Dizaino įrankis**.
2.  Pasirinkite **Našumo sekimas**.
3.  Lentelėje **Našumo sekimas** pasirinkite viršutinį naujausio ER formato vykdymo sekimo įrašą, kuris naudoja dabartinį modelio susiejimo komponentą.
4.  Pasirinkite **Gerai**.

    Atkreipkite dėmesį, kad vykdymo statistika informuoja apie pasikartojančius programos lentelių kvietimus:

    - **ERSolutionTable** buvo iškviesta tiek kartų, kiek yra lentelės **ERSolutionVersionTable** konfigūracijos versijų įrašų, o tokių kvietimų skaičių, siekiant pagerinti našumą, galima sumažinti kartais.
    - **ERVendorTable** buvo iškviesta po du kartus kiekvienam lentelėje **ERSolutionVersionTable** rastam konfigūracijos versijos įrašui, o tokių kvietimų skaičių taip pat galima sumažinti.

    ![ER modelio susiejimo dizaino įrankio puslapis](./media/GER-JoinDS-Set1Run2.PNG)

5.  Uždarykite puslapį.

### <a name="execute-er-format"></a> ER formato vykdymas

1.  Pereikite į žiniatinklio naršyklės skirtuką, kuriame vyksta antrasis „Finance“ arba RCS seansas.
2.  Pasirinkite **Vykdyti**.
3.  Dialogo lange pasirinkite parinktį **Taip**, esančią lauke **Naudoti sujungimo duomenų šaltinį**.
4.  Pasirinkite **Gerai**.
5.  Peržiūrėkite sugeneruotą failą.

    ![ER vartotojo dialogo puslapis](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze"></a> ER formato vykdymo sekimo analizė

1.  Pirmajame „Finance“ arba RCS seanse pasirinkite **Dizaino įrankis**.
2.  Pasirinkite **Našumo sekimas**.
3.  Lentelėje **Našumo sekimas** pasirinkite viršutinį įrašą, atitinkantį naujausią ER formato vykdymo sekimą, kuris naudoja dabartinį modelio susiejimo komponentą.
4.  Pasirinkite **Gerai**.

    Atkreipkite dėmesį, kad vykdymo statistika informuoja apie šiuos veiksmus:

    - Programos duomenų bazė buvo iškviesta vieną kartą siekiant gauti laukus iš lentelių **ERVendorTable**, **ERSolutionTable** ir **ERSolutionVersionTable** ir taip pasiekti reikiamus laukus.

    ![ER modelio susiejimo dizaino įrankio puslapis](./media/GER-JoinDS-Set2Run2.PNG)

    - Programos duomenų bazė buvo iškviesta vieną kartą siekiant apskaičiuoti konfigūracijos versijų skaičių ir tam naudojant sąryšius, sukonfigūruotus duomenų šaltinyje **Details**.

    ![ER modelio susiejimo dizaino įrankio puslapis](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[ER formato vykdymo sekimas siekiant diagnozuoti našumo problemas](trace-execution-er-troubleshoot-perf.md)

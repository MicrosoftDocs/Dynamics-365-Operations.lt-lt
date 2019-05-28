---
title: ER konfigūracijų kūrimas pildymui PDF šablonuose
description: Šioje temoje pateikiama informacija apie tai, kaip sukurti elektroninės ataskaitos (ER) formatą, kad būtų galima pildyti PDF šabloną.
author: NickSelin
manager: AnnBe
ms.date: 04/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1ab6b6ae8a301e24751653dd74fad66417723360
ms.sourcegitcommit: 0400bfd66e98af50e64444a1c102575099a9312f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/09/2019
ms.locfileid: "1539185"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>ER konfigūracijų kūrimas pildymui PDF šablonuose

[!include[banner](../includes/banner.md)]

Šios temos procedūros yra pavyzdžiai, kurie rodo, kaip vartotojas, kuriam priskirtas **sistemos administratoriaus** arba **elektroninių ataskaitų programuotojo** vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, kuris generuoja ataskaitas kaip PDF failus, naudojant pildomus PDF dokumentus kaip ataskaitų šablonus. Šiuos veiksmus galima atlikti bet kurioje „Microsoft Dynamics 365 for Finance and Operations“ arba „Regulatory Configuration Service“ (RCS) įmonėje.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami, turite turėti vieną iš šių prieigos tipų, atsižvelgiant į paslaugą, naudojamą procedūroms užbaigti šioje temoje:

- Prieiga prie „Finance and Operations“ naudojant vieną iš tolesnių vaidmenų.

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

- Prieiga prie RCS naudojant vieną iš tolesnių vaidmenų.

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

Taip pat turite atlikti [Sukurti konfigūracijų teikėją ir jį pažymėti kaip aktyvų](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedūrą.

Galiausiai, turite atsisiųsti šiuos failus iš [CustomerSource](https://go.microsoft.com/fwlink/?linkid=874111).

| Turinio aprašas                       | Failo vardas                                     |
|-------------------------------------------|-----------------------------------------------|
| Pirmo ataskaitos puslapio šablonas | [IntrastatReportTemplate1.pdf](https://mbs.microsoft.com/Files/public/CS)                  |
| Kitų ataskaitos puslapių šablonas    | [IntrastatReportTemplate2.pdf](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatReportTemplate2.pdf)                  |
| ER formato pavyzdys – PDF                          | [Intrastat report (PDF).version.1.1.xml](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatreportPDFversion11.xml)        |
| ER formato pavyzdys – „Excel“                          | [Intrastat (import from Excel).version.1.1.xml](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatimportfromExcelversion11.xml) |
| Pavyzdiniai duomenys                            | [Intrastat sample data.xlsx](https://mbs.microsoft.com/Files/public/CS/AX/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>Formato konfigūracijos kūrimas

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Gaukite prieigą prie „Microsoft“ teikiamų konfigūracijų sąrašo

1. Eikite į **Organizacijos administravimas \> Darbo sritys \> Elektroninės ataskaitos**.
2. Įsitikinkite, kad teikėjas **„Litware, Inc.“** yra galimas ir pažymėtas kaip aktyvus.
3. **„Microsoft“** tiekėjo plytelėje pasirinkite **Saugyklos**.

    > [!NOTE]
    > Jei jau yra **LCS** tipo saugykla, praleiskite likusius šios procedūros veiksmus.

4. Pasirinkite **Įtraukti**.
5. Išplečiamojo dialogo lango laukų grupėje **Konfigūracijos saugyklos tipas** pasirinkite parinktį **LCS**.
6. Pasirinkite **Kurti saugyklą**.
7. Pasirinkite **Gerai**.

### <a name="get-the-model-configurations-provided-by-microsoft"></a>Gaukite „Microsoft“ teikiamas modelio konfigūracijas

1. Puslapio **Konfigūracijos saugyklos** kairėje pusėje pasirinkite mygtuką **Rodyti filtrus** (piltuvėlio simbolį).
2. Įtraukite filtrą **LCS** vertei lauke **Tipas** ir naudokite operatorių **prasideda nuo**.
3. Pasirinkite **Taikyti**.
4. Pasirinkite **Atidaryti**.
5. Medyje pasirinkite **Intrastat (model)**.
6. Sparčiajame skirtuke **Versijos** paspauskite **1**.

    > [!NOTE]
    > Jei nėra mygtuko **Importuoti** sparčiajame skirtuke **Versijos**, praleiskite likusius šios procedūros veiksmus.

7. Pasirinkite **Importuoti**.
8. Pasirinkite **Taip**, jei norite patvirtinti pasirinktos **„Intrastat modelio** versijos modelio konfigūracijos importavimą.

### <a name="create-a-new-format-configuration"></a>Kurti naują formato konfigūraciją

1. Darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.
2. Medyje pasirinkite **Intrastat (model)**.
3. Pasirinkite **Kurti konfigūraciją**.

    > [!NOTE]
    > Jei mygtuko **Kurti konfigūraciją** nėra, turite įjungti dizaino režimą **elektroninių ataskaitų parametrų** puslapyje, kurį galima atidaryti darbo srityje **Elektroninės ataskaitos**.

4. Išplečiamojo dialogo lango laukų grupėje **Naujas** pasirinkite parinktį **Formatas pagal duomenų modelį „Intrastat“**.
5. Lauke **Pavadinimas** įveskite **„Intrastat“ ataskaita (PDF)**.
6. Lauke **Aprašas** įveskite **„Intrastat“ ataskaita PDF formatu**.

    > [!NOTE]
    > Automatiškai įvedamas aktyvios konfigūracijos teikėjas. Šis teikėjas galės prižiūrėti šią konfigūraciją. Nors kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.

7. Pasirinktinai: lauke **Formato tipas** galite pasirinkti specialų elektroninio dokumento formatą. Jei kurdami pasirinksite **PDF**, ER operacijų kūrimo priemonė pasiūlys tik PDF formatu generuojamiems dokumentams taikomus formatavimo elementus (**PDF\Failas**, **PDF\PDF suliejimas** ir t. t.). Jei paliksite šį lauką tuščią, kai ER operacijų kūrimo metu bus įtrauktas pirmo formato elementas, bus nurodytas elektroninio dokumento formatas. Pavyzdžiui, įtraukus **„Excel“\Failas** kaip pirmąjį formato elementą, ER operacijų kūrimo priemonė pateiks tik „Excel“ formatu generuojamiems dokumentams taikomus formatavimo elementus (**„Excel“\Langelis**, **„Excel“\Diapazonas** ir t. t.). formatas.
8. Pasirinkite **Kurti konfigūraciją**.

Sukuriama nauja ER formato konfigūracija. Galite naudoti šios konfigūracijos juodraštinę versiją, kad galėtumėte Išsaugoti ER formato komponentą, kuris sukurtas generuoti elektroninius dokumentus PDF formatu.

### <a name="design-the-format-of-an-electronic-document"></a>Kurti elektroninio dokumento formatą

Tada savo sukurtoje ER formato konfigūracijoje, sukursite ER formatą, kuris sugeneruoja **„Intrastat“ valdymo** ataskaitą PDF formatu. Pirmame šios ataskaitos puslapyje turi būti rodoma ataskaitos suvestinė ir išsami informacija apie užregistruotas užsienio prekybos operacijas. Kituose puslapiuose turi būti rodoma tik informacija apie užsienio prekybos operacijas, apie kurias pranešta. Kadangi sugeneruotose ataskaitos puslapiuose turi būti skirtingi maketai, ER formatui bus naudojami du skirtingi PDF formato šablonai.

Bet kurioje PDF peržiūros programoje atsidarykite PDF šablonus, kuriuos atsisiuntėte. Atkreipkite dėmesį, kad kiekviename šablone yra keli laukai, kuriuos reikia užpildyti. Kiekvieno šablono informacija apie užsienio prekybos operacijas pateikiama kaip 42 eilutės, kurių kiekvienoje yra devyni laukai. Eilutės numeris pasirodo kiekvieno lauko pavadinimo pabaigoje (pvz., **Data 1**…**Data 42** ir **Prekė 1**…**Prekė 42**).

Šioje iliustracijoje rodomas pirmasis PDF šablono ataskaitos puslapis.

![Šablonas 1](media/rcs-ger-filloutpdf-template1.png)

Šioje iliustracijoje rodomi kiti PDF šablono ataskaitos puslapiai.

![Šablonas 2](media/rcs-ger-filloutpdf-template2.png)

1. Puslapyje **Konfigūracijos** pasirinkite **Dizaino įrankis**.
2. Pasirinkite **Įtraukti šaknį**.
3. Išplečiamojo dialogo lango medyje pasirinkite **PDF \>PDF suliejimas**.

    Kai pasirenkate **PDF suliejimo** elementą kaip šakninį formato elementą, visi PDF dokumentai, sugeneruoti vykdymo metu, bus sulieti į vieną galutinį PDF dokumentą. Jeigu jums reikia tik vieno PDF šablono, kad būtų galima sugeneruoti visus reikalingus dokumentus, naudojant jūsų sukurtą ER formatą, galite pasirinkti šakninį elementą **PDF failas**.

4. Lauke **Pavadinimas** įveskite **Išvestis**.
5. Lauke **Kalbos nuostatos** pasirinkite **Vartotojo nuostata**. Ataskaita bus sugeneruota ją vykdančio vartotojo pageidaujama kalba.
6. Lauke **Kultūros nuostatos** pasirinkite **Vartotojo nuostata**. Ataskaitos puslapiuose pateiktos vertės ir datos bus formatuojamos pagal pageidaujamą vartotojo, kuris vykdo ataskaitą, vietą.
7. Pasirinkite **Gerai**.
8. Veiksmų srities skirtuke **Importavimas** pasirinkite **Importuoti iš PDF**.

    Kai pildomas PDF dokumentas importuojamas kaip šablonas šiam ER formatui, visi reikiami konkretaus formato elementai (**PDF failas**, **Laukų grupė**ir **Laukas**) automatiškai sukuriami formatu, kuris yra sukurtas, remiantis importuoto PDF dokumento struktūra.

9. Pasirinkite **Naršyti**. Naršykite ir pasirinkite **IntrastatReportTemplate1.pdf** failą, kurį anksčiau atsisiuntėte kaip būtinąjį komponentą.
10. Pasirinkite **Gerai**.

    Pasirinktas failas yra įkeliamas ir užpildomas laukas **Šablonas** dialogo lange lango **Importuoti iš PDF**.

11. Parinktį **Grupuoti laukus** nustatykite kaip **Taip**. Jei pasirinktame PDF dokumente yra bet kokios laukų grupės, jos bus naudojamos sukurtiem ER formato elementams grupuoti. Šiuo tikslu bus sukurtas formato elementas **Laukų grupė**.

    Jei ši pasirinktis nustatyta kaip **Ne**, reikiami ER formato elementai bus sukurti kaip standartinis sąrašas elementų, įdėtų po sukurtu **PDF failo** formato elementu.

12. Pasirinkite **Gerai**.

    ![Importuoti iš PDF dialogo lango](media/rcs-ger-filloutpdf-importtemplate.png)

13. Medyje išplėskite **Išvestis**.

    Turėkite omenyje, kad komponentas **PDF failas** automatiškai sukurtas valdyti pirmojo vykdant sugeneruotos ataskaitos puslapio kūrimą.

14. Medyje išplėskite **Išvestis \> PDF failas**.

    Atkreipkite dėmesį, kad formato elementų struktūrinis sąrašas yra sukurtas automatiškai šiuo ER formatu, remiantis pildomo PDF dokumento, kurį importavote anksčiau, struktūra.

15. Medyje pasirinkite **Išvestis \> PDF failas**.
16. Lauke **Pavadinimas** įveskite **Puslapis 1**.

    Šis formato elementas bus naudojamas generuoti pirmąjį ataskaitos **„Intrastat“ kontrolė** puslapį. Šiame puslapyje bus rodoma ataskaitos suvestinė ir informacija apie užsienio prekybos operacijas.

    Jei paliksite lauką **Kalbos nuostatos** tuščią, ataskaitos, sukurtos naudojant šį formato elementą, kalba bus nustatyta pagal pirminio elemento **PDF Merger** parametrą **Kalbos nuostatos**. Galite pasirinkti kitą vertę, kad būtų nepaisoma pirminio elemento parametro.

    Jei paliksite lauką **Kultūros nuostatos** tuščią, ataskaitos, sukurtos naudojant šį formato elementą, kalba bus nustatyta pagal pirminio elemento **PDF Merger** parametrą **Kultūros nuostatos**. Lokalė nustato verčių ir datų formatą ataskaitos puslapiuose. Galite pasirinkti kitą vertę, kad būtų nepaisoma pirminio elemento parametro.

17. Veiksmų srityje pasirinkite skirtuką **Importuoti**. Turėkite omenyje, kad mygtukas **Atnaujinti iš PDF** tapo prieinamas pasirinktam formato elementui **PDF failas.**

    Šį mygtuką galite naudoti atnaujintam PDF šablonui importuoti į redaguotą formatą. Kai atnaujinamas PDF šablonas importuojamas, formato elementų sąrašas atitinkamai pasikeis:

    - Visiems naujiems laukams atnaujintame PDF šablone sukuriami nauji formato elementai redaguotu ER formatu.
    - Jei atnaujintuose PDF šablonuose nebėra laukų, kurie atitinka visus esamus formato elementus, esančius redaguoto formato formatu, šie formato elementai panaikinami iš ER formato.

18. Skirtuke **Formatas** pasirinkite **Priedai.**

    Atkreipkite dėmesį, kad importuotas PDF dokumentas pridedamas prie redaguoto ER formato.

    ![PDF priedo peržiūra](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. Norėdami tęsti formato kūrimą, importuokite antrą PDF šabloną, pridėdami reikiamus susiejimus su duomenų šaltiniais ir pan.
20. Pasirinkite **Įrašyti**.
21. Uždarykite puslapį.
22. Pasirinkite **Naikinti**.
23. Pasirinkite **Taip**.

Norėdami sužinoti, kaip naudoti formato elementus **PDF suliejimas**, **PDF failas**, **Laukų grupė** ir **Laukas** dokumentams generuoti PDF formatu, galite importuoti ir analizuoti pavyzdinį ER formatą.

### <a name="import-the-format-configuration"></a>Importuoti formato konfigūraciją

Tada importuosite anksčiau atsisiųstą pavyzdinį ER formatą, kad sugeneruotumėte **„Intrastat“ kontrolės** ataskaitą PDF formatu. Pirmame šios ataskaitos puslapyje turi būti rodoma ataskaitos suvestinė ir išsami informacija apie užregistruotas užsienio prekybos operacijas. Kituose puslapiuose turi būti rodoma tik informacija apie užsienio prekybos operacijas, apie kurias pranešta.

1. Puslapyje **Konfigūracijos** pasirinkite **Keitimas \> Įkelti iš XML failo**.
2. Pasirinkite **Naršyti**. Naršykite ir pasirinkite **Intrastat report (PDF).version.1.1.xml** failą, kurį anksčiau atsisiuntėte kaip būtinąjį komponentą.
3. Pasirinkite **Gerai**.

## <a name="analyze-the-format-configuration"></a>Analizuoti formato konfigūraciją

### <a name="format-layout"></a>Maketo formatavimas

1. Puslapyje **Konfigūracijos** esančiame medyje pasirinkite **„Intrastat“ modelis \> „Intrastat“ ataskaita (PDF)**.
2. Pasirinkite **Dizaino įrankis**.
3. Pasirinkite **Rodyti informaciją**.
4. Medyje išplėskite **Išvestis: PDF suliejimas**.

    Atkreipkite dėmesį, kad šiame ER formate yra su **PDF failas** elementai, kurie naudoja skirtingus PDF šablonus. Vienas šablonas naudojamas kuriant pirmą ataskaitos puslapį PDF formatu, o kitas šablonas naudojamas kitiems puslapiams generuoti.

5. Medyje išplėskite **Išvestis: PDF suliejimas \> Puslapis 1: PDF failas (IntrastatReportTemplate1)**.
6. Medyje išplėskite **Išvestis: PDF suliejimas \> Puslapis N: PDF failas (IntrastatReportTemplate2)**.

    Turėkite omenyje, kad kadangi dviejų PDF šablonų turinys skiriasi, taip pat skiriasi ir dviejų **PDF failas** elementų įdėtųjų formato elementų struktūra.

### <a name="format-mapping"></a>Formato susiejimas

1. Puslapyje **Formato kūrimo įrankis** pasirinkite skirtuką **Susiejimas**.
2. Medyje išplėskite **Puslapių kaita \> Puslapiai**.

    ![Formulės kūrimo įrankio puslapis su išplėstu medžio modeliu](media/rcs-ger-filloutpdf-reviewformat.png)

    Įsidėmėkite toliau pateiktą informaciją.

    - **PDF failas** tipo formato elementas **Išvestis \> Puslapis 1** nėra susietas su jokiu duomenų šaltiniu ir šio formato elemento **Įjungta** išraiška yra tuščia. Todėl vykdant **IntrastatReportTemplate1** PDF šablonas užpildytas tik vieną kartą, sugeneravus atskirą PDF dokumentą.
    - **PDF failas** tipo formato elementas **Išvestis \> Puslapis N** yra susietas su **Įrašų sąrašo** tipo duomenų šaltiniu **Puslapių kaita.PuslapisN** ir šio formato elemento **Įjungta** išraiška yra tuščia. Todėl vykdant **IntrastatReportTemplate2** PDF šablonas užpildytas kiekvienam įrašui iš susieto įrašų sąrašo, kai sugeneruojamas atskiras PDF dokumentas.
    - Kadangi formato elementai **Puslapis 1: PDF failas** ir **Puslapis N: PDF failas** yra antriniai formato elemento **Išvestis: PDF suliejimas** elementai, visi užpildyti PDF dokumentai bus sulieti į vieną galutinį PDF dokumentą.
    - Duomenų šaltiniai **Puslapių kaita.Puslapis1** ir **Puslapių kaita.PuslapisN** yra sukonfigūruoti kaip įrašų filtrai iš duomenų šaltinio **Puslapių kaita.Puslapiai**. Šis duomenų šaltinis sukonfigūruotas išskaidyti visą užsienio prekybos operacijų rinkinį į paketus. Kiekviename pakete yra iki 42 įrašų. Šios ER išraiškos naudojamos norint išskaidyti operacijas į paketus:

        SPLITLIST(Totals.CommodityRecord,42)

    - Duomenų šaltinyje **Puslapių kaita.Puslapiai** yra elementas **Puslapių kaita.Puslapiai.Sunumeruoti**, kuris pateikia visų paketo įrašų informaciją. Šią informaciją sudaro įrašo seka dabartiniame pakete (lauke **Puslapių kaita.Puslapiai.Sunumeruoti.Numeris**). Laukas **Puslapių kaita.Puslapiai.Sunumeruoti.Numeris** naudojamas formato elementų **PDF laukas** išraiškoje **Pavadinimas** dinamiškai sugeneruoti laiko pavadinimą, paremtą operacijos numeriu pakete. Tada sugeneruotas lauko pavadinimas naudojamas užpildyti tinkamą PDF lauką naudojamame PDF šablone.
    - **PDF grupė** tipo formato elementas **Išvestis \> Puslapis N \> Informacija 2** yra susietas **Įrašų sąrašas** tipo duomenų šaltiniu **Puslapių kaita.Puslapiai.Sunumeruoti** (arba **\@.Sunumeruoti**, jei naudojamas rodinio režimas **Santykinis kelias**). Todėl vykdant įdėtieji šios PDF grupės elementai bus užpildyti kiekvienu įrašu iš susietų įrašų sąrašo. Tokiu būdu, atskiros PDF eilutės virtualiai generuojamos, kai sąrašo **Puslapių kaita.Puslapiai.Sunumeruoti** kiekvienam N iš 42 įrašų užpildomi šie PDF laukai: Data N, Kryptis N, Prekė N ir t. t. Todėl šiuo atžvilgiu šios **Laukų grupė** formato elemento veikimas primena formato elementų **XML \> Seka** ir **Tekstas \> Seka** veikimą.

3. Medyje išplėskite **Išvestis \> Puslapis N \> Informacija2**.
4. Medyje pasirinkite **Išvestis \> Puslapis N \> Informacija 2 \> PageFooter.**

    Turėkite omenyje, kad šio formato elemento atributas **Pavadinimas** apibrėžiamas kaip **PageFooter**. Taip pat atkreipkite dėmesį, kad formato elemento išraiška **Pavadinimas** yra tuščia.

5. Medyje pasirinkite **Išvestis \> Puslapis N \> Informacija 2 \> Taisymas 1.**

    Turėkite omenyje, kad šio formato elemento atributas **Pavadinimas** apibrėžiamas kaip **Taisymas 1**. Taip pat atkreipkite dėmesį, kad formato elemento išraiška **Pavadinimas** apibrėžta kaip **Puslapių kaita.Lauko pavadinimas(„Taisymas“,\@.Numeris)**.

![Formato kūrimo įrankis, kur pažymimas susiejimas](media/rcs-ger-filloutpdf-reviewformat2.png)

Atkreipkite dėmesį formato elementas **Laukas** naudojamas užpildyti atskirus laukus pildomame PDF dokumente, apibrėžtame kaip formato elemento **PDF failas** šablonas. Formato elemento **PDF failas** arba į jį įdėtų elementų formato elementų, jei jis jų turi, susiejimas nurodo vertę, įvestą atitinkamuose PDF laukuose. Skirtingos formato elemento **Laukas** ypatybės gali būti naudojamos nurodyti, kuris PDF laukas užpildomas atskiru formato elementu:

- Skirtuko **Formatas** formato elemento atributas **Pavadinimas**
- Skirtuko **Susiejimas** formato elemento išraiška **Pavadinimas**

Kadangi abi ypatybės yra pasirinktinės formato elementui **Laukas**, tiksliniam PDF laukui nurodyti taikomos šios taisyklės:

- Jei atributas **Pavadinimas** yra tuščias, o išraiška **Pavadinimas** vykdymo metu pateikia tuščią eilutę, vykdymo metu pateikiama išimtis, nurodanti vartotojui, kad PDF lauko nepavyksta rasti PDF šablone, kuris naudojamas pildyti PDF dokumentui.
- Jei nurodytas atributas **Pavadinimas**, bet išraiška **Pavadinimas** yra tuščia, PDF laukas, kurio pavadinimas sutampa su formato elemento atributu **Pavadinimas**, yra užpildytas.
- Jei nurodytas atributas **Pavadinimas**, bet išraiška **Pavadinimas** yra sukonfigūruota, PDF laukas, kurio vertę pateikia formato elemento išraiška **Pavadinimas**, yra užpildytas.

> [!NOTE]
> PDF žymės langelis gali būti pažymėtas šiais būdais:
>
> - Kai atitinkamas formato elementas **Laukas** susietas su **Boolean** duomenų tipo duomenų šaltinio lauku, kurio vertė **True**
> - Kai atitinkamas formato elementas **Laukas** turi įdėtąjį formato elementą **Eilutė**, susietą duomenų šaltinio lauku, kurio tekstinė vertė yra **1**, **True** arba **Taip**

## <a name="run-the-format-configuration"></a>Formato konfigūracijos vykdymas

### <a name="import-the-format-configuration"></a>Importuoti formato konfigūraciją

Tada įkelsite pavyzdinį ER formatą **„Intrastat“ (importuoti iš „Excel“)**. Šis formatas skirtas vartotojo pasirinktai „Microsoft Excel“ darbaknygei, kuri imituoja užsienio prekybos operacijas, analizuoti.

1. Puslapyje **Konfigūracijos** pasirinkite **Keitimas \> Įkelti iš XML failo**.
2. Pasirinkite **Naršyti**. Naršykite ir pasirinkite **Intrastat (import from Excel).version.1.1.xml** failą, kurį anksčiau atsisiuntėte kaip būtinąjį komponentą.
3. Pasirinkite **Gerai**.
4. Medyje pasirinkite **„Intrastat“ modelis \> „Intrastat“ (importuoti iš „Excel“)**.
5. Pasirinkite **Redaguoti**.
6. Nustatykite parinktį **Numatytasis modelių susiejimui** į **Taip**.

    > [!NOTE]
    > Jeigu anksčiau nustatėte parinktį **Numatytasis modelių susiejimui** į **Taip**, kad būtų galima naudoti **„Intrastat“ modelis** konfigūraciją arba kitą konfigūraciją, įdėtą į **„Intrastat“ modelis** konfigūraciją, nustatykite pasirinktį **Ne**.

    Kai parinktis **Numatytasis modelių susiejimui** parinktis yra nustatyta į **Taip**, importuotas ER formatas **„Intrastat“ (importuoti iš „Excel“)** yra priskiriamas kaip numatytasis duomenų šaltinis formato konfigūracijai **„Intrastat“ ataskaita (PDF)**. Tada, kai vykdoma formato konfigūracija **„Intrastat“ ataskaita (PDF)**, „Excel“ darbaknygės turinys, kurį išanalizavo **„Intrastat“ (importuoti iš „Excel“)** ER formatas, modeliuos užsienio prekybos operacijas, apie kurias privaloma pranešti. Toliau pateikiamoje iliustracijoje rodomas „Excel“ darbaknygės pavyzdys.

    ![„Excel“ darbaknygė, kurioje yra duomenų pavyzdžių](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>Formato konfigūracijos vykdymas

1. Puslapyje **Konfigūracijos** esančiame medyje pasirinkite **„Intrastat“ modelis \> „Intrastat“ ataskaita (PDF)**.
2. Pasirinkite **Vykdyti**.
3. Pasirinkite **Naršyti**. Naršykite ir pasirinkite **Intrastat sample data.xlsx** failą, kurį anksčiau atsisiuntėte kaip būtinąjį komponentą.
4. Pasirinkite **Gerai**.
5. Lauke **Ataskaitos kryptis** pasirinkite **Abi**, kad užpildytumėte visas operacijas iš importuotos „Excel“ darbaknygės sugeneruotoje PDF ataskaitoje.
6. Pasirinkite **Gerai**.
7. Peržvelkite sugeneruotą PDF dokumentą.

Šioje iliustracijoje rodomas pavyzdys, kaip generuojamas pirmasis ataskaitos puslapis.

![Pirmasis sugeneruotos ataskaitos puslapis](media/rcs-ger-filloutpdf-generatedreport.png)

Šioje iliustracijoje rodomas pavyzdys, kaip generuojamas kitas ataskaitos puslapis.

![Kitas sugeneruotos ataskaitos puslapis](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="additional-resources"></a>Papildomi ištekliai

- [ER: konfigūracijos, skirtos generuoti ataskaitoms OPENXML formatu, kūrimas](tasks/er-design-reports-openxml-2016-11.md)
- [ER konfigūracijų kūrimas siekiant generuoti ataskaitas „Microsoft WORD“ formatu](tasks/er-design-configuration-word-2016-11.md)

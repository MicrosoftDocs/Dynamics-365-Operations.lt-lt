---
title: ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas
description: Šioje temoje pateikiama informacijos apie tai, kaip elektroninėse ataskaitose (ER) naudojantis našumo sekimo funkcija spręsti našumo problemas.
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 23b965bb51a4323164ae52bf70050133c9c9c9da
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344887"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas

[!include[banner](../includes/banner.md)]

Kurdami elektroninių ataskaitų (ER) konfigūracijas, kuriomis naudojantis generuojami elektroniniai dokumentai, nurodote būdą, kuriuo naudodamiesi gaunate duomenis iš programos, ir įvedate jį į sugeneruotą išvestį. Naudojantis ER našumo sekimo funkcija gali pastebimai sutrumpėti laikas, per kurį renkama informacija apie ER formato vykdymą, panaudojant ją našumo problemoms spręsti, ir gali būti patiriama mažiau išlaidų. Šioje mokymo programoje pateikiama rekomendacijų apie tai, kaip atsižvelgti į įvykdytų ER formatų našumo sekimus ir kaip panaudoti šiuos sekimus siekiant pagerinti našumą.

## <a name="prerequisites"></a>Būtinieji komponentai

Norint įvykdyti šios mokymo programos pavyzdžių užduotis, reikia toliau nurodytų prieigų.

- Prieiga prie vieno iš toliau pateikiamų vaidmenų.

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

- Prieiga prie „Regulatory Configuration Services“ (RCS) egzemplioriaus, sukonfigūruoto tam pačiam nuomininkui, kuriam sukonfigūruota programa, vienam iš toliau nurodytų vaidmenų atlikti.

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

Taip pat turite atsiųsti ir vietoje saugoti toliau nurodytus failus.

| Failas                                  | Turinys                               |
|---------------------------------------|---------------------------------------|
| Našumo sekimo modelis.versija.1     | [ER duomenų modelio konfigūracijos pavyzdys](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| Našumo sekimo metaduomenys.versija.1  | [ER metaduomenų konfigūracijos pavyzdys](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| Našumo sekimo susiejimas.versija.1.1 | [ER modelio susiejimo konfigūracijos pavyzdys](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| Našumo sekimo formatas.versija.1.1  | [ER formato konfigūracijos pavyzdys](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a>ER parametrų konfigūravimas

Kiekvienas programoje sugeneruotas ER našumo sekimas saugomas kaip vykdymo žurnalo įrašo priedas. Šiems priedams tvarkyti naudojama dokumentų tvarkymo (DM) sistema. Norėdami nurodyti DM dokumento tipą, kuris turėtų būti naudojamas našumo sekimams pridėti, turite iš anksto sukonfigūruoti ER parametrus. Darbo srityje **Elektroninės ataskaitos** pasirinkite **Elektroninių ataskaitų parametrai**. Tada puslapyje **Elektroninių ataskaitų parametrai** esančio skirtuko **Priedai** lauke **Kiti** pasirinkite DM dokumento tipą, kuris bus naudojamas našumo sekimui.

![Elektroninių ataskaitų parametrų puslapis.](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

Norint, kad DM dokumento tipu būtų galima naudotis peržvalgos lauke **Kiti**, jis turi būti atitinkamai sukonfigūruotas puslapyje **Dokumentų tipai** (**Organizacijos administravimas \> Dokumentų valdymas \> Dokumentų tipai**):

- **Klasė:** pridėti failą
- **Grupė:** failas

![Puslapis Dokumentų tipai.](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> Pasirinktas dokumento tipas turi būti pasiekiamas visose dabartinio egzemplioriaus įmonėse, nes DM priedai skirti konkrečioms įmonėms.

### <a name="configure-rcs-parameters"></a>RCS parametrų konfigūravimas

Sugeneruoti ER našumo sekimai importuojami į RCS analizei atlikti naudojant ER formato dizaino įrankį ir ER susiejimo dizaino įrankį. Kadangi ER našumo sekimai saugomi kaip su ER formatu susieto vykdymo žurnalo įrašo priedai, reikia iš anksto konfigūruoti RCS parametrus, kad būtų nurodytas DM dokumento tipas, kuris turėtų būti naudojamas našumo sekimams pridėti. Jūsų įmonei sukurto RCS egzemplioriaus darbo srityje **Elektroninės ataskaitos** pasirinkite **Elektroninių ataskaitų parametrai**. Tada puslapyje **Elektroninių ataskaitų parametrai** esančio skirtuko **Priedai** lauke **Kiti** pasirinkite DM dokumento tipą, kuris bus naudojamas našumo sekimui.

![RCS elektroninių ataskaitų parametrų puslapis.](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

Norint, kad DM dokumento tipu būtų galima naudotis peržvalgos lauke **Kiti**, jis turi būti atitinkamai sukonfigūruotas puslapyje **Dokumentų tipai** (**Organizacijos administravimas \> Dokumentų valdymas \> Dokumentų tipai**):

- **Klasė:** pridėti failą
- **Grupė:** failas

## <a name="design-an-er-solution"></a>ER sprendimo kūrimas

Tarkime, kad jau pradėjau kurti naują ER sprendimą, kad būtų sugeneruota nauja ataskaita, kurioje pateikiamos tiekėjo operacijos. Šiuo metu pasirinkto tiekėjo operacijas rasite puslapyje **Tiekėjo operacijos** (eikite į **Mokėtina suma \> Tiekėjai \> Visi tiekėjai**, pasirinkite tiekėją, paskui veiksmų srities skirtuko **Tiekėjas** grupėje **Operacijos** pasirinkite **Operacijos**). Tačiau norite vienu metu turėti visas tiekėjo operacijas viename elektroniniame dokumente XML formatu. Šį sprendimą sudaro kelios ER konfigūracijos, apimančios reikiamą duomenų modelį, metaduomenis, modelio susiejimą ir formato komponentus.

1. Prisijunkite prie jūsų įmonei sukurto RCS egzemplioriaus.
2. Šioje mokymo programoje kursite ir modifikuosite pavyzdinės įmonės **„Litware, Inc.“** konfigūracijas. Todėl įsitikinkite, kad šis konfigūracijos teikėjas buvo pridėtas prie RCS ir pasirinktas kaip aktyvus. Instrukcijos aprašytos procedūroje [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.
4. Puslapyje **Konfigūracijos** importuokite į RCS kaip būtinąjį komponentą atsisiųstas ER konfigūracijas tokia tvarka: duomenų modelis, metaduomenys, modelio susiejimas, formatas. Kurdami kiekvieną konfigūraciją atlikite toliau nurodytus veiksmus.

    1. Veiksmų srityje pasirinkite **Keitimas \> Įkelti iš XML failo**.
    2. Paspaudę **Naršyti** pasirinkite reikiamą ER konfigūracijos failą XML formatu.
    3. Pasirinkite **Gerai**.

    ![RCS puslapis Konfigūracijos.](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>ER vykdymo sekimo sprendimo vykdymas

Tarkime, kad baigėte kurti pirmąją ER sprendimo versiją. Dabar norite ją patikrinti naudodami savo egzempliorių ir išanalizuoti vykdymo našumą.

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a>ER konfigūracijų importavimas iš RCS į „Finance and Operations”

1. Prisijunkite prie programos egzemplioriaus.
2. Dirbdami su šia mokymo programa, konfigūracijas importuosite iš savo RCS egzemplioriaus (kuriame kuriate savo ER komponentus) į savo egzempliorių (kuriame jas tikrinate ir galiausiai naudojate). Todėl turite įsitikinti, kad paruošti visi reikiami artefaktai. Instrukcijas rasite procedūroje [Elektroninių ataskaitų (ER) konfigūracijų importavimas iš „Regulatory Configuration Services“ (RCS)](rcs-download-configurations.md).
3. Atlikdami toliau nurodytus veiksmus importuokite konfigūracijas iš RCS į programą.

    1. Darbo srityje **Elektroninės ataskaitos** konfigūracijos tiekėjui **„Litware, Inc.“** skirtoje plytelėje pasirinkite **Saugyklos**.
    2. Puslapyje **Konfigūracijų saugykla** pasirinkite tipo **RCS** saugyklą, paskui pasirinkite **Atidaryti**.
    3. „FastTab“ **Konfigūracijos** pasirinkite konfigūraciją **Našumo sekimo formatas**.
    4. „FastTab“ **Versijos** pasirinkite pasirinktos ER konfigūracijos versiją **1.1**, paskui pasirinkite **Importuoti**.

    ![Konfigūracijos saugyklos puslapis.](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

Atitinkamų versijų duomenų modeliai ir modelio susiejimo konfigūracijos automatiškai importuojami kaip būtinieji importuotos ER formato konfigūracijos komponentai.

### <a name="turn-on-the-er-performance-trace"></a>ER veiklos sekimo įjungimas

1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Dialogo lango **Vartotojo parametrai** skyriuje **Vykdymo sekimas** atlikite toliau nurodytus veiksmus.

    1. Lauke **Vykdymo sekimo formatas** nurodykite sugeneruoto našumo sekimo formatą, kurio vykdymo informacija turėtų būtų saugoma ER formatui ir susiejimo elementams:

        - **Derinti sekimo formatą** – pasirinkite šią reikšmę, jei planuojate interaktyviai paleisti ER formatą, turintį trumpą vykdymo laiką. Tada pradedamas išsamios ER formato vykdymo informacijos rinkinys. Pasirinkus šią reikšmę, našumo sekimas surenka informaciją apie laiką, praleistą toliau nurodytiems veiksmams atlikti:

            - Kiekvieno duomenims gauti iškviesto modelio susiejimo duomenų šaltinio vykdymas
            - Kiekvieno formato elemento apdorojimas įvedant duomenis į sugeneruotą išvestį

            Jei pasirenkate **Derinti sekimo formatą** reikšmę, galėsite analizuoti sekimo turinį ER operacijų dizaino įrankyje. Ten galite peržiūrėti ER formatą arba susiejimo elementus, kurie nurodyti sekime.

        - **Agreguotas sekimo formatas** – pasirinkite šią reikšmę, jei planuojate paleisti ER formatą, turintį ilgą vykdymo laiką paketiniu režimu. Tada pradedamas agreguotos išsamios ER formato vykdymo informacijos rinkinys. Pasirinkus šią reikšmę, našumo sekimas surenka informaciją apie laiką, praleistą toliau nurodytiems veiksmams atlikti:

            - Kiekvieno duomenims gauti iškviesto modelio susiejimo duomenų šaltinio vykdymas
            - Kiekvieno duomenims gauti iškviesto formato susiejimo duomenų šaltinio vykdymas
            - Kiekvieno formato elemento apdorojimas įvedant duomenis į sugeneruotą išvestį

            **Agreguoto sekimo formato** reikšmė galima 10.0.20 ir vėlesnėse „Microsoft Dynamics 365 Finance” versijose.

            ER formato dizaino įrankyje ir ER modelio susiejimo dizaino įrankyje galite peržiūrėti bendrą vieno komponento vykdymo laiką. Be to, sekimas apima išsamią vykdymo informaciją, pavyzdžiui, vykdymų skaičių ir minimalų bei maksimalų vieno vykdymo laiką.

            > [!NOTE]
            > Šis sekimas yra surenkamas remiantis sekamų komponentų maršrutu. Todėl statistiniai duomenys gali būti klaidingi, kai viename pirminiame komponente yra keli antriniai komponentai, neturintys pavadinimo, arba kai keli antriniai komponentai yra to paties pavadinimo.

    2. Nustatykite tolesnių parinkčių reikšmes **Taip**, kad būtų galima rinkti konkrečią informaciją apie ER modelio susiejimo vykdymą ir ER formato komponentus.

        - **Rinkti užklausų statistiką** – įjungus šią parinktį, našumo sekimas renka toliau nurodytą informaciją.

            - Duomenų šaltinių atliktų duomenų bazės iškvietimų skaičius
            - Pasikartojančių iškvietimų į duomenų bazę skaičius
            - Informacija apie duomenų bazės iškvietimams atlikti naudotus SQL išrašus

        - **Talpyklos sekimo prieiga** – įjungus šią parinktį, našumo sekimas renka informaciją apie ER modelio susiejimo talpyklos naudojimą.
        - **Sekimo duomenų prieiga** – įjungus šią parinktį, našumo sekimas renka informaciją apie iškvietimų į įvykdytų įrašo sąrašo tipo duomenų šaltinių duomenų bazę skaičių.
        - **Sekimų sąrašo išvardijimas** – įjungus šią parinktį, našumo sekimas renka informaciją apie iš įrašo sąrašo tipo duomenų šaltinių pageidaujamų įrašų skaičių.

    > [!NOTE]
    > Dialogo lange **Vartotojo parametrai** nurodyti vartotojo ir dabartinės įmonės parametrai.

    ![Vartotojo parametrų dialogo langas.](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a>ER formato vykdymas

1. Pasirinkite įmonę **DEMF**.
2. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
3. Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite elementą **Našumo sekimo formatas**.
4. Veiksmų srityje pasirinkite **Vykdyti**.

Atkreipkite dėmesį, kad sugeneruotame faile pateikiama informacijos apie 265 šešių tiekėjų operacijas.

## <a name="review-the-execution-trace"></a>Vykdymo sekimo peržiūra

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a>Sugeneruotos sekimo programos eksportavimas iš programos

Našumo sekimai atsiejami nuo šaltinio ER formato ir gali būti išdėstyti eilutėmis išoriniame ZIP faile.

1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos derinimo žurnalai**.
2. Puslapio **Elektroninių ataskaitų vykdymo žurnalai** kairiosios srities lauke **Konfigūracijos pavadinimas** pasirinkite **Našumo sekimo formatą**, kad rastumėte žurnalo įrašus, sugeneruotus vykdant konfigūraciją **Našumo sekimo formatas**.
3. Paspauskite viršutiniame dešiniajame puslapio kampe esantį mygtuką (sąvaržėlės simbolis) **Priedai** arba paspauskite **Ctrl+Shift+A**.

    ![Puslapio Elektroninių ataskaitų vykdymo žurnalai mygtukas Priedai.](./media/GER-PerfTrace-GER-DebugLog.png)

4. Norėdami gauti našumo sekimą kaip ZIP failą ir saugoti jį vietoje, puslapio **Elektroninių ataskaitų vykdymo žurnalų priedai** veiksmų srityje pasirinkite **Atidaryti**.

    ![Elektroninių ataskaitų vykdymo žurnalų priedai.](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> Sugeneruotame sekime yra nuoroda į šaltinio ER ataskaitą naudojant unikalų ataskaitos identifikatorių tik **GUID** formatu. Į formato versijos numeravimą neatsižvelgiama.

Atkreipkite dėmesį, kad ryšys tarp įvykdyto ER formatui sugeneruoto našumo sekimo ir ER modelio susiejimo paremtas naudotu šakniniu aprašu ir bendru duomenų modeliu. Į formato ir modelio susiejimo versijos numeravimą neatsižvelgiama. Taip pat neatsižvelgiama į modelio susiejimo žymę **Numatytasis modelių susiejimui**.

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a>Sugeneruoto sekimo importavimas į RCS

1. RCS darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.
2. Puslapio **Konfigūracijos** konfigūracijų medyje išplėskite elementą **Našumo sekimo modelis** ir pasirinkite elementą **Našumo sekimo formatas**.
3. Veiksmų srityje pasirinkite **Dizaino įrankis**.
4. Puslapio **Formato dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.
5. Dialogo lange **Našumo sekimo rezultato parametrai** pasirinkite **Importuoti našumo sekimą**.
6. Pasirinkite **Naršyti** ir pasirinkite ZIP failą, kurį eksportavote anksčiau.
7. Pasirinkite **Gerai**.

    ![Našumo sekimo rezultato parametrų dialogo langas, esantis RCS.](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>Našumo sekimo naudojimas analizei naudojantis RCS – Formato vykdymas

1. RCS puslapyje **Formato dizaino įrankis** pasirinkę **Išplėsti / sutraukti** išplėskite visų formato elementų turinį.

    Atkreipkite dėmesį, kad rodoma papildomos informacijos apie kai kuriuos dabartinio formato elementus.

    - Faktinis laikas, sugaištas įvedant duomenis į sugeneruotą išvestį naudojant formato elementą
    - Tas pats laikas išreikštas kaip viso laiko, praleisto generuojant visą išvestį, procentinė dalis

    ![RCS formato dizaino įrankio puslapis.](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. Uždarykite puslapį **Formato dizaino įrankis**.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a>Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas

1. RCS puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite elementą **Našumo sekimo susiejimas**.
2. Veiksmų srityje pasirinkite **Dizaino įrankis**.
3. Pasirinkite **Dizaino įrankis**.
4. Puslapio **Modelio susiejimo dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.
5. Pasirinkite anksčiau importuotą sekimą.
6. Pasirinkite **Gerai**.

Atkreipkite dėmesį, kad atsiranda naujos informacijos apie kai kuriuos dabartinio modelio susiejimo duomenų šaltinio elementus.

- Faktinis laikas, sugaištas gaunant duomenis naudojant duomenų šaltinį
- Tas pats laikas, išreikštas kaip viso laiko, praleisto vykdant visą modelio susiejimą, procentinė dalis

Atkreipkite dėmesį, kad ER informuoja tuo atveju, kai dabartinis modelio susiejimas sutampa su duomenų bazės užklausomis, kai paleistas duomenų šaltinis VendTable/\<Relations/VendTrans.VendTable\_AccountNum. Šis pasikartojimas įvyksta todėl, kad kiekvieno pasikartojančio tiekėjo įrašo atveju tiekėjo operacijų sąrašas iškviečiamas du kartus.

- Vienas iškvietimas atliekamas norint į duomenų modelį įvesti informaciją apie kiekvieną operaciją pagal sukonfigūruotus susiejimus.
- Vienas iškvietimas atliekamas norint įvesti apskaičiuotą kiekvieno duomenų modelio tiekėjo operacijų skaičių.

![Pranešimas apie pasikartojančias RCS puslapio Modelio susiejimo dizaino įrankis duomenų bazės užklausas.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

Reikšmė **\[q:530\]** nurodo, kad lentelė VendTrans buvo iškviesta 530 kartų, kad į duomenų šaltinį VendTable/\<Relations/VendTrans.VendTable\_AccountNum būtų pateiktas tos lentelės įrašas. Reikšmė **\[530\]** nurodo, kad duomenų šaltinis VendTable/\<Relations/VendTrans.VendTable\_AccountNum buvo iškviestas 530 kartus, kad būtų pateiktas to duomenų šaltinio įrašas ir duomenų modelyje būtų įvesta jo informacija.

Rekomenduojame naudoti duomenų šaltiniui VendTable/\<Relations/VendTrans.VendTable\_AccountNum skirtą talpyklą, kad sumažėtų siekiant gauti informacijos apie 265 operacijas atliktų iškvietimų skaičius ir pagerėtų modelio susiejimo našumas.

Taip pat gali būti naudinga sumažinti į duomenų šaltinį LedgerTransTypeList atliktų iškvietimų skaičių. Šis duomenų šaltinis naudojamas norint susieti kiekvieną išvardijimo **LedgerTransType** reikšmę su jos žyme. Naudodami šį duomenų šaltinį, galite rasti atitinkamą žymę ir įvesti ją kiekvieno tiekėjo operacijos duomenų modelyje. Dabartinis iškvietimų į šį duomenų šaltinį skaičius (9027) gana didelis, turint omenyje, kad apdorojamos 265 operacijos.

![RCS puslapis Modelio susiejimo dizaino įrankis, kuriame rodomi 9027 iškvietimai į duomenų šaltinį.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Patobulinkite modelio susiejimą pagal iš vykdymo sekimo gautą informacija

### <a name="modify-the-logic-of-the-model-mapping"></a>Modelio susiejimo logikos keitimas

1. Atlikite toliau nurodytus veiksmus, kad būtų kaupiama talpykloje ir išvengiama pasikartojančių iškvietimų į duomenų bazę.

    1. RCS puslapio **Modelio susiejimo dizaino įrankis** srityje **Duomenų šaltiniai** pasirinkite elementą **VendTable**.
    2. Pasirinkite **Talpykla**.
    3. Išplėskite elementą **VendTable**, išplėskite duomenų šaltinio VendTable ryšių „vienas su daugeliu“ sąrašą (elementas **\<Ryšiai**) ir pasirinkite elementą **VendTrans.VendTable\_AccountNum**.
    4. Pasirinkite **Talpykla**.

    ![Kaupimo talpykloje nustatymas, kad būtų išvengta pasikartojančių iškvietimų.](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. Atlikite toliau nurodytus veiksmus, norėdami, kad duomenų šaltinis LedgerTransTypeList patektų į duomenų šaltinio VendTable sritį.

    1. Srityje **Duomenų šaltinio tipai** išplėskite elementą **Funkcijos** ir pasirinkite elementą **Apskaičiuotasis laukas**.
    2. Srityje **Duomenų šaltiniai** pasirinkite elementą **VendTable**.
    3. Pasirinkite **Įtraukti**.
    4. Lauke **Pavadinimas** įveskite **\$TransType**.
    5. Pasirinkite **Redaguoti formulę**.
    6. Lauke **Formulė** įveskite **LedgerTransTypeList**.
    7. Pasirinkite **Įrašyti**.
    8. Uždarykite puslapį **Formulės rengyklė**.
    9. Spustelėkite **Gerai**.

3. Atlikę toliau nurodytus veiksmus atlikite lauko **\$TransType** talpyklinius mainus.

    1. Pasirinkite elementą **LedgerTransTypeList**.
    2. Pasirinkite **Talpykla**.
    3. Pasirinkite elementą **VendTable.\$TransType**.
    4. Pasirinkite **Talpykla**.

    ![Lauko $TransType kaupimo talpykloje sąranka.](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. Atlikę toliau nurodytus veiksmus pakeiskite lauką **\$TransTypeRecord**, kad jis galėtų naudoti talpykloje esantį lauką **\$TransType**.

    1. Srityje **Duomenų šaltiniai** išplėskite elementą **VendTable**, išplėskite elementą **\<Ryšiai**, išplėskite elementą **VendTrans.VendTable\_AccountNum** ir pasirinkite elementą **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.
    2. Pasirinkite **Redaguoti**.
    3. Pasirinkite **Redaguoti formulę**.
    4. Lauke **Formulė** suraskite toliau nurodytą išraišką.

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. Lauke **Formulė** įveskite toliau nurodytą išraišką.

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. Pasirinkite **Įrašyti**.
    7. Uždarykite puslapį **Formulės rengyklė**.
    8. Pasirinkite **Gerai**.

5. Pasirinkite **Įrašyti**.
6. Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.
7. Uždarykite puslapį **Modelio susiejimai**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Modifikuotos ER modelio susiejimo versijos užbaigimas

1. RCS puslapio **Konfigūracijos** „FastTab“ **Versijos** pasirinkite konfigūracijos **Našumo sekimo susiejimas** versiją **1.2**.
2. Pasirinkti **Keisti būseną**.
3. Pasirinkite **Baigti**.

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a>Modifikuotos ER modelio susiejimo konfigūracijos importavimas iš RCS į programą

Pakartokite veiksmus, aprašytus ankstesniame šios temos skyriuje [ER konfigūracijos importavimas iš RCS į „Finance and Operations“](#import-configuration) ir importuokite konfigūracijos **Našumo sekimo susiejimas** 1.2 versiją.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Modifikuoto ER vykdymo sekimo sprendimo vykdymas

### <a name="run-the-er-format"></a>ER formato vykdymas

Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.

## <a name="work-with-the-execution-trace"></a>Darbas su vykdymo sekimu

### <a name="export-the-generated-trace-from-the-application"></a>Sugeneruotos sekimo eksportavimas iš programos

Pakartoję ankstesniame šios temos skyriuje [Sugeneruoto sekimo eksportavimas iš programos](#export-trace) nurodytus veiksmus, vietiniame tinkle įrašykite naują našumo sekimą.

### <a name="import-the-generated-trace-into-rcs"></a>Sugeneruoto sekimo importavimas į RCS

Pakartoję ankstesniame šios temos skyriuje [Sugeneruoto sekimo importavimas į RCS](#import-trace) nurodytus veiksmus importuokite naują našumo sekimą į RCS.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas

Pakartoję ankstesniame šios temos skyriuje [Našumo sekimo naudojimas analizei naudojantis RCS – Modelio susiejimas](#use-trace) nurodytus veiksmus išanalizuokite naujausią našumo sekimą.

Atkreipkite dėmesį, kad atlikus modelio susiejimo pakeitimus, nebeliko pasikartojančių užklausų į duomenų bazę. Taip pat sumažėjo šio modelio susiejimo iškvietimų į duomenų bazės lenteles ir duomenų šaltinius skaičius. Todėl pagerėjo viso ER sprendimo našumas.

![RCS puslapio modelio susiejimo dizaino įrankio duomenų šaltinio VendTable informacijos sekimas.](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

Sekimo informacijoje duomenų šaltinio VendTable reikšmė **\[12\]** nurodo, kad šis duomenų šaltinis buvo iškviestas 12 kartų. Reikšmė **\[Q:6\]** nurodo, kad šeši iškvietimai paversti duomenų bazės iškvietimais lentelėje VendTable. Reikšmė **\[C:6\]** nurodo, kad iš duomenų bazės surinkti įrašai buvo įrašyti į talpyklą, o šeši kiti iškvietimai apdoroti naudojant talpyklą.

Atkreipkite dėmesį, kad iškvietimų į duomenų šaltinį LedgerTransTypeList skaičius sumažėjo nuo 9027 iki 240.

![RCS puslapio modelio susiejimo dizaino įrankio duomenų šaltinio LedgerTransTypeList informacijos sekimas.](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a>Vykdymo sekimo peržiūra programoje

Galimybė naudotis ER sistemos dizaino įrankiu gali būti siūloma ne tik RCS, bet ir kai kuriose versijose. Šiose versijose galima įjungti parinktį **Kūrimo režimo įjungimas**. Šią pasirinktį galite rasti puslapio **Elektroninių ataskaitų parametrai**, kurį galite atidaryti darbo srityje **Elektroninės ataskaitos**, skirtuke **Bendra**.

![Kūrimo režimo parinkties įjungimas Elektroninių ataskaitų parametrų puslapyje.](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Jei naudojatės viena iš šių versijų, sugeneruotų našumo sekimų informaciją galite analizuoti tiesiogiai programoje. Nereikia eksportuoti informacijos iš programos ir importuoti ją į RCS.

## <a name="review-the-execution-trace-by-using-external-tools"></a>Vykdymo sekimo peržiūra naudojantis išoriniais įrankiais

### <a name="configure-user-parameters"></a>Vartotojo parametrų konfigūravimas

1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Dialogo lango **Vartotojo parametrai** skyriaus **Vykdymo sekimas** lauke **Vykdymo sekimo formatas** pasirinkite **PerfView XML**.

### <a name="run-the-er-format"></a>ER formato vykdymas

Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.

Atkreipkite dėmesį, kad interneto naršyklėje siūloma atsisiųsti ZIP failą. Šiame faile pateikiamas našumo sekimas PerfView formatu. Naudodamiesi PerfView našumo analizės įrankiu galite išanalizuoti informaciją apie ER formato vykdymą.

![Našumo sekimo informacija „PerfView” formatu.](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a>Norėdami peržiūrėti vykdymo sekimą, apimantį duomenų bazės užklausas, naudokite išorinius įrankius

Dėl patobulinimų, atliktų ER sistemoje, efektyvumo sekimo duomenys, sugeneruoti „PerfView“ formatu, dabar teikia daugiau išsamios informacijos apie ER formato vykdymą. Naudojant „Microsoft Dynamics 365 for Finance and Operations“ 10.0.4 versiją (2019 m. liepos mėn.), šiuose sekimo duomenyse taip pat gali būti pateikiama informacija apie vykdytas SQL užklausas į programos duomenų bazę.

### <a name="configure-user-parameters"></a>Vartotojo parametrų konfigūravimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Dialogo lango **Vartotojo parametrai** skyriuje **Vykdymo sekimas** nustatykite toliau nurodytus parametrus.

    - Lauke **Vykdymo sekimo formatas** pasirinkite **„PerfView“ XML**.
    - Nustatykite parinkties **Rinkti užklausų statistiką** reikšmę **Taip**.
    - Nustatykite parinkties **Įjungti profilį** reikšmę **Taip**.

    ![Skyrius Vykdymo sekimas, dialogo langas Vartotojo parametrai.](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a>ER formato vykdymas

Pakartoję ankstesniame šios temos skyriuje [ER formato vykdymas](#run-format) nurodytus veiksmus sugeneruokite naują našumo sekimą.

Atkreipkite dėmesį, kad interneto naršyklėje siūloma atsisiųsti ZIP failą. Šiame faile pateikiamas našumo sekimas PerfView formatu. Naudodamiesi PerfView našumo analizės įrankiu galite išanalizuoti informaciją apie ER formato vykdymą. Dabar šis sekimas apims informaciją apie SQL duomenų bazės prieigą vykdant ER formatą.

![Įvykdyto ER formato informacijos sekimas naudojant „PerfView“.](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [ER sprendimų našumo didinimas įtraukiant parametrizuotų duomenų šaltinių APSKAIČIUOTAS LAUKAS](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

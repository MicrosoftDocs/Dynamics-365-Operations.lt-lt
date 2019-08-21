---
title: Programos metaduomenų, kurie bus naudojami RCS ir ER, paruošimas
description: Šioje temoje paaiškinama, kaip paruošti programos metaduomenis, skirtus „Regulatory Configuration Service“ (RCS) ir elektroninėms ataskaitoms (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a540676ba11bc3c0fb7855a2fdaff998819dfbe
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849690"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a>Programos metaduomenų, skirtų RCS, paruošimas

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiama toliau nurodytų užduočių pavyzdžių:

- [Programos metaduomenų, kuriuos galima naudoti RCS, paruošimas](#prepare-application-metadata-that-can-be-used-in-rcs)
- [Prieiga prie programos metaduomenų naudojant ER konfigūraciją](#access-application-metadata-by-using-an-er-configuration)
- [Prieiga prie programos metaduomenų naudojant prijungtas programas](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>Programos metaduomenų, kuriuos galima naudoti RCS, paruošimas

Toliau pateikta procedūra parodo, kaip „Finance and Operations“ vartotojas, turintis vaidmens **Sistemos administratorius** arba **Elektroninės ataskaitos kūrėjas** teises, gali sukurti elektroninės ataskaitos (ER) konfigūraciją, kurioje būtų metaduomenys, skirti „Microsoft Dynamics 365 for Finance and Operations“ programai, ir kurią naudojant būtų kuriamos ER modelių susiejimo konfigūracijos naudojant „Regulatory Configuration Service“ (RCS). Šiame pavyzdyje sukurta ER modelio susiejimo konfigūracija bus naudojama norint pasiekti užsienio prekybos operacijas.

Šiame pavyzdyje jūs norite naudodami RCS sukurti ER sprendimą, skirtą „Finance and Operations“, kurį naudojant bus generuojami elektroniniai dokumentai, kuriuose pateikiama informacija iš užsienio prekybos verslo srities. Norint susieti ER duomenų modelį su reikiamų duomenų šaltiniais, reikia turėti prieigą prie RCS „Finance and Operations“ programos metaduomenų. Todėl, norėdami sukurti ER sprendimą, turite sukonfigūruoti naują ER metaduomenų konfigūraciją, kurioje būtų visi metaduomenys, kurių šiuo metu reikia norint generuoti pasirinktos verslo srities ER ataskaitas.

> [!NOTE]
> Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

1. Eikite į **Organizacijos administravimas \> Darbo sritys \> Elektroninės ataskaitos**.
2. Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**. Jei nematote šio konfigūracijos teikėjo, atlikite procedūrą [Sukurti konfigūracijų teikėją ir jį pažymėti kaip aktyvų](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Pasirinkite **Metaduomenų konfigūracijos**.
4. Pasirinkite **Kurti konfigūraciją**.
5. Išplečiamojo dialogo lango lauke **Pavadinimas** įveskite pavadinimą. Šiame pavyzdyje įveskite **Užsienio prekybos metaduomenys**.
6. Pasirinkite **Kurti konfigūraciją**.
7. Pasirinkite **Dizaino įrankis**.
8. Pasirinkite **Įtraukti**.

    > [!NOTE]
    > Galite pasirinkti visus metaduomenis, skirtus visai programai arba skirtus pasirinktiems modeliams ar moduliams. Atminkite, kad abiem atvejais šie metaduomenys bus įtraukti automatiškai: įrašų lentelės, išvardijimai ir išplėstiniai duomenų tipai (EDT). Jei reikia papildomų metaduomenų tipų, juos reikia įtraukti rankiniu būdu.

Turite įtraukti metaduomenų, susijusių su užsienio prekybos operacijomis, ir rankiniu būdu pasirinkti metaduomenų elementus.

9. Pasirinkite **Įtraukti duomenų šaltinį \> Lentelės įrašai**.
10. Filtruokite pagal **Intrastat** reikšmę lauke **Pavadinimas**.
11. Pasirinkite **Intrastat** lentelės įrašą.
12. Pasirinkite **Gerai**.

Turite įtraukti metaduomenų informaciją apie „Intrastat“ įrašų lentelę.

13. Medyje pasirinkite **Lentelės įrašai „Intrastat“ \> \>Ryšiai \> IntrastatCommodity (lentelės įrašai EcoResCategory)**.
14. Pasirinkite **Įtraukti metaduomenis**.

    > [!NOTE]
    > Metaduomenis apie reikalingus ryšius, skirtus pasirinktai įrašų lentelei, reikia įtraukti rankiniu būdu.

15. Pasirinkite **Įtraukti duomenų šaltinį**.
16. Pasirinkite **Išvardijimas**.
17. Filtruokite pagal **IntrastatDirection** reikšmę lauke **Pavadinimas**.
18. Pasirinkite **IntrastatDirection** išvardijimo įrašą.
19. Pasirinkite **Gerai**.
20. Pasirinkite **Įrašyti**.
21. Uždarykite puslapį.
22. Užpildykite metaduomenų konfigūracijos juodraštinę versiją:

    1. Pasirinkite **Keisti būseną \> Baigta**.
    2. Pasirinkite **Gerai**.
    3. Pasirinkite baigtą versiją 1.

23. Eksportuokite baigtą metaduomenų konfigūracijos versiją iš programos kaip XML failą:

    1. Pasirinkite **Keitimas \> Eksportuoti kaip XML failą**.
    2. Pasirinkite **Gerai**.

Jūsų sukurta ER metaduomenų konfigūracija įrašoma kaip failas **Užsienio prekybos metaduomenys.xml**. Dabar galite jį importuoti į RCS ir naudoti jį „Finance and Operations“ kaip užsienio prekybos verslo srities metaduomenų šaltinį. Remdamiesi šia informacija, galite nurodyti susiejimą tarp programos metaduomenų ir ER duomenų modelio.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>Prieiga prie programos metaduomenų naudojant ER konfigūraciją

Toliau pateiktoje procedūroje parodoma, kaip RCS vartotojas, turintis vaidmens **Sistemos administratorius** arba **Elektroninės ataskaitos kūrėjas** teises, gali sukurti naują ER modelio susiejimą naudodamas „Finance and Operations“ programos metaduomenis. Programos metaduomenys bus pasiekiami naudojant ER metaduomenų konfigūraciją, kurioje yra metaduomenų pavyzdžių rinkinys, skirtas užsienio prekybos operacijoms pasiekti.

Kad galėtumėte atlikti šią procedūrą, pirmiausia atlikite toliau nurodytas procedūras.

- [Sukurti konfigūracijų teikėją ir jį pažymėti kaip aktyvų](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [Programos metaduomenų, kuriuos galima naudoti RCS, paruošimas](#prepare-application-metadata-that-can-be-used-in-rcs)

1. Eikite į **Visos darbo sritys \> Elektroninės ataskaitos**.
2. Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**. Jei nematote šio konfigūracijos teikėjo, atlikite procedūrą [Sukurti konfigūracijų teikėją ir jį pažymėti kaip aktyvų](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Importuokite ER metaduomenų konfigūraciją, kurioje yra „Finance and Operations“ programos metaduomenys ir kuri sukonfigūruota generuoti elektroninius dokumentus, skirtus užsienio prekybos verslo sričiai. Jūs sukūrėte šią ER metaduomenų konfigūraciją ir eksportavote ją kaip XML failą atlikdami šioje temoje anksčiau pateiktą procedūrą [Programos metaduomenų, kuriuos galima naudoti RCS, paruošimas](#prepare-application-metadata-that-can-be-used-in-rcs).

    1. Pasirinkite **Metaduomenų konfigūracijos**.
    2. Pasirinkite **Keitimas**.
    3. Pasirinkite **Įkelti iš XML failo**.
    4. Raskite ir pasirinkite failą **Užsienio prekybos metaduomenys.xml**.
    5. Pasirinkite **Gerai**.
    6. Uždarykite puslapį.

4. Sukurkite duomenų modelio konfigūraciją:

    1. Pasirinkite **Ataskaitų konfigūracijos**.
    2. Pasirinkite **Kurti konfigūraciją**.
    3. Išplečiamojo dialogo lango lauke **Pavadinimas** įveskite **Užsienio prekybos modelis**.
    4. Pasirinkite **Kurti konfigūraciją**.
    5. Pasirinkite **Dizaino įrankis**.
    6. Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.

        1. Lauke **Pavadinimas** įveskite **Šaknis**.
        2. Pasirinkite **Įtraukti**.
    
    7. Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.

        1. Lauke **Pavadinimas** įveskite **Operacija**.
        2. Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.
        3. Pasirinkite **Įtraukti**.
 
    8. Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.

        1. Lauke **Pavadinimas** įveskite **Prekės kodas**.
        2. Lauke **Elemento tipas** pasirinkite **Eilutė**.
        3. Pasirinkite **Įtraukti**.

    9. Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.

        1. Lauke Pavadinimas įveskite **Sąskaitos faktūros suma**.
        2. Lauke **Elemento tipas** pasirinkite **Realusis skaičius**.
        3. Pasirinkite **Įtraukti**.

    10. Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.

        1. Lauke **Pavadinimas** įveskite **Data**.
        2. Lauke **Elemento tipas** pasirinkite **Data**.
        3. Pasirinkite **Įtraukti**.
 
    11. Pasirinkite **Įtraukti \> Šakninė nuoroda**.
    12. Pasirinkite **Gerai**.
    13. Pasirinkite **Įrašyti**.
    14. Uždarykite puslapį.
    15. Pasirinkite **Keisti būseną \> Baigta**.
    16. Pasirinkite **Gerai**.

5. Sukurkite modelio susiejimo konfigūraciją:

    1. Pasirinkite **Kurti konfigūraciją**.
    2. Išplečiamojo dialogo lango lauke **Naujas** įveskite **Modelio susiejimas remiantis duomenų modeliu Užsienio prekybos modelis**.
    3. Lauke **Pavadinimas** įveskite **Užsienio prekybos susiejimas**.
    4. Pasirinkite **Kurti konfigūraciją**.
    5. „FastTab“ **Būtinieji komponentai** pasirinkite **Redaguoti**.
    6. Pasirinkite **Naujas**.
    7. Lauke **Būtinojo komponento tipas** pasirinkite **Konfigūracija**.
    8. Pasirinkite konfigūraciją **Užsienio prekybos metaduomenys**.
    9. Pasirinkite **Įrašyti**. Atkreipkite dėmesį, kad nuoroda įtraukiama į konfigūracijos **Užsienio prekybos metaduomenys** 1 versiją. Kuriant modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys.
    10. Uždarykite puslapį.
    11. Pasirinkite **Dizaino įrankis**.
    12. Pasirinkite **Dizaino įrankis**.
    13. Medyje pasirinkite **„Dynamics 365 for Operations“ \> Lentelės įrašai**.
    14. Pasirinkite **Įtraukti šaknį**.
    15. Lauke **Pavadinimas** įveskite **Intrastat**.
    16. Pasirinkite **Intrastat** lentelės įrašus.
    17. Pasirinkite **Gerai**.

        > [!NOTE]
        > Siūlomos tik dvi lentelės, nes tik dvi lentelės įtrauktos į šiuo metu naudojamą metaduomenų rinkinį.

    18. Pasirinkite **Susieti**.
    19. Medyje pasirinkite **Intrastat \> AmountMST**.
    20. Medyje pasirinkite **Operacija = „Intrastat“ \> Sąskaitos faktūros suma**.
    21. Pasirinkite **Susieti**.
    22. Medyje pasirinkite **Intrastat \> TransDate**.
    23. Medyje pasirinkite **Operacija = „Intrastat“ \> Data**.
    24. Pasirinkite **Susieti**.
    25. Medyje pasirinkite **„Intrastat“ \> \>Ryšiai \> IntrastatCommodity \> Kodas**.
    26. Medyje pasirinkite **Operacija = „Intrastat“ \> Prekės kodas**.
    27. Pasirinkite **Susieti**.
    28. Pasirinkite **Tikrinti**.

        > [!NOTE]
        > Kai tikrinimas baigtas, sėkmingai susiejote duomenų modelio elementus su duomenų šaltinių elementais, kurie aprašomi naudojant programos metaduomenų informaciją iš nurodytos ER metaduomenų konfigūracijos.

    29. Pasirinkite **Įrašyti**.

Jei reikia, galite išplėsti esamą „Finance and Operations“ metaduomenų rinkinį. Tada galite eksportuoti naują baigtą ER metaduomenų konfigūracijos versiją iš „Finance and Operations“, importuoti į RCS ir atnaujinti sukonfigūruotos modelio susiejimo konfigūracijos būtinuosius komponentus, kad būtų nurodoma nauja importuotos metaduomenų konfigūracijos versija.

> [!NOTE]
> Tai yra vienintelis būdas gauti informaciją apie programos metaduomenis naudojant vietinėje sistemoje įdiegtas programas (t. y. kai „Finance and Operations“ naudojamas vietos verslo duomenų \[LBD\] arba vietinio diegimo modelis).

## <a name="access-application-metadata-by-using-connected-applications"></a>Prieiga prie programos metaduomenų naudojant prijungtas programas

Toliau pateiktoje procedūroje parodoma, kaip RCS vartotojas, turintis vaidmens **Sistemos administratorius** arba **Elektroninės ataskaitos kūrėjas** teises, gali sukurti naują ER modelio susiejimą naudodamas „Finance and Operations“ programos metaduomenis. Programos metaduomenys bus pasiekiami tinkle naudojant programą, prijungtą prie RCS. Bus sukonfigūruotas ER modelio susiejimo pavyzdys, siekiant pasiekti užsienio prekybos operacijas.

Norėdami atlikti šią procedūrą, pirmiau turite atlikti RCS procedūrą [Sukurti konfigūracijų teikėją ir jį pažymėti kaip aktyvų](tasks/er-configuration-provider-mark-it-active-2016-11.md). Jei dar neatlikote anksčiau šioje temoje pateiktos procedūros [Prieiga prie programos metaduomenų naudojant ER konfigūraciją](#access-application-metadata-by-using-an-er-configuration), eikite į puslapį [Elektroninių ataskaitų užduočių vedliai, skirti „Dynamics 365 for Finance and Operations 8.1“](https://go.microsoft.com/fwlink/?linkid=2082739) ir iš anksto atsisiųskite toliau nurodytus ER konfigūracijos failus ir įrašykite juos vietinėje sistemoje: **Užsienio prekybos metaduomenys.xml**, **Užsienio prekybos modelis.xml** ir **Užsienio prekybos susiejimas.xml**.


### <a name="get-required-er-configurations"></a>Reikiamų ER konfigūracijų gavimas

Jei jau atlikote anksčiau šioje temoje nurodytos procedūros [Prieiga prie programos metaduomenų naudojant ER konfigūraciją](#access-application-metadata-by-using-an-er-configuration) veiksmus, jūs jau turite visas reikiamas ER konfigūracijas (užsienio prekybos metaduomenų, modelio ir susiejimo konfigūracijas) dabartiniame RCS egzemplioriuje. Tokiu atveju galite praleisti šią procedūrą.

1. Eikite į **Visos darbo sritys \> Elektroninės ataskaitos**.
2. Pasirinkite **Ataskaitų konfigūracijos**.
3. Įkelkite konfigūracijos failus **Užsienio prekybos metaduomenys.xml**, **Užsienio prekybos modelis.xml** ir **Užsienio prekybos susiejimas.xml**, su kiekvienu failu atlikdami toliau nurodytus veiksmus:

    1. Pasirinkite **Keitimas**.
    2. Pasirinkite **Įkelti iš XML failo**.
    3. Pasirinkite **Naršyti** ir pasirinkite failą.
    4. Pasirinkite **Gerai**.

### <a name="register-the-connection-with-finance-and-operations"></a>Ryšio su „Finance and Operations‟ užregistravimas

1. Eikite į **Visos darbo sritys \> Elektroninės ataskaitos**.
2. Pasirinkite **Prijungtos programos**.
3. Įsitikinkite, kad sukonfigūruota programa veikia „Microsoft Azure“ pagrindu ir kad ji apskritai pasiekiama RCS vartotojams. Esamas RCS vartotojas turi turėti prieigą prie registruojamos sukonfigūruotos programos kaip programos vartotojas, kuriam priskirtas vaidmuo suteikia teises pasiekti programos metaduomenis.
4. Pasirinkite **Naujas**.
5. Lauke **Pavadinimas** įveskite **MyConnectedApp** kaip prijungtos programos pavadinimą.
6. Lauke **Programa** nurodykite programos URL.
7. Lauke **Nuomotojas** nurodykite programos teikėją.
8. Pasirinkite **Įrašyti**. 
9. Kai tikrinate ryšį su sukonfigūruota programa, puslapyje **Prisijungti prie nuotolinės programos** pasirinkite saitą **Pasirinkite čia, kad prisijungtumėte prie pasirinktos nuotolinės programos**. 
10. Pasirinkite **Tikrinti ryšį**, kad patikrintumėte prieigą prie sukonfigūruotos programos.
11. Pasirinkite **Uždaryti**.

Atlikus šią procedūrą ir sėkmingai atlikus ryšio patikrą, sukonfigūruotos programos versijos ir nuomotojo informacija bus atnaujinta dabartiniame tinklelyje.

### <a name="review-the-existing-model-mapping-configuration"></a>Esamo modelio susiejimo konfigūracijos peržiūra

1. Eikite į **Visos darbo sritys \> Elektroninės ataskaitos**.
2. Pasirinkite **Ataskaitų konfigūracijos**.
3. Medyje pasirinkite **Užsienio prekybos modelis \> Užsienio prekybos susiejimas**.
4. Pasirinkite „FastTab“ **Būtinieji komponentai**.

    > [!NOTE]
    > Šiuo metu šis susiejimas nurodo metaduomenų konfigūraciją. Kuriant šį modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys.

4. Pasirinkite **Dizaino įrankis**.
5. Pasirinkite **Dizaino įrankis**.
6. Medyje pasirinkite **„Dynamics 365 for Operations“ \> Lentelės įrašai**.
7. Pasirinkite **Įtraukti šaknį**.
8. Lauke **Lentelė** įveskite arba pasirinkite reikšmę.

    > [!NOTE]
    > Šiuo metu šis susiejimas nurodo metaduomenų konfigūraciją. Kuriant šį modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys.

9. Pasirinkite **Atšaukti**.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>Prijungtos programos priskyrimas modelio susiejimui

1. Pasirinkite **Redaguoti**.
2. **Prijungtos programos lauke** pasirinkite programą **MyConnectedApp**.

    > [!NOTE]
    > Šis susiejimas nurodo pasirinktos prijungtos programos metaduomenis. Jei tas pats susiejimas tuo pačiu metu nurodo metaduomenų konfigūraciją ir prijungtą programą, bus naudojami prijungtos programos metaduomenys.

3. Pasirinkite **Dizaino įrankis**.
4. Pasirinkite **Dizaino įrankis**.
5. Medyje pasirinkite **„Dynamics 365 for Operations“ \> Lentelės įrašai**.
6. Pasirinkite **Įtraukti šaknį**.
7. Lauke **Lentelė** įveskite arba pasirinkite reikšmę.

    > [!NOTE]
    > Šiuo metu siūlomos daugiau nei dvi programos lentelės, nes šis susiejimas naudoja visus prijungtos programos, kuri buvo priskirta, metaduomenis.

8. Pasirinkite **Atšaukti**.
9. Pasirinkite **Tikrinti**.

Jūs susiejote duomenų modelio elementus su duomenų šaltinių elementais, kurie aprašomi naudojant prijungtos programos, priskirtos šiam susiejimui, metaduomenis.

Jei reikia įvertinti šio modelio susiejimą naudojant skirtingos programos versijos metaduomenis, užregistruokite kitą prijungtą programą, priskirkite ją šiam modelio susiejimui ir patikrinkite ją naudodami naujus metaduomenis.

## <a name="additional-resources"></a>Papildomi ištekliai

Arba galite „Finance and Operations“ paleisti užduočių vedlį **Programos metaduomenų, kuriuos galima naudoti RCS, paruošimas** ir taip pat RCS galite paleisti užduočių vedlius **Prieiga prie programos metaduomenų naudojant ER konfigūraciją** ir **Prieiga prie programos metaduomenų naudojant prijungtas programas**. Šiuos užduočių vedlius galima atsisiųsti iš puslapio [Elektroninių ataskaitų užduočių vedliai, skirti „Dynamics 365 for Finance and Operations 8.1“](https://go.microsoft.com/fwlink/?linkid=2082739).

---
title: TDS mokėjimų TDS valdžios tiekėjams nustatymas ir TDS išdavimo generavimas
description: Šioje temoje paaiškinama, kaip sudengti iš šaltinio (TDS) mokėjimus TDS valdžios institucijų tiekėjams.
author: kailiang
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023455"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a>TDS mokėjimų TDS valdžios tiekėjams nustatymas ir TDS išdavimo generavimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip sudengti iš šaltinio (TDS) mokėjimus TDS valdžios institucijų tiekėjams.

1. Eikite į **Mokėtinos sumos \> Mokėjimai \> Tiekėjo mokėjimų žurnalas**.

    [![Tiekėjo mokėjimų žurnalo puslapis](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)

2. Puslapyje **Tiekėjo mokėjimų žurnalas** pasirinkite **Naujas,** kad sukurtumėte žurnalo eilutę.
3. Lauke **Sąskaita** rinkitės TDS valdžios tiekėją, sudengsią su TDS mokėjimais.
4. Rinkitės **Sudengimo operacijas** norėdami atidaryti **Sudengimo operacijų** puslapį, kur galėsite peržiūrėti TDS institucijos tiekėjo sudengtas TDS operacijas.

    Sudengimo laikotarpio sudengtos TDS operacijos parodomos tokiu būdu:

    - TDS operacijos, kai vertinimo kategorijos pobūdis yra **Įmonė**, rodoma kaip viena operacijos eilutė.
    - TDS operacijos, kai vertinimo kategorijos pobūdis yra **HUF**, **Firma**, **Asmenys**, **AOP**, **BOI**, **vietos valdžios institucijos** ar **Kiti**, rodomos kaip viena operacijos eilutė.
    - Lauke **Suma** rodoma bendroji TDS suma, kurią reikia sumokėti TDS institucijos tiekėjui.

5. Norėdami peržiūrėti **išsamią informaciją** apie kitas TDS operacijas, kurios įtrauktos į sudengimo įrašą. Šiame puslapyje galite peržiūrėti kiekvienos TDS operacijos, įtrauktos į sudengimo laikotarpio sudengimo procesą, skaidimą.
6. Skirtuke **Peržiūra** pažymėkite **Žymės** TDS operacijų langelį, norėdami sudengti TDS institucijos tiekėjui.

    Skirtuke **Peržiūros** rodoma ši kiekvienos atvertos TDS operacijos informacija:

    - **Data** – TDS perlaidos data.
    - **Kvitas** – Kvito numeris.
    - **Šaltinis** – modulis, kuriame publikuota TDS operacija.
    - **Tiekėjas/klientas** – tiekėjo arba kliento kodas, iš kurio atimtas TDS.
    - **Atskaitymo/šalies pavadinimas** – tiekėjo arba kliento, iš kurio atimtas TDS, pavadinimas.
    - **Vertinimo pobūdis** – vertinimo kategorijos, kuriai priklauso atskaitymas, pobūdis.
    - **Suma** – Sąskaitos suma, kuriai buvo suskaičiuota TDS.
    - **Mokesčio suma** – TDS mokesčio suma, apskaičiuota operacijai.

    > [!NOTE]
    > Išvalykite **Žymę** kurios TDS operacijų, kurios neturi būti sudengtos TDS institucijos tiekėjui, žymės langelį.

    Skirtuko **Bendra** lauke **PAN** rodomas nuolatinės išskaitomos sąskaitos numeris (PAN). Lauke **Data** rodoma TDS skaičiavimo data, o vertės lauke rodomas bendrasis procentas, kuris buvo naudojamas **vertė** skaičiuoti.

7. Pasirinkite **kvitą**, norėdami peržiūrėti TDS operacijos kvitų įrašus.
8. Uždarykite puslapį.
10. Rinkitės **išskaitomo mokesčio komponentų** norėdami atidaryti **Išskaitomo mokesčio komponentų** puslapį, kur galėsite peržiūrėti TDS mokesčio komponento, apskaičiuoto konkretaus TDS mokesčio kodo, TDS.

    Skirtuko **Peržiūra** lauke **Mokesčio komponentas** TDS mokesčio komponentas, kuris buvo naudojamas operacijai. Lauke **Suma** rodoma TDS suma, apskaičiuota TDS mokesčio komponentui bazine valiuta. Lauke **Sukaupta suma** rodoma bendroji TDS suma, apskaičiuota visų sudengtų operacijų TDS mokesčio komponentui.

    Skirtuke **Suma** skyriuje **Numatytoji valiuta** rodoma TDS suma, apskaičiuota TDS mokesčio komponentui numatytąja valiuta. Skyriuje **Antrinė valiuta** rodoma antrinės valiutos suma.

11. Uždarykite **Išskaitomo mokesčio komponentų** puslapį.
12. Puslapyje **Atviros operacijos redagavimas** lauke **Suma** atkreipkite dėmesį, kad atnaujinama sudengimo laikotarpio bendroji suma, kurią reikia sudengti TDS institucijos tiekėjui.
13. Norėdami sudengti skirtingų TDS sudengimo laikotarpių TDS operacijas TDS institucijos tiekėjui, **pažymėkite** operacijų žymės langelį.
14. Uždarykite **atviros operacijos redagavimo** puslapį.

    > [!NOTE]
    > Jei pasirinktos tik kelios operacijos sudengti **Išskaitymo mokesčio operacijų** puslapyje, bendroji pasirinktų operacijų TDS suma atnaujinama puslapio **Redagavimas** lauke **Atvirų operacijų redagavimas** puslapyje. Koregavimo suma atnaujinama žurnalo eilutėje, kuri yra **žurnalo kvito** puslapyje, ir **atidarytos operacijos redagavimo** puslapis yra uždarytas.

    **Žurnalo kvito** puslapyje, **debeto** lauke rodoma bendroji suma, kurią reikia sumokėti TDS valdžios institucijos tiekėjui.

15. Įvesti korespondentinės sąskaitos informaciją.

    > [!NOTE]
    > Jei TDS operacijos turi skirtingus mokesčių sąskaitų numerius (TAN), žurnalo eilutės kiekvienam TAN sukuriamos **žurnalo kvito** puslapyje.

16. Skirtuke **Mokėjimo mokestis** lauke **Mokesčio ID** rinkitės ID mokestį, kurio mokesčio tipas **Palūkanos** ar **Kitas** norėdami apmokestinti mokėjimo mokestį už atidėtus mokėjimus, kurie atlikti TDS valdžios tiekėjui.

    Skirtuko **Mokesčių informacijos**, esančio **Įmonės informacija** skyriuje **pavadinimas** yra rodomas įmonės pavadinimas. **Išskaitomo mokesčio** skyriuje, mokesčių **sąskaitos numerio (TAN)** laukas rodo TAN, kuris pridėtas prie operacijos eilutės.

17. Patikrinkite ir užregistruokite žurnalą.
18. Norėdami **įvesti operacijos \> išskaitomo mokesčio** išskaitomo mokesčio informaciją, pasirinkite Išskaitomo mokesčio informaciją.

    **Kvitas** – laukelis, kuriame rodomas operacijos kvito numeris.
    
19. Pažymėkite **TDS, deponuotais pagal knygos įrašą** žymės langelį, jei TDS suma yra pervesti naudojant knygos įrašą.
20. Lauke TDS numeris įveskite **šanalų numerį** naudojamą mokėjimui TDS institucijos tiekėjui atlikti.
21. Lauke **Datos** įveskite šalano datą.
22. Lauke **Banko pavadinimas** pasirinkite banko pavadinimą, į kurį TDS suma, mokėtina TDS institucijos tiekėjui, turėtų būti pervesti į depozitą. Šiame lauke pateikiamos visos banko sąskaitos, nustatytos TDS valdžios tiekėjui mokėtinomis su **mokėtinomis sąskaitomis \> Visi tiekėjai \> Nustatyti \> banko sąskaitos**.
23. Lauke **BSR kodas** įveskite banko pagrindinį statistinės grąžinimo (BSR) kodą.
24. Uždarykite puslapį.

### <a name="example"></a>Pavyzdys

Laikotarpis 2009 04 01 sudengtas **nuomos** TDS komponentų grupei naudojant periodinį TDS sudengimo procesą. Bendroji TDS suma, 141 625,00 TDS sudengimo laikotarpio TDS tiekėjo institucijos sąskaitoje. Šią **sumą** galite peržiūrėti TDS institucijos tiekėjo **atvirų operacijų redagavimo** puslapio lauke Suma.

Jei pasirenkate **Išskaitomo mokesčio operacijas** norėdami peržiūrėti skirtingas to laikotarpio TDS operacijas, rodoma ši informacija.

| TDS suma |
|------------|
| 16,995.00  |
| 22,660.00  |
| 28,325.00  |
| 16,995.00  |
| 28,325.00  |
| 16,995.00  |
| 11,330.00  |

Norėdami peržiūrėti konkrečią pasirinktą TDS sumą, apskaičiuotą pagal konkretaus TDS mokesčio kodo TDS mokesčio komponentą, pasirinkite **išskaitomo mokesčio komponentus**. Kaip pavyzdį, TDS sumos pasirenkate **išskaitomo mokesčio komponentus** , 16995,00. Rodoma mokesčio suma, apskaičiuota kiekvienam operacijos komponentui.

| Mokesčių komponentas | Suma    | Sukaupta suma |
|---------------|-----------|--------------------|
| TDS           | 1,5000.00 | 125,000.00         |
| Papildomos išlaidos     | 1,500.00  | 12,500.00          |
| PE įrašai       | 330.00    | 2,750.00           |
| SHE Įrašai      | 165.00    | 1,375.00           |

Jei pasirinkote tik TDS sumas, 16995,00, 22660,00, 28325,00 sudengti **išskaitomo mokesčio operacijų** puslapyje, bendra sudengimo suma rodoma kaip **67 980,00** lauke **Taisymai** puslapyje **Atidaryti operacijos redagavimo** puslapį. Jeigu ši operacija pažymėta sudengti ir uždarytas **atvirų operacijų redagavimo** puslapis, suma **67 980,00** rodoma **Debeto** lauke **žurnalo kvito** puslapyje.

Dabar galite registruoti žurnalą ir generuoti TDS ištas.

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a>TDS valdžios tiekėjų išankstinių mokėjimų koregavimas

Norėdami koreguoti išankstinį mokėjimą, kuris buvo atliktas TDS valdžios institucijos tiekėjui kaip faktinis mokėjimas, eikite į **mokėtinos sumos \> Tiekėjai \> Visi tiekėjai \> Operacijų redagavimas** Jei faktinis atliktas mokėjimas viršija išankstinį mokėjimą, operacijai sugeneruojami du išankstinti numeriai. Tačiau TDS užklausoje rodomas tik pirmasis iškleidimas.

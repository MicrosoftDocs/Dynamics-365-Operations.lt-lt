---
title: „Intrastat” įsigijimų ir išsiuntimų registravimas
description: Šiame straipsnyje pateikiamas pavyzdys, kaip registruoti Intrastat gymus ir išsiuntimus.
author: anasyash
ms.date: 8/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: aef20f0261e103be7fe231a7efb39751ab4d1151
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862970"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>„Intrastat” įsigijimų ir išsiuntimų registravimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiamas pavyzdys, kaip registruoti Intrastat gymus ir išsiuntimus. Šiame pavyzdyje naudojamas juridinis subjektas **ITCO**.

## <a name="setup"></a>Sąranka

1. Importuokite naujausią toliau pateikiamų elektroninių ataskaitų (ER) konfigūracijų versiją.

    - Intrastat modelis
    - Intrastat ataskaita
    - „Intrastat” (IT)

    Daugiau informacijos rasite skyriuje [ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

2. Microsoft Dynamics 365 finansuose ištisinės numeracijos nurodykite: **Genas\_ 397**, **Acco\_ 16403**, **Genas\_ 407** ir **PUR\_ ES**.

    1. Pasirinkite **Organizacijos administravimas** > **Numeracijos** > **Numeracijos**.
    2. Tinklelyje pasirinkite vieną iš numeracijų kodų.
    3. Veiksmų srityje pasirinkite **Redaguoti**.
    4. „FastTab“ **Bendra**, dalyje **Sąranka**, nustatykite parinkties **Tęstinė** reikšmę **Taip**.
    5. Veiksmų srityje pasirinkite **Įrašyti**.

3. Sandėlio adreso nustatymas.

    1. Eikite į **Sandėlio valdymas** &gt; **Sąranka** &gt; **Sandėlis** &gt; **Sandėliai**.
    2. Sąraše pasirinkite sandėlis **11**.
    3. „FastTab“ **Adresas** pasirinkite **Įtraukti**.
    4. Dialogo lango **Naujas** **adresas** lauke **Pavadinimas** **arba** **aprašas** įveskite **Pagrindinis**.
    5. Lauke **Šalis / regionas** pasirinkite **ITA (Italija)**.
    6. Lauke **Miestas** pasirinkite **Aprilija**.
    7. Pasirinkite **Gerai**.

4. Nustatyti operacijų kodus.

    1. Pasirinkite **Mokesčiai** > **Nustatymas** > **Užsienio prekyba** > **Operacijų kodai**.
    2. Pasirinkite **Naujas** ir nustatykite turto pervedimų operacijos kodą.

        - Lauke **Operacijos kodas** įveskite **„1”**.
        - Lauke **Pavadinimas** įveskite **Turto pervedimas**.

    3. Pasirinkite **Naujas** ir nustatykite grąžinimų operacijos kodą.

        - Lauke **Operacijos** **kodas** lauke įveskite **2**.
        - Lauke **Pavadinimas** įveskite **Prekių grąžinimas**.

5.  Nustatyti užsienio prekybos parametrus.

    1. Pasirinkite **Mokesčiai** > **Nustatymai** > **Užsienio prekyba** > **Užsienio prekybos parametrai**.
    2. Skirtuke **Intrastat** „FastTab” **Bendri**, **Perlaidos** **kode** laukelis rinkitės **1**.
    3. Lauke **Kredito pažyma** pasirinkite **2**.
    4. Lauke **Pardavimo ataskaitinis laikotarpis** pasirinkite **Mėnuo**.
    5. Lauke **Pirkimo ataskaitinis laikotarpis** pasirinkite **Mėnuo**.
    6. „FastTab” **Elektroninės ataskaitos** lauke **Failo formato susiejimas** pasirinkite **„Intrastat” (IT)**.
    7. Lauke **Ataskaitų formatų susiejimas** pasirinkite **„Intrastat” ataskaita**.
    8. „FastTab” **Prekių kodų hierarchija** lauke **Kategorijų hierarchija** pasirinkite **„Intrastat”**.
    9. „FastTab” **Statistinė vertė** nustatykite **Spausdinti ir eksportuoti statistinius duomenis** parinktį į **Taip**.
    10. Skirtuke **Šalies / regiono ypatybės** patikrinkite, ar yra toliau pateikiamos eilutės.

        | **Šalies šalis / regionas** | **Intrastat kodas** | **Valiuta** | **Šalies/regiono tipas** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | IT                 | EUR          | Vietinė                |
        | SMR                      | SM                 | EUR          | Specialus vietinis        |

    11. Įrankių juostoje pasirinkite **Nauja**, kad sukurtumėte tolesnę eilutę.

        | **Šalies šalis / regionas** | **Intrastat kodas** | **Valiuta** | **Šalies/regiono tipas** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | DKK          | ES                      |

6. Neapmokestinimo kodų nustatymas.

    1. Eikite į **Mokestis** > **Nustatymas** > **PVM** > **Neapmokestinimo kodai**.
    2. Veiksmų srityje pasirinkite **Nauja**, kad sukurtumėte tolesnes eilutes.

        | **Šalis/regionas** | **Mokesčių lengvatos numeris** | **Įmonės pavadinimas** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | ES TIEKĖJAS        |
        | DNK                | DK0987654321          | Kliento ER      |

7. Tiekėjo adreso nustatymas.

    1. Eikite į **Mokėtinos sumos** &gt; **Tiekėjai** &gt; **Visi tiekėjai**.
    2. Tinklelyje pasirinkite **ES tiekėjas**.
    3. „FastTab“ **Adresai** pasirinkite **Įtraukti**.
    4. Dialogo lango **Naujas adresas** lauke **Pavadinimas arba aprašas** įveskite **Vokietija**.
    5. Lauke **Šalis/regionas** pasirinkite **„DEU”**.
    6. Pasirinkite **Gerai**, kad sukurtumėte naują adresą.
    7. „FastTab” **Sąskaita faktūra ir pristatymas** skyriaus **PVM** lauke **Neapmokestinimo kodas** pasirinkite **Visi**, tada pasirinkite **DE1234567890**.
    8. Veiksmų srityje pasirinkite **Įrašyti**.

8. Kliento adresų nustatymas.

    1. Pasirinkite **Gautinos sumos** > **Klientai** > **Visi klientai**.
    2. Tinklelyje pasirinkite **ITCO-000001**.
    3. „FastTab“ **Adresai** pasirinkite **Redaguoti**.
    4. Dialogo lango **Naujas adresas** lauke **Pavadinimas arba aprašas** įveskite **San Marinas**.
    5. Lauke **Šalis/regionas** pasirinkite **„SMR”**.
    6. Pasirinkite **Gerai**, kad sukurtumėte naują adresą.
    7. „FastTab” **Sąskaita faktūra ir pristatymas** skyriaus **Sąskaita faktūra** lauke **Mokėtojo kodas** pasirinkite **ITCO-000001**.
    8. Lauke **Numeracijos grupė** pasirinkite **IT\_VENDOM**.
    9. Veiksmų juostoje pasirinkite **Įrašyti** ir užverkite puslapį.
    10. Puslapio **Visi klientai** tinklelyje pasirinkite **ITCO-000002**.
    11. „FastTab“ **Adresai** pasirinkite **Įtraukti**.
    12. Dialogo lango **Naujas adresas** lauke **Pavadinimas arba aprašas** įveskite **Danija**.
    13. Lauke **Šalis/regionas** pasirinkite **„DNK”**.
    14. Pasirinkite **Gerai**, kad sukurtumėte naują adresą.
    15. „FastTab” **Pardavimo demografiniai duomenys** lauke **Valiuta** pasirinkite **DKK**.
    16. „FastTab” **Sąskaita faktūra ir pristatymas** skyriaus **PVM** lauke **PVM grupė** pasirinkite **IT\_PUREU**.
    17. Lauke **Neapmokestinimo kodas** pasirinkite **Visi**, tada pasirinkite **DK0987654321**.
    18. Veiksmų srityje pasirinkite **Įrašyti**.

9. Kategorijos hierarchijos nustatymas.

    1. Pasirinkite **Produkto informacijos valdymas** > **Nustatymas** > **Kategorijos ir atributai** > **Kategorijų hierarchijos**.
    2. Tinklelyje pasirinkite **„Intrastat”**.
    3. Veiksmų srityje pasirinkite **Naujas kategorijos mazgas**.
    4. Lauke **Pavadinimas** įveskite **Paslauga**.
    5. Lauke **Kodas** įveskite **123456**.
    6. Veiksmų srityje pasirinkite **Įrašyti**.

10. Nustatykite produktus.

    1. Eikite į **Produkto informacijos valdymas** > **Produktai** > **Patvirtinti produktai**.
    2. Tinklelyje pasirinkite **ITEM**.
    3. „FastTab” **Pirkimas** skyriaus **Administravimas** lauke **Tiekėjas** pasirinkite **ITCO-000001**.
    4. „FastTab” **Užsienio prekyba** skyriaus **„Intrastat”** lauke **Prekė** pasirinkite **\[100 200 30\] Pranešėjas**.
    5. Skyriuje **Kilmė** lauke **Šalis/regionas** rinkitės **DEU**.
    6. Lauke **Valstybė / provincija** pasirinkite **BE**.
    7. „FastTab” **Valdyti atsargas** skyriaus **Grynieji matavimai** lauke **Grynasis svoris** įveskite **5**.
    8. Veiksmų srityje pasirinkite **Įrašyti**.
    9. Puslapio **Išleisti produktai** tinklelyje pasirinkite **Aptarnavimo prekė**.
    10. „FastTab” **Užsienio prekyba** skyriaus **„Intrastat”** lauke **Prekė** pasirinkite **\[123456\] Paslauga**.
    11. Veiksmų srityje pasirinkite **Įrašyti**.

11. Transportavimo būdų nustatymas.

    1. Pasirinkite **Mokesčiai** > **Nustatymas** > **Užsienio prekyba** > **Transportavimo būdas**.
    2. Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte tolesnius transportavimo būdus.

        | **Transportavimas** | **Aprašas** |
        |---------------|-----------------|
        | 1             | Kelias            |
        | 2             | Aviacijos             |

12. Pristatymo būdo nustatymas.

    1. Eikite į **Įsigijimas ir šaltinio pasirinkimas** > **Nustatymai** > **Skirstymas** > **Pristatymo režimai**.
    2. Veiksmų srityje pasirinkite **Naujas**.
    3. Lauke **Pristatymo būdas** įveskite **1**.
    4. Lauke **Aprašas** įveskite **Sunkvežimis**.
    5. „FastTab“ **Užsienio prekyba** lauke **Transportas** pasirinkite **1 (kelias)**.
    6. Veiksmų srityje pasirinkite **Įrašyti**.

13. Pristatymo sąlygų nustatymas.

    1. Eikite į **Mokėtinos sumos** > **Nustatymas** > **Pristatymo sąlygos**.
    2. Sąraše pasirinkite **CFR**.
    3. „FastTab“ **Bendra** lauke **„Intrastat” kodas** įveskite **1**.

## <a name="post-arrivals-for-intrastat"></a>„Intrastat” įsigijimų registravimas

### <a name="purchase-goods-by-using-a-purchase-order"></a>Prekių pirkimas naudojant pirkimo užsakymą

Šioje pavyzdžio dalyje parodyta, kaip naudoti pirkimo užsakymą perkant prekes iš Europos Sąjungos (ES) šalių.

1. Eikite į **Mokėtinos sumos** > **Pirkimo užsakymai** > **Visi pirkimo užsakymai**.
2.  Veiksmų srityje pasirinkite **Naujas**.
3.  Dialogo lango **Sukurti pirkimo užsakymą** lauke **Tiekėjo paskyra** pasirinkite **ES tiekėjas**.
4.  „FastTab” **Administravimas** lauke **Kalba** pasirinkite **it**.
5.  Pasirinkite **Gerai**.
6.  Rodinio **Antraštė** „FastTab” **Užsienio** **prekyba** patikrinkite, ar laukas **Operacijos kodas** nustatytas į **1**.
7.  Patikrinkite, ar laukas **Kilmės / paskirties šalis** nustatytas į **RM**.
8.  „FastTab” **Pristatymas** skyriaus **Pristatymas** lauke **Pristatymo būdas** pasirinkite **1**.
9.  Lauke **Pristatymo sąlygos** pasirinkite **CFR**.
10. Rodinio **Eilutės** „FastTab” **Pirkimo užsakymo eilutės** lauke **Prekės numeris** pasirinkite **Prekė**.
11. Lauke **Vieta** pasirinkite **1**.
12. Lauke **Sandėlis** pasirinkite **11**.
13. Lauke **Kiekis** įveskite **10**.
14. Lauke **Vieneto kaina** įveskite **100**.
15. Skirtuko **Sąranka** dalies **PVM** lauke **Prekės PVM grupė** pasirinkite **22%EU**.
16. Veiksmų srities skirtuke **Pirkimas**, grupėje **Veiksmai**, pasirinkite **Patvirtinti**.
17. Veiksmų srities skirtuke **SF**, esančiame grupėje **Generuoti**, pasirinkite **SF**.
18. Veiksmų juostoje, pasirinkite **Numatyt. iš**.
19. Lauke **Numatytasis eilučių kiekis** pasirinkite **Užsakytas kiekis**, tada pasirinkite **Gerai**.
20. „FastTab” **Tiekėjo SF antraštė** skyriaus **Sąskaitos faktūros identifikavimas** lauke **Numeris** įveskite **0001**.
21. Skyriaus **Sąskaitos faktūros datos** lauke **Sąskaitos faktūros data** pasirinkite **2021-07-09**.
22. Norėdami registruoti sąskaitą faktūrą, veiksmų srityje pasirinkite **Registruoti**.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>Paslaugų pirkimas naudojant tiekėjo SF

Šioje pavyzdžio dalyje parodyta, kaip naudoti tiekėjo SF perkant paslaugas iš ES šalių.

1. Eikite į **Mokėtinos sumos** > **Sąskaitos faktūros** > **SF žurnalas**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Lauke **Pavadinimas** pasirinkite **VEND\_EUINV**.
4. Veiksmų srityje pasirinkite **Eilutės**.
5. Lauke **Data** įveskite **2021-07-09**.
6. Lauke **Sąskaitos tipas** pasirinkite **Tiekėjas**.
7. Lauke **Sąskaita** pasirinkite **ES tiekėjas**.
8. Lauke **Sąskaitos faktūros data** pasirinkite **2021-07-09**.
9. Lauke **Sąskaita faktūra** įveskite **ITA-0004**.
10. Lauke **Kreditas** įveskite **120000**.
11. Lauke **Korespondentinės sąskaitos** **tipas** pasirinkite **Didžioji knyga**.
12. Lauke **Korespondentinė sąskaita** pasirinkite **110130**.
13. Lauke **PVM grupė** pasirinkite **IT\_PUREU**.
14. Lauke **Prekės PVM grupė** pasirinkite **22%EU**.
15. Skirtuke **Užsienio prekyba** atlikite toliau nurodytus veiksmus.

    1. Lauke **Operacijos kodas** pasirinkite **„1”**.
    2. Lauke **Transportas** pasirinkite **2 (oro)**.
    3. Lauke **Prekė** pasirinkite **\[123456\] Paslauga**.
    4. Lauke **Šalis/regionas** pasirinkite **„ITA”**.
    5. Lauke **Valstybė / provincija** pasirinkite **LAZ**.
    6. Lauke **Kilmės / paskirties šalis** pasirinkite **LT**.


16. Veiksmų srityje pasirinkite **Registruoti**.
17. „Intrastat” įsigijimų deklaracijos kūrimas.

    1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
    2. Veiksmų srityje pasirinkite **Perduoti**.
    3. Dialogo lange **„Intrastat” (perkėlimas)** nustatykite parinktį **Tiekėjo SF** į **Taip**.
    4. Norėdami perkelti operacijas, pasirinkite **Gerai**, tada peržiūrėkite „Intrastat” žurnalą.

   ![„Intrastat” žurnalo puslapio apžvalgos skirtukas.](media/ita_intrastat_journal_vendor_invoice.png)

18. Pirkimo užsakymo skirtuko **Bendra** peržiūra.

    ![„Intrastat” žurnalo eilutės pirkimo užsakymo išsami informacija](media/ita_intrastat_journal_purchase_order_line_details.png)

19. Tiekėjo SF skirtuko **Bendra** peržiūra.

    ![„Intrastat” žurnalo eilutės tiekėjo SF išsami informacija](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. „Intrastat ” įsigijimų ataskaitos generavimas.

    1. Veiksmų srityje pasirinkite **Išvestis** > **Ataskaita**.
    2. Dialogo lango **„Intrastat” ataskaita** skyriaus **Data** lauke **Pradžios data** pasirinkite **2021-07-01**.
    3. Lauke **Pabaigos data** pasirinkite **2021-07-31**.
    4. Skyriuje **Eksportavimo parinktys** nustatykite parinktis **Generuoti failą** ir **Generuoti ataskaitą** į **Taip**.
    5. Lauke **Failo pavadinimas** įveskite **Įsigijimų failas**.
    6. Lauke **Ataskaitos failo pavadinimas** įveskite **Įsigijimų ataskaita**.
    7. Lauke **Kryptis** pasirinkite **Įsigijimai**.
    8. Lauke **Nuorodos numeris** įveskite **123456**.
    9. Norėdami sugeneruoti „Intrastat” ataskaitą, „Intrastat” failą ir juos peržiūrėti, pasirinkite **Gerai**.

    Toliau pateikiamoje iliustracijoje rodomas „Intrastat“ ataskaitos pavyzdys.

    ![„Intrastat” įsigijimų ataskaita.](media/ita_intrastat_arrivals_report.png)

    Toliau pateikiamoje iliustracijoje rodomas „Intrastat“ failo pavyzdys.

    ![„Intrastat” įsigijimų failas.](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>„Intrastat” išsiuntimų registravimas

### <a name="sell-goods-by-using-a-sales-order"></a>Prekių pardavimas naudojant pardavimo užsakymą

Šioje pavyzdžio dalyje parodyta, kaip naudoti pardavimo užsakymą parduodant prekes į Europos Sąjungos (ES) šalis.

1. Pasirinkite **Gautinos sumos** > **Užsakymai** > **Visi pardavimo užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite **ITCO-000002**.
4. Pasirinkite **Gerai**.
5. Rodinyje **Antraštė**, „FastTab” **Pristatymas** skyriaus **Pap. pristatymo informacija** lauke **Pristatymo būdas** pasirinkite **1 (sunkvežimis)**.
6. Lauke **Pristatymo sąlygos** pasirinkite **CFR**.
7. Rodinyje **Eilutės**, „FastTab” **Pardavimo užsakymo eilutės** lauke **Prekės numeris** pasirinkite **ITEM**.
8. Lauke **Kiekis** įveskite **50**.
9. Lauke **Vieta** pasirinkite **1**.
10. Lauke **Sandėlis** pasirinkite **11**.
11. Lauke **Vieneto kaina** įveskite **250**.
12. „FastTab” **Eilutės išsami informacija** skirtuko **Sąranka** dalies **PVM** lauke **Prekės PVM grupė** pasirinkite **22%EU**.
13. Veiksmų srityje pasirinkite **Įrašyti**.
14. Veiksmų srities skirtuke **Sąskaita faktūra**, grupėje **Generuoti**, pasirinkite **Sąskaita faktūra**, kad sukurtumėte užsakymo sąskaitą faktūrą.
15. Dialogo lango **SF registravimas**, esančio „FastTab” **Parametrai** skyriaus **Parametras** lauke **Kiekis** pasirinkite **Visi**.
16. „FastTab” **Sąranka** lauke **Sąskaitos faktūros** **data** pasirinkite **2021-07-09**.
17. Pasirinkite **Gerai**.
18. „Intrastat” žurnalo eilučių peržiūra.

    1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
    2. Veiksmų srityje pasirinkite **Perduoti**.
    3. Dialogo lange **„Intrastat” (perkėlimas)** nustatykite parinktį **Kliento SF** į **Taip**.
    4. Norėdami perkelti operacijas, pasirinkite **Gerai**, tada peržiūrėkite „Intrastat” žurnalą. Kredito pažymos operacija pažymėta kaip taisymas ir turi neigiamą sąskaitos faktūros sumą.

        ![„Intrastat” žurnalo puslapis](media/ita_intrastat_journal_sales_order.png)

        ![„Intrastat” žurnalo eilutės pardavimo užsakymo išsami informacija](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>Prekių grąžinimas naudojant kredito pažymą

Šioje pavyzdžio dalyje parodyta, kaip naudoti kredito pažymą grąžinant prekes iš Europos Sąjungos (ES) šalių.

1. Pasirinkite **Gautinos sumos** > **Užsakymai** > **Visi pardavimo užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite **ITCO-000002**.
4. Pasirinkite **Gerai**.
5. Rodinyje **Antraštė**, „FastTab” **Pristatymas** skyriaus **Pap. pristatymo informacija** lauke **Pristatymo būdas** pasirinkite **1 (sunkvežimis)**.
6. Lauke **Pristatymo sąlygos** pasirinkite **CFR**.
7. „FastTab“ **Užsienio prekyba** lauke **Operacijos kodas** pasirinkite **2 (kelias)**.
8. Skirtuko **Eilutės** „FastTab” **Pardavimo užsakymo eilutės** lauke **Prekės numeris** pasirinkite **ITEM**.
9. Lauke **Kiekis** įveskite **–10**.
10. Lauke **Vieta** pasirinkite **1**.
11. Lauke **Sandėlis** pasirinkite **11**.
12. Lauke **Vieneto kaina** įveskite **250**.
13. „FastTab” **Eilutės išsami informacija** skirtuko **Sąranka** dalies **PVM** lauke **Prekės PVM grupė** pasirinkite **22%EU**.
14. Skyriaus **Grąžintas užsakymas** lauke **Grąžintos partijos ID** pasirinkite anksčiau sukurtą partiją.
15. Veiksmų srityje pasirinkite **Įrašyti**.
16. Veiksmų srities skirtuke **Sąskaita faktūra**, grupėje **Generuoti**, pasirinkite **Sąskaita faktūra**, kad sukurtumėte užsakymo sąskaitą faktūrą.
17. „FastTab” **Parametrai** skyriaus **Parametras** lauke **Kiekis** pasirinkite **Visi**.
18. Dialogo lango **SF registravimas** „FastTab” **Sąranka** lauke **Sąskaitos faktūros** **data** pasirinkite **2021-07-09**.
19. Spustelėkite **Gerai**, kad registruotumėte sąskaitą.
20. „Intrastat” žurnalo eilučių peržiūra.

    1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
    2. Veiksmų srityje pasirinkite **Perduoti**.
    3. Dialogo lange **„Intrastat” (perkėlimas)** nustatykite parinktį **Kliento SF** į **Taip**.
    4. Norėdami perkelti operacijas, pasirinkite **Gerai**, tada peržiūrėkite „Intrastat” žurnalą. Kredito pažymos operacija pažymėta kaip taisymas ir turi neigiamą sąskaitos faktūros sumą.

    ![„Intrastat” žurnalo kredito pažyma](media/ita_intrastat_journal_credit_note.png)

    ![„Intrastat” žurnalo eilutės kredito pažymos išsami informacija](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>Prekių pardavimas į San Mariną naudojant pardavimo užsakymą

Šioje pavyzdžio dalyje parodyta, kaip naudoti pardavimo užsakymą parduodant prekes į San Mariną.

1. Pasirinkite **Gautinos sumos** > **Užsakymai** > **Visi pardavimo užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite **ITCO-000001**.
4. Pasirinkite **Gerai**.
5. Rodinyje **Antraštė**, „FastTab” **Pristatymas** skyriaus **Pap. pristatymo informacija** lauke **Pristatymo būdas** pasirinkite **1**.
6. Lauke **Pristatymo sąlygos** pasirinkite **CFR**.
7. Skirtuko **Eilutės** „FastTab” **Pardavimo užsakymo eilutės** lauke **Prekės numeris** pasirinkite **ITEM**.
8. Lauke **Kiekis** įveskite **30**.
9. Lauke **Vieta** pasirinkite **1**.
10. Lauke **Sandėlis** pasirinkite **11**.
11. Lauke **Vieneto kaina** įveskite **200**.
12. Veiksmų srityje pasirinkite **Įrašyti**.
13. Veiksmų srities skirtuke **Sąskaita faktūra**, grupėje **Generuoti**, pasirinkite **Sąskaita faktūra**, kad sukurtumėte užsakymo sąskaitą faktūrą.
14. „FastTab” **Parametrai** skyriaus **Parametras** lauke **Kiekis** pasirinkite **Visi**.
15. Dialogo lango **SF registravimas** „FastTab” **Sąranka** lauke **Sąskaitos faktūros** **data** pasirinkite **2021-07-09**.
16. Spustelėkite **Gerai**, kad registruotumėte sąskaitą.
17. „Intrastat” žurnalo eilučių peržiūra.

    1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
    2. Veiksmų srityje pasirinkite **Perduoti**.
    3. Dialogo lange **„Intrastat” (perkėlimas)** nustatykite parinktį **Kliento SF** į **Taip**.
    4. Norėdami perkelti operacijas, pasirinkite **Gerai**, tada peržiūrėkite „Intrastat” žurnalą.

   ![„Intrastat” žurnalas, skirtas San Marinui](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![„Intrastat” žurnalo eilutės San Marino išsami informacija](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. „Intrastat” išsiuntimų deklaracijos kūrimas.

    1. Eikite į **Mokesčiai** &gt; **Deklaracijos** &gt; **Užsienio prekyba** &gt; **„Intrastat”**.
    2. Veiksmų srityje pasirinkite **Išvestis** &gt; **Ataskaita**.
    3. Dialogo lango **„Intrastat” ataskaita** skyriaus **Data** lauke **Pradžios data** pasirinkite **2021-07-01**.
    4. Lauke **Pabaigos data** pasirinkite **2021-07-31**.
    5. Skyriuje **Eksportavimo parinktys** nustatykite parinktis **Generuoti failą** ir **Generuoti ataskaitą** į **Taip**.
    6. Lauke **Failo pavadinimas** įveskite **Išsiuntimų failas**.
    7. Lauke **Ataskaitos failo pavadinimas** įveskite **Išsiuntimų ataskaita**.
    8. Lauke **Kryptis** pasirinkite **Išsiuntimai**.
    9. Lauke **Nuorodos numeris** įveskite **98754**.
    10. Norėdami sugeneruoti „Intrastat” ataskaitą ir „Intrastat” failą, pasirinkite **Gerai**.

        Toliau pateikiamoje iliustracijoje rodomas atspausdintos „Intrastat“ ataskaitos pavyzdys.

        ![Intrastat ataskaita](media/ita_intrastat_report_for_dispatches.png)

        Toliau pateikiamoje iliustracijoje rodomas atspausdinto „Intrastat“ failo pavyzdys.

        ![„Intrastat” išsiuntimų failas](media/ita_intrastat_file_for_dispatches.png)

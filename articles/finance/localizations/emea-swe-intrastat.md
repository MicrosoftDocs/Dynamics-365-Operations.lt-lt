---
title: Švedijos „Intrastat”
description: Šiame straipsnyje pateikiama informacija apie Švedijos Intrastat ataskaitas.
author: anasyash
ms.date: 8/24/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: a81f0c19923d1a4747c2ecb8ab03dd86b45497ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886266"
---
# <a name="swedish-intrastat"></a>Švedijos „Intrastat”

[!include[banner](../includes/banner.md)]

Puslapis **„Intrastat”** yra naudojamas generuoti ir skelbti informaciją apie prekybą tarp Europos Sąjungos (ES) šalių. Švedijos „Intrastat” deklaracijoje yra ataskaitoms skirtos informacijos apie prekybą prekėmis.

Į Švedijos „Intrastat” deklaraciją įtraukti toliau nurodyti laukai.

   - Partnerio šalies ISO kodas
   - Operacijos kodas
   - Prekės Kodas
   - Papildomas vienetas
   - Svarba
   - Sąskaitos faktūros suma

## <a name="set-up-intrastat"></a>„Intrastat” nustatymas

Importuokite naujausią toliau pateikiamų elektroninių ataskaitų (ER) konfigūracijų versiją.

   - Intrastat modelis
   - Intrastat ataskaita
   - „Intrastat” (SE)

Daugiau informacijos žr. [ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-foreign-trade-parameters"></a>Nustatyti užsienio prekybos parametrus

1. Microsoft Dynamics 365 finansuose eikite į **Mokesčių nustatymo** > **užsienio** > **prekybos parametrus**.
2. Skirtuko **„Intrastat”** „FastTab“ **Elektroninės ataskaitos** lauke **Failo formato susiejimas** pasirinkite **„Intrastat” (SE)**.
3. **Ataskaitos formatų susiejimas** lauke pasirinkite **„Intrastat” ataskaita**.
4. „FastTab” **Prekių kodų hierarchija** lauke **Kategorijų hierarchija** pasirinkite **„Intrastat”**.
5. **Operacijos kodas** lauke rinkitės pasirinkite turto perkėlimų operacijos kodą. Šis kodas naudojamas operacijoms, kurios sukuria esamus ar planuotus turto pervedimus gavus atlygį (finansinį ar kitą). Taip pat jį naudojate pataisymams. Švedijos įmonės naudoja vieno skaitmens operacijų kodus.
6. **Kredito pažyma** lauke rinkitės pasirinkite prekių grąžinimo operacijos kodą.
7. Skirtuke **Šalies/regiono ypatybės**, laukelyje **šalis/regionas**, išvardykite visas šalis ar regionus, su kuriais įmonė daro verslą. Kiekvienai ES šaliai lauke **Šalies / regiono tipas** pasirinkite **ES**, kad ši šalis būtų rodoma jūsų „Intrastat” ataskaitoje.

## <a name="set-up-the-product-parameters-for-the-intrastat-declaration"></a>„Intrastat” deklaracijos produkto parametrų nustatymas

1. Eikite į **Produkto informacijos valdymas** > **Produktai** > **Patvirtinti produktai**.
2. Tinklelyje pasirinkite produktą.
3. „FastTab” **Užsienio prekyba** skyriaus **„Intrastat”** lauke **Prekė** pasirinkite atitinkamą prekės kodą.
4. „FastTab” **Atsargų valdymas** lauke **Grynasis svoris** įveskite produkto svorį kilogramais.
5. Eikite į **Mokesčiai** > **Nustatymas** > **Užsienio prekyba** > **„Intrastat“ glaudinimas**, ir pasirinkite laukus, kurie turi būti lyginami apibendrinant „Intrastat” informaciją. Pasirinkite toliau pateikiamus laukus, skirtus Švedijos „Intrastat“.

    - Prekė
    - Operacijos kodas
    - Kryptis
    - Šalis/regionas
    - Koregavimas
    - PVM sąskaita faktūra

## <a name="intrastat-transfer"></a>„Intrastat” perkėlimas

Veiksmų srities puslapyje **„Intrastat”** galite pasirinkti **Perkelti**, kad informacija apie ES vidaus prekybą būtų automatiškai perkelta iš jūsų pardavimo užsakymų, laisvos formos SF, pirkimo užsakymų, tiekėjo SF, tiekėjo produktų gavimo kvitų, projekto SF ir perkėlimo užsakymų. Bus perkelti tik dokumentai, kurių paskirties šalis ar regionas (išsiuntimams) arba siuntimas (įsigijimams) yra ES šalis.

Taip pat rankiniu būdu galite įvesti operacijas pasirinkę **Nauja** veiksmų srityje.

### <a name="generate-an-intrastat-report"></a>„Intrastat” ataskaitos generavimas

1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
2. Veiksmų srityje pasirinkite **Išvestis** > **Ataskaita**.
3. Dialogo lange **„Intrastat” ataskaita** nustatykite toliau nurodytus laukus.

    | Laukas            | Aprašas                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Nuo datos        | Pasirinkite ataskaitos pradžios datą.                                                                                               |
    | Iki datos          | Pasirinkite ataskaitos pabaigos datą.                                                                                                 |
    | Sugeneruoti failą    | Šią parinktį nustatykite į **Taip**, kad sugeneruotumėte „Intrastat” ataskaitos .txt failą.                                                       |
    | Failo vardas        | Įveskite .txt failo pavadinimą.                                                                                                    |
    | Generuoti ataskaitą  | Šią parinktį nustatykite į **Taip**, kad sugeneruotumėte „Intrastat” ataskaitos .xlsx failą.                                                     |
    | Ataskaitos failo vardas | Įveskite .xlsx failo pavadinimą.                                                                                                   |
    | Kryptis        | Pasirinkite **Įsigijimai** ataskaitai apie ES vidaus įsigijimus. Pasirinkite **Išsiuntimai** ataskaitai apie ES vidaus išsiuntimus. |

4. Pasirinkite **Gerai** ir peržiūrėkite sugeneruotas ataskaitas.

## <a name="example"></a>Pavyzdys

Šis pavyzdys rodo, kaip registruoti Intrastat gymus ir išsiuntimus. Jis naudoja **„DEMF”** juridinį subjektą.

### <a name="preliminary-setup"></a>Pirminis nustatymas

1. Eikite į **Organizacijos administracija** > **Organizacija** > **Juridiniai subjektai** ir pasirinkite juridinį subjektą **DEMF**.
2. „FastTab” **Adresai** pasirinkite **Redaguoti**, tada lauke **Šalis / regionas** pasirinkite **SWE (Švedija)**.
3. Importuokite naujausią toliau pateikiamų ER konfigūracijų versiją.

    - Intrastat modelis
    - Intrastat ataskaita
    - „Intrastat” (SE)

### <a name="create-transaction-codes"></a>Operacijos kodų kūrimas

1. Pasirinkite **Mokesčiai** > **Nustatymas** > **Užsienio prekyba** > **Operacijų kodai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Lauke **Operacijos** **kodas** lauke įveskite **1**.
4. Lauke **Pavadinimas** įveskite **Įprastos operacijos**
5. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="set-up-foreign-trade-parameters"></a>Nustatyti užsienio prekybos parametrus

1. Pasirinkite **Mokesčiai** > **Nustatymai** > **Užsienio prekyba** > **Užsienio prekybos parametrai**.
2. Skirtuke **Intrastat** „FastTab” **Bendri**, **Perlaidos** **kode** laukelis rinkitės **1**.
3. „FastTab” **Elektroninės ataskaitos** lauke **Failo formato susiejimas** pasirinkite **„Intrastat” (SE)**.
4. **Ataskaitos formatų susiejimas** lauke pasirinkite **„Intrastat” ataskaita**.
5. „FastTab” **Prekių kodų hierarchija** lauke **Kategorijų hierarchija** laukelyje įsitikinkite, kad **„Intrastat”** yra pasirinktas.
6. Skirtuke **Šalis/regione ypatybėse** rinkitės **Naujas**.
7. Lauke **Šalis valstybės/regione** pasirinkite **SWE**.
8. Lauke **Šalies / regiono tipas** pasirinkite **Vietinė**.
9. Lauke **Šalies šalis / regionas** pasirinkite **DEU**, tada lauke **Šalies / regiono tipas** – **ES**.

### <a name="set-up-product-information"></a>Produkto informacijos nustatymas

1. Eikite į **Produkto informacijos valdymas** > **Produktai** > **Išleisti produktai**.
2. Tinklelyje pasirinkite **D0001**.
3. „FastTab” **Užsienio prekyba** srityje **Intrastat** lauke **Prekės** rinkitės **100 200 30**.
4. Skirtuko **Valdyti atsargas** FastTab", **Svorio matavimo** skyriuje **Grynasis svoris** laukelis rinkitės **5**.
5. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="change-the-site-address"></a>Vietos adreso keitimas

1. Eikite į **Sandėlio valdymas** > **Sąranka** > **Sandėlis** > **Vietos**.
2. Tinklelyje pasirinkite **„1”**.
3. „FastTab“ **Adresai** pasirinkite **Redaguoti**.
4. Dialogo lange **Redaguoti adresą** lauke **Šalis / regionas** pasirinkite **SWE**.
5. Pasirinkite **Gerai**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Pardavimo užsakymo ES klientui kūrimas

1. Pasirinkite **Gautinos sumos** > **Užsakymai** > **Visi pardavimo užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Dialogo lango **Kurti pardavimo užsakymą** „FastTab“ **Klientas** skyriuje **Klientas** lauke **Kliento paskyra** rinkitės **DE-015**.
4. Skirtuko **Bendra** „FastTab" **saugojimo dimensijų** skyriuje, **lauke** Svetainė, pasirinkite **1**.
5. Lauke **Sandėlis** pasirinkite **11**.
6. Pasirinkite **Gerai**.
7. Skirtuko **Eilutės** „FastTab” **Pardavimo užsakymo eilutės** lauke **Prekės numeris** pasirinkite **D0001**. Tada, lauke **Kiekis** įveskite **10**.
8. Įsitikinkite, kad „FastTab” **Eilutės išsami informacija** skirtuko **Užsienio prekyba** laukai **Operacijos kodas** ir **Prekė** nustatyti automatiškai.
9. Veiksmų srityje pasirinkite **Įrašyti**.
10. Veiksmų srities skirtuke **SF**, esančiame **Generuoti** skyriuje, pasirinkite **SF**.
11. Dialogo lango **SF registravimas**, esančio „FastTab” **Parametrai** skyriaus **Parametras** lauke **Kiekis** pasirinkite **Visi**.
12. Spustelėkite **Gerai**, kad registruotumėte sąskaitą.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Operacijos perkėlimas į „Intrastat” žurnalą ir rezultato peržiūra

1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
2. Veiksmų srityje pasirinkite **Perduoti**.
3. Dialogo lango **„Intrastat” (Perkelti)** skyriuje **Parametrai** nustatykite **Kliento sąskaitos faktūros** parinktį į **Taip**.
4. Pasirinkite **Filtras**.
5. Teksto laukelyje **Intrastat filtras** skirtuke **Intervalas** pasirinkite pirmąją eilutę ir įsitikinkite, kad **Laukelis** yra nustatytas **Data**.
6. Lauke **Kriterijai** pasirinkite dabartinę datą.
7. Pasirinkite **Gerai**, kad uždarytumėte „Intrastat“ filtrą **Užklausa**.
8. Rinkitės **Gerai** tam, kad užvertumėte **Intrastat (Perduoti)** teksto laukelį ir peržiūrėkite rezultatą. Eilutėje rodomas prekybos užsakymas, kurį sukurėte anksčiau.

    ![„Intrastat” žurnalo pardavimo užsakymo eilutės](media/swe_intrastat_journal_sales_order.png)

9. Pasirinkite operacijos eilutę, tada, norėdami peržiūrėti **daugiau** informacijos, pasirinkite skirtuką Bendra.

    ![„Intrastat” žurnalo eilutės pardavimo užsakymo išsami informacija](media/swe_intrastat_journal_sales_order_line_details.png)

10. Veiksmų srityje pasirinkite **Išvestis** > **Ataskaita**.
11. Dialogo lango **„Intrastat” ataskaita**, esančio „FastTab” **Parametrai** skyriuje **Data** pasirinkite sukurto pardavimo užsakymo mėnesį.
12. Skyriuje **Eksportavimo** **parinktys** nustatykite **Generuoti failą** į **Taip**. Tada lauke **Failo pavadinimas** įveskite reikiamą pavadinimą.
13. Parinktį **Generuoti ataskaitą** nustatykite kaip **Taip**. Tada lauke **Ataskaitos failo pavadinimas** įveskite reikiamą pavadinimą.
14. Lauke **Kryptis** pasirinkite **Išsiuntimai**.
15. Pasirinkite **Gerai** ir peržiūrėkite sugeneruotą ataskaitą .txt formatu. Toliau pateikiamoje lentelėje nurodomos pavyzdžio ataskaitos vertės.

    | Partnerio šalies ISO kodas | Operacijos kodas | Prekės Kodas | Papildomas vienetas | Svarba | Sąskaitos faktūros suma |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 50     | 3290           |

16. Peržiūrėkite sukurtą ataskaitą „Excel“ formatu.

    ![Intrastat ataskaita](media/swe_intrastat_report_for_dispatches.png)

### <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

1. Eikite į **Mokėtinos sumos** > **Pirkimo užsakymai** > **Visi pirkimo užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Dialogo lango **Sukurti pirkimo užsakymą** lauke **Tiekėjo paskyra** pasirinkite **DE-001**.
4. Pasirinkite **Gerai**.
5. Skirtuko **Antraštė** „FastTab” **Užsienio** **prekyba** patikrinkite, ar laukas **Operacijos kodas** nustatytas į **1**.
6. Skirtuko **Eilutės** „FastTab” **Pirkimo užsakymo eilutės** lauke **Prekės numeris** pasirinkite **D0001**. Tada, lauke **Kiekis** įveskite **6**.
7. Veiksmų srities skirtuke **Pirkimas**, grupėje **Veiksmai**, pasirinkite **Patvirtinti**.
8. Veiksmų srities skirtuke **SF**, esančiame grupėje **Generuoti**, pasirinkite **SF**.
9. Veiksmų juostoje, pasirinkite **Numatyt. iš**. Lauke **Numatytasis eilučių kiekis** pasirinkite **Užsakytas kiekis**. Tada pasirinkite **Gerai**.
10. „FastTab” **Tiekėjo SF antraštė** skyriaus **Sąskaitos faktūros identifikavimas** lauke **Numeris** įveskite **0001**.
11. Norėdami registruoti sąskaitą faktūrą, veiksmų srityje pasirinkite **Registruoti**.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>„Intrastat” įsigijimų deklaracijos kūrimas

1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
2. Veiksmų srityje pasirinkite **Perduoti**.
3. Dialogo lange **„Intrastat” (perkėlimas)** nustatykite parinktį **Tiekėjo SF** į **Taip**.
4. Norėdami perkelti operacijas, pasirinkite **Gerai**, tada peržiūrėkite „Intrastat” žurnalą.

    ![Pirkimo užsakymo „Intrastat” žurnalas](media/swe_intrastat_journal_purchase_order.png)

5. Pirkimo užsakymo skirtuko **Bendra** peržiūra.

    ![„Intrastat” žurnalo eilutės pirkimo užsakymo išsami informacija](media/swe_intrastat_journal_purchase_order_line_details.png)

6. Veiksmų srityje pasirinkite **Išvestis** > **Ataskaita**.
7. Dialogo lango **„Intrastat” ataskaita**, esančio „FastTab” **Parametrai** skyriuje **Data** pasirinkite sukurto pardavimo užsakymo mėnesį.
8. Skyriuje **Eksportavimo** **parinktys** nustatykite **Generuoti failą** į **Taip**. Tada lauke **Failo pavadinimas** įveskite reikiamą pavadinimą.
9. Parinktį **Generuoti ataskaitą** nustatykite kaip **Taip**. Tada lauke **Ataskaitos failo pavadinimas** įveskite reikiamą pavadinimą.
10. Lauke **Kryptis** pasirinkite **Įsigijimai**.
11. Pasirinkite **Gerai** ir peržiūrėkite sugeneruotą ataskaitą .txt formatu. Toliau pateikiamoje lentelėje nurodomos pavyzdžio ataskaitos vertės.

    | Partnerio šalies ISO kodas | Operacijos kodas | Prekės Kodas | Papildomas vienetas | Svarba | Sąskaitos faktūros suma |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 30     | 1714           |

12. Peržiūrėkite sukurtą ataskaitą „Excel“ formatu.

    ![„Intrastat” įsigijimų ataskaita](media/swe_intrastat_arrivals_report.png)

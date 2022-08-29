---
title: Vokietijos Intrastat
description: Šiame straipsnyje pateikiama informacija apie Vokietijos Intrastat deklaraciją.
author: AdamTrukawka
ms.date: 09/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: ae978b28098d92d84415c29bbe76157144f862d8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269441"
---
# <a name="german-intrastat"></a>Vokietijos Intrastat

[!include [banner](../includes/banner.md)]

Puslapis **„Intrastat”** yra naudojamas generuoti ir skelbti informaciją apie prekybą tarp Europos Sąjungos (ES) šalių. Vokietijos Intrastat deklaracijoje yra informacijos apie prekybą prekėmis ataskaitoms. Ataskaita suformuota pagal Vokietijos valdžios institucijų gaires, pateiktas [6.2 failo deklaracijos INSTAT/XML formatu](https://www-idev.destatis.de/idev/doc/intra_en/hilfe6_2.html) puslapyje.

Toliau pateiktoje lentelėje rodomi Vokietijos „Intrastat” deklaracijos laukai.

| Laukai | Išsiuntimai | Gavimai |
|-------------------------|-------------------------|-------------------------|
| Nuorodos laikotarpis | X | X |
| Krypties kodas | X | X |
| Intrastat deklaracijos valiuta</br>**Pastaba:** Ši valiuta yra <em>apskaitos valiuta</em>. | X | X |
| Prekės kodas | X | X |
| Prekės pavadinimas | X | X |
| Papildomo vieneto kodas | X | X |
| Konsignacijos/paskirties valstybė narė | X | X |
| Grynoji masė | X | X |
| Kiekis papildomais vienetais | X | X |
| Kilmės šalis |  | X |
| Sąskaitos faktūros suma | X |  |
| Statistinė vertė | X | X |
| Operacijų pobūdis | X | X |
| Transportavimo būdas | X | X |
| Regiono kodas</br>**Pastaba:**</br><ul></br><li>Jei kilmės šalis arba regionas yra Vokietija, o SF skirta išsiuntimams, rodomas kilmės šalies Intrastat kodas.</li></br><li>Jei kilmės šalis arba regionas nėra Vokietija, o SF skirta išsiuntimams, rodomas kodas **99**.</li></br><li>Jei SF skirta atvykimams, rodomas šalies Intrastat kodas.</li></br></ul> | X | X |
| Prievado/paslaugos/inlando prievado kodas | X | X |
| Pristatymo sąlygos | X | X |


## <a name="set-up-intrastat"></a>„Intrastat” nustatymas

1. Nustatyti įmonės kodus.

    1. Pasirinkite **Organizacijos administravimas** > **Organizacijos** > **Juridiniai subjektai**.
    2. Užsienio **prekybos ir logistikos** „FastTab" **identifikavimo** skyriaus ID lauke įveskite mainų sutarties **DVR**. Šis ID bus įtrauktas į ataskaitą.
    3. Lauke **PVM kodo eksportavimo** įveskite savo įmonės pridėtinės vertės įveskite savo įmonės pridėtinės vertės
    4. Lauke **PVM kodo importavimo** įveskite savo įmonės pridėtinės vertės mokesčio įveskite savo įmonės pridėtinės vertės
    5. Intrastat **kodo lauke** įveskite Intrastat kodą, kuris priskirtas juridiniam subjektui.
    6. FastTab **Mokesčių registracija** lauke **Mokesčių mokėtojo kodas** įveskite savo įmonės mokesčių mokėtojo kodą.

    > [!NOTE]
    > Jei sugeneruojate susijusių įmonių Intrastat ataskaitą, **mokesčio registracijos numerio** lauke savo pirminės įmonės mokesčio registracijos numerį.

2. [„Microsoft Dynamics Lifecycle Services” (LCS)](https://lcs.dynamics.com/Logon/Index) bendrai naudojamo turto bibliotekoje atsisiųskite naujausias šių Elektroninių ataskaitų (ER) konfigūracijų versijas „Intrastat” deklaracijai.

    - Intrastat modelis
    - Intrastat ataskaita
    - INSTAT XML
    - INSTAT XML (DE)

3. Nustatyti užsienio prekybos parametrus:

    1. Programoje "Dynamics 365 Finance" eikite į **mokesčių nustatymo** > **užsienio** > **prekybos parametrus**.
    2. Skirtuke **Intrastat** tab, „FastTab“ **Elektroninės ataskaitos** lauke **Failo formato susiejimas** laukelyje rinkitės **Intrastat XML (DE)**.
    3. **Ataskaitos formatų susiejimas** lauke pasirinkite **„Intrastat” ataskaita**.
    4. „FastTab” **Prekių kodų hierarchija** lauke **Kategorijų hierarchija** pasirinkite **„Intrastat”**.
    5. **Operacijos kodas** lauke rinkitės pasirinkite turto perkėlimų operacijos kodą. Naudojate šį kodą operacijoms, kurios sukuria esamus ar planuotus turto pervedimus gavus atlygį (finansinis ar kitas). Taip pat jį naudojate pataisymams.
    6. **Kredito pažyma** lauke rinkitės pasirinkite prekių grąžinimo operacijos kodą.
    7. Lauke **Darbuotojas** pasirinkite kontaktinį asmenį „Intrastat” ataskaitai. Taip pat galite skirtuke **Kontaktas** įvesti arba pasirinkti laukų **Pavadinimas**, **Telefonas**, **Faksas**, **El. paštas** ir **Internetinis adresas** reikšmes. Šie laukai yra įtraukti į ataskaitą.
    8. Valdžios **lauke** pasirinkite Intrastat instituciją.
    9. Eikite į **Mokesčiai** > **Netiesioginiai mokesčiai** > **Pardavimo mokesčiai** > **Pardavimo mokesčio įgaliojimai** ir įveskite tolesnę informaciją apie „Intrastat“ teises, kurias pasirinkote ankstesniame žingsnyje:

       - Valdžios institucijos identifikacija
       - Adresas
       - Kontaktinė informacija

    10. Skirtuke **Šalies/regiono ypatybės**, laukelyje **šalis/regionas**, išvardykite visas šalis ar regionus, su kuriais įmonė daro verslą. Kiekvienos šalies arba regiono **šalies/regiono tipo** laukeliui rinkitės **ES**, kad šalis arba regionas būtų jūsų Intrastat ataskaitoje.

4. Nustatyti regiono kodus.

    1. Pasirinkite **Organizacijos administravimas** > **Visuotinė adresų knygelė** > **Adresai** > **Adresų nustatymas**.
    2. Lauko **Valstybė/regionas** skirtuke **Šalis/regionas** pasirinkite **DEU** tada pasirinkite **Taikyti filtrą**.
    3. Tinklelyje pasirinkite būseną. Tada **Intrastat kodas** įveskite unikalų „Intrastat“ kodą.

5. Nustatyti produkto kilmės adresą.

    1. Eikite į **Produkto informacijos valdymas** > **Produktai** > **Patvirtinti produktai**.
    2. Tinklelyje pasirinkite produktą.
    3. „FastTab” **Užsienio prekyba** srityje **Intrastat** lauke **Kilmės šalis** rinkitės **DEU**.

6. Eikite į **Mokesčiai** > **Nustatymas** > **Užsienio prekyba** > **„Intrastat“ glaudinimas**, ir pasirinkite laukus, kurie turi būti lyginami apibendrinant „Intrastat” informaciją. Vokietijos „Intrastat“ rinkitės šiuos laukus:

    - Prekė
    - Šalis/regionas
    - Koregavimas
    - Kryptis
    - Pristatymo sąlygos
    - PVM sąskaita faktūra
    - Kilmės šalis/regionas
    - Uostas
    - Siuntėjo šalis / regionas
    - Siuntėjo valstybė
    - Statistikos procedūra
    - Operacijos kodas
    - Transportavimas
    - Mokesčių lengvatos numeris

### <a name="intrastat-transfer"></a>„Intrastat” perkėlimas

Veiksmų srities puslapyje **Intrastat** puslapyje, veiksmų juostoje rinkitės **Perkelti** kad informacija apie ES vidaus prekybą būtų automatiškai perkelta iš jūsų pardavimo užsakymų, laisvos formos SF, pirkimo užsakymų, tiekėjo SF, tiekėjo produktų gavimo kvitų **,** projekto SF ir perkėlimo užsakymų. Bus perkelti tik dokumentai, kurių paskirties šalis ar regionas (išsiuntimams) arba siuntimas (įsigijimams) yra ES šalis.

Taip pat rankiniu būdu galite įvesti operacijas pasirinkę **Nauja** veiksmų srityje.

### <a name="generate-an-intrastat-report"></a>„Intrastat” ataskaitos generavimas

1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
2. Veiksmų srityje pasirinkite **Išvestis** > **Ataskaita**.
3. Dialogo lange **„Intrastat” ataskaita** nustatykite toliau nurodytus laukus.

    | Laukas | Aprašas |
    |-------------------------|-------------------------|
    | Nuo datos | Pasirinkite ataskaitos pradžios datą. |
    | Iki datos | Pasirinkite ataskaitos pabaigos datą. |
    | Sugeneruoti failą | Šią parinktį nustatykite į **Taip**, kad sugeneruotumėte .xml failą. |
    | Failo vardas | Palikite šį lauką tuščią. Failo vardas generuojamas automatiškai ir jį sudaro failo vardo **&lt;plėtinio &gt;** XML žymę plius failo vardo plėtinio **.xml** vertė.</br>**&lt;Glausta &gt;** Id vertė yra šių elementų suastingimas šia tvarka:</br><ol type="1"></br><li>Skirtuko **&lt;interchangeAgreementId&gt;** vertė</li></br><li>Brūkšnelis (-)</li></br><li>Vertė **&lt;referencePeriod in YYYYMM&gt;** skirtuke</li></br><li>Brūkšnelis (-)</li></br><li>Žymės **&lt;Envelope/DateTime/date in YYYYMMDD&gt;** vertė</li></br><li>Brūkšnelis (-)</li></br><li>Žymės **&lt;Envelope/DateTime/time in hhmm&gt;** vertė</li></br></ol> |
    | Kryptis | <ul></br><li>Pasirinkite **Įsigijimai** ataskaitai apie ES vidaus įsigijimus.</li></br><li>Pasirinkite **Išsiuntimai** ataskaitai apie ES vidaus išsiuntimus.</li></br><li>Pasirinkite **Abu** gavimai ir išleidimai.</li></br></ul> |
    | PVM mokėtojo kodas | Įvesti registracijos numerį, naudotią siuntėjo identifikavimo kodui sugeneruoti, jei numeris skiriasi nuo juridinio subjekto mokesčių registracijos numerio. |


## <a name="example"></a>Pavyzdys

Šis pavyzdys rodo, kaip registruoti Intrastat gymus ir išsiuntimus. Jis naudoja **„DEMF”** juridinį subjektą.

1. Lauke [LCS](https://lcs.dynamics.com/Logon/Index), bendrai naudojamo turto bibliotekoje atsisiųskite naujausias šių ER konfigūracijų versijas „Intrastat” deklaracijos formatui:

    - Intrastat modelis
    - Intrastat ataskaita
    - Intrastat XML
    - Intrastat XML (DE)

2. Kurti operacijos kodus.

    1. Pasirinkite **Mokesčiai** > **Nustatymas** > **Užsienio prekyba** > **Operacijų kodai**.
    2. Veiksmų srityje pasirinkite **Naujas**.
    3. Lauke **Operacijos** **kodas** lauke įveskite **21**.
    4. Lauke **Pavadinimas** įveskite **Prekių grąžinimas**.
    5. Veiksmų srityje pasirinkite **Įrašyti**.

3. Nustatyti valdžios identifikavimo numerį.

    1. Eikite į **Mokestis** > **Netiesioginiai mokesčiai** > **PVM** > **PVM institucijos**.
    2. Sąraše **TA** rinkitės.
    3. Valdžios **identifikavimo lauke** įveskite **123**.

4. Nustatyti regiono kodus.

    1. Pasirinkite **Organizacijos administravimas** > **Visuotinė adresų knygelė** > **Adresai** > **Adresų nustatymas**.
    2. Lauko **Valstybė/regionas** skirtuke **Šalis/regionas** pasirinkite **DEU** tada pasirinkite **Taikyti filtrą**.
    3. Tinklelyje pasirinkite **BE**, tada Intrastat kodo **lauke** įveskite **11**.
    4. Veiksmų srityje pasirinkite **Įrašyti**.

5. Nustatyti užsienio prekybos parametrus.

    1. Pasirinkite **Mokesčiai** > **Nustatymai** > **Užsienio prekyba** > **Užsienio prekybos parametrai**.
    2. Skirtuke **Intrastat** „FastTab” **Bendri**, **Perlaidos** **kode** laukelis rinkitės **11**.
    3. Lauke **Kredito pažyma** pasirinkite **21**.
    4. Laukelis **Teisės** rinkitės **TA**.
    5. „FastTab” **Elektroninės ataskaitos** lauke **Failo formato susiejimas** pasirinkite **INSTAT XML (DE)**.
    6. **Ataskaitos formatų susiejimas** lauke pasirinkite **„Intrastat” ataskaita**.
    7. „FastTab” **Prekių kodų hierarchija** lauke **Kategorijų hierarchija** laukelyje įsitikinkite, kad **„Intrastat”** yra pasirinktas.
    8. Skirtuke **Šalis/regione ypatybėse** rinkitės **Naujas**.
    9. Lauke **Šalis valstybės/regione** pasirinkite **FRA**.
    10. Lauke **Šalies / regiono tipas** pasirinkite **EU**.

6. Priskirti prekės kodą produktui ir nustatyti produkto kilmę. Pasirinkus **Prekės kodas**, **Šalis/kilmės regionas**, ir **Kilmės šalis** laukeliai tuomet bus automatiškai nustatomi prekybos užsakymuose ir pirkimo užsakymuose pasirenkante produktą.

    1. Eikite į **Produkto informacijos valdymas** > **Produktai** > **Patvirtinti produktai**.
    2. Tinklelyje pasirinkite **D0001**.
    3. „FastTab” **Užsienio prekyba** srityje **Intrastat** lauke **Prekės** rinkitės **920 20 34**.
    4. Skyriuje **Kilmė** lauke **Šalis/regionas** rinkitės **DEU**.
    5. Skirtuko **Valdyti atsargas** FastTab", **Svorio matavimo** skyriuje **Grynasis svoris** laukelis rinkitės **12**.
    6. Veiksmų srityje pasirinkite **Įrašyti**.

7. Priskirti transportą pristatymo būdui. Transportavimo kodas užsakymuose bus nustatytas automatiškai, kai pasirenkate pristatymo būdą.

    1. Eikite į **Įsigijimas ir šaltinio pasirinkimas** > **Nustatymai** > **Skirstymas** > **Pristatymo režimai**.
    2. Sąraše pasirinkite **10**.
    3. „FastTab“ **Užsienio prekyba** lauke **Transportas** pasirinkite **„01”**.

8. Kurti pardavimo užsakymą ES klientui.

    1. Pasirinkite **Gautinos sumos** > **Užsakymai** > **Visi pardavimo užsakymai**.
    2. Veiksmų srityje pasirinkite **Naujas**.
    3. Dialogo lango **Kurti pardavimo užsakymą** „FastTab“ **Klientas** skyriuje **Klientas** lauke **Kliento paskyra** rinkitės **DE-012**.
    4. Skirtuko **Bendra** „FastTab" **saugojimo dimensijų** skyriuje, **lauke** Svetainė, pasirinkite **1**.
    5. Lauke **Sandėlis** pasirinkite **11**.
    6. Pasirinkite **Gerai**.
    7. Skirtuke **Antraštė** „FastTab“ **Užsienio prekyba** laukelyje **Prievadas** rinkitės **53**.
    8. Statistinės **procedūros lauke** pasirinkite **31710**.
    9.  Skirtuke **Eilutės** eilutėse **Prekybos užsakymas** **eilutės** „FastTab“ lauke **Prekės numeris** rinkitės **D0001**. Tada, lauke **Kiekis** įveskite **10**.
    10. „FastTab“ **Eilutės informacijos** skirtuke **Užsienio prekyba** įsitikinkite, kad **Perlaidos kodas**, **Transportas**, **Prekė** ir **Kilmės šalis/regionas** laukelis yra nustatytas automatiškai.
    11. Veiksmų srityje pasirinkite **Įrašyti**.
    12. Veiksmų srities skirtuke **SF**, esančiame **Generuoti** skyriuje, pasirinkite **SF**.
    13. Dialogo lango **SF registravimas**, esančio „FastTab” **Parametrai** skyriaus **Parametras** lauke **Kiekis** pasirinkite **Visi**.
    14. Spustelėkite **Gerai**, kad registruotumėte sąskaitą.

9.  Perkelti operaciją į Intrastat žurnalą ir peržiūrėti rezultatą.

    1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
    2. Veiksmų srityje pasirinkite **Perduoti**.
    3. Dialogo lango **„Intrastat” (Perkelti)** skyriuje **Parametrai** nustatykite **Kliento sąskaitos faktūros** parinktį į **Taip**.
    4. Pasirinkite **Filtras**.
    5. Teksto laukelyje **Intrastat filtras** skirtuke **Intervalas** pasirinkite pirmąją eilutę ir įsitikinkite, kad **Laukelis** yra nustatytas **Data**.
    6. Lauke **Kriterijai** pasirinkite dabartinę datą.
    7. Pasirinkite **Gerai**, kad uždarytumėte „Intrastat“ filtrą **Užklausa**.
    8. Rinkitės **Gerai** tam, kad užvertumėte **Intrastat (Perduoti)** teksto laukelį ir peržiūrėkite rezultatą. Eilutėje rodomas prekybos užsakymas, kurį sukurėte anksčiau.

        ![Eilutė, kurioje rodomas pardavimo užsakymai „Intrastat“ puslapyje](media/intrastat_deu_1.png)

10. Pasirinkite operacijos eilutę, tada, norėdami peržiūrėti **daugiau** informacijos, pasirinkite skirtuką Bendra.

    ![Išsami pardavimo užsakymo informacija „Intrastat“ puslapio skirtuke Bendra](media/intrastat_deu_2.png)

11. Kredito pažymos naudojant prekybos užsakymą.

    1. Pasirinkite **Gautinos sumos** > **Užsakymai** > **Visi pardavimo užsakymai**.
    2. Veiksmų srityje pasirinkite **Naujas**.
    3. Dialogo lango **Kurti pardavimo užsakymą** „FastTab“ **Klientas** skyriuje **Klientas** lauke **Kliento paskyra** rinkitės **DE-012**.
    4. Skirtuko **Bendra** „FastTab" **saugojimo dimensijų** skyriuje, **lauke** Svetainė, pasirinkite **1**.
    5. Lauke **Sandėlis** pasirinkite **11**.
    6. Skirtuke **Antraštė** „FastTab“ **Užsienio prekyba** laukelyje **Prievadas** rinkitės **53**.
    7. Statistinės **procedūros lauke** pasirinkite **31710**.
    8. Skirtuke **Eilutės** eilutėse **Prekybos užsakymas** **eilutės** „FastTab“ lauke **Prekės numeris** rinkitės **D0001**. Tada, lauke **Kiekis** įveskite **-2**.
    9. „FastTab” **Eilutės informacija** skirtuko **Užsienio prekyba** lauke **Operacijos kodas** pasirinkite **„21”**.
    10. Įsitikinkite, kad **Transportas**, **Prekės** ir **Prekė ir Kilmės šalis/regionas** yra nustatomi automatiškai.
    11. Veiksmų srityje pasirinkite **Įrašyti**.
    12. Veiksmų srities skirtuke **SF**, esančiame **Generuoti** skyriuje, pasirinkite **SF**.
    13. Dialogo lango **SF registravimas**, esančio „FastTab” **Parametrai** skyriaus **Parametras** lauke **Kiekis** pasirinkite **Visi**.
    14. Spustelėkite **Gerai**, kad registruotumėte sąskaitą.

12. Perkelti operaciją į Intrastat žurnalą ir peržiūrėti rezultatą.

    1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
    2. Veiksmų srityje pasirinkite **Perduoti**.
    3. Dialogo lango **„Intrastat” (Perkelti)** skyriuje **Parametrai** nustatykite **Kliento sąskaitos faktūros** parinktį į **Taip**.
    4. Rinkitės **Gerai** tam, kad užvertumėte **Intrastat (Perduoti)** teksto laukelį ir peržiūrėkite rezultatą. Pridėta nauja eilutė, kur nustatytas laukas **Kryptis** yra nustatytas **Gavimai**.            
        Ši eilutė nurodo fizinį prekių grąžinimą.

        ![Faktinio prekių grąžinimo eilutė Intrastat puslapyje](media/intrastat_deu_3.png)

13. Pasirinkite operacijos eilutę, tada, norėdami peržiūrėti **daugiau** informacijos, pasirinkite skirtuką Bendra.

    ![Faktinio prekių grąžinimo informacija Intrastat puslapio skirtuke Bendra](media/intrastat_deu_4.png)

14. Kurti taisymą naudojant prekybos užsakymą:

    1. Pasirinkite **Gautinos sumos** > **Užsakymai** > **Visi pardavimo užsakymai**.
    2. Veiksmų srityje pasirinkite **Naujas**.
    3. Dialogo lango **Kurti pardavimo užsakymą** „FastTab“ **Klientas** skyriuje **Klientas** lauke **Kliento paskyra** rinkitės **DE-012**.
    4. Skirtuko **Bendra** „FastTab" **saugojimo dimensijų** skyriuje, **lauke** Svetainė, pasirinkite **1**.
    5. Lauke **Sandėlis** pasirinkite **11**.
    6. Skirtuke **Antraštė** „FastTab“ **Užsienio prekyba** laukelyje **Prievadas** rinkitės **53**.
    7. Statistinės **procedūros lauke** pasirinkite **31710**.
    8. Skirtuke **Eilutės** eilutėse **Prekybos užsakymas** **eilutės** „FastTab“ lauke **Prekės numeris** rinkitės **D0001**. Tada, lauke **Kiekis** įveskite **-3**.
    9. „FastTab” **Eilutės informacija** skirtuko **Užsienio prekyba** lauke **Operacijos kodas** pasirinkite **„11”**.
    10. Įsitikinkite, kad **Transportas**, **Prekės** ir **Prekė ir Kilmės šalis/regionas** yra nustatomi automatiškai.
    11. Veiksmų srityje pasirinkite **Įrašyti**.
    12. Įsitikinkite, kad laukas **Perlaidos kodas** nustatytas į 11.
    13. Veiksmų srities skirtuke **SF**, esančiame **Generuoti** skyriuje, pasirinkite **SF**.
    14. Dialogo lango **SF registravimas**, esančio „FastTab” **Parametrai** skyriaus **Parametras** lauke **Kiekis** pasirinkite **Visi**.
    15. Spustelėkite **Gerai**, kad registruotumėte sąskaitą.

15. Perkelti operaciją į Intrastat žurnalą ir peržiūrėti rezultatą:

    1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
    2. Veiksmų srityje pasirinkite **Perduoti**.
    3. Dialogo lango **„Intrastat” (Perkelti)** skyriuje **Parametrai** nustatykite **Kliento sąskaitos faktūros** parinktį į **Taip**.
    4. Rinkitės **Gerai** tam, kad užvertumėte **Intrastat (Perduoti)** teksto laukelį ir peržiūrėkite rezultatą. Nauja eilutė, kurioje koregavimo stulpelyje atsiranda **varnelė**.

        ![Intrastat puslapio taisymo eilutė](media/intrastat_deu_5.png)

16. Pasirinkite operacijos eilutę, tada, norėdami peržiūrėti **daugiau** informacijos, pasirinkite skirtuką Bendra.

    ![Išsami keitimo informacija „Intrastat“ puslapio skirtuke Bendra](media/intrastat_deu_6.png)

17. Veiksmų srityje pasirinkite **Išvestis** > **Ataskaita**.
18. Dialogo lango **„Intrastat” ataskaita**, esančio „FastTab” **Parametrai** skyriuje **Data** pasirinkite sukurto pardavimo užsakymo mėnesį.
19. Skyriuje **Eksportavimo** **parinktys** nustatykite **Generuoti failą** į **Taip**.
20. Lauke **Failo pavadinimas** įveskite reikiamą pavadinimą.
21. Pasirinkite **Gerai** ir peržiūrėkite sugeneruotą ataskaitą. Toliau pateikiamoje lentelėje nurodomos pavyzdžio ataskaitos vertės.

    | **Pavadinimas / vardas ir (arba) pavardė**                  | **Pardavimo sąskaita faktūra**  |   **Koregavimas**   | **Kredito sąskaita** |
    |---------------------------|--------------------|--------------------|-----------------|
    | declarationId             | 2021-07-D          | 2021-07-A          |                 |
    | referencePeriod           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functionCode              | O                  | O                  |                 |
    | flowCode                  | D                  | A                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | itemNumber                | 0000362            | 0000362            | 0000361         |
    | CN8 Kodas                   | 9202034            | 9202034            | 9202034         |
    | goodsDescription          | Pranešėjas            | Pranešėjas            | Pranešėjas         |
    | MSConsDestCode            | FR                 | FR                 | FR              |
    | countryOfOriginCode       | \-                 | \-                 | DE              |
    | netMass                   | 120                | -36                | 24              |
    | invoicedAmount            | 3290               | -987               | \-              |
    | StatisticalValue          | 3290               | -987               | 658             |
    | natureOfTransactionACode  | 1                  | 1                  | 2               |
    | natureOfTransactionBCode  | 1                  | 1                  | 1               |
    | modeOfTransportCode       | 01                 | 01                 | 01              |
    | regionCode                | 11                 | 11                 | 11              |
    | portAirportInlandportCode | 53                 | 53                 | 53              |


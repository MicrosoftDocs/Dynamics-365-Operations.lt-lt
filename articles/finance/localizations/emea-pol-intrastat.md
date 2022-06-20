---
title: Lenkijos „Intrastat“
description: Šiame straipsnyje pateikiama informacija apie Intrastat ataskaitas Lenkijos ataskaitose.
author: andosip
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.openlocfilehash: 45bd1d3c90d0a8a8ad5db6d0b80c5eed0aa489e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871107"
---
# <a name="polish-intrastat"></a>Lenkijos „Intrastat“

[!include[banner](../includes/banner.md)]

Puslapis **„Intrastat”** yra naudojamas generuoti ir skelbti informaciją apie prekybą tarp Europos Sąjungos (ES) šalių. Lenkijos Intrastat deklaracijoje yra informacijos apie prekybą prekėmis ataskaitoms.

Šie laukai yra įtraukti į Lenkijos Intrastat deklaraciją. **Visi laukai yra įtraukti atvežant ir išsiuntimuose, išskyrus RodzajTransportu** (transportavimo būdą) **ir Patamspochodcenia** (kilmės šalį arba regioną), kurie neįtraukiami išsiuntimuose ir **IdKontrahenta** (kliento užsienio PVM numeris), kuris neįtrauktas į atvykimus.

| Lauko pavadinimas | Aprašymas |
|-------------------------|-------------------------|
| Deklaracja duomenys | Data, kada dokumentas sukurtas. |
| Mieskaitė | Deklaracijos nuorodos mėnuo. |
| Rok | Deklaracijos nuorodų metai. |
| Skaičius | Deklaracijos numeris ataskaitiniu laikotarpiu. |
| Wersja | Deklaracijos versijos numeris. |
| Nr. Išd. | Deklaracijos identifikatorius. Vertė sugeneruojama automatiškai. |
| Tipo įvestis | Ataskaitos kryptis.</br><li>Gavimų atveju išspausdinama "P".</li><li>Išsiuntimams spausdinama "W".</li> |
| Rodzaj | Deklaracijos tipas. Vertė nurodo, ar ataskaita yra originali deklaracija, ar koregavimo deklaracija. |
| UC | Vieneto kodas, į kurį yra adresinė Intrastat deklaracija. Vertė yra nurodyta pvm **skyriaus, kuris** **yra** užsienio prekybos parametrų puslapio **skirtuke Agentas** **, lauke PVM** kodas. |
| Turiva | Įmonės pavadinimas. |
| Miejmt sąsk., Yranumeris, KodPoczt užd. | Visas juridinio subjekto adresas. |
| Nop | Lenkijos mokesčių identifikavimo numeris (pridėtinės vertės mokesčio [PVM] ID). |
| Regonas | Lenkijos statistinis identifikavimo numeris (įmonės numeris). |
| LacznaWartoscFaktur | SF verčių suma. |
| LacznaWartoscStatystyczna | Statistinių verčių suma. |
| LacznaLiczbaPozycji | Bendras prekių skaičius. |
| "PozId" | D punkto prekių skaičius eina iš eilės. |
| OpisTowaru | Prekės prekybos pavadinimas. |
| AlcPochodzeniaWyshomeki | Tarptautinės standartizavimo organizacijos (ISO) kodas, skirtas kitai šaliai arba regionui. |
| Tamsusis demensas | Pristatymo sąlygų Intrastat kodas. |
| RodzajTransakcji | Operacijos pobūdį nurodantis kodas. Lenkiškos įmonės naudoja dviejų skaitmenų operacijų kodus. |
| KodTowarade | Aštuonių skaitmenų prekės kodas pagalCombined Nomenclature. |
| RodzajTransportu | Transportavimo režimo Intrastat kodas. |
| AlcPochodcenia | Šalies ar regiono, kuriame prekės buvo pagamintos arba pagamintos, ISO kodas. |
| Netto | Grynoji masė visiškai kilogramais. |
| IloscPvupelniajacaJm | Kiekis, nurodytas papildomais matavimo vienetais, s visos skaičiais. |
| ArbatoscFaktury | Visų operacijų, kurias apima viena prekė, SF vertė. |
| ArbatoscStatystyczna | Statistinė vertė. |
| Pelniajacy: HlwiskoImie, Telefon, Faks, el. paštas | Asmens, kuris pateikia deklaraciją, vardas ir pavardė, telefono numeris, fakso numeris ir el. pašto adresas. |
| IdKontrahenta | Kliento užsienio PVM numeris ES šalyje narėje. |


## <a name="set-up-intrastat"></a>„Intrastat” nustatymas

Iš visuotinės saugyklos importuokite naujausią šių elektroninių ataskaitų (ER) konfigūracijų versiją:

   - Intrastat modelis
   - Intrastat ataskaita
   - Intrastat (PL)

Daugiau informacijos žr. [ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Nustatykite savo įmonės PVM ID ir įmonės numerį

### <a name="create-registration-types-for-company-codes"></a>Kurti įmonės kodų registracijos tipus

Turite sukurti du įmonės kodų registracijos tipus: vieną – PVM ID (NIP kodui) ir kitą – įmonės numeriui (Regon kodas).

1. Eikite į **organizacijos administravimo** > **visuotinės adresų knygelės** > **registracijos tipų** > **registracijos tipus**.
2. Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte PVM ID registracijos tipą.
3. Į dialogo **langą Įvesti registracijos** tipo informaciją **, lauke** Pavadinimas įveskite naujo registracijos tipo pavadinimą. Pvz., įveskite **NIP**.
4. Lauke **Šalis/regionas** pasirinkite **„POL”**.
5. Pasirinkite **Kurti**.
6. Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte įmonės numerio registracijos tipą.
7. Į dialogo **langą Įvesti registracijos** tipo informaciją **, lauke** Pavadinimas įveskite naujo registracijos tipo pavadinimą. Pavyzdžiui, įveskite **Regon**.
8. Lauke **Šalis/regionas** pasirinkite **„POL”**.
9. Pasirinkite **Kurti**.

### <a name="match-the-registration-types-with-registration-categories"></a>Registracijos tipus sugretinti su registracijos kategorijomis

1. Eikite į **organizacijos administravimo** > **visuotinės adresų knygelės** > **registracijos tipų** > **registracijos kategorijas**.
2. Veiksmų srityje pasirinkite Naujas, kad **sukurtumėte** saitą tarp kiekvieno sukurto registracijos tipo ir registracijos kategorijos.

    - Norėdami nustatyti PVM ID (NIP kodo) registracijos tipą, pasirinkite **PVM ID registracijos** kategoriją.
    - Norėdami nustatyti įmonės numerio registracijos tipą (Regon kodas), pasirinkite įmonės **ID (COID) registracijos** kategoriją.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Nustatykite savo įmonės PVM ID ir įmonės numerį

1. Pasirinkite **Organizacijos administravimas** > **Organizacijos** > **Juridiniai subjektai**.
2. Tinklelyje pasirinkite savo įmonę.
3. Veiksmų srityje pasirinkite **registracijos PVM**.
4. **Registracijos ID** "FastTab" pasirinkite **Įtraukti**.
5. Registracijos tipo **lauke** pasirinkite vieną iš registracijos tipų, kuriuos sukūrėte anksčiau.
6. Įveskite savo įmonės PVM ID (NIP kodą) arba įmonės numerį (Regon kodas), priklausomai nuo registracijos tipo, kurį pasirinkote ankstesniame veiksme.
7. Kito registracijos tipo, kurį sukūrėte anksčiau, atveju pakartokite 4–6 veiksmus.

## <a name="set-up-a-company-address"></a>Įmonės adreso pasirinkimas

1. Pasirinkite **Organizacijos administravimas** > **Organizacijos** > **Juridiniai subjektai**.
2. Tinklelyje pasirinkite savo įmonę.
3. Skirtuke **Adresai** pasirinkite **Redaguoti**.
4. **Dialogo lango Redaguoti** adresą lauke **Pašto indeksas** pasirinkite įmonės pašto indeksą.
5. Lauke Gatvė **įveskite** adresą.
6. Lauke Miestas **pasirinkite** miestą.

## <a name="set-up-foreign-trade-parameters"></a>Nustatyti užsienio prekybos parametrus

1. Pereikite prie **mokesčių nustatymo** > **·** > **užsienio prekybos parametrų**.
2. Intrastat skirtuko **elektroninės** ataskaitos **"FastTab"** failo formato išdėstymo **lauke** pasirinkite **Intrastat (PL).**
3. **Ataskaitos formatų susiejimas** lauke pasirinkite **„Intrastat” ataskaita**.
4. „FastTab” **Prekių kodų hierarchija** lauke **Kategorijų hierarchija** pasirinkite **„Intrastat”**.
5. **Operacijos kodas** lauke rinkitės pasirinkite turto perkėlimų operacijos kodą. Šis kodas naudojamas operacijoms, kurios sukuria esamus ar planuotus turto pervedimus gavus atlygį (finansinį ar kitą). Taip pat jį naudojate pataisymams. Lenkijos įmonės naudoja dviejų skaitmenų operacijų kodus.
6. **Kredito pažyma** lauke rinkitės pasirinkite prekių grąžinimo operacijos kodą.
7. Skirtuke **Šalies/regiono ypatybės**, laukelyje **šalis/regionas**, išvardykite visas šalis ar regionus, su kuriais įmonė daro verslą. Kiekvienos šalies, kuri yra ES dalis, **·** **šalies/** regiono tipo lauke pasirinkite ES, kad šalis būtų rodoma jūsų Intrastat ataskaitoje. Lenkijai lauke **Šalies** /regiono tipas **pasirinkite Vietinis**.
8. Agento **skirtuko** Agento **·**"FastTab **·** **·**" PVM skyriaus PVM lauke įveskite 420 000 **,** kad nurodykite vieneto kodą, į kurį adres įrašoma Intrastat deklaracija.
9. Skirtuke **Kontaktas** įveskite asmens, kuris pateikia deklaraciją, vardą, telefono numerį, fakso numerį ir el. pašto adresą.
10. Skirtuke **Numeracijos** nurodykite **·** **XML** failo numerio nuorodos numeracijos kodo lauką, kuriame yra daugiausiai devyni simboliai. Šis laukas naudojamas Intrastat ataskaitos deklaracijos identifikatoriaus lauko **vertei** automatiškai generuoti.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Nustatyti Intrastat deklaracijos produkto parametrus

1. Eikite į **Produkto informacijos valdymas** > **Produktai** > **Patvirtinti produktai**.
2. Tinklelyje pasirinkite produktą.
3. „FastTab” **Užsienio prekyba** skyriaus **„Intrastat”** lauke **Prekė** pasirinkite atitinkamą prekės kodą. Prekės pavadinimas bus spausdinamas **Intrastat ataskaitos lauke** Prekės aprašymas.
4. **Kilmės** skyriaus lauke **Šalis/regionas** pasirinkite produkto kilmės šalį arba regioną.
5. „FastTab” **Atsargų valdymas** lauke **Grynasis svoris** įveskite produkto svorį kilogramais.

## <a name="set-up-compression-of-intrastat"></a>Nustatyti Intrastat suspaudimą

-   Eikite į **Mokesčiai** > **Nustatymas** > **Užsienio prekyba** > **„Intrastat“ glaudinimas**, ir pasirinkite laukus, kurie turi būti lyginami apibendrinant „Intrastat” informaciją. Jei norite pasirinkti Lenkijos Intrastat, pasirinkite šiuos laukus:

    - Prekė
    - Operacijos kodas
    - Kilmės šalis/regionas
    - Transportavimas
    - Pristatymo sąlygos
    - Siuntėjo šalis / regionas
    - Šalis / regionas
    - Koregavimas
    - Mokesčių lengvatos numeris
    - Kryptis
    - Sąskaita faktūra

## <a name="set-up-the-transport-method-and-delivery-terms"></a>Nustatyti transportavimo metodą ir pristatymo sąlygas

1.  Nustatyti transportavimo kodus.

    1. Pasirinkite **Mokesčiai** > **Nustatymas** > **Užsienio prekyba** > **Transportavimo būdas**.
    2. Veiksmų srityje pasirinkite **Naujas**.
    3. Į lauką **Transportavimas** įveskite unikalų kodą. Lenkiškos įmonės naudoja vieno skaitmens transportavimo kodus.

2.  Nustatyti pristatymo būdo Intrastat kodus.

    1. Eikite **į įsigijimo ir pirkimo nustatymo** > **·** > **pristatymo** > **paskirstymo sąlygas**.
    2. Tinklelyje pasirinkite pristatymo sąlygų rinkinį.
    3. Bendrajame **FastTab**, Intrastat kodo **lauke**, įveskite unikalų kodą.

## <a name="intrastat-transfer"></a>„Intrastat” perkėlimas

Veiksmų srities puslapyje **„Intrastat”** galite pasirinkti **Perkelti**, kad informacija apie ES vidaus prekybą būtų automatiškai perkelta iš jūsų pardavimo užsakymų, laisvos formos SF, pirkimo užsakymų, tiekėjo SF, tiekėjo produktų gavimo kvitų, projekto SF ir perkėlimo užsakymų. Bus perkelti tik dokumentai, kurių ES šalis yra paskirties arba konsignacijos šalis arba regionas.

Operacijas galite įvesti ir neautomatiniu būdu veiksmų **srityje** pasirinkdami Naujas.

### <a name="generate-an-intrastat-report"></a>„Intrastat” ataskaitos generavimas

1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
2. Veiksmų srityje pasirinkite **Išvestis** &gt; **Ataskaita**.
3. Dialogo lange **„Intrastat” ataskaita** nustatykite toliau nurodytus laukus.

    | Laukas | Aprašymas |
    |-------------------------|-------------------------|
    | Nuo datos | Pasirinkite ataskaitos pradžios datą. |
    | Sugeneruoti failą | Nustatyti šią pasirinktį **kaip Taip**, kad būtų sugeneruotas jūsų Intrastat ataskaitos .xml failas. |
    | Failo vardas | Įveskite .xml failo pavadinimą. |
    | Generuoti ataskaitą | Šią parinktį nustatykite į **Taip**, kad sugeneruotumėte „Intrastat” ataskaitos .xlsx failą. |
    | Ataskaitos failo vardas | Įveskite .xlsx failo pavadinimą. |
    | Kryptis | Pasirinkite **Įsigijimai** ataskaitai apie ES vidaus įsigijimus.</br>Pasirinkite **Išsiuntimai** ataskaitai apie ES vidaus išsiuntimus. |
    | Deklaracijos identifikatorius | Dokumento ID sugeneruojamas automatiškai ir jį galima atnaujinti. |
    | Deklaracijos tipas | Pasirinkite **originalios** deklaracijos deklaraciją.</br>Pasirinkite **Deklaracijos taisymas – pataisymų** deklaracijos pakeitimas, skirtas visiškai pakeisti esamą, anksčiau pateiktą originalią arba pataisų deklaraciją. |
    | Miestas, kuriame sukurtas dokumentas | Įveskite vertę, kuri turi būti išspausdinta **Intrastat deklaracijos lauke Miejinimosc**. |
    | Dokumento sukūrimo data | Įveskite vertę, kuri turi būti išspausdinta **Intrastat deklaracijos lauke** Deklaracja Duomenys. |
    | Dokumento Nr. | Įvesti vertę, kuri turi būti išspausdinta **Intrastat deklaracijos** lauke Numer. |
    | Dokumento versija | Įvesti vertę, kuri turi būti išspausdinta **Intrastat deklaracijos lauke Wersja**. |

4. Pasirinkite **Gerai** ir peržiūrėkite sugeneruotas ataskaitas.

## <a name="example"></a>Pavyzdys

Šiame pavyzdyje nurodoma, kaip registruoti Intrastat gymus ir išsiuntimus naudojant **DEMF juridinį** subjektą.

### <a name="preliminary-setup"></a>Pirminis nustatymas

Importuokite naujausią toliau pateikiamų ER konfigūracijų versiją.

   - Intrastat modelis
   - Intrastat ataskaita
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Įmonės adreso pasirinkimas

1. Pasirinkite **Organizacijos administravimas** > **Visuotinė adresų knygelė** > **Adresai** > **Adresų nustatymas**.
2. Skirtuke **Miestas** pasirinkite **Naujas**.
3. Lauke **Šalis/regionas** pasirinkite **„POL”**.
4. Lauke Miestas **įveskite Paslaugos** **.**
5. Skirtuke **Pašto indeksas** pasirinkite **Naujas**.
6. Lauke **Šalis/regionas** pasirinkite **„POL”**.
7. Lauke Miestas **pasirinkite** Paslaugos **·**.
8. Lauke pašto **indeksas įveskite** **00–844**.
9. Eikite į **Organizacijos administracija** > **Organizacija** > **Juridiniai subjektai** ir pasirinkite juridinį subjektą **DEMF**.
10. „FastTab“ **Adresai** pasirinkite **Redaguoti**.
11. Lauke **Šalis/regionas** pasirinkite **„POL”**.
12. Lauke Pašto **indeksas pasirinkite** **31–111**.
13. Lauke Gatvė **įveskite** **Statystyczna 22/1**.
14. Lauke Miestas **pasirinkite** Paslaugos **·**.
15. Pasirinkite **Gerai**.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>Jūsų įmonei nustatyti PVM ID ir įmonės numerio kodą

### <a name="create-registration-types-for-company-codes"></a>Kurti įmonės kodų registracijos tipus

1. Eikite į **organizacijos administravimo** > **visuotinės adresų knygelės** > **registracijos tipų** > **registracijos tipus**.
2. Veiksmų srityje pasirinkite Naujas **, kad** sukurtumėte PVM ID (NIP kodo) registracijos tipą.
3. Į dialogo **langą Įvesti registracijos** tipo informaciją lauke **Pavadinimas** įveskite **NIP**.
4. Lauke **Šalis/regionas** pasirinkite **„POL”**.
5. Pasirinkite **Kurti**.
6. Veiksmų srityje pasirinkite Naujas **, kad** sukurtumėte įmonės numerio (Regon kodas) registracijos tipą.
7. Į dialogo **langą Įvesti registracijos** tipo informaciją, lauke **Pavadinimas** įveskite **Regon**.
8. Lauke **Šalis/regionas** pasirinkite **„POL”**.
9. Pasirinkite **Kurti**.

### <a name="match-the-registration-types-with-registration-categories"></a>Registracijos tipus sugretinti su registracijos kategorijomis

1. Eikite į **organizacijos administravimo** > **visuotinės adresų knygelės** > **registracijos tipų** > **registracijos kategorijas**.
2. Veiksmų srityje pasirinkite Naujas, kad **sukurtumėte** saitą tarp kiekvieno sukurto registracijos tipo ir registracijos kategorijos.

    - Norėdami pasirinkti **NIP** registracijos tipą, pasirinkite **PVM ID** registracijos kategoriją.
    - **Regon registracijos** tipui pasirinkite įmonės **ID (COID) registracijos** kategoriją.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Nustatykite savo įmonės PVM ID ir įmonės numerį

1. Pasirinkite **Organizacijos administravimas** > **Organizacijos** > **Juridiniai subjektai**.
2. Tinklelyje pasirinkite **DEMF**.
3. Veiksmų srityje pasirinkite **registracijos PVM**.
4. **Registracijos ID** "FastTab" pasirinkite **Įtraukti**.
5. **Lauke Registracijos tipas** pasirinkite **NIP**.
6. Į registracijos **numerio lauką** įveskite **1234567890**.
7. Pasirinkite **Įtraukti**.
8. **Lauke Registracijos tipas** pasirinkite **Regon**.
9. Į registracijos **numerio lauką** įveskite **12345678901234**.

### <a name="set-up-a-number-sequence-code"></a>Numeracijos kodo pasirinkimas

1. Pasirinkite **Organizacijos administravimas** > **Numeracijos** > **Numeracijos**.
2. Veiksmų srities skirtuke Numeracija **, grupėje Naujas** **, pasirinkite Numeracija** **.**
3. Skirtuke **Identifikavimas** "FastTab" numeracijos **kodo** lauke įveskite **XML\_ failą**.
4. Aprėpties **parametrų** "FastTab" lauke **Apimtis** pasirinkite **Įmonė**.
5. **Lauke Įmonė** pasirinkite **DEMF**.
6. Segmentų **"** FastTab" lauke **Ilgis įveskite** Raidinis-skaitinis **segmentas** **4**.
7. Skyriaus **Nustatymas** bendro FastTab **nustatykite** pasirinktį Ištisinis **kaip** **Ne**.
8. Numerių paskirstymo **skyriuje, lauke Didžiausias** **, įveskite** 9999 **.**

### <a name="set-up-foreign-trade-parameters"></a>Nustatyti užsienio prekybos parametrus

1. Pasirinkite **Mokesčiai** > **Nustatymai** > **Užsienio prekyba** > **Užsienio prekybos parametrai**.
2. Skirtuke **Intrastat** „FastTab” **Bendri**, **Perlaidos** **kode** laukelis rinkitės **11**.
3. Elektroninės ataskaitos **"** FastTab" failo formato **susiejimo lauke** pasirinkite **Intrastat (PL).**
4. **Ataskaitos formatų susiejimas** lauke pasirinkite **„Intrastat” ataskaita**.
5. Prekių kodų **hierarchijos** "FastTab" patikrinkite, ar **kategorijų hierarchijos** laukas nustatytas kaip **Intrastat**.
6. Skirtuke **Šalis/regione ypatybėse** rinkitės **Naujas**.
7. Lauke **Šalis valstybės/regione** pasirinkite **POL**. Tada lauke Šalies **/regiono tipas** pasirinkite **Vietinis**.
8. Lauke **Šalis valstybės/regione** pasirinkite **DEU**. Tada lauke Šalies **/regiono tipas** pasirinkite **ES**.
9. Agento **skirtuko** Agento **·**"FastTab **·**" PVM skyriaus PVM lauke, **PVM** mokėtojo kodo lauke, įveskite **420 000.**
10. Skirtuko Kontaktas **lauke** Pavadinimas **įveskite** Nebaigta **Žmogusra**.
11. Lauke Telefonas **įveskite 425-555-5068** **.**
12. **Lauke Fakso numeris** įveskite 425-555-5049 **·**.
13. Lauke El **. paštas** įveskite manishc@contoso.com **·**.
14. **Skirtuke Numeracijos**, XML failo **numerio nuorodos** numeracijos kodo **lauke** pasirinkite **XML\_ failą**.

### <a name="set-up-product-information"></a>Produkto informacijos nustatymas

1. Eikite į **produkto informacijos valdymo** > **produktus išleistus** > **·** **produktus.**
2. Tinklelyje pasirinkite **D0001**.
3. „FastTab” **Užsienio prekyba** srityje **Intrastat** lauke **Prekės** rinkitės **100 200 30**.
4. Skirtuko **Valdyti atsargas** FastTab", **Svorio matavimo** skyriuje **Grynasis svoris** laukelis rinkitės **2**.
5. Veiksmų srityje pasirinkite **Įrašyti**.
6. Tinklelyje pasirinkite **D0003**.
7. „FastTab” **Užsienio prekyba** srityje **Intrastat** lauke **Prekės** rinkitės **100 200 30**.
8. Skyriuje **Kilmė** lauke **Šalis/regionas** rinkitės **DEU**.
9. Skirtuko **Valdyti atsargas** FastTab", **Svorio matavimo** skyriuje **Grynasis svoris** laukelis rinkitės **5**.
10. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="change-the-site-address"></a>Vietos adreso keitimas

1. Eikite į **Sandėlio valdymas** > **Sąranka** > **Sandėlis** > **Vietos**.
2. Tinklelyje pasirinkite **„1”**.
3. „FastTab“ **Adresai** pasirinkite **Redaguoti**.
4. Dialogo lange **Redaguoti adresą** lauke **Šalis / regionas** pasirinkite **POL**.
5. Pasirinkite **Gerai**.

### <a name="set-up-a-transport-method"></a>Transportavimo metodo nustatyti

1. Kurti transportavimo būdą.

    1. Pasirinkite **Mokesčiai** > **Nustatymas** > **Užsienio prekyba** > **Transportavimo būdas**.
    2. Veiksmų srityje pasirinkite **Naujas**.
    3. **Lauke Transportavimas** įveskite **3**.
    4. Aprašymo **lauke** įveskiteVz.transportavimas **·**.

2. Priskirti naują transportavimo metodą pristatymo režimui. Tokiu būdu galite nustatyti numatytąsias vertes, naudojamas transportavimo metodui, kai pasirinktas atitinkamas pristatymo būdas.

    1. Eikite į **Įsigijimas ir šaltinio pasirinkimas** > **Nustatymai** > **Skirstymas** > **Pristatymo režimai**.
    2. Tinklelyje pasirinkite **„10”**.
    3. „FastTab“ **Užsienio prekyba** lauke **Transportas** pasirinkite **„3”**.

3. Pasirinkti numatytąjį kliento pristatymo būdą.

    1. Pasirinkite **Gautinos sumos** > **Klientai** > **Visi klientai**.
    2. Tinklelyje pasirinkite **DE-016**.
    3. **SF ir pristatymo "** FastTab" pristatymo **būdo lauke** pasirinkite **10**.

4. Pasirinkti numatytąjį tiekėjo pristatymo būdą.

    1. Eiti į Mokėtinų **sumų** > **tiekėjai** > **Visi tiekėjai**.
    2. Tinklelyje pasirinkite **DE-001**.
    3. **SF ir pristatymo "** FastTab" pristatymo **būdo lauke** pasirinkite **10**.

### <a name="set-up-codes-for-terms-of-delivery"></a>Nustatyti pristatymo sąlygų kodus

1. Nustatyti pristatymo sąlygų Intrastat kodą.

    1. Eikite **į įsigijimo ir pirkimo nustatymo** > **·** > **pristatymo** > **paskirstymo sąlygas**.
    2. Tinklelyje pasirinkite **CIF**.
    3. Skirtuko Bendra **FastTab** intrastat kodo **lauke** įveskite **CIF**.

2. Pasirinkti kliento numatytąsias pristatymo sąlygas.

    1. Pasirinkite **Gautinos sumos** > **Klientai** > **Visi klientai**.
    2. Tinklelyje pasirinkite **DE-016**.
    3. SF ir **pristatymo "** FastTab", lauke **Pristatymo sąlygos**, pasirinkite **CIF**.

3. Pasirinkti numatytąsias tiekėjo pristatymo sąlygas.

    1. Eiti į Mokėtinų **sumų** > **tiekėjai** > **Visi tiekėjai**.
    2. Tinklelyje pasirinkite **DE-001**.
    3. SF ir **pristatymo "** FastTab", lauke **Pristatymo sąlygos**, pasirinkite **CIF**.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>ES kliento neapmokestinimo kodo tikrinimas

1. Pasirinkite **Gautinos sumos** > **Klientai** > **Visi klientai**.
2. Tinklelyje pasirinkite **DE-016**.
3. SF ir **pristatymo "FastTab** **" PVM skyriuje patikrinkite,** ar LAUKAS PVM mokėtojo **kodas nustatytas kaip** DE9012 **·**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Pardavimo užsakymo ES klientui kūrimas

1. Pasirinkite **Gautinos sumos** > **Užsakymai** > **Visi pardavimo užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Dialogo lango **Kurti pardavimo užsakymą** „FastTab“ **Klientas** skyriuje **Klientas** lauke **Kliento paskyra** rinkitės **DE-016**.
4. Skirtuko **Bendra** „FastTab" **saugojimo dimensijų** skyriuje, **lauke** Svetainė, pasirinkite **1**.
5. Lauke **Sandėlis** pasirinkite **11**.
6. Skirtuke **Adresas** patikrinkite, **·** **ar laukas Adresas nustatytas kaip Terastos 12, Kkie, 24103, DEU**, nes klientas yra iš Vokietijos.
7. Pasirinkite **Gerai**.
8. Skirtuko **Antraštėje**, **pristatymo** "FastTab", patikrinkite, **·** **ar lauke Pristatymo sąlygos nustatyta kaip CIF**, **o pristatymo** būdo lauke nustatyta **10.**
9. Skirtuko **Eilutės** „FastTab” **Pardavimo užsakymo eilutės** lauke **Prekės numeris** pasirinkite **D0001**. Tada, lauke **Kiekis** įveskite **8**.
10. Skirtuke Eilutės informacija FastTab, **užsienio** prekybos skirtuke, patikrinkite, **·** **ar operacijos kodas lauke nustatytas kaip 11**, **·** **prekės lauke nustatyta 100 200 30**, **o kilmės šalis / regionas** laukas nustatytas **kaip POL.** **·**
11. Veiksmų srityje pasirinkite **Įrašyti**.
12. Veiksmų srities skirtuke **SF**, esančiame grupėje **Generuoti**, pasirinkite **SF**.
13. Dialogo lango **SF registravimas**, esančio „FastTab” **Parametrai** skyriaus **Parametras** lauke **Kiekis** pasirinkite **Visi**.
14. Lauko Pardavimo **data** nustatymo "FastTab **·**" pasirinkite **2021-18-10 (2021** m. spalio 18 d.).
15. Spustelėkite **Gerai**, kad registruotumėte sąskaitą.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Operacijos perkėlimas į „Intrastat” žurnalą ir rezultato peržiūra

1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
2. Veiksmų srityje pasirinkite **Perduoti**.
3. Dialogo lango **„Intrastat” (Perkelti)** skyriuje **Parametrai** nustatykite **Kliento sąskaitos faktūros** parinktį į **Taip**.
4. Pasirinkite **Filtras**.
5. Intrastat filtro **dialogo lange**, skirtuke **Diapazonas**, pasirinkite pirmą eilutę ir patikrinkite, **ar lauko laukas** nustatytas kaip **Data**.
6. Lauke **Kriterijai** pasirinkite dabartinę datą.
7. Pasirinkite **Gerai**, kad uždarytumėte „Intrastat“ filtrą **Užklausa**.
8. Rinkitės **Gerai** tam, kad užvertumėte **Intrastat (Perduoti)** teksto laukelį ir peržiūrėkite rezultatą. Eilutėje rodomas prekybos užsakymas, kurį sukurėte anksčiau.

    ![Eilutė, kurioje rodomas pardavimo užsakymai „Intrastat“ puslapyje](media/intrastat_pl_1.png)

9. Pasirinkite operacijos eilutę, tada, norėdami peržiūrėti **daugiau** informacijos, pasirinkite skirtuką Bendra.

    ![Išsami pardavimo užsakymo informacija „Intrastat“ puslapio skirtuke Bendra](media/intrastat_pl_2.png)

10. Veiksmų srityje pasirinkite **Išvestis** > **Ataskaita**.
11. Intrastat ataskaitos **dialogo lango parametrų** **FastTab, skyriuje Data,** **lauke** Nuo **datos pasirinkite pirmą dabartinio mėnesio dieną.**
12. Skyriuje **Eksportavimo** **parinktys** nustatykite **Generuoti failą** į **Taip**. Tada lauke **Failo pavadinimas** įveskite reikiamą pavadinimą.
13. Parinktį **Generuoti ataskaitą** nustatykite kaip **Taip**. Tada lauke **Ataskaitos failo pavadinimas** įveskite reikiamą pavadinimą.
14. Lauke **Kryptis** pasirinkite **Išsiuntimai**.
15. Failo formato **susiejimo skyriuje** patikrinkite, ar deklaracijos **tipo laukas** nustatytas kaip **Deklaracija**.
16. Į dokumentų **kūrimo miestą** įveskiteVz., Užd **·**.
17. Lauke Dokumento **sukūrimo data pasirinkite** **2021-19-10 (2021** m. spalio 19 d.).
18. Į lauką **Dokumento** nr. įveskite **11**.
19. Lauke Dokumento **versija** įveskite **22**.
20. Pasirinkite **Gerai** ir peržiūrėkite sugeneruotą XML formato ataskaitą. Toliau pateikiamoje lentelėje nurodomos pavyzdžio ataskaitos vertės.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Lauko pavadinimas</strong></p>
    </td>
    <td>
    <p><strong>Lauko aprašas</strong></p>
    </td>
    <td>
    <p><strong>Reikšmė</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informacija apie dokumentą</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja duomenys</p>
    </td>
    <td>
    <p>Data, kada buvo sukurtas dokumentas.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miej į sąsk.</p>
    </td>
    <td>
    <p>Miestas, kuriame dokumentas buvo sukurtas.</p>
    </td>
    <td>
    <p>Krokuva</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Bendras prekių skaičius.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Bendroji statistinė vertė.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Bendroji SF vertė.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Vieneto kodas.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Deklaracijos tipas.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Dokumento versija.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Skaičius</p>
    </td>
    <td>
    <p>Dokumento numeris.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Mieskaitė</p>
    </td>
    <td width="330">
    <p>Nuorodos mėnuo.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="330">
    <p>Nuorodos metai.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Tipo įvestis</p>
    </td>
    <td width="330">
    <p>Ataskaitos kryptis.</p>
    </td>
    <td>
    <p>T</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Nr. Išd.</p>
    </td>
    <td width="330">
    <p>Deklaracijos identifikatorius.</p>
    </td>
    <td>
    <p>21ISTDEMF-0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informacija apie įmonę</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miej į sąsk.</p>
    </td>
    <td width="330">
    <p>Miestas, kuriame yra įmonė.</p>
    </td>
    <td>
    <p>Varšuva</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regonas</p>
    </td>
    <td width="330">
    <p>Įmonės Regon kodas.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nop</p>
    </td>
    <td>
    <p>Įmonės NIP kodas.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPoczt užd.</p>
    </td>
    <td>
    <p>Įmonės pašto indeksas.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Įsanika-skaitas</p>
    </td>
    <td>
    <p>Gatvė, kurioje yra įmonė.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Turiva</p>
    </td>
    <td>
    <p>Įmonės pavadinimas.</p>
    </td>
    <td>
    <p>"Contoso" pramogų sistemos Vokietija</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informacija apie tinkamas</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>ArbatoscStatystyczna</p>
    </td>
    <td>
    <p>Statistinė vertė.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>ArbatoscFaktury</p>
    </td>
    <td>
    <p>SF vertė.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Netto</p>
    </td>
    <td>
    <p>Grynoji masė.</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IdKontrahenta</p>
    </td>
    <td>
    <p>Kliento PVM numeris.</p>
    </td>
    <td>
    <p>"DE9012"</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarade</p>
    </td>
    <td>
    <p>Prekės kodas.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Operacijos kodas.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Tamsusis demensas</p>
    </td>
    <td>
    <p>Pristatymo būdo sąlygos.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>AlcPochodzeniaWyshomeki</p>
    </td>
    <td>
    <p>Išsiuntimo / paskirties šalies arba regiono kodas.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Prekių aprašymas.</p>
    </td>
    <td>
    <p>Aparatūra</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>"PozId"</p>
    </td>
    <td>
    <p>Prekės numeris.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Kontaktinė informacija</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>El. laiškas</p>
    </td>
    <td>
    <p>Pateikimo asmens el. pašto adresas.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Itks</p>
    </td>
    <td>
    <p>Pateikimo aparato fakso numeris.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefonų telefonai</p>
    </td>
    <td>
    <p>Pateikimo šalies telefono numeris.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>HlwiskoImie</p>
    </td>
    <td>
    <p>Pateikimo asmens vardas.</p>
    </td>
    <td>
    <p>Nebaigta dara</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Peržiūrėkite sukurtą ataskaitą „Excel“ formatu.

    !["Intrastat" išsiuntimų ataskaita](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

1. Eikite į **Mokėtinos sumos** > **Pirkimo užsakymai** > **Visi pirkimo užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Dialogo lango **Sukurti pirkimo užsakymą** lauke **Tiekėjo paskyra** pasirinkite **DE-001**.
4. Lauke Vieta **pasirinkite** **1**.
5. Lauke Sandėlis **pasirinkite** **11**.
6. Pasirinkite **Gerai**.
7. Skirtuko **Antraštėje**,**pristatymo** "FastTab", patikrinkite, **·** **ar pristatymo būdo lauke nustatyta 10**,**o** lauke Pristatymo sąlygos nustatyta **kaip CIF.**
8. Skirtuko **Eilutės** „FastTab” **Pirkimo užsakymo eilutės** lauke **Prekės numeris** pasirinkite **D0003**. Tada, lauke **Kiekis** įveskite **6**.
9. Skirtuke **Eilutės informacija FastTab,** **užsienio prekybos skirtuke, patikrinkite,** **ar** operacijos kodas nustatytas kaip 11 **,** **transportavimo** lauke nustatyta 3 **,** **prekės** lauke nustatyta 100 200 30, **o kilmės šalies / regiono** laukas nustatytas **kaip DEU.** **·**
10. Veiksmų srities skirtuke **Pirkimas**, grupėje **Veiksmai**, pasirinkite **Patvirtinti**.
11. Veiksmų srities skirtuke **SF**, esančiame grupėje **Generuoti**, pasirinkite **SF**.
12. Veiksmų srityje pasirinkite Numatytasis **nuo**, tada lauke Numatytasis **eilučių kiekis pasirinkite** Užsakytas **kiekis**. Tada pasirinkite **Gerai**.
13. Tiekėjo SF **antraštės "** FastTab", SF **identifikavimo** skyriaus lauke **Numeris**, įveskite **00010**.
14. **SF datų** skyriaus SF **datos lauke** pasirinkite dabartinę datą. Ši data bus naudojama Intrastat perkėlime.
15. Lauke Gauti **dokumento datą pasirinkite** **2021-18-10 (2021** m. spalio 18 d.).
16. Norėdami registruoti sąskaitą faktūrą, veiksmų srityje pasirinkite **Registruoti**.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>„Intrastat” įsigijimų deklaracijos kūrimas

1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
2. Veiksmų srityje pasirinkite **Perduoti**.
3. Dialogo lange **„Intrastat” (perkėlimas)** nustatykite parinktį **Tiekėjo SF** į **Taip**.
4. Norėdami perkelti operacijas, pasirinkite **Gerai**, tada peržiūrėkite „Intrastat” žurnalą.

    ![Eilutė, kuri rodo pirkimo užsakymą Intrastat puslapyje](media/intrastat_pl_4.png)

5. Peržiūrėkite pirkimo užsakymo **informaciją** skirtuke Bendra.

    ![Išsami pirkimo užsakymo informacija Intrastat puslapio skirtuke Bendra](media/intrastat_pl_5.png)

6. Veiksmų srityje pasirinkite **Išvestis** > **Ataskaita**.
7. Intrastat ataskaitos **dialogo lango parametrų** **FastTab, skyriuje Data,** **lauke** Nuo **datos pasirinkite pirmą dabartinio mėnesio dieną.**
8. Skyriuje **Eksportavimo** **parinktys** nustatykite **Generuoti failą** į **Taip**. Tada lauke **Failo pavadinimas** įveskite reikiamą pavadinimą.
9. Parinktį **Generuoti ataskaitą** nustatykite kaip **Taip**. Tada lauke **Ataskaitos failo pavadinimas** įveskite reikiamą pavadinimą.
10. Lauke **Kryptis** pasirinkite **Įsigijimai**.
11. Failo formato **susiejimo skyriuje** patikrinkite, ar deklaracijos **tipo laukas** nustatytas kaip **Deklaracija**.
12. Į dokumentų **kūrimo miestą** įveskiteVz., Užd **·**.
13. Lauke Dokumento **sukūrimo data pasirinkite** **2021-19-10 (2021** m. spalio 19 d.).
14. Į lauką **Dokumento** nr. įveskite **11**.
15. Lauke Dokumento **versija** įveskite **22**.
16. Pasirinkite **Gerai** ir peržiūrėkite sugeneruotą XML formato ataskaitą. Toliau pateikiamoje lentelėje nurodomos pavyzdžio ataskaitos vertės.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Lauko pavadinimas</strong></p>
    </td>
    <td>
    <p><strong>Lauko aprašas</strong></p>
    </td>
    <td>
    <p><strong>Reikšmė</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informacija apie dokumentą</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja duomenys</p>
    </td>
    <td>
    <p>Data, kada buvo sukurtas dokumentas.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miej į sąsk.</p>
    </td>
    <td>
    <p>Miestas, kuriame dokumentas buvo sukurtas.</p>
    </td>
    <td>
    <p>Krokuva</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Bendras prekių skaičius.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Bendroji statistinė vertė.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Bendroji SF vertė.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Vieneto kodas.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Deklaracijos tipas.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Dokumento versija.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Skaičius</p>
    </td>
    <td>
    <p>Dokumento numeris.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Mieskaitė</p>
    </td>
    <td width="332">
    <p>Nuorodos mėnuo.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="332">
    <p>Nuorodos metai.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Tipo įvestis</p>
    </td>
    <td width="332">
    <p>Ataskaitos kryptis.</p>
    </td>
    <td>
    <p>P</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Nr. Išd.</p>
    </td>
    <td width="332">
    <p>Deklaracijos identifikatorius.</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informacija apie įmonę</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miej į sąsk.</p>
    </td>
    <td width="332">
    <p>Miestas, kuriame yra įmonė.</p>
    </td>
    <td>
    <p>Varšuva</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regonas</p>
    </td>
    <td width="332">
    <p>Įmonės Regon kodas.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nop</p>
    </td>
    <td>
    <p>Įmonės NIP kodas.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPoczt užd.</p>
    </td>
    <td>
    <p>Įmonės pašto indeksas.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Įsanika-skaitas</p>
    </td>
    <td>
    <p>Gatvė, kurioje yra įmonė.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Turiva</p>
    </td>
    <td>
    <p>Įmonės pavadinimas.</p>
    </td>
    <td>
    <p>"Contoso" pramogų sistemos Vokietija</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informacija apie tinkamas</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>ArbatoscStatystyczna</p>
    </td>
    <td>
    <p>Statistinė vertė.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>ArbatoscFaktury</p>
    </td>
    <td>
    <p>SF vertė.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Netto</p>
    </td>
    <td>
    <p>Grynoji masė.</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>AlcPochodcenia</p>
    </td>
    <td>
    <p>Kilmės šalies arba regiono kodas.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>Transportavimo kodo režimas.</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarade</p>
    </td>
    <td>
    <p>Prekės kodas.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Operacijos kodas.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Tamsusis demensas</p>
    </td>
    <td>
    <p>Pristatymo būdo sąlygos.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>AlcPochodzeniaWyshomeki</p>
    </td>
    <td>
    <p>Išsiuntimo / paskirties šalies arba regiono kodas.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Prekių aprašymas.</p>
    </td>
    <td>
    <p>Aparatūra</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>"PozId"</p>
    </td>
    <td>
    <p>Prekės numeris.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Kontaktinė informacija</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>El. laiškas</p>
    </td>
    <td>
    <p>Pateikimo asmens el. pašto adresas.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Itks</p>
    </td>
    <td>
    <p>Pateikimo aparato fakso numeris.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefonų telefonai</p>
    </td>
    <td>
    <p>Pateikimo šalies telefono numeris.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>HlwiskoImie</p>
    </td>
    <td>
    <p>Pateikimo asmens vardas.</p>
    </td>
    <td>
    <p>Nebaigta dara</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Peržiūrėkite sukurtą ataskaitą „Excel“ formatu.

    ![Intrastat gavimų ataskaita](media/intrastat_pl_6.png)

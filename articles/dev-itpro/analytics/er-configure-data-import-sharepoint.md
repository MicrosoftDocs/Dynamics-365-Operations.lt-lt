---
title: "Duomenų importavimo iš „SharePoint“ konfigūravimas"
description: "Šioje temoje paaiškinta, kaip importuoti duomenis iš „Microsoft SharePoint“."
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 4285db9c71208bce45d64933e692a25ef3f46b26
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2018

---
# <a name="configure-data-import-from-sharepoint"></a>Duomenų importavimo iš „SharePoint“ konfigūravimas

[!include[banner](../includes/banner.md)]

Norėdami importuoti duomenis iš gaunamo failo naudodami elektroninių ataskaitų (ER) sistemą, turite konfigūruoti ER formatą, kuris palaiko importavimą, ir paleisti tipo **Į paskirties vietą** modelio susiejimą, kuris naudoja tą formatą kaip duomenų šaltinį. Norėdami importuoti duomenis, turite pereiti į failą, kurį norite importuoti. Gaunamą failą vartotojas gali pasirinkti rankiniu būdu. Su nauja ER galimybe palaikyti iš „Microsoft SharePoint“ importuojamus duomenis, šį procesą galima konfigūruoti kaip naudojamą be priežiūros. Galite naudoti ER konfigūracijas norėdami duomenų importavimą atlikti iš failų, saugomų „Microsoft SharePoint“ aplankuose. Šioje temoje paaiškinta, kaip atlikti importavimą iš „SharePoint“ į „Microsoft Dynamics 365 for Finance and Operations“. Pavyzdžiuose tiekėjo operacijos naudojamos kaip verslo duomenys.

## <a name="prerequisites"></a>Būtinieji komponentai
Norint įvykdyti šios temos pavyzdžių užduotis, reikia toliau nurodytų prieigų.

- Prieiga prie „Finance and Operations“ naudojant vieną iš tolesnių vaidmenų.

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

- Prieiga prie „Microsoft SharePoint Server“ egzemplioriaus, kuris sukonfigūruotas naudoti su „Finance and Operations“
- 1099 mokėjimams naudojami ER formatas ir modelio konfigūracijos

### <a name="create-required-er-configurations"></a>Reikiamų ER konfigūracijų kūrimas
Leiskite užduočių vedlius **ER importavimo duomenys iš „Microsoft Excel“ failas**, kurie yra **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų(10677)** verslo proceso dalis. Šie užduočių vedliai parodys jums ER konfigūracijų kūrimo ir naudojimo procesą, norint interaktyviai importuoti tiekėjo operacijas iš išorinių „Microsoft Excel“ failų. Daugiau informacijos rasite [Gaunamų dokumentų analizė „Microsoft Excel“](parse-incoming-documents-excel.md). Galiausiai turėsite:

- ER konfigūracijos:

    - ER modelio konfigūracija, **1099 mokėjimų modelis**
    - ER formato konfigūracija, **Tiekėjų operacijų importavimo iš „Excel“ formatas**

[![ER konfigūracijos duomenims importuoti iš „SharePoint“](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)

- Gaunamo duomenų importavimo failo pavyzdys:

    - „Excel“ failas **1099import-data.xlsx**, kuriame yra tiekėjo operacijos, importuotinos į „Finance and Operations“

[![„Microsoft Excel“ failo, skirto importuoti iš „SharePoint“ pavyzdys](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)

> [!NOTE]
> Tiekėjo operacijų importavimo formatas pasirenkamas kaip numatytasis modelio susiejimas. Todėl jei vykdote modelio susiejimą **1099 mokėjimų modelis** ir to modelio susiejimo tipas yra **Į paskirties vietą**, modelio susiejimas vykdo šį formatą importuojant duomenis iš išorinių failų. Tada šie duomenys naudojami atnaujinant programos lenteles.

## <a name="configure-document-management-parameters"></a>Dokumentų valdymo parametrų konfigūravimas
1. Puslapyje **Dokumentų valdymo parametrai** sukonfigūruokite prieigą prie „SharePoint Server“ egzemplioriaus, kuris bus naudojamas įmonėje, prie kurios šiuo metu esate prisijungę. Šiame pavyzdyje įmonė yra USMF.
2. Patikrinkite ryšį su „SharePoint Server“ egzemplioriumi ir įsitikinkite, kad prieiga jums suteikta.

[![Dokumentų valdymo parametrai – „SharePoint“ serveris](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)

3. Atidarykite sukonfigūruotą „SharePoint“ svetainę ir kurkite šiuos aplankus, kur galima saugoti gaunamus failus:

    - Failų importavimo šaltinis (pagrindinis)
    - Failų importavimo šaltinis (alternatyvus)

[![Dokumentų valdymo parametrai – „SharePoint“ serveris](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

[![Dokumentų valdymo parametrai – „SharePoint“ serveris](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)

4. „Finance and Operations“ puslapyje **Dokumentų tipai** sukurkite toliau nurodytus dokumentų tipus, kurie bus naudojami norint pasiekti ką tik sukurtus „SharePoint“ aplankus.

    - SP pagrindinis
    - SP alternatyvus

5. Sukurtiems dokumentų tipams lauke **Grupė** įveskite **Failas**, o lauke **Vieta** įveskite **„SharePoint“**. Tuomet įveskite „SharePoint“ aplanko adresą:

    - Dokumento tipui **SP pagrindinis**: Failų importavimo šaltinis (pagrindinis)
    - Dokumento tipui **SP alternatyvus**: Failų importavimo šaltinis (alternatyvus)

[![„SharePoint“ parametras – naujas dokumento tipas](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>ER formato ER šaltinių konfigūravimas
1. Spustelėkite **Organizacijos administravimas** > **Elektroninės ataskaitos** > **Elektroninių ataskaitų šaltinis**.
2. Puslapyje **Elektroninių ataskaitų šaltinis** konfigūruokite duomenų importavimo šaltinio failus naudodami sukonfigūruotą ER formatą.
3. Nurodykite failo pavadinimo šabloną, kad būtų importuoti tik failai su .xlsx plėtiniu. Failo pavadinimo šablonas yra pasirinktinis ir naudojamas tik tada, jei buvo nurodytas. Galite nurodyti tik po vieną kiekvieno ER formato šabloną.
4. Pasirinkite abu „SharePoint“ aplankus, kuriuos sukūrėte anksčiau.

[![ER failų šaltinio parametras](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
>ER *šaltinis* nurodytas kiekvienai programos įmonei atskirai. Tačiau, ER *konfigūracijos* yra bendrai naudojamos keliose įmonėse.

> [!NOTE]
> Panaikinus ER formato ER šaltinio parametrą, taip pat panaikinamos visų prijungtų failų būsenos (žr. toliau).

## <a name="review-the-files-states-for-the-er-format"></a>ER formato failų būsenų peržiūra
1. Puslapyje **Elektroninių ataskaitų šaltinis** pasirinkite **Šaltinių failų būsenos** norėdami peržiūrėti dabartinio ER formato sukonfigūruotų failų šaltinių turinį.
2. Skyriuje **Failai** peržiūrėkite failų sąrašą. Šiame sąraše pristatomi šie elementai:

    - Šaltinio failus, kurie taikomi pagal failo pavadinimo šabloną (jei failo pavadinimo šablonas nurodytas) ir kurie parengti duomenims importuoti. Šių failų skyrius **Importavimo formato šaltinių žurnalas** yra tuščias.
    - Anksčiau importuoti failai. Kiekvienam iš šių failų skyriuje **Importavimo formato šaltinių žurnalas** galite peržiūrėti šio failo importavimo retrospektyvą.

Be to, galite atidaryti puslapį **Šaltinių failų būsenos** pasirinkę **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Šaltinių failų būsenos**. Šiuo atveju puslapyje pateikiama informacija apie visų ER formatų failų šaltinius, kuriems failų šaltiniai buvo sukonfigūruoti įmonėje, prie kurios šiuo metu esate prisijungę.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Importuoti duomenis iš „Excel“ failų, esančių „SharePoint“ aplanke
1. Programoje „SharePoint“ įkelkite „Microsoft Excel“ failą **1099import-data.xlsx**, kuriame yra tiekėjo operacijos, į anksčiau sukurtą „SharePoint“ aplanką **Failų importavimo šaltinis (pagrindinis)**.

[![„SharePoint“ turinys – „Microsoft Excel“ failas, skirtas importuoti](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Sprendimo „Finance and Operations“ puslapyje **Šaltinių failų būsenos** pasirinkę **Atnaujinti** atnaujinkite puslapį. Atkreipkite dėmesį, kad „Excel“ failo, kuris buvo įkeltas į „SharePoint“, šioje formoje būsena buvo **Parengta**. Šiuo metu palaikomos šios būsenos:

    - **Parengta** – automatiškai priskiriama kiekvienam naujam „SharePoint“ aplankui. Ši būsena reiškia, kad failas parengtas importuoti.
    - **Importuojama** – priskiriama automatiškai pagal ER ataskaitą, kai failas bus užrakintas dėl importavimo proceso, kad jo nebūtų galima naudoti kituose procesuose (jei vienu metu veikia keletas jų).
    - **Importuota** – priskiriama automatiškai pagal ER ataskaitą, kai failo importavimas sėkmingai baigtas. Ši būsena reiškia, kad importuotas failas panaikintas iš sukonfigūruotų failų šaltinio („SharePoint“ aplanko).
    - **Nepavyko** – priskiriama automatiškai pagal ER ataskaitą, kai failo importavimas baigtas su klaidomis arba išimtimis.
    - **Sulaikyta** – vartotojo priskiriama rankiniu būdu šioje formoje. Ši būsena reiškia, kad failas kol kas nebus importuojamas. Šią būseną galima naudoti norint atidėti kai kurių failų importavimą.

[![Pasirinktų šaltinių ER failų būsenų puslapis](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Duomenų importavimas iš „SharePoint“ failų
1. Atidarykite ER konfigūracijos medį, pasirinkite **1099 mokėjimų modelis** ir išplėskite ER modelio komponentų sąrašą.
2. Pasirinkę modelio susiejimo modelio pavadinimą atidarykite pasirinkto ER modelio konfigūracijos modelių susiejimo sąrašą.

[![Pasirinktų šaltinių ER failų būsenų puslapis](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Pasirinkę **Vykdyti** paleisite pasirinkto modelio susiejimą. Todėl, kad sukonfigūravote ER formato failų šaltinius, galite pagal poreikį keisti parametrą į parinktį **Failo šaltinis**. Jei paliksite šį pasirinkties parametrą, .xslx failai bus importuojami iš sukonfigūruotų šaltinių (šiame pavyzdyje – „SharePoint“ aplankų).

    Šiame pavyzdyje importuojate tik vieną failą. Tačiau, jei yra keli failai, jie pasirinkti importuoti ta tvarka, kuria jie buvo įtraukti į „SharePoint“ aplanką. Kaskart vykdant ER formatą, importuojamas vienas pasirinktas failas.

[![ER modelio susiejimo vykdymas](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Modelio susiejimą galima vykdyti paketiniu režimu be priežiūros. Tokiu atveju, kiekvieną kartą, kai paketas vykdomas šiuo ER formatu, iš sukonfigūruotų failų šaltinių importuojamas vienas failas. Naudokite šį kodą norėdami įdiegti šį paketo paleidimą.

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    Kai failas sėkmingai importuotas iš „SharePoint“ aplanko, jis panaikinamas iš šio katalogo.

5. Įveskite kvito ID, pvz., **V-00001**, tada pasirinkite **Gerai**.

[![ER modelio susiejimo vykdymas](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Puslapyje **Šaltinių failų būsenos** pasirinkę **Atnaujinti** atnaujinsite puslapį.

[![Pasirinktų šaltinių ER failų būsenų puslapis](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Skyriuje **Failai** peržiūrėkite failų sąrašą. Skyriuje **Importavimo formato šaltinių žurnalas** pateikiama „Excel“ failo importavimo retrospektyva. Kadangi šis failas buvo sėkmingai importuotas, „SharePoint“ aplanke jis pažymėtas kaip **Panaikintas**.
8. Peržiūrėkite „SharePoint“ aplanką **Failų importavimo šaltinis (pagrindinis)**. Tie „Excel“ failai, kurie buvo sėkmingai importuoti, yra panaikinti iš šio aplanko.
9. Sprendime „Finance and Operations“ pasirinkite **Mokėtinos sumos** \> **Periodinės užduotys** \> **Mokestis 1099** \> **1099 tiekėjo sudengimas**.
10. Laukuose **Pradžios data** ir **Pabaigos data** įveskite tinkamas vertes. Tada pasirinkite **Rankiniu būdu atliekamos 1099 operacijos**.

    Tiekėjo operacijos, kurios buvo importuotos iš „SharePoint“ platformoje esančių „Excel“ failų kvitui **V-00001**, yra pateikiamos puslapyje.

[![1099 tiekėjo operacijų puslapis](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>„Excel“ failo paruošimas importuoti
1. Atidarykite „Excel“ failą, kurį naudojote anksčiau. Į 3 eilutės 1 stulpelį įtraukite tiekėjo kodą, kurio nėra programoje. Įtraukite papildomą klaidingą tiekėjo informaciją į eilutę.

[![„Microsoft Excel“ failo, skirto importuoti iš „SharePoint“ pavyzdys](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Įkelti atnaujintą „Excel“ failą, kuriame yra tiekėjų operacijos, į „SharePoint“ aplanką **Failų importavimo šaltinis (pagrindinis)**.
3. Sprendime „Finance and Operations“ atidarykite ER konfigūracijos medį, pasirinkite **1099 mokėjimų modelis** ir išplėskite ER modelio komponentų sąrašą.
4. Pasirinkite modelio susiejimo pavadinimą norėdami atnaujinti modelio susiejimą taip, kad duomenų importavimo proceso metu neteisingas tiekėjo kodas būtų laikomas klaida.
5. Pasirinkite **Dizaino įrankis**.
6. Skirtuke **Tikrinimai** turite pakeisti tolesnio tikrinimo veiksmą tos tikrinimo taisyklės, kuri buvo sukonfigūruota norint įvertinti, ar importuota tiekėjo sąskaita yra programoje. Atnaujinkite lauko **Tolesnio tikrinimo veiksmas** vertę į **Sustabdyti vykdymą**, įrašykite pakeitimus ir uždarykite puslapį.

[![ER modelio susiejimo dizaino įrankio puslapis](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Įrašykite pakeitimus ir uždarykite ER modelio susiejimo dizaino įrankį.
8. Pasirinkę **Vykdyti** paleisite modifikuotą ER modelio susiejimą.
9. Įveskite kvito ID, pvz., **V-00002**, tada pasirinkite **Gerai**.

    Atkreipkite dėmesį, kad informaciniame žurnale yra pranešimas, informuojantis, kad „SharePoint“ aplanko faile yra netinkama tiekėjo sąskaita ir importuoti negalima.

[![ER modelio susiejimo vykdymas](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Puslapyje **Šaltinių failų būsenos** pasirinkite **Atnaujinti**, tuomet skyriuje **Failai** peržiūrėkite failų sąrašą.

[![Pasirinktų šaltinių ER failų būsenų puslapis](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

Skyriuje **Importavimo formato šaltinių žurnalas** nurodyta, kad importavimo procesas nepavyko ir kad failas vis dar yra „SharePoint“ aplanke (žymės langelis **Panaikintas** nėra pažymėtas). Jei ištaisysite šį failą „SharePoint“ įtraukę tinkamą tiekėjo kodą, tada pakeisite failo būseną iš **Nepavyko** į **Parengta** skyriuje **Importavimo formato šaltinių žurnalas**, vėl galėsite importuoti failą.

11. Peržiūrėkite „SharePoint“ aplanką **Failų importavimo šaltinis (pagrindinis)**. Atkreipkite dėmesį, kad „Excel“ failas, kuris nebuvo importuotas, vis dar yra šiame aplanke.
12. Sprendime „Finance and Operations“ pasirinkite **Mokėtinos sumos** \> **Periodinės užduotys** \> **1099 mokestis** \> **1099 tiekėjo sudengimas**, laukuose **Pradžios data** ir **Pabaigos data** įveskite atitinkamas vertes, tada pasirinkite **Rankiniu būdu atliekamos 1099 operacijos**.

    Galimos tik V-00001 kvito operacijos. Jokios kvito V-00002 operacijos nėra galimos, nors paskutinės importuotos operacijos klaida rasta „Excel“ faile.


---
title: Duomenų importavimo iš „SharePoint“ konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip importuoti duomenis iš "Microsoft"SharePoint.
author: kfend
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 11208267de0cc35db55c64ccf2de224df854404d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277793"
---
# <a name="configure-data-import-from-sharepoint"></a>Duomenų importavimo iš „SharePoint“ konfigūravimas

[!include[banner](../includes/banner.md)]

Norėdami importuoti duomenis iš gaunamo failo naudodami elektroninių ataskaitų (ER) sistemą, turite konfigūruoti ER formatą, kuris palaiko importavimą, ir paleisti tipo **Į paskirties vietą** modelio susiejimą, kuris naudoja tą formatą kaip duomenų šaltinį. Norėdami importuoti duomenis, turite pereiti į failą, kurį norite importuoti. Gaunamą failą vartotojas gali pasirinkti rankiniu būdu. Su nauja ER galimybe palaikyti iš „Microsoft SharePoint“ importuojamus duomenis, šį procesą galima konfigūruoti kaip naudojamą be priežiūros. Galite naudoti ER konfigūracijas norėdami duomenų importavimą atlikti iš failų, saugomų „Microsoft SharePoint“ aplankuose. Šiame straipsnyje paaiškinama, kaip baigti importavimą iš SharePoint. Pavyzdžiuose tiekėjo operacijos naudojamos kaip verslo duomenys.

## <a name="prerequisites"></a>Būtinieji komponentai
Norėdami užbaigti pavyzdžius šiame straipsnyje, turite turėti šią prieigą:

- Prieiga naudojant vieną iš tolesnių vaidmenų.

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

- Prieiga prie „Microsoft SharePoint Server“ egzemplioriaus, kuris sukonfigūruotas naudoti su programa.
- 1099 mokėjimams naudojami ER formatas ir modelio konfigūracijos.

### <a name="create-required-er-configurations"></a>Reikiamų ER konfigūracijų kūrimas
Leiskite užduočių vedlius **ER importavimo duomenys iš „Microsoft Excel“ failas**, kurie yra **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų(10677)** verslo proceso dalis. Šie užduočių vedliai parodys jums ER konfigūracijų kūrimo ir naudojimo procesą, norint interaktyviai importuoti tiekėjo operacijas iš „Microsoft Excel“ failų. Daugiau informacijos žr. [„Excel“ formatu gaunamų dokumentų analizė](parse-incoming-documents-excel.md). Atlikus užduočių vadovo veiksmus, bus nustatytos toliau pateiktos parinktys.

#### <a name="er-configurations"></a>ER konfigūracijos

- ER modelio konfigūracija, **1099 mokėjimų modelis**
- ER formato konfigūracija, **Tiekėjų operacijų importavimo iš „Excel“ formatas**

![ER konfigūracijos duomenims importuoti iš „SharePoint“.](./media/GERImportFromSharePoint-01-Configurations.PNG)

#### <a name="sample-of-the-incoming-file-for-data-import"></a>Gaunamo duomenų importavimo failo pavyzdys

- „Excel“ failas **1099import-data.xlsx**, kuriame yra tiekėjo operacijos, kurias reikia importuoti.

![„Excel“ failo, skirto importuoti iš „SharePoint“, pavyzdys.](./media/GERImportFromSharePoint-02-Excel.PNG)
    
> [!NOTE]
> Tiekėjo operacijų importavimo formatas pasirenkamas kaip numatytasis modelio susiejimas. Todėl jei vykdote modelio susiejimą **1099 mokėjimų modelis** ir to modelio susiejimo tipas yra **Į paskirties vietą**, modelio susiejimas vykdo šį formatą importuojant duomenis iš išorinių failų. Tada šie duomenys naudojami atnaujinant programos lenteles.

## <a name="configure-access-to-sharepoint-for-file-storage"></a>Prieigos prie „SharePoint“ konfigūravimas failų saugyklai
Norėdami saugoti elektroninių ataskaitų failus „SharePoint“ vietoje, turite sukonfigūruoti prieigą prie „SharePoint Server“ egzemplioriaus, kuris bus naudojamas dabartinės įmonės. Šiame pavyzdyje įmonė yra USMF. Instrukcijų ieškokite [„SharePoint“ saugyklos konfigūravimas](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).

1. Atlikite veiksmus, nurodytus temoje [„SharePoint“ saugyklos konfigūravimas](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).
2. Atidarykite sukonfigūruotą „SharePoint“ svetainę.
3. Sukurkite šiuos aplankus, kur gali būti saugomi gaunamų elektroninių ataskaitų failai:

     - Failų importavimo šaltinis (pagrindinis) (ekrano kopijoje apačioje rodomas pavyzdys)
     - Failų importavimo šaltinis (alternatyvus)

    ![Failų importavimo šaltinis (pagrindinis).](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

4. (Pasirinktinai) sukurkite šiuos aplankus, kur gali būti saugomi failai atlikus importavimą. 

    - Failų archyvo aplankas – šis aplankas skirtas sėkmingai importuotiems failams.
    - Failų įspėjimo aplankas – šis aplankas skirtas failams, kurie buvo importuoti su perspėjimu.
    - Failų klaidų aplankas – šis aplankas skirtas failams, kurių nepavyko importuoti.

4. Eikite į **Organizacijos administravimas > Dokumentų valdymas > Dokumentų tipai**.
5. Sukurkite toliau nurodytus dokumentų tipus, kurie bus naudojami pasiekti „SharePoint“ aplankus, kuriuos ką tik sukūrėte. Instrukcijų ieškokite temoje [Dokumentų tipų konfigūravimas](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types).

|Dokumento tipas       | Grupuoti              | Buvimo vieta      | „SharePoint“ aplankas      |
|--------------------|--------------------|---------------|------------------------|
|SP pagrindinis             |Failas                |„SharePoint“     |Failų importavimo šaltinis (pagrindinis)|
|SP alternatyvus             |Failas                |„SharePoint“     |Failų importavimo šaltinis (alternatyvus)|
|SP archyvas             |Failas                |„SharePoint“     |Failų archyvo aplankas|
|SP įspėjimas             |Failas                |„SharePoint“     |Failų įspėjimų aplankas|
|SP klaida             |Failas                |„SharePoint“     |Failų klaidų aplankas|

![„SharePoint“ parametras – naujas dokumento tipas.](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>ER formato ER šaltinių konfigūravimas
1. Spustelėkite **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Elektroninių ataskaitų šaltinis**.
2. Puslapyje **Elektroninių ataskaitų šaltinis** konfigūruokite duomenų importavimo šaltinio failus naudodami sukonfigūruotą ER formatą.
3. Nurodykite failo pavadinimo šabloną, kad būtų importuoti tik failai su .xlsx plėtiniu. Failo pavadinimo šablonas yra pasirinktinis ir naudojamas tik tada, jei buvo nurodytas. Galite nurodyti tik po vieną kiekvieno ER formato šabloną.
4. Pakeiskite **Rūšiuoti failus prieš importuojant** į **Nerūšiuoti**, jei yra daug importuotinų failų, o importavimo tvarka nėra svarbi
5. Pasirinkite visus „SharePoint“ aplankus, kuriuos sukūrėte anksčiau.

    [![ER failų šaltinio parametras.](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
> - ER *šaltinis* nurodytas kiekvienai programos įmonei atskirai. Tačiau, ER *konfigūracijos* yra bendrai naudojamos keliose įmonėse.
> - Panaikinus ER formato ER šaltinio parametrą, patvirtinus taip pat panaikinamos visų prijungtų failų būsenos (žr. toliau).

## <a name="review-the-files-states-for-the-er-format"></a>ER formato failų būsenų peržiūra
1. Puslapyje **Elektroninių ataskaitų šaltinis** pasirinkite **Šaltinių failų būsenos** norėdami peržiūrėti dabartinio ER formato sukonfigūruotų failų šaltinių turinį.
2. Skyriuje **Failai** peržiūrėkite failų sąrašą. Šiame sąraše pristatomi šie elementai:

    - Šaltinio failus, kurie taikomi pagal failo pavadinimo šabloną (jei failo pavadinimo šablonas nurodytas) ir kurie parengti duomenims importuoti. Šių failų skyrius **Importavimo formato šaltinių žurnalas** yra tuščias.
    - Anksčiau importuoti failai. Kiekvienam iš šių failų skyriuje **Importavimo formato šaltinių žurnalas** galite peržiūrėti šio failo importavimo retrospektyvą.

Be to, galite atidaryti puslapį **Šaltinių failų būsenos** pasirinkę **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Šaltinių failų būsenos**. Šiuo atveju puslapyje pateikiama informacija apie visų ER formatų failų šaltinius, kuriems failų šaltiniai buvo sukonfigūruoti įmonėje, prie kurios šiuo metu esate prisijungę.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Importuoti duomenis iš „Excel“ failų, esančių „SharePoint“ aplanke
1. Programoje „SharePoint“ įkelkite „Microsoft Excel“ failą **1099import-data.xlsx**, kuriame yra tiekėjo operacijos, į anksčiau sukurtą „SharePoint“ aplanką **Failų importavimo šaltinis (pagrindinis)**.

    [![„SharePoint“ turinys – „Microsoft Excel“ failas, skirtas importuoti.](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Puslapyje **Šaltinių failų būsenos** pasirinkę **Atnaujinti** atnaujinsite puslapį. „Excel“ failo, kuris buvo įkeltas į „SharePoint“, šiame puslapyje būsena buvo **Parengta**. Šiuo metu palaikomos šios būsenos:

    - **Parengta** – automatiškai priskiriama kiekvienam naujam „SharePoint“ aplankui. Ši būsena reiškia, kad failas parengtas importuoti.
    - **Importuojama** – priskiriama automatiškai pagal ER ataskaitą, kai failas bus užrakintas dėl importavimo proceso, kad jo nebūtų galima naudoti kituose procesuose (jei vienu metu veikia keletas jų).
    - **Importuota** – priskiriama automatiškai pagal ER ataskaitą, kai failo importavimas sėkmingai baigtas. Ši būsena reiškia, kad importuotas failas panaikintas iš sukonfigūruotų failų šaltinio („SharePoint“ aplanko).
    - **Nepavyko** – priskiriama automatiškai pagal ER ataskaitą, kai failo importavimas baigtas su klaidomis arba išimtimis.
    - **Sulaikyta** – vartotojo priskiriama rankiniu būdu šiame puslapyje. Ši būsena reiškia, kad failas kol kas nebus importuojamas. Šią būseną galima naudoti norint atidėti kai kurių failų importavimą.

    [![Atnaujintas pasirinktų šaltinių ER failų būsenų puslapis.](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Duomenų importavimas iš „SharePoint“ failų
1. Atidarykite ER konfigūracijos medį, pasirinkite **1099 mokėjimų modelis** ir išplėskite ER modelio komponentų sąrašą.
2. Pasirinkę modelio susiejimo modelio pavadinimą atidarykite pasirinkto ER modelio konfigūracijos modelių susiejimo sąrašą.

    [![Puslapis Konfigūracija.](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Pasirinkę **Vykdyti** paleisite pasirinkto modelio susiejimą. Todėl, kad sukonfigūravote ER formato failų šaltinius, galite pagal poreikį keisti parametrą į parinktį **Failo šaltinis**. Jei paliksite šį pasirinkties parametrą, .xslx failai bus importuojami iš sukonfigūruotų šaltinių (šiame pavyzdyje – „SharePoint“ aplankų).

    Šiame pavyzdyje importuojate tik vieną failą. Tačiau, jei yra keli failai, jie pasirinkti importuoti ta tvarka, kuria jie buvo įtraukti į „SharePoint“ aplanką. Kaskart vykdant ER formatą, importuojamas vienas pasirinktas failas.

    [![Importavimas iš „SharePoint“ ir ER modelio susiejimo vykdymas.](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Modelio susiejimą galima vykdyti paketiniu režimu [be priežiūros](#limitations). Tokiu atveju, kiekvieną kartą, kai paketas vykdomas šiuo ER formatu, iš sukonfigūruotų failų šaltinių importuojamas vienas failas.

    Kai failas sėkmingai importuotas iš „SharePoint“ aplanko, jis panaikinamas iš to katalogo ir perkeliamas į sėkmingai importuotų failų aplanką arba į aplanką, skirtą importuotiems failams su įspėjimais. Kitu atveju, jis perkeliamas į aplanką nepavykusius failus arba, jei nenustatytas nepavykusių failų aplankas, lieka šiame aplanke. 

5. Įveskite kvito ID, pvz., **V-00001**, tada pasirinkite **Gerai**.

    [![ER modelio susiejimo vykdymas.](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Puslapyje **Šaltinių failų būsenos** pasirinkę **Atnaujinti** atnaujinsite puslapį.

    [![Šaltinių puslapio ER failų būsenos.](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Skyriuje **Failai** peržiūrėkite failų sąrašą. Skyriuje **Importavimo formato šaltinių žurnalas** pateikiama „Excel“ failo importavimo retrospektyva. Kadangi šis failas buvo sėkmingai importuotas, „SharePoint“ aplanke jis pažymėtas kaip **Panaikintas**.
8. Peržiūrėkite „SharePoint“ aplanką **Failų importavimo šaltinis (pagrindinis)**. Tie „Excel“ failai, kurie buvo sėkmingai importuoti, yra panaikinti iš šio aplanko.
9. Pasirinkite **Mokėtinos sumos** \> **Periodinės užduotys** \> **Mokesčiai 1099** \> **1099 tiekėjo sudengimas**.
10. Laukuose **Pradžios data** ir **Pabaigos data** įveskite tinkamas vertes. Tada pasirinkite **Rankiniu būdu atliekamos 1099 operacijos**.

    Tiekėjo operacijos, kurios buvo importuotos iš „SharePoint“ platformoje esančių „Excel“ failų kvitui **V-00001**, yra pateikiamos puslapyje.

    [![1099 tiekėjo operacijų puslapis.](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>„Excel“ failo paruošimas importuoti
1. Atidarykite „Excel“ failą, kurį naudojote anksčiau. Į 3 eilutės 1 stulpelį įtraukite tiekėjo kodą, kurio nėra programoje. Įtraukite papildomą klaidingą tiekėjo informaciją į eilutę.

    [![„Microsoft Excel” failo, skirto importuoti iš „SharePoint”, pavyzdys.](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Įkelti atnaujintą „Excel“ failą, kuriame yra tiekėjų operacijos, į „SharePoint“ aplanką **Failų importavimo šaltinis (pagrindinis)**.
3. Atidarykite ER konfigūracijos medį, pasirinkite **1099 mokėjimų modelis** ir išplėskite ER modelio komponentų sąrašą.
4. Pasirinkite modelio susiejimo pavadinimą norėdami atnaujinti modelio susiejimą taip, kad duomenų importavimo proceso metu neteisingas tiekėjo kodas būtų laikomas klaida.
5. Pasirinkite **Dizaino įrankis**.
6. Skirtuke **Tikrinimai** turite pakeisti tolesnio tikrinimo veiksmą tos tikrinimo taisyklės, kuri buvo sukonfigūruota norint įvertinti, ar importuota tiekėjo sąskaita yra programoje. Atnaujinkite lauko **Tolesnio tikrinimo veiksmas** vertę į **Sustabdyti vykdymą**, įrašykite pakeitimus ir uždarykite puslapį.

    [![ER modelio susiejimo dizaino įrankio puslapis.](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Įrašykite pakeitimus ir uždarykite ER modelio susiejimo dizaino įrankį.
8. Pasirinkę **Vykdyti** paleisite modifikuotą ER modelio susiejimą.
9. Įveskite kvito ID, pvz., **V-00002**, tada pasirinkite **Gerai**.

    Informaciniame žurnale yra pranešimas, informuojantis, kad „SharePoint“ aplanko faile yra netinkama tiekėjo paskyra ir importuoti negalima.

    [![Baigtas ER modelio susiejimo vykdymas.](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Puslapyje **Šaltinių failų būsenos** pasirinkite **Atnaujinti**, tuomet skyriuje **Failai** peržiūrėkite failų sąrašą.

    [![Pasirinktų šaltinių ER failų būsenų puslapis.](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

   Skyriuje **Importavimo formato šaltinių žurnalas** nurodyta, kad importavimo procesas nepavyko ir kad failas yra failų klaidų „SharePoint“ aplanke (žymės langelis **Panaikintas** nėra pažymėtas). Jei pataisote šį failą, esantį „SharePoint“, įtraukdami tinkamą tiekėjo kodą ir perkeliate jį į failų importavimo šaltinio (pagrindinį) „SharePoint“ aplanką, galite importuoti failą dar kartą.

11. Pasirinkite **Mokėtinos sumos** \> **Periodinės užduotys** \> **1099 mokestis** \> **1099 tiekėjo sudengimas**, laukuose **Pradžios data** ir **Pabaigos data** įveskite atitinkamas vertes, tada pasirinkite **Rankiniu būdu atliekamos 1099 operacijos**.

    Galimos tik V-00001 kvito operacijos. Jokios kvito V-00002 operacijos nėra galimos, nors paskutinės importuotos operacijos klaida rasta „Excel“ faile.

## <a name=""></a><a name="limitations">Apribojimai</a>

Naudojant "Dynamics 365 Finance" versijas prieš 10.0.25 versiją, ER sistemos vartotojo sąsaja (UI) nesiūlya galimybės inicijuoti naujos paketinės užduoties, kuri paleis duomenų importavimo modelio susiejimą be paslaugų režimu. Todėl jūs turite sukurti naują logiką, kad sukonfigūruotą ER modelio konvertavimą būtų galima iškviesti iš programos vartotojo sąsajos, kad būtų galima importuoti duomenis iš gaunamų failų. Norint sukurti šią logiką, reikia tam tikrų inžinerijos darbų. 

Norėdami gauti daugiau informacijos apie atitinkamą ER API, žr. kodą, [...](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import)[norėdami vykdyti duomenų importavimo skyriaus formato konvertavimą ER sistemos API pakeitimų programoje atnaujinimas 7.3](er-apis-app73.md). Peržiūrėkite modelio `Application Suite` klasės `BankImport_RU` kodą, kad pamatytumėte, kaip galima įdiegti pasirinktinę logiką. Klasė `BankImport_RU` išplečia klasę `RunBaseBatch`. Visų pirma peržiūrėkite metodą `runER()`, pagal kurį `ERIModelMappingDestinationRun` objektas kuriamas kaip ER modelio susiejimo vykdyklė.

Naudojant 10.0.25 arba vėlesnę finansų versiją ER sistemos UI suteikia galimybę inicijuoti naują paketinę užduotį, kuri paleis duomenų importavimo modelio susiejimą be siūlyto režimu. Daugiau informacijos apie šį procesą ieškokite Importuokite duomenis [paketiniu režimu iš rankiniu būdu pasirinktų failų](er-configure-data-import-batch.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[„Application Update 7.3“ ER sistemos API pakeitimai](er-apis-app73.md)

[„Application Update 10.0.23“ ER sistemos API pakeitimai](er-apis-app10-0-23.md)

[„Application Update 10.0.25“ ER sistemos API pakeitimai](er-apis-app10-0-25.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

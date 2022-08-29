---
title: Įrankio Elektroninės ataskaitos (ER) konfigūravimas duomenims perkelti į „Power BI“
description: Šiame straipsnyje paaiškinama, kaip galite naudoti savo elektroninių ataskaitų (ER) konfigūraciją, kad sutvarkytumėte duomenų perdavimą iš egzemplioriaus į Power BI tarnybas.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: be0e79bb767a8bd2db4c02dc2b73bfbc5cb95675
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281729"
---
# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a>Įrankio Elektroninės ataskaitos (ER) konfigūravimas duomenims perkelti į „Power BI“

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip galite naudoti savo elektroninių ataskaitų (ER) konfigūraciją, kad sutvarkytumėte duomenų perdavimą iš egzemplioriaus į Power BI tarnybas. Kaip pavyzdį šiame straipsnyje kaip verslo duomenys, kuriuos reikia perkelti, naudojamos Intrastat operacijos. „Power BI“ schemos vizualizacijoje naudojami šie „Intrastat“ operacijų duomenys, kad „Power BI“ ataskaitoje būtų pateiktas įmonės importavimo / eksportavimo veiklų analizės rodinys.

## <a name="overview"></a>Peržiūra

„Microsoft Power BI“ yra programinės įrangos paslaugų, programų ir jungčių, kurios kartu naudojamos norint išorinius duomenų šaltinius paversti nuosekliomis, vizualiai įtraukiančiomis ir interaktyvių įžvalgomis, rinkinys. Elektroninės ataskaitos (ER) vartotojams suteikia galimybę lengvai konfigūruoti duomenų šaltinius ir išdėstyti duomenų perkėlimą iš programos į „Power BI“. Duomenys perkeliami kaip failai „OpenXML“ darbalapio („Microsoft Excel“ darbaknygės failų) formatu. Perkelti failai saugomi „Microsoft SharePoint Server“, kuris šiuo tikslu sukonfigūruotas. Saugomi failai naudojami „Power BI“ norint kurti ataskaitas su vizualizacijomis (lentelėmis, diagramomis, schemomis ir t.t.). „Power BI“ ataskaitas bendrai naudoja „Power BI“ vartotojai, ir jas galima pasiekti „Power BI“ ataskaitų srityse bei programos puslapiuose. Šiame straipsnyje paaiškinamos šios užduotys:

- Sukonfigūruokite Microsoft Dynamics 365 finansus.
- ER formato konfigūracijos parengimas, norint gauti duomenis iš „Finance“ programos.
- ER aplinkos konfigūravimas duomenims į „Power BI“ perkelti.
- Perkeltų duomenų naudojimas „Power BI“ ataskaitai kurti.
- „Power BI“ ataskaitos prieigos programoje „Finance“ kūrimas.

## <a name="prerequisites"></a>Būtinieji komponentai
Norėdami užbaigti pavyzdį šiame straipsnyje, turite turėti šią prieigą:

- Prieiga naudojant vieną iš tolesnių vaidmenų.

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

- Prieiga prie „SharePoint Server“, kuris sukonfigūruotas naudoti su programa
- Prieiga prie „Power BI“ sistemos

## <a name="configure-document-management-parameters"></a>Dokumentų valdymo parametrų konfigūravimas
1. Puslapyje **Dokumentų valdymo parametrai** sukonfigūruokite prieigą prie „SharePoint Server“, kuris bus naudojamas įmonėje, prie kurios esate prisijungę (šiame pavyzdyje – įmonėje DEMF).
2. Patikrinkite ryšį su „SharePoint Server“ ir įsitikinkite, kad prieiga jums suteikta.

    [![Puslapis Dokumentų valdymo parametrai.](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)

3. Atidarykite sukonfigūruotą „SharePoint“ svetainę. Sukurkite naują aplanką, kuriame ER išsaugos „Excel“ failus su verslo duomenimis, kurie „Power BI“ ataskaitose reikalingi kaip „Power BI“ duomenų rinkinių šaltinis.
4. Puslapyje **Dokumentų tipai** sukurkite naują dokumento tipą, kuris bus naudojamas norint pasiekti ką tik sukurtą „SharePoint“ aplanką. Lauke **Grupė** įveskite **Failas**, lauke **Vieta** įveskite **SharePoint** ir tada įveskite „SharePoint“ aplanko adresą.

    [![Puslapis Dokumentų tipai.](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>ER parametrų konfigūravimas
1. Darbo srityje **Elektroninės ataskaitos** spustelėkite saitą **Elektroninių ataskaitų parametrai**.
2. Visuose skirtuko **Priedai** laukuose pasirinkite dokumentų tipą **Failas**.
3. Darbo srityje **Elektroninės ataskaitos** nustatykite reikiamą teikėją kaip aktyvų, spustelėdami **Nustatyti kaip aktyvų**. Norėdami gauti daugiau informacijos, paleiskite užduočių vedlį **ER: paslaugų teikėjo pasirinkimas**.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>ER duomenų modelio kaip duomenų šaltinio naudojimas
ER duomenų modelis turi būti nustatytas kaip verslo duomenų, kurie bus naudojami „Power BI“ ataskaitose, šaltinis. Šis duomenų modelis įkeliamas iš ER konfigūracijų saugyklos. Daugiau informacijos žr. puslapyje [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](download-electronic-reporting-configuration-lcs.md) arba paleiskite užduočių vedlį **ER: konfigūracijos importavimas iš „Lifecycle Services‟**. Pasirinkite **Intrastat** kaip duomenų modelį, kuris bus įkeltas iš pasirinktos ER konfigūracijų saugyklos. (Šiame pavyzdyje naudojama 1 modelio versija.) **Intrastat** ER modelio konfigūraciją galite pasiekti puslapyje **Konfigūracijos**.

[![„Intrastat ER" modelio kofigūracija konfigūracijos puslapyje.](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>ER formato konfigūracijos kūrimas
Turite sukurti naują ER formato konfigūraciją, kuri **Intrastat** duomenų modelį naudoja kaip verslo duomenų šaltinį. Šio formato konfigūracija turi išvesties rezultatus generuoti kaip „OpenXML“ („Excel“ failo) formato elektroninius dokumentus. Norėdami gauti daugiau informacijos, paleiskite užduočių vedlį **ER: konfigūracijos, skirtos generuoti ataskaitas OPENXML formatu, kūrimas**. Naują konfigūraciją pavadinkite **Importavimo / eksportavimo veiklos**, kaip pavaizduota tolesnėje iliustracijoje. Kurdami ER formatą, naudokite „Excel“ failą [ER duomenys – importavimo ir eksportavimo informacija](https://download.microsoft.com/download/f/7/5/f755c0fd-025c-4aa9-920b-909abb8302ad/ER-data-import-and-export-details.xlsx) kaip šabloną. (Norėdami daugiau informacijos apie tai, kaip importuoti formato šabloną, paleiskite užduočių vedlį).

[![Importavimo / eksportavimo veiklų konfigūracija.](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)

Norėdami keisti formato **Importavimo / eksportavimo veiklos** konfigūraciją, atlikite tolesnius veiksmus.

1. Spustelėkite **Konstruktorius**.
2. Skirtuke **Formatas** šio formato failo elementą pavadinkite **„Excel“ išvesties failas**.

    [![„Excel“ išvesties failo elementas.](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)

3. Skirtuke **Susiejimas** nurodykite „Excel“ failo, kuris bus visada generuojamas naudojant šį formatą, pavadinimą. Konfigūruokite susijusią išraišką, kad būtų pateikta reikšmė **Importavimo ir eksportavimo informacija** (failo vardo plėtinys .xlsx bus pridėtas automatiškai).

    [![Formato kūrimo įrankis.](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)

4. Įtraukite naują šio formato duomenų šaltinio elementą. (Šis išvardijimas bus reikalingas atliekant tolesnį duomenų susiejimą.)

    1. Duomenų šaltinį pavadinkite **direction\_enum**.
    2. Pasirinkite duomenų šaltinio tipą **Duomenų modelių išvardijimas**.
    3. Nurodykite duomenų modelio išvardijimą **Kryptis**.

    [![„direction_enum”.](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)

5. Atlikite **Intrastat** duomenų modelio elementų ir sukurto formato elementų susiejimą, kaip pavaizduota tolesnėje iliustracijoje.

    [![Susiejimo užbaigimas.](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Paleidus ER formatą sugeneruojamas išvesties rezultatas „Excel“ formatu. „Intrastat“ operacijų informacija nusiunčiama į išeigos rezultatą ir atskiriama kaip operacijos, nurodančios importavimo veiklas arba eksportavimo veiklas. Spustelėkite **Paleisti**, norėdami išbandyti naują „Intrastat“ operacijų sąrašo ER formatą puslapyje **Intrastat** (**Mokestis** &gt; **Deklaracijos** &gt; **Užsienio prekyba** &gt; **Intrastat**).

[![Puslapis „Intrastat“.](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)

Sugeneruojamas tolesnis išeigos rezultatas. Failas pavadintas **Importavimo ir eksportavimo informacija.xlsx**, kaip nurodėte formato parametruose.

[![Importavimo ir eksportavimo informacija.xlsx.](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>ER paskirties vietos konfigūravimas
Turite sukonfigūruoti ER sistemą siųsti naujos ER formato konfigūracijos išeigos rezultatą ypatingu būdu.

- Išeigos rezultatas turi būti siunčiamas pasirinkto „SharePoint Server“ aplanką.
- Kiekvieną kartą paleidus formato konfigūraciją, turi būti nauja to paties „Excel“ failo versija.

Puslapyje **Elektroninės ataskaitos** (**Organizacijos administravimas** &gt; **Elektroninės ataskaitos**) spustelėkite elementą **Elektroninių ataskaitų paskirtis** ir įtraukite naują paskirties vietą. Lauke **Nuoroda** pasirinkite anksčiau sukurtą formato konfigūraciją **Importavimo / eksportavimo veiklos**. Atlikite šiuos veiksmus, norėdami įtraukti naują nuorodos failo paskirties vietos įrašą.

1. Lauke **Pavadinimas** įveskite failo paskirties vietos pavadinimą.
2. Lauke **Failo vardas** pasirinkite „Excel“ failo formato komponento vardą **„Excel“ išvesties failas**.

Spustelėkite naujo paskirties vietos įrašo mygtuką **Parametrai**. Tada dialogo lange **Paskirties vietos parametrai** atlikite tolesnius veiksmus.

1. Skirtuke **Power BI** nustatykite parinktį **Įjungta** į **Taip**.
2. Lauke **SharePoint** pasirinkite anksčiau sukurtą dokumentų tipą **Bendrai naudojama**.

## <a name="schedule-execution-of-the-configured-er-format"></a>Sukonfigūruoto ER formato vykdymo planavimas
1. Puslapio **Konfigūracijos** (**Organizacijos administravimas** &gt; **Elektroninės ataskaitos** &gt; **Konfigūracijos**) konfigūracijų medyje pasirinkite anksčiau sukurtą konfigūraciją **Importavimo / eksportavimo veiklos**.
2. Keisti 1.1 versijos būseną iš **Juodraštis** į **Baigta**, kad šį formatą būtų galima naudoti.

    [![Importuoti/eksportuoti veiklos konfigūraciją konfigūracijos puslapyje.](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)

3. Pasirinkite baigtą konfigūracijos **Importavimo / eksportavimo veiklos** versiją ir spustelėkite **Paleisti**. Atkreipkite dėmesį, kad sukonfigūruota paskirties vieta taikoma išeigos rezultatui, sugeneruotam „Excel“ formatu.
4. Nustatykite parinktį **Paketinis vykdymas** į **Taip**, norėdami šią ataskaitą paleisti režimu be priežiūros.
5. Spustelėkite **Pasikartojimas**, norėdami suplanuoti reikiamą šio paketinio vykdymo pasikartojimą. Pasikartojimas nurodo, kaip dažnai atnaujinti duomenys bus perduoti į „Power BI“.

    [![Elektroninių ataskaitų parametrų dialogo langas.](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)

6. Sukonfigūruotą ER ataskaitos vykdymo užduotį galite rasti puslapyje **Paketinės užduotys** (**Sistemos administravimas &gt; Užklausos &gt; Paketinės užduotys**).

    [![Puslapis Paketinės užduotys.](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)

7. Kai ši užduotis vykdoma pirmą kartą, pasirinktame „SharePoint“ aplanke paskirties vieta sukuria naują „Excel“ failą sukonfigūruotu pavadinimu. Kaskart vėliau paleidus užduotį, paskirties vieta sukuria naują šio „Excel“ failo versiją.

    [![Nauja „Excel“ failo versija.](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>„Power BI“ duomenų rinkinio kūrimas naudojant ER formato išeigos rezultatą
1. Prisijunkite prie „Power BI“ ir atidarykite esamą „Power BI“ grupę (darbo sritis) arba sukurkite naują grupę. Skyriaus **Duomenų importavimas arba prijungimas** dalyje **Failai** spustelėkite **Įtraukti** arba kairiosios srities dalyje **Duomenų rinkiniai** spustelėkite pliuso ženklą (**+**).

    [![Duomenų rinkinio kūrimas.](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)

2. Pasirinkite parinktį **SharePoint – komandos svetainės**, tada įveskite naudojamo „SharePoint Server“ kelią (pateiktame pavyzdyje – `https://ax7partner.litware.com`).
3. Nueikite į aplanką **/Shared Documents/GER data/PowerBI** bei pasirinkite „Excel“ failą, kurį sukūrėte kaip naujo „Power BI“ duomenų rinkinio duomenų šaltinį.

    [![„Excel“ failo pasirinkimas.](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)

4. Spustelėkite **Prijungti**, tada – **Importuoti**. Sukuriamas naujas duomenų rinkinys, pagrįstas pasirinktu „Excel“ failu. Duomenų rinkinį taip pat galima automatiškai įtraukti į naujai sukurtą ataskaitų sritį.

    [![Duomenų rinkinys ataskaitų srityje.](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)

5. Konfigūruoti šio duomenų rinkinio naujinimo grafiką norėdami vykdyti periodinį naujinimą. Periodiniai naujinimai suteikia galimybę naudoti naujus verslo duomenis, periodiškai paleidžiant ER ataskaitą per naujas „Excel“ failo versijas, sukurtas „SharePoint Server“.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>„Power BI“ ataskaitos kūrimas naudojant naują duomenų rinkinį
1. Spustelėkite sukurtą „Power BI“ duomenų rinkinį **Importavimo ir eksportavimo informacija**.
2. Sukonfigūruokite vizualizaciją. Pvz., pasirinkite vizualizaciją **Užpildyta schema** ir sukonfigūruokite ją, kaip nurodyta toliau.

    - Duomenų rinkinio lauką **CountryOrigin** priskirkite schemos vizualizacijos laukui **Vieta**.
    - Duomenų rinkinio lauką **Amount** priskirkite schemos vizualizacijos laukui **Spalvų sotis**.
    - Duomenų rinkinio laukus **Veikla** ir **Metai** įtraukite schemos vizualizacijos laukų rinkinį **Filtrai**.

3. Įrašykite „Power BI“ ataskaitą kaip ataskaitą **Importavimo ir eksportavimo informacija**.

    [![Importavimo ir eksportavimo informacijos ataskaita.](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)

    Atkreipkite dėmesį, kad schemoje rodomos šalys / regionai, nurodyti „Excel“ faile (šiame pavyzdyje – Austrija ir Šveicarija). Šios šalys / regionai pateikiami naudojant skirtingas spalvas, kad būtų parodyta proporcinga kiekvienoje šalyje / regione išrašytų SF sumų dalis.

4. Atnaujinkite „Intrastat“ operacijų sąrašą. Įtraukiama eksportavimo operacija, kuri buvo sugeneruota Italijoje.

    [![Intrastat operacijų sąrašas.](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)

5. Palaukite kito suplanuoto ER ataskaitos vykdymo ir kito suplanuoto „Power BI“ duomenų rinkinio naujinimo. Tada peržiūrėkite „Power BI“ ataskaitą (pasirinkite, kad būtų rodomos tik importuotos operacijos). Atnaujintoje schemoje dabar rodoma Italija.

    [![Atnaujinta schema.](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance"></a>Prieiga prie „Power BI“ ataskaitos
Nustatykite integravimą su „Power BI“. Daugiau informacijos žr. [„Power BI“ integravimo kūrimas darbo sričiai](configure-power-bi-integration.md).

1. Darbo sričių puslapyje **Elektroninės ataskaitos**, kuriame palaikomas „Power BI“ integravimas (**Organizacijos administravimas** &gt; **Darbo sritys** &gt; **Elektroninių ataskaitų darbo sritis**), spustelėkite **Parinktys** &gt; **Atidaryti ataskaitų katalogą**.
2. Pasirinkite sukurtą „Power BI“ ataskaitą **Importavimo ir eksportavimo informacija**, kad ta ataskaita pasirinktame puslapyje būtų rodoma kaip veiksmo elementas.
3. Spustelėkite veiksmo elementą, norėdami atidaryti puslapį, kuriame rodoma ataskaita, sukurta naudojant „Power BI“.

    [![Importavimo ir eksportavimo informacijos ataskaita, skirta „Power BI”.](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

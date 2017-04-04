---
title: "Elektroninė duomenų perdavimo suteikti Power BI duomenų dinamika 365 operacijoms nustatyti"
description: "Šioje temoje paaiškinama, kaip galima naudoti elektroninio ataskaitų (ER) konfigūraciją, norint išdėstyti duomenų perkėlimą iš „Dynamics 365 for Operations“ egzemplioriaus į „Power BI“ tarnybas. Šioje temoje pateikiamame pavyzdyje „Intrastat“ operacijos naudojamos kaip verslo duomenys, kuriuos reikia perkelti. „Power BI“ schemos vizualizacijoje naudojami šie „Intrastat“ operacijų duomenys, kad „Power BI“ ataskaitoje būtų pateiktas įmonės importavimo / eksportavimo veiklų analizės rodinys."
author: kfend
manager: AnnBe
ms.date: 2016-10-31 13 - 22 - 29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ed0192c44b6d7e88120c64e539ebb0ac3b379831
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-electronic-reporting-to-provide-power-bi-with-data-from-dynamics-365-for-operations"></a>Elektroninė duomenų perdavimo suteikti Power BI duomenų dinamika 365 operacijoms nustatyti

Šioje temoje paaiškinama, kaip galima naudoti elektroninio ataskaitų (ER) konfigūraciją, norint išdėstyti duomenų perkėlimą iš „Dynamics 365 for Operations“ egzemplioriaus į „Power BI“ tarnybas. Šioje temoje pateikiamame pavyzdyje „Intrastat“ operacijos naudojamos kaip verslo duomenys, kuriuos reikia perkelti. „Power BI“ schemos vizualizacijoje naudojami šie „Intrastat“ operacijų duomenys, kad „Power BI“ ataskaitoje būtų pateiktas įmonės importavimo / eksportavimo veiklų analizės rodinys.

<a name="overview"></a>Apžvalga
--------

„Microsoft Power BI“ yra programinės įrangos paslaugų, programų ir jungčių, kurios kartu naudojamos norint išorinius duomenų šaltinius paversti nuosekliomis, vizualiai įtraukiančiomis ir interaktyvių įžvalgomis, rinkinys. Elektroninės ataskaitos (ER) „Microsoft Dynamics 365 for Operations“ vartotojams suteikia galimybę lengvai konfigūruoti duomenų šaltinius ir išdėstyti duomenų perkėlimą iš „Dynamics 365 for Operations“ į „Power BI“. Duomenys perkeliami kaip failai „OpenXML“ darbalapio („Microsoft Excel“ darbaknygės failų) formatu. Perkelti failai saugomi „Microsoft SharePoint Server“, kuris šiuo tikslu sukonfigūruotas. Saugomi failai naudojami „Power BI“ norint kurti ataskaitas su vizualizacijomis (lentelėmis, diagramomis, schemomis ir t.t.). „Power BI“ ataskaitas bendrai naudoja „Power BI“ vartotojus ir jas galima pasiekti „Power BI“ ataskaitų srityse bei „Dynamics 365 for Operations“ puslapiuose. Šioje temoje paaiškinamos toliau nurodytos užduotys.

-   „Dynamics 365 for Operations“ konfigūravimas.
-   ER formato konfigūracijos parengimas, norint gauti duomenis „Dynamics 365 for Operations“.
-   ER aplinkos konfigūravimas duomenims į „Power BI“ perkelti.
-   Perkeltų duomenų naudojimas „Power BI“ ataskaitai kurti.
-   „Power BI“ ataskaitos prieigos „Dynamics 365 for Operations“ kūrimas.

## <a name="prerequisites"></a>Būtinieji komponentai
Norint įvykdyti šios temos pavyzdžio užduotis, reikia toliau nurodytų prieigų.

-   Prieiga prie „Dynamics 365 for Operations“ naudojant vieną iš tolesnių vaidmenų.
    -   Elektroninės ataskaitos kūrėjas
    -   Elektroninės ataskaitos funkcijų konsultantas
    -   Sistemos administratorius
-   Prieiga prie „SharePoint Server“, kuris sukonfigūruotas naudoti su „Dynamics 365 for Operations“
-   Prieiga prie „Power BI“ sistemos

## <a name="configure-document-management-parameters"></a>Dokumentų valdymo parametrų konfigūravimas
1.  Puslapyje **Dokumentų valdymo parametrai** sukonfigūruokite prieigą prie „SharePoint Server“, kuris bus naudojamas įmonėje, prie kurios esate prisijungę (šiame pavyzdyje – įmonėje DEMF).
2.  Patikrinkite ryšį su „SharePoint Server“ ir įsitikinkite, kad prieiga jums suteikta. [![Dokumentų valdymo parametrų puslapyje](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Atidarykite sukonfigūruotą „SharePoint“ svetainę. Sukurkite naują aplanką, kuriame ER išsaugos „Excel“ failus su verslo duomenimis, kurie „Power BI“ ataskaitose reikalingi kaip „Power BI“ duomenų rinkinių šaltinis.
4.  „Dynamics 365 for Operations“ puslapyje **Dokumentų tipai** sukurkite naują dokumento tipą, kuris bus naudojamas norint pasiekti ką tik sukurtą „SharePoint“ aplanką. Lauke **Grupė** įveskite **Failas**, lauke **Vieta** įveskite **SharePoint** ir tada įveskite „SharePoint“ aplanko adresą. [![Dokumento tipų puslapį](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>ER parametrų konfigūravimas
1.  Darbo srityje **Elektroninės ataskaitos** spustelėkite saitą **Elektroninių ataskaitų parametrai**.
2.  Visuose skirtuko **Priedai** laukuose pasirinkite dokumentų tipą **Failas**.
3.  Darbo srityje **Elektroninės ataskaitos** nustatykite reikiamą teikėją kaip aktyvų, spustelėdami **Nustatyti kaip aktyvų**. Norėdami gauti daugiau informacijos, paleiskite užduočių vedlį **ER: paslaugų teikėjo pasirinkimas**.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>ER duomenų modelio kaip duomenų šaltinio naudojimas
ER duomenų modelis turi būti nustatytas kaip verslo duomenų, kurie bus naudojami „Power BI“ ataskaitose, šaltinis. Šis duomenų modelis įkeliamas iš ER konfigūracijų saugyklos. Daugiau informacijos žr. puslapyje [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](download-electronic-reporting-configuration-lcs.md) arba paleiskite užduočių vedlį **ER: konfigūracijos importavimas iš „Lifecycle Services‟**. Pasirinkite **Intrastat** kaip duomenų modelį, kuris bus įkeltas iš pasirinktos ER konfigūracijų saugyklos. (Šiame pavyzdyje modelio 1 variantas yra naudoti.) Galite pasiekti ir **Intrastat** ER modelio konfigūraciją, kad **konfigūracijos** puslapis. [![Konfigūracijos puslapis](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>ER formato konfigūracijos kūrimas
Turite sukurti naują ER formato konfigūraciją, kuri **Intrastat** duomenų modelį naudoja kaip verslo duomenų šaltinį. Šio formato konfigūracija turi išvesties rezultatus generuoti kaip „OpenXML“ („Excel“ failo) formato elektroninius dokumentus. Norėdami gauti daugiau informacijos, paleiskite užduočių vedlį **ER: konfigūracijos, skirtos generuoti ataskaitas OPENXML formatu, kūrimas**. Naują konfigūraciją pavadinkite **Importavimo / eksportavimo veiklos**, kaip pavaizduota tolesnėje iliustracijoje. Kurdami ER formatą, naudokite „Excel“ failą [ER duomenys – importavimo ir eksportavimo informacija](https://go.microsoft.com/fwlink/?linkid=845208) kaip šabloną. (Dėl informacijos, kaip importuoti formos šabloną, žaisti užduoties vadovas.) [![Importo / eksporto veiklą konfigūracijos](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) keisti į **importo / eksporto veikla** formatu konfigūracijos, atlikite šiuos veiksmus.

1.  Spustelėkite **Konstruktorius**.
2.  Skirtuke **Formatas** šio formato failo elementą pavadinkite **„Excel“ išvesties failas**. [!["Excel" išvesties failo elementas](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  Skirtuke **Susiejimas** nurodykite „Excel“ failo, kuris bus visada generuojamas naudojant šį formatą, pavadinimą. Konfigūruokite susijusią išraišką, kad būtų pateikta reikšmė **Importavimo ir eksportavimo informacija** (failo vardo plėtinys .xlsx bus pridėtas automatiškai). [![Format designer](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Įtraukite naują šio formato duomenų šaltinio elementą. (Šis išvardijimas bus reikalingas atliekant tolesnį duomenų susiejimą.)
    1.  Duomenų šaltinio pavadinimas **kryptimi\_išvardijimo**.
    2.  Pasirinkite duomenų šaltinio tipą **Duomenų modelių išvardijimas**.
    3.  Nurodykite duomenų modelio išvardijimą **Kryptis**.

    [![kryptis\_išvardijimas](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  Atlikite **Intrastat** duomenų modelio elementų ir sukurto formato elementų susiejimą, kaip pavaizduota tolesnėje iliustracijoje. [![Užbaigti privalomas](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Paleidus ER formatą sugeneruojamas išvesties rezultatas „Excel“ formatu. „Intrastat“ operacijų informacija nusiunčiama į išeigos rezultatą ir atskiriama kaip operacijos, nurodančios importavimo veiklas arba eksportavimo veiklas. Spustelėkite **paleisti** išbandyti naują ER formatą Intrastat operacijų sąrašą ir **Intrastat** puslapis (**mokesčių**&gt;**deklaracijas**&gt;**užsienio prekybos**&gt;**Intrastat**). [![Intrastato puslapis](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) sukuriamas išvesties rezultatai tokie. Failas pavadintas **Importavimo ir eksportavimo informacija.xlsx**, kaip nurodėte formato parametruose. [![Importo ir eksporto details.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>ER paskirties vietos konfigūravimas
Turite sukonfigūruoti ER sistemą siųsti naujos ER formato konfigūracijos išeigos rezultatą ypatingu būdu.

-   Išeigos rezultatas turi būti siunčiamas pasirinkto „SharePoint Server“ aplanką.
-   Kiekvieną kartą paleidus formato konfigūraciją, turi būti nauja to paties „Excel“ failo versija.

Dėl į **elektroninės** puslapis (**organizacijos administracijos**&gt;**elektroninės**), spustelėkite į **elektroninių ataskaitų paskirties** elementą, ir pridėti naują paskirties. Lauke **Nuoroda** pasirinkite anksčiau sukurtą formato konfigūraciją **Importavimo / eksportavimo veiklos**. Atlikite šiuos veiksmus, norėdami įtraukti naują nuorodos failo paskirties vietos įrašą.

1.  Lauke **Pavadinimas** įveskite failo paskirties vietos pavadinimą.
2.  Lauke **Failo vardas** pasirinkite „Excel“ failo formato komponento vardą **„Excel“ išvesties failas**.

Spustelėkite naujo paskirties vietos įrašo mygtuką **Parametrai**. Tada dialogo lange **Paskirties vietos parametrai** atlikite tolesnius veiksmus.

1.  Skirtuke **Power BI** nustatykite parinktį **Įjungta** į **Taip**.
2.  Lauke **SharePoint** pasirinkite anksčiau sukurtą dokumentų tipą **Bendrai naudojama**.

## <a name="schedule-execution-of-the-configured-er-format"></a>Sukonfigūruoto ER formato vykdymo planavimas
Dėl į **konfigūracijos** puslapis (**organizacijos administracijos**&gt;**elektroninės**&gt;**konfigūracijos**), konfigūracijų medyje pasirinkite į **importo / eksporto veikla** konfigūracijos, kurį sukūrėte anksčiau. Keisti 1.1 versijos būseną iš **Juodraštis** į **Baigta**, kad šį formatą būtų galima naudoti. [![Konfigūracijos puslapis](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) pasirinkite baigė versija su **importo / eksporto veikla** konfigūracija, o tada spustelėkite **paleisti**. Atkreipkite dėmesį, kad sukonfigūruota paskirties vieta taikoma išeigos rezultatui, sugeneruotam „Excel“ formatu. Nustatykite parinktį **Paketinis vykdymas** į **Taip**, norėdami šią ataskaitą paleisti režimu be priežiūros. Spustelėkite **Pasikartojimas**, norėdami suplanuoti reikiamą šio paketinio vykdymo pasikartojimą. Pasikartojimas nurodo, kaip dažnai atnaujinti duomenys bus perduoti iš „Dynamics 365 for Operations“ į „Power BI“. [![Elektroninės ataskaitos parametrų dialogo](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) po to, kai jis yra sukonfigūruota, jūs galite rasti ER ataskaitos vykdymo užduotis, **paketines užduotis** puslapis (**sistemos administravimo &gt;tyrimai &gt;paketines užduotis**). [![Partijos darbo pasiūlymų puslapyje](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) kai ši užduotis vykdoma pirmą kartą, į paskirties vietą sukuria naują "Excel" failą, kuris yra sukonfigūruotas pavadinimas pasirinkto SharePoint aplanko. Kaskart vėliau paleidus užduotį, paskirties vieta sukuria naują šio „Excel“ failo versiją. [![Nauja versija "Excel" failą](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>„Power BI“ duomenų rinkinio kūrimas naudojant ER formato išeigos rezultatą
Prisijunkite prie „Power BI“ ir atidarykite esamą „Power BI“ grupę (darbo sritis) arba sukurkite naują grupę. Arba paspauskite **pridėti** pagal **failus**, kad **importo arba prijungti prie duomenų** skyrių arba spustelėkite pliuso ženklą (**+**) šalia **duomenų rinkinius** kairiojoje srityje. [![Sukurti duomenų rinkinio](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) pasirinkti, **"SharePoint" – komandos svetaines**, ir tada įveskite SharePoint serveryje, kurį naudojate kelias (**https://ax7partner.spoppe.com** mūsų pavyzdyje). Tada naršykite ir atidarykite aplanką **/Shared Documents/GER data/PowerBI** bei pasirinkite „Excel“ failą, kurį sukūrėte kaip naujo „Power BI“ duomenų rinkinio duomenų šaltinį. [![Pasirinkdami "Excel" failą](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) spustelėkite **jungtis**, ir tada spustelėkite **importo**. Sukuriamas naujas duomenų rinkinys, pagrįstas pasirinktu „Excel“ failu. Duomenų rinkinį taip pat galima automatiškai įtraukti į naujai sukurtą ataskaitų sritį. [![Duomenų rinkinio ant prietaisų skydelio](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) konfigūruoti atnaujinimo tvarkaraštį, šiame duomenų rinkinyje priversti periodiškai atnaujinti. Periodiniai naujinimai suteikia galimybę naudoti naujus „Dynamics 365 for Operations“ verslo duomenis, periodiškai paleidžiant ER ataskaitą per naujas „Excel“ failo versijas, sukurtas „SharePoint Server“.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>„Power BI“ ataskaitos kūrimas naudojant naują duomenų rinkinį
Norėdami kurti naują „Power BI“ ataskaitą, spustelėkite sukurtą „Power BI“ duomenų rinkinį **Importavimo ir eksportavimo informacija**. Tada konfigūruokite vizualizaciją. Pvz., pasirinkite vizualizaciją **Užpildyta schema** ir sukonfigūruokite ją, kaip nurodyta toliau.

-   Duomenų rinkinio lauką **CountryOrigin** priskirkite schemos vizualizacijos laukui **Vieta**.
-   Duomenų rinkinio lauką **Amount** priskirkite schemos vizualizacijos laukui **Spalvų sotis**.
-   Duomenų rinkinio laukus **Veikla** ir **Metai** įtraukite schemos vizualizacijos laukų rinkinį **Filtrai**.

Įrašyti „Power BI“ ataskaitą **Importavimo ir eksportavimo informacijos ataskaita**. [![Importo ir eksporto duomenys ataskaitoje](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) Atkreipkite dėmesį, kad šis žemėlapis rodo šalyse/regionuose, kurie nurodyti "Excel" failą (Austrija ir Šveicarija šiame pavyzdyje). Šios šalys / regionai pateikiami naudojant skirtingas spalvas, kad būtų parodyta proporcinga kiekvienoje šalyje / regione išrašytų SF sumų dalis. Atnaujinkite „Intrastat“ operacijų sąrašą. Įtraukiama eksportavimo operacija, kuri buvo sugeneruota Italijoje. [![Intrastat operacijų sąrašo](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) laukti, kol kitas suplanuotas vykdyti ER ataskaitos ir kito planinio naujinimo Power BI duomenų rinkinio. Tada peržiūrėkite „Power BI“ ataskaitą (pasirinkite, kad būtų rodomos tik importuotos operacijos). Atnaujintoje schemoje dabar rodoma Italija. [![Atnaujinti žemėlapį](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-dynamics-365-for-operations"></a>Prieiga prie „Power BI“ ataskaitų programoje „Dynamics 365 for Operations“
Nustatykite „Dynamics 365 for Operations“ ir „Power BI“ integravimą. Daugiau informacijos rasite puslapyje [„Power BI‟ integravimo konfigūravimas darbo sritims](configure-power-bi-integration.md). Dėl į **elektroninės** darbo srities puslapį, kuris palaiko Power BI integracijos (**organizacijos administracijos**&gt;**darbo sritis**&gt;**elektroninių ataskaitų srities**), spustelėkite **funkcijos**&gt;**atidaryti ataskaitą katalogas**. Pasirinkite sukurtą „Power BI“ ataskaitą **Importavimo ir eksportavimo informaciją**, kad ta ataskaita pasirinktame puslapyje būtų rodoma kaip veiksmo elementas. Spustelėkite veiksmo elementą, norėdami atidaryti „Dynamics 365 for Operations“ puslapį, kuriame rodoma ataskaita, sukurta naudojant „Power BI“. [![Importo ir eksporto duomenys ataskaitoje](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Elektroninių ataskaitų paskirties vietos](electronic-reporting-destinations.md)

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)



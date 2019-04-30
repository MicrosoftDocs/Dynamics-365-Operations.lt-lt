---
title: „Dynamics 365 for Talent“ ir „Dynamics 365 for Finance and Operations“ integravimo DUK
description: Šioje temoje paaiškinama, kokie duomenys sinchronizuojami „Talent“ ir „Finance and Operations“ integracijoje.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 438c2b5689e450b9aae9c55168993f2ee84be4d5
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/12/2019
ms.locfileid: "950088"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a>„Dynamics 365 for Talent“ ir „Dynamics 365 for Finance and Operations“ integravimo DUK

[!include [banner](includes/banner.md)]

Ši tema atsako į dažnai užduodamus klausimus apie tai, kokie duomenys sinchronizuojami, kai „Dynamics 365 for Talent“ integruojama su „Dynamics 365 for Finance and Operations“.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Ar visi dokumentai sinchronizuojami, ar tik tam tikri duomenų objektai?

Naudojant „Core Human Resources“ (HR) sinchronizuojamas antrinis duomenų rinkinys. Visų objektų sąrašo žr. [Integravimas iš „Dynamics 365 for Talent“ į „Dynamics 365 for Finance and Operations“](talent-financeandoperations-integration.md).

Naudojant „Attract“ ir „Onboard“, visi duomenys yra integruoti į „Common Data Service“.

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Ar galiu sukurti naują susiejimą nenaudodamas šablonų?

Šablonai yra pradinis taškas. Galite sukurti savo šabloną, tačiau šablonas visada reikalingas kuriant integracijos projektą. Daugiau informacijos apie duomenų integratorių (DI), šablonus ir projektus žr. [Duomenų integravimas į „Common Data Service“](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a>Ar galiu susieti finansines dimensijas ir perkelti iš „Talent“ į „Finance and Operations“ arba atvirkščiai?

„Common Data Service“ finansinių dimensijų šiuo metu naudoti negalima, todėl jos neįtrauktos į numatytąjį šabloną. Šis objektas suplanuotas, bet šiuo metu nepateikiama jokia išleidimo laiko juosta.

Jei duomenys yra „Finance and Operations“, bet net „Talent“, susiekite abi sistemas kartu naudodami „Talent“ funkciją **Konfigūruoti saitus**. Daugiau informacijos apie tai, kaip konfigūruoti „Talent“ ir „Finance and Operations“ saitus žr. [Kas nauja arba pakeista „Dynamics 365 for Talent Core HR“ (2018 m. spalio 31 d.)](whats-new-talent-october-31.md).

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a>Kartais, kai importuoju darbuotojus, jie tampa neaktyviais darbuotojais „Finance and Operations“. Kodėl?

Šią klaidą galite gauti, jei „Talent“ nėra aktyvių darbuotojų įdarbinimo informacijos įrašų. Norėdami išspręsti šią problemą, pasirinkite **Personalo valdymas \> Darbuotojai \> Įdarbinimo retrospektyva \> Duomenų tvarkytuvas** ir patikrinkite, ar yra aktyvus įdarbinimo informacijos įrašas.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Jei pasirinksiu susieti tik antrinį laukų rinkinį, ar nesusietuose laukuose atlikti pakeitimai suaktyvins sinchronizavimą?

Duomenų sinchronizavimas vykdomas pagal vykdymo grafiką. Integracija paims įrašą, jei bet kuris įrašo laukas pakeičiamas, neatsižvelgiant į tai, ar laukas priskirtas integracijos susiejimui.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Kaip siųsti tik aktyvius darbuotojų pakeitimus, o ne atleistų asmenų įrašų pakeitimus?

Naudodami parinktį „Išplėstinė užklausa“ galite filtruoti ir pertvarkyti šaltinio duomenis prieš perduodami juos į paskirties vietą.

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a>Ar galiu nurodyti, kokius laukus siųsti „Finance and Operations“ dėl konkretaus objekto?

Laukai gali būti įtraukti arba pašalinti iš integracijos užduoties. Ne visi duomenų laukai, kurie yra „Common Data Service“ objekte, bus užpildomi iš „Core HR“.
Papildomi duomenys gali būti užpildomi naudojant „PowerApps“.

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Nustačiau integravimą kaip paketinę užduotį, bet „Talent“ prarado ryšį su paskirties sistema. Kaip į paskirties sistemą išsiųsti tuos pačius pakeitimus?

Tvarkant išimtis speciali sąranka nereikalinga. Duomenų integratorius automatiškai ieškos ir praneš apie klaidas, kurios įvyksta šaltinyje ir paskirties vietoje, ir leis neautomatiškai bandyti dar kartą. Tačiau jis neleidžia neautomatiškai koreguoti duomenis. Jei duomenų naujinimai būtini, jie turėtų būti įdiegti šaltinyje arba paskirties vietoje.

## <a name="can-i-set-up-bi-directional-integration"></a>Ar galiu nustatyti dvikryptį integravimą?

Ne, šiuo metu integravimas yra tik vienakryptis („Talent“ į „Finance and Operations“). Tačiau galima naudoti numatytąjį šabloną ir siųsti duomenis iš „Talent“ to „Finance and Operations“.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Ar integracijoje galima leisti naikinti įrašus?

Ne, duomenų integratorius neįtrauks panaikintų įrašų į duomenų perkėlimą. Šiuo metu įtraukti tik duomenų kūrimas ir naujinimai (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Ar galiu iš naujo vykdyti, jei vykdymas buvo klaidingas? Jei taip, ar man atsiųs visą failą, ar tik pakeitimus?

Pirmasis duomenų integratoriaus paleidimas visada yra išsamus. Vėlesni paleidimai paremti keitimų sekimu. Kai vykdomas klaidingas paleidimas, įrašai išskleidžiami vykdymo aprėptimi ir naujausi pakeitimai siunčiami „Common Data Service“.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Įrašius projekto gaunu klaidą: „Projekte yra susiejimo klaidų.“ Ką daryti?

Patikrinkite integravimo raktų sąranką, atlikite reikiamus sąrankos pakeitimus, tada atnaujinkite projekto objektus.

Kai naudojamas numatytasis šablonas, integravimo raktai importuojami automatiškai. Ši problema gali kilti, kai naujos užduotys yra įtraukiamos į esamą šabloną.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Jei aš turiu N skaičių juridinių subjektų, kuriuose darbuotojai yra įdarbinti, ar turiu sukurti kiekvienam iš jų skirtą susiejimą?

Taip, kiekvienam „Finance and Operations“ juridiniam subjektui reikia atskiro integravimo projekto duomenų integracijoje.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Noriu perkelti duomenis, kurie nepriklauso „Microsoft“ teikiamam numatytajam šablonui. Ar galiu tai padaryti?

Taip, laukai gali būti įtraukti į esamą šabloną arba iš jo pašalinti. Šabloną galima modifikuoti įtraukiant papildomų duomenų iš kitų programų „Common Data Service“ objektų. Objektas turi būti „Common Data Service“, kad jis būtų įtrauktas į šabloną. 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Ką tik sukūriau naujas „Finance and Operations“ ir „Talent“ aplinkas ir gaunu klaidą „Duomenų reikšmė pažeidžia vientisumo apribojimus.“ Kodėl?

Šios klaidos priežastys gali būti

- Duomenų perdavimo metu išgaunami įrašų dublikatai šaltinyje („Common Data Service“).

- Duomenų perdavimo „null“ reikšmė rodomos tuose laukuose, kurie būtini „Finance and Operations“. Įsitikinkite, kad duomenys yra „Common Data Service“ ir jie atitinka „Finance and Operations“ reikalavimus.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Jei kilo vykdymo klaidų ir nesinchronizuojamas Darbuotojo ID, kaip rasti retrospektyvos užduotį, kurioje yra nepavykęs darbuotojo įrašas?

Duomenų integratorius sukurs kelis projektus „Finance and Operations“. Ryšys tarp duomenų integratoriaus užduoties ir „Finance and Operations“ projekto yra tipo vienas su vienu.

Atsekite laiką iš duomenų integratoriaus vykdymo retrospektyvos ir programoje „Finance and Operations“ žr. indekso projektą –1. Jei duomenų integratoriuje užduočių skaičius yra 9, „Finance and Operations“ indeksas yra 8.

1. Užfiksuokite užduoties indeksą iš duomenų integratoriaus (šiame pavyzdyje tai „9“).

![Užfiksuokite užduoties indeksą iš duomenų integratoriaus](media/CaptureTaskIndex.png)

2. Stebėkite projekto vykdymo laiką.

![Stebėkite projekto vykdymo laiką](media/CaptureTimeOfExecution.png)

3. „Finance and Operations“ nustatykite indeksą – 1. Šiame pavyzdyje projektas su priesaga „8“ ir indekso vykdymo laikas „0“ sutampa su 2 veiksmo vykdymo laiku.

![Indekso identifikavimas](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a>Integravus „Talent“ ir „Finance and Operations“ nesimato mano „Talent“ duomenų programoje „Finance and Operation“. Ką daryti?

Integravimas su „Finance and Operations“ yra dviejų veiksmų procesas. Pirmiausia, patikrinti, ar „Talent“ yra atnaujinta ir teikiama „Common Data Service“. Tai yra beveik sinchronizavimas realiuoju laiku ir tai galima patikrinti „PowerApps“ ieškant duomenų duomenų objektuose.

![Duomenys „Common Data Service“](media/DataInCDS.png)

Jei duomenys nėra rodomi „Common Data Service“, kaip tikėtasi, patikrinkite, ar objektas palaikomas integracijoje. Norint įtraukti papildomų duomenų į „Common Data Service“, pakeitimą turi atlikti „Microsoft“.

Jei objektas yra palaikomas ir duomenys yra teikiami „Common Data Service“, patikrinkite, ar susiejimas yra tinkamas duomenų integratoriuje. Jei integratoriaus susiejimas atrodo tinkamai, tada patikrinkite, ar duomenų valdymo užduotys sėkmingai įvykdytos. Paketinių užduočių vykdymo metu gali kilti klaidų. Daugiau informacijos apie duomenų valdymą žr. [Duomenų valdymas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a>Mano darbuotojų adresai yra netikslūs juos importavus į „Finance and Operations“. Ką daryti?

**Vietos ID** numeracija naudoja tą patį modelį „Talent“ ir „Finance and Operations“. Numeracija turi būti unikali abiejose pusėse, kad adresai nesusikirstų integruojant duomenis iš „Common Data Service“ į „Finance and Operations“.

„Talent“ diegimo metu patikrinkite, ar „Talent“ ir „Finance and Operations“ numeracijos nesutampa. Įsitikinkite, kad visos numeracijos neidentiškos ir duomenys gali būti tvarkomi abiejose sistemose.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Kuriant jungčių rinkinį man nepavyksta matyti jungties išplečiamajame sąraše Jungtis. Ką daryti?

Įsitikinkite, kad kurdami jungtis pasirenkate „Dynamics 365 for Finance and Operations“ (šiuo metu – peržiūroje) ir „Common Data Service“.

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Sinchronizuojant įdiegtis gaunamos klaidos „CompanyInfo_FK doesn’t exist“ arba „The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.“ Ką daryti?

Įsitikinkite, kuria siejate tinkamus juridinius subjektus. Juridinių subjektų sinchronizavimas nėra numatytojo šablono dalis, todėl tikimasi, kad kiekvienas juridinis subjektas, esantis „Talent“ ir „Common Data Service“, taip pat bus ir „Finance and Operations“.
Taip pat įsitikinkite, kad, esate pasirinkę tinkamus susieto jungčių rinkinio juridinius subjektus.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a>Nustačius projektą atrodo, kad laukų susiejimas „Finance and Operations“ yra nenurodytas. Ką daryti?

Atnaujinkite duomenų objektus „Finance and Operations“ pasirinkdami **Duomenų valdymas \> Sistemos parametrai \> Objekto parametrai \> Naujinti objektų sąrašą.** Tai turėtų užtrukti porą minučių, tada turėtumėte matyti tuos susiejimus. Taip atsitinka, kai kuriami nauji projektai.

![Nenurodytas laukų susiejimas](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Papildomi ištekliai

- Duomenų integratorius (DI): 

  - [Duomenų integravimas į „Common Data Service“](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [Duomenų integratoriaus klaidų valdymas ir trikčių šalinimas](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [Atsakymas į DSR užklausas, sistemai sugeneruojant žurnalus „PowerApps“, „Microsoft Flow“ ir „Common Data Service“](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Duomenų valdymas:

  - [Duomenų valdymas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)

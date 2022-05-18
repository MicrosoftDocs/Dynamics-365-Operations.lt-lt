---
title: Integravimo su „Finance“ DUK
description: Šioje temoje paaiškinama, kokie duomenys sinchronizuojami „Human Resources“ ir „Finance“ integravime.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9b83250bdb54ea6e78709dd3a3ea434a994f6211
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694010"
---
# <a name="integration-with-finance-faq"></a>Integravimo su „Finance“ DUK


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šioje temoje pateikiami į bendruosius klausimus, susijusius su tai, kurie duomenys Dynamics 365 Human Resources sinchronizuojami, kai integruojami su "Dynamics 365 Finance".

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>Ar galiu redaguoti „Dynamics 365 Talent“ programos naudotoją „Power Apps“?

Ne. Jei redaguojate „Human Resources“ programos vartotoją, integravimas tarp „Human Resources“ ir „Dataverse“ gali nepavykti. Tolesnė lentelė rodo nustatytuosius nustatymus „Talent“ programos naudotojui.

| Vardas, pavardė | Programos ID | „Azure AD“ objekto ID | Programos ID URI |
| --- | --- | --- | --- |
| „Dynamics365“ skirtas „Talent“ | „f9be0c49-aa22-4ec6-911a-c5da515226ff“ | „27fd8129-4b3c-43f7-b1bf-47495d3a049b“ | „f9be0c49-aa22-4ec6-911a-c5da515226ff“ |

![Nustatytieji nustatymai „Talent“ programos naudotojui.](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Ar visi dokumentai sinchronizuojami, ar tik tam tikri duomenų objektai?

Sinchronizuojamas duomenų poaibis. Norėdami gauti visų objektų sąrašą, žr. Integravimas su ["Dynamics 365 Finance"](hr-admin-integration-finance.md).

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a>Kodėl nematau jokių duomenų, sinchronizuotų su „Dataverse“?

Esant numatytiesiems parametrams, naujose aplinkose, kuriose nėra pateiktų demonstracinių duomenų, „Dataverse“ integravimas yra išjungtas. Esant numatytiesiems nustatymams, jis įjungiamas naujose aplinkose, kuriose yra demonstracinių duomenų, o duomenų sinchronizavimas pradedamas sukonfigūravus aplinką. Kai jūsų aplinka yra pasiruošta sinchronizuoti duomenis, galite įjungti integravimą. Daugiau informacijos žr. [„Dataverse“ integravimo konfigūravimas](hr-admin-integration-common-data-service.md).

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Ar galiu sukurti naują susiejimą nenaudodamas šablonų?

Šablonai yra pradinis taškas. Galite sukurti savo šabloną, tačiau šablonas visada reikalingas kuriant integracijos projektą. Daugiau informacijos apie duomenų integratorių (DI), šablonus ir projektus žr. [Duomenų integravimas į „Microsoft Dataverse“](/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>Ar galiu susieti finansines dimensijas ir perkelti iš „Human Resources“ į „Finance“ arba atvirkščiai?

„Dataverse“ finansinių dimensijų šiuo metu naudoti negalima, todėl jos neįtrauktos į numatytąjį šabloną. Šis objektas suplanuotas, bet šiuo metu nepateikiama jokia išleidimo laiko juosta.

Jei duomenys yra „Finance“, bet net „Human Resources“, susiekite abi sistemas kartu naudodami „Human Resources“ funkciją **Konfigūruoti saitus**.

![Susieti finansines dimensijas.](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Kartais, kai importuoju darbuotojus, „Finance“ jie tampa neaktyviais darbuotojais. Kodėl?

Šią klaidą galite gauti, jei „Human Resources“ nėra aktyvių darbuotojų įdarbinimo informacijos įrašų. Norėdami išspręsti šią problemą, pasirinkite **Personalo valdymas \> Darbuotojai \> Įdarbinimo retrospektyva \> Duomenų tvarkytuvas** ir patikrinkite, ar yra aktyvus įdarbinimo informacijos įrašas.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Jei pasirinksiu susieti tik antrinį laukų rinkinį, ar nesusietuose laukuose atlikti pakeitimai suaktyvins sinchronizavimą?

Duomenų sinchronizavimas vykdomas pagal vykdymo grafiką. Integracija paims įrašą, jei bet kuris įrašo laukas pakeičiamas, neatsižvelgiant į tai, ar laukas priskirtas integracijos susiejimui.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Kaip siųsti tik aktyvius darbuotojų pakeitimus, o ne atleistų asmenų įrašų pakeitimus?

Naudodami parinktį „Išplėstinė užklausa“ galite filtruoti ir pertvarkyti šaltinio duomenis prieš perduodami juos į paskirties vietą.

![Aktyvių darbininkų išplėstinė užklausa.](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Ar galiu nurodyti, kokius laukus siųsti į „Finance“ dėl konkretaus objekto?

Laukai gali būti įtraukti arba pašalinti iš integracijos užduoties. Ne visi duomenų laukeliai esantys „Dataverse“ lentelėje bus užpildyti iš „Human Resources“.
Papildomi duomenys gali būti užpildomi naudojant „Power Apps“.

![Laukų įtraukimas arba pašalinimas iš integracijos užduoties.](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Nustačiau integravimą kaip paketinę užduotį, bet „Human Resources“ prarado ryšį su paskirties sistema. Kaip į paskirties sistemą išsiųsti tuos pačius pakeitimus?

Tvarkant išimtis speciali sąranka nereikalinga. Duomenų integratorius automatiškai ieškos ir praneš apie klaidas, kurios įvyksta šaltinyje ir paskirties vietoje, ir leis neautomatiškai bandyti dar kartą. Tačiau jis neleidžia neautomatiškai koreguoti duomenis. Jei duomenų naujinimai būtini, jie turėtų būti įdiegti šaltinyje arba paskirties vietoje.

## <a name="can-i-set-up-bi-directional-integration"></a>Ar galiu nustatyti dvikryptį integravimą?

Ne, integravimas šiuo metu yra vien way (Žmogiškieji ištekliai į finansus ir operacijas). Tačiau galima naudoti numatytąjį šabloną ir siųsti duomenis iš „Human Resources“ į „Finance“.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Ar integracijoje galima leisti naikinti įrašus?

Ne, duomenų integratorius neįtrauks panaikintų įrašų į duomenų perkėlimą. Šiuo metu įtraukti tik duomenų kūrimas ir naujinimai (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Ar galiu iš naujo vykdyti, jei vykdymas buvo klaidingas? Jei taip, ar man atsiųs visą failą, ar tik pakeitimus?

Pirmasis duomenų integratoriaus paleidimas visada yra išsamus. Vėlesni paleidimai paremti keitimų sekimu. Kai vykdomas klaidingas paleidimas, įrašai išskleidžiami vykdymo aprėptimi ir naujausi pakeitimai siunčiami „Dataverse“.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Įrašius projekto gaunu klaidą: „Projekte yra susiejimo klaidų.“ Ką daryti?

Patikrinkite integravimo raktų sąranką, atlikite reikiamus sąrankos pakeitimus, tada atnaujinkite projekto objektus.

Kai naudojamas numatytasis šablonas, integravimo raktai importuojami automatiškai. Ši problema gali kilti, kai naujos užduotys yra įtraukiamos į esamą šabloną.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Jei aš turiu N skaičių juridinių subjektų, kuriuose darbuotojai yra įdarbinti, ar turiu sukurti kiekvienam iš jų skirtą susiejimą?

Taip, kiekvienam „Finance“ juridiniam subjektui reikia atskiro integravimo projekto duomenų integravime.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Noriu perkelti duomenis, kurie nepriklauso „Microsoft“ teikiamam numatytajam šablonui. Ar galiu tai padaryti?

Taip, laukai gali būti įtraukti į esamą šabloną arba iš jo pašalinti. Šablonas gali būti modifikuotas taip, kad apimtų papildomus duomenis iš kitų „Dataverse“ lentelių. Objektas turi būti „Dataverse“, kad jis būtų įtrauktas į šabloną. 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Ką tik sukūriau naujas „Finance“ ir „Human Resources“ aplinkas ir matau klaidą „Duomenų reikšmė pažeidžia vientisumo apribojimus“. Kodėl?

Šios klaidos priežastys gali būti

- Duomenų perdavimo metu išgaunami įrašų dublikatai šaltinyje („Dataverse“).

- Duomenų perdavimo „null“ reikšmė rodomos tuose laukuose, kurie būtini „Finance and Operations“. Įsitikinkite, kad duomenys yra „Dataverse“ ir jie atitinka „Finance and Operations“ reikalavimus.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Jei kilo vykdymo klaidų ir nesinchronizuojamas Darbuotojo ID, kaip rasti retrospektyvos užduotį, kurioje yra nepavykęs darbuotojo įrašas?

Duomenų integratorius „Finance“ sukurs keletą projektų. Ryšys tarp Duomenų integratoriaus užduoties ir „Finance“ projekto yra vienas su vienu.

Atsekite laiką iš Duomenų integratoriaus vykdymo retrospektyvos ir programoje „Finance“ ieškokite projekto su –1 indeksu. Jei Duomenų integratoriuje užduoties numeris yra 9, „Finance“ indeksas yra 8.

1. Užfiksuokite užduoties indeksą iš duomenų integratoriaus (šiame pavyzdyje tai „9“).

    ![Užfiksuokite užduoties indeksą iš duomenų integratoriaus.](media/CaptureTaskIndex.png)

2. Stebėkite projekto vykdymo laiką.

    ![Stebėkite projekto vykdymo laiką.](media/CaptureTimeOfExecution.png)

3. Programoje „Finance“ raskit –1 indeksą. Šiame pavyzdyje projektas su priesaga „8“ ir indekso vykdymo laikas „0“ sutampa su 2 veiksmo vykdymo laiku.

    ![Indekso identifikavimas.](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>Integravęs „Human Resources“ ir „Finance“ nematau savo „Human Resources“ duomenų „Finance“ programoje. Ką daryti?

Integravimo su „Finance“ procesą sudaro du veiksmai. Pirmiausia, patikrinkite, ar „Human Resources“ yra atnaujinta ir teikiama „Dataverse“. Tai yra artimas realaus laiko sinchronizavimas ir gali būti tikrinamas „Power Apps“ ieškant duomenų duomenų lentelėse.

![Duomenys „Dataverse“.](media/DataInCDS.png)

Jei duomenys nėra rodomi „Dataverse“, kaip tikėtasi, patikrinkite, ar objektas palaikomas integracijoje. Norint įtraukti papildomų duomenų į „Dataverse“, pakeitimą turi atlikti „Microsoft“.

Jei objektas yra palaikomas ir duomenys yra teikiami „Dataverse“, patikrinkite, ar susiejimas yra tinkamas duomenų integratoriuje. Jei integratoriaus susiejimas atrodo tinkamai, tada patikrinkite, ar duomenų valdymo užduotys sėkmingai įvykdytos. Paketinių užduočių vykdymo metu gali kilti klaidų. Daugiau informacijos apie duomenų valdymą žr. [Duomenų valdymas](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Mano darbuotojų adresai yra netikslūs juos importavus į „Finance“. Ką daryti?

**Vietos ID** numeracija naudoja tą patį modelį programose „Human Resources“ ir „Finance“. Numeracija turi būti unikali abiejose pusėse, kad adresai nesusikirstų integruojant duomenis iš „Dataverse“ į „Finance and Operations“.

„Human Resources“ diegimo metu patikrinkite, kad „Human Resources“ ir „Finance“ numeracijos nesutaptų. Įsitikinkite, kad visos numeracijos neidentiškos ir duomenys gali būti tvarkomi abiejose sistemose.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Kuriant jungčių rinkinį man nepavyksta matyti jungties išplečiamajame sąraše Jungtis. Ką daryti?

Kurdami ryšius būtinai pasirinkite "Dynamics 365 Finance" ir Dataverse.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Sinchronizuojant įdiegtis gaunamos klaidos „CompanyInfo_FK doesn’t exist“ arba „The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.“ Ką daryti?

Įsitikinkite, kuria siejate tinkamus juridinius subjektus. Juridinių subjektų sinchronizavimas nėra numatytojo šablono dalis, todėl tikimasi, kad kiekvienas juridinis subjektas, esantis „Human Resources“ ir „Dataverse“, taip pat bus ir „Finance“. Taip pat įsitikinkite, kad, esate pasirinkę tinkamus susieto jungčių rinkinio juridinius subjektus.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>Nustačius projektą atrodo, kad laukų susiejimas „Finance“ yra tuščias. Ką daryti?

Atnaujinkite duomenų objektus programoje „Finance“, pasirinkdami **Duomenų valdymas \> Sistemos parametrai \> Objekto parametrai \> Naujinti objektų sąrašą.** Tai turėtų užtrukti porą minučių, tada turėtumėte matyti tuos susiejimus. Taip atsitinka, kai kuriami nauji projektai.

![Nenurodytas laukų susiejimas.](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Papildomi ištekliai

- Duomenų integratorius (DI): 

  - [Duomenų integravimas į „Microsoft Dataverse“](/powerapps/administrator/data-integrator)

  - [Duomenų integratoriaus klaidų valdymas ir trikčių šalinimas](/powerapps/administrator/data-integrator-error-management)

  - [Atsakymas į DSR užklausas, sistemai sugeneruojant žurnalus „Power Apps“, „Microsoft Power Automate“ ir „Dataverse“](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Duomenų valdymas:

  - [Duomenų valdymas](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

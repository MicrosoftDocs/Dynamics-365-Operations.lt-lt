---
title: Peržiūros versija Dynamics 365 Supply Chain Management 10.0.29 (2022 m. spalis)
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos programoje Microsoft Dynamics 365 Supply Chain Management 10.0.29.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 316650de19d3275f2c60c79c10d6ac8a8c79e1aa
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427880"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10029-october-2022"></a>Peržiūros versija Dynamics 365 Supply Chain Management 10.0.29 (2022 m. spalis)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje pateikiamos priemonės, kurios yra naujos arba pakeistos "Microsoft Dynamics 365 Supply Chain Management preview" versijoje 10.0.29. Ši versija turi versijos 10.0.1326 versiją ir yra pasiekiama šiame grafike:

- **Peržiūrėti leidimą:** 2022 m. rugpjūčio mėn.
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2022 m. rugsėjo mėn.
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2022 m. spalio mėn.

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Mes galime atnaujinti šį straipsnį, kad būtų įtrauktos funkcijos, kurios buvo įtrauktos į versiją iš pradžių publikuous šį straipsnį.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė   |
|---|---|---|---|
| Atsargos ir logistika | [Paskirstyti ir rezervuoti WMS prekes atsargų matomume](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | Jau greitai | Įgalinta pagal numatytuosius nustatymus |
| Atsargos ir logistika | [Iš anksto įkelti supaprastintą turimų atsargų sąrašus](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | Jau greitai | Įgalinta pagal numatytuosius nustatymus |
| Tiekimo automatizavimas pagal užsakymą | [Tiekimo automatizavimas pagal užsakymą](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Tiekimo automatizavimas pagal užsakymą](../master-planning/make-to-order-supply-automation.md) | Priemonių valdymas:<br>*Tiekimo automatizavimas pagal užsakymą* |
| Planuojama | [Peržiūrėti ir taikyti išsamias DDMRP žinias](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Poreikio valdomas medžiagų poreikių planavimo peržiūra](../master-planning/planning-optimization/ddmrp-overview.md) | Priemonių valdymas:<br>*(Peržiūros versija) Planavimo optimizavimo DDMRP* |
| Gamybos kontrolė | [Padarykite užbaigtas prekes fiziškai prieinamas prieš paskelbdami žurnaluose](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Padarykite užbaigtas prekes fiziškai prieinamas prieš paskelbdami žurnaluose](../production-control/deferred-posting.md) | Priemonių valdymas:<br>*(Peržiūros versija) Padarykite užbaigtas prekes fiziškai prieinamas prieš paskelbdami žurnaluose* |
| Sandėlio valdymas | [Ieškoti atitinkamų duomenų sandėlio mobilioje programoje](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Duomenų užklausa naudojant „Warehouse Management“ mobiliosios programėlės apėjimus](../warehousing/warehouse-app-data-inquiry.md) | Priemonių valdymas:<br>*„Warehouse Management“ programos duomenų užklausos srautas* |

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip).

Jei norite įjungti arba išjungti bet kurią iš šių priemonių, tai turite atlikti funkcijų [valdymo metu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Funkcijos pavadinimas funkcijos valdyme | Daugiau informacijos |
|---|---|---|
| Kaštų valdymas | Sudėties produkto laukiančios kainos skaičiavimo optimizavimas | Ši priemonė ištaiso nesuderinamumą, kuris kartais gali įvykti, kai sudėtiniame produkte kainos apskaičiuojamos naudojant keletą gijų. Dėl to sistema užtikrina, kad kiekviena sudėtijo produkto kaina būtų skaičiuojama tik vieną kartą. Tada šio skaičiavimo rezultatas naudojamas kaip visų kitų skaičiavimų įvestis. Jei laukiama kaina jau yra, naudojama ši kaina. |
| Bendrasis planavimas | Planavimo optimizavimo grupės operacijos | Ši funkcija gali padėti sumažinti suplanuotų užsakymų, sugeneruotų siekiant pateikti vieną pardavimo užsakymo eilutę, skaičių, kai naudojate planavimo optimizavimą. Kai ši funkcija įjungta, planavimo optimizavimas visas užsakymo eilutės atsargų operacijas sugrupuos į vieną viso kiekio reikalavimą. (Šis veikimo būdas atitinka įtaisyto planavimo modulio veikimo būdą.) Tiekimas ir poreikis grupuojami atskirai. Todėl priemonė padeda sumažinti operacijos apimtį, kai skaidote operacijas ir kai naudojate dimensijas (pvz., paketo numerius ar serijos numerius), kurios nėra padengimo dimensijos. |
| Paraiškos | Sulaikyti tiekėją pirkimo užsakymams | Ši funkcija leidžia sulaikyti tiekėją pirkimo užsakymams. Jis įtraukia naują pirkimo užsakymo sulaikymas *tipą*, kuris pažymi pirkimo užsakymų tiekėją kaip sulaikytą. Negalėsite sukurti naujų pirkimo užsakymų tiekėjams, kurie sulaikyti pirkimo užsakymams, bet vis tiek galėsite toliau tęsti bet kokias atviras SF arba mokėjimus tiems tiekėjams. |
| Pardavimas ir rinkodara | Skaičiuoti eilutės grynąją sumą importuojant | Ši funkcija leidžia kontroliuoti, *ar* sistema turi perskaičiuoti eilučių *sumas*, kai importuojate duomenis naudodami pardavimo užsakymo eilutes, *pardavimo* pasiūlymo eilutes ar grąžinimo užsakymo eilučių objektą, naudodami OData ar dvigubo rašymo funkciją. Jis veikia tik **tada**, kai taip pat turite prekybos sutarties vertinimo strategijų, kurios apriboja pardavimo užsakymo eilučių, pardavimo pasiūlymo eilučių ir (arba) grąžinimo užsakymų eilučių grynosios sumos lauko pakeitimus. Jis įtraukia parametrą, vadinamą **Skaičiuoti eilutės grynąją** **sumą į gautinų sumų nustatymo >, > parametrų** puslapyje. Kai šis parametras nustatytas kaip *Taip*, sistema, kai reikės, visada perskaičiuos eilučių sumas (tokiu būdu neatsižvelgdama į bet kokią eilutės grynosios sumos prekybos sutarties vertinimo strategiją). Kai parametras *nustatytas* kaip Ne, sistema niekada automatiškai apskaičiuos grynąją eilutės sumą, net jei įeinant į eilutės kainą, kiekį ir (arba) nuolaidą būtų galima perskaičiuoti eilutės grynąją sumą. Numatyta, kad ši funkcija įgalinta, o pirmiausia nustato **Eilutės grynosios sumos skaičiavimo** reikšmę *Taip*. *Parametras* Atitinka sistemos veikimo būdą prieš 10.0.23 versiją ir pateiktas iš anksto, kad palaiky būtų palaikomi senesni integravimo scenarijai.<br><br>Daugiau informacijos rasite eilutės [grynųjų sumų perskaičiavimą importuojant pardavimo užsakymus, pasiūlymus ir grąžinimus](../sales-marketing/calc-line-net-amounts-import.md). |
| Pardavimas ir rinkodara | Apskaičiuokite pardavimo bendrąsias sumas naudodami kelias gijas | Ši funkcija padeda pagerinti našumą, įgalindama sistemą naudoti lygiagretų apdorojimą, kai ji skaičiuoja bendras pardavimo sumas pakete. Funkcija įtrauks naują gijų **skaičių lauką** į dialogo langą **Skaičiuoti pardavimo sumas**. Jei pasirinksite vykdyti skaičiavimą pakete, naudodami šį lauką galėsite nustatyti didžiausią gijų skaičių. Jei nustatote vertę kaip *0* (nulį) arba *1*, bus naudojama viena gija. Virš 1 vertės įgalina daugiaskaitas. |
| Pardavimas ir rinkodara | Naujinti kainas ir nuolaidas, įvestas rankiniu būdu vidinei įmonei | Ši funkcija vidinės įmonės užsakymų neautomatinio pakeitimo strategijų palaiko. Ji apima vidinės įmonės pardavimo ir pirkimo užsakymų neautomatinio pakeitimo strategijų perkėlimą. Anksčiau ne vidinės įmonės užsakymuose palaikomos tik neautomatinio pakeitimo strategijos. Kai ši funkcija įgalinta, sistema jums suteikia pasirinktį atnaujinti kainas ir nuolaidas įrašius vidinės įmonės užsakymo pakeitimus. Ši pasirinktis leidžia pasirinkti, ar vidinės įmonės užsakymui norite taikyti naujų kainų ir nuolaidų informaciją, ar palikti užsakymą nepakeitusį. |

## <a name="new-and-updated-documentation-resources"></a>Nauji ir naujinti dokumentų šaltiniai

Neseniai įtraukėme arba pastebimai atnaujinome šiuos žinyno straipsnius. Šie straipsniai nebūtinai susiję su naujomis funkcijomis, kurios buvo pridėtos prie šio leidimo, kaip išvardyta ankstesniuose skyriuose. Tačiau jos gali padėti gauti daugiau informacijos apie esamas funkcijas.

| Funkcijos sritis | Nauji arba atnaujinti straipsniai |
|---|---|
| Bendrasis planavimas, CTP | [Pardavimo užsakymo pristatymo datų skaičiavimas naudojant CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Bendrasis planavimas, DDMRP | [Poreikio valdomas medžiagų poreikių planavimo peržiūra](../master-planning/planning-optimization/ddmrp-overview.md)<br>[Įjunkite savo sistemos DDMRP funkciją](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Atsargų registravimas](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Kaupimo profilis ir lygiai](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Poreikio planavimas](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Vaizdinis ir bendrasis vykdymas](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Sandėlio valdymas | [Konteinerių pakavimas siuntimui](../warehousing/packing-containers.md)<br>[Siunčiamų konteinerių pakavimo ir siuntų apdorojimo pakavimo darbas](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Šiame leidime yra funkcijų būsenos pakeitimai

Šioje lentelėje pateikiamos priemonės, kurios versijoje 10.0.29 tampa privalomomis arba pagal numatytuosius nustatymus. Visos šios priemonės bus automatiškai įjungtos jūsų sistemai, kai tik bus atnaujinta į 10.0.29 versiją. Privalomų priemonių išjungti negalima, tačiau pagal numatytuosius nustatymus įjungtas funkcijas vis tiek galima išjungti naudojant funkcijų [valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Lentelėje taip pat pateikiamos priemonės, kurios anksčiau buvo viešos peržiūros metu, bet kurios buvo pakeistos į bendrai pasiekiamas versijoje 10.0.29. Šis pakeitimas parodo, kad dabar šias priemones rekomenduojama naudoti gamybos aplinkose. Numatyta, kad šios priemonės išjungiamos, nebent pažymėta kitaip. Todėl, norėdami jas [įgalinti,](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) turite naudoti priemonių valdymą.

| Modulis | Funkcijos pavadinimas | Naujos funkcijos būsena |
| --- | --- | --- |
| Turto valdymas | [Turto valdymo funkcijos gamybos vietos vykdymo sąsajai](../production-control/production-floor-execution-configure.md) | Privalomas |
| Kaštų valdymas | [Uždarymo ir koregavimo formoje pakeisti žymą Atšaukimas į Atšaukti](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Privalomas |
| Kaštų valdymas | Valyti KS skaičiavimo informacijos kryžminio įkainojimo versijas | Privalomas |
| Kaštų valdymas | [Palyginti prekių saugojimo kainas](../cost-management/compare-item-price.md) | Privalomas |
| Kaštų valdymas | [Išlaidų skaičiavimo lygis](../cost-management/cost-calculation-level.md) | Įjungta pagal numatytuosius parametrus |
| Kaštų valdymas | Vartotojo nustatyto paketo numerio sąrankos įjungimas atsargų uždarymui atvirkštine tvarka | Įjungta pagal numatytuosius parametrus |
| Kaštų valdymas | [Išsami informacija apie atsargų uždarymo eigą](whats-new-scm-10-0-21.md) | Įjungta pagal numatytuosius parametrus |
| Kaštų valdymas | [Atsargų vertės ataskaitų saugykla](../cost-management/inventory-value-report-storage.md) | Privalomas |
| Kaštų valdymas | Atsargų vertės ataskaitos duomenų valymas | Privalomas |
| Kaštų valdymas | Slankiojo vidurkio atsarginės savikainos seka | Privalomas |
| Kaštų valdymas | Rodyti atsargų uždarymo žurnalą tinklelyje | Privalomas |
| Kaštų valdymas | Rodyti prekes, kurių operacijos nėra visiškai sudengtos, suvestinės formatu | Privalomas |
| Atsargų ir sandėlio valdymas | Leisti tuščias paketo atributų reikšmes | Privalomas |
| Atsargų ir sandėlio valdymas | Automatiškai padidinami atsargų perkėlimo užsakymo eilučių numeriai | Privalomas |
| Atsargų ir sandėlio valdymas | Kurti perkėlimo užsakymą iš pardavimo eilutės | Privalomas |
| Atsargų ir sandėlio valdymas | Išjungti atsargų žurnalo eilutės lauką darbo eigoje | Privalomas |
| Atsargų ir sandėlio valdymas | Įjungti atsargų kokybės valdymo parametrų įspėjimo funkciją | Privalomas |
| Atsargų ir sandėlio valdymas | (Kinija) Neįtraukti fizinių kvitų ir išlaidų į vidutines mėnesio išlaidas | Įjungta pagal numatytuosius parametrus |
| Atsargų ir sandėlio valdymas | [Atsargų žurnalo tvirtinimo darbo eigą](../inventory/inventory-journal-workflow.md) | Privalomas |
| Atsargų ir sandėlio valdymas | [Turimų atsargų ataskaitos saugykla](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Privalomas |
| Atsargų ir sandėlio valdymas | [Įrašyti atsargų valdymo rodiniai](saved-views-scm.md) | Privalomas |
| Atsargų ir sandėlio valdymas | Perkėlimo užsakymo atšaukimas | Privalomas |
| Atsargų ir sandėlio valdymas | Matavimo vienetų ir vienetų kiekio naudojimas atsargų žurnaluose | Privalomas |
| Atsargų ir sandėlio valdymas | Atrakinti atsargų žurnalą | Privalomas |
| Gamyba | [Automatinis su sandėliu susietų medžiagų paėmimas automatiškai užregistruotiems paėmimo sąrašams](whats-new-scm-10-0-23.md) | Bendrai prieinama |
| Gamyba | Įgalinti atsargų matmenų rodymą medžiagų sąraše gamybos maršruto operacijoms | Privalomas |
| Gamyba | [Įgalinkite paketo ir serijos numerių įvedimą, kai pranešate apie baigimą darbo kortelės įrenginiu](../production-control/report-finished-job-device.md) | Įjungta pagal numatytuosius parametrus |
| Gamyba | Pagerintas produkcijos esamo svorio parinkimas | Įjungta pagal numatytuosius parametrus |
| Gamyba | [Gamybos vietos vykdymo sąsajos užduočių ieška](../production-control/production-floor-execution-configure.md) | Privalomas |
| Gamyba | [Gamybos vykdymo sistemos integracija](../production-control/mes-integration.md) | Įjungta pagal numatytuosius parametrus |
| Gamyba | [Gamybos vietos vykdymo sąsajos rodinys „Mano diena“](../production-control/production-floor-execution-configure.md) | Įjungta pagal numatytuosius parametrus |
| Gamyba | [Gamybos užsakymų medžiagų pasiekiamumo pareikalavus patikra](whats-new-scm-10-0-24.md) | Įjungta pagal numatytuosius parametrus |
| Gamyba | [Nepaisyti numatytojo gamybos rezervavimo](../production-control/override-default-reservation-principle.md) | Privalomas |
| Gamyba | [Registruokite medžiagų suvartojimą gamybos vietos vykdymo sąsajoje (ne WMS)](../production-control/production-floor-execution-configure.md) | Bendrai prieinama |
| Gamyba | [Ataskaita apie esamo svorio prekes iš gamybos vietos vykdymo sąsajos](../production-control/production-floor-execution-configure.md) | Bendrai prieinama |
| Gamyba | [Ataskaita apie sudėtinius ir šalutinius produktus iš gamybos vietos vykdymo sąsajos](../production-control/production-floor-execution-configure.md) | Įjungta pagal numatytuosius parametrus |
| Gamyba | [Pranešti apie prekių planavimą gamybos vietos vykdymo sąsajoje](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | Įjungta pagal numatytuosius parametrus |
| Gamyba | [Gamybos kontrolės įrašyti rodiniai](saved-views-scm.md) | Privalomas |
| Gamyba | [Rodyti visą serijos, paketo ir valstybinį numerius gamybos aukšto vykdymo sąsajoje](../production-control/production-floor-execution-configure.md) | Privalomas |
| Gamyba | [Tikrinti žaliavų galiojimo pabaigą pagal suplanuoto suvartojimo datą](whats-new-scm-10-0-23.md) | Įjungta pagal numatytuosius parametrus |
| Bendrasis planavimas | [Automatinis planavimo optimizavimo patvirtinimas](../master-planning/planning-optimization/planned-order-firming.md) | Privalomas |
| Bendrasis planavimas | [Paketais valdomas tvirtinimas ir konsolidacija suplanuotiems nesupakuotiems ir supakuotiems paketiniams užsakymams](whats-new-scm-10-0-20.md) | Įjungta pagal numatytuosius parametrus |
| Bendrasis planavimas | [Įtraukti prekes su turimu likučiu, kai įjungti išankstinio apdorojimo filtrai](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | Įjungta pagal numatytuosius parametrus |
| Bendrasis planavimas | [Neribotas pajėgumų planavimas planavimo optimizavimui](../master-planning/planning-optimization/infinite-capacity-planning.md) | Įjungta pagal numatytuosius parametrus |
| Bendrasis planavimas | [Planavimo optimizavimo paraštės](../master-planning/planning-optimization/safety-margins.md) | Privalomas |
| Bendrasis planavimas | [Planavimo optimizavimo neigiamos dienos](../master-planning/planning-optimization/delay-tolerance.md) | Privalomas |
| Bendrasis planavimas | [Vienu metu vykdomas pakoreguotos poreikio prognozės įgaliojimas](whats-new-scm-10-0-20.md) | Privalomas |
| Bendrasis planavimas | [Suplanuotų užsakymų patvirtinimas naudojant filtrus](../master-planning/planning-optimization/planned-order-firming.md) | Privalomas |
| Bendrasis planavimas | [Suplanuoti planavimo optimizavimo gamybos užsakymai](../master-planning/planning-optimization/production-planning.md) | Privalomas |
| Bendrasis planavimas | [Pirkimo prekybos sutartys planavimo optimizavimui](../master-planning/planning-optimization/purchase-trade-agreement.md) | Privalomas |
| Bendrasis planavimas | [Įrašyti suplanuotų užsakymų rodiniai](saved-views-scm.md) | Privalomas |
| Paraiškos | Pirkimo užsakymų išlaidos nuo ir iki sumų | Privalomas |
| Paraiškos | Išjungti pirkimo paraiškos paskirstymo nustatymo iš naujo mygtuką | Įjungta pagal numatytuosius parametrus |
| Paraiškos | [Įjungti su įsigijimu susijusių darbo eigų nustatymą iš naujo](whats-new-scm-10-0-20.md) | Įjungta pagal numatytuosius parametrus |
| Paraiškos | [Apriboti pirkimo užsakymo eilučių skaičių kiekvienai paketinei užduočiai](whats-new-scm-10-0-27.md) | Įjungta pagal numatytuosius parametrus |
| Paraiškos | [Sujunkite tiekėjo finansines dimensijas su aktyvia dimensijos susiejimo finansine dimensija pirkimo užsakyme](whats-new-scm-10-0-25.md) | Privalomas |
| Paraiškos | [Registruoti užregistruotus atsargose laikomų produktų kiekius ir atsargose nelaikomų produktų likučius kvituose bei tiekėjo sąskaitose faktūrose](whats-new-scm-10-0-26.md) | Bendrai prieinama |
| Paraiškos | [Užkirsti kelią bendro biudžeto rezervavimų pereikvojimui, kai darbo eigoje yra kelios pirkimo paraiškos](whats-new-scm-10-0-21.md) | Įjungta pagal numatytuosius parametrus |
| Paraiškos | [Už pirkimo sutartį atsakinga šalis](../procurement/purchase-agreements.md) | Privalomas |
| Paraiškos | [Įrašyti pirkimo užsakymų rodiniai](saved-views-scm.md) | Privalomas |
| Produkto informacijos valdymas | KS ataskaitos išankstinis apdorojimas, kad būtų išvengta skirtojo laiko pabaigos | Privalomas |
| Produkto informacijos valdymas | Nustatyti finansines dimensijas pagal numatytuosius parametrus atskirai, kai naudojami prekių šablonai | Privalomas |
| Produkto informacijos valdymas | Įjungti produktų dimensijų grupes prekių šablonuose | Privalomas |
| Produkto informacijos valdymas | Prekė – brūkšninio kodo objekto patobulinimai | Privalomas |
| Produkto informacijos valdymas | Iš naujo generuoti produkto variantų pavadinimus pagal nomenklatūrą | Privalomas |
| Produkto informacijos valdymas | [Įrašyti išleistų produktų rodiniai](saved-views-scm.md) | Privalomas |
| Produkto informacijos valdymas | [Siūlomų variantų puslapio patobulinimai](../pim/tasks/create-predefined-product-variants.md) | Privalomas |
| Pardavimas ir rinkodara | [Mokesčių paskirstymas pardavimo užsakyme](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | Privalomas |
| Pardavimas ir rinkodara | Valyti pardavimo užsakymo atnaujinimų istoriją | Privalomas |
| Pardavimas ir rinkodara | [Valyti pardavimo naujinimo istoriją pagal terminą](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | Privalomas |
| Pardavimas ir rinkodara | [Kontaktinio asmens duomenų objekto eksportavimo optimizavimas](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Privalomas |
| Pardavimas ir rinkodara | Kopijuoti pardavimo kredito pažymos bendros nuolaidos grupę | Privalomas |
| Pardavimas ir rinkodara | [Įjungti pardavimo pasiūlymų dokumentų įvado ir dokumentų išvadų laukų peržvalgą](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Privalomas |
| Pardavimas ir rinkodara | [Pagerinti 100 populiariausių klientų ataskaitos našumą](whats-new-scm-10-0-23.md) | Privalomas |
| Pardavimas ir rinkodara | Į istorijos valymo užduotis įtraukite laukiančius įrašus | Privalomas |
| Pardavimas ir rinkodara | Apriboti pardavimo užsakymo eilučių skaičių kiekvienai paketinei užduočiai | Įjungta pagal numatytuosius parametrus |
| Pardavimas ir rinkodara | [Apribokite pardavimo užsakymų, kuriuos galima pasirinkti registruoti, skaičių](whats-new-scm-10-0-21.md) | Privalomas |
| Pardavimas ir rinkodara | Perskaičiuoti numatomą klientų likutį | Privalomas |
| Pardavimas ir rinkodara | [Prekių grąžinimo užsakymo eilutės registravimas dešimtainiu tikslumu su ir be esamo svorio](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Privalomas |
| Pardavimas ir rinkodara | [Pardavimų ir rinkodaros modulio įrašyti rodiniai](saved-views-scm.md) | Privalomas |
| Pardavimas ir rinkodara | [Pardavimo užsakymo patvirtinimas vienu spustelėjimu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | Privalomas |
| Transportavimo valdymas | Leisti nesusieti transportavimo sąskaitų iš transportavimo SF eilučių, jei nėra užregistruoto tiekėjo SF žurnalo | Įjungta pagal numatytuosius parametrus |
| Transportavimo valdymas | [Įjungti tiekėjo SF žurnalo kūrimą, kai atmetama transportavimo sąskaita](whats-new-scm-10-0-20.md) | Įjungta pagal numatytuosius parametrus |
| Transportavimo valdymas | [Mažų siuntinių gabenimas](../warehousing/small-parcel-shipping.md) | Privalomas |
| Transportavimo valdymas | [USMCA kilmės sertifikato dokumentas](../transportation/usmca-certification-of-origin.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Papildomos vietos zona](../warehousing/additional-location-zones.md) | Privalomas |
| Sandėlio valdymas | [Atšaukti darbą](../warehousing/cancel-warehouse-work.md) | Privalomas |
| Sandėlio valdymas | [Konsoliduoti siuntą](../warehousing/configure-shipment-consolidation-policies.md) | Privalomas |
| Sandėlio valdymas | [Kurti ir apdoroti perkėlimo užsakymus naudojant sandėlio programą](../warehousing/create-transfer-order-from-warehouse-app.md) | Privalomas |
| Sandėlio valdymas | Prekių skirstymo šablonai su vietovės nurodymais | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Atskirti atidėjimo darbą nuo ASN](whats-new-scm-10-0-21.md) | Privalomas |
| Sandėlio valdymas | [Atidėtos padėjimo operacijos](../warehousing/deferred-processing-manual-inventory-movement.md) | Privalomas |
| Sandėlio valdymas | Atidėtas padėjimas – konteineris | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | Atidėtas pateikimo apdorojimas – įgalinkite audito šablono funkciją, kai paleidimo įvykis nustatytas kaip Ankstesnis | Privalomas |
| Sandėlio valdymas | [Išjunkite numatomus kvitus iš kokybės užsakymų, kurie ima mėginius iš blokuojamų atsargų](../inventory/inventory-blocking.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | Įjungti greitą patvirtinimą sandėlio mobiliuosiuose įrenginiuose | Privalomas |
| Sandėlio valdymas | [Išplėstiniai GS1 brūkšninių kodų analizatoriai](../warehousing/gs1-barcodes.md) | Bendrai prieinama |
| Sandėlio valdymas | [Kintamas užsakymo įvykdymo numerio lentelės rezervavimas](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Privalomas |
| Sandėlio valdymas | [Kintamas sandėlio lygio dimensijos rezervavimas](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Privalomas |
| Sandėlio valdymas | [Prekės konsolidacijos vietos naudojimas](../warehousing/item-consolidation-location-utilization.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | Numerio lentelių gavimo retrospektyva | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Rankinė siuntos konsolidacija](../warehousing/consolidate-shipments-manual-workbench.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Administratoriaus arba panašių patikimų vartotojų perkėlimo eilutės išrinkimo rankiniu būdu paslauga](whats-new-scm-10-0-28.md) | Bendrai prieinama |
| Sandėlio valdymas | [Medžiagų tvarkymo įrangos sąsaja](../warehousing/mhax.md) | Privalomas |
| Sandėlio valdymas | [Nauji krovinio planavimo darbo srityje puslapiai](whats-new-scm-10-0-24.md) | Bendrai prieinama |
| Sandėlio valdymas | [Siunčiamo darbo krūvio vizualizavimas](../warehousing/outbound-workload-visualization.md) | Privalomas |
| Sandėlio valdymas | [Suplanuotas prekių skirstymas](../warehousing/planned-cross-docking.md) | Privalomas |
| Sandėlio valdymas | [Apdoroti sandėlio programos įvykius](../warehousing/warehouse-app-events.md) | Privalomas |
| Sandėlio valdymas | Sudėtinio produkto ir šalutinio produkto atidėjimo darbo šablono užklausos patobulinimas | Privalomas |
| Sandėlio valdymas | [Suapvalinti kiekius iki artimiausio pardavimo vieneto išleidžiant į sandėlį](whats-new-scm-10-0-19.md) | Privalomas |
| Sandėlio valdymas | [Įrašyti rodiniai krovinio planavimo darbo sričiai](saved-views-scm.md) | Privalomas |
| Sandėlio valdymas | [Įrašytas išsamios darbo informacijos puslapio rodinys](saved-views-scm.md) | Privalomas |
| Sandėlio valdymas | [Įrašytas rodinys bangos apdorojimui](saved-views-scm.md) | Privalomas |
| Sandėlio valdymas | [Įrašyti rodiniai krovinio apdorojimui](saved-views-scm.md) | Privalomas |
| Sandėlio valdymas | [Įrašyti rodiniai siuntos apdorojimui](saved-views-scm.md) | Privalomas |
| Sandėlio valdymas | [Nuskaityti GS1 brūkšninius kodus](../warehousing/gs1-barcodes.md) | Bendrai prieinama |
| Sandėlio valdymas | Išsami siuntos bangos žymų informacija | Privalomas |
| Sandėlio valdymas | [Atkarpos mišrūs vienetai](whats-new-scm-10-0-21.md) | Privalomas |
| Sandėlio valdymas | [Naudokite greitesnę API, jei norite uždaryti / iš naujo atidaryti konteinerius pakavimo stotyje](whats-new-scm-10-0-21.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Patvirtinti šablonus, pasirinktus papildymo užduotims](whats-new-scm-10-0-20.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Paaukštinti sandėlio programėlės laukai](../warehousing/warehouse-app-promoted-fields.md) | Privalomas |
| Sandėlio valdymas | [Sandėlio programos veiksmo instrukcijos](../warehousing/mobile-app-titles-instructions.md) | Privalomas |
| Sandėlio valdymas | [Sandėlio vietos būsena](../warehousing/warehouse-location-status.md) | Privalomas |
| Sandėlio valdymas | [„Warehouse Management“ programos apėjimas](../warehousing/warehouse-app-detours.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Išsami bangos paketinės užduoties informacija](../warehousing/wave-processing.md) | Privalomas |
| Sandėlio valdymas | [Bangos vykdymo pranešimai](../warehousing/wave-execution-notifications.md) | Privalomas |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių platformos naujinimai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.29 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, žr. [finansų ir operacijų programėlių 10.0.29 versijos platformos naujinimus (2022 m. spalio mėn.)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md).

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti informacijos apie klaidos pataisas, įtrauktas į visus naujinimus, kurie yra 10.0.29 versijos dalis, prisiregistruokite prie ciklo tarnybų (LCS) [ir peržiūrėkite žinių bazės straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>"Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 1 planas

Norite sužinoti apie būsimas ir neseniai išleistas mūsų verslo programų ar platformos galimybes?

Patikrinkite ["Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 2 planas](/dynamics365-release-plan/2022wave2/). Visą išsamią informaciją užfiksavome viename dokumente, kurį galite naudoti planuodami.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Pašalintos ir pasenusios „Supply Chain Management“ funkcijos

Straipsnyje [pašalintos arba pasenusios Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) funkcijos aprašomos priemonės, kurios buvo arba yra suplanuotos pašalinti arba pasenusios tiekimo grandinės valdymui.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Prieš pašalinant bet kokią priemonę iš produkto, [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) pranešimai dėl nušalinimo bus pereiti prie pašalintų arba pasenusių funkcijų 12 mėnesių prieš pašalinimą.

Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejetainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, tai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

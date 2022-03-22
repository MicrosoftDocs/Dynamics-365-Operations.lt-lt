---
title: „Dynamics 365 Supply Chain Management” 10.0.25 (2022 m. balandžio mėn.) peržiūra
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.25 funkcijos.
author: kamaybac
ms.date: 02/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 068e65d0bd76d7a9af36c6c3539d0c813efd528a
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384543"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10025-april-2022"></a>„Dynamics 365 Supply Chain Management” 10.0.25 (2022 m. balandžio mėn.) peržiūra

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje pristatomos funkcijos, kurios yra naujos arba pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.25 peržiūros versijoje. Šios versijos komponavimo numeris yra 10.0.1149 ir jis pasiekiamas tokius būdu:

- **Leidimo peržiūra** 2022 m. vasario mėn
- **Bendras leidimo prieinamumas (savaiminis naujinimas):** 2022 m. kovo mėn.
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2022 m. balandžio mėn.

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Galime atnaujinti šią temą, kad būtų įtraukti funkcijų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė   |
|---|---|---|---|
| Atsargos&nbsp;ir&nbsp;logistika | [Pavojingų medžiagų patobulinimai](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/hazardous-materials-enhancements) | Jau greitai | Priemonių valdymas:<br>*Pavojingų medžiagų patobulinimai* |
| Atsargos&nbsp;ir&nbsp;logistika | [Pakavimo vietų pakavimo darbas](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/packing-work-packing-stations) | Jau greitai | Priemonių valdymas:<br>*Pakavimo vietų pakavimo darbas* |
| Atsargos&nbsp;ir&nbsp;logistika | [Nuskaityti brūkšninius kodus sandėlyje naudojant GS1 formato standartus](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1 brūkšniniai kodai ir QR kodai](../warehousing/gs1-barcodes.md) | Priemonių valdymas:<br>*Nuskaityti GS1 brūkšninius kodus* |
| Gamyba | [Medžiagų suvartojimas ir rezervavimas gamybos laiko vykdymo sąsajoje](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Kaip darbuotojai naudoja gamybos vietos vykdymo sąsają](../production-control/production-floor-execution-use.md) | Priemonių valdymas:<br>*(Peržiūros versija) Registruokite medžiagų suvartojimą gamybos vietos vykdymo sąsajoje (ne WMS)*<br><br>Ir (arba):<br><br>Priemonių valdymas:<br>*(Peržiūros versija) Užregistruokite medžiagų suvartojimą gamybos vietos vykdymo sąsajoje (veikia WMS)* |
| Gamyba | [Registruoti medžiagų suvartojimą skalės vienetais](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Gamybos vykdymo darbo krūviai, skirti debesies ir briaunos skalės vienetams](../cloud-edge/cloud-edge-workload-manufacturing.md) | Priemonių valdymas:<br>*Užregistruokite medžiagų suvartojimą mobiliojoje programėlėje, esančioje svėrimo įrenginyje* |
| Planuojama | [Esamo tiekimo optimizavimo pasiūlymų planavimas](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Veiksmų pranešimai](../master-planning/action-messages.md) | Įgalinta pagal numatytuosius nustatymus |
| Planuojama | Supaprastinti planuoti užsakymai | [Supaprastinti planuoti užsakymai](../master-planning/planning-optimization/planned-orders-simplified.md ) | Priemonių valdymas:<br>*Supaprastinti planuoti užsakymai* |

## <a name="feature-enhancements-included-in-this-release"></a>Funkcijos patobulinimai, įtraukti į šį leidimą

Toliau pateiktoje lentelėje pateikti funkcijos patobulinimai, įtraukti į šį leidimą. Kiekvienas iš jų suteikia didesnį esamos funkcijos patobulinimą. Kadangi jie yra tik patobulinimai, jie nėra išvardyti [leidimo plane](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) Tačiau, siekiant užtikrinti, kad šie patobulinimai bus suderinti su jūsų esamais tinkinimais ar nuostatomis, kiekvienas iš jų yra išjungiamas pagal numatytuosius nustatymus (nebent nurodyta kitaip).

Jei norite įjungti arba išjungti bet kurią iš šių priemonių, tai turite atlikti funkcijų [valdymo metu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Funkcijos pavadinimas funkcijos valdyme | Daugiau informacijos |
|---|---|---|
| Atsargų ir sandėlio valdymas | (Lenkija) Leisti susieti kelias SAD sąskaitas faktūras su viena pirkimo užsakymo eilute viename SAD | Ši priemonė leidžia suskaidyti pirkimo užsakymo eilutes ir susieti jas su vienu administravimo dokumentu (SAD), kai tos pirkimo užsakymo eilutės buvo užregistruotos kelioms skirtingoms SF (pvz., skirtingoms siuntoms). |
| Paraiškos | Sujunkite kelias pirkimo paraiškas į vieną pirkimo užsakymą pagal apskaitos datą | Ši funkcija leidžia konsoliduoti kelias pirkimo paraiškas į vieną pirkimo užsakymą, jei skirtingų pirkimo paraiškų apskaitos datos skiriasi. Pirkimo užsakymo kūrimas ir poreikio konsolidavimo pirkimo strategijos taisyklės gali būti nustatytos automatizuojant sprendimą grupuoti paraiškos eilutes pagal apskaitos datą pirkimo užsakymo lygiu. Pirkimo užsakymo konsolidavimas pagal apskaitos datą nepalaikomas, jei biudžeto kontrolė įgalinta, nes apskaitos data naudojama biudžeto rezervavimams ir biudžeto rezervavimams. Todėl jis turėtų būti išlaikytas pereinant iš pirkimo paraiškos į pirkimo užsakymą. |
| Paraiškos | Rodyti senstelėjusius numatytųjų RFQ atsakymo laukų parametrus | Ši priemonė iš naujo pateikia senesnius numatytuosius pasiūlymo patvirtinimo (RFQ) atsakymo lauko parametrus, kurie anksčiau buvo pašalinti iš vartotojo sąsajos. Šie parametrai neįeja jokios funkcijos į lauką, bet gali būti pritaikyti, kad juos būtų galima pateikti pagal reikiamus parametrus. Įgalinkite šią funkciją, jei jūsų organizacija jau įtraukė numatytųjų RFQ atsakymo lauko parametrų funkcijas arba planuojama į ją. Įgalinę šią funkciją, **galite** pasiekti parametrus pereidami į įsigijimo ir gavimo parametrų puslapį, **·** **atidarydami pasiūlymo patvirtinimo skirtuką ir pasirinkdami numatytuosius pasiūlymo patvirtinimo atsakymo laukus**. |
| Paraiškos | Sujunkite tiekėjo finansines dimensijas su aktyvia dimensijos susiejimo finansine dimensija pirkimo užsakyme | Ši funkcija leidžia sulieti finansines dimensijas iš tiekėjų su aktyvia dimensijos sąsaja finansines dimensijas po pirkimo paraiškos patvirtinimo, jei nustatote finansinės dimensijos ir svetainės atsargų dimensijos saitą. Pirkimo užsakymo kūrimas ir poreikio konsolidavimo pirkimo strategijos taisyklės gali būti nustatytos taip, kad būtų galima valdyti sprendimą sulieti finansines dimensijas iš tiekėjų su aktyvia dimensijos saito finansine dimensija pirkimo užsakymo antraštės lygyje. |
| Gamybos kontrolė | (Rusija) Įgalinti numatytąjį vietos nustatymą, gamybos formulę / KS ir automatinį GTD rezervavimą / suvartojimą gamyboje | Priemonė įgalina papildomas gamybos iš importuotų žaliavų pasirinktis (tik rusiška lokalizacija):<ul><li>Pasirinkti nustatyti automatinę numatytąją gamybos formulių ir komplektavimo specifikacijos vietą išteklių grupėse ir sandėliuose.</li><li>Automatinis žaliavų rezervavimas pagal *GTD numerio* dimensiją WMS aktyvuose sandėliuose pagal ne WMS rezervavimo algoritmą. Tai taikoma *tais* **·** *atvejais*, kai žaliavų paėmimo darbo strategija, kurios darbo kūrimo metodas nustatytas kaip Niekada, o sandėlio, vietos ir prekės numerio nustatymas atitinka gamybos (paketinio) užsakymo atsargų operacijas.</li><li>Automatinis žaliavų suvartojimas pagal *GTD numerio dimensiją* išrinkimo dokumentų registravimo metu pagal anksčiau apibūdintą įsigytą rezervavimą.</li></ul> |
| Sandėlio valdymas | (Peržiūros versija) Gaunamų ir išsiunčiamų sandėlio užsakymų svėrimo įrenginių palaikymas | Dėl šios funkcijos sistema gali kurti siunčiamus sandėlio užsakymus paleidimo į sandėlį proceso metu ir kurti gavimo sandėlio užsakymus, kai perkėlimo užsakymai registruojami kaip išsiųsti. Sistema susinchronizuoja kiekvieną atvežimo ar siuntimo sandėlio užsakymą su skalės vienetu, atsakingu už užsakymo siuntimą arba gavimą. Atkreipkite dėmesį, kad įgalinus šią funkciją reikia atnaujinti sandėlio vykdymo darbo krūvius. Daugiau informacijos rasite [Sandėlio valdymo darbo krūviai debesies ir briaunos skalės vienetams](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Šiai funkcijai *reikia "Decouple" naudojimo iš ASN funkcijos ir bus galima gauti perkėlimo užsakymus* naudojant numerio lentelės gavimo procesą sandėlio valdymo mobilioje programoje. |

## <a name="feature-state-changes-in-this-release"></a>Šiame leidime yra funkcijų būsenos pakeitimai

Šioje lentelėje pateikiamos priemonės, kurios tampa privalomos arba pagal numatytuosius nustatymus prasideda 10.0.25. Visos šios priemonės bus automatiškai įjungtos jūsų sistemai, kai tik bus atnaujinta į 10.0.25. Privalomų priemonių išjungti negalima, tačiau pagal numatytuosius nustatymus įjungtas funkcijas vis tiek galima išjungti naudojant funkcijų [valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Lentelėje taip pat pateikiamos priemonės, kurios anksčiau buvo viešos peržiūros metu, bet kurios pasikeitė į galimos 10.0.25, t. y. jas dabar rekomenduojama naudoti gamybos aplinkose. Numatyta, kad šios priemonės išjungiamos, nebent pažymėta kitaip, [todėl](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) norėdami jas įgalinti turite naudoti funkcijų valdymą, jei norite jas naudoti.

| Modulis | Funkcijos pavadinimas | Funkcijos būsena |
| --- | --- | --- |
| Turto valdymas | [Taikymo taisykles darbo užsakymų grupavimui vykdant priežiūros planą](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | Bendrai prieinama |
| Turto valdymas | [Skaitikliu pagrįsti priežiūros patobulinimai](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | Bendrai prieinama |
| Kaštų valdymas | [Išlaidų skaičiavimo lygis](../cost-management/cost-calculation-level.md) | Bendrai prieinama |
| Kaštų valdymas | Vartotojo nustatyto paketo numerio sąrankos įjungimas atsargų uždarymui atvirkštine tvarka | Bendrai prieinama |
| Kaštų valdymas | [Išsami informacija apie atsargų uždarymo eigą](whats-new-scm-10-0-21.md) | Bendrai prieinama |
| Kaštų valdymas | [Atsargų standartinės savikainos perkainojimo finansinių dimensijų numatytojo vykdymo parinktys](../cost-management/manage-standard-cost-updates.md) | Bendrai prieinama |
| Kaštų valdymas | Atsargų vertės ataskaitos duomenų valymas | Įjungta pagal numatytuosius parametrus |
| Kaštų valdymas | [Atsargų vertės ataskaitų saugykla](../cost-management/inventory-value-report-storage.md) | Įjungta pagal numatytuosius parametrus |
| Kaštų valdymas | Rodyti atsargų uždarymo žurnalą tinklelyje | Įjungta pagal numatytuosius parametrus |
| Inžinerinių pakeitimų valdymas | [Pakeitimų valdymo įjungimas esamiems produktams](../engineering-change-management/change-management-existing-products.md) | Įjungta pagal numatytuosius parametrus |
| Inžinerinių pakeitimų valdymas | [Inžinerijos pakeitimų valdymas](../engineering-change-management/product-engineering-overview.md) | Įjungta pagal numatytuosius parametrus |
| Inžinerinių pakeitimų valdymas | [Inžinerijos pranešimai gamybai](../engineering-change-management/engineering-change-management.md) | Įjungta pagal numatytuosius parametrus |
| Inžinerinių pakeitimų valdymas | [Patobulintas atributų paveldimumas inžinerinių pakeitimų valdymui](../engineering-change-management/engineering-attributes-and-search.md) | Įjungta pagal numatytuosius parametrus |
| Inžinerinių pakeitimų valdymas | [Tvarkyti formulių ir jų sudedamųjų dalių keitimus](../engineering-change-management/manage-formula-changes.md) | Įjungta pagal numatytuosius parametrus |
| Inžinerinių pakeitimų valdymas | [Produkto parengties patikros](../engineering-change-management/product-readiness.md) | Įjungta pagal numatytuosius parametrus |
| Inžinerinių pakeitimų valdymas | [Inžinierinių produktų variantų generavimas](../engineering-change-management/engineering-variants.md) | Įjungta pagal numatytuosius parametrus |
| Atsargų ir sandėlio valdymas | Naršymas iki KS versijos iš KS eilučių | Privalomas |
| Bendrasis planavimas | [Paketais valdomas tvirtinimas ir konsolidacija suplanuotiems nesupakuotiems ir supakuotiems paketiniams užsakymams](whats-new-scm-10-0-20.md) | Bendrai prieinama |
| Bendrasis planavimas | Išteklių planavimas ir priežiūra | Bendrai prieinama |
| Bendrasis planavimas | Įgalinti bendrojo plano nustatymo vedlio priemones | Privalomas |
| Bendrasis planavimas | [Prognozės modelio pasirinkimas poreikio prognozės informacijoje](../master-planning/manual-adjustments-baseline-forecast.md) | Privalomas |
| Bendrasis planavimas | [Pagrindinio planavimo eigos vizualizavimas](../master-planning/tasks/monitor-master-planning-run.md) | Privalomas |
| Bendrasis planavimas | [Lygiagretusis suplanuotų užsakymų patvirtinimas](../master-planning/planning-optimization/planned-order-firming.md) | Privalomas |
| Bendrasis planavimas | [Suplanuotų užsakymų patvirtinimas naudojant filtrus](../master-planning/planning-optimization/planned-order-firming.md) | Įjungta pagal numatytuosius parametrus |
| Bendrasis planavimas | [Įrašyti suplanuotų užsakymų rodiniai](saved-views-scm.md) | Įjungta pagal numatytuosius parametrus |
| Paraiškos | Išjungti pirkimo apraiškos paskirstymo anuliavimo mygtuką | Bendrai prieinama |
| Paraiškos | [Įjungti su įsigijimu susijusių darbo eigų nustatymą iš naujo](whats-new-scm-10-0-20.md) | Bendrai prieinama |
| Paraiškos | Galimybė patvirtinti priimtus paketinius pirkimo užsakymus iš tiekėjo bendradarbiavimo | Privalomas |
| Paraiškos | Pirkimo sutarties būsena Uždaryta | Privalomas |
| Paraiškos | Įtraukti eilutes į PO sąskaitas faktūras, susietas su pirkimo sutartimi | Įjungta pagal numatytuosius parametrus |
| Paraiškos | Įtraukti lauką Užsakytas kiekis į registruojamo gavimo dokumento puslapį | Įjungta pagal numatytuosius parametrus |
| Paraiškos | [Leisti tiekėjams kreiptis dėl įsigijimų kategorijų bendradarbiaujant pardavėjams](../procurement/category-requests-from-vendors.md) | Įjungta pagal numatytuosius parametrus |
| Paraiškos | Mokesčiai nuo ir iki sumų pirkimo užsakymuose | Įjungta pagal numatytuosius parametrus |
| Paraiškos | Mokesčių nustatymas naudojant teritoriją ir sandėlį | Įjungta pagal numatytuosius parametrus |
| Paraiškos | Įgalinti pirkimo muito mokesčio apskaičiavimą remiantis metiniu tarifu | Įjungta pagal numatytuosius parametrus |
| Paraiškos | [Už pirkimo sutartį atsakinga šalis](../procurement/purchase-agreements.md) | Įjungta pagal numatytuosius parametrus |
| Paraiškos | [Įrašyti pirkimo užsakymų rodiniai](saved-views-scm.md) | Įjungta pagal numatytuosius parametrus |
| Produkto informacijos valdymas | [Numatytųjų užsakymų kiekių griežta patikra](../production-control/default-order-settings.md) | Privalomas |
| Produkto informacijos valdymas | KS ataskaitos išankstinis apdorojimas, kad būtų išvengta skirtojo laiko pabaigos | Įjungta pagal numatytuosius parametrus |
| Produkto informacijos valdymas | Nustatyti finansines dimensijas pagal numatytuosius parametrus atskirai, kai naudojami prekių šablonai | Įjungta pagal numatytuosius parametrus |
| Produkto informacijos valdymas | Įjungti produktų dimensijų grupes prekių šablonuose | Įjungta pagal numatytuosius parametrus |
| Produkto informacijos valdymas | Iš naujo generuoti produkto variantų pavadinimus pagal nomenklatūrą | Įjungta pagal numatytuosius parametrus |
| Produkto informacijos valdymas | [Siūlomų variantų puslapio patobulinimai](../pim/tasks/create-predefined-product-variants.md) | Įjungta pagal numatytuosius parametrus |
| Gamybos kontrolė | Pagerintas produkcijos esamo svorio parinkimas | Bendrai prieinama |
| Gamybos kontrolė | Naujas mygtukas sustabdyti pertrauką įtrauktas į užduoties kortelės terminalo puslapį | Privalomas |
| Gamybos kontrolė | [Įgalinkite automatinį numerio lentelės numerio generavimą, kai Užduoties kortelės įrenginyje pranešama apie pabaigimą](../production-control/production-floor-execution-configure.md) | Privalomas |
| Gamybos kontrolė | Įgalinti dalinį subrangos prekių gavimą ir taisyti išdavimą su tiekėjo tipo KS eilučių nurašymo skaičiavimu | Privalomas |
| Gamybos kontrolė | [Funkcija skirta užrakinti darbo kortelės prietaisą ir darbo kortelės terminalą jų valymui](../production-control/production-floor-execution-configure.md) | Privalomas |
| Gamybos kontrolė | Dialogo langų Patvirtinti ir Perkelti užduotis patobulinimai | Privalomas |
| Gamybos kontrolė | [Užbaigtos ataskaitos numerio lentelė įtraukta į užduoties kortelės įrenginį](../production-control/production-floor-execution-configure.md) | Privalomas |
| Gamybos kontrolė | [Spausdinti etiketę iš užduoties kortelės įrenginio](../production-control/production-floor-execution-configure.md) | Privalomas |
| Gamybos kontrolė | [Gamybos vietos vykdymas](../production-control/production-floor-execution-configure.md) | Privalomas |
| Gamybos kontrolė | [Turto valdymo funkcijos gamybos vietos vykdymo sąsajai](../production-control/production-floor-execution-configure.md) | Įjungta pagal numatytuosius parametrus |
| Gamybos kontrolė | [Gamybos vietos vykdymo sąsajos užduočių ieška](../production-control/production-floor-execution-configure.md) | Įjungta pagal numatytuosius parametrus |
| Gamybos kontrolė | [Nepaisyti numatytojo gamybos rezervavimo](../production-control/override-default-reservation-principle.md) | Įjungta pagal numatytuosius parametrus |
| Gamybos kontrolė | [Rodyti visą serijos, paketo ir valstybinį numerius gamybos aukšto vykdymo sąsajoje](whats-new-scm-10-0-21.md) | Įjungta pagal numatytuosius parametrus |
| Pardavimas ir rinkodara | [Pardavimo užsakymo informacijos našumo gerinimas](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Bendrai prieinama |
| Pardavimas ir rinkodara | Pardavimo pasiūlymo informacijos našumo gerinimas | Bendrai prieinama |
| Pardavimas ir rinkodara | Pardavimo užsakyme nurodyta duomenų eksportavimo politika | Privalomas |
| Pardavimas ir rinkodara | [Pardavimo užsakymo ryšio su pirkimo užsakymu eilutės trynimo strategija](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | Privalomas |
| Pardavimas ir rinkodara | [Pardavimo pasiūlyme nurodyta duomenų eksportavimo politika](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| Privalomas |
| Pardavimas ir rinkodara | [Kontaktinio asmens duomenų objekto eksportavimo optimizavimas](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Įjungta pagal numatytuosius parametrus |
| Pardavimas ir rinkodara | Įjungti pardavimo pasiūlymų dokumentų įvado ir dokumentų išvadų laukų peržvalgą | Įjungta pagal numatytuosius parametrus |
| Pardavimas ir rinkodara | [Pagerinti 100 populiariausių klientų ataskaitos našumą](whats-new-scm-10-0-23.md) | Įjungta pagal numatytuosius parametrus |
| Pardavimas ir rinkodara | Perskaičiuoti numatomą klientų likutį | Įjungta pagal numatytuosius parametrus |
| Pardavimas ir rinkodara | [Prekių grąžinimo užsakymo eilutės registravimas dešimtainiu tikslumu su ir be esamo svorio](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Įjungta pagal numatytuosius parametrus |
| Pardavimas ir rinkodara | [Įrašyti pardavimo ir rinkodaros rodiniai](saved-views-scm.md) | Įjungta pagal numatytuosius parametrus |
| Pardavimas ir rinkodara | Pardavimo užsakymo patvirtinimas vienu spustelėjimu | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Prekių skirstymo šablonai su vietovės nurodymais](../warehousing/planned-cross-docking.md) | Bendrai prieinama |
| Sandėlio valdymas | [Išjunkite numatomus kvitus iš kokybės užsakymų, kurie ima mėginius iš blokuojamų atsargų](../inventory/inventory-blocking.md) | Bendrai prieinama |
| Sandėlio valdymas | Numerio lentelių gavimo retrospektyva | Bendrai prieinama |
| Sandėlio valdymas | [Medžiagų tvarkymo įrangos sąsaja](../warehousing/mhax.md) | Bendrai prieinama |
| Sandėlio valdymas | [Suapvalinti kiekius iki artimiausio pardavimo vieneto išleidžiant į sandėlį](whats-new-scm-10-0-19.md) | Bendrai prieinama |
| Sandėlio valdymas | Skalės vieneto palaikymas sandėlio programos darbo sąrašams | Bendrai prieinama |
| Sandėlio valdymas | Išsami siuntos bangos žymų informacija | Bendrai prieinama |
| Sandėlio valdymas | [Naudokite greitesnę API, jei norite uždaryti / iš naujo atidaryti konteinerius pakavimo stotyje](whats-new-scm-10-0-21.md) | Bendrai prieinama |
| Sandėlio valdymas | [Patvirtinti šablonus, pasirinktus papildymo užduotims](whats-new-scm-10-0-20.md) | Bendrai prieinama |
| Sandėlio valdymas | Leisti papildymo šablonui naudoti esamą skubaus papildymo darbą (visiems vienetams) | Privalomas |
| Sandėlio valdymas | Automatinis GUID priskyrimas whS vartotojo kūrimui | Privalomas |
| Sandėlio valdymas | Kai gaunate krovinio prekes, fiksuokite produktų variantus ir sekimo dimensijas sandėliavimo programoje | Privalomas |
| Sandėlio valdymas | [Pakeisti prekių, valdomų taikant stebėjimo dimensijas, atsargų būseną](../inventory/inventory-statuses.md) | Privalomas |
| Sandėlio valdymas | [Darbo telkinio keitimas](../warehousing/change-work-pool-on-work.md) | Privalomas |
| Sandėlio valdymas | [Klasterio padėtis pilna](../warehousing/cluster-position-full.md) | Privalomas |
| Sandėlio valdymas | [Klasterio atidėjimo funkcija](../warehousing/putaway-clusters.md) | Privalomas |
| Sandėlio valdymas | [Tvirtinimas ir perkėlimas](../warehousing/confirm-and-transfer.md) | Privalomas |
| Sandėlio valdymas | [Patvirtinti siunčiamas siuntas naudojant paketines užduotis](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | Privalomas |
| Sandėlio valdymas | [Kontroliuokite, ar mobiliuosiuose įrenginiuose rodyti gavimo suvestinės puslapį](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Privalomas |
| Sandėlio valdymas | [Atidėtas rankinio atsargų perkėlimo operacijos apdorojimas](../warehousing/deferred-processing-manual-inventory-movement.md) | Privalomas |
| Sandėlio valdymas | Neleisti kurti krovinių, kurie neatitinka bangos krovinio kūrimo šablono reikalavimų | Privalomas |
| Sandėlio valdymas | [Patobulinti valstybinių numerių žymių maketai](../warehousing/document-routing-layout-for-license-plates.md) | Privalomas |
| Sandėlio valdymas | [Įvertinkite visus „Multi SKU“ vietos nustatymo direktyvų veiksmus](../troubleshooting/warehousing/evaluate-multiple-location-directive-actions.md) | Privalomas |
| Sandėlio valdymas | Bendros vertės lauko slėpimas puslapiuose „Visi kroviniai“ ir „Krovinio informacija“ | Privalomas |
| Sandėlio valdymas | Numerio lentelės etiketės komponavimo konfigūracija | Privalomas |
| Sandėlio valdymas | Administratorių arba panašių patikimų vartotojų krovinio eilutės taisymas rankiniu būdu | Privalomas |
| Sandėlio valdymas | [Vietos numerio lentelės padėtis](../warehousing/location-license-plate-positioning.md) | Privalomas |
| Sandėlio valdymas | [Vietos produkto dimensijos maišymas](../warehousing/location-product-dimension-mixing.md) | Privalomas |
| Sandėlio valdymas | Įgalinkite mobiliojo įrenginio atsargų judėjimo atsargų būsenos lauko redagavimą | Privalomas |
| Sandėlio valdymas | Administratoriaus arba panašių patikimų vartotojų pardavimo eilutės išrinkimo rankiniu būdu paslauga | Privalomas |
| Sandėlio valdymas | [Neleiskite, kad perduotos užsakymo siuntos numerio lentelės būtų naudojamos kituose sandėliuose nei paskirties sandėlis](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Privalomas |
| Sandėlio valdymas | Paraginti išspręsti dviprasmiškus „Vieta / NL“ pavadinimus | Privalomas |
| Sandėlio valdymas | [Kokybės patikra](../warehousing/quality-check.md) | Privalomas |
| Sandėlio valdymas | [Naujos sandėlio programos vartotojo nustatymai, piktogramos ir žingsnių pavadinimai](../warehousing/install-configure-warehouse-management-app.md) | Privalomas |
| Sandėlio valdymas | [Papildomos vietos zona](../warehousing/additional-location-zones.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Kurti ir apdoroti perkėlimo užsakymus naudojant sandėlio programą](../warehousing/create-transfer-order-from-warehouse-app.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | Įjungti greitą patvirtinimą sandėlio mobiliuosiuose įrenginiuose | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Maksimalus vykdymo laikas, skirtas turimo kiekio įrašų ištrynimo užduočiai valdant sandėlį](../warehousing/onhand-cleanup.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Siunčiamo darbo krūvio vizualizavimas](../warehousing/outbound-workload-visualization.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Apdoroti sandėlio programos įvykius](../warehousing/warehouse-app-events.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Įrašyti rodiniai krovinio planavimo darbo sričiai](saved-views-scm.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Įrašytas išsamios darbo informacijos puslapio rodinys](saved-views-scm.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Įrašytas rodinys bangos apdorojimui](saved-views-scm.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Įrašyti rodiniai krovinio apdorojimui](saved-views-scm.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Įrašyti rodiniai siuntos apdorojimui](saved-views-scm.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Išsami bangos paketinės užduoties informacija](../warehousing/wave-processing.md) | Įjungta pagal numatytuosius parametrus |
| Sandėlio valdymas | [Bangos vykdymo pranešimai](../warehousing/wave-execution-notifications.md) | Įjungta pagal numatytuosius parametrus |

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių platformos naujinimai

„Microsoft Dynamics 365 Supply Chain Management“ 10.0.25 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, žr. [finansų ir operacijų programėlių 10.0.25 versijos platformos naujinimus (2022 m. balandžio mėn.](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md)).

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.25 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>"Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 1 planas

Norite sužinoti apie būsimas ir neseniai išleistas mūsų verslo programų ar platformos galimybes?

Patikrinkite ["Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 1 planas](/dynamics365-release-plan/2022wave1/). Visą išsamią informaciją užfiksavome viename dokumente, kurį galite naudoti planuodami.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Pašalintos ir pasenusios „Supply Chain Management“ funkcijos

Temoje [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) aprašomos „Supply Chain Management“ funkcijos, kurios yra pašalintos, yra suplanuotos pašalinti arba yra pasenusios.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Prieš pašalinant iš produkto bet kokią funkciją, pranešimas apie nebenaudojimą bus paskelbtas [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) temoje 12 mėnesių prieš pašalinimą.

Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejetainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, tai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

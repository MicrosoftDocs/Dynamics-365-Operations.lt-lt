---
title: „Human Resources“ klientų perkėlimo DUK
description: Šiame straipsnyje pateikiami atsakymai į dažnai užduodamus klausimus apie Microsoft Dynamics 365 Human Resources perkėlimą į finansų ir operacijų sulietą infrastruktūrą.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e11d26ebe084762a8616c8aa0aa041a87306473
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734364"
---
# <a name="human-resources-customer-migration"></a>Personalo kliento perkėlimas

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Kaip klientai Dynamics 365 Human Resources turi planuoti veiksmus finansų ir operacijų infrastruktūrose?

Bus paveiktos dvi "Microsoft Dynamics 365 Human Resources " klientų kategorijos ir jos turės atlikti pakeitimus, kad užtikrintų, jog jie priklauso naujausiai finansų ir operacijų infrastruktūrai:

- Klientai, kurie naudoja Dynamics 365 Human Resources ir neturi jokių kitų "Dynamics 365" operacijų programėlių
- Klientai, naudojantys ir Dynamics 365 Human Resources "Dynamics 365 Finance", Dynamics 365 Supply Chain Management arba Dynamics 365 Commerce Dynamics 365 Project Operations

Neatsižvelgiant į kategoriją, kuriai jie priklauso, klientai turės perkelti duomenis į naujai sukurtą finansų ir operacijų infrastruktūros aplinką ir patikrinti, ar sulieta sėkmingai.

Eja į Dynamics 365 Human Resources priekį, programa turės atskirą finansų ir operacijų aplinką, kuri atskiria nuo kitų operacijų programėlių. Tokiu būdu klientai galės pasinaudoti extensibility pasirinktimis nenaudodami dabartinių duomenų sulieti. "Microsoft" pateiks įrankių ir sandų dėžės aplinką, kurią klientai gali naudoti duomenų perkėlimą patikrinti ir patvirtinti prieš perkeliant į gamybos aplinką. Įrankiai įgalins beveik automatizuotą procesą ir bus galimi nuo 2022 m. rugpjūčio iki lapkričio mėn.

Klientai, kurie naudoja kitas programėles finansų ir operacijų infrastruktūrose, turės pasirinktį sulieti savo personalo duomenis su esama aplinka. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>Kada klientai bus perkelti į finansų ir operacijų infrastruktūrą?

Kiekvienos įmonės perėjimas priklausys nuo dabartinės įmonės konfigūracijos ir pasirengimo pereiti prie finansų ir operacijų infrastruktūros. Rekomenduojame klientams dirbti su savo "Microsoft" partneriu, kad būtų galima nustatyti geriausią kelią į priekį.

- Organizacijos, kurios naudoja **personalo** valdymo modulį "Dynamics 365 Finance Dynamics 365 Human Resources ", galės įgalinti naujas galimybes, kaip įprasto vienos versijos atnaujinimo proceso dalį. Naujos priemonės planuojamos, kad jos būtų galimos pradedant 2022 m. sausio mėn.
- Organizacijos, kurios naudoja Dynamics 365 Human Resources, turės prieigą prie įrankių, kuriuos jos gali naudoti infrastruktūros suliejimui užbaigti. "Microsoft" su klientais pereiti prie kitų darbo vietų, kad išvengtų bet kokių aptarnavimo trukdžių. Klientams bus per 12 mėnesių pereiti, pradedant nuo to laiko, kai bus galima naudoti perkėlimo įrankį.
- Organizacijos, kurios naudoja ir Dynamics 365 Human Resources personalo valdymo **modulį**, gali perkelti savo atskirą personalo infrastruktūrą į finansų ir operacijų infrastruktūrą. Kita pasirinktis – naudoti sąlajos įrankį, kad aplinka būtų atjungta prie vienos aplinkos. Nėra reikalavimo arba laiko tarpo dviem aplinkai sulieti.

Naujausia informacija reguliariai patikrinkite paleidimo [planus](/dynamics365/release-plans/).

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>Ar klientams vis tiek reikės pasirinktinių integravimo Dynamics 365 Human Resources tarp personalo modulio ir jo?

- Klientai, kurie turi abi Dynamics 365 Human Resources ir kitas finansų ir operacijų infrastruktūros aplinkas, kurios šiuo metu integruotos, po suliejimo turės toliau integruoti dvi aplinkas.
- Klientai, kurie pasirenka Dynamics 365 Human Resources savo aplinką atskirti nuo esamų finansų ir operacijų programų aplinkos, turės toliau integruoti aplinkas, kad duomenys būtų pasiekiami abiejose aplinkose.
- Klientai gali toliau naudoti duomenų integratorių duomenims tarp dviejų aplinkos kopijuoti. Klientai, kurie sulieja duomenis vienoje aplinkoje po perkėlimo, nebeturės integruoti duomenų, nes visi duomenys bus vienoje duomenų bazėje.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>Ar kliento ISV sprendimai bus perkelti automatiškai?

Kiekvieno nepriklausomo programinės įrangos tiekėjo (ISV) sprendimo perkėlimo patirtis skirsis, priklausomai nuo sprendimo integravimo metodo. Microsoft glaudžiai dirbs su ISV, kad būtų sklandus perėjimas prie finansų ir operacijų infrastruktūros. Daugelis ISV sprendimų kuriami Dataverse naudojant galimybes Microsoft Power Platform. Šie sprendimai priklauso nuo Dataverse aplinkos Dynamics 365 Human Resources ir aplinkos Dataverse integravimo. Integracija Dataverse pasenusi kaip infrastruktūros suliejimo dalis. Finansinėse ir operacijų infrastruktūrose naujos dvigubo rašymo schemos planuojamos, siekiant pakeisti integravimo Dataverse funkcijas.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Kaip bus paveiktas duomenų integratorius, kuris perkelia duomenis tarp Dynamics 365 Human Resources kitų "Dynamics 365" programėlių?

Po to, kai klientai pereis į finansų ir operacijų infrastruktūrą, jie turės toliau integruoti duomenis tarp dviejų aplinkose. Klientai gali toliau naudoti duomenų integratorių šioms duomenų perkėlimo užduotims atlikti. Klientai, kurie planuojate savo aplinką Dynamics 365 Human Resources atskirti nuo esamų finansų ir operacijų programėlių aplinkos, turės toliau integruoti duomenis iš vienos aplinkos į kitas. Klientams, kurie sulieja dvi aplinkas į vieną aplinką, šioms dviem aplinkai daugiau nebebus reikalingas integravimas.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>Kaip duomenys bus perkelti iš vienos Dynamics 365 Human Resources finansinės ir operacijos infrastruktūros į kitą ir Dataverse po perkėlimo?

Dabartinė integracija Dataverse į Dynamics 365 Human Resources finansų ir Dataverse operacijų infrastruktūrą yra pasenusi. Yra planų pristatyti dvigubo rašymo schemas, siekiant su lentelėmis susieti finansų ir operacijų objektus Dataverse. Klientai turės nuspręsti, kurios dvigubo rašymo schemos reikalingos jų diegimo metu. Rekomenduojame virtualias lenteles naudoti integruojant ir ISV sprendimus, Dataverse nebent norint vykdyti verslo logiką duomenys turi būti dubliuoti, privalo būti konkretus verslo poreikis.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>Kaip perkėlimas paveikia plėtinius Dataverse Dynamics 365 Human Resources?

Prieš perkeliant gamybos aplinką, klientai turės perkelti į sandbox aplinką. Kai klientai perkelia savo sandbox aplinką, Dataverse jie turės sukurti savo aplinkos kopiją, kad prisijungtų prie naujos finansų ir operacijų perkeltos aplinkos. Rekomenduojame klientui nukopijuoti ir duomenis, ir aplinkos sprendimus, kad jie atitiktų esamą kliento gamybos aplinką.

Kai klientai pasiruošę perkelti savo gamybos aplinką, "Microsoft" Dynamics 365 Human Resources automatiškai perkels duomenų bazę ir "Azure BLOB" saugyklą. Perkelta duomenų bazė ir saugykla iškels naują finansų ir operacijų infrastruktūros aplinką į tą pačią gamybos aplinką Dataverse. Prieš tęsdami Dataverse duomenų kopijavimą, klientai turės įgalinti bet kokias dvigubo rašymo schemas, kurių reikia jų integravimui, plėtinius ir ISV sprendimus, kurie įtaisyti Dataverse.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Ar Microsoft Power Platform komponentai, kurie buvo sukurti Dynamics 365 Human Resources automatiškai dirbti baigus perkelti infrastruktūrą?

Sukurtos programos, eigos Power Apps sukurtose eigose ir kiti tinkinimai Power Automate yra Microsoft Power Platform pvz., Dataverse plėtiniai. Perkėlimo į kliento gamybos aplinką metu, aplinkose, įskaitant plėtinius Dataverse, įtakos neturi. Programėlių, srautų ir kitų "Power Microsoft Platform" tinkinimų naudojimas turi veikti nereikalavus papildomos konfigūracijos.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>Kas bus daroma perkėlimo Dataverse metu virtualios lentelės Dynamics 365 Human Resources objektuose?

Kai klientai perkelia savo Dynamics 365 Human Resources aplinką į finansų ir operacijų infrastruktūrą, aplinka Dataverse ir toliau bus prijungta prie aplinkos, prie kurios šiuo metu yra prijungta Dynamics 365 Human Resources. Aplinkoje Dataverse sugeneruotos virtualiosios lentelės veiks nereikalaudami papildomos konfigūracijos. Virtualias lenteles gali tekti Dataverse regeneruoti aplinkoje, kuri prijungta prie esamos kliento finansų ir operacijų aplinkos.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>Kaip bus integravimą, kuris naudoja pretendento sekimo sistemos (ATS) API, algalapių API, Dataverse virtualias Dynamics 365 Human Resources Dataverse lenteles ar kitus objektus interneto API darbui, atlikus infrastruktūros suliejimą?

Kai klientai perkelia savo Dynamics 365 Human Resources aplinką į finansų ir operacijų infrastruktūrą, aplinka Dataverse ir toliau bus prijungta prie aplinkos, prie kurios šiuo metu yra prijungta Dynamics 365 Human Resources. Bet kokia integracija, kuri buvo sukurta naudojant interneto Dataverse API, bus tęsiama baigus perkėlimą.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>Mūsų organizacija sukonfigūravo pasirinktinę saugą Dynamics 365 Human Resources. Ar jis vis tiek bus taikomas baigus infrastruktūros perkėlimą?

Taip, pasirinktinės saugos konfigūracijos bus įtrauktos į duomenų perkėlimą.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Ar darbo eigos bus Dynamics 365 Human Resources perkeltos automatiškai?

Taip, darbo eigos konfigūracijos, darbo eigos retrospektyva ir dabartinės apdorojamos darbo eigos bus perkeltos į sulietą infrastruktūrą.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Ar įrašyti rodiniai Dynamics 365 Human Resources bus perkelti automatiškai?

Taip, įrašytos peržiūros bus perkeltos į susietą infrastruktūrą.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Ar priemonės, kurios yra įgalintos automatiškai Dynamics 365 Human Resources, bus prieinamos po infrastruktūros suliejimo?

- Klientų, kurie naudoja personalo **valdymo modulį**, priemonės, kurias galima naudoti tik Dynamics 365 Human Resources, bus valdomos naudojant funkcijų valdymą. Paprastai šios priemonės pagal numatytuosius nustatymus nebus įgalintos. Visos priemonės, kurias reikia įgalinti pagal numatytuosius nustatymus, bus dokumentuotos.
- Klientams, kurie naudoja Dynamics 365 Human Resources, priemonės bus prieinamos infrastruktūrose. Visos funkcijos, kurių nėra, bus dokumentuotos. Kiekvienas funkcijų valdymo raktas, įgalintas dabartinėje aplinkoje Dynamics 365 Human Resources, bus įgalintas susietos infrastruktūrose. Daugiau informacijos žr. [Funkcijų valdymo apžvalga](/fin-ops/get-started/feature-management-overview.md).

## <a name="what-happens-to-byod-databases-during-the-migration"></a>Kas atsitinka su BYOD duomenų bazėmis perkėlimo metu?

Importavimo ir eksportavimo konfigūracijos, kad jūsų duomenų bazė (BYOD) būtų perkelta į finansų ir operacijų infrastruktūrą.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>Ar paveikta "Azure" regionas, kai perkeliama kliento aplinka?

Aplinka Dynamics 365 Human Resources ir toliau bus tame pačiame "Azure" regione, kad būtų galima perkelti. Jei reikalaujama perkelti aplinką į kitą "Azure" regioną, klientas turės laikytis standartinių veiksmų, kurie bus perkelti į naują regioną baigus perkėlimą.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>Kas atsitinka su "Azure" duomenų į įrenginį perkėlimo metu?

Perkėlus visi šiuo metu sukonfigūruoti "Azure Data Azure" duomenų "Azure" finansų ir operacijų programėlių eksportavimai turės tą pačią konfigūraciją.

> [!NOTE]
> Dvigubo rašymo schemos turės būti įgalintos toliau rašyti duomenis iš personalo aplinkos į Dataverse.

Klientai, kurie nori eksportuoti personalo duomenis į duomenų perkėlimą į finansų ir operacijų infrastruktūrą gali įgalinti šią funkciją. Norėdami gauti daugiau informacijos, žr. [duomenų "azure" architektūros centrą](/azure/architecture/data-guide/scenarios/data-lake).

Klientai gali susieti kelias finansų ir operacijų aplinkas su tomis pačiomis duomenų objektų aplinkamis. Tačiau kiekviena aplinka pereis į kitą aplanką ir konteinerį. Klientai, kurie vėliau planuojate sulieti aplinkas, turi kruopščiai suplanuoti savo požiūrį.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>Koks perkėlimas bus reikalingas, jei klientas šiuo metu naudoja personalo valdymo modulį?

Klientai, kurie naudoja **personalo valdymo** modulį Dynamics 365 Human Resources, turės naujas funkcijų funkcijas, kurios taikomos jų aplinkai per standartinį vienos versijos naujinimo procesą. Klientai gali tikėtis pamatyti naujas funkcijas savo aplinkoje po to, kai jos bus galimos kiekviename naujinime. Klientai gali naudotis funkcijų valdymu, norėdami įgalinti šias funkcijas. Klientai turi suplanuoti patikrinti šias naujas funkcijas, naudodami procesus, kuriuos jie jau turi ir naudoti kitiems savo aplinkos naujinams tikrinti.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>Kas bus daroma pasirinktiniam integravimui į išorines sistemas?

Klientai turės perkelti savo integravimą į finansų ir operacijų aplinką. Šios aplinkos galinis punktas skiriasi, todėl klientams gali tekti atnaujinti arba pakeisti integravimą, kad jie būtų nurodyti naujoje aplinkoje. Pirmiausia ši užduotis bus neautomatinis procesas, o reikalingi pakeitimai priklausys nuo integravimo architektūros. Klientai turi dirbti su "Microsoft" partneriu, kad nustatytų geriausią integravimo perkėlėjimo būdą.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>Kas bus su Microsoft Power Platform (Dataverse) plėtiniais, jei klientai sujungsite aplinką Dynamics 365 Human Resources su esama finansų ir operacijų aplinka?

Jei klientai nusprendžia po Dynamics 365 Human Resources Dataverse perkėlimo susieti aplinką ir esamą finansų ir operacijų aplinką su vienu egzemplioriumi, Dataverse jų aplinkos turi būti sujungtos, kaip suliejimo proceso dalis. Šiai užduočiai atlikti reikės, kad visos naudojant sukurtos Power Apps programėlės ir kiti tinkinimai būtų iš naujo įdiegti naujo naujoje aplinkoje.

## <a name="what-will-happen-to-documents-during-the-migration"></a>Kas bus su dokumentais perkėlimo metu?

Kai klientai perkelia savo Dynamics 365 Human Resources aplinką į finansų ir operacijų infrastruktūrą, dokumentai liks esamoje dokumentų saugykloje ir bus automatiškai susieti su nauja finansų ir operacijų infrastruktūros aplinka.

Būsimoje versijoje bus pateikti nauji duomenų objektai. Po šio pakeitimo klientai, kurie pasirenka susieti savo aplinką su esama finansų ir operacijų aplinka, Dynamics 365 Human Resources galės eksportuoti dokumentus ir perkelti juos į esamą aplinką.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>Po perkėlimo kas atsitinka su paketine užduotimis, kurios buvo sukonfigūruotos Dynamics 365 Human Resources?

Paketinės užduotys turės būti iš naujo sukonfigūruotos finansų ir operacijų aplinkoje. Klientai turės įvertinti kiekvieną paketinę užduotį ir palyginti ją su dabartiniu paketinių užduočių sąrašu finansų ir operacijų aplinkoje. Klientai taip pat turi analizuoti visą paketo grafiką, kai jie sulieja du paketinių užduočių rinkinius, kad nustatytų, ar reikia keisti paketo grafiką, prioritetus ar paketų grupes.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>Kaip perkėlimas paveiks LCS projektą Dynamics 365 Human Resources?

Klientai turės sukurti Microsoft Dynamics naują vykdymo ciklo tarnybos (LCS) projektą, **o** jie turės pasirinkti finansų ir operacijų programėles kaip produkto ir diegimo parinktis kaip projekto tipą. Be to, sukūrus LCS projektą galimas naujas subprojekto tipo laukas. Klientai turės pasirinkti perkėlimo parinktį, kad Dynamics 365 Human Resources galėtų perkelti esamą personalo LCS projektą į finansų ir operacijų infrastruktūrą.

Finansų ir operacijų LCS projektų funkcijos skiriasi nuo personalo LCS projektų funkcijų.

Norėdami vykti tiesiogiai, nauji klientai turės atlikti šias užduotis:

- Baigti projektą.
- Užbaikite metodologiją.
- Užpildyti abonemento įvertinatorių.
- Užbaikite pasirengimo vykti procesą.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>Kaip bus perkeltas verslo procesų modeliavimo priemonė?

Klientai turės eksportuoti savo verslo procesų modelių biblioteką iš personalo LCS projekto ir importuoti ją į finansų ir operacijų LCS projektą. Be to, klientams reikės atnaujinti programos žinyno parametrus, kad jie būtų nurodyti naujame LCS projekte.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>Kaip perkėlimas paveiks tarnybos naujinimo procesą?

Po perkėlimo klientai turės daug daugiau lankstumo dėl programos ciklo valdymo (LTL) ir aptarnavimo atnaujinimų. Personalo aplinkai tarnybos naujinimai nebebus automatiškai taikomi. Vietoj to tarnyba turės laikytis vienos versijos tarnybos naujinimo procesų ir funkcijų, o naujinimų konfigūravimo naudojant LCS parinktys bus įgalintos.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>Ar klientai galės gauti "FastTrack" pagalbą su infrastruktūros sąlaja?

"Microsoft" vis dar nustato, kokie įrankiai ir ištekliai bus galimi "FastTrack", kad padėtų sulieti.

## <a name="licensing-impact"></a>Licencijos poveikis

Daugiau informacijos apie tai, kaip paveikti licencijavimas, žr. infrastruktūros [Dynamics 365 Human Resources suliejimą](hr-infrastructure-merge.md#licensing).

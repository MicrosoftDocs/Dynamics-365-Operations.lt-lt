---
title: „Dynamics 365 Human Resources” infrastruktūros sujungimo DUK
description: Ši tema atsako į dažniausiai užduodamus klausimus apie „Microsoft“ infrastruktūros sujungimą Dynamics 365 Human Resources ir Finansų ir operacijų programėlės.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c022bb15975a1411230d28067a2225c95c0573bf
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062730"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>„Dynamics 365 Human Resources” infrastruktūros sujungimo DUK

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Ši tema atsako į dažniausiai užduodamus klausimus apie „Microsoft“ infrastruktūros sujungimą Dynamics 365 Human Resources ir Finansų ir operacijų programėlės.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Kas yra „Dynamics 365 Human Resources” infrastruktūros sujungimas?

Dynamics 365 Human Resources yra atskira programa, kuri naudoja skirtingą infrastruktūrą nei kitos „Finance and Operations“ programos, pvz Dynamics 365 Finance,Dynamics 365 Supply Chain Management,Dynamics 365 Commerce ir Dynamics 365 Project Operations. Infrastruktūros sujungimas atneš Dynamics 365 Human Resources į tą pačią infrastruktūrą kaip ir kitos „Finance and Operations“ programos.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktūros sujungimo vertė ir privalumai

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Mano organizacija naudoja „Dynamics 365 Human Resources” savo žmogiškųjų išteklių operacijoms valdyti. Kokią naudą patirsime iš šių pokyčių?

- Šie pakeitimai pašalina kelis painius žmogiškųjų išteklių (HR) galimybių rinkinius iš „Dynamics 365”.
- Jie suteikia tiek „Microsoft Power Platform” išplėtimą, tiek būdą išplėsti verslo logiką ir funkcijų parinktis.
- Jie suteikia nuoseklumo tarp Dynamics 365 Human Resources ir kitos finansų ir operacijų programos, susijusios su programos gyvavimo ciklo valdymu (ALM),Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS), geografinis pasiekiamumas, išplėtimas ir kt.
- Jie leidžia jums pasinaudoti bendromis paslaugomis ir įrankiais bei sumažinti išlaidas.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Mano organizacija naudoja „Human Resources“ modulį „Dynamics 365 Finance“, „Supply Chain Management“, „Commerce“ ar „Project Operations“. Kokią naudą patirsime iš šių pokyčių?

Galimybės ir investicijos, padarytos „Dynamics 365 Human Resources” platformoje, dabar bus prieinamos klientams, kurie naudoja žmogiškųjų išteklių modulį, esantį „Dynamics 365 Finance”. Kai kurios iš šių galimybių yra atostogų ir neatvykimų valdymas, išmokų valdymas ir užduočių valdymas.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Ar prarasiu kurias nors dabar naudojamas funkcijas ar galimybes?

Tarp jų bus funkcinis lygumas Dynamics 365 Human Resources ir HR modulis „Finance and Operations“ programėlėse. „Dynamics 365 Human Resources” turės pranašumą panašioms funkcijoms. Daugiau informacijos žr. [Funkcijų valdymo apžvalga](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Ar mano vartotojų patirtis keisis?

Naujos personalo galimybės bus valdomos naudojant Funkcijų valdymą. Klientai nuspręs, ar norės jas naudoti. Kai kuriais atvejais galimybės gali būti modifikuotos. Tais atvejais bus pateikiama dokumentacija.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Kaip šis pakeitimas paveiks mane, jei esu esamas klientas ir naudoju HR modulį Finansų ir operacijų infrastruktūroje ir Dynamics 365 Human Resources per pasirinktines integracijas?

Pasirinktiniai integravimai tarp „Dynamics 365 Human Resources” ir žmogiškųjų išteklių modulio „Dynamics 365 Finance” platformoje nebebus būtini. Visi HR duomenys bus toje pačioje duomenų bazėje kaip ir kitos „Finance and Operations“ programos.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Migracija iš Dynamics 365 Human Resources į „Finance and Operations“ programas

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Mano organizacija naudoja „Dynamics 365 Human Resources” žmogiškųjų išteklių operacijoms valdyti. Ką turime suplanuoti naujos patirties perkėlimui?

Jei jūsų organizacija naudoja Dynamics 365 Human Resources bet nenaudoja jokių kitų „Finance and Operations“ programų, jūsų žmogiškųjų išteklių aplinka bus perkelta į naują infrastruktūrą. Didelė dalis šio perkėlimo proceso bus automatizuota. Procesai bus paruošti jūsų duomenų bazei perkelti ir jai sinchronizuoti su nauja infrastruktūra.

Be to, bus sukurti įrankiai, kad prieš perkeliant jūsų gamybos aplinką būtų galima patikrinti perkėlimo procesą ir jūsų duomenis bei patirtį.

Jei jūsų organizacija naudoja abu Dynamics 365 Human Resources ir kitose „Finance and Operations“ programėlėse, turėtumėte planuoti daugiau laiko patvirtinimui, kad įsitikintumėte, jog jūsų duomenys tinkamai perkelti į naują aplinką. Perkėlus į naują infrastruktūrą duomenys iš žmogiškųjų išteklių aplinkos bus sujungti su jūsų finansų ir operacijų aplinka. Tačiau nesuderinamų duomenų atvejais reikės vartotojo įvesties, kad nustatytų, kaip konfliktas turėtų būti išspręstas. Vartotojai ir administratoriai turės sutvarkyti duomenų susiejimus, kuriuose yra konfliktų, ir patikrinti perkėlimą smėlio dėžės aplinkose prieš jūsų gamybos aplinkos perkėlimą.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Mano organizacija naudoja „Human Resources“ modulį „Dynamics 365 Finance“, „Supply Chain Management“, „Commerce“ ar „Project Operations“. Ką turime suplanuoti naujos patirties perkėlimui?

Organizacijoms, kurios naudoja HR modulį „Finance and Operations“ programose, naujos funkcijos funkcijos iš Dynamics 365 Human Resources bus pritaikyti jūsų aplinkai per standartinį vienos versijos atnaujinimo procesą. Jūs galite tikėtis pamatyti naujas funkcijas jūsų aplinkoje, kai jos tampa galimos kiekviename naujinime. Funkcijų valdymą galite naudoti norėdami įjungti naujas priemones, tačiau šias priemones reikėtų patikrinti. Vadovaukitės jūsų turimais procesais, kad patikrintumėte kitus jūsų aplinkos atnaujinimus. Daugiau informacijos apie tai, kaip naujinimai taikomi programoms „Finance and Operations“, žr [Vienos versijos apžvalga](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Kada mano organizacija bus perkelta?

Kiekvienos organizacijos perkėlimas priklausys nuo dabartinės konfigūracijos ir pasirengimo perkėlimui į naują infrastruktūrą. Šios datos gali keistis.

- Organizacijos, kurios naudoja žmogiškųjų išteklių modulį „Finance and Operations“ programėlėse, gaus žmogiškųjų išteklių funkcijas Dynamics 365 Human Resources kaip įprasto vienos versijos atnaujinimo proceso dalis. Planuojama, kad naujos funkcijos bus bendrai pasiekiamos 2022 m. sausio pradžioje.
- Organizacijos, kurios šiuo metu naudoja tik „Dynamics 365 Human Resources, turės prieigą prie perkėlimo įrankio, kad galėtų pradėti testavimą ir perkėlimą 2022 metų viduryje. Dar nenustatyta data, kada būtina užbaigti perkėlimą į naują infrastruktūrą. Tačiau ji bus bent po vienerių metų po to, kai perkėlimo įrankis taps prieinamas.
- Organizacijos, kurios naudoja abu Dynamics 365 Human Resources ir kitos „Finance and Operations“ programos turės prieigą prie perkėlimo įrankių, kad galėtų pradėti testavimą ir pradėti perkėlimą nuo 2022 m. pabaigos. Dar nenustatyta data, kada būtina užbaigti perkėlimą į naują infrastruktūrą. Tačiau ji bus bent po vienerių metų po to, kai perkėlimo įrankis taps prieinamas.

Daugiau informacijos apie naujas „Dynamics 365 Human Resources” funkcijas rasite [Kas naujo ar pasikeitė Žmogiškuosiuose ištekliuose](./hr-admin-whats-new.md).

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>Mano organizacija dar ne live „Dynamics 365 Human Resources“ live. Ar turėtume pradėti naudoti žmogiškųjų išteklių modulį programose „Finance and Operations“ ar su Dynamics 365 Human Resources programėlę senoje infrastruktūroje?

Svarbios prekės, į kurias reikia atsižvelgti, yra tos personalo funkcijos ir kada jos bus prieinamos naujoje infrastruktūrose. Jei organizacijai reikia pagrindinių personalo valdymo funkcijų, tai šiuo metu galima rasti naujos infrastruktūros programėlių „Finance and Operations“ personalo modulyje. Funkcijų paritetas tarp „Finance and Operations“ programų personalo modulio ir Dynamics 365 Human Resources Tikimasi, kad programa bus išleista 10.0.25 versijoje, kuri paprastai bus pasiekiama 2022 m. kovo mėn. Integravimo priemonės, pvz., „Teams“ „Dataverse“ programa ir objekto integravimas, bus galimos vėlesniuose leidimuose.

Jei organizacijos personalo funkcijų poreikiai bus pasiekiami naujoje infrastruktūroje per laikotarpį, per kurį organizacija pradės veikti, gali būti lengviau pradėti tiesiogiai naudojant „Finance and Operations“ programų žmogiškųjų išteklių modulį. Todėl bus lengviau perkelti, nes bus atnaujintas standartinis programos naujinimas į programą, o klientas „Dynamics 365 Human Resources“ jau bus naujoje infrastruktūrose. Jei organizacija nusprendžia vykti į programą senesnėje infrastruktūrą, reikės perkelti aplinką į naują „Dynamics 365 Human Resources“ infrastruktūrą. Tai gali būti neįmanoma, jei pereisite į naują infrastruktūrą.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Aš naudoju naujas galimybes, kurios galimos tik „Dynamics 365 Human Resources” (pavyzdžiui, **Atostogos ir neatvykimas** bei **Išmokų valdymas**). Ar šios galimybės dabar bus pasiekiamos ir Finansų ir operacijų infrastruktūros žmogiškųjų išteklių modulyje?

Taip, visi moduliai iš Dynamics 365 Human Resources veiks kaip yra „Finance and Operations“ programose ir bus 100 procentų funkcijų paritetas. Vykdant bendrą perkėlimo strategiją klientams, kurie šiuo metu naudoja šias žmogiškųjų išteklių galimybes, klientų duomenys bus perkelti taip, kad jie toliau veiktų „Finance and Operations“ infrastruktūroje.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Aš naudoju naujas „Dynamics 365 Human Resources” išmokų valdymo galimybes. Sukūriau pasirinktines integracijas su HR moduliu finansų ir operacijų infrastruktūroje, kad galėčiau pasinaudoti atlyginimų mokėjimo galimybėmis naudodamas išmokų duomenis. Ar vėliau šie pasirinktiniai integravimai bus būtini?

Infrastruktūros sujungimo metu HR duomenys įkeliami į tą pačią duomenų bazę, kaip ir kitos „Finance and Operations“ programos. „Finance and Operations“ programėlių modulių integracija nebereikės.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Mano organizacija naudoja vieną ar daugiau ISV sprendimų su „Dynamics 365 Human Resources”. Ar mūsų ISV sprendimai bus perkelti automatiškai?

Kiekvieno nepriklausomo programinės įrangos tiekėjo (ISV) sprendimo perkėlimo patirtis skirsis, priklausomai nuo sprendimo integravimo metodo. „Microsoft” glaudžiai dirbs su ISV, kad būtų užtikrintas sklandus perėjimas prie naujos infrastruktūros.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Mano organizacija naudoja „LinkedIn Talent Hub” integravimą su „Dynamics 365 Human Resources”. Ar šis integravimas ir toliau veiks, kai bus baigtas infrastruktūros pakeitimas?

Ne, „LinkedIn Talent Hub” integravimas neveiks po perkėlimo į naują infrastruktūrą. „LinkedIn Talent" hub integravimo paslauga bus atmestas iš senosios „Dynamics 365 Human Resources“ infrastruktūros.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Mano organizacija naudoja Žmogiškųjų išteklių programą, skirtą „Teams”. Ar programa ir toliau veiks, kai bus baigtas infrastruktūros pakeitimas?

Taip, Žmogiškųjų išteklių programos, skirtos „Teams” ir toliau veiks po perkėlimo į naują infrastruktūrą.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Mano organizacija sukonfigūravo pasirinktinę saugą „Dynamics 365 Human Resources” platformoje. Ar mūsų pasirinktinė sauga vis dar bus taikoma, kai infrastruktūros pakeitimas bus baigtas?

Taip, pasirinktinės saugos konfigūracijos bus įtrauktos į duomenų perkėlimą į naują infrastruktūrą.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Naudojame duomenų integratorių duomenims perkelti Dynamics 365 Human Resources ir Finansų ir operacijų programėlės. Kaip bus paveikti šiuo metu integruojami duomenys?

Personalo duomenys, šiuo metu valdomi „Dynamics 365 Human Resources”, yra sinchronizuojami su „Dataverse”. Tada duomenų integratorius gali būti naudojamas vienpusei sinchronizacijai su „Finance and Operations“ programomis. Perkėlus į naują infrastruktūrą, personalo duomenys bus įtraukti į „Finance and Operations“ programas. Duomenų integratoriaus nebereikės sinchronizuoti duomenų tarp „Finance and Operations“ programų ir žmogiškųjų išteklių.

Dabartinės personalo „Dataverse” vietinių duomenų lentelės ir toliau sinchronizuos duomenis iš aplinkos naujoje infrastruktūroje. Objektai bus konvertuoti, kad palaikytų dvigubą rašymą. Bet kurie kiti duomenų integravimai, sukonfigūruoti naudojant duomenų integratorių pagal šias lenteles, skirtas kitoms „Dynamics 365” programoms, ir toliau veiks taip, kaip jie sukonfigūruoti šiuo metu.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Naudojame dvigubą rašymą, kad perkeltume HR duomenis Dataverse ir kitos „Finance and Operations“ programos. Kaip šiuo metu integruojami duomenys bus paveikti perkėlimo į naują infrastruktūrą?

HR duomenys bus įtraukti į „Finance and Operations“ programas naujos infrastruktūros aplinkoje. Tada dvigubas rašymas bus panaudotas siekiant perkelti personalo duomenims tarp naujos ir „Dataverse” aplinkos.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Sukūrėme pasirinktinius integravimus iš „Dynamics 365 Human Resources” į vieną ar daugiau išorinių sistemų. Ar mes turėsime sukurti naujus integravimus, kai bus baigtas infrastruktūros pakeitimas?

Tai priklauso nuo integravimo galinio punkto. Norėdami gauti daugiau informacijos apie integravimo technologijas, kurios yra „Finance and Operations“ programėlėse, ir kaip pasirinkti geriausią integravimo technologiją, žr.[Integracijos apžvalga](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Mes išplėtėme „Dataverse”, skirtą „Dynamics 365 Human Resources”. Ar šie plėtiniai bus perkelti automatiškai?

Jei Dynamics 365 Human Resources ir Finansų ir operacijų aplinkos, kurios bus sujungtos į aplinką naujoje infrastruktūroje, yra prijungtos prie to paties Dataverse aplinką, abi programos ir toliau bus prijungtos prie to paties Dataverse aplinka po migracijos. Todėl jokiems „Dataverse” plėtiniams nebūtinas perkėlimas.

Tačiau, jei Dynamics 365 Human Resources ir „Finance and Operations“ aplinkos šiuo metu yra prijungtos prie atskirų Dataverse aplinka, dvi Dataverse aplinkos turės būti sujungtos taip, kad jos būtų sujungtos su viena aplinka naujoje infrastruktūroje. Šiuo „Dataverse” perkėlimo atveju, „Dataverse” lentelės, kurios yra standartinės Žmogiškųjų išteklių spendimuose, gali būti sujungtos ir pakartotinai sinchronizuotos su nauja „Dataverse” aplinka. Tačiau jokie „Dataverse” aplinkos plėtiniai nebus perkeliami automatiškai, bet jie turi būti iš naujo įdiegiami naujoje aplinkoje. Jūsų „Dataverse” plėtinių valdymui rekomenduojame naudoti valdomus sprendimus. Daugiau informacijos rasite [Įžanga į sprendimus](/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Sukonfigūravome „Microsoft Power Automate” srautus ir (arba) „Microsoft Power Apps”, kad jie veiktų su „Dynamics 365 Human Resources”. Ar šie „Microsoft Power Platform” komponentai bus perkelti ir veiks automatiškai po to, kai bus baigtas infrastruktūros pakeitimas?

„Power Apps”, „Power Automate” srautai ir kiti „Microsoft Power Platform” tinkinimai yra panašūs į „Dataverse” plėtinius. Ar jos veiks automatiškai po perkėlimo į naują infrastruktūrą, priklauso nuo to, ar programėlė „Žmogiškieji ištekliai“ ir „Finance and Operations“ yra prijungtos prie to paties.Power Apps aplinka prieš migraciją.

Jei programos šiuo metu yra sujungtos su ta pačia „Power Apps” aplinka, po perkėlimo į naują infrastruktūrą jos ir toliau bus sujungtos su ta „Power Apps” aplinka. Šiuo atveju „Power Apps”, „Power Automate” srautai ir kiti „Microsoft Power Platform” tinkinimai ir toliau veiks be jokios papildomos konfigūracijos. Jūsų „Dataverse” platformos programos plėtinių valdymui rekomenduojame naudoti valdomus sprendimus. Daugiau informacijos rasite [Įžanga į sprendimus](/powerapps/developer/data-platform/introduction-solutions).

Tačiau jei žmogiškųjų išteklių programa ir finansų ir operacijų programos yra sujungtos atskirai Power Apps aplinkos, jie turės būti sujungti kaip migracijos dalis. Šiai užduočiai reikės, kad bet kurios „Power Apps” ir kiti tinkinimai būtų iš naujo įdiegti naujoje aplinkoje.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Įgalinome virtualias „Dataverse” lenteles, skirtas „Dynamics 365 Human Resources”. Kas atsitiks šioms lentelėms perkėlimo metu?

Po perkėlimo, jei naujos infrastruktūros aplinka lieka prijungta prie „Dataverse” aplinkos, kuri šiuo metu prijungta prie „Dynamics 365 Human Resources”, „Dataverse” virtualios lentelės, kurios buvo sugeneruotos šioje aplinkoje, ir toliau veiks be jokios papildomos konfigūracijos.

Tačiau, jei naujos infrastruktūros aplinka po perkėlimo yra sujungta su kita „Dataverse” aplinka, virtualias lenteles reikės atkurti naujoje „Dataverse” aplinkoje.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Sukūrėme integravimą naudodami Pretendento sekimo sistemos (ATS) API, Atlyginimų API, „Dataverse” virtualias lenteles, skirtas „Dynamics 365 Human Resources”, ar kitus „Dataverse” Žiniatinklio API objektus. Ar šie integravimai ir toliau veiks, kai bus baigtas infrastruktūros pakeitimas?

Po perkėlimo, jei naujos infrastruktūros aplinka lieka prijungta prie „Dataverse” aplinkos, kuri šiuo metu prijungta prie „Dynamics 365 Human Resources”, bet kurie integravimai, kurie buvo sukurti pagal „Dataverse” žiniatinklio API, ir toliau veiks užbaigus perkėlimą.

Tačiau, jei naujos infrastruktūros aplinka po perkėlimo yra sujungta su kita „Dataverse” aplinka, bet kurie integravimai, sukurti naudojant „Dataverse” žiniatinklio API, bus perkonfigūruoti, kad būtų galima prisijungti prie naujos „Dataverse” aplinkos.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Ar daroma įtaką „Azure” regionui, kai perkeliama mano aplinka?

Tikimasi, kad perkėlimo metu jūsų Žmogiškųjų išteklių aplinka įprastai išliks tame pačiame „Azure” regione. Vienintelė išimtis yra, jei žmogiškųjų išteklių aplinka bus sujungta su Finansų ir operacijų aplinka, esančia kitame regione. Tokiu atveju žmogiškųjų išteklių aplinka bus perkelta į „Finance and Operations“ aplinkos Azure regioną.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Mano organizacija priklauso nuo darbo eigų „Dynamics 365 Human Resources” platformoje vienam ar daugiau verslo procesų. Ar darbo eigos bus perkeltos automatiškai?

Taip, darbo eigos konfigūracijos, darbo eigos retrospektyva ir dabartinės apdorojamos darbo eigos bus perkeltos.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Kokie mokymai ir ištekliai bus galimi perkėlimo proceso pagalbai?

Bus pateikta išsami dokumentacija, aprašanti kiekvieną perkėlimo proceso veiksmą. Atsižvelgiant į poreikį, gali būti prieinami ir papildomi mokymo ištekliai, pavyzdžiui, vaizdo įrašai ir dirbtuvės.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Mano organizacija sukūrė Įrašytus rodinius „Dynamics 365 Human Resources” platformoje, kad pagerintų sąsajos tinkamumo naudoti galimybes. Ar Įrašyti rodiniai bus perkelti automatiškai?

Taip, Įrašyti rodiniai bus perkelti į naują infrastruktūrą.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Mes naudojame „Ceridian” su „Dynamics 365 Human Resources”. Ar „Ceridian” integravimas bus galimas, kai bus baigtas infrastruktūros pakeitimas? 

Integravimas su „Ceridian” bus perkeltas į algalapių API integravimą. Failų integracija, kuri šiuo metu yra Dynamics 365 Human Resources nebus perkelti į „Finance and Operations“ infrastruktūrą. Daugiau informacijos rasite [Įžanga į algalapio API](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Kaip perkėlimas paveiks tarnybos atnaujinimo procesą?

Po perkėlimo klientai turės daugiau lankstumo ALM ir tarnybos atnaujinimų požiūriu. Tarnybos naujinimai nebebus automatiškai taikomi Žmogiškųjų išteklių aplinkoms. Vietoj to, tarnyba seks Vienos versijos tarnybos naujinimo procesais ir funkcijomis. Todėl atnaujinimų konfigūravimo parinktys bus galimos naudojant LCS. Daugiau informacijos rasite [Vienos versijos apžvalga](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Kaip perkėlimas paveiks mano LCS projektą, skirtą „Dynamics 365 Human Resources”?

Perkėlus į naują infrastruktūrą, jūsų valdymas bus perkeltas Dynamics 365 Human Resources aplinkos į Finansų ir operacijų įgyvendinimo projektą LCS. Jei migracija susilieja Dynamics 365 Human Resources su esama „Finance and Operations“ aplinka, jūsų žmogiškųjų išteklių LCS projektas bus sujungtas su „Finance and Operations“ programėlės LCS diegimo projektu. Jei šiuo metu naudojate tik „Dynamics 365 Human Resources”, bus sukurtas naujas LCS diegimo projektas, o esamas Žmogiškųjų išteklių LCS projektas bus perkeltas į naują projektą.

Naujasis projektas bus to paties tipo projektas, kurį naudoja programos „Finance and Operations“. Ji turės tas pačias aplinkos valdymo funkcijas ir galimybes. Dėl daugiau informacijos rasite [„Lifecycle services“ ištekliai](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Susiejome savo užduočių įrašus su verslo procesų modeliavimo įrankiu Žmogiškuosiuose ištekliuose. Kaip verslo procesų modeliavimo įrankis bus perkeltas ir sulietas į LCS?

Verslo procesų bibliotekos LCS projektui bus perkeltos į naują Žmogiškųjų išteklių LCS projektą.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Mano organizacija šiuo metu naudoja tik „Dynamics 365 Human Resources”. Kokie ištekliai prieinami, kad mes galėtume daugiau sužinoti apie kūrimo galimybes po to, kai infrastruktūros pakeitimas bus baigtas?

Abu Microsoft Power Platform bus prieinamos ir gali būti naudojamos plėtrai. Daugiau informacijos rasite [Pagrindinio puslapio kūrimas ir tinkinimas](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Įgalinome funkcijas „Dynamics 365 Human Resources” platformoje. Ar perkėlimo metu šios funkcijos bus įgalintos automatiškai?

Tai, ar funkcija bus įjungta automatiškai naujoje infrastruktūroje, bus nusprendžiama atskirai kiekvienai funkcijai. Ši informacija bus įtraukta į funkcijų dokumentaciją.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Kas nutiks su mano BYOD duomenų baze perkėlimo metu?

„Atsineškite savo duomenų bazę” (BYOD) importavimo ir eksportavimo konfigūracijos bus perkeltos į naują infrastruktūrą.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Kas nutiks su mano „Azure Data Lake” perkėlimo metu?

Bet koks šiuo metu sukonfigūruotas eksportavimas Azure Data Lake Storage „Finance and Operations“ programose po perkėlimo išliks ta pati konfigūracija.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Šiuo metu mes naudojame „Dynamics AX 2012”. Ar šiuo metu galimi atnaujinimo įrankiai bus naudojami atnaujinti „AX” 2012 personalo modulį į „Dynamics 365 Human Resources”?

Taip. Dynamics 365 Human Resources bus įtraukta į sujungtą „Finance and Operations“ programėlių kodų bazę ir infrastruktūrą. Atnaujinimas iš Dynamics AX 2012 iki Dynamics 365 Human Resources naudos tą patį naujinimo kelią ir įrankius, kurie naudojami atnaujinant į naujausią „Finance and Operations“ programų versiją.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Mes naudojame dokumentų tvarkymą su „Dynamics 365 Human Resources”. Kas atsitiks dokumentams perkėlimo metu?

Dokumentai išliks esamoje dokumentų saugykloje. Jie bus iš naujo susieti su aplinka naujoje infrastruktūroje.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Kas atsitinka su paketinėmis užduotimis, kurias sukonfigūravome „Dynamics 365 Human Resources” po perkėlimo?

Taikomos paketinės užduotys bus automatiškai perkeltos į naują infrastruktūrą.

## <a name="licensing-impact"></a>Licencijos poveikis

Ši dokumentacija neanuliuoja ar nepakeičia jokios naudojimo teisių teisinės dokumentacijos.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Mano organizacija naudoja „Dynamics 365 Human Resources” savo žmogiškųjų išteklių operacijoms valdyti. Ar keičiasi mūsų licencijos ar kaina?

Klientai, įsigiję „Dynamics 365 Human Resources” licencijas, nebus paveikti. Šiems klientams nėra licencijavimo perkėlimo. Nebebus taikomas papildomas smėlio dėžės sandėliavimo vienetas (SKU), kuris buvo būdingas Žmogiškiesiems ištekliams. Vietoj to klientai gali nusipirkti „Finance and Operations Apps Tier 2“ smėlio dėžę už šiek tiek mažesnę kainą. Esami klientai, įsigiję žmogiškųjų išteklių smėlio dėžę, bus perkelti į „Finance and Operations Apps Tier 2“ smėlio dėžę be papildomų mokesčių.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Mano organizacija naudoja „Human Resources“ modulį „Dynamics 365 Finance“, „Supply Chain Management“, „Commerce“ ar „Project Operations“. Ar keičiasi mano licencijos ar kaina?

Esami „Dynamics 365” vartotojai ir atskirų „Dynamics 365 Finance”, „Supply Chain Management”, „Commerce” ir „Project Operations” programų vartotojai gali pasiekti Žmogiškuosius išteklius kaip dalį šių licencijų iki 2025 m. vasario arba iki tol, kol baigiasi licencijavimo sutartis, priklausomai nuo to, kuri data ankstesnė. Galite pasirinkti perkelti į Žmogiškųjų išteklių licencijas anksčiau, jei tai padės jums sutaupyti. Nuo 2025 m. vasario mėn. visi esami CSP ir EA klientai turi atsisakyti HR modulio ir įsigyti žmogiškųjų išteklių licencijas, kad galėtų pasinaudoti naujomis „Finance and Operations“ programėlėmis teikiamomis galimybėmis.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Mano organizacija yra realiuoju laiku su „Dynamics 365 Finance”, „Supply Chain Management”, „Commerce”, arba „Project Operations”. Ar reikės įsigyti papildomą aplinką infrastruktūros sujungimo palaikymui?

Papildomos aplinkos nebūtinos, kad būtų galima palaikyti infrastruktūros pokyčius.

### <a name="where-should-i-go-if-i-have-additional-questions-about-product-licensing"></a>Kur turėčiau kreiptis, jei turiu papildomų klausimų apie produkto licencijavimą?

Jei turite klausimų apie licencijavimą, daugiau informacijos galite rasti [„Biz Apps Hub” – D365 Kainodara ir licencijavimas](https://businessapplications.transform.microsoft.com/resources/pricing-and-licensing?tab=grandfathering). Jei ši informacija nepadės išspręsti jūsų problemos, atidarykite užklausą naudodami „LicenseQ”.

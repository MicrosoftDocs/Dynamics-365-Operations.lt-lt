---
title: „Dynamics 365 Human Resources” infrastruktūros sujungimo DUK
description: Šiame straipsnyje pateikiami atsakymai į dažnai užduodamus klausimus apie "Microsoft" ir finansų ir Dynamics 365 Human Resources operacijų programėlių infrastruktūros suliejimą.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fd71d728f9c97dc9e2c44a7e7a0e773be891b818
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203206"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>„Dynamics 365 Human Resources” infrastruktūros sujungimo DUK

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Kas yra Dynamics 365 Human Resources?

"Microsoft Dynamics 365 Human Resources " pateikia įrankius, kurie padeda personalo komandoms padidinti organizacinį sąsumą, transformuoti darbuotojų patirtį ir optimizuoti personalo programas, kad būtų sukurta darbo vieta, kurioje žmonės ir verslas gali dingti. Norėdami sužinoti daugiau apie Dynamics 365 Human Resources, žr. [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Transformuoti darbuotojų patirtį.** Išlaikykite aukščiausius dėstytojais ir suteikti teisę vadovams ir darbuotojams pereiti prie susijusios savitarnos patirties, kuri veikia įsipareigojimą ir didėjimo galimybes.
- **Optimizuokite personalo programas.** Sumažinti veikimo išlaidas ir sukurti žmonių centines atostogų ir neatvykimų, laiko, išmokų ir kompensacijų valdymo programas.
- **Padidinti organizacijos skirstymo pagal terminus.** Įgalinti personalą, kad būtų galima dirbti su dexterity Dataverse Microsoft Power Platform, kuris reikalingas verslui, naudojant ir centralizuoti žmonių duomenis bei lengvai išplėsti Dynamics 365 Human Resources.
- **Atrasti darbo jėgos informaciją.** Priimti duomenimis pagrįstus sprendimus, suteikia galimybę analizuoti ir vizualizuoti žmonių duomenis raiškiosiose skelbimų lentose, kurios galimos bet kuriame įrenginyje.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktūros sujungimo vertė ir privalumai

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Kas yra „Dynamics 365 Human Resources” infrastruktūros sujungimas?

Šiuo metu "Dynamics 365" yra du atskiri personalo pajėgumų rinkiniai dviejose skirtingose infrastruktūrose:

- **Dynamics 365 Human Resources**– atskira programa, vykdoma nepriklausomai infrastruktūrai. Paleidus šią programą, infrastruktūra buvo atskirta nuo kitų "Dynamics 365" operacijų programėlių. Mūsų klientai naudoja šią programą norėdami padidinti organizacijos sąsamumą, optimizuoti personalo programas, transformuoti darbuotojų patirtį ir gauti darbo jėgos žinių.
- **Personalo modulis** – senesnių pajėgumų rinkinys, kuris anksčiau buvo bendrojo operacijų licencijavimo atsargų saugojimo vieneto (SKU) dalis. Personalo modulis veikia finansų ir operacijų infrastruktūrose, kurios yra tokios pačios visose operacijų programėlėse. Šios programėlės apima "Dynamics 365 Finance" Dynamics 365 Project Operations ir Dynamics 365 Supply Chain Management. Klientai gavo personalo pajėgumus kaip "Dynamics 365" finansų arba dalį Dynamics 365 Supply Chain Management.

Per paskutinius trejus metus "Microsoft" įtraukė naujų pajėgumo ar patobulinimų prie personalo modulio. Užuot tai darę, mūsų esk norėtumėte kryptingai skirti programai Dynamics 365 Human Resources.

Uždūrdami šiuos du pajėgumų rinkinius į tą pačią infrastruktūrą, mes padėsime klientams pasinaudoti šiomis galimybėmis:

- Per pastaruosius trejus metus įtraukti patobulinimai Dynamics 365 Human Resources, įskaitant patobulintas atostogas ir neatvykimą, išmokų valdymą ir ataskaitas.
- Patobulintas išplėtimas ir galimybė Microsoft Power Platform išplėsti verslo logiką, kad būtų pritaikyti puslapiai.
- Patobulintas diegimas, atnaujinimai ir priežiūra, kurie nuosekliai priklauso nuo programos ciklo valdymo (OF), ciklo tarnybų, geografinės užimtumo ir kt.
- Daugiau darbo, nes mūsų inžinerijos komanda naudoja bendrai naudojamas paslaugas, įrankius ir sumažino platformas.

Šis perėjimas paveiks klientus, kurie šiuo metu naudoja arba senesnį Dynamics 365 Human Resources personalo modulį.

## <a name="glossary-of-terms-used-in-this-faq"></a>Šiame DUK naudojamų terminų žodynėlis

- **Dynamics 365 Human Resources**– mūsų dabartinis ir būsimas produktas, kuris teikia personalo pajėgumus rinkoje.
- **Personalo modulis** – senesnių galimybių rinkinys, anksčiau licencijuotas naudojant suvienodintas operacijas, siūlant. Galimybės įgalintos, kai klientui priklauso "Dynamics 365" finansai arba .Dynamics 365 Supply Chain Management
- **Finansų ir operacijų infrastruktūra** – programavimo architektūra, kurią naudoja operacijos, įskaitant Dynamics 365 finansus, Dynamics 365 Supply Chain Management ir Dynamics 365 Project Operations. Ši infrastruktūra yra ta, kuri bus naudojama į priekį. Šiame DUK terminas sulieta *infrastruktūra* nurodo finansų ir operacijų aplinką.
- **Personalo infrastruktūra** – programavimo architektūra, anksčiau naudota programai Dynamics 365 Human Resources. Infrastruktūros suliejimo projektas iškelia Dynamics 365 Human Resources į finansų ir operacijų infrastruktūrą. Autonominė infrastruktūra bus nutraukta.

## <a name="general-questions-about-the-infrastructure-merge"></a>Bendrieji klausimai apie infrastruktūros suliejimą

### <a name="will-customers-lose-any-features-or-capabilities"></a>Ar klientai praras visas funkcijas ar galimybes?

Mūsų tikslas yra sumažinti šio perėjimo poveikį klientams. Mes nepašalinsime jokių funkcijų ar galimybių. Bus funkcinis ryšys tarp personalo Dynamics 365 Human Resources modulio ir jo. Jei priemonė yra abiejose infrastruktūrose, bus Dynamics 365 Human Resources naudojama patirtis.

### <a name="will-the-user-experience-change"></a>Ar vartotojas keisis?

Vartotojų patirtis atitiks standartinį "Dynamics 365" platformos patirtį. Nors bendra skelbimų lentos ir meniu patirtis liks panaši, ji bus sulygiuota su standartine "Dynamics 365" finansų programos patirtimi. Naršymo metu bus ir moduliai, ir darbo sritys, leidžiama naudoti parankinius ir kt. Darbo Dynamics 365 Human Resources sritys, pavyzdžiui, Personalo **valdymas ir** Žmonės **·**, bus sulietos į finansų ir operacijų infrastruktūrą. Ateityje nauji pajėgumai bus pristatyti naudojant funkcijų valdymą, kuris leis klientams peržiūrėti naujas funkcijas ir nuspręsti, kurias iš jų naudos. Daugiau informacijos ieškokite Funkcijų valdymo [peržiūra ir](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) Vartotojo sąsajos [dokumentai](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json).

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Kada bus užbaigtas Dynamics 365 Human Resources infrastruktūros suliejimas?

Infrastruktūros suliejimas sulietas etapais, kad klientams būtų galima suplanuoti ir atlikti reikalingus veiksmus. Pradėjome taikyti pajėgumus "Dynamics 2021" 2 leidimo bangoje. Mes planuojame baigti visas produkto kūrimo pastangas šiam projektui iki 2022 m. pradžios bangos 2 pabaigos. Nepamirškite, kad laiko juostos gali būti keičiamos. Naujausia informacija pateikta [paleidimo planuose](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Koks mokymas ir ištekliai bus galimi padėti susieti infrastruktūrą?

Mes teikiame dokumentus, kurie išsamiai aprašo kiekvieną infrastruktūros suliejimo proceso žingsnį. Mes teiksime papildomus mokymo išteklius, pvz., vaizdo įrašus ir dirbtuves, kurie padės klientams ir partneriams pereiti sklandžiai.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Ar baigus infrastruktūros suliejimą bus pakeisti programavimo pajėgumai?

Norėdami daugiau sužinoti apie programavimo galimybes, žr. ["Kurti ir pritaikyti pagrindinį puslapį"](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

## <a name="feature-availability-questions"></a>Funkcijos pasiekiamumo klausimai

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>Ar LinkedIn talentų centro integravimas veikia su finansų ir operacijų infrastruktūra?

Ne, LinkedIn Talent Hub integravimas nebus susietos infrastruktūros dalis. Viešoji prašymo programavimo sąsaja (API) galima sukurti integravimą su įdarbinimo ir pretendento sekimo sprendimais. Klientai, kurie planuoja naudoti LinkedIn Talent Hub turi dirbti su savo Microsoft partneriu, kad jie būtų integruotis naudodami pateiktą API. Daugiau informacijos apie pretendento sekimo sistemos (ATS) integravimo API ieškokite pretendento [sekimo sistemos integravimo API įžangoje](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Ar baigus sąlają Dynamics 365 Human Resources bus galima naudoti tik dabar turimas galimybes (pvz., atostogų valdymą ir išmokų valdymą)?

Taip. Visi Dynamics 365 Human Resources programų pajėgumai yra pateikiami finansų ir operacijų infrastruktūrai. Priemonės bus prieinamos etapais. Naujausia informacija apie funkcijos pasiekiamumą susietai infrastruktūrai, reguliariai peržiūrėkite paleidimo [planus](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Ar Baigus infrastruktūrą bus užbaigtas Dynamics 365 Human Resources Ceri integraciją naudoti?

Cerikaitė kuriama V2 integracija, naudojanti Dynamics 365 Human Resources algalapio API. Šiuo metu egzistuojama failų integracija Dynamics 365 Human Resources nebus perkelta į finansų ir operacijų infrastruktūrą. Daugiau informacijos rasite [Įžanga į algalapio API](./hr-admin-integration-payroll-api-introduction.md).

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Ar bus įtrauktas pretendento sekimas ir (arba) darbuotojo funkcijų lenta?

Ankstesniuose leidimuose sukūrėme ATS integravimo API, siekiant įgalinti partnerius ir klientus kurti ATS integravimą su personalo ištekliais. Papildomos ATS susijusios funkcijos tampa galimos 2022 bangoje 1. Toliau tęsime šių API tęsime būsimuose leidimuose.

Personalo funkcijos, kurios šiuo metu yra finansų ir operacijų infrastruktūrose, apima tam tikrą įdarbinimo valdymo funkciją, kurios nėra Dynamics 365 Human Resources. Kai infrastruktūros suliejimas baigtas, ši funkcija bus pasiekiama visiems personalo klientams. Šios funkcijos suteikia supaprastintosią ATS funkciją. Tačiau mes planuojame išplėsti šią funkciją ateityje. Klientai, kuriems reikia daugiau patobulintos funkcijos, gali pasinaudoti partnerio ATS integrais. Daugiau informacijos apie ATS integravimo API ieškokite pretendento sekimo [sistemos integravimo API įžangoje](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Ar "Dynamics AX 2012" naujinimo įrankiai bus naudojami atnaujinus personalo modulį AX programoje 2012 Dynamics 365 Human Resources?

Taip. Atnaujinti iš "Dynamics AX 2012 Dynamics 365 Human Resources ", kad būtų naudojamas tas pats naujinimo maršrutas ir įrankiai, naudojami siekiant atnaujinti į naujausią kitų "Dynamics 365" operacijų programėlių versiją, pvz., "Dynamics 365 Finance" arba "Dynamics 365"Dynamics 365 Supply Chain Management.

Daugiau informacijos apie perkėlimą į finansų ir operacijų infrastruktūrą ieškokite DUK dėl [personalo klientų perkėlimo](./customer-migration.md).

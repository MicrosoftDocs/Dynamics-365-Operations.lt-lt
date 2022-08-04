---
title: Personalo parengimas finansų ir operacijų infrastruktūrose
description: Šiame straipsnyje paaiškinamas naujos "Microsoft Dynamics 365 Human Resources " gamybos aplinkos parengimo procesas finansų ir operacijų infrastruktūrose.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15060d8bdd598476081c22d7280319da3db0cb31
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178419"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>Personalo parengimas finansų ir operacijų infrastruktūrose

_**Taikoma: Finansų** ir operacijų programos infrastruktūros žmogiškieji ištekliai_ 

> [!NOTE]
> Nuo 2022 m. liepos mėn. naujų personalo aplinkos negali būti sukurtos atskiras personalo infrastruktūrą ir Microsoft Dynamics naujus ciklo tarnybų (LCS) projektus. Klientai gali įdiegti personalo aplinkas finansų ir operacijų infrastruktūrose.

Šiame straipsnyje paaiškinamas naujos "Microsoft Dynamics 365 Human Resources " gamybos aplinkos parengimo procesas finansų ir operacijų infrastruktūrose.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradedant kurti naują aplinką, turi būti įdiegti šie būtinieji sąlyga:

- Personalo pirkote naudodami debesies sprendimų teikėjo (CSP) ar įmonės architektūros (ŠIUO metu) sutartį. Jei turite esamą "Dynamics 365" licenciją, kurioje jau yra personalo paslaugų planas, ir negalite atlikti šiame straipsnyje nurodytų veiksmų, susisiekite su palaikymo tarnyba.
- Visuotinis administratorius užsiregistravo vykdymo [Microsoft Dynamics ciklo tarnybose (LCS)](https://lcs.dynamics.com) ir sukūrė naują finansų ir operacijų projektą.

## <a name="provision-a-human-resources-trial-environment"></a>„Human Resources” bandomosios aplinkos parengimas

> [!NOTE]
> Nuo 2022 m. balandžio mėn. autonominėje programoje nebus galima naudoti personalo bandomojo aplinkos. Potencialūs klientai, kurie nori įvertinti personalo pajėgumus finansų ir operacijų programėlei, gali naudoti nemokamą 30 dienų bandomąjį naudojimą ir demonstracinius duomenis. "Dynamics 365 Finance" apims personalo pajėgumus, kurie bus naudojami finansų infrastruktūrai, suliedami atskirą programą. Norėdami gauti daugiau informacijos, žr [. personalo pasiūlymų suliejimą klientams kartu](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Daugiau informacijos apie "Dynamics 365" finansų bandymus [ieškokite nuoseklioje vadove](../fin-ops-core/fin-ops/get-started/before-you-buy.md).

## <a name="plan-human-resources-environments"></a>Planuokite „Human Resources“ aplinkas

Prieš jums sukuriant pirma „Human Resources“ aplinką, turėtumėte atsargiai suplanuoti aplinkos poreikius savo projektui. Pagrindinis personalo abonementas apima dvi aplinkas: gamybos aplinką ir numatytąją standartinę priėmimo tikrinimo (Sandbox) aplinką. Atsižvelgiant į jūsų projekto sudėtingumą, galima pasirinkti pirkti papildomas aplinkas, kurios palaikys projektų veiklą.

Papildomose pasirinktinose aplinkose yra keletas aplinkybių:

- **Duomenų perkėlimas** – duomenų perkėlimo veikla įgalina jūsų sandų dėžės aplinką naudoti tikrinant projekto metu. Kai turite papildomą aplinką, duomenų perkėlimo veikla gali būti tęsiama, kai tikrinimo ir konfigūravimo veiklos vienu metu vyksta kitoje aplinkoje.
- **Integravimas** – konfigūruokite ir patikrinkite integravimą, kuris gali apimti vietinius integravimą ar pasirinktinį integravimą, pvz., algalapio, pretendento sekimo sistemų ar išmokų sistemų ir teikėjų.
- **Mokymas** – gali būti reikalinga atskira aplinka, sukonfigūruota su mokymo duomenų rinkinys, kad galėtumėte traukinys savo darbuotojams naudoti naująją sistemą. 
- **Kelių etapų projektas** – gali reikėti papildomos aplinkos, kad būtų galima palaikyti konfigūraciją, duomenų perkėlimą, bandymą ar kitą veiklą projekto etape, suplanuotame po pradinio projekto etapo.
- **Kūrimas** – finansų ir operacijų infrastruktūrose dabar galite išplėsti sprendimą ir kurti savo pritaikymus. Kiekvienas programuotojas turi naudoti savo programavimo aplinką. Norėdami gauti daugiau informacijos, žr. [Deploy ir pasiekite programavimo aplinkas](/fin-ops-core/dev-itpro/dev-tools/access-instances).
- **AUKSINĖ** – naujų diegimų atveju paprastai naudojama atskira AUKSINĖ aplinka, kuri saugoma nesudėvusi konfigūracijoje ir duomenų perkėlme. Šią aplinką galima naudoti visoje diegimo metu, norint atnaujinti kitas aplinkas. Jis bus naudojamas kuriant naują gamybos aplinką, kurioje yra pagrindinė konfigūracija ir duomenų perkėlimas. Negalite įdiegti gamybos aplinkos finansų ir operacijų infrastruktūros, kol nebaigėte tiesioginio pasirengimo proceso. Daugiau informacijos rasite Pasiruošti [vykti.](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live)

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> Nagrinėkime savo aplinkas rekomenduojame naudoti tokį būdą:
>
> - Naudokite numatytąją standartinę priėmimo tikrinimo (anksčiau – Sandbox) aplinką ar kitą aplinką, norėdami atlikti tarpą prieš tęsdami.
> - Saugokite išsamų perkėlimo kontrolinį sąrašą, kuriame būtų kiekvienas duomenų paketas, kurio reikia norint perkelti galutinius duomenis į gamybos aplinką per tiesioginio perkėlimo galutinę laikotarpį. Ši rekomendacija itin svarbi, jei neturite atskiros AUKSinės aplinkos, kurioje saugosite savo konfigūracijas.
> - Naudokite numatytąją standartinę priėmimo tikrinimo (anksčiau – "Sandbox") aplinką arba kitą pakopų 2 arba aukštesnę aplinką kaip viso projekto tikrinimo aplinką. Jei jums reikia papildomų aplinkos, jūsų organizacija gali jas pirkti už papildomas išlaidas.

## <a name="create-an-lcs-project"></a>LCS projekto kūrimas

Norėdami naudoti LCS „Human Resources“ aplinkoms valdyti, pirma turite sukurti LCS projektą. Jei perkeliate savo personalo aplinką į finansų ir operacijų infrastruktūrą, turite sukurti naują LCS projektą, skirtas finansų ir operacijų programoms. Daugiau informacijos ieškokite Personalo [aplinkos perkėlimas](hr-admin-migrate-overview). Jei jau turite LCS projektą kitoms finansų ir operacijų programoms, galite įgalinti personalo funkcijas funkcijų valdymo **darbo** srityje. Daugiau informacijos žr. [Funkcijų valdymo apžvalga](/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Kai naujas klientas pasirašo personalo valdymo abonementą, abonemente yra diegimo projekto darbo sritis. Klientui suaktyvinus tarnybą, nuomininkų administratorius turi prisiregistruoti <https://lcs.dynamics.com> naudodamas nuomininko abonementą. Projekto darbo sritis automatiškai sukuriama organizacijai. Norėdami gauti daugiau informacijos, finansų [ir operacijų programėlių klientams žr. vykdymo ciklo tarnybas](/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs) (LCS).

> [!NOTE]
> Norint užtikrinti sėkmingą parengimą, abonementas, kurį naudojate personalo aplinkai konfigūruoti, turi būti priskirtas sistemos administratoriaus vaidmeniui arba sistemos pritaikymo priemonės vaidmeniui aplinkoje, **·** **·** Power Apps kuri susieta su personalo aplinka. Daugiau informacijos apie tai, kaip priskirti saugos vaidmenis vartotojams, žr Microsoft Power Platform. Vartotojo saugos [konfigūravimas pagal išteklius](/power-platform/admin/database-security).

Kad būtų galima pradėti diegti aplinkas, būtina užbaigti LCS projekto įsk. procesą. Daugiau informacijos rasite Project [onboarding](/fin-ops-core/dev-itpro/lifecycle-services/project-onboarding). Daugiau informacijos apie LCS naudojimą ieškokite ciklo [tarnybų (LCS) vartotojo vadove](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide).

## <a name="deploy-human-resources-environments"></a>Personalo aplinkos diegimas

Norint debesyje įdiegti finansų ir operacijų programėles, įskaitant personalo valdymo programėles, reikia suprasti aplinką ir abonementą, kuriam iš naujo diegiate, kam galima atlikti užduotis ir kokius duomenis bei pritaikymus turite valdyti. Diegiant naujas aplinkas rekomenduojame vietoj įvardytąjį vartotoją naudoti tarnybos abonementą. Daugiau informacijos apie tai, kaip diegti aplinkas finansų ir operacijų infrastruktūrose, ieškokite debesies [diegimo apžvalga](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview).

Norėdami finansų ir operacijų infrastruktūrose įdiegti personalo gamybos aplinką, turite užbaigti tiesioginio pasirengimo procesą. Daugiau informacijos rasite Pasiruošti [vykti.](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live) Šiame procese įtrauktas LCS abonemento įvertinimas. Daugiau informacijos ieškokite Abonemento [įvertinyme](/fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator).

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Integruoti Microsoft Power Platform su personalo ištekliais

Microsoft Power Platform suteikia "Dynamics 365" programų pajėgumų komplektą per administravimo Power Platform centrą. Galite integruoti ir išplėsti personalo duomenų naudojimą naudodami Microsoft Power Platform. Informacijos, kaip integruoti personalo išteklius, ieškokite integravimą Microsoft Power Platform su [Microsoft Power Platform finansų ir operacijų programėle](/fin-ops-core/dev-itpro/power-platform/overview).

## <a name="supported-geographies"></a>Palaikomi geografiniai grafikai

Informacijos apie kalbas ir geografinius diagramas, kurias palaiko žmogiškieji ištekliai, [ieškokite Visuotiniai pagal dizainą: sužinoti apie palaikomas šalis ir kalbas](https://dynamics.microsoft.com/availability-reports/).

## <a name="grant-access-to-the-environment"></a>Prieigos prie aplinkos suteikimas

Pagal numatytuosius nustatymus, aplinką sukūręs visuotinis administratorius turi prie jos prieigą. Papildomiems programos vartotojams prieiga turi būti aiškiai suteikta. Turite pridėti vartotojų ir priskirti jiems tinkamus vaidmenis „Human Resources“ aplinkoje. Daugiau informacijos rasite [Naujų vartotojų kūrimas](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ir [Vartotojų priskyrimas saugos vaidmenims](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).

## <a name="additional-resources"></a>Papildomi ištekliai
Daugiau informacijos apie tai, kaip naudoti ir valdyti LCS projektus finansų ir operacijų programų infrastruktūrose, galite naudoti šiuos išteklius:

- [„Lifecycle Services“ ištekliai](/fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [„Lifecycle Services“ (LCS) vartotojo vadovas](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Visuotinio savitarnos paslaugos diegimo apžvalga](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [Duomenų bazės perkėlimo operacijų pagrindinis puslapis](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Dynamics 365 Human Resources kliento perkėlimas į finansų ir operacijų infrastruktūrą
description: Šiame straipsnyje aprašomas kliento "Microsoft" perkėlimas Dynamics 365 Human Resources į finansų ir operacijų infrastruktūrą.
author: twheeloc
ms.date: 10/25/2022
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
ms.openlocfilehash: 4df9a68ea0128378224bf77bd66423fd2e13fa55
ms.sourcegitcommit: e5b290bac7e8f468167caa1a5607aac6eac9aaea
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2022
ms.locfileid: "9760368"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources kliento perkėlimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Klientų perkėlimas – tai klientų duomenų bazės perkėlimo "perkėlimas" į finansų ir operacijų infrastruktūrą "lifto ir pamainos perkėlimas". Naudojamas automatinis perkėlimo įrankis. Rezultatas yra nauja finansų ir operacijų aplinka, kuri naudoja kliento personalo duomenų bazę.

## <a name="prerequisites"></a>Būtinieji komponentai

### <a name="user-access-and-permissions"></a>Vartotojo prieiga ir teisės

- Ciklo Microsoft Dynamics tarnybų vartotojas turi turėti organizacijos **administratoriaus** vaidmenį.
- Vartotojas turėtų turėti galimybę [kurti Azure DevOps projektus](/azure/devops/organizations/projects/create-project) arba naudoti esamą Azure DevOps projektą.
- Vartotojas turi turėti prieigą prie asmeninės [prieigos Azure DevOps saugos atpažinimo](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) ženklo kūrimo arba turėti atpažinimo ženklą, kurį galima naudoti.

### <a name="dataverse-environment-backup-sandbox"></a>Dataverse aplinkos atsarginė kopija (sandbox)

 - Pasirinktinai, bet rekomenduojama: atnaujinkite esamą personalo sandų dėžės aplinką naudodami personalo gamybos aplinkos kopiją.
 - Sukurkite naują Dataverse aplinką naudodami administravimo Power Platform centrą.
 - Nukopijuokite esamą Dataverse aplinką, susietą su atskira personalo programa, į aplinką, kurią sukūrėte ankstesniu veiksmu.

> [!NOTE]
> Kai pridedate duomenų bazę, įsitikinkite, kad parinktis **Įgalinti "Dynamics 365** " programėles nustatyta kaip **Taip**. Išsamesnės informacijos ieškokite [Aplinkos paruošimas Power Platform](hr-cust-migration.md#prepare-a-power-platform-environment)

### <a name="dataverse-capacity"></a>Dataverse Pajėgumų

1. Naudokite administravimo **centro** suvestinės puslapį Power Platform, norėdami patikrinti, ar [Dataverse saugykloje](/power-platform/admin/finance-operations-storage-capacity) yra pakankamai pajėgumų aplinkos kopijai.
2. Jei nepakanka pajėgumų, naudokite nurodymą, kaip [atlaisvinti vietos saugykloje,](/power-platform/admin/free-storage-space) kad būtų galima sumažinti bendrą suvartojimą. Klientai taip pat gali [įtraukti papildomą saugojimo pajėgumą](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Kliento perkėlimo procesas

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Kurti žmogiškųjų išteklių perkėlimo ciklo tarnybų projektą

Pirmas veiksmas yra sukurti naują finansų ir operacijų vykdymo projektą vykdymo ciklo tarnybose. Klientas turės esamą personalo ciklo tarnybų projektą. Esamos personalo aplinkos bus perkeltos į naują finansų ir operacijų diegimo projektą.

Norėdami sukurti naują projektą, atlikite šiuos veiksmus.

1. Prisijunkite prie ciklo tarnybų kaip visuotinis administratorius arba nurodytas tarnybos abonemento vartotojas.
2. Ciklo tarnybų pagrindiniame puslapyje pasirinkite Kurti **/naujas (+).**.
3. Pasirinkite finansų ir operacijų programėles kaip produktą.
4. Lauke Projekto **paskirtis** pasirinkite **Diegimas**.
5. Įveskite projekto pavadinimą ir aprašymą.
6. Pasirinktinio **projekto tipo lauke pasirinkite** "Microsoft" **Dynamics 365 Human Resources perkėlimas**.
7. Pažymėti žymės langelį norint sutikti su sąlygomis.
8. Pasirinkite **Kurti**.

Sukūrę naują ciklo tarnybų projektą, pagal šiuos veiksmus jį nustatykite ir sukonfigūruokite.

1. Norėdami **baigti projektą, pasirinkite** Projekto įėjimas į darbo lentą. Daugiau informacijos rasite Project [onboarding](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md).

    - Pasirinkti tą patį regioną kaip ir dabartinės aplinkos. Šis pasirinkimas neturės įtakos perkėlimą.
    - Jei norite naudoti senstelėjusias sistemas, pasirinkite **Kita**.

2. Baigti projekto parametrus. Atlikdami šį veiksmą turėtumėte sukonfigūruoti interneto SharePoint biblioteką ir "Azure" ryšius, Azure DevOps jei jų reikia. Norėdami gauti daugiau informacijos, žr [. ciklo tarnybų (LCS) vartotojo vadovą](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Klientai gali naudoti esamą projektą Azure DevOps ir susijusį asmeninės prieigos saugos atpažinimo ženklą. Jei naudojamas esamas projektas, su projektu susijusios konfigūracijos yra galimos automatiškai ir gali būti peržiūrėtos jų tikslumu.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Perkelti personalo sand. aplinką

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Pasirengimas perkelti sand. aplinką

Sukūrus naują ciklo tarnybų projektą ir baigus projekto įsk. procesą, būsite pasiruošę perkelti pirmąją aplinką. Prieš pradedant šį procesą rekomenduojame atnaujinti sandbox aplinką, kurią norite perkelti iš savo gamybos aplinkos į atskirą infrastruktūrą.

#### <a name="prepare-a-power-platform-environment"></a>Aplinkos paruošimas Power Platform

> [!NOTE]
> Šis veiksmas taikomas tik perkelti sand. į dėžę. Kai perkeliate gamybos aplinką, esama administravimo Power Platform centro aplinka, pridėta prie gamybos aplinkos, bus perkelta. Kai įtraukiate duomenų bazę, įsitikinkite, kad nustatytas **mygtukas Įgalinti "Dynamics 365** " programėles kaip **Taip**. 

- "Power Platform" administravimo centre sukurkite aplinką su duomenų baze [,](/power-platform/admin/create-environment#create-an-environment-with-a-database) kurioje būtų galima perkelti sandus, arba pasirinkite esamą aplinką.
- [Kopijuoti aplinką](/power-platform/admin/copy-environment), kad būtų atnaujinta Power Platform susiejimui naudojama aplinka.

#### <a name="migrate-the-sandbox-environment"></a>Perkelti sandbox aplinką

1. Prisijunkite prie ciklo tarnybų kaip visuotinis administratorius arba nurodytas tarnybos abonemento vartotojas.

    > [!NOTE]
    > Rekomenduojame naudoti įvardytąjį vartotojo abonementą. Prisiregistravęs vartotojas turi turėti projekto **savininko** arba **aplinkos** tvarkytuvo saugos vaidmenį atskirą personalo ciklo tarnybų projekte.

2. Atidaryti naujai sukurtą personalo perkėlimo projektą.
3. Peržiūrėkite ir baikite atitinkamus perkėlimo metodologijos ir projekto parengimo etapus.
4. Projekto skelbimų skelbimų srityje Numatytoji **: standartinė priėmimo tikrinimo** sritis pasirinkite **Perkelti personalą**.
5. Norėdami perkelti **sritį pasirinktyje** Pasirinkti aplinką pasirinkite atitinkamą ciklo tarnybų projektą ir šaltinį Personalo aplinka (iš šaltinio atskirą personalo valdymo programą).
6. Įjunkite **schemą su Power Platform nauja** aplinka ir pasirinkite reikiamą Power Platform aplinką. Tada rinkitės **Kitas**.
7. Baikite **diegimo parametrų (finansų ir operacijų – sandbox)** vedlį, kad patvirtintumėte informaciją ir kliento išjungimą, tada pasirinkite **Diegti**.

Aplinkos būsena rodys eigą. Būsena bus pakeista iš įkėlimo į **įdiegtį** **.** **·**

> [!NOTE]
> Gamybos sritis bus galima tik tada, kai bus baigtas tiesioginio projekto pasirengimo kontrolinis sąrašas. Daugiau informacijos rasite Pasiruošti [vykti.](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md)

#### <a name="considerations-and-assumptions"></a>Aplinkybės ir prielaidos

Personalo sandų dėžės aplinka yra nuomininko, kuris turi šias savybes, ciklo tarnybų projekte:

- Personalo sandų dėžės aplinka nėra susieta su esama sulieta aplinka. Vienu metu galima perkelti tik vieną nurodytą personalo aplinkos perkėlimą.
- Šiuo metu leidžiamų sandų dėžės aplinkos skaičius pagrįstas personalo licencijavimo parinktimi. Jei nuomininkui buvo nupirkta pakankamai licencijų, **papildomos** sand. aplinka bus nurodyta projekto srityje Aplinkos.
- Būtina perkelti į to paties tipo aplinkas. Kitaip tariant, galima perkelti tik sand. į sand. lauką arba perkėlimą į gamybą.

    > [!NOTE]
    > Kai nustatoma gamybos arba sandbox būsena, atsižvelgiama tik į personalo aplinkos tipus. Jei aplinkos yra netinkamai suskirstytos į kategorijas (t. y. gamybos aplinka pažymėta kaip sandbox aplinka arba sandbox aplinka pažymėta kaip gamybos aplinka), susisiekite su palaikymo tarnyba.

- Jei perkėlimas nesėkmingas, bus rodomas klaidos pranešimas apie triktį **ir bus galimas** mygtukas Naikinti. Naudokite šį mygtuką, norėdami panaikinti nepavykusį perkėlimą. Tada galite pakartotinai miguoti aplinką.

#### <a name="validate-the-sandbox-migration"></a>Tikrinti sand. dėžės perkėlimą

Sėkmingai atlikus sandbox perkėlimo procesą, sukurkite išsamų tikrinimo planą, kad patvirtintumėte ir atjungtumėte visus verslo procesus.

Prieš pradėdami tikrinti, patikrinkite toliau nurodytą informaciją:

- Patvirtinkite, kad perkelta aplinka pasiekiama naudojant sugeneruotą URL.
- Patvirtinkite, kad vartotojai gali pasiekti perkeltą sand. dėžę.
- Patvirtinkite, Dataverse kad galima pasiekti aplinką, susietą su perkelta sandbox aplinka.
- Vietoje patikrinkite skirtingus duomenis, kad patvirtintumėte, jog yra naujausia duomenų.
- Užbaikite svarbius verslo procesus patikrinti.
- Patvirtinkite, kad jūsų saugos strategijos taikomos.
- Patvirtinkite, kad paketinės užduotys paleistos, kaip tikėtasi.

Neturite nuotolinio darbalaukio prieigos prie perkeltos sand. langelio. Galite naudoti savitarnos pajėgumus ir įrankius, norėdami atlikti šiuos veiksmus savo 2+ pakopų sandbox aplinkoje:

- Prieiga prie " [Azure" SQL duomenų bazės](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database).
- Prieiti prie [žurnalo failų](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files).
- Naudokite ["Perfmon" įrankius](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools).
- Įjungti [/ išjungti priežiūros režimą](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs).
- Iš naujo [paleisti tarnybas](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services).
- Sukonfigūruokite [Regression komplekto automatizavimo įrankį](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool).

Norėdami gauti daugiau informacijos, peržiūrėkite [DUK apie savitarnos diegimą](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Perkelti personalo gamybos aplinką

Baigę perkelti ir galioti sandbox aplinką, atlikite šiuos veiksmus norėdami perkelti gamybos aplinką.

#### <a name="prerequisites"></a>Būtinieji komponentai

- Abonemento įvertinimas turi būti atliktas.
- Turėtų būti atliktas pasirengimo [pereiti](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) į darbą vertinimas.

#### <a name="migrate-the-production-environment"></a>Perkelti gamybos aplinką

1. Prisijunkite prie ciklo tarnybų kaip visuotinis administratorius arba nurodytas tarnybos abonemento vartotojas.

    > [!NOTE]
    > Rekomenduojame naudoti įvardytąjį vartotojo abonementą. Prisiregistravęs vartotojas turi turėti projekto **savininko** arba **aplinkos** tvarkytuvo saugos vaidmenį ciklo tarnybų projekte.

2. Atidarykite naują personalo perkėlimo projektą.
3. Peržiūrėkite ir baikite atitinkamus perkėlimo metodologijos ir projekto parengimo etapus.
4. Projekto skelbimų srityje gamybos **srityje pasirinkite Perkelti** personalą **·**.
5. Norėdami perkelti **sritį pasirinkite** atitinkamą ciklo tarnybų projektą ir šaltinį personalo aplinkai (iš šaltinio atskirą personalo valdymo programos). Tada rinkitės **Kitas**.
6. Baikite **diegimo parametrų (finansų ir operacijų – sandbox)** vedlį, kad patvirtintumėte informaciją ir kliento išjungimą, tada pasirinkite **Diegti**.

Aplinkos būsena rodys diegimo eigą. Būsena bus pakeista iš įkėlimo į **įdiegtį** **.** **·**

#### <a name="post-migration-considerations"></a>Po perkėlimo aplinkybės

- Savo aplinkai pritaikyti [naujausius](/fin-ops-core/fin-ops/get-started/quality-updates) kokybės naujinimus.
- Jei naudojate virtualias lenteles [, perkonfigūruokite](hr-admin-integration-common-data-service-virtual-entities.md) galinius punktus.
- Perkonfigūruoti dvigubo rašymo integravimą. Įvertinti, kuriuos objektus reikia įgalinti.
- Apsvarstykite galimybę naudoti virtualias lenteles norėdami pakeisti dvigubo rašymo funkciją integravimui.

#### <a name="dual-write-integration"></a>Dvigubo rašymo integravimas

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Nustatyti dvigubo Microsoft Power Platform rašymo integravimą

1. Eikite į Power Platform administravimo centrą ir kairiajame **naršyme** pasirinkite Aplinkos.
2. Pasirinkite anksčiau nukopijuotą / atnaujinti aplinką ir patvirtinkite, kad būsena **parengta**.
3. Eikite į ciklo tarnybas ir patvirtinkite, kad perkėlimo projekto būsena **įdiegta**.
4. Perkeltoje aplinkoje pasirinkite Išsami informacija **, norėdami** peržiūrėti papildomą informaciją ir [nustatyti dvigubo rašymo programą](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. **Dvigubo rašymo programos konfigūracijos** srityje pažymėkite žymės langelį, kad būtų sutarta susieti ir sinchronizuoti duomenis tarp duomenų bazių, o tada pasirinkti **Konfigūruoti**.
6. Kai pranešimų langas praneša apie sėkmingą dvigubo rašymo konfigūraciją, pasirinkite **Gerai**.
7. Išsamioje informaciją galite stebėti konfigūracijos eigą.
8. Baigę konfigūruoti pasirinkite Susieti su aplinka **, kurioje Power Platform** sinchronizuojami galimi duomenų objektai.
9. Kai būsena nurodo, kad aplinkos sėkmingai susietos, eikite į administravimo centrą, Power Platform kad peržiūrėtumėte ir pasirinktumėte atitinkamus duomenų objektus.
10. Kairiajame lange pasirinkite " **Dynamics 365" programėlių \> ištekliai**.
11. Patvirtinkite, kad dvigubo rašymo personalo programos būsena yra **Įgalinta**.
12. Pasirinkite dvigubo rašymo personalo programą, tada pasirinkite **Diegti**.
13. Diegimo dvigubo **rašymo Dynamics 365 Human Resources programos** srityje pasirinkite atitinkamą aplinką, kurioje norite diegti paketą.
14. Pažymėkite žymės langelį, norėdami sutikti su paslaugų sąlygomis, tada pasirinkite **Diegti**.
15. "Dynamics 365" programos aplinkoje **diegimo metu** bus diegiama būsena. Jis bus atnaujintas į **Įdiegtas**, kai bus baigta diegti.

##### <a name="review-and-apply-a-dual-write-solution"></a>Peržiūrėti ir taikyti dvigubo rašymo sprendimą

1. Naujoje finansų ir operacijų aplinkoje eikite į Duomenų valdymo **dvigubo \> rašymo.**
2. Pasirinkite **Taikyti sprendimą**.
3. Srityje pasirinkite Dynamics įdiegtus **sprendimus**, dvigubo **rašymo programų pagrindines objektų schemas** ir **Dynamics 365 Human Resources schemas**. Tada pasirinkite **Taikyti**. Pranešime patvirtinama, kad sprendimas yra taikomas. Sėkmingai pritaikius sprendimą, bus rodomos visos galimos lentelių schemos.
4. Peržiūrėkite galimas lentelės schemas, norėdami pasirinkti ir paleisti integravimą naudodami dvigubo rašymo funkciją.
5. Kai vykdote dvigubo rašymo integravimą pirmą kartą lentelės žemėlapiams, pažymėkite žymės langelį **Pradinis** sinchronizavimas. Jei yra esamas integravimas iš šaltinio personalo aplinkos, **paleidus** lentelių žemėlapių integravimą nereikia pažymėti žymės langelio Pradinis sinchronizavimas.

#### <a name="recommended-practices"></a>Rekomenduojamos praktikos

Šiame skyriuje pateikiamos rekomendacijos, kaip perkelti iš autonominės infrastruktūros į finansų ir operacijų infrastruktūrą.

- Rekomenduojame dirbti su partneriu, kad būtų galima Microsoft Dynamics gauti pagalbos dėl personalo aplinkos perkėlimo.
- Planuokite tinkamą laiką, kada reikia atlikti viso vartotojo priėmimo testą (UAT) sand laukelio perkeltoje aplinkoje.
- Planuokite ir dokumentuokite išsamius veiksmus, perkeliant integravimą į perkeltą aplinką.
- Sukurti išsamų kontrolinį sąrašą, siekiant apibrėžti jūsų perkėlimo procesą.
- Planuokite atitinkamą prasto darbo laiką savo verslui, kol jie bus perkelti.
- Rekomenduojame "FastTrack" pasirinktiems klientams dirbti su jų "FastTrack" sprendimų architektu, kad padėtų prižiūrėti perkėlimo procesą.
- Rekomenduojame prieš pirmą perkėlimą atnaujinti savo sandbox aplinką atskira infrastruktūra. Į šį atnaujinimą turi būti Dataverse įtraukta jūsų aplinka, sujungta su sandbox aplinka, į kurią planuojate perkelti.
- Rekomenduojame diegiant, perkelti ir kurti ciklo tarnybų projektą naudoti paslaugos sąskaitą.
- Planuokite atnaujinti sandbox aplinką UAT tikrinimo pagal paskutinį bendrą pasiekiamumą (GA) paleidimą. Daugiau informacijos ieškokite [aplinkybėse](hr-infrastructure-merge.md#considerations).

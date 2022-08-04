---
title: Egzemplioriaus kopijavimas
description: Galite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS), kad nukopijuotumėte „Microsoft Dynamics 365 Human Resources“ duomenų bazę į smėlio dėžės aplinką.
author: twheeloc
ms.date: 07/22/2020
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
ms.openlocfilehash: 935c2e6cb45df193e6cbf70634f3561154c6fe38
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178540"
---
# <a name="copy-an-instance"></a>Egzemplioriaus kopijavimas

_**Taikoma:** žmogiškieji ištekliai autonominėje infrastruktūrose_ 

> [!NOTE]
> Nuo 2022 m. birželio mėn. personalo aplinkas galima įdiegti tik finansų ir operacijų programų infrastruktūrose. Daugiau informacijos ieškokite Finansų [ir operacijų infrastruktūros personalo parengimas](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finansų ir operacijų infrastruktūra nepalaiko kopijos egzemplioriaus funkcijos. Galite įdiegti naujas aplinkas ir naudoti duomenų bazės perkėlimą kopijoms kurti. Daugiau informacijos apie savitarnos diegimą ieškokite savitarnos [diegimo apžvalga](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md). Daugiau informacijos apie duomenų bazės perkėlimą finansų ir operacijų infrastruktūrose ieškokite duomenų bazės [perkėlimo operacijų pagrindinį puslapį](../fin-ops-core/dev-itpro/database/dbmovement-operations.md).

Galite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS), kad nukopijuotumėte „Microsoft Dynamics 365 Human Resources“ duomenų bazę į smėlio dėžės aplinką. Jei turite kitą smėlio dėžės aplinką, taip pat galite kopijuoti duomenų bazę iš šios aplinkos į tikslinę smėlio dėžės aplinką.

Kad nukopijuotumėte egzempliorių, atminkite šiuos patarimus:

- „Human Resources“ egzempliorius, kurį norite perrašyti, turi būti smėlio dėžės aplinka.

- Aplinkos, iš kurių ir į kurias kopijuojate, privalo būti tame pačiame regione. Negalite kopijuoti skirtinguose regionuose.

- Turite būti paskirties aplinkos administratorius, kad nukopijavę egzempliorių galėtumėte prisijungti prie jo.

- Kai kopijuojate „Human Resources“ duomenų bazę, nenukopijuojate elementų (programų arba duomenų), esančių „Microsoft Power Apps“ aplinkoje. Norėdami gauti informacijos apie tai, kaip kopijuoti „Power Apps“ aplinkos elementus, žr. [Aplinkos kopijavimas](/power-platform/admin/copy-environment). „Power Apps“ egzempliorius, kurį norite perrašyti, turi būti smėlio dėžės aplinka. Norėdami pakeisti „Power Apps“ gamybos aplinką į smėlio dėžės aplinką, turite būti visuotinis nuomotojo administratorius. Daugiau informacijos apie „Power Apps“ aplinkos keitimą žr. [Egzemplioriaus keitimas](/dynamics365/admin/switch-instance).

- Jei kopijuojate egzempliorių į savo smėlio dėžės aplinką ir norite integruoti savo smėlio dėžės aplinką į „Dataverse”, privalote pasirinktinius laukus iš naujo taikyti „Dataverse” lenteles. Žr. [Taikyti pasirinktinius laukus „Dataverse”](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>„Human Resources“ duomenų bazės kopijavimo poveikis

Šie įvykiai įvyksta, kai kopijuojate „Human Resources“ duomenų bazę:

- Kopijavimo procesu trinama esama duomenų bazė, esanti paskirties aplinkoje. Kai kopijavimo procesas baigtas, negalėsite atkurti esamos duomenų bazės.

- Paskirties aplinka nebus pasiekiama, kol nebus baigtas kopijavimo procesas.

- Dokumentai, esantys „Microsoft Azure“ didelių dvejetainių objektų saugykloje, nėra kopijuojami iš vienos aplinkos į kitą. Todėl bet kurie pridėti dokumentai ir šablonai nebus kopijuojami ir liks šaltinio aplinkoje.

- Visi vartotojai, išskyrus tuos, kurių saugos vaidmuo "Sistemos administratorius" ir kiti vidinių paslaugų vartotojų abonementai yra negalimi. Vartotojas administratorius gali panaikinti duomenis prieš tai, kai kitiems vartotojams neleidžiama grįžti į sistemą.

- Bet kuris vartotojas su sistemos administratoriaus saugumo vaidmeniu gali atlikti būtinus konfigūravimo keitimus, pvz., iš naujo sujungti integravimo galinius punktus su konkrečiomis tarnybomis arba konkrečiais URL.

## <a name="copy-the-human-resources-database"></a>„Human Resources“ duomenų bazės kopijavimas

Norėdami atlikti šią užduotį, pirmiausia nukopijuokite egzempliorių, tada prisijunkite prie „Microsoft Power Platform“ administravimo centro, kad nukopijuotumėte savo „Power Apps“ aplinką.

> [!WARNING]
> Kai kopijuojate egzempliorių, duomenų bazė ištrinama paskirties egzemplioriuje. Šio proceso metu paskirties egzemplioriaus naudoti negalima.

1. Prisijunkite prie LCS ir pasirinkite LCS projektą, kuriame yra egzempliorius, kurį norite kopijuoti.

2. LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**.

3. Pasirinkite kopijuotiną egzempliorių ir pasirinkite **Kopijuoti**.

4. Užduočių srityje **Kopijuoti egzempliorių** pasirinkite egzempliorių, kurį norite perrašyti, tada – **Kopijuoti**. Lauką Kopijavimo **būsena atnaujinsite** į **Baigta**.

   ![[Pasirinkite norimą perrašyti egzempliorių.](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Pažymėkite **„Power Platform“** ir prisijunkite prie „Microsoft Power Platform“ administravimo centro.

   ![[Pasirinkti Power Platform.](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Pasirinkite kopijuotiną „Power Apps“ aplinką ir pasirinkite **Kopijuoti**.

Daugiau informacijos apie aplinkos kopijavimą Power Apps žr. Kopijuokite [aplinką](/power-platform/admin/copy-environment#copy-an-environment-1).

7. Kai kopijavimo procesas baigtas, prisijunkite prie paskirties egzemplioriaus ir įjunkite „Dataverse“ integravimą. Daugiau informacijos ir instrukcijų žr. [„Dataverse“ integravimo konfigūravimas](./hr-admin-integration-common-data-service.md).

## <a name="data-elements-and-statuses"></a>Duomenų elementai ir būsenos

Kai kopijuojate „Human Resources“ egzempliorių, šie duomenų elementai nebus nukopijuoti:

- El. pašto adresai lentelėje **LogisticsElectronicAddress**

- Paketinių užduočių retrospektyva lentelėse **BatchJobHistory**, **BatchHistory** ir **BatchConstraintHistory**

- Paprastųjų pašto siuntų protokolo (SMTP) slaptažodis lentelėje **SysEmailSMTPPassword**

- SMTP perdavimo serveris lentelėje **SysEmailParameters**

- Spausdinimo valdymo parametrai lentelėse **PrintMgmtSettings** ir **PrintMgmtDocInstance**

- Aplinkai būdingi įrašai lentelėse **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ir **BatchServerGroup**

- Dokumentų priedai, esantys „DocuValue“ lentelėje. Šiuose prieduose yra „Microsoft Office“ šablonų, perrašytų šaltinio aplinkoje

- Ryšio eilutės lentelėje **PersonnelIntegrationConfiguration**

Kai kurie iš šių elementų negali būti kopijuojami, nes jie būdingi tam tikrai aplinkai. Pavyzdžiai apima įrašus **BatchServerConfig** ir **SysCorpNetPrinters**. Kiti elementai nėra nukopijuoti dėl palaikymo bilietų apimties. Pvz.:

- Dubliuoti el. laiškai gali būti siunčiami, nes SMTP vis dar yra įgalintas vartotojo priėmimo bandymų (smėlio dėžės) aplinkoje.

- Negaliojantys integravimo pranešimai gali būti siunčiami, nes paketinės užduotys vis dar yra įgalintos.

- Vartotojai gali būti įgalinti prieš administratoriams atliekant valymo po atnaujinimo veiksmus.

Taip pat, šios būsenos keičiasi, kai nukopijuojate egzempliorių:

- Visi vartotojai, išskyrus tuos, kurių saugos vaidmuo Sistemos administratorius nustatytas kaip **Išjungta**.

- Visos paketinės užduotys, išskyrus kai kurias sistemos užduotis, yra nustatytos kaip **Sulaikyti**.

## <a name="environment-admin"></a>Aplinkos administratorius

Visi paskirties smėlio dėžės aplinkos vartotojai, įskaitant administratorius, pakeičiami šaltinio aplinkos vartotojais. Prieš tai kai nukopijuojate egzempliorių, įsitikinkite, kad šaltinio aplinkoje esate Administratorius. Jei jūsų nėra, baigę kopijuoti, negalite įeiti į paskirties sandų dėžės aplinką.

Visi ne administratoriaus teises turintys vartotojai paskirties smėlio dėžės aplinkoje yra išjungti, kad būtų užkirstas kelias nepageidaujamiems prisijungimams smėlio dėžės aplinkoje. Jei reikia, administratoriai gali iš naujo įgalinti vartotojus.

## <a name="apply-custom-fields-to-dataverse"></a>Taikyti pasirinktinius laukus „Dataverse”

Jei kopijuojate egzempliorių į savo smėlio dėžės aplinką ir norite integruoti savo smėlio dėžės aplinką į „Dataverse”, privalote pasirinktinius laukus iš naujo taikyti „Dataverse” lenteles.

Kiekvienam pasirinktiniam laukui, rodomam „Dataverse” lentelėse, atlikite šiuos veiksmus:

1. Eikite į pasirinktinį lauką ir pasirinkite **Redaguoti**.

2. Anuliuokite **Įgalinti** lauką kiekvienam cdm_* objektui, kuriam įjungtas pasirinktinis laukas.

3. Pasirinkite **Taikyti pakeitimus**.

4. Dar kartą pasirinkite **Redaguoti**.

5. Pasirinkite **Įgalinti** lauką kiekvienam cdm_* objektui, kuriam įjungtas pasirinktinis laukas.

6. Dar kartą pasirinkite **Taikyti pakeitimus**.

Anuliavimo, pakeitimų taikymo, perrinkimo ir pakeitimų taikymo iš naujo procesas ragina schemos „Dataverse” atnaujinimus, kad būtų įtraukti pasirinktiniai laukai.

Norėdami gauti daugiau informacijos apie pasirinktinius laukus, žr. [Darbas su pasirinktiniais laukais ir jų kūrimas](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).

## <a name="see-also"></a>Taip pat žiūrėkite

[„Human Resources“ parengimas](hr-admin-setup-provision.md)</br>
[Egzemplioriaus šalinimas](hr-admin-setup-remove-instance.md)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

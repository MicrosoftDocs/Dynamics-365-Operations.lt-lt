---
title: Egzemplioriaus kopijavimas
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009892"
---
# <a name="copy-an-instance"></a>Egzemplioriaus kopijavimas

Galite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS), kad nukopijuotumėte „Microsoft Dynamics 365 Human Resources“ duomenų bazę į smėlio dėžės aplinką. Jei turite kitą smėlio dėžės aplinką, taip pat galite kopijuoti duomenų bazę iš šios aplinkos į tikslinę smėlio dėžės aplinką.

Norėdami nukopijuoti egzempliorių, turite užtikrinti, kad atitinkamos šios sąlygos:

- „Human Resources“ egzempliorius, kurį norite perrašyti, turi būti smėlio dėžės aplinka.

- Aplinkos, iš kurių kopijuojate, turi būti tame pačiame regione. Negalite kopijuoti skirtinguose regionuose.

- Turite būti paskirties aplinkos administratorius, kad nukopijavę egzempliorių galėtumėte prisijungti prie jo.

- Kai kopijuojate „Human Resources“ duomenų bazę, nenukopijuojate elementų (programų arba duomenų), esančių „Microsoft PowerApps“ aplinkoje. Norėdami gauti informacijos apie tai, kaip kopijuoti „PowerApps“ aplinkos elementus, žr. [Aplinkos kopijavimas](https://docs.microsoft.com/power-platform/admin/copy-environment). „PowerApps“ egzempliorius, kurį norite perrašyti, turi būti smėlio dėžės aplinka. Norėdami pakeisti „PowerApps“ gamybos aplinką į smėlio dėžės aplinką, turite būti visuotinis nuomotojo administratorius. Daugiau informacijos apie „PowerApps“ aplinkos keitimą žr. [Egzemplioriaus keitimas](https://docs.microsoft.com/dynamics365/admin/switch-instance).

## <a name="effects-of-copying-a-human-resources-database"></a>„Human Resources“ duomenų bazės kopijavimo poveikis

Šie įvykiai įvyksta, kai kopijuojate „Human Resources“ duomenų bazę:

- Kopijavimo procesu trinama esama duomenų bazė, esanti paskirties aplinkoje. Kai kopijavimo procesas baigtas, negalėsite atkurti esamos duomenų bazės.

- Paskirties aplinka nebus pasiekiama, kol nebus baigtas kopijavimo procesas.

- Dokumentai, esantys „Microsoft Azure“ didelių dvejetainių objektų saugykloje, nėra kopijuojami iš vienos aplinkos į kitą. Todėl visi pridėti dokumentai ir šablonai nebus nukopijuoti ir liks šaltinio aplinkoje.

- Visi vartotojai išskyrus administratoriaus teises turintį vartotoją ir kiti vidinių paslaugų vartotojų klientai nebus pasiekiami. Todėl administratoriaus teises turintis vartotojas gali panaikinti arba paslėpti duomenis, prieš tai, kai prie sistemos galės prisijungti kiti vartotojai.

- Administratoriaus teises turintis vartotojas turi atlikti būtinus konfigūravimo keitimus, pvz., iš naujo sujungti integravimo galinius punktus su konkrečiomis tarnybomis arba konkrečiais URL.

## <a name="copy-the-human-resources-database"></a>„Human Resources“ duomenų bazės kopijavimas

Norėdami atlikti šią užduotį, pirmiausia nukopijuokite egzempliorių, tada prisijunkite prie „Microsoft Power Platform“ administravimo centro, kad nukopijuotumėte savo „PowerApps“ aplinką.

> [!WARNING]
> Kai kopijuojate egzempliorių, duomenų bazė ištrinama paskirties egzemplioriuje. Šio proceso metu paskirties egzemplioriaus naudoti negalima.

1. Prisijunkite prie LCS ir pasirinkite LCS projektą, kuriame yra egzempliorius, kurį norite kopijuoti.

2. LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**.

3. Pasirinkite kopijuotiną egzempliorių ir pasirinkite **Kopijuoti**.

4. Užduočių srityje **Kopijuoti egzempliorių** pasirinkite egzempliorių, kurį norite perrašyti, tada – **Kopijuoti**. Palaukite, kol lauko **Kopijuoti būseną** reikšmė bus atnaujinta į **Baigta**.

   ![[Perrašytino egzemplioriaus pasirinkimas](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Pažymėkite **„Power Platform“** ir prisijunkite prie „Microsoft Power Platform“ admininstravimo centro.

   ![[„Power Platform“ pasirinkimas](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Pasirinkite kopijuotiną „PowerApps“ aplinką ir pasirinkite **Kopijuoti**.

7. Kai kopijavimo procesas baigtas, prisijunkite prie paskirties egzemplioriaus ir įjunkite „Common Data Service“ integravimą. Daugiau informacijos ir instrukcijų žr. [„Common Data Service“ integravimo konfigūravimas](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

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

Kai kurie šių elementų nėra nukopijuoti, nes jie yra tik aplinkai būdingi. Pavyzdžiai apima įrašus **BatchServerConfig** ir **SysCorpNetPrinters**. Kiti elementai nėra nukopijuoti dėl palaikymo bilietų apimties. Pavyzdžiui, pasikartojančius el. laiškus galima siųsti, nes SMTP vis dar yra įjungtas vartotojo priėmimo testavimo (smėlio dėžės) aplinkoje, netinkamo integravimo pranešimai gali būti siunčiami, nes vis dar yra įgalintos paketinės užduotys, o vartotojai gali būti įjungti prieš administratoriams atliekant valymo veiksmus po atnaujinimo.

Be to, kai kopijuojate egzempliorių, pasikeičia šios būsenos:

- Visi vartotojai, išskyrus administratorių, nustatyti kaip **Išjungtas**.

- Visos paketinės užduotys, išskyrus kai kurias sistemos užduotis, yra nustatytos kaip **Sulaikyti**.

## <a name="environment-admin"></a>Aplinkos administratorius

Visi paskirties smėlio dėžės aplinkos vartotojai, įskaitant administratorius, pakeičiami šaltinio aplinkos vartotojais. Prieš kopijuodami egzempliorių, patikrinkite, ar esate paskirties aplinkos administratorius. Jei nesate, baigę kopijuoti, negalėsite prisijungti prie paskirties smėlio dėžės aplinkos.

Visi ne administratoriaus teises turintys vartotojai paskirties smėlio dėžės aplinkoje yra išjungti, kad būtų užkirstas kelias nepageidaujamiems prisijungimams smėlio dėžės aplinkoje. Jei reikia, administratoriai gali iš naujo įgalinti vartotojus.

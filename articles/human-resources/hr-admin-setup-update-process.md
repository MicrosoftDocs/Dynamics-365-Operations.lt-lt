---
title: Atnaujinimo procesas
description: „Microsoft Dynamics 365 Human Resources“ yra tipiška programinės įrangos nuomos paslauga („SaaS“), teikianti nepertraukiamus, bekontakčius paslaugų naujinimus, skirtus programai ir platformai keisti.
author: twheeloc
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 25889f9d4a7ffb4f155b7b7c12ec3b21a44a4710
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178450"
---
# <a name="update-process"></a>Atnaujinimo procesas

_**Taikoma:** žmogiškieji ištekliai autonominėje infrastruktūrose_ 

> [!NOTE]
> Nuo 2022 m. liepos mėn. naujų personalo aplinkos negali būti sukurtos atskiras personalo infrastruktūrą ir Microsoft Dynamics naujus ciklo tarnybų (LCS) projektus. Klientai gali įdiegti personalo aplinkas finansų ir operacijų infrastruktūrose. Daugiau informacijos ieškokite Finansų [ir operacijų infrastruktūros personalo parengimas](/hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finansų ir operacijų programos infrastruktūros naujinimo ir karštųjų pataisų procesas skiriasi nuo autonominio personalo naujinimo ir karštųjų pataisų proceso. Daugiau informacijos apie atnaujinimo procesą ieškokite Procesas, [skirtas pereiti prie vėliausio finansų ir operacijų naujinimo](../fin-ops-core/dev-itpro/migration-upgrade/upgrade-latest-update.md). Norėdami gauti daugiau informacijos apie karštąsias pataisas, [žr. atsisiuntimo naujinimus iš ciklo tarnybų (LCS)](/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs.md). 

„Microsoft Dynamics 365 Human Resources“ yra puiki programinės įrangos nuomos paslauga („SaaS“), teikianti nepertraukiamus, bekontakčius paslaugų naujinimus. Šiuose naujinimuose yra programos ir platformų keitimų, kurie dažnai teikia esminius paslaugų pagerinimus, įskaitant reguliavimo naujinimus.

## <a name="update-policy"></a>Naujinimo strategija

Naujinimai išleidžiami reguliariais intervalais visoms aplinkoms. „Human Resources“ palaikoma atsižvelgiant į [„Microsoft Lifecycle“ strategiją](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kuri numato nuoseklias ir prognozuojamas palaikymo pasiekiamumo gaires.

## <a name="release-cadence"></a>Leidimo intervalai 

„Human Resources“ naujinimai taikomi visoms aplinkoms automatiškai. „Human Resources“ teikia dviejų tipų leidimus:

- **Paslaugų naujinimai**: naujinimai, kuriuose yra klaidų taisymai ir naujos funkcijos, vykdomi kas dvi savaites. Į aptarnavimo naujinimus taip pat įtraukiami taikomi platformos naujinimai, kai jie išleidžiami. Norėdami gauti daugiau informacijos apie platformos paleidimus, žr [. "Kas naujo" arba "Platform" atnaujinimų metu pakeista](../fin-ops-core/dev-itpro/get-started/whats-new-home-page.md). Naujinimų visuotinis diegimas etapų metu yra tarp regionų. Daugiau informacijos apie atnaujinimus ieškokite [Kas naujo arba pakeista Dynamics 365 Human Resources](hr-admin-whats-new.md).

- **„Dataverse“ sprendimų naujinimai**: šie naujinimai vykdomi maždaug kas šešios savaitės, jei reikia. Juose yra naujų objektų ir esamų objektų, esančių „Dataverse“, keitimų. Šie atnaujinimai išleidžiami į tuos pačius regionus kaip ir dviejų savaičių atnaujinimai, jie truks apie šešias savaites, kad dubliuoti visuose duomenų centruose. Sprendimų naujinimai sutampa arba nesutampa su paslaugų naujinimais, vykdomais kas dvi savaites.

> [!NOTE]
> Sprendimų naujinimai pasiekiami visuose duomenų centruose, kai jie išleidžiami. Jei nenorite laukti, kol naujinimai bus dubliuojami automatiškai, galite rankiniu būdu taikyti šiuos naujinimus bet kuriai aplinkai bet kuriame duomenų centre.

Kai reikia, Žmogiškieji ištekliai pateikia šiuos pataisymų tipus:

- **Tikslinimas (karštosios pataisos)**: klaidų pataisos, kurios gali būti vykdomos kartu su paslaugų naujinimo kas dvi savaites leidimu arba atskirai nuo jo

- **Avarinis taisymas**: aktyvios ir reaktyviosios karštosios pataisos, kurios yra įprastai vykdomos atskirai, gali apimti tik konfigūracijų arba kodo keitimus, siekiant išspręsti tiesiogines svetainės problemas ir gali būti taikomos atskirai nuo paslaugų naujinimo kas dvi savaites leidimo

Leidimai yra peržiūrimi, tikrinami ir patvirtinami vidinėje aplinkoje. Kai atsijungiama nuo komponavimo versijų, jos bus įdiegtos gamybai.

## <a name="release-cadence-exceptions-in-2021"></a>Numatomi išleidimo intervalai 2021 m.

Norint atsiskaityti už atostogas, toliau pateiktas 2021 m. lapkričio ir gruodžio mėn. leidimų grafikas.

- Lapkričio mėn. leidimas: lapkričio 1 d. – lapkričio 14 d.
- Gruodžio mėn. leidimas: lapkričio 29 d. – gruodžio 12 d.
 
Dviejų savaičių išleidimo intervalai bus tęsiami kaip įprasta 2022 m. sausio 10 d.

## <a name="communications"></a>Kontaktai

Galite sužinoti, kas rengiama programai „Human Resources“ ir ką išleidome, šiose vietose:

- [„Dynamics 365 Human Resources“ veiksmų planas](https://dynamics.microsoft.com/roadmap/human-resources/)

- [„Dynamics 365“ leidimo planai](/dynamics365/release-plans/)

- [Kas nauja arba pasikeitė „Dynamics 365 Human Resources“](hr-admin-whats-new.md)

- [Problemų ieška portale „Lifecycle Services“ (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (tik su platforma susijusioms klaidoms)

- [„Human Resources“ tinklaraštis](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [„Human Resources“ „Yammer“ bendruomenė](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Peržiūros funkcijos smėlio dėžės aplinkoje

Galite patikrinti peržiūros funkcijas smėlio dėžės aplinkoje prieš įjungdami jas savo gamybos aplinkoje. Daugiau informacijos apie naujų funkcijų įjungimą žr. temoje [Funkcijų valdymo apžvalga](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Visos naujos funkcijos išlieka peržiūroje bent 30 dienų ir paprastai 30–60 dienų. Pagrindinės funkcijos paprastai pasiekiamos kiekvienų metų spalį ir balandį po peržiūros laikotarpio. Kai tik pradedame naujas galimybes darbo srityje **Funkcijų valdymas**, galite jas įjungti. Kai kurios funkcijos gali būti pagal numatytuosius parametrus.

Kartais integrali funkcija bus įjungta pagal numatytuosius nustatymus ir jos nebus galima išjungti (pavyzdžiui, darbo sritis Funkcijų valdymas).

Kai funkcija jau pasiekiama, ją galima įjungti arba išjungti gamybos aplinkose. Darbo sritis **Funkcijų valdymas** nurodo, kada peržiūros funkcija taps privaloma. Paprastai ši data yra spalio 1 d. arba balandžio 1 d., siekiant suderinti su pusmečio leidimų planais. Negalite išjungti privalomų funkcijų. Kol ji taps privaloma, šią funkciją galite įjungti ir išjungti visose aplinkose.

Primygtinai rekomenduojame peržiūrėti funkcijas, esančias smėlio dėžės arba bandomojoje aplinkoje. Geriausia sukurti savo esamos gamybos aplinkos arba duomenų bazės kopiją į smėlio dėžės aplinką, kad galėtumėte gauti visą naujų funkcijų su savo duomenimis patirtį.

Norėdami gauti daugiau informacijos apie smėlio dėžės aplinkos parengimą, žr. [„Human Resources“ projekto parengimas](hr-admin-setup-provision.md). Norėdami pašalinti tikrinimo aplinką, žr. [Egzemplioriaus šalinimas](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Pranešimas apie klaidas

Tikrindami peržiūros funkcijas arba išbandydami naujas galimybes, galite aptikti elementų, neveikiančių taip, kaip tikėtasi. Praneškite apie klaidas per [„Microsoft Dynamics 365“ palaikymą](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Taip pat žiūrėkite

[„Dynamics 365“ ir „Power Platform“ leidimo planai](/dynamics365/release-plans)</br>
[Kas nauja ar pasikeitė programoje „Dynamics 365 Human Resources”](hr-admin-whats-new.md)</br>
[Programinės įrangos ciklo strategija](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

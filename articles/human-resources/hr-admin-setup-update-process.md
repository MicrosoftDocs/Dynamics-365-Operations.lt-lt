---
title: Atnaujinimo procesas
description: „Microsoft Dynamics 365 Human Resources“ yra tipiška programinės įrangos nuomos paslauga („SaaS“), teikianti nepertraukiamus, bekontakčius paslaugų naujinimus, skirtus programai ir platformai keisti.
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
ms.openlocfilehash: 267682f4497bacf70f93840a948d0e525dfa4aa1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092206"
---
# <a name="update-process"></a>Atnaujinimo procesas

„Microsoft Dynamics 365 Human Resources“ yra puiki programinės įrangos nuomos paslauga („SaaS“), teikianti nepertraukiamus, bekontakčius paslaugų naujinimus. Šiuose naujinimuose yra programos ir platformų keitimų, kurie dažnai teikia esminius paslaugų pagerinimus, įskaitant reguliavimo naujinimus.

## <a name="update-policy"></a>Naujinimo strategija

Naujinimai išleidžiami reguliariais intervalais visoms aplinkoms. „Human Resources“ palaikoma atsižvelgiant į [„Microsoft Lifecycle“ strategiją](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kuri numato nuoseklias ir prognozuojamas palaikymo pasiekiamumo gaires.

## <a name="release-cadence"></a>Leidimo intervalai

„Human Resources“ naujinimai taikomi visoms aplinkoms automatiškai. „Human Resources“ teikia dviejų tipų leidimus:

- **Paslaugų naujinimai**: savaitiniai naujinimai, kuriuose yra klaidų taisymai ir naujos funkcijos. Į paslaugos naujinimus taip pat įtraukiami taikomi platformų naujinimai, kai jie išleidžiami. Norėdami sužinoti, kada platformų naujinimai išleidžiami, žr. [3 lentelė: platformų leidimai](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases). Savaitiniai naujinimai paprastai išleidžiami trečiadieniais. Daugiau informacijos apie savaitinius naujinimus žr. [Kas nauja arba pasikeitė programoje „Dynamics 365 Human Resources“](https://docs.microsoft.com/dynamics365/talent/whats-new).

    Visi palaikomi duomenų centrai teikia naujinimus kas savaitę, nebent nurodyta kitaip. Savaitiniai naujinimai paprastai prasideda trečiadienį ir baigiasi iki sekmadienio. JAV, Australija, Europa, JK, Azija ir Kanada yra įtraukiamos į savaitinius naujinimus. 

- **„Common Data Service“ sprendimų naujinimai**: šie naujinimai vykdomi maždaug kas šešios savaitės, jei reikia. Juose yra naujų objektų ir esamų objektų, esančių „Common Data Service“, keitimų. Šie naujinimai išleidžiami tuose pačiuose regionuose kaip ir savaitiniams naujinimams, bei užtrunka apie šešias savaites, kol jie dubliuojami visuose duomenų centruose. Sprendimų naujinimai sutampa arba nesutampa su savaitiniais paslaugų naujinimais.

Šioje lentelėje parodytas pavyzdinis grafikas:

| Savaitė | Naujinimo tipas |
| --- | --- |
| 1 | Paslaugų naujinimas (visi regionai) |
| 2 | Paslaugų naujinimas (visi regionai) + sprendimų naujinimas (1 savaitės regionai) |
| 3 | Paslaugų naujinimas (visi regionai) + sprendimų naujinimas (2 savaitės regionai) |
| 4 | Paslaugų naujinimas (visi regionai) + sprendimų naujinimas (3 savaitės regionai) |
| 5 | Paslaugų naujinimas (visi regionai) + sprendimų naujinimas (4 savaitės regionai) |
| 6 | Paslaugų naujinimas (visi regionai) + sprendimų naujinimas (5 savaitės regionai) |
| 7 | Paslaugų naujinimas (visi regionai) + sprendimų naujinimas (6 savaitės regionai) |
| 8 | Paslaugų naujinimas (visi regionai) |

> [!NOTE]
> Sprendimų naujinimai pasiekiami visuose duomenų centruose, kai jie išleidžiami. Jei nenorite laukti, kol naujinimai bus dubliuojami automatiškai, galite rankiniu būdu taikyti šiuos naujinimus bet kuriai aplinkai bet kuriame duomenų centre.

Kai reikia, „Human Resources“ taip pat teikia šiuos taisymų tipus:

- **Tikslinimas (karštosios pataisos)**: klaidų pataisos, kurios gali būti vykdomos kartu su savaitiniu paslaugų naujinimo leidimu arba atskirai nuo jo

- **Avarinis taisymas**: aktyvios ir reaktyviosios karštosios pataisos, kurios yra įprastai vykdomos atskirai, gali apimti tik konfigūracijų arba kodo keitimus, siekiant išspręsti tiesiogines svetainės problemas ir gali būti taikomos atskirai nuo savaitinio paslaugų naujinimo leidimo

Leidimai yra peržiūrimi, tikrinami ir patvirtinami vidinėje aplinkoje. Kai atsijungiama nuo komponavimo versijų, jos bus įdiegtos gamybai.

## <a name="exceptions-in-2019"></a>2019 m. išimtys

Šiomis datomis numatomos išimtys įprastame leidimų grafike:

| Data | Aprašymas |
| --- | --- |
| Lapkričio 25 d. savaitė | Nėra naujinimų |
| Gruodžio 16 d. savaitė | Tik smulkūs naujinimai |
| Gruodžio 23 d. savaitė | Nėra naujinimų |
| Gruodžio 30 d. savaitė | Nėra naujinimų |

## <a name="communications"></a>Kontaktai

Galite sužinoti, kas rengiama programai „Human Resources“ ir ką išleidome, šiose vietose:

- [„Dynamics 365 Human Resources“ veiksmų planas](https://dynamics.microsoft.com/roadmap/talent/)

- [„Dynamics 365“ leidimo planai](https://docs.microsoft.com/dynamics365/release-plans/)

- [Kas nauja arba pasikeitė „Dynamics 365 Human Resources“](hr-admin-whats-new.md)

- [Problemų ieška portale „Lifecycle Services“ (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (tik su platforma susijusioms klaidoms)

- [„Human Resources“ tinklaraštis](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [„Human Resources“ „Yammer“ bendruomenė](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Peržiūros funkcijos smėlio dėžės aplinkoje

Galite patikrinti peržiūros funkcijas smėlio dėžės aplinkoje prieš įjungdami jas savo gamybos aplinkoje. Daugiau informacijos apie naujų funkcijų įjungimą žr. temoje [Funkcijų valdymo apžvalga](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Visos naujos funkcijos išlieka peržiūroje bent 30 dienų ir paprastai 30–60 dienų. Pagrindinės funkcijos paprastai pasiekiamos kiekvienų metų spalį ir balandį po peržiūros laikotarpio. Kai tik pradedame naujas galimybes darbo srityje Funkcijų valdymas, galite jas įjungti. Kai kurios funkcijos gali būti pagal numatytuosius parametrus.

Kartais integrali funkcija bus įjungta pagal numatytuosius nustatymus ir jos nebus galima išjungti (pavyzdžiui, darbo sritis Funkcijų valdymas).

Kai funkcija jau pasiekiama, ją galima įjungti arba išjungti gamybos aplinkose. Darbo sritis Funkcijų valdymas nurodo, kada peržiūros funkcija taps privaloma. Paprastai ši data yra spalio 1 d. arba balandžio 1 d., siekiant suderinti su pusmečio leidimų planais. Negalite išjungti privalomų funkcijų. Kol ji taps privaloma, šią funkciją galite įjungti ir išjungti visose aplinkose.

Primygtinai rekomenduojame peržiūrėti funkcijas, esančias smėlio dėžės arba bandomojoje aplinkoje. Geriausia sukurti savo esamos gamybos aplinkos arba duomenų bazės kopiją į smėlio dėžės aplinką, kad galėtumėte gauti visą naujų funkcijų su savo duomenimis patirtį.

Norėdami gauti daugiau informacijos apie smėlio dėžės aplinkos parengimą, žr. [„Human Resources“ projekto parengimas](hr-admin-setup-provision.md). Norėdami pašalinti tikrinimo aplinką, žr. [Egzemplioriaus šalinimas](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Pranešimas apie klaidas

Tikrinandami peržiūros funkcijas arba išbandandydami naujas galimybes, galite aptikti elementų, neveikiančių taip, kaip tikėtasi. Praneškite apie klaidas per [„Microsoft Dynamics 365“ palaikymą](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Taip pat žiūrėkite

- [„Dynamics 365“ ir „Power Platform“ leidimo planai](https://docs.microsoft.com/dynamics365/release-plans)
- [Kas nauja ar pasikeitė programoje „Dynamics 365 Human Resources”](hr-admin-whats-new.md)
- [Programinės įrangos ciklo strategija](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)


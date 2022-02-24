---
title: Trikčių, susijusių su dvigubo rašymo moduliu „Finance and Operations” programose, šalinimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su dvigubo rašymo moduliu „Finance and Operations” programose.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2241e7e6219f95115f55bc45a4d94550276e1e21
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683628"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Trikčių, susijusių su dvigubo rašymo moduliu „Finance and Operations” programose, šalinimas

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Dataverse“ programų trikčių šalinimo informacija. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, naudojant **dvigubo rašymo** modulį „Finance and Operations” programose.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Negalite įkelti dvigubo rašymo modulio „Finance and Operations” programoje

Jeigu negalite atidaryti **dvigubo rašymo** puslapio darbo srityje **Duomenų valdymas** pasirinkdami plytelę **Dvigubas rašymas**, tikriausiai duomenų integravimo paslauga neveikia. Norėdami paprašyti iš naujo paleisti duomenų integravimo paslaugą, sukurkite palaikymo bilietą.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Bandant sukurti naują lentelės schemą įvyko klaida

**Reikiami kredencialai, norint išspręsti problemą:** tas pats vartotojas, nustatęs dvigubą rašymą.

Kai bandote konfigūruoti naują dvigubo rašymo objektą, galite gauti toliau pateiktą klaidos pranešimą. Vienintelis vartotojas, galintis sukurti schemą, yra vartotojas, nustatęs dvigubo rašymo ryšį.

*Atsakymo būsenos kodas nenurodo sėkmės: 401 (neautorizuota)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Atidarant dvigubo rašymo vartotojo sąsają įvyko klaida

Kai bandote pasiekti dvigubą rašymą iš darbo srities **Duomenų valdymas**, galbūt gausite tokį klaidos pranešimą:

*Nepavyko užmegzti ryšio su login.microsoftonline.com*.

Norėdami išspręsti šią problemą, prisijunkite, naudodami „Microsoft Edge” langą „InPrivate”, inkognito langą „Chromium” arba inkognito langą „Google Chrome”. Taip pat turite atblokuoti arba išvalyti trečiosios šalies slapukus.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Susiejant dvigubo rašymo aplinką arba pridedant naują susiejimą su lentele įvyko klaida

**Reikiamas vaidmuo, norint išspręsti problemą:** „Finance and Operations” programų ir „Dataverse” sistemos administratorius.

Kai susiejate arba kuriate schemas, gali įvykti tokia klaida:

*Atsakymo būsenos kodas nenurodo sėkmės: 403 (tokenexchange).<br> Seanso ID: \<your session id\><br> Šakninės veiklos ID: \<your root activity id\>*

Ši klaida gali įvykti, jei neturite pakankamai teisių susieti dvigubą rašymą arba kurti schemas. Ši klaida taip pat gali įvykti, jei „Dataverse” aplinka buvo nustatyta iš naujo neatsiejus dvigubo rašymo. Bet kuris vartotojas, kuriam priskirtas sistemos administratorius vaidmuo „Finance and Operations” programose ir „Dataverse”, gali susieti aplinkas. Tik vartotojas, nustatęs dvigubo rašymo ryšį, gali įtraukti naujų lentelių schemų. Atlikus nustatymą, bet kuris vartotojas, kuriam priskirtas sistemos administratorius vaidmuo, gali stebėti būseną ir redaguoti susiejimus.

## <a name="error-when-you-stop-the-table-mapping"></a>Stabdant susiejimą su lentele įvyko klaida

Kai bandote sustabdyti susiejimus su lentele, galite gauti tokį klaidos pranešimą:

*\[Draudžiama\], \[{"būsena":403,"šaltinis":"","pranešimas":"atpažinimo ženklo keitimo klaida: vartotojui neleidžiama pasiekti ryšį dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], nuotolinis serveris pateikė klaidą: (403) draudžiama.*

Ši klaida įvyksta, kai nėra susietos „Dataverse” aplinkos.

Norėdami išspręsti šią problemą, sukurkite duomenų integravimo komandai skirtą bilietą. Pridėkite tinklo sekimą, kad duomenų integravimo komanda galėtų pažymėti vidines schemas kaip **Nevykdomos**.

## <a name="error-while-trying-to-start-an-table-mapping"></a>Bandant pradėti lentelių susiejimą įvyko klaida

Bandydami nustatyti susiejimo būseną į **Vykdoma**, galite gauti klaidos pranešimą, panašų į pateiktą toliau:

*Nepavyko baigti pradinių duomenų sinchronizavimo. Klaida: dvigubo rašymo triktis – nepavyko registruoti priedo. Nepavyko sukurti dvigubo rašymo peržvalgos metaduomenų. Klaidos objekto nuoroda nenustatyta kaip objekto egzempliorius.*

Šios klaidos sprendimas priklauso nuo klaidos priežasties.

+ Jei susiejime yra priklausomieji susiejimai, įsitikinkite, kad įgalinote šios lentelės susiejimo priklausomuosius susiejimus.
+ Gali trūkti susiejimo šaltinio arba paskirties laukų. Jei „Finance and Operations” programoje trūksta lauko, atlikite veiksmus, aprašytus skyriuje [Trūkstamų objektų laukų problema schemose](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps). Jei „Dataverse” trūksta lauko, spustelėkite susiejimo mygtuką **Atnaujinti lenteles**, kad laukai būtų automatiškai įvesti į susiejimą.

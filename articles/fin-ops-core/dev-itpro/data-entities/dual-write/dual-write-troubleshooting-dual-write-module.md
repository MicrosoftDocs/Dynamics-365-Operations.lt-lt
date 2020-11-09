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
ms.openlocfilehash: f99f3760e75ec1bbf2ccdea497cf2eec3e28e233
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997379"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Trikčių, susijusių su dvigubo rašymo moduliu „Finance and Operations” programose, šalinimas

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, naudojant **dvigubo rašymo** modulį „Finance and Operations” programose.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Negalite įkelti dvigubo rašymo modulio „Finance and Operations” programoje

Jeigu negalite atidaryti **dvigubo rašymo** puslapio darbo srityje **Duomenų valdymas** pasirinkdami plytelę **Dvigubas rašymas** , tikriausiai duomenų integravimo paslauga neveikia. Norėdami paprašyti iš naujo paleisti duomenų integravimo paslaugą, sukurkite palaikymo bilietą.

## <a name="error-when-you-try-to-create-a-new-entity-map"></a>Bandant sukurti naują objekto schemą įvyko klaida

**Reikiami kredencialai, norint išspręsti problemą:** tas pats vartotojas, nustatęs dvigubą rašymą.

Kai bandote konfigūruoti naują dvigubo rašymo objektą, galite gauti toliau pateiktą klaidos pranešimą. Vienintelis vartotojas, galintis sukurti schemą, yra vartotojas, nustatęs dvigubo rašymo ryšį.

*Atsakymo būsenos kodas nenurodo sėkmės: 401 (neautorizuota)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Atidarant dvigubo rašymo vartotojo sąsają įvyko klaida

Kai bandote pasiekti dvigubą rašymą iš darbo srities **Duomenų valdymas** , galbūt gausite tokį klaidos pranešimą:

*Nepavyko užmegzti ryšio su login.microsoftonline.com*.

Norėdami išspręsti šią problemą, prisijunkite, naudodami „Microsoft Edge” langą „InPrivate”, inkognito langą „Chromium” arba inkognito langą „Google Chrome”. Taip pat turite atblokuoti arba išvalyti trečiosios šalies slapukus.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Susiejant dvigubo rašymo aplinką arba pridedant naują susiejimą su objektu įvyko klaida

**Reikiamas vaidmuo, norint išspręsti problemą:** „Finance and Operations” programų ir „Common Data Service” sistemos administratorius.

Kai susiejate arba kuriate schemas, gali įvykti tokia klaida:

*Atsakymo būsenos kodas nenurodo sėkmės: 403 (tokenexchange).<br> Seanso ID: \<your session id\><br> Šakninės veiklos ID: \<your root activity id\>*

Ši klaida gali įvykti, jei neturite pakankamai teisių susieti dvigubą rašymą arba kurti schemas. Ši klaida taip pat gali įvykti, jei „Common Data Service” aplinka buvo nustatyta iš naujo neatsiejus dvigubo rašymo. Bet kuris vartotojas, kuriam priskirtas sistemos administratorius vaidmuo „Finance and Operations” programose ir „Common Data Service”, gali susieti aplinkas. Tik vartotojas, nustatęs dvigubo rašymo ryšį, gali įtraukti naujų objektų schemų. Atlikus nustatymą, bet kuris vartotojas, kuriam priskirtas sistemos administratorius vaidmuo, gali stebėti būseną ir redaguoti susiejimus.

## <a name="error-when-you-stop-the-entity-mapping"></a>Stabdant susiejimą su objektu įvyko klaida

Kai bandote sustabdyti susiejimus su objektu, galite gauti tokį klaidos pranešimą:

*\[Draudžiama\], \[{"būsena":403,"šaltinis":"","pranešimas":"atpažinimo ženklo keitimo klaida: vartotojui neleidžiama pasiekti ryšį dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], nuotolinis serveris pateikė klaidą: (403) draudžiama.*

Ši klaida įvyksta, kai nėra susietos „Common Data Service” aplinkos.

Norėdami išspręsti šią problemą, sukurkite duomenų integravimo komandai skirtą bilietą. Pridėkite tinklo sekimą, kad duomenų integravimo komanda galėtų pažymėti vidines schemas kaip **Nevykdomos**.

## <a name="error-while-trying-to-start-an-entity-mapping"></a>Bandant pradėti objektų susiejimą įvyko klaida

Bandydami nustatyti susiejimo būseną į **Vykdoma** , galite gauti klaidos pranešimą, panašų į pateiktą toliau:

*Nepavyko baigti pradinių duomenų sinchronizavimo. Klaida: dvigubo rašymo triktis – nepavyko registruoti priedo. Nepavyko sukurti dvigubo rašymo peržvalgos metaduomenų. Klaidos objekto nuoroda nenustatyta kaip objekto egzempliorius.*

Šios klaidos sprendimas priklauso nuo klaidos priežasties.

+ Jei susiejime yra priklausomieji susiejimai, įsitikinkite, kad įgalinote šio objekto susiejimo priklausomuosius susiejimus.
+ Gali trūkti susiejimo šaltinio arba paskirties laukų. Jei „Finance and Operations” programoje trūksta lauko, atlikite veiksmus, aprašytus skyriuje [Trūkstamų objektų laukų problema schemose](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps). Jei „Common Data Service” trūksta lauko, spustelėkite susiejimo mygtuką **Atnaujinti objektus** , kad laukai būtų automatiškai įvesti į susiejimą.

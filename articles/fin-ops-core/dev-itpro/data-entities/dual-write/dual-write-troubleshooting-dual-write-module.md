---
title: Dvigubo rašymo „Finance and Operations“ programų problemų šalinimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su dvigubo rašymo moduliu „Finance and Operations” programose.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 90ff55540c153ef4f3ac07bf5316a3abb4755f2c
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380145"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Dvigubo rašymo „Finance and Operations“ programų problemų šalinimas

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Dataverse“ programų trikčių šalinimo informacija. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, naudojant **dvigubo rašymo** modulį „Finance and Operations” programose.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Negalite įkelti dvigubo rašymo modulio „Finance and Operations” programoje

Jeigu negalite atidaryti **dvigubo rašymo** puslapio darbo srityje **Duomenų valdymas** pasirinkdami plytelę **Dvigubas rašymas**, tikriausiai duomenų integravimo paslauga neveikia. Norėdami paprašyti iš naujo paleisti duomenų integravimo paslaugą, sukurkite palaikymo bilietą.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Bandant sukurti naują lentelės schemą įvyko klaida

**Reikiami kredencialai, norint išspręsti problemą:** tas pats vartotojas, nustatęs dvigubą rašymą.

Kai bandote konfigūruoti naują dvigubo rašymo lentelę, galite gauti toliau pateiktą klaidos pranešimą. Vienintelis vartotojas, galintis sukurti schemą, yra vartotojas, nustatęs dvigubo rašymo ryšį.

*Atsakymo būsenos kodas nenurodo sėkmės: 401 (neautorizuota).*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Atidarant dvigubo rašymo vartotojo sąsają įvyko klaida

Kai bandote pasiekti dvigubą rašymą iš darbo srities **Duomenų valdymas**, galbūt gausite tokį klaidos pranešimą:

*Nepavyko užmegzti ryšio su login.microsoftonline.com*.

Norėdami išspręsti šią problemą, prisijunkite, naudodami „Microsoft Edge” langą „InPrivate”, inkognito langą „Chromium” arba inkognito langą „Google Chrome”. Taip pat turite atblokuoti arba išvalyti trečiosios šalies slapukus.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Susiejant dvigubo rašymo aplinką arba pridedant naują susiejimą su lentele įvyko klaida

**Reikiamas vaidmuo, norint išspręsti problemą:** „Finance and Operations” programų ir „Dataverse” sistemos administratorius.

Kai susiejate arba kuriate schemas, gali įvykti tokia klaida:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

Ši klaida gali įvykti, jei neturite pakankamai teisių susieti dvigubą rašymą arba kurti schemas. Ši klaida taip pat gali įvykti, jei „Dataverse” aplinka buvo nustatyta iš naujo neatsiejus dvigubo rašymo. Bet kuris vartotojas, kuriam priskirtas sistemos administratorius vaidmuo „Finance and Operations” programose ir „Dataverse”, gali susieti aplinkas. Tik vartotojas, nustatęs dvigubo rašymo ryšį, gali įtraukti naujų lentelių schemų. Atlikus nustatymą, bet kuris vartotojas, kuriam priskirtas sistemos administratorius vaidmuo, gali stebėti būseną ir redaguoti susiejimus.

## <a name="error-when-you-stop-the-table-mapping"></a>Stabdant susiejimą su lentele įvyko klaida

Kai bandote sustabdyti susiejimus su lentele, galite gauti tokį klaidos pranešimą:

*\[Draudžiama\], \[{"būsena":403,"šaltinis":"","pranešimas":"atpažinimo ženklo keitimo klaida: vartotojui neleidžiama pasiekti ryšį dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], nuotolinis serveris pateikė klaidą: (403) draudžiama.*

Ši klaida įvyksta, kai nėra susietos „Dataverse” aplinkos.

Norėdami išspręsti šią problemą, sukurkite duomenų integravimo komandai skirtą bilietą. Pridėkite tinklo sekimą, kad duomenų integravimo komanda galėtų pažymėti vidines schemas kaip **Nevykdomos**.

## <a name="errors-while-trying-to-start-a-table-mapping"></a>Klaidos, įvykusios bandant pradėti lentelių susiejimą

### <a name="unable-to-complete-initial-data-sync"></a>Nepavyksta užbaigti pradinio duomenų sinchronizavimo

Kai bandote vykdyti pradinį sinchronizavimą, galite gauti tokį klaidos pranešimą:

*Nepavyko baigti pradinių duomenų sinchronizavimo. Klaida: dvigubo rašymo triktis – nepavyko registruoti priedo. Nepavyko sukurti dvigubo rašymo peržvalgos metaduomenų. Klaidos objekto nuoroda nenustatyta kaip objekto egzempliorius.*

Bandydami nustatyti susiejimo būseną į **Vykdoma**, galite gauti toliau pateikiamą klaidos pranešimą. Sprendimas priklauso nuo klaidos priežasties.

+ Jei susiejime yra priklausomieji susiejimai, įsitikinkite, kad įgalinote šios lentelės susiejimo priklausomuosius susiejimus.
+ Gali trūkti susiejimo šaltinio arba paskirties stulpelių. Jei „Finance and Operations” programoje trūksta stulpelio, atlikite veiksmus, aprašytus skyriuje [Trūkstamų lentelių stulpelių problema schemose](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Jei „Dataverse” trūksta stulpelio, spustelėkite susiejimo mygtuką **Atnaujinti lenteles** tam, kad stulpeliai būtų automatiškai įvesti į susiejimą.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Versijų neatitikimo klaida ir dvigubo rašymo sprendimų atnaujinimas

Kai bandote vykdyti susiejimus su lentele, galite gauti tokius klaidos pranešimus:

+ *Klientų grupės (msdyn_customergroups): dvigubo rašymo funkcijos klaida – „Dynamics 365 for Sales” sprendimo „Dynamics365Company” versijų neatitikimas. Versija: 2.0.2.10 Reikalinga versija: 2.0.133*
+ *„Dynamics 365 for Sales” sprendimo „Dynamics365FinanceExtended” versijų neatitikimas. Versija: 1.0.0.0 Reikalinga versija: 2.0.227*
+ *„Dynamics 365 for Sales” sprendimo „Dynamics365FinanceAndOperationsCommon” versijų neatitikimas. Versija: 1.0.0.0 Reikalinga versija: 2.0.133*
+ *„Dynamics 365 for Sales” sprendimo „CurrencyExchangeRates” versijų neatitikimas. Versija: 1.0.0.0 Reikalinga versija: 2.0.133*
+ *„Dynamics 365 for Sales” sprendimo „Dynamics365SupplyChainExtended” versijų neatitikimas. Versija: 1.0.0.0 Reikalinga versija: 2.0.227*

Norėdami išspręsti problemas, atnaujinkite dvigubo rašymo sprendimus programoje „Dataverse”. Atnaujinkite sprendimą į naujausią versiją, atitinkančią reikiamą sprendimo versiją.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

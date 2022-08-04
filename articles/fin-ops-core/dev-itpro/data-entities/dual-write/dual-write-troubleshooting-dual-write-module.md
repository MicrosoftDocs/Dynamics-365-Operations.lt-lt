---
title: Dvigubo rašymo trikčių šalinimas finansų ir operacijų taikomosiose programose
description: Šiame straipsnyje pateikiama trikčių diagnostikos informacija, kuri gali padėti išspręsti problemas, susijusias su dvigubo rašymo moduliu, finansų ir operacijų programėle.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2743b99538b332af7cc6ad8d951eede562c14235
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111177"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Dvigubo rašymo trikčių šalinimas finansų ir operacijų taikomosiose programose

[!include [banner](../../includes/banner.md)]



Šiame straipsnyje pateikiama trikčių diagnostikos informacija, skirta dvigubo rašymo integravimui tarp finansų ir operacijų programėlių ir Dataverse. Taigi, pateikiama informacija, kuri gali padėti išspręsti problemas, **susijusias su dvigubo rašymo** moduliu, finansų ir operacijų programėle.

> [!IMPORTANT]
> Kai kurioms šio straipsnio adresams gali reikėti sistemos administratoriaus vaidmens arba "Microsoft Azure Active Directory " () nuomininkų Azure AD administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Dvigubo rašymo modulio negalima įkelti į finansų ir operacijų programą

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

**Reikalingas vaidmuo problemai išspręsti: sistemos** administratorius finansų ir operacijų programėlių ir Dataverse.

Kai susiejate arba kuriate schemas, gali įvykti tokia klaida:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

Ši klaida gali įvykti, jei neturite pakankamai teisių susieti dvigubą rašymą arba kurti schemas. Ši klaida taip pat gali įvykti, jei „Dataverse” aplinka buvo nustatyta iš naujo neatsiejus dvigubo rašymo. Bet kuris vartotojas, kuris turi sistemos administratoriaus vaidmenį ir finansų, ir operacijų Dataverse programėlei ir gali susieti aplinką. Tik vartotojas, nustatęs dvigubo rašymo ryšį, gali įtraukti naujų lentelių schemų. Atlikus nustatymą, bet kuris vartotojas, kuriam priskirtas sistemos administratorius vaidmuo, gali stebėti būseną ir redaguoti susiejimus.

## <a name="error-when-you-stop-the-table-mapping"></a>Stabdant susiejimą su lentele įvyko klaida

Kai bandote sustabdyti susiejimus su lentele, galite gauti tokį klaidos pranešimą:

*\[Draudžiama\], \[{"būsena":403,"šaltinis":"","pranešimas":"atpažinimo ženklo keitimo klaida: vartotojui neleidžiama pasiekti ryšį dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], nuotolinis serveris pateikė klaidą: (403) draudžiama.*

Ši klaida įvyksta, kai nėra susietos „Dataverse” aplinkos.

Norėdami išspręsti šią problemą, sukurkite duomenų integravimo komandai skirtą bilietą. Pridėkite tinklo sekimą, kad duomenų integravimo komanda galėtų pažymėti vidines schemas kaip **Nevykdomos**.

## <a name="enable-parallel-processing-in-finance-and-operations-apps-to-improve-performance"></a>Lygiagretaus apdorojimo finansų ir operacijų programose įgalinimas siekiant padidinti efektyvumą

Įgalinus lygiagretų apdorojimą gali būti sumažintas laikas, kurio reikia duomenims importuoti iš "Dynamics 365" klientų įsipareigojimo programėlių Microsoft Dataverse ir finansų bei operacijų programėlių. 

Norėdami įjungti lygiagretų finansų ir operacijų programėlių apdorojimą, atlikite nurodytus veiksmus.

1. Prisijunkite prie savo finansų ir operacijų aplinkos.
2. Eikite **į duomenų valdymo > sistemos parametrus**.
3. Pasirinkite Objekto parametrai ir **pasirinkite Konfigūruoti** objekto vykdymo parametrus **.**
4. Įtraukite paralelinio apdorojimo parametrus:
    - **Importo slenkstis** įrašų skaičius – įrašų, kuriuos reikia pasiekti prieš įgalinant lygiagretų apdorojimą, skaičius.
    - **Importo užduočių skaičius** – gijų (užduočių) skaičius, kurios bus paleidžiamos lygiagrečiai.
5. Pasirinkite **Įrašyti**.


## <a name="errors-while-trying-to-start-a-table-mapping"></a>Klaidos, įvykusios bandant pradėti lentelių susiejimą

### <a name="unable-to-complete-initial-data-sync"></a>Nepavyksta užbaigti pradinio duomenų sinchronizavimo

Kai bandote vykdyti pradinį sinchronizavimą, galite gauti tokį klaidos pranešimą:

*Nepavyko baigti pradinių duomenų sinchronizavimo. Klaida: dvigubo rašymo triktis – nepavyko registruoti priedo. Nepavyko sukurti dvigubo rašymo peržvalgos metaduomenų. Klaidos objekto nuoroda nenustatyta kaip objekto egzempliorius.*

Bandydami nustatyti susiejimo būseną į **Vykdoma**, galite gauti toliau pateikiamą klaidos pranešimą. Sprendimas priklauso nuo klaidos priežasties.

+ Jei susiejime yra priklausomieji susiejimai, įsitikinkite, kad įgalinote šios lentelės susiejimo priklausomuosius susiejimus.
+ Gali trūkti susiejimo šaltinio arba paskirties stulpelių. Jei finansų ir operacijų programoje trūksta stulpelio, [tada atlikite veiksmus skyriuje Trūksta lentelės stulpelių išdavimo pagal schemas](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Jei „Dataverse” trūksta stulpelio, spustelėkite susiejimo mygtuką **Atnaujinti lenteles** tam, kad stulpeliai būtų automatiškai įvesti į susiejimą.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Versijų neatitikimo klaida ir dvigubo rašymo sprendimų atnaujinimas

Kai bandote vykdyti susiejimus su lentele, galite gauti tokius klaidos pranešimus:

+ *Klientų grupės (msdyn_customergroups): dvigubo rašymo funkcijos klaida – „Dynamics 365 for Sales” sprendimo „Dynamics365Company” versijų neatitikimas. Versija: 2.0.2.10 Reikalinga versija: 2.0.133*
+ *„Dynamics 365 for Sales” sprendimo „Dynamics365FinanceExtended” versijų neatitikimas. Versija: 1.0.0.0 Reikalinga versija: 2.0.227*
+ *„Dynamics 365 for Sales” sprendimo „Dynamics365FinanceAndOperationsCommon” versijų neatitikimas. Versija: 1.0.0.0 Reikalinga versija: 2.0.133*
+ *„Dynamics 365 for Sales” sprendimo „CurrencyExchangeRates” versijų neatitikimas. Versija: 1.0.0.0 Reikalinga versija: 2.0.133*
+ *„Dynamics 365 for Sales” sprendimo „Dynamics365SupplyChainExtended” versijų neatitikimas. Versija: 1.0.0.0 Reikalinga versija: 2.0.227*

Norėdami išspręsti problemas, atnaujinkite dvigubo rašymo sprendimus programoje „Dataverse”. Atnaujinkite sprendimą į naujausią versiją, atitinkančią reikiamą sprendimo versiją.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


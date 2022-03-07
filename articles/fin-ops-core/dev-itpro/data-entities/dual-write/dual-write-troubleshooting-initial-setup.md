---
title: Problemų šalinimas pradinio nustatymo metu
description: Šioje temoje pateikiama informacija, kuri gali padėti išspręsti problemas, kylančias pradinės dvigubos rašymo integracijos sąrankos metu.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: c9bf5d9017579b4207e09769cff38361442e3938
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781445"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Problemų šalinimas pradinio nustatymo metu

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Dataverse“ programų trikčių šalinimo informacija. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinės dvigubos rašymo integracijos sąrankos metu.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Negalite susieti „Finance and Operations” programos su „Dataverse”

**Reikiamas vaidmuo, norint nustatyti dvigubo rašymo funkciją:** „Finance and Operations” programų ir „Dataverse” sistemos administratorius.

Klaidos puslapyje **Susiejimo su „Dataverse” sąranka** dažniausiai atsiranda dėl neužbaigtos sąrankos arba su teisėmis susijusių problemų. Įsitikinkite, kad puslapyje **Susiejimo su „Dataverse” sąranka** atlikta visiška būsenos patikra, kaip parodyta tolesnėje iliustracijoje. Negalite susieti dvigubo rašymo, neatlikę visiškos būsenos patikros.

![Sėkmingai atlikta būsenos patikra.](media/health_check.png)

Jei norite susieti „Finance and Operations” ir „Dataverse” aplinkas, privalote turėti „Azure AD” nuomotojo administratoriaus kredencialus. Susiejus aplinkas, vartotojai gali prisijungti, naudodami savo paskyros kredencialus, ir atnaujinti esamą lentelės schemą.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Raskite juridinių lentelių ar įmonių, kurios gali būti susietos naudojant dvigubo rašymo funkciją, skaičiaus limitą

Kai bandote įgalinti schemas, galite gauti tokį klaidos pranešimą:

*Dvigubo rašymo funkcijos klaida – nepavyko registruoti priedo: [(nepavyko gauti skaidinio schemos projektui DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Klaida. Viršijamas maksimalus susiejimui leidžiamų skaidinių skaičius DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], įvyko viena ar daugiau klaidų.*

Dabartinis limitas susiejant aplinkas yra maždaug 40 juridinių lentelių. Ši klaida įvyksta, jei bandote įgalinti schemas, o daugiau nei 40 juridinių lentelių yra susieti su aplinkomis.

## <a name="connection-set-failed-while-linking-environment"></a>Susiejant aplinką nepavyko susieti ryšių rinkinio

Susiejant dvigubo rašymo aplinką, veiksmas nepavyksta ir pateikiamas klaidos pranešimas:

*Nepavyko įrašyti ryšių rinkinio! Prekė tokiu pačiu raktu jau įtraukta.*

Dvigubo rašymo funkcija nepalaiko kelių juridinių subjektų / įmonių tokiu pačiu pavadinimu. Pavyzdžiui, jei programoje „Dataverse” turite dvi įmones pavadinimu „DAT”, bus pateiktas šis klaidos pranešimas.

Norėdami atblokuoti klientą, pašalinkite besidubliuojančius įrašus programos „Dataverse” lentelėje **cdm_company**. Be to, jei lentelėje **cdm_company** yra įrašų tuščiu pavadinimu, pašalinkite arba pataisykite šiuos įrašus.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Klaida atidarant dvigubo rašymo puslapį „Finance and Operations” programose

Kai bandote susieti dvigubo rašymo „Dataverse“ aplinką, galite gauti toliau pateiktą klaidos pranešimą.

*Atsakymo būsenos kodas nenurodo sėkmės: 404 (nerasta).*

Ši klaida įvyksta, kai programos sutikimo veiksmas neužbaigtas. Prisijungus prie `portal.azure.com`, naudojant nuomotojo administratoriaus klientą, galima patikrinti, ar buvo suteiktas sutikimas ir ar trečiosios šalies programa, kurios ID `33976c19-1db5-4c02-810e-c243db79efde`, rodoma AAD „Enterprise“ programų sąraše. Jei ne, grįžkite prie sutikimo veiksmo kaip nurodyta kitame skyriuje.

### <a name="providing-app-consent"></a>Programos sutikimo suteikimas

+ Naudodami administratoriaus kredencialus, paleiskite šį URL.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Norėdami sutikti, pasirinkite **Sutikti**. Sutinkate savo nuomotojuje įdiegti programą (kurios `id=33976c19-1db5-4c02-810e-c243db79efde`).
+ Ši programa reikalinga, kad „Dataverse” palaikytų ryšį su „Finance and Operations” programos.

    ![Pradinio sinchronizavimo sąrankos trikčių šalinimas.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Jei tai neveikia, paleiskite URL „Microsoft Edge” privačiu režimu arba „Chrome” incognito režimu.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Nepavyksta aptikti „Finance and Operations” aplinkos

Galbūt gausite tolesnį klaidos pranešimą:

*„Finance and Operations” programų aplinkos \*\*\*.cloudax.dynamics.com aptikti nepavyksta.*

Yra du dalykai, dėl kurių gali kilti problema, kai aplinkos aptikti nepavyksta:

+ Prisijungęs vartotojas nėra tas pats nuomotojas kaip „Finance and Operations” egzempliorius.
+ Yra keli senesni „Microsoft“ nuomojami „Finance and Operations” egzemplioriai, kuriuose kildavo aptikimo problema. Norėdami išspęsti šią problemą, atnaujinkite „Finance and Operations” egzempliorių. Aplinką galima aptikti, naudojant bet kurį atnaujinimą.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

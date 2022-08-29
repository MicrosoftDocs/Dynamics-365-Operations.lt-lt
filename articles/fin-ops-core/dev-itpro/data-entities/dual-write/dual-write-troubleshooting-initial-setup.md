---
title: Problemų šalinimas pradinio nustatymo metu
description: Šiame straipsnyje pateikiama informacija, kuri gali padėti išspręsti problemas, kurios atsiranda atliekant pradinį dvigubo rašymo integravimo nustatymą.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d33fc6f4895b53f16cc6957a3a2fc6b1abe90a2f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289521"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Problemų šalinimas pradinio nustatymo metu

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiama trikčių diagnostikos informacija, skirta dvigubo rašymo integravimui tarp finansų ir operacijų programėlių ir Dataverse. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinės dvigubos rašymo integracijos sąrankos metu.

> [!IMPORTANT]
> Kai kurioms šio straipsnio adresams gali reikėti sistemos administratoriaus vaidmens arba "Microsoft Azure Active Directory " () nuomininkų Azure AD administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Negalima susieti finansų ir operacijų programos su Dataverse

**Nustatytas dvigubo rašymo vaidmuo: sistemos administratorius** finansų ir operacijų programėlių ir Dataverse.

Klaidos puslapyje **Susiejimo su „Dataverse” sąranka** dažniausiai atsiranda dėl neužbaigtos sąrankos arba su teisėmis susijusių problemų. Įsitikinkite, kad puslapyje **Susiejimo su „Dataverse” sąranka** atlikta visiška būsenos patikra, kaip parodyta tolesnėje iliustracijoje. Negalite susieti dvigubo rašymo, neatlikę visiškos būsenos patikros.

![Sėkmingai atlikta būsenos patikra.](media/health_check.png)

Norėdami susieti finansus Azure AD ir operacijas bei aplinkas, turite turėti nuomininkų administratoriaus Dataverse kredencialus. Susiejus aplinkas, vartotojai gali prisijungti, naudodami savo paskyros kredencialus, ir atnaujinti esamą lentelės schemą.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Raskite juridinių lentelių ar įmonių, kurios gali būti susietos naudojant dvigubo rašymo funkciją, skaičiaus limitą

Kai bandote įgalinti schemas, galite gauti tokį klaidos pranešimą:

*Dvigubo rašymo funkcijos klaida – nepavyko registruoti priedo: [(nepavyko gauti skaidinio schemos projektui DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Klaida. Viršijamas maksimalus susiejimui leidžiamų skaidinių skaičius DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], įvyko viena ar daugiau klaidų.*

Dabartinis limitas susiejant aplinkas yra maždaug 40 juridinių lentelių. Ši klaida įvyksta, jei bandote įgalinti schemas, o daugiau nei 40 juridinių lentelių yra susieti su aplinkomis.

## <a name="connection-set-failed-while-linking-environment"></a>Susiejant aplinką nepavyko susieti ryšių rinkinio

Susiejant dvigubo rašymo aplinką, veiksmas nepavyksta ir pateikiamas klaidos pranešimas:

*Nepavyko įrašyti ryšių rinkinio! Prekė tokiu pačiu raktu jau įtraukta.*

Dvigubo rašymo funkcija nepalaiko kelių juridinių subjektų / įmonių tokiu pačiu pavadinimu. Pavyzdžiui, jei turite dvi įmones, kurių pavadinimas DAT Dataverse, bus pateiktas šis klaidos pranešimas.

Norėdami atblokuoti klientą, pašalinkite besidubliuojančius įrašus programos „Dataverse” lentelėje **cdm_company**. Be to, jei lentelėje **cdm_company** yra įrašų tuščiu pavadinimu, pašalinkite arba pataisykite šiuos įrašus.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Klaida atidarant dvigubo rašymo puslapį finansų ir operacijų programėlei

Kai bandote susieti dvigubo rašymo „Dataverse“ aplinką, galite gauti toliau pateiktą klaidos pranešimą.

*Atsakymo būsenos kodas nenurodo sėkmės: 404 (nerasta).*

Ši klaida įvyksta, kai programos sutikimo veiksmas neužbaigtas. Prisijungus prie `portal.azure.com`, naudojant nuomotojo administratoriaus klientą, galima patikrinti, ar buvo suteiktas sutikimas ir ar trečiosios šalies programa, kurios ID `33976c19-1db5-4c02-810e-c243db79efde`, rodoma AAD „Enterprise“ programų sąraše. Jei ne, grįžkite prie sutikimo veiksmo kaip nurodyta kitame skyriuje.

### <a name="providing-app-consent"></a>Programos sutikimo suteikimas

+ Naudodami administratoriaus kredencialus, paleiskite šį URL.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Norėdami sutikti, pasirinkite **Sutikti**. Sutinkate savo nuomotojuje įdiegti programą (kurios `id=33976c19-1db5-4c02-810e-c243db79efde`).
+ Kad būtų galima susisiekti su finansų ir Dataverse operacijų programėle, reikia šios programos.

    ![Pradinio sinchronizavimo sąrankos trikčių šalinimas.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Jei tai neveikia, paleiskite URL „Microsoft Edge” privačiu režimu arba „Chrome” incognito režimu.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finansų ir operacijų aplinkos neįmanoma atrasti

Galbūt gausite tolesnį klaidos pranešimą:

*Finansų ir operacijų programėlių \*\*\* aplinkos cloudax.dynamics.com neįmanoma atrasti.*

Yra du dalykai, dėl kurių gali kilti problema, kai aplinkos aptikti nepavyksta:

+ Vartotojui, kuris buvo naudojamas prisijungti, nėra tas pats nuomininkas, kaip ir finansų ir operacijų egzempliorius.
+ Yra senesnių finansų ir operacijų egzempliorių, kurie "Microsoft" laikomi su surasti išdavimu. Norėdami tai ištaisyti, atnaujinkite finansų ir operacijų egzempliorių. Aplinką galima aptikti, naudojant bet kurį atnaujinimą.

## <a name="403-forbidden-error-while-connections-are-being-created"></a>403 (draudžiama) klaida kuriant ryšius

Kaip dvigubo rašymo susiejimo proceso dalis, Power Apps du ryšiai (*taip pat vadinami Apihub* ryšiais) sukuriami vartotojo vardu susietame aplinkoje Dataverse. Jei klientas neturi Power Apps aplinkos licencijos, ApiHub ryšių sukurti nepavyksta, rodoma 403 (Draudžiama). Čia yra klaidos pranešimo pavyzdys:

> MSG=Nepavyko\[ nustatyti dvigubo rašymo aplinkos. Klaidos informacija: atsakymo būsenos kodas nerodo sėkmės: 403 (draudžiama). – atsakymo būsenos kodas nerodo sėkmės: 403 (Draudžiama).\] STACKTRACE =\[ į Microsoft.Dynamics.Integrator.ProjectManagementService.DualWrite.DualWriteConnectionSetProcessor.\<CreateDualWriteConnectionSetAsync\> d\_\_ 29.MoveNext() X:\\ bt\\ 1158727\\ repo\\ src\\ ProjectManagementService\\ DualWrite\\ DualWriteConnectionSetProcessor.cs:line 297 --- --- dėklo sekimo pabaiga iš ankstesnės vietos, kur buvo System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw() System.Runtime.CompilerServices.TaskHoriter.HandleNonSuccessAndDebuggerNotification(Task task), Microsoft.Dynamics.Integrator.ProjectManagementService.Controllers.DualWriteEnvironmentManagementController.\<SetupDualWriteEnvironmentAsync\> d\_\_ 34.MoveNext() X:\\ bt\\ 1158727\\ repo\\ src\\ ProjectManagementService\\ Controllers\\ DualWriteEnvironmentManagementController.cs:line 265\]

Ši klaida įvyksta dėl licencijos trūkumo Power Apps. Priskirkite vartotojui tinkamą licenciją (pvz., Power Apps Bandomasis 2 planas), kad vartotojas turėtų teisę kurti ryšius. Norėdami patikrinti licenciją, klientas gali eiti [į "Mano](https://portal.office.com/account/?ref=MeControl#subscriptions) sąskaitos" svetainę ir peržiūrėti dabar vartotojui priskirtas licencijas.

Norėdami gauti daugiau informacijos Power Apps apie licenciją, žr. šiuos straipsnius:

- [Licencijų priskyrimas vartotojams](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide)
- [Jūsų Power Apps organizacijos pirkimas](/power-platform/admin/signup-for-powerapps-admin)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


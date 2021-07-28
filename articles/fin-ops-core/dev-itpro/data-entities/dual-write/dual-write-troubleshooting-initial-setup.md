---
title: Problemų šalinimas pradinio nustatymo metu
description: Šioje temoje pateikiama informacija, kuri gali padėti išspręsti problemas, kylančias pradinės dvigubos rašymo integracijos sąrankos metu.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c641849b2aec76124b6661f339175325a312efce
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350841"
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

## <a name="error-when-you-open-the-link-to-dataverse-page"></a>Atidarant puslapį „Susiejimo su „Dataverse” sąranka“ įvyko klaida

**Reikiami kredencialai, norint išspręsti problemą:** „Azure AD” nuomotojo administratorius

Kai „Finance and Operations” programoje atidarote puslapį „**Susiejimo su „Dataverse”** sąranka“, galite gauti tokį klaidos pranešimą:

*Atsakymo būsenos kodas nenurodo sėkmės: 404 (nerasta).*

Ši klaida įvyksta, kai sutikimo veiksmas neužbaigtas. Norėdami patikrinti, ar sutikimo veiksmas užbaigtas, prisijunkite prie portal.Azure.com, naudodami „Azure AD” nuomotojo administratoriaus paskyrą, ir patikrinkite, ar trečiosios šalies programa, kurios ID yra **33976c19-1db5-4c02-810e-c243db79efde**, atsiranda „Azure AD” sąraše **„Enterprise“ programos**. Jei neatsiranda, turite suteikti programos sutikimą.

Norėdami suteikti programos sutikimą, atlikite šiuos veiksmus.

1. Naudodami administratoriaus kredencialus, atidarykite šį URL. Būsite paraginti pateikti sutikimą.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Norėdami nurodyti, kad sutinkate, kad trečiosios šalies programa, kurios ID yra **33976c19-1db5-4c02-810e-c243db79efde** būtų diegiama jūsų nuomotojuje, pasirinkite **Priimti**.

    > [!TIP]
    > Ši programa reikalauja susieti „Dataverse” ir „Finance and Operations” programas. Jei atliekant šį veiksmą kyla problemų, atidarykite savo naršyklę inkognito režimu („Google Chrome”) arba „InPrivate” režimu („Microsoft Edge”).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Patikrinkite, ar susiejimo metu yra tinkamai nustatyti įmonės duomenys ir dvigubo rašymo komandos

Siekiant užtikrinti, kad dvigubas rašymas veiktų tinkamai, įmonės, kurias pasirenkate konfigūravimo metu, yra kuriamos „Dataverse” aplinkoje. Pagal numatytuosius parametrus, šios įmonės yra tik skaitomas, o ypatybė **IsDualWriteEnable** yra nustatyta kaip **Teisinga**. Be to, sukuriami numatytasis verslo struktūros vieneto savininkas ir komanda ir įtraukiamas įmonės pavadinimas. Prieš įgalindami schemas, patikrinkite, ar nurodytas numatytasis komandos savininkas. Norėdami rasti lentelę **Įmonės (CDM\_įmonė)**, atlikite šiuos veiksmus.

1. Modeliu grįstos „Dynamics 365” programos viršutiniame dešiniajame kampe pasirinkite filtrą.
2. Išplečiamajame sąraše pasirinkite **Įmonė**.
3. Norėdami pamatyti rezultatus, pasirinkite **Vykdyti**.
4. Pasirinkite įmonę, kuri buvo susieta konfigūruojant dvigubą rašymą.
5. Patikrinkite, ar stulpelyje **Numatytoji komanda savininkė** yra reikšmė. Šioje iliustracijoje stulpelis **Numatytoji komanda savininkė** nustatytas kaip **USMF dvigubas rašymas**.

    ![Numatytosios komandos savininkės tikrinimas.](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Raskite juridinių lentelių ar įmonių, kurios gali būti susietos naudojant dvigubo rašymo funkciją, skaičiaus limitą

Kai bandote įgalinti schemas, galite gauti tokį klaidos pranešimą:

*Dvigubo rašymo funkcijos klaida – nepavyko registruoti priedo: \[(nepavyko gauti skaidinio schemos projektui DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Klaida. Viršijamas maksimalus susiejimui leidžiamų skaidinių skaičius DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], įvyko viena ar daugiau klaidų.*

Dabartinis limitas susiejant aplinkas yra maždaug 40 juridinių lentelių. Ši klaida įvyksta, jei bandote įgalinti schemas, o daugiau nei 40 juridinių lentelių yra susieti su aplinkomis.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
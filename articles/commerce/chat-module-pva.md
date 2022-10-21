---
title: "\"Commerce Chat\" su moduliu Power Virtual Agents"
description: Šiame straipsnyje aprašomas "Commerce Chat" su moduliu Power Virtual Agents, kuris integruoja "Microsoft" su Power Virtual Agents žiniatinklio svetainėmis Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690961"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>"Commerce Chat" su moduliu Power Virtual Agents

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomas "Commerce Chat" su moduliu Power Virtual Agents, kuris integruoja "Microsoft" su Power Virtual Agents žiniatinklio svetainėmis Dynamics 365 Commerce.

"Commerce Chat" su Power Virtual Agents funkcija suteikia "Dynamics 365" el. komercijos Power Virtual Agents klientams galimybę naudotis pokalbio galimybėsmis jų užklausoms tvarkyti. Dynamics 365 Commerce Kaip 10.0.30 leidimą ši funkcija gali būti įtraukta į el. komercijos svetaines naudojant "Commerce Chat Power Virtual Agents" su moduliu, kuris yra "Commerce" modulių bibliotekos dalis.

"Commerce Chat" Power Virtual Agents su funkcija padeda įmonėms pasiekti šiuos tikslus:

- Padidinkite asmeninį įsipareigojimą savo vartotojams ir patobulinkite užlaikymą.
- Padidinti klientų aptarnavimą integruojant savitarnos pokalbius.
- Padidinkite bendrą klientų pasitenkinimą ir dėl to padidinkite pardavimą.

> [!NOTE]
> Norėdami sužinoti apie skirtumus tarp "Dynamics 365" Klientų aptarnavimo ir programų Prekybos modulių, Power Virtual Agents žr [. "Commerce" pokalbių modulių peržiūrą](/commerce-chat-modules-overview.md).

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a> Būtinos naudojimo sąlygos Power Virtual Agents

Norėdami naudotis "Commerce Chat" Power Virtual Agents funkcija, pirmiausia turite sukurti el Power Virtual Agents . komercijos svetainės pokalbių portalą. Instrukcijų ieškokite " [Power Virtual Agent Bot" kūrimas](/power-virtual-agents/authoring-first-bot).

Sukonfigūrę pokalbių portalą, **turite nukopijuoti Bot ID** **ir nuomininkų ID** pokalbių parametrų vertes, kad konfigūruosite komercijos pokalbių patirtį. Informacijos apie šių verčių kopijavimą rasite Nuskaitykite [savo bot Power Virtual Agents parametrus](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>Konfigūruoti savo el. komercijos svetainę 

Vienas rekomenduojamas būdas įdiegti pokalbių su jūsų el. prekybai svetainę būdą yra įtraukti "Commerce Susirašinė Power Virtual Agents " su moduliu į bendrinamą antraštės fragmentą, kuris naudojamas jūsų svetainės puslapiuose.

Norėdami įtraukti pokalbio modulį į savo svetainės antraštės fragmentą Komercijos svetainės generatoriuje, atlikite šiuos veiksmus.

1. "Commerce" svetainės generatoriuje, skirtame jūsų svetainei, eikite į **Fragmentai**.
1. Pasirinkite **Nauja**.
1. Dialogo lange **Pasirinkti fragmentą** pasirinkite "Commerce Susirašinė **" Power Virtual Agents** su moduliu, įveskite fragmento pavadinimą, tada pasirinkite **Gerai**.
1. Struktūros rodinyje pasirinkite Msari365 **pva pokalbių jungties atminties kortelių atminties** jungtį.
1. Dešinėje ypatybės srityje atlikite šiuos veiksmus:

    1. Po **Bot Parametrai**, interneto pokalbių **Bot Framework CDN URL** lauke, palikite numatytąją vertę (pvz., `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. Autentifikavimo **Bot Framework Direct Line URL lauke** palikite numatytąją vertę (pvz., `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. **Lauke Bot ID įveskite** Bot ID Power Virtual Agents vertę, kurią nukopijavote į būtinuosius **komponentus,**[kad būtų galima naudoti Power Virtual Agents](#prereq) skyrių.
    1. Lauke Nuomininko **ID įveskite nukopijuotą** nuomininko ID **vertę**.

1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite **į** fragmentus ir atidarykite savo svetainės antraštės fragmentą.
1. Numatytoje **konteinerio** atminties atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **fragmentą**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite anksčiau sukurtą pokalbio fragmentą ir pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="proactive-chat-parameters"></a>Išaktyvi pokalbių parametrai

Išsamų aktyvių pokalbių konfigūravimo parametrų sąrašą rasite " [Commerce" pokalbių modulio iš anksto aktyvių pokalbių parametrų sąraše](chat-proactive-chat-parameters.md).

> [!NOTE]
> Šiuo metu Power Virtual Agents B2C Azure Active Directory (Azure AD B2C) autentifikavimas nepalaikotas. Jis palaiko tik anoniminius Retail Cloud Scale Unit (RCSU) skambučius, norint gauti produkto prieinamumą arba sąveikauti su kitais anoniminiais API. Norint naudoti autentifikuotas API naudojant Power Virtual Agents pokalbių registracijas, reikia pateikti aiškų kliento prisijungimą.

## <a name="additional-resources"></a>Papildomi ištekliai

["Commerce" pokalbių funkcijų peržiūra](commerce-chat-overview.md)

[Klientų aptarnavimo modulio "Commerce Susirašinėti su Cbchannel"](commerce-chat-module.md)

["Commerce" pokalbių modulio proactive pokalbių parametrai](chat-proactive-chat-parameters.md)

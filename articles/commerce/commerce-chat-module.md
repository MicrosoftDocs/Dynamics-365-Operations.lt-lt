---
title: Klientų aptarnavimo modulio "Commerce Susirašinėti su Cbchannel"
description: Šiame straipsnyje aprašomas "Commerce Chat" su klientų aptarnavimo modulio Modulyje "Cbchannel"Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: e4a004b929138f0a04c19d6a94278cfad6e83303
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346098"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Klientų aptarnavimo modulio "Commerce Susirašinėti su Cbchannel"

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šiame straipsnyje aprašomas " *Commerce Chat" su klientų aptarnavimo modulio* Modulyje "Cbchannel"Microsoft Dynamics 365 Commerce.

"Commerce" 10.0.29 versijoje naujas "Commerce Chat" su klientų aptarnavimo modulio "Commerce" moduliu buvo pridėtas prie "Commerce" modulio bibliotekos. "Commerce" pokalbių funkcija teikia el. prekybos klientams galimybę susirašinėti su "Dynamics 365" klientų aptarnavimo portalu, kuris apima tiesioginį agentų palaikymą, padėsią adresuoti klientų užklausas, suteikti klientų aptarnavimo paslaugas ir palengvinti pardavimą "Commerce" klientams.

"Commerce" pokalbių funkcija leidžia mažmenininkams pasiekti šiuos tikslus:

- Padidinkite asmeninį įsipareigojimą klientams, kad pagerinti klientų išsaugojimą.
- Pagerinti klientų aptarnavimą integruojant personalo agentą ir savitarnos pokalbių pokalbius.
- Žinyno agentai turi patirties realiuoju laiku vykdant klientų profilį, užsakymus ir pirkimo duomenis, kurie padeda patobulinti veiklą ir vykdyti įsipareigojimus.
- Pagerinti bendrą klientų pasitenkinimą, kad būtų padidintas pardavimas.

Šios galimybės galimos kaip "Commerce" pokalbių pokalbių funkcijos dalis:

- Klientų aptarnavimo "Commerce Susirašinėti su Verslo klientų aptarnavimo tarnyba"
- "Commerce Call **Center" pridėjimas** kaip programos skirtukas agentų patirties programoje "Dynamics 365" Klientų aptarnavimo aptarnavimas

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Klientų aptarnavimo klientų aptarnavimo būtinosios sąlygos

Būtinuosius komponentus turite sukonfigūruoti klientų aptarnavimo administravimo sąrašams skirtame "Dnschannel" lange ir gauti keletą parametrų, kaip sukonfigūruoti "Commerce" pokalbių patirtį. Instrukcijų ieškokite pokalbių [kanalo konfigūravimas](/dynamics365/customer-service/set-up-chat-widget).

Sukonfigūrę klientų aptarnavimo administracijos vartotojo susirašinėlį, gausite scenarijų, kuris yra panašus į šį pavyzdį.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Kopijuokite šį scenarijų, nes, norint sukonfigūruoti pokalbių modulį, reikės jo verčių.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>"Commerce Susirašinėti su Klientų aptarnavimo privalomuose laukuose esančiuose Klientų aptarnavimo portalo susirašinyje

Toliau pateikiamoje lentelėje pateikiamos scenarijų vertės iš Klientų aptarnavimo administracijos valdiklio, kurio reikia norint sukonfigūruoti "Commerce Susirašinėti su Klientų aptarnavimo modulio "Dnschannel".

| Valdiklio ypatybė | Aprašymas |
| ------------- |--------------|
| Scenarijaus šaltinis | **SRC vertė pokalbio** elementų scenarijuje. |
| Duomenų programos ID | **Duomenų -app-ID vertė** pokalbių sąrašmenų scenarijuje. |
| Duomenų organizacijos ID | **Duomenų -org-ID** vertė pokalbių sąrašmenų scenarijuje. |
| Duomenų organizacijos URL | **Duomenų -org-URL vertė pokalbių** sąrašmenų scenarijuje. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>Konfigūruoti savo el. komercijos svetainės "Commerce" pokalbių patirtį

Vienas rekomenduojamas būdas įdiegti pokalbių su jūsų el. prekybai svetainę būdą yra įtraukti "Commerce Susirašinėlį su klientų aptarnavimo moduliu" į bendrinamą antraštės fragmentą, kuris naudojamas jūsų el. komercijos svetainės puslapiuose.

Norėdami įtraukti pokalbio modulį į savo svetainės antraštės fragmentą Komercijos svetainės generatoriuje, atlikite šiuos veiksmus.

1. Savo svetainės generatoriuje eikite į **Fragmentai**.
1. Pasirinkite **Nauja**.
1. Lauke Pasirinkti **fragmentą dialogo lange pasirinkite**"Commerce Susirašinėjimas su klientų aptarnavimo moduliu "Cbchannel **", įveskite fragmento** pavadinimą, tada pasirinkite **Gerai**.
1. Struktūros rodinyje pasirinkite Msari365 **cs pokalbių jungties atminties atminties** jungtį.
1. Dešinėje pokalbio **ypatybės** srityje atlikite šiuos veiksmus:

    1. Scenarijų **šaltinio lauke** įveskite SRC **vertę,** kurią gavote iš klientų aptarnavimo scenarijaus Lauko.
    1. Lauke Duomenų **programos ID** įveskite duomenų -app-ID **vertę,** kurią gavote iš klientų aptarnavimo scenarijaus "Laukuose Jūsų ieškos".
    1. Lauke Duomenų **organizacijos ID** esanti duomenų -org-ID **vertė,** kurią gavote iš klientų aptarnavimo scenarijaus "Jūsų duomenų organizacijos" scenarijaus.
    1. Lauke Duomenų **organizacijos URL** įveskite duomenų **-org-url** vertę, kurią gavote iš klientų tarnybos scenarijaus "Tarpchannel".

    !["Commerce Chat" modulio fragmento kūrimas "Commerce" svetainės generatoriuje.](media/Commerce-chat-creating-new-fragment.png)

1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite **į** fragmentus ir atidarykite savo svetainės antraštės fragmentą.
1. Numatytoje **konteinerio** atminties atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **fragmentą**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite anksčiau sukurtą pokalbio fragmentą ir pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Įtraukti "Commerce Headquarters" kaip klientų aptarnavimo klientų aptarnavimo programos skirtuką

Klientų aptarnavimo portale "Commerce Headquarters" galite pridėti programos skirtuką. Tiesioginio valdymo agentai tada gali naudoti klientų Dynamics 365 Commerce aptarnavimo agentų patirties vartotojo sąsają, kad galėtų lengvai pasiekti klientų aptarnavimo modulį, kuriame yra kontekstinė kliento informacija ir jų pardavimo užsakymų informacija. Be to, klientų aptarnavimo agentai gali pateikti naujus užsakymus, inicijuoti grąžinimus ir patikrinti užsakymo būsenos informaciją.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Sukurkite naują programos skirtuką, į kurį įkeliama "Commerce Headquarters" modulyje iFrame 

Norėdami sukurti naują programos skirtuką, į kurį įkeliama "Commerce Headquarters" iFrame į modulį, atlikite šiuos veiksmus.

1. Atidarykite kūrėjo [Power Apps portalą](https://make.powerapps.com).
1. Kairėje naršymo srityje pasirinkite **Programos**.
1. Pasirinkite **klientų aptarnavimo administravimo centrą**.
1. Eiti į agento **patirtį**.
1. Jei norite **naudoti skirtukų programos** šablonus, pasirinkite **Valdyti**.
1. Sukurkite naują trečiosios šalies svetainės **tipo prašymo skirtuką**. Instrukcijų ieškokite Skirtukų [Tvarkyti prašymo šablonus](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter).
1. Url **parametro** **Vertės** lauko dalyje **Parametrai įveskite toliau** nurodytą URL, kur `<YourOrganizationHeadquartersURL>` ir `<LegalEntityname>` jie pakeičiami atitinkamomis vertėmis. Klientų aptarnavimo tarnyba perskaito iš **{AccountNumber}** pokalbių konteksto. Todėl palikite **{AccountNumber}** taip, kaip yra.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. Duomenų parametro **vertės** lauką **palikite** tuščią.

![Kuriamas programos skirtukas "Dynamics 365" Klientų aptarnavimo tarnyba.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Įjungti naują klientų agentų programos skirtuką "Dynamics 365" Kliento aptarnavimo laukeChannel

Norėdami įjungti naują klientų agentų programos skirtuką programoje "Dynamics 365" Klientų aptarnavimo portalas" atlikite šiuos veiksmus.
    
1. Atidarykite kūrėjo [Power Apps portalą](https://make.powerapps.com).
1. Kairėje naršymo srityje pasirinkite **Programos**.
1. Pasirinkite **klientų aptarnavimo administravimo centrą**.
1. Eikite į **klientų aptarnavimo \> darbo srautus**.
1. Atidarykite savo agentams sukurtą darbo srautą, tada dalyje **Išplėstiniai** parametrai pasirinkite Numatytieji **seansai**.
1. Skirtuke **Programos skirtukai** pasirinkite **Įtraukti esamą programos** skirtuką, tada pridėkite naują anksčiau sukurtą programos skirtuką. Šis veiksmas užtikrina, kad programos skirtukas, į kurį įkeliama "Commerce Headquarters" modulyje, bus rodomas tada, kai agentas gaus gauna pokalbio skambutį iš el. komercijos iFrame svetainės.

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Įtraukti konteksto kintamuosius į "Dynamics 365" Klientų aptarnavimo skyrių

Norėdami įtraukti konteksto kintamuosius į "Dynamics 365" Klientų aptarnavimo skyrių, atlikite šiuos veiksmus.

1. Atidarykite kūrėjo [Power Apps portalą](https://make.powerapps.com).
1. Kairėje naršymo srityje pasirinkite **Programos**.
1. Pasirinkite **klientų aptarnavimo administravimo centrą**.
1. Eikite į **klientų aptarnavimo \> darbo srautus**.
1. Atidarykite darbo srautą, kurį sukūrėte savo agentams, **tada dalyje Išplėstiniai parametrai** eikite į konteksto kintamojo **skyrių**.
1. Pasirinkite **Redaguoti**, tada pridėkite **AccountNumber** kaip teksto tipo konteksto **kintamąjį**. Šis kintamasis padės "Commerce Headquarters" įkelti kliento informaciją su atitinkančiais sąskaitų numeriais.

> [!NOTE]
> Jei norite skaityti el. pašto adresus ir prisijungusių vartotojų pavadinimus iš el. komercijos kanalo, be konteksto kintamųjų AccountNumber **,** **·** **galite** pridėti el. pašto ir pavadinimo kaip teksto tipo konteksto kintamuosius.**·**

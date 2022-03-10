---
title: Įgalinti kliento įregistravimo pranešimus kasos punkte (EKA)
description: Šioje temoje aprašoma, kaip įgalinti kliento įregistravimo pranešimus į „Microsoft Dynamics 365 Commerce“ kasos kodą (EKA).
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 95b4e3a1750cf072db919492f7445e87654701da
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983166"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Įgalinti kliento įregistravimo pranešimus kasos punkte (EKA)

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip įgalinti kliento įregistravimo pranešimus į „Microsoft Dynamics 365 Commerce“ kasos kodą (EKA).

Savo el. laiškų „užsakymas paruoštas paimti" organizacijos gali pateikti saitą ar mygtuką, kuris leidžia klientams informuoti parduotuvę, kad jie yra patalpose ir laukia, kol jų pakuotė bus jiems parengta. Tada klientai gauna įregistravimo patvirtinimą, o parduotuvė savo EKA programoje gauna pranešimą kaip užduotį. Ši užduotis naudojama kaip raginimas susieti pardavimą ir pristatyti užsakymą kliento transporto priemonei. Todėl klientas neturi įvesti parduotuvės.

Kliento įregistravimo darbo eigą taip pat galima konfigūruoti, kad iš klientų būtų renkama papildoma informacija, pvz., automobilio stovėjimo vietos numeris, transporto priemonės gamintojas, modelis ir spalva bei pristatymo instrukcijos. Parduotuvės lankomumo centras gali naudoti šią informaciją, kad galėtų lengviau įvykdyti užsakymą.

## <a name="enable-customer-check-in"></a>Įjungti kliento įregistravimą

Kai kliento įregistravimo funkcija įjungta, „Commerce" sugeneruoja užsakymo patvirtinimo ID (dar vadinamą kanalo nuorodos ID). Ji taip pat generuoja užsakymų, kurie kuriami naudojant kasos kodą (EKA) arba skambučių centro kanalus, užsakymų patvirtinimo ID. 

Norėdami įjungti kliento registravimo funkciją „Commerce“ štabe, atlikite šiuos žingsnius.

1. Eikite į **Darbo sritys \> Funkcijų valdymas**.
2. Ieškoti nuosekliojo **kanalo nuorodos ID formato kanalų** funkcijai generuoti. 
3. Pasirinkite norimą įjungti funkciją, tada dešinioje ypatybių juostoje pasirinkite **Įjungti dabar**. 

## <a name="create-a-check-in-confirmation-page"></a>Kurti įregistravimo patvirtinimo puslapį

Savo el. komercijos svetainėje turite sukurti naują puslapį, kuris bus naudojamas kaip įregistravimo patvirtinimo patirtis. Papildomas konfigūracijas puslapyje taip pat galima įtraukti formą, kuri renka papildomą klientų informaciją ir palengvina užsakymų vykdymą. Informacijos, kaip nustatyti puslapį ir modulį, ieškokite [Kliento įregistravimo modulyje](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>Operacijų el. laiško šablono konfigūravimas

Turite įtraukti aš čia esantį saitą arba mygtuką į operacijų el. laiško, kurį gauna klientai, kai jų užsakymas yra **parengtas** paimti, šabloną. Klientai naudoja šį saitą arba mygtuką, norėdami pranešti parduotuvei, kad ji buvo pristatyta, paimti užsakymą. 

Pridėti saitą arba mygtuką prie šablono, susieto su pranešimo apie pakavimą pranešimo tipu ir pristatymo režimu, kurį naudojate **pasipriešinimo** užsakymui vykdyti. Šablone sukurkite HTML saitą arba mygtuką, kuris nurodo jūsų sukurto patvirtinimo puslapio įregistravimo URL ir parametrų pavadinimus bei vertes, kaip pavaizduota šiame pavyzdyje.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

Daugiau informacijos apie el. laiškų šablonų konfigūravimą rasite [tinkinti el. laiškus pagal pristatymo](customize-email-delivery-mode.md) būdą. 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>EKA sukurta įregistravimo patvirtinimo užduotis

Klientui pranešus apie parduotuvę, kurioje jie yra paimti, įregistravimo puslapyje rodomas patvirtinimo pranešimas ir pasirinktinis QR kodas, kuriame yra kliento užsakymo patvirtinimo ID. Tuo pat metu užduotis sukuriama parduotuvės, kurioje klientas priima užsakymą, užduočių sąraše. Šią užduotį sudaro visa kliento ir užsakymo informacija, kurios reikia norint įvykdyti užsakymą. Užduoties instrukcijų lauke rodoma bet kokia informacija, kliento surinkta naudojant papildomos informacijos formą.

## <a name="end-to-end-testing"></a>Tikrinimas iki pabaigos

Kliento įsiregistravimas reikalauja, kad specialūs parametrai ir vertės būtų perduotos į įregistravimo puslapį, o tada kliento įregistravimo API. Todėl paprasčiausias būdas yra tikrinti priemonę aplinkoje, kurioje gali būti sukurtas ir supakuotas tikrinimo užsakymas. Tokiu būdu gali būti sugeneruotas "užsakymas paruoštas paėmimui", kuriame yra URL, kuriame yra būtini parametrų pavadinimai ir vertės.

Norėdami patikrinti kliento įregistravimo priemonę, atlikite šiuos veiksmus.

1. Sukurkite kliento įregistravimo puslapį, tada pridėkite ir sukonfigūruokite kliento įregistravimo modulį. Daugiau informacijos ieškokite [Įregistravimas, skirtas paėmimo moduliui](check-in-pickup-module.md). 
1. Tikrinkite puslapį, bet jo nepaskelbkite.
1. Pridėkite šią saitą prie el. laiško šablono, kurį iškviečiamas baigto pakavimo pranešimo tipas, kai naudojamas pristatymo paėmimo režimas. Daugiau informacijos rasite operacijų [įvykių el. laiškų šablonų kūrimas](email-templates-transactions.md).

    - **Išankstinių gamybų (UAT) aplinkose: įtraukite kodo fragmentą iš anksčiau šioje temoje skyriaus Konfigūruoti operacijų**[el](#configure-the-transactional-email-template). laiško šabloną.
    - **Gamybos aplinkose pridėkite** šį komentaro kodą, kad esami klientai nepakentė jų.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Kurti užsakymą, kuriame nurodytas paėmimo pristatymo būdas.
1. Kai gaunate el. laišką, kurį suaktyvino baigto pakavimo pranešimo tipas, patikrinkite įregistravimo srautą atidarydami įregistravimo puslapį, kuriame yra anksčiau įtrauktas URL. Kadangi URL apima vėliavėlę, prieš tai, kai galėsite peržiūrėti puslapį, `&preview=inprogress` būsite paraginti autentifikuoti.
1. Įveskite bet kokią papildomą informaciją, kurios reikia moduliui konfigūruoti.
1. Patikrinkite, ar įregistravimo patvirtinimo rodinys yra teisingai rodomas.
1. Atidarykite parduotuvės, kurioje bus paimtas užsakymas, EKA mokėjimo terminalą.
1. Pasirinkite **užsakymus, kuriuos norite paimti** išklotinės dalies, ir patikrinkite, ar užsakymas rodomas.
1. Patikrinkite, ar bet kokia papildoma įregistravimo modulyje sukonfigūruota informacija rodoma informacijos srityje.

Patikrinus, kad kliento įregistravimo priemonė veikia nuo pabaigos iki pabaigos, atlikite šiuos veiksmus.

1. Publikuoti įregistravimo puslapį.
1. Jei imate tikrinti gamybos aplinkoje, atsiekite URL atsiekite URL el. laiško šablone "Paruošta paimti" tam, kad būtų rodomas mano čia nuoroda **arba** mygtukas. Tada iš naujo įkelkite šabloną.

## <a name="additional-resources"></a>Papildomi ištekliai

[Registravimasis paėmimo moduliui](check-in-pickup-module.md)

[Tinkinti perlaidų el. paštus pagal pristatymo būdą](customize-email-delivery-mode.md)

[El. laiškų šablonų, skirtų operacijų įvykiams, kūrimas](email-templates-transactions.md)

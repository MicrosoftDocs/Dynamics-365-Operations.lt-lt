---
title: Įgalinti kliento įregistravimo pranešimus kasos punkte (EKA)
description: Šioje temoje aprašoma, kaip įgalinti kliento įregistravimo pranešimus į „Microsoft Dynamics 365 Commerce“ kasos kodą (EKA).
author: bicyclingfool
ms.date: 04/23/2021
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
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271430"
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

Pridėti saitą arba mygtuką prie šablono, susieto su pranešimo apie pakavimą pranešimo tipu ir pristatymo režimu, kurį naudojate **pasipriešinimo** užsakymui vykdyti. Šablone sukurkite HTML saitą arba mygtuką, kuris nurodo jūsų sukurto patvirtinimo puslapio URL. Toliau pateikiamas pavyzdys.

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
Daugiau informacijos apie el. laiškų šablonų konfigūravimą rasite [tinkinti el. laiškus pagal pristatymo](customize-email-delivery-mode.md) būdą. 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>EKA sukurta įregistravimo patvirtinimo užduotis

Klientui pranešus apie parduotuvę, kurioje jis yra paėmimo atveju, jis gavo įregistravimo patvirtinimo pranešimą ir užduotis sukuriama parduotuvės, kurioje klientas priima užsakymą, užduočių sąraše. Užduotyje yra visa kliento ir užsakymo informacija, kurios reikia norint įvykdyti užsakymą. Užduoties metu instrukcijų lauke rodoma bet kokia informacija, kliento surinkta naudojant papildomos informacijos formą. 

## <a name="additional-resources"></a>Papildomi ištekliai

[Registravimasis paėmimo moduliui](check-in-pickup-module.md)

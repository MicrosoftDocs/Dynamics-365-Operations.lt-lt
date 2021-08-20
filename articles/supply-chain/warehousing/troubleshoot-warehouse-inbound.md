---
title: Trikčių šalinimo įvesties sandėlio veiksmai
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su įvesties sandėli veiksmais „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6d7fcb2ed32c57b8701bee5b90889a0a63e1f7061aa9014480ae8c543e1f229a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748672"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Trikčių šalinimo įvesties sandėlio veiksmai

[!include [banner](../includes/banner.md)]

Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su įvesties sandėli veiksmais „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Gautu tolesnį klaidos pranešimą: „Kokybės užsakymas %1 buvo sukurtas. Klasterio profilio nepavyko rasti, prašome patikrinti konfigūravimą."

### <a name="issue-description"></a>Problemos aprašas

Šis klaidos pranešimas yra susijęs su gavimo procesu, nes kokybės valdymas (QMS) yra įjungtas. Priklausomai nuo konfigūravimų jūsų aplinkoje, papildoma informacija apie perlaidą, sukurianti klaidos pranešimą, gali padėti ištaisyti triktį.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Pirmiausia, peržiūrėkite [klasterio paėmimo](set-up-cluster-picking.md) nustatymus ir įsitikinkite, kad klasterio profiliai yra tinkamai nustatyti. Negalite naudoti prekės mobiliojo įrenginio meniu klasterio paėmimui nebent klasterio profilis yra nustatytas. Priklausomai nuo aplinkos, galbūt jums reikės peržiūrėti taip pat kitas susijusias konfigūracijas.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Maišytos licencijos plokštelės gavimas neveikia jokiam suteiktam kodui, išskyrus kredito.

### <a name="issue-description"></a>Problemos aprašas

Kai **Veiksmo** laukelis nustatytam kodui yra nustatytas *Kreditas* ar *Atmestas*, galite naudoti tik [Maišytos licencijos plokštelės gavimas](mixed-license-plate-receiving.md) meniu prekės į proceso sugrąžintas prekes.

### <a name="issue-resolution"></a>Problemos paaiškinimas

„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą. Šiuo metu tik [suteikti kodai](../service-management/set-up-disposition-codes.md), kai **Veiksmo** laukelis yra nustatytas į *Kreditai* ar *Atmestas* yra palaikomi maišytos licencijos plokštelės gavime.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Man vykdant naujinimo produkto gavimų periodinę užduotį, nepatvirtinti pirkimo užsakymai yra patvirtinami.

### <a name="issue-description"></a>Problemos aprašas

Man įvykdžius *Naujinimo produkto gavimų* periodinę užduotį, sistema automatiškai patvirtina nepatvirtintus pirkimo užsakymus, kurie turi inventoriaus perlaidos būseną *Registruotą*.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Nauja įvesties apkrovos tvarkymo funkcija, *Per krovinio kiekių gavimą*, ištaiso šią triktį. Norėdami įjungti šią funkciją, eikite į [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį ir įjunkite tolesnes funkcijas (tam, kad jos būtų sąraše):

1. Susieti pirkimo užsakymo atsargų operacijas su kroviniu
1. Krovinio kiekio perviršis

Dėl išsamesnės informacijos, žr. [Publikuoti registruotus produktų kiekius pagal pirkimo užsakymus](inbound-load-handling.md#post-registered-quantities).

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>Registruodamas gaunamus užsakymus, gaunu tokį klaidos pranešimą: „Netinkamas kiekis.”

### <a name="issue-description"></a>Problemos aprašas

Jeigu laukas **Numerio lentelių grupavimo politika** nustatytas į *Vartotojo apibrėžtas* mobiliojo įrenginio meniu elementui, naudojamam registruoti gaunamiems užsakymams, gausite klaidos pranešimą („Netinkamas kiekis”) ir negalėsite užbaigti registracijos.

### <a name="issue-cause"></a>Problemos priežastis

Kai *Vartotojo apibrėžta* yra naudojama kaip registracijos numerių grupavimo strategija, sistema išskaido gaunamas atsargas į atskiras numerio lenteles, kaip nurodyta pagal vienetų sekų grupę. Jeigu paketo ar serijos numeriai yra naudojami gaunamai prekei sekti, kiekvieno paketo ar serijos kiekiai turi būti nurodyti užregistruotoje numerio lentelėje. Jeigu numerio lentelėje nurodytas kiekis viršija kiekį, kurį vis dar reikia gauti pagal dabartines dimensijas, gausite klaidos pranešimą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Kai registruojate prekę naudodami mobiliojo įrenginio meniu elementą, kurio laukas **Numerio lentelių grupavimo strategija** nustatytas į *Vartotojo apibrėžta*, sistema gali reikalauti, kad patvirtintumėte arba įvestumėte numerio lentelės, paketo arba serijos numerius.

Numerio lentelės patvirtinimo puslapyje sistema rodys kiekį, priskirtą dabartinei numerio lentelei. Paketo arba serijos patvirtinimo puslapiuose sistema rodys kiekį, kuris vis dar turi būti gautas pagal dabartinę numerio lentelę. Juose taip pat bus laukas, kuriame galite įvesti registruotiną kiekį tam numerio lentelės ir paketo ar serijos numerio deriniui. Tokiu atveju įsitikinkite, kad registruojamas numerio lentelės kiekis neviršija kiekio, kuris vis dar turi būti gautas.

Kitu atveju, jei gavimo užsakymo registracijoje generuojama per daug numerio numerių, lauko **Numerio lentelių grupavimo strategija** reikšmė gali pasikeisti į *Numerio lentelių grupavimas*, nauja vienetų sekos grupės gali būti priskirta prekei arba parinktis **Numerio lentelių grupavimas** vienetų sekos grupei gali būti deaktyvuota.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

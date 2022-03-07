---
title: Aptarnavimo užsakymai
description: Šioje temoje pateikiama apžvalga, kaip dirbti su aptarnavimo užsakymai.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8dc88d445e1331e1532cb3b7385cda39c4f22e80
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566124"
---
# <a name="service-orders"></a>Aptarnavimo užsakymai

[!include [banner](../includes/banner.md)]

Aptarnavimo užsakymas rodo techniko apsilankymą pas klientą tam tikrą dieną. Kiekvieną aptarnavimo užsakymą sudaro viena arba daugiau aptarnavimo užsakymo eilučių. Aptarnavimo užsakymo eilutėse rodomos privalomos techniko darbo valandos ir susijusios prekės, išlaidos bei mokesčiai.

Prie aptarnavimo užsakymo eilutės galite pridėti užduočių ir objektų. Po to galite galite grupuoti aptarnavimo užsakymo eilutes pagal užduotį arba objektą. Taip pat prie aptarnavimo užsakymo eilučių galima pridėti atsargose išvardytų prekių.

## <a name="create-service-orders"></a>Kurti aptarnavimo užsakymus

Pagal aptarnavimo sutartį ir tos sutarties eilutes galite sukurti aptarnavimo užsakymus. Tačiau galite sukurti aptarnavimo užsakymus, kurie susieti su aptarnavimo sutartimi tik sutartyje nurodytu laikotarpiu. Pavyzdžiui, jei aptarnavimo sutartis galioja 2011 kalendoriniams metams, galite sukurti sutarties aptarnavimo užsakymą nuo 2011 m. sausio 1 d. iki 2011 m. gruodžio 31 d.

Taip pat galite sukurti atskirus aptarnavimo užsakymus, nesusiedami jų su sutartimi. Šiuos aptarnavimo užsakymus galima panaudoti apdorojant nesuplanuotus arba vienkartinius aptarnavimo vizitus. Pavyzdžiui, kovo mėnesį jūsų klientas nori, kad aptarnavimas būtų atliktas dviem mašinoms, neskaitant aptarnavimo sutartyje nurodytų mašinų. Šiai užduočiai sukuriate aptarnavimo užsakymus, bet nesusiejate jų su sutartimi.


> [!NOTE]
> Norėdami sukurti su aptarnavimo sutartimi nesusietus aptarnavimo užsakymus, formoje **Aptarnavimo valdymo parametrai** turite pažymėti žymės puslapį **Leisti be aptarnavimo sutarties**.

### <a name="scenario"></a>Scenarijus

Toliau pateiktoje situacijoje aprašoma kita situacija, kurioje naudinga sukurti su aptarnavimo sutartimi nesusietą aptarnavimo užsakymą.

Įmonės dispečeris sulaukia skambučio dėl skubaus elevatoriaus remonto. Nėra laiko paruošti aptarnavimo sutartį ir aptarnavimo projektą. Todėl dispečeris aptarnavimo užsakymą sukuria tiesiogiai pusalpyje **Aptarnavimo užsakymai**, prie esamo projekto prideda aptarnavimo užsakymą ir sukuria aptarnavimo užsakymo eilutes. Esamam aptarnavimo užsakymui dispečeris taip pat sukuria užduoties arba objekto ryšį, kad būtų galima įrašyti su aptarnavimo sutartimi nesusijusį darbą. Daugiau informacijos rasite failuose [Neautomatinis aptarnavimo užsakymų kūrimas](create-service-orders-manually.md) ir [Aptarnavimo užduočių ryšių kūrimas](create-service-task-relations.md).

## <a name="monitor-the-progress-of-service-orders"></a>Stebėkite aptarnavimo užsakymų vykdymo eigą

Norėdami stebėti pardavimo užsakymo vykdymo eigą (pagal įvairias komandas ir darbo procesus), galite nustatyti aptarnavimo užsakymų etapų sistemą ir priežasčių kodus. Galite nurodyti leistinus kiekvieno etapo veiksmus. Daugiau informacijos rasite faile [Priežasčių kodų kūrimas](create-reason-codes.md).

### <a name="example"></a>Pavyzdys

Aptarnavimo užsakymą patvirtina dispečeris. Dispečeris atnaujina aptarnavimo užsakymo etapą ir nurodo priežasties kodą, reiškiantį, kad aptarnavimo užsakymas perduotas aptarnaujančiam technikui. Technikas vyksta pas klientą ir atlieka aptarnavimo darbus.

## <a name="specify-item-requirements-for-service-orders"></a>Prekių poreikių nurodymas pagal aptarnavimo užsakymus

Galite nurodyti aptarnavimo užsakymams vykdyti reikiamas atsargų prekes. Tačiau aptarnavimo užsakymas turi būti susietas su projektu. Prekės poreikiai aptarnavimo užsakymuose apdorojami vykdant projektą. 

### <a name="example"></a>Pavyzdys

Pagal aptarnavimo sutartį sukurtus aptarnavimo užsakymus apdoroja dispečeris. Dispečeris pastebi, kad norint įvykdyti pirmą aptarnavimo užsakymą technikui prireiks svarbios atsarginės detalės, kurios nėra atsargose. Todėl tiesiogiai aptarnavimo užsakyme dispečeris sukuria tos atsarginės dalies prekės poreikį.

## <a name="move-and-post-lines"></a>Eilučių perkėlimas ir registravimas

Aptarnavimo technikas grįžta po aptarnavimo vizito ir pakeičia bei atnaujina aptarnavimo užsakymo eilutes. Per šį aptarnavimo vizitą technikas taip pat atliko aptarnavimo užduotį, kurią buvo suplanuota atlikti per kitą aptarnavimo vizitą. Todėl kito aptarnavimo vizito eilutes technikas perkelia į dabartinį aptarnavimo vizitą. Po to technikas užregistruoja aptarnavimo užsakymą. Daugiau informacijos rasite faile [Aptarnavimo užsakymų eilučių perkėlimas](move-service-order-lines.md).

## <a name="cancel-service-orders"></a>Atšaukti aptarnavimo užsakymus

Vienas iš kitų sausio mėnesiui sugeneruotų aptarnavimo užsakymų tampa nereikalingas, nes užduotis atšaukta. Todėl dispečeris atšaukia aptarnavimo užsakymą. Daugiau informacijos rasite faile [Aptarnavimo užsakymų atšaukimas](cancel-service-orders.md).

## <a name="post-from-projects"></a>Registravimas iš projektų

Kiekvienos savaitės pabaigoje dispečeris nori užregistruoti visus prie tam tikro projekto pridėtus aptarnavimo užsakymus. Todėl dispečeris suranda reikiamą projektą puslapyje **Projektai** ir užregistruoja įvykdytus aptarnavimo užsakymus. Daugiau informacijos ieškokite [Aptarnavimo užsakymų registravimas (klasės forma)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).

## <a name="delete-service-orders"></a>Naikinti aptarnavimo užsakymus

Antroje metų pusėje jūsų klientas nusprendžia, kad aptarnavimo vizitai pernelyg reti. Likusiam aptarnavimo sutarties laikotarpiui turite sukurti naują, dažnesnių apsilankymų seriją. Todėl reikia panaikinti esamus aptarnavimo užsakymus ir sukurti naujus. Daugiau informacijos rasite faile [Aptarnavimo užsakymų naikinimas](delete-service-orders.md).

## <a name="see-also"></a>Taip pat žiūrėkite

[Aptarnavimo užsakymai (forma)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
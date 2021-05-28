---
title: Ribinės vertės ir išimčių ribinės vertės riba
description: Šioje temoje aprašomos ribinės ir išimčių ribos, taikomos šaltinyje (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1bf0d3a01ede559d288581d3b58b3777d0e608dc
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023442"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>Ribinės vertės ir išimčių ribinės vertės riba

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos ribinės ir išimčių ribos, taikomos šaltinyje (TDS). TDS SF ir mokėjimuose visada skaičiuojami atsižvelgiant į ribinės ir išimčių ribinės vertės ribą, nurodytą TDS mokesčių komponentams **išskaitomo mokesčio komponentų** puslapyje. TDS mokesčio komponentai pridėti prie TDS mokesčių kodų, kurie įtraukiami į TDS mokesčių grupes. TDS mokesčių grupės pridedamos tiekėjams ir klientams, kad TDS būtų skaičiuojama SF arba mokėjimo lygiu.

TDS skaičiuojamas, jei operacijos suma arba sukauptos operacijos, užregistruotos su konkrečia tiekėjo TDS grupe, viršija ribą, nurodytą **išskaitomo mokesčio komponentų** puslapyje. TDS nebus skaičiuojamas, kol kaupiamoji operacijos suma viršija nurodytą ribinės vertės ribą.

Jei ribinė išimties riba yra nurodyta kartu su TDS komponento ribinė riba, TDS skaičiuojama, kai konkrečios operacijos suma viršija išimties ribinės vertės ribą, net jei kaupiamoji operacijos suma neviršija nurodytos ribinės ribos.

### <a name="example"></a>Pavyzdys
Mokesčių komponentas vadinamas TDS, nustatomas ir pridedamas prie TDS mokesčių grupės, vadinamos Rangovas. Ribinė vertė nustatyta kaip 50 000, o TDS mokesčio komponento išimties ribinė vertė nurodyta kaip 20 000. TDS grupės rangovas apibrėžiamas kaip numatytoji tiekėjo 1 TDS grupė.

Užregistruojama 1 tiekėjo 10 000 pirkimo SF. SF TDS neskaičiuojama, nes SF suma perėjo ribinės arba išimties ribinės vertės ribą. Užregistruojama 002 tiekėjo 25 000 pirkimo SF. SF TDS neskaičiuojama, nes SF suma perėjo ribinės arba išimties ribinės vertės ribą. Užregistruojama 003 Tiekėjo 20 000 pirkimo SF. SF TDS apskaičiuojamas, nes bendroji trijų tiekėjo išduotų SF suma perėjo ribinę vertę. TDS skaičiuojama pagal visas tiekėjui išduotas SF, kurių TDS nebuvo apskaičiuotos anksčiau. Todėl TDS yra skaičiuojama 30 000; tai yra bendroji SF 001 ir 003 SF suma.

Ribinė vertė ir išlygos slenksčio limitas nėra įtraukti į TDS skaičiavimą, jei **Peržiūros slenksčio** žymimas laukelis yra pasirinktas TDS mokesčio kodams TDS grupėje, kuri įtraukta į operaciją. Ribinė riba nebus naudojama TDS mokesčių koduose, TDS grupėje, kurios žymės langelis **Besiribojantis su slenksčiu** yra skirtas.

Jei **Besiribojantis su slenksčiu** žymimas laukelis yra pasirinktas konkrečiai TDS grupei kai kurioms SF, bet nepasirinktas kitoms sąskaitoms, kurios sukuriamos konkrečiam tiekėjui ar klientui, TDS skaičiavimas be peržiūros slenksčio limito kelioms sąskaitoms gali vykti atsižvelgiant į bendras sumas visų sąskaitų, kuriose TDS nebuvo anksčiau suskaičiuotas.

Pavyzdžiui, ribinė riba yra 25 000. Tolesnės sąskaitos sukurtos Tiekėjui A.

- 1 SF – 20000 – (**neparinktas žymės** langelis): TDS neskaičiuojamas.

- 2 SF – 4000 – neparinktas (**žymės langelis** DSS neskaičiuojamas): TDS yra 4000.

- Sąskaita 2 – 3000 – (**Nepasirinktas žymės** langelis): Be išlaidų: TDS apskaičiuojama kaip kaupiamoji SF suma, t. y. 27000 (20000+4000+3000) viršijo ribinės vertės ribą. TDS skaičiuojama pagal kaupiamąją SF sumą, kurios TDS nebuvo apskaičiuotas anksčiau, t. 23 000 (20000+3000).

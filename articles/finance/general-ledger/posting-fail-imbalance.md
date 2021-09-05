---
title: Žurnalo registravimo triktis dėl disbalanso
description: Šioje temoje paaiškinama, kodėl kvitų operacijose gali būti nesubalansuoti debetai ir kreditai, todėl jų negalima registruoti. Temoje taip pat yra išdavimo taisymo veiksmai.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a59724ff698b6ad0e84b0642240da5f8953ab3d1
ms.sourcegitcommit: 9642494da87c0d237f9fcbe15df14315d9e88fa2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/15/2021
ms.locfileid: "7385728"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Žurnalo registravimo triktis dėl disbalanso

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kodėl kvitų operacijose gali būti nesubalansuoti debetai ir kreditai, todėl jų negalima registruoti. Temoje taip pat yra išdavimo taisymo veiksmai.

## <a name="symptom"></a>Požymis

Kai kuriais atvejais žurnalo registruoti negalima, ir rodomas šis pranešimas: "Konkretaus kvito operacijos tam tikrą datą nesubalansuos (apskaitos valiuta: 0,01 – ataskaitų valiuta: 0,06)." Kodėl žurnalas nėra publikuojamas?

## <a name="resolution"></a>Sprendimas

Registruojant DK kiekvienas kvitas turi būti subalansuotas operacijos valiuta, apskaitos valiuta ir ataskaitų valiuta, jei šios valiutos yra apibrėžtos **DK nustatymo** puslapyje. (Kvitai subalansuoti, kai bendra debeto suma lygi viso kredito sumai.)

Žurnalo eilučių puslapio apačioje bendrosios sumos rodomos apskaitos valiuta ir ataskaitų valiuta. Jie **nerodoma** operacijos valiuta užsienio valiutos operacijoms. Be to, klaidos pranešimas, kurį vartotojai gauna modeliavimo ar registravimo metu, rodo skirtumus tik apskaitos valiuta ir ataskaitų valiuta. Jis nerodo jų operacijos valiuta, kadangi viename kvite gali būti daugiau nei viena operacijos valiuta, o žurnale gali būti kvitų skirtingomis operacijų valiutomis. Todėl svarbu įsitikinti, ar kiekvieno kvito operacijos valiutos sumos yra subalansuotos.

### <a name="transaction-currency"></a>Operacijos valiuta

Modeliavimo ir registravimo metu sistema patikrina, ar kiekvienas kvitas yra subalansuotas operacijos valiuta. Kiekviename įvestame kvite gali būti viena ar daugiau operacijos valiutos valiutų. Pavyzdžiui, kvitas, kuris įvestas į bendrąjį žurnalą, gali turėti dvi operacijų valiutas, kai grynieji pinigai perkeliami iš banko sąskaitos, kurioje naudojami eurais (EUR) į banko sąskaitą, kurioje naudojami Kanados doleriai (CAD).

Jei kvite yra tik viena operacijos valiuta, bendra debeto suma turi būti lygi kvito bendrai kredito sumai. Klientai aptiko šiuos scenarijus, kuriuose nepavyko tinkamai registruoti, nes nebuvo subalansuotos operacijos valiutos sumos:

- Bendras debetas ir visi kreditai nesubalansuoti operacijos valiuta, bet jie buvo subalansuoti **nebuvo** su apskaitos valiuta ir ataskaitų valiuta. Klientas laikė, kad kvitas vis tiek bus registruojamas. Tačiau ši prielaida buvo klaidinga. **Operacijos valiutos sumos kvite visada turi būti subalansuotos, kai visose kvito eilutėse yra ta pati valiuta.**
- Kvitas buvo importuotas „Microsoft Excel“ naudojant, o vartotojas apgalvoo, kad operacijos valiutos sumos buvo subalansuotos. Excel darbaknygėje importuotos sumos buvo nustatytos kaip **skaitinės** vertės, o ne **valiutos** vertės. Šiame scenarijuje skaitinės sumos darbaknygėje buvo su daugiau nei dviem dešimtainėmis dalimis ir importuotos sumos buvo įtrauktos daugiau nei dviem dešimtainėmis dalimis. Todėl debetai nebuvo lygūs kreditams, nes jie buvo lygūs centų trupmenai. Žurnalas neatrodė šio skirtumo kvito eilutėse, nes rodomos sumos turi tik du dešimtainius skaičius po kablelio.
- Kvitas buvo importuotas „Excel“ naudojant, o vartotojas apgalvoo, kad operacijos valiutos sumos buvo subalansuotos. Nors kvitas buvo subalansuotas, kai kurių kvito eilučių operacijų datos skiriasi. Jei pridėjote bendrą debetą ir bendrą kreditą pagal kvitą ir operacijos datą, jie nebus subalansuoti. Dabar sistema apsaugo šį scenarijų. Kvite gali būti tik viena operacijos data. Šis reikalavimas taikomas, kai įvedate kvitą per bendrąjį žurnalą sistemoje. Tačiau, ji nebuvo iš pradžių nustatyta, kai kvitas buvo importuotas per Excel.

Viename palaikomame scenarijuje kvitas gali turėti daugiau nei vieną operacijos valiutą. Šiuo atveju sistema nepatikrinta, ar debetai lygūs kreditams operacijos valiuta, nes **neatitinka** valiutų. Vietoj to sistema patikrina, ar apskaitos valiutos sumos yra subalansuotos.

### <a name="accounting-currency"></a>Apskaitos valiuta

Jei visų kvito eilučių operacijos valiuta yra ta pati, o operacijos valiutos sumos yra subalansuotos, sistema patikrina, ar apskaitos valiutos sumos yra subalansuotos. Jei kvitas įvestas užsienio valiuta, kvito eilučių valiutos kursas naudojamas operacijos valiutos sumoms į apskaitos valiutą versti. Pirma, kiekviena kvito eilutė yra išversta. Tada eilutės sumuojamos, kad būtų galima nustatyti bendrą debetą ir bendrą kreditą. Kadangi kiekviena eilutė yra išversta, gali būti nesubalansuoti visi debetai ir visi kreditai. Neatsižvelgiant į tai, ar skirtumas yra didesnis nei **maksimali centų skirtumo** vertė, kuri nustatyta **DK parametrų** puslapyje, kvitas bus užregistruotas, o skirtumas automatiškai užregistruojamas centų skirtumo sąskaitoje.

Jei kvite yra daugiau nei viena operacijos valiuta, kiekviena kvito eilutė konvertuojama į apskaitos valiutą, tada eilutės sumuojamos, kad būtų galima nustatyti bendrą debetą ir bendrą kreditą. Norint būti subalansuoti, reikia subalansuoti debetus ir kreditus bei neturi būti apvalinimo centais skirtumo.

### <a name="reporting-currency"></a>Ataskaitų valiuta

Jei visų kvito eilučių operacijos valiuta yra ta pati, o operacijos valiutos sumos yra subalansuotos, sistema patikrina, ar apskaitos valiutos sumos yra subalansuotos. Jei kvitas įvestas užsienio valiuta, kvito eilučių valiutos kursas naudojamas operacijos valiutos sumoms į apskaitos valiutą versti. Pirma, kiekviena kvito eilutė yra išversta. Tada eilutės sumuojamos, kad būtų galima nustatyti bendrą debetą ir bendrą kreditą. Kadangi kiekviena eilutė yra išversta, gali būti nesubalansuoti visi debetai ir visi kreditai. Neatsižvelgiant į tai, ar skirtumas yra didesnis nei **maksimali centų skirtumo apvalinimo ataskaitos valiutoje** vertė, kuri nustatyta **DK parametrų** puslapyje, kvitas bus užregistruotas, o skirtumas automatiškai užregistruojamas centų skirtumo sąskaitoje.

Jei kvite yra daugiau nei viena operacijos valiuta, kiekviena kvito eilutė konvertuojama į apskaitos valiutą, tada eilutės sumuojamos, kad būtų galima nustatyti bendrą debetą ir bendrą kreditą. Norint būti subalansuoti, reikia subalansuoti debetus ir kreditus bei neturi būti apvalinimo centais skirtumo.

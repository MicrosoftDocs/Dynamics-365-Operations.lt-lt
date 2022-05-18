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
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 07408e608496dcc19562b866449b3b27f5f80edd
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719938"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Žurnalo registravimo triktis dėl disbalanso

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kodėl kvitų operacijose gali būti nesubalansuoti debetai ir kreditai, todėl jų negalima registruoti. Temoje taip pat yra išdavimo taisymo veiksmai.

## <a name="symptom"></a>Požymis

Kai kuriais atvejais žurnalo registruoti negalima, ir rodomas šis pranešimas: "Konkretaus kvito operacijos tam tikrą datą nesubalansuos (apskaitos valiuta: 0,01 – ataskaitų valiuta: 0,06)." Kodėl žurnalas nėra publikuojamas?

## <a name="resolution"></a>Sprendimas

Registruojant DK kiekvienas kvitas turi būti subalansuotas operacijos valiuta, apskaitos valiuta ir ataskaitų valiuta, jei šios valiutos yra apibrėžtos **DK nustatymo** puslapyje. (Kvitai subalansuoti, kai bendra debeto suma lygi viso kredito sumai.)

Žurnalo eilučių puslapio apačioje bendrosios sumos rodomos apskaitos valiuta ir ataskaitų valiuta. Jie **nerodoma** operacijos valiuta užsienio valiutos operacijoms. Be to, klaidos pranešimas, kurį vartotojai gauna modeliavimo ar registravimo metu, rodo skirtumus tik apskaitos valiuta ir ataskaitų valiuta. Jis nerodo jų operacijos valiuta, kadangi viename kvite gali būti daugiau nei viena operacijos valiuta, o žurnale gali būti kvitų skirtingomis operacijų valiutomis. Todėl svarbu rankiniu būdu patikrinti, ar sandorio valiutos sumos už kiekvieną čekį, kuriame yra tik viena operacijos valiuta, yra subalansuotos.

### <a name="transaction-currency"></a>Operacijos valiuta

Modeliavimo ir registravimo metu sistema patikrina, ar kiekvienas kvitas, kuris turi tik vieną sandorio valiutą, yra subalansuotas operacijos valiuta. Kiekviename įvestame kvite gali būti viena ar daugiau operacijos valiutos valiutų. Pavyzdžiui, kvitas, kuris įvestas į bendrąjį žurnalą, gali turėti dvi operacijų valiutas, kai grynieji pinigai perkeliami iš banko sąskaitos, kurioje naudojami eurais (EUR) į banko sąskaitą, kurioje naudojami Kanados doleriai (CAD).

Jei kvite yra tik viena operacijos valiuta, bendra debeto suma turi būti lygi kvito bendrai kredito sumai sandorio valiuta. Klientai aptiko šiuos scenarijus, kuriuose nepavyko tinkamai registruoti, nes nebuvo subalansuotos operacijos valiutos sumos:

- Bendras debetas ir visi kreditai nesubalansuoti operacijos valiuta, bet jie buvo subalansuoti **nebuvo** su apskaitos valiuta ir ataskaitų valiuta. Klientas laikė, kad kvitas vis tiek bus registruojamas. Tačiau ši prielaida buvo klaidinga. **Operacijos valiutos sumos kvite visada turi būti subalansuotos, kai visose kvito eilutėse yra ta pati operacijos valiuta.**
- Kvitas buvo importuotas su duomenų objektu per duomenų valdymo sistemą (DMF), o vartotojas pagalvojo, kad operacijos valiutos sumos buvo subalansuotos. Šiame importuojamame faile, kai kurios skaitinės sumos darbaknygėje buvo su daugiau nei dviem dešimtainėmis dalimis ir importuotos sumos buvo įtrauktos daugiau nei dviem dešimtainėmis dalimis. Todėl debetai nebuvo lygūs kreditams, nes jie buvo lygūs centų trupmenai. Žurnalas neatrodė šio skirtumo kvito eilutėse, nes rodomos sumos turi tik du dešimtainius skaičius po kablelio.
- Kvitas buvo importuotas, naudojant objekto duomenis per DMF ir vartotojas pagalvojo, kad operacijos valiutos sumos buvo subalansuotos. Nors **kvitas** buvo subalansuotas, kai kurių kvito eilučių operacijų datos skiriasi. Jei pridėjote bendrą debetą ir bendrą kreditą operacijos valiuta pagal **kvitą ir operacijos datą**, jie nebuvo subalansuoti. Šis reikalavimas taikomas, kai įvedate kvitą per bendrąjį žurnalą sistemoje. Tačiau, tai nėra vykdoma, kai kvitas yra importuojamas su duomenų objektu per DMF.

Viename palaikomame scenarijuje kvitas gali turėti daugiau nei vieną operacijos valiutą. Šiuo atveju sistema nepatikrinta, ar debetai lygūs kreditams operacijos valiuta, nes **neatitinka** valiutų. Vietoj to sistema patikrina, ar apskaitos valiutos ir ataskaitos valiutos sumos yra subalansuotos.

### <a name="accounting-currency"></a>Apskaitos valiuta

Jei visų kvito eilučių operacijos valiuta yra ta pati, o operacijos valiutos sumos yra subalansuotos, sistema patikrina, ar apskaitos valiutos sumos yra subalansuotos. Jei kvitas įvestas užsienio valiuta, kvito eilučių valiutos kursas naudojamas operacijos valiutos sumoms į apskaitos valiutą versti. Pirma, kiekviena kvito eilutė konvertuojama ir apvalinama iki dviejų dešimtainių dalių. Tada eilutės sumuojamos, kad būtų galima nustatyti bendrą debetą ir bendrą kreditą. Kadangi kiekviena eilutė yra išversta, gali būti nesubalansuoti visi debetai ir visi kreditai. Neatsižvelgiant į tai, ar absoliučios vertės skirtumas yra didesnis nei **Maksimali centų skirtumo** vertė, kuri nustatyta **DK parametrų** puslapyje, kvitas bus užregistruotas, o skirtumas automatiškai užregistruojamas centų skirtumo sąskaitoje.

Jei kvite yra daugiau nei viena operacijos valiuta, kiekviena kvito eilutė konvertuojama į apskaitos valiutą, tada eilutės sumuojamos, kad būtų galima nustatyti bendrą debetą ir bendrą kreditą. Kad būtų subalansuota, debetai ir kreditai turi būti subalansuoti apskaitos valiuta.  Skirtumo centais sąskaita niekada neįrašoma į kvitą apskaitos valiuta, kad debetas ir kreditas būtų subalansuoti. 

### <a name="reporting-currency"></a>Ataskaitų valiuta

Jei visų kvito eilučių operacijos valiuta yra ta pati, o operacijos valiutos sumos yra subalansuotos, sistema patikrina, ar apskaitos valiutos sumos yra subalansuotos. Jei kvitas įvestas užsienio valiuta, kvito eilučių valiutos kursas naudojamas operacijos valiutos sumoms į apskaitos valiutą versti. Pirma, kiekviena kvito eilutė konvertuojama ir apvalinama iki dviejų dešimtainių dalių. Tada eilutės sumuojamos, kad būtų galima nustatyti bendrą debetą ir bendrą kreditą. Kadangi kiekviena eilutė yra išversta, gali būti nesubalansuoti visi debetai ir visi kreditai. Neatsižvelgiant į tai, ar skirtumas yra didesnis nei **maksimali centų skirtumo apvalinimo ataskaitos valiutoje** vertė, kuri nustatyta **DK parametrų** puslapyje, kvitas bus užregistruotas, o skirtumas automatiškai užregistruojamas centų skirtumo sąskaitoje.

Jei kvite yra daugiau nei viena operacijos valiuta, kiekviena kvito eilutė konvertuojama į ataskaitų valiutą, tada eilutės sumuojamos, kad būtų galima nustatyti bendrą debetą ir bendrą kreditą. Kad būtų subalansuota, debetai ir kreditai turi būti subalansuoti ataskaitų valiuta.  Skirtumo centais sąskaita niekada neįvedami į kvitą ataskaitų valiuta, kad debetai ir kreditai subalansuoti.

### <a name="example-for-an-accounting-currency-imbalance"></a>Apskaitos valiutos disbalanso pavyzdys

> [!NOTE]
> Ataskaitų valiutos suma skaičiuojama iš operacijos valiutos sumos tuo pačiu būdu, kaip ir apskaitos valiutos suma.

Valiutos kursas: 1.5

| Eilutė | Kvitas | Paskyra | Valiuta | Debetas (Operacija) | Kreditas (Operacija) | Debetas (Apskaita) | Kredito (Apskaita) |
|---|---|---|---|---|---|---|---|
| 1 | 001 | 1101–01 | EUR | 3.33 | | 5.00 (4.995) | |
| 2 | 001 | 1101–02 | EUR | 3.33 | | 5.00 (4.995) | |
| 3 | 001 | 1101–03 | EUR | 3.34 | | 5.01 | |
| 4 | 001 | 4101- | EUR | | 10,00 | | 15.00 |
| **Bendroji suma** | | | | **10.00** | **10.00** | **15.01** | **15.00** |

Apskaitos valiutos balansas neviršija 0,01. Tačiau, jei maksimalus apvalinimas centais apskaitos valiuta yra mažiausiai 0,01, skirtumas automatiškai užregistruojamas centų skirtumo sąskaitoje, ir kvitas bus sėkmingai užregistruotas.

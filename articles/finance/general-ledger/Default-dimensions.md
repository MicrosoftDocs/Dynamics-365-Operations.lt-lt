---
title: Finansinės dimensijos ir registravimas
description: Planuodami ir nustatydami sąskaitų planą turite apsvarstyti, kaip įvairūs komponentai veiks kartu registruojant dokumentą ar žurnalą. Šie komponentai apima sąskaitų struktūras, išplėstines taisykles, balansavimą ir fiksuotas dimensijas. Šioje temoje paaiškinta, kas yra kiekvienas komponentas ir kaip komponentai veikia kartu.
author: aprilolson
manager: AnnBe
ms.date: 08/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a6179841259186c8438c72bb4a4f9cd2bf5dbaa8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985092"
---
# <a name="financial-dimensions-and-posting"></a>Finansinės dimensijos ir registravimas 

[!include [banner](../includes/banner.md)]

Planuodami ir nustatydami sąskaitų planą turite apsvarstyti, kaip įvairūs komponentai veiks kartu registruojant dokumentą ar žurnalą. Šie komponentai apima sąskaitų struktūras, išplėstines taisykles, balansavimą ir fiksuotas dimensijas. Šioje temoje paaiškinta, kas yra kiekvienas komponentas ir kaip komponentai veikia kartu.

## <a name="chart-of-accounts-and-financial-dimension-components"></a>Sąskaitų plano ir finansinių dimensijų komponentai

Išsami taisyklėmis pagrįsta sistema, naudojama pagrindinių sąskaitų ir finansinių dimensijų tinkamų derinių apibrėžimui. Šiame skyriuje trumpai apžvelgiamos kiekvienos sudedamosios dalies funkcijos ir paaiškinama, kur galima rasti komponentą.

### <a name="account-structures"></a>Sąskaitų struktūros

Nustatant didžiąją knygą būtina sąskaitos struktūra. Būtina apibrėžti ir suaktyvinti bent vieną sąskaitos struktūrą, be to, ją būtina priskirti DK. Sąskaitos struktūroje turi būti pagrindinė sąskaita. Galima nurodyti segmentų tvarką, kuri geriausiai tinka jūsų įmonei. Apibrėžus pagrindinę sąskaitą sistema gali nustatyti naudojamą sąskaitos struktūrą. Perkeliant pagrindinę sąskaitą į viršų arba struktūros priekyje galima apriboti reikšmes ir padėti sistemai taikyti naujausią žinomą tinkamą reikšmę kaip numatytąją. Sąskaitos struktūroje gali būti iki 10 papildomų finansinių dimensijų. Sąskaitos struktūra apibrėžia, kurios dimensijos vertės galioja kartu su kitomis vertėmis. Ji taip pat apibrėžia, ar reikia įvesti dimensijų vertes.

### <a name="advanced-rules"></a>Išplėstinės taisyklės

Išplėstinės taisyklės yra pasirenkamasis komponentas nustatant sąskaitų planą. Į sąskaitos struktūrą galima įtraukti norimą skaičių išplėstinių taisyklių. Išplėstinės taisyklės dažnai naudojamos tvarkyti scenarijus, kur papildomos finansinės dimensijos turi būti stebimos, kai atitinkami konkretūs kriterijai. Pvz., jei naudojate kelionės išlaidų sąskaitą, galite sekti papildomą informaciją, pavyzdžiui, įvykį, į kurį keliauja darbuotojas. Jei yra kelios išplėstinės taisyklės, jos taikomos abėcėlės tvarka pagal taisyklių pavadinimus. Segmentus, kuriuos prideda taisyklė, galima taikyti tik po sąskaitos struktūros segmentų.

### <a name="balancing-dimension"></a>Balansavimo dimensija

Galima pasirinktinai nurodyti balansavimo finansinę dimensiją. Puslapyje **DK** galima nurodyti finansinę dimensiją, kuri turi būti subalansuota. Kai operacijos registruojamos toje finansinėje dimensijoje, sistema automatiškai sukuria ir užregistruoja įrašus, kad finansinė dimensija būtų subalansuota.

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>Numatytosios / pataisytos finansinės dimensijos pagrindinėje sąskaitoje

Numatytosios dimensijos gaunamos iš įvairių vietų, pagrindinius pvz., pagrindinių įrašų (kliento ar tiekėjo įrašų), dokumentų antraščių ir pagrindinės sąskaitos. Šioje temoje dėmesys skiriamas numatytosioms dimensijoms pagrindinėje sąskaitoje pagal juridinį subjektą. Galima nurodyti, ar pagrindinė sąskaita turi **Nefiksuotą** ar **Fiksuotą** vertę kiekvienai finansinei dimensijai, naudojamai visose DK sąskaitos struktūrose. Jei finansinė dimensija yra **Nefiksuota**, ji naudoja numatytąją vertę, tačiau tos vertės negalima perrašyti. Tokia veiksena taikoma visoms numatytosioms vertėms sistemoje, net numatytosioms vertėms, gaunamoms iš pagrindinių įrašų. Jei finansinė dimensija yra **Fiksuotos** vertės, ta vertė taikoma visada, nepriklausomai nuo to, ar gauta iš kur nors kaip numatytoji vertė, ar ją įvedė vartotojas.

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>Tvarka, kuria dimensijos taikomos atliekant registravimą

Žmonėms dažnai kyla klausimų apie tvarką, kuria vykdomi įvairūs komponentai. Labai svarbu suprasti, kaip taikomos numatytosios dimensijos, nes ši veiksena daro įtaką nustatymo metodams.

> [!NOTE]
> Ši informacija taikoma tik numatytosios dimensijos taikymui programoje. Jei importuojate duomenis naudodami „Microsoft Excel“ arba „Data Management Framework“, veiksena skiriasi.

### <a name="example-1"></a>1 pavyzdys

**Sąskaitos struktūra**

| Korespondentinė sąskaita, subsąskaita            | Verslo struktūros vienetas           | Skyrius              | Išlaidų centras             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Leidžiamos visos vertės. | Leidžiamos visos vertės. | Leidžiamos visos vertės. | Leidžiamos visos vertės. |

**Korespondentinė sąskaita, subsąskaita**

| Korespondentinė sąskaita, subsąskaita | Vardas          | Juridinis subjektas | Skyrius                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | Produkto pardavimas | USMF         | Fiksuotos – 022 pardavimo ir rinkodaros skyrius |

Šioje iliustracijoje parodyta fiksuota numatytoji dimensija, kuri nustatyta pagrindinėje sąskaitoje 401100.

[![Numatytosios finansinės dimensijos](./media/default-dimensions.png)](./media/default-dimensions.png)

Šiame pavyzdyje įvesime bendrąjį žurnalą, kuriame padalinio dimensija nustatyta naudoti numatytąją vertę **023** (operacijos). Įvesime ir užregistruosime DK sąskaitą. Tolesnėje iliustracijoje parodyta numatytoji finansinė dimensija didžiosios knygos antraštėje.

[![Pagrindiniai žurnalai](./media/general-journal.png)](./media/general-journal.png)

Dėl numatytosios dimensijos žurnalo antraštėje padalinys 023 bus taikomas pagal numatytuosius nustatymus pardavimo sąskaitos eilutėje. Tolesnėje iliustracijoje pateikta bendrojo žurnalo eilutė, kurioje taikoma **023** numatytosios dimensijos vertė iš antraštės.

[![Žurnalo kvitas](./media/journal-voucher.png)](./media/journal-voucher.png)

Tačiau kai eilutė registruojama, taikoma fiksuotoji dimensija ir eilutė registruojama padalinyje 022. Tolesnėje iliustracijoje pateiktas užregistruotas kvitas, kuriame fiksuotoji dimensija taikoma pardavimo sąskaitai.

[![Kvitų operacijos](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>2 pavyzdys

Šiame pavyzdyje naudojama tokia pati sąranka, kaip pirmajame. Tačiau mes įtrauksime antrąjį komponentą ir naudosime padalino dimensiją kaip balansavimo dimensiją. Tolesnėje iliustracijoje **Padalinys** nustatytas kaip USMF DK balansavimo finansinė dimensija.

[![DK](./media/ledger.png)](./media/ledger.png)

Kai naudojama ta patiurnalo antraštės sąranka ir registruojama ta pati operacija, iš pradžių taikoma fiksuotoji dimensija. Tada taikoma balansavimo logika siekiant padėti užtikrinti, kad kiekvienas padalinys turi subalansuoti įrašą. Tolesnėje iliustracijoje pateiktos kvito operacijos, apimančios balansavimo įrašą pritaikius fiksuotą dimensiją.

[![Kvitų operacijos](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>3 pavyzdys

Šiame pavyzdyje įtrauksime išplėstinę taisyklę. Išplėstinė taisyklė nurodo, kad naudojant pardavimo sąskaitą 401100 ir padalinį 022 (pardavimas ir rinkodara), sistema turi sekti papildomą segmentą, kuris vadinamas Klientas.

Šis pavyzdys svarbus dėl pateiktos tvarkos. Sąskaitos struktūra nustatoma įvedus pagrindinę sąskaitą. Jei nurodote sąskaitos struktūros sąranką, sistema gali nustatyti, kad pagrindinė sąskaita, verslo struktūros vienetas ir išlaidų centras nėra aktualūs. Šiuo metu išplėstinė taisyklė nebuvo suaktyvinta, nes fiksuota dimensija žurnalo kvitui taikoma tik registravimo metu pritaikius numatytąsias dimensijas. Tolesnėje iliustracijoje nėra segmento Klientas, nes nebuvo įvykdyti išplėstinės taisyklės kriterijai.

[![DK sąskaita](./media/drop-down.png)](./media/drop-down.png)

Registravimas nebus sėkmingas, nes fiksuota dimensija buvo pritaikyta proceso pabaigoje. Dimensijos tikrinimas nustato, kad segmentas Klientas būtinas, jeigu pagrindinė sąskaita yra 401100, o padalinys 022. Registravimas negali būti vykdomas dėl tikrinimo klaidos. Tolesnėje iliustracijoje pateiktas pranešimas, rodomas po dimensijos tikrinimo nustačius, kad segmentas Klientas yra būtinas.

[![Pranešimo informacija](./media/message.png)](./media/message.png)

Šiame pavyzdyje būtina perrašyti numatytąją vertę, kad būtų suaktyvinama išplėstinė taisyklė ir būtų galima įvesti segmentą Klientas. Tačiau šis sprendimas ne visada pasiekiamas ir kai kurie vartotojai net nežino apie registravimo taisykles. Todėl svarbu suprasti numatytųjų dimensijų taikymo tvarką nustatant sąskaitų planą.

Norėdami pasiekti savo tikslų, šiame pavyzdyje galite keisti konfigūraciją keliais būdais. Galima sukurti naują sąskaitos struktūrą pardavimo sąskaitoms ir įtraukti į struktūrą segmentą Klientas. Galima įtraukti daugiau eilučių į esamą sąskaitos struktūrą ir nurodyti pagrindinės sąskaitos ir tinkamo padalinio vertes. Tada papildomoje kliento struktūroje galima naudoti atskirą pardavimo sąskaitų struktūrą, kurioje būtų naudojamas segmentas Klientas.

## <a name="additional-resources"></a>Papildomi ištekliai 

Kai kurie iš šių išteklių nurodo ankstesnę mūsų programinės įrangos versiją. Tačiau didžioji dalis informacijos apie numatytosios dimensijos taikymą ir daugelis koncepcijų yra tokios pačios ankstesnėje versijoje ir joms tinka pateiktos nuorodos.

[Subalansuoti žurnalai susijusių vienetų apskaitai](example-balanced-journals-interunit-accounting.md)

[Sąskaitų plano rengimas](plan-chart-of-accounts.md) 

[Sąskaitų plano sudarymas AX 2012 tinklaraštyje](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/) – šis saitas nukreipia į septynių dalių serijos 1 dalį.

[Dimensijų naudojimas apskaitos paskirstymuose](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2013/12/16/dimension-defaulting-in-accounting-distributions-part-1-introduction/)

[Dimensijų naudojimas dimensijų sistemoje](https://docs.microsoft.com/archive/blogs/ax_gfm_framework_team_blog/dimension-defaulting-part-1-financial-dimensions-discovery)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
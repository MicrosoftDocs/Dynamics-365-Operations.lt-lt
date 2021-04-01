---
title: Sukonfigūruoti sąskaitų struktūras
description: Šioje temoje pateikiama informacija apie sąskaitų struktūras ir finansines dimensijas.
author: aprilolson
manager: AnnBe
ms.date: 06/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9c7fd8fcad7de3ec8b4b23d5c5e6456ae3ef372
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212354"
---
# <a name="configure-account-structures"></a>Sukonfigūruoti sąskaitų struktūras

[!include[banner](../includes/banner.md)]

Kuriant taisyklių, kurias naudojant nustatoma tvarka ir reikšmės, kai įvedamas sąskaitos numeris, rinkinį, sąskaitų struktūrose naudojama pagrindinė sąskaita ir finansinės dimensijos. Sąskaitų struktūrų galite sukurti tiek, kiek reikia jūsų verslui. Sąskaitų struktūros priskiriamos įmonės didžiosios knygos sąrankai, kad jas būtų galima bendrinti.

Kuriant sąskaitos struktūrą didžiausias segmentų skaičius yra 11. Jei jums reikia dar daugiau segmentų, kruopščiai įvertinkite savo sąranką ir reikalavimus, nes tai turės įtakos vartotojo patirčiai. Apsvarstykite, ar segmento negalima išvesti iš ataskaitų scenarijaus naudojant hierarchiją, o ne vedant duomenis arba naudojant vartotojo nustatytą lauką. Pavyzdžiui, jei norite pranešti apie vietą, tačiau ją galite nustatyti pagal padalinį arba išlaidų centrą, jums nereikės kaip vietos nurodyti finansinės dimensijos. Jei įvertinę visgi nustatote, kad reikia daugiau kaip 11 segmentų, papildomų segmentų galite įtraukti naudodami išplėstines taisykles.

Sąskaitų struktūroms reikalinga pagrindinė sąskaita. Pagrindinė sąskaita struktūroje nebūtinai turi būti pirmas segmentas, tačiau pagal ją nustatoma, kokios sąskaitos struktūra naudojama vedant sąskaitos numerį. Dėl šios priežasties pagrindinės sąskaitos reikšmė gali būti nurodyta tik vienoje didžiosios knygos struktūroje, kad reikšmės nepersidengtų. Nustačius sąskaitos struktūrą, filtruojamas leidžiamų verčių sąrašas, siekiant nukreipti vartotoją taip, kad jis pasirinktų tik tinkamas dimensijų reikšmes ir taip sumažėtų galimybė sukurti neteisingą žurnalo įrašą.

> [!NOTE] 
> Jei biudžetą planuojate pagal finansinę dimensiją, ji turės būti sąskaitos struktūros dalimi. Dabar sudarant biudžetą išplėstinės taisyklės nenaudojamos.

## <a name="example"></a>Pavyzdys
Pateikdami šį geriausios praktikos pavyzdį, skirtą sąskaitos struktūrai nustatyti, laikysime, kad įmonė nori sekti savo balanso sąskaitas (100000..399999) sąskaitos ir verslo struktūros vieneto finansinės dimensijos lygiu. Įplaukų ir išlaidų sąskaitų atveju (400000..999999) galima sekti finansinių dimensijų verslo struktūros vienetą, skyrių ir išlaidų centrą. Atlikus pardavimą, taip pat galima sekti klientą. Naudojant šį scenarijų rekomenduojama turėti dvi sąskaitos struktūras, priskirtas įmonės DK – vieną balanso ir vieną pelno ir nuostolio sąskaitoms. Norint optimizuoti vartotojo patirtį ir tikrinimą, klientui reikia taikyti išplėstinę taisyklę, taikomą tik tada, kai naudojama pardavimo sąskaita.

**Balanso sąskaitos struktūra**

|Korespondentinė sąskaita, subsąskaita          | Verslo struktūros vienetas    |
|----------------------|-----------|
|100000..399999 | *;” “|

**Pelno ir nuostolio sąskaitos struktūra**

|Korespondentinė sąskaita, subsąskaita          | Verslo struktūros vienetas    |Skyrius          | Išlaidų centras    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | *;” “|*;” “|*;” “|*;” “|

**Išplėstinė taisyklė klientui įtraukti**

Kriterijai: klientą įtraukite tarp pagrindinės sąskaitos numerių 400000 ir 499999. Kriterijų laukas turi būti nurodytas.

|Klientas         |
|-----------------|
|* |

Supaprastintame pavyzdyje leidžiamos visos reikšmės ir tušti laukai, todėl naudojami simboliai * ir “ “.

## <a name="segments-and-allowed-values"></a>Segmentai ir leidžiamos reikšmės
Skyriuje **Segmentai** ir **Leidžiama verčių informacija** pateikiamas į vartotojo patirtį panašus tinklelis, skirtas taisyklėms, kurių bus laikomasi registravimo metu atliekant tikrinimą, įvesti. Galite rašyti tiesiai tinklelio langeliuose, importuoti tinklelį iš „Excel“ arba naudotis skyriumi **Leidžiama reikšmės informacija**, kuriame pateikta informacija padės jums atlikti šį procesą.

Skyriuje **Leidžiama reikšmės informacija** pateikta informacija padės jums sukurti kriterijus naudojant **operatorius**, pvz., „prasideda“, „yra tarp“, „apima“ ir daugelį kitų.

[![Leidžiamos reikšmės](./media/account.png)](./media/account.png) 

Leistinos vertės bus nustatytos į numatytąsias vertes žurnale arba apskaitos paskirstymo įrašo puslapyje, kai nėra kitų galimų verčių, kurias būtų galima pasirinkti pagal sąskaitos struktūros nustatymą.

Čia pateikiamas tipo **Pelno ir nuostolio sąskaitos struktūra** pavyzdys.

|Korespondentinė sąskaita, subsąskaita          | Verslo struktūros vienetas    |Skyrius          | Išlaidų centras    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | 002 | 022 | 014 |

Kai atidarote žurnalą ir pasirenkate sąskaitą pelno ir nuostolių intervale, pasirinkus 002 verslo vienetą, bus nustatytos numatytosios verčių 022 ir 014 reikšmės sąskaitos valdiklyje. Tai taip pat nutiks ir apskaitos paskirstymo puslapyje. 

## <a name="more-than-7-criteria-needed"></a>Būtina naudoti daugiau nei 7 kriterijus

Jei naudojate daugiau nei 7 būtinus kriterijus, juos toliau įtraukti galite kitoje eilutėje. Dirbdami skyriuje **Leidžiama reikšmės informacija** pastebėsite, kad kriterijus **+Įtraukti naują**, įvedus septintą kriterijų, taps nebeaktyvus. Toliau nurodyta keletas veiksnių, dėl kurių taip nutinka. 
 - Stulpelio plotis 
 - Duomenų saugojimo būdas 
 - Skyriaus **Leidžiama reikšmės informacija** našumo kontrolė
 - Naudojimas  
 
Norėdami tęsti papildomų kriterijų įtraukimą, spustelėkite **Dubliuoti segmente** ir **Leidžiamų reikšmių skyrius**. Tai atlikus kriterijai bus nukopijuoti į naują eilutę. Tada galite įvesti arba keisti skyriuje **Leidžiama reikšmės informacija** pateiktą informaciją.

## <a name="best-practices"></a>Geriausia praktika
Nustatydami sąskaitų struktūras, galite vadovautis keletu geriausios praktikos pavyzdžių. Tačiau jie tik rekomendaciniai, todėl rengiant diskusiją turite visapusiškai aptarti savo verslo, augimo ir priežiūros planą.

- Pagrindinę sąskaitą nustatykite kaip pirmą arba padėkite ją kuo įmanoma arčiau pagrindinės struktūros priekinės dalies, kad vartotojai kurdami sąskaitos įrašą gautų kuo įmanoma geresnę valdymo patirtį.

- Pakartotinai naudokite kuo įmanoma daugiau sąskaitų struktūrų, kad visus juridinius subjektus reikėtų kuo mažiau tikrinti.

- Apsvarstykite, ar juridinių subjektų variantams nereikėtų taikyti išplėstinių taisyklių, kad būtų galima pakartotinai naudoti sąskaitų struktūras.

- Apibrėždami leistinas reikšmes kuo įmanoma dažniau naudokite diapazonus ir pakaitos simbolius. Taip sistema ne tik leis augti ir atlikti pakeitimų be priežiūros, bet ir, esant šiai konfigūracijai, geriau veiks.

- Neprirašykite žvaigždutės ties kiekvienu segmentu sąskaitos struktūroje ir nepasikliaukite vien tik išplėstinėmis taisyklėmis. Tai gali būti sunkiai valdoma ir atliekant priežiūrą ištikti vartotojo klaida, dėl kurios sistemai gali nepavykti atlikti registravimo procedūros.

## <a name="account-structure-activation"></a>Sąskaitos struktūros aktyvinimas
Kai būsite patenkinti nauja sąskaitos struktūros sąranka arba pakeitimu, turėsite ją aktyvinti. Jei sąskaitos struktūra priskirta didžiajai knygai, aktyvinimo procesas gali būti ilgas, nes visos sistemoje neužregistruotos operacijos turės būti sinchronizuotos pagal naują struktūrą. Pakeitus sąskaitos struktūrą, užregistruotos operacijos nepaveikiamos.

Daugiau informacijos ieškokite temose [Savo sąskaitų plano rengimas](plan-chart-of-accounts.md), [Finansinės dimensijos](financial-dimensions.md) bei [Sąskaitų ir dimensijų kombinacijų (segmentuoto įrašo valdiklis) įvedimas](enter-account-dimension-combinations-segmented-entry-control.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
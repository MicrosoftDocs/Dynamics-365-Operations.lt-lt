---
title: Numeravimai
description: "Numeracija naudojama bendrųjų duomenų įrašų ir operacijų įrašų, kuriems reikia identifikatorių, nuskaitomiems unikaliems identifikatoriams sugeneruoti."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5f4ff7eb8ee9b87b9d90af4d215743596555fd73
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="number-sequences"></a>Numeravimai

[!INCLUDE [banner](../includes/banner.md)]

Numeracija naudojama bendrųjų duomenų įrašų ir operacijų įrašų, kuriems reikia identifikatorių, nuskaitomiems unikaliems identifikatoriams sugeneruoti. Pagrindinių duomenų įrašas arba operacijų įrašas, kuriam reikia identifikatoriaus, vadinamas *nuoroda*.

Kad galėtumėte kurti naujus įrašus kaip nuorodas, turite nustatyti numeraciją ir susieti ją su nuoroda. Rekomenduojame naudoti puslapius dalyje **Organizacijos administravimas**, kad nustatytumėte numeracijas. Jei reikalingi konkretaus modulio parametrai, galite naudoti parametrų puslapį modulyje, kad nurodytumėte numeracijas to modulio nuorodoms. Pvz., dalyje **Gautinos sumos** ir **Mokėtinos sumos** galite nustatyti numeracijos grupes, kad priskirtumėte konkrečias numeracijas konkretiems klientams arba tiekėjams. 

Kai nustatote numeraciją, turite nustatyti aprėptį, kur apibūdina, kokia organizacija naudoja numeraciją. Aprėptis gali būti **Bendrai naudojama**, **Įmonės**, **Juridinio subjekto** arba **Valdymo vieneto**. **Juridinio subjekto** ir **Įmonės** aprėptys gali būt sujungtos su **Ataskaitiniu kalendoriniu laikotarpiu**, kad būtų kuriamos dar konkretesnės numeracijos. 

Numeracijų formatus sudaro segmentai. Numeracijos, kurių aprėptis yra kita nei **Bendrai naudojama**, gali apimti segmentus, kurie atitinka aprėptį. Pvz., numeracijoje, kurios apimtis **Juridinio subjekto**, gali būti juridinio subjekto segmentas. Įtraukdami aprėpties segmentą į numeracijos formatą, galite nustatyti konkretaus įrašo aprėptį pagal jo numerį. 

Be segmentų, atitinkančių aprėptis, numeracijų formatai gali apimti **Pastoviuosius** ir **Raidinius-skaitinius segmentus**. **Pastovusis** segmentas apima raidžių, skaitmenų arba simbolių, kurie nesikeičia, rinkinį. **Raidinis-skaitinis** segmentas apima raidžių ir skaitmenų rinkinį, kuris didinamas kaskart panaudojus skaičių. Naudokite skaičiaus ženklą (\#) norėdami nurodyti didėjančius skaičius ir ampersandus (&) norėdami nurodyti didėjančias raides. Pvz., pagal formatą \#\#\#\#\#\_2017 sukuriamos sekos 00001\_2017, 00002\_2017 ir t.t.

<a name="number-sequence-examples"></a>Numeracijos pavyzdžiai
------------------------

Toliau pateiktuose pavyzdžiuose parodyta, kaip naudoti segmentus kuriant numeracijų formatus. Konkrečiai pavyzdžiai parodo aprėpties segmentų poveikį.

### <a name="expense-report-numbers"></a>Išlaidų ataskaitos numeriai

Tolesniame pavyzdyje išlaidų ataskaitos numeriai nustatyti juridiniam subjektui, kuris pavadintas **CS**. 

- **Sritis:** kelionės ir išlaidos 
- **Nuoroda:** išlaidų ataskaitos numeris. 
- **Aprėptis:** juridinis subjektas 
- **Juridinis subjektas:** CS

| Segmentai  | Segmento tipas | Vertė     |
|-----------|--------------|-----------|
| 1 segmentas | Juridinis subjektas | CS        |
| 2 segmentas | Pastovus     | -IŠLAIDOS- |
| 3 segmentas | Raidinis ir skaitinis | \#\#\#\#  |

**Suformatuoto numerio pavyzdys**: CS-EXPENSE-0039 

Galite nustatyti panašų numeracijos formatą kitiems juridiniams subjektams. Pvz., jei pakeisite tik juridinio subjekto, pavadinimu **RW**, segmento vertę, suformatuotas numeris bus RW-EXPENSE-0039. Taip pat galite pakeisti visą kitų juridinių subjektų numeracijų formatą. Pvz., galite praleisti juridinio subjekto aprėpties segmentą, kad sukurtumėte formatuotą numerį, pvz., Exp-0001.

### <a name="sales-order-numbers"></a>Pardavimo užsakymo numeriai

Tolesniame pavyzdyje pardavimo užsakymo numeriai nustatyti įmonės ID **CEU**. 

- **Sritis:** pardavimas 
- **Nuoroda:** pardavimo užsakymas 
- **Aprėptis:** įmonė 
- **Įmonė:** CEU

| Segmentai  | Segmento tipas | Vertė    |
|-----------|--------------|----------|
| 1 segmentas | Pastovus     | SO-      |
| 2 segmentas | Raidinis ir skaitinis | \#\#\#\# |

**Suformatuoto numerio pavyzdys**: SO-0029 

Nors aprėpties segmentas neįtrauktas į formatą, iš naujo pradedama kiekvieno įmonės ID numeracija. Jei naudojate tą patį formatą visiems įmonėms ID, tie patys numeriai naudojami kiekvienoje įmonėje. Pvz., pardavimo užsakymo numeris SO-0029 naudojamas kiekvienoje įmonėje. Taip pat galite pakeisti visą kitų įmonės ID numeracijų formatą.

### <a name="purchase-requisition-numbers"></a>Pirkimo paraiškos numeriai

Tolesniame pavyzdyje pirkimo paraiškos numeriai taikomi visoje organizacijoje. 

- **Sritis:** pirkimas 
- **Nuoroda:** pirkimo paraiška 
- **Aprėptis:** bendrai naudojama

| Segmentai  | Segmento tipas | Vertė    |
|-----------|--------------|----------|
| 1 segmentas | Pastovus     | Reik.      |
| 2 segmentas | Raidinis ir skaitinis | \#\#\#\# |

**Suformatuoto numerio pavyzdys**: Req0052 

Kadangi aprėptis yra **Bendrai naudojama**, numeracijos formatas naudojamas visoje organizacijoje. Negalite nustatyti kitokių numeracijų formatų skirtingoms organizacijos dalims. 

<a name="performance-considerations-for-number-sequences"></a>Numeracijų našumo aplinkybės
-----------------------------------------------

Apsvarstykite toliau nurodytą informaciją apie tai, kaip numeracijų konfigūracija gali paveikti sistemos našumą, prieš nustatydami numeracijas.

### <a name="continuous-and-non-continuous-number-sequences"></a>Tęstinės ir netęstinės numeracijos

Numeracijos gali būti tęstinės arba netęstinės. Tęstinėje numeracijoje nepraleidžiami jokie skaičiai, bet skaičiai gali būti naudojami ne paeiliui. Skaičiai iš netęstinės numeracijos naudojami paeiliui, bet numeracijoje gali būti praleisti skaičiai. Pvz., jei naudotojas atšaukia operaciją, numeris sugeneruojamas, bet nenaudojamas. Tęstinėje numeracijoje skaičiai pakartotinai panaudojami vėliau. Netęstinėje numeracijoje skaičius nenaudojamas. 

Tęstinės numeracijos paprastai reikalingos išoriniams dokumentams, pvz., pirkimo užsakymams, pardavimo užsakymams ir SF. Tačiau tęstinės numeracijos gali turėti neigiamos įtakos sistemos atsako laikui, nes sistema turi pareikalauti skaičiaus iš duomenų bazės kaskart, kai sukuriamas naujas dokumentas arba įrašas. 

Jei naudojate netęstinę numeraciją, **Numeracijų** puslapio **Našumo** „FastTab‟ galite įgalinti **Išankstinį paskirstymą**. Kai nurodote iš anksto priskiriamų numerių kiekį, sistema parenka tuos numerius ir saugo atmintyje. Naujų numerių prašoma iš duomenų bazės tik panaudojus iš anksto priskirtą kiekį. 

Rekomenduojame naudoti netęstines numeracijas, kad užtikrintumėte geresnį našumą, nebent taikomi reglamento reikalavimai.

### <a name="automatic-cleanup-of-number-sequences"></a>Automatinis numeracijų valymas

Nutrūkus maitinimui, įvykus klaidai arba kitai netikėtai trikčiai, sistema negali perskirstyti tęstinių numeracijų skaičių automatiškai. Galite vykdyti valymo procesą rankiniu būdu arba automatiškai atkurti prarastus numerius. 

Atidžiai apsvarstykite serverio naudojimą, kai planuojate valymo procesą. Rekomenduojame ne piko valandomis atlikti valymą kaip paketinę užduotį.







---
title: "Numeracijos apžvalga"
description: "Numeracijų Microsoft Dynamics 365 operacijoms naudojami generuoti duomenų įrašų ir sandorių įrašus, kurie reikalauja identifikatoriai, skaitymo, unikalus identifikatorius. Pagrindinių duomenų įrašas arba operacijų įrašas, kuriam reikia identifikatoriaus, vadinamas <em>nuoroda</em>."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a812c93a13fd36f44e659c9976099af62793098f
ms.lasthandoff: 03/31/2017


---

# <a name="number-sequence-overview"></a>Numeracijos apžvalga

Numeracijų Microsoft Dynamics 365 operacijoms naudojami generuoti duomenų įrašų ir sandorių įrašus, kurie reikalauja identifikatoriai, skaitymo, unikalus identifikatorius. Pagrindinių duomenų įrašas arba operacijų įrašas, kuriam reikia identifikatoriaus, vadinamas <em>nuoroda</em>.

Prieš kurdami naujus įrašus už nuoroda Microsoft Dynamics 365 operacijoms, turite nustatyti numeraciją ir susieti jį su nuoroda. Rekomenduojame naudoti puslapius dalyje **Organizacijos administravimas**, kad nustatytumėte numeracijas. Jei reikalingi konkretaus modulio parametrai, galite naudoti parametrų puslapį modulyje, kad nurodytumėte numeracijas to modulio nuorodoms. Pvz., dalyje **Gautinos sumos** ir **Mokėtinos sumos** galite nustatyti numeracijos grupes, kad priskirtumėte konkrečias numeracijas konkretiems klientams arba tiekėjams. Kai nustatote numeraciją, turite nustatyti aprėptį, kur apibūdina, kokia organizacija naudoja numeraciją. Aprėptis gali būti **Bendrai naudojama**, **Įmonės**, **Juridinio subjekto** arba **Valdymo vieneto**. **Juridinio subjekto** ir **Įmonės** aprėptys gali būt sujungtos su **Ataskaitiniu kalendoriniu laikotarpiu**, kad būtų kuriamos dar konkretesnės numeracijos. Numeracijų formatus sudaro segmentai. Numeracijos, kurių aprėptis yra kita nei **Bendrai naudojama**, gali apimti segmentus, kurie atitinka aprėptį. Pvz., numeracijoje, kurios apimtis **Juridinio subjekto**, gali būti juridinio subjekto segmentas. Įtraukdami aprėpties segmentą į numeracijos formatą, galite nustatyti konkretaus įrašo aprėptį pagal jo numerį. Be segmentų, atitinkančių aprėptis, numeracijų formatai gali apimti **Pastoviuosius** ir **Raidinius-skaitinius segmentus**. **Pastovusis** segmentas apima raidžių, skaitmenų arba simbolių, kurie nesikeičia, rinkinį. **Raidinis-skaitinis** segmentas apima raidžių ir skaitmenų rinkinį, kuris didinamas kaskart panaudojus skaičių. Naudoti numerio ženklas (\#) atstovauti rodmens numerius ir ampersendą (&) atstovauti rodmens raides. Pvz., pateikiant \#\#\#\#\#\_2017 m. sukuria seka 00001\_2017 m. 00002\_2017 m., ir taip toliau.
Numeracijos pavyzdžiai
------------------------

Toliau pateiktuose pavyzdžiuose parodyta, kaip naudoti segmentus kuriant numeracijų formatus. Konkrečiai pavyzdžiai parodo aprėpties segmentų poveikį.
### <a name="expense-report-numbers"></a>Išlaidų ataskaitos numeriai

Tolesniame pavyzdyje išlaidų ataskaitos numeriai nustatyti juridiniam subjektui, kuris pavadintas **CS**. **Sritis: **Kelionės ir išlaidos** Nuoroda: **Išlaidų ataskaitos numeris** Aprėptis: **Juridinis subjektas** Juridinis subjektas:** CS
| Segmentai  | Segmento tipas | Vertė     |
|-----------|--------------|-----------|
| 1 segmentas | Juridinis subjektas | CS        |
| 2 segmentas | Pastovus     | -IŠLAIDOS- |
| 3 segmentas | Raidinis ir skaitinis | \#\#\#\#  |

**Suformatuoto numerio pavyzdys**: CS-EXPENSE-0039 Panašų numeracijos formatą galite nustatyti kitiems juridiniams subjektams. Pvz., jei pakeisite tik juridinio subjekto, pavadinimu **RW**, segmento vertę, suformatuotas numeris bus RW-EXPENSE-0039. Taip pat galite pakeisti visą kitų juridinių subjektų numeracijų formatą. Pvz., galite praleisti juridinio subjekto aprėpties segmentą, kad sukurtumėte formatuotą numerį, pvz., Exp-0001.

### <a name="sales-order-numbers"></a>Pardavimo užsakymo numeriai

Tolesniame pavyzdyje pardavimo užsakymo numeriai nustatyti įmonės ID **CEU**. **Sritis: **Pardavimas** Nuoroda: **Pardavimo užsakymas** Aprėptis: **Įmonė** Įmonė: **CEU
| Segmentai  | Segmento tipas | Vertė    |
|-----------|--------------|----------|
| 1 segmentas | Pastovus     | SO-      |
| 2 segmentas | Raidinis ir skaitinis | \#\#\#\# |

**Suformatuoto numerio pavyzdys**: SO-0029 Nors aprėpties segmentas neįtrauktas į formatą, iš naujo pradedama kiekvieno įmonės ID numeracija. Jei naudojate tą patį formatą visiems įmonėms ID, tie patys numeriai naudojami kiekvienoje įmonėje. Pvz., pardavimo užsakymo numeris SO-0029 naudojamas kiekvienoje įmonėje. Taip pat galite pakeisti visą kitų įmonės ID numeracijų formatą.

### <a name="purchase-requisition-numbers"></a>Pirkimo paraiškos numeriai

Tolesniame pavyzdyje pirkimo paraiškos numeriai taikomi visoje organizacijoje. **Sritis: **Pirkimas** Nuoroda: **Pirkimo paraiška** Aprėptis: **Bendrai naudojama
| Segmentai  | Segmento tipas | Vertė    |
|-----------|--------------|----------|
| 1 segmentas | Pastovus     | Reik.      |
| 2 segmentas | Raidinis ir skaitinis | \#\#\#\# |

**Suformatuoto numerio pavyzdys**: Req0052 Kadangi aprėptis yra **Bendrai naudojama**, numeracijos formatas yra naudojamas visoje organizacijoje. Negalite nustatyti kitokių numeracijų formatų skirtingoms organizacijos dalims. Numeracijų našumo aplinkybės
-----------------------------------------------

Apsvarstykite toliau nurodytą informaciją apie tai, kaip numeracijų konfigūracija gali paveikti sistemos našumą, prieš nustatydami numeracijas.
### <a name="continuous-and-non-continuous-number-sequences"></a>Tęstinės ir netęstinės numeracijos

Numeracijos gali būti tęstinės arba netęstinės. Tęstinėje numeracijoje nepraleidžiami jokie skaičiai, bet skaičiai gali būti naudojami ne paeiliui. Skaičiai iš netęstinės numeracijos naudojami paeiliui, bet numeracijoje gali būti praleisti skaičiai. Pvz., jei naudotojas atšaukia operaciją, numeris sugeneruojamas, bet nenaudojamas. Tęstinėje numeracijoje skaičiai pakartotinai panaudojami vėliau. Netęstinėje numeracijoje skaičius nenaudojamas. Tęstinės numeracijos paprastai reikalingos išoriniams dokumentams, pvz., pirkimo užsakymams, pardavimo užsakymams ir SF. Tačiau tęstinės numeracijos gali turėti neigiamos įtakos sistemos atsako laikui, nes sistema turi pareikalauti skaičiaus iš duomenų bazės kaskart, kai sukuriamas naujas dokumentas arba įrašas. Jei naudojate netęstinę numeraciją, **Numeracijų** puslapio **Našumo** „FastTab‟ galite įgalinti **Išankstinį paskirstymą**. Kai nurodote iš anksto priskiriamų numerių kiekį, sistema parenka tuos numerius ir saugo atmintyje. Naujų numerių prašoma iš duomenų bazės tik panaudojus iš anksto priskirtą kiekį. Rekomenduojame naudoti netęstines numeracijas, kad užtikrintumėte geresnį našumą, nebent taikomi reglamento reikalavimai.

### <a name="automatic-cleanup-of-number-sequences"></a>Automatinis numeracijų valymas

Nutrūkus maitinimui, įvykus klaidai arba kitai netikėtai trikčiai, sistema negali perskirstyti tęstinių numeracijų skaičių automatiškai. Galite vykdyti valymo procesą rankiniu būdu arba automatiškai atkurti prarastus numerius. Atidžiai apsvarstykite serverio naudojimą, kai planuojate valymo procesą. Rekomenduojame ne piko valandomis atlikti valymą kaip paketinę užduotį.





---
title: "Organizacijos ir organizacinės hierarchijos (komercijos pagrindai)"
description: "Prekybos pagrindai yra trijų tipų vidaus organizacijų, kurias galima apibrėžti padės organizacijai vykdyti verslo procesą ir pasiekti tikslą."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21251
ms.assetid: 2bfc6bfe-784b-42e8-8bf0-116e9f0a558e
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 93711977ad8d861ca75ba80ee542ee112c8ddd2f
ms.lasthandoff: 03/31/2017


---

# <a name="organizations-and-organizational-hierarchies-commerce-essentials"></a>Organizacijos ir organizacinės hierarchijos (komercijos pagrindai)

Prekybos pagrindai yra trijų tipų vidaus organizacijų, kurias galima apibrėžti padės organizacijai vykdyti verslo procesą ir pasiekti tikslą. 

Organizacija yra grupė žmonių, kurie dirba kartu vykdydami verslo procesą arba siekdami tikslo. Organizacijos hierarchija nurodo ryšius tarp verslo struktūros vienetų, kurie sudaro jūsų organizaciją.

## <a name="organizations"></a>Organizacijos
Naudojant „Commerce Essentials“ galima nurodyti trijų tipų vidines organizacijas: juridinius subjektus, valdymo vienetus ir komandas. Programoje „Microsoft Dynamics AX“ visos vidinės organizacijos yra objekto Šalis tipo. Todėl šios organizacijos naudoja adresų knygelę, kurioje saugomi adresai ir kita kontaktinė informacija. Šalis gali būti asmuo arba organizacija, ir ji gali priklausyti vienai ar daugiau adresų knygelių.
### <a name="legal-entities"></a>Juridiniai subjektai

Juridinis subjektas yra organizacija, turinti registruotą ar įteisintą teisinę struktūrą. Juridiniai subjektai gali sudaryti teisines sutartis ir privalo paruošti išrašus apie savo veiklą. Įmonė yra „Microsoft Dynamics AX“ juridinio subjekto tipas, ir kiekvienas juridinis subjektas yra susietas su įmonės ID. Šis susiejimas taikomas todėl, kad kai kuriose duomenų modelių funkcinėse programos srityse naudojamas įmonės ID arba DataAreaId. Dėl duomenų saugumo, šiose funkcinėse srityse naudojimas ribojamas įmonės viduje. Vartotojai gali gauti prieigą tik prie tos įmonės duomenų, prie kurios yra prisiregistravę.

### <a name="operating-units"></a>Valdymo vienetai

Valdymo vienetas yra organizacija, kuri yra naudojama ekonominiams ištekliams valdyti ir verslo veiklos procesams skirstyti. Valdymo vienete žmonės turi maksimaliai išnaudoti negausius išteklius, pagerinti procesus ir atsiskaityti už savo našumą. „Commerce Essentials“ valdymo vienetų tipai apima išlaidų centrus, verslo struktūros vienetus, vertės srautus, padalinius ir mažmeninės prekybos kanalus. Tolesnėje lentelėje pateikta daugiau informacijos apie kiekvieną valdymo vieneto tipą.
|                         |                                                                                         |                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Valdymo vienetų tipai** | **Aprašymas**                                                                         | **Paskirtis**                                                                                                                                 |
| Verslo struktūros vienetas           | Pusiau savarankiškas valdymo vienetas, sukurtas strateginiams verslo tikslams pasiekti. | Naudokite verslo struktūros vienetus finansinėms ataskaitoms, pagrįstoms pramonės šakomis ar produkto eilutėmis, kurias organizacija prižiūri keliuose juridiniuose subjektuose. |
| Mažmeninės prekybos kanalas          | Valdymo vienetas, nurodantis plytų ir skiedinio parduotuvę.                             | Naudokite norėdami tvarkyti ir valdyti vieną arba daugiau parduotuvių viename ar keliuose juridiniuose subjektuose.                                                               |

## <a name="organizational-hierarchies"></a>Organizacijų hierarchijos
Naudojant „Commerce Essentials“ kiekvienai hierarchijai priskiriama paskirtis. Hierarchijos paskirtis apibrėžia organizacijų, kurias galima įtraukti į hierarchiją, tipus. Paskirtis taip pat apibrėžia taikymo scenarijus, kuriuose hierarchija gali būti naudojama. Pvz., mažmeninės prekybos hierarchiją galima pirkti ir parduoti produktus per mažmeninės prekybos parduotuvėje. Organizacijos hierarchijoje galite bendrai naudoti parametrus, strategijas ir operacijas. Organizacija gali perimti arba nepaisyti jos pirminės organizacijos parametrų. Tačiau bendrai naudojami bendrieji duomenys, pvz., produktai ir adresų knygelės, taikomi visai organizacijai ir jų negalima nepaisyti atskiroms organizacijoms.
### <a name="best-practices-for-setting-up-an-organization-in-a-hierarchy"></a>Geriausia organizacijos nustatymo hierarchijoje praktika

Įgyvendindami organizacijos hierarchiją, atsižvelkite į šiuos geriausios praktikos pavyzdžius:
-   Norėdami nurodyti juridinio subjekto ir verslo struktūros vieneto sankirtą, sukurkite skyrių. Tada galite pridėti duomenis iš skyriaus prie juridinio subjekto privalomosioms ataskaitoms ir iš skyriaus prie verslo struktūros vieneto vidinėms ataskaitoms.
-   Viename juridiniame subjekte nenustatykite kelių hierarchijų tam pačiam hierarchijos tikslui.
-   Nekurkite hierarchijos kiekvienam tikslui. Paprastai vieną hierarchiją galite naudoti keliems tikslams. Pavyzdžiui, vieną valdymo vienetų hierarchiją galima priskirti visiems su strategija susijusiems tikslams.
-   Kurkite subalansuotas hierarchijas. Hierarchijoje visi mazgai, esantys tokiu pačiu atstumu nuo šakninio mazgo, apibrėžiami kaip lygis. Subalansuotoje hierarchijoje kiekviename lygyje gali būti tik vieno tipo valdymo vienetas, o atstumas nuo šakninio mazgo iki kiekvieno lygio yra nuoseklus. Jei tarp skyriaus ir juridinio subjekto arba verslo struktūros vieneto yra tarpinių lygių, norint sukurti subalansuotą hierarchiją gali reikėti organizacijų-rezervavimo ženklų.
-   Nenustatykite atskiros valdymo vienetų hierarchijos, jei juridinių subjektų struktūra yra ir jūsų valdymo struktūra. Mišri juridinių subjektų ir valdymo vienetų hierarchija gali tarnauti abiem tikslams.
-   Prieš nustatydami pagrindinius pertvarkymo scenarijus, poveikio analizei ir tikrinimo bandymui atlikti naudokite hierarchijos įsigaliojimo datas.
-   Įrašykite hierarchiją kaip juodraštį, jei prieš publikuodami hierarchiją gali keisti.
-   Ribokite skaičių žmonių, turinčių teisę įtraukti organizacijos į hierarchiją arba šalinti iš jos gamybos aplinkoje. Mažesnis skaičius sumažina brangių klaidų ir reikalingų taisymų pavojų.

## <a name="retail-store-management"></a>Mažmeninės prekybos parduotuvės valdymas
Toliau pateiktoje lentelėje aprašomi „Commerce Essentials“ scenarijai, kuriuose galima naudoti organizacijos hierarchijas.
| Užduotis                                                                           | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                                | Hierarchijos paskirtis    |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Mažmeninės prekybos asortimentų tvarkymas                                                      | Identifikuokite produktus, kurie pasiekiami kiekvienoje parduotuvėje.                                                                                                                                                                                                                                             | Mažmeninės prekybos asortimentas    |
| Mažmeninės prekybos papildymo tvarkymas                                                    | Grupuokite parduotuves norėdami papildyti atsargas pagal papildymo taisykles.                                                                                                                                                                                                                                          | Mažmeninės prekybos papildymas |
| Parduotuvių duomenų pranešimas                                                         | Grupuokite parduotuves norėdami paruošti ataskaitas.                                                                                                                                                                                                                                                                                | Mažmeninės prekybos ataskaitos     |
| Parduotuvių grupės atsargų registravimas, išrašų skaičiavimas arba jų registravimas | Sukurkite parduotuvių grupę, kurią galima priskirti paketinei užduočiai. Kai apibrėžiate paketinę užduotį norėdami užregistruoti atsargas, apskaičiuoti arba registruoti išrašus, galite nustatyti, kuriai hierarchijai užduotis yra taikoma. Kai parduotuvės įtraukiamos į hierarchiją arba pašalinamos, paketinės užduoties modifikuoti nereikia. | Retail POS registravimas   |





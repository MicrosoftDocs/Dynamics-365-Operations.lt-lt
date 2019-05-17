---
title: Mažmeninės prekybos operacijų vientisumo tikrintuvas
description: Šioje temoje aprašomos mažmeninės prekybos operacijų vientisumo tikrintuvo funkcijos „Microsoft Dynamics 365 for Retail“.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 972c4d6b244eebc85cc801353ce8fb25ecbc0655
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517126"
---
# <a name="retail-transaction-consistency-checker"></a>Mažmeninės prekybos operacijų vientisumo tikrintuvas


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Šioje temoje aprašomos mažmeninės prekybos operacijų vientisumo tikrintuvo funkcijos, veikiančios „Microsoft Dynamics 365 for Finance and Operations“ 8.1.3 versijoje. Vientisumo tikrintuvas identifikuoja ir atskiria nesuderinamas operacijas prieš jas paimant į išrašų registravimo procesą.

Išrašą registruojant „Retail“, užregistruoti gali nepavykti dėl mažmeninės prekybos operacijų lentelėse esančių nesuderinamų duomenų. Duomenų problema galėjo įvykti dėl nenumatytų problemų elektroninio kasos aparato (EKA) programoje arba dėl netinkamo operacijų importavimo iš trečiųjų šalių EKA sistemų. Šio nesuderinamumo atvejų pavyzdžiai: 

  - Operacijų suma, nurodyta antraštės lentelėje, nesutampa su eilučių operacijų suma.
  - Eilučių skaičius, nurodytas antraštės lentelėje, nesutampa su operacijų lentelės eilučių skaičiumi.
  - Mokesčiai, nurodyti antraštės lentelėje, nesutampa su mokesčių suma eilutėse. 
  
Kai nesuderinamos operacijos paimamos į išrašo registravimo procesą, sukuriamos nesuderinamos pardavimo SF ir mokėjimo žurnalai, todėl nepavyksta visas išrašų registravimo procesas. Norint atkurti išrašus iš tokios būsenos reikia pataisyti nemažai duomenų įvairiose operacijų lentelėse. Mažmeninės prekybos operacijų vientisumo tikrintuvas apsaugo nuo tokių problemų.

Šioje diagramoje parodytas registravimo procesas naudojant operacijų vientisumo tikrintuvą.

![Išrašų registravimo procesas naudojant mažmeninės prekybos operacijų vientisumo tikrintuvą](./media/validchecker.png "Išrašų registravimo procesas naudojant mažmeninės prekybos operacijų vientisumo tikrintuvą")

Paketinis vykdymas **Tikrinti parduotuvės operacijas** tikrina mažmeninės prekybos operacijų lentelių vientisumą tolesniais aspektais.

- Kliento kodas – tikrinama, ar kliento kodas, nurodytas mažmeninės prekybos operacijų lentelėse, yra HQ kliento bendruosiuose duomenyse.
- Eilučių skaičius – tikrinama, ar eilučių skaičius, nurodytas operacijos antraštės lentelėje, sutampa su pardavimo operacijų lentelių eilučių skaičiumi.

## <a name="set-up-the-consistency-checker"></a>Vientisumo tikrintuvo nustatymas
Sukonfigūruokite, kad paketinis vykdymas Tikrinti parduotuvės operacijas būtų paleidžiamas periodiškai, įėję į **Mažmeninė prekyba \> Mažmeninės prekybos IT \> EKA registravimas**. Paketinė užduotis gali būtu suplanuota pagal parduotuvės organizacijos hierarchiją, panašiai kaip nustatyti procesai Skaičiuoti išrašus pakete ir Registruoti išrašus pakete. Rekomenduojame sukonfigūruoti šį paketinį vykdymą, kad jis būtų paleistas keletą kartų per dieną, ir suplanuoti taip, kad jis būtų vykdomas kiekvienos P užduoties pabaigoje.

## <a name="results-of-validation-process"></a>Tikrinimo proceso rezultatai
Paketinio vykdymo tikrinimo rezultatai yra pažymimi atitinkamoje mažmeninės prekybos operacijoje. Mažmeninės prekybos operacijos įrašo lauko **Tikrinimo būsena** reikšmė pateikiama arba **Sėkmingai**, arba **Klaida**, o lauke **Paskutinio tikrinimo laikas** rodoma paskutinio tikrinimo data.

Norėdami peržiūrėti išsamesnį klaidos tekstą tikrinimui nepavykus, pasirinkite atitinkamą mažmeninės prekybos parduotuvės operacijos įrašą ir spustelėkite mygtuką **Tikrinimo klaidos**.

Operacijos, kurias tikrinant rasta klaidų ir kurios dar nebuvo patikrintos, į išrašus įtrauktos nebus. Proceso Skaičiuoti išrašą metu vartotojams bus pranešta, jei bus operacijų, kurios galėjo būti įtrauktos į išrašą, tačiau nebuvo.

Radus tikrinimo klaidų, vienintelis būdas jas ištaisyti yra kreiptis į „Microsoft“ pagalbos tarnybą. Būsimame leidime bus įtraukta galimybė vartotojui pataisyti klaidingus įrašus vartotojo sąsajoje. Be to, pradės veikti registravimo ir audito funkcijos, kad būtų galima sekti pakeitimų retrospektyvą.

> [!NOTE]
> Į būsimas versijas bus įtraukta papildomų tikrinimo taisyklių, kurios palaikys daugiau scenarijų.

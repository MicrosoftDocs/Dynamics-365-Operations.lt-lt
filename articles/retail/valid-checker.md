---
title: Mažmeninės prekybos operacijų vientisumo tikrintuvas
description: Šioje temoje aprašomos mažmeninės prekybos operacijų vientisumo tikrintuvo funkcijos „Dynamics 365 Retail“.
author: josaw1
manager: AnnBe
ms.date: 05/30/2019
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
ms.openlocfilehash: 0413c2b236e442fb56098f1902b4d5b247ed4649
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018423"
---
# <a name="retail-transaction-consistency-checker"></a>Mažmeninės prekybos operacijų vientisumo tikrintuvas


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Šioje temoje aprašomos mažmeninės prekybos operacijų vientisumo tikrintuvo funkcijos. Vientisumo tikrintuvas identifikuoja ir atskiria nesuderinamas operacijas prieš jas paimant į išrašų registravimo procesą.

Išrašą registruojant „Retail“, užregistruoti gali nepavykti dėl mažmeninės prekybos operacijų lentelėse esančių nesuderinamų duomenų. Duomenų problema galėjo įvykti dėl nenumatytų problemų elektroninio kasos aparato (EKA) programoje arba dėl netinkamo operacijų importavimo iš trečiųjų šalių EKA sistemų. Šio nesuderinamumo atvejų pavyzdžiai: 

- Operacijų suma, nurodyta antraštės lentelėje, nesutampa su eilučių operacijų suma.
- Eilučių skaičius, nurodytas antraštės lentelėje, nesutampa su operacijų lentelės eilučių skaičiumi.
- Mokesčiai, nurodyti antraštės lentelėje, nesutampa su mokesčių suma eilutėse. 

Kai nesuderinamos operacijos paimamos į išrašo registravimo procesą, sukuriamos nesuderinamos pardavimo SF ir mokėjimo žurnalai, todėl nepavyksta visas išrašų registravimo procesas. Norint atkurti išrašus iš tokios būsenos reikia pataisyti nemažai duomenų įvairiose operacijų lentelėse. Mažmeninės prekybos operacijų vientisumo tikrintuvas apsaugo nuo tokių problemų.

Šioje diagramoje parodytas registravimo procesas naudojant operacijų vientisumo tikrintuvą.

![Išrašų registravimo procesas naudojant mažmeninės prekybos operacijų vientisumo tikrintuvą](./media/validchecker.png "Išrašų registravimo procesas naudojant mažmeninės prekybos operacijų vientisumo tikrintuvą")

Paketinis vykdymas **Tikrinti parduotuvės operacijas** tikrina mažmeninės prekybos operacijų lentelių vientisumą tolesniais aspektais.

- **Kliento kodas** – tikrinama, ar kliento kodas, nurodytas mažmeninės prekybos operacijų lentelėse, yra HQ kliento bendruosiuose duomenyse.
- **Eilučių skaičius** – tikrinama, ar eilučių skaičius, nurodytas operacijos antraštės lentelėje, sutampa su pardavimo operacijų lentelių eilučių skaičiumi.
- **Į kainą įtrauktas mokestis** – tikrinama, ar parametras **Į kainą įtrauktas mokestis** yra nuoseklus visose operacijos eilutėse.
- **Mokėjimo suma** – tikrinama, ar mokėjimo įrašai atitinka antraštėje nurodytą mokėjimo sumą.
- **Bendra suma** – tikrinama, ar antraštėje nurodyta bendra suma yra eilutėse nurodytų grynųjų sumų ir mokesčio sumos suma.
- **Grynoji suma** – tikrinama, ar antraštėje nurodyta grynoji suma yra eilutėse nurodytų grynųjų sumų suma.
- **Nepriemoka / permoka** – tikrinama, ar antraštėje nurodytos bendros sumos ir mokėjimo sumos skirtumas neviršija didžiausios nepriemokos / permokos konfigūracijos.
- **Nuolaidos suma** – tikrinama, ar nuolaidos suma nuolaidos lentelėse ir nuolaidos suma mažmeninės prekybos operacijų eilučių lentelėse yra nuoseklios, bei ar antraštėje nurodyta nuolaidos suma yra eilutėse nurodytų nuolaidos sumų suma.
- **Eilutės nuolaida** – tikrinama, ar operacijos eilutėje nurodyta eilutės nuolaida yra visų nuolaidų lentelėje, atitinkančioje operacijos eilutę, esančių eilučių suma.
- **Dovanų kortelės prekė** – „Retail“ dovanų kortelių prekių grąžinimo nepalaiko. Tačiau dovanų kortelės likutį galima išgryninti. Bet kokiai dovanų kortelės prekei, kuri yra apdorojama ne kaip išgryninimo eilutė, o kaip grąžinimo eilutė, išrašo registravimo proceso vykdyti nepavyksta. Dovanų kortelių prekių tikrinimo procesas padeda užtikrinti, kad mažmeninės prekybos operacijų lentelėse būtų tik tos grąžinamos dovanų kortelių eilučių prekės, kurios yra dovanų kortelių išgryninimo eilutės.
- **Neigiama kaina** – tikrinama, ar nėra neigiamos kainos operacijų eilučių.
- **Prekė ir variantas** – tikrinama, ar operacijų eilutėse nurodytos prekės ir variantai egzistuoja pagrindiniame prekių ir variantų faile.
- **Mokesčio suma** – tikrinama, ar mokesčių įrašai atitinka eilutėse nurodytas mokesčių sumas. 

## <a name="set-up-the-consistency-checker"></a>Vientisumo tikrintuvo nustatymas

Sukonfigūruokite, kad paketinis vykdymas Tikrinti parduotuvės operacijas būtų paleidžiamas periodiškai, įėję į **Mažmeninė prekyba \> Mažmeninės prekybos IT \> EKA registravimas**. Paketinė užduotis gali būtu suplanuota pagal parduotuvės organizacijos hierarchiją, panašiai kaip nustatyti procesai Skaičiuoti išrašus pakete ir Registruoti išrašus pakete. Rekomenduojame sukonfigūruoti šį paketinį vykdymą, kad jis būtų paleistas keletą kartų per dieną, ir suplanuoti taip, kad jis būtų vykdomas kiekvienos P užduoties pabaigoje.

## <a name="results-of-validation-process"></a>Tikrinimo proceso rezultatai

Paketinio vykdymo tikrinimo rezultatai yra pažymimi atitinkamoje mažmeninės prekybos operacijoje. Mažmeninės prekybos operacijos įrašo lauko **Tikrinimo būsena** reikšmė pateikiama arba **Sėkmingai**, arba **Klaida**, o lauke **Paskutinio tikrinimo laikas** rodoma paskutinio tikrinimo data.

Norėdami peržiūrėti išsamesnį klaidos tekstą tikrinimui nepavykus, pasirinkite atitinkamą mažmeninės prekybos parduotuvės operacijos įrašą ir spustelėkite mygtuką **Tikrinimo klaidos**.

Operacijos, kurias tikrinant rasta klaidų ir kurios dar nebuvo patikrintos, į išrašus įtrauktos nebus. Proceso Skaičiuoti išrašą metu vartotojams bus pranešta, jei bus operacijų, kurios galėjo būti įtrauktos į išrašą, tačiau nebuvo.

Radus tikrinimo klaidų, vienintelis būdas jas ištaisyti yra kreiptis į „Microsoft“ pagalbos tarnybą. Būsimame leidime bus įtraukta galimybė vartotojui pataisyti klaidingus įrašus vartotojo sąsajoje. Be to, pradės veikti registravimo ir audito funkcijos, kad būtų galima sekti pakeitimų retrospektyvą.

> [!NOTE]
> Į būsimas versijas bus įtraukta papildomų tikrinimo taisyklių, kurios palaikys daugiau scenarijų.

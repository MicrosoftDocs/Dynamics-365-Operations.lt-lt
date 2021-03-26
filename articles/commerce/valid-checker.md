---
title: Mažmeninės prekybos operacijų vientisumo tikrintuvas
description: Šioje temoje aprašomos operacijų vientisumo tikrintuvo funkcijos „Dynamics 365 Commerce“.
author: josaw1
manager: AnnBe
ms.date: 10/07/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: cce0d408ac6d372fb726eff8fa4b0358ec200243
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211000"
---
# <a name="retail-transaction-consistency-checker"></a>Mažmeninės prekybos operacijų vientisumo tikrintuvas

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos operacijų vientisumo tikrintuvo funkcijos „Microsoft Dynamics 365 Commerce“. Vientisumo tikrintuvas identifikuoja ir atskiria nesuderinamas operacijas prieš jas paimant į išrašų registravimo procesą.

Registruojant įrašą, užregistruoti gali nepavykti dėl prekybos operacijų lentelėse esančių nesuderinamų duomenų. Duomenų problema galėjo įvykti dėl nenumatytų problemų elektroninio kasos aparato (EKA) programoje arba dėl netinkamo operacijų importavimo iš trečiųjų šalių EKA sistemų. Šio nesuderinamumo atvejų pavyzdžiai: 

- Operacijų suma, nurodyta antraštės lentelėje, nesutampa su eilučių operacijų suma.
- Eilučių skaičius, nurodytas antraštės lentelėje, nesutampa su operacijų lentelės eilučių skaičiumi.
- Mokesčiai, nurodyti antraštės lentelėje, nesutampa su mokesčių suma eilutėse. 

Kai nesuderinamos operacijos paimamos į išrašo registravimo procesą, sukuriamos nesuderinamos pardavimo SF ir mokėjimo žurnalai, todėl nepavyksta visas išrašų registravimo procesas. Norint atkurti išrašus iš tokios būsenos reikia pataisyti nemažai duomenų įvairiose operacijų lentelėse. Operacijų vientisumo tikrintuvas apsaugo nuo tokių problemų.

Šioje diagramoje parodytas registravimo procesas naudojant operacijų vientisumo tikrintuvą.

![Išrašo registravimo procesas naudojant operacijų vientisumo tikrintuvą](./media/validchecker.png "Išrašo registravimo procesas naudojant mažmeninės prekybos operacijų vientisumo tikrintuvą")

Paketinis vykdymas **Tikrinti parduotuvės operacijas** tikrina prekybos operacijų lentelių vientisumą tolesniais aspektais.

- **Kliento kodas** – tikrinama, ar kliento kodas, nurodytas operacijų lentelėse, yra HQ kliento bendruosiuose duomenyse.
- **Eilučių skaičius** – tikrinama, ar eilučių skaičius, nurodytas operacijos antraštės lentelėje, sutampa su pardavimo operacijų lentelių eilučių skaičiumi.
- **Į kainą įtrauktas mokestis** – tikrinama, ar parametras **Į kainą įtrauktas mokestis** yra nuoseklus visose operacijos eilutėse ir pardavimo eilutėje nurodyta kaina atitinka į kainą įtraukto mokesčio ir neapmokestinimo konfigūraciją.
- **Mokėjimo suma** – tikrinama, ar mokėjimo įrašai atitinka antraštėje nurodytą mokėjimo sumą, ir taip pat konfigūracijoje skaidoma daugikliais, kad didžiojoje knygoje būtų apvalinama centais.
- **Bendra suma** – tikrinama, ar antraštėje nurodyta bendra suma yra eilutėse nurodytų grynųjų sumų ir mokesčio sumos suma, ir taip pat konfigūracijoje skaidoma daugikliais, kad didžiojoje knygoje būtų apvalinama centais.
- **Grynoji suma** – tikrinama, ar antraštėje nurodyta grynoji suma yra eilutėse nurodytų grynųjų sumų suma, ir taip pat konfigūracijoje skaidoma daugikliais, kad didžiojoje knygoje būtų apvalinama centais.
- **Nepriemoka / permoka** – tikrinama, ar antraštėje nurodytos bendros sumos ir mokėjimo sumos skirtumas neviršija didžiausios nepriemokos / permokos konfigūracijos, ir taip pat konfigūracijoje skaidoma daugikliais, kad didžiojoje knygoje būtų apvalinama centais.
- **Nuolaidos suma** – tikrinama, ar nuolaidos suma nuolaidos lentelėse ir nuolaidos suma operacijų eilučių lentelėse yra nuoseklios, bei ar antraštėje nurodyta nuolaidos suma yra eilutėse nurodytų nuolaidos sumų suma, ir taip pat konfigūracijoje skaidoma daugikliais, kad didžiojoje knygoje būtų apvalinama centais.
- **Eilutės nuolaida** – tikrinama, ar operacijos eilutėje nurodyta eilutės nuolaida yra visų nuolaidų lentelėje, atitinkančioje operacijos eilutę, esančių eilučių suma.
- **Dovanų kortelės prekė** – prekyba dovanų kortelių prekių grąžinimo nepalaiko. Tačiau dovanų kortelės likutį galima išgryninti. Bet kokiai dovanų kortelės prekei, kuri yra apdorojama ne kaip išgryninimo eilutė, o kaip grąžinimo eilutė, išrašo registravimo proceso vykdyti nepavyksta. Dovanų kortelių prekių tikrinimo procesas padeda užtikrinti, kad operacijų lentelėse būtų tik tos grąžinamos dovanų kortelių eilučių prekės, kurios yra dovanų kortelių išgryninimo eilutės.
- **Neigiama kaina** – tikrinama, ar nėra neigiamos kainos operacijų eilučių.
- **Prekė ir variantas** – tikrinama, ar operacijų eilutėse nurodytos prekės ir variantai egzistuoja pagrindiniame prekių ir variantų faile.
- **Mokesčio suma** – tikrinama, ar mokesčių įrašai atitinka eilutėse nurodytas mokesčių sumas.
- **Serijos numeris** – tikrina, ar serijos numerio kontroliuojamų prekių operacijų eilutėse yra serijos numeris.
- **Ženklas** – tikrina, ar kiekio ir grynosios sumos ženklas yra toks pat visose operacijų eilutėse.
- **Verslo data** – tikrinama, ar visų operacijų verslo datų finansiniai laikotarpiai yra atidaryti.
- **Mokesčiai** – tikrinama, ar antraštės ir eilutės mokesčių suma atitinka kainą, įskaitant mokesčio ir neapmokestinimo konfigūraciją.

## <a name="set-up-the-consistency-checker"></a>Vientisumo tikrintuvo nustatymas

Sukonfigūruokite, kad paketinis vykdymas Tikrinti parduotuvės operacijas būtų paleidžiamas periodiškai, įėję į **„Retail“ ir „Commerce“ \> „Retail“ ir „Commerce“ IT \> EKA registravimas**. Paketinė užduotis gali būtu suplanuota pagal parduotuvės organizacijos hierarchiją, panašiai kaip nustatyti procesai Skaičiuoti išrašus pakete ir Registruoti išrašus pakete. Rekomenduojame sukonfigūruoti šį paketinį vykdymą, kad jis būtų paleistas keletą kartų per dieną, ir suplanuoti taip, kad jis būtų vykdomas kiekvienos P užduoties pabaigoje.

## <a name="results-of-validation-process"></a>Tikrinimo proceso rezultatai

Paketinio vykdymo tikrinimo rezultatai yra pažymimi atitinkamoje operacijoje. Operacijos įrašo lauko **Tikrinimo būsena** reikšmė pateikiama arba **Sėkmingai**, arba **Klaida**, o lauke **Paskutinio tikrinimo laikas** rodoma paskutinio tikrinimo data.

Norėdami peržiūrėti išsamesnį klaidos tekstą tikrinimui nepavykus, pasirinkite atitinkamą parduotuvės operacijos įrašą ir spustelėkite mygtuką **Tikrinimo klaidos**.

Operacijos, kurias tikrinant rasta klaidų ir kurios dar nebuvo patikrintos, į išrašus įtrauktos nebus. Proceso Skaičiuoti išrašą metu vartotojams bus pranešta, jei bus operacijų, kurios galėjo būti įtrauktos į išrašą, tačiau nebuvo.

Radus tikrinimo klaidų, vienintelis būdas jas ištaisyti yra kreiptis į „Microsoft“ pagalbos tarnybą. Būsimame leidime bus įtraukta galimybė vartotojui pataisyti klaidingus įrašus vartotojo sąsajoje. Be to, pradės veikti registravimo ir audito funkcijos, kad būtų galima sekti pakeitimų retrospektyvą.

> [!NOTE]
> Į būsimas versijas bus įtraukta papildomų tikrinimo taisyklių, kurios palaikys daugiau scenarijų.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
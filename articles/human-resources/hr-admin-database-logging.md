---
title: Duomenų bazės registravimo konfigūravimas ir valdymas
description: Galite sekti lentelių ir laukų pakeitimus „Dynamics 365 Human Resources” naudodami duomenų bazės registravimą.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fd0f69df4a141e509c8c250f767cbbc3a20ef4ab7ac3dcec2bc6faa15eababb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781662"
---
# <a name="configure-and-manage-database-logging"></a>Duomenų bazės registravimo konfigūravimas ir valdymas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Galite sekti lentelių ir laukų pakeitimus „Dynamics 365 Human Resources” naudodami duomenų bazės registravimą. Šioje temoje aprašoma, kaip:

- Tvarkyti duomenų bazės registravimo saugą ir efektyvumą
- Nustatyti duomenų bazės registravimą
- Valyti duomenų bazės žurnalus

## <a name="overview-of-database-logging"></a>Duomenų bazės registravimo peržiūrą

Duomenų bazės registravimo funkcija stebi „Microsoft Dynamics 365 Human Resources” lentelių ir laukų pakeitimus. Šie pakeitimai apima įterpimo, atnaujinimo arba naikinimo veiksmus. Duomenų bazės registravimas išsaugo lentelių arba laukų, esančių duomenų bazės žurnalo lentelėje, keitimų įrašą.

Verslas duomenų bazės registravimą naudoja šiais tikslais:

- Kurti konkrečių lentelių, kuriose yra slaptos informacijos, keitimų audito įrašą.
- Sekti vienkartines operacijas. Duomenų bazės registravimas nėra skirtas automatinėms operacijoms, paleidžiamoms paketinėse užduotyse.

## <a name="security-for-database-logging"></a>Duomenų bazės registravimo sauga

Duomenų bazės žurnaluose gali būti slaptų duomenų. Riboti prieigą, kad būtų galima naudoti tik tuos saugos vaidmenis, kuriems reikalinga prieiga prie žurnalo duomenų.

## <a name="database-logging-and-performance"></a>Duomenų bazės registravimas ir našumas

Nors verslo perspektyva yra vertingas, duomenų bazės registravimas gali būti brangus išteklių naudojimo ir valdymo srityje. Duomenų bazės registravimą galima naudoti šiais tikslais:

- Duomenų bazės žurnalo lentelė gali greitai plėstis ir padidinti duomenų bazės dydį. Augimas priklauso nuo užregistruotų duomenų kiekio, kurį nusprendėte saugoti. Pagal numatytuosius nustatymus, duomenų bazės žurnalo lentelėje palaikomi tik 30 dienų žurnalo duomenys. 

- Duomenų bazės registravimas gali neigiamai paveikti ilgai trunkančius automatinius procesus, pvz., ilgai trunkančius duomenų importavimus.

### <a name="best-practices"></a>Geriausia praktika

Norėdami padidinti našumą, apribokite žurnalo įrašus pasirinkdami konkrečius laukus registruoti, o ne ištisas lenteles. Norint palaikyti bendrą našumą, duomenų bazės registravimas apribotas 20 lentelių.

> [!NOTE]
> Tik naujinimai gali būti registruojami atskiruose laukuose.

## <a name="set-up-database-logging"></a>Nustatyti duomenų bazės registravimą

Galite naudoti **Duomenų bazės pakeitimų registravimas** vedlį, kad nustatytumėte duomenų bazės registravimą. Vedlys suteikia lanksčią galimybę nustatyti lentelių arba laukų registravimą.

1. Eikite į **Sistemos administravimas > Saitai > Duomenų bazė > Duomenų bazės žurnalo nustatymas**. Pasirinkite **Nauja**, kad įjungtumėte **Registravimo duomenų bazės pakeitimai** vedlį.
2. Pasirinkite **Toliau**. 
3. Vedlio puslapyje Lentelės ir laukai pasirinkite lenteles ir laukus, kuriuose norite įgalinti duomenų **bazės** registravimą, ir pasirinkite **Pirmyn**.

   > [!Note]
   > Duomenų bazės registravimas negalimas visose Personalo duomenų bazės lentelėse. Pasirinkus Rodyti visas lenteles sąraše išplečiamas lentelių ir laukų sąrašas, kad būtų parodytos visos duomenų bazės lentelės, kuriose galimas duomenų bazės registravimas, bet tai bus viso duomenų bazių lentelių sąrašo **subrinkinyje**.

4. Vedlio pakeitimų tipų puslapyje pasirinkite duomenų operacijas, kurių kiekvienos lentelės ir laukų keitimus norite sekti, ir **pasirinkite** **Pirmyn**. Informacijos apie duomenų operacijas, kurias galima registruoti, ieškokite toliau esančioje lentelėje.
5. Puslapyje **Baigti** peržiūrėkite atliktus keitimus ir pasirinkite **Baigti**.

| Operacija | Aprašas |
| -- | -- |
| Sekti naujas operacijas | Kurti naujų lentelėje sukurtų įrašų žurnalą. |
| Atnaujinimas | Kurti lentelių įrašų naujinimų žurnalą arba atnaujinimų į atskirai pasirinktus lentelės laukus žurnalą. Jei pasirenkate registruoti lentelės atnaujinimus, žurnalo įrašas sukuriamas kiekvieną kartą, kai atnaujinamas bet kurio lentelės įrašo laukas. Jei pasirenkate registruoti tam tikrų laukų atnaujinimus, žurnalo įrašas sukuriamas tik tų lentelės įrašų laukų atnaujinimų metu. |
| Panaikinti | Kurti iš lentelės panaikintų įrašų žurnalą. |
| Pervadinti raktą | Pervardijus lentelės raktą, sukurti žurnalo įrašą. |


## <a name="clean-up-database-logs"></a>Valyti duomenų bazės žurnalus

Galite naikinti dalį arba visus duomenų bazės žurnalus naudodami šias parinktis:

- Pasirinkite konkrečios lentelės visus žurnalus.
- Pasirinkite konkrečius duomenų bazės žurnalo tipus.
- Pasirinkite datą ir laiką, kada buvo sukurtas žurnalas.

Norėdami nustatyti duomenų bazės žurnalo valymą, atlikite šiuos veiksmus: 

1. Eikite į **Sistemos administravimas > Saitai > Duomenų bazė > Duomenų bazės žurnalas**. Pasirinkite **Valyti žurnalą**.

2. Pasirinkite žurnalų, kuriuos reikia panaikinti, pasirinkimo būdą įvesdami vieną iš šių pasirinkčių:

   - Lentelės ID
   - Žurnalo tipas
   - Sukūrimo data ir laikas

3. Naudokite **Duomenų bazės žurnalo valymas** skirtuką, kad nustatytumėte, kada paleisti žurnalo valymo užduotį. Pagal numatytuosius nustatymus, duomenų bazės žurnalai prieinami 30 dienų.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

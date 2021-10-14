---
title: Gamybos registravimas
description: Šiame straipsnyje pateikiama informacija apie įvairių tipų registravimus gamybos procese.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee3eaf11f5d77861e7abd29bb428f67b57a3e0e3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565956"
---
# <a name="production-posting"></a>Gamybos registravimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie įvairių tipų registravimus gamybos procese.

Gamybos registravimo veiklos atliekamos užbaigus gamybos procesus, aprašytus toliau pateiktuose skyriuose.

## <a name="material-consumption"></a>Medžiagų suvartojimas
Vykdant gamybos procesą ir užregistravus gamybos išrinkimo dokumento žurnalą, medžiagos užregistruojamos suvartotomis. Vykdant medžiagų suvartojimo procesą generuojamos išdavimo operacijos, kurias atliekant atskaitomos turimos atsargos. Gamybos parametrų dalyje galite nurodyti, ar apdorojamų (nebaigtos gamybos \[WIP\]) žaliavų reikšmė turėtų būti užregistruojama didžiojoje knygoje. Tuomet apdorojamų (NG) žaliavų reikšmė užregistruojama paskirtoje išrinkimo dokumento sąskaitoje ir paskirtoje išrinkimo dokumento korespondentinėje sąskaitoje.

## <a name="time-consumption"></a>Laiko suvartojimas
Darbuotojų sugaištamas laikas gamybos užduotims atlikti įrašomas technologinės kortelės žurnale arba užduoties kortelės žurnale. Užregistravus šiuos žurnalus, naudojamiems (NG) ištekliams skirtoje sąskaitoje registruojama didžioji knyga. Ją užregistravus nurodoma laiko, skirto gamybos užsakymui atlikti, vertė. Gamybos užsakymą užregistravus baigtu, sudengiamos NG sąskaitos.

## <a name="reporting-finished-goods-and-error-quantities"></a>Paskelbimas apie pagamintų prekių ir klaidų kiekius
Gamybos užsakymą paskelbus baigtu, pagamintų prekių kiekis atnaujinamas atsargų valdymo modulyje naudojant paskelbtų baigtais žurnalą. Jei naudojate NG apskaitą, kurią galima nustatyti gamybos parametrų dalyje, sukuriamas DK žurnalas, skirtas NG sąskaitų vertėms sumažinti ir pagamintų prekių atsargoms padidinti. Žurnale naudojama nustatyta produkto standartinė savikaina.

## <a name="ending-the-production-order"></a>Gamybos užsakymo baigimas
Prieš užbaigiant gamybos užsakymą apskaičiuojamos faktinės pagaminto prekių kiekio išlaidos. Visos numatytosios medžiagų, darbo ir papildomos išlaidos yra anuliuojamos ir pakeičiamos faktinėmis išlaidomis. Bendrosios baigtos prekės išlaidos nurašomos nuo atsargų gavimo sąskaitos ir įrašomos į atsargų išdavimų sąskaitą. Jei atlikdami išlaidų apskaičiavimo veiksmą pažymėsite žymės langelį **Galutinė užduotis**, gamybos užsakymo būsena bus pakeista į **Baigta**. Ši būsena neleidžia registruoti jokių netyčinių papildomų išlaidų užbaigtam gamybos užsakymui. Galite nurodyti, kad pateikiant ataskaitą kaip baigtų paskelbtų klaidingų kiekių vertės būtų priskiriamos kaip baigtais paskelbtiems tinkamiems kiekiams. Be to, galite nurodyti, kad klaidų kiekio vertė būtų registruojama paskirtoje nurašymų sąskaitoje.

## <a name="controlling-the-level-of-ledger-posting"></a>DK registravimo lygio valdymas
Puslapyje **Gamybos kontrolės parametrai** naudodami lauką **DK registravimas** galite nustatyti DK registravimo lygį, kai vykdomi gamybos procesai. Galimos šios vertės:

-   **Prekė ir ištekliai** – naudokite DK sąskaitas, kurios nustatytos žaliavų ir pagamintų prekių grupėms. Laiko suvartojimo NG medžiagos paimamos iš maršruto operacijų išteklių arba išteklių grupės.
-   **Prekė ir kategorija** – naudokite DK sąskaitas, kurios nustatytos žaliavų ir pagamintų prekių grupėms. Laiko suvartojimo NG medžiagos paimamos iš su maršruto operacijomis susietų išlaidų kategorijų.
-   **Gamybos grupės** – naudokite DK sąskaitas, kurios nustatytos medžiagų ir laiko suvartojimo gamybos grupėms. Gamybos grupės susietos su išleistais produktais ir, sukūrus gamybos užsakymus, nukopijuojamos į juos. Tada apdorojus su gamybos užsakymu susietas gamybos grupes bus pradėta jas registruoti gamybos užsakymuose.

**Pastaba.** Jei naudojamas standartinis baigtos prekės išlaidų skaičiavimo metodas, tai atsispindi galutinėse operacijose. Jei faktinės išlaidos skiriasi nuo naudojant standartinį metodą apskaičiuotų išlaidų, skirtumas užregistruojamas sąskaitoje, kurioje nurodomas pelnas ar nuostolis.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
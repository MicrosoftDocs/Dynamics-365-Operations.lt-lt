---
title: "Mokėjimo būdai"
description: "Kiekvienos mokėjimo tipą, kad agentas priima turi būti sukonfigūruotas mažmeninės prekybos ir komercijos Microsoft Dynamics 365 operacijoms, kai sistema yra nustatyti. Šiame straipsnyje aprašyti mokėjimo tipai, kuriuos galite nustatyti, ir aprašytas jų nustatymo procesas."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: MargoC
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b887fc5d03ea8982515e92725ce98cc416e56f9e
ms.openlocfilehash: 011beec07bf1ab858892ab1c374f1acf3839e877
ms.lasthandoff: 03/31/2017


---

# <a name="payment-methods"></a>Mokėjimo būdai

Kiekvienos mokėjimo tipą, kad agentas priima turi būti sukonfigūruotas mažmeninės prekybos ir komercijos Microsoft Dynamics 365 operacijoms, kai sistema yra nustatyti. Šiame straipsnyje aprašyti mokėjimo tipai, kuriuos galite nustatyti, ir aprašytas jų nustatymo procesas.

Mažmenininkai gali priimti įvairių tipų mokėjimą mainais už produktus ir paslaugas, kurias jie parduoda. Nors dažniausia mokėjimo forma yra grynieji pinigai, pardavėjai taip pat gali priimti mokėjimą čekiais, kortelėmis, kvitais ir t. t.. Kiekvienos mokėjimo tipą, kad agentas priima turi būti sukonfigūruotas Dynamics 365 operacijų - kai sistemoje yra nustatytas mažmeninės prekybos. Toliau pateikiamame sąraše aprašomi kiekvienos mokėjimo tipą, kurie gali būti įsteigti Dynamics 365 operacijų - mažmeninės prekybos:

-   **Grynieji pinigai** – pinigai fizine valiutos forma, pavyzdžiui, banknotai ir monetos. Ši valiuta gali būti įmonės valiuta arba vietinė parduotuvės valiuta.
-   **Čekis** – perduodamas dokumentas, nurodantis konkrečios sumos konkrečia valiuta mokėjimą, kurį garantuoja konkretus bankas. Čekis paprastai galioja neribotą laiką arba šešis mėnesius nuo išdavimo datos, jei nenurodytas kitoks galiojimo laikotarpis. Šis laikotarpis priklauso nuo banko, garantuojančio mokėjimą pagal čekį. Yra įvairūs čekių tipai, pavyzdžiui, užsakymo čekiai, skaitiklio čekiai, pateikėjo čekiai ir sąskaitos gavėjo čekiai. Galite nustatyti čekius kaip kiekvienos parduotuvės mokėjimo būdą. Gali būti priimami čekiai valiuta, nurodyta įmonės lygiu arba parduotuvės lygiu. Mokėjimą čekiu parduotuvėje galėsite priimti tik nustatę čekius kaip mokėjimo būdą.
-   **Valiuta** – pagrindinė mokėjimo forma ne įmonės numatytąja valiuta. Monetos ir popieriniai pinigai yra valiutos formos. Mokėjimo valiuta būdas apima visas valiutas, naudojamas mažmeninėje prekyboje ir prekyboje. Šį mokėjimo būdą galėsite naudoti tik nustatę valiutas ir nurodę valiutų mažmeninės prekybos kurso informaciją.
-   **Kortelė** – visų rūšių kortelės, naudojamos mažmeninėje prekybos ir prekyboje, pavyzdžiui, debeto ir kredito kortelės. Naudinga nustatyti vieną mokėjimo kortele būdą organizacijos lygiu, apimantį bet kokias korteles. Tada parduotuvės lygiu nustatykite mokėjimo būdą, taikomą kiekvienai kortelei arba kortelių rinkiniui, kuris apdorojamas naudojant tuos pačius parametrus. Mokėjimą kortelėmis parduotuvėje galėsite priimti tik nustatę rinkoje esančias gamintojo korteles, pavyzdžiui, debeto ir kredito korteles.
-   **Kredito pažyma** – kredito pažymos, išduodamos arba panaudojamos naudojant elektroninį kasos aparatą. Kredito pažyma gali būti kredito arba grąžinimo kredito pažyma, išduota pagal pardavimo grąžinimo pardavimą. Jei kredito pažymos panaudojamos tik dalinai, programa išduoda naują kredito pažymą, kurioje nurodomas naujas balansas. Naujos kredito pažymos numeris yra naujas. Kredito pažymą galima naudoti tik kartą, ir sistema išsaugo įrašą apie visas panaudotas sumas. Įrašą galima peržiūrėti puslapyje **Kredito pažymos lentelė**. Klientas negali panaudoti didesnės nei kredito pažymos vertė sumos.
-   **Dovanų kortelė** – dovanų kortelės, išduodamos ir panaudojamos naudojant elektroninį kasos aparatą. Dovanų kortelėms permokėjimai neleidžiami.
-   **Kliento sąskaita** – mokėjimai, kuriuos parduodant galima išskaityti iš kasos aparato į kliento sąskaitą. Šio mokėjimo būdą taip pat galite naudoti pardavimo informacijai ar konkretaus kliento nuolaidoms rinkti, kai klientas atlieka mokėjimą naudodamas kitą mokėjimo būdą. Tokiu atveju turite nustatyti konkretaus kliento informaciją.
-   **Lojalumo taškai** – pažymi, kad klientai sukaupti lojalumo programas. Jei norite sukurti lojalumo programas, Klientai gali pelnyti taškų ir panaudoti juos įvairiais būdais. Pavyzdžiui, pagal kai kurias lojalumo programas, klientai gali panaudoti lojalumo taškus nuolaidos forma arba net naudoti juos kaip mokėjimo formą.

Norėdami nustatyti mažmeninės prekybos ir prekybos mokėjimo būdus, turite atlikti tokias užduotis.

1.  Nustatykite organizacijos mokėjimo būdus. Sukurkite mokėjimo būdus, priimamus visos organizacijos.
2.  Sukurti visos organizacijos kortelių tipai ir kortelių numerius. Jei kredito kortelės arba debeto kortelės yra priimamos, galite sukurti vieną mokėjimo būdą korteles, ir tada sukurti visos organizacijos kortelių tipai ir kortelių numerius.
3.  Nustatyti parduotuvės mokėjimo metodą. Mokėjimo būdų susieti su kiekviena parduotuve ir įveskite kiekvienam mokėjimo metodui būdingus parametrus.
4.  Nustatykite kortelės mokėjimo būdus ir parduotuvėse. Bet kortelės mokėjimo metodus, parduotuvės priima, pilnas kortelės nustatymu.




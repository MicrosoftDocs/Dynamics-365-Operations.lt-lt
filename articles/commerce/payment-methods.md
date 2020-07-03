---
title: Mokėjimo būdai
description: Nustačius sistemą, reikia sukonfigūruoti kiekvieną pardavėjo priimamą mokėjimo tipą. Šiame straipsnyje aprašyti mokėjimo tipai, kuriuos galite nustatyti, ir aprašytas jų nustatymo procesas.
author: sericks007
manager: AnnBe
ms.date: 06/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 710c2f3bbe5b76af6d0bc0bf9a469e52c98c18d2
ms.sourcegitcommit: 550006e6376815237c21b5b30e928353f62fd97c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2020
ms.locfileid: "3463165"
---
# <a name="payment-methods"></a>Mokėjimo būdai

[!include [banner](includes/banner.md)]

Nustačius sistemą, reikia sukonfigūruoti kiekvieną pardavėjo priimamą mokėjimo tipą. Šiame straipsnyje aprašyti mokėjimo tipai, kuriuos galite nustatyti, ir aprašytas jų nustatymo procesas.

Mažmenininkai gali priimti įvairių tipų mokėjimą mainais už produktus ir paslaugas, kurias jie parduoda. Nors dažniausia mokėjimo forma yra grynieji pinigai, pardavėjai taip pat gali priimti mokėjimą čekiais, kortelėmis, kvitais ir t. t.. Nustačius sistemą, „Dynamics 365 Commerce“ reikia sukonfigūruoti kiekvieną mokėjimo tipą, kurį pardavėjas priima. Šiame sąraše aprašomas kiekvienas mokėjimo tipas, kurį galima nustatyti.

- **Grynieji pinigai** – pinigai fizine valiutos forma, pavyzdžiui, banknotai ir monetos. Ši valiuta gali būti įmonės valiuta arba vietinė parduotuvės valiuta.
- **Čekis** – perduodamas dokumentas, nurodantis konkrečios sumos konkrečia valiuta mokėjimą, kurį garantuoja konkretus bankas. Čekis paprastai galioja neribotą laiką arba šešis mėnesius nuo išdavimo datos, jei nenurodytas kitoks galiojimo laikotarpis. Šis laikotarpis priklauso nuo banko, garantuojančio mokėjimą pagal čekį. Yra įvairūs čekių tipai, pavyzdžiui, užsakymo čekiai, skaitiklio čekiai, pateikėjo čekiai ir sąskaitos gavėjo čekiai. Galite nustatyti čekius kaip kiekvienos parduotuvės mokėjimo būdą. Gali būti priimami čekiai valiuta, nurodyta įmonės lygiu arba parduotuvės lygiu. Mokėjimą čekiu parduotuvėje galėsite priimti tik nustatę čekius kaip mokėjimo būdą.
- **Valiuta** – pagrindinė mokėjimo forma ne įmonės numatytąja valiuta. Monetos ir popieriniai pinigai yra valiutos formos. Mokėjimo valiuta būdas apima visas naudojamas valiutas. Prieš naudodamiesi šiuo mokėjimo metodu, turite nustatyti valiutas ir nurodyti valiutų keitimo informaciją.
- **Kortelė** – visų rūšių naudojamos kortelės, pavyzdžiui, debeto ir kredito kortelės. Naudinga nustatyti vieną mokėjimo kortele būdą organizacijos lygiu, apimantį bet kokias korteles. Tada parduotuvės lygiu nustatykite mokėjimo būdą, taikomą kiekvienai kortelei arba kortelių rinkiniui, kuris apdorojamas naudojant tuos pačius parametrus. Mokėjimą kortelėmis parduotuvėje galėsite priimti tik nustatę rinkoje esančias gamintojo korteles, pavyzdžiui, debeto ir kredito korteles.
- **Kredito pažyma** – kredito pažymos, išduodamos arba panaudojamos naudojant elektroninį kasos aparatą. Kredito pažyma gali būti kredito arba grąžinimo kredito pažyma, išduota pagal pardavimo grąžinimo pardavimą. Jei kredito pažymos panaudojamos tik dalinai, programa išduoda naują kredito pažymą, kurioje nurodomas naujas balansas. Naujos kredito pažymos numeris yra naujas. Kredito pažymą galima naudoti tik kartą, ir sistema išsaugo įrašą apie visas panaudotas sumas. Įrašą galima peržiūrėti puslapyje **Kredito pažymos lentelė**. Klientas negali panaudoti didesnės nei kredito pažymos vertė sumos.
- **Dovanų kortelė** – dovanų kortelės, išduodamos ir panaudojamos naudojant elektroninį kasos aparatą. Dovanų kortelėms permokėjimai neleidžiami. Visos dovanų kortelės turi turėti kortelės numerio susiejimus. 
- **Kliento sąskaita** – mokėjimai, kuriuos parduodant galima išskaityti iš kasos aparato į kliento sąskaitą. Šio mokėjimo būdą taip pat galite naudoti pardavimo informacijai ar konkretaus kliento nuolaidoms rinkti, kai klientas atlieka mokėjimą naudodamas kitą mokėjimo būdą. Tokiu atveju turite nustatyti konkretaus kliento informaciją.
- **Lojalumo taškai** – taškai, kuriuos klientas kaupia dalyvaudamas lojalumo programose. Sukūrus lojalumo programas klientai gali gauti taškų, o po to juos įvairiais būdais panaudoti. Pavyzdžiui, pagal kai kurias lojalumo programas, klientai gali panaudoti lojalumo taškus nuolaidos forma arba net naudoti juos kaip mokėjimo formą.

Norėdami nustatyti mokėjimo būdus, turite atlikti toliau nurodytus veiksmus.

1. Nustatykite organizacijos mokėjimo būdus. Sukurkite mokėjimo būdus, priimamus visos organizacijos.
2. Sukurkite visai organizacijai taikomų kortelių tipus ir kortelių numerius. Jei priimamos kredito ar debeto kortelės, turite sukurti vieną mokėjimo būdą, naudojamą atsiskaitant kortelėmis, o po to sukurti visai organizacijai taikomus kortelių tipus ir kortelių numerius.
3. Nustatykite parduotuvės mokėjimo būdą. Susiekite mokėjimo būdus su kiekviena parduotuve, o po to įveskite kiekvienos parduotuvės mokėjimo būdo parametrus.
4. Nustatykite parduotuvių mokėjimo kortelėmis būdus. Nustatykite kiekvieno parduotuvės priimamo mokėjimo kortele būdo kortelę.

---
title: Apdoroti priminimo laiškus
description: Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti priminimo laiškus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549634"
---
# <a name="process-collection-letters"></a>Apdoroti priminimo laiškus

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti priminimo laiškus. Šioje užduotyje naudojama demonstracinė įmonė USMF.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Registravimo šablone nustatykite priminimo laiškų seką.
1. Pasirinkite **Kreditas ir mokėjimų priežiūra > Sąranka > Klientų registravimo šablonai**.
2. Spustelėkite **Redaguoti**.
3. Išplečiamajame sąraše pasirinkite priminimo laiškų seką. Jei nenorite generuoti operacijų priminimo laiškų naudodami šį registravimo šabloną, palikite lauką tuščią.  
4. Išplėskite lentelių apribojimų skirtuką, kad pakeistumėte būdą, kuriuo apdorojami priminimo laiškai. Jei šio lauko reikšmė nustatyta kaip **Taip**, bus kuriami šio registravimo šablono priminimo laiškai.  

## <a name="create-collection-letters"></a>Kurti priminimo laiškus
1. Pasirinkite **Kreditas ir mokėjimų priežiūra > Priminimo laiškas > Kurti priminimo laiškus**.
2. Pasirinkite operacijų, kurių laiškus rinksite, tipus. Skaičiuojant bus įtrauktos visos atidarytos šių tipų operacijos.  
2. Lauke **Priminimo laiškas** pasirinkite parinktį.
3. Įveskite priminimo laiško datą.
4. Pasirinkite registravimo šabloną, jei **Naudoti registravimo šabloną iš** pakeitėte į **Pasirinkti**. Yra dvi registravimo profilio parinktys:   
   - **Sąskaita** – naudokite registravimo šabloną, priskirtą kliento sąskaitai, kiekvienai delspinigių pažymai.   
   - **Pasirinkti** – naudokite registravimo šabloną, kurį pasirenkate lauke **Registravimo šablonas**.  
5. Išplėskite dalį **Įtrauktini įrašai**.
6. Spustelėkite **Filtras**.
7. Lauke **Kriterijai** įveskite Kliento ID. Pvz., įveskite „US-001‟.
8. Spustelėkite **Gerai**.
9. Spustelėkite **Gerai**.

## <a name="print-collection-letters"></a>Priminimo laiškų spausdinimas
1. Pasirinkite **Kreditas ir mokėjimų priežiūra > Priminimo laiškas > Peržiūrėti ir apdoroti priminimo laiškus**.
2. Lauke **Būsena** pasirinkite **Sukurta**.
3. Lauke **Išspausdinta** pasirinkite **Neišspausdinta**.
4. Spustelėkite **Spausdinti**.
5. Spustelėkite **Priminimo laiško pastaba**.
6. Išplėskite dalį **Įtrauktini įrašai**.
7. Įveskite registravimų galutinę datą.
8. Spustelėkite **Gerai**, jei norite spausdinti priminimo laišką.
9. Priminimo laiško registravimas.
   1. Spustelėkite **Registruoti.**
   2. Įveskite priminimo laiško registravimo datą.
   3. Išplėskite dalį **Įtrauktini įrašai**.
   4. Spustelėkite **Gerai**.
   5. Lauke **Būsena** pasirinkite **Užregistruota**.
   6. Lauke **Išspausdinta** pasirinkite parinktį.

## <a name="control-collection-letters-at-the-customer-level"></a>Valdykite priminimo laiškus kliento lygiu
Taip pat galite nustatyti priminimo laiškus kliento lygiu, kad būtų sekamas kiekvienos operacijos priminimo laiško kodas, tačiau priminimo laiško apdorojimas bus grindžiamas vieno priminimo laiško lygiu, kuris saugomas klientui. Viename priminimo laiške bus visos pradelstos kliento operacijos. Nors atidėjimo dienos dabar sekamos kliento lygiu, kitas priminimo laiškas nebus išsiųstas, kol nepraeis kito sekoje esančio priminimo laiško atidėjimo dienų skaičius net jei po paskutinio išsiųsto priminimo laiško operacijos taps pradelstos. Ši parinktis sumažina priminimo laiškų, kuriuos siųsite vienam klientui, skaičių. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Nustatykite klientą, kad galėtumėte valdyti priminimo laiškus kliento lygiu
1.  Pasirinkite **Kreditas ir mokėjimų priežiūra > Sąranka > Gautinų sumų parametrai** ir spustelėkite skirtuką **Mokėjimų priežiūra**. 
2.  Pakeiskite parametro **Priminimo laiško kūrimas** vertę į **Klientas**. 
3.  Pasirinkite **Kreditas ir mokėjimų priežiūra > Priminimo laiškas > Peržiūrėti ir apdoroti priminimo laiškus**. Klientui bus sugeneruotas tik vienas priminimo laiškas su visomis pradelstomis operacijomis.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą
Jei į operacijas įtraukiami mokėjimai ir kredito pažymos, kurios bus įtrauktos į priminimo laiškus, gali būti mokėjimų arba kredito pažymų, kurios suaktyvins priminimo laišką. Galite kontroliuoti, kaip mokėjimai ir kredito pažymos valdo priminimo laiško kodą, keisdami parametro **Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą** vertę. 

Norėdami nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą, atlikite toliau nurodytus veiksmus.
1. Pasirinkite **Kreditas ir mokėjimų priežiūra > Sąranka > Gautinų sumų parametrai** ir spustelėkite skirtuką **Mokėjimų priežiūra**. 
2. Pakeiskite parametro **Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą** vertę į **Taip**.

---
title: Priminimo laiškų apdorojimas
description: Šioje temoje nurodoma, kaip kurti, spausdinti ir registruoti priminimo laiškus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179071"
---
# <a name="process-collection-letters"></a>Priminimo laiškų apdorojimas

[!include [banner](../../includes/banner.md)]

Šioje temoje nurodoma, kaip kurti, spausdinti ir registruoti priminimo laiškus. Šioje užduotyje naudojama demonstracinė įmonė USMF.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Registravimo šablone nustatykite priminimo laiškų seką.
1. Eikite į **Naršymo sritis > Moduliai > Kreditas ir mokesčių rinkimas > Sąranka > Klientų registravimo šablonai**.
2. Spustelėkite **Redaguoti**.
3. Išplečiamajame sąraše pasirinkite priminimo laiškų seką. Jei nenorite generuoti operacijų priminimo laiškų naudodami šį registravimo šabloną, palikite lauką tuščią.  
4. Išskleiskite skirtuką **Lentelės apribojimai**, kad pakeistumėte priminimo laiškų apdorojimo būdą. Jei šio lauko reikšmė nustatyta kaip **Taip**, bus kuriami šio registravimo šablono priminimo laiškai.  

## <a name="create-collection-letters"></a>Kurti priminimo laiškus
1. Eikite į **Naršymo sritis > Moduliai > Kreditas ir mokesčių rinkimas > Priminimo laiškas > Kurti priminimo laiškus**.
2. Pasirinkite operacijų, kurių laiškus rinksite, tipus. Skaičiuojant bus įtrauktos visos atidarytos šių tipų operacijos.  
3. Lauke **Priminimo laiškas** pasirinkite parinktį.
4. Lauke **Priminimo laiško data** įveskite priminimo laiško datą.
5. Pasirinkite registravimo šabloną, jei **Naudoti registravimo šabloną iš** pakeitėte į **Pasirinkti**. Yra dvi registravimo profilio parinktys:   

   - **Sąskaita** – naudokite registravimo šabloną, priskirtą kliento sąskaitai, kiekvienai delspinigių pažymai.   
   - **Pasirinkti** – naudokite registravimo šabloną, kurį pasirenkate lauke **Registravimo šablonas**.  

6. Išplėskite dalį **Įtrauktini įrašai**.
7. Pasirinkite **Filtras**.
8. Lauke **Kriterijai** įveskite Kliento ID. Pvz., įveskite „US-001‟.
9. Pasirinkite **Gerai**.
10. Pasirinkite **Gerai**.

## <a name="print-collection-letters"></a>Priminimo laiškų spausdinimas
1. Eikite į **Naršymo sritis > Moduliai > Kreditas ir mokesčių rinkimas > Priminimo laiškas > Peržiūrėti ir apdoroti priminimo laiškus**.
2. Lauke **Būsena** pasirinkite **Sukurta**.
3. Lauke **Išspausdinta** pasirinkite **Neišspausdinta**.
4. Pasirinkite **Spausdinti**.
5. Pasirinkite **Priminimo laiško pažyma**.
6. Skyriuje **Parametrai** įveskite galutinę laiškų registravimo datą.
7. Išskleiskite skyrių **Įtraukti į įrašus** ir įveskite išsamią informaciją apie priminimo laiško pažymą.
8. Pasirinkite **Gerai**, kad pradėtumėte spausdinti priminimo laišką.
9. Priminimo laiško registravimas.

    1. Pasirinkite **Registruoti**.
    1. Įveskite priminimo laiško registravimo datą.
    1. Išplėskite dalį **Įtrauktini įrašai**.
    1. Pasirinkite **Gerai**.
    1. Lauke **Būsena** pasirinkite **Užregistruota**.
    1. Lauke **Išspausdinta** pasirinkite parinktį.

## <a name="control-collection-letters-at-the-customer-level"></a>Valdykite priminimo laiškus kliento lygiu
Taip pat galite nustatyti priminimo laiškus kliento lygiu, kad būtų sekamas kiekvienos operacijos priminimo laiško kodas, tačiau priminimo laiško apdorojimas bus grindžiamas vieno priminimo laiško lygiu, kuris saugomas klientui. Viename priminimo laiške bus visos pradelstos kliento operacijos. Nors atidėjimo dienos dabar sekamos kliento lygiu, kitas priminimo laiškas nebus išsiųstas, kol nepraeis kito sekoje esančio priminimo laiško atidėjimo dienų skaičius net jei po paskutinio išsiųsto priminimo laiško operacijos taps pradelstos. Ši parinktis sumažina priminimo laiškų, kuriuos siųsite vienam klientui, skaičių. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Nustatykite klientą, kad galėtumėte valdyti priminimo laiškus kliento lygiu
1.  Eikite į **Naršymo sritis > Moduliai > Kreditas ir mokesčių rinkimas > Sąranka > Gautinos sumos parametrai** ir pasirinkite skirtuką **Mokesčių rinkimas**. 
2.  Pakeiskite parametro **Priminimo laiško kūrimas** vertę į **Klientas**. 
3.  Eikite į **Naršymo sritis > Moduliai > Kreditas ir mokesčių rinkimas > Priminimo laiškas > Peržiūrėti ir apdoroti priminimo laiškus**. Klientui bus sugeneruotas tik vienas priminimo laiškas su visomis pradelstomis operacijomis.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą
Jei į operacijas įtraukiami mokėjimai ir kredito pažymos, kurios bus įtrauktos į priminimo laiškus, gali būti mokėjimų arba kredito pažymų, kurios suaktyvins priminimo laišką. Galite kontroliuoti, kaip mokėjimai ir kredito pažymos valdo priminimo laiško kodą, keisdami parametro **Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą** vertę. 

Norėdami nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Naršymo sritis > Moduliai > Kreditas ir mokesčių rinkimas > Sąranka >Gautinų sumų parametrai** ir paspauskite skirtuką **Mokesčių rinkimas**. 
2. Pakeiskite parametro **Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą** vertę į **Taip**.

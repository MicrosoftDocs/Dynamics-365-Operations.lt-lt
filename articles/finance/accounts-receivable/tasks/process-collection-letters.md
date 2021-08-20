---
title: Priminimo laiškų apdorojimas
description: Šioje temoje nurodoma, kaip kurti, spausdinti ir registruoti priminimo laiškus.
author: ShivamPandey-msft
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 9355409076886b70ad224c82561cf0cf81066e9b97e1a22ad59ce04be2c90158
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762120"
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
Jei priminimo laiškai nustatomi operacijos lygiu, klientui gali būti sugeneruota keletas raidžių, remiantis operacijos skirstymu pagal terminus. Jei operacijos pateikiamos skirtingomis raidžių sekomis, kiekvienai pradelstų operacijų grupei klientui bus sugeneruoti atskiri priminimo laiškai. Todėl klientas gali gauti, pavyzdžiui, vieną priminimo laišką už pradelstas 60 dienų operacijas ir kitą priminimo laišką už pradelstas 90 dienų operacijas. 

Kiekvienas priminimo laiškas taip pat susietas su priminimo laiško kodu. Priminimo laiško kodas yra susietas su individualia operacija ir jį naudojant nustatoma, kada turi būti sugeneruotas kitas kiekvienos operacijos priminimo laiškas. Pavyzdžiui, jei operacija yra pradelsta daugiau nei 30 dienų, priminimo laiško kodas nurodo, kad kitas priminimo laiškas bus išsiųstas tada, kai operacija pradelsta 60 dienų, jei ji nesumokama anksčiau. 

Priminimo laiškus taip pat galima nustatyti kliento lygiu. Tokiu atveju stebimas kiekvienos operacijos priminimo laiško kodas, tačiau priminimo laiško apdorojimas bus grindžiamas vieno priminimo laiško lygiu, kuris saugomas klientui. Viename priminimo laiške bus visos pradelstos kliento operacijos. Nors atidėjimo dienos dabar sekamos kliento lygiu, kitas priminimo laiškas nebus išsiųstas, kol nepraeis kito sekoje esančio priminimo laiško atidėjimo dienų skaičius net jei po paskutinio išsiųsto priminimo laiško operacijos taps pradelstos. Ši parinktis sumažina priminimo laiškų, kuriuos turite siųsti kiekvienam klientui, skaičių.

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Nustatykite klientą, kad galėtumėte valdyti priminimo laiškus kliento lygiu
1.  Eikite į **Naršymo sritis > Moduliai > Kreditas ir mokesčių rinkimas > Sąranka > Gautinos sumos parametrai** ir pasirinkite skirtuką **Mokesčių rinkimas**. 
2.  Pakeiskite parametro **Priminimo laiško kūrimas** vertę į **Klientas**. 
3.  Eikite į **Naršymo sritis > Moduliai > Kreditas ir mokesčių rinkimas > Priminimo laiškas > Peržiūrėti ir apdoroti priminimo laiškus**. Klientui bus sugeneruotas tik vienas priminimo laiškas su visomis pradelstomis operacijomis.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą
Jei į operacijas įtraukiami mokėjimai ir kredito pažymos, kurios bus įtrauktos į priminimo laiškus, gali būti mokėjimų arba kredito pažymų, kurios suaktyvins priminimo laišką. Galite kontroliuoti, kaip mokėjimai ir kredito pažymos valdo priminimo laiško kodą, keisdami parametro **Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą** vertę. 

Norėdami nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Naršymo sritis > Moduliai > Kreditas ir mokesčių rinkimas > Sąranka >Gautinų sumų parametrai** ir paspauskite skirtuką **Mokesčių rinkimas**. 
2. Pakeiskite parametro **Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą** vertę į **Taip**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
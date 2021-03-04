---
title: Grynųjų pinigų valdymo patobulinimai
description: Šioje temoje aprašomi EKA grynųjų pinigų valdymo patobulinimai, skirti „Dynamics 365 Commerce“.
author: anpurush
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
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
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0c561c39dfcbfa739c5a22394c05191e7f9bc107
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414312"
---
# <a name="cash-management-improvements"></a>Grynųjų pinigų valdymo patobulinimai

[!include [banner](includes/banner.md)]


Grynųjų pinigų valdymas yra pagrindinė fizinių mažmeninės prekybos parduotuvių funkcija. Mažmenininkai nori, kad jų parduotuvėse veiktų sistemos, galinčios padėti užtikrinti visišką grynųjų pinigų atsekamumą ir atskaitomybę bei jų judėjimą tarp įvairių parduotuvės registrų ir kasininkų. Jie privalo galėti suderinti visus skirtumus ir nustatyti atskaitomybę.


Į „Microsoft Dynamics 365 Commerce“ įtrauktos grynųjų pinigų valdymo galimybės elektroninio kasos aparato (EKA) programoje. Tačiau „Retail“ versijose, kurios yra ankstesnės nei 10.0.3 versija, grynųjų pinigų valdymo funkcijos nėra nepakankamai galinga, kad būtų užtikrintas visiškas grynųjų pinigų judėjimo parduotuvėse atsekamumas. Nors mažmenininkai gali suderinti parduotuvės grynuosius pinigus, jie negali tiksliai nustatyti atskaitomybės, jei kilo grynųjų pinigų neatitikimų.


„Retail“ 10.0.3 ir naujesnėse versijoje mažmenininkai galės atsekti grynųjų pinigų valdymą. Naudodami šią atsekamumo funkciją mažmenininkai galės nustatyti seifus, dvipuses grynųjų pinigų operacijas ir suderinti grynųjų pinigų valdymo operacijas.

## <a name="set-up-traceability-and-define-safes"></a>Atsekamumo ir seifų nustatymas

Norėdami nustatyti naują grynųjų pinigų valdymo funkciją, atlikite toliau nurodytus veiksmus ir sukonfigūruokite parduotuvių funkcijų profilį.

1. Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> EKA sąranka \> EKA profiliai \> Funkcijų profiliai** ir pasirinkite funkcijų profilį, susietą su parduotuvėmis, kurių galimų grynųjų pinigų valdymo patobulinimus norite atlikti.
2. Funkcijų profilio „FastTab“ **Funkcijos** skiltyje **Išplėstinis grynųjų pinigų valdymas** nustatykite parinkties **Įjungti grynųjų pinigų atsekamumą** vertę **Taip**.
3. Norėdami nustatyti seifus, pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalai \> Parduotuvės \> Visos parduotuvės** ir pasirinkite parduotuvę.
4. Puslapio **Parduotuvės** veiksmų srities skirtuke **Sąranka**, grupėje **Sąranka** pasirinkite **Seifai**. Naudodami šią parinktį galite nustatyti ir tvarkyti kelis parduotuvės seifus.
4. Prieš naudodami funkciją turite paleisti paketinę paskirstymo užduotį **1070 kanalo konfigūravimas**, kad sinchronizuotumėte šias konfigūracijas su kanalo duomenų baze.

## <a name="additional-cash-management-changes"></a>Papildomi grynųjų pinigų valdymo pakeitimai

„Retail“ 10.0.3 ir naujesnėje versijose taip pat pateikiamos toliau nurodytos galimybės, susijusios su grynųjų pinigų operacijomis.

- Vartotojas, kuris yra paragintas „deklaruoti pradžios sumą“, turi įvesti grynųjų pinigų šaltinį. Vartotojas gali ieškoti galimų seifų, kurie nurodyti parduotuvėje, ir pasirinkti seifą, iš kurio išimami grynieji pinigai, kad jie būtų įtraukti į registrą.
- Vartotojas, kuris atlieka operaciją „mokėjimo priemonės pašalinimas“, atidarytų „srauto įrašų“ operacijų sąraše paraginamas pasirinkti operaciją, kuri susijusi su atliekama operacija. Jei sistemoje nėra atitinkamo srauto įrašo, vartotojas gali sukurti nesusijusią mokėjimo priemonės pašalinimo operaciją.
- „Srauto įrašo“ operacija „mokėjimo priemonių pašalinimo“ operacijų sąraše paragina vartotoją pasirinkti operaciją, kuri susijusi su atliekama srauto įrašo operacija. Jei sistemoje nėra atitinkamo mokėjimo priemonės pašalinimo, vartotojas gali sukurti nesusijusią srauto įrašo operaciją.
- „Pinigų įnešimo į seifą“ operaciją atliekantis vartotojas paraginamas pasirinkti seifą, į kurį bus įnešti pinigai.
- Jei seifai nustatomi parduotuvėje, vartotojai gali valdyti operacijas, pvz., pradžios sumos deklaravimo, srauto įrašo kūrimo, mokėjimo priemonės pašalinimo ir pinigų įnešimo į banką operacijas.
- Vartotojams, kuriems priskirtos atitinkamos vartotojo teisės, „pamainų valdymo“ operacijos rodo aktyvių, sulaikytų ir anonimiškai uždarytų pamainų grynųjų pinigų balansai.
- Norėdami suderinti grynųjų pinigų operacijas pamainoje arba pamainose, pasirinkite pamainą, kurią norite derinti, tada pasirinkite **Derinti**. Atidarytas rodinys pateikia suderintų ir nesuderintų operacijų sąrašą atskiruose skirtukuose. Šiame rodinyje vartotojai gali pasirinkti nesuderintas operacijas ir jas suderinti arba pasirinkti anksčiau suderintas operacijas ir panaikinti jų suderinimą.
- Jei derinant pažymėta operacija nėra subalansuojama, vartotojas turi įvesti nesubalansuoto suderinimo priežasties aprašą. Vartotojai gali pasirinkti vieną operaciją ir suderinti ją pagal poreikį naudodami atitinkamą priežasties aprašą.
- Vartotojai gali ir toliau derinti operacijas bei naikinti operacijų suderinimą, kol pamaina neuždaryta. Uždarius pamainą, operacijų suderinimo panaikinti negalima.
- Kai vartotojas pasirenka uždaryti pamainą, „Commerce“ patikrina, ar pamainoje nėra nesuderintų grynųjų pinigų valdymo operacijų. Vartotojai negali uždaryti pamainos, jei yra nesuderintų operacijų.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
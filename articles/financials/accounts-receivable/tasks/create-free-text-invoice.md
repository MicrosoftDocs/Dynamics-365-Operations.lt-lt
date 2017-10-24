--- 
title: "Kurti laisvos formos sąskaitą faktūrą"
description: "Šis užduočių vadovas parodo, kaip sukurti laisvos formos SF."
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 33324a9b95026600bcc6facb9c22a04fd2e323c8
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-free-text-invoice"></a>Kurti laisvos formos sąskaitą faktūrą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas parodo, kaip sukurti laisvos formos SF. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pasirinkite Gautinos sumos > Sąskaitos faktūros > Visos laisvos formos SF.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita pasirinkite reikšmę.
    * Pagal numatytąsias nuostatas SF sąskaita bus ta pati, kuri naudojama kaip kliento sąskaita.   
    * Jei SF neužregistruota, pirmoji apskaitos būsena yra Vykdoma.   
    * SF numeris bus priskirtas užregistravus SF.  
    * Jei naudojate SEPA įgaliojimus, jums pasirinkus kliento sąskaitą, tiesioginio debeto įgaliojimas bus automatiškai užpildytas įgaliojimu.  
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Pagrindinė sąskaita nurodykite sąskaitos numerį be dimensijų.
    * Norėdami rasti savo sąskaitą, taip pat galite įvesti vieną ar kelis pagrindinės sąskaitos simbolius ir naudoti peržvalgą. Dimensijas įvesite vėliau šiame vadove.  
6. Išplėtę „FastTab‟ Išsami eilutės informacija, galėsite į savo pagrindinę sąskaitą pridėti dimensijų.
7. Spustelėkite skirtuką Finansinių dimensijų eilutė.
    * Nurodytos tik pasirinktos eilutės dimensijos.    
    * PVM grupė automatiškai užpildoma pagal klientą. Jei klientas neturi PVM grupės, naudojama PVM grupė iš pagrindinės sąskaitos.  
    * Prekių PVM grupė automatiškai užpildoma pagal pagrindinę sąskaitą. Jei pagrindinė sąskaita neturi prekių PVM grupės, tada naudojama prekių PVM grupė, esanti DK PVM parametruose.    
8. Lauke Kiekis įveskite skaičių.
    * Kiekis yra neprivalomas.  
9. Lauke Vieneto kaina įveskite skaičių.
    * Vieneto kaina yra neprivaloma.  
    * Suma skaičiuojama kaip kiekis, padaugintas iš vieneto kainos. Tačiau to skaičiavimo galite nepaisyti ir sumą įvesti.  
10. Spustelėję ant PVM, galėsite peržiūrėti apskaičiuotą SF PVM.
    * Peržiūrėkite PVM sumas šiame puslapyje, arba galite pakeisti sumas skirtuke Koregavimas.  
11. Spustelėkite GERAI.
12. Spustelėję Išlaidos, galėsite į savo sąskaitą faktūrą įtraukti išlaidų. 
13. Lauke Išlaidų kodas surinkite reikšmę.
14. Lauke Išlaidų vertė įveskite skaičių.
15. Uždarykite puslapį.
16. Spustelėję Bendrosios sumos, galėsite peržiūrėti suvestinės SF informaciją ir bendrąsias sumas.
17. Spustelėkite Uždaryti.
18. Norėdami registruoti sąskaitą faktūrą, spustelėkite Registruoti. Prieš registruodami galėsite atšaukti.
    * Norėdami pakeisti laiką, kad spausdinamos jūsų SF: pasirinkus Iškart, atnaujinus kiekvieną SF ji iškart spausdinama, arba Vėliau (SF spausdinamos, kai atnaujintos visos SF).  
    * Jei norite pakeisti, kaip prieš registruojant tikrinamas kliento kredito limitas, pakeiskite kredito limito tipą.  
    * Jei norite spausdinti sąskaitą faktūrą, pasirinkite Taip.  
    * Jei norite registruoti sąskaitą faktūrą, pasirinkite Taip. Galite spausdinti SF jos neregistruodami.  
19. Spustelėkite GERAI.



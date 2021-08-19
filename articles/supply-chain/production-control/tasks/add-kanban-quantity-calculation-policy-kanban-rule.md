---
title: Į „kanban“ taisyklę įtraukti „kanban“ kiekio skaičiavimo strategiją
description: Šios procedūros tikslas yra sukurti „kanban“ kiekio skaičiavimo strategiją ir įtraukti ją į „kanban“ taisyklę, siekiant optimizuoti „kanban“ dydį ir kiekius.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules, KanbanQuantityCalculation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57d5bc5c93fa8f1aef58b9c346df06d17edef0d7cdd863f5e6ce2d42bc3d56aa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754661"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Į „kanban“ taisyklę įtraukti „kanban“ kiekio skaičiavimo strategiją

[!include [banner](../../includes/banner.md)]

Šios procedūros tikslas yra sukurti „kanban“ kiekio skaičiavimo strategiją ir įtraukti ją į „kanban“ taisyklę, siekiant optimizuoti „kanban“ dydį ir kiekius. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta vertės srauto vadybininkui. Ši procedūra yra būtina norint sukurti procedūrą „Skaičiuoti „kanban“ kiekio pasiūlymus“. 


## <a name="create-a-kanban-quantity-calculation-policy"></a>Sukurti „kanban“ kiekio skaičiavimo strategiją
1. Pasirinkite Gamybos kontrolė > Periodinės užduotys > „Kanban“ kiekio skaičiavimas > „Kanban“ kiekio skaičiavimo strategijos.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
    * Pvz., įveskite „Speaker2016“.  
4. Lauke „Bendrasis planas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite „StaticPlan“ poreikiui apskaičiuoti.  
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Spustelėkite Įrašyti.
8. Lauke „Žemiausias „kanban“ kiekis“ įveskite „1“.
    * Tai yra papildomas „kanban“ skaičius, įtrauktas į „kanban“ kiekio skaičiavimą.  
9. Nustatykite pakankamumo koeficiento reikšmę „1“.
    * Tai yra koeficientas, naudojamas papildomam pakankamų atsargų kiekiui apskaičiuoti.  
10. Lauke „Dienų į priekį“ įveskite „30‟.
    * Tai yra dienų skaičius prieš „kanban“ kiekio skaičiavimo datą, įtrauktas į poreikio skaičiavimą.  
11. Lauke „Dienų atgal“ įveskite „30‟.
    * Tai yra dienų skaičius nuo „kanban“ kiekio skaičiavimo datos, įtrauktas į poreikio skaičiavimą.  Skaičiavimui naudojama formulė rodoma su faktinėmis reikšmėmis. Pvz., „kanban“ kiekis = ((vidutinis kasdienis poreikis x gamybos laikas x 2,00) / produkto kiekis sandėliavimo vienetui) + 1  
12. Uždarykite puslapį.

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Į „kanban“ taisyklę įtraukti „kanban“ kiekio skaičiavimo strategiją
1. Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Šiai procedūrai pasirinkite „kanban“ taisyklę 000020.  
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Perjunkite skyriaus „Kanban“ kiekio skaičiavimo strategija“ išplėtimą.
5. Spustelėkite Pridėti.
    * Pridėkite „kanban“ kiekio skaičiavimo strategiją, kurią ką tik sukūrėte ankstesnėje papildomoje užduotyje.  
6. Sąraše pažymėkite pasirinktą eilutę.
7. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite „Speaker2016“ strategiją, kurią ką tik sukūrėte ankstesnėje papildomoje užduotyje.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
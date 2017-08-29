--- 
title: " Mažmeninės prekybos parduotuvės išrašo kūrimas, skaičiavimas ir registravimas"
description: "Ši procedūra padeda neautomatiškai kurti, apskaičiuoti ir registruoti parduotuvės išrašą."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 60bcafffc922e6d57e52a5dff104a0fbb252f6ce
ms.contentlocale: lt-lt
ms.lasthandoff: 07/28/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a> Mažmeninės prekybos parduotuvės išrašo kūrimas, skaičiavimas ir registravimas

[!include[task guide banner](../includes/task-guide-banner.md)]

Ši procedūra padeda neautomatiškai kurti, apskaičiuoti ir registruoti parduotuvės išrašą. Taip pat galima sukonfigūruoti tų pačių užduočių paketines užduotis. Paketinių užduočių konfigūravimo ir paleidimo veiksmai aprašyti kitose temose. Norint atlikti šią procedūrą, reikalingos operacijos, kurios atliktos naudojant EKA ir įtrauktos į „Dynamics AX“. Šiame įraše naudojama demonstracinių duomenų įmonė USRT. Šioje procedūroje gali būti nurodyta „Microsoft Dynamics AX“. Atkreipkite dėmesį, kad „Dynamics AX“ dabar vadinama „Microsoft Dynamics 365 for Operations“.

1. Eikite į Visos darbo sritys > .. > Mažmeninės prekybos parduotuvės finansai.
2. Spustelėkite Naujas išrašas.
3. Lauke Parduotuvės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Spustelėkite GERAI.
    * Tam tikri nustatymo grupės parametrai kontroliuoja, kurios operacijos įtraukiamos į išrašą ir kaip jos bus grupuojamos išrašo eilutėse. Galite atidaryti nustatymo grupę ir keisti šiuos parametrus arba galite naudoti numatytuosius.  
    * Laukas Išrašo metodas nurodo, kaip bus grupuojamos išrašo eilutės.  
    * Pasirinkite darbuotoją arba registrą, jei norite apskaičiuoti tik konkretaus darbuotojo arba registro išrašą.  
6. Lauke Uždarymo metodas pasirinkite parinktį.
7. Spustelėkite Skaičiuoti išrašą.
8. Spustelėkite Taip.
    * Apskaičiavus išrašą, turėtų būti sukurtos eilutės su kiekvieno naudoto mokėjimo metodo ir išrašo metodo bendrosiomis sumomis.  
    * Įveskite apskaičiuotą sumą kiekvienoje eilutėje, jei ji turi būti įvesta arba atnaujinta. Apskaičiuotas laukas užpildomas naudojant sumas iš EKA atliktų mokėjimo priemonių deklaracijų.  
9. Spustelėkite Registruoti išrašą.
10. Spustelėkite Uždaryti.
11. Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Mažmeninės prekybos parduotuvės finansai.
12. Spustelėkite skirtuką Užregistruoti išrašai.



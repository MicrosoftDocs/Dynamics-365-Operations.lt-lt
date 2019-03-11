---
title: " Mažmeninės prekybos parduotuvės išrašo kūrimas, skaičiavimas ir registravimas"
description: Ši procedūra padeda neautomatiškai kurti, apskaičiuoti ir registruoti parduotuvės išrašą.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9ea30e7e008bfcce77a7ee2f4d7d01a6cf1ababc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "354396"
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


---
title: Mažmeninės prekybos parduotuvės išrašų kūrimas, skaičiavimas ir registravimas
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
ms.openlocfilehash: 693d1821779d5f7af95b900daa3bb7a2c38a6354
ms.sourcegitcommit: cb63259ad8fa5649ff12bc4a7f195bd1e40bd968
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755528"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Mažmeninės prekybos parduotuvės išrašų kūrimas, skaičiavimas ir registravimas

[!include[task guide banner](../includes/task-guide-banner.md)]

Ši procedūra padeda neautomatiškai kurti, apskaičiuoti ir registruoti parduotuvės išrašą. Taip pat galima sukonfigūruoti tų pačių užduočių paketines užduotis. Paketinių užduočių konfigūravimo ir paleidimo veiksmai aprašyti kitose temose. Norint atlikti šią procedūrą, reikalingos operacijos, kurios atliktos naudojant EKA ir įtrauktos į „Dynamics Dynamics 365 for Finance and Operations“. Šiame įraše naudojama demonstracinių duomenų įmonė USRT.

1. Pagrindiniame puslapyje pasirinkite **Mažmeninės prekybos parduotuvės finansai**.
2. Pasirinkite **Naujas išrašas**.
3. Lauke **Parduotuvės numeris** spustelėkite išplečiamąjį mygtuką, kad pasirinktumėte parinktį.
4. Pasirinkite **Gerai**.
5. Tam tikri grupės **Sąranka** parametrai kontroliuoja, kurios operacijos įtraukiamos į išrašą ir kaip jos bus grupuojamos išrašo eilutėse. Galite atidaryti grupę **Sąranka** ir keisti šiuos parametrus arba galite naudoti numatytuosius.  
    - Laukas **Išrašo metodas** nurodo, kaip bus grupuojamos išrašo eilutės.  
    - Pasirinkite darbuotoją arba registrą, jei lauke **darbuotojai arba registras** norite apskaičiuoti tik konkretaus darbuotojo arba registro išrašą.  
6. Lauke **Uždarymo metodas** pasirinkite parinktį.
7. Veiksmų srityje pasirinkite **Skaičiuoti išrašą**.
8. Pasirinkite **Taip**.
    - Apskaičiavus išrašą, turėtų būti sukurtos eilutės su kiekvieno naudoto mokėjimo metodo ir išrašo metodo bendrosiomis sumomis.  
    - Įveskite apskaičiuotą sumą kiekvienoje eilutėje, jei ji turi būti įvesta arba atnaujinta. Apskaičiuotas laukas užpildomas naudojant sumas iš EKA atliktų mokėjimo priemonių deklaracijų.  
9. Veiksmų srityje pasirinkite **Registruoti išrašą**.
10. Pasirinkite **Uždaryti**.
11. Uždarykite puslapį.
12. Pagrindiniame puslapyje pasirinkite **Parduotuvės finansai**.
13. Spustelėkite skirtuką **Užregistruoti išrašai**.


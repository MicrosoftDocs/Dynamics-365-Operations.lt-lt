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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 455dee5a14ca0c44ba823a467baa78352b367ec8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221310"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Mažmeninės prekybos parduotuvės išrašų kūrimas, skaičiavimas ir registravimas

[!include [banner](../includes/banner.md)]

Ši procedūra padeda neautomatiškai kurti, apskaičiuoti ir registruoti parduotuvės išrašą. Taip pat galima sukonfigūruoti tų pačių užduočių paketines užduotis. Paketinių užduočių konfigūravimo ir paleidimo veiksmai aprašyti kitose temose. Norint atlikti šią procedūrą, reikalingos operacijos, kurios atliktos naudojant EKA ir įtrauktos į „Dynamics Dynamics 365 Commerce“. Šiame įraše naudojama demonstracinių duomenų įmonė USRT.

1. Pagrindiniame puslapyje pasirinkite **Parduotuvės finansai**.
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
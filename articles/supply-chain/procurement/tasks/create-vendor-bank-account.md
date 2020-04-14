---
title: Sukurti tiekėjo banko sąskaitą
description: Šia procedūra parodoma, kaip kurti tiekėjo banko kodą.
author: mkirknel
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be06343aba974ff23a7f328d2175f00768a76465
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149578"
---
# <a name="create-a-vendor-bank-account"></a>Sukurti tiekėjo banko sąskaitą

[!include [banner](../../includes/banner.md)]

Šia procedūra parodoma, kaip kurti tiekėjo banko kodą. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.

1. Eikite į **Naršymo sritis > Moduliai > Įsigijimas ir išteklių paskirstymas > Tiekėjai > Visi tiekėjai**.
2. Pasirinkite tiekėją, kuriam norite sukurti banko sąskaitą, tada spustelėkite saitą lauke **Tiekėjo kliento ID**.
3. **Veiksmų sritis** spustelėkite **Tiekėjas**.
4. Spustelėkite **Banko sąskaitos**.
5. **Veiksmų sritis** spustelėkite **Naujas**.
6. Lauke **Banko sąskaita** įveskite reikšmę. Šis ID bus naudojamas siekiant identifikuoti tiekėjo įrašo banko kodą.  
7. Lauke **Pavadinimas** įveskite reikšmę.
8. Lauke **Banko grupės** įveskite arba pažymėkite reikšmę.
9. Lauke **Numerio tipo maršrutizavimas** pažymėkite parinktį. Tai yra banko kodo, naudojamo tarptautiniams mokėjimams atlikti, tipas.  
10. Lauke **Banko sąskaitos numeris** įveskite reikšmę.
11. Lauke **SWIFT kodas** įveskite reikšmę.
12. Lauke **IBAN** įveskite reikšmę.
    - IBAN numeris turi būti tinkamo formato. Pavyzdžiui, galite naudoti DE89370400440532013000.  
    - Banko sąskaitos būsena yra Aktyvi, jei pasiekta Aktyvinimo data, o galiojimo laikas dar nesibaigė. Ji taip pat aktyvi, jei laukai Aktyvinimo data ir Galiojimo data yra nenurodyti. Jei datos nurodytos laukuose Aktyvinimo data ir Galiojimo data yra būsimos, elektroniniai mokėjimai nėra galimi. Kiti mokėjimo tipai yra galimi ir banko sąskaita yra aktyvi.  
13. Išplėskite skyrių **Sąranka**.
14. Lauke **Tekstinis kodas** įveskite reikšmę. Šiame lauke nurodomas kodas, kuris bus rodomas gavėjo banko išraše.  
15. Lauke **Pranešimas bankui** įveskite reikšmę.
16. Lauke **Valiutos nuoroda** įveskite reikšmę. Tai yra bet kurio būsimo ar fiksuoto valiutos kurso nuorodos numeris.
17. Lauke **Valiuta** įveskite arba pažymėkite reikšmę. Išduodant išankstinius pranešimus, šioje sekcijoje pateikiama jų būsenų (laukiama arba patvirtinta) apžvalga.  
18. Išplėskite skyrių **Adresas**.
19. Išplėskite skyrių **Išankstinis pranešimas**.
20. Išplėskite skyrių **Kontaktinė informacija**.
21. Lauke **Telefonas** įveskite reikšmę.
22. Uždarykite puslapį.
23. Spustelėkite **Redaguoti**.
24. Išplėskite skyrių **Mokėjimas**.
25. Lauke **Banko sąskaita** pažymėkite ką tik sukurtą sąskaitą.
26. Spustelėkite **Įrašyti**. Adresą galima nuskaityti iš bankų grupės, jei ji nurodyta, arba galima jį įtraukti čia.  


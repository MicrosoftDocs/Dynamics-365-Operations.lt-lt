---
title: (ER) Konfigūracijų importavimas iš RCS
description: Šioje temoje pateikiama informacija apie tai, kaip vartotojas gali importuoti naują ER konfigūracijos versiją iš RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 799abeafe5f0929e6dd2f8a5f437f3c10b3b06d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570541"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Konfigūracijų importavimas iš RCS

[!include [banner](../../includes/banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo rolę turintis vartotojas gali importuoti naują elektroninių ataskaitų (ER) versiją iš „Microsoft Regulatory Configuration Service“ (RCS). Šiame pavyzdyje jūs pasirinksite ER konfigūracijos versiją, kuri buvo sukonfigūruota RCS egzemplioriuje, ir importuosite ją į dabartinį tos pačios įmonės („Litware, Inc.“) egzempliorių. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas įmonės naudoja bendrai. Norint atlikti šiuos veiksmus, pirmiausia reikia atlikti veiksmus, nurodytus temoje [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md). Norėdami atlikti šiuos veiksmus, taip pat turite turėti prieigą prie RCS egzemplioriaus, kuriame yra bent viena būsenos **Baigta** arba **Bendrinama** konfigūracija.

1. Eikite į **Organizacijos administravimas** > **Darbo sritys** > **Elektroninės ataskaitos**. 
2. Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**. Jei nematote šio konfigūracijos teikėjo, atlikite veiksmus, nurodytus temoje [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md). 
3. Jei jūsų įmonėje nėra sukonfigūruotos RKS aplinkos, pasirinkite išorinį saitą **Regulatory Services – Configuration** ir vykdykite instrukcijas, kad sukonfigūruotumėte RCS aplinką. 
4. Pasirinkite **Elektroninių ataskaitų parametrai**. 
5. Pasirinkite skirtuką **RCS**. 
6. Jei RCS aplinka jūsų įmonėje jau sukonfigūruota, norėdami ją pasiekti naudokite puslapyje pateiktus URL. 
7. Uždarykite puslapį. 

## <a name="register-a-new-er-repository"></a>Užregistruokite naują ER saugyklą. 
1. Sąraše pažymėkite pasirinktą eilutę. 
2. Pasirinkite teikėją „Litware, Inc.“. 
3. Pasirinkite Saugyklos. 
4. Pasirinkite Įtraukti ir atidarykite išplečiamąjį dialogo langą. 
5. Lauke Konfigūracijų saugyklos tipas įveskite „RCS“. 
6. Pasirinkite Kurti saugyklą. 
7. Lauke RCS aplinkos rodomas pavadinimas įveskite arba pasirinkite reikšmę. 
8. Pasirinkite norimą RCS egzempliorių. Galite turėti kelis iš jų. 
9. Pasirinkite Gerai. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>ER konfigūracijų importavimas iš RCS saugyklos
1. Pasirinkite **Rodyti filtrus**. 
2. Įveskite filtro reikšmę „RCS“ lauke **Pavadinimas** naudodami filtro operatorių **prasideda**. 
3. Atidarę pažymėtą saugyklą, puslapyje **Prijungimas prie „Regulatory Configuration Services“** pasirinkite saitą **Pasirinkite čia norėdami prijungti prie „Regulatory Configuration Services“**. 
4. Pasirinkite **Atidaryti**. 
5. Pasirinkite **Uždaryti**. 
6. Pasirinkite norimą ER konfigūracijos versiją ir pasirinkite **Importuoti**, kad importuotumėte ją į dabartinį egzempliorių.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
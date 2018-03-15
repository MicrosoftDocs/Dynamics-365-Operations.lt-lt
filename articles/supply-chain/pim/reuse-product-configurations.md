---
title: "Pakartotinai naudoti produkto konfigūracijas"
description: "Galite nurodyti, kad produkto konfigūracija būtų pakartotinai naudojama automatiškai. Tada, kai vartotojas baigia konfigūravimo seansą, sistema patikrina, ar konfigūracija, kuris atitinka vartotojo pasirinkimus, jau yra. Jei sutampanti konfigūracija rasta, pakartotinai naudojami konfigūracijos ID, atitinkama komplektavimo specifikacija (KS) ir maršrutas."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: c447440c33c1f80c6056974086b90d3b43e8499e
ms.contentlocale: lt-lt
ms.lasthandoff: 02/07/2018

---

# <a name="reuse-product-configurations"></a>Pakartotinai naudoti produkto konfigūracijas

[!include[banner](../includes/banner.md)]


Galite nurodyti, kad produkto konfigūracija būtų pakartotinai naudojama automatiškai. Tada, kai vartotojas baigia konfigūravimo seansą, sistema patikrina, ar konfigūracija, kuris atitinka vartotojo pasirinkimus, jau yra. Jei sutampanti konfigūracija rasta, pakartotinai naudojami konfigūracijos ID, atitinkama komplektavimo specifikacija (KS) ir maršrutas.

<a name="requirements-for-reusing-configurations"></a>Pakartotinio konfigūracijų naudojimo reikalavimai
---------------------------------------

Norėdami įjungti pakartotinio konfigūracijų naudojimo funkciją, turite nurodyti toliau pateiktą komponentų ir atributų informaciją puslapyje **Produkto konfigūracijos modelio informacija**.

-   **Komponentai ir subkomponentai** – „FastTab“ **Bendra** lauke **Pakartotinai naudoti konfigūracijas** pasirinkite **Taip**.
-   **Atributai** – „FastTab“ **Atributai** pasirinkite parinktį **Įtraukti į pakartotinį naudojimą**. Ši pasirinktis rodoma tik kai įjungta susijusio komponento pakartotinio naudojimo funkcija. Jei nepasirinksite jokių komponentų, kuriuos norėtumėte naudoti pakartotinai, konfigūracija visada naudojama pakartotinai, nepriklausomai nuo to, ką vartotojas pasirenka konfigūravimo seanso metu. Esamos konfigūracijos atributo reikšmės turi atitikti vartotojo pasirinkimus. Pavyzdžiui, jei konfigūracijos seanso metu vartotojas kaip spalvą pasirenka parinktį **Mėlyna**, sistema patikrina, ar dabartinėje komponento konfigūracijoje yra mėlyna spalva.

## <a name="resetting-configuration-reuse"></a>Pakartotinio konfigūracijos naudojimo nustatymas iš naujo
Kai iš naujo nustatote pakartotinio konfigūracijos naudojimo funkciją, anksčiau sukurtos konfigūracijos nebenaudojamos. Galite iš naujo nustatyti pakartotinio konfigūracijos naudojimo funkciją, jei buvo pakeistas maršrutas arba KS, bet atributai pakeisti nebuvo. Pakartotinio konfigūracijos naudojimo funkcija nustatoma komponento „FastTab“ **Bendra**.





---
title: "Tiekėjo portalo vartotojo saugą"
description: "Šiame straipsnyje paaiškinama, kaip nustatyti išorinių tiekėjų, kurie naudoja Tiekėjo portalą, saugą. Ši informacija taikoma tik iki 2016 m. vasario &amp;Dynamics AX &quot;gegužės 2016&quot; versijos."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 3a5c6a256f8330ba238ea3c0c25f14b10a9a58e6
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-portal-user-security"></a>Tiekėjo portalo vartotojo saugą

Šiame straipsnyje paaiškinama, kaip nustatyti išorinių tiekėjų, kurie naudoja Tiekėjo portalą, saugą. Ši informacija taikoma tik iki 2016 m. vasario &amp;Dynamics AX "gegužės 2016" versijos.

Tiekėjo portalo funkcionalumą pakeitė ilgą tiekėjo intoms bendradarbiavimo funkcinėms galimybėms Dynamics 365 operacijų versija 1611. Daugiau informacijos apie saugos tiekėjo bendradarbiavimo nustatymą, peržiūrėkite [nustatyti įsteigimas ir tiekėjo bendradarbiavimo](set-up-maintain-vendor-collaboration.md). Tiekėjo portale išoriniams tiekėjams pateikiamas ribotas informacijos apie pirkimo užsakymus (PU) kiekis. Svarbu tinkamai nustatyti Tiekėjo portalo vartotojų teises programoje „Microsoft Dynamics AX“, kad tiekėjai neturėtų nenumatytų prieigos prie papildomos informacijos teisių jūsų „Dynamics AX“ sistemoje. **Svarbu:** skirtingai nuo kitų vartotojų, išoriniams tiekėjams neturėtų būti priskiriamas vaidmuo **Sistemos vartotojas**. Vaidmuo **Sistemos vartotojas** suteikia prieigą prie tam tikrų teisių, kurios nėra skirtos išoriniams vartotojams.

## <a name="setting-up-a-vendor-portal-user"></a>Tiekėjo portalo vartotojo nustatymas
Prieš kurdami asmens, kuris naudos tiekėjo portalą, vartotojo paskyrą, turite leisti tiekėjui leisti bendradarbiauti naudojant tiekėjo portalą. Naudokite puslapio **Tiekėjai** skirtuko **Bendra** lauką **Pirkimo užsakymo bendradarbiavimas**. Toliau pateikiama tiekėjo portalą naudojančių išorinių tiekėjų sąranka.

-   Turi būti užregistruota tiekėjo „Microsoft Azure Active Directory“ (AAD) vartotojo paskyra „Dynamics AX“ puslapyje **Vartotojai**.
-   Tiekėjo saugos vaidmuo turi būti **Tiekėjas (išorinis)**, o ne **Sistemos vartotojas **. **Pastaba:** vaidmuo **Sistemos vartotojas** yra suteikiamas automatiškai, kai „Dynamics AX“ sukuriate naują vartotojo paskyrą. Todėl turite pašalinti šį vaidmenį ir patvirtinti įspėjimo pranešimą, kurį gausite.
-   Su tiekėju susijęs vartotojas neturėtų gauti teisės įtraukti papildomų laukų iš PU lentelių į savo PU rodinį. Skirtuke **Personalizavimas**, kuris yra skirtuke **Vartotojai**, nustatykite parinkties **Leidžiamas tiesioginis personalizavimas** reikšmę kaip **Ne**.
-   Vartotojo paskyra turi būti susieta su užregistruotu kontaktiniu asmenimi. Puslapyje **Vartotojai** pasirinkite kontaktinį asmenį lauke **Vardas**. Atitinkamo tiekėjo pasirinkto asmens vaidmuo turi būti **Kontaktas**.

Jei asmeniui reikia suteikti tiekėjo portalo prieigą prie kelių tiekėjų paskyrų (pvz., skirtingų juridinių subjektų), visos to asmens vartotojo paskyros turi būti susietos su tuo pačiu užregistruotu kontaktiniu asmenimi. Vaidmuo **Tiekėjas (išorinis)** apima visas pagrindines galimybes, kurių reikia norint naudoti tiekėjo portale pateikiamas funkcijas. Ši sąranka padeda užtikrinti, kad vartotojo sąsaja, kurią išorinis vartotojas mato, atitiktų tik numatomą scenarijų.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Vendor collaboration](collaborate-vendors-vendor-portal.md)



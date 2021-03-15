---
title: Tiekėjo portalo vartotojų sauga
description: Šiame straipsnyje paaiškinama, kaip nustatyti išorinių tiekėjų, kurie naudoja Tiekėjo portalą, saugą. Ši informacija taikoma tik 2016 m. vasario mėn. ir 2016 m. &amp; gegužės mėn. „Dynamics AX“ versijoms.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1be210728a6d5fa9a26daf9f13865ff08de03d2d
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018192"
---
# <a name="vendor-portal-user-security"></a>Tiekėjo portalo vartotojų sauga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti išorinių tiekėjų, kurie naudoja Tiekėjo portalą, saugą. Ši informacija taikoma tik 2016 m. vasario mėn. ir 2016 m. &amp; gegužės mėn. „Dynamics AX“ versijoms.

Tiekėjo portalo funkcija buvo pakeistą išplėstine tiekėjo bendradarbiavimo funkcija 1611 „Dynamics 365 for Operations“ versija. Daugiau informacijos apie tiekėjo bendradarbiavimo saugos nustatymą [Tiekėjo bendradarbiavimo saugos nustatymas ir tvarkymas](set-up-maintain-vendor-collaboration.md). Tiekėjo portale išoriniams tiekėjams pateikiamas ribotas informacijos apie pirkimo užsakymus (PU) kiekis. Svarbu tinkamai nustatyti Tiekėjo portalo vartotojų teises programoje „Microsoft Dynamics AX“, kad tiekėjai neturėtų nenumatytų prieigos prie papildomos informacijos teisių jūsų „Dynamics AX“ sistemoje. **Svarbu:** skirtingai nuo kitų vartotojų, išoriniams tiekėjams neturėtų būti priskiriamas vaidmuo **Sistemos vartotojas**. Vaidmuo **Sistemos vartotojas** suteikia prieigą prie tam tikrų teisių, kurios nėra skirtos išoriniams vartotojams.

## <a name="setting-up-a-vendor-portal-user"></a>Tiekėjo portalo vartotojo nustatymas
Prieš kurdami asmens, kuris naudos tiekėjo portalą, vartotojo paskyrą, turite leisti tiekėjui leisti bendradarbiauti naudojant tiekėjo portalą. Naudokite puslapio **Tiekėjai** skirtuko **Bendra** lauką **Pirkimo užsakymo bendradarbiavimas**. Toliau pateikiama tiekėjo portalą naudojančių išorinių tiekėjų sąranka.

-   Turi būti užregistruota tiekėjo „Microsoft Azure Active Directory“ (AAD) vartotojo paskyra „Dynamics AX“ puslapyje **Vartotojai**.
-   Tiekėjo saugos vaidmuo turi būti **Tiekėjas (išorinis)**, o ne **Sistemos vartotojas**. **Pastaba**: vaidmuo **Sistemos vartotojas** yra suteikiamas automatiškai, kai „Dynamics AX“ sukuriate naują vartotojo paskyrą. Todėl turite pašalinti šį vaidmenį ir patvirtinti įspėjimo pranešimą, kurį gausite.
-   Su tiekėju susijęs vartotojas neturėtų gauti teisės įtraukti papildomų laukų iš PU lentelių į savo PU rodinį. Skirtuke **Personalizavimas**, kuris yra skirtuke **Vartotojai**, nustatykite parinkties **Leidžiamas tiesioginis personalizavimas** reikšmę kaip **Ne**.
-   Vartotojo paskyra turi būti susieta su užregistruotu kontaktiniu asmenimi. Puslapyje **Vartotojai** pasirinkite kontaktinį asmenį lauke **Vardas**. Atitinkamo tiekėjo pasirinkto asmens vaidmuo turi būti **Kontaktas**.

Jei asmeniui reikia suteikti tiekėjo portalo prieigą prie kelių tiekėjų paskyrų (pvz., skirtingų juridinių subjektų), visos to asmens vartotojo paskyros turi būti susietos su tuo pačiu užregistruotu kontaktiniu asmenimi. Vaidmuo **Tiekėjas (išorinis)** apima visas pagrindines galimybes, kurių reikia norint naudoti tiekėjo portale pateikiamas funkcijas. Ši sąranka padeda užtikrinti, kad vartotojo sąsaja, kurią išorinis vartotojas mato, atitiktų tik numatomą scenarijų.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Bendradarbiavimas su tiekėjais naudojant tiekėjo portalą](collaborate-vendors-vendor-portal.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
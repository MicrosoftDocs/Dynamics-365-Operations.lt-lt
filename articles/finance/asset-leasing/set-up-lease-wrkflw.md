---
title: Nuomos patvirtinimo darbo eigų nustatymas
description: Temoje paaiškinama, kaip nustatyti patvirtinimo darbo eigą, kuri bus vykdoma sukūrus naują nuomos sutartį.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f7781fcb643d678fed528af947efb01911899f54
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724619"
---
# <a name="set-up-lease-approval-workflows"></a>Nuomos patvirtinimo darbo eigų nustatymas

[!include [banner](../includes/banner.md)]

Temoje paaiškinama, kaip nustatyti patvirtinimo darbo eigą, kuri bus vykdoma sukūrus naują nuomos sutartį. Informacijos apie tai, kaip naudoti darbo eigą, ieškokite [Nuomos tvirtinimo darbo eigų naudojimas](use-create-lease-wrkflw.md). 

1. Eikite į **Turto nuoma \> Sąranka \> Nuomos darbo eiga**.
2. Puslapyje **Nuomos darbo eiga** pasirinkite **Nauja**.
3. Pasirodžiusiame dialogo lange, srityje **Darbo eigos tipas** pasirinkite saitą **Nuomos darbo eiga**.

    Programa atidaroma. Ją paleidus, prisijunkite prie „Azure Active Directory“ („Azure AD“), kad nukreiptų į darbo eigos programą.

4. Nuvilkite elementą **Nuomos darbo eigos patvirtinimo** ant darbo eigos.
5. Sujungti vieną mazgą iš **Pradžia** į **Nuomos darbo eigos patvirtinimas**. Tada norėdami **baigti** prijunkite **nuomos darbo eigos patvirtinimą**.
6. Du kartus spustelėkite **Nuomos darbo eigos patvirtinimas**.
7. Pasirinkite **Ypatybės**, tada dalyje **Pagrindiniai parametrai** įveskite darbo eigos pavadinimą.

    Šiame puslapyje taip pat galite nustatyti daugiau darbo eigos parametrų. Jei įjungėte **automatinius veiksmus**, sistema automatiškai imsis konkretaus veiksmo. Pranešimus galima siųsti, jei jie nurodyti skirtuke **Pranešimai**. Skirtuke **Išplėstiniai parametrai** galite nurodyti galutinį tvirtintoją, nustatyti laiko limitą ir nurodyti konkrečius veiksmus, kuriuos reikia atlikti.

8. Kai baigsite nustatyti darbo eigos parametrus, pasirinkite **Uždaryti**.
9. Pasirinkite **1 veiksmas**, tada – **Ypatybės**.
10. Dalyje **Pagrindiniai parametrai** įveskite veiksmo pavadinimą, sukurkite patvirtinimo temos eilutę ir nurodykite patvirtinimo instrukcijas.
11. Puslapyje **Priskyrimas** pasirinkite priskyrimo tipą.
12. Norėdami patvirtinti tam tikrus vartotojus, pasirinkite **Vartotojas**, pasirinkite vartotojus, kurie patvirtina nuomą, ir pasirinkite **Uždaryti**.
13. Pasirinkite **Įrašyti ir uždaryti**, kad sukurtumėte darbo eigą. Tada, kai būsite raginami, pasirinkite **Gerai**.
14. Puslapyje **Darbo eigos kūrimas** pasirinkite **Uždaryti**.
14. Pasirinkite naują darbo eigą ir pasirinkite **Versijos**. Tada pasirinkite **Suaktyvinti**, kad įsitikintumėte, jog darbo eiga yra aktyvi.
15. Pasirinkite **Uždaryti**. Rodoma nauja aktyvi versija.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

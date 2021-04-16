---
title: „Azure Active Directory” EKA prisijungimo autentifikavimo įjungimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti „Microsoft Dynamics 365 Commerce” elektroninio kasos aparato (EKA) prisijungimo funkcijas, kad būtų naudojamas „Azure Active Directory” autentifikavimas.
author: boycezhu
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 50088aee8c2474708682c9041251d2336e84d971
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796347"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>EKA prisijungimo „Azure Active Directory“ autentifikavimo įjungimas
[!include [banner](includes/banner.md)]


Daug klientų, kurie naudoja „Microsoft Dynamics 365 Commerce”, taip pat naudoja kitas „Microsoft” debesies tarnybas ir jie gali naudoti „Azure Active Directory” („Azure AD”) šioms tarnyboms valdyti vartotojo kredencialus. Tokiais atvejais klientai gali norėti naudoti tą pačią „Azure AD” paskyrą keliose programose. Šioje temoje paaiškinama, kaip sukonfigūruoti „Commerce” elektroninio kasos aparato (EKA) prisijungimo funkcijas, kad būtų naudojamas „Azure AD” autentifikavimas.

## <a name="configure-azure-ad-authentication"></a>„Azure AD” autentifikavimo konfigūravimas

Norėdami, kad „Azure AD” būtų pasiekiama kaip EKA prisijungimo prie parduotuvės autentifikavimo metodas, turite sukonfigūruoti parduotuvės funkcijų šablono parametrus ir tada taikyti šiuos parametrus EKA klientams.

Norėdami sukonfigūruoti funkcijų šabloną, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalo sąranka** \> **EKA sąranka** \> **EKA profiliai** \> **Funkcionalumo profiliai**.
1. Pasirinkite funkcijų šabloną, kurį norite pakeisti.
1. „FastTab” **Funkcijos**, skyriuje **EKA darbuotojų prisijungimas**, pakeiskite lauko **Prisijungimo autentifikavimo būdas** vertę iš **Darbuotojo ID ir slaptažodis** į **„Azure Active Directory”**.

Pagal numatytuosius parametrus visi funkcijų šablonai naudoja **Darbuotojo ID ir slaptažodis** kaip EKA autentifikavimo metodą. Todėl, jei norite naudoti „Azure AD”, turite pakeisti lauko **Prisijungimo autentifikavimo metodas** vertę. Atlikus šį pakeitimą bus paveiktos visos mažmeninės prekybos parduotuvės, kurios yra susijusios su pasirinktu funkcijų šablonu.

Norėdami taikyti parametrus EKA klientams, atlikite toliau pateikiamus veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba** \> **Mažmeninės prekybos ir prekybos IT“** \> **Paskirstymo grafikas**.
1. Paleiskite paskirstymo grafiką **1070** (**Kanalo konfigūracija**).

> [!NOTE]
> „Azure AD” autentifikavimui reikia interneto ryšio. Jis neveiks, kai EKA veikia atjungties režimu.
> 
> Šiuo metu **valdytojo nepaisymo** funkcija nepalaiko „Azure AD“ kaip autentifikavimo būdo. Operatoriaus ID ir slaptažodis yra privalomi, net jei jie „Azure AD“ sukonfigūruoti kaip EKA prisijungimo autentifikavimo metodas.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>„Azure AD” paskyros susiejimas su darbininku

Prieš tai, kai parduotuvės darbininkas gali naudoti „Azure AD” paskyrą, kad prisijungtų prie EKA programos, „Azure AD” paskyra turi būti susieta su tuo darbininku.

Norėdami susieti „Azure AD” paskyrą su darbininku, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba** \> **Darbuotojai** \> **Darbininkai**.
1. Atidarykite darbininko informacijos puslapį.
1. Veiksmų srities skirtuko **Prekyba** grupėje **Išorinė tapatybė** pasirinkite **Susieti esamą tapatybę**.
1. Dialogo lange **Naudoti esamą išorinę tapatybę** pasirinkite **Ieškoti pagal el. paštą**, įveskite „Azure AD” el. pašto adresą ir pasirinkite **Ieškoti**.
1. Pasirinkite gautą „Azure AD” paskyrą ir pasirinkite **Gerai**.

Darbininko informacijos puslapio laukai **Pseudonimas**, **UPN**, **Išorinis antrinis identifikatorius**, esančius skirtuke **Prekyba**, bus automatiškai užpildomi.

> [!NOTE]
> Po darbuotojo įrašo įkėlimo, jei pavyzdžiui, nauja „Azure AD“ paskyra yra susieta, slaptažodis yra pakeičiamas arba atnaujinama darbuotojo adresų knyga, jums rekomenduojama vykdyti **1060** (**Personalo**) paskirstymo grafiką tam, kad būtų sinchronizuota naujausia informaciją į kanalą. Tokiu būdu, POS programa gali gauti tikslius duomenis vartotojo autentifikavimui ir autorizavimo patikrai.

## <a name="additional-resources"></a>Papildomi ištekliai

[MPOS ir „Cloud POS“ išplėstinės registracijos funkcijų nustatymas](extended-logon.md)

[Mažmeninės prekybos funkcijų šablono kūrimas](retail-functionality-profile.md)

[ Konfigūruoti darbininką](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
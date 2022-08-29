---
title: Konfigūruoti CPOS, kad būtų galima naudoti pasirinktinę Azure AD programą
description: Šiame straipsnyje paaiškinama, kaip sukonfigūruoti "Cloud POS" (CPOS), kad būtų galima naudoti pasirinktinę Azure Active Directory (Azure AD) programą.
author: boycez
ms.date: 08/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: baa0c3da25308345037b5dd1b4c5907d6213e7f7
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/03/2022
ms.locfileid: "9223822"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>Konfigūruoti CPOS, kad būtų galima naudoti pasirinktinę Azure AD programą

[!include [banner](includes/banner.md)]

Pagal numatytuosius nustatymus, debesies EKA (CPOS) Microsoft Dynamics 365 Commerce taškai į užregistruotą pirmojo šalies "Microsoft" programą Azure Active Directory (Azure AD). Dėl to galite naudoti CPOS neateidami jokių pakeitimų Azure AD. Tačiau jūs galite norėti nurodyti savo CPOS egzempliorių, kad tai būtų jūsų kontroliuojama Azure AD pasirinktinė programa. Šiame straipsnyje paaiškinama, kaip konfigūruoti CPOS, kad būtų galima naudoti pasirinktinę Azure AD programą.

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Nustatyti pasirinktinę "Retail Server" programą Azure AD

Norėdami sukurti ir konfigūruoti pasirinktinę "Retail Server" programą, atlikite Azure AD šiuos veiksmus.

1. Prisiregistruokite administravimo [Azure Active Directory centre](https://aad.portal.azure.com) naudodami bet kokį vartotojo Azure AD abonementą. Vartotojo abonementui nereikia turėti administratoriaus teisių.
1. Pasirinkti  **Azure Active Directory**.
1. Pasirinkite **Programos registracijos**, tada pasirinkite Nauja **registracija, kad** atidarytumėte **programos dialogo** langą Registruoti.
1. Užpildykite toliau nurodytus laukus:

    - **Pavadinimas** – įveskite pasirinktinį programos pavadinimą. Pvz., įveskite pasirinktinį **"Retail Server"**.
    - **Sąskaitų tipų palaikymas** – pasirinkite numatytąją pasirinktį, **Sąskaitas šiame organizacinyje kataloge (tik Microsoft – Vienas nuomininkas)**.
    - **Nukreipimo URI** – šis laukas nėra būtinas. Palikite tuščią.
    - **Aptarnavimo medžio ID** – šis laukas nėra būtinas. Palikite tuščią.
    
1. Pasirinkite **Registruotis**. Pasirodo naujai užregistruotos programos konfigūracijos puslapis.
1. Skyriuje Apžvalga **\> pagrindai pasirinkite** Įtraukti programos **ID URI**, **tada pasirinkite Nustatyti** šalia programos **ID URI**. Pasižymėkite apie siūlomą vertę ir pasirinkite **Įrašyti**, kad priimtumėte tą vertę. 
1. Pasirinkite **Įtraukti aprėptį** ir tada nustatykite šiuos laukus:

    - **Aprėpties** pavadinimas – įveskite pasirinktinį aprėpties pavadinimą. Pvz., įveskite **Legacy.Access.Full**.
    - **Kas gali sutikti** – nurodykite, ar ir administratoriai, ir vartotojai, arba tik administratoriai gali suteikti sutikimą, remdami savo organizacijos saugos strategija.
    - **Administratoriaus sutikimas rodyti** pavadinimą – įveskite rodomą pavadinimą. Pvz., įveskite Prieigą **prie parduotuvės serverio**.
    - **Administratoriaus sutikimo** aprašymas – įveskite aprašą. Pvz., įveskite **Suteikia prieigą prie "Retail Server" API**.

1. Norėdami **užbaigti aprėpties** kūrimo procesą pasirinkite Įtraukti aprėptį.

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Nustatyti pasirinktinę CPOS programą Azure AD

Norėdami sukurti ir konfigūruoti pritaikytą CPOS programą, atlikite Azure AD šiuos veiksmus.

1. Prisiregistruokite administravimo [Azure Active Directory centre](https://aad.portal.azure.com) naudodami bet kokį vartotojo Azure AD abonementą. Vartotojo abonementui nereikia turėti administratoriaus teisių.
1. Pasirinkti  **Azure Active Directory**.
1. Pasirinkite **Programos registracijos**, tada pasirinkite Nauja **registracija, kad** atidarytumėte **programos dialogo** langą Registruoti.
1. Užpildykite toliau nurodytus laukus:

    - **Pavadinimas** – įveskite programos pavadinimą. Pavyzdžiui, įveskite pasirinktinį **debesies EKA**.
    - **Sąskaitų tipų palaikymas** – pasirinkite numatytąją pasirinktį, **Sąskaitas šiame organizacinyje kataloge (tik Microsoft – Vienas nuomininkas)**.
    - **Nukreipimo URI** – **išplečiamajame sąraše pasirinkite vieno puslapio programą (SPA)** ir įveskite savo CPOS URI.
    - **Aptarnavimo medžio ID** – šis laukas nėra būtinas. Palikite tuščią.

1. Pasirinkite **Registruotis**. Pasirodo naujai užregistruotos programos konfigūracijos puslapis.
1. Deklaracijos skyriuje **nustatykite** **oauth2AllowIdTokenImplicitFlow** **ir oauth2AllowImplipliFlow** **parametrus kaip teisingas**, tada pasirinkite **Įrašyti.**
1. Atpažinimo ženklo **konfigūracijos skyriuje,** norėdami įtraukti dvi pretenzijas, atlikite šiuos veiksmus:

    - Pasirinkite Įtraukti **papildomą paraišką**. Nustatykite **atpažinimo ženklo** tipo lauką **kaip ID**, tada pasirinkite "sid" **paraišką**. Pasirinkite **Įtraukti**.
    - Pasirinkite Įtraukti **papildomą paraišką**. Nustatykite **atpažinimo ženklo tipo** lauką **Prieiga**, tada pasirinkite "sid" **paraišką**. Pasirinkite **Įtraukti**.

1. **API teisių skyriuje** pasirinkite Įtraukti **teisę**.
1. Skirtuke **API, kurį naudoja** mano organizacija, ieškokite "Retail Server [" programos, kurią sukūrėte skyriuje Nustatyti pasirinktinę "Retail Server" programą Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad). Tada pasirinkite **Įtraukti teises**.
1. **Peržiūros skyriuje**, programos (kliento) ID **lauke** pasižymkite vertę.

## <a name="update-the-cpos-configuration-file"></a>Atnaujinti CPOS konfigūracijos failą

Atidarykite CPOS config.json failą ir jame atlikite šiuos atnaujinimus.

1. **Pakeisti AADClientId** **rakto vertę pasirinktinės CPOS programos, kurią sukūrėte skyriuje Nustatyti pasirinktinę CPOS**[programą, programos (kliento) ID Azure AD](#set-up-a-custom-cpos-app-in-azure-ad) verte.
1. **Pakeiskite AADRetailServerResourceId** **rakto reikšmę programos ID URI reikšme** pasirinktinės "Retail Server [" programos, kurią sukūrėte skyriuje Nustatyti pasirinktinę "Retail Server Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad)" programą.

CPOS siųs užklausas saugos atpažinimo ženklui Azure AD gauti, naudos abu parametrus.

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Naujinti tapatybės teikėjų parametrus "Commerce Headquarters"

Tada turite atnaujinti tapatybės teikėjų parametrus "Commerce Headquarters".

1. "Commerce Headquarters" atidarykite bendrai naudojamų **"Commerce" parametrų** puslapį.
1. Skirtuko Tapatybės **teikėjai skyriuje** **Tapatybės** teikėjai pasirinkite eilutę, **·** **Azure Active Directory** **kurioje** laukas Tipas nustatytas ir laukas Išdavėjas nurodo jūsų nuomininką.Azure AD Šis parametras patvirtina, kad jūs dirbsite su antriniais tinkleliais, kuriuose yra duomenys, susiję su jūsų nuomininką atitinkančiu tapatybės Azure AD teikėju.
1. Skyriuje **Priklausančios šalys** pasirinkite **Įtraukti**, kad įtrauktumėte eilutę.
1. Užpildykite toliau nurodytus laukus:

    - **ClientId** – įveskite pasirinktinės **CPOS** programos (kliento) ID [vertę, kurią sukūrėte skyriuje nustatyti pasirinktinę CPOS programą Azure AD](#set-up-a-custom-cpos-app-in-azure-ad).
    - **Tipas** – pasirinkti **viešąjį**.
    - **UserType** – pasirinkite **darbuotoją**.

1. Pasirinkite pridėtą eilutę. Skyriuje **Serverio išteklių ID** pateikiamame po skyriumi **Priklausančios šalys** rodomi programos „Retail Server“ ID, kuriuos galima pasiekti naudojant programą, kurią pasirinkote tinklelyje **Priklausančios šalys**.
1. Skyriuje Serverio **išteklių ID pasirinkite** Įtraukti, **kad** įtraukumėte eilutę.
1. Lauke Serverio **išteklių ID įveskite** pasirinktinės "Retail Server **" programos, kurią sukūrėte skyriuje Nustatyti pasirinktinę "Retail Server**" programą, [programos ID URI Azure AD](#set-up-a-custom-retail-server-app-in-azure-ad) reikšmę.

    > [!IMPORTANT]
    > Visuose laukuose, kurie yra nurodyti ankstesniuose žingsniuose, abc nuo abc. Reikšmės, kurias įvedate, turi tiksliai atitikti vertes, kurios sukonfigūruotos administravimo Azure AD centre.

1. Pereikite į " **Retail" ir "Commerce IT \> Distribution"** grafiką ir paleiskite **užduotį 1110** (**visuotinis** konfigūravimas).

Dabar galite aktyvinti CPOS įrenginius naudodami savo Azure AD programą.

## <a name="additional-resources"></a>Papildomi ištekliai

[Point of sale (EKA) įrenginio aktyvinimas](dev-itpro/retail-device-activation.md)

[Sąskaitų aktyvinimo ir įrenginių tikrinimo valdymas](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Konfigūruoti „Azure Active Directory“ autentifikavimą POS prisijungimui
description: Šioje temoje paaiškinama, kaip konfigūruoti „Azure Active Directory“ kaip autentifikavimo metodą „Microsoft Dynamics 365 Commerce“ prekybos taškui.
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 63121a9b5f1b062b7ca927f6b9eb1689ce8aa698
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270688"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>Konfigūruoti „Azure Active Directory“ autentifikavimą POS prisijungimui

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip konfigūruoti „Azure Active Directory“ („Azure AD“) kaip autentifikavimo metodą „Microsoft Dynamics 365 Commerce“ prekybos taškui (POS).

Mažmenininkai, kurie naudoja kartu su kitomis „Microsoft" debesies „Dynamics 365 Commerce“ paslaugomis, pvz., „Microsoft Azure“ „Microsoft 365", ir paprastai nori naudoti centralizuoto vartotojo kredencialų valdymo, kad būtų galima saugiai ir sklandžiai prisijungti „Microsoft Teams“ visose „Azure AD“ programose. Norėdami naudoti „Azure AD“ „Commerce POS" autentifikavimą, pirmiausia turite „Azure AD“ „Commerce Headquarters" sukonfigūruoti kaip autentifikavimo metodą.

## <a name="configure-pos-authentication-method"></a>Konfigūruoti POS autentifikavimo metodą

Norėdami konfigūruoti laiko vietos funkciją „Commerce“ štabe, atlikite šiuos žingsnius.
    
1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> EKA sąranka \> EKA profiliai \> Funkcijų profiliai** ir pasirinkite keičiamą funkcijų profilį.
1. EKA darbuotojų registravimosi skyriuje Funkcijų „FastTab" pasirinkite norimą autentifikavimo metodo pasirinktį iš išplečiamojo **sąrašo** **Registravimosi** **autentifikavimo** metodas.

    **Registravimosi autentifikavimo** metodas turi tris pasirinktis:
    
    - **Personalo ID ir slaptažodis – pasirinkus šią numatytąją parinktį EKA vartotojai turi įvesti personalo ID ir slaptažodį, kad prisiregistruotų prie EKA ir prieiti prie vadovo** nepaisymo funkcijų.
    - **„Azure AD“ be vieno prisijungimo – naudojant šią parinktį EKA vartotojai turi naudoti kredencialus prisijungdami prie EKA ir prieigos** „Azure AD“ vadovo nepaisymo funkcijų. Kai EKA klientas atnaujinamas arba pakartotinai atidaromas, EKA vartotojas turi pateikti „Azure AD“ kredencialus, kad vėl prisiregistruotų.
    - **„Azure AD“su vienu prisiregistru – kai ši pasirinktis pasirinkta, EKA vartotojai gali prisiregistruoti prie "Cloud POS" (CPOS) naudodami aktyvius kredencialus, kuriuos naudoja kitos žiniatinklio programos toje pačioje žiniatinklio naršyklėje arba prisiregistruoja prie** „Modernus EKA" (MPOS), naudodami kredencialus, prisijungusius „Azure AD“, „Azure AD“ prie „Windows". Abu metodai leidžia prisijungti neįrašant „Azure AD“ kredencialų EKA prisijungimo ekrane. Tačiau, jei norite pasiekti EKA tvarkytuvo nepaisoma funkcijų, vis tiek reikės prisijungti naudojant „Azure AD“ kredencialus.

1. Pereikite į Mažmeninę prekybą ir komerciją > Mažmeninės prekybos ir komercijos IT > paskirstymo grafiką ir paleiskite **1070** (kanalo konfigūracija) užduotį, norėdami sinchronizuoti naujausius funkcijų šablono parametrus **EKA** klientams.

> [!NOTE]
> - Parinktis **„Azure AD“ Be vieno** prisiregistravimo autentifikavimo metodo pakeičia pasirinktį **„Azure Active Directory** „Commerce" versijoje 10.0.18 ir ankstesnėje versijoje.
> - „Azure AD“ autentifikuoti reikalingas aktyvus interneto ryšys ir jis negali veikti, kai EKA ne tinkle.

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Abonementų „Azure AD“ susiejimas su EKA vartotojais

Norėdami naudoti „Azure AD“ kaip EKA autentifikavimo metodą turite susieti sąskaitas su „Azure AD“ „Commerce Headquarters" vartotojais. 

Norėdami susieti „Azure AD“ sąskaitas su EKA vartotojais „Commerce Headquarters", atlikite šiuos veiksmus.
    
1. Eikite **į „Retail" ir "Commerce" > Darbuotojai** > Darbuotojai ir atidarykite darbuotojo įrašą.
1. Veiksmų srities skirtuko **Prekyba** grupėje rinkitės **Išorinė tapatybė** tada pasirinkite **Susieti esamą tapatybę**. 
1. Dialogo lange **Naudoti esamą išorinę tapatybę** pasirinkite **Ieškoti pagal el. paštą**, įveskite „Azure AD” el. pašto adresą ir pasirinkite **Ieškoti**.
1. Pasirinkite gautą „Azure AD” paskyrą ir pasirinkite **Gerai**.

Po konfigūravimo veiksmų prieš tai, **Pseudonimas**, **UPN**, **Išorinis antrinis identifikatorius**, esančius skirtuke **Prekyba**, bus automatiškai užpildomi.

Norėdami sinchronizuoti naujausius EKA vartotojo ir sąskaitos duomenis su kanalu, turite vykdyti užduotį 1060 (Darbuotojai) dalyje Mažmeninė prekyba ir Prekyba > Mažmeninė prekyba ir Prekyba **IT** > **Paskirstymo** „Azure AD“ grafikas.

> [!NOTE]
> Geriausiai po darbuotojo informacijos, pvz., slaptažodžio, EKA teisių, susietos sąskaitos arba darbuotojų adresų knygelės, atnaujinus „Azure AD“ „Commerce Headquarters", rekomenduojame paleisti **1060 (darbuotojų) užduotį, kad būtų galima sinchronizuoti naujausią darbuotojo informaciją su** kanalu. Tokiu būdu, EKA klientas gali gauti tikslius duomenis vartotojo autentifikavimui ir autorizavimo patikroms.

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>EKA užrakto registras ir atjungimas autentifikuoti „Azure AD“

Kai EKA sukonfigūruotas naudoti autentifikavimo „Azure AD“ metodą, atsiranda:

- **EKA programoje nebus galima** užrakto registro funkcija. 
- Automatiškai **užrakinimo** funkcija veiks taip pat, kaip ir automatiškai **atsijungimo** funkcija.
- Jei EKA vartotojas pasirenka išsiregistruoti, vartotojas bus paprašytas prisijungti kredencialais, kitą kartą paleidus EKA, neatsižvelgiant į tai, ar įgalintas **vienas** „Azure AD“ prisijungimas.

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Vadovo nepaisoma funkcijų autentifikuoti „Azure AD“

Kai EKA yra sukonfigūruotas naudoti autentifikavimą, vadybininkas perrašo funkcijas ir atidaro dialogo langą, kuriame raginamas įvesti vadybininko „Azure AD“ vartotojo „Azure AD“ kredencialus. Patvirtinus vadovo prisijungimą, vadybininko kredencialai bus atmesti, o ankstesni vartotojo kredencialai bus naudojami „Azure AD“, „Azure AD“ vėlesnioms EKA operacijoms.

> [!NOTE]
> - Naudojant „Commerce" 10.0.18 ir ankstesnes versijas vadovo nepaisymo funkcija „Azure AD“ nepalaikoma. Darbuotojų ID ir slaptažodis yra privalomi, net jei „Azure AD“ sukonfigūruoti kaip EKA prisijungimo autentifikavimo metodas.
> - Kai naudojate CPOS su Automatiškai iOS įrenginio interneto naršykle, norėdami dirbti su autentifikavimu, pirmiausia turite išjungti „Blokuoti iššokančius langus" parametruose tvarkytuvo **nepaisymo** „Azure AD“ funkciją. 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>Bendrinamų įrenginių „Azure AD“ šiuo metu pagrįsto EKA autentifikavimo saugos geriausios praktikos

Daugelis mažmenininkų nustato savo parduotuvės aplinką taip, kad keli vartotojai turės prieigą prie EKA naudojant bendrai naudojamą fizinį įrenginį. Šiame kontekste, kai vienkartinis prisijungimas suteikia patogią ir nuoseklią autentifikavimo patirtį, ji taip pat gali sukurti saugos ciklą, kur dabartinis EKA vartotojas gali nepastebti, kad EKA operacijoms ar operacijoms vykdyti naudojami kito vartotojo kredencialai. Prieš konfigūrant EKA naudoti autentifikavimo metodą, rekomenduojame peržiūrėti savo saugos strategiją ir bendrai naudojamo įrenginio prisijungimo parametrus, siekiant nuspręsti, kuri „Azure AD“ parinktis geriausia.

- Jei jūsų mažmeninės prekybos aplinkoje faktiniam įrenginiui prisijungti naudojama bendrai naudojama sąskaita (pvz., vietinė sąskaita), rekomenduojama naudoti parinktį be vieno **„Azure AD“ prisiregistrimo**. Taip užtikrinama, kad kiekvienas EKA vartotojas aiškiai pateikia „Azure AD“ prisijungimo prie EKA kredencialus.
- Jei jūsų mažmeninės prekybos aplinka reikalauja, kad darbuotojai prisijungtų prie EKA ir kad jie nuomotų fizinį įrenginį, rekomenduojame naudoti vieną prisijungimo „Azure AD“, **„Azure AD“ pasirinktį**.

## <a name="additional-resources"></a>Papildomi ištekliai

[ Konfigūruoti darbininką](tasks/worker.md)

[Mažmeninės prekybos funkcijų šablono kūrimas](retail-functionality-profile.md)


[MPOS ir „Cloud POS“ išplėstinės registracijos funkcijų nustatymas](extended-logon.md)

[Bendrinamos aplinkos „Cloud POS“ saugos geriausios praktikos](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

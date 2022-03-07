---
title: Naujų vartotojų kūrimas
description: Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 480d181e8abb3af5a7406efd13c8bd9961a7490a
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595391"
---
# <a name="create-new-users"></a>Naujų vartotojų kūrimas

[!include [banner](../../includes/banner.md)]

Kad galėtumėte pasiekti „Finance and Operations” programas, pirmiausia turite būti pridėti prie **Vartotojai** puslapio (**Sistemos administravimas \> Vartotojai \> Vartotojai**). Vartotojai apima vidinius jūsų organizacijos vidinius darbuotojus arba išorinius klientus ir tiekėjus. Vartotojus galima importuoti arba pridėti neautomatiniu būdu. Visi vartotojai turi turėti tinkamą licenciją atitinkamam naudojimui.

Informaciją apie tai, kaip įsigyti ir licencijuoti „Finance and Operations programoms, rasite [„Microsoft Dynamics 365” licencijavimo vadove](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Licencijos priskyrimas vartotojui
Sistemos administratoriai gali [priskirti licencijas vartotojams](/office365/admin/subscriptions-and-billing/assign-licenses-to-users) [„Microsoft 365” administravimo centre](/office365/admin/admin-overview/about-the-admin-center).

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Išorinio vartotojo pridėjimas „Azure AD” ir licencijos priskyrimas 
Išoriniai vartotojai turi būti atstovaujami jūsų nuomotojo kataloge („Azure Active Directory” („Azure AD”)) tam, kad jiems galėtų būti priskirtos licencijos. Minėtus išorinius vartotojus reikia įtraukti į „Azure AD“ esantį nuomotoją kaip vartotojus svečius ir priskirti jiems atitinkamas licencijas. Reikalavimas „Finance and Operations” programoms yra toks, kad vartotojo svečio įmonė turi naudoti „Azure AD”. Norėdami gauti daugiau informacijos, žr. [„Azure Active Directory“ B2B bendradarbiavimo vartotojų įtraukimas „Azure“ portale](/azure/active-directory/b2b/add-users-administrator).

## <a name="import-new-users-from-azure-ad"></a>Naujų vartotojų importavimas iš „Azure AD“ 
1. Eikite į **Sistemos administravimas** \> **Vartotojas** \> **Vartotojai**.
2. Veiksmų srityje pasirinkite **Importuoti vartotojus**.
3. Pasirinkite importuotinus vartotojus. Sąrašas apima „Azure AD” vartotojus, kurie šiuo metu nėra šios aplinkos vartotojai.
4. Pasirinkite **Importuoti vartotojus**.
5. Pasirinkite **Uždaryti**.

> [!NOTE]
> Lauko **Įmonė** reikšmė bus nustatyta pagal dabartinę administratoriaus seanso įmonę. Po importavimo, turite priskirti vaidmenis ir organizacijas kaip taikomas. Norėdami gauti daugiau informacijos, žr. [Vartotojų priskyrimas saugos vaidmenims](assign-users-security-roles.md). Sąlygiškai gali reikėti susieti vartotoją su **Asmeniu** ir atnaujinti vartotojo pasirinktis, pavyzdžiui, kalbą.

## <a name="manually-add-a-new-user"></a>Naujo vartotojo įtraukimas rankiniu būdu
1. Eikite į **Sistemos administravimas** \> **Vartotojai** \> **Vartotojai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Lauke **Vartotojo ID** įveskite vartotojo unikalųjį identifikatorių (ID).   
4. Lauke **Vartotojo vardas** įveskite vartotojo vardą.  
5. Lauke **Teikėjas**:
 - Vidiniams vartotojams naudokite numatytąją vertę. Pavyzdžiui, jūsų „Azure AD” nuomotoją su priešvardžiu https://sts.windows.net/.  
 - Ne „Azure AD” vartotojams, pavyzdžiui, „Service-2-Service” paskyroms, įveskite pagrindinę teksto vertę. Pavyzdžiui, NA. Ši vertė padės išvengti neteisingų autentifikavimo skambučių, kurie gali sukelti klaidas, jei naudojama tinkama tapatybės tiekėjo vertė.  
 - Išoriniams arba svečiams vartotojams pridėkite „Azure AD” nuomotojo pavadinimą po https://sts.windows.net/.
6. Lauke **El. paštas** įveskite vartotojo visą el. pašto/vartotojo principo pavadinimą.  
7. Lauke **Įmonė** pasirinkite numatytąją vartotojo paleisties įmonę. 
8. Pasirinkite **Įrašyti**.

Tapatybės teikėjo ir telemetrijos ID vertės bus atnaujintos remiantis [„Microsoft” diagramos](/graph/overview) iškvietimu, kai išsaugomas vartotojo įrašas. Telemetrijos ID remiasi vartotojo objekto ID/saugos identifikatoriumi (SID) „Azure AD”.

> [!NOTE]
> Kai įtraukiate vartotoją, privalote priskirti vaidmenis ir organizacijas kaip taikomas. Norėdami gauti daugiau informacijos, žr. [Vartotojų priskyrimas saugos vaidmenims](assign-users-security-roles.md). Sąlygiškai gali reikėti susieti vartotoją su **Asmeniu** ir atnaujinti **Vartotojo pasirinktis**, pavyzdžiui, kalbą.

## <a name="change-a-user-id"></a>Vartotojo ID keitimas
Norėdami pakeisti vartotojo ID, turite pervardyti raktą duomenų bazėje. Kai keičiate vartotojo ID naudodami šią procedūrą, visi susiję vartotojo parametrai yra modifikuojami, kad būtų galima naudoti naują vartotojo ID. Pavyzdžiui, naudojimo informacija lentelėje **„SysLastValue”** yra atnaujinama, kad būtų galima nurodyti naują vartotojo ID.

> [!NOTE]
> Šis vartotojo ID yra vartotojo informacijos lentelės pirminis raktas. Esamų vartotojų pirminio rakto pervardijimas gali šiek tiek užtrukti, nes visos nuorodos į raktą taip pat atnaujinamos duomenų bazėje. 

1. Eikite į **Sistemos administravimas \> Vartotojai \> Vartotojai**.
2. Pasirinkite vartotoją iš sąrašo ir **Pasirinktys\> Įrašo informacija**.
3. Pasirinkite **Pervardyti**.
4. Įveskite naują ir unikalią vartotojo ID reikšmę ir pasirinkite **Gerai**. 
5. Pasirinkite **Taip** patvirtinimui.

## <a name="additional-resources"></a>Papildomi ištekliai

Norėdami gauti daugiau B2B vartotojų įgyvendinimo pasirinkčių, žiūrėkite [B2B vartotojų eksportavimas į „Azure AD”](../implement-b2b.md).

Informaciją apie iš anksto sukonfigūruotas sistemos sąskaitas rasite [Iš anksto sukonfigūruotos sistemos sąskaitos](../pre-configured-system-accounts.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
---
title: Tiekėjo bendradarbiavimo nustatymas ir tvarkymas
description: Šioje temoje paaiškinama, kaip nustatyti tiekėjų bendradarbiavimą Dynamics 365 Supply Chain Management programoje. Taip pat paaiškinama, kaip numatyti naujus tiekėjo bendradarbiavimo vartotojus ir valdyti tų vartotojų saugos vaidmenis.
author: Henrikan
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b635255fffa6fd3c6612cd248dc692df204aa76d
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652050"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>Tiekėjo bendradarbiavimo nustatymas ir tvarkymas

[!include [banner](../includes/banner.md)]

Tiekėjo bendradarbiavimo sąsajoje išorinių tiekėjų vartotojams pateikiamaa ribotas informacijos kiekis apie pirkimo užsakymus, SF ir konsignacijos atsargas. Šioje sąsajoje tiekėjas taip pat gali atsakyti į pasiūlymo užklausas (RFQ) ir peržiūrėti bei redaguoti pagrindinę įmonės informaciją.

Šioje temoje paaiškinama, kaip nustatyti tiekėjų bendradarbiavimą Dynamics 365 Supply Chain Management programoje. Taip pat paaiškinama, kaip nustatyti darbo srautą, kad būtų galima numatyti naujus tiekėjo bendradarbiavimo vartotojus ir kaip valdyti tų vartotojų saugos vaidmenis.

> [!NOTE]
> Informacija apie tiekėjų bendradarbiavimo saugos vaidmenų nustatymą taikoma tik dabartinei Finance and Operations versijai. „Microsoft Dynamics AX 7.0“ (2016 m. vasario mėn.) ir „Microsoft Dynamics AX“ 7.0.1 programos versijoje (2016 m. gegužės mėn.) su tiekėjais galite bendradarbiauti naudodami modulį **Tiekėjo portalas**. Informacijos apie tiekėjo portalo vartotojo teises Microsoft Dynamics AX programoje žr. [Tiekėjo portalo vartotojo sauga](configure-security-vendor-portal-users.md).

## <a name="set-up-vendor-collaboration-security-roles"></a>Tiekėjo bendradarbiavimo saugos vaidmenų nustatymas

Įsigijimo specialistas ar tiekėjas, kuris turi pakankamai teisių, gali prašyti, kad kontaktinis asmuo būtų numatytas kaip vartotojas, kontaktinio asmens įraše įgalinant **Numatytą tiekėjo vartotoją**. Parengimo proceso metu, naujam išoriniam vartotojui parenkamos vartotojo teisės ir pateikiama naujo tiekėjo vartotojo užklausa. Svarbu, teisingai nustatyti vartotojo teises, kurias galima pasirinkti tiekėjo vartotojo užklausoje. Kitu atveju, tiekėjams gali būti suteikta prieiga prie informacijos, prie kurios Supply Chain Management programoje jie prieigos neturėtų turėti.

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>Nustatyti saugos vaidmenis, kuriuos galima pasirinkti, kai kontaktiniam asmeniui naudojama nauja vartotojo užklausa

1. Pasirinkite **Sistemos administravimas** &gt; **Sauga** &gt; **Išoriniai vaidmenys**.
2. Pasirinkite **Naujas**, tada pasirinkite saugos vaidmenį ir **Ttiekėjo** šalies vaidmenį.

Galbūt norėsite įtraukti **Tiekėjų administratoriaus (išorinius)** ir **Tiekėjo (išorinius)** vaidmenis, kurie pateikiami Supply Chain Management programoje. Taip pat galite naudoti saugos vaidmenis, kuriuos sukūrė jūsų įmonė.

Turėtumėte padaryti **Tiekėjo administratoriaus (išorinį)** vaidmenį prieinamą tik tuo atveju, jei tiekėjai turėtų galimybę kurti naujus kontaktus, pateikti tiekėjų bendradarbiavimo vartotojo užklausas naujiems vartotojams ir pakeisti vartotojo informaciją, ir tvarkyti šias užklausas per darbo srautą.

Jei planuojate rankiniu būdu nustatyti tiekėjų kontaktus ir vartotojus, galite padaryti prieinamą tik **Tiekėjo (išorinį) vaidmenį**. Tuomet šis vaidmuo bus vienintelis vaidmuo, kurio galima prašyti per tiekėjo vartotojo užklausą.

> [!NOTE]
> **SystemUser** vaidmuo yra suteikiamas automatiškai, kai naują vartotojo paskyrą sukuriate rankiniu būdu. Todėl turite pašalinti šį vaidmenį ir priskirti **SystemExternalUser** vaidmenį. Jei naujos vartotojo paskyros sukuriamos per darbo srautą, kurį inicijavo su tiekėju susijusi vartotojo užklausa pateikti naują vartotoją, bus priskirtas vienas ar daugiau vaidmenų, kuriuos nustatėte tiekėjų bendradarbiavimo srityje ir taip pat **SystemExternalUser** vaidmuo.

#### <a name="vendor-admin-external-security-role"></a>Tiekėjo administratoriaus (išorinis) saugos vaidmuo

**Tiekėjo administratoriaus (išorinis)** vaidmuo gali būti naudojamas išoriniams tiekėjams, kurie prižiūri tiekėjo kontaktinę informaciją ir pateikia užklausas parengti naujus tiekėjų bendradarbiavimo vartotojus. Šį saugos vaidmenį atliekantys išoriniai vartotojai gali atlikti šias užduotis:

- Peržiūrėti ir keisti kontaktinio asmens informaciją, pvz., asmens pareigas, el. pašto adresą ir telefono numerį.
- Į tiekėjo sąskaitas, kurių kontaktas jie yra, įtraukti naują arba esamą kontaktinį asmenį.
- Panaikinti visus jų sukurtus kontaktinius asmenius.
- Aktyvinti arba išjungti kontaktinio asmens ir tiekėjo sąskaitos susiejimą. Kai kontaktinio asmens ir tiekėjo sąskaitos susiejimas išjungiamas, kontaktinis asmuo negali būti nurodytas naujuose pirkimo užsakymuose arba kituose dokumentuose.
- Atmesti arba leisti kontaktinio asmens prieigą prie tiekėjo bendradarbiavimo sąsajos dokumentų, kurie yra specifiniai to tiekėjo paskyrai. Kai kontaktinio asmens ir tiekėjo sąskaitos susiejimas išjungiamas, prieiga prie dokumentų, kurie yra specifiniai tiekėjo paskyrai, visada uždrausta.
- Kontaktiniam asmeniui pateikti naujo vartotojo paskyrą naudojant **Parengti vartotoją** veiksmą.
- Prašyti, kad kontaktinio asmens vartotojo paskyra būtų išjungta.
- Prašyti, kad kontaktinio asmens vartotojo paskyra būtų keičiama,kad būtų įtraukti ar pašalinti saugos vaidmenys.
- RFQ rodinys.

#### <a name="vendor-external-security-role"></a>Tiekėjo (išorinis) saugos vaidmuo

**Tiekėjo (išorinis) vaidmuo** gali būti naudojamas išoriniams tiekėjams, kurie dirbs su pirkimo užsakymais. Šį saugos vaidmenį atliekantys išoriniai vartotojai gali atlikti šias užduotis:

- Atsakyti į pirkimo užsakymus ir peržiūrėti informaciją apie juos.
- Tvarkyti tiekėjo bendradarbiavimo SF.
- Rodyti konsignacijos atsargas.
- Peržiūrėti ir atsakyti į RFQ.
- Peržiūrėti tiekėjo informaciją.

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>Nustatyti saugos vaidmenis, naudojamus, kai yra priskiriami galimi tiekėjai

Norėdami priskirti tiekėjus, kurie inicijuojami pagal galimo tiekėjo registracijos užklausą, turite nustatyti išorinį saugos vaidmenį. Šis vaidmuo bus priskirtas naujiems vartotojams parengimo proceso, kurį kontroliuoja **Vartotojo užklausos darbo srautas (platforma)** tipo darbo srautas, metu. Norėdami gauti daugiau informacijos, toliau šioje temoje žr. skyrių [Nustatyti darbo eigas, kad būtų apdorojamos tiekėjo bendradarbiavimo vartotojo užklausos](#set-up-workflows-to-process-vendor-collaboration-user-requests).

Informacijos apie tai, kaip pateikti galimus tiekėjus, ieškokite [Tiekėjų pateikimas](vendor-onboarding.md).

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>Nustatyti saugos vaidmenį, kuris naudojamas, kai pateikiama nauja galimo tiekėjo vartotojo užklausa

1. Pasirinkite **Sistemos administravimas** > **Sauga** > **Išoriniai vaidmenys**.
2. Pasirinkite **Naujas**, tada pasirinkite saugos vaidmenį ir **Galimo tiekėjo** šalies vaidmenį.

Turėtumėte įtraukti **Tiekėjo galimą (išorinį)** vaidmenį, kuris teikiamas Supply Chain management programoje.

Saugos vaidmuo suteiks prieigą tik prie naujo tiekėjo registracijos vedlio.

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>Nustatyti darbo srautus tiekėjo bendradarbiavimo vartotojo užklausoms apdoroti

Norėdami užtikrinti, kad visos atitinkamos užduotys užbaigtos ir kad būtų suteikti atitinkami patvirtinimai, turite nustatyti darbo srautus tiekėjų bendradarbiavimo vartotojų užklausoms tvarkyti.

Tiekėjo bendradarbiavimo vartotojo užklausos pateikiamos per išorinius tiekėjus, kurie turi **Tiekėjo administratoriaus (išorinį)** saugos vaidmenį ar panašias teises, arba jūsų įmonėje yra įsigijimo specialistai. Jie taip pat gali būti generuojami pagal galimo tiekėjo registracijos užklausas, atliekant tiekėjo parengimo procesą.

Yra trys užklausų tipai:

- Užklausos parengti naują vartotoją
- Užklausos suaktyvinti esamą vartotoją
- Užklausos pakeisti esamo vartotojo saugos vaidmenis

Daugiau informacijos apie tiekėjo bendradarbiavimo vartotojų už-klausas žr. [Tiekėjo bendradarbiavimo vartotojų valdymas](manage-vendor-collaboration-users.md).

Turite sukurti du ar daugiau darbo srautų, kad būtų apdorojamos visų trijų tipų tiekėjų bendradarbiavimo vartotojų užklausos. Nauji darbo srautai kuriami **Vartotojo darbo srautai** puslapyje.

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>Darbo eigos, kai reikia nustatyti naujus vartotojus ir pakeisti saugos vaidmenis, pavyzdys

Norėdami tvarkyti su tiekėju susijusio vartotojo užklausas sukurti naujus vartotojus ir pakeisti saugos vaidmenis, darbo eigos pradžioje galite nustatyti filialų sąlygą. Tokiu būdu naudojama kita darbo srauto šaka, atsižvelgiant į tai, ar užklausa turi sukurti naują vartotoją, ar pakeisti esamą.

Norint nustatyti šį šakojimąsi, reikia sukurti naują **Vartotojo Užklausos Darbo srauto (platforma)** tipo darbo srautą. Šios darbo srauto šakos gali turėti šiuos elementus.

#### <a name="branch-to-provision-new-users"></a>Naujų vartotojų parengimo filialas

1. Priskirkite patvirtinimo užduotį asmeniui, atsakingam už tai, kad naujiems vartotojams turėtų būti suteikta prieiga prie tiekėjo bendradarbiavimo informacijos.
2. Priskirkite užduotį asmeniui, atsakingam už naujų Microsoft Azure Active Directory (Azure AD) vartotojo paskyras Azure portale. Šiam veiksmui atlikti naudokite iš anksto nustatytą **Send Azure B2B vartotojo kvietimo** užduotį. B2B vartotojai gali būti automatiškai eksportuoti į Azure AD. Naudokite iš anksto nustatytą **Parengti Azure AD B2B vartotoją**. Daugiau informacijos žr. [Eksportuoti B2B vartotojus į Azure AD](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md).
3. Priskirkite patvirtinimo užduotį asmeniui, kuris įkelia į Azure. Jei paskyros nepavyksta sėkmingai sukurti, šis asmuo atmeta užduotį ir baigiasi darbo srautas. Ši patvirtinimo užduotis gali būti praleista, jei įtraukėte veiksmą, kuris naujų vartotojų paskyras automatiškai eksportuoja į Azure, naudojant B2B programos programavimo sąsają (API).
4. Įtraukite automatizuotą užduotį, kuri parengia naują vartotoją. Šiam veiksmui atlikti naudokite iš anksto nustatytą **Automatizuotą galimą vartotoją**.
5. Įtraukite užduotį, kuri įspėja apie naują vartotoją. Galbūt norėsite naujam vartotojui išsiųsti pasisveikinimo el. laišką, kuriame yra Supply Chain Management programos URL. Šis el. laiškas gali naudoti šabloną, kurį sukuriate puslapyje **El. laiškai** ir tada pasirinkite **Vartotojo darbo srauto parametrai** puslapyje. Šablone gali būti **%portalURL%** žymė. Kai bus sugeneruotas pasisveikinimo el. laiškas, ši žymė bus pakeista Supply Chain Management programos nuomininko URL.

    > [!NOTE]
    > Šį darbo srautą galima naudoti keliuose scenarijuose, kuris apima vartotojo parengimą. Pavyzdžiui, jis gali būti naudojamas, kai galimiems tiekėjams arba kontaktiniams asmenims reikalinga tiekėjo bendradarbiavimo paskyra. Todėl turėtumėte frazuoti el. laišką kaip bendrąjį teiginį, kuris gali būti naudojamas keliems tikslams.

#### <a name="branch-to-modify-security-roles"></a>Filialas saugos vaidmenims modifikuoti

1. Priskirkite patvirtinimo užduotį asmeniui, atsakingam už saugos vaidmenų pakeitimų patvirtinimą.
2. Įtraukite automatizuotą užduotį, kuri prideda arba pašalina susijusius saugos vaidmenis. Šiam veiksmui atlikti naudokite **Automatizuotas galimas vartotojas** užduotį.

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>Vartotojo išjungimo darbo srauto pavyzdys

Sukurkite **Neaktyvaus vartotojo užklausos darbo srauto platformos** tipo darbo srautą, tada įtraukite šias užduotis.

1. Priskirkite patvirtinimo užduotį asmeniui, atsakingam už neaktyvių vartotojų užklausų priėmimą. Norėdami automatizuoti šį patvirtinimo veiksmą, galite pridėti sąlygų.
2. Įtraukite automatizuotą užduotį, kuri išjungia vartotoją. Šiam veiksmui atlikti naudokite **Automatizuotas vartotojo išjungimas** užduotį.
3. Įtraukite visas reikalingas valymo užduotis. Pavyzdžiui, galite įtraukti užduotį, kuri pašalina paskyrą iš Azure portalo katalogo.

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>Įgalinkite tiekėjo bendradarbiavimą konkrečiam tiekėjui

Prieš kurdami asmens, kuris naudos tiekėjo bendradarbiavimą, vartotojo paskyrą, turite nustatyti tiekėją taip, kad jis galėtų naudoti tiekėjo bendradarbiavimną. Puslapio **Tiekėjai** skirtuke **Bendra** nustatykite lauką **Bendradarbiavimo aktyvinimas**. Galimos toliau nurodytos parinktys:

- **Aktyvus (PU yra automatiškai patvirtinamas)**– pirkimo užsakymai automatiškai patvirtinami, jei tiekėjas priima juos neprašydamas keitimų.
- **Aktyvus (PU automatiškai netvirtinamas)** – jūsų organizacija turi rankiniu būdu patvirtinti pirkimo užsakymus po to, kai tiekėjas juos priima.

> [!NOTE]
> Jūsų įmonės įsigijimo specialistai taip pat gali atlikti šią užduotį.

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>Naujų tiekėjo bendradarbiavimo vartotojų parengimo trikčių šalinimas

Nauji tiekėjų bendradarbiavimo vartotojai yra parengti per darbo srautą, kurį nustatėte apdoroti tiekėjo bendradarbiavimo vartotojo užklausas, kurių tipas yra **Galimas tiekėjo vartotojas**.

Jei naujo tiekėjo bendradarbiavimo el. pašto adresas priklauso domenui, kuris registruojamas su "Azure" kaip nuomininkas (t. y. jei tai valdomo domeno paskyra), el. pašto adresas turi būti esamos Azure AD paskyros. Kitaip, parengimo proceso baigti negalima.

Daugiau informacijos apie procesą, kuris naudojamas **Siųsti Azure B2B vartotojui kvietimo** užduotį Azure AD paskyros valdymo darbo sraute, žr. [Azure Active Directory B2B bendradarbiavimas](/azure/active-directory/external-identities/what-is-b2b).

## <a name="additional-resources"></a>Papildomi ištekliai

[Tiekėjo bendradarbiavimas su išoriniais tiekėjais](vendor-collaboration-work-external-vendors.md)

Peržiūrėkite trumpą tiekėjo parengimo proceso vaizdo įrašą: [Naujo tiekėjoparengimas](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: „Mokėti sumokėjus“ tiekėjo mokėjimų nustatymas ir naudojimas
description: Šioje temoje aiškinama, kaip kurti „mokėti sumokėjus“ (PWP) sąlygas, kad galėtumėte išleisti dalinius tiekėjo mokėjimus, pagrįstus kliento mokėjimais.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284118"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>„Mokėti sumokėjus“ tiekėjo mokėjimų nustatymas ir naudojimas

[!include [banner](../includes/banner.md)]

Kai patvirtinate tiekėją ir jam leidžiate dirbti kaip subrangovui, mokėjimą tiekėjui galite sulaikyti tol, kol jums už projektą sumokės jūsų klientas. Pagal šį scenarijų, sąlygas „mokėti sumokėjus‟ (PWP) galite nustatyti tada, kai su tiekėju nustatote pirkimo užsakymą (PU).

Pavyzdžiui, kai klientas sumoka projekto SF sumą, galite išleisti dalį tiekėjo SF sumos arba visą sumą. Tiesiog nustatykite tokias PWP sąlygas, kuriomis nurodoma, kad tiekėjui bus sumokėta po to, kai iš kliento gausite susijusio mokėjimo procentą. Jei iš kliento gaunate dalinį mokėjimą, galite rankiniu būdu apmokėti išleisti kai kurias susijusias tiekėjo SF.

Toliau pateiktas pavyzdys apibūdina procesą, kai naudojamos PWP sąlygos.

## <a name="example"></a>Pavyzdys

Jūsų organizacija sutinka pateikti klientui 100 kompiuterių, kuriuose įdiegta programinė įranga. Vieno kompiuterio kaina – 150 JAV dolerių (USD). Tada jūs pasamdote tiekėją, kuris jums pateiks kompiuterius su įdiegta programinė įranga. Pagal sutartį klientas turi patvirtinti kompiuterių kokybę prieš sumokėdamas jūsų organizacijai. Jūsų organizacijos strategija yra sustabdyti mokėjimą tiekėjams, kol jums sumokės klientas. Todėl nustatote projektą taip, kad jo PWP procentas būtų 100 procentų.

Tiekėjas atsiunčia jums 100 kompiuterių, kuriuose įdiegta programinė įranga, kartu su sąskaita faktūra 10 000 USD sumai. PWP sąlygos nustatytos jūsų projektui, todėl gavęs kompiuterius jūs tiekėjui nesumokate. Vietoj to, jūs išsiunčiate kompiuterius klientui kartu su sąskaita faktūra 15 000 sumai. Klientas kompiuterius patikrina ir patvirtina visą projekto sąskaitos faktūros sumą.

Iš kliento gavę visą mokėjimą, tiekėjui sumokate tiekėjui 10 000 – visą tiekėjo SF sumą.

## <a name="set-up-pwp-terms-for-a-project"></a>Projekto PWP sąlygų nustatymas

Kai nustatote projekto PWP sąlygas, turite nurodyti (procentais) minimalią sumą, kurią klientas turi jums sumokėti už projektą, prieš jums sumokant tiekėjui. Ribinė suma automatiškai apskaičiuojama projekto kliento SF. Norėdami nustatyti PWP sąlygų ribinės vertės procentinį dydį, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**.
2. Suraskite ir atidarykite projektą, kuriam norite nustatyti PWP sąlygas.
3. „FastTab“ konteineryje **Tiekėjo sutartys** pasirinkite **Įtraukti eilutę**.
3. Lauke **Sąskaitos kodas** pasirinkite vieną iš toliau nurodytų parinkčių.

    - **Lentelė** – PWP sąlygos taikomos vienam tiekėjui.
    - **Grupė** – PWP sąlygos taikomos visiems tiekėjų grupės tiekėjams.
    - **Viskas** – PWP sąlygos taikomos visiems tiekėjams.

4. Jei ankstesniame veiksme pasirinkote **Lentelė** arba **Grupė**, lauke **Tiekėjas / tiekėjų grupė** pasirinkite tiekėją arba tiekėjų grupę, kuriai taikomos PWP sąlygos. Jei ankstesniame veiksme pasirinkote **Viskas**, lauko **Tiekėjas / tiekėjų grupė** redaguoti negalima.
5. Jei tiekėjui projekte nustatytos tiekėjo užlaikymo sąlygos, lauke **Tiekėjo užlaikymo sąlygos** pasirinkite užlaikymo sąlygų taisyklės ID.
6. Lauke **PWP ribinės vertės procentinis dydis** įveskite projekto ribinės vertės procentinį dydį. Jūsų įvestas projekto procentinis dydis apibrėžia minimalią sumą, kurią jums turi sumokėti klientas prieš jums sumokant tiekėjui.

## <a name="create-a-po-that-has-pwp-terms"></a>PU su PWP sąlygomis sukūrimas

Kai registruojate sąskaitą faktūrą iš tiekėjo, kuriam taikomos PWP sąlygos, tos sąlygos rodomos PU eilutėse. Norėdami sukurti PU su PWP sąlygomis, atlikite toliau nurodytus veiksmus.

1. Eikite į **Pirkimas ir tiekėjų parinkimas** \> **Pirkimo užsakymai** \> **Visi pirkimo užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas**. Tada dialogo lange **Kurti pirkimo užsakymą** įveskite reikiamą informaciją ir pasirinkite **Gerai**.

    Arba sąrašo puslapyje **Visi pirkimo užsakymai** galite atidaryti esamą PU.

4. Puslapyje **Pirkimo užsakymas**, „FastTab“ konteineryje **Pirkimo užsakymo eilutės** peržiūrėkite tiekėjui skirtos PU eilutės informaciją. Parinktis **Mokėti sumokėjus** yra pasirinkta automatiškai, o lauko **PWP ribinės vertės procentinis dydis** reikšmė automatiškai nukopijuojama iš lauko **PWP ribinės vertės procentinis dydis** puslapyje **Projektai**.
6. Jei nenorite, kad PU eilutėje tiekėjui būtų taikomos PWP sąlygos, išvalykite parinktį **Mokėti sumokėjus**. Šiuo atveju PU eilutei skirto lauko **PWP ribinės vertės procentinis dydis** reikšmė bus iš naujo nustatyta kaip 0 (nulis).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Kliento mokėjimo naujinimas ir mokėjimas tiekėjui

Kai tiekėjas baigia darbus projekte ir atsiunčia jums sąskaitą faktūrą, turite peržiūrėti projekto būseną ir kliento sąskaitas faktūras bei nustatyti, ar buvo įvykdytos projekto PWP sąlygos. Jei PWP sąlygos tiekėjui buvo vykdomos, galite nustatyti, kurias tiekėjo SF eilutes apmokėti, remdamiesi kliento mokėjimais už projektą. Jei nusprendžiate sumokėti tiekėjui, nors PWP sąlygos nebuvo įvykdytos, PWP sąlygų galite nepaisyti puslapyje **Tiekėjo SF, kurioms taikomas principas „mokėti sumokėjus“**.

1. Eikite į **Projektų valdymas ir apskaita** \> **Užklausos ir ataskaitos** \> **Užklausos apie užlaikymą** \> **Tiekėjo SF, kurioms taikomas principas „mokėti sumokėjus“**.
2. Norėdami rasti norimą peržiūrėti tiekėjo SF, puslapio **Tiekėjo SF, kurioms taikomas principas „mokėti sumokėjus“** ieškos lauke įveskite reikšmes ir pasirinkite **Ieškoti**.
3. „FastTab“ konteineryje **Tiekėjo SF eilutės** pasirinkite eilutes, kurias norite pakeisti.
4. Jei tenkinamos sąskaitos faktūros eilutės sąlygos **Mokėti sumokėjus**, pasirinkite **Pateikti tiekėjo mokėjimą**. Parinktis **Mokėti sumokėjus** yra išvaloma, o lauko **Paruošta mokėjimui** reikšmė pakeičiama į **Taip**.

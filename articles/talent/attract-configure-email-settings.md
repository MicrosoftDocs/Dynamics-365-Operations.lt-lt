---
title: „Attract“ el. pašto parametrų konfigūravimas
description: Šioje temoje paaiškinama, kaip konfigūruoti el. pašto, siunčiamo iš „Microsoft Dynamcis 365 Talent - Attract“, parametrus.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c1ebfaeb2e9bc2836bb70e87afa93484c829b6cb
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833120"
---
# <a name="configure-email-settings-in-attract"></a>„Attract“ el. pašto parametrų konfigūravimas

[!include [banner](includes/banner.md)]

Jūsų prekės ženklas kuria patikimumo įspūdį ir padeda užmegzti ryšį su kandidatais dar prieš jiems kandidatuojant į jūsų siūlomas darbo vietas. Teigiamas prekės ženklo įvaizdis pritraukia geriausius talentus ir didina esamų darbuotojų lojalumą. „Microsoft Dynamics 365 Talent: Attract“ galima sukonfigūruoti el. laiškus, kad juose atsispindėtų jūsų įmonės prekės ženklas. Todėl kandidatavimo proceso metu užtikrinsite nuoseklią kandidatų patirtį.

„Attract“ galite atlikti toliau nurodytus veiksmus.

- Konfigūruokite el. pašto parametrus, kad būtų naudojama jūsų įmonės „Microsoft Exchange“ el. pašto tarnybos paskyra. Taip kandidatai žinos, kad el. laiškai gaunami iš jūsų įmonės. Pavyzdžiui, galite sukonfigūruoti savo parametrus, kad kandidatai gautų el. laiškus iš `recruiting@contoso.com`, o ne `contoso@microsoft.com`.
- Užtikrinkite nuoseklų prekės ženklo naudojimą visuose el. laiškuose, nustatydami visuotines el. laiško šablonų antraštes ir poraštes. 

> [!NOTE]
> Jei norite sukonfigūruoti „Attract“, kad el. laiškai būtų siunčiami naudojant jūsų įmonės el. pašto tarnybos paskyrą, reikalingas priedas „Comprehensive hiring“.

## <a name="connect-an-email-service-account"></a>El. pašto tarnybos paskyros prijungimas

Prijungus savo įmonės el. pašto tarnybos paskyrą, kandidatai į darbo vietas gaus el. laiškus, kuriuose atsispindės jūsų prekės ženklas. Jei neprijungsite savo įmonės paskyros, „Attract“ naudos numatytąją „Microsoft“ prekės ženklo el. pašto tarnybos paskyrą.

1. Pasirinkite **Parametrai** (viršutiniame dešiniajame kampe esantis krumpliaračio simbolis) ir pasirinkite **Administravimo centras**.
2. Skirtuko **El. pašto parametrai** dalyje **El. pašto tarnybos paskyros** pasirinkite **Prijungti įmonės paskyrą**.

    ![Įmonės el. pašto tarnybos paskyros prijungimas naudojant „Attract“](./media/attract-admin-email-service-accounts.png)

    Daugiau informacijos, kaip kurti bendrinamą el. pašto paskyrą, žr. [Bendrinamos pašto dėžutės programoje „Exchange Online“](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).

3. „Microsoft“ prisijungimo lange prisijunkite naudodami savo įmonės kredencialus.
4. Jei dar nesate nustatę el. pašto tarnybos paskyros arba jei norite įtraukti naują, pasirinkite **Įtraukti naują tarnybos paskyrą** ir įveskite savo el. pašto paskyros informaciją. Jei jau nustatėte el. pašto tarnybos paskyrą, kurią norite naudoti, pasirinkite ją.

Sėkmingai sukonfigūravus jūsų el. pašto tarnybos paskyrą, ji bus rodoma dalyje **El. pašto tarnybos paskyros**.

## <a name="disconnect-an-email-service-account"></a>El. pašto tarnybos paskyros atjungimas

Jei nebenorite naudoti savo įmonės domeno el. laiškuose, siunčiamuose naudojant „Attract“, galite atjungti el. pašto tarnybos paskyrą.

1. Pasirinkite **Parametrai** (viršutiniame dešiniajame kampe esantis krumpliaračio simbolis) ir pasirinkite **Administravimo centras**.
2. Skirtuko **El. pašto parametrai** dalyje **El. pašto tarnybos paskyros** pasirinkite mygtuką **Daugiau** (trys vertikalūs taškai), esantį šalia el. pašto tarnybos paskyros, kurią norite atjungti.
3. Pasirinkite **Atjungti el. pašto paskyrą**.

    ![Įmonės el. pašto tarnybos paskyros atjungimas](./media/attract-admin-disconnect-email-account.png)

4. Kai būsite paraginti patvirtinti operaciją, pasirinkite **Atjungti**.

    ![Įmonės el. pašto tarnybos paskyros atjungimo patvirtinimas](./media/attract-admin-email-confirm-disconnect.png)

Jei neprijungsite kitos el. pašto tarnybos paskyros, siunčiant el. laiškus iš „Attract“ bus naudojama numatytoji „Microsoft“ prekės ženklo el. pašto tarnybos paskyra.

## <a name="configure-email-template-settings"></a>El. pašto šablonų parametrų konfigūravimas

Galite el. laiškų antraštėje naudoti savo įmonės logotipo vaizdą ir kitą informaciją. Taip pat galite el. laiško poraštėse nurodyti savo privatumo strategijos ir naudojimo sąlygų saitų.

> [!NOTE]
> Turite laikytis ne tik visų jūsų šalyje arba regione, bet ir el. laiško gavėjo šalyje arba regione galiojančių teisės aktų. Tai apima ir apsaugos nuo pašto šiukšlių nuostatas.

1. Pasirinkite **Parametrai** (viršutiniame dešiniajame kampe esantis krumpliaračio simbolis) ir pasirinkite **Administravimo centras**.
2. Skirtuko **El. pašto parametrai** dalyje **El. pašto šablonų parametrai** nuvilkite vaizdą, kurį norite naudoti kaip el. laiško antraštę, į vaizdo lauką arba spustelėkite vaizdo lauką ir raskite failą. Norėdami pakeisti esamą vaizdą, pirmiausia šalia vaizdo pasirinkite **Pašalinti**. Vaizdas turi būti JPEG, JPG, PNG arba SVG formato failas. Rekomenduojamas vaizdų dydis: 25–800 pikselių pločio ir 25–150 pikselių aukščio. Didžiausias antraštei tinkamas failo dydis yra 1 megabaitas (MB).

    ![Vaizdo įtraukimas į įmonės el. laiškų antraštę](./media/attract-admin-email-header.png)

3. Dalyje **Jūsų privatumo strategija bendravimui** nurodykite savo įmonės privatumo strategijos saitą. Dalyje **Jūsų bendravimo sąlygos** nurodykite savo įmonės naudojimo sąlygų saitą.

    ![Įmonės privatumo strategijos ir naudojimo sąlygų saitų įtraukimas į el. laiško poraštę](./media/attract-admin-email-footer.png)

4. Pasirinkite **Įrašyti**, kad įrašytumėte savo el. pašto šablono parametrus.

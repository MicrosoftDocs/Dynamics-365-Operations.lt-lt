---
title: „Microsoft Power Apps“ portalų naudojimas su šalies duomenų modeliu
description: Šiame straipsnyje aprašomi portalų žiniatinklio vaidmenų pakeitimai Microsoft Power Apps dėl dvigubo rašymo šalies duomenų modelio.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: 8d7a6ae48834ddd5f06f73bfe3129e44d14d86b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288993"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>„Microsoft Power Apps“ portalų naudojimas su šalies duomenų modeliu

[!INCLUDE[banner](../../includes/banner.md)]



Dvigubo rašymo programos instrumentavimo sprendimo 2.0.999.0 vėlesniuose versijose yra įrašo ir visuotinės adresų knygelės, skirti sąskaitų ir kontaktų lentelėms, duomenų modelio keitimai. Pakeitimai leidžia atlikti daug ryšių, kurie palaiko išplėstinius verslo scenarijus. Šių pakeitimų nepalaiko portalo žiniatinklio vaidmenys, įskaitant klientų portalą, kurie išsiųsti be lango arba kurie prieš įdiegdami dvigubą rašymo programą buvo jūsų aplinkoje. Kad žiniatinklio vaidmenys veiktų taip, kaip tikėjotės, turėsite sukurti naujus žiniatinklio vaidmenis naudodami naują duomenų modelį. 

Apibendrinant, kokiu būdu lentelės sąveikauja, bet kliento portale lentelės teisės nepasikeitė. Šiame straipsnyje paaiškinama, kaip sukurti naujus žiniatinklio vaidmenis, kurie veikia su naujuoju išplėstiniu duomenų modeliu.

Šioje diagramoje rodomas lentelės ryšys **be šalies ir visuotinės adresų** knygelės duomenų modelio:

   ![be šalies modelio.](media/without-party-model.PNG)

Šioje diagramoje rodomas lentelės ryšys **su šalies ir visuotinės adresų** knygelės duomenų modeliu:

   ![su šalies modeliu.](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Kurti naują lentelės teisę

Norėdami sukurti šias naujas lentelės teises, atlikite šiuos veiksmus:

1. Prisiregistruokite [„Power Apps“](https://make.powerapps.com) ir eikite į programėles.
2. Pasirinkite savo portalo valdymo programą.
3. Šoninioje juostoje pasirinkite **Sauga > Lentelės** teisės.

    Turite sukurti tris naujas teises:

    + **Kontakto** į **Šalį** lentelės ryšys
    + **Šalies** į **Paskyrą** lentelės ryšys
    + **Paskyros** į **Užsakymą** lentelės ryšys

4. Sukurkite ir įrašykite naują kontakto įrašo ryšio teisę, nustatydami šiuos parametrus:

    + **Pavadinimas**: **Šalis** į **Paskyrą** (arba jūsų pasirinktinis)
    + **Lentelės** pavadinimas: msdyn_contactforparty
    + **Svetainė**: Kliento portalas
    + **Tikslas**: kontaktas
    + **Teisės**: pasirinkti viską
    + **Žiniatinklio** vaidmenys: autentifikuoti vartotojai, klientų atstovas (arba jūsų pasirinkimas)

5. Sukurkite ir įrašykite naują kontakto šalies su paskyra ryšio teisę, nustatydami šiuos parametrus:

    + **Pavadinimas**: sąskaitos ryšio šalis (arba jūsų pasirinkimas)
    + **Lentelės** pavadinimas: sąskaita
    + **Svetainė**: Kliento portalas
    + **Tikslas**: pirminė
    + **Teisės**: pasirinkti viską
    + **Pirminės lentelės** teisės: kontakto į šalies ryšį

6. Sukurkite ir įrašykite naują kontakto paskyros su užsakymu ryšio teisę, nustatydami šiuos parametrus:

    + **Pavadinimas**: paskyros su užsakymo ryšys (arba jūsų pasirinkimas)
    + **Lentelės** pavadinimas: pardavimo užsakymas
    + **Svetainė**: Kliento portalas
    + **Tikslas**: pirminė
    + **Teisės**: pasirinkti viską
    + **Pirminės lentelės** teisės: šalies su paskyra ryšys

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

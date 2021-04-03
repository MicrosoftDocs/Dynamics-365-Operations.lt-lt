---
title: Aptarnavimo sutarčių ir projektų integravimas
description: Kai dirbate su aptarnavimo sutartimis ir aptarnavimo sutarties eilutėmis, naudojate šiose skyriaus Projektų valdymas ir apskaita srityse nustatytus duomenis.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd0a7de17e8ff098220fd183b714b77225cc217f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247315"
---
# <a name="integration-for-service-agreements-and-projects"></a>Aptarnavimo sutarčių ir projektų integravimas 

[!include [banner](../includes/banner.md)]


Kai dirbate su aptarnavimo sutartimis ir aptarnavimo sutarties eilutėmis, naudojate šiose skyriaus **Projektų valdymas ir apskaita** srityse nustatytus duomenis.

## <a name="project-prices"></a>Projekto kainos

Aptarnavimo sutarties operacijos savikaina ir pardavimo kaina yra išvestos iš savikainos nustatymo, taikomo prie aptarnavimo sutarties pridėtam projektui. Savikaina ir pardavimo kaina gali būti nustatyta pagal projektą, darbuotoją ir kategoriją. 

## <a name="project-validation"></a>Projekto tikrinimas

Projektus, darbuotojus ir kategorijas, kuriuos galima pasirinkti aptarnavimo sutarties eilutėje, galima riboti nustatant tikrinimą **Projektų valdymas ir apskaita**. Nustatydami tikrinimą galite jungti darbuotojus, projektus ir kategorijas valdymo prieigai. 

## <a name="project-line-properties"></a>Projekto eilučių ypatybės

Aptarnavimo sutarties eilutės ypatybė įvedama automatiškai.

Eilučių ypatybės kuriamos formos **Eilutės ypatybės** dalyje **Projektų valdymas ir apskaita**. Aptarnavimo sutartyje įvesta eilutės ypatybė pridedama prie projekto, kuris pasirinktas aptarnavimo sutarčiai, ir vėliau ją paveldi aptarnavimo sutarties eilutė. 

## <a name="default-offset-accounts"></a>Numatytosios korespondentinės sąskaitos

Jei įvesite išlaidų operaciją, šiai operacijai automatiškai pasirenkama numatytoji išlaidų korespondentinė sąskaita. Numatytoji išlaidų sąskaita nustatoma projekte, pridėtame prie dabartinės aptarnavimo sutarties.

## <a name="project-categories"></a>Projekto kategorijos

Galimos aptarnavimo sutarties eilučių kategorijos nustatomos formos **Projekto kategorijos** dalyje **Projektų valdymas ir apskaita**. 

> [!NOTE]
> <P>Galima pasirinkti kategorijas, kurių žymės langelis <STRONG>Aktyvus žurnaluose</STRONG> pažymėtas skirtuko <STRONG>Projektas</STRONG> formoje <STRONG>Projektų kategorijos</STRONG>. Tačiau, jei žymės langelis <STRONG>Neaktyvios kategorijos</STRONG> pažymėtas skirtuko <STRONG>Žurnalai</STRONG> formoje <STRONG>Projektų valdymo ir apskaitos parametrai</STRONG>, galima pasirinkti visas kategorijas.</P>

## <a name="project-parameters"></a>Projekto parametrai

Jei pasirinktas laukas **Atleisti darbuotojai**, esantis skirtuko **Žurnalai** formoje **Projektų valdymo ir apskaitos parametrai**, neaktyvius ir aktyvius darbuotojus formose **Aptarnavimo sutartys** ir **Aptarnavimo objektai**.

Taip pat, jei norite įvesti pradžios ir pabaigos laiką aptarnavimo užsakymo eilutėse, galite įgalinti laukus **Pradžios laikas** ir **Pabaigos laikas**, esančius skirtuko **Projektas** formoje **Aptarnavimo užsakymai**.

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>Aptarnavimo užsakymų pradžios ir pabaigos laiko funkcijos įgalinimas

1.  Spustelėkite **Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**.

2.  Spustelėkite skirtuką **Žurnalai**, tada pažymėkite žymės langelį **Rodyti pradžios / pabaigos laikus**.

3.  Spustelėkite **Projektų valdymas ir apskaita** \> **Sąranka** \> **Žurnalai** \> **Žurnalų pavadinimai**.

4.  Pasirinkite žurnalo, kuris pridėtas prie aptarnavimo užsakymo, pavadinimą.

5.  Spustelėkite skirtuką **Bendra**, tada pažymėkite žymės langelį **Rodyti pradžios / pabaigos laikus**.


> [!NOTE]
> <P>Aptarnavimo užsakymo žurnalo pavadinimą pasirinkite lauke <STRONG>Valanda</STRONG>, esančiame skirtuko <STRONG>Žurnalai</STRONG> formoje <STRONG>Aptarnavimo valdymo parametrai</STRONG>.</P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
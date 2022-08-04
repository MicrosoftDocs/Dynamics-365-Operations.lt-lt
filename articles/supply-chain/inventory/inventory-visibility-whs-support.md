---
title: WMS prekių „Inventory Visibility“ palaikymas
description: Šiame straipsnyje aprašomas prekių, kurios įgalintos sandėlio valdymo procesams (WMS prekėms), atsargų matomumo palaikymas.
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 54ce637d2d7b590988f7590eae5248276bcc4b96
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066617"
---
# <a name="inventory-visibility-support-for-wms-items"></a>WMS prekių „Inventory Visibility“ palaikymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomas prekių, kurios įgalintos sandėlio valdymo procesams (WMS), atsargų matomumo palaikymas. Funkcija, kuri įtraukia šią galimybę į atsargų matomumą, vadinama išplėsta *WMS*.

## <a name="wms-items"></a>WMS prekės

WMS prekė yra prekė, kurią galima naudoti WMS ir apdoroti sandėlyje, kuriame taip pat įgalinta WMS.

Daugiau informacijos apie WMS ir "Microsoft" sandėlio **valdymo** modulį Dynamics 365 Supply Chain Management ieškokite Sandėlio [valdymo peržiūra](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Priemonės apimtis

Išplėstinė WMS funkcija, skirta atsargų matomumo židiniams, skirti turimo kiekio skaičiavimams, pagrįstiems turimo kiekio užklausomis. Ši funkcija nėra skirta leisti naudoti atsargų matomumą norint bendrai valdyti sandėlio apdorojimo veiklas. Atsargų matomumas neturi tam tikrų sandėlio sąvokų savo vartotojams. Štai keletas šių sąvokų pavyzdžių:

- Rezervavimo hierarchija
- Ar prekė arba sandėlis yra įgalinti WMS
- Vienetų sekų grupės ID
- Sandėliui konkretūs procesai, pvz., siuntos, kroviniai, bangos ir darbas

Ši informacija, paremta duomenimis, siunčiamais iš tiekimo grandinės valdymo, rodo atsargų matomumą. WMS konkretūs duomenys (kitaip tariant, lentelės duomenys `WHSInventReserve`) nematomi vartotojams.

Kai naudojate išplėstinę WMS funkciją atsargų matomumui nustatyti, visi užklausos rezultatai bus identiški užklausų, tiesiogiai gaminamų tiekimo grandinės valdymo funkcijai, rezultatams. Tačiau jos nebus identiškos užklausų, kurios buvo pagamintos naudojant sandėlio valdymo mobiliąją programą, rezultatams, nes mobiliųjų įrenginių programa šiek tiek naudoja kitokią skaičiavimo logiką.

## <a name="when-to-use-the-feature"></a>Kada naudoti funkciją

Rekomenduojame naudoti išplėstinę WMS funkciją atsargų matomumui scenarijuose, kur tenkinamos visos šios sąlygos:

- Sinchronizuojate tiekimo grandinės valdymo duomenis su atsargų matomumu.
- WMS naudojate tiekimo grandinės valdymo srityje.
- Vartotojai rezervuojant WMS prekes ne sandėlio lygiu (pvz., dėl to, kad naudojate sandėlio darbą).

Kituose scenarijuose turimų atsargų užklausų rezultatai bus vienodi, nepaisant to, ar įgalinta atsargų matomumo išplėstinė WMS funkcija. Be to, jei šių scenarijų funkcijos įjungsite ne taip, bus geriau veikia našumas, nes yra mažiau skaičiavimų ir mažiau papildomų duomenų.

## <a name="enable-the-advanced-wms-feature-for-inventory-visibility"></a>Įjungti išplėstinę WMS funkciją atsargų matomumui nustatyti

Norėdami įjungti išplėstinę WMS funkciją atsargų matomumui, atlikite šiuos veiksmus.

1. Prisijungti prie tiekimo grandinės valdymo kaip administratorius.
1. Atidarykite [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį ir įgalinkite šias priemones šia tvarka:

    1. *Atsargų matomumo integravimas*
    1. *Įgalinti sandėlio prekes atsargų matomumo skiltyje*

1. Eikite į **Atsargų valdymas \> Sąranka \> Atsargų ir sandėlio matomumo integravimo parametrai**.
1. Skirtuke **Įgalinti WMS prekes** nustatykite parinktį **Įgalinti WMS prekes** kaip *Taip*.
1. Prisijungti prie „Power Apps”.
1. Atidarykite **konfigūracijos** puslapį, tada funkcijų valdymo **skirtuke** įjunkite funkciją *AdvancedWHS*.
1. Tiekimo grandinės valdymo srityje eikite į atsargų **valdymo periodinių užduočių \> atsargų \> matomumo integravimą**.
1. Veiksmų srityje pasirinkite Uždrausti, kad **laikinai** išjungtumėte atsargų matomumą.
1. Veiksmų srityje pasirinkite Įgalinti **, kad** atsargų matomumą būtų galima pakeisti. Priedas įkeliamas iš naujo ir dabar įgalinta nauja funkcija. Su WMS susiję duomenys pradedama sinchronizuoti su atsargų matomumu.

## <a name="query-on-hand-quantities-of-wms-items"></a>Pateikti užklausą dėl WMS prekių turimos kiekio

Norėdami pateikti WMS prekių užklausą naudokite tą pačią [programos programavimo sąsają (API)](inventory-visibility-api.md) ir pranešimo sintaksę, kurią naudojate ne WMS prekėms. Jums nereikia nurodyti, ar prekė yra WMS prekė, ar ne WMS prekė. Atsargų matomumas automatiškai atskiria prekes pagal saugomus duomenis.

WMS prekių užklausų rezultatai iš esmės yra tokie patys, kaip ir ne WMS prekių rezultatai. Vienintelis skirtumas yra tai, kad šie faktiniai duomenų `fno` šaltinio duomenys apskaičiuojami remiantis tiekimo grandinės valdymo WMS logika:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Visi kiti faktiniai priemonės skaičiuojami taip pat, kaip kai išjungta atsargų matomumo išplėstinė WMS funkcija.

Išsamesnės informacijos apie tai, kaip veikia WMS prekių turimi skaičiavimai, [ieškokite sandėlio valdymo baltosios knygos rezervavimuose](https://www.microsoft.com/download/details.aspx?id=43284).

Į eksportuojamus duomenų objektus Dataverse dar negalima atnaujinti WMS prekių kiekių. Kiekiai, rodomi duomenų objektuose, yra tinkami ir ne WMS prekėms, ir kiekiams, kurių nepatako WMS logika (tai yra, priemonės, `AvailPhysical` išskyrus, `AvailOrdered` ir `ReservPhysical``ReservOrdered``fno` duomenų šaltinyje).

WMS prekių kiekių, saugomų tiekimo grandinės valdymo duomenų šaltinyje, pakeitimus draudžiama. Šis apribojimas taikomas, kaip ir kitoms atsargų matomumo funkcijoms, kad išvengtų konfliktų.

## <a name="soft-reservations-on-wms-items-in-inventory-visibility"></a>Švelniai WMS prekių rezervavimas atsargų matomume

Apskritai, palaikomi [WMS](inventory-visibility-reservations.md) prekių švelniai rezervavimai. Galite įtraukti su WMS susijusius faktinius duomenis į soft reservation calculations. 

Žinomame apribojime WMS *prekės šiuo* metu nepalaiko rezervavimo skaičiavimo. Todėl jei rezervavimas viršija dabartines dimensijas, kuriose vyksta švelniai rezervavimas, *galimas rezervavimo skaičiavimas* yra klaidingas. Soft rezervavimai nebus paveikti, kai parinktisCheckAvailForReserv **yra** išjungta soft [reservation API](inventory-visibility-api.md#create-one-reservation-event).

Šis apribojimas taip pat taikomas funkcijoms ir pritaikymams, kurie pagrįsti švelniais rezervavimais (pvz., paskirstymu).

## <a name="calculate-available-to-promise-quantities"></a>Apskaičiuoti prieinamų prekių kiekius

Sprendimas visiškai palaiko WMS [prekių prieinamų prekių prieinamą](inventory-visibility-available-to-promise.md) atsargos (ATP). Galite nurodyti ATP skaičiavimus nenaudodami WMS konkrečios informacijos.

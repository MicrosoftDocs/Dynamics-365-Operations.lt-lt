---
title: Valdyti funkcijas „Human Resources“
description: Šiame straipsnyje aprašoma funkcijų valdymo funkcija ir kaip ją naudoti.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5023e8b60ede1f75961abff158bec9424d1aca4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907615"
---
# <a name="manage-features-in-human-resources"></a>Valdyti funkcijas „Human Resources“


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Mūsų nuolatinis naujų galimybių, skirtų „Microsoft Dynamics 365 Human Resources“, išleidimas apima norą leisti vartotojams kuo greičiau išbandyti naujas funkcijas. Teikiamos peržiūros funkcijos, kurios yra beveik paruoštos visuotinai pasiekti, ir kurioms jau buvo atlikta daug bandymų. Mes tiesiog laukiame galutinio klientų atsiliepimų etapo ir tikrinimo prieš jas bendrai išleisdami.

Daugiau informacijos apie naujas „Human Resources“ funkcijas žr. [Kas nauja programoje „Human Resources“](hr-admin-whats-new.md) ir  [„Dynamics 365“ ir „Power Platform“ leidimo planas](/dynamics365/release-plans/?panel=products1#pivot=products).

Darbo srityje **Funkcijų valdymas** pateikiamas priemonių, pristatytų kiekviename leidime, sąrašas. Pagal numatytuosius nustatymus naujos funkcijos yra išjungtos. Galite naudoti darbo sritį, norėdami jas įjungti ir peržiūrėti jų dokumentaciją. Daugiau informacijos apie funkcijų valdymą žr. [Funkcijos valdymo apžvalga](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Visos naujos funkcijos išlieka peržiūroje bent 30 dienų ir paprastai 30–60 dienų. Pagrindinės funkcijos paprastai pasiekiamos kiekvienų metų spalį ir balandį po peržiūros laikotarpio. Kai tik pradedame naujas galimybes darbo srityje **Funkcijų valdymas**, galite jas įjungti. Kai kurios funkcijos gali būti pagal numatytuosius parametrus.

Kai funkcija jau pasiekiama, ją galima įjungti arba išjungti gamybos aplinkose. Darbo sritis **Funkcijų valdymas** nurodo, kada peržiūros funkcija taps privaloma. Paprastai ši data yra spalio 1 d. arba balandžio 1 d., siekiant suderinti su pusmečio leidimų planais. Negalite išjungti privalomų funkcijų. Kol ji taps privaloma, šią funkciją galite įjungti ir išjungti visose aplinkose.

## <a name="enable-or-disable-preview-features"></a>Peržiūros funkcijų įjungimas arba išjungimas

Norėdami pasiekti peržiūros funkcijas, pirmiausia turite jas įjungti savo aplinkoje. Peržiūros funkcijų įjungimas arba išjungimas priklauso nuo aplinkos.

> [!IMPORTANT]
> Peržiūros funkcijos pasiekiamos tik aplinkose **Smėlio dėžė**. Įjungę peržiūros funkciją, ją įjungsite visiems jūsų organizacijos vartotojams, esantiems šioje aplinkoje. Išjungę šią peržiūros funkciją, ją išjungsite ir ji taps nepasiekiama jūsų vartotojams. Peržiūros funkcijos programoje „Human Resources“ turi ribotą palaikymą. Galima naudoti mažiau privatumo ir saugos priemonių, jos nėra įtrauktos į „Human Resources“ teikiamų paslaugų sutartį (SLA). Asmens duomenims (t. y., bet kokiai informacijai, kuri galėtų jus identifikuoti) arba kitiems duomenims, kuriems yra taikomi teisiniai ar atitikties reikalavimai, apdoroti nenaudokite peržiūros funkcijų.

1. Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.

2. Pasirinkite plytelę **Funkcijų valdymas**.

3. Norėdami įjungti peržiūros funkciją, pasirinkite ją iš sąrašo, tada pažymėkite **Įjungti**. Norėdami išjungti peržiūros funkciją, pasirinkite ją iš sąrašo, tada pažymėkite **Išjungti**.

## <a name="enable-or-disable-benefits-management"></a>Išmokų valdymo įjungimas arba išjungimas

Norėdami įgalinti išmokų valdymą, atlikite procedūrą, esančią [Peržiūros funkcijų įjungimas arba išjungimas](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Po to, kai **gamybos** aplinkoje įgalinate išmokų valdymą, jo išjungti negalima. Tačiau galite išjungti išmokų valdymą **smėlio dėžės** aplinkose.

Daugiau informacijos apie išmokų valdymo konfigūravimą ir naudojimą žr. [Išmokų valdymo apžvalga](hr-benefits-management-overview.md).

Išmokų valdymu pakeičiamos funkcijos darbo srityje **Išmokos**. Kai įjungiate peržiūros funkciją Išmokų valdymas, nebegalite naudotis šiomis formomis darbo srityje **Išmokos**:

- **Išmokos**
- **Išmokos elementai**
- **Įnašų apskaičiavimo tarifai**
- **Registracijos išmokai gauti rezultatai**
- **Išmokos galiojimo nutraukimo ir pratęsimo rezultatai**
- **Išmokos tinkamumo strategijos taisyklių tipai**
- **Teisės į išmoką strategijos**
- **Tinkamumo įvykiai**

Galite peržiūrėti šių puslapių informaciją tik skaitymo režimu. Jei norite redaguoti informaciją, pirmiausia turite išjungti išmokų valdymą (taikoma tik **smėlio dėžės** aplinkose).

## <a name="enable-or-disable-leave-and-absence"></a>Atostogų ir neatvykimų įjungimas arba išjungimas

Norėdami įgalinti atostogas ir neatvykimus, atlikite procedūrą, esančią [Peržiūros funkcijų įjungimas arba išjungimas](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Po to, kai įjungiate atostogų ir neatvykimų funkciją **Keli atostogų tipai**, jos išjungti negalima. Tai taikoma ir **smėlio dėžės**, ir **gamybos** aplinkose.

Daugiau informacijos apie atostogų ir neatvykimų peržiūros funkcijas žr. [Atostogų ir neatvykimų peržiūros funkcijos](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

## <a name="send-us-feedback"></a>Atsiųskite atsiliepimą

Norime sužinoti jūsų nuomonę apie jūsų įspūdžius naudojant peržiūros funkcijas. Naudojant šias arba bet kurias kitas funkcijas, skatiname reguliariai registruoti savo atsiliepimus toliau nurodytose svetainėse.

- [Bendruomenė](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – ši svetainė yra puikus šaltinis, kuriame vartotojai gali diskutuoti, naudoti atvejus, užduoti klausimų ir gauti bendruomenės pagalbos.
- Praneškite mums apie funkcijas, kurias norite matyti produkte, arba praneškite apie esamų funkcijų pakeitimus, kurie, jūsų manymu, turi būti atlikti. Siūlykite produktų idėjų skiltyje [„Human Resource“ idėjos](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources).
    
Neįtraukite asmeninių duomenų (bet kokios informacijos, kuri gali jus identifikuoti) į savo atsiliepimų ar produkto apžvalgų pateikimus. Surinkta informacija gali būti analizuojama toliau, ji nebus naudojama atsakyti į užklausas pagal taikomus privatumo įstatymus. Atskirai surinktiems asmeniniams duomenims pagal šias programas taikomos [„Microsoft“ privatumo nuostatos](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Taip pat žiūrėkite

- [Kas nauja programoje „Human Resources“](hr-admin-whats-new.md)
- [„Dynamics 365“ ir „Power Platform“ leidimo planas](/dynamics365/release-plans/?panel=products1#pivot=products)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

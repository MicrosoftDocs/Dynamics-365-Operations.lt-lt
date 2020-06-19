---
title: Mokėjimo tiekėjui užlaikymo sąlygų kūrimas ir taikymas
description: Šioje temoje pateikiama informacija apie tai, kaip nustatyti ir tvarkyti mokėjimo tiekėjui užlaikymo sąlygas.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410249"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Mokėjimo tiekėjui užlaikymo sąlygų kūrimas ir taikymas

[!include [banner](../includes/banner.md)] 

Projekto mokėjimo tiekėjui užlaikymo sąlygas nustatyti naudinga, kai jūsų organizacija nori užlaikyti tiekėjui atliekamų mokėjimų dalį. Pavyzdžiui, kai norite sulaikyti mokėjimą tiekėjui, kol pristatyti produktai atitiks jūsų lūkesčius. Mokėjimo tiekėjui užlaikymo sąlygas galima nurodyti derybų dėl tiekėjo sutarties metu.

## <a name="create-vendor-payment-retention-terms"></a>Mokėjimo tiekėjui užlaikymo sąlygų kūrimas

Galite įvesti mokėjimo tiekėjui procentinę dalį, kurią norite užlaikyti, ir anksčiau užlaikytų sumų procentinę dalį, kurią norite atiduoti. Sumos automatiškai užlaikomos tiekėjo SF, kol pasiekiama nurodyta sutarties pabaigimo būsena. Nustatę užlaikymo sąlygas, galite jas taikyti bet kuriame šio tiekėjo projekte.

Vadovaudamiesi toliau pateiktais veiksmais nustatykite ir tvarkykite mokėjimo tiekėjui užlaikymo sąlygas. 

1. Eikite į **Projektų valdymas ir apskaita** > **Užlaikymas** > **Mokėjimo tiekėjui užlaikymo sąlygos**.
2. Pasirinkite **Nauja**, kad įtrauktumėte naują tiekėjo užlaikymo sąlygą. Naujos sąlygos **Taisyklės ID** reikšmė įvedama automatiškai. 
3. Įveskite trumpą aprašymą lauke **Aprašymas**, „FastTab“ **Sąlygos** pasirinkite **Įtraukti eilutę** ir įveskite toliau pateiktas vertes:

   - **Pristatytų vienetų procentinė dalis** – įveskite sąlygoje naudojamą užbaigtumo procentinį dydį. Sumos automatiškai užlaikomos tiekėjo SF, kol projekto užbaigtumo būsena netampa lygi jūsų nurodytam procentiniam dydžiui. Pvz., jei įvedate 50,00, sumos užlaikomos, kol 50 procentų projekto nebūna baigta.
   - **Užlaikytina procentinė dalis** – įveskite tiekėjo SF sumos procentinę dalį, kuri bus užlaikyta. Pvz., jei įvedate 10,00, užlaikoma 10 procentų tiekėjo SF sumos, kol nepasiekiamas projekto užbaigtumo procentinis dydis, nustatytas lauke **Pristatytų vienetų procentinė dalis**.
   - **Atiduodama procentinė dalis** – pasirinkite **Įtraukti eilutę** ir įveskite bet kurių anksčiau užlaikytų sumų procentinę dalį, kurią norite atiduoti esant pasirinktam projekto užbaigtumo lygiui.

> [!NOTE]
> Jei naudojate daugiau nei vieną skirtingų projekto užbaigtumo lygių etapą, įveskite atskirą kiekvienos užlaikymo taisyklės tiekėjo užlaikymo sąlygos eilutę. Kiekvienoje eilutėje galima nurodyti vis kitą procentinę dalį, kurią norite užlaikyti ir kurią reikia atiduoti pasiekus kiekvieną sukurtą projekto užbaigtumo lygį.

Sukūrę užlaikymo sąlygas tiekėjui, galite jas taikyti bet kuriam šio tiekėjo projektui.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Tiekėjo užlaikymo sąlygų taikymas projektui

1. Eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Visi projektai** ir atidarykite projektą iš projektų sąrašo puslapio.
2. „FastTab“ konteineryje **Tiekėjo sutartys** pasirinkite **Įtraukti eilutę**.
3. Lauke **Sąskaitos kodas** pasirinkite vieną iš toliau nurodytų parinkčių. 

   - **Lentelė** – tiekėjo užlaikymo sąlygos taikomos vienam tiekėjui.
   - **Grupė** – tiekėjo užlaikymo sąlygos taikomos visiems tiekėjų grupės tiekėjams.
   - **Visi** – tiekėjo užlaikymo sąlygos taikomos visiems tiekėjams.

4. Lauke **Tiekėjas / tiekėjų grupė** pasirinkite tiekėją arba tiekėjų grupę, kuriam (-iai) taikomos tiekėjo užlaikymo sąlygos. Jei atlikdami ankstesnį veiksmą pasirinkote **Visi**, šio lauko naudoti negalima.
5. Lauke **Tiekėjo užlaikymo sąlygos** pasirinkite užlaikymo sąlygas, kurias sukūrėte ankstesnėje procedūroje.
6. Jei projekte tiekėjui taip pat nustatytos sąlygos „mokėti sumokėjus“ (PWP), lauke **PWP ribinės vertės procentinis dydis** įveskite projekto ribinės vertės procentinį dydį.

Tiekėjo užlaikymo sąlygos taip pat rodomos pirkimo užsakymuose, kuriuos sukuriate tiekėjui.

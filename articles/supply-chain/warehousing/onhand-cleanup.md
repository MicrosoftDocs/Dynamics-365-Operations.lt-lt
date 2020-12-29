---
title: Sandėlio valdymo turimų įrašų valymo užduotis
description: Šioje temoje aprašoma turimų atsargų valymo užduotis, kuri padeda pagerinti sistemos efektyvumą nustatant ir naikinant susijusius, bet nereikalingus įrašus.
author: perlynne
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 9d01c577fc33564d3517d242e9b01f73cc8e079c
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433978"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Sandėlio valdymo turimų įrašų valymo užduotis

Užklausų, naudojamų skaičiuojant turimas atsargas, efektyvumas priklauso nuo įtrauktų lentelių įrašų skaičius. Vienas iš būdų pagerinti efektyvumą yra sumažinti įrašų, kuriuos turi įvertinti duomenų bazė, skaičių.

Šioje temoje aprašomos turimų įrašų valymo užduotys, kurios panaikina nereikalingus įrašus lentelėse „InventSum“ ir „WHSInventReserve“. Šiose lentelėse saugoma turima informacija apie prekes, kurios yra įjungtos atliekant sandėlio valdymo apdorojimą. (Šios prekės vadinamos WHS prekėmis.) Šio įrašo panaikinimas gali ženkliai pagerinti turimų skaičiavimų efektyvumą.

## <a name="what-the-cleanup-job-does"></a>Ką atlieka valymo užduotis

Turimų įrašų valymo užduotis panaikina visus įrašus, esančius lentelėse „WHSInventReserve“ ir „InventSum“, kur visų laukų reikšmės yra *0* (nulis). Šiuos įrašus galima panaikinti, nes jie neprisideda prie turimos informacijos. Užduotis panaikina tik žemesnius nei **Vietos** lygmens įrašus.

Jei leidžiamos neigiamos fizinės atsargos, valymo užduočiai gali nepavykti panaikinti visų atitinkamų įrašų. Šis apribojimas taikomas todėl, kad užduotis turi numatyti specialų scenarijų, kai numerio lentelėje yra keli serijos numeriai, o vienas iš tų serijos numerių tapo neigiamu. Pavyzdžiui, sistemos numerio lentelėje bus nulis, kai numerio lentelėje yra +1 vnt. 1 serijos numerio 1 ir –1 vnt. 2 serijos numerio. Naudojant šį specialų scenarijų, pirmiausia bus bendrai panaikinti žemesnių lygių įrašai.

## <a name="schedule-and-configure-the-cleanup-job"></a>Valymo užduočių planavimas ir konfigūravimas

Turimų atsargų valymo užduotį galima atlikti dalyje **Atsargų valdymas \> Reguliarios užduotys \> Valyti \> Sandėlio valdymo turimų įrašų valymas**. Naudokite standartines užduoties nuostatas, norėdami valdyti užduoties vykdymo apimtį ir grafiką. Be to, suteikiami toliau nurodyti parametrai:

- **Naikinti, jei neatnaujinta nurodytą dienų skaičių** – įveskite minimalų dienų skaičių, kurį turi laukti ši užduotis, prieš panaikindama turimą įrašo, kurio kiekis sumažėjo iki nulio. Naudokite šį parametrą, kad nepanaikintumėte vis dar naudojamų turimų įrašų. Jei norite, kad valymas būtų atliekamas kuo greičiau, įveskite *0* (nulis) arba palikite lauką tuščią.
- **Maksimalus vykdymo laikas (valandomis)** – įveskite maksimalų valymo užduoties vykdymo laiką valandomis. Jei užduotis neužbaigiama per šį laikotarpį, atliktas darbas įrašomas ir užduotis išsijungia. Šis galimybė ypač aktuali atvejais, kai atsargos aktyviai naudojamos. Tokiais atvejais turite suplanuoti užduotį, kurią reikia paleisti, kai sistemos apkrova yra kuo mažesnė. Jei norite, kad paketinė užduotis tęstųsi, kol ji bus baigta, įveskite *0* (nulis) arba palikite lauką tuščią. Šis parametras galimas tik tada, kai [jūsų sistemoje įjungta susijusi funkcija](#max-execution-time).

Nors užduotį galite vykdyti įprastomis darbo valandomis, rekomenduojame paleisti ją ne darbo valandomis. Tokiu būdu išvengsite konfliktų, kurių gali kilti, jei vartotojas dirba su įrašu, kuris tuo pačiu yra naikinamas.

Jei užduotis mėgina panaikinti prekės įrašą, kol įrašu naudojasi kitas vartotojas, valymo užduočiai arba naudotojui pranešama apie aklavietės klaidą.

Kai užduotis vykdoma, jos vykdymo dydis yra 100. Kitaip tariant, ji bus vykdoma kas 100 panaikinimų. Tačiau, kadangi kai kurie naikinimai yra grįsti rinkiniais, kai kuriais atvejais ta pačia operacija galima panaikinti daugiau kaip 100 įrašų. Todėl vis tiek gali kilti konfliktų.

## <a name="possible-user-impact"></a>Galimas poveikis vartotojams

Vartotojai gali pajusti poveikį, jei turimų įrašų valymo užduotis panaikina visus nurodyto lygio įrašus (pvz., numerio lentelės lygį). Tokiu atveju numerio lentelės atsargos gali būti nerodomos kaip numatyta, nes atitinkamų turimi įrašų nebėra. (Ši funkcija patikrina sąlygą **Kiekis \<\> 0** **Dimensijos rodinio** parametruose, kai vartotojai peržiūri turimą informaciją.) Tačiau našumo pagerėjimas, kurį suteikia valymo užduotis, turėtų kompensuoti šį nežymų funkcionalumo praradimą.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Maksimalaus vykdymo laiko parametro įgalinimas

Pagal numatytuosius nustatymus **Maksimalaus vykdymo laiko** parametras yra nepasiekiamas. Jei norite juo naudotis, turite naudoti [funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad galėtumėte įjungti susijusią priemonę savo sistemoje. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *maksimalus vykdymo laikas sandėlio valdymo turimų įrašų valymo užduočiai*

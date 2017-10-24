---
title: "Užsakymo apdorojimo pasirinkčių nustatymas"
description: "Šioje temoje pateikiama informacija apie tai, kaip apdoroti skambučių centro užsakymus naudojant „Microsoft Dynamics 365 for Retail“."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a0f3d1aea49f0251ecc68e70b4b6054e1813c8ad
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-order-processing-options"></a>Užsakymo apdorojimo parinkčių nustatymas

[!include[banner](includes/banner.md)]


Šioje temoje pateikiama informacija apie tai, kaip apdoroti skambučių centro užsakymus naudojant „Microsoft Dynamics 365 for Retail“. 

„Retail‟ palaiko kelis mažmeninės prekybos kanalus, pvz., internetines parduotuves, tradicines parduotuves ir skambučių centrus. Skambučių centruose darbuotojai priima klientų užsakymus telefonu ir kuria pardavimo užsakymus. Šioje temoje aprašoma, kaip sukurti skambučių centrą ir konfigūruoti skambučių centro parinktis. Kiekvienas skambučių centras gali turėti atskirus vartotojus, mokėjimo būdus, kainų grupes, finansines dimensijas ir pristatymo būdus. Šias parinktis galite konfigūruoti kurdami skambučių centrą. **Svarbu:** prieš naudojant skambučių centro darbo eigą, kai vartotojas kuria pardavimo užsakymus, vartotojas privalo būti priskirtas skambučių centrui kaip skambučių centro vartotojas. Galite naudoti puslapį **Skambučių centras**, norėdami įjungti arba išjungti unikalių skambučių centrų funkcijų grupes. Galima įjungti toliau nurodytas funkcijų grupes.

-   **Užsakymo baigimas** – ši grupė apima funkcijas, susijusias su mokėjimais ir užsakymo baigimu puslapyje **Pardavimo užsakymas**.
-   **Tiesioginis pardavimas** – ši grupė apima funkcijas, susijusias su šaltinio kodais, scenarijais ir katalogų užklausomis.

Kai įjungiate šias funkcijas skambučių centro parametruose, puslapyje **Pardavimo užsakymas** jas gali pasiekti su skambučių centru susieti vartotojai. Norint naudoti daugumą šių funkcijų, reikia atlikti papildomą nustatymą. Kaip konkretaus skambučių centro tiesioginio pardavimo parametro dalis suaktyvinami vaizdai ir scenarijai. Jei šios funkcijos įjungtos, scenarijai ir produktų vaizdai yra rodomi puslapio **Pardavimo užsakymas** „FactBox“ srityje. Rodomas nustatytas numatytasis produkto vaizdas. Galima sukonfigūruoti prekės, katalogo, kliento arba prekės katalogo kontekste scenarijus. Skambučių centro užsakymuose gali būti rodoma papildoma informacija apie tai, kaip buvo gauta konkrečios užsakymo eilutės kaina. Pavyzdžiui, užsakymuose rodoma, kurios nuolaidos buvo pritaikytos. Šią funkciją įgalinkite **Gautinos sumos** &gt; **Sąranka** &gt; **Gautinų sumų parametrai** &gt; **Kainos** &gt; **Kainų informacija**. Puslapį **Kainų informacija** galima atidaryti išplečiamajame sąraše **Pardavimo užsakymo eilutė**. Užsakymų įvykių sekimą galite naudoti auditui, norėdami peržiūrėti su užsakymu susijusius veiksmus užsakymo naudojimo laikotarpiu, arba norėdami stebėti konkretaus vartotojo veiksmus. Pavyzdžiui, galite registruoti veiksmą kiekvieną kartą, kai vartotojas sukuria pardavimo užsakymą, nustato užsakymo sulaikymą, nepaiso mokesčio arba atnaujina užsakymo eilutę. Galite nustatyti užsakymų įvykių funkcija, kad būtų sekami konkrečių vartotojų, vartotojų grupių arba visų vartotojų veiksmai konkrečiu laikotarpiu. Galite peržiūrėti su dokumentu atliktus veiksmus, to dokumento puslapio veiksmų srityje atidarydami puslapį **Užsakymo įvykiai**. Užsakymo įvykius galite konfigūruoti **Pardavimas ir rinkodara** &gt; **Sąranka** &gt; **Įvykiai** &gt; **Užsakymo įvykiai**. Kai kliento užsakymo negalima pristatyti laiku, įmonė gali automatiškai klientui siųsti pranešimų el. laiškus norėdama paaiškinti užsakymo būseną ir suteikti klientui galimybę atšaukti užsakymą. Jei vėluojama daugiau negu nurodyta ribinė vertė, užsakymą galima atšaukti automatiškai. Nustatytais laiko intervalais galima išsiųsti iki trijų toliau nurodytų el. laiškų.

1.  **Pirmasis atšaukimo pranešimas** – klientas gali atšaukti užsakymą.
2.  **Antrasis atšaukimo pranešimas** – klientas gali atšaukti užsakymą.
3.  **Galutinis atšaukimo pranešimas** – sistema atšaukia užsakymą, o klientui pranešama apie atšaukimą.

Atskiriems klientams galite automatiškai nepranešti, o produktams netaikyti atšaukimo proceso. Įspėjimas dėl maržos suaktyvinamas, kai įtraukiate prekę į užsakymą. Įspėjime pateikiama svarbi informacija apie prekę, pvz., kainos maržą ir prekės pelningumą. Galite naudoti šią informaciją norėdami nuspręsti, ar kainos perrašymas yra tinkamas, kai įtraukiate prekę į pardavimo užsakymą. Pavyzdžiui, galite nustatyti prekybos maržų ribines vertes, norėdami nurodyti, kad 40 ar daugiau procentų už prekės savikainą didesnė ribinė reikšmė yra priimtina, o nuo 20 iki 39 procentų – abejotina. Šiuo atveju bet kuri prekė, kurios ribinė reikšmė yra nuo 20 iki 39 procentų, suaktyvina įspėjimą. Bet kuri prekė, kurios ribinė reikšmė yra mažesnė nei 20 procentų už prekės savikainą, negali būti parduota, o prekės kainos negalima koreguoti. Įspėjimus dėl maržos galite konfigūruoti **Gautinos sumos** &gt; **Sąranka** &gt; **Gautinų sumų parametrai** &gt; **Įspėjimai dėl maržos**. Kai nustatote PVM priskyrimą pagal numatytąsias taisykles, galite nustatyti adreso elementų atitikimo prioritetą. Pavyzdžiui, galite nurodyti, kad PVM grupės atitikimas pagal pašto indeksą turi didesnį prioritetą nei PVM grupės atitikimas pagal apskritį. Kai įvedate naujų klientų adresų įrašų, PVM grupė automatiškai priskiriama pagal tai, kaip kliento adresas atitinka numatytąsias taisykles ir jūsų apibrėžtą prioritetinį atitikimą. Šią funkciją galite konfigūruoti puslapyje **DK parametrai**.





---
title: Operacijų planavimas
description: Šioje temoje pateikiama informacija apie operacijų planavimą. Galite naudoti operacijų planavimą, norėdami bendrai įvertinti gamybos procesą per tam tikrą laikotarpį.
author: ChristianRytt
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 94ac865db8a01f6b3c72e3a8851d6be4fe2ce0cf9faaa21bdb0d465605066b4f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734144"
---
# <a name="operations-scheduling"></a>Operacijų planavimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie operacijų planavimą. Galite naudoti operacijų planavimą, norėdami bendrai įvertinti gamybos procesą per tam tikrą laikotarpį.

Gamybą galite planuoti operacijos lygiu ir darbo lygiu. Lyginant su užduočių planavimu, operacijų planavimo metu maršruto gamybos operacijos neišskaidomos į užduotis. Jei norite įtraukti daugiau planavimo informacijos, pavyzdžiui, apie dabartinį pajėgumą, galite paleisti užduočių planavimą po to, kai įvykdėte operacijų planavimą. Taip pat galite paleisti tik užduočių planavimą. Užduočių planavimas paprastai naudojamas norint planuoti atskiras darbo laiko užduotis, kurios bus atliekamos iškart arba greitai.

## <a name="components-of-operations-scheduling"></a>Operacijų planavimo komponentai
Pagrindiniai operacijų planavimo komponentai yra planavimo krytis, išteklių pajėgumai ir medžiagų optimizavimas. Naudodami operacijų planavimą, galite pasiekti tolesnius tikslus.

-   Kontroliuoti planavimo metodą planuodami į priekį arba atgal tam tikros datos.
-   Optimizuoti išteklių panaudojimą planuodami gamybą pagal išteklių pajėgumą. Šis metodas taip pat padeda nustatyti, kada naudoti alternatyvius išteklius.
-   Optimizuoti medžiagų panaudojimą planuodami gamybą pagal reikiamų medžiagų pasiekiamumą.
-   Planuoti ir sinchronizuoti gamybos nuorodas. Kai gamybos užsakymo grafikas pakeičiamas, pakoreguojamos gamybos nuorodų datos.

Operacijų planavimą galima atlikti tik įvertinus gamybos užsakymo sąnaudas. Jei įvertinimo neatliksite, jis bus atliktas automatiškai prieš inicijuojant operacijų planavimo procesą. Operacijų grafike nurodoma tolesnė informacija.

-   Produktas, kurį planuojama gaminti
-   Produkto konfigūracija.
-   Kiekiai, įtraukti į gamybą
-   Gamybos pradžios ir pabaigos datos
-   Išteklių, kurie atlieka gamybos veiklas, pajėgumo rezervavimai

Gamybos operacijų sąrankos laikas, vykdymo laikas ir apdorojimo laikas. Atlikus operacijų planavimą, gamybos užsakymo būsena tampa **Suplanuotas** ir visos operacijos suplanuojamos gamybos maršrute nurodyta tvarka. Tačiau nurodoma tik operacijos trukmė. Pradžios ir pabaigos laikas nenurodomas.

## <a name="scheduling-direction-and-date"></a>Planavimo kryptis ir data
Planavimo kryptis yra esminė planavimo proceso dalis. Gamybą galima planuoti pirmyn arba atgal nuo bet kurios datos, atsižvelgiant į laiko ir planavimo poreikius.

-   **Į priekį nuo planavimo datos** – galite planuoti, kad gamyba būtų pradedama kaip įmanoma anksčiau. Gamybą galima pradėti šiandien, rytoj ar nuo bet kurios kitos datos ateityje. Gamyba suplanuojama suplanuojamą į priekį iki anksčiausios galimos pabaigos datos.
-   **Atgal nuo planavimo datos** – galite planuoti, kad gamyba būtų pradedama kaip įmanoma vėliau. Atgalinis planavimas nustatomas pagal datą, kurią gamyba turi būti baigta. Grafikas atgal nuo tos datos iki vėliausios galimos datos, kada galima pradėti gamybą ir baigti laiku.

## <a name="resource-scheduling"></a>Išteklių planavimas
Paleidus operacijų grafiką, suplanuojama kiekviena nurodyto operacijos ištekliaus gamybos maršruto operacija. Be to, gamybos maršrute nurodoma kiekvienos operacijos trukmė. Jei nurodyta operacijos išteklių grupė, planuojant rezervuojamas grupės pajėgumas. Tačiau, skirtingai nei atliekant užduočių planavimą, operacijų planavimo metu konkretūs grupės ištekliai nėra pasirenkami. Jei pajėgumas yra ribotas, grafikas priklauso nuo išteklių, reikalingų gamybai atlikti, prieinamumo. Operacijų planavimas vykdomas pagal gamybos maršrute nurodytą operaciją seką. Planavimas rezervuoja pajėgumą išteklių grupėse pagal operacijų laiką, nurodytą gamybos maršruto. Naudojamų išteklių galimų pajėgumų suma nurodo išteklių grupės pajėgumą. Esami išteklių pajėgumų rezervavimai laikomi neprieinamu pajėgumu. Jei nėra pakankamai pajėgumų gamybai vykdyti, gamybos užsakymus galima atidėti arba net sustabdyti. Taip pat galite nurodyti į gamybą įtrauktų išteklių efektyvumą, kurio tikitės. Ištekliaus efektyvumas nurodomas procentais. Efektyvumo procentas reguliuoja ištekliaus našumą. Šis koregavimas keičia ištekliui rezervuotą laiką. Atitinkamai pakoreguojamas operacijų, naudojančių išteklių, vykdymo laikas.

## <a name="operations-scheduling-and-master-planning"></a>Operacijų planavimas ir bendrasis planavimas
Operacijų planas taip pat veikia bendrąjį planavimą ir lemia visų reikalingų medžiagų apskaičiavimus. Atliekant operacijų planavimą naudojama tolesnė informacija.

-   **Neatliktą gamyba** – produktai, kurie suplanuoti, išleisti arba pradėti.
-   **Medžiagų turimumas** – atsargos, antrinė gamyba, tiekėjai
-   **Turimas pajėgumas** – ištekliai, reikalingi gamybai baigti

> [!NOTE]
> Jei naudojate kelių gijų bendrąjį planavimą ir operacijų planavimą, į ribotą pajėgumą neatsižvelgiama. 

## <a name="cancellations"></a>Atšaukimai
Paleidus operacijų planavimą, galima atšaukti tam tikras maršruto dalis. Šios dalys apima laukimo eilėje laiką, sąrankos laiką, vykdymo laiką, persidengiantį laiką ir transportavimo laiką.

## <a name="finite-materials"></a>Ribotos medžiagos
Jei dirbate su ribotomis medžiagomis, planavimas taip pat priklauso nuo medžiagų, kurių reikia gamybai, turimumo. Jei neužtenka komponentų, reikalingų gamybai, gamybą galima atidėti. Galite pagrįsti planavimą medžiagų naudojimu, nurodydami gamybos medžiagas, kurios turi būti prieinamos. Kai optimizuojame tiek išteklių pajėgumą, tiek medžiagų prieinamumą, gamyba apskaičiuojama pagal šiuos apribojimus. Negalima suplanuoti gamybos užsakymo vykdymo pradžios, jei tuo pačiu metu nėra reikiamo kiekio pajėgumo ir medžiagų.

## <a name="additional-resources"></a>Papildomi ištekliai

[Operacijų planavimo parinktys](operation-scheduling-options.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
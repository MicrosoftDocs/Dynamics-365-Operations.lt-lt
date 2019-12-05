---
title: Įmonės koncepcija „Common Data Service“
description: Šioje temoje aprašomas įmonės duomenų integravimas tarp „Finance and Operations“ ir „Common Data Service“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 21c2143f4fa58d51f64e349c7963cb17e04bad97
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772442"
---
## <a name="company-concept-in-common-data-service"></a>Įmonės koncepcija „Common Data Service“

[!include [banner](../includes/banner.md)]

„Finance and Operations“ *įmonės* koncepcija yra tiek teisinis, tiek verslo konstruktas. Ji taip pat apibrėžia duomenų saugos ir matomumo ribas. Vartotojai visada dirba vienos įmonės kontekste, o dauguma duomenų yra įmonės suskirstyti.

„Common Data Service“ nenaudojama lygiavertė koncepcija. Artimiausia koncepcija yra *verslo struktūros vienetas*, kuris pirmiausia apima vartotojo duomenų saugos ir matomumo ribas. Ši koncepcija neturi tokios pačios teisinės ar verslo reikšmės kaip įmonės koncepcija.

Verslo struktūros vienetas ir įmonė nėra lygiavertės koncepcijos, todėl „Common Data Service“ integracijos tikslais negalima taikyti jų vienas su vienu (1:1) susiejimo. Tačiau vartotojai turi, kaip numatyta, galėti peržiūrėti tuos pačius įrašus programoje ir „Common Data Service“, todėl „Microsoft“ pristatė naują subjektą „Common Data Service”, kuris pavadintas cdm\_Company. Šis objektas yra lygiavertis įmonės objektui programoje. Siekiant užtikrinti įrašų matomumo lygiavertiškumą pradėjus naudoti programą ir „Common Data Service“, rekomenduojame toliau pateiktus „Common Data Service“ duomenų nustatymus.

+ Kiekvienam „Finance and Operations“ įmonės įrašui, kuris įgalintas dvigubam rašymui, sukuriamas susietas cdm\_Company įrašas.
+ Sukūrus cdm\_Company įrašą ir įgalinus dvigubam rašymui, sukuriamas numatytasis verslo struktūros vienetas tuo pačiu pavadinimu. Nors tam verslo struktūros vienetui automatiškai sukuriama numatytoji komanda, verslo struktūros vienetas nėra naudojamas.
+ Sukuriama atskira savininko komanda tokiu pačiu pavadinimu. Ji taip pat susiejama su verslo struktūros vienetu.
+ Pagal numatytuosius nustatymus, bet kurio įrašo, kuris sukuriamas ir įrašomas dvigubu rašymu „Common Data Service“, savininkas nustatomas į „DW Owner“ komandą, kuri susiejama su susijusiu verslo struktūros vienetu.

Tolesnėje iliustracijoje pateikiamas šio duomenų nustatymo „Common Data Service“ pavyzdys.

![Duomenų nustatymas „Common Data Service“](media/dual-write-company-1.png)

Dėl tokios konfigūracijos bet koks įrašas, susietas su USMF įmone, priklauso komandai, kuri yra susieta su USMF verslo struktūros vienetu „Common Data Service“. Todėl tuos įrašus gali matyti bet kuris vartotojas, kuris turi prieigą prie to verslo struktūros vieneto pasitelkiant saugos vaidmenį, kuris nustatytas verslo struktūros vieneto lygio matomumui. Toliau pateikiamas pavyzdys, kaip komandos gali būti naudojamos norint suteikti tinkamą prieigą prie tų įrašų.

+ Vaidmuo „Pardavimo vadybininkas“ priskiriamas „USMF pardavimas“ komandos nariams.
+ Vartotojai, turintys vaidmenį „Pardavimo vadybininkas“, turi prieigą prie visų paskyros įrašų, kurie yra to paties verslo struktūros vieneto nariai.
+ „USMF pardavimas“ komanda susiejama su anksčiau minėtu USMF verslo struktūros vienetu.
+ Todėl „USMF pardavimas“ komandos nariai gali matyti bet kurią paskyrą, priklausančią „USMF DW“ vartotojui, kuris būtų gautas iš USMF įmonės objekto naudojant „Finance and Operations“.

![Komandų naudojimas](media/dual-write-company-2.png)

Kaip parodyta ankstesnėje iliustracijoje, šis 1:1 susiejimas tarp verslo struktūros vieneto, įmonės ir komandos yra tik pradžios taškas. Tolesniame pavyzdyje naujas verslo struktūros vienetas „Europa“ rankiniu būdu sukuriamas „Common Data Service“ kaip DEMF ir ESMF pirminis elementas. Šis naujas šakninis verslo struktūros vienetas nėra susijęs su dvigubu rašymu. Tačiau jis gali būti naudojamas siekiant suteikti „EUR pardavimas“ komandos nariams prieigą prie paskyros duomenų tiek DEMF, tiek ESMF nustatant duomenų matomumą į **Pirminis/antrinis BU** susietam saugos vaidmeniui.

Paskutinėje temoje aptariama, kaip dvigubas rašymas nustato, kuriai savininkų komandai reikėtų priskirti įrašus. Šią veikseną kontroliuoja laukas **Numatytoji komanda savininkė** įraše cdm\_Company. Kai cdm\_Company įrašas yra įgalintas dvigubam rašymui, priedas automatiškai sukuria susietą verslo struktūros vienetą ir savininko komandą (jei jos dar nėra) ir nustato lauką **Numatytoji komanda savininkė**. Administratorius gali pakeisti šį lauką kita reikšme. Tačiau administratorius negali išvalyti lauko tol, kol objektui įgalintas dvigubas rašymas.

> [!div class="mx-imgBorder"]
![Laukas Numatytoji komanda savininkė](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Įmonės paskirstymas ir įkėlimas

„Common Data Service“ integracija suteikia įmonės lygiavertiškumą naudojant įmonės identifikatorių, skirtą paskirstyti duomenis. Kaip parodyta toliau pateiktoje iliustracijoje, visi konkrečios įmonės objektai išplečiami taip, kad su cdm\_Company objektu turėtų ryšį „daugelis su vienu“ (N:1).

> [!div class="mx-imgBorder"]
![N:1 ryšys tarp konkrečios įmonės objekto ir cdm_Company objekto](media/dual-write-bootstrapping.png)

+ Įtraukus ir įrašius įmonę įrašų reikšmė tampa skirta tik skaityti. Todėl vartotojai turėtų įsitikinti, kad pasirinko tinkamą įmonę.
+ Tik tie įrašai, kurie apima įmonės duomenis, gali būti dvigubo rašymo tarp programos ir „Common Data Service“.
+ Esamiems „Common Data Service“ duomenims netrukus bus teikiama administratoriaus vadovaujama įkėlimo patirtis.

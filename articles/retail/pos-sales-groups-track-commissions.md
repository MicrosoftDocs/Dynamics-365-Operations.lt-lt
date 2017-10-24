---
title: Sekti EKA komisinius naudojant pardavimo grupes
description: "Mažmeninėje prekyboje įprasta sekti pardavimus pagal su klientu dirbusį atstovą, kuris teikė pagalbą, atliko papildomą pardavimą, kryžminį pardavimą ir operacijos apdorojimą."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dcc136f658a06c0bcea4736e4512dce6e8e18fa8
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Sekti EKA komisinius naudojant pardavimo grupes

[!include[banner](includes/banner.md)]


Mažmeninėje prekyboje įprasta sekti pardavimus pagal su klientu dirbusį atstovą, kuris teikė pagalbą, atliko papildomą pardavimą, kryžminį pardavimą ir operacijos apdorojimą.

Sekant pardavimo atstovo pardavimus matuojamos atstovo pardavimo galimybės, o iš kasininko pardavimų galima spręsti apie greitį ir našumą. Pardavimo atstovo sekami pardavimai taip pat dažnai naudojami norint apskaičiuoti komisinius arba kitas paskatas.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Darbuotojo konfigūravimas būti EKA pardavimo atstovu
Kai darbuotojas įtraukiamas į pardavimo grupę, jam gali būti paskiriami komisiniai ir sistemoje jis gali būti identifikuojamas kaip pardavimo atstovas. Darbuotojui, kuris nėra pardavimo grupėje, komisiniai negali būti skiriami ir jis nebus įtraukiamas į elektroninio kasos aparato (EKA) programos sąrašus kaip pardavimo atstovas. EKA pardavimo atstovų sąrašai sudaromi iš visų pardavimo grupių, kuriose yra bent vienas parduotuvei priskirtas darbuotojas. Sąrašas rodomas EKA kaip pardavimo grupės ID ir pavadinimo (ID : Pavadinimas) derinys. Numatytąją pardavimo grupę darbuotojams galima priskirti norint, kad būtų palaikomi scenarijai, kai mažmenininkas nusprendžia pardavimo atstovą nustatyti automatiškai EKA eilutėse. Vartotojai gali pasirinkti bet kurią pardavimo grupę, kurioje darbuotojas yra narys.

## <a name="functionality-profile-settings"></a>Funkcijų šablono parametrai
Yra keletas parduotuvės funkcijų šablono parametrų, kuriuos naudojant nustatomas EKA srautas ir procesas ir kurie skirti pardavimo atstovams.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Šablonas**                           | **Aprašas**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Pagal numatytuosius nustatymus nustatyti kasininką, kai įmanoma** | Jei ši parinktis įjungta, EKA automatiškai sukuria operacijų eilutes, kuriose nurodoma dabartinio kasininko numatytoji pardavimo grupė. Jei numatytoji kasininko pardavimo grupė nenurodyta, vertė nenustatoma. Vartotojas vis tiek gali pats nustatyti pardavimo grupę naudodamas EKA mygtukyno mygtuką.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Raginimas nurodyti pardavimo atstovą**   | Galimos trys šios parinkties vertės: **Ne **– pasirinkus šią parinktį vartotojas nebus raginamas pasirinkti pardavimo grupės. Vertę vis tiek galima nustatyti naudojant numatytąją kasininko pardavimo grupę („Sales“) arba mechaniškai naudojant EKA mygtukyno mygtuką. **Operacijos pradžia** – jeigu pasirinkta ši parinktis ir arba neįjungta parinktis **Pagal numatytuosius nustatymus nustatyti kasininką**, arba dabartiniam kasininkui nepriskirta numatytoji pardavimo grupė, kiekvienos operacijos pradžioje vartotojas bus paragintas pasirinkti pardavimo grupę. Pasirinkus pardavimo grupę pagal šį raginimą visos kitos pasirinktos pardavimo grupės eilutės bus numatytosios. Vartotojas vis tiek gali pats nustatyti pardavimo grupę naudodamas EKA mygtukyno mygtuką. **Kiekvienai eilutei** – jeigu pasirinkta ši parinktis ir arba neįjungta parinktis **Pagal numatytuosius nustatymus nustatyti kasininką**, arba dabartiniam kasininkui nepriskirta numatytoji pardavimo grupė, įtraukęs kiekvieną eilutę vartotojas bus paragintas pasirinkti pardavimo grupę. Vartotojas vis tiek gali pats nustatyti pardavimo grupę („Sales“) naudodamas EKA mygtukyno mygtuką. |
| **Reikia**                           | Ši parinktis taikoma tik tada, kai sukonfigūruota, jog EKA ragintų nurodyti pardavimo atstovą. Jei parinktis įjungta, norėdamas tęsti vartotojas turės pasirinkti pardavimo grupę. Priešingu atveju vartotojas paraginamas, bet gali atšaukti ir tęsti nepasirinkęs. Įtraukus eilutę reikiamą kiekį leidimų turintis vartotojas vis tiek gali pašalinti pardavimo grupę iš eilutės. Šiuo atveju parinktis „Prašyti pardavimo atstovo“ nėra priverstinė.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Informacijos apie pardavimo atstovą rodymas EKA operacijų ekrane
EKA operacijos ekraną ir turinį galima konfigūruoti naudojant ekrano išdėstymo kūrimo priemonę ir priskirti ekrano išdėstymus parduotuvėms, registrams arba darbuotojams. Lauką **Pardavimo atstovas** galima įtraukti į Kvitų srities skirtuką Eilutės.  Taip bus rodomas kiekvienos operacijos ekrano eilutės nurodytos pardavimo grupės ID.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Pardavimo atstovo operacijų įtraukimas į EKA mygtukynus
Naudodamiesi EKA vartotojai gali konfigūruoti į ekrano išdėstymus įtraukiamus mygtukynus, kad juose būtų pateikiama prieiga prie EKA operacijų. Toliau nurodytas EKA operacijas galima priskirti pardavimo atstovams skirtiems mygtukyno mygtukams.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Operacija**                             | **Aprašas**                                                                                                                                                                                                                                                                              |
| Nustatyti pardavimo atstovą eilutėje          | EKA operacijoje rodomas tinkamų parduotuvės pardavimo grupių (ID : Pavadinimas) sąrašas. Šiame sąraše pasirinkus pardavimo grupę („Sales“) nustatoma dabartinės operacijos eilutės vertė.                                                                                                            |
| Išvalyti pardavimo atstovą eilutėje        | Atliekant šią EKA operaciją iš dabartinės operacijos eilutės pašalinama dabartinė pardavimo grupės („Sales“) vertė.                                                                                                                                                                                                  |
| Nustatyti operacijos pardavimo atstovą   | EKA operacijoje rodomas tinkamų parduotuvės pardavimo grupių (ID : Pavadinimas) sąrašas. Šiame sąraše pasirinkus pardavimo grupę („Sales“) nustatoma numatytoji dabartinės operacijos vertė. Nustatomos visos esamos eilutės, kurioms nepriskirta pardavimo grupė, taip pat visos vėliau įtrauktos eilutės. |
| Išvalyti operacijos pardavimo atstovą | Atliekant šią EKA operaciją iš dabartinės operacijos pašalinama dabartinė numatytoji pardavimo grupės („Sales“) vertė. Tai neturi įtakos kitoms jau esamoms operacijos eilutėms.                                                                                                                             |

## <a name="calculating-commissions"></a>Komisinių skaičiavimas
Nurodytų pardavimo grupių darbuotojų komisiniai skaičiuojami registruojant išrašą arba pardavimo užsakymą. Komisinių suma nustatoma pagal pardavimo grupėje nurodytą darbuotojo komisinių dalį ir susijusius klientui ir (arba) operacijos produktui taikomus komisinių skaičiavimo parametrus.





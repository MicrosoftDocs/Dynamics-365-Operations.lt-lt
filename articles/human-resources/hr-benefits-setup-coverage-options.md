---
title: Padengimo parinkčių kūrimas
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009884"
---
# <a name="create-coverage-options"></a>Padengimo parinkčių kūrimas

[!include [banner](includes/preview-feature.md)]

„Microsoft Dynamics 365 Human Resources“ padengimo parinktys yra padengimo lygiai, skirti išmokų plano ar programos dalyviams išrinkti, pvz., medicinos planas, skirtas tik darbuotojams, arba gyvybes draudimo planas, skirtas gaunantiems 2 x atlyginimus. Apibrėžus išmokų padengimo parinktis, galima jas naudoti pakartotinai, taip pat galite susieti parinktį su vienu ar daugiau planų.

Apibrėžę padengimo parinktis, susiekite padengimo parinktis su išmokų plano tipu. Tada plano tipas susiejamas su išmokų planu ar programa. Su plano tipu susietas parinktis bus galima taikyti visiems planams, sukurtiems, naudojant šį plano tipą. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Padengimo parinktys**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Padengimo parinktis** | Unikalus padengimo parinkties pavadinimas. |
   | **Aprašas** | Padengimo parinkties aprašas. |
   | **Padengimo kodas** | Pagal padengimo kodus kiekvienam reikalavimus atitinkančiam dengiamam asmens tipui priskiriama mažiausia ir didžiausia suma. Padengimo kodas nurodo, kas yra dengiamas, arba plano tipui leidžiamą padengimo sumą. Padengimo suma galima išreikšti doleriais arba procentais. Pavyzdys:</br></br>- **„Emp+1“** – kad būtų tinkamas, darbuotojas turi būti pasirinkęs vieną priklausomąjį (jei pasirinkta daugiau nei vienas, darbuotojas nebetinka).</br></br>- **„Emp+family“** – kad būtų tinkamas, darbuotojas turi būti pasirinkęs bent du priklausomuosius. |
   | **Didžiausias skaičius** | Didžiausias priklausomųjų skaičius. |
   | **Būsena** | Padengimo parinkties būsena. Jei padengimo parinkties būsena nustatyta kaip neaktyvi, plano tipų padengimo parinkčių pasirinkti negalima. |
   | **Procentas** | Procentinė suma. Šis laukas yra aktyvus tik tada, kai padengimo kodo lauke buvo pasirinkta % x atlyginimas. |
   | **Daliklis** | Skaičiuojant naudojamas daliklis, kai pasirenkamas padengimo kodas % x atlyginimas. |
   | **Mažiausias procentas** | Mažiausias procentinis dydis, kai pasirenkamas padengimo kodas procentais. |
   | **Didžiausias procentas** | Didžiausias procentinis dydis, kai pasirenkamas padengimo kodas procentais. |

4. Dalyje **Asmeninio kontakto tinkamumo parinktys**pridėkite tinkamą asmeninių kontaktų tinkamumo parinktį, skirtą kiekvienai padengimo parinkčiai.

5. Dalyje **Savitarna** nurodykite šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Leisti darbuotojo įnašo sumą** | Nurodo, ar leisti darbuotojams keisti įnašo sumą išmokų savitarnoje, kai jie renkasi išmokas. Jei pažymėsite šį žymės langelį, sistema apskaičiuos išmokų plano parametrus pagal įnašo sumą, kurią darbuotojas įveda išmokų savitarnoje. |
   | **Leisti darbuotojo padengimo sumą** | Nurodo, ar leisti darbuotojams keisti padengimo sumą išmokų savitarnoje, kai jie renkasi išmokas. Jei pažymėsite šį žymės langelį, sistema apskaičiuos išmokų plano parametrus pagal padengimo sumą, kurią darbuotojas įveda darbuotojų savitarnoje. |

6. Pasirinkite **Įrašyti**. 

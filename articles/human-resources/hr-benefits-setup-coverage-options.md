---
title: Padengimo parinkčių kūrimas
description: „Microsoft Dynamics 365 Human Resources” padengimo parinktys yra padengimo lygiai, skirti išmokų plano ar programos dalyviams išrinkti.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9f67a97ec57bade840e1035c6011b94427a77c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055585"
---
# <a name="create-coverage-options"></a>Padengimo parinkčių kūrimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

„Microsoft Dynamics 365 Human Resources” padengimo parinktys yra padengimo lygiai, skirti išmokų plano ar programos dalyviams išrinkti. Pvz., padengimo parinktys gali apimti medicinos planą, skirtą **tik darbuotojams**, arba gyvybės draudimo planą, skirtą gaunantiems **2 x atlyginimus**. Apibrėžus išmokų padengimo parinktis, jas galima naudoti pakartotinai. Galite susieti parinktį su vienu ar daugiau planų.

Apibrėžę padengimo parinktis, susiekite padengimo parinktis su išmokų plano tipu. Tada plano tipas susiejamas su išmokų planu ar programa. Su plano tipu susietas parinktis galima taikyti visiems planams, sukurtiems, naudojant šį plano tipą. 

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

4. Dalyje **Asmeninio kontakto tinkamumo parinktys** pridėkite tinkamą asmeninių kontaktų tinkamumo parinktį, skirtą kiekvienai padengimo parinkčiai.

5. Dalyje **Savitarna** nurodykite šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Leisti darbuotojo įnašo sumą** | Nurodo, ar leisti darbuotojams keisti įnašo sumą išmokų savitarnoje, kai jie renkasi išmokas. Jei pažymėsite šį žymės langelį, sistema apskaičiuos išmokų plano parametrus pagal įnašo sumą, kurią darbuotojas įveda išmokų savitarnoje. |
   | **Leisti darbuotojo padengimo sumą** | Nurodo, ar leisti darbuotojams keisti padengimo sumą išmokų savitarnoje, kai jie renkasi išmokas. Jei pažymėsite šį žymės langelį, sistema apskaičiuos išmokų plano parametrus pagal padengimo sumą, kurią darbuotojas įveda darbuotojų savitarnoje. |

6. Pasirinkite **Įrašyti**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
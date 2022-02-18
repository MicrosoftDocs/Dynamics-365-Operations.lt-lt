---
title: Padengimo parinkčių kūrimas
description: Šioje temoje paaiškintos „Microsoft Dynamics 365 Human Resources” padengimo parinktys yra padengimo lygiai, skirti išmokų plano ar programos dalyviams išrinkti.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 01eb0c56578cf6f6b070c4a05768ec5361993555
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065873"
---
# <a name="create-coverage-options"></a>Padengimo parinkčių kūrimas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Padengimo galimybės nustato tai, kas turėtų būti apdraustas arba tai, koks padengimas yra galimas draudimo plane. Pavyzdžiui, medicininiame plane galite turėti **tik darbuotojas** parinktį, **darbuotojas + 1** parinktį ir **šeima** parinktį. Gyvybės draudimui galite pasiūlyti **1 x atlyginimo** arba **2 x atlyginimo** padengimą.

Apibrėžę išmokų padengimo parinktis, jas galite naudoti pakartotinai. Galite susieti parinktį su vienu ar daugiau planų.

> [!IMPORTANT]
> Apibrėžę padengimo parinktis, susiekite jas su išmokų plano tipu. Tada plano tipas susiejamas su išmokų planu ar programa. Su plano tipu susietas parinktis galima taikyti visiems sukurto tipo planams.

## <a name="create-coverage-options"></a>Padengimo parinkčių kūrimas
1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Padengimo parinktys**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Padengimo parinktis** | Unikalus padengimo parinkties pavadinimas. |
   | **Aprašas** | Padengimo parinkties aprašas. |
   | **Padengimo kodas** | Pagal padengimo kodus kiekvienam reikalavimus atitinkančiam dengiamam asmens tipui priskiriama mažiausia ir didžiausia suma. Padengimo kodas nurodo, kas yra dengiamas, arba plano tipui leidžiamą padengimo sumą. Padengimo suma galima išreikšti doleriais arba procentais. Pavyzdys:<ul><li>**Darbuotojas+1** – tam, kad būtų tinkamas, darbuotojas turi būti pasirinkęs vieną priklausomąjį (jei pasirinkta daugiau nei vienas, darbuotojas nebetinka).</li><li>**Darbuotojas+šeima** – tam, kad būtų tinkamas, darbuotojas turi būti pasirinkęs bent du priklausomuosius.</li></ul> |
   | **Didžiausias skaičius** | Didžiausias priklausomųjų skaičius. |
   | **Būsena** | Padengimo parinkties būsena. Jei padengimo parinkties būsena nustatyta kaip **neaktyvi**, plano tipams negalima pasirinkti padengimo parinkties. |
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

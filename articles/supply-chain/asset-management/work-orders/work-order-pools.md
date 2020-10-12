---
title: Darbo užsakymų telkiniai
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas dirbti su darbo užsakymų telkiniais.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3e95a4fdfaf4817867f3d2df7774df6a27ee6599
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889510"
---
# <a name="work-order-pools"></a>Darbo užsakymų telkiniai

[!include [banner](../../includes/banner.md)]


Naudodami darbo užsakymų telkinius, galite grupuoti kažką bendra turinčius darbo užsakymus. Toliau pateikti keli objektų, kuriems galite sukurti darbo užsakymų telkinius, pavyzdžiai:

- Darbo brigados, pavyzdžiui, A priežiūros brigada, B priežiūros brigada  

- Profesiniai įgūdžiai, pavyzdžiui, elektrikai ar santechnikai  

- Fizinės vietos  

- Grafikai, pavyzdžiui, savaičių ar kitų laikotarpių  

Kai reikia, vieną darbo užsakymą galite naudoti keliuose darbo užsakymų telkiniuose.


## <a name="create-a-work-order-pool"></a>Darbo užsakymų telkinio kūrimas

Sąrašo puslapyje **Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai** galite apžvelgti savo darbo užsakymų telkinius ir kurti naujus telkinius.

1. Pasirinkite **Turto valdymas** > **Bendra** > **Darbo užsakymų telkiniai** > **Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai**.

2. Pasirinkite **Naujas**.

3. Lauke **Telkinys** įveskite darbo užsakymų telkinio ID.

4. Lauke **Pavadinimas** įveskite pavadinimą.

5. Nustatykite parinkties **Aktyvus** reikšmę **Taip**, jei norite nurodyti, kad darbo užsakymų telkinys yra aktyvus.

6. Nustatykite parinkties **Panaikinti darbo užsakymų ryšius** reikšmę **Taip**, jei darbo užsakymai turi būti automatiškai pašalinami iš darbo užsakymų telkinio.

7. Lauke **Naikinti ciklo būseną** pasirinkite darbo užsakymo ciklo būseną. Pavyzdžiui, darbo užsakymo įvykdymo ciklo būseną galima nustatyti taip, kad būtų automatiškai panaikinami ryšiai su darbo užsakymų telkiniais.

    Į darbo užsakymų telkinį darbo užsakymus galite pradėti įtraukti iš karto.

8. „FastTab“ **Darbo užsakymai** pasirinkite **Įtraukti eilutę**.

9. Lauke **Darbo užsakymas** pasirinkite darbo užsakymą. Susiję laukai automatiškai atnaujinami.

10. Norėdami pridėti daugiau darbo užsakymų, pakartokite 8–9 veiksmus.

11. Jei įtraukti darbo užsakymai turi būti atlikti tam tikrame užsakyme, lauke **Rūšiavimo tvarka** galite įvesti skaičius **1**, **2**, **3** ir t. t., kad nurodytumėte užsakymą.

12. Norėdami peržiūrėti visų darbo užsakymų, įtrauktų į darbo užsakymų telkinį, sąrašą, veiksmų srityje, esančioje skirtuke **Darbo užsakymų telkinys**, grupėje **Peržiūrėti susijusių darbo užsakymų telkinį**, pasirinkite **Darbo užsakymai**, kad atidarytumėte sąrašo puslapį **Visi darbo užsakymai**.

13. Norėdami apskaičiuoti ir peržiūrėti priežiūros grafiko, nesuplanuotų darbo užsakymų ir suplanuotų darbo užsakymų pajėgumą, veiksmų srityje, esančioje skirtuke **Darbo užsakymų telkinys**, grupėje **Peržiūrėti susijusių darbo užsakymų telkinį**, pasirinkite **Pajėgumas**, kad atidarytumėte dialogo langą **Pajėgumo skaičiavimas**.

14. Norėdami apskaičiuoti ir peržiūrėti su priežiūros grafiku, nesuplanuotais darbo užsakymais ir suplanuotais darbo užsakymais susijusių elementų (atsarginių dalių ir kitų reikalingų elementų) prognozes, veiksmų srityje, esančioje skirtuke **Darbo užsakymų telkinys**, grupėje **Peržiūrėti susijusių darbo užsakymų telkinį**, pasirinkite **Elemento prognozė**, kad atidarytumėte dialogo langą **Apskaičiuoti elemento prognozę**.

15. Norėdami peržiūrėti pirkimo paraiškų, susijusių su darbo užsakymais, esančiais darbo užsakymų telkinyje, sąrašą, veiksmų srityje, esančioje skirtuke **Darbo užsakymų telkinys**, grupėje **Įsigijimas**, pasirinkite **Darbo užsakymo pirkimo paraiška**, kad atidarytumėte sąrašo puslapį **Darbo užsakymo pirkimo paraiška**.

16. Norėdami peržiūrėti pirkimo užsakymų, susijusių su darbo užsakymais, esančiais darbo užsakymų telkinyje, sąrašą, veiksmų srityje, esančioje skirtuke **Darbo užsakymų telkinys**, grupėje **Įsigijimas**, pasirinkite **Darbo užsakymo pirkimas**, kad atidarytumėte sąrašo puslapį **Darbo užsakymo pirkimas**.

>[!NOTE]
>Kai tam tikras darbo užsakymų telkinys planuojant darbą nebėra aktualus, nustatykite telkinio parinkties **Aktyvus** reikšmę **Ne**, pasiekiamą puslapio **Darbo užsakymų telkinys** sąrašo rodinyje.

Norėdami pašalinti visas darbuotojo užsakymo eilutes, nustatykite parinkties **Panaikinti darbo užsakymų ryšius** reikšmę **Taip**. Ši parinktis naudinga, jei, pavyzdžiui, norite sukurti tuščią telkinį, kurį vėliau galėsite naudoti kitiems darbo užsakymams. Kai esate pasiruošę naudodami darbo užsakymų telkinį vėliau kurti naujus darbo užsakymų ryšius, nepamirškite nustatyti parinkties **Panaikinti darbo užsakymų ryšius** reikšmės **Ne**.

Toliau pateiktame paveikslėlyje parodytas sąrašo puslapio **Darbo užsakymų telkinys** pavyzdys.

![1 pav.](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>Darbo užsakymo įtraukimas į darbo užsakymų telkinį

Kaip aprašyta ankstesniame skyriuje, kurdami darbo užsakymų telkinį, į jį galite įtraukti darbo užsakymų. Darbo užsakymus į darbo užsakymų kaupinį taip pat galite įtraukti sąrašo puslapyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

1. Pasirinkite darbo užsakymą, o tada veiksmų srityje, skirtuke **Darbo užsakymas**, grupėje **Tvarkyti**, pasirinkite **Darbo užsakymų telkinys**.

2. Sąraše pasirinkite darbo užsakymą ir spustelėkite **Darbo užsakymų telkinys**.

3. Dialogo lango **Tvarkyti darbo užsakymų telkinį** lauke **Įtraukti / šalinti** pasirinkite **Įtraukti**.

4. Lauke **Telkinys** pasirinkite darbo užsakymų telkinį.

5. Pasirinkite **Gerai**.

6. Norėdami pridėti darbo užsakymą, kurį įtraukėte konkrečiame užsakyme, pire darbo užsakymų telkinio, sąrašo puslapyje **Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai** pasirinkite telkinį ir pasirinkite **Redaguoti**. Tada puslapyje **Darbo užsakymų telkinys**, „FastTab“ **Darbo užsakymai**, naudokite lauką **Rūšiavimo tvarka**, kad nustatytumėte į telkinį įtrauktų darbo užsakymų rūšiavimo tvarką.

Norėdami pašalinti pasirinktą darbo užsakymą iš darbo užsakymų telkinio, pakartokite šiuos veiksmus, tačiau atlikdami 3 veiksmą pasirinkite **Šalinti**.


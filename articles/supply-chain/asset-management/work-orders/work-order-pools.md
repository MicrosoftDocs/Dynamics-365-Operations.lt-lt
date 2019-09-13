---
title: Darbo užsakymų telkiniai
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas dirbti su darbo užsakymų telkiniais.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875799"
---
# <a name="work-order-pools"></a>Darbo užsakymų telkiniai


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Naudodami darbo užsakymų telkinius, galite grupuoti kažką bendra turinčius darbo užsakymus. Pavyzdžiui, galite kurti darbo užsakymų telkinius, skirtus

- darbo brigadoms, pavyzdžiui, A priežiūros brigadai, B priežiūros brigadai,  

- profesiniams įgūdžiams, pavyzdžiui, elektrikams ar santechnikams,  

- fizinėms vietoms,  

- laiko grafikams, pavyzdžiui, savaitėms ar kitiems laikotarpiams.  


Jei reikia, vieną darbo užsakymą galima įdėti į kelis darbo užsakymų telkinius.


## <a name="create-work-order-pool"></a>Darbo užsakymų telkinio kūrimas

Dalyje **Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai** galite apžvelgti savo darbo užsakymų telkinius ir kurti naujus telkinius.

1. Spustelėkite **Turto valdymas** > **Bendra** > **Darbo užsakymų telkiniai** > **Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai**.

2. Spustelėkite **Naujas**.

3. Lauke **Telkinys** įterpkite darbo užsakymų telkinio ID, o lauke **Pavadinimas** – pavadinimą.

4. Perjungimo mygtuke **Aktyvus** pasirinkite Taip, jei norite nurodyti, kad darbo užsakymų telkinys yra aktyvus.

5. Perjungimo mygtuke **Panaikinti darbo užsakymų ryšius** pasirinkite Taip, jei norite, kad darbo užsakymai būtų automatiškai pašalinami iš darbo užsakymų telkinio.

6. Lauke **Naikinti ciklo būseną** pasirinkite darbo užsakymo ciklo būseną. Pavyzdžiui, darbo užsakymo įvykdymo ciklo būseną galima nustatyti taip, kad būtų automatiškai panaikinami ryšiai su darbo užsakymų telkiniais.

7. Į darbo užsakymų telkinį darbo užsakymus galite pradėti įtraukti iš karto. „FastTab“ konteineryje **Darbo užsakymai** spustelėkite **Įtraukti eilutę**.

8. Lauke **Darbo užsakymas** pasirinkite darbo užsakymą. Susiję laukai automatiškai atnaujinami.

9. Jei norite įtraukti daugiau darbo užsakymų, pakartokite 7–8 veiksmus.

10. Lauke **Rikiavimo tvarka** galite nurodyti, ar darbo užsakymus reikia vykdyti tam tikra tvarka. Įterpdami skaičius 1, 2, 3 ir t. t., galite nurodyti konkrečią pasirinktų darbo užsakymų seką.

11. Spustelėję mygtuką **Darbo užsakymai**, matysite visų į darbo užsakymų telkinį įtrauktų darbo užsakymų sąrašą.

12. Spustelėję mygtuką **Pajėgumas**, atidarysite sritį **Pajėgumas** ir galėsite skaičiuoti bei peržiūrėti priežiūros grafiko, nesuplanuotų darbo užsakymų ir suplanuotų darbo užsakymų pajėgumą.

13. Spustelėję mygtuką **Prekių prognozė**, atidarysite sritį **Prekių prognozė** ir galėsite skaičiuoti bei peržiūrėti prekių (atsarginių dalių ir kitų reikiamų prekių), susijusių su priežiūros grafiku, nesuplanuotais darbo užsakymais ir suplanuotais darbo užsakymais, prognozes.

14. Spustelėję mygtuką **Darbo užsakymo pirkimo paraiška**, atidarysite sąrašą **Darbo užsakymo pirkimo paraiška** ir matysite pirkimo paraiškų, susijusių su darbo užsakymų telkinyje esančiais darbo užsakymais, sąrašą.

15. Spustelėję mygtuką **Darbo užsakymų pirkimas**, atidarysite sąrašą **Darbo užsakymų pirkimas** ir matysite pirkimo užsakymų, susijusių su darbo užsakymų telkinyje esančiais darbo užsakymais, sąrašą.

>[!NOTE]
>Kai tam tikras darbo užsakymų telkinys planuojant darbą nebėra aktualus, sąrašo rodinyje **Darbo užsakymų telkinys** esantį to telkinio žymės langelį **Aktyvus** nustatykite kaip Ne.

Jei norite panaikinti visas darbo užsakymų eilutes, pavyzdžiui, norėdami sukurti tuščią telkinį, kurį vėliau galėtumėte naudoti su kitais darbo užsakymais, pažymėkite žymės langelį **Panaikinti darbo užsakymų ryšius**. Jei, naudodami darbo užsakymų telkinį, vėliau norite kurti naujus darbo užsakymų ryšius, nepamirškite žymės langelio **Panaikinti darbo užsakymų ryšius** išvalyti.


![1 pav.](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a>Darbo užsakymo įtraukimas į darbo užsakymų telkinį

Kaip aprašyta pirmesniame skyriuje, kurdami darbo užsakymų telkinį, į jį galite įtraukti darbo užsakymų. Į darbo užsakymų telkinį darbo užsakymą taip pat galite įtraukti iš sąrašo **Visi darbo užsakymai**.

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Sąraše pasirinkite darbo užsakymą ir spustelėkite **Darbo užsakymų telkinys**.

3. Lauke **Įtraukti / šalinti** pasirinkite Įtraukti.

4. Lauke **Telkinys** pasirinkite darbo užsakymų telkinį.

5. Spustelėkite **Gerai**.

6. Jei, į darbo užsakymų telkinį įtraukę darbo užsakymą, jį norite padėti į konkrečią telkinio seką: atidarykite vieną darbo užsakymų telkinių sąrašo puslapių, pasirinkite telkinį ir spustelėkite **Redaguoti** bei formos **Darbo užsakymų telkinys** „FastTab“ konteinerio **Darbo užsakymai** lauke **Rikiavimo tvarka** koreguokite į telkinį įtrauktų darbo užsakymų rikiavimo tvarką.

Jei pasirinktą darbo užsakymą norite pašalinti iš darbo užsakymų telkinio, atlikdami 3 veiksmą pasirinkite Šalinti.


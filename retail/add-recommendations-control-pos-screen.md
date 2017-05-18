---
title: "Rekomendacijų valdiklio įtraukimas į EKA įrenginio operacijų puslapį"
description: "Šioje temoje paaiškinama, kaip rekomendacijų valdiklį įtraukti į elektroninio kasos aparato (EKA) įrenginio operacijų ekraną naudojant ekrano maketo dizaino įrankį programoje „Microsoft Dynamics 365 for Operations“."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 590a009fa4afaf8020b9905020266c4b7293d228
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Rekomendacijų valdiklio įtraukimas į EKA įrenginio operacijų puslapį

[!include[banner](includes/banner.md)]


Šioje temoje paaiškinama, kaip rekomendacijų valdiklį įtraukti į elektroninio kasos aparato (EKA) įrenginio operacijų ekraną naudojant ekrano maketo dizaino įrankį programoje „Microsoft Dynamics 365 for Operations“.

Naudodami „Microsoft Dynamics 365 for Operations“ galite rodyti produktų rekomendacijas savo EKA įrenginyje. *Rekomendacijos* –tai prekės, kurios gali sudominti jūsų klientą atsižvelgiant į jo pirkimo istoriją, prekės, kurias klientas įtraukė į savo norų sąrašą, ir prekės, kurias kiti klientai įsigijo internetu ir įprastose parduotuvėse. Norėdami rodyti produktų rekomendacijas, turite valdiklį įtraukti į operacijų ekraną naudodami ekrano maketo dizaino įrankį.

## <a name="open-layout-designer"></a>Atidarykite maketo dizaino įrankį
1.  Pasirinkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA** &gt; **Ekrano maketai**.
2.  Naudokite spartųjį filtrą, kad rastumėte ekraną, į kurį norite įtraukti valdiklį. Pvz., filtruokite lauką **Ekrano maketo ID** naudodami reikšmę „F2CP16:9M“.
3.  Sąraše raskite ir pasirinkite norimą įrašą. Pvz., pasirinkite „Pavadinimas: F2CP16:9M Ekrano maketo ID: F2CP16:9M“
4.  Spustelėkite dalį **Maketo dizaino įrankis**.
5.  Vykdykite paraginimo instrukcijas, kad paleistumėte maketo dizaino įrankį. Kai būsite paraginti įvesti kredencialus, įveskite tuos pačius kredencialus, kuriuos naudojote paleisdami maketo dizaino įrankį iš puslapio **Ekrano maketai**.
6.  Prisijungus bus parodytas puslapis, panašus į toliau pateiktą puslapį. Maketas skirsis, atsižvelgiant į jūsų parduotuvėje atliktus tinkinimus.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Pasirinkite rodymo parinktį
-----------------------

Galima pasirinkti iš dviejų konfigūracijų parinkčių. Pasirinkite geriausiai jūsų parduotuvei tinkančią parinktį ir vadovaukitės likusiomis instrukcijomis, kad baigtumėte valdiklio nustatymą. Toliau nurodytos dvi parinktys.
-   Rekomendacijos rodomos visada.
-   Skirtukas **Rekomendacijos** rodomos ekrano kairiojoje pusėje esančiame tinklelyje.

#### <a name="to-make-recommendations-always-visible"></a>Norėdami rekomendacijas rodyti visada, atlikite tolesnius veiksmus.

1.  Sumažinkite operacijų eilučių informacijos srities aukštį, kad ji būtų tokio paties aukščio kaip jos kairėje esanti kliento sritis.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Iš kairiojo meniu rekomendacijų valdiklį nuvilkite tarp operacijų eilučių informacijos srities ir mygtukyno į operacijų ekrano apatinėje dalyje, centre. Keiskite valdiklio dydį, kad jis tilptų toje erdvėje.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.
4.  Programoje „Dynamics 365 for Operations“ atidarykite **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikai**.
5.  Išplečiamajame sąraše pasirinkite **1090 registrai**.
6.  Spustelėkite **Paleisti dabar**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Norėdami skirtuką Rekomendacijos įtraukti į ekrano kairiojoje pusėje esantį mygtukyną, atlikite tolesnius veiksmus

1.  Dešiniuoju pelės klavišu spustelėkite tuščią erdvę po paskutiniuoju skirtuku mygtukyne, kuris yra kairiojoje puslapio pusėje.
2.  Spustelėkite **Tinkinti**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Spustelėkite **Naujas skirtukas**.
4.  Raskite naują skirtuką, kurį ką tik įtraukėte. Gali reikėti slinkti žemyn.
5.  Išplečiamajame sąraše **Turinys** pasirinkite **Rekomenduojami produktai**. [![pic-6](./media/pic-6.png)](./media/pic-6.png)
6.  Lauke **Žyma** įveskite rekomendacijų skirtuko pavadinimą. Pvz., įveskite „Rekomenduojami produktai“.
7.  Lauke **Vaizdas** pasirinkite vaizdą, kuris bus rodomas skirtuke.
8.  Spustelėkite **Gerai**. Naujasis skirtukas atsiranda mygtukyne.
9.  Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.
10. Programoje „Dynamics 365 for Operations“ atidarykite **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikai**.
11. Išplečiamajame sąraše pasirinkite **1090 registrai**.
12. Spustelėkite **Paleisti dabar**.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Pritaikytų produkto rekomendacijų apžvalga](personalized-product-recommendations.md)





---
title: Skambučių centro kanalo nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują skambučių centro kanalą.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3f8c47c00b920dae01213d1d241ac8ee6a18d4e3
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/24/2020
ms.locfileid: "4414499"
---
# <a name="set-up-a-call-center-channel"></a>Skambučių centro kanalo nustatymas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują skambučių centro kanalą.

## <a name="overview"></a>Peržiūra


Programoje „Dynamics 365 Commerce“ skambučių centras yra tam tikras „Commerce“ kanalas, kurį galima nustatyti programoje. Nustačius skambučių centro objektų kanalą, sistema leidžia susieti tam tikrus duomenis ir užsakymų apdorojimą pagal numatytuosius pardavimo užsakymus. Nors įmonė gali nustatyti kelis skambučių centro kanalus programoje „Commerce“, svarbu pažymėti, kad atskiras vartotojas gali būti susietas tik su vienu skambučių centro kanalu. 

Prieš kurdami naują skambučių centro kanalą, įsitikinkite, kad įvykdėte [būtinąsias kanalo nustatymo sąlygas](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Naujo skambučių centro kanalo kūrimas ir konfigūravimas

Norėdami sukurti ir sukonfigūruoti naują skambučių centro kanalą, atlikite tolesnius veiksmus.

1. Naršymo srityje eikite į **Mažmeninė prekyba ir prekyba \> Kanalai \> Skambučių centrai \> Visi skambučių centrai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Lauke **Pavadinimas** įveskite naujo kanalo pavadinimą.
1. Pasirinkite atitinkamą **juridinį subjektą** iš išplečiamojo meniu.
1. Pasirinkite atitinkamą **sandėlio** vietą iš išplečiamojo meniu. Ši vieta bus naudojama kaip numatytoji pardavimo užsakymuose, sukurtuose šiam skambučių centro kanalui, tik tuo atveju, jei kliento arba prekės lygyje nebuvo nustatyta kitų numatytųjų reikšmių.
1. Lauke **Numatytasis klientas** pateikite galiojantį numatytąjį klientą. Šie duomenys naudojami, kai kuriami nauji kliento įrašai, kad būtų automatiškai užpildoma numatytosiomis reikšmėmis. Kuriant skambučių centro užsakymus, nėra patartina sukurti užsakymų numatytajam klientui.
1. Lauke **El. paštu siunčiamo pranešimo šablonas** pateikite galiojantį el. siunčiamo pranešimo šabloną. Kadangi skambučių centro užsakymai kuriami ir apdorojami, el. paštu siunčiamo pranešimo šablonas naudojamas suaktyvinti automatinių el. pašto įspėjimų siuntimą klientams su informacija apie jų užsakymo būseną.
1. Pateikite **Kainos perrašymas** informacinį kodą. Pirmiausia gali prireikti sukurti informacinį kodą. Šis informacinis kodas pateikia priežasčių kodų rinkinį, kurį vartotojas bus raginamas pasirinkti, kai skambučių centro užsakyme naudojama kainos perrašymo funkcija.
1. Nurodykite **Sulaikymo kodas** informacinį kodą. Pirmiausia gali prireikti sukurti informacinį kodą. Šis informacinis kodas pateikia pasirinktinų priežasčių kodų rinkinį, iš kurio vartotojas bus raginamas pasirinkti, kai užsakymas yra sulaikomas.
1. Nurodykite **Kreditas** informacinį kodą. Pirmiausia gali prireikti sukurti informacinį kodą. Šis informacinis kodas pateikia priežasčių kodų rinkinį, iš kurio vartotojas gali pasirinkti, naudodamas skambučių centro užsakymo kredito funkcijas, kad klientas galėtų gauti įvairias grąžinamąsias išmokas dėl klientų aptarnavimo priežasčių.
1. Pasirinktinai: nustatykite finansines dimensijas „FastTab“ **Finansinės dimensijos**. Čia įvestos dimensijos bus numatytosios visuose pardavimo užsakymuose, sukurtuose šiame skambučių centro kanale.
1. Spustelėkite **Įrašyti**.

Toliau pateiktame vaizde parodytas naujo skambučių centro kanalo kūrimas.

![Naujas skambučių centro kanalas](media/channel-setup-callcenter-1.png)

Toliau pateiktame vaizde parodytas skambučių centro kanalo pavyzdys.

![Skambučių centro kanalo pavyzdys](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Papildoma kanalų sąranka

Papildomos užduotys, reikalingos skambučių centro kanalo sąrankai, apima mokėjimo metodų ir pristatymo būdų nustatymą.

Toliau pateiktame atvaizde rodomos sąrankos parinktys **Pristatymo būdai** ir **Mokėjimo metodai**, esančios skirtuke **Nustatyti**.

![Papildomi skambučių centro kanalo nustatymo veiksmai](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Nustatyti mokėjimo būdus

Atlikite toliau nurodytus veiksmus, norėdami nustatyti kiekvieno mokėjimo tipo, palaikomo šiame kanale, mokėjimo metodus. Vartotojams reikės pasirinkti iš anksto nustatytų mokėjimo metodų, kuriuos reikia susieti su skambučių centro kanalu. Prieš nustatydami savo skambučių centro mokėjimo metodus, pirmiausia nustatykite savo pagrindinius atsiskaitymo būdus dalyje **Mažmeninė prekyba ir prekyba \>Kanalų sąranka \> Mokėjimo metodai \> Mokėjimo metodai**.

1. Veiksmų srityje pasirinkite skirtuką **Sąranka**, tada pasirinkite **Mokėjimo metodai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Naršymo srityje pasirinkite mokėjimo metodą iš anksto nustatytų galimų mokėjimų.
1. Konfigūruokite visus papildomus parametrus, kurių reikia mokėjimo tipui. Kredito kortelėms, dovanų kortelėms ar lojalumo kortelėms reikalingi papildomi parametrai pasirenkant funkciją **Kortelės sąranka**. 
1. Konfigūruokite tinkamas mokėjimo tipo registravimo sąskaitas skyriuje **Registravimas**.
1. Veiksmų srityje spustelėkite **Įrašyti**.

Toliau pateiktame vaizde parodytas mokėjimas grynaisiais pinigais pavyzdys.

![Mokėjimo metodų pavyzdys](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a>Nustatyti pristatymo būdus

Galite peržiūrėti sukonfigūruotus pristatymo būdus pasirikdami **Pristatymo būdai** skirtuke **Nustatymas**, esančiame **Veiksmų sritis**.  

Norėdami pakeisti arba pridėti pristatymo būdą, kuris bus susietas su skambučių centro kanalu, atlikite šiuos veiksmus.

1. Skambučių centro pristatymo būdo parinktyse pasirinkite **Valdyti pristatymo būdus**
1. Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte naują pristatymo režimą, arba pasirinkite esamą režimą.
1. Skyriuje **Mažmeninės prekybos kanalai** spustelėkite **Įtraukti eilutę**, kad galėtumėte įtraukti skambučių centro kanalą. Kanalų įtraukimas naudojant organizacijos mazgus, užuot įtraukus kiekvieną kanalą atskirai, gali racionalizuoti kanalų įtraukimą.
1. Įsitikinkite, kad pristatymo būdas sukonfigūruotas su duomenimis, nurodytais „FastTab“**Produkai** ir „FastTab“ **Adresai**. Jei pristatymo būdui nėra tinkamų prekių ar pristatymo adresų, pasirenkant jį užsakymo įvedimo metu atsiras klaidų.
1. Po to, kai buvo atlikti bet kokie skambučių centro pristatymo būdo konfigūracijų keitimai, užduotis **Apdoroti pristatymo būdus** turi būti vykdoma, kad išskleistumėte keitimo matricą. Šią užduotį galima surasti pereinant į **Mažmeninė prekyba ir prekyba \>Mažmeninės prekybos ir prekybos IT \>Apdoroti pristatymo būdus**.

Toliau pateiktame vaizde parodytas pristatymo būdo pavyzdys.

![Nustatyti pristatymo būdus](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Kanalo vartotojų nustatymas

Norėdamas sukurti pardavimo užsakymą, kuris yra susietas su skambučių centro kanalu iš „Commerce Headquarters”, pardavimo užsakymą kuriantis vartotojas turi būti susietas su skambučių centro kanalu. Vartotojas rankiniu būdu negali susieti pardavimo užsakymo, sukurto „Commerce Headquarters”, su skambučių centro kanalu. Saitas yra sistemingas, jis paremtas vartotoju ir vartotojo ryšiu su skambučių centro kanalu. Vartotojas gali būti susietas tik su vienu skambučių centro kanalu.

1. Veiksmų srityje pasirinkite skirtuką **Kanalas**, tada pasirinkite **Kanalo vartotojai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Pasirinkite esamą **Vartotojo ID** iš išplečiamojo pasirinkimo sąrašo, jei norite susieti šį vartotoją su skambučių centro kanalu

Kai kanalo vartotojų sąranka baigta ir vartotojas sukūrė naują pardavimo užsakymą programoje „Commerce Headquarters”, pardavimo užsakymas bus susietas su jo susietu skambučių centro kanalu. Visos šio kanalo konfigūracijos bus sistemingai taikomos pardavimo užsakymui. Vartotojas gali patvirtinti, su kuriuo skambučių centro kanalu pardavimo užsakymas yra susietas, pardavimo užsakymo antraštėje peržiūrėdamas kanalo pavadinimo nuorodą.


### <a name="set-up-price-groups"></a>Nustatyti kainų grupes

Kainos grupės yra pasirinktinės, tačiau, jei jos naudojamos, galima kontroliuoti, kurios pardavimo kainos bus siūlomos klientams, pateikiantiems užsakymus skambučių centro kanale. Jei kainos grupė nesukonfigūruota klientui, arba jei katalogo kainos grupės nėra taikomos pardavimo užsakymui (skambučių centro užsakymo antraštėje naudojant lauką **Šaltinio kodo ID**), tada kanalo kainos grupė naudojama prekių kainoms rasti. Jei kainos grupė skambučių centro kanale nerasta, naudojamos numatytosios pagrindinės prekės kainos. 

Norėdami nustatyti kainos grupę, atlikite šiuos veiksmus.

1. Veiksmų srityje spustelėkite skirtuką **Kanalas**, tada pasirinkite **Kainos grupės**.
1. Veiksmų srityje spustelėkite **Naujas**.
1. Išplečiamajame pasirinkimo sąraše pažymėkite **Mažmeninės kainos grupė**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md)

[Skambučių centro pardavimo funkcijos](call-center-functionality.md)

[Skambučių centro užsakymo apdorojimo parinkčių nustatymas](set-up-order-processing-options.md)

[Skambučių centro katalogai](call-center-catalogs.md)

[Įspėjimų dėl apgaulės nustatymas ir jų naudojimas](set-up-fraud-alerts.md)

[Skambučių centrų tęstinumo programų nustatymas](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: "Mobilioji tiekėjų bendradarbiavimo sritis, skirta programai „Microsoft Dynamics 365 for Operations“"
description: "Tiekėjai, naudodami mobiliąją tiekėjų bendradarbiavimo sritį, gali gauti naujausią jiems patvirtinti išsiųstų pirkimo užsakymų informaciją bei peržiūrėti informaciją apie naujus ir atnaujintus pirkimo užsakymus ir kontaktus."
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d5157e6f4b10b6158aa08279a9f68dae676f5666
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilioji tiekėjų bendradarbiavimo sritis, skirta programai „Microsoft Dynamics 365 for Operations“

[!include[banner](../includes/banner.md)]


Tiekėjai, naudodami mobiliąją tiekėjų bendradarbiavimo sritį, gali gauti naujausią jiems patvirtinti išsiųstų pirkimo užsakymų informaciją bei peržiūrėti informaciją apie naujus ir atnaujintus pirkimo užsakymus ir kontaktus.

<a name="prerequisites"></a>Būtinieji komponentai
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Būtinoji sąlyga</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Skaitykite apie „Microsoft Dynamics 365 for Operations“ mobiliąją platformą</td>
<td><a href="https://ax.help.dynamics.com/en/wiki/mobile-development-handbook/">Mobilioji „Dynamics 365 for Operations“ platforma</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Įsitikinkite, kad naudojate aplinką, kurioje yra „Microsoft Dynamics 365 for Operations“ 1611 versijos ir „Microsoft Dynamics for Operations“ 3 platformos naujinimas (2016 m. lapkričio mėn.).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000">Mobilusis įrenginys, kuriame įdiegta programa „Dynamics 365 for Operations“</span></td>
<td><span style="color: #000000">Iš mobiliųjų įrenginių programėlių parduotuvės atsisiųskite programą „Dynamics 365 for Operations“.</span></td>
</tr>
<tr class="even">
<td>Karštosios pataisos KB 4013633</td>
<td>Įdiegę karštąsias pataisas įjunksite „Dynamics 365 for Operations“ pateikiamas darbo sritis.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000"><span style="color: #000000">Karštosios pataisos KB 3216943</span> </span></td>
<td>Įdiegę karštąsias pataisas įjunksite mobiliąją tiekėjų bendradarbiavimo sritį.</td>
</tr>
<tr class="even">
<td>Su tiekėju susijęs vartotojas turi pasiekti tiekėjų bendradarbiavimo žiniatinklio sąsają programoje „Dynamics 365 for Operations“ ir nustatyti su tiekėju susijusį bendradarbiaujantį vartotoją.</td>
<td>Atlikę toliau pateiktose temose aprašytus veiksmus nustatykite tiekėjų bendradarbiavimo žiniatinklio sąsają ir ją naudodami vykdykite veiklą.
<ul>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-external-vendors/">Tiekėjų bendradarbiavimo sąsajos naudojimas veiklai su išoriniais tiekėjais vykdyti</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/manage-vendor-collaboration-users/">Tiekėjo bendradarbiavimo vartotojų valdymas</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/set-up-and-maintain-vendor-collaboration/">Tiekėjo bendradarbiavimo nustatymas ir tvarkymas</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-customers-in-dynamics-365-for-operations/">Tiekėjų bendradarbiavimo sąsajos naudojimas veiklai su klientais vykdyti programoje „Dynamics 365 for Operations“</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Apžvalga
Tiekėjai, naudodami mobiliąją tiekėjų bendradarbiavimo sritį, gauna naujausią informaciją apie naujus pirkimo užsakymus, tad jie gali juos peržiūrėti ir imtis su jais susijusių veiksmų naudodami žiniatinklio klientą „Dynamics 365 for Operations“. 

**Pastaba.** Vien tik mobilioji darbo sritis neturėtų būti naudojama – naudokite ją ir tiekėjų bendradarbiavimo žiniatinklio sąsają. 

Tiekėjai, naudodami mobiliąją tiekėjų bendradarbiavimo sritį, gali peržiūrėti naujus patvirtinti išsiųstus pirkimo užsakymus. Joje pateikiama pirkimo užsakymų informacija, pvz., produktai, kiekis ar pageidaujamos pristatymo datos. Kainų informacija pasiekiama atsižvelgiant į kiekvieno tiekėjo konfigūraciją. 

Vartotojui prisijungus kaip tiekėjui bus pateikiami pirkimo užsakymai, kurių atžvilgiu atlikta veiksmų, arba pirkimo užsakymai, kurių atžvilgiu klientas dar neatliko veiksmų. Tiekėjas galėjo pasiūlyti kitą pristatymo datą, kuri dar nesuderinta su klientu, tad klientas dar turi atlikti su pirkimo užsakymu susijusį veiksmą. Tiekėjui taip pat bus pateikiamas patvirtintų pirkimo užsakymų, kurių produktai dar nepristatyti, sąrašas. 

Norėdamas atlikti su pirkimo užsakymu susijusį veiksmą, tiekėjas turi naudoti tiekėjų bendradarbiavimo žiniatinklio sąsają, kuri pasiekiama naudojant žiniatinklio klientą „Dynamics 365 for Operations“. Šioje sąsajoje tiekėjas gaus ir daugiau užsakymo informacijos, pvz., apie dokumentų priedus, pristatymo adresą kiekvienoje eilutėje ar su tiekėju susijusius mokesčius. 

Jei tiekėjui bus suteiktas tam tikras saugos vaidmuo, jis galės peržiūrėti tiekėjo sąskaitoje užregistruotus kontaktinius asmenis. Esant tam pačiam saugos vaidmeniui tiekėjas galės peržiūrėti bet kurios pateiktos vartotojo užklausos būseną. 

Nauji kontaktai turi būti kuriami bei naujos vartotojo užklausos turi būti pateikiamos tiekėjų bendradarbiavimo sąsajoje, kuri pasiekiama naudojant žiniatinklio klientą „Dynamics 365 for Operations“. 

Tiekėjas, naudodamas mobiliąją darbo sritį, gali atlikti toliau nurodytus veiksmus.

-   Peržiūrėti naujus tiekėjui nusiųstus pirkimo užsakymus.
-   Peržiūrėti pirkimo užsakymus, kurių atžvilgiu tiekėjas atliko veiksmus, tačiau klientas jų atžvilgiu dar neatliko veiksmų.
-   Peržiūrėti pirkimo užsakymus, kurių būsena – Patvirtintas, tačiau gauti ne visi jų produktai.
-   Peržiūrėti tiekėjo sąskaitoje užregistruotų kontaktinių asmenų informaciją (būtinai turi būti suteiktas papildomas saugos vaidmuo).
-   Peržiūrėti informaciją ir stebėti tiekėjo pateiktos vartotojo užklausos būseną (būtinai turi būti suteiktas papildomas saugos vaidmuo).

## <a name="get-started"></a>Darbo pradžia
Norėdami pradėti naudoti šią darbo sritį mobiliajame įrenginyje, atlikite tolesnius veiksmus.

1.  Iš mobiliųjų įrenginių programėlių parduotuvės atsisiųskite ir įdiekite programą „Microsoft Dynamics 365 for Operations“.
2.  Paleiskite programą savo mobiliajame įrenginyje.
3.  Įveskite savo „Dynamics 365“ URL.
4.  Įveskite įmonę, prie kurios norite prisijungti. Pavyzdžiui, įveskite **USMF**.
5.  Pirmą kartą prisijungus būsite paraginti įvesti savo „Microsoft Dynamics 365 for Operations“ paskyros vartotojo vardą ir slaptažodį.

Prijungus programą nepateikiama jokia darbo sritis. Norėdami darbo sritis peržiūrėti savo mobiliojoje programoje, pirmiausia turite pageidaujamas sritis publikuoti programoje „Dynamics 365 for Operations“. Norint publikuoti darbo sritį, reikės sistemos administravimo teisių.

1.  Paleiskite „Dynamics 365 for Operations“.
2.  Pasirinkite **Sistemos administravimas** &gt; **Sąranka** &gt; **Sistemos parametrai**.
3.  Pasirinkite **Tvarkyti mobiliąją programą**.
4.  Pasirinkite darbo sritį **Tiekėjų bendradarbiavimas**, kad ją publikuotumėte mobiliojoje platformoje.
5.  Pasirinkite **Publikuoti darbo sritį**.
6.  Atnaujinkite įrenginio rodinį, kad matytumėte publikuojamas darbo sritis.
7.  Pasirinkite darbo sritį **Tiekėjų bendradarbiavimas**. Bus pateiktas toliau nurodytas puslapis.

    [![vendor-collaboration-mobile-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontaktai
Puslapyje **Kontaktai** galite peržiūrėti visus tiekėjo sąskaitoje nustatytus kontaktus. Jame pateikiami kontaktinių asmenų vardai ir pavardės, pagrindiniai el. paštai bei vartotojų pseudonimai (jei naudojami). Jame taip pat nurodoma, ar kontaktinių asmenų vartotojo paskyros yra aktyvios. Pasirinkus kontaktą pateikiama kontakto informacija, pvz., kontakto atstovaujami juridiniai subjektai, telefono numeris ar kitas el. pašto adresas.

## <a name="user-requests"></a>Vartotojų užklausos
Puslapyje **Vartotojų užklausos** galite peržiūrėti visas naudojant tiekėjų bendradarbiavimo žiniatinklio sąsają pateiktas vartotojo užklausas ir stebėti būseną. Pasirinkus vartotojo užklausą galima peržiūrėti užklausoje pateiktą informaciją, įtraukti ar išjungti vartotoją, keisti saugą bei peržiūrėti prašytus vartotojo saugos vaidmenis.

## <a name="purchase-orders-ready-for-review"></a>Parengti peržiūrėti pirkimo užsakymai
Puslapyje **Parengti peržiūrėti pirkimo užsakymai** galite peržiūrėti visus kliento išsiųstus pirkimo užsakymus, į kuriuos nėra atsakyta. Galite peržiūrėti pasirinktą užsakymo informaciją, pvz., apie pageidautus produktus ir pristatymo datą. Kainų informacija pasiekiama tik ją sukonfigūravus naudoti su tiekėjo informacija. Galite peržiūrėti, ar į pirkimo užsakymą įtraukta pastabų ar priedų. Norėdami atidaryti priedus, turėsite naudoti tiekėjų bendradarbiavimo sąsają, esančią žiniatinklio kliente. Pasirinkę **Pirkimo užsakymo eilutė** peržiūrėsite visas eilutes ir jų išsamią informaciją. Atkreipkite dėmesį, kad kiekvienoje eilutėje indikatorius nurodys, ar yra įtraukta pastabų ar priedų bei ar yra įtrauktas pristatymo adresas, besiskiriantis nuo antraštėje pateikiamo adreso. Norėdami atlikti su pirkimo užsakymu susijusį veiksmą, turėsite naudoti tiekėjų bendradarbiavimo žiniatinklio klientą.

## <a name="awaiting-customer-action"></a>Laukiama kliento veiksmo
Puslapyje **Laukiama kliento veiksmo** galite rasti pirkimo užsakymus, kurių atžvilgiu jūs arba kuris nors jūsų įmonės asmuo, taip pat turintis teisę pasiekti tiekėjų bendradarbiavimo sąsają, atliko veiksmus. Šiame sąraše pirkimo užsakymai pateikiami tik tada, kai klientui reikia atlikti kurį nors toliau nurodytą pirkimo užsakymo veiksmą.

-   Jei pirkimo užsakymas buvo atmestas, klientas turės atnaujinti išsiųstą užsakymą ir iš naujo jį išsiųsti arba atšaukti užsakymą ir iš naujo jį išsiųsti. Pirkimo užsakymą išsiuntus iš naujo, jis bus neberodomas puslapyje **Laukiama kliento veiksmo**.
-   Jei pirkimo užsakymas buvo priimtas su pakeitimais, klientas turės atnaujinti pradinį užsakymą ir iš naujo jį išsiųsti peržiūrėti arba jį atnaujinti atsižvelgdamas į pakeitimus ir iš karto patvirtinti. Abiem atvejais pirkimo užsakymas bus neberodomas puslapyje **Laukiama kliento veiksmo**.
-   Jei pirkimo užsakymas buvo priimtas ir yra pateikiamas puslapyje **Laukiama kliento veiksmo**, tuomet pirkimo užsakymas nebuvo automatiškai patvirtintas jį priėmus. Laukiama, kol pirkimo agentas pakeis užsakymo būseną į Patvirtintas. Paprastai pirkimo užsakymas laikomas sutartimi tarp kliento ir tiekėjo, sudaryta iš karto tiekėjui priėmus užsakymą. Tėra formalumas pakeisti pirkimo užsakymo būseną į Patvirtintas.

Pasirinkus pirkimo užsakymą pateikiama papildoma informacija apie atliktą veiksmą. Galite peržiūrėti išsamią kiekvienos eilutės informaciją ir atliktą veiksmą. Eilutės būsena nurodo, kuris iš toliau nurodytų veiksmų buvo atliktas.

-   Priimta
-   Atmestas
-   Priimta su pakeitimais
-   Pakeistas / pakaitas
-   Išskaidytas grafike / grafiko eilutė

Atminkite, kad indikatorius **Pristatymas** = taip / ne yra naudojamas nurodyti, kad eilučių produktai nebus pristatyti. Produktai gali būti nepristatomi dėl šių priežasčių: eilutė buvo atmesta; eilutė buvo pakeista ir nesitikima pristatyti pradinių eilučių produktų; eilutė buvo išskaidyta keliose grafiko eilutėse ir nesitikima pristatyti pradinės eilutės produktų, pageidautų gautame užsakyme. Pateikiami visi užsakymo eilutės veiksmo pakeitimai, išskyrus nusiųstas pastabas ir priedus, kuriuos galima peržiūrėti naudojant tiekėjų bendradarbiavimo žiniatinklio sąsają.

## <a name="open-confirmed-orders"></a>Atidaryti patvirtinti užsakymai
Kai klientas patvirtins pirkimo užsakymą, t. y. jo būsena bus pakeista į Patvirtintas, pirkimo užsakymas bus pateikiamas atidarytų patvirtintų užsakymų sąraše. Šiame sąraše jis bus rodomas tol, kol bus užregistruotas kliento gautu užsakymu.






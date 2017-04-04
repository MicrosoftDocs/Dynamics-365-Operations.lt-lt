---
title: "Veiksmo ieška"
description: "Šiame straipsnyje aprašoma veiksmų paieškos funkcija &quot;Microsoft Dynamics 365&quot; operacijoms. Veiksmų paieška padės jums rasti ir paleisti veiksmų puslapyje."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>Veiksmo ieška

Šiame straipsnyje aprašoma veiksmų paieškos funkcija "Microsoft Dynamics 365" operacijoms. Veiksmų paieška padės jums rasti ir paleisti veiksmų puslapyje.

<a name="introduction"></a>Įžanga
------------

Puslapius Microsoft Dynamics 365 operacijoms, visų pirma atskleisti komandos veiksmų sričių, standartinis veiksmų sritis, kuri pasirodo puslapio viršuje ir įrankių juostas, įvairių skyrių puslapyje rodomi. Ankstesnėse versijose klavišų patarimais funkcija leidžia greitai pasiekti bet kurį mygtuką veiksmų srities paspausdami klavišą Alt ir tada sudaro raidžių. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) vis dėlto dabartiniame Dynamics 365 operacijoms, klavišų patarimais nebėra bet pakeitė veiksmo paieškos funkcija. Ši nauja funkcija suteikia galimybę greitai ieškoti ir suaktyvinti bet kurios matomos veiksmų srities mygtuką.

## <a name="using-action-search"></a>Veiksmo ieškos naudojimas
Norėdami naudoti veiksmo ieškos funkciją, atlikite toliau nurodytus veiksmus.

1.  Veiksmų srityje spustelėkite lauką **veiksmo ieška**. (Lauke **veiksmo ieška** rodoma padidinamojo stiklo piktograma.)
2.  Įveskite visą arba dalį pavadinimo mygtuką, kurį norite paleisti. Jūs taip pat galite ieškoti naudodami žodžius iš mygtuko "kelyje." (Daugiau informacijos rasite kitame šio straipsnio skyriuje.) Paprastai mygtuką atsiras rezultatų sąrašo viršuje, po to, kai įvedėte dviejų iki keturių simbolių.
3.  Raskite ir aktyvinkite mygtuką rezultatų sąraše (naudodami pelę arba klaviatūrą).

Paleidus mygtuką suaktyvinama vėliausia aktyvi puslapio padėtis ir galima tęsti darbą. 

[![veiksmų paieškos lauką](./media/action-search-field.png)](./media/action-search-field.png)

Taip pat galite pradėti veiksmo iešką paspausdami CTRL + / arba ALT + Q. Vėl paspauskite klaviatūros spartųjį klavišą, kad būtų suaktyvinta vėliausia aktyvi puslapio padėtis.

## <a name="understanding-the-results-list"></a>Rezultatų sąrašo supratimas
Dažnai, Dynamics 365 operacijoms, jūs turite žinoti vietą ir atsižvelgiant į mygtuką iki galo suprasti tą mygtuką tikslas. Todėl papildoma informacija yra parodomas kiekvieno punkto rezultatų sąraše, kad galėtumėte tiksliai suprasti, kurie mygtukai rodomi sąraše. Konkrečiai yra rodomas mygtuko „kelias“. Šis kelias gali apimti susijusias toliau nurodytų vartotojo sąsajos elementų žymes.

-   Veiksmų srities skirtukas
-   Mygtukų grupė
-   Meniu mygtukas (jei mygtukas yra meniu mygtuko viduje)
-   Meniu skyriklis (jei mygtukas yra įvardytos meniu mygtuko grupės viduje)
-   Puslapio grupė arba skirtukas (pvz., „FastTab“ pavadinimas)

Pvz., **veiksmo ieškos** lauke įvedate **tot** nagrinėjate rezultatų sąrašą. Pirmas įrašas, mygtuką, pavadintą **sumos**, yra paryškinamas. Mygtuką kelias **pardavimų užsakymų**&gt;**Peržiūrėti** taip pat rodomas. Į **pardavimo užsakymas** kelias dalis atitinka į **pardavimo užsakymas** į veiksmų sritį, skirtuko ir **Peržiūrėti** kelias dalis atitinka į **Rodyti** grupės šio skirtuko. Taip pat kelias į **bendros nuolaidos** mygtuką (**parduoti**&gt;**skaičiuoti**) jus informuoja, kad šis mygtukas yra įsikūręs į **skaičiuoti** skirtuko į **parduoti** skirtuko veiksmo srities. Todėl ši informacija padeda jums suprasti, tiksliai kuris mygtukas bus būti sukeltas veiksmų paieškos (jei pasirinksite mygtuką, ieškos rezultatuose). 

[![veiksmas-paieškos-lauko-su-duomenys](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Ankstesniame pavyzdyje buvo rodomi puslapio viršuje esančios veiksmų srities veiksmo ieškos rezultatai. Tačiau taip pat rodomi kitose puslapio vietose esančių įrankių juostų veiksmo ieškos rezultatai. Pavyzdžiui, jūs ieškote į **turimas atsargas** mygtuką, esantį į **pardavimo užsakymo eilutės,** FastTab. Tokiu atveju mygtuką kelias rezultatų sąraše (**pardavimo užsakymo eilutės,**&gt;**atsargų**&gt;**Peržiūrėti**) informuoja jus, kad šis mygtukas yra pagal į **Rodyti** eilutė į **atsargų** meniu mygtuką į **pardavimo užsakymo eilutės,** FastTab. 

[![dėl turimų atsargų](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Veiksmo ieška ir naršymo ieška
Kadangi veiksmų paieškos yra skirta surasti ir paleisti veiksmų puslapyje, yra atskiri paieškos mechanizmas ir navigacija puslapiai Dynamics 365 operacijoms. Daugiau informacijos apie šią funkciją ieškokite su [navigacija paieškos](navigation-search.md) straipsnyje.



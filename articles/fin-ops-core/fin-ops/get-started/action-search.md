---
title: Veiksmo ieška
description: Šiame straipsnyje aprašyta veiksmo ieškos funkcija. Naudojant veiksmo iešką galima puslapyje rasti ir paleisti veiksmus.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd4d81f010149c762dac0f4e6fa912c2e2cef072
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112173"
---
# <a name="action-search"></a>Veiksmo ieška

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašyta veiksmo ieškos funkcija. Naudojant veiksmo iešką galima puslapyje rasti ir paleisti veiksmus.

## <a name="introduction"></a>Įžanga

Puslapiuose pirmiausia pateikiamos veiksmų sričių, įskaitant standartinę veiksmų sritį, rodomą puslapio viršuje, ir įvairiose puslapyje srityse rodomas įrankių juostas, komandas. Ankstesnėse versijose klavišų patarimų funkcija suteikė galimybę greitai pasiekti bet kurį veiksmų srities mygtuką paspaudžiant klavišą ALT ir raidžių seką.

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)

Klavišų patarimų funkciją pakeitė veiksmo ieškos funkcija. Ši nauja funkcija suteikia galimybę greitai ieškoti ir suaktyvinti bet kurios matomos veiksmų srities mygtuką.

## <a name="using-action-search"></a>Veiksmo ieškos naudojimas

Norėdami naudoti veiksmo ieškos funkciją, atlikite toliau nurodytus veiksmus.

1. Veiksmų srityje spustelėkite lauką **veiksmo ieška**. (Lauke **veiksmo ieška** rodoma padidinamojo stiklo piktograma.)
2. Įveskite visą mygtuko, kurį norite suaktyvinti, pavadinimą arba jo dalį. Taip pat galite ieškoti naudodami žodžius iš mygtuko „kelio“. (Daugiau informacijos žr. kitame šio straipsnio skyriuje.) Paprastai mygtukas bus rodomas rezultatų sąrašo viršuje po to, kai įvedate nuo dviejų iki keturių simbolių.
3. Raskite ir aktyvinkite mygtuką rezultatų sąraše (naudodami pelę arba klaviatūrą).

Paleidus mygtuką suaktyvinama vėliausia aktyvi puslapio padėtis ir galima tęsti darbą.

[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)

Taip pat galite pradėti veiksmo iešką paspausdami CTRL + / arba ALT + Q. Vėl paspauskite klaviatūros spartųjį klavišą, kad būtų suaktyvinta vėliausia aktyvi puslapio padėtis.

## <a name="understanding-the-results-list"></a>Rezultatų sąrašo supratimas

Turite žinoti mygtuko vietą ir kontekstą, kad visiškai suprastumėte to mygtuko funkciją. Todėl rezultatų sąraše rodoma papildoma kiekvieno elemento informacija padeda tiksliai suprasti, kurie mygtukai rodomi sąraše. Konkrečiai yra rodomas mygtuko „kelias“. Šis kelias gali apimti susijusias toliau nurodytų vartotojo sąsajos elementų žymes.

- Veiksmų srities skirtukas
- Mygtukų grupė
- Meniu mygtukas (jei mygtukas yra meniu mygtuko viduje)
- Meniu skyriklis (jei mygtukas yra įvardytos meniu mygtuko grupės viduje)
- Puslapio grupė arba skirtukas (pvz., „FastTab“ pavadinimas)

Pvz., **veiksmo ieškos** lauke įvedate **tot** nagrinėjate rezultatų sąrašą. Pirmasis įrašas, skirtas mygtukui, pavadinimu **Sumos**, yra paryškintas. Taip pat rodomas mygtuko kelias **Pardavimo užsakymas** &gt; **Rodinys**. Kelio dalis **Pardavimo užsakymas** atitinka veiksmų srities skirtuką **Pardavimo užsakymas**, o kelio dalis **Rodinys** atitinka šio skirtuko grupę **Rodinys**. Panašiai mygtuko **Bendroji nuolaida** kelias (**Pardavimas** &gt; **Skaičiuoti**) informuoja, kad šis mygtukas yra veiksmų srities skirtuko **Pardavimas** grupėje **Skaičiuoti**. Todėl ši informacija padeda tiksliai suprasti, kurį mygtuką veiksmo ieška suaktyvins (jei tą mygtuką pasirinksite rezultatų sąraše).

[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)

Ankstesniame pavyzdyje buvo rodomi puslapio viršuje esančios veiksmų srities veiksmo ieškos rezultatai. Tačiau taip pat rodomi kitose puslapio vietose esančių įrankių juostų veiksmo ieškos rezultatai. Pvz., ieškote mygtuko **Turimos atsargos**, esančio „FastTab“ **Pardavimo užsakymo eilutės**. Šiuo atveju rezultatų sąraše pateikiamas mygtuko kelias (**Pardavimo užsakymo eilutės** &gt; **Atsargos** &gt; **Rodinys**) informuoja, kad šis mygtukas yra antraštėje **Rodinys**, kuri yra „FastTab“ **Pardavimo užsakymo eilutės** meniu mygtuke **Atsargos**.

[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

> [!NOTE]
> Kai kurie mygtukai nerodomi veiksmo ieškoje. Šie mygtukai – tiesioginio pokalbio mygtukai ir mygtukai iš papildomų formų. 

## <a name="action-search-vs-navigation-search"></a>Veiksmo ieška ir naršymo ieška

Veiksmo ieška skirta rasti ir vykdyti veiksmus puslapyje, bet yra atskiras ieškos mechanizmas, skirtas ieškoti ir naršyti puslapius. Daugiau informacijos apie šią funkciją ieškokite straipsnyje [Naršymo ieška](navigation-search.md).

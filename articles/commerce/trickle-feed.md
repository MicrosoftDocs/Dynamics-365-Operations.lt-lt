---
title: Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms
description: Šioje temoje aprašomas nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms „Microsoft Dynamics 365 Commerce”.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3f691017ad06d3416e4ba0e86d7a0bc207aba5bd
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004279"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms (viešoji peržiūros versija)

[!include [banner](includes/banner.md)]



„Dynamics 365 Retail” 10.0.4 ir ankstesnėse versijose išrašo registravimas yra dienos pabaigoje atliekama operacija. Visos operacijos knygose įregistruojamos dienos pabaigoje. Tuomet dideles operacijas reikia apdoroti per ribotą laiką, dėl to kartais kyla apkrovos ir užraktų bei išrašo registravimo klaidų. Be to, mažmenininkai savo knygose negali atpažinti įplaukų ir mokėjimų per dieną.

Su „Retail” 10.0.5 versijoje pristatyta nuolatiniu duomenų perdavimu mažais kiekiais pagrįsto užsakymų kūrimo viešąja vertinimo versija operacijos apdorojamos visą dieną, o dienos pabaigoje tvarkomas tik finansinis mokėjimo priemonių derinimas ir kitos grynųjų pinigų valdymo operacijos. Ši funkcija išskaido pardavimo užsakymų, SF ir mokėjimų kūrimą per visą dieną, taip užtikrindama didesnį našumą ir galimybę atpažinti įplaukas bei mokėjimus knygose beveik tikruoju laiku. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Kaip naudoti nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą registravimą
  
1. Norėdami įjungti nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą operacijų registravimą, eikite į **Sistemos administravimas > Sąranka > Licencijos konfigūracija** ir išjunkite raktą **Išrašai**.

2. Tame pačiame puslapyje įjunkite licencijos raktą **Išrašai (duomenų perdavimas mažais kiekiais) – peržiūra**. Įjungę šį raktą įsitikinkite, kad nėra patvirtinimo laukiančių išrašų, kuriuos reikia užregistruoti. 

    > [!Important]
    > Prieš įjungdami licencijos raktą **Išrašai (duomenų perdavimas mažais kiekiais) – peržiūra**, įsitikinkite, kad nėra patvirtinimo laukiančių išrašų, kuriuos reikia užregistruoti.

3. Dabartinis išrašo dokumentas bus padalintas į du skirtingus tipus: operacijų išrašą ir finansinę ataskaitą.

      - Operacijų išraše bus pateikiamos visos neužregistruotos ir patvirtintos operacijos ir kuriami pardavimo užsakymai, pardavimo sąskaitos faktūros, įmokų ir nuolaidų žurnalai bei pajamų ir išlaidų operacijos jūsų sukonfigūruotame režime. Turite sukonfigūruoti šį procesą taip, kad šis veiktų dideliu dažnumu ir dokumentai būtų sukuriami operacijas įkėlus į būstinę per P užduotį. Naudojant operacijų išrašą, kuris jau sukuria pardavimo užsakymus ir pardavimo sąskaitas faktūras, nėra realaus poreikio konfigūruoti paketinę užduotį **Registruoti atsargas**. Tačiau ją vis tiek galite naudoti konkretiems verslo poreikiams patenkinti.  
      
     - Finansinė ataskaita turi būti sukurta dienos pabaigoje, ji palaiko tik **Pamaina** uždarymo metodą. Šis išrašas bus taikomas tik finansiniam suderinimui ir sukurs tik skirtingų mokėjimo priemonių apskaičiuotos sumos ir operacijos sumos skirtumo sumų žurnalus bei kitų grynųjų pinigų valdymo operacijų žurnalus.   

4. Norėdami apskaičiuoti operacijų išrašą, spustelėkite **Mažmeninė prekyba ir prekyba> Mažmeninės prekybos ir prekybos IT > EKA registravimas > Atlikti operacijų išrašų paketinį skaičiavimą**. Norėdami atlikti paketinį operacijų išrašų registravimą, spustelėkite **Mažmeninė prekyba ir prekyba> Mažmeninės prekybos ir prekybos IT > EKA registravimas > Atlikti operacijų išrašų paketinį registravimą**.

5. Norėdami apskaičiuoti finansinę ataskaitą, spustelėkite **Mažmeninė prekyba ir prekyba> Mažmeninės prekybos ir prekybos IT > EKA registravimas > Atlikti finansinių ataskaitų paketinį skaičiavimą**. Norėdami registruoti finansines ataskaitas pakete, spustelėkite **Mažmeninė prekyba ir prekyba> Mažmeninės prekybos ir prekybos IT > EKA registravimas > Registruoti finansines ataskaitas pakete**.

> [!NOTE]
> Iš šios naujos funkcijos pašalinti meniu elementai **Mažmeninė prekyba ir prekyba > Mažmeninės prekybos ir prekybos IT > EKA registravimas > Atlikti paketinį išrašų apskaičiavimą** ir **Mažmeninė prekyba ir prekyba > Mažmeninės prekybos ir prekybos IT > EKA registravimas > Atlikti paketinį išrašų registravimą**.

Operacijų ir finansinių ataskaitų tipus galima kurti ir neautomatiniu būdu. Eikite į **Mažmeninė prekyba ir prekyba > Kanalai > Parduotuvės** ir spustelėkite **Išrašai**. Spustelėkite **Naujas** ir pasirinkite norimo sukurti išrašo tipą. Puslapyje **Išrašai** esančiuose laukuose ir puslapyje **Išrašo grupė** esančiuose veiksmuose bus rodomi susiję duomenys ir veiksmai pagal pasirinktą išrašo tipą.

---
title: Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms
description: Šioje temoje aprašomas nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms „Microsoft Dynamics365 Retail”.
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
ms.openlocfilehash: 80233a73dbffc7380503cf03703758b187824c2a
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622671"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms (viešoji vertinimo versija)

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

„Dynamics 365 Retail” 10.0.4 ir ankstesnėse versijose mažmeninės prekybos išrašo registravimas yra dienos pabaigoje atliekama operacija, o visos operacijos knygose įregistruojamos dienos pabaigoje. Tuomet dideles operacijas reikia apdoroti per ribotą laiką, dėl to kartais kyla apkrovos ir užraktų bei išrašo registravimo klaidų. Be to, mažmenininkai savo knygose negali atpažinti įplaukų ir mokėjimų per dieną.

Su „Retail” 10.0.5 versijoje pristatyta nuolatiniu duomenų perdavimu mažais kiekiais pagrįsto užsakymų kūrimo viešąja vertinimo versija operacijos apdorojamos visą dieną, o dienos pabaigoje tvarkomas tik finansinis mokėjimo priemonių derinimas ir kitos grynųjų pinigų valdymo operacijos. Ši funkcija išskaido pardavimo užsakymų, SF ir mokėjimų kūrimą per visą dieną, taip užtikrindama didesnį našumą ir galimybę atpažinti įplaukas bei mokėjimus knygose beveik tikruoju laiku. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Kaip naudoti nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą registravimą
  
1. Norėdami įjungti nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą mažmeninės prekybos operacijų registravimą, eikite į **Sistemos administravimas > Sąranka > Licencijos konfigūracija** ir išjunkite raktą **Mažmeninės prekybos išrašai**.

2. Tame pačiame puslapyje įjunkite licencijos raktą **Mažmeninės prekybos išrašai (duomenų perdavimas mažais kiekiais) – Peržiūra**. Įjungę šį raktą įsitikinkite, kad nėra patvirtinimo laukiančių išrašų, kuriuos reikia užregistruoti. 

> [!Important]
> Prieš įjungdami licencijos raktą **Mažmeninės prekybos išrašai (duomenų perdavimas mažais kiekiais) – Peržiūra**, įsitikinkite, kad nėra patvirtinimo laukiančių išrašų, kuriuos reikia užregistruoti.

3. Dabartinis išrašo dokumentas bus padalintas į du skirtingus tipus: operacijų išrašą ir finansinę ataskaitą.

      - Operacijų išraše bus pateikiamos visos neužregistruotos ir patvirtintos mažmeninės prekybos operacijos ir kuriami pardavimo užsakymai, pardavimo SF, įmokų ir nuolaidų žurnalai bei pajamų ir išlaidų operacijos jūsų sukonfigūruotame režime. Turite sukonfigūruoti šį procesą taip, kad šis veiktų dideliu dažnumu ir dokumentai būtų sukuriami mažmeninės prekybos operacijas įkėlus į „Retail Headquarters” per P užduotį. Naudojant operacijų išrašą, kuris jau sukuria pardavimo užsakymus ir pardavimo SF, nėra realaus poreikio konfigūruoti paketinę užduotį **Registruoti atsargas**. Tačiau ją vis tiek galite naudoti konkretiems verslo poreikiams patenkinti.  
      
     - Finansinė ataskaita turi būti sukurta dienos pabaigoje, ji palaiko tik **Pamaina** uždarymo metodą. Šis išrašas bus taikomas tik finansiniam suderinimui ir sukurs tik skirtingų mokėjimo priemonių apskaičiuotos sumos ir operacijos sumos skirtumo sumų žurnalus bei kitų grynųjų pinigų valdymo operacijų žurnalus.   

4. Norėdami apskaičiuoti operacijų išrašą, spustelėkite **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti operacijų išrašų paketinį skaičiavimą**. Norėdami atlikti paketinį operacijų išrašų registravimą, spustelėkite **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti operacijų išrašų paketinį registravimą**.

5. Norėdami apskaičiuoti finansinę ataskaitą, spustelėkite **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti finansinių ataskaitų paketinį skaičiavimą**. Norėdami atlikti finansinių ataskaitų paketinį registravimą, spustelėkite **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti finansinių ataskaitų paketinį registravimą**.

> [!NOTE]
> Iš šios naujos funkcijos pašalinti meniu elementai **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti paketinį išrašų apskaičiavimą** ir **Mažmeninė prekyba > Mažmeninės prekybos IT > EKA registravimas > Atlikti paketinį išrašų registravimą**.

Operacijų ir finansinių ataskaitų tipus galima kurti ir neautomatiniu būdu. Eikite į **Mažmeninė prekyba > Kanalai > Mažmeninės prekybos parduotuvės** ir spustelėkite **Mažmeninės prekybos išrašai**. Spustelėkite **Naujas** ir pasirinkite norimo sukurti išrašo tipą. Puslapyje **Mažmeninės prekybos išrašai** esančiuose laukuose ir puslapyje **Išrašo grupė** esančiuose veiksmuose bus rodomi susiję duomenys ir veiksmai pagal pasirinktą išrašo tipą.

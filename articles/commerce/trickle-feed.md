---
title: Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms
description: Šioje temoje aprašomas nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas operacijoms „Microsoft Dynamics 365 Commerce”.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0fdb1f636183e8365729ab8947a50614a77eaeac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211050"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms

[!include [banner](includes/banner.md)]

„Dynamics 365 Retail” 10.0.4 ir ankstesnėse versijose išrašo registravimas yra dienos pabaigoje atliekama operacija. Visos operacijos knygose įregistruojamos dienos pabaigoje. Tuomet dideles operacijas reikia apdoroti per ribotą laiką, dėl to kartais kyla apkrovos ir užraktų bei išrašo registravimo klaidų. Be to, mažmenininkai savo knygose negali atpažinti įplaukų ir mokėjimų per dieną.

Naudojant „Retail” 10.0.5 versijoje pristatytą nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą užsakymų kūrimą operacijos apdorojamos visą dieną, o dienos pabaigoje tvarkomas tik finansinis mokėjimo priemonių derinimas ir kitos grynųjų pinigų valdymo operacijos. Ši funkcija išskaido pardavimo užsakymų, SF ir mokėjimų kūrimą per visą dieną, taip užtikrindama didesnį našumą ir galimybę atpažinti įplaukas bei mokėjimus knygose beveik tikruoju laiku. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Kaip naudoti nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą registravimą
  
1. Norėdami įjungti mažmeninės prekybos operacijų nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą registravimą, įjunkite funkciją pavadinimu **Mažmeninės prekybos išrašai – duomenų perdavimas mažais kiekiais** naudodami funkcijų valdymą.

    > [!IMPORTANT]
    > Prieš įjungdami šią funkciją įsitikinkite, kad nėra patvirtinimo laukiančių išrašų, kuriuos reikia užregistruoti.

2. Dabartinis išrašo dokumentas bus padalintas į du tipus: operacijų išrašą ir finansinę ataskaitą.

      - Operacijų išraše bus pateikiamos visos neužregistruotos ir patvirtintos operacijos ir kuriami pardavimo užsakymai, pardavimo sąskaitos faktūros, įmokų ir nuolaidų žurnalai bei pajamų ir išlaidų operacijos jūsų sukonfigūruotame režime. Turite sukonfigūruoti šį procesą taip, kad šis veiktų dideliu dažnumu ir dokumentai būtų sukuriami operacijas įkėlus į būstinę per P užduotį. Naudojant operacijų išrašą, kuris jau sukuria pardavimo užsakymus ir pardavimo sąskaitas faktūras, nėra realaus poreikio konfigūruoti paketinę užduotį **Registruoti atsargas**. Tačiau ją vis tiek galite naudoti konkretiems verslo poreikiams patenkinti.  
      
     - Finansinė ataskaita turi būti sukurta dienos pabaigoje, ji palaiko tik **Pamaina** uždarymo metodą. Šis išrašas bus taikomas tik finansiniam suderinimui ir sukurs tik skirtingų mokėjimo priemonių apskaičiuotos sumos ir operacijos sumos skirtumo sumų žurnalus bei kitų grynųjų pinigų valdymo operacijų žurnalus.   

3. Norėdami apskaičiuoti operacijų išrašą, eikite į **„Retail“ ir „Commerce“> „Retail“ ir „Commerce“ IT > EKA registravimas > Atlikti operacijų išrašų paketinį skaičiavimą**. Norėdami atlikti paketinį operacijų išrašų registravimą, eikite į **„Retail“ ir „Commerce“ > „Retail“ ir „Commerce“ IT > EKA registravimas > Atlikti operacijų išrašų paketinį registravimą**.

4. Norėdami apskaičiuoti finansinę ataskaitą, eikite į **„Retail“ ir „Commerce“ > „Retail“ ir „Commerce“ IT > EKA registravimas > Atlikti finansinių ataskaitų paketinį skaičiavimą**. Norėdami atlikti finansinių ataskaitų paketinį registravimą, eikite į **„Retail“ ir „Commerce“ > „Retail“ ir „Commerce“ IT > EKA registravimas > Registruoti finansines ataskaitas pakete**.

> [!NOTE]
> Iš šios naujos funkcijos pašalinti meniu elementai **„Retail“ ir „Commerce“ > „Retail“ ir „Commerce“ IT > EKA registravimas > Atlikti paketinį išrašų apskaičiavimą** ir **„Retail“ ir „Commerce“ > „Retail“ ir „Commerce“ IT > EKA registravimas > Atlikti paketinį išrašų registravimą**.

Operacijų ir finansinių ataskaitų tipus galima kurti ir neautomatiniu būdu. Eikite į **„Retail“ ir „Commerce“ > Kanalai > Parduotuvės** ir spustelėkite **Išrašai**. Spustelėkite **Naujas** ir pasirinkite norimo sukurti išrašo tipą. Puslapyje **Išrašai** esančiuose laukuose ir puslapyje **Išrašo grupė** esančiuose veiksmuose bus rodomi susiję duomenys ir veiksmai pagal pasirinktą išrašo tipą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Produktams su serijos numeriais taikomi EKA patobulinimai
description: "Šioje temoje išvardyti patobulinimai, skirti produktams su serijos numeriais, kad galėtumėte sutaupyti laiko ir būti produktyvesni."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 83c2ce79f5bef058f55af0ecf498b207efc0507a
ms.contentlocale: lt-lt
ms.lasthandoff: 12/14/2017

---

# <a name="pos-improvements-for-serialized-products"></a>Produktams su serijos numeriais taikomi EKA patobulinimai

[!include[banner](includes/banner.md)]

## <a name="overview"></a>Peržiūra 
Pagal modulio Mažmeninių pardavimų valdymas parametrus produktus galima klasifikuoti kaip turinčius serijos numerius arba jų neturinčius. Kai produktai yra su serijos numeriais, kiekvienai prekei gali būti priskiriamas unikalus numeris, kuris padeda sekti garantijas, prekes ir patvirtinti nuosavybę. Nors galimybė produktams priskirti serijos numerius egzistavo mūsų moderniajame / debesies elektroniniame kasos aparate (EKA), įtraukta keletas patobulinimų, kurie kasininkams padės sutaupyti laiko ir būti produktyvesniems.  

## <a name="pos-improvements"></a>EKA patobulinimai

- **Serijos numerių iki tikrinimo etapo nereikia** – anksčiau kasininkas, į operaciją įtraukęs serijos numerį turintį produktą, turėjo nurodyti jo serijos numerį. Šis reikalavimas tapo problema dirbant su klientais, kai kasininkai ir pardavimo darbuotojai turėdavo galimybę parduoti papildomą produktų kiekį. Iki mokėjimo veiksmo produktai būdavo dažnai atnaujinami krepšelyje. Todėl kiekvieną kartą, kai kasininkas įtraukdavo naują produktą, sistema jo reikalaudavo nurodyti serijos numerį. Serijos numerio dialogo lange dabar yra mygtukas **Įtraukti vėliau**. Todėl pardavimo darbuotojai prekę gali įtraukti į operaciją, o serijos numerį nurodyti vėliau. Pardavimo darbuotojai gali greitai į krepšelį įtraukti ir jame pakeisti produktus su serijos numeriais, o serijos numerį nurodyti tik prieš tikrinimo etapą. Jei nenurodytas kurio nors serijos numerį turinčio produkto serijos numeris, kasininkas, kuris bando baigti operaciją, gauna klaidos pranešimą. Šiame pranešime nurodoma, kad kasininkas tęsti galės tik nurodęs trūkstamus serijos numerius.

    Po kiekvieno serijos numerį turinčio produkto, kurio serijos numeris nebuvo nurodytas, operacijos eilute rodomas komentaras. Šiame komentare nurodoma, kad nenurodytas prekės serijos numeris. Todėl kasininkas gali greitai rasti prekes su trūkstamais serijos numeriais.

    Prekių, kurių serijos numeris nenurodytas, serijos numerį taip pat galima nurodyti naudojant naują operaciją **Įtraukti serijos numerį**. Nurodžius serijos numerį, jo redaguoti negalima. Kasininkas turi anuliuoti eilutę ir produktą įtraukti dar kartą. 
    
- **Norint pateikti klientų užsakymus, serijos numeriai nėra būtini** klientų užsakymus galima pateikti vienoje parduotuvėje, o įvykdyti kitoje. Kasininkas, kuris pateikia kliento užsakymą, neprivalo nurodyti serijos numerio. Serijos numeris bus nurodytas atliekant išrinkimo arba paėmimo veiksmą. Tačiau serijos numerį reikia nurodyti visoms eilutės prekėms, kurioms parinktas pristatymo tipas **Išsinešti**. Kitu atveju operacijos baigti negalima.    
- **Produktai su serijos numeriais netelkiami operacijų ekrane** – puslapio **Funkcijų šablonas** laukų grupės **Terminalas** parametras **Telkti produktus** leidžia operacijų ekrane telkti tuos pačius serijos numerių neturinčius produktus. Telkiant tuos pačius produktus, juos lengviau matyti operacijų tinklelyje. Tačiau, kadangi serijos numeriai paprastai yra unikalūs ir pardavimo darbuotojai jų neprivalo įvesti iki tikrinimo etapo, parametras **Telkti produktus** produktams su serijos numeriais netaikomas. Todėl, jei pasirinktas parametras **Telkti produktus**, operacijų ekrane produktai su serijos numeriais nebus telkiami.
- **Galimybė ieškoti žurnalų pagal serijos numerį** – dabar žurnalų galima ieškoti papildomai pagal serijos numerius. Norėdami tai padaryti, atidarykite operaciją Žurnalai ir programos juostoje paspauskite mygtuką Išplėstinė ieška. Naudodami mygtuką Įtraukti filtrą, ieškai pagal serijos numerius galite taip pat galite taikyti filtrą.


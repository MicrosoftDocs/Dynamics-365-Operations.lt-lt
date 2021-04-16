---
title: Kelių kanalų bendrinimo funkcijos įjungimas ir naudojimas
description: Šioje temoje aprašoma, kaip įjungti ir naudoti „Microsoft Dynamics 365 Commerce” svetainių daryklės kelių kanalų bendrinimo funkciją.
author: psimolin
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: de317c2fae4607f5b8b887dd5e866d812043dcd3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799522"
---
# <a name="enable-and-use-cross-channel-sharing"></a>Bendrinimo tarp kelių kanalų įjungimas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip įjungti ir naudoti „Microsoft Dynamics 365 Commerce” svetainių daryklės kelių kanalų bendrinimo funkciją.

Kelių kanalų bendrinimo funkcija leidžia mažmenininkams pakartotinai naudoti ir bendrinti turinį keliuose svetainės kanaluose. Ši galimybė naudinga, kai svetainės kanalų pagrindinė kalba yra suderinama arba kai juose yra daug bendrų turinio elementų.

Kelių kanalų bendrinimo funkcija veikia įgalinus numatytąjį kanalą, kuriame bus ieškoma pasiekiamo turinio, kai nerandama pageidaujamo turinio kanalui būdinga versija. Turinys, skirtas bendrinimui kanaluose, sukuriamas numatytajame kanale. Šis turinys gali būti lokalizuotas bet kurioje lokalėje, kuri naudojama bet kuriame svetainės kanale.

## <a name="when-to-use-cross-channel-sharing"></a>Kada naudoti kelių kanalų bendrinimą

Kelių kanalų bendrinimo funkcija naudinga, kai keli vienos svetainės kanalai gali bendrinti turinį. Pavyzdžiui, mažmenininkas, turintis kelis prekės ženklus ir parduotuves, sugrupuotus pagal vieną svetainę, gali bendrinti turinį su kai kuriomis arba visomis parduotuvėmis. Šis bendrinamas turinys gali apimti sąlygų, mokėjimo sąlygų, siuntimo būdų ir dažnai užduodamų klausimų (DUK) puslapius.

Kelių kanalų bendrinimo funkcija taip pat palaiko fragmentus. Todėl turinio puslapis, kuriame yra kanalui būdingų fragmentų, gali būti sukurtas kaip kelių kanalų turinys. Tokiu atveju, nors didžioji dalis turinio bus bendrinama kanaluose, kanalui būdingi fragmentai kelių kanalų puslapyje bus atvaizduoti tik tada, kai jų prašoma iš atitinkamo parduotuvės kanalo.

Svetainėms, turinčioms tik vieną kanalą arba turinčioms kelis kanalus, kurie negali bendrinti turinio, kelių kanalų bendrinimo funkcija nebus naudinga.

## <a name="enable-cross-channel-sharing"></a>Kelių kanalų bendrinimo funkcijos įjungimas

Kelių kanalų bendrinimo funkcija įjungiama svetainės lygiu. Ši operacija yra vienkryptė. Kitaip tariant, po to, kai kelių kanalų bendrinimo funkcija įjungta, jos negalima išjungti.

Norėdami įjungti kelių kanalų bendrinimo funkciją „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.

1. Eikite į **Svetainės parametrai \> Funkcijos**.
1. Nustatykite funkcijos **Keli kanalai** parinktį į **Įjungta**.

    ![Parinktis Keli kanalai nustatyta į Įjungta „Commerce” svetainių daryklėje](./media/enabling-cross-channel-sharing.png)

Po to, kai įgalinsite kelių kanalų bendrinimo funkciją, kelių kanalų informacija bus rodoma skyriuje **Kanalai** , esančiame **Svetainės parametrai \> Funkcijos**, kaip parodyta toliau pateiktos iliustracijos pavyzdyje.

![Kanalų informacija matoma, kai įjungta kelių kanalų bendrinimo funkcija](./media/channels-cross-channel.png)

Be to, įjungus kelių kanalų bendrinimo funkciją, į lauką **Kanalas**, esantį viršutiniame dešiniajame „Commerce” svetainių daryklės kampe, bus įtraukta parinktis **Kelių kanalų internetinė parduotuvė**, kurią galima naudoti kelių kanalų turiniui valdyti, kaip parodyta toliau pateiktoje iliustracijoje.

![Parinktis Kelių kanalų internetinė parduotuvė, esanti lauke Kanalai, įjungus kelių kanalų bendrinimo funkciją](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>Kelių kanalų turinio kūrimas ir naudojimas

Kelių kanalų turinį galite kurti ir naudoti keliais būdais. Pavyzdžiui, galite sukurti kelių kanalų fragmentus, kelių kanalų puslapius, naudojančius kelių kanalų ir kanalui būdingą turinį, ir keisti kelių kanalų fragmentus kanalui būdingomis fragmentų versijomis.

### <a name="create-a-cross-channel-fragment"></a>Kelių kanalų fragmento kūrimas

Norėdami sukurti kelių kanalų fragmentą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.

1. Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.
1. Dialogo lange **Naujas fragmentas** pasirinkite modulį **Reklaminė juosta**, tada dalyje **Fragmento pavadinimas** įveskite pavadinimą (pavyzdžiui, **Kelių kanalų juosta**). Tada pasirinkite **Gerai**.
1. Modulio **Reklaminė juosta** ypatybių srityje pasirinkite **Įtraukti pranešimą**, tada pasirinkite **Pranešimas**.
1. Dialogo lango **Pranešimas** dalyje **Tekstas** įveskite **Keli kanalai** ir pasirinkite **Gerai**. 
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Šis kelių kanalų fragmentas gali būti naudojamas kelių kanalų arba kanalui būdinguose puslapiuose, sukurtuose bet kokiame svetainės kanale.

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>Kelių kanalų puslapio, naudojančio kelių kanalų turinį, kūrimas

Kelių kanalų puslapius galima naudoti bet kuriame jūsų svetainės kanale. Todėl galite sukurti bendrinamo turinio puslapį vieną kartą ir atlikti vėlesnius atnaujinimus vienoje vietoje. Pavyzdžiui, kelių kanalų puslapis **Sąlygos**, kuriame yra URL `/toc`, gali būti bendrinamas visuose svetainės kanaluose. Jei svetainės kanalų pagrindiniai URL yra `www.fabrikam.com/brand1` ir `www.fabrikam.com/brand2`, tas pats bendrinamas kelių kanalų puslapis **Sąlygos** bus pasiekiamas naudojant abu svetainės kanalų atitinkamus URL `www.fabrikam.com/brand1/toc` ir `www.fabrikam.com/brand2/toc`. Jei puslapis **Sąlygos** turi būti atnaujintas vėliau, turite atnaujinti tik vieną bendrinamą puslapį.

Norėdami sukurti kelių kanalų puslapį „Commerce” svetainių daryklėje, naudojantį kelių kanalų turinį, atlikite toliau pateiktus veiksmus.

1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Pasirinkti šabloną** pasirinkite šabloną, pvz., **Rinkodara**.
1. Dalyje **Puslapio pavadinimas** įveskite puslapio pavadinimą, (pavyzdžiui, **Kelių kanalų puslapis**).
1. Dalyje **Puslapio URL** įveskite puslapio URL (pvz., **pavyzdinispuslapis**) ir pasirinkite **Gerai**.
1. Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti fragmentą**.
1. Dialogo lange **Įtraukti fragmentą** pasirinkite kelių kanalų fragmentą, turintį reklaminę juostą, kurį sukūrėte anksčiau, ir pasirinkite **Gerai**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Turėtumėte matyti reklaminę juostą, kurioje parašyta „Keli kanalai.”
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>Kanalui būdingo puslapio, naudojančio kelių kanalų turinį, kūrimas

Naudodami kelių kanalų turinį kanalui būdinguose puslapiuose, galite sukurti bendrinamą turinio fragmentą vieną kartą ir naudoti jį kanalui būdinguose puslapiuose. Šis vieno šaltinio pasirinkimas yra naudingas naudojant bendrinamą turinį, pvz., sąlygas, mokėjimo sąlygas arba kontaktinę informaciją.

Norėdami sukurti kanalui būdingą puslapį „Commerce” svetainių daryklėje, naudojantį kelių kanalų turinį, atlikite toliau pateiktus veiksmus.

1. Iš konkretaus kanalo, pvz., **„Fabrikam“ išplėstinė internetinė parduotuvė**, eikite į **Puslapiai** ir pasirinkite **Naujas**, norėdami sukurti naują puslapį.
1. Dialogo lange **Pasirinkti šabloną** pasirinkite šabloną, pvz., **Rinkodara**.
1. Dalyje **Puslapio pavadinimas** įveskite puslapio pavadinimą, (pavyzdžiui, **Kanalui būdingas puslapis**).
1. Dalyje **Puslapio URL** įveskite puslapio URL (pvz., **kanaluibūdingaspuslapis**) ir pasirinkite **Gerai**.
1. Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti fragmentą**.
1. Dialogo lango **Įtraukti fragmentą** dalyje **Kanalas** pasirinkite **Kelių kanalų internetinė parduotuvė**. Kelių kanalų fragmentas, kurį sukūrėte anksčiau, turėtų būti rodomas sąraše. Pasirinkite jį, tada pasirinkite **Gerai**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Turėtumėte matyti reklaminę juostą, kurioje parašyta „Keli kanalai.”
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>Kanalui būdingos kelių kanalų puslapio versijos kūrimas

Kelių kanalų bendrinimo funkcija palaiko kelių kanalų turinio perrašymus. Pavyzdžiui, visi jūsų svetainės kanalai, išskyrus vieną, bendrai naudoja tą patį turinio vienetą. Tam vienam svetainės kanalui reikalingas kitoks turinys. Norėdami įdiegti skirtingą šio kanalo turinį, pakeiskite kelių kanalų turinį kanalui būdingu turiniu, sukurdami kanalui būdingą kelių kanalų puslapio versiją.

Norėdami sukurti kanalui būdingą kelių kanalų puslapio versiją „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.

1. Lauke **Kanalas**, esančiame viršutiniame dešiniajame kampe, pasirinkite **Kelių kanalų internetinė parduotuvė**.
1. Atidarykite kelių kanalų puslapį, kurį sukūrėte anksčiau.
1. Lauke **Kanalas**, esančiame viršutiniame dešiniajame kampe, pasirinkite kanalą, kurio turinys turi būti skirtingas. Puslapio rengyklėje rodomas pranešimas, raginantis sukurti naują puslapio variantą.
1. Pasirinkite **Kurti puslapio variantą**.
1. Puslapio varianto vietoje **Pagrindinis** pasirinkite daugtaškį (**...**), tada pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Reklaminė juosta**, tada pasirinkite **Gerai**.
1. Modulio **Reklaminė juosta** ypatybių srityje pasirinkite **Įtraukti pranešimą**, tada pasirinkite **Pranešimas**.
1. Dialogo lango **Pranešimas** dalyje **Tekstas** įveskite **Kanalui būdingas** ir pasirinkite **Gerai**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Turėtumėte matyti reklaminę juostą, kurioje parašyta „Kanalui būdingas.”
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Dabar, jei naudosite pagrindinį kanalo URL ir eisite į tos svetainės kelių kanalų puslapio URL, vietoje kelių kanalo turinio matysite kanalui būdingą turinį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Turinio įtraukimo būdai](add-manage-content.md)

[Puslapio modelio žodynas](page-elements-overview.md)

[Dokumentų būsenos ir vykdymo ciklas](document-states-overview.md)

[Darbas su publikavimo grupėmis](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

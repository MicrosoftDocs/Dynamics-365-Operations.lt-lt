---
title: "Tiekėjo bendradarbiavimo vartotojų valdymas"
description: "Šioje temoje aprašoma, kaip teikti užklausas dėl naujų tiekėjo bendradarbiavimo vartotojų konfigūravimo ir kaip įtraukti naujų tiekėjo bendradarbiavimo kontaktų."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 380f1bcdf7109dc12fd898199033eac7710d863c
ms.lasthandoff: 03/31/2017


---

# <a name="manage-vendor-collaboration-users"></a>Tiekėjo bendradarbiavimo vartotojų valdymas

Šioje temoje aprašoma, kaip teikti užklausas dėl naujų tiekėjo bendradarbiavimo vartotojų konfigūravimo ir kaip įtraukti naujų tiekėjo bendradarbiavimo kontaktų. 

„Microsoft Dynamics 365 for Operations“ tiekėjo bendradarbiavimo sąsajoje išoriniams tiekėjams pateikiama informacija apie pirkimo užsakymus, SF ir konsignacijos atsargas. Galite kurti naujus tiekėjo bendradarbiavimo kontaktus ir reikalauti, kad nauji vartotojai būtų konfigūruojami, jei dirbate kaip išorinis tiekėjas, naudojantis saugos vaidmenį **Tiekėjo administratorius (išorinis)** ar turintis panašių teisių. Taip pat galite šias užduotis atlikti, jei dirbate kaip įsigijimo specialistas. Šioje temoje šis vaidmuo nurodo įsigijimo specialistą, dirbantį įmonėje, kuriai priklauso „Dynamics 365 for Operations“ egzempliorius. Daugiau informacijos apie tai, kaip naudoti tiekėjo bendradarbiavimas, jei esate išorės tiekėjo, rasite [tiekėjo klientų](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Daugiau informacijos apie tai, kaip naudoti tiekėjo bendradarbiavimas, jei esate profesionalus pirkimui, rasite [tiekėjo bendradarbiavimo su užsienio tiekėjais](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Naujo tiekėjo bendradarbiavimo kontakto įtraukimas
Jei norite kam nors priskirti prieigą prie tiekėjo bendradarbiavimo, pirmiausią tą asmenį reikia įtraukti kaip tiekėjo bendradarbiavimo kontaktą. Taip pat galite kaip kontaktus įtraukti įmonės darbuotojus, kurie tiekėjo bendradarbiavimo nenaudos. Pavyzdžiui, jie gali būti kontaktiniai asmenys dėl kitos įsigijimo informacijos. Nauji Kontaktai įtraukiami ant į **visus kontaktus** puslapyje, prieinamame iš į **tiekėjo bendradarbiavimas**&gt;**Kontaktai** meniu. Norėdami įtraukti naują kontaktą, atlikite tolesnius veiksmus.

1.  Spustelėkite **Naujas.**
2.  Įveskite kontaktinio asmens informaciją.
3.  Pasirinkite, kurį juridinį subjektą jūsų įmonėje asmuo atstovauja ir su kuriuo juridiniu subjektu jis dirbs įmonėje, su kuria bendradarbiaus. Galite tai padaryti pažymėdami tam **juridinio asmens mano įmonėje**/**juridinio asmens kliento įmonėje** pora.
4.  Spustelėkite **Kurti**.

Jei norite kontaktą panaikinti, galima naikinti kontaktus, kuriuos jūs sukūrėte.

## <a name="vendor-collaboration-user-requests"></a>Tiekėjo bendradarbiavimo vartotojo užklausos
Tiekėjo bendradarbiavimo vartotojo užklausas gali teikti įsigijimo specialistas arba išorinio tiekėjo administratorius.

-   Jei yra išorės tiekėjo, pateikdami prašymus į **visus kontaktus** puslapį per į **tiekėjo bendradarbiavimas** modulis.
-   Jei esate įsigijimo specialistas, užklausas teikite naudodami puslapį **Peržiūrėti kontaktus**. Norėdami tai padaryti, įrašyti į tiekėjų sąrašą, be to **nustatymas** skyrių į į veiksmų sritį, pasirinkite **Kontaktai**&gt;**Rodyti kontaktus**.

Galite pateikti užklausą vartotojui konfigūruoti, išaktyvinti arba keisti saugos vaidmenis. Jei esate išorinio tiekėjo administratorius, turite būti prisiregistravę kaip tiekėjų kodų, dėl kurių norite teikti užklausas, kontaktinis asmuo ir turite turėti prieigą prie tų tiekėjų kodų tiekėjo bendradarbiavimo sąsajos.  

Pateikus užklausą, ji įtraukiamą į modulio **Tiekėjo bendradarbiavimas** sąrašą **Tiekėjo bendradarbiavimo vartotojo užklausos** ir modulio **Paraiškos** sąrašą **Tiekėjo bendradarbiavimo vartotojo užklausa** (modulio Paraiškos išoriniai vartotojai pasiekti negali).

### <a name="provision-a-user"></a>Vartotojo konfigūravimas

Prieš teikiant užklausą vartotojui konfigūruoti, tas asmuo turi būti nustatytas kaip vieno ar daugiau tiekėjų kodų kontaktas. Norėdami kurti naujo tiekėjo bendradarbiavimo vartotojo užklausą, atlikite tolesnius veiksmus.

1.  Dėl to **Visi kontaktai** spustelėkite **nuostata tiekėjo vartotojo**.
2.  Įveskite vartotojo el. pašto adresą. Vartotojas šį adresą naudos norėdamas prisijungti prie „Dynamics 365 for Operations“. Jei el. pašto adreso domenas užregistruotas kaip „Microsoft Azure“ nuomininkas, tada el. pašto adresas turi būti esama „Azure Active Directory“ (ADD) paskyra, kad konfigūravimo procesą būtų galima sėkmingai baigti. Jei el. pašto adreso domenas nėra užregistruotas kaip „Microsoft Azure“ nuomininkas, paskyra bus sukurta konfigūravimo proceso metu ir naujas vartotojas gaus laišką su kvietimu. Vartotojų el. pašto adresai su srityse pvz., @hotmail.com, @gmail.com, arba @comcast.netnegali būti naudojama užsiregistruoti Dynamics 365 operacijų vartotojui.
3.  Parinktį **Tiekėjo bendradarbiavimo prieiga leidžiama** nustatykite į **Taip** visiems juridiniams subjektams, prieigą prie kurių vartotojui reikia priskirti.
4.  Skyriuje **Priskirti vartotojų vaidmenis** pažymėkite tų saugos vaidmenų, kuriuos reikia priskirti naujam vartotojui, žymės langelį **Priskirti**.
5.  Spustelėkite **Pateikti**.

Kai tiekėjo vartotojo prašymas, kad **tiekėjo bendradarbiavimas prieiga leidžiama** laukas yra nustatytas **taip** už pasirinkto tiekėjo ir vartotojo prašyti darbo eiga bus pradėta. Darbo eigos metu „Dynamics 365 for Operations“ sukuriamas naujas vartotojas ir priskiriami saugos vaidmenys. Be to, suaktyvinama „Azure B2B“ tarnyba, kuri inicijuoja sąveiką su „Azure“ portalu ir naują arba esamą ADD paskyrą susieja su „Dynamics 365 for Operations“ vartotojo paskyra.

### <a name="inactivate-a-user"></a>Vartotojo išaktyvinimas

Vartotojo prieigą prie tiekėjo bendradarbiavimo galima pašalinti dviem būdais.

-   Tiekėjo puslapyje **Kontaktai** nustatykite kontakto parinktį **Tiekėjo bendradarbiavimo prieiga leidžiama** į **Ne**. Tai galima atlikti atskirai su kiekvienu juridiniu subjektu, kurio kontaktas pasirinktas asmuo yra. Šią parinktį gali naudoti tik įsigijimo specialistai.
-   Išaktyvinkite visą vartotojo paskyrą, pateikdami užklausą **Išaktyvinti su tiekėju susijusį vartotoją**.

Prašyti, kad vartotojas yra inaktyvuota:

1.  Dėl to **Visi kontaktai** spustelėkite **Inactivate****tiekėjo vartotojo**.
2.  Lauke **Verslo pagrindimas** įveskite komentarą.
3.  Spustelėkite **Pateikti**.

### <a name="modify-security-roles"></a>Saugos vaidmenų modifikavimas

Į **išlaikyti tiekėjo vartotojų vaidmenis** puslapyje yra toks pat kaip ir **nuostata tiekėjo vartotojo** puslapį, išskyrus tai, kad saugos vaidmenų sąrašą galima redaguoti.  

Prašyti, kad apsaugos roles yra pritaikyta vartotojui:

1.  Dėl į **visus kontaktus** spustelėkite **palaikyti****tiekėjo vartotojų vaidmenis**.
2.  Lauke **Verslo pagrindimas** įveskite komentarą.
3.  Skyriuje **Tvarkyti vartotojo vaidmenis** pasirinkite saugos vaidmenis, kuriuos norite priskirti, arba panaikinkite šalintinų vaidmenų žymėjimą.
4.  Spustelėkite **Pateikti**.




---
title: Tiekėjo bendradarbiavimo vartotojų valdymas
description: Šiame straipsnyje aprašoma, kaip pateikti užklausą dėl naujų tiekėjo bendradarbiavimo vartotojų parengimo ir kaip įtraukti naujus tiekėjo bendradarbiavimo kontaktus.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 823e92cadc36659264a70132ed1390c7bcf8bc5d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852308"
---
# <a name="manage-vendor-collaboration-users"></a>Tiekėjo bendradarbiavimo vartotojų valdymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip pateikti užklausą dėl naujų tiekėjo bendradarbiavimo vartotojų parengimo ir kaip įtraukti naujus tiekėjo bendradarbiavimo kontaktus. 

„Dynamics 365 Supply Chain Management“ tiekėjo bendradarbiavimo sąsajoje išoriniams tiekėjams pateikiama informacija apie pirkimo užsakymus, SF ir konsignacijos atsargas. Galite kurti naujus tiekėjo bendradarbiavimo kontaktus ir reikalauti, kad nauji vartotojai būtų konfigūruojami, jei dirbate kaip išorinis tiekėjas, naudojantis saugos vaidmenį **Tiekėjo administratorius (išorinis)** ar turintis panašių teisių. Taip pat galite šias užduotis atlikti, jei dirbate kaip įsigijimo specialistas. Šiame straipsnyje šis vaidmuo nurodo įsigijimo specialistą, kuris dirba įmonėje, kuri valdo tiekimo grandinės valdymo egzempliorių. Daugiau informacijos apie tai, kaip naudoti tiekėjo bendradarbiavimą, jei esate išorinis tiekėjas, žr. [Tiekėjo bendradarbiavimas su klientais](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Daugiau informacijos apie tai, kaip naudoti tiekėjo bendradarbiavimą, jei esate įsigijimo specialistas, žr. [Tiekėjo bendradarbiavimas su išoriniais tiekėjais](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Naujo tiekėjo bendradarbiavimo kontakto įtraukimas
Jei norite kam nors priskirti prieigą prie tiekėjo bendradarbiavimo, pirmiausią tą asmenį reikia įtraukti kaip tiekėjo bendradarbiavimo kontaktą. Taip pat galite kaip kontaktus įtraukti įmonės darbuotojus, kurie tiekėjo bendradarbiavimo nenaudos. Pavyzdžiui, jie gali būti kontaktiniai asmenys dėl kitos įsigijimo informacijos. Nauji kontaktai įtraukiami į puslapį **Visi kontaktai**, kurį galima pasiekti pasirinkus meniu **Tiekėjo bendradarbiavimas** &gt; **Kontaktai**. Norėdami įtraukti naują kontaktą, atlikite tolesnius veiksmus.

1.  Spustelėkite **Naujas.**
2.  Įveskite kontaktinio asmens informaciją.
3.  Pasirinkite, kurį juridinį subjektą jūsų įmonėje asmuo atstovauja ir su kuriuo juridiniu subjektu jis dirbs įmonėje, su kuria bendradarbiaus. Galite tai atlikti pasirinkę porą **Mano įmonės juridinis subjektas** / **Kliento įmonės juridinis subjektas**.
4.  Spustelėkite **Kurti**.

Jei norite kontaktą panaikinti, galima naikinti kontaktus, kuriuos jūs sukūrėte.

## <a name="vendor-collaboration-user-requests"></a>Tiekėjo bendradarbiavimo vartotojo užklausos
Tiekėjo bendradarbiavimo vartotojo užklausas gali teikti įsigijimo specialistas arba išorinio tiekėjo administratorius.

-   Jei esate išorinis tiekėjas, užklausas teikite naudodami modulio **Tiekėjo bendradarbiavimas** puslapį **Visi kontaktai**.
-   Jei esate įsigijimo specialistas, užklausas teikite naudodami puslapį **Peržiūrėti kontaktus**. Norėdami tai atlikti, tiekėjo įrašo veiksmų srities skyriuje **Sąranka** pasirinkite **Kontaktai** &gt; **Peržiūrėti kontaktus**.

Galite pateikti užklausą vartotojui konfigūruoti, išaktyvinti arba keisti saugos vaidmenis. Jei esate išorinio tiekėjo administratorius, turite būti prisiregistravę kaip tiekėjų kodų, dėl kurių norite teikti užklausas, kontaktinis asmuo ir turite turėti prieigą prie tų tiekėjų kodų tiekėjo bendradarbiavimo sąsajos.  

Pateikus užklausą, ji įtraukiamą į modulio **Tiekėjo bendradarbiavimas** sąrašą **Tiekėjo bendradarbiavimo vartotojo užklausos** ir modulio **Paraiškos** sąrašą **Tiekėjo bendradarbiavimo vartotojo užklausa** (modulio Paraiškos išoriniai vartotojai pasiekti negali).

### <a name="provision-a-user"></a>Vartotojo konfigūravimas

Prieš teikiant užklausą vartotojui konfigūruoti, tas asmuo turi būti nustatytas kaip vieno ar daugiau tiekėjų kodų kontaktas. Norėdami kurti naujo tiekėjo bendradarbiavimo vartotojo užklausą, atlikite tolesnius veiksmus.

1. Puslapyje **Visi kontaktai** spustelėkite **Pateikti su tiekėju susijusį vartotoją**.
2. Įveskite vartotojo el. pašto adresą. Šis adresas bus naudojamas vartotojo norint prisijungti prie „Supply Chain Management“. Jei el. pašto adreso domenas užregistruotas kaip „Microsoft Azure“ nuomininkas, tada el. pašto adresas turi būti esama „Azure Active Directory“ (AAD) paskyra, kad konfigūravimo procesą būtų galima sėkmingai baigti. Jei el. pašto adreso domenas nėra užregistruotas kaip „Microsoft Azure“ nuomininkas, paskyra bus sukurta konfigūravimo proceso metu ir naujas vartotojas gaus laišką su kvietimu. Vartotojų el. pašto adresai su domenais, pvz., @hotmail.com, @gmail.com arba @comcast.net. negali būti naudojami norint registruoti vartotoją.
3. Parinktį **Tiekėjo bendradarbiavimo prieiga leidžiama** nustatykite į **Taip** visiems juridiniams subjektams, prieigą prie kurių vartotojui reikia priskirti.
4. Skyriuje **Priskirti vartotojų vaidmenis** pažymėkite tų saugos vaidmenų, kuriuos reikia priskirti naujam vartotojui, žymės langelį **Priskirti**.
5. Spustelėkite **Pateikti**.

Kai su tiekėju susijusio vartotojo užklausa pateikta, nustatoma pasirinkto tiekėjo kodo lauko **Tiekėjo bendradarbiavimo prieiga leidžiama** parinktis **Taip** ir pradedama vartotojo užklausos darbo eiga. Darbo eigos metu sukuriamas naujas vartotojas ir priskiriami saugos vaidmenys. Be to, suaktyvinama „Azure B2B“ tarnyba, kuri inicijuoja sąveiką su „Azure“ portalu ir naują arba esamą ADD paskyrą susieja su „Supply Chain Management“ vartotojo paskyra. Norėdami gauti daugiau informacijos, žr. [Kas yra „Azure AD“ B2B bendradarbiavimas?](/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).

### <a name="inactivate-a-user"></a>Vartotojo išaktyvinimas

Vartotojo prieigą prie tiekėjo bendradarbiavimo galima pašalinti dviem būdais.

-   Tiekėjo puslapyje **Kontaktai** nustatykite kontakto parinktį **Tiekėjo bendradarbiavimo prieiga leidžiama** į **Ne**. Tai galima atlikti atskirai su kiekvienu juridiniu subjektu, kurio kontaktas pasirinktas asmuo yra. Šią parinktį gali naudoti tik įsigijimo specialistai.
-   Išaktyvinkite visą vartotojo paskyrą, pateikdami užklausą **Išaktyvinti su tiekėju susijusį vartotoją**.

Norėdami pateikti užklausą vartotojui išaktyvinti, atlikite tolesnius veiksmus.

1.  Puslapyje **Visi kontaktai** spustelėkite **Išaktyvinti** **su tiekėju susijusį vartotoją**.
2.  Lauke **Verslo pagrindimas** įveskite komentarą.
3.  Spustelėkite **Pateikti**.

### <a name="modify-security-roles"></a>Saugos vaidmenų modifikavimas

Puslapis **Prižiūrėti tiekėjo vartotojo vaidmenis** yra toks pat kaip puslapis **Konfigūruoti su tiekėju susijusį vartotoją**, išskyrus tai, kad pirmajame galima redaguoti saugos vaidmenų sąrašą.  

Norėdami pateikti užklausą vartotojo saugos vaidmenims modifikuoti, atlikite tolesnius veiksmus.

1.  Puslapyje **Visi kontaktai** spustelėkite **Tvarkyti** **su tiekėju susijusio vartotojo vaidmenis**.
2.  Lauke **Verslo pagrindimas** įveskite komentarą.
3.  Skyriuje **Tvarkyti vartotojo vaidmenis** pasirinkite saugos vaidmenis, kuriuos norite priskirti, arba panaikinkite šalintinų vaidmenų žymėjimą.
4.  Spustelėkite **Pateikti**.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
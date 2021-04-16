---
title: Nustatykite B2B el. komercijos saitą
description: Šioje temoje aprašoma, kaip nustatyti verslo su verslu (B2B) el. komercijos saitą „Microsoft Dynamics 365 Commerce“.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3c6ea6118c3ba0ab77fea91b2eafa75c89b8d71d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799762"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>B2B el. prekybos svetainės nustatymas

[!include [banner](../../includes/banner.md)]

Verslo su verslu (B2B) el. komercijos saitas suteikia kelias pagrindines ypatybes, kurios optimizuoja B2B vartotojo darbo eigą. Šioje temoje aprašoma, kaip nustatyti verslo su verslu (B2B) el. komercijos saitą „Microsoft Dynamics 365 Commerce“. Jis eina per modulius ir saito nustatymus, kurie turi būti konfigūruojami siekiant į jungti B2B konkrečius scenarijus.

## <a name="prerequisites"></a>Būtinieji komponentai

- Norėdami nustatyti B2B el. komercijos saitą, turite galėti įjungti ir konfigūruoti konkrečias funkcijas „Commerce“ būstinėje, kaip aprašoma šioje temoje.
- Pagrindinės patirtys, tokios kaip produkto atradimas, produkto informacijos puslapiai, vežimėlis ir išsiregistravimas yra valdomi tų pačių modulių, kurie naudojami verslo su verslu (B2C) el. komercijos saituose. Saito autoriai turėtų žinoti su visais moduliais, kuriuos „Dynamics 365 Commerce“ palaiko. Dėl daugiau informacijos, žr. [Modulio bibliotekos apžvalga](../starter-kit-overview.md).
- Šioje temoje laikoma, kad saito autoriai supranta „Commerce“ saito kūrimo įrankio pagrindus, šablonus, fragmentus ir puslapius taip, kad jie galėtų įjungti B2B funkcijas el. komercijos saitams.

## <a name="site-level-settings"></a>Saito lygio nustatymai

Galite prieiti prie saito lygio nustatymų saito kūrimo įrankyje **Saito nustatymai \> Plėtiniai**. Tolesni du saito lygio nustatymai taikomi B2B scenarijams:

- **Įjunkite kliento sąskaitos mokėjimus** – Ši ypatybė leidžia vartotojams mokėti už užsakymus su kliento sąskaitomis. Esamo vertės yra **Įjungtos B2B klientams**, **Įjungtos B2C klientams**, **Įjungtos visiems klientams** ir **Išjungtos visiems**. Jei jūsų B2B saitas palaiko kliento sąskaitas, turėtumėte pasirinkti **Įjungti B2C klientams**.
- **Įjungti užsakymo kiekio apribojimus** – Ši ypatybė jums leidžia nustatyti apribojimus prekių skaičiui, kurį galima užsakyti kiekvienam produktui ar kategorijai. Esamo vertės yra **Įjungtos B2B klientams**, **Įjungtos B2C klientams**, **Įjungtos visiems klientams** ir **Išjungtos visiems**.

> [!NOTE]
> Jums naujinant į naujausią modulio bibliotekos versiją privalote atlikti tolesnius žingsnius siekiant užsitikrinti, kad anksčiau aprašyti saito nustatymai yra prieinami jūsų aplinkoje. Dėl daugiau informacijos, žr. [Naujinti app.settings.json failą](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="create-business-partner-sign-up-pages"></a>Kurti verslo partnerio prisijungimų puslapius

Norėdami tapti verslo partneriu, vartotojai privalo pateikti verslo partnerio užklausą. Nuoroda į verslo partnerio užklausos puslapį bus prieinama B2B pagrindiniame puslapyje, todėl vartotojai gali pradėti procesą. Po to, kai vartotojai pateikia verslo partnerio užklausą, jie gaus patvirtinimą, kad užklausa buvo pateikta. 

### <a name="create-a-business-partner-request-page"></a>Kurti verslo partnerio užklausos puslapį

Modulis **Partnerio prisijungimas** verslo partnerio užklausos puslapyje yra naudojamas siekiant pradėti vartotojo užklausas tapti verslo partneriais. Toks modulis leidžia jums rinkti vartotojo informaciją, kurios reikia prisijungimo procesui. Taip pat, **Verslo sąskaitos adreso** modulis yra naudojamas apimti vartotojo adresą.

Norėdami nustatyti ir konfigūruoti verslo partnerio užklausos puslapį saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Kurkite šabloną pavadinimu **Prisijungimas**. Šis šablonas turi apimti tolesnius modulius:

    - Partnerio prisijungimas
    - Naršymo kelias
    - Antraštė
    - Paraštė
    - Turinio blokas
    - Teksto blokas
    - Produktų rinkinys

1. Naudokite **Prisijungimo** šabloną, kad sukurtumėte puslapį pavadinimu **Verslo partnerio užklausa**.
1. Vietoje **Antraštė** įtraukite antraštės fragmentą, kuris iš anksto konfigūruojamas su saito antrašte.
1. Vietoje **Poraštė** įtraukite poraštės fragmentą, kuris iš anksto konfigūruojamas su saito porašte.
1. Vietoje **Pagrindinė** įtraukite **Konteinerio** modulį. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.
1. Vietoje **Konteineris** įtraukite **Džiūvėsėlio** modulį. Modulio ypatybių juostoje, skyriuje **Nuorodos**, konfigūruokite nuorodą į pagrindinį puslapį ir įveskite **Pagrindinis** kaip nuorodos tekstą.
1. Vietoje **Konteineris** įtraukite **Partnerio prisijungimo** modulį po **Džiūvėsėlio** moduliu. Modulio ypatybių juostoje, **Antraštėje** įveskite **Tapti verslo partneriu**.
1. Vietoje **Partnerio prisijungimas** įtraukite **Verslo sąskaitos adreso** modulį.
1. Vietoje **Konteineris** įtraukite **Teksto blokavimo** modulį po **Partnerio prisijungimo** moduliu. Čia galite nustatyti kai kurias sąvokas ir sąlygas prisijungimo procesui.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Publikuoti URL puslapiui.

### <a name="create-a-business-partner-request-confirmation-page"></a>Kurti verslo partnerio užklausos patvirtinimo puslapį

Po to, kai pateikta verslo partnerio užklausa, patvirtinimo puslapis turi būti rodomas vartotojui siekiant pripažinti pateikimą. 

Norėdami nustatyti ir konfigūruoti užklausos patvirtinimo puslapį saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Naudokite anksčiau jūsų sukurtą **Prisijungimo** šabloną, kad sukurtumėte puslapį pavadinimu **Partnerio užklausos patvirtinimas**.
1. Vietoje **Antraštė** įtraukite antraštės fragmentą, kuris iš anksto konfigūruojamas su saito antrašte.
1. Vietoje **Poraštė** įtraukite poraštės fragmentą, kuris iš anksto konfigūruojamas su saito porašte.
1. Vietoje **Pagrindinė** įtraukite **Konteinerio** modulį. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.
1. Vietoje **Konteineris** įtraukite **Turinio blokavimo** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Užklausos pateikimą**. Laukelyje **Praturtintas tekstas**, įveskite **Jūsų užklausa buvo pateikta**. Skyriuje **Nuorodos**, konfigūruokite nuorodą į pagrindinį puslapį ir įveskite **Atgal į apsipirkimą** kaip nuorodos tekstą.
1. Įtraukite kitą **Konteinerio** modulį ir įtraukite **Produkto kolekcijos** modulį į jį.
1. Konfigūruokite **Produkto kolekcijos** modulį su rekomendacija ar kategorijos sąrašu, kurį norite rodyti puslapyje.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Publikuoti URL puslapiui.

Norėdami įtraukti nuorodą į užklausos patvirtinimo puslapį saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Eikite į **Verslo partnerio užklausos** puslapį, kurį anksčiau sukūrėte ir rinkitės **Redaguoti**. 
1. Rinkitės **Partnerio prisijungimo** modulio vieta. Ypatybių juostoje, **Susieti su prisijungimo patvirtinimo puslapio**, konfigūruokite nuorodą į verslo partnerio užklausos puslapį, kurį anksčiau sukūrėte. 
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>Įtraukite verslo partnerio užklausos nuorodą į pagrindinį puslapį

Po to, kai verslo partnerio užklausos prisijungimo ir patvirtinimo puslapiai yra sukurti, turite padaryti prisijungimo puslapį prieinamą per nuorodą į pagrindinį puslapį. Galite užbaigti šią užduotį įtraukdami nuorodą į bet kurį **Turinio blokavimo** modulį pagrindiniame puslapyje.

Norėdami įtraukti verslo partnerio užklausos nuorodą į pagrindinį puslapį saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Eikite į pagrindinį puslapį savo saite ir rinkitės **Redaguoti**.
1. Rinkitės **Turinio blokavimo** modulio vieta. Modulio ypatybių juostoje, **Nuorodos**, konfigūruokite nuorodą į verslo partnerio užklausos puslapį, kurį anksčiau sukūrėte ir įveskite **Prisijungti siekiant tapti verslo partneriu** ar panašų tekstą kaip nuorodos tekstą. Įtraukite paveikslėlį, kaip tinkami.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="account-management-landing-page"></a>Paskyros valdymo nukreipimo puslapis

Sąskaitos valdymo nusileidimo puslapis apima visą sąskaitos valdymo informaciją, kurios reikia B2B ir B2C el. komercijos saitams. Tik prisijungę vartotojai gali peržiūrėti šį puslapį.

Norėdami sukurti ir konfigūruoti B2B sąskaitos valdymo nusileidimo puslapį saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Kurkite šabloną pavadinimu **Sąskaitos valdymas**. Šis šablonas turi apimti tolesnius modulius:

    - Antraštė
    - Paraštė
    - Naršymo kelias
    - Paskyros sveikinimo plytelė
    - Bendroji paskyros plytelė
    - Sąskaitos adreso plytelė
    - Paskyros pageidavimų sąrašo plytelė
    - Paskyros adreso plytelė
    - Paskyros lojalumo plytelė
    - Sąskaitos kliento balanso plytelė
    - Sąskaitos užsakymo šablonų plytelė
    - Organizacijos vartotojai
    - Verslo organizacijos sąrašas
    - Kliento sąskaitos balansas
    - Užsakymo šablono eilutės
    - Užsakymo šablono sąrašas
    - Paskyros sąskaitos plytelė
    - Sąskaitų sąrašas
    - SF informacija

1. Naudokite **Sąskaitos valdymas** šabloną tam, kad sukurtumėte puslapį pavadinimu **Mano sąskaita**.
1. Vietoje **Antraštė** įtraukite antraštės fragmentą, kuris iš anksto konfigūruojamas su saito antrašte.
1. Vietoje **Poraštė** įtraukite poraštės fragmentą, kuris iš anksto konfigūruojamas su saito porašte.
1. Vietoje **Pagrindinė** įtraukite **Konteinerio** modulį. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**. 
1. Vietoje **Konteineris** įtraukite **Džiūvėsėlio** modulį. Modulio ypatybių juostoje, skyriuje **Nuorodos**, konfigūruokite nuorodą į pagrindinį puslapį ir įveskite **Pagrindinis** kaip nuorodos tekstą.
1. Vietoje **Konteineris** įtraukite **Pasisveikinimo plytelės** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Pasisveikinimas**.
1. Vietoje **Pagrindinis** įtraukite kitą **Konteinerio** modulį (**Konteineris 2**). Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**. Nustatykite **Vaikų rodymo** vertę į **Du**. 
1. Vietoje **Konteineris 2** įtraukite **Sąskaitos bendros plytelės** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Mano profilis**. Skyriuje **Nuorodos**, konfigūruokite nuorodą į **Mano profilio** puslapį. 
1. Vietoje **Konteineris 2** įtraukite kitą **Sąskaitos bendros plytelės** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Užsakymo istorija**. Skyriuje **Nuorodos** konfigūruokite nuorodą į užsakymo istorijos puslapį.
1. Vietoje **Pagrindinis** įtraukite kitą **Konteinerio** modulį (**Konteineris 3**). Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**. Nustatykite **Vaikų rodymo** vertę į **Du**. 
1. Vietoje **Konteineris 3** įtraukite **Sąskaitos adreso plytelės** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Mano adresas**. Skyriuje **Nuorodos**, konfigūruokite nuorodą į **Mano adresas** puslapį. 
1. Vietoje **Konteineris 3** įtraukite **Sąskaitos norų sąrašo plytelės** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Mano norų sąrašas**. Skyriuje **Nuorodos**, konfigūruokite nuorodą į **Mano norų sąrašas** puslapį.
1. Vietoje **Pagrindinis** įtraukite kitą **Konteinerio** modulį (**Konteineris 4**). Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**. Nustatykite **Vaikų rodymo** vertę į **Du**. 
1. Vietoje **Konteineris 4** įtraukite **Organizacijos vartotojų** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Organizacijos vartotojų**. 
1. Vietoje **Konteineris 4** įtraukite **Sąskaitos kliento balanso plytelės** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Sąskaitos kreditas**. 
1. Vietoje **Pagrindinis** įtraukite kitą **Konteinerio** modulį (**Konteineris 5**). Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**. Nustatykite **Vaikų rodymo** vertę į **Du**. 
1. **Konteineris 5** modulyje, įtraukite **Sąskaitos užsakymo šablonų plytelės** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Užsakymo šablonai**. 
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

> [!NOTE] 
> Kai kurie skyriai, kuriuos įtraukėte nuo 13 iki 18 veiksmuose nebus rodomi „tai, ką matote yra tai, ką gausite“ (WYSIWIG) drobės saito kūrimo įrankyje, nes jiems reikia prisijungimo B2B sąskaitos.

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>Kurkite ir konfigūruokite kliento balanso puslapius ir modulius 

Kliento sąskaitos gali būti naudojamas siekiant sumokėti už užsakymus. Esamas balansas kliento sąskaitoje gali būti peržiūrėtas vartotojo paskyros valdymo puslapyje.

### <a name="create-a-customer-balance-page"></a>Kurkite kliento balanso puslapį 

Prieš tai, kai prisijungę B2B vartotojai gali peržiūrėti savo kliento balansą, turite sukurti kliento balanso puslapį. 

Norėdami sukurti kliento balanso puslapį saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Naudokite **Sąskaitos valdymo** šabloną, kad sukurtumėte puslapį pavadinimu **Kliento balansas**.
1. Vietoje **Antraštė** įtraukite antraštės fragmentą, kuris iš anksto konfigūruojamas su saito antrašte.
1. Vietoje **Poraštė** įtraukite poraštės fragmentą, kuris iš anksto konfigūruojamas su saito porašte.
1. Vietoje **Pagrindinis** įtraukite kitą **Konteinerio** modulį (**Konteineris 3**). Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**. Nustatykite **Vaikų rodymo** vertę į **Du**.
1. Vietoje **Konteineris** įtraukite **Džiūvėsėlio** modulį. Modulio ypatybių juostoje, skyriuje **Nuorodos**, konfigūruokite nuorodą sąskaitos valdymo nusileidimo puslapį ir įveskite **Mano sąskaita** kaip nuorodos tekstą.
1. Vietoje **Konteineris** įtraukite **Kliento sąskaitos balanso** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Sąskaitos balansas**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Publikuoti URL puslapiui.
1. Eikite į sąskaitos valdymo nusileidimo puslapį (**Mano sąskaita**), kurį sukūrėte anksčiau.
1. Ypatybių juostoje **Sąskaitos kliento balanso plytelė** modulyje, įtraukite nuorodą į kliento balanso puslapį. 
1. Įrašykite ir publikuokite puslapį.

Kliento balanso puslapis dabar buvo sukurtas ir vartotojai gali prieiti prie jo iš sąskaitos valdymo nusileidimo puslapio.

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>Konfigūruokite išsiregistravimo puslapį taip, kad kliento balansą galima būtų naudoti kaip mokėjimą formą

Modulyje **Kliento sąskaitos mokėjimas** turi galėti įjungti kliento balansą, kuris naudojamas kaip mokėjimo forma. Šis modulis turi būti įtrauktas į išsiregistravimo puslapį kaip mokėjimo forma. Dėl informacijos apie tai, kaip sukonfigūruoti išsiregistravimo puslapį ir modulius, kurių reikia išsiregistruoti, įskaitant visą mokėjimo informaciją, žr. [Išsiregistravimo modulis](../add-checkout-module.md).

Po to, kai sukonfigūruosite išsiregistravimo puslapyje, turite įtraukti **Kliento sąskaitos mokėjimo** modulį į mokėjimo skyrių ir tada įrašyti bei publikuoti puslapį. B2B vartotojai tuomet galės prisijungti prie el. komercijos saito ir taikyti jų turimą kliento balansą užsakymams išsiregistravimo metu.

Taip pat, **Saito kūrimo įrankis \> Plėtiniai**, turite įsitikinti, kad **Įjungti kliento sąskaitos mokėjimų** ypatybę nustatytą **Įjungta B2B klientams**.

## <a name="create-order-template-pages"></a>Sukurkite užsakymo šablono puslapius

Du užsakymo šablono puslapiai gali būti nustatyti B2B el. komercijos saitui: užsakymo šablonų sąrašo puslapis ir užsakymo šablono eilučių puslapis.

Užsakymo šablono sąrašo puslapis rodo užsakymo šablonų sąrašą, kuris yra prieinamas. Jis nustatomas naudojant **Užsakymo šablonų** modulį. Užsakymo šablonų sąrašo puslapis jums leidžia kurti ar naikinti šabloną ir įtraukti prekes šablone į vežimėlį.

Užsakymo šablono eilutės puslapis rodo išsamią užsakymo šablono informaciją, kuri yra pasirinkta užsakymo šablonų sąrašo puslapyje. Jis nustatomas naudojant **Užsakymo šablonų eilučių** modulį. Kai vartotojai pasirenka šablono pavadinimą užsakymo šablonų sąrašo puslapyje, užsakymo šablono eilučių puslapis pasirodo ir rodo išsamią šablono informaciją. Vartotojas gali tuomet peržiūrėti ir redaguoti prekes šablone.

### <a name="create-an-order-templates-list-page"></a>Kurti užsakymo šablonų sąrašo puslapį

Norėdami sukurti užsakymo šablonų sąrašo puslapį saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Naudokite **Sąskaitos valdymo** šabloną, kad sukurtumėte puslapį pavadinimu **Užsakymo šablonai**.
1. Vietoje **Antraštė** įtraukite antraštės fragmentą, kuris iš anksto konfigūruojamas su saito antrašte.
1. Vietoje **Poraštė** įtraukite poraštės fragmentą, kuris iš anksto konfigūruojamas su saito porašte.
1. Vietoje **Pagrindinė** įtraukite **Konteinerio** modulį. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.
1. Vietoje **Konteineris** įtraukite **Džiūvėsėlio** modulį. Modulio ypatybių juostoje, skyriuje **Nuorodos**, konfigūruokite nuorodą sąskaitos valdymo nusileidimo puslapį ir įveskite **Mano sąskaita** kaip nuorodos tekstą.
1. **Konteineris 5** vietoje, įtraukite **Užsakymo šablonų sąrašo** modulį.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Publikuoti URL puslapiui.
1. Eikite į sąskaitos valdymo nusileidimo puslapį (**Mano sąskaita**), kurį sukūrėte anksčiau.
1. Ypatybių juostoje **Sąskaitos užsakymo šablonų plytelėje** modulyje, skyriuje **Nuorodos**, konfigūruokite nuorodą į užsakymo šablonų sąrašo puslapį, kurį ką tik sukūrėte.
1. Įrašykite ir publikuokite puslapį.

Užsakymo šablonų sąrašo puslapis dabar buvo sukurtas ir vartotojai gali prieiti prie jo iš sąskaitos valdymo nusileidimo puslapio.

### <a name="create-an-order-template-lines-page"></a>Kurti užsakymo šablonų eilučių puslapį

Norėdami sukurti užsakymo šablonų eilučių puslapį saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Naudokite **Sąskaitos valdymo** šabloną, kad sukurtumėte puslapį pavadinimu **Užsakymo šablono eiltuės**.
1. Vietoje **Antraštė** įtraukite antraštės fragmentą, kuris iš anksto konfigūruojamas su saito antrašte.
1. Vietoje **Poraštė** įtraukite poraštės fragmentą, kuris iš anksto konfigūruojamas su saito porašte.
1. Vietoje **Pagrindinė** įtraukite **Konteinerio** modulį. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.
1. Vietoje **Konteineris** įtraukite **Džiūvėsėlio** modulį. Modulio ypatybių juostoje, skyriuje **Nuorodos**, konfigūruokite nuorodą sąskaitos valdymo nusileidimo puslapį ir įveskite **Mano sąskaita** kaip nuorodos tekstą.
1. **Konteineris** vietoje, įtraukite **Užsakymo šablono eilutės** modulį.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Publikuoti URL puslapiui.

## <a name="onboard-business-partner-users"></a>Įtraukimo verslo partnerio vartotojai

Organizacija naudoja puslapį, kuris leidžia verslo partnerio organizacijos administratoriui įtraukti papildomus vartotojus iš tos organizacijos į B2B el. komercijos saitą. Jis nustatomas naudojant **Verslo organizacijos sąrašo** modulį. Organizacijos vartotojų puslapyje administratorius gali įtraukti ar pašalinti vartotojus, nustatyti sąskaitos balansus ir užklausos pareiškimus vartotojui.

Norėdami sukurti organizacijos vartotojų puslapį saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Naudokite **Sąskaitos valdymo** šabloną, kad sukurtumėte puslapį pavadinimu **Organizacijos vartotojai**.
1. Vietoje **Antraštė** įtraukite antraštės fragmentą, kuris iš anksto konfigūruojamas su saito antrašte.
1. Vietoje **Poraštė** įtraukite poraštės fragmentą, kuris iš anksto konfigūruojamas su saito porašte.
1. Vietoje **Pagrindinė** įtraukite **Konteinerio** modulį. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.
1. Vietoje **Konteineris** įtraukite **Džiūvėsėlio** modulį. Modulio ypatybių juostoje, skyriuje **Nuorodos**, konfigūruokite nuorodą sąskaitos valdymo nusileidimo puslapį ir įveskite **Mano sąskaita** kaip nuorodos tekstą.
1. Vietoje **Konteineris 4** įtraukite **Verslo organizacijos sąrašo** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Organizacijos vartotojų**.
1. Modulio ypatybių juostoje **Verslo organizacijos sąrašas** įjunkite **Lentelės rūšiavimą** ir **Lentelės puslapių** ypatybes. Nustatykite puslapių skaičiavimą į **5**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Publikuoti URL puslapiui.
1. Eikite į sąskaitos valdymo nusileidimo puslapį (**Mano sąskaita**), kurį sukūrėte anksčiau.
1. Ypatybių juostoje **Organizacijos vartotojų plytos** modulyje, skyriuje **Nuorodos**, konfigūruokite nuorodą į organizacijos vartotojų puslapį, kurį ką tik sukūrėte. 
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="create-invoice-pages"></a>Kurti sąskaitos puslapius

Sąskaitų sąrašo puslapis rodo esamų sąskaitų sąrašą. Jis nustatomas naudojant **Sąskaitų sąrašo** modulį. Iš sąskaitų sąrašo puslapio, vartotojai gali mokėti ar prašyti sąskaitų. 

Sąskaitos išsamios informacijos puslapis rodo sąskaitos išsamią informaciją, kuris pasirinkta sąskaitos sąrašo puslapyje. Jis nustatomas naudojant **Sąskaitos išsamios informacijos** modulį. Vartotojui pasirinkus sąskaitos ID sąskaitos sąrašo puslapyje, sąskaitos išsamios informacijos puslapis pasirodo išsamios sąskaitos sąskaitoje.

### <a name="create-an-invoices-list-page"></a>Kurti sąskaitų sąrašo puslapį

Norėdami sukurti sąskaitos sąrašo puslapį saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Naudokite **Sąskaitos valdymo** šabloną, kad sukurtumėte puslapį pavadinimu **Sąskaitų sąrašas**.
1. Vietoje **Antraštė** įtraukite antraštės fragmentą, kuris iš anksto konfigūruojamas su saito antrašte.
1. Vietoje **Poraštė** įtraukite poraštės fragmentą, kuris iš anksto konfigūruojamas su saito porašte.
1. Vietoje **Pagrindinė** įtraukite **Konteinerio** modulį. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.
1. Vietoje **Konteineris** įtraukite **Džiūvėsėlio** modulį. Modulio ypatybių juostoje, skyriuje **Nuorodos**, konfigūruokite nuorodą sąskaitos valdymo nusileidimo puslapį ir įveskite **Mano sąskaita** kaip nuorodos tekstą.
1. Vietoje **Konteineris** įtraukite **Sąskaitų sąrašo** modulį. Modulio ypatybių juostoje, **Antraštėje** įveskite **Sąskaitos**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Publikuoti URL puslapiui.
1. Eikite į sąskaitos valdymo nusileidimo puslapį (**Mano sąskaita**), kurį sukūrėte anksčiau.
1. Ypatybių juostoje **Paskyros sąskaitos plytelėje** modulyje, skyriuje **Nuorodos**, konfigūruokite nuorodą į sąskaitos sąrašo puslapį, kurį ką tik sukūrėte. 
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

### <a name="create-an-invoice-details-page"></a>Kurti sąskaitos išsamios informacijos puslapį

Norėdami sukurti sąskaitos išsamios informacijos puslapį saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Naudokite **Sąskaitos valdymo** šabloną, kad sukurtumėte puslapį pavadinimu **Sąskaitos išsami informacija**.
1. Vietoje **Antraštė** įtraukite antraštės fragmentą, kuris iš anksto konfigūruojamas su saito antrašte.
1. Vietoje **Poraštė** įtraukite poraštės fragmentą, kuris iš anksto konfigūruojamas su saito porašte.
1. Vietoje **Pagrindinė** įtraukite **Konteinerio** modulį. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.
1. Vietoje **Konteineris** įtraukite **Džiūvėsėlio** modulį. Modulio ypatybių juostoje, skyriuje **Nuorodos**, konfigūruokite nuorodą sąskaitos valdymo nusileidimo puslapyje ir įveskite **Mano sąskaita** kaip nuorodos tekstą. Tuomet konfigūruokite nuorodą į sąskaitos sąrašo puslapį ir įveskite **Sąskaitos sąrašus** kaip nuorodos tekstą.
1. Vietoje **Konteineris** įtraukite **Sąskaitos išsamios informacijos** modulį.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Publikuoti URL puslapiui.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](../starter-kit-overview.md)

[Turinio kūrimo puslapio apžvalga](../authoring-home-overview.md)

[Šablonų ir maketų apžvalga](../templates-layouts-overview.md)

[Darbas su fragmentais](../work-with-fragments.md)

[Įtraukti naują svetainės puslapį](../add-new-page.md)

[Pirkimo užbaigimo modulis](../add-checkout-module.md)

[Turinio bloko modulis](../add-hero-module.md)

[Produkto kolekcija](../product-collection-module-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
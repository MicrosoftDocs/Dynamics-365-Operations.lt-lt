---
title: "Pasiūlymų valdymo nustatymas"
description: "Šioje temoje aprašoma, kaip nustatyti „Talent“ pasiūlymus."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: fa2f2f9f67562524961352a87a7db49992776e46
ms.contentlocale: lt-lt
ms.lasthandoff: 10/22/2018

---
# <a name="set-up-offer-management"></a>Pasiūlymų valdymo nustatymas 

[!include [banner](includes/banner.md)]

Kai kandidatas perkeliamas į „Dynamics 365 for Talent: Attract“ pasiūlymo etapą, reikia užtikrinti, kad bus galima greitai kurti kandidatui skirtus pasiūlymus, juos atitinkamai patvirtinti ir išsiųsti kandidatui. Kadangi dauguma pasiūlymų standartiniai, juos galima sukurti naudojant pakartotinai naudotinus šablonus. Naudojantis „Attract“ visi pasiūlymai įtraukiami į pasiūlymų paketą, kuris yra vieno ar kelių pasiūlymo dokumentų rinkinys. 

Šioje temoje pateikiamas visų veiksmų, kuriuos turėtų atlikti „Attract“ administratorius, norėdamas kaip „Attract“ pasiūlymo valdymo galimybės dalį nustatyti kitus pasiūlymo paketo šablonus, sąrašas. Vartotojai, kuriems priskirti ne administratoriaus vaidmenys, šiomis galimybėmis naudotis negalės.

>[!NOTE]
> Pasiūlymo valdymo galimybės pateikiamos kaip išsamios įdarbinimo informacijos priedo dalis.

## <a name="offer-data"></a>Pasiūlymo duomenys 

Pasiūlymo duomenys yra mažiausias pasiūlymo paketo šablono vienetas. Įprastą pasiūlymą sudaro standartinis tekstas ir reikšmių rinkinys. Reikšmių rinkiniai yra vienintelės tarp pasiūlymų galinčios pasikeisti dalys. Kuriant pasiūlymą svarbiausias aspektas, į kurį atsižvelgia pasiūlymo kūrėjas, yra pasiūlymo paketo šablone esančių pasiūlymo duomenų vietos rezervavimo ženklų sąrašas. Norėdami nustatyti pasiūlymo duomenis, atlikite toliau nurodytus veiksmus.

1.  Eikite į **Pasiūlymo valdymas**.

1.  Išplėskite kairiosios naršymo srities skyrių **Biblioteka**, paskui eikite į **Pasiūlymo duomenys**.

    >[!NOTE]
    > Puslapyje **Pasiūlymo duomenys** yra skyrius **Kandidato informacija** ir **Informacija apie darbą**. „Attract“ siūloma keletas parengtų naudoti pasiūlymo duomenų vietos rezervavimo ženklų.
    
    > Puslapyje yra skyrių, skirtų grupuoti skirtingus pasiūlymų duomenų vietos rezervavimo ženklus į logines grupes. Šie skyriai gali padėti tvarkyti pasiūlymo duomenis ir įvesti duomenis kuriant pasiūlymą.

1.  Norėdami sukurti naują pasiūlymo duomenų skyrių, spustelėkite **Įtraukti skyrių** ir įveskite unikalų skyriaus pavadinimą.

1.  Norėdami pasiūlymo duomenų vietos rezervavimo ženklus įtraukti į bet kurį skyrių, spustelėkite **Įtraukti pasiūlymo duomenis** ir įveskite unikalų vietos rezervavimo ženklo pavadinimą.

1.  Norėdami redaguoti bet kurio skyriaus pavadinimą, laikykite žymiklį virš skyriaus pavadinimo ir atnaujinkite pavadinimą.

1.  Norėdami redaguoti bet kurio esamo pasiūlymo duomenų vietos rezervavimo ženklo pavadinimą, pirmiausia įsitikinkite, kad vietos rezervavimo ženklas nėra jokio šablono dalis. Paskui, laikydami žymiklį virš pasiūlymo duomenų vietos rezervavimo ženklo pavadinimo, atnaujinkite pavadinimą.

1. Norėdami panaikinti esamą pasiūlymo duomenų vietos rezervavimo ženklą, pirmiausia įsitikinkite, kad vietos rezervavimo ženklas nėra jokio kito šablono dalis. Paskui laikykite žymiklį virš vietos rezervavimo ženklo ir, pasirodžius šiukšliadėžės piktogramai, spustelėkite ją ir panaikinkite pasiūlymo duomenų vietos rezervavimo ženklą.
    >[!NOTE]
    > Šalia kiekvieno pasiūlymo duomenų esantis skaičius nurodo, keliems šablonams priskiriamas pasiūlymo duomenų vietos rezervavimo ženklas. 

1. Norėdami panaikinti bet kurį skyrių, laikykite žymiklį virš pavadinimo. Jei nė vienas skyriaus pasiūlymo duomenų vietos rezervavimo ženklų nerodomas jokiame šablone, spustelėję šiukšliadėžės piktogramą galite jį panaikinti. 
    >[!NOTE]
    > Panaikinus skyrių taip pat panaikinami visi to skyriaus pasiūlymo duomenų vietos rezervavimo ženklai.

Nustatę pasiūlymo duomenų vietos rezervavimo ženklus, galite juos naudoti bet kuriame dokumento šablone. Pasiūlymo duomenų vietos rezervavimo ženklai gali būti naudojami ne tik konkrečiame šablone -- tą patį rinkinį galima naudoti visuose šablonuose.

## <a name="offer-data-rules"></a>Pasiūlymo duomenų taisyklės

Daugumoje organizacijų nustatytos pasiūlymų kūrimo taisyklės. Pavyzdžiui, organizacija gali reikalauti, kad maksimalaus metinio konkrečios vietos atlyginimo pasiūlymo ir paaukštinimo lygio derinys patektų į tam tikrą intervalą, arba kad samdant naują darbuotoją būtų galimos tik kelios konkrečios pasiūlymo lygio vertės. „Attract“ šiuo metu palaiko visas tokias duomenų taisykles (naudojant CSV failą).

Norėdami parengti duomenų taisyklių CSV failą, atlikite toliau nurodytus veiksmus.

1.  Nustatykite taisyklių rinkinio pasiūlymo duomenų vietos rezervavimo ženklą. Pavyzdžiui, **Metinis atlyginimas**.

1.  Nurodykite priklausomąsias pasiūlymo duomenų vietos rezervavimo ženklo vertes. Pavyzdžiui, **Darbo vieta** ir **Lygis**.

1.  1 ir 2 stulpelyje nurodykite **Darbo vieta** ir **Lygis**.

1.  Norint įkelti intervalo vertę, 3 ir 4 stulpeliai turi būti **Metinis atlyginimas**. Norint įkelti konkrečią reikšmę, o ne intervalą, 3 stulpelis turi būti **Metinis atlyginimas**.

1.  Automatiškai užpildykite „Microsoft Excel“ failą pagal reikiamus vaidmenis.

1.  Patikrinkite, ar kiekvienoje eilutėje pateikiama unikali visų susumuotų verčių kombinacija.

1.  Failą išsaugokite CSV formatu.

Norėdami įkelti pasiūlymo duomenų taisyklių failą, atlikite toliau nurodytus veiksmus.

1.  Eikite į **Pasiūlymo valdymas**.

1.  Išplėskite kairiosios naršymo srities skyrių **Biblioteka**, paskui eikite į **Pasiūlymo duomenų taisyklės**.

1.  Spustelėjus **Naujas duomenų rinkinys** rodomas dialogo langas **Įkelti**.

1.  Nurodykite unikalų taisyklių rinkinio pavadinimą, paskui įkelkite išsaugotą CSV failą.

1.  Spustelėkite **Įtraukti**.
    Taisyklių rinkinys bus vykdomas fone ir jums bus pranešta (programoje ir elektroniniu paštu), kai veiksmas bus baigtas.

    Jums bus pranešta, jei vykdant įkėlimą kiltų klaidų. Tada galite atsisiųsti klaidų žurnalą, pataisyti failą ir įkelti jį dar kartą.

1.  Norėdami atsisiųsti taisyklių rinkinį ir atnaujinti reikšmių rinkinį (**…**), naudokitės elipsės mygtuko parinktimi. Atlikę atnaujinimą failą galite įkelti dar kartą.

1.  Galite panaikinti esamą taisyklių rinkinio įkėlimą (jei apibrėžiamas vietos rezervavimo ženklas nenaudojamas kitame dokumento šablone).

>[!NOTES]
> - Kiekvienas vietos rezervavimo ženklas gali turėti tik vieną unikalų stulpelių rinkinį, nuo kurio jis priklauso. Pavyzdžiui, jei **Metinis atlyginimas** priklauso nuo verčių **Darbo vieta** ir **Lygis**, negalite įkelti kito taisyklių rinkinio, kuriame **Metinis atlyginimas** priklauso nuo kito stulpelių rinkinio.

> - Pasiūlymo duomenų taisyklių rinkinių pavyzdžius galite atsisiųsti iš puslapio **Pasiūlymo duomenų taisyklės** skirtuko **Pavyzdžiai**.

> - Kai pasiūlymo kūrėjas perrašo pasiūlymo duomenų taisyklėse rekomenduojamas vertes, pasiūlymas pažymimas kaip nestandartinis, o pasiūlymo patvortinimo darbo eiga privaloma.

## <a name="document-templates"></a>Dokumento šablonai

Pasiūlymo dokumento šablonas gali būti pagalba administratoriams kuriant pasiūlymo laiškus. Pasiūlymo dokumento šablonas yra į pasiūlymą ketinamas įtraukti tekstas, taip pat nurodyti pasiūlymo duomenų vietos rezervavimo ženklai. 

Norėdami sukurti pasiūlymo dokumento šabloną, atlikite toliau nurodytus veiksmus.

1.  Eikite į **Pasiūlymo valdymas**.

1.  Išplėskite kairiosios naršymo srities skyrių **Biblioteka** ir eikite į **Šablonai**.

    Puslapyje **Šablonai** rodomas jau apibrėžtų dokumentų šablonų sąrašas.

1.  Norėdami sukurti naują dokumento šabloną, spustelėkite **Naujas šablonas**.

1.  Įveskite unikalų šablono pavadinimą ir spustelėkite **Kurti**.

1.  Naudodamiesi raiškiojo teksto rengykle galite įterpti arba redaguoti pasiūlymo dokumento turinį. Naudodamiesi tekstų rengyklės viršuje pateikiamomis parinktimis, galite įterpti lentelių, vaizdų ir hipersaitų.

1.  Norėdami į pasiūlymo šablono dokumentą įtraukti pasiūlymo duomenų vietos rezervavimo ženklų, atlikite toliau nurodytus veiksmus.

    - Nuvilkite nuo dešiniosios srities.

    - Saitažodžiu susiekite pasiūlymo duomenų vietos rezervavimo ženklą. Įveskite **\#**, o paskui pradėkite rašyti pasiūlymo duomenų vietos rezervavimo ženklo pavadinimą. Išplečiamajame sąraše bus rodomos parinktys. Spustelėję arba paspaudę **Enter** įveskite pasiūlymo duomenų vietos rezervavimo ženklą.

    >[!NOTES]
    > - Norėdami susieti vietos rezervavimo ženklą su pasiūlymo dokumento šablonu, nenurodant jo vertės kandidatui, laikykite žymiklį virš pasiūlymo duomenų vietos rezervavimo ženklo ir spustelėkite piktogramą **Prisegti**. Tokiu būdu vietos rezervavimo ženklas bus pastumtas į pasiūlymo dokumento šablono skyrių **Prisegti pasiūlymo duomenys**. Norėdami atsegti, atlikite tuos pačius veiksmus, bet pasiūlymo duomenų vietos rezervavimo ženklų sąraše spustelėkite **Atsegti**.

    > - Norėdami peržiūrėti aktyvių pasiūlymo duomenų vietos rezervavimo ženklų sąrašą, įjunkite dešiniosios srities skirtuką **Aktyvūs**.

    > - Įterpę vietos rezervavimo ženklą, kuriam taikomas pasiūlymo duomenų taisyklių rinkinys, galite matyti to pasiūlymo vietos rezervavimo ženklo priklausomybę nuo kitų verčių.

    > - Arba galite **Importuoti** turinį iš jūsų vietinio įrenginio .docx failo ir atlikti reikiamus pakeitimus. Tokiu būdu jums nereikės įvesti viso turinio rengyklėje.

1. Norėdami peržiūrėti pasiūlymo dokumentą, naudokitės puslapio viršuje esančia parinktimi **Peržiūra**.

1. Norėdami kontroliuoti, ar pasiūlymo kūrėjas gali redaguoti pasiūlymo dokumento turinį, naudokitės puslapio viršuje esančia parinktimi **Valdyti teisę**. Jei norite, kad pasiūlymo kūrėjas galėtų tik įterpti vietos rezervavimo ženklo vertes, bet negalėtų redaguoti teksto, nustatykite teisės vertę **Ne**.

1. Spustelėkite **Įrašyti** ir išsaugokite savo eigą. Šablonas bus išsaugotas juodraščio būsenos.

1. Norėdami baigti ir pažymėti dokumentą pagal tai, koks jis buvo paskelbtas, spustelėkite **Baigti**.

1. Galite matyti, kurie dokumento šablonai šiuo metu aktyvūs (juodraščio režimu), taip pat yra archyvuojami ir nebus naudojami naudojantis dokumentų šablonų bibliotekos nukreipimo patirtimi.

>[!NOTE]
> Galite panaikinti bet kurį pasiūlymo dokumento šabloną, kuris nėra esamo pasiūlymo paketo šablono dalis.


## <a name="offer-package-templates"></a>Pasiūlymo paketo šablonai

Pasiūlymų paketai yra pasiūlymo artefaktai, kurie bendrinami su kandidatu ir yra sudaryti iš vieno ar kelių pasiūlymo dokumento šablonų. Norėdami sukurti pasiūlymo paketą, atlikite toliau nurodytus veiksmus.

1.  Eikite į **Pasiūlymo valdymas**.

1.  Kairiojoje naršymo srityje eikite į **Pakuotės**.

    Rodomas aktyvių paketo šablonų, kuriais gali naudotis pasiūlymo kūrėjai, sąrašas.

1.  Norėdami sukurti naują pasiūlymo paketą, spustelėkite **Naujas paketas**.

1.  Įveskite unikalų pavadinimą ir spustelėkite **Kurti**.

1.  Spustelėkite **Įtraukti šabloną**.

    >[!NOTES]
    > - Galite pasirinkti sukurti naują šabloną arba pasirinkti iš esamų.

    > - Pasirinkę įtraukti esamą šabloną turite įsitikinti, kad pasiūlymo dokumento šablonas įrašytas, baigtas ir pažymėtas kaip aktyvus.
    
    > - Galite pasirinkti tiek dokumentų šablonųų, kiek norite. 
    
1.  Spustelėkite **Atlikta** ir grįžkite į **Paketų valdymas**.

    Galite sukonfigūruoti dokumentų seką, taip pat pažymėti, ar kuriant pasiūlymą reikalingas konkretaus pasiūlymo dokumentas. Pasiūlymo kūrėjas turi galimybę panaikinti dokumentus, pažymėtus **Nebūtina**.

1. Norėdami įrašyti pasiūlymo paketo šabloną, kad juo galėtų naudotis visi pasiūlymo kūrėjai, spustelėkite **Įrašyti ir paskelbti**.

   Norėdami peržiūrėti pasiūlymo paketo šablonų juodraščius, eikite į skirtuką **Juodraščiai**. Atlikus pasiūlymo paketo šablono pakeitimą, būtina jį įrašyti ir paskelbti iš naujo.

## <a name="configure-an-offer-process"></a>Pasiūlymo proceso konfigūravimas

Yra keletas pasiūlymo kūrimo proceso dalių, kurias gali konfigūruoti „Attract“ administratorius.

- **Pasiūlymų patvirtinimai** – pasirinkite, ar, prieš siunčiant pasiūlymą kandidatui, būtina jį patvirtinti. Jei esate administratorius, taip pat galite nuspręsti, ar visi pasiūlymų patvirtinimai vyks eilės tvarka, ar lygiagrečia patvirtinimo darbo eiga. Taip pat gali nurodyti, ar pasiūlymų tvirtintojams būtina tvirtinant pasiūlymą pateikti ir komentarą. Visų nestandartinių pasiūlymų atveju patvirtinimai būtini.

- **Kandidato pasiūlymo patirtis** – jei esate administratorius, galite pasirinkti nustatyti, ar visi pasiūlymai turės galiojimo datą, ir, jei taip, koks bus numatytasis galiojimo datos poslinkis. Taip pat galite sukonfigūruoti ar kandidatai gali atmesti pasiūlymą.

- **El. parašai** – šiuo metu vienintelė galima elektroninio parašo parinktis – galimybė kandidatams priimant pasiūlymą pasiūlymo pakete įvesti savo vardą. Ateityje galėsime pasiūlyti partnerių integraciją su kitais elektroninio parašo tiekėjais.


Norėdami daugiau sužinoti apie pasiūlymo kūrimo procesą, žr. [Pasiūlymų kūrimas, tvirtinimas ir pasirašymas](./creating-offers.md).


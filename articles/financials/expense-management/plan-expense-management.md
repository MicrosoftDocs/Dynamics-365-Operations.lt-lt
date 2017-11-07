---
title: "Konfigūruoti išlaidų valdymą"
description: "Šiame straipsnyje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš konfigūruodami Išlaidų valdymą programoje „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 198e37258f45966b92d963cc0c233d4790ca049e
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="configure-expense-management"></a>Konfigūruoti išlaidų valdymą

[!include[banner](../includes/banner.md)]


Šioje temoje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš konfigūruodami „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ modulį Išlaidų valdymas. Modulyje Išlaidų valdymas galite saugoti informaciją apie mokėjimo būdus, kelionių paraiškas, išlaidų ataskaitas, strategijas ir t. t.

Kadangi daugelis sprendimų, kuriuos priimate planuodami savo Išlaidų valdymo konfigūraciją, paremti jūsų organizacijos hierarchija ir finansine struktūra, turite žr. tų sričių planavimo dokumentus.

## <a name="intercompany-expenses"></a>Vidinės įmonės išlaidos

Kai įgalinate vidinės įmonės išlaidas, juridiniams subjektams ir darbuotojams leidžiate numatyti išlaidas kito juridinio subjekto vardu ir rinkti mokėjimus iš įdarbinusio juridinio subjekto, priklausančio jūsų organizacijai. Pavyzdžiui, juridinio subjekto A darbuotojas įvykdo projektą juridiniam subjektui B ir projekto metu patiriama su keliavimu susijusių išlaidų. Jei įgalintos vidinės įmonės išlaidos, darbuotojas gali pateikti išlaidų ataskaitą, kurioje išlaidos bus užregistruotos juridiniam subjektui B, o jas padengti turės juridinis subjektas A. Jei jūsų organizacijoje nėra kelių juridinių subjektų, įgalinti vidinės įmonės išlaidų nereikia.

**Sprendimas:** ar norite įgalinti vidinės įmonės išlaidas?

## <a name="financial-management"></a>Finansų valdymas

Išlaidų valdymas yra glaudžiai integruotas su jūsų organizacijos finansų valdymu. Didelė modulio Išlaidų valdymas konfigūracijos dalis bus paremta sprendimais, kuriuos priėmėte dėl savo organizacijos finansų. Toliau pateikiamuose skyriuose aprašomos įvairios sritys, kurioms reikia planavimo ir sprendimų, paremtų jūsų organizacijos finansiniais sprendimais ir vadovavimo komandos patarimais.

### <a name="per-diems"></a>Dienpinigiai

Turite apibrėžti darbuotojų dienpinigius, kuriuos suteikia jūsų organizacija. Kadangi dienpinigiai paprastai naudojami padengti tokioms išlaidoms kaip maistas, apgyvendinimas ir kitos papildomos išlaidos, galite kurti dienpinigių, kuriuos suteikia jūsų organizacija, taisykles. dienpinigių tarifus galima nustatyti pagal metų laiką, kelionės vietą, arba abu. Apibrėždami dienpinigių taisyklę, galite nurodyti, kad, jeigu darbuotojas nemokamai gauna maitinimą ar paslaugas, iš dienpinigių bus išskaitytas tam tikras procentas. Taip pat galite apibrėžti dienpinigių tarifų pakopas, taip nustatant mažiausią ir didžiausią valandų skaičių, kada dienpinigių tarifas gali būti taikomas darbuotojo kelionei.

**Sprendimai:**

- Toliau pateiktos numatytosios pirmosios ir paskutiniosios dienų dienpinigių taisykles.

    - Koks yra minimalus valandų skaičius, kurio darbuotojas gali reikalauti ir vis tiek gauti dienpinigius?
    - Ar pirmąją dieną ir paskutiniąją dieną maistui siūloma mažesnė suma? Jei suma sumažėjo, koks yra sumažėjimo procentas?
    - Ar pirmąją dieną ir paskutiniąją dieną viešbučiui siūloma mažesnė suma? Jei suma sumažėjo, koks yra sumažėjimo procentas?
    - Ar pirmąją dieną ir paskutiniąją dieną patirtoms kitoms išlaidoms siūloma mažesnė suma? Jei suma sumažėjo, koks yra sumažėjimo procentas?

- Toliau pateiktos numatytosios dienpinigių taisyklės.

    - Ar kiekvienam valgiui dienpinigių skiriama tam tikru procentu mažiau, jei, pavyzdžiui, maistas yra nemokamas? Jei suma sumažėjo, koks yra kiekvieno valgio sumos sumažėjimo procentas?
    - Ar maisto dienpinigių sumažinimas skaičiuojamas dienai, kelionei, ar pagal valgių per dieną skaičių?
    - Ar dienpinigių sumas reikia apvalinti įprastai, ar iki didesnio skaičiaus?
    - Ar dienpinigiai skaičiuojami 24 valandų laikotarpiui, ar kalendorinei dienai?

- Toliau nurodytos dienpinigių taisyklės pagal vietą.

    - Ar dienpinigių tarifai skiriasi atsižvelgiant į vietą? Kokios vietos yra įtrauktos?
    - Jei dienpinigių tarifai skiriasi atsižvelgiant į vietą, kokia procentinė suma yra numatyta tolesnių tipų išlaidoms kiekvienoje vietoje.

        - Maitinimo išlaidos
        - Viešbutis
        - Kitos išlaidos

### <a name="expense-management-journals-and-accounts"></a>Išlaidų valdymo žurnalai ir sąskaitos

Valdant išlaidas reikia naudoti kelis žurnalus ir sąskaitas. Turite nuspręsti, pvz., ar tą pačią sąskaitą naudoti avansams grynaisiais pinigais ir kredito kortelės konfliktams.

**Sprendimai:**

- Kuriame DK žurnale registruojamos patvirtintos išlaidų ataskaitos?
- Kuri sąskaita naudojama avansams grynaisiais pinigais?
- Ar avansai grynaisiais pinigais turėtų būti registruojami nedelsiant?

### <a name="payment-methods"></a>Mokėjimo būdai

Kai darbuotojams leidžiate jūsų įmonės vardu numatyti išlaidas, turite apibrėžti mokėjimo metodus, kuriuos darbuotojams leidžiama naudoti. Pavyzdžiui, galite darbuotojams leisti naudoti grynųjų pinigų ar įmonės kredito kortelę. Taip pat darbuotojams galite leisti naudoti asmenines kredito korteles, ir tada jiems sumokėti kompensacijas. Dėl kiekvieno leidžiamo mokėjimo būdo turite atlikti toliau nurodytus sprendimus.

**Sprendimai:**

- Kokie mokėjimo būdai leidžiami?
- Kam priklauso mokėjimo būdo išlaidos?
- Ar yra koks korespondentinės sąskaitos tipas? Jei yra korespondentinės sąskaitos tipas, koks jis?
- Jei korespondentinė sąskaita yra, kuri ji?
- Jei mokėjimo būdas yra kredito kortelė, ar mokėjimo būdas turėtų būti naudojamas tik su importuotomis operacijomis?

### <a name="expense-categories-and-shared-categories"></a>Išlaidų kategorijos ir bendro naudojimo kategorijos

Darbuotojams kuriant išlaidų ataskaitą, visos jų įrašomos išlaidos turi būti susietos su išlaidų kategorija. Išlaidų kategorijos išvedamos iš bendro naudojimo kategorijų, kurios gali būti bendrai naudojamos visuose jūsų organizacijos juridiniuose subjektuose. Šios kategorijos taip pat gali būti bendrai naudojamos modulyje Projektų valdymas ir apskaita – tai priklauso nuo to, kaip apibrėžta jūsų organizacija. Pagal savo organizacijos apibrėžtį ir diegimo komandos patarimus nustatykite, ar modulyje Išlaidų valdymas naudojamos kategorijos bus naudojamos tik modulyje Išlaidų valdymas, ar jas reikia bendrai naudoti moduliuose Projektų valdymas ir apskaita bei Išlaidų valdymas. Atkreipkite dėmesį, kad šios kategorijos gali būti bendrai naudojamos Projektui ir Išlaidoms arba Projektui ir Gamybai, bet ne Išlaidoms ir Gamybai. Dėl kiekvienos išlaidų kategorijos turite priimti toliau nurodytus sprendimus.

**Sprendimai:**

- Kas yra išlaidų kategorija? Pavyzdžiui, skrydžių, viešbučio ar kilometražo kategorijos.
- Ar išlaidų kategoriją taip pat galima naudoti modulyje Projektų valdymas ir apskaita?
- Kas yra išlaidų tipas?
- Koks yra numatytasis išlaidų kategorijos mokėjimo būdas?
- Ar išlaidų kategorijos išlaidas reikia detaliai išvardyti?
- Kuri yra pagrindinė numatytoji išlaidų kategorijos sąskaita?
- Kokia yra numatytoji išlaidų kategorijos prekių PVM grupė?
- Ar leidžiami papildomi išlaidų kategorijos mokėjimo būdai? Jei leidžiami papildomi mokėjimo būdai, kokie jie?
- Ar šioje išlaidų kategorijoje yra subkategorijų? Jei subkategorijų yra, taip pat turite priimti tolesnius sprendimus.

    - ar kuri nors subkategorija neįtraukta į mokesčių susigrąžinimo procesą?
    - Kokia yra subkategorijų prekių PVM grupė?

Jei išlaidų kategorija taip pat naudojama modulyje Projektų valdymas ir apskaita, atsakykite į likusius klausimus. Kitu atveju pereikite prie kito skyriaus.

- Kokios išlaidų sąskaitos bus naudojamos toliau nurodytoms išlaidoms?

    - Savikaina
    - Atlyginimo paskirstymas
    - NG - Savikaina
    - Išlaidos – prekė
    - Vykdomas projektas – Išlaidų vertė – Prekė
    - Sukauptas nuostolis
    - NG – sukauptas nuostolis

- Kokios pajamų sąskaitos bus naudojamos toliau nurodytiems dalykams?

    - Įplaukos, kurioms išrašyta SF
    - Sukauptos įplaukos – pardavimo vertė
    - NG – Pardavimo vertė
    - Sukauptos įplaukos – gamyba
    - NG – gamyba
    - Sukauptos įplaukos – pelnas
    - NG – pelnas
    - Sukauptos įplaukos – abonementas
    - NG – abonementas

### <a name="taxes"></a>Mokesčiai

Turite nustatyti, kurie su išlaidomis susiję mokesčiai įtraukti ar įgalinti išlaidų ataskaitose.

**Sprendimai:**

- Ar į išlaidų sumas įtrauktas PVM?
- Ar turėtų būti įgalintas išlaidų mokesčių susigrąžinimas?

    > [!NOTE]
    > Jei, planuodami didžiąją knygą, nusprendėte taikyti JAV PVM ir naudojimo mokesčio taisykles, išlaidoms mokesčių susigrąžinimo funkcijos įjungti negalite. (Norėdami taikyti JAV PVM ir naudojimo mokesčio taisykles, parinktį **Taikyti PVM apmokestinimo taisykles** nustatykite kaip **Taip**.)

## <a name="policies"></a>Strategijos

Sukūrę išlaidų ataskaitų strategijų, savo organizacijai galite padėti sutaupyti laiko ir pinigų, kai darbuotojai jos vardu numato išlaidas. Strategijos padeda užtikrinti, kad darbuotojai neviršytų biudžeto, pateiktų visą reikiamą informaciją ir pinigus leistų, tik kai reikia. Dėl kiekvienos išlaidų ataskaitų strategijos ir kiekvienos išlaidų ataskaitų patvirtinimo strategijos, kurią sukuriate, turite priimti toliau nurodytus sprendimus.

**Sprendimai:**

- Koks yra strategijos pavadinimas?
- Kam išlaidų strategija skirta?
- Jei anksčiau nusprendėte įgalinti vidinės įmonės išlaidas, kurioms jūsų organizacijos įmonėms ši strategija bus taikoma?
- Kada strategija įsigalioja?
- Kai strategija baigia galioti?
- Kas yra strategijos taisyklė?
- Koks yra strategijos taisyklės rezultatas?


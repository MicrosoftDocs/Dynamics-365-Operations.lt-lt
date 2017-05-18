---
title: "Konfigūruoti išlaidų valdymą"
description: "Šiame straipsnyje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš konfigūruodami Išlaidų valdymą programoje „Microsoft Dynamics AX“. Išlaidų valdymo srityje galite saugoti informaciją apie mokėjimo būdus, kelionės paraiškas, išlaidų ataskaitas ir, be visa kita, strategijas."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 447ba56a279a29392b00119730c3594fa4ea80f6
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="configure-expense-management"></a>Konfigūruoti išlaidų valdymą

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš konfigūruodami Išlaidų valdymą programoje „Microsoft Dynamics AX“. Išlaidų valdymo srityje galite saugoti informaciją apie mokėjimo būdus, kelionės paraiškas, išlaidų ataskaitas ir, be visa kita, strategijas. 

Kadangi daugelis sprendimų, kuriuos priimate planuodami savo Išlaidų valdymo konfigūraciją, paremti jūsų organizacijos hierarchija ir finansine struktūra, turite žr. tų sričių planavimo dokumentus.

## <a name="intercompany-expenses"></a>Vidinės įmonės išlaidos
Kai įgalinate vidinės įmonės išlaidas, juridiniams subjektams ir darbuotojams leidžiate numatyti išlaidas kito juridinio subjekto jūsų organizacijoje vardu ir iš jo rinkti mokėjimus. Pvz., darbuotojas juridiniame subjekte A atlieka projektą juridiniam subjektui B. Jei įgalintos vidinės įmonės išlaidos, darbuotojas gali juridiniam subjektui B pateikti tabelį ir iš subjekto gauti mokėjimą. Jei jūsų organizacijoje nėra kelių juridinių subjektų, įgalinti vidinės įmonės išlaidų jums nereikės. **Sprendimas:** ar norite įgalinti vidinės įmonės išlaidas?

## <a name="financial-management"></a>Finansų valdymas
Išlaidų valdymas yra glaudžiai integruotas su jūsų organizacijos finansų valdymu. Didelė Išlaidų valdymo konfigūracijos dalis bus paremta sprendimais, kuriuos priėmėte dėl savo organizacijos finansų. Toliau pateikiamuose skyriuose aprašomos skirtingos sritys, kurioms reikia planavimo ir sprendimų, paremtų jūsų organizacijos finansiniais sprendimais ir vadovavimo komandos patarimais.

### <a name="per-diems"></a>Dienpinigiai

Turite apibrėžti darbuotojų dienpinigius, kuriuos suteikia jūsų organizacija. Kadangi dienpinigiai paprastai naudojami padengti tokioms išlaidoms kaip maistas, apgyvendinimas ir kitos papildomos išlaidos, galite kurti dienpinigių, kuriuos suteikia jūsų organizacija, taisykles. Dienpinigių tarifus galima nustatyti pagal metų laiką, kelionės vietą, arba abu. Apibrėždami dienpinigių taisyklę, galite nurodyti, kad, jeigu darbuotojas nemokamai gauna maitinimą ar paslaugas, iš dienpinigių bus išskaitytas tam tikras procentas. Taip pat galite apibrėžti dienpinigių tarifų pakopas, taip nustatant mažiausią ir didžiausią valandų skaičių, kada dienpinigių tarifas gali būti taikomas darbuotojo kelionei. **Sprendimai:**

-   Toliau pateiktos numatytosios pirmosios ir paskutiniosios dienų dienpinigių taisykles.
    -   Koks yra minimalus valandų skaičius, kurio darbuotojas gali reikalauti ir vis tiek gauti dienpinigius?
    -   Ar pirmąją ir paskutiniąją dieną maistui siūloma mažesnė suma? Jei taip, koks sumažėjimo procentas?
    -   Ar pirmąją ir paskutiniąją dieną viešbučiui siūloma mažesnė suma? Jei taip, koks sumažėjimo procentas?
    -   Ar pirmąją ir paskutiniąją dieną patirtoms kitoms išlaidoms siūloma mažesnė suma? Jei taip, koks sumažėjimo procentas?
-   Toliau pateiktos numatytosios dienpinigių taisyklės.
    -   Ar kiekvienam valgiui dienpinigių skiriama tam tikru procentu mažiau, jei, pavyzdžiui, maistas yra nemokamas? Jei taip, koks yra sumažėjimo procentas kiekvienam valgiui?
    -   Ar maisto dienpinigių sumažinimas skaičiuojamas dienai, kelionei, ar pagal valgių per dieną skaičių?
    -   Ar dienpinigių sumas reikia apvalinti įprastai, ar aukštyn?
    -   Ar dienpinigiai skaičiuojami 24 valandų laikotarpiui, ar kalendorinei dienai?
-   Toliau nurodytos dienpinigių taisyklės pagal vietą.
    -   Ar dienpinigių tarifai skiriasi atsižvelgiant į vietą, ir kokios vietos įtrauktos?
    -   Jei dienpinigių tarifas pagal kiekvieną vietą skiriasi, koks sumos procentas suteikiamas:
        -   maistui;
        -   viešbučiui;
        -   kitoms išlaidoms.

### <a name="expense-management-journals-and-accounts"></a>Išlaidų valdymo žurnalai ir sąskaitos

Valdant išlaidas reikia naudoti kelis žurnalus ir sąskaitas. Turite nuspręsti, pvz., ar tą pačią sąskaitą naudoti avansams grynaisiais pinigais ir kredito kortelės konfliktams. **Sprendimai:**

-   Kuriame DK žurnale registruojamos patvirtintos išlaidų ataskaitos?
-   Kuri sąskaita naudojama avansams grynaisiais pinigais?
-   Ar avansai grynaisiais pinigais turėtų būti registruojami nedelsiant?

### <a name="payment-methods"></a>Mokėjimo būdai

Kai darbuotojams leidžiate jūsų įmonės vardu numatyti išlaidas, turite apibrėžti mokėjimo metodus, kuriuos darbuotojams leidžiama naudoti. Pavyzdžiui, galite darbuotojams leisti naudoti grynųjų pinigų ar įmonės kredito kortelę. Taip pat darbuotojams galite leisti naudoti asmenines kredito korteles, ir tada jiems sumokėti kompensacijas. Dėl kiekvieno leidžiamo mokėjimo būdo turite atlikti toliau nurodytus sprendimus. **Sprendimai:**

-   Kokie mokėjimo būdai leidžiami?
-   Kam priklauso mokėjimo būdo išlaidos?
-   Ar yra koks korespondentinės sąskaitos tipas? Jei taip, koks?
-   Jei korespondentinė sąskaita yra, kuri ji?
-   Jei mokėjimo būdas yra kredito kortelė, ar mokėjimo būdas turėtų būti naudojamas tik su importuotomis operacijomis?

### <a name="expense-categories-and-shared-categories"></a>Išlaidų kategorijos ir bendro naudojimo kategorijos

Darbuotojams kuriant išlaidų ataskaitą, visos jų įrašomos išlaidos turi būti susietos su išlaidų kategorija. Išlaidų kategorijos išvedamos iš Bendro naudojimo kategorijų, kurios gali būti bendrai naudojamos visuose jūsų organizacijos juridiniuose subjektuose. Šios kategorijos taip pat gali būti bendrai naudojamos Projektų valdymo ir apskaitos modulyje – tai priklauso nuo to, kaip apibrėžta jūsų organizacija. Pagal savo organizacijos apibrėžtį ir diegimo komandos patarimus nustatykite, ar valdant išlaidas naudojamos kategorijos turėtų būti naudojamos tik išlaidoms, ar jas turėtų bendrai naudoti Projektas ir Išlaidos. Atkreipkite dėmesį, kad šios kategorijos gali būti bendrai naudojamos Projektui ir Išlaidoms arba Projektui ir Gamybai, bet ne Išlaidoms ir Gamybai. Dėl kiekvienos išlaidų kategorijos turite priimti toliau nurodytus sprendimus. **Sprendimai:**

-   Kas yra išlaidų kategorija? Pvz., skrydžių, viešbučių, ar kilometražo.
-   Ar šią išlaidų kategoriją taip galima naudoti Projektų valdymo ir apskaitos modulyje?
-   Kas yra išlaidų tipas?
-   Koks yra numatytasis išlaidų kategorijos mokėjimo būdas?
-   Ar šios kategorijos išlaidas reikia detaliai išvardyti?
-   Kuri yra pagrindinė numatytoji išlaidų kategorijos sąskaita?
-   Kokia yra numatytoji išlaidų kategorijos prekių PVM grupė?
-   Ar leidžiami papildomi išlaidų kategorijos mokėjimo būdai? Jei taip, kokie jie?
-   Ar išlaidų kategorijoje yra subkategorijų? Jei taip:
    -   ar kuri nors subkategorija neįtraukta į mokesčių susigrąžinimo procesą?
    -   Kokia yra subkategorijų prekių PVM grupė?

    Jeigu ši išlaidų kategorija taip pat naudojama Projektų valdymo ir apskaitos modulyje, atsakykite į likusius klausimus. Kitu atveju šiame skyriuje atlikote viską.
-   Kokios išlaidų sąskaitos bus naudojamos toliau nurodytiems dalykams?
    -   Išlaidos
    -   Atlyginimo paskirstymas
    -   NG – savikaina
    -   Išlaidos – prekė
    -   NG – savikaina vertė – prekė
    -   Sukauptas nuostolis
    -   NG – sukauptas nuostolis
-   Kokios pajamų sąskaitos bus naudojamos toliau nurodytiems dalykams?
    -   Įplaukos, kurioms išrašyta SF
    -   Sukauptos įplaukos – pardavimo vertė
    -   NG – Pardavimo vertė
    -   Sukauptos įplaukos – gamyba
    -   NG – gamyba
    -   Sukauptos įplaukos – pelnas
    -   NG – pelnas
    -   Sukauptos įplaukos – abonementas
    -   NG – abonementas

 

### <a name="taxes"></a>Mokesčiai

Turite nustatyti, kurie su išlaidomis susiję mokesčiai įtraukti ar įgalinti išlaidų ataskaitose. **Sprendimai:**

-   Ar į išlaidų sumas įtrauktas PVM?
-   Ar turėtų būti įgalintas išlaidų mokesčių susigrąžinimas?

Atkreipkite dėmesį, kad, jei planuodami DK nusprendėte taikyti JAV PVM ir naudoti mokesčių taisykles, o tai atliekama lauką **Taikyti PVM apmokestinimo taisykles** perjungiant į Taip, išlaidų mokesčių susigrąžinimo įgalinti negalima.

## <a name="policies"></a>Strategijos
Galite sukurti išlaidų ataskaitų strategijas, kad jūsų organizacija galėtų sutaupyti laiko ir pinigų, kai darbuotojai jos vardu numato išlaidas. Strategijomis užtikrinama, kad darbuotojai neviršytų biudžeto, pateiktų visą reikiamą informaciją ir pinigus leistų tik kai tai būtina. Dėl kiekvienos išlaidų ataskaitų strategijos ir kiekvienos išlaidų ataskaitų patvirtinimo strategijos, kurią sukuriate, turite priimti toliau nurodytus sprendimus. **Sprendimai:**

-   Koks yra strategijos pavadinimas?
-   Kam išlaidų strategija skirta?
-   Jei anksčiau nusprendėte įgalinti vidinės įmonės išlaidas, kurioms jūsų organizacijos įmonėms ši strategija bus taikoma?
-   Kada strategija įsigalioja?
-   Kai strategija baigia galioti?
-   Kas yra strategijos taisyklė?
-   Koks yra strategijos taisyklės rezultatas?






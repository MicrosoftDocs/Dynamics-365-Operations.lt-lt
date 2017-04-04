---
title: "Konfigūruoti Mokėtinas sumas"
description: "Šiame straipsnyje aprašomi puslapiai, kuriuos naudojate norėdami nustatyti pagrindines ir laisvai pasirenkamas funkcijas programos „Microsoft Dynamics AX“ modulyje Mokėtinos sumos. Jame taip pat aprašomi nustatymo veiksmai, kuriuos turite atlikti prieš pradėdami nustatyti Mokėtinas sumas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: b06623a0eb754654f41c50b92af67dc94a069663
ms.lasthandoff: 03/31/2017


---

# <a name="configure-accounts-payable"></a>Konfigūruoti Mokėtinas sumas

Šiame straipsnyje aprašomi puslapiai, kuriuos naudojate norėdami nustatyti pagrindines ir laisvai pasirenkamas funkcijas programos „Microsoft Dynamics AX“ modulyje Mokėtinos sumos. Jame taip pat aprašomi nustatymo veiksmai, kuriuos turite atlikti prieš pradėdami nustatyti Mokėtinas sumas.

<a name="prerequisites-for-accounts-payable-setup"></a>Būtinosios Mokėtinų sumų sąrankos sąlygos
----------------------------------------

Prieš nustatydami Mokėtinas sumas, turite atlikti toliau nurodytą sąranką.

-   Didžiojoje knygoje.
    -   Jei planuojate naudoti mokėjimų žurnalus, juos nustatykite.
    -   Jei planuojate vykdyti valiutos kurso koregavimus, puslapyje Valiutos nustatykite valiutų kodus, puslapyje Valiutų kursų tipai nustatykite valiutų kursų tipus, o Valiutų kursų puslapyje nustatykite valiutų kursus.
-   Grynųjų pinigų ir banko valdymo modulyje nustatykite banko sąskaitas, kurias norite naudoti su mokėjimo būdais.

## <a name="setup-pages-for-accounts-payable"></a>Atidaromas puslapis mokėtinos sąskaitos

Norėdami nustatyti pagrindines kiekvieno juridinio subjekto Mokėtinų sumų funkcijas, naudokite toliau nurodytus puslapius. Puslapiai išvardyti rekomenduojama sąrankos tvarka. Norėdami palengvinti sąrankos procesą, galite kurti šablonus iš pirmųjų sukurtų įrašų. Šablone reikšmės paprastai įvedamos keliuose laukuose, kad būtų atspindimos savybės, kurias organizacija nori pritaikyti tam tikram klientų tipui.
1.  Mokėjimo sąlygų puslapyje apibrėžkite mokėjimo sąlygas, kurias norite priskirti pardavimo užsakymams, pirkimo užsakymams, klientams ir tiekėjams, ir kurios apibrėžia SF terminus.
2.  Puslapyje Mokėjimo metodai – tiekėjai kurkite ir prižiūrėkite informaciją apie tai, kaip organizacija moka savo tiekėjams.
3.  Tiekėjų grupių puslapyje kurkite ir prižiūrėkite tiekėjų grupes su tokiais pat svarbiais registravimo, sudengimo ir mokėjimo, ataskaitų kūrimo bei prognozavimo parametrais.
4.  Tiekėjų registravimo profilių puslapyje apibrėžkite, kaip tiekėjų operacijos registruojamos į DK.
5.  Mokėtinų sumų parametrų puslapyje nustatykite numatytąsias nuostatas, taikomas, jei nenurodoma konkretesnė nuostata, įvairių funkcijų parametrai ir įvairios Mokėtinų sumų numeracijos.
6.  Formų sąrankos puslapyje apibrėžkite įvairių dokumentų, susijusių su tiekėjais ir kuriuos naudoja organizacija gavimams iš tiekėjų sekti ir mokėjimų tiekėjams nurodyti srauto priežastis, formatą.
7.  Tiekėjų puslapyje kurkite ir prižiūrėkite tiekėjų sąskaitas bei mokesčių institucijas, kurioms jūsų organizacija teikia PVM ataskaitas.

## <a name="optional-setup-pages-for-accounts-payable"></a>Pasirinktinės sąrankos puslapių mokėtinos sąskaitos
Be pagrindinių funkcijų, Mokėtinos sumos turi kitų funkcijų, kurias galite nustatyti.

Papildomi sąrankos puslapiai sisteminami pagal funkcijas.

**Policies**
-   Tiekėjo SF strategijos puslapyje nustatykite tiekėjo SF strategijas.

**Invoice matching**

-   SF sumų leistinų nuokrypių puslapyje nustatykite leistinus SF sumų nuokrypius.
-   Puslapyje Gretinimo strategija nustatykite dvišalio ir trišalio gretinimo strategijas.
-   Puslapyje Leistini kainų nuokrypiai nustatykite leistinus vieneto kainų nuokrypius.
-   Leistinų prekių kainų nuokrypių grupių puslapyje nustatykite leistinų prekių kainų nuokrypių grupes.
-   Leistinų tiekėjo kainų nuokrypių grupių puslapyje nustatykite leistinų tiekėjo kainų nuokrypių grupes.
-   Puslapyje Leistini išlaidų nuokrypiai nustatykite leistinus išlaidų nuokrypius.

**Workflow**

-   Mokėtinų sumų darbo eigų puslapyje nustatykite žurnalų patvirtinimo ir pirkimo paraiškų darbo eigų konfigūracijas.

**Reasons**

-   Tiekėjo priežasčių puslapyje nustatykite priežasčių kodus.

**Charges**

-   Puslapyje Išlaidų kodas nustatykite išlaidų kodus, naudojamus pirkimo užsakymuose.
-   Tiekėjo mokesčių grupės puslapyje, kurti ir tvarkyti mokesčių grupes tiekėjų.
-   Prekių išlaidų grupių puslapyje kurkite ir prižiūrėkite prekių išlaidų grupes.
-   Automatinių išlaidų puslapyje apibrėžkite išlaidas, kurios yra automatiškai priskiriamos užsakymams.

**Supplementary items**

-   Papildomų prekių grupių – tiekėjų puslapyje kurkite ir prižiūrėkite tiekėjų papildomų prekių grupes.
-   Papildomų prekių grupių – atsargų puslapyje kurkite ir prižiūrėkite prekių papildomų prekių grupes.

**Distribution**

-   Pristatymo sąlygų puslapyje kurkite ir prižiūrėkite prekės perdavimo iš pardavėjo pirkėjui sąlygas.
-   Pristatymo būdų puslapyje kurkite ir prižiūrėkite transportavimo būdus, naudojamus pristatant užsakymą iš pardavėjo pirkėjui.
-   Paskirties kodų puslapyje kurkite ir prižiūrėkite pristatymo vietų identifikatorius ir aprašus.

**Forms**

-   Formų pastabų puslapyje sukurkite standartinį tekstą, rodomą įvairiuose puslapiuose.
-   Formų rūšiavimo parametrų puslapyje nustatykite paraiškų, gavimų sąrašų, važtaraščių ir sąskaitų faktūrų rūšiavimo tvarką.
-   Spausdinimo valdymo sąrankos puslapyje nustatykite puslapių originalų ir kopijų spausdinimo valdymo informaciją.

**Payments**

-   Mokėjimo nuolaidų puslapyje nustatykite ir prižiūrėkite mokėjimo nuolaidų gavimo sąlygas. Mokėjimo nuolaidų kodai susiejami su tiekėjais ir taikomi pirkimo užsakymams.
-   Mokėjimų grafikų puslapyje nustatykite mokėjimų grafikus, kurie naudojami valdant įmokų mokėjimus tiekėjams.
-   Mokėjimo dienų puslapyje apibrėžkite mokėjimo dienas, naudojamas terminams skaičiuoti, ir nurodykite konkrečios savaitės ar mėnesio dienos mokėjimo dienas.
-   Mokėjimo mokesčio puslapyje kurkite ir prižiūrėkite su tiekėjais susietus mokėjimų mokesčius.
-   Mokėjimo instrukcijos puslapyje kurkite ir prižiūrėkite mokėjimų instrukcijas.

**Statistics**

-   Skirstymo pagal terminus laikotarpių apibrėžčių puslapyje nustatykite naudotojo apibrėžtus intervalus, kurie naudojami analizuoti tiekėjų sąskaitų paskirstymui pagal mokėjimo terminus.
-   Verslo šakos puslapyje kurkite verslo šakų (LOB) kodus, priskiriamus tiekėjams.

**Mokesčio 1099**

-   Dėl to **1099 laukuose** puslapyje, tikrinti ir atnaujinti minimalias sumas, apie kuriuos turi pranešti, kad vidaus pajamų tarnybos (IRS), pagal naujausius IRS reikalavimus.

## <a name="optional-setup-for-other-modules"></a>**Pasirinktinė sąranka kitų modulių**
**Organization administration**

-   Numeracijų puslapyje nustatykite SF numerių numeracijų grupes.
-   Toliau nurodytuose puslapiuose nustatykite adreso informaciją.
    -   Adreso sąranka
    -   NAF kodai
    -   Importuoti pašto indeksus

**General ledger**

-   Finansinių dimensijų puslapyje nustatykite finansines dimensijas.
-   Toliau nurodytuose puslapiuose nustatykite mokesčių informaciją.
    -   PVM kodai
    -   PVM grupės
    -   Prekės PVM grupės
    -   Sąskaitų grupė
    -   Neapmokestinimo PVM kodai
    -   PVM jurisdikcijos
    -   PVM rinkėjai
    -   PVM sudengimo laikotarpiai

**Cash and bank management**

-   Mokėjimų paskirčių kodų puslapyje nustatykite centrinio banko paskirties kodą.





---
title: "Serijos numerių registravimas pardavimo proceso metu"
description: "Šioje temoje aiškinama, kaip pardavimo proceso metu galite registruoti važtaraščių ar SF serijos numerius. Ši funkcija naudinga, jei įmonė nori užfiksuoti serijos numerius paslaugų ir garantijos tikslais, tačiau nenori tvarkyti serijos numerių atsargose nuo gavimo iki išdavimo."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 62f59c857980932f4cf75d928deb0f89fae2f8eb
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="register-serial-numbers-in-the-sales-process"></a>Serijos numerių registravimas pardavimo proceso metu

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Šioje temoje aiškinama, kaip pardavimo proceso metu galite registruoti važtaraščių ar SF serijos numerius. Ši funkcija naudinga, jei įmonė nori užfiksuoti serijos numerius paslaugų ir garantijos tikslais, tačiau nenori tvarkyti serijos numerių atsargose nuo gavimo iki išdavimo.

Daug įmonių tiesiog nori užfiksuoti serijinius numerius paslaugų ir garantijos tikslais, ir nenori turėti serijinių numerių atsargose nuo gavimo iki išdavimo. Šiose situacijose „Microsoft Dynamics 365 for Finance and Operations“ važtaraščių ar sąskaitų faktūrų serijos numerius leidžia registruoti produktus parduodant. Jei produktai yra vėliau grąžinami, galite atsekti kiekvieną produktą sąskaitoje faktūroje ir nustatyti, ar pardavėte produktą ar paslaugą ir ar galioja garantiniai įsipareigojimai.

Pardavimo procesui turite įjungti serijinius numerius, pasirinkdami **Aktyvus pardavimų procese** parinktį iš **Sekimo dimensijos grupių** puslapio. Tada sprendime „Microsoft Dynamics 365 for Finance and Operations“ įvyksta tolesni įvykiai.
-   Iš **Serijos numerių** „FastTab“ pasirenkama **Serijos numerių kontrolė** parinktis. Pažymėję šią parinktį, turite užregistruoti vieną serijinį numerį kiekvienai prekei ant važtaraščio arba sąskaitos faktūros.
-   Visi serijinių numerių pasirinkimai sekimo dimensijų grupėje anuliuojami, išskyrus **Galimas tuščias išdavimas** parinktį. Galite pasirinkti **Galimas tuščias išdavimas** parinktį, norėdami nepaisyti serijos numerių kontrolės, ir leisti supakuoti prekes ir išrašyti sąskaitą neužregistravę serijos numerių.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Kada užregistruoti serijos numerius pardavimo proceso metu?
Serijos numerius galite užregistruoti ant pardavimo užsakymo važtaraščio arba sąskaitos faktūros. Kai paruošite sąskaitą faktūrą serijos prekei, kuri atgabenta kartu su važtaraščiu, galite pasirinkti, kurie serijos numeriai ant važtaraščio bus įtraukti į sąskaitą faktūrą. Registruotų serijos numerių skaičius neturi viršyti atgabentų prekių kiekio. Jei kuriate dalinę sąskaitą faktūrą, galite pasirinkti mažiau serijos prekių nei įregistruota važtaraštyje. Kai spausdinate važtaraštį arba sąskaitą faktūrą, įtraukiami serijos numeriai, kurie buvo užregistruoti.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Ar galiu įvesti serijos numerius juos nuskaitant, ar juos reikia spausdinti?
Galite nuskaityti arba spausdinti serijos numerius. Kai naudojate skaitytuvą, skenavimas režimas nustato, ar serijos numeriai yra įvedami, ar pašalinami iš serijos numerių sąskaitoje faktūroje arba važtaraščio sąrašo. Jei norite nuskaityti serijos numerius, naudodami, pavyzdžiui, rankinį brūkšninių kodų skaitytuvą, sukonfigūruokite skaitytuvą siuntimui, paspaudę Enter arba TAB komandą po serijos numerio. Ši komanda nurodo duomenų srauto pabaigą. Priešingu atveju, nuskaitę kiekvieną serijos numerį turite spausti Enter arba TAB ant klaviatūros.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Jei įjungsiu serijos numerius pardavimo procesui, ar turėsiu registruoti visus serijos numerius visoms prekėms?
Prekei priskirtos sekimo dimensijos grupės sąranka nustato, ar serijos numerius reikia registruoti visoms prekėms sąskaitoje faktūroje arba važtaraštyje. Įjungus serijos numerius pardavimo procesui, automatiškai pasirenkama **Serijos numerių kontrolės** parinktis. Tada turite užregistruoti vieną serijos numerį arba užregistruoti tuščią registraciją už neįskaitomam skaičiui kiekvienos prekės apie važtaraštyje arba sąskaitoje faktūroje. Jei nenorite reikalauti serijos numerio kiekvienai prekei, pasirinkite **Galimi tušti išdavimai** parinktį sekimo dimensijos grupėje, kuri priskirta prekei. Tada galite registruoti mažiau serijos numerių, nei gabenamų prekių kiekis. Jei užregistruosite daugiau serijos numerių, nei gabenamų prekių kiekis, negalėsite išrašyti važtaraštį arba sąskaitos faktūros.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Ar galiu registruoti serijos numerius dalinėms sąskaitoms faktūroms ir dalinėms siuntoms?
Galite kurti dalines sąskaitas faktūras ir važtaraščius pardavimų užsakymams ir registruoti tik serijos numerius tų prekių, kurios yra įtrauktos į sąskaitas faktūras ir važtaraščius. Jei norite sukurti dalinę sąskaitą faktūrą ir turite daugiau nei vieną važtaraštį vienam pardavimo užsakymui, galite įtraukti serijos numerius iš daugiau nei vieno važtaraščio. Tačiau gali būti tik vienas važtaraštis, neapimantis visų serijos numerių. Pavyzdžiui, jei turite tris važtaraščius, ir kiekvienas važtaraštis apima dvi serijos prekes, negalite sukurti dalinės sąskaitos faktūros vienai prekei iš kiekvieno važtaraščio.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Ką daryti, kai serijos numeris yra neįskaitomas?
Jei serijos numeris neįskaitomas ir nenuskanuojamas, galite sukurti prekei tuščią eilutę, paspaudę **Neįskaitomas** **Serijos numerių** puslapyje. Jei serijos numeris tampa žinomas vėliau, galite atnaujinti sąskaitą faktūrą ar važtaraštį. Norėdami gauti daugiau informacijos, skaitykite kitą skyrių „Ar galiu pataisyti arba pakeisti serijos numerius užregistruotam pardavimo užsakymui?“

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Ar galiu pataisyti arba pakeisti serijos numerius užregistruotam pardavimo užsakymui?
Taip, galite ištaisyti serijos numerius, jei įvykdomos šios sąlygos:
-   **Sąskaitos** – galite pakeisti serijos numerius prekių, kurioms dar neišrašėte sąskaitos. Tada atnaujinamas ir važtaraštis. Tačiau jei pardavimo užsakymo eilutė buvo ištaisyta registruojant neigiamą kiekį, serijos numerių pardavimo užsakymo eilutei pakeisti negalite.
-   **Važtaraščiai** – galite dalinai pataisyti važtaraščio eilutę, kurioje yra serijos prekės. Turite atšaukti visą tos eilutės kiekį. Jeigu važtaraštis buvo atšauktas arba taisytas, nereikia vėl registruoti atvirkštinių serijos numerių, kai kuriate naują tų pačių serijinių prekių važtaraštį. Bus naudojami užregistruoti numeriai.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Ar galiu peržiūrėti serijos numerius, atsiųstus kartu su konkrečiu važtaraščiu, arba tuos, kurie buvo įtraukti į sąskaitą faktūrą?
Taip, galite atlikti užklausą važtaraščio žurnalo eilutėje arba sąskaitos faktūros žurnalo eilutėje ir peržiūrėti visų serijos numerių, įtrauktų į tą dokumentą, sąrašą.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Ar galiu peržiūrėti savo turimas prekes su serijos numeriais?
Ne, negalite peržiūrėti serijos prekių, kurias turite po ranka, nes serijiniai numeriai neregistruojami tol, kol prekės neparduodamos.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Ar galiu registruoti esamo svorio prekių serijos numerius?
Ne, negalite registruotis serijos numerių sveriamoms prekėms pardavimo proceso metu. Be to, jei prekė nustatyta kaip sveriama, negalite priskirti prekės sekimo dimensijos grupei, kuri skirta naudoti serijos numerius tik pardavimo proceso metu.

## <a name="can-i-register-serial-numbers-at-the-retail-pos"></a>Ar galiu registruoti serijos numerius mažmeninės prekybos EKA?

Taip, mažmeninės prekybos taškas (EKA) paskatins vartotoją įvesti serijos numerį, kai vartotojas parduoda prekę, kuri yra priskirta sekimo dimensijos grupei, kuri yra sukurta naudoti serijos numerius tik pardavimo proceso metu.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Kokie saugos vaidmenys yra privalomi norint įregistruoti serijos numerius pardavimo proceso metu??
Ši funkcija yra prieinama visiems vaidmenims, kurie gali tvarkyti pardavimų važtaraščius ir pardavimo sąskaitas faktūras. Šie vaidmenys leidžia darbuotojams redaguoti serijos numerius ir registruoti tuščius serijos numerių įrašus, kurių negalima įskaityti ar nuskenuoti:
-   Tvarkyti serijos numerių koregavimą
-   Tvarkyti neįskaitomų serijos numerių registravimą







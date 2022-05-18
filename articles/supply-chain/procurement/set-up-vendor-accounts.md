---
title: Tiekėjų sąskaitų nustatymas
description: Šioje temoje aprašoma informacijos, kurią turite nurodyti kurdami naują tiekėjo sąskaitą, tipai.
author: GalynaFedorova
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: smmContactPerson, VendBankAccounts, VendTable, VendOnHoldUpdate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d524ff99cba733fdd607d9708abba440248d6cc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676980"
---
# <a name="set-up-vendor-accounts"></a>Tiekėjų sąskaitų nustatymas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma informacijos, kurią turite nurodyti kurdami naują tiekėjo sąskaitą, tipai.

Kai kuriate tiekėjo sąskaitą, galite įvesti tiekėjo informaciją. Ši informacija naudojama duomenims į dokumentus automatiškai įvesti ir su tiekėju susijusiai veiklai sekti. Pvz., galite konfigūruoti toliau nurodytą tiekėjo informaciją.

-   Priskirkite tiekėjų grupę. Kiekvienas tiekėjas turi būti priskirtas tiekėjų grupei. Tos pačios tiekėjų grupės tiekėjai turi bendrus parametrus. Pvz., tas pačias mokėjimo sąlygas.
-   Sukonfigūruokite katalogo importavimo tiekėją. Tiekėjai gali pateikti failą, kuriame yra jų prekių ir paslaugų katalogas. Šį failą galima nusiųsti, kad jūsų darbuotojai galėtų užsakyti iš tiekėjo.
-   Priskirkite tiekėją įsigijimo kategorijoms.
-   Leiskite dabartiniam tiekėjui bendradarbiauti su kitu organizacijos juridiniu subjektu.
-   Sulaikykite konkrečių tipų tiekėjo operacijas.
-   Nustatykite banko informaciją tiekėjui, kad apmokėjimus galėtumėte siųsti elektroniniu būdu.
-   Nustatykite tiekėjo mokesčių, sąskaitos faktūros ir mokėjimo informaciją. Pagal numatytuosius nustatymus šie nustatymai yra nukopijuojami į naujus dokumentus, kuriuos kuriate tiekėjui.
-   Nustatykite numatytąsias finansines dimensijas, kurios bus naudojamos automatiškai registruoti tiekėjo operacijas į finansines sąskaitas.

Norėdami paspartinti tiekėjų kodų kūrimo procesą, galite kurti šablonus. Norėdami kurti šabloną, puslapio **Tiekėjas** veiksmų srityje spustelėkite **Parinktys** &gt; **Įrašo informacija**. Tada spustelėkite **Įmonės sąskaitų šablonas**. Įmonės sąskaitų šablonai yra bendrinami su kitais vartotojais.  

Taip pat galite kurti vartotojo šabloną, kurį naudosite patys. Tiekėjo, kuris yra susijęs su kitais įrašais, pavyzdžiui, kontaktais arba produktais, naikinti negalima.

## <a name="vendor-account-numbers"></a>Tiekėjų sąskaitų numeriai
Sąskaitos numeris yra unikalus tiekėjo identifikatorius. Galite nustatyti sąskaitų numerius taip, kad, pasirinkus tiekėją, jie būtų generuojami automatiškai. Taip pat galite konfigūruoti numeraciją, kad sąskaitų numeriai būtų įvedami neautomatiniu būdu. Pavyzdžiui, galbūt norėsite naudoti tiekėjo telefono numerį kaip identifikatorių.

## <a name="vendor-organizations-and-individual-vendors"></a>Tiekėjų organizacijos ir atskiri tiekėjai
Kai kuriate naują tiekėjo kodą, turite pasirinkti, ar tiekėjas yra organizacija, ar asmuo. Nuo jūsų pasirinkimo priklausys, kokią tiekėjo informaciją turėsite įvesti. Jei tai asmuo, ši informacija apima asmens vardą, pavardę ir pareigas. Jei tai organizacija, ši informacija apima organizacijos numerį ir darbuotojų skaičių.

## <a name="addresses"></a>Adresai
Galite nustatyti kelis kiekvieno tiekėjo adresus, kurių kiekvienas būtų naudojamas skirtingiems tikslams. Pvz., galite sukurti adresą, kurio tikslas yra **SF**. Arba, jei tiekėjui mokėsite čekiais, galite sukurti adresą, kurio tikslas yra **Pervesti gavėjui**. Jei reikia nurodyti adresą, kuris naudojamas pinigams į užsienio bankus pervesti, tikslas bus **SWIFT**.

## <a name="vendor-contacts"></a>Tiekėjo kontaktai
Galite saugoti tiekėjo kontaktus. Šiuos kontaktus galima naudoti dokumentuose, pvz., pirkimo užsakymuose arba pasiūlymo patvirtinimuose (RFQ).  

Norėdami įtraukti tiekėjo kontaktus, puslapio **Visi tiekėjai** skirtuko **Tiekėjas** grupėje **Nustatyti** spustelėkite **Kontaktai** &gt; **Įtraukti kontaktus**.  

Galite kurti tiekėjo kontaktus nuo pradžių. Taip pat galite kopijuoti informaciją iš kito asmens, kuris jau užregistruotas Tiekimo grandinės valdyme, ir pagal poreikį informaciją redaguoti.  

**Pastaba.** Tiekėjo kontakto įtraukimas ir tiekėjo kontaktinės informacijos įtraukimas nėra tas pats veiksmas. Nors galite įtraukti bendrą tiekėjo kontaktinę informaciją, gali būti, kad toje įmonėje kontaktai yra keli konkretūs žmonės ir jie visi turi savo kontaktinę informaciją.  

Kontaktinio asmens įrašo naikinti negalima, jei kontaktas yra nuorodas dokumente. Tačiau kontaktą galima inaktyvinti.  

Tiekėjo kontaktus galite įtraukti į savo asmeninius kontaktus „Microsoft 365“. Tačiau pirmiausia turite nustatyti Tiekimo grandinės valdymo ir „Microsoft 365“ sinchronizavimą tiek „Microsoft Exchange Server“ sinchronizavime, tiek „Microsoft Outlook“ nustatymo vedlyje.

## <a name="vendors-in-different-legal-entities"></a>Skirtingų juridinių subjektų tiekėjai
Jei tiekėjas jūsų organizacijoje registruotas tik vienam juridiniam subjektui ir kiti juridiniai subjektai turi registruoti tą patį tiekėją, galite naudoti puslapį **Įtraukti tiekėją į kitą juridinį subjektą**, norėdami sukonfigūruoti tiekėją vykdyti verslo veiklą su kitu juridiniu subjektu. Pasirinktame juridiniame subjekte turite pasirinkti tiekėjų grupę, valiutą ir tiekėjo sulaikymo būseną.  

Jei keli jūsų organizacijos juridiniai subjektai bendradarbiauja su tuo pačiu tiekėju ir kiekvienas juridinis subjektas turi atskirą tam tiekėjui skirtą sąskaitą, galite sulieti to tiekėjo kodų šalies ID. Tokiu būdu informaciją, pvz., adresą ir darbuotojų skaičių, galima bendrinti, kad ją naujinti reikėtų tik vienoje vietoje.  

Norėdami sulieti šalies ID, atlikite tolesnius veiksmus.

1.  Puslapyje **Visuotinė adresų knygelė** pasirinkite adresų knygelės įrašus, nurodančius tiekėją kiekviename juridiniame subjekte, kuris turi būti įtrauktas į liejimą.
2.  Veiksmų srityje spustelėkite **Sulieti įrašus**.

## <a name="agreements"></a>Sutartys
Kai nustatote tiekėjo kodą, taip pat galite registruoti sutartis, kurias esate sudarę su tiekėju. Galite nustatyti kainų ir nuolaidų sutartis, naudodami veiksmus tiekėjo įraše. Taip pat galite nustatyti pirkimo sutartį puslapyje **Pirkimo sutartys**.

## <a name="putting-a-vendor-on-hold"></a>Tiekėjo sulaikymas
Galite sulaikyti įvairių tipų tiekėjo operacijas. Galimos toliau nurodytos pasirinktys:

-   **Ne** – tiekėjui netaikomi jokie sulaikymai.
-   **SF** – neleidžiama registruoti sąskaitų faktūrų tiekėjui.
-   **Visos** – sulaikomos visų tipų tiekėjo operacijos. Šie operacijų tipai apima pirkimo paraiškas, SF ir mokėjimus.
-   **Mokėjimas** – neleidžiama generuoti mokėjimų tiekėjui.
-   **Paraiška** – negalima sukurti tiekėjo pirkimo paraiškų, o paraiškos eilučių, jau sukurtų prieš tai, kai buvo nustatyta sulaikyti tiekėją, negalima konvertuoti į pirkimo užsakymą. Tiekėjo paraiškos eilutės bus atšauktos, jei jūsų strategija nustatyta taip, kad pirkimo užsakymai būtų kuriami automatiškai.
-   **Niekada** – tiekėjas niekada nėra sulaikomas dėl neaktyvumo.

Kai sulaikote tiekėją, taip pat galite nurodyti priežastį ir datą, kada sulaikymo būsena pasibaigs. Jei pabaigos datos neįvesite, tiekėjo sulaikymo būsena galios neribotą laiką.

Galite masiškai naujinti tiekėjų sulaikymo būseną į **Visi** pagal puslapyje **Tiekėjo išaktyvinimas** pasirinktus kriterijus ir priskirti priežastį, nurodančią, kodėl tiekėjas yra sulaikytas.

Toliau pateikti kriterijai naudojami norint įtraukti tiekėjus, kurie tam tikrą laikotarpį buvo neaktyvūs, įtraukti arba neįtraukti tiekėjų, kurie yra darbuotojai, ir neįtraukti tiekėjų, kuriems skirtas atidėjimo laikas prieš kitą sulaikymą.

- Pagal į puslapio **Tiekėjo išaktyvinimas** lauke **Nedarbingumo laikotarpis** įvestą dienų skaičių programa apskaičiuoja vėliausią datą, kurią dar gali būti registruota tiekėjo veikla, bet tiekėjas būtų laikomas neaktyviu. T. y. dabartinė data, atėmus jūsų įvestą dienų skaičių. Jei yra viena ar daugiau tiekėjo SF, kurių data yra vėlesnė už apskaičiuotą vėliausią datą, tiekėjas nebus įtrauktas į išaktyvinimo sąrašą. Tai taip pat galioja, jei yra vėliau nei ta dieną registruotų tiekėjo mokėjimų, atidarytų pirkimo paraiškų, atidarytų pirkimo užsakymų, pasiūlymų patvirtinimų arba atsakymų.
- Vėliausia atidėjimo data apskaičiuojama naudojant lauke **Atidėjimo laikas prieš kitą sulaikymą** nurodytą dienų skaičių. T. y. dabartinė data, atėmus jūsų įvestą dienų skaičių. Tai taikoma tik tiekėjams, kurie anksčiau buvo išaktyvinti. Jei tiekėjas buvo anksčiau išaktyvintas, programa patikrina kitų tiekėjo išaktyvinimo atvejų retrospektyvą ir nustato, ar vėliausias išaktyvinimas atliktas po vėliausios atidėjimo dienos. Jei taip, tiekėjas bus įtrauktas į išaktyvinimo procesą.
- Parametras **Įtraukti darbuotojus** nurodo tiekėjus, kurie susieti su darbuotojais. Jei norite, galite nustatyti, kad tie darbuotojai būtų įtraukti.

Į šį procesą niekada nebus įtraukti tiekėjai, jei jų lauko **Tiekėjo sulaikymas** reikšmė yra **Niekada**.

Tikrinimą praėję tiekėjai sulaikomi, nustatomos lauko **Tiekėjo sulaikymas** reikšmė **Visi** ir pasirinkta lauko **Priežastis** reikšmė. Sulaikymo retrospektyvoje sukuriamas tiekėjo įrašas.

## <a name="vendor-invoice-account"></a>Tiekėjo mokėtojo kodas
Jei daugiau nei vienas tiekėjas turi tokį patį sąskaitos adresą arba jei tiekėjui SF išrašoma per trečiąją šalį, tiekėjo įraše galite nurodyti SF kodą. SF kodas yra kodas, kuriame kredituojama SF suma, kai iš pirkimo užsakymo kuriate tiekėjo SF. Tiekėjo įraše neįvedus SF kodo, jo vietoje naudojamas tiekėjo kodas.

## <a name="vendor-bank-accounts"></a>Tiekėjų banko sąskaitos
Jei mokėjimus turite atlikti į tiekėjo banko sąskaitą, galite įvesti informaciją apie tiekėjo banką ir banko sąskaitas puslapyje **Tiekėjo banko sąskaitos**. Taip pat galite įvesti banko sąskaitos tikrinimo ir mokėjimų informaciją. Pavyzdžiui, į tiekėjo banko sąskaitas galite įtraukti išankstinių pranešimų. Šiuos išankstinius pranešimus galima naudoti norint patvirtinti sąskaitos duomenų, tokių kaip nukreipimo numeriai ir sąskaitos numeriai, tikslumą. Turite nurodyti numatytąją mokėjimų tiekėjui sąskaitą. Tačiau atlikdami mokėjimą galite šią sąskaitą pakeisti į vieną iš kitų tiekėjo sąskaitų.

## <a name="ledger-accounts"></a>DK sąskaitos
Galite nurodyti numatytąsias sąskaitas, kurios bus automatiškai rodomos nurodyto tiekėjo SF žurnaluose. Ši funkcija gali būti naudinga, jei paprastai mokate už tos pačios rūšies prekes arba paslaugas iš tų pačių tiekėjų. Kai nurodote numatytąją sąskaitą, SF žurnale galite greitai ir efektyviai įvesti žurnalo įrašus. Jūsų nurodytos numatytosios sąskaitos nėra naudojamos pirkimo užsakymuose arba tiekėjo SF, kurias įvedate puslapyje **Tiekėjo SF**.  

Numatytąsias sąskaitas galite pasirinkti puslapyje **Numatytosios sąskaitos nustatymas**, kurį galite atidaryti naudodami tiekėjo įrašo skirtuką **SF**. Čia pasirinktos sąskaitos rodomos filtruotame tiekėjo sąskaitų sąraše, kai įvedate žurnalo įrašą. Vieną iš sąskaitų galite nustatyti kaip numatytąją sąskaitą.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
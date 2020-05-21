---
title: Projekto SF išrašymas
description: Šiame straipsnyje pateikiama projekto SF išrašymo Laiko ir medžiagų bei Fiksuotos kainos projektams apžvalga. Taip pat pateikiama informacija apie SF pasiūlymus (preliminarias SF), SF kontrolę, aktyvių SF išrašymą, tiekėjo SF išrašymą ir kredito pažymas.
author: ShylaThompson
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81a3d64d04ceb20fec2f5ca4bb005e7ecb3c1929
ms.sourcegitcommit: d2b111bf7a5fbf62ff2874d6c57c5ef8412df82e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331377"
---
# <a name="project-invoicing"></a>Projekto SF išrašymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama projekto SF išrašymo Laiko ir medžiagų bei Fiksuotos kainos projektams apžvalga. Taip pat pateikiama informacija apie SF pasiūlymus (preliminarias SF), SF kontrolę, aktyvių SF išrašymą, tiekėjo SF išrašymą ir kredito pažymas.

Projekto tipas nurodo, kokia SF išrašymo procedūra turi būti taikoma. SF gali būti išrašomos tik dviejų tipų išoriniams projektams – Laiko ir medžiagų bei Fiksuotos kainos. Laiko ir medžiagų bei Fiksuotos kainos projektai visada pridedami prie projekto sutarties.

-   **Fiksuotos kainos projektai** – kliento SF suma paremta SF išrašymo grafikais. SF išrašomos naudojant laisvos formos sąskaitos sąranką, kuri taip pat vadinama atsiskaitymo grafiku. Fiksuotos kainos projektų SF gali būti išrašomos pagal projektą arba pagal projekto sutartį.
-   **Laiko ir medžiagų projektai** – kliento SF sumos pagrindas yra įvestų projektų operacijų eilutės. Operacijų SF gali būti išrašomos pagal projektą arba pagal projekto sutartį.

Laiko ir medžiagų projektus bei Fiksuotos kainos projektus prie SF projektų galima pridėti trimis toliau nurodytais būdais.

-   **Išrašant laisvos formos sąskaitų SF** – Laiko ir medžiagų bei Fiksuotos kainos projektams SF gali būti išrašomos pagal sąskaitą. Reikalinga dviejų tipų laisvos formos sąskaitų sąranka – po vieną kiekvienam projektų tipui.
-   **Išrašant SF periodiniame skyriuje** – naudojant periodines funkcijas galima išrašyti kelių projektų operacijų SF. Periodinės funkcijos leidžia peržiūrėti operacijas, kurioms reikia išrašyti SF.
-   **Naudojant kredito pažymas SF išrašyti** – galima sukurti ir Laiko ir medžiagų, ir Fiksuotos kainos projektų kredito pažymą.

## <a name="invoice-proposals"></a>SF pasiūlymai
Prieš kurdami projekto kliento SF, galite sukurti preliminarią SF arba SF pasiūlymą. SF pasiūlyme galite pasirinkti, kurias projekto operacijas įtraukti į projekto SF. Tada galite peržiūrėti SF informaciją ir projekto SF registruoti bei išsiųsti klientui ar kitam lėšų skyrimo šaltiniui.

### <a name="creating-invoice-proposals"></a>SF pasiūlymų kūrimas

Galite kurti SF pasiūlymus rankiniu būdu pasirinkdami konkretaus projekto operacijų sąraše. Taip pat galite nustatyti atsiskaitymo taisykles, kada automatiškai kurti SF pasiūlymą. Pvz., galite sukurti atsiskaitymo taisyklę, kad būtų kuriamas SF pasiūlymas, kai darbas prie projekto yra 25 proc., 50 proc., 75 proc. ir 100 proc. baigtas. 

Galite kurti toliau nurodytų operacijų SF pasiūlymus.

-   Valandų, išlaidų ir kitos projekto operacijos.
-   Sumos, kurias klientai išskaitė ankstesnėse projekto SF.
-   Kredito pažymos
-   Sumos, kurias jums sumokėjo klientas prieš pradedant projektą.

> [!NOTE]
> Funkcija **Suaktyvinti rūšiavimą pagal išteklius kuriant projekto SF** leidžia projekto apskaitininkui naujo projekto SF pasiūlymo kūrimo metu rūšiuoti projekto operacijas, kurioms sąskaitas galima kurti pagal išteklių. Lentelėje, kurioje rodomos galimos projekto operacijos, bus atskiras ištekliaus ID ir ištekliaus laukas, kuris leidžia vartotojui atlikti filtravimą ir rūšiavimą pagal ištekliaus pavadinimą. Esant numatytiesiems parametrams, ši funkcija yra išjungta, o ją įjungti galima naudojant **Darbo sritys > Funkcijų valdymas**. Norėdami suaktyvinti šią funkciją, kreipkitės į sistemos administratorių.

SF pasiūlyme galite sukurti mokesčių operacijas. Taip pat galite modifikuoti pardavimo kainą pagal valandą, išlaidas, prekę ir mokesčių operacijas. Kai užregistruojate SF pasiūlymą, atnaujintos kainos ir operacijos įtraukiamos į projekto ataskaitas ir operacijų retrospektyvą. 

Norėdami sukurti kelias projekto klientų SF, turite sukurti SF pasiūlymą kiekvienai SF. Pvz., galite kurti SF pagal operacijos tipą. Norėdami nurodyti valandas vienoje kliento SF, o prekes – kitoje, turite sukurti atskirus SF pasiūlymus valandinėms operacijoms ir mokesčių operacijoms. 

Jei projekte yra daugiau kaip vienas finansavimo šaltinis, galite sukurti atskirą SF pasiūlymą kiekvienam finansavimo šaltiniui. **Lėšų skyrimo taisyklių paskirstymų** puslapyje galite apibrėžti operacijos sumos procentą, skirtiną kiekvienam lėšų skyrimo šaltiniui ir šaltinį, kuriame registruoti apvalinimo skirtumus.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Klientų SF kūrimas iš SF pasiūlymų

Sukūrus ir užregistravus SF pasiūlymą, automatiškai sukuriama kliento SF operacijoms, kurios įtrauktos į SF pasiūlymą. 

Prieš registruodami SF pasiūlymą, į jį galite pridėti arba jame panaikinti operacijų. Pvz., galite pašalinti išlaidų operacijas, kurios buvo užregistruotos projekte, bet neapmokestinamos klientui. 

Jei organizacijoje reikalaujama, kad SF pasiūlymai būtų peržiūrėti prie juos registruojant, SF pasiūlymą, prieš jį registruojant, gali reikėti patvirtinti naudojant darbo eigą „Peržiūrėti projekto SF pasiūlymus‟.

## <a name="on-account-invoicing"></a>Aktyvus SF išrašymas
Projekto suma, kurią įvedate laisvos formos SF, yra pagrįsta laiku, įvykdymo procentu ir kitomis atsiskaitymo sąlygomis, nurodytomis susijusioje projekto sutartyje. Suma nėra skaičiuojama pagal valandas, prekes, išlaidas arba projekte įregistruotus mokesčius. 

Prieš pridėdami laisvos formos sąskaitos operaciją į projekto SF, turite sukurti tą Laiko ir medžiagų projekto arba Fiksuotos kainos projekto laisvos formos sąskaitos operaciją. Laisvos formos sąskaitos operacijoje įveskite kliento SF sumą. Norėdami sukurti sumos projekto SF, sukurkite preliminarią SF (SF pasiūlymą). Tame SF pasiūlyme pasirinkite laisvos formos sąskaitos operaciją. Prieš sukurdami SF pasiūlymo projekto SF, pasiūlyme galite peržiūrėti laisvos formos sąskaitos informaciją.

### <a name="fixed-price-projects"></a>Fiksuotos kainos projektai

Fiksuotos kainos projektuose laisvos formos sąskaitos operacijos pagrįstos sutartų etapų, pristatymo vieneto arba sąskaitų pateikimo eigos susitarimu, nurodytu projekto sutartyje. Sukuriama viena kiekvieno mokėjimo, kurį reikia gauti iš projekto kliento, eilutė. Išskaityti nereikia.

### <a name="time-and-material-projects"></a>Laiko ir medžiagų projektai

Laiko ir medžiagų projektuose naudodami laisvos formos SF pasiūlymą galite išrašyti klientui arba kitam lėšų skyrimo šaltiniui išankstinio mokėjimo sumos sąskaitą. Įveskite laisvos formos sąskaitos operacijas kaip vieną eilutę. Neprivaloma: norėdami kompensuoti bet kokius kliento jau atliktus išankstinius mokėjimus, galite įvesti papildomų eilučių kaip atskaitymų. Norėdami sukurti atskaitymo eilučių, prieš sumą padėkite minuso ženklą.

## <a name="invoice-control"></a>SF kontrolė
SF kontrolę galite naudoti sekti tiek toms operacijoms, kurioms SF išrašytos, tiek toms, kurioms jos neišrašytos ir toms operacijoms analizuoti pagal pasiūlymus tiesioginiame projektų rodinyje – nuo pasiūlymo etapo iki pabaigos. Galite matyti, kurios konkretaus projekto operacijos pateiktos apmokėti ir kurioms eilutėms išrašytos SF. Taip pat galite peržiūrėti atskiras operacijas, kad, užregistravę, galėtumėte jas koreguoti.

## <a name="invoicing-fixed-price-projects"></a>Fiksuotos kainos projektų SF išrašymas
Norėdami išrašyti Fiksuotos kainos projekto SF, turite apibrėžti atsiskaitymo grafiką ir atlikti SF išrašymo procedūrą.

### <a name="billing-schedule"></a>Atsiskaitymo grafikas

Išrašyti Fiksuotos kainos projektų SF galite pagal atsiskaitymo grafiką. Atsiskaitymo grafikas apibrėžiamas vieno ar kelių projekto etapų atžvilgiu. Galite apibrėžti konkrečią kiekvieno etapo datą, pardavimo valiutą, pardavimo kainą ir veiklą. 

Pavyzdžiui, galite nustatyti toliau pateiktą atsiskaitymo grafiką.

-   20 procentų, kai pasirašoma projekto sutartis.
-   30 procentų atlikus pirmą pristatymą.
-   15 procentų atlikus antrą pristatymą.
-   35 procentų atlikus paskutinį pristatymą.

### <a name="invoicing-procedure"></a>SF išrašymo procedūra

Kai galima išrašyti etapų mokėjimų SF, naudojate laisvos formos sąskaitų sumų SF išrašymo procedūrą.

## <a name="vendor-invoicing"></a>Tiekėjo sąskaitų faktūrų išrašymas
Kai iš tiekėjo užsakote prekę ir ją priskiriate projektui, jūsų pasirinkta tos prekės pirkimo užsakymo eilutės ypatybė nustato, ar už nupirktą prekę klientui išrašoma SF. Jei nustatote numatytąsias eilučių ypatybes, prekės jos rodomos pirkimo užsakymo eilutėje (Eilučių informacija  &gt; Projektas &gt;  Eilutės ypatybė). Modifikuoti eilutės ypatybę galima toliau nurodytais dviem būdais.

-   Už prekę SF išrašyti klientui: prekės eilutės ypatybę nustatykite į pirkimo užsakymo apmokestinamą reikšmę ir, naudodami tinkamą projekto SF išrašymo būdą, klientui išrašykite SF.
-   Už prekę SF išrašyti ne projekto klientui: nesirinkite prekės **Apmokestinamos** eilutės ypatybės, esančios pirkimo užsakyme. Tada už pirkimo užsakymą galite išrašyti SF, ir nereikia atlikti jokių kitų veiksmų.

> [!NOTE] 
> Leidimo užlaikymo eilutės nėra apmokestinamos pagal numatytuosius parametrus. Tai reiškia, kad yra galimybė kurti SF pasiūlymą, nes išleistas užlaikymas neįjungtas.

## <a name="credit-notes"></a>Kredito pažymos
Kai kliento SF sumos reikšmė yra neigiama, SF klasifikuojama kaip kredito pažyma. Spausdinant dokumentą, jo pavadinimas yra „Kredito pažyma‟. 

Kai kuriate kredito pažymą kredituoti sumai, kuriai anksčiau buvo išrašyta SF, visų pirma kreditavimui turite pasirinkti SF sumą. Tada, vadovaudamiesi tokia pačia procedūra, kokią naudotumėte įprastai kliento SF sukurti, sukuriate kredito pažymą. Kitaip tariant, pasirenkate operacijas, anksčiau užregistruotas kliento SF ir sukuriate bei išspausdinate pasiūlymo kredito pažymą. 

Tame pačiame dokumente gali būti operacijos, pasirinktos kredituoti, atlikti kredito operacijoms ar užregistruotoms operacijoms. Dokumentas klasifikuojamas kaip SF arba kredito pažyma, atsižvelgiant į tai, ar bendroji suma yra teigiama, ar neigiama. 

Norėdami kredituoti sumą, kuriai išrašyta SF, pirmiausia pasirenkate sumą, kuriai išrašyta SF ir kurią norite kredituoti bei sukuriate kredito pažymą. Kredito pažyma kuriama vadovaujantis tokia pačia procedūra, kokią naudotumėte kliento SF generuoti. 

Galite sukurti SF su neigiama suma; tokia sąskaita faktūra klasifikuojama kaip kredito pažyma. Norėdami sukurti ir išspausdinti kredito pažymą, turite pasirinkti operacijas, anksčiau užregistruotas kliento SF ir jas modifikuoti. SF pavadinimas bus „Koreguojamoji SF‟, nebent pagrindinis juridinio subjekto adresas yra Vokietijoje.




---
title: Projekto SF išrašymas
description: Ši tema pateikia sąskaitų išrašymo apžvalgą laikui ir medžiagų projektams bei fiksuotos kainos projektams. Taip pat pateikiama informacija apie SF pasiūlymus (preliminarias SF), SF kontrolę, aktyvių SF išrašymą, tiekėjo SF išrašymą ir kredito pažymas.
author: TaylorVH
manager: AnnBe
ms.date: 07/10/2020
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
ms.author: roschlom
ms.search.validFrom: 2020-07-06
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ba2f9d69295f9f5cfb4a2a791be781de32b50f46
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445945"
---
# <a name="project-invoicing"></a>Projekto SF išrašymas

[!include [banner](../includes/banner.md)]

Ši tema pateikia sąskaitų išrašymo apžvalgą laikui ir medžiagų projektams bei fiksuotos kainos projektams. Taip pat pateikiama informacija apie SF pasiūlymus (preliminarias SF), SF kontrolę, aktyvių SF išrašymą, tiekėjo SF išrašymą ir kredito pažymas.

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

Galite sukurti sąskaitų pasiūlymus rankiniu būdu pasirinkdami perlaidas iš esamų perlaidų sąrašo konkrečiam projektui. Galite taip pat nustatyti sąskaitų išrašymo taisykles, kurios nurodo, kada sukurti sąskaitos pasiūlymą automatiniu būdu. Pavyzdžiui, galite sukurti sąskaitos taisyklę siekiant sukurti sąskaitos pasiūlymą dirbant su projektu 25, 50, 75 ir 100 procentų baigtumu. 

Galite kurti toliau nurodytų operacijų SF pasiūlymus.

-   Valandų, išlaidų ir kitos projekto operacijos.
-   Sumos, kurias klientai išskaitė ankstesnėse projekto SF.
-   Kredito pažymos
-   Sumos, kurias jums sumokėjo klientas prieš pradedant projektą.

> [!NOTE]
> Funkcija **Suaktyvinti rūšiavimą pagal išteklius kuriant projekto SF** leidžia projekto apskaitininkui naujo projekto SF pasiūlymo kūrimo metu rūšiuoti projekto operacijas, kurioms sąskaitas galima kurti pagal išteklių. Tinklelis rodo esamas prjekto perlaidas, kurios turi atskirus laukelius **Resursų ID** ir **Resursai**. Šie laukeliai leidžia jums filtruoti ir rūšiuoti resurso pavadinimą. Ši funkcija išjungta pagal nutylėjimą. Ją galimą įjungti naudojant **Funkcijos valdymo** puslapį (**Darbo sritys > Funkcijų valdymas**). Susiekite su savo sistemos administratoriumi dėl pagalbos įjungiant šią funkciją.

SF pasiūlyme galite sukurti mokesčių operacijas. Taip pat galite modifikuoti pardavimo kainą pagal valandą, išlaidas, prekę ir mokesčių operacijas. Kai dalinatės sąskaitos pasiūlymu, atnaujintos kainos ir perlaidos yra įtraukiamos į projekto ataskaitas ir perlaidos istoriją. 

Norėdami sukurti kelias projekto klientų SF, turite sukurti SF pasiūlymą kiekvienai SF. Pvz., galite kurti SF pagal operacijos tipą. Siekiant nurodyti valandas į vieną kliento sąskaitą ir elementus į kitą, turite sukurti atskirus sąskaitos pasiūlymus valandos perlaidoms ir mokesčio perlaidoms. 

Jei projekte yra daugiau kaip vienas finansavimo šaltinis, galite sukurti atskirą SF pasiūlymą kiekvienam finansavimo šaltiniui. **Finansavimo taisyklės priskyrimo** puslapyje galite nustatyti perlaidos kiekio procentą, kurią priskirsite kiekvienam finansavimo šaltiniui ir šaltinio publikavimo apvalinimo skirtumus.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Klientų SF kūrimas iš SF pasiūlymų

Sukūrus ir užregistravus SF pasiūlymą, automatiškai sukuriama kliento SF operacijoms, kurios įtrauktos į SF pasiūlymą. 

Prieš registruodami SF pasiūlymą, į jį galite pridėti arba jame panaikinti operacijų. Pavyzdžiui, galite pašalinti išlaidų perlaidas, kurios buvo publikuotos projekte, tačiau mokestis už jas klientui nėra taikomas. 

Jei jūsų organizacija reikalauja, kad sąskaitų pasiūlymai būtų atnaujinti prieš jų skelbimą, jums gali reikėti patvirtinti jas per „Peržiūrėti projekto sąskaitos pasiūlymų“ darbo srautą prieš publikavimą.

### <a name="view-grant-information-on-project-invoice-list-pages"></a>Peržiūrėkite suteiktą informaciją apie projekto sąskaitos sąrašo puslapius

Viešojo sektoriaus naudotojai gali įtraukti **Suteikti ID** ir **Suteikti vardą** į **Projekto sąskaitos pasiūlymus** ir **Projekto sąskaitų** sąrašo puslapius. Šie stulpeliai yra šjungti naudojant **Įtraukti suteikiamą informaciją projekto sąskaitų sąrašo puslapiams** funkciją. Ši funkcija išjungta pagal nutylėjimą ir gali būti įjungta **Darbo sritys > Funkcijos valdymas**. Susiekite su savo sistemos administratoriumi dėl pagalbos įjungiant šią funkciją.

## <a name="on-account-invoicing"></a>Aktyvus SF išrašymas
Projekto suma, kurią įvedate laisvos formos SF, yra pagrįsta laiku, įvykdymo procentu ir kitomis atsiskaitymo sąlygomis, nurodytomis susijusioje projekto sutartyje. Suma nėra skaičiuojama pagal valandas, prekes, išlaidas arba projekte įregistruotus mokesčius. 

Privalote sukurti paskyros perlaidą laiko ir medžiagos projektui arba fiksuotos kainos projektui prieš tai, kai įtrauksite paskyros perlaidas į projekto sąskaitą. Laisvos formos sąskaitos operacijoje įveskite kliento SF sumą. Norėdami sukurti sumos projekto SF, sukurkite preliminarią SF (SF pasiūlymą). Tame SF pasiūlyme pasirinkite laisvos formos sąskaitos operaciją. Prieš sukurdami SF pasiūlymo projekto SF, pasiūlyme galite peržiūrėti laisvos formos sąskaitos informaciją. 

### <a name="fixed-price-projects"></a>Fiksuotos kainos projektai
Fiksuotos kainos projektuose laisvos formos sąskaitos operacijos pagrįstos sutartų etapų, pristatymo vieneto arba sąskaitų pateikimo eigos susitarimu, nurodytu projekto sutartyje. Sukuriama viena kiekvieno mokėjimo, kurį reikia gauti iš projekto kliento, eilutė. Išskaityti nereikia.

### <a name="time-and-material-projects"></a>Laiko ir medžiagų projektai

Laiko ir medžiagų projektuose naudodami laisvos formos SF pasiūlymą galite išrašyti klientui arba kitam lėšų skyrimo šaltiniui išankstinio mokėjimo sumos sąskaitą. Įveskite laisvos formos sąskaitos operacijas kaip vieną eilutę. Neprivaloma: norėdami kompensuoti bet kokius kliento jau atliktus išankstinius mokėjimus, galite įvesti papildomų eilučių kaip atskaitymų. Siekiant sukurti atskaičiavimo eilutes, įveskite minuso ženklą prieš sumą.

## <a name="invoice-control"></a>SF kontrolė
SF kontrolę galite naudoti sekti tiek toms operacijoms, kurioms SF išrašytos, tiek toms, kurioms jos neišrašytos ir toms operacijoms analizuoti pagal pasiūlymus tiesioginiame projektų rodinyje – nuo pasiūlymo etapo iki pabaigos. Galite matyti, kurios konkretaus projekto operacijos pateiktos apmokėti ir kurioms eilutėms išrašytos SF. Taip pat galite peržiūrėti atskiras operacijas, kad, užregistravę, galėtumėte jas koreguoti.

## <a name="invoicing-fixed-price-projects"></a>Fiksuotos kainos projektų SF išrašymas
Norėdami išrašyti Fiksuotos kainos projekto SF, turite apibrėžti atsiskaitymo grafiką ir atlikti SF išrašymo procedūrą.

### <a name="billing-schedule"></a>Atsiskaitymo grafikas

Galite išrašyti sąskaitos fiksuotos kainos projektus sąskaitų grafike. Atsiskaitymo grafikas apibrėžiamas vieno ar kelių projekto etapų atžvilgiu. Galite apibrėžti konkrečią kiekvieno etapo datą, pardavimo valiutą, pardavimo kainą ir veiklą. 

Pavyzdžiui, galite nustatyti toliau pateiktą atsiskaitymo grafiką.

-   20 procentų, kai pasirašoma projekto sutartis.
-   30 procentų atlikus pirmą pristatymą.
-   15 procentų atlikus antrą pristatymą.
-   35 procentų atlikus paskutinį pristatymą.

### <a name="invoicing-procedure"></a>SF išrašymo procedūra

Kai eapo mokėjimai yra paruošti sąskaitų išrašymui, naudokite sumų paskyroje sąskaitos išrašymo procedūrą.

## <a name="vendor-invoicing"></a>Tiekėjo sąskaitų faktūrų išrašymas
Kai iš tiekėjo užsakote prekę ir ją priskiriate projektui, jūsų pasirinkta tos prekės pirkimo užsakymo eilutės ypatybė nustato, ar už nupirktą prekę klientui išrašoma SF. Jei nustatoti iš anksto pasirinktas eilutės ypatybes, jos yra rodomos prekei prekybos užsakymo eilutejė (**Eilutės informacija > Projektas > Eilutės ypatybių suma**). Modifikuoti eilutės ypatybę galima toliau nurodytais dviem būdais.

-   Sąskaita projekto klientui už prekę. Tam, kad tą atliktumėte, nustatykite eilutės ypatybes prekei į apmokestinamą vertę pagal prekybos užsakymą ir tuomet išrašykite sąskaitą klientui naudodami tinkamą projekto sąskaitos metodą.
-   Nerašykite sąskaitos projekto klientui už prekę. Tam, kad tą atliktumėte, nesirinkite **Apmokestinama** eilutės ypatybių prekybos užsakymo eilutėje prekei. Tada už pirkimo užsakymą galite išrašyti SF, ir nereikia atlikti jokių kitų veiksmų.

> [!NOTE] 
> Leidimo užlaikymo eilutės nėra apmokestinamos pagal numatytuosius parametrus. Tai reiškia, kad yra galimybė kurti SF pasiūlymą, nes išleistas užlaikymas neįjungtas.

## <a name="credit-notes"></a>Kredito pažymos
Kai kliento SF sumos reikšmė yra neigiama, SF klasifikuojama kaip kredito pažyma. Spausdinant dokumentą, jo pavadinimas yra „Kredito pažyma‟. 

Kai kuriate kredito pažymą kredituoti sumai, kuriai anksčiau buvo išrašyta SF, visų pirma kreditavimui turite pasirinkti SF sumą. Tuomet sukurkite kreditinę sąskaitą atlikdami tokią pačią procedūrą, kuri yra naudojama sukurti įprastą kliento sąskaitą. Pasirenkate perlaidas, kurios buvo anksčiau paskelbtos kliento sąskaitoje ir tuomet sukuriate ir publikuojate kreditinės kortelės siūlymą. 

Tame pačiame dokumente gali būti operacijos, pasirinktos kredituoti, atlikti kredito operacijoms ar užregistruotoms operacijoms. Dokumentas klasifikuojamas kaip SF arba kredito pažyma, atsižvelgiant į tai, ar bendroji suma yra teigiama, ar neigiama. 

Norėdami kredituoti sumą, kuriai išrašyta SF, pirmiausia pasirenkate sumą, kuriai išrašyta SF ir kurią norite kredituoti bei sukuriate kredito pažymą. Kredito pažyma kuriama vadovaujantis tokia pačia procedūra, kokią naudotumėte kliento SF generuoti. 

Galite sukurti SF su neigiama suma; tokia sąskaita faktūra klasifikuojama kaip kredito pažyma. Norėdami sukurti ir išspausdinti kredito pažymą, turite pasirinkti operacijas, anksčiau užregistruotas kliento SF ir jas modifikuoti. SF pavadinimas bus „Koreguojamoji SF‟, nebent pagrindinis juridinio subjekto adresas yra Vokietijoje.




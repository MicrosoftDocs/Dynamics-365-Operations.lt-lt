---
title: "Vidinės įmonės SF išrašymas"
description: "Šiame straipsnyje pateikiama informacija ir pavyzdžiai apie „Microsoft Dynamics 365 for Finance and Operations“ projektų vidinės įmonės SF išrašymą."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3d4354316d0c37c6556c0ec3d27a3c62c5afb7b0
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="intercompany-invoicing"></a>Vidinės įmonės SF išrašymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija ir pavyzdžiai apie „Microsoft Dynamics 365 for Finance and Operations“ projektų vidinės įmonės SF išrašymą.

Jūsų organizacijoje gali būti keli padaliniai, filialai ir kiti juridiniai subjektai, kurie siunčia vieni kitiems su projektais susijusius produktus ir teikia paslaugas. Juridinis subjektas, teikiantis paslaugą arba tiekiantis produktą, vadinamas *skolinančiu juridiniu subjektu*, o juridinis subjektas, gaunantis paslaugą arba produktą – *besiskolinančiu juridiniu subjektu*. 

Toliau pateiktoje iliustracijoje parodytas tipiškas scenarijus, kai du juridiniai subjektai, SI FR (besiskolinantis juridinis subjektas) ir SI JAV (skolinantis juridinis subjektas), bendrai naudoja išteklius, kad galėtų projektą įvykdyti A klientui. Šiame scenarijuje SI FR pagal sutartį turi darbą suteikti A klientui. 

[![Vidinės įmonės SF išrašymo pavyzdys](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Tikslas yra vidinių įmonių projektų operacijų išlaidų kontrolę, įplaukų pripažinimą, mokesčius ir perdavimo kainą padaryti lankstesnius ir veiksmingesnius. Be to, suteikiamos toliau nurodytos galimybės.

-   Kliento SF kūrimas pagal besiskolinančio juridinio subjekto projektą, naudojant skolinančio juridinio subjekto vidinės įmonės grafikus, išlaidas ir tiekėjo SF.
-   Mokesčių skaičiavimo ir netiesioginių išlaidų palaikymas.
-   Skolinančio juridinio subjekto įplaukų pripažinimo atidėjimas ir laiko, kada besiskolinantis juridinis subjektas turėtų pripažinti išlaidas, atidėjimas.
-   Skolinančio juridinio subjekto nebaigtos gamybos (NG) įplaukų kaupimas.
-   Perkėlimo kainų, kurios gali būti grįstos įvairiais kainų modeliais, nustatymas. Štai keletas pavyzdžių:
    -   **Kiekis** – suma, įvedama lauke **Kainos**, yra faktinės kiekio arba vieneto išlaidos.
    -   **Išlaidų suma** – operacijos kaina / išlaidos ir išlaidų suma, įvedama lauke **Kainos**
    -   **Išlaidų procentinis dydis** – perkėlimo kaina yra operacijos kaina / išlaidos, padaugintos iš išlaidų procentinio dydžio, įvedamo lauke **Kainos**.
    -   **Pardavimo kainos procentinis dydis** – pardavimo kainos, perkeliamos skolinančiam juridiniam subjektui, procentinė dalis.
    -   **Už pardavimo kainą mažesnė suma** – pardavimo kainos dalies suma, kurią besiskolinantis juridinis subjektas pasilieka prieš perkeldamas skolinančiam juridiniam subjektui.
    -   **Įnašo koeficientas** – skaičius, įvedamas lauke **Kainos**, yra įnašo koeficientas, kuris išreiškiamas kaip pardavimo kainos procentinė dalis.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>1 Pavyzdys: vidinės įmonės SF išrašymo parametrai
Šiame pavyzdyje USSI yra skolinantis juridinio subjektas, o jo ištekliai teikia laiko ataskaitas pagal besiskolinantį juridinį subjektą, FRSI, kuris yra sudaręs sutartį su galutiniu klientu. Valandos ir išlaidos, apie kurias USSI darbuotojai teikia ataskaitas, gali būti įtraukiamos į FRSI generuojamą projekto SF. Be to, gali būti trečias operacijų šaltinis, susijęs su skolinančiu juridiniu subjektu (šiame pavyzdyje – USSI), kai jis filialams (pvz., FRSI) suteikia bendrų tiekėjų paslaugas ir tada užregistruoja tas išlaidas kaip tų filialų projektų išlaidas. Visus sutampančius sąskaitų faktūrų dokumentus užbaigia ir mokesčius suskaičiuoja „Finance and Operations“. 

Šiame pavyzdyje FRSI turi būti USSI juridinio subjekto klientas, o USSI turi būti FRSI juridinio subjekto tiekėjas. Tada galite nustatyti vidinės įmonės ryšį tarp dviejų juridinių subjektų. Tolesnėje procedūroje parodoma, kaip nustatyti parametrus, kad abu juridiniai subjektai galėtų dalyvauti išrašant vidinės įmonės SF.

1. Nustatykite FRSI kaip USSI juridinio subjekto klientą, o USSI nustatykite kaip FRSI juridinio subjekto tiekėją. Šios užduoties veiksmams atlikti naudojamos trys įvesties vietos.

   | Veiksmas |                                                       Įvesties taškas                                                        |                                                                                                                                                                                               aprašymas                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Pasirinkite USSI ir spustelėkite <strong>Gautinos sumos</strong> &gt; <strong>Klientai</strong> &gt; <strong>Visi klientai</strong>. |                                                                                                                                                                  Sukurkite naują FRSI kliento įrašą ir pasirinkite klientų grupę.                                                                                                                                                                  |
   |  Mlrd.   |    Pasirinkite FRSI ir spustelėkite <strong>Mokėtinos sumos</strong> &gt; <strong>Tiekėjai</strong> &gt; <strong>Visi tiekėjai</strong>.     |                                                                                                                                                                    Sukurkite naują USSI tiekėjo įrašą ir pasirinkite tiekėjų grupę.                                                                                                                                                                    |
   |  K   |                                  Pasirinkę FRSI atidarykite tiekėjo įrašą, kurį ką tik sukūrėte.                                  | Veiksmų srityje, skirtuke <strong>Bendra</strong>, grupėje <strong>Nustatymas</strong> spustelėkite <strong>Vidinė įmonė</strong>. Puslapio <strong>Vidinė įmonė</strong> skirtuke <strong>Prekybiniai ryšiai</strong> slankiklį <strong>Aktyvus</strong> nustatykite į <strong>Taip</strong>. Lauke <strong>Kliento įmonė</strong> pasirinkite kliento įrašą, kurį sukūrėte atlikdami A veiksmą. |


2. Spustelėkite **Projektų valdymas ir apskaita** &gt; **Sąranka** &gt; **Projektų valdymo ir apskaitos parametrai**, tada spustelėkite skirtuką **Vidinė įmonė**. Parametrų nustatymo būdas priklauso nuo to, ar esate besiskolinantysis juridinis subjektas, ar skolinantysis juridinis subjektas.
   -   Jei esate besiskolinantis juridinis subjektas, pasirinkite įsigijimo kategoriją, naudotiną siekiant gretinti tiekėjo SF, kurios sugeneruojamos automatiškai.
   -   Jei esate skolinantis juridinis subjektas, kiekvienam besiskolinančiam objektui pažymėkite kiekvieno operacijos tipo numatytąją projekto kategoriją. Projekto kategorijos naudojamos mokesčių konfigūracijoje, kai vidinės įmonės operacijų SF išrašymo kategorija taikoma tik besiskolinančiam juridiniam subjektui. Galite pasirinkti kaupti vidinės įmonės operacijų įplaukas. Šis kaupimas atliekamas, kai operacijos yra registruojamos, ir jis atšaukiamas, kai vidinės įmonės SF yra užregistruota.

3. Spustelėkite **Projektų valdymas ir apskaita** &gt; **Sąranka** &gt; **Kainos** &gt; **Perkėlimo kaina**.
4. Pasirinkite valiutą, operacijos tipą ir perkėlimo kainos modelį. SF naudojama valiuta sukonfigūruojama skolinančio juridinio subjekto kliento įraše, skirtame besiskolinančiam juridiniam subjektui. Valiuta yra naudoja įrašams perkėlimo kainų lentelėje gretinti.
5. Spustelėkite **DK** &gt; **Registravimo sąranka** &gt; **Vidinės įmonės apskaita** ir nustatykite ryšį tarp USSI ir FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>2 pavyzdys: vidinės įmonės grafiko kūrimas ir registravimas
USSI, skolinantis juridinis subjektas, turi kurti ir registruoti FRSI, besiskolinančio juridinio subjekto, projekto grafiką. Šios užduoties veiksmams atlikti naudojamos dvi įvesties vietos.

| Veiksmas | Įvesties taškas                                                                       | aprašymas                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektų valdymas ir apskaita** &gt; **Grafikai** &gt; **Visi grafikai** | Sukurkite naują grafiką. Grafiko eilutės lauke **Juridinis subjektas** pasirinkite **FRSI**. Lauke **Projekto ID** pasirinkite FRSI projektą. Įveskite kiekvienos savaitės dienos darbo valandas. |
| Mlrd.    | Puslapis **Grafikas**                                                                | Pradėjus darbo eigą, užregistruokite grafiką ir pasižymėkite kvito numerį.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>3 pavyzdys: vidinės įmonės tiekėjo SF kūrimas ir registravimas
USSI, skolinantis juridinis subjektas, turi kurti ir registruoti FRSI, besiskolinančio juridinio subjekto, projekto vidinės įmonės tiekėjo SF. Šioje tiekėjo SF nurodoma užsakomųjų paslaugų darbo jėga ir išlaidos, kurias tiekėjams padengė USSI. Šios užduoties veiksmams atlikti naudojamos dvi įvesties vietos.

| Žingsnis | Įvesties taškas                                                                                      | aprašymas                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Mokėtinos sumos** &gt; **SF** &gt; **Atviros tiekėjų SF** &gt; **Nauja tiekėjo SF** | Sukurkite naują tiekėjo SF ir įveskite į paslaugas, užsakytas vykdant FRSI projektą.                                                                                                                                                                                  |
| Mlrd.    | Puslapis **Tiekėjo SF**                                                                      | Įveskite eilutes, kuriose nurodytos FRSI užsakomosios paslaugos. „FastTab“ **Eilutės informacija**, SF eilutės skirtuke **Projektas**, lauke **Projekto įmonė** įveskite **FRSI**. Įveskite projekto ir atitinkamą informaciją. Tada užregistruokite tiekėjo SF. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>4 pavyzdys: vidinės įmonės SF kūrimas ir registravimas
USSI, skolinantis juridinis subjektas, turi kurti ir registruoti vidinės įmonės SF. Šios užduoties veiksmams atlikti naudojamos dvi įvesties vietos.

| Veiksmas | Įvesties taškas                                                                                             | aprašymas                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektų valdymas ir apskaita** &gt; **Projektų SF** &gt; **Vidinės įmonės kliento SF**  | Spustelėkite **Nauja**, kad atidarytumėte puslapį **Vidinės įmonės SF kūrimas**.                                                                                  |
| Mlrd.    | **Projektų valdymas ir apskaita** &gt; **Projektų SF** &gt; **Vidinės įmonės kliento SF** | Puslapyje **Vidinės įmonės SF kūrimas** įveskite juridinį subjektą, nurodykite operaciją, kurią reikia įtraukti, ir tada spustelėkite **Ieškoti**. |
| K    | **Projektų valdymas ir apskaita** &gt; **Projektų SF** &gt; **Vidinės įmonės kliento SF** | Pasirinkite operacijas, kurių SF išrašyti, arba spustelėkite **Žymėti viską**, kad būtų išrašytos visų sąrašo operacijų SF, o tada spustelėkite **Gerai**.                  |
| D    | Puslapis **Vidinės įmonės SF**                                                                       | Rodomas vidinės įmonės kliento SF pasiūlymas.                                                                                             |
| E    | Puslapis **Vidinės įmonės SF**                                                                       | Spustelėkite **Registruoti.**                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>5 pavyzdys: tiekėjo SF registravimas ir SF išrašymas klientui
Kai skolinantis juridinis subjektas, USSI, užregistruoja vidinės įmonės kliento SF, besiskolinančiame juridiniame subjekte, FRSI, sukuriama atitinkanti laukianti tiekėjo SF. Užregistravus šią tiekėjo SF, FRSI projekto klientui taip pat išrašo SF už darbo valandas, kurias įvedė USSI. Šios užduoties veiksmams atlikti naudojamos trys įvesties vietos.

| Žingsnis | Įvesties taškas                                                                                        | aprašymas                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Mokėtinos sumos** &gt; **SF** &gt; **Laukiančios tiekėjų SF**                            | Peržiūrėkite SF ir įsitikinkite, kad įtrauktos grafiko reikšmės, o tada užregistruokite tiekėjo SF.                  |
| Mlrd.    | **Projektų valdymas ir apskaita** &gt; **Projekto SF** &gt; **Projekto SF pasiūlymai** | Sukurkite naują projekto SF ir įsitikinkite, kad rodomos užregistruotos valandinės operacijos.            |
| K    | Puslapis **Projekto SF**                                                                       | Pasirinkite projekto SF ir tada spustelėkite **Peržiūrėti informaciją**, kad peržiūrėtumėte išlaidų ir pardavimo sumą. Tada SF užregistruokite. |


Daugiau informacijos žr. [Konfigūruoti vidinės įmonės projekto SF išrašymą](tasks/configure-intercompany-project-invoicing.md).




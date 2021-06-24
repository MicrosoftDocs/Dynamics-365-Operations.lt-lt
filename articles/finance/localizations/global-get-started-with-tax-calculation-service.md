---
title: Pradėti naudoti mokesčių skaičiavimą
description: Šioje temoje paaiškinama, kaip nustatyti Mokesčių skaičiavimą.
author: wangchen
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e72b81d4a109db2dd8b4c6ca2ca0b030220e25f3
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216724"
---
# <a name="get-started-with-the-tax-calculation-preview"></a>Pradėti naudoti Mokesčių skaičiavimą (Peržiūros versija)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šioje temoje pateikiama informacija apie tai, kaip pradėti dirbti su Mokesčių skaičiavimu. Pirmiausia ši tema padės atlikti konfigūracijos veiksmus, esančius „Microsoft Dynamics Lifecycle Services“ (LCS), „Regulatory Configuration Service“ (RCS) bei „Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“. Tada peržiūrimas bendras Mokesčių skaičiavimo galimybių naudojimo procesas „Finance” ir „Supply Chain Management“ operacijose.

Nustatymą sudaro keturi pagrindiniai veiksmai:

1. „LCS” įdiekite Mokesčių skaičiavimą.
2. RCS nustatykite Mokesčių skaičiavimo funkciją. Šie nustatymo duomenys nėra specifiniai kiekvienam juridiniam subjektui. Jį galima bendrai naudoti su juridiniais subjektais „Finance and Supply Chain Management“.
3. „Finance” ir „Supply Chain Management“ nustatykite Mokesčių skaičiavimo parametrus pagal juridinį subjektą.
4. „Finance” ir „Supply Chain Management“ sukurkite operacijas, pavyzdžiui, pardavimo užsakymus, ir naudokite Mokesčių skaičiavimą mokesčiams nustatyti ir skaičiuoti.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš užbaigdami procedūrą šioje temoje, galite atlikti tolesnes išankstines sąlygas:

- Turite prieigą prie savo LCS abonemento ir esate įdiegę LCS projektą su 2 (arba aukštesnės) pakopos aplinka, kurioje veikia „Dynamics 365” 10.0.18 su [„KB4616360”](https://fix.lcs.dynamics.com/Issue/Details?kb=4616360&bugId=568738&dbType=3&qc=1f1c04ff39adad74ef871f539e8d73e14c1893ef7cc4b6e3f7d5c5864ec2781a) arba naujesnė versija.
- Turite prieigą prie savo RCS abonemento.
- Susisiekėte su „Microsoft", kad įgalintumėte skrydžio funkciją įdiegtoje „Finance and Supply Chain Management“ aplinkoje.

## <a name="set-up-tax-calculation-in-lcs"></a>Mokesčių skaičiavimo nustatymas „LCS”

1. Prisijunkite prie [LCS](https://lcs.dynamics.com)
2. Baikite integravimo „Microsoft Power Platform“ nustatymą. Daugiau informacijos žr. [Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Pasirinkite vieną iš įdiegtų ne gamybos aplinkos, tada **pasirinkite Diegti naują papildinį**.
4. Pasirinkite **Mokesčių skaičiavimas (peržiūros versija)**.
5. Perskaitykite ir sutinkate su sąlygomis, tada pasirinkite **Diegti**.

## <a name="set-up-tax-calculation-in-rcs"></a>Mokesčių skaičiavimo nustatymas „RCS”

Šio skyriaus veiksmai nėra susiję su konkrečiu juridiniu subjektu. Šią procedūrą turite užbaigti tik vieną kartą ir galite užbaigti ją bet kuriame RCS juridiniame subjekte.

1. Prisijunkite prie [RCS](https://marketing.configure.global.dynamics.com/).
2. Darbo palinkoje **Elektroninių ataskaitų**, įtraukite naują konfigūravimo tiekėją. Naudokite savo įmonės pavadinimą kaip tiekėjo pavadinimą. Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Pasirinkite ką tik sukurtą konfigūravimo tiekėją, tada veiksmų srityje pasirinkite **Nustatykite įjungtą**.
4. Pasirinkite **„Microsoft“** konfigūravimo tiekėją, rinkitės **Saugyklos**.
5. Lauke **Tipas** pasirinkite **Bendri**.
6. Pasirinkite **Atidaryti**.
7. Eikite š **Mokesčių duomenų modelis**, išplėskite failų medį, o tada pasirinkite **Mokesčių konfigūracija**.
8. Pasirinkite naujausią versiją, o tada pasirinkite **Importuoti**.
9. Grįžkite į **Globalizavimo funkcijų (Peržiūros versija)** darbo sritį, pasirinkite **Funkcijos** , pasirinkite **Mokesčių skaičiavimas** plytelę, o tada pasirinkite **Įtraukti**.
10. Pasirinkti vieną iš šių tolesnių funkcijų tipų:

    - **Nauja funkcija** – kurti priemonės nustatymą, kuriame yra tuščias turinys.
    - **Pagal esamą priemonę** – kurti priemonę iš esamos priemonės ir kopijuoti turinį iš esamos priemonės nustatymo.

11. Įveskite naujos išankstinės parinkties funkciją ir aprašą ir pasirinkite **Kurti funkciją**.

    Sukūrus priemonę, automatiškai sukuriama jos juodraščio versija.

12. Pasirinkite nustatymo šablono funkcijos versiją ir tada pasirinkite **Redaguoti**. Puslapis **Mokesčių skaičiavimo nustatymas** yra užpildytas.
13. Pasirinkite **Konfigūravimo versiją**. Turėtumėte matyti konfigūracijos versiją, kurią importavote 8 žingsniu.

    „Microsoft" pateikia numatytąją mokesčių skaičiavimo priedo mokesčio konfigūraciją. Ši konfigūracija apima daugelį mokesčių skaičiavimo elgsenų reikalavimų. Jis bus atnaujintas atsižvelgiant į rinkos grįžtamąjį ryšį. Jei turite išplėsti konfigūraciją, kad ji atitiktų konkrečius reikalavimus, informacijos apie tai, kaip generuoti ir pasirinkti savo mokesčių konfigūraciją, žr. [Kaip sukurti mokesčių](./tax-service-add-data-fields-tax-integration-by-extension.md) tarnybos plėtinį.

    Kai pasirenkate **konfigūracijos** versiją, pasirodo keli papildomi skirtukai:

    - **Mokesčių kodai** – Šis skirtukas yra privalomas. Tai naudojama siekiant prižiūrėti mokesčių kodų pagrindinius duomenis. Visi mokesčių kodai, sukurti šiame skirtuke, automatiškai sinchronizuojami su „Finance“, kai juridiniame subjekte įgalinate dabartinę mokesčių priemonės nustatymo versiją.
    - **Mokesčių kodų taikymas** – Šis skirtukas yra privalomas. Jis naudojamas matricai, kuri nurodo mokesčio kodą, mokesčių grupę ir prekės mokesčių grupę, apibrėžti. Mokesčio kodas, kuris yra naudojamas mokesčio sumai apskaičiuoti. Mokesčių **kodo, mokesčių** grupės ir prekių mokesčių grupės laukų vertės **grąžinamos** į **„Finance“**.
    - **Kliento mokesčių registracijos numerio taikymas** – Šis skirtukas yra nebūtinas. Jei turite kelis vieno kliento mokesčių registracijos numerius, Mokesčių skaičiavimas gali automatiškai nustatyti teisingą mokesčių registracijos numerį. Šioje skirtuko matricoje apibrėžiate taisykles, kurios naudojamos nustatymui atlikti. Kitaip „Finance and Supply Chain Management“ toliau naudos numatytąjį mokesčio registracijos numerį pardavimo operacijų apmokestinamuose dokumentuose.
    - **Tiekėjo mokesčių registracijos numerio taikymas** – Šis skirtukas yra nebūtinas. Jei turite kelis vieno tiekėjo mokesčių registracijos numerius, Mokesčių skaičiavimas gali automatiškai nustatyti teisingą mokesčių registracijos numerį. Šioje skirtuko matricoje apibrėžiate taisykles, kurios naudojamos nustatymui atlikti. Kitaip „Finance and Supply Chain Management“ toliau naudos numatytąjį mokesčio registracijos numerį pirkimo operacijų apmokestinamuose dokumentuose.
    - **Sąrašo kodo taikymas** – Šis skirtukas nebūtinas. Tai gali padėti automatiškai nustatyti sąrašo kodo **lauko** vertę, naudojant lankstesnes ir konfigūruotinas taisykles. Šioje skirtuko matricoje galite apibrėžti taisykles, kurios naudojamos nustatymui atlikti. Kitaip „Finance and Supply Chain Management“ toliau naudos numatytąjį mokesčio kodo mokesčių dokumentuose.

14. Skirtuke **Mokesčių kodai** **pasirinkite** Įtraukti, tada įveskite mokesčio kodą ir aprašymą.
15. Pasirinkite **Mokesčių komponentą**. Mokesčių komponentas yra grupė metodų, nustatytų ankstesnėje pasirinktos mokesčių konfigūracijos versijoje. Prieinami šie mokesčių komponentai:

    - Pagal grynąją sumą
    - Pagal sumą su mokesčiais
    - Pagal kiekį
    - Pagal maržą
    - Mokestis nuo mokesčio

16. Pasirinkite **Įrašyti**. Atsižvelgiant į pasirinktą mokesčio komponentą, tampa galima naudoti daugiau laukų.
17. Norėdami nustatyti mokesčio kodo pobūdį, naudokite šias pasirinktis:

    - Atleidžiama nuo mokesčių
    - Mokesčiai taikomi
    - Taikomas atvirkštinis apmokestinimas
    - Neįtraukti į Pagrindinės sumos skaičiavimą

    Naudojimo mokesčio scenarijui nustatykite vieną mokesčio kodą, kuris turi teigiamą mokesčio tarifą, ir pažymėkite jį kaip **Naudojimo mokestį**.

    Atvirkštinio apmokestinimo scenarijui nustatykite du mokesčių kodus, iš kurių vienas turi teigiamą mokesčio tarifą, o kitas – neigiamą mokesčio tarifą, tačiau tą pačią tarifo vertę. Neigiamas mokesčio kodas pažymėkite kaip **Yra atvirkštinis mokestis**. Daugiau informacijos apie „Finance“ mokėjimo atšaukimas rasite PVM / [GST schemos atvirkštinio apmokestinimo](emea-reverse-charge.md) mechanizmą.
    
    Kai kuriems mokesčių tipams, kurie turėtų būti neįtraukti skaičiuojant kainą įtraukiančių operacijų pagrindinę sumą, pavyzdžiui, muito mokestį kai kuriose šalyse, pasirinkite žymės langelį **Neįtraukti į pagrindinės sumos skaičiavimą**.

    Tvarkyti šio mokesčio kodo mokesčių tarifus ir mokesčių sumos ribas.

18. Pakartodami 14–17 veiksmus įtraukite visus reikiamus mokesčių kodus.
19. Mokesčių **kodų taikomumo** skirtuke pasirinkite stulpelius, kurių reikia teisingam mokesčio kodui nustatyti, tada pasirinkite **Įtraukti**.
20. Įvesti arba pasirinkti kiekvieno stulpelio vertes. Mokesčių **kodo, mokesčių** grupės ir prekių mokesčių grupės laukų vertės **grąžinamos** į **matricą**.
21. Norėdami nustatyti kliento mokesčių registracijos numerių, tiekėjo mokesčių registracijos numerių ir sąrašo kodų taikomumą, pakartokite 19–20 žingsnius.
22. Pasirinkite **Įrašyti** ir uždarykite puslapį.
23. Pasirinkite **Keisti statusą** \> **Užbaigtas**. Pakeitus būseną **į Baigta**, versijos redaguoti nebegalima.
24. Rinkitės **Keiskite būseną** \> **Publikuoti**. Ši mokesčių priemonės nustatymo versija bus perstumta į visuotinę saugyklą ir ji bus matoma kiekvienam „Finance“ juridiniam subjektui.

## <a name="dynamics-365-setup"></a>„Dynamics 365" nustatymas

Užbaigę RCS nustatymą, kaip aprašyta ankstesniame skyriuje, turėsite publikuotą mokesčių priemonės versiją. Atlikite tolesnius veiksmus, kad nustatytumėte Mokesčių skaičiavimą „Finance“ platformoje.

Šiame skyriuje nustatymą atlikti gali juridinis subjektas. Turite jį sukonfigūruoti kiekvienam juridiniam subjektui, kuriam „Finance“ platformoje norite įjungti Mokesčių skaičiavimą.

1. „Finance” platformoje eikite į **Mokesčiai** \> **Nustatymas** \> **Mokesčių konfigūracija** \> **Mokesčių apskaičiavimo nustatymas (Peržiūros versija)**.
2. Skirtuke **Bendra** nustatykite toliau pateiktus laukus.

    - **Įgalinti Mokesčių skaičiavimą** – pasirinkite šį žymės langelį, norėdami įgalinti Mokesčių skaičiavimo priedą juridiniam subjektui. Jeigu jis nėra įgalintas dabartiniam juridiniam subjektui, juridinis subjektas ir toliau naudos esamą mokesčių variklį mokesčiams nustatyti ir apskaičiuoti.
    - **Funkcijos nustatymas** – pasirinkite publikuotų mokesčių priemonės nustatymą ir juridinio subjekto versiją. Daugiau informacijos apie tai, kaip nustatyti ir baigti publikuotą mokesčių funkciją, rasite ankstesniame šios temos skyriuje.
    - **Verslo procesas** – Pasirinkite verslo procesus, kuriuos norite įgalinti.
    - **Įjungti mokesčio kodo** koregavimą – nustatykite šią **pasirinkti** kaip Taip, norėdami įjungti mokesčių kodo koregavimus PVM puslapyje.

3. Skirtuke **Skaičiavimas** nurodykite numatomą juridinio subjekto apvalinimo taisyklę.
4. Skirtuke **Klaidų tvarkymas** nurodykite numatomą juridinio subjekto klaidų tvarkymo metodą. Kiekvienam rezultato kodui galimos trys parinktys:

    - Ne
    - Perspėjimas
    - Klaida

5. Įrašykite nustatymą.
6. Kartokite 1–5 veiksmus su kiekvienu papildomu juridiniu asmeniu.

## <a name="transaction-processing"></a>Operacijos vykdymas

Atlikę visas nustatymo procedūras, galite naudoti Mokesčių skaičiavimo funkciją, kad nustatytumėte ir apskaičiuotumėte mokesčius „Finance“ platformoje. Veiksmai, kuriuos reikia atlikti operacijoms apdoroti, lieka tokie pat. „Finance“ versijoje 10.0.18 palaikomos šios operacijos:

- Pardavimo procesas

    - Pardavimo pasiūlymas
    - Pardavimo užsakymas
    - Patvirtinimas
    - Išrinkimo dokumentas
    - Važtaraštis
    - Pardavimo sąskaita faktūra
    - Kredito sąskaita
    - Grąžinimo užsakymas
    - Antraštės lygmenyje pateikiamos išlaidos
    - Eilutės mokestis

- Pirkimo procesas

    - Pirkimo užsakymas
    - Patvirtinimas
    - Gavimų sąrašas
    - Gavimo dokumentas
    - Pirkimo SF
    - Antraštės lygmenyje pateikiamos išlaidos
    - Eilutės mokestis
    - Kredito sąskaita
    - Grąžinimo užsakymas
    - Pirkimo paraiška
    - Pirkimo reikalavimo eilutės keitimas
    - Pasiūlymo patvirtinimas
    - Pasiūlymo patvirtinimo antraštės kainas
    - Pasiūlymo patvirtinimo eilutės mokesčiai

- Atsargų procesas

    - Perlaidos užsakymas - siuntimas
    - Perlaidos užsakymas - gavimas

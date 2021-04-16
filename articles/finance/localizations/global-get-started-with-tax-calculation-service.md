---
title: Pradėti nuo mokesčių skaičiavimo priedo
description: Šioje temoje paaiškinta, kaip nustatyti mokesčių skaičiavimo priedą.
author: wangchen
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 835ae33fba31d4bccb218969aa9aa61eaa7a3061
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832598"
---
# <a name="get-started-with-the-tax-calculation-add-in-preview"></a>Pradėti nuo mokesčių skaičiavimo priedo (peržiūra)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šioje temoje pateikiama informacija apie tai, kaip pradėti nuo mokesčių skaičiavimo priedo. Pirmiausia ši tema padės atlikti konfigūracijos veiksmus, esančius „Microsoft Dynamics Lifecycle Services“ (LCS), „Regulatory Configuration Service“ (RCS) bei „Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“. Tada peržiūri bendrą procesą, kaip naudoti mokesčių skaičiavimo priedą „Finance and Supply Chain Management“ transakcijos.

Nustatymą sudaro keturi pagrindiniai veiksmai:

1. LCS, įdiekite mokesčių skaičiavimo priedą.
2. RCS nustatykite mokesčių skaičiavimo priemonę. Šie nustatymo duomenys nėra specifiniai kiekvienam juridiniam subjektui. Jį galima bendrai naudoti su juridiniais subjektais „Finance and Supply Chain Management“.
3. „Finance and Supply Chain Management“ nustatykite mokesčių skaičiavimo priedų parametrus pagal juridinį subjektą.
4. „Finance and Supply Chain Management“ metu kurkite operacijas, pvz., pardavimo užsakymus, ir naudodami mokesčio skaičiavimo priedą nustatykite ir skaičiuokite mokesčius.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš užbaigdami procedūrą šioje temoje, galite atlikti tolesnes išankstines sąlygas:

- Turite prieigą prie savo LCS abonemento ir įdiegę LCS projektą su 2 pakopos (arba aukščiau) aplinka, kurioje veikia „Dynamics 365" 10.0.18 arba naujesnė versija.
- Turite prieigą prie savo RCS abonemento.
- Susisiekėte su „Microsoft", kad įgalintumėte skrydžio funkciją įdiegtoje „Finance and Supply Chain Management“ aplinkoje.

## <a name="set-up-the-tax-calculation-add-in-in-lcs"></a>Nustatykite mokesčių skaičiavimo priedą LCS

1. Prisijungti prie [LCS](https://lcs.dynamics.com)
2. Baikite integravimo „Microsoft Power Platform“ nustatymą. Daugiau informacijos žr. [Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Pasirinkite vieną iš įdiegtų ne gamybos aplinkos, tada **pasirinkite Diegti naują papildinį**.
4. Rinkitės **Mokesčių skaičiavimas (peržiūra)**.
5. Perskaitykite ir sutinkate su sąlygomis, tada pasirinkite **Diegti**.

## <a name="set-up-the-tax-calculation-add-in-in-rcs"></a>Nustatykite mokesčių skaičiavimo priedą RCS

Šio skyriaus veiksmai nėra susiję su konkrečiu juridiniu subjektu. Šią procedūrą turite užbaigti tik vieną kartą ir galite užbaigti ją bet kuriame RCS juridiniame subjekte.

1. Prisijunkite prie [RCS](https://marketing.configure.global.dynamics.com/).
2. „Finance“ **Elektrininių ataskaitų** darbo aplinkoje, įtraukite naują konfigūravimo tiekėją. Naudokite savo įmonės pavadinimą kaip tiekėjo pavadinimą. Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Pasirinkite ką tik sukurtą konfigūravimo tiekėją, tada veiksmų srityje pasirinkite **Nustatykite įjungtą**.
4. Pasirinkite **„Microsoft“** konfigūravimo tiekėją, rinkitės **Saugyklos**.
5. Lauke **Tipas** pasirinkite **Bendri**.
6. Pasirinkite **Atidaryti**.
7. Eikite **į mokesčių duomenų** modelį, išplėskite failų medį, tada pasirinkite **Mokesčių konfigūracija –** Europa.
8. Pasirinkite naujausią versiją, o tada pasirinkite **Importuoti**.
9. Grįžkite **į globalizavimo priemones (Peržiūros) darbo sritį,** **pasirinkite** Funkcijos, pasirinkite **mokesčių skaičiavimo** išklotinę dalį, tada pasirinkite **Įtraukti**.
10. Pasirinkti vieną iš šių tolesnių funkcijų tipų:

    - **Nauja funkcija** – kurti priemonės nustatymą, kuriame yra tuščias turinys.
    - **Pagal esamą priemonę** – kurti priemonę iš esamos priemonės ir kopijuoti turinį iš esamos priemonės nustatymo.

11. Įveskite naujos išankstinės parinkties funkciją ir aprašą ir pasirinkite **Kurti funkciją**.

    Sukūrus priemonę, automatiškai sukuriama jos juodraščio versija.

12. Pasirinkite nustatymo šablono funkcijos versiją ir tada pasirinkite **Redaguoti**. Užpildytas **mokesčių skaičiavimo** nustatymo puslapis.
13. Pasirinkite **Konfigūravimo versiją**. Turėtumėte matyti konfigūracijos versiją, kurią importavote 8 žingsniu.

    „Microsoft" pateikia numatytąją mokesčių skaičiavimo priedo mokesčio konfigūraciją. Ši konfigūracija apima daugelį mokesčių skaičiavimo elgsenų reikalavimų. Jis bus atnaujintas atsižvelgiant į rinkos grįžtamąjį ryšį. Jei turite išplėsti konfigūraciją, kad ji atitiktų konkrečius reikalavimus, informacijos apie tai, kaip generuoti ir pasirinkti savo mokesčių konfigūraciją, žr. [Kaip sukurti mokesčių](https://go.microsoft.com/fwlink/?linkid=2138483) tarnybos plėtinį.

    Kai pasirenkate **konfigūracijos** versiją, pasirodo keli papildomi skirtukai:

    - **Mokesčių kodai** – šis skirtukas privalomas mokesčių skaičiavimo tarnybai. Tai naudojama siekiant prižiūrėti mokesčių kodų pagrindinius duomenis. Visi mokesčių kodai, sukurti šiame skirtuke, automatiškai sinchronizuojami su „Finance“, kai juridiniame subjekte įgalinate dabartinę mokesčių priemonės nustatymo versiją.
    - **Mokesčių kodų taikymas** – šis skirtukas privalomas mokesčių skaičiavimo priedui. Jis naudojamas matricai, kuri nurodo mokesčio kodą, mokesčių grupę ir prekės mokesčių grupę, apibrėžti. Mokesčio kodas, kuris yra naudojamas mokesčio sumai apskaičiuoti. Mokesčių **kodo, mokesčių** grupės ir prekių mokesčių grupės laukų vertės **grąžinamos** į **„Finance“**.
    - **Kliento mokesčių registracijos numerio taikymas** – šis skirtukas pasirenkamas mokesčių skaičiavimo priedui. Jei turite kelis vieno kliento mokesčio registracijos numerius, mokesčių skaičiavimo priedas gali automatiškai nustatyti teisingą mokesčio registracijos numerį. Šiame skirtuko matricoje apibrėžiate taisykles, kurias priedas naudoja nustatymui atlikti. Kitaip „Finance and Supply Chain Management“ toliau naudos numatytąjį mokesčio registracijos numerį pardavimo operacijų apmokestinamuose dokumentuose.
    - **Tiekėjo mokesčių registracijos numerio taikymas** – šis skirtukas pasirenkamas mokesčių skaičiavimo priedui. Jei turite kelis vieno tiekėjo mokesčio registracijos numerius, mokesčių skaičiavimo priedas gali automatiškai nustatyti teisingą mokesčio registracijos numerį. Šiame skirtuko matricoje apibrėžiate taisykles, kurias priedas naudoja nustatymui atlikti. Kitaip „Finance and Supply Chain Management“ toliau naudos numatytąjį mokesčio registracijos numerį pirkimo operacijų apmokestinamuose dokumentuose.
    - **Sąrašo kodų taikymas** – šis skirtukas pasirenkamas mokesčių skaičiavimo priedui. Tai gali padėti automatiškai nustatyti sąrašo kodo **lauko** vertę, naudojant lankstesnes ir konfigūruotinas taisykles. Šioje skirtuko matricoje galite apibrėžti taisykles, kurias priedas naudoja nustatymui atlikti. Kitaip „Finance and Supply Chain Management“ toliau naudos numatytąjį mokesčio kodo mokesčių dokumentuose.

14. Skirtuke **Mokesčių kodai** **pasirinkite** Įtraukti, tada įveskite mokesčio kodą ir aprašymą.
15. Pasirinkite **mokesčio komponentą**. Mokesčio komponentas yra mokesčių skaičiavimo metodų, kurie buvo nustatyti ankstesnėje pasirinktos mokesčių konfigūracijos versijoje, grupė. Prieinami šie mokesčių komponentai:

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
    - Neįtraukti skaičiuojant pagrindinę sumą

    Naudojimo mokesčio scenarijui nustatykite vieną mokesčio kodą, kuris turi teigiamą mokesčio tarifą, ir pažymėkite jį kaip **Naudojimo mokestį**.

    Atvirkštinio apmokestinimo scenarijui nustatykite du mokesčių kodus, iš kurių vienas turi teigiamą mokesčio tarifą, o kitas – neigiamą mokesčio tarifą, tačiau tą pačią tarifo vertę. Neigiamas mokesčio kodas pažymėkite kaip **Yra atvirkštinis mokestis**. Daugiau informacijos apie „Finance“ mokėjimo atšaukimas rasite PVM / [GST schemos atvirkštinio apmokestinimo](emea-reverse-charge.md) mechanizmą.
    
    Kai kuriuose mokesčių tipuose, kurie turi būti neįtraukti skaičiuojant į kainą įtrauktų operacijų pagrindinę sumą, pvz., kai kurių šalių pasirinktinio muito mokestį, pažymėkite žymės langelį Neįtraukti bazinės sumos **skaičiavime**.

    Tvarkyti šio mokesčio kodo mokesčių tarifus ir mokesčių sumos ribas.

18. Pakartodami 14–17 veiksmus įtraukite visus reikiamus mokesčių kodus.
19. Mokesčių **kodų taikomumo** skirtuke pasirinkite stulpelius, kurių reikia teisingam mokesčio kodui nustatyti, tada pasirinkite **Įtraukti**.
20. Įvesti arba pasirinkti kiekvieno stulpelio vertes. Mokesčių **kodo, mokesčių** grupės ir prekių mokesčių grupės laukų vertės **grąžinamos** į **matricą**.
21. Norėdami nustatyti kliento mokesčių registracijos numerių, tiekėjo mokesčių registracijos numerių ir sąrašo kodų taikomumą, pakartokite 19–20 žingsnius.
22. Pasirinkite **Įrašyti** ir uždarykite puslapį.
23. Pasirinkite **Keisti statusą** \> **Užbaigtas**. Pakeitus būseną **į Baigta**, versijos redaguoti nebegalima.
24. Rinkitės **Keiskite būseną** \> **Publikuoti**. Ši mokesčių priemonės nustatymo versija bus perstumta į visuotinę saugyklą ir ji bus matoma kiekvienam „Finance“ juridiniam subjektui.

## <a name="dynamics-365-setup"></a>„Dynamics 365" nustatymas

Užbaigę RCS nustatymą, kaip aprašyta ankstesniame skyriuje, turėsite publikuotą mokesčių priemonės versiją. Atlikite tolesnius veiksmus, kad nustatytumėte mokesčių skaičiavimą „Finance“ priede.

Šiame skyriuje nustatymą atlikti gali juridinis subjektas. Turite jį sukonfigūruoti kiekvienam juridiniam subjektui, kuriam norite įjungti mokesčių skaičiavimo priedą „Finance“.

1. Finansų srityje eikite **į**\>**Mokesčių**\>**nustatymo**\>**mokesčių konfigūracijos mokesčių perskaičiavimo priedo nustatymą** (Peržiūra).
2. Skirtuke **Bendra** nustatykite toliau pateiktus laukus.

    - **Įgalinti mokesčių skaičiavimo priedą** – pažymėkite šį žymės langelį, norėdami įgalinti juridinio subjekto mokesčių skaičiavimo priedą. Jei nėra įgalintas dabartinio juridinio subjekto mokesčių skaičiavimo priedas, juridinis subjektas ir toliau naudos esamą mokesčių sistemą mokesčiui nustatyti ir apskaičiuoti.
    - **Funkcijos nustatymas** – pasirinkite publikuotų mokesčių priemonės nustatymą ir juridinio subjekto versiją. Daugiau informacijos apie tai, kaip nustatyti ir baigti publikuotą mokesčių funkciją, rasite ankstesniame šios temos skyriuje.
    - **Verslo procesas** – pasirinkite verslo procesus, kad įgalintumėte mokesčių skaičiavimo priedą.
    - **Įjungti mokesčio kodo** koregavimą – nustatykite šią **pasirinkti** kaip Taip, norėdami įjungti mokesčių kodo koregavimus PVM puslapyje.

3. Skirtuke **Skaičiavimas** nurodykite numatomą juridinio subjekto apvalinimo taisyklę.
4. Skirtuke **Klaidų tvarkymas** nurodykite numatomą juridinio subjekto klaidų tvarkymo metodą. Mokesčių skaičiavimo papildinys gali pasirinkti tris kiekvieno rezultato kodo pasirinktis:

    - nr.
    - Perspėjimas
    - Klaida

5. Įrašykite mokesčių skaičiavimo priedą nustatyme.
6. Kartokite 1–5 veiksmus su kiekvienu papildomu juridiniu asmeniu.

## <a name="transaction-processing"></a>Operacijos vykdymas

Baigę visas nustatymo procedūras, galite naudoti mokesčių skaičiavimo priedą, norėdami nustatyti ir apskaičiuoti „Finance“ mokesčius. Veiksmai, kuriuos reikia atlikti operacijoms apdoroti, lieka tokie pat. „Finance“ versijoje 10.0.18 palaikomos šios operacijos:

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

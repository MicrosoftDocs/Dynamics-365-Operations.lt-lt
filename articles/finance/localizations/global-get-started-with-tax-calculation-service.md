---
title: Pradėti naudoti mokesčių skaičiavimą
description: Šioje temoje paaiškinama, kaip nustatyti Mokesčių skaičiavimą.
author: wangchen
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f26f8e5eafe29e88c26d3fb6cfa950466ec6be9
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647439"
---
# <a name="get-started-with-tax-calculation"></a>Pradėti naudoti mokesčių skaičiavimą

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie tai, kaip pradėti dirbti su Mokesčių skaičiavimu. Ši tema padės atlikti konfigūracijos veiksmus, esančius „Microsoft Dynamics Lifecycle Services“ (LCS), „Regulatory Configuration Service“ (RCS), „Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“. Tada peržiūrimas bendras Mokesčių skaičiavimo galimybių naudojimo procesas „Finance” ir „Supply Chain Management“ operacijose.

Nustatymą sudaro keturi pagrindiniai veiksmai:

1. Sprendime LCS įdiekite papildinį Mokesčių skaičiavimas.
2. RCS nustatykite Mokesčių skaičiavimo funkciją. Šie nustatymo duomenys nėra specifiniai kiekvienam juridiniam subjektui. Jį galima bendrai naudoti su juridiniais subjektais „Finance and Supply Chain Management“.
3. „Finance” ir „Supply Chain Management“ nustatykite Mokesčių skaičiavimo parametrus pagal juridinį subjektą.
4. „Finance” ir „Supply Chain Management“ sukurkite operacijas, pavyzdžiui, pardavimo užsakymus, ir naudokite Mokesčių skaičiavimą mokesčiams nustatyti ir skaičiuoti.

## <a name="prerequisites"></a>Būtinieji komponentai

Kad galėtumėte atlikti šioje temoje nurodytas procedūras, turi būti tenkinamos kiekvieno aplinkos tipo būtinosios sąlygos.

Turi būti laikomasi šių būtinųjų komponentų:

- Turite turėti prieigą prie savo LCS paskyros ir turite būti įdiegę LCS projektą su 2 arba didesnės pakopos aplinka, kurioje veikia „Dynamics 365" 10.0.21 arba naujesnė versija.
- Savo organizacijai turite sukurti RCS aplinką ir turite turėti prieigą prie savo paskyros. Daugiau informacijos apie RCS aplinkos kūrimą ieškokite temoje [„Regulatory Configuration Service“ apžvalga](rcs-overview.md).
- Atsižvelgiant į verslo poreikius, jūsų įdiegtos „Finance“ arba „Supply Chain Management“ aplinkos darbo srityje **Funkcijų valdymas** turi būti įjungtos tolesnės funkcijos.

    - Mokesčių skaičiavimo paslauga
    - Palaikyti kelis PVM registracijos numerius
    - Perkėlimo užsakymo dokumente nurodytas mokestis

- Jūsų įdiegtos RCS aplinkos darbo srityje **Funkcijų valdymas** turi būti įjungtos toliau nurodytos funkcijos.

    - Globalizacijos funkcijos

## <a name="set-up-tax-calculation-in-lcs"></a>Mokesčių skaičiavimo nustatymas „LCS”

1. Prisijunkite prie [LCS](https://lcs.dynamics.com)
2. Baikite integravimo „Microsoft Power Platform“ nustatymą. Daugiau informacijos žr. [Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Pasirinkite vieną iš įdiegtų aplinkų, tada pasirinkite **Diegti naują papildinį**.
4. Pasirinkite **Mokesčių skaičiavimas**.
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
8. Pagal savo „Finance“ versiją pasirinkite tinkamą mokesčių konfigūracijos versiją, tada – **Importuoti**.

    | Leidimo versija | Mokesčių konfigūracija                       |
    | --------------- | --------------------------------------- |
    | 10.0.18         | Mokesčių konfigūracija – Europa 30.12.82     |
    | 10.0.19         | Mokesčių skaičiavimo konfigūracija 36.38.193 |
    | 10.0.20         | Mokesčių skaičiavimo konfigūracija 40.43.208 |
    | 10.0.21         | Mokesčių skaičiavimo konfigūracija 40.48.215 |

9. Darbo srityje **Globalizacijos funkcijos** pasirinkite **Funkcijos**, plytelę **Mokesčių skaičiavimas**, o tada pasirinkite **Įtraukti**.
10. Pasirinkti vieną iš šių tolesnių funkcijų tipų:

    - **Nauja funkcija** – kurti priemonės nustatymą, kuriame yra tuščias turinys.
    - **Pagal esamą priemonę** – kurti priemonę iš esamos priemonės ir kopijuoti turinį iš esamos priemonės nustatymo.

11. Įveskite naujos išankstinės parinkties funkciją ir aprašą ir pasirinkite **Kurti funkciją**.

    Sukūrus priemonę, automatiškai sukuriama jos juodraščio versija. Jei norite juodraščio versiją pritaikyti kaip bet kurią baigtą versiją, galite pasirinkti **Gauti šią versiją**.

12. Pasirinkite nustatymo šablono funkcijos versiją ir tada pasirinkite **Redaguoti**. Puslapis **Mokesčių skaičiavimo nustatymas** yra užpildytas.
13. Pasirinkite **Konfigūravimo versiją**. Turėtumėte matyti konfigūracijos versiją, kurią importavote 8 žingsniu.

    „Microsoft" pateikia numatytąją mokesčių konfigūraciją mokesčiams skaičiuoti. Ši konfigūracija apima daugelį mokesčių skaičiavimo elgsenų reikalavimų. Jis bus atnaujintas atsižvelgiant į rinkos grįžtamąjį ryšį. Jei turite išplėsti konfigūraciją, kad ji atitiktų konkrečius reikalavimus, informacijos apie tai, kaip generuoti ir pasirinkti savo mokesčių konfigūraciją, žr. [Kaip sukurti mokesčių](./tax-service-add-data-fields-tax-integration-by-extension.md) tarnybos plėtinį.

14. Kai pasirenkate **Konfigūracijos versija**, pasirodo keli papildomi skirtukai. Norėdami atlikti privalomąją skirtukų sąranką, vadovaukitės čia pateikta tvarka.

    **Privalomoji sąranka**

    - **Mokesčių kodai** – tvarkomi bendrieji mokesčių kodų duomenys. Visi mokesčių kodai, sukurti šiame skirtuke, automatiškai sinchronizuojami su „Finance“, kai įgalinate dabartinę versiją.
    - **Mokesčių grupė** – šioje grupėje nurodykite bendruosius mokesčių grupės duomenis ir mokesčių kodus.
    - **Prekių mokesčių grupė** – šioje grupėje nurodykite bendruosius prekių mokesčių grupės duomenis ir mokesčių kodus.

    **Pasirinktinis nustatymas**

    - **Mokesčių grupės taikymas** – nustatykite matricą, pagal kurią nustatoma mokesčių grupė. Jei šioje matricoje jokia taikymo taisyklė nesutampa su „Dynamics 365“ apmokestinamu dokumentu, Mokesčių skaičiavimas naudoja numatytąją vertę apmokestinamo dokumento eilutėje.
    - **Prekių mokesčių grupės taikymas** – nustatykite matricą, pagal kurią nustatoma prekių mokesčių grupė. Jei šioje matricoje jokia taikymo taisyklė nesutampa su „Dynamics 365“ apmokestinamu dokumentu, Mokesčių skaičiavimas naudoja numatytąją vertę apmokestinamo dokumento eilutėje.
    - **Kliento mokesčių registracijos numerio taikymas** – jei turite kelis vieno kliento mokesčių registracijos numerius, Mokesčių skaičiavimas gali automatiškai nustatyti tinkamą mokesčių registracijos numerį. Šio skirtuko matricoje apibrėžkite taisykles, kurios turi būti naudojamos nustatymui atlikti. Kitaip „Finance and Supply Chain Management“ toliau naudos numatytąjį mokesčio registracijos numerį pardavimo operacijų apmokestinamuose dokumentuose.
    - **Tiekėjo mokesčių registracijos numerio taikymas** – jei turite kelis vieno tiekėjo mokesčių registracijos numerius, Mokesčių skaičiavimas gali automatiškai nustatyti tinkamą mokesčių registracijos numerį. Šio skirtuko matricoje apibrėžkite taisykles, kurios turi būti naudojamos nustatymui atlikti. Kitaip „Finance and Supply Chain Management“ toliau naudos numatytąjį mokesčio registracijos numerį pirkimo operacijų apmokestinamuose dokumentuose.
    - **Sąrašo kodo taikymas** – galite automatiškai nustatyti lauko **Sąrašo kodas** vertę, naudodami lankstesnes ir konfigūruotinas taisykles. Šio skirtuko matricoje apibrėžkite taisykles, kurios turi būti naudojamos nustatymui atlikti. Kitaip „Finance and Supply Chain Management“ toliau naudos numatytąjį mokesčio kodo mokesčių dokumentuose.

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
    - Yra naudojimo mokestis
    - Yra atvirkštinis apmokestinimas
    - Neįtraukti į pagrindinės sumos skaičiavimą

    Naudojimo mokesčio scenarijui nustatykite vieną mokesčio kodą, kuris turi teigiamą mokesčio tarifą, ir pažymėkite jį kaip **Yra naudojimo mokestis**.

    Atvirkštinio apmokestinimo scenarijui nustatykite du mokesčių kodus, iš kurių vienas turi teigiamą mokesčio tarifą, o kitas – neigiamą mokesčio tarifą, tačiau tą pačią tarifo vertę. Neigiamas mokesčio kodas pažymėkite kaip **Yra atvirkštinis mokestis**. Daugiau informacijos apie „Finance“ mokėjimo atšaukimas rasite PVM / [GST schemos atvirkštinio apmokestinimo](emea-reverse-charge.md) mechanizmą.

    Kai kuriems mokesčių tipams, kurie turi būti neįtraukti skaičiuojant kainą apimančių operacijų pagrindinę sumą (pavyzdžiui, muito mokestį kai kuriose šalyse ar regionuose), pažymėkite žymės langelį **Neįtraukti į pagrindinės sumos skaičiavimą**. Daugiau informacijos apie šį parametrą ieškokite temoje [Mokesčio, pridedamo prie kainos, skaičiavimas, kai įjungta Kainos apima mokesčius](global-exclude-from-tax-base-amount-calculation.md)

    Tvarkyti šio mokesčio kodo mokesčių tarifus ir mokesčių sumos ribas.

18. Pakartodami 14–17 veiksmus įtraukite visus reikiamus mokesčių kodus.
19. Skirtuke **Mokesčių grupė** pasirinkite stulpelį **Mokesčių grupė**, įtraukite jį į matricą kaip įvesties sąlygą, o tada įtraukite eilutes bendriesiems mokesčių grupės duomenims tvarkyti.

    Toliau pateikiamas pavyzdys.

    | Mokesčių grupė    | Mokesčių kodai           |
    | ------------ | ------------------- |
    | DEU_Domestic | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Domestic | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

20. Skirtuke **Prekių mokesčių grupė** pasirinkite stulpelį **Prekių mokesčių grupė**, įtraukite jį į matricą kaip įvesties sąlygą, o tada įtraukite eilutes bendriesiems prekių mokesčių grupės duomenims tvarkyti.

    Toliau pateikiamas pavyzdys.

    | Prekių mokesčių grupė | Mokesčių kodai                                    |
    | -------------- | -------------------------------------------- |
    | Pilnas           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Exempt |
    | Sumažintas        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

21. Skirtuke **Mokesčių grupės taikymas** pasirinkite stulpelius, kurių reikia tinkamai mokesčių grupei nustatyti, tada pasirinkite **Įtraukti**. Įvesti arba pasirinkti kiekvieno stulpelio vertes. Šios matricos išvestis bus laukas **Mokesčių grupė**. Jei šis skirtukas nebus sukonfigūruotas, bus naudojama operacijos eilutėje nurodyta mokesčių grupė.

    Toliau pateikiamas pavyzdys.

    | Verslo procesas | Pristatyti iš | Gavėjas | Mokesčių grupė    |
    | ---------------- | --------- | ------- | ------------ |
    | Pardavimas            | DEU       | DEU     | DEU_Domestic |
    | Pardavimas            | DEU       | FRA     | DEU_EU       |
    | Pardavimas            | BEL       | BEL     | BEL_Domestic |
    | Pardavimas            | BEL       | FRA     | BEL_EU       |

22. Skirtuke **Prekių mokesčių grupės taikymas** pasirinkite stulpelius, kurių reikia tinkamam mokesčių kodui nustatyti, tada pasirinkite **Įtraukti**. Įvesti arba pasirinkti kiekvieno stulpelio vertes. Šios matricos išvestis bus laukas **Prekių mokesčių grupė**. Jei šis skirtukas nebus sukonfigūruotas, bus naudojama operacijos eilutėje nurodyta prekių mokesčių grupė.

    Toliau pateikiamas pavyzdys.

    | Prekės kodas | Prekių mokesčių grupė |
    | --------- | -------------- |
    | D0001     | Pilnas           |
    | D0003     | Sumažintas        |

    Daugiau informacijos apie tai, kaip mokesčių kodai yra nustatomi papildinyje Mokesčių skaičiavimas, žr. [PVM grupės ir prekių PVM grupės nustatymo logika](global-sales-tax-group-determination.md).

23. Pagal verslo poreikius nustatykite kliento mokesčių registracijos numerių, tiekėjo mokesčių registracijos numerių ir sąrašo kodų taikymą.
24. Pasirinkite **Įrašyti** ir uždarykite puslapį.
25. Pasirinkite **Keisti statusą** \> **Užbaigtas**. Pakeitus būseną **į Baigta**, versijos redaguoti nebegalima.
26. Rinkitės **Keiskite būseną** \> **Publikuoti**. Ši mokesčių priemonės nustatymo versija bus perstumta į visuotinę saugyklą ir ji bus matoma kiekvienam „Finance“ juridiniam subjektui.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Papildinio Mokesčių skaičiavimas nustatymas programoje „Dynamics 365“

Baigę RCS sąranką turėsite publikuotą mokesčių funkcijos versiją. Atlikite tolesnius veiksmus, kad nustatytumėte Mokesčių skaičiavimą „Finance“ platformoje.

Šiame skyriuje nustatymą atlikti gali juridinis subjektas. Turite jį sukonfigūruoti kiekvienam juridiniam subjektui, kuriam „Finance“ platformoje norite įjungti Mokesčių skaičiavimą.

1. „Finance” platformoje eikite į **Mokesčiai** \> **Nustatymas** \> **Mokesčių konfigūracija** \> **Mokesčių skaičiavimo parametrai**.
2. Skirtuke **Bendra** nustatykite toliau pateiktus laukus.

    - **Įgalinti mokesčių skaičiavimo tarnybą** – pažymėkite šį žymės langelį, norėdami įgalinti papildinį Mokesčių skaičiavimas juridiniam subjektui. Jeigu jis nėra įgalintas dabartiniam juridiniam subjektui, juridinis subjektas ir toliau naudos esamą mokesčių variklį mokesčiams nustatyti ir apskaičiuoti.
    - **Funkcijos nustatymas** – pasirinkite publikuotų mokesčių priemonės nustatymą ir juridinio subjekto versiją. Daugiau informacijos apie tai, kaip nustatyti ir baigti publikuotą mokesčių funkciją, rasite ankstesniame šios temos skyriuje.
    - **Verslo procesas** – Pasirinkite verslo procesus, kuriuos norite įgalinti.

3. Skirtuke **Skaičiavimas** nurodykite numatomą juridinio subjekto apvalinimo taisyklę. Daugiau informacijos apie apvalinimo logiką ieškokite srityje [Mokesčių skaičiavimo apvalinimo taisyklės](https://go.microsoft.com/fwlink/?linkid=2166988).
4. Skirtuke **Klaidų tvarkymas** nurodykite numatomą juridinio subjekto klaidų tvarkymo metodą. Galimos tolesnės trys parinktys.

    - nr.
    - Perspėjimas
    - Klaida

    Skyriuje **Išsami informacija** galite nustatyti kiekvieno rezultatų kodo klaidų tvarkymo metodą. Arba, jei kai kurie rezultatų kodai nesinchronizuojami iš mokesčių skaičiavimo tarnybos, skyriuje **Bendra** galite nustatyti numatytąjį metodą.

5. Skirtuke **Kelios PVM registracijos** galite atskirai įjungti PVM deklaraciją, ES pardavimo sąrašą ir „Intrastat“, kad galėtumėte dirbti su keliomis PVM registracijomis. Daugiau informacijos apie kelių PVM registracijų mokesčių ataskaitas rasite temoje [Kelių PVM registracijų ataskaitos](emea-reporting-for-multiple-vat-registrations.md).
6. Įrašykite sąranką ir pakartokite ankstesnius veiksmus su kiekvienu papildomu juridiniu subjektu. Kai publikuojama nauja versija ir norite ją taikyti, nustatykite lauką **Funkcijų sąranka**, esantį puslapio **Mokesčių skaičiavimo parametrai** skirtuke **Bendra** (žr. 2 veiksmą).

## <a name="transaction-processing"></a>Operacijos vykdymas

Atlikę visas nustatymo procedūras, galite naudoti papildinį Mokesčių skaičiavimas, kad nustatytumėte ir apskaičiuotumėte mokesčius „Finance“ platformoje. Veiksmai, kuriuos reikia atlikti operacijoms apdoroti, lieka tokie pat. „Finance“ versijoje 10.0.21 palaikomos šios operacijos:

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

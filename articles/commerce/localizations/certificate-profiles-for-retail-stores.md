---
title: Vartotojo apibrėžti mažmeninės prekybos parduotuvių sertifikatų profiliai
description: Šioje temoje pateikiama sertifikatų naudojimo mažmeninės prekybos parduotuvėse apžvalga.
author: josaw
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 81fa3770a137471e3d7f8cab3c7d7f37febe64fa
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018873"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Vartotojo apibrėžti mažmeninės prekybos parduotuvių sertifikatų profiliai

[!include [banner](../includes/banner.md)]


## <a name="overview"></a>Peržiūra

Šioje temoje pateikiama sertifikatų profilių, pasiekiamų „Microsoft Dynamics 365 Commerce“, apžvalga. Šios funkcijos praplečia funkcijos [Mažmeninės prekybos kanalų slaptųjų raktų valdymas](../dev-itpro/manage-secrets.md) galimybes, įtraukdamos vietinių sertifikatų palaikymą.

Kai elektroninis kasos aparatas (EKA) veikia autonominiu režimu, jis negali pasiekti sertifikatų, saugomų raktų saugykloje. Todėl reikia naudoti vietinį sertifikatą. Palaikomos toliau nurodytos galimybės.

- Vietinių sertifikatų naudojimas raktų saugyklos atsarginiuose scenarijuose
- Vietinių sertifikatų naudojimas be raktų saugyklos (pavyzdžiui, vietiniame diegime)
- Laipsniškas sertifikatų naujinimas, kai kai kurios parduotuvės ir terminalai naudoja naują sertifikato versiją, bet kitos parduotuvės ir terminalai ir toliau naudoja ankstesnę versiją

Sertifikatų profilių funkcijos leidžia nurodyti numatytąjį sertifikatą ir nustatyti tvarką, pagal kurią ieškoma sertifikatų tame pačiame sertifikato profilyje. Šios funkcijos taip pat teikia panašų vietinių sertifikatų ir raktų saugyklos sertifikatų nustatymo būdą. Galima įtraukti įmonei būdingus sertifikatų parametrus, tačiau „Commerce” kanaluose galima naudoti unikalų kiekvieno sertifikato visų įmonių identifikatorių.

### <a name="scenarios"></a>Scenarijai

Sertifikatų profilių funkcijos palaiko toliau pateiktus „Commerce” kanalų scenarijus.

- Vietinio sertifikato naudojimas raktų saugyklos atsarginiuose scenarijuose. Toliau pateikiami keli atsarginių scenarijų pavyzdžiai:

    - Raktų saugykla nepasiekiama.
    - Sertifikato negalima surasti raktų saugykloje.
    - EKA veikia autonominiu režimu.

- Vietinių sertifikatų naudojimas neišsaugojant jų raktų saugykloje (pavyzdžiui, vietiniame diegime).
- Laipsniškas sertifikatų naujinimas, kai nauja sertifikato versija naudojama tik parduotuvėse ar terminaluose, kuriuose nauja versija jau pasiekiama.
- To paties sertifikato naudojimas keliose įmonėse.

## <a name="set-up-certificate-profiles"></a>Sertifikatų profilių nustatymas

Toliau pateikta procedūra paaiškina, kaip nustatyti sertifikatų profilius. Prieš pradėdami naudoti sertifikatų profilius „Commerce” kanaluose, atlikite toliau pateiktus veiksmus, kad sukonfigūruotumėte parametrus.

1. Darbo srityje **Funkcijų valdymas** įjunkite funkciją **Vartotojo apibrėžti mažmeninės prekybos parduotuvių sertifikatų profiliai**.
2. Eikite į **Sistemos administravimas \> Sąranka \> Sertifikatų profiliai**.
3. Sukurkite įrašą ir nustatykite jo laukus **Sertifikato profilis**, **Pavadinimas** ir **Aprašas**.

    > [!NOTE]
    > Sertifikato profilis yra unikalus sertifikato identifikatorius visose įmonėse ir „Commerce” komponentuose.

3. Skirtuke **Juridiniai subjektai** įtraukite eilutę ir pasirinkite juridinį subjektą (įmonę), kuris turi būti naudojamas dabartiniam sertifikato profiliui. Jei sertifikato profilis turi būti naudojamas keliems juridiniams subjektams, pakartokite šį veiksmą, kad įtrauktumėte eilutę kiekvienam papildomam juridiniam subjektui.
4. Pasirinkite **Parametrai**, kad būtų atidarytas puslapis **Sertifikato profilio parametrai**, kuriame galite įvesti įmonei būdingus sertifikato profilio parametrus.

### <a name="certificate-profile-settings"></a>Sertifikato profilio parametrai

Pasirinkus sertifikato profilio eilučių **parametrus**, atsiranda puslapis **Sertifikato profilio parametrai**. Šiame puslapyje galite nurodyti, kurie sertifikatai gali būti naudojami, kai dabartinis sertifikato profilis iškviečiamas „Commerce” kanaluose. Taip pat galite nurodyti tvarką, pagal kurią turi būti ieškoma sertifikatų.

> [!NOTE]
> Laukas **Prioritetas** nustatomas automatiškai. Reikšmė **1** nurodo didžiausią prioritetą. Kai nauja eilutė įtraukiama į puslapį **Sertifikato profilio parametrai**, jos prioritetas nustatomas kaip skaičių, kuris vienu skaičiumi didesnis nei ankstesnės eilutės prioriteto skaičius. Norėdami pakeisti konkrečios eilutės prioritetą, pasirinkite eilutę ir tada pasirinkite **Perkelti aukštyn**, norėdami padidinti prioritetą, arba **Perkelti žemyn**, norėdami sumažinti prioritetą.

Kai įtraukiate naują eilutę į puslapį **Sertifikato profilio parametrai**, nustatykite toliau nurodytus laukus.

- **Vietos tipas** – pasirinkite vietą, kurioje saugomas sertifikatas. Yra dvi galimos šio lauko reikšmės: **Vietinis sertifikatas** ir **„Key Vault”**.
- **„Key Vault” sertifikatas** – šis laukas reikalingas, jei nustatote lauką **Vietos tipas** į **„Key Vault”**. Naudokite jį, norėdami nurodyti „Key Vault” sertifikato slaptąjį raktą.

    > [!NOTE]
    > Prieš pradėdami naudoti „Key Vault” sertifikatą sertifikatų profiliuose, nusiųskite sertifikatą į raktų saugyklą ir sekite instrukcijas, pateiktas [„Azure Key Vault“ kliento nustatymas](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).

- **Saugyklos pavadinimas** – šis laukas yra pasirinktinis ir yra galimas tik tada, jei nustatote lauką **Vietos tipas** į **Vietinis sertifikatas**. Naudokite jį, norėdami nurodyti numatytąjį saugyklos pavadinimą, kurį reikia naudoti ieškant vietinių sertifikatų.
- **Saugojimo vieta** – šis laukas yra pasirinktinis ir yra galimas tik tada, jei nustatote lauką **Vietos tipas** į **Vietinis sertifikatas**. Naudokite jį, norėdami nurodyti numatytąją saugojimo vietą, kurią reikia naudoti ieškant vietinių sertifikatų.

    > [!NOTE]
    > Numatytasis saugyklos pavadinimas ir saugojimo vieta įtraukiami siekiant supaprastinti vietinių sertifikatų ieškojimo „Commerce Runtime” procesą. X509StoreProvider yra aplankų, kuriuose saugomi sertifikatai, sąrašas. Jei nenurodytas numatytasis saugyklos pavadinimas ir numatytoji saugojimo vieta, X509StoreProvider bando rasti sertifikatą kituose jo sąrašo aplankuose.

- **Kontrolinis kodas** – šis laukas yra būtinas ir yra galimas tik tada, jei nustatote lauką **Vietos tipas** į **Vietinis sertifikatas**. Naudokite jį, norėdami nurodyti sertifikato kontrolinį kodą.
- **Komentarai** – šis laukas yra pasirinktinis ir leidžia vartotojams įvesti pastabas.

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Darbo eiga: sertifikatų ieška „Commerce Runtime”

Toliau nurodyta pagrindinė darbo eiga, naudojama ieškant sertifikato, kai sertifikato profilis iškviečiamas „Commerce Runtime”.

1. Sistema identifikuoja, ar sertifikato profilyje yra įmonei būdingi dabartinio juridinio subjekto parametrai.
1. Sistema bando rasti sertifikatą, naudodama puslapio **Sertifikato profilio parametrai** reikšmes toje eilutėje, kurioje laukas **Prioritetas** nustatytas į **1**.

    - Jei laukas **Vietos tipas** nustatytas į **„Key Vault”**, lauko **„Key Vault” sertifikato slaptasis raktas** reikšmė naudojama ieškant sertifikato puslapyje **Raktų saugyklos parametrai**. Tada sertifikato ieškoma raktų saugykloje.
    - Jei laukas **Vietos tipas** nustatytas į **Vietinis sertifikatas**, X509StoreProvider pirmiausia ieško sertifikato naudodama numatytąjį saugyklos pavadinimą ir saugojimo vietą, jei šie parametrai nurodyti. Tada ieškoma visuose kituose aplankų sąrašo aplankuose.

1. Jei sertifikato nerandama, procesas kartojamas eilutei, kurios laukas **Prioritetas** nustatytas į **2**, ir t. t.

> [!NOTE]
> Jei sertifikato profilyje nėra dabartinio juridinio subjekto parametrų arba jei visų eilučių sertifikato ieška yra nesėkminga puslapyje **Sertifikato profilio parametrai**, sertifikato negalima rasti.

#### <a name="caching-the-results-of-certificate-searches"></a>Sertifikato paieškų rezultatų kaupimas talpykloje

Sertifikato paieškų rezultatai kaupiami talpykloje. Numatytasis talpyklos galiojimo pabaigos laikas yra viena valanda. Tačiau šį laiką galima tinkinti ir nustatyti į maksimalią 24 valandų reikšmę.

### <a name="gradual-update"></a>Laipsniškas naujinimas

Jei įdiegiama nauja sertifikato versija, bet jos negalima atnaujinti visose parduotuvėse vienu metu, sertifikatų profilių funkcijos leidžia palaipsniui atnaujinti sertifikatą.

1. Raskite sertifikato profilį ir eilutę, kuri turi būti atnaujinta, tada pasirinkite **Parametrai**.
1. Įtraukite eilutę ir nurodykite parametrus, susijusius su naujausia sertifikato versija.
1. Padidinkite naujos eilutės reikšmę **Prioritetas**. Norėdami perkelti eilutę taip, kad ji būtų virš to paties sertifikato ankstesnės versijos eilutės, naudokite mygtuką **Perkelti aukštyn**.

> [!NOTE]
> „Commerce Runtime” pirmiausia bus iškviesta nauja sertifikato versija. Jei sertifikatas dar neatnaujintas konkrečioje parduotuvėje arba terminale, bus iškviesta ankstesnė versija.

---
title: Vartotojo apibrėžti mažmeninės prekybos parduotuvių sertifikatų profiliai
description: Šiame straipsnyje pateikta sertifikatų profilių, kurie yra galimi, apžvalga Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558443"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Vartotojo apibrėžti mažmeninės prekybos parduotuvių sertifikatų profiliai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta sertifikatų profilių, kurie yra galimi, apžvalga Microsoft Dynamics 365 Commerce. Šios funkcijos praplečia funkcijos [Mažmeninės prekybos kanalų slaptųjų raktų valdymas](../dev-itpro/manage-secrets.md) galimybes, įtraukdamos vietinių sertifikatų palaikymą.

Kol "Point of sale" (EKA) veikia režimu ne tinkle, jis negali pasiekti sertifikatų, Microsoft Azure saugomų "Key Vault". Todėl reikia naudoti vietinį sertifikatą. Palaikomos toliau nurodytos galimybės.

- Vietinių sertifikatų naudojimas "Key Vault" atsarginuose scenarijuose
- Vietinių sertifikatų naudojimas be kodo "Vault" (pvz., diegiant vietiniame kompiuteryje)
- Laipsniškas sertifikatų naujinimas, kai kai kurios parduotuvės ir terminalai naudoja naują sertifikato versiją, bet kitos parduotuvės ir terminalai ir toliau naudoja ankstesnę versiją

Sertifikatų profilių funkcijos leidžia nurodyti numatytąjį sertifikatą ir nustatyti tvarką, pagal kurią ieškoma sertifikatų tame pačiame sertifikato profilyje. Šios funkcijos taip pat teikia panašų vietinių sertifikatų ir raktų saugyklos sertifikatų nustatymo būdą. Galima įtraukti įmonei būdingus sertifikatų parametrus, tačiau „Commerce” kanaluose galima naudoti unikalų kiekvieno sertifikato visų įmonių identifikatorių.

### <a name="scenarios"></a>Scenarijai

Sertifikatų profilių funkcijos palaiko toliau pateiktus „Commerce” kanalų scenarijus.

- Naudokite vietinį sertifikatą "Key Vault" atsarginuose scenarijuose. Toliau pateikiami keli atsarginių scenarijų pavyzdžiai:

    - Raktų saugykla nepasiekiama.
    - Sertifikato negalima surasti raktų saugykloje.
    - EKA veikia autonominiu režimu.

- Naudokite vietinius sertifikatus, bet jų neįrašę į "Key Vault" (pvz., vietiniame diegime).
- Laipsniškas sertifikatų naujinimas, kai nauja sertifikato versija naudojama tik parduotuvėse ar terminaluose, kuriuose nauja versija jau pasiekiama.
- To paties sertifikato naudojimas keliose įmonėse.

## <a name="set-up-certificate-profiles"></a>Sertifikatų profilių nustatymas

Toliau pateikta procedūra paaiškina, kaip nustatyti sertifikatų profilius.

### <a name="set-up-key-vault"></a>Nustatyti "Key Vault"

Kad naudodami skaitmeninį sertifikatą, saugomą "Key Vault", galėsite naudoti šiuos veiksmus.

1. Sukurkite rakto "Vault" saugyklos sąskaitą. Rekomenduojame saugyklos sąskaitą įdiegti tame pačiame geografiniame regione kaip ir "Commerce Scale Unit".
1. Įkelti skaitmeninį sertifikatą į "Key Vault" saugyklos sąskaitą.
1. Įgaliokite programos objektų serverio (AOS) programą skaityti paslapius iš rakto Vault saugyklos abonemento.

Norėdami gauti daugiau informacijos apie tai, kaip dirbti su "Key Vault", žr [. "Pradėkite naudodami "Azure Key Vault"](/azure/key-vault/key-vault-get-started).

### <a name="set-up-system-parameters"></a>Nustatyti sistemos parametrus

Prieš konfigūrdami sertifikatų šablonus "Commerce" kanaluose, turite įgalinti "Commerce" naudoti ir sertifikatus, kurie saugomi rakto Vault bei sertifikatų profiliuose.

Norėdami nustatyti sistemos parametrus "Commerce Headquarters", atlikite šiuos veiksmus.

1. Sistemos parametrų **puslapyje** nustatykite parinktį Naudoti išplėstinę **sertifikatų saugyklą** kaip **Taip**.
1. Darbo srityje **Funkcijų valdymas** įjunkite funkciją **Vartotojo apibrėžti mažmeninės prekybos parduotuvių sertifikatų profiliai**.

### <a name="set-up-key-vault-parameters"></a>Nustatyti "Key Vault" parametrus

**"Key Vault" parametrų** puslapyje, norėdami pasiekti "Key Vault" saugyklą, turite nurodyti šiuos parametrus:

- **Vardas** ir **aprašymas** – rakto Vault saugyklos sąskaitos pavadinimas ir aprašas.
- **Rakto "Vault" URL – "Key Vault" saugyklos sąskaitos URL**.
- **Kodo Vault klientas** – interaktyvios programos, kuri susieta su rakto Vault saugyklos sąskaita, kad būtų galima autentifikuoti, ID Azure Active Directory Azure AD. Šis klientas turi turėti prieigą skaityti paslapčių iš saugyklos sąskaitos.
- **Rakto Vault slapyvo** raktas – slaptasis Azure AD raktas, susietas su programa, kuri naudojama autentifikuoti "Key Vault" saugyklos sąskaitoje.
- **Pavadinimas**, **aprašymas** ir slapti **nuoroda** – sertifikato pavadinimas, aprašymas ir slapti nuoroda.

Norėdami gauti daugiau informacijos, žr. ["Azure Key Vault" kliento programą](../../finance/localizations/setting-up-azure-key-vault-client.md).

### <a name="configure-a-certificate-profile"></a>Sertifikato profilio konfigūravimas

Norėdami sukonfigūruoti sertifikato šabloną "Commerce Headquarters", atlikite šiuos veiksmus.

1. Eikite į **Sistemos administravimas \> Sąranka \> Sertifikatų profiliai**.
1. Veiksmų srityje pasirinkite **Naujas** įrašui sukurti.
1. Įveskite vertes į laukus **Sertifikato profilis** **·**, Pavadinimas **ir** Aprašymas.

    > [!NOTE]
    > Sertifikato profilis yra unikalus sertifikato identifikatorius visose įmonėse ir „Commerce” komponentuose.

1. Norėdami įtraukti **eilutę**, juridinių subjektų "**FastTab**" pasirinkite Įtraukti.
1. Po **juridiniu subjektu** pasirinkite juridinį subjektą (įmonę), kuriam turėtų būti naudojamas dabartinio sertifikato profilis.

    Jei sertifikato šablonas turėtų būti naudojamas keliems juridiniams subjektams, pakartokite 4 ir 5 veiksmus, kad prie kiekvieno papildomo juridinio subjekto pridėtumėte eilutę.

1. Pasirinkite **Parametrai**, kad būtų atidarytas puslapis **Sertifikato profilio parametrai**, kuriame galite įvesti įmonei būdingus sertifikato profilio parametrus. Nurodyti, kurie sertifikatai gali būti naudojami, kai dabartinis sertifikatų profilis iškvievie naudojamas komercijos kanaluose. Įtraukite tiek sertifikatų, kiek jums reikia, ir nustatykite jų prioritetus. Jei sertifikato, kuris yra aukštesnis prioritetas, nėra, bus naudojamas kitas sertifikatas, atsižvelgiant į prioritetą. Daugiau informacijos rasite skyriuje Darbo eiga [: sertifikatų ieška komercijos vykdymo laiko](#workflow-searching-certificates-in-the-commerce-runtime) skyriuje.

    > [!NOTE]
    > Laukas **Prioritetas** nustatomas automatiškai. Reikšmė **1** nurodo didžiausią prioritetą. Kai nauja eilutė įtraukiama į puslapį **Sertifikato profilio parametrai**, jos prioritetas nustatomas kaip skaičių, kuris vienu skaičiumi didesnis nei ankstesnės eilutės prioriteto skaičius. Norėdami pakeisti konkrečios eilutės prioritetą, pasirinkite eilutę ir tada pasirinkite **Perkelti aukštyn**, norėdami padidinti prioritetą, arba **Perkelti žemyn**, norėdami sumažinti prioritetą.

1. Kai pridedate naują eilutę sertifikato profilio **parametrų** puslapyje, nustatykite šiuos laukus:

    - **Vietos tipas** – pasirinkite vietą, kurioje saugomas sertifikatas. Yra dvi galimos šio lauko reikšmės: **Vietinis sertifikatas** ir **„Key Vault”**.
    - **„Key Vault” sertifikatas** – šis laukas reikalingas, jei nustatote lauką **Vietos tipas** į **„Key Vault”**. Naudokite jį, norėdami nurodyti „Key Vault” sertifikato slaptąjį raktą.
    - **Saugyklos pavadinimas** – šis laukas yra pasirinktinis ir yra galimas tik tada, jei nustatote lauką **Vietos tipas** į **Vietinis sertifikatas**. Naudokite jį, norėdami nurodyti numatytąjį saugyklos pavadinimą, kurį reikia naudoti ieškant vietinių sertifikatų.
    - **Saugojimo vieta** – šis laukas yra pasirinktinis ir yra galimas tik tada, jei nustatote lauką **Vietos tipas** į **Vietinis sertifikatas**. Naudokite jį, norėdami nurodyti numatytąją saugojimo vietą, kurią reikia naudoti ieškant vietinių sertifikatų.

        > [!NOTE]
        > Numatytasis saugyklos pavadinimas ir saugojimo vieta įtraukiami siekiant supaprastinti vietinių sertifikatų ieškojimo „Commerce Runtime” procesą. X509StoreProvider yra aplankų, kuriuose saugomi sertifikatai, sąrašas. Jei nenurodytas numatytasis parduotuvės pavadinimas ir numatytoji saugojimo vieta, X509StoreProvider bando rasti sertifikatą kituose jos sąrašo aplankuose. Norėdami gauti daugiau informacijos apie galimas parduotuvės pavadinimo ir parduotuvės vietos reikšmes, žr [. StoreName Enum ir](/dotnet/api/system.security.cryptography.x509certificates.storename)[StoreLocation Enum](//dotnet/api/system.security.cryptography.x509certificates.storelocation).

    - **Nykščio** atspaudas – šis laukas yra būtinas ir jį galima naudoti tik tada, jei vietos **tipo lauką** nustatote kaip vietinį **sertifikatą**. Naudokite jį, norėdami nurodyti sertifikato kontrolinį kodą.

        > [!IMPORTANT]
        > Turite užtikrinti, kad programą paleidęs vartotojas, kuris turi naudoti vietinį sertifikatą (pvz., "Modern POS" autonominiu režimu) turėtų bent tik skaitymo prieigą prie sertifikato privačiojo rakto.

    - **Komentarai** – šis laukas yra pasirinktinis ir leidžia vartotojams įvesti pastabas.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>Darbo eiga: sertifikatų ieška „Commerce Runtime”

Toliau nurodyta pagrindinė darbo eiga, naudojama ieškant sertifikato, kai sertifikato profilis iškviečiamas „Commerce Runtime”.

1. Sistema identifikuoja, ar sertifikato profilyje yra įmonei būdingi dabartinio juridinio subjekto parametrai.
1. Sistema bando rasti sertifikatą, naudodama puslapio **Sertifikato profilio parametrai** reikšmes toje eilutėje, kurioje laukas **Prioritetas** nustatytas į **1**.

    - Jei laukas **Vietos tipas** nustatytas į **„Key Vault”**, lauko **„Key Vault” sertifikato slaptasis raktas** reikšmė naudojama ieškant sertifikato puslapyje **Raktų saugyklos parametrai**. Tada sertifikato ieškoma raktų saugykloje.
    - Jei laukas **Vietos tipas** nustatytas į **Vietinis sertifikatas**, X509StoreProvider pirmiausia ieško sertifikato naudodama numatytąjį saugyklos pavadinimą ir saugojimo vietą, jei šie parametrai nurodyti. Tada ieškoma visuose kituose aplankų sąrašo aplankuose.

1. Jei sertifikato nerandama, procesas kartojamas eilutei, kurios laukas **Prioritetas** nustatytas į **2**, ir t. t.

> [!NOTE]
> Jei sertifikato profilyje nėra dabartinio juridinio subjekto parametrų arba jei visų eilučių sertifikato ieška yra nesėkminga puslapyje **Sertifikato profilio parametrai**, sertifikato negalima rasti.

### <a name="caching-the-results-of-certificate-searches"></a>Sertifikato paieškų rezultatų kaupimas talpykloje

Sertifikato paieškų rezultatai kaupiami talpykloje. Numatytasis talpyklos galiojimo pabaigos laikas yra viena valanda. Tačiau šį laiką galima tinkinti ir nustatyti į maksimalią 24 valandų reikšmę.

## <a name="gradual-update"></a>Laipsniškas naujinimas

Jei įdiegiama nauja sertifikato versija, bet jos negalima atnaujinti visose parduotuvėse vienu metu, sertifikatų profilių funkcijos leidžia palaipsniui atnaujinti sertifikatą.

1. Raskite sertifikato profilį ir eilutę, kuri turi būti atnaujinta, tada pasirinkite **Parametrai**.
1. Įtraukite eilutę ir nurodykite parametrus, susijusius su naujausia sertifikato versija.
1. Padidinkite naujos eilutės reikšmę **Prioritetas**. Norėdami perkelti eilutę taip, kad ji būtų virš to paties sertifikato ankstesnės versijos eilutės, naudokite mygtuką **Perkelti aukštyn**.
> [!NOTE]
> „Commerce Runtime” pirmiausia bus iškviesta nauja sertifikato versija. Jei sertifikatas dar neatnaujintas konkrečioje parduotuvėje arba terminale, bus iškviesta ankstesnė versija.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

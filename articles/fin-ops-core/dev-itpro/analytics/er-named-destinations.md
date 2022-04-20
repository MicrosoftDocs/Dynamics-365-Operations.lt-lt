---
title: Konkrečių spausdinimo valdymo įrašų ER paskirties vietų konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti, konkrečių spausdinimo valdymo įrašų paskirties vietas.
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 4cd99b1d2c0dbbf48e7eee7e1233e3b078d14ba3
ms.sourcegitcommit: 6109fc2fe5f407363bb6f240d64b7214657f5914
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/15/2022
ms.locfileid: "8603060"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Konkrečių spausdinimo valdymo įrašų ER paskirties vietų konfigūravimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip sistemos administratoriaus arba gautinų sumų klerko vaidmenį turintis vartotojas gali atlikti tolesnes užduotis.

- Konfigūruoti ER sprendimo, kuris generuoja laisvos formos sąskaitas faktūras, įvardytąsias [elektroninių ataskaitų (ER)](general-electronic-reporting.md) paskirties vietas.
- Priskirti ER paskirties vietą vienam [spausdinimo valdymo](document-reporting-services.md) įrašui.

Šias procedūras galima atlikti USMF įmonėje. Kodavimas nebūtinas.

## <a name="introduction"></a>Įžanga

Galite konfigūruoti [paskirties vietas](electronic-reporting-destinations.md) kiekvienam ER [formato](general-electronic-reporting.md) [konfigūracijos](general-electronic-reporting.md#Configuration), naudojamos siunčiamam dokumentui generuoti, failo išvesties komponento aplankui. Kai vykdote šio tipo ER formatą ir turite atitinkamas prieigos teises, taip pat gali keisti sukonfigūruotus paskirties vietos parametrus vykdymo metu.

Microsoft Dynamics 365 **10.0.17** ir vėlesnės finansų versijose galima nustatyti ER formato veiksmo kodą, kad būtų galima nurodyti veiksmą, [kurį](er-apis-app10-0-17.md) vartotojai vykdo paleisdami tą ER formatą. Pavyzdžiui, modulio **Gautinos sumos** spausdinimo valdymo parametrų srityje galite pasirinkti ER formatą, generuojantį tam tikrą verslo dokumentą, pavyzdžiui, laisvos formos sąskaitą faktūrą. Tada galėsite pasirinkti **Rodinys** sąskaitai faktūrai peržiūrėti arba **Spausdinti** jos nusiuntimui į spausdintuvą. Jei veiksmas yra perduotas vykdomam ER formatui vykdymo metu, galite [konfigūruoti skirtingas ER paskirties vietas skirtingiems vartotojo veiksmams](er-action-dependent-destinations.md).

**10.0.21 ir vėlesnėse „Finance“ versijose** įvardytoji paskirties vieta gali būti [nustatyta](er-apis-app10-0-21.md) ER formatui ir priskirta spausdinimo valdymo įrašui, kuris apdorojamas, kai ER formatas vykdomas. Pavyzdžiui, modulio **Gautinos sumos** spausdinimo valdymo parametrų srityje rekomenduojame sukonfigūruoti įrašą **Pradinis**, kad būtų atlikti tolesni veiksmai.

- Vykdomas ER formatas.
- Sugeneruota SF el. paštu siunčiama klientui.
- Sukonfigūruojamas įrašas **Kopija**, kad būtų vykdomas toks pat formatas.
- SF kopijos spausdinimas tinklo spausdintuvu.

Šiuo atveju turite sukonfigūruoti skirtingas vykdomo ER formato ER paskirties vietas ir pasirinkti paskirtis skirtingiems spausdinimo valdymo įrašams.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradedant, darbo srityje [Funkcijų valdymas](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) turi būti įjungta funkcija **Leisti nustatyti ER paskirties vietas pagal spausdinimo valdymo elementą**. Šaltinio kodas taip pat turi būti pakeistas, kad būtų galima konfigūruoti dabartiniame „Finance“ egzemplioriuje nurodytas ER paskirties vietas ir įjungti [naująją](er-apis-app10-0-21.md) ER API.

Be to, į „Finance“ egzempliorių turi būti [importuota](er-download-configurations-global-repo.md) ER konfigūracija **Laisvos formos sąskaita faktūra („Excel“)**.

## <a name="configure-a-new-er-destination"></a>Naujos ER paskirties vietos konfigūravimas

1. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
2. Pasirinkite kliento paskyros **US-001** sąskaitą faktūrą.
3. Puslapio **Laisvos formos sąskaita faktūra** skirtuko **Sąskaita faktūra** grupėje **Spausdinimo valdymas** pasirinkite **Spausdinimo valdymas**.
4. Puslapyje **Spausdinimo valdymo sąranka** išplėskite **Modulis – gautinos sumos** \> **Dokumentai** \> **Laisvos formos sąskaita faktūra**, pasirinkite įrašą **Pradinis** ir atlikite tolesnius veiksmus.

    1.  Įsidėmėkite dabartinius toliau nurodytus pasirinkto įrašo parametrus.
        -   Lauke **Ataskaitos formatas** pasirinkta numatytoji SSRS ataskaita **FreeTextInvoice.Report**.
        -   Lauke **Paskirties vieta** rodomas pavadinimas **\<Default\>**, informuojant, kad nėra pasirinktos pasirinktinės paskirties vietos, skirtos priskirtai SSRS ataskaitai. 
    2.  Lauke **Ataskaitos formatas** pasirinkite ER formato konfigūraciją **Laisvos formos sąskaita faktūra („Excel”)**.
        -   Lauko **Paskirties vieta** pavadinimas pakeičiamas į **Paskirties vietos pavadinimas**.
        -   Lauke **Paskirties vietos pavadinimas** rodomas pavadinimas **\<No named destination\>**, informuojant, kad nėra pasirinktos įvardytosios paskirties vietos, skirtos priskirtam ER formatui.
    3.  Pasirinkite rodyklės mygtuką, esantį dešinėje lauko **Paskirties vietos pavadinimas** pusėje.    
    4. Puslapio **Įvardytoji elektroninių ataskaitų paskirties vieta** lauke **Pavadinimas** įveskite **Pagrindinė paskirties vieta**.
    5. Pasirinkite **Įrašyti**.
    6. „FastTab“ **Failų paskirties vieta** [sukonfigūruokite](er-destination-type-email.md) komponento **Ataskaita** paskirties vietą **El. paštas**.
    7. Uždarykite puslapį **Įvardytoji elektroninių ataskaitų paskirties vieta**.
    8. Puslapio **Spausdinimo valdymo sąranka** lauke **Paskirties vietos pavadinimas** pasirinkite įvardytąją paskirties vietą **Pagrindinė paskirties vieta**.

    ![Pasirinkto ER formato įvardytosios ER paskirties vietos konfigūravimas ir priskyrimas sukonfigūruotam spausdinimo valdymo įrašui puslapyje Spausdinimo valdymo sąranka](./media/er-named-destinations-01.gif)

    Dabar sukonfigūravote formato **Laisvos formos sąskaita faktūra („Excel“)** įvardytąją ER paskirties vietą **Pagrindinė paskirties vieta** ir priskyrėte ją spausdinimo valdymo įrašui **Pradinis** dalyje **Modulis – gautinos sumos** \> **Dokumentai** \> **Laisvos formos sąskaita faktūra**.

5. Išplėskite **Modulis – gautinos sumos** \> **Paskyra – US-001** \> **Laisvos formos sąskaita faktūra**, pasirinkite įrašą **Pradinis** ir atlikite tolesnius veiksmus.

    1. Pasirinkite ir palaikykite (arba dešiniuoju pelės mygtuku spustelėkite) įrašą ir pasirinkite **Keisti**.
    2. Pasirinkite rodyklės mygtuką, esantį dešinėje lauko **Paskirties vietos pavadinimas** pusėje.
    3. Puslapio **Įvardytoji elektroninių ataskaitų paskirties vieta** veiksmų srityje pasirinkite **Naujas**.
    4. Lauke **Pavadinimas** įveskite **US-001 paskirties vieta**.
    5. „FastTab“ **Failų paskirties vieta** [sukonfigūruokite](er-destination-type-print.md) komponento **Ataskaita** paskirties vietą **Spausdintuvas**.
    6. Uždarykite puslapį **Įvardytoji elektroninių ataskaitų paskirties vieta**.
    7. Puslapio **Spausdinimo valdymo sąranka** lauke **Paskirties vietos pavadinimas** pasirinkite įvardytąją paskirties vietą **US-001 paskirties vieta**.

    ![Pasirinkto ER formato įvardytosios ER paskirties vietos konfigūravimas ir priskyrimas sukonfigūruotam spausdinimo valdymo įrašui puslapyje Spausdinimo valdymo sąranka](./media/er-named-destinations-02.gif)

    Dabar sukonfigūravote formato **Laisvos formos sąskaita faktūra („Excel“)** įvardytąją ER paskirties vietą **US-001 paskirties vieta** ir priskyrėte ją spausdinimo valdymo įrašui **Pradinis** dalyje **Modulis – gautinos sumos** \> **Paskyra – US-001** \> **Laisvos formos sąskaita faktūra**.

Dabar, kai apdorojama laisvos formos SF, vykdomas ER formatas **Laisvos formos sąskaita faktūra („Excel“)** ir įvyksta vienas iš tolesnių įvykių.

- Jei laisvos formos SF skirta kitam klientui nei US-001, sugeneruotas dokumentas siunčiamas el. paštu.
- Jei laisvos formos SF skirta klientui US-001, sugeneruotas dokumentas išspausdinamas.

> [!NOTE]
> Kai įvardytoji paskirties vieta nėra apibrėžta spausdinimo valdymo įrašui, kuris apdorojamas vykdymo metu, naudojamos numatytosios ER paskirties vietos, jei jų yra apibrėžta vykdomam ER formatui.

> [!IMPORTANT]
> Jei puslapyje **Elektroninių ataskaitų paskirties vieta** (**Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Elektroninių ataskaitų paskirties vieta**) pasirenkate ER formatą, kuriam buvo sukonfigūruota bent viena įvardytoji paskirties vieta, jums pranešama apie esamas įvardytąsias paskirties vietas.
>
> ![Pranešimas apie esamas sukonfigūruotas pasirinkto ER formato įvardytąsias paskirties vietas puslapyje Elektroninių ataskaitų paskirties vieta](./media/er-named-destinations-03.png)
>
> Jei panaikinate numatytąją paskirties vietą, visos įvardytosios paskirties vietos taip pat panaikinamos. Jei šios įvardytosios paskirties vietos buvo pasirinktos spausdinimo valdymo įrašams, šių įvardytųjų paskirties vietų pasirinkimas atšaukiamas.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Esamos ER paskirties vietos kopijavimas kaip naujos įvardytosios paskirties vietos

Kai galima numatytoji įvardytoji ER formato ER paskirties vieta, ji gali būti naudojama kaip naujų ER paskirties vietų šablonas. Norėdami sukurti naują ER paskirties vietą, paremtą numatytąja paskirties vieta, puslapyje **Įvardytoji elektroninių ataskaitų paskirties vieta** pasirinkite **Kopijuoti pagal numatytąją**. Naujoji paskirties vieta pavadinama **Numatytoji**. Galite kartoti šį veiksmą tiek kartų, kiek reikia.

Bet kurią esamą įvardytąją paskirties vietą galite pasirinkti kaip šabloną naujai įvardytajai paskirties vietai. Norėdami sukurti naują įvardytąją ER paskirties vietą, paremtą pasirinkta įvardytąja paskirties vieta, puslapyje **Įvardytoji elektroninių ataskaitų paskirties vieta** pasirinkite **Kopijuoti**. Naujosios paskirties vietos pavadinimas yra toks pat, kaip pasirinktos įvardytosios paskirties vietos, tik pridedama priesaga „Kopija“. Galite kartoti šį veiksmą tiek kartų, kiek reikia.

## <a name="security-considerations"></a>Saugos klausimai

Puslapyje **Spausdinimo valdymo sąranka** įvardytąsias ER paskirties vietas galite nustatyti tik tada, jei turite [teisę](../sysadmin/role-based-security.md#permissions) atlikti šią užduotį. Jums teisė gali būti suteikta, jei vienam iš jūsų [saugos vaidmenų](../sysadmin/role-based-security.md#security-roles) priskiriama [pareiga](../sysadmin/role-based-security.md#duties) **Konfigūruoti elektroninių ataskaitų formato paskirties vietą**. Dėl platesnės informacijos žr. [Saugos klausimai](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)

[„Application Update 10.0.17“ elektroninės ataskaitų sistemos API pakeitimai](er-apis-app10-0-17.md)

[„Application Update 10.0.21“ elektroninės ataskaitų sistemos API pakeitimai](er-apis-app10-0-21.md)

[Kodo keitimas, kad vartotojai galėtų konfigūruoti ir naudoti įvardytąsias ER paskirties vietas](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

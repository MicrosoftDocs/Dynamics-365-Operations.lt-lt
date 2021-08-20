---
title: Atidėjimo klasteriai
description: Atidėjimo klasteriai siūlo būda paimti keletą licencijos lentelių tuo pačiu metu ir tada paimti jas atidėjimui skirtingose vietose. Jos gali būti labai naudingos mažmenos verslui, kai licencijos lentelės dažniausiai nėra pilni inventoriaus padėklai.
author: Mirzaab
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c2b12798a6ef9c2d4aa022e0c270d8191b2cf4e7fc844042ed88c4eb9f5b98a5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741913"
---
# <a name="putaway-clusters"></a>Atidėjimo klasteriai

[!include [banner](../includes/banner.md)]

Atidėjimo klasteriai siūlo būda paimti keletą licencijos lentelių tuo pačiu metu ir tada paimti jas atidėjimui skirtingose vietose. Šis procesas dažnai yra vadinamas *pieno vykdymu*. Atidėjimo klasteriai gali būti labai naudingi mažmenos verslui, kai licencijos lentelės dažniausiai nėra pilni inventoriaus padėklai. 

## <a name="turn-on-the-cluster-putaway-feature"></a>įjunkite klasterio atidėjimo funkciją

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Klasterio atidėjimo funkcija*

## <a name="setup-for-the-example-scenario"></a>Nustatymas pavyzdžio scenarijui

### <a name="cluster-profiles"></a>Klasterio šablonai

Atidėjimo klasterio profilis nustato, ar prekė eis pagrindžiant vieta, kuri yra priskirta elementui gavimo metu. Jei kiti klasteriai yra reikalingi, skirtingi atidėjimo klasteriai turi būti sukurti, kurių kiekvienas turi būti mobiliam įrenginio meniu prekei.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Klasterio šablonai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Rodinyje **Antrašte**, nustatykite tolesnes vertes:

    - **Atidėjimo klasterio profilio ID:** *Klasterio atidėjimas*
    - **Atidėjimo klasterio profilio ID pavadinimas:** *Klasterio atidėjimas*
    - **Klasterio tipas:** *Atidėjimas*
    - **Sekos numeris:** Priimkite numatytąją vertę.

1. Pasirinkite **Įrašyti** tam, kad sudarytume būtinus laukelius **Bendrų** prieinamame „FastTab“.
1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Klasterio priskyrimo laikas:** *Gavimo metu*

        Šis laukelis nustato, ar atidėjimo klasteris turi būti priskirtas nedelsiant, kai inventorius bus gautas arba jis turi būti rūšiuojamas vėliau.

    - **Klasterio priskyrimo taisyklė:** *Rankinė*

        Šis laukelis nustato, ar klasterio priskyrimas turi būti nustatomas automatiškai sistemos ar rankiniu būdu vartotojo.

    - **Nurodymo kodas:** Palikite šį lauką tuščią.
    - **Atidėjimo klasterio aptikimas:** *Gavimas*

        Galimos šios vertės:

        - **Gavimas** – Vieta yra nedelsiant randami gavimo metu.
        - **Klasterio uždarymas** – Vieta yra randama, kai klasteris yra uždarytas.
        - **Naudotojo nukreiptas** – Vieta yra randama, kai licencijos lentelė yra paimama iš klasterio atidėjimui. Tokiu atveju, nėra jokios vietos nurodytos, kai atidėjimo darbas yra sukurtas. Atidėjimo metu, vartotojas gali nuskaityti licencijos lentelę ar darbo ID, kad pradėtų padėjimo žingsnį. Sistema tuomet suranda padėjimo vietą dar kartą ir pasako vartotojui, kuri padėti paimtą kiekį.

    - **Atidėjimo klasteris vartotojui:** *Ne*

        Šis laukelis nustato, ar kiekvienas klasteris turi būti unikalus vartotojui, kai klasteriai yra priskiriami automatiškai. Jis prieinamas tik kai **Klasterio priskyrimo taisyklės** laukelis nustatytas į *Automatinis*.

    - **Vieneto apribojimas:** Palikite šį laukelį tuščią.

        Laukelis nurodo vienetą, kuris turi gauto profilį, kad jis galiotų. Jei jis paliktas tuščias, visi vienetai galioja.

    - **Darbo vieneto suskaldymas:** *Asmeninis*

        Šis laukelis nustato, ar visas inventorius turėtų būti konsoliduotas (naudojant klasterio ID ir licencijos plokštelė) vienoje licencijos plokštelėje uždarius klasterį ir ar jis turi būti atidėtas kaip viena licencijos plokštelė ar atskiras gaunamose licencijos plokštelėse. Šis laukelis yra neprieinamas, kai **Atidėjimo klasterio vietos** laukelis yra nustatytas *Gautas*.

    - **Klasteris galioja kaip valdanti licencijos plokštelė:** *Ne*

        Jei ši parinktis nustatyta į *Ne*, tuomet padėjimo žingsnis yra užbaigtas, klasterio ID taps valdančia licencijos plokštele ir visos prekės klasterio ID bus susietos su ta valdančia licencijos plokštele.

1. **Klasterio rūšiavimo** „FastTab“, galite nustatyti atidėjimo rūšiavimo kriterijus. Pasirinkite **Naujas** įrankių juostoje, kad įtrauktumėte eilutę ir tada nustatykite tolesnes vertes:

    - **Sekos numeris:** Priimkite numatytąją vertę.
    - **Laukelio pavadinimas:** *WMSLocationId*

        Šis laukelis nustato laukelį, kurį eilutė turi naudoti kaip rūšiavimo kriterijų.

    - **Rūšiavimas:** *Didėjantis*

        Šis laukelis nurodo, ar rūšiavimas turi būti atliekamas didėjančia ar mažėjančia tvarka.

1. **Klasterio darbo šablono** „FastTab“, pasirinkite **Kitas** įrankių juostoje, kad įtrauktumėte eilutę ir tada nustatykite tolesnes vertes:

    - **Darbo užsakymo tipas:** *Įsigijimo užsakymai*
    - **Darbo šablonas:** *61 PO tiesiognis*

1. Veiksmų juostoje pasirinkite **Įrašyti** ir tada pasirinkite **Redaguoti užklausą**.
1. **Klasterio atidėjimo** teksto laukelyje, **Intervalas** skirtuke pasirinkite **Įtraukti**, kad įtrauktumėte antrą liniją į užklausą. Tuomet atnaujinkite užklausos eilutes kaip rodoma tolesnėje lentelėje.

    | Lentelė | Išvestinė lentelė | Laukas | Kriterijai |
    |---|---|---|---|
    | Darbas | Darbas | Sandėlis | *61* |
    | Darbas | Darbas | Darbo ID | Palikite šį lauką tuščią. |

1. Pasirinkite **Gerai**, kad įrašytumėte užklausą ir uždarytumėte dialogo langą.
1. Veiksmų juostoje pasirinkite **Įrašyti** ir užverkite puslapį.

> [!IMPORTANT]
> Laukeliai klasterio profilyje, kurie pasirodo prigęsę, kai **Sukurti klasterio ID** yra nustatyti į *Taip* yra neprieinami ir nebus laikomi galiojančiais, kai ši funkcija yra naudojama.

### <a name="mobile-device-menu-items"></a>Mobiliojo įrenginio meniu elementai

Du nauji mobiliojo įrenginio meniu prekės yra prieinamos šiai funkcijai. **Gauti ir rūšiuoti klasterį** meniu prekė yra naudojama siekiant rūšiuoti gautą inventorių į atidėjimo klasterį po gavimo. **Klasterio atidėjimo** meniu prekė yra naudojama norint atidėti klasterį po jo priskyrimo.

#### <a name="receive-and-sort-cluster"></a>Gauti ir rūšiuoti klasterį

Sukurkite naują mobiliojo įrenginio meniu prekę inventoriaus gavimui ir rūšiuokite į klasterį. Ši meniu prekė sukurs išorės darbą po to, kai inventorius bus gautas, o tai rodo, kad gautas meniu prekė bus naudojama atidėjimo klasteriams.

> [!NOTE]
> **Gauti ir rūšiuoti klasterį** meniu elementas gali būti naudojamas tolesnėms gavimo meniu prekėms:
>
> - Gaunama pirkimo užsakymo eilutė
> - Gaunama pirkimo užsakymo prekė
> - Krovinio prekės gavimas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Rodinyje **Antrašte**, nustatykite tolesnes vertes:

    - **Meniu prekės pavadinimas:** *Gauti ir rūšiuoti klasterį*
    - **Pavadinimas:** *Gauti ir rūšiuoti klasterį*
    - **Režimas:** *Darbas*
    - **Naudoti sukurtą darbą:** *Ne*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Darbo sukūrimo procesas:** *Įsigijimo užsakymo prekės gavimas*
    - **Generuoti numerio lentelę:** *Taip*
    - **Priskirkite atidėjimo klasterį:** *Taip*

        > [!NOTE]
        > **Priskyrimo atidėjimo klasterio** parinktis yra prieinama tik vienam žingsniui *Darbo sukūrimo proceso* veiklai gavimui.

    Priimkite nustatytąsias vertes likusiems laukeliams.

1. Veiksmų srityje pasirinkite **Įrašyti**.

#### <a name="cluster-putaway"></a>Klasterio atidėjimas

Sukurkite naują mobiliojo įrenginio meniu prekę klasterio atidėjimui po jo priskyrimo.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Rodinyje **Antrašte**, nustatykite tolesnes vertes:

    - **Meniu prekės pavadinimas:** *Klasterio atidėjimo funkcija*
    - **Pavadinimas:** *Klasterio atidėjimas*
    - **Režimas:** *Darbas*
    - **Naudoti esamą darbą:** *Taip*

1. **Bendrų**„ FastTab“, nustatykite **Valdomas** laukelis į *Klasterio atidėjimą*. Priimkite nustatytąsias vertes likusiems laukeliams.
1. **Darbo klasės** „FastTab“, nustatykite galiojančią darbo klasę šiai mobiliojo įrenginio meniu prekei:

    - **Darbo klasės ID:** *Įsigijimas*
    - **Darbo užsakymo tipas:** *Įsigijimo užsakymai*

1. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="mobile-device-menu"></a>Mobiliojo įrenginio meniu

Įtraukite meniu prekes, kurias kątik sukūrėte įvesties meniu mobiliojoje programoje.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Meniu sąraše pasirinkite **Įvestis**.
1. **Prieinami meniu ir meniu prekių** sąraše suraskite ir pasirinkite **Gauti ir rūšiuoti klasterį**.
1. Pasirinkite dešinės rodyklės mygtuką, kad pasirinktumėte meniu prekę į **Menius struktūros** sąrašą.
1. Naudokite rodyklės aukštyn ir žemyn mygtuką, kad perkeltumėte meniu prekę į norimą padėtį meniu.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Pakartokite žingsnius nuo 4 iki 7, kad įtrauktumėte likusias meniu prekes:

    - Priskirkite klasterį
    - Klasterio atidėjimas

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Šis scenarijus atkartoja atidėjimo klasterio apdorojimą.

### <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

1. Eikite į **Mokėtinos sumos \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pirkimo užsakymą** nustatykite šias vertes:

    - **Tiekėjo paskyra:** *1001*
    - **Sandėlis:** *61*

1. Pasirinkite **Gerai**.

    **Visi pirkimo užsakymai** puslapis pasirodo.

1. Puslapyje **Visi pirkimo užsakymai**, **Pirkimo užsakymo eilutės** „FastTab“, naudokite **Įtraukti eilutę** mygtuką, kad įtrauktumėte tolesnes eilutes:

    - Pirkimo užsakymo eilutė 1:

        - **Prekės numeris:** *A0001*
        - **Kiekis:** *10*

    - Pirkimo užsakymo eilutė 2:

        - **Prekės numeris:** *A0002*
        - **Kiekis:** *20*

    - Pirkimo užsakymo eilutė 3:

        - **Prekės numeris:** *M9215*
        - **Kiekis:** *30*

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Pasižymėkite pirkimo užsakymo numerį.

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a>Gaukite inventorių ir atidėkite iš mobiliojo įrenginio

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a>Gaukite ir rūšiuokite inventorių į klasterį

1. Prisijunkite prie sandėlio valdymo mobiliųjų įrenginių programėlės kaip vartotojas, nustatytas *61 sandėliui*.
1. Pagrindiniame meniu pasirinkite **Įvestis**.
1. Meniu **Įvestis** rinkitės **Gauti ir rūšiuoti klasterį**.
1. Laukelyje **Ponum** įveskite pirkimo užsakymo numerį.
1. Rinkitės **GERAI** (pažymėkite žymimą mygtuką).
1. Rinkitės **Prekės** laukelį ir įveskite numerį *A0001* ir tada rinkitės **GERAI**.
1. Pasirinkite **Qty** laukelį ir įveskite *10* naudodami skaičių klaviatūra ir tada rinkitės pažymėti mygtuką.
1. Užduoties puslapyje **Kiekis** rinkitės **Gerai** (pažymėkite mygtuką), kad patvirtintumėte įvestą kiekį.
1. Užduoties puslapyje **Prekė** rinkitės **Gerai** kad patvirtintumėte prekę *A0001*, kuri buvo įvesta.
1. Rinkitės **Klasterio ID** laukelį ir įveskite vertę, kad priskirtumėte ID klasteriui, kurį sukūrėte.

    Jūsų įvestas ID čia bus naudojamas, kai dvi likusios prekės pirkimo užsakyme bus gautos.

1. Pasirinkite **Gerai**.

    **Ponum** užduoties puslapis pasirodo ir rodo „Darbas baigtas“ pranešimą.

    Prekė *A0001* dabar buvo gauta į *RECV* vietą ir priskirta klasterio ID, kurį įvedėte žingsnyje 10.

1. Pakartokite žingsnius nuo 4 iki 11, kad gautumėte likusias dvi prekes iš pirkimo užsakymo ir priskirtumėte jas klasterio ID:

    - Kiekis *20* prekei *A0002*
    - Kiekis *30* prekei *M9215*

#### <a name="close-the-cluster"></a>Užverkite klasterį

Prieš tai, kai prekės klasteryje gali būti atidėtos, klasterį reikia užverti.

1. „Supply Chain Management“ eiktie į **Sandėlio valdymas \> Darbas \> Išvestis \> Darbo klasteriai**.
1. Puslapyje **Darbo klasteriai** skyriuje **Darbo klasteris** ieškokite **Klasterio ID** laukelio klasterio ID, kurį įvedėte anksčiau.
1. Jei klsateris nerodomas, jis jau gali būti užvertas. Norėdami nustatyti, ar klasteris užvertas, pasirinkite **Rodyti užvėrimo darbą** žymimą laukelį ir ieškokite klasterio ID, kurį įvedėte anksčiau. Tuomet atlikite vieną iš toliau nurodytų veiksmų.

    - Jei klasteris buvo užvertas, praleiskite likusius šios procedūros žingsnius ir judėkite toliau prie kitos procedūros, [Klasterio atidėjimas](#put-the-cluster-away).
    - Jei klasteris nebuvo užvertas, atlikite likusius šios procedūros žingsnius, kad rankinu būdu užvertumėte klasterį. Tuomet judėkite prie kitos procedūros.

1. Skyriuje **Darbo klasteris** pasirinkite klasterio ID, kurį įvedėte anksčiau.
1. Veiksmų juosoje rinkitės **Užverti klasterį**.

    Po to, kai klasteris buvo užvertas, jis neberodomas **Darbo klasteris** skyriuje (nebent **Rodyti užvertą darbą** žymimas laukelis pasirinktas).

#### <a name="put-the-cluster-away"></a>Klasterio atidėjimas

1. Prisijunkite prie sandėlio valdymo mobiliųjų įrenginių programėlės kaip vartotojas, nustatytas *61 sandėliui*.
1. Pagrindiniame meniu pasirinkite **Įvestis**.
1. Meniu **įvestis** rinkitės **Klasterio atidėjimas**.
1. Rinkitės **Klasterio ID** ir įveskite klasterio ID, kurį įvedėte anksčiau užvertam klasteriui.
1. Pasirinkite **Gerai**.

    **Klasterio atidėjimas: Paėmimas** puslapis pasirodo. Jis rodo klasterio ID, paėmimo vietą, prekes (vertė *Keletas* bus rodoma) ir bendras kiekis klasteryje, kurį reikia paimti.

1. Pasirinkite **Gerai**.

    **Klasterio atidėjimas: Padėjimas** puslapis pasirodo. **padėjimo** instrukcijos nustato klasterio ID, padėjimo vietą, prekes, bendrą kiekį ir licencijos lentelės ID prekėms, kurios buvo gautos klasteryje.

    Turite standartines parinktis, kurios viršys arba praleis šį žingsnį.

    ![Klasterio atidėjimas: Padėjimo puslapis.](media/Cluster_putaway-Put.png "Klasterio atidėjimas: Padėjimo puslapis")

1. Rinkitės **GERAI**, kad patvirtintumėte klasterio atidėjimą.

    Rodomas pranešimas „Klasteris baigtas“.

## <a name="notes-and-tips"></a>Pastabos ir patarimai

Dėl atvejų, kai klasterio ID tampa valdančia licencijos plokštele pakrautam padėklui, padėjimo padėtis automatiškai suteikiama, kai nuskaitomas atitinkamas klasterio ID. Negalima nuskaityti jokios tolesnės licencijos plokštelės, net jei licencijos plokštelės sukūrimas nustatytas į rankinį.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
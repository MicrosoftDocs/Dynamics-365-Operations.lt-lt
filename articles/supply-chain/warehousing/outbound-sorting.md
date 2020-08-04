---
title: Siunčiamas rūšiavimas
description: Šiame skyriuje pateikta informacija apie siunčiamą rūšiavimą. Ši funkcija padeda paprasčiau tvarkyti mažas talpyklas ir sandėlio darbuotojams geriau susiplanuoti ir suorganizuoti padėklų talpą sunkvežimyje.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e72249e26fb8f291f804cf5f2e4ce98bf88cd5bf
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596256"
---
# <a name="outbound-sorting"></a>Siunčiamas rūšiavimas

[!include [banner](../includes/banner.md)]

Ši funkcija padeda paprasčiau tvarkyti mažas talpyklas ir sandėlio darbuotojams geriau susiplanuoti ir suorganizuoti padėklų talpą sunkvežimyje. Naudodami siunčiamą rūšiavimą galite rūšiuoti supakuotas talpyklas ant tinkamo padėklo po to, kai jie palieka pakavimo stotį. Taip pat galite pastatyti pakavimo hierarchiją.

Ši funkcija leidžia sustatyti padėklus iš talpyklių, kurie yra supakuoti naudojant pakavimo funkciją. Talpykla nėra siunčiama į galutinę siuntimo vietą taip kaip tai daroma originaliame pakavimo sraute. Šiuo atveju darbuotojai gali uždaryti talpyklą ir patraukti ją į rūšiavimo tipo vietą. Jie gali rūšiuoti talpyklas į padėtis, kurių kiekviena turi licencijos numerį (LP). Po talpyklų rūšiavimo, galima sukurti užduotį, kuri bus siunčiama visą LP į galutinį siuntimo uostą ar tarpinę vietą pagal vietos instrukcijas ar jūsų pačių reikalavimus. Taip pat, rūšiavimo vietos uždarymo veiksmas gali nedelsiant pergabinti inventorių į galutinę siuntimo vietą ir paimti jį į užsakymą.

## <a name="turn-on-the-outbound-sorting-feature"></a>Įjunkite Siunčiamo rūšiavimo funkciją

Prieš naudodami šią funkciją, turite ją įjungti savo sistemoje. Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Siunčiamas rūšiavimas*

## <a name="setup"></a>Sąranka

Dėl šio scenarijaus, privalote naudoti standartinius **USMF** demo duomenis ir *62* sandėlį. Taip pat privalote užbaigti sąranką, kuri aprašyta tolesniuose skirsniuose.

### <a name="set-up-a-wave-template"></a>Bangos šablono nustatymas

Ši sąranka automatiškai apdoroja bangą ir sukuria darbą, kai sandėliui yra išduodama linija.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
1. Šabloniniame sąraše pasirinkite**Sandėlis 62**.
1. „FastTab“ **Bendra** įsitikinkite, kad **Bangos apdorojimas išleidžiant į sandėlį** parinktis yra nustatyta ties *Taip* padėtimi.

### <a name="set-up-a-worker"></a>Nustatykite darbuotoją

Pakavimo stotis yra laikoma vieta. Sandėlio darbuotojai, pasirašantys pakavimo stotyje, mato ir dirba tik su siuntimais ir talpyklomis suplanuotomis specifinėje pakavimo vietoje. Vartotojas prisijungęs prie „Microsoft Dynamics 365“ turi būti nustatytas kaip Sandėlio tvarkymo darbuotojas. Jei vartotojo vardas nepasirodo užduoties vartotojų sąraše, laikykitės šios procedūros jo pridėjimui.

> [!NOTE]
> Šiais žingsniais laikoma, kad vartotojas jau yra sistemoje ir buvo susietas kaip darbuotojas ar darbininkas **Žmogiškųjų išteklių** modulyje.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Darbuotojai**.
1. Pasirinkite **Naujas**.
1. **Darbuotojo** laukelyje pasirinkite paskirties vartotoją darbuotojų sąraše.
1. Pasirinkite **Pasirinkti**.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. **Vartotojų** gretajame skirtuke pasirinkite **Naujas** tam, kad sukurtumėte mobilaus prietaiso paskyrą ir nustatykite jai šias vertes:

    - **Vartotojo identifikavimo numeris** Įveskite unikalų identifikavimo numerį.
    - **Vartotojo vardas:** Įveskite vardą identifikavimo numeriui.
    - **Nustatytasis sandėlis:** *62*
    - **Meniu pavadinimas:** *Pagrindinis*

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Pasirodo**Slaptažodžio nustatymas** teksto laukelis, kuriame galit sukurti paprastą slaptažodį, kurį vartotojas galės naudoti prisijungdamas prie mobilios programos. Nustatykite toliau nurodytas reikšmes.

    - **Slaptažodis:** Įveskite paprastą slaptažodį.
    - **Patvirtinti slaptažodį:** Įveskite tą patį slaptažodį dar kartą.

1. Pasirinkite **Nustatyti slaptažodį**.

    Pranešimas Veiksmų centre jus informuos, kad slaptažodis buvo nustatytas jūsų sukurtam vartotojui.

### <a name="create-a-location-type"></a>Sukurkite vietos tipą

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos tipai**.
1. Veiksmų juostoje pasirinkite **Naujas** vietos tipo sukūrimui ir nustatykite jam šias vertes:

    - **Vietos tipas:** *RŪŠIUOTI*
    - **Aprašas:** *Rūšiuoti*

1. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="set-up-warehouse-management-parameters"></a>Nustatykite Sandėlio tvarkymo parametrus

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. **Pagrindiniame** skirtuke **Vietos tipai** „FastTab“ nustatykite **Vietos tipo rūšiavimo** laukelį į *RŪŠIUOTI* padėtį.
1. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="set-up-a-location-profile"></a>Nustatykite vietos profilį

1. Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlys \> Vietos profiliai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Antraštėje nustatykite šias vertes:

    - **Vietos profilio identifikavimo numeris:** *Rūšiavimas*
    - **Pavadinimas:** *Rūšiavimas*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Vietos formatas:** *ASRB* (Aisle-Rack-Shelf-Bin)
    - **Vietos tipas:** *RŪŠIUOTI*
    - **Naudoti licencijos numerio sekimą:** *Taip*
    - **Leisti maišytus elementus:** *Taip* (Kai nustatote šią parinktį į *Taip* padėtį, **Leisti maišyto inventoriaus paketus** parinktis automatiškai nustatoma į *Taip* padėtį ir nebegali būti keičiama nepriklausomai.)

1. Pasirinkite **Įrašyti**.

### <a name="set-up-a-location"></a>Nustatykite vietą

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos**.
1. Antraštėje išvalykite **Kurti patikrinimo skaičius vietai** žymimą laukelį.
1. Veiksmų juostoje pasirinkite **Naujas** vietos tipo sukūrimui ir nustatykite jam šias vertes:

    - **Sandėlis:** *62*
    - **Vieta:** *SORT*
    - **Vietos profilio identifikavimo numeris:** *SORTING*

1. Pasirinkite **Įrašyti**.

### <a name="set-up-an-outbound-sorting-template"></a>Nustatykite siunčiamo rūšiavimo šabloną

Siunčiamo rūšiavimo šablonas nustato, ar veiksmas yra sukuriamas vietos rūšiavimu sukurtas, ar rūšiavimas atliekamas rankiniu būdu, ar automatiškai.

Esant šiam scenarijui, sukursite siunčiamo rūšiavimo šabloną tam, kad sukurtumėte padėklus po pakavimo stoties.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Pakavimas \> Siunčiamo rūšiavimo šablonas**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujojo šablono antraštėje nustatykite šias vertes:

    - **Siunčiamo rūšiavimo šablono identifikavimo kodas:** *Automatinis veiksmas*
    - **Aprašas:** *Automatinio veiksmo sukūrimas*
    - **Siunčiamo rūšiavimo šablono identifikavimo tipas:** *Talpykla*
    - **Sandėlis:** *62*
    - **Vieta:** *SORT*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Rūšiavimo patvirtinimas:** *Padėties nuskaitymas*
    - **Sukurkite veiksmą vietos uždaryme:** *Taip*

        Jei ši parinktis nustatyta *Taip*, vietos uždarymo metu, veiksmas bus sukuriamas inventoriaus nugabenimui į galutinę siuntimo vietą. Jei ši parinktis nustatyta *Ne*, inventorius bus nedelsiant paimtas į užsakymą, kai padėtis bus uždaryta.

    - **Padėties priskyrimas:** *Automatinis*

        Jei šis laukelis nustatytas į *Rankinį*, vartotojas privalo visuomet nurodyti padėtį, kurioje inventorius turi būti rūšiuojamas. Jei jis nustatytas į *Automatinį*, sistema automatiškai ves inventorių į bet kurią jai prieinamą padėtį pagal rūšiavimo šablono pertrūkius.

1. Pasirinkite **Išsaugoti** tam, kad **Redaguoti užklausą** mygtuką pastatytumėte į Veiksmų juostą.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Užklausos tvartyklėje, **Rūšiavimas** skirtuke įtraukite liniją su šiomis vertėmis:

    - **Lentelė:** *Siuntos*
    - **Išvestinė lentelė:** *Siuntos*
    - **Laukas:** *Vežėjo paslauga*

        Kai pasirenkate šią vertę, galite gauti šį pranešimą: „Laukelio vežėjo paslaugos nėra indekso laukelis. Ar norite įtraukti rūšiavimą?“ Pasirinkite **Taip**.

    - **Paieškos kryptis:** *Didėjanti*

1. Pasirinkite **Gerai**.
1. Galite gauti šį pranešimą: „Grupavimas bus perkrautas, ar tęsti?“ Pasirinkite **Taip**.

    **Siunčiamo rūšiavimo šablono pertrūkio** mygtukas pasirodo veiksmų juostoje.

1. Veiksmų juostoje pasirinkite **Siunčiamo rūšiavimo šablono pertrūkiai**.
1. **Siunčiamo rūšiavimo kriterijų** teksto laukelyje, nustatykite šias vertes:

    - **Referencinės lentelės pavadinimas:** *Siuntimai*
    - **Referencinis laukelio pavadinimas:** *Vežėjo paslaugos*
    - **Grupavimas laukeliais:** Pasirinkite šį žymimą laukelį tam, kad sugrupuotumėte siuntimo pagal vežėjo paslaugas.

1. Norėdami įrašyti parametrus ir uždaryti dialogo langą, pasirinkite **Gerai**.

### <a name="set-up-container-packing-policies"></a>Nustatykite konteinerio pakavimo politiką

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Talpyklos \> Talpyklos rūšiavimo politika**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujosios politikos antraštėje, nustatykite šias vertes:

    - **Konteinerio pakavimo politika:** *Rūšiuoti*
    - **Aprašas:** *Rūšiuoti*

1. **Peržiūros** „FastTab“, nustatykite šias vertes:

    - **Sandėlis:** *62*
    - **Nustatytoji vieta rūšiavimui:** *SORT*
    - **Svorio vienetas:** *kg*
    - **Talpyklos uždarymo politika:** *Automatinis išleidimas*
    - **Talpyklos išleidimo politika:** *Priskirti talpyklą prie siunčiamo rūšiavimo padėties*

1. Pasirinkite **Įrašyti**.

### <a name="set-up-packing-profiles"></a>Pakavimo profilių nustatymas

Sukurkite naują pakavimo profilį, kuris bus naudojamas kartu su rūšiavimo funkcija.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Pakavimas \> Pakavimo profiliai**.
1. Veiksmų juostoje pasirinkite **Naujas** linijos sukūrimui ir nustatykite jam šias vertes:

    - **Pakavimo profilio identifikavimo numeris:** *Rūšiuoti*
    - **Aprašas:** *Rūšiuoti*
    - **Konteinerio pakavimo politika:** *Rūšiuoti*
    - **Talpyklos identifikavimo numerio režimas:** *Automatinis*
    - **Talpyklos tipas:** *Plati dėžė*
    - **Automatinis talpyklos sukūrimas jam esant uždarytam:** Išvalyta (= *Ne*)

1. Pasirinkite **Įrašyti**.

### <a name="set-up-work-classes"></a>Darbo klasių nustatymas

Nustatykite darbo klasę, kuri bus naudojama kartu su rūšiavimu.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.
1. Veiksmų juostoje pasirinkite **Naujas** rūšiavimo darbo klasės sukūrimui ir nustatykite jam šias vertes:

    - **Darbo klasės identifikavimo numeris:** *Rūšiuoti*
    - **Aprašas:** *Rūšiuoti*
    - **Darbo tvarkos tipas:** *Rūšiuoto inventoriaus paėmimas*

1. Pasirinkite **Įrašyti**.

### <a name="set-up-mobile-device-menu-items"></a>Nustatykite mobilaus prietaiso meniu elementus

#### <a name="set-up-a-new-pallet-menu-item"></a>Nustatykite naujo padėklo meniu elementus

Sukurkite mobilaus prietaiso meniu elementus padėklų rūšiavimo metu sukūrimui.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Antraštėje nustatykite šias vertes:

    - **Meniu elemento pavadinimas:** *Padėklo sukūrimas*
    - **Pavadinimas:** *Padėklo sukūrimas*
    - **Režimas:** *Netiesioginis*
    - **Naudoti sukurtą darbą:** *Ne*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Veiksmo kodas:** *Siunčiamas rūšiavimas*

        Kai laukelis nustatytas į *Siunčiamą rūšiavimą*, rodomas **Siunčiamo rūšiavimo šablono identifikavimo kodo** laukelis.

    - **Naudoti proceso gidą:** *Taip*

        Kai **Veiksmo kodo** laukelis yra nustatytas į *Siunčiamą rūšiavimą*, ši parinktis automatiškai nustatoma į *Taip*.

    - **Siunčiamo rūšiavimo šablono identifikavimo kodas:** *Automatinis veiksmas*

1. Pasirinkite **Įrašyti**.

#### <a name="set-up-a-new-loading-menu-item"></a>Nustatykite naujo krovimo meniu elementus

Po to, sukurkite meniu elementą leidžiantį vartotojams judinti rūšiuotus inventoriaus elementus į gabenimo vietą.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Antraštėje nustatykite šias vertes:

    - **Meniu elemento pavadinimas:** *Krauti iš Rūšiavimo*
    - **Pavadinimas:** *Krauti iš Rūšiavimo*
    - **Režimas:** *Darbas*
    - **Naudoti esantį darbą:** *Taip*

1. **Bendra** „FastTab“, nustatykite **Valdoma** laukelį į *Valdoma vartotojo*.
1. **Darbo klasių** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes:

    - **Darbo klasės identifikavimo numeris:** *SORT*
    - **Darbo tvarkos tipas:** *Rūšiuoto inventoriaus paėmimas*

1. Pasirinkite **Įrašyti**.

### <a name="set-up-the-mobile-device-menu"></a>Nustatykite mobilaus prietaiso meniu

Privalote dabar pridėti naujus meniu elementus į mobilaus prietaiso meniu.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
1. Pasirinkite **Siunčiama** meniu.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. **Esančiuose meniu ir meniu elementų** stulpelyje, suraskite ir pasirinkite **Padėklo kūrimas**.
1. Pasirinkite dešinės rodyklės mygtuką **Padėklo kūrimo** judinimui į **Meniu struktūros** stulpelį.
1. Naudokite viršutinės ir apatinės rodyklės mygtukus **Padėklo kūrimo** meniu elementui padėti į norimą padėtį mobilaus prietaiso meniu.
1. Pasirinkite **Įrašyti**.
1. Pakartokite šią procedūrą **Krauti iš rūšiavimo** meniu elemento įtraukimui į **Siuntimo** meniu.

### <a name="set-up-location-directives"></a>Nustatyti vietos nurodymus

*Vietos direktyvos* yra taisyklės padedančios identifikuoti paėmimo ir padėjimo vietas inventoriaus judėjime. Dabar privalote sukurti taisyklę rūšiavimo veiksmo valdymui.

#### <a name="set-up-a-single-sku-directive"></a>Nustatykite vieną SKU direktyvą

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Kairėje jusotoje pakeiskite **Darbo tvarkos tipo**laukelio vertę į *Rūšiuoto inventoriaus paėmimas*.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Antraštėje nustatykite šias vertes:

    - **Seka:** *1*
    - **Pavadinimas:** *Baydoor*

1. **Padėties direktyvos** „FastTab“, nustatykite šias vertes:

    - **Darbo tipas:** *Padėjimas*
    - **Vieta:** *6*
    - **Sandėlis:** *62*
    - **Keletas SKU:** *Ne*

1. Pasirinkite **Įrašyti** įrankių juostai padėti į **Linijos** „FastTab“.
1. **Linijos** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes naujoje linijoje. Priimkite nustatytąsias vertes visiems kitiems laukeliams.

    - **Seka:** *1*
    - **Iš:** *0*
    - **Į:** *1 000 000*

1. Pasirinkite **Įrašyti** įrankių juostai padėti į **Vietos direktyvos veiksmai** „FastTab“.
1. **Vietos direktyvos veiksmai** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes naujoje linijoje. Priimkite nustatytąsias vertes visiems kitiems laukeliams.

    - **Seka:** *1*
    - **Pavadinimas:** *Baydoor*

1. Pasirinkite **Įrašyti**.
1. „FastTab“ **Vietos nurodymų veiksmai** pasirinkite **Redaguoti užklausą**.
1. Užklausos tvarkyklėje, **Intervalas** skirtuke, suraskite eilutę, kurioje **Laukelis** laukelis yra nustatytas į *Vieta*. Nustatykite **Kriterijų** laukelį šiai eilutei į *Baydoor*.
1. Pasirinkite **OK** tam, kad įrašytumėte savo nustatymus uždarytumėte užklausos tvarkyklę.

#### <a name="set-up-a-multiple-sku-directive"></a>Nustatykite kelių SKU direktyvų

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Kairėje jusotoje pakeiskite **Darbo tvarkos tipo**laukelio vertę į *Rūšiuoto inventoriaus paėmimas*.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Antraštėje nustatykite šias vertes:

    - **Seka:** *2*
    - **Pavadinimas:** *Baydoor Multi*

1. **Padėties direktyvos** „FastTab“, nustatykite šias vertes:

    - **Darbo tipas:** *Padėjimas*
    - **Vieta:** *6*
    - **Sandėlis:** *62*
    - **Keletas SKU:** *Taip*

1. Pasirinkite **Įrašyti** įrankių juostai padėti į **Linijos** „FastTab“.
1. **Linijos** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes naujoje linijoje. Priimkite nustatytąsias vertes visiems kitiems laukeliams.

    - **Seka:** *1*
    - **Iš:** *0*
    - **Į:** *1 000 000*

1. Pasirinkite **Įrašyti** įrankių juostai padėti į **Vietos direktyvos veiksmai** „FastTab“.
1. **Vietos direktyvos veiksmai** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes naujoje linijoje. Priimkite nustatytąsias vertes visiems kitiems laukeliams.

    - **Seka:** *1*
    - **Pavadinimas:** *Baydoor Multi*

1. Pasirinkite **Įrašyti**.
1. „FastTab“ **Vietos nurodymų veiksmai** pasirinkite **Redaguoti užklausą**.
1. Užklausos tvarkyklėje, **Intervalas** skirtuke, suraskite eilutę, kurioje **Laukelis** laukelis yra nustatytas į *Vieta*. Nustatykite **Kriterijų** laukelį šiai eilutei į *Baydoor*.
1. Pasirinkite **OK** tam, kad įrašytumėte savo nustatymus uždarytumėte užklausos tvarkyklę.

### <a name="set-up-work-templates"></a>Nustatyti darbo šablonus

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Pakeiskite **Darbo tvarkos tipo**laukelio vertę į *Rūšiuoto inventoriaus paėmimas*.
1. Veiksmų juostoje pasirinkite **Naujas** tam, kad sukurtumėte darbo šabloną.
1. **Peržiūros** skirtuke, nustatykite šias vertes:

    - **Seka:** *1*
    - **Darbo šablonas:** *Rūšiuoti*
    - **Darbo šablono aprašas:** *Rūšiuoti*

1. Pasirinkite **Įrašyti,** kad būtų galima naudoti **Darbo šablono išsami informacija** „FastTab“ skirtuką.
1. **Darbo šablono informacija** „FastTab“ pasirinkite **Naujas** tam, kad pridėtumėte liniją ir tuomet nustatykite šias vertes:

    - **Darbo tipas:** *Paėmimas*
    - **Darbo klasės identifikavimo numeris:** *SORT*

1. Pasirinkite **Naujas** dar kartą, kad pridėtumėte antrą liniją ir tuomet nustatykite jai šias vertes:

    - **Darbo tipas:** *Padėjimas*
    - **Darbo klasės identifikavimo numeris:** *SORT*

1. Pasirinkite **Įrašyti**.

## <a name="scenario"></a>Scenarijus

Scenarijus simuliuoja situaciją, kai paimtos talpyklos turėtų automatiškai būti rūšiuojamos į skirtingas padėtis (padėklus) po pakavimo stoties priklausomai nuo siuntimo vežėjo paslaugos. Po to, kai visi elementai iš pakrovimo yra supakuoti ir rūšiuoti pagal adresą, padėklai bus patraukti į „bay door“.

### <a name="create-sales-orders-and-picking-work"></a>Sukurkite prekybos užsakymus ir paėmimo tvarką

#### <a name="create-sales-order-1"></a>Pardavimo užsakymo 1 sukūrimas

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-005*
    - **Sandėlis:** *62*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

    Naujas pardavimo užsakymas yra atidarytas.

1. Perjunkite **Antraštės** rodinį.
1. „FastTab“ skirtuko **Pristatymas** dalyje **Transportavimas**, nustatykite šias vertes:

    - **Siuntos vežėjas:** *Oro transportas*
    - **Vežėjo paslauga:** *oro*

1. Perjunkite į **Linijų** peržiūrą.
1. Jei nauja, tuščia linija nėra automatiškai įtraukta į tinklelį **Prekybos užsakymo linijų** „FastTab“, vienos linijos įtraukimui pasirinkite **Įtraukti liniją**.
1. Naujo užsakymo linijoje nustatykite šias vertes:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *2*

1. Kai naujo užsakymo linija dar yra pasirinkta **Prekybos užsakymo linijoje** „FastTab“, **Inventoriaus** meniu virš tinklelio, pasirinkite **Rezervavimas**.
1. **Rezervavimo** puslapyje, pasirinkite **Rezervuoti vietą** viso pasirinktos linijos sandėlyje kiekio rezervavimui.
1. Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.
1. Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.
1. Gausite informacinį pranešimą apie užsakymo siuntimą ir bangą. Užrašykite bangos identifikavimo kodo pastabą ir siuntimo identifikavimo numerius.

#### <a name="sales-order-2"></a>Pardavimo užsakymas 2

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-006*
    - **Sandėlis:** *62*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.
1. Naujas pardavimo užsakymas yra atidarytas. Jame turi būti nauja tuščia eilutė, esanti **Pardavimo užsakymo eilutės** „FastTab” skirtuko tinklelyje. Nustatykite šias vertes užsakymo linijoje:

    - **Prekė:** *A0001*
    - **Kiekis:** *1*

1. **Linijos informacijoje** „FastTab“, **Pristatymo** skirtuke, nustatykite **Pristatymo būdo** laukelį į *Flowe-STD*.
1. **Prekybos užsakymo linijos** „FastTab“, pasirinkite **Įtraukti liniją** ir tuomet nustatykite tolesnes vertes antrojo užsakymo linijoje:

    - **Prekė:** *A0002*
    - **Kiekis:** *1*

1. **Linijos informacijoje** „FastTab“, **Pristatymo** skirtuke, pakeiskite **Pristatymo būdo** laukelio vertę į *Air C-Air*.
1. **Prekybos užsakymo linijos** „FastTab“, pasirinkite pirmojo užsakymo liniją. Vėliau,**Inventorius** meniu virš tinklelio, pasirinkite **Rezervavimas**.
1. **Rezervavimo** puslapyje, pasirinkite **Rezervuoti vietą** viso pasirinktos linijos sandėlyje kiekio rezervavimui.
1. Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.
1. **Prekybos užsakymo linijos** „FastTab“, pasirinkite antrojo užsakymo liniją. Vėliau,**Inventorius** meniu virš tinklelio, pasirinkite **Rezervavimas**.
1. **Rezervavimo** puslapyje, pasirinkite **Rezervuoti vietą** viso pasirinktos linijos sandėlyje kiekio rezervavimui.
1. Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.
1. Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.
1. Gausite informacinį pranešimą apie užsakymo siuntimą ir bangą. Atkreipkite dėmesį, kad dviejų bangų identifikavimo numeriai ir du siuntimo identifikavimo numeriai buvo sukurti, kiekvienas iš jų teko pristatymo būdui prekybos užsakymo linijose.

#### <a name="get-the-work-ids-from-the-work-details"></a>Gaukite darbo identifikavimo numerį iš darbo informacijos

1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.
1. Puslapis rodo darbo identifikavimo numerį, kuris buvo sukurtas iš prekybos užsakymų. Naudokite bangos ir siuntimo identifikavimo numerius prekybos užsakymams, kuriuos kursite tam, kad surastumėte darbo identifikavimo numerį kiekvienai bangai ir siuntimui. Pažymėkite šiuos darbo identifikavimo numerius, nes jums jų reikės kituose žingsniuose. Atkreipkite dėmesį, kad du darbo identifikavimo numeriai buvo sukurti antrajam prekybos užsakymui. Jei paimami skirtingi elementai iš skirtingų vietų, sukuriamas atskiras žodžių identifikavimo numeris.

### <a name="pick-items-for-the-sales-orders"></a>Paėmimo elementai prekybos užsakymui

Užbaigite sukurtą darbą naudodami mobilų prietaisą, kuriuo perkelsite elementus į pakavimo stotį.

1. Mobiliame prietaise prisijunkite prie *62* sandėlio naudodami vartotojo identifikavimo kodą, kurį sukūrėte šiam scenarijui (arba esančių demo duomenų vartotojo identifikavimo kodą).
1. Pagrindiniame meniu pasirinkite **Siunčiama**.
1. **Siunčiama** meniu pasirinkite **Prekybos paėmimas**.
1. **identifikavimo kodo** laukelyje įveskite darbo identifikavimo kodą, kuris buvo sukurtas prekybos užsakymui 1.
1. Pasirinkite **Gerai**.
1. **Prekybos užsakymai - Paėmimas** puslapyje įveskite paskirties LP, kuris buvo sukurtas prekybos užsakymui 1. Atkreipkite dėmesį, kad yra rodoma paėmimo vieta (*bulk-001*), elementas (*A0001*) ir kokybė (*2 vnt.*).
1. Pasirinkite **Gerai**.
1. Peržiūrėkite informaciją **Prekybos užsakymai - Paėmimas** puslapyje. **Loc** laukelis turi rodyti, kad paimti elementai bus *Pakavimo* vietoje.
1. Pasirinkite **Gerai**.

    **Nuskaityti darbo / licencijos numerio identifikavimo kodą** puslapyje gausite „Darbas baigtas“ pranešimą, kuris rodo, jog darbo identifikavimo kodas ir prekybos užsakymas 1 buvo užbaigti.

    Dabar paimsite prekybos užsakymą 2.

1. **identifikavimo kodo** laukelyje įveskite darbo identifikavimo kodą, kuris buvo sukurtas prekybos užsakymui 2, kuriame linija 1 turi elementą *A0001*.
1. Pasirinkite **Gerai**.
1. **Prekybos užsakymai - Paėmimas** puslapyje įveskite paskirties LP. Atkreipkite dėmesį, kad yra rodoma paėmimo vieta (*bulk-001*), elementas (*A0001*) ir kokybė (*1 vnt.*).
1. Pasirinkite **Gerai**.
1. Peržiūrėkite informaciją **Prekybos užsakymai - Paėmimas** puslapyje. **Loc** laukelis turi rodyti, kad paimti elementai bus *Pakavimo* vietoje.
1. Pasirinkite **Gerai**.

    **Darbo / licencijos numerio identifikavimo kodo nuskaitymo** puslapyje jums bus parodytas pranešimas „Darbas baigtas“. Šis pranešimas rodo, kad darbo identifikavimo kodas 2 prekybos užsakymo 1 linijoje buvo užbaigtas.

1. **identifikavimo kodo** laukelyje įveskite darbo identifikavimo kodą, kuris buvo sukurtas prekybos užsakymui 2, kuriame linija 2 turi elementą *A0002*.
1. Pasirinkite **Gerai**.
1. **Prekybos užsakymai - Paėmimas** puslapyje įveskite paskirties LP. Atkreipkite dėmesį, kad yra rodoma paėmimo vieta (*bulk-002*), elementas (*A0001*) ir kokybė (*1 vnt.*).
1. Pasirinkite **Gerai**.
1. Peržiūrėkite informaciją **Prekybos užsakymai - Paėmimas** puslapyje. **Loc** laukelis turi rodyti, kad paimti elementai bus *Pakavimo* vietoje.
1. Pasirinkite **Gerai**.

    **Darbo / licencijos numerio identifikavimo kodo nuskaitymo** puslapyje jums bus parodytas pranešimas „Darbas baigtas“. Šis pranešimas rodo, kad darbo identifikavimo kodas 2 prekybos užsakymo 2 linijoje buvo užbaigtas.

### <a name="pack-sales-orders-into-containers"></a>Prekybos užsakymų pakavimas į talpyklas

#### <a name="pack-sales-order-1-into-containers"></a>Prekybos užsakymo 1 pakavimas į talpyklas

1. Eikite į **Sandėlio tvarkymas \> Pakavimas ir dėjimas į talpyklas \> Pakavimas**.

    Pasirodo**Pasirinkit pakavimo stotį** teksto laukelis. Pagal nutylėjimą, **Darbuotojo** laukelis turi būti nustatytas į darbuotojo vardą, kurį nustatėte anksčiau.

1. Nustatykite tolesnes vertes tam, kad peržiūrėtumėte ir dirbtumėte su siuntimais ir talpyklomis, kuriuos yra planuojamos konkrečioje pakavimo vietoje:

    - **Vieta:** *6*
    - **Sandėlis:** *62*
    - **Vieta:** *Pakavimas*
    - **Pakavimo profilio identifikavimo numeris:** *Rūšiuoti*

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.
1. **Pakavimo** puslapyje, **Licencijos numeris ar siuntimas** laukelyje įveskite paskirties LP prekybos užsakymui 1. Tuomet pasirinkite **Skirtuką** ar **Įvesties** raktą savo klaviatūroje, kad išeitumėte iš laukelio.
1. Veiksmų juostoje pasirinkite**Naujas talpykla**.
1. Priimkite visus nustatytuosius nustatymus ir pasirinkite **OK**. Užsirašykite talpyklos identifikavimo kodą.
1. **Elemento pakavimo** „FastTab“, nustatykite šias vertes:

    - **Kiekis:** *1*
    - **Identifikavimo kodo:** Elementas *A0001*

1. Veiksmų juostoje pasirinkite**Uždaryti talpyklą**.
1. **Talpyklos uždarymo** teksto laukelyje, pasirinkite **Gauti sistemos svorį**tam, kad sistema atnaujintų **Bendro svorio** laukelį.
1. Pasirinkite **Gerai**. Talpykla turi būti perkelta į *SORT* vietą ir parengta rūšiavimui.
1. Sukurkite antrą talpyklą tam, kad įtrauktumėte antrą elementą iš LP prekybos užsakymo 1 į naują talpyklą.
1. Veiksmų juostoje pasirinkite**Naujas talpykla**.
1. Priimkite visus nustatytuosius nustatymus ir pasirinkite **OK**. Užsirašykite talpyklos identifikavimo kodą.
1. **Elemento pakavimo** „FastTab“, nustatykite šias vertes:

    - **Kiekis:** *1*
    - **Identifikavimo kodo:** Elementas *A0001*

1. Veiksmų juostoje pasirinkite**Uždaryti talpyklą**.
1. **Talpyklos uždarymo** teksto laukelyje, pasirinkite **Gauti sistemos svorį**tam, kad sistema atnaujintų **Bendro svorio** laukelį.
1. Pasirinkite **Gerai**. Talpykla turi būti perkelta į *SORT* vietą ir parengta rūšiavimui.

#### <a name="pack-sales-order-2-into-containers"></a>Prekybos užsakymo 2 pakavimas į talpyklas

1. **Pakavimo** puslapyje, **Licencijos numeris ar siuntimas** laukelyje įveskite paskirties LP prekybos užsakymui 2. Tuomet pasirinkite **Skirtuką** ar **Įvesties** raktą savo klaviatūroje, kad išeitumėte iš laukelio.
1. Veiksmų juostoje pasirinkite**Naujas talpykla**.
1. Priimkite visus nustatytuosius nustatymus ir pasirinkite **OK**. Užsirašykite talpyklos identifikavimo kodą.
1. **Elemento pakavimo** „FastTab“, nustatykite šias vertes:

    - **Kiekis:** *1*
    - **Identifikavimo kodo:** Elementas *A0001*

1. Veiksmų juostoje pasirinkite**Uždaryti talpyklą**.
1. **Talpyklos uždarymo** teksto laukelyje, pasirinkite **Gauti sistemos svorį**tam, kad sistema atnaujintų **Bendro svorio** laukelį.
1. Pasirinkite **Gerai**. Talpykla turi būti perkelta į *SORT* vietą ir parengta rūšiavimui.
1. **Licencijos numeris ar siuntimas** laukelyje įveskite paskirties LP prekybos užsakymui 2. Tuomet pasirinkite **Skirtuką** ar **Įvesties** raktą savo klaviatūroje, kad išeitumėte iš laukelio.
1. Veiksmų juostoje pasirinkite**Naujas talpykla**.
1. Priimkite visus nustatytuosius nustatymus ir pasirinkite **OK**. Užsirašykite talpyklos identifikavimo kodą.
1. **Elemento pakavimo** „FastTab“, nustatykite šias vertes:

    - **Kiekis:** *1*
    - **Identifikavimo laukelis:** Elementas *A0002*

1. Veiksmų juostoje pasirinkite**Uždaryti talpyklą**.
1. **Talpyklos uždarymo** teksto laukelyje, pasirinkite **Gauti sistemos svorį**tam, kad sistema atnaujintų **Bendro svorio** laukelį.
1. Pasirinkite **Gerai**. Talpykla turi būti perkelta į *SORT* vietą ir parengta rūšiavimui.

Talpyklos informacijso peržiūrai, eikite į **Sandėlio valdymas \> Pakavimas ir dėjimas į talpyklas \> Talpyklos** ir ieškokite talpyklos identifikavimo kodo, kuris buvo sukurtas pakavimo metu.

### <a name="sort-the-containers"></a>Rūšiuokite talpyklas

> [!IMPORTANT]
> Patekę į **Padėklo kūrimo** meniu elementą mobiliame prietaise rūšiavimo siuntimui, matysite mygtuką pavadinimu **Pilnas**. *Nenaudokite **Pilnas** mygtuko padėties rūšiavimui ir uždarymui.*
>
> **Pilnas** mygtukas yra pateikiamas pagal nutylėjimą ir negali būti išjungtas ar pašalinas iš puslapio. Jis nėrra naudojamas *Siunčiamo rūšiavimo* funkcijai.

#### <a name="sort-the-first-container"></a>Rūšiuokite pirmą talpyklą

1. Mobiliame prietaise prisijunkite prie *62* sandėlio naudodami vartotojo identifikavimo kodą, kurį sukūrėte šiam scenarijui (arba esančių demo duomenų vartotojo identifikavimo kodą).
1. Pagrindiniame meniu pasirinkite **Siunčiama**.
1. **Siunčiama** meniu pasirinkite **Padėklo sukūrimas**.
1. **LP/Con** laukelyje įveskite pirmosios talpyklos identifikavimo kodą, kuris yra susietas su prekybos užsakymu 1.
1. Pasirinkite **Gerai**.
1. Kadangi šiuo metu nėra jokių rūšiavimo padėčių, turite bent vieną nurodyti. **Rūšiavimo padėties identififikavimo kodo** laukelyje įveskite *SP01*.
1. Kadangi šiuo metu nėra susieto jokio LP su esama padėtimi *SP01*, turite bent vieną nurodyti. **LP** laukelyje įveskite *PLP01*.
1. Pasirinkite **Gerai**.
1. Kadangi rūšiavimo padėties patvirtinimas yra įjungtas, privalo įvesti rūšiavimo padėties identifikavimo kodą dar kartą. **Rūšiavimo padėties identififikavimo kodo** laukelyje įveskite *SP01*.
1. Pasirinkite **Gerai**.

    Matysite „Darbas baigtas“ pranešimą.

> [!TIP]
> Rūšiuotos padėties peržiūrai ir LP joje peržiūrai, eikite į**Sandėlio valdymas \> Pakavimas ir dėjimas į konteinerius \> Siunčiamo rūšiavimo padėties priskyrimai**.
>
> **Siunčiamo rūšiavimo padėties priskyrimai** langas rodo visas rūšiavimo padėtis, kurios šiuo metu yra įjungtos. **Rūšiavimo padėties pervedimai** laukelis rodo LP, kuris yra susietas su kiekviena rūšiavimo padėtimi ir rūšiavimo padėtyje nesančiomis talpyklomis. Atkreipkite dėmesį, kad viena rūšiavimo padėtis šiuo metu egzistuoja ir **Padėties rūšiavimo kriterijų** „FastTab“ rodo **Siuntimo – Vežėjo paslaugų - Oro** kriterijų.

#### <a name="sort-the-remaining-containers"></a>Rūšiuokite likusias talpyklas

1. Mobiliame prietaise prisijunkite prie *62* sandėlio naudodami vartotojo identifikavimo kodą, kurį sukūrėte šiam scenarijui (arba esančių demo duomenų vartotojo identifikavimo kodą).
1. Pagrindiniame meniu pasirinkite **Siunčiama**.
1. **Siunčiama** meniu pasirinkite **Padėklo sukūrimas**.
1. **LP/Con** laukelyje įveskite antrosios talpyklos identifikavimo kodą, kuris yra susietas su prekybos užsakymu 1.
1. Pasirinkite **Gerai**. Kadangi rūšiavimo šablonas yra nustatytas automatiniam rūšiavimui ir kriterijus atitinkantis padėties rūšiavimas jau egzistuoja, esate automatiškai nukreipiami į tinkamą rūšiavimo padėtį.
1. Pasirinkite **Gerai**.
1. Patvirtinkite rūšiavimo padėties identifikavimo kodą tam, kad nurodytumėte, jog inventorius yra tinkamoje vietoje. **Rūšiavimo padėties identififikavimo kodo** laukelyje įveskite *SP01*.
1. Pasirinkite **Gerai**.

    Darbas yra baigtas antrojoje talpykloje iš prekybos užsakymo 1. Dabar rūšiuosite likusias talpyklas iš prekybos užsakymo 2.

1. **LP/Con** laukelyje įveskite antrosios talpyklos identifikavimo kodą, kuris yra susietas su prekybos užsakymu 2 *A0001*. Kadangi vežėjo paslaugos skiriasi, jums siūloma įvesti naują rūšiavimo padėtį ir priskirti LP tai padėčiai. Naudokite padėties rūšiavimą *SP02* ir LP *PLP02*.
1. Pasirinkite **Gerai**.
1. Patikrinkite rūšiavimo padėtį įvesdami *SP02* **Padėties rūšiavimo identifikavimo kodo** laukelyje.
1. Pasirinkite **Gerai**.

    Darbas talpykloje baigtas.

1. **LP/Con** laukelyje įveskite likusios talpyklos identifikavimo kodą, kuris yra susietas su prekybos užsakymu 2 *A0002*. Kadangi vežėjo paslaugos sutampa su prekybos užsakymo 1 vežėjo paslaugomis, sistema rodo esančią rūšiavimo padėtį, kuri atitinka kriterijus.
1. Pasirinkite **Gerai**.
1. Patikrinkite rūšiavimo padėtį įvesdami *SP02* **Padėties rūšiavimo identifikavimo kodo** laukelyje.
1. Pasirinkite **Gerai**.

    Darbas talpykloje baigtas.

### <a name="close-the-outbound-sorting-positions"></a>Uždarykite siunčiamo rūšiavimo padėtis

Kai inventorius yra rūšiuotas, padėtis turi būti uždaryti prieš darbo sukūrimą. Rūšiuoto inventoriaus paėmimo darbas bus sukuriamas tam, kad inventorius būtų paimtas į „bay door“.

#### <a name="close-a-position-from-the-mobile-device"></a>Uždarykite padėtį mobiliame prietaise

1. Mobiliame prietaise prisijunkite prie *62* sandėlio naudodami vartotojo identifikavimo kodą, kurį sukūrėte šiam scenarijui (arba esančių demo duomenų vartotojo identifikavimo kodą).
1. Pagrindiniame meniu pasirinkite **Siunčiama**.
1. **Siunčiama** meniu pasirinkite **Padėklo sukūrimas**.
1. **LP/Con** laukelyje įveskite talpyklos identifikavimo numerį, kuris buvo rūšiuotas padėties *SP01* rūšiavimui.
1. Pasirinkite **Gerai**.
1. Matysite šį pranešimą: „Talpykla jau rūšiuota padėčiai SP01. Uždaryti padėtį?“ Pasirinkite **Uždaryti**.

    Darbas užbaigtas.

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a>Uždaryti padėtį iš siunčiamo rūšiavimo padėties priskyrimo

1. Eikite į **Sandėlio valdymas \> Pakavimas ir dėjimas į konteinerius \> Siunčiamo rūšiavimo padėties priskyrimai**.
1. Kairiame stulpelyje pasirinkite **SP02**. Ši siunčiamo rūšiavimo padėties eilutė yra ta, kurią uždarėte.
1. Veiksmų juostoje pasirinkite**Uždaryti padėtį**. Rūšiavimo padėties įrašas yra uždarytas ir neberodomas.

    > [!TIP]
    > Visų uždarytų padėčių įrašų rodymui, pasirinkite **Rodyti uždarytus** žymimą laukelį.

### <a name="sorted-inventory-picking"></a>Surūšiuotų atsargų paėmimas

Privalote pabaigti rūšiuoto inventoriaus paėmimo darbą. Kai jis pabaigtas, inventorius bus paimamas į prekybos užsakymą. Dabar, visi kiti sandėlio procesai yra pritaikyti.

1. Mobiliame prietaise prisijunkite prie *62* sandėlio naudodami vartotojo identifikavimo kodą, kurį sukūrėte šiam scenarijui (arba esančių demo duomenų vartotojo identifikavimo kodą).
1. Pagrindiniame meniu pasirinkite **Siunčiama**.
1. **Siunčiama** meniu pasirinkite **Pakrovimas iš rūšiavimo**.
1. Įveskite paskirties LP identifikavimo kodą iš pirmosios rūšiavimo padėties, *SP01*. Nustatykite **identifikavimo kodo** lauką į *PLP01*.
1. Pasirinkite **Gerai**.
1. **Rūšiuoto inventoriaus paėmimas: Paimti** puslapis rodo būtiną atlikti paėmimo darbą. Paimkite iš *SORT* vietos ir paskirties LP *PLP01* turės daugelį elementų ir *3* kiekį.
1. Pasirinkite **Gerai**.
1. **Rūšiuoto inventoriaus paėmimas: Padėti** puslapis rodo būtiną atlikti padėjimo darbą. Padėkite į *Baydoor* vietą ir paskirties LP *PLP01* turės daugelį elementų ir *3* kiekį.
1. Pasirinkite **Gerai**.

    Darbas užbaigtas.

1. Įveskite paskirties licencijos numerio identifikavimo kodą iš antrosios rūšiavimo padėties, *SP02*. Nustatykite **identifikavimo kodo** lauką į *PLP02*.
1. Pasirinkite **Gerai**.
1. **Rūšiuoto inventoriaus paėmimas: Paimti** puslapis rodo būtiną atlikti paėmimo darbą. Paimkite iš *SORT* vietos ir paskirties LP *PLP02* turės daugelį elementų ir *1* kiekį.
1. Pasirinkite **Gerai**.
1. **Rūšiuoto inventoriaus paėmimas: Padėti** puslapis rodo būtiną atlikti padėjimo darbą. Padėkite į *Baydoor* vietą ir paskirties LP *PLP02* turės daugelį elementų ir *1* kiekį.
1. Pasirinkite **Gerai**.

    Darbas užbaigtas.

Nuo dabar, visi kiti sandėlio procesai yra pritaikyti.

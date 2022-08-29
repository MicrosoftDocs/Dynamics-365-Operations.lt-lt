---
title: Dėjimas prie sienos - dėjimas į parduotuvę
description: Šiame straipsnyje pateikiama informacija apie "Padėti į sienos" – parduotuvės funkcijas. Funkcijos leidžia jums tvarkyti scenarijus, kuriuose privalote konsoliduoti produktą į išankstinio pakavimo sritį pagal konfigūruojamus kriterijus. Jis padeda sumažinti pakavimo laiką, nes leidžia paimti vieną paskirties licencijos numerį ir gali naudoti daugiau padėjimo padėčių klasterinio paėmimo metu.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: af6dcb6d822ab14b0b4b881ca32626ea6eae4c28
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334513"
---
# <a name="put-to-wall---put-to-store"></a>Dėjimas prie sienos - dėjimas į parduotuvę

[!include [banner](../includes/banner.md)]

*Dėjimo prie sienos - dėjimo į parduotuvę* funkcija eidžia jums tvarkyti scenarijus, kuriuose privalote konsoliduoti produktą į išankstinio pakavimo sritį pagal konfigūruojamus kriterijus. Kadangi ši funkcija leidžia paimti vieną paskirties licencijos numerį ir gali naudoti daugiau padėjimo padėčių klasterinio paėmimo metu, bendrovės siunčiančios į parduotuves ar tvarkančios mažus elementus gauna naudos iš sutrumpinto pakavimo laiko.

Darbo srautas šiai funkcija valdo paimtą produktą į rūšiavimo vietos distribuciją įvairiuose talpyklų tipuose. Bendrai, visos rūšiavimo vietos apima daugelį rūšiavimo padėčių. Kiekviena rūšiavimo padėtis yra priskirta pagal kriterijus nustatytus verslo procese. Dažniausi kriterijai yra galutinė paskirties vieta, siuntimas ar krovimas. Po to, kai gaminys atvyksta, jis paskirstoams visoms rūšiavimo vietoms pagal kiekį susietą su užsakymu, paskirties vieta, siuntimo ar kroviniu. Kai talpykla yra pilna ar užbaigta, ji patraukiama į stacionarią vietą ar siunčiama į vietą tolesniam tvarkymui, priklausomai nuo verslo proceso.

Ši sandėlio savybė taip pat rodoma kitais pavadinimais, tokiais kaip dėjimas į šviesą ar tarpo atidarymas.

## <a name="turn-on-the-outbound-sorting-feature"></a>Įjunkite Siunčiamo rūšiavimo funkciją

Prieš naudojant padėjimo *į* sienos funkciją, *reikia* įjungti sistemos siuntimo rūšiavimo funkciją. Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Siunčiamas rūšiavimas*

*Siunčiamo rūšiavimo* savybė gali būti naudojama kartu su *Plačios bangos žingsnio kodo organizavimo* funkcija, jei ji yra įjungta. Privalote taip pat įjungti šią funkciją, jei naudosite iš anksto nustaytus kodus, nurodytus bangos žingsni koduose. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Organizacijos bangos žingsnio kodas*

## <a name="setup"></a>Sąranka

Šiai demonstracijai, standartiniai „Contoso“ duomenys ir sandėlis *62* yra naudojamas. Keletas vėliau išvardytų priedų yra taip pat naudojami.

### <a name="location-type"></a>Vietos tipas

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos tipai**.
1. Veiksmų juostoje pasirinkite **Naujas** tam, kad sukurtumėte vietos tipo rūšiavimą.
1. Nustatykite toliau nurodytas reikšmes.

    - **Vietos tipas:** *RŪŠIUOTI*
    - **Aprašas:** *Rūšiuoti*

1. Pasirinkite **Įrašyti**.

### <a name="warehouse-management-parameters"></a>Sandėlio valdymo parametrai

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. **Pagrindiniame** skirtuke **Vietos tipai** „FastTab“ nustatykite **Vietos tipo rūšiavimo** lauklį, įveskite *RŪŠIUOTI*.
1. Pasirinkite **Įrašyti**.

### <a name="location-profile"></a>Vietos profilis

1. Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlys \> Vietos profiliai**.
1. Veiksmų juostoje pasirinkite **Naujas** tam, kad sukurtumėte profilį rūšiavimo vietai.
1. Antraštėje nustatykite šias vertes:

    - **Vietos profilio identifikavimo numeris:** *Rūšiuoti*
    - **Pavadinimas:** *Rūšiuoti*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Vietos formatas:** *PAKUOTĖ*
    - **Vietos tipas:** *RŪŠIUOTI*
    - **Naudoti licencijos numerio sekimą:** *Taip*
    - **Leiskite maišytus elementus:** *Taip*
    - **Leiskite maišytas inventoriaus būsenas:** *Taip*

1. Pasirinkite **Įrašyti**.

### <a name="locations"></a>Vietos

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos**.
1. Išvalykite **Kurti patikrinimo skaičius vietai** žymimą laukelį.
1. Veiksmų juostoje “, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes:

    - **Sandėlis:** *62*
    - **Vieta:** *Rūšiuoti*
    - **Vietos profilio identifikavimo numeris:** *Rūšiuoti*

1. Pasirinkite **Įrašyti**.

### <a name="packing-profiles"></a>Pakavimo šablonai

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Pakavimas \> Pakavimo profiliai**.
1. Veiksmų juostoje “, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes:

    - **Pakavimo profilio identifikavimo numeris:** *Rūšiuoti*
    - **Aprašas:** *Rūšiuoti*
    - **Talpyklos pakavimo politika** Palikite šį laukelį tuščią.
    - **Talpyklos identifikavimo numerio režimas:** *Automatinis*
    - **Talpyklos tipas:** *PADĖKLAS 48x48*
    - **Automatinis talpyklos sukūrimas jam esant uždarytam:** Palikite šį laukelį tuščią.

1. Pasirinkite **Įrašyti**.

### <a name="wave-step-codes"></a>Bangos veiksmo kodai

Jei įjungėte *Plačios bangos žingsnio kodo organizavimo* funkciją, nustatykite šiuos kodus.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos žingsnio kodai**.
1. Veiksmų juostoje “, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes:

    - **Bangos žingsnio kodas:** *Rūšiuoti*
    - **Bangos žingsnio aprašas:** *Rūšiuoti*
    - **Bangos žingsnio tipas:** *Rūšiavimo šablonas*

1. Pasirinkite **Įrašyti**.

### <a name="outbound-sorting-template"></a>Siuntimo rūšiavimo šablonas

Rūšiavimo pavyzdys kontroliuoja, ar rūšiavimo padėtys yra sukurtos, kokie kriterijai yra naudojami ir kitas rūšiavimo proceso savybes.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Pakavimas \> Siunčiamo rūšiavimo šablonas**.
1. Veiksmų juostoje pasirinkite **Naujas** tam, kad rūšiuotumėte šabloną.
1. Naujojo šablono antraštėje nustatykite šias vertes:

    - **Siunčiamo rūšiavimo šablono identifikavimo kodas:** *Bangos rūšiavimas*
    - **Aprašas:** *Bangos rūšiavimas*
    - **BRūšiuoti šablono tipą:** *Bangos poreikis*

        Šis laukelis nulemia procesą, kuriam naudojamas rūšiavimo šablonas. Galimos šios vertės:

        - **Bangos poreikis** – Rūšiavimo šablonas naudojamas *Pridėti prie sienos* procesui. Šio šablono tipas yra naudojamas pakavimo stočiai apeiti ir apdoroti inventorių tiesiogiai ne bangoje. Galite naudoti šį tipą tik jei **rūšiavimo** bangos proceso metodas yra įtrauktas į bangos šabloną.
        - **Talpykla** – Rūšiavimo šablonas yra naudojamas *Padėklo statymui po paėmimo* proceso metu. Šis šablono tipas yra naudojamas apdoroti talpyklas, kurios yra uždarytos pakavimo stotyje ir turi būti surūšiuotos ant padėklų.

    - **Sandėlis:** *62*
    - **Vieta:** *Rūšiuoti*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Rūšiavimo patvirtinimas:** *Padėties nuskaitymas*

        Šis laukelis nulemia patvirtinimą, kurio reikia rūšiavimo metu. Galimos šios vertės:

        - Jokia
        - Numerio lentelės nuskaitymas
        - Padėties nuskaitymas

    - **Sukurkite veiksmą vietos uždaryme:** *Taip*

        Jei ši parinktis nustatyta *Taip*, vietos uždarymo metu, veiksmas bus sukuriamas inventoriaus nugabenimui į galutinę siuntimo vietą. Jei ši parinktis nustatyta *Ne*, inventorius bus nedelsiant paimtas į užsakymą, kai padėtis bus uždaryta.

    - **Padėties priskyrimas:** *Rankinis*

        Šis laukelis nulemia priskyrimo padėties tipą. Galimos šios vertės:

        - **Rankinis** – Vartotojas privalo visuomet nurodyti padėtį, kurioje inventorius turi būti rūšiuojamas.
        - **Automatinis** – Sistema automatiškai ves inventorių į bet kurią padėtį pagal rūšiavimo šablono tarpus.

    - **Priskirti rūšiavimo vietos kriterijus:** *Naudoti tik tuščias padėtis*

        Šis laukelis kontroliuoja, ar jau rūšiavimo padėtyse esantis inventorius yra įtraukiamas, kai padėtis priskiriama poreikiui. Galimos šios vertės:

        - **Naudoti tik tuščią padėtį** – Inventorių jau turinčios ir su juo susietos padėtys bus priimtos domėn
        - **Tuščios padėties priėmimas** – Į visą jau padėtyje esantį inventorių priskyrimo metu atsižvelgta nebus. Visos naudojamos esamos padėtys.

    - **Bangos žingsnio kodas:** *Rūšiuoti*

        Jei *Plačios bangos žingsnio kodo organizavimo* funkcija yra įjungta, *Rūšiavimo* bangos žingsnio kodas turi taip pat būti nustatytas bangos žingsnio koduose.

    - **Automatinio uždarymo rūšiavimo padėtis:** *Taip*

        Jei ši parinktis nustatyta *Taip*, vietos rūšiavimas bus automatiškai uždaromas, kai visi darbai ateinantys į padėtį bus užbaigti.

    - **Rūšiuotų padėčių skaičius:** *3*

        Šis laukelis nulemia didžiausią rūšiuojamų padėčių skaičių, kurį sistema sukurs.

    - **Rūšiavimo padėties priešdėlis:** *SP-*

        Šis laukelis nulemia priešdėlį, kurį sistema priskiria prieš padėties numerį.

    - **Automatinio pakavimo rūšiavimo padėtis:** *Taip*

        Jei ši parinktis nustatyta *Taip*, inventorius rūšiavimo padėtyje bus supakuotas į talpyklą, kai padėtis bus uždaroma.

    - **Pakavimo profilio identifikavimo numeris:** *Rūšiuoti*

        Šis laukelis nulemia pakavimo profilį, kuris bus naudojamas rūšiuojant padėtį supakuotą į talpyklą.

1. Veiksmų juostoje pasirinkite **Redaguoti užklausą** tam, kad nurodytumėte kriterijus naudojamus šiam rūšiavimo šablonui.
1. Užklausos teksto laukelyje, **Rūšiavimo** skirtuke, pasirinkite **Naujas** eilutės įtraukimui ir tuomet nustatykite šias vertes:

    - **Lentelė:** *Krovinio išsami informacija*
    - **Išvestinė lentelė:** *Krovinio išsami informacija*
    - **Laukas:** *Siuntos ID*
    - **Paieškos kryptis:** *Didėjanti*

1. Pasirinkite **Gerai**.
1. Galite gauti šį pranešimą: „Grupavimas bus perkrautas, ar tęsti?“ Pasirinkite **Taip**.

    **Siunčiamo rūšiavimo šablono pertrūkio** mygtukas pasirodo veiksmų juostoje.

1. Veiksmų juostoje pasirinkite **Siunčiamo rūšiavimo šablono pertrūkiai**.
1. Pasirinkite **Grupavimas laukeliais:** žymimą laukelį tam, kad sugrupuotumėte pagal siuntimo identifikavimo kodą.

    Šis nustatymas sukurs vieną padėtį siuntimui, kuris yra talpykla bangoje.

1. Pasirinkite **Gerai**.

### <a name="wave-process-methods"></a>Bangos apdorojimo metodai

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos apdorojimo metodai**.
1. Veiksmų srityje spustelėkite **Pakartotinai generuoti metodus**.

    **Rūšiavimo** metodas yra įtraukiamas į esamų metodų sąrašą, o *Siuntimo* bangos šablono tipas jam yra pasirenkamas.

### <a name="wave-templates"></a>Bangos šablonai

Redaguokite bangos šabloną, naudojamą bangos poreikio rūšiavimui.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
1. **Bangos šablono itpo** laukelyje, pasirinkite *Siuntimas*.
1. Pasirinkite esantį **62 siuntimo nustatytąjį** šabloną.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. **Bendri** „FastTab“, atlikite šiuos pakeitimus:

    - Parinktį **Apdoroti bangą išleidžiant ją į sandėlį** nustatykite į *Ne*.
    - Nustatykite **Priskirti atviroms bangoms** parinktį į *Taip*.

1. **Metodai** „FastTab“, nustatykite **rūšiavimo** metodą:

    1. **Likę metodai** tinklelyje, pasirinkite **rūšiavimas**.
    2. Pasirinkite dešinės rodyklės mygtuką **rūšiavimas** perkėlimui į **Pasirinkti metodai** tinklelį.
    3. **Pasirnkti metodai** tinklelyje, pasirinkite **rūšiavimas**.
    4. Nustatykite **Bangos žingsnio kodo** laukelį į *Rūšiuoti*.

1. Pasirinkite **Įrašyti**.

### <a name="mobile-device-menu-items"></a>Mobiliojo įrenginio meniu elementai

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Antraštėje nustatykite šias vertes:

    - **Meniu elemento pavadinimas:** *Rūšiuoti*
    - **Pavadinimas:** *Rūšiuoti*
    - **Režimas:** *Netiesioginis*
    - **Naudoti sukurtą darbą:** *Ne*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Veiksmo kodas:** *Siunčiamas rūšiavimas*
    - **Naudoti proceso gidą:** *Taip* (nustatytoji vertė)
    - **Siunčiamo rūšiavimo šablono identifikavimo kodas:** *Bangos rūšiavimas*

1. Pasirinkite **Įrašyti**.

### <a name="mobile-device-menu"></a>Mobiliojo įrenginio meniu

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
1. Meniu sąraše pasirinkite **Siuntimas**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. **Esančiuose meniu ir meniu elementų** tinklelyje suraskite ir pasirinkite **Rūšiavimo** meniu elementą, kurį kątik sukūrėte.
1. Pasirinkite dešinės rodyklės mygtuką **Rūšiavimas** perkėlimui į **Meniu struktūros** tinklelį. Šiuo būdu, galėsite įtraukite naują meniu elementą **Siuntimai** meniu.
1. Pasirinkite **Įrašyti**.

### <a name="location-directives"></a>Vietos nurodymai

Privalote sukurti vietos direktyvas, kurios vestų sukurtą darbą po to, kai rūšiavimas yra užbaigtas.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. **Darbo tvarkos tipo** laukelyje pasirinkite *Rūšiuoto inventoriaus paėmimas*.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Antraštėje nustatykite šias vertes:

    - **Seka:** *1*
    - **Pavadinimas:** *Dėti į „Baydoor“*

1. **Padėties direktyvos** „FastTab“, nustatykite šias vertes:

    - **Darbo tipas:** *Padėjimas*
    - **Vieta:** *6*
    - **Sandėlis:** *62*
    - **Nurodymo kodas:** Palikite šį lauką tuščią.
    - **Keletas SKU:** *Ne*

1. Pasirinkite **Įrašyti,** kad būtų galima naudoti **Eilutės** „FastTab“ skirtuką.
1. **Linijų** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes. Priimkite nustatytąsias vertes visiems kitiems laukeliams.

    - **SEekos numeris:** *1*
    - **Pradinis kiekis:** *0*
    - **Galutinis kiekis:** *1000000*

1. Pasirinkite **Įrašyti,** kad būtų galima naudoti **Vietos nurodymų veiksmų** „FastTab“ skirtuką.
1. **Vietos direktyvos veiksmai** „FastTab“, pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes naujoje linijoje. Priimkite nustatytąsias vertes visiems kitiems laukeliams.

    - **SEekos numeris:** *1*
    - **Pavadinimas:** *Baydoor*

1. Pasirinkite **Įrašyti** tam, kad atliktumėte **Siūlymo redagavimo** mygtuką **Vietos direktyvos veiksmai** „FastTab“ prieinamą.
1. „FastTab“ **Vietos nurodymų veiksmai** pasirinkite **Redaguoti užklausą**.
1. Užklausos teksto laukelyje, **Intervalas** skirtuke, suraskite eilutę, kurioje **Laukelis** laukelis yra nustatytas į *Vieta*. Nustatykite **Kriterijų** laukelį šiai eilutei į *Baydoor*.
1. Pasirinkite **OK** redagavimo patvirtinimui.

### <a name="work-classes"></a>Darbo klasės

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Antraštėje nustatykite šias vertes:

    - **Darbo klasės identifikavimo numeris:** *Rūšiavimas*
    - **Aprašas:** *Rūšiavimas*
    - **Darbo tvarkos tipas:** *Rūšiuoto inventoriaus paėmimas*

1. Pasirinkite **Įrašyti**.

### <a name="work-templates"></a>Darbo šablonai

1. Eikite į **Sandėlio valdymas \> Darbas \> Darbo šablonai**.
1. Lauke **Darbo užsakymo tipas** pasirinkite *Pardavimo užsakymai*.
1. Tinklelyje, pasirinkite **62 pasirinkite pakuoti** darbo šabloną.
1. Veiksmų juostoje pasirinkite **Darbo antraštės tarpai**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Linijoje, kurioje **Laukelio pavadinimas** laukelė nustatykite *Siuntimo identifikavimo kodas*, ištrinkite **Grupuoti pagal šį laukelį** žymimą laukelį.
1. Pasirinkite **Įrašyti** ir tuomet uždarykite **Darbo antraštės tarpai** teksto laukelį.
1. **Darbo tvarkos tipo** laukelyje pasirinkite *Rūšiuoto inventoriaus paėmimas*.
1. Pasirinkite **Naujas** tam, kad sukurtumėte darbo šabloną.
1. **Peržiūros** skyriuje, nustatykite šias vertes. Priimkite nustatytąsias vertes visiems kitiems laukeliams.

    - **Darbo šablonas:** *Rūšiuotas paėmimas*
    - **Darbo šablono aprašas:** *Rūšiuotas paėmimas*

1. Pasirinkite **Įrašyti** tam, kad padarytumėte **Darbo šablono informacijos** skyrių prieinamą.
1. **Darbo šablono informacijos** skyriuje sukursti dvi eilutes. Pasirinkite **Naujas** ir tuomet nustatykite tolesnes vertes eilutei 1:

    - **Darbo tipas:** *Paėmimas*
    - **Privaloma:** Pasirinkite (= *Taip*)
    - **Darbo klasės identifikavimo numeris:** *Rūšiavimas*

1. Pasirinkite **Naujas** dar kartą ir tuomet nustatykite tolesnes vertes eilutei 2:

    - **Darbo tipas:** *Padėjimas*
    - **Privaloma:** Pasirinkite (= *Taip*)
    - **Darbo klasės identifikavimo numeris:** *Rūšiavimas*

1. Pasirinkite **Įrašyti**.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Šis scenarijus simuliuoja situaciją, kuomet sandėlis talpina mažus objektus vietose ir turi pakuoti juos į dėžės prieš siuntimą bei kai pakavimo stoties veikimas nėra labai tinkamas. Darbuotojai paima užsakymus daugeliui klientų ir skirtingais adresais tuo pačiu metu taip padidindami paėmimo greitį. Po paėmimo, darbuotojais atvyksta į rūšiavimo vietą, kurioje paimti objektai gali būti surūšiuoti į tinkamas dėžės pagal būtinus kriterijus. Šiame pavyzdyje siuntimo identifikavimo kodas bus naudojamas nulemti tinkamą dėžę, nes visi siuntimai turi skirtingus adresus. Po to, kai visi objektai iš krovimo yra supakuoti ir rūšiuoti pagal siuntimus, dėžės bus patraukiamos į paruošimo vietą ir vėliau pakraunamo į sunkvežimį.

Prieš šio scenarijaus pradžią, įsitikinkite, kad visos standartinės sandėlio funkcijos jūsų sandėlyje yra nustatytos tinkamai. Standartinis „Contoso“ sandėlis *62* yra naudojamas šiuo tikslu. Standartinės konfigūracijos nebuvo pakeistos, taip pat nepakeista informacija nustatymuose.

### <a name="create-demand"></a>Kurti paklausą

Prieš funkcijų rodymą, privalote sukurti šiek tiek poreikio. Šiame scenarijui, sukursti tris prekybos užsakymus trims skirtingiems klientams tam, kad simuliuotumėte skirtingus pristatymo adresus, Tokiu būdu, sukursite tris skirtingus siuntimus.

Prieš sukuriant prekybos užsakymus ir siuntimus, įsitikinkite, kad paėmimo vietos turi pakankamai inventoriaus visiems objektams užsakymuose. Peržiūrėkite vietos direktyvos nustatymus, kad patvirtintumėte paėmimo vietas naudojamas prekybos užsakymo paėmime. Jei reikia koreguoti atsargas, galite sukurti rankinius perkėlimus, naudoti papildymą arba bet kokį kitą srautą. Tuomet rezervuokite inventorių.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Naujas** prekybos užsakymo sukūrimui užsakymui 1.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Klientas:** *US-001*
    - **Sandėlis:** *62*

1. Pasirinkite **Gerai**.
1. Nauja eilutė pridedama į „FastTab” skirtuką **Pardavimo užsakymo eilutės**. Nustatykite toliau nurodytas reikšmes.

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *5*

1. Pasirinkite **Įtraukti eilutę** antrai eilutei įtraukti ir nustatykite šias reikšmes:

    - **Prekės numeris:** *A0002*
    - **Kiekis:** *10*

1. Pakartokite tolesnius žingsnius kiekvienai prekybos eilutei užsakyme tam, kad rezervuotumėte jam inventorių:

    1. „FastTab“ skirtuke **Pardavimo užsakymo eilutės** meniu **Atsargos** pasirinkite **rezervavimas**.
    1. **Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.
    1. Pasirinkite **Įrašyti**.

1. Pasirinkite **Naujas** prekybos užsakymo sukūrimui užsakymui 2.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Klientas:** *US-004*
    - **Sandėlis:** *62*

1. Pasirinkite **Gerai**.
1. Nauja eilutė pridedama į „FastTab” skirtuką **Pardavimo užsakymo eilutės**. Nustatykite toliau nurodytas reikšmes.

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *7*

1. Pasirinkite **Įtraukti eilutę** antrai eilutei įtraukti ir nustatykite šias reikšmes:

    - **Prekės numeris:** *A0002*
    - **Kiekis:** *3*

1. Pakartokite tolesnius žingsnius kiekvienai prekybos eilutei užsakyme tam, kad rezervuotumėte jam inventorių:

    1. „FastTab“ skirtuke **Pardavimo užsakymo eilutės** meniu **Atsargos** pasirinkite **rezervavimas**.
    1. **Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.
    1. Pasirinkite **Įrašyti**.

1. Pasirinkite **Naujas** prekybos užsakymo sukūrimui užsakymui 3.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Klientas:** *US-007*
    - **Sandėlis:** *62*

1. Pasirinkite **Gerai**.
1. Nauja eilutė pridedama į „FastTab” skirtuką **Pardavimo užsakymo eilutės**. Nustatykite toliau nurodytas reikšmes.

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *8*

1. Pakartokite šiuos žingsnius tam, kad rezervuotumėte inventorių prekybos eilutei:

    1. „FastTab“ skirtuke **Pardavimo užsakymo eilutės** meniu **Atsargos** pasirinkite **rezervavimas**.
    1. **Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.
    1. Pasirinkite **Įrašyti**.

Pabaikite tolesnias procedūras tam, kad paleistumėte visus prekybos užsakymus sandėliui. Bus sukurti trys skirtingi siuntimai. Tuomet galėsite įtraukti tris skirtingus siuntimus vienai bangai.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Tinklelyje pasirinkite pirmą savo sukurtą prekybos užsakymą.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Gausite informacinį pranešimą, kuris rodys sukurtą bangos identifikavimo kodą ir siuntimo identifikavimo kodą.

1. Pakartokite ankstesnius žingsnius prekybos užsakymų 2 ir 3 išleidimui į sandelį. Atkreipkite dėmesį, kad jūsų gautas informacinis pranešimas nurodo, kad siuntimas buvo įtrauktas į bangą sukurtą jūsų išleistam prekybos užsakymui 1.
1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
1. Pasirinkite bangos identifikavimo kodą, kuris buvo sukurtas iš prekybos užsakymui tam, kad atidarytumėte **Bangų** puslapį. Puslapis rodo bangos informaciją. **Bangos eilučių**„FastTab“ rodo sukurtus siuntimus.

    Privalote dabar sukurti darbą objektų nusiuntimui į paėmimo vietas rūšiavimo vietoje.

1. Veiksmų juostoje pasirinkite **Apdoroti**.

    Bangos apdorojimo metu, rūšiavimo metodas naudos rūšiavimo šabloną priskirdamas inventorių rūšiavimo padėtims. Kai banga yra apdorota, gausite informacinį pranešimą sakantį, kad banga buvo publikuota ir darbas buvo sukurtas.

1. Veiksmų juostoje, **Bangos** skirtuke, **Susijusios informacijos** grupėje, pasirinkite **Darbas** tam, kad peržiūrėtumėte šiai bangą sukurtą darbą. Pasižymėkite darbo ID.
1. Eikite į **Sandėlio valdymas \> Pakavimas ir dėjimas į konteinerius \> Siunčiamo rūšiavimo padėties priskyrimai**.
1. Kairiame stulpelyje galite peržiūrėti siunčiamą rūšiavimo padėtį sukurtą visiems siuntimams.
1. **Rūšiavimo padėties kriterijų** „FastTab“, galite peržiūrėti siuntimo identifikavimo kodą tai padėčiai.

Buvo sukurtas vienas darbo identifikavimo kodas tam, kad nusiųstų inventorių iš paėmimo vietų į rūšiavimo vietą. Darbo užbaigimui jums reikės darbo identifikavimo kodo, kuris buvo sukurtas bangos apdorojimo metu.

### <a name="sales-order-picking-to-the-sorting-location"></a>Prekybos užsakymo paėmimas rūšiavimo vietai

1. Prisijunkite prie mobilios programos kaip darbuotojas sandėlyje *62*.
1. Pagrindiniame meniu pasirinkite **Siunčiama**.
1. **Siunčiama** meniu pasirinkite **Prekybos paėmimas**.
1. Pasirinkite **identifikavimo kodo** laukelį ir tuomet įveskite darbo identifikavimo kodą iš bangos apdorojimo.
1. Patvirtinkite savo įrašą.

    Po to, būsite paskatinti įvesti galutinį licencijos numerį (LP). Atkreipkite dėmesį, kad eilutė 1 iš prekybos užsakymo 1, kuris turi būti paimtas ir įtrauktas į galutinį licencijos numerį. Rodomas objekto numeris, kiekis, aprašas ir paėmimo vieta.

1. **Galutinio LP** laukelyje įveskite licencijos numerį.

    Paimsite visas eilutes, kurios buvo sukurtos bangos apdorojimo metu į tą patį galutinį licencijos numerį.

1. Patvirtinkite savo įrašą.

    Mobili programa dabar rodo **Paėmimo** puslapio serijas, kurios rodo jums paėmimo vietas ir objektą bei būtiną paimti kiekį. Po to, kai objektas yra įtrauktas į licencijos numerį, patvirtinsite paėmimo darbą. Paskutinis puslapis bus darbas, kuris paėmė objektus į rūšiavimo vietą.

1. Patvirtinkite pirmą paėmimo darbą.
1. Rodomas kitas paėmimo darbas. Patvirtinkite paėmimą.
1. Tęskite tvirtindami likusį paėmimo darbą.
1. Paskutinis žingsnis yra pabaigti padėjimo darbą. Patvirtinkite padėjimą šalin į rūšiavimo vietą.

    Matysite „Darbas baigtas“ pranešimą.

1. Išeikite iš **Prekybos paėmimo** mobilioje programoje.

### <a name="sortingput-to-wall"></a>Rūšiavimas/dėjimas prie sienos

Dabar, kai visas inventorius buvo įdėtas į rūšiavimo vietą, jis turi būti surūšiuotas į teisingą rūšiavimo vietą.

1. Prisijungimas prie mobilios programos.
1. Pagrindiniame meniu pasirinkite **Siunčiama**.
1. **Siuntimo** meniu pasirinkite **Rūšiuoti** objektų rūšiavimo pradžiai.
1. **LP/CON** laukelyje įveskite paimto prekybos užsakymo darbo paskirties licencijos numerį.
1. Patvirtinkite savo įrašą.
1. Įveskite objekto numerį, kurį reikia rūšiuoti pirma.
1. Sistema nusprendža, jurią rūšiavimo vietą reikia rodyti pirmiausiai. Patvirtinkite rūšiavimo padėtį.
1. Būsite paskatinti priskirti licencijos numerį rūšiavimo vietai. Pasirinkite **LP** laukelį ir įveskite licencijos numerį ir tuomet patvirtinkite savo įrašą.

    Kadangi rūšiavimo padėtis yra susieta su siuntimo identifikavimo kodu, jūs rūšiuosite paimtus objektus į licencijos numerį, nurodytą siunčiamame siuntime ir prekybos užsakyme.

    Kitas puslapis rodo objekto identifikavimo numerį, kokybę, rūšiavimo padėties identifikavimo numerį ir iš kur (paėmimas) į kur (rūšiavimas) licencijos numerio identifikavimo kodus. Informacija šiame puslapyje aiškina jums, kaip rūšiuoti konkrečius objektus ir kiekius iš paėmimo licencijos numerio į rūšiavimo licencijos numerį.

1. Patvirtinkite rūšiavimo padėtį.
1. Rūšiuokite objektus į pirmą rūšiavimo padėtį. Kai pabaigėte, sistema nukreips jus į kitą rūšiavimo padėtį.
1. Pakartokite šią procedūrą visoms paimtoms eilutėms darbo užsakyme. Taip pat turėtumėte naudoti šį procesą, kai esama kelių paėmimo eilučių, kurios turi tą patį objekto numerį.

    Kartojant šį procesą su visais objektais, sistema vertina kriterijus iš nuskaityto kito objekto (darbo linijos) ir nusprendžia, kuris rūšiavimo padėtis turi būti padėta. Jūs automatiškai nukreipiami tam, kad padėtumėte objektą į tinkamą rūšiavimo padėtį. Priklausomai nuo patvirtinimo nustatymų, esate nukreiptas patvirtinti šį veiksmą įvedant padėties numerį ar licencijos numerio identifikavimo kodą.

    > [!NOTE]
    > Jei įjungtas automatinis rūšiavimas, rankinis pakeitimas nėra galimas.

1. Kai baigėte, „Microsoft Dynamics 365 Supply Chain Management“, atidarykite **Siuntimo rūšiavimo padėties priskyrimo** puslapį, kad peržiūrėtumėte padėčių būseną.

    - Jei padėtys yra uždaromos automatiškai, pasirinkite **Rodyti uždarytas** tam, kad rodytumėte uždarytas padėtis.
    - Atkreipkite dėmesį, kad yra rodomi rūšiavimo padėties pervedimai. Apdorotas objektas ir kiekis yra apdorojami per rodomas padėtis.

    Kai nustatote siunčiamo rūšiavimo šabloną, nustatote **Automatinio uždarymo rūšiavimo padėties** parinktį į *Taip*. Dėl to, padėtis yra automatiškai uždaroma po to, kai paskutinis tikėtinas intventorius yra patalpintas. Rūšiavimo padėtyes yra **Uždarytos** būsenoje ir darbas buvo sukurtas tam, kad perkeltų rūšiuotą inventorių į *Baydoor* vietą.

1. Pabaikite rūšiuoto inventoriaus paėmimo darbą tam, kad perkeltumėte inventorių į siuntimo vietą. Kai inventorius yra paruoštas, patvirtinkite jo siuntimą.

> [!NOTE]
> Rūšiuoto inventoriaus paėmimo darbo tinkamam apdorojimui, mobilaus prietaiso meniu objektas turi darbo klasės identifikavimo kodą, kuriame **Darbo tvarkos tipo** laukelis yra nustatytas *Rūšiuoto inventoriaus paėmimas* ir turi būti naudojamas judėjimo ir krovimo procedūroms.

### <a name="manually-close-a-position-optional"></a>Rankiniu būdu uždarykite padėtį (pasirinktinai)

Jei rūšiavimo padėtys turi būti uždarytos rankiniu būdu, **Automatinio uždarymo rūšiavimo padėties** parinktis siunčiamo rūšiavimo šablonui turi būti nustatyta į *Ne* ir uždarymas turi būti atliktas prieš inventoriaus judėjimą į „bay door“ sritį. Padėtys gali būti uždaromos įvariais būdais:

- Per Sandėlio valdymo mobiliųjų įrenginių programėlę:

    - Vartotojai gali nuskaityti vieną iš objektų, kurie jau yra padėtyje ir tuomet pasirinkti **Uždaryti** padėties uždarymui.
    - Jei vartotojas nuskaito talpyklą, kuri jau buvo rūšiuota talpykloje, rodomas klaidos pranešimas. Nepaisant to, vartotojas gali ir toliau tęsti padėties uždarymą.

- „Microsoft Dynamics 365 Supply Chain Management“ **Siunčiamo rūšiavimo padėties priskyrimuose** puslapyje:

    - Vartotojai gali pasirinkti siunčiamo rūšiavimo padėties įrašą ir tuomet pasirinkti **Uždaryti padėtį** veiksmų juostoje.

## <a name="tips"></a>Patarimai

- Objektus galima judinti tarp padėčių po to, kai jie buvo vienai priskirti. Sistema įvertina, kiek kiekvieno objekto vienetų turėtų eiti į konkrečią padėtį.
- Rūšiavimo šablonas gali būti kofigūruojamas automatiškai sukurti talpyklas, kai padėtys yra uždarytos. Šis požiūris sukurs standartinės talpyklos identifikavimo kodo strukūtrą, kuri paremta konkrečiu pakavim profiliu.

> [!IMPORTANT]
> Po to, kai judėjimo darbas yra sukurti pagal rūšiavimo vietą, privalote neatšaukti darbo. Kitu atveju, pozicija ir talpyklos jame bus pašalintos iš sistemos ir neprieinamos tolesniam apdorojimui. Inventorius taip pat bus pašalintas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
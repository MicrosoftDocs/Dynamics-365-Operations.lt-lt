---
title: Prailgintų garantijų kūrimas ir konfigūravimas
description: Šioje temoje aptariamos prailgintos garantijos ir aprašoma, kaip sukurti ir sukonfigūruoti jas „Microsoft Microsoft Dynamics 365 Commerce“.
author: sijoshi
manager: annbe
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: sijoshi
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2457f2cf1d6bfb228aae63a0aebaca0d159b7323
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209082"
---
# <a name="create-and-configure-extended-warranties"></a>Išplėstinių garantijų kūrimas ir konfigūravimas

[!include [banner](includes/banner.md)]

Šioje temoje aptariamos prailgintos garantijos ir aprašoma, kaip sukurti ir sukonfigūruoti jas „Microsoft Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

Pirkėjai vis dažniau renkasi ilgiau teikiamą pagalbą ir paslaugas pirkdami produktus, ypač vartojimo produktus, parduodamus mažiausia suapvalinta kaina, pavyzdžiui, telefonus ir kompiuterius. Teikdami prailgintas pardavimo garantijas, mažmeninės prekybos atstovai padeda sukurti klientų lojalumą. Prailgintos garantijos užtikrina klientus, kad jie turės į ką kreiptis dėl paslaugos ir pagalbos. Todėl jie gali būti tikri, kad jų problemos bus veiksmingai išspręstos.

Prailgintos garantijos gali būti parduodamos klientams mažmeninės prekybos kanalu pirmojo produkto pirkimo metu. Jie taip pat gali būti parduodami ribotą laiko tarpą po pirmojo pirkimo.

### <a name="warranty-item-setup"></a>Garantinės prekės nustatymas

„Dynamics 365 Commerce” suteikia funkciją, leidžiančią sukurti garantinę prekę ir nustatyti jos atributus. Šie atributai susieja produktą ir garantinę prekę, garantijos kainą ir garantinį laikotarpį. Po to, kai garantinė prekė sukonfigūruojama ir išleidžiama į organizacinį vienetą, pardavėjas gali parduoti garantijas naudodamas modernų kasos aparatą (EKA), internetines parduotuves ir kitus mažmeninės prekybos kanalus.

### <a name="warranty-item-sales"></a>Garantinės prekės pardavimai

Prailgintos garantijos gali būti parduodamos klientams mažmeninės prekybos kanalu pirmojo produkto pirkimo metu. Jie taip pat gali būti parduodami ribotą laiko tarpą po pirmojo pirkimo.

Kasoje (EKA) pardavėjai paraginami įtraukti prailgintą garantiją, kai susijęs produktas pridedamas į kliento krepšelį. Todėl papildomo pardavimo arba kryžminis pardavimo galimybė pateikiama pardavėjams kaip pardavimų srauto dalis.

Klientai taip pat gali sugrįžti vėliau ir įsigyti prailgintą garantiją anksčiau įsigytam produktui. Tokiais atvejais, pardavėjas gali surasti pirminę operaciją ir parduoti susijusią prailgintos garantijos prekę.

### <a name="warranty-terminology"></a>Garantijos terminologija

Toliau pateikiamoje lentelėje nurodyti tam tikri su garantija susiję terminai.

| Terminas | aprašymas |
|------------------------------|--------------|
| Prailginta garantija/garantija | *Prailginta garantija* nurodo paslaugos susitarimą arba sutartį, suteikiančią prailgintą garantiją klientams. Į prailgintą garantiją įeina papildoma prekių keitimo ir remonto paslauga per prailgintą garantinį laikotarpį. |
| Gamintojo garantija | *Gamintojo garantija* (dažnai vadinama *ribotąją garantija*) yra garantija, kurią klientai gauna įsigydami produktą. Štai keletas gamintojo garantijos funkcijų:<ul><li>Garantijos kaštai įtraukiami į produkto savikainą. Klientams nereikia mokėti papildomos gamintojo garantijos sumos.</li><li>Atsižvelgiant į produkto kategoriją, gamintojo garantija paprastai trunka 30 dienų, šešis mėnesius arba vienerius metus. (Daugumai buitinės elektronikos, garantija trunka vienerius metus).</li><li>Garantija taikoma visiems trūkumams, atsiradusiems dėl mechaninių ar elektroninių gedimų. Padengimas yra ribotas ir į jį neįeina jokie atsitiktiniai įsigyto produkto sugadinimai. Klientai, norintys apsaugoti jų įsigytus produktus nuo kasdienių pažeidimų, turėtų investuoti į prailgintą garantiją. Prailgintos garantijos trunka nuo dvejų iki dešimties metų, atsižvelgiant į produkto kategoriją. Jie taip pat turi platesnę aprėptį ir padengia daugiau kasdienių pažeidimų, pavyzdžiui, numetimų, išsipylimų ir dėmių.</li></ul> |
| Garantinė prekė | *Garantinė prekė* yra prailgintos garantijos prekė, parduodama kaip prekė, kuriai gali būti suteikiama garantija. Pavyzdys yra dvejų metų atsitiktinio nešiojamųjų kompiuterių apsaugos planas. |
| Garantinė prekė | *Garantinė prekė* yra nuolat leidžiamas produktas, kuriam parduodama garantija. Pavyzdžiui, nešiojamas kompiuteris yra garantinė prekė, kuriai parduodamos dviejų ir trijų metų garantijos. |
| Garantijų grupė | *Garantijų grupė* yra ryšys tarp garantinių prekių ir galimai garantinių prekių. EKA naudoja garantijų grupes, kad nustatytų, kurias garantines prekes pardavėjai turėtų būti paraginti pridėti, kai galimai garantinė prekė yra pridėta į kliento krepšelį. |
| Garantijos strategija | *Garantijos politika* yra objektas, sukuriamas „Commerce”, kai garantijos politika parduodama. Garantijos politikoje yra tokia informacija, kaip įsigytų garantinės prekės pradžios ir pabaigos datos, sąlygos bei garantinio produkto serijos numeris. Garantijos politikos numerius galima bendrinti su klientais, kad jie turėtų nuorodą į jų įsigytą pratęsto garantinio laikotarpio prekę. |

## <a name="create-a-warranty-item"></a>Sukurkite garantinę prekę

Norėdami sukurti garantinę prekę „Commerce”, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Produktai**.
1. Pasirinkite **Naujas**, kad sukurtumėte garantinę prekę.
1. Dialogo lange **Naujas produktas** **Produkto tipas** lauke pasirinkite **Paslauga**.
1. **Produkto potipis** lauke pasirinkite **Produktas**.
1. **Produkto paslaugos tipas** lauke pasirinkite **Paslauga**.
1. **Produkto pavadinimas** lauke įveskite produkto pavadinimą.
1. **Mažmeninės prekybos kategorija** lauke pasirinkite vertę išplečiamojo dialogo lange ir pasirinkite **Gerai**.
1. **Produkto numeris** lauke įveskite produkto numerį.
1. Pasirinkite **Gerai**.
1. **Produkto išsami informacija** puslapyje, „FastTab” skirtuke **Garantija** nustatykite **Laiko vienetas** ir **Trukmė** laukus.

    | Lauko pavadinimas | Vertė | aprašymas |
    |------------|-------|-------------|
    | Laiko vienetas | **Diena (-os)**, **Savaitė (-ės)**, **Mėnuo (-esiai)** arba **Metai** | Šis laukas nurodo laiko vienetą, naudojamą garantijai. |
    | Laiko trukmė | Teigiamo sveikojo skaičiaus vertė | Šis laukas nurodo garantijos trukmę pasirinktame laiko vienete. |

    Pavyzdžiui, dvejų metų garantijai nustatykite **Laiko vienetas** lauką į **Metai** ir **Trukmė** lauką į **2**. Taip pat nustatykite **Laiko vienetas** lauką į **Mėnuo (-esiai)** ir **Trukmė** lauką į **24** kaip parodyta šioje iliustracijoje.

    ![Produkto išsamios informacijos puslapis garantinei prekei](./media/ew-time-properties.png)

1. Pasirinkite **Įrašyti**, kad įrašytumėte garantinę prekę.
1. Išleiskite garantinį produktą įmonei, kad jį galėtų parduoti. Daugiau informacijos rasite [Mažmeninės prekybos produktų nustatymas](set-up-retail-products.md).
1. **Išleisto produkto išsami informacija** puslapyje, **Garantija** „FastTab” skirtuke, nustatykite **Kainos intervalo bazė**, **Žemutinė riba** ir **Viršutinė riba**.

    | Lauko pavadinimas | Vertė | aprašymas |
    |------------|-------|-------------|
    | Bazinis kainų diapazoną | **Nėra**, **Bazinė kaina** arba **Pardavimo kaina** | <ul><li>**Nėra** – **Žemutinė riba** ir **Viršutinė riba** kainos vertės intervalai netaikomi.</li><li>**Bazinė kaina** – nurodyta garantija bus taikoma, atsižvelgiant į galimai garantinės prekės kainą, jei galimai garantinės prekės bazinė kaina (t. y. kaina be nuolaidų) svyruoja tarp čia nurodytų **Žemutinė riba** ir **Viršutinė riba** verčių.</li><li>**Pardavimo kaina** – ši vertė rezervuota būsimiems tikslams.</li></ul> |
    | Žemutinė riba, viršutinė riba | Teigiamo sveikojo skaičiaus vertė | Šie laukai apibrėžia galimai garantinės prekės viršutinę ir žemutinės kainos ribas ir kaip dabartinė garantinė prekė taikoma galimai garantinei prekei. Šios ribos paremtos galimai garantinės prekės bazine kaina (dar vadinama gamintojo pasiūlyta mažmeninės prekybos kaina \[angl. Manufacturer's Suggested Retail Price (MSRP )\]). Jei **Kainos intervalo bazė** laukas nustatytas kaip **Bazinė kaina**, tik galimai garantinė prekė (produktas), kurio bazinė kaina svyruoja tarp **Žemutinė riba** ir **Viršutinė riba** verčių paskatins iššauks raginimą pridėti galimai garantinę prekę į EKA. |

    Pavyzdžiui, toliau pateiktoje iliustracijoje parodytas **Kainos intervalo bazė** laukas, nustatytas į **Bazinė kaina**, **Žemutinė riba** laukas nustatytas į 500 $ ir **Viršutinė riba** laukas nustatytas į 1000 $.
    
    ![Išleisto produkto išsamios informacijos puslapis garantinei prekei](./media/ew-release-product-details.png)

1. Surūšiuokite garantinę prekę kanale, kuriame jis bus parduodama. Daugiau informacijos žr. [Asortimento nustatymas](set-up-assortments.md).

### <a name="example"></a>Pavyzdys

Nešiojamo kompiuterio galimai garantinė prekė (produktas), kurios bazinė kaina yra 999 $ bazinę kainą, ir yra dvi nešiojamų kompiuterių garantinės prekės:

- Garantija Nr. \_ 1 turi žemutinę 500 $ ribą ir viršutinę 1000 $ ribą, o **Kainos intervalo bazė** laukas nustatytas kaip **Bazinė kaina**.
- Garantija Nr. \_ 2 turi žemutinę 1001 $ ribą ir viršutinę 2000 $ ribą, o **Kainos intervalo bazė** laukas nustatytas kaip **Bazinė kaina**.

Šiuo atveju, kai į kliento krepšelį pridedama nešiojamo kompiuterio galimai garantinė prekė, atsiranda raginimas pridėti Garantiją Nr.\_1 bus parodyta EKA, nes nešiojamo kompiuterio kaina svyruoja tarp žemutinės ir viršutinės ribų, skirtų Garantijai Nr. \_1.

> [!NOTE]
> Pavyzdžiui, jei norite, kad raginimai būtų rodomai tiek Garantijai Nr.\_1 ir Garantijai Nr.\_2 nepriklausomai nuo galimai garantinės prekės kainos, nustatykite **Kainos intervalo bazė** lauką į **Nėra**.

## <a name="configure-channel-specific-settings"></a>Kanalui būdingų parametrų nustatymas

Nustatydami kanalui būdingus parametrus, galite nurodyti, ar raginimas pridėti garantinę prekę bus rodomas EKA, kai galimai garantinė prekė pridedama į kliento krepšelį.

Norėdami sukonfigūruoti kanalui būdingą parametrą „Commerce”, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Garantija \> Garantijos parametrai**.
1. **Kanalui būdinga** skirtuke, esančiame **Garantijos raginimas** jūsų kanalo stulpelyje, atlikite šiuos veiksmus:

    - Pažymėkite šį žymės langelį, jei garantinės prekės raginimas turėtų būti rodomas EKA, kai garantinė prekė pridedama į krepšelį.
    - Atžymėkite žymės langelį, jei nenorite, kad būtų rodomas garantinės prekės raginimas EKA, kai garantinė prekė pridedama į krepšelį.

1. Paleiskite **1070** užduotį sinchronizuoti duomenis su kanalu.

## <a name="configure-a-number-sequence-for-warranty-policies"></a>Konfigūruokite garantinių strategijų numeraciją

Kiekviena unikalią garantinę strategiją identifikuoja garantinės strategijos numeris, kurį sugeneruoja numeracija. Daugiau informacijos apie numeracijas rasite [Numeracijų apžvalga](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Norėdami sukonfigūruoti garantinių strategijų numeraciją „Commerce”, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Garantija \> Garantijos parametrai**.
1. **Numeracijos** skirtuke **Garantijos politika** nuorodos eilutėje, įveskite arba pasirinkite vertę, esančią **Numeracijos kodas** lauke.

## <a name="set-up-a-warranty-group"></a>Garantijų grupės nustatymas

Garantijų grupė yra ryšys tarp garantinių prekių ir galimai garantinių prekių. EKA naudoja garantijų grupes, kad nustatytų, kurias garantines prekes pardavėjai turėtų būti paraginti pridėti, kai galimai garantinė prekė yra pridėta į kliento krepšelį.

Norėdami nustatyti garantijų grupę „Commerce”, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir komercija \> Produktai ir kategorijos \> Garantija \> Garantijos grupės**.
1. Pasirinkite **Naujas**, kad sukurtumėte garantijų grupę.
1. Lauke **Pavadinimas** įveskite naujos grupės pavadinimą.
1. **Bendra** „FastTab” skirtuke, **Aprašas** lauke, įveskite grupės pavadinimą.
1. **Garantiniai produktai** „FastTab” skirtuke pasirinkite **Pridėti eilutę**, kad pridėtumėte garantinę prekę.
1. **Rodymo tvarka** lauke įveskite numerį, kad suklasifikuotumėte garantijų grupę EKA. EKA pasirodys garantinės prekės didėjančia tvarka garantinės prekės raginimo lange.
1. **Galimai garantiniai produktai** „FastTab” skirtuke pasirinkite **Pridėti eilutę**, kad pridėtumėte galimai garantinius produktus.
1. Jei garantinė prekė taikoma visai galimai garantinių prekių (produktų) kategorijai, pasirinkite kategoriją **Kategorija** lauke. Jei garantinė prekė taikoma konkrečiai galimai garantinei prekei (produktui), pasirinkite produktą **Produktas** lauke.
1. **Taikytini kanalai** „FastTab” skirtuke pasirinkite **Pridėti eilutę**, kad galėtumėte pridėtumėte kanalą, kuriame norite parduoti garantinę prekę.
1. Pasirinkite **Įrašyti**, kad įrašytumėte konfigūraciją.
1. Pasirinkite **Publikuoti**, kad publikuotumėte garantijų grupę.
1. Paleiskite **1040** užduotį sinchronizuoti duomenis kanale.

## <a name="sell-warranty-items-at-the-pos"></a>Garantinių prekių pardavimas EKA

Dvi EKA operacijos leidžia pardavėjams parduoti garantines prekes per klientų pirkimų darbo eigą:

- **Pridėti garantiją** – ši operacija paleidžia raginimą, kuriame rodomos taikytinos garantijos krepšelyje pažymėtai galimai garantinei prekei.
- **Pridėti garantiją esamai operacijai** – ši operacija leidžia pardavėjams parduoti garantijas anksčiau parduotoms galimai garantinėms prekėms. Pardavėjai gali surasti galimai garantinės prekės pirmąją operaciją įvesdami operacijos kvito numerį.

Toliau pateiktoje iliustracijoje pateikiamas EKA terminalo puslapio su raginimu pridėti garantinę prekę esamos galimai garantinės prekės dabartiniam pirkimui pavyzdys.

![Raginimo pridėti dabartinio pirkimo garantinę prekę pavyzdys](./media/ew-sell-warranty.png)

Toliau pateiktoje iliustracijoje parodytas šios funkcijos pavyzdys, skirtas pridėti garantinę prekę galimai anksčiau parduotai garantinei prekei.

![Funkcijos, skirtos pridėti garantinę prekę į anksčiau parduotą galimai garantinę prekę, pavyzdys](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>Apdoroti garantijos operacijas

Kai garantijos parduodamos grynųjų pinigų operacijose, užregistravus operacijas „Commerce” būstinėje, „Commerce” vartotojai gali paleisti **Apdoroti garantijų operacijas** užduotį, kad apdorotų garantijų operacijas ir sukurtų garantijų politikas.

Norėdami apdoroti garantijų operacijas „Commerce“ būstinėje, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Garantija \> Apdoroti garantijų operacijas**.
1. Dialogo lange **Pasirinkti organizacijos mazgus** **Organizacinė hierarchija** lauke pasirinkite vertę.
1. **Galimi organizacijos mazgai** sąraše pasirinkite atskirą parduotuvę arba, jei norite sukurti parduotuvių grupės paketinę užduotį, mazgą.
1. Pasirinkite dešinės rodyklės mygtuką, kad pridėtumėte pasirinkimą į **Pasirinkti organizaciniai mazgai** sąrašą.
1. Pasirinkti **Leisti fone** skirtuką.
1. Nustatykite **Paketo apdorojimas** pasirinktį į **Taip**, tada pasirinkite **Pasikartojimas**.
1. Dialogo lange **Apibrėžti pasikartojimą** **Pradžios data** lauke pasirinkite arba įveskite pasikartojimo pradžios datą.
1. **Pradžios laikas** lauke pasirinkite arba įveskite pasikartojimo pradžios laiką.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Pasirinkite **Be pabaigos datos** parinktį, jei nenorite, kad pasikartojimas pasibaigtų.
    - Pasirinkite **Pabaiga po** parinktį, jei pasikartojimas turėtų baigtis po tam tikro paleidimų skaičiaus. Jei pasirinksite šią parinktį, įveskite paleidimų skaičių.
    - Pasirinkite **Baigiasi iki** parinktį, jei norite, kad pasikartojimas baigtųsi iki konkrečios datos. Jei pasirinksite šią parinktį, pasirinkite arba įveskite datą.

1. Pasirinkite **Gerai**.
1. Pasirinkite **Gerai**.

## <a name="warranty-policies"></a>Garantijų politikos

Pardavus prailgintą garantiją, automatiškai sukuriamas garantinės strategijos objektas. Garantijos politikos numerius galite bendrinti su klientais, kad jie turėtų jų įsigytos garantinės prekės nuorodą. Į garantinės politiką pradžią įeina įsigaliojimo pradžia ir garantijos galiojimo data, sąlygos ir galimai garantinės prekės, kuriai parduota garantija, serijos numeris. 

> [!NOTE]
> Garantinės politikos ypatybės yra automatiškai sugeneruojamos, kai sukuriami politikų objektai. Šiuo metu jų negalima sukonfigūruoti arba redaguoti įprastiniu būdu.

Šioje lentelėje aprašomos garantijos politikos ypatybės ir jų vertės. „Commerce” būstinėje duomenų bazės lentelė pavadinta „GARANTIJOSPOLITIKA”.

| Ypatybės pavadinimas | Vertė | aprašymas |
|---------------|-------|-------------|
| PolitikosNumeris | Simbolių eilutė (daugiausiai 20 simbolių) | Garantijos politikos numeris |
| GarantinėsPrekėsId | Simbolių eilutė (daugiausiai 20 simbolių) | Galimai garantinės prekės ID |
| GarantiniųAtsargųPartijosId | Simbolių eilutė (daugiausiai 20 simbolių) | Galimai garantinės prekės atsargų partijos ID |
| GarantinioSerijosNumeris | Simbolių eilutė (daugiausiai 20 simbolių) | Galimai garantinės prekės serijos numeris |
| GarantinėsPrekėsĮvykdymoData | Data | Galimai garantinės prekės įvykdymo data |
| GarantinėsPrekėsId | Simbolių eilutė (daugiausiai 20 simbolių) | Garantinės prekės ID |
| GarantiniųAtsargųPartijosId | Simbolių eilutė (daugiausiai 20 simbolių) | Garantinės prekės atsargų partijos ID |
| GarantijųPardavimųData | Data | Garantinės prekės pardavimo data |
| GarantijosĮsigaliojimoData | Data | Garantijos politikos įsigaliojimo data |
| GarantijosGaliuojimoData | Data | Garantijos politikos galiojimo data |
| CustAccount | Simbolių eilutė (daugiausiai 20 simbolių) | Kliento kodas |
| Būsena | **Sukurta**, **Anuliuota**, **Galiojanti** arba **Pasibaigusi** | Garantijos politikos būsena |
| Pastabos | Simbolių eilutė (daugiausiai 255 simbolių) | Pastabos apie garantijos politiką, pavyzdžiui, sąlygas |

## <a name="frequently-asked-questions-faq"></a>Dažnai užduodami klausimai (DUK)

**Kodėl EKA nematau garantijos raginimo?**

Įsitikinkite, kad garantinė prekė surūšiuota kanale. Taip pat įsitikinkite, kad garantijų grupė sukonfigūruota taip, kad apimtų atitinkamą kanalą.

**Bandant pridėti garantiją esamoje operacijoje ir įvesti kliento užsakymo kvito numerį, kodėl nematau jokių operacijos eilučių elementų?**

Kvitus galite rasti tik, jei gavimo užduotis (G-užduotis) paleista įkelti kvitus „Commerce” būstinėje. Norėdami paleisti G-užduotį, eikite į **Mažmeninė prekyba ir komercija \>Mažmeninė prekyba ir IT prekyba \> Paskirstymo grafikas** , pasirinkite **P-0001** užduotį ir pasirinkite **Leisti dabar**.

**Kodėl garantijos funkcija taikoma tik nuolat leidžiamiems produktams?**

Garantija yra paslauga, teikiama konkrečiam, unikaliam produktui. „Dynamics 365” unikalų produktą galima identifikuoti tik pagal serijos numerį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Mažmeninės prekybos produktų nustatymas](set-up-retail-products.md)

[Asortimentų nustatymas](set-up-assortments.md)

[Numeracijų apžvalga](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
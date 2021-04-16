---
title: Darbo strategijos
description: Šis skyrius paaiškina, kaip nustatyti darbo strategijas.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 39a9ba00763fac220eff16bdd42aa07cc8e35ba4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838135"
---
# <a name="work-policies"></a>Darbo strategijos

[!include [banner](../includes/banner.md)]

Šis skyrius paaiškina, kaip nustatyti sistemą ir sandėlio valdymo mobiliųjų įrenginių programėlę taip, kad jos palaikytų darbo strategijas. Galite naudoti šią funkciją, kad greitai priregistruotumėte inventorių be kūrimo atidedamo darbo kūrimo, kai gaunate įsigijimo ar perdavimo užsakymus arba kai pabaigiate gamybos procesus. Ši tema pateikia bendrą informaciją. Išsamesnę informaciją, susijusios su licencijos numerio gavimu, rasite [Numerio lentelės gavimas naudojant sandėlio valdymo mobiliųjų įrenginių programėlę](warehousing-mobile-device-app-license-plate-receiving.md).

Darbo strategija valdo, ar sandėlio darbas yra kuriamas, kai ataskaitoje pagamintas elementas yra paskelbiamas baigtu, ar kai prekės yra gaunamos naudojant sandėlio valdymo mobiliųjų įrenginių programėlę. Jūs nustatote visas darbo strategijas nustatydami sąlygas, kai jos yra taikomos: darbo užsakymo tipai ir procesai, inventoriaus vieta ir (pasirinktinai) gaminiai. Pavyzdžiui, produkto įsigjimo užsakymas *A0001* turi būti gaunamas *RECV* vietoje sandėlyje *24*. Vėliau, produktas vartojamas kitame procese *RECV* vietoje. Šiuo atveju, galite nustatyti darbo strategiją siekiant apsaugoti atidedamą darbą nuo sukūrimo, kai darbuotojas praneša apie produktą *A0001* kaip gautą vietoje *RECV*.

> [!NOTE]
> - Tam, kad darbo strategija būtų aktyvi, privalote nustatyti mažiausiai vieną jai vietą **Inventoriaus vietose** **Darbo strategijų** puslapyje „FastTab“. 
> - Negalite nurodyti tos pačios kelių darbo strategijų vietos.
> - **Spausdinti etiketęl** parinktis mobilaus prietaiso meniu elementams neatspausdins licencijos numerio etiketės, nebent darbas bus sukurtas.

## <a name="activate-the-features-in-your-system"></a>Įjungti funkcijas jūsų sistemoje

Tam, kad visos šioje temoje aprašytus funkcijos būtų prieinamos jūsų sistemoje, įjunkite tolesnes dvi funkcijas [Funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Numerio lentelės gavimas patobulinimai
- Gaunamo darbo strategijos patobulinimai

## <a name="the-work-policies-page"></a>Darbo strategijų puslapis

Darbo strategijų nustatymui, eikite į **Darbo valdymas \> Parametrai \> Darbas \> Darbo strategijos**. Tuomet, kiekviename „FastTab“ nustatykite laukus, kaip aprašyta tolesniuose papildomuose skyriuose.

### <a name="the-work-order-types-fasttab"></a>Darbo užsakkymo tipai „FastTab“

**Darbo užsakymo tipai** „FastTab“, įtraukite visus darbo užsakymo tipus ir susijusius darbo procesus, kuriuose taiko darbo strategija. Tolesni darbo užsakymo tipai ir susiję darbo procesai palaikomi darbo strategijose.

| Darbo užsakymo tipas | Darbo procesas |
|---|---|
| Žaliavų paėmimas| Visi susiję procesai |
| Sudėtinis produktas ir šalutinis produktas atidėti | Visi susiję procesai |
| Baigtos atidedamos prekės | Visi susiję procesai |
| Perkelti gavimą | Gaunamas licencijos ženklas (ir atidėjimas) |
| Pirkimo užsakymai | <ul><li>Gaunamas licencijos ženklas (ir atidėjimas)</li><li>Gaunamas kraunamas elementas (ir atidėjimas)</li><li>Įsigijimo užsakymo eilutė (ir atidėjimas)</li><li>Gaunamas įsigijimo užsakymo elementas (ir atidėjimas)</li></ul> |

Darbo strategijos nustatymui, kuri taikoma keliems to paties darbo užsakymo tipo darbo procesams, įtraukite atskirą eilutę kiekvienam darbo procesui tinklelyje.

Kiekviena tinklelio linijai, nustatykite **Darbo sukūrimo metodo** lauką viename iš tolesnių verčių:

- **Niekada** – Darbo strategija apsaugos sandėlio darbą nuo sukūrimo pasirinkta, darbo užsakymo tipui ir susijusiam darbo procesui.
- **Kryžminis skirstymas** – Darbo strategija sukurs kryžminio skirstymo darbą naudodama strategiją, kurią pasirenkate **Kryžminio skirstymo strategijos pavadinimas** laukelyje.

### <a name="the-inventory-locations-fasttab"></a>Inventoriaus vietos „FastTab“

**Inventoriaus vietos** „FastTab“, įtraukite visas vietas, kuriose ši darbo strategija turi būti taikoma. Jei nėra susijusios jokios vietos su darbo strategija, darbo strategija nebus taikoma jokiems procesams.

Negalite nurodyti tos pačios kelių darbo strategijų vietos.

Galite naudoti sandėli vietą, kurią priskyrėte į vietos profilį, kai **Naudojamas licencijos numerio sekimas** prinktis yra išjungta. Tokiu atveju, darbuotojai tiesiogiai registruos turimą inventorių.

### <a name="the-products-fasttab"></a>Produktų „FastTab“

**Produktų** skirtuke, nustatykite **Produkto pasirinkimo** laukelį siekiant valdyti, kurie produktai strategijai turi būti taikomi:

- **Visi** – strategija turi būti taikoma visiems produktams.
- **Pasirinkta** – strategija turi būti taikoma tik produktams, esantiems tinklelyje. Naudokite įrankių juostą **Produktus** „FastTab“ siekiant įtraukti produktus į tinklelį ar pašalinti juos iš tinklelio.

## <a name="default-and-custom-to-locations"></a>Nustatytosios ir pasirinktos „į“ vietos

> [!NOTE]
> Tam, kad šiame skyriuje aprašyta funkcija būtų jūsų sistemoje, turite įjungti *Licencijos ženklo gavimo įtraukimus* ir *Darbo strategijos įtraukimą į vidinius darbus* funkcijas[Funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Anksčiau sistema palaikė tik numatytąją vietą, nurodytą kiekvienam sandėliui. Nepaisant to, mobilaus prietaiso meniu elementai naudoja tolesnius darbo sukūrimo procesus dabar suteiks **Naudokite nustatytuosius duomenis** parinktį. Ši parinktis leidžia jums priskirti pasirinktą „į“ vietą į vieną ar keletą meniu elementų. (Šią pasirinktį jau buvo galima naudoti kai kuriuose kituose meniu elementų tipuose.)

- Gaunamas licencijos ženklas (ir atidėjimas)
- Gaunamas kraunamas elementas (ir atidėjimas)
- Įsigijimo užsakymo eilutė (ir atidėjimas)
- Gaunamas įsigijimo užsakymo elementas (ir atidėjimas)

**Į vietą** parametrai meniu elemente viršija nustatytąją gaunamą vietą sandėlyje, visiems užsakymams, kurie yra apdorojami naudojant tą meniu elementą.

Mobilaus prietaiso meniu elemento nustatymui, kuris palaiko gaunamą tinkintą vietą, atlikite šiuos žingsnius.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Pasirinkite arba sukurkite meniu elementą, kuris naudoja vieną iš darbo sukūrimo procesų aprašytų anksčiau šiame skyriuje.
1. **Bendras** „FastTab“, nustatykite **Naudokite nustatytuosius duomenis** parinktį į **Taip**.
1. Veiksmų juostoje, pasirinkite **Nustatytieji duomenys**.
1. Skirtuke **Nystatytieji duomenis** puslapis, nustatykite tolesnes reikšmes:

    - **Nustatytųjų duomenų laukelis:** Nustatykite šį laukelį į *Į vietą*.
    - **Sandėlis:** Pasirinkite sandėlio paskirtį naudojamą su šiuo meniu elementu.
    - **Vieta:** Šis laukelis išvardyja visas vietų ID, kurie yra prieinami pasirinktam sandėliui. Nepaisant to, šio laukelio paremtrai neturi jokio poveikio. Dėl to, galite palikti jį tuščią. Nepaisant to, galite naudoti sąrašą patvirtinimui, kad ID, kurį privalote įvesti **Kietai užkoduotų verčių** laukelyje.
    - **Kietai užkoduota vertė:** Įveskite vietos ID gaunamai vietai, kuri taikoma šiam meniu elementui.

> [!TIP]
> Darbo strategija gali būti taikoma tik, jei visos gaunamos vietos yra išvardytos atitinkamame darbo strategijos nustatyme. Šis reikalavimas taikomas nepriklausomai nuo to, ar naudojate nustatytąją sandėlio gavimo vietą ar tinkintą „į“ vietą.

## <a name="example-scenario-warehouse-receiving"></a>Pavyzdinis scenarijus: Sandėlio gavimas

Visi produktai gauti *Prekybos užsakymo prekės gavime (ir atidėti)* procesu turi būti registruoti vietoje *FL-001* ir jie turi būti prieinami sandėlyje *24*. Nepaisant to, darbas neturi būti kuriamas. Visais kitais procesais gauti produktai (tai yra, naudojant kito mobilaus prietaiso meniu elementus) turi būti registruojami nustatytame sandėlyje gaunant vietą (*RECV*) ir darbas turi būti kuriamas kaip įprasta. (Šis scenarijus nerodo nustatytojo gauto nustatymo.)

Šis scenarijus reikalauja tolesnių elementų:

- Darbo strategija *Įsigijimo užsakymo elemento gavimas (ir atidėjimas)* procesas vietoje *FL-001* visiems produktams
- Mobilaus prietaiso meniu elementas turintis nustatytuosius duomenis ir kuris nustato **Į vietą** laukelį į *FL-001*

### <a name="prerequisites"></a>Būtinieji komponentai

Tam, kad šiame skyriuje aprašytas scenarijus būtų jūsų sistemoje, turite įjungti *Licencijos ženklo gavimo įtraukimus* ir *Darbo strategijos įtraukimą į vidinius darbus* funkcijas[Funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Šis scenarijus naudoja standartinius demonstracinius duomenis. Dėl to, jei norite dirbti su scenarijumi naudojant čia pateiktas vertes, įsitikinkite, privalote dirbti su sistema, kurioje demonstraciniai duomenys yra įdiegti. Taip pat, turite pasirinkti **USMF** juridinį subjektą.

### <a name="set-up-a-work-policy"></a>Nustatyti darbo strategiją

1. Eikite į **Sandėlio valdymą \> Nustatymai \> Darbas \> Darbo strategijos**.
1. Pasirinkite **Naujas**.
1. **Darbo strategijos pavadinimas** laukelyje, įveskite *Jokio įsigijimo elemento atidėjimo darbas*.
1. Pasirinkite **Įrašyti**.
1. **Darbo užsakymo tipai** „FastTab“, pasirinkite **Įtraukti** įtraukti eilutę į tinklelį ir tuomet nustatyti tolesnes vertes naujai eilutei:

    - **Darbo užsakymo tipas:** *Įsigijimo užsakymai*
    - **Darbo procesas:** *Įsigijimo užsakymo elementų gavimas (ir atidėjimas)*
    - **Darbo sukūrimo metodas:** *Niekuomet*
    - **Skirstymo doko strategijos pavadinimas:** Palikite šį laukelį tuščią.

1. **Atsargų vietos** „FastTab“, pasirinkite **Įtraukti** įtraukti eilutę į tinklelį ir tuomet nustatyti tolesnes vertes naujai eilutei:

    - **Sandėlis:** *24*
    - **Vieta:** *FL-001*

1. **Produktai** „FastTab“, nustatykite **Produkto pasirinkimas** laukelį į *Visi*.
1. Pasirinkite **Įrašyti**.

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a>Mobiliojo įrenginio meniu elementas skirtas pakeisti gaunamą vietą

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Kairiojoje juostoje, pasirinkite esamą **Įsigijimo gavimo** meniu elementas.
1. **Bendras** „FastTab“, nustatykite **Naudokite nustatytuosius duomenis** parinktį į *Taip*.
1. Pasirinkite **Įrašyti**.
1. Veiksmų juostoje, pasirinkite **Nustatytieji duomenys**.
1. **Nustatytieji duomenys** puslapyje, veiksmų juostoje pasirinkite **Naujas** siekiant įtraukti eilutę į tinklelį ir tuomet nustatyti tolesnes vertes naujai eilutei:

    - **Nustatytųjų duomenų laukelis:** *Į vietą*
    - **Sandėlis:** *24*
    - **Vieta:** Palikite šį laukelį tuščią.
    - **Kietai užšifruota vertė:** *FL-001*

1. Pasirinkite **Įrašyti**.

### <a name="receive-a-purchase-order-without-creating-work"></a>Gauti įsigijimo užsakymą be sukūrimo darbo

Pavyzdys šiame skyriuje rodo, kaip gauti prekybos užsakymo elementą be kūrimo darbo vietoje, kuri skiriasi nuo pasirinktos gavimo vietos, kuri yra nustatyta sandėlyje. Šis pavyzdys naudoja darbo strategiją ir mobilaus prietaiso elementą, kurį sukūrėte anksčiau šiame scenarijuje.

#### <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pirkimo užsakymą** nustatykite šias vertes:

    - **Pardavėjo paskyra:** *US-101*
    - **Vieta:** *2*
    - **Sandėlis:** *24*

1. Pasirinkite **Gerai** tam, kad uždarytumėte teksto laukelį ir atidarytumėte naują įsigijimo užsakymą.
1. **Įsigijimo užsakymo linijos** „FastTab“, nustatykite tolesnes vertes tuščiai eilutei:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *1*

1. Pasirinkite **Įrašyti**.
1. Pasižymėkite pirkimo užsakymo numerį.

#### <a name="receive-a-purchase-order"></a>Gauti įsigijimo užsakymą

1. Mobiliame prietaise, prisijunkite prie sandėlio *24* naudodami *24* kaip vartotojo ID ir *1* kaip slaptažodį.
1. Pasirinkite **Viduje**.
1. Pasirinkite **Įsigijimo gavimas**. **Vietos** laukelis turi būti nustatytas į *FL-001*.
1. Įveskite įsigijimo užsakymo numerį įsigijimo užsakymui, kurį sukūrėte ankstesnėje procedūroje.
1. **Elemento numerio** laukelyje, įveskite *A0001*.
1. Pasirinkite **Gerai**.
1. Lauke **Kiekis** įveskite *1*.
1. Pasirinkite **Gerai**.

Įsigijimo užsakymas dabar yra gaunamas, tačiau joks darbas su juo nesusiejamas. Turimos atsargos buvo atnaujintos ir kiekis *1* elemento *A0001* dabar yra prieinamas vietoje *FL-001*.

## <a name="example-scenario-manufacturing"></a>Pavyzdinis scenarijus: gamyba

Tolesniame pavyzdyje, esama dviejų gamybos užsakymų, *PRD-001* ir *PRD-002*. Gamybos užsakymas *PRD-001* turi operaciją pavadintą *Surinkimas*, kurioje gaminys *SC1* yra nusiunčiamas kaip baigtas į vietą *001*. Gamybos užsakymas *PRD-002* turi operaciją pavadintą *Dažymas* ir naudoja gaminį *SC1* iš vietos *001*. Gamybos užsakymas *PRD-002* taip pat naudoja žaliavas *RM1* iš vietos *001*. Žaliavos *RM1* yra laikomos sandėlio vietoje *BULK-001* ir bus paimtos į vietą *001* sandėlio darbui žaliavos medžiagos paėmimui. Paėmimo darbas yra generuojamas, kai produkcija *PRD-002* išleidžiama.

[![Sandėlio darbo strategijos](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)

Jums planuojant konfigūruoti sandėlio darbo strategiją šiame scenarijui, turėtumėte apsvarstyti tolesnius aspektus:

- Sandėlio darbas baigtų prekių atidėjimui nereikalaujamas, kai jūs darote ataskaitą apie *SC1* produktą kaip baigtą iš prekybos užsakymo *PRD-001* į vietą *001*. Tai yra dėl to, kad *Dažymo* veiksmas gamybos užsakymui *PRD-002* vartoja produktą *SC1* toje pačioje vietoje.
- Sandėlio darbas žaliavos medžiagos paėmimui būtinas tam, kad būtų judinamos žaliavų medžiagos *RM1* iš sandėlio vietos *BULK-001* į vietą *001*.

Toliau pateikiamas darbo strategijos pavyzdys, kurį galite nustatyti pagal šiuos apsvarstymus:

- **Darbo strategijos pavadinimas:** *Nėra jokio atidedamo darbo*
- **Darbo užsakymo tipai:** *Pabaigtų prekių atidėjimas* ir *Papildomas produktas ir šalia produkto atidėjimas*
- **Atsargų vietos:** Sandėlis *51* ir vieta *001*
- **Produktai:** *SC1*

Tolesnis pavyzdinis scenarijus pateikia žingsnis po žingsnio instrukciją nustatant sandėlio darbo strategiją šiame scenarijui.

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Pavyzdinis scenarijus: Skelbimas baigtais į vietą, kuri nėra licencijos numerio kontroliuojama

Šis scenarijus rodo pavyzdį, kuriame gamybos užsakymas yra raportuojamas kaip baigtas į vietą, kuri nėra licencijos numerio kontroliuojama.

Šis scenarijus naudoja standartinius demonstracinius duomenis. Dėl to, jei norite dirbti su scenarijumi naudojant čia pateiktas vertes, įsitikinkite, privalote dirbti su sistema, kurioje demonstraciniai duomenys yra įdiegti. Taip pat, turite pasirinkti **USMF** juridinį subjektą.

### <a name="set-up-a-warehouse-work-policy"></a>Sandėlio darbo strategijos nustatymas

Į sandėlio procesus ne visada įeina sandėlio darbas. Nustatant darbo strategiją, galite apsaugoti sukūrimo darbą žaliavų paėmimui ir padėjimui baigtiems gaminiams nustatyti gaminiui konkrečiose vietose.

1. Eikite į **Sandėlio valdymą \> Nustatymai \> Darbas \> Darbo strategijos**.
1. Pasirinkite **Naujas**.
1. **Darbo strategijos pavadinimas** laukelyje, įveskite *Jokio įsigijimo elemento atidėjimo darbas*.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. **Darbo užsakymo tipai** „FastTab“, pasirinkite **Įtraukti** įtraukti eilutę į tinklelį ir tuomet nustatyti tolesnes vertes naujai eilutei:

    - **Darbo užsakymo tipas** *Baigtų prekių atidėjimas*
    - **Darbo procesas:** *Visi susiję darbo procesai*
    - **Darbo sukūrimo metodas:** *Niekuomet*
    - **Skirstymo doko strategijos pavadinimas:** Palikite šį laukelį tuščią.

1. Pasirinkite **Įtraukti** darkart, kad įtrauktumėte antrą eilutę į tinklelį ir tuomet nustatytumėte tolesnes vertes naujoje eilutėje:

    - **Darbo užsakymo tipas:** *Papildomas gaminys ir šalia gaminio atidėjimas*
    - **Darbo procesas:** *Visi susiję darbo procesai*
    - **Darbo sukūrimo metodas:** *Niekuomet*
    - **Skirstymo doko strategijos pavadinimas:** Palikite šį laukelį tuščią.

1. **Atsargų vietos** „FastTab“, pasirinkite **Įtraukti** įtraukti eilutę į tinklelį ir tuomet nustatyti tolesnes vertes naujai eilutei:

    - **Sandėlis:** *51*
    - **Vieta:** *001*

1. **Produktai** „FastTab“, nustatykite **Produkto pasirinkimas** laukelį į *Pasirinkti*.
1. **Produktai** „FastTab“, pasirinkite **Įtraukti** tam, kad įtrauktumėte eilutę į tinklelį.
1. Naujoje eilutėje, nustatykite **Elemento numerio** laukelį į *L0101*.
1. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="set-up-an-output-location"></a>Išeigos vietos nustatymas

1. Eikite į **Organizacijos administravimas \> Resursai \> Resursų grupės**.
1. Kairėje juostoje, pasirinkite resurso grupę **5102**.
1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Išeigos sandėlis:** *51*
    - **Išeigos vieta:** *001*

1. Veiksmų srityje pasirinkite **Įrašyti**.

> [!NOTE]
> Vieta *001* nėra licencijos numerio kontroliuojama vieta. Galite nustatyti išeigos vietą, kuri nėra licencijos numerio kontroliuojama tik, jei taikoma darbo strategija vietai egzistuoja.

### <a name="create-a-production-order-and-report-it-as-finished"></a>Gamybos užsakymo sukūrimas ir jo skelbimas baigtu

1. Eikite į **Gamybos valdymas \> Gamybos užsakymai \> Visi gamybos užsakymai**.
1. Veiksmų juostoje, pasirinkite **Nauji gamybos užsakymai**.
1. **Sukurti gamybos užsakymą** teksto laukelyje nustatykite **Elemento numerio** laukelį į *L0101*.
1. Pasirinkite **Sukurti** tam, kad sukurtumėte užsakymą ir uždarytumėte teksto laukelį.

    Naujas gamybos užsakymas yra įtrauktas į tinklelį **Visi gamybos užsakymai** puslapyje.

    Laikykite naują gamybos užsakymą pasirinktą.

1. Veiksmų juostoje, **Gamybos užsakymas** skirtuke, **Procesas** grupėje pasirinkite **Apskaičiuoti**.
1. **Apskaičiavimo** teksto laukelyje perskaitykite apskaičiavimą ir tuomet pasirinkite **Gerai** teksto laukelio uždarymui.
1. Veiksmų juostoje, **Gamybos užsakymas** skirtuke, **Procesas** grupėje pasirinkite **Pradėti**.
1. **Pradėti** teksto laukelyje, **Bendra** skirtuke nustatykite **Automatinis BOM vartojimas** laukelį į *Niekada*.
1. Pasirinkite **Gerai** tam, kad įrašytumėte savo nustatymus ir uždarytumėte teksto laukelį.
1. Veiksmų juostoje, **Gamybos užsakymas** skirtuke, **Procesas** grupėje pasirinkite **Raportuoti kaip baigtą**.
1. **Raportuoti kaip baigą** teksto laukelyje, **Bendra** skirtuke nustatykite **Priimti klaidą** parinktį į *Taip*.
1. Pasirinkite **Gerai** tam, kad įrašytumėte savo nustatymus ir uždarytumėte teksto laukelį.
1. Veiksmų srityje, skirtuke **Sandėlis**, grupėje **Bendra** pasirinkite **Darbo informacija**.

Kai gamybos užsakymas yra raportuojamas kaip baigtas, joks darbas atidėjimui nėra sukuriamas. Toks elgesys atsitinka, nes darbo strategija yra apibrėžiama taip, kad apsaugotų darbą nuo sukūrimo, kai produktas *L0101* raportuojamas kaip baigtas į vietą *001*.

## <a name="more-information"></a>Daugiau informacijos

Daugiau informacijos apie mobiliojo įrenginio meniu elementus žr. [Mobiliųjų įrenginių nustatymas darbui sandėlyje](configure-mobile-devices-warehouse.md).

Išsamesnę informaciją apie licencijos numerio gavimą ir darbo strategijas rasite[Numerio lentelės gavimas naudojant sandėlio valdymo mobiliųjų įrenginių programėlę](warehousing-mobile-device-app-license-plate-receiving.md).

Daugiau informacijos apie gaunamos apkrovos valdymą rasite [Sandėlio pirkimų užsakymų gaunamos apkrovos tvarkymas](inbound-load-handling.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
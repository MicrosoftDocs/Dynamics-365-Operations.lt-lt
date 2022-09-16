---
title: Kaupimo profilis ir lygiai
description: Šiame straipsnyje pateikta informacija apie buferio šablonus ir lygius, kurie nustato minimalius ir maksimalius atsargų lygius, kurie turi būti kiekvieno iššiavimo taško atžvilgiu.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 57ee6206da926d0dbf62f562197538bfcdd41148
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428150"
---
# <a name="buffer-profile-and-levels"></a>Kaupimo profilis ir lygiai

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Nu identifikę savo iššiuos taškus (pagrindinius elementus, kuriuos strateginiu būdu išlaikysite atsargose), turite nuspręsti, kiek atsargų (buferio) išlaikysite kiekvienoje iš jų. Ši užduotis yra antrasis poreikio turimo medžiagų išteklių planavimo (DDMRP) veiksmas.

## <a name="buffer-levels-and-zones"></a>Buferio lygiai ir zonos

Kiekvienas atsargų buferis DDMRP nurodomas naudojant tris vertes: mažiausią kiekį, maksimalų kiekį ir užsakymo vietos. Šios vertės sudaro tris skirtumo zonas, kurios identifikuojamos pagal šiuos spalvų kodus:

- **Raudona zona** – sritis, mažesnė nei minimalus kiekis. Minimalus kiekis taip pat vadinamas "raudona viršuje", o jūsų planavimo strategija turi būti sukurta taip, kad užtikrinti, jog atsargų lygiai visada yra aukščiau šio taško.
- **Geltona zona** – sritis tarp minimalaus kiekio ir užsakymo vietos. Užsakymo vieta taip pat vadinama geltona viršuje. Pasiekus šį tašką, sistema turi būti persisakyta.
- **Žalia zona** – sritis tarp užsakymo vietos ir maksimalaus kiekio. Didžiausias kiekis dar vadinamas žaliais. Tai yra maksimalus lygis, iki kada atsargos bus papildytos.

Šioje iliustracijoje pateikiamos trys spalvinės zonos ir kaip jos susijusios su minimaliu kiekiu, maksimaliu kiekiu ir užsakymo vieta.

![DDMRP buferio zonos ir lygiai.](media/ddmrp-buffer-levels.png "DDMRP buferio zonos ir lygiai")

## <a name="calculating-the-buffer-zones"></a>Buferio zonų apskaičiavimas

Šiame skyriuje paaiškinama, kaip apskaičiuojamas kiekvienos buferio zonos aukštis.

Geltona zona paprastai skaičiuojama pirmiausiai. Ši zona nurodo kiekį, kurį naudojate nuo to momento, kai užsakymas dar nėra pristatytas. Kitaip tariant, tai yra numatomas suvartojimas per papildymo gamybos laiką. Jis skaičiuojamas naudojant šią lygtį:

- **Geltona zonos** = *vidutinis kasdienis naudojimas (ADU)* × Išsąstų *gamybos laikas*

Išsąstų *gamybos* laikas rodo laiką, reikalingą prekei pagaminti arba gauti, jei iššifravimo taškai visada yra atsargose. Paprastai jis yra daug trumpesnis nei kaupiamasis *gamybos laikas*, kuris įprastai naudojamas bendrojo planavimo metu. Tinkami buferio parametrai yra pagrindiniai, kurie užtikrina, kad iššiojimo taškai visada yra atsargose, bet nėra per daug sandėliuojami.

Raudona zona skaičiuojama naudojant šias lygtis:

- **Raudona bazinė** = *ADU* × *Gamybos laiko ×* gamybos *laiko koeficientas*
- **Raudonas saugos** = *raudonas* × *nuokrypio koeficientas*
- **Raudona zona –** = *raudonas pagrindinis raudonas* + *sauga*

Žalia zona skaičiuojama kaip maksimalus šių trijų lygčių rezultatas:

- *Mažiausias užsakymo kiekis*
- *ADU* × *užsakymo ciklas*
- *ADU* × *išsąstos gamybos* × ir *gamybos laiko koeficientas*

## <a name="calculating-average-daily-usage"></a>Skaičiuojamas vidutinis kasdienis naudojimas

Apskaičiuodama per dieną suvartojamą kiekį sistema naudoja vieną iš trijų būdų:

- **Vidutinis kasdienis naudojimas (buvusis)** – šis būdas pagrįstas faktiniu praėjusius suvartojimą.
- **Vidutinis kasdienis naudojimas (būsimas)** – šis būdas paremtas prognozuojamu būsimu suvartojimu.
- **Vidutinis kasdienis naudojimas (maišomas)** – šis būdas pagrįstas svertiniu buvusio ir prognozuojamo suvartojimo maišu.

### <a name="average-daily-usage-past"></a>Vidutinis kasdienis naudojimas (praeitis)

Praėję ADU apskaičiuojami kaip vidurkis, pridedant kiekius, kurie naudojami kiekvieną dieną nurodytu praėjusių dienų skaičiumi ir tada bendras kiekis padalintas iš dienų skaičiaus. Toliau pateikta iliustracija rodo, kaip šis būdas veikia, kai skaičiavimas atrodo praėjus trims dienoms.

![Vidutinio kasdienio naudojimo (buvusio) diagrama.](media/ddmrp-adu-past.png "Vidutinio kasdienio naudojimo (buvusio) diagrama")

Ankstesniame pavyzdyje, jei šiandien yra birželio 11 d. rytas, ADU per ankstesnes tris dienas (birželio 8 d., 9 ir 10 d.) yra 21.

- **ADU (praeitis)** = (29 + 11 + 23) ÷ 3 = 21

Skaičiuojant vidutinį dienos naudojimą (buvusią), atsižvelgiama į šias operacijas:

- Operacijos, kurios daugina prekės kiekį (lentelėje `inventtrans`, kur kiekis mažesnis už nulį)
- Operacijos, kurių būsena Užsakyta *, Rezervuota* *ir Rezervuota* faktiškai *,* Paimta *·*, *Atskaityta* arba *Parduota*
- Operacijos, datuoti pasirinktu atgaliniu laikotarpiu (vidutinis praėjusis dienos naudojimo laikotarpis)
- Operacijos, kurios nėra sandėlio darbas, sulaikavimas, pardavimo pasiūlymai arba išrašai (`WHSWork`, `WHSQuarantine``SalesQuotation`, ir )`Statement`
- Operacijos, kurios nėra perkėlimo žurnalai, o tos pačios padengimo dimensijos

### <a name="average-daily-usage-forward"></a>Vidutinis kasdienis naudojimas (pirmyn)

Naujam produktui gali būti, kad nėra buvusių naudojimo duomenų. Todėl galbūt jūs norėsite naudoti ir prognozuotas ADU, kurie bus pirmyn (pvz., pagal prognozuotą poreikį). Šiame pavyzdyje parodyta, kaip veikia šis būdas, kai skaičiavimas vyksta trimis dienomis į ateitį (įskaitant šiandien).

![Vidutinio kasdienio naudojimo (į priekį) diagrama.](media/ddmrp-adu-forward.png "Vidutinio kasdienio naudojimo (į priekį) diagrama")

Ankstesniame pavyzdyje, jei šiandien yra birželio 11 d. rytas, ADU, per kitas tris dienas (birželio 11 d., 12 ir 13 d.) yra 21,66.

- **ADU (pirmyn)** = (18 + 18 + 29) ÷ 3 = 21,66

Skaičiuojant vidutinį kasdienį naudojimą (į priekį) atsižvelgiama į šias operacijas:

- Prekės, kurios pagrindiniame plane pasirinkta prognozė, prognozės operacijos
- Operacijos, datuoti pasirinktu laikotarpiu į priekį (vidutinis kasdienis naudojimas į priekį)

### <a name="average-daily-usage-blended"></a>Vidutinis kasdienis naudojimas (sumaišytas)

Sujungti ADU sujungia vidutinį bitesį naudojimą ir vidutinį naudojimą į priekį, kaip parodyta toliau pateiktame pavyzdyje.

![Vidutinio kasdienio naudojimo (maišyto) diagrama.](media/ddmrp-adu-blended.png "Vidutinis kasdienis naudojimas (maišyto) diagrama")

Ankstesniame pavyzdyje, jei šiandien yra birželio 11 d. rytas, sulietas ankstesnės ir kitos trijų dienų (nuo birželio 8 d. iki 13 d.) ADU yra 21,33.

- **ADU, sulietas** = (*ADU praeities* + *ADU pirmyn*) ÷ 2<br>= (21 + 21,66) ÷ 2<br>= 21,33

## <a name="buffer-calculation-factors"></a>Buferio skaičiavimo koeficientai

Galite nurodyti du kiekvienos prekės koeficientus, pagal kuriuos būtų galima koreguoti, kokio dydžio turi būti raudona ir žalia zona. Tokiu būdu galite kompensuoti numatomą gamybos laiką ir poreikio nukrypimą.

![Gamybos laiko ir nuokrypio koeficientai.](media/ddmrp-zone-factors.png "Gamybos laiko ir nuokrypio koeficientai")

Pirmas koeficientas yra gamybos *laiko koeficientas*. Vertė yra dešimtainė vertė nuo 0 iki 1. Kuo ilgesnis gamybos laikas, tuo mažesnė vertė turi būti. Poreikio valdomas institutas rekomenduoja šiuos diapazonus:

- **Ilgas gamybos laikas:** 0.20–0.40
- **Vidutinis gamybos laikas:** 0.41–0,60
- **Trumpas gamybos laikas:** 0.61–1.00

Antrasis koeficientas yra *nuokrypio koeficientas*. Vertė yra dešimtainė vertė nuo 0 iki 1. Kuo didesnis poreikio nuokrypis, tuo mažesnė vertė turi būti. Poreikio valdomas institutas rekomenduoja šiuos diapazonus:

- **Mažas nuokrypis:** 0.20–0,40
- **Vidutinis nuokrypis:** 0.41–0,60
- **Didelis nuokrypis:** 0.61–1.00

## <a name="buffer-calculation-examples"></a>Buferio skaičiavimo pavyzdžiai

Šis pavyzdys tęsia pateisinimo gamybos pavyzdį, kuris pateikiamas [atsargų padėties nustatymo metu](ddmrp-inventory-positioning.md). Šiame pavyzdyje pasirinkote atsiejimo taškus, kurie sumažina gamybos laiką nuo 21 dienos iki penkių dienų, kaip parodyta šioje iliustracijoje.

![Atsietos gamybos laiko pavyzdys.](media/ddmrp-bom-decoupled-lead-time-example.png "Atsietos gamybos laiko pavyzdys")

Pavyzdžiui, tarkime, kad ADU apskaičiuotas kaip 23 vienetai, ir, kaip parodyta ankstesniame pavyzdyje, šis gamybos laikas yra penkios dienos. Naudodami šias vertes galite apskaičiuoti geltona zoną naudodami šią lygtį:

- **Geltona zona** = *ADU* × *Išsąstos gamybos laikas* = 115

![Geltona zonos skaičiavimo pavyzdys.](media/ddmrp-example-calc-yellow.png "Geltona zonos skaičiavimo pavyzdys")

Raudonos zonos skaičiavimas yra panašus į geltonas zonos skaičiavimus, bet jis yra tam, kad būtų galima nuokrypį ir gamybos laiką. Pavyzdžiui, tarkime, kad pažymėjote vidutinį gamybos laiką (koeficientas = 0,50) ir didelio poreikio nukrypimą (koeficientas = 0,8). Naudodami šias vertes kartu su komponentais iš geltona zonos lygties, galite apskaičiuoti raudoną zoną naudodami šias lygtis:

- **Raudona bazinė** = *ADU* × *gamybos laiko ×* *gamybos laiko koeficientas* = 57,5
- **Raudonas saugos** = *raudonas* × *nuokrypio koeficientas* = 46
- **Raudona zona** = *Raudona, pagrindinė* + *raudona,* sauga = 103,5

Sistema apvalins raudoną zoną iki 104 vienetų (jau), nes vienetai skaičiuojami skaičiais.

![Raudonos zonos skaičiavimo pavyzdys.](media/ddmrp-example-calc-red.png "Raudonos zonos skaičiavimo pavyzdys")

Į žalia zonos skaičiavimą įtraukti ir komponentai iš geltona zonos lygties, tačiau leidžia atlikti minimalų užsakymo dydį, užsakymo ciklą ir gamybos laiko koeficientą. Pavyzdžiui, tarkime, kad nėra užsakymo ciklo (todėl neturite jokių laiko apribojimų, susijusių su tuo, kaip dažnai užsakote), o minimalus užsakymo kiekis yra 10 vienetų. Tada žalia zona skaičiuojama kaip maksimalus šių trijų lygčių rezultatas:

- *Mažiausias užsakymo kiekis* = 10
- *ADU* × *užsakymo ciklas* = 0
- *ADU* × *Išsąstos gamybos* × *koeficientas* = 57,5

Sistema apvalins žalia zoną iki 58 vienetų (jau), nes vienetai suskaičiuoti skaičiuotais skaičiais.

![Raudonai žalios spalvos skaičiavimo pavyzdys.](media/ddmrp-example-calc-green.png "Žalia zonos skaičiavimo pavyzdys")

Šioje iliustracijoje apibendrinami šie zonos skaičiavimo rezultatai naudojant piltuvėlio grafinį vaizdą, kuris dažnai naudojamas DDMRP.

![Zonos skaičiavimo rezultatų suvestinė.](media/ddmrp-example-calc-summary.png "Zonos skaičiavimo rezultatų suvestinė")

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a> Dinaminis koregavimas

Dinaminis koregavimas leidžia taikyti poreikio *koregavimo koeficientą* per didelės arba mažos paklausos laikotarpius. Šis koeficientas visuose pasirinkto laikotarpio skaičiavimuose daugina ADU. Tada buferio zonos modifikuojami paeilių metu. Paprastai šį koeficientą taikysite sugeneruodami pirmines buferio vertes, kad per tam tikrą laiką ir reaguodamas į sąlygų keitimo sąlygas jas būtų galima suderinti. Ši užduotis yra trečiasis DDMRP veiksmas.

Pavyzdžiui, rugpjūčio mėnesį gali būti daugiau poreikio turėti daug produktų, nes žmonės atostogauti išeina. Todėl numatoma, kad pardavimas bus didesnis. Tokiu atveju galite pakeisti visų rugpjūčio **mėn.** *savaičių produkto poreikio koregavimo koeficiento vertę į 1,5*.

Tokiu būdu galite apskaičiuoti buferio vertes per tam tikrą laiką ir tada jas koreguoti pagal daugiau, nei tik sistemos turimos informacijos. Viso DDMRP diegimo metu, naujas buferio vertes skaičiuosite kiekvieną dieną, per paketinę užduotį, ir automatiškai priimsite vertes. Tada paleisite planavimą kaip paketinę užduotį ir peržiūrėsite suplanuotus užsakymus kiekvieną dieną, norėdami papildyti buferius.

## <a name="implement-buffers-in-supply-chain-management"></a>Vykdyti buferius tiekimo grandinės valdymo srityje

Šiame skyriuje aprašoma, kaip įdiegti savo buferio zonos strategiją Programoje "Microsoft"Dynamics 365 Supply Chain Management. Laikoma, kad jau atlikote analizes ir skaičiavimus, kurie nurodyti pirmoje šio straipsnio dalyje.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a> Nustatyti iššiamų taškų prekės buferius

Norėdami nustatyti iššiamo taško buferio vertes, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite išleistą prekę, kuri nustatyta kaip iššiavimo taškas. (Daugiau informacijos žr. [Atsargų padėties valdymas](ddmrp-inventory-positioning.md).)
1. Veiksmų srities skirtuke Planas **pasirinkite Prekės padengimas** **.**
1. Prekių padengimo **puslapyje** pasirinkite prekės padengimo įrašą, kuris sukuria iššipimo tašką. (Šiame įraše bus rodomas padengimo grupės, nustatytos sukurti atsišiejimo taškus, pavadinimas.)
1. Pasirinkite skirtuką **Bendra**.
1. Jei norite, kad sistema perskaičiuotų buferio vertes kiekvieną dieną arba kas savaitę, remdamasi savo pardavimo retrospektyva, prognozėmis ir padengimo grupės parametrais, atlikite šiuos veiksmus:

    1. Nustatykite **buferio verčių per tam** tikrą laiką parinktį *Taip*.
    1. Pranešimų langas praneša, kad jūsų rankiniai buferio parametrai (**minimalus**, **·** **užsakymo** vietos ir maksimalaus) bus nustatyti iš naujo, jei tęsite. Jei norite **palikti** naują parametrą, pasirinkite Taip.

    Arba jei jums labiau tinka skaičiuoti ar įvesti buferio parametrus tik vieną kartą, atlikite šiuos veiksmus:

    1. Nustatyti buferio **verčių per tam tikrą** laiką parinktį *Ne*.
    1. Nustatykite **laukus Minimalus**, **Užsakymo vieta** ir Maksimalus **,** kad būtų apskaičiuotos prekės buferio vertės, kaip aprašyta anksčiau šiame straipsnyje.

1. Norėdami baigti DDMRP skaičiavimų prekei nustatymą, nustatykite šiuos laukus:

    - **Užsakymo ciklas** – nurodykite dienų skaičių, kuris turi praeiti tarp prekės pirkimo užsakymų. Jei užsakymo apribojimų nėra *, vertę nustatykite kaip 0* (nulį). Šis laukas veikia maksimalų kiekio buferį, kaip anksčiau aptarta šiame straipsnyje.
    - **Vidutinis kasdienis** naudojimas – galite pasirinktinai įvesti įvertintą prekės ADU. Šis laukas naudojamas tik informaciniais tikslais. Paprastai vertė automatiškai apskaičiuojama kaip buferio skaičiavimų dalis.
    - **Užsakymo slenkstis** – nurodyti mažiausią kasdienio prekės pardavimo skaičių, kuris atitinka pardavimo slenkstį (beveik didelis poreikis). Sistema naudoja šį lauką didelio poreikio laikotarpiais suplanuotų užsakymų pakartotinio užsakymo kiekiui didinti. Daugiau informacijos rasite poreikio [planavimu](ddmrp-planning.md).

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a> Skaičiuoti arba įvesti susietą gamybos laiką

Prekėms, kuriose [pasirenkate](#set-up-buffers) leisti sistemai automatiškai apskaičiuoti buferio zonas, atlikite šiuos veiksmus, norėdami suskaičiuoti arba įvesti iššifravimo taškų prekės gamybos laiką.

1. Atidarykite savo **atsiejimo** taško prekės padengimo puslapį. (Daugiau informacijos žr. [Nustatykite iššiamų taškų prekės buferius](#set-up-buffers).)
1. Pasirinkite prekės padengimo įrašą, kuris sukuria atsiejimo tašką.
1. Pasirinkite skirtuką **Buferio** vertės.
1. Jei tinklelyje laikotarpiai nerodoma, veiksmų srities skirtuke Buferio **vertės** pasirinkite Įtraukti **laikotarpius**. Sistema užpildo tinklelį eilutėmis kiekvienam dienos ar savaitės laikotarpiui, atsižvelgiant į tai, **ar padengimo grupės laukas Min.,**[maks](ddmrp-inventory-positioning.md). ir pakartotinio užsakymo taškų laikotarpio nustatytas kaip *Kasdienis* ar *Savaitinis.* Sistema įtrauks pakankamai eilučių, kad pasiektų laiko ribas, nustatytas prekei priskirtai padengimo grupei.
1. Pasirinkti laikotarpį, kuriame norite skaičiuoti susietą gamybos laiką. (Paprastai šis laikotarpis yra laikotarpis, į kurį įtraukta šios dienos data.)
1. Veiksmų srities skirtuke Buferio **vertės pasirinkite** Skaičiuoti išsąstų **gamybos laiką**.
1. Dialogo lange **Skaičiuoti iš dalies susietą** gamybos laiką nustatykite šiuos laukus:

    - **KS** – pasirinkite komplektavimo specifikaciją (KS), kurią norite skaičiuoti.
    - **Data** – pasirinkite datą, kada norite vykdyti skaičiavimą. Galimų KS rinkinys bus filtruojamas, kad būtų rodomos tik pasirinktos datos aktyvios KS.
    - **Kiekis** – įveskite kiekį, kurio skaičiavimą norite vykdyti. Galimų KS rinkinys bus filtruojamas, kad būtų rodomos tik nurodytam kiekiui taikomos KS.

1. Pasirinkite **Gerai,** norėdami vykdyti skaičiavimą ir uždaryti dialogo **langą Skaičiuoti** gamybos laiką. Pasirinkto **laikotarpio paskaičiuotas** gamybos laiko stulpelis dabar rodo apskaičiuotą vertę.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a> Skaičiuoti arba įvesti vidutinį kasdienį naudojimą

Prekėms, kuriose [pasirenkate](#set-up-buffers) leisti sistemai automatiškai apskaičiuoti jūsų buferio zonas, atlikite šiuos veiksmus, norėdami apskaičiuoti arba įvesti atsiejimo taškų prekės ADU.

1. Atidarykite savo **atsiejimo** taško prekės padengimo puslapį. (Daugiau informacijos žr. [Nustatykite iššiamų taškų prekės buferius](#set-up-buffers).)
1. Pasirinkite prekės padengimo įrašą, kuris sukuria atsiejimo tašką.
1. Pasirinkite skirtuką **Buferio** vertės.
1. Jei tinklelyje laikotarpiai nerodoma, veiksmų srities skirtuke Buferio **vertės** pasirinkite Įtraukti **laikotarpius**. Sistema užpildo tinklelį eilutėmis kiekvienam dienos ar savaitės laikotarpiui, atsižvelgiant į tai, **ar padengimo grupės laukas Min.,**[maks](ddmrp-inventory-positioning.md). ir pakartotinio užsakymo taškų laikotarpio nustatytas kaip *Kasdienis* ar *Savaitinis.* Be to, numatytosios gamybos laiko koeficiento **ir** kintamumo **koeficiento** laukų vertės yra imamos iš padengimo grupės. Jei reikia, šias vertes galite redaguoti kiekvienoje eilutėje.
1. Pasirinkite laikotarpį, kurio ADU norite skaičiuoti.
1. Veiksmų srities skirtuke Buferio vertės **pasirinkite** Skaičiuoti vidutinį dienos **naudojimą**. Sistema bando surinkti duomenis, kurie reikalingi ADU skaičiavimui, kaip nustatyta padengimo [grupei](ddmrp-inventory-positioning.md).
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei reikiami duomenys yra, skaičiavimo rezultatai pridedami prie stulpelio Vidutinis **dienos** naudojimas. Šiuo atveju nereikia atlikti jokių veiksmų.
    - Jei reikiami duomenys negalimi, automatiškai nepridėta jokių verčių. Tokiu atveju rankiniu būdu įveskite kiekvienos eilutės, kurios buferio vertes planuojate apskaičiuoti, įvertintas vertes.

### <a name="calculate-and-apply-buffer-values"></a>Apskaičiuoti ir taikyti buferio vertes

Prekėms, kuriose pasirenkate leisti [sistemai](#set-up-buffers) automatiškai skaičiuoti buferio zonas, galite neautomatiniu būdu paleisti buferio verčių skaičiavimą, kuris atliktas šiais veiksmais.

1. Konfigūruokite atitinkamos iššifravimo taškų prekės buferio skaičiavimą, [...](#set-up-buffers)[apskaičiuokite](#calc-lead-time) arba įveskite atsietą gamybos laiką ir [apskaičiuokite](#calc-adu) arba įveskite vidutinį visų atitinkamų laikotarpių kasdienį naudojimą, kaip anksčiau aprašyta šiame straipsnyje.
1. Atidarykite savo **atsiejimo** taško prekės padengimo puslapį.
1. Pasirinkite skirtuką **Buferio** vertės, kuris jau turi rodyti laikotarpių sąrašą.
1. Pasirinkite laikotarpį, per kurį norite apskaičiuoti buferio vertes. (Paprastai šis laikotarpis yra šios dienos laikotarpis.) Jūsų pasirinktoje eilutėje jau turi būti ne nulinės vertės vidutinio **kasdienio naudojimo ir** išs **sususietainio gamybos laiko stulpeliuose**.
1. Redaguokite **vienos ar daugiau** eilučių poreikio koregavimo koeficiento lauką, jei reikia. Sistema taiys koeficientą vidutinio kasdienio **naudojimo vertei visuose** buferio skaičiavimuose, kur naudojama ši vertė. Šis faktorius leidžia koreguoti taip, kaip poreikis svyruoja pagal datą (pvz., švenčių dienomis ar sezoniniais elementais).
1. Veiksmų srities skirtuke Buferio vertės **pasirinkite Skaičiuoti min** ., **maks. ir neįvykdyto užsakymo taškų kiekius**. Sistema apskaičiuoja ir užpildo puslapio Prekių padengimas tinklelyje apskaičiuotą min., **·** **·** **apskaičiuotą užsakymo tašką ir apskaičiuotus maks**. stulpelius.**·**
1. Baigę peržiūrėti apskaičiuotas vertes, turite jas taikyti. Priešingu atveju, jos neturi įtakos. Kai taikote skaičiavimą vienai ar daugiau eilučių, **vertės iš apskaičiuoto min**., **·** **·** **apskaičiuoto užsakymo ir apskaičiuoto maks. laukų yra atitinkamai kopijuojamos į min**., **·** **užsakymo** tašką ir maks. Veiksmų srities skirtuko Buferio **vertės grupėje** Imtis veiksmų **pasirinkite** vieną iš šių mygtukų:

    - **Priimti visus skaičiavimus** – taikyti visas apskaičiuotas reikšmes tinklelyje.
    - **Priimti pasirinktų eilučių skaičiavimus** – taikyti apskaičiuotas vertes tik pasirinktoms eilutėms.
    - **Atmesti visus skaičiavimus** – atmesti visas apskaičiuotas minimalių kiekių, maksimalių kiekių ir pakartotinio užsakymo taškų tinklelyje vertes.
    - **Atmesti pasirinktų eilučių skaičiavimus** – atmeskite visas apskaičiuotas minimalių kiekių, maksimalių kiekių ir pasirinktų eilučių užsakymų taškų vertes.

### <a name="schedule-automatic-buffer-value-calculations"></a>Planuoti automatinius buferio vertės skaičiavimus

Visiškai nustatę DDMRP parametrus ir patvirtinę, kad jie veikia kaip tikėjotės, tikriausiai norėsite nustatyti paketinę užduotį periodiškai perskaičiuoti ADU ir susijusias buferio vertes pagal faktinio suvartojimo duomenis ir (arba) atnaujintas prognozes. Ši procedūra taikoma tik prekėms, kuriose pasirenkate leisti sistemai automatiškai [apskaičiuoti buferio zonas](#set-up-buffers).

Norėdami suplanuoti automatinius buferio vertės skaičiavimus, atlikite šiuos veiksmus.

1. Pereikite į bendrojo **planavimo \> bendrojo planavimo \> DDMRP buferio \> verčių apskaičiavimas**.
1. Dialogo lange **Apskaičiuoti buferio** vertes nustatykite šiuos laukus:

    - **Apskaičiuoti vidutinį kasdienį** naudojimą – nustatykite šią *pasirinktį* kaip Taip, norėdami kaskart, kai vykdoma užduotis, perskaičiuoti iššiamų taškų prekių ADU. Nustatyti, kad šis *skaičiavimas* būtų praleidžiamas. Paprastai šią pasirinktį reikia nustatyti kaip *Taip*.
    - **Apskaičiuoti susietą gamybos laiką** – nustatyti šią pasirinktį *kaip Taip,* kad kiekvieną kartą, kai vykdoma užduotis, būtų perskaičiuotas gamybos laikas. Nustatyti, kad šis *skaičiavimas* būtų praleidžiamas. Paprastai šią pasirinktį reikia nustatyti kaip *Taip*.
    - **Apskaičiuoti buferio** vertes – nustatykite šią pasirinktį *kaip Taip*, jei norite kiekvieną kartą, kai paleidžiama užduotis, perskaičiuoti buferio vertes. Nustatyti, kad šis *skaičiavimas* būtų praleidžiamas. Paprastai šią pasirinktį reikia nustatyti kaip *Taip*.
    - **Priimti min.,** maks. ir pakartotinio užsakymo taškų skaičiavimą – *nustatykite* šią pasirinktį kaip Taip, norėdami automatiškai patvirtinti ir taikyti perskaičiuotas buferio vertes kiekvieną kartą, kai vykdoma užduotis. Nustatykite, *kad* būtų netaikomos perskaičiuotos vertės. Šiuo atveju perskaičiuotos vertės neturi įtakos, nebent kas rankiniu būdu jas pritaikys vėliau kiekvieno produkto prekių **padengimo** puslapyje. Paprastai šią pasirinktį reikia nustatyti kaip *Taip*.
    - **Bendrasis planas** – pasirinkite bendrąjį planą, į kurį įtrauktos prekės, kurioms įtakos turės skaičiavimas. Skaičiavimas bus taikomas visoms plano filtro prekėms, kurias toliau apribos **šio** dialogo lango filtravimo parametrai.

1. Norėdami apriboti įrašų, kuriuose turi būti vykdoma ši paketinė užduotis, rinkinį, įrašuose, **kuriuose** reikia įtraukti "FastTab", pasirinkite Filtras, **·** **kad atidarytumėte dialogo** langą Užklausa. Šis dialogo langas veikia taip pat kaip ir kitiems tiekimo grandinės [valdymo fono](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams.
1. Fone " **FastTab" vykdyti** nurodykite kaip, kada ir kaip dažnai turėtų būti atliekami pasirinktų elementų skaičiavimai. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ [fono](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams.
1. Pasirinkite **Gerai,** norėdami įtraukti naują užduotį į paketinių užduočių eilę vykdymui.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Peržiūrėti ir perskaičiuoti visų prekių išjungtus gamybos laikus

Norėdami peržiūrėti ir perskaičiuoti visus juridinio subjekto (įmonės) gamybos laikus, atlikite šiuos veiksmus.

1. Pereikite prie **bendrojo planavimo \> bendrojo planavimo \> DDMRP \> prijungto gamybos laiko**.
1. Atsietame **gamybos laiko** puslapyje, naršykite ir filtruokite sąrašą, kurio reikia informacijai, kurios ieškote. Norėdami peržiūrėti dar daugiau informacijos apie prekę, pasirinkite jos saitą stulpelyje **Prekės** numeris.
1. Jei norite perskaičiuoti bet kurios prekės susietą gamybos laiką, pasirinkite prekę, **tada veiksmų srityje pasirinkite Skaičiuoti susietą** gamybos laiką. Atsiranda **dialogo langas Skaičiuoti susietą gamybos** laiką. Šis dialogo langas veikia taip pat, kaip ir skaičiuojant [tos pačios](#calc-lead-time)**prekės gamybos laiką prekių padengimo** puslapyje.

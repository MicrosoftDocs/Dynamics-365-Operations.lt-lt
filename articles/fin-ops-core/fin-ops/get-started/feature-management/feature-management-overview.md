---
title: Funkcijų valdymo apžvalga
description: Šioje temoje aprašomas priemonių valdymas ir kaip jį naudoti.
author: Peakerbl
ms.date: 01/10/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 6605fe68576ce80726438b60c1f1fbf3782d0934
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984464"
---
# <a name="feature-management-overview"></a>Funkcijų valdymo apžvalga

[!include [banner](../../includes/banner.md)]

Funkcijos įtraukiamos ir atnaujinamos kiekviename leidime. Funkcijų valdymo patirtis suteikia darbo sritį, kurioje galite peržiūrėti kiekviename leidime pristatytų funkcijų sąrašą. Tada galite naudoti darbo sritį priemonių dokumentacijai peržiūrėti ir funkcijoms įjungti ar išjungti.

## <a name="the-feature-management-workspace"></a>Funkcijų valdymo darbo sritis.

Galite atidaryti **Funkcijų valdymo** darbo sritį, pasirinkdami reikiamą plytelę ataskaitų srityje. Pasirodys puslapis, kuriame pateikiamas visų leidimų, kuriuos palaiko funkcijos valdymo patirtis, funkcijų sąrašas. 

Funkcijų sąraše pateikiama toliau nurodyta informacija.

- **Funkcijos pavadinimas** – pridėtos funkcijos aprašymas.
- **Įjungimo būsena** – simbolis nurodo, ar funkcija įjungta (varnelė), ar neįgalinta (tuščia), ar ji numatyta įjungti (laikrodis), ar yra privalomai įjungta (spyna). Čia rodomas parametras naudojamas visiems juridiniams subjektams. Atkreipkite dėmesį, kad net jei funkcija buvo įjungta, ją vis dar valdo sauga. Todėl funkcija bus prieinama tik tiems vartotojams, kurie turi prieigą prie jos, atsižvelgiant į jų saugos vaidmenį. Ji taip pat bus prieinama tik juridiniams subjektams, prie kurių vartotojas turi prieigą.
- **Įjungimo data** – diena, kurią funkcija buvo įjungta arba yra suplanuota ją įjungti.
- **Funkcija įtraukta** – data, kai funkcija buvo įdėta į jūsų aplinką. Ši data automatiškai įvedama, kai atnaujinate savo aplinką mėnesio išleidimo ciklais.
- **Funkcijos būsena** – dabartinė funkcijos ciklo būsena: **Peržiūra**, **Paleista** (rodoma kaip tuščia), **Pagal numatytuosius**, ir **Privaloma**. Vėliau šioje temoje bus įtrauktos valstijos. 
- **Modulis** – modulis, kurį paveikė nauja funkcija.

> [!NOTE]
> **Funkcijos būsenos** stulpelis įtrauktas kaip 10.0.21 versija.

Pasirinkus funkciją, išsamios informacijos srityje rodoma daugiau informacijos funkcijų sąrašo dešinėje. Srities viršuje matysite funkcijos pavadinimą, datą, kada funkcija buvo papildyta, modulį, kuris yra paveiktas funkcijos ir saitą **Sužinoti daugiau**. Pasirinkite šį saitą norėdami peržiūrėti funkcijos dokumentaciją. Jei dokumentacija nepasiekiama, būsite nukreipti į laikiną puslapį. Informacijos srityje taip pat yra laukas **Komentarai**, į kurį galite įtraukti savo komentarus apie funkciją.

Darbo srityje **Funkcijų valdymas** taip pat yra keli skirtukai ir kiekviename iš jų pateikiamas funkcijų sąrašas.

- **Nauja** – šis skirtukas rodo visas funkcijas, kurios buvo įtrauktos po paskutinio mėnesio atnaujinimo. Jei neįdiegėte kurio nors mėnesio atnaujinimo, skirtuke bus parodytos visos naujos funkcijos, kurios buvo įtrauktos po paskutinio jūsų atnaujinimo. Naujausios funkcijos rodomos sąrašo viršuje. Bendras naujų funkcijų skaičius taip pat rodomas plytelėje puslapio viršuje.
- **Neįjungta** – šiame skirtuke rodomos visos neįjungtos funkcijos. Naujausios funkcijos rodomos sąrašo viršuje. Be to, puslapio viršuje esanti išklotinė dalis rodo bendrą dabar išjungtas naujų funkcijų skaičių.
- **Suplanuota** – šiame skirtuke rodomos visos funkcijos, kurios suplanuotos įjungti ateityje. Funkcijos, kurios bus įjungtos anksčiausiai, rodomos sąrašo viršuje. Taip pat, laukelyje puslapio viršuje rodomas bendras suplanuotų funkcijų skaičius.
- **Visos** – šiame skirtuke rodomos visos funkcijos. Naujausios funkcijos rodomos sąrašo viršuje.

## <a name="feature-states"></a>Funkcijos valstybių
Priemonės gali pereiti iš vienos šalies į kitos, nuo jas supažindinant su funkcijų valdymu, kol produktas galiausiai tampa privalomas. Šiame skyriuje aprašomos galiojančios priemonių valstijos.

### <a name="preview-features-optional"></a>Funkcijų peržiūra (pasirenkama)

Produktų komandos gali nuspręsti iš pradžių pradėti naują priemonę kaip peržiūros priemonę. Peržiūros priemonės nėra įgalintos pagal numatytuosius nustatymus, todėl jos yra pasirenkamos. Priklausoma produktų komanda atnaujins funkcijas, kad būtų išleistos po to, kai jos bus sėkmingai išleistos per peržiūros laikotarpį.

> [!NOTE]
> Peržiūros funkcijoms taikomos konkrečios peržiūros [terminai ir sąlygos](https://go.microsoft.com/fwlink/?linkid=2105274). 

### <a name="released-features-optional"></a>Išleistos funkcijos (pasirinktinai)

Šių **priemonių būsenos** stulpelis yra tuščias. Priemonės, kurios iš pradžių pridėtos kaip išleistos, pagal numatytuosius nustatymus nėra įjungiamos, o įgalinimas yra pasirinktinis. Priemonės, kurios atnaujinamos iš peržiūros, išlaiko jų įgalinimo būseną.

### <a name="on-by-default-features-optional"></a>Pagal numatytąsias priemones (pasirinktinai)

Priemonės, kurios atnaujintos į Įjungta **pagal numatytuosius** nustatymus, yra įjungiamos pagal numatytuosius nustatymus, tačiau jas galima išjungti. Po to, kai funkcijos, kurias galima išjungti, **būsena** mažiausiai šešis mėnesius buvo paleista, tikimasi, kad jos pereis į šią būseną kitame stambiame leidime. Priemonės, kurios **pagal numatytuosius** nustatymus bus pereina prie [Kas nauja](../whats-new-changed.md) paleidimo temoje. Atnaujinimą inicijuoja produkto valdymo komanda.

> [!NOTE]
> Šios priemonės bus įgalintos automatiškai, todėl svarbu nustatyti, ar jūsų organizacija parengta šioms funkcijoms naudoti ar daugiau laiko reikia. Jei reikia daugiau laiko, gali reikėti laikinai išjungti šias funkcijas. Atkreipkite dėmesį, kad **pagal numatytuosius nustatymus** priemonės perėjimas prie On paprastai atliekamas stambiojo paleidimo metu, prieš tai, kai priemonė tampa **Privaloma**. Tada neturėsite pasirinkties išjungti funkcijos. 

### <a name="mandatory"></a>Privalomas

**Privaloma** yra numatoma galutinė priemonių būsena. Tai nurodo, kad priemonės yra įjungtos ir kad negalite jų išjungti nenaudodami „Microsoft". Pasirinktines priemones tikimasi padaryti privalomomis po dviejų pagrindinių leidimų. Kritinės priemonės gali būti išimties tvarka įvestos kaip privalomos.

## <a name="example-of-expected-feature-lifecycles"></a>Numatytų funkcijų ciklo pavyzdys

Priemonės, kurias galima išjungti ir kurios buvo pridėtos kaip išleistos ir pasirenkamos prieš arba kaip balandžio leidimo dalis, numatyta, kad bus pereiti prie **Pagla numatytuosius nustatymus** kitame spalio leidime. Tada tikimasi, kad šių metų balandžio mėnesį jos taps **privalomomis**.

Priemonė, kurią galima išjungti ir kurios buvo pridėtos kaip išleistos ir pasirenkamos prieš arba kaip balandžio leidimo dalis, numatyta, kad bus pereiti prie **Privaloma** kitų metų balandį.

## <a name="enable-a-feature"></a>Įgalinti funkcija

Jei funkcija neįjungta, informacijos srityje rodomas mygtukas **Įjungti dabar**. Šį mygtuką galite naudoti, jei norite įgalinti funkciją.

Kai kurių priemonių negalima išjungti po to, kai jas įgalinsite. Jei funkcija, kurią mėginate įjungti, negali būti įjungta, gausite įspėjimą. Šiuo metu galite pasirinkti **Atšaukti**, norėdami atšaukti operaciją ir palikti funkciją išjungtą. Tačiau, jei pasirinksite **Įgalinti** ir įjungsite funkciją, negalėsite jos išjungti vėliau.

Kai kurios funkcijos rodys pranešimą, kuriame bus pateikta papildoma informacija, prieš jas įjungiant. Šios funkcijos nurodomos geltonu įspėjamuoju simboliu. Turėtumėte atidžiai perskaityti papildomą informaciją, kad geriau suprastumėte, kas įvyks, kai funkcija bus įjungta. Tačiau vis tiek galite pasirinkti **Įjungti**, kad įjungtumėte funkciją.

Kai kurios funkcijos rodys pranešimą, kad funkcija negali būti įjungta, kol nebus imtasi veiksmų. Šios funkcijos nurodomos raudonu „X“ simboliu. Prieš įgalindami funkciją, turite atlikti apraše aprašytus veiksmus. Pavyzdžiui, jei negalite naudoti funkcijos, kol konfigūracijos raktas nebus išjungtas, pirmiausia turite išjungti konfigūracijos raktą, o tada grįžti į funkcijos valdymą, kad įgalintumėte funkciją.

Kai funkcija įjungta, informacijos srityje pasirodo pranešimas **Sužinokite daugiau**. Šis pranešimas nurodo, kad funkcija buvo įjungta, arba nurodo, kada funkcija suplanuota įjungti ateityje. Jis rodomas kiekvieną kartą, kai pasirenkate funkciją sąraše.

Funkcijos, kurios yra suplanuotos įjungti ateityje, rodomos skirtuke **Suplanuota**. Paketinis vykdymas jas įjungs nurodytos dienos vidurnaktį, atsižvelgiant į sistemoje nustatytą laiko juostą.

## <a name="reschedule-a-feature"></a>Iš naujo suplanuoti funkciją

Jei funkcija suplanuota įjungti ateityje, informacijos srityje atsiranda mygtukas **Planuoti**. Šį mygtuką galite naudoti, jei norite pakeisti lauko **Įjungimo data** vertę į kitą datą.

1. Pasirinkite suplanuotą funkciją, kurią norite perplanuoti, tada informacijos srityje pasirinkite **Planuoti**.
2. Pasirodžiusio dialogo lango lauke **Įjungimo data** nurodykite naują funkcijos įjungimo datą.
3. Pasirinkite **Įgalinti**, jei norite perplanuoti priemonę **Išjungti**, kad atšauktumėte planą.

## <a name="disable-a-feature"></a>Funkcijos išjungimas

Jei funkcija jau įgalinta, išsamios informacijos srityje atsiranda mygtukas **Išjungti**. Šį mygtuką galite naudoti, jei norite išjungti funkciją. Mygtukas **Išjungti** neveikia, jei funkcija negali būti išjungta ją įjungus. 

Kai funkcija įjungta, informacijos srityje pasirodo pranešimas **Sužinokite daugiau**. Šis pranešimas nurodo, kad funkcija dar nebuvo įjungta. Jis rodomas kiekvieną kartą, kai pasirenkate funkciją sąraše. Neįjungtos funkcijos rodomos skirtuke **Neįjungta**.

## <a name="features-that-must-be-enabled"></a>Funkcijos, kurias reikia įjungti

Kartais įtraukiama svarbi funkcija, kurią būtina įjungti automatiškai, kai naujinate. Šios funkcijos bus automatiškai įjungiamos lauke **Įjungimo data** nurodytą dieną. Naudojant šias funkcijas, informacijos srityje pasirodo pranešimas **Sužinokite daugiau**. Šis pranešimas nurodo, kad funkcija buvo įjungta arba nurodo, kada funkcija bus įjungta ateityje. Jis rodomas kiekvieną kartą, kai pasirenkate funkciją sąraše.

## <a name="enable-all-features"></a>Įgalinti visas funkcijas

Galite įjungti visas funkcijas pažymėdami mygtuką **Įjungti viską**. 

Kai pasirenkate **„Įjungti viską“**, parinktis pasirodys ten, kur jums reikia pateikti šią informaciją:

- Visų funkcijų, kurias reikia patvirtinti prieš jas įjungiant, sąrašas. Jei norite įjungti sąraše esančias funkcijas, pasirinkite parinktį **Taip**, skirtą mygtukui **Įjungti funkcijas, reikalaujančias patvirtinimo**.
- Pasirodys visų funkcijų, kurių negalima įjungti, sąrašas. Šios funkcijos nebus įjungtos.

Visos funkcijos, kurias galima įjungti, bus įjungtos. Jei jau planuojama fukciją įjungti ateityje, grafikas nepasikeis. 

## <a name="enable-all-features-automatically"></a>Automatinis visų funkcijų įjungimas

Tačiau, jei norite automatiškai įjungti visas naujas funkcijas, galite naudoti išplečiamąjį sąrašą, esantį darbo srities pavadinime, kad pakeistumėte tai, kas atsitinka, kai įtraukiamos naujos funkcijos.

- Pasirinkite **Įjungti naujas funkcijas automatiškai**, kad automatiškai įjungtumėte visas naujas į jūsų aplinką įtraukiamas funkcijas.
- Pasirinkite **Neįjungti naujų funkcijų automatiškai**, kad pagal numatytuosius parametrus visos naujos į jūsų aplinką įtraukiamos funkcijos būtų išjungtos.

Kai įjungiate visas funkcijas automatiškai, tai įgalins visas funkcijas, kurios būtų įjungtos spustelėjus mygtuką **Įjungti viską**. Tai neįjungs funkcijų, kurioms reikia patvirtinimo arba kurių negalima įjungti, kol nebus imtasi veiksmų.

## <a name="check-for-updates"></a>Tikrinti, ar yra naujinimų

Po kiekvieno atnaujinimo funkcijos pridedamos prie jūsų aplinkos. Tačiau galite rankiniu būdu patikrinti, ar yra naujinimų, spustelėdami mygtuką **Tikrinti, ar nėra atnaujinimų**. Bet kuri funkcija, kuri buvo įtraukta į sistemą po atnaujinimo, bus įtraukta į funkcijų sąrašą. Pavyzdžiui, jei suaktyvinta funkcija yra įjungta po išleidimo, tada galite ieškoti naujinimų ir funkcija bus įtraukta į jūsų sąrašą.

## <a name="assigning-roles"></a>Vaidmenų priskyrimas

Darbo sritį **Funkcijų valdymas** gali atidaryti sistemos administratoriai ir vartotojai, kuriems priskirtas vaidmuo Funkcijų tvarkytojas arba Funkcijų tikrintojas. Šie du vaidmenys buvo sukurti, kad būtų palaikoma funkcijų valdymo sąsaja. Funkcijų tvarkymo vaidmens vartotojai gali įjungti arba išjungti bet kokią funkciją. Jie taip pat gali atnaujinti funkcijos lauką **Komentarai**. Vartotojai, esantys funkcijos peržiūros vaidmenyje, gali tik peržiūrėti darbo sritį **Funkcijų valdymas**. Jie negali įjungti arba išjungti funkcijų.

Funkcijų tvarkymo vaidmuo ir funkcijų peržiūros vaidmuo neperrašo esamos saugos, kurią turi vartotojas. Jie paprasčiausiai valdo tai, ar vartotojas gali įjungti arba išjungti funkcijas. Jie nesuteikia prieigos prie pačios funkcijos.

## <a name="features-that-use-configuration-keys"></a>Funkcijos, naudojančios konfigūracijos raktus

Jei funkcija naudoja konfigūracijos raktą, bet konfigūracijos raktas nėra įjungtas, darbo srities **Funkcijų valdymas** galimų funkcijų sąraše funkcija nerodoma. Įjungę konfigūracijos raktą, turite atnaujinti funkcijų sąrašą naudodami elementą **Tikrinti naujinius**. Tada funkcija bus rodoma funkcijų sąraše.

Jei išjungsite konfigūracijos raktą, funkcija nebus pašalinta iš funkcijų sąrašo.

## <a name="data-entities"></a>Duomenų objektai

Duomenų objektas pavadinimu **Funkcijų valdymas** suteikia galimybę eksportuoti funkcijų valdymo parametrus iš vienos aplinkos ir importuoti juos į kitą aplinką. Šis objektas atnaujina tik esamas funkcijas. Objekto verslo logika taip pat padeda užtikrinti, kad atlikus importavimą bus taikomos tos pačios taisyklės, kurios naudojamos darbo srityje **Funkcijų valdymas**. Pavyzdžiui, negalite perrašyti privalomų funkcijų nustatymo pašalindami datą importavimo metu.

Toliau pateikiami pavyzdžiai apibūdina, kas atsitinka, kai duomenis importuojami naudojant objektą **Funkcijų valdymas**.

- Jei lauko **Įjungta** vertę pakeisite į **Taip**, ši funkcija bus įjungta, o lauke **Įjungimo data** bus nustatyta esama data.
- Jei lauko **Įjungta** vertę pakeisite į **Ne** paliksite lauką **Įjungimo data** tuščią, funkcija bus išjungta, o laukas **Įjungimo data** – išvalytas. Negalite išjungti privalomos funkcijos arba funkcijos, kurios negalima išjungti ją įjungus.
- Jei lauko **Įjungimo data** vertę pakeisite į būsimą datą, funkcija bus suplanuota įjungti tą dieną.
- Jei lauko **Įjungta** vertę pakeisite į **Taip**, o lauko **Įjungimo data** vertę pakeisite į būsimą datą, ši funkcija bus įjungti tą dieną. 
- Jei lauko **Įjungta** vertę pakeisite į **Ne**, o lauko **Įjungimo data** vertę pakeisite į būsimą datą, ši funkcija bus įjungti tą dieną.
- Jei funkcija įjungta, o jūs įtraukiate lauką **Įjungimo data**, kuris nustatytas į būsimą datą, funkcija lieka įjungta. Norėdami perplanuoti funkciją, turite pakeisti lauko **Įjungta** vertę į **Ne**.

## <a name="feature-management-and-flighting"></a>Funkcijų valdymas ir versijos

Funkcijų valdymas suteikia jums galimybę kontroliuoti funkcijas, kurios įtraukiamos į kiekvieną leidimą. Versijos suteikia galimybę „Microsoft“ komandoms išleisti funkcijas ribotam klientų skaičiui, kad funkcijos galėtų būti išbandytos ir patikrintos nepakenkiant visiems klientams. Funkcijų valdymas nekontroliuoja funkcijų versijų.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Funkcijų valdymo naudojimas, siekiant įgalinti ISV funkcijas arba pasirinktines funkcijas

Funkcijų valdymas šiuo metu negalimas, jei funkcijas pateikė nepriklausomi programinės įrangos tiekėjai (ISV) arba jei jos pasirinktinės funkcijos. Tačiau „Microsoft“ įtraukia daugiau funkcijų, kad funkcijų valdymas būtų patobulintas. Baigusi šiuos patobulinimus „Microsoft“ suteiks galimybę naudoti funkcijų valdymą tvarkant visas funkcijas ir pateiks funkcijų naujinimo instrukcijas.

## <a name="frequently-asked-questions-faq"></a>Dažnai užduodami klausimai (DUK)

### <a name="when-are-features-added-removed-or-changed"></a>Kada yra funkcijos pridedamos, pašalinamos, pakeistos? 
Funkcijos pridedamos, pašalinamos ir pakeičiamos naudojant kodų pakeitimus. Aplinkos reikia atnaujinti, kad šie pakeitimai būtų atlikti.

### <a name="does-a-feature-become-mandatory-automatically"></a>Ar funkcija automatiškai tampa privaloma? 
Ne, funkcija netampa privaloma automatiškai. Produkto komandos turi atlikti kodo pakeitimą.

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>Kodėl nėra konkrečios privalomumo įjungimo datos? 
Išleidimo laiko naujinimas yra kintamasis, aplinkos atnaujinimo laikas yra kintamasis, o klientai gali pasirinkti praleisti kai kuriuos naujinimus. Todėl konkrečias datas sunku nustatyti. 

### <a name="wheres-the-documentation-for-features-that-are-mandatory"></a>Kur pateikta privalomų funkcijų dokumentacija? 
Šią dokumentaciją pateikia kiekvienos „Dynamics 365” programos komanda. Dažnai šios funkcijos bus paminėtos [Kliento funkcijų būsenų atnaujinimuose](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states) arba [Pašalintos ar nerekomenduojamos funkcijos](../../../dev-itpro/migration-upgrade/deprecated-features.md). 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>Ar yra pranešimas ar signalas apie produktą, kuriam funkcija bus privalomai įjungta? 
Nėra pranešimo mechanizmo, susijusio su privalomos funkcijos įjungimu.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>Ar funkcijos kada nors yra įjungtos be kliento žinios? 
Taip, priemonės gali būti įgalintos be kliento žinių šiose situacijose:
- Funkcija yra perkeliama į **Pagal nutylėjimą**. Šią būseną vis tiek galima išjungti. 
- Priemonė atnaujinta į **Privaloma**. Šis pakeitimas įvyks tik kartu su stambiu paleidimu. Kritinės funkcijos, išimtimi, gali būti perkeltos į **Privalomą** bet kuriame atnaujinimą.

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>Kas yra testuojama funkcija ir kaip ji veikia funkcijų valdymą? 
Testuojamos funkcijos yra „Microsoft” valdomi realiojo laiko įjungimo/išjungimo mygtukai. Jų negali valdyti klientai, kitaip nei Funkcijų valdyme. 
- Kol jos yra testuojamos, privačios peržiūros funkcijos nebus pateiktos Funkcijų valdyme. Tam, kad gamyba vyktų, klientas turi sutikti, kad dalyvaus specialioje programoje.
- Viešoji peržiūra ir Išleistos (paprastai prieinamos) funkcijos bus išvardintos Funkcijų valdyme, nebent jų testavimas išjungtas. Funkcijos testavimo išjungimas laikomas paskutine išeitimi produktų komandos, jei randama kritinė problema ir dažnai sprendžiama kaip individualaus kliento atvejis.

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>Ar funkcijų testavimas kada nors yra išjungiamas be kliento žinios? 
Taip, jei funkcija veikia aplinkos funkcionalumą, jei ji nedaro įtakos, ji gali būti įjungta pagal numatytuosius nustatymus.

### <a name="how-can-feature-enablement-be-checked-in-code"></a>Kaip galima patikrinti, ar funkcija yra įjungta, naudojant kodą?
Naudokite metodą **isFeatureEnabled**, priklausantį klasei **FeatureStateProvider**, ir perduokite funkcijos klasės egzempliorių. Pavyzdys:

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>Kaip galima patikrinti, ar funkcija yra įjungta, naudojant metaduomenis?
Nustatyti, kad kai kurie metaduomenis yra susiję su funkcija, galima naudojant ypatybę **FeatureClass**. Turi būti naudojamas klasės pavadinimas, kuris yra naudojamas funkcijai, pvz., **BatchContentionPreventionFeature**. Šie metaduomenys matomi tik toje funkcijoje. Ypatybę **FeatureClass** gali turėti meniu, meniu elementai, sąrašo reikšmės ir lentelės / peržiūros laukai.

### <a name="what-is-a-feature-class"></a>Kas yra funkcijos klasė?
Funkcijų valdymo funkcijos apibrėžiamos kaip *funkcijų klasės*. Funkcijų klasė realizuoja **IFeatureMetadata** ir naudoja funkcijų klasės atributą, kad galėtų identifikuoti save funkcijų valdymo darbo srityje. Yra daug galimų funkcijų klasių pavyzdžių, kurių įjungimą kode galima patikrinti naudojant ypatybę **FeatureStateProvider** API, o metaduomenyse – naudojant ypatybę **FeatureClass**. Pavyzdys:

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>Kas yra IFeatureLifecycle, realizuotas kai kurių funkcijų klasių?
IFeatureLifecycle yra „Microsoft“ vidinis mechanizmas, skirtas nurodyti funkcijos ciklo etapą. Funkcijos gali būti:
- `PrivatePreview` – reikia, aktyvinti, kad būtų matoma.
- `PublicPreview` – rodoma pagal numatytuosius parametrus, bet su perspėjimu, kad funkcijos versija yra peržiūros.
- `Released` – visiškai išleista.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

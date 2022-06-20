---
title: Dvigubo naudojimo prekės
description: Šiame straipsnyje paaiškinama, kaip sekti produktus, kurie nurodyti kaip dvigubo naudojimo prekės, saugoti kiekvienos susijusios produkto ir paskirties šalies sertifikato numerius ir išspausdinti atitinkamus sertifikatų numerius atitinkamose SF, važtaraščiuose ir (arba) pardavimo užsakymuose.
author: t-benebo
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 02b154b9ea849c6b905d76edb256c4106b254acd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878909"
---
# <a name="dual-use-goods"></a>Dvigubo naudojimo prekės

[!include [banner](../includes/banner.md)]

Dvigubo naudojimo prekės yra dažniausiai elementai turintys civilinį ir karinį pritaikymą. Pavyzdžiui, cheminės medžiagos gali būti naudojamos kaip trąšos ar kaip sprogios medžiagos. Daugelis šalių turi specialius įstatymus taikomis dvigubo naudojimo prekių eksportavimui, importavimui ir transportavimui. Dėl to, svarbu, kad bendrovės įtrauktos į tarptautinę dvigubo naudojimo prekių prekybą sektų įvairius įstatymus ir sertifikatus.

Dvigubo naudojimo savybė padeda bendrovėms sekti dvigubo naudojimo prekes, kiekvieno produkto ir paskirties šalies parduotuvių sertifikatų numerius bei spausdinti galiojančius sertifikatų numerius reikiamose sąskaitose, pakavimo lipdukus ir (arba) prekybos užsakymus. Tai padeda užtikrinti, kad kai jūsų produktai yra siunčiami, jie visuomet turėtų atnaujintus sertifikatus.

Apgalvokite šiuos scenarijus:

1. **Dvigubo naudojimo šalies nustatymų** puslapis jūsų sistemoje rodo, kad siuntimui į Prancūziją reikalingas sertifikatas.
2. **Išleisto produkto informacijos** puslapis X-100 produktui rodo, kad tai dviejų naudojimų prekė. Kartu, kodas, kategorija, grupė ir režimas rodo eksportavimo valdymo klasifikavimą, kad produktas jiems priklauso.
3. **Dvigubo naudojimo sertifikatų** puslapis apima sertifikatą X-100 gaminiui, kai jis siunčiamas į Prancūziją. Šis sertifikatas baigia galioti 2020 m sausio 1 d.
4. 2020 m. birželio 17 d. sukuriate prekybos užsakymą kliento bendrovei, kuri yra Prancūzijoje ir užsakymas apima X-100 produktą.
5. Patvirtinus pardavimo užsakymą, sistema nustato šią informaciją:

    1. Ar užsakymas apima bet kokius produktus, kurie yra dvigubo panaudojimo prekės?
    2. Jei užsakymas apie dvigubo panaudojimo prekes, ar paskirties šalis reikalauja dvigubo panaudojimo sertifikatų?
    3. Jei šalis reikalauja dvigubo naudojimo sertifikatų, ar sertifikatas galioja dvigubo panaudojimo prekei paskirties šalyje?

6. Užsakymas apima X-100 produktą, produktas siunčiamas į Prancūziją ir Prancūzijos sertifikatas yra išduotas produktui. Nepaisant to, sertifikatas nebegalioja. Dėl to, gaunate šią perspėjančią žinutę: „Dvigubo panaudojimo sertifikatas vienam ar keliems dvigubo panaudojimo elementas šiame užsakyme negalioja. Ar norite tęsti patvirtinimą?“

Šiame straipsnyje paaiškinama, kaip konfigūruoti visus parametrus, reikalingus norint nustatyti dvigubo naudojimo prekes, ir palaikyti šį scenarijų.

## <a name="define-dual-use-requirements-for-each-relevant-country"></a>Nustatykite dvigubo panaudojimo reikalavimus kiekvienai būtinai šaliai

Skirtingos šalys turi skirtingus dvigubo prekių panaudojimo reikalavimams. Naudojate **Dvigubo panaudojimo šalies nustatymų** puslapį tam, kad sektumėte šalis, kurios reikalauja ar nereikalauja sertifikato: Informacija, kurią čia nurodote, yra patikrinama, kai kuriate prekybos užsakymus ir jums bus priminta apie būtinų sertifikatų pateikimą.

Informacijos apie dvigubo panaudojimo reikalavimų nustatymą skirtingoms šalims, atlikite šiuos veiksmus.

1. Eikite į **Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Dvigubo panaudojimo produktai \> Dvigubo panaudojimo šalies nustatymas**.
2. Pasirinkite esančią šalies sąranką jos redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujos šalies sąranką.
3. Naujosios ar pasirinktos šalies nustatyme, nustatykite šias vertes:

    | Laukas | aprašymas |
    |---|---|
    | Šalis/regionas | Pasirinkite šalį, kuriai sekate reikalavimus. |
    | Sertifikatas reikalingas | Pasirinkite šį žymimą laukelį šalims, kurios reikalauja sertifikato dvigubo panaudojimo prekėms. Išvalykite jį šalims, kurios sertifikato nereikalauja. |

## <a name="create-dual-use-categories"></a>Sukurkite dviejų panaudojimų kategorijas

Dvigubo panaudojimo prekės turi būti dažnai suskirstytos į kategorijas pagal jų eksportavimo valdymo klasifikavimo numerį (ECCN). ECCN yra skaitmeninis ir raidinis kodas, kuris suskirsto į kategorijas elementus pagal tokius faktorius kaip prekės ir technologija. **Dvigubo panaudojimo kategorijų** puslapis jums padeda sudaryti jūsų naudojamų kategorijų sąrašą ataskaitų rengimo tikslais.

Dvigubo panaudojimo kategorijų nustatymui atlikite šiuos žingsnius.

1. Eikite į **Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Dvigubo panaudojimo produktai \> Dvigubo panaudojimo kategorijos**.
2. Pasirinkite esančią šalies kategoriją jos redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujos šalies kategoriją.
3. Naujoje ar pasirinktoje kategorijoje nustatykite šias vertes:

    | Laukai | aprašymas |
    |---|---|
    | Dvigubo naudojimo kodas | Įveskite visą ECCN kodą (pavyzdžiui, *3A001*).|
    | Dvigubo naudojimo kategorija | Įveskite komercijos kontroliavimo sąrašą (CCL) ECCN kodo kategorijos daliai. Pavyzdžiui, ECCN kodui *3A001*, ši vertė yra *3*. |
    | Dvigubo naudojimo grupė | Įveskite ECCN kodo produkto grupės dalį. Pavyzdžiui, ECCN kodui *3A001*, ši vertė yra *A*. |
    | Dvigubo naudojimo režimas | Įveskite režimo kodą elementui. Šis kodas nustato priežastį, kodėl elementas yra klasifikuojamas kaip dvigubo naudojimo prekė. Pavyzdžiui, ECCN kodui *3A001*, ši vertė yra *001*. |

## <a name="apply-dual-use-categories-to-products"></a>Pritaikykite dvigubo panaudojimo kategorijas produktams

Produkto kaip dvigubo panaudojimo prekės nustatymui ir dvigubo panaudojimo kategorijos pritaikymui, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.
1. Pasirinkite ar sukurkite produktą, kad atidarytumėte jo **Išleisto produkto informacija** puslapį.
1. **Užsienio prekybos** „FastTab“, nustatykite **Dvigubo naudojimo produktų** parinktį į **Taip** tam, kad nustatytumėte esamą produktą kaip dvigubo panaudojimo prekę.
1. Nustatykite **Dvigubo panaudojimo kodo** laukelį, kuris taikomas dabartiniam produktui. (Jūs šį kodą nustatėte **Dvigubo panaudojimo kategorijų** puslapyje.)

Šis nustatymas yra tikrinamas, kai kuriate prekybos užsakymą.

## <a name="set-up-dual-use-certificates"></a>Dvigubo panaudojimo sertifikatų nustatymas

Naudojate **Dvigubo panaudojimo sertifikatų** puslapį, kad nustatytumėte ir valdytumėte būtinus dvigubo panaudojimo sertifikatus kiekvienam produktui ir šaliai. Galite sekti visų sertifikatų informaciją, tokių kaip šalies ir duomenų galiojimą. Galite taip pat nustatyti pasirinkimus tam, kad nurodytumėte, kur ši informacija turi būti atspausdinta. Pavyzdžiui, informacija gali būti atspausdinta sąskaitoje, pakavimo lipduke ir (arba) prekybos užsakyme. Šis nustatymas yra tikrinamas, kai kuriate prekybos užsakymą.

1. Eikite į **Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Dvigubo panaudojimo produktai \> Dvigubo panaudojimo sertifikatai**.
2. Pasirinkite esančią sertifikato sąranką jos redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujo sertifikato sąranką.
3. Naujam ar pasirinktam sertifikatui nustatykite šias vertes.

    | Laukas | Aprašymas |
    |---|---|
    | Prekės numeris | Pasirinkite dvigubo panaudojimo prekės elemento numerį, kuriam taikomas šis sertifikatas. |
    | Šalis/regionas | Paskirties šalis ar regionas, kuriame privalote naudoti šį sertifikatą. |
    | Sertifikato numeris | Skaičius pasirodantis sertifikate, kuris yra išduotas pardavėjui ar klientui. |
    | Galioja | Pasirinkite pirmą datą, kai esamas sertifikatas galioja.|
    | Galiojimas | Pasirinkite paskutinę datą, kai esamas sertifikatas galioja. |
    | Atspausdinkite sąskaitą | Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale. |
    | Atspausdinkite pakavimo lipduką | Pasirinkite žymimą laukelį, kad atspausdintumėte pakavimo lipdukų numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale. |
    | Prekybos užsakymo spausdinimas | Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį ar prekybos užsakymus, kurie yra siunčiami konkrečiai šaliai nurodytų duomenų intervale. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

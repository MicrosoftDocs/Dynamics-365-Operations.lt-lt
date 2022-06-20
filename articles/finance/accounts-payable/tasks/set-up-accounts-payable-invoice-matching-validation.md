---
title: Mokėtinų sumų SF gretinimo patvirtinimo nustatymas
description: Šiame straipsnyje pateikiama informacija, kaip nustatyti mokėtinų sumų SF gretinimo tikrinimą.
author: abruer
ms.date: 02/14/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86cc5cf688e3b66cf976fc7f507bd8f8df757612
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904965"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Mokėtinų sumų SF gretinimo tikrinimo nustatymas

[!include [banner](../../includes/banner.md)]

Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas. Jei jūsų juridinis subjektas seka išlaidas, pavyzdžiui, transportavimo, įsitikinkite, kad pasirinktas konfigūracijos raktas Išlaidos.  Mokėtinų sumų SF gretinimas yra tiekėjo SF, pirkimo užsakymo ir produkto gavimo kvito informacijos gretinimo procesas. Skirtumai tarp šių dokumentų vadinami gretinimo neatitikimais. Gretinimo nesutapimai lyginami su nurodytais leistinais nuokrypiais. Jei gretinimo nesutapimas viršija leistino nuokrypio procentą arba sumą, puslapiuose **Tiekėjo SF** ir **SF gretinimo informacija** rodomos gretinimo nuokrypio piktogramos.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Nustatykite, kokį SF gretinimo tikrinimą reikia naudoti
Galimi keturi skirtingi gretinimo tikrinimo tipai. 

- **Eilutės lygio gretinimas** – labiausiai įprastas gretinimo tipas yra eilučių gretinimas. Eilučių lygio gretinimas gali būti dvikryptis arba trikryptis. Puslapyje **Mokėtinos sumos** galima nurodyti juridinio subjekto numatytąjį eilučių lygio gretinimą. Dvikryptis gretinimas lygina sąskaitos faktūros prekės kainos informaciją su pirkimo užsakymo prekės kainos informacija. Trikryptis gretinimas papildomai lygina sąskaitoje faktūroje nurodytą kiekį su gretinamo produkto gavimo kvite nurodytu kiekiu.
- **SF bendrų sumų gretinimas** – gretinamos SF bendros sumos su pirkimo užsakymo bendromis sumomis. Šis SF gretinimo tipas apima mažiausiai informacijos, todėl šią parinktį galite naudoti norėdami nustatyti valdiklius, kurie minimizuotų darbuotojų laiką, kurio reikia peržiūrėti SF gretinimo informacijai. Lyginamos šešios bendros sumos, įskaitant tarpinę sumą, bendrą nuolaidos sumą, mokesčius, PVM, apvalinimą ir sąskaitos faktūros sumą. Sistema tikrins, ar bent viena iš šių verčių, esančių sąskaitoje faktūroje, nukrypsta nuo numatomų sumų viršydama priimtiną nuokrypį.
- **Mokesčių gretinimas** – sąskaitoje faktūroje esanti mokesčių informacija (sumos) gretinama su pirkimo užsakyme esančia mokesčių informacija (sumomis)
- **Eilutės prekės kainos bendrųjų sumų gretinimas** – šis gretinimo tipas naudingas įmonėms, kurios paprastai gauna kelias vienos pirkimo užsakymo eilutės sąskaitas faktūras. Jei paprastai kiekvienai pirkimo užsakymo eilutei gaunate tik vieną sąskaitą faktūrą, šis gretinimo tipas nereikalingas. Naudojant šį gretinimo tipą būtina, kad būtų įjungtas dvikryptis arba trikryptis gretinimas, tikrinantis, kad nebūtų viršijama grynoji suma atsižvelgiant į leistino nuokrypio procentus ir sumas.  Šis gretinimo tipas lygina kiekvienos sąskaitos faktūros eilutės ir visų laukiančių bei anksčiau užregistruotų sąskaitų faktūrų eilučių grynosios sumos kainos informaciją su atitinkamos pirkimo užsakymo eilutės grynąja suma. Grynoji suma nustatoma pagal šią formulę: (Vieneto kaina * Eilutės kiekis) + Eilutės mokesčiai – Eilutės nuolaidos. Kai kainos bendrosios sumos gretinamos pagal procentą, sistema lygina reikšmes naudodama operacijos valiutą. Kai kainos bendrosios sumos gretinamos pagal sumą, sistema lygina reikšmes naudodama apskaitos valiutą.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>SF gretinimo tikrinimo įgalinimo parametrų nustatymas
1. Eikite į **Mokėtinos sumos > Sąranka > Mokėtinų sumų parametrai**
2. Pasirinkite skirtuką **SF tikrinimas.**.
3. Pažymėkite arba atžymėkite žymės langelį **Įgalinti SF gretinimo tikrinimą**.
    * Pasirinkite, ar reikalauti patvirtinimo prieš registruojant SF, kurioje yra SF gretinimo nesutapimų. Jei nustatyta parinktis **Leisti įspėjant**, kai SF gretinimo nesutapimas viršys leistiną nuokrypį, tai bus parodyta vizualiai. Tačiau SF galėsite registruoti. Kad galėtumėte darbo eigas naudoti kartu su SF gretinimo tikrinimo funkcija, įsitikinkite, kad lauko **Registruoti SF su nesutapimais** reikšmė nustatyta kaip **Leisti įspėjant**, kad nereikėtų tvirtinti kelis kartus.  
    * Lauke **Automatiškai atnaujinti sąskaitos faktūros antraštės gretinimo būseną** pasirinkite, ar sistemai įvedant sąskaitos faktūros duomenis gretinimas bus atliekamas automatiškai. Rekomenduojamas nustatymas **Taip**, išskyrus atvejus, jei jums kyla duomenų įvedimo efektyvumo problemų. Išjungus automatinius atnaujinimus gali pagreitėti sistemos efektyvumas, nes SF gretinimo tikrinimas įvedant duomenis bus praleistas. Duomenų įvedimo klerkas turės rankiniu būdu atnaujinti SF gretinimo būseną, kad pamatytų SF gretinimo patvirtinimo rezultatus, kai tai nustatyta į **„Ne“**.  
4. Parinkties **SF bendrų sumų gretinimas** nustatymas.
5. Pažymėkite arba atžymėkite žymės langelį **Gretinti sąskaitos faktūros sumas**, kad sugretintumėte faktines sąskaitos faktūros bendras sumas su numatytomis bendromis sumomis.
    * Pasirinkite, ar rodyti piktogramą, jei SF gretinimo neatitikimas viršija leistiną nuokrypį. Galite pasirinkti rodyti piktogramą, kai teigiamas neatitikimas viršija leistiną nuokrypį arba kai teigiamas ar neigiamas neatitikimas viršija leistiną nuokrypį.  
    * Pvz., leistinas nuokrypis yra 5 proc., o pirkimo užsakymo bendroji SF suma yra 100,00. Todėl kainų gretinimo piktograma rodoma, jei SF bendroji suma viršija 105,00. Pažymėjus parinktį **Jei didesnis arba mažesnis nei leistinas nuokrypis**, piktograma taip pat rodoma, kai sąskaitos faktūros suma yra mažesnė nei 95,00.  
6. Lauke **Sąskaitos faktūros bendrų sumų leistino nuokrypio procentas** įveskite priimtiną leistino nuokrypio procentą. Ši vertė yra numatytoji įmonės vertė. Konkretiems tiekėjams šią vertę galima pakeisti puslapyje **Sąskaitos faktūros sumų leistini nuokrypiai**. Informacijos apie tai, kaip nepaisyti konkretaus tiekėjo SF bendrųjų sumų leistino nuokrypio procento, žr. šio straipsnio skyriuje "Nustatyti tiekėjų SF bendrųjų sumų gretinimo leistiną nuokrypį".
7. Parinkties **Kainos ir kiekio gretinimas** nustatymas.
8. Lauke **Eilučių atitikimo strategija** pasirinkite reikšmę, kurią norite naudoti kaip numatytąją juridinio subjekto, su kuriuo dirbate, strategiją. **Nebūtina** reiškia, kad nereikia tikrinti atskirų sąskaitos faktūros eilučių kainų su pirkimo užsakymo kainomis bei sąskaitos faktūros kiekių su važtaraščio kiekiais. **Dvipusis gretinimas** reiškia, kad reikia patvirtinti SF eilutes, tačiau tikrinamas tik pirkimo užsakymas ir tiekėjo SF dokumentai. Neatsižvelgiama į produkto gretinimo patvirtinimą. **Tripusis gretinimas** reiškia, kad SF grynoji vieneto kaina bus palyginta su pirkimo užsakymo grynąja vieneto kaina, o gretinamo produkto gavimo kiekis bus lyginamas su SF kiekiu.
9. Norėdami leisti, kad prekei, tiekėjui, tiekėjo ir prekės deriniui arba pirkimo užsakymo eilutei būtų taikomas kitoks gretinimo lygis, pasirinkite lauko **Leisti keisti atitikimo strategiją** reikšmę. Konkretaus tiekėjo, prekės ar tiekėjo ir prekės derinio juridinio subjekto eilučių atitikimo strategiją galima pakeisti puslapyje **Atitikimo strategija**.
    * Jei naudojate dvikrypčio gretinimo arba trikrypčio gretinimo eilučių atitikimo strategiją, puslapyje **Leistinas prekių kainų nuokrypis** galite nustatyti juridinio subjekto, prekių ir tiekėjų leistinų kainų nuokrypių procentus. Numatytasis juridinio subjekto dvikrypčio ir trikrypčio gretinimo leistino kainų nuokrypio procentas bus nustatytas kaip nulis. Kai tiekėjo SF palyginamos su pirkimo užsakymų informacija, ieškoma taikytino leistino kainų nuokrypio procento.   
10. Norėdami gretinti sąskaitų faktūrų eilučių prekių kainų bendras sumas, pasirinkite lauko **Gretinti kainų bendras sumas** reikšmę. Šis gretinimo tipas yra naudingas, kai tiekėjas už tą pačią pirkimo užsakymo eilutę siunčia kelias SF. Kiekvienos SF eilutės ir visų laukiančių bei anksčiau užregistruotų SF eilučių grynosios sumos kainos informaciją galite palyginti su atitinkamos pirkimo užsakymo eilutės grynąja suma.  Galimos parinktys: **Nėra**, **Procentas**, **Suma** arba **Procentas ir suma**.
11. Lauke **Pirkimo kainos viso leistino nuokrypio procentas** įveskite nuokrypio, kurį priimsite, procentą. Šis laukas pasiekiamas, kai lauke **Gretinti kainų bendras sumas** pasirinkta reikšmė **Procentas** arba **Procentas ir suma**.
12. Lauke **Pirkimo kainos visas leistinas nuokrypis** įveskite sumą apskaitos valiuta. Šis laukas pasiekiamas, kai lauke **Gretinti kainų bendras sumas** pasirinkta reikšmė **Suma** arba **Procentas ir suma**.
13. Lauke **Rodyti kainų bendrų sumų gretinimo piktogramą** pasirinkite, kada rodyti piktogramą, jei SF gretinimo nesutapimas viršija leistiną nuokrypį. Piktograma gali būti rodoma, kai teigiamas nesutapimas viršija leistiną nuokrypį arba kai teigiamas ar neigiamas nesutapimas viršija leistiną nuokrypį.
Pvz., leistinas nuokrypis yra 5 proc., o pirkimo užsakymo eilutės kainos bendroji suma yra 10,00. Todėl kainų gretinimo piktograma rodoma, jei SF eilutės kainos bendroji suma viršija 10,50. Pažymėjus parinktį **Jei didesnis arba mažesnis nei leistinas nuokrypis**, piktograma taip pat rodoma, kai sąskaitos faktūros eilučių kainų bendra suma yra mažesnė nei 9,50.
13. Nustatykite išlaidų **gretinimą**.
14. Norėdami sugretinti faktinius mokesčius su numatytais mokesčiais pagal pirkimo užsakymo informaciją, pažymėkite žymės langelį **Gretinti mokesčius**.

## <a name="set-up-unit-price-tolerance-percentages"></a>Leistinų prekių kainų nuokrypių procentų nustatymas
Norėdami apibrėžti leistino kainų nuokrypio procentus eikite į **Mokėtinos sumos > Sąranka > SF gretinimo sąranka > Leistini kainų nuokrypiai**. Jei naudojate dvikrypčio gretinimo arba trikrypčio gretinimo eilučių atitikimo strategiją, galite nustatyti juridinio subjekto, prekių ir tiekėjų leistinų kainų nuokrypių procentus. Kai tiekėjo SF palyginamos su pirkimo užsakymų informacija, ieškoma taikytino leistino kainų nuokrypio procento. Toliau pateikiama numatytoji ieškos tvarka.
* Lentelė / lentelė
* Lentelė / grupė
* Lentelė / viskas
* Grupė / lentelė
* Grupė / grupė
* Grupė / viskas
* Viskas / lentelė
* Viskas / grupė
* Viskas / viskas

Numatytasis juridinio subjekto leistino kainų nuokrypio procentas yra 0, jis taikomas visoms prekėms ir visoms sąskaitoms (Visi, Visi). Juridinio subjekto numatytojo leistino kainų nuokrypio įrašo panaikinti negalima.

Pagal numatytąjį nustatymą leidžiami ir neigiami kainų nesutapimai. Tačiau neigiamo skaičiaus negalima įvesti kaip leistino kainų nuokrypio procento. Norėdami sekti neigiamus leistinų kainų nuokrypių procentus, puslapio **Mokėtinų sumų parametrai** lauke **Rodyti prekių kainų gretinimo piktogramą** pažymėkite parinktį **Jei didesnis arba mažesnis nei leidžiamas nuokrypis**. Tada puslapyje **Leistini kainų nuokrypiai** įveskite leistinų kainų nuokrypių procentus.

## <a name="set-up-matching-policy-override"></a>Atitikimo strategijos keitimo nustatymas

Eikite **į mokėtinų sumų > SF > SF gretinimo nustatymo >** **atitikimo strategija, kad apibrėžtų numatytąjį eilučių atitikimo strategijos** **lauko įrašą pirkimo užsakymo** puslapyje. Ši sąranka neprivaloma. Naudokite šį puslapį norėdami nustatyti dviaigius prekių, tiekėjų ar prekių ir tiekėjų derinių gretinimą ar triaipipą gretinimą. Naudodami šiuos įrašus galite apibrėžti detalesnes atitikimo strategijas nei juridinio subjekto atitikimo strategija, kurią apibrėžėte puslapyje **Mokėtinų sumų parametrai**. Numatytoji juridinio subjekto eilučių atitikimo strategija taikoma visoms prekėms ir tiekėjams, išskyrus tuos, kuriems šiame puslapyje yra apibrėžta kita atitikimo strategija.

Šiame puslapyje pažymėkite **Atitikimo strategijos lygis**. Atitikimo strategijų hierarchijoje pasirinkite eilučių atitikimo strategijos lygį.

- **Prekė ir tiekėjas** – nurodykite šią atitikimo strategiją konkrečioms prekėms, pirktoms iš konkrečių tiekėjų.
- **Prekė** – nurodykite šią atitikimo strategiją konkrečioms prekėms, pirktoms iš bet kokio tiekėjo, išskyrus tas, kurios nurodytos lygyje Prekė ir tiekėjas.
- **Tiekėjas** – nurodykite šią atitikimo strategiją visoms prekėms, pirktoms iš konkrečių tiekėjų, išskyrus tas, kurios nurodytos lygyje Prekė ir tiekėjas.
  
Siekiant nustatyti naudojamą atitikimo strategiją taikoma toliau nurodyta hierarchija.
  *  Prekė ir tiekėjas
  *  Elementas
  *  Tiekėjas
  *  Juridinis subjektas
  
## <a name="set-up-invoice-totals-matching-tolerance-for-vendors"></a>Tiekėjų sąskaitų faktūrų bendrų sumų gretinimo leidžiamų nuokrypių nustatymas

Norėdami nurodyti konkretiems tiekėjams taikomus leistinus sąskaitų faktūrų bendrų sumų gretinimo nuokrypius eikite į **Mokėtinos sumos > Sąranka > SF gretinimo sąranka > Sąskaitos faktūros sumų leistini nuokrypiai**. Apskaičiuojant gretinimo reikšmes naudojamas sąskaitų faktūrų sumų leistino nuokrypio procentas iš tiekėjo sąskaitos, kuri tiekėjo sąskaitoje faktūroje yra nurodyta kaip užsakymo sąskaita. Jei tiekėjo sąskaitoje nėra nurodyto sąskaitų faktūrų sumų leistino nuokrypio procento, bus naudojamas puslapyje **Mokėtinų sumų parametrai** nurodytas juridinio subjekto sąskaitų faktūrų sumų leistino nuokrypio procentas.

1. Norėdami nurodyti atskiriems tiekėjams taikomus leistinus nuokrypius, pakeičiančius numatytąjį nuokrypį, pasirinkite **Tiekėjo sąskaita**.
2. Įveskite nuokrypio procentinį dydį, kurį priimsite šiam tiekėjui.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

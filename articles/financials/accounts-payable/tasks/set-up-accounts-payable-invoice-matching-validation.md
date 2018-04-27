--- 
title: "Nustatyti mokėtinų sumų SF sugretinimo patvirtinimą"
description: "Šiame įraše naudojama demonstracinė įmonė USMF."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9bf83269c34133509734691fd018ee703c40626
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Nustatyti mokėtinų sumų SF sugretinimo patvirtinimą

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Šiame įraše naudojama demonstracinė įmonė USMF. Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo. Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas. Jei jūsų juridinis subjektas seka išlaidas, pavyzdžiui, transportavimo, įsitikinkite, kad pasirinktas konfigūracijos raktas Išlaidos.  Mokėtinų sumų SF gretinimas yra tiekėjo SF, pirkimo užsakymo ir produkto gavimo kvito informacijos gretinimo procesas. Skirtumai tarp šių dokumentų vadinami gretinimo neatitikimais. Gretinimo nesutapimai lyginami su nurodytais leistinais nuokrypiais. Jei gretinimo neatitikimas viršija leistino nuokrypio procentą ar sumą, formoje Tiekėjo SF ir formoje SF gretinimo informacija rodomos gretinimo nuokrypio piktogramos.

1. Pasirinkite Mokėtinos sumos > Sąranka > Mokėtinų sumų parametrai.
2. Spustelėkite skirtuką SF tikrinimas.
3. Pažymėkite arba atžymėkite žymės langelį Įgalinti SF gretinimo tikrinimą.
    * Pasirinkite, ar reikalauti patvirtinimo prieš registruojant SF, kurioje yra SF gretinimo nesutapimų. Jei nustatyta Leisti įspėjant, kai SF gretinimo nesutapimas viršys leistiną nuokrypį, tai bus vizualiai parodoma. Tačiau SF galėsite registruoti. Norėdami kartu naudoti darbo eigas ir SF gretinimo tvirtinimą, įsitikinkite, kad laukas Registruoti SF su nesutapimais nustatytas į Leisti įspėjant, kad nereikėtų tvirtinti kelis kartus.  
    * Lauke Automatiškai atnaujinti sąskaitos faktūros antraštės atitikimo būseną pasirinkite, ar sistemai įvedant SF duomenis, gretinimas bus atliekamas automatiškai. Rekomenduojama nuostata yra Taip, nebent susiduriate su duomenų įvedimo efektyvumo problemomis. Išjungus automatinius atnaujinimus gali pagreitėti sistemos efektyvumas, nes SF gretinimo tikrinimas įvedant duomenis bus praleistas. Kai nustatyta Ne, duomenų įvedimo klerkas turės rankiniu būdu atnaujinti SF gretinimo būseną, kad matytų SF gretinimo tikrinimo rezultatus.  
4. Perjunkite dalies SF bendrųjų sumų gretinimas išplėtimą.
5. Pažymėkite arba atžymėkite žymės langelį Gretinti SF sumas, kad sugretintumėte faktines SF sumas su numatomomis sumomis.
    * Pasirinkite, ar rodyti piktogramą, jei SF gretinimo neatitikimas viršija leidžiamą nuokrypį. Galite pasirinkti rodyti piktogramą, kai teigiamas neatitikimas viršija leidžiamą nuokrypį arba kai teigiamas ar neigiamas neatitikimas viršija leidžiamą nuokrypį.  
    * Pvz., leidžiamas nuokrypis yra 5 proc., o pirkimo užsakymo bendroji SF suma yra 100,00. Todėl kainų gretinimo piktograma rodoma, jei SF bendroji suma viršija 105,00. Pažymėjus parinktį Jei didesnis arba mažesnis nei leidžiamas nuokrypis, piktograma taip pat rodoma, kai SF suma yra mažesnė nei 95,00.  
6. Lauke SF sumų leistino nuokrypio procentas įveskite skaičių.
7. Perjunkite dalies Kainos ir kiekio gretinimas išplėtimą.
    * Lauke Eilučių atitikimo strategija pasirinkite reikšmę, naudotiną kaip numatytoji juridinio subjekto, su kuriuo dirbate, strategija. „Nebūtina‟ reiškia, kad nereikia tikrinti atskirų SF eilučių kainų ir pirkimo užsakymo kainų bei SF kiekių ir važtaraščio kiekių. „Dvišalis atitikimas‟ reiškia, kad tikrinti SF eilutes reikia, bet tikrinant įtraukiami tik pirkimo užsakymo ir tiekėjo SF dokumentai. Produkto gavimo kvitas į gretinimo tikrinimus neįtraukiamas. „Trišalis atitikimas‟ reiškia, kad SF grynoji prekės kaina bus lyginama su pirkimo užsakymo grynąja prekės kaina, o atitinkantis produkto gavimo kvito kiekis bus lyginamas su SF kiekiu.  
    * Jei naudojate eilučių atitikimo strategiją Dvišalis atitikimas arba Trišalis atitikimas, puslapyje Leistinas prekių kainų nuokrypis galite nustatyti juridinio subjekto, prekių ir tiekėjų leistino kainų nuokrypio procentus. Kai tiekėjo SF palyginamos su pirkimo užsakymų informacija, ieškoma taikytino leidžiamo kainų nuokrypio procento.  
8. Lauke Eilučių atitikimo strategija pasirinkite parinktį.
    * Norėdami leisti prekei, tiekėjui, tiekėjo ir prekės deriniui arba pirkimo užsakymo eilutei taikyti skirtingą gretinimo lygį, pasirinkite reikšmę lauke Leisti nepaisyti atitikimo strategijos. Konkretaus tiekėjo, prekės ar tiekėjo ir prekės derinio juridinio subjekto eilučių atitikimo strategiją galima pakeisti puslapyje Atitikimo strategija.  
    * Norėdami sugretinti SF eilučių prekių bendrąsias kainas, pasirinkite reikšmę lauke Gretinti kainų sumas. Šis gretinimo tipas yra naudingas, kai tiekėjas už tą pačią pirkimo užsakymo eilutę siunčia kelias SF. Kiekvienos SF eilutės ir visų laukiančių bei anksčiau užregistruotų SF eilučių grynosios sumos kainos informaciją galite palyginti su atitinkamos pirkimo užsakymo eilutės grynąja suma.  
9. Lauke Gretinti kainų sumas pasirinkite parinktį.
10. Lauke Pirkimo kainos visas leistinas nuokrypis įveskite skaičių.
11. Perjunkite dalies Išlaidų gretinimas išplėtimą.
12. Norėdami sugretinti faktines išlaidas ir tikėtinas išlaidas, remdamiesi pirkimo užsakymo informacija, pažymėkite žymės langelį Gretinti išlaidas.
13. Uždarykite puslapį.



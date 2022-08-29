---
title: Užsakymų vykdymo perspektyva
description: Šiame straipsnyje pateikiama informacija apie užsakymų įsipareigojimus. Užsakymų įsipareigojimai suteikia galimybę patikimai įsipareigoti klientui laikytis pristatymo datų ir suteikia lankstumo, kad tų datų laikytumėtės.
author: Henrikan
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c835e25348b937c1dd68d8fa45b0264bd6815c23
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228273"
---
# <a name="order-promising"></a>Užsakymų vykdymo perspektyva

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie užsakymų įsipareigojimus. Užsakymų įsipareigojimai suteikia galimybę patikimai įsipareigoti klientui laikytis pristatymo datų ir suteikia lankstumo, kad tų datų laikytumėtės.

Užsakymų žadėjimas apskaičiuoja anksčiausias siuntimo ir gavimo datas ir yra paremtas pristatymo datos kontrolės būdu ir transportavimo dienomis. Galite pasirinkti iš šių pristatymo datos valdymo metodų:

- **Pardavimo vykdymo laikas** – pardavimo vykdymo laikas yra laikas tarp pardavimo užsakymo sukūrimo ir prekių siuntimo. Pristatymo datos skaičiavimas pagrįstas numatytuoju dienų skaičiumi, bet nenagrinėkime atsargų prieinamumo, žinomo poreikio ar suplanuoto tiekimo.
- **ATP (prieinamos atsargos)** – ATP yra prieinamas kiekis, kurį galima klientui pažadėti pristatyti konkrečią dieną. Skaičiuojant ATP, apimamos nefiksuotos atsargos, vykdymo laikai, suplanuoti gavimai ir išdavimai.
- **ATP + išdavimo laiko** rezervas – siuntimo data lygi ATP datai, pridėjus prekės išdavimo maržą. Išdavimo laiko rezervas yra laikas, reikalingas prekes paruošti siuntimui.
- **CTP (galimos pažadėti atsargos)** – prieinamumas skaičiuojamas naudojant išskleidimą. Jei naudojate planavimo optimizavimą, *CTP* pristatymo datos valdymo metodas neleidžiamas, todėl jį pasirinkus bus įvyko klaida skaičiuojant. Daugiau informacijos apie tai, kaip nustatyti ir naudoti CTP, ieškokite pardavimo užsakymo [pristatymo datų skaičiavimas naudojant CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).
- **CTP planavimo optimizavimui** – naudokite CTP skaičiavimą, kuris pateikiamas planavimo optimizavimo. Ši pasirinktis neturi jokios įtakos, jei naudojate įtaisytą bendrojo planavimo sistemą. Daugiau informacijos apie tai, kaip nustatyti ir naudoti CTP, ieškokite pardavimo užsakymo [pristatymo datų skaičiavimas naudojant CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

> [!NOTE]
> Atnaujinus prekybos užsakymą, užsakymo prognozės informacija yra tik naujinama, jei esantys užsakymo prognozės duomenys negali būt įgyvendinti kaip parodyta tolesniuose pavyzdžiuose:
>
> - **Pavyzdys 1**: Esamo užsakymo prognozavimo data yra liepos 20, bet dėl padidinto kiekio negalėsite pristatyti iki liepos 25. Kadangi esama data nebegalioja, užsakymo prognozavimas yra įjungiamas.
> - **2 pavyzdys**: Esama užsakymo vykdymo data yra liepos 20 d., tačiau dėl sumažino kiekio dabar galima pristatyti liepos 15 d. Tačiau, kadangi šiandienos data vis dar gali būti įvykdyta, užsakymo vykdymo terminas nėra suaktyvintas, o liepos 20 d. lieka užsakymo vykdymo data.

## <a name="atp-calculations"></a>ATP skaičiavimai

ATP kiekis skaičiuojamas naudojant "kaupiamąjį ATP" skaičiuojant į priekį". Pagrindinis šio ATP skaičiavimo būdo privalumas yra tai, kad juo galima tvarkyti atvejus, kai gavimų išdavimų suma yra didesnė už vėliausią gavimą (pavyzdžiui, kai, norint patenkinti poreikį, naudojamas ankstesnio gavimo kiekis). "Kaupiamoji ATP su "look-ahead" skaičiavimo metodu yra visi išdavimai, kol gautinas kaupiamasis kiekis viršija kaupiamąjį išduotinas kiekį. Todėl šis ATP skaičiavimo būdas įvertina, ar kokį nors ankstesnio laikotarpio kiekį galima naudoti vėlesniu laikotarpiu.

ATP kiekis yra nefiksuotų atsargų balansas pirmuoju laikotarpiu. Paprastai jis apskaičiuojamas kiekvienam laikotarpiui, kuriame suplanuotas gavimas. Programa apskaičiuoja ATP laikotarpį dienomis ir dabartinę datą ATP kiekiui apskaičiuoja kaip pirmą datą. Pirmą laikotarpį ATP apima turimas atsargas ir atėmus klientų užsakymus, kurie yra mokėtini ir laiku nesumokėti.

ATP apskaičiuojamos pagal šią formulę:

ATP = ankstesnio laikotarpio ATP + dabartinio laikotarpio gavimai – dabartinio laikotarpio išdavimai – kiekvieno būsimo laikotarpio grynasis išdavimo kiekis iki laikotarpio, kai visų būsimų laikotarpių gavimų suma (iki būsimo laikotarpio įskaitytinai) yra didesnė nei išdavimų suma iki būsimo laikotarpio įskaitytinai.

Atkreipkite dėmesį, kad ATP skaičiavime nėra informacijos apie galiojimo datą ir už ATP laiko ribų, kurių sistema tikisi, kai gali būti pažadėtas bet koks kiekis.

Kai daugiau nėra svarstytinų išdavimų arba gavimų, ATP kiekis šioms datoms yra toks pat kaip vėliausias apskaičiuotas ATP kiekis.

Jeigu atlikus ATP patikrinimą pateiktos ne visos prekei naudojamos dimensijos, jas dar galima nurodyti išdavime ir gavimuose. Šiuo atveju, skaičiuojant ATP, gavimai ir išdavimai turi būti sudedami pagal esamas dimensijas, kad būtų sumažintas ATP skaičiavime naudojamų gavimo ir išdavimo eilučių skaičius.

Rodomas ATP kiekis visada yra didesnis už 0 (nulį) arba jam lygus. Jeigu skaičiuojant gaunamas neigiamas ATP kiekis (pavyzdžiui, jeigu anksčiau pažadėtas kiekis viršija turimą kiekį), kiekis automatiškai nustatomas į 0.

### <a name="example"></a>Pavyzdys

**ATP atgalinio poreikio laiko ribos** laukas kontroliuoja, kaip toli atgal ieškoti atidėtų poreikio užsakymų ar atsargų išdavimų. **ATP atgalinio tiekimo laiko ribos** laukas kontroliuoja, kaip toli atgal ieškoti atidėtų tiekimo užsakymų ar atsargų gavimų. Pavyzdžiui, jei, skaičiuojant ATP, reikia atsižvelgti į užsakymus, atidėtus tik septyniomis dienomis, abu laukai turi būti nustatyti į **7**.

**ATP atidėto poreikio poslinkio laiko** ir **ATP atidėto tiekimo poslinkio laiko** laukai kontroliuoja, kada, skaičiuojant ATP, bus atsižvelgiama į atidėtą poreikį ar tiekimą. Pavyzdžiui, jei, skaičiuojant ATP, į atidėtą tiekimą ir poreikį reikia atsižvelgti poryt, abu laukai turi būti nustatyti į **2**. Reikšmė **2** reiškia, kad atidėto pirkimo užsakymo prekės kiekis, į kurį reikėtų atsižvelgti skaičiuojant ATP, bus vertinamas kaip galimos dvi dienos po dabartinės datos.

Toliau pateiktame pavyzdyje į **ATP atgalinio poreikio laiko ribos** ir **ATP atgalinio tiekimo laiko ribos** laukus įvedama **7**, o į **ATP atidėto poreikio poslinkio laiko** ir **ATP atidėto tiekimo poslinkio laiko** laukus įvedama **1**.

200 produkto vienetų pirkimo užsakymas, kuris turėjo būti gautas prieš tris dienas, dar negautas. Todėl 75 to paties produkto vienetų pardavimo užsakymo eilutė, kuri turėjo būti išsiųsta vakar, neišsiųsta.

Paskambina klientas ir nori užsakyti 150 to paties produkto vienetų. Kai patikrinate produkto prieinamumą, aptinkate, kad kitas 100 to produkto vienetų pirkimo užsakymas bus pristatytas po 10 dienų.

Sukuriate produkto pardavimo užsakymo eilutę ir kaip kiekį įvedate **150**.

Kadangi pristatymo datos valdymo metodas yra ATP, ATP duomenys apskaičiuojami taip, kad rastų anksčiausią įmanomą siuntimo datą. Pagal nuostatas atsižvelgiama į atidėtą pirkimo užsakymą ir pardavimo užsakymą, ir dabartinei datai gautas ATP kiekis yra 0. Rytoj, kai atidėtą pirkimo užsakymą tikimasi gauti, ATP kiekis apskaičiuojamas kaip didesnis nei 0 (šiuo atveju apskaičiuojama 125). Tačiau, po 10 dienų, kai tikimasi gauti papildomą 100 vienetų pirkimo užsakymą, ATP kiekis tampa didesnis nei 150.

Todėl pagal ATP skaičiavimą siuntimo data nustatoma po 10 dienų. Todėl klientui pasakote, kad pageidaujamą kiekį galima pristatyti po 10 dienų.

## <a name="ctp-calculations"></a>CTP skaičiavimai

CTP funkcija leidžia suteikti klientams realias datas, kada galite pateikti konkrečių prekių. Galima pateikti kiekvienos pardavimo eilutės datą, atsižvelgiant į turimas atsargas, gamybos pajėgumą ir transportavimo laiką.

CTP išplečia ATP funkcijas, nes tai pateikiama atsižvelgiant į pajėgumo informaciją. Kadangi ATP atsižvelgiama tik į medžiagų prieinamumą ir laiko neribotus pajėgumo išteklius, CTP atsižvelgiama į medžiagų ir pajėgumų prieinamumą. Todėl jis pateikia realesnius vaizdą apie tai, ar poreikis gali būti patenkintas per nurodytą laikotarpį.

CTP šiek tiek veikia kitaip, priklausomai nuo bendrojo planavimo modulio, kurį naudojate (planavimo optimizavimas arba įtaisytasis modulis). CTP planavimo optimizavimui šiuo metu palaiko tik CTP scenarijų, kuriuos palaiko įtaisytasis variklis, subgrupį.

Išsamesnės informacijos apie tai, kaip nustatyti ir naudoti CTP kiekvienam moduliui, ieškokite [apskaičiuoti pardavimo užsakymo pristatymo datas naudojant CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

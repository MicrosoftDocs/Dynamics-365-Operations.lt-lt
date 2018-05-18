---
title: "Užsakymų vykdymo perspektyva"
description: "Šiame straipsnyje pateikiama informacija apie užsakymų įsipareigojimus. Užsakymų įsipareigojimai suteikia galimybę patikimai įsipareigoti klientui laikytis pristatymo datų ir suteikia lankstumo, kad tų datų laikytumėtės."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 039bc5c572d204d9fa3e10a9f33cb4f4eb00b31c
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="order-promising"></a>Užsakymų vykdymo perspektyva

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie užsakymų įsipareigojimus. Užsakymų įsipareigojimai suteikia galimybę patikimai įsipareigoti klientui laikytis pristatymo datų ir suteikia lankstumo, kad tų datų laikytumėtės.

Užsakymų žadėjimas apskaičiuoja anksčiausias siuntimo ir gavimo datas ir yra paremtas pristatymo datos kontrolės būdu ir transportavimo dienomis. Galite pasirinkti iš toliau nurodytų keturių pristatymo datos kontrolės būdų.

-   **Pardavimo vykdymo laikas** – pardavimo vykdymo laikas yra laikas tarp pardavimo užsakymo sukūrimo ir prekių siuntimo. Pristatymo data skaičiuojama pagal numatytąjį dienų skaičių, neatsižvelgiant į atsargų prieinamumą, žinomą poreikį ar suplanuotą tiekimą.
-   **ATP (prieinamos atsargos)** – ATP yra prieinamas kiekis, kurį galima klientui pažadėti pristatyti konkrečią dieną. Skaičiuojant ATP, apimamos nefiksuotos atsargos, vykdymo laikai, suplanuoti gavimai ir išdavimai.
-   **ATP ir išdavimo laiko rezervas** – siuntimo data yra tokia pati, kaip ir ATP data ir prekės išdavimo laiko rezervas. Išdavimo laiko rezervas yra laikas, reikalingas prekes paruošti siuntimui.
-   **CTP (galimos pažadėti atsargos)** – prieinamumas skaičiuojamas naudojant išskleidimą.

## <a name="atp-calculations"></a>ATP skaičiavimai
ATP kiekis apskaičiuojamas naudojant „kaupiamojo ATP žvelgiant į ateitį“ būdą. Pagrindinis šio ATP skaičiavimo būdo privalumas yra tai, kad juo galima tvarkyti atvejus, kai gavimų išdavimų suma yra didesnė už vėliausią gavimą (pavyzdžiui, kai, norint patenkinti poreikį, naudojamas ankstesnio gavimo kiekis). „Kaupiamojo ATP žvelgiant į ateitį‟ skaičiavimo būdas apima visus išdavimus, kol kaupiamasis gautinas kiekis viršija kaupiamąjį išduotiną kiekį. Todėl šis ATP skaičiavimo būdas įvertina, ar kokį nors ankstesnio laikotarpio kiekį galima naudoti vėlesniu laikotarpiu.  

ATP kiekis yra nefiksuotų atsargų balansas pirmuoju laikotarpiu. Paprastai jis apskaičiuojamas kiekvienam laikotarpiui, kuriame suplanuotas gavimas. Programa apskaičiuoja ATP laikotarpį dienomis ir dabartinę datą ATP kiekiui apskaičiuoja kaip pirmą datą. Pirmą laikotarpį ATP apima turimas atsargas ir atėmus klientų užsakymus, kurie yra mokėtini ir laiku nesumokėti.  

APT apskaičiuojamos pagal tolesnę formulę.  

ATP = ankstesnio laikotarpio ATP + dabartinio laikotarpio gavimai – dabartinio laikotarpio išdavimai – kiekvieno būsimo laikotarpio grynasis išdavimo kiekis iki laikotarpio, kai visų būsimų laikotarpių gavimų suma (iki būsimo laikotarpio įskaitytinai) yra didesnė nei išdavimų suma iki būsimo laikotarpio įskaitytinai.  

Kai daugiau nėra svarstytinų išdavimų arba gavimų, ATP kiekis šioms datoms yra toks pat kaip vėliausias apskaičiuotas ATP kiekis.  

Jeigu atlikus ATP patikrinimą pateiktos ne visos prekei naudojamos dimensijos, jas dar galima nurodyti išdavime ir gavimuose. Šiuo atveju, skaičiuojant ATP, gavimai ir išdavimai turi būti sudedami pagal esamas dimensijas, kad būtų sumažintas ATP skaičiavime naudojamų gavimo ir išdavimo eilučių skaičius.  

Rodomas ATP kiekis visada yra didesnis už 0 (nulį) arba jam lygus. Jeigu skaičiuojant gaunamas neigiamas ATP kiekis (pavyzdžiui, jeigu anksčiau pažadėtas kiekis viršija turimą kiekį), programa automatiškai nustato kiekį į **0**.

### <a name="example"></a>Pavyzdys

**ATP atgalinio poreikio laiko ribos** laukas kontroliuoja, kaip toli atgal ieškoti atidėtų poreikio užsakymų ar atsargų išdavimų. **ATP atgalinio tiekimo laiko ribos** laukas kontroliuoja, kaip toli atgal ieškoti atidėtų tiekimo užsakymų ar atsargų gavimų. Pavyzdžiui, jei, skaičiuojant ATP, reikia atsižvelgti į užsakymus, atidėtus tik septyniomis dienomis, abu laukai turi būti nustatyti į **7**.  

**ATP atidėto poreikio poslinkio laiko** ir **ATP atidėto tiekimo poslinkio laiko** laukai kontroliuoja, kada, skaičiuojant ATP, bus atsižvelgiama į atidėtą poreikį ar tiekimą. Pavyzdžiui, jei, skaičiuojant ATP, į atidėtą tiekimą ir poreikį reikia atsižvelgti poryt, abu laukai turi būti nustatyti į **2**. Reikšmė **2** reiškia, kad atidėto pirkimo užsakymo prekės kiekis, į kurį reikėtų atsižvelgti skaičiuojant ATP, bus vertinamas kaip galimos dvi dienos po dabartinės datos.  

Toliau pateiktame pavyzdyje į **ATP atgalinio poreikio laiko ribos** ir **ATP atgalinio tiekimo laiko ribos** laukus įvedama **7**, o į **ATP atidėto poreikio poslinkio laiko** ir **ATP atidėto tiekimo poslinkio laiko** laukus įvedama **1**.  

200 produkto vienetų pirkimo užsakymas, kuris turėjo būti gautas prieš tris dienas, dar negautas. Todėl 75 to paties produkto vienetų pardavimo užsakymo eilutė, kuri turėjo būti išsiųsta vakar, neišsiųsta.  

Paskambina klientas ir nori užsakyti 150 to paties produkto vienetų. Kai patikrinate produkto prieinamumą, aptinkate, kad kitas 100 to produkto vienetų pirkimo užsakymas bus pristatytas po 10 dienų.  

Sukuriate produkto pardavimo užsakymo eilutę ir kaip kiekį įvedate **150**.  

Kadangi pristatymo datos kontrolės būdas yra ATP, skaičiuojami ATP duomenys, siekiant rasti anksčiausią galimą siuntimo datą. Pagal nuostatas atsižvelgiama į atidėtą pirkimo užsakymą ir pardavimo užsakymą, ir dabartinei datai gautas ATP kiekis yra 0. Rytoj, kai atidėtą pirkimo užsakymą tikimasi gauti, ATP kiekis apskaičiuojamas kaip didesnis nei 0 (šiuo atveju apskaičiuojama 125). Tačiau, po 10 dienų, kai tikimasi gauti papildomą 100 vienetų pirkimo užsakymą, ATP kiekis tampa didesnis nei 150.  

Todėl pagal ATP skaičiavimą siuntimo data nustatoma po 10 dienų. Todėl klientui pasakote, kad pageidaujamą kiekį galima pristatyti po 10 dienų.





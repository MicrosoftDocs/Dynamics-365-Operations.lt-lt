---
title: "Užsakymų vykdymo perspektyva"
description: "Šiame straipsnyje pateikiama informacija apie užsakymų įsipareigojimus. Užsakymų įsipareigojimai suteikia galimybę patikimai įsipareigoti klientui laikytis pristatymo datų ir suteikia lankstumo, kad tų datų laikytumėtės."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8aa0a58b03ee18e42ca7770ea3e22311c1ddba67
ms.lasthandoff: 03/31/2017


---

# <a name="order-promising"></a>Užsakymų vykdymo perspektyva

Šiame straipsnyje pateikiama informacija apie užsakymų įsipareigojimus. Užsakymų įsipareigojimai suteikia galimybę patikimai įsipareigoti klientui laikytis pristatymo datų ir suteikia lankstumo, kad tų datų laikytumėtės.

Užsakymų žadėjimas apskaičiuoja anksčiausias siuntimo ir gavimo datas ir yra paremtas pristatymo datos kontrolės būdu ir transportavimo dienomis. Galite pasirinkti iš toliau nurodytų keturių pristatymo datos kontrolės būdų.

-   **Pardavimo vykdymo laikas** -pardavimo laikas yra laikas nuo sukurti pardavimo užsakymą prekių siuntimą. Pristatymo datos skaičiavimus yra pagal nutylėjimą keletą dienų, ir mano turima prekių, žinomų paklausos arba planuojamos pasiūlos.
-   **ATP (galima pristatyti)** – ATP – elementą, kuris yra prieinamas ir gali pažadėjo pirkėjui tam tikrą dieną kiekis. Skaičiuojant ATP, apimamos nefiksuotos atsargos, vykdymo laikai, suplanuoti gavimai ir išdavimai.
-   **ATP ir išdavimo laiko rezervas** – siuntimo data yra tokia pati, kaip ir ATP data ir prekės išdavimo laiko rezervas. Išdavimo laiko rezervas yra laikas, reikalingas prekes paruošti siuntimui.
-   **CTP (galimos pažadėti atsargos)** – prieinamumas skaičiuojamas naudojant išskleidimą.

## <a name="atp-calculations"></a>ATP skaičiavimai
"Kaupiamasis ATP su išankstinė" metodu skaičiuojamas ATP kiekis. Šis ATP skaičiavimo metodo pagrindinis privalumas yra, kad jis gali dirbti kai aktualijas pajamų suma yra daugiau nei naujausias gavimo (pavyzdžiui, kai kiekis nuo ankstesnio prašymo gavimo dienos turi būti naudojamas patenkinti reikalavimą). "Kaupiamasis ATP su išankstinė" skaičiavimo metodas apima visus klausimus, kol gauti Kaupiamasis kiekis viršija bendrą kiekį, išduoti. Todėl šis ATP skaičiavimo būdas įvertina, ar kokį nors ankstesnio laikotarpio kiekį galima naudoti vėlesniu laikotarpiu.  

ATP kiekis yra nefiksuotų atsargų balansas pirmuoju laikotarpiu. Paprastai jis apskaičiuojamas kiekvienam laikotarpiui, kuriame suplanuotas gavimas. Programa apskaičiuoja ATP laikotarpį dienomis ir dabartinę datą ATP kiekiui apskaičiuoja kaip pirmą datą. Pirmą laikotarpį ATP apima turimas atsargas ir atėmus klientų užsakymus, kurie yra mokėtini ir laiku nesumokėti.  

APT apskaičiuojamos pagal tolesnę formulę.  

ATP = ATP ankstesnio laikotarpio + gavimus dabartiniu laikotarpiu – klausimus einamuoju laikotarpiu – grynieji klausimu kiekį kiekvienam ateities laikotarpiui iki laikotarpio, kai kvitus visiems būsimiesiems laikotarpiams, iki ir įskaitant būsimuoju laikotarpiu, suma viršija problemos suma iki ir įskaitant ateities laikotarpio.  

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

Kadangi pristatymo datos kontrolės būdas yra ATP, skaičiuojami ATP duomenys, siekiant rasti anksčiausią galimą siuntimo datą. Pagal parametrus, yra laikomi atidėtas pirkimo užsakyme, ir pardavimo užsakyme, ir nustatytas ATP kiekis šios dienos yra 0. Rytoj, kai atidėtas pirkimo užsakymą tikimasi gauti, ATP kiekis yra apskaičiuojamas kaip daugiau nei 0 (šiuo atveju ji apskaičiuojama kaip 125). Tačiau 10 dienų nuo dabar, kai papildomų pirkimo užsakymą už 100 vienetų tikimasi priimti ATP kiekis tampa daugiau nei 150.  

Todėl siuntimo data yra nustatytas 10 dienų nuo dabar, pagal ATP skaičiavimo. Todėl klientui pasakote, kad pageidaujamą kiekį galima pristatyti po 10 dienų.



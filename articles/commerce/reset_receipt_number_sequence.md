---
title: Kvitų numerių nustatymas iš naujo
description: Šiame straipsnyje aprašoma, kaip iš naujo nustatyti kvitų numerius, naudojamus įvairiems veiksmams pageidaujamą datą (pvz., finansinius metus arba kalendorinius metus).
author: ShalabhjainMSFT
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Application update 10.0.9
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, Commerce
ms.search.form: ''
ms.openlocfilehash: 3034a1b8f1a9f304b8d8803a7f906418321d81d9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272747"
---
# <a name="reset-receipt-numbers"></a>Kvitų numerių nustatymas iš naujo 

[!include [banner](includes/banner.md)]

> [!NOTE]
> Prieš naudojantis ta funkcija, būtina, kad pasirinktumėte **Nepriklausoma seka** ypatybę visiems kvitų tipams funkcijų profilyje. Be to, įrenginio sistemos laiko juosta, kurioje naudojamas EKA, turi sutapti su atitinkama parduotuvės laiko juosta. Atsižvelgiant į šiuos apribojimus, rekomenduojame nenaudoti šios funkcijos gamybai, kol mes dirbame, kad išspręstumėte šias problemas būsimoje versijoje. 

Mažmenininkai sugeneruoja kvitų numerius įvairiems veiksmams parduotuvėje, tokiems kaip atsiskaitymo grynaisiais operacijoms, grąžinimo operacijoms, klientų užsakymams, pasiūlymams ir mokėjimams. Nors mažmenininkai nustato savo kvitų formatus, kai kurios šalys ar regionai turi taisykles, kurios riboja šiuos kvitų formatus. Pavyzdžiui, šios taisyklės gali apriboti kvite esančių simbolių skaičių, reikalauti iš eilės gaunamų kvitų numerius, apriboti kai kuriuos specialiuosius ženklus arba reikalauti atkurti kvito numerius metų pradžioje. „Microsoft Dynamics 365 Commerce“ leidžia labai lanksčiai tvarkyti kvitų numerius, kad padėtų mažmenininkams įvykdyti norminius reikalavimus. Šiame straipsnyje paaiškinama, kaip naudoti gavimo numerių nustatymo iš naujo funkcijas.

„Commerce“ kvitų formatai gali būti raidiniai ir skaitiniai. Į juos galite įdėti ir statinį, ir dinaminį turinį. Statinį turinį sudaro abėcėlės simboliai, skaičiai ir specialieji simboliai. Dinaminį turinį sudaro vienas ar keli simboliai, pateikiantys tokią informaciją kaip parduotuvės numeris, terminalo numeris, data, mėnuo, metai ir skaičių sekos, kurios automatiškai didinamos. Formatai yra apibrėžti funkcionalumo profilio skyriuje **Kvito numeracija**. Šioje lentelėje aprašomi simboliai, pateikiantys dinaminį turinį.

| Simboliai | Aprašymas |
|------------|-------------|
| Š.          | Simbolis **S** naudojamas parduotuvės numeriui. Pavyzdžiui, jei parduotuvės numeris HOUSTON1, formatas **SSS** kvite rodomas kaip „ON1“. Formatas **SSSSS** kvite rodomas kaip „STON1“. |
| T          | Simbolis **T** naudojamas terminalo numeriui. Pavyzdžiui, jei terminalo numeris 0001, formatas **TTTT** kvite rodomas kaip „0001“. |
| K          | Simbolis **C** naudojamas darbuotojo ID numeriui. Pavyzdžiui, jei darbuotojo ID numeris 000160, formatas **CCCC** kvite rodomas kaip „0160“. |
| ddd        | Simboliai **ddd** reiškia metų dieną nuo 1 iki 366. Pavyzdžiui, sausio 15 d. formatas **ddd** kvite rodomas kaip „015“. |
| MM         | Simboliai **MM** naudojami dviejų skaitmenų mėnesiui. Pavyzdžiui, sausio mėnesį formatas **MM** kvite rodomas kaip „01“. |
| DD         | Simboliai **DD** naudojami dviejų skaitmenų dienai. Pavyzdžiui, sausio 15 d. formatas **DD** kvite rodomas kaip „15“. |
| YY         | Simboliai **YY** naudojami dviejų skaitmenų metams. Pavyzdžiui, bet kurį 2020 metų mėnesį formatas **YY** kvite rodomas kaip „20“. |
| \#         | Skaičių ženklas (**\#**) naudojamas nuosekliajam numeravimui. Pavyzdžiui, formatas **####** kvite rodomas kaip „0001“, „0002“, „0003“ ir t. t. |

Galite atkurti nuoseklųjį kvito numeravimą konkrečią dieną. Tada pirmajai operacijai, kuri įvyksta po pasirinktos atkūrimo datos po 12:00 val. ryto, sistema atkuria kvitų skaičių seką į 1. Taip pat galite nurodyti, ar atkurti nuoseklųjį kvito numeravimą tik vieną kartą, ar jį kartoti kiekvienais metais. Jei nurodomas numeravimas kiekvienais metais, nuoseklusis kvito numeravimas atkuriamas automatiškai kiekvienais metais, kol mažmenininkas nusprendžia jį sustabdyti. 

Norėdami įjungti atkūrimą, atlikite toliau nurodytus veiksmus.

1. Eikite į **„Retail and Commerce“\> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**.
1. „FastTab“ skyriuje **Kvito numeracija** pasirinkite **Nustatyti numerio atkūrimo datą**.
1. Išplečiamajame dialogo lange, lauke **Nustatyti datą** pasirinkite būsimą datą, kada turėtų įvykti atkūrimas.
1. Lauke **Nustatyti kvito tipą** pasirinkite **Vieną kartą** arba **Kasmet**.
1. Pasirinkite **Gerai**.

![Kvito atkūrimo datos pasirinkimas.](media/Enable_receipt_reset.png "Kvito atkūrimo datos pasirinkimas")

Pasirinkus datą, ji pasirodys stulpelyje **Kito kvito numerio atkūrimo data**. Atkūrimo data taikoma visų tipų kvitų gavimo operacijoms. Todėl atkuriama visų tipų kvitų numerių seka.

Atkūrimo dieną kvito numeris atkuriamas kiekvieno tipo pirmajai operacijai. Be to, funkcionalumo profilyje atkūrimo data perkeliama iš stulpelio **Kito kvito numerio atkūrimo data** į stulpelį **Einamojo kvito numerio atkūrimo data**. Šis pakeitimas rodo, kad jei registras nenaudojamas atkūrimo dieną, kvito numeris bus atkuriamas kitą kartą naudojant registrą *yra*. Pavyzdžiui, 2019 m. gruodžio 3 d. kaip atkūrimo datą pasirenkate **2020 m. sausio 1 d**. Sausio 1 d., kai registrai atlieka pirmą operaciją, atkuriamas kvito numeris. Tačiau vienas registras nenaudojamas gruodžio ir sausio mėnesiais, o vėliau pradedamas naudoti vasario mėnesį. Šiuo atveju, kadangi buvo nustatytas atkūrimas, to registro kvito numeris bus atkuriamas tada, kai registras atliks pirmąją operaciją vasario mėnesį.

Norėdami išvalyti būsimas atkūrimo datas, galite naudoti funkciją **Ištrinti atkūrimo dieną**. Tačiau jei atkūrimo diena įvyko praeityje, jos negalima anuliuoti. Todėl atkūrimas vis tiek bus atliekamas visuose registruose, kuriuose nebuvo atliktas naujas atkūrimas.

> [!NOTE]
> Priklausomai nuo jūsų pasirinktos atkūrimo datos ir kvito formato, gali būti, kad turėsite kvitų numerių dublikatus. Nors elektroninės kasos aparato (EKA) sistema gali valdyti šias situacijas, grąžinimų apdorojimo procesas užtrunka ilgiau, nes pardavėjai turi pasirinkti vieną iš dviejų kvitų dublikatų. Jei nebuvo pagalvota apie dublikatų kvitus, gali kilti kitų su duomenų valymu susijusių sunkumų. Todėl rekomenduojame naudoti dinaminius datos simbolius (pvz., **ddd**, **MM**, **DD** ir **YY**), kad išvengtumėte kvitų numerių dublikatų po atkūrimo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

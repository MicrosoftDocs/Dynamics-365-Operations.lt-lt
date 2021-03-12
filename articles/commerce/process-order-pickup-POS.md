---
title: Apdorokite kliento užsakymo paėmimus POS
description: Šioje temoje paaiškinamos funkcijos, kurios yra prieinamos prekybos vietos (POS) programoje siekiant sutvarkyti kliento užsakymo paėmimus.
author: Hhainesms
manager: annbe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2156542ed0932fab6fb4fa4035e009ad89eeb18f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003758"
---
# <a name="process-customer-order-pickups-in-pos"></a>Apdorokite kliento užsakymo paėmimus POS

[!include [banner](includes/banner.md)]

Kai [kliento užsakymas](customer-orders-overview.md) yra sukuriamas atsiėmimui iš parduotuvės, parduotuvės vartotojas gali naudoti prekybos vietos (POS) programą, kad pradėtų paimti inventorių. POS vykdys galutinio mokėjimo apėmimą, kaip būtina. Jis taip pat užbaigs inventorių ir finansinį publikavimą paimamiems kiekiams.

Jei esate parduotuvės vartotojas, galite atlikti paėmimą naudodami **Atšaukti užsakymą** veiksmą arba **Užsakymo įgyvendinimas** veiksmą POS. Norėdami padaryti **Paėmimo** veiksmą prieinamą, pirmiausia turite atlikti vieną šių veiksmų:

- Norėdami naudoti **Atšaukti užsakymą** veiksmą, ieškokite ir rinkitės užsakymą, kuris bus paimtas.
- Norėdami naudoti **Užsakymo įgyvendinimo** veiksmą, ieškokite ir rinkitės vieną ar kelias užsakymo eilutes.

Jei pasirinktas užsakymas ar jo eilutės nėra konfigūruotos paėmimui konkrečioje parduotuvėje arba jei užsakymas jau yra visiškai paimtas, **Paėmimo** veiksmas bus neprieinamas.

![Paėmimo veiksmas](media/pickupoperation.png)

„Microsoft Dynamics 365 Commerce“ versijoje 10.0.17 ir vėlesnėse **Pagerinta vartotojo patirtis užsakymo atsiėmimo tvarkymui prekybos vietoje** funkcija gali būti įjungta per funkcijos valdymą „Commerce“ būstinėje. Jei ši funkcija išjungta, vartotojai negali pasirinkti paimamų kiekių. Pagal nutylėjimą, visas užsakytas kiekis eilutei yra kiekis, kuris bus paimtas. Ši patirtis gali turėti problemų, nes vartotojai gali pamiršti pasirinkti kelias prekes atsiėmimiui jiems atliekant paėmimą per užsakymo įgyendinimą.

Funkcija **Pagerinta vartotojo patirtis atsiėmimui tvarkomo užsakymo prekybos vietoje** leidžia vartotojams labiau kontroliuoti prekių pasirinkimą, kurios bus paimtos ir jų atsiimamą kiekį. Vartotojai nerpivalo rinktis kiekvienos prekybos užsakymo eilutės įgyvendinamo užsakymo puslapyje prieš pasirinkdami **Atsiėmimas**. Visos atsiimti galimos prekės bus rodomos. Vartotojai gali nurodyti kelias eilutes atsiėmimui, net jei tik viena prekės eilutė yra pasirinkta.

Kai **Gerinti vartotojo patirtį atsiėmimo užsakymo tvarkymui prekybos vietoje** funkcija yra įjungta ir jūs renkatės **Atsiėmimo** veiksmą, pasirodo **Atsiėmimo** teksto laukelis. Jame galite rinktis prekes ir kiekius, kurie bus atsiimti. Pagal nutylėjimą, visas užsakytas kiekis, turintis inventorių su paimtu ir supakuotu statusu, yra laikomas galimu atsiimti. Pagal nutylėjimą, tas kiekis yra nustatyas atsiimamu kiekiu. Galite keisti įvestą kiekį su sąlyga, kad kiekis nėra 0 (nulis) ir neviršija viso atviro (neįtraukiamo į sąskaitą) kiekio pasirinktai eilutei.

![Atsiėmimo teksto laukelis](media/pickupselect.png)

Pasirinkus kiekius, kurie bus atsiimti ir tuomet pasirinkus **Atsiimti**, pasirodo transakcijos puslapis. Jei [omni kanalo mokėjimai](omni-channel-payments.md) funkcija yra įjungta ir esama iš anksto leistinų kredito kortelės mokėjimų faile, turite taikyti mokėjimą.

Transakcijos puslapyje, sistema skaičiuoja kiekius, kurie yra užbaigti pagal skaičiavimą bendro kiekio ir kuris yra pasirinktas prekių atsiėmimui ir tuomet paimamas iš anksčiau taikomų indėlių ar leistinų kredito kortelių mokėjimų. Privalote tvarkyti mokėjimą, kad užbaigtumėte atsiėmimo transakciją. Jei [ekrano išdėstymas](pos-screen-layouts.md) tansakcijos puslapyje yra konfigūruojamas taip, kad apimtų **Užbaigti transakciją** veiksmą ir joks kiekis nėra užbaigtas, gali užbaigti transakciją nepasirinkdami mokėjimo metodo. Jei **Užbaigti transakciją** veiksmas nėra prieinamas, galite rinktis **$0.00 laukiantį kiekį** nuorodą **Bendrų** juostoje, kad pabaigtumėte transakciją be poreikio pasirinkti mokėjimo metodą.

![Transakcijos puslapis kliento užsakymo atsiėmimo transakcijai](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>Atsiėmimo eilučių ar kiekių keitimas

Jei turite keisti atsiėmimo kiekį pasirinkę prekes, kurios bus atsiimtos, galite rinktis **Nustatyti kiekį**. Negalite nustatyti atsiėmimo kiekio lygaus **0** (nuliui) ar didint jo iki vertės, kuri viršija neįtrauktą į sąskaitą kiekį, kuris lieka užsakymo eilutėje. Norėdami pašalinti atsiėmimo eilutę iš transakcijos vežimėlio, rinkitės **Panaikinti transakciją**. Esama transakcija bus sustabdyta ir eiga **Atsiėmimo** veiksmui bus paleista iš naujo.

Jei **Gerinti vartotojo patirtį atsiėmimo užsakymo tvarkymui prekybos vietoje** funkcija yra įjungta, organizacijos gali įtraukti mygtuką **Keisti paėmimo eilutes** veiksmą į ekrano išdėstymą transakcijos puslapyje. Jums sukūrus atsiėmimo transakcijos vežimėlį POS ir pasirinkus prekes, galite pasirinkti **Keisti paėmimo eilutes**, jei privalote keisti paėmimo prekes, bet nenorite panaikinti visos transakcijos. Pasirodžiusiame teksto laukelyje **Keisti atsiėmimo eilutes**, galite keisti atsiimamas prekes ir kiekius. Transakcijos vežimėlis tuomet yra naujinamas, kad atsipindėtų jūsų keitimus.

![Keisti atsiimamų prekių teksto laukelį](media/pickupchange.png)

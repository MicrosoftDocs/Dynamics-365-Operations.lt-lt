---
title: Pristatymo grafikai
description: "Naudojant pristatymo grafikus galima sekti užsakymo eilučių kiekį, kai išsiunčiate kelis pardavimo užsakymus, pardavimo pasiūlymus ar pirkimo užsakymus."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 84ae84a567e5f45bc0b20538d04917c6feb21336
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="delivery-schedules"></a>Pristatymo grafikai

[!include[banner](../includes/banner.md)]


Naudojant pristatymo grafikus galima sekti užsakymo eilučių kiekį, kai išsiunčiate kelis pardavimo užsakymus, pardavimo pasiūlymus ar pirkimo užsakymus.

Naudokite pristatymo grafiką, kai bendras užsakymo ar pasiūlymo eilutės kiekis turi būti pristatytas keliomis siuntomis. Atskiras siuntas nurodo pristatymo eilutės. Dvi ar daugiau pristatymo eilučių sudaro vieną pristatymo grafiką. Pristatymo eilutėse gali skirtis pristatymo datos, kiekiai, pristatymo būdai ir saugojimo dimensijos, pvz., teritorija ir sandėlis.  

**Pristatymo grafiko pavyzdys**

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| Bendrasis užsakymas (pradinė užsakymo eilutė) | 600 kėdžių                               |
| Pageidaujamas pristatymo grafikas       | 100 kėdžių per mėnesį                     |
| Pageidaujama pristatymo laikotarpis | 6 mėnesiai, pristatant kiekvieno mėnesio pirmą dieną |

Pagal šį scenarijų klientas reikalauja pristatyti 600 kėdžių 100 kėdžių paketais per šešis mėnesius. Norėdami sekti pristatymo reikalavimus, galite kurti pristatymo grafiką. Puslapyje Pristatymo grafikas galite kurti šešias atskiras pristatymo eilutes. Kiekvienoje eilutėje nurodyta 100 kėdžių ir jų pristatymo data. Šiuo atveju kiekviena eilutė yra korespondentė pirmąjį iš šešių mėnesių.  

Kai kuriate pristatymo grafiką, pradinės užsakymo eilutės tipas automatiškai pakeičiamas į **Užsakymo eilutė su keliais pristatymais**. Šio tipo eilutė vadinama komercine eilute ir yra pažymėta piktograma. Pristatymo eilutė pažymima kita piktograma. Pakeitus pristatymo eilutės kiekį, prekybos eilutė atnaujinama bendruoju pristatymo grafiko kiekiu. Jei prekybos sutartyje nurodyta bendra užsakymo nuolaida, pristatymo grafikas užtikrina, kad jūsų užsakymui būtų taikoma bendra užsakymo nuolaida, net kai užsakymas yra padalintas į atskirus pristatymus.  

Užsakymai, turintys pristatymo grafiką, apdorojamos pagal pristatymo eilutes. Apdorojimo metu registruojami važtaraščiai, produktų gavimo kvitai ir išrašomos SF.  

Užsakymų ir pasiūlymų, turinčių pristatymo grafiką, dokumentų spaudiniuose rodomos tik pristatymo eilutės. Juose nerodomos pradinės eilutės (komercinės eilutės). **Pastaba:** be to, rodomos tik pristatymo eilutės, kai atliekate toliau nurodytus veiksmus.

-   Skelbti
-   Kopijuoti puslapius
-   Naršyti sąrašo puslapius ir ataskaitas

Kai patvirtinsite pardavimo pasiūlymus, gautuose pardavimo užsakymuose rodomas visas pristatymo grafikas, įskaitant net užsakymo eilutes, turinčias kelis pristatymus. Be to, visas pristatymo grafikas yra rodomas visuose pagrindiniuose puslapiuose, pvz., pardavimo užsakymuose, pardavimo pasiūlymuose ir pirkimo užsakymuose.





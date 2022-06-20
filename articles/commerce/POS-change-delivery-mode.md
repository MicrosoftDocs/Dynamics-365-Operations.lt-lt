---
title: Pristatymo būdo keitimas EKA
description: Šiame straipsnyje aprašoma, kaip konfigūruoti ir naudoti EKA pristatymo būdo keitimo būdą.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 583f568164d0de70e22998bf5ded5f4616b00bd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855826"
---
# <a name="change-mode-of-delivery-in-pos"></a>Pristatymo būdo keitimas EKA

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti "pristatymo būdo keitimo būdo" funkciją jūsų point point sale (EKA) aplinkoje. 

„Dynamics 365 Commerce“ 10.0.10 ir naujesnėse versijose prieinama operacija **„Pristatymo būdo keitimas“** (647), kuri leidžia pridėti EKA ekrano maketus.

Pristatymo būdo keitimo funkcija suteikia galimybę pakeisti vienos ar kelių sukonfigūruotų siuntų pardavimo eilučių pristatymo būdus EKA operacijose. Ankstesnėse „Commerce“ versijose reikėjo pereiti per visus **Siųsti viską** ar **Išsiųsti pasirinktus** konfigūracijos srautus, jei norėjote pakeisti pristatymo būdą esamoje eilutėje, kuri buvo sukonfigūruota siuntai. Šis procesas buvo ilgas, todėl galėjo įvykti atsitiktiniai pristatymo kilmės arba linijos pristatymo datų pakeitimai. Nauja funkcija pateikia alternatyvų metodą, kaip efektyviai atnaujinti pristatymo būdą šiose pardavimo linijose.

Daugiau informacijos apie tai, kaip į mygtuką, esantį jūsų EKA mygtukyne, įtraukti operaciją, rasite skyriuje [„Elektroninio kasos aparato ekrano maketai“](pos-screen-layouts.md).

Kai ši funkcija sukonfigūruota EKA, pasirinkus **„Pristatymo būdo keitimas“**, pateikiamas sąrašo puslapis, kuriame galėsite pasirinkti operacijos eilutes, kurių pristatymo būdą norite pakeisti. Galite pasirinkti kelias eilutes, visas eilutes arba išeiti neatlikus jokių pakeitimų. Galite pakeisti tik tas pardavimų eilutes, kurios anksčiau buvo sukonfigūruotos siuntimui. Jei norite pakeisti eilutę, skirtą paėmimui arba pristatymui į namus atlikti, naudokite operaciją **Siųsti viską** arba **Išsiųsti pasirinktus**. Ir atvirkščiai, jei norite pakeisti eilutę, kuri buvo pažymėta kaip siuntos paėmimas arba išsineštinis, naudokite operacijas **Paimti viską**, **Paimti pasirinktus**, **Išsinešti visus** arba **Išsinešti pasirinktus**.

Pasirinkę eilutes, kurias norite pakeisti, spustelėkite **Pristatymo būdo keitimas**, kad būtų galima pasirinkti pristatymo būdo parinktis. Jei pasirinkote keletą eilučių, kurias norite pakeisti, EKA bus rodomi tik tie pristatymo būdai, kurie buvo sukonfigūruoti kaip leistini visiems pasirinktiems produktams. Pristatymo būdus galima sukonfigūruoti taip, kad jie palaikytų konkrečius produktus ir pristatymo adresus. Jei yra pristatymo būdas, kuris yra priimtinas vienam produktui ir adresų deriniui, bet nepriimtinas kitam pasirinktam produktui ir adreso deriniui, pristatymo būdas negalimas. Jei norite pasirinkti pristatymo būdą vienam produktui, kurio nepalaiko kitas produktas, gali tekti pasirinkti eilutes po vieną ir pakeisti kiekvienos eilutės pristatymo būdą atskirai.  

Pasirinkus naują pristatymo būdą, rodomas operacijos puslapis. Norėdami peržiūrėti naujus pristatymo būdo pasirinkimus, operacijų sąraše pasirinkite skirtuką **Pristatymas**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Skambučių centro užsakymų kūrimas](tasks/create-call-center-orders.md)

[Tinkinti perlaidų el. paštus pagal pristatymo būdą](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
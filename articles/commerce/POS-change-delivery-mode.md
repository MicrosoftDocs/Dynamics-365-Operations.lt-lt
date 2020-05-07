---
title: EKA pristatymo būdo keitimas
description: Šioje temoje aprašoma, kaip sukonfigūruoti ir naudoti pristatymo būdo keitimą, esantį EKA.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: d2691ef6b08a44a845857c34fe60072211364f82
ms.sourcegitcommit: 02640a0f63daa9e509146641824ed623c4d69c7f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2020
ms.locfileid: "3265485"
---
# <a name="change-mode-of-delivery-in-pos"></a>EKA pristatymo būdo keitimas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti ir naudoti funkciją „pristatymo būdo keitimas“ elektroninio kasos aparato (EKA) aplinkoje. 

„Dynamics 365 Commerce“ 10.0.10 ir naujesnėse versijose prieinama operacija **„Pristatymo būdo keitimas“** (647), kuri leidžia pridėti EKA ekrano maketus.

Pristatymo būdo keitimo funkcija suteikia galimybę pakeisti vienos ar kelių sukonfigūruotų siuntų pardavimo eilučių pristatymo būdus EKA operacijose. Ankstesnėse „Commerce“ versijose reikėjo pereiti per visus **Siųsti viską** ar **Išsiųsti pasirinktus** konfigūracijos srautus, jei norėjote pakeisti pristatymo būdą esamoje eilutėje, kuri buvo sukonfigūruota siuntai. Šis procesas buvo ilgas, todėl galėjo įvykti atsitiktiniai pristatymo kilmės arba linijos pristatymo datų pakeitimai. Nauja funkcija pateikia alternatyvų metodą, kaip efektyviai atnaujinti pristatymo būdą šiose pardavimo linijose.

Daugiau informacijos apie tai, kaip į mygtuką, esantį jūsų EKA mygtukyne, įtraukti operaciją, rasite skyriuje [„Elektroninio kasos aparato ekrano maketai“](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).

Kai ši funkcija sukonfigūruota EKA, pasirinkus **„Pristatymo būdo keitimas“**, pateikiamas sąrašo puslapis, kuriame galėsite pasirinkti operacijos eilutes, kurių pristatymo būdą norite pakeisti. Galite pasirinkti kelias eilutes, visas eilutes arba išeiti neatlikus jokių pakeitimų. Galite pakeisti tik tas pardavimų eilutes, kurios anksčiau buvo sukonfigūruotos siuntimui. Jei norite pakeisti eilutę, skirtą paėmimui arba pristatymui į namus atlikti, naudokite operaciją **Siųsti viską** arba **Išsiųsti pasirinktus**. Ir atvirkščiai, jei norite pakeisti eilutę, kuri buvo pažymėta kaip siuntos paėmimas arba išsineštinis, naudokite operacijas **Paimti viską**, **Paimti pasirinktus**, **Išsinešti visus**arba **Išsinešti pasirinktus**.

Pasirinkę eilutes, kurias norite pakeisti, spustelėkite **Pristatymo būdo keitimas**, kad būtų galima pasirinkti pristatymo būdo parinktis. Jei pasirinkote keletą eilučių, kurias norite pakeisti, EKA bus rodomi tik tie pristatymo būdai, kurie buvo sukonfigūruoti kaip leistini visiems pasirinktiems produktams. Pristatymo būdus galima sukonfigūruoti taip, kad jie palaikytų konkrečius produktus ir pristatymo adresus. Jei yra pristatymo būdas, kuris yra priimtinas vienam produktui ir adresų deriniui, bet nepriimtinas kitam pasirinktam produktui ir adreso deriniui, pristatymo būdas negalimas. Jei norite pasirinkti pristatymo būdą vienam produktui, kurio nepalaiko kitas produktas, gali tekti pasirinkti eilutes po vieną ir pakeisti kiekvienos eilutės pristatymo būdą atskirai.  

Pasirinkus naują pristatymo būdą, rodomas operacijos puslapis. Norėdami peržiūrėti naujus pristatymo būdo pasirinkimus, operacijų sąraše pasirinkite skirtuką **Pristatymas**.   

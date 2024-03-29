---
title: Vidinės įmonės apskaitos nustatymas
description: Šiame straipsnyje paaiškinama, kaip nustatyti vidinės įmonės apskaitą, kad būtų galima naudoti vidinės įmonės žurnalus DK paskirstymams ir finansiniams žurnalams, pvz., kasdienės žurnalams, tiekėjo SF žurnalams ir mokėjimo žurnalams.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 309c121c1ef4b3814d676cad6f3c2b6826b59843
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871223"
---
# <a name="intercompany-accounting-setup"></a>Vidinės įmonės apskaitos nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti vidinės įmonės apskaitą, kad būtų galima naudoti vidinės įmonės žurnalus DK paskirstymams ir finansiniams žurnalams, pvz., kasdienės žurnalams, tiekėjo SF žurnalams ir mokėjimo žurnalams.

Vidinės įmonės žurnalus galima kurti pagal įvairius scenarijus, pvz., kasdieninių žurnalų, tiekėjo SF žurnalų, DK paskirstymų ir centralizuotų mokėjimų. Norėdami įgalinti šiuos scenarijus, turite nustatyti vidinės įmonės apskaitą.

## <a name="define-main-accounts"></a>Pagrindinių sąskaitų nustatymas
Pirmiausia, turite sukurti vidinės įmonės pagrindines sąskaitas, kurios bus naudojamos apskaitos įrašams „Gavėjas“ ir „Mokėtojas“. Tikslinga kiekvienam įmonei naudoti unikalias pagrindines sąskaitas, kad būtų galima paprasčiau derinti ir šalinti vidinės įmonės apskaitos įrašus. Jei naudojate verslo partnerio ar kolegos dimensiją, kad nustatytumėte vidinės įmonės šalį, šią dimensiją galite nurodyti kaip fiksuotą pagrindinėje sąskaitoje, kuri nurodyta vidinės įmonės apskaitoje. Kai nustatote pagrindines sąskaitas, puslapyje **Pagrindinės sąskaitos** nustatykite lauko **Pagrindinės sąskaitos tipas** reikšmę **Balansas**.

## <a name="define-journal-names"></a>Žurnalų pavadinimų nustatymas
Tada turite nustatyti žurnalo pavadinimą. Puslapyje **Žurnalų pavadinimai** nustatykite lauko **Žurnalo tipas** reikšmę **Kasdienis**. Tikslinga naudoti konkretų žurnalo pavadinimą vidinės įmonės apskaitai.

## <a name="define-intercompany-accounting-setup"></a>Vidinės įmonės apskaitos sąrankos nustatymas
Puslapis **Įmonės vidinės apskaita** dabar naudojamas norint kurti visas sandorį galinčias sudaryti juridinių subjektų poras. Vidinės įmonės apskaitos sąranka yra bendrinama, todėl sąranka matoma visuose juridiniuose subjektuose. Kurdami naują juridinių subjektų porą įsitikinkite, kad žinote, kuris juridinis subjektas turi būti nustatytas kaip pradinė įmonė, o kuris – kaip paskirties įmonė. Įvedant vidinės įmonės operacijas, operacija nustato, kuris juridinis subjektas operaciją inicijuoja. Pvz., nustatoma įmonių USMF (pradinė) ir USSI (paskirties) vidinės įmonės apskaita. Jei vartotojas yra aktyvus įmonėje USSI ir jis įveda vidinės įmonės operaciją, susijusią su USMF, operacija nebus registruojama, nes vidinės įmonės apskaita nustatyta tik USMF nurodžius kaip pradinę įmonę. Jei abi įmonės gali inicijuoti operacijas, turėsite sukurti antrą juridinių subjektų porą ir nustatyti abipusę sąranką. 

Pradiniame ir paskirties juridiniuose subjektuose nustatykite parinktis **Debeto sąskaita (mokėtojas)** ir **Kredito sąskaita (gavėjas)**. Nurodykite, kuris **Žurnalo pavadinimas** bus naudojamas, kai operacija kuriama paskirties įmonėje. Pradinės įmonės žurnalas jau žinomas, nes kuriant vidinės įmonės operaciją jį pasirenka vartotojas. 

Galiausiai pasirinkite, kuriam juridiniam subjektui bus teikiama galimų sumų apskaita, pvz., centralizuotų mokėjimų nuolaidos arba gauto pelno / patirto nuostolio apskaita. 

Abipusį ryšį galima lengvai nustatyti puslapyje **Vidinės įmonės apskaita** naudojant mygtuką **Kurti abipusį ryšį**, kai pirmoji juridinių subjektų pora jau sukurta. Kai abipusio ryšio pora sukurta, paskirties įmonės informacija nukopijuojama į pradinę įmonę (ir atvirkščiai). Nustatytas paskirties įmonės žurnalas liks toks pat. Dauguma organizacijų naudoja tokią pačią savo žurnalų pavadinimų kūrimo strategiją, kad jų žurnalo pavadinimas būtų toks pat. Jei žurnalo pavadinimas kitoks, lauke bus rodomas pranešimas, įspėjantis, kad žurnalo nėra ir galima pasirinkti kitą žurnalą.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

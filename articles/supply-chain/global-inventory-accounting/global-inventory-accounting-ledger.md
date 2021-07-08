---
title: Visuotinės Atsargų Apskaitos didžioji knyga
description: Šioje temoje aprašomos Visuotinės atsargų apskaitos didžiosios knygos, kurias apibrėžia valiutos, kalendoriaus, konvencijos ir susiejimo su juridiniu subjektu derinys.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273196"
---
# <a name="global-inventory-accounting-ledger"></a>Visuotinės Atsargų Apskaitos didžioji knyga

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Visuotinė atsargų apskaita turi savo didžiųjų knygų rinkinį. Kiekvieną kartą, kai su atsargomis susijusi operacija apdorojama susijusiam juridiniam subjektui, sistema gali atlikti tos operacijos apskaitą tiek Visuotinės atsargų apskaitos didžiosiose knygose, kiek reikia.

Didžioji knyga yra debeto ir kredito priemonių registras. Šios priemonės klasifikuotos naudojant išlaidų elementus ir papildomos knygos sąskaitas. Visuotinės atsargų apskaitos didžiąją knygą apibrėžia valiutos, kalendoriaus, konvencijos ir susiejimo su juridiniu subjektu derinys.

Norėdami nustatyti savo Visuotinės atsargų apskaitos didžiąsias knygas, eikite į **Visuotinį atsargų apskaita \> Nustatymas \> Visuotinės atsargų apskaitos didžiosios knygos**. Kiekvienai didžiajai knygai nustatykite toliau pateiktus laukus:

- **Pavadinimas** – įveskite didžiosios knygos pavadinimą.
- **Aprašas** – įveskite didžiosios knygos aprašą.
- **Finansinis kalendorius** – Nurodykite didžiosios knygos finansinį kalendorių.
- **Valiutos ir valiutos kurso tipas** – Norėdami pasirinkti didžiosios knygos naudojamą apskaitos valiutą ir valiutos kurso tipą naudokite šio „FastTab” laukus. Jūsų pasirinkta valiuta gali skirtis nuo juridinio subjekto naudojamos valiutos. Visuotinėje atsargų apskaitoje vartotojai gali apibrėžti tiek įkainojimo didžiųjų knygų, kiek reikia. Visuotinė atsargų apskaita palaiko atsargų apskaitą keliomis valiutomis ir keliais vertinimais. Užpildykite toliau nurodytus laukus:

    - **Valiuta** – Pasirinkite įkainojimo valiutą, kuria tvarkomos su atsargomis susijusios vertės. Šios vertės apima atsargų vertę, parduotų prekių savikainą, tranzito atsargas ir visų rūšių nuokrypius.
    - **Valiutos kurso tipas** – Pasirinkite valiutos kursą, kurį sistema turėtų naudoti operacijos sumai konvertuoti į operacijos valiutą ir standartinei prekių savikainai konvertuoti į įkainojimo valiutą.

- **Konvencijos pavadinimas** – Nurodykite konvenciją. Konvencija yra strategijų, nustatančių kaip išlaidos bus apskaičiuotos šioje didžiojoje knygoje, rinkinys.
- **Juridinis subjektas** – Didžioji knyga surašys dokumentus, užregistruotus pasirinktame juridiniame subjekte.
- **Turto valdymas** – Pasirinkite, ar atsargų operacijos, sukurtos prieš didžiosios knygos sukūrimą, turėtų būti apdorojamos pagal didžiosios knygos valiutą ir konvenciją. Pasirinkite vieną iš šių reikšmių:

    - **Suaktyvinta** – Didžioji knyga turi apdoroti operacijas, kurios buvo sukurtos prieš didžiosios knygos sukūrimą.
    - **Išjungta** – Didžioji knyga turi apdoroti tik tas operacijas, kurios bus sukurtos po didžiosios knygos sukūrimo.

    > [!IMPORTANT]
    > Jūs **negalėsite** grįžti ir nustatyti šio lauko po to, kai įvesite naujus dokumentus.

- **Būsena** – Sistema automatiškai nustato naujai sukurtų didžiųjų knygų būseną į *Paruošti*.

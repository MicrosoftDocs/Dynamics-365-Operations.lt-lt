---
title: Susieti kuro indeksą su vežėju kaip mokestį už papildomas paslaugas
description: Šiame vadove nurodoma, kaip sukurti papildomų paslaugų priskyrimą, vežėjo papildomų paslaugų mokestį, papildomo degalų mokesčio papildomų paslaugų šabloną ir susieti vežėjo degalų indeksą su vežėju.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f69a6350a5a84ed19dcb37e174c25b112c16bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974140"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Susieti kuro indeksą su vežėju kaip mokestį už papildomas paslaugas

[!include [banner](../../includes/banner.md)]

Šiame vadove nurodoma, kaip sukurti papildomų paslaugų priskyrimą, vežėjo papildomų paslaugų mokestį, papildomo degalų mokesčio papildomų paslaugų šabloną ir susieti vežėjo degalų indeksą su vežėju. Prieš paleisdami šį vadovą turite nustatyti vežėjo degalų indeksą. Norėdami tai padaryti, galite naudoti vadovą „Nustatyti vežėjo degalų indeksą“. Šias nustatymo užduotis paprastai atlieka logistikos vadovas. Kuriant šią procedūrą buvo naudojami USMF demonstraciniai duomenys.


## <a name="create-an-accessorial-master"></a>Kurti papildomų paslaugų šabloną
1. Pasirinkite Transportavimo valdymas > Nustatymas > Vertinimas > Papildomų paslaugų šablonai.
2. Spustelėkite Naujas.
3. Lauke „Papildomų paslaugų šablonas“ įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Spustelėkite Įrašyti.

## <a name="create-a-carrier-accessorial-charge"></a>Kurti vežėjo papildomų paslaugų mokestį
1. Pasirinktie Transportavimo valdymas > Nustatymas > Vertinimas > Vežėjo papildomų paslaugų mokesčiai.
2. Spustelėkite Naujas.
3. Lauke „Vežėjo papildomų paslaugų ID“ įveskite reikšmę.
4. Lauke „Siuntų vežėjas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše raskite ir pasirinkite norimą įrašą.
    * Šiame pavyzdyje pasirinkite „Sunkvežimio vežėjas“.  
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Lauke „Vežėjo paslauga“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke „Papildomų paslaugų šablonas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
10. Sąraše raskite ir pasirinkite norimą įrašą.
    * Šiame pavyzdyje pasirinkite naujai sukurtą papildomų paslaugų šabloną.  
11. Spustelėkite Įrašyti.

## <a name="create-an-accessorial-assignment"></a>Kurti papildomų paslaugų priskyrimą
1. Spustelėkite „Papildomų paslaugų priskyrimai“.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Perjunkite skyriaus „Kriterijai“ išplėtimą.
    * Kriterijuose visada galite taikyti papildomą degalų mokestį arba šiame pavyzdyje galite pasirinkti, kad jis būtų taikomas tik tam tikrame regione.  
5. Lauke „Pašto kodas iš“ įveskite reikšmę.
6. Lauke „Pašto kodas į“ įveskite reikšmę.
7. Perjunkite skyriaus „Skaičiavimas“ išplėtimą.
    * Skaičiavimo skyriuje galite nurodyti, kaip skaičiuoti papildomą degalų mokestį. Šis skaičiavimas priklauso nuo papildomų paslaugų vieneto, kurį pasirinkote skaičiavimo pagrindu.  
8. Lauke „Mokesčio už papildomas paslaugas tipas“ pasirinkite „Papildomas degalų mokestis“.
9. Lauke „Papildomų paslaugų vienetas“ pasirinkite „Kilometražas“.
10. Lauke „Regionas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše spustelėkite saitą pasirinktoje eilutėje.
12. Spustelėkite Įrašyti.

## <a name="update-the-carrier-rating-profile"></a>Atnaujinti vežėjo vertinimo profilį
1. Pasirinkite Transportavimo valdymas > Nustatymas > Vežėjai > Siuntų vežėjai.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Perjunkite skyriaus „Vertinimo šablonai“ išplėtimą.
4. Spustelėkite Redaguoti.
5. Lauke „Vežėjo degalų indeksas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Spustelėkite Įrašyti.


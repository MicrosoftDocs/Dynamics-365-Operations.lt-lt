---
title: Darbo su Brazilijos elektroninių SF išrašymo priedu pradžia
description: Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis Brazilijos elektroninių SF išrašymo priedu „Finance” ir „Supply Chain Management”.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: eaf9433ad2d9ccf3d3c5632d0f2d4fe772ff8bde
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592675"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Darbo su Brazilijos elektroninių SF išrašymo priedu pradžia 

[!include [banner](../includes/banner.md)]

Ši tema paaiškina, kaip pradėti su elektroninės sąskaitos priedo paslaugų administravimu Brazilijai. Šios temos aprašytos procedūros padės jums atlikti konfigūravimo veiksmus, priklausančius nuo „Regulatory Configuration Services” (RCS), ir papildyti temoje [Darbo su elektroniniu SF išrašymo priedu pradžia](e-invoicing-get-started.md) aprašytus veiksmus.

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Šaliai skirta Brazilijos NF-e (BR) elektroninių SF išrašymo priemonės konfigūracija

Konfigūruojant Brazilijos NF-e (BR) elektroninių SF išrašymo priemonę reikia, kad atlikti konkrečius veiksmus. Kai kurie konfigūracijų parametrai publikuojami su numatytosiomis vertėmis, todėl juos reikia peržiūrėti ir atnaujinti, kad jie geriau atitiktų jūsų verslo operaciją.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš atlikdami šiame skyriuje aprašytą procedūrą, sukurkite Brazilijos NF-e (BR) elektroninių SF išrašymo funkciją savo įmonei, kaip aprašoma temos skyriuje **Elektroninės SF kūrimas vadovaujant jūsų įmonės teikėjui**, [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

1. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Globalizacijos funkcija**, pasirinkite plytelę **Elektroninių SF priedas**.
2. Puslapyje **Elektroninių SF išrašymo priedo funkcijos** patikrinkite, ar pasirinkta jūsų sukurta elektroninio SF išrašymo funkcija **Brazilijos NF-e (BR)**.
3. Skirtuke **Versijos** patikrinkite, ar pasirinkta versija **Šablonas**.
4. Skirtuke **Nustatymai**, tinklelyje pasirinkite **Pateikti**, tada pasirinkite **Redaguoti.**
5. Skirtuke **Veiksmai**, laukelių grupėje **Veiksmai** pasirinkite veiksmą **(Peržiūra) pasirašytas xml dokumentas**.
6. Laukelių grupėje **Parametrai** pasirinkite **Sertifikato pavadinimas**, o laukelyje **Vertė** įveskite su jūsų raktų saugykla susieto sertifikato pavadinimą.
7. Skirtuke **Veiksmai**, laukelių grupėje **Veiksmai** pasirinkite veiksmą **(Peržiūra) Skambinti Brazilijos SEFAZ tarnybai**.
8. Laukelių grupėje **Parametrai** pasirinkite parametrą **URL adresas**.
9. Jei reikia, laukelyje **Vertė** peržiūrėkite ir atnaujinkite SEFAZ dokumentacijos paskelbtų tinklo tarnybų URL savo būsenai ir pasirinkite **Išsaugoti**.
10. Skirtuke **Pritaikymo taisyklės**, laukelių grupėje **Pritaikymo taisyklės sąranka** peržiūrėkite ir prireikus atnaujinkite laukelio **Būsena** kriterijus tai pačiai būsenai, kurią nurodo tinklo tarnybų URL.
11. Pasirinkite **Išsaugoti** ir uždarykite puslapį.
12. Norėdami sukonfigūruoti programos nustatymą, žr. skyrių [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Šaliai skirta Brazilijos NF-e (BR) elektroninių SF išrašymo priemonės programos sąrankos konfigūracija

Konfigūruojant Brazilijos NF-e (BR) elektroninių SF išrašymo priemonės programos sąranką reikia, kad atlikti konkrečius veiksmus. Prieš diegdami elektroninių SF išrašymo funkciją savo elektroninio SF išrašymo paslaugų aplinkoje, atlikite šiuos veiksmus.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš atlikdami šiame skyriuje aprašytą procedūrą, sukurkite ir paleiskite Brazilijos NF-e (BR) elektroninių SF išrašymo funkcijos programos konfigūraciją savo įmonei, kaip aprašoma temos skyriuje **Programos sąrankos konfigūravimas**, [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

1. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Globalizacijos funkcija**, pasirinkite plytelę **Elektroninių SF priedas**.
2. Puslapyje **Elektroninių SF išrašymo priedo funkcijos** patikrinkite, ar pasirinkta elektroninio SF išrašymo funkcija **Brazilijos NF-e (BR)**.
3. Skirtuke **Versijos** patikrinkite, ar pasirinkta versija **Šablonas**.
4. Skirtuke **Nustatymai** pasirinkite **Programos sąranka** ir laukelyje **Prijungta programa** pasirinkite programą, kurioje norite diegti.
5. Laukelyje **Lentelės pavadinimas** patikrinkite, ar pasirinkta funkcija **Finansinio dokumento antraštė**.
6. Pasirinkite **Atsakymų tipai**, o tada pasirinkite **Nauja**.
7. Laukelyje **Atsakymo tipas** atsakymą įveskite kaip fiksuotą reikšmę, o laukelyje **Aprašas** įveskite „Aprašas“.
8. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
9. Laukelyje **Modelio susiejimas** pasirinkite funkciją **Modelio susiejimas iš atsakymo pranešimo** bei **(Peržiūra) Atsakymo pranešimo importavimo formatas**, o tada pasirinkite **Išsaugoti**.
10. Pasirinkite **Naujas** ir laukelyje **Atsakymo tipas** įveskite „Atsakymo duomenys“ kaip fiksuotą reikšmę ir laukelyje **Aprašas** įveskite „Aprašas“.
11. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
12. Laukelyje **Modelio susiejimas** pasirinkite funkciją **Atsakymo duomenų importavimas** bei **NF-e atsakymo importavimo formatas (BR)**, o tada pasirinkite **Išsaugoti**.
13. Norėdami įdiegti elektroninių SF išrašymo funkciją, žr. skyrių [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Šaliai skirta Brazilijos NFS-e ABRASF Kuritibos (BR) elektroninių SF išrašymo priemonės konfigūracija

Konfigūruojant Brazilijos NF-e ABRASF Kuritibos (BR) elektroninių SF išrašymo priemonę reikia, kad atlikti konkrečius veiksmus. Kai kurie konfigūracijų parametrai publikuojami su numatytosiomis vertėmis, todėl juos reikia peržiūrėti ir atnaujinti, kad jie geriau atitiktų jūsų verslo operaciją.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš užbaigdami procedūrą šiame skyriuje, savo įmonėje sukurkite Brazilijos NFS-e ABRASF Kuritibos (BR) elektroninių SF išrašymo funkciją. Tai aprašyta temos skyriuje **Elektroninės SF konfigūravimas**, [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

1. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Globalizacijos funkcija**, pasirinkite plytelę **Elektroninių SF priedas**.
2. Puslapyje **Elektroninių SF išrašymo priedo funkcijos** patikrinkite, ar pasirinkta jūsų sukurta elektroninio SF išrašymo funkcija **Brazilijos NFS-e ABRASF Kuritiba (BR)**.
3. Skirtuke **Versijos** patikrinkite, ar funkcija **Šablonas** pasirinkta, o skirtuke **Nustatymai**, tinklelyje, pasirinkite **Pateikti**.
4. Pasirinkite **Redaguoti** ir skirtuke **Veiksmai**, laukelių grupėje **Veiksmai** pasirinkite pirmąjį **(Peržiūra) pasirašyto xml dokumento** variantą.
5. Laukelių grupėje **Parametrai** pasirinkite **Sertifikato pavadinimas**.
6. Laukelyje **Reikšmė** įveskite su jūsų raktų saugyklos parametru susieto sertifikato pavadinimą.
7. Laukelių grupėje **Veiksmai** pasirinkite antrąjį **(Peržiūra) pasirašytą xml dokumentą**.
8. Laukelių grupėje **Parametrai** pasirinkite **Sertifikato pavadinimas**.
9. Laukelyje **Reikšmė** įveskite su jūsų raktų saugyklos parametru susieto sertifikato pavadinimą.
10. Skirtuke **Veiksmai**, laukelių grupėje **Veiksmai** pasirinkite veiksmą **(Peržiūra) Skambinti Brazilijos SEFAZ tarnybai**.
11. Laukelių grupėje **Parametrai** pasirinkite parametrą **URL adresas**.
12. Jei reikia, laukelyje **Vertė** peržiūrėkite ir atnaujinkite Kuritibos mokesčių inspekcijos paskelbtų tinklo tarnybų URL ir pasirinkite **Išsaugoti**.
13. Skirtuke **Nustatymai**, tinklelyje pasirinkite **Teirautis**, tada pasirinkite **Redaguoti.**
14. Skirtuke **Veiksmai**, laukelių grupėje **Veiksmai** pasirinkite veiksmą **(Peržiūra) Skambinti Brazilijos SEFAZ tarnybai**.
15. Laukelių grupėje **Parametrai** pasirinkite parametrą **URL adresas**.
16. Jei reikia, laukelyje **Vertė** peržiūrėkite ir atnaujinkite Kuritibos mokesčių inspekcijos paskelbtų tinklo tarnybų URL.
17. Pasirinkite **Įrašyti** ir uždarykite puslapį.
18. Norėdami sukonfigūruoti programos nustatymą, žr. skyrių [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Šaliai skirta Brazilijos NFS-e ABRASF Kuritibos (BR) elektroninių SF išrašymo priemonės programos sąrankos konfigūracija

Konfigūruojant Brazilijos NFS-e ABRASF Kuritibos (BR) elektroninių SF išrašymo funkciją reikia, kad prieš diegiant savo elektroninių SF išrašymo priemonę į savo elektroninių SF išrašymo priedų aptarnavimo aplinką, būtų atlikti konkretūs veiksmai.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš atlikdami šiame skyriuje aprašytą procedūrą, sukurkite ir paleiskite Brazilijos NFS-e ABRASF Kuritibos (BR) elektroninių SF išrašymo funkcijos programos konfigūraciją savo įmonei, kaip aprašoma temos skyriuje **Programos sąrankos konfigūravimas**, [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

1. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Globalizacijos funkcija**, pasirinkite plytelę **Elektroninių SF priedas**.
2. Puslapyje **Elektroninių SF išrašymo priedo funkcijos** patikrinkite, ar pasirinkta elektroninio SF išrašymo funkcija **Brazilijos NFS-e ABRASF Kuritiba (BR)**.
3. Skirtuke **Versijos** patikrinkite, ar funkcija **Šablonas** pasirinkta, o skirtuke **Nustatymai**, pasirinkite **Programos sąranka**.
4. Laukelyje **Prijungta programa** pasirinkite programą, kurią norite diegti.
5. Laukelyje **Lentelės pavadinimas** patikrinkite, ar pažymėta finansinio dokumento antraštė.
6. Pasirinkite **Atsakymų tipai** ir pasirinkite **Nauja**.
7. Laukelyje **Atsakymo tipas** ABRASF Kuritibos pateikimo atsakymą įveskite kaip fiksuotą reikšmę, o laukelyje **Aprašas** įveskite „Aprašas“.
8. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
9. Laukelyje **Modelio susiejimas** pasirinkite funkciją **Atsakymo pranešimo importavimas** bei **NFS-e ABRASF Kuritibos atsakymo pranešimo importavimas (BR)**, o tada pasirinkite **Išsaugoti**.
10. Pasirinkite **Naujas** ir laukelyje **Atsakymo tipas** įveskite „ABRASF Kuritibos atsakymo pateikimo duomenys“ ir laukelyje **Aprašas** įveskite „Aprašas“.
11. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
12. Laukelyje **Modelio susiejimas** pasirinkite funkciją **Atsakymo duomenų importavimas** bei **(Peržiūra) NFS-e ABRASF atsakymo importavimo formatas (BR)**, o tada pasirinkite **Išsaugoti**.
13. Pasirinkite **Naujas** ir laukelyje **Atsakymo tipas** įveskite „ABRASF Kuritibos atsakymo prašymas“ kaip fiksuotą reikšmę ir laukelyje **Aprašas** įveskite „Aprašas“.
14. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
15. Laukelyje **Modelio susiejimas** pasirinkite funkciją **Atsakymo pranešimo importavimas** bei **(Peržiūra) NFS-e ABRASF Kuritibos atsakymo pranešimo importavimas (BR).**
16. Pasirinkite **Išsaugoti**, tada grįžkite prie temos, [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md), kad išskleistumėte elektroninių SF išrašymo funkciją.

## <a name="privacy-notice"></a>Privatumo pranešimas
Įjungus funkciją **NF-e federalinė Brazilijos elektroninė SF (BR)** ir **NFS-e Brazilijos tarnybos (miesto) elektroninė SF** gali prireikti siųsti ribotus duomenis, įskaitant įmonės mokesčių registracijos ID. Šie duomenys persiunčiami mokesčių inspekcijos patvirtintoms trečiųjų šalių agentūroms, kad būtų galima siųsti elektronines SF šiai mokesčių inspekcijai iš anksto nustatytu formatu, reikalingu integravimui su vyriausybės žiniatinklio tarnyba. Kaip administratorius, galite įjungti arba išjungti **NF-e federalinę Brazilijos elektroninių SF (BR)** ir **NFS-e Brazilijos tarnybos (miestas) elektroninių SF** funkcijas. Toliau parodyta kaip tai padaryti: 

1. Eikite į **Organizacijos administravimas** > **Nustatymas** > **Elektroninių dokumentų parametrai**. 
2. Skirtuke **Funkcijos** pasirinkite eilutę, kurioje yra funkcija **NF-e federalinė Brazilijos elektroninė SF (BR)** arba **NFS-e Brazilijos tarnybos (miestas) elektroninė SF**, o tada pasirinkite funkciją. Duomenims, importuotiems iš šių išorinių sistemų į šią „Dynamics 365” internetinę paslaugą, taikomos [privatumo nuostatos](https://go.microsoft.com/fwlink/?LinkId=512132). Daugiau informacijos ieškokite skyriuose Privatumo pranešimas, esančiuose konkrečios šalies funkcijos dokumentacijoje.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių SF išrašymo priedo apžvalga](e-invoicing-service-overview.md)
- [Darbo su elektroninių SF priedu tarnybos administravimui pradžia](e-invoicing-get-started-service-administration.md)
- [Darbo su elektroninių SF priedu pradžia](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

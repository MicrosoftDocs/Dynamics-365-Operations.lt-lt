---
title: Parduotuvės darbo valandų kūrimas ir atnaujinimas
description: Šioje temoje aprašyta, kaip kurti ir atnaujinti parduotuvės darbo valandas naudojant „Retail Headquarters“.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 1b55b91246b22951f4e1d148f59444423e1d8a3d
ms.sourcegitcommit: e54607a2c80bec4db05045825914f50947f6e31e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1917517"
---
# <a name="create-and-update-store-hours"></a>Parduotuvės darbo valandų kūrimas ir atnaujinimas

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>Apžvalga

Mažmenininkai vienoje vietoje gali kurti, prižiūrėti ir valdyti skirtingų parduotuvių įvairiuose geografiniuose regionuose darbo valandas. Tada parduotuvės darbo valandos gali būti rodomos elektroninio kasos aparato (EKA) terminaluose. Tokiu būdu kasininkai gali su klientais bendrinti parduotuvės darbo valandas ir geriau padėti pirkėjams, kuriuos domina atsargos kitose parduotuvėse. Parduotuvės darbo valandos taip pat gali būti spausdinamos ant kvitų, jei vėliau klientai norėtų sugrįžti į parduotuvę.

Skirtinguose kanaluose galima sukonfigūruoti įvairias parduotuvės darbo valandas. Šie kanalai apima fizines parduotuves, skambučių centrus, mobiliuosius įrenginius ir el. prekybos svetaines.

Jei klientas turi kitos parduotuvės paėmimo užsakymą, kasininkas gali pasirinkti datas, kada toje parduotuvėje bus galima paimti prekes. Parduotuvių peržvalgoje bus pateikta nuoroda į datas ir parduotuvių darbo laiką. Kasininkas gali pasirinkti datą ir vietą bei atspausdinti paėmimo kvitą, kuriame bus nurodytos parduotuvės darbo valandos.

Ši funkcija pasiekiama „Microsoft Dynamics 365 for Retail“ 8.1.2 ir naujesnėse versijose.

## <a name="configure-store-hours"></a>Parduotuvės darbo valandų konfigūravimas

Atlikite toliau nurodytus veiksmus, kad sukonfigūruotumėte parduotuvės darbo valandas.

1. Eikite į **Mažmeninė prekyba** \> **Kanalo sąranka** \> **Parduotuvės darbo valandos**.
2. Pasirinkite **Naujas**, kad sukurtumėte naują parduotuvės darbo valandų šabloną. Norėdami naudoti esamą šabloną, pasirinkite šabloną kairiojoje srityje.
3. Dialogo lange **Intervalo įtraukimas** nustatykite datos intervalą, parduotuvės darbo valandas ir reikalingas šventines dienas.

    - Jei parduotuvės darbo valandos nesikeičia, lauke **Pabaigos data** pasirinkite **Niekada nesibaigia**.
    - Jei nustatomos konkretaus mėnesio, savaitės ar dienos parduotuvės darbo valandos, laukuose **Pradžios data** ir **Pabaigos data** nustatykite reikiamas datas.

    > [!NOTE]
    > Gali sukurti kelis šablonus, kurių pradžios ir pabaigos datos persidengia. Todėl, pavyzdžiui, galite nustatyti skirtingose laiko juostose esančių parduotuvių darbo valandas.

    ![Intervalo įtraukimo dialogo langas](../dev-itpro/media/Storehours1.png "Intervalo įtraukimo dialogo langas")

4. Parduotuvės darbo valandų šabloną susiekite su parduotuvėmis, kuriose jis bus naudojamas. Dialogo lange **Pasirinkti organizacijos mazgus** pasirinkite parduotuves, regionus ir organizacijas, su kuriomis turėtų būti susietas šablonas.

    - Su kiekviena parduotuve galima susieti tik vieną parduotuvės darbo valandų šabloną.
    - Pasirinkite parduotuves, regionus ar organizacijas naudodami rodyklių mygtukus. Kalendorius bus pasiekiamas parduotuvėms ar parduotuvių grupėms ir matomas EKA.

    ![Organizacijos mazgų pasirinkimo dialogo langas](../dev-itpro/media/Storehours2.png "Organizacijos mazgų pasirinkimo dialogo langas")

5. Puslapyje **Paskirstymo grafikas** vykdykite **1070** ir **1090** užduotis, kad parduotuvės darbo valandos būtų pasiekiamos EKA.

## <a name="add-store-hours-to-printed-receipts"></a>Parduotuvės darbo valandų įtraukimas į išspausdintus kvitus

Norėdami parduotuvės darbo valandas įtraukti į išspausdintus EKA kvitus, atlikite toliau nurodytus veiksmus.

1. Atidarykite kvito dizaino įrankį.
2. Apatiniame kairiajame kampe pasirinkite **Poraštė**.
3. Elementą **Parduotuvės darbo valandos** iš kairiosios srities nuvilkite į kvito šablono apačioje esančią poraštę.
4. Jei reikia, galite redaguoti elemento **Parduotuvės darbo valandos** numatytąją žymą.
5. Įrašykite kvitą ir uždarykite kvitų dizaino įrankį.
6. Puslapyje **Paskirstymo grafikas** vykdykite **1070** ir **1090** užduotis.
7. Prisijunkite prie EKA.
8. Užbaikite pardavimą ir pasirinkite spausdinti kvitą.

Dabar EKA kvituose nurodomos parduotuvės darbo valandos. Jei į šabloną buvo įtraukta šventinių dienų, jos rodomos ant kvito.

![Kvito pavyzdys](../dev-itpro/media/Storehours3.png "Kvito pavyzdys")
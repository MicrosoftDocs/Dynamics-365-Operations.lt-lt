---
title: Grąžinti serijos numeriais kontroliuojamus produktus naudojant EKA
description: Šiame straipsnyje aprašomos galimybės galiojant Microsoft Dynamics 365 Commerce eilutėmis išrašomas prekes kaip grąžinimo proceso dalį point point sale (EKA) programoje.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9fa7e47b6d650370afe4b98d7eca01253bd1bc36
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268480"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>Grąžinti serijos numeriais kontroliuojamus produktus naudojant EKA

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomos galimybės galiojant Microsoft Dynamics 365 Commerce eilutėmis išrašomas prekes kaip grąžinimo proceso dalį point point sale (EKA) programoje.

> [!NOTE]
> "Commerce 10.0.20" versijoje ir vėliau galima naudoti naują funkciją, kuri **EKA vadinama bendrojo grąžinamo apdorojimo** patirtimi. Norėdami naudoti serijos numerio tikrinimą apdorojant grąžinimo užsakymą EKA, turite įjungti šią funkciją. Informacijos apie kitas galimybes, kurias suteikia ši funkcija, kai ji įjungta, žr. [Kurti grąžinimus EKA)](POS-returns.md).
>
> Kai priemonė įjungta, jos išjungti negalima.

## <a name="options-for-validating-serialized-returns"></a>Eilutėmis grąžintų grąžinimų pateisinimo parinktys

Kai **EKA priemonėje įjungta bendrojo grąžinimo apdorojimo** organizacijos gali atlikti prekių, kurių serijos numeris kontroliuojamas naudojant EKA, grąžinamų tikrinimą. Ši galimybė gali įspėti vartotojus, jei grąžinamas serijos numeris skiriasi nuo pradinio parduoto serijos numerio. „Commerce" 10.0.20 versijoje ir vėliau pranešimas, kurį gauna vartotojai, yra tik įspėjamasis pranešimas. Vartotojai gali toliau apdoroti grąžinimą pagal serijos numerį, kuris skiriasi nuo serijos numerio, kuris buvo parduotas iš pradžių.

Norėdami konfigūruoti organizacijos serijos numerio tikrinimą įjungę **bendrojo grąžinimo apdorojimo funkciją EKA** eikite į **Mažmena ir komercija \> Štabo nustatymai \> Parameters \> „Commerce“ parametrai** „Commerce“ štabe. Skirtuko **Atsargos** „FastTab“ **Parduotuvės atsargų operacijų** nustatykite **Įgalinti EKA grąžinimų serijos numerių tinkinimo** parinktį į **Taip**.

## <a name="process-returns-for-serialized-items-in-pos"></a>Apdoroti EKA eilutėmis išduotų prekių grąžinimus

Jei **parinktis Įgalinti serijos numerių tikrinimą EKA grąžinimo pasirinktyje nustatyta** kaip **Taip**, ai naudojant EKA grąžinama serijos numeriu kontroliuojama prekė, vartotojas gali įvesti grąžinimo eilutės serijos numerį į informacijos sritį, esančioje **Produktų grąžinimo** puslapyje. Jei įvestas serijos numeris neatitinka pradinio serijos numerio, parduoto pardavimo operacijai, vartotojas gauna įspėjimo pranešimą. Tačiau programa neleidžia vartotojui tęsti grąžinimo.

> [!NOTE]
> Šiuo metu EKA palaiko tik grąžinimo eilučių serijos numerių tikrinimą, kai pradinis užsakytas kiekis ne didesnis kaip vienas. Jei pradinė pardavimo užsakymo eilutė sukurta ne EKA kanale ir jei kiekis, užsakytas šios pardavimo eilutės eilutėms išdėstyti, yra didesnis nei vienas, per EKA negalima teisingai grąžinti prekės.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kurti grąžinimus EKA](POS-returns.md)

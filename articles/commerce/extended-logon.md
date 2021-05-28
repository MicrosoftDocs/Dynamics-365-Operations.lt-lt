---
title: MPOS ir „Cloud POS“ išplėstinės registracijos funkcijos nustatymas
description: Šioje temoje aprašomos „Cloud POS“ ir „Retail Modern POS“ (MPOS) išplėstinio prisijungimo nustatymo parinktys.
author: rubencdelgado
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f9d8889581e2e11fa5261805c866a6014df57611
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027581"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a>MPOS ir „Cloud POS“ išplėstinės registracijos funkcijų nustatymas

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos „Cloud POS“ ir „Retail Modern POS“ (MPOS) išplėstinio prisijungimo nustatymo parinktys.

## <a name="setting-up-extended-logon"></a>Išplėstinės registracijos nustatymas

Brūkšninių kodų skaičių sekų sąranką galite rasti pasirinkdami **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA šablonai** &gt; **Funkcijų šablonai**. „FastTab“ **Funkcijos** pateikiamos toliau nurodytos parinktys, susijusios su išplėstine registracija.

### <a name="staff-bar-code-logon"></a>Darbuotojo brūkšninio kodo registravimas

Kai parinktis **Darbuotojo brūkšninio kodo registravimas** įjungta, darbuotojai, kurių elektroninio kasos aparato (EKA) kredencialams priskirta išplėstinės registracijos funkcija, gali prisijungti naudodami brūkšninį kodą.

### <a name="staff-bar-code-logon-requires-password"></a>Darbuotojui registruojantis naudojant brūkšninį kodą reikia slaptažodžio

Kai parinktis **Darbuotojui registruojantis naudojant brūkšninį kodą reikia slaptažodžio** įjungta, darbuotojų brūkšninio kodo registracijos funkcija parenka tik tą darbuotoją, kuris yra priskirtas pateiktai išplėstinei registracijai. Kai ši parinktis įjungta, darbuotojai vis tiek turi įvesti savo slaptažodį.

### <a name="staff-card-logon"></a>Darbuotojo kortelės registravimas

Kai parinktis **Darbuotojo kortelės registravimas** įjungta, darbuotojai, kurių EKA kredencialams priskirta išplėstinės registracijos funkcija, gali prisijungti naudodami magnetinę juostelę.

### <a name="staff-card-logon-requires-password"></a>Darbuotojui registruojantis naudojant kortelę reikia slaptažodžio

Kai parinktis **Darbuotojui registruojantis naudojant kortelę reikia slaptažodžio** įjungta, darbuotojų kortelės registracijos funkcija parenka tik tą darbuotoją, kuris yra priskirtas pateiktai išplėstinei registracijai. Kai ši parinktis įjungta, darbuotojai vis tiek turi įvesti savo slaptažodį.

## <a name="assigning-an-extended-logon"></a>Išplėstinės registracijos priskyrimas

Pagal numatytuosius parametrus tik vadovai gali darbuotojams priskirti išplėstinės registracijos funkciją. Norėdami priskirti išplėstinės registracijos funkciją, EKA pasirinkite **Išplėstinė registracija**. Tada ieškokite darbuotojo, ieškos lauke įvesdami darbuotojo operatoriaus ID. Pasirinkite darbuotoją ir spustelėkite **Priskirti**. Kitame puslapyje perbraukite arba nuskaitykite išplėstinę registraciją, kad priskirtumėte darbuotoją. Jei perbraukimas arba nuskaitymas sėkmingas, mygtukas **Gerai** tampa aktyvus. Spustelėkite **Gerai**, norėdami įrašyti to darbuotojo išplėstinę registraciją.

## <a name="deleting-an-extended-logon"></a>Išplėstinės registracijos naikinimas

Norėdami panaikinti darbuotojui priskirtą išplėstinę registraciją, ieškokite darbuotojo naudodami operaciją **Išplėstinė registracija**. Pasirinkite darbuotoją ir spustelėkite **Atšaukti priskyrimą**. Pašalinami visi su tuo darbuotoju susieti išplėstinės registracijos kredencialai.

## <a name="extending-extended-logon"></a>Išplėstinės registracijos išplėtimas

Registravimosi paslaugą galima išplėsti, kad būtų palaikomi papildomi išplėstinės registracijos įrenginiai, pvz., delnų skaitytuvai. Daugiau informacijos ieškokite EKA išplečiamumo dokumentuose.

## <a name="using-extended-logon"></a>Išplėstinės registracijos naudojimas

Jei išplėstinė registracija yra sukonfigūruota, o darbuotojui buvo priskirtas brūkšninis kodas arba magnetinė juostelė, darbuotojas tiesiog turi perbraukti arba nuskaityti savo kortelę, kai rodomas EKA registracijos puslapis. Jei prieš tęsiant registraciją būtina įvesti slaptažodį, darbuotojas bus paragintas įvesti savo slaptažodį.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
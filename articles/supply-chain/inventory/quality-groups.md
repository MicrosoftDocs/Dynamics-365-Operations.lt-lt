---
title: Prekių kokybės grupės
description: Šioje temoje aprašoma, kaip naudoti ir sukurti prekių kokybės grupes, norint logiškai grupuoti produktus, kad jie būtų priskirti automatinio kokybės užsakymų generavimo kokybės susiejimams.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f7a4932c561c052bec1eb0094a390e315b9b1bb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580917"
---
# <a name="item-quality-groups"></a>Prekių kokybės grupės

[!include [banner](../includes/banner.md)]

Kokybės grupė nurodo bendruosius prekių tikrinimo reikalavimus. Šioje temoje aprašoma, kaip naudoti ir sukurti prekių kokybės grupes, norint logiškai grupuoti produktus, kad jie būtų priskirti automatinio kokybės užsakymų generavimo kokybės susiejimams.

Naudodami šį puslapį galite nustatyti, redaguoti ir peržiūrėti kokybės grupei priskirtas prekes arba kokybės grupes, priskirtas prekei, eikite į **Atsargų valdymas \> Nustatymai \> Kokybės grupės**. **Bandymų grupių** puslapyje apibrėžę bandymų reikalavimus, galite apibrėžti taisykles, skirtas automatiškai generuoti kokybės užsakymams. Kad procesas būtų paprastesnis, nenustatinėjate taisyklių atskiroms prekėms. Vietoj to taisykles apibrėžiate kokybės grupei, naudodami **Kokybės susiejimų** puslapį.

## <a name="example-of-an-item-quality-group"></a>Prekių kokybės grupės pavyzdys

Gamybos įmonė perka įvairių žaliavų, kurių gaunamų objektų patikrinimo bandymų reikalavimai tokie patys. Dėl to, įmonė apibrėžia kokybės grupę ir tada tai grupei priskiria prekių numerius, susietus su žaliavomis. Vėliau įmonė perka naują žaliavos tipą, kurio bandymų reikalavimai tokie patys. Užuot nustatydama naujosios medžiagos naujus bandymų reikalavimus, įmonė naujos medžiagos prekės numerį prideda į esamą kokybės grupę.

Ta pati gamybos įmonė taip pat gamina prekes, kurių gamybos bandymų reikalavimai tokie patys, ir siunčia prekes, kurių tie patys reikalavimai bandymams prieš siuntimą. Dėl to, įmonė apibrėžia dvi papildomas kokybės grupes ir tada kiekvienai grupei priskiria atitinkamus prekių numerius.

## <a name="create-a-quality-group"></a>Kurti kokybės grupę

Norėdami sukurti kokybės grupę, atlikite tolesnius veiksmus.

1. Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Kokybės grupės**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Kokybės grupė** – įveskite unikalų kokybės grupės ID arba pavadinimą.
    - **Aprašas** – įveskite išsamų kokybės grupės aprašą.

1. Uždarykite puslapį.

## <a name="manually-add-items-to-a-quality-group"></a>Rankiniu būdu įtraukite prekes į kokybės grupę

Norėdami rankiniu būdu įtraukti prekes į kokybės grupę, atlikite šiuos veiksmus.

1. Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Kokybės grupės**.
1. Pasirinkite kokybės grupę, į kurią norite įtraukti prekes.
1. Veiksmų srityje pasirinkite **Prekės**.
1. Puslapyje **Prekių kokybės grupės** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį. Tada nustatykite naujos eilutės **lauką** Prekės numeris kaip prekės numerį, kurį norite pridėti.
1. Pakartokite ankstesnį veiksmą su kiekviena papildoma preke, kurią reikia pridėti.
1. Uždarykite puslapius.

## <a name="add-multiple-items-to-a-quality-group"></a>Įtraukite kelias prekes į kokybės grupę

Norėdami rankiniu būdu įtraukti kelias prekes į kokybės grupę, atlikite šiuos veiksmus.

1. Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Kokybės grupės**.
1. Kurkite ar rinkitės kokybės grupę, į kurią norite įtraukti prekes.
1. Veiksmų srityje pasirinkite **Įtraukti prekes**.
1. Į **užklausos** dialogo langą įvesti elementų, kuriuos norite įtraukti, filtro kriterijus. Pavyzdžiui, galite filtruoti visas konkrečios prekių grupės prekes.
1. Pasirinkite **Gerai**.
1. Dialogo lange **Įtraukti elementus rodomas visas** užklausą atitinkančias prekes. Peržiūrėkite rezultatus.

    Jei reikia atlikti kokius nors pakeitimus, **pasirinkite** Pasirinkti, norėdami grįžti į **užklausos dialogo langą ir** pakoreguokite savo užklausą.

1. Kai rezultatuose yra visos norimos pridėti prekės, pasirinkite **Gerai**.
1. Uždarykite puslapį.

## <a name="manually-associate-an-item-with-a-quality-group"></a>Rankiniu būdu susieti prekę su kokybės grupe

Norėdami rankiniu būdu susieti prekes su kokybės grupe, atlikite šiuos veiksmus.

1. Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Prekės kokybės grupės**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Prekės numeris** – pasirinkite norimą pridėti prekės numerį.
    - **Kokybės grupė** – pasirinkite kokybės grupę, norimą priskirti prekei.

1. Pakartokite ankstesnį veiksmą su kiekviena papildoma prekės ir kokybės grupės, kurią reikia pridėti, kombinacija.
1. Uždarykite puslapius.

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>Rankiniu būdu įtraukti kokybės grupę iš puslapio Išleisti produktai

Norėdami rankiniu būdu įtraukti kokybės grupę iš **Išleistų produktų** puslapio, atlikite šiuos žingsnius.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite produktą, kuriam norite priskirti kokybės grupę.
1. Veiksmų srityje, skirtuke **Tvarkyti atsargas**, grupėje **Kokybė**, pasirinkite **Prekės kokybės grupės**.
1. Puslapyje **Prekių kokybės grupės** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį. Tada nustatykite naujos eilutės lauką **Kokybės grupė kaip kokybės** grupę, kurią norite priskirti produktui.
1. Pakartokite ankstesnį veiksmą kiekvienai papildomai kokybės grupei, kurią norite priskirti produktui.
1. Uždarykite puslapius.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo bandymo instrumentai](quality-test-instruments.md)
- [Kokybės valdymo bandymai](quality-tests.md)
- [Kokybės valdymo bandymo grupės](quality-test-groups.md)
- [Kokybės valdymo bandymo kintamieji](quality-test-variables.md)
- [Kokybės susiejimai](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

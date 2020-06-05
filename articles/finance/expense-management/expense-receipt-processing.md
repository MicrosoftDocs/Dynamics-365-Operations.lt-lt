---
title: Išlaidų kvitų apdorojimas
description: Šioje temoje pateikiama informacija apie kvitų apdorojimą naudojant optinį ženklų atpažinimą (OCR). Ši funkcija sukurta siekiant pagerinti vartotojo patirtį kuriant išlaidų ataskaitas programoje „Microsoft Dynamics 365 Finance“.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378236"
---
# <a name="expense-receipt-processing"></a>Išlaidų kvitų apdorojimas

[!include [banner](../includes/banner.md)]

Išlaidų įvedimas buvo patobulintas įvedus kvitų apdorojimą per optinį ženklų atpažinimą (OCR). Ši funkcija sukurta siekiant pagerinti vartotojo patirtį kuriant išlaidų ataskaitas.

## <a name="key-features"></a>Pagrindinės funkcijos

- Prekybininko pavadinimas, data ir bendra suma paimami iš kvitų.
- Funkcija bando sugretinti nepridėtus kvitus su nepridėtomis išlaidų operacijomis.
- Vartotojai gali kurti rankiniu būdu įvestas išlaidų operacijas pagal kvitus.

## <a name="usage-examples"></a>Naudojimo pavyzdžiai

Norėdami automatiškai pridėti kvitus, kuriuose yra kredito kortelės operacijų, kai sukuriama išlaidų ataskaita, atlikite toliau nurodytus veiksmus.

  1. Atidarykite darbo sritį **Išlaidų valdymas**.
  2. Skirtuke **Kvitai** patikrinkite, ar yra nepridėtų kvitų. Skirtuke **Kvitai** taip pat galite nusiųsti kvitus.
  3. Skirtuke **Išlaidos** patikrinkite, ar yra nepridėtų išlaidų. Paprastai išlaidų administratorius importuoja šias išlaidas iš kredito kortelės teikėjo.
  4. Pasirinkite **Nauja išlaidų ataskaita**. Atkreipkite dėmesį, kad kurdami išlaidų ataskaitą, dabar taip pat galite į ją įtraukti išlaidų ir kvitų. Jei įtrauksite ir išlaidų, ir kvitų, paleidžiamas automatinis kvitų ir išlaidų gretinimas.

Norėdami kurti išlaidas arba sugretinti išlaidas iš kvito, atlikite toliau nurodytus veiksmus.

  1. Išlaidų ataskaitoje skirtuke **Kvitai** pridėkite kvitą, pasirinkdami **Įtraukti kvitų**.
  2. Atkreipkite dėmesį, kad po nusiųsto kvito vaizdu yra parinktys **Kurti** ir **Sugretinti**.

      - Pasirinkite **Kurti**, kad sukurtumėte rankiniu būdu įvestą išlaidų operaciją ir įvestumėte iš kvito paimtas vertes.
      - Jei pasirinksite **Sugretinti**, sistema bandys sugretinti esamas išlaidas su kvitu.

## <a name="installation"></a>Diegimas

Ši funkcija veikia kartu su funkcija **Išlaidų ataskaitos iš naujo atvaizduotos**, kad išlaidų patirtis būtų paprastesnė. Ši funkcija galima tik 2 ir vėlesnių pakopų aplinkose, kurios yra smėlio dėžės ir gamybos aplinkos.

Norėdami naudoti šias išplėstines išlaidų galimybes, įdiekite „Microsoft Dynamics 365 Finance“ išlaidų valdymo paslaugos papildinį ir įjunkite funkcijas savo egzemplioriuje. Papildinį galite pasiekti iš savo projekto „Microsoft Dynamics Lifecycle Services“ (LCS).

1. Prisijunkite prie LCS ir atsidarykite pageidaujamą aplinką.
2. Eikite į **Išsami informacija**.
3. Pasirinkite **Tvarkyti**arba slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.
4. Pasirinkite **Diegti naują papildinį**.
5. Pasirinkite **Išlaidų valdymo paslauga**.
6. Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.
7. Pasirinkti **Diegti**.

Darbo srityje **Funkcijų valdymas** įjunkite toliau pateikiamas funkcijas.

- Išlaidų ataskaitos iš naujo atvaizduotos
- Automatiškai suderinkite ir sukurkite išlaidas pagal kvitą.

Kai įjungiate šias funkcijas, atliekami tolesni veiksmai.

- Esama darbo sritis **Išlaidų valdymas** pakeičiama nauja darbo sritimi.
- Įtrauktas naujas meniu elementas išlaidų lauko matomumui.
- Vis tiek galite atidaryti ankstesnį puslapį **Išlaidų ataskaitos**, perėję į **Išlaidų valdymas > Mano išlaidos > Išlaidų ataskaitos**.
- Darbo eigos ir patvirtinimai vis dar nukreipia į esamą išlaidų ataskaitų puslapį.
- Kvitai bus apdorojami naudojant „Microsoft Azure Cognitive Services“, o metaduomenys bus gaunami ir įtraukiami.
- Pridėta parinktis, leidžianti sukurti išlaidų ataskaitą, kurioje yra sugretintų nepridėtų kvitų.
- Parinktis, kuri įtraukiama į išlaidų ataskaitas, leidžia sukurti išlaidų eilutę pagal kvitą arba bando sugretinti esamą kvitą ir esamą išlaidų eilutę.

Daugiau informacijos apie funkciją Išlaidų ataskaitos iš naujo atvaizduotos žr. [Išlaidų ataskaitos iš naujo atvaizduotos](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

**Ar „Microsoft“ savo modeliuose naudoja mano duomenis?**

Ne, „Microsoft“ savo kvitų apdorojimo paslaugai sukūrė bendrą mašininio mokymo modelį. Šis modelis negrindžiamas kvitais, kuriuos nusiunčiate.

**Kur ši funkcija yra pasiekiama ir apdorojama?**

Šiuo metu palaikomos Jungtinės Valstijos.

**Kas atsitinka mano kvitams?**

„Finance“ susisieks su „Cognitive Services“, kad gautų laukų duomenis. „Cognitive Services“ saugo jūsų kvito kopiją iki 24 valandų, kol vyksta apdorojimas. Baigus apdoroti, „Cognitive Services“ pašalins kvitą. Kvitai vis tiek saugomi „Finance“.

Norėdami gauti daugiau informacijos, žr. [Įjungti kvitų supratimą naudojant naują formų atpažinimo funkcijos galimybę](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).

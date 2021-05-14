---
title: Kokybės valdymo bandymo kintamieji
description: Šioje temoje aprašoma, kaip sukurti tikrinimo priemones, kurias galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e94972b41baf3f59a633fa7bbc7434abfb90460
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956759"
---
# <a name="quality-management-test-variables"></a>Kokybės valdymo bandymo kintamieji

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti tikrinimo priemones, kurias galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.

Turite apibrėžti kiekvieno kokybinio bandymo, kuris apibrėžtas puslapyje **Bandymai**, turite nustatyti kintamąjį ir galimus rezultatus. (Kokybinių bandymų **tipas** laukelis **Bandymų** puslapyje nustatytas į *Parinktis*.)

Naudokitee **Bandymo kintamųjų** puslapį siekiant nustatyti, redaguoti ir peržiūrėti galimus rezultatus testo kintamajam, susietam su kokybės testu. Kiekvienam rezultatui priskiriate rezultato būseną Teigiamas arba Nesėkmingas, kad nurodytų, ar tikrinimas buvo perduotas ar nesėkmingas, kai šis rezultatas pasirenkamas *kaip* tikrinimo *rezultatas*. Naudokite **Bandymų grupių** puslapį, kad atskiram kokybiniam bandymui priskirtumėte bandymų kintamąjį ir numatytąjį rezultatą.

Kiekvienam bandymo kintamajam rekomenduojame nustatyti bent du rezultatus: vieno rezultato būsena yra Perdavimas, o jo rezultato *būsena* – *Nepavyko*. Nėra bendro kintamųjų arba pasekmių, kurias galima nustatyti, skaičiaus limito. Be to, norėdami įrašyti rezultatus, keliuose bandymuose gali būti naudojami tie patys bandymo kintamieji.

## <a name="examples-of-test-variables"></a>Bandymo kintamųjų pavyzdžiai

### <a name="example-1"></a>1 pavyzdys

Gamybos įmonė atlieka du pagamintų medžiagų bandymus. Vieno bandymo metu pH lygis siejamas su spalvos juostelėmis. Priimtini pH lygiai yra šviesesnės spalvos, o nepriimtina pH lygiai yra tamsesnės spalvos. Atliekant kitą tikrinimą atliekami keli vaizdiniai tikrinimai, o kokybės darbuotojai naudoja savo patikrą, norėdami nustatyti, ar prekė įeina, ar neiš tikrina vaizdinio tikrinimo.

### <a name="example-2"></a>2 pavyzdys

Gamybos įmonė, kepanti sausainius, naudoja galutinio produkto bandymą. Šis bandymas turi keletą kintamųjų. Vienas kintamasis yra skonis, ir galimi šio kintamojo rezultatai yra „geras“ ir „blogas“. Antras kintamasis yra spalva, ir galimi rezultatai yra „per tamsūs“, „per šviesūs“ ir „tinkami“.

## <a name="create-a-test-variable"></a>Naujo bandymo kintamojo kūrimas

Atlikite šiuos žingsnius, kad sukurtumėte bandymo kintamąjį.

1. Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Kintamųjų testavimas**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Kintamasis** – įveskite unikalų kintamojo prietaiso ID arba pavadinimą.
    - **Aprašas** – įveskite išsamų bandymo kintamojo aprašą.

1. Kol nauja eilutė vis dar pasirinkta, **Rezultatai** Neatitikties tipai.
1. Puslapyje **Bandymo kintamojo rezultatai** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Išvados** – įveskite unikalų išvados ID arba pavadinimą.
    - **Aprašas** – įveskite išsamų išvados aprašą.
    - **Išvados būsena** – Rinkitės *atitiko* ar *neatitikol* kad nurodytumėte, ar tikrinimas buvo perduotas ar nesėkmingas, kai šis rezultatas pasirenkamas.

1. Pakartokite ankstesnį veiksmą kiekvienam papildomam rezultatui. Įsitikinkite, kad bent vieno rezultato būsena yra *Perdavimas, o bent vieno* rezultato būsena yra *Nepavyko*.
1. Uždarykite puslapius.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo bandymo instrumentai](quality-test-instruments.md)
- [Kokybės valdymo bandymai](quality-tests.md)
- [Kokybės valdymo bandymo grupės](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

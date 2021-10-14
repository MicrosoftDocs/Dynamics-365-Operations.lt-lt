---
title: Pradinio vidinės įmonės pardavimo užsakymo keitimas arba naikinimas
description: Šioje temoje paaiškinama, kaip keisti ir panaikinti pradinio pardavimo užsakymo funkciją
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7bd6bdbf65499e9f18bf6bb5e160a5634bc37fba
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548421"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>Pradinio vidinės įmonės pardavimo užsakymo keitimas arba naikinimas

[!include [banner](../../includes/banner.md)]

Pardavimo užsakymus galima keisti, kai pakeitimai automatiškai sinchronizuojami su atitinkamu vidinės įmonės pirkimo užsakymu ir vidinės įmonės pardavimo užsakymu.

> [!NOTE]
> išorinių tiekėjų pirkimo užsakymams pakeitimai nepritaikomi, o pradinio pardavimo eilutės nesujungiamos su išorinio tiekėjo pirkimo užsakymo eilutėmis.

Šioje lentelėje apibendrinami jūsų atlikti pakeitimai ir numatomi rezultatai.

| Operacija | Rezultatas |
|---|---|
| Panaikinti&nbsp;pradinį&nbsp;pardavimo&nbsp;užsakymą&nbsp;užsakymą. | Kartu panaikinami ir susiję vidinės įmonės pirkimo ir pardavimo užsakymai. Jei užsakymo būsena yra **Važtaraštis** arba atitinkanti vėlesnį proceso etapą, pardavimo užsakymo panaikinti neįmanoma. |
| Panaikinti pradinio pardavimo užsakymo eilutę. | Kartu panaikinamos ir susijusios vidinės įmonės pirkimo ir pardavimo užsakymo eilutės. Jei užsakymo būsena yra **Važtaraštis** arba atitinkanti vėlesnį proceso etapą, pardavimo užsakymo eilutės panaikinti neįmanoma. |
| Prie pradinio pardavimo užsakymo pridėti naują pardavimo eilutę. | Nauja pardavimo eilutė sukuriama ir vidinės įmonės pirkimo užsakyme, ir vidinės įmonės pardavimo užsakyme. |
| Pradinio pardavimo užsakymo eilutėje pakeisti kiekį. | Kiekis sinchronizuojamas su vidinės įmonės pirkimo ir pardavimo užsakymo eilutėmis. Grynoji suma perskaičiuojama visuose užsakymuose. |
| Uždrausti tiesioginį pradinio pardavimo užsakymo pristatymą. | Pradinio pardavimo užsakymo lauko **Tiesioginio pristatymo** eisti negalima, jei vidinės įmonės pardavimo užsakymo eilutėje pasiektas minimalus išrinkimo dokumento, išeigos užsakymo arba **Važtaraštis**, **Išvesties užsakymas**, ar **Važtaraščio žurnalas**. Vidinės įmonės pirkimo užsakyme pristatymo adresas pakeičiamas į standartinį pristatymo adresą (standartinio pirkimo užsakymo pristatymo adresą). Be to, vidinės įmonės pirkimo užsakymo eilutės pakeistos į standartinį eilučių pristatymo adresą. Šie laukai yra sinchronizuoti pagal pradinio vidinės įmonės pardavimo užsakymo eilutes. Visose pradinio pardavimo užsakymo eilutėse pristatymo tipas pakeičiamas **Joks**, ir laukas sinchronizuojamas su vidinės įmonės pirkimo užsakymo eilutėmis. išorinių tiekėjų pirkimo užsakymams pakeitimai nepritaikomi, o pradinio pardavimo eilutės nesujungiamos su išorinio tiekėjo pirkimo užsakymo eilutėmis. Be to, atnaujinamos vidinės įmonės pirkimo užsakymo bei eilučių pristatymo datos ir pageidaujamos vidinės įmonės pardavimo užsakymo ir eilučių gavimo ar išsiuntimo datos. |
| Įgalinti tiesioginį pradinio pardavimo užsakymo pristatymą. | Pradinio pardavimo užsakymo lauko **Tiesioginio pristatymo** eisti negalima, jei vidinės įmonės pardavimo užsakymo eilutėje pasiektas minimalus išrinkimo dokumento, išeigos užsakymo arba **Važtaraštis**, **Išvesties užsakymas**, negalite keisti **Tiesioginio pristatymo**. Vidinės įmonės pirkimo užsakyme nurodytas adresas pakeičiamas į pradiniame pardavimo užsakyme nurodytą pristatymo adresą ir susinchronizuojamas su vidinės įmonės pardavimo užsakymu. Visose pradinio pardavimo užsakymo eilutėse pristatymo tipas pakeičiamas **Tiesioginis pristatymas**, ir laukas sinchronizuojamas su vidinės įmonės pirkimo užsakymo eilutėmis. Kiekvienos pradinio pardavimo užsakymo eilutės pristatymo adresas susinchronizuojamas su vidinės įmonės pirkimo ir pardavimo užsakymų eilutėmis. Be to, atnaujinamos vidinės įmonės pirkimo užsakymo bei eilučių pristatymo datos ir pageidaujamos vidinės įmonės pardavimo užsakymo ir eilučių gavimo ar išsiuntimo datos. |
| Pridėti pastabą prie pradinio pardavimo užsakymo antraštės ir eilučių. | Pastaba nukopijuojama į vidinės įmonės pirkimo ir pardavimo užsakymus. |
| Keisti arba naikinti pastabą. | Pakeitus arba panaikinus pastabą, kartu bus pakeistos arba panaikintos ir atitinkamos vidinės įmonės pirkimo ir pardavimo užsakymų pastabos. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Sinchronizuoti perdavimo kodus
description: Šioje temoje paaiškinamas vidinės įmonės depozito kodų kliento informacijos komercijai
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 27b587e576900f2b7f7fed7ee2a27a282306f0fe
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671764"
---
# <a name="synchronize-intercompany-disposition-codes"></a>Sinchronizuoti vidinės įmonės perdavimo kodus

[!include [banner](../../includes/banner.md)]

Siekiant padėti susidoroti su vidinės įmonės grąžinimais „Microsoft Dynamics 365 Supply Chain Management“ suteikia funkcijų, skirtų iš išorės nurodytiems perdavimo kodams su atitinkamais vidiniais perdavimo kodais susieti. Kai vidinės įmonės grandinė nustatoma, perdavimo veiksmai dviejose įmonėse, kurios susietos viena su kita, turi būti tokie patys. Jei jos skiriasi, sinchronizavimo procesas bus nesėkmingas.

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>Apie depozito kodus trijų lygių tiesioginius grąžinimus

Perdavimo kodai yra sinchronizuoti vidinės įmonės pardavimo užsakymo eilutės ir pradinio pardavimo užsakymo eilutės kodai. Tačiau sinchronizavimas turi tik vieną tiesioginę įtaką pradinio pardavimo užsakymo eilutei. Dėl to panaikinamos papildomos eilutės išlaidos, atsižvelgiant į perdavimo kodą ir papildomas išlaidas, nustatytas įmonėje A. Įmonė A yra grąžinimo užsakymą kurianti įmonė.

Trijų lygių tiesioginis pristatymo grandinėje, visi perdavimo veiksmai palaikomi vidinės įmonės pardavimo užsakymo eilutėje tripusio pristatymo grandinėje. Tačiau tais atvejais, jei produktas grąžintas klientui, labai svarbu patvirtinti, jog grąžinimo užsakyme nurodytas pristatymo adresas atitinka pristatymo adresą, kuris nurodytas pradiniame užsakyme.

> [!NOTE]
> Pirkimo užsakymai perdavimo kodų neturi. Todėl vidinės įmonės pardavimo užsakymo ir pradinio grąžinimo sinchronizavimo kodų sinchronizavimas turi būti atliekamas sinchronizuojant pardavimo užsakymo su pardavimo užsakymu kodus.

## <a name="replacing-returned-items"></a>Grąžintų prekių pakeitimas

Jei grąžinta aprėkė pakeista, o pakeitimo užsakymas B įmonėje jau sukurtas, perdavimo kodo pasirinkti nebegalima ir jokių papildomų pakeitimo užsakymų A įmonėje sukurta negali būti.

## <a name="rules-for-intercompany-direct-deliveries"></a>Apie tiesioginius vidinės įmonės taisyklės pristatymus

Vidinės įmonės tiesioginio pristatymo scenarijuose pradiniams grąžinimo užsakymams užsakymams taikomos šios taisyklės:

- Jei pridedamas pradinio pardavimo užsakymo eilutės perdavimo veiksmas yra kreditavimas ir nurašymas į atliekas, nurašymas į atliekas, kreditavimas arba grąžinimas klientui, tada taikomas perdavimo veiksmas yra kreditavimas. Tačiau grąžinimo klientui veiksmo kodas esamoje eilutėje ir naujai sinchronizuotoje pagal vidinės įmonės pardavimo užsakymą eilutėje nustatys grynąją sumą 0 (nulis). Be to, nurašymo į atliekas eilutės niekada nesinchronizuojamos. Kai eilutė pridedama prie vidinės įmonės pardavimo užsakymo, ji niekada nesinchronizuojama su pardavimo užsakymu, kurio kiekis teigiamas, o perdavimo veiksmas nurašymas į atliekas (pvz., kreditavimas ir nurašymas į atliekas arba pakeitimas ir nurašymas į atliekas).
- Neatmestas pagrindinis perdavimo veiksmai kredituoti ir pakeisti arba nurašyti į atliekas ir pakeisti. Jis laikomas pagrindinis perdavimo veiksmai kredituoti ir pakeisti arba nurašyti į atliekas ir pakeisti. Ši taisyklė taikoma net jei įmonėje A nėra sukurta nurašymo eilutė, o įmonėje B (įmonėje, kuri gavo grąžintos prekės) nėra sukurtas joks pakeitimo užsakymas. Pakeitimo užsakymas sukuriamas A įmonėje tik tada, kai vykdomas atnaujintas važtaraštis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

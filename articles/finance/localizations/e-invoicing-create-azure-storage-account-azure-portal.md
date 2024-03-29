---
title: „Azure“ saugyklos paskyros kūrimas „Azure“ portale
description: Šiame straipsnyje paaiškinama, kaip sukurti "Azure" saugyklos sąskaitą elektroniniam SF išrašymui.
author: gionoder
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5eca23985c48f4e577bd4567cc2e324df5aa9690
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291643"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>„Azure“ saugyklos paskyros kūrimas „Azure“ portale

[!include [banner](../includes/banner.md)]

Visi elektroniniai failai, kuriuos sugeneravo elektroninių SF išrašymo tarnyba, arba kurie apdorojami eina į paslaugą, saugomi jūsų saugyklos sąskaitos Microsoft Azure konteineriuose. Norėdami užtikrinti, kad elektroninis SF išrašymas galėtų prieiti prie šių konteinerių, turite pateikti bendrai naudojamos prieigos parašą (SAS) saugojimo abonemento atpažinimo ženklą elektroninių SF išrašymo tarnybai. Be to, norėdami užtikrinti, kad atpažinimo ženklas saugomas saugiai, tiesiogiai nesireikite SAS atpažinimo ženklo. Užduot tai darę, saugokite "Azure" rakto saugykloje ir pateikite "Azure Key" "Vault" slaptą saugyklą.

1. Atidarykite saugojimo abonementą, kurį planuojate naudoti su elektroninių SF išrašymo paslauga.
2. Eikite **į parametrų** \> **konfigūraciją** ir įsitikinkite, kad nustatytas **parametras Leisti BLOB** viešąją prieigą yra įgalintas.**·**
3. Eiti į duomenų **saugojimo konteinerius** \> **ir** kurti konteinerį.
4. Įveskite konteinerio pavadinimą ir nustatykite lauką **Viešosios prieigos lygis** į **Privatus (ne anoniminė prieiga)**.
5. Atidarykite naują konteinerį ir eikite į **parametrų** \> **prieigos strategiją.**
6. Pasirinkite **Įtraukti strategiją**, norėdami įtraukti saugomą prieigos strategiją.
7. Atitinkamai nustatykite **lauką** Identifikatorius.
8. **Teisių lauke** pasirinkite visas teises.

    ![Visos teisės, pasirinktos lauke Teisės dialogo lange Įtraukti strategiją.](media/e-invoicing-azure-1.png)

9. Įveskite pradžios ir pabaigos datas. Galiojimo data turi būti data ateityje.
10. Pasirinkite **Gerai**, norėdami įrašyti strategiją, tada įrašykite konteinerio keitimus.
11. Eikite **į Parametrų** \> **bendrai naudojamos prieigos atpažinimo ženklus** ir nustatykite lauko vertes.
12. Įveskite pradžios ir pabaigos datas. Galiojimo data turi būti data ateityje.
13. **Teisių lauke** pasirinkite šias teises:

    - Skaityti
    - Pridėti
    - Kurti
    - Rašyti
    - Delete
    - Sąrašas

14. Pasirinkite **Generuoti SAS atpažinimo ženklą ir URL**.
15. Nukopijuokite ir saugokite reikšmę **BLOB SAS URL** lauke. Ši vertė bus naudojama vėliau šios procedūros metu ir bus nurodyta kaip bendrai naudojamos prieigos *parašo URI*.
16. Atidarykite raktų saugyklą, kurią planuojate naudoti su elektroninių SF išrašymo priedu.
17. Pereikite prie Parametrų **paslapčių** \> **ir** pasirinkite Generuoti **/Importuoti, norėdami** sukurti slaptą.
18. Puslapio **Sukurti slaptąjį raktą** lauke **Nusiuntimo parinktys** pasirinkite **Rankinis**.
19. Įveskite slaptojo rakto pavadinimą. Šis pavadinimas bus naudojamas atliekant reguliavimo konfigūracijos tarnybos (RCS) *tarnybos sąranką ir bus nurodytas kaip rakto saugyklos slapto vardas*. Norėdami gauti daugiau informacijos apie RCS nustatyti, žr. [Reguliavimo konfigūracijos tarnybos (RCS) nustatyti](e-invoicing-set-up-rcs.md).
20. Reikšmės lauke **įveskite** bendrai naudojamos prieigos parašo URI, kurį nukopijavote anksčiau.
21. Pasirinkite **Kurti**.

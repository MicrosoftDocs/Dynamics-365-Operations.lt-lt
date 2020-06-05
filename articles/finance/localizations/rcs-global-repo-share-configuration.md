---
title: RCS / bendrosios saugyklos ER konfigūracijų bendrinimas su išorinėmis organizacijomis
description: Šioje temoje paaiškinama, kaip „Microsoft Regulatory Configuration Service“ (RCS) / bendrojoje saugykloje esančių elektroninių ataskaitų (ER) konfigūracijas tiesiogiai bendrinti su išorinėmis organizacijomis.
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 04c46824123906eccbfff18a03974c8043729e0a
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371258"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>„Regulatory Configuration Service“ (RCS) bendrojoje saugykloje esančių elektroninių ataskaitų (ER) konfigūracijų bendrinimas su išorinėmis organizacijomis

[!include [banner](../includes/banner.md)]

Elektroninių ataskaitų (ER) konfigūracijoms bendrinti galite naudoti „Microsoft Regulatory Configuration Services“ (RCS), o tada publikuoti jas išorinėse organizacijose.

Toliau aprašytos procedūros paaiškina, kaip RCS vartotojas gali bendrinti RCS egzemplioriuje sukonfigūruotą ER konfigūracijos versiją su išorine organizacija. Kad galėtumėte atlikti šias procedūras, pirmiausia turite įgyvendinti toliau nurodytas būtinąsias sąlygas.

- Pasiekti RCS egzempliorių.
- Sikurti aktyvų konfigūracijos teikėją. Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
- Sukurti ir nusiųsti naują ER konfigūracijos versiją. Daugiau informacijos žr. [Naujos elektroninės ataskaitos (ER) konfigūracijos versijos kūrimas ir nusiuntimas](rcs-global-repo-upload.md).

Taip pat turite įsitikinti, kad RCS aplinka yra parengta jūsų įmonei.

1. Programoje „Finance and Operations“ eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Jei jūsų įmonei RCS aplinka neparengta, pasirinkite **„Regulatory Services“ – išorinė konfigūracija** ir vykdykite instrukcijas, kad ją parengtumėte.

Jei RCS aplinka jūsų įmonei jau parengta, pasiekite ją naudodami puslapio URL ir pasirinkdami prisijungimo parinktį.

## <a name="verify-the-configuration-that-you-want-to-share"></a>Konfigūracijos, kurią norite bendrinti, patikrinimas

Norėdami patikrinti, ar konfigūracija, kurią norite bendrinti, jau nusiųsta į bendrąją saugyklą, atlikite toliau nurodytus veiksmus.

1. Darbo srityje **Elektroninės ataskaitos** prie savo konfigūracijos teikėjo pasirinkite **Saugyklos**.

    ![Konfigūracijos teikėjai](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_config_provider.JPG)

2. Pasirinkite **Bendroji saugykla** \> **Atidaryti**.
3. Ieškoktie konfigūracijos, kurią norite bendrinti. Ieškai susiaurinti galite naudoti filtravimo lauką. Jei bendrojoje saugykloje negalite rasti konfigūracijos, atlikite veiksmus, pateiktus dalyje [Naujos elektroninės ataskaitos (ER) konfigūracijos versijos kūrimas ir nusiuntimas](rcs-global-repo-upload.md).

## <a name="share-er-configurations-with-external-organizations"></a>ER konfigūracijų bendrinimas su išorinėmis organizacijomis

Sukūrus jūsų konfigūracijos teikėjo konfigūraciją, galite ją tiesiogiai bendrinti su išorinėmis organizacijomis, naudodami „FastTab“ konteinerį **Bendrinama su**, esantį puslapyje **Bendroji konfigūracijos saugykla**.

1. Darbo srityje **Elektroninės ataskaitos** prie savo konfigūracijos teikėjo pasirinkite **Saugyklos**.
2. Pasirinkite **Bendroji saugykla** \> **Atidaryti**. 
3. Pasirinkite konfigūraciją, kurią norite bendrinti.
4. „FastTab“ konteineryje **Bendrinama su** pasirinkite **Organizacija**.

    ![Bendrinama su „FastTab“](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_org.JPG)

5. Dialogo lange įveskite išorinės organizacijos domeno pavadinimą ir pasirinkite **Gerai**.

    ![Konfigūracijos versijos bendrinimo su išorine organizacija dialogo langas](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_form.JPG)

Konfigūracija yra bendrinama su išorine organizacija ir šiai organizacijai pasiekiama bendrojoje saugykloje. Iš ten ji gali būti importuota į organizacijos RCS egzempliorių arba į „Finance and Operations“ programų egzempliorius.

![Su išorine organizacija bendrinama konfigūracija](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_test.com)

6. Norėdami atšaukti anksčiau su išorine organizacija bendrintos konfigūracijos bendrinimą, pasirinkite konfigūraciją ir spustelėkite **Atšaukti bendrinimą**, tada pasirinkite **Gerai**.

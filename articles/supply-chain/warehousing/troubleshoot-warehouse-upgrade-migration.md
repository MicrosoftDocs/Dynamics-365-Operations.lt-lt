---
title: Trikčių šalinimo gerinimo ir perkėlimas į papildomą sandėlio valdymą
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti naujindami ir perkeldami siekiant pagerinti sandėlio valdymą.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993896"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Trikčių šalinimo gerinimo ir perkėlimas į papildomą sandėlio valdymą

[!include [banner](../includes/banner.md)]

Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti naujindami ir perkeldami siekiant pagerinti sandėlio valdymą.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Gaunu tolesnį klaidos pranešimą: „java.security.cert.certPathValidatorException: Pasitikėjimo inkaras sertifikavimo keliui nerastas."

### <a name="issue-description"></a>Problemos aprašas

Gavote šį klaidos pranešimą sandėlio programoje, nes savaime prisijungusiais sertifikatais nėra pasitikima „Android“ 8+ patalpų aplinkose.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Naudokite išorės (viešąją) seritfikavimo įstaigą (CA). Šios trikties pašalinimas yra prieinamas sandėlio programose 1.9.0.0 versijoje. Dėl daugiau informacijos apie šią triktį ir kaip ją pataisyti, žr. [Trikties šalinimo sandėlio programos jungties triktys](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Kas yra patvirtintas procesas perkėlimui iš pagrindinio sandėliavimo į pagerintą sandėliavimą?

### <a name="issue-description"></a>Problemos aprašas

Dabar vykdote sandėliavimo/inventoriaus valdymą ir naudojate pagrindines sandėlio funkcijas ir norite perkelti pagerintą sandeliavimą tam, kad pasinaudotumėte mobiliuoju įrenginiu, bangomis ir darbu geriau. Nepaisant to, patiriate trikčių bandydami padaryti šį perkėlimą. Pavyzdžiui, negali pakeisti savo produktų taip, kad jie naudotų talpinimo matmenis (vietą, sandėlį ir vietą), nes produktai turi perlaidas jų atžvilgiu. Dėl to, privalote išmokti patvirtintą procesą perkėlimui iš pagrindinio sandėliavimo į pagerintą sandėliavimą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Dėl daugiau informacijos apie procesą perkėlimui iš pagrindinio sandėliavimo į pagerintą sandėliavimą, žr. tolesnius tinklaraščio įrašus ir dokumentus:

- [Įjungti sandėlio valdymo procesą esantiems elementams ir sandėliams](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [„Microsoft Dynamics AX“ perkėlimas WMS į naują R3 sandėlį ir gabenimo funkcijos](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2 elemento perkėlimas](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Sandėlio valdymo pagerinimas iš „Microsoft Dynamics“ AX 2012 iki „Supply Chain Management“](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)

---
title: Mokesčio kodo nustatyti negalima
description: Šioje temoje paaiškinama, kaip šalinti "Mokesčio kodo nustatyti negalima" klaidą mokesčių skaičiavimo tarnybose.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 3c0914f0013ad2de61cd5a59e3092fef149742e4
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648152"
---
# <a name="tax-code-cannot-be-determined"></a>Mokesčio kodo nustatyti negalima

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinami trikčių diagnostikos veiksmai, kuriuos galite atlikti, jei mokesčių skaičiavimo paslaugoje gaunate klaidą "Mokesčio kodas negali būti nustatytas".

## <a name="symptom"></a>Požymis

Jūs gaunate tokį klaidos pranešimą: "Antraštė/eilutės - 1, mokesčių kodo nustatyti negalima". Taip pat trikčių šalinimo faile rasite klaidą, kaip parodyta toliau pateiktame pavyzdyje. Daugiau informacijos ieškokite trikčių [šalinimo derinimo režimo įgalinimas](tcs-troubleshooting-enable-debug-mode.md).

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Priežastis

Problema gali kartoti, nes mokesčių grupė ir prekės mokesčių grupė nėra susiekę.

## <a name="troubleshoot"></a>Šalinti triktis

Norėdami pašalinti problemą, atlikite šiuos veiksmus.

1. Trikčių šalinimo faile patikrinkite, ar nustatyta mokesčių grupė ir prekės mokesčių grupė. Jei mokesčių grupės **ir prekių** **mokesčių grupės vertės** tuščios, mokesčių grupė ir prekių mokesčių grupė nebuvo nustatytos. Jei jos nustatytos, rezultatai gali būti klaidingi.

    Čia yra trikčių šalinimo failo pavyzdys.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
                            "Adjustment": null
                        }
                    ],
                    "Measures": {
                        ...
                    },
                    ...
                }
            ]
        },
        ...
    }
    ```

2. Patikrinkite, ar **įgalinta pardavimo** užsakymo eilutės informacijos **skirtuko** Nustatymas parinktis Perrašyti PVM.

    - Jį įgalinus, mokesčių kodus nustato **operacijos** **eilutėje** įvedamos mokesčių grupės ir prekių mokesčių grupės vertės. Patikrinkite, ar šios vertės įvestos teisingai.
    - Jei ji neįgalinta, patikrinkite, ar **·** **nustatytos teisingos mokesčių grupės taikomumo ir prekių mokesčių grupės taikomumo laukų** vertės. Daugiau informacijos ieškokite nerastas [nė vienas sutampantys rezultatai](tcs-troubleshooting-no-matching-result.md).

3. Jei mokesčių grupė ir prekės mokesčių grupė teisingai nustatytos, nustatykite, ar yra jų sukirtimas.

    1. RCS eikite į mokesčių **priemonių mokesčių** \> **kodus ir grupes** \> **Mokesčių grupė.**

        | Eilutė. Mokesčių grupė | Mokesčių kodai |
        |----------------|-----------|
        | Grupė A        | „A”         |

    2. Eikite **į Mokesčių priemonės** \> **Mokesčių kodai ir grupės** \> **Prekės mokesčių grupė**.

        | Eilutė. Prekės mokesčių grupė | Mokesčių kodai |
        |---------------------|-----------|
        | Grupė B             | „B”         |

    Jei nėra mokesčių grupės ir prekės mokesčių grupės sukirtimo, mokesčio kodas nebus nustatytas.

## <a name="mitigation"></a>Mažinimo priemonė

1. Pereikite prie kiekvieno šios temos trikčių [diagnostikos](#troubleshoot) skyriaus žingsnio ir pataisykite nustatymą, kaip reikia. Jei mokesčių grupė ir prekių mokesčių grupė nebuvo teisingai nustatytos, žr. [Negretinimo rezultatų.](tcs-troubleshooting-no-matching-result.md)
2. Jei nėra mokesčių grupės ir prekės mokesčių grupės susikirtimo, sukurkite naują RCS priemonių versiją ir pataisykite nustatymą.

    - Eikite **į Mokesčių** \> **priemonės Mokesčių kodai ir groupsItem** > **mokesčių grupė.**

        | Eilutė. Prekės mokesčių grupė | Mokesčių kodai |
        |---------------------|-----------|
        | Grupė B             | A; B       |

    Mokesčio kodas bus nustatytas kaip **A**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

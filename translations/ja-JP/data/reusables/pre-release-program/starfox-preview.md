---
ms.openlocfilehash: 3557e85680e20919fbe049cfe30ccacc93d9c17c
ms.sourcegitcommit: 47bd0e48c7dba1dde49baff60bc1eddc91ab10c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2022
ms.locfileid: "145121390"
---
{% note %}

**注:** プロジェクト カードの詳細が、プロジェクト関連の Issue およびタイムライン イベントの REST API 応答に示されるようになりました。 この機能は、プレビューとして開発者が利用できるようになりました。 詳細については、[ブログ記事](https://developer.github.com/changes/2018-09-05-project-card-events)を参照してください。

`project_card` 属性を受け取るには、リポジトリに対してプロジェクト ボードを[有効](/articles/disabling-project-boards-in-a-repository)にする必要があります。また、`Accept` ヘッダーでカスタム [メディアの種類](/rest/overview/media-types)を指定する必要があります。

```
application/vnd.github.starfox-preview+json
```

{% endnote %}

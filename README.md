# Ultimate Geography（终极地理）

**为[Anki](http://ankisrs.net/)设计的地理知识记忆卡片**，包含：

- 世界上的**[205个主权国家](https://en.wikipedia.org/wiki/List_of_sovereign_states)**（820张卡片）
- **59个领地、世界区域和其他实体**（103张卡片）
- **48个海洋和海域**（仅48张地图卡片）
- **7大洲**（仅7张地图卡片）
- 总计**319个独特笔记**、**978张卡片**、**221面国旗**和**319张地图**。

此卡片组提供多种语言版本：**英语**、**德语**、**西班牙语**、**法语**、**挪威语（书面）**、**捷克语**、**俄语**、**荷兰语**、**瑞典语**、**葡萄牙语**、**中文**（简体和繁体）、**波兰语**、**意大利语**和**丹麦语**。

---

#### 目录

- [**功能特点**](#features)
  - [补充信息](#supplementary-information)
  - [自定义学习](#custom-study)
- [**开始使用**](#getting-started)
- [**升级**](#upgrading)
  - [从APKG导入后首次升级](#first-upgrade-after-apkg-import)
  - [保留卡组自定义设置](#keeping-deck-customisations)
  - [从标准版升级到扩展版（或实验版）](#levelling-up-from-standard-to-extended-or-to-experimental)
  - [主要版本升级](#major-version)
- [**卡组结构**](#deck-structure)
- [**自定义卡组**](#customising-the-deck)
  - [可以保留的更改](#changes-that-are-or-can-be-preserved-)
  - [会被还原的更改](#changes-that-get-reverted-)
  - [会阻止升级的更改](#changes-that-prevent-upgrading-)

## 功能特点

标准版卡组包含四种笔记模板：_国家 - 首都_、_首都 - 国家_、_国旗 - 国家_和_地图 - 国家_。此外还有一个**扩展版**，其中包含两个额外的笔记模板：_国家 - 国旗_和_国家 - 地图_。[实验版](https://github.com/anki-geo/ultimate-geography/wiki/Experimental-extended-deck)是扩展版的克隆版本，但它为_国家 - 地图_笔记模板提供了交互功能。

<table>
  <tr><th scope="col" colspan="2">国旗 - 国家</th></tr>
  <tr><th scope="col">正面</th><th scope="col">背面</th></tr>
  <tr>
    <td><img src="doc/Flag - Country -- Front -- Christmas island.png"></td>
    <td><img src="doc/Flag - Country -- Back -- Christmas island.png"></td>
  </tr>
</table>

<table>
  <tr><th scope="col" colspan="2">地图 - 国家</th></tr>
  <tr><th scope="col">正面</th><th scope="col">背面</th></tr>
  <tr>
    <td><img src="doc/Map - Country -- Front -- Mexico.png"></td>
    <td><img src="doc/Map - Country -- Back -- Mexico.png"></td>
  </tr>
</table>

<table>
  <tr><th scope="col" colspan="2">国家 - 首都</th></tr>
  <tr><th scope="col">正面</th><th scope="col">背面</th></tr>
  <tr>
    <td><img src="doc/Country - Capital -- Front -- Sri Lanka.png"></td>
    <td><img src="doc/Country - Capital -- Back -- Sri Lanka.png"></td>
  </tr>
</table>

<table>
  <tr><th scope="col" colspan="2">首都 - 国家</th></tr>
  <tr><th scope="col">正面</th><th scope="col">背面</th></tr>
  <tr>
    <td><img src="doc/Capital - Country -- Front -- Finland.png"></td>
    <td><img src="doc/Capital - Country -- Back -- Finland.png"></td>
  </tr>
</table>

### 补充信息

为了帮助记忆并在学习过程中提供背景信息，大多数笔记包含额外的信息：

- **相似国旗** - 例如，冰岛 = _挪威（红色背景，蓝色十字）_
- **治理信息** - 例如，开曼群岛 = _英国的海外领土_
- **替代和前国名** - 例如，东帝汶 = _也称为东帝汶_
- **其他首都信息** - 例如，苏克雷，玻利维亚 = _虽然苏克雷是宪法规定的首都，但拉巴斯是政府所在地。_
- **国家地位信息** - 例如，德涅斯特里 = _被摩尔多瓦声称的独立国家_。

### 自定义学习

Anki的[搜索功能](https://docs.ankiweb.net/searching)结合卡组全面的[标签结构](#deck-structure)，允许创建[过滤卡组](https://docs.ankiweb.net/filtered-decks#creating-manually)来满足各种学习目标和能力。以下是一些可用的搜索查询：

- `card:"Flag - Country"` 仅学习国旗；
- `tag:UG::Sovereign_State` 专注于主权国家，不包括属地、水域和大陆；
- `-tag:"UG::Oceans+Seas"` （在过滤器前加上"`-`"）学习除海洋、海域和其他水域外的所有内容；
- `card:"Map - Country" tag:UG::Sovereign_State tag:UG::Europe` 学习欧洲主权国家的地理位置；
- `(card:"Country - Capital" or card:"Capital - Country") tag:UG::Sovereign_State` 学习世界主权国家的首都；
- `tag:UG::North_America -tag:UG::Caribbean` 专注于北美洲的国家，但不包括加勒比海地区（即只包含北美和中美地区）。

另一种方式是，不将你想要的卡片子集移入过滤卡组，而是暂停其余卡片。在这种情况下，你需要搜索你想要的子集的反向集合，然后[暂停](https://docs.ankiweb.net/browsing.html?highlight=suspend#cards)这些搜索结果。例如，要仅学习国旗（如上面的第一个例子），你应该搜索`deck:"Ultimate Geography" -card:"Flag - Country"`。（你需要第一个条件只在UG卡组中搜索，并使用`-`表示反向。）暂停卡片的优点是过滤卡组没有便捷的方式来配置每日新卡片限制。缺点是操作略显繁琐，尤其是如果你计划后续学习剩余的卡片（你需要暂停和取消暂停卡片）。

## 开始使用

第一次使用？欢迎！👋

要安装并在以后升级 _终极地理_，你需要先安装一个名为 [CrowdAnki](https://github.com/Stvad/CrowdAnki) 的 Anki 插件：

1. 在你的电脑上打开 Anki，进入 _工具_ 菜单并选择 _插件_。
1. 在对话框中，点击 _获取插件..._ 并粘贴[该页面](https://ankiweb.net/shared/info/1788670778)上提供的代码。
1. 点击 _确定_ 来安装插件，然后重启 Anki。

你现在已准备好安装 _终极地理_：

1. 前往 **[_发布页面_](https://github.com/anki-geo/ultimate-geography/releases)**。
1. 在最新发布版本的 _资源_ 部分，下载你想要使用的卡组版本的 ZIP 压缩包。你可以在多种[语言](#ultimate-geography)中选择[标准版、扩展版和实验版](#features) -- 例如，如果你需要标准德语版本，下载 `Ultimate_Geography_v[...]_DE.zip`。
1. 将压缩包内容解压到你的计算机上。
1. 打开 Anki 并确保你的所有设备均已同步。
1. 通过 _文件 -> 创建备份_ 创建[手动备份](https://docs.ankiweb.net/backups.html#creating)，以防出现问题。
1. 在 _文件_ 菜单中，选择 _CrowdAnki: 从磁盘导入_。
1. 浏览并选择你从压缩包中提取的文件夹，该文件夹包含卡组的 JSON 文件和 `media` 文件夹 -- 例如 `Ultimate Geography [DE]`。
1. 在打开的 _CrowdAnki 导入设置_ 对话框中不要更改任何内容 -- 直接按 _确定_ 开始导入。然后应该会出现一个对话框，确认导入成功。

👉 要及时了解新版本，请确保[关注该仓库的发布](https://help.github.com/en/articles/watching-and-unwatching-releases-for-a-repository)。

## 升级

升级过程通常与[前面部分](#getting-started)所解释的安装过程相同。然而，某些情况需要额外注意。作为一般原则，**始终仔细阅读发布说明**；它们通常会告诉你如何操作或将你引导到相关页面。

### 从APKG导入后首次升级

你可能最初是通过导入**APKG文件**安装_终极地理_的。你可能从这个仓库或从AnkiWeb上的[卡组页面](https://ankiweb.net/shared/info/2109889812)下载了这样的文件，因为这曾经是推荐的安装方式。

如果你处于这种情况并希望升级，请按以下步骤操作：

1. 精确执行_开始使用_部分的步骤。
1. 你应该会得到两个卡组：你的原始卡组名为“终极地理”和一个新的、重复的卡组名为“终极地理_2”。除非你创建了一些自己的笔记，否则你原始卡组中的每张卡片应该已自动移动到新卡组中，而你的原始卡组现在应该是空的。你可以在Anki的[卡片浏览器](https://docs.ankiweb.net/browsing)中验证这一点。
1. 要回到只有一个卡组的状态，将你自己的卡片从原始卡组移出并删除原始卡组。然后，将新卡组重命名为“终极地理”。从这里开始，以后的升级将非常顺利。

如果你是从v3.3或更早版本升级，那么你可能还需要遵循[v4.0发布版的说明](https://github.com/anki-geo/ultimate-geography/releases/tag/v4.0)。

### 保留卡组自定义设置

如果你已经对你的_终极地理_卡组进行了任何更改，或者正在考虑进行更改，请查看下面的[自定义卡组](#customising-the-deck)部分，了解在下次升级时这些更改会发生什么情况，以及你是否需要采取任何措施来保存这些更改。

### 从标准版升级到扩展版（或实验版）

在标准版卡组上导入扩展版卡组是棘手的，需要小心操作。你可能更值得考虑从头开始学习扩展版卡组。要做到这一点，可以：

- 首先按照下面[主要版本升级](#major-version)部分的说明删除标准版卡组，或者
- 在单独的Anki配置文件中导入扩展版卡组。

如果你想保留你的学习进度，请按照以下步骤操作：

1. 精确执行_开始使用_部分的步骤。
1. 不会出现确认导入成功的对话框，而是会出现另一个标题为_更改笔记类型_的对话框。在_卡片_部分，将_将Flag - Country更改为:_设置为"Flag - Country"（而非"Country - Flag"），并将_将Map - Country更改为:_设置为"Map - Country"（而非"Flag - Country"）。
1. 检查其他卡片和字段是否正确映射，然后点击_确定_开始导入。

从标准版切换到扩展版的“映射”，以及所有当前可能的卡组类型变更的表格格式可以在[这里](https://github.com/anki-geo/ultimate-geography/wiki/Switching-deck-type#specific-guides)找到。

### 主要版本升级

主要版本（如`v3.0`）通常表示，[“常规方式”](#upgrading)升级可能会导致重要的学习进度丢失，或者失去你对卡组进行的、原本可以被保留的[一些自定义设置](#customising-the-deck)。例如，当卡组结构发生[重大变化](https://github.com/anki-geo/ultimate-geography/releases/tag/v3.0)时，就可能会发生这种情况。

wiki上的[发布说明](https://github.com/anki-geo/ultimate-geography/releases)和[升级指南](https://github.com/anki-geo/ultimate-geography/wiki/Upgrade-instructions)通常会提供一种方法，让你在_不_丢失学习进度的情况下升级到主要版本。然而，在某些情况下，这个过程可能会很棘手。😰 如果保留学习进度不值得花费这些精力，或者如果你只是想从头开始重新学习这个卡组，那么我们建议你执行“清洁导入”，如下：

1. 打开Anki并确保你的所有设备均已同步。
1. 删除`终极地理`卡组。
1. 在_工具_菜单中，选择_管理笔记类型_，然后删除`终极地理`笔记类型。
1. 在_工具_菜单中，选择_检查数据库_。
1. 将变更与AnkiWeb和所有设备同步。
1. 现在你可以按照[开始使用](#getting-started)部分的步骤来安装主要版本。

## 卡组结构

笔记基于一种名为_终极地理_的**笔记类型**，它定义了**八个字段**：_国家_、_国家信息_、_首都_、_首都信息_、_首都提示_、_国旗_、_国旗相似性_和_地图_。

卡片在导入时由Anki根据**四种模板**生成：_国家 - 首都_、_首都 - 国家_、_国旗 - 国家_和_地图 - 国家_。卡组的扩展版包含两个额外的模板：_国家 - 国旗_和_国家 - 地图_。

卡片的外观完全由CSS控制；笔记的内容不包含HTML标记。

每个笔记都有标签。这些标签按类别列出，以`UG::`为前缀，以避免与其他卡组冲突。它们可用于为[自定义学习](#custom-study)创建[过滤卡组](https://docs.ankiweb.net/filtered-decks#creating-manually)。

- 类型 - `UG::Sovereign_State`（主权国家）、`UG::Oceans+Seas`（海洋和海域）、`UG::Continents`（大洲）
- 大洲 - `UG::Africa`（非洲）、`UG::Asia`（亚洲）、`UG::Europe`（欧洲）、`UG::North_America`（北美洲）、`UG::Oceania`（大洋洲）、`UG::South_America`（南美洲）
- 地区 - `UG::Caribbean`（加勒比海）、`UG::Middle_East`（中东）、`UG::Southeast_Asia`（东南亚）、`UG::European_Union`（欧盟）、`UG::Mediterranean`（地中海）、`UG::East_Africa`（东非）、`UG::West_Africa`（西非）

## 自定义卡组

有兴趣在Anki中对卡组进行更改？以下是你需要了解的内容。

### 可以保留的更改 💖

- **添加你自己的卡片和媒体文件**

  尽情发挥。🌊 升级不会影响你创建的新卡片，或你添加到新卡片中的任何新媒体文件。

  如果[在导入时创建了重复的卡组](#first-upgrade-after-apkg-import)，你自己的卡片将保留在原始卡组中。

- **将卡片移入另一个卡组**

  一些人希望把多个卡组合并到一个卡组中以便于一起复习。

  默认情况下，CrowdAnki在导入时会将所有卡片移回到_终极地理_卡组中。要防止这种行为并就地更新现有卡片，请确保在按照[开始使用](@getting-started)部分的步骤操作时，在_CrowdAnki导入设置_对话框中勾选_不移动现有卡片_复选框。

  > 请注意，如果你之前删除了_终极地理_卡组，它将被重新创建，并可能包含新卡片。

- **更改卡组的选项**

  卡组选项包括，例如，每天的新卡片数量、每天的最大复习数量等。

  在首次导入卡组时，CrowdAnki会创建一个名为_终极地理_的新“选项组”（除非它已经存在）。如果你对这个组的选项进行了任何更改，它们在导入时将被恢复。

  为了避免失去你的选项，创建你自己的选项组并给它一个独特的名称。升级后，你只需要将卡组切换回这个选项组。

- **自定义模板和样式**

  你对_终极地理_笔记类型的内置模板所做的任何编辑在升级时都会被恢复。所有模板共享的CSS样式也是如此。

  一种解决方法并保留你的更改是首先[克隆笔记类型](https://docs.ankiweb.net/editing#adding-a-note-type)，然后在Anki浏览器中将所有卡片切换到新的笔记类型。你然后可以在克隆的笔记类型中进行模板和样式的更改，而不会影响原始笔记类型。下次升级时，所有卡片将切换回原始笔记类型，但你可以在Anki浏览器中轻松将它们切换回你的自定义笔记类型。

  > 请注意，之后你可能需要更新你的自定义模板和样式，以保持与内置模板一致。

  警告⬇️：上述解决方法不保证有效，所以在升级前，你可能希望先通过CrowdAnki导出来备份你的本地卡组。

### 会被还原的更改 😬

下面列出的更改将在下次升级时丢失，除了在升级后再次手动进行更改外，没有其他解决方法。

- **重命名卡组或更改其描述**

  升级始终会恢复卡组的默认名称和描述。

- **编辑笔记的内容**

  例如：

  - 在库拉索的_国家信息_字段中添加指向维基百科的链接；
  - 在波兰的_国旗相似性_字段中添加你自己的记忆提示；
  - 在笔记中添加或删除标签；
  - 重命名标签。

  > 如果你纠正了拼写错误或其他错误，不要忘记[提交问题](https://github.com/anki-geo/ultimate-geography/issues/new)或发起合并请求，这样你就不会在下次升级时丢失你的更正。🚉

- **删除卡片**

  升级将会使卡片重新出现。如果你完全不想学习某张卡片，或者想要推迟学习，可以考虑：

  - 暂停或淹污该卡片；
  - 创建一个不包含该卡片的[过滤卡组](#custom-study)；
  - 将卡片移入一个“冰箱”卡组，并在下次升级时勾选_不移动现有卡片_，如上一部分中_将卡片移入另一个卡组_所解释的。

- **添加或删除模板**

  如果你在_终极地理_笔记类型中添加了你自己的模板，在升级时你将失去它和所有从它创建的卡片。在升级过程中，你将看到一个对话框，要求你将当前模板与卡组的内置模板匹配。（在[将标准版卡组升级为扩展版](#levelling-up-from-standard-to-extended)时也会出现这个对话框。）不幸的是，你别无选择，只能将额外模板映射到“无”。升级后你可以重新添加它来重新创建卡片，但你在这些卡片上的学习进度将会丢失。

  如果你删除了模板，在升级时你将看到相同的对话框。然后该模板及其相关卡片将被重新创建。如果你愿意，可以在升级后再次轻松删除该模板。

### 会阻止升级的更改 ⛔

- **添加新字段（人口、货币等）**

  在_终极地理_笔记类型中添加新字段将完全阻止你升级卡组。当你尝试再次导入时，Anki很可能会出错，而你将面临失去所有学习进度的风险。希望Anki、CrowdAnki、Brain Brew和UG能够[有一天](https://github.com/ohare93/brain-brew/issues/4#issuecomment-644975261)找到一种方法来实现这一点。

  请注意，在_自定义模板和样式_中解释的克隆笔记类型的技术在这里不起作用。如果你添加了新字段并希望升级，你别无选择，只能先从笔记类型中**删除该字段**。

  > 如果你真的知道自己在做什么，你可以尝试使用CrowdAnki导出你的卡组，将卡组新版本的JSON文件小心地合并到你导出的卡组的JSON文件中，然后将你的卡组导回到Anki...但如果你有这样的能力，你的技能将在为[CrowdAnki](https://github.com/Stvad/CrowdAnki)和[Brain Brew](https://github.com/ohare93/brain-brew/)做贡献中得到更好的利用！😁

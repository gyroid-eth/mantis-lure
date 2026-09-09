# カマキリ画面刺激研究 — 文献調査

**結論（BLUF）**: 標的の視角は約10〜25°（種依存、20°付近がSphodromantis属で高反応）、角速度は約45〜120°/s（一部研究では上限180°/s超も報告）、コントラストは暗い標的×明るい背景が明るい標的×暗い背景より一貫して有利（Michelson contrast ±0.7〜1.0）、迫ってくる刺激（looming/段階的拡大）は最低0.8秒/段の持続で最大反応、を既定値の出発点とする。**最大の未解決点**: 色（波長）が輝度と独立に襲撃判断に効くかどうかを直接検証した「行動」研究が見つからず、既存研究は主にモノクロ刺激またはコントラストのみで実験している。もう一つの未解決点は、市販LCD/タブレットの60HzリフレッシュとsRGB色域がカマキリ視覚系（フリッカー感度・受容体分光）にどう見えるかを直接検証した研究が存在しないこと（研究は特殊な狭帯域LED/CRTベースの装置を使っている）。

---

## (1) 捕食反応を誘発する画面刺激の定量パラメータ

### 視角（標的サイズ）

| 指標 | 種 | 数値 | 出典 |
|---|---|---|---|
| 追跡閾値（erratic motion） | *Parasphendale affinis* | 8.6° | Prete, Theis, Dominguez & Bogue (2013) *J Exp Biol* 216(23):4443–4453. https://doi.org/10.1242/jeb.089474 |
| 襲撃閾値（erratic motion） | *P. affinis* | 6.9° | 同上 |
| 襲撃反応ピーク（円形刺激） | *P. affinis* | 9°の円盤 | 同上 |
| 高反応な矩形刺激 | *P. affinis* | 14×27–35° | 同上 |
| 追跡閾値（erratic motion） | *Popa spurca* | 7.4° | 同上 |
| 襲撃閾値（erratic motion） | *P. spurca* | 9.2°（漸増し44°まで反応率上昇） | 同上 |
| 平行矩形刺激ピーク | *P. spurca* | 35° | 同上 |
| 襲撃率が最大となる中間サイズ | *Sphodromantis lineola* | 10–20°（それより大小で反応低下、逆U字） | 同上 |
| 上昇順提示時の襲撃閾値 | *P. affinis* | <2° | 同上（提示順で閾値が大きく変動する点に注意） |
| 上昇順提示時の襲撃閾値 | *P. spurca* | 5.5–6.1° | 同上 |
| 上昇順提示時の襲撃閾値 | *S. lineola* | 3° | 同上 |
| 最大捕食反応を誘発した視角（水平×垂直） | *Sphodromantis viridis* | 約20–23°（水平）× 16–19°（垂直） | 出典URL不明のまま値のみ複数の二次資料に引用されているのを検出——**原典未確認。本文を読んでいないため数値の断定は避ける。** 一次資料の追跡調査を要する（Prete系の別論文の可能性）。 |
| 好適標的直径（ステレオ視モデル） | モデル計算（S. lineolaの生理データに基づく） | 10–25°（広い許容帯：半値幅7–25°程度） | O'Keeffe, Yap, Llamas-Cornejo, Nityananda & Read (2022) *PLOS Comput Biol* 18(5):e1009666. https://doi.org/10.1371/journal.pcbi.1009666 |

注記: 上表の「約20–23°×16–19°」の行は複数の検索結果に断片的に現れたが、一次論文のページ・DOIを本調査では確認できなかった。**この値は使わず、Prete et al. 2013の実測値（種ごとの閾値・ピーク値）を既定値の根拠にすべき。**

### 角速度（度/秒）

| 数値 | 文脈 | 出典 |
|---|---|---|
| 46–119°/s で最大捕食反応（*S. viridis*、二次資料経由） | 同上の未確認値と同系統。**原典未確認につき参考値扱い** | 同上注記 |
| Erratic path刺激: 143°/s | Prete et al. 2013 実験条件 | Prete et al. (2013), https://doi.org/10.1242/jeb.089474 |
| 直線矩形刺激: 180°/s | 同上 | 同上 |
| 直線刺激（stop-test）: 74°/s | 同上 | 同上 |
| モデルでの模擬刺激速度: 82°/s | O'Keeffe et al. 2022ステレオ視モデルの入力値 | https://doi.org/10.1371/journal.pcbi.1009666 |
| 標的速度: 43 cm/s（画面上、「昆虫の中程度の飛行速度」として設定） | Wang et al. (2025) — 画面サイズ・視距離が不明なため度/秒には変換不可。生値のみ記録 | Wang et al. (2025) *Behavioral Ecology* 36(5):araf107. https://doi.org/10.1093/beheco/araf107; データ: https://datadryad.org/dataset/doi:10.5061/dryad.nzs7h453b |

Prete et al. (2013) の速度条件はいずれも「実験条件として設定した値」であり、必ずしも「これが最適速度」という意味ではない点に注意（本文で反応率と速度の相関を分けて確認する必要があるが、本調査では相関の数値までは抽出できていない＝**要追加読解**）。

### コントラスト・明暗の向き

- Prete et al. (2013): 白背景×黒円盤 vs 黒背景×白円盤で比較し、**3種すべてで「黒い標的が白背景を動く」条件のほうが「逆」より高い襲撃率**。使用したMichelson contrastは黒背景/白背景で±0.97、グレー刺激では−0.7〜+0.8の範囲。 https://doi.org/10.1242/jeb.089474
- Nityananda et al. (2015) *J Comp Physiol A* 201(8):741–750 https://doi.org/10.1007/s00359-015-1008-5（*S. lineola*のコントラスト感度関数）:
  - 最低検出可能コントラスト: 約0.015625（Michelson比 約1.6%）
  - 最適空間周波数（0.03 cycles/deg）・最適時間周波数（3Hz）付近での閾値: 約0.038
  - 有効な空間周波数レンジ: 0.0071–0.4073 cycles/deg、感度ピークは約0.05 cycles/deg付近
  - 時間周波数は0.25/8/30Hzで比較、8Hzで最良の応答
  - 実験時の平均輝度: 13.18 cd/m²（画面最大輝度の50%）

### 色・波長感度

- Nityananda et al. (2016) *Sci Rep* 6:18718（"Insect stereopsis demonstrated using a 3D insect cinema"）https://doi.org/10.1038/srep18718: 3Dメガネ実験では**赤色光がカマキリにほとんど見えないため、緑と青のフィルタ**でアナグリフを構成し、緑・青の出力が狭帯域なLEDモニタを使用した。**円偏光フィルタはクロストークが大きく失敗し、分光（色）フィルタ方式のアナグリフで3D錯視に成功**——これは「色そのものの弁別」の証拠ではなく、単に左右眼分離の手段として波長を使った点に注意。
- Zhu et al. (2025) "Praying mantises possess multiple spectral photoreceptor classes" *J Comp Physiol A* https://doi.org/10.1007/s00359-025-01776-z（**アブストラクトのみ・本文未読**）: *Theopropus elegans* と *Popa spurca* はERGで緑（515–525 nm）に主感度ピーク、紫外（350–360 nm）と青（441 nm・416 nmの2群）に副次ピークを持ち、三色型の可能性。*Hymenopus coronatus* はより単純な二色型パターン。**測定波長域は350–650 nm**。
- 上記は**受容体レベルの分光感度**であり、「色が行動（捕食判断）に効くか、輝度だけで説明できるか」を直接検証した行動実験は本調査で発見できなかった。Second-order motion（輝度非依存の二次運動）に関する行動研究（下記）はあるが、これは色ではなくパターン/コントラストの二次統計量の話であり、色覚そのものの話ではない。
- 結論: **色（波長）が捕食判断に独立して効くという直接的な行動データは未確認。既知なのは受容体の分光感度のみ**。既定値は輝度コントラストを主軸に置き、色は演出上の付加要素とすべき。

### Looming / 段階的サイズ変化

- Nityananda, Tan, Boonyarittiwong, Collett, Sridharan & Read (2019) *J Exp Biol* 222(11):jeb198614 https://doi.org/10.1242/jeb.198614:
  - 疑似接近: 画面上の視距離換算で**20cm→2.5cm**まで接近をシミュレート。最終視角: 近距離で22.62°、遠距離で5.72°。
  - 純粋なlooming（輝度エッジが拡大する古典的刺激）: 襲撃率 約60%（サイズ変化あり・視差変化あり = veridical looming条件）
  - サイズ一定・大＋視差変化のみ: 約35%
  - サイズ一定・小＋視差変化のみ: 約15%
  - 視差（両眼視差）変化だけで奥行き運動を装った条件では、交差視差ありで襲撃率58.33% vs 非交差視差で6.3%（実験1、定常奥行き条件）
  - 運動中奥行き（motion-in-depth, IOVD型）条件では交差/非交差で有意差なし（31.25% vs 32.3%、定常条件との比較）
  - 結論: **カマキリは奥行き運動の検出に、両眼視差の時間変化（IOVD的なステレオ手がかり）よりも、輝度エッジの拡大（古典的looming）を主に使う**。
- Journal of Insect Behavior（*S. viridis* target size change論文, 2013）: **段階的にサイズが増大する刺激は、各段階の持続時間が少なくとも0.8秒のとき最大の捕食反応を誘発**。サイズが減少する刺激は「peering（頭部の左右振り）」のみを誘発し襲撃を誘発しない。**注記: 本論文（Springer, DOI 10.1007/s10905-013-9422-4）は認証ページにリダイレクトされ本文を直接取得できず、この数値は事前の二次検索結果からの引用。原典PDFでの再確認が望ましい。**
- Yamawaki他 (2011) *J Insect Physiol* (*Tenodera aridifolia*の防御行動、捕食ではなく被食側の反応だが、視覚パラメータの参考になる) https://www.sciencedirect.com/science/article/abs/pii/S0022191011002253 / PubMed: https://pubmed.ncbi.nlm.nih.gov/21851823:
  - 正面から衝突コースで接近する物体で防御反応（cryptic reaction: 前脚を素早く引くまたは伸ばす）の発生率が最大。水平方向へのズレがあると発生率低下。
  - 接近速度が速いほど防御反応率が上昇。接近が途中で停止する距離が遠いほど反応率は低下。
  - 防御開始のタイミングは「物体半径サイズ／接近速度」の比と線形関係——大きく・遅く迫る物体には早期に反応。
  - 視覚を遮ると反応率が低下＝視覚由来の反応であることを確認。

### 運動パターン（らせん・直線・断続・ジグザグ）

- Wang, Chai他 (2025) *Behavioral Ecology* 36(5):araf107 https://doi.org/10.1093/beheco/araf107（*Hierodula majuscula*, n=17雌）:
  - 画面: Samsung 27" S6U QHD (2560×1440px, 596.736×335.664mm), **75Hz**リフレッシュ。アニメーションはMaya 2023 + Arnoldでレンダリング、1080p/75fps。
  - 標的サイズ: 大2.4×1.44cm（面積2.71cm²）、小1.68×1.03cm（面積1.36cm²）
  - 速度: 43cm/s（一定）
  - 直線軌道: 1パス2.00秒。Erratic軌道: ハエの飛行データから生成（300ステップ、ステップ長は正規分布 平均1・SD1、旋回角SDはπ/2ラジアン）、1パス2.24–2.68秒。
  - **追跡率**: 大標的79–85% vs 小標的10–47%（χ²=14.92, P<0.001）。**直線軌道のほうが追跡率が高い**: 直線59–85% vs erratic 14–57%（χ²=7.63, P=0.006）。
  - **襲撃までの潜時**: erraticのほうが速い（5.60–7.22秒 vs 直線8.18–10.55秒、χ²=5.11, P=0.024）——「追跡はされにくいが、追跡された場合の襲撃は速い」というトレードオフ。
  - **攻撃精度**: 光沢(glossy)×erratic の組み合わせで誤差最大（27.39mm、他条件は14.85–19.45mm、χ²=5.13, P=0.024）——単純に「直線か曲線か」ではなく、光沢（質感）との交互作用で精度が変わる。
- Apparent Motion Perception in the Praying Mantis: Psychophysics and Modelling（bioRxiv, 未刊行誌不明、10.1101/320606）https://www.biorxiv.org/content/10.1101/320606: 直線・erratic・spiral・zigzagを含む複数の運動軌道と速度閾値を検証しているが、**本調査ではPDF本文の数値を十分に抽出できず（メタデータ層の制約）。著者名・DOI・具体数値は要再取得**。

### 視距離・捕獲圏（strike range）・両眼視差

- O'Keeffe et al. (2022) *PLOS Comput Biol* 18(5):e1009666 https://doi.org/10.1371/journal.pcbi.1009666（*S. lineola*生理データに基づくモデル）:
  - 好適襲撃距離（モデル最適）: 2.1cm
  - 実効捕獲圏: 1.5–5.63cm、約3.8cm超で襲撃率が大きく低下
  - 両眼視差35mm相当→55mm相当のスクリーン視差変化（5°相当）で襲撃率が1.0→0.6に低下
  - 眼間距離（モデル入力）: 7mm
- Nityananda et al. (2019) https://doi.org/10.1242/jeb.198614: 疑似接近20cm→2.5cmのcatch range閾値を使用（上記looming節と同じ実験）。
- 結論: **視差だけで距離判断が完結するわけではなく、looming（輝度エッジの拡大）が主要な奥行き手がかり**。ステレオ視差はcatch range内かどうかの判断を補助する形で働く（"is there prey at the right distance to catch"）— Nityananda, EurekAlert二次資料 https://www.eurekalert.org/news-releases/593691 での発言。

### 標的の形状・アスペクト比・進行方向に対する長軸の向き

- Prete et al. (2013) https://doi.org/10.1242/jeb.089474:
  - *Popa spurca* は長軸が進行方向と**平行**（parallel）な細長い刺激（≥35°）で追跡・襲撃率が有意に高い（"robust parallel preference"）。
  - *P. affinis* と *S. lineola* は向き（parallel/perpendicular）による有意差なし。
- Kral, Prete (2004ごろ) および Prete et al. (2011) *J Comp Physiol A* 197(9) https://link.springer.com/article/10.1007/s00359-011-0649-2（**認証ページにリダイレクトされ本文未取得。二次資料からの引用に留まる**）: 3種の形態的に異なるカマキリでの appetitive behavior比較。本調査では数値抽出に至らず、追加読解が必要。

### Prete の "10 properties"（獲物と判定する刺激特性）

原典: Prete, F.R. (1999) "Prey recognition." In *The Praying Mantids* (Prete, Wells, Wells & Hurd eds.), Johns Hopkins University Press. および Kral & Prete (2004ほか) の一連の論文。本調査ではJohns Hopkins University Press版の書籍本文には到達できず（書籍PDFへのアクセス不可）、**複数の後続論文（Prete et al. 2011, 2013; Kral & Prete）が要約として引用する形**で10特性のリストを検索により再構成した。挙げられている特性は次の通り（数と表現は論文間で若干揺れがあるため、複数出典を統合）:

1. 標的の全体サイズ（overall size / visual angle）
2. 前縁（leading edge）の長さ
3. 背景に対するコントラスト
4. 視野内の位置（location in the visual field / retinal eccentricity）
5. 見かけの速度（apparent speed）
6. 運動方向（direction of movement）
7. 進行方向に対する形状の向き（geometry relative to direction of movement）
8. 網膜上を移動した距離（retinal distance traversed）
9. 閾下刺激要素の時間的加重（temporal summation of sub-threshold elements）
10. 閾下刺激要素の空間的加重（spatial summation of sub-threshold elements）

出典（統合元）:
- Prete, Theis, Dominguez, Bogue (2013) *J Exp Biol* 216:4443–4453. https://doi.org/10.1242/jeb.089474
- Prete et al. (2011) *J Comp Physiol A* 197:877–890. https://link.springer.com/article/10.1007/s00359-011-0649-2 （**本文未読、章立ての要約のみ**）
- 二次検索結果内の直接引用文（"For mantises, known visual stimulus parameters that fall within this schema... (1) size, (2) contrast..., (9)...summed over time and (10) space"）

**注記: これは原典（1999年の書籍章）そのものを読んで確認したリストではない。後続論文の要約の再構成である。原典入手ができれば再検証すべき。**

---

## (2) LCD/タブレットで昆虫に刺激を見せるときの既知の落とし穴

### フリッカー・リフレッシュレート

- カマキリ自身の臨界融合周波数（CFF）の直接測定値は、本調査では**発見できなかった**（検索語「mantis critical flicker fusion frequency」で複数回試したが、他の昆虫種のデータしか出てこない）。
- 近縁または比較対象となる昆虫のCFF実測値（Miall, R.C. (1978) "The flicker fusion frequencies of six laboratory insects, and the response of the compound eye to mains fluorescent 'ripple'." *Physiological Entomology* 3(2). https://doi.org/10.1111/j.1365-3032.1978.tb00139.x）:
  - イエバエ（housefly）受容体: 約200Hz
  - ツェツェバエ (*Glossina morsitans*): 85–205Hz
  - ミバエ属 (*Drosophila hydei*): 60–100Hz
  - トノサマバッタ (*Locusta migratoria*): 40–90Hz
  - ワモンゴキブリ (*Periplaneta americana*): 25–60Hz（**Dictyoptera上目でカマキリに系統的に近い**が、カマキリそのものではない点に注意）
  - オオミズアオ系のガ (*Saturnia pavonia*): 65–85Hz、(*Antheraea pernyi*): 25–70Hz
  - ミツバチ: 二次資料で約300Hzという言及もあるが、原典未確認
- **含意**: ゴキブリで25–60Hzという実測があることから、**60Hzの一般的LCD/タブレットはカマキリにとってフリッカーが見える可能性がある**（人間の閾値50–90Hzより低いカマキリ視覚系がもしゴキブリに近いなら60Hzはギリギリか不足）。ただし種特異的な実測がないため断定はできない。Nityananda関連研究（Sci Rep 2016等）が意図的に高フレームレート/特殊モニタを使う背景には、この不確実性への配慮があると考えられる（ただし論文中で「フリッカー対策」と明示した記述は本調査では未確認——リフレッシュレート言及は主に色分離・輝度制御の目的として言及されている）。

### 偏光・UV欠落・色域のズレ

- Nityananda et al. (2016) *Sci Rep* https://doi.org/10.1038/srep18718: 実験では**円偏光フィルタ方式のアナグリフはクロストークが大きく失敗**、分光（色）フィルタ方式に切り替えた。液晶ディスプレイは偏光を利用する表示方式であるため、偏光を利用する実験系との相性に注意が必要。
- 一般的なLCDパネルはUV光をほぼ通さない／発しない（パネル素材依存でUV透過率が変動）ことが、Didion, Smith & Layne (2020) *Methods Ecol Evol* 11(5):690–696. https://doi.org/10.1111/2041-210X.13375 で指摘されている。この論文は動物の色覚実験のためにLCD（ツイステッドネマティック型）の背面偏光板を外し、2色のLEDでバックライトを構成する改造法を提案——**標準的なRGB LCD/タブレットは、ヒトの三色覚に最適化されたsRGB原色を使うため、カマキリのような別の受容体構成を持つ動物にとっては「意図した色」を提示できているとは限らない**、という含意。
- カマキリの受容体分光感度（Zhu et al. 2025、上記(1)節、**アブストラクトのみ**）は緑・青・UV帯にピークがあり、標準LCDのRGB原色（特に赤主体のR）とは対応が悪い可能性がある。

### 実験でどう回避されているか

- 高フレームレート・特殊モニタの使用: Wang et al. (2025) は75Hzモニタを使用（一般的な60Hzより高い）。
- 狭帯域LEDバックライト・アナグリフ分光フィルタ: Nityananda et al. (2016)。
- LCD改造（背面偏光板除去＋LED化）による色制御: Didion et al. (2020)（カマキリ対象ではないが同様の問題設定）。
- 輝度校正: Nityananda et al. (2015) は実験輝度を「画面最大輝度の50%＝13.18 cd/m²」と明示的に校正・記録している。
- CRTの使用に関する明示的な記述（「なぜCRTを使うか」を述べた一次資料）は、本調査では**発見できなかった**。一般的な視覚実験の文脈（CRT vs LCDでの提示タイミング精度）に関する資料はあるが（PMC7181856）、カマキリ研究に特化した言及ではない。

---

## (3) 先行実装・製品・OSS

### カマキリ向けの同種アプリ

- 一般消費者向けの「カマキリ用画面おもちゃアプリ」は、本調査では**発見できなかった**。見つかったのはSNS上の逸話（iPhoneのゲームに反応するカマキリの動画・記事: PetHelpful https://pethelpful.com/pet-news/praying-mantis-playing-game-on-iphone 、AOL記事 https://www.aol.com/praying-mantis-tries-attack-spider-133200053.html ）で、いずれも研究目的ではなく個人の飼育者による非公式な観察。ライセンス・公開コードなし。
- GitHub上でヒットした唯一の関連プロジェクトは "Snake-game-kill-the-praying-mantis"（Owl67h2） https://github.com/Owl67h2/Snake-game-kill-the-praying-mantis で、これはPythonのturtle graphicsで作られた人間向けゲームであり、**カマキリに見せるための刺激提示ツールではない**（無関係）。

### 猫用アプリの類例

- "Games for Cats!" (App Store) https://apps.apple.com/us/app/games-for-cats/id1394742877 、"Mouse for Cats" https://www.mouseforcats.com/mouse-for-cats/ 、Tembrica "Games for Cats" https://tembrica.com/en/cat-games など複数の商用アプリが存在。
- 設計上の語られている知見（二次資料経由、原典的な行動学論文ではない）:
  - 魚やマウス型の標的は「不規則な動き・速度変化」が「怪我をした/怯えた動物」を模し捕食トリガーになりやすいとされる（二次資料の記述であり、対照実験による検証は確認できていない）。
  - 猫は二色型（青・黄に強く、赤・緑の弁別が弱い）視覚を持つとされ、それに合わせた青黄パレットを採用するアプリがある。
  - 短時間・頻回のセッションが推奨され、連続使用による慣化（habituation）への言及がある。
  - **これらは業界の経験則であり、査読された行動学研究による定量的な裏付けは本調査では確認できていない**。カマキリの企画に猫アプリの知見を転用する際は「効くはずのアナロジー」程度の重みで扱うべき。

### 研究用刺激提示ソフトでのカマキリ利用例

- MATLAB Psychtoolbox: カマキリの視覚研究（アピアレントモーション論文 bioRxiv 10.1101/320606、ステレオ視神経相関論文 *Nat Commun* https://www.nature.com/articles/s41467-019-10721-z 等）でMatlab+Psychtoolboxベースの刺激提示が使われていると複数の二次資料が言及。
- **m3toolbox**（"Man, Mantis and Machine" Project） https://github.com/m3project/m3toolbox — Newcastle大学Institute of Neuroscience（Nityananda / Readグループ系列と推定される）が公開しているMatlabツールボックス。カマキリ視覚系の刺激生成・心理物理実験の実行・データ収集・計算モデル構築に使われると説明されている。**これは実際に公開されているカマキリ向け刺激提示コードであり、本企画にとって最も直接参照すべき先行実装**。ライセンス・詳細は本調査ではリポジトリの中身まで読み込んでいない（要フォローアップ: ライセンス種別、対応言語、刺激生成APIの確認）。
- PsychoPy（Python）でのカマキリ直接利用例は本調査では発見できなかった。

### Newcastle 3Dメガネ研究の刺激提示コード

- 3Dメガネ実験そのもののコード（アナグリフ生成・モニタ制御スクリプト）が単独のGitHubリポジトリとして公開されているという直接証拠は、本調査では**発見できなかった**。上記m3toolboxが同グループの汎用ツールボックスであり、関連コードが含まれている可能性が高いが、本調査ではリポジトリ内部を確認していない。

---

## (4) この企画への含意

1. 既定の視角は**12〜20°（対角）を中心域**とし、6〜9°を下限（追跡開始閾値相当）、35°前後を上限（サイズ提示順で反応が変わるため固定閾値と考えない）とする段階的スケールを用いるべき——Prete et al. (2013) の種間差が大きいため、単一の「正解サイズ」は存在しないことを前提にUIで調整可能にする。
2. 既定の角速度は**45〜90°/s**を穏当な中心とし、120°/s程度までを上限レンジとして許容する——ただし度/秒は視距離（iPadから被写体までの距離）に依存するため、cm/s換算だけでなく実際の視距離を入力させて度/秒を計算する設計が必須。
3. コントラストは**暗い標的×明るい背景を既定（デフォルト）**とし、明暗反転はオプション扱いにする——Prete et al. (2013) で3種一致した唯一の明確な結果。
4. 色は演出用のオプションに留め、**輝度コントラストを主変数として設計**する——色が独立に効くという行動学的証拠がないため、色を主要パラメータとして最適化する根拠が現時点でない。
5. 60Hzタブレットのフリッカーがカマキリにどう見えるかは未解決（近縁種でも25–90Hz帯に閾値がある例があり60Hzは境界的）——可能なら90Hz以上のリフレッシュに対応させ、フリッカー起因の誤差を減らす方向で設計すべき。

---

**検索器の健全性確認**: 調査開始時に "praying mantis prey capture" で検索し、複数の関連論文（PNAS, J Exp Biol, Frontiers等）が返ることを確認した上で、以降の「0件＝存在しない」という判断を行った（例: カマキリ向け同種アプリ、カマキリ特異的CFF実測値、3Dメガネ実験の単独公開リポジトリなど）。

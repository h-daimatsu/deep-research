# 2024年以降のグローバル半導体サプライチェーン再編: 要因と波及効果

**作成日**: 2026-07-03 JST

## エグゼクティブサマリー

2024年以降、グローバル半導体サプライチェーンは効率性優先の水平分業から、地政学的耐性・産業政策・AI需要を軸にした多極化・重複投資型の構造へ再編されている。この再編は単一の原因ではなく、地政学的要因（台湾一極集中と輸出規制）、産業政策要因（各国の補助金競争とその実効性の分岐）、技術・需要要因（AI/HBM需要による先端逼迫と成熟ノードの過剰供給）という3つの力が同時に作用した結果である。

調査で得られた最も重要な発見は3点ある。第一に、SEMIの予測では中国のみがファブ投資額を縮小させる（2024年の630億ドルから2028年に280億ドルへ）一方、米国・日本・欧州・韓国・東南アジアは軒並み増加しており、地政学的分断が投資地図に非対称な形で現れている[^1]。第二に、サプライチェーンの再編は前工程（ファブ）と後工程（パッケージング・テスト）で異なる速度と論理で進行しており、前工程は地政学的動機で米・日・欧・韓・台に分散する一方、後工程は機能的な効率性の論理で東南アジア・インドに再配置されている。第三に、この再編は地政学的耐性を高める一方でコストと重複投資という代償を伴い、AI投資の過熱、人材不足の恒常化、成熟ノードでの供給過剰といった新たな脆弱性を生んでいる。

再編の持続可能性は、AI需要の実需とハイパースケーラーの投資意欲が金融市場の期待とどこまで整合するか、および各国が数千億ドル規模で投じた補助金が人材不足という構造的制約を乗り越えられるかに左右される。台湾海峡での軍事衝突という低頻度・高損失シナリオは、依然として多極化投資の経済的合理性を支える最大の論拠として機能している。

## サプライチェーン再編の全体像

### 地域別投資の非対称な変化

SEMIの World Fab Forecast（2025年第1四半期版）によれば、世界のファブ設備投資は2019年の560億ドルから2025年推計1,430億ドルへと拡大した[^1]。2025年から2027年の3年間で300mm設備投資は累計3,740億ドルに達する見通しであり、2026年と2027年は2桁成長が続くとSEMIは予測している[^2]。

この拡大の内実は地域によって著しく異なる。SEMIが示す2024年から2028年の地域別ファブ投資額（設備投資と建設投資の合計）を見ると、米国は50億ドルから70億ドルへ、欧州・中東は70億ドルから150億ドルへ、日本は240億ドルから330億ドルへ、韓国は190億ドルから300億ドルへ、東南アジアは220億ドルから320億ドルへと、いずれも増加が見込まれている[^1]。対照的に中国だけは630億ドルから280億ドルへと縮小する予測になっている。2020年から2028年までの年平均成長率も、欧州・中東が21%、米国が19%、東南アジアが20%と高い一方、中国は5%と最も低い[^1]。SEMIはこの投資シフトの背景として、地政学的要因、各国のChip Act、サプライチェーン強靭化イニシアチブのいずれもが寄与していると分析している[^1]。

中国のみが投資額を縮小させるという事実は、単純な需要低迷では説明できない。中国は同時期に世界最大級の半導体関連補助金を投じており（後述）、投資額の縮小は輸出規制によって先端装置の調達が制約された結果、投資の質が先端ロジックから成熟ノード・国産装置開発へ再配分されていることを示唆する。

### 中国の生産能力シェアに見る不均等発展

SEMIのデータは、中国の半導体生産能力（200mm相当ウェーハ換算の月産能力）の世界シェアが、半導体の種類によって大きく異なることも示している。ディスクリート半導体では2024年の47%から2028年に49%へ、アナログ半導体では30%から36%へと拡大する見通しである一方、メモリは25%前後で横ばい、ロジック・マイクロは18%から24%への拡大が見込まれる[^1]。中国は輸出規制の対象になりにくい成熟ノード（ディスクリート・アナログ）に生産資源を集中させ、規制の直接的な対象となる先端ロジックでは相対的に緩やかな拡大に留まっている。この不均等な発展パターンは、後述する技術・需要要因の章で扱う「先端の逼迫と成熟の過剰供給」という対比構造の起点となる。

### 米国の生産能力反転という歴史的転換

半導体産業協会（SIA）とボストン・コンサルティング・グループ（BCG）が2024年5月に公表した報告書は、米国がCHIPS法制定時の2022年から2032年までに国内半導体生産能力を3倍（203%増）に拡大すると予測している[^3]。これにより米国の世界シェアは10%から14%へ上昇し、数十年ぶりに反転する見通しである。先端ロジック（10ナノメートル未満）に限れば、米国は2032年までに世界の28%を担うと予測されている[^3]。SIA会長のジョン・ヌーファー氏は、この反転について「回復には何年もかかる」と述べており、政策効果の即効性には限界があることを当事者自身が認めている[^3]。

2024年の世界半導体売上は地域別の伸びが大きく分岐した。米州が45.2%増、中国が20.0%増、アジア太平洋その他が12.2%増となった一方、日本は0.3%減、欧州は8.1%減となっている[^4]。AI関連需要が集中する米州の突出した成長と、成熟ノード中心の欧州・日本の停滞という対照が、2024年時点で既に明確に現れていた。

## 再編を駆動する3つの力

### 地政学的要因: 台湾一極集中と輸出規制の実効性論争

台湾は2024年時点で世界の半導体の60%、最先端半導体（3ナノメートル・5ナノメートル等）の90%から95%を生産している[^5]。台湾積体電路製造（TSMC）単独で世界のファウンドリ売上の約70%、最先端ノードの90%超を占める[^6]。トランプ政権の商務長官ハワード・ラトニック氏も2025年9月の会見で台湾が先端半導体の世界供給の95%を生産していると明言しており、政策当局者自身がこの集中度を集中リスクとして認識している[^7]。

この集中度は「シリコンシールド」と呼ばれる抑止理論の根拠になってきた。台湾の半導体産業が持つ抑止効果は二重の構造を持つ。中国が台湾に侵攻すれば自国が依存する半導体供給が途絶するため中国の侵攻インセンティブが下がるという経路と、米国も台湾製チップに依存するため軍事介入の可能性が高まるという経路である[^7]。しかし2024年以降、TSMCのアリゾナへの1650億ドル投資に代表される米国オンショアリングの進展により、シールドが希薄化するとの懸念が台湾国内で高まっている[^7]。台湾にとって、米国への技術移転を進めるほど自国の地政学的レバレッジが弱まるというジレンマが生じている。

米国の対中輸出規制は2022年10月の開始以降、段階的に範囲を拡大してきた。当初はAI訓練用の先端半導体を標的としていたが、2023年10月、2024年4月、2024年12月と相次いで規制を強化し、半導体製造装置の国別包括規制やEUVに加えたDUVの一部規制まで対象を広げた[^8]。2025年には「AI Diffusion Rule」によってAIモデルの重みや米国設計チップの輸出にライセンス制度を導入し、国別に許可レベルを階層化する仕組みへ移行している[^9]。

輸出規制の実効性については評価が対立している。米戦略国際問題研究所（CSIS）の分析は、オランダによるASMLの最先端EUV露光装置の輸出禁止が中国の2ナノメートル・3ナノメートル級製造を原理的に封じると評価する[^10]。一方で、中国のSMICが規制対象の欧米製装置を確保してHuawei向けチップの生産に成功した実例が報告されており、元TSMC副社長のバーン・リン氏は同じ装置を用いてSMICが5ナノメートルまで到達可能と証言している[^11]。学術分析はこうした事例を踏まえ、規制がむしろ中国の自前技術開発を加速させたと指摘する[^12]。SMICの2023年売上は輸出規制の影響で前年の72.7億ドルから63.2億ドルへ13.1%減少したが、これが国内市場での需要創出につながり、中国国内サプライヤーへの代替が進行した[^13]。中国はDUVリソグラフィ装置を大量に確保・在庫化し、Huawei Ascend 910C等の7ナノメートル級チップの生産を継続している[^14]。

トランプ政権の関税政策は不確実性を伴いながら展開した。2025年夏には半導体への最大100%の関税が表明されたが、米国内で製造する（またはその意思を示した）企業を免除するという条件付きだった。2025年11月には対中貿易摩擦の回避を理由に実施が延期される観測が報じられたが、最終的に2026年1月14日、大統領令（Proclamation 11002）によりAI関連の狭いカテゴリーの半導体に25%のSection 232関税が発効した[^15]。より広範な関税は今後の交渉次第で検討するとしつつ、米国内投資企業には関税相殺プログラムが用意されている[^15]。

台湾有事という低頻度・高損失シナリオの経済的影響は看過できない規模である。ブルームバーグ・エコノミクスが2026年2月に公表した分析によれば、台湾海峡での軍事衝突が米中対立に発展した場合、世界経済への損失は1年間で約1600兆円に達し、GDP減少率は日本が14.7%、中国が11%、米国が6.6%という試算が示されている[^16]。この規模の損失リスクは、多極化投資という非効率な戦略の経済的合理性を正当化する最大の論拠として機能している。

### 産業政策要因: 補助金競争と実効性の分岐

主要国・地域は2022年以降、同時多発的に巨額の産業政策を投入した。米国のCHIPS and Science Actは390億ドルの製造補助金、130億ドルの研究開発資金、35%の投資税額控除で構成される[^17]。中国は国家集積回路産業投資基金（大基金）等を通じて2000億ドル超規模の支援を行っているとされる[^17]。EUのEuropean Chips Actは430億ユーロ規模、韓国のK-Chips Actは160億ドルの税優遇を提供する[^17]。

これらの政策の実効性は国・地域によって明確に分岐した。米国では、CHIPS法の補助金の大半がIntel、TSMC、Samsung、Micronの4社に配分され、3万人以上の高賃金雇用創出が計画されたが[^18]、Intelのオハイオ工場は稼働開始予定が2025年から2027年から2028年へ延期され、Samsungのテキサス工場も延期された[^19]。2025年8月、トランプ政権はIntelへの未払いCHIPS法補助金56.7億ドルと国防省「Secure Enclave」計画の32億ドルを合算し、合計89億ドルをIntel株式（4億3330万株、1株20.47ドル）に転換し、米政府がIntelの9.9%を保有する事態となった[^20]。この措置は補助金政策の性質を「産業育成のための資金供与」から「政府による産業出資」へ転換するものであり、情報技術イノベーション財団（ITIF）はこれをCHIPS法が本来目指した製造コスト差の縮小という目的に反し、株式希薄化により将来の資金調達をむしろ困難にすると批判している[^21]。

EUの産業政策はより明確な停滞に陥った。European Chips Actは2030年までに世界シェアを10%から20%へ倍増させる目標を掲げたが、2025年8月にIntelが独マグデブルクの300億ユーロ規模のファブ計画を正式に撤回した[^22]。ドイツ政府はこの計画に99億ユーロの補助金を用意していたが、投資自体が実現しなかった。欧州会計監査院は2025年の報告書で20%目標の達成は極めて困難と断定しており、2024年時点のEUの世界価値鎖シェアは10.5%とChips Act制定前とほぼ同水準に留まっている[^23]。欧州のテック系メディアの記者は、Intel撤退後の欧州について「近い将来、少なくとも欧州大陸には先端ロジックの製造経路が存在しなくなる」と評し、欧州がAI用のNvidiaチップは購入するが、それを製造するファブを持たないという構造的な矛盾を指摘している[^24]。欧州の政策シンクタンクBruegelは、自給自足ではなく不可欠なパートナーとしての地位を目指す「Chips Act 2.0」への転換を提言している[^25]。

対照的に、日本とインドの産業政策は具体的な進展を見せた。日本ではTSMC熊本第1・第2工場に合計で最大約1兆2080億円が補助されている[^26]。国産先端半導体を目指すラピダスへの支援は段階的に拡大し、2024年10月時点で追加5900億円が決定され、累計の支援額は2.9兆円に達する方針が報じられている[^27]。日本政府はこれとは別枠で10兆円超規模の半導体・AI関連の公的支援枠組みを検討している[^28]。野村総合研究所の論説は、安易な支援が事業失敗リスクを高め国民負担増につながりうると慎重な対応を求めているが、TSMC熊本の実際の稼働という実績は他の主要国・地域の産業政策と比べて際立っている[^28]。インドでは2026年5月、Tata ElectronicsがASMLと提携協定を締結し、グジャラート州でのインド初の前工程ファブ建設に向けて前進した[^29]。同月にはMicronのアッセンブリ・テスト・パッケージング施設が同州サナンドで稼働を開始している[^29]。

日本とインドの前進とEUの停滞という分岐は、既存の需要企業との連携の有無、補助金の実行スピードと確実性、投資判断における政治的安定性の評価という複数の要因が組み合わさった結果と考えられる。米国のCHIPS法の株式化という政策の性質転換は、産業政策が政権交代によって前提から変わりうるという不確実性を象徴し、これが企業の投資判断における重要なリスク要因になっている。

### 技術・需要要因: 先端の逼迫と成熟の過剰供給

AI需要は先端ロジックとメモリの両方で資本支出の記録的拡大を引き起こしている。TSMCの資本支出は2024年の289億ドルから2025年の409億ドル、2026年計画では520億ドルから560億ドルへと拡大しており、ハイパフォーマンスコンピューティング分野が同社売上の58%を占めるに至った[^30]。同社は2026年後半に2ナノメートルプロセスの量産ランプアップを予定し、2ナノメートル市場の機会を2兆ドル規模と見積もっている[^30]。

メモリ市場ではAI向け高帯域幅メモリ（HBM）需要が従来型メモリの供給構造を侵食している。2025年第3四半期時点でDRAM価格は前年比172%上昇した[^31]。Micron、Samsung、SK Hynixの3社はDRAM・NAND等の生産能力をHBMへ転用しており、Micronは主力製品ラインの生産中止を決定してHBM・AI顧客を優先する方針を明示した[^31]。SK HynixとMicronは2026年のHBM生産分を完売したと報告されている[^32]。HBM市場シェアはSK Hynixが2024年第4四半期の51%から2025年第4四半期の57%へ拡大したのに対し、Samsungは40%から22%へ急落した。これはSamsung製HBM3EがNVIDIAの品質認証に不合格を繰り返したことが要因とされ、過熱と電力消費に関する技術的課題が背景にある[^33]。メモリ産業全体の売上は2023年の谷（850億から900億ドル）から2027年予測の8000億から8500億ドル規模へ急拡大する見通しであり、AIサーバー向けメモリ支出は2025年の350億から400億ドルから2027年の1750億から1900億ドルへ、2年で5倍に拡大すると予測されている[^34]。

この先端の逼迫と対照的な現象が成熟ノードで進行している。中国は輸出規制により先端ノードへのアクセスを制約された結果、28ナノメートル以上のレガシーチップに生産資源を集中的に再配分し、2025年末までに世界の成熟ノード生産能力の28%を占める見通しである[^35]。米商務省産業安全保障局(BIS)の調査によれば、中国系ファウンドリの価格は非中国系より平均10%安く、調査対象の72%のケースで中国系ファウンドリが最も安価だった[^36]。この価格競争力の高さは西側の既存レガシー半導体メーカーの事業存続に対する懸念を招いている。

中国の成熟ノード拡大が実際に「過剰供給」に至るかどうかについては評価が対立している。CSISとフランス国際関係研究所(Ifri)は、太陽光パネルや電気自動車で見られた過剰生産構造とは性質が異なり、過剰供給への懸念は誇張されていると反論する[^37]。一方でロディウム・グループ、欧州政策分析センター(CEPA)、ワイヤーチャイナは、中国の成熟ノード拡大を持続的な問題と評価している[^38]。同じデータに対する評価の対立は、太陽光パネル・電気自動車との類推の妥当性、及び分析対象期間の取り方の違いに起因すると考えられる。

先端ロジックとメモリでは西側・台湾・韓国が投資を集中させ、成熟ノードでは中国が世界的な影響力を拡大するという二極化した専門化構造が生まれている。この分業は効率性の観点では機能的だが、地政学的な緊張が高まった場合には両陣営とも相手方の工程に依存し続けるという脆弱性を伴う。

## 企業の戦略的分岐

### TSMC: アリゾナ集中投資とその代償

TSMCは総額1650億ドルという史上最大の対米直接投資をアリゾナに投じ、最大12棟のファブと3から4棟の先端パッケージング施設からなる「ギガファブ・クラスター」を計画している[^39]。第1ファブは既にApple・NVIDIA向けの先端チップを量産中であり、2026年第3四半期には第2ファブの設備導入が始まる予定である[^39]。この資源集中には代償が伴う。2025年7月の報道によれば、TSMCはアリゾナへの投資加速の一方で、日本とドイツでの拡張計画を停滞させている[^40]。アリゾナ工場は台湾に比べ最大30%のコスト高であり、人材不足、サプライチェーンの不備、労務慣行の違いから2025年第3四半期には利益率が急落する見通しも指摘されている[^41]。

2025年8月、トランプ政権によるTSMCへの株式取得の可能性が報じられたが、TSMC会長のC.C.ウェイ氏は米政権がTSMCの株式を取得しないと明言し、Intelとの取り扱いの違いを強調した[^42]。ウェイ氏はAIが日常生活を再構築しており、半導体技術が新たな能力とアプリケーションの基盤になっているとして、米国投資拡大の合理性を説明している[^42]。

### Samsung: 慎重化する海外展開

SamsungのテキサスTaylor工場（当初計画170億ドル）は完成が遅延していると2025年7月に報道されたが、同社は2026年開設予定を維持すると声明を出した[^43]。TSMCがアリゾナに資源を集中させる一方で、Samsungは日本への拠点拡張を見送ったとの分析もあり、両社の海外展開戦略には明確な差異が生じている[^44]。

### Intel: Foundry戦略の混乱と政府による株式化

2025年3月に就任した新CEOのリップブー・タン氏は、前任のパット・ゲルシンガー氏が注力した18Aプロセスについて、外部顧客からの関心が薄れていると2025年6月頃から言及したと報じられている[^45]。2026年に入り18A-PT（3次元ダイスタッキング対応）や14Aプロセスへの移行を強調するも、大口の外部顧客を獲得できていない状況が続いている[^46]。オハイオ工場の稼働開始は2025年予定から2027年から2028年へ延期された。同社は前述の通り、CHIPS法補助金の株式化により米政府が9.9%を保有する立場となっており、産業政策の後押しを受けてもファウンドリ事業の競争力を確立できていない状況が続いている。

### 中国SMIC・Huawei: 国家チーム体制による自給化

SMICは2021年から2024年に成熟ノードのファブ拡張に集中し、深センに23.5億ドル規模のファブを建設した[^47]。同社はDUVリソグラフィを用いた7ナノメートルプロセス(N+2)を開発し、2023年のHuawei Kirin 9000Sチップでその実用性を実証した[^47]。2025年から2026年にはHuawei Ascend 910B・910Cの量産という戦略的AIチップの生産に軸足を移し、2026年には7ナノメートル生産能力を倍増する計画である[^47]。SMICはHuawei Ascendシリーズの専属ファウンドリとなり、5ナノメートルノードの共同開発も進行中である[^47]。

Huaweiは設計から生産まで垂直統合的にサプライチェーンへの関与を深める「国家チーム」の主導役として位置づけられており、その役割分担の不透明性が西側による技術移転リスクの評価を困難にしていると分析されている[^48]。中国の半導体製造装置分野における技術的進展について、専門メディアは2020年代末までに世界のIT産業へ大きな影響を与える段階に達したと評価している[^49]。

TSMC・Samsung・Intelという西側3社を比較すると、地政学的耐性の確保を最優先課題として資源集中の判断を下したTSMCと、技術ロードマップと外部顧客獲得の両立に苦戦するIntelとの間には明確な実行力の差がある。中国はSMIC・Huaweiという国家主導体制のもとで、輸出規制下でも独自技術を用いたAIチップの内製化を進めており、規制の実効性を巡る論争を実務レベルで裏付ける事例となっている。

## 地域への波及: 二層構造化する供給網

地域別の影響を横断的に見ると、単純な国別の並列関係ではなく、「前工程の地政学的分散」と「後工程の機能的分散」という異なるメカニズムで再編が進行する二層構造が浮かび上がる。前工程は巨額投資と高度技術を要するため国家補助金と大企業の戦略的判断に左右され、後工程は相対的に参入障壁が低いため、地政学的リスクの低さと効率性を求める企業の判断によって東南アジア・インドが受益地となっている。

### 前工程の地政学的分散

米国では、CHIPS法による大規模な投資誘導が進む一方、半導体生産の倍増には23万人以上の新規雇用が必要とされる[^50]。2030年までに技術系人材の需要は385万人増加する見通しだが、そのうち136万人分は人材不足により欠員が生じるリスクがある[^51]。TSMCアリゾナ第1工場は当初2024年開設予定だったが、複雑な設備導入に必要な熟練労働者の不足により遅延した実例が報告されている[^52]。人材不足は補助金による誘導だけでは解消できない、オンショアリングの実務的な制約要因になっている。

日本では、電子情報技術産業協会(JEITA)の推計によれば、半導体部会に参加する9社だけで今後10年間に4万3000人の新規人材が必要とされる。この数字にはTSMC/JASM熊本やラピダス千歳の需要は含まれていない[^53]。日本全体では10年で4万人が必要とされ、そのうち九州がその4分の1を占めるとされる[^54]。日本は言語の壁により技術者が国内に留まりやすく、世界的に見て人材が豊富な地域と評価される側面もあり、これが海外大手半導体企業の日本進出の一因になっているとの指摘もある[^54]。内閣府の分析では、熊本のTSMC投資による地域経済効果は2024年秋から2025年から2026年頃に本格化すると予測されているが、地価上昇や人材確保、賃上げの波及効果への目配りが必要とされている[^55]。

欧州では、Intel撤退後の欧州半導体人材ギャップは2030年までに27万1400人と推計されている[^56]。ASMLという世界で唯一のEUV独占企業を域内に持ちながら、それを活用した製造拠点を確保できていないという「レバレッジの不活用」が指摘されている。台湾は世界の先端半導体90%超を担う一方、その集中度自体が地政学的リスクの源泉となっている。TSMCの海外投資拡大は台湾国内での技術・人材の空洞化への懸念を生んでおり、地政学的耐性の確保と自国の経済的独自性の維持という二つの目標がトレードオフの関係にある。

中国は輸出規制により先端ノードで制約を受けつつ、成熟ノードでは世界シェア28%に達する見通しであることは前述した。SMIC・Huaweiが国家主導で先端AIチップの内製化を進める一方、CXMT等はHBM量産化を目指すが、先端HBMへのアクセス制限が制約要因として残っている。

### 後工程の機能的分散

東南アジアの半導体市場は2025年の260.6億ドルから2034年の566.4億ドルへ拡大すると予測されており、年平均成長率は8.74%である[^57]。2032年までに世界のアセンブリ・テスト・パッケージング(ATP)容量の約25%を東南アジアが占める見通しで、マレーシア・フィリピンが中心的な役割を担う[^58]。シンガポール・マレーシアは域内のIC輸出額の78%を占めており、マレーシアは政治的安定性と物流ハブとしての地位を強みに「China+1」戦略の主要な受益国となっている[^59]。ベトナムはIntel・Amkor・Samsungの主要投資を集め、マレーシアのペナンはグローバルなアウトソース半導体組立・テスト(OSAT)拠点としての地位を強化している[^59]。

インドでは、Tata・ASML提携によるグジャラート州での前工程ファブ計画、Micronのアッセンブリ・テスト・パッケージング施設の稼働開始など、東南アジアと並ぶ後工程・組立拠点としての立ち上がりに加え、前工程への進出を目指す野心的な位置づけが見られる。

前工程と後工程で異なる速度の再編が進行していることは、サプライチェーン全体が単一の論理（地政学的耐性）だけで再編されているわけではないことを示している。地政学的リスクの高い工程（先端ロジック製造）は国家補助金と大企業の戦略的判断による重い投資判断を要し、地政学的リスクの低い工程（組立・パッケージング）は市場原理に近い効率性の論理で東南アジア・インドへの再配置が進んでいる。

## 持続可能性への問い: 耐性とコストのトレードオフ

再編の持続可能性を評価するには、地政学的耐性の確保という目的とコスト効率という制約のトレードオフを検討する必要がある。

### コスト増と重複投資の非効率性

米国・日本・欧州・台湾・韓国が同時に前工程ファブへ巨額投資する構造は、地政学的耐性の確保という目的には合理的だが、グローバルな生産効率の観点では同じ機能を持つファブを複数地域に重複して建設することによる固定費増大を意味する。TSMCアリゾナの対台湾コスト差が最大30%に達するという事実は、この非効率性の具体的な表れである。PwC Japanは、複数地域で製造能力が拡大すれば需要を上回る過剰生産能力というリスクが生じ、競争の激化と持続不可能な価格設定につながりかねないと評価している[^60]。

### 人材不足の恒常化

米国の23万人、日本の4万3000人、欧州の27万1400人という人材ギャップは、地域を問わず共通する制約要因である。これは短期的な補助金投資では解決できない構造的な制約であり、今後10年間のサプライチェーン再編の実現速度を規定する最大のボトルネックになる可能性が高い。補助金による生産能力拡大計画（SEMIが示す地域別投資額の予測）と実際の稼働開始時期には、Intel・Samsung・TSMCの各社で共通して数年単位の遅延が生じており、計画と実績のギャップは今後も継続するリスクを示唆する。

### シリコンサイクルの逆転リスクと成熟ノードの過剰供給

半導体産業の歴史においては、大規模投資の後に供給過剰による価格暴落が繰り返し発生してきた[^61]。この経験則（シリコンサイクル）に基づけば、レガシー半導体を中心に過剰供給が再び問題化するリスクが指摘されている。先端ロジックとメモリでは需要が供給能力を上回る逼迫状況が続く一方、成熟ノードでは既に一部で過剰供給の懸念が現実化しつつあるという非対称な状況が、業界の先行きを不確実にしている。

### AI投資の過熱とバブルリスク

2026年に入り、著名投資家マイケル・バーリ氏は現在の半導体相場が1999年から2000年のドットコムバブル終盤に似ていると警告し、SOXX ETFやNvidia等に対するプットオプションを取得した[^62]。フィラデルフィア半導体指数(SOX)は2026年に年初来65%上昇し、200日移動平均線を60%上回る歴史的に極端な水準に達した[^62]。2026年6月には半導体セクターで単日1.3兆ドル規模の急落も発生している[^63]。

一方でハイパースケーラー各社のAI投資は拡大が続いている。大手5社のAIインフラ投資は2026年に約7250億ドル（前年比64%増）に達する見通しであり[^64]、国際データコーポレーション(IDC)の統計では世界のAIインフラ投資は2024年の1530億ドルから2025年の3180億ドルへと倍増した[^65]。ゴールドマン・サックスの分析では、米国のデータセンター容量不足は現在11ギガワット超であり、2028年には45ギガワットに拡大するとされ、需要が供給を上回る状況が続くとの見方も併存している[^66]。技術的な実需（AIチップへの需要）と金融市場の期待（株価形成）が分離しうるという構図が、今後数年の最大の不確実性を形成している。

半導体製造の水集約的な性質も新たなコスト要因になっている。ファブ新設が最も進むアリゾナ・テキサスは、同時に最も水資源が逼迫した地域に分類されており、地域の水資源政策との衝突リスクが指摘されている[^67]。

### 地政学シナリオ: テールリスクとしての台湾有事

前述した台湾有事シナリオ（世界経済損失年間約1600兆円）は、依然として低頻度・高損失のテールリスクとして存在する。この一点だけで、現在進行中のサプライチェーン多極化・重複投資という非効率な戦略の経済的合理性が正当化されている。マッキンゼーは2030年までに業界全体で約1兆ドルの新規投資が計画されているが、人材・水資源・地政学・資本コストという規模拡大への障壁を克服する必要があると評価している[^68]。

## 情報の矛盾・不確実な点

調査の過程で、以下の点についてソース間の矛盾や確認の限界が確認された。

輸出規制の実効性については、CSISが原理的に中国の先端製造を封じると評価する一方、学術分析はむしろ中国の自前開発を加速させたと評価しており、評価が対立している[^10][^12]。これは分析対象とする技術レイヤー（EUVかDUVか）の違いに起因する可能性があるが、本文では両論を併記しヘッジ語を用いた。

中国の成熟ノード拡大が過剰供給に至るかどうかについても、CSIS・Ifriの「懸念は誇張されている」という評価と、ロディウム・グループ・CEPAの「持続的な問題」という評価が対立している[^37][^38]。同じデータに対する評価の相違であり、いずれか一方を確定的な結論として採用することはできない。

台湾有事シナリオの経済損失試算（世界経済損失年間約1600兆円）は、ブルームバーグ・エコノミクスという単一機関のシナリオ分析モデルに基づいており、他の独立機関による同種の推計との照合ができていない。前提条件（衝突の規模・期間）に強く依存する推定値として扱う必要がある[^16]。

日本の半導体関連支援の総額（「10兆円超」）は執筆時点で審議中の枠組みであり、確定額ではない[^28]。ラピダスへの累計支援額(2.9兆円)およびTSMC熊本への補助額(1兆2080億円)は、経済産業省の一次資料への直接照合ができておらず、日本経済新聞等の報道記事に基づく[^26][^27]。

中国の半導体関連補助金の総額（2000億ドル超）とファブ投資額の縮小予測（630億ドルから280億ドルへ）の関係は、本調査だけでは完全に解明できていない。補助金の使途内訳（装置購入、研究開発、企業救済等）の詳細な分解データには到達できなかった。

TSMCが日本拠点拡張を遅延させているという情報は2025年7月の報道に基づくが、TSMC自身の公式発表による直接確認はできていない[^40]。Intel 18Aの外部顧客の関心低下も匿名の関係者情報に基づく報道であり、Intel社自身は2026年に入り18Aの外部提供拡大に前向きな発言をしている点で、報道間にニュアンスの差がある[^45][^46]。

マイケル・バーリ氏の半導体バブル警告は、SEC提出資料に基づく報道に依拠しており、一次資料への直接照合はできていない。単一の著名投資家の見解であり、市場の総意を示すものではないことに留意する必要がある[^62]。

## 追加調査が必要な領域

本調査の範囲では十分にカバーできなかった論点として、以下が挙げられる。

中国の半導体補助金の使途内訳（成熟ノード拡張、装置国産化開発、既存企業救済への配分比率）は、投資額縮小という表面的な事実の背後にある実態を理解するために重要だが、本調査では詳細なデータに到達できなかった。

東南アジアのアセンブリ・テスト・パッケージング容量シェア予測（2032年に世界の25%）は業界系メディアの記述に依拠しており、SEMI等のより権威ある一次データ機関による裏付けが望ましい。

半導体製造装置分野における中国の自給化の進展度合いについて、具体的な生産数量・技術水準を示す定量データには到達できなかった。専門メディアの評価（技術的躍進の時代が到来した）の妥当性を検証するには、より詳細な技術指標の調査が必要である。

AI投資のバブルリスクと実需の関係については、2026年後半以降のハイパースケーラー各社の決算動向を追跡する必要がある。現時点の情報だけでは、金融市場の過熱がAI半導体の実需にどこまで先行しているかを判断することは難しい。

## 結論

本レポートの主題は、2024年以降のグローバル半導体サプライチェーン再編を駆動する要因と、その波及効果の解明であった。調査の結果、この再編は地政学的要因（台湾一極集中と輸出規制）、産業政策要因（各国の補助金競争とその実効性の分岐）、技術・需要要因（AI需要による先端逼迫と成熟ノードの過剰供給）という3つの力が同時に、かつ相互に強め合う形で作用した結果であることが明らかになった。地政学的リスクの認識が産業政策を正当化し、産業政策の遂行がAI需要という技術的な駆動力と結びついて、サプライチェーンを効率性優先の水平分業から多極化・重複投資型の構造へ転換させている。

最も重要な発見は3点に整理できる。第一に、この再編は前工程と後工程で異なる速度と論理で進行している。前工程（ファブ）は地政学的動機によって米国・日本・欧州・韓国・台湾に分散し、後工程（パッケージング・テスト）は効率性の論理によって東南アジア・インドに再配置されている。第二に、産業政策の効果は国・地域によって大きく分岐した。日本とインドは具体的な進展を見せた一方、EUはIntelの撤退と欧州会計監査院による目標未達の評価という停滞に陥り、米国はCHIPS法の株式化という政策の性質転換によって不確実性を増した。第三に、先端ノードでの需要逼迫と成熟ノードでの供給過剰が同時に進行するという二極化が生じており、この構造は西側と中国が異なる工程で相互に依存し続けるという新たな脆弱性を内包している。

この再編の含意は関係者によって異なる。政策当局にとっては、補助金の投入だけでは人材不足という構造的制約を解消できないという事実が、今後の産業政策設計における重要な教訓になる。半導体企業にとっては、地政学的耐性の確保とコスト効率の両立が困難であるという現実が、投資判断における恒常的なジレンマとして残る。投資家にとっては、AI半導体需要の実需と金融市場の期待がどこまで整合しているかという不確実性が、当面の最大のリスク要因になる。

今後注視すべき先行指標としては、TSMCアリゾナをはじめとする米国内ファブの実際の量産開始時期と歩留まりの推移、EUのChips Act 2.0の具体的な制度設計、中国の成熟ノード生産能力が実際に西側企業の事業性を損なう水準まで拡大するかどうか、そして2026年後半以降のハイパースケーラー各社の決算におけるAI投資の持続性が挙げられる。

短期から中期の展望としては、先端ノードにおける需要逼迫は少なくとも2027年頃までは継続する可能性が高く、TSMC・SK Hynix等の資本支出拡大はこの逼迫を反映した合理的な対応と評価できる。一方で、成熟ノードにおける供給過剰は既に一部で現実化しており、西側の既存レガシー半導体メーカーの事業再編が今後数年で進む可能性が高い。台湾有事という低頻度・高損失シナリオが解消されない限り、多極化投資という非効率な戦略は継続すると見込まれるが、この戦略の経済的な持続可能性は、各国の補助金政策が人材不足という構造的な制約をどこまで克服できるかに依存する。

## 出典

[^1]: [SEMI Fab Investment Outlook and Capacity Growth Projection](https://www.semi.org/sites/semi.org/files/2025-05/SEMI_Capex_market_outlook_5.28.2025_shared.pdf) — SEMI (2025/5) 〔一次照合〕

[^2]: [SEMI Reports Global 300mm Fab Equipment Spending Expected to Total $374 Billion Over Next Three Years](https://www.semi.org/en/products-services/market-data/fab-forecast) — SEMI 〔一次照合〕

[^3]: [America Projected to Triple Semiconductor Manufacturing Capacity by 2032](https://www.semiconductors.org/america-projected-to-triple-semiconductor-manufacturing-capacity-by-2032-the-largest-rate-of-growth-in-the-world) — SIA (2024/5/8) 〔一次照合〕

[^4]: [2025 State of the U.S. Semiconductor Industry](https://www.semiconductors.org/wp-content/uploads/2025/07/SIA-State-of-the-Industry-Report-2025.pdf) — SIA (2025/7) 〔一次照合〕

[^5]: [The Silicon Shield Erosion: Fortifying Taiwan Against Geopolitical Shocks](https://www.isdp.eu/the-silicon-shield-erosion-fortifying-taiwan-against-geopolitical-shocks) — ISDP (2024) 〔二次・独立複数〕

[^6]: [The Taiwan Semiconductor Risk: The $10 Trillion Chokepoint](https://longyield.substack.com/p/the-taiwan-semiconductor-risk-the) — Longyield / Substack 〔二次・独立複数〕

[^7]: [Why Taiwan Fears 'America First' Risks Eroding Its 'Silicon Shield'](https://www.stimson.org/2025/why-taiwan-fears-america-first-risks-eroding-its-silicon-shield) — Stimson Center (2025) 〔二次・独立複数〕

[^8]: [U.S. Export Controls and China: Advanced Semiconductors](https://www.congress.gov/crs-product/R48642) — Congressional Research Service 〔一次照合〕

[^9]: [Explaining all the US semiconductor export controls](https://forum.effectivealtruism.org/posts/C9fGQBGZmdTS3Gik6/explaining-all-the-us-semiconductor-export-controls) — EA Forum

[^10]: [Balancing the Ledger: Export Controls on U.S. Chip Technology to China](https://www.csis.org/analysis/balancing-ledger-export-controls-us-chip-technology-china) — CSIS

[^11]: [Balancing the Ledger: Export Controls on U.S. Chip Technology to China](https://www.csis.org/analysis/balancing-ledger-export-controls-us-chip-technology-china) — CSIS（Burn J. Lin氏証言の引用）

[^12]: [China's semiconductor conundrum: understanding US export controls and their efficacy](https://www.tandfonline.com/doi/full/10.1080/23311886.2025.2528450) — Tandfonline (2025) 〔二次・独立複数〕

[^13]: [China's semiconductor conundrum: understanding US export controls and their efficacy](https://www.tandfonline.com/doi/full/10.1080/23311886.2025.2528450) — Tandfonline（SMIC 2023年決算引用）

[^14]: [Selling the Forges of the Future](https://chinaselectcommittee.house.gov/sites/evo-subsites/selectcommitteeontheccp.house.gov/files/evo-media-document/selling-the-forges-of-the-future.pdf) — Select Committee on the CCP (2024) 〔一次照合〕

[^15]: [Adjusting Imports of Semiconductors, Semiconductor Manufacturing Equipment](https://www.whitehouse.gov/presidential-actions/2026/01/adjusting-imports-of-semiconductors-semiconductor-manufacturing-equipment-and-their-derivative-products-into-the-united-states) — The White House (2026/1/14) 〔一次照合〕

[^16]: [もし台湾侵攻が起きたなら 米中衝突や半導体危機、世界経済を揺るがす五つのシナリオ](https://www.bloomberg.com/jp/news/articles/2026-02-25/TAKKHBT96OSP00) — Bloomberg (2026/2/25) 〔要確認: 単一源泉/一次未確認〕

[^17]: [2025 State of the U.S. Semiconductor Industry](https://www.semiconductors.org/wp-content/uploads/2025/07/SIA-State-of-the-Industry-Report-2025.pdf) — SIA (2025/7) 〔一次照合〕

[^18]: [Where the CHIPS Fell: An Analysis of the CHIPS Act's Early Returns](https://sites.lsa.umich.edu/mje/2025/04/04/where-the-chips-fell-an-analysis-of-the-chips-acts-early-returns) — Michigan Journal of Economics (2025/4)

[^19]: [TSMC Semiconductor 2026, $52.7B CHIPS Act, Intel Delays](https://enkiai.com/ai-infrastructure/semiconductor-intel-tsmc-chips-act) — EnkiAI

[^20]: [Intel and Trump Administration Reach Historic Agreement](https://www.intc.com/news-events/press-releases/detail/1748/intel-and-trump-administration-reach-historic-agreement-to) — Intel IR (2025/8) 〔一次照合〕

[^21]: [The Trump Administration Should Refrain From Taking Equity in Semiconductor Companies](https://itif.org/publications/2025/08/21/the-trump-administration-should-refrain-from-taking-equity-in-semiconductor-companies) — ITIF (2025/8/21)

[^22]: [Intel's Retreat Shifts Europe Semiconductor Reality](https://www.eetimes.com/intel-retreat-shifts-europe-semiconductor-reality) — EE Times

[^23]: [EU Auditors criticize EU Chips Act targets amid EU Commission progress update](https://ieu-monitoring.com/editorial/european-chips-act-eu-commission-update-on-the-latest-milestones/614420) — European Court of Auditors 〔一次照合〕

[^24]: [Intel's Retreat Shifts Europe Semiconductor Reality](https://www.eetimes.com/intel-retreat-shifts-europe-semiconductor-reality) — EE Times（Bösenberg氏発言の引用）

[^25]: [Revamping Europe's chips strategy: indispensability, not self-sufficiency](https://www.bruegel.org/analysis/revamping-europes-chips-strategy-indispensability-not-self-sufficiency) — Bruegel

[^26]: [TSMC熊本第2工場に最大7,320億円補助 経産相表明](https://www.nikkei.com/article/DGXZQOUA2425J0U4A220C2000000/) — 日本経済新聞 〔要確認: 単一源泉/一次未確認〕

[^27]: [政府のラピダス支援、1兆円上積み方針 累計2.9兆円に](https://www.nikkei.com/article/DGXZQOUA218OG0R21C25A1000000/) — 日本経済新聞 〔要確認: 単一源泉/一次未確認〕

[^28]: [ラピダス支援を念頭に政府は10兆円の半導体・AI支援を決定](https://www.nri.com/jp/media/column/kiuchi/20241112_2.html) — 野村総合研究所 (2024/11/12)

[^29]: [India's Semiconductor Sector: Govt Support and Investment Trends](https://www.bisinfotech.com/indias-semiconductor-sector-a-deep-dive-into-government-support-and-investment-trends) — BISinfotech (2026)

[^30]: [Chipmaker TSMC Projects 2026 Capex will Reach $52 Billion-$56 Billion](https://www.industrialinfo.com/iirenergy/industry-news/article/chipmaker-tsmc-projects-2026-capex-will-reach-52-billion-56-billion--352061) — Industrial Info 〔二次・独立複数〕

[^31]: [What the AI-Driven Memory Chip Shortage Means for Buyers](https://www.z2data.com/guides/ai-memory-chip-shortage) — Z2Data

[^32]: [HBM Supply Crisis 2026: The Bottleneck Redefining AI](https://enkiai.com/data-center/hbm-supply-crisis-2026-the-bottleneck-redefining-ai) — EnkiAI (2026)

[^33]: [Samsung lost half its AI memory chip market share in 12 months](https://www.linkedin.com/posts/marko-vidrih_samsung-lost-half-its-ai-memory-chip-market-activity-7460999411662344192-jvUU) — LinkedIn / Marko Vidrih 〔要確認: 単一源泉/一次未確認〕

[^34]: [Memory's $200B Inflection](https://www.thediligencestack.com/p/memorys-200b-inflection) — The Diligence Stack / Ben Bajarin

[^35]: [China's mature chips to make up 28% of world production](https://finance.yahoo.com/news/chinas-mature-chips-28-world-163223670.html) — Yahoo Finance（TrendForce分析引用） 〔要確認: 単一源泉/一次未確認〕

[^36]: [Public Report on the Use of Mature-Node Semiconductors](https://www.bis.gov/media/documents/public-report-use-mature-node-semiconductors-december-2024) — BIS (2024/12) 〔一次照合〕

[^37]: [Legacy Chip Overcapacity in China: Myth and Reality](https://www.csis.org/blogs/trustee-china-hand/legacy-chip-overcapacity-china-myth-and-reality) — CSIS

[^38]: [Legacy Chips are a Lasting Problem](https://www.thewirechina.com/2025/10/12/legacy-chips-are-a-lasting-problem) — The Wire China (2025/10/12)

[^39]: [TSMC's $165B Arizona GigaFab: Reshaping US Chips](https://tech-insider.org/tsmc-arizona-165-billion-expansion-gigafab-2026) — Tech Insider (2026)

[^40]: [TSMC reportedly accelerates investment in Arizona chip complex as Samsung delays Texas fab](https://siliconangle.com/2025/07/04/tsmc-reportedly-accelerates-investment-arizona-chip-complex-samsung-delays-texas-fab) — SiliconANGLE (2025/7/4)

[^41]: [TSMC reportedly set to build 12 Arizona fabs as Japan, Germany expansions stall](https://www.digitimes.com/news/a20260106PD217/tsmc-arizona-market-germany-2026.html) — DigiTimes (2026/1/6)

[^42]: [TSMC Navigates Choppy Waters in Global Expansion Push](https://topics.amcham.com.tw/2025/09/tsmc-navigates-choppy-waters-in-global-expansion-push) — Taiwan Business Topics (2025/9)

[^43]: [Samsung will build $17B fab in Texas](https://www.sourcengine.com/blog/samsung-selects-taylor-texas-location-17-billion-chip-factory) — Sourcengine

[^44]: [Why TSMC Is Scaling in Arizona—and Why Samsung Said No to Japan](https://tspasemiconductor.substack.com/p/why-tsmc-is-scaling-in-arizonaand) — TSPA Semiconductor / Substack 〔要確認: 単一源泉/一次未確認〕

[^45]: [Exclusive: Intel's new CEO explores big shift in chip manufacturing business](https://www.reuters.com/business/retail-consumer/intels-new-ceo-explores-big-shift-chip-manufacturing-business-2025-07-02/) — Reuters (2025/7/2)

[^46]: [Intel reportedly reconsidering 18A strategy as CEO signals openness to external foundry customers](https://www.digitimes.com/news/a20260305VL209/intel-lip-bu-tan-semiconductor-foundry-technology.html) — DigiTimes (2026/3/5)

[^47]: [SMIC AI Chip Strategy 2026: Inside China's 5nm Power Play](https://enkiai.com/ai-market-intelligence/smic-ai-chip-strategy-2026-inside-chinas-5nm-power-play) — EnkiAI (2026) 〔二次・独立複数〕

[^48]: [Huawei is quietly dominating China's semiconductor supply chain](https://merics.org/en/report/huawei-quietly-dominating-chinas-semiconductor-supply-chain) — MERICS

[^49]: [Innovation under Pressure: China's Semiconductor Industry at a Crossroads](https://americanaffairsjournal.org/2026/02/innovation-under-pressure-chinas-semiconductor-industry-at-a-crossroads) — American Affairs Journal (2026/2) 〔要確認: 単一源泉/一次未確認〕

[^50]: [Rebuilding Our Semiconductor Workforce](https://lightcast.io/resources/research/rebuilding-our-semiconductor-workforce) — Lightcast 〔二次・独立複数〕

[^51]: [Chipping Away: Assessing and Addressing the Labor Market Gap](https://www.semiconductors.org/chipping-away-assessing-and-addressing-the-labor-market-gap-facing-the-u-s-semiconductor-industry) — SIA 〔一次照合〕

[^52]: [Shortage of semiconductor workers could impact climate firms](https://www.hbs.edu/bigs/shortage-of-semiconductor-workers-could-impact-climate-firms) — Harvard Business School

[^53]: [失われた20年を取り戻せ 日本脚光で半導体の人材不足に官民動く](https://special.nikkeibp.co.jp/atclh/ONB/24/fptjapan_gih/p14/) — 日経ビジネス 〔二次・独立複数〕

[^54]: [巨大な半導体市場がＡＩ需要で「今後１０年で倍」](https://www.yomiuri.co.jp/local/kyushu/news/20251219-GYS1T00018/) — 読売新聞 (2025/12/19)

[^55]: [地域課題分析レポート（2024年夏号）～半導体投資による地域経済への影響～](https://www5.cao.go.jp/j-j/cr/cr24-2/chr24-2youyaku.pdf) — 内閣府 (2024/9) 〔一次照合〕

[^56]: [Semiconductor Manufacturing Boom Faces a Workforce Challenge](https://www.linkedin.com/pulse/semiconductor-manufacturing-boom-faces-workforce-challenge-8chili-ugv6c) — LinkedIn（European Chips Skills Academy報告書引用） 〔要確認: 単一源泉/一次未確認〕

[^57]: [Southeast Asia Semiconductor Market Size and Report 2034](https://www.imarcgroup.com/southeast-asia-semiconductor-market) — IMARC Group

[^58]: [Semiconductor industry across Southeast Asia catching up!](https://pradeepstechpoints.wordpress.com/2025/11/25/semiconductor-industry-across-southeast-asia-catching-up) — PRADEEP's TECHPOINTS 〔要確認: 単一源泉/一次未確認〕

[^59]: [Malaysia is still the front-runner for China+1 strategy](https://research.jllapsites.com/malaysia-is-still-the-front-runner-for-china-plus-one-strategy) — JLL

[^60]: [半導体産業の現状](https://www.pwc.com/jp/ja/knowledge/thoughtleadership/state-of-the-semicon-industry.html) — PwC Japan

[^61]: [半導体不足の現状と解消見通し](https://orutedia.com/semiconductor-shortage/) — オルテディア

[^62]: [Michael Burry Semiconductor Bubble Warning](https://intellectia.ai/blog/semiconductor-bubble-warning-2026) — Intellectia (2026) 〔要確認: 単一源泉/一次未確認〕

[^63]: [Are AI and Semiconductor Stocks a Once-in-a-Generation Opportunity or an Overvalued Bubble?](https://www.kucoin.com/blog/are-ai-and-semiconductor-stocks-a-once-in-a-generation-opportunity-or-an-overvalued-bubble) — KuCoin (2026)

[^64]: [AI Capex Cycle 2026: $725B Hyperscaler Buildout](https://alcapitaladvisory.com/research/intelligence/ai-infrastructure.html) — AL Capital Advisory (2026/5/22) 〔二次・独立複数〕

[^65]: [Are AI and Semiconductor Stocks a Once-in-a-Generation Opportunity or an Overvalued Bubble?](https://www.kucoin.com/blog/are-ai-and-semiconductor-stocks-a-once-in-a-generation-opportunity-or-an-overvalued-bubble) — KuCoin（IDCデータ引用、2026/4）

[^66]: [AI Capex Cycle 2026: $725B Hyperscaler Buildout](https://alcapitaladvisory.com/research/intelligence/ai-infrastructure.html) — AL Capital Advisory（Goldman Sachs分析引用）

[^67]: [Rebuilding the US supply chain in a high-stakes world](https://www.pwc.com/us/en/industries/tmt/library/rebuilding-us-supply-chain.html) — PwC US

[^68]: [Semiconductors have a big opportunity—but barriers to scale remain](https://www.mckinsey.com/industries/semiconductors/our-insights/semiconductors-have-a-big-opportunity-but-barriers-to-scale-remain) — McKinsey

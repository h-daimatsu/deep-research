# 生成AIの電力需要がデータセンター立地と電力網に与える影響（シナリオ別分析）

**作成日**: 2026-07-03 JST

## エグゼクティブサマリー

本レポートの主題は、生成AIの電力需要急増がデータセンター(DC)の立地選択と電力網の設計、運用をどう構造的に変えつつあり、需要が高成長、基本、減速のどのシナリオをたどるかで何が起こりうるか、である。

調査から3点が明らかになった。第一に、需要の規模は大きいが不確実性も大きい。IEAはグローバルのDC電力消費が2024年の約460 TWhから2030年に約945 TWhへ倍増すると見込む一方、米国の2030年予測は機関により200 TWh未満から1,050 TWh超まで5倍以上に開く[^1][^2][^5][^6]。第二に、電力が立地の第一制約に転じた。系統接続に4〜10年を要するため、DCは「電力のある場所へ動く」(テキサス、中西部への地理的再編)か「電力を自前で持つ」(behind-the-meterガス、原子力併設)かの二方向に適応している[^11][^12][^18]。第三に、需要急増は電力網に不可逆的なコストを課し始めた。PJMでは容量価格が1年で約9倍に跳ね、独立市場監視はその上昇の63%(93億ドル)をDCに帰属させ、影響を「不可逆」と評した[^24][^26]。

結論の要旨は、需要が実現しても萎んでも、コストとリスクは一般消費者、系統、環境に非対称に転嫁される点にある。ハイパースケーラーは10 GW超の原子力契約と自家発で自らのリスクをヘッジする一方、系統価格の上昇、化石燃料設備の排出ロックイン、投機案件による接続渋滞は、需要が下振れした場合でも残存する[^30][^36][^40]。規制は「speed-to-power(接続の加速)」と「ratepayer protection(消費者保護)」という相反する二目標の間で、このコストを誰に配分するかを決めつつある。

## 生成AIの電力需要の規模と成長軌道

本章は、需要が現在どの程度で、どれだけ速く増え、予測がなぜこれほど食い違うかを扱う。以降の全章の出発点となる需要の量的枠組みを定める。

### グローバルと米国の需要の現状

IEAの特別報告書『Energy and AI』(2025)は、グローバルのDC電力消費を2024年の約460 TWhから2030年に約945 TWhへ倍増すると見込む。これは2030年時点でも世界の電力消費の3%弱にとどまるが、2024〜2030年に年約15%で増え、他の全部門合計の4倍超の速さである[^1]。DCへ供給する発電量ベースでは、460 TWh(2024)から1,000 TWh超(2030)、1,300 TWh(2035)へ拡大する[^3]。2025年だけでDC電力消費は17%増え、AI特化型DCに限れば50%急増した。同年、主要モデル提供者はアクティブユーザーの3倍増と収益の5倍増を報告している[^4]。

地理的な偏りが大きい。中国と米国で世界の成長の約80%を占め、米国は2024年比で+240 TWh(+130%)、中国は+175 TWh(+170%)増える見通しである[^1]。この集中が、後述する特定系統への負荷集中の起点となる。

### 主要機関の予測とレンジ

米国に焦点を絞ると、電力研究所(EPRI)の『Powering Intelligence 2026』は、DCが2030年に米国電力の9〜17%を消費すると予測する。現在の4〜5%からの倍増超であり、2024年版の推計より約60%上方修正された[^2]。ローレンス、バークレー国立研究所(LBNL)の2024年12月の議会報告は325〜580 TWh(米国電力の6.7〜12%)、マッキンゼーは最大12%とする[^5]。Rystad Energyは2024〜2035年に100 GW超のDC需要がオンライン化すると見込み、これはニューヨーク市の夏ピーク需要の約10倍に相当する[^5]。

### 予測が5倍に開く不確実性の源泉

米国の2030年予測は200 TWh未満から1,050 TWh超(上限はBCG、米国発電の約1/4相当)まで開く[^5][^6]。この5倍の開きは、後のシナリオ章の伏線であり、それ自体が重要な発見である。開きを生む要因は4つに整理できる。第一にAI利用率と普及速度の不確実性、第二にチップとソフトの効率改善速度、第三に冷却効率、第四にモデリング手法の差である。EPRIは商業開発案件のデータ、LBNLはチップ出荷見込みを基礎に置き、両者は2028年までは概ね整合する[^2][^5]。

WRIが指摘するとおり、DC電力消費が横ばいの時代が終わったことにはほぼ普遍的な合意がある一方、今後10年の増加幅については合意が乏しい[^5]。この「方向は確実、程度は不確実」という構図が、立地と系統への影響を評価する際の基本前提となる。

## 需要を押し上げる構造的ドライバー

前章の需要規模が「なぜ」生じるのかを、本章は計算需要の構造、効率化との関係、設備投資の三点から説明する。これらは需要が単なる一時的ブームではなく構造的に固定されつつある理由を示す。

### 計算需要の構造

需要増は3層で駆動される。第一に、チップ単体の消費電力が世代ごとにほぼ倍増している。DCのラック電力密度は従来型の約10 kWから、NVIDIA GB200 NVL72では最大132 kWへ跳ね上がった[^8][^9]。NVIDIAのCEOは2027年までにラックあたり600 kW、電力需要3倍を見込む[^10]。第二に、この高密度実装により空冷単独では熱を捨てきれず、液冷が必須となる。第三に、AI利用の普及が推論の総量を押し上げる。学習はモデル開発時に電力を集中的に消費するが、推論は1クエリあたりは小さくとも利用規模の拡大で総量を膨らませる。IEAはアクセラレーテッドサーバーがDC電力純増の約半分を占めると分析している[^1]。液冷必須化は、次章で述べる立地要件(冷却水、電力供給密度)の変化に直結する。

### 効率化は総需要を減らさない

「チップが効率化すれば電力問題は解決する」という楽観論には構造的な反証がある。2025年1月、中国のDeepSeekが低コストで高性能なモデルを示した際、電力、半導体株が急落したが、Microsoft CEOのSatya Nadellaは「Jevons paradox strikes again!(ジェボンズのパラドックス再来)」と投稿した[^13]。ジェボンズのパラドックスは、資源効率の改善がコストを下げて利用を拡大させ、結果として総消費を増やすという19世紀の経済学的知見である。効率化(FLOPS/W改善)は単位あたり消費を下げるが、AIの利用可能領域を広げることで総需要を押し上げる[^14][^15]。実際、DeepSeekの直後にMetaは2025年のAI支出を600〜650億ドル(+50%)へ引き上げ、Zuckerbergは「インフラのスケールアップは依然として重要な長期優位」と述べた[^16]。効率化が投資を抑えるのではなく加速させた事例である。

### 設備投資が固定する需要の下限

需要の下限は、すでに投じられた資本によってかなりの程度固定されている。米ハイパースケーラー4社(Amazon、Microsoft、Google、Meta)の2026年設備投資は合計約7,250億ドルに達する見込みで、2025年の約4,100億ドルから+77%である。内訳はAmazon約2,000億、Microsoft約1,900億、Google 1,750〜1,850億、Meta 1,150〜1,350億ドルで、大半がAI基盤(DC、チップ、電力)に向かう。アナリストは2027年に1兆ドル超を予測する[^17]。この規模の資本コミットメントは、短期の需要が投資済み案件でほぼ確定していることを意味する。需要が縮むには、これらの投資が撤回される必要があり、それには相応の摩擦が伴う。この点は減速シナリオの下限を規定する。

## データセンター立地の再編

前章の高密度化、液冷必須化、巨額投資を受けて、DCの立地はどう変わるか。本章は、電力制約が立地の第一決定要因となり、「電力のある場所へ動く」と「電力を自前で持つ」の二方向の適応を生み、その裏で系統接続キューが渋滞している構造を扱う。

### 立地決定要因の転換

DCの立地決定要因の首位が「電力アクセス」に交代した。CBREとBloom Energyの調査では、意思決定者の84%が電力可用性を上位3要因に挙げる[^19][^20]。かつて立地を決めた人口近接、光ファイバ、不動産コストを、電力が上書きした。系統接続のリードタイムは主要市場で4〜10年に伸び、接続タイミング(time-to-power)が不動産評価より先に検討される第一制約となった。業界では「Power Ready or Left Behind(電力が用意できなければ取り残される)」と表現される[^11]。

電力と並ぶ制約が水である。冷却に大量の水を要するため、イリノイ大学の分析によれば北バージニアのDC水使用量は2019〜2023年に約86%増えた[^21]。少数の施設が不均衡なシェアを占め、施設別の取水、消費、還流データは非開示が多く透明性が低い。この水制約は、後述する乾燥地域(テキサス)への集中と衝突しうる。

### 電力のある場所へ動く

第一の適応は、電力の得やすい地域への地理的再編である。Cushman & Wakefieldの2026年グローバルDC市場比較では、ダラスが初めて世界首位の主要DC市場となり、アトランタ(2位)、バージニア(3位)、コロンバス(4位)、ジョホール(5位)が続いた[^22]。バージニアは運用容量11.3 GWで最大を維持するが、テキサスは6.5 GWを建設中で、JLLは2030年に世界最大市場になると見込む。ERCOT系統の柔軟性、広大な土地、多様な電源が誘因である[^22][^23]。中西部(オハイオ、コロンバス)も全米2位のハブとして台頭した。米州全体で建設中容量の約80%を占める[^22]。

この再編は問題の解決ではなく移動の側面を持つ。特定系統の負荷集中を新規地域の系統へ移すだけで、水の乏しい地域への集中という新たな摩擦も生む。

### 電力を自前で持つ

第二の適応は、系統に頼らず電源を自前で確保するbehind-the-meter(BTM)方式である。BTMガス発電は系統接続を回避し、約18ヶ月で稼働できるため、年間数十億ドルの収益を生むAI案件にとって決定的な速さの優位を持つ[^12]。Meta とWilliamsはオハイオのNew Albany Hub向けに200 MWのガス発電を2基建設し、International Electric Powerはペンシルベニアで944 MWのガス発電をPJM接続を当面回避して計画する。CrusoeのアビリーンサイトはOracleとOpenAI向けに10基のタービンで360 MWを賄う[^12]。

原子力併設も進む。Talen EnergyのSusquehanna原発(ペンシルベニア)にはAmazonのDCが併設され、Talenは近隣の複合火力2.9 GWを35億ドルで取得した[^18]。BTM、原子力併設は系統接続を回避するため短期的には系統逼迫を緩和する一方、系統外での発電増(排出、地域環境影響)を生み、後述する「系統価格上昇を回避できる主体と負担が残る主体の格差」の起点となる。

### 系統接続キューの逼迫

二方向の適応の背後で、系統接続キューが渋滞している。PJM(13州、6,500万人をカバー)は2025年12月の容量オークションで、史上初めて信頼性要件に6.6 GW不足した(調達145,777 MW)。2027年夏に初めて容量不足に陥る見込みで、その主因はDC成長が新規電源を2対1で上回っていることにある[^11]。Gartnerは2027年までにAI DCの40%が電力制約に直面すると予測する[^11]。時間内に接続できる電力そのものが希少資源となり、これが立地の二方向適応を駆動している。

## 電力網への波及

前章の立地集中とBTM化が、電力網の運用、発電構成、料金にどう跳ね返るか。本章は送電網の逼迫、化石燃料回帰、一般消費者への価格転嫁の三点を扱う。

### 送電網の逼迫と増強コストの転嫁

需要急増に新規電源と送電が追いつかず、系統の増強コストが発生している。Goldman Sachsは、DC電力需要の+165%(2030年まで)を賄うにはこの10年で約7,200億ドルの系統投資が必要と試算する[^25]。問題は、この費用の負担が需要地と一致しないことである。メリーランド州は州外のDC負荷増のための送電プロジェクト費用を負担しており、PJMは2010〜2030年に43億ドルの送電資本費をメリーランドに配分した[^28]。DCがメリーランドになくとも、州の需要家が州外DCの系統増強を負担する構図である。送電費の他州転嫁は、ペンシルベニア州でのPJM離脱論など制度的緊張を生んでいる[^24]。

### 発電構成の化石燃料回帰

速く建設できる電源が優先される結果、発電構成は化石燃料へ回帰している。電力会社はDC需要を理由に石炭火力の退役を延期または再稼働し、新規ガス火力を建設している。DominionはClover石炭ピーカー(バージニア州Halifax郡)の退役延期の主因にDC需要を挙げた[^29]。ガス火力の拡大は顕著で、米国の夏季ガス火力焚き量は過去最高の40.3 Bcf/dに達する見込みである[^31]。Global Energy Monitorによれば、米国は新規ガス火力開発で世界首位となり、テキサスは80.6 GWを開発中で、うち約40 GWがDCを直接の電源とする。テキサス単独で次点7州の合計を上回り、世界では中国のみが上回る規模である[^30]。BCGは炭素回収付きガス火力が2030年までの約80 GWの信頼性ギャップを埋めうるとする[^32]。

この化石燃料回帰には長期のコストが伴う。ガス拡張と石炭退役延期は数十年分の温室効果ガス排出を固定化する。WRIとEESIが警告するとおり、仮に需要が実現しなくても設備は残り、排出のロックインが生じる[^7][^33]。

### 系統信頼性と一般消費者への価格転嫁

最も可視的な波及が、一般消費者への価格転嫁である。PJMの容量オークションの支払総額は147億ドルから161億ドルへ上昇した[^27]。独立市場監視のMonitoring Analyticsは、2025/26オークションの価格上昇の63%がDCに起因し、顧客が負担する額は93億ドルに上ると推計した[^26]。容量価格は2024/25から2025/26で約9倍に跳ね、2026/27でさらに+22%上がった[^24]。13州の消費者は2026年夏から電気料金が1.5〜5%上昇する見込みである[^27]。卸電力価格ではさらに急で、PJMのQ1 2026の卸価格は前年同期比約76%上昇し($77.78→$136.53/MWh)、市場監視は「顧客への価格影響は非常に大きく、不可逆」と評した[^24]。

信頼性面でも懸念が生じている。NERCは稀なLevel 3警報を発出し、DC負荷が瞬時に脱落する挙動が系統の安定を脅かすとして対策を義務付けた[^37]。ただし価格上昇の原因は単一ではない。CATFは、地域ごとに主要ドライバーが異なり、燃料費、供給網、送電など複数要因が絡むと留保する[^34]。DCは主要な押し上げ要因の一つだが、唯一の要因ではない。この「不可逆」な価格影響は、需要が後に鈍化しても消費者負担が残ることを意味し、次章のシナリオ分析における非対称性の核心となる。

## シナリオ別の帰結

第2〜5章の因果構造を、需要の分岐点で束ねる。本章は高成長、基本、減速の3シナリオで立地、電力網、価格、排出の帰結を横断的に示し、最後にシナリオを貫く非対称リスクを論じる。分岐を決める要因は5つある。AI収益化、需要実現度、効率改善速度(ただしジェボンズで相殺されうる)、投機的キューと実需の比率、物理供給制約(変圧器、タービン、接続枠)、資金調達の持続性である。

### 高成長シナリオ

需要が予測の上限で推移するシナリオである。Goldman Sachsは米国DC電力を31 GW(2025)から41 GW(2026)、66 GW(2027)へ、容量を2027年末に約95 GWへ倍増(稼働率70%仮定)すると予測する。年間容量追加は2024年の6.4 GW、2025年の8.5 GWから2026年13.6 GW、2027年36.3 GWへ加速する[^35]。EPRIのHighシナリオ(米国電力の17%)がこれに対応する[^2]。このシナリオを下支えするのは、ハイパースケーラーの「AI投資の減速は過剰投資より大きなリスク」という戦略姿勢であり、約6,500〜7,250億ドルの支出は当面大幅削減されないと見られる[^17][^36]。この局面では資本ではなく物理資産(通電済み電力、変圧器、系統接続権、建屋)がボトルネックとなる[^36]。帰結として、立地は「電力のある場所+自家発」へ一段と再編し、系統価格の上昇と化石燃料回帰が加速する。

### 基本シナリオ

中位の普及が続き、供給が概ね追随するシナリオである。IEAのBase Case(グローバル約945 TWh)とEPRIのMediumシナリオ(米国電力の約12%)が対応する[^1][^2]。EPRIのMediumシナリオでは、バージニアに加えて7州が2030年にDC比率20%超に達する[^2]。このシナリオでも系統逼迫と価格上昇は続くが、高成長シナリオほど急激ではなく、規制と系統増強がある程度追いつく余地がある。

### 効率化と減速のシナリオ

需要が下振れするシナリオで、根拠は複数ある。第一に投機的接続要求の水増しである。同一案件が複数の系統キューに重複登録され、負荷予測を過大化させる。カリフォルニア州ではCECが接続要求を基に公式負荷予測を作るため、過剰建設のリスクがある[^38]。ITIFは、取り下げられた要求でも系統運用者に信頼性検討を強いてキューを渋滞させ、住宅、病院、再エネの接続を遅らせると指摘する[^39]。第二に歴史的前例である。1990年代のインターネット期待で光ファイバ網が大幅に過剰建設され、容量が実需を上回って資産が長年ストランドした[^41]。スタンフォードのAmory Lovinsらは、投機的サージが12桁(数千億ドル)規模の過剰建設を招くと警告し、1999年に石炭業界が「ITが2020年までに米国電力の半分を必要とする」と主張して外した前例を挙げる[^42]。第三に資金面のバブル論で、2025年11月に半導体株が急落し、収益化が未実証のまま巨額投資が先行しているとの懸念がある[^43]。

ただし需要の実在性は一様ではない。SemiAnalysisは、キャンセルや遅延は構造的に供給過剰な層に集中し、site control、発注済み機器、系統接続契約を備えた「本物」の案件は堅いと分析する[^44]。EPRIのLowシナリオ(米国電力の9%)やLBNLの下限(325 TWh帯)がこのシナリオに対応する[^2][^5]。

### シナリオ横断の非対称リスク

3シナリオを貫く構造的な発見が、コストとリスクの非対称な配分である。需要が実現すれば、系統逼迫、価格上昇、化石燃料回帰が加速する。需要が萎んでも、投機キューによる接続渋滞と、前倒しで建設したガス火力、送電設備の座礁資産化、排出ロックインは残る。どちらに転んでも、一般消費者、系統、環境がコストを負担しうる構造である[^33][^39][^42]。この非対称性を増幅するのがBTM自家発である。系統価格の上昇を回避できるハイパースケーラーと、系統に残されて負担を被る一般消費者との格差を広げるためである[^12][^24]。次章のステークホルダー分析は、このコストを誰に配分するかを巡る攻防として読める。

## ステークホルダーと政策規制の対応

各シナリオの実現性を左右するアクターの行動を整理する。本章は、需要と系統の橋渡しをする三者(ハイパースケーラー、系統側の主体、地域社会と政治)がどう動いているかを扱う。

### ハイパースケーラーの調達戦略

ハイパースケーラーは、系統制約と価格上昇を回避すべく電源を自前で確保する垂直統合を進めている。ホワイトハウスが2026年3月に示した「build, bring, or buy(自前建設、持ち込み、購入)」という枠組みは、彼らの行動を的確に整理する[^45]。中核は原子力ラッシュである。2026年5月時点で主要ハイパースケーラー全社が最低1件の原子力契約を結び、合計10 GW超の新規原子力を契約した。各社の発表と報道によれば、Microsoftは160億ドルでThree Mile Island(Crane Clean Energy Center)を再稼働(835 MW、初電力2027年)、Googleは500 MWのKairos SMR、Amazonは200億ドルのSusquehanna投資、MetaはVistraとの契約に加え1〜4 GWのRFPを出した[^40]。20年PPAという契約期間は、AI電力需要が数十年続くという業界の賭けを示す。NVIDIAとMicrosoftは2026年3月に「AI for nuclear」で提携し、許認可、設計、運転をAIで効率化しようとしている[^46]。

単一電源ではスケール、信頼性、持続可能性を同時に満たせないため、原子力、再エネPPA(Brookfieldの10.5 GW枠組み)、ガスバックアップ、核融合(Helion)を組み合わせるマルチ技術、マルチ地域調達が標準となっている[^47]。ただしCarnegie Endowmentは、これらの原子力コミットメントを米国エネルギーの現実に照らすと、新設のタイムラインとコスト超過のリスクが大きいと留保する[^48]。

### 電力会社、系統運用者、規制当局

系統側では、連邦が歴史的な介入に踏み切った。DOE長官の指示を受けたFERCは、2026年6月18日、連邦電力法206条に基づき6つのRTO/ISO(PJM、MISO、ISO-NE、NYISO、SPP、CAISO)全てに「show cause命令」を発出し、大規模負荷の託送料金扱いを「不当、不合理」と暫定認定した[^49][^50]。狙いは、DCへのspeed-to-power(接続の加速)と他の需要家保護の両立である。従来、負荷の系統接続は州、地方の管轄だったが、連邦が枠組みを定める方向に動いた。州レベルでは、PG&Eが大規模負荷専用料金を提案するなど、全米の電力会社がDCに魅力的でありつつ他の需要家にコストを転嫁しない料金設計を模索している。争点は、送電設備のコスト配分の管轄、送電費の負担主体、他の需要家クラスへのコストやリスクの転嫁の回避である[^51]。

### 地域社会、一般消費者、議会

第4章、第5章で見た価格転嫁は、政治的な反発を生んでいる。同じ消費者保護でも処方は真逆に割れる。ホワイトハウスのbuild/bring/buy誓約が、DCに自らの電力コストを負担させることで系統への影響を抑える市場的アプローチであるのに対し、Sanders上院議員とAOC下院議員が2026年3月25日に提出した「AI Data Center Moratorium Act(S.4214)」は、料金保護が保証されるまでハイパースケールDC建設そのものを一時停止する規制的アプローチである[^45][^52]。地域社会の反対と州レベルのモラトリアムも現実の逆風となっている[^48]。これらの政策は前章の非対称リスクの配分に直接作用する。専用料金やコスト配分ルールが「DCが自らのコストを負担する」方向に進めば、投機的キューの淘汰が進んで減速シナリオ側に作用し、speed-to-power優先なら高成長側を後押しする。

## 情報の矛盾・不確実な点

- **需要予測の巨大なレンジ**: 米国DCの2030年予測は200 TWh未満から1,050 TWh超まで5倍以上開く[^5]。これは矛盾というより方法論(商業開発データ vs チップ出荷 vs トップダウン)と前提(AI普及率、効率化)の差に起因する。本レポートは特定の一点予測を採用せず、シナリオ幅として扱った。
- **テキサスのガス開発規模(80.6 GW、DC向け40 GW)**: 単一ソース(Global Energy Monitor)に依拠しており、一次照合ができていない〔要確認: 単一源泉〕[^30]。方向(米国のガス火力世界首位化)は複数ソースで裏付けられるが、正確なGW値は要確認である。
- **変圧器5年バックログ**: 供給制約の代表例として引用したが、出所がSNS経由(All-inポッドキャスト)であり、一次的な統計に未到達である〔要確認: 単一源泉〕。変圧器、タービンのリードタイム長期化という方向は複数ソースと整合する[^36]。
- **契約金額(Microsoft TMI 160億ドル、Amazon Susquehanna 200億ドル)**: 報道ベースで複数媒体が一致するが、各社IR原本の文言、金額を直接照合できていない〔要確認: 一次未確認〕[^40]。
- **北バージニアの水使用+86%(2019-23)**: 単一の学術ソース(イリノイ大学)に依拠し、一次の公益事業データに未到達である〔要確認: 単一源泉〕[^21]。
- **価格上昇のDC寄与度(63%)**: PJM独立市場監視という一次的機関の推計だが、原本レポートを直接照合しておらず、複数媒体の引用に依拠した。CATFが指摘するとおり価格は複合要因であり、単一の帰属には幅がある[^26][^34]。

## 追加調査が必要な領域

- **米国外の状況**: 本レポートは米国を主軸としたが、中国(世界成長の約半分)、欧州、日本、東南アジア(ジョホール)の立地と系統の動向は十分に調査できなかった。グローバルな需要の8割を占める米中の比較は結論を左右しうる。
- **一次原本の照合**: FERC show cause命令(原本URL存在)は照合できたが、各社IRの契約金額、PJM市場監視レポート原本、Global Energy Monitorのデータセットは直接照合していない。事実抽出系の正確な数値確定には一次照合が必要である。
- **AIの収益化の実証**: 需要の持続性はAIの収益化に依存するが、本調査では収益化の実データ(ROI、普及率の推移)まで踏み込めなかった。減速シナリオの蓋然性を評価する鍵となる。
- **水、地域環境影響の定量化**: 水使用、消費、還流の施設別データは非開示が多く、立地再編の環境制約を定量評価できなかった。
- **系統技術の緩和策**: 需要の柔軟化(curtailment、負荷シフト)、蓄電、送電技術の進展が非対称リスクをどこまで緩和しうるかは、今後の動向で結論が変わりうる。

## 結論

本レポートの主題は、生成AIの電力需要急増がDCの立地と電力網をどう変え、シナリオ別に何が起こりうるか、であった。その答えは、需要の程度は不確実だが方向は確実であり、いずれのシナリオでもコストとリスクは一般消費者、系統、環境に非対称に転嫁される、というものである。

調査で最も重要な発見は3点である。第一に、電力が立地の第一制約に転じ、DCは「電力のある場所へ動く」(テキサス、中西部)か「電力を自前で持つ」(BTMガス、原子力併設)かの二方向に適応している。第二に、需要急増はPJMで容量価格を約9倍に押し上げ、その6割超がDCに帰属し、市場監視が「不可逆」と評すほど消費者負担が固定化している。第三に、この負担は非対称である。需要が実現すれば系統逼迫と化石燃料回帰が進み、萎んでも投機キューの渋滞と設備の座礁、排出ロックインが残る。

この構造の意味は、関係者ごとに異なる。ハイパースケーラーにとっては、原子力、自家発への垂直統合が系統リスクからの合理的なヘッジであり、build/bring/buyはそのコストを内部化する枠組みとして機能する。電力会社と系統運用者にとっては、投機的キューと実需の腑分けが最大の実務課題であり、専用料金とコスト配分ルールの設計が需要の淘汰を左右する。一般消費者にとっては、DC由来の系統コストをどこまで自らが負担するかが料金として跳ね返る。規制当局にとっては、speed-to-powerとratepayer protectionの相反を、どちらに軸足を置いて調停するかが問われている。

注視すべき先行指標は、DC専用料金とコスト配分ルールの帰趨(DCがコストを内部化する方向か)、系統接続キューの投機案件の淘汰状況(site controlや発注済み機器を伴う実需の比率)、PJMをはじめとする容量、卸価格の推移、ハイパースケーラーの設備投資ガイダンスの上方/下方修正、そしてFERCのshow cause手続きの着地である。これらは需要がどのシナリオに向かうかを2026〜2028年に判別する材料となる。

短期から中期の展望としては、現時点で利用可能な情報に基づくと、需要規模はIEA Base CaseとEPRI Mediumが示す基本シナリオ近傍(米国電力の約12%)に収束する蓋然性が最も高い。約7,000億ドル規模の設備投資が下限を固定する一方、系統接続の物理制約(4〜10年待ち、変圧器、タービン不足)が上限を抑えるためである。ただしこの見立ては、AIの収益化が続きハイパースケーラーが投資姿勢を維持することを前提とする。収益化が失速すれば減速シナリオへ、逆に生成AIの用途が急拡大すれば高成長シナリオへ振れる。いずれのシナリオでも非対称リスクの配分は残るため、規制と料金設計がコストを誰に負わせるかを決める。この配分の設計が、今後2〜3年で最も注視すべき論点である。

## 出典

[^1]: [Energy demand from AI — Energy and AI](https://www.iea.org/reports/energy-and-ai/energy-demand-from-ai) — IEA (2025) 〔一次照合〕

[^2]: [Executive Summary — Powering Intelligence 2026](https://powering-intelligence.epri.com/executive-summary.html) — EPRI (2026) 〔一次照合〕

[^3]: [Energy supply for AI — Energy and AI](https://www.iea.org/reports/energy-and-ai/energy-supply-for-ai) — IEA (2025) 〔一次照合〕

[^4]: [Executive summary — Key Questions on Energy and AI](https://www.iea.org/reports/key-questions-on-energy-and-ai/executive-summary) — IEA (2025) 〔一次照合〕

[^5]: [Powering the US Data Center Boom: Why Forecasting Can Be So Difficult](https://www.wri.org/insights/us-data-centers-electricity-demand) — WRI 〔二次・独立複数〕

[^6]: [US Data Center Power Demand Forecast (206–970 TWh by 2030)](https://incorrys.com/data-centers/us-data-center-power-demand-forecast/) — Incorrys 〔二次・独立複数〕

[^7]: [Data Centers and Rising Energy Demand in the US](https://www.wri.org/energy/data-centers-and-rising-energy-demand-us) — WRI 〔二次・独立複数〕

[^8]: [AI data center design and deployment are moving at an incredible pace](https://blog.se.com/datacenter/2025/07/23/ai-data-center-design-and-deployment-are-moving-at-an-incredible-pace-3-ways-to-approach-a-changing-landscape) — Schneider Electric Blog (2025/7/23) 〔二次・独立複数〕

[^9]: [End-to-End Critical Power and Cooling Reference Designs for NVIDIA GB200 NVL72](https://www.youtube.com/watch?v=m0cehU9JHOA) — Vertiv (2024/10/15) 〔二次・独立複数〕

[^10]: [NVIDIA Data Center GPU Specs: A Complete Comparison Guide](https://intuitionlabs.ai/articles/nvidia-data-center-gpu-specs) — IntuitionLabs 〔二次・独立複数〕

[^11]: [Power Ready or Left Behind: Data Center Site Selection in 2026](https://www.lviassociates.com/en-us/industry-insights/hiring-advice/power-ready-or-left-behind-data-center-site-selection-in-2026) — LVI Associates (2026) 〔二次・独立複数〕

[^12]: [How AI Labs Are Solving the Power Crisis: The Onsite Gas Deep Dive](https://newsletter.semianalysis.com/p/how-ai-labs-are-solving-the-power) — SemiAnalysis 〔二次・独立複数〕

[^13]: [DeepSeek claims to have cured AI's environmental headache. The Jevons paradox suggests it might make things worse](https://theconversation.com/deepseek-claims-to-have-cured-ais-environmental-headache-the-jevons-paradox-suggests-it-might-make-things-worse-248720) — The Conversation 〔二次・独立複数〕

[^14]: [Why the AI world is suddenly obsessed with Jevons paradox](https://www.npr.org/sections/planet-money/2025/02/04/g-s1-46018/ai-deepseek-economics-jevons-paradox) — NPR Planet Money (2025/2/4) 〔二次・独立複数〕

[^15]: [How the AI boom shrugged off the DeepSeek shock and keeps gaining steam](https://www.piie.com/blogs/realtime-economics/2026/how-ai-boom-shrugged-deepseek-shock-and-keeps-gaining-steam) — PIIE (2026) 〔二次・独立複数〕

[^16]: [The Jevons Paradox in AI Infrastructure: DeepSeek Efficiency Breakthroughs to Drive Energy Demand](https://substack.com/home/post/p-156281340) — Substack 〔二次〕

[^17]: [AI Hyperscaler Capex Compared: Why Microsoft, Google, Meta, and Amazon Are All Spending at Once](https://valueaddvc.com/blog/ai-hyperscaler-capex-compared-why-microsoft-google-meta-and-amazon-are-all-spending-at-once) — ValueAdd VC 〔二次・独立複数〕

[^18]: [Power Hungry: AI-Fueled Data Center Boom Sets Energy Delivery's New Course](https://www.enr.com/articles/61083-power-hungry-ai-fueled-data-center-boom-sets-energy-deliverys-new-course) — Engineering News-Record 〔二次・独立複数〕

[^19]: [Power Availability: The New #1 in Data Center Site Selection](https://www.hanwhadatacenters.com/blog/power-availability-the-new-1-in-data-center-site-selection) — Hanwha Data Centers 〔二次・独立複数〕

[^20]: [2026 Data Center Power Report](https://www.bloomenergy.com/wp-content/uploads/2026-power-report.pdf) — Bloom Energy (2026) 〔一次照合〕

[^21]: [Data Center Expansion in Virginia: Closing Critical Gaps for Informed Water Planning and Permitting](https://securewater.illinois.edu/data-center-expansion-in-virginia-closing-critical-gaps-for-informed-water-planning-and-permitting) — Univ. of Illinois Center for Secure Water 〔要確認: 単一源泉/一次未確認〕

[^22]: [Dallas, Texas Ranked No. 1 Primary Data Market in the World](https://ir.cushmanwakefield.com/news/press-release-details/2026/Dallas-Texas-Ranked-No--1-Primary-Data-Market-in-the-World-as-AI-Demand-Power-Constraints-and-Regulation-Reshape-CRE-Strategy/default.aspx) — Cushman & Wakefield IR (2026) 〔一次照合〕

[^23]: [U.S. Data Center Expansion by Region](https://www.irecruit.co/insights/us-data-center-expansion-by-region) — iRecruit 〔二次・独立複数〕

[^24]: [Data centers drive 76% surge in PJM power prices](https://www.eenews.net/articles/data-centers-drive-76-surge-in-pjm-power-prices) — E&E News by POLITICO 〔二次・独立複数〕

[^25]: [AI to drive 165% increase in data center power demand by 2030](https://www.goldmansachs.com/insights/articles/ai-to-drive-165-increase-in-data-center-power-demand-by-2030) — Goldman Sachs Research 〔一次照合〕

[^26]: [Projected data center growth spurs PJM capacity prices by factor of 10](https://ieefa.org/resources/projected-data-center-growth-spurs-pjm-capacity-prices-factor-10) — IEEFA 〔二次・独立複数〕

[^27]: [Energy bills likely to tick up again in 2026 after electricity auction clears at maximum price](https://marylandmatters.org/2025/07/23/energy-bills-likely-to-tick-up-again-in-2026-after-electricity-auction-clears-at-maximum-price) — Maryland Matters (2025/7/23) 〔二次・独立複数〕

[^28]: [Rising Transmission Costs (2026-03-25)](https://opc.maryland.gov/Portals/0/Files/Publications/Rising%20Transmission%20Costs%202026-03-25%20CORRECTED%20FINAL.pdf) — Maryland Office of People's Counsel (2026/3/25) 〔一次照合〕

[^29]: [Coal- and gas-fired power plants have a new best friend: data centers](https://www.utilitydive.com/news/fossil-fuel-gas-coal-climate-data-centers/753565/) — Utility Dive 〔二次・独立複数〕

[^30]: [Betting big on data centers, U.S. now leads world for new gas power development](https://globalenergymonitor.org/research/betting-big-data-centers-us-now-leads-world-new-gas-power-development) — Global Energy Monitor 〔要確認: 単一源泉/一次未確認〕

[^31]: [Record Power Burn Expected This Summer as Coal Retirements and Data Centers Drive Gas Demand](https://www.powermag.com/record-power-burn-expected-this-summer-as-coal-retirements-and-data-centers-drive-gas-demand/) — POWER Magazine 〔二次・独立複数〕

[^32]: [Solving the US Data Center Power Crunch](https://www.bcg.com/publications/2026/solving-the-us-data-center-power-crunch) — BCG (2026) 〔二次・独立複数〕

[^33]: [Data Center Buildout Is Hungry for Fossil Fuels](https://www.eesi.org/articles/view/data-center-buildout-is-hungry-for-fossil-fuels) — EESI 〔二次・独立複数〕

[^34]: [A data-driven look at rising U.S. electricity costs and policy solutions](https://www.catf.us/2026/03/data-driven-look-rising-us-electricity-costs-policy-solutions) — Clean Air Task Force (2026/3) 〔二次・独立複数〕

[^35]: [What Is the Forecast for US Data Center Power Demand?](https://www.marcus.com/us/en/resources/heard-at-gs/what-is-the-forecast-for-us-data-center-power-demand-) — Goldman Sachs Research / Marcus 〔二次・独立複数〕

[^36]: [U.S. AI Data Center Delays: 7 GW Capacity Crisis](https://tech-insider.org/us-ai-data-center-delays-cancellations-7gw-capacity-crisis-2026/) — Tech Insider (2026) 〔要確認: 単一源泉/一次未確認〕

[^37]: [NERC issues Level 3 alert, mandates action to address data center load losses](https://www.utilitydive.com/news/nerc-issues-rare-level-3-alert-over-data-center-load-losses/819295/) — Utility Dive 〔二次・独立複数〕

[^38]: [How Will Data Center Growth Impact California Ratepayers?](https://www.publicadvocates.cpuc.ca.gov/press-room/commentary/251027-how-will-data-center-growth-impact-california-ratepayers) — CPUC Public Advocates Office 〔一次照合〕

[^39]: [Five Concerns About AI Data Centers, and What to Do About Them](https://itif.org/publications/2026/04/06/five-concerns-about-ai-data-centers-and-what-to-do-about-them/) — ITIF (2026/4/6) 〔二次・独立複数〕

[^40]: [Nuclear power for AI: inside the data center energy deals](https://introl.com/blog/nuclear-power-ai-data-centers-microsoft-google-amazon-2025) — Introl 〔要確認: 一次未確認〕

[^41]: [How AI and Data Centers Are Driving Load Volatility](https://www.resource-innovations.com/resource/how-ai-and-data-centers-are-driving-load-volatility) — Resource Innovations 〔二次・独立複数〕

[^42]: [Artificial Intelligence Meets Natural Stupidity: Managing the Risks](https://integrative-design-for-radical-energy-efficiency.stanford.edu/sites/extreme_energy_efficiency/files/media/file/data-centersaiel-dr-16-10-may-2025.pdf) — Stanford / Amory Lovins et al. (2025/5) 〔二次・独立複数〕

[^43]: [AI Data Center Mania is 'Epic Bubble,' Says Brad Conger](https://www.youtube.com/watch?v=WK7wNRs5G68) — Bloomberg Podcasts (2025/11/5) 〔二次〕

[^44]: [Stop Saying Half of 2026 US Datacenter Capacity Is Canceled](https://newsletter.semianalysis.com/p/stop-saying-half-of-2026-us-datacenter) — SemiAnalysis 〔二次・独立複数〕

[^45]: [Fact Sheet: President Donald J. Trump Advances Energy Affordability with the Ratepayer Protection Pledge](https://www.whitehouse.gov/fact-sheets/2026/03/fact-sheet-president-donald-j-trump-advances-energy-affordability-with-the-ratepayer-protection-pledge/) — The White House (2026/3) 〔一次照合〕

[^46]: [Beyond the Hype: Assessing Hyperscaler Nuclear Commitments Against U.S. Energy Realities](https://carnegieendowment.org/research/2026/06/beyond-the-hype-assessing-hyperscaler-nuclear-commitments-against-us-energy-realities) — Carnegie Endowment (2026/6) 〔二次・独立複数〕

[^47]: [The Data Center Power Boom: AI Demand, Hyperscaler Offtake, and 50+ GW of Incremental Load](https://ibinterviewquestions.com/guides/energy-investment-banking/data-center-power-boom-ai-demand-hyperscaler) — Energy IB 〔二次〕

[^48]: [Data Center Investment in 2026: AI Demand, Power Constraints, and Private Equity Trends](https://www.ropesgray.com/en/insights/viewpoints/102mvfl/data-center-investment-in-2026-ai-demand-power-constraints-and-private-equity) — Ropes & Gray (2026) 〔二次・独立複数〕

[^49]: [FERC orders grid operators to promptly revise or justify interconnection rules for data centers and large loads](https://www.whitecase.com/insight-alert/ferc-orders-grid-operators-promptly-revise-or-justify-interconnection-rules-data) — White & Case (2026/6) 〔二次・独立複数〕

[^50]: [Order Instituting Proceeding Under Section 206 (195 FERC ¶ 61213)](https://spp.org/documents/76996/20260618_show%20cause%20order%20on%20large%20and%20co-located%20loads_el26-68-000.pdf) — FERC (2026/6/18) 〔一次照合〕

[^51]: [A Tariff on Data Centers Could Help Them Pay Their Fair Share](https://legal-planet.org/2026/06/29/a-tariff-on-data-centers-could-help-them-pay-their-fair-share) — Legal Planet (2026/6/29) 〔二次・独立複数〕

[^52]: [Resolved: The United States Federal Government Should Enact a Moratorium on Hyperscale Data Center Construction](https://debatearguments.substack.com/p/resolved-the-united-states-federal-fd0) — Debate Arguments 〔二次〕

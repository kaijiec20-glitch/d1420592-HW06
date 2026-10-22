<!DOCTYPE html>
<!-- 宣告使用 HTML5；DOCTYPE 是文件類型宣告，不需要結束標籤。 -->
<html lang="zh-Hant">
<!-- html 包住整份文件；lang="zh-Hant" 表示主要使用繁體中文。 -->
<head>
    <!-- head 放網頁資訊；這些資訊不會直接成為頁面中的報導文字。 -->
    <meta charset="UTF-8">
    <!-- UTF-8 可正確處理中文；meta 是空元素，不寫結束標籤。 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- viewport 讓行動裝置使用裝置寬度；不代表固定寬度的圖片會自動縮小。 -->
    <meta name="description" content="走進台中糖廠（湧泉公園與帝國製糖廠），認識百年工業遺產與湖濱生態，透過清單、表格、照片和影片閱讀城市轉型故事。">
    <!-- description 提供網頁摘要；author 標示作者。 -->
    <meta name="author" content="陳楷劼d1420592">
    <title>台中糖廠報導｜工業遺產與湖濱新生</title>
    <!-- title 顯示在瀏覽器分頁；與 body 中的 h1 用途不同。 -->

    <style>
        /* ==========================================================
           HW05 CSS 樣式設定
           主題：台中糖廠工業遺產與湖濱新生
           風格：人文赤陶紅與深灰工業質感配色
           ========================================================== */

        /* 全局變數設定 */
        :root {
            --primary-color: #8c3b2b;       /* 帝國糖廠紅磚赤陶色 */
            --primary-hover: #6a2c20;       /* 深紅 hover 狀態 */
            --secondary-color: #2c3e50;     /* 沉穩藍灰/鐵色 */
            --bg-color: #fcfbf9;            /* 暖調微黃背景 */
            --card-bg: #ffffff;             /* 卡片白底 */
            --text-main: #333333;           /* 主文字深灰 */
            --text-muted: #666666;          /* 次要文字灰 */
            --border-color: #e2dacd;        /* 溫和框線顏色 */
            --accent-bg: #f4efe8;           /* 區塊底色 */
            --shadow: 0 4px 12px rgba(0, 0, 0, 0.05); /* 輕微陰影 */
        }

        /* 基礎重置與整體排版 */
        * {
            box-sizing: border-box;
        }

        body {
            font-family: "PingFang TC", "Microsoft JhengHei", "Noto Sans TC", sans-serif;
            line-height: 1.8;
            color: var(--text-main);
            background-color: var(--bg-color);
            margin: 0;
            padding: 20px;
        }

        /* 限制整體內容最大寬度並置中 */
        header, nav, main, footer {
            max-width: 900px;
            margin: 0 auto;
        }

        /* 連結樣式優化 */
        a {
            color: var(--primary-color);
            text-decoration: none;
            transition: color 0.2s ease, text-decoration 0.2s ease;
        }

        a:hover, a:focus {
            color: var(--primary-hover);
            text-decoration: underline;
        }

        /* 分隔線 */
        hr {
            border: none;
            border-top: 2px dashed var(--border-color);
            max-width: 900px;
            margin: 30px auto;
        }

        /* 頁首 (Header) */
        header {
            background-color: var(--card-bg);
            padding: 30px 40px;
            border-radius: 12px;
            border-left: 8px solid var(--primary-color);
            box-shadow: var(--shadow);
            margin-bottom: 25px;
        }

        header h1 {
            color: var(--primary-color);
            font-size: 2rem;
            margin-top: 0;
            margin-bottom: 10px;
            letter-spacing: 0.5px;
        }

        header p {
            margin: 6px 0;
            color: var(--text-muted);
        }

        /* 導覽目錄 (Nav) */
        nav {
            background-color: var(--accent-bg);
            padding: 20px 30px;
            border-radius: 10px;
            border: 1px solid var(--border-color);
            margin-bottom: 25px;
        }

        nav h2 {
            font-size: 1.25rem;
            color: var(--secondary-color);
            margin-top: 0;
            margin-bottom: 12px;
            border-bottom: 2px solid var(--primary-color);
            display: inline-block;
            padding-bottom: 4px;
        }

        nav ul {
            list-style-type: none;
            padding-left: 0;
            margin: 0;
            display: flex;
            flex-wrap: wrap;
            gap: 12px 20px;
        }

        nav li a {
            font-weight: bold;
            display: inline-block;
            padding: 4px 8px;
            border-radius: 4px;
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
        }

        nav li a:hover {
            background-color: var(--primary-color);
            color: #ffffff;
            text-decoration: none;
        }

        /* 主體區塊 (Main & Article & Section) */
        main {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        section {
            background-color: var(--card-bg);
            padding: 30px;
            border-radius: 10px;
            border: 1px solid var(--border-color);
            box-shadow: var(--shadow);
        }

        section h2 {
            color: var(--primary-color);
            font-size: 1.5rem;
            margin-top: 0;
            margin-bottom: 18px;
            padding-bottom: 8px;
            border-bottom: 2px solid var(--accent-bg);
        }

        section h3 {
            color: var(--secondary-color);
            font-size: 1.2rem;
            margin-top: 20px;
            margin-bottom: 10px;
        }

        /* 清單間距優化 */
        ul, ol {
            padding-left: 24px;
            margin-bottom: 15px;
        }

        li {
            margin-bottom: 8px;
        }

        /* 表格 (Table) 樣式調整 */
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background-color: var(--card-bg);
            font-size: 0.95rem;
        }

        caption {
            caption-side: top;
            text-align: left;
            font-weight: bold;
            margin-bottom: 10px;
            color: var(--secondary-color);
        }

        th, td {
            padding: 12px 16px;
            border: 1px solid var(--border-color);
            text-align: left;
        }

        thead tr {
            background-color: var(--primary-color);
            color: #ffffff;
        }

        thead th {
            font-weight: 600;
        }

        tbody tr:nth-child(even) {
            background-color: var(--accent-bg);
        }

        tbody th {
            background-color: rgba(140, 59, 43, 0.05);
            color: var(--primary-color);
            font-weight: bold;
        }

        /* 多媒體呈現 (Figure & Image & Video) */
        figure {
            margin: 20px 0 0 0;
            text-align: center;
        }

        img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            box-shadow: var(--shadow);
            border: 1px solid var(--border-color);
        }

        figcaption {
            margin-top: 10px;
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        /* 響應式嵌入影片容器 (RWD 16:9) */
        .video-container {
            position: relative;
            width: 100%;
            padding-bottom: 56.25%; /* 16:9 比例 */
            height: 0;
            overflow: hidden;
            border-radius: 8px;
            box-shadow: var(--shadow);
            margin-bottom: 15px;
        }

        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: 0;
        }

        /* 頁尾 (Footer) */
        footer {
            text-align: center;
            padding: 20px;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        footer a {
            display: inline-block;
            margin-top: 8px;
            font-weight: bold;
        }

        /* 平板與手機版微調 (RWD) */
        @media (max-width: 600px) {
            body {
                padding: 10px;
            }
            header, section, nav {
                padding: 20px;
            }
            header h1 {
                font-size: 1.5rem;
            }
            nav ul {
                flex-direction: column;
                gap: 8px;
            }
            th, td {
                padding: 8px 10px;
                font-size: 0.85rem;
            }
        }
    </style>
</head>

<body>
    <!--
        第四次作業：一頁式台中糖廠專題報導。
        本範例保留標準 HTML5 語意標籤，並透過 head 內的 CSS 進行外觀美化與響應式排版。
        註解使用「小於符號、驚嘆號、兩個連字號」開始，並以兩個連字號及大於符號結束。
        使用一致的四個空格縮排；成對標籤都明確寫出結束標籤。
    -->

    <!-- header 是頁首；id="top" 是下方「回到頁首」連結的目的地。 -->
    <header id="top">
        <!-- h1 是本頁主標題；h2 用於各章節，依內容階層選用標題。 -->
        <h1>台中糖廠：工業遺產與湖濱新生的對話</h1>
        <p>從舊台中糖廠到帝國糖廠湖濱公園與湧泉公園，一起見證東區的百年工業記憶。</p>
        <!-- time 的 datetime 以標準日期格式提供機器可讀的日期。 -->
        <p>作者：陳楷劼d1420592｜報導整理日期：<time datetime="2026-10-09">2026 年 10 月 9 日</time></p>
        <p><small>本文為資料整理型教學報導，非現場採訪紀錄。</small></p>
    </header>

    <!-- nav 表示導覽區；href="#名稱" 會跳到本頁相同 id 的元素。 -->
    <nav aria-label="報導目錄">
        <h2>報導目錄</h2>
        <ul>
            <li><a href="#intro">糖廠簡介</a></li>
            <li><a href="#highlights">景點特色與參觀順序</a></li>
            <li><a href="#table">景點比較表</a></li>
            <li><a href="#photo">帝國糖廠照片</a></li>
            <li><a href="#video">影音報導</a></li>
            <li><a href="#sources">資料來源</a></li>
        </ul>
    </nav>

    <hr>

    <!-- main 包住本頁主要內容；article 表示可獨立閱讀的完整報導。 -->
    <main>
        <article aria-label="台中糖廠專題報導">
            <!-- section 將報導分成有標題的章節；同一頁中的 id 不可重複。 -->
            <section id="intro">
                <h2>一、糖廠簡介</h2>
                <!-- p 表示段落；strong 強調重要資訊，不用來取代標題。 -->
                <p>
                    台中糖廠創建於日治時期（1912年），曾是中部地區重要的製糖重鎮，
                    見證了台灣糖業的輝煌歷史與鐵道運輸的發展。隨著時代變遷，
                    糖廠停止生產後歷經多年轉型，如今已蛻變為結合歷史建築與生態休閒的公共空間。
                </p>
                <p>
                    園區內最具代表性的核心建築為<strong>帝國糖廠台中營業所</strong>，
                    結合周邊的湧泉公園與星泉湖生態綠地，
                    成為台中東區兼具文創展覽與親水休憩的熱門地標。
                </p>
                <p>
                    從工業機具的歷史遺跡到現代化的湖濱生態公園，台中糖廠宛如一部立體的城市發展史。
                    本篇將透過景點整理與建議參觀順序，帶領讀者重新認識這處新舊交融的場域。
                </p>
                <!-- br 僅用於同段文字中需要的換行；不要用很多 br 製造間距。 -->
                <p>園區地址：台中市東區進德路 700 號。<br>閱讀重點：歷史建築、湖濱生態與工業遺產轉型。</p>
            </section>

            <section id="highlights">
                <h2>二、景點特色與參觀順序</h2>
                <h3>值得留意的三個特色</h3>
                <!-- ul 是無序清單；li 是個別項目，適合不分先後的資訊。 -->
                <ul>
                    <li><strong>歷史建築：</strong>帝國糖廠營業所展現日治時期的紅磚與鋼構建築美學。</li>
                    <li><strong>湖濱生態：</strong>湧泉公園與星泉湖畔的環湖步道提供豐富的自然景觀。</li>
                    <li><strong>文創基地：</strong>結合展覽、市集與餐飲，為老舊工業區注入全新活力。</li>
                </ul>

                <h3>建議參觀順序</h3>
                <p>以下是本報導規劃的參觀建議，並非官方指定路線。</p>
                <!-- ol 是有序清單；瀏覽器會依 li 的排列產生編號。 -->
                <ol>
                    <li>抵達園區後，先參觀帝國糖廠營業所本館，了解糖廠歷史展覽。</li>
                    <li>走到湧泉公園與星泉湖畔，沿著環湖步道欣賞水面與周邊景致。</li>
                    <li>前往戶外休憩區與裝置藝術景點，觀察工業遺產的保存現況。</li>
                    <li>在園區內的咖啡廳或文創空間稍作休息，總結今日的參觀收穫。</li>
                </ol>
            </section>

            <section id="table">
                <h2>三、景點比較表</h2>
                <!--
                    table 用於呈現資料，不用來排版整個網頁。
                    透過 CSS 移除過時的內聯 border 屬性，改由外部 CSS 統一管制樣式。
                -->
                <table>
                    <!-- caption 是表格標題，放在 table 內最前面。 -->
                    <caption>台中糖廠園區三處重點區域特色與觀察重點</caption>
                    <!-- thead 包住表頭；tr 是一橫列；th 是標題儲存格。 -->
                    <thead>
                        <tr>
                            <!-- scope="col" 表示這個 th 是整欄的標題。 -->
                            <th scope="col">區域名稱</th>
                            <th scope="col">主要特色</th>
                            <th scope="col">建議觀察重點</th>
                        </tr>
                    </thead>
                    <!-- tbody 包住資料列；td 是一般資料儲存格。 -->
                    <tbody>
                        <tr>
                            <!-- scope="row" 表示這個 th 是本列的標題。 -->
                            <th scope="row">帝國糖廠營業所</th>
                            <td>保留完整的歷史建築與常設展</td>
                            <td>建築外觀結構與內部文創展覽空間</td>
                        </tr>
                        <tr>
                            <th scope="row">湧泉公園</th>
                            <td>結合生態與休憩的湖濱公園</td>
                            <td>星泉湖生態、環湖步道與綠地景觀</td>
                        </tr>
                        <tr>
                            <th scope="row">湖濱綠地步道</th>
                            <td>結合舊鐵道與綠化景觀的散步道</td>
                            <td>工業遺址地景與現代休閒設施的結合</td>
                        </tr>
                    </tbody>
                </table>
            </section>

            <section id="photo">
                <h2>四、帝國糖廠照片</h2>
                <!-- figure 將圖片與圖說組成一個單位；figcaption 是圖說。 -->
                <figure>
                    <!--
                        img 是空元素，不寫 /img 結束標籤。
                        src 指定圖片網址；本範例使用外部圖片，需要連線才能載入。
                        alt 描述照片內容，圖片未載入時或使用螢幕閱讀器時仍可理解。
                    -->
                    <img
                        src="https://images.abic.com.tw/photoDB/post/1729412342.jpg"
                        alt="台中糖廠帝國糖廠湖濱公園與景觀"
                        width="480">
                    <figcaption>
                        帝國糖廠湖濱公園是台中東區的地標。
                        圖片來源：<a href="https://www.abic.com.tw/place/view/id/12946" target="_blank" rel="noopener noreferrer">親子台灣景點介紹頁</a>。
                    </figcaption>
                </figure>
            </section>

            <section id="video">
                <h2>五、影音報導</h2>
                <p>透過下方影片認識台中糖廠、帝國糖廠與湧泉公園，再比較影片畫面與本文介紹的景點。</p>
                <!--
                    使用 .video-container 包裹 iframe 以實現響應式 16:9 播放器。
                -->
                <div class="video-container">
                    <iframe
                        src="https://www.youtube.com/embed/eROq8N6AExg"
                        title="台中湧泉公園與帝國糖廠介紹影片"
                        allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                        referrerpolicy="strict-origin-when-cross-origin"
                        allowfullscreen>
                    </iframe>
                </div>
                <!-- a 提供一般影片連結；播放器無法播放時仍能前往 YouTube。 -->
                <p>
                    若播放器無法播放，請
                    <a href="https://youtu.be/eROq8N6AExg" target="_blank" rel="noopener noreferrer">在 YouTube 觀看湧泉公園與帝國糖廠介紹影片（另開分頁）</a>。
                </p>
                <p><small>影片為外部作者發布的歷史與景點介紹，現場狀況請以最新官方資訊為準。</small></p>
            </section>

            <section id="sources">
                <h2>六、資料來源</h2>
                <p>本報導依下列資料整理，參觀順序與觀察建議由作者規劃。</p>
                <!--
                    target="_blank" 另開分頁；rel 保護開啟新頁面的關聯。
                    網址中的 & 在 HTML 原始碼中寫成 &amp;。
                -->
                <ul>
                    <li><a href="https://www.taichung.gov.tw/" target="_blank" rel="noopener noreferrer">臺中市政府觀光旅遊網：帝國糖廠湖濱公園</a></li>
                    <li><a href="https://www.abic.com.tw/place/view/id/12946" target="_blank" rel="noopener noreferrer">親子旅遊網：帝國糖廠湖濱公園介紹（含圖片來源）</a></li>
                    <li><a href="https://youtu.be/eROq8N6AExg" target="_blank" rel="noopener noreferrer">YouTube：湧泉公園與帝國糖廠介紹影片</a></li>
                </ul>
                <p><small>資料整理日期：2026 年 10 月 9 日。</small></p>
            </section>
        </article>
    </main>

    <hr>
    <!-- footer 是頁尾；來源與作者標示應依自己的作品修改。 -->
    <footer>
        <p>第五次 HTML/CSS 作業範例｜台中糖廠專題報導</p>
        <p><a href="#top">回到頁首</a></p>
    </footer>
</body>
</html>
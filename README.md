<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>武田病院グループ 夏期インターンシッププログラム「フクシノイリグチ」</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css"> <!-- フォーム用に追加 -->
    <style>
        /* グローバルなスタイル */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8f9fa;
            color: #343a40;
            overflow-x: hidden; /* 横方向のスクロールを防止 */
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            color: #28a745; /* 緑色 */
            margin-bottom: 2rem;
            text-align: center;
        }
        .card {
            background-color: #ffffff;
            border-radius: 1rem;
            box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.1);
            padding: 2rem;
            margin-bottom: 2rem;
        }
        .header-bg {
            background: linear-gradient(to right, #28a745, #218838);
            color: white;
            padding: 4rem 2rem;
            text-align: center;
            border-bottom-left-radius: 2rem;
            border-bottom-right-radius: 2rem;
        }
        .btn-primary {
            background-color: #28a745;
            color: white;
            padding: 0.75rem 2rem;
            border-radius: 0.75rem;
            font-weight: 600;
            transition: background-color 0.3s ease;
            display: block; /* ボタンをブロック要素にして改行 */
            margin-left: auto; /* 中央寄せ */
            margin-right: auto; /* 中央寄せ */
            cursor: pointer;
            text-decoration: none; /* aタグのデフォルトの下線を消す */
        }
        .btn-primary:hover {
            background-color: #218838;
        }
        /* テキストロゴのスタイル */
        .text-logo {
            font-size: 3.5rem; /* より大きく */
            font-weight: 700;
            color: white; /* ヘッダーの背景色に合わせて白に */
            margin-bottom: 2rem;
            display: block; /* 中央揃えのため */
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3); /* テキストに影を追加 */
        }
        @media (max-width: 768px) {
            .text-logo {
                font-size: 2.5rem; /* モバイルでの表示調整 */
            }
        }

        /* ハイライトされたテキストの背景スタイル */
        .highlight-box {
            background-color: rgba(220, 255, 220, 0.9); /* 薄い緑色の背景 */
            padding: 1.5rem;
            border-radius: 1rem;
            margin-top: 1.5rem; /* 上の要素との間隔 */
            margin-bottom: 1.5rem; /* 下の要素との間隔 */
            box-shadow: 0 0.25rem 0.75rem rgba(0,0,0,0.1); /* 影を追加 */
            display: inline-block; /* コンテンツの幅に合わせる */
            max-width: 100%; /* 親要素からはみ出さないように */
        }

        .course-card {
            background-color: #e9ecef;
            border-radius: 1rem;
            padding: 1.5rem;
            margin-bottom: 1rem;
        }
        .course-title {
            font-size: 1.75rem;
            font-weight: 600;
            color: #28a745;
            margin-bottom: 0.5rem;
        }
        .feature-list li {
            list-style: none;
            margin-bottom: 0.5rem;
            padding-left: 1.5rem;
            position: relative;
        }
        .feature-list li::before {
            content: '✓';
            color: #28a745;
            position: absolute;
            left: 0;
        }
        .facility-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }
        .facility-card {
            background-color: #ffffff;
            border-radius: 1rem;
            box-shadow: 0 0.25rem 0.5rem rgba(0, 0, 0, 0.05);
            padding: 1.5rem;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 250px;
        }
        .contact-info {
            background-color: #e9ecef;
            border-radius: 1rem;
            padding: 2rem;
            text-align: center;
        }
        .btn-secondary {
            background-color: #6c757d;
            color: white;
            padding: 0.75rem 2rem;
            border-radius: 0.75rem;
            font-weight: 600;
            transition: background-color 0.3s ease;
            margin-top: 1rem;
        }
        .btn-secondary:hover {
            background-color: #5a6268;
            transform: translateY(-2px);
        }

        /* フォームの埋め込みスタイル */
        /* main.containerに適用されているpaddingを考慮し、form-page-containerはbodyのpaddingで対応 */
        .form-page-container {
            max-width: 700px;
            margin: 0 auto;
            padding: 0 20px; /* bodyのpaddingと合わせる */
        }
        .internship-form-section h2 {
            font-size: 2.5rem;
            margin-bottom: 30px;
            color: #0056b3;
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
        }
        .internship-form-section h2::after {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            bottom: 0;
            width: 60px;
            height: 3px;
            background-color: #28a745;
            border-radius: 2px;
        }
        .internship-form-section p {
            max-width: 700px;
            margin: 0 auto 30px;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        .internship-form {
            max-width: 700px;
            margin: 0 auto;
            padding: 40px;
            background-color: #fff;
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
            text-align: left;
        }
        .form-group {
            margin-bottom: 25px;
        }
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #555;
            font-size: 1rem;
        }
        .form-group input[type="text"],
        .form-group input[type="email"],
        .form-group input[type="tel"],
        .form-group textarea,
        .form-group select,
        .form-group input[type="date"] {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: border-color 0.3s ease, box-shadow 0.3s ease;
        }
        .form-group .date-range-group {
            display: flex;
            gap: 10px;
            align-items: center;
        }
        .form-group .date-range-group input[type="date"] {
            width: calc(50% - 15px);
        }
        .form-group .date-range-group span {
            width: 30px;
            text-align: center;
        }
        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus,
        .form-group input[type="date"]:focus {
            border-color: #007bff;
            box-shadow: 0 0 0 3px rgba(0,123,255,0.25);
            outline: none;
        }
        .required-star {
            color: #dc3545;
            margin-left: 5px;
            font-size: 0.9em;
        }
        .btn-submit-form { /* フォーム内の送信ボタンのスタイル */
            width: 100%;
            padding: 15px;
            background-color: #28a745;
            color: #fff;
            border: none;
            border-radius: 8px;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.2s ease;
            box-shadow: 0 4px 15px rgba(40,167,69,0.4);
        }
        .btn-submit-form:hover {
            background-color: #218838;
            transform: translateY(-2px);
        }
        
        /* Confirmation Modal Styles (フォームと共通で再定義) */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 2000;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }
        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }
        .modal-content {
            background-color: #fff;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            max-width: 600px;
            width: 90%;
            transform: scale(0.95);
            transition: transform 0.3s ease;
            position: relative;
        }
        .modal-overlay.active .modal-content {
            transform: scale(1);
        }
        .modal-content h3 {
            font-size: 2rem;
            color: #0056b3;
            margin-bottom: 25px;
            text-align: center;
        }
        .confirmation-details {
            border-top: 1px solid #eee;
            padding-top: 20px;
            margin-top: 20px;
            max-height: 400px;
            overflow-y: auto;
        }
        .confirmation-detail-item {
            display: flex;
            flex-wrap: wrap;
            margin-bottom: 15px;
            align-items: baseline;
            line-height: 1.5;
        }
        .confirmation-detail-label {
            font-weight: bold;
            color: #333;
            min-width: 120px;
            flex-basis: 30%;
            text-align: right;
            padding-right: 15px;
            box-sizing: border-box;
        }
        .confirmation-detail-value {
            color: #555;
            flex-basis: 70%;
            flex-grow: 1;
            text-align: left;
            word-break: break-word;
        }
        @media (max-width: 550px) {
            .confirmation-detail-item {
                flex-direction: column;
                align-items: flex-start;
            }
            .confirmation-detail-label {
                text-align: left;
                min-width: unset;
                flex-basis: 100%;
                padding-right: 0;
                margin-bottom: 5px;
            }
            .confirmation-detail-value {
                flex-basis: 100%;
            }
        }
        .modal-actions {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #eee;
        }
        .modal-button {
            padding: 12px 25px;
            border-radius: 8px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
            border: none;
        }
        .modal-button.btn-edit {
            background-color: #6c757d;
            color: #fff;
            box-shadow: 0 4px 15px rgba(108,117,125,0.4);
        }
        .modal-button.btn-edit:hover {
            background-color: #5a6268;
            transform: translateY(-2px);
        }
        .modal-button.btn-confirm-submit {
            background-color: #28a745;
            color: #fff;
            box-shadow: 0 4px 15px rgba(40,167,69,0.4);
        }
        .modal-button.btn-confirm-submit:hover {
            background-color: #218838;
            transform: translateY(-2px);
        }
    </style>
</head>
<body>
    <div id="event-page-content">
        <!-- ヘッダーセクション -->
        <header class="header-bg">
            <div class="container">
                <!-- 武田病院グループのロゴをテキストに置き換え -->
                <h2 class="text-logo">武田病院グループ本部福祉介護部</h2>
                <h1 class="text-4xl md:text-5xl font-bold mb-4">2025年夏期インターンシッププログラム</h1>
                <p class="text-2xl md:text-3xl font-semibold mb-6">「フクシノイリグチ」<br>見て聞いて触れる1日業界研究</p>
                <div class="highlight-box mx-auto">
                    <p class="text-xl leading-relaxed text-black">
                        <span class="font-bold">当グループのインターンシップを受けていただくと、</span><br>
                        <span class="font-bold text-green-600">「人に感謝される仕事のやりがい」</span><br>
                        <span class="font-bold text-green-600">「エッセンシャルワークの本質」</span><br>
                        <span class="font-bold text-green-600">「介護の仕事に対するマイナスイメージの払拭」</span><br>
                        <span class="font-bold">これらを実感していただけることをお約束します！</span>
                    </p>
                </div>
                <button onclick="showApplicationForm()" class="btn-primary block mx-auto mt-8">エントリーはこちら</button>
            </div>
        </header>

        <main class="container">
            <!-- コース紹介セクション -->
            <section id="courses" class="py-12">
                <h2 class="section-title">コース紹介</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <!-- コースI -->
                    <div class="card">
                        <h3 class="course-title">Ⅰ. 企業説明会・施設見学会<br>（オープンカンパニー）</h3>
                        <p class="text-gray-700 mb-4">対面・オンライン形式で開催し、介護業界や武田病院グループについて深く知ることができます。</p>
                        <ul class="feature-list">
                            <li>日程：令和7年7月～9月</li>
                            <li>定員：1日につき3名</li>
                            <li>所要時間：1時間30分程度（オンラインは1時間）</li>
                        </ul>
                        <p class="text-gray-600 mt-4">「介護業界を知りたい」「施設の中を見てみたい」という方に最適です。</p>
                    </div>

                    <!-- コースII -->
                    <div class="card">
                        <h3 class="course-title">Ⅱ. 介護の仕事・相談援助の仕事<br>お気軽体験1日コース</h3>
                        <p class="text-gray-700 mb-4">介護現場の1日の流れや認知症の方への対応、相談援助の具体的な内容を体験できます。</p>
                        <ul class="feature-list">
                            <li>日程：令和7年7月～9月</li>
                            <li>定員：1日につき2名</li>
                            <li>時間：10:00～15:00（昼食付）</li>
                        </ul>
                        <p class="text-gray-600 mt-4">実際の介護現場を体験し、仕事のイメージを掴みたい方におすすめです。</p>
                    </div>

                    <!-- コースIII -->
                    <div class="card">
                        <h3 class="course-title">Ⅲ. 介護の仕事・相談援助の仕事<br>ガッツリ体験フリーカスタマイズコース</h3>
                        <p class="text-gray-700 mb-4">あなたの希望に合わせて、介護や相談援助の仕事を深く、自由に体験できるプログラムです。</p>
                        <ul class="feature-list">
                            <li>日程：令和7年7月～9月</li>
                            <li>定員：介護体験型 1日につき2名、相談援助体験型 1日につき1名</li>
                            <li>時間：10:00～15:00（昼食付）</li>
                        </ul>
                        <p class="text-gray-600 mt-4">24時間365日異なる介護や、多様な相談援助の仕事を体験できます。</p>
                    </div>
                </div>
            </section>

            <!-- 各コース詳細セクション -->
            <section id="course-details" class="py-12">
                <h2 class="section-title">各コース詳細</h2>

                <!-- コースI 詳細 -->
                <div class="card">
                    <h3 class="text-2xl font-bold text-green-700 mb-4">Ⅰ. オープンカンパニー（企業説明会・施設見学会）</h3>
                    <p class="mb-4">介護業界、武田病院グループ、働き方、職場の雰囲気について知りたいというあなたの疑問を解消するセミナーです。</p>
                    <p class="font-bold mb-2">オンラインも同時開催中！（所要時間1時間程度）</p>
                    <p class="text-sm text-gray-600 mb-4">（オンライン開催は、企業説明のみです。）</p>
                    <p class="text-lg mb-2">こんな方におすすめ：</p>
                    <ul class="list-disc list-inside ml-4">
                        <li>介護業界について知りたい</li>
                        <li>武田病院グループのことについて知りたい</li>
                        <li>施設の中を見てみたい</li>
                        <li>どんな働き方をしているのか知りたい</li>
                        <li>どんな人が働いているのか知りたい</li>
                    </ul>
                </div>

                <!-- コースII 詳細 -->
                <div class="card">
                    <h3 class="text-2xl font-bold text-green-700 mb-4">Ⅱ. 介護の仕事・相談援助の仕事<br>お気軽体験1日コース</h3>
                    <p class="mb-4">介護の仕事の流れや認知症の方への対応、相談援助の具体的な内容を体験できます。</p>
                    <p class="font-bold mb-2">タイムスケジュール例（介護体験 Ⅱ-①）</p>
                    <ul class="list-disc list-inside ml-4">
                        <li>10:00 担当者との顔合わせ、今日一日のスケジュール確認</li>
                        <li>10:15 介護現場での注意点など座学にて勉強会</li>
                        <li>11:00 いざ現場体験へ！昼食前の嚥下体操に参加、食事準備など</li>
                        <li>12:30 休憩（食事は準備します！）職員との団欒も♪</li>
                        <li>13:30 実際の介護体験、見学！車椅子の使い方やベッドでの体位変換体験など</li>
                        <li>14:30 担当者からのフィードバック</li>
                        <li>15:00 終了</li>
                    </ul>
                </div>

                <!-- コースIII 詳細 -->
                <div class="card">
                    <h3 class="text-2xl font-bold text-green-700 mb-4">Ⅲ. 介護の仕事・相談援助の仕事<br>ガッツリ体験フリーカスタマイズコース</h3>
                    <p class="mb-4">2種類の介護体験プログラムです。いずれのコースもフリーカスタマイズ型なので、ご希望を伺いながら「あなただけ」のプログラムを作成します！</p>
                    <div class="course-card">
                        <p class="font-bold text-lg mb-2">★介護体験型　定員：1日につき2名</p>
                        <p class="text-gray-700 mb-2">例：日勤×2日、夜勤×1日、休み×1日、日勤×1日のプラン</p>
                        <p class="text-gray-700">ご利用者に寄り添う介護の体験を少し深く知りたい方、24時間、365日違う介護を体験してみませんか？</p>
                    </div>
                    <div class="course-card">
                        <p class="font-bold text-lg mb-2">★相談援助体験型　定員：1日につき1名</p>
                        <p class="text-gray-700 mb-2">例：1、2日目：特養施設相談員のお仕事</p>
                        <p class="text-gray-700 mb-2">　　3日目：通所相談員のお仕事</p>
                        <p class="text-gray-700 mb-2">　　4日目：地域包括支援センターでのお仕事</p>
                        <p class="text-700">　　5日目：特養施設相談員のお仕事とフィードバック</p>
                    </div>
                </div>
            </section>

            <!-- 体験施設一覧セクション -->
            <section id="facilities" class="py-12">
                <h2 class="section-title">体験施設一覧</h2>
                <p class="text-center text-lg mb-8">自宅から、学校から近い場所は？特別養護老人ホームについて知りたい！老人保健施設ってなんだろう？などなど選ぶ理由は様々でOK!</p>
                <div class="facility-grid">
                    <!-- 各施設のカードから画像タグを削除 -->
                    <div class="facility-card">
                        <h4 class="font-bold text-lg text-gray-800">特別養護老人ホームヴィラ稲荷山</h4>
                        <p class="text-sm text-gray-600">（京都市伏見区）</p>
                        <p class="text-sm text-green-700">Ⅰ・Ⅱ①②・Ⅲ対応</p>
                    </div>
                    <div class="facility-card">
                        <h4 class="font-bold text-lg text-gray-800">老人保健施設白寿</h4>
                        <p class="text-sm text-gray-600">（京都市伏見区）</p>
                        <p class="text-sm text-green-700">Ⅰ・Ⅱ①②・Ⅲ対応</p>
                    </div>
                    <div class="facility-card">
                        <h4 class="font-bold text-lg text-gray-800">特別養護老人ホームヴィラ山科</h4>
                        <p class="text-sm text-gray-600">（京都市山科区）</p>
                        <p class="text-sm text-green-700">Ⅰ・Ⅱ①②・Ⅲ対応</p>
                    </div>
                    <div class="facility-card">
                        <h4 class="font-bold text-lg text-gray-800">老人保健施設いわやの里</h4>
                        <p class="text-sm text-gray-600">（京都市山科区）</p>
                        <p class="text-sm text-green-700">Ⅰ・Ⅱ①②・Ⅲ対応</p>
                    </div>
                    <div class="facility-card">
                        <h4 class="font-bold text-lg text-gray-800">京都認知症総合センター</h4>
                        <p class="text-sm text-gray-600">（京都府宇治市）</p>
                        <p class="text-sm text-green-700">Ⅰ・Ⅱ①②・Ⅲ対応</p>
                    </div>
                    <div class="facility-card">
                        <h4 class="font-bold text-lg text-gray-800">特別養護老人ホーム加茂の里</h4>
                        <p class="text-sm text-gray-600">（京都府木津川市）</p>
                        <p class="text-sm text-green-700">Ⅰ・Ⅱ①対応</p>
                    </div>
                    <div class="facility-card">
                        <h4 class="font-bold text-lg text-gray-800">有料老人ホームあいらの杜宇治五ケ庄</h4>
                        <p class="text-sm text-gray-600">（京都府宇治市）</p>
                        <p class="text-sm text-green-700">Ⅱ①対応</p>
                    </div>
                    <div class="facility-card">
                        <h4 class="font-bold text-lg text-gray-800">城陽市立東部デイサービスセンター</h4>
                        <p class="text-sm text-gray-600">（京都府城陽市）</p>
                        <p class="text-sm text-green-700">Ⅱ①対応</p>
                    </div>
                    <div class="facility-card">
                        <h4 class="font-bold text-lg text-gray-800">グループホーム鳳凰槇島</h4>
                        <p class="text-sm text-gray-600">（京都府宇治市）</p>
                        <p class="text-sm text-green-700">Ⅰ・Ⅱ①対応</p>
                    </div>
                    <!-- その他の施設 -->
                    <div class="facility-card">
                        <h4 class="font-bold text-lg text-gray-800">木津屋橋介護医療院</h4>
                        <p class="text-sm text-gray-600">（京都市下京区）</p>
                        <p class="text-sm text-green-700">Ⅱ①対応</p>
                    </div>
                    <div class="facility-card">
                        <h4 class="font-bold text-lg text-gray-800">京都市下京中部地域包括支援センター</h4>
                        <p class="text-sm text-gray-600">（京都市下京区）</p>
                        <p class="text-sm text-green-700">Ⅱ②対応</p>
                    </div>
                </div>
                <p class="text-center text-lg mt-8 text-gray-700">※体験できる施設表示</p>
                <ul class="list-disc list-inside text-left mx-auto w-fit">
                    <li>Ⅰ　…オープンカンパニー</li>
                    <li>Ⅱ①…介護1日体験</li>
                    <li>Ⅱ②…相談援助1日体験</li>
                    <li>Ⅲ　…体験フリーカスタマイズ</li>
                </ul>
            </section>

            <!-- お問い合わせ・エントリーセクション -->
            <section id="contact" class="py-12">
                <h2 class="section-title">お問い合わせ・エントリー</h2>
                <div class="contact-info card">
                    <p class="text-xl font-bold mb-4">エントリーお待ちしています！</p>
                    <p class="text-lg mb-2">登録いただいたLINEに、質問はもちろん、エントリーに関することでも何でもコメントOK！お気軽にお問い合わせください！</p>
                    <button onclick="showApplicationForm()" class="btn-primary block mx-auto mt-4 mb-8">今すぐエントリー！</button>
                    <div class="mt-8">
                        <p class="text-lg font-bold">武田病院グループ本部福祉介護部</p>
                        <p class="text-lg font-bold">インターンシップ担当　小野　智子</p>
                        <p class="text-lg font-bold">携帯：080-3100-2234</p>
                    </div>
                </div>
            </section>
        </main>

        <!-- フッターセクション -->
        <footer class="bg-gray-800 text-white text-center py-6 mt-12 rounded-t-2xl">
            <p>&copy; 2025 武田病院グループ. All rights reserved.</p>
        </footer>
    </div> <!-- /#event-page-content -->

    <div id="form-page-content" style="display: none;">
        <!-- インターンシップ申込フォームの内容をここに配置 -->
        <div class="container">
            <section id="internship-form-section" class="internship-form-section">
                <h2>インターンシップ お申込みフォーム</h2>
                <p>下記フォームに必要事項をご記入の上、送信してください。</p>
                <form class="internship-form" id="internshipForm">
                    <div class="form-group">
                        <label for="name">お名前 <span class="required-star">*</span></label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="kana">フリガナ <span class="required-star">*</span></label>
                        <input type="text" id="kana" name="kana" placeholder="例: ヤマダ タロウ" required>
                    </div>
                    <div class="form-group">
                        <label for="email">メールアドレス <span class="required-star">*</span></label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">電話番号 <span class="required-star">*</span></label>
                        <input type="tel" id="phone" name="phone" placeholder="例: 090-1234-5678" required>
                    </div>
                    <!-- インターンを希望する事業所 -->
                    <div class="form-group">
                        <label for="desired-facility">インターンを希望する事業所 <span class="required-star">*</span></label>
                        <select id="desired-facility" name="desired-facility" required>
                            <option value="">選択してください</option>
                            <option value="special-nursing-home-inariyama">特別養護老人ホームヴィラ稲荷山</option>
                            <option value="special-nursing-home-yamashina">特別養護老人ホームヴィラ山科</option>
                            <option value="kyoto-dementia-center">京都認知症総合センター</option>
                            <option value="special-nursing-home-kamonosato">特別養護老人ホーム加茂の里</option>
                            <option value="nursing-home-hakuju">老人保健施設白寿</option>
                            <option value="nursing-home-iwayanosato">老人保健施設いわやの里</option>
                            <option value="joyo-east-day-service">城陽市立東部デイサービスセンター</option>
                            <option value="yuryo-rojin-home-ujigokasho">有料老人ホームあいらの杜宇治五ケ庄</option> <!-- 追加 -->
                            <option value="group-home-houou-makishima">グループホーム鳳凰槇島</option> <!-- 追加 -->
                            <option value="kizuya-bashi-kaigo-iryoin">木津屋橋介護医療院</option> <!-- 追加 -->
                            <option value="kyoto-shimogyo-chubu-houkatsu-shien-center">京都市下京中部地域包括支援センター</option> <!-- 追加 -->
                            <option value="other-facility">その他（備考欄に記入）</option>
                        </select>
                    </div>
                    <!-- 希望するインターンを追加 -->
                    <div class="form-group">
                        <label for="desired-role">希望するインターン <span class="required-star">*</span></label>
                        <select id="desired-role" name="desired-role" required>
                            <option value="">選択してください</option>
                            <option value="facility-tour-and-info-session">施設見学+企業説明</option>
                            <option value="care-work-experience">介護業務体験</option>
                            <option value="consultation-support-experience">相談援助体験</option>
                            <option value="other-role">その他（備考欄に記入）</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="school-name">学校名・学部 <span class="required-star">*</span></label>
                        <input type="text" id="school-name" name="school-name" required>
                    </div>
                    <!-- 期間 -->
                    <div class="form-group">
                        <label for="internship-duration">期間 <span class="required-star">*</span></label>
                        <select id="internship-duration" name="internship-duration" required>
                            <option value="">選択してください</option>
                            <option value="1-day">1日</option>
                            <option value="2-days">2日</option>
                            <option value="3-days">3日</option>
                            <option value="4-days">4日</option>
                            <option value="5-days">5日</option>
                            <option value="other-duration">その他（備考欄に記入）</option>
                        </select>
                    </div>
                    <!-- 参加希望日（第1希望期間） -->
                    <div class="form-group">
                        <label for="desired-date-1-from">第1希望期間 <span class="required-star">*</span></label>
                        <div class="date-range-group" style="display: flex; gap: 10px; align-items: center;">
                            <input type="date" id="desired-date-1-from" name="desired-date-1-from" required>
                            <span>〜</span>
                            <input type="date" id="desired-date-1-to" name="desired-date-1-to" required>
                        </div>
                    </div>
                    <!-- 参加希望日（第2希望期間） -->
                    <div class="form-group">
                        <label for="desired-date-2-from">第2希望期間</label>
                        <div class="date-range-group" style="display: flex; gap: 10px; align-items: center;">
                            <input type="date" id="desired-date-2-from" name="desired-date-2-from">
                            <span>〜</span>
                            <input type="date" id="desired-date-2-to" name="desired-date-2-to">
                        </div>
                    </div>
                    <!-- 参加希望日（第3希望期間） -->
                    <div class="form-group">
                        <label for="desired-date-3-from">第3希望期間</label>
                        <div class="date-range-group" style="display: flex; gap: 10px; align-items: center;">
                            <input type="date" id="desired-date-3-from" name="desired-date-3-from">
                            <span>〜</span>
                            <input type="date" id="desired-date-3-to" name="desired-date-3-to">
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="message">その他ご質問・メッセージ</label>
                        <textarea id="message" name="message" rows="5"></textarea>
                    </div>
                    <button type="submit" class="btn-submit-form">上記内容で申し込む</button>
                    <button type="button" onclick="showEventPage()" class="btn-secondary block mx-auto mt-4">イベントページに戻る</button>
                </form>
            </section>
        </div>
        <!-- Confirmation Modal (フォームページ内で共通) -->
        <div id="confirmationModal" class="modal-overlay">
            <div class="modal-content">
                <h3>お申込み内容のご確認</h3>
                <p>下記の内容でよろしければ「送信する」ボタンを押してください。</p>
                <div class="confirmation-details" id="confirmationDetails">
                    <!-- Confirmation details will be inserted here by JavaScript -->
                </div>
                <div class="modal-actions">
                    <button type="button" class="modal-button btn-edit" id="editButton">修正する</button>
                    <button type="button" class="modal-button btn-confirm-submit" id="confirmSubmitButton">送信する</button>
                </div>
            </div>
        </div>
    </div> <!-- /#form-page-content -->

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const eventPageContent = document.getElementById('event-page-content');
            const formPageContent = document.getElementById('form-page-content');
            const internshipForm = document.getElementById('internshipForm');
            const confirmationModal = document.getElementById('confirmationModal');
            const confirmationDetails = document.getElementById('confirmationDetails');
            const editButton = document.getElementById('editButton');
            const confirmSubmitButton = document.getElementById('confirmSubmitButton');

            // フォームから取得するデータのラベルマッピング
            const fieldLabels = {
                'name': 'お名前',
                'kana': 'フリガナ',
                'email': 'メールアドレス',
                'phone': '電話番号',
                'desired-facility': 'インターン希望事業所',
                'desired-role': '希望するインターン',
                'school-name': '学校名・学部',
                'internship-duration': '期間',
                'message': 'その他ご質問・メッセージ'
            };

            // イベントページを表示する関数
            window.showEventPage = function() {
                if (eventPageContent && formPageContent) {
                    eventPageContent.style.display = 'block';
                    formPageContent.style.display = 'none';
                    window.scrollTo(0, 0); // ページトップに戻る
                }
            }

            // 申込フォームを表示する関数
            window.showApplicationForm = function() {
                if (eventPageContent && formPageContent) {
                    eventPageContent.style.display = 'none';
                    formPageContent.style.display = 'block';
                    window.scrollTo(0, 0); // ページトップに戻る
                }
            }

            // 初回表示はイベントページ
            showEventPage();

            if (internshipForm) {
                // フォームの送信（確認画面表示）
                internshipForm.addEventListener('submit', async function(event) {
                    event.preventDefault(); // フォームのデフォルト送信をキャンセル

                    // フォームの入力値検証
                    if (!internshipForm.checkValidity()) {
                        internshipForm.reportValidity(); // ブラウザ標準のバリデーションメッセージを表示
                        return; // 送信処理を中断
                    }

                    const form = event.target;
                    const formData = new FormData(form);
                    const data = {}; // このdataオブジェクトに日本語のテキストを格納する

                    // フォームデータを取得し、dataオブジェクトに日本語テキストを格納
                    for (let [key, value] of formData.entries()) {
                        if (key === 'desired-facility' || key === 'desired-role' || key === 'internship-duration') {
                            const selectElement = form.querySelector(`#${key}`);
                            // selectボックスの表示テキスト（日本語）を取得
                            data[key] = selectElement && selectElement.options[selectElement.selectedIndex] ? selectElement.options[selectElement.selectedIndex].text : value;
                        } else {
                            data[key] = value; // その他のフィールドはそのままの値
                        }
                    }
                    
                    // 確認画面用のHTMLを生成 (dataオブジェクトから日本語テキストを使用)
                    let detailsHtml = '';
                    for (let key in data) { // dataオブジェクトを直接ループ
                        // 希望期間の from/to は個別に確認画面に表示しないようにスキップ
                        if (key.startsWith('desired-date-') && (key.endsWith('-from') || key.endsWith('-to'))) {
                             continue;
                        }

                        // 確認画面表示用のHTML生成
                        if (fieldLabels[key]) {
                            detailsHtml += `
                                <div class="confirmation-detail-item">
                                    <span class="confirmation-detail-label">${fieldLabels[key]}</span>
                                    <span class="confirmation-detail-value">${data[key] || '未入力'}</span>
                                </div>
                            `;
                        }
                    }

                    // 希望期間を個別にまとめて表示するための追加処理 (dataオブジェクトから値を使用)
                    for (let i = 1; i <= 3; i++) {
                        const fromKey = `desired-date-${i}-from`;
                        const toKey = `desired-date-${i}-to`;
                        const fromValue = data[fromKey] || ''; // dataオブジェクトから取得
                        const toValue = data[toKey] || '';     // dataオブジェクトから取得

                        // 両方とも空の場合は表示しない
                        if (fromValue || toValue) {
                            detailsHtml += `
                                <div class="confirmation-detail-item">
                                    <span class="confirmation-detail-label">第${i}希望期間</span>
                                    <span class="confirmation-detail-value">${fromValue || '未入力'} 〜 ${toValue || '未入力'}</span>
                                </div>
                            `;
                        }
                    }

                    confirmationDetails.innerHTML = detailsHtml;
                    confirmationModal.classList.add('active'); // モーダルを表示
                });

                // 確認画面の「修正する」ボタン
                editButton.addEventListener('click', function() {
                    confirmationModal.classList.remove('active'); // モーダルを非表示
                });

                // 確認画面の「送信する」ボタン (GASへのデータ送信)
                confirmSubmitButton.addEventListener('click', async function() {
                    confirmationModal.classList.remove('active'); // 送信後はモーダルを閉じる
                    
                    const form = internshipForm; // フォームの参照を再利用
                    const formData = new FormData(form);
                    const data = {}; // 送信用にも新しいdataオブジェクトを用意し直す

                    // 送信用データも日本語テキストで構成
                    for (let [key, value] of formData.entries()) {
                        if (key === 'desired-facility' || key === 'desired-role' || key === 'internship-duration') {
                            const selectElement = form.querySelector(`#${key}`);
                            data[key] = selectElement && selectElement.options[selectElement.selectedIndex] ? selectElement.options[selectElement.selectedIndex].text : value;
                        } else {
                            data[key] = value;
                        }
                    }
                    
                    // Google Apps ScriptのウェブアプリURLをここに設定
                    // ★★★ ここを、Apps Scriptをデプロイした後に得られるURLに置き換えてください ★★★
                    // 例: "https://script.google.com/macros/s/AKfycbzJ93pIIJdU0M_LWZ-tlWhT7qDsrNGBAKxOINYQQIMU3-nlSZYIZWToP6GZJJim2JxZ/exec"
                    const appsScriptUrl = "https://script.google.com/macros/s/AKfycbxHL1QsZkb9ZEcIH2y7f0Frk5mPLXeo4_XzQ7iWQFElt8iA7V_xufUzgRxLN_mHS9U/exec"; // この部分を置き換える必要があります

                    // URLがプレースホルダーのままではないか確認し、エラーを出す
                    if (appsScriptUrl === "YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE" || !appsScriptUrl.startsWith("https://script.google.com/macros/s/")) {
                        console.error("エラー: Google Apps ScriptのURLが設定されていません。コード内の 'YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE' を実際のURLに置き換えてください。");
                        alert("設定エラー: お申込みを送信できませんでした。開発者にお問い合わせください。");
                        return; // 送信処理を中断
                    }

                    try {
                        // データ送信中はユーザーに待機メッセージを表示することも検討
                        // 例: alert('送信中です。しばらくお待ちください...');

                        const response = await fetch(appsScriptUrl, {
                            method: 'POST',
                            mode: 'no-cors', // CORSエラーを避けるため（ただし正確なレスポンスは受け取れない）
                            headers: {
                                'Content-Type': 'application/json; charset=UTF-8', // 文字コードを明示的に指定
                            },
                            body: JSON.stringify(data), // 日本語テキストを含むdataオブジェクトを送信
                        });

                        console.log('Form submission attempted. Check Google Sheet.');
                        alert('お申込みありがとうございます。内容を確認後、担当者よりご連絡いたします。'); // ユーザーへのフィードバック
                        form.reset(); // フォームをリセット
                        showEventPage(); // 送信後、イベントページに戻る

                    } catch (error) {
                        console.error('Error submitting form:', error);
                        alert('お申込み中にエラーが発生しました。もう一度お試しいただくか、直接お問い合わせください。');
                    }
                });

            } else {
                console.error("エラー: 'internshipForm' 要素が見つかりません。HTMLフォームにid='internshipForm'があることを確認してください。");
            }
        });
    </script>
</body>
</html>

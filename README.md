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
            box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.05);
            padding: 1.5rem;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 250px;
        }
        /* Style for course support text inside facility card (align left) */
        .facility-card .course-support-text {
            text-align: left; /* Align left */
            width: 100%; /* Occupy full width of parent */
            padding-left: 0; /* Reset padding */
            padding-right: 0; /* Reset padding */
            color: #343a40; /* Set parent p tag to normal (black) color, adjust span for specific color */
        }
        /* Style for "対応可能なインターンシップ" heading (orange) */
        .facility-card .course-support-text .orange-text {
            color: rgb(234, 88, 12); /* Change to orange */
            font-weight: bold; /* Bold */
            display: block; /* Line break */
            margin-bottom: 0.25rem; /* Spacing from next item */
        }
        /* Style for each course item (e.g., "・オープンカンパニー") */
        .facility-card .course-support-text span {
            display: block; /* Line break for each course */
            margin-bottom: 0.25rem; /* Spacing between items */
            color: #28a745; /* Change to green */
        }
        .facility-card .course-support-text span:last-child {
            margin-bottom: 0; /* Remove spacing from last item */
        }

        /* Access information style */
        .facility-card .access-info {
            text-align: left;
            width: 100%;
            margin-top: 0.75rem;
            font-size: 0.9rem;
            color: #6c757d; /* Overall text color for access info (gray) */
        }
        .facility-card .access-info a {
            color: #007bff; /* Change to blue */
            font-weight: bold; /* Bold */
            text-decoration: underline;
        }
        .facility-card .access-info a:hover {
            color: #0056b3;
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

        /* Form embed style */
        .form-page-container {
            max-width: 700px;
            margin: 0 auto;
            padding: 0 20px;
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
        /* Checkbox specific styling */
        .checkbox-group {
            display: flex;
            flex-direction: column;
        }
        .checkbox-group label {
            font-weight: normal; /* Override bold for individual checkbox labels */
            margin-bottom: 0; /* Adjust spacing */
            display: flex; /* Align checkbox and text */
            align-items: center;
        }
        .checkbox-group input[type="checkbox"] {
            width: auto; /* Allow checkbox to take its natural width */
            margin-right: 0.5rem; /* Space between checkbox and label */
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
        .btn-submit-form { /* Form submit button style */
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
            /* Changed box-shadow color to a neutral gray */
            box-shadow: 0 4px 15px rgba(0,0,0,0.2); 
        }
        .btn-submit-form:hover {
            background-color: #218838;
            transform: translateY(-2px);
        }
        
        /* Confirmation Modal Styles (common for form page) */
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
            box-shadow: 0 44px 15px rgba(40,167,69,0.4);
        }
        .modal-button.btn-confirm-submit:hover {
            background-color: #218838;
            transform: translateY(-2px);
        }
    </style>
</head>
<body>
    <div id="event-page-content">
        <!-- Header section -->
        <header class="header-bg">
            <div class="container">
                <!-- Replace Takeda Hospital Group logo with text -->
                <h2 class="text-logo">武田病院グループ本部福祉介護部</h2>
                <h1 class="text-4xl md:text-5xl font-bold mb-4">2025年夏期インターンシッププログラム</h1>
                <p class="text-2xl md:text-3xl font-semibold mb-6">「フクシノイリグチ」<br>見て聞いて触れる1日業界研究</p>
                <div class="highlight-box mx-auto">
                    <p class="text-xl leading-relaxed text-black">
                        <span class="font-bold">当グループのインターンシップは</span><br>
                        <span class="font-bold text-green-600">「人に感謝される仕事のやりがい」</span><br>
                        <span class="font-bold text-green-600">「エッセンシャルワークの本質」</span><br>
                        <span class="font-bold text-green-600">「介護の仕事に対するマイナスイメージの払拭」</span><br>
                        <span class="font-bold">これらを実感していただけることをお約束します！</span>
                    </p>
                </div>
                <button id="entryButton" class="btn-primary block mx-auto mt-8">エントリーはこちら</button>
            </div>
        </header>

        <main class="container">
            <!-- Course Introduction section -->
            <section id="courses" class="py-12">
                <h2 class="section-title">コース紹介</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <!-- Course I -->
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

                    <!-- Course II -->
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

                    <!-- Course III -->
                    <div class="card">
                        <h3 class="course-title">Ⅲ. 介護の仕事・相談援助の仕事<br>ガッツリ体験フリーカスタマイズコース</h3>
                        <p class="text-gray-700 mb-4">あなたの希望に合わせて、介護や相談援助の仕事を深く,自由に体験できるプログラムです。</p>
                        <ul class="feature-list">
                            <li>日程：令和7年7月～9月</li>
                            <li>定員：介護体験型 1日につき2名、相談援助体験型 1日につき1名</li>
                            <li>時間：10:00～15:00（昼食付）</li>
                        </ul>
                        <p class="text-gray-600 mt-4">24時間365日異なる介護や、多様な相談援助の仕事を体験できます。</p>
                    </div>
                </div>
            </section>

            <!-- Course details section -->
            <section id="course-details" class="py-12">
                <h2 class="section-title">各コース詳細</h2>
                <!-- I. Open Company (Company Info Session & Facility Tour) -->
                <div class="card">
                    <h3 class="text-2xl font-bold text-green-700 mb-4">Ⅰ. オープンカンパニー（企業説明会・施設見学会）</h3>
                    <p class="mb-4">介護業界、武田病院グループ、働き方、職場の雰囲気について知りたいというあなたの疑問を解消するセミナーです。<br>
                    オンラインも同時開催中！（所要時間1時間程度）<br>
                    （オンライン開催は、企業説明のみです。）</p>
                    <p class="text-lg mb-2">こんな方におすすめ：</p>
                    <ul class="list-disc list-inside ml-4 text-left">
                        <li>介護業界について知りたい</li>
                        <li>武田病院グループのことについて知りたい</li>
                        <li>施設の中を見てみたい</li>
                        <li>どんな働き方をしているのか知りたい</li>
                        <li>どんな人が働いているのか知りたい</li>
                    </ul>
                </div>

                <!-- II. Care Work / Consultation Support Experience 1-Day Course -->
                <div class="card">
                    <h3 class="text-2xl font-bold text-green-700 mb-4">Ⅱ. 介護の仕事・相談援助の仕事<br>お気軽体験1日コース</h3>
                    <p class="mb-4">介護の仕事の流れや認知症の方への対応、相談援助の具体的な内容を体験できます。<br>
                    <span class="font-bold">タイムスケジュール例：</span><br>
                    10:00 担当者との顔合わせ、今日一日のスケジュール確認<br>
                    10:15 介護現場での注意点など座学にて勉強会<br>
                    11:00 いざ現場体験へ！昼食前の嚥下体操に参加、食事準備など<br>
                    12:30 休憩（食事は準備します！）職員との団欒も♪<br>
                    13:30 実際の介護体験、見学！車椅子の使い方やベッドでの体位変換体験など<br>
                    14:30 担当者からのフィードバック<br>
                    15:00 終了<br>
                    ※スケジュールはカスタマイズ可能です</p>
                </div>

                <!-- III. Intensive Experience Free Customization Course -->
                <div class="card">
                    <h3 class="text-2xl font-bold text-green-700 mb-4">Ⅲ. 介護の仕事・相談援助の仕事<br>ガッツリ体験フリーカスタマイズコース</h3>
                    <p class="mb-4">2種類の介護体験プログラムです。ご希望を伺いながら「あなただけ」のプログラムを作成します！</p>
                    <p class="font-bold text-lg mb-2">★介護体験型　定員：1日につき2名</p>
                    <p class="text-gray-700 mb-2">例：日勤×2日、夜勤×1日、休み×1日、日勤×1日のプラン<br>
                    ご利用者に寄り添う介護の体験を少し深く知りたい方、24時間、365日違う介護を体験してみませんか？</p>
                    <p class="font-bold text-lg mt-4 mb-2">★相談援助体験型　定員：1日につき1名</p>
                    <p class="text-gray-700">例：1、2日目：特養施設相談員のお仕事<br>
                    　　3日目：通所相談員のお仕事<br>
                    　　4日目：地域包括支援センターでのお仕事<br>
                    　　5日目：特養施設相談員のお仕事とフィードバック</p>
                </div>
            </section>


            <section id="facilities" class="py-12">
                <h2 class="section-title">体験施設一覧</h2>
                <p class="text-center text-lg mb-8">自宅から、学校から近い場所は？特別養護老人ホームについて知りたい！老人保健施設ってなんだろう？などなど選ぶ理由は様々でOK!</p>
                <div class="facility-grid">
                    <!-- Corrected course notation for each facility card -->
                    <div class="facility-card">
                        <!-- Image of Villa Inariyama -->
                        <img src="https://i.imgur.com/epI7drI.jpeg" alt="特別養護老人ホームヴィラ稲荷山 画像" class="w-full h-48 object-cover rounded-t-lg mb-4" onerror="this.onerror=null;this.src='https://placehold.co/300x200/cccccc/ffffff?text=画像+読み込み失敗';console.error('画像読み込み失敗: 特別養護老人ホームヴィラ稲荷山。Imgurの直接リンクが正しいか、Imgurの共有設定を確認してください。');">
                        <h4 class="font-bold text-lg text-gray-800">特別養護老人ホームヴィラ稲荷山</h4>
                        <p class="text-sm text-gray-600">（京都市伏見区）</p>
                        <p class="text-sm course-support-text">
                            <span class="orange-text">対応可能なインターンシップ</span>
                            <span class="text-green-600">・オープンカンパニー</span>
                            <span class="text-green-600">・介護1日体験</span>
                            <span class="text-green-600">・相談援助1日体験</span>
                            <span class="text-green-600">・体験フリーカスタマイズ</span>
                        </p>
                        <p class="text-sm text-gray-600 mt-2 access-info">
                            <span class="font-bold">アクセス：</span><br>
                            京阪本線「鳥羽街道」下車、徒歩5分<br>
                            ＪＲ奈良線「東福寺」または「稲荷」下車、徒歩15分<br>
                            <a href="https://www.google.com/maps/place/%E7%89%B9%E5%88%A5%E9%A4%8A%E8%AD%B7%E8%80%81%E4%BA%BA%E3%83%9B%E3%83%BC%E3%83%A0+%E3%83%B4%E3%82%A3%E3%83%A9%E7%A8%B2%E8%8D%B7%E5%B1%B1/@34.973428,135.773016,15z/data=!4m6!3m5!1s0x60010f38d335bbc7:0x95628922e797d8e3!8m2!3d34.9734284!4d135.7730161!16s%2Fg%2F1tfjfflc?hl=ja&entry=ttu&g_ep=EgoyMDI1MDYxNy4wIKXMDSoASAFQAw%3D%3D" target="_blank" class="text-blue-600 font-bold">詳細はこちら</a>
                        </p>
                    </div>
                    <div class="facility-card">
                        <img src="https://i.imgur.com/KmTP9pI.png" alt="老人保健施設白寿 画像" class="w-full h-48 object-cover rounded-t-lg mb-4" onerror="this.onerror=null;this.src='https://placehold.co/300x200/cccccc/ffffff?text=画像+読み込み失敗';console.error('画像読み込み失敗: 老人保健施設白寿。Imgurの直接リンクが正しいか、Imgurの共有設定を確認してください。');">
                        <h4 class="font-bold text-lg text-gray-800">老人保健施設白寿</h4>
                        <p class="text-sm text-gray-600">（京都市伏見区）</p>
                        <p class="text-sm course-support-text">
                            <span class="orange-text">対応可能なインターンシップ</span>
                            <span class="text-green-600">・オープンカンパニー</span><span class="text-green-600">・介護1日体験</span><span class="text-green-600">・相談援助1日体験</span><span class="text-green-600">・体験フリーカスタマイズ</span>
                        </p>
                        <p class="text-sm text-gray-600 mt-2 access-info">
                            <span class="font-bold">アクセス：</span><br>
                            京都市営地下鉄東西線「石田駅」下車 徒歩5分<br>
                            <a href="https://www.google.com/maps?ll=34.938771,135.804961&z=16&t=m&hl=ja&gl=US&mapclient=embed&q=%E3%80%92601-1434+%E4%BA%AC%E9%83%BD%E5%BA%9C%E4%BA%AC%E9%83%BD%E5%B8%82%E4%BC%8F%E8%A6%8B%E5%8C%BA%E7%9F%B3%E7%94%B0%E6%A3%AE%E5%8D%97%E7%94%BA%EF%BC%99+%E6%97%A5%E6%9C%AC" target="_blank" class="text-blue-600 font-bold">詳細はこちら</a>
                        </p>
                    </div>
                    <div class="facility-card">
                        <img src="https://i.imgur.com/5FTNIG0.png" alt="特別養護老人ホームヴィラ山科 画像" class="w-full h-48 object-cover rounded-t-lg mb-4" onerror="this.onerror=null;this.src='https://placehold.co/300x200/cccccc/ffffff?text=画像+読み込み失敗';console.error('画像読み込み失敗: 特別養護老人ホームヴィラ山科。Imgurの直接リンクが正しいか、Imgurの共有設定を確認してください。');">
                        <h4 class="font-bold text-lg text-gray-800">特別養護老人ホームヴィラ山科</h4>
                        <p class="text-sm text-gray-600">（京都市山科区）</p>
                        <p class="text-sm course-support-text">
                            <span class="orange-text">対応可能なインターンシップ</span>
                            <span class="text-green-600">・オープンカンパニー</span><span class="text-green-600">・介護1日体験</span><span class="text-green-600">・相談援助1日体験</span><span class="text-green-600">・体験フリーカスタマイズ</span>
                        </p>
                        <p class="text-sm text-gray-600 mt-2 access-info">
                            <span class="font-bold">アクセス：</span><br>
                            地下鉄東西線「椥辻」駅徒歩15分<br>
                            JR「山科」駅から京阪バス26系統大宅行「大宅」停下車徒歩7分<br>
                            <a href="https://www.google.com/maps?ll=34.971131,135.826098&z=15&t=m&hl=ja&gl=JP&mapclient=embed&cid=9465310590999781784" target="_blank" class="text-blue-600 font-bold">詳細はこちら</a>
                        </p>
                    </div>
                    <div class="facility-card">
                        <img src="https://i.imgur.com/q1WNomE.png" alt="老人保健施設いわやの里 画像" class="w-full h-48 object-cover rounded-t-lg mb-4" onerror="this.onerror=null;this.src='https://placehold.co/300x200/cccccc/ffffff?text=画像+読み込み失敗';console.error('画像読み込み失敗: 老人保健施設いわやの里。Imgurの共有設定を確認してください。');">
                        <h4 class="font-bold text-lg text-gray-800">老人保健施設いわやの里</h4>
                        <p class="text-sm text-gray-600">（京都市山科区）</p>
                        <p class="text-sm course-support-text">
                            <span class="orange-text">対応可能なインターンシップ</span>
                            <span class="text-green-600">・オープンカンパニー</span><span class="text-green-600">・介護1日体験</span>
                            <span class="text-green-600">・相談援助1日体験</span><span class="text-green-600">・体験フリーカスタマイズ</span>
                        </p>
                        <p class="text-sm text-gray-600 mt-2 access-info">
                            <span class="font-bold">アクセス：</span><br>
                            京都市営地下鉄東西線「なぎ辻駅」下車徒歩15分<br>
                            京阪バス「京都橘大学」停留所下車徒歩3分<br>
                            <a href="https://www.google.com/maps?ll=34.970768,135.826439&z=15&t=m&hl=ja&gl=JP&mapclient=embed&cid=17053488229120904928" target="_blank" class="text-blue-600 font-bold">詳細はこちら</a>
                        </p>
                    </div>
                    <div class="facility-card">
                        <img src="https://i.imgur.com/5ojwEnj.png" alt="京都認知症総合センター 画像" class="w-full h-48 object-cover rounded-t-lg mb-4" onerror="this.onerror=null;this.src='https://placehold.co/300x200/cccccc/ffffff?text=画像+読み込み失敗';console.error('画像読み込み失敗: 京都認知症総合センター。Imgurの共有設定を確認してください。');">
                        <h4 class="font-bold text-lg text-gray-800">京都認知症総合センター</h4>
                        <p class="text-sm text-gray-600">（京都府宇治市）</p>
                        <p class="text-sm course-support-text">
                            <span class="orange-text">対応可能なインターンシップ</span>
                            <span class="text-green-600">・オープンカンパニー</span><span class="text-green-600">・介護1日体験</span>
                            <span class="text-green-600">・相談援助1日体験</span><span class="text-green-600">・体験フリーカスタマイズ</span>
                        </p>
                        <p class="text-sm text-gray-600 mt-2 access-info">
                            <span class="font-bold">アクセス：</span><br>
                            JR奈良線「宇治駅」から北に約310m<br>
                            <a href="https://www.google.com/maps?ll=34.893037,135.801848&z=13&t=m&hl=ja&gl=JP&mapclient=embed&cid=6422154141261135181" target="_blank" class="text-blue-600 font-bold">詳細はこちら</a>
                        </p>
                    </div>
                    <div class="facility-card">
                        <img src="https://i.imgur.com/YLdOgrW.png" alt="特別養護老人ホーム加茂の里 画像" class="w-full h-48 object-cover rounded-t-lg mb-4" onerror="this.onerror=null;this.src='https://placehold.co/300x200/cccccc/ffffff?text=画像+読み込み失敗';console.error('画像読み込み失敗: 特別養護老人ホーム加茂の里。Imgurの共有設定を確認してください。');">
                        <h4 class="font-bold text-lg text-gray-800">特別養護老人ホーム加茂の里</h4>
                        <p class="text-sm text-gray-600">（京都府木津川市）</p>
                        <p class="text-sm course-support-text">
                            <span class="orange-text">対応可能なインターンシップ</span><br>
                            <span class="text-green-600">・オープンカンパニー</span>
                            <span class="text-green-600">・介護1日体験</span>
                        </p>
                        <p class="text-sm text-gray-600 mt-2 access-info">
                            <span class="font-bold">アクセス：</span><br>
                            JR大和路線「加茂駅」前（徒歩3分）<br>
                            <a href="https://www.google.com/maps?ll=34.754362,135.8718&z=15&t=m&hl=ja&gl=JP&mapclient=embed&cid=15908933367036581542" target="_blank" class="text-blue-600 font-bold">詳細はこちら</a>
                        </p>
                    </div>
                    <div class="facility-card">
                        <img src="https://i.imgur.com/YbosDVu.jpeg" alt="有料老人ホームあいらの杜宇治五ケ庄 画像" class="w-full h-48 object-cover rounded-t-lg mb-4" onerror="this.onerror=null;this.src='https://placehold.co/300x200/cccccc/ffffff?text=画像+読み込み失敗';console.error('画像読み込み失敗: 有料老人ホームあいらの杜宇治五ケ庄。Imgurの共有設定を確認してください。');">
                        <h4 class="font-bold text-lg text-gray-800">有料老人ホームあいらの杜宇治五ケ庄</h4>
                        <p class="text-sm text-gray-600">（京都府宇治市）</p>
                        <p class="text-sm course-support-text">
                            <span class="orange-text">対応可能なインターンシップ</span><br>
                            <span class="text-green-600">・介護1日体験</span>
                        </p>
                        <p class="text-sm text-gray-600 mt-2 access-info">
                            <span class="font-bold">アクセス：</span><br>
                            JR奈良線、京阪宇治線「黄檗駅」から南西に徒歩15分<br>
                            京阪電車「三室戸駅」から北西に徒歩15分<br>
                            <a href="https://www.google.com/maps?ll=34.906845,135.798297,15z/data=!4m6!3m5!1s0x600111b7a43af13f:0xf90536d85377c501!8m2!3d34.906845!4d135.7982968!16s%2Fg%2F11bxfg78r4?hl=ja&entry=ttu&g_ep=EgoyMDI1MDYxNy4wIKXMDSoASAFQAw%3D%3D" target="_blank" class="text-blue-600 font-bold">詳細はこちら</a>
                        </p>
                    </div>
                    <div class="facility-card">
                        <img src="https://i.imgur.com/H94mVyo.jpeg" alt="城陽市立東部デイサービスセンター 画像" class="w-full h-48 object-cover rounded-t-lg mb-4" onerror="this.onerror=null;this.src='https://placehold.co/300x200/cccccc/ffffff?text=画像+読み込み失敗';console.error('画像読み込み失敗: 城陽市立東部デイサービスセンター。Imgurの共有設定を確認してください。');">
                        <h4 class="font-bold text-lg text-gray-800">城陽市立東部デイサービスセンター</h4>
                        <p class="text-sm text-gray-600">（京都府城陽市）</p>
                        <p class="text-sm course-support-text">
                            <span class="orange-text">対応可能なインターンシップ</span><br>
                            <span class="text-green-600">・介護1日体験</span>
                        </p>
                        <p class="text-sm text-gray-600 mt-2 access-info">
                            <span class="font-bold">アクセス：</span><br>
                            近鉄京都線「久津川駅」下車徒歩8分<br>
                            JR奈良線「城陽駅」下車徒歩15分<br>
                            <a href="https://www.google.com/maps?ll=34.861938,135.778045&z=15&t=m&hl=ja&gl=JP&mapclient=embed&cid=4696354945431619474" target="_blank" class="text-blue-600 font-bold">詳細はこちら</a>
                        </p>
                    </div>
                    <div class="facility-card">
                        <img src="https://i.imgur.com/CLGBYk8.jpeg" alt="グループホーム鳳凰槇島 画像" class="w-full h-48 object-cover rounded-t-lg mb-4" onerror="this.onerror=null;this.src='https://placehold.co/300x200/cccccc/ffffff?text=画像+読み込み失敗';console.error('画像読み込み失敗: グループホーム鳳凰槇島。Imgurの共有設定を確認してください。');">
                        <h4 class="font-bold text-lg text-gray-800">グループホーム鳳凰槇島</h4>
                        <p class="text-sm text-gray-600">（京都府宇治市）</p>
                        <p class="text-sm course-support-text">
                            <span class="orange-text">対応可能なインターンシップ</span><br>
                            <span class="text-green-600">・オープンカンパニー</span><span class="text-green-600">・介護1日体験</span>
                        </p>
                        <p class="text-sm text-gray-600 mt-2 access-info">
                            <span class="font-bold">アクセス：</span><br>
                            近鉄「小倉駅」徒歩20分<br>
                            向島駅 京都京阪バス 系統「１０」「１０Ａ」停留所 槇島コミセン下車 徒歩5分<br>
                            <a href="https://www.google.com/maps?ll=34.905483,135.781991&z=14&t=m&hl=ja&gl=JP&mapclient=embed&cid=7194888715494382893" target="_blank" class="text-blue-600 font-bold">詳細はこちら</a>
                        </p>
                    </div>
                    <!-- Other facilities -->
                    <div class="facility-card">
                        <img src="https://i.imgur.com/7WnQNC7.png" alt="木津屋橋武田病院介護医療院 画像" class="w-full h-48 object-cover rounded-t-lg mb-4" onerror="this.onerror=null;this.src='https://placehold.co/300x200/cccccc/ffffff?text=画像+読み込み失敗';console.error('画像読み込み失敗: 木津屋橋武田病院介護医療院。Imgurの共有設定を確認してください。');">
                        <h4 class="font-bold text-lg text-gray-800">木津屋橋武田病院介護医療院</h4>
                        <p class="text-sm text-gray-600">（京都市下京区）</p>
                        <p class="text-sm course-support-text">
                            <span class="orange-text">対応可能なインターンシップ</span><br>
                            <span class="text-green-600">・介護1日体験</span>
                        </p>
                        <p class="text-sm text-gray-600 mt-2 access-info">
                            <span class="font-bold">アクセス：</span><br>
                            JR京都駅・近鉄京都駅・京都市営地下鉄京都駅から徒歩10分<br>
                            京都市営バス 七条堀川バス停から徒歩3分・下京総合庁舎前から徒歩5分<br>
                            <a href="https://www.google.com/maps/place/%E6%9C%A8%E6%B4%A5%E5%B1%8B%E6%A9%8B%E6%AD%A6%E7%94%B0%E7%97%85%E9%99%A2+%E4%BB%8B%E8%AD%B7%E5%8C%BB%E7%99%82%E9%99%A2/@34.988622,135.753995,15z/data=!4m6!3m5!1s0x600108a7afa97a6b:0xe3481695ae573098!8m2!3d34.9886224!4d135.7539945!16s%2Fg%2F1tk67l8g?hl=ja&entry=ttu&g_ep=EgoyMDI1MDYxNy4wIKXMDSoASAFQAw%3D%3D" target="_blank" class="text-blue-600 font-bold">詳細はこちら</a>
                        </p>
                    </div>
                    <div class="facility-card">
                        <img src="https://i.imgur.com/p2Bmis6.jpeg" alt="京都市下京・中部地域包括支援センター 画像" class="w-full h-48 object-cover rounded-t-lg mb-4" onerror="this.onerror=null;this.src='https://placehold.co/300x200/cccccc/ffffff?text=画像+読み込み失敗';console.error('画像読み込み失敗: 京都市下京・中部地域包括支援センター。Imgurの共有設定を確認してください。');">
                        <h4 class="font-bold text-lg text-gray-800">京都市下京・中部地域包括支援センター</h4>
                        <p class="text-sm text-gray-600">（京都市下京区）</p>
                        <p class="text-sm course-support-text">
                            <span class="orange-text">対応可能なインターンシップ</span><br>
                            <span class="text-green-600">・相談援助1日体験</span>
                        </p>
                        <p class="text-sm text-gray-600 mt-2 access-info">
                            <span class="font-bold">アクセス：</span><br>
                            JR「京都駅」徒歩10分<br>
                            <a href="https://www.google.com/maps?ll=34.987577,135.755123&z=15&t=m&hl=ja&gl=JP&mapclient=embed&cid=1694371115490976876" target="_blank" class="text-blue-600 font-bold">詳細はこちら</a>
                        </p>
                    </div>
                </div>
                <!-- Remove legend section -->
                <ul class="list-disc list-inside text-left mx-auto w-fit" style="display: none;">
                    <li>Ⅰ　…オープンカンパニー</li>
                    <li>Ⅱ①…介護1日体験</li>
                    <li>Ⅱ②…相談援助1日体験</li>
                    <li>Ⅲ　…体験フリーカスタマイズ</li>
                </ul>
            </section>

            <!-- Contact/Entry section -->
            <section id="contact" class="py-12">
                <h2 class="section-title">お問い合わせ・エントリー</h2>
                <div class="contact-info card">
                    <p class="text-xl font-bold mb-4">エントリーお待ちしています！</p>
                    <p class="text-lg mb-2">登録いただいたLINEに、質問はもちろん、エントリーに関することでも何でもコメントOK！お気軽にお問い合わせください！</p>
                    <button id="entryButtonContact" class="btn-primary block mx-auto mt-4 mb-8">今すぐエントリー！</button>
                    <div class="mt-8">
                        <p class="text-lg font-bold">武田病院グループ本部福祉介護部</p>
                        <p class="text-lg font-bold">インターンシップ担当　小野　智子</p>
                        <p class="text-lg font-bold">携帯：080-3100-2234</p>
                    </div>
                </div>
            </section>
        </main>

        <!-- Footer section -->
        <footer class="bg-gray-800 text-white text-center py-6 mt-12 rounded-t-2xl">
            <p>&copy; 2025 武田病院グループ. All rights reserved.</p>
        </footer>
    </div> <!-- /#event-page-content -->

    <div id="form-page-content" style="display: none;">
        <!-- Internship Application Form content goes here -->
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
                    <!-- Desired internship facility -->
                    <div class="form-group">
                        <label for="desired-facility">インターンを希望する事業所 <span class="required-star">*</span></label>
                        <div class="checkbox-group">
                            <label><input type="checkbox" name="desired-facility" value="特別養護老人ホームヴィラ稲荷山">特別養護老人ホームヴィラ稲荷山</label>
                            <label><input type="checkbox" name="desired-facility" value="特別養護老人ホームヴィラ山科">特別養護老人ホームヴィラ山科</label>
                            <label><input type="checkbox" name="desired-facility" value="京都認知症総合センター">京都認知症総合センター</label>
                            <label><input type="checkbox" name="desired-facility" value="特別養護老人ホーム加茂の里">特別養護老人ホーム加茂の里</label>
                            <label><input type="checkbox" name="desired-facility" value="老人保健施設白寿">老人保健施設白寿</label>
                            <label><input type="checkbox" name="desired-facility" value="老人保健施設いわやの里">老人保健施設いわやの里</label>
                            <label><input type="checkbox" name="desired-facility" value="城陽市立東部デイサービスセンター">城陽市立東部デイサービスセンター</label>
                            <label><input type="checkbox" name="desired-facility" value="有料老人ホームあいらの杜宇治五ケ庄">有料老人ホームあいらの杜宇治五ケ庄</label>
                            <label><input type="checkbox" name="desired-facility" value="グループホーム鳳凰槇島">グループホーム鳳凰槇島</label>
                            <label><input type="checkbox" name="desired-facility" value="木津屋橋武田病院介護医療院">木津屋橋武田病院介護医療院</label>
                            <label><input type="checkbox" name="desired-facility" value="京都市下京・中部地域包括支援センター">京都市下京・中部地域包括支援センター</label>
                            <label><input type="checkbox" name="desired-facility" value="体験場所が決められないので相談したい">体験場所が決められないので相談したい</label> <!-- Added option -->
                            <label><input type="checkbox" name="desired-facility" value="その他（備考欄に記入）">その他（備考欄に記入）</label>
                        </div>
                    </div>
                    <!-- Add desired internship -->
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
                    <!-- Period -->
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
                    <!-- Desired participation date (1st preference period) -->
                    <div class="form-group">
                        <label for="desired-date-1-from">第1希望期間 <span class="required-star">*</span></label>
                        <div class="date-range-group" style="display: flex; gap: 10px; align-items: center;">
                            <input type="date" id="desired-date-1-from" name="desired-date-1-from" required>
                            <span>〜</span>
                            <input type="date" id="desired-date-1-to" name="desired-date-1-to" required>
                        </div>
                    </div>
                    <!-- Desired participation date (2nd preference period) -->
                    <div class="form-group">
                        <label for="desired-date-2-from">第2希望期間</label>
                        <div class="date-range-group" style="display: flex; gap: 10px; align-items: center;">
                            <input type="date" id="desired-date-2-from" name="desired-date-2-from">
                            <span>〜</span>
                            <input type="date" id="desired-date-2-to" name="desired-date-2-to">
                        </div>
                    </div>
                    <!-- Desired participation date (3rd preference period) -->
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
                    <button type="button" id="backToEventPageButton" class="btn-secondary block mx-auto mt-4">イベントページに戻る</button>
                </form>
            </section>
        </div>
        <!-- Confirmation Modal (common for form page) -->
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
            // Get elements by ID
            const entryButton = document.getElementById('entryButton');
            const entryButtonContact = document.getElementById('entryButtonContact'); // Button in contact section
            const backToEventPageButton = document.getElementById('backToEventPageButton'); // Back button in form


            // Mapping of form field names to Japanese labels
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

            // Function to display event page
            window.showEventPage = function() {
                if (eventPageContent && formPageContent) {
                    eventPageContent.style.display = 'block';
                    formPageContent.style.display = 'none';
                    window.scrollTo(0, 0); // Scroll to top of page
                }
            }

            // Function to display application form
            window.showApplicationForm = function() {
                if (eventPageContent && formPageContent) {
                    eventPageContent.style.display = 'none';
                    formPageContent.style.display = 'block';
                    window.scrollTo(0, 0); // Scroll to top of page
                }
            }

            // Display event page on initial load
            showEventPage();

            // Assign event listeners
            if (entryButton) {
                entryButton.addEventListener('click', showApplicationForm);
            } else {
                console.error("Error: 'entryButton' element not found.");
            }
            // Assign event listener to button in contact section
            if (entryButtonContact) {
                entryButtonContact.addEventListener('click', showApplicationForm);
            } else {
                console.error("Error: 'entryButtonContact' element not found.");
            }

            if (backToEventPageButton) {
                backToEventPageButton.addEventListener('click', showEventPage);
            } else {
                console.error("Error: 'backToEventPageButton' element not found.");
            }


            if (internshipForm) {
                // Form submission (display confirmation screen)
                internshipForm.addEventListener('submit', async function(event) {
                    event.preventDefault(); // Cancel default form submission

                    // Validate form input
                    const desiredFacilityCheckboxes = document.querySelectorAll('input[name="desired-facility"]');
                    let isFacilityChecked = false;
                    for(const checkbox of desiredFacilityCheckboxes) {
                        if (checkbox.checked) {
                            isFacilityChecked = true;
                            break;
                        }
                    }

                    if (!isFacilityChecked) {
                        alert("インターンを希望する事業所を1つ以上選択してください。");
                        return;
                    }

                    if (!internshipForm.checkValidity()) {
                        internshipForm.reportValidity(); // Display browser's default validation message
                        return; // Stop submission process
                    }

                    const form = event.target;
                    const data = {}; // Object to store Japanese text for confirmation and email

                    // Populate 'data' object for confirmation modal and email body display
                    data['name'] = form.elements['name'].value;
                    data['kana'] = form.elements['kana'].value;
                    data['email'] = form.elements['email'].value;
                    data['phone'] = form.elements['phone'].value;

                    // Handle desired-facility from checked checkboxes
                    const selectedFacilitiesForDisplay = Array.from(document.querySelectorAll('input[name="desired-facility"]:checked'))
                        .map(cb => cb.value);
                    data['desired-facility'] = selectedFacilitiesForDisplay.join(', ');

                    // Handle desired-role (select dropdown) - get displayed text
                    const desiredRoleSelect = form.elements['desired-role'];
                    data['desired-role'] = desiredRoleSelect.selectedOptions[0].text;

                    // Handle internship-duration (select dropdown) - get displayed text
                    const internshipDurationSelect = form.elements['internship-duration'];
                    data['internship-duration'] = internshipDurationSelect.selectedOptions[0].text;

                    data['desired-date-1-from'] = form.elements['desired-date-1-from'].value;
                    data['desired-date-1-to'] = form.elements['desired-date-1-to'].value;
                    data['desired-date-2-from'] = form.elements['desired-date-2-from'].value;
                    data['desired-date-2-to'] = form.elements['desired-date-2-to'].value;
                    data['desired-date-3-from'] = form.elements['desired-date-3-from'].value;
                    data['desired-date-3-to'] = form.elements['desired-date-3-to'].value;
                    data['message'] = form.elements['message'].value;
                    
                    // Generate HTML for confirmation screen (use Japanese text from data object)
                    let detailsHtml = '';
                    for (let key in data) { // Loop directly through data object
                        // Skip from/to of desired period as they are displayed separately in confirmation screen
                        if (key.startsWith('desired-date-') && (key.endsWith('-from') || key.endsWith('-to'))) {
                             continue;
                        }

                        // Generate HTML for confirmation screen display
                        if (fieldLabels[key]) {
                            detailsHtml += `
                                <div class="confirmation-detail-item">
                                    <span class="confirmation-detail-label">${fieldLabels[key]}</span>
                                    <span class="confirmation-detail-value">${data[key] || '未入力'}</span>
                                </div>
                            `;
                        }
                    }

                    // Additional processing to display desired period together (use values from data object)
                    for (let i = 1; i <= 3; i++) {
                        const fromKey = `desired-date-${i}-from`;
                        const toKey = `desired-date-${i}-to`;
                        const fromValue = data[fromKey] || ''; // Get from data object
                        const toValue = data[toKey] || '';     // Get from data object

                        // Do not display if both are empty
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
                    confirmationModal.classList.add('active'); // Display modal
                });

                // "Revise" button on confirmation screen
                editButton.addEventListener('click', function() {
                    confirmationModal.classList.remove('active'); // Hide modal
                });

                // "Submit" button on confirmation screen (data submission to GAS)
                confirmSubmitButton.addEventListener('click', async function() {
                    console.log("Attempting to send form data..."); // Add log
                    confirmationModal.classList.remove('active'); // Close modal after submission
                    
                    const form = internshipForm;
                    const formData = new FormData(form);

                    // Create URLSearchParams for submission, collecting all data including multiple checkboxes
                    const submissionParams = new URLSearchParams();
                    // For text/email/tel/textarea/date fields, FormData.entries() works directly
                    formData.forEach((value, key) => {
                        // Skip desired-facility, desired-role, and internship-duration here, as they are handled explicitly
                        if (key !== 'desired-facility' && key !== 'desired-role' && key !== 'internship-duration') {
                             submissionParams.append(key, value);
                        }
                    });

                    // Manually append all checked desired-facility values
                    Array.from(document.querySelectorAll('input[name="desired-facility"]:checked'))
                        .map(cb => cb.value)
                        .forEach(facility => {
                            submissionParams.append('desired-facility', facility);
                        });

                    // Manually append selected text (not value) for desired-role and internship-duration
                    const desiredRoleSelect = form.elements['desired-role'];
                    submissionParams.append('desired-role', desiredRoleSelect.selectedOptions[0].text);

                    const internshipDurationSelect = form.elements['internship-duration'];
                    submissionParams.append('internship-duration', internshipDurationSelect.selectedOptions[0].text);


                    console.log("Data to be sent (URLSearchParams):", submissionParams.toString()); // Log the actual string being sent
                    
                    // Google Apps ScriptのウェブアプリURLをここに設定
                    const appsScriptUrl = "https://script.google.com/macros/s/AKfycbwKQu3LMXWsr_4j7qb2Mv_PxiItLvY0FMcKz1-M92JRWsaVIsiBpqt431YST2MuQble/exec"; 

                    // Check if URL is still a placeholder and raise an error
                    if (appsScriptUrl === "YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE" || !appsScriptUrl.startsWith("https://script.google.com/macros/s/")) {
                        console.error("エラー: Google Apps ScriptのURLが設定されていません。コード内の 'YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE' を実際のURLに置き換えてください。");
                        alert("設定エラー: お申込みを送信できませんでした。開発者にお問い合わせください。");
                        return; // Stop submission process
                    }

                    try {
                        console.log("Sending fetch request to:", appsScriptUrl); // Add log
                        const response = await fetch(appsScriptUrl, {
                            method: 'POST',
                            mode: 'no-cors', // To avoid CORS errors (but exact response cannot be received)
                            headers: {
                                'Content-Type': 'application/x-www-form-urlencoded; charset=UTF-8', // Change Content-Type
                            },
                            body: submissionParams.toString(), // Send as URL-encoded string
                        });

                        console.log('Form submission attempted. Check Google Sheet.');
                        alert('お申込みありがとうございます。内容を確認後、担当者よりご連絡いたします。'); // Feedback to user
                        internshipForm.reset(); // Reset form
                        showEventPage(); // Return to event page after submission

                    } catch (error) {
                        console.error('Error submitting form:', error);
                        alert('お申込み中にエラーが発生しました。もう一度お試しいただくか、直接お問い合わせください。');
                    }
                });

            } else {
                console.error("Error: 'internshipForm' element not found. Please ensure your HTML form has id='internshipForm'.");
            }
        });
    </script>
</body>
</html>

/*The following code opens access to specific google drive folders containing photoes from hiking in Zagoria - day by day*/
[index.html](https://github.com/user-attachments/files/28405793/index.html)
<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>טיול נודד בזגוריה 19-25.5.26</title>
    <style>
        :root {
            --bg-gradient: linear-gradient(135deg, #11261a 0%, #08120d 100%);
            --card-bg: rgba(20, 43, 30, 0.6);
            --card-border: rgba(61, 106, 76, 0.4);
            --card-hover-border: rgba(143, 188, 143, 0.8);
            --primary-text: #ffffff;
            --muted-text: #a3b8ad;
            --accent-color: #8fbc8f;
            --shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        body {
            font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: var(--bg-gradient);
            background-attachment: fixed;
            color: var(--primary-text);
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: flex-start; /* מאפשר גלילה טבעית מתחילת העמוד */
            min-height: 100vh;
            direction: rtl;
            overflow-y: auto; /* מבטיח גלילה אנכית תקינה */
        }

        .container {
            width: 100%;
            max-width: 750px;
            padding: 50px 20px;
            box-sizing: border-box;
        }

        header {
            text-align: center;
            margin-bottom: 45px;
            position: relative;
        }

        header h1 {
            font-size: 3rem;
            margin: 0 0 10px 0;
            font-weight: 800;
            letter-spacing: -1px;
            background: linear-gradient(to bottom, #ffffff, #a3b8ad);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 2px 10px rgba(0,0,0,0.5);
        }

        header p {
            color: var(--muted-text);
            font-size: 1.25rem;
            margin: 0;
            font-weight: 400;
        }

        .logo-tiuli {
            position: absolute;
            top: 0;
            left: 20px;
            font-size: 1.5rem;
            opacity: 0.2;
            font-weight: bold;
        }

        .links-grid {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .folder-btn {
            background: var(--card-bg);
            backdrop-filter: blur(8px);
            -webkit-backdrop-filter: blur(8px);
            border: 1px solid var(--card-border);
            border-radius: 16px;
            padding: 24px 28px;
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            align-items: center;
            text-decoration: none;
            color: var(--primary-text);
            box-shadow: var(--shadow);
            transition: var(--transition);
            cursor: pointer;
            gap: 24px;
        }

        .folder-btn:hover {
            transform: translateY(-4px) scale(1.01);
            border-color: var(--card-hover-border);
            background: rgba(25, 54, 38, 0.8);
            box-shadow: 0 12px 40px rgba(0, 0, 0, 0.5);
        }

        .text-content {
            flex-grow: 1;
            text-align: right;
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .folder-date {
            font-size: 1.35rem;
            font-weight: 700;
            color: #ffffff;
            border-bottom: 1px solid rgba(255,255,255,0.08);
            padding-bottom: 6px;
        }

        .folder-description {
            font-size: 1.05rem;
            color: var(--muted-text);
            line-height: 1.6;
            font-weight: 400;
        }

        .action-area {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
        }

        .arrow-svg {
            width: 24px;
            height: 24px;
            fill: none;
            stroke: var(--muted-text);
            stroke-width: 2.5;
            stroke-linecap: round;
            stroke-linejoin: round;
            transition: var(--transition);
        }

        .folder-btn:hover .arrow-svg {
            stroke: #ffffff;
            transform: translateX(-6px);
        }

        footer {
            text-align: center;
            margin-top: 60px;
            font-size: 0.95rem;
            color: var(--muted-text);
            border-top: 1px solid rgba(61, 106, 76, 0.2);
            padding-top: 20px;
        }

        @media (max-width: 480px) {
            header h1 { font-size: 2.2rem; }
            .folder-btn { padding: 20px; gap: 15px; }
            .folder-date { font-size: 1.15rem; }
            .folder-description { font-size: 0.95rem; }
            .arrow-svg { width: 20px; height: 20px; }
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="logo-tiuli">Tiuli</div>
        <header>
            <h1>טיול נודד בזגוריה</h1>
            <p>19-25.5.26 | אלבומי תמונות לפי ימים</p>
        </header>

        <main class="links-grid">
            
            <a href="https://drive.google.com/drive/folders/1sswluqXdMeKJ-VbNTJXxW9RElW97LNsr" target="_blank" class="folder-btn">
                <div class="text-content">
                    <span class="folder-date">יום ג' - 19.5.26</span>
                    <span class="folder-description">יואנינה, מערת הנטיפים והעיר העתיקה</span>
                </div>
                <div class="action-area">
                    <svg class="arrow-svg" viewBox="0 0 24 24"><path d="M15 18l-6-6 6-6"/></svg>
                </div>
            </a>

            <a href="https://drive.google.com/drive/folders/1ooRgjjQXkfL7onCyGSL_wxp5sRVfaG4_" target="_blank" class="folder-btn">
                <div class="text-content">
                    <span class="folder-date">יום ד' - 20.5.26</span>
                    <span class="folder-description">תצפית על המגה לאקוס, הליכה לתצפית בלוי על קניון הויקוס, מדרגות ורידטו וטיפוס ללינה בקאפסובו</span>
                </div>
                <div class="action-area">
                    <svg class="arrow-svg" viewBox="0 0 24 24"><path d="M15 18l-6-6 6-6"/></svg>
                </div>
            </a>

            <a href="https://drive.google.com/drive/folders/1pjX7aLc2JXxIGF4hzL5-WUHR42ytMdi2" target="_blank" class="folder-btn">
                <div class="text-content">
                    <span class="folder-date">יום ה' - 21.5.26</span>
                    <span class="folder-description">הליכה דרך מקורות הויקוס, מפעלי טחנות קמח, על ומתחת גשרי שלושת הקשתות, עלייה במדרגות ויצה. לינה בויצה תחתית</span>
                </div>
                <div class="action-area">
                    <svg class="arrow-svg" viewBox="0 0 24 24"><path d="M15 18l-6-6 6-6"/></svg>
                </div>
            </a>

            <a href="https://drive.google.com/drive/folders/1Ke5j5hNTPlPhfblojUO27O24XGXFDpVC" target="_blank" class="folder-btn">
                <div class="text-content">
                    <span class="folder-date">יום ו' - 22.5.26</span>
                    <span class="folder-description">מעבר דרך ויצה עילית ומונודנדרי, ירידה לקניון הויקוס והליכה לאורכו עד מעיין וידומאטיס, טיפוס לפאפיגו, לינה במגה פאפיגו</span>
                </div>
                <div class="action-area">
                    <svg class="arrow-svg" viewBox="0 0 24 24"><path d="M15 18l-6-6 6-6"/></svg>
                </div>
            </a>

            <a href="https://drive.google.com/drive/folders/1mMFNwpYN5BXz7hUTn5RtwAdhCoxqFkgh" target="_blank" class="folder-btn">
                <div class="text-content">
                    <span class="folder-date">יום שבת - 23.5.26</span>
                    <span class="folder-description">יום ראפטינג, קניוניג וסיור בפאפיגו</span>
                </div>
                <div class="action-area">
                    <svg class="arrow-svg" viewBox="0 0 24 24"><path d="M15 18l-6-6 6-6"/></svg>
                </div>
            </a>

            <a href="https://drive.google.com/drive/folders/192Wt5KiWuSgGSpmjfdwSRQUTFz5QN5hg" target="_blank" class="folder-btn">
                <div class="text-content">
                    <span class="folder-date">יום א' - 24.5.26</span>
                    <span class="folder-description">סיור במקטע הבריכות, מעבר למיקרו פאפיגו וטיפוס לאסטרקה, הליכה לאגם הדרקון דרקולימני</span>
                </div>
                <div class="action-area">
                    <svg class="arrow-svg" viewBox="0 0 24 24"><path d="M15 18l-6-6 6-6"/></svg>
                </div>
            </a>

            <a href="https://drive.google.com/drive/folders/1D9cN4QAetTsOzZKM2vrTUFdgk-MnkCxK" target="_blank" class="folder-btn">
                <div class="text-content">
                    <span class="folder-date">יום ב' - 25.5.26</span>
                    <span class="folder-description">הליכה בשדות כרכומים ושלוגיות בין האסטרקה לגמילה, ודרך המגה לאקוס חזרה לנקודת ההתחלה</span>
                </div>
                <div class="action-area">
                    <svg class="arrow-svg" viewBox="0 0 24 24"><path d="M15 18l-6-6 6-6"/></svg>
                </div>
            </a>

        </main>

        <footer>
            <p>לחצו על הימים לפתיחת התיקייה בלשונית חדשה</p>
        </footer>
    </div>

</body>
</html>

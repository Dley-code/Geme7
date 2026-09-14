<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>Мобильный Игровой Хаб</title>
<style>
    :root {
        --bg-color: #0f0f13;
        --bg-gradient: radial-gradient(circle at 20% 0%, #1a1a2e 0%, #0f0f13 60%);
        --card-bg: rgba(30, 30, 40, 0.85);
        --card-border: rgba(255,255,255,0.06);
        --primary: #4caf50;
        --secondary: #ff9800;
        --match3-color: #9c27b0;
        --reaction-color: #00bcd4;
        --puzzle-color: #f44336;
        --arknoid-color: #3f51b5;
        --premium-color: #ffc107;
        --tetris-color: #00e676;
        --tower-color: #ff5722;
        --race-color: #ff3d00;
        --flappy-color: #ffc400;
        --duel-color: #e91e63;
        --duel2-color: #00e5ff;
        --ad-color: #ff4081;
        --gold: #ffd54f;
        --text: #ffffff;
        --text-secondary: #9a9aa8;
        --shadow: 0 10px 30px rgba(0,0,0,0.4);
    }
    * { box-sizing: border-box; }
    body {
        background-color: var(--bg-color);
        background-image: var(--bg-gradient);
        background-attachment: fixed;
        color: var(--text);
        font-family: system-ui, -apple-system, "Segoe UI", sans-serif;
        margin: 0; padding: 0;
        display: flex; flex-direction: column;
        align-items: center;
        min-height: 100vh;
        overflow-x: hidden;
        -webkit-font-smoothing: antialiased;
    }
    .screen { display: none; width: 100%; max-width: 460px; padding: 20px; flex-direction: column; align-items: center; }
    .screen.active { display: flex; animation: fadeIn 0.3s ease; }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: translateY(0); } }
    .header-bar { width: 100%; display: flex; justify-content: space-between; align-items: center; margin-bottom: 4px; }
    h1 {
        text-align: center; margin: 8px 0 0;
        font-size: 30px; font-weight: 800; letter-spacing: 2px;
        background: linear-gradient(90deg, #4caf50, #ff9800, #9c27b0, #00bcd4, #f44336, #3f51b5, #00e676, #ff5722, #ff4081, #ff3d00, #ffc400, #e91e63, #00e5ff, #ffc107);
        -webkit-background-clip: text; background-clip: text; color: transparent;
        animation: hueShift 8s linear infinite;
    }
    @keyframes hueShift { 0%,100% { filter: hue-rotate(0deg); } 50% { filter: hue-rotate(30deg); } }
    .coin-badge {
        display: inline-flex; align-items: center; gap: 6px;
        background: linear-gradient(135deg, rgba(255,193,7,0.15), rgba(255,152,0,0.1));
        border: 1px solid rgba(255,193,7,0.4);
        color: var(--gold);
        padding: 6px 12px; border-radius: 20px;
        font-weight: 800; font-size: 15px;
        box-shadow: 0 0 14px rgba(255,193,7,0.15);
    }
    .coin-badge.bump { animation: coinBump 0.4s ease; }
    @keyframes coinBump { 0% { transform: scale(1); } 50% { transform: scale(1.25); box-shadow: 0 0 24px rgba(255,193,7,0.6); } 100% { transform: scale(1); } }
    .ad-banner {
        width: 100%; margin-top: 14px;
        background: linear-gradient(135deg, rgba(255,64,129,0.15), rgba(156,39,176,0.1));
        border: 1px solid rgba(255,64,129,0.4);
        border-radius: 16px; padding: 14px 16px;
        display: flex; align-items: center; gap: 12px;
        cursor: pointer;
        transition: transform 0.15s, box-shadow 0.25s;
        box-shadow: 0 6px 20px rgba(255,64,129,0.15);
        -webkit-tap-highlight-color: transparent;
    }
    .ad-banner:active { transform: scale(0.97); box-shadow: 0 0 24px rgba(255,64,129,0.4); }
    .ad-banner-icon { font-size: 28px; flex-shrink: 0; }
    .ad-banner-info { flex: 1; text-align: left; }
    .ad-banner-info h4 { margin: 0 0 3px 0; font-size: 15px; font-weight: 800; color: #ff4081; }
    .ad-banner-info p { margin: 0; font-size: 12px; color: var(--text-secondary); }
    .ad-banner-reward {
        background: linear-gradient(135deg, #ffc107, #ff9800);
        color: #1a1200; font-weight: 800; font-size: 13px;
        padding: 6px 10px; border-radius: 12px; white-space: nowrap;
    }
    /* ВКЛАДКИ */
    .tabs {
        display: flex;
        gap: 8px;
        width: 100%;
        margin-top: 18px;
        background: rgba(255,255,255,0.03);
        border: 1px solid rgba(255,255,255,0.08);
        border-radius: 14px;
        padding: 5px;
    }
    .tab {
        flex: 1;
        text-align: center;
        padding: 10px 8px;
        border-radius: 10px;
        font-weight: 700;
        font-size: 14px;
        cursor: pointer;
        transition: background 0.2s, color 0.2s, transform 0.15s;
        -webkit-tap-highlight-color: transparent;
        color: var(--text-secondary);
    }
    .tab.active {
        background: linear-gradient(135deg, rgba(76,175,80,0.25), rgba(0,188,212,0.2));
        color: #fff;
        box-shadow: 0 2px 10px rgba(0,188,212,0.2);
    }
    .tab:active { transform: scale(0.96); }
    .tab-content { display: none; width: 100%; }
    .tab-content.active { display: block; }
    .section-title {
        width: 100%; margin: 20px 0 6px;
        font-size: 14px; font-weight: 700; letter-spacing: 1.5px;
        color: var(--text-secondary); text-transform: uppercase;
        display: flex; align-items: center; gap: 10px;
    }
    .section-title::after { content: ""; flex: 1; height: 1px; background: linear-gradient(90deg, rgba(255,255,255,0.12), transparent); }
    .section-title.premium { color: var(--gold); }
    .section-title.premium::after { background: linear-gradient(90deg, rgba(255,193,7,0.4), transparent); }
    .section-title.duo { color: var(--duel-color); }
    .section-title.duo::after { background: linear-gradient(90deg, rgba(233,30,99,0.4), transparent); }
    .grid-menu { display: flex; flex-direction: column; gap: 12px; width: 100%; }
    .game-card {
        position: relative;
        background: var(--card-bg);
        backdrop-filter: blur(12px);
        -webkit-backdrop-filter: blur(12px);
        border: 1px solid var(--card-border);
        border-radius: 18px; padding: 16px 18px;
        display: flex; align-items: center; justify-content: space-between;
        cursor: pointer; overflow: hidden;
        box-shadow: var(--shadow);
        transition: transform 0.15s ease, box-shadow 0.25s ease;
        -webkit-tap-highlight-color: transparent;
    }
    .game-card::before {
        content: ""; position: absolute; inset: 0;
        background: linear-gradient(120deg, transparent 30%, rgba(255,255,255,0.06) 50%, transparent 70%);
        transform: translateX(-100%); transition: transform 0.6s ease;
    }
    .game-card:hover::before { transform: translateX(100%); }
    .game-card:active { transform: scale(0.97); }
    .card-snake { border-left: 3px solid var(--primary); }
    .card-2048 { border-left: 3px solid var(--secondary); }
    .card-match3 { border-left: 3px solid var(--match3-color); }
    .card-reaction { border-left: 3px solid var(--reaction-color); }
    .card-puzzle { border-left: 3px solid var(--puzzle-color); }
    .card-arknoid { border-left: 3px solid var(--arknoid-color); }
    .card-race { border-left: 3px solid var(--race-color); }
    .card-flappy { border-left: 3px solid var(--flappy-color); }
    .card-duel { border-left: 3px solid var(--duel-color); }
    .card-duel2 { border-left: 3px solid var(--duel2-color); }
    .card-premium { border-left: 3px solid var(--premium-color); background: linear-gradient(135deg, rgba(255,193,7,0.08), rgba(156,39,176,0.08)), var(--card-bg); }
    .card-tetris { border-left: 3px solid var(--tetris-color); background: linear-gradient(135deg, rgba(0,230,118,0.08), rgba(0,188,212,0.08)), var(--card-bg); }
    .card-tower { border-left: 3px solid var(--tower-color); background: linear-gradient(135deg, rgba(255,87,34,0.08), rgba(255,193,7,0.08)), var(--card-bg); }
    .card-snake:active { box-shadow: 0 0 24px rgba(76,175,80,0.35); }
    .card-2048:active { box-shadow: 0 0 24px rgba(255,152,0,0.35); }
    .card-match3:active { box-shadow: 0 0 24px rgba(156,39,176,0.35); }
    .card-reaction:active { box-shadow: 0 0 24px rgba(0,188,212,0.35); }
    .card-puzzle:active { box-shadow: 0 0 24px rgba(244,67,54,0.35); }
    .card-arknoid:active { box-shadow: 0 0 24px rgba(63,81,181,0.4); }
    .card-race:active { box-shadow: 0 0 24px rgba(255,61,0,0.4); }
    .card-flappy:active { box-shadow: 0 0 24px rgba(255,196,0,0.4); }
    .card-duel:active { box-shadow: 0 0 24px rgba(233,30,99,0.4); }
    .card-duel2:active { box-shadow: 0 0 24px rgba(0,229,255,0.4); }
    .card-premium:active { box-shadow: 0 0 28px rgba(255,193,7,0.4); }
    .card-tetris:active { box-shadow: 0 0 28px rgba(0,230,118,0.4); }
    .card-tower:active { box-shadow: 0 0 28px rgba(255,87,34,0.4); }
    .game-info h3 { margin: 0 0 4px 0; font-size: 18px; font-weight: 700; }
    .game-info p { margin: 0; color: var(--text-secondary); font-size: 13px; }
    .game-icon { font-size: 32px; filter: drop-shadow(0 4px 10px rgba(0,0,0,0.4)); transition: transform 0.3s ease; }
    .game-card:active .game-icon { transform: scale(1.15) rotate(-6deg); }
    .price-tag {
        display: inline-flex; align-items: center; gap: 4px;
        background: linear-gradient(135deg, #ffc107, #ff9800);
        color: #1a1200; font-weight: 800; font-size: 13px;
        padding: 4px 10px; border-radius: 12px; margin-top: 4px;
        box-shadow: 0 2px 8px rgba(255,152,0,0.4);
    }
    .price-tag.tetris-price { background: linear-gradient(135deg, #00e676, #00b8d4); color: #001a0a; box-shadow: 0 2px 8px rgba(0,230,118,0.4); }
    .price-tag.tower-price { background: linear-gradient(135deg, #ff5722, #ff9800); color: #1a0a00; box-shadow: 0 2px 8px rgba(255,87,34,0.4); }
    .price-tag.owned { background: linear-gradient(135deg, #66bb6a, #2e7d32); color: #fff; }
    .back-btn {
        align-self: flex-start;
        background: rgba(255,255,255,0.06);
        color: white; border: 1px solid rgba(255,255,255,0.1);
        padding: 10px 18px; border-radius: 10px;
        font-size: 15px; font-weight: 600; margin-bottom: 15px;
        cursor: pointer; backdrop-filter: blur(8px);
        transition: background 0.2s, transform 0.15s;
    }
    .back-btn:active { transform: scale(0.94); background: rgba(255,255,255,0.12); }
    .score-container { display: flex; gap: 12px; margin-bottom: 15px; font-size: 16px; width: 100%; justify-content: center; }
    .score-box {
        background: var(--card-bg);
        backdrop-filter: blur(10px);
        padding: 10px 16px; border-radius: 12px;
        border: 1px solid var(--card-border);
        text-align: center; flex: 1; max-width: 140px;
        box-shadow: var(--shadow);
    }
    .score-box.p1 { border-color: rgba(233,30,99,0.5); }
    .score-box.p2 { border-color: rgba(0,229,255,0.5); }
    .score-box.record { border-color: rgba(255,213,79,0.5); box-shadow: 0 0 18px rgba(255,213,79,0.25); }
    .score-val { font-weight: 800; color: #fff; display: block; font-size: 20px; transition: transform 0.2s, color 0.3s; }
    .score-val.bump { animation: bump 0.4s ease; }
    @keyframes bump { 0% { transform: scale(1); } 50% { transform: scale(1.35); color: #ffd54f; } 100% { transform: scale(1); } }
    canvas { border-radius: 12px; max-width: 100%; height: auto; display: block; box-shadow: var(--shadow); touch-action: none; }
    #snakeCanvas { border: 2px solid rgba(76,175,80,0.5); background-color: #060a06; }
    #canvas2048 { border: 2px solid rgba(255,152,0,0.5); background-color: #1a1610; }
    #match3Canvas { border: 2px solid rgba(156,39,176,0.5); background-color: #100812; }
    #reactionCanvas { border: 2px solid rgba(0,188,212,0.5); background-color: #041014; }
    #puzzleCanvas { border: 2px solid rgba(244,67,54,0.5); background-color: #140606; }
    #shooterCanvas { border: 2px solid rgba(255,193,7,0.5); background-color: #000510; }
    #arknoidCanvas { border: 2px solid rgba(63,81,181,0.5); background-color: #04060f; }
    #tetrisCanvas { border: 2px solid rgba(0,230,118,0.5); background-color: #021208; }
    #towerCanvas { border: 2px solid rgba(255,87,34,0.5); background-color: #0f0602; }
    #raceCanvas { border: 2px solid rgba(255,61,0,0.5); background-color: #1a0a00; }
    #flappyCanvas { border: 2px solid rgba(255,196,0,0.5); background-color: #041a2e; }
    #duelCanvas { border: 2px solid rgba(233,30,99,0.5); background-color: #0f0408; }
    #duel2Canvas { border: 2px solid rgba(0,229,255,0.5); background-color: #04080f; }
    .controls {
        display: grid;
        grid-template-areas: ".    up    ." "left .     right" ".    down  .";
        gap: 10px; margin-top: 20px; width: 210px;
    }
    .btn {
        background: rgba(255,255,255,0.06);
        color: white; border: 1px solid rgba(255,255,255,0.12);
        border-radius: 14px; padding: 18px;
        font-size: 22px; font-weight: bold;
        user-select: none; outline: none; cursor: pointer;
        backdrop-filter: blur(8px);
        transition: background 0.15s, transform 0.1s, border-color 0.15s;
        -webkit-tap-highlight-color: transparent;
    }
    .btn:active { transform: scale(0.9); }
    .snake-btn:active { background: rgba(76,175,80,0.4); border-color: #81c784; }
    .btn2048:active { background: rgba(255,152,0,0.4); border-color: #ffb74d; }
    .btn-match3:active { background: rgba(156,39,176,0.4); border-color: #ba68c8; }
    .btn-arknoid:active { background: rgba(63,81,181,0.4); border-color: #7986cb; }
    .btn-tetris:active { background: rgba(0,230,118,0.4); border-color: #69f0ae; }
    .btn-shooter:active { background: rgba(255,193,7,0.4); border-color: #ffe082; }
    .btn-tower:active { background: rgba(255,87,34,0.4); border-color: #ff8a65; }
    .btn-race:active { background: rgba(255,61,0,0.4); border-color: #ff8a65; }
    .btn-up { grid-area: up; } .btn-down { grid-area: down; } .btn-left { grid-area: left; } .btn-right { grid-area: right; }
    /* Панели для 2 игроков */
    .duo-controls {
        display: flex;
        gap: 8px;
        margin-top: 14px;
        width: 100%;
        justify-content: space-between;
    }
    .duo-panel {
        flex: 1;
        display: flex;
        flex-direction: column;
        gap: 6px;
        padding: 8px;
        border-radius: 14px;
    }
    .duo-panel.p1 { background: rgba(233,30,99,0.1); border: 1px solid rgba(233,30,99,0.3); }
    .duo-panel.p2 { background: rgba(0,229,255,0.1); border: 1px solid rgba(0,229,255,0.3); }
    .duo-label {
        font-size: 12px;
        font-weight: 800;
        letter-spacing: 1px;
        text-align: center;
        margin-bottom: 2px;
    }
    .duo-panel.p1 .duo-label { color: #e91e63; }
    .duo-panel.p2 .duo-label { color: #00e5ff; }
    .duo-row { display: flex; gap: 6px; }
    .duo-btn {
        flex: 1;
        padding: 14px 4px;
        border-radius: 10px;
        border: none;
        background: rgba(255,255,255,0.08);
        color: #fff;
        font-size: 18px;
        font-weight: 800;
        cursor: pointer;
        user-select: none;
        -webkit-tap-highlight-color: transparent;
        transition: transform 0.1s, background 0.15s;
    }
    .duo-btn:active { transform: scale(0.9); }
    .duo-btn.p1 { background: rgba(233,30,99,0.25); }
    .duo-btn.p1:active { background: rgba(233,30,99,0.6); }
    .duo-btn.p2 { background: rgba(0,229,255,0.25); }
    .duo-btn.p2:active { background: rgba(0,229,255,0.6); }
    /* Реакция на двоих */
    .duel2-split {
        display: flex;
        width: 100%;
        gap: 8px;
        margin-top: 14px;
    }
    .duel2-side {
        flex: 1;
        padding: 30px 10px;
        border-radius: 16px;
        text-align: center;
        font-weight: 800;
        font-size: 18px;
        cursor: pointer;
        user-select: none;
        -webkit-tap-highlight-color: transparent;
        transition: transform 0.1s, filter 0.15s;
        border: 2px solid;
    }
    .duel2-side:active { transform: scale(0.96); }
    .duel2-side.p1 { background: rgba(233,30,99,0.2); border-color: #e91e63; color: #ff80ab; }
    .duel2-side.p1.flash { background: #e91e63; color: #fff; filter: brightness(1.4); }
    .duel2-side.p2 { background: rgba(0,229,255,0.2); border-color: #00e5ff; color: #80deea; }
    .duel2-side.p2.flash { background: #00e5ff; color: #003040; filter: brightness(1.4); }
    .big-action-btn {
        margin-top: 18px; padding: 16px 36px;
        font-size: 18px; font-weight: 800; letter-spacing: 1px;
        border: none; border-radius: 16px; cursor: pointer;
        color: white;
        background: linear-gradient(135deg, #00bcd4, #0097a7);
        box-shadow: 0 8px 24px rgba(0,188,212,0.35);
        transition: transform 0.15s, box-shadow 0.2s;
        -webkit-tap-highlight-color: transparent;
    }
    .big-action-btn:active { transform: scale(0.94); }
    .big-action-btn.puzzle-style { background: linear-gradient(135deg, #f44336, #c62828); box-shadow: 0 8px 24px rgba(244,67,54,0.35); }
    .big-action-btn.tetris-btn { background: linear-gradient(135deg, #00e676, #00b8d4); color: #001a0a; box-shadow: 0 8px 24px rgba(0,230,118,0.4); }
    .big-action-btn.flappy-btn { background: linear-gradient(135deg, #ffc400, #ff9800); color: #1a1200; box-shadow: 0 8px 24px rgba(255,196,0,0.4); }
    .big-action-btn.duel-btn { background: linear-gradient(135deg, #e91e63, #9c27b0); box-shadow: 0 8px 24px rgba(233,30,99,0.4); }
    .big-action-btn.duel2-btn { background: linear-gradient(135deg, #00e5ff, #0077ff); color: #001a2a; box-shadow: 0 8px 24px rgba(0,229,255,0.4); }
    .big-action-btn:disabled { opacity: 0.5; cursor: not-allowed; transform: none; }
    .hint-text { margin-top: 12px; font-size: 13px; color: var(--text-secondary); text-align: center; max-width: 340px; line-height: 1.4; }
    .toast {
        position: fixed; top: 20px; left: 50%;
        transform: translateX(-50%) translateY(-100px);
        background: rgba(30,30,40,0.95);
        backdrop-filter: blur(12px);
        border: 1px solid rgba(255,255,255,0.1);
        padding: 14px 24px; border-radius: 14px;
        box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        font-size: 15px; font-weight: 600; z-index: 1000;
        opacity: 0;
        transition: transform 0.4s cubic-bezier(0.2, 1.2, 0.4, 1), opacity 0.3s;
        pointer-events: none; text-align: center; max-width: 90vw;
    }
    .toast.show { transform: translateX(-50%) translateY(0); opacity: 1; }
    .toast.success { border-color: rgba(76,175,80,0.5); }
    .toast.info { border-color: rgba(255,152,0,0.5); }
    .toast.record { border-color: rgba(255,213,79,0.7); background: rgba(50,40,10,0.95); }
    .toast.coin { border-color: rgba(255,193,7,0.7); color: var(--gold); }
    .toast.ad { border-color: rgba(255,64,129,0.7); color: #ff4081; }
    .modal-overlay {
        position: fixed; inset: 0;
        background: rgba(0,0,0,0.7);
        backdrop-filter: blur(6px);
        display: none; align-items: center; justify-content: center;
        z-index: 999; padding: 20px;
    }
    .modal-overlay.show { display: flex; animation: fadeIn 0.25s ease; }
    .modal {
        background: linear-gradient(160deg, #1e1e2e, #141420);
        border: 1px solid rgba(255,193,7,0.3);
        border-radius: 22px; padding: 26px 22px;
        max-width: 360px; width: 100%;
        text-align: center;
        box-shadow: 0 20px 60px rgba(0,0,0,0.7), 0 0 40px rgba(255,193,7,0.15);
    }
    .modal-icon { font-size: 56px; margin-bottom: 6px; }
    .modal h2 { margin: 4px 0 8px; font-size: 22px; background: linear-gradient(135deg, #ffc107, #ff9800); -webkit-background-clip: text; background-clip: text; color: transparent; }
    .modal h2.tetris-title { background: linear-gradient(135deg, #00e676, #00b8d4); -webkit-background-clip: text; background-clip: text; }
    .modal h2.tower-title { background: linear-gradient(135deg, #ff5722, #ff9800); -webkit-background-clip: text; background-clip: text; }
    .modal p { color: var(--text-secondary); font-size: 14px; margin: 6px 0 18px; line-height: 1.5; }
    .modal-price { display: inline-flex; align-items: center; gap: 6px; font-size: 22px; font-weight: 800; color: var(--gold); margin-bottom: 18px; }
    .modal-buttons { display: flex; gap: 10px; }
    .modal-btn { flex: 1; padding: 14px; border-radius: 12px; border: none; font-weight: 700; font-size: 15px; cursor: pointer; transition: transform 0.15s; }
    .modal-btn:active { transform: scale(0.94); }
    .modal-btn.cancel { background: rgba(255,255,255,0.08); color: white; border: 1px solid rgba(255,255,255,0.1); }
    .modal-btn.buy { background: linear-gradient(135deg, #ffc107, #ff9800); color: #1a1200; box-shadow: 0 6px 20px rgba(255,193,7,0.4); }
    .modal-btn.buy:disabled { opacity: 0.5; cursor: not-allowed; }
    .ad-modal {
        background: linear-gradient(160deg, #1e1e2e, #141420);
        border: 1px solid rgba(255,64,129,0.4);
        border-radius: 22px; padding: 22px;
        max-width: 400px; width: 100%;
        text-align: center;
        box-shadow: 0 20px 60px rgba(0,0,0,0.7), 0 0 40px rgba(255,64,129,0.2);
    }
    .ad-modal h2 { margin: 0 0 6px; font-size: 22px; background: linear-gradient(135deg, #ff4081, #9c27b0); -webkit-background-clip: text; background-clip: text; color: transparent; }
    .ad-modal .ad-channel { color: var(--text-secondary); font-size: 13px; margin: 0 0 14px; }
    .ad-modal .ad-channel strong { color: #ff4081; }
    .ad-slide-container {
        position: relative; width: 100%;
        aspect-ratio: 16 / 11;
        background: linear-gradient(135deg, #1a0a2e, #0a0620);
        border-radius: 14px; overflow: hidden;
        box-shadow: 0 6px 20px rgba(0,0,0,0.5);
        margin-bottom: 14px;
        border: 1px solid rgba(255,64,129,0.2);
    }
    .ad-slide {
        position: absolute; inset: 0;
        display: flex; flex-direction: column; align-items: center; justify-content: center;
        padding: 16px; opacity: 0;
        transform: scale(0.9) translateY(10px);
        transition: opacity 0.5s ease, transform 0.5s ease;
        text-align: center;
    }
    .ad-slide.active { opacity: 1; transform: scale(1) translateY(0); }
    .ad-slide-icon { font-size: 42px; margin-bottom: 6px; filter: drop-shadow(0 4px 12px rgba(255,64,129,0.5)); animation: adIconFloat 2s ease-in-out infinite; }
    @keyframes adIconFloat { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-6px); } }
    .ad-slide-title { font-size: 18px; font-weight: 800; margin: 0 0 6px; background: linear-gradient(135deg, #ff4081, #ffc107); -webkit-background-clip: text; background-clip: text; color: transparent; letter-spacing: 0.5px; }
    .ad-slide-text { font-size: 12px; color: #ccc; line-height: 1.45; margin: 0 0 8px; max-width: 300px; }
    .ad-slide-tag { display: inline-block; margin-bottom: 8px; padding: 3px 10px; background: rgba(255,64,129,0.15); border: 1px solid rgba(255,64,129,0.4); border-radius: 10px; font-size: 10px; font-weight: 700; color: #ff4081; letter-spacing: 0.5px; }
    .ad-slide-actions { display: flex; gap: 6px; flex-wrap: wrap; justify-content: center; margin-top: 4px; }
    .ad-slide-btn {
        display: inline-flex; align-items: center; gap: 4px;
        padding: 8px 14px; border-radius: 10px; border: none;
        font-weight: 700; font-size: 12px; cursor: pointer;
        text-decoration: none; color: #fff;
        transition: transform 0.15s, box-shadow 0.2s;
        -webkit-tap-highlight-color: transparent; white-space: nowrap;
    }
    .ad-slide-btn:active { transform: scale(0.93); }
    .ad-slide-btn.vk { background: linear-gradient(135deg, #0077ff, #0055cc); box-shadow: 0 4px 14px rgba(0,119,255,0.45); animation: vkPulse 2s ease-in-out infinite; }
    @keyframes vkPulse { 0%, 100% { box-shadow: 0 4px 14px rgba(0,119,255,0.45); } 50% { box-shadow: 0 4px 22px rgba(0,119,255,0.75); } }
    .ad-slide-btn.video { background: linear-gradient(135deg, #ff4081, #9c27b0); box-shadow: 0 4px 14px rgba(255,64,129,0.45); }
    .ad-slide-btn.time { background: linear-gradient(135deg, #ffc107, #ff9800); color: #1a1200; box-shadow: 0 4px 14px rgba(255,193,7,0.45); }
    .ad-progress-dots { display: flex; justify-content: center; gap: 6px; margin-bottom: 12px; }
    .ad-dot { width: 8px; height: 8px; border-radius: 50%; background: rgba(255,255,255,0.15); transition: background 0.3s, transform 0.3s; }
    .ad-dot.active { background: #ff4081; transform: scale(1.3); box-shadow: 0 0 10px rgba(255,64,129,0.6); }
    .ad-dot.done { background: rgba(255,64,129,0.5); }
    .ad-timer-bar { width: 100%; height: 6px; background: rgba(255,255,255,0.1); border-radius: 3px; overflow: hidden; margin-bottom: 12px; }
    .ad-timer-fill { height: 100%; background: linear-gradient(90deg, #ff4081, #9c27b0); width: 0%; transition: width 1s linear; }
    .ad-status { font-size: 14px; color: var(--text-secondary); margin-bottom: 14px; min-height: 20px; }
    .ad-status strong { color: var(--gold); }
    .ad-modal-buttons { display: flex; gap: 10px; }
    .ad-modal-btn { flex: 1; padding: 14px; border-radius: 12px; border: none; font-weight: 700; font-size: 15px; cursor: pointer; transition: transform 0.15s; }
    .ad-modal-btn:active { transform: scale(0.94); }
    .ad-modal-btn.cancel { background: rgba(255,255,255,0.08); color: white; border: 1px solid rgba(255,255,255,0.1); }
    .ad-modal-btn.claim { background: linear-gradient(135deg, #ff4081, #9c27b0); color: white; box-shadow: 0 6px 20px rgba(255,64,129,0.4); }
    .ad-modal-btn.claim:disabled { opacity: 0.5; cursor: not-allowed; }
    .tower-tools { display: grid; grid-template-columns: repeat(4, 1fr); gap: 8px; margin-top: 14px; width: 100%; max-width: 320px; }
    .tool-btn {
        background: rgba(255,255,255,0.06);
        border: 1px solid rgba(255,255,255,0.12);
        border-radius: 12px; padding: 8px 4px;
        color: white; display: flex; flex-direction: column; align-items: center; gap: 2px;
        cursor: pointer; transition: transform 0.12s, background 0.15s, border-color 0.15s;
        -webkit-tap-highlight-color: transparent;
    }
    .tool-btn:active { transform: scale(0.92); }
    .tool-btn.selected { background: rgba(255,87,34,0.25); border-color: #ff5722; box-shadow: 0 0 16px rgba(255,87,34,0.4); }
    .tool-btn:disabled { opacity: 0.4; }
    .tool-icon { font-size: 20px; }
    .tool-name { font-size: 10px; font-weight: 700; letter-spacing: 0.3px; }
    .tool-cost { font-size: 10px; font-weight: 800; color: var(--gold); background: rgba(255,193,7,0.15); padding: 1px 5px; border-radius: 6px; }
    .tool-start { background: linear-gradient(135deg, rgba(0,230,118,0.2), rgba(0,188,212,0.15)); border-color: rgba(0,230,118,0.4); }
</style>
</head>
<body>

<div id="toast" class="toast"></div>

<div class="modal-overlay" id="buyModal">
    <div class="modal">
        <div class="modal-icon" id="modalIcon">🚀</div>
        <h2 id="modalTitle">Космический Шутер</h2>
        <p id="modalDesc"></p>
        <div class="modal-price"><span>🪙</span><span id="modalPrice">200</span></div>
        <div class="modal-buttons">
            <button class="modal-btn cancel" onclick="closeBuyModal()">Отмена</button>
            <button class="modal-btn buy" id="modalBuyBtn" onclick="confirmBuy()">Купить</button>
        </div>
    </div>
</div>

<div class="modal-overlay" id="adModal">
    <div class="ad-modal">
        <h2>📺 Реклама</h2>
        <p class="ad-channel">Канал: <strong>Dley перезаливы</strong> · VK Video</p>
        <div class="ad-slide-container" id="adSlideContainer"></div>
        <div class="ad-progress-dots" id="adDots"></div>
        <div class="ad-timer-bar"><div class="ad-timer-fill" id="adTimerFill"></div></div>
        <div class="ad-status" id="adStatus">Смотрите рекламу <strong>15 секунд</strong></div>
        <div class="ad-modal-buttons">
            <button class="ad-modal-btn cancel" onclick="closeAdModal()">Закрыть</button>
            <button class="ad-modal-btn claim" id="adClaimBtn" onclick="claimAdReward()" disabled>Получить 40 🪙</button>
        </div>
    </div>
</div>

<div id="menu-screen" class="screen active">
    <div class="header-bar">
        <h1>GAME HUB</h1>
        <div class="coin-badge" id="coinBadge"><span>🪙</span><span id="coinCount">0</span></div>
    </div>
    <div class="ad-banner" id="adBanner" onclick="openAdModal()">
        <div class="ad-banner-icon">📺</div>
        <div class="ad-banner-info">
            <h4>Смотреть рекламу</h4>
            <p>Канал Dley перезаливы · VK Video</p>
        </div>
        <div class="ad-banner-reward" id="adBannerReward">+40 🪙</div>
    </div>

    <!-- ВКЛАДКИ -->
    <div class="tabs">
        <div class="tab active" onclick="switchTab('solo')" id="tab-solo">🎮 Игры</div>
        <div class="tab" onclick="switchTab('duo')" id="tab-duo">👥 На двоих</div>
    </div>

    <!-- ВКЛАДКА: ОДИНОЧНЫЕ -->
    <div class="tab-content active" id="tab-content-solo">
        <div class="section-title">Бесплатные игры</div>
        <div class="grid-menu">
            <div class="game-card card-snake" onclick="openGame('snake-screen')">
                <div class="game-info"><h3>Змейка</h3><p>Рекорд: <span id="menu-snake-best">0</span></p></div>
                <div class="game-icon">🐍</div>
            </div>
            <div class="game-card card-2048" onclick="openGame('game2048-screen')">
                <div class="game-info"><h3>2048</h3><p>Рекорд: <span id="menu-2048-best">0</span></p></div>
                <div class="game-icon">🔢</div>
            </div>
            <div class="game-card card-match3" onclick="openGame('match3-screen')">
                <div class="game-info"><h3>3 в ряд</h3><p>Рекорд: <span id="menu-match3-best">0</span></p></div>
                <div class="game-icon">💎</div>
            </div>
            <div class="game-card card-reaction" onclick="openGame('reaction-screen')">
                <div class="game-info"><h3>Реакция</h3><p>Лучшее: <span id="menu-reaction-best">—</span></p></div>
                <div class="game-icon">⚡</div>
            </div>
            <div class="game-card card-puzzle" onclick="openGame('puzzle-screen')">
                <div class="game-info"><h3>Пятнашки</h3><p>Рекорд: <span id="menu-puzzle-best">0</span> ходов</p></div>
                <div class="game-icon">🧩</div>
            </div>
            <div class="game-card card-arknoid" onclick="openGame('arknoid-screen')">
                <div class="game-info"><h3>Арканоид</h3><p>Рекорд: <span id="menu-arknoid-best">0</span></p></div>
                <div class="game-icon">🧱</div>
            </div>
            <div class="game-card card-race" onclick="openGame('race-screen')">
                <div class="game-info"><h3>Гонки</h3><p>Рекорд: <span id="menu-race-best">0</span></p></div>
                <div class="game-icon">🏎</div>
            </div>
            <div class="game-card card-flappy" onclick="openGame('flappy-screen')">
                <div class="game-info"><h3>Flappy Bird</h3><p>Рекорд: <span id="menu-flappy-best">0</span></p></div>
                <div class="game-icon">🐦</div>
            </div>
        </div>
        <div class="section-title premium">💎 Премиум игры</div>
        <div class="grid-menu">
            <div class="game-card card-premium" onclick="onPremiumClick('shooter')">
                <div class="game-info"><h3>Космический Шутер</h3><p>Волны врагов, боссы, бонусы</p><div class="price-tag" id="shooterPriceTag">🪙 200</div></div>
                <div class="game-icon">🚀</div>
            </div>
            <div class="game-card card-tetris" onclick="onPremiumClick('tetris')">
                <div class="game-info"><h3>Тетрис</h3><p>Классика с новым дыханием</p><div class="price-tag tetris-price" id="tetrisPriceTag">🪙 250</div></div>
                <div class="game-icon">🧊</div>
            </div>
            <div class="game-card card-tower" onclick="onPremiumClick('tower')">
                <div class="game-info"><h3>Защитник Башни</h3><p>Tower Defense с волнами врагов</p><div class="price-tag tower-price" id="towerPriceTag">🪙 300</div></div>
                <div class="game-icon">🛡️</div>
            </div>
        </div>
    </div>

    <!-- ВКЛАДКА: НА ДВОИХ -->
    <div class="tab-content" id="tab-content-duo">
        <div class="section-title duo">Игры на двоих (один телефон)</div>
        <div class="grid-menu">
            <div class="game-card card-duel" onclick="openGame('duel-screen')">
                <div class="game-info"><h3>Танковая дуэль</h3><p>2 танка · стрельба · отскок снарядов</p></div>
                <div class="game-icon">⚔</div>
            </div>
            <div class="game-card card-duel2" onclick="openGame('duel2-screen')">
                <div class="game-info"><h3>Реакция-дуэль</h3><p>Кто быстрее нажмёт — 5 раундов</p></div>
                <div class="game-icon">⚡</div>
            </div>
        </div>
        <div class="hint-text" style="margin-top:16px">
            Играйте вдвоём, держа телефон горизонтально или вертикально.<br>
            Игрок 1 — 🔴 розовая сторона, Игрок 2 — 🔵 голубая сторона.
        </div>
    </div>
</div>

<!-- ЗМЕЙКА -->
<div id="snake-screen" class="screen">
    <button class="back-btn" onclick="closeGame('snake-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box">Очки <span id="snake-score" class="score-val">0</span></div>
        <div class="score-box" id="snake-best-box">Рекорд <span id="snake-best" class="score-val">0</span></div>
    </div>
    <canvas id="snakeCanvas" width="320" height="320"></canvas>
    <div class="controls">
        <button class="btn snake-btn btn-up" onpointerdown="setSnakeDir(0,-1)">▲</button>
        <button class="btn snake-btn btn-left" onpointerdown="setSnakeDir(-1,0)">◀</button>
        <button class="btn snake-btn btn-right" onpointerdown="setSnakeDir(1,0)">▶</button>
        <button class="btn snake-btn btn-down" onpointerdown="setSnakeDir(0,1)">▼</button>
    </div>
</div>

<!-- 2048 -->
<div id="game2048-screen" class="screen">
    <button class="back-btn" onclick="closeGame('game2048-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box">Счет <span id="score2048" class="score-val">0</span></div>
        <div class="score-box" id="best2048-box">Рекорд <span id="best2048" class="score-val">0</span></div>
    </div>
    <canvas id="canvas2048" width="320" height="320"></canvas>
    <div class="controls">
        <button class="btn btn2048 btn-up" onpointerdown="move2048('up')">▲</button>
        <button class="btn btn2048 btn-left" onpointerdown="move2048('left')">◀</button>
        <button class="btn btn2048 btn-right" onpointerdown="move2048('right')">▶</button>
        <button class="btn btn2048 btn-down" onpointerdown="move2048('down')">▼</button>
    </div>
</div>

<!-- 3 В РЯД -->
<div id="match3-screen" class="screen">
    <button class="back-btn" onclick="closeGame('match3-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box">Очки <span id="match3-score" class="score-val">0</span></div>
        <div class="score-box" id="match3-best-box">Рекорд <span id="match3-best" class="score-val">0</span></div>
    </div>
    <canvas id="match3Canvas" width="320" height="320"></canvas>
    <div class="controls">
        <button class="btn btn-match3 btn-up" onpointerdown="moveMatch3('up')">▲</button>
        <button class="btn btn-match3 btn-left" onpointerdown="moveMatch3('left')">◀</button>
        <button class="btn btn-match3 btn-right" onpointerdown="moveMatch3('right')">▶</button>
        <button class="btn btn-match3 btn-down" onpointerdown="moveMatch3('down')">▼</button>
    </div>
    <div class="hint-text">Нажимайте на кристаллы, свайпайте или используйте кнопки.</div>
</div>

<!-- РЕАКЦИЯ -->
<div id="reaction-screen" class="screen">
    <button class="back-btn" onclick="closeGame('reaction-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box">Время <span id="reaction-time" class="score-val">—</span></div>
        <div class="score-box" id="reaction-best-box">Лучшее <span id="reaction-best" class="score-val">—</span></div>
    </div>
    <canvas id="reactionCanvas" width="320" height="320"></canvas>
    <button class="big-action-btn" id="reactionBtn" onpointerdown="reactionTap(event)">СТАРТ</button>
    <div class="hint-text">Дождитесь зелёного экрана и нажмите как можно быстрее.</div>
</div>

<!-- ПЯТНАШКИ -->
<div id="puzzle-screen" class="screen">
    <button class="back-btn" onclick="closeGame('puzzle-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box">Ходы <span id="puzzle-moves" class="score-val">0</span></div>
        <div class="score-box" id="puzzle-best-box">Рекорд <span id="puzzle-best" class="score-val">0</span></div>
    </div>
    <canvas id="puzzleCanvas" width="320" height="320"></canvas>
    <button class="big-action-btn puzzle-style" onpointerdown="shufflePuzzle()">ПЕРЕМЕШАТЬ</button>
    <div class="hint-text">Нажимайте на плитку рядом с пустой клеткой.</div>
</div>

<!-- АРКАНОИД -->
<div id="arknoid-screen" class="screen">
    <button class="back-btn" onclick="closeGame('arknoid-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box">Очки <span id="arknoid-score" class="score-val">0</span></div>
        <div class="score-box">Уровень <span id="arknoid-level" class="score-val">1</span></div>
        <div class="score-box" id="arknoid-best-box">Рекорд <span id="arknoid-best" class="score-val">0</span></div>
    </div>
    <canvas id="arknoidCanvas" width="320" height="380"></canvas>
    <div class="controls">
        <button class="btn btn-arknoid btn-up" onpointerdown="arknoidControl('fire')">🔥</button>
        <button class="btn btn-arknoid btn-left" onpointerdown="arknoidControl('left')">◀</button>
        <button class="btn btn-arknoid btn-right" onpointerdown="arknoidControl('right')">▶</button>
        <button class="btn btn-arknoid btn-down" onpointerdown="arknoidControl('pause')">⏸</button>
    </div>
    <div class="hint-text">Бонусы: 🟢 расширение · ⚪ липкая · 🔵 3 мяча · 🔴 лазер</div>
</div>

<!-- ШУТЕР -->
<div id="shooter-screen" class="screen">
    <button class="back-btn" onclick="closeGame('shooter-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box">Очки <span id="shooter-score" class="score-val">0</span></div>
        <div class="score-box" id="shooter-best-box">Рекорд <span id="shooter-best" class="score-val">0</span></div>
    </div>
    <canvas id="shooterCanvas" width="320" height="380"></canvas>
    <div class="controls">
        <button class="btn btn-shooter btn-up" onpointerdown="shooterControl('fire')">🔥</button>
        <button class="btn btn-shooter btn-left" onpointerdown="shooterControl('left')">◀</button>
        <button class="btn btn-shooter btn-right" onpointerdown="shooterControl('right')">▶</button>
        <button class="btn btn-shooter btn-down" onpointerdown="shooterControl('pause')">⏸</button>
    </div>
    <div class="hint-text">Бонусы 💎 щит, ⚡ тройной выстрел, 💣 бомба. Боссы каждые 500 очков!</div>
</div>

<!-- ТЕТРИС -->
<div id="tetris-screen" class="screen">
    <button class="back-btn" onclick="closeGame('tetris-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box">Очки <span id="tetris-score" class="score-val">0</span></div>
        <div class="score-box" id="tetris-best-box">Рекорд <span id="tetris-best" class="score-val">0</span></div>
    </div>
    <canvas id="tetrisCanvas" width="240" height="380"></canvas>
    <div class="controls">
        <button class="btn btn-tetris btn-up" onpointerdown="tetrisControl('rotate')">🔄</button>
        <button class="btn btn-tetris btn-left" onpointerdown="tetrisControl('left')">◀</button>
        <button class="btn btn-tetris btn-right" onpointerdown="tetrisControl('right')">▶</button>
        <button class="btn btn-tetris btn-down" onpointerdown="tetrisControl('drop')">⬇</button>
    </div>
    <button class="big-action-btn tetris-btn" id="tetrisPauseBtn" onpointerdown="tetrisControl('pause')">ПАУЗА</button>
    <div class="hint-text">Собирайте линии из блоков.</div>
</div>

<!-- ЗАЩИТНИК БАШНИ -->
<div id="tower-screen" class="screen">
    <button class="back-btn" onclick="closeGame('tower-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box">Волна <span id="tower-wave" class="score-val">0</span></div>
        <div class="score-box">🪙 <span id="tower-gold" class="score-val">0</span></div>
        <div class="score-box" id="tower-best-box">Рекорд <span id="tower-best" class="score-val">0</span></div>
    </div>
    <canvas id="towerCanvas" width="320" height="380"></canvas>
    <div class="tower-tools" id="towerTools">
        <button class="tool-btn" data-type="arrow" onclick="selectTower('arrow')" onpointerdown="selectTower('arrow')">
            <span class="tool-icon">🏹</span><span class="tool-name">Лучник</span><span class="tool-cost">50</span>
        </button>
        <button class="tool-btn" data-type="fire" onclick="selectTower('fire')" onpointerdown="selectTower('fire')">
            <span class="tool-icon">🔥</span><span class="tool-name">Огонь</span><span class="tool-cost">100</span>
        </button>
        <button class="tool-btn" data-type="ice" onclick="selectTower('ice')" onpointerdown="selectTower('ice')">
            <span class="tool-icon">❄️</span><span class="tool-name">Лёд</span><span class="tool-cost">75</span>
        </button>
        <button class="tool-btn tool-start" onclick="startTowerWave()" onpointerdown="startTowerWave()">
            <span class="tool-icon">▶</span><span class="tool-name">Волна</span><span class="tool-cost">GO</span>
        </button>
    </div>
    <div class="hint-text">Выберите башню и тапните по дорожке. Запустите волну!</div>
</div>

<!-- ГОНКИ -->
<div id="race-screen" class="screen">
    <button class="back-btn" onclick="closeGame('race-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box">Очки <span id="race-score" class="score-val">0</span></div>
        <div class="score-box">Скорость <span id="race-speed" class="score-val">1</span></div>
        <div class="score-box" id="race-best-box">Рекорд <span id="race-best" class="score-val">0</span></div>
    </div>
    <canvas id="raceCanvas" width="320" height="440"></canvas>
    <div class="controls">
        <button class="btn btn-race btn-up" onpointerdown="raceControl('pause')">⏸</button>
        <button class="btn btn-race btn-left" onpointerdown="raceControl('left')">◀</button>
        <button class="btn btn-race btn-right" onpointerdown="raceControl('right')">▶</button>
        <button class="btn btn-race btn-down" onpointerdown="raceControl('boost')">⚡</button>
    </div>
    <div class="hint-text">Объезжайте машины. Чем дольше едете — тем выше скорость.</div>
</div>

<!-- FLAPPY -->
<div id="flappy-screen" class="screen">
    <button class="back-btn" onclick="closeGame('flappy-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box">Очки <span id="flappy-score" class="score-val">0</span></div>
        <div class="score-box" id="flappy-best-box">Рекорд <span id="flappy-best" class="score-val">0</span></div>
    </div>
    <canvas id="flappyCanvas" width="320" height="440"></canvas>
    <button class="big-action-btn flappy-btn" id="flappyBtn" onpointerdown="flappyFlap(event)">ЛЕТЕТЬ</button>
    <div class="hint-text">Нажимайте, чтобы птичка подпрыгивала. Пролетай между трубами!</div>
</div>

<!-- ТАНКОВАЯ ДУЭЛЬ -->
<div id="duel-screen" class="screen">
    <button class="back-btn" onclick="closeGame('duel-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box p1">🔴 П1: <span id="duel-s1" class="score-val">0</span></div>
        <div class="score-box p2">🔵 П2: <span id="duel-s2" class="score-val">0</span></div>
    </div>
    <canvas id="duelCanvas" width="400" height="400"></canvas>
    <div class="duo-controls">
        <div class="duo-panel p1">
            <div class="duo-label">🔴 ИГРОК 1</div>
            <div class="duo-row">
                <button class="duo-btn p1" onpointerdown="duelControl('p1-left')">◀</button>
                <button class="duo-btn p1" onpointerdown="duelControl('p1-right')">▶</button>
            </div>
            <div class="duo-row">
                <button class="duo-btn p1" onpointerdown="duelControl('p1-fire')">🔥 ОГОНЬ</button>
            </div>
        </div>
        <div class="duo-panel p2">
            <div class="duo-label">🔵 ИГРОК 2</div>
            <div class="duo-row">
                <button class="duo-btn p2" onpointerdown="duelControl('p2-left')">◀</button>
                <button class="duo-btn p2" onpointerdown="duelControl('p2-right')">▶</button>
            </div>
            <div class="duo-row">
                <button class="duo-btn p2" onpointerdown="duelControl('p2-fire')">🔥 ОГОНЬ</button>
            </div>
        </div>
    </div>
    <button class="big-action-btn duel-btn" onclick="duelReset()">🔄 НОВЫЙ РАУНД</button>
    <div class="hint-text">Попади в танк соперника 3 раза, чтобы победить. Снаряды отскакивают от стен.</div>
</div>

<!-- РЕАКЦИЯ-ДУЭЛЬ -->
<div id="duel2-screen" class="screen">
    <button class="back-btn" onclick="closeGame('duel2-screen')">◀ Меню</button>
    <div class="score-container">
        <div class="score-box p1">🔴 П1: <span id="duel2-s1" class="score-val">0</span></div>
        <div class="score-box" id="duel2-round-box">Раунд <span id="duel2-round" class="score-val">0</span>/5</div>
        <div class="score-box p2">🔵 П2: <span id="duel2-s2" class="score-val">0</span></div>
    </div>
    <canvas id="duel2Canvas" width="400" height="280"></canvas>
    <div class="duel2-split">
        <div class="duel2-side p1" id="duel2-side1" onpointerdown="duel2Tap('p1')">🔴 ИГРОК 1<br><small>ЖДИ...</small></div>
        <div class="duel2-side p2" id="duel2-side2" onpointerdown="duel2Tap('p2')">🔵 ИГРОК 2<br><small>ЖДИ...</small></div>
    </div>
    <button class="big-action-btn duel2-btn" id="duel2Btn" onclick="duel2Start()">НАЧАТЬ РАУНД</button>
    <div class="hint-text">Когда экран загорится цветом вашей стороны — нажмите свою кнопку! Кто быстрее в 3 из 5 раундов — победил.</div>
</div>

<script>
/* ============================================================
   УТИЛИТЫ
============================================================ */
const $ = id => document.getElementById(id);
function toast(msg, type = 'info', duration = 2200) {
    const el = $('toast');
    el.textContent = msg;
    el.className = 'toast show ' + type;
    clearTimeout(el._t);
    el._t = setTimeout(() => el.classList.remove('show'), duration);
}
function haptic(ms = 12) { if (navigator.vibrate) navigator.vibrate(ms); }
function bump(el) { el.classList.remove('bump'); void el.offsetWidth; el.classList.add('bump'); }
function getBest(key) { return parseInt(localStorage.getItem(key) || '0', 10); }
function getBestFloat(key) { return parseFloat(localStorage.getItem(key) || '0'); }
function roundRect(ctx, x, y, w, h, r) {
    ctx.beginPath();
    if (ctx.roundRect) { ctx.roundRect(x, y, w, h, r); return; }
    ctx.moveTo(x + r, y);
    ctx.arcTo(x + w, y, x + w, y + h, r);
    ctx.arcTo(x + w, y + h, x, y + h, r);
    ctx.arcTo(x, y + h, x, y, r);
    ctx.arcTo(x, y, x + w, y, r);
    ctx.closePath();
}

/* ВКЛАДКИ МЕНЮ */
function switchTab(tabName) {
    haptic(8);
    document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
    document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
    $('tab-' + tabName).classList.add('active');
    $('tab-content-' + tabName).classList.add('active');
}

/* ============================================================
   МОНЕТЫ
============================================================ */
function getCoins() { return parseInt(localStorage.getItem('coins') || '0', 10); }
function setCoins(v) { localStorage.setItem('coins', Math.max(0, v)); updateCoinsUI(); }
function addCoins(n, showToast = true) {
    if (n <= 0) return;
    setCoins(getCoins() + n);
    if (showToast) toast('+' + n + ' 🪙', 'coin', 1200);
}
function updateCoinsUI() {
    $('coinCount').textContent = getCoins();
    const badge = $('coinBadge');
    badge.classList.remove('bump');
    void badge.offsetWidth;
    badge.classList.add('bump');
}

/* ============================================================
   ПРЕМИУМ
============================================================ */
const PREMIUM = {
    shooter: { title: 'Космический Шутер', icon: '🚀', price: 200, desc: 'Волны врагов, боссы каждые 500 очков, бонусы и комбо.', ownedKey: 'shooter_owned', screen: 'shooter-screen', tagId: 'shooterPriceTag', titleClass: '' },
    tetris: { title: 'Тетрис', icon: '🧊', price: 250, desc: 'Легендарная головоломка с падающими блоками.', ownedKey: 'tetris_owned', screen: 'tetris-screen', tagId: 'tetrisPriceTag', titleClass: 'tetris-title' },
    tower: { title: 'Защитник Башни', icon: '🛡️', price: 300, desc: 'Tower Defense: враги идут по дорожке, вы ставите башни.', ownedKey: 'tower_owned', screen: 'tower-screen', tagId: 'towerPriceTag', titleClass: 'tower-title' }
};
function isOwned(key) { return localStorage.getItem(PREMIUM[key].ownedKey) === '1'; }
function setOwned(key) { localStorage.setItem(PREMIUM[key].ownedKey, '1'); }
function updatePremiumTags() {
    for (const key in PREMIUM) {
        const p = PREMIUM[key];
        const tag = $(p.tagId);
        if (isOwned(key)) { tag.textContent = '✅ Куплено'; tag.classList.add('owned'); }
        else { tag.textContent = '🪙 ' + p.price; tag.classList.remove('owned'); }
    }
}
let pendingPurchase = null;
function onPremiumClick(key) { haptic(12); if (isOwned(key)) openGame(PREMIUM[key].screen); else openBuyModal(key); }
function openBuyModal(key) {
    const p = PREMIUM[key];
    pendingPurchase = key;
    $('modalIcon').textContent = p.icon;
    $('modalTitle').textContent = p.title;
    $('modalTitle').className = p.titleClass || '';
    $('modalDesc').textContent = p.desc;
    $('modalPrice').textContent = p.price;
    const canAfford = getCoins() >= p.price;
    const btn = $('modalBuyBtn');
    btn.disabled = !canAfford;
    btn.textContent = canAfford ? 'Купить' : 'Не хватает 🪙';
    $('buyModal').classList.add('show');
}
function closeBuyModal() { $('buyModal').classList.remove('show'); pendingPurchase = null; }
function confirmBuy() {
    if (!pendingPurchase) return;
    const p = PREMIUM[pendingPurchase];
    if (getCoins() < p.price) { toast('Недостаточно монет', 'info', 1500); return; }
    setCoins(getCoins() - p.price);
    setOwned(pendingPurchase);
    haptic(40);
    const screen = p.screen;
    closeBuyModal();
    updatePremiumTags();
    toast('🎉 Игра куплена! Она ваша навсегда', 'success', 2000);
    setTimeout(() => openGame(screen), 400);
}

/* ============================================================
   РЕКЛАМА
============================================================ */
const AD_DURATION = 15;
const AD_REWARD = 40;
const VK_CHANNEL_URL = 'https://vk.com/club239085797';
const VK_VIDEO_URL = 'https://vkvideo.ru/video-239085797_456239018';
const VK_VIDEO_TIME = 'https://vkvideo.ru/video-239085797_456239018?t=43s';
const AD_SLIDES = [
    { icon: '📺', title: 'Dley перезаливы', text: 'Лучшие видео, нарезки и приколы каждый день.', tag: 'VK VIDEO', buttons: [{text: '📺 Подписаться', url: VK_CHANNEL_URL, cls: 'vk'}] },
    { icon: '🎬', title: 'Новые видео каждый день', text: 'Свежие перезаливы популярных роликов!', tag: 'СМОТРЕТЬ', buttons: [{text: '🔥 Смотреть видео', url: VK_VIDEO_URL, cls: 'video'}] },
    { icon: '🔥', title: 'Топ-нарезки недели', text: 'Самое смешное и крутое — в одном канале.', tag: 'VK VIDEO', buttons: [{text: '📺 Подписаться', url: VK_CHANNEL_URL, cls: 'vk'}, {text: '▶ С 43 сек', url: VK_VIDEO_TIME, cls: 'time'}] },
    { icon: '🎮', title: 'Игровые моменты', text: 'Забавные ситуации из игр, реакции и фейлы.', tag: 'СМОТРЕТЬ', buttons: [{text: '🎬 Открыть видео', url: VK_VIDEO_URL, cls: 'video'}] },
    { icon: '💎', title: 'Канал Dley перезаливы', text: 'Тысячи подписчиков уже смотрят. Присоединяйся!', tag: 'ПОДПИСАТЬСЯ', buttons: [{text: '📺 Подписаться на канал', url: VK_CHANNEL_URL, cls: 'vk'}] }
];
let adTimer = null, adSecondsLeft = 0, adSlideIndex = 0, adSlideInterval = null;
function buildAdSlides() {
    const container = $('adSlideContainer');
    container.innerHTML = '';
    AD_SLIDES.forEach((s, i) => {
        const div = document.createElement('div');
        div.className = 'ad-slide' + (i === 0 ? ' active' : '');
        let buttonsHTML = '';
        if (s.buttons && s.buttons.length) {
            buttonsHTML = '<div class="ad-slide-actions">' + s.buttons.map(b => `<a class="ad-slide-btn ${b.cls}" href="${b.url}" target="_blank" rel="noopener noreferrer">${b.text}</a>`).join('') + '</div>';
        }
        div.innerHTML = `
            <div class="ad-slide-icon">${s.icon}</div>
            <div class="ad-slide-title">${s.title}</div>
            <p class="ad-slide-text">${s.text}</p>
            <span class="ad-slide-tag">${s.tag}</span>
            ${buttonsHTML}
        `;
        container.appendChild(div);
    });
}
function buildAdDots() {
    const container = $('adDots');
    container.innerHTML = '';
    AD_SLIDES.forEach((_, i) => {
        const dot = document.createElement('div');
        dot.className = 'ad-dot' + (i === 0 ? ' active' : '');
        container.appendChild(dot);
    });
}
function showAdSlide(index) {
    document.querySelectorAll('.ad-slide').forEach((el, i) => el.classList.toggle('active', i === index));
    document.querySelectorAll('.ad-dot').forEach((el, i) => {
        el.classList.remove('active', 'done');
        if (i === index) el.classList.add('active');
        else if (i < index) el.classList.add('done');
    });
}
function openAdModal() {
    haptic(15);
    buildAdSlides();
    buildAdDots();
    $('adTimerFill').style.width = '0%';
    $('adStatus').innerHTML = `Смотрите рекламу <strong>${AD_DURATION} секунд</strong>`;
    $('adClaimBtn').disabled = true;
    $('adClaimBtn').textContent = 'Получить ' + AD_REWARD + ' 🪙';
    $('adModal').classList.add('show');
    adSecondsLeft = AD_DURATION;
    adSlideIndex = 0;
    showAdSlide(0);
    clearInterval(adSlideInterval);
    adSlideInterval = setInterval(() => {
        adSlideIndex = (adSlideIndex + 1) % AD_SLIDES.length;
        showAdSlide(adSlideIndex);
        haptic(5);
    }, 3000);
    clearInterval(adTimer);
    adTimer = setInterval(() => {
        adSecondsLeft--;
        const pct = ((AD_DURATION - adSecondsLeft) / AD_DURATION) * 100;
        $('adTimerFill').style.width = pct + '%';
        if (adSecondsLeft > 0) $('adStatus').innerHTML = `Осталось: <strong>${adSecondsLeft} сек</strong>`;
        else {
            clearInterval(adTimer);
            clearInterval(adSlideInterval);
            $('adStatus').innerHTML = `✅ Готово! Забирайте награду`;
            $('adClaimBtn').disabled = false;
            haptic(30);
        }
    }, 1000);
}
function closeAdModal() {
    clearInterval(adTimer);
    clearInterval(adSlideInterval);
    $('adModal').classList.remove('show');
}
function claimAdReward() {
    if (adSecondsLeft > 0) return;
    haptic(40);
    addCoins(AD_REWARD, false);
    toast('+' + AD_REWARD + ' 🪙 за просмотр рекламы!', 'ad', 2000);
    closeAdModal();
}

/* ============================================================
   РЕКОРДЫ + НАВИГАЦИЯ
============================================================ */
function tryUpdateRecord(key, value, uiEl, boxEl, format = 'int', lowerIsBetter = false) {
    if (lowerIsBetter && value <= 0) return false;
    const cur = format === 'float' ? getBestFloat(key) : getBest(key);
    const isRecord = lowerIsBetter ? (cur === 0 || value < cur) : (value > cur);
    if (isRecord) {
        localStorage.setItem(key, value);
        if (uiEl) { uiEl.textContent = format === 'float' ? value.toFixed(0) : value; bump(uiEl); }
        if (boxEl) { boxEl.classList.add('record'); setTimeout(() => boxEl.classList.remove('record'), 1200); }
        return true;
    }
    return false;
}
function updateBestScoresUI() {
    const keys = {
        'snake_best': ['snake-best', 'menu-snake-best'],
        '2048_best': ['best2048', 'menu-2048-best'],
        'match3_best': ['match3-best', 'menu-match3-best'],
        'puzzle_best': ['puzzle-best', 'menu-puzzle-best'],
        'arknoid_best': ['arknoid-best', 'menu-arknoid-best'],
        'race_best': ['race-best', 'menu-race-best'],
        'flappy_best': ['flappy-best', 'menu-flappy-best'],
        'shooter_best': ['shooter-best', null],
        'tetris_best': ['tetris-best', null],
        'tower_best': ['tower-best', null]
    };
    for (const k in keys) {
        const [el1, el2] = keys[k];
        const v = getBest(k);
        if (el1 && $(el1)) $(el1).textContent = v;
        if (el2 && $(el2)) $(el2).textContent = v;
    }
    const rBest = getBest('reaction_best');
    const rTxt = rBest > 0 ? rBest + ' мс' : '—';
    $('reaction-best').textContent = rTxt;
    $('menu-reaction-best').textContent = rTxt;
    updateCoinsUI();
    updatePremiumTags();
}
let currentScreen = 'menu-screen';
const screenHooks = {
    'snake-screen': { enter: startSnake, exit: stopSnake },
    'game2048-screen': { enter: start2048, exit: null },
    'match3-screen': { enter: startMatch3, exit: stopMatch3 },
    'reaction-screen': { enter: startReaction, exit: stopReaction },
    'puzzle-screen': { enter: startPuzzle, exit: stopPuzzle },
    'arknoid-screen': { enter: startArknoid, exit: stopArknoid },
    'shooter-screen': { enter: startShooter, exit: stopShooter },
    'tetris-screen': { enter: startTetris, exit: stopTetris },
    'tower-screen': { enter: startTower, exit: stopTower },
    'race-screen': { enter: startRace, exit: stopRace },
    'flappy-screen': { enter: startFlappy, exit: stopFlappy },
    'duel-screen': { enter: startDuel, exit: stopDuel },
    'duel2-screen': { enter: startDuel2, exit: stopDuel2 }
};
function openGame(screenId) {
    haptic(15);
    const hook = screenHooks[screenId];
    if (hook && hook.enter) hook.enter();
    switchScreen(screenId);
}
function closeGame(screenId) {
    haptic(10);
    const hook = screenHooks[screenId];
    if (hook && hook.exit) hook.exit();
    switchScreen('menu-screen');
}
function switchScreen(screenId) {
    document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
    $(screenId).classList.add('active');
    currentScreen = screenId;
    updateBestScoresUI();
}

/* ============================================================
   ЗМЕЙКА
============================================================ */
const sCanvas = $('snakeCanvas');
const sCtx = sCanvas.getContext('2d');
const sScoreEl = $('snake-score');
const sBestEl = $('snake-best');
const sBestBox = $('snake-best-box');
const sGrid = 16;
const sTiles = sCanvas.width / sGrid;
let snake, food, sDx, sDy, sScore, snakeInterval, snakeRunning = false;
function startSnake() {
    snake = [{x: 8, y: 8}]; food = {x: 4, y: 4};
    sDx = 1; sDy = 0; sScore = 0;
    sScoreEl.textContent = '0';
    sBestEl.textContent = getBest('snake_best');
    clearInterval(snakeInterval);
    snakeRunning = true;
    spawnFood();
    snakeInterval = setInterval(updateSnake, 130);
    drawSnake();
}
function stopSnake() { clearInterval(snakeInterval); snakeRunning = false; }
function updateSnake() {
    if (!snakeRunning) return;
    const head = {x: snake[0].x + sDx, y: snake[0].y + sDy};
    const hitWall = head.x < 0 || head.x >= sTiles || head.y < 0 || head.y >= sTiles;
    const hitSelf = snake.some((p, i) => i !== 0 && p.x === head.x && p.y === head.y);
    if (hitWall || hitSelf) { gameOverSnake(); return; }
    snake.unshift(head);
    if (head.x === food.x && head.y === food.y) {
        sScore += 10;
        sScoreEl.textContent = sScore;
        bump(sScoreEl); haptic(20);
        addCoins(1, false);
        if (tryUpdateRecord('snake_best', sScore, sBestEl, sBestBox)) toast('🏆 Новый рекорд: ' + sScore, 'record', 1400);
        spawnFood();
    } else snake.pop();
    drawSnake();
}
function drawSnake() {
    sCtx.fillStyle = '#060a06'; sCtx.fillRect(0, 0, sCanvas.width, sCanvas.height);
    sCtx.strokeStyle = 'rgba(76,175,80,0.05)';
    for (let i = 1; i < sTiles; i++) {
        sCtx.beginPath(); sCtx.moveTo(i*sGrid, 0); sCtx.lineTo(i*sGrid, sCanvas.height); sCtx.stroke();
        sCtx.beginPath(); sCtx.moveTo(0, i*sGrid); sCtx.lineTo(sCanvas.width, i*sGrid); sCtx.stroke();
    }
    const t = performance.now() / 300;
    const pulse = 1 + Math.sin(t) * 0.12;
    const fx = food.x * sGrid + sGrid/2, fy = food.y * sGrid + sGrid/2;
    const fr = (sGrid/2 - 2) * pulse;
    const grad = sCtx.createRadialGradient(fx, fy, 0, fx, fy, fr * 1.6);
    grad.addColorStop(0, '#ff8a65'); grad.addColorStop(1, 'rgba(255,87,34,0)');
    sCtx.fillStyle = grad;
    sCtx.beginPath(); sCtx.arc(fx, fy, fr * 1.6, 0, Math.PI*2); sCtx.fill();
    sCtx.fillStyle = '#ff5722';
    sCtx.beginPath(); sCtx.arc(fx, fy, fr, 0, Math.PI*2); sCtx.fill();
    snake.forEach((p, i) => {
        const x = p.x * sGrid, y = p.y * sGrid;
        const isHead = i === 0;
        const pad = isHead ? 1 : 2;
        sCtx.fillStyle = isHead ? '#a5d6a7' : `hsl(122, 39%, ${45 - Math.min(i*1.5, 20)}%)`;
        roundRect(sCtx, x + pad, y + pad, sGrid - pad*2, sGrid - pad*2, 4);
        sCtx.fill();
    });
}
function spawnFood() {
    do { food.x = Math.floor(Math.random() * sTiles); food.y = Math.floor(Math.random() * sTiles); }
    while (snake.some(p => p.x === food.x && p.y === food.y));
}
function gameOverSnake() {
    stopSnake(); haptic(80);
    toast('Игра окончена. Очки: ' + sScore, 'info', 1600);
    setTimeout(() => { if (currentScreen === 'snake-screen') startSnake(); }, 900);
}
function setSnakeDir(nx, ny) {
    if (!snakeRunning) return;
    if (nx === -sDx && sDx !== 0) return;
    if (ny === -sDy && sDy !== 0) return;
    sDx = nx; sDy = ny; haptic(8);
}

/* ============================================================
   2048
============================================================ */
const canvas2048 = $('canvas2048');
const ctx2048 = canvas2048.getContext('2d');
const score2048El = $('score2048');
const best2048El = $('best2048');
const best2048Box = $('best2048-box');
const size2048 = 4;
const cellW = canvas2048.width / size2048;
const tileColors = {2:'#eee4da',4:'#ede0c8',8:'#f2b179',16:'#f59563',32:'#f67c5f',64:'#f65e3b',128:'#edcf72',256:'#edcc61',512:'#edc850',1024:'#edc53f',2048:'#edc22e'};
let board2048 = [], score2048 = 0, board2048Anim = {}, lastCoinMilestone = 0;
function start2048() {
    board2048 = Array.from({length: size2048}, () => Array(size2048).fill(0));
    score2048 = 0; lastCoinMilestone = 0;
    score2048El.textContent = '0';
    best2048El.textContent = getBest('2048_best');
    addTile2048(); addTile2048();
    drawBoard2048();
}
function addTile2048() {
    const empty = [];
    for (let r = 0; r < size2048; r++) for (let c = 0; c < size2048; c++) if (board2048[r][c] === 0) empty.push({r, c});
    if (!empty.length) return;
    const cell = empty[Math.floor(Math.random() * empty.length)];
    board2048[cell.r][cell.c] = Math.random() < 0.9 ? 2 : 4;
    board2048Anim[cell.r + ',' + cell.c] = performance.now();
}
function drawBoard2048() {
    ctx2048.fillStyle = '#1a1610';
    ctx2048.fillRect(0, 0, canvas2048.width, canvas2048.height);
    for (let r = 0; r < size2048; r++) {
        for (let c = 0; c < size2048; c++) {
            const val = board2048[r][c];
            const x = c * cellW + 5, y = r * cellW + 5, w = cellW - 10;
            ctx2048.fillStyle = 'rgba(255,255,255,0.04)';
            roundRect(ctx2048, x, y, w, w, 8); ctx2048.fill();
            if (val > 0) {
                const key = r + ',' + c;
                const born = board2048Anim[key] || 0;
                const age = (performance.now() - born) / 150;
                const scale = age < 1 ? 0.5 + age * 0.5 : 1;
                ctx2048.save();
                ctx2048.translate(x + w/2, y + w/2);
                ctx2048.scale(scale, scale);
                ctx2048.translate(-(x + w/2), -(y + w/2));
                ctx2048.fillStyle = tileColors[val] || '#3c3a32';
                roundRect(ctx2048, x, y, w, w, 8); ctx2048.fill();
                ctx2048.fillStyle = (val === 2 || val === 4) ? '#776e65' : '#f9f6f2';
                const fontSize = val > 1000 ? 18 : val > 100 ? 22 : 28;
                ctx2048.font = `bold ${fontSize}px system-ui, sans-serif`;
                ctx2048.textAlign = 'center'; ctx2048.textBaseline = 'middle';
                ctx2048.fillText(val, x + w/2, y + w/2 + 1);
                ctx2048.restore();
            }
        }
    }
}
function move2048(dir) {
    if (currentScreen !== 'game2048-screen') return;
    haptic(8);
    let moved = false;
    if (dir === 'right') { reverseBoard(); moved = slideLeft(); reverseBoard(); }
    else if (dir === 'left') { moved = slideLeft(); }
    else if (dir === 'up') { transposeBoard(); moved = slideLeft(); transposeBoard(); }
    else if (dir === 'down') { transposeBoard(); reverseBoard(); moved = slideLeft(); reverseBoard(); transposeBoard(); }
    if (moved) {
        addTile2048();
        score2048El.textContent = score2048;
        bump(score2048El);
        const milestone = Math.floor(score2048 / 50);
        if (milestone > lastCoinMilestone) { addCoins(milestone - lastCoinMilestone, false); lastCoinMilestone = milestone; }
        if (tryUpdateRecord('2048_best', score2048, best2048El, best2048Box)) toast('🏆 Новый рекорд: ' + score2048, 'record', 1400);
        drawBoard2048();
        if (isGameOver2048()) {
            haptic(80);
            toast('Игра окончена. Счет: ' + score2048, 'info', 1800);
            setTimeout(() => { if (currentScreen === 'game2048-screen') start2048(); }, 1100);
        }
    }
}
function slideLeft() {
    let moved = false;
    for (let r = 0; r < size2048; r++) {
        let row = board2048[r].filter(v => v !== 0);
        for (let i = 0; i < row.length - 1; i++) if (row[i] === row[i + 1]) { row[i] *= 2; score2048 += row[i]; row.splice(i + 1, 1); moved = true; }
        while (row.length < size2048) row.push(0);
        if (JSON.stringify(board2048[r]) !== JSON.stringify(row)) moved = true;
        board2048[r] = row;
    }
    return moved;
}
function reverseBoard() { board2048.forEach(r => r.reverse()); }
function transposeBoard() { board2048 = board2048.map((_, i) => board2048.map(row => row[i])); }
function isGameOver2048() {
    for (let r = 0; r < size2048; r++) for (let c = 0; c < size2048; c++) {
        if (board2048[r][c] === 0) return false;
        if (c < size2048 - 1 && board2048[r][c] === board2048[r][c+1]) return false;
        if (r < size2048 - 1 && board2048[r][c] === board2048[r+1][c]) return false;
    }
    return true;
}

/* ============================================================
   3 В РЯД
============================================================ */
const mCanvas = $('match3Canvas');
const mCtx = mCanvas.getContext('2d');
const mScoreEl = $('match3-score');
const mBestEl = $('match3-best');
const mBestBox = $('match3-best-box');
const mSize = 6;
const mCell = mCanvas.width / mSize;
const gemColors = ['#e91e63', '#2196f3', '#4caf50', '#ffeb3b', '#9c27b0', '#ff9800'];
let mBoard = [], mScore = 0, selR = 0, selC = 0, mInterval, mRunning = false;
let mParticles = [], mFirstTap = null, mCoinMilestoneM3 = 0;
function startMatch3() {
    mScore = 0; mScoreEl.textContent = '0';
    mBestEl.textContent = getBest('match3_best');
    selR = 0; selC = 0; mFirstTap = null; mCoinMilestoneM3 = 0; mParticles = [];
    initMatch3Board();
    clearInterval(mInterval);
    mRunning = true;
    mInterval = setInterval(drawMatch3, 60);
    drawMatch3();
}
function stopMatch3() { clearInterval(mInterval); mRunning = false; }
function initMatch3Board() {
    for (let r = 0; r < mSize; r++) {
        mBoard[r] = [];
        for (let c = 0; c < mSize; c++) {
            let idx, guard = 0;
            do { idx = Math.floor(Math.random() * gemColors.length); guard++; }
            while (guard < 50 && ((c >= 2 && mBoard[r][c-1] === idx && mBoard[r][c-2] === idx) || (r >= 2 && mBoard[r-1][c] === idx && mBoard[r-2][c] === idx)));
            mBoard[r][c] = idx;
        }
    }
    if (checkMatchesMatch3()) initMatch3Board();
}
let blinkPhase = 0;
function drawMatch3() {
    if (!mRunning) return;
    blinkPhase += 0.08;
    mCtx.fillStyle = '#100812';
    mCtx.fillRect(0, 0, mCanvas.width, mCanvas.height);
    mCtx.strokeStyle = 'rgba(156,39,176,0.08)';
    for (let i = 1; i < mSize; i++) {
        mCtx.beginPath(); mCtx.moveTo(i * mCell, 0); mCtx.lineTo(i * mCell, mCanvas.height); mCtx.stroke();
        mCtx.beginPath(); mCtx.moveTo(0, i * mCell); mCtx.lineTo(mCanvas.width, i * mCell); mCtx.stroke();
    }
    for (let r = 0; r < mSize; r++) {
        for (let c = 0; c < mSize; c++) {
            const color = gemColors[mBoard[r][c]];
            const cx = c * mCell + mCell / 2, cy = r * mCell + mCell / 2;
            const radius = mCell / 2 - 7;
            const glow = mCtx.createRadialGradient(cx, cy, 0, cx, cy, radius * 1.8);
            glow.addColorStop(0, color + '55'); glow.addColorStop(1, 'rgba(0,0,0,0)');
            mCtx.fillStyle = glow;
            mCtx.beginPath(); mCtx.arc(cx, cy, radius * 1.8, 0, Math.PI * 2); mCtx.fill();
            mCtx.fillStyle = color;
            mCtx.beginPath(); mCtx.arc(cx, cy, radius, 0, Math.PI * 2); mCtx.fill();
            mCtx.fillStyle = 'rgba(255,255,255,0.35)';
            mCtx.beginPath(); mCtx.arc(cx - radius * 0.3, cy - radius * 0.3, radius * 0.35, 0, Math.PI * 2); mCtx.fill();
            if (r === selR && c === selC) {
                const a = 0.6 + Math.sin(blinkPhase * 6) * 0.4;
                mCtx.strokeStyle = `rgba(255,255,255,${a})`;
                mCtx.lineWidth = 3;
                mCtx.beginPath(); mCtx.arc(cx, cy, radius + 3, 0, Math.PI * 2); mCtx.stroke();
            }
        }
    }
    for (let i = mParticles.length - 1; i >= 0; i--) {
        const p = mParticles[i];
        p.x += p.vx; p.y += p.vy; p.vy += 0.15; p.life -= 0.02;
        if (p.life <= 0) { mParticles.splice(i, 1); continue; }
        mCtx.globalAlpha = p.life;
        mCtx.fillStyle = p.color;
        mCtx.beginPath(); mCtx.arc(p.x, p.y, p.size, 0, Math.PI * 2); mCtx.fill();
    }
    mCtx.globalAlpha = 1;
}
function trySwap(r1, c1, r2, c2) {
    if (Math.abs(r1 - r2) + Math.abs(c1 - c2) !== 1) return false;
    [mBoard[r1][c1], mBoard[r2][c2]] = [mBoard[r2][c2], mBoard[r1][c1]];
    if (!checkMatchesMatch3()) { [mBoard[r1][c1], mBoard[r2][c2]] = [mBoard[r2][c2], mBoard[r1][c1]]; return false; }
    return true;
}
function moveMatch3(dir) {
    if (!mRunning || currentScreen !== 'match3-screen') return;
    haptic(10);
    let nr = selR, nc = selC;
    if (dir === 'up') nr--; else if (dir === 'down') nr++; else if (dir === 'left') nc--; else if (dir === 'right') nc++;
    if (nr < 0 || nr >= mSize || nc < 0 || nc >= mSize) return;
    if (!trySwap(selR, selC, nr, nc)) { toast('Нет линии из 3', 'info', 900); return; }
    selR = nr; selC = nc;
    processMatches();
}
function match3Tap(r, c) {
    if (!mRunning) return;
    if (r < 0 || r >= mSize || c < 0 || c >= mSize) return;
    if (mFirstTap === null) { selR = r; selC = c; mFirstTap = {r, c}; haptic(8); return; }
    if (mFirstTap.r === r && mFirstTap.c === c) { mFirstTap = null; haptic(8); return; }
    if (trySwap(mFirstTap.r, mFirstTap.c, r, c)) { selR = r; selC = c; mFirstTap = null; haptic(15); processMatches(); }
    else { selR = r; selC = c; mFirstTap = {r, c}; haptic(8); }
}
function checkMatchesMatch3() {
    for (let r = 0; r < mSize; r++) for (let c = 0; c < mSize; c++) {
        if (c < mSize - 2 && mBoard[r][c] === mBoard[r][c+1] && mBoard[r][c] === mBoard[r][c+2]) return true;
        if (r < mSize - 2 && mBoard[r][c] === mBoard[r+1][c] && mBoard[r][c] === mBoard[r+2][c]) return true;
    }
    return false;
}
function processMatches() {
    const toRemove = Array.from({length: mSize}, () => Array(mSize).fill(false));
    for (let r = 0; r < mSize; r++) for (let c = 0; c < mSize; c++) {
        if (c < mSize - 2 && mBoard[r][c] === mBoard[r][c+1] && mBoard[r][c] === mBoard[r][c+2]) toRemove[r][c] = toRemove[r][c+1] = toRemove[r][c+2] = true;
        if (r < mSize - 2 && mBoard[r][c] === mBoard[r+1][c] && mBoard[r][c] === mBoard[r+2][c]) toRemove[r][c] = toRemove[r+1][c] = toRemove[r+2][c] = true;
    }
    let removed = 0;
    for (let r = 0; r < mSize; r++) for (let c = 0; c < mSize; c++) if (toRemove[r][c]) removed++;
    if (removed === 0) return;
    for (let r = 0; r < mSize; r++) for (let c = 0; c < mSize; c++) if (toRemove[r][c]) {
        const color = gemColors[mBoard[r][c]];
        const cx = c * mCell + mCell / 2, cy = r * mCell + mCell / 2;
        for (let k = 0; k < 4; k++) mParticles.push({ x: cx, y: cy, vx: (Math.random() - 0.5) * 4, vy: (Math.random() - 0.5) * 4 - 1, life: 1, size: 2 + Math.random() * 2, color });
    }
    for (let c = 0; c < mSize; c++) {
        let writeRow = mSize - 1;
        for (let r = mSize - 1; r >= 0; r--) if (!toRemove[r][c]) { mBoard[writeRow][c] = mBoard[r][c]; writeRow--; }
        for (let r = writeRow; r >= 0; r--) mBoard[r][c] = Math.floor(Math.random() * gemColors.length);
    }
    mScore += removed * 10;
    mScoreEl.textContent = mScore;
    bump(mScoreEl); haptic(20);
    const milestone = Math.floor(mScore / 30);
    if (milestone > mCoinMilestoneM3) { addCoins(milestone - mCoinMilestoneM3, false); mCoinMilestoneM3 = milestone; }
    if (tryUpdateRecord('match3_best', mScore, mBestEl, mBestBox)) toast('🏆 Новый рекорд: ' + mScore, 'record', 1400);
    setTimeout(() => { if (mRunning) processMatches(); }, 280);
}
function match3Click(e) {
    if (!mRunning) return;
    const rect = mCanvas.getBoundingClientRect();
    const x = (e.clientX - rect.left) * (mCanvas.width / rect.width);
    const y = (e.clientY - rect.top) * (mCanvas.height / rect.height);
    match3Tap(Math.floor(y / mCell), Math.floor(x / mCell));
}

/* ============================================================
   РЕАКЦИЯ
============================================================ */
const rCanvas = $('reactionCanvas');
const rCtx = rCanvas.getContext('2d');
const rTimeEl = $('reaction-time');
const rBestEl = $('reaction-best');
const rBestBox = $('reaction-best-box');
const rBtn = $('reactionBtn');
let rState = 'idle', rStartTime = 0, rTimeout = null;
function startReaction() {
    rState = 'idle';
    rTimeEl.textContent = '—';
    rBestEl.textContent = getBest('reaction_best') > 0 ? getBest('reaction_best') + ' мс' : '—';
    rBtn.textContent = 'СТАРТ';
    drawReactionIdle();
    clearTimeout(rTimeout);
}
function stopReaction() { clearTimeout(rTimeout); rState = 'idle'; }
function drawReactionIdle() {
    rCtx.fillStyle = '#041014'; rCtx.fillRect(0, 0, rCanvas.width, rCanvas.height);
    rCtx.fillStyle = 'rgba(0,188,212,0.4)'; rCtx.font = 'bold 22px system-ui, sans-serif';
    rCtx.textAlign = 'center'; rCtx.textBaseline = 'middle';
    rCtx.fillText('НАЖМИТЕ СТАРТ', rCanvas.width/2, rCanvas.height/2);
}
function drawReactionState(color, text) {
    rCtx.fillStyle = color; rCtx.fillRect(0, 0, rCanvas.width, rCanvas.height);
    rCtx.fillStyle = '#ffffff'; rCtx.font = 'bold 32px system-ui, sans-serif';
    rCtx.textAlign = 'center'; rCtx.textBaseline = 'middle';
    rCtx.fillText(text, rCanvas.width/2, rCanvas.height/2);
}
function reactionTap(e) {
    if (e) e.preventDefault();
    haptic(15);
    if (rState === 'idle') {
        rState = 'waiting';
        rBtn.textContent = 'ЖДИТЕ...';
        drawReactionState('#b71c1c', 'ЖДИТЕ...');
        rTimeout = setTimeout(() => {
            if (rState !== 'waiting') return;
            rState = 'ready'; rStartTime = performance.now();
            drawReactionState('#1b5e20', 'ЖМИ!');
            rBtn.textContent = 'ЖМИ!';
            haptic(40);
        }, 1500 + Math.random() * 2500);
    } else if (rState === 'waiting') {
        clearTimeout(rTimeout);
        rState = 'idle';
        drawReactionState('#4a148c', 'РАНО!');
        toast('Слишком рано!', 'info', 1200);
        rBtn.textContent = 'ПОПРОБОВАТЬ СНОВА';
        haptic(60);
    } else if (rState === 'ready') {
        const t = Math.round(performance.now() - rStartTime);
        rState = 'done';
        rTimeEl.textContent = t + ' мс';
        bump(rTimeEl);
        drawReactionState('#0d47a1', t + ' мс');
        rBtn.textContent = 'ЕЩЁ РАЗ';
        haptic(30);
        const coins = t < 250 ? 5 : t < 400 ? 3 : t < 600 ? 1 : 0;
        if (coins > 0) addCoins(coins, false);
        if (tryUpdateRecord('reaction_best', t, rBestEl, rBestBox, 'int', true)) toast('🏆 Новый рекорд: ' + t + ' мс!', 'record', 1600);
        else if (coins > 0) toast('+' + coins + ' 🪙', 'coin', 1000);
    } else if (rState === 'done') startReaction();
}

/* ============================================================
   ПЯТНАШКИ
============================================================ */
const pCanvas = $('puzzleCanvas');
const pCtx = pCanvas.getContext('2d');
const pMovesEl = $('puzzle-moves');
const pBestEl = $('puzzle-best');
const pBestBox = $('puzzle-best-box');
const pSize = 3, pTotal = pSize * pSize, pCell = pCanvas.width / pSize;
let pBoard = [], pMoves = 0, pSolved = false;
function startPuzzle() {
    pMoves = 0; pMovesEl.textContent = '0';
    pBestEl.textContent = getBest('puzzle_best') || 0;
    pSolved = false;
    shufflePuzzle();
    drawPuzzle();
}
function stopPuzzle() {}
function shufflePuzzle() {
    haptic(15);
    pBoard = [];
    for (let i = 0; i < pTotal; i++) pBoard.push(i);
    let emptyIdx = pTotal - 1;
    const steps = 80 + Math.floor(Math.random() * 40);
    for (let s = 0; s < steps; s++) {
        const neighbors = getNeighbors(emptyIdx);
        const pick = neighbors[Math.floor(Math.random() * neighbors.length)];
        [pBoard[emptyIdx], pBoard[pick]] = [pBoard[pick], pBoard[emptyIdx]];
        emptyIdx = pick;
    }
    pMoves = 0; pMovesEl.textContent = '0'; pSolved = false;
    drawPuzzle();
}
function getNeighbors(idx) {
    const r = Math.floor(idx / pSize), c = idx % pSize;
    const out = [];
    if (r > 0) out.push(idx - pSize);
    if (r < pSize - 1) out.push(idx + pSize);
    if (c > 0) out.push(idx - 1);
    if (c < pSize - 1) out.push(idx + 1);
    return out;
}
function drawPuzzle() {
    pCtx.fillStyle = '#140606';
    pCtx.fillRect(0, 0, pCanvas.width, pCanvas.height);
    const pad = 5, w = pCell - pad * 2;
    for (let i = 0; i < pTotal; i++) {
        const val = pBoard[i];
        const r = Math.floor(i / pSize), c = i % pSize;
        const x = c * pCell + pad, y = r * pCell + pad;
        if (val === 0) { pCtx.fillStyle = 'rgba(255,255,255,0.03)'; roundRect(pCtx, x, y, w, w, 10); pCtx.fill(); continue; }
        const isCorrect = val === i + 1;
        const grad = pCtx.createLinearGradient(x, y, x + w, y + w);
        if (isCorrect) { grad.addColorStop(0, '#66bb6a'); grad.addColorStop(1, '#2e7d32'); }
        else { grad.addColorStop(0, '#ef5350'); grad.addColorStop(1, '#b71c1c'); }
        pCtx.fillStyle = grad;
        roundRect(pCtx, x, y, w, w, 10); pCtx.fill();
        pCtx.fillStyle = 'rgba(255,255,255,0.15)';
        roundRect(pCtx, x + 4, y + 4, w - 8, w * 0.35, 6); pCtx.fill();
        pCtx.fillStyle = '#fff';
        pCtx.font = 'bold 32px system-ui, sans-serif';
        pCtx.textAlign = 'center'; pCtx.textBaseline = 'middle';
        pCtx.fillText(val, x + w/2, y + w/2 + 2);
    }
}
function puzzleClick(e) {
    if (pSolved) return;
    const rect = pCanvas.getBoundingClientRect();
    const x = (e.clientX - rect.left) * (pCanvas.width / rect.width);
    const y = (e.clientY - rect.top) * (pCanvas.height / rect.height);
    const c = Math.floor(x / pCell), r = Math.floor(y / pCell);
    if (r < 0 || r >= pSize || c < 0 || c >= pSize) return;
    const idx = r * pSize + c;
    const emptyIdx = pBoard.indexOf(0);
    if (!getNeighbors(emptyIdx).includes(idx)) return;
    [pBoard[emptyIdx], pBoard[idx]] = [pBoard[idx], pBoard[emptyIdx]];
    pMoves++; pMovesEl.textContent = pMoves; bump(pMovesEl); haptic(10);
    drawPuzzle();
    if (isPuzzleSolved()) {
        pSolved = true; haptic(60);
        const coins = pMoves <= 30 ? 20 : pMoves <= 60 ? 10 : 5;
        addCoins(coins, false);
        if (tryUpdateRecord('puzzle_best', pMoves, pBestEl, pBestBox, 'int', true)) toast('🏆 Рекорд: ' + pMoves + ' ходов! +' + coins + '🪙', 'record', 2000);
        else toast('Собрано за ' + pMoves + ' ходов! +' + coins + '🪙', 'success', 1800);
    }
}
function isPuzzleSolved() {
    for (let i = 0; i < pTotal - 1; i++) if (pBoard[i] !== i + 1) return false;
    return pBoard[pTotal - 1] === 0;
}

/* ============================================================
   АРКАНОИД
============================================================ */
const arkCanvas = $('arknoidCanvas');
const arkCtx = arkCanvas.getContext('2d');
const arkScoreEl = $('arknoid-score');
const arkLevelEl = $('arknoid-level');
const arkBestEl = $('arknoid-best');
const arkBestBox = $('arknoid-best-box');
const ARK_W = arkCanvas.width, ARK_H = arkCanvas.height;
const ARK_PADDLE_H = 12, ARK_PADDLE_Y = ARK_H - 30;
const ARK_BALL_R = 6;
const ARK_BRICK_ROWS = 5, ARK_BRICK_COLS = 8;
const ARK_BRICK_H = 18, ARK_BRICK_GAP = 4, ARK_BRICK_TOP = 50, ARK_BRICK_SIDE = 8;
const ARK_MAX_LEVEL = 10;
const ARK_POWERUP_TYPES = ['expand', 'sticky', 'multi', 'laser'];
const ARK_POWERUP_COLORS = { expand: '#66bb6a', sticky: '#ffffff', multi: '#42a5f5', laser: '#ef5350' };
const ARK_POWERUP_ICONS = { expand: '⬌', sticky: '⊛', multi: '●●●', laser: '⌇' };
let arkRunning = false, arkFrameId = null, arkLastTime = 0;
let arkPaddleX = ARK_W / 2, arkPaddleW = 70, arkDir = 0;
let arkBalls = [];
let arkBricks = [], arkScore = 0, arkLevel = 1, arkLives = 3;
let arkPaused = false, arkCoinMilestone = 0, arkParticles = [];
let arkPowerups = [];
let arkActiveEffects = {};
let arkSticky = false;
let arkLaserTime = 0;
let arkLaserCooldown = 0;
let arkBossActive = null;
let arkMoveTimer = 0;
const ARK_BRICK_COLORS = ['#e53935', '#fb8c00', '#fdd835', '#43a047', '#1e88e5', '#8e24aa'];
function startArknoid() {
    arkPaddleX = ARK_W / 2; arkPaddleW = 70; arkDir = 0;
    arkScore = 0; arkLevel = 1; arkLives = 3;
    arkPaused = false; arkCoinMilestone = 0; arkParticles = [];
    arkPowerups = []; arkActiveEffects = {};
    arkSticky = false; arkLaserTime = 0; arkLaserCooldown = 0;
    arkBossActive = null; arkMoveTimer = 0;
    arkScoreEl.textContent = '0';
    arkLevelEl.textContent = '1';
    arkBestEl.textContent = getBest('arknoid_best');
    buildArknoidLevel(1);
    resetArknoidBall();
    arkRunning = true;
    arkLastTime = performance.now();
    if (arkFrameId) cancelAnimationFrame(arkFrameId);
    arkFrameId = requestAnimationFrame(arknoidLoop);
}
function stopArknoid() { arkRunning = false; if (arkFrameId) cancelAnimationFrame(arkFrameId); arkFrameId = null; }
function resetArknoidBall() {
    arkBalls = [{ x: arkPaddleX, y: ARK_PADDLE_Y - ARK_BALL_R - 2, vx: 0, vy: 0, launched: false }];
}
function launchArknoidBall() {
    const ball = arkBalls[0];
    if (!ball || ball.launched) return;
    const angle = (-60 + Math.random() * 120) * Math.PI / 180;
    const speed = 4.2 + arkLevel * 0.15;
    ball.vx = Math.sin(angle) * speed;
    ball.vy = -Math.abs(Math.cos(angle) * speed);
    if (Math.abs(ball.vx) < 1.5) ball.vx = ball.vx > 0 ? 1.5 : -1.5;
    ball.launched = true;
    haptic(15);
}
function buildArknoidLevel(level) {
    arkBricks = []; arkBossActive = null;
    if (level % 5 === 0) {
        arkBossActive = { x: ARK_W / 2 - 60, y: 60, w: 120, h: 50, hp: 20 + level * 5, maxHp: 20 + level * 5, color: '#ff4081', dir: 1, shootTimer: 0 };
        for (let c = 0; c < ARK_BRICK_COLS; c++) {
            arkBricks.push({
                x: ARK_BRICK_SIDE + c * ((ARK_W - ARK_BRICK_SIDE * 2) / ARK_BRICK_COLS),
                y: 130,
                w: (ARK_W - ARK_BRICK_SIDE * 2) / ARK_BRICK_COLS - ARK_BRICK_GAP,
                h: ARK_BRICK_H, hp: 2, maxHp: 2, color: '#9c27b0', points: 10
            });
        }
        return;
    }
    const totalW = ARK_W - ARK_BRICK_SIDE * 2;
    const brickW = (totalW - ARK_BRICK_GAP * (ARK_BRICK_COLS - 1)) / ARK_BRICK_COLS;
    const layout = (level - 1) % 4;
    for (let r = 0; r < ARK_BRICK_ROWS; r++) {
        for (let c = 0; c < ARK_BRICK_COLS; c++) {
            let skip = false;
            if (layout === 1 && ((r + c) % 2 === 0)) skip = true;
            if (layout === 2 && (c >= 3 && c <= 4)) skip = true;
            if (layout === 3 && r === 2) skip = true;
            if (skip) continue;
            const hp = Math.min(3, 1 + Math.floor((ARK_BRICK_ROWS - 1 - r) / 2) + (level > 3 ? 1 : 0));
            arkBricks.push({
                x: ARK_BRICK_SIDE + c * (brickW + ARK_BRICK_GAP),
                y: ARK_BRICK_TOP + r * (ARK_BRICK_H + ARK_BRICK_GAP),
                w: brickW, h: ARK_BRICK_H,
                hp: hp, maxHp: hp,
                color: ARK_BRICK_COLORS[r % ARK_BRICK_COLORS.length],
                points: (ARK_BRICK_ROWS - r) * 5 * hp
            });
        }
    }
}
function arknoidControl(action) {
    if (!arkRunning) return;
    if (action === 'left') { arkDir = -1; haptic(6); }
    else if (action === 'right') { arkDir = 1; haptic(6); }
    else if (action === 'fire') { launchArknoidBall(); haptic(10); }
    else if (action === 'pause') { arkPaused = !arkPaused; haptic(10); }
}
function arknoidLoop(t) {
    if (!arkRunning) return;
    const dt = Math.min(40, t - arkLastTime);
    arkLastTime = t;
    if (!arkPaused) updateArknoid(dt, t);
    drawArknoid();
    arkFrameId = requestAnimationFrame(arknoidLoop);
}
function arknoidScoreAdd(points) {
    arkScore += points;
    arkScoreEl.textContent = arkScore;
    bump(arkScoreEl);
    const ms = Math.floor(arkScore / 30);
    if (ms > arkCoinMilestone) { addCoins(ms - arkCoinMilestone, false); arkCoinMilestone = ms; }
    if (tryUpdateRecord('arknoid_best', arkScore, arkBestEl, arkBestBox)) toast('🏆 Новый рекорд: ' + arkScore, 'record', 1400);
}
function arknoidSpawnPowerup(x, y) {
    if (Math.random() < 0.18) {
        const type = ARK_POWERUP_TYPES[Math.floor(Math.random() * ARK_POWERUP_TYPES.length)];
        arkPowerups.push({ x, y, type, vy: 2.2 });
    }
}
function applyArknoidPowerup(type) {
    haptic(20);
    if (type === 'expand') { arkPaddleW = Math.min(130, arkPaddleW + 30); arkActiveEffects.expand = performance.now() + 10000; toast('🟢 Платформа расширена!', 'success', 1200); }
    else if (type === 'sticky') { arkSticky = true; arkActiveEffects.sticky = performance.now() + 10000; toast('⚪ Липкая платформа!', 'success', 1200); }
    else if (type === 'multi') {
        const base = arkBalls[0];
        if (base && base.launched) {
            for (let i = 0; i < 2; i++) {
                const angle = (Math.random() - 0.5) * Math.PI / 2;
                const speed = Math.hypot(base.vx, base.vy) || 5;
                arkBalls.push({ x: base.x, y: base.y, vx: Math.sin(angle) * speed, vy: -Math.abs(Math.cos(angle) * speed), launched: true });
            }
            toast('🔵 Мультимяч!', 'success', 1200);
        } else toast('🔵 Бонус активируется при запуске', 'info', 1200);
    }
    else if (type === 'laser') { arkLaserTime = performance.now() + 8000; toast('🔴 Лазер! Жмите 🔥', 'success', 1200); }
}
function updateArknoid(dt, t) {
    arkPaddleX += arkDir * 0.45 * dt;
    arkPaddleX = Math.max(arkPaddleW/2, Math.min(ARK_W - arkPaddleW/2, arkPaddleX));
    if (arkActiveEffects.expand && t > arkActiveEffects.expand) { arkPaddleW = 70; delete arkActiveEffects.expand; }
    if (arkActiveEffects.sticky && t > arkActiveEffects.sticky) { arkSticky = false; delete arkActiveEffects.sticky; }
    if (arkLaserTime && t > arkLaserTime) arkLaserTime = 0;
    if (arkLaserTime > 0 && t - arkLaserCooldown > 200) {
        arkLaserCooldown = t;
        for (const dx of [-arkPaddleW/2 + 4, arkPaddleW/2 - 4]) {
            const bx = arkPaddleX + dx;
            for (let i = arkBricks.length - 1; i >= 0; i--) {
                const b = arkBricks[i];
                if (bx > b.x && bx < b.x + b.w && b.y > ARK_PADDLE_Y - 200) {
                    b.hp--;
                    for (let k = 0; k < 3; k++) arkParticles.push({x: bx, y: b.y + b.h/2, vx: (Math.random() - 0.5) * 3, vy: (Math.random() - 0.5) * 3, life: 1, size: 2, color: '#ef5350'});
                    if (b.hp <= 0) { arknoidScoreAdd(b.points); arknoidSpawnPowerup(b.x + b.w/2, b.y + b.h/2); arkBricks.splice(i, 1); }
                    break;
                }
            }
            if (arkBossActive) {
                const boss = arkBossActive;
                if (bx > boss.x && bx < boss.x + boss.w) {
                    boss.hp--;
                    for (let k = 0; k < 3; k++) arkParticles.push({x: bx, y: boss.y + boss.h/2, vx: (Math.random() - 0.5) * 3, vy: (Math.random() - 0.5) * 3, life: 1, size: 2, color: '#ff4081'});
                    if (boss.hp <= 0) {
                        arknoidScoreAdd(200);
                        for (let k = 0; k < 30; k++) arkParticles.push({x: boss.x + Math.random() * boss.w, y: boss.y + Math.random() * boss.h, vx: (Math.random() - 0.5) * 6, vy: (Math.random() - 0.5) * 6, life: 1, size: 3, color: '#ff4081'});
                        addCoins(15, false);
                        toast('🎉 Босс повержен! +200', 'success', 1800);
                        haptic(80);
                        arkBossActive = null;
                    }
                    break;
                }
            }
        }
    }
    for (let bi = arkBalls.length - 1; bi >= 0; bi--) {
        const ball = arkBalls[bi];
        if (!ball.launched) { ball.x = arkPaddleX; ball.y = ARK_PADDLE_Y - ARK_BALL_R - 2; }
        else {
            ball.x += ball.vx * dt * 0.06;
            ball.y += ball.vy * dt * 0.06;
            if (ball.x < ARK_BALL_R) { ball.x = ARK_BALL_R; ball.vx = Math.abs(ball.vx); }
            if (ball.x > ARK_W - ARK_BALL_R) { ball.x = ARK_W - ARK_BALL_R; ball.vx = -Math.abs(ball.vx); }
            if (ball.y < ARK_BALL_R) { ball.y = ARK_BALL_R; ball.vy = Math.abs(ball.vy); }
            if (ball.y + ARK_BALL_R > ARK_PADDLE_Y && ball.y - ARK_BALL_R < ARK_PADDLE_Y + ARK_PADDLE_H &&
                ball.x > arkPaddleX - arkPaddleW/2 - ARK_BALL_R && ball.x < arkPaddleX + arkPaddleW/2 + ARK_BALL_R && ball.vy > 0) {
                ball.y = ARK_PADDLE_Y - ARK_BALL_R;
                const rel = (ball.x - arkPaddleX) / (arkPaddleW/2);
                const angle = rel * Math.PI / 3;
                const speed = Math.min(7.5, Math.hypot(ball.vx, ball.vy) + 0.02);
                ball.vx = Math.sin(angle) * speed;
                ball.vy = -Math.abs(Math.cos(angle) * speed);
                if (arkSticky) { ball.launched = false; ball.vx = 0; ball.vy = 0; ball.y = ARK_PADDLE_Y - ARK_BALL_R - 2; haptic(12); continue; }
                haptic(6);
            }
            let brickHit = false;
            for (let i = arkBricks.length - 1; i >= 0; i--) {
                const b = arkBricks[i];
                if (ball.x + ARK_BALL_R > b.x && ball.x - ARK_BALL_R < b.x + b.w && ball.y + ARK_BALL_R > b.y && ball.y - ARK_BALL_R < b.y + b.h) {
                    const oL = (ball.x + ARK_BALL_R) - b.x, oR = (b.x + b.w) - (ball.x - ARK_BALL_R);
                    const oT = (ball.y + ARK_BALL_R) - b.y, oB = (b.y + b.h) - (ball.y - ARK_BALL_R);
                    const minOv = Math.min(oL, oR, oT, oB);
                    if (minOv === oL || minOv === oR) ball.vx = -ball.vx; else ball.vy = -ball.vy;
                    b.hp--;
                    for (let k = 0; k < 4; k++) arkParticles.push({x: b.x + b.w/2, y: b.y + b.h/2, vx: (Math.random() - 0.5) * 3, vy: (Math.random() - 0.5) * 3, life: 1, size: 2, color: b.color});
                    haptic(8);
                    if (b.hp <= 0) { arknoidScoreAdd(b.points); arknoidSpawnPowerup(b.x + b.w/2, b.y + b.h/2); arkBricks.splice(i, 1); }
                    brickHit = true;
                    break;
                }
            }
            if (!brickHit && arkBossActive) {
                const boss = arkBossActive;
                if (ball.x + ARK_BALL_R > boss.x && ball.x - ARK_BALL_R < boss.x + boss.w && ball.y + ARK_BALL_R > boss.y && ball.y - ARK_BALL_R < boss.y + boss.h) {
                    const oL = (ball.x + ARK_BALL_R) - boss.x, oR = (boss.x + boss.w) - (ball.x - ARK_BALL_R);
                    const oT = (ball.y + ARK_BALL_R) - boss.y, oB = (boss.y + boss.h) - (ball.y - ARK_BALL_R);
                    const minOv = Math.min(oL, oR, oT, oB);
                    if (minOv === oL || minOv === oR) ball.vx = -ball.vx; else ball.vy = -ball.vy;
                    boss.hp--;
                    for (let k = 0; k < 6; k++) arkParticles.push({x: ball.x, y: ball.y, vx: (Math.random() - 0.5) * 4, vy: (Math.random() - 0.5) * 4, life: 1, size: 2, color: '#ff4081'});
                    haptic(10);
                    if (boss.hp <= 0) {
                        arknoidScoreAdd(200);
                        for (let k = 0; k < 30; k++) arkParticles.push({x: boss.x + Math.random() * boss.w, y: boss.y + Math.random() * boss.h, vx: (Math.random() - 0.5) * 6, vy: (Math.random() - 0.5) * 6, life: 1, size: 3, color: '#ff4081'});
                        addCoins(15, false);
                        toast('🎉 Босс повержен! +200', 'success', 1800);
                        haptic(80);
                        arkBossActive = null;
                    }
                }
            }
            if (ball.y > ARK_H + 20) {
                arkBalls.splice(bi, 1);
                if (arkBalls.length === 0) {
                    arkLives--;
                    haptic(80);
                    if (arkLives <= 0) { gameOverArknoid(); return; }
                    toast('💔 Потерян мяч! Осталось: ' + arkLives, 'info', 1000);
                    resetArknoidBall();
                }
            }
        }
    }
    for (let i = arkPowerups.length - 1; i >= 0; i--) {
        const p = arkPowerups[i];
        p.y += p.vy * dt * 0.06;
        if (p.y > ARK_H + 20) { arkPowerups.splice(i, 1); continue; }
        if (Math.abs(p.x - arkPaddleX) < arkPaddleW/2 + 10 && Math.abs(p.y - ARK_PADDLE_Y) < 20) { applyArknoidPowerup(p.type); arkPowerups.splice(i, 1); }
    }
    if (arkBossActive) {
        const boss = arkBossActive;
        boss.x += boss.dir * 0.8 * dt * 0.06;
        if (boss.x < 10) { boss.x = 10; boss.dir = 1; }
        if (boss.x + boss.w > ARK_W - 10) { boss.x = ARK_W - 10 - boss.w; boss.dir = -1; }
        boss.shootTimer += dt;
        if (boss.shootTimer > 1200) boss.shootTimer = 0;
    }
    if (arkLevel > 2 && arkBricks.length > 0) {
        arkMoveTimer += dt;
        if (arkMoveTimer > 2000) {
            arkMoveTimer = 0;
            const shift = Math.random() < 0.5 ? -4 : 4;
            for (const b of arkBricks) {
                b.x += shift;
                if (b.x < ARK_BRICK_SIDE) b.x = ARK_BRICK_SIDE;
                if (b.x + b.w > ARK_W - ARK_BRICK_SIDE) b.x = ARK_W - ARK_BRICK_SIDE - b.w;
            }
        }
    }
    for (let i = arkParticles.length - 1; i >= 0; i--) {
        const p = arkParticles[i];
        p.x += p.vx; p.y += p.vy; p.life -= 0.03;
        if (p.life <= 0) arkParticles.splice(i, 1);
    }
    if (arkBricks.length === 0 && !arkBossActive) {
        arkScore += 100;
        arkScoreEl.textContent = arkScore;
        addCoins(15, false);
        if (tryUpdateRecord('arknoid_best', arkScore, arkBestEl, arkBestBox)) toast('🏆 Новый рекорд: ' + arkScore, 'record', 1600);
        if (arkLevel >= ARK_MAX_LEVEL) {
            toast('🎉 Все ' + ARK_MAX_LEVEL + ' уровней пройдены!', 'success', 2500);
            setTimeout(() => { if (arkRunning) { arkLevel = 1; arkLevelEl.textContent = '1'; buildArknoidLevel(1); resetArknoidBall(); } }, 1500);
        } else {
            toast('🎉 Уровень ' + arkLevel + ' пройден! +100', 'success', 1600);
            setTimeout(() => { if (!arkRunning) return; arkLevel++; arkLevelEl.textContent = arkLevel; buildArknoidLevel(arkLevel); resetArknoidBall(); }, 900);
        }
    }
}
function gameOverArknoid() {
    stopArknoid();
    toast('Игра окончена! Очки: ' + arkScore + ' · Уровень: ' + arkLevel, 'info', 2200);
    setTimeout(() => { if (currentScreen === 'arknoid-screen') startArknoid(); }, 1400);
}
function drawArknoid() {
    const grad = arkCtx.createLinearGradient(0, 0, 0, ARK_H);
    grad.addColorStop(0, '#04060f'); grad.addColorStop(1, '#0a0620');
    arkCtx.fillStyle = grad; arkCtx.fillRect(0, 0, ARK_W, ARK_H);
    for (const b of arkBricks) {
        const hpRatio = b.hp / b.maxHp;
        arkCtx.globalAlpha = 0.4 + hpRatio * 0.6;
        arkCtx.fillStyle = b.color;
        arkCtx.shadowColor = b.color;
        arkCtx.shadowBlur = 8;
        roundRect(arkCtx, b.x, b.y, b.w, b.h, 4); arkCtx.fill();
        arkCtx.shadowBlur = 0;
        arkCtx.globalAlpha = 1;
        arkCtx.fillStyle = 'rgba(255,255,255,' + (0.1 + hpRatio * 0.2) + ')';
        roundRect(arkCtx, b.x + 2, b.y + 2, b.w - 4, b.h * 0.4, 3); arkCtx.fill();
        if (hpRatio < 0.7) {
            arkCtx.strokeStyle = 'rgba(0,0,0,0.5)';
            arkCtx.lineWidth = 1;
            arkCtx.beginPath();
            arkCtx.moveTo(b.x + b.w * 0.3, b.y + 3);
            arkCtx.lineTo(b.x + b.w * 0.5, b.y + b.h - 3);
            arkCtx.lineTo(b.x + b.w * 0.7, b.y + 3);
            arkCtx.stroke();
        }
    }
    if (arkBossActive) {
        const boss = arkBossActive;
        arkCtx.fillStyle = '#ff4081';
        arkCtx.shadowColor = '#ff4081';
        arkCtx.shadowBlur = 20;
        roundRect(arkCtx, boss.x, boss.y, boss.w, boss.h, 12); arkCtx.fill();
        arkCtx.shadowBlur = 0;
        arkCtx.fillStyle = '#fff';
        arkCtx.font = 'bold 36px system-ui';
        arkCtx.textAlign = 'center';
        arkCtx.textBaseline = 'middle';
        arkCtx.fillText('👹', boss.x + boss.w/2, boss.y + boss.h/2);
        const hpPct = boss.hp / boss.maxHp;
        arkCtx.fillStyle = 'rgba(0,0,0,0.5)';
        arkCtx.fillRect(boss.x, boss.y - 10, boss.w, 5);
        arkCtx.fillStyle = '#ff4081';
        arkCtx.fillRect(boss.x, boss.y - 10, boss.w * hpPct, 5);
    }
    arkCtx.fillStyle = arkSticky ? '#ffffff' : '#3f51b5';
    arkCtx.shadowColor = arkCtx.fillStyle;
    arkCtx.shadowBlur = 14;
    roundRect(arkCtx, arkPaddleX - arkPaddleW/2, ARK_PADDLE_Y, arkPaddleW, ARK_PADDLE_H, 6);
    arkCtx.fill();
    arkCtx.shadowBlur = 0;
    arkCtx.fillStyle = 'rgba(255,255,255,0.3)';
    roundRect(arkCtx, arkPaddleX - arkPaddleW/2 + 4, ARK_PADDLE_Y + 2, arkPaddleW - 8, 3, 2); arkCtx.fill();
    for (const ball of arkBalls) {
        arkCtx.fillStyle = '#fff';
        arkCtx.shadowColor = '#fff';
        arkCtx.shadowBlur = 14;
        arkCtx.beginPath(); arkCtx.arc(ball.x, ball.y, ARK_BALL_R, 0, Math.PI * 2); arkCtx.fill();
        arkCtx.shadowBlur = 0;
    }
    for (const p of arkPowerups) {
        arkCtx.fillStyle = ARK_POWERUP_COLORS[p.type];
        arkCtx.shadowColor = ARK_POWERUP_COLORS[p.type];
        arkCtx.shadowBlur = 14;
        arkCtx.beginPath(); arkCtx.arc(p.x, p.y, 10, 0, Math.PI * 2); arkCtx.fill();
        arkCtx.shadowBlur = 0;
        arkCtx.fillStyle = '#000';
        arkCtx.font = 'bold 10px system-ui';
        arkCtx.textAlign = 'center';
        arkCtx.textBaseline = 'middle';
        arkCtx.fillText(ARK_POWERUP_ICONS[p.type], p.x, p.y + 1);
    }
    for (const p of arkParticles) {
        arkCtx.globalAlpha = p.life;
        arkCtx.fillStyle = p.color;
        arkCtx.beginPath(); arkCtx.arc(p.x, p.y, p.size, 0, Math.PI * 2); arkCtx.fill();
    }
    arkCtx.globalAlpha = 1;
    if (arkBalls[0] && !arkBalls[0].launched && !arkPaused) {
        arkCtx.fillStyle = 'rgba(255,255,255,0.5)';
        arkCtx.font = 'bold 12px system-ui';
        arkCtx.textAlign = 'center';
        arkCtx.fillText('НАЖМИТЕ 🔥 ДЛЯ ЗАПУСКА', ARK_W/2, ARK_PADDLE_Y - 30);
    }
    for (let i = 0; i < arkLives; i++) {
        arkCtx.fillStyle = '#3f51b5';
        arkCtx.font = 'bold 14px system-ui';
        arkCtx.textAlign = 'left';
        arkCtx.fillText('❤', 8 + i * 16, 20);
    }
    let ex = 8;
    const now = performance.now();
    if (arkActiveEffects.expand) { arkCtx.fillStyle = '#66bb6a'; arkCtx.font = 'bold 11px system-ui'; arkCtx.fillText('⬌ ' + Math.ceil((arkActiveEffects.expand - now)/1000) + 'с', ex, 38); ex += 50; }
    if (arkActiveEffects.sticky) { arkCtx.fillStyle = '#fff'; arkCtx.font = 'bold 11px system-ui'; arkCtx.fillText('⊛ ' + Math.ceil((arkActiveEffects.sticky - now)/1000) + 'с', ex, 38); ex += 50; }
    if (arkLaserTime) { arkCtx.fillStyle = '#ef5350'; arkCtx.font = 'bold 11px system-ui'; arkCtx.fillText('⌇ ' + Math.ceil((arkLaserTime - now)/1000) + 'с', ex, 38); }
    arkCtx.fillStyle = 'rgba(255,255,255,0.6)';
    arkCtx.font = 'bold 12px system-ui';
    arkCtx.textAlign = 'right';
    arkCtx.fillText('Уровень ' + arkLevel + ' / ' + ARK_MAX_LEVEL, ARK_W - 8, 20);
    if (arkPaused) {
        arkCtx.fillStyle = 'rgba(0,0,0,0.5)';
        arkCtx.fillRect(0, 0, ARK_W, ARK_H);
        arkCtx.fillStyle = '#fff';
        arkCtx.font = 'bold 28px system-ui';
        arkCtx.textAlign = 'center';
        arkCtx.textBaseline = 'middle';
        arkCtx.fillText('ПАУЗА', ARK_W/2, ARK_H/2);
    }
}

/* ============================================================
   ГОНКИ
============================================================ */
const raceCanvas = $('raceCanvas');
const raceCtx = raceCanvas.getContext('2d');
const raceScoreEl = $('race-score');
const raceSpeedEl = $('race-speed');
const raceBestEl = $('race-best');
const raceBestBox = $('race-best-box');
const RACE_W = raceCanvas.width, RACE_H = raceCanvas.height;
const RACE_LANES = 3;
const RACE_LANE_W = RACE_W / RACE_LANES;
let raceRunning = false, raceFrameId = null, raceLastTime = 0;
let racePlayerLane = 1;
let racePlayerX = RACE_LANE_W * 1.5;
let raceDir = 0;
let raceScore = 0;
let raceSpeed = 1;
let raceCars = [];
let raceStars = [];
let racePaused = false;
let raceLastSpawn = 0;
let raceBoostTime = 0;
let raceCoinMilestone = 0;
let raceParticles = [];
const RACE_CAR_COLORS = ['#e53935', '#1e88e5', '#43a047', '#fb8c00', '#8e24aa', '#00acc1'];
function startRace() {
    racePlayerLane = 1;
    racePlayerX = RACE_LANE_W * 1.5;
    raceDir = 0;
    raceScore = 0;
    raceSpeed = 1;
    raceCars = [];
    raceStars = [];
    racePaused = false;
    raceLastSpawn = 0;
    raceBoostTime = 0;
    raceCoinMilestone = 0;
    raceParticles = [];
    raceScoreEl.textContent = '0';
    raceSpeedEl.textContent = '1';
    raceBestEl.textContent = getBest('race_best');
    for (let i = 0; i < 20; i++) raceStars.push({ x: RACE_LANE_W/2 + Math.random() * RACE_W, y: Math.random() * RACE_H, len: 20 + Math.random() * 30 });
    raceRunning = true;
    raceLastTime = performance.now();
    if (raceFrameId) cancelAnimationFrame(raceFrameId);
    raceFrameId = requestAnimationFrame(raceLoop);
}
function stopRace() { raceRunning = false; if (raceFrameId) cancelAnimationFrame(raceFrameId); raceFrameId = null; }
function raceControl(action) {
    if (!raceRunning) return;
    if (action === 'left') { raceDir = -1; racePlayerLane = Math.max(0, racePlayerLane - 1); haptic(6); }
    else if (action === 'right') { raceDir = 1; racePlayerLane = Math.min(RACE_LANES - 1, racePlayerLane + 1); haptic(6); }
    else if (action === 'boost') {
        if (performance.now() < raceBoostTime) return;
        raceBoostTime = performance.now() + 1000;
        haptic(20);
        toast('⚡ Ускорение!', 'success', 800);
    } else if (action === 'pause') { racePaused = !racePaused; haptic(10); }
}
function raceLoop(t) {
    if (!raceRunning) return;
    const dt = Math.min(40, t - raceLastTime);
    raceLastTime = t;
    if (!racePaused) updateRace(dt, t);
    drawRace();
    raceFrameId = requestAnimationFrame(raceLoop);
}
function updateRace(dt, t) {
    raceSpeed = 1 + raceScore / 200;
    const speedMul = performance.now() < raceBoostTime ? 2 : 1;
    const speed = raceSpeed * speedMul;
    const targetX = RACE_LANE_W * racePlayerLane + RACE_LANE_W / 2;
    racePlayerX += (targetX - racePlayerX) * 0.25;
    raceDir = 0;
    for (const s of raceStars) {
        s.y += speed * 6 * dt * 0.06;
        if (s.y > RACE_H) { s.y = -s.len; s.x = RACE_LANE_W/2 + Math.random() * RACE_W; }
    }
    if (t - raceLastSpawn > 1400 - raceSpeed * 100) {
        raceLastSpawn = t;
        const lane = Math.floor(Math.random() * RACE_LANES);
        const color = RACE_CAR_COLORS[Math.floor(Math.random() * RACE_CAR_COLORS.length)];
        raceCars.push({ x: RACE_LANE_W * lane + RACE_LANE_W/2, y: -50, w: 40, h: 70, color: color, lane: lane });
    }
    for (let i = raceCars.length - 1; i >= 0; i--) {
        const c = raceCars[i];
        c.y += speed * 4.5 * dt * 0.06;
        if (c.y > RACE_H + 60) {
            raceCars.splice(i, 1);
            raceScore += 10;
            raceScoreEl.textContent = raceScore;
            bump(raceScoreEl);
            const ms = Math.floor(raceScore / 100);
            if (ms > raceCoinMilestone) { addCoins(ms - raceCoinMilestone, false); raceCoinMilestone = ms; }
            if (tryUpdateRecord('race_best', raceScore, raceBestEl, raceBestBox)) toast('🏆 Новый рекорд: ' + raceScore, 'record', 1400);
        }
    }
    const playerY = RACE_H - 90;
    const playerW = 40, playerH = 70;
    for (let i = raceCars.length - 1; i >= 0; i--) {
        const c = raceCars[i];
        if (Math.abs(c.x - racePlayerX) < (c.w + playerW)/2 - 8 && Math.abs(c.y - playerY) < (c.h + playerH)/2 - 8) { raceCars.splice(i, 1); gameOverRace(); return; }
    }
    for (let i = raceParticles.length - 1; i >= 0; i--) {
        const p = raceParticles[i];
        p.x += p.vx; p.y += p.vy; p.life -= 0.03;
        if (p.life <= 0) raceParticles.splice(i, 1);
    }
}
function gameOverRace() {
    stopRace();
    haptic(80);
    for (let k = 0; k < 20; k++) raceParticles.push({ x: racePlayerX, y: RACE_H - 90, vx: (Math.random() - 0.5) * 8, vy: (Math.random() - 0.5) * 8, life: 1, size: 3, color: '#ff3d00' });
    toast('💥 Авария! Очки: ' + raceScore, 'info', 1800);
    setTimeout(() => { if (currentScreen === 'race-screen') startRace(); }, 1300);
}
function drawRace() {
    const grad = raceCtx.createLinearGradient(0, 0, 0, RACE_H);
    grad.addColorStop(0, '#1a0a00'); grad.addColorStop(1, '#0a0500');
    raceCtx.fillStyle = grad;
    raceCtx.fillRect(0, 0, RACE_W, RACE_H);
    raceCtx.fillStyle = '#2a1a10';
    raceCtx.fillRect(0, 0, RACE_LANE_W - 10, RACE_H);
    raceCtx.fillRect(RACE_W - RACE_LANE_W + 10, 0, RACE_LANE_W - 10, RACE_H);
    raceCtx.strokeStyle = 'rgba(255,255,255,0.6)';
    raceCtx.lineWidth = 3;
    for (let i = 1; i < RACE_LANES; i++) {
        const x = RACE_LANE_W * i;
        raceCtx.setLineDash([20, 20]);
        raceCtx.beginPath(); raceCtx.moveTo(x, 0); raceCtx.lineTo(x, RACE_H); raceCtx.stroke();
    }
    raceCtx.setLineDash([]);
    for (const s of raceStars) {
        raceCtx.strokeStyle = 'rgba(255,255,255,0.4)';
        raceCtx.lineWidth = 3;
        raceCtx.beginPath(); raceCtx.moveTo(s.x, s.y); raceCtx.lineTo(s.x, s.y + s.len); raceCtx.stroke();
    }
    for (const c of raceCars) {
        raceCtx.fillStyle = 'rgba(0,0,0,0.5)';
        raceCtx.beginPath(); raceCtx.ellipse(c.x, c.y + c.h/2 - 4, c.w/2, 8, 0, 0, Math.PI * 2); raceCtx.fill();
        raceCtx.fillStyle = c.color;
        raceCtx.shadowColor = c.color;
        raceCtx.shadowBlur = 10;
        roundRect(raceCtx, c.x - c.w/2, c.y - c.h/2, c.w, c.h, 8); raceCtx.fill();
        raceCtx.shadowBlur = 0;
        raceCtx.fillStyle = 'rgba(0,0,0,0.5)';
        roundRect(raceCtx, c.x - c.w/2 + 5, c.y - c.h/2 + 12, c.w - 10, c.h * 0.35, 4); raceCtx.fill();
        raceCtx.fillStyle = 'rgba(255,255,255,0.4)';
        roundRect(raceCtx, c.x - c.w/2 + 7, c.y - c.h/2 + 14, c.w - 14, 6, 2); raceCtx.fill();
    }
    const playerY = RACE_H - 90;
    raceCtx.fillStyle = 'rgba(0,0,0,0.6)';
    raceCtx.beginPath(); raceCtx.ellipse(racePlayerX, playerY + 30, 24, 10, 0, 0, Math.PI * 2); raceCtx.fill();
    raceCtx.fillStyle = '#ffd54f';
    raceCtx.shadowColor = '#ffd54f';
    raceCtx.shadowBlur = 14;
    roundRect(raceCtx, racePlayerX - 20, playerY - 35, 40, 70, 8); raceCtx.fill();
    raceCtx.shadowBlur = 0;
    raceCtx.fillStyle = 'rgba(0,0,0,0.5)';
    roundRect(raceCtx, racePlayerX - 14, playerY - 22, 28, 25, 4); raceCtx.fill();
    raceCtx.fillStyle = 'rgba(150,200,255,0.6)';
    roundRect(raceCtx, racePlayerX - 12, playerY - 20, 24, 8, 2); raceCtx.fill();
    raceCtx.fillStyle = '#fff9c4';
    raceCtx.beginPath(); raceCtx.arc(racePlayerX - 12, playerY - 33, 3, 0, Math.PI * 2); raceCtx.fill();
    raceCtx.beginPath(); raceCtx.arc(racePlayerX + 12, playerY - 33, 3, 0, Math.PI * 2); raceCtx.fill();
    if (performance.now() < raceBoostTime) {
        raceCtx.fillStyle = '#ff5722';
        raceCtx.shadowColor = '#ff5722';
        raceCtx.shadowBlur = 20;
        raceCtx.beginPath();
        raceCtx.moveTo(racePlayerX - 10, playerY + 35);
        raceCtx.lineTo(racePlayerX, playerY + 35 + 20 + Math.random() * 15);
        raceCtx.lineTo(racePlayerX + 10, playerY + 35);
        raceCtx.closePath();
        raceCtx.fill();
        raceCtx.shadowBlur = 0;
    }
    for (const p of raceParticles) {
        raceCtx.globalAlpha = p.life;
        raceCtx.fillStyle = p.color;
        raceCtx.beginPath(); raceCtx.arc(p.x, p.y, p.size, 0, Math.PI * 2); raceCtx.fill();
    }
    raceCtx.globalAlpha = 1;
    raceCtx.fillStyle = 'rgba(255,255,255,0.7)';
    raceCtx.font = 'bold 14px system-ui';
    raceCtx.textAlign = 'left';
    raceCtx.fillText('🏎 ' + raceSpeed.toFixed(1) + 'x', 10, 25);
    if (racePaused) {
        raceCtx.fillStyle = 'rgba(0,0,0,0.6)';
        raceCtx.fillRect(0, 0, RACE_W, RACE_H);
        raceCtx.fillStyle = '#fff';
        raceCtx.font = 'bold 28px system-ui';
        raceCtx.textAlign = 'center';
        raceCtx.textBaseline = 'middle';
        raceCtx.fillText('ПАУЗА', RACE_W/2, RACE_H/2);
    }
}

/* ============================================================
   FLAPPY
============================================================ */
const flappyCanvas = $('flappyCanvas');
const flappyCtx = flappyCanvas.getContext('2d');
const flappyScoreEl = $('flappy-score');
const flappyBestEl = $('flappy-best');
const flappyBestBox = $('flappy-best-box');
const FLAPPY_W = flappyCanvas.width, FLAPPY_H = flappyCanvas.height;
const FLAPPY_GRAVITY = 0.35;
const FLAPPY_JUMP = -6.5;
const FLAPPY_PIPE_W = 60;
const FLAPPY_GAP = 140;
const FLAPPY_PIPE_SPEED = 2.2;
let flappyRunning = false, flappyFrameId = null, flappyLastTime = 0;
let flappyBird = { x: 80, y: FLAPPY_H / 2, vy: 0, r: 12 };
let flappyPipes = [];
let flappyScore = 0;
let flappyState = 'waiting';
let flappyPaused = false;
let flappyLastPipe = 0;
let flappyCoinMilestone = 0;
let flappyParticles = [];
function startFlappy() {
    flappyBird = { x: 80, y: FLAPPY_H / 2, vy: 0, r: 12 };
    flappyPipes = [];
    flappyScore = 0;
    flappyState = 'waiting';
    flappyPaused = false;
    flappyLastPipe = 0;
    flappyCoinMilestone = 0;
    flappyParticles = [];
    flappyScoreEl.textContent = '0';
    flappyBestEl.textContent = getBest('flappy_best');
    flappyRunning = true;
    flappyLastTime = performance.now();
    if (flappyFrameId) cancelAnimationFrame(flappyFrameId);
    flappyFrameId = requestAnimationFrame(flappyLoop);
}
function stopFlappy() { flappyRunning = false; if (flappyFrameId) cancelAnimationFrame(flappyFrameId); flappyFrameId = null; }
function flappyFlap(e) {
    if (e) e.preventDefault();
    haptic(8);
    if (flappyState === 'waiting') { flappyState = 'playing'; flappyBird.vy = FLAPPY_JUMP; return; }
    if (flappyState === 'dead') { startFlappy(); return; }
    if (flappyState === 'playing') flappyBird.vy = FLAPPY_JUMP;
}
function flappyLoop(t) {
    if (!flappyRunning) return;
    const dt = Math.min(40, t - flappyLastTime);
    flappyLastTime = t;
    if (!flappyPaused) updateFlappy(dt, t);
    drawFlappy();
    flappyFrameId = requestAnimationFrame(flappyLoop);
}
function updateFlappy(dt, t) {
    if (flappyState === 'waiting') { flappyBird.y = FLAPPY_H / 2 + Math.sin(t / 300) * 8; return; }
    if (flappyState === 'dead') {
        flappyBird.vy += FLAPPY_GRAVITY * dt * 0.06;
        flappyBird.y += flappyBird.vy * dt * 0.06;
        for (let i = flappyParticles.length - 1; i >= 0; i--) {
            const p = flappyParticles[i];
            p.x += p.vx; p.y += p.vy; p.life -= 0.03;
            if (p.life <= 0) flappyParticles.splice(i, 1);
        }
        return;
    }
    flappyBird.vy += FLAPPY_GRAVITY * dt * 0.06;
    flappyBird.y += flappyBird.vy * dt * 0.06;
    if (t - flappyLastPipe > 1500) {
        flappyLastPipe = t;
        const minTop = 60;
        const maxTop = FLAPPY_H - FLAPPY_GAP - 60;
        const topH = minTop + Math.random() * (maxTop - minTop);
        flappyPipes.push({ x: FLAPPY_W, topH: topH, bottomY: topH + FLAPPY_GAP, passed: false });
    }
    for (let i = flappyPipes.length - 1; i >= 0; i--) {
        const p = flappyPipes[i];
        p.x -= FLAPPY_PIPE_SPEED * dt * 0.06 * 1.5;
        if (!p.passed && p.x + FLAPPY_PIPE_W < flappyBird.x) {
            p.passed = true;
            flappyScore++;
            flappyScoreEl.textContent = flappyScore;
            bump(flappyScoreEl);
            haptic(15);
            const ms = Math.floor(flappyScore / 5);
            if (ms > flappyCoinMilestone) { addCoins(ms - flappyCoinMilestone, false); flappyCoinMilestone = ms; }
            if (tryUpdateRecord('flappy_best', flappyScore, flappyBestEl, flappyBestBox)) toast('🏆 Новый рекорд: ' + flappyScore, 'record', 1400);
        }
        if (p.x < -FLAPPY_PIPE_W) flappyPipes.splice(i, 1);
    }
    for (const p of flappyPipes) {
        if (flappyBird.x + flappyBird.r > p.x && flappyBird.x - flappyBird.r < p.x + FLAPPY_PIPE_W) {
            if (flappyBird.y - flappyBird.r < p.topH || flappyBird.y + flappyBird.r > p.bottomY) { flappyGameOver(); return; }
        }
    }
    if (flappyBird.y - flappyBird.r < 0) { flappyBird.y = flappyBird.r; flappyBird.vy = 0; }
    if (flappyBird.y + flappyBird.r > FLAPPY_H) { flappyGameOver(); return; }
}
function flappyGameOver() {
    flappyState = 'dead';
    haptic(80);
    for (let k = 0; k < 15; k++) flappyParticles.push({ x: flappyBird.x, y: flappyBird.y, vx: (Math.random() - 0.5) * 6, vy: (Math.random() - 0.5) * 6 - 2, life: 1, size: 3, color: '#ffc400' });
    toast('💥 Очки: ' + flappyScore + '. Нажмите, чтобы играть снова', 'info', 2000);
}
function drawFlappy() {
    const grad = flappyCtx.createLinearGradient(0, 0, 0, FLAPPY_H);
    grad.addColorStop(0, '#041a2e');
    grad.addColorStop(0.6, '#0a2540');
    grad.addColorStop(1, '#1a3a5e');
    flappyCtx.fillStyle = grad;
    flappyCtx.fillRect(0, 0, FLAPPY_W, FLAPPY_H);
    flappyCtx.fillStyle = 'rgba(255,255,255,0.05)';
    for (let i = 0; i < 8; i++) {
        const bx = i * 50;
        const bh = 40 + (i * 13) % 60;
        flappyCtx.fillRect(bx, FLAPPY_H - 80 - bh, 40, bh);
    }
    for (const p of flappyPipes) {
        flappyCtx.fillStyle = '#4caf50';
        flappyCtx.shadowColor = '#4caf50';
        flappyCtx.shadowBlur = 10;
        roundRect(flappyCtx, p.x, 0, FLAPPY_PIPE_W, p.topH, 6); flappyCtx.fill();
        roundRect(flappyCtx, p.x, p.bottomY, FLAPPY_PIPE_W, FLAPPY_H - p.bottomY, 6); flappyCtx.fill();
        flappyCtx.shadowBlur = 0;
        flappyCtx.fillStyle = 'rgba(255,255,255,0.2)';
        flappyCtx.fillRect(p.x + 6, 0, 8, p.topH);
        flappyCtx.fillRect(p.x + 6, p.bottomY, 8, FLAPPY_H - p.bottomY);
        flappyCtx.fillStyle = '#388e3c';
        roundRect(flappyCtx, p.x - 4, p.topH - 20, FLAPPY_PIPE_W + 8, 20, 4); flappyCtx.fill();
        roundRect(flappyCtx, p.x - 4, p.bottomY, FLAPPY_PIPE_W + 8, 20, 4); flappyCtx.fill();
    }
    flappyCtx.fillStyle = '#3e2723';
    flappyCtx.fillRect(0, FLAPPY_H - 30, FLAPPY_W, 30);
    flappyCtx.fillStyle = '#5d4037';
    flappyCtx.fillRect(0, FLAPPY_H - 30, FLAPPY_W, 6);
    flappyCtx.save();
    flappyCtx.translate(flappyBird.x, flappyBird.y);
    const angle = flappyState === 'dead' ? Math.PI / 2 : Math.atan2(flappyBird.vy, 10) * 0.5;
    flappyCtx.rotate(angle);
    flappyCtx.fillStyle = '#ffc400';
    flappyCtx.shadowColor = '#ffc400';
    flappyCtx.shadowBlur = 12;
    flappyCtx.beginPath();
    flappyCtx.ellipse(0, 0, flappyBird.r + 4, flappyBird.r, 0, 0, Math.PI * 2);
    flappyCtx.fill();
    flappyCtx.shadowBlur = 0;
    flappyCtx.fillStyle = '#ff9800';
    flappyCtx.beginPath(); flappyCtx.ellipse(-2, 2, 7, 5, -0.3, 0, Math.PI * 2); flappyCtx.fill();
    flappyCtx.fillStyle = '#fff';
    flappyCtx.beginPath(); flappyCtx.arc(5, -3, 4, 0, Math.PI * 2); flappyCtx.fill();
    flappyCtx.fillStyle = '#000';
    flappyCtx.beginPath(); flappyCtx.arc(6, -3, 2, 0, Math.PI * 2); flappyCtx.fill();
    flappyCtx.fillStyle = '#ff5722';
    flappyCtx.beginPath();
    flappyCtx.moveTo(11, -1);
    flappyCtx.lineTo(17, 2);
    flappyCtx.lineTo(11, 5);
    flappyCtx.closePath();
    flappyCtx.fill();
    flappyCtx.restore();
    for (const p of flappyParticles) {
        flappyCtx.globalAlpha = p.life;
        flappyCtx.fillStyle = p.color;
        flappyCtx.beginPath(); flappyCtx.arc(p.x, p.y, p.size, 0, Math.PI * 2); flappyCtx.fill();
    }
    flappyCtx.globalAlpha = 1;
    if (flappyState === 'waiting') {
        flappyCtx.fillStyle = 'rgba(255,255,255,0.85)';
        flappyCtx.font = 'bold 18px system-ui';
        flappyCtx.textAlign = 'center';
        flappyCtx.textBaseline = 'middle';
        flappyCtx.fillText('НАЖМИТЕ «ЛЕТЕТЬ»', FLAPPY_W/2, FLAPPY_H/2 - 60);
        flappyCtx.font = 'bold 14px system-ui';
        flappyCtx.fillStyle = 'rgba(255,255,255,0.5)';
        flappyCtx.fillText('или тапните по экрану', FLAPPY_W/2, FLAPPY_H/2 - 35);
    }
    if (flappyState === 'dead') {
        flappyCtx.fillStyle = 'rgba(0,0,0,0.5)';
        flappyCtx.fillRect(0, 0, FLAPPY_W, FLAPPY_H);
        flappyCtx.fillStyle = '#fff';
        flappyCtx.font = 'bold 32px system-ui';
        flappyCtx.textAlign = 'center';
        flappyCtx.textBaseline = 'middle';
        flappyCtx.fillText('ИГРА ОКОНЧЕНА', FLAPPY_W/2, FLAPPY_H/2 - 30);
        flappyCtx.font = 'bold 20px system-ui';
        flappyCtx.fillStyle = '#ffd54f';
        flappyCtx.fillText('Очки: ' + flappyScore, FLAPPY_W/2, FLAPPY_H/2 + 10);
        flappyCtx.font = 'bold 14px system-ui';
        flappyCtx.fillStyle = 'rgba(255,255,255,0.7)';
        flappyCtx.fillText('Нажмите для рестарта', FLAPPY_W/2, FLAPPY_H/2 + 45);
    }
    flappyCtx.fillStyle = '#fff';
    flappyCtx.font = 'bold 32px system-ui';
    flappyCtx.textAlign = 'center';
    flappyCtx.textBaseline = 'top';
    flappyCtx.shadowColor = '#000';
    flappyCtx.shadowBlur = 6;
    flappyCtx.fillText(flappyScore, FLAPPY_W/2, 20);
    flappyCtx.shadowBlur = 0;
}

/* ============================================================
   КОСМИЧЕСКИЙ ШУТЕР
============================================================ */
const shCanvas = $('shooterCanvas');
const shCtx = shCanvas.getContext('2d');
const shScoreEl = $('shooter-score');
const shBestEl = $('shooter-best');
const shBestBox = $('shooter-best-box');
const SH_W = shCanvas.width, SH_H = shCanvas.height;
let shRunning = false;
let shPlayerX = SH_W / 2, shPlayerW = 36, shPlayerH = 30;
let shBullets = [], shEnemies = [], shEnemyBullets = [], shStars = [], shParticles = [];
let shPowerups = [];
let shScore = 0, shLives = 3, shMaxLives = 5;
let shLastFire = 0, shLastEnemySpawn = 0, shLastEnemyShot = 0, shLastPowerupSpawn = 0;
let shDir = 0, shFrameId = null, shLastTime = 0, shPaused = false, shCoinMilestoneSh = 0;
let shBossActive = null, shNextBossScore = 500;
let shShieldTime = 0, shTripleTime = 0, shCombo = 0, shLastKillTime = 0;
const SH_PLAYER_Y = SH_H - 60;
const SH_FIRE_COOLDOWN = 220;
const SH_POWERUP_DURATION = 8000;
function startShooter() {
    shPlayerX = SH_W / 2;
    shBullets = []; shEnemies = []; shEnemyBullets = []; shParticles = []; shPowerups = [];
    shScore = 0; shLives = 3;
    shScoreEl.textContent = '0';
    shBestEl.textContent = getBest('shooter_best');
    shDir = 0; shLastFire = 0; shLastEnemySpawn = 0; shLastEnemyShot = 0; shLastPowerupSpawn = 0;
    shCoinMilestoneSh = 0; shPaused = false;
    shBossActive = null; shNextBossScore = 500;
    shShieldTime = 0; shTripleTime = 0; shCombo = 0; shLastKillTime = 0;
    initStars();
    shRunning = true;
    shLastTime = performance.now();
    if (shFrameId) cancelAnimationFrame(shFrameId);
    shFrameId = requestAnimationFrame(shooterLoop);
}
function stopShooter() { shRunning = false; if (shFrameId) cancelAnimationFrame(shFrameId); shFrameId = null; }
function initStars() {
    shStars = [];
    for (let i = 0; i < 60; i++) shStars.push({x: Math.random() * SH_W, y: Math.random() * SH_H, speed: 0.3 + Math.random() * 2, size: 0.5 + Math.random() * 1.8});
}
function shooterControl(action) {
    if (!shRunning) return;
    if (action === 'left') { shDir = -1; haptic(6); }
    else if (action === 'right') { shDir = 1; haptic(6); }
    else if (action === 'fire') { fireBullet(true); haptic(10); }
    else if (action === 'pause') { shPaused = !shPaused; haptic(10); }
}
function fireBullet(force = false) {
    const now = performance.now();
    if (!force && now - shLastFire < SH_FIRE_COOLDOWN) return;
    shLastFire = now;
    const triple = now < shTripleTime;
    if (triple) {
        shBullets.push({x: shPlayerX, y: SH_PLAYER_Y - 4, vy: -8});
        shBullets.push({x: shPlayerX - 10, y: SH_PLAYER_Y - 4, vy: -8, vx: -1});
        shBullets.push({x: shPlayerX + 10, y: SH_PLAYER_Y - 4, vy: -8, vx: 1});
    } else shBullets.push({x: shPlayerX, y: SH_PLAYER_Y - 4, vy: -8});
}
function shooterLoop(t) {
    if (!shRunning) return;
    const dt = Math.min(40, t - shLastTime);
    shLastTime = t;
    if (!shPaused) updateShooter(dt, t);
    drawShooter();
    shFrameId = requestAnimationFrame(shooterLoop);
}
function updateShooter(dt, t) {
    shPlayerX += shDir * 0.34 * dt;
    shPlayerX = Math.max(shPlayerW/2, Math.min(SH_W - shPlayerW/2, shPlayerX));
    for (const s of shStars) {
        s.y += s.speed * dt * 0.06;
        if (s.y > SH_H) { s.y = 0; s.x = Math.random() * SH_W; }
    }
    if (t - shLastFire > SH_FIRE_COOLDOWN) fireBullet();
    for (let i = shBullets.length - 1; i >= 0; i--) {
        const b = shBullets[i];
        b.y += b.vy * dt * 0.06;
        if (b.vx) b.x += b.vx * dt * 0.06;
        if (b.y < -10 || b.x < -10 || b.x > SH_W + 10) shBullets.splice(i, 1);
    }
    if (!shBossActive && t - shLastEnemySpawn > 800 + Math.random() * 800) { shLastEnemySpawn = t; spawnEnemy(); }
    if (t - shLastPowerupSpawn > 5000 + Math.random() * 4000 && shPowerups.length < 2) { shLastPowerupSpawn = t; spawnPowerup(); }
    if (!shBossActive && shScore >= shNextBossScore) {
        shBossActive = spawnBoss();
        shNextBossScore += 500;
        toast('👹 БОСС!', 'info', 1500);
        haptic(60);
    }
    for (let i = shEnemies.length - 1; i >= 0; i--) {
        const e = shEnemies[i];
        e.y += e.vy * dt * 0.06;
        e.x += e.vx * dt * 0.06;
        if (e.x < e.w/2 || e.x > SH_W - e.w/2) e.vx *= -1;
        if (e.y > SH_H + 20) { shEnemies.splice(i, 1); continue; }
        for (let j = shBullets.length - 1; j >= 0; j--) {
            const b = shBullets[j];
            if (Math.abs(b.x - e.x) < e.w/2 && Math.abs(b.y - e.y) < e.h/2) {
                shBullets.splice(j, 1);
                e.hp--;
                for (let k = 0; k < 4; k++) shParticles.push({x: e.x, y: e.y, vx: (Math.random() - 0.5) * 3, vy: (Math.random() - 0.5) * 3, life: 1, size: 2 + Math.random() * 2, color: e.color});
                if (e.hp <= 0) killEnemy(e, i);
                break;
            }
        }
    }
    if (shBossActive) {
        const b = shBossActive;
        b.y += b.vy * dt * 0.06;
        b.x += b.vx * dt * 0.06;
        if (b.x < b.w/2 || b.x > SH_W - b.w/2) b.vx *= -1;
        if (b.y > 100) { b.y = 100; b.vy = 0; }
        b.shootTimer = (b.shootTimer || 0) + dt;
        if (b.shootTimer > 900) {
            b.shootTimer = 0;
            for (let k = -1; k <= 1; k++) shEnemyBullets.push({x: b.x + k * 20, y: b.y + b.h/2, vy: 4});
        }
        for (let j = shBullets.length - 1; j >= 0; j--) {
            const bullet = shBullets[j];
            if (Math.abs(bullet.x - b.x) < b.w/2 && Math.abs(bullet.y - b.y) < b.h/2) {
                shBullets.splice(j, 1);
                b.hp--;
                for (let k = 0; k < 5; k++) shParticles.push({x: bullet.x, y: bullet.y, vx: (Math.random() - 0.5) * 4, vy: (Math.random() - 0.5) * 4, life: 1, size: 2 + Math.random() * 2, color: '#ff4081'});
                if (b.hp <= 0) {
                    shScore += 500;
                    shScoreEl.textContent = shScore;
                    bump(shScoreEl);
                    for (let k = 0; k < 30; k++) shParticles.push({x: b.x + (Math.random() - 0.5) * b.w, y: b.y + (Math.random() - 0.5) * b.h, vx: (Math.random() - 0.5) * 6, vy: (Math.random() - 0.5) * 6, life: 1, size: 3 + Math.random() * 3, color: '#ff4081'});
                    addCoins(10, false);
                    toast('🎉 Босс повержен! +500', 'success', 1800);
                    haptic(80);
                    if (tryUpdateRecord('shooter_best', shScore, shBestEl, shBestBox)) toast('🏆 Новый рекорд: ' + shScore, 'record', 1600);
                    shBossActive = null;
                }
                break;
            }
        }
    }
    for (let i = shPowerups.length - 1; i >= 0; i--) {
        const p = shPowerups[i];
        p.y += 1.2 * dt * 0.06;
        if (p.y > SH_H + 20) { shPowerups.splice(i, 1); continue; }
        if (Math.abs(p.x - shPlayerX) < shPlayerW/2 + 10 && Math.abs(p.y - SH_PLAYER_Y) < shPlayerH/2 + 10) { applyPowerup(p.type); shPowerups.splice(i, 1); }
    }
    if (t - shLastEnemyShot > 900 && shEnemies.length > 0) {
        shLastEnemyShot = t;
        const e = shEnemies[Math.floor(Math.random() * shEnemies.length)];
        shEnemyBullets.push({x: e.x, y: e.y + e.h/2, vy: 4});
    }
    for (let i = shEnemyBullets.length - 1; i >= 0; i--) {
        const b = shEnemyBullets[i];
        b.y += b.vy * dt * 0.06;
        if (b.y > SH_H + 10) { shEnemyBullets.splice(i, 1); continue; }
        if (Math.abs(b.x - shPlayerX) < shPlayerW/2 && Math.abs(b.y - SH_PLAYER_Y) < shPlayerH/2) { shEnemyBullets.splice(i, 1); damagePlayer(); }
    }
    for (let i = shEnemies.length - 1; i >= 0; i--) {
        const e = shEnemies[i];
        if (Math.abs(e.x - shPlayerX) < (e.w + shPlayerW)/2 - 6 && Math.abs(e.y - SH_PLAYER_Y) < (e.h + shPlayerH)/2 - 6) { shEnemies.splice(i, 1); damagePlayer(); }
    }
    for (let i = shParticles.length - 1; i >= 0; i--) {
        const p = shParticles[i];
        p.x += p.vx; p.y += p.vy; p.life -= 0.03;
        if (p.life <= 0) shParticles.splice(i, 1);
    }
    if (performance.now() > shTripleTime) shTripleTime = 0;
    if (performance.now() > shShieldTime) shShieldTime = 0;
}
function killEnemy(e, idx) {
    shEnemies.splice(idx, 1);
    const now = performance.now();
    if (now - shLastKillTime < 1500) shCombo++; else shCombo = 1;
    shLastKillTime = now;
    const comboMult = Math.min(5, shCombo);
    const points = e.points * comboMult;
    shScore += points;
    shScoreEl.textContent = shScore;
    bump(shScoreEl);
    if (shCombo > 1) toast('×' + shCombo + ' комбо! +' + points, 'success', 900);
    const ms = Math.floor(shScore / 100);
    if (ms > shCoinMilestoneSh) { addCoins((ms - shCoinMilestoneSh) * 2, false); shCoinMilestoneSh = ms; }
    if (tryUpdateRecord('shooter_best', shScore, shBestEl, shBestBox)) toast('🏆 Новый рекорд: ' + shScore, 'record', 1400);
}
function spawnEnemy() {
    const types = [
        {w: 30, h: 26, hp: 1, vy: 1.0, points: 10, color: '#ff5252'},
        {w: 34, h: 30, hp: 2, vy: 0.8, points: 20, color: '#e040fb'},
        {w: 26, h: 22, hp: 1, vy: 1.4, points: 15, color: '#40c4ff'},
        {w: 40, h: 34, hp: 3, vy: 0.6, points: 30, color: '#ffa726'}
    ];
    const t = types[Math.floor(Math.random() * types.length)];
    shEnemies.push({x: t.w + Math.random() * (SH_W - t.w * 2), y: -t.h, w: t.w, h: t.h, hp: t.hp, vy: t.vy, vx: (Math.random() - 0.5) * 0.6, points: t.points, color: t.color});
}
function spawnBoss() { return {x: SH_W / 2, y: -60, w: 90, h: 70, hp: 30 + Math.floor(shScore / 500) * 10, vy: 1.5, vx: 1.2, shootTimer: 0}; }
function spawnPowerup() {
    const types = ['shield', 'triple', 'bomb', 'life'];
    const weights = [0.35, 0.35, 0.2, 0.1];
    let r = Math.random(), acc = 0, type = 'shield';
    for (let i = 0; i < types.length; i++) { acc += weights[i]; if (r < acc) { type = types[i]; break; } }
    shPowerups.push({x: 30 + Math.random() * (SH_W - 60), y: -20, type});
}
function applyPowerup(type) {
    haptic(20);
    if (type === 'shield') { shShieldTime = performance.now() + SH_POWERUP_DURATION; toast('💎 Щит активен!', 'success', 1200); }
    else if (type === 'triple') { shTripleTime = performance.now() + SH_POWERUP_DURATION; toast('⚡ Тройной выстрел!', 'success', 1200); }
    else if (type === 'bomb') {
        for (const e of shEnemies) { shScore += e.points; for (let k = 0; k < 6; k++) shParticles.push({x: e.x, y: e.y, vx: (Math.random() - 0.5) * 4, vy: (Math.random() - 0.5) * 4, life: 1, size: 2 + Math.random() * 2, color: e.color}); }
        const count = shEnemies.length;
        shEnemies = []; shEnemyBullets = [];
        shScoreEl.textContent = shScore;
        bump(shScoreEl);
        toast('💣 Бомба! Уничтожено: ' + count, 'success', 1400);
        if (tryUpdateRecord('shooter_best', shScore, shBestEl, shBestBox)) toast('🏆 Новый рекорд: ' + shScore, 'record', 1400);
    } else if (type === 'life') {
        if (shLives < shMaxLives) { shLives++; toast('❤ +1 жизнь!', 'success', 1200); }
        else { shScore += 100; shScoreEl.textContent = shScore; toast('❤ Максимум! +100', 'info', 1200); }
    }
}
function damagePlayer() {
    if (performance.now() < shShieldTime) { toast('💎 Щит поглотил удар', 'info', 800); return; }
    shLives--;
    haptic(80);
    shCombo = 0;
    if (shLives <= 0) gameOverShooter();
    else toast('💥 Попадание! Жизней: ' + shLives, 'info', 900);
}
function gameOverShooter() {
    stopShooter();
    const coinsEarned = Math.floor(shScore / 100) * 2;
    toast('Игра окончена! Очки: ' + shScore + (coinsEarned ? ' (+' + coinsEarned + '🪙)' : ''), 'info', 2000);
    setTimeout(() => { if (currentScreen === 'shooter-screen') startShooter(); }, 1200);
}
function drawShooter() {
    const grad = shCtx.createLinearGradient(0, 0, 0, SH_H);
    grad.addColorStop(0, '#000510'); grad.addColorStop(1, '#0a0620');
    shCtx.fillStyle = grad; shCtx.fillRect(0, 0, SH_W, SH_H);
    for (const s of shStars) {
        shCtx.fillStyle = 'rgba(255,255,255,' + (0.3 + s.speed * 0.3) + ')';
        shCtx.beginPath(); shCtx.arc(s.x, s.y, s.size, 0, Math.PI * 2); shCtx.fill();
    }
    for (const p of shPowerups) {
        const colors = {shield: '#00bcd4', triple: '#ffeb3b', bomb: '#ff5252', life: '#f44336'};
        const icons = {shield: '💎', triple: '⚡', bomb: '💣', life: '❤'};
        shCtx.fillStyle = colors[p.type];
        shCtx.shadowColor = colors[p.type];
        shCtx.shadowBlur = 14;
        shCtx.beginPath(); shCtx.arc(p.x, p.y, 12, 0, Math.PI * 2); shCtx.fill();
        shCtx.shadowBlur = 0;
        shCtx.font = 'bold 14px system-ui';
        shCtx.textAlign = 'center';
        shCtx.textBaseline = 'middle';
        shCtx.fillStyle = '#000';
        shCtx.fillText(icons[p.type], p.x, p.y + 1);
    }
    for (const b of shBullets) {
        shCtx.fillStyle = '#ffeb3b';
        shCtx.shadowColor = '#ffeb3b';
        shCtx.shadowBlur = 10;
        shCtx.fillRect(b.x - 1.5, b.y - 8, 3, 12);
        shCtx.shadowBlur = 0;
    }
    for (const e of shEnemies) {
        shCtx.fillStyle = e.color;
        shCtx.shadowColor = e.color;
        shCtx.shadowBlur = 12;
        shCtx.beginPath();
        shCtx.moveTo(e.x, e.y + e.h/2);
        shCtx.lineTo(e.x - e.w/2, e.y - e.h/2);
        shCtx.lineTo(e.x + e.w/2, e.y - e.h/2);
        shCtx.closePath();
        shCtx.fill();
        shCtx.shadowBlur = 0;
        shCtx.fillStyle = '#fff';
        shCtx.beginPath(); shCtx.arc(e.x, e.y - 2, 2.5, 0, Math.PI * 2); shCtx.fill();
    }
    if (shBossActive) {
        const b = shBossActive;
        shCtx.fillStyle = '#ff4081';
        shCtx.shadowColor = '#ff4081';
        shCtx.shadowBlur = 20;
        roundRect(shCtx, b.x - b.w/2, b.y - b.h/2, b.w, b.h, 12);
        shCtx.fill();
        shCtx.shadowBlur = 0;
        shCtx.fillStyle = '#fff';
        shCtx.font = 'bold 28px system-ui';
        shCtx.textAlign = 'center';
        shCtx.textBaseline = 'middle';
        shCtx.fillText('👹', b.x, b.y);
        const maxHp = 30 + Math.floor(shScore / 500) * 10;
        const hpPct = b.hp / maxHp;
        shCtx.fillStyle = 'rgba(0,0,0,0.5)';
        shCtx.fillRect(b.x - b.w/2, b.y - b.h/2 - 10, b.w, 5);
        shCtx.fillStyle = '#ff4081';
        shCtx.fillRect(b.x - b.w/2, b.y - b.h/2 - 10, b.w * hpPct, 5);
    }
    for (const b of shEnemyBullets) {
        shCtx.fillStyle = '#ff5252';
        shCtx.shadowColor = '#ff5252';
        shCtx.shadowBlur = 8;
        shCtx.beginPath(); shCtx.arc(b.x, b.y, 3, 0, Math.PI * 2); shCtx.fill();
        shCtx.shadowBlur = 0;
    }
    for (const p of shParticles) {
        shCtx.globalAlpha = p.life;
        shCtx.fillStyle = p.color;
        shCtx.beginPath(); shCtx.arc(p.x, p.y, p.size, 0, Math.PI * 2); shCtx.fill();
    }
    shCtx.globalAlpha = 1;
    if (performance.now() < shShieldTime) {
        shCtx.strokeStyle = 'rgba(0,188,212,0.6)';
        shCtx.lineWidth = 2;
        shCtx.beginPath();
        shCtx.arc(shPlayerX, SH_PLAYER_Y, shPlayerW * 0.7, 0, Math.PI * 2);
        shCtx.stroke();
    }
    shCtx.save();
    shCtx.translate(shPlayerX, SH_PLAYER_Y);
    shCtx.fillStyle = '#4dd0e1';
    shCtx.shadowColor = '#4dd0e1';
    shCtx.shadowBlur = 14;
    shCtx.beginPath();
    shCtx.moveTo(0, -shPlayerH/2);
    shCtx.lineTo(-shPlayerW/2, shPlayerH/2);
    shCtx.lineTo(-shPlayerW/4, shPlayerH/2 - 6);
    shCtx.lineTo(shPlayerW/4, shPlayerH/2 - 6);
    shCtx.lineTo(shPlayerW/2, shPlayerH/2);
    shCtx.closePath();
    shCtx.fill();
    shCtx.shadowBlur = 0;
    shCtx.fillStyle = '#b2ebf2';
    shCtx.beginPath(); shCtx.arc(0, -2, 5, 0, Math.PI * 2); shCtx.fill();
    shCtx.restore();
    for (let i = 0; i < shLives; i++) {
        shCtx.fillStyle = '#4dd0e1';
        shCtx.font = 'bold 14px system-ui';
        shCtx.textAlign = 'left';
        shCtx.fillText('❤', 6 + i * 16, 20);
    }
    if (shCombo > 1) {
        shCtx.fillStyle = '#ffd54f';
        shCtx.font = 'bold 16px system-ui';
        shCtx.textAlign = 'right';
        shCtx.fillText('×' + Math.min(5, shCombo) + ' КОМБО', SH_W - 8, 22);
    }
    let by = 40;
    if (performance.now() < shShieldTime) { shCtx.fillStyle = '#00bcd4'; shCtx.font = 'bold 12px system-ui'; shCtx.textAlign = 'left'; shCtx.fillText('💎 ' + Math.ceil((shShieldTime - performance.now())/1000) + 'с', 8, by); by += 16; }
    if (performance.now() < shTripleTime) { shCtx.fillStyle = '#ffeb3b'; shCtx.font = 'bold 12px system-ui'; shCtx.textAlign = 'left'; shCtx.fillText('⚡ ' + Math.ceil((shTripleTime - performance.now())/1000) + 'с', 8, by); }
    if (shPaused) {
        shCtx.fillStyle = 'rgba(0,0,0,0.5)';
        shCtx.fillRect(0, 0, SH_W, SH_H);
        shCtx.fillStyle = '#fff';
        shCtx.font = 'bold 28px system-ui';
        shCtx.textAlign = 'center';
        shCtx.textBaseline = 'middle';
        shCtx.fillText('ПАУЗА', SH_W/2, SH_H/2);
    }
}

/* ============================================================
   ТЕТРИС
============================================================ */
const tCanvas = $('tetrisCanvas');
const tCtx = tCanvas.getContext('2d');
const tScoreEl = $('tetris-score');
const tBestEl = $('tetris-best');
const tBestBox = $('tetris-best-box');
const tPauseBtn = $('tetrisPauseBtn');
const T_COLS = 10, T_ROWS = 20, T_CELL = tCanvas.width / T_COLS;
const T_PIECES = {
    I: {shape: [[1,1,1,1]], color: '#00e5ff'},
    O: {shape: [[1,1],[1,1]], color: '#ffeb3b'},
    T: {shape: [[0,1,0],[1,1,1]], color: '#ba68c8'},
    S: {shape: [[0,1,1],[1,1,0]], color: '#66bb6a'},
    Z: {shape: [[1,1,0],[0,1,1]], color: '#ef5350'},
    J: {shape: [[1,0,0],[1,1,1]], color: '#42a5f5'},
    L: {shape: [[0,0,1],[1,1,1]], color: '#ff9800'}
};
let tGrid = [], tCurrent = null, tNext = null, tScore = 0;
let tRunning = false, tPaused = false, tFrameId = null, tLastTime = 0;
let tDropInterval = 700, tDropCounter = 0, tLines = 0, tCoinMilestone = 0;
function startTetris() {
    tGrid = Array.from({length: T_ROWS}, () => Array(T_COLS).fill(null));
    tScore = 0; tLines = 0; tCoinMilestone = 0;
    tScoreEl.textContent = '0';
    tBestEl.textContent = getBest('tetris_best');
    tPaused = false;
    tPauseBtn.textContent = 'ПАУЗА';
    tDropInterval = 700; tDropCounter = 0;
    tNext = randomTetrisPiece();
    spawnTetrisPiece();
    tRunning = true;
    tLastTime = performance.now();
    if (tFrameId) cancelAnimationFrame(tFrameId);
    tFrameId = requestAnimationFrame(tetrisLoop);
}
function stopTetris() { tRunning = false; if (tFrameId) cancelAnimationFrame(tFrameId); tFrameId = null; }
function randomTetrisPiece() {
    const keys = Object.keys(T_PIECES);
    const k = keys[Math.floor(Math.random() * keys.length)];
    return {type: k, shape: T_PIECES[k].shape.map(row => row.slice()), color: T_PIECES[k].color, x: 0, y: 0};
}
function spawnTetrisPiece() {
    tCurrent = tNext || randomTetrisPiece();
    tNext = randomTetrisPiece();
    tCurrent.x = Math.floor((T_COLS - tCurrent.shape[0].length) / 2);
    tCurrent.y = 0;
    if (collidesTetris(tCurrent.x, tCurrent.y, tCurrent.shape)) gameOverTetris();
}
function collidesTetris(x, y, shape) {
    for (let r = 0; r < shape.length; r++) for (let c = 0; c < shape[r].length; c++) {
        if (!shape[r][c]) continue;
        const nx = x + c, ny = y + r;
        if (nx < 0 || nx >= T_COLS || ny >= T_ROWS) return true;
        if (ny >= 0 && tGrid[ny][nx]) return true;
    }
    return false;
}
function lockTetrisPiece() {
    for (let r = 0; r < tCurrent.shape.length; r++) for (let c = 0; c < tCurrent.shape[r].length; c++) if (tCurrent.shape[r][c]) {
        const ny = tCurrent.y + r, nx = tCurrent.x + c;
        if (ny >= 0) tGrid[ny][nx] = tCurrent.color;
    }
    clearTetrisLines();
    spawnTetrisPiece();
}
function clearTetrisLines() {
    let cleared = 0;
    for (let r = T_ROWS - 1; r >= 0; r--) {
        if (tGrid[r].every(cell => cell)) { tGrid.splice(r, 1); tGrid.unshift(Array(T_COLS).fill(null)); cleared++; r++; }
    }
    if (cleared > 0) {
        const points = [0, 100, 300, 500, 800][cleared] || 800;
        tScore += points;
        tLines += cleared;
        tScoreEl.textContent = tScore;
        bump(tScoreEl);
        haptic(cleared >= 4 ? 60 : 25);
        const ms = Math.floor(tScore / 200);
        if (ms > tCoinMilestone) { addCoins(ms - tCoinMilestone, false); tCoinMilestone = ms; }
        if (tryUpdateRecord('tetris_best', tScore, tBestEl, tBestBox)) toast('🏆 Новый рекорд: ' + tScore, 'record', 1400);
        else if (cleared === 4) toast('🎉 ТЕТРИС! +800', 'success', 1200);
        tDropInterval = Math.max(120, 700 - Math.floor(tLines / 5) * 80);
    }
}
function tetrisControl(action) {
    if (!tRunning) return;
    if (action === 'pause') { tPaused = !tPaused; tPauseBtn.textContent = tPaused ? 'ПРОДОЛЖИТЬ' : 'ПАУЗА'; haptic(10); return; }
    if (tPaused) return;
    if (action === 'left') { if (!collidesTetris(tCurrent.x - 1, tCurrent.y, tCurrent.shape)) tCurrent.x--; haptic(6); }
    else if (action === 'right') { if (!collidesTetris(tCurrent.x + 1, tCurrent.y, tCurrent.shape)) tCurrent.x++; haptic(6); }
    else if (action === 'rotate') {
        const rotated = rotateMatrix(tCurrent.shape);
        if (!collidesTetris(tCurrent.x, tCurrent.y, rotated)) tCurrent.shape = rotated;
        haptic(8);
    } else if (action === 'drop') {
        while (!collidesTetris(tCurrent.x, tCurrent.y + 1, tCurrent.shape)) tCurrent.y++;
        lockTetrisPiece();
        haptic(12);
    }
}
function rotateMatrix(m) {
    const rows = m.length, cols = m[0].length;
    const out = Array.from({length: cols}, () => Array(rows).fill(0));
    for (let r = 0; r < rows; r++) for (let c = 0; c < cols; c++) out[c][rows - 1 - r] = m[r][c];
    return out;
}
function tetrisLoop(t) {
    if (!tRunning) return;
    const dt = t - tLastTime;
    tLastTime = t;
    if (!tPaused) {
        tDropCounter += dt;
        if (tDropCounter > tDropInterval) {
            tDropCounter = 0;
            if (!collidesTetris(tCurrent.x, tCurrent.y + 1, tCurrent.shape)) tCurrent.y++;
            else lockTetrisPiece();
        }
    }
    drawTetris();
    tFrameId = requestAnimationFrame(tetrisLoop);
}
function gameOverTetris() {
    stopTetris();
    const coinsEarned = Math.floor(tScore / 200);
    toast('Игра окончена! Очки: ' + tScore + (coinsEarned ? ' (+' + coinsEarned + '🪙)' : ''), 'info', 2000);
    setTimeout(() => { if (currentScreen === 'tetris-screen') startTetris(); }, 1200);
}
function drawTetris() {
    tCtx.fillStyle = '#021208';
    tCtx.fillRect(0, 0, tCanvas.width, tCanvas.height);
    tCtx.strokeStyle = 'rgba(0,230,118,0.08)';
    for (let i = 1; i < T_COLS; i++) { tCtx.beginPath(); tCtx.moveTo(i * T_CELL, 0); tCtx.lineTo(i * T_CELL, tCanvas.height); tCtx.stroke(); }
    for (let i = 1; i < T_ROWS; i++) { tCtx.beginPath(); tCtx.moveTo(0, i * T_CELL); tCtx.lineTo(tCanvas.width, i * T_CELL); tCtx.stroke(); }
    for (let r = 0; r < T_ROWS; r++) for (let c = 0; c < T_COLS; c++) if (tGrid[r][c]) drawTetrisCell(c, r, tGrid[r][c]);
    if (tCurrent) for (let r = 0; r < tCurrent.shape.length; r++) for (let c = 0; c < tCurrent.shape[r].length; c++) if (tCurrent.shape[r][c]) drawTetrisCell(tCurrent.x + c, tCurrent.y + r, tCurrent.color);
    if (tNext) {
        const previewX = tCanvas.width - 60, previewY = 10;
        tCtx.fillStyle = 'rgba(0,0,0,0.6)';
        roundRect(tCtx, previewX - 6, previewY - 4, 56, 56, 8); tCtx.fill();
        tCtx.fillStyle = 'rgba(255,255,255,0.5)';
        tCtx.font = 'bold 9px system-ui';
        tCtx.textAlign = 'center';
        tCtx.fillText('ДАЛЕЕ', previewX + 22, previewY + 6);
        const cellSize = 10;
        const offX = previewX + 22 - (tNext.shape[0].length * cellSize) / 2;
        const offY = previewY + 16;
        for (let r = 0; r < tNext.shape.length; r++) for (let c = 0; c < tNext.shape[r].length; c++) if (tNext.shape[r][c]) { tCtx.fillStyle = tNext.color; tCtx.fillRect(offX + c * cellSize, offY + r * cellSize, cellSize - 1, cellSize - 1); }
    }
    if (tPaused) {
        tCtx.fillStyle = 'rgba(0,0,0,0.6)';
        tCtx.fillRect(0, 0, tCanvas.width, tCanvas.height);
        tCtx.fillStyle = '#fff';
        tCtx.font = 'bold 24px system-ui';
        tCtx.textAlign = 'center';
        tCtx.textBaseline = 'middle';
        tCtx.fillText('ПАУЗА', tCanvas.width/2, tCanvas.height/2);
    }
}
function drawTetrisCell(c, r, color) {
    const x = c * T_CELL, y = r * T_CELL;
    tCtx.fillStyle = color;
    tCtx.shadowColor = color;
    tCtx.shadowBlur = 8;
    roundRect(tCtx, x + 1, y + 1, T_CELL - 2, T_CELL - 2, 3); tCtx.fill();
    tCtx.shadowBlur = 0;
    tCtx.fillStyle = 'rgba(255,255,255,0.25)';
    roundRect(tCtx, x + 2, y + 2, T_CELL - 4, T_CELL * 0.35, 2); tCtx.fill();
}

/* ============================================================
   ЗАЩИТНИК БАШНИ
============================================================ */
const twCanvas = $('towerCanvas');
const twCtx = twCanvas.getContext('2d');
const twWaveEl = $('tower-wave');
const twGoldEl = $('tower-gold');
const twBestEl = $('tower-best');
const twBestBox = $('tower-best-box');
const TW_W = twCanvas.width, TW_H = twCanvas.height;
const TW_PATH = [{x: 0, y: 60}, {x: 120, y: 60}, {x: 120, y: 160}, {x: 220, y: 160}, {x: 220, y: 260}, {x: 80, y: 260}, {x: 80, y: 340}, {x: TW_W, y: 340}];
const TW_SLOTS = [{x: 60, y: 100}, {x: 90, y: 130}, {x: 150, y: 100}, {x: 180, y: 130}, {x: 60, y: 200}, {x: 90, y: 220}, {x: 150, y: 200}, {x: 180, y: 220}, {x: 60, y: 300}, {x: 130, y: 300}, {x: 180, y: 300}, {x: 240, y: 220}, {x: 250, y: 130}, {x: 250, y: 60}, {x: 170, y: 60}];
const TOWER_TYPES = {
    arrow: {name: 'Лучник', cost: 50, range: 80, damage: 8, fireRate: 400, color: '#8bc34a', projectileColor: '#cddc39'},
    fire: {name: 'Огонь', cost: 100, range: 60, damage: 20, fireRate: 800, color: '#ff5722', projectileColor: '#ff7043'},
    ice: {name: 'Лёд', cost: 75, range: 70, damage: 5, fireRate: 500, color: '#03a9f4', projectileColor: '#4fc3f7', slow: 0.5, slowDuration: 1500}
};
let twRunning = false, twFrameId = null, twLastTime = 0;
let twTowers = [], twEnemies = [], twProjectiles = [], twParticles = [];
let twGold = 200, twWave = 0, twWaveActive = false, twSelectedType = null, twLives = 20, twBest = 0;
let twCoinMilestone = 0, twSpawnQueue = [], twSpawnTimer = 0, twWaveCompletePending = false;
function startTower() {
    twTowers = []; twEnemies = []; twProjectiles = []; twParticles = [];
    twGold = 200; twWave = 0; twWaveActive = false; twSelectedType = null; twLives = 20;
    twSpawnQueue = []; twSpawnTimer = 0; twWaveCompletePending = false; twCoinMilestone = 0;
    twBest = getBest('tower_best');
    twWaveEl.textContent = '0';
    twGoldEl.textContent = twGold;
    twBestEl.textContent = twBest;
    TW_SLOTS.forEach(s => s.occupied = false);
    updateTowerTools();
    twRunning = true;
    twLastTime = performance.now();
    if (twFrameId) cancelAnimationFrame(twFrameId);
    twFrameId = requestAnimationFrame(towerLoop);
}
function stopTower() { twRunning = false; if (twFrameId) cancelAnimationFrame(twFrameId); twFrameId = null; }
function updateTowerTools() {
    document.querySelectorAll('.tool-btn[data-type]').forEach(btn => {
        const type = btn.dataset.type;
        btn.disabled = twGold < TOWER_TYPES[type].cost;
        btn.classList.toggle('selected', twSelectedType === type);
    });
}
function selectTower(type) {
    if (!twRunning) return;
    haptic(10);
    twSelectedType = twSelectedType === type ? null : type;
    updateTowerTools();
}
function startTowerWave() {
    if (!twRunning || twWaveActive) return;
    haptic(20);
    twWave++;
    twWaveEl.textContent = twWave;
    twWaveActive = true;
    twWaveCompletePending = false;
    const count = 5 + twWave * 2;
    const hp = 20 + twWave * 8;
    const speed = 0.6 + twWave * 0.05;
    twSpawnQueue = [];
    for (let i = 0; i < count; i++) twSpawnQueue.push({hp, speed, reward: 15 + twWave * 2});
    twSpawnTimer = 0;
}
function towerLoop(t) {
    if (!twRunning) return;
    const dt = Math.min(40, t - twLastTime);
    twLastTime = t;
    updateTower(dt, t);
    drawTower();
    twFrameId = requestAnimationFrame(towerLoop);
}
function towerClick(e) {
    if (!twRunning) return;
    const rect = twCanvas.getBoundingClientRect();
    const x = (e.clientX - rect.left) * (twCanvas.width / rect.width);
    const y = (e.clientY - rect.top) * (twCanvas.height / rect.height);
    for (const slot of TW_SLOTS) {
        if (Math.hypot(slot.x - x, slot.y - y) < 22) {
            if (slot.occupied) { toast('Здесь уже стоит башня', 'info', 900); return; }
            if (!twSelectedType) { toast('Сначала выберите башню', 'info', 1000); return; }
            const t = TOWER_TYPES[twSelectedType];
            if (twGold < t.cost) { toast('Не хватает золота', 'info', 900); return; }
            twGold -= t.cost;
            twGoldEl.textContent = twGold;
            bump(twGoldEl);
            twTowers.push({x: slot.x, y: slot.y, type: twSelectedType, ...t, lastShot: 0, angle: 0});
            slot.occupied = true;
            haptic(15);
            updateTowerTools();
            return;
        }
    }
}
function updateTower(dt, t) {
    if (twWaveActive && twSpawnQueue.length > 0) {
        twSpawnTimer -= dt;
        if (twSpawnTimer <= 0) {
            twSpawnTimer = 700;
            const e = twSpawnQueue.shift();
            twEnemies.push({x: TW_PATH[0].x, y: TW_PATH[0].y, pathIdx: 0, hp: e.hp, maxHp: e.hp, speed: e.speed, reward: e.reward, slowUntil: 0, slowFactor: 1});
        }
    }
    for (let i = twEnemies.length - 1; i >= 0; i--) {
        const e = twEnemies[i];
        const slowMul = t < e.slowUntil ? e.slowFactor : 1;
        const speed = e.speed * slowMul;
        const target = TW_PATH[e.pathIdx + 1];
        if (!target) { twEnemies.splice(i, 1); twLives--; haptic(60); if (twLives <= 0) { gameOverTower(); return; } continue; }
        const dx = target.x - e.x, dy = target.y - e.y;
        const dist = Math.hypot(dx, dy);
        const move = speed * dt * 0.08;
        if (dist <= move) { e.x = target.x; e.y = target.y; e.pathIdx++; }
        else { e.x += (dx / dist) * move; e.y += (dy / dist) * move; }
    }
    for (const tower of twTowers) {
        if (t - tower.lastShot < tower.fireRate) continue;
        let target = null, minDist = Infinity;
        for (const e of twEnemies) { const d = Math.hypot(e.x - tower.x, e.y - tower.y); if (d < tower.range && d < minDist) { minDist = d; target = e; } }
        if (target) {
            tower.lastShot = t;
            tower.angle = Math.atan2(target.y - tower.y, target.x - tower.x);
            twProjectiles.push({x: tower.x, y: tower.y, target, damage: tower.damage, speed: 5, color: tower.projectileColor, slow: tower.slow, slowDuration: tower.slowDuration});
        }
    }
    for (let i = twProjectiles.length - 1; i >= 0; i--) {
        const p = twProjectiles[i];
        if (!p.target || p.target.hp <= 0) { twProjectiles.splice(i, 1); continue; }
        const dx = p.target.x - p.x, dy = p.target.y - p.y;
        const dist = Math.hypot(dx, dy);
        const move = p.speed * dt * 0.15;
        if (dist <= move) {
            p.target.hp -= p.damage;
            if (p.slow) { p.target.slowUntil = t + p.slowDuration; p.target.slowFactor = p.slow; }
            for (let k = 0; k < 4; k++) twParticles.push({x: p.target.x, y: p.target.y, vx: (Math.random() - 0.5) * 3, vy: (Math.random() - 0.5) * 3, life: 1, size: 2 + Math.random() * 2, color: p.color});
            if (p.target.hp <= 0) {
                twGold += p.target.reward;
                twGoldEl.textContent = twGold;
                bump(twGoldEl);
                const ms = Math.floor((twGold - 200) / 100);
                if (ms > twCoinMilestone) { addCoins(ms - twCoinMilestone, false); twCoinMilestone = ms; }
                for (let k = 0; k < 8; k++) twParticles.push({x: p.target.x, y: p.target.y, vx: (Math.random() - 0.5) * 5, vy: (Math.random() - 0.5) * 5, life: 1, size: 2 + Math.random() * 2, color: '#ff5722'});
                const idx = twEnemies.indexOf(p.target);
                if (idx >= 0) twEnemies.splice(idx, 1);
                updateTowerTools();
            }
            twProjectiles.splice(i, 1);
        } else { p.x += (dx / dist) * move; p.y += (dy / dist) * move; }
    }
    for (let i = twParticles.length - 1; i >= 0; i--) {
        const p = twParticles[i];
        p.x += p.vx; p.y += p.vy; p.life -= 0.025;
        if (p.life <= 0) twParticles.splice(i, 1);
    }
    if (twWaveActive && twSpawnQueue.length === 0 && twEnemies.length === 0 && !twWaveCompletePending) {
        twWaveActive = false;
        twWaveCompletePending = true;
        const bonus = 30 + twWave * 5;
        twGold += bonus;
        twGoldEl.textContent = twGold;
        bump(twGoldEl);
        toast('🎉 Волна ' + twWave + ' пройдена! +' + bonus + '🪙 золота', 'success', 1600);
        if (twWave > twBest) { twBest = twWave; localStorage.setItem('tower_best', twBest); twBestEl.textContent = twBest; bump(twBestEl); }
        updateTowerTools();
    }
}
function gameOverTower() {
    stopTower();
    toast('Игра окончена! Волна: ' + twWave, 'info', 2000);
    setTimeout(() => { if (currentScreen === 'tower-screen') startTower(); }, 1200);
}
function drawTower() {
    const grad = twCtx.createLinearGradient(0, 0, 0, TW_H);
    grad.addColorStop(0, '#0f0602'); grad.addColorStop(1, '#050200');
    twCtx.fillStyle = grad;
    twCtx.fillRect(0, 0, TW_W, TW_H);
    twCtx.strokeStyle = 'rgba(255,193,7,0.3)';
    twCtx.lineWidth = 30;
    twCtx.lineCap = 'round';
    twCtx.lineJoin = 'round';
    twCtx.beginPath();
    twCtx.moveTo(TW_PATH[0].x, TW_PATH[0].y);
    for (let i = 1; i < TW_PATH.length; i++) twCtx.lineTo(TW_PATH[i].x, TW_PATH[i].y);
    twCtx.stroke();
    twCtx.fillStyle = '#4caf50';
    twCtx.beginPath(); twCtx.arc(TW_PATH[0].x, TW_PATH[0].y, 10, 0, Math.PI * 2); twCtx.fill();
    const end = TW_PATH[TW_PATH.length - 1];
    twCtx.fillStyle = '#f44336';
    twCtx.beginPath(); twCtx.arc(end.x, end.y, 12, 0, Math.PI * 2); twCtx.fill();
    twCtx.fillStyle = '#fff';
    twCtx.font = 'bold 12px system-ui';
    twCtx.textAlign = 'center';
    twCtx.textBaseline = 'middle';
    twCtx.fillText('🏠', end.x, end.y);
    for (const slot of TW_SLOTS) {
        if (slot.occupied) continue;
        twCtx.strokeStyle = 'rgba(255,255,255,0.2)';
        twCtx.lineWidth = 2;
        twCtx.setLineDash([4, 4]);
        twCtx.beginPath(); twCtx.arc(slot.x, slot.y, 18, 0, Math.PI * 2); twCtx.stroke();
        twCtx.setLineDash([]);
        if (twSelectedType) {
            const t = TOWER_TYPES[twSelectedType];
            twCtx.fillStyle = t.color;
            twCtx.globalAlpha = 0.15;
            twCtx.beginPath(); twCtx.arc(slot.x, slot.y, t.range, 0, Math.PI * 2); twCtx.fill();
            twCtx.globalAlpha = 1;
        }
    }
    for (const tower of twTowers) {
        twCtx.fillStyle = tower.color;
        twCtx.globalAlpha = 0.08;
        twCtx.beginPath(); twCtx.arc(tower.x, tower.y, tower.range, 0, Math.PI * 2); twCtx.fill();
        twCtx.globalAlpha = 1;
        twCtx.fillStyle = tower.color;
        twCtx.shadowColor = tower.color;
        twCtx.shadowBlur = 10;
        twCtx.beginPath(); twCtx.arc(tower.x, tower.y, 14, 0, Math.PI * 2); twCtx.fill();
        twCtx.shadowBlur = 0;
        twCtx.strokeStyle = '#333';
        twCtx.lineWidth = 4;
        twCtx.beginPath();
        twCtx.moveTo(tower.x, tower.y);
        twCtx.lineTo(tower.x + Math.cos(tower.angle) * 16, tower.y + Math.sin(tower.angle) * 16);
        twCtx.stroke();
        twCtx.fillStyle = '#000';
        twCtx.font = 'bold 12px system-ui';
        twCtx.textAlign = 'center';
        twCtx.textBaseline = 'middle';
        const icon = tower.type === 'arrow' ? '🏹' : tower.type === 'fire' ? '🔥' : '❄️';
        twCtx.fillText(icon, tower.x, tower.y);
    }
    for (const e of twEnemies) {
        const hpPct = e.hp / e.maxHp;
        const isSlowed = performance.now() < e.slowUntil;
        twCtx.fillStyle = isSlowed ? '#4fc3f7' : '#e53935';
        twCtx.shadowColor = twCtx.fillStyle;
        twCtx.shadowBlur = 8;
        twCtx.beginPath(); twCtx.arc(e.x, e.y, 12, 0, Math.PI * 2); twCtx.fill();
        twCtx.shadowBlur = 0;
        twCtx.fillStyle = '#fff';
        twCtx.beginPath(); twCtx.arc(e.x - 3, e.y - 2, 2, 0, Math.PI * 2); twCtx.fill();
        twCtx.beginPath(); twCtx.arc(e.x + 3, e.y - 2, 2, 0, Math.PI * 2); twCtx.fill();
        twCtx.fillStyle = 'rgba(0,0,0,0.5)';
        twCtx.fillRect(e.x - 12, e.y - 20, 24, 4);
        twCtx.fillStyle = hpPct > 0.5 ? '#4caf50' : hpPct > 0.25 ? '#ff9800' : '#f44336';
        twCtx.fillRect(e.x - 12, e.y - 20, 24 * hpPct, 4);
    }
    for (const p of twProjectiles) {
        twCtx.fillStyle = p.color;
        twCtx.shadowColor = p.color;
        twCtx.shadowBlur = 8;
        twCtx.beginPath(); twCtx.arc(p.x, p.y, 4, 0, Math.PI * 2); twCtx.fill();
        twCtx.shadowBlur = 0;
    }
    for (const p of twParticles) {
        twCtx.globalAlpha = p.life;
        twCtx.fillStyle = p.color;
        twCtx.beginPath(); twCtx.arc(p.x, p.y, p.size, 0, Math.PI * 2); twCtx.fill();
    }
    twCtx.globalAlpha = 1;
    twCtx.fillStyle = '#ff5722';
    twCtx.font = 'bold 14px system-ui';
    twCtx.textAlign = 'left';
    twCtx.textBaseline = 'top';
    twCtx.fillText('🏠 ' + twLives, 8, 6);
    if (twWaveActive) {
        twCtx.fillStyle = '#ffd54f';
        twCtx.font = 'bold 13px system-ui';
        twCtx.textAlign = 'right';
        twCtx.fillText('Волна ' + twWave + ' идёт', TW_W - 8, 8);
    } else if (twWave > 0) {
        twCtx.fillStyle = '#4caf50';
        twCtx.font = 'bold 13px system-ui';
        twCtx.textAlign = 'right';
        twCtx.fillText('✅ Волна ' + twWave + ' пройдена', TW_W - 8, 8);
    }
}

/* ============================================================
   ТАНКОВАЯ ДУЭЛЬ (на двоих)
============================================================ */
const duelCanvas = $('duelCanvas');
const duelCtx = duelCanvas.getContext('2d');
const duelS1El = $('duel-s1');
const duelS2El = $('duel-s2');
const DUEL_W = duelCanvas.width, DUEL_H = duelCanvas.height;
let duelRunning = false, duelFrameId = null, duelLastTime = 0;
let duelTanks = [];
let duelBullets = [];
let duelParticles = [];
let duelWins = [0, 0];        // победы каждого
let duelRoundActive = true;
let duelWinner = null;
let duelRespawnTimer = 0;

function startDuel() {
    duelWins = [0, 0];
    duelS1El.textContent = '0';
    duelS2El.textContent = '0';
    duelReset();
    duelRunning = true;
    duelLastTime = performance.now();
    if (duelFrameId) cancelAnimationFrame(duelFrameId);
    duelFrameId = requestAnimationFrame(duelLoop);
}
function stopDuel() {
    duelRunning = false;
    if (duelFrameId) cancelAnimationFrame(duelFrameId);
    duelFrameId = null;
}
function duelReset() {
    duelTanks = [
        { id: 0, x: 60, y: DUEL_H - 60, angle: 0, color: '#e91e63', hp: 3, maxHp: 3, side: 'p1', dir: 0 },
        { id: 1, x: DUEL_W - 60, y: 60, angle: Math.PI, color: '#00e5ff', hp: 3, maxHp: 3, side: 'p2', dir: 0 }
    ];
    duelBullets = [];
    duelParticles = [];
    duelRoundActive = true;
    duelWinner = null;
    haptic(15);
    toast('🔔 Раунд начался!', 'info', 1000);
}
function duelControl(action) {
    if (!duelRunning || !duelRoundActive) return;
    const t1 = duelTanks[0];
    const t2 = duelTanks[1];
    if (action === 'p1-left') { t1.dir = -1; haptic(5); }
    else if (action === 'p1-right') { t1.dir = 1; haptic(5); }
    else if (action === 'p1-fire') { duelFire(t1); haptic(10); }
    else if (action === 'p2-left') { t2.dir = -1; haptic(5); }
    else if (action === 'p2-right') { t2.dir = 1; haptic(5); }
    else if (action === 'p2-fire') { duelFire(t2); haptic(10); }
}
function duelFire(tank) {
    const now = performance.now();
    if (tank.lastShot && now - tank.lastShot < 500) return;
    tank.lastShot = now;
    // Стреляем в сторону противоположного танка по горизонтали и вертикали
    const angle = tank.side === 'p1' ? -Math.PI / 4 * (tank.angle === 0 ? 1 : 1) : -Math.PI * 3 / 4;
    // Проще: стреляем вверх-вправо для p1 и вниз-влево для p2
    let vx, vy;
    if (tank.side === 'p1') { vx = 3.5; vy = -3.5; }
    else { vx = -3.5; vy = 3.5; }
    duelBullets.push({
        x: tank.x, y: tank.y,
        vx: vx, vy: vy,
        owner: tank.side,
        color: tank.color,
        life: 0
    });
}
function duelLoop(t) {
    if (!duelRunning) return;
    const dt = Math.min(40, t - duelLastTime);
    duelLastTime = t;
    if (duelRoundActive) updateDuel(dt, t);
    drawDuel();
    duelFrameId = requestAnimationFrame(duelLoop);
}
function updateDuel(dt, t) {
    // Движение танков
    for (const tank of duelTanks) {
        if (tank.dir !== 0) {
            tank.x += tank.dir * 0.32 * dt;
            tank.x = Math.max(30, Math.min(DUEL_W - 30, tank.x));
            tank.angle = tank.dir === 0 ? tank.angle : 0;
        }
    }
    // Пули
    for (let i = duelBullets.length - 1; i >= 0; i--) {
        const b = duelBullets[i];
        b.x += b.vx * dt * 0.06;
        b.y += b.vy * dt * 0.06;
        b.life += dt;
        // Отскок от стен
        if (b.x < 8) { b.x = 8; b.vx = Math.abs(b.vx); }
        if (b.x > DUEL_W - 8) { b.x = DUEL_W - 8; b.vx = -Math.abs(b.vx); }
        if (b.y < 8) { b.y = 8; b.vy = Math.abs(b.vy); }
        if (b.y > DUEL_H - 8) { b.y = DUEL_H - 8; b.vy = -Math.abs(b.vy); }

        // Попадание в танк
        for (const tank of duelTanks) {
            if (tank.side === b.owner) continue;
            if (Math.abs(b.x - tank.x) < 22 && Math.abs(b.y - tank.y) < 22) {
                tank.hp--;
                haptic(40);
                for (let k = 0; k < 12; k++) {
                    duelParticles.push({
                        x: tank.x + (Math.random() - 0.5) * 30,
                        y: tank.y + (Math.random() - 0.5) * 30,
                        vx: (Math.random() - 0.5) * 6,
                        vy: (Math.random() - 0.5) * 6,
                        life: 1, size: 3, color: tank.color
                    });
                }
                duelBullets.splice(i, 1);
                if (tank.hp <= 0) {
                    duelRoundEnd(tank.side === 'p1' ? 'p2' : 'p1');
                }
                break;
            }
        }
        // Долго летит — убираем
        if (b.life > 6000 || b.x < -20 || b.x > DUEL_W + 20 || b.y < -20 || b.y > DUEL_H + 20) {
            duelBullets.splice(i, 1);
        }
    }
    // Частицы
    for (let i = duelParticles.length - 1; i >= 0; i--) {
        const p = duelParticles[i];
        p.x += p.vx; p.y += p.vy; p.life -= 0.03;
        if (p.life <= 0) duelParticles.splice(i, 1);
    }
    // Автовосстановление
    if (duelWinner) {
        duelRespawnTimer += dt;
        if (duelRespawnTimer > 1500) {
            duelRespawnTimer = 0;
            duelReset();
        }
    }
}
function duelRoundEnd(winnerSide) {
    duelRoundActive = false;
    duelWinner = winnerSide;
    haptic(80);
    if (winnerSide === 'p1') {
        duelWins[0]++;
        duelS1El.textContent = duelWins[0];
        bump(duelS1El);
        toast('🏆 Игрок 1 побеждает!', 'success', 1800);
    } else {
        duelWins[1]++;
        duelS2El.textContent = duelWins[1];
        bump(duelS2El);
        toast('🏆 Игрок 2 побеждает!', 'success', 1800);
    }
    // Награда монет
    addCoins(5, false);
    if (duelWins[0] >= 3 || duelWins[1] >= 3) {
        const champ = duelWins[0] >= 3 ? 'Игрок 1' : 'Игрок 2';
        setTimeout(() => {
            toast('👑 ' + champ + ' выиграл матч!', 'record', 2500);
        }, 1800);
    }
}
function drawDuel() {
    // Фон
    const grad = duelCtx.createLinearGradient(0, 0, 0, DUEL_H);
    grad.addColorStop(0, '#0f0408');
    grad.addColorStop(1, '#050202');
    duelCtx.fillStyle = grad;
    duelCtx.fillRect(0, 0, DUEL_W, DUEL_H);

    // Диагональная линия-разделитель
    duelCtx.strokeStyle = 'rgba(255,255,255,0.08)';
    duelCtx.lineWidth = 2;
    duelCtx.setLineDash([8, 8]);
    duelCtx.beginPath();
    duelCtx.moveTo(0, 0); duelCtx.lineTo(DUEL_W, DUEL_H);
    duelCtx.moveTo(DUEL_W, 0); duelCtx.lineTo(0, DUEL_H);
    duelCtx.stroke();
    duelCtx.setLineDash([]);

    // Рамка
    duelCtx.strokeStyle = 'rgba(255,255,255,0.15)';
    duelCtx.lineWidth = 4;
    duelCtx.strokeRect(2, 2, DUEL_W - 4, DUEL_H - 4);

    // Танки
    for (const tank of duelTanks) {
        duelCtx.save();
        duelCtx.translate(tank.x, tank.y);
        // Корпус
        duelCtx.fillStyle = tank.color;
        duelCtx.shadowColor = tank.color;
        duelCtx.shadowBlur = 14;
        roundRect(duelCtx, -18, -18, 36, 36, 6);
        duelCtx.fill();
        duelCtx.shadowBlur = 0;
        // Башня
        duelCtx.fillStyle = '#222';
        duelCtx.beginPath();
        duelCtx.arc(0, 0, 10, 0, Math.PI * 2);
        duelCtx.fill();
        // Ствол — направлен по диагонали к противнику
        duelCtx.strokeStyle = '#111';
        duelCtx.lineWidth = 5;
        duelCtx.lineCap = 'round';
        duelCtx.beginPath();
        if (tank.side === 'p1') { duelCtx.moveTo(0, 0); duelCtx.lineTo(14, -14); }
        else { duelCtx.moveTo(0, 0); duelCtx.lineTo(-14, 14); }
        duelCtx.stroke();
        duelCtx.restore();
        // HP-бар
        duelCtx.fillStyle = 'rgba(0,0,0,0.5)';
        duelCtx.fillRect(tank.x - 20, tank.y - 30, 40, 5);
        duelCtx.fillStyle = tank.color;
        duelCtx.fillRect(tank.x - 20, tank.y - 30, 40 * (tank.hp / tank.maxHp), 5);
    }

    // Пули
    for (const b of duelBullets) {
        duelCtx.fillStyle = b.color;
        duelCtx.shadowColor = b.color;
        duelCtx.shadowBlur = 12;
        duelCtx.beginPath();
        duelCtx.arc(b.x, b.y, 5, 0, Math.PI * 2);
        duelCtx.fill();
        duelCtx.shadowBlur = 0;
    }

    // Частицы
    for (const p of duelParticles) {
        duelCtx.globalAlpha = p.life;
        duelCtx.fillStyle = p.color;
        duelCtx.beginPath();
        duelCtx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
        duelCtx.fill();
    }
    duelCtx.globalAlpha = 1;

    // Надпись победителя
    if (duelWinner) {
        duelCtx.fillStyle = 'rgba(0,0,0,0.6)';
        duelCtx.fillRect(0, DUEL_H/2 - 40, DUEL_W, 80);
        duelCtx.fillStyle = duelWinner === 'p1' ? '#e91e63' : '#00e5ff';
        duelCtx.font = 'bold 32px system-ui';
        duelCtx.textAlign = 'center';
        duelCtx.textBaseline = 'middle';
        duelCtx.fillText(duelWinner === 'p1' ? '🔴 П1 ПОБЕДИЛ' : '🔵 П2 ПОБЕДИЛ', DUEL_W/2, DUEL_H/2);
    }
}

/* ============================================================
   РЕАКЦИЯ-ДУЭЛЬ (на двоих)
============================================================ */
const duel2Canvas = $('duel2Canvas');
const duel2Ctx = duel2Canvas.getContext('2d');
const duel2S1El = $('duel2-s1');
const duel2S2El = $('duel2-s2');
const duel2RoundEl = $('duel2-round');
const duel2Btn = $('duel2Btn');
const duel2Side1 = $('duel2-side1');
const duel2Side2 = $('duel2-side2');
const DUEL2_W = duel2Canvas.width, DUEL2_H = duel2Canvas.height;

let duel2Running = false, duel2FrameId = null, duel2LastTime = 0;
let duel2State = 'idle'; // idle | waiting | ready | round-end | match-end
let duel2Round = 0;
let duel2Wins = [0, 0];
let duel2StartTime = 0;
let duel2Timeout = null;
let duel2WinnerRound = null;
let duel2Countdown = 0;

function startDuel2() {
    duel2Wins = [0, 0];
    duel2Round = 0;
    duel2S1El.textContent = '0';
    duel2S2El.textContent = '0';
    duel2RoundEl.textContent = '0';
    duel2State = 'idle';
    duel2WinnerRound = null;
    duel2Btn.textContent = 'НАЧАТЬ РАУНД';
    duel2Side1.classList.remove('flash');
    duel2Side2.classList.remove('flash');
    duel2Side1.innerHTML = '🔴 ИГРОК 1<br><small>ЖДИ...</small>';
    duel2Side2.innerHTML = '🔵 ИГРОК 2<br><small>ЖДИ...</small>';
    duel2Running = true;
    duel2LastTime = performance.now();
    if (duel2FrameId) cancelAnimationFrame(duel2FrameId);
    duel2FrameId = requestAnimationFrame(duel2Loop);
}
function stopDuel2() {
    duel2Running = false;
    clearTimeout(duel2Timeout);
    if (duel2FrameId) cancelAnimationFrame(duel2FrameId);
    duel2FrameId = null;
}
function duel2Start() {
    if (!duel2Running) return;
    if (duel2State === 'match-end') { startDuel2(); return; }
    if (duel2State === 'waiting' || duel2State === 'ready') return;
    duel2Round++;
    if (duel2Round > 5) duel2Round = 5;
    duel2RoundEl.textContent = duel2Round;
    duel2State = 'waiting';
    duel2Btn.textContent = 'ЖДИТЕ...';
    duel2WinnerRound = null;
    duel2Side1.classList.remove('flash');
    duel2Side2.classList.remove('flash');
    duel2Side1.innerHTML = '🔴 ИГРОК 1<br><small>ЖДИ...</small>';
    duel2Side2.innerHTML = '🔵 ИГРОК 2<br><small>ЖДИ...</small>';
    haptic(15);
    const delay = 1500 + Math.random() * 3000;
    duel2Timeout = setTimeout(() => {
        if (duel2State !== 'waiting') return;
        duel2State = 'ready';
        duel2StartTime = performance.now();
        duel2Btn.textContent = 'ЖМИ!';
        duel2Side1.classList.add('flash');
        duel2Side2.classList.add('flash');
        duel2Side1.innerHTML = '🔴 ЖМИ!';
        duel2Side2.innerHTML = '🔵 ЖМИ!';
        haptic(40);
    }, delay);
}
function duel2Tap(side) {
    if (!duel2Running) return;
    if (duel2State === 'waiting') {
        // Нажали рано
        clearTimeout(duel2Timeout);
        duel2State = 'round-end';
        duel2WinnerRound = side === 'p1' ? 'p2' : 'p1'; // кто НЕ нажал — побеждает
        duel2EndRound();
        return;
    }
    if (duel2State !== 'ready') return;
    const t = performance.now() - duel2StartTime;
    duel2State = 'round-end';
    duel2WinnerRound = side;
    duel2EndRound(t);
}
function duel2EndRound(time) {
    if (duel2WinnerRound === 'p1') {
        duel2Wins[0]++;
        duel2S1El.textContent = duel2Wins[0];
        bump(duel2S1El);
        toast('🔴 Игрок 1 выиграл раунд! ' + (time ? Math.round(time) + ' мс' : 'Соперник рано нажал'), 'success', 1600);
        duel2Side1.innerHTML = '🔴 ПОБЕДА!';
        duel2Side2.innerHTML = '🔵 УВЫ';
        duel2Side1.classList.remove('flash');
        duel2Side2.classList.remove('flash');
    } else {
        duel2Wins[1]++;
        duel2S2El.textContent = duel2Wins[1];
        bump(duel2S2El);
        toast('🔵 Игрок 2 выиграл раунд! ' + (time ? Math.round(time) + ' мс' : 'Соперник рано нажал'), 'success', 1600);
        duel2Side2.innerHTML = '🔵 ПОБЕДА!';
        duel2Side1.innerHTML = '🔴 УВЫ';
        duel2Side1.classList.remove('flash');
        duel2Side2.classList.remove('flash');
    }
    haptic(30);
    // 3 победы = матч
    if (duel2Wins[0] >= 3 || duel2Wins[1] >= 3) {
        duel2State = 'match-end';
        duel2Btn.textContent = 'ИГРАТЬ СНОВА';
        const champ = duel2Wins[0] >= 3 ? '🔴 Игрок 1' : '🔵 Игрок 2';
        setTimeout(() => toast('👑 ' + champ + ' выиграл матч!', 'record', 2500), 1000);
    } else {
        duel2State = 'idle';
        duel2Btn.textContent = 'СЛЕДУЮЩИЙ РАУНД';
    }
}
function duel2Loop(t) {
    if (!duel2Running) return;
    duel2LastTime = t;
    drawDuel2();
    duel2FrameId = requestAnimationFrame(duel2Loop);
}
function drawDuel2() {
    duel2Ctx.fillStyle = '#04080f';
    duel2Ctx.fillRect(0, 0, DUEL2_W, DUEL2_H);
    // Левая половина
    duel2Ctx.fillStyle = duel2State === 'ready' ? 'rgba(233,30,99,0.4)' : 'rgba(233,30,99,0.08)';
    duel2Ctx.fillRect(0, 0, DUEL2_W / 2, DUEL2_H);
    // Правая половина
    duel2Ctx.fillStyle = duel2State === 'ready' ? 'rgba(0,229,255,0.4)' : 'rgba(0,229,255,0.08)';
    duel2Ctx.fillRect(DUEL2_W / 2, 0, DUEL2_W / 2, DUEL2_H);
    // Разделитель
    duel2Ctx.strokeStyle = 'rgba(255,255,255,0.4)';
    duel2Ctx.lineWidth = 2;
    duel2Ctx.beginPath();
    duel2Ctx.moveTo(DUEL2_W / 2, 0);
    duel2Ctx.lineTo(DUEL2_W / 2, DUEL2_H);
    duel2Ctx.stroke();
    // Текст
    duel2Ctx.fillStyle = '#fff';
    duel2Ctx.font = 'bold 26px system-ui';
    duel2Ctx.textAlign = 'center';
    duel2Ctx.textBaseline = 'middle';
    let text = '';
    if (duel2State === 'idle') text = 'Нажмите «Начать раунд»';
    else if (duel2State === 'waiting') text = '⏳ ЖДИТЕ...';
    else if (duel2State === 'ready') text = '⚡ ЖМИ!';
    else if (duel2State === 'round-end') text = duel2WinnerRound === 'p1' ? '🔴 П1 выиграл' : '🔵 П2 выиграл';
    else if (duel2State === 'match-end') text = duel2Wins[0] >= 3 ? '🔴 П1 ЧЕМПИОН!' : '🔵 П2 ЧЕМПИОН!';
    duel2Ctx.fillText(text, DUEL2_W / 2, DUEL2_H / 2);
    // Крупные надписи сторон
    duel2Ctx.font = 'bold 20px system-ui';
    duel2Ctx.fillStyle = 'rgba(233,30,99,0.8)';
    duel2Ctx.fillText('ИГРОК 1', DUEL2_W / 4, 40);
    duel2Ctx.fillStyle = 'rgba(0,229,255,0.8)';
    duel2Ctx.fillText('ИГРОК 2', DUEL2_W * 3 / 4, 40);
    duel2Ctx.font = 'bold 36px system-ui';
    duel2Ctx.fillStyle = 'rgba(255,255,255,0.15)';
    duel2Ctx.fillText(duel2Wins[0], DUEL2_W / 4, DUEL2_H - 40);
    duel2Ctx.fillText(duel2Wins[1], DUEL2_W * 3 / 4, DUEL2_H - 40);
}

/* ============================================================
   СВАЙПЫ + КЛИКИ
============================================================ */
function attachSwipe(canvas, handler, threshold = 24) {
    let sx = 0, sy = 0, tracking = false;
    canvas.addEventListener('touchstart', e => {
        const t = e.touches[0];
        sx = t.clientX; sy = t.clientY; tracking = true;
    }, {passive: true});
    canvas.addEventListener('touchend', e => {
        if (!tracking) return;
        tracking = false;
        const t = e.changedTouches[0];
        const dx = t.clientX - sx, dy = t.clientY - sy;
        if (Math.abs(dx) < threshold && Math.abs(dy) < threshold) return;
        if (Math.abs(dx) > Math.abs(dy)) handler(dx > 0 ? 'right' : 'left');
        else handler(dy > 0 ? 'down' : 'up');
    }, {passive: true});
}
attachSwipe(sCanvas, dir => {
    if (dir === 'up') setSnakeDir(0, -1);
    else if (dir === 'down') setSnakeDir(0, 1);
    else if (dir === 'left') setSnakeDir(-1, 0);
    else if (dir === 'right') setSnakeDir(1, 0);
});
attachSwipe(canvas2048, dir => move2048(dir));
attachSwipe(mCanvas, dir => moveMatch3(dir));
attachSwipe(tCanvas, dir => {
    if (dir === 'left') tetrisControl('left');
    else if (dir === 'right') tetrisControl('right');
    else if (dir === 'down') tetrisControl('drop');
    else if (dir === 'up') tetrisControl('rotate');
});
mCanvas.addEventListener('click', match3Click);
mCanvas.addEventListener('touchstart', e => { e.preventDefault(); const t = e.changedTouches[0]; match3Click({ clientX: t.clientX, clientY: t.clientY }); }, {passive: false});
pCanvas.addEventListener('click', puzzleClick);
pCanvas.addEventListener('touchstart', e => { e.preventDefault(); const t = e.changedTouches[0]; puzzleClick({ clientX: t.clientX, clientY: t.clientY }); }, {passive: false});
twCanvas.addEventListener('click', towerClick);
twCanvas.addEventListener('touchstart', e => { e.preventDefault(); const t = e.changedTouches[0]; towerClick({ clientX: t.clientX, clientY: t.clientY }); }, {passive: false});
flappyCanvas.addEventListener('click', flappyFlap);
flappyCanvas.addEventListener('touchstart', e => { e.preventDefault(); flappyFlap(); }, {passive: false});

/* ============================================================
   КЛАВИАТУРА
============================================================ */
document.addEventListener('keydown', e => {
    const dirMap = {'ArrowUp':'up','ArrowDown':'down','ArrowLeft':'left','ArrowRight':'right','w':'up','s':'down','a':'left','d':'right'};
    const dir = dirMap[e.key];
    // Для танковой дуэли: WASD для P1, стрелки для P2
    if (currentScreen === 'duel-screen') {
        if (e.key === 'a' || e.key === 'A' || e.key === 'ф' || e.key === 'Ф') duelControl('p1-left');
        else if (e.key === 'd' || e.key === 'D' || e.key === 'в' || e.key === 'В') duelControl('p1-right');
        else if (e.key === ' ') duelControl('p1-fire');
        else if (e.key === 'ArrowLeft') duelControl('p2-left');
        else if (e.key === 'ArrowRight') duelControl('p2-right');
        else if (e.key === 'ArrowUp' || e.key === 'Enter') duelControl('p2-fire');
        if ([' ', 'ArrowLeft', 'ArrowRight', 'ArrowUp', 'ArrowDown', 'a', 'A', 'd', 'D', 'ф', 'Ф', 'в', 'В'].includes(e.key)) {
            e.preventDefault();
        }
        return;
    }
    // Для реакции-дуэли: Q/A для P1, P/L для P2
    if (currentScreen === 'duel2-screen') {
        if (e.key === 'a' || e.key === 'A' || e.key === 'ф' || e.key === 'Ф') { duel2Tap('p1'); e.preventDefault(); }
        else if (e.key === 'l' || e.key === 'L' || e.key === 'д' || e.key === 'Д') { duel2Tap('p2'); e.preventDefault(); }
        else if (e.key === ' ') { duel2Start(); e.preventDefault(); }
        return;
    }
    if (!dir) {
        if (e.key === ' ' || e.key === 'Enter') {
            if (currentScreen === 'reaction-screen') reactionTap();
            else if (currentScreen === 'shooter-screen') shooterControl('fire');
            else if (currentScreen === 'arknoid-screen') arknoidControl('fire');
            else if (currentScreen === 'tetris-screen') tetrisControl('drop');
            else if (currentScreen === 'tower-screen') startTowerWave();
            else if (currentScreen === 'flappy-screen') flappyFlap();
            else if (currentScreen === 'race-screen') raceControl('boost');
        }
        return;
    }
    e.preventDefault();
    if (currentScreen === 'snake-screen') {
        if (dir === 'up') setSnakeDir(0, -1);
        else if (dir === 'down') setSnakeDir(0, 1);
        else if (dir === 'left') setSnakeDir(-1, 0);
        else if (dir === 'right') setSnakeDir(1, 0);
    } else if (currentScreen === 'game2048-screen') move2048(dir);
    else if (currentScreen === 'match3-screen') moveMatch3(dir);
    else if (currentScreen === 'shooter-screen') {
        if (dir === 'left') shooterControl('left');
        else if (dir === 'right') shooterControl('right');
    } else if (currentScreen === 'arknoid-screen') {
        if (dir === 'left') arknoidControl('left');
        else if (dir === 'right') arknoidControl('right');
    } else if (currentScreen === 'tetris-screen') {
        if (dir === 'left') tetrisControl('left');
        else if (dir === 'right') tetrisControl('right');
        else if (dir === 'down') tetrisControl('drop');
        else if (dir === 'up') tetrisControl('rotate');
    } else if (currentScreen === 'race-screen') {
        if (dir === 'left') raceControl('left');
        else if (dir === 'right') raceControl('right');
    }
});
document.addEventListener('keyup', e => {
    if (currentScreen === 'shooter-screen' && (e.key === 'ArrowLeft' || e.key === 'ArrowRight' || e.key === 'a' || e.key === 'd')) shDir = 0;
    if (currentScreen === 'arknoid-screen' && (e.key === 'ArrowLeft' || e.key === 'ArrowRight' || e.key === 'a' || e.key === 'd')) arkDir = 0;
    if (currentScreen === 'race-screen' && (e.key === 'ArrowLeft' || e.key === 'ArrowRight' || e.key === 'a' || e.key === 'd')) raceDir = 0;
});

/* ============================================================
   СТАРТ
============================================================ */
updateBestScoresUI();
updatePremiumTags();
updateTowerTools();
</script>
</body>
</html>

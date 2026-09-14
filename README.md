<!DOCTYPE html><html lang="ru"><head><meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1.0,user-scalable=no"><title>GAME HUB</title><style>:root{--bg:#0f0f13;--card:rgba(30,30,40,0.85);--cb:rgba(255,255,255,0.06);--gold:#ffd54f;--t:#fff;--ts:#9a9aa8;--sh:0 10px 30px rgba(0,0,0,0.4)}*{box-sizing:border-box}body{background:radial-gradient(circle at 20% 0%,#1a1a2e 0%,#0f0f13 60%);background-attachment:fixed;color:var(--t);font-family:system-ui,sans-serif;margin:0;padding:0;display:flex;flex-direction:column;align-items:center;min-height:100vh;overflow-x:hidden}.screen{display:none;width:100%;max-width:500px;padding:16px;flex-direction:column;align-items:center}.screen.active{display:flex}.hdr{width:100%;display:flex;justify-content:space-between;align-items:center;margin-bottom:4px}h1{text-align:center;margin:8px 0 0;font-size:30px;font-weight:800;letter-spacing:2px;background:linear-gradient(90deg,#4caf50,#ff9800,#9c27b0,#00bcd4,#f44336,#3f51b5,#00e676,#ff5722,#ff4081);-webkit-background-clip:text;background-clip:text;color:transparent}.coin{display:inline-flex;align-items:center;gap:6px;background:linear-gradient(135deg,rgba(255,193,7,0.15),rgba(255,152,0,0.1));border:1px solid rgba(255,193,7,0.4);color:var(--gold);padding:6px 12px;border-radius:20px;font-weight:800;font-size:15px}.coin.bump{animation:cb 0.4s ease}@keyframes cb{0%{transform:scale(1)}50%{transform:scale(1.25)}100%{transform:scale(1)}}.ad{width:100%;margin-top:14px;background:linear-gradient(135deg,rgba(255,64,129,0.15),rgba(156,39,176,0.1));border:1px solid rgba(255,64,129,0.4);border-radius:16px;padding:14px 16px;display:flex;align-items:center;gap:12px;cursor:pointer;box-shadow:0 6px 20px rgba(255,64,129,0.15)}.ad:active{transform:scale(0.97)}.ad-i{font-size:28px}.ad-b{flex:1;text-align:left}.ad-b h4{margin:0 0 3px 0;font-size:15px;font-weight:800;color:#ff4081}.ad-b p{margin:0;font-size:12px;color:var(--ts)}.ad-r{background:linear-gradient(135deg,#ffc107,#ff9800);color:#1a1200;font-weight:800;font-size:13px;padding:6px 10px;border-radius:12px;white-space:nowrap}.tabs{display:flex;gap:8px;width:100%;margin-top:18px;background:rgba(255,255,255,0.03);border:1px solid rgba(255,255,255,0.08);border-radius:14px;padding:5px}.tab{flex:1;text-align:center;padding:10px 8px;border-radius:10px;font-weight:700;font-size:14px;cursor:pointer;color:var(--ts)}.tab.active{background:linear-gradient(135deg,rgba(76,175,80,0.25),rgba(0,188,212,0.2));color:#fff}.tc{display:none;width:100%}.tc.active{display:block}.st{width:100%;margin:20px 0 6px;font-size:14px;font-weight:700;letter-spacing:1.5px;color:var(--ts);text-transform:uppercase;display:flex;align-items:center;gap:10px}.st::after{content:"";flex:1;height:1px;background:linear-gradient(90deg,rgba(255,255,255,0.12),transparent)}.st.p{color:var(--gold)}.st.d{color:#e91e63}.gm{display:flex;flex-direction:column;gap:12px;width:100%}.gc{background:var(--card);border:1px solid var(--cb);border-radius:18px;padding:16px 18px;display:flex;align-items:center;justify-content:space-between;cursor:pointer;box-shadow:var(--sh)}.gc:active{transform:scale(0.97)}.c1{border-left:3px solid #4caf50}.c2{border-left:3px solid #ff9800}.c3{border-left:3px solid #9c27b0}.c4{border-left:3px solid #00bcd4}.c5{border-left:3px solid #f44336}.c6{border-left:3px solid #3f51b5}.c7{border-left:3px solid #7e57c2}.cp{border-left:3px solid #ffc107;background:linear-gradient(135deg,rgba(255,193,7,0.08),rgba(156,39,176,0.08)),var(--card)}.ct{border-left:3px solid #00e676;background:linear-gradient(135deg,rgba(0,230,118,0.08),rgba(0,188,212,0.08)),var(--card)}.ctw{border-left:3px solid #ff5722;background:linear-gradient(135deg,rgba(255,87,34,0.08),rgba(255,193,7,0.08)),var(--card)}.crpg{border-left:3px solid #8bc34a;background:linear-gradient(135deg,rgba(139,195,74,0.08),rgba(76,175,80,0.08)),var(--card)}.cgl{border-left:3px solid #d32f2f;background:linear-gradient(135deg,rgba(211,47,47,0.08),rgba(255,152,0,0.08)),var(--card)}.cr{border-left:3px solid #ff3d00}.cf{border-left:3px solid #ffc400}.cd{border-left:3px solid #e91e63}.cd2{border-left:3px solid #00e5ff}.cpp{border-left:3px solid #26c6da}.ctt{border-left:3px solid #ef6c00}.gi h3{margin:0 0 4px 0;font-size:18px;font-weight:700}.gi p{margin:0;color:var(--ts);font-size:13px}.ico{font-size:32px}.pt{display:inline-flex;align-items:center;gap:4px;background:linear-gradient(135deg,#ffc107,#ff9800);color:#1a1200;font-weight:800;font-size:13px;padding:4px 10px;border-radius:12px;margin-top:4px}.pt.tp{background:linear-gradient(135deg,#00e676,#00b8d4);color:#001a0a}.pt.tw{background:linear-gradient(135deg,#ff5722,#ff9800);color:#1a0a00}.pt.rp{background:linear-gradient(135deg,#8bc34a,#4caf50);color:#0a1a00}.pt.gl{background:linear-gradient(135deg,#d32f2f,#ff9800);color:#fff}.pt.o{background:linear-gradient(135deg,#66bb6a,#2e7d32);color:#fff}.bb{align-self:flex-start;background:rgba(255,255,255,0.06);color:#fff;border:1px solid rgba(255,255,255,0.1);padding:10px 18px;border-radius:10px;font-size:15px;font-weight:600;margin-bottom:15px;cursor:pointer}.rb{position:absolute;top:16px;right:16px;background:rgba(244,67,54,0.15);color:#f44336;border:1px solid rgba(244,67,54,0.4);padding:6px 12px;border-radius:8px;font-size:12px;font-weight:700;cursor:pointer}.sc{display:flex;gap:8px;margin-bottom:12px;font-size:13px;width:100%;justify-content:center;flex-wrap:wrap}.sb{background:var(--card);padding:8px 12px;border-radius:10px;border:1px solid var(--cb);text-align:center;flex:1;min-width:70px}.sb.r{border-color:rgba(255,213,79,0.5)}.sv{font-weight:800;color:#fff;display:block;font-size:18px}.sv.bump{animation:b 0.4s ease}@keyframes b{0%{transform:scale(1)}50%{transform:scale(1.35);color:#ffd54f}100%{transform:scale(1)}}canvas{border-radius:12px;max-width:100%;height:auto;display:block;box-shadow:var(--sh);touch-action:none}#snakeCanvas{border:2px solid rgba(76,175,80,0.5);background:#060a06}#c2048{border:2px solid rgba(255,152,0,0.5);background:#1a1610}#match3Canvas{border:2px solid rgba(156,39,176,0.5);background:#100812}#reactionCanvas{border:2px solid rgba(0,188,212,0.5);background:#041014}#puzzleCanvas{border:2px solid rgba(244,67,54,0.5);background:#140606}#arknoidCanvas{border:2px solid rgba(63,81,181,0.5);background:#04060f}#shooterCanvas{border:2px solid rgba(255,193,7,0.5);background:#000510}#tetrisCanvas{border:2px solid rgba(0,230,118,0.5);background:#021208}#towerCanvas{border:2px solid rgba(255,87,34,0.5);background:#0f0602}#raceCanvas{border:2px solid rgba(255,61,0,0.5);background:#1a0a00}#flappyCanvas{border:2px solid rgba(255,196,0,0.5);background:#041a2e}#duelCanvas{border:2px solid rgba(233,30,99,0.5);background:#0f0408}#duel2Canvas{border:2px solid rgba(0,229,255,0.5);background:#04080f}#memoryCanvas{border:2px solid rgba(126,87,194,0.5);background:#0a0612}#rpgSnakeCanvas{border:2px solid rgba(139,195,74,0.5);background:#041004}#gladiatorCanvas{border:2px solid rgba(211,47,47,0.5);background:#140404}#pingCanvas{border:2px solid rgba(38,198,218,0.5);background:#041016}#tttCanvas{border:2px solid rgba(239,108,0,0.5);background:#1a0a00}.ctrl{display:grid;grid-template-areas:". up ." "l . r" ". d .";gap:10px;margin-top:20px;width:210px}.btn{background:rgba(255,255,255,0.06);color:#fff;border:1px solid rgba(255,255,255,0.12);border-radius:14px;padding:18px;font-size:22px;font-weight:bold;cursor:pointer}.btn:active{transform:scale(0.9)}.up{grid-area:up}.dn{grid-area:d}.lf{grid-area:l}.rt{grid-area:r}.bab{margin-top:14px;padding:14px 30px;font-size:16px;font-weight:800;border:none;border-radius:14px;cursor:pointer;color:#fff;background:linear-gradient(135deg,#00bcd4,#0097a7)}.bab:active{transform:scale(0.94)}.bab.ps{background:linear-gradient(135deg,#f44336,#c62828)}.bab.tb{background:linear-gradient(135deg,#00e676,#00b8d4);color:#001a0a}.bab.fb{background:linear-gradient(135deg,#ffc400,#ff9800);color:#1a1200}.bab.db{background:linear-gradient(135deg,#e91e63,#9c27b0)}.bab.d2{background:linear-gradient(135deg,#00e5ff,#0077ff);color:#001a2a}.bab.rp{background:linear-gradient(135deg,#8bc34a,#4caf50);color:#0a1a00}.bab.gl{background:linear-gradient(135deg,#d32f2f,#b71c1c)}.bab.pp{background:linear-gradient(135deg,#26c6da,#00838f);color:#001a1a}.bab.tt{background:linear-gradient(135deg,#ef6c00,#e65100)}.ht{margin-top:12px;font-size:13px;color:var(--ts);text-align:center;max-width:380px}.tst{position:fixed;top:20px;left:50%;transform:translateX(-50%) translateY(-100px);background:rgba(30,30,40,0.95);border:1px solid rgba(255,255,255,0.1);padding:14px 24px;border-radius:14px;font-size:15px;font-weight:600;z-index:1000;opacity:0;transition:transform 0.4s,opacity 0.3s;pointer-events:none;text-align:center}.tst.show{transform:translateX(-50%) translateY(0);opacity:1}.tst.s{border-color:rgba(76,175,80,0.5)}.tst.i{border-color:rgba(255,152,0,0.5)}.tst.r{border-color:rgba(255,213,79,0.7);background:rgba(50,40,10,0.95)}.tst.c{border-color:rgba(255,193,7,0.7);color:var(--gold)}.tst.a{border-color:rgba(255,64,129,0.7);color:#ff4081}.tst.sv{border-color:rgba(0,188,212,0.7);color:#4dd0e1}.mo{position:fixed;inset:0;background:rgba(0,0,0,0.7);display:none;align-items:center;justify-content:center;z-index:999;padding:20px}.mo.show{display:flex}.md,.rm,.am{background:linear-gradient(160deg,#1e1e2e,#141420);border-radius:22px;padding:26px 22px;max-width:360px;width:100%;text-align:center;border:1px solid rgba(255,193,7,0.3)}.mi{font-size:56px;margin-bottom:6px}.md h2,.rm h2,.am h2{margin:4px 0 8px;font-size:22px}.md p,.rm p{color:var(--ts);font-size:14px;margin:6px 0 18px}.mp{font-size:22px;font-weight:800;color:var(--gold);margin-bottom:18px}.mbt{display:flex;gap:10px}.mb{flex:1;padding:14px;border-radius:12px;border:none;font-weight:700;font-size:15px;cursor:pointer}.mb.c{background:rgba(255,255,255,0.08);color:#fff}.mb.b{background:linear-gradient(135deg,#ffc107,#ff9800);color:#1a1200}.mb.rs{background:linear-gradient(135deg,#00bcd4,#0097a7);color:#fff}.mb.n{background:rgba(255,255,255,0.08);color:#fff}.mb.b:disabled{opacity:0.5}.rs-st{color:var(--gold);font-weight:700;font-size:15px;margin:10px 0 18px}.am-ch{color:var(--ts);font-size:13px;margin:0 0 14px}.am-ch strong{color:#ff4081}.ad-sc{position:relative;width:100%;aspect-ratio:16/11;background:linear-gradient(135deg,#1a0a2e,#0a0620);border-radius:14px;overflow:hidden;margin-bottom:14px;border:1px solid rgba(255,64,129,0.2)}.ad-sl{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;padding:16px;opacity:0;text-align:center}.ad-sl.act{opacity:1}.ad-si{font-size:42px;margin-bottom:6px}.ad-st{font-size:18px;font-weight:800;margin:0 0 6px;color:#ff4081}.ad-sx{font-size:12px;color:#ccc;margin:0 0 8px}.ad-stg{display:inline-block;margin-bottom:8px;padding:3px 10px;background:rgba(255,64,129,0.15);border:1px solid rgba(255,64,129,0.4);border-radius:10px;font-size:10px;font-weight:700;color:#ff4081}.ad-sa{display:flex;gap:6px;flex-wrap:wrap;justify-content:center}.ad-sb{display:inline-flex;padding:8px 14px;border-radius:10px;font-weight:700;font-size:12px;text-decoration:none;color:#fff}.ad-sb.vk{background:linear-gradient(135deg,#0077ff,#0055cc)}.ad-sb.vd{background:linear-gradient(135deg,#ff4081,#9c27b0)}.ad-pd{display:flex;justify-content:center;gap:6px;margin-bottom:12px}.ad-d{width:8px;height:8px;border-radius:50%;background:rgba(255,255,255,0.15)}.ad-d.act{background:#ff4081}.ad-d.dn{background:rgba(255,64,129,0.5)}.ad-tb{width:100%;height:6px;background:rgba(255,255,255,0.1);border-radius:3px;overflow:hidden;margin-bottom:12px}.ad-tf{height:100%;background:linear-gradient(90deg,#ff4081,#9c27b0);width:0%;transition:width 1s linear}.ad-st2{font-size:14px;color:var(--ts);margin-bottom:14px;min-height:20px}.ad-st2 strong{color:var(--gold)}.ad-mb{display:flex;gap:10px}.ad-mbtn{flex:1;padding:14px;border-radius:12px;border:none;font-weight:700;font-size:15px;cursor:pointer}.ad-mbtn.c{background:rgba(255,255,255,0.08);color:#fff}.ad-mbtn.cl{background:linear-gradient(135deg,#ff4081,#9c27b0);color:#fff}.ad-mbtn.cl:disabled{opacity:0.5}.tt{display:grid;grid-template-columns:repeat(4,1fr);gap:6px;margin-top:10px;width:100%;max-width:400px}.tbt{background:rgba(255,255,255,0.06);border:1px solid rgba(255,255,255,0.12);border-radius:12px;padding:8px 4px;color:#fff;display:flex;flex-direction:column;align-items:center;gap:2px;cursor:pointer;font-family:inherit}.tbt.sel{background:rgba(255,87,34,0.25);border-color:#ff5722}.tbt:disabled{opacity:0.4}.tbi{font-size:18px}.tbn{font-size:9px;font-weight:700}.tbc{font-size:10px;font-weight:800;color:var(--gold);background:rgba(255,193,7,0.15);padding:1px 5px;border-radius:6px}.tbs{background:linear-gradient(135deg,rgba(0,230,118,0.2),rgba(0,188,212,0.15))}.tbm{background:linear-gradient(135deg,rgba(156,39,176,0.2),rgba(255,193,7,0.15))}.dc{display:flex;gap:8px;margin-top:14px;width:100%;justify-content:space-between}.dp{flex:1;display:flex;flex-direction:column;gap:6px;padding:8px;border-radius:14px}.dp.p1{background:rgba(233,30,99,0.1);border:1px solid rgba(233,30,99,0.3)}.dp.p2{background:rgba(0,229,255,0.1);border:1px solid rgba(0,229,255,0.3)}.dl{font-size:12px;font-weight:800;text-align:center}.dp.p1 .dl{color:#e91e63}.dp.p2 .dl{color:#00e5ff}.dr{display:flex;gap:6px}.db{flex:1;padding:14px 4px;border-radius:10px;border:none;background:rgba(255,255,255,0.08);color:#fff;font-size:16px;font-weight:800;cursor:pointer}.db.p1{background:rgba(233,30,99,0.25)}.db.p2{background:rgba(0,229,255,0.25)}.db:active{transform:scale(0.9)}.d2s{display:flex;width:100%;gap:8px;margin-top:14px}.d2sd{flex:1;padding:30px 10px;border-radius:16px;text-align:center;font-weight:800;font-size:18px;cursor:pointer;border:2px solid}.d2sd.p1{background:rgba(233,30,99,0.2);border-color:#e91e63;color:#ff80ab}.d2sd.p1.fl{background:#e91e63;color:#fff}.d2sd.p2{background:rgba(0,229,255,0.2);border-color:#00e5ff;color:#80deea}.d2sd.p2.fl{background:#00e5ff;color:#003040}.ppctrl{display:flex;gap:8px;margin-top:14px;width:100%}.ppside{flex:1;display:flex;flex-direction:column;gap:6px;padding:8px;border-radius:14px;align-items:center}.ppside.p1{background:rgba(38,198,218,0.1);border:1px solid rgba(38,198,218,0.3)}.ppside.p2{background:rgba(239,108,0,0.1);border:1px solid rgba(239,108,0,0.3)}.ppb{width:100%;padding:18px;border-radius:12px;border:none;background:rgba(255,255,255,0.08);color:#fff;font-size:22px;font-weight:800;cursor:pointer}.ppside.p1 .ppb{background:rgba(38,198,218,0.3)}.ppside.p2 .ppb{background:rgba(239,108,0,0.3)}.ppb:active{transform:scale(0.9)}</style></head><body>
<div id="toast" class="tst"></div>
<div class="mo" id="buyModal"><div class="md"><div class="mi" id="modalIcon">🚀</div><h2 id="modalTitle">Космический Шутер</h2><p id="modalDesc"></p><div class="mp"><span>🪙</span><span id="modalPrice">200</span></div><div class="mbt"><button class="mb c" onclick="closeBuyModal()">Отмена</button><button class="mb b" id="modalBuyBtn" onclick="confirmBuy()">Купить</button></div></div></div>
<div class="mo" id="adModal"><div class="am"><h2>📺 Реклама</h2><p class="am-ch">Канал: <strong>Dley перезаливы</strong> · VK Video</p><div class="ad-sc" id="adSlideContainer"></div><div class="ad-pd" id="adDots"></div><div class="ad-tb"><div class="ad-tf" id="adTimerFill"></div></div><div class="ad-st2" id="adStatus">Смотрите рекламу <strong>15 секунд</strong></div><div class="ad-mb"><button class="ad-mbtn c" onclick="closeAdModal()">Закрыть</button><button class="ad-mbtn cl" id="adClaimBtn" onclick="claimAdReward()" disabled>Получить 40 🪙</button></div></div></div>
<div class="mo" id="resumeModal"><div class="rm"><div class="mi">💾</div><h2>Найден прогресс</h2><p>Продолжить с того же места?</p><div class="rs-st" id="resumeStats"></div><div class="mbt"><button class="mb n" onclick="resumeChoice('new')">🔄 Заново</button><button class="mb rs" onclick="resumeChoice('continue')">▶ Продолжить</button></div></div></div>
<div id="menu-screen" class="screen active">
<div class="hdr"><h1>GAME HUB</h1><div class="coin" id="coinBadge"><span>🪙</span><span id="coinCount">0</span></div></div>
<div class="ad" onclick="openAdModal()"><div class="ad-i">📺</div><div class="ad-b"><h4>Смотреть рекламу</h4><p>Канал Dley перезаливы · VK Video</p></div><div class="ad-r">+40 🪙</div></div>
<div class="tabs"><div class="tab active" onclick="switchTab('solo')" id="tab-solo">🎮 Игры</div><div class="tab" onclick="switchTab('duo')" id="tab-duo">👥 На двоих</div></div>
<div class="tc active" id="tab-content-solo">
<div class="st">Бесплатные игры</div>
<div class="gm">
<div class="gc c1" onclick="openGame('snake-screen')"><div class="gi"><h3>Змейка</h3><p>Рекорд: <span id="menu-snake-best">0</span></p></div><div class="ico">🐍</div></div>
<div class="gc c2" onclick="openGame('game2048-screen')"><div class="gi"><h3>2048</h3><p>Рекорд: <span id="menu-2048-best">0</span></p></div><div class="ico">🔢</div></div>
<div class="gc c3" onclick="openGame('match3-screen')"><div class="gi"><h3>3 в ряд</h3><p>Рекорд: <span id="menu-match3-best">0</span></p></div><div class="ico">💎</div></div>
<div class="gc c4" onclick="openGame('reaction-screen')"><div class="gi"><h3>Реакция</h3><p>Лучшее: <span id="menu-reaction-best">—</span></p></div><div class="ico">⚡</div></div>
<div class="gc c5" onclick="openGame('puzzle-screen')"><div class="gi"><h3>Пятнашки</h3><p>Рекорд: <span id="menu-puzzle-best">0</span> ходов</p></div><div class="ico">🧩</div></div>
<div class="gc c6" onclick="openGame('arknoid-screen')"><div class="gi"><h3>Арканоид</h3><p>Рекорд: <span id="menu-arknoid-best">0</span></p></div><div class="ico">🧱</div></div>
<div class="gc c7" onclick="openGame('memory-screen')"><div class="gi"><h3>Мемо</h3><p>Рекорд: <span id="menu-memory-best">0</span> ходов</p></div><div class="ico">🧠</div></div>
<div class="gc cr" onclick="openGame('race-screen')"><div class="gi"><h3>Гонки</h3><p>Рекорд: <span id="menu-race-best">0</span></p></div><div class="ico">🏎</div></div>
<div class="gc cf" onclick="openGame('flappy-screen')"><div class="gi"><h3>Flappy Bird</h3><p>Рекорд: <span id="menu-flappy-best">0</span></p></div><div class="ico">🐦</div></div>
</div>
<div class="st p">💎 Премиум игры</div>
<div class="gm">
<div class="gc crpg" onclick="onPremiumClick('rpgSnake')"><div class="gi"><h3>Змейка-РПГ</h3><p>Сюжетная змейка с уровнями</p><div class="pt rp" id="rpgSnakePriceTag">🪙 250</div></div><div class="ico">🐉</div></div>
<div class="gc cgl" onclick="onPremiumClick('gladiator')"><div class="gi"><h3>Арена Гладиаторов</h3><p>Бой с волнами врагов</p><div class="pt gl" id="gladiatorPriceTag">🪙 250</div></div><div class="ico">⚔</div></div>
<div class="gc cp" onclick="onPremiumClick('shooter')"><div class="gi"><h3>Космический Шутер</h3><p>Волны врагов, боссы</p><div class="pt" id="shooterPriceTag">🪙 200</div></div><div class="ico">🚀</div></div>
<div class="gc ct" onclick="onPremiumClick('tetris')"><div class="gi"><h3>Тетрис</h3><p>Классика</p><div class="pt tp" id="tetrisPriceTag">🪙 250</div></div><div class="ico">🧊</div></div>
<div class="gc ctw" onclick="onPremiumClick('tower')"><div class="gi"><h3>Защитник Базы</h3><p>Tower Defense</p><div class="pt tw" id="towerPriceTag">🪙 300</div></div><div class="ico">🛡️</div></div>
</div>
</div>
<div class="tc" id="tab-content-duo">
<div class="st d">Игры на двоих</div>
<div class="gm">
<div class="gc cd" onclick="openGame('duel-screen')"><div class="gi"><h3>Танчики</h3><p>Разрушаемые блоки, 4 стороны</p></div><div class="ico">⚔</div></div>
<div class="gc cd2" onclick="openGame('duel2-screen')"><div class="gi"><h3>Реакция-дуэль</h3><p>Кто быстрее нажмёт</p></div><div class="ico">⚡</div></div>
<div class="gc cpp" onclick="openGame('ping-screen')"><div class="gi"><h3>Пинг-понг</h3><p>До 7 очков</p></div><div class="ico">🏓</div></div>
<div class="gc ctt" onclick="openGame('ttt-screen')"><div class="gi"><h3>Крестики-нолики</h3><p>3×3 · до 3 побед</p></div><div class="ico">⭕</div></div>
</div>
</div>
</div>

<div id="snake-screen" class="screen"><button class="bb" onclick="closeGame('snake-screen')">◀ Меню</button><button class="rb" onclick="resetGame('snake')">🔄 Сброс</button><div class="sc"><div class="sb">Очки <span id="snake-score" class="sv">0</span></div><div class="sb r" id="snake-best-box">Рекорд <span id="snake-best" class="sv">0</span></div></div><canvas id="snakeCanvas" width="320" height="320"></canvas><div class="ctrl"><button class="btn up" onpointerdown="setSnakeDir(0,-1)">▲</button><button class="btn lf" onpointerdown="setSnakeDir(-1,0)">◀</button><button class="btn rt" onpointerdown="setSnakeDir(1,0)">▶</button><button class="btn dn" onpointerdown="setSnakeDir(0,1)">▼</button></div></div>
<div id="game2048-screen" class="screen"><button class="bb" onclick="closeGame('game2048-screen')">◀ Меню</button><button class="rb" onclick="resetGame('2048')">🔄 Сброс</button><div class="sc"><div class="sb">Счет <span id="score2048" class="sv">0</span></div><div class="sb r" id="best2048-box">Рекорд <span id="best2048" class="sv">0</span></div></div><canvas id="c2048" width="320" height="320"></canvas><div class="ctrl"><button class="btn up" onpointerdown="move2048('up')">▲</button><button class="btn lf" onpointerdown="move2048('left')">◀</button><button class="btn rt" onpointerdown="move2048('right')">▶</button><button class="btn dn" onpointerdown="move2048('down')">▼</button></div></div>
<div id="match3-screen" class="screen"><button class="bb" onclick="closeGame('match3-screen')">◀ Меню</button><button class="rb" onclick="resetGame('match3')">🔄 Сброс</button><div class="sc"><div class="sb">Очки <span id="match3-score" class="sv">0</span></div><div class="sb r" id="match3-best-box">Рекорд <span id="match3-best" class="sv">0</span></div></div><canvas id="match3Canvas" width="320" height="320"></canvas><div class="ctrl"><button class="btn up" onpointerdown="moveMatch3('up')">▲</button><button class="btn lf" onpointerdown="moveMatch3('left')">◀</button><button class="btn rt" onpointerdown="moveMatch3('right')">▶</button><button class="btn dn" onpointerdown="moveMatch3('down')">▼</button></div></div>
<div id="reaction-screen" class="screen"><button class="bb" onclick="closeGame('reaction-screen')">◀ Меню</button><div class="sc"><div class="sb">Время <span id="reaction-time" class="sv">—</span></div><div class="sb r" id="reaction-best-box">Лучшее <span id="reaction-best" class="sv">—</span></div></div><canvas id="reactionCanvas" width="320" height="320"></canvas><button class="bab" id="reactionBtn" onpointerdown="reactionTap(event)">СТАРТ</button></div>
<div id="puzzle-screen" class="screen"><button class="bb" onclick="closeGame('puzzle-screen')">◀ Меню</button><button class="rb" onclick="resetGame('puzzle')">🔄 Сброс</button><div class="sc"><div class="sb">Ходы <span id="puzzle-moves" class="sv">0</span></div><div class="sb r" id="puzzle-best-box">Рекорд <span id="puzzle-best" class="sv">0</span></div></div><canvas id="puzzleCanvas" width="320" height="320"></canvas><button class="bab ps" onpointerdown="startPuzzle()">ПЕРЕМЕШАТЬ</button></div>
<div id="arknoid-screen" class="screen"><button class="bb" onclick="closeGame('arknoid-screen')">◀ Меню</button><button class="rb" onclick="resetGame('arknoid')">🔄 Сброс</button><div class="sc"><div class="sb">Очки <span id="arknoid-score" class="sv">0</span></div><div class="sb">Уровень <span id="arknoid-level" class="sv">1</span></div><div class="sb r" id="arknoid-best-box">Рекорд <span id="arknoid-best" class="sv">0</span></div></div><canvas id="arknoidCanvas" width="320" height="380"></canvas><div class="ctrl"><button class="btn up" onpointerdown="arknoidControl('fire')">🔥</button><button class="btn lf" onpointerdown="arknoidControl('left')">◀</button><button class="btn rt" onpointerdown="arknoidControl('right')">▶</button><button class="btn dn" onpointerdown="arknoidControl('pause')">⏸</button></div></div>
<div id="memory-screen" class="screen"><button class="bb" onclick="closeGame('memory-screen')">◀ Меню</button><button class="rb" onclick="resetGame('memory')">🔄 Сброс</button><div class="sc"><div class="sb">Ходы <span id="memory-moves" class="sv">0</span></div><div class="sb">Пары <span id="memory-pairs" class="sv">0/8</span></div><div class="sb r" id="memory-best-box">Рекорд <span id="memory-best" class="sv">0</span></div></div><canvas id="memoryCanvas" width="340" height="340"></canvas><button class="bab" onpointerdown="memoryShuffle()">🔄 ПЕРЕМЕШАТЬ</button></div>
<div id="race-screen" class="screen"><button class="bb" onclick="closeGame('race-screen')">◀ Меню</button><div class="sc"><div class="sb">Очки <span id="race-score" class="sv">0</span></div><div class="sb r" id="race-best-box">Рекорд <span id="race-best" class="sv">0</span></div></div><canvas id="raceCanvas" width="320" height="440"></canvas><div class="ctrl"><button class="btn up" onpointerdown="raceControl('pause')">⏸</button><button class="btn lf" onpointerdown="raceControl('left')">◀</button><button class="btn rt" onpointerdown="raceControl('right')">▶</button><button class="btn dn" onpointerdown="raceControl('boost')">⚡</button></div></div>
<div id="flappy-screen" class="screen"><button class="bb" onclick="closeGame('flappy-screen')">◀ Меню</button><div class="sc"><div class="sb">Очки <span id="flappy-score" class="sv">0</span></div><div class="sb r" id="flappy-best-box">Рекорд <span id="flappy-best" class="sv">0</span></div></div><canvas id="flappyCanvas" width="320" height="440"></canvas><button class="bab fb" onpointerdown="flappyFlap(event)">ЛЕТЕТЬ</button></div>
<div id="shooter-screen" class="screen"><button class="bb" onclick="closeGame('shooter-screen')">◀ Меню</button><button class="rb" onclick="resetGame('shooter')">🔄 Сброс</button><div class="sc"><div class="sb">Очки <span id="shooter-score" class="sv">0</span></div><div class="sb r" id="shooter-best-box">Рекорд <span id="shooter-best" class="sv">0</span></div></div><canvas id="shooterCanvas" width="320" height="380"></canvas><div class="ctrl"><button class="btn up" onpointerdown="shooterControl('fire')">🔥</button><button class="btn lf" onpointerdown="shooterControl('left')">◀</button><button class="btn rt" onpointerdown="shooterControl('right')">▶</button><button class="btn dn" onpointerdown="shooterControl('pause')">⏸</button></div></div>
<div id="tetris-screen" class="screen"><button class="bb" onclick="closeGame('tetris-screen')">◀ Меню</button><button class="rb" onclick="resetGame('tetris')">🔄 Сброс</button><div class="sc"><div class="sb">Очки <span id="tetris-score" class="sv">0</span></div><div class="sb r" id="tetris-best-box">Рекорд <span id="tetris-best" class="sv">0</span></div></div><canvas id="tetrisCanvas" width="240" height="380"></canvas><div class="ctrl"><button class="btn up" onpointerdown="tetrisControl('rotate')">🔄</button><button class="btn lf" onpointerdown="tetrisControl('left')">◀</button><button class="btn rt" onpointerdown="tetrisControl('right')">▶</button><button class="btn dn" onpointerdown="tetrisControl('drop')">⬇</button></div><button class="bab tb" id="tetrisPauseBtn" onpointerdown="tetrisControl('pause')">ПАУЗА</button></div>
<div id="tower-screen" class="screen"><button class="bb" onclick="closeGame('tower-screen')">◀ Меню</button><button class="rb" onclick="resetGame('tower')">🔄 Сброс</button><div class="sc"><div class="sb">Волна <span id="tower-wave" class="sv">0</span></div><div class="sb">🪙 <span id="tower-gold" class="sv">0</span></div><div class="sb">❤ <span id="tower-hp" class="sv">100</span></div><div class="sb r" id="tower-best-box">Рекорд <span id="tower-best" class="sv">0</span></div></div><canvas id="towerCanvas" width="400" height="500"></canvas><div class="tt"><button class="tbt" data-type="arrow" onpointerdown="selectTower('arrow')"><span class="tbi">🏹</span><span class="tbn">Лучник</span><span class="tbc">50</span></button><button class="tbt" data-type="fire" onpointerdown="selectTower('fire')"><span class="tbi">🔥</span><span class="tbn">Огонь</span><span class="tbc">100</span></button><button class="tbt" data-type="ice" onpointerdown="selectTower('ice')"><span class="tbi">❄️</span><span class="tbn">Лёд</span><span class="tbc">75</span></button><button class="tbt tbs" onpointerdown="startTowerWave()"><span class="tbi">▶</span><span class="tbn">Волна</span><span class="tbc">GO</span></button></div><div class="tt" style="margin-top:6px"><button class="tbt tbm" onpointerdown="toggleMergeMode()"><span class="tbi">🔗</span><span class="tbn">Слияние</span><span class="tbc" id="mergeModeLabel">OFF</span></button><button class="tbt" onpointerdown="towerAbility('bomb')"><span class="tbi">💣</span><span class="tbn">Бомба</span><span class="tbc">200</span></button><button class="tbt" onpointerdown="towerAbility('freeze')"><span class="tbi">🧊</span><span class="tbn">Заморозка</span><span class="tbc">150</span></button><button class="tbt" onpointerdown="towerAbility('heal')"><span class="tbi">💚</span><span class="tbn">Лечить</span><span class="tbc">100</span></button></div></div>
<div id="rpgSnake-screen" class="screen"><button class="bb" onclick="closeGame('rpgSnake-screen')">◀ Меню</button><button class="rb" onclick="resetGame('rpgSnake')">🔄 Сброс</button><div class="sc"><div class="sb">HP <span id="rpgSnake-hp" class="sv">5</span></div><div class="sb">Уровень <span id="rpgSnake-level" class="sv">1</span></div><div class="sb">Очки <span id="rpgSnake-score" class="sv">0</span></div></div><canvas id="rpgSnakeCanvas" width="360" height="360"></canvas><div class="ctrl"><button class="btn up" onpointerdown="rpgSnakeDir(0,-1)">▲</button><button class="btn lf" onpointerdown="rpgSnakeDir(-1,0)">◀</button><button class="btn rt" onpointerdown="rpgSnakeDir(1,0)">▶</button><button class="btn dn" onpointerdown="rpgSnakeDir(0,1)">▼</button></div><div class="ht">Собирай 💎, сражайся с 👹. Растёт сложность!</div></div>
<div id="gladiator-screen" class="screen"><button class="bb" onclick="closeGame('gladiator-screen')">◀ Меню</button><button class="rb" onclick="resetGame('gladiator')">🔄 Сброс</button><div class="sc"><div class="sb">HP <span id="gl-hp" class="sv">100</span></div><div class="sb">Волна <span id="gl-wave" class="sv">0</span></div><div class="sb r" id="gl-best-box">Рекорд <span id="gl-best" class="sv">0</span></div></div><canvas id="gladiatorCanvas" width="360" height="400"></canvas><div class="ctrl"><button class="btn up" onpointerdown="glControl('attack')">⚔</button><button class="btn lf" onpointerdown="glControl('left')">◀</button><button class="btn rt" onpointerdown="glControl('right')">▶</button><button class="btn dn" onpointerdown="glControl('block')">🛡</button></div><div class="ht">Атакуй ⚔, блокируй 🛡. Побеждай врагов!</div></div>
<div id="duel-screen" class="screen"><button class="bb" onclick="closeGame('duel-screen')">◀ Меню</button><div class="sc"><div class="sb">🔴 П1: <span id="duel-s1" class="sv">0</span></div><div class="sb">Раунд <span id="duel-round" class="sv">0</span></div><div class="sb">🔵 П2: <span id="duel-s2" class="sv">0</span></div></div><canvas id="duelCanvas" width="440" height="440"></canvas><div class="dc"><div class="dp p1"><div class="dl">🔴 ИГРОК 1</div><div class="dr"><button class="db p1" onpointerdown="duelControl('p1-left')">◀</button><button class="db p1" onpointerdown="duelControl('p1-up')">▲</button><button class="db p1" onpointerdown="duelControl('p1-down')">▼</button><button class="db p1" onpointerdown="duelControl('p1-right')">▶</button></div><div class="dr"><button class="db p1" onpointerdown="duelControl('p1-fire')">🔥</button></div></div><div class="dp p2"><div class="dl">🔵 ИГРОК 2</div><div class="dr"><button class="db p2" onpointerdown="duelControl('p2-left')">◀</button><button class="db p2" onpointerdown="duelControl('p2-up')">▲</button><button class="db p2" onpointerdown="duelControl('p2-down')">▼</button><button class="db p2" onpointerdown="duelControl('p2-right')">▶</button></div><div class="dr"><button class="db p2" onpointerdown="duelControl('p2-fire')">🔥</button></div></div></div><button class="bab db" onclick="duelNewMatch()">🔄 НОВЫЙ МАТЧ</button></div>
<div id="duel2-screen" class="screen"><button class="bb" onclick="closeGame('duel2-screen')">◀ Меню</button><div class="sc"><div class="sb">🔴 П1: <span id="duel2-s1" class="sv">0</span></div><div class="sb">Раунд <span id="duel2-round" class="sv">0</span>/5</div><div class="sb">🔵 П2: <span id="duel2-s2" class="sv">0</span></div></div><canvas id="duel2Canvas" width="400" height="280"></canvas><div class="d2s"><div class="d2sd p1" id="duel2-side1" onpointerdown="duel2Tap('p1')">🔴 ИГРОК 1<br><small>ЖДИ...</small></div><div class="d2sd p2" id="duel2-side2" onpointerdown="duel2Tap('p2')">🔵 ИГРОК 2<br><small>ЖДИ...</small></div></div><button class="bab d2" id="duel2Btn" onclick="duel2Start()">НАЧАТЬ РАУНД</button></div>
<div id="ping-screen" class="screen"><button class="bb" onclick="closeGame('ping-screen')">◀ Меню</button><div class="sc"><div class="sb">🟦 П1: <span id="ping-s1" class="sv">0</span></div><div class="sb r" id="ping-best-box">До 7</div><div class="sb">🟧 П2: <span id="ping-s2" class="sv">0</span></div></div><canvas id="pingCanvas" width="360" height="480"></canvas><div class="ppctrl"><div class="ppside p1"><div class="dl">🟦 ИГРОК 1</div><button class="ppb" onpointerdown="pingControl('p1-up')" onpointerup="pingControl('p1-stop')">▲</button><button class="ppb" onpointerdown="pingControl('p1-down')" onpointerup="pingControl('p1-stop')">▼</button></div><div class="ppside p2"><div class="dl">🟧 ИГРОК 2</div><button class="ppb" onpointerdown="pingControl('p2-up')" onpointerup="pingControl('p2-stop')">▲</button><button class="ppb" onpointerdown="pingControl('p2-down')" onpointerup="pingControl('p2-stop')">▼</button></div></div><button class="bab pp" onclick="pingNewMatch()">🔄 НОВЫЙ МАТЧ</button></div>
<div id="ttt-screen" class="screen"><button class="bb" onclick="closeGame('ttt-screen')">◀ Меню</button><div class="sc"><div class="sb">🔴 X: <span id="ttt-s1" class="sv">0</span></div><div class="sb">Раунд <span id="ttt-round" class="sv">0</span></div><div class="sb">🔵 O: <span id="ttt-s2" class="sv">0</span></div></div><canvas id="tttCanvas" width="340" height="340"></canvas><div class="ht" id="tttStatus">Ход: 🔴 X (Игрок 1)</div><button class="bab tt" onclick="tttNewMatch()">🔄 НОВЫЙ МАТЧ</button></div>

<script>var $=function(id){return document.getElementById(id)};
function toast(m,t,d){t=t||'i';d=d||2200;var e=$('toast');if(!e)return;e.textContent=m;e.className='tst show '+t;clearTimeout(e._t);e._t=setTimeout(function(){e.classList.remove('show')},d)}
function haptic(ms){ms=ms||12;if(navigator.vibrate)navigator.vibrate(ms)}
function bump(e){if(!e)return;e.classList.remove('bump');void e.offsetWidth;e.classList.add('bump')}
function getBest(k){return parseInt(localStorage.getItem(k)||'0',10)}
function getBestF(k){return parseFloat(localStorage.getItem(k)||'0')}
function roundRect(c,x,y,w,h,r){c.beginPath();if(c.roundRect){c.roundRect(x,y,w,h,r);return}c.moveTo(x+r,y);c.arcTo(x+w,y,x+w,y+h,r);c.arcTo(x+w,y+h,x,y+h,r);c.arcTo(x,y+h,x,y,r);c.arcTo(x,y,x+w,y,r);c.closePath()}
var SV=1;
function saveP(k,d){try{localStorage.setItem('save_'+k,JSON.stringify({v:SV,t:Date.now(),data:d}))}catch(e){}}
function loadP(k){try{var r=localStorage.getItem('save_'+k);if(!r)return null;var p=JSON.parse(r);if(!p||p.v!==SV)return null;return p.data}catch(e){return null}}
function clearP(k){try{localStorage.removeItem('save_'+k)}catch(e){}}
var pendingResume=null;
function askResume(k,onC,onN){var d=loadP(k);if(!d){onN();return}pendingResume={k:k,onC:onC,onN:onN};var st='';if(d.score!==undefined)st+='Очки: '+d.score+' · ';if(d.level!==undefined)st+='Уровень: '+d.level+' · ';if(d.wave!==undefined)st+='Волна: '+d.wave;$('resumeStats').textContent=st.replace(/ · $/,'')||'Прогресс сохранён';$('resumeModal').classList.add('show');haptic(15)}
function resumeChoice(c){$('resumeModal').classList.remove('show');if(!pendingResume)return;var p=pendingResume;if(c==='continue'){haptic(20);p.onC()}else{haptic(20);clearP(p.k);p.onN()}pendingResume=null}
function resetGame(k){haptic(20);clearP(k);toast('Прогресс сброшен','sv',1400);var m={snake:startSnake,'2048':start2048,match3:startMatch3,puzzle:startPuzzle,arknoid:startArknoid,memory:memoryShuffle,shooter:startShooter,tetris:startTetris,tower:startTower,rpgSnake:startRpgSnake,gladiator:startGladiator};if(m[k])m[k]()}
function saveCurrentGameState(){try{if(typeof saveSnakeState==='function')saveSnakeState()}catch(e){}try{if(typeof save2048State==='function')save2048State()}catch(e){}try{if(typeof saveMatch3State==='function')saveMatch3State()}catch(e){}try{if(typeof savePuzzleState==='function')savePuzzleState()}catch(e){}try{if(typeof saveArkState==='function')saveArkState()}catch(e){}try{if(typeof saveMemoryState==='function')saveMemoryState()}catch(e){}try{if(typeof saveShooterState==='function')saveShooterState()}catch(e){}try{if(typeof saveTetrisState==='function')saveTetrisState()}catch(e){}try{if(typeof saveTowerState==='function')saveTowerState()}catch(e){}try{if(typeof saveRpgSnakeState==='function')saveRpgSnakeState()}catch(e){}try{if(typeof saveGladiatorState==='function')saveGladiatorState()}catch(e){}}
window.addEventListener('beforeunload',saveCurrentGameState);window.addEventListener('pagehide',saveCurrentGameState);document.addEventListener('visibilitychange',function(){if(document.hidden)saveCurrentGameState()});
function getCoins(){return parseInt(localStorage.getItem('coins')||'0',10)}
function setCoins(v){localStorage.setItem('coins',Math.max(0,v));updateCoinsUI()}
function addCoins(n,st){if(st===undefined)st=true;if(n<=0)return;setCoins(getCoins()+n);if(st)toast('+'+n+' 🪙','c',1200)}
function updateCoinsUI(){var e=$('coinCount');if(!e)return;e.textContent=getCoins();var b=$('coinBadge');if(b){b.classList.remove('bump');void b.offsetWidth;b.classList.add('bump')}}
function switchTab(n){haptic(8);var t=document.querySelectorAll('.tab');for(var i=0;i<t.length;i++)t[i].classList.remove('active');var c=document.querySelectorAll('.tc');for(var j=0;j<c.length;j++)c[j].classList.remove('active');var tt=$('tab-'+n);if(tt)tt.classList.add('active');var cc=$('tab-content-'+n);if(cc)cc.classList.add('active')}
var PREMIUM={shooter:{title:'Космический Шутер',icon:'🚀',price:200,desc:'Волны врагов, боссы, бонусы.',ownedKey:'shooter_owned',screen:'shooter-screen',tagId:'shooterPriceTag'},tetris:{title:'Тетрис',icon:'🧊',price:250,desc:'Легендарная головоломка.',ownedKey:'tetris_owned',screen:'tetris-screen',tagId:'tetrisPriceTag'},tower:{title:'Защитник Базы',icon:'🛡️',price:300,desc:'Tower Defense.',ownedKey:'tower_owned',screen:'tower-screen',tagId:'towerPriceTag'},rpgSnake:{title:'Змейка-РПГ',icon:'🐉',price:250,desc:'Сюжетная змейка с уровнями.',ownedKey:'rpgSnake_owned',screen:'rpgSnake-screen',tagId:'rpgSnakePriceTag'},gladiator:{title:'Арена Гладиаторов',icon:'⚔',price:250,desc:'Бой с волнами врагов.',ownedKey:'gladiator_owned',screen:'gladiator-screen',tagId:'gladiatorPriceTag'}};
function isOwned(k){return localStorage.getItem(PREMIUM[k].ownedKey)==='1'}
function setOwned(k){localStorage.setItem(PREMIUM[k].ownedKey,'1')}
function updatePremiumTags(){for(var k in PREMIUM){var p=PREMIUM[k],t=$(p.tagId);if(!t)continue;if(isOwned(k)){t.textContent='✅ Куплено';t.classList.add('o')}else{t.textContent='🪙 '+p.price;t.classList.remove('o')}}}
var pendingPurchase=null;
function onPremiumClick(k){haptic(12);if(isOwned(k))openGame(PREMIUM[k].screen);else openBuyModal(k)}
function openBuyModal(k){var p=PREMIUM[k];pendingPurchase=k;$('modalIcon').textContent=p.icon;$('modalTitle').textContent=p.title;$('modalDesc').textContent=p.desc;$('modalPrice').textContent=p.price;var c=getCoins()>=p.price,b=$('modalBuyBtn');b.disabled=!c;b.textContent=c?'Купить':'Не хватает 🪙';$('buyModal').classList.add('show')}
function closeBuyModal(){$('buyModal').classList.remove('show');pendingPurchase=null}
function confirmBuy(){if(!pendingPurchase)return;var p=PREMIUM[pendingPurchase];if(getCoins()<p.price){toast('Недостаточно монет','i',1500);return}setCoins(getCoins()-p.price);setOwned(pendingPurchase);haptic(40);var s=p.screen;closeBuyModal();updatePremiumTags();toast('🎉 Игра куплена!','s',2000);setTimeout(function(){openGame(s)},400)}
var AD_DURATION=15,AD_REWARD=40;
var VK_CH='https://vk.com/club239085797',VK_VD='https://vkvideo.ru/video-239085797_456239018';
var AD_SLIDES=[{icon:'📺',title:'Dley перезаливы',text:'Лучшие видео каждый день.',tag:'VK VIDEO',buttons:[{text:'📺 Подписаться',url:VK_CH,cls:'vk'}]},{icon:'🎬',title:'Новые видео',text:'Свежие перезаливы!',tag:'СМОТРЕТЬ',buttons:[{text:'🔥 Смотреть',url:VK_VD,cls:'vd'}]},{icon:'💎',title:'Канал Dley',text:'Тысячи подписчиков!',tag:'ПОДПИСАТЬСЯ',buttons:[{text:'📺 Подписаться',url:VK_CH,cls:'vk'}]}];
var adTimer=null,adSecLeft=0,adSlIdx=0,adSlInt=null;
function buildAdSlides(){var c=$('adSlideContainer');c.innerHTML='';for(var i=0;i<AD_SLIDES.length;i++){var s=AD_SLIDES[i],d=document.createElement('div');d.className='ad-sl'+(i===0?' act':'');var b='';if(s.buttons){b='<div class="ad-sa">';for(var j=0;j<s.buttons.length;j++){var x=s.buttons[j];b+='<a class="ad-sb '+x.cls+'" href="'+x.url+'" target="_blank" rel="noopener">'+x.text+'</a>'}b+='</div>'}d.innerHTML='<div class="ad-si">'+s.icon+'</div><div class="ad-st">'+s.title+'</div><p class="ad-sx">'+s.text+'</p><span class="ad-stg">'+s.tag+'</span>'+b;c.appendChild(d)}}
function buildAdDots(){var c=$('adDots');c.innerHTML='';for(var i=0;i<AD_SLIDES.length;i++){var d=document.createElement('div');d.className='ad-d'+(i===0?' act':'');c.appendChild(d)}}
function showAdSlide(idx){var s=document.querySelectorAll('.ad-sl');for(var i=0;i<s.length;i++){if(i===idx)s[i].classList.add('act');else s[i].classList.remove('act')}var d=document.querySelectorAll('.ad-d');for(var j=0;j<d.length;j++){d[j].classList.remove('act');d[j].classList.remove('dn');if(j===idx)d[j].classList.add('act');else if(j<idx)d[j].classList.add('dn')}}
function openAdModal(){haptic(15);buildAdSlides();buildAdDots();$('adTimerFill').style.width='0%';$('adStatus').innerHTML='Смотрите рекламу <strong>'+AD_DURATION+' секунд</strong>';$('adClaimBtn').disabled=true;$('adClaimBtn').textContent='Получить '+AD_REWARD+' 🪙';$('adModal').classList.add('show');adSecLeft=AD_DURATION;adSlIdx=0;showAdSlide(0);clearInterval(adSlInt);adSlInt=setInterval(function(){adSlIdx=(adSlIdx+1)%AD_SLIDES.length;showAdSlide(adSlIdx);haptic(5)},3000);clearInterval(adTimer);adTimer=setInterval(function(){adSecLeft--;var p=((AD_DURATION-adSecLeft)/AD_DURATION)*100;$('adTimerFill').style.width=p+'%';if(adSecLeft>0)$('adStatus').innerHTML='Осталось: <strong>'+adSecLeft+' сек</strong>';else{clearInterval(adTimer);clearInterval(adSlInt);$('adStatus').innerHTML='✅ Готово!';$('adClaimBtn').disabled=false;haptic(30)}},1000)}
function closeAdModal(){clearInterval(adTimer);clearInterval(adSlInt);$('adModal').classList.remove('show')}
function claimAdReward(){if(adSecLeft>0)return;haptic(40);addCoins(AD_REWARD,false);toast('+'+AD_REWARD+' 🪙','a',2000);closeAdModal()}
function tryUpdateRecord(k,v,ui,bx,f,lb){f=f||'int';lb=lb||false;if(lb&&v<=0)return false;var c=f==='float'?getBestF(k):getBest(k);var r=lb?(c===0||v<c):(v>c);if(r){localStorage.setItem(k,v);if(ui){ui.textContent=f==='float'?v.toFixed(0):v;bump(ui)}if(bx){bx.classList.add('r');setTimeout(function(){bx.classList.remove('r')},1200)}return true}return false}
function updateBestScoresUI(){var k={snake_best:['snake-best','menu-snake-best'],'2048_best':['best2048','menu-2048-best'],match3_best:['match3-best','menu-match3-best'],puzzle_best:['puzzle-best','menu-puzzle-best'],arknoid_best:['arknoid-best','menu-arknoid-best'],memory_best:['memory-best','menu-memory-best'],race_best:['race-best','menu-race-best'],flappy_best:['flappy-best','menu-flappy-best']};for(var key in k){var p=k[key],v=getBest(key),e1=p[0]?$(p[0]):null,e2=p[1]?$(p[1]):null;if(e1)e1.textContent=v;if(e2)e2.textContent=v}var rb=getBest('reaction_best'),rt=rb>0?rb+' мс':'—';if($('reaction-best'))$('reaction-best').textContent=rt;if($('menu-reaction-best'))$('menu-reaction-best').textContent=rt;updateCoinsUI();updatePremiumTags()}
var currentScreen='menu-screen';
function openGame(id){haptic(15);try{if(id==='snake-screen')enterSnake();else if(id==='game2048-screen')enter2048();else if(id==='match3-screen')enterM3();else if(id==='reaction-screen')startReaction();else if(id==='puzzle-screen')enterPuzzle();else if(id==='arknoid-screen')enterArk();else if(id==='memory-screen')enterMemory();else if(id==='race-screen')startRace();else if(id==='flappy-screen')startFlappy();else if(id==='shooter-screen')enterShooter();else if(id==='tetris-screen')enterTetris();else if(id==='tower-screen')enterTower();else if(id==='rpgSnake-screen')enterRpgSnake();else if(id==='gladiator-screen')enterGladiator();else if(id==='duel-screen')startDuel();else if(id==='duel2-screen')startDuel2();else if(id==='ping-screen')startPing();else if(id==='ttt-screen')startTTT()}catch(e){toast('Ошибка: '+e.message,'i',3000)}switchScreen(id)}
function closeGame(id){haptic(10);saveCurrentGameState();try{if(id==='snake-screen')stopSnake();else if(id==='match3-screen')stopM3();else if(id==='reaction-screen')stopReaction();else if(id==='arknoid-screen')stopArk();else if(id==='memory-screen')stopMemory();else if(id==='race-screen')stopRace();else if(id==='flappy-screen')stopFlappy();else if(id==='shooter-screen')stopShooter();else if(id==='tetris-screen')stopTetris();else if(id==='tower-screen')stopTower();else if(id==='rpgSnake-screen')stopRpgSnake();else if(id==='gladiator-screen')stopGladiator();else if(id==='duel-screen')stopDuel();else if(id==='duel2-screen')stopDuel2();else if(id==='ping-screen')stopPing();else if(id==='ttt-screen')stopTTT()}catch(e){}switchScreen('menu-screen')}
function switchScreen(id){var s=document.querySelectorAll('.screen');for(var i=0;i<s.length;i++)s[i].classList.remove('active');var e=$(id);if(e)e.classList.add('active');currentScreen=id;updateBestScoresUI()}

var sCanvas,sCtx,sScoreEl,sBestEl,sBestBox,sGrid=16,sTiles=20,snake,food,sDx,sDy,sScore,snakeInterval,snakeRunning=false;
function initSnakeRefs(){if(sCanvas)return;sCanvas=$('snakeCanvas');sCtx=sCanvas.getContext('2d');sScoreEl=$('snake-score');sBestEl=$('snake-best');sBestBox=$('snake-best-box');sTiles=sCanvas.width/sGrid}
function enterSnake(){initSnakeRefs();var s=loadP('snake');if(s)askResume('snake',function(){resumeSnake(s)},function(){startSnake()});else startSnake()}
function saveSnakeState(){if(!snakeRunning||!snake)return;saveP('snake',{snake:snake.map(function(p){return{x:p.x,y:p.y}}),food:{x:food.x,y:food.y},dx:sDx,dy:sDy,score:sScore})}
function resumeSnake(s){initSnakeRefs();snake=s.snake.map(function(p){return{x:p.x,y:p.y}});food={x:s.food.x,y:s.food.y};sDx=s.dx;sDy=s.dy;sScore=s.score;sScoreEl.textContent=sScore;sBestEl.textContent=getBest('snake_best');clearInterval(snakeInterval);snakeRunning=true;snakeInterval=setInterval(updateSnake,130);drawSnake();toast('💾 Продолжаем','sv',1500)}
function startSnake(){initSnakeRefs();snake=[{x:8,y:8}];food={x:4,y:4};sDx=1;sDy=0;sScore=0;sScoreEl.textContent='0';sBestEl.textContent=getBest('snake_best');clearInterval(snakeInterval);snakeRunning=true;spawnFood();snakeInterval=setInterval(updateSnake,130);drawSnake()}
function stopSnake(){saveSnakeState();clearInterval(snakeInterval);snakeRunning=false}
function updateSnake(){if(!snakeRunning)return;var h={x:snake[0].x+sDx,y:snake[0].y+sDy};var hw=h.x<0||h.x>=sTiles||h.y<0||h.y>=sTiles;var hs=false;for(var i=1;i<snake.length;i++){if(snake[i].x===h.x&&snake[i].y===h.y){hs=true;break}}if(hw||hs){gameOverSnake();return}snake.unshift(h);if(h.x===food.x&&h.y===food.y){sScore+=10;sScoreEl.textContent=sScore;bump(sScoreEl);haptic(20);addCoins(1,false);if(tryUpdateRecord('snake_best',sScore,sBestEl,sBestBox))toast('🏆 Рекорд: '+sScore,'r',1400);spawnFood()}else snake.pop();drawSnake();if(snake.length%3===0)saveSnakeState()}
function drawSnake(){if(!sCtx)return;sCtx.fillStyle='#060a06';sCtx.fillRect(0,0,sCanvas.width,sCanvas.height);sCtx.strokeStyle='rgba(76,175,80,0.05)';for(var i=1;i<sTiles;i++){sCtx.beginPath();sCtx.moveTo(i*sGrid,0);sCtx.lineTo(i*sGrid,sCanvas.height);sCtx.stroke();sCtx.beginPath();sCtx.moveTo(0,i*sGrid);sCtx.lineTo(sCanvas.width,i*sGrid);sCtx.stroke()}var t=performance.now()/300,p=1+Math.sin(t)*0.12,fx=food.x*sGrid+sGrid/2,fy=food.y*sGrid+sGrid/2,fr=(sGrid/2-2)*p,g=sCtx.createRadialGradient(fx,fy,0,fx,fy,fr*1.6);g.addColorStop(0,'#ff8a65');g.addColorStop(1,'rgba(255,87,34,0)');sCtx.fillStyle=g;sCtx.beginPath();sCtx.arc(fx,fy,fr*1.6,0,Math.PI*2);sCtx.fill();sCtx.fillStyle='#ff5722';sCtx.beginPath();sCtx.arc(fx,fy,fr,0,Math.PI*2);sCtx.fill();for(var j=0;j<snake.length;j++){var pt=snake[j],x=pt.x*sGrid,y=pt.y*sGrid,hd=j===0,pd=hd?1:2;sCtx.fillStyle=hd?'#a5d6a7':'hsl(122,39%,'+(45-Math.min(j*1.5,20))+'%)';roundRect(sCtx,x+pd,y+pd,sGrid-pd*2,sGrid-pd*2,4);sCtx.fill()}}
function spawnFood(){do{food.x=Math.floor(Math.random()*sTiles);food.y=Math.floor(Math.random()*sTiles)}while(snake.some(function(p){return p.x===food.x&&p.y===food.y}))}
function gameOverSnake(){clearInterval(snakeInterval);snakeRunning=false;clearP('snake');haptic(80);toast('Игра окончена. Очки: '+sScore,'i',1600);setTimeout(function(){if(currentScreen==='snake-screen')startSnake()},900)}
function setSnakeDir(nx,ny){if(!snakeRunning)return;if(nx===-sDx&&sDx!==0)return;if(ny===-sDy&&sDy!==0)return;sDx=nx;sDy=ny;haptic(8)}

var c2048,ctx2048,sc2048El,best2048El,best2048Box,size2048=4,cellW;
var board2048=[],score2048=0,board2048Anim={},lastCM=0;
var tileColors={2:'#eee4da',4:'#ede0c8',8:'#f2b179',16:'#f59563',32:'#f67c5f',64:'#f65e3b',128:'#edcf72',256:'#edcc61',512:'#edc850',1024:'#edc53f',2048:'#edc22e'};
function init2048Refs(){if(c2048)return;c2048=$('c2048');ctx2048=c2048.getContext('2d');sc2048El=$('score2048');best2048El=$('best2048');best2048Box=$('best2048-box');cellW=c2048.width/size2048}
function enter2048(){init2048Refs();var s=loadP('2048');if(s)askResume('2048',function(){resume2048(s)},function(){start2048()});else start2048()}
function save2048State(){if(!board2048||!board2048.length)return;saveP('2048',{board:board2048.map(function(r){return r.slice()}),score:score2048})}
function resume2048(s){init2048Refs();board2048=s.board.map(function(r){return r.slice()});score2048=s.score;sc2048El.textContent=score2048;best2048El.textContent=getBest('2048_best');drawBoard2048();toast('💾 Продолжаем','sv',1500)}
function start2048(){init2048Refs();board2048=[];for(var r=0;r<size2048;r++){board2048.push([]);for(var c=0;c<size2048;c++)board2048[r].push(0)}score2048=0;lastCM=0;sc2048El.textContent='0';best2048El.textContent=getBest('2048_best');addTile2048();addTile2048();drawBoard2048()}
function addTile2048(){var e=[];for(var r=0;r<size2048;r++)for(var c=0;c<size2048;c++)if(board2048[r][c]===0)e.push({r:r,c:c});if(!e.length)return;var cl=e[Math.floor(Math.random()*e.length)];board2048[cl.r][cl.c]=Math.random()<0.9?2:4;board2048Anim[cl.r+','+cl.c]=performance.now()}
function drawBoard2048(){if(!ctx2048)return;ctx2048.fillStyle='#1a1610';ctx2048.fillRect(0,0,c2048.width,c2048.height);for(var r=0;r<size2048;r++)for(var c=0;c<size2048;c++){var v=board2048[r][c],x=c*cellW+5,y=r*cellW+5,w=cellW-10;ctx2048.fillStyle='rgba(255,255,255,0.04)';roundRect(ctx2048,x,y,w,w,8);ctx2048.fill();if(v>0){var k=r+','+c,born=board2048Anim[k]||0,age=(performance.now()-born)/150,sc=age<1?0.5+age*0.5:1;ctx2048.save();ctx2048.translate(x+w/2,y+w/2);ctx2048.scale(sc,sc);ctx2048.translate(-(x+w/2),-(y+w/2));ctx2048.fillStyle=tileColors[v]||'#3c3a32';roundRect(ctx2048,x,y,w,w,8);ctx2048.fill();ctx2048.fillStyle=(v===2||v===4)?'#776e65':'#f9f6f2';var fs=v>1000?18:v>100?22:28;ctx2048.font='bold '+fs+'px system-ui,sans-serif';ctx2048.textAlign='center';ctx2048.textBaseline='middle';ctx2048.fillText(v,x+w/2,y+w/2+1);ctx2048.restore()}}}
function move2048(dir){if(currentScreen!=='game2048-screen')return;haptic(8);var mv=false;if(dir==='right'){reverseBoard();mv=slideLeft();reverseBoard()}else if(dir==='left'){mv=slideLeft()}else if(dir==='up'){transposeBoard();mv=slideLeft();transposeBoard()}else if(dir==='down'){transposeBoard();reverseBoard();mv=slideLeft();reverseBoard();transposeBoard()}if(mv){addTile2048();sc2048El.textContent=score2048;bump(sc2048El);var ms=Math.floor(score2048/50);if(ms>lastCM){addCoins(ms-lastCM,false);lastCM=ms}if(tryUpdateRecord('2048_best',score2048,best2048El,best2048Box))toast('🏆 Рекорд: '+score2048,'r',1400);drawBoard2048();save2048State();if(isGameOver2048()){clearP('2048');haptic(80);toast('Игра окончена. Счет: '+score2048,'i',1800);setTimeout(function(){if(currentScreen==='game2048-screen')start2048()},1100)}}}
function slideLeft(){var mv=false;for(var r=0;r<size2048;r++){var row=board2048[r].filter(function(v){return v!==0});for(var i=0;i<row.length-1;i++)if(row[i]===row[i+1]){row[i]*=2;score2048+=row[i];row.splice(i+1,1);mv=true}while(row.length<size2048)row.push(0);if(JSON.stringify(board2048[r])!==JSON.stringify(row))mv=true;board2048[r]=row}return mv}
function reverseBoard(){for(var i=0;i<board2048.length;i++)board2048[i].reverse()}
function transposeBoard(){var nb=[];for(var i=0;i<size2048;i++){nb.push([]);for(var j=0;j<size2048;j++)nb[i].push(board2048[j][i])}board2048=nb}
function isGameOver2048(){for(var r=0;r<size2048;r++)for(var c=0;c<size2048;c++){if(board2048[r][c]===0)return false;if(c<size2048-1&&board2048[r][c]===board2048[r][c+1])return false;if(r<size2048-1&&board2048[r][c]===board2048[r+1][c])return false}return true}

var mCanvas,mCtx,mScoreEl,mBestEl,mBestBox,mSize=6,mCell;
var gemColors=['#e91e63','#2196f3','#4caf50','#ffeb3b','#9c27b0','#ff9800'];
var mBoard=[],mScore=0,selR=0,selC=0,mInterval,mRunning=false,mParticles=[],mFirstTap=null,mCM3=0,blinkPhase=0;
function initM3(){if(mCanvas)return;mCanvas=$('match3Canvas');mCtx=mCanvas.getContext('2d');mScoreEl=$('match3-score');mBestEl=$('match3-best');mBestBox=$('match3-best-box');mCell=mCanvas.width/mSize}
function enterM3(){initM3();var s=loadP('match3');if(s)askResume('match3',function(){resumeM3(s)},function(){startMatch3()});else startMatch3()}
function saveMatch3State(){if(!mRunning||!mBoard||!mBoard.length)return;saveP('match3',{board:mBoard.map(function(r){return r.slice()}),score:mScore})}
function resumeM3(s){initM3();mBoard=s.board.map(function(r){return r.slice()});mScore=s.score;mScoreEl.textContent=mScore;mBestEl.textContent=getBest('match3_best');selR=0;selC=0;mFirstTap=null;mCM3=Math.floor(mScore/30);mParticles=[];clearInterval(mInterval);mRunning=true;mInterval=setInterval(drawMatch3,60);drawMatch3();toast('💾 Продолжаем','sv',1500)}
function startMatch3(){initM3();mScore=0;mScoreEl.textContent='0';mBestEl.textContent=getBest('match3_best');selR=0;selC=0;mFirstTap=null;mCM3=0;mParticles=[];initM3Board();clearInterval(mInterval);mRunning=true;mInterval=setInterval(drawMatch3,60);drawMatch3()}
function stopM3(){saveMatch3State();clearInterval(mInterval);mRunning=false}
function initM3Board(){var g;for(var r=0;r<mSize;r++){mBoard[r]=[];for(var c=0;c<mSize;c++){var idx;g=0;do{idx=Math.floor(Math.random()*gemColors.length);g++}while(g<50&&((c>=2&&mBoard[r][c-1]===idx&&mBoard[r][c-2]===idx)||(r>=2&&mBoard[r-1][c]===idx&&mBoard[r-2][c]===idx)));mBoard[r][c]=idx}}if(checkM3())initM3Board()}
function drawMatch3(){if(!mRunning||!mCtx)return;blinkPhase+=0.08;mCtx.fillStyle='#100812';mCtx.fillRect(0,0,mCanvas.width,mCanvas.height);mCtx.strokeStyle='rgba(156,39,176,0.08)';for(var i=1;i<mSize;i++){mCtx.beginPath();mCtx.moveTo(i*mCell,0);mCtx.lineTo(i*mCell,mCanvas.height);mCtx.stroke();mCtx.beginPath();mCtx.moveTo(0,i*mCell);mCtx.lineTo(mCanvas.width,i*mCell);mCtx.stroke()}for(var r=0;r<mSize;r++)for(var c=0;c<mSize;c++){var col=gemColors[mBoard[r][c]],cx=c*mCell+mCell/2,cy=r*mCell+mCell/2,rad=mCell/2-7,glow=mCtx.createRadialGradient(cx,cy,0,cx,cy,rad*1.8);glow.addColorStop(0,col+'55');glow.addColorStop(1,'rgba(0,0,0,0)');mCtx.fillStyle=glow;mCtx.beginPath();mCtx.arc(cx,cy,rad*1.8,0,Math.PI*2);mCtx.fill();mCtx.fillStyle=col;mCtx.beginPath();mCtx.arc(cx,cy,rad,0,Math.PI*2);mCtx.fill();mCtx.fillStyle='rgba(255,255,255,0.35)';mCtx.beginPath();mCtx.arc(cx-rad*0.3,cy-rad*0.3,rad*0.35,0,Math.PI*2);mCtx.fill();if(r===selR&&c===selC){var a=0.6+Math.sin(blinkPhase*6)*0.4;mCtx.strokeStyle='rgba(255,255,255,'+a+')';mCtx.lineWidth=3;mCtx.beginPath();mCtx.arc(cx,cy,rad+3,0,Math.PI*2);mCtx.stroke()}}for(var k=mParticles.length-1;k>=0;k--){var p=mParticles[k];p.x+=p.vx;p.y+=p.vy;p.vy+=0.15;p.life-=0.02;if(p.life<=0){mParticles.splice(k,1);continue}mCtx.globalAlpha=p.life;mCtx.fillStyle=p.color;mCtx.beginPath();mCtx.arc(p.x,p.y,p.size,0,Math.PI*2);mCtx.fill()}mCtx.globalAlpha=1}
function trySwapM3(r1,c1,r2,c2){if(Math.abs(r1-r2)+Math.abs(c1-c2)!==1)return false;var t=mBoard[r1][c1];mBoard[r1][c1]=mBoard[r2][c2];mBoard[r2][c2]=t;if(!checkM3()){t=mBoard[r1][c1];mBoard[r1][c1]=mBoard[r2][c2];mBoard[r2][c2]=t;return false}return true}
function moveMatch3(dir){if(!mRunning||currentScreen!=='match3-screen')return;haptic(10);var nr=selR,nc=selC;if(dir==='up')nr--;else if(dir==='down')nr++;else if(dir==='left')nc--;else if(dir==='right')nc++;if(nr<0||nr>=mSize||nc<0||nc>=mSize)return;if(!trySwapM3(selR,selC,nr,nc)){toast('Нет линии из 3','i',900);return}selR=nr;selC=nc;processMatches()}
function match3Tap(r,c){if(!mRunning)return;if(r<0||r>=mSize||c<0||c>=mSize)return;if(mFirstTap===null){selR=r;selC=c;mFirstTap={r:r,c:c};haptic(8);return}if(mFirstTap.r===r&&mFirstTap.c===c){mFirstTap=null;haptic(8);return}if(trySwapM3(mFirstTap.r,mFirstTap.c,r,c)){selR=r;selC=c;mFirstTap=null;haptic(15);processMatches()}else{selR=r;selC=c;mFirstTap={r:r,c:c};haptic(8)}}
function checkM3(){for(var r=0;r<mSize;r++)for(var c=0;c<mSize;c++){if(c<mSize-2&&mBoard[r][c]===mBoard[r][c+1]&&mBoard[r][c]===mBoard[r][c+2])return true;if(r<mSize-2&&mBoard[r][c]===mBoard[r+1][c]&&mBoard[r][c]===mBoard[r+2][c])return true}return false}
function processMatches(){var tr=[];for(var i=0;i<mSize;i++){tr.push([]);for(var j=0;j<mSize;j++)tr[i].push(false)}for(var r=0;r<mSize;r++)for(var c=0;c<mSize;c++){if(c<mSize-2&&mBoard[r][c]===mBoard[r][c+1]&&mBoard[r][c]===mBoard[r][c+2])tr[r][c]=tr[r][c+1]=tr[r][c+2]=true;if(r<mSize-2&&mBoard[r][c]===mBoard[r+1][c]&&mBoard[r][c]===mBoard[r+2][c])tr[r][c]=tr[r+1][c]=tr[r+2][c]=true}var rem=0;for(var r2=0;r2<mSize;r2++)for(var c2=0;c2<mSize;c2++)if(tr[r2][c2])rem++;if(rem===0)return;for(var r3=0;r3<mSize;r3++)for(var c3=0;c3<mSize;c3++)if(tr[r3][c3]){var col=gemColors[mBoard[r3][c3]],cx=c3*mCell+mCell/2,cy=r3*mCell+mCell/2;for(var k=0;k<4;k++)mParticles.push({x:cx,y:cy,vx:(Math.random()-0.5)*4,vy:(Math.random()-0.5)*4-1,life:1,size:2+Math.random()*2,color:col})}for(var c4=0;c4<mSize;c4++){var wr=mSize-1;for(var r4=mSize-1;r4>=0;r4--)if(!tr[r4][c4]){mBoard[wr][c4]=mBoard[r4][c4];wr--}for(var r5=wr;r5>=0;r5--)mBoard[r5][c4]=Math.floor(Math.random()*gemColors.length)}mScore+=rem*10;mScoreEl.textContent=mScore;bump(mScoreEl);haptic(20);var ms=Math.floor(mScore/30);if(ms>mCM3){addCoins(ms-mCM3,false);mCM3=ms}if(tryUpdateRecord('match3_best',mScore,mBestEl,mBestBox))toast('🏆 Рекорд: '+mScore,'r',1400);saveMatch3State();setTimeout(function(){if(mRunning)processMatches()},280)}
function match3Click(e){if(!mRunning)return;var rect=mCanvas.getBoundingClientRect();var x=(e.clientX-rect.left)*(mCanvas.width/rect.width),y=(e.clientY-rect.top)*(mCanvas.height/rect.height);match3Tap(Math.floor(y/mCell),Math.floor(x/mCell))}

var rCanvas,rCtx,rTimeEl,rBestEl,rBestBox,rBtn,rState='idle',rStartTime=0,rTimeout=null;
function initReactionRefs(){if(rCanvas)return;rCanvas=$('reactionCanvas');rCtx=rCanvas.getContext('2d');rTimeEl=$('reaction-time');rBestEl=$('reaction-best');rBestBox=$('reaction-best-box');rBtn=$('reactionBtn')}
function startReaction(){initReactionRefs();rState='idle';rTimeEl.textContent='—';rBestEl.textContent=getBest('reaction_best')>0?getBest('reaction_best')+' мс':'—';rBtn.textContent='СТАРТ';drawReactionIdle();clearTimeout(rTimeout)}
function stopReaction(){clearTimeout(rTimeout);rState='idle'}
function drawReactionIdle(){if(!rCtx)return;rCtx.fillStyle='#041014';rCtx.fillRect(0,0,rCanvas.width,rCanvas.height);rCtx.fillStyle='rgba(0,188,212,0.4)';rCtx.font='bold 22px system-ui';rCtx.textAlign='center';rCtx.textBaseline='middle';rCtx.fillText('НАЖМИТЕ СТАРТ',rCanvas.width/2,rCanvas.height/2)}
function drawReactionState(col,txt){if(!rCtx)return;rCtx.fillStyle=col;rCtx.fillRect(0,0,rCanvas.width,rCanvas.height);rCtx.fillStyle='#fff';rCtx.font='bold 32px system-ui';rCtx.textAlign='center';rCtx.textBaseline='middle';rCtx.fillText(txt,rCanvas.width/2,rCanvas.height/2)}
function reactionTap(e){if(e)e.preventDefault();haptic(15);if(rState==='idle'){rState='waiting';rBtn.textContent='ЖДИТЕ...';drawReactionState('#b71c1c','ЖДИТЕ...');rTimeout=setTimeout(function(){if(rState!=='waiting')return;rState='ready';rStartTime=performance.now();drawReactionState('#1b5e20','ЖМИ!');rBtn.textContent='ЖМИ!';haptic(40)},1500+Math.random()*2500)}else if(rState==='waiting'){clearTimeout(rTimeout);rState='idle';drawReactionState('#4a148c','РАНО!');toast('Слишком рано!','i',1200);rBtn.textContent='ПОПРОБОВАТЬ СНОВА';haptic(60)}else if(rState==='ready'){var t=Math.round(performance.now()-rStartTime);rState='done';rTimeEl.textContent=t+' мс';bump(rTimeEl);drawReactionState('#0d47a1',t+' мс');rBtn.textContent='ЕЩЁ РАЗ';haptic(30);var cn=t<250?5:t<400?3:t<600?1:0;if(cn>0)addCoins(cn,false);if(tryUpdateRecord('reaction_best',t,rBestEl,rBestBox,'int',true))toast('🏆 Рекорд: '+t+' мс!','r',1600);else if(cn>0)toast('+'+cn+' 🪙','c',1000)}else if(rState==='done')startReaction()}

var pCanvas,pCtx,pMovesEl,pBestEl,pBestBox,pSize=3,pTotal=9,pCell,pBoard=[],pMoves=0,pSolved=false;
function initPuzzleRefs(){if(pCanvas)return;pCanvas=$('puzzleCanvas');pCtx=pCanvas.getContext('2d');pMovesEl=$('puzzle-moves');pBestEl=$('puzzle-best');pBestBox=$('puzzle-best-box');pCell=pCanvas.width/pSize}
function enterPuzzle(){initPuzzleRefs();var s=loadP('puzzle');if(s)askResume('puzzle',function(){resumePuzzle(s)},function(){startPuzzle()});else startPuzzle()}
function savePuzzleState(){if(!pBoard||!pBoard.length||pSolved)return;saveP('puzzle',{board:pBoard.slice(),moves:pMoves})}
function resumePuzzle(s){initPuzzleRefs();pBoard=s.board.slice();pMoves=s.moves;pMovesEl.textContent=pMoves;pBestEl.textContent=getBest('puzzle_best');pSolved=false;drawPuzzle();toast('💾 Продолжаем','sv',1500)}
function startPuzzle(){initPuzzleRefs();pMoves=0;pMovesEl.textContent='0';pBestEl.textContent=getBest('puzzle_best')||0;pSolved=false;shufflePuzzle();drawPuzzle()}
function shufflePuzzle(){haptic(15);pBoard=[];for(var i=0;i<pTotal;i++)pBoard.push(i);var ei=pTotal-1,steps=80+Math.floor(Math.random()*40);for(var s=0;s<steps;s++){var nb=getNeighbors(ei),pk=nb[Math.floor(Math.random()*nb.length)],tmp=pBoard[ei];pBoard[ei]=pBoard[pk];pBoard[pk]=tmp;ei=pk}pMoves=0;pMovesEl.textContent='0';pSolved=false;drawPuzzle()}
function getNeighbors(idx){var r=Math.floor(idx/pSize),c=idx%pSize,o=[];if(r>0)o.push(idx-pSize);if(r<pSize-1)o.push(idx+pSize);if(c>0)o.push(idx-1);if(c<pSize-1)o.push(idx+1);return o}
function drawPuzzle(){if(!pCtx)return;pCtx.fillStyle='#140606';pCtx.fillRect(0,0,pCanvas.width,pCanvas.height);var pad=5,w=pCell-pad*2;for(var i=0;i<pTotal;i++){var v=pBoard[i],r=Math.floor(i/pSize),c=i%pSize,x=c*pCell+pad,y=r*pCell+pad;if(v===0){pCtx.fillStyle='rgba(255,255,255,0.03)';roundRect(pCtx,x,y,w,w,10);pCtx.fill();continue}var cor=v===i+1,g=pCtx.createLinearGradient(x,y,x+w,y+w);if(cor){g.addColorStop(0,'#66bb6a');g.addColorStop(1,'#2e7d32')}else{g.addColorStop(0,'#ef5350');g.addColorStop(1,'#b71c1c')}pCtx.fillStyle=g;roundRect(pCtx,x,y,w,w,10);pCtx.fill();pCtx.fillStyle='rgba(255,255,255,0.15)';roundRect(pCtx,x+4,y+4,w-8,w*0.35,6);pCtx.fill();pCtx.fillStyle='#fff';pCtx.font='bold 32px system-ui';pCtx.textAlign='center';pCtx.textBaseline='middle';pCtx.fillText(v,x+w/2,y+w/2+2)}}
function puzzleClick(e){if(pSolved)return;var rect=pCanvas.getBoundingClientRect();var x=(e.clientX-rect.left)*(pCanvas.width/rect.width),y=(e.clientY-rect.top)*(pCanvas.height/rect.height);var c=Math.floor(x/pCell),r=Math.floor(y/pCell);if(r<0||r>=pSize||c<0||c>=pSize)return;var idx=r*pSize+c,ei=pBoard.indexOf(0);if(getNeighbors(ei).indexOf(idx)===-1)return;var tmp=pBoard[ei];pBoard[ei]=pBoard[idx];pBoard[idx]=tmp;pMoves++;pMovesEl.textContent=pMoves;bump(pMovesEl);haptic(10);drawPuzzle();savePuzzleState();if(isPuzzleSolved()){pSolved=true;haptic(60);clearP('puzzle');var cn=pMoves<=30?20:pMoves<=60?10:5;addCoins(cn,false);if(tryUpdateRecord('puzzle_best',pMoves,pBestEl,pBestBox,'int',true))toast('🏆 Рекорд: '+pMoves+' ходов! +'+cn+'🪙','r',2000);else toast('Собрано за '+pMoves+' ходов! +'+cn+'🪙','s',1800)}}
function isPuzzleSolved(){for(var i=0;i<pTotal-1;i++)if(pBoard[i]!==i+1)return false;return pBoard[pTotal-1]===0}

var arkCanvas,arkCtx,arkScoreEl,arkLevelEl,arkBestEl,arkBestBox,ARK_W=320,ARK_H=380,ARK_PH=12,ARK_PY,ARK_BR=6,ARK_BH=18,ARK_BG=4,ARK_BT=50,ARK_BS=8,ARK_MAX=10;
var arkPUColors={expand:'#66bb6a',sticky:'#ffffff',multi:'#42a5f5',laser:'#ef5350'};
var arkPUIcons={expand:'⬌',sticky:'⊛',multi:'●●●',laser:'⌇'};
var arkRunning=false,arkFId=null,arkLT=0,arkPX=160,arkPW=70,arkDir=0,arkBalls=[],arkBricks=[],arkScore=0,arkLevel=1,arkLives=3,arkPaused=false,arkCM=0,arkParticles=[],arkPUs=[],arkAE={},arkSticky=false,arkLaserT=0,arkBrickCols=['#e53935','#fb8c00','#fdd835','#43a047','#1e88e5','#8e24aa'];
function initArk(){if(arkCanvas)return;arkCanvas=$('arknoidCanvas');arkCtx=arkCanvas.getContext('2d');arkScoreEl=$('arknoid-score');arkLevelEl=$('arknoid-level');arkBestEl=$('arknoid-best');arkBestBox=$('arknoid-best-box');ARK_W=arkCanvas.width;ARK_H=arkCanvas.height;ARK_PY=ARK_H-30;arkPX=ARK_W/2}
function enterArk(){initArk();var s=loadP('arknoid');if(s)askResume('arknoid',function(){resumeArk(s)},function(){startArknoid()});else startArknoid()}
function saveArkState(){if(!arkRunning||!arkBricks)return;saveP('arknoid',{px:arkPX,pw:arkPW,balls:arkBalls.map(function(b){return{x:b.x,y:b.y,vx:b.vx,vy:b.vy,launched:b.launched}}),bricks:arkBricks.map(function(b){return{x:b.x,y:b.y,w:b.w,h:b.h,hp:b.hp,maxHp:b.maxHp,color:b.color,points:b.points}}),score:arkScore,level:arkLevel,lives:arkLives})}
function resumeArk(s){initArk();arkPX=s.px;arkPW=s.pw;arkDir=0;arkBalls=s.balls.map(function(b){return{x:b.x,y:b.y,vx:b.vx,vy:b.vy,launched:b.launched}});arkBricks=s.bricks.map(function(b){return{x:b.x,y:b.y,w:b.w,h:b.h,hp:b.hp,maxHp:b.maxHp,color:b.color,points:b.points}});arkScore=s.score;arkLevel=s.level;arkLives=s.lives;arkPaused=false;arkCM=Math.floor(arkScore/30);arkParticles=[];arkPUs=[];arkAE={};arkSticky=false;arkLaserT=0;arkScoreEl.textContent=arkScore;arkLevelEl.textContent=arkLevel;arkBestEl.textContent=getBest('arknoid_best');arkRunning=true;arkLT=performance.now();if(arkFId)cancelAnimationFrame(arkFId);arkFId=requestAnimationFrame(arkLoop);toast('💾 Уровень '+arkLevel,'sv',1500)}
function startArknoid(){initArk();arkPX=ARK_W/2;arkPW=70;arkDir=0;arkScore=0;arkLevel=1;arkLives=3;arkPaused=false;arkCM=0;arkParticles=[];arkPUs=[];arkAE={};arkSticky=false;arkLaserT=0;arkScoreEl.textContent='0';arkLevelEl.textContent='1';arkBestEl.textContent=getBest('arknoid_best');buildArkLevel(1);resetArBall();arkRunning=true;arkLT=performance.now();if(arkFId)cancelAnimationFrame(arkFId);arkFId=requestAnimationFrame(arkLoop)}
function stopArk(){saveArkState();arkRunning=false;if(arkFId)cancelAnimationFrame(arkFId);arkFId=null}
function resetArBall(){arkBalls=[{x:arkPX,y:ARK_PY-ARK_BR-2,vx:0,vy:0,launched:false}]}
function launchArBall(){var b=arkBalls[0];if(!b||b.launched)return;var a=(-60+Math.random()*120)*Math.PI/180,sp=4.2+arkLevel*0.15;b.vx=Math.sin(a)*sp;b.vy=-Math.abs(Math.cos(a)*sp);if(Math.abs(b.vx)<1.5)b.vx=b.vx>0?1.5:-1.5;b.launched=true;haptic(15)}
function buildArkLevel(lvl){arkBricks=[];var tw=ARK_W-ARK_BS*2,bw=(tw-ARK_BG*7)/8;for(var r=0;r<5;r++)for(var c=0;c<8;c++){var hp=Math.min(3,1+Math.floor((4-r)/2)+(lvl>3?1:0));arkBricks.push({x:ARK_BS+c*(bw+ARK_BG),y:ARK_BT+r*(ARK_BH+ARK_BG),w:bw,h:ARK_BH,hp:hp,maxHp:hp,color:arkBrickCols[r%6],points:(5-r)*5*hp})}}
function arknoidControl(a){if(!arkRunning)return;if(a==='left'){arkDir=-1;haptic(6)}else if(a==='right'){arkDir=1;haptic(6)}else if(a==='fire'){launchArBall();haptic(10)}else if(a==='pause'){arkPaused=!arkPaused;haptic(10)}}
function arkLoop(t){if(!arkRunning)return;var dt=Math.min(40,t-arkLT);arkLT=t;if(!arkPaused)updateArk(dt,t);drawArk();arkFId=requestAnimationFrame(arkLoop)}
function arkScoreAdd(p){arkScore+=p;arkScoreEl.textContent=arkScore;bump(arkScoreEl);var ms=Math.floor(arkScore/30);if(ms>arkCM){addCoins(ms-arkCM,false);arkCM=ms}if(tryUpdateRecord('arknoid_best',arkScore,arkBestEl,arkBestBox))toast('🏆 Рекорд: '+arkScore,'r',1400)}
function arkSpawnPU(x,y){if(Math.random()<0.18){var t=['expand','sticky','multi','laser'][Math.floor(Math.random()*4)];arkPUs.push({x:x,y:y,type:t,vy:2.2})}}
function applyArPU(t){haptic(20);if(t==='expand'){arkPW=Math.min(130,arkPW+30);arkAE.expand=performance.now()+10000;toast('🟢 Расширение!','s',1200)}else if(t==='sticky'){arkSticky=true;arkAE.sticky=performance.now()+10000;toast('⚪ Липкая!','s',1200)}else if(t==='multi'){var b=arkBalls[0];if(b&&b.launched){for(var i=0;i<2;i++){var a=(Math.random()-0.5)*Math.PI/2,sp=Math.hypot(b.vx,b.vy)||5;arkBalls.push({x:b.x,y:b.y,vx:Math.sin(a)*sp,vy:-Math.abs(Math.cos(a)*sp),launched:true})}toast('🔵 Мультимяч!','s',1200)}else toast('🔵 Активируется при запуске','i',1200)}else if(t==='laser'){arkLaserT=performance.now()+8000;toast('🔴 Лазер!','s',1200)}}
function updateArk(dt,t){arkPX+=arkDir*0.45*dt;arkPX=Math.max(arkPW/2,Math.min(ARK_W-arkPW/2,arkPX));if(arkAE.expand&&t>arkAE.expand){arkPW=70;delete arkAE.expand}if(arkAE.sticky&&t>arkAE.sticky){arkSticky=false;delete arkAE.sticky}if(arkLaserT&&t>arkLaserT)arkLaserT=0;for(var bi=arkBalls.length-1;bi>=0;bi--){var b=arkBalls[bi];if(!b.launched){b.x=arkPX;b.y=ARK_PY-ARK_BR-2}else{b.x+=b.vx*dt*0.06;b.y+=b.vy*dt*0.06;if(b.x<ARK_BR){b.x=ARK_BR;b.vx=Math.abs(b.vx)}if(b.x>ARK_W-ARK_BR){b.x=ARK_W-ARK_BR;b.vx=-Math.abs(b.vx)}if(b.y<ARK_BR){b.y=ARK_BR;b.vy=Math.abs(b.vy)}if(b.y+ARK_BR>ARK_PY&&b.y-ARK_BR<ARK_PY+ARK_PH&&b.x>arkPX-arkPW/2-ARK_BR&&b.x<arkPX+arkPW/2+ARK_BR&&b.vy>0){b.y=ARK_PY-ARK_BR;var rel=(b.x-arkPX)/(arkPW/2),ang=rel*Math.PI/3,sp=Math.min(7.5,Math.hypot(b.vx,b.vy)+0.02);b.vx=Math.sin(ang)*sp;b.vy=-Math.abs(Math.cos(ang)*sp);if(arkSticky){b.launched=false;b.vx=0;b.vy=0;b.y=ARK_PY-ARK_BR-2;haptic(12);continue}haptic(6)}for(var i=arkBricks.length-1;i>=0;i--){var br=arkBricks[i];if(b.x+ARK_BR>br.x&&b.x-ARK_BR<br.x+br.w&&b.y+ARK_BR>br.y&&b.y-ARK_BR<br.y+br.h){var oL=b.x+ARK_BR-br.x,oR=br.x+br.w-(b.x-ARK_BR),oT=b.y+ARK_BR-br.y,oB=br.y+br.h-(b.y-ARK_BR),mo=Math.min(oL,oR,oT,oB);if(mo===oL||mo===oR)b.vx=-b.vx;else b.vy=-b.vy;br.hp--;for(var k=0;k<4;k++)arkParticles.push({x:br.x+br.w/2,y:br.y+br.h/2,vx:(Math.random()-0.5)*3,vy:(Math.random()-0.5)*3,life:1,size:2,color:br.color});haptic(8);if(br.hp<=0){arkScoreAdd(br.points);arkSpawnPU(br.x+br.w/2,br.y+br.h/2);arkBricks.splice(i,1)}break}}if(b.y>ARK_H+20){arkBalls.splice(bi,1);if(arkBalls.length===0){arkLives--;haptic(80);if(arkLives<=0){gameOverArk();return}toast('💔 Мяч потерян!','i',1000);resetArBall()}}}}for(var pi=arkPUs.length-1;pi>=0;pi--){var p=arkPUs[pi];p.y+=p.vy*dt*0.06;if(p.y>ARK_H+20){arkPUs.splice(pi,1);continue}if(Math.abs(p.x-arkPX)<arkPW/2+10&&Math.abs(p.y-ARK_PY)<20){applyArPU(p.type);arkPUs.splice(pi,1)}}for(var ai=arkParticles.length-1;ai>=0;ai--){var pp=arkParticles[ai];pp.x+=pp.vx;pp.y+=pp.vy;pp.life-=0.03;if(pp.life<=0)arkParticles.splice(ai,1)}if(arkBricks.length===0){arkScore+=100;arkScoreEl.textContent=arkScore;addCoins(15,false);if(tryUpdateRecord('arknoid_best',arkScore,arkBestEl,arkBestBox))toast('🏆 Рекорд: '+arkScore,'r',1600);if(arkLevel>=ARK_MAX){clearP('arknoid');toast('🎉 Все уровни пройдены!','s',2500);setTimeout(function(){if(arkRunning){arkLevel=1;arkLevelEl.textContent='1';buildArkLevel(1);resetArBall()}},1500)}else{toast('🎉 Уровень '+arkLevel+' пройден!','s',1600);setTimeout(function(){if(!arkRunning)return;arkLevel++;arkLevelEl.textContent=arkLevel;buildArkLevel(arkLevel);resetArBall();saveArkState()},900)}}}
function gameOverArk(){arkRunning=false;if(arkFId)cancelAnimationFrame(arkFId);arkFId=null;clearP('arknoid');toast('Игра окончена! Очки: '+arkScore,'i',2200);setTimeout(function(){if(currentScreen==='arknoid-screen')startArknoid()},1400)}
function drawArk(){if(!arkCtx)return;var g=arkCtx.createLinearGradient(0,0,0,ARK_H);g.addColorStop(0,'#04060f');g.addColorStop(1,'#0a0620');arkCtx.fillStyle=g;arkCtx.fillRect(0,0,ARK_W,ARK_H);for(var i=0;i<arkBricks.length;i++){var b=arkBricks[i],hpr=b.hp/b.maxHp;arkCtx.globalAlpha=0.4+hpr*0.6;arkCtx.fillStyle=b.color;arkCtx.shadowColor=b.color;arkCtx.shadowBlur=8;roundRect(arkCtx,b.x,b.y,b.w,b.h,4);arkCtx.fill();arkCtx.shadowBlur=0;arkCtx.globalAlpha=1}arkCtx.fillStyle=arkSticky?'#fff':'#3f51b5';arkCtx.shadowColor=arkCtx.fillStyle;arkCtx.shadowBlur=14;roundRect(arkCtx,arkPX-arkPW/2,ARK_PY,arkPW,ARK_PH,6);arkCtx.fill();arkCtx.shadowBlur=0;for(var bi=0;bi<arkBalls.length;bi++){var ba=arkBalls[bi];arkCtx.fillStyle='#fff';arkCtx.shadowColor='#fff';arkCtx.shadowBlur=14;arkCtx.beginPath();arkCtx.arc(ba.x,ba.y,ARK_BR,0,Math.PI*2);arkCtx.fill();arkCtx.shadowBlur=0}for(var pi=0;pi<arkPUs.length;pi++){var pu=arkPUs[pi];arkCtx.fillStyle=arkPUColors[pu.type];arkCtx.beginPath();arkCtx.arc(pu.x,pu.y,10,0,Math.PI*2);arkCtx.fill();arkCtx.fillStyle='#000';arkCtx.font='bold 10px system-ui';arkCtx.textAlign='center';arkCtx.textBaseline='middle';arkCtx.fillText(arkPUIcons[pu.type],pu.x,pu.y+1)}for(var ai=0;ai<arkParticles.length;ai++){var pp=arkParticles[ai];arkCtx.globalAlpha=pp.life;arkCtx.fillStyle=pp.color;arkCtx.beginPath();arkCtx.arc(pp.x,pp.y,pp.size,0,Math.PI*2);arkCtx.fill()}arkCtx.globalAlpha=1;for(var li=0;li<arkLives;li++){arkCtx.fillStyle='#3f51b5';arkCtx.font='bold 14px system-ui';arkCtx.textAlign='left';arkCtx.fillText('❤',8+li*16,20)}arkCtx.fillStyle='rgba(255,255,255,0.6)';arkCtx.font='bold 12px system-ui';arkCtx.textAlign='right';arkCtx.fillText('Уровень '+arkLevel+' / '+ARK_MAX,ARK_W-8,20)}

var memCanvas,memCtx,memMovesEl,memPairsEl,memBestEl,memBestBox,MEM_ROWS=4,MEM_COLS=4,MEM_CELL;
var MEM_ICONS=['🍎','🍌','🍇','🍒','🍓','🥝','🍍','🍑'];
var memBoard=[],memRevealed=[],memMatched=[],memMoves=0,memPairsFound=0,memFirstFlip=null,memLocked=false,memTimeout=null;
function initMem(){if(memCanvas)return;memCanvas=$('memoryCanvas');memCtx=memCanvas.getContext('2d');memMovesEl=$('memory-moves');memPairsEl=$('memory-pairs');memBestEl=$('memory-best');memBestBox=$('memory-best-box');MEM_CELL=memCanvas.width/MEM_COLS}
function enterMemory(){initMem();var s=loadP('memory');if(s)askResume('memory',function(){resumeMemory(s)},function(){memoryShuffle()});else memoryShuffle()}
function saveMemoryState(){if(!memBoard||!memBoard.length)return;saveP('memory',{board:memBoard.slice(),revealed:memRevealed.slice(),matched:memMatched.slice(),moves:memMoves,pairsFound:memPairsFound})}
function resumeMemory(s){initMem();memBoard=s.board.slice();memRevealed=s.revealed.slice();memMatched=s.matched.slice();memMoves=s.moves;memPairsFound=s.pairsFound;memFirstFlip=null;memLocked=false;memMovesEl.textContent=memMoves;memPairsEl.textContent=memPairsFound+'/'+MEM_ICONS.length;memBestEl.textContent=getBest('memory_best')||0;drawMemory();toast('💾 Продолжаем','sv',1500)}
function memoryShuffle(){initMem();haptic(15);clearP('memory');var cards=[];for(var i=0;i<MEM_ICONS.length;i++){cards.push(MEM_ICONS[i]);cards.push(MEM_ICONS[i])}for(var i=cards.length-1;i>0;i--){var j=Math.floor(Math.random()*(i+1)),t=cards[i];cards[i]=cards[j];cards[j]=t}memBoard=cards;memRevealed=[];memMatched=[];for(var k=0;k<16;k++){memRevealed.push(false);memMatched.push(false)}memMoves=0;memPairsFound=0;memFirstFlip=null;memLocked=false;clearTimeout(memTimeout);memMovesEl.textContent='0';memPairsEl.textContent='0/'+MEM_ICONS.length;memBestEl.textContent=getBest('memory_best')||0;drawMemory()}
function drawMemory(){if(!memCtx)return;memCtx.fillStyle='#0a0612';memCtx.fillRect(0,0,memCanvas.width,memCanvas.height);var pad=6,cw=MEM_CELL-pad*2;for(var r=0;r<MEM_ROWS;r++)for(var c=0;c<MEM_COLS;c++){var i=r*MEM_COLS+c,x=c*MEM_CELL+pad,y=r*MEM_CELL+pad;var rev=memRevealed[i]||memMatched[i],mt=memMatched[i];if(rev){var g=memCtx.createLinearGradient(x,y,x+cw,y+cw);if(mt){g.addColorStop(0,'#66bb6a');g.addColorStop(1,'#2e7d32')}else{g.addColorStop(0,'#7e57c2');g.addColorStop(1,'#4527a0')}memCtx.fillStyle=g;roundRect(memCtx,x,y,cw,cw,10);memCtx.fill();memCtx.font='bold '+Math.round(cw*0.6)+'px system-ui';memCtx.textAlign='center';memCtx.textBaseline='middle';memCtx.fillText(memBoard[i],x+cw/2,y+cw/2+2)}else{var g2=memCtx.createLinearGradient(x,y,x+cw,y+cw);g2.addColorStop(0,'#3a2a5a');g2.addColorStop(1,'#1e1430');memCtx.fillStyle=g2;roundRect(memCtx,x,y,cw,cw,10);memCtx.fill();memCtx.fillStyle='rgba(255,255,255,0.1)';memCtx.font='bold '+Math.round(cw*0.35)+'px system-ui';memCtx.textAlign='center';memCtx.textBaseline='middle';memCtx.fillText('?',x+cw/2,y+cw/2)}}}
function memoryClick(e){if(memLocked)return;var rect=memCanvas.getBoundingClientRect();var x=(e.clientX-rect.left)*(memCanvas.width/rect.width),y=(e.clientY-rect.top)*(memCanvas.height/rect.height);var c=Math.floor(x/MEM_CELL),r=Math.floor(y/MEM_CELL);if(r<0||r>=MEM_ROWS||c<0||c>=MEM_COLS)return;var i=r*MEM_COLS+c;if(memMatched[i]||memRevealed[i])return;haptic(10);memRevealed[i]=true;drawMemory();if(memFirstFlip===null){memFirstFlip=i;return}var first=memFirstFlip,second=i;memMoves++;memMovesEl.textContent=memMoves;bump(memMovesEl);if(memBoard[first]===memBoard[second]){memMatched[first]=true;memMatched[second]=true;memRevealed[first]=false;memRevealed[second]=false;memFirstFlip=null;memPairsFound++;memPairsEl.textContent=memPairsFound+'/'+MEM_ICONS.length;bump(memPairsEl);haptic(30);setTimeout(drawMemory,400);if(memPairsFound===MEM_ICONS.length){setTimeout(function(){var cn=memMoves<=30?25:memMoves<=45?15:8;addCoins(cn,false);if(tryUpdateRecord('memory_best',memMoves,memBestEl,memBestBox,'int',true))toast('🏆 Рекорд: '+memMoves+' ходов! +'+cn+'🪙','r',2500);else toast('Собрано за '+memMoves+' ходов! +'+cn+'🪙','s',2000);clearP('memory');setTimeout(function(){if(currentScreen==='memory-screen')memoryShuffle()},2500)},500)}}else{memLocked=true;memTimeout=setTimeout(function(){memRevealed[first]=false;memRevealed[second]=false;memFirstFlip=null;memLocked=false;drawMemory();saveMemoryState()},800)}}
function stopMemory(){saveMemoryState();clearTimeout(memTimeout)}var shCanvas,shCtx,shScoreEl,shBestEl,shBestBox,SH_W,SH_H;
var shRun=false,shPX,shDir=0,shBullets=[],shEnemies=[],shEBullets=[],shStars=[],shParticles=[],shPUs=[];
var shScore=0,shLives=3,shMaxLives=5,shLastFire=0,shLastESpawn=0,shLastEShot=0,shLastPSpawn=0;
var shFId=null,shLT=0,shPaused=false,shCM=0,shBoss=null,shNextBoss=500,shShieldT=0,shTripleT=0,shCombo=0,shLastKill=0;
var SH_PY,SH_FCD=220,SH_PD=8000;
function initShooter(){if(shCanvas)return;shCanvas=$('shooterCanvas');shCtx=shCanvas.getContext('2d');shScoreEl=$('shooter-score');shBestEl=$('shooter-best');shBestBox=$('shooter-best-box');SH_W=shCanvas.width;SH_H=shCanvas.height;SH_PY=SH_H-60;shPX=SH_W/2}
function enterShooter(){initShooter();var s=loadP('shooter');if(s)askResume('shooter',function(){resumeShooter(s)},function(){startShooter()});else startShooter()}
function saveShooterState(){if(!shRun)return;saveP('shooter',{px:shPX,score:shScore,lives:shLives,bullets:shBullets.map(function(b){return{x:b.x,y:b.y,vx:b.vx,vy:b.vy}}),enemies:shEnemies.map(function(e){return{x:e.x,y:e.y,w:e.w,h:e.h,hp:e.hp,vy:e.vy,vx:e.vx,points:e.points,color:e.color}}),stars:shStars.map(function(s){return{x:s.x,y:s.y,speed:s.speed,size:s.size}}),boss:shBoss,nextBoss:shNextBoss})}
function resumeShooter(s){initShooter();shPX=s.px;shBullets=s.bullets.map(function(b){return{x:b.x,y:b.y,vx:b.vx,vy:b.vy}});shEnemies=s.enemies.map(function(e){return{x:e.x,y:e.y,w:e.w,h:e.h,hp:e.hp,vy:e.vy,vx:e.vx,points:e.points,color:e.color}});shStars=s.stars.map(function(s2){return{x:s2.x,y:s2.y,speed:s2.speed,size:s2.size}});shScore=s.score;shLives=s.lives;shBoss=s.boss;shNextBoss=s.nextBoss;shEBullets=[];shParticles=[];shPUs=[];shDir=0;shLastFire=0;shLastESpawn=0;shLastEShot=0;shLastPSpawn=0;shCM=Math.floor(shScore/100);shPaused=false;shShieldT=0;shTripleT=0;shCombo=0;shLastKill=0;shScoreEl.textContent=shScore;shBestEl.textContent=getBest('shooter_best');shRun=true;shLT=performance.now();if(shFId)cancelAnimationFrame(shFId);shFId=requestAnimationFrame(shLoop);toast('💾 Продолжаем','sv',1500)}
function startShooter(){initShooter();shPX=SH_W/2;shBullets=[];shEnemies=[];shEBullets=[];shParticles=[];shPUs=[];shScore=0;shLives=3;shScoreEl.textContent='0';shBestEl.textContent=getBest('shooter_best');shDir=0;shLastFire=0;shLastESpawn=0;shLastEShot=0;shLastPSpawn=0;shCM=0;shPaused=false;shBoss=null;shNextBoss=500;shShieldT=0;shTripleT=0;shCombo=0;shLastKill=0;initShStars();shRun=true;shLT=performance.now();if(shFId)cancelAnimationFrame(shFId);shFId=requestAnimationFrame(shLoop)}
function stopShooter(){saveShooterState();shRun=false;if(shFId)cancelAnimationFrame(shFId);shFId=null}
function initShStars(){shStars=[];for(var i=0;i<60;i++)shStars.push({x:Math.random()*SH_W,y:Math.random()*SH_H,speed:0.3+Math.random()*2,size:0.5+Math.random()*1.8})}
function shooterControl(a){if(!shRun)return;if(a==='left'){shDir=-1;haptic(6)}else if(a==='right'){shDir=1;haptic(6)}else if(a==='fire'){fireShBullet(true);haptic(10)}else if(a==='pause'){shPaused=!shPaused;haptic(10)}}
function fireShBullet(force){var now=performance.now();if(!force&&now-shLastFire<SH_FCD)return;shLastFire=now;if(now<shTripleT){shBullets.push({x:shPX,y:SH_PY-4,vy:-8});shBullets.push({x:shPX-10,y:SH_PY-4,vy:-8,vx:-1});shBullets.push({x:shPX+10,y:SH_PY-4,vy:-8,vx:1})}else shBullets.push({x:shPX,y:SH_PY-4,vy:-8})}
function shLoop(t){if(!shRun)return;var dt=Math.min(40,t-shLT);shLT=t;if(!shPaused)updateSh(dt,t);drawSh();shFId=requestAnimationFrame(shLoop)}
function updateSh(dt,t){shPX+=shDir*0.34*dt;shPX=Math.max(18,Math.min(SH_W-18,shPX));for(var i=0;i<shStars.length;i++){var s=shStars[i];s.y+=s.speed*dt*0.06;if(s.y>SH_H){s.y=0;s.x=Math.random()*SH_W}}if(t-shLastFire>SH_FCD)fireShBullet();for(var i=shBullets.length-1;i>=0;i--){var b=shBullets[i];b.y+=b.vy*dt*0.06;if(b.vx)b.x+=b.vx*dt*0.06;if(b.y<-10||b.x<-10||b.x>SH_W+10)shBullets.splice(i,1)}if(!shBoss&&t-shLastESpawn>800+Math.random()*800){shLastESpawn=t;spawnShEnemy()}if(t-shLastPSpawn>5000+Math.random()*4000&&shPUs.length<2){shLastPSpawn=t;spawnShPU()}if(!shBoss&&shScore>=shNextBoss){shBoss=spawnShBoss();shNextBoss+=500;toast('👹 БОСС!','i',1500);haptic(60)}for(var i=shEnemies.length-1;i>=0;i--){var e=shEnemies[i];e.y+=e.vy*dt*0.06;e.x+=e.vx*dt*0.06;if(e.x<e.w/2||e.x>SH_W-e.w/2)e.vx*=-1;if(e.y>SH_H+20){shEnemies.splice(i,1);continue}for(var j=shBullets.length-1;j>=0;j--){var b2=shBullets[j];if(Math.abs(b2.x-e.x)<e.w/2&&Math.abs(b2.y-e.y)<e.h/2){shBullets.splice(j,1);e.hp--;for(var k=0;k<4;k++)shParticles.push({x:e.x,y:e.y,vx:(Math.random()-0.5)*3,vy:(Math.random()-0.5)*3,life:1,size:2+Math.random()*2,color:e.color});if(e.hp<=0)killShEnemy(e,i);break}}}if(shBoss){var bs=shBoss;bs.y+=bs.vy*dt*0.06;bs.x+=bs.vx*dt*0.06;if(bs.x<45||bs.x>SH_W-45)bs.vx*=-1;if(bs.y>100){bs.y=100;bs.vy=0}bs.shootT=(bs.shootT||0)+dt;if(bs.shootT>900){bs.shootT=0;for(var k=-1;k<=1;k++)shEBullets.push({x:bs.x+k*20,y:bs.y+35,vy:4})}for(var j=shBullets.length-1;j>=0;j--){var bul=shBullets[j];if(Math.abs(bul.x-bs.x)<45&&Math.abs(bul.y-bs.y)<35){shBullets.splice(j,1);bs.hp--;for(var k=0;k<5;k++)shParticles.push({x:bul.x,y:bul.y,vx:(Math.random()-0.5)*4,vy:(Math.random()-0.5)*4,life:1,size:2+Math.random()*2,color:'#ff4081'});if(bs.hp<=0){shScore+=500;shScoreEl.textContent=shScore;bump(shScoreEl);for(var k=0;k<30;k++)shParticles.push({x:bs.x+(Math.random()-0.5)*90,y:bs.y+(Math.random()-0.5)*70,vx:(Math.random()-0.5)*6,vy:(Math.random()-0.5)*6,life:1,size:3+Math.random()*3,color:'#ff4081'});addCoins(10,false);toast('🎉 Босс повержен! +500','s',1800);haptic(80);if(tryUpdateRecord('shooter_best',shScore,shBestEl,shBestBox))toast('🏆 Рекорд: '+shScore,'r',1600);shBoss=null}break}}}for(var i=shPUs.length-1;i>=0;i--){var p=shPUs[i];p.y+=1.2*dt*0.06;if(p.y>SH_H+20){shPUs.splice(i,1);continue}if(Math.abs(p.x-shPX)<28&&Math.abs(p.y-SH_PY)<25){applyShPU(p.type);shPUs.splice(i,1)}}if(t-shLastEShot>900&&shEnemies.length>0){shLastEShot=t;var e2=shEnemies[Math.floor(Math.random()*shEnemies.length)];shEBullets.push({x:e2.x,y:e2.y+e2.h/2,vy:4})}for(var i=shEBullets.length-1;i>=0;i--){var b3=shEBullets[i];b3.y+=b3.vy*dt*0.06;if(b3.y>SH_H+10){shEBullets.splice(i,1);continue}if(Math.abs(b3.x-shPX)<18&&Math.abs(b3.y-SH_PY)<15){shEBullets.splice(i,1);damageShPlayer()}}for(var i=shEnemies.length-1;i>=0;i--){var e3=shEnemies[i];if(Math.abs(e3.x-shPX)<(e3.w+36)/2-6&&Math.abs(e3.y-SH_PY)<(e3.h+30)/2-6){shEnemies.splice(i,1);damageShPlayer()}}for(var i=shParticles.length-1;i>=0;i--){var p2=shParticles[i];p2.x+=p2.vx;p2.y+=p2.vy;p2.life-=0.03;if(p2.life<=0)shParticles.splice(i,1)}if(performance.now()>shTripleT)shTripleT=0;if(performance.now()>shShieldT)shShieldT=0;if(Math.floor(t/1000)%3===0)saveShooterState()}
function killShEnemy(e,idx){shEnemies.splice(idx,1);var now=performance.now();if(now-shLastKill<1500)shCombo++;else shCombo=1;shLastKill=now;var cm=Math.min(5,shCombo),pts=e.points*cm;shScore+=pts;shScoreEl.textContent=shScore;bump(shScoreEl);if(shCombo>1)toast('×'+shCombo+' комбо! +'+pts,'s',900);var ms=Math.floor(shScore/100);if(ms>shCM){addCoins((ms-shCM)*2,false);shCM=ms}if(tryUpdateRecord('shooter_best',shScore,shBestEl,shBestBox))toast('🏆 Рекорд: '+shScore,'r',1400)}
function spawnShEnemy(){var types=[{w:30,h:26,hp:1,vy:1,points:10,color:'#ff5252'},{w:34,h:30,hp:2,vy:0.8,points:20,color:'#e040fb'},{w:26,h:22,hp:1,vy:1.4,points:15,color:'#40c4ff'},{w:40,h:34,hp:3,vy:0.6,points:30,color:'#ffa726'}];var t=types[Math.floor(Math.random()*types.length)];shEnemies.push({x:t.w+Math.random()*(SH_W-t.w*2),y:-t.h,w:t.w,h:t.h,hp:t.hp,vy:t.vy,vx:(Math.random()-0.5)*0.6,points:t.points,color:t.color})}
function spawnShBoss(){return{x:SH_W/2,y:-60,w:90,h:70,hp:30+Math.floor(shScore/500)*10,vy:1.5,vx:1.2,shootT:0}}
function spawnShPU(){var types=['shield','triple','bomb','life'],weights=[0.35,0.35,0.2,0.1];var r=Math.random(),acc=0,type='shield';for(var i=0;i<types.length;i++){acc+=weights[i];if(r<acc){type=types[i];break}}shPUs.push({x:30+Math.random()*(SH_W-60),y:-20,type:type})}
function applyShPU(t){haptic(20);if(t==='shield'){shShieldT=performance.now()+SH_PD;toast('💎 Щит!','s',1200)}else if(t==='triple'){shTripleT=performance.now()+SH_PD;toast('⚡ Тройной!','s',1200)}else if(t==='bomb'){for(var i=0;i<shEnemies.length;i++){var e=shEnemies[i];shScore+=e.points;for(var k=0;k<6;k++)shParticles.push({x:e.x,y:e.y,vx:(Math.random()-0.5)*4,vy:(Math.random()-0.5)*4,life:1,size:2+Math.random()*2,color:e.color})}var cnt=shEnemies.length;shEnemies=[];shEBullets=[];shScoreEl.textContent=shScore;bump(shScoreEl);toast('💣 Бомба! Уничтожено: '+cnt,'s',1400);if(tryUpdateRecord('shooter_best',shScore,shBestEl,shBestBox))toast('🏆 Рекорд: '+shScore,'r',1400)}else if(t==='life'){if(shLives<shMaxLives){shLives++;toast('❤ +1 жизнь!','s',1200)}else{shScore+=100;shScoreEl.textContent=shScore;toast('❤ Максимум! +100','i',1200)}}}
function damageShPlayer(){if(performance.now()<shShieldT){toast('💎 Щит поглотил удар','i',800);return}shLives--;haptic(80);shCombo=0;if(shLives<=0)gameOverSh();else toast('💥 Попадание! Жизней: '+shLives,'i',900)}
function gameOverSh(){shRun=false;if(shFId)cancelAnimationFrame(shFId);shFId=null;clearP('shooter');var ce=Math.floor(shScore/100)*2;toast('Игра окончена! Очки: '+shScore+(ce?' (+'+ce+'🪙)':''),'i',2000);setTimeout(function(){if(currentScreen==='shooter-screen')startShooter()},1200)}
function drawSh(){if(!shCtx)return;var g=shCtx.createLinearGradient(0,0,0,SH_H);g.addColorStop(0,'#000510');g.addColorStop(1,'#0a0620');shCtx.fillStyle=g;shCtx.fillRect(0,0,SH_W,SH_H);for(var i=0;i<shStars.length;i++){var s=shStars[i];shCtx.fillStyle='rgba(255,255,255,'+(0.3+s.speed*0.3)+')';shCtx.beginPath();shCtx.arc(s.x,s.y,s.size,0,Math.PI*2);shCtx.fill()}var puc={shield:'#00bcd4',triple:'#ffeb3b',bomb:'#ff5252',life:'#f44336'},pui={shield:'💎',triple:'⚡',bomb:'💣',life:'❤'};for(var i=0;i<shPUs.length;i++){var p=shPUs[i];shCtx.fillStyle=puc[p.type];shCtx.shadowColor=puc[p.type];shCtx.shadowBlur=14;shCtx.beginPath();shCtx.arc(p.x,p.y,12,0,Math.PI*2);shCtx.fill();shCtx.shadowBlur=0;shCtx.font='bold 14px system-ui';shCtx.textAlign='center';shCtx.textBaseline='middle';shCtx.fillStyle='#000';shCtx.fillText(pui[p.type],p.x,p.y+1)}for(var i=0;i<shBullets.length;i++){var b=shBullets[i];shCtx.fillStyle='#ffeb3b';shCtx.shadowColor='#ffeb3b';shCtx.shadowBlur=10;shCtx.fillRect(b.x-1.5,b.y-8,3,12);shCtx.shadowBlur=0}for(var i=0;i<shEnemies.length;i++){var e=shEnemies[i];shCtx.fillStyle=e.color;shCtx.shadowColor=e.color;shCtx.shadowBlur=12;shCtx.beginPath();shCtx.moveTo(e.x,e.y+e.h/2);shCtx.lineTo(e.x-e.w/2,e.y-e.h/2);shCtx.lineTo(e.x+e.w/2,e.y-e.h/2);shCtx.closePath();shCtx.fill();shCtx.shadowBlur=0;shCtx.fillStyle='#fff';shCtx.beginPath();shCtx.arc(e.x,e.y-2,2.5,0,Math.PI*2);shCtx.fill()}if(shBoss){var bs=shBoss;shCtx.fillStyle='#ff4081';shCtx.shadowColor='#ff4081';shCtx.shadowBlur=20;roundRect(shCtx,bs.x-45,bs.y-35,90,70,12);shCtx.fill();shCtx.shadowBlur=0;shCtx.fillStyle='#fff';shCtx.font='bold 28px system-ui';shCtx.textAlign='center';shCtx.textBaseline='middle';shCtx.fillText('👹',bs.x,bs.y);var mh=30+Math.floor(shScore/500)*10,hpp=bs.hp/mh;shCtx.fillStyle='rgba(0,0,0,0.5)';shCtx.fillRect(bs.x-45,bs.y-45,90,5);shCtx.fillStyle='#ff4081';shCtx.fillRect(bs.x-45,bs.y-45,90*hpp,5)}for(var i=0;i<shEBullets.length;i++){var b4=shEBullets[i];shCtx.fillStyle='#ff5252';shCtx.shadowColor='#ff5252';shCtx.shadowBlur=8;shCtx.beginPath();shCtx.arc(b4.x,b4.y,3,0,Math.PI*2);shCtx.fill();shCtx.shadowBlur=0}for(var i=0;i<shParticles.length;i++){var p2=shParticles[i];shCtx.globalAlpha=p2.life;shCtx.fillStyle=p2.color;shCtx.beginPath();shCtx.arc(p2.x,p2.y,p2.size,0,Math.PI*2);shCtx.fill()}shCtx.globalAlpha=1;if(performance.now()<shShieldT){shCtx.strokeStyle='rgba(0,188,212,0.6)';shCtx.lineWidth=2;shCtx.beginPath();shCtx.arc(shPX,SH_PY,25,0,Math.PI*2);shCtx.stroke()}shCtx.save();shCtx.translate(shPX,SH_PY);shCtx.fillStyle='#4dd0e1';shCtx.shadowColor='#4dd0e1';shCtx.shadowBlur=14;shCtx.beginPath();shCtx.moveTo(0,-15);shCtx.lineTo(-18,15);shCtx.lineTo(-9,9);shCtx.lineTo(9,9);shCtx.lineTo(18,15);shCtx.closePath();shCtx.fill();shCtx.shadowBlur=0;shCtx.fillStyle='#b2ebf2';shCtx.beginPath();shCtx.arc(0,-2,5,0,Math.PI*2);shCtx.fill();shCtx.restore();for(var i=0;i<shLives;i++){shCtx.fillStyle='#4dd0e1';shCtx.font='bold 14px system-ui';shCtx.textAlign='left';shCtx.fillText('❤',6+i*16,20)}if(shCombo>1){shCtx.fillStyle='#ffd54f';shCtx.font='bold 16px system-ui';shCtx.textAlign='right';shCtx.fillText('×'+Math.min(5,shCombo)+' КОМБО',SH_W-8,22)}}

var tCanvas,tCtx,tScoreEl,tBestEl,tBestBox,tPauseBtn,tGrid=[],tCur=null,tNext=null,tScore=0,tRun=false,tPaused=false,tFId=null,tLT=0,tDI=700,tDC=0,tLines=0,tCM=0;
var T_COLS=10,T_ROWS=20,T_CELL;
var T_PIECES={I:{shape:[[1,1,1,1]],color:'#00e5ff'},O:{shape:[[1,1],[1,1]],color:'#ffeb3b'},T:{shape:[[0,1,0],[1,1,1]],color:'#ba68c8'},S:{shape:[[0,1,1],[1,1,0]],color:'#66bb6a'},Z:{shape:[[1,1,0],[0,1,1]],color:'#ef5350'},J:{shape:[[1,0,0],[1,1,1]],color:'#42a5f5'},L:{shape:[[0,0,1],[1,1,1]],color:'#ff9800'}};
function initTetris(){if(tCanvas)return;tCanvas=$('tetrisCanvas');tCtx=tCanvas.getContext('2d');tScoreEl=$('tetris-score');tBestEl=$('tetris-best');tBestBox=$('tetris-best-box');tPauseBtn=$('tetrisPauseBtn');T_CELL=tCanvas.width/T_COLS}
function enterTetris(){initTetris();var s=loadP('tetris');if(s)askResume('tetris',function(){resumeTetris(s)},function(){startTetris()});else startTetris()}
function saveTetrisState(){if(!tRun)return;saveP('tetris',{grid:tGrid.map(function(r){return r.map(function(c){return c})}),current:tCur?{type:tCur.type,shape:tCur.shape.map(function(r){return r.slice()}),color:tCur.color,x:tCur.x,y:tCur.y}:null,next:tNext?{type:tNext.type,shape:tNext.shape.map(function(r){return r.slice()}),color:tNext.color}:null,score:tScore,lines:tLines,dropInterval:tDI})}
function resumeTetris(s){initTetris();tGrid=s.grid.map(function(r){return r.map(function(c){return c})});tCur=s.current?{type:s.current.type,shape:s.current.shape.map(function(r){return r.slice()}),color:s.current.color,x:s.current.x,y:s.current.y}:null;tNext=s.next?{type:s.next.type,shape:s.next.shape.map(function(r){return r.slice()}),color:s.next.color}:null;tScore=s.score;tLines=s.lines;tDI=s.dropInterval;tDC=0;tCM=Math.floor(tScore/200);tScoreEl.textContent=tScore;tBestEl.textContent=getBest('tetris_best');tPaused=false;tPauseBtn.textContent='ПАУЗА';tRun=true;tLT=performance.now();if(tFId)cancelAnimationFrame(tFId);tFId=requestAnimationFrame(tLoop);toast('💾 Продолжаем','sv',1500)}
function startTetris(){initTetris();tGrid=[];for(var r=0;r<T_ROWS;r++){var row=[];for(var c=0;c<T_COLS;c++)row.push(null);tGrid.push(row)}tScore=0;tLines=0;tCM=0;tScoreEl.textContent='0';tBestEl.textContent=getBest('tetris_best');tPaused=false;tPauseBtn.textContent='ПАУЗА';tDI=700;tDC=0;tNext=randTP();spawnTP();tRun=true;tLT=performance.now();if(tFId)cancelAnimationFrame(tFId);tFId=requestAnimationFrame(tLoop)}
function stopTetris(){saveTetrisState();tRun=false;if(tFId)cancelAnimationFrame(tFId);tFId=null}
function randTP(){var keys=Object.keys(T_PIECES),k=keys[Math.floor(Math.random()*keys.length)];return{type:k,shape:T_PIECES[k].shape.map(function(r){return r.slice()}),color:T_PIECES[k].color,x:0,y:0}}
function spawnTP(){tCur=tNext||randTP();tNext=randTP();tCur.x=Math.floor((T_COLS-tCur.shape[0].length)/2);tCur.y=0;if(collTP(tCur.x,tCur.y,tCur.shape))gameOverT()}
function collTP(x,y,shape){for(var r=0;r<shape.length;r++)for(var c=0;c<shape[r].length;c++){if(!shape[r][c])continue;var nx=x+c,ny=y+r;if(nx<0||nx>=T_COLS||ny>=T_ROWS)return true;if(ny>=0&&tGrid[ny][nx])return true}return false}
function lockTP(){for(var r=0;r<tCur.shape.length;r++)for(var c=0;c<tCur.shape[r].length;c++)if(tCur.shape[r][c]){var ny=tCur.y+r,nx=tCur.x+c;if(ny>=0)tGrid[ny][nx]=tCur.color}clearTL();spawnTP()}
function clearTL(){var cl=0;for(var r=T_ROWS-1;r>=0;r--){var full=true;for(var c=0;c<T_COLS;c++)if(!tGrid[r][c]){full=false;break}if(full){tGrid.splice(r,1);var row=[];for(var k=0;k<T_COLS;k++)row.push(null);tGrid.unshift(row);cl++;r++}}if(cl>0){var pts=[0,100,300,500,800][cl]||800;tScore+=pts;tLines+=cl;tScoreEl.textContent=tScore;bump(tScoreEl);haptic(cl>=4?60:25);var ms=Math.floor(tScore/200);if(ms>tCM){addCoins(ms-tCM,false);tCM=ms}if(tryUpdateRecord('tetris_best',tScore,tBestEl,tBestBox))toast('🏆 Рекорд: '+tScore,'r',1400);else if(cl===4)toast('🎉 ТЕТРИС! +800','s',1200);tDI=Math.max(120,700-Math.floor(tLines/5)*80);saveTetrisState()}}
function tetrisControl(a){if(!tRun)return;if(a==='pause'){tPaused=!tPaused;tPauseBtn.textContent=tPaused?'ПРОДОЛЖИТЬ':'ПАУЗА';haptic(10);return}if(tPaused)return;if(a==='left'){if(!collTP(tCur.x-1,tCur.y,tCur.shape))tCur.x--;haptic(6)}else if(a==='right'){if(!collTP(tCur.x+1,tCur.y,tCur.shape))tCur.x++;haptic(6)}else if(a==='rotate'){var rot=rotM(tCur.shape);if(!collTP(tCur.x,tCur.y,rot))tCur.shape=rot;haptic(8)}else if(a==='drop'){while(!collTP(tCur.x,tCur.y+1,tCur.shape))tCur.y++;lockTP();haptic(12)}}
function rotM(m){var rows=m.length,cols=m[0].length,out=[];for(var c=0;c<cols;c++){var row=[];for(var r=0;r<rows;r++)row.push(0);out.push(row)}for(var r2=0;r2<rows;r2++)for(var c2=0;c2<cols;c2++)out[c2][rows-1-r2]=m[r2][c2];return out}
function tLoop(t){if(!tRun)return;var dt=t-tLT;tLT=t;if(!tPaused){tDC+=dt;if(tDC>tDI){tDC=0;if(!collTP(tCur.x,tCur.y+1,tCur.shape))tCur.y++;else lockTP()}}drawT();tFId=requestAnimationFrame(tLoop)}
function gameOverT(){tRun=false;if(tFId)cancelAnimationFrame(tFId);tFId=null;clearP('tetris');var ce=Math.floor(tScore/200);toast('Игра окончена! Очки: '+tScore+(ce?' (+'+ce+'🪙)':''),'i',2000);setTimeout(function(){if(currentScreen==='tetris-screen')startTetris()},1200)}
function drawT(){if(!tCtx)return;tCtx.fillStyle='#021208';tCtx.fillRect(0,0,tCanvas.width,tCanvas.height);tCtx.strokeStyle='rgba(0,230,118,0.08)';for(var i=1;i<T_COLS;i++){tCtx.beginPath();tCtx.moveTo(i*T_CELL,0);tCtx.lineTo(i*T_CELL,tCanvas.height);tCtx.stroke()}for(var j=1;j<T_ROWS;j++){tCtx.beginPath();tCtx.moveTo(0,j*T_CELL);tCtx.lineTo(tCanvas.width,j*T_CELL);tCtx.stroke()}for(var r=0;r<T_ROWS;r++)for(var c=0;c<T_COLS;c++)if(tGrid[r][c])drawTC(c,r,tGrid[r][c]);if(tCur)for(var r2=0;r2<tCur.shape.length;r2++)for(var c2=0;c2<tCur.shape[r2].length;c2++)if(tCur.shape[r2][c2])drawTC(tCur.x+c2,tCur.y+r2,tCur.color);if(tNext){var px=tCanvas.width-60,py=10;tCtx.fillStyle='rgba(0,0,0,0.6)';roundRect(tCtx,px-6,py-4,56,56,8);tCtx.fill();tCtx.fillStyle='rgba(255,255,255,0.5)';tCtx.font='bold 9px system-ui';tCtx.textAlign='center';tCtx.fillText('ДАЛЕЕ',px+22,py+6);var cs=10,ox=px+22-(tNext.shape[0].length*cs)/2,oy=py+16;for(var r3=0;r3<tNext.shape.length;r3++)for(var c3=0;c3<tNext.shape[r3].length;c3++)if(tNext.shape[r3][c3]){tCtx.fillStyle=tNext.color;tCtx.fillRect(ox+c3*cs,oy+r3*cs,cs-1,cs-1)}}if(tPaused){tCtx.fillStyle='rgba(0,0,0,0.6)';tCtx.fillRect(0,0,tCanvas.width,tCanvas.height);tCtx.fillStyle='#fff';tCtx.font='bold 24px system-ui';tCtx.textAlign='center';tCtx.textBaseline='middle';tCtx.fillText('ПАУЗА',tCanvas.width/2,tCanvas.height/2)}}
function drawTC(c,r,color){var x=c*T_CELL,y=r*T_CELL;tCtx.fillStyle=color;tCtx.shadowColor=color;tCtx.shadowBlur=8;roundRect(tCtx,x+1,y+1,T_CELL-2,T_CELL-2,3);tCtx.fill();tCtx.shadowBlur=0;tCtx.fillStyle='rgba(255,255,255,0.25)';roundRect(tCtx,x+2,y+2,T_CELL-4,T_CELL*0.35,2);tCtx.fill()}

var twCanvas,twCtx,twWaveEl,twGoldEl,twHpEl,twBestEl,twBestBox,TW_W,TW_H;
var TW_PATH=[{x:-20,y:60},{x:100,y:60},{x:100,y:180},{x:300,y:180},{x:300,y:300},{x:100,y:300},{x:100,y:420},{x:340,y:420},{x:340,y:480}];
var TW_SLOTS=[{x:60,y:30},{x:60,y:90},{x:140,y:30},{x:140,y:90},{x:220,y:30},{x:220,y:90},{x:340,y:30},{x:340,y:90},{x:60,y:150},{x:140,y:150},{x:220,y:150},{x:340,y:150},{x:220,y:220},{x:260,y:220},{x:140,y:220},{x:60,y:250},{x:60,y:320},{x:140,y:250},{x:140,y:320},{x:220,y:250},{x:220,y:320},{x:340,y:250},{x:340,y:320},{x:60,y:390},{x:220,y:390},{x:260,y:390},{x:340,y:390},{x:220,y:460},{x:280,y:460}];
var TOWER_TYPES={arrow:{name:'Лучник',baseCost:50,baseRange:85,baseDamage:8,baseFireRate:400,color:'#8bc34a',projectileColor:'#cddc39'},fire:{name:'Огонь',baseCost:100,baseRange:65,baseDamage:22,baseFireRate:800,color:'#ff5722',projectileColor:'#ff7043'},ice:{name:'Лёд',baseCost:75,baseRange:75,baseDamage:6,baseFireRate:500,color:'#03a9f4',projectileColor:'#4fc3f7',slow:0.5,slowDuration:1500}};
var TOWER_MAX=5,TOWER_MULT={damage:[1,1.5,2.2,3.2,4.5],range:[1,1.1,1.2,1.3,1.45],fireRate:[1,0.9,0.8,0.72,0.65]};
function twStat(type,lvl,stat){var base=TOWER_TYPES[type],l=Math.max(1,Math.min(TOWER_MAX,lvl));if(stat==='damage')return Math.round(base.baseDamage*TOWER_MULT.damage[l-1]);if(stat==='range')return Math.round(base.baseRange*TOWER_MULT.range[l-1]);if(stat==='fireRate')return Math.round(base.baseFireRate*TOWER_MULT.fireRate[l-1]);return base[stat]}
function twUpCost(tw){if(tw.level>=TOWER_MAX)return null;return Math.round(TOWER_TYPES[tw.type].baseCost*(0.8+tw.level*0.7))}
function twSell(tw){return Math.round(TOWER_TYPES[tw.type].baseCost*0.5+(tw.level-1)*30)}
var twRun=false,twFId=null,twLT=0,twTowers=[],twEnemies=[],twProj=[],twParticles=[],twGold=250,twWave=0,twWaveActive=false,twSelType=null,twHp=100,twHpMax=100,twBest=0,twCM=0,twSQ=[],twSpawnT=0,twWCP=false,twMerge=false,twSelTower=null,twFreezeT=0;
var TW_AB={bomb:{cost:200},freeze:{cost:150},heal:{cost:100}};
function initTower(){if(twCanvas)return;twCanvas=$('towerCanvas');twCtx=twCanvas.getContext('2d');twWaveEl=$('tower-wave');twGoldEl=$('tower-gold');twHpEl=$('tower-hp');twBestEl=$('tower-best');twBestBox=$('tower-best-box');TW_W=twCanvas.width;TW_H=twCanvas.height}
function enterTower(){initTower();var s=loadP('tower');if(s)askResume('tower',function(){resumeTower(s)},function(){startTower()});else startTower()}
function saveTowerState(){if(!twRun)return;saveP('tower',{towers:twTowers.map(function(t){return{x:t.x,y:t.y,type:t.type,level:t.level,angle:t.angle||0}}),gold:twGold,wave:twWave,baseHp:twHp,baseHpMax:twHpMax})}
function resumeTower(s){initTower();twTowers=s.towers.map(function(t){return{x:t.x,y:t.y,type:t.type,level:t.level,lastShot:0,angle:t.angle||0}});twGold=s.gold;twWave=s.wave;twHp=s.baseHp;twHpMax=s.baseHpMax||100;twEnemies=[];twProj=[];twParticles=[];twWaveActive=false;twWCP=false;twSQ=[];twSpawnT=0;twSelType=null;twMerge=false;twSelTower=null;twFreezeT=0;twCM=Math.floor(twGold/100);twBest=getBest('tower_best');twWaveEl.textContent=twWave;twGoldEl.textContent=twGold;twHpEl.textContent=Math.max(0,Math.round(twHp));twBestEl.textContent=twBest;for(var i=0;i<TW_SLOTS.length;i++)TW_SLOTS[i].occupied=false;for(var j=0;j<twTowers.length;j++){var t2=twTowers[j];for(var k=0;k<TW_SLOTS.length;k++){if(Math.hypot(TW_SLOTS[k].x-t2.x,TW_SLOTS[k].y-t2.y)<15)TW_SLOTS[k].occupied=true}}updateTwTools();twRun=true;twLT=performance.now();if(twFId)cancelAnimationFrame(twFId);twFId=requestAnimationFrame(twLoop);toast('💾 Волна '+twWave,'sv',1500)}
function startTower(){initTower();twTowers=[];twEnemies=[];twProj=[];twParticles=[];twGold=250;twWave=0;twWaveActive=false;twSelType=null;twHp=100;twHpMax=100;twSQ=[];twSpawnT=0;twWCP=false;twCM=0;twMerge=false;twSelTower=null;twFreezeT=0;twBest=getBest('tower_best');twWaveEl.textContent='0';twGoldEl.textContent=twGold;twHpEl.textContent=twHp;twBestEl.textContent=twBest;for(var i=0;i<TW_SLOTS.length;i++)TW_SLOTS[i].occupied=false;updateTwTools();twRun=true;twLT=performance.now();if(twFId)cancelAnimationFrame(twFId);twFId=requestAnimationFrame(twLoop)}
function stopTower(){saveTowerState();twRun=false;if(twFId)cancelAnimationFrame(twFId);twFId=null}
function updateTwTools(){var btns=document.querySelectorAll('.tbt[data-type]');for(var i=0;i<btns.length;i++){var t=btns[i].dataset.type;btns[i].disabled=twGold<TOWER_TYPES[t].baseCost;if(twSelType===t)btns[i].classList.add('sel');else btns[i].classList.remove('sel')}var ml=$('mergeModeLabel');if(ml)ml.textContent=twMerge?'ON':'OFF'}
function selectTower(t){if(!twRun)return;haptic(10);twSelType=twSelType===t?null:t;if(twSelType)twMerge=false;twSelTower=null;updateTwTools()}
function toggleMergeMode(){if(!twRun)return;haptic(15);twMerge=!twMerge;twSelType=null;twSelTower=null;updateTwTools();toast(twMerge?'🔗 Слияние: тапни 2 одинаковые':'Слияние выкл','i',1200)}
function startTowerWave(){if(!twRun||twWaveActive)return;haptic(20);twWave++;twWaveEl.textContent=twWave;twWaveActive=true;twWCP=false;var cnt=6+twWave*2,bhp=25+twWave*10,sp=0.6+twWave*0.04;twSQ=[];for(var i=0;i<cnt;i++){var type='normal',r=Math.random();if(twWave>=2&&r<0.2)type='fast';else if(twWave>=3&&r<0.35)type='tank';else if(twWave>=4&&r<0.5)type='flying';var hp=bhp,s=sp,rw=15+twWave*2;if(type==='fast'){hp=bhp*0.6;s=sp*1.8;rw=12+twWave*2}if(type==='tank'){hp=bhp*2.5;s=sp*0.6;rw=30+twWave*3}if(type==='flying'){hp=bhp*0.8;s=sp*1.3;rw=20+twWave*2}twSQ.push({hp:hp,speed:s,reward:rw,type:type})}if(twWave%5===0)twSQ.push({hp:bhp*10,speed:sp*0.4,reward:200+twWave*10,type:'boss'});twSpawnT=0;saveTowerState()}
function twLoop(t){if(!twRun)return;var dt=Math.min(40,t-twLT);twLT=t;updateTw(dt,t);drawTw();twFId=requestAnimationFrame(twLoop)}
function towerClick(e){if(!twRun)return;var rect=twCanvas.getBoundingClientRect(),x=(e.clientX-rect.left)*(twCanvas.width/rect.width),y=(e.clientY-rect.top)*(twCanvas.height/rect.height);var tapped=null;for(var i=0;i<twTowers.length;i++){if(Math.hypot(twTowers[i].x-x,twTowers[i].y-y)<22){tapped=twTowers[i];break}}if(tapped){if(twMerge){if(!twSelTower){twSelTower=tapped;haptic(10);return}if(twSelTower===tapped){twSelTower=null;return}if(twSelTower.type!==tapped.type||twSelTower.level!==tapped.level||twSelTower.level>=TOWER_MAX){toast('Нельзя слить','i',1200);twSelTower=null;return}var idx=twTowers.indexOf(twSelTower);if(idx>=0){twTowers.splice(idx,1);for(var s2=0;s2<TW_SLOTS.length;s2++){if(Math.hypot(TW_SLOTS[s2].x-twSelTower.x,TW_SLOTS[s2].y-twSelTower.y)<15)TW_SLOTS[s2].occupied=false}}tapped.level++;haptic(40);toast('🔗 Слияние! Ур.'+tapped.level,'s',1600);twSelTower=null;updateTwTools();saveTowerState();return}var cost=twUpCost(tapped);if(cost===null){var sv=twSell(tapped);if(confirm('Продать за '+sv+'🪙?')){twGold+=sv;twGoldEl.textContent=twGold;var i2=twTowers.indexOf(tapped);if(i2>=0)twTowers.splice(i2,1);for(var s3=0;s3<TW_SLOTS.length;s3++){if(Math.hypot(TW_SLOTS[s3].x-tapped.x,TW_SLOTS[s3].y-tapped.y)<15)TW_SLOTS[s3].occupied=false}haptic(30);toast('Продано','s',1000);updateTwTools();saveTowerState()}return}if(twGold<cost){toast('Мало золота','i',900);return}twGold-=cost;twGoldEl.textContent=twGold;bump(twGoldEl);tapped.level++;haptic(30);toast('⬆ Ур.'+tapped.level+'! Урон: '+twStat(tapped.type,tapped.level,'damage'),'s',1400);updateTwTools();saveTowerState();return}for(var i=0;i<TW_SLOTS.length;i++){var slot=TW_SLOTS[i];if(Math.hypot(slot.x-x,slot.y-y)<22){if(slot.occupied){toast('Занято','i',900);return}if(!twSelType){toast('Выберите башню','i',1000);return}var bc=TOWER_TYPES[twSelType].baseCost;if(twGold<bc){toast('Мало золота','i',900);return}twGold-=bc;twGoldEl.textContent=twGold;bump(twGoldEl);twTowers.push({x:slot.x,y:slot.y,type:twSelType,level:1,lastShot:0,angle:0});slot.occupied=true;haptic(15);updateTwTools();saveTowerState();return}}}
function towerAbility(ab){if(!twRun)return;var c=TW_AB[ab];if(!c)return;if(twGold<c.cost){toast('Мало золота','i',900);return}twGold-=c.cost;twGoldEl.textContent=twGold;bump(twGoldEl);haptic(30);if(ab==='bomb'){var cnt=0;for(var i=twEnemies.length-1;i>=0;i--){var e=twEnemies[i];if(e.type==='boss'){e.hp-=100;if(e.hp<=0){twGold+=e.reward;twEnemies.splice(i,1);cnt++}}else{twGold+=e.reward;twEnemies.splice(i,1);cnt++}}twGoldEl.textContent=twGold;toast('💣 Уничтожено: '+cnt,'s',1600)}else if(ab==='freeze'){twFreezeT=performance.now()+5000;for(var i=0;i<twEnemies.length;i++){twEnemies[i].slowUntil=performance.now()+5000;twEnemies[i].slowFactor=0.1}toast('🧊 Заморожено!','s',1600)}else if(ab==='heal'){twHp=Math.min(twHpMax,twHp+30);twHpEl.textContent=Math.max(0,Math.round(twHp));bump(twHpEl);toast('💚 +30 HP','s',1600)}updateTwTools()}
function spawnTwEnemy(type,hp,sp,rw){twEnemies.push({x:TW_PATH[0].x,y:TW_PATH[0].y,pathIdx:0,hp:hp,maxHp:hp,speed:sp,reward:rw,type:type,slowUntil:0,slowFactor:1})}
function updateTw(dt,t){if(twWaveActive&&twSQ.length>0){twSpawnT-=dt;var interval=600-Math.min(300,twWave*15);if(twSpawnT<=0){twSpawnT=interval;var e=twSQ.shift();spawnTwEnemy(e.type,e.hp,e.speed,e.reward)}}for(var i=twEnemies.length-1;i>=0;i--){var e=twEnemies[i],sm=t<e.slowUntil?e.slowFactor:1,sp=e.speed*sm,tg=TW_PATH[e.pathIdx+1];if(!tg){twEnemies.splice(i,1);var dmg=e.type==='boss'?30:e.type==='tank'?12:6;twHp-=dmg;twHpEl.textContent=Math.max(0,Math.round(twHp));bump(twHpEl);haptic(80);if(twHp<=0){gameOverTw();return}toast('💔 База: -'+dmg+' HP','i',900);continue}var dx=tg.x-e.x,dy=tg.y-e.y,dist=Math.hypot(dx,dy),mv=sp*dt*0.08;if(dist<=mv){e.x=tg.x;e.y=tg.y;e.pathIdx++}else{e.x+=dx/dist*mv;e.y+=dy/dist*mv}}for(var i=0;i<twTowers.length;i++){var tw=twTowers[i],fr=twStat(tw.type,tw.level,'fireRate');if(t-tw.lastShot<fr)continue;var range=twStat(tw.type,tw.level,'range'),target=null,minD=Infinity;for(var j=0;j<twEnemies.length;j++){var e2=twEnemies[j],d=Math.hypot(e2.x-tw.x,e2.y-tw.y);if(d<range&&d<minD){minD=d;target=e2}}if(target){tw.lastShot=t;tw.angle=Math.atan2(target.y-tw.y,target.x-tw.x);var b=TOWER_TYPES[tw.type];twProj.push({x:tw.x,y:tw.y,target:target,damage:twStat(tw.type,tw.level,'damage'),speed:5,color:b.projectileColor,slow:b.slow,slowDuration:b.slowDuration})}}for(var i=twProj.length-1;i>=0;i--){var p=twProj[i];if(!p.target||p.target.hp<=0){twProj.splice(i,1);continue}var dx=p.target.x-p.x,dy=p.target.y-p.y,dist=Math.hypot(dx,dy),mv=p.speed*dt*0.15;if(dist<=mv){p.target.hp-=p.damage;if(p.slow){p.target.slowUntil=t+p.slowDuration;p.target.slowFactor=p.slow}for(var k=0;k<4;k++)twParticles.push({x:p.target.x,y:p.target.y,vx:(Math.random()-0.5)*3,vy:(Math.random()-0.5)*3,life:1,size:2+Math.random()*2,color:p.color});if(p.target.hp<=0){twGold+=p.target.reward;twGoldEl.textContent=twGold;bump(twGoldEl);var ms=Math.floor(twGold/100);if(ms>twCM){addCoins((ms-twCM)*2,false);twCM=ms}var idx=twEnemies.indexOf(p.target);if(idx>=0)twEnemies.splice(idx,1);updateTwTools()}twProj.splice(i,1)}else{p.x+=dx/dist*mv;p.y+=dy/dist*mv}}for(var i=twParticles.length-1;i>=0;i--){var p2=twParticles[i];p2.x+=p2.vx;p2.y+=p2.vy;p2.life-=0.025;if(p2.life<=0)twParticles.splice(i,1)}if(twWaveActive&&twSQ.length===0&&twEnemies.length===0&&!twWCP){twWaveActive=false;twWCP=true;var bonus=40+twWave*8;twGold+=bonus;twGoldEl.textContent=twGold;bump(twGoldEl);twHp=Math.min(twHpMax,twHp+15);twHpEl.textContent=Math.max(0,Math.round(twHp));bump(twHpEl);twHpMax+=5;toast('🎉 Волна '+twWave+'! +'+bonus+'🪙','s',2000);if(twWave>twBest){twBest=twWave;localStorage.setItem('tower_best',twBest);twBestEl.textContent=twBest;bump(twBestEl)}updateTwTools();saveTowerState()}}
function gameOverTw(){twRun=false;if(twFId)cancelAnimationFrame(twFId);twFId=null;clearP('tower');toast('💀 База уничтожена! Волна: '+twWave,'i',2500);setTimeout(function(){if(currentScreen==='tower-screen')startTower()},1500)}
function drawTw(){if(!twCtx)return;var g=twCtx.createLinearGradient(0,0,0,TW_H);g.addColorStop(0,'#0f0602');g.addColorStop(1,'#050200');twCtx.fillStyle=g;twCtx.fillRect(0,0,TW_W,TW_H);twCtx.strokeStyle='rgba(255,193,7,0.35)';twCtx.lineWidth=34;twCtx.lineCap='round';twCtx.lineJoin='round';twCtx.beginPath();twCtx.moveTo(TW_PATH[0].x,TW_PATH[0].y);for(var i=1;i<TW_PATH.length;i++)twCtx.lineTo(TW_PATH[i].x,TW_PATH[i].y);twCtx.stroke();var end=TW_PATH[TW_PATH.length-1];twCtx.fillStyle=twHp>twHpMax*0.5?'#4caf50':twHp>twHpMax*0.25?'#ff9800':'#f44336';twCtx.shadowColor=twCtx.fillStyle;twCtx.shadowBlur=16;roundRect(twCtx,end.x-22,end.y-22,44,44,8);twCtx.fill();twCtx.shadowBlur=0;twCtx.fillStyle='#fff';twCtx.font='bold 20px system-ui';twCtx.textAlign='center';twCtx.textBaseline='middle';twCtx.fillText('🏰',end.x,end.y);for(var i=0;i<TW_SLOTS.length;i++){var s=TW_SLOTS[i];if(s.occupied)continue;twCtx.strokeStyle='rgba(255,255,255,0.2)';twCtx.lineWidth=2;twCtx.setLineDash([4,4]);twCtx.beginPath();twCtx.arc(s.x,s.y,18,0,Math.PI*2);twCtx.stroke();twCtx.setLineDash([])}for(var i=0;i<twTowers.length;i++){var tw=twTowers[i],range=twStat(tw.type,tw.level,'range'),base=TOWER_TYPES[tw.type];twCtx.fillStyle=base.color;twCtx.globalAlpha=0.06+tw.level*0.01;twCtx.beginPath();twCtx.arc(tw.x,tw.y,range,0,Math.PI*2);twCtx.fill();twCtx.globalAlpha=1;if(twSelTower===tw){twCtx.strokeStyle='#ba68c8';twCtx.lineWidth=4;twCtx.beginPath();twCtx.arc(tw.x,tw.y,20,0,Math.PI*2);twCtx.stroke()}twCtx.fillStyle=base.color;twCtx.shadowColor=base.color;twCtx.shadowBlur=10+tw.level*2;twCtx.beginPath();twCtx.arc(tw.x,tw.y,14,0,Math.PI*2);twCtx.fill();twCtx.shadowBlur=0;twCtx.fillStyle='#000';twCtx.font='bold 12px system-ui';twCtx.textAlign='center';twCtx.textBaseline='middle';var ic=tw.type==='arrow'?'🏹':tw.type==='fire'?'🔥':'❄️';twCtx.fillText(ic,tw.x,tw.y);twCtx.fillStyle='#ffd54f';twCtx.font='bold 10px system-ui';twCtx.fillText('★'.repeat(tw.level),tw.x,tw.y+22)}for(var i=0;i<twEnemies.length;i++){var e=twEnemies[i],hpp=e.hp/e.maxHp,isS=t<e.slowUntil||performance.now()<twFreezeT;var color,size=12,icon='';if(e.type==='fast'){color='#ffeb3b';size=10}else if(e.type==='tank'){color='#8e24aa';size=16}else if(e.type==='flying'){color='#00bcd4';size=12;icon='🦅'}else if(e.type==='boss'){color='#ff4081';size=22;icon='👹'}else color='#e53935';if(isS)color='#4fc3f7';twCtx.fillStyle=color;twCtx.shadowColor=color;twCtx.shadowBlur=8;twCtx.beginPath();twCtx.arc(e.x,e.y,size,0,Math.PI*2);twCtx.fill();twCtx.shadowBlur=0;if(icon){twCtx.font='bold '+(size+4)+'px system-ui';twCtx.textAlign='center';twCtx.textBaseline='middle';twCtx.fillText(icon,e.x,e.y-size-6)}twCtx.fillStyle='rgba(0,0,0,0.5)';twCtx.fillRect(e.x-14,e.y-size-4,28,4);twCtx.fillStyle=hpp>0.5?'#4caf50':hpp>0.25?'#ff9800':'#f44336';twCtx.fillRect(e.x-14,e.y-size-4,28*hpp,4)}for(var i=0;i<twProj.length;i++){var p=twProj[i];twCtx.fillStyle=p.color;twCtx.shadowColor=p.color;twCtx.shadowBlur=8;twCtx.beginPath();twCtx.arc(p.x,p.y,4,0,Math.PI*2);twCtx.fill();twCtx.shadowBlur=0}for(var i=0;i<twParticles.length;i++){var p2=twParticles[i];twCtx.globalAlpha=p2.life;twCtx.fillStyle=p2.color;twCtx.beginPath();twCtx.arc(p2.x,p2.y,p2.size,0,Math.PI*2);twCtx.fill()}twCtx.globalAlpha=1;twCtx.fillStyle='rgba(0,0,0,0.5)';twCtx.fillRect(0,0,TW_W,20);twCtx.fillStyle=twWaveActive?'#ffd54f':'#4caf50';twCtx.font='bold 12px system-ui';twCtx.textAlign='left';twCtx.textBaseline='middle';if(twWaveActive)twCtx.fillText('⚔ Волна '+twWave+' · Врагов: '+(twEnemies.length+twSQ.length),8,10);else if(twWave>0)twCtx.fillText('✅ Волна '+twWave+' пройдена',8,10);else twCtx.fillText('Расставь башни и жми ▶',8,10);if(twMerge){twCtx.fillStyle='#ba68c8';twCtx.fillRect(TW_W-70,0,70,20);twCtx.fillStyle='#fff';twCtx.fillText('🔗 СЛИЯНИЕ',TW_W-62,10)}}

var duelCanvas,duelCtx,duelS1El,duelS2El,duelRoundEl,DUEL_W,DUEL_H,DUEL_GRID=11,DUEL_CELL;
var duelRun=false,duelFId=null,duelLT=0,duelTanks=[],duelBullets=[],duelParticles=[],duelWins=[0,0],duelRoundNum=0,duelActive=true,duelWinner=null,duelRT=0,duelWalls=[];
function initDuel(){if(duelCanvas)return;duelCanvas=$('duelCanvas');duelCtx=duelCanvas.getContext('2d');duelS1El=$('duel-s1');duelS2El=$('duel-s2');duelRoundEl=$('duel-round');DUEL_W=duelCanvas.width;DUEL_H=duelCanvas.height;DUEL_CELL=DUEL_W/DUEL_GRID}
function duelBuildMap(){duelWalls=[];for(var i=0;i<DUEL_GRID;i++){duelWalls.push({gx:i,gy:0,type:'solid'});duelWalls.push({gx:i,gy:DUEL_GRID-1,type:'solid'});duelWalls.push({gx:0,gy:i,type:'solid'});duelWalls.push({gx:DUEL_GRID-1,gy:i,type:'solid'})}var mid=5;for(var i=2;i<DUEL_GRID-2;i++){if(i===mid)continue;duelWalls.push({gx:i,gy:mid,type:'brick',hp:2})}for(var i=2;i<DUEL_GRID-2;i++){if(i===mid)continue;duelWalls.push({gx:mid,gy:i,type:'brick',hp:2})}duelWalls.push({gx:2,gy:2,type:'solid'});duelWalls.push({gx:DUEL_GRID-3,gy:2,type:'solid'});duelWalls.push({gx:2,gy:DUEL_GRID-3,type:'solid'});duelWalls.push({gx:DUEL_GRID-3,gy:DUEL_GRID-3,type:'solid'})}
function duelIsWall(gx,gy){for(var i=0;i<duelWalls.length;i++)if(duelWalls[i].gx===gx&&duelWalls[i].gy===gy)return duelWalls[i];return null}
function startDuel(){initDuel();duelWins=[0,0];duelRoundNum=0;duelS1El.textContent='0';duelS2El.textContent='0';duelRoundEl.textContent='0';duelNewRound();duelRun=true;duelLT=performance.now();if(duelFId)cancelAnimationFrame(duelFId);duelFId=requestAnimationFrame(duelLoop)}
function stopDuel(){duelRun=false;if(duelFId)cancelAnimationFrame(duelFId);duelFId=null}
function duelNewMatch(){haptic(20);duelWins=[0,0];duelRoundNum=0;duelS1El.textContent='0';duelS2El.textContent='0';duelRoundEl.textContent='0';duelNewRound()}
function duelNewRound(){duelBuildMap();duelRoundNum++;duelRoundEl.textContent=duelRoundNum;duelTanks=[{side:'p1',color:'#e91e63',hp:3,maxHp:3,gx:1,gy:1,dir:0,lastShot:0,canFire:true},{side:'p2',color:'#00e5ff',hp:3,maxHp:3,gx:DUEL_GRID-2,gy:DUEL_GRID-2,dir:0,lastShot:0,canFire:true}];duelBullets=[];duelParticles=[];duelActive=true;duelWinner=null;duelRT=0;haptic(15);toast('🔔 Раунд '+duelRoundNum,'i',1000)}
function duelControl(a){if(!duelRun||!duelActive)return;var side=null,cmd=null;if(a.indexOf('p1-')===0){side='p1';cmd=a.slice(3)}else if(a.indexOf('p2-')===0){side='p2';cmd=a.slice(3)}if(!side)return;var tank=null;for(var i=0;i<duelTanks.length;i++)if(duelTanks[i].side===side)tank=duelTanks[i];if(!tank)return;var now=performance.now();if(cmd==='left'||cmd==='right'||cmd==='up'||cmd==='down'){if(tank.lastMove&&now-tank.lastMove<120)return;tank.lastMove=now;var nx=tank.gx,ny=tank.gy;if(cmd==='left')nx--;else if(cmd==='right')nx++;else if(cmd==='up')ny--;else if(cmd==='down')ny++;if(duelIsWall(nx,ny)){haptic(5);return}var other=null;for(var i=0;i<duelTanks.length;i++)if(duelTanks[i].side!==side)other=duelTanks[i];if(other&&other.gx===nx&&other.gy===ny)return;tank.gx=nx;tank.gy=ny;tank.dir=cmd;haptic(4)}else if(cmd==='fire'){if(!tank.canFire)return;if(now-tank.lastShot<600)return;tank.lastShot=now;var vx=0,vy=0;if(tank.dir==='left')vx=-1;else if(tank.dir==='right')vx=1;else if(tank.dir==='up')vy=-1;else if(tank.dir==='down')vy=1;else{var other=null;for(var i=0;i<duelTanks.length;i++)if(duelTanks[i].side!==side)other=duelTanks[i];if(other){var dx=other.gx-tank.gx,dy=other.gy-tank.gy;if(Math.abs(dx)>Math.abs(dy))vx=dx>0?1:-1;else vy=dy>0?1:-1}else vx=1}duelBullets.push({x:tank.gx*DUEL_CELL+DUEL_CELL/2,y:tank.gy*DUEL_CELL+DUEL_CELL/2,vx:vx*4,vy:vy*4,owner:tank.side,color:tank.color,life:0});haptic(8)}}
function duelLoop(t){if(!duelRun)return;var dt=Math.min(40,t-duelLT);duelLT=t;if(duelActive)updateDuel(dt,t);drawDuel();duelFId=requestAnimationFrame(duelLoop)}
function updateDuel(dt,t){for(var i=duelBullets.length-1;i>=0;i--){var b=duelBullets[i];var steps=4,removed=false;for(var s=0;s<steps;s++){b.x+=b.vx*dt*0.06/steps*2;b.y+=b.vy*dt*0.06/steps*2;var gx=Math.floor(b.x/DUEL_CELL),gy=Math.floor(b.y/DUEL_CELL);var wall=duelIsWall(gx,gy);if(wall){if(wall.type==='brick'){wall.hp--;if(wall.hp<=0){var idx=duelWalls.indexOf(wall);if(idx>=0)duelWalls.splice(idx,1);haptic(20)}}else haptic(5);for(var k=0;k<6;k++)duelParticles.push({x:b.x,y:b.y,vx:(Math.random()-0.5)*4,vy:(Math.random()-0.5)*4,life:1,size:2,color:b.color});duelBullets.splice(i,1);removed=true;break}for(var j=0;j<duelTanks.length;j++){var tank=duelTanks[j];if(tank.side===b.owner)continue;var tx=tank.gx*DUEL_CELL+DUEL_CELL/2,ty=tank.gy*DUEL_CELL+DUEL_CELL/2;if(Math.abs(b.x-tx)<DUEL_CELL*0.4&&Math.abs(b.y-ty)<DUEL_CELL*0.4){tank.hp--;haptic(60);for(var k=0;k<15;k++)duelParticles.push({x:tx,y:ty,vx:(Math.random()-0.5)*8,vy:(Math.random()-0.5)*8,life:1,size:3,color:tank.color});duelBullets.splice(i,1);removed=true;if(tank.hp<=0)duelRoundEnd(tank.side==='p1'?'p2':'p1');break}}if(removed)break;if(b.x<0||b.x>DUEL_W||b.y<0||b.y>DUEL_H){duelBullets.splice(i,1);removed=true;break}}if(removed)continue;b.life+=dt;if(b.life>5000)duelBullets.splice(i,1)}for(var i=duelParticles.length-1;i>=0;i--){var p=duelParticles[i];p.x+=p.vx;p.y+=p.vy;p.life-=0.03;if(p.life<=0)duelParticles.splice(i,1)}if(duelWinner){duelRT+=dt;if(duelRT>1800)duelNewRound()}}
function duelRoundEnd(w){duelActive=false;duelWinner=w;haptic(80);if(w==='p1'){duelWins[0]++;duelS1El.textContent=duelWins[0];bump(duelS1El);toast('🏆 Игрок 1 побеждает!','s',1800)}else{duelWins[1]++;duelS2El.textContent=duelWins[1];bump(duelS2El);toast('🏆 Игрок 2 побеждает!','s',1800)}addCoins(5,false);if(duelWins[0]>=3||duelWins[1]>=3){var champ=duelWins[0]>=3?'🔴 Игрок 1':'🔵 Игрок 2';setTimeout(function(){toast('👑 '+champ+' выиграл матч!','r',2500);addCoins(20,false)},1800)}}
function drawDuel(){if(!duelCtx)return;var g=duelCtx.createLinearGradient(0,0,0,DUEL_H);g.addColorStop(0,'#0f0408');g.addColorStop(1,'#050202');duelCtx.fillStyle=g;duelCtx.fillRect(0,0,DUEL_W,DUEL_H);duelCtx.strokeStyle='rgba(255,255,255,0.03)';duelCtx.lineWidth=1;for(var i=0;i<=DUEL_GRID;i++){duelCtx.beginPath();duelCtx.moveTo(i*DUEL_CELL,0);duelCtx.lineTo(i*DUEL_CELL,DUEL_H);duelCtx.stroke();duelCtx.beginPath();duelCtx.moveTo(0,i*DUEL_CELL);duelCtx.lineTo(DUEL_W,i*DUEL_CELL);duelCtx.stroke()}for(var i=0;i<duelWalls.length;i++){var w=duelWalls[i],x=w.gx*DUEL_CELL,y=w.gy*DUEL_CELL;if(w.type==='solid'){duelCtx.fillStyle='#37474f';roundRect(duelCtx,x+1,y+1,DUEL_CELL-2,DUEL_CELL-2,3);duelCtx.fill()}else{duelCtx.fillStyle='#8d6e63';duelCtx.globalAlpha=0.5+(w.hp/2)*0.5;roundRect(duelCtx,x+1,y+1,DUEL_CELL-2,DUEL_CELL-2,3);duelCtx.fill();duelCtx.globalAlpha=1}}for(var i=0;i<duelTanks.length;i++){var tank=duelTanks[i],x=tank.gx*DUEL_CELL+DUEL_CELL/2,y=tank.gy*DUEL_CELL+DUEL_CELL/2;duelCtx.save();duelCtx.translate(x,y);var ang=0;if(tank.dir==='up')ang=-Math.PI/2;else if(tank.dir==='down')ang=Math.PI/2;else if(tank.dir==='left')ang=Math.PI;duelCtx.rotate(ang);var bs=DUEL_CELL*0.75;duelCtx.fillStyle=tank.color;duelCtx.shadowColor=tank.color;duelCtx.shadowBlur=12;roundRect(duelCtx,-bs/2,-bs/2,bs,bs,4);duelCtx.fill();duelCtx.shadowBlur=0;duelCtx.fillStyle='rgba(0,0,0,0.5)';duelCtx.fillRect(-bs/2,-bs/2,bs*0.2,bs);duelCtx.fillRect(bs/2-bs*0.2,-bs/2,bs*0.2,bs);duelCtx.fillStyle='#222';duelCtx.beginPath();duelCtx.arc(0,0,bs*0.22,0,Math.PI*2);duelCtx.fill();duelCtx.strokeStyle='#111';duelCtx.lineWidth=bs*0.14;duelCtx.lineCap='round';duelCtx.beginPath();duelCtx.moveTo(0,0);duelCtx.lineTo(bs*0.55,0);duelCtx.stroke();duelCtx.restore();var bw=DUEL_CELL*0.8;duelCtx.fillStyle='rgba(0,0,0,0.6)';duelCtx.fillRect(x-bw/2,y-DUEL_CELL*0.55,bw,4);duelCtx.fillStyle=tank.color;duelCtx.fillRect(x-bw/2,y-DUEL_CELL*0.55,bw*(tank.hp/tank.maxHp),4)}for(var i=0;i<duelBullets.length;i++){var b=duelBullets[i];duelCtx.fillStyle=b.color;duelCtx.shadowColor=b.color;duelCtx.shadowBlur=15;duelCtx.beginPath();duelCtx.arc(b.x,b.y,5,0,Math.PI*2);duelCtx.fill();duelCtx.shadowBlur=0}for(var i=0;i<duelParticles.length;i++){var p=duelParticles[i];duelCtx.globalAlpha=p.life;duelCtx.fillStyle=p.color;duelCtx.beginPath();duelCtx.arc(p.x,p.y,p.size,0,Math.PI*2);duelCtx.fill()}duelCtx.globalAlpha=1;if(duelWinner){duelCtx.fillStyle='rgba(0,0,0,0.7)';duelCtx.fillRect(0,DUEL_H/2-40,DUEL_W,80);duelCtx.fillStyle=duelWinner==='p1'?'#e91e63':'#00e5ff';duelCtx.font='bold 28px system-ui';duelCtx.textAlign='center';duelCtx.textBaseline='middle';duelCtx.fillText(duelWinner==='p1'?'🔴 П1 ПОБЕДИЛ':'🔵 П2 ПОБЕДИЛ',DUEL_W/2,DUEL_H/2)}}

var d2Canvas,d2Ctx,d2S1El,d2S2El,d2RoundEl,d2Btn,d2Side1,d2Side2,D2_W,D2_H,d2Run=false,d2FId=null,d2LT=0,d2State='idle',d2Round=0,d2Wins=[0,0],d2Start=0,d2Timeout=null,d2WinnerRound=null;
function initD2(){if(d2Canvas)return;d2Canvas=$('duel2Canvas');d2Ctx=d2Canvas.getContext('2d');d2S1El=$('duel2-s1');d2S2El=$('duel2-s2');d2RoundEl=$('duel2-round');d2Btn=$('duel2Btn');d2Side1=$('duel2-side1');d2Side2=$('duel2-side2');D2_W=d2Canvas.width;D2_H=d2Canvas.height}
function startDuel2(){initD2();d2Wins=[0,0];d2Round=0;d2S1El.textContent='0';d2S2El.textContent='0';d2RoundEl.textContent='0';d2State='idle';d2WinnerRound=null;d2Btn.textContent='НАЧАТЬ РАУНД';d2Side1.classList.remove('fl');d2Side2.classList.remove('fl');d2Side1.innerHTML='🔴 ИГРОК 1<br><small>ЖДИ...</small>';d2Side2.innerHTML='🔵 ИГРОК 2<br><small>ЖДИ...</small>';d2Run=true;d2LT=performance.now();if(d2FId)cancelAnimationFrame(d2FId);d2FId=requestAnimationFrame(d2Loop)}
function stopDuel2(){d2Run=false;clearTimeout(d2Timeout);if(d2FId)cancelAnimationFrame(d2FId);d2FId=null}
function duel2Start(){if(!d2Run)return;if(d2State==='match-end'){startDuel2();return}if(d2State==='waiting'||d2State==='ready')return;d2Round++;if(d2Round>5)d2Round=5;d2RoundEl.textContent=d2Round;d2State='waiting';d2Btn.textContent='ЖДИТЕ...';d2WinnerRound=null;d2Side1.classList.remove('fl');d2Side2.classList.remove('fl');d2Side1.innerHTML='🔴 ИГРОК 1<br><small>ЖДИ...</small>';d2Side2.innerHTML='🔵 ИГРОК 2<br><small>ЖДИ...</small>';haptic(15);var delay=1500+Math.random()*3000;d2Timeout=setTimeout(function(){if(d2State!=='waiting')return;d2State='ready';d2Start=performance.now();d2Btn.textContent='ЖМИ!';d2Side1.classList.add('fl');d2Side2.classList.add('fl');d2Side1.innerHTML='🔴 ЖМИ!';d2Side2.innerHTML='🔵 ЖМИ!';haptic(40)},delay)}
function duel2Tap(side){if(!d2Run)return;if(d2State==='waiting'){clearTimeout(d2Timeout);d2State='round-end';d2WinnerRound=side==='p1'?'p2':'p1';duel2EndRound();return}if(d2State!=='ready')return;var t=performance.now()-d2Start;d2State='round-end';d2WinnerRound=side;duel2EndRound(t)}
function duel2EndRound(time){if(d2WinnerRound==='p1'){d2Wins[0]++;d2S1El.textContent=d2Wins[0];bump(d2S1El);toast('🔴 П1 выиграл! '+(time?Math.round(time)+' мс':'П2 рано'),'s',1600);d2Side1.innerHTML='🔴 ПОБЕДА!';d2Side2.innerHTML='🔵 УВЫ'}else{d2Wins[1]++;d2S2El.textContent=d2Wins[1];bump(d2S2El);toast('🔵 П2 выиграл! '+(time?Math.round(time)+' мс':'П1 рано'),'s',1600);d2Side2.innerHTML='🔵 ПОБЕДА!';d2Side1.innerHTML='🔴 УВЫ'}d2Side1.classList.remove('fl');d2Side2.classList.remove('fl');haptic(30);if(d2Wins[0]>=3||d2Wins[1]>=3){d2State='match-end';d2Btn.textContent='ИГРАТЬ СНОВА';var champ=d2Wins[0]>=3?'🔴 Игрок 1':'🔵 Игрок 2';setTimeout(function(){toast('👑 '+champ+' выиграл матч!','r',2500)},1000)}else{d2State='idle';d2Btn.textContent='СЛЕДУЮЩИЙ РАУНД'}}
function d2Loop(t){if(!d2Run)return;d2LT=t;drawD2();d2FId=requestAnimationFrame(d2Loop)}
function drawD2(){if(!d2Ctx)return;d2Ctx.fillStyle='#04080f';d2Ctx.fillRect(0,0,D2_W,D2_H);d2Ctx.fillStyle=d2State==='ready'?'rgba(233,30,99,0.4)':'rgba(233,30,99,0.08)';d2Ctx.fillRect(0,0,D2_W/2,D2_H);d2Ctx.fillStyle=d2State==='ready'?'rgba(0,229,255,0.4)':'rgba(0,229,255,0.08)';d2Ctx.fillRect(D2_W/2,0,D2_W/2,D2_H);d2Ctx.strokeStyle='rgba(255,255,255,0.4)';d2Ctx.lineWidth=2;d2Ctx.beginPath();d2Ctx.moveTo(D2_W/2,0);d2Ctx.lineTo(D2_W/2,D2_H);d2Ctx.stroke();d2Ctx.fillStyle='#fff';d2Ctx.font='bold 26px system-ui';d2Ctx.textAlign='center';d2Ctx.textBaseline='middle';var txt='';if(d2State==='idle')txt='Нажмите «Начать раунд»';else if(d2State==='waiting')txt='⏳ ЖДИТЕ...';else if(d2State==='ready')txt='⚡ ЖМИ!';else if(d2State==='round-end')txt=d2WinnerRound==='p1'?'🔴 П1 выиграл':'🔵 П2 выиграл';else if(d2State==='match-end')txt=d2Wins[0]>=3?'🔴 П1 ЧЕМПИОН!':'🔵 П2 ЧЕМПИОН!';d2Ctx.fillText(txt,D2_W/2,D2_H/2);d2Ctx.font='bold 20px system-ui';d2Ctx.fillStyle='rgba(233,30,99,0.8)';d2Ctx.fillText('ИГРОК 1',D2_W/4,40);d2Ctx.fillStyle='rgba(0,229,255,0.8)';d2Ctx.fillText('ИГРОК 2',D2_W*3/4,40)}

var raceCanvas,raceCtx,raceScoreEl,raceBestEl,raceBestBox,RACE_W,RACE_H,RACE_LW;
var raceRun=false,raceFId=null,raceLT=0,racePLane=1,racePX,raceDir=0,raceScore=0,raceSpeed=1,raceCars=[],raceStars=[],racePaused=false,raceSpawnT=0,raceBoostT=0,raceCM=0,raceParticles=[];
var RACE_COLORS=['#e53935','#1e88e5','#43a047','#fb8c00','#8e24aa','#00acc1'];
function initRace(){if(raceCanvas)return;raceCanvas=$('raceCanvas');raceCtx=raceCanvas.getContext('2d');raceScoreEl=$('race-score');raceBestEl=$('race-best');raceBestBox=$('race-best-box');RACE_W=raceCanvas.width;RACE_H=raceCanvas.height;RACE_LW=RACE_W/3;racePX=RACE_LW*1.5}
function startRace(){initRace();racePLane=1;racePX=RACE_LW*1.5;raceDir=0;raceScore=0;raceSpeed=1;raceCars=[];raceStars=[];racePaused=false;raceSpawnT=0;raceBoostT=0;raceCM=0;raceParticles=[];raceScoreEl.textContent='0';raceBestEl.textContent=getBest('race_best');for(var i=0;i<20;i++)raceStars.push({x:RACE_LW/2+Math.random()*RACE_W,y:Math.random()*RACE_H,len:20+Math.random()*30});raceRun=true;raceLT=performance.now();if(raceFId)cancelAnimationFrame(raceFId);raceFId=requestAnimationFrame(raceLoop)}
function stopRace(){raceRun=false;if(raceFId)cancelAnimationFrame(raceFId);raceFId=null}
function raceControl(a){if(!raceRun)return;if(a==='left'){raceDir=-1;racePLane=Math.max(0,racePLane-1);haptic(6)}else if(a==='right'){raceDir=1;racePLane=Math.min(2,racePLane+1);haptic(6)}else if(a==='boost'){if(performance.now()<raceBoostT)return;raceBoostT=performance.now()+1000;haptic(20);toast('⚡ Ускорение!','s',800)}else if(a==='pause'){racePaused=!racePaused;haptic(10)}}
function raceLoop(t){if(!raceRun)return;var dt=Math.min(40,t-raceLT);raceLT=t;if(!racePaused)updateRace(dt,t);drawRace();raceFId=requestAnimationFrame(raceLoop)}
function updateRace(dt,t){raceSpeed=1+raceScore/200;var mul=performance.now()<raceBoostT?2:1,sp=raceSpeed*mul,tg=RACE_LW*racePLane+RACE_LW/2;racePX+=(tg-racePX)*0.25;raceDir=0;for(var i=0;i<raceStars.length;i++){var s=raceStars[i];s.y+=sp*6*dt*0.06;if(s.y>RACE_H){s.y=-s.len;s.x=RACE_LW/2+Math.random()*RACE_W}}if(t-raceSpawnT>1400-raceSpeed*100){raceSpawnT=t;var ln=Math.floor(Math.random()*3),cl=RACE_COLORS[Math.floor(Math.random()*RACE_COLORS.length)];raceCars.push({x:RACE_LW*ln+RACE_LW/2,y:-50,w:40,h:70,color:cl,lane:ln})}for(var j=raceCars.length-1;j>=0;j--){var c=raceCars[j];c.y+=sp*4.5*dt*0.06;if(c.y>RACE_H+60){raceCars.splice(j,1);raceScore+=10;raceScoreEl.textContent=raceScore;bump(raceScoreEl);var ms=Math.floor(raceScore/100);if(ms>raceCM){addCoins(ms-raceCM,false);raceCM=ms}if(tryUpdateRecord('race_best',raceScore,raceBestEl,raceBestBox))toast('🏆 Рекорд: '+raceScore,'r',1400)}}var py=RACE_H-90;for(var k=raceCars.length-1;k>=0;k--){var cc=raceCars[k];if(Math.abs(cc.x-racePX)<(cc.w+40)/2-8&&Math.abs(cc.y-py)<(cc.h+70)/2-8){raceCars.splice(k,1);gameOverRace();return}}for(var p=raceParticles.length-1;p>=0;p--){var pp=raceParticles[p];pp.x+=pp.vx;pp.y+=pp.vy;pp.life-=0.03;if(pp.life<=0)raceParticles.splice(p,1)}}
function gameOverRace(){stopRace();haptic(80);for(var k=0;k<20;k++)raceParticles.push({x:racePX,y:RACE_H-90,vx:(Math.random()-0.5)*8,vy:(Math.random()-0.5)*8,life:1,size:3,color:'#ff3d00'});toast('💥 Авария! Очки: '+raceScore,'i',1800);setTimeout(function(){if(currentScreen==='race-screen')startRace()},1300)}
function drawRace(){if(!raceCtx)return;var g=raceCtx.createLinearGradient(0,0,0,RACE_H);g.addColorStop(0,'#1a0a00');g.addColorStop(1,'#0a0500');raceCtx.fillStyle=g;raceCtx.fillRect(0,0,RACE_W,RACE_H);raceCtx.fillStyle='#2a1a10';raceCtx.fillRect(0,0,RACE_LW-10,RACE_H);raceCtx.fillRect(RACE_W-RACE_LW+10,0,RACE_LW-10,RACE_H);raceCtx.strokeStyle='rgba(255,255,255,0.6)';raceCtx.lineWidth=3;for(var i=1;i<3;i++){raceCtx.setLineDash([20,20]);raceCtx.beginPath();raceCtx.moveTo(RACE_LW*i,0);raceCtx.lineTo(RACE_LW*i,RACE_H);raceCtx.stroke()}raceCtx.setLineDash([]);for(var s=0;s<raceStars.length;s++){var st=raceStars[s];raceCtx.strokeStyle='rgba(255,255,255,0.4)';raceCtx.lineWidth=3;raceCtx.beginPath();raceCtx.moveTo(st.x,st.y);raceCtx.lineTo(st.x,st.y+st.len);raceCtx.stroke()}for(var c=0;c<raceCars.length;c++){var cc=raceCars[c];raceCtx.fillStyle=cc.color;raceCtx.shadowColor=cc.color;raceCtx.shadowBlur=10;roundRect(raceCtx,cc.x-cc.w/2,cc.y-cc.h/2,cc.w,cc.h,8);raceCtx.fill();raceCtx.shadowBlur=0;raceCtx.fillStyle='rgba(0,0,0,0.5)';roundRect(raceCtx,cc.x-cc.w/2+5,cc.y-cc.h/2+12,cc.w-10,cc.h*0.35,4);raceCtx.fill()}var py=RACE_H-90;raceCtx.fillStyle='#ffd54f';raceCtx.shadowColor='#ffd54f';raceCtx.shadowBlur=14;roundRect(raceCtx,racePX-20,py-35,40,70,8);raceCtx.fill();raceCtx.shadowBlur=0;raceCtx.fillStyle='rgba(0,0,0,0.5)';roundRect(raceCtx,racePX-14,py-22,28,25,4);raceCtx.fill();if(performance.now()<raceBoostT){raceCtx.fillStyle='#ff5722';raceCtx.shadowColor='#ff5722';raceCtx.shadowBlur=20;raceCtx.beginPath();raceCtx.moveTo(racePX-10,py+35);raceCtx.lineTo(racePX,py+35+20+Math.random()*15);raceCtx.lineTo(racePX+10,py+35);raceCtx.closePath();raceCtx.fill();raceCtx.shadowBlur=0}for(var p=0;p<raceParticles.length;p++){var pp=raceParticles[p];raceCtx.globalAlpha=pp.life;raceCtx.fillStyle=pp.color;raceCtx.beginPath();raceCtx.arc(pp.x,pp.y,pp.size,0,Math.PI*2);raceCtx.fill()}raceCtx.globalAlpha=1;raceCtx.fillStyle='rgba(255,255,255,0.7)';raceCtx.font='bold 14px system-ui';raceCtx.textAlign='left';raceCtx.fillText('🏎 '+raceSpeed.toFixed(1)+'x',10,25)}

var flappyCanvas,flappyCtx,flappyScoreEl,flappyBestEl,flappyBestBox,FLAPPY_W,FLAPPY_H;
var flappyRun=false,flappyFId=null,flappyLT=0,flappyBird={x:80,y:220,vy:0,r:12},flappyPipes=[],flappyScore=0,flappyState='waiting',flappyPaused=false,flappyLastPipe=0,flappyCM=0,flappyParticles=[];
var FG=0.35,FJ=-6.5,FPW=60,FGAP=140,FPS=2.2;
function initFlappy(){if(flappyCanvas)return;flappyCanvas=$('flappyCanvas');flappyCtx=flappyCanvas.getContext('2d');flappyScoreEl=$('flappy-score');flappyBestEl=$('flappy-best');flappyBestBox=$('flappy-best-box');FLAPPY_W=flappyCanvas.width;FLAPPY_H=flappyCanvas.height}
function startFlappy(){initFlappy();flappyBird={x:80,y:FLAPPY_H/2,vy:0,r:12};flappyPipes=[];flappyScore=0;flappyState='waiting';flappyPaused=false;flappyLastPipe=0;flappyCM=0;flappyParticles=[];flappyScoreEl.textContent='0';flappyBestEl.textContent=getBest('flappy_best');flappyRun=true;flappyLT=performance.now();if(flappyFId)cancelAnimationFrame(flappyFId);flappyFId=requestAnimationFrame(flappyLoop)}
function stopFlappy(){flappyRun=false;if(flappyFId)cancelAnimationFrame(flappyFId);flappyFId=null}
function flappyFlap(e){if(e)e.preventDefault();haptic(8);if(flappyState==='waiting'){flappyState='playing';flappyBird.vy=FJ;return}if(flappyState==='dead'){startFlappy();return}if(flappyState==='playing')flappyBird.vy=FJ}
function flappyLoop(t){if(!flappyRun)return;var dt=Math.min(40,t-flappyLT);flappyLT=t;if(!flappyPaused)updateFlappy(dt,t);drawFlappy();flappyFId=requestAnimationFrame(flappyLoop)}
function updateFlappy(dt,t){if(flappyState==='waiting'){flappyBird.y=FLAPPY_H/2+Math.sin(t/300)*8;return}if(flappyState==='dead'){flappyBird.vy+=FG*dt*0.06;flappyBird.y+=flappyBird.vy*dt*0.06;for(var i=flappyParticles.length-1;i>=0;i--){var p=flappyParticles[i];p.x+=p.vx;p.y+=p.vy;p.life-=0.03;if(p.life<=0)flappyParticles.splice(i,1)}return}flappyBird.vy+=FG*dt*0.06;flappyBird.y+=flappyBird.vy*dt*0.06;if(t-flappyLastPipe>1500){flappyLastPipe=t;var mt=60,mtx=FLAPPY_H-FGAP-60,th=mt+Math.random()*(mtx-mt);flappyPipes.push({x:FLAPPY_W,topH:th,bottomY:th+FGAP,passed:false})}for(var j=flappyPipes.length-1;j>=0;j--){var p=flappyPipes[j];p.x-=FPS*dt*0.06*1.5;if(!p.passed&&p.x+FPW<flappyBird.x){p.passed=true;flappyScore++;flappyScoreEl.textContent=flappyScore;bump(flappyScoreEl);haptic(15);var ms=Math.floor(flappyScore/5);if(ms>flappyCM){addCoins(ms-flappyCM,false);flappyCM=ms}if(tryUpdateRecord('flappy_best',flappyScore,flappyBestEl,flappyBestBox))toast('🏆 Рекорд: '+flappyScore,'r',1400)}if(p.x<-FPW)flappyPipes.splice(j,1)}for(var k=0;k<flappyPipes.length;k++){var pp=flappyPipes[k];if(flappyBird.x+flappyBird.r>pp.x&&flappyBird.x-flappyBird.r<pp.x+FPW){if(flappyBird.y-flappyBird.r<pp.topH||flappyBird.y+flappyBird.r>pp.bottomY){flappyGameOver();return}}}if(flappyBird.y-flappyBird.r<0){flappyBird.y=flappyBird.r;flappyBird.vy=0}if(flappyBird.y+flappyBird.r>FLAPPY_H){flappyGameOver();return}}
function flappyGameOver(){flappyState='dead';haptic(80);for(var k=0;k<15;k++)flappyParticles.push({x:flappyBird.x,y:flappyBird.y,vx:(Math.random()-0.5)*6,vy:(Math.random()-0.5)*6-2,life:1,size:3,color:'#ffc400'});toast('💥 Очки: '+flappyScore,'i',2000)}
function drawFlappy(){if(!flappyCtx)return;var g=flappyCtx.createLinearGradient(0,0,0,FLAPPY_H);g.addColorStop(0,'#041a2e');g.addColorStop(0.6,'#0a2540');g.addColorStop(1,'#1a3a5e');flappyCtx.fillStyle=g;flappyCtx.fillRect(0,0,FLAPPY_W,FLAPPY_H);for(var i=0;i<flappyPipes.length;i++){var p=flappyPipes[i];flappyCtx.fillStyle='#4caf50';flappyCtx.shadowColor='#4caf50';flappyCtx.shadowBlur=10;roundRect(flappyCtx,p.x,0,FPW,p.topH,6);flappyCtx.fill();roundRect(flappyCtx,p.x,p.bottomY,FPW,FLAPPY_H-p.bottomY,6);flappyCtx.fill();flappyCtx.shadowBlur=0;flappyCtx.fillStyle='#388e3c';roundRect(flappyCtx,p.x-4,p.topH-20,FPW+8,20,4);flappyCtx.fill();roundRect(flappyCtx,p.x-4,p.bottomY,FPW+8,20,4);flappyCtx.fill()}flappyCtx.fillStyle='#3e2723';flappyCtx.fillRect(0,FLAPPY_H-30,FLAPPY_W,30);flappyCtx.save();flappyCtx.translate(flappyBird.x,flappyBird.y);var ang=flappyState==='dead'?Math.PI/2:Math.atan2(flappyBird.vy,10)*0.5;flappyCtx.rotate(ang);flappyCtx.fillStyle='#ffc400';flappyCtx.shadowColor='#ffc400';flappyCtx.shadowBlur=12;flappyCtx.beginPath();flappyCtx.ellipse(0,0,flappyBird.r+4,flappyBird.r,0,0,Math.PI*2);flappyCtx.fill();flappyCtx.shadowBlur=0;flappyCtx.fillStyle='#ff9800';flappyCtx.beginPath();flappyCtx.ellipse(-2,2,7,5,-0.3,0,Math.PI*2);flappyCtx.fill();flappyCtx.fillStyle='#fff';flappyCtx.beginPath();flappyCtx.arc(5,-3,4,0,Math.PI*2);flappyCtx.fill();flappyCtx.fillStyle='#000';flappyCtx.beginPath();flappyCtx.arc(6,-3,2,0,Math.PI*2);flappyCtx.fill();flappyCtx.fillStyle='#ff5722';flappyCtx.beginPath();flappyCtx.moveTo(11,-1);flappyCtx.lineTo(17,2);flappyCtx.lineTo(11,5);flappyCtx.closePath();flappyCtx.fill();flappyCtx.restore();for(var pp=0;pp<flappyParticles.length;pp++){var pt=flappyParticles[pp];flappyCtx.globalAlpha=pt.life;flappyCtx.fillStyle=pt.color;flappyCtx.beginPath();flappyCtx.arc(pt.x,pt.y,pt.size,0,Math.PI*2);flappyCtx.fill()}flappyCtx.globalAlpha=1;if(flappyState==='waiting'){flappyCtx.fillStyle='rgba(255,255,255,0.85)';flappyCtx.font='bold 18px system-ui';flappyCtx.textAlign='center';flappyCtx.textBaseline='middle';flappyCtx.fillText('НАЖМИТЕ «ЛЕТЕТЬ»',FLAPPY_W/2,FLAPPY_H/2-60)}if(flappyState==='dead'){flappyCtx.fillStyle='rgba(0,0,0,0.5)';flappyCtx.fillRect(0,0,FLAPPY_W,FLAPPY_H);flappyCtx.fillStyle='#fff';flappyCtx.font='bold 32px system-ui';flappyCtx.textAlign='center';flappyCtx.textBaseline='middle';flappyCtx.fillText('ИГРА ОКОНЧЕНА',FLAPPY_W/2,FLAPPY_H/2-30);flappyCtx.font='bold 20px system-ui';flappyCtx.fillStyle='#ffd54f';flappyCtx.fillText('Очки: '+flappyScore,FLAPPY_W/2,FLAPPY_H/2+10)}flappyCtx.fillStyle='#fff';flappyCtx.font='bold 32px system-ui';flappyCtx.textAlign='center';flappyCtx.textBaseline='top';flappyCtx.shadowColor='#000';flappyCtx.shadowBlur=6;flappyCtx.fillText(flappyScore,FLAPPY_W/2,20);flappyCtx.shadowBlur=0}

var rpgCanvas,rpgCtx,rpgHpEl,rpgLevelEl,rpgScoreEl,rpgRun=false,rpgFId=null,rpgLT=0,rpgSnake,rpgFood,rpgEnemies=[],rpgDx=1,rpgDy=0,rpgScore=0,rpgHp=5,rpgLevel=1,rpgTiles=24,rpgGrid,rpgInterval,rpgFoodEaten=0,rpgParticles=[];
function initRpg(){if(rpgCanvas)return;rpgCanvas=$('rpgSnakeCanvas');rpgCtx=rpgCanvas.getContext('2d');rpgHpEl=$('rpgSnake-hp');rpgLevelEl=$('rpgSnake-level');rpgScoreEl=$('rpgSnake-score');rpgGrid=rpgCanvas.width/rpgTiles}
function enterRpgSnake(){initRpg();var s=loadP('rpgSnake');if(s)askResume('rpgSnake',function(){resumeRpg(s)},function(){startRpgSnake()});else startRpgSnake()}
function saveRpgSnakeState(){if(!rpgRun)return;saveP('rpgSnake',{snake:rpgSnake.map(function(p){return{x:p.x,y:p.y}}),food:{x:rpgFood.x,y:rpgFood.y},enemies:rpgEnemies.map(function(e){return{x:e.x,y:e.y,hp:e.hp}}),dx:rpgDx,dy:rpgDy,score:rpgScore,hp:rpgHp,level:rpgLevel,foodEaten:rpgFoodEaten})}
function resumeRpg(s){initRpg();rpgSnake=s.snake.map(function(p){return{x:p.x,y:p.y}});rpgFood={x:s.food.x,y:s.food.y};rpgEnemies=s.enemies.map(function(e){return{x:e.x,y:e.y,hp:e.hp}});rpgDx=s.dx;rpgDy=s.dy;rpgScore=s.score;rpgHp=s.hp;rpgLevel=s.level;rpgFoodEaten=s.foodEaten;rpgHpEl.textContent=rpgHp;rpgLevelEl.textContent=rpgLevel;rpgScoreEl.textContent=rpgScore;clearInterval(rpgInterval);rpgRun=true;rpgInterval=setInterval(updateRpg,150);drawRpg();toast('💾 Уровень '+rpgLevel,'sv',1500)}
function startRpgSnake(){initRpg();rpgSnake=[{x:10,y:10},{x:9,y:10},{x:8,y:10}];rpgFood={x:15,y:10};rpgEnemies=[];rpgDx=1;rpgDy=0;rpgScore=0;rpgHp=5;rpgLevel=1;rpgFoodEaten=0;rpgParticles=[];rpgHpEl.textContent=rpgHp;rpgLevelEl.textContent=rpgLevel;rpgScoreEl.textContent=rpgScore;spawnRpgFood();spawnRpgEnemy();clearInterval(rpgInterval);rpgRun=true;rpgInterval=setInterval(updateRpg,150);drawRpg()}
function stopRpgSnake(){saveRpgSnakeState();clearInterval(rpgInterval);rpgRun=false}
function updateRpg(){if(!rpgRun)return;var h={x:rpgSnake[0].x+rpgDx,y:rpgSnake[0].y+rpgDy};if(h.x<0||h.x>=rpgTiles||h.y<0||h.y>=rpgTiles){rpgHp--;rpgHpEl.textContent=rpgHp;haptic(60);if(rpgHp<=0){gameOverRpg();return}h.x=rpgSnake[0].x;h.y=rpgSnake[0].y}var hitSelf=false;for(var i=1;i<rpgSnake.length;i++)if(rpgSnake[i].x===h.x&&rpgSnake[i].y===h.y){hitSelf=true;break}if(hitSelf){rpgHp--;rpgHpEl.textContent=rpgHp;haptic(60);if(rpgHp<=0){gameOverRpg();return}}else{rpgSnake.unshift(h);var hitEnemy=false;for(var i=rpgEnemies.length-1;i>=0;i--){if(rpgEnemies[i].x===h.x&&rpgEnemies[i].y===h.y){rpgEnemies[i].hp--;haptic(40);for(var k=0;k<8;k++)rpgParticles.push({x:h.x*rpgGrid+rpgGrid/2,y:h.y*rpgGrid+rpgGrid/2,vx:(Math.random()-0.5)*4,vy:(Math.random()-0.5)*4,life:1,size:2,color:'#ff5722'});if(rpgEnemies[i].hp<=0){rpgEnemies.splice(i,1);rpgScore+=50;rpgScoreEl.textContent=rpgScore;addCoins(3,false);toast('⚔ Враг повержен! +50','s',900);if(rpgEnemies.length<2+Math.floor(rpgLevel/2))spawnRpgEnemy()}hitEnemy=true;break}}if(h.x===rpgFood.x&&h.y===rpgFood.y){rpgFoodEaten++;rpgScore+=10;rpgScoreEl.textContent=rpgScore;bump(rpgScoreEl);haptic(20);addCoins(1,false);if(rpgFoodEaten%5===0){rpgLevel++;rpgLevelEl.textContent=rpgLevel;toast('⬆ Уровень '+rpgLevel+'!','s',1500);spawnRpgEnemy();addCoins(10,false)}spawnRpgFood()}else if(!hitEnemy)rpgSnake.pop();drawRpg()}}
function spawnRpgFood(){do{rpgFood.x=Math.floor(Math.random()*rpgTiles);rpgFood.y=Math.floor(Math.random()*rpgTiles)}while(rpgSnake.some(function(p){return p.x===rpgFood.x&&p.y===rpgFood.y})||rpgEnemies.some(function(e){return e.x===rpgFood.x&&e.y===rpgFood.y}))}
function spawnRpgEnemy(){var x,y,guard=0;do{x=Math.floor(Math.random()*rpgTiles);y=Math.floor(Math.random()*rpgTiles);guard++}while(guard<50&&(rpgSnake.some(function(p){return Math.abs(p.x-x)<3&&Math.abs(p.y-y)<3})||rpgEnemies.some(function(e){return e.x===x&&e.y===y})));rpgEnemies.push({x:x,y:y,hp:1+Math.floor(rpgLevel/3)})}
function rpgSnakeDir(nx,ny){if(!rpgRun)return;if(nx===-rpgDx&&rpgDx!==0)return;if(ny===-rpgDy&&rpgDy!==0)return;rpgDx=nx;rpgDy=ny;haptic(6)}
function gameOverRpg(){rpgRun=false;clearInterval(rpgInterval);clearP('rpgSnake');haptic(80);toast('💀 Игра окончена! Уровень '+rpgLevel+', очки '+rpgScore,'i',2500);setTimeout(function(){if(currentScreen==='rpgSnake-screen')startRpgSnake()},1500)}
function drawRpg(){if(!rpgCtx)return;rpgCtx.fillStyle='#041004';rpgCtx.fillRect(0,0,rpgCanvas.width,rpgCanvas.height);rpgCtx.strokeStyle='rgba(139,195,74,0.08)';rpgCtx.lineWidth=1;for(var i=1;i<rpgTiles;i++){rpgCtx.beginPath();rpgCtx.moveTo(i*rpgGrid,0);rpgCtx.lineTo(i*rpgGrid,rpgCanvas.height);rpgCtx.stroke();rpgCtx.beginPath();rpgCtx.moveTo(0,i*rpgGrid);rpgCtx.lineTo(rpgCanvas.width,i*rpgGrid);rpgCtx.stroke()}var t=performance.now()/300,p=1+Math.sin(t)*0.15,fx=rpgFood.x*rpgGrid+rpgGrid/2,fy=rpgFood.y*rpgGrid+rpgGrid/2,fr=(rpgGrid/2-2)*p,g=rpgCtx.createRadialGradient(fx,fy,0,fx,fy,fr*1.6);g.addColorStop(0,'#a5d6a7');g.addColorStop(1,'rgba(76,175,80,0)');rpgCtx.fillStyle=g;rpgCtx.beginPath();rpgCtx.arc(fx,fy,fr*1.6,0,Math.PI*2);rpgCtx.fill();rpgCtx.fillStyle='#66bb6a';rpgCtx.beginPath();rpgCtx.arc(fx,fy,fr,0,Math.PI*2);rpgCtx.fill();for(var i=0;i<rpgEnemies.length;i++){var e=rpgEnemies[i],ex=e.x*rpgGrid+rpgGrid/2,ey=e.y*rpgGrid+rpgGrid/2;rpgCtx.fillStyle=e.hp>1?'#ff1744':'#ff5252';rpgCtx.shadowColor='#ff5252';rpgCtx.shadowBlur=8;rpgCtx.beginPath();rpgCtx.arc(ex,ey,rpgGrid/2-2,0,Math.PI*2);rpgCtx.fill();rpgCtx.shadowBlur=0;rpgCtx.fillStyle='#fff';rpgCtx.font='bold '+(rpgGrid-8)+'px system-ui';rpgCtx.textAlign='center';rpgCtx.textBaseline='middle';rpgCtx.fillText('👹',ex,ey)}for(var j=0;j<rpgSnake.length;j++){var pt=rpgSnake[j],x=pt.x*rpgGrid,y=pt.y*rpgGrid,hd=j===0,pd=hd?1:2;rpgCtx.fillStyle=hd?'#dcedc8':'hsl(88,50%,'+(55-Math.min(j*1.2,25))+'%)';roundRect(rpgCtx,x+pd,y+pd,rpgGrid-pd*2,rpgGrid-pd*2,4);rpgCtx.fill()}for(var k=0;k<rpgParticles.length;k++){var pp=rpgParticles[k];pp.x+=pp.vx;pp.y+=pp.vy;pp.life-=0.03;rpgCtx.globalAlpha=pp.life;rpgCtx.fillStyle=pp.color;rpgCtx.beginPath();rpgCtx.arc(pp.x,pp.y,pp.size,0,Math.PI*2);rpgCtx.fill()}rpgCtx.globalAlpha=1}

var glCanvas,glCtx,glHpEl,glWaveEl,glBestEl,glBestBox;
var glRun=false,glFId=null,glLT=0,glPlayer={x:180,y:300,hp:100,maxHp:100,blocking:false,invul:0},glEnemies=[],glProjectiles=[],glParticles=[],glWave=0,glWaveActive=false,glSpawnT=0,glWaveCount=0,glAttacks=[],glBest=0,glKeys={left:false,right:false};
function initGl(){if(glCanvas)return;glCanvas=$('gladiatorCanvas');glCtx=glCanvas.getContext('2d');glHpEl=$('gl-hp');glWaveEl=$('gl-wave');glBestEl=$('gl-best');glBestBox=$('gl-best-box')}
function enterGladiator(){initGl();var s=loadP('gladiator');if(s)askResume('gladiator',function(){resumeGl(s)},function(){startGladiator()});else startGladiator()}
function saveGladiatorState(){if(!glRun)return;saveP('gladiator',{player:{x:glPlayer.x,y:glPlayer.y,hp:glPlayer.hp,maxHp:glPlayer.maxHp},wave:glWave,enemies:glEnemies.map(function(e){return{x:e.x,y:e.y,hp:e.hp,maxHp:e.maxHp,type:e.type}}),best:glBest})}
function resumeGl(s){initGl();glPlayer={x:s.player.x,y:s.player.y,hp:s.player.hp,maxHp:s.player.maxHp,blocking:false,invul:0};glWave=s.wave;glEnemies=s.enemies.map(function(e){return{x:e.x,y:e.y,hp:e.hp,maxHp:e.maxHp,type:e.type,attackCD:1000}});glBest=s.best||getBest('gl_best');glProjectiles=[];glParticles=[];glAttacks=[];glWaveActive=false;glSpawnT=0;glWaveCount=0;glHpEl.textContent=Math.max(0,Math.round(glPlayer.hp));glWaveEl.textContent=glWave;glBestEl.textContent=glBest;glRun=true;glLT=performance.now();if(glFId)cancelAnimationFrame(glFId);glFId=requestAnimationFrame(glLoop);toast('💾 Волна '+glWave,'sv',1500)}
function startGladiator(){initGl();glPlayer={x:180,y:300,hp:100,maxHp:100,blocking:false,invul:0};glEnemies=[];glProjectiles=[];glParticles=[];glWave=0;glWaveActive=false;glSpawnT=0;glWaveCount=0;glAttacks=[];glBest=getBest('gl_best');glHpEl.textContent='100';glWaveEl.textContent='0';glBestEl.textContent=glBest;spawnGlWave();glRun=true;glLT=performance.now();if(glFId)cancelAnimationFrame(glFId);glFId=requestAnimationFrame(glLoop)}
function stopGladiator(){saveGladiatorState();glRun=false;if(glFId)cancelAnimationFrame(glFId);glFId=null}
function spawnGlWave(){glWave++;glWaveEl.textContent=glWave;glWaveActive=true;glWaveCount=3+glWave*2;glSpawnT=0}
function glControl(a){if(!glRun)return;if(a==='left'){glKeys.left=true;glPlayer.x=Math.max(30,glPlayer.x-40);haptic(6)}else if(a==='right'){glKeys.right=true;glPlayer.x=Math.min(330,glPlayer.x+40);haptic(6)}else if(a==='attack'){glAttack();haptic(10)}else if(a==='block'){glPlayer.blocking=!glPlayer.blocking;haptic(10);toast(glPlayer.blocking?'🛡 Блок':'Открыт','i',700)}}
function glAttack(){var now=performance.now();if(glPlayer.lastAttack&&now-glPlayer.lastAttack<300)return;glPlayer.lastAttack=now;glAttacks.push({x:glPlayer.x,y:glPlayer.y-30,life:0.3});for(var i=glEnemies.length-1;i>=0;i--){var e=glEnemies[i];if(Math.abs(e.x-glPlayer.x)<50&&Math.abs(e.y-glPlayer.y)<70){e.hp-=20;haptic(30);for(var k=0;k<6;k++)glParticles.push({x:e.x,y:e.y,vx:(Math.random()-0.5)*4,vy:(Math.random()-0.5)*4,life:1,size:2,color:'#ffeb3b'});if(e.hp<=0){glEnemies.splice(i,1);addCoins(2,false);glParticles.push({x:e.x,y:e.y,vx:0,vy:0,life:1,size:15,color:'#ff5252'});toast('⚔ +'+e.points,'s',700)}}}}
function glLoop(t){if(!glRun)return;var dt=Math.min(40,t-glLT);glLT=t;updateGl(dt,t);drawGl();glFId=requestAnimationFrame(glLoop)}
function updateGl(dt,t){if(glWaveActive){glSpawnT-=dt;if(glWaveCount>0&&glSpawnT<=0){glSpawnT=900;glWaveCount--;var x=40+Math.random()*280;glEnemies.push({x:x,y:-40,hp:20+glWave*8,maxHp:20+glWave*8,type:glWave%3===0?'fast':'normal',attackCD:1000,vy:0.5+glWave*0.05,points:20+glWave*3})}}for(var i=glEnemies.length-1;i>=0;i--){var e=glEnemies[i];e.y+=e.vy*dt*0.06;if(e.y>60){e.attackCD-=dt;if(e.attackCD<=0){e.attackCD=1500;if(!glPlayer.blocking&&performance.now()>glPlayer.invul){glPlayer.hp-=5+glWave;glPlayer.invul=performance.now()+500;haptic(60);glHpEl.textContent=Math.max(0,Math.round(glPlayer.hp));if(glPlayer.hp<=0){gameOverGl();return}}}}if(e.y>glCanvas.height+40)glEnemies.splice(i,1)}for(var i=glProjectiles.length-1;i>=0;i--){var p=glProjectiles[i];p.x+=p.vx*dt*0.06;p.y+=p.vy*dt*0.06;p.life-=dt;if(p.life<=0||p.y<-20||p.y>glCanvas.height+20)glProjectiles.splice(i,1)}for(var i=glParticles.length-1;i>=0;i--){var p2=glParticles[i];p2.x+=p2.vx;p2.y+=p2.vy;p2.life-=0.03;if(p2.life<=0)glParticles.splice(i,1)}for(var i=glAttacks.length-1;i>=0;i--){glAttacks[i].life-=dt;if(glAttacks[i].life<=0)glAttacks.splice(i,1)}if(glPlayer.invul>0&&performance.now()>glPlayer.invul)glPlayer.invul=0;if(glWaveActive&&glWaveCount===0&&glEnemies.length===0){glWaveActive=false;glPlayer.hp=Math.min(glPlayer.maxHp,glPlayer.hp+20);glHpEl.textContent=Math.round(glPlayer.hp);bump(glHpEl);addCoins(10,false);if(glWave>glBest){glBest=glWave;localStorage.setItem('gl_best',glBest);glBestEl.textContent=glBest;bump(glBestEl)}toast('🎉 Волна '+glWave+' пройдена! +10🪙','s',1800);setTimeout(function(){if(glRun)spawnGlWave()},1500)}}
function gameOverGl(){glRun=false;if(glFId)cancelAnimationFrame(glFId);glFId=null;clearP('gladiator');toast('💀 Гладиатор пал! Волна: '+glWave,'i',2500);setTimeout(function(){if(currentScreen==='gladiator-screen')startGladiator()},1500)}
function drawGl(){if(!glCtx)return;var g=glCtx.createLinearGradient(0,0,0,glCanvas.height);g.addColorStop(0,'#140404');g.addColorStop(1,'#050101');glCtx.fillStyle=g;glCtx.fillRect(0,0,glCanvas.width,glCanvas.height);glCtx.fillStyle='rgba(211,47,47,0.1)';for(var i=0;i<6;i++){glCtx.fillRect(0,i*70,glCanvas.width,2)}for(var i=0;i<glEnemies.length;i++){var e=glEnemies[i];glCtx.fillStyle=e.type==='fast'?'#ff5252':'#d32f2f';glCtx.shadowColor='#d32f2f';glCtx.shadowBlur=10;roundRect(glCtx,e.x-15,e.y-15,30,30,6);glCtx.fill();glCtx.shadowBlur=0;glCtx.fillStyle='#fff';glCtx.font='bold 20px system-ui';glCtx.textAlign='center';glCtx.textBaseline='middle';glCtx.fillText('👹',e.x,e.y);var hpp=e.hp/e.maxHp;glCtx.fillStyle='rgba(0,0,0,0.5)';glCtx.fillRect(e.x-16,e.y-24,32,4);glCtx.fillStyle=hpp>0.5?'#4caf50':'#f44336';glCtx.fillRect(e.x-16,e.y-24,32*hpp,4)}glCtx.fillStyle=glPlayer.invul>0?'rgba(255,235,59,0.5)':(glPlayer.blocking?'#1976d2':'#ffeb3b');glCtx.shadowColor=glCtx.fillStyle;glCtx.shadowBlur=14;roundRect(glCtx,glPlayer.x-18,glPlayer.y-22,36,44,6);glCtx.fill();glCtx.shadowBlur=0;glCtx.fillStyle='#fff';glCtx.font='bold 24px system-ui';glCtx.textAlign='center';glCtx.textBaseline='middle';glCtx.fillText(glPlayer.blocking?'🛡':'⚔',glPlayer.x,glPlayer.y);for(var i=0;i<glAttacks.length;i++){var a=glAttacks[i];glCtx.strokeStyle='rgba(255,235,59,'+a.life*3+')';glCtx.lineWidth=4;glCtx.beginPath();glCtx.arc(a.x,a.y,40,Math.PI,Math.PI*2);glCtx.stroke()}for(var i=0;i<glParticles.length;i++){var p=glParticles[i];glCtx.globalAlpha=p.life;glCtx.fillStyle=p.color;glCtx.beginPath();glCtx.arc(p.x,p.y,p.size,0,Math.PI*2);glCtx.fill()}glCtx.globalAlpha=1;glCtx.fillStyle='#fff';glCtx.font='bold 14px system-ui';glCtx.textAlign='left';glCtx.textBaseline='top';glCtx.fillText('Волна '+glWave+(glWaveActive?' · Врагов: '+(glEnemies.length+glWaveCount):''),8,25)}

var pingCanvas,pingCtx,pingS1El,pingS2El,pingBestBox,PING_W,PING_H;
var pingRun=false,pingFId=null,pingLT=0,pingP1={x:20,y:200,h:80,vy:0},pingP2={x:340,y:200,h:80,vy:0},pingBall={x:180,y:240,vx:0,vy:0,r:8},pingS1=0,pingS2=0,pingP1Dir=0,pingP2Dir=0,pingParticles=[],pingScore=0,pingServing='p1';
function initPing(){if(pingCanvas)return;pingCanvas=$('pingCanvas');pingCtx=pingCanvas.getContext('2d');pingS1El=$('ping-s1');pingS2El=$('ping-s2');pingBestBox=$('ping-best-box');PING_W=pingCanvas.width;PING_H=pingCanvas.height}
function startPing(){initPing();pingP1={x:20,y:PING_H/2-40,h:80,vy:0};pingP2={x:PING_W-20,y:PING_H/2-40,h:80,vy:0};pingS1=0;pingS2=0;pingS1El.textContent='0';pingS2El.textContent='0';resetPingBall('p1');pingP1Dir=0;pingP2Dir=0;pingParticles=[];pingRun=true;pingLT=performance.now();if(pingFId)cancelAnimationFrame(pingFId);pingFId=requestAnimationFrame(pingLoop)}
function stopPing(){pingRun=false;if(pingFId)cancelAnimationFrame(pingFId);pingFId=null}
function resetPingBall(server){pingBall.x=PING_W/2;pingBall.y=PING_H/2;pingBall.vx=server==='p1'?4:-4;pingBall.vy=(Math.random()-0.5)*4;pingServing=server}
function pingControl(a){if(!pingRun)return;if(a==='p1-up'){pingP1Dir=-1;haptic(4)}else if(a==='p1-down'){pingP1Dir=1;haptic(4)}else if(a==='p1-stop')pingP1Dir=0;else if(a==='p2-up'){pingP2Dir=-1;haptic(4)}else if(a==='p2-down'){pingP2Dir=1;haptic(4)}else if(a==='p2-stop')pingP2Dir=0}
function pingLoop(t){if(!pingRun)return;var dt=Math.min(40,t-pingLT);pingLT=t;updatePing(dt);drawPing();pingFId=requestAnimationFrame(pingLoop)}
function updatePing(dt){pingP1.y+=pingP1Dir*0.5*dt;pingP2.y+=pingP2Dir*0.5*dt;pingP1.y=Math.max(0,Math.min(PING_H-pingP1.h,pingP1.y));pingP2.y=Math.max(0,Math.min(PING_H-pingP2.h,pingP2.y));pingBall.x+=pingBall.vx*dt*0.06;pingBall.y+=pingBall.vy*dt*0.06;if(pingBall.y-pingBall.r<0){pingBall.y=pingBall.r;pingBall.vy=Math.abs(pingBall.vy)}if(pingBall.y+pingBall.r>PING_H){pingBall.y=PING_H-pingBall.r;pingBall.vy=-Math.abs(pingBall.vy)}if(pingBall.x-pingBall.r<pingP1.x+8&&pingBall.x+pingBall.r>pingP1.x&&pingBall.y>pingP1.y&&pingBall.y<pingP1.y+pingP1.h&&pingBall.vx<0){pingBall.x=pingP1.x+8+pingBall.r;pingBall.vx=Math.abs(pingBall.vx)*1.05;var rel=(pingBall.y-(pingP1.y+pingP1.h/2))/(pingP1.h/2);pingBall.vy=rel*5;haptic(15)}if(pingBall.x+pingBall.r>pingP2.x-8&&pingBall.x-pingBall.r<pingP2.x+8&&pingBall.y>pingP2.y&&pingBall.y<pingP2.y+pingP2.h&&pingBall.vx>0){pingBall.x=pingP2.x-8-pingBall.r;pingBall.vx=-Math.abs(pingBall.vx)*1.05;var rel2=(pingBall.y-(pingP2.y+pingP2.h/2))/(pingP2.h/2);pingBall.vy=rel2*5;haptic(15)}if(pingBall.x<0){pingS2++;pingS2El.textContent=pingS2;bump(pingS2El);haptic(60);checkPingWin('p2')}else if(pingBall.x>PING_W){pingS1++;pingS1El.textContent=pingS1;bump(pingS1El);haptic(60);checkPingWin('p1')}for(var i=pingParticles.length-1;i>=0;i--){var p=pingParticles[i];p.x+=p.vx;p.y+=p.vy;p.life-=0.03;if(p.life<=0)pingParticles.splice(i,1)}}
function checkPingWin(w){if(pingS1>=7||pingS2>=7){pingRun=false;if(pingFId)cancelAnimationFrame(pingFId);pingFId=null;toast('🏆 '+(w==='p1'?'🟦 Игрок 1':'🟧 Игрок 2')+' выиграл! '+pingS1+':'+pingS2,'r',3000);addCoins(20,false);setTimeout(function(){if(currentScreen==='ping-screen')startPing()},2000)}else{setTimeout(function(){if(pingRun)resetPingBall(w)},500)}}
function pingNewMatch(){haptic(20);startPing()}
function drawPing(){if(!pingCtx)return;pingCtx.fillStyle='#041016';pingCtx.fillRect(0,0,PING_W,PING_H);pingCtx.strokeStyle='rgba(38,198,218,0.15)';pingCtx.lineWidth=2;pingCtx.setLineDash([10,15]);pingCtx.beginPath();pingCtx.moveTo(PING_W/2,0);pingCtx.lineTo(PING_W/2,PING_H);pingCtx.stroke();pingCtx.setLineDash([]);pingCtx.fillStyle='#26c6da';pingCtx.shadowColor='#26c6da';pingCtx.shadowBlur=14;roundRect(pingCtx,pingP1.x-5,pingP1.y,10,pingP1.h,4);pingCtx.fill();pingCtx.shadowBlur=0;pingCtx.fillStyle='#ef6c00';pingCtx.shadowColor='#ef6c00';pingCtx.shadowBlur=14;roundRect(pingCtx,pingP2.x-5,pingP2.y,10,pingP2.h,4);pingCtx.fill();pingCtx.shadowBlur=0;pingCtx.fillStyle='#fff';pingCtx.shadowColor='#fff';pingCtx.shadowBlur=16;pingCtx.beginPath();pingCtx.arc(pingBall.x,pingBall.y,pingBall.r,0,Math.PI*2);pingCtx.fill();pingCtx.shadowBlur=0;pingCtx.font='bold 48px system-ui';pingCtx.textAlign='center';pingCtx.textBaseline='top';pingCtx.fillStyle='rgba(38,198,218,0.3)';pingCtx.fillText(pingS1,PING_W/4,20);pingCtx.fillStyle='rgba(239,108,0,0.3)';pingCtx.fillText(pingS2,PING_W*3/4,20);for(var i=0;i<pingParticles.length;i++){var p=pingParticles[i];pingCtx.globalAlpha=p.life;pingCtx.fillStyle=p.color;pingCtx.beginPath();pingCtx.arc(p.x,p.y,p.size,0,Math.PI*2);pingCtx.fill()}pingCtx.globalAlpha=1}

var tttCanvas,tttCtx,tttS1El,tttS2El,tttRoundEl,tttStatusEl,TTT_W,TTT_H,TTT_CELL;
var tttRun=false,tttBoard=[],tttCurrent='p1',tttWins=[0,0],tttRound=0,tttGameOver=false,tttWinLine=null,tttLineProgress=0;
function initTTT(){if(tttCanvas)return;tttCanvas=$('tttCanvas');tttCtx=tttCanvas.getContext('2d');tttS1El=$('ttt-s1');tttS2El=$('ttt-s2');tttRoundEl=$('ttt-round');tttStatusEl=$('tttStatus');TTT_W=tttCanvas.width;TTT_H=tttCanvas.height;TTT_CELL=TTT_W/3}
function startTTT(){initTTT();tttWins=[0,0];tttRound=0;tttS1El.textContent='0';tttS2El.textContent='0';tttRoundEl.textContent='0';tttRun=true;tttNewRound()}
function stopTTT(){tttRun=false}
function tttNewMatch(){haptic(20);tttWins=[0,0];tttRound=0;tttS1El.textContent='0';tttS2El.textContent='0';tttRoundEl.textContent='0';tttNewRound()}
function tttNewRound(){tttBoard=[null,null,null,null,null,null,null,null,null];tttCurrent=tttRound%2===0?'p1':'p2';tttRound++;tttRoundEl.textContent=tttRound;tttGameOver=false;tttWinLine=null;tttLineProgress=0;haptic(15);tttUpdateStatus();tttDraw()}
function tttUpdateStatus(){if(tttGameOver)return;var e=tttCurrent==='p1'?'🔴 X (Игрок 1)':'🔵 O (Игрок 2)';tttStatusEl.textContent='Ход: '+e;tttStatusEl.style.color=tttCurrent==='p1'?'#e91e63':'#00e5ff'}
function tttClick(e){if(!tttRun||tttGameOver)return;var rect=tttCanvas.getBoundingClientRect(),x=(e.clientX-rect.left)*(tttCanvas.width/rect.width),y=(e.clientY-rect.top)*(tttCanvas.height/rect.height);var c=Math.floor(x/TTT_CELL),r=Math.floor(y/TTT_CELL);if(r<0||r>=3||c<0||c>=3)return;var i=r*3+c;if(tttBoard[i])return;tttBoard[i]=tttCurrent;haptic(15);tttDraw();var win=tttCheckWin();if(win){tttGameOver=true;tttWinLine=win;tttLineProgress=0;if(tttCurrent==='p1'){tttWins[0]++;tttS1El.textContent=tttWins[0];bump(tttS1El);toast('🔴 X победил!','s',1800)}else{tttWins[1]++;tttS2El.textContent=tttWins[1];bump(tttS2El);toast('🔵 O победил!','s',1800)}haptic(60);addCoins(5,false);var lp=0;var anim=setInterval(function(){lp+=0.08;tttLineProgress=Math.min(1,lp);tttDraw();if(lp>=1){clearInterval(anim);if(tttWins[0]>=3||tttWins[1]>=3){var champ=tttWins[0]>=3?'🔴 Игрок 1':'🔵 Игрок 2';setTimeout(function(){toast('👑 '+champ+' выиграл матч!','r',2500)},800);setTimeout(function(){tttNewMatch()},3000)}else{setTimeout(function(){if(tttRun)tttNewRound()},1800)}}},30);return}if(tttBoard.every(function(c){return c!==null})){tttGameOver=true;tttStatusEl.textContent='🤝 Ничья!';tttStatusEl.style.color='#ffd54f';haptic(40);toast('🤝 Ничья!','i',1500);setTimeout(function(){if(tttRun)tttNewRound()},1800);return}tttCurrent=tttCurrent==='p1'?'p2':'p1';tttUpdateStatus()}
function tttCheckWin(){var lines=[[0,1,2],[3,4,5],[6,7,8],[0,3,6],[1,4,7],[2,5,8],[0,4,8],[2,4,6]];for(var i=0;i<lines.length;i++){var l=lines[i];if(tttBoard[l[0]]&&tttBoard[l[0]]===tttBoard[l[1]]&&tttBoard[l[0]]===tttBoard[l[2]])return l}return null}
function tttDraw(){if(!tttCtx)return;tttCtx.fillStyle='#1a0a00';tttCtx.fillRect(0,0,TTT_W,TTT_H);tttCtx.strokeStyle='rgba(239,108,0,0.5)';tttCtx.lineWidth=4;tttCtx.beginPath();tttCtx.moveTo(TTT_CELL,0);tttCtx.lineTo(TTT_CELL,TTT_H);tttCtx.moveTo(TTT_CELL*2,0);tttCtx.lineTo(TTT_CELL*2,TTT_H);tttCtx.moveTo(0,TTT_CELL);tttCtx.lineTo(TTT_W,TTT_CELL);tttCtx.moveTo(0,TTT_CELL*2);tttCtx.lineTo(TTT_W,TTT_CELL*2);tttCtx.stroke();for(var i=0;i<9;i++){var r=Math.floor(i/3),c=i%3,x=c*TTT_CELL+TTT_CELL/2,y=r*TTT_CELL+TTT_CELL/2;if(tttBoard[i]==='p1'){tttCtx.strokeStyle='#e91e63';tttCtx.shadowColor='#e91e63';tttCtx.shadowBlur=15;tttCtx.lineWidth=8;tttCtx.lineCap='round';var off=TTT_CELL*0.25;tttCtx.beginPath();tttCtx.moveTo(x-off,y-off);tttCtx.lineTo(x+off,y+off);tttCtx.moveTo(x+off,y-off);tttCtx.lineTo(x-off,y+off);tttCtx.stroke();tttCtx.shadowBlur=0}else if(tttBoard[i]==='p2'){tttCtx.strokeStyle='#00e5ff';tttCtx.shadowColor='#00e5ff';tttCtx.shadowBlur=15;tttCtx.lineWidth=8;tttCtx.beginPath();tttCtx.arc(x,y,TTT_CELL*0.3,0,Math.PI*2);tttCtx.stroke();tttCtx.shadowBlur=0}}if(tttWinLine&&tttLineProgress>0){var a=tttWinLine[0],cc=tttWinLine[2];var ax=(a%3)*TTT_CELL+TTT_CELL/2,ay=Math.floor(a/3)*TTT_CELL+TTT_CELL/2;var cx=(cc%3)*TTT_CELL+TTT_CELL/2,cy=Math.floor(cc/3)*TTT_CELL+TTT_CELL/2;var curX=ax+(cx-ax)*tttLineProgress,curY=ay+(cy-ay)*tttLineProgress;var color=tttBoard[a]==='p1'?'#ff4081':'#40c4ff';tttCtx.strokeStyle=color;tttCtx.shadowColor=color;tttCtx.shadowBlur=25;tttCtx.lineWidth=10;tttCtx.lineCap='round';tttCtx.beginPath();tttCtx.moveTo(ax,ay);tttCtx.lineTo(curX,curY);tttCtx.stroke();tttCtx.shadowBlur=0}}

function attachSwipe(c,h,th){th=th||24;var sx=0,sy=0,tr=false;c.addEventListener('touchstart',function(e){var t=e.touches[0];sx=t.clientX;sy=t.clientY;tr=true},{passive:true});c.addEventListener('touchend',function(e){if(!tr)return;tr=false;var t=e.changedTouches[0];var dx=t.clientX-sx,dy=t.clientY-sy;if(Math.abs(dx)<th&&Math.abs(dy)<th)return;if(Math.abs(dx)>Math.abs(dy))h(dx>0?'right':'left');else h(dy>0?'down':'up')},{passive:true})}

function init(){updateBestScoresUI();try{initSnakeRefs();attachSwipe(sCanvas,function(d){if(d==='up')setSnakeDir(0,-1);else if(d==='down')setSnakeDir(0,1);else if(d==='left')setSnakeDir(-1,0);else if(d==='right')setSnakeDir(1,0)})}catch(e){}try{init2048Refs();attachSwipe(c2048,function(d){move2048(d)})}catch(e){}try{initM3();attachSwipe(mCanvas,function(d){moveMatch3(d)});mCanvas.addEventListener('click',match3Click);mCanvas.addEventListener('touchstart',function(e){e.preventDefault();var t=e.changedTouches[0];match3Click({clientX:t.clientX,clientY:t.clientY})},{passive:false})}catch(e){}try{initPuzzleRefs();pCanvas.addEventListener('click',puzzleClick);pCanvas.addEventListener('touchstart',function(e){e.preventDefault();var t=e.changedTouches[0];puzzleClick({clientX:t.clientX,clientY:t.clientY})},{passive:false})}catch(e){}try{initReactionRefs()}catch(e){}try{initArk()}catch(e){}try{initMem();memCanvas.addEventListener('click',memoryClick);memCanvas.addEventListener('touchstart',function(e){e.preventDefault();var t=e.changedTouches[0];memoryClick({clientX:t.clientX,clientY:t.clientY})},{passive:false})}catch(e){}try{initRace()}catch(e){}try{initFlappy()}catch(e){}try{initShooter()}catch(e){}try{initTetris();attachSwipe(tCanvas,function(d){if(d==='left')tetrisControl('left');else if(d==='right')tetrisControl('right');else if(d==='down')tetrisControl('drop');else if(d==='up')tetrisControl('rotate')})}catch(e){}try{initTower();twCanvas.addEventListener('click',towerClick);twCanvas.addEventListener('touchstart',function(e){e.preventDefault();var t=e.changedTouches[0];towerClick({clientX:t.clientX,clientY:t.clientY})},{passive:false})}catch(e){}try{initRpg();attachSwipe(rpgCanvas,function(d){if(d==='up')rpgSnakeDir(0,-1);else if(d==='down')rpgSnakeDir(0,1);else if(d==='left')rpgSnakeDir(-1,0);else if(d==='right')rpgSnakeDir(1,0)})}catch(e){}try{initGl()}catch(e){}try{initDuel()}catch(e){}try{initD2()}catch(e){}try{initPing()}catch(e){}try{initTTT();tttCanvas.addEventListener('click',tttClick);tttCanvas.addEventListener('touchstart',function(e){e.preventDefault();var t=e.changedTouches[0];tttClick({clientX:t.clientX,clientY:t.clientY})},{passive:false})}catch(e){}console.log('GAME HUB ready')}
if(document.readyState==='loading')document.addEventListener('DOMContentLoaded',init);else init();
</script></body></html>        --duel2-color: #00e5ff;
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

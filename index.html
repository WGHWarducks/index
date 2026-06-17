<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes, viewport-fit=cover">
  <title>AoS 4th • Damage Calculator v0.6</title>
  <style>
    * { margin:0; padding:0; box-sizing:border-box; }
    body {
      background:#0a0a0a;
      font-family:Georgia,'Times New Roman',serif;
      color:#e0e0e0;
      font-size:14px;
      line-height:1.4;
      padding-bottom:62px;
      -webkit-tap-highlight-color:transparent;
      user-select:none;
    }
    .app { max-width:750px; margin:0 auto; padding:8px 8px; }
    .wgh-banner { background:#0d0d0d; border-bottom:2px solid #c9a84c; text-align:center; padding:10px 0 6px; margin-bottom:10px; }
    .wgh-banner span { font-family:Georgia,'Times New Roman',serif; font-size:24px; letter-spacing:8px; color:#c9a84c; text-transform:uppercase; text-shadow:0 0 10px #000, 0 0 20px #c9a84c; }
    .screen { display:none; } .screen.active { display:block; }
    h2 { color:#c9a84c; font-weight:normal; font-size:18px; letter-spacing:1px; margin-bottom:8px; }
    h4 { color:#c9a84c; font-weight:normal; font-size:15px; letter-spacing:1px; margin-bottom:6px; }
    .card {
      background:#111;
      border:1px solid rgba(201,168,76,0.3);
      border-radius:8px;
      padding:10px;
      margin-bottom:10px;
    }
    .card-header {
      display:flex;
      align-items:center;
      justify-content:space-between;
      margin-bottom:8px;
      flex-wrap:wrap;
      gap:4px;
    }
    .profile-name {
      background:transparent;
      border:1px solid rgba(201,168,76,0.4);
      color:#c9a84c;
      font-family:Georgia,serif;
      font-size:14px;
      padding:6px 8px;
      border-radius:6px;
      width:140px;
    }
    .colour-dot { width:14px; height:14px; border-radius:50%; display:inline-block; margin-right:4px; flex-shrink:0; }
    .weapon-card {
      background:#181818;
      border:1px solid rgba(201,168,76,0.2);
      border-radius:6px;
      padding:8px;
      margin:6px 0;
    }
    .weapon-header { display:flex; align-items:center; justify-content:space-between; margin-bottom:4px; gap:4px; }
    .weapon-name {
      background:transparent;
      border:1px solid rgba(201,168,76,0.3);
      color:#c0c0c0;
      font-family:Georgia,serif;
      font-size:13px;
      padding:5px 6px;
      border-radius:5px;
      width:110px;
    }
    .stepper-row { display:flex; align-items:center; justify-content:space-between; margin-bottom:4px; flex-wrap:wrap; gap:2px; }
    .stepper-label { font-size:12px; color:#aaa; width:60px; flex-shrink:0; }
    .stepper-control { display:flex; align-items:center; gap:1px; background:#1a1a1a; border-radius:6px; padding:2px; }
    .stepper-btn {
      background:#2a2a2a; border:none; color:#c9a84c; font-size:20px; font-weight:bold;
      width:42px; height:42px; border-radius:6px; cursor:pointer; touch-action:manipulation;
      display:flex; align-items:center; justify-content:center;
    }
    .stepper-btn:active { background:#3a3a3a; }
    .stepper-btn.small { width:32px; height:32px; font-size:16px; }
    .stepper-value { min-width:40px; text-align:center; font-size:16px; color:#e0e0e0; font-weight:bold; padding:0 4px; }
    .damage-input {
      background:#1a1a1a; border:1px solid rgba(201,168,76,0.4); color:#e0e0e0;
      font-family:Georgia,serif; font-size:14px; padding:8px; border-radius:6px; width:90px; text-align:center;
    }
    .damage-input:focus { outline:1px solid #c9a84c; }
    .damage-input.invalid { border-color:#c0392b; }
    .error-hint { color:#c0392b; font-size:10px; margin-left:2px; display:none; }
    .error-hint.visible { display:inline; }
    .radio-group { display:flex; flex-wrap:wrap; gap:4px; margin:2px 0; }
    .radio-option, .toggle-option {
      display:flex; align-items:center; gap:4px; background:#1a1a1a; padding:5px 10px;
      border-radius:14px; border:1px solid rgba(201,168,76,0.3); font-size:11px; cursor:pointer;
    }
    .radio-option input, .toggle-option input { accent-color:#c9a84c; width:14px; height:14px; }
    .leader-toggle {
      display:flex; align-items:center; gap:6px; background:#1a1a1a; padding:6px 12px;
      border-radius:16px; border:1px solid rgba(201,168,76,0.3); font-size:12px; cursor:pointer;
    }
    .leader-toggle input { accent-color:#c9a84c; width:16px; height:16px; }
    .summary-line {
      font-size:12px; color:#c9a84c; margin-top:6px; font-style:italic;
      border-top:1px solid rgba(201,168,76,0.2); padding-top:6px;
    }
    .btn {
      background:#2a2a2a; border:1px solid #c9a84c; color:#c9a84c; padding:10px 14px;
      border-radius:6px; font-size:13px; font-family:Georgia,serif; cursor:pointer;
      min-height:42px; touch-action:manipulation; margin-right:4px; margin-bottom:4px;
    }
    .btn:active { background:#3a3a3a; }
    .btn.danger { border-color:#c0392b; color:#c0392b; }
    .btn.small { font-size:11px; padding:5px 8px; min-height:30px; }
    .btn.tiny { font-size:10px; padding:3px 6px; min-height:26px; }
    .visibility-toggle { display:flex; align-items:center; gap:4px; font-size:12px; color:#aaa; cursor:pointer; }
    .visibility-toggle input { accent-color:#c9a84c; }

    /* Bottom nav wrapper — constrains nav to max-width and centers on PC */
    .bottom-nav-wrapper {
      position:fixed; bottom:0; left:0; right:0; z-index:100;
      background:#0a0a0a;
      border-top:1px solid rgba(201,168,76,0.4);
    }
    .bottom-nav {
      max-width:750px; margin:0 auto;
      display:flex; justify-content:space-around;
      padding:4px 2px; height:54px;
    }
    .nav-btn {
      background:transparent; border:none; color:#888; font-size:11px; font-family:Georgia,serif;
      display:flex; flex-direction:column; align-items:center; gap:1px; padding:6px 2px;
      border-radius:10px; min-width:55px; cursor:pointer; touch-action:manipulation;
    }
    .nav-btn.active { color:#c9a84c; background:#1a1a1a; }
    .nav-btn span:first-child { font-size:18px; }
    svg { display:block; background:#0a0a0a; border-radius:6px; }
    .chart-scroll { width:100%; overflow-x:auto; -webkit-overflow-scrolling:touch; padding-bottom:2px; }
    .chart-scroll svg { width:auto; max-width:none; min-width:550px; height:auto; }
    .scroll-hint { text-align:center; color:#888; font-size:10px; padding:2px; display:none; }
    @media (max-width:650px){ .scroll-hint{ display:block; } }
    table { width:100%; border-collapse:collapse; margin-top:8px; font-size:11px; }
    th { color:#c9a84c; text-align:left; padding:6px 3px; border-bottom:1px solid rgba(201,168,76,0.3); }
    td { padding:6px 3px; border-bottom:1px solid #222; }
    .best-cell { color:#c9a84c; font-weight:bold; }
    .flex-row { display:flex; gap:8px; flex-wrap:wrap; align-items:center; margin:6px 0; }
    select {
      background:#1a1a1a; color:#e0e0e0; border:1px solid #c9a84c; padding:8px;
      border-radius:6px; font-family:Georgia,serif; font-size:13px; min-height:40px;
    }
    .stat-grid { display:grid; grid-template-columns:1fr 1fr; gap:4px; font-size:12px; }
    .bar-row { display:flex; align-items:center; gap:6px; margin:3px 0; }
    .bar-label { width:70px; text-align:right; font-size:12px; color:#e0e0e0; flex-shrink:0; }
    .bar-fill { height:16px; border-radius:3px; min-width:2px; transition:width 0.3s; }
    .pct { color:#c9a84c; }
    .skull { font-size:16px; }
    .total-attacks-info { color:#aaa; font-size:12px; margin-bottom:4px; }
    .version-badge { display:inline-block; background:#c9a84c; color:#000; font-size:8px; padding:1px 6px; border-radius:6px; margin-left:4px; vertical-align:middle; }
    .toggle-combine {
      display:inline-flex; align-items:center; gap:4px; background:#1a1a1a; border:1px solid rgba(201,168,76,0.3);
      padding:5px 10px; border-radius:14px; font-size:12px; cursor:pointer;
    }
    .toggle-combine input { accent-color:#c9a84c; }
    .buff-toggles-row, .debuff-toggles-row { margin-top:6px; display:flex; flex-wrap:wrap; align-items:center; gap:6px; }
    .buff-toggles-row span, .debuff-toggles-row span { color:#aaa; font-size:12px; flex-shrink:0; }
    .buff-toggle {
      display:inline-flex; align-items:center; gap:4px; background:#1a2a1a; border:1px solid rgba(76,201,76,0.3);
      padding:5px 10px; border-radius:14px; font-size:11px; cursor:pointer;
    }
    .buff-toggle input { accent-color:#4cc94c; }

    /* Mobile optimizations */
    @media (max-width:480px) {
      body { font-size:12px; padding-bottom:52px; }
      .app { padding:6px 4px; }
      .wgh-banner span { font-size:20px; letter-spacing:6px; }
      h2 { font-size:16px; }
      .card { padding:8px; margin-bottom:8px; }
      .profile-name { width:120px; font-size:13px; }
      .weapon-name { width:100px; font-size:12px; }
      .stepper-btn { width:36px; height:36px; font-size:18px; }
      .stepper-btn.small { width:28px; height:28px; font-size:14px; }
      .stepper-value { min-width:34px; font-size:14px; }
      .damage-input { width:75px; font-size:13px; padding:6px; }
      .radio-option, .toggle-option { padding:4px 8px; font-size:10px; }
      .leader-toggle { padding:5px 10px; font-size:11px; }
      .stat-grid { grid-template-columns:1fr; }
      .bar-label { width:60px; font-size:11px; }
      select { font-size:12px; min-height:36px; padding:6px; }
      .btn { padding:8px 10px; font-size:12px; min-height:36px; }
      .nav-btn { font-size:10px; min-width:48px; }
      .nav-btn span:first-child { font-size:16px; }
      .bottom-nav { height:46px; }
    }
  </style>
</head>
<body>
<div class="app" id="app">
  <div class="wgh-banner"><span>WGH Warducks</span></div>
  <div id="screen1" class="screen active"><h2>⚔️ Attack Profiles <span class="version-badge">v0.6</span></h2><div id="profilesContainer"></div><button class="btn" id="addProfileBtn">➕ Add Profile</button></div>
  <div id="screen2" class="screen"><h2>📊 Save Comparison</h2><div class="flex-row"><label style="color:#e0e0e0;font-size:12px;">Ward: <select id="globalWardSelect"><option value="0">None</option><option value="6">6+</option><option value="5">5+</option><option value="4">4+</option></select></label><label class="toggle-combine"><input type="checkbox" id="combineWeaponsToggle" onchange="combineWeapons=this.checked;renderScreen2();renderScreen3();"> Combine weapons</label></div><div id="saveChartContainer" class="card" style="padding:4px;"></div><div id="saveTableContainer"></div></div>
  <div id="screen3" class="screen"><h2>🎲 Damage Distribution</h2><div class="flex-row"><label style="color:#e0e0e0;font-size:12px;">Save: <select id="distSaveSelect"><option value="0">None</option><option value="6">6+</option><option value="5">5+</option><option value="4" selected>4+</option><option value="3">3+</option><option value="2">2+</option></select></label><label style="color:#e0e0e0;font-size:12px;">Ward: <select id="distWardSelect"><option value="0">None</option><option value="6">6+</option><option value="5">5+</option><option value="4">4+</option></select></label><label style="color:#e0e0e0;font-size:12px;">Show: <select id="distProfileSelect"><option value="all">All Profiles</option></select></label></div><div id="distChartContainer" class="card chart-scroll" style="padding:4px;"><div class="scroll-hint">← scroll chart →</div></div><div id="distStatsContainer" class="card"></div></div>
  <div id="screen4" class="screen"><h2>💀 Kill Probability</h2><div class="card"><div class="stepper-row"><span class="stepper-label">Wounds</span><div class="stepper-control" id="killWoundsStepper"></div></div><div class="stepper-row"><span class="stepper-label">Models</span><div class="stepper-control" id="killModelsStepper"></div></div><div class="flex-row"><label style="color:#e0e0e0;font-size:12px;">Save: <select id="killSaveSelect"><option value="0">None</option><option value="6">6+</option><option value="5">5+</option><option value="4">4+</option><option value="3">3+</option><option value="2">2+</option></select></label><label style="color:#e0e0e0;font-size:12px;">Ward: <select id="killWardSelect"><option value="0">None</option><option value="6">6+</option><option value="5">5+</option><option value="4">4+</option></select></label></div><div class="buff-toggles-row"><span>Buffs:</span><div id="buffToggles" style="display:flex;flex-wrap:wrap;gap:4px;"></div></div><div class="debuff-toggles-row"><span>Debuffs:</span><div id="debuffToggles" style="display:flex;flex-wrap:wrap;gap:4px;"></div><button class="btn tiny" onclick="clearBuffsDebuffs()">Clear all</button></div></div><div id="killStatsContainer"></div><div id="killChartContainer" class="card" style="padding:4px;"></div><div id="killBreakdownContainer" class="chart-scroll"><div class="scroll-hint">← scroll table →</div></div></div>
</div>
<div class="bottom-nav-wrapper">
  <nav class="bottom-nav">
    <button class="nav-btn active" data-screen="1"><span>⚔️</span>Profiles</button>
    <button class="nav-btn" data-screen="2"><span>📊</span>Saves</button>
    <button class="nav-btn" data-screen="3"><span>🎲</span>Dist</button>
    <button class="nav-btn" data-screen="4"><span>💀</span>Kill</button>
  </nav>
</div>

<script>
  // ==================== v0.6 – Ward fix + bug fixes + code cleanup + AoA/AoD + responsive + skull + fixed nav ====================
  let combineWeapons = true;
  const PALETTE = ['#c9a84c', '#cd7f32', '#c0c0c0', '#7f8c8d'];
  let profiles = [], distSelectedVal = 'all', killState = { wounds:2, models:5 }, pendingRender = false;
  let killDebuffs = { hit: false, wound: false, attacks: false };
  let killBuffs = { aoa: false, aod: false };

  // --- utility functions ---
  function escHtml(s) { return String(s).replace(/[&<>"']/g, m => ({ '&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;' })[m]); }

  function parseDiceExpr(expr) {
    const t = String(expr).trim().replace(/\s+/g, '');
    if (/^\d+$/.test(t)) return { type: 'fixed', value: parseInt(t), valid: true };
    const parts = t.split('+');
    let dice = [], constant = 0;
    for (let p of parts) {
      p = p.trim();
      if (/^\d+$/.test(p)) { constant += parseInt(p); continue; }
      let m = p.match(/^(\d*)D(\d+)$/i);
      if (m) {
        let count = m[1] ? parseInt(m[1]) : 1, sides = parseInt(m[2]);
        if (sides < 2 || sides > 6 || count < 1 || count > 20) return { valid: false, error: 'D3/D6' };
        for (let i = 0; i < count; i++) dice.push(sides);
        continue;
      }
      return { valid: false, error: 'Invalid' };
    }
    if (dice.length === 0) return { type: 'fixed', value: constant, valid: true };
    return { type: 'dice', dice, constant, valid: true };
  }

  function singleDieDist(sides) { let d = []; for (let i = 1; i <= sides; i++) d.push({ value: i, prob: 1 / sides }); return d; }

  function convolveArrays(a, b) {
    let map = new Map();
    for (let x of a) for (let y of b) {
      let v = x.value + y.value;
      map.set(v, (map.get(v) || 0) + x.prob * y.prob);
    }
    let r = [];
    for (let [v, p] of map) r.push({ value: v, prob: p });
    r.sort((a, b) => a.value - b.value);
    return r;
  }

  function distribution(expr) {
    let p = parseDiceExpr(expr);
    if (!p || !p.valid) return null;
    if (p.type === 'fixed') return [{ value: p.value, prob: 1.0 }];
    let d = [{ value: 0, prob: 1.0 }];
    for (let s of p.dice) d = convolveArrays(d, singleDieDist(s));
    if (p.constant) d = d.map(x => ({ value: x.value + p.constant, prob: x.prob }));
    return d;
  }

  function expectedValue(d) { return d.reduce((a, x) => a + x.value * x.prob, 0); }

  function probGE(d, t) {
    let sum = 0;
    for (let x of d) if (x.value >= t) sum += x.prob;
    return sum;
  }

  function binomialDistribution(n, p) {
    let dist = [{ value: 0, prob: 1 }];
    for (let i = 0; i < n; i++) {
      dist = convolveArrays(dist, [{ value: 1, prob: p }, { value: 0, prob: 1 - p }]);
    }
    return dist;
  }

  function formatProb(p) {
    if (p >= 0.99995) return '<span class="skull">💀</span>';
    return (p * 100).toFixed(2) + '%';
  }

  function saveFailProb(saveChar, rendVal, aodBonus = 0) {
    if (saveChar === 0) return 1;
    let effectiveSave = saveChar - aodBonus;
    let modSave = effectiveSave - rendVal;
    if (modSave > 6) return 1;
    return (Math.max(2, modSave) - 1) / 6;
  }

  function wardFailProb(wardVal) {
    if (!wardVal || wardVal === 0) return 1;
    return (wardVal - 1) / 6;
  }

  function applyModifiers(weapon, debuffs, buffs) {
    let hitMod = 0;
    if (debuffs?.hit) hitMod += 1;
    if (buffs?.aoa) hitMod -= 1;
    return {
      hitTarget: Math.min(6, Math.max(2, weapon.hit + hitMod)),
      woundTarget: debuffs?.wound ? Math.min(6, weapon.wound + 1) : weapon.wound,
      attacksMod: debuffs?.attacks ? -1 : 0,
      aodBonus: buffs?.aod ? 1 : 0
    };
  }

  // ================== CORE ATTACK DISTRIBUTION ==================
  function singleAttackDistribution(weapon, saveChar, wardVal, debuffs = null, buffs = null) {
    const { hitTarget, woundTarget, aodBonus } = applyModifiers(weapon, debuffs, buffs);
    const pMiss = (hitTarget - 1) / 6;
    const pHit = (7 - hitTarget - 1) / 6;
    const pSix = 1 / 6;
    const pWound = (7 - woundTarget) / 6;
    const pWardFail = wardFailProb(wardVal);
    const pFail = saveFailProb(saveChar, weapon.rend, aodBonus);
    const dmgDist = distribution(weapon.damage);
    if (!dmgDist) return null;
    const critType = weapon.critType;

    function normalHitMap() {
      let map = new Map();
      let through = pWound * pFail * pWardFail;
      for (let d of dmgDist) map.set(d.value, (map.get(d.value) || 0) + through * d.prob);
      let missProb = 1 - through;
      if (missProb > 0) map.set(0, (map.get(0) || 0) + missProb);
      return map;
    }

    if (critType === 'none') {
      let allHitMap = normalHitMap();
      let final = new Map();
      final.set(0, pMiss);
      for (let [v, p] of allHitMap) final.set(v, (final.get(v) || 0) + (pHit + pSix) * p);
      return Array.from(final, ([v, p]) => ({ value: v, prob: p })).sort((a, b) => a.value - b.value);
    }

    function critHitMap() {
      if (critType === 'mortal') {
        let result = new Map();
        for (let d of dmgDist) {
          let binom = binomialDistribution(d.value, pWardFail);
          for (let {value: k, prob: bp} of binom) result.set(k, (result.get(k) || 0) + d.prob * bp);
        }
        return result;
      } else {
        let base = new Map();
        let through = pFail * pWardFail;
        for (let d of dmgDist) {
          let dmg = d.value;
          if (critType === 'doubleDamage') dmg *= 2;
          base.set(dmg, (base.get(dmg) || 0) + through * d.prob);
        }
        let missProb = 1 - through;
        if (missProb > 0) base.set(0, (base.get(0) || 0) + missProb);
        if (critType === 'extraHit') {
          let extra = normalHitMap();
          let result = new Map();
          for (let [v1, p1] of base) for (let [v2, p2] of extra) { let v = v1 + v2; result.set(v, (result.get(v) || 0) + p1 * p2); }
          return result;
        }
        return base;
      }
    }

    let final = new Map();
    final.set(0, pMiss);
    let normalMap = normalHitMap();
    for (let [v, p] of normalMap) final.set(v, (final.get(v) || 0) + pHit * p);
    let critMap = critHitMap();
    for (let [v, p] of critMap) final.set(v, (final.get(v) || 0) + pSix * p);

    let total = 0;
    for (let p of final.values()) total += p;
    if (total > 0 && Math.abs(total - 1) > 1e-10) for (let [k, p] of final) final.set(k, p / total);
    return Array.from(final, ([v, p]) => ({ value: v, prob: p })).sort((a, b) => a.value - b.value);
  }

  function computeWeaponDamageDistribution(profile, weaponIdx, saveChar, wardVal, debuffs = null, buffs = null) {
    const weapon = profile.weapons[weaponIdx];
    let perAttack = singleAttackDistribution(weapon, saveChar, wardVal, debuffs, buffs);
    if (!perAttack) return null;
    let attDist = distribution(weapon.attacks);
    if (!attDist) return null;
    if (debuffs?.attacks) attDist = attDist.map(x => ({ value: Math.max(1, x.value - 1), prob: x.prob }));
    let maxAtt = Math.max(...attDist.map(a => a.value));
    let dists = [[{ value: 0, prob: 1.0 }]];
    for (let n = 1; n <= maxAtt; n++) dists[n] = convolveArrays(dists[n - 1], perAttack);
    let resultMap = new Map();
    for (let a of attDist) { let d = dists[a.value]; for (let { value, prob } of d) resultMap.set(value, (resultMap.get(value) || 0) + prob * a.prob); }
    let result = []; for (let [v, p] of resultMap) result.push({ value: v, prob: p }); result.sort((a, b) => a.value - b.value);
    return result;
  }

  function computeProfileDistribution(profile, saveChar, wardVal, debuffs = null, buffs = null) {
    let combined = [{ value: 0, prob: 1.0 }];
    for (let wi = 0; wi < profile.weapons.length; wi++) { let wd = computeWeaponDamageDistribution(profile, wi, saveChar, wardVal, debuffs, buffs); if (!wd) return null; combined = convolveArrays(combined, wd); }
    let modelDist = [{ value: 0, prob: 1.0 }];
    for (let i = 0; i < profile.models; i++) modelDist = convolveArrays(modelDist, combined);
    if (profile.leader && profile.weapons.length > 0) { let lb = singleAttackDistribution(profile.weapons[0], saveChar, wardVal, debuffs, buffs); if (lb) modelDist = convolveArrays(modelDist, lb); }
    return modelDist;
  }

  // --- profile management ---
  function newWeapon(index) { return { id: Date.now() + Math.random(), name: 'Weapon ' + (index + 1), attacks: '2', hit: 4, wound: 4, rend: 0, damage: '1', critType: 'none' }; }
  function newProfile(name, color) { return { id: Date.now() + Math.random(), name, color, models: 1, leader: false, weapons: [newWeapon(0)], visible: true }; }
  function initProfiles() {
    profiles = [
      { id:1, name:'Dracoth Riders', color:PALETTE[0], models:2, leader:false, weapons:[{ id:101, name:'Storm-wreathed Blades', attacks:'3', hit:3, wound:3, rend:-1, damage:'1', critType:'mortal' }], visible:true },
      { id:2, name:'Vindictors', color:PALETTE[1], models:5, leader:true, weapons:[{ id:201, name:'Stormstrike Halberd', attacks:'2', hit:3, wound:4, rend:0, damage:'1', critType:'none' }], visible:true }
    ];
  }
  function getUnusedColor() { let u = profiles.map(p => p.color); for (let c of PALETTE) if (!u.includes(c)) return c; return PALETTE[profiles.length % PALETTE.length]; }
  function setProfileField(i, f, v) { if (i >= 0 && i < profiles.length) { profiles[i][f] = v; scheduleRefresh(); } }
  function setWeaponField(pi, wi, f, v) { if (pi >= 0 && pi < profiles.length && wi >= 0 && wi < profiles[pi].weapons.length) { profiles[pi].weapons[wi][f] = v; scheduleRefresh(); } }
  function addWeapon(pi) { if (pi >= 0 && pi < profiles.length && profiles[pi].weapons.length < 4) { profiles[pi].weapons.push(newWeapon(profiles[pi].weapons.length)); scheduleRefresh(); } }
  function removeWeapon(pi, wi) { if (pi >= 0 && pi < profiles.length && profiles[pi].weapons.length > 1 && wi >= 0 && wi < profiles[pi].weapons.length) { profiles[pi].weapons.splice(wi, 1); scheduleRefresh(); } }
  function scheduleRefresh() { if (pendingRender) return; pendingRender = true; requestAnimationFrame(() => { pendingRender = false; refreshAll(); }); }
  function refreshAll() { renderProfiles(); renderScreen2(); renderScreen3(); renderScreen4(); }

  // ==================== UNIFIED STEPPER BUILDER ====================
  function buildStepper(id, config) {
    let el = document.getElementById(id); if (!el) return; el.innerHTML = '';
    let current = config.value;
    let minus = document.createElement('button'); minus.className = 'stepper-btn' + (config.small ? ' small' : ''); minus.textContent = '−';
    let plus = document.createElement('button'); plus.className = 'stepper-btn' + (config.small ? ' small' : ''); plus.textContent = '+';
    let display = document.createElement('span'); display.className = 'stepper-value';
    display.textContent = config.format ? config.format(current) : String(current);
    function update() { display.textContent = config.format ? config.format(current) : String(current); }
    minus.onclick = () => { if (current > config.min) { current--; update(); config.onChange(current); } };
    plus.onclick = () => { if (current < config.max) { current++; update(); config.onChange(current); } };
    el.append(minus, display, plus);
    return { setValue: (v) => { current = v; update(); } };
  }

  function adjustDiceField(pi, wi, field, delta) {
    let w = profiles[pi].weapons[wi], parsed = parseDiceExpr(w[field]);
    if (!parsed || !parsed.valid) return;
    if (parsed.type === 'fixed') { setWeaponField(pi, wi, field, String(Math.max(1, parsed.value + delta))); }
    else { let nc = Math.max(0, parsed.constant + delta), ds = parsed.dice.map(s => 'D' + s).join('+'); setWeaponField(pi, wi, field, nc > 0 ? (ds ? ds + '+' + nc : String(nc)) : (ds || '0')); }
  }

  function validateWeaponInput(pi, wi, field) {
    let i = document.getElementById((field === 'attacks' ? 'watt' : 'wdmg') + '-' + pi + '-' + wi), e = document.getElementById((field === 'attacks' ? 'watt-err' : 'wdmg-err') + '-' + pi + '-' + wi);
    if (!i || !e) return; let v = parseDiceExpr(i.value).valid; i.classList.toggle('invalid', !v); e.classList.toggle('visible', !v);
  }

  function buildWeaponCritRadios(id, pi, wi, sel) {
    let e = document.getElementById(id); if (!e) return;
    let t = [{ val:'none', label:'No Crits' },{ val:'mortal', label:'Mortal on Crit' },{ val:'autoWound', label:'Auto-wound' },{ val:'doubleDamage', label:'Double Damage' },{ val:'extraHit', label:'Crit 2 Hits' }];
    e.innerHTML = t.map(x => `<label class="radio-option"><input type="radio" name="wcrit${pi}-${wi}" value="${x.val}" ${sel===x.val?'checked':''} onchange="setWeaponField(${pi},${wi},'critType','${x.val}')">${x.label}</label>`).join('');
  }

  // ==================== UI RENDERING ====================
  function renderProfileCard(idx) {
    let p = profiles[idx], totalAttacks = 0;
    p.weapons.forEach(w => { let ad = distribution(w.attacks); totalAttacks += Math.round((ad ? expectedValue(ad) : 0) * p.models); });
    if (p.leader && p.weapons.length > 0) totalAttacks += 1;
    return `<div class="card"><div class="card-header"><span class="colour-dot" style="background:${p.color}"></span><input class="profile-name" value="${escHtml(p.name)}" onfocus="this.select()" onchange="let v=this.value.trim();if(v)setProfileField(${idx},'name',v);else this.value=profiles[${idx}].name;"><div style="display:flex;align-items:center;gap:4px;"><label class="visibility-toggle"><input type="checkbox" ${p.visible?'checked':''} onchange="setProfileField(${idx},'visible',this.checked)"> Show</label><button class="btn small" onclick="duplicateProfile(${idx})">📋</button>${profiles.length>1?`<button class="btn small danger" onclick="deleteProfile(${idx})">🗑</button>`:''}</div></div><div class="stepper-row"><span class="stepper-label">Models</span><div class="stepper-control" id="models-stepper-${idx}"></div></div><div class="stepper-row"><span class="stepper-label">Leader</span><label class="leader-toggle"><input type="checkbox" ${p.leader?'checked':''} onchange="setProfileField(${idx},'leader',this.checked)"> +1 Attack (Champion, uses Weapon 1)</label></div><div class="total-attacks-info">Total attacks: <b class="pct">${totalAttacks}</b> across ${p.weapons.length} weapon${p.weapons.length>1?'s':''}</div><div id="weapons-container-${idx}"></div><button class="btn small" onclick="addWeapon(${idx})" ${p.weapons.length>=4?'disabled style="opacity:0.4"':''}>➕ Add Weapon</button><div class="summary-line" id="summary-${idx}">Avg — vs 4+ save</div></div>`;
  }

  function renderProfiles() {
    let c = document.getElementById('profilesContainer'); c.innerHTML = '';
    profiles.forEach((p, idx) => { c.insertAdjacentHTML('beforeend', renderProfileCard(idx)); buildStepper('models-stepper-'+idx,{min:1,max:20,value:p.models,onChange:(v)=>setProfileField(idx,'models',v)}); renderWeapons(idx); updateSummaryLine(idx); });
  }

  function renderWeapons(pi) {
    let container = document.getElementById('weapons-container-'+pi); if (!container) return; let p = profiles[pi]; container.innerHTML = '';
    p.weapons.forEach((w, wi) => {
      let wc = document.createElement('div'); wc.className = 'weapon-card';
      wc.innerHTML = `<div class="weapon-header"><input class="weapon-name" value="${escHtml(w.name)}" onfocus="this.select()" onchange="setWeaponField(${pi},${wi},'name',this.value)">${p.weapons.length>1?`<button class="btn tiny danger" onclick="removeWeapon(${pi},${wi})">✕ Remove</button>`:''}</div><div class="stepper-row"><span class="stepper-label">Attacks</span><div style="display:flex;align-items:center;gap:4px;"><button class="stepper-btn small" onclick="adjustDiceField(${pi},${wi},'attacks',-1)">−</button><input class="damage-input" id="watt-${pi}-${wi}" value="${escHtml(w.attacks)}" onfocus="this.select()" onchange="setWeaponField(${pi},${wi},'attacks',this.value);validateWeaponInput(${pi},${wi},'attacks')"><button class="stepper-btn small" onclick="adjustDiceField(${pi},${wi},'attacks',1)">+</button></div><span class="error-hint" id="watt-err-${pi}-${wi}">Invalid</span></div><div class="stepper-row"><span class="stepper-label">Hit</span><div class="stepper-control" id="whit-${pi}-${wi}"></div></div><div class="stepper-row"><span class="stepper-label">Wound</span><div class="stepper-control" id="wwnd-${pi}-${wi}"></div></div><div class="stepper-row"><span class="stepper-label">Rend</span><div class="stepper-control" id="wrend-${pi}-${wi}"></div></div><div class="stepper-row"><span class="stepper-label">Damage</span><div style="display:flex;align-items:center;gap:4px;"><button class="stepper-btn small" onclick="adjustDiceField(${pi},${wi},'damage',-1)">−</button><input class="damage-input" id="wdmg-${pi}-${wi}" value="${escHtml(w.damage)}" onfocus="this.select()" onchange="setWeaponField(${pi},${wi},'damage',this.value);validateWeaponInput(${pi},${wi},'damage')"><button class="stepper-btn small" onclick="adjustDiceField(${pi},${wi},'damage',1)">+</button></div><span class="error-hint" id="wdmg-err-${pi}-${wi}">Invalid</span></div><div class="radio-group" id="wcrit-${pi}-${wi}"></div>`;
      container.appendChild(wc);
      buildStepper('whit-'+pi+'-'+wi,{min:2,max:6,value:w.hit,format:(v)=>v+'+',onChange:(v)=>setWeaponField(pi,wi,'hit',v)});
      buildStepper('wwnd-'+pi+'-'+wi,{min:2,max:6,value:w.wound,format:(v)=>v+'+',onChange:(v)=>setWeaponField(pi,wi,'wound',v)});
      buildStepper('wrend-'+pi+'-'+wi,{min:-3,max:0,value:w.rend,format:(v)=>v===0?'—':'−'+Math.abs(v),onChange:(v)=>setWeaponField(pi,wi,'rend',v)});
      buildWeaponCritRadios('wcrit-'+pi+'-'+wi,pi,wi,w.critType); validateWeaponInput(pi,wi,'attacks'); validateWeaponInput(pi,wi,'damage');
    });
  }

  function updateSummaryLine(idx) { let p=profiles[idx],d=computeProfileDistribution(p,4,0),avg=d?expectedValue(d).toFixed(2):'—',el=document.getElementById('summary-'+idx); if(el)el.textContent='Avg '+avg+' damage vs 4+ save (no ward)'; }
  function duplicateProfile(idx) { if(profiles.length>=4)return; let c=JSON.parse(JSON.stringify(profiles[idx]));c.id=Date.now()+Math.random();c.name+=' copy';c.color=getUnusedColor();profiles.splice(idx+1,0,c);scheduleRefresh(); }
  function deleteProfile(idx) { if(profiles.length<=1)return;profiles.splice(idx,1);scheduleRefresh(); }
  document.getElementById('addProfileBtn').onclick=()=>{if(profiles.length>=4)return;profiles.push(newProfile('Profile '+(profiles.length+1),getUnusedColor()));scheduleRefresh();};

  // ==================== SCREEN 2 ====================
  function renderScreen2() {
    let ward=parseInt(document.getElementById('globalWardSelect').value),saves=[0,6,5,4,3,2];
    document.getElementById('combineWeaponsToggle').checked=combineWeapons;
    let lines=[];profiles.filter(p=>p.visible).forEach(p=>{if(combineWeapons)lines.push({name:p.name,color:p.color,getValues:()=>saves.map(s=>{let d=computeProfileDistribution(p,s,ward);return d?expectedValue(d):0})});else p.weapons.forEach((w,wi)=>{let wp=JSON.parse(JSON.stringify(p));wp.weapons=[w];wp.leader=false;lines.push({name:w.name||(p.name+' W'+(wi+1)),color:p.color,getValues:()=>saves.map(s=>{let d=computeProfileDistribution(wp,s,ward);return d?expectedValue(d):0})})})});
    let data=lines.map(l=>({name:l.name,color:l.color,values:l.getValues()})),cc=document.getElementById('saveChartContainer'),tc=document.getElementById('saveTableContainer');
    if(data.length===0){cc.innerHTML='<p style="color:#888;padding:20px;">No visible profiles</p>';tc.innerHTML='';return;}
    let mv=Math.max(...data.flatMap(d=>d.values),0.1),w=600,h=230,pL=50,pR=30,pT=18,pB=30,pW=w-pL-pR,pH=h-pT-pB;
    let svg=`<svg viewBox="0 0 ${w} ${h}" preserveAspectRatio="xMidYMid meet">`;
    for(let i=0;i<=4;i++){let yV=(mv/4)*i,y=h-pB-(yV/mv)*pH;svg+=`<line x1="${pL}" y1="${y}" x2="${w-pR}" y2="${y}" stroke="#333" stroke-dasharray="3,3"/><text x="${pL-4}" y="${y+3}" text-anchor="end" fill="#888" font-size="10" font-family="Georgia,serif">${yV.toFixed(1)}</text>`;}
    saves.forEach((s,i)=>{let x=pL+(i/(saves.length-1))*pW;svg+=`<text x="${x}" y="${h-4}" text-anchor="middle" fill="#888" font-size="10" font-family="Georgia,serif">${s===0?'None':s+'+'}</text>`;});
    data.forEach(d=>{let pts=d.values.map((v,i)=>`${pL+(i/(saves.length-1))*pW},${h-pB-(v/mv)*pH}`).join(' ');svg+=`<polyline points="${pts}" fill="none" stroke="${d.color}" stroke-width="2" stroke-linejoin="round"/>`;d.values.forEach((v,i)=>{let x=pL+(i/(saves.length-1))*pW,y=h-pB-(v/mv)*pH;svg+=`<circle cx="${x}" cy="${y}" r="3" fill="${d.color}"/>`;})});
    data.forEach((d,i)=>{let label=escHtml(d.name);if(label.length>12)label=label.slice(0,10)+'…';svg+=`<rect x="${w-140}" y="${pT+i*16}" width="10" height="10" fill="${d.color}" rx="2"/><text x="${w-126}" y="${pT+9+i*16}" fill="#c0c0c0" font-size="10" font-family="Georgia,serif">${label}</text>`;});
    svg+='</svg>';cc.innerHTML=svg;
    let html='<table><tr><th>Save</th>'+data.map(d=>`<th>${escHtml(d.name)}</th>`).join('')+'</tr>';
    saves.forEach((s,i)=>{let best=Math.max(...data.map(d=>d.values[i]));html+=`<tr><td>${s===0?'None':s+'+'}</td>`;data.forEach(d=>{let v=d.values[i].toFixed(2);html+=`<td class="${d.values[i]===best&&best>0&&data.filter(x=>x.values[i]===best).length===1?'best-cell':''}">${v}</td>`;});html+='</tr>';});
    html+='</table>';tc.innerHTML=html;
  }
  document.getElementById('globalWardSelect').onchange=()=>renderScreen2();

  // ==================== SCREEN 3 ====================
  function renderScreen3() {
    let save=parseInt(document.getElementById('distSaveSelect').value),ward=parseInt(document.getElementById('distWardSelect').value),sel=document.getElementById('distProfileSelect');
    sel.innerHTML='<option value="all">All Profiles</option>'+profiles.map((p,i)=>`<option value="${i}" ${String(i)===distSelectedVal?'selected':''}>${escHtml(p.name)}</option>`).join('');
    let val=sel.value;distSelectedVal=val;let allDists=[];
    if(val==='all'){profiles.forEach(p=>{let d=computeProfileDistribution(p,save,ward);if(d)allDists.push({name:p.name,color:p.color,dist:d})})}
    else{let p=profiles[parseInt(val)];if(combineWeapons){let d=computeProfileDistribution(p,save,ward);if(d)allDists.push({name:p.name,color:p.color,dist:d})}else p.weapons.forEach((w,wi)=>{let wp=JSON.parse(JSON.stringify(p));wp.weapons=[w];wp.leader=false;let d=computeProfileDistribution(wp,save,ward);if(d)allDists.push({name:w.name||(p.name+' W'+(wi+1)),color:p.color,dist:d})})}
    let cc=document.getElementById('distChartContainer'),sc=document.getElementById('distStatsContainer');
    if(allDists.length===0){cc.innerHTML='<p style="color:#c0392b;padding:20px;">Invalid expression</p>';sc.innerHTML='';return;}
    let globalMax=Math.max(...allDists.flatMap(d=>d.dist.map(x=>x.value)),1),globalMaxP=Math.max(...allDists.flatMap(d=>d.dist.map(x=>x.prob)),0.001),displayMax=Math.min(globalMax,40),labelStep=displayMax>=20?5:(displayMax>=10?2:1),barW=Math.max(7,Math.min(24,480/(allDists.length*(displayMax+1)+2))),groupW=barW*allDists.length+2,tw=Math.max(560,(displayMax+1)*(groupW+2)+60),h=240,pL=50,pR=30,pT=22,pB=35,pH=h-pT-pB;
    let svg=`<svg viewBox="0 0 ${tw} ${h}" preserveAspectRatio="xMidYMid meet">`;
    for(let i=0;i<=4;i++){let yV=(globalMaxP/4)*i,y=h-pB-(yV/globalMaxP)*pH;svg+=`<line x1="${pL}" y1="${y}" x2="${tw-pR}" y2="${y}" stroke="#333"/><text x="${pL-4}" y="${y+3}" text-anchor="end" fill="#888" font-size="10" font-family="Georgia,serif">${(yV*100).toFixed(0)}%</text>`;}
    for(let v=0;v<=displayMax;v++){allDists.forEach(({color,dist},di)=>{let d=dist.find(x=>x.value===v),prob=d?d.prob:0,x=pL+v*(groupW+2)+di*barW,barH=Math.max(prob>0?1.5:0,(prob/globalMaxP)*pH);svg+=`<rect x="${x}" y="${h-pB-barH}" width="${barW-1}" height="${barH}" fill="${color}" opacity="0.85"/>`;});if(v%labelStep===0||v===displayMax){let x=pL+v*(groupW+2)+(allDists.length*barW)/2;svg+=`<text x="${x}" y="${h-8}" text-anchor="middle" fill="#888" font-size="9" font-family="Georgia,serif">${v}</text>`;}}
    allDists.forEach(({name,color},i)=>{let label=escHtml(name);if(label.length>12)label=label.slice(0,10)+'…';svg+=`<rect x="${tw-140}" y="${pT+i*16}" width="10" height="10" fill="${color}" rx="2"/><text x="${tw-126}" y="${pT+9+i*16}" fill="#c0c0c0" font-size="10" font-family="Georgia,serif">${label}</text>`;});
    svg+='</svg>';cc.innerHTML='<div class="scroll-hint">← scroll chart →</div>'+svg;
    let sh='';allDists.forEach(({name,color,dist})=>{let sorted=[...dist].sort((a,b)=>a.value-b.value),mean=expectedValue(dist),p5=(probGE(dist,5)*100).toFixed(2),p10=(probGE(dist,10)*100).toFixed(2),p15=(probGE(dist,15)*100).toFixed(2),cum=0,p25=null,p75=null;for(let d of sorted){cum+=d.prob;if(cum>=0.25&&p25===null)p25=d.value;if(cum>=0.75&&p75===null){p75=d.value;break}}if(p75===null)p75=sorted[sorted.length-1].value;if(p25===null)p25=sorted[0].value;sh+=`<div style="margin-bottom:8px;border-left:3px solid ${color};padding-left:8px;"><b style="color:${color}">${escHtml(name)}</b><div class="stat-grid"><div>Mean: <b class="pct">${mean.toFixed(2)}</b></div><div>Min/Max: <b class="pct">${sorted[0].value}/${sorted[sorted.length-1].value}</b></div><div>P(≥5): <b class="pct">${p5}%</b></div><div>P(≥10): <b class="pct">${p10}%</b></div><div>P(≥15): <b class="pct">${p15}%</b></div><div>25th–75th: <b class="pct">${p25===p75?p25+' (all)':p25+' – '+p75}</b></div></div></div>`});sc.innerHTML=sh;
  }
  ['distSaveSelect','distWardSelect'].forEach(id=>{document.getElementById(id).onchange=()=>renderScreen3();});
  document.getElementById('distProfileSelect').onchange=function(){distSelectedVal=this.value;renderScreen3();};

  // ==================== SCREEN 4 ====================
  function buildKillSteppers(){function bk(id,key,min,max){buildStepper(id,{min:min,max:max,value:killState[key],onChange:(v)=>{killState[key]=v;renderScreen4();}})}bk('killWoundsStepper','wounds',1,40);bk('killModelsStepper','models',1,20)}
  function buildBuffToggles(){let c=document.getElementById('buffToggles');if(!c)return;c.innerHTML='';[{key:'aoa',label:'AoA'},{key:'aod',label:'AoD'}].forEach(o=>{let l=document.createElement('label');l.className='buff-toggle';let i=document.createElement('input');i.type='checkbox';i.checked=killBuffs[o.key];i.onchange=()=>{killBuffs[o.key]=i.checked;renderScreen4();};l.appendChild(i);l.appendChild(document.createTextNode(o.label));c.appendChild(l)})}
  function buildDebuffToggles(){let c=document.getElementById('debuffToggles');if(!c)return;c.innerHTML='';[{key:'hit',label:'‑1 Hit'},{key:'wound',label:'‑1 Wound'},{key:'attacks',label:'‑1 Attack'}].forEach(o=>{let l=document.createElement('label');l.className='toggle-option';let i=document.createElement('input');i.type='checkbox';i.checked=killDebuffs[o.key];i.onchange=()=>{killDebuffs[o.key]=i.checked;renderScreen4();};l.appendChild(i);l.appendChild(document.createTextNode(o.label));c.appendChild(l)})}
  function clearBuffsDebuffs(){killBuffs={aoa:false,aod:false};killDebuffs={hit:false,wound:false,attacks:false};renderScreen4()}

  function renderScreen4(){
    buildKillSteppers();buildBuffToggles();buildDebuffToggles();
    let save=parseInt(document.getElementById('killSaveSelect').value),ward=parseInt(document.getElementById('killWardSelect').value),tw=killState.wounds*killState.models,deb=(killDebuffs.hit||killDebuffs.wound||killDebuffs.attacks)?killDebuffs:null,buff=(killBuffs.aoa||killBuffs.aod)?killBuffs:null,sc=document.getElementById('killStatsContainer'),cc=document.getElementById('killChartContainer'),bc=document.getElementById('killBreakdownContainer');
    if(profiles.length===0){sc.innerHTML='<p style="color:#888;">No profiles</p>';cc.innerHTML='';bc.innerHTML='';return;}
    let results=profiles.map(p=>{let d=computeProfileDistribution(p,save,ward,deb,buff);if(!d)return{name:p.name,color:p.color,pkFull:0,pkHalf:0,pkOne:0,expKills:0,bd:[]};let pkF=probGE(d,tw),pkH=probGE(d,Math.ceil(tw/2)),pkO=probGE(d,killState.wounds),expKills=0;for(let k=1;k<=killState.models;k++)expKills+=probGE(d,k*killState.wounds);let bd=[];for(let m=1;m<=killState.models;m++)bd.push({models:m,probAtLeast:probGE(d,m*killState.wounds)});return{name:p.name,color:p.color,pkFull:pkF,pkHalf:pkH,pkOne:pkO,expKills:expKills,bd}});
    sc.innerHTML=results.map(r=>`<div class="card" style="margin-bottom:6px;"><b style="color:${r.color}">${escHtml(r.name)}</b><div style="margin-top:3px;font-size:12px;">P(kill ≥1): <b class="pct">${formatProb(r.pkOne)}</b> | P(kill ≥half): <b class="pct">${formatProb(r.pkHalf)}</b> | P(kill all): <b class="pct">${formatProb(r.pkFull)}</b><br>Expected models killed: <b class="pct">${r.expKills.toFixed(2)}</b></div></div>`).join('');
    let mP=Math.max(...results.map(r=>r.pkFull),0.01),bh=results.map(r=>{let pct=(r.pkFull/mP)*100,label=r.pkFull>=0.99995?'💀':(r.pkFull*100).toFixed(2)+'%';return`<div class="bar-row"><span class="bar-label">${escHtml(r.name)}</span><div style="flex:1;background:#1a1a1a;border-radius:3px;height:16px;"><div class="bar-fill" style="width:${pct}%;background:${r.color};"></div></div><span style="font-size:12px;width:50px;">${label}</span></div>`}).join('');cc.innerHTML=`<h4 style="color:#c9a84c;margin-bottom:6px;">P(kill entire unit)</h4>${bh}`;
    if(results.length>0&&results[0].bd.length>0){let th='<table><tr><th>Models killed</th>'+results.map(r=>`<th>${escHtml(r.name)}</th>`).join('')+'</tr>';for(let i=0;i<killState.models;i++){th+=`<tr><td>≥${i+1}</td>`;results.forEach(r=>{let b=r.bd[i]||{probAtLeast:0},display=b.probAtLeast>=0.99995?'💀':(b.probAtLeast*100).toFixed(2)+'%';th+=`<td><b class="pct">${display}</b></td>`});th+='</tr>'}th+='</table>';bc.innerHTML='<div class="scroll-hint">← scroll table →</div>'+th}else{bc.innerHTML='<p style="color:#c0392b;">Invalid expression</p>'}
  }
  ['killSaveSelect','killWardSelect'].forEach(id=>{document.getElementById(id).onchange=()=>renderScreen4();});

  // ==================== NAVIGATION ====================
  document.querySelectorAll('.nav-btn').forEach(b=>{b.addEventListener('click',()=>{document.querySelectorAll('.nav-btn').forEach(x=>x.classList.remove('active'));b.classList.add('active');let s=b.dataset.screen;document.querySelectorAll('.screen').forEach(x=>x.classList.remove('active'));document.getElementById('screen'+s).classList.add('active');if(s==='2')renderScreen2();if(s==='3')renderScreen3();if(s==='4')renderScreen4()})});
  function fullInit(){initProfiles();renderProfiles();renderScreen2();renderScreen3();renderScreen4();}
  fullInit();
</script>
</body>
</html>

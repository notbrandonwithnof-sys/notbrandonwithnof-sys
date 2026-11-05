<!DOCTYPE html>
<html lang="en"><head><meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Educational Versions of Games</title>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:wght@400;600;800&display=swap" rel="stylesheet">
<style>
:root{--bg:#f6f0ed;--pn:#fff;--ln:#e2d2cd;--tx:#241a1b;--mu:#7a6a6a;--rd:#c42b32;--gd:#b07a14;--lt:#e6d3c9;--dk:#d01920;--ok:#1d8a4f;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
:root[data-theme=dark]{--bg:#0f0c0d;--pn:#1a1415;--ln:#3b2428;--tx:#f2eae7;--mu:#a39393;--rd:#e5484d;--gd:#e8b04a;--lt:#cdb3a8;--dk:#b01218;--ok:#4ad0a0}
@media(prefers-color-scheme:dark){:root:not([data-theme=light]){--bg:#0f0c0d;--pn:#1a1415;--ln:#3b2428;--tx:#f2eae7;--mu:#a39393;--rd:#e5484d;--gd:#e8b04a;--lt:#cdb3a8;--dk:#b01218;--ok:#4ad0a0}}
*{box-sizing:border-box}html,body{margin:0}body{background:var(--bg);color:var(--tx);font-family:'Bricolage Grotesque',system-ui,sans-serif;min-height:100%}
.hide{display:none!important}
header{display:flex;flex-wrap:wrap;gap:.6rem;align-items:center;justify-content:space-between;padding:.8rem 1rem;border-bottom:1px solid var(--ln)}
h1{font-size:1.25rem;font-weight:800;margin:0;color:var(--rd)}h3{margin:0 0 .5rem;font-size:.95rem}
.pill{border:1px solid var(--ln);background:var(--pn);border-radius:10px;padding:.35rem .6rem;font-size:.8rem}.pill b{color:var(--gd)}
.bar{display:flex;gap:.4rem;flex-wrap:wrap}
button{font:inherit;cursor:pointer}.b{background:var(--pn);color:var(--tx);border:1px solid var(--ln);border-radius:10px;padding:.4rem .7rem;font-size:.8rem;font-weight:600}.b:hover{border-color:var(--rd)}.b.pr{background:var(--rd);border-color:var(--rd);color:#fff}
.av{width:36px;height:36px;border-radius:50%;background:var(--ok);color:#fff;border:0;font-weight:800}
main{display:grid;grid-template-columns:250px minmax(0,1fr) 230px;gap:1rem;max-width:1200px;margin:0 auto;padding:1rem}
@media(max-width:900px){main{grid-template-columns:1fr}}
.card{background:var(--pn);border:1px solid var(--ln);border-radius:14px;padding:.9rem;margin-bottom:1rem}
.mid{display:flex;flex-direction:column;gap:.7rem;align-items:center}.status{width:100%;max-width:560px;text-align:center;font-weight:600;padding:.5rem;border:1px solid var(--ln);border-radius:10px;background:var(--pn)}
.board{width:100%;max-width:560px}.g8{display:grid;grid-template-columns:repeat(8,minmax(0,1fr));border-radius:10px;overflow:hidden;border:2px solid var(--dk)}
.sq{display:grid;place-items:center;aspect-ratio:1;cursor:pointer;position:relative;min-width:0;overflow:hidden;container-type:size}.l{background:var(--lt)}.d{background:var(--dk)}
.sel{outline:3px solid var(--gd);outline-offset:-3px}.dot::after{content:"";width:28%;height:28%;border-radius:50%;background:#e8b04acc;position:absolute}.cap{box-shadow:inset 0 0 0 4px #e8b04a}.last{filter:brightness(1.18)}.hint{box-shadow:inset 0 0 0 4px #2fc08a}.chk{background:radial-gradient(#ff5a5a,var(--dk))!important}
.pc{font-size:clamp(1rem,7vw,3rem);font-size:68cqw;line-height:1}.pc.w{color:#fff7f0;text-shadow:0 0 2px #000,0 1px 3px #000}.pc.b{color:#17100f;text-shadow:0 0 2px #fff7f0}
.ck{width:72%;height:72%;border-radius:50%;display:grid;place-items:center}.ck.w{background:#f1e6de;border:3px solid #fff;color:#7a2f33}.ck.b{background:#1b1213;border:3px solid #55353a;color:#e8b04a}
.mn{display:grid;grid-template-columns:1fr 6fr 1fr;gap:.5rem;aspect-ratio:2.6/1;padding:.6rem;background:var(--dk);border-radius:14px}
.st{display:grid;place-content:center;text-align:center;background:#0005;border-radius:40px;font-size:1.8rem;font-weight:800;color:#fff}.st small{font-size:.65rem;font-weight:600}
.pits{display:grid;grid-template-columns:repeat(6,1fr);gap:.5rem}.pit{border:0;border-radius:45%;background:var(--lt);color:#241a1b;font-size:1.3rem;font-weight:800;cursor:default}.pit.on{outline:3px solid var(--gd);cursor:pointer}.pit.hint{box-shadow:0 0 0 4px #2fc08a}.pit.last{filter:brightness(1.15)}
.evalw{width:100%;max-width:560px;font-size:.75rem;font-weight:600}.lab{display:flex;justify-content:space-between}.evb{height:10px;border-radius:6px;background:#222;overflow:hidden}.evb i{display:block;height:100%;width:50%;background:#f4ece8;transition:width .3s}
#log{max-height:420px;overflow:auto;font-size:.8rem;display:grid;gap:.3rem}.mv{display:flex;gap:.5rem;padding:.3rem .5rem;border-radius:8px;border:1px solid var(--ln)}.mv b{color:var(--mu);min-width:1.6rem}.mv.b{background:#0002}
.prow{font-size:.75rem;margin-bottom:.5rem}.prow div:first-child{display:flex;justify-content:space-between}.tr{height:7px;background:var(--ln);border-radius:5px;overflow:hidden}.tr i{display:block;height:100%;background:var(--rd);width:0}
.modal{position:fixed;inset:0;background:#000b;display:flex;align-items:center;justify-content:center;padding:1rem;z-index:9}
.dlg{background:var(--pn);border:1px solid var(--ln);border-radius:16px;padding:1.2rem;max-width:480px;width:100%;max-height:90vh;overflow:auto;display:grid;gap:.8rem}
.dlg h2{margin:0;color:var(--rd)}.dlg label{font-size:.8rem;font-weight:600;color:var(--mu)}
.seg{display:flex;gap:.4rem;flex-wrap:wrap}.seg button{flex:1;padding:.5rem;border-radius:10px;border:1px solid var(--ln);background:var(--bg);color:var(--tx);font-weight:600}.seg button.on{border:2px solid var(--rd);color:var(--rd)}
input[type=text],input[type=password]{width:100%;padding:.6rem;border-radius:10px;border:1px solid var(--ln);background:var(--bg);color:var(--tx);font:inherit}
.opt{display:block;width:100%;text-align:left;padding:.6rem;border-radius:10px;border:1px solid var(--ln);background:var(--bg);color:var(--tx);margin-bottom:.4rem}.opt.on{border:2px solid var(--rd)}
.ex{padding:.6rem;border-radius:10px;font-size:.85rem;border:1px solid}.ex.ok{border-color:var(--ok);color:var(--ok)}.ex.er,.er{border-color:var(--rd);color:var(--rd)}.ok{color:var(--ok)}
.g3{display:grid;grid-template-columns:repeat(3,1fr);gap:.5rem;text-align:center;font-size:.8rem}.g3 b{display:block;font-size:1.2rem}
.lr{display:grid;grid-template-columns:2rem 1fr auto;gap:.5rem;padding:.4rem .5rem;border:1px solid var(--ln);border-radius:8px;font-size:.85rem}
#toast{position:fixed;top:calc(12px + env(safe-area-inset-top,0px));left:50%;transform:translateX(-50%);background:var(--rd);color:#fff;padding:.6rem 1rem;border-radius:10px;font-weight:700;z-index:20}
@media(prefers-reduced-motion:reduce){*{transition:none!important}}
</style><style>
.av.owner{background:linear-gradient(135deg,#f9e08b,#e8b04a 55%,#b07a14);color:#241a1b;box-shadow:0 0 0 2px #fff8dc,0 0 0 4px #e8b04a,0 0 14px #e8b04acc;font-size:1.15rem;display:grid;place-items:center;padding:0}
#ownerBadge{background:linear-gradient(135deg,#f9e08b,#e8b04a);color:#241a1b;border-color:#e8b04a}#ownerBadge b{color:#241a1b}
</style>
</head><body>
<header>
<h1>Educational Versions of Games</h1>
<span class="pill" id="badge"></span>
<span class="pill" id="eloB">AI rating <b id="hElo">1200</b></span>
<span class="pill">White 🔥<b id="sw">0</b> <span id="rw"></span> &nbsp; Black 🔥<b id="sb">0</b> <span id="rb"></span></span>
<span class="pill">Score <b id="score">0</b> &nbsp; Accuracy <b id="acc">100%</b></span>
<div class="bar">
<button class="b" id="lb">🏆 Leaderboard</button><button class="av" id="acct" title="Account">👤</button>
<button class="b" id="coachB">Coach: on</button><button class="b" id="snd">Sound: on</button>
<button class="b pr" id="setup">Change game</button><button class="b" id="rev">Reverse</button><button class="b" id="reset">Reset</button>
<button class="b" id="adminB" title="Admin">⚙️ Admin</button>
</div></header>
<main>
<aside><section class="card"><h3>Performance by subject</h3><div id="perf"></div></section>
<section class="card" id="coachP"><h3>Gambit coach</h3><button class="b" id="ask">Ask for advice</button><p id="coachT" style="font-size:.85rem;color:var(--mu)">Ask for advice to see a suggested move.</p></section></aside>
<section class="mid"><div class="status" id="status"></div><div class="board" id="board"></div>
<div class="evalw"><div class="lab"><span>White</span><span id="evT">+0.0</span><span>Black</span></div><div class="evb"><i id="evW"></i></div></div></section>
<aside class="card"><h3>Move log <small id="mc" style="color:var(--mu)"></small></h3><div id="log"></div></aside>
</main>

<div class="modal" id="m-setup"><div class="dlg">
<h2>Educational Versions of Games</h2>
<label>Game</label><div class="seg" data-k="v"><button data-v="mancala" class="on">Mancala</button><button data-v="chess">Chess</button><button data-v="checkers">Checkers</button></div>
<label>Subject</label><div class="seg" data-k="subj"><button data-v="history" class="on">History</button><button data-v="math">Math</button><button data-v="ela">ELA</button><button data-v="science">Science</button></div>
<label>Grade level</label><div class="seg" data-k="grade"><button data-v="elem">Elementary</button><button data-v="middle" class="on">Middle</button><button data-v="high">High</button></div>
<label>Opponent</label><div class="seg" data-k="mode"><button data-v="ai" class="on">Vs AI</button><button data-v="pvp">2 players</button></div>
<label>Play style</label><div class="seg" data-k="edu"><button data-v="1" class="on">Educational (answer to move)</button><button data-v="0">Classic</button></div>
<div id="eloP"><label>AI rating: <b id="eloV">1200</b> <span id="eloT">Intermediate</span></label><input type="range" id="elo" min="400" max="3000" step="50" value="1200" style="width:100%"></div>
<div class="bar"><button class="b" id="mAcc">Account</button><button class="b" id="mLb">Leaderboard</button><button class="b" id="mAdmin">Admin</button></div>
<button class="b pr" id="go" style="padding:.7rem">Start game</button></div></div>

<div class="modal hide" id="m-q"><div class="dlg"><div class="pill" id="qsub"></div><h3 id="qt" style="font-size:1.05rem"></h3><div id="qo"></div><div id="qx" class="hide"></div><button class="b pr" id="qgo" disabled>Submit answer</button></div></div>
<div class="modal hide" id="m-promo"><div class="dlg"><h2>Promote your pawn</h2><div class="seg"><button data-p="Q">♛</button><button data-p="R">♜</button><button data-p="B">♝</button><button data-p="N">♞</button></div></div></div>
<div class="modal hide" id="m-over"><div class="dlg" style="text-align:center"><h2 id="ot"></h2><p id="om" style="margin:0;color:var(--mu)"></p>
<div class="g3"><div>Score<b id="os"></b></div><div>White rank<b id="orw" style="font-size:.8rem"></b></div><div>Black rank<b id="orb" style="font-size:.8rem"></b></div></div>
<div class="g3" id="oq"></div><button class="b pr" id="again">Play again</button></div></div>
<div class="modal hide" id="m-pin"><div class="dlg"><h2 id="pinT"></h2><input type="password" id="pin" maxlength="20" placeholder="Passcode"><div id="pinE" class="er" style="font-size:.8rem"></div><div class="bar"><button class="b" id="pinNo">Cancel</button><button class="b pr" id="pinOk">Continue</button></div></div></div>
<div class="modal hide" id="m-acc"><div class="dlg"><h2>Academy account</h2>
<div id="av-out"><label>Username</label><input type="text" id="u" maxlength="20" autocomplete="username"><label>Password (6+ characters)</label><input type="password" id="pw" autocomplete="current-password"><div id="am" style="font-size:.8rem;margin:.4rem 0"></div><div class="bar"><button class="b" id="login">Log in</button><button class="b pr" id="reg">Create account</button></div></div>
<div id="av-in" class="hide"><p id="who" style="font-weight:800"></p><label>Profile picture</label><div class="seg" id="avs" style="margin-bottom:.6rem"></div><label>Your account code</label><textarea id="myCode" readonly rows="3" style="width:100%;padding:.6rem;border-radius:10px;border:1px solid var(--ln);background:var(--bg);color:var(--tx);font:inherit;font-size:.7rem;word-break:break-all;resize:none"></textarea><small style="color:var(--mu)">Holds your score, wins, losses, draws and quiz stats. Your account syncs automatically to the shared online leaderboard when available. <span id="codeAge"></span></small><div class="bar"><button class="b" id="copyCode">Copy code</button><button class="b" id="logout">Sign out</button></div></div>
<button class="b" id="accX">Close (guests can play too)</button></div></div>
<div class="modal hide" id="m-lb"><div class="dlg"><h2>Leaderboard</h2><p style="margin:0;font-size:.8rem;color:var(--mu)">Players who created accounts in this browser.</p><div id="lbl" style="display:grid;gap:.4rem"></div><small style="color:var(--mu)">Player accounts are collected automatically from the shared online leaderboard when available.</small><small id="lbNext" style="color:var(--mu)"></small><button class="b" id="lbX">Close</button></div></div>
<div class="modal hide" id="m-admin"><div class="dlg">
<h2>Admin panel</h2>
<div id="admin-login">
<label>Admin password</label>
<input type="password" id="adminPw" maxlength="40" placeholder="Enter password" autocomplete="off">
<div id="adminErr" class="er" style="font-size:.8rem;min-height:1.2em"></div>
<div class="bar"><button class="b" id="adminCancel">Cancel</button><button class="b pr" id="adminGo">Unlock</button></div>
</div>
<div id="admin-panel" class="hide">
<p style="margin:0;font-size:.85rem;color:var(--mu)">Session unlocked. Changes apply to this browser only.</p>
<label style="margin-top:.2rem">Edit account</label>
<select id="adPick" style="width:100%;padding:.5rem;border-radius:10px;border:1px solid var(--ln);background:var(--bg);color:var(--tx);font:inherit;margin:.3rem 0 .6rem">
<option value="">— Current session —</option>
</select>
<div class="g3" style="margin:.4rem 0">
<div>Score<br><b id="adScore">0</b></div>
<div>Wins<br><b id="adWins">0</b></div>
<div>Accounts<br><b id="adAccs">0</b></div>
</div>
<label style="margin-top:.4rem">Give / Take</label>
<div style="display:grid;gap:.5rem;margin:.4rem 0 .8rem">
  <div style="display:flex;gap:.4rem;align-items:center;flex-wrap:wrap">
    <span style="min-width:5.5rem;font-size:.85rem;font-weight:600">LB points</span>
    <input type="number" id="adAmtPts" value="50" min="1" max="99999" style="width:5rem;padding:.4rem;border-radius:8px;border:1px solid var(--ln);background:var(--bg);color:var(--tx);font:inherit">
    <button class="b" id="adGivePts">+ Give</button>
    <button class="b" id="adTakePts">− Take</button>
  </div>
  <div style="display:flex;gap:.4rem;align-items:center;flex-wrap:wrap">
    <span style="min-width:5.5rem;font-size:.85rem;font-weight:600">Wins</span>
    <input type="number" id="adAmtW" value="1" min="1" max="100" style="width:5rem;padding:.4rem;border-radius:8px;border:1px solid var(--ln);background:var(--bg);color:var(--tx);font:inherit">
    <button class="b" id="adGiveW">+ Give</button>
    <button class="b" id="adTakeW">− Take</button>
  </div>
</div>
<label>Quick actions</label>
<button class="opt" id="adOpenLb">View / refresh leaderboard</button>
<button class="opt" id="adResetScore">Reset selected score & wins</button>
<button class="opt" id="adResetStats">Reset subject accuracy stats</button>
<button class="opt" id="adDeleteAcc" style="border-color:var(--rd);color:var(--rd)">Delete selected account</button>
<button class="opt" id="adClearAcc">Clear all local accounts & leaderboard</button>
<button class="opt" id="adClearPin">Clear undo passcode</button>
<button class="opt" id="adForceClassic">Force classic mode (no questions)</button>
<button class="opt" id="adForceEdu">Force educational mode</button>
<div class="bar" style="margin-top:.8rem">
<button class="b" id="adminLock">Lock panel</button>
<button class="b pr" id="adminX">Close</button>
</div>
</div>
</div></div>
<div id="toast" class="hide"></div>

<script>
const $=i=>document.getElementById(i),sh=a=>{a=a.slice();for(let i=a.length;i>1;){const j=Math.random()*i--|0;[a[i],a[j]]=[a[j],a[i]]}return a},oth=t=>t==='w'?'b':'w',R=a=>a[Math.random()*a.length|0];
const esc=s=>String(s).replace(/[&<>"']/g,c=>'&#'+c.charCodeAt(0)+';'),show=i=>$(i).classList.remove('hide'),hide=i=>$(i).classList.add('hide');
const LS={get(k,d){try{return JSON.parse(localStorage.getItem(k))??d}catch{return d}},set(k,v){try{localStorage.setItem(k,JSON.stringify(v))}catch{}}};
async function hash(s){try{const h=await crypto.subtle.digest('SHA-256',new TextEncoder().encode('sa:'+s));return[...new Uint8Array(h)].map(x=>x.toString(16).padStart(2,'0')).join('')}catch{return btoa(s)}}
let AC;function beep(f,d=.1,ty='triangle'){if(!S.sound)return;try{AC=AC||new(window.AudioContext||window.webkitAudioContext)();const o=AC.createOscillator(),g=AC.createGain();o.type=ty;o.frequency.value=f;g.gain.setValueAtTime(.12,AC.currentTime);g.gain.exponentialRampToValueAtTime(.001,AC.currentTime+d);o.connect(g);g.connect(AC.destination);o.start();o.stop(AC.currentTime+d)}catch{}}
function toast(t){const e=$('toast');e.textContent=t;show('toast');setTimeout(()=>hide('toast'),1500)}

const S={v:'mancala',subj:'history',grade:'middle',mode:'ai',edu:1,elo:1200,coach:1,sound:1,user:null,score:0,rec:{w:0,l:0,d:0,g:0},streak:{w:0,b:0,mw:0,mb:0},stats:{history:{correct:0,total:0},math:{correct:0,total:0},ela:{correct:0,total:0},science:{correct:0,total:0}},admin:false};

/* ---------- Question bank: [question, options, answerIndex, explanation] (objects {q,options,a,exp} also work) ---------- */
const QB={
elem:{history:[["Who was the first U.S. President?",["George Washington","Abraham Lincoln","John Adams","Thomas Jefferson"],0,"George Washington served from 1789 to 1797."],["Which ship carried the Pilgrims to America in 1620?",["Santa Maria","Mayflower","Endeavour","Titanic"],1,"The Mayflower landed near Plymouth, Massachusetts."],["Who guided enslaved people to freedom on the Underground Railroad?",["Betsy Ross","Clara Barton","Harriet Tubman","Amelia Earhart"],2,"Harriet Tubman made many trips to lead people north."]],
ela:[["Which word is a noun?",["Quickly","Happiness","Run","Bright"],1,"Happiness names an idea or feeling."],["What is the plural of 'child'?",["Childs","Childen","Children","Childrens"],2,"Child has an irregular plural: children."],["Which word is the opposite of 'giant'?",["Huge","Tiny","Tall","Large"],1,"Tiny is the antonym of giant."]],
science:[["What process do plants use to make food from sunlight?",["Respiration","Photosynthesis","Evaporation","Digestion"],1,"Photosynthesis turns light, water and carbon dioxide into sugar."],["Which planet is called the Red Planet?",["Venus","Jupiter","Mars","Saturn"],2,"Iron oxide gives Mars its red color."],["How many legs does an insect have?",["4","6","8","10"],1,"Insects have six legs."]]},
middle:{history:[["What event started World War I in 1914?",["Attack on Pearl Harbor","Assassination of Archduke Franz Ferdinand","Invasion of Poland","Treaty of Versailles"],1,"The assassination in Sarajevo set off the war."],["Which trade route linked China to the Mediterranean?",["Royal Road","Silk Road","Spice Route","Amber Road"],1,"The Silk Road carried goods and ideas for centuries."],["Which amendment gave women the right to vote?",["13th","15th","19th","21st"],2,"The 19th Amendment was ratified in 1920."]],
ela:[["'The wind whispered through the trees' is an example of:",["Simile","Hyperbole","Personification","Alliteration"],2,"The wind is given a human action."],["What is the theme of a story?",["The setting","The central message","The narrator","The plot summary"],1,"Theme is the underlying message or lesson."],["Which sentence contains a metaphor?",["Time is a thief.","She ran fast as a cheetah.","Boom!","I could eat a horse."],0,"A metaphor compares directly without 'like' or 'as'."]],
science:[["Which organelle is the powerhouse of the cell?",["Nucleus","Ribosome","Mitochondria","Vacuole"],2,"Mitochondria produce ATP."],["What is the pH of pure water?",["0","7","10","14"],1,"7 is neutral."],["Newton's First Law is also called the law of:",["Gravity","Inertia","Action and reaction","Acceleration"],1,"Objects keep their motion unless a force acts."]]},
high:{history:[["Which 1648 treaties ended the Thirty Years' War?",["Peace of Westphalia","Treaty of Utrecht","Congress of Vienna","Treaty of Tordesillas"],0,"Westphalia helped establish state sovereignty."],["Which case established judicial review in 1803?",["Marbury v. Madison","McCulloch v. Maryland","Dred Scott v. Sandford","Brown v. Board"],0,"Chief Justice Marshall wrote the opinion."],["Which 1823 doctrine warned Europe against new colonies in the Americas?",["Truman Doctrine","Monroe Doctrine","Marshall Plan","Open Door Policy"],1,"President Monroe issued it."]],
ela:[["Which rhetorical appeal targets credibility?",["Pathos","Logos","Ethos","Kairos"],2,"Ethos appeals to character and authority."],["Who wrote Macbeth?",["Marlowe","Shakespeare","Milton","Chaucer"],1,"Macbeth is a Shakespeare tragedy."],["A 'foil' character is one who:",["Is the main villain","Contrasts with another to highlight traits","Narrates the story","Appears once"],1,"Foils sharpen our view of another character."]],
science:[["What is the chemical formula for glucose?",["CO2","H2O2","C6H12O6","CH4"],2,"Six carbon, twelve hydrogen, six oxygen atoms."],["Which change turns a solid directly into a gas?",["Sublimation","Deposition","Condensation","Melting"],0,"Dry ice sublimes."],["About how fast does light travel in a vacuum?",["3,000 km/s","30,000 km/s","300,000 km/s","3,000,000 km/s"],2,"Roughly 300,000 km per second."]]}};
function numOpts(ans,f=x=>x){const s=new Set([ans]);while(s.size<4){const v=ans+(Math.random()<.5?-1:1)*Math.ceil(Math.random()*Math.max(3,Math.abs(ans)*.2));if(ans<0||v>=0)s.add(v)}const o=sh([...s]);return{options:o.map(f),a:o.indexOf(ans)}}
function mathQ(g){const a=2+Math.random()*8|0,b=2+Math.random()*10|0,x=2+Math.random()*10|0,k=R([0,1,2]);let q,ans,e,f;
if(g==='elem'){if(k===0){q=`What is ${a} × ${b}?`;ans=a*b;e=`${a} × ${b} = ${ans}.`}else if(k===1){q=`What is ${a*b+x} − ${x}?`;ans=a*b;e=`${a*b+x} − ${x} = ${ans}.`}else{q=`What is ${a*b} ÷ ${b}?`;ans=a;e=`${a} × ${b} = ${a*b}.`}}
else if(g==='middle'){if(k===0){q=`Solve for x: ${a}x + ${b} = ${a*x+b}`;ans=x;f=n=>'x = '+n;e=`${a}x = ${a*x}, so x = ${x}.`}else if(k===1){const p=(1+Math.random()*9|0)*10,v=(1+Math.random()*20|0)*10;q=`What is ${p}% of ${v}?`;ans=p*v/100;e=`${p}/100 × ${v} = ${ans}.`}else{const n=a+2;q=`What is the square root of ${n*n}?`;ans=n;e=`${n} × ${n} = ${n*n}.`}}
else{if(k===0){const n=b%3+2;q=`What is the derivative of ${a}x^${n}?`;ans=a*n;f=v=>v+(n>2?'x^'+(n-1):'x');e=`Power rule: ${n} × ${a} = ${ans}.`}else if(k===1){const n=b%5+2;q=`Solve for x: log₂(x) = ${n}`;ans=2**n;e=`2^${n} = ${ans}.`}else{q=`What is the sum of the roots of x² − ${a+b}x + ${a*b} = 0?`;ans=a+b;e=`The roots are ${a} and ${b}; their sum is ${a+b}.`}}
return{q,...numOpts(ans,f),exp:e}}
function pickQ(){let q;if(S.subj==='math')q=mathQ(S.grade);else{q=R((QB[S.grade]||QB.middle)[S.subj]||QB.middle.history);if(Array.isArray(q))q={q:q[0],options:q[1],a:q[2],exp:q[3]}}
const ix=sh(q.options.map((_,i)=>i));return{q:q.q,options:ix.map(i=>q.options[i]),a:ix.indexOf(q.a),exp:q.exp}}

/* ---------- Shared helpers ---------- */
const DR=[[-1,0],[1,0],[0,-1],[0,1]],DD=[[-1,-1],[-1,1],[1,-1],[1,1]],DN=[[-2,-1],[-2,1],[-1,-2],[-1,2],[1,-2],[1,2],[2,-1],[2,1]],DK=DR.concat(DD),ok=(r,c)=>r>=0&&r<8&&c>=0&&c<8,sq=i=>'abcdefgh'[i&7]+(8-(i>>3));

/* ---------- Chess: full rules (castling, en passant, promotion) ---------- */
function cInit(){const b=Array(64).fill(null),k='RNBQKBNR';for(let c=0;c<8;c++){b[c]='b'+k[c];b[8+c]='bP';b[48+c]='wP';b[56+c]='w'+k[c]}return{b,t:'w',cr:{wK:1,wQ:1,bK:1,bQ:1},ep:-1}}
function att(b,s,by){const r=s>>3,c=s&7,pr=by==='w'?r+1:r-1;
for(const dc of[-1,1])if(ok(pr,c+dc)&&b[pr*8+c+dc]===by+'P')return 1;
for(const[a,d]of DN)if(ok(r+a,c+d)&&b[(r+a)*8+c+d]===by+'N')return 1;
for(const[a,d]of DK)if(ok(r+a,c+d)&&b[(r+a)*8+c+d]===by+'K')return 1;
for(const[a,d]of DK){let y=r+a,x=c+d;while(ok(y,x)){const q=b[y*8+x];if(q){if(q[0]===by&&(q[1]==='Q'||q[1]===(a&&d?'B':'R')))return 1;break}y+=a;x+=d}}return 0}
function cGen(p){const b=p.b,t=p.t,o=oth(t),M=[];
for(let i=0;i<64;i++){const x=b[i];if(!x||x[0]!==t)continue;const ty=x[1],r=i>>3,c=i&7;
const add=(to,e)=>{if(ty==='P'&&(to>>3)===(t==='w'?0:7))for(const q of'QRBN')M.push({f:i,t:to,pr:q});else M.push({f:i,t:to,...e})};
if(ty==='P'){const d=t==='w'?-1:1,r1=r+d;if(r1<0||r1>7)continue;
if(!b[r1*8+c]){add(r1*8+c);if(r===(t==='w'?6:1)&&!b[(r+2*d)*8+c])add((r+2*d)*8+c)}
for(const dc of[-1,1]){if(c+dc<0||c+dc>7)continue;const to=r1*8+c+dc;if(b[to]&&b[to][0]===o)add(to);else if(to===p.ep)add(to,{ep:1})}}
else if(ty==='N'||ty==='K'){for(const[a,d]of ty==='N'?DN:DK)if(ok(r+a,c+d)){const to=(r+a)*8+c+d;if(!b[to]||b[to][0]===o)add(to)}
if(ty==='K'&&i===(t==='w'?60:4)&&!att(b,i,o)){
if(p.cr[t+'K']&&!b[i+1]&&!b[i+2]&&b[i+3]===t+'R'&&!att(b,i+1,o)&&!att(b,i+2,o))M.push({f:i,t:i+2,cs:'K'});
if(p.cr[t+'Q']&&!b[i-1]&&!b[i-2]&&!b[i-3]&&b[i-4]===t+'R'&&!att(b,i-1,o)&&!att(b,i-2,o))M.push({f:i,t:i-2,cs:'Q'})}}
else for(const[a,d]of ty==='R'?DR:ty==='B'?DD:DK){let y=r+a,z=c+d;while(ok(y,z)){const to=y*8+z;if(b[to]){if(b[to][0]===o)add(to);break}add(to);y+=a;z+=d}}}
return M}
function cApply(p,m){const b=p.b.slice(),x=b[m.f],t=p.t,cr={...p.cr};let ep=-1;
b[m.t]=m.pr?t+m.pr:x;b[m.f]=null;if(m.ep)b[m.t+(t==='w'?8:-8)]=null;
if(x[1]==='P'&&Math.abs(m.t-m.f)===16)ep=(m.f+m.t)/2;
if(m.cs){const w=t==='w'?56:0;if(m.cs==='K'){b[w+5]=b[w+7];b[w+7]=null}else{b[w+3]=b[w];b[w]=null}}
if(x[1]==='K')cr[t+'K']=cr[t+'Q']=0;const cor={0:'bQ',7:'bK',56:'wQ',63:'wK'};if(cor[m.f])cr[cor[m.f]]=0;if(cor[m.t])cr[cor[m.t]]=0;
return{b,t:oth(t),cr,ep}}
const cLegal=p=>cGen(p).filter(m=>{const n=cApply(p,m);return!att(n.b,n.b.indexOf(p.t+'K'),n.t)});
const PV={P:100,N:320,B:330,R:500,Q:900,K:0};
function cEval(p){let s=0;for(let i=0;i<64;i++){const x=p.b[i];if(!x)continue;const r=i>>3,c=i&7;let v=PV[x[1]];if(x[1]!=='K')v+=(3.5-Math.max(Math.abs(r-3.5),Math.abs(c-3.5)))*6;if(x[1]==='P')v+=(x[0]==='w'?6-r:r-1)*5;s+=x[0]==='w'?v:-v}return s}
const cTerm=p=>att(p.b,p.b.indexOf(p.t+'K'),oth(p.t))?(p.t==='w'?-1e5:1e5):0;

/* ---------- Checkers: forced captures, multi-jumps, kings ---------- */
function kInit(){const b=Array(64).fill(null);for(let i=0;i<64;i++){const r=i>>3,c=i&7;if((r+c)%2){if(r<3)b[i]='b';else if(r>4)b[i]='w'}}return{b,t:'w'}}
function kMoves(p){const t=p.t,J=[],St=[];
for(let i=0;i<64;i++){const x=p.b[i];if(!x||x.toLowerCase()!==t)continue;const kg=x!==t,dirs=kg?DD:t==='w'?[[-1,-1],[-1,1]]:[[1,-1],[1,1]];
const jump=(cur,bd,path,caps,k)=>{let more=0;for(const[a,d]of k?DD:dirs){const r=(cur>>3)+a,c=(cur&7)+d,r2=r+a,c2=c+d;if(!ok(r2,c2))continue;const m=r*8+c,l=r2*8+c2,y=bd[m];
if(y&&y.toLowerCase()!==t&&!bd[l]){more=1;const nb=bd.slice();nb[m]=null;if(!k&&r2===(t==='w'?0:7))J.push({f:i,t:l,path:[...path,l],caps:[...caps,m]});else jump(l,nb,[...path,l],[...caps,m],k)}}
if(!more&&caps.length)J.push({f:i,t:cur,path,caps})};
const b0=p.b.slice();b0[i]=null;jump(i,b0,[i],[],kg);
for(const[a,d]of dirs){const r=(i>>3)+a,c=(i&7)+d;if(ok(r,c)&&!p.b[r*8+c])St.push({f:i,t:r*8+c})}}
return J.length?J:St}
function kApply(p,m){const b=p.b.slice();let x=b[m.f];b[m.f]=null;(m.caps||[]).forEach(s=>b[s]=null);if((m.t>>3)===(p.t==='w'?0:7))x=x.toUpperCase();b[m.t]=x;return{b,t:oth(p.t)}}
function kEval(p){let s=0;for(let i=0;i<64;i++){const x=p.b[i];if(!x)continue;const w=x.toLowerCase()==='w',v=(x===x.toUpperCase()?170:100)+(x===x.toUpperCase()?0:(w?7-(i>>3):i>>3)*3);s+=w?v:-v}return s}
const kTerm=p=>p.t==='w'?-1e5:1e5;

/* ---------- Mancala (Kalah): sowing, captures, extra turns, end sweep ---------- */
const mInit=()=>({b:[4,4,4,4,4,4,0,4,4,4,4,4,4,0],t:'w'});
function mMoves(p){const o=p.t==='w'?0:7,r=[];for(let i=o;i<o+6;i++)if(p.b[i])r.push({f:i,t:i});return r}
function mApply(p,m){const b=p.b.slice(),t=p.t,st=t==='w'?6:13,sk=t==='w'?13:6;let n=b[m.f],i=m.f,nt=oth(t);b[m.f]=0;
while(n--){i=(i+1)%14;if(i===sk)i=(i+1)%14;b[i]++}
if(i===st)nt=t;else if((t==='w'?i<6:i>6&&i<13)&&b[i]===1&&b[12-i]){b[st]+=b[i]+b[12-i];b[i]=b[12-i]=0}
if(b.slice(0,6).every(x=>!x)||b.slice(7,13).every(x=>!x))for(let k=0;k<6;k++){b[6]+=b[k];b[k]=0;b[13]+=b[7+k];b[7+k]=0}
return{b,t:nt}}
const sum=(b,a,z)=>b.slice(a,z).reduce((x,y)=>x+y,0),mEval=p=>(p.b[6]-p.b[13])*100+(sum(p.b,0,6)-sum(p.b,7,13))*10,mTerm=p=>(p.b[6]-p.b[13])*1e3;

const G={chess:{init:cInit,moves:cLegal,apply:cApply,eval:cEval,term:cTerm},checkers:{init:kInit,moves:kMoves,apply:kApply,eval:kEval,term:kTerm},mancala:{init:mInit,moves:mMoves,apply:mApply,eval:mEval,term:mTerm}};

/* ---------- AI: alpha-beta search; depth and blunder rate scale with rating ---------- */
function search(g,p,d,a,b){if(!d)return g.eval(p);const ms=g.moves(p);if(!ms.length){const T=g.term(p);return T+(T>0?d:T<0?-d:0)}
const mx=p.t==='w';let best=mx?-Infinity:Infinity;
for(const m of ms){const v=search(g,g.apply(p,m),d-1,a,b);if(mx){if(v>best)best=v;if(v>a)a=v}else{if(v<best)best=v;if(v<b)b=v}if(a>=b)break}return best}
function rank(p,d){const g=G[S.v],mx=p.t==='w';return sh(g.moves(p)).map(m=>[m,search(g,g.apply(p,m),d-1,-1e9,1e9)]).sort((a,b)=>mx?b[1]-a[1]:a[1]-b[1])}
const depth=()=>S.v==='chess'?(S.elo<1100?1:S.elo<2200?2:3):Math.min(6,2+((S.elo-400)/520|0));
const same=(a,b)=>a.f===b.f&&a.t===b.t&&a.pr===b.pr;
function nt(p,m){const x=p.b[m.f];if(S.v==='mancala')return'Pit '+(m.f%7+1);if(S.v==='checkers')return m.path?m.path.map(sq).join('x'):sq(m.f)+'-'+sq(m.t);if(m.cs)return m.cs==='K'?'O-O':'O-O-O';return(x[1]==='P'?'':x[1])+sq(m.f)+(p.b[m.t]||m.ep?'x':'-')+sq(m.t)+(m.pr?'='+m.pr:'')}

/* ---------- Game flow ---------- */
function initGame(){clearTimeout(S.timer);Object.assign(S,{pos:G[S.v].init(),sel:null,hl:[],hist:[],snaps:[],last:null,hint:null,over:false,busy:false,q:{w:{good:0,bad:0},b:{good:0,bad:0}}});hide('m-over');$('coachT').textContent='Ask for advice to see a suggested move.';after()}
const snap=()=>JSON.parse(JSON.stringify({pos:S.pos,hist:S.hist,q:S.q,last:S.last}));
function commit(m){const p=S.pos,g=G[S.v],mv=p.t,r=rank(p,2),mine=r.find(a=>same(a[0],m)),diff=mv==='w'?r[0][1]-mine[1]:mine[1]-r[0][1];
S.q[mv][diff>=100?'bad':'good']++;S.snaps.push(snap());S.hist.push({t:mv,n:nt(p,m)});
const cap=S.v==='chess'?(p.b[m.t]||m.ep):m.caps;beep(cap?280:440,.1,cap?'square':'triangle');
S.last={f:m.f,t:S.v==='mancala'?m.f:m.t};S.sel=null;S.hl=[];S.hint=null;S.pos=g.apply(p,m);S.mover=mv;after()}
function after(){clearTimeout(S.timer);render();log();ev();stats();const p=S.pos,L=G[S.v].moves(p);
if(!L.length){end(p);return}
let t=S.mode==='ai'?(p.t==='w'?'Your turn':'Black is thinking…'):(p.t==='w'?'White':'Black')+"'s turn";
if(S.v==='chess'&&att(p.b,p.b.indexOf(p.t+'K'),oth(p.t))){t='Check! '+t;beep(700,.2,'sawtooth')}
if(S.v==='mancala'&&S.mover===p.t&&S.hist.length)t='Extra turn! '+t;
if(S.v==='checkers'&&L[0].caps)t='Capture required. '+t;
$('status').textContent=t;
if(S.mode==='ai'&&p.t==='b'){S.busy=true;S.timer=setTimeout(aiGo,450)}else S.busy=false;render()}
function aiGo(){if(S.over)return;const r=rank(S.pos,depth());let m=r[0][0];if(Math.random()<Math.max(0,(1500-S.elo)/1300))m=R(r)[0];S.busy=false;commit(m)}
function end(p){S.over=true;let w=null,msg;
if(S.v==='mancala'){const d=p.b[6]-p.b[13];w=d>0?'w':d<0?'b':null;msg=`Final seeds: White ${p.b[6]}, Black ${p.b[13]}.`}
else if(S.v==='chess'){const c=att(p.b,p.b.indexOf(p.t+'K'),oth(p.t));w=c?oth(p.t):null;msg=c?'Checkmate.':'Stalemate: no legal moves.'}
else{w=oth(p.t);msg=(p.t==='w'?'White':'Black')+' has no moves left.'}
if(w){
  S.streak[w]++;S.streak[oth(w)]=0;S.streak['m'+w]=Math.max(S.streak['m'+w],S.streak[w]);
  // Every win by the player = +1 leaderboard point
  // Vs AI: player is White. Vs PVP: either color winning counts for the logged-in account.
  const playerWon = (S.mode==='ai' && w==='w') || (S.mode==='pvp');
  if(playerWon){S.score+=1}
  if(playerWon)S.rec.w++;else S.rec.l++;
  save();
}else S.rec.d++;
S.rec.g++;
$('ot').textContent=w?(w==='w'?'White':'Black')+' wins':'Draw';$('om').textContent=msg;$('os').textContent=S.score;$('orw').textContent=rk(S.streak.mw).t;$('orb').textContent=rk(S.streak.mb).t;
$('oq').innerHTML=['w','b'].map(t=>{const q=S.q[t],n=q.good+q.bad;return`<div>${t==='w'?'White':'Black'}<b>${n?Math.round(q.good/n*100):100}%</b>${q.good} good, ${q.bad} weak</div>`}).join('<div></div>');
$('status').textContent=msg;stats();save();render();beep(523,.15,'sine');setTimeout(()=>beep(784,.3,'sine'),150);show('m-over')}
function undo(n){if(!S.snaps.length)return;n=Math.min(n,S.snaps.length);const s=S.snaps[S.snaps.length-n];S.snaps.length-=n;Object.assign(S,{pos:s.pos,hist:s.hist,q:s.q,last:s.last,sel:null,hl:[],hint:null,over:false});S.mover=null;hide('m-over');after()}

/* ---------- Input ---------- */
$('board').onclick=e=>{const el=e.target.closest('[data-i]');if(el)click(+el.dataset.i)};
function click(i){if(S.busy||S.over||(S.mode==='ai'&&S.pos.t==='b'))return;const L=G[S.v].moves(S.pos);
if(S.v==='mancala'){const m=L.find(m=>m.f===i);if(m)attempt([m]);return}
const tg=S.sel!==null?S.hl.filter(m=>m.t===i):[];if(tg.length){attempt(tg);return}
const own=L.filter(m=>m.f===i);S.sel=own.length?i:null;S.hl=own;render()}
function attempt(ms){if(ms[0].pr){S.pend=ms;show('m-promo');return}go(ms[0])}
const go=m=>S.edu?ask(m):commit(m);
document.querySelectorAll('#m-promo [data-p]').forEach(b=>b.onclick=()=>{hide('m-promo');go(S.pend.find(x=>x.pr===b.dataset.p))});
function ask(m){S.busy=true;const q=pickQ(),o=$('qo');S.cq=q;S.cm=m;S.pick=null;$('qsub').textContent=S.subj+', '+S.grade;$('qt').textContent=q.q;o.innerHTML='';
q.options.forEach((t,i)=>{const b=document.createElement('button');b.className='opt';b.textContent=t;b.onclick=()=>{S.pick=i;[...o.children].forEach((c,j)=>c.classList.toggle('on',j===i));$('qgo').disabled=false};o.append(b)});
$('qgo').disabled=true;$('qx').className='hide';show('m-q')}
$('qgo').onclick=()=>{const q=S.cq,good=S.pick===q.a,st=S.stats[S.subj];st.total++;if(good){st.correct++;S.score+=10;beep(523,.1,'sine')}else beep(200,.25,'sawtooth');
const x=$('qx');x.textContent=(good?'Correct. ':'Not quite. ')+q.exp+(good?'':' Your move was cancelled. Pick again.');x.className='ex '+(good?'ok':'er');$('qgo').disabled=true;stats();save();
setTimeout(()=>{hide('m-q');S.busy=false;if(good)commit(S.cm);else{S.sel=null;S.hl=[];render()}},good?900:1900)};

/* ---------- Rendering ---------- */
function render(){const B=$('board'),p=S.pos;if(!p)return;let h='';
if(S.v==='mancala'){B.className='board mn';const live=!S.busy&&!S.over&&!(S.mode==='ai'&&p.t==='b');
const pit=i=>`<button class="pit${live&&p.t===(i<6?'w':'b')&&p.b[i]?' on':''}${S.hint&&S.hint.f===i?' hint':''}${S.last&&S.last.f===i?' last':''}" data-i="${i}">${p.b[i]}</button>`;
h=`<div class="st">${p.b[13]}<small>Black</small></div><div class="pits">${[12,11,10,9,8,7].map(pit).join('')}${[0,1,2,3,4,5].map(pit).join('')}</div><div class="st">${p.b[6]}<small>White</small></div>`}
else{B.className='board g8';const GL={K:'♚',Q:'♛',R:'♜',B:'♝',N:'♞',P:'♟'},ki=S.v==='chess'&&att(p.b,p.b.indexOf(p.t+'K'),oth(p.t))?p.b.indexOf(p.t+'K'):-1;
for(let i=0;i<64;i++){const x=p.b[i],c=['sq',((i>>3)+(i&7))%2?'d':'l'];
if(S.sel===i)c.push('sel');if(S.hl.some(m=>m.t===i))c.push(x?'cap':'dot');if(S.last&&(S.last.f===i||S.last.t===i))c.push('last');if(S.hint&&(S.hint.f===i||S.hint.t===i))c.push('hint');if(i===ki)c.push('chk');
const inner=x?(S.v==='chess'?`<span class="pc ${x[0]}">${GL[x[1]]}</span>`:`<span class="ck ${x.toLowerCase()}">${x===x.toUpperCase()?'♛':''}</span>`):'';
h+=`<div class="${c.join(' ')}" data-i="${i}">${inner}</div>`}}
B.innerHTML=h}
function log(){$('mc').textContent=S.hist.length+' moves';const l=$('log');l.innerHTML=S.hist.length?S.hist.map((m,i)=>`<div class="mv ${m.t}"><b>${i+1}</b>${m.t==='w'?'W':'B'} ${esc(m.n)}</div>`).join(''):'<i style="color:var(--mu)">No moves yet.</i>';l.scrollTop=l.scrollHeight}
function ev(){const v=G[S.v].eval(S.pos);$('evW').style.width=(50+50*Math.tanh(v/700))+'%';$('evT').textContent=(v>=0?'+':'')+(v/100).toFixed(1)}
const rk=n=>n>=20?{t:'Imperator Apex',b:'👑 Apex'}:n>=10?{t:'Grandmaster Scholar',b:'🏰 Grandmaster'}:n>=7?{t:'Board Strategist',b:'♟ Strategist'}:n>=5?{t:'Tactical Apprentice',b:'⚔ Apprentice'}:{t:'Novice Initiate',b:'🛡 Novice'};
function stats(){let c=0,t=0;$('perf').innerHTML=['history','math','ela','science'].map(s=>{const x=S.stats[s];c+=x.correct;t+=x.total;const p=x.total?Math.round(x.correct/x.total*100):0;return`<div class="prow"><div><span>${s[0].toUpperCase()+s.slice(1)}</span><span>${x.correct}/${x.total} (${p}%)</span></div><div class="tr"><i style="width:${p}%"></i></div></div>`}).join('');
$('acc').textContent=(t?Math.round(c/t*100):100)+'%';$('score').textContent=S.score;$('sw').textContent=S.streak.w;$('sb').textContent=S.streak.b;$('rw').textContent=rk(S.streak.w).b;$('rb').textContent=rk(S.streak.b).b}

/* ---------- Setup, coach, undo ---------- */
document.querySelectorAll('.seg[data-k] button').forEach(b=>b.onclick=()=>{const k=b.parentNode.dataset.k;S[k]=k==='edu'?+b.dataset.v:b.dataset.v;[...b.parentNode.children].forEach(c=>c.classList.toggle('on',c===b));if(k==='mode')$('eloP').classList.toggle('hide',S.mode==='pvp')});
$('elo').oninput=e=>{S.elo=+e.target.value;$('eloV').textContent=S.elo;$('hElo').textContent=S.elo;$('eloT').textContent=S.elo<=900?'Beginner':S.elo<=1500?'Intermediate':S.elo<=2100?'Advanced':'Grandmaster'};
$('go').onclick=()=>{hide('m-setup');$('badge').textContent=`${S.v[0].toUpperCase()+S.v.slice(1)}, ${S.subj}, ${S.grade}`;$('eloB').classList.toggle('hide',S.mode==='pvp');initGame()};
$('setup').onclick=()=>show('m-setup');$('reset').onclick=initGame;$('again').onclick=initGame;
$('coachB').onclick=()=>{S.coach=!S.coach;$('coachB').textContent='Coach: '+(S.coach?'on':'off');$('coachP').classList.toggle('hide',!S.coach)};
$('snd').onclick=()=>{S.sound=!S.sound;$('snd').textContent='Sound: '+(S.sound?'on':'off')};
$('ask').onclick=()=>{if(S.over||S.busy)return;const r=rank(S.pos,2)[0];S.hint=r[0];$('coachT').textContent=`Try ${nt(S.pos,r[0])}. It holds up best after two moves of lookahead.`;render()};
$('rev').onclick=()=>{$('pin').value='';$('pinE').textContent='';$('pinT').textContent=LS.get('sa_pin')?'Enter your undo passcode':'Create an undo passcode';show('m-pin')};
$('pinNo').onclick=()=>hide('m-pin');
$('pinOk').onclick=async()=>{const v=$('pin').value,h=await hash('pin:'+v),st=LS.get('sa_pin');
if(!st){if(v.length<4){$('pinE').textContent='Use at least 4 characters.';return}LS.set('sa_pin',h);hide('m-pin');toast('Passcode saved. Tap Reverse to use it.');return}
if(st!==h){$('pinE').textContent='Incorrect passcode.';beep(200,.2,'sawtooth');return}
hide('m-pin');toast('Reversing 3 moves');setTimeout(()=>undo(3),900)};

/* ---------- Accounts and leaderboard (stored in this browser only) ---------- */
function save(){if(!S.user)return;const A=LS.get('sa_acc',{});if(!Object.hasOwn(A,S.user))return;A[S.user].score=S.score;A[S.user].rec=S.rec;A[S.user].streak=Math.max(A[S.user].streak||0,S.streak.mw);if(S.av)A[S.user].av=S.av;LS.set('sa_acc',A)}
function accView(){$('av-out').classList.toggle('hide',!!S.user);$('av-in').classList.toggle('hide',!S.user);if(S.user)$('who').textContent=S.user+' ('+rk(S.streak.mw).t+')';$('acct').title=S.user||'Account'}
async function auth(reg){const u=$('u').value.trim(),pw=$('pw').value,m=$('am'),A=LS.get('sa_acc',{}),say=(t,g)=>{m.textContent=t;m.className=g?'ok':'er'};
if(reg){if(!/^[A-Za-z0-9]\w{2,19}$/.test(u)||pw.length<6)return say('Username: 3-20 letters, numbers or _. Password: 6+ characters.');if(Object.hasOwn(A,u))return say('That name is taken. Log in or pick another.');A[u]={h:await hash(u+':'+pw),score:0,streak:0};LS.set('sa_acc',A)}
else if(!Object.hasOwn(A,u)||A[u].h!==await hash(u+':'+pw))return say('Wrong username or password.');
S.user=u;S.score=A[u].score||0;S.rec=Object.assign({w:0,l:0,d:0,g:0},A[u].rec);S.streak.mw=Math.max(S.streak.mw,A[u].streak||0);say(reg?'Account created.':'Logged in.',1);stats();setTimeout(()=>{if(!reg)hide('m-acc');accView()},500)}
$('reg').onclick=()=>auth(1);$('login').onclick=()=>auth(0);
$('logout').onclick=()=>{S.user=null;S.score=0;S.rec={w:0,l:0,d:0,g:0};stats();accView()};
const openAcc=()=>{accView();show('m-acc')};$('acct').onclick=openAcc;$('mAcc').onclick=openAcc;$('accX').onclick=()=>hide('m-acc');
function openLb(){const A=LS.get('sa_acc',{}),r=Object.keys(A).map(n=>({n,s:A[n].score||0,k:A[n].streak||0,av:A[n].av})).sort((a,b)=>b.s-a.s||b.k-a.k);
$('lbl').innerHTML=r.length?r.map((p,i)=>`<div class="lr"><b>#${i+1}</b><span>${esc(p.av||'👤')} ${esc(dn(p.n))}<br><small style="color:var(--mu)">${rk(p.k).t}</small></span><span><b>${p.s} pts</b><br><small>🔥 ${p.k} wins</small></span></div>`).join(''):'<i style="color:var(--mu)">No players yet. Create an account, log in, then win a game (or use Admin → Give points).</i>';
document.querySelector('#m-lb p').textContent='Local accounts — each win = 1 point. Log in so your wins are saved.';
show('m-lb')}
$('lb').onclick=openLb;$('mLb').onclick=openLb;$('lbX').onclick=()=>hide('m-lb');

/* ---------- Shared accounts: username + password saved online (needs claude.ai storage) ---------- */
let CL=null;const lsSave=save,lsAuth=auth,lsLb=openLb,dk=u=>'acc/'+u.toLowerCase(),zs=()=>({history:{correct:0,total:0},math:{correct:0,total:0},ela:{correct:0,total:0},science:{correct:0,total:0}});
async function pbk(pw,salt){const e=new TextEncoder(),k=await crypto.subtle.importKey('raw',e.encode(pw),'PBKDF2',false,['deriveBits']),b=await crypto.subtle.deriveBits({name:'PBKDF2',salt:e.encode(salt),iterations:150000,hash:'SHA-256'},k,256);return[...new Uint8Array(b)].map(x=>x.toString(16).padStart(2,'0')).join('')}
function cloudUi(){document.querySelector('#m-lb p').textContent=CL?'Saved online. Everyone who plays here can see this list.':'Players who created accounts in this browser.'}
let wq=Promise.resolve();const HOLD=Math.random().toString(36).slice(2),pause=ms=>new Promise(z=>setTimeout(z,ms));
/* Settles conflicts: take a short lock on the player's entry, read the latest, add only what this device changed, write, release */
const cloudWrite=()=>(wq=wq.then(async()=>{if(!CL||!S.user)return;const sy=S.sync||{s:0,w:0,l:0,d:0},r=S.rec||{},ref=CL.db.doc('lb/'+S.user.toLowerCase());
for(let i=0;i<6;i++){const g=await ref.acquire({holder:HOLD,ttlMs:3000});if(g.acquired)break;await pause(300+Math.random()*400)}
const c=(await ref.get()).data()||{},P=(a,b,x)=>Math.max(0,Math.floor(Number(a)||0)+x-b),n={s:P(c.s,sy.s,S.score),w:P(c.w,sy.w,r.w||0),l:P(c.l,sy.l,r.l||0),d:P(c.d,sy.d,r.d||0),k:Math.max(Math.floor(Number(c.k)||0),S.streak.mw)};
await Promise.all([ref.set({n:S.user,s:n.s,k:n.k,av:S.av,w:n.w,l:n.l,d:n.d}),CL.db.doc(dk(S.user)).update({score:n.s,streak:n.k,stats:S.stats,rec:{...S.rec,w:n.w,l:n.l,d:n.d}})]);
S.score=n.s;S.rec.w=n.w;S.rec.l=n.l;S.rec.d=n.d;S.streak.mw=n.k;S.sync={s:n.s,w:n.w,l:n.l,d:n.d};stats()}).catch(()=>{}));
save=function(){if(!CL)return lsSave();if(!S.user)return;clearTimeout(CL.t);CL.t=setTimeout(()=>cloudWrite().catch(()=>{}),400)};
auth=async function(reg){if(!CL)return lsAuth(reg);const u=$('u').value.trim(),pw=$('pw').value,m=$('am'),say=(t,g)=>{m.textContent=t;m.className=g?'ok':'er'},okU=/^[A-Za-z0-9]\w{2,19}$/.test(u);
if(reg&&(!okU||pw.length<6))return say('Username: 3-20 letters, numbers or _. Password: 6+ characters.');
if(!okU||!pw)return say('Wrong username or password.');
let d;try{const r=CL.db.doc(dk(u)),s=await r.get();
if(reg){if(s.exists)return say('That name is taken. Log in or pick another.');const salt=crypto.randomUUID();d={n:u,salt,h:await pbk(pw,salt),score:0,streak:0,stats:zs()};await r.set(d);await CL.db.doc('lb/'+u.toLowerCase()).set({n:u,s:0,k:0})}
else{d=s.exists&&s.data();if(!d||d.h!==await pbk(pw,d.salt||''))return say('Wrong username or password.')}}
catch{CL=null;cloudUi();return say('Online accounts are not available for you here. Tap again to use a password saved in this browser instead.')}
S.user=d.n;S.score=d.score||0;S.rec=Object.assign({w:0,l:0,d:0,g:0},d.rec);S.streak.mw=Math.max(S.streak.mw,d.streak||0);S.stats=Object.assign(zs(),d.stats||{});say(reg?'Account created.':'Logged in.',1);stats();setTimeout(()=>{if(!reg)hide('m-acc');accView()},500)};
$('logout').onclick=()=>{S.user=null;S.score=0;S.rec={w:0,l:0,d:0,g:0};if(CL){S.stats=zs();S.streak={w:0,b:0,mw:0,mb:0}}stats();accView()};
openLb=function(){lsLb()};
$('lb').onclick=openLb;$('mLb').onclick=openLb;
let RO=null;(async()=>{try{const db=await claude.use('db');if(!db)return;let cw=null;try{const u=await claude.use('user');cw=u&&u.can?await u.can('data.write'):null}catch{}RO=db;if(cw!==false){CL={db};cloudUi()}liveLb();autoUpdate()}catch{}})();


/* ---------- Account codes + 5-minute leaderboard sync ---------- */
const CODE_V='SA1',CHECK_INTERVAL=5000;let CR={},nextAt=Date.now()+CHECK_INTERVAL;
const b64e=t=>btoa(unescape(encodeURIComponent(t))).replace(/\+/g,'-').replace(/\//g,'_').replace(/=+$/,'');
const b64d=t=>{t=t.replace(/-/g,'+').replace(/_/g,'/');while(t.length%4)t+='=';return decodeURIComponent(escape(atob(t)))};
const ck=t=>{let h=2166136261;for(let i=0;i<t.length;i++){h^=t.charCodeAt(i);h=Math.imul(h,16777619)}return(h>>>0).toString(36)};
const ni=(v,m=1e7)=>{v=Math.floor(Number(v));return Number.isFinite(v)&&v>=0?Math.min(v,m):0};
function makeCode(){const r=S.rec||{};const o={n:S.user,s:S.score,k:S.streak.mw,w:r.w||0,l:r.l||0,d:r.d||0,g:r.g||0,av:S.av||'👤',st:S.stats,t:Date.now()};const b=b64e(JSON.stringify(o));return CODE_V+'.'+b+'.'+ck(b)}
function readCode(c){const m=String(c||'').trim().replace(/\s+/g,'').split('.');if(m.length!==3||m[0]!==CODE_V||ck(m[1])!==m[2])return null;let o;try{o=JSON.parse(b64d(m[1]))}catch{return null}
if(!o||typeof o.n!=='string'||!/^[A-Za-z0-9]\w{2,19}$/.test(o.n))return null;const st={};for(const k of['history','math','ela','science']){const x=(o.st||{})[k]||{};st[k]={correct:ni(x.correct),total:ni(x.total)}}
return{n:o.n,s:ni(o.s),k:ni(o.k),w:ni(o.w),l:ni(o.l),d:ni(o.d),g:ni(o.g),av:String(o.av||'👤').slice(0,8),st,t:ni(o.t,9e15)}}
function addToBoard(o){const B=LS.get('sa_board',{}),key=o.n.toLowerCase(),old=B[key];if(old&&old.t>o.t)return false;B[key]=o;LS.set('sa_board',B);return true}
function pushOwn(){if(!S.user)return;const o=readCode(makeCode());if(o)addToBoard(o)}
function refreshCode(){const el=$('myCode');if(el)el.value=S.user?makeCode():''}
const accViewCode=accView;accView=function(){accViewCode();refreshCode();pushOwn()};
const save1=save;save=function(){save1.apply(this,arguments);refreshCode()};
$('copyCode').onclick=async()=>{const el=$('myCode');try{await navigator.clipboard.writeText(el.value);toast('Code copied')}catch{el.select();try{document.execCommand('copy');toast('Code copied')}catch{toast('Select the code and copy it')}}};
async function refreshCloud(){const D=CL?CL.db:RO;if(!D)return;try{const c=D.collection&&D.collection('lb');if(!c)return;const r=await(c.get?c.get():c.list());const docs=r&&(r.docs||r);if(docs&&docs.forEach){const n={};docs.forEach(d=>{const v=typeof d.data==='function'?d.data():d;if(v&&v.n)n[String(v.n).toLowerCase()]={n:v.n,s:v.s||0,k:v.k||0,w:v.w||0,l:v.l||0,d:v.d||0,av:v.av}});CR=n}}catch{}}
function boardRows(){const R={},B=LS.get('sa_board',{});for(const k in B)R[k]=B[k];for(const k in CR)R[k]=CR[k];
const A=LS.get('sa_acc',{});for(const n in A){const a=A[n],r=a.rec||{};R[n.toLowerCase()]={n,s:a.score||0,k:a.streak||0,w:r.w||0,l:r.l||0,d:r.d||0,av:a.av}}
if(S.user)R[S.user.toLowerCase()]={n:S.user,s:S.score,k:S.streak.mw,w:S.rec.w,l:S.rec.l,d:S.rec.d,av:S.av};
return Object.values(R).sort((a,b)=>b.s-a.s||b.k-a.k||b.w-a.w)}
function renderLb(){const r=boardRows();$('lbl').innerHTML=r.length?r.map((p,i)=>`<div class="lr"><b>#${i+1}</b><span>${esc(p.av||'👤')} ${esc(dn(p.n))}<br><small style="color:var(--mu)">${rk(p.k).t} · 🔥 best streak ${p.k}</small></span><span><b>${p.s} pts</b><br><small>${p.w}W · ${p.l}L · ${p.d}D</small></span></div>`).join(''):'<i style="color:var(--mu)">No players yet. Create an account, win a game, or paste a player code below.</i>';
document.querySelector('#m-lb p').textContent=LBU?'Each win = 1 point. Accounts from every device appear here live.':'Each win = 1 point. Checks for changes every few seconds.'}
openLb=function(){renderLb();show('m-lb')};$('lb').onclick=openLb;$('mLb').onclick=openLb;
async function autoUpdate(){nextAt=Date.now()+CHECK_INTERVAL;try{if(S.user)pushOwn();await refreshCloud();adoptCloud();refreshCode();if(!$('m-lb').classList.contains('hide'))renderLb()}catch{}}
setInterval(autoUpdate,CHECK_INTERVAL);
document.addEventListener('visibilitychange',()=>{if(!document.hidden&&Date.now()>=nextAt)autoUpdate()});
setInterval(()=>{const t=Math.max(0,Math.round((nextAt-Date.now())/1000)),x=LBU?'Live: new scores and accounts appear instantly':'Next automatic check in '+Math.floor(t/60)+':'+String(t%60).padStart(2,'0');if($('lbNext'))$('lbNext').textContent=x;if($('codeAge'))$('codeAge').textContent=x+'.'},1000);
autoUpdate();
/* Keep every device's account: if the same account moved ahead on another device, take the higher numbers so nothing is overwritten */
function adoptCloud(){if(!S.user||!S.sync)return;const c=CR[S.user.toLowerCase()];if(!c)return;let ch=0;
if(c.s>S.sync.s){S.score+=c.s-S.sync.s;S.sync.s=c.s;ch=1}
for(const x of['w','l','d'])if(c[x]>S.sync[x]){S.rec[x]=(S.rec[x]||0)+c[x]-S.sync[x];S.sync[x]=c[x];ch=1}
if(c.k>S.streak.mw){S.streak.mw=c.k;ch=1}if(ch)stats()}
const auth9=auth;auth=async function(r){await auth9(r);S.sync=S.user?{s:S.score,w:S.rec.w||0,l:S.rec.l||0,d:S.rec.d||0}:null};
/* Live leaderboard: every device's accounts appear automatically */
let LBU=null;
function liveLb(){const D=CL?CL.db:RO;if(!D||LBU)return;try{LBU=D.collection('lb').onSnapshot(s=>{const n={};s.docs.forEach(d=>{const v=d.data()||{};if(v.n)n[String(v.n).toLowerCase()]={n:String(v.n),s:ni(v.s),k:ni(v.k),w:ni(v.w),l:ni(v.l),d:ni(v.d),av:String(v.av||'👤').slice(0,8)}});CR=n;adoptCloud();if(!$('m-lb').classList.contains('hide'))renderLb();if(!liveLb.done){liveLb.done=1;syncLocal()}},()=>{LBU=null})}catch{LBU=null}}
/* Accounts made on this device before online sync are added to the shared board once */
async function syncLocal(){if(!CL)return;const A=LS.get('sa_acc',{});for(const n in A){const k=n.toLowerCase(),a=A[n],r=a.rec||{};if(CR[k]&&CR[k].s>=(a.score||0))continue;try{const x=await CL.db.doc(dk(n)).get();if(x.exists)continue;await CL.db.doc('lb/'+k).set({n,s:a.score||0,k:a.streak||0,av:a.av||'👤',w:r.w||0,l:r.l||0,d:r.d||0})}catch{}}}

/* ---------- Profile picture (emoji avatar, saved with the account) ---------- */
const AVS=['👤','🦊','🐼','🐯','🦉','🐙','🦄','🐲','🚀','⚽','🎨','🎸','🌟','🔥','📚','🧠'];S.av='👤';
const accView0=accView;accView=function(){accView0();$('acct').textContent=S.av;$('avs').innerHTML=AVS.map(a=>`<button data-a="${a}" class="${a===S.av?'on':''}" style="font-size:1.4rem;flex:0 0 auto">${a}</button>`).join('')};
function saveAv(){if(!S.user)return;if(CL){CL.db.doc(dk(S.user)).update({av:S.av}).catch(()=>{});CL.db.doc('lb/'+S.user.toLowerCase()).update({av:S.av}).catch(()=>{})}else{const A=LS.get('sa_acc',{});if(Object.hasOwn(A,S.user)){A[S.user].av=S.av;LS.set('sa_acc',A)}}}
$('avs').onclick=e=>{const b=e.target.closest('[data-a]');if(!b||!S.user)return;S.av=b.dataset.a;accView();saveAv()};
const auth0=auth;auth=async function(r){await auth0(r);if(!S.user)return;try{if(CL){const s=await CL.db.doc(dk(S.user)).get();S.av=(s.data()||{}).av||'👤'}else{const A=LS.get('sa_acc',{});S.av=(A[S.user]||{}).av||'👤'}}catch{S.av='👤'}accView()};
const out0=$('logout').onclick;$('logout').onclick=()=>{out0();S.av='👤';accView()};

/* ---------- Admin panel (password: phonedcorn) ---------- */
const ADMIN_PASS='phonedcorn';
function getAccMap(){return LS.get('sa_acc',{})}
function setAccMap(A){LS.set('sa_acc',A)}
function refreshAdmin(){
  const A=getAccMap(), pick=$('adPick').value, names=new Map();
  Object.keys(A).forEach(n=>names.set(n.toLowerCase(),n));
  Object.values(CR||{}).forEach(v=>{if(v&&v.n&&!names.has(String(v.n).toLowerCase()))names.set(String(v.n).toLowerCase(),v.n)});
  $('adPick').innerHTML='<option value="">— Current session —</option>'+
    [...names.values()].sort((a,b)=>a.localeCompare(b)).map(n=>`<option value="${esc(n)}">${esc(dn(n))}${Object.hasOwn(A,n)?'':' (online)'}</option>`).join('');
  if(pick && names.has(pick.toLowerCase()))$('adPick').value=pick;
  const sel=$('adPick').value, local=A[sel], cloud=CR[sel.toLowerCase()];
  if(sel && (local||cloud)){
    $('adScore').textContent=local?.score??cloud?.s??0;
    $('adWins').textContent=local?.streak??cloud?.k??0;
  }else{
    $('adScore').textContent=S.score;$('adWins').textContent=S.streak.mw||0;
  }
  $('adAccs').textContent=names.size;
}
function targetAcc(){
  const sel=$('adPick').value, A=getAccMap();
  if(sel && Object.hasOwn(A,sel))return {type:'acc', name:sel, data:A[sel], A};
  return {type:'session', name:null, data:null, A};
}
function adjPts(sign){
  const n=Math.max(1,parseInt($('adAmtPts').value,10)||1);
  const t=targetAcc();
  if(t.type==='acc'){
    t.data.score=Math.max(0,(t.data.score||0)+sign*n);
    setAccMap(t.A);
    if(S.user===t.name){S.score=t.data.score;stats()}
    toast((sign>0?'Gave +':'- Took ')+n+' LB pts from '+dn(t.name));
  }else if(S.user){
    // logged in but dropdown on "current session" — still update their account
    S.score=Math.max(0,S.score+sign*n);
    const A=getAccMap();
    if(Object.hasOwn(A,S.user)){A[S.user].score=S.score;setAccMap(A)}
    stats();
    toast((sign>0?'Gave +':'- Took ')+n+' LB pts → '+dn(S.user));
  }else{
    S.score=Math.max(0,S.score+sign*n);
    stats();
    toast((sign>0?'+':'-')+n+' session pts (log in or pick an account for leaderboard)');
  }
  refreshAdmin();
}
function adjWins(sign){
  const n=Math.max(1,parseInt($('adAmtW').value,10)||1);
  const t=targetAcc();
  if(t.type==='acc'){
    t.data.streak=Math.max(0,(t.data.streak||0)+sign*n);
    t.data.score=Math.max(0,(t.data.score||0)+sign*n); // each win = 1 leaderboard point
    setAccMap(t.A);
    if(S.user===t.name){
      S.streak.mw=t.data.streak;S.streak.w=Math.max(0,S.streak.w+sign*n);
      S.score=t.data.score;stats();
    }
    toast((sign>0?'+':'-')+n+' win'+(n===1?'':'s')+' (+pts) → '+dn(t.name));
  }else{
    S.streak.mw=Math.max(0,(S.streak.mw||0)+sign*n);
    S.streak.w=Math.max(0,(S.streak.w||0)+sign*n);
    S.score=Math.max(0,S.score+sign*n);
    if(S.user){const A=getAccMap();if(Object.hasOwn(A,S.user)){A[S.user].streak=S.streak.mw;A[S.user].score=S.score;setAccMap(A)}}
    stats();
    toast((sign>0?'+':'-')+n+' win'+(n===1?'':'s')+' (+pts) (session)');
  }
  refreshAdmin();
}
function openAdmin(){
  $('adminPw').value='';$('adminErr').textContent='';
  if(S.admin){hide('admin-login');show('admin-panel');refreshAdmin()}
  else{show('admin-login');hide('admin-panel')}
  show('m-admin');
}
$('adminB').onclick=openAdmin;
$('mAdmin').onclick=openAdmin;
$('adminCancel').onclick=$('adminX').onclick=()=>hide('m-admin');
$('adminLock').onclick=()=>{S.admin=false;hide('m-admin');toast('Admin locked')};
$('adminGo').onclick=()=>{
  if($('adminPw').value===ADMIN_PASS){
    S.admin=true;$('adminErr').textContent='';
    hide('admin-login');show('admin-panel');refreshAdmin();beep(523,.1,'sine');
  }else{
    $('adminErr').textContent='Incorrect password.';beep(200,.25,'sawtooth');
  }
};
$('adminPw').onkeydown=e=>{if(e.key==='Enter')$('adminGo').click()};
$('adPick').onchange=()=>refreshAdmin();
$('adOpenLb').onclick=()=>{hide('m-admin');openLb()};
$('adGivePts').onclick=()=>adjPts(1);
$('adTakePts').onclick=()=>adjPts(-1);
$('adGiveW').onclick=()=>adjWins(1);
$('adTakeW').onclick=()=>adjWins(-1);
$('adResetScore').onclick=()=>{
  const t=targetAcc();
  if(t.type==='acc'){
    t.data.score=0;t.data.streak=0;setAccMap(t.A);
    if(S.user===t.name){S.score=0;S.streak={w:0,b:0,mw:0,mb:0};stats()}
    toast('Reset '+dn(t.name));
  }else{
    S.score=0;S.streak={w:0,b:0,mw:0,mb:0};stats();
    if(S.user){const A=getAccMap();if(Object.hasOwn(A,S.user)){A[S.user].score=0;A[S.user].streak=0;setAccMap(A)}}
    toast('Session score & wins reset');
  }
  refreshAdmin();
};
$('adDeleteAcc').onclick=async()=>{
  const name=$('adPick').value;
  if(!name){toast('Select an account first');return}
  if(name.toLowerCase()===OWNER_USER){toast('The Owner account is protected');return}
  if(!confirm('Permanently delete the account "'+name+'" and its leaderboard entry? This cannot be undone.'))return;
  const key=name.toLowerCase();
  if(CR[key]&&!CL){toast('Online account needs database write access to delete.');return}
  if(CL){
    try{await Promise.all([CL.db.doc(dk(name)).delete(),CL.db.doc('lb/'+key).delete()]);}
    catch(e){toast('Online deletion failed. Check database permissions.');return;}
  }
  const A=getAccMap(), B=LS.get('sa_board',{});
  delete A[name];delete B[key];setAccMap(A);LS.set('sa_board',B);
  if(S.user&&S.user.toLowerCase()===key){
    S.user=null;S.score=0;S.rec={w:0,l:0,d:0,g:0};S.streak={w:0,b:0,mw:0,mb:0};
    S.stats=zs();S.av='👤';accView();stats();
  }
  delete CR[key];$('adPick').value='';refreshAdmin();
  if(!$('m-lb').classList.contains('hide'))renderLb();
  toast('Deleted account: '+dn(name));
};
$('adResetStats').onclick=()=>{
  S.stats={history:{correct:0,total:0},math:{correct:0,total:0},ela:{correct:0,total:0},science:{correct:0,total:0}};
  stats();refreshAdmin();toast('Subject stats reset');
};
$('adClearAcc').onclick=()=>{
  if(!confirm('Delete ALL local accounts and leaderboard data? This cannot be undone.'))return;
  setAccMap({});LS.set('sa_board',{});S.rec={w:0,l:0,d:0,g:0};S.user=null;S.score=0;S.av='👤';S.streak={w:0,b:0,mw:0,mb:0};stats();accView();refreshAdmin();toast('All local accounts cleared');
};
$('adClearPin').onclick=()=>{
  localStorage.removeItem('sa_pin');toast('Undo passcode cleared');
};
$('adForceClassic').onclick=()=>{
  S.edu=0;document.querySelectorAll('.seg[data-k=edu] button').forEach(b=>b.classList.toggle('on',b.dataset.v==='0'));
  toast('Classic mode forced (no questions)');
};
$('adForceEdu').onclick=()=>{
  S.edu=1;document.querySelectorAll('.seg[data-k=edu] button').forEach(b=>b.classList.toggle('on',b.dataset.v==='1'));
  toast('Educational mode forced');
};

/* ---------- Owner account (login: brandon / phonedcorn, displays as "Owner") ---------- */
const OWNER_USER='brandon',OWNER_PASS='phonedcorn',OWNER_LABEL='Owner';
function dn(n){return n&&String(n).toLowerCase()===OWNER_USER?OWNER_LABEL:n}
const isOwner=()=>!!S.user&&S.user.toLowerCase()===OWNER_USER;
(function(){
  // display name everywhere the signed-in name is shown
  const accView1=accView;
  accView=function(){
    if(isOwner()&&!AVS.includes('👑'))AVS.push('👑');
    if(!isOwner()){const i=AVS.indexOf('👑');if(i>-1)AVS.splice(i,1)}
    if(isOwner()&&S.av!=='👑'){S.av='👑';saveAv()}
    accView1();
    if(S.user){$('who').textContent=(isOwner()?'👑 ':'')+dn(S.user)+' ('+rk(S.streak.mw).t+')';$('acct').title=dn(S.user)}
    $('acct').classList.toggle('owner',isOwner());
    const pk=$('avs');pk.classList.toggle('hide',isOwner());if(pk.previousElementSibling)pk.previousElementSibling.classList.toggle('hide',isOwner());
    const ob=document.getElementById('ownerBadge');if(ob)ob.classList.toggle('hide',!isOwner());
  };
  // header badge
  const b=document.createElement('span');b.id='ownerBadge';b.className='pill hide';b.innerHTML='👑 <b>Owner</b>';
  document.querySelector('header .bar').prepend(b);

  // make sure the owner record exists with the owner password (local + online), so nobody else can claim it
  async function ensureOwner(){
    if(CL){
      try{
        const r=CL.db.doc(dk(OWNER_USER)),s0=await r.get(),d=s0.exists&&s0.data();
        if(!d||d.h!==await pbk(OWNER_PASS,d.salt||'')){
          const salt=crypto.randomUUID();
          await r.set(Object.assign({},d||{},{n:OWNER_USER,salt,h:await pbk(OWNER_PASS,salt),score:(d&&d.score)||0,streak:(d&&d.streak)||0,stats:(d&&d.stats)||zs()}));
          await CL.db.doc('lb/'+OWNER_USER).set({n:OWNER_USER,s:(d&&d.score)||0,k:(d&&d.streak)||0,av:(d&&d.av)||'👑'});
        }
      }catch{}
    }
    const A=LS.get('sa_acc',{}),h=await hash(OWNER_USER+':'+OWNER_PASS);
    if(!Object.hasOwn(A,OWNER_USER)||A[OWNER_USER].h!==h){A[OWNER_USER]=Object.assign({score:0,streak:0,av:'👑'},A[OWNER_USER]||{},{h});LS.set('sa_acc',A)}
  }

  const auth1=auth;
  auth=async function(reg){
    const u=$('u').value.trim(),pw=$('pw').value,m=$('am'),low=u.toLowerCase();
    if(low===OWNER_USER||low===OWNER_LABEL.toLowerCase()){
      if(reg||low!==OWNER_USER){m.textContent='That name is taken. Log in or pick another.';m.className='er';return}
      if(pw!==OWNER_PASS){m.textContent='Wrong username or password.';m.className='er';return}
      $('u').value=OWNER_USER;await ensureOwner();
      await auth1(0);
      if(isOwner()){
        if(S.av==='👤'){S.av='👑';saveAv()}
        S.admin=true;accView();toast('Welcome back, Owner');
      }
      return;
    }
    return auth1(reg);
  };
  $('reg').onclick=()=>auth(1);$('login').onclick=()=>auth(0);

  // owner: no admin password, no undo passcode
  const openAdmin1=openAdmin;
  openAdmin=function(){if(isOwner())S.admin=true;openAdmin1()};
  $('adminB').onclick=openAdmin;$('mAdmin').onclick=openAdmin;
  const rev1=$('rev').onclick;
  $('rev').onclick=()=>{
    if(isOwner()){if(!S.snaps.length){toast('Nothing to reverse yet');return}toast('Reversing 3 moves');setTimeout(()=>undo(3),600);return}
    rev1();
  };

  // signing out locks the admin panel again
  const out1=$('logout').onclick;
  $('logout').onclick=()=>{const was=isOwner();out1();if(was)S.admin=false;accView()};
})();
accView();

initGame();
</script></body></html>

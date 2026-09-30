# 24BDA70363-sandesh-sharma-FULL-STACK
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>TRAVELX — Smart Travel Planning & Booking</title>
<style>
:root{--p:#4f46e5;--p2:#7c3aed;--a:#06b6d4;--bg:#f6f8fc;--card:#fff;--txt:#172033;--muted:#697386;--line:#e7eaf0;--good:#10b981;--danger:#ef4444}
*{box-sizing:border-box;margin:0;padding:0}html{scroll-behavior:smooth}
body{font-family:Inter,Segoe UI,Arial,sans-serif;background:var(--bg);color:var(--txt);transition:.25s}
button,input,select{font:inherit}button{cursor:pointer}
body.dark{--bg:#0b1120;--card:#111a2e;--txt:#f3f6ff;--muted:#9aa7bd;--line:#24304a}
.top{height:72px;background:color-mix(in srgb,var(--card) 92%,transparent);backdrop-filter:blur(15px);border-bottom:1px solid var(--line);display:flex;align-items:center;padding:0 5%;position:sticky;top:0;z-index:100}
.logo{font-size:25px;font-weight:950;letter-spacing:-1px;color:var(--txt)}.logo b{color:var(--p)}
.nav{display:flex;gap:25px;margin-left:55px}.nav a{color:var(--muted);text-decoration:none;font-size:14px;font-weight:750}.nav a:hover{color:var(--p)}
.navright{margin-left:auto;display:flex;gap:9px;align-items:center}
.btn,.ghost{border:0;border-radius:10px;padding:11px 16px;font-weight:800}.btn{background:linear-gradient(135deg,var(--p),var(--p2));color:#fff;box-shadow:0 8px 20px #4f46e533}.ghost{background:var(--card);border:1px solid var(--line);color:var(--txt)}
.hero{min-height:650px;padding:80px 5%;display:flex;align-items:center;background:radial-gradient(circle at 80% 20%,#22d3ee33,transparent 28%),radial-gradient(circle at 20% 80%,#7c3aed2e,transparent 32%),linear-gradient(135deg,#111827,#172554 52%,#312e81);color:#fff;overflow:hidden}
.heroinner{max-width:1180px;width:100%;margin:auto}.eyebrow{display:inline-flex;padding:8px 13px;border:1px solid #ffffff2c;background:#ffffff12;border-radius:30px;font-size:12px;font-weight:900;letter-spacing:.5px}.hero h1{font-size:64px;line-height:.98;letter-spacing:-3px;max-width:850px;margin:22px 0}.hero h1 span{background:linear-gradient(90deg,#67e8f9,#a78bfa);color:transparent;background-clip:text}.hero p{max-width:700px;color:#cbd5e1;font-size:18px;line-height:1.7}
.search{margin-top:32px;background:#fff;padding:10px;border-radius:17px;display:grid;grid-template-columns:1.5fr 1fr 1fr 1fr auto;gap:8px;max-width:1100px;box-shadow:0 25px 70px #0006}.search input,.search select,.field input,.field select{width:100%;border:1px solid #e2e8f0;background:#fff;color:#172033;padding:14px;border-radius:10px;outline:0}.search button{border:0;border-radius:10px;padding:0 22px;background:linear-gradient(135deg,#4f46e5,#7c3aed);color:#fff;font-weight:900}
.metrics{display:flex;gap:45px;margin-top:38px}.metrics strong{font-size:27px}.metrics small{display:block;color:#a5b4fc;margin-top:4px}
.wrap{width:90%;max-width:1200px;margin:auto}section{padding:75px 0}.heading{text-align:center;margin-bottom:40px}.heading h2{font-size:35px;letter-spacing:-1px}.heading p{color:var(--muted);margin-top:8px}
.cards4{display:grid;grid-template-columns:repeat(4,1fr);gap:17px}.feature,.card,.package,.review,.plannerbox,.bookbox{background:var(--card);border:1px solid var(--line);border-radius:17px;box-shadow:0 10px 30px #0f172a08}.feature{padding:24px;transition:.25s}.feature:hover,.card:hover,.package:hover{transform:translateY(-5px);box-shadow:0 18px 40px #0f172a18}.ico{font-size:34px;margin-bottom:13px}.feature h3{margin-bottom:7px}.feature p,.card p,.package p,.review p{color:var(--muted);font-size:14px;line-height:1.6}
.sectionhead{display:flex;justify-content:space-between;align-items:end;margin-bottom:25px}.sectionhead h2{font-size:31px}.chips{display:flex;gap:7px;flex-wrap:wrap}.chip{border:1px solid var(--line);background:var(--card);color:var(--muted);padding:8px 13px;border-radius:20px;font-weight:800}.chip.on{background:#eef2ff;color:var(--p);border-color:#c7d2fe}
.destgrid{display:grid;grid-template-columns:repeat(4,1fr);gap:18px}.card{overflow:hidden}.photo{height:185px;display:flex;align-items:center;justify-content:center;font-size:70px;position:relative}.one{background:linear-gradient(135deg,#bfdbfe,#dbeafe)}.two{background:linear-gradient(135deg,#fed7aa,#ffedd5)}.three{background:linear-gradient(135deg,#bbf7d0,#dcfce7)}.four{background:linear-gradient(135deg,#ddd6fe,#ede9fe)}.pill{position:absolute;left:12px;top:12px;background:#fff;color:#111827;border-radius:20px;padding:6px 9px;font-size:10px;font-weight:950}.cardbody{padding:17px}.stars{color:#f59e0b;font-size:13px;margin-top:5px}.cardfoot{display:flex;align-items:center;justify-content:space-between;margin-top:14px}.price{color:var(--p);font-weight:950}
.packages{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}.package{padding:25px;position:relative}.package.hot{border:2px solid #818cf8}.ribbon{position:absolute;right:15px;top:15px;background:#ede9fe;color:#5b21b6;padding:6px 9px;border-radius:20px;font-size:10px;font-weight:950}.package h3{font-size:23px;margin:12px 0 8px}.package ul{list-style:none;margin:15px 0}.package li{padding:6px 0;color:var(--muted);font-size:14px}.tag{display:inline-block;background:#eef2ff;color:#4f46e5;padding:6px 10px;border-radius:20px;font-size:10px;font-weight:950}
.plannerbg{background:linear-gradient(180deg,#eef2ff88,var(--bg))}.plannerbox{padding:27px;max-width:980px;margin:auto}.grid2{display:grid;grid-template-columns:1fr 1fr;gap:17px}.field label{display:block;font-size:13px;font-weight:850;margin-bottom:7px}.full{grid-column:1/-1}.result{display:none;margin-top:20px;padding:20px;background:#ecfdf5;border:1px solid #a7f3d0;color:#064e3b;border-radius:13px;line-height:1.85}
.bookinglayout{display:grid;grid-template-columns:1.3fr .7fr;gap:20px}.bookbox{padding:27px}.summary{background:linear-gradient(145deg,#111827,#312e81);color:#fff;border-radius:17px;padding:27px;box-shadow:0 18px 40px #312e8130}.sumrow{display:flex;justify-content:space-between;border-bottom:1px solid #ffffff1f;padding:14px 0;color:#c7d2fe}.sumrow b{color:#fff}
.reviews{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}.review{padding:23px}.review .stars{font-size:16px}.avatar{margin-top:15px;font-weight:850}
footer{background:#0b1120;color:#fff;padding:50px 5%}.footgrid{max-width:1200px;margin:auto;display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:35px}.footgrid p,.footgrid li{color:#94a3b8;line-height:1.9;font-size:14px}.footgrid ul{list-style:none}.copyright{text-align:center;border-top:1px solid #ffffff14;margin-top:35px;padding-top:20px;color:#64748b}
.modal{display:none;position:fixed;inset:0;background:#0009;z-index:500;align-items:center;justify-content:center}.modalbox{width:92%;max-width:450px;background:var(--card);border-radius:18px;padding:28px;position:relative}.x{position:absolute;right:18px;top:10px;font-size:27px;cursor:pointer}.modalbox input{width:100%;padding:13px;border:1px solid var(--line);background:var(--card);color:var(--txt);border-radius:9px;margin:7px 0}
.toast{display:none;position:fixed;right:22px;bottom:22px;background:#111827;color:#fff;padding:14px 19px;border-radius:11px;z-index:999;box-shadow:0 12px 35px #0005}
.dashboard{position:fixed;right:20px;bottom:75px;width:270px;background:var(--card);border:1px solid var(--line);padding:18px;border-radius:15px;box-shadow:0 20px 50px #0003;display:none;z-index:200}.dashboard h3{margin-bottom:10px}.dashitem{display:flex;justify-content:space-between;padding:9px 0;border-bottom:1px solid var(--line);font-size:13px}
@media(max-width:950px){.nav{padding:0 3%}.navlinks{display:none}.search{grid-template-columns:1fr 1fr}.cards4,.destgrid{grid-template-columns:1fr 1fr}.packages,.reviews,.bookinglayout,.footgrid{grid-template-columns:1fr}.hero h1{font-size:48px}}
@media(max-width:600px){.search,.grid2,.cards4,.destgrid{grid-template-columns:1fr}.hero h1{font-size:38px}.metrics{gap:20px;flex-wrap:wrap}.sectionhead{display:block}.chips{margin-top:15px}}
</style>
</head>
<body>

<header class="top">
<div class="logo">TRAVEL<b>X</b></div>
<nav class="nav"><a href="#home">Home</a><a href="#explore">Explore</a><a href="#packages">Packages</a><a href="#planner">AI Planner</a><a href="#booking">Booking</a></nav>
<div class="navright"><button class="ghost" onclick="toggleDark()">◐</button><button class="ghost" onclick="showDashboard()">Dashboard</button><button class="btn" onclick="openLogin()">Login</button></div>
</header>

<section class="hero" id="home">
<div class="heroinner">
<span class="eyebrow">✦ NEXT-GEN TRAVEL PLATFORM</span>
<h1>Travel smarter.<br><span>Experience more.</span></h1>
<p>A complete travel ecosystem for discovering destinations, building intelligent itineraries and managing bookings — all from one powerful interface.</p>
<div class="search">
<input id="sDest" placeholder="📍 Destination">
<input id="sDate" type="date">
<select id="sType"><option value="">Travel type</option><option>Flight</option><option>Hotel</option><option>Tour Package</option></select>
<select id="sGuest"><option>1 Traveler</option><option>2 Travelers</option><option>3 Travelers</option><option>4 Travelers</option><option>5+ Travelers</option></select>
<button onclick="globalSearch()">EXPLORE</button>
</div>
<div class="metrics"><div><strong>120+</strong><small>Destinations</small></div><div><strong>450+</strong><small>Packages</small></div><div><strong>25K+</strong><small>Travelers</small></div><div><strong>4.9/5</strong><small>User Rating</small></div></div>
</div>
</section>

<section>
<div class="wrap"><div class="heading"><h2>One platform. Every journey.</h2><p>Designed like a real-world travel product, not just a static website.</p></div>
<div class="cards4">
<div class="feature"><div class="ico">🧭</div><h3>Discover</h3><p>Explore destinations, experiences and curated travel packages.</p></div>
<div class="feature"><div class="ico">🤖</div><h3>Smart Planning</h3><p>Generate personalized day-wise itineraries from your preferences.</p></div>
<div class="feature"><div class="ico">🎫</div><h3>Unified Booking</h3><p>Manage destination, dates, travelers and booking details together.</p></div>
<div class="feature"><div class="ico">📊</div><h3>Trip Dashboard</h3><p>View your current booking and trip information in one place.</p></div>
</div></div>
</section>

<section id="explore">
<div class="wrap">
<div class="sectionhead"><div><h2>Explore the world</h2><p style="color:var(--muted);margin-top:6px">Choose a destination that matches your travel mood.</p></div>
<div class="chips"><button class="chip on" onclick="filterCards('all',this)">All</button><button class="chip" onclick="filterCards('mountain',this)">Mountain</button><button class="chip" onclick="filterCards('beach',this)">Beach</button><button class="chip" onclick="filterCards('city',this)">City</button></div></div>
<div class="destgrid">
<div class="card dest" data-cat="mountain"><div class="photo one">🏔️<span class="pill">TOP PICK</span></div><div class="cardbody"><h3>Manali</h3><div class="stars">★★★★★ 4.8</div><p>Snow peaks, valleys and adventure activities.</p><div class="cardfoot"><span class="price">₹12,999+</span><button class="ghost" onclick="choose('Manali')">Plan Trip</button></div></div></div>
<div class="card dest" data-cat="beach"><div class="photo two">🏝️<span class="pill">TRENDING</span></div><div class="cardbody"><h3>Goa</h3><div class="stars">★★★★★ 4.7</div><p>Beaches, nightlife and coastal experiences.</p><div class="cardfoot"><span class="price">₹10,999+</span><button class="ghost" onclick="choose('Goa')">Plan Trip</button></div></div></div>
<div class="card dest" data-cat="city"><div class="photo three">🌆<span class="pill">POPULAR</span></div><div class="cardbody"><h3>Dubai</h3><div class="stars">★★★★★ 4.9</div><p>Luxury, skyline, shopping and desert safari.</p><div class="cardfoot"><span class="price">₹34,999+</span><button class="ghost" onclick="choose('Dubai')">Plan Trip</button></div></div></div>
<div class="card dest" data-cat="city"><div class="photo four">🗼<span class="pill">EUROPE</span></div><div class="cardbody"><h3>Paris</h3><div class="stars">★★★★★ 4.8</div><p>Culture, cuisine, art and iconic landmarks.</p><div class="cardfoot"><span class="price">₹45,999+</span><button class="ghost" onclick="choose('Paris')">Plan Trip</button></div></div></div>
</div></div>
</section>

<section id="packages" style="background:color-mix(in srgb,var(--p) 5%,var(--bg))">
<div class="wrap"><div class="heading"><h2>Curated experiences</h2><p>Packages with accommodation, activities and transfers.</p></div>
<div class="packages">
<div class="package"><div style="font-size:48px">🏖️</div><span class="tag">4 DAYS · 3 NIGHTS</span><h3>Goa Escape</h3><p>Relax by the coast with a balanced sightseeing itinerary.</p><ul><li>✓ Hotel stay</li><li>✓ Breakfast</li><li>✓ Local sightseeing</li><li>✓ Airport transfer</li></ul><b class="price">₹18,999 / person</b><br><button class="btn" style="margin-top:15px" onclick="packageSelect('Goa Escape',18999)">Book Package</button></div>
<div class="package hot"><span class="ribbon">MOST POPULAR</span><div style="font-size:48px">🏔️</div><span class="tag">5 DAYS · 4 NIGHTS</span><h3>Manali Adventure</h3><p>Mountains, activities and scenic Himalayan experiences.</p><ul><li>✓ Mountain hotel</li><li>✓ Breakfast & dinner</li><li>✓ Sightseeing</li><li>✓ Adventure activity</li></ul><b class="price">₹22,999 / person</b><br><button class="btn" style="margin-top:15px" onclick="packageSelect('Manali Adventure',22999)">Book Package</button></div>
<div class="package"><div style="font-size:48px">🌇</div><span class="tag">6 DAYS · 5 NIGHTS</span><h3>Dubai Explorer</h3><p>City highlights, premium stay and desert experiences.</p><ul><li>✓ Premium hotel</li><li>✓ City tour</li><li>✓ Desert safari</li><li>✓ Airport transfer</li></ul><b class="price">₹49,999 / person</b><br><button class="btn" style="margin-top:15px" onclick="packageSelect('Dubai Explorer',49999)">Book Package</button></div>
</div></div>
</section>

<section class="plannerbg" id="planner">
<div class="wrap"><div class="heading"><h2>AI-style Smart Trip Planner</h2><p>Tell us your preferences and generate a complete itinerary.</p></div>
<div class="plannerbox">
<div class="grid2">
<div class="field"><label>Destination</label><input id="pDest" placeholder="e.g. Manali"></div>
<div class="field"><label>Duration</label><select id="pDays"><option>3 Days</option><option selected>4 Days</option><option>5 Days</option><option>7 Days</option></select></div>
<div class="field"><label>Travel Date</label><input id="pDate" type="date"></div>
<div class="field"><label>Travelers</label><select id="pPeople"><option>1</option><option>2</option><option>3</option><option>4</option><option>5+</option></select></div>
<div class="field full"><label>Travel Style</label><select id="pStyle"><option>Adventure</option><option>Relaxation</option><option>Culture & Sightseeing</option><option>Family</option><option>Luxury</option></select></div>
<div class="full"><button class="btn" style="width:100%;padding:15px" onclick="generate()">✦ GENERATE PERSONALIZED ITINERARY</button></div>
</div>
<div class="result" id="result"></div>
</div></div>
</section>

<section id="booking">
<div class="wrap"><div class="heading"><h2>Secure your booking</h2><p>Enter your details and generate a unique booking reference.</p></div>
<div class="bookinglayout">
<div class="bookbox">
<div class="grid2">
<div class="field"><label>Full Name *</label><input id="bName" placeholder="Your name"></div>
<div class="field"><label>Email *</label><input id="bEmail" type="email" placeholder="name@email.com"></div>
<div class="field"><label>Phone *</label><input id="bPhone" placeholder="+91 XXXXX XXXXX"></div>
<div class="field"><label>Booking Type *</label><select id="bType"><option value="">Choose</option><option>Tour Package</option><option>Flight</option><option>Hotel</option></select></div>
<div class="field"><label>Destination *</label><input id="bDest" placeholder="Destination"></div>
<div class="field"><label>Travel Date *</label><input id="bDate" type="date"></div>
<div class="field"><label>Travelers</label><input id="bPeople" type="number" min="1" value="1"></div>
<div class="field"><label>Special Request</label><input id="bReq" placeholder="Optional"></div>
<div class="full"><button class="btn" style="width:100%;padding:15px" onclick="book()">✓ CONFIRM BOOKING</button></div>
</div>
</div>
<div class="summary"><h2>Trip Summary</h2><div class="sumrow"><span>Destination</span><b id="sumD">Not selected</b></div><div class="sumrow"><span>Booking Type</span><b id="sumT">Not selected</b></div><div class="sumrow"><span>Travelers</span><b id="sumP">1</b></div><div class="sumrow"><span>Status</span><b>Ready</b></div><div style="margin-top:22px;padding:14px;background:#ffffff12;border-radius:10px;color:#c7d2fe;font-size:13px">🔒 Demo secure booking flow for academic project.</div></div>
</div></div>
</section>

<section><div class="wrap"><div class="heading"><h2>Traveler feedback</h2><p>Designed around convenience, discovery and simplicity.</p></div>
<div class="reviews"><div class="review"><div class="stars">★★★★★</div><p>“The smart planner turns a destination into a structured trip plan in seconds.”</p><div class="avatar">Aarav · Frequent Traveler</div></div><div class="review"><div class="stars">★★★★★</div><p>“The booking dashboard makes the project feel like a real travel product.”</p><div class="avatar">Mehak · Explorer</div></div><div class="review"><div class="stars">★★★★★</div><p>“Everything from exploring to booking is connected in one interface.”</p><div class="avatar">Rohan · Traveler</div></div></div></div></section>

<footer><div class="footgrid"><div><h2>TRAVELX</h2><p style="margin-top:12px">Smart travel planning and booking platform built as a full-stack-ready academic project.</p></div><div><h3>Platform</h3><ul><li>Explore</li><li>Packages</li><li>Smart Planner</li></ul></div><div><h3>Services</h3><ul><li>Flights</li><li>Hotels</li><li>Tour Packages</li></ul></div><div><h3>Contact</h3><ul><li>support@travelx.com</li><li>+91 98765 43210</li><li>India</li></ul></div></div><div class="copyright">© 2026 TRAVELX · Smart Travel Planning & Booking Platform</div></footer>

<div class="modal" id="login"><div class="modalbox"><span class="x" onclick="closeLogin()">×</span><h2>Welcome back</h2><p style="color:var(--muted);margin:7px 0 15px">Access your travel account.</p><input id="le" placeholder="Email"><input id="lp" type="password" placeholder="Password"><button class="btn" style="width:100%;margin-top:8px" onclick="login()">Sign In</button></div></div>
<div class="dashboard" id="dash"><h3>Trip Dashboard</h3><div class="dashitem"><span>Booking</span><b id="dashId">—</b></div><div class="dashitem"><span>Destination</span><b id="dashDest">—</b></div><div class="dashitem"><span>Status</span><b style="color:#34d399">Active</b></div></div>
<div class="toast" id="toast"></div>

<script>
const $=id=>document.getElementById(id);
function toast(m){$('toast').textContent=m;$('toast').style.display='block';setTimeout(()=>$('toast').style.display='none',2600)}
function toggleDark(){document.body.classList.toggle('dark');localStorage.setItem('travelxDark',document.body.classList.contains('dark'))}
if(localStorage.getItem('travelxDark')==='true')document.body.classList.add('dark');
function globalSearch(){let d=$('sDest').value.trim();if(!d)return toast('Enter a destination first');$('pDest').value=d;choose(d);toast('Destination added to Smart Planner')}
function choose(d){$('pDest').value=d;$('bDest').value=d;$('sumD').textContent=d;$('planner').scrollIntoView({behavior:'smooth'})}
function packageSelect(n,p){$('bDest').value=n;$('bType').value='Tour Package';$('sumD').textContent=n;$('sumT').textContent='Tour Package';$('booking').scrollIntoView({behavior:'smooth'});toast(n+' selected · ₹'+p.toLocaleString())}
function filterCards(cat,btn){document.querySelectorAll('.chip').forEach(x=>x.classList.remove('on'));btn.classList.add('on');document.querySelectorAll('.dest').forEach(x=>x.style.display=cat==='all'||x.dataset.cat===cat?'block':'none')}
function generate(){let d=$('pDest').value.trim();if(!d)return toast('Enter a destination');let days=parseInt($('pDays').value),style=$('pStyle').value,date=$('pDate').value,people=$('pPeople').value;let base=style==='Adventure'?'adventure activities and outdoor experiences':style==='Relaxation'?'leisure, scenic spots and local cuisine':style==='Family'?'family attractions and relaxed sightseeing':style==='Luxury'?'premium experiences, fine dining and exclusive activities':'museums, landmarks, culture and local food';let out='<h3>🧭 '+d+' · '+days+' Day Itinerary</h3><p><b>Travelers:</b> '+people+' &nbsp; <b>Style:</b> '+style+' &nbsp; <b>Date:</b> '+(date||'Flexible')+'</p>';for(let i=1;i<=days;i++){let a=i===1?'Arrival, hotel check-in and local exploration.':i===days?'Shopping, checkout and departure.':`Explore ${d} with ${base}.`;out+='<div><b>Day '+i+':</b> '+a+'</div>'}$('result').innerHTML=out;$('result').style.display='block';toast('Personalized itinerary generated')}
function book(){let n=$('bName').value,e=$('bEmail').value,p=$('bPhone').value,t=$('bType').value,d=$('bDest').value,date=$('bDate').value,people=$('bPeople').value;if(!n||!e||!p||!t||!d||!date)return toast('Please complete all required fields');let id='TX-'+Math.floor(100000+Math.random()*900000);$('dashId').textContent=id;$('dashDest').textContent=d;localStorage.setItem('travelxBooking',JSON.stringify({id,d,n,t,date,people}));alert('BOOKING CONFIRMED\\n\\nReference: '+id+'\\nName: '+n+'\\nDestination: '+d+'\\nType: '+t+'\\nDate: '+date+'\\nTravelers: '+people+'\\n\\nThank you for using TRAVELX!');toast('Booking '+id+' created')}
function openLogin(){$('login').style.display='flex'}function closeLogin(){$('login').style.display='none'}function login(){if(!$('le').value||!$('lp').value)return toast('Enter email and password');closeLogin();toast('Login successful')}
function showDashboard(){let x=$('dash');x.style.display=x.style.display==='block'?'none':'block';let b=JSON.parse(localStorage.getItem('travelxBooking')||'null');if(b){$('dashId').textContent=b.id;$('dashDest').textContent=b.d}}
window.onclick=e=>{if(e.target===$('login'))closeLogin()}
</script>
</body>
</html>

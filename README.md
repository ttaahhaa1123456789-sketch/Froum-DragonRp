# Froum-DragonRp
<!DOCTYPE html>
<html lang="fa">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>فروم Dragon RolePlay</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">
<style>
body{
  margin:0;
  font-family:'Orbitron', sans-serif;
  background: linear-gradient(135deg,#0f1c2c,#1a2b4c);
  color:#fff;
  overflow-x:hidden;
}

/* ===== Navbar Tabs ===== */
.navbar{
  display:flex;
  justify-content:center;
  gap:15px;
  padding:15px;
  background:rgba(0,0,0,0.85);
  position:fixed;
  width:100%;
  top:0;
  z-index:1000;
}
.navbar a{
  text-decoration:none;
  color:#00f7ff;
  padding:8px 15px;
  border-radius:8px;
  transition:.3s;
  font-weight:bold;
}
.navbar a:hover{
  background:#00f7ff;
  color:#000;
  box-shadow:0 0 15px #00f7ff;
}

/* ===== Sections ===== */
.section{
  display:none;
  padding:120px 20px 40px 20px;
  max-width:1200px;
  margin:20px auto;
  border-radius:12px;
  background:rgba(0,0,0,0.6);
  box-shadow:0 0 25px #00f7ff inset;
}
.section.active{
  display:block;
}

/* ===== Cards ===== */
.cards{
  display:flex;
  flex-wrap:wrap;
  justify-content:center;
  gap:25px;
  margin-top:20px;
}
.card{
  background:rgba(0,0,0,0.7);
  padding:15px;
  width:220px;
  border-radius:15px;
  text-align:center;
  box-shadow:0 0 15px #00f7ff;
  transition:.3s;
}
.card img{
  width:100%;
  height:150px;
  object-fit:cover;
  border-radius:10px;
  box-shadow:0 0 10px #00f7ff;
}
.card:hover{
  transform:scale(1.05);
  box-shadow:0 0 25px #f0f;
}

/* ===== Inputs ===== */
input[type="file"], input[type="text"], input[type="password"], select{
  width:100%;
  margin:8px 0;
  padding:10px;
  border-radius:8px;
  border:none;
  font-family: 'Orbitron', sans-serif;
  font-size:16px;
}

/* ===== Buttons ===== */
.btn{
  padding:12px 25px;
  border:none;
  border-radius:12px;
  font-weight:bold;
  cursor:pointer;
  transition:0.3s;
  box-shadow: 0 5px 15px rgba(0,0,0,0.3);
  text-transform: uppercase;
  color:white;
  margin-top:10px;
}
.btn-blue{
  background: linear-gradient(45deg,#1E90FF,#00BFFF);
}
.btn-blue:hover{
  background: linear-gradient(45deg,#00BFFF,#1E90FF);
  transform: scale(1.08);
  box-shadow: 0 8px 20px rgba(0,191,255,0.6);
}
.btn-pink{
  background: linear-gradient(45deg,#FF1493,#FF69B4);
}
.btn-pink:hover{
  background: linear-gradient(45deg,#FF69B4,#FF1493);
  transform: scale(1.08);
  box-shadow: 0 8px 20px rgba(255,20,147,0.6);
}
.btn-green{
  background: linear-gradient(45deg,#32CD32,#00FA9A);
}
.btn-green:hover{
  background: linear-gradient(45deg,#00FA9A,#32CD32);
  transform: scale(1.08);
  box-shadow: 0 8px 20px rgba(50,205,50,0.6);
}
.btn-gold{
  background: linear-gradient(45deg,#FFD700,#FFA500);
  color:#222;
}
.btn-gold:hover{
  background: linear-gradient(45deg,#FFA500,#FFD700);
  transform: scale(1.08);
  box-shadow: 0 8px 20px rgba(255,215,0,0.6);
}

/* ===== Admin Panel ===== */
#adminContent{
  display:none;
  margin-top:20px;
}
.admin-order{
  display:flex;
  justify-content:space-between;
  align-items:center;
  background:rgba(0,255,255,0.1);
  padding:8px;
  margin-bottom:5px;
  border-radius:6px;
}
.admin-order button{
  background:red;
  border:none;
  padding:4px 8px;
  border-radius:5px;
  color:#fff;
  cursor:pointer;
}
.admin-order button:hover{
  background:#ff5555;
}

footer{
  text-align:center;
  padding:20px;
  color:#00f7ff;
}
</style>
</head>
<body>

<nav class="navbar">
  <a href="#" data-target="forumGov">فروم دولت</a>
  <a href="#" data-target="forumGhetto">فروم گتو</a>
  <a href="#" data-target="adminPanel">پنل مدیریت</a>
</nav>

<!-- فروم دولت -->
<section id="forumGov" class="section active">
  <h2>فروم دولت</h2>
  <input type="text" id="gov_accName" placeholder="نام اکانت">
  <input type="text" id="gov_accLevel" placeholder="لول">
  <input type="text" id="gov_accAge" placeholder="سن اکانت">
  <input type="text" id="gov_accOld" placeholder="اکانت سابقه">
  <input type="text" id="gov_factionHistory" placeholder="سابقه در فکشن‌های دولتی">
  <input type="file" id="gov_accImage">
  <input type="text" id="gov_wbook" placeholder="Wbook">
  <input type="text" id="gov_realName" placeholder="نام واقعی">
  <input type="text" id="gov_realAge" placeholder="سن واقعی">
  <input type="text" id="gov_rubikaID" placeholder="آیدی روبیکا">
  <input type="text" id="gov_playTime" placeholder="تایم پلی روزانه">
  <input type="text" id="gov_leadGoal" placeholder="هدف از لیدری">
  
  <!-- فکشن دولت -->
  <h3>انتخاب فکشن</h3>
  <select id="gov_factionSelect">
    <option value="Medic">Medic</option>
    <option value="News">News</option>
    <option value="Army">Army</option>
    <option value="FBI">FBI</option>
    <option value="LsPd">LsPd</option>
  </select>

  <button class="btn btn-gold" onclick="addForum('gov')">ارسال فروم دولت</button>

  <h3>فروم‌های ثبت شده دولت</h3>
  <div class="cards" id="forumsContainerGov"></div>
</section>

<!-- فروم گتو -->
<section id="forumGhetto" class="section">
  <h2>فروم گتو</h2>
  <input type="text" id="ghetto_accName" placeholder="نام اکانت">
  <input type="text" id="ghetto_accLevel" placeholder="لول">
  <input type="text" id="ghetto_accAge" placeholder="سن اکانت">
  <input type="text" id="ghetto_accOld" placeholder="اکانت سابقه">
  <input type="text" id="ghetto_factionHistory" placeholder="سابقه در فکشن‌های گتو">
  <input type="file" id="ghetto_accImage">
  <input type="text" id="ghetto_wbook" placeholder="Wbook">
  <input type="text" id="ghetto_realName" placeholder="نام واقعی">
  <input type="text" id="ghetto_realAge" placeholder="سن واقعی">
  <input type="text" id="ghetto_rubikaID" placeholder="آیدی روبیکا">
  <input type="text" id="ghetto_playTime" placeholder="تایم پلی روزانه">
  <input type="text" id="ghetto_leadGoal" placeholder="هدف از لیدری">

  <!-- فکشن گتو -->
  <h3>انتخاب فکشن گتو</h3>
  <select id="ghetto_factionSelect">
    <option value="Vagos">Vagos</option>
    <option value="Ballas">Ballas</option>
    <option value="Rifa">Rifa</option>
    <option value="Aztecs">Aztecs</option>
    <option value="GroveStreet">Grove Street</option>
  </select>

  <button class="btn btn-pink" onclick="addForumGhetto()">ارسال فروم گتو</button>

  <h3>فروم‌های ثبت شده گتو</h3>
  <div class="cards" id="forumsContainerGhetto"></div>
</section>

<!-- پنل مدیریت -->
<section id="adminPanel" class="section">
  <h2>پنل مدیریت</h2>
  <input type="password" id="adminPass" placeholder="رمز عبور مدیر">
  <button class="btn btn-blue" onclick="checkAdminPass()">ورود</button>
  <div id="adminContent">
    <h3>سفارش‌ها / پست‌ها</h3>
    <div id="orderList"></div>
  </div>
</section>

<footer>
  Tavsot Tim Dragon Rp
</footer>

<script>
const links = document.querySelectorAll('.navbar a');
const sections = document.querySelectorAll('.section');
const forumsContainerGov = document.getElementById('forumsContainerGov');
const forumsContainerGhetto = document.getElementById('forumsContainerGhetto');
const orderList = document.getElementById('orderList');

// Navbar تب‌ها
links.forEach(link=>{
  link.addEventListener('click', e=>{
    e.preventDefault();
    const target = link.getAttribute('data-target');
    sections.forEach(sec=>sec.classList.remove('active'));
    document.getElementById(target).classList.add('active');
  });
});

// تابع ثبت فروم دولت
function addForum(type){
  const accName = document.getElementById('gov_accName').value;
  const leadGoal = document.getElementById('gov_leadGoal').value;
  const factionSelect = document.getElementById('gov_factionSelect').value;
  const file = document.getElementById('gov_accImage').files[0];

  if(!accName || !leadGoal){
    alert("نام اکانت و هدف از لیدری الزامی است!");
    return;
  }

  const postDiv = document.createElement('div');
  postDiv.className = "card";

  // عکس
  if(file){
    const reader = new FileReader();
    reader.onload = function(e){
      const img = document.createElement('img');
      img.src = e.target.result;
      postDiv.appendChild(img);
    }
    reader.readAsDataURL(file);
  }

  const p = document.createElement('p');
  p.innerHTML = `<b>نام اکانت:</b> ${accName}<br>
  <b>هدف از لیدری:</b> ${leadGoal}<br>
  <b>فکشن انتخاب شده:</b> ${factionSelect}`;
  postDiv.appendChild(p);

  forumsContainerGov.prepend(postDiv);

  // اضافه کردن به پنل مدیریت
  const adminDiv = document.createElement('div');
  adminDiv.className = "admin-order";
  adminDiv.innerHTML = `<span>${accName} - ${factionSelect}</span> <button onclick="this.parentElement.remove()">حذف</button>`;
  orderList.prepend(adminDiv);

  document.getElementById('gov_accName').value="";
  document.getElementById('gov_leadGoal').value="";
  document.getElementById('gov_factionSelect').value="Medic";
  document.getElementById('gov_accImage').value="";
}

// تابع ثبت فروم گتو
function addForumGhetto(){
  const accName = document.getElementById('ghetto_accName').value;
  const leadGoal = document.getElementById('ghetto_leadGoal').value;
  const factionSelect = document.getElementById('ghetto_factionSelect').value;
  const file = document.getElementById('ghetto_accImage').files[0];

  if(!accName || !leadGoal){
    alert("نام اکانت و هدف از لیدری الزامی است!");
    return;
  }

  const postDiv = document.createElement('div');
  postDiv.className = "card";

  // عکس
  if(file){
    const reader = new FileReader();
    reader.onload = function(e){
      const img = document.createElement('img');
      img.src = e.target.result;
      postDiv.appendChild(img);
    }
    reader.readAsDataURL(file);
  }

  const p = document.createElement('p');
  p.innerHTML = `<b>نام اکانت:</b> ${accName}<br>
  <b>هدف از لیدری:</b> ${leadGoal}<br>
  <b>فکشن انتخاب شده:</b> ${factionSelect}`;
  postDiv.appendChild(p);

  forumsContainerGhetto.prepend(postDiv);

  // اضافه کردن به پنل مدیریت
  const adminDiv = document.createElement('div');
  adminDiv.className = "admin-order";
  adminDiv.innerHTML = `<span>${accName} - ${factionSelect}</span> <button onclick="this.parentElement.remove()">حذف</button>`;
  orderList.prepend(adminDiv);

  document.getElementById('ghetto_accName').value="";
  document.getElementById('ghetto_leadGoal').value="";
  document.getElementById('ghetto_factionSelect').value="Vagos";
  document.getElementById('ghetto_accImage').value="";
}

// پنل مدیریت
function checkAdminPass(){
  const pass = document.getElementById('adminPass').value;
  if(pass==="123321"){
    document.getElementById('adminContent').style.display="block";
    alert("پنل مدیر فعال شد.");
  } else{
    alert("رمز اشتباه است!");
  }
}
</script>
<!-- Global Music Player -->
<div id="music-player">
  <button id="music-btn">🔊</button>
</div>

<audio id="bg-music" loop>
  <source src="https://uploadkon.ir/uploads/898c16_26Unknown-artist-GTA-Songs-320-.mp3" type="audio/mpeg">
</audio>

<style>
  #music-player {
    position: fixed;
    bottom: 20px;
    left: 20px;
    z-index: 999999;
  }
  
  #music-btn {
    width: 55px;
    height: 55px;
    border-radius: 50%;
    border: none;
    background: linear-gradient(135deg, #00e5ff, #2979ff);
    color: white;
    font-size: 22px;
    box-shadow: 0 0 15px #00e5ff, 0 0 30px #2979ff;
    cursor: pointer;
    transition:
</body>
</html>

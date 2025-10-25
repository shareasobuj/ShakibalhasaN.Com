# ShakibalhasaN.Com

<html lang="bn">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Shakib Al Hasan — Complete Fan / Info Site</title>

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" />

  <style>
    :root { --brand:#0b7a4d; }
    body { background:#f8f9fa; padding-top:70px; font-family: 'Helvetica Neue', Arial, sans-serif; }
    .navbar { background: var(--brand); }
    .navbar-brand, .nav-link { color: #fff !important; }
    .hero { background: linear-gradient(180deg, rgba(11,122,77,0.95), rgba(7,90,58,0.95)); color:#fff; padding:60px 20px; text-align:center; }
    .hero h1 { font-size: 2.6rem; margin-bottom:.3rem; }
    .card-img-thumb { object-fit:cover; height:200px; width:100%; border-radius:8px; }
    footer { background: var(--brand); color: #fff; padding:12px 0; margin-top:40px; }
    .admin-badge { position: fixed; right: 18px; bottom: 18px; z-index: 1100; }
    .page-section { padding: 30px 0; }
    .small-muted { color:#6c757d; font-size:.9rem; }
    .note-box { background:#fff3cd; padding:12px; border-radius:6px; border:1px solid #ffeeba; }
  </style>
</head>
<body>
<nav class="navbar fixed-top">
  <div class="container">
    <a class="navbar-brand" href="#" onclick="showPage('home')">Shakib Al Hasan</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navmenu">
      <span class="navbar-toggler-icon" style="color:#fff">☰</span>
    </button>
    <div class="collapse navbar-collapse" id="navmenu">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link" href="#" onclick="showPage('home')">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="#" onclick="showPage('biography')">Biography</a></li>
        <li class="nav-item"><a class="nav-link" href="#" onclick="showPage('career')">Career</a></li>
        <li class="nav-item"><a class="nav-link" href="#" onclick="showPage('achievements')">Achievements</a></li>
        <li class="nav-item"><a class="nav-link" href="#" onclick="showPage('records')">Records</a></li>
        <li class="nav-item"><a class="nav-link" href="#" onclick="showPage('gallery')">Gallery</a></li>
        <li class="nav-item"><a class="nav-link" href="#" onclick="showPage('media')">Media</a></li>
        <li class="nav-item"><a class="nav-link" href="#" onclick="showPage('contact')">Contact</a></li>
        <li class="nav-item"><a class="nav-link" href="#" onclick="showPage('admin')">Admin</a></li>
      </ul>
    </div>
  </div>
</nav>

<div class="container" id="main-content"></div>

<footer>
  <div class="container text-center">
    <small>© 2025 Shakib Al Hasan Fan/Info Site</small>
  </div>
</footer>

<script>
const pages = {
  home: `<div class="hero"><h1>শাকিব আল হাসান</h1><p>বিশ্বের সেরা অলরাউন্ডার ক্রিকেটার</p></div>`,
  biography: `<div class="page-section"><h2>Biography</h2><p>শাকিব আল হাসান বাংলাদেশের কিংবদন্তি ক্রিকেটার, অলরাউন্ডার হিসেবে বিশ্বে সেরা। জন্ম: ২৪ মার্চ ১৯৮৭, মাগুরা, বাংলাদেশ।</p></div>`,
  career: `<div class="page-section"><h2>Career</h2><p>শাকিব জাতীয় এবং আন্তর্জাতিক ক্রিকেটে অসাধারণ পারফরম্যান্স দেখিয়েছেন। ওয়ার্ল্ড টি-২০, ওয়ানডে এবং টেস্টে গুরুত্বপূর্ণ অবদান।</p></div>`,
  achievements: `<div class="page-section"><h2>Achievements</h2><ul><li>ICC Player of the Year 2012</li><li>Multiple double centuries</li><li>Captain of Bangladesh National Team</li></ul></div>`,
  records: `<div class="page-section"><h2>Records</h2><ul><li>Bangladesh highest wicket-taker in Tests & ODIs</li><li>Leading all-rounder in ICC rankings</li></ul></div>`,
  gallery: `<div class="page-section"><h2>Gallery</h2><div class="row"><div class="col-md-4 mb-3"><img class="card-img-thumb" src="https://i.ibb.co/W2Z4j9X/shakib1.jpg" alt="Shakib"></div><div class="col-md-4 mb-3"><img class="card-img-thumb" src="https://i.ibb.co/0yFh0yJ/shakib2.jpg" alt="Shakib"></div><div class="col-md-4 mb-3"><img class="card-img-thumb" src="https://i.ibb.co/Wk6zVt2/shakib3.jpg" alt="Shakib"></div></div></div>`,
  media: `<div class="page-section"><h2>Media</h2><p>শাকিবের সাম্প্রতিক খেলার ভিডিও ও সংবাদ:</p><iframe width="100%" height="315" src="https://www.youtube.com/embed/abcd1234" frameborder="0" allowfullscreen></iframe></div>`,
  contact: `<div class="page-section"><h2>Contact</h2><p>সরাসরি যোগাযোগের জন্য ফর্ম:</p><form><input class="form-control mb-2" placeholder="Name"><input class="form-control mb-2" placeholder="Email"><textarea class="form-control mb-2" placeholder="Message"></textarea><button class="btn btn-success">Send</button></form></div>`,
  admin: `<div class="page-section"><h2>Admin Panel</h2><p>এইখানে Frontend simulation ব্যবহার করে ডেটা update করা যাবে।</p></div>`
};

function showPage(page){
  const container = document.getElementById('main-content');
  container.innerHTML = pages[page] || `<p>Page not found.</p>`;
}

// default page
showPage('home');
</script>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>


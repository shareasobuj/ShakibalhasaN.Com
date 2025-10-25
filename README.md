# ShakibalhasaN.Com

<html lang="bn">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Shakib Al Hasan — Complete Fan / Info Site</title>

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" />

  <!-- React + ReactDOM + Babel -->
  <script src="https://unpkg.com/react@18/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>

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
<div id="root"></div>

<script type="text/babel">

const { useState, useEffect } = React;

function App(){
  const [page, setPage] = useState('home');
  const [session, setSession] = useState(null);

  function handleLogin(email, pass) { /* Part 4 এ যোগ করা হবে */ }
  function handleSignup(name, email, pass) { /* Part 4 এ যোগ করা হবে */ }
  function handleLogout() { setSession(null); setPage('home'); }

  return (
    <div>
      <Navbar page={page} setPage={setPage} session={session} onLogout={handleLogout} />

      <main className="container">
        {/* Pages will be inserted here in Part 2 & Part 3 */}
      </main>

      {session && <div className="admin-badge">
        <div className="card shadow-sm">
          <div className="card-body p-2">
            <small>Signed in as <strong>{session.name}</strong></small>
            <div className="mt-2 d-flex gap-2">
              <button className="btn btn-sm btn-outline-primary" onClick={()=>setPage('admin')}>Admin</button>
              <button className="btn btn-sm btn-outline-danger" onClick={handleLogout}>Logout</button>
            </div>
          </div>
        </div>
      </div>}

      <Footer />
    </div>
  );
}

/* ---------- Navbar ---------- */
function Navbar({ page, setPage, session, onLogout }) {
  return (
    <nav className="navbar fixed-top">
      <div className="container">
        <a className="navbar-brand" href="#" onClick={(e)=>{e.preventDefault(); setPage('home');}}>Shakib Al Hasan</a>
        <button className="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navmenu">
          <span className="navbar-toggler-icon" style={{color:'#fff'}}>☰</span>
        </button>
        <div className="collapse navbar-collapse" id="navmenu">
          <ul className="navbar-nav ms-auto">
            <li className="nav-item"><a className="nav-link" href="#" onClick={(e)=>{e.preventDefault(); setPage('home');}}>Home</a></li>
            <li className="nav-item"><a className="nav-link" href="#" onClick={(e)=>{e.preventDefault(); setPage('biography');}}>Biography</a></li>
            <li className="nav-item"><a className="nav-link" href="#" onClick={(e)=>{e.preventDefault(); setPage('career');}}>Career</a></li>
            <li className="nav-item"><a className="nav-link" href="#" onClick={(e)=>{e.preventDefault(); setPage('achievements');}}>Achievements</a></li>
            <li className="nav-item"><a className="nav-link" href="#" onClick={(e)=>{e.preventDefault(); setPage('records');}}>Records</a></li>
            <li className="nav-item"><a className="nav-link" href="#" onClick={(e)=>{e.preventDefault(); setPage('gallery');}}>Gallery</a></li>
            <li className="nav-item"><a className="nav-link" href="#" onClick={(e)=>{e.preventDefault(); setPage('media');}}>Media</a></li>
            <li className="nav-item"><a className="nav-link" href="#" onClick={(e)=>{e.preventDefault(); setPage('contact');}}>Contact</a></li>
            <li className="nav-item">
              {session ?
                <a className="nav-link" href="#" onClick={(e)=>{e.preventDefault(); setPage('admin');}}>Admin</a> :
                <a className="nav-link" href="#" onClick={(e)=>{e.preventDefault(); setPage('login');}}>Admin Login</a>
              }
            </li>
          </ul>
        </div>
      </div>
    </nav>
  );
}

/* ---------- Footer ---------- */
function Footer() {
  return (
    <footer>
      <div className="container text-center">
        <small>© {new Date().getFullYear()} Shakib Al Hasan Fan/Info Site</small>
      </div>
    </footer>
  );
}

ReactDOM.createRoot(document.getElementById('root')).render(<App />);
</script>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>


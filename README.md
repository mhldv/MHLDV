```css
:root {
  --bg: #f8fafc;
  --card: #ffffff;
  --ink: #0f172a;
  --muted: #64748b;
  --brand: #0ea5e9;
  --brand2: #6366f1;
  --ok: #10b981;
  --line: #e2e8f0;
  --shadow: 0 20px 60px rgba(15, 23, 42, 0.08);
  --radius: 20px;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Inter, ui-sans-serif, system-ui, Segoe UI, Roboto, sans-serif;
  background: linear-gradient(180deg, #f0f9ff 0%, #f8fafc 40%, #ffffff 100%);
  color: var(--ink);
}

.container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 28px 20px;
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px 0;
}

.logo {
  display: flex;
  gap: 12px;
  align-items: center;
  font-weight: 800;
  letter-spacing: -0.02em;
}

.logo i {
  width: 40px;
  height: 40px;
  border-radius: 12px;
  display: grid;
  place-items: center;
  background: linear-gradient(135deg, var(--brand), var(--brand2));
  color: white;
  box-shadow: var(--shadow);
}

.badge {
  padding: 6px 12px;
  border-radius: 999px;
  background: #e0f2fe;
  color: #0369a1;
  font-size: 12px;
  font-weight: 700;
}

.hero {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  gap: 28px;
  padding: 28px 0 10px;
}

@media (max-width: 900px) {
  .hero {
    grid-template-columns: 1fr;
  }
}

.h1 {
  font-size: 42px;
  line-height: 0.95;
  letter-spacing: -0.03em;
  font-weight: 900;
}

.h1 span {
  background: linear-gradient(90deg, var(--brand), var(--brand2));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.sub {
  color: var(--muted);
  font-size: 17px;
  line-height: 1.6;
  margin-top: 12px;
}

.card {
  background: var(--card);
  border: 1px solid var(--line);
  border-radius: var(--radius);
  box-shadow: var(--shadow);
  padding: 22px;
}

.grid3 {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
}

@media (max-width: 900px) {
  .grid3 {
    grid-template-columns: 1fr;
  }
}

.course-card {
  transition: 0.25s;
  cursor: pointer;
}

.course-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 30px 80px rgba(15, 23, 42, 0.12);
}

.course-card .top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 10px;
}

.course-card h3 {
  margin: 6px 0 8px;
  font-size: 18px;
}

.meta {
  color: var(--muted);
  font-size: 13px;
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
}

.btn {
  appearance: none;
  border: 0;
  border-radius: 999px;
  padding: 12px 18px;
  font-weight: 700;
  cursor: pointer;
  transition: 0.2s;
}

.btn-primary {
  background: linear-gradient(90deg, var(--brand), var(--brand2));
  color: white;
  box-shadow: 0 10px 20px rgba(14, 165, 233, 0.25);
}

.btn-primary:hover {
  filter: brightness(1.05);
  transform: translateY(-1px);
}

.btn-ghost {
  background: #f1f5f9;
  color: var(--ink);
}

.lesson-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: grid;
  gap: 10px;
}

.lesson-item {
  display: flex;
  gap: 12px;
  align-items: center;
  padding: 12px 14px;
  border: 1px solid var(--line);
  border-radius: 14px;
  background: #ffffff;
}

.lesson-item.active {
  border-color: var(--brand);
  background: #f0f9ff;
}

.num {
  width: 32px;
  height: 32px;
  border-radius: 10px;
  background: #0f172a;
  color: #ffffff;
  display: grid;
  place-items: center;
  font-size: 13px;
  font-weight: 800;
  flex-shrink: 0;
}

.progress {
  height: 10px;
  background: #e2e8f0;
  border-radius: 999px;
  overflow: hidden;
}

.progress i {
  display: block;
  height: 100%;
  background: linear-gradient(90deg, var(--brand), var(--brand2));
  width: 0%;
  transition: 0.4s;
}

.quiz {
  margin-top: 18px;
}

.q {
  padding: 18px;
  border: 1px solid var(--line);
  border-radius: 16px;
  margin-bottom: 14px;
  background: white;
}

.q h4 {
  margin: 0 0 10px;
  font-size: 15px;
}

.opt {
  display: flex;
  gap: 10px;
  align-items: center;
  padding: 10px 12px;
  border-radius: 12px;
  border: 1px solid transparent;
  cursor: pointer;
  margin-top: 8px;
  background: #f8fafc;
}

.opt:hover {
  background: #f1f5f9;
}

.opt.correct {
  background: #dcfce7;
  border-color: #86efac;
}

.opt.wrong {
  background: #fee2e2;
  border-color: #fca5a5;
}

.certificate {
  position: relative;
  background: radial-gradient(1200px 500px at 20% -10%, #e0f2fe, transparent), radial-gradient(800px 400px at 100% 0%, #e0e7ff, transparent), white;
  border: 1.5px solid #0f172a;
  border-radius: 24px;
  padding: 36px;
  text-align: center;
  overflow: hidden;
}

.certificate:before {
  content: '';
  position: absolute;
  inset: 10px;
  border: 1px dashed #cbd5e1;
  border-radius: 16px;
  pointer-events: none;
}

.cert-title {
  font-family: Georgia, serif;
  font-size: 34px;
  font-weight: 800;
  letter-spacing: -0.02em;
}

.cert-sub {
  color: var(--muted);
  margin-top: 6px;
}

.seal {
  width: 86px;
  height: 86px;
  border-radius: 50%;
  background: linear-gradient(135deg, #0f172a, #334155);
  color: white;
  display: grid;
  place-items: center;
  margin: 18px auto;
  font-weight: 900;
  box-shadow: var(--shadow);
}

.qr-box {
  display: flex;
  gap: 18px;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  margin-top: 16px;
}

.input {
  width: 100%;
  padding: 14px 16px;
  border-radius: 14px;
  border: 1px solid var(--line);
  font-size: 15px;
}

.input:focus {
  outline: 2px solid #bae6fd;
  border-color: transparent;
}

.pill {
  display: inline-flex;
  gap: 8px;
  align-items: center;
  padding: 8px 12px;
  border-radius: 999px;
  background: #f1f5f9;
  font-size: 12px;
  font-weight: 700;
}

.verify-hero {
  text-align: center;
  padding: 40px 0;
}

.kbd {
  font-family: monospace;
  background: #0f172a;
  color: #ffffff;
  padding: 3px 8px;
  border-radius: 6px;
  font-size: 12px;
}
```

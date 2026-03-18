---
title: "Обо мне"
description: "Alex Ma — Data Engineer / Analyst"
showRecent: false
---

<style>
/* ───── Layout ───── */
.about-card {
  display: flex;
  gap: 2rem;
  align-items: flex-start;
  padding: 1.5rem;
  border: 1px solid color-mix(in srgb, currentColor 20%, transparent);
  border-radius: 8px;
  margin-bottom: 1.5rem;
}
.about-card__photo {
  flex-shrink: 0;
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
  object-position: center top;
}
.about-card__info {
  flex: 1;
}
.about-card__name {
  font-size: 1.4rem;
  font-weight: 700;
  margin: 0 0 0.25rem;
}
.about-card__role {
  font-size: 0.95rem;
  opacity: 0.7;
  margin: 0 0 0.8rem;
}
.about-card__meta {
  display: grid;
  grid-template-columns: auto 1fr;
  gap: 0.2rem 0.75rem;
  font-size: 0.9rem;
  line-height: 1.6;
}
.about-card__meta dt {
  opacity: 0.6;
  white-space: nowrap;
  grid-column: 1;
}
.about-card__meta dd {
  margin: 0;
  grid-column: 2;
}

/* ───── Toggle ───── */
.about-toggle-bar {
  margin: 1rem 0 1.5rem;
}
.about-toggle-btn {
  padding: 0.35rem 1.1rem;
  cursor: pointer;
  border-radius: 4px;
  border: 1px solid currentColor;
  background: transparent;
  font-size: 0.9rem;
  font-family: inherit;
}

/* ───── Section content visibility ───── */
.full-only {
  display: none;
}
.brief-only {
  display: block;
}
.about-expanded .full-only {
  display: block;
}
.about-expanded .brief-only {
  display: none;
}

/* ───── Section layout ───── */
.about-section-content {
  margin-bottom: 0.5rem;
}
.about-field {
  display: grid;
  grid-template-columns: auto 1fr;
  gap: 0.15rem 0.75rem;
  font-size: 0.95rem;
  line-height: 1.7;
  margin-bottom: 0.5rem;
}
.about-field dt {
  opacity: 0.6;
  white-space: nowrap;
  font-weight: 500;
  grid-column: 1;
}
.about-field dd {
  margin: 0;
  grid-column: 2;
}
.about-item {
  margin-bottom: 0.8rem;
}
.about-item strong {
  display: block;
}
.about-item span {
  font-size: 0.88rem;
  opacity: 0.75;
}

/* ───── Print ───── */
@media print {
  .about-toggle-bar,
  nav,
  header,
  footer,
  aside,
  .full-only {
    display: none !important;
  }
  .brief-only {
    display: block !important;
  }
  .about-card {
    border: 1px solid #ccc;
    break-inside: avoid;
  }
  body, .prose {
    font-size: 11pt;
  }
}
</style>

<div class="about-card">
  <img class="about-card__photo" src="/img/avatar.jpg" alt="Alex Ma">
  <div class="about-card__info">
    <p class="about-card__name">Alex Ma</p>
    <p class="about-card__role">Data Engineer · Data Analyst</p>
    <dl class="about-card__meta">
      <dt>Дата рождения</dt><dd>20.02.2002</dd>
      <dt>Город</dt><dd>Омск</dd>
      <dt>Статус занятости</dt><dd>Открыт к сотрудничеству</dd>
      <dt>Ожидаемая з/п</dt><dd>от 350 000 р. / мес.</dd>
    </dl>
  </div>
</div>

<div class="about-toggle-bar">
  <button id="about-toggle-btn" class="about-toggle-btn" onclick="toggleAbout()">Подробнее ↓</button>
</div>

<div id="about-body">

---

## Образование

<div class="brief-only about-section-content">
<div class="about-item">
<strong>Экономист</strong>
<span>Омский государственный университет им. Ф.М. Достоевского · Экономический факультет · Экономическая теория</span>
</div>
</div>

<div class="full-only about-section-content">
<div class="about-item">
<strong>Аспирантура</strong>
<span>Омкий государственный университет им. Ф.М. Достоевского · Экономический факультет</span>
</div>
</div>

<div class="full-only about-section-content">
<div class="about-item">
<strong>Бакалавр</strong>
<span>Омский государственный технический университет · Факультет транспорта, нефти и газа · Проектирование, сооружение и эксплуатация газонефтепроводов и газонефтехранилищ</span>
</div>
</div>

<h3>Дополнительное</h3>

<div class="about-section-content">
<div class="about-item">
<strong>Управление данными (data-driven), бизнес-анализ · 2025 · 80 ч.</strong>
<span>ФГБОУВО «Уфимский государственный нефтяной технический университет»</span>
</div>
<div class="about-item">
<strong>Аналитик данных · 2022–2023 · 350 ч.</strong>
<span>АНО ДПО «Образовательные технологии Яндекса»</span>
</div>
</div>

---

## В сети

<div class="full-only"><h3>Контроль версий</h3></div>

<div class="brief-only about-section-content">
<div class="about-item">
<strong>GitHub · <a href="https://github.com/A1eksMa">A1eksMa</a></strong>
</div>
</div>

<div class="full-only about-section-content">
<div class="about-item">
<strong>GitHub · <a href="https://github.com/A1eksMa">A1eksMa</a></strong>
<span>Международная платформа. Код, проекты с открытым исходным кодом, портфолио.</span>
</div>
<div class="about-item">
<strong>GitVerse · <a href="https://gitverse.ru/a1ex_ma">a1ex_ma</a></strong>
<span>Российская платформа контроля версий. Проекты для русскоязычного сообщества.</span>
</div>
</div>

<div class="full-only"><h3>Учебные платформы</h3></div>

<div class="brief-only about-section-content">
<div class="about-item">
<strong>LeetCode · <a href="https://leetcode.com/u/a1ex_ma">a1ex_ma</a></strong>
</div>
</div>

<div class="full-only about-section-content">
<div class="about-item">
<strong>LeetCode · <a href="https://leetcode.com/u/a1ex_ma">a1ex_ma</a></strong>
<span>Практика решения алгоритмических задач. Редко нахожу на это время, но стараюсь не забрасывать.</span>
</div>
<div class="about-item">
<strong>JavaRush · <a href="https://javarush.com/users/3534015">a1ex_ma</a></strong>
<span>Интерактивный курс Java с упором на практику.</span>
</div>
</div>

<div class="full-only">
<h3>Социальные сети</h3>
<div class="about-section-content">
<div class="about-item">
<strong>Discord · @a1ex_ma</strong>
<span>Аудио- и видеосвязь, голосовые чаты, рабочие обсуждения и коллаборации.</span>
</div>
<div class="about-item">
<strong>ВКонтакте · <a href="https://vk.com/a1ex_ma">a1ex_ma</a></strong>
<span>Когда я не программирую — рисую. Здесь вы найдёте витрину моих работ.</span>
</div>
</div>
</div>

---

## Контакты

<dl class="about-field">
<dt>Email</dt>
<dd><a href="mailto:a1ex_ma@mail.ru">a1ex_ma@mail.ru</a></dd>
<dt>Телефон</dt>
<dd>
<details>
<summary>Показать номер</summary>
+7 (XXX) XXX-XX-XX
</details>
</dd>
</dl>

<div class="full-only"><h3>Мессенджеры</h3></div>

<dl class="about-field brief-only">
<dt>Telegram</dt>
<dd><a href="https://t.me/a1ex_ma">@a1ex_ma</a></dd>
</dl>

<dl class="about-field full-only">
<dt>Telegram</dt>
<dd><a href="https://t.me/a1ex_ma">@a1ex_ma</a> — Предпочтительный способ связи</dd>
<dt>MAX</dt>
<dd>@a1ex_ma</dd>
<dt>WhatsApp</dt>
<dd>@a1ex_ma</dd>
</dl>

</div><!-- #about-body -->

<script>
function toggleAbout() {
  var body = document.getElementById('about-body');
  var btn = document.getElementById('about-toggle-btn');
  var expanded = body.classList.toggle('about-expanded');
  btn.textContent = expanded ? 'Кратко ↑' : 'Подробнее ↓';
}
</script>

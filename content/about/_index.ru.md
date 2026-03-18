---
title: "Обо мне"
description: "Alex Ma — Data Engineer / Analyst"
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
}
.about-card__meta dd {
  margin: 0;
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
}
.about-field dd {
  margin: 0;
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
      <dt>Дата рождения</dt><dd>20 февраля 2002</dd>
      <dt>Город</dt><dd>Омск</dd>
      <dt>Статус</dt><dd>Открыт к предложениям</dd>
      <dt>Email</dt><dd><a href="mailto:a1ex_ma@mail.ru">a1ex_ma@mail.ru</a></dd>
      <dt>Telegram</dt><dd><a href="https://t.me/a1ex_ma">@a1ex_ma</a></dd>
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
<strong>Омский государственный университет им. Ф.М. Достоевского</strong>
<span>Экономический факультет · Экономическая теория · 2003</span>
</div>
</div>

<div class="full-only about-section-content">
<div class="about-item">
<strong>Омский государственный университет им. Ф.М. Достоевского</strong>
<span>Экономический факультет · Экономическая теория · 2003</span>
</div>
<div class="about-item">
<strong>Омский государственный технический университет</strong>
<span>Факультет транспорта, нефти и газа · Проектирование, сооружение и эксплуатация газонефтепроводов и газонефтехранилищ · 2016</span>
</div>
</div>

---

## Дополнительное образование

<div class="brief-only about-section-content">
<em>Доступно в полном режиме</em>
</div>

<div class="full-only about-section-content">
<div class="about-item">
<strong>АНО ДПО «Образовательные технологии Яндекса»</strong>
<span>Аналитик данных · 2022–2023 · 350 ч.</span>
</div>
<div class="about-item">
<strong>ФГБОУ ВО «Уфимский государственный нефтяной технический университет»</strong>
<span>Управление данными (data-driven), бизнес-анализ · 2025 · 80 ч.</span>
</div>
</div>

---

## Системы контроля версий

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

---

## Социальные сети

<div class="brief-only about-section-content">
<div class="about-item">
<strong>ВКонтакте · <a href="https://vk.com/a1ex_ma">a1ex_ma</a></strong>
</div>
<div class="about-item">
<strong>LeetCode · <a href="https://leetcode.com/u/a1ex_ma">a1ex_ma</a></strong>
</div>
</div>

<div class="full-only about-section-content">
<div class="about-item">
<strong>Discord · @a1ex_ma</strong>
<span>Аудио- и видеосвязь, голосовые чаты, рабочие обсуждения и коллаборации.</span>
</div>
<div class="about-item">
<strong>ВКонтакте · <a href="https://vk.com/a1ex_ma">a1ex_ma</a></strong>
<span>Когда я не программирую — рисую. Здесь вы найдёте витрину моих работ.</span>
</div>
<div class="about-item">
<strong>LeetCode · <a href="https://leetcode.com/u/a1ex_ma">a1ex_ma</a></strong>
<span>Практика решения алгоритмических задач. Редко нахожу на это время, но стараюсь не забрасывать.</span>
</div>
</div>

---

## Мессенджеры

<div class="brief-only about-section-content">
<div class="about-item">
<strong>Telegram · <a href="https://t.me/a1ex_ma">@a1ex_ma</a></strong>
<span>Предпочтительный способ связи по рабочим вопросам</span>
</div>
</div>

<div class="full-only about-section-content">
<div class="about-item">
<strong>Telegram · <a href="https://t.me/a1ex_ma">@a1ex_ma</a></strong>
<span>Предпочтительный способ связи по рабочим вопросам</span>
</div>
<div class="about-item">
<strong>MAX · @a1ex_ma</strong>
</div>
<div class="about-item">
<strong>WhatsApp · @a1ex_ma</strong>
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

</div><!-- #about-body -->

<script>
function toggleAbout() {
  var body = document.getElementById('about-body');
  var btn = document.getElementById('about-toggle-btn');
  var expanded = body.classList.toggle('about-expanded');
  btn.textContent = expanded ? 'Кратко ↑' : 'Подробнее ↓';
}
</script>

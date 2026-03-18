---
title: "Обо мне"
description: "Alex Ma — Data Engineer / Analyst"
layout: "single"
showAuthor: false
---

<style>
/* ───── Layout ───── */
.about-card {
  display: flex;
  gap: 2rem;
  align-items: stretch;
  padding: 1.5rem;
  border: 1px solid color-mix(in srgb, currentColor 20%, transparent);
  border-radius: 8px;
  margin-bottom: 1.5rem;
}
.about-card__photo-wrap {
  flex-shrink: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.6rem;
}
.about-card__photo {
  flex: 1;
  width: auto;
  min-width: 120px;
  max-width: 220px;
  aspect-ratio: 1;
  border-radius: 50%;
  object-fit: cover;
  object-position: center top;
}
.about-card__social {
  display: flex;
  gap: 0.65rem;
}
.about-card__social a {
  opacity: 0.55;
  color: inherit;
  line-height: 0;
}
.about-card__social a:hover {
  opacity: 1;
}
.about-card__social svg {
  width: 20px;
  height: 20px;
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
  margin: 0 0 1.6rem;
}
.about-card__meta {
  display: grid;
  grid-template-columns: auto 1fr;
  gap: 0.2rem 0.75rem;
  font-size: 0.9rem;
  line-height: 1.6;
}
.about-card__meta-key {
  opacity: 0.6;
  white-space: nowrap;
}

/* ───── Toggle ───── */
.about-toggle-bar {
  margin: 1rem 0 1.5rem;
}

/* ───── Section content visibility ───── */
.full-only {
  display: none;
}
.brief-only {
  display: block;
}
.about-field.full-only {
  display: none;
}
.about-expanded .full-only {
  display: block;
}
.about-expanded .full-only.about-field {
  display: grid;
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
.about-field-key {
  opacity: 0.6;
  white-space: nowrap;
  font-weight: 500;
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

/* ───── Section headings ───── */
#about-body h2 {
  background: rgba(var(--color-primary-500), 0.22);
  border-radius: 6px;
  padding: 0.2em 0.6em;
  margin-left: -0.6em;
}
#about-body h3 {
  background: rgba(var(--color-primary-400), 0.09);
  border-radius: 5px;
  padding: 0.15em 0.5em;
  margin-left: -0.5em;
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
  #about-body h2,
  #about-body h3 {
    background: none;
    padding: 0;
    margin-left: 0;
  }
  body, .prose {
    font-size: 11pt;
  }
}
</style>

<div class="about-card">
  <div class="about-card__photo-wrap">
    <img class="about-card__photo" src="/img/avatar.jpg" alt="Alex Ma">
    <div class="about-card__social">
      {{< author-links >}}
    </div>
  </div>
  <div class="about-card__info">
    <p class="about-card__name">Alex Ma</p>
    <p class="about-card__role">Data Scientist · Software Developer</p>
    <div class="about-card__meta">
      <span class="about-card__meta-key">Дата рождения</span><span>20.02.2002</span>
      <span class="about-card__meta-key">Город</span><span>Омск</span>
      <span class="about-card__meta-key">Статус</span><span>Безработный айтишник</span>
      <span class="about-card__meta-key">Ожидаемая з/п</span><span>от 350 000 р. / мес.</span>
    </div>
  </div>
</div>

<div class="about-toggle-bar">
  <button id="about-toggle-btn" class="inline-block !rounded-md bg-primary-600 px-4 py-1 !text-neutral hover:!bg-primary-500 dark:bg-primary-800 dark:hover:!bg-primary-700" onclick="toggleAbout()">Подробнее ↓</button>
</div>

<div id="about-body">

## Образование

<div class="about-section-content">
<div class="about-item">
<strong>Экономист</strong>
<span>Омский государственный университет им. Ф.М. Достоевского · Экономический факультет · Экономическая теория</span>
</div>
</div>

<div class="full-only about-section-content">
<div class="about-item">
<strong>Аспирантура</strong>
<span>Омский государственный университет им. Ф.М. Достоевского · Экономический факультет</span>
</div>
</div>

<div class="full-only about-section-content">
<div class="about-item">
<strong>Бакалавр</strong>
<span>Омский государственный технический университет · Факультет транспорта, нефти и газа · Проектирование, сооружение и эксплуатация газонефтепроводов и газонефтехранилищ</span>
</div>
</div>

<h3>Дополнительное образование</h3>

<div class="about-section-content">
<div class="about-item">
<strong>Управление данными (data-driven), бизнес-анализ</strong>
<span>ФГБОУВО «Уфимский государственный нефтяной технический университет» · 2025 · 80 ч.</span>
</div>
<div class="about-item">
<strong>Аналитик данных</strong>
<span>АНО ДПО «Образовательные технологии Яндекса» · 2022–2023 · 350 ч.</span>
</div>
</div>

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
<strong>Discord · <a href="https://discord.gg/3MMgWb62mn">@a1ex_ma</a></strong>
<span>Аудио- и видеосвязь, голосовые чаты, рабочие обсуждения и коллаборации.</span>
</div>
<div class="about-item">
<strong>ВКонтакте · <a href="https://vk.com/a1ex_ma">a1ex_ma</a></strong>
<span>Когда я не программирую — я рисую, чтобы немного разгрузить мозг. Здесь вы найдёте витрину моих работ.</span>
</div>
</div>
</div>

## Контакты

<div class="about-field">
<span class="about-field-key">Email</span><span><a href="mailto:a1ex_ma@mail.ru">a1ex_ma@mail.ru</a></span>
<span class="about-field-key">Телефон</span><span><details><summary>Показать номер</summary>+7 (XXX) XXX-XX-XX</details></span>
<span class="about-field-key brief-only">Telegram</span><span class="brief-only"><a href="https://t.me/a1ex_ma">@a1ex_ma</a></span>
</div>

<div class="full-only"><h3>Мессенджеры</h3></div>

<div class="about-field full-only">
<span class="about-field-key">Telegram</span><span><a href="https://t.me/a1ex_ma">@a1ex_ma</a> — Предпочтительный способ связи</span>
<span class="about-field-key">MAX</span><span><a href="https://max.ru/u/a1ex_ma">@a1ex_ma</a></span>
<span class="about-field-key">WhatsApp</span><span><a href="https://wa.me/7xxxxxxxxxx">@a1ex_ma</a></span>
</div>

</div><!-- #about-body -->

<script>
function toggleAbout() {
  var body = document.getElementById('about-body');
  var btn = document.getElementById('about-toggle-btn');
  var expanded = body.classList.toggle('about-expanded');
  btn.textContent = expanded ? 'Кратко ↑' : 'Подробнее ↓';
}
</script>

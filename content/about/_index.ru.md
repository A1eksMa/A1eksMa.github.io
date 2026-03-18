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
.about-card__photo-wrap {
  flex-shrink: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.6rem;
}
.about-card__photo {
  width: 150px;
  height: 150px;
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
  margin: 0 0 0.8rem;
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
  <div class="about-card__photo-wrap">
    <img class="about-card__photo" src="/img/avatar.jpg" alt="Alex Ma">
    <div class="about-card__social">
      <a href="https://github.com/A1eksMa" title="GitHub" target="_blank" rel="noopener"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 496 512"><path fill="currentColor" d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"/></svg></a>
      <a href="https://t.me/a1ex_ma" title="Telegram" target="_blank" rel="noopener"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 496 512"><path fill="currentColor" d="M248,8C111.033,8,0,119.033,0,256S111.033,504,248,504,496,392.967,496,256,384.967,8,248,8ZM362.952,176.66c-3.732,39.215-19.881,134.378-28.1,178.3-3.476,18.584-10.322,24.816-16.948,25.425-14.4,1.326-25.338-9.517-39.287-18.661-21.827-14.308-34.158-23.215-55.346-37.177-24.485-16.135-8.612-25,5.342-39.5,3.652-3.793,67.107-61.51,68.335-66.746.153-.655.3-3.1-1.154-4.384s-3.59-.849-5.135-.5q-3.283.746-104.608,69.142-14.845,10.194-26.894,9.934c-8.855-.191-25.888-5.006-38.551-9.123-15.531-5.048-27.875-7.717-26.8-16.291q.84-6.7,18.45-13.7,108.446-47.248,144.628-62.3c68.872-28.647,83.183-33.623,92.511-33.789,2.052-.034,6.639.474,9.61,2.885a10.452,10.452,0,0,1,3.53,6.716A43.765,43.765,0,0,1,362.952,176.66Z"/></svg></a>
      <a href="mailto:a1ex_ma@mail.ru" title="Email"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="currentColor" d="M207.8 20.73c-93.45 18.32-168.7 93.66-187 187.1c-27.64 140.9 68.65 266.2 199.1 285.1c19.01 2.888 36.17-12.26 36.17-31.49l.0001-.6631c0-15.74-11.44-28.88-26.84-31.24c-84.35-12.98-149.2-86.13-149.2-174.2c0-102.9 88.61-185.5 193.4-175.4c91.54 8.869 158.6 91.25 158.6 183.2l0 16.16c0 22.09-17.94 40.05-40 40.05s-40.01-17.96-40.01-40.05v-120.1c0-8.847-7.161-16.02-16.01-16.02l-31.98 .0036c-7.299 0-13.2 4.992-15.12 11.68c-24.85-12.15-54.24-16.38-86.06-5.106c-38.75 13.73-68.12 48.91-73.72 89.64c-9.483 69.01 43.81 128 110.9 128c26.44 0 50.43-9.544 69.59-24.88c24 31.3 65.23 48.69 109.4 37.49C465.2 369.3 496 324.1 495.1 277.2V256.3C495.1 107.1 361.2-9.332 207.8 20.73zM239.1 304.3c-26.47 0-48-21.56-48-48.05s21.53-48.05 48-48.05s48 21.56 48 48.05S266.5 304.3 239.1 304.3z"/></svg></a>
    </div>
  </div>
  <div class="about-card__info">
    <p class="about-card__name">Alex Ma</p>
    <p class="about-card__role">Data Scientist · Data Engineer · Software Developer</p>
    <div class="about-card__meta">
      <span class="about-card__meta-key">Дата рождения</span><span>20.02.2002</span>
      <span class="about-card__meta-key">Город</span><span>Омск</span>
      <span class="about-card__meta-key">Статус занятости</span><span>Открыт к сотрудничеству</span>
      <span class="about-card__meta-key">Ожидаемая з/п</span><span>от 350 000 р. / мес.</span>
    </div>
  </div>
</div>

<div class="about-toggle-bar">
  <button id="about-toggle-btn" class="inline-block !rounded-md bg-primary-600 px-4 py-1 !text-neutral hover:!bg-primary-500 dark:bg-primary-800 dark:hover:!bg-primary-700" onclick="toggleAbout()">Подробнее ↓</button>
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

<div class="about-field">
<span class="about-field-key">Email</span><span><a href="mailto:a1ex_ma@mail.ru">a1ex_ma@mail.ru</a></span>
<span class="about-field-key">Телефон</span><span><details><summary>Показать номер</summary>+7 (XXX) XXX-XX-XX</details></span>
</div>

<div class="full-only"><h3>Мессенджеры</h3></div>

<div class="about-field brief-only">
<span class="about-field-key">Telegram</span><span><a href="https://t.me/a1ex_ma">@a1ex_ma</a></span>
</div>

<div class="about-field full-only">
<span class="about-field-key">Telegram</span><span><a href="https://t.me/a1ex_ma">@a1ex_ma</a> — Предпочтительный способ связи</span>
<span class="about-field-key">MAX</span><span>@a1ex_ma</span>
<span class="about-field-key">WhatsApp</span><span>@a1ex_ma</span>
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

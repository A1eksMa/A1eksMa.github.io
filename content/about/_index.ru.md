---
title: "Обо мне"
description: "Alex Ma — Data Engineer / Analyst"
---

<!-- photo placeholder -->

**Alex Ma**

**Дата рождения:** 20 февраля 2002
**Город:** Омск
**Статус:** Открыт к предложениям

<div style="margin: 1.5rem 0;">
  <button id="about-toggle-btn" onclick="toggleAbout()" style="padding: 0.35rem 1.1rem; cursor: pointer; border-radius: 4px; border: 1px solid currentColor; background: transparent; font-size: 0.9rem; font-family: inherit;">
    Подробнее ↓
  </button>
</div>

---

## Образование

**Омский государственный университет имени Ф.М. Достоевского**
Экономический факультет · Экономическая теория · 2003

<div class="about-full" style="display:none">
<p><strong>Омский государственный технический университет</strong><br>
Факультет транспорта, нефти и газа · Проектирование, сооружение и эксплуатация газонефтепроводов и газонефтехранилищ · 2016</p>
</div>

<div class="about-full" style="display:none">
<hr>
<h2>Дополнительное образование</h2>
<p><strong>Data Analyst</strong> · 2022–2023</p>
<p><strong>Data Driven</strong> · 2025</p>
</div>

<div class="about-full" style="display:none">
<hr>
<h2>Системы контроля версий</h2>
<p><strong>GitHub</strong> · <a href="https://github.com/A1eksMa">A1eksMa</a><br>
Международная платформа. Код, проекты с открытым исходным кодом, портфолио.</p>
<p><strong>GitVerse</strong> · <a href="https://gitverse.ru/a1ex_ma">a1ex_ma</a><br>
Российская платформа контроля версий. Проекты для русскоязычного сообщества.</p>
</div>

<div class="about-full" style="display:none">
<hr>
<h2>Социальные сети</h2>
<p><strong>Discord</strong> · @a1ex_ma<br>
Аудио- и видеосвязь, голосовые чаты, рабочие обсуждения и коллаборации.</p>
<p><strong>ВКонтакте</strong> · <a href="https://vk.com/a1ex_ma">a1ex_ma</a><br>
Когда я не программирую — рисую. Здесь вы найдёте витрину моих работ.</p>
<p><strong>LeetCode</strong> · <a href="https://leetcode.com/u/a1ex_ma">a1ex_ma</a><br>
Практика решения алгоритмических задач. Редко нахожу на это время, но стараюсь не забрасывать.</p>
</div>

---

## Мессенджеры

**Telegram** · [@a1ex_ma](https://t.me/a1ex_ma) — предпочтительный способ связи по рабочим вопросам

<div class="about-full" style="display:none">
<p><strong>MAX</strong> · @a1ex_ma</p>
<p><strong>WhatsApp</strong> · @a1ex_ma</p>
</div>

---

## Связаться со мной

**Email:** [a1ex_ma@mail.ru](mailto:a1ex_ma@mail.ru)

**Телефон:**
<details>
<summary>Показать номер телефона</summary>

+7 (XXX) XXX-XX-XX

</details>

<script>
function toggleAbout() {
  var btn = document.getElementById('about-toggle-btn');
  var expanded = btn.getAttribute('data-expanded') === 'true';
  expanded = !expanded;
  btn.setAttribute('data-expanded', String(expanded));
  document.querySelectorAll('.about-full').forEach(function(el) {
    el.style.display = expanded ? 'block' : 'none';
  });
  btn.textContent = expanded ? 'Кратко ↑' : 'Подробнее ↓';
}
</script>

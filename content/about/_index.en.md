---
title: "About"
description: "Alex Ma — Data Engineer / Analyst"
---

<!-- photo placeholder -->

**Alex Ma**

**Born:** February 20, 2002
**Location:** Omsk, Russia
**Status:** Open to opportunities

<div style="margin: 1.5rem 0;">
  <button id="about-toggle-btn" onclick="toggleAbout()" style="padding: 0.35rem 1.1rem; cursor: pointer; border-radius: 4px; border: 1px solid currentColor; background: transparent; font-size: 0.9rem; font-family: inherit;">
    Full ↓
  </button>
</div>

---

## Education

**Omsk State University named after F.M. Dostoevsky**
Faculty of Economics · Economic Theory · 2003

<div class="about-full" style="display:none">
<p><strong>Omsk State Technical University</strong><br>
Faculty of Transport, Oil and Gas · Pipeline and Storage Design, Construction and Operation · 2016</p>
</div>

<div class="about-full" style="display:none">
<hr>
<h2>Additional Education</h2>
<p><strong>Data Analyst</strong> · 2022–2023</p>
<p><strong>Data Driven</strong> · 2025</p>
</div>

<div class="about-full" style="display:none">
<hr>
<h2>Version Control</h2>
<p><strong>GitHub</strong> · <a href="https://github.com/A1eksMa">A1eksMa</a><br>
International platform. Code, open source projects, portfolio.</p>
<p><strong>GitVerse</strong> · <a href="https://gitverse.ru/a1ex_ma">a1ex_ma</a><br>
Russian version control platform. Projects for the Russian-speaking community.</p>
</div>

<div class="about-full" style="display:none">
<hr>
<h2>Socials</h2>
<p><strong>Discord</strong> · @a1ex_ma<br>
Audio and video communication, voice chats, work discussions and collaboration.</p>
<p><strong>VKontakte</strong> · <a href="https://vk.com/a1ex_ma">a1ex_ma</a><br>
When I'm not coding — I draw. A showcase of my artwork.</p>
<p><strong>LeetCode</strong> · <a href="https://leetcode.com/u/a1ex_ma">a1ex_ma</a><br>
Algorithmic problem solving. Rarely find time for it, but try not to abandon it.</p>
</div>

---

## Messengers

**Telegram** · [@a1ex_ma](https://t.me/a1ex_ma) — preferred contact for work matters

<div class="about-full" style="display:none">
<p><strong>MAX</strong> · @a1ex_ma</p>
<p><strong>WhatsApp</strong> · @a1ex_ma</p>
</div>

---

## Contact Me

**Email:** [a1ex_ma@mail.ru](mailto:a1ex_ma@mail.ru)

**Phone:**
<details>
<summary>Show phone number</summary>

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
  btn.textContent = expanded ? 'Brief ↑' : 'Full ↓';
}
</script>

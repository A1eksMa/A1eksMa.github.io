---
title: "Проекты"
description: "Репозитории, организации и open-source проекты"
layout: "single"
showAuthor: false
---

<style>
/* ───── Headings ───── */
#projects-body h2 {
  background: rgba(var(--color-primary-500), 0.15);
  border-radius: 6px;
  padding: 0.2em 0.6em;
  margin-left: -0.6em;
  color: rgba(var(--color-neutral-800), 1);
}
#projects-body h3 {
  background: rgba(var(--color-primary-400), 0.09);
  border-radius: 5px;
  padding: 0.15em 0.5em;
  margin-left: -0.5em;
  color: rgba(var(--color-neutral-600), 1);
}
.dark #projects-body h2 { color: rgba(var(--color-neutral-100), 1); }
.dark #projects-body h3 { color: rgba(var(--color-neutral-400), 1); }

/* ───── Org grid (2 col = 50%) ───── */
.proj-org-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
  margin: 1rem 0 1.5rem;
}
@media (max-width: 640px) {
  .proj-org-grid { grid-template-columns: 1fr; }
}

/* ───── Org card ───── */
.proj-org-card {
  display: flex;
  align-items: stretch;
  border: 1px solid color-mix(in srgb, currentColor 20%, transparent);
  border-radius: 8px;
  overflow: hidden;
}
.proj-org-card__accent {
  flex-shrink: 0;
  width: 3rem;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(var(--color-primary-600), 0.22);
  font-size: 1.4rem;
  font-weight: 700;
  color: rgba(var(--color-primary-600), 0.8);
}
.proj-org-card__body {
  flex: 1;
  padding: 0.85rem 1rem;
  display: flex;
  flex-direction: column;
  gap: 0.35rem;
}
.proj-org-card__name {
  font-size: 1rem;
  font-weight: 700;
  margin: 0;
}
.proj-org-card__desc {
  font-size: 0.88rem;
  opacity: 0.75;
  margin: 0;
  line-height: 1.5;
}
.proj-org-card__links {
  display: flex;
  gap: 0.75rem;
  font-size: 0.82rem;
  margin-top: 0.25rem;
}
.proj-org-card__links a {
  opacity: 0.7;
  text-decoration: underline;
}
.proj-org-card__links a:hover { opacity: 1; }
.proj-org-card__since {
  font-size: 0.78rem;
  opacity: 0.45;
  margin-top: auto;
  padding-top: 0.25rem;
}

/* ───── Repo grid (~33%) ───── */
.proj-repo-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.85rem;
  margin: 1rem 0 1.5rem;
}
@media (max-width: 900px) {
  .proj-repo-grid { grid-template-columns: repeat(2, 1fr); }
}
@media (max-width: 560px) {
  .proj-repo-grid { grid-template-columns: 1fr; }
}

/* ───── Repo card ───── */
.proj-repo-card {
  border: 1px solid color-mix(in srgb, currentColor 20%, transparent);
  border-radius: 8px;
  padding: 0.85rem 1rem;
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
}
.proj-repo-card__header {
  display: flex;
  align-items: baseline;
  justify-content: space-between;
  gap: 0.5rem;
}
.proj-repo-card__name {
  font-weight: 700;
  font-size: 0.95rem;
  text-decoration: none;
}
.proj-repo-card__name:hover { opacity: 0.7; }
.proj-repo-card__stars {
  font-size: 0.78rem;
  opacity: 0.55;
  white-space: nowrap;
}
.proj-repo-card__desc {
  font-size: 0.83rem;
  opacity: 0.75;
  margin: 0;
  line-height: 1.5;
}
.proj-repo-card__meta {
  font-size: 0.75rem;
  opacity: 0.45;
  margin-top: auto;
  padding-top: 0.2rem;
}

/* ───── Tags ───── */
.proj-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.3rem;
}
.proj-tag {
  font-size: 0.73rem;
  padding: 0.1em 0.5em;
  border-radius: 999px;
  background: rgba(var(--color-neutral-500), 0.12);
}
.proj-tag--lang {
  background: rgba(var(--color-primary-500), 0.15);
  font-weight: 500;
}
</style>

<div id="projects-body">

## Организации

<div class="proj-org-grid">

<div class="proj-org-card">
  <div class="proj-org-card__accent">S</div>
  <div class="proj-org-card__body">
    <p class="proj-org-card__name">SigilGate</p>
    <p class="proj-org-card__desc">Частная сетевая инфраструктура, устойчивая к DPI и блокировкам.</p>
    <div class="proj-org-card__links">
      <a href="https://sigilgate.github.io" target="_blank" rel="noopener">Сайт</a>
      <a href="https://github.com/sigilgate" target="_blank" rel="noopener">GitHub</a>
      <a href="/projects/orgs/sigilgate/">Репозитории →</a>
    </div>
    <span class="proj-org-card__since">с февраля 2026</span>
  </div>
</div>

<div class="proj-org-card">
  <div class="proj-org-card__accent">I</div>
  <div class="proj-org-card__body">
    <p class="proj-org-card__name">info-tech-io</p>
    <p class="proj-org-card__desc">Образовательная платформа INFOTEKA — интерактивные курсы по Linux и IT.</p>
    <div class="proj-org-card__links">
      <a href="https://info-tech-io.github.io" target="_blank" rel="noopener">Сайт</a>
      <a href="https://github.com/info-tech-io" target="_blank" rel="noopener">GitHub</a>
      <a href="/projects/orgs/info-tech-io/">Репозитории →</a>
    </div>
    <span class="proj-org-card__since">с 2025</span>
  </div>
</div>

</div>

## Проекты

<div class="proj-repo-grid">
{{< repo-card owner="A1eksMa" repo="nier" >}}
</div>

</div>

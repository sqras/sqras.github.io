---
layout: home
title: Головна
---

# Вітаю! Я Тарас — SEO спеціаліст та розробник.

Я займаюсь просуванням сайтів та автоматизацією процесів. Мій підхід базується на конкретиці: від глибокого технічного аудиту до створення інструментів, що полегшують життя бізнесу.

---

### 🚀 Мої проєкти та розробки
*   **Goodreeds** — музичний сервіс із системою збору лірики через Telegram та Viber ботів.
*   **Автоматизація SEO** — впровадження семантичного аналізу та технік на базі embeddings.
*   **Workflow Automation** — побудова складних сценаріїв у n8n для інтеграції різних сервісів.

---

### 📩 Зв'язатися зі мною
Маєте запитання щодо SEO-аудиту чи розробки бота? Напишіть мені прямо тут:

<form id="contact-form" style="display: flex; flex-direction: column; gap: 10px; max-width: 400px;">
  <input type="email" id="email" placeholder="Ваш Email" required style="padding: 8px; border: 1px solid #ccc; border-radius: 4px;">
  <textarea id="message" placeholder="Ваше повідомлення" rows="5" required style="padding: 8px; border: 1px solid #ccc; border-radius: 4px; font-family: sans-serif;"></textarea>
  <button type="submit" style="padding: 10px; background-color: #2ea44f; color: white; border: none; border-radius: 4px; cursor: pointer;">Надіслати заявку</button>
</form>

<div id="form-status" style="margin-top: 10px; display: none;"></div>

<script>
  const form = document.getElementById('contact-form');
  const status = document.getElementById('form-status');

  form.addEventListener('submit', async (e) => {
    e.preventDefault();
    status.style.display = 'block';
    status.innerText = 'Надсилаю...';
    
    const data = {
      email: document.getElementById('email').value,
      message: document.getElementById('message').value,
      source: 'GitHub Pages Portfolio'
    };
    
    try {
      // Замініть посилання нижче на ваш реальний Webhook URL в n8n
      const response = await fetch('https://ВАШ_N8N_DOMAIN/webhook/contact', {
        method: 'POST',
        body: JSON.stringify(data),
        headers: { 'Content-Type': 'application/json' }
      });
      
      if (response.ok) {
        status.innerText = '✅ Повідомлення відправлено! Я відповім найближчим часом.';
        form.reset();
      } else {
        throw new Error();
      }
    } catch (err) {
      status.innerText = '❌ Помилка. Спробуйте пізніше або напишіть мені в Telegram.';
      status.style.color = 'red';
    }
  });
</script>

---

### 🛠 Технічна документація
Для модераторів та рекламних мереж:
*   [app-ads.txt](/app-ads.txt) — Авторизація цифрових оголошень.
*   [Privacy Policy](/privacy-policy) — Політика конфіденційності для мобільних застосунків.

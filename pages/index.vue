<template>
  <div class="page home-page">
    <header>
      <div class="container-fluid">
        <h2 class="mb-0">Сервисная страница</h2>
        <p>
          Программное обеспечение на основе языковой модели нейросети — это
          продвинутый инструмент искусственного интеллекта, предназначенный для
          общения с пользователями в текстовом формате. Эта система обучается на
          обширном массиве текстовых данных, что позволяет ей понимать запросы
          на разных языках и генерировать осмысленные ответы. Программа способна
          выполнять широкий спектр задач, включая предоставление информации,
          ведение бесед, помощь в обучении и поддержку пользователя.
        </p>
        <!-- <button class="btn btn-dark">Присоединиться</button> -->
      </div>
    </header>

    <main>
      <section id="advantages">
        <div class="container-fluid">
          <h4>Некоторые возможности</h4>
        </div>
        <div class="advantages-content">
          <div class="custom-card">
            <h6 class="card-heading mb-2">Напишите программу тренировок</h6>
            <p class="small mb-2">
              Преобразуйте общение с вашим чат-ботом в персонализированное
              <b>тренировочное решение!</b>
            </p>
            <nuxt-img src="/1.png" width="300" />
            <!-- <button class="btn btn-dark btn-sm my-2">Добавить переводы</button> -->
          </div>
          <div class="custom-card">
            <h6 class="card-heading mb-2">Получайте четкие инструкции</h6>
            <p class="small mb-2">
              Наш чат-бот предоставляет четкие и структурированные инструкции для каждого запроса
            </p>
            <nuxt-img src="/2.png" width="300" />
            <!-- <button class="btn btn-dark btn-sm my-2">Добавить материалы</button> -->
          </div>
          <div class="custom-card">
            <h6 class="card-heading mb-2">Уроки английского</h6>
            <p class="small mb-2">
              Пользователи смогут учить новые слова и фразы
              <b>прямо в диалоге.</b>
            </p>
            <nuxt-img src="/3.png" width="300" />
            <!-- <button class="btn btn-dark btn-sm my-2">Добавить материалы</button> -->
          </div>
        </div>
      </section>

      <section id="doc-install">
        <div class="container-fluid">
          <h3>Руководство по установке и развертыванию ПО</h3>
          <ul>
            <li>
              <a
                href="javascript:void(0)"
                style="text-decoration: underline !important"
                >Загрузите приложение</a
              >
            </li>
            <li>
              Откройте загруженное приложение <b>electron-app-win-32-x64.exe</b>
            </li>
            <li>Укажите директорию установки</li>
            <li>Откройте установленное приложение</li>
          </ul>
        </div>
      </section>

      <section id="instruct">
        <div class="container-fluid">
          <h3>Инструкция пользователя</h3>
          <ul>
            <li>Начните диалог, введя приветственное сообщение или вопрос.</li>
          </ul>
        </div>
      </section>

      <section id="char">
        <div class="container-fluid">
          <h3>Описание функциональных характеристик</h3>
          <div class="advantages-content">
            <div class="custom-card">
              <h6 class="card-heading mb-2">Интерактивное общение</h6>
              <p class="small mb-2">
                Чат-бот обеспечивает непрерывное и эффективное взаимодействие с
                пользователями, обрабатывая запросы в реальном времени и
                предоставляя мгновенные ответы.
              </p>
              <!-- <button class="btn btn-dark btn-sm my-2">Добавить переводы</button> -->
            </div>
            <div class="custom-card">
              <h6 class="card-heading mb-2">Персонализация</h6>
              <p class="small mb-2">
                Благодаря анализу предыдущих взаимодействий, бот адаптирует свои
                ответы под индивидуальные предпочтения и нужды каждого
                пользователя
              </p>
              <!-- <button class="btn btn-dark btn-sm my-2">Добавить материалы</button> -->
            </div>
            <div class="custom-card">
              <h6 class="card-heading mb-2">Изучение языка</h6>
              <p class="small mb-2">
                Встроенные модули для обучения английскому языку помогают
                пользователям улучшать свои языковые навыки, предлагая
                разнообразные упражнения и практические задания.
              </p>
              <!-- <button class="btn btn-dark btn-sm my-2">Добавить материалы</button> -->
            </div>
          </div>

          <div class="tech-char">
            <h5>Платформы поддержки: &nbsp;&nbsp;<code>win 10/11</code></h5>
            <h5>
              Требования к системе: &nbsp;&nbsp;<code
                >минимальные требования включают 1 ГБ оперативной памяти, 400 МБ
                свободного пространства</code
              >
            </h5>
            <h5>Используемые технологии:</h5>
            <ul>
              <li>
                Разработан на базе последней версии фреймворка для
                искусственного интеллекта.
              </li>
              <li>
                Использует технологии машинного обучения для адаптации и
                персонализации ответов.
              </li>
            </ul>
            <h5>Безопасность</h5>
            <ul>
              <li>
                Защищен с помощью современных методов шифрования и соответствует
                международным стандартам безопасности данных.
              </li>
              <li>
                Регулярные обновления безопасности для защиты пользовательских
                данных.
              </li>
            </ul>
            <h5>Масштабируемость</h5>
            <ul>
              <li>
                Спроектирован для обеспечения стабильной работы при увеличении
                числа пользователей и объема запросов.
              </li>
              <li>
                Поддерживает горизонтальное и вертикальное масштабирование.
              </li>
            </ul>
          </div>
        </div>
      </section>

      <section id="pricing">
        <div class="container-fluid">
          <h3>Тариф</h3>
          <p>Подписка на месяц: <b>20 000 руб</b></p>
        </div>
      </section>

      <section id="info">
        <div class="container-fluid">
          <h3>Информация о разработчике</h3>
          <p>
            Автоматизированная Система Искусственного Интеллекта (АСИИ). Данные
            о разработчике ПО: ООО Технолоджи, ИНН 5406820684
          </p>
          <button class="btn btn-primary" @click="downloadExe">
            <i class="bi bi-download"></i> &nbsp;Скачать тестовую версию
          </button>
        </div>
      </section>
    </main>
  </div>
</template>

<style lang="scss" scoped>
header {
  padding: 50px 0;
}
#doc-install {
  margin: 3rem 0;
}
#char {
  margin: 3rem 0;
  .advantages-content {
    margin-bottom: 1rem;
  }
}
#info {
  margin: 3rem 0;
}
#pricing {
  margin: 3rem 0;
}
img {
  margin-top: 15px;
  border-radius: 5px;
  display: block;
  box-shadow: 0 0 15px 0 #333;
}

.advantages-content {
  padding: 1rem;
  background: var(--custom-wrapper-background-color);
  width: fit-content;
  border-radius: 5px;
  display: flex;
  gap: 1rem;
  .custom-card {
    padding: 1rem;
    min-height: 150px;
    border-radius: 8px;
    background: var(--custom-wrapper-inner-background-color);
    width: 350px;
  }
}

@media screen and (max-width: 1200px) {
  .advantages-content {
    .custom-card {
      width: 30%;
    }
  }
}

@media screen and (max-width: 768px) {
  .advantages-content {
    flex-wrap: wrap;
    .custom-card {
      width: 350px;
    }
  }
}
// footer {
//   padding: 30px 0;
//   background-color: #111;
//   color: #fff;
//   min-height: 400px;
// }
</style>

<script setup lang="ts">
const downloadExe = () => {
  // Замените URL ниже на актуальный путь к вашему .exe файлу
  const exeUrl = "https://disk.yandex.ru/d/oTvLKcnrGJydgg";
  const link = document.createElement("a");
  link.href = exeUrl;
  link.download = "your_application.exe";
  link.click();
};
</script>

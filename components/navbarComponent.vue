<template>
  <nav :class="{ expanded: navbarIsExpanded }">
    <!-- Logotype -->
    <div class="logotype">
      <h4 class="title">
        <NuxtLink to="/">АСИИ</NuxtLink>
      </h4>
      <div class="description">
        <p>Автоматизированная система искусственного интеллекта</p>
      </div>
    </div>

    <!-- Right Side Menu -->
    <div class="menu-wrapper">
      <div class="menu-content">
        <div class="theme-switcher">
          <button
            class="btn btn-sm"
            :class="{ active: themeStore.isLightTheme }"
            @click="setTheme('light')"
          >
            <i class="bi bi-sun"></i>
          </button>
          <button
            class="btn btn-sm"
            :class="{ active: !themeStore.isLightTheme }"
            @click="setTheme('dark')"
          >
            <i class="bi bi-moon"></i>
          </button>
        </div>
        <ul class="menu">
          <li>
            <a href="#advantages" to="/">Возможности</a>
          </li>
          <li>
            <a href="#doc-install" to="/">Руководство</a>
          </li>
          <li>
            <a href="#instruct" to="/">Инструкция</a>
          </li>
          <li>
            <a href="#char" to="/">Характеристики</a>
          </li>
          <li>
            <a href="#pricing" to="/">Цена</a>
          </li>
          <li>
            <a href="#info" to="/">О нас</a>
          </li>
          <!-- <li>
        <NuxtLink to="/dialogs">Диалоги</NuxtLink>
      </li> -->
        </ul>
        <div class="userdata" v-if="token">

        </div>
        <div v-else class="my-auto auth">
          <button class="btn btn-primary" @click="downloadExe"><i class="bi bi-download"></i> &nbsp; Тестовая версия</button>
        </div>
        <div class="logout">
          <p><a href="javascript:void(0)"><i class="bi bi-box-arrow-left"></i> <span>Выйти</span></a></p>
          <button @click="themeStore.closeNavbar()" class="btn btn-sm btn-dark" style="display: flex; padding: 3px 12px; border-radius: 5px; font-size: 14px;"><i class="bi bi-x-square" style="margin-right: 5px; margin-top: 1px;"></i> <span>Закрыть</span></button>
        </div>
      </div>
      <button class="btn btn-dark menu-toggler" @click="themeStore.openNavbar()">Меню</button>
    </div>
  </nav>
</template>

<script lang="ts" setup>
import { useUserStore } from "@/stores/userStore";
import { useThemeStore } from "@/stores/themeStore"; // Импортируем наше новое хранилище

const userStore = useUserStore();
const themeStore = useThemeStore(); // Используем хранилище темы
const { navbarIsExpanded } = storeToRefs(themeStore);
const token = ref(useCookie("token").value);
const downloadExe = () => {
  // Замените URL ниже на актуальный путь к вашему .exe файлу
  const exeUrl = "https://disk.yandex.ru/d/oTvLKcnrGJydgg";
  const link = document.createElement("a");
  link.href = exeUrl;
  link.download = "your_application.exe";
  link.click();
};
onMounted(() => {
  userStore.fetchUser();
});

const user = computed(() => userStore.user); // Реактивное свойство для доступа к пользователю

// Функция для смены темы через хранилище
const setTheme = (theme: string) => {
  themeStore.setTheme(theme);
};

const closeNavbar = async () => {
  themeStore.closeNavbar()
}
</script>

<style lang="scss" scoped>
.menu-toggler {
  display: none;
}
.logotype {
  h4,
  p {
    margin-bottom: 0;
  }
}
.logout {
  display: none;
  margin: 1rem auto 2rem 3.5rem;
  a {
    display: flex;
    width: fit-content;
    padding: 5px 15px;
    background-color: #111;
    color: #eee;
    border-radius: 5px;
    i {
      display: block;
      margin-right: 5px;
    }
  }
}
.menu-wrapper {
  display: flex;
  margin: auto 0 auto auto;
  position: relative;
}
.menu-content {
  display: flex;
  margin: auto 0 auto auto;
  position: relative;
}

.auth {
  // margin-left: 3.5rem;
  margin-left: 1rem;
  margin-top: 1rem !important;
  margin-bottom: 1rem !important;
}
.theme-switcher {
  margin: auto 0 auto auto;
  background-color: var(--notify-background-color);
  display: flex;
  border-radius: 1rem;
  transition: 400ms;
}
.btn-sm {
  border-radius: 1rem;
  font-size: 12px;
  padding: 2px 5px;
  display: block;
  margin: auto 0;
  border: 0;
  transition: 400ms;
  &.active {
    background-color: var(--bs-body-color);
    color: var(--body-background-color);
  }
}
nav {
  display: flex;
  margin-bottom: 1rem;
  ul {
    margin: auto 0 auto 1rem;
    padding: 0;
    list-style-type: none;
    li {
      a {
        text-decoration: none;
      }
    }
  }
}

.userdata {
  margin: auto 15px;
  h6 {
    margin: 0;
  }
}

.menu {
  display: flex;
  li {
    margin: 0 0.5rem;
  }
}

.to-dashboard {
  text-decoration: none;
}
@media screen and (max-width: 768px) {
  .menu-toggler {
    display: block;
  }
  .menu-wrapper {
    position: inherit;
  }
  .menu-content {
    position: absolute;
    background-color: var(--menu-content-background-color);
    padding: 1rem;
    font-size: 1.5rem;
    top: 0;
    left: 0;
    flex-direction: column;
    width: 100%;
    min-height: 100vh;
    // background-color: #ccc;
    transition: 400ms;
    left: -100%;
    .menu {
      flex-direction: column;
    }
  }

  .expanded {
    .menu-content {
      left: 0;
    }
  }

  .btn-sm {
    padding: 2px 7px;
    font-size: 1.5rem;
    border-radius: 5rem;
  }
  .theme-switcher {
    margin: 3rem auto 0;
    border-radius: 5rem;
  }
  .userdata {
    margin: 2rem 3.5rem auto;
    h6 {
      margin: 0;
      font-size: 24px;
    }
  }
  nav {
    ul {
      margin: 3rem 0 0 3rem;
      li {
        a {
          text-decoration: none;
          font-size: 24px;
          display: block;
          margin: 5px 0;
          transition: 400ms;
          position: relative;
          left: 0;
          &:hover {
            left: 5px;
          }
        }
      }
    }
  }
  .auth {
    margin-left: 3.5rem;
  }
  .logout {
    display: block;
  }
}
</style>

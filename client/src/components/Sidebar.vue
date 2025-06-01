<template>
  <section class="sidebar">
    <div class="logo">
      <img src="@/public/sidebar/logo.svg" alt="Trello Clone">

      <h1>Trello Clone</h1>
    </div>

    <div class="bottom-side">
      <ul class="options">
        <li
            class="option"
            v-for="(option, index) in options"
            :key="index"
        >
          <a :href="option.link">
            <img :src="option.img" :alt="option.title">

            <h2>{{ option.title }}</h2>
          </a>
        </li>
      </ul>

      <div class="auth">
        <a
            v-if="isAuth"
            href="/logout"
        >
          <img src="@/public/sidebar/logout.svg" alt="logout">

          <h2>Log out</h2>
        </a>

        <a
            v-else
            href="/login"
        >
          <img src="@/public/sidebar/login.svg" alt="login">

          <h2>Log In</h2>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
import dashboard from '@/public/sidebar/dashboard.svg';
import board from '@/public/sidebar/board.svg';
import analytics from '@/public/sidebar/analytics.svg';
import settings from '@/public/sidebar/settings.svg';

export default {
  data() {
    return {
      isAuth: true,
      options: [
        {
          link: 'dashboard',
          img: dashboard,
          title: 'Dashboard'
        },
        {
          link: 'board',
          img: board,
          title: 'Board'
        },
        {
          link: 'analytics',
          img: analytics,
          title: 'Analytics'
        },
        {
          link: 'settings',
          img: settings,
          title: 'Settings'
        },
      ]
    }
  }
}
</script>

<style scoped>
.sidebar {
  height: 100vh;
  width: 100%;
  max-width: 225px;
  box-shadow: 7px 0 10px rgba(0, 0, 0, 0.1);

  display: flex;
  flex-direction: column;

  .logo {
    margin: 0 auto;
    display: flex;
    padding-top: 32px;
    padding-bottom: 32px;
    gap: 10px;

    h1 {
      font-family: Poppins, sans-serif;
      font-size: 16px;
      font-weight: bold;
    }
  }

  .bottom-side {
    padding-top: 32px;
    padding-bottom: 84px;
    height: 100%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .options {
    list-style: none;
    display: flex;
    flex-direction: column;
    margin: 0 auto;
    gap: 37px;

    .option {
      a {
        display: flex;
        gap: 16px;
        text-decoration: none;

        h2 {
          font-family: Poppins, sans-serif;
          font-weight: 600;
          font-size: 16px;
          color: #707070;
        }
      }
    }
  }

  .auth {
    a {
      display: flex;
      gap: 20px;
      text-decoration: none;
    }

    h2 {
      font-family: Poppins, sans-serif;
      font-weight: 600;
      font-size: 16px;
      color: #000000;
    }
  }
}
</style>
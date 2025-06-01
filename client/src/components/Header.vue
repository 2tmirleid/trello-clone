<template>
  <header>
    <div class="search">
      <button type="submit">
        <img src="@/public/header/loupe.svg" alt="search">
      </button>

      <input type="text" placeholder="Search">
    </div>

    <div class="personal">
      <a
          class="notifications"
          href="#"
      >
        <img
            v-if="!notifications"
            src="@/public/header/notifications.svg"
            alt="notifications"
        >

        <img
            v-else
            src="@/public/header/notifications_alert.svg"
            alt="notifications"
        >
      </a>

      <a
          class="help"
          href="#"
      >
        <img src="@/public/header/help.svg" alt="help">
      </a>

      <a
          v-if="isAuth"
          class="account"
          href="#"
      >
        <img src="@/public/header/user.svg" alt="account">
      </a>

      <a
          v-else
          class="account"
          href="#"
      >
        <img src="@/public/header/default_user.svg" alt="account">
      </a>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      notifications: false,
      isAuth: false,
    }
  },
  methods: {

  }
}
</script>

<style scoped>
header {
  max-width: 1220px;
  height: 90px;
  width: 100%;
  margin: 0 auto;

  display: flex;
  justify-content: space-between;
  align-items: center;
  align-content: center;

  padding-right: 56px;
  padding-left: 35px;

  .search {
    display: flex;
    justify-content: center;
    align-content: center;
    align-items: center;
    gap: 16px;

    button {
      background: none;
      border: none;
      cursor: pointer;
    }

    input {
      height: 25px;
      border: none;
      outline: none;
      background-color: #FFFFFF;

      font-family: Poppins, sans-serif;
      font-size: 16px;
      color: #707070;
    }
  }

  .personal {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 38px;

    .account {
      img {
        width: 32px;
        height: 32px;
      }
    }
  }
}
</style>